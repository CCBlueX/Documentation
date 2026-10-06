## Stable API

Add-ons compile against the whole client, there is no separate API artifact. What an add-on can rely on between builds is everything marked `@AddonApi`: a marked class with its public members, or a single marked function or property. The rest of the client is public as well, but may change in any build.

### What stable means

The marked declarations are recorded in [`api/LiquidBounce.api`](https://github.com/CCBlueX/LiquidBounce/blob/nextgen/api/LiquidBounce.api) in the LiquidBounce repository, and the client's build compares its code against that file. A marked declaration therefore cannot change or disappear by accident. When it changes on purpose, the file changes with it, visible in the commit.

Stable does not cover Minecraft. An add-on is built for one Minecraft version and is rebuilt for the next, see [Publishing](/docs/add-on-api/developers/publishing#compatibility).

If an add-on needs something that is not marked, ask for it on [GitHub](https://github.com/CCBlueX/LiquidBounce/issues) instead of copying it.

### What is marked

| Area       | Declarations                                                                                                          |
|------------|-----------------------------------------------------------------------------------------------------------------------|
| Add-on     | `LiquidBounceAddon`, `AddonMetadata`, `AddonState`                                                                    |
| Modules    | `ClientModule`, `ModuleCategory`, `ModuleCategories`, `ModuleManager.get`, `ModuleClickGui`, `MinecraftShortcuts`     |
| Settings   | `ValueGroup` with every builder, `ToggleableValueGroup`, `Value`, `Config`, `ChoiceListValue.getChoicesStrings`, `ModeValueGroup.getModeStrings` |
| Events     | `Event`, `CancellableEvent`, `EventState`, `EventListener` with `on`, `onTick`, `after` and `every`, `EventManager`, the events in the [Events](/docs/add-on-api/developers/events#stable-events) table, `EventPriorityConvention` |
| Commands   | `CommandRegistrar`, `ClientCommandSource`, `CommandManager.execute`, `CommandManager.isRootTaken`, `CommandManager.GlobalSettings` |
| HUD        | `HudComponent`, `NativeHudComponent`, `HudComponentFactory.NativeHudComponentFactory`, `HudComponentManager`, `HudComponentTweak`, `Alignment` |
| Rendering  | `WorldRenderEnvironment`, `renderEnvironment`, `withPositionRelativeToCamera`, `drawBox`, `drawLine`, `FULL_BOX`, `drawQuad`, `FontManager`, `AbstractFontRenderer`, `HorizontalAnchor`, `VerticalAnchor`, `Color4b` |
| Browser    | `BrowserBackend`, `BrowserBackendProvider`, `BrowserBackendManager.registerBackend`, `Browser`, `BrowserTexture`, `BrowserViewport`, `BrowserState`, `BrowserSettings`, `InputAcceptor`, `InputHandler`, `isBrowserSkipped` |
| Chat       | `chat`, `notification`, `regular`, `variable`, `highlight`, `warning`, `markAsError`, `MessageMetadata`, `translation` |
| Combat     | `attackEntity`, `findEnemy`, `findEnemies`, `shouldBeAttacked`, `shouldBeShown`, `CombatManager`, `EntityTargetingInfo`, `EntityTargetClassification`, `FriendManager.add`, `remove` and `clear` |
| Rotations  | `RotationManager.setRotationTarget`, `currentRotation`, `serverRotation`, `RotationTarget`, `RotationsValueGroup`, `Rotation`, `MovementCorrection`, `Priority` |
| World      | `BlockPos.state`, `stateOrEmpty`, `getBlock`, `outlineBox`, `BlockState.isInteractable`, `doPlacement`, `doBreak`, `SwingMode` |
| Inventory  | `Slots`, `ItemSlot`, `HotbarItemSlot`, `SilentHotbar`, `useHotbarSlotOrOffhand`, `InventoryManager.isInventoryOpen`, `isHandledScreenOpen` |
| Movement   | `DirectionalInput`, `LocalPlayer.moving`, `Entity.horizontalSpeed`, `Vec3.withStrafe`, `LocalPlayer.stopXZVelocity`, `Timer.requestTimerSpeed` |
| Misc       | `sendPacketSilently`, `inGame`, `Chronometer`, `InputBind`, `MarketplaceItemType`, `MarketplaceItemHandler`, `MarketplaceManager` handlers, `SubscribedItem`, `QuickFix`, `QuickFixes`, `Instructions`, `ClientError` |

The API file is the complete list.

### What is not marked

Some of what the template and these pages use is public but not marked:

- the handler functions `handler`, `tickHandler`, `sequenceHandler` and the waits `waitTicks`, `tickUntil`, `waitMatches`. `on`, `onTick`, `after` and `every` are their stable counterparts.
- the command DSL (`register`, `literal`, `argument`, `optional`, `exec`, `suggestions`). Plain Brigadier builders are the stable counterpart.
- `Mode` and most of `ModeValueGroup`.
- built-in modules, and everything else not in the list.

A change to them is not caught by the client's build.

### Changing the API

For contributors to LiquidBounce: mark a declaration with `@AddonApi` to make it stable, then record it:

```sh
./gradlew updateKotlinAbi
```

Commit the updated `api/LiquidBounce.api` together with the change. `./gradlew checkKotlinAbi` fails while the code and the file disagree, so a change to a marked declaration always shows up in review. Marked declarations look unused from inside the client, remove them only on purpose.
