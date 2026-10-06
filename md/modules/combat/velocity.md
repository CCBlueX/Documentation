## Velocity

Velocity (also known as AntiKnockback) changes how much knockback you take when something hits you. When a player or mob strikes you, the server pushes you back; this module intercepts that push and lets you cancel it, shrink it, redirect it, or delay it so you can stay on top of your target instead of getting bounced away. It's a staple for close-range fights, especially when paired with [KillAura](/docs/modules/combat/killaura).

The behavior depends entirely on the **Mode** you pick. Generic modes like Modify, Reversal, Strafe, JumpReset, Lag and Reduce work on a wide range of servers, while the named modes (Hypixel, Dexland, Hylex, BlocksMC) and anticheat modes (Grim2371, Grim2344-117, AAC4.4.2, Intave) are tuned to slip past specific setups. Some modes simply scale the knockback packet, some reverse it, and the Lag-based modes hold incoming knockback for a few ticks (similar to [Blink](/docs/modules/player/blink) and [FakeLag](/docs/modules/combat/fakelag)) before releasing it.

Because aggressive knockback reduction is one of the most heavily watched behaviors on modern anticheats, use the global **Delay** to spread out when velocity is applied and **PauseOnFlag** to back off automatically after the server corrects your position, lowering the chance of being flagged.

**Category:** Combat
**Enabled by default:** Yes

### Settings

