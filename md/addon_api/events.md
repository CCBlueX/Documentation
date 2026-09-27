## Events

The client raises events for what happens in the game, and event listeners react to them. Modules, modes, toggleable groups, HUD components and the add-on itself are listeners, so they can declare handlers directly.

### When handlers run

A handler runs only while its listener's `running` is true:

| Listener                   | Running while                                                         |
|----------------------------|-----------------------------------------------------------------------|
| `ClientModule`             | the module is enabled and the player is in a world                     |
| `Mode`                     | it is the selected mode and its parent is running                     |
| `ToggleableValueGroup`     | it is enabled and its parent is running                               |
| HUD component              | it is enabled and the HUD module is running                           |
| `LiquidBounceAddon`        | the add-on's state is `LOADED`                                        |
| any other `EventListener`  | always, unless `running` is overridden                                |

Handlers are registered once and stay registered. They are skipped while their listener is not running, they are not added and removed on every toggle.

### Handlers

```kotlin
object ModuleNoSwear : ClientModule("NoSwear", ModuleCategories.MISC) {

    private val word by text("Word", "heck")

    @Suppress("unused")
    private val chatHandler = handler<ChatSendEvent> { event ->
        if (event.message.contains(word, ignoreCase = true)) {
            event.cancelEvent()
        }
    }

}
```

`handler<T>` registers the handler when the property is initialized. `@Suppress("unused")` silences the warning that the property is never read.

Events that extend `CancellableEvent` can be cancelled with `cancelEvent()`, which usually stops what the event announced: the chat message is not sent, the packet is dropped, the jump does not happen. `isCancelled` tells whether an earlier handler cancelled it.

Handlers run on the thread that raises the event. That is the render thread for most events, `PacketEvent` can arrive on the network thread.

### Priority

Handlers with a higher priority run first, the default is 0. `EventPriorityConvention` names the values the client uses:

| Constant                         | Value  |
|----------------------------------|--------|
| `FIRST_PRIORITY`                 | 1000   |
| `CRITICAL_MODIFICATION`          | 500    |
| `MODEL_STATE`                    | -10    |
| `SAFETY_FEATURE`                 | -50    |
| `OBJECTION_AGAINST_EVERYTHING`   | -100   |
| `FINAL_DECISION`                 | -500   |
| `READ_FINAL_STATE`               | -1000  |

```kotlin
@Suppress("unused")
private val packetHandler = handler<PacketEvent>(priority = EventPriorityConvention.FIRST_PRIORITY) { event ->
    if (event.origin == TransferOrigin.INCOMING && event.packet is ClientboundSetTimePacket) {
        event.cancelEvent()
    }
}
```

### Sequences

A sequence is a handler that can wait. `tickHandler` runs its block on every tick, but not again until the previous run has finished, so waiting inside it spaces the runs out:

```kotlin
object ModuleReminder : ClientModule("Reminder", ModuleCategories.MISC) {

    private val interval by int("Interval", 1200, 20..12000, "ticks")

    @Suppress("unused")
    private val tickHandler = tickHandler {
        waitTicks(interval)
        chat("Drink some water.")
    }

}
```

`sequenceHandler<T>` starts a sequence for every event of type `T`, each running on its own:

```kotlin
@Suppress("unused")
private val attackHandler = sequenceHandler<AttackEntityEvent> { event ->
    val target = event.entity
    val ticks = tickUntil { !target.isAlive || it >= 40 }
    if (!target.isAlive) {
        chat("Took ${target.name.string} down in $ticks ticks.")
    }
}
```

Handling the event itself is over once the sequence first waits, so cancelling or changing the event only works before that.

| Function               | Waits                                                                            |
|------------------------|----------------------------------------------------------------------------------|
| `waitTicks(ticks)`     | the given number of ticks                                                        |
| `waitSeconds(seconds)` | `seconds * 20` ticks                                                             |
| `tickUntil { ticks -> done }` | until the condition is true, checked once per tick; returns the ticks waited |
| `waitMatches<T> { event -> matches }` | until an event of type `T` matches, and returns it                  |

`waitTicks`, `waitSeconds` and `tickUntil` resume on the render thread, `waitMatches` on the thread that raised the matching event. When the listener stops running, for example because the module was disabled, its sequences are cancelled at their next wait.

### Without Kotlin

`handler`, `tickHandler` and `sequenceHandler` are Kotlin extensions. Every listener also has plain methods, which work from Java and Kotlin alike and return an `AutoCloseable` that unregisters again:

