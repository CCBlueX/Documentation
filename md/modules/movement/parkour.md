## Parkour

Parkour jumps for you at the very edge of a block, so you can run across gaps without pressing Jump. It only jumps while you walk and are not sneaking.

**Category:** Movement
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Assist | Toggleable Group | On |  | Helps you land your jumps. It picks the block across the gap you run toward, turns you toward it, steers you in the air and stops you on small landing spots. |
| Assist → MaxAngle | Decimal | 35 | 5..90 ° | How far to the side of where you are running a block can be and still be picked. |
| Assist → Rotations | Setting Group |  |  | See [Shared: Rotations](/docs/modules/shared-settings/rotations). |
| Assist → Render | Toggleable Group | On |  | Shows the jump Assist goes for: the flight, where you take off, the block you land on and where to look. A second arc shows when a slime bounce carries on. |
| Assist → Render → CanBeCovered | Toggle | false |  | Lets blocks hide the drawing. |
| Assist → Render → Arc | Color | White, see-through |  | Color of the flight path. |
| Assist → Render → TakeOff | Color | Orange-yellow |  | Color of the bar where the jump starts. |
| Assist → Render → Landing | Color | Green |  | Color of the block you land on. |
| Assist → Render → Aim | Color | LiquidBounce blue |  | Color of the post that shows where to look. |

---
*Last updated: 2026-11-12, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/ModuleParkour.kt)*
