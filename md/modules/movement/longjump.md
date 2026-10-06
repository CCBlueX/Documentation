## LongJump

LongJump greatly extends the horizontal distance you can cover in a single jump. When you jump (or when AutoJump handles it automatically), the module applies a speed boost mid-air so you travel much farther than normal before landing. This makes it useful for crossing gaps, reaching platforms, or escaping danger quickly on servers that do not fully patch the underlying mechanics being exploited.

The module offers four modes, each targeting a specific anticheat. **NoCheatPlusBoost** simply multiplies your horizontal velocity the moment you leave the ground. **NoCheatPlusBow** fires a series of arrows straight up to accumulate knockback energy, then converts that stored boost into a fast forward jump — you must have a bow and arrows in your inventory for this mode to work. **Vulcan289** sends a crafted sequence of movement packets to trigger a server-side correction that it then exploits for extra speed. **Matrix-7.14.5-Flag** intentionally triggers position-correction flags from Matrix anticheat and uses the resulting momentum to fly forward. Pick the mode that matches the anticheat running on your target server.

Enable **AutoJump** to have the module jump for you automatically whenever you move, so you do not have to time the jump yourself. Turn on **DisableAfterFinished** if you only want a single boosted jump per activation — the module will switch itself off once the boost sequence completes, so you do not need to manually toggle it off each time.

**Category:** Movement
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | NoCheatPlusBoost | — | Selects the long-jump technique. Choose the mode that matches the anticheat on your server. Available modes: NoCheatPlusBoost, NoCheatPlusBow, Vulcan289, Matrix-7.14.5-Flag. |
| Mode → [NoCheatPlusBoost] → NCPBoost | Decimal | 4.25 | 1.0 – 10.0 | Multiplier applied to horizontal velocity on the tick you jump. Higher values send you farther but are more likely to be flagged. |
| Mode → [NoCheatPlusBow] → Rotations | Setting Group | — | — | See [Shared: Rotations](/docs/modules/shared-settings/rotations). |
| Mode → [NoCheatPlusBow] → Charged | Integer | 4 | 3 – 20 | Number of ticks the bow must be held before each arrow is released. Lower values shoot faster; higher values produce fully-charged shots. |
| Mode → [NoCheatPlusBow] → Speed | Decimal | 2.5 | 0.0 – 20.0 | Horizontal strafe speed applied when the module launches the forward jump after collecting arrow boosts. |
| Mode → [NoCheatPlusBow] → ArrowsToShoot | Integer | 8 | 0 – 20 | Number of arrows fired upward to accumulate knockback energy before the jump is executed. |
| Mode → [NoCheatPlusBow] → FallDistanceToJump | Decimal | 0.42 | 0.0 – 2.0 | Fall distance that must be reached before the module triggers each additional jump impulse during the boost phase. |
| Mode → [Matrix-7.14.5-Flag] → BoostSpeed | Decimal | 1.97 | 0.1 – 5.0 | Horizontal speed applied to the player during each flag-induced boost burst. |
| Mode → [Matrix-7.14.5-Flag] → MotionY | Decimal | 0.42 | 0.0 – 5.0 | Upward velocity set during each boost burst. Increase to gain more air time; decrease to stay closer to the ground. |
| Mode → [Matrix-7.14.5-Flag] → Delay | Integer | 0 | 0 – 3 | Number of ticks to wait after leaving the ground before the boost is applied. Small delays can help bypass certain flag thresholds. |
| AutoJump | Toggle | false | — | When enabled, automatically jumps for you whenever you are on the ground and moving, so you do not have to time the jump manually. Has no effect in NoCheatPlusBow mode. |
| DisableAfterFinished | Toggle | false | — | Automatically disables LongJump after one complete boost sequence, useful if you only need a single long jump per activation. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/longjump/ModuleLongJump.kt)*