| Method                                    | Description                                                                              |
|-------------------------------------------|------------------------------------------------------------------------------------------|
| `on(type, handler)`                       | Calls `handler` for every event of `type` while the listener is running.                 |
| `on(type, priority, handler)`             | The same with a priority.                                                                |
| `onTick(task)`                            | Runs `task` on every tick while the listener is running.                                 |
| `after(ticks, task)`                      | Runs `task` once, `ticks` ticks from now.                                                |
| `every(ticks, task)`                      | Runs `task` every `ticks` ticks, the first time after `ticks`.                           |

`after` and `every` start counting right away and are cancelled for good as soon as the listener is not running. Call them while it runs, for example from a handler, not from a constructor. See [Using Java](/docs/add-on-api/developers/using-java).

### Listeners of your own

Anything can implement `EventListener`. Handlers of a plain listener run as long as the client does, so register it with `registerListeners` to have it unregistered when the add-on fails:

```kotlin
object ChatLogger : EventListener {

    @Suppress("unused")
    private val chatHandler = handler<ChatReceiveEvent> { event ->
        println(event.message)
    }

}
```

Override `running` to pause it, `parent()` to tie it to another listener, and call `unregister()` to remove its handlers for good.

### Events of your own

Subclass `Event`, or `CancellableEvent`, and raise it with `EventManager.callEvent`. It returns the event after every handler ran.

```kotlin
class GreetingEvent(val name: String) : Event()

fun greet(name: String) {
    EventManager.callEvent(GreetingEvent(name))
}
```

### Stable events

These events are part of the [stable API](/docs/add-on-api/developers/stable-api). The client raises many more, see the [event classes](https://github.com/CCBlueX/LiquidBounce/tree/nextgen/src/main/kotlin/net/ccbluex/liquidbounce/event/events), but those may change between releases.

| Event                            | Raised                                                                                                  |
|----------------------------------|---------------------------------------------------------------------------------------------------------|
| `GameTickEvent`                  | On every client tick, at its start.                                                                     |
| `PlayerTickEvent`                | Before the local player ticks. Cancel to skip the tick.                                                 |
| `PlayerPostTickEvent`            | After the local player ticked.                                                                          |
| `PlayerNetworkMovementTickEvent` | When the player's position is sent, `PRE` before and `POST` after. In `PRE`, `x`, `y`, `z` and `ground` change what is sent, cancelling sends nothing. |
| `PlayerMoveEvent`                | When the local player moves. `movement` can be changed.                                                 |
| `PlayerJumpEvent`                | When the local player jumps. `motion` and `yaw` can be changed, cancel to not jump.                     |
| `MovementInputEvent`             | When the movement keys are read. `directionalInput`, `jump` and `sneak` can be changed.                 |
| `AttackEntityEvent`              | Before the player attacks an entity. Cancel to not attack.                                              |
| `TagEntityEvent`                 | When the client decides how to treat an entity: `dontTarget()`, `ignore()`, `assumeFriend()`, `color(...)`. |
| `PacketEvent`                    | For every packet, `OUTGOING` or `INCOMING`. Cancel to drop it.                                          |
| `ChatSendEvent`                  | When the player sends a chat message. Cancel to not send it.                                            |
| `ChatReceiveEvent`               | When a chat or game message arrives. Cancel to hide it.                                                 |
| `ScreenEvent`                    | When a screen is opened, with `null` when screens are closed. Cancel to keep the current one.           |
| `KeyboardKeyEvent`               | When a key is pressed, repeated or released.                                                            |
| `MouseButtonEvent`               | When a mouse button is pressed or released.                                                             |
| `OverlayRenderEvent`             | While the HUD is drawn, see [Rendering](/docs/add-on-api/developers/rendering).                                    |
| `WorldRenderEvent`               | While the world is drawn, see [Rendering](/docs/add-on-api/developers/rendering).                                  |
| `WorldChangeEvent`               | When the client's world changes, with `null` when leaving it.                                           |
| `ChunkLoadEvent`                 | When the server sends a chunk, with its chunk coordinates.                                              |
| `BlockChangeEvent`               | When a block in the client's world changes.                                                             |
| `WorldEntityRemoveEvent`         | When an entity is removed from the client's world, with the reason.                                     |
| `DisconnectEvent`                | When the player leaves a server or world.                                                               |
| `ModuleToggleEvent`              | When a module is enabled or disabled.                                                                   |
| `RefreshArrayListEvent`          | Raise it to make the HUD's module list read names and tags again.                                       |
| `FriendChangeEvent`              | When a friend is added or removed.                                                                      |
| `NotificationEvent`              | When a notification is shown.                                                                           |
