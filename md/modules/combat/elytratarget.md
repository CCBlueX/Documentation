## ElytraTarget

ElytraTarget turns your elytra into a homing missile against another player. While you're gliding, it automatically steers your view toward the selected target and keeps you pointed at them, even as they move and try to juke you. It's designed to work hand-in-hand with [KillAura](/docs/modules/combat/killaura), so you can chase a target down in the air and land hits without manually fighting the elytra's momentum.

To keep your speed up during the chase, it can fire fireworks for you on a timer (see AutoFirework below), and it can predict where a fleeing target is heading so you aim slightly ahead of them instead of trailing behind. The module only does its work while you are actually fall-flying — if you aren't gliding, it stays idle.

Use it when you want aggressive aerial pursuit: pick your target with the shared [Target](/docs/modules/shared-settings/target) settings, take off, and let ElytraTarget handle the steering and rocket spam while you focus on clicking.

**Category:** Combat
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
| --- | --- | --- | --- | --- |
| Target | Setting Group | — | — | See [Shared: Target](/docs/modules/shared-settings/target). |
| Rotations | Setting Group | — | — | Controls how your view is steered toward the target while gliding. |
| Rotations → Sharp | Toggle | false | — | Makes the aiming turn faster and more aggressive instead of smoothly tracking. |
| Rotations → IgnoreKillAuraRotation | Toggle | true | — | Lets ElytraTarget keep steering your flight even while [KillAura](/docs/modules/combat/killaura) is setting its own attack rotations, so the two don't fight each other. |
| Rotations → Look | Toggle | false | — | Turns your actual camera toward the target instead of only adjusting your movement direction silently. |
| Rotations → AutoDistance | Toggle | true | — | Eases your aim when you get very close to the target to avoid overshooting and flying past them. |
| Rotations → Prediction | Toggleable Group | On | — | Aims ahead of the target based on their movement so you intercept rather than chase. |
| Rotations → Prediction → Mode | Choice | Simple | Simple, WithGravity | How the target's future position is estimated. WithGravity also accounts for the target falling. |
| Rotations → Prediction → GlidingOnly | Toggle | true | — | Only predicts ahead when the target is themselves gliding on an elytra. |
| Rotations → Prediction → Multiplier | Decimal Range | 1.0..1.1 | 0.5..3.0 | How far ahead of the target you aim; higher leads the target more. A random value in this range is used. |
| Rotations → RotateAt | Choice | Eyes | Eyes, Center | Whether to aim at the target's eyes or the middle of their body. |
| AutoFirework | Toggleable Group | On | — | Automatically uses firework rockets to keep your speed up during the chase. |
| AutoFirework → UseMode | Choice | Normal | Normal, Packet | How the firework is used — Normal swaps and uses it, Packet sends the use directly without a visible swap. |
| AutoFirework → ExtraDistance | Decimal | 50.0 | 5.0..100.0 m | Distance threshold to the target; when farther than this, the longer cooldown is used so rockets are spent more sparingly. |
| AutoFirework → SlotResetDelay | Integer Range | 0..0 | 0..20 ticks | Delay before switching back from the firework slot, picked randomly within this range. |
| AutoFirework → SyncCooldownWithKillAura | Toggle | false | — | Times firework use around [KillAura](/docs/modules/combat/killaura)'s attacks so rockets aren't fired mid-hit. |
| AutoFirework → Cooldown | Integer Range | 8..10 | 1..50 ticks | How long to wait between fireworks, chosen randomly within this range. |
| TargetRendering | Toggleable Group | On | — | See [Shared: TargetRendering](/docs/modules/shared-settings/target-rendering). |
| Safe | Toggle | true | — | Nudges you slightly upward when you're about to collide with terrain, helping you avoid crashing into blocks during the chase. |
| AlwaysGlide | Toggle | false | — | Keeps you gliding toward the target even when you would otherwise stop fall-flying. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/elytratarget/ModuleElytraTarget.kt)*
