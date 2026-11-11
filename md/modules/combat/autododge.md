## AutoDodge

AutoDodge moves you out of the way of arrows and thrown tridents before they hit you. It works out where each one is flying and steps you to the side. Normally it only changes how you walk and leaves your aim alone.

**Category:** Combat
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Ignore | Multi-Select | OpenInventory, UsingItem, UsingScaffold | OpenInventory, UsingItem, UsingScaffold | Does not dodge while a picked thing is true: a menu or chest is open (OpenInventory), you are eating, drinking or pulling a bow (UsingItem), or [Scaffold](/docs/modules/world/scaffold) is on (UsingScaffold). |
| AllowRotationChange | Toggleable Group | Off | | Lets AutoDodge also turn you toward a safe spot when stepping aside is not enough. Other players can see this. |
| AllowRotationChange → AllowJump | Toggle | true | | Lets AutoDodge also jump when that helps you get away faster. |
| AllowTimer | Toggleable Group | Off | | Lets AutoDodge speed up the game for a moment when there is not enough time to get away. |
| AllowTimer → TimerSpeed | Decimal | 2.0 | 1.0..10.0 x | How much faster the game runs while dodging. Higher values are easier for anticheats to notice. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/autododge/ModuleAutoDodge.kt)*
