## AutoWindCharge

AutoWindCharge throws a wind charge at your feet every time you land while you hold the jump key, and jumps at the same moment. The blast and the jump together launch you high into the air, so you keep bouncing. It uses one wind charge per bounce and takes it from your hotbar or offhand, so you don't need to hold it.

It does nothing while you swim, glide with an elytra, or are in water or lava.

Normally it throws straight down to launch you up. Hold the **HorizontalBoost** key (Left Control) to throw at an angle instead, which launches you forward, in the direction you are walking, to cover more distance.

**Category:** Player
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
| --- | --- | --- | --- | --- |
| HorizontalBoost | Toggleable Group | On | | Lets you hold a key to launch forward instead of straight up. |
| HorizontalBoost → Pitch | Decimal Range | 70.0..70.0 | 0.0..90.0 | How far down you look for the forward throw. Lower launches you flatter, 90 is straight down. |
| HorizontalBoost → Key | Key | Left Control | | Hold this key for a forward launch. |
| Rotate | Toggleable Group | On | | Turns your view to the throw direction before landing and only throws once you are aimed right. |
| Rotate → Rotations | Setting Group | | | See [Shared: Rotations](/docs/modules/shared-settings/rotations). |
| CombatPauseTime | Integer | 0 | 0..40 ticks | How long to pause attacking while it aims, in ticks (20 per second). |
| SlotResetDelay | Integer Range | 0..0 | 0..40 ticks | Wait before switching back from the wind charge slot. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/ModuleAutoWindCharge.kt)*
