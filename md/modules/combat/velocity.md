## Velocity

Velocity changes how far you get pushed back when something hits you. You can take less knockback, none at all, or get pushed later. This helps you stay close to the enemy in a fight. Most modes are made for one server or anticheat, so pick the one for where you play.

**Category:** Combat
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Choice | Modify | Modify, Reversal, Strafe, JumpReset, Lag, Reduce, Hypixel, Dexland, Hylex, BlocksMC, Grim-2.3.71, Grim-2.3.44-MC1.17, AAC-4.4.2, Intave-2026-10-02 | How knockback is changed. The first six work on many servers. The others are made for one server or anticheat. |
| Mode → [Modify] → Horizontal | Decimal | 0.0 | -1.0..1.0 | How much sideways knockback you take. 0 means none, 1 means normal. |
| Mode → [Modify] → Vertical | Decimal | 0.0 | -1.0..1.0 | How much upward knockback you take. |
| Mode → [Modify] → MotionHorizontal | Decimal | 0.0 | 0.0..1.0 | How much of your own sideways speed you keep when Horizontal is 0. |
| Mode → [Modify] → MotionVertical | Decimal | 0.0 | 0.0..1.0 | How much of your own upward speed you keep when Vertical is 0. |
| Mode → [Modify] → Chance | Integer | 100 | 0..100 % | How often the knockback is changed. |
| Mode → [Modify] → Filter | Choice | Always | Always, OnGround, InAir | Only works on the ground, only in the air, or always. |
| Mode → [Modify] → OnlyMove | Toggle | false | | Only works while you are moving. |
| Mode → [Modify] → TransactionBuffer | Integer | 0 | 0..3 | Helps against some anticheats. Leave it at 0 if you are not sure. |
| Mode → [Modify] → ConsiderExplosion | Toggle | true | | Also changes knockback from explosions. |
| Mode → [Reversal] → Delay | Integer | 2 | 1..5 ticks | How long to wait before pushing you back the other way, in ticks (20 per second). |
| Mode → [Reversal] → XModifier | Decimal | 0.5 | 0.0..1.0 | How strongly you are pushed back east or west. |
| Mode → [Reversal] → ZModifier | Decimal | 0.5 | 0.0..1.0 | How strongly you are pushed back north or south. |
| Mode → [Reversal] → OnlyMoving | Toggle | false | | Only works while you are moving. |
| Mode → [Strafe] → Delay | Integer | 2 | 0..10 ticks | How long to wait after the hit before turning your knockback into the direction you walk. |
| Mode → [Strafe] → Strength | Decimal | 1.0 | 0.1..2.0 | How strongly you move in your walking direction. |
| Mode → [Strafe] → OnlyFacing | Toggleable Group | Off | | Only works while you look at an enemy close to you. |
| Mode → [Strafe] → OnlyFacing → Range | Decimal | 3.5 | 0.1..6.0 | How close the enemy has to be, in blocks. |
| Mode → [Strafe] → UntilGround | Toggle | false | | Keeps going until you land. |
| Mode → [JumpReset] → Chance | Decimal | 100.0 | 0.0..100.0 % | How often you jump when you get hit. Jumping at the right moment makes the knockback smaller. |
| Mode → [JumpReset] → JumpByReceivedHits | Toggleable Group | Off | | Only jumps after you got hit a number of times. |
| Mode → [JumpReset] → JumpByReceivedHits → HitsUntilJump | Integer Range | 2..2 | 0..10 | How many hits to take before jumping. |
| Mode → [JumpReset] → JumpByDelay | Toggleable Group | On | | Waits a little before jumping. |
| Mode → [JumpReset] → JumpByDelay → UntilJump | Integer Range | 2..2 | 0..20 ticks | How long to wait before jumping. |
| Mode → [Lag] → LagTime | Integer Range | 5..5 | 1..20 ticks | How long to hold back the knockback before it is used. |
| Mode → [Lag] → JumpReset | Toggle | false | | Also jumps when the knockback is used. |
| Mode → [Lag] → ConsiderExplosion | Toggle | true | | Also holds back knockback from explosions. |
| Mode → [Reduce] → AttackCount | Integer Range | 3..3 | 0..20 | How many of your hits make your knockback smaller. |
| Mode → [Reduce] → LagTargetRange | Decimal Range | 2.0..6.0 | 0.0..20.0 | How close an enemy has to be for the lag part to work, in blocks. |
| Mode → [Reduce] → LagMaxDelay | Integer | 10 | 1..1000 ticks | How long the knockback can be held back at most. |
| Mode → [Reduce] → LagRequireKillAura | Toggle | false | | Only lags while [KillAura](/docs/modules/combat/killaura) is on. |
| Mode → [Reduce] → Horizontal | Decimal | 0.6 | 0.0..1.0 | How much sideways knockback you take each time you hit. |
| Mode → [Reduce] → Vertical | Decimal | 1.0 | 0.0..1.0 | How much upward knockback you take each time you hit. |
| Mode → [Reduce] → Debug | Toggleable Group | Off | | Tells you what the mode is doing. |
| Mode → [Reduce] → Debug → ChatMessage | Toggle | false | | Writes it in chat. |
| Mode → [Reduce] → Debug → Notification | Toggle | false | | Shows it as a notification. |
| Mode → [Reduce] → BlinkEsp | Choice | Wireframe | Box, Model, Wireframe, None | How your real spot is drawn while knockback is held back. |
| Mode → [Reduce] → BlinkEsp → [Box] → Color | Color | | | Color inside the box. |
| Mode → [Reduce] → BlinkEsp → [Box] → OutlineColor | Color | | | Color of the box's edges. |
| Mode → [Reduce] → BlinkEsp → [Model] → OutlineColor | Color | | | Color of the model's outline. |
| Mode → [Reduce] → BlinkEsp → [Model] → LightPercent | Integer | 60 | 0..100 % | How bright the model is. |
| Mode → [Reduce] → BlinkEsp → [Wireframe] → Color | Color | | | Color of the wireframe. |
| Mode → [Reduce] → BlinkEsp → [Wireframe] → OutlineColor | Color | | | Color of the wireframe's edges. |
| Mode → [Dexland] → HReduce | Decimal | 0.3 | 0.0..1.0 | How much sideways knockback you take. |
| Mode → [Dexland] → AttacksToWork | Integer | 4 | 1..10 | How many hits it takes before it starts working. |
| Mode → [Grim-2.3.44-MC1.17] → AlternativeBypass | Toggle | true | | Uses a different way to get past the anticheat. |
| Mode → [AAC-4.4.2] → Reduce | Decimal | 0.62 | 0.0..1.0 | How much knockback you take while in the air. |
| Mode → [Intave-2026-10-02] → ReduceOnAttack | Toggleable Group | On | | Makes knockback smaller when you hit back. |
| Mode → [Intave-2026-10-02] → ReduceOnAttack → Factor | Decimal | 0.6 | 0.6..1.0 | How much knockback you take. |
| Mode → [Intave-2026-10-02] → ReduceOnAttack → HurtTime | Integer Range | 5..7 | 1..10 | Only works this many ticks after you got hit. |
| Mode → [Intave-2026-10-02] → ReduceOnAttack → LastAttackTimeToReduce | Integer | 2000 | 1..10000 | Only works if you hit someone this recently, in milliseconds. |
| Mode → [Intave-2026-10-02] → JumpReset | Toggleable Group | On | | Jumps when you get hit to take less knockback. |
| Mode → [Intave-2026-10-02] → JumpReset → Chance | Decimal | 50.0 | 0.0..100.0 % | How often you jump. |
| Mode → [Intave-2026-10-02] → JumpReset → Randomize | Toggleable Group | Off | | Waits a random time before jumping. |
| Mode → [Intave-2026-10-02] → JumpReset → Randomize → DelayTicks | Integer Range | 0..5 | 0..10 | How long to wait, in ticks. |
| Delay | Integer Range | 0..0 | 0..40 ticks | Waits this long before your knockback is changed. |
| PauseOnFlag | Integer | 0 | 0..20 ticks | How long to stop working after the server pulls you back. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/velocity/ModuleVelocity.kt)*
