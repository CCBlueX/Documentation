## ElytraTarget

ElytraTarget chases another player while you fly with an elytra. It steers you toward them and can use fireworks for you to keep your speed up. Use it together with [KillAura](/docs/modules/combat/killaura) to hit them in the air. It only works while you are flying.

**Category:** Combat
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Target | Setting Group |  | | See [Shared: Target](/docs/modules/shared-settings/target). |
| Rotations | Setting Group | | | How you are steered toward the target. |
| Rotations → Sharp | Toggle | false | | Turns faster and sharper. |
| Rotations → IgnoreKillAuraRotation | Toggle | true | | Keeps steering even while KillAura turns you to hit. |
| Rotations → Look | Toggle | false | | Also turns your camera toward the target. |
| Rotations → AutoDistance | Toggle | true | | Aims more carefully when you get very close, so you don't fly past. |
| Rotations → Prediction | Toggleable Group | On | | Aims at where the target will be, not where it is now. |
| Rotations → Prediction → Mode | Choice | Simple | Simple, WithGravity | How to guess where the target will be. WithGravity also counts that the target falls. |
| Rotations → Prediction → GlidingOnly | Toggle | true | | Only aims ahead when the target is flying with an elytra too. |
| Rotations → Prediction → Multiplier | Decimal Range | 1.8..2.0 | 0.5..3.0 | How far ahead to aim. Higher means further ahead. |
| Rotations → RotateAt | Choice | Eyes | Eyes, Center | Aim at the target's eyes or the middle of their body. |
| AutoFirework | Toggleable Group | On | | Uses fireworks for you to keep your speed up. |
| AutoFirework → UseMode | Choice | Normal | Normal, Packet | How the firework is used. Normal switches to it and uses it. Packet uses it without you seeing the switch. |
| AutoFirework → ExtraDistance | Decimal | 50.0 | 5.0..100.0 m | When the target is further away than this, fireworks are used more often. |
| AutoFirework → SlotResetDelay | Integer Range | 0..0 | 0..20 ticks | How long to wait before switching back to your old item. |
| AutoFirework → SyncCooldownWithKillAura | Toggle | false | | Times the fireworks around KillAura's hits. |
| AutoFirework → Cooldown | Integer Range | 8..10 | 1..50 ticks | How long to wait between fireworks, in ticks (20 per second). |
| TargetRendering | Toggleable Group | On | | See [Shared: TargetRendering](/docs/modules/shared-settings/targetrendering). |
| Safe | Toggle | true | | Pulls you up a bit when you are about to fly into blocks. |
| AlwaysGlide | Toggle | false | | Keeps flying toward the target even when you would stop gliding. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/elytratarget/ModuleElytraTarget.kt)*