| Setting | Type | Default | Range | Description |
| --- | --- | --- | --- | --- |
| Mode | Mode Selector | JumpReset | Modify, Reversal, Strafe, JumpReset, Lag, Reduce, Hypixel, Dexland, Hylex, BlocksMC, Grim2371, Grim2344-117, AAC4.4.2, Intave | Chooses how knockback is handled. Generic modes work broadly; named and anticheat modes target specific servers. |
| Mode → [Modify] → Horizontal | Decimal | 0.0 | -1.0..1.0 | Multiplier for sideways knockback (0 cancels it). |
| Mode → [Modify] → Vertical | Decimal | 1.0 | -1.0..1.0 | Multiplier for upward knockback. |
| Mode → [Modify] → MotionHorizontal | Decimal | 0.0 | 0.0..1.0 | Sideways motion kept when Horizontal is 0, to avoid an obvious dead stop. |
| Mode → [Modify] → MotionVertical | Decimal | 1.0 | 0.0..1.0 | Upward motion kept when Vertical is 0. |
| Mode → [Modify] → Chance | Integer | 100 | 0..100 % | How often the modification is applied. |
| Mode → [Modify] → Filter | Choice | Always | Always, OnGround, InAir | Restricts the effect to being on the ground, in the air, or always. |
| Mode → [Modify] → OnlyMove | Toggle | false | — | Only modify knockback while you are actively moving. |
| Mode → [Modify] → TransactionBuffer | Integer | 0 | 0..3 | Buffers server transactions to help hide the effect. |
| Mode → [Modify] → ConsiderExplosion | Toggle | true | — | Also modify knockback caused by explosions. |
| Mode → [Reversal] → Delay | Integer | 2 | 1..5 ticks | Ticks to wait before reversing your velocity. |
| Mode → [Reversal] → XModifier | Decimal | 0.5 | 0.0..1.0 | Strength of the reversed motion on the X axis. |
| Mode → [Reversal] → ZModifier | Decimal | 0.5 | 0.0..1.0 | Strength of the reversed motion on the Z axis. |
| Mode → [Reversal] → OnlyMoving | Toggle | false | — | Only reverse velocity while you are moving. |
| Mode → [Strafe] → Delay | Integer | 0 | 0..10 ticks | Ticks to wait after being hit before strafing. |
| Mode → [Strafe] → Strength | Decimal | 1.0 | 0.1..2.0 | How strongly your movement is redirected after taking knockback. |
| Mode → [Strafe] → OnlyFacing | Toggleable Group | off | — | Only strafe while looking at a nearby enemy. |
| Mode → [Strafe] → OnlyFacing → Range | Decimal | 3.5 | 0.1..6.0 | Distance within which an enemy counts for OnlyFacing. |
| Mode → [Strafe] → UntilGround | Toggle | false | — | Keep applying the strafe until you land. |
| Mode → [JumpReset] → Chance | Decimal | 100.0 | 0.0..100.0 % | How often a jump-reset is performed when hit. |
| Mode → [JumpReset] → JumpByReceivedHits | Toggleable Group | off | — | Trigger the jump after a set number of received hits. |
| Mode → [JumpReset] → JumpByReceivedHits → HitsUntilJump | Integer Range | 2..2 | 0..10 | Hits taken before jumping. |
| Mode → [JumpReset] → JumpByDelay | Toggleable Group | off | — | Trigger the jump after a tick delay instead. |
| Mode → [JumpReset] → JumpByDelay → UntilJump | Integer Range | 2..2 | 0..20 ticks | Ticks waited before jumping. |
| Mode → [Lag] → LagTime | Integer Range | 5..5 | 1..20 ticks | How many ticks of knockback to hold back before releasing. |
| Mode → [Lag] → JumpReset | Toggle | false | — | Also jump when the held knockback is released. |
| Mode → [Lag] → ConsiderExplosion | Toggle | true | — | Also delay knockback caused by explosions. |
| Mode → [Reduce] → AttackCount | Integer Range | 3..3 | 0..20 | Number of attacks over which knockback is reduced. |
| Mode → [Reduce] → LagTargetRange | Decimal Range | 2.0..6.0 | 0.0..20.0 | Distance window for selecting and lagging toward a target. |
| Mode → [Reduce] → LagMaxDelay | Integer | 10 | 1..1000 ticks | Maximum ticks knockback can be held before forced release. |
| Mode → [Reduce] → LagRequireKillAura | Toggle | false | — | Only lag while [KillAura](/docs/modules/combat/killaura) is running. |
| Mode → [Reduce] → Horizontal | Decimal | 0.6 | 0.0..1.0 | Sideways knockback multiplier applied on each attack. |
| Mode → [Reduce] → Vertical | Decimal | 1.0 | 0.0..1.0 | Upward knockback multiplier applied on each attack. |
| Mode → [Reduce] → Debug | Toggleable Group | off | — | Show diagnostic feedback about the reduce/lag state. |
| Mode → [Reduce] → Debug → ChatMessage | Toggle | false | — | Print debug info to chat. |
| Mode → [Reduce] → Debug → Notification | Toggle | false | — | Show debug info as notifications. |
| Mode → [Reduce] → BlinkEsp | Mode Selector | Wireframe | Box, Model, Wireframe, None | How the lagged target's real position is rendered while held. |
| Mode → [Reduce] → BlinkEsp → [Box] → Color | Color | — | — | Fill color of the box render. |
| Mode → [Reduce] → BlinkEsp → [Box] → OutlineColor | Color | — | — | Outline color of the box render. |
| Mode → [Reduce] → BlinkEsp → [Model] → OutlineColor | Color | — | — | Outline color of the model render. |
| Mode → [Reduce] → BlinkEsp → [Model] → LightPercent | Integer | 60 | 0..100 % | Brightness of the rendered model. |
| Mode → [Reduce] → BlinkEsp → [Wireframe] → Color | Color | — | — | Fill color of the wireframe render. |
| Mode → [Reduce] → BlinkEsp → [Wireframe] → OutlineColor | Color | — | — | Outline color of the wireframe render. |
| Mode → [Dexland] → HReduce | Decimal | 0.3 | 0.0..1.0 | Sideways knockback multiplier for the Dexland bypass. |
| Mode → [Dexland] → AttacksToWork | Integer | 4 | 1..10 | Attacks needed before the reduction kicks in. |
| Mode → [Grim2344-117] → AlternativeBypass | Toggle | false | — | Use an alternative packet sequence for the bypass. |
| Mode → [AAC4.4.2] → Reduce | Decimal | 0.62 | 0.0..1.0 | Knockback multiplier applied while airborne and hurt. |
| Mode → [Intave] → ReduceOnAttack | Toggleable Group | on | — | Reduce knockback when you attack, within timing limits. |
| Mode → [Intave] → ReduceOnAttack → Factor | Decimal | 0.97 | 0.6..1.0 | Knockback multiplier applied on attack. |
| Mode → [Intave] → ReduceOnAttack → HurtTime | Integer Range | 5..7 | 1..10 | Hurt-time window during which the reduction applies. |
| Mode → [Intave] → ReduceOnAttack → LastAttackTimeToReduce | Integer | 2000 | 1..10000 | Max milliseconds since your last attack for the reduction to apply. |
| Mode → [Intave] → JumpReset | Toggleable Group | on | — | Perform jump-resets to shed knockback. |
| Mode → [Intave] → JumpReset → Chance | Decimal | 50.0 | 0.0..100.0 % | How often a jump-reset is attempted. |
| Mode → [Intave] → JumpReset → Randomize | Toggleable Group | off | — | Randomize the delay between jump-resets. |
| Mode → [Intave] → JumpReset → Randomize → DelayTicks | Integer Range | 0..5 | 0..10 | Random tick delay range before each jump-reset. |
| Delay | Integer Range | 0..0 | 0..40 ticks | Delays the incoming velocity update by a random amount within this range. |
| PauseOnFlag | Integer | 2 | 0..20 ticks | Ticks to pause the module after the server corrects your position, to avoid further flags. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/velocity/ModuleVelocity.kt)*
