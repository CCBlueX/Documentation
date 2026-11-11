## Rotations

The Rotations settings control how your head turns when a module looks at something, like an enemy or a block. Fast, instant turns are easy for anticheats to notice. Slower, smoother turns look more like a real player.

The server can see you look somewhere else than your screen shows. Your camera only moves when MovementCorrection is set to ChangeLook.

Many modules use these settings, for example [KillAura](/docs/modules/combat/killaura), [AutoRod](/docs/modules/combat/autorod), [Scaffold](/docs/modules/world/scaffold) and [Nuker](/docs/modules/world/nuker).

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| AngleSmooth | Choice | Linear | Linear, Sigmoid, Interpolation, Acceleration, AI | How your head turns. Interpolation and AI are only in [KillAura](/docs/modules/combat/killaura) and [TpAura](/docs/modules/combat/tpaura). |
| AngleSmooth → [Linear] → HorizontalTurnSpeed | Decimal Range | 180.0..180.0 | 0.0..180.0 | How far you can turn left and right per tick (20 ticks per second), in degrees. |
| AngleSmooth → [Linear] → VerticalTurnSpeed | Decimal Range | 180.0..180.0 | 0.0..180.0 | How far you can turn up and down per tick. |
| AngleSmooth → [Sigmoid] → HorizontalTurnSpeed | Decimal Range | 180.0..180.0 | 0.0..180.0 | Fastest turn left and right per tick. You turn fast when far away from the target and slow down when close. |
| AngleSmooth → [Sigmoid] → VerticalTurnSpeed | Decimal Range | 180.0..180.0 | 0.0..180.0 | Fastest turn up and down per tick. |
| AngleSmooth → [Sigmoid] → Steepness | Decimal | 10.0 | 0.0..20.0 | How suddenly the turn slows down. |
| AngleSmooth → [Sigmoid] → Midpoint | Decimal | 0.3 | 0.0..1.0 | Where during the turn it starts to slow down. |
| AngleSmooth → [Interpolation] → HorizontalSpeed | Integer Range | 80..85 | 1..100 % | How fast you turn left and right. |
| AngleSmooth → [Interpolation] → VerticalSpeed | Integer Range | 20..25 | 1..100 % | How fast you turn up and down. |
| AngleSmooth → [Interpolation] → DirectionChangeFactor | Integer Range | 95..100 | 0..100 % | How fast you follow when the target changes direction. |
| AngleSmooth → [Interpolation] → Midpoint | Decimal | 0.35 | 0.0..1.0 | Where during the turn you move fastest. |
| AngleSmooth → [Acceleration] → YawAcceleration | Decimal Range | 20.0..25.0 | 1.0..180.0 | How quickly your left and right turning can speed up or slow down. Your head speeds up and slows down like a real hand moving the mouse. |
| AngleSmooth → [Acceleration] → PitchAcceleration | Decimal Range | 20.0..25.0 | 1.0..180.0 | The same for up and down. |
| AngleSmooth → [Acceleration] → DynamicAccel | Toggleable Group | Off | | Changes the acceleration by how far away the target is and whether your crosshair is on it. |
| AngleSmooth → [Acceleration] → DynamicAccel → CoefDistance | Decimal | -1.393 | -2.0..2.0 | How much the distance changes the acceleration. Below 0 means slower for far targets. |
| AngleSmooth → [Acceleration] → DynamicAccel → YawCrosshairAccel | Decimal Range | 17.0..20.0 | 1.0..180.0 | Left and right acceleration while your crosshair is on the target. |
| AngleSmooth → [Acceleration] → DynamicAccel → PitchCrosshairAccel | Decimal Range | 17.0..20.0 | 1.0..180.0 | Up and down acceleration while your crosshair is on the target. |
| AngleSmooth → [Acceleration] → AccelerationError | Toggleable Group | On | | Adds small random mistakes to the acceleration. |
| AngleSmooth → [Acceleration] → AccelerationError → YawAccelError | Decimal | 0.1 | 0.01..1.0 | How big the mistakes left and right are. |
| AngleSmooth → [Acceleration] → AccelerationError → PitchAccelError | Decimal | 0.1 | 0.01..1.0 | How big the mistakes up and down are. |
| AngleSmooth → [Acceleration] → ConstantError | Toggleable Group | On | | Adds a small random shake every tick. |
| AngleSmooth → [Acceleration] → ConstantError → YawConstantError | Decimal | 0.1 | 0.01..1.0 | How big the shake left and right is, in degrees. |
| AngleSmooth → [Acceleration] → ConstantError → PitchConstantError | Decimal | 0.1 | 0.01..1.0 | How big the shake up and down is, in degrees. |
| AngleSmooth → [Acceleration] → SigmoidDeceleration | Toggleable Group | Off | | Slows the turn down as you get close to the target. |
| AngleSmooth → [Acceleration] → SigmoidDeceleration → Steepness | Decimal | 10.0 | 0.0..20.0 | How suddenly it slows down. |
| AngleSmooth → [Acceleration] → SigmoidDeceleration → Midpoint | Decimal | 0.3 | 0.0..1.0 | Where during the turn it starts to slow down. |
| AngleSmooth → [AI] → Model | Choice | | | A trained model that turns your head like a player it learned from. |
| AngleSmooth → [AI] → Correction | Choice | Interpolation | Interpolation, Linear, None | Smooths the model's turns a bit more. Interpolation works best. |
| AngleSmooth → [AI] → OutputMultiplier → Yaw | Decimal | 1.5 | 0.5..2.0 | Makes the model's left and right turns bigger or smaller. |
| AngleSmooth → [AI] → OutputMultiplier → Pitch | Decimal | 1.0 | 0.5..2.0 | Makes the model's up and down turns bigger or smaller. |
| ShortStop | Toggleable Group | Off | | Sometimes stops turning for a moment. Only in KillAura and TpAura. |
| ShortStop → Rate | Integer | 3 | 1..25 % | How often it stops, each tick. |
| ShortStop → Duration | Integer Range | 1..2 | 1..5 ticks | How long it stops. |
| Fail | Toggleable Group | Off | | Sometimes looks a bit away from the target, like a player who misses. Only in KillAura and TpAura. |
| Fail → Rate | Integer | 3 | 1..100 % | How often it looks away, each tick. |
| Fail → Factor | Decimal | 0.04 | 0.01..0.99 | How far it drifts away. |
| Fail → StrengthHorizontal | Decimal Range | 5.0..10.0 | 1.0..90.0 ° | How far it looks away left or right. |
| Fail → StrengthVertical | Decimal Range | 0.0..2.0 | 0.0..90.0 ° | How far it looks away up or down. |
| Fail → TransitionInDuration | Integer Range | 1..4 | 0..20 ticks | How long it looks away. |
| MovementCorrection | Choice | Silent | Off, Strict, Silent, ChangeLook | How your walking fits the way the server sees you look. Off walks where your screen looks; it feels best but anticheats can notice. Strict walks the way the server sees you look. Silent does the same but keeps your walking direction smoother. ChangeLook really turns your camera. |
| ResetThreshold | Decimal | 2.0 | 1.0..180.0 | When turning back, how close to where you really look counts as done, in degrees. |
| TicksUntilReset | Integer | 5 | 1..30 ticks | How long to wait after the module is done before turning back to where you really look. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/utils/aiming/RotationsValueGroup.kt)*
