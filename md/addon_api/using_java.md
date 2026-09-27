## Using Java

Everything in the add-on API works from Java, and Kotlin and Java can be mixed in one add-on: [Extras](https://github.com/CCBlueX/LiquidBounce-Addon-Extras) has half of its modules in each. The classes add-ons build on offer Java-friendly signatures; this page lists where Java code looks different from the Kotlin examples in the other pages.

### Entrypoint

```java
public class ExampleAddon extends LiquidBounceAddon {

    @Override
    public List<ModuleCategory> getCategories() {
        return List.of(ExampleCategories.EXAMPLE);
    }

    @Override
    public void onInitialize() {
        registerModules(new ModuleLowHealth(), new ModuleBedrockFinder());
        registerCommand(new CommandHello());
    }

    @Override
    public void onStarted() {
        getLogger().info("{} {} started", getId(), getVersion());
    }

}
```

A Java module is a class, instantiated once and passed to `registerModules`. Kotlin properties become getters: `getId()`, `getLogger()`, `getPlayer()`, `getWorld()`, `getMc()`, `getNetwork()`, `getInGame()`.

### Settings

Settings are fields holding the `Value`, read with `get()` and changed with `set(value)`. `boolean`, `int` and `float` are Java keywords, so these three builders are called differently, and take `min, max` instead of a range:

| Kotlin                                   | Java                                         |
|------------------------------------------|----------------------------------------------|
| `boolean("Respawn", true)`               | `bool("Respawn", true)`                      |
| `int("Delay", 20, 0..100, "ticks")`      | `integer("Delay", 20, 0, 100, "ticks")`      |
| `float("Threshold", 6f, 1f..20f, "HP")`  | `floating("Threshold", 6f, 1f, 20f, "HP")`   |
| `enumChoice("Output", Output.CHAT)`      | `enumChoice("Output", Output.CHAT)`          |
| `multiEnumChoice("Outputs", Output.CHAT)`| `multiEnumChoice("Outputs", Output.class, EnumSet.of(Output.CHAT))` |

Most other builders are called the same, see [Settings](/docs/add-on-api/settings). Enums used for choices implement `Tagged`, whose `getTag()` is the name shown in the ClickGUI.

### Events

Handlers are registered in the constructor with `on`, `onTick` is a handler for every tick. `after` and `every` schedule a task instead of a `tickHandler` with `waitTicks`; call them while the module runs, for example from a handler, since they are cancelled for good once it stops. See [Events](/docs/add-on-api/events).

```java
public class ModuleLowHealth extends ClientModule {

    enum Output implements Tagged {
        CHAT("Chat"),
        NOTIFICATION("Notification"),
        SOUND("Sound");

        private final String tag;

        Output(String tag) {
            this.tag = tag;
        }

        @Override
        public String getTag() {
            return tag;
        }
    }

    private final Value<Float> threshold = floating("Threshold", 6f, 1f, 20f, "HP");
    private final MultiChoiceListValue<Output> outputs = multiEnumChoice("Outputs", Output.class, EnumSet.of(Output.CHAT));
    private final Value<Boolean> respawn = bool("Respawn", true);
    private final Value<Integer> delay = integer("Delay", 20, 0, 100, "ticks");

    private boolean warned;
    private boolean respawning;

    public ModuleLowHealth() {
        super("LowHealth", ModuleCategories.PLAYER);
        literalDescription(() -> "Warns you at low health and respawns you after death.");

        onTick(this::check);
        on(ScreenEvent.class, this::onScreen);
    }

    private void check() {
        boolean low = getPlayer().getHealth() < threshold.get();
        if (low && !warned) {
            if (outputs.get().contains(Output.CHAT)) {
                ClientChat.chat("Low health!", this);
            }
            if (outputs.get().contains(Output.NOTIFICATION)) {
                ClientChat.notification("LowHealth", "Low health!", NotificationEvent.Severity.ERROR);
            }
        }
        warned = low;
    }

    private void onScreen(ScreenEvent event) {
        if (respawn.get() && event.getScreen() instanceof DeathScreen && !respawning) {
            respawning = true;
            after(delay.get(), () -> {
                respawning = false;
                getPlayer().respawn();
            });
        }
    }

    @Override
    public void onDisabled() {
        warned = false;
        respawning = false;
    }

}
```

`literalDescription` gives a module without a [translation](/docs/add-on-api/translations) its description; without either, the client logs a missing description key.

### Modes

Modes are inner classes extending `Mode`, which return their group from `getParent()`. `choices` selects the first one by default:

```java
private final ModeValueGroup<Style> style = choices("Style", new Plain(), new Boxed());

abstract class Style extends Mode {
    Style(String name) {
        super(name);
    }

    @Override
    public ModeValueGroup<?> getParent() {
        return style;
    }
}
```

`ModuleSpeedometer` in Extras shows the whole module.

### Kotlin functions

Top-level Kotlin functions and extensions are static methods of a class named after their file, with the receiver as first argument:

| Kotlin                                           | Java                                                          |
|--------------------------------------------------|---------------------------------------------------------------|
| `chat("Hello")`, `regular(...)`, `variable(...)` | `ClientChat.chat("Hello")`, `ClientChat.regular(...)`, `ClientChat.variable(...)` |
| `translation("key")`                             | `LanguageKt.translation("key")`                               |
| `pos.state`                                      | `BlockExtensionsKt.getState(pos)`                             |
| `attackEntity(entity, SwingMode.DO_NOT_HIDE)`     | `CombatExtensionsKt.attackEntity(entity, SwingMode.DO_NOT_HIDE)` |
| `context.drawQuad(...)`                          | `Render2DKt.drawQuad(context, ...)`                            |
| `drawBox(FULL_BOX, ...)`                         | `RenderShortcutsKt.drawBox(environment, RenderShortcutsKt.FULL_BOX, ...)` |
| `FontManager.FONT_RENDERER`                      | `FontManager.getFONT_RENDERER()`                              |
| `EventManager.callEvent(event)`                  | `EventManager.INSTANCE.callEvent(event)`                      |

Kotlin `object`s are reached through `INSTANCE`, unless the member is marked `@JvmStatic` or `@JvmField` like `ModuleCategories.MISC`. Where a helper takes a Kotlin lambda with a receiver, there is an overload taking a `Consumer`:

```java
private void render(WorldRenderEvent event) {
    if (found == null) {
        return;
    }

    RenderShortcutsKt.withPositionRelativeToCamera(event.getEnvironment(), found, env ->
        RenderShortcutsKt.drawBox(env, RenderShortcutsKt.FULL_BOX, new Color4b(255, 0, 0, 80), Color4b.RED));
}
```

### Commands

Commands use Brigadier's builders directly, see [Creating Commands](/docs/add-on-api/creating-commands#plain-brigadier).
