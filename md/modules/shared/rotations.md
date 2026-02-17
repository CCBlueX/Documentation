## Rotations

The Rotations setting group controls how the player's head rotation changes when a module needs to look at a target. It manages the speed and style of rotation transitions, optional movement correction to keep the player moving correctly while aiming in a different direction, and how long the rotation persists before resetting. Since server-side rotations differ from the client-side camera, these settings govern what the server sees rather than what the player sees on screen.

The Rotations setting group appears in the following modules:
- [KillAura](/docs/modules/combat/killaura) (combat-specific: includes ShortStop, Fail, Interpolation, and AI modes)
- [AutoRod](/docs/modules/combat/autorod)
- [AutoShoot](/docs/modules/combat/autoshoot)
- [ProjectileAimbot](/docs/modules/combat/projectileaimbot)
- [DroneControl](/docs/modules/combat/dronecontrol)
- [FastExp](/docs/modules/player/fastexp)
- [AntiAFK](/docs/modules/player/antiafk)
- [AutoWindCharge](/docs/modules/player/autowindcharge)
- [NoRotateSet](/docs/modules/player/norotateset)
- [AutoBuff](/docs/modules/player/autobuff)
- [ChestAura](/docs/modules/player/chestaura)
- [Scaffold](/docs/modules/world/scaffold)
- [Extinguish](/docs/modules/world/extinguish)
- [ProjectilePuncher](/docs/modules/world/projectilepuncher)
- [AutoFarm](/docs/modules/world/autofarm)
- [Fucker](/docs/modules/world/fucker)
- [PacketMine](/docs/modules/world/packetmine)
- [AutoTrap](/docs/modules/world/autotrap)
- [Nuker](/docs/modules/world/nuker) (Legit mode)
- [Sprint](/docs/modules/movement/sprint)
- [FreeCam](/docs/modules/render/freecam)
- [Derp](/docs/modules/misc/derp)
- [Notebot](/docs/modules/misc/notebot)
- [EasyPearl](/docs/modules/misc/easypearl)
- [AutoPearl](/docs/modules/misc/autopearl)

### Settings

| Setting | Type | Default | Range | Description |
|---------|------|---------|-------|-------------|
| AngleSmooth | Mode | Linear | See [AngleSmooth Modes](#anglesmooth-modes) | The algorithm used to smooth rotation transitions toward the target. Controls how quickly and naturally the player's aim moves. |
| ShortStop | Toggleable Group | Off | See [ShortStop](#shortstop-combat-modules-only) | Temporarily halts aiming at the target based on a random rate. **Only available in combat-specific modules (KillAura).** |
| Fail | Toggleable Group | Off | See [Fail](#fail-combat-modules-only) | Intentionally misses the target at a configurable rate by shifting the rotation away. **Only available in combat-specific modules (KillAura).** |
| MovementCorrection | Enum | Silent | See [MovementCorrection](#movementcorrection) | Determines how player movement input is adjusted to compensate for the server-side rotation differing from the client-side view direction. |
| ResetThreshold | Float | 2.0 | 1.0..180.0 | The minimum angular distance (in degrees) between the server rotation and the player's actual look direction before the rotation is considered close enough to reset. |
| TicksUntilReset | Integer | 5 | 1..30 | The number of ticks to wait after the module stops requesting a rotation before the server-side rotation resets back to the player's actual look direction. |

### AngleSmooth Modes

The AngleSmooth setting determines the algorithm used to transition from the current rotation toward the target rotation each tick. All modes that use turn speed factors work by computing a horizontal (yaw) and vertical (pitch) speed value, then linearly interpolating the current rotation toward the target by that amount per tick.

#### Linear

Moves toward the target at a constant turn speed per tick. Each tick, a random value within the configured range is chosen independently for yaw and pitch. This is the simplest and most predictable smoothing mode.

| Setting | Type | Default | Range | Description |
|---------|------|---------|-------|-------------|
| HorizontalTurnSpeed | Float Range | 180.0..180.0 | 0.0..180.0 | Maximum degrees per tick the yaw can change. A random value within this range is chosen each tick. |
| VerticalTurnSpeed | Float Range | 180.0..180.0 | 0.0..180.0 | Maximum degrees per tick the pitch can change. A random value within this range is chosen each tick. |

#### Sigmoid

Adjusts turn speed based on the angular distance to the target using a sigmoid (S-curve) function. When the target is far away, rotation is faster; as the aim gets closer to the target, rotation slows down. The turn speed is scaled by the sigmoid output, producing a decelerating approach. This mode is deprecated in favor of Interpolation.

| Setting | Type | Default | Range | Description |
|---------|------|---------|-------|-------------|
| HorizontalTurnSpeed | Float Range | 180.0..180.0 | 0.0..180.0 | Maximum degrees per tick the yaw can change. Scaled by the sigmoid curve. |
| VerticalTurnSpeed | Float Range | 180.0..180.0 | 0.0..180.0 | Maximum degrees per tick the pitch can change. Scaled by the sigmoid curve. |
| Steepness | Float | 10.0 | 0.0..20.0 | Controls how sharply the sigmoid transitions between slow and fast speeds. Higher values create a sharper transition. |
| Midpoint | Float | 0.3 | 0.0..1.0 | The normalized distance at which the sigmoid is centered. Below this point the speed ramps up; above it the speed approaches maximum. |

#### Interpolation *(combat-specific modules only)*

Combines sigmoid and quadratic Bézier interpolation for a more natural-looking aim transition. When the angular distance is large (above the midpoint), a Bézier curve produces smooth deceleration. When the distance is small (below the midpoint), a sigmoid curve handles fine adjustments. Also factors in direction changes — when the target moves and the aim direction shifts, an additional speed boost is applied.

| Setting | Type | Default | Range | Description |
|---------|------|---------|-------|-------------|
| HorizontalSpeed | Integer Range | 80..85 | 1..100 (%) | Horizontal turn speed as a percentage. A random value within this range is chosen each tick. |
| VerticalSpeed | Integer Range | 20..25 | 1..100 (%) | Vertical turn speed as a percentage. A random value within this range is chosen each tick. |
| DirectionChangeFactor | Integer Range | 95..100 | 0..100 (%) | How much additional speed to apply when the aim direction changes between ticks. Higher values make the aim react faster to moving targets. |
| Midpoint | Float | 0.35 | 0.0..1.0 | The normalized angular distance threshold that switches between Bézier (above) and sigmoid (below) interpolation curves. |

#### Acceleration

Simulates realistic aim by applying acceleration to the rotation. Instead of moving directly toward the target, it adjusts the current rotation velocity using a clamped acceleration value each tick. The new rotation is the previous rotation plus the previous velocity plus the acceleration, producing momentum-based aiming with gradual speed changes. Includes optional sub-groups for error injection and sigmoid-based deceleration.

| Setting | Type | Default | Range | Description |
|---------|------|---------|-------|-------------|
| YawAcceleration | Float Range | 20.0..25.0 | 1.0..180.0 | The maximum acceleration (degrees per tick²) applied to the yaw. A random value within this range is used to clamp the acceleration each tick. |
| PitchAcceleration | Float Range | 20.0..25.0 | 1.0..180.0 | The maximum acceleration (degrees per tick²) applied to the pitch. A random value within this range is used to clamp the acceleration each tick. |

**DynamicAccel** (toggleable, default: off) — Adjusts acceleration based on whether the crosshair is currently over the target entity and the distance to it. When the crosshair is on the target, a separate (typically lower) acceleration range is used for finer control. Distance to the target scales the acceleration range via a configurable coefficient.

| Setting | Type | Default | Range | Description |
|---------|------|---------|-------|-------------|
| CoefDistance | Float | -1.393 | -2.0..2.0 | Multiplied by the distance to the target and added to the acceleration range bounds. Negative values reduce acceleration at greater distances. |
| YawCrosshairAccel | Float Range | 17.0..20.0 | 1.0..180.0 | Yaw acceleration range used when the crosshair is over the target. |
| PitchCrosshairAccel | Float Range | 17.0..20.0 | 1.0..180.0 | Pitch acceleration range used when the crosshair is over the target. |

**AccelerationError** (toggleable, default: on) — Adds a random error proportional to the current acceleration, simulating imprecise human aim adjustments.

| Setting | Type | Default | Range | Description |
|---------|------|---------|-------|-------------|
| YawAccelError | Float | 0.1 | 0.01..1.0 | The acceleration error multiplier for yaw. The actual error each tick is `acceleration × random(-value, value)`. |
| PitchAccelError | Float | 0.1 | 0.01..1.0 | The acceleration error multiplier for pitch. |

**ConstantError** (toggleable, default: on) — Adds a small random constant offset to each tick's rotation, independent of acceleration.

| Setting | Type | Default | Range | Description |
|---------|------|---------|-------|-------------|
| YawConstantError | Float | 0.1 | 0.01..1.0 | Maximum constant error in degrees added to yaw each tick. The actual error is `random(-value, value)`. |
| PitchConstantError | Float | 0.1 | 0.01..1.0 | Maximum constant error in degrees added to pitch each tick. |

**SigmoidDeceleration** (toggleable, default: off) — Applies a sigmoid-based multiplier to the acceleration, causing the rotation to decelerate as it approaches the target. Uses the same sigmoid function as the Sigmoid angle smooth mode.

| Setting | Type | Default | Range | Description |
|---------|------|---------|-------|-------------|
| Steepness | Float | 10.0 | 0.0..20.0 | Controls how sharply the deceleration transitions. Higher values create a more abrupt slowdown near the target. |
| Midpoint | Float | 0.3 | 0.0..1.0 | The normalized distance at which deceleration is centered. |

#### AI *(combat-specific modules only)*

Uses a trained deep learning model to predict the next rotation delta each tick. The model takes as input the current and previous rotation direction vectors, the target direction vector, velocity deltas, player and target movement differences, hurt time, and distance. The raw model output (yaw and pitch deltas) is scaled by configurable multipliers and then optionally refined by a correction mode. If the deep learning engine is not available on the platform, it falls back to the Interpolation mode (or Linear if Interpolation is unavailable).

| Setting | Type | Default | Range | Description |
|---------|------|---------|-------|-------------|
| Model | Mode | — | — | Selects which trained model file to use for inference. Models are loaded from the deep learning model manager. |
| Correction | Mode | Interpolation | Interpolation / Linear / None | A secondary angle smooth applied after the model output to refine the result. Interpolation works best with the model. Linear is not recommended as it eliminates acceleration effects. None passes the model output directly. |

**OutputMultiplier** — Scales the raw model output before correction is applied.

| Setting | Type | Default | Range | Description |
|---------|------|---------|-------|-------------|
| Yaw | Float | 1.5 | 0.5..2.0 | Multiplier applied to the model's yaw delta output. |
| Pitch | Float | 1.0 | 0.5..2.0 | Multiplier applied to the model's pitch delta output. |

### ShortStop *(combat-specific modules only)*

ShortStop is a toggleable processor (default: off) that temporarily pauses rotation toward the target at a random rate. When triggered, the rotation nearly freezes for a short duration, only moving by a tiny amount (0.0–0.1 degrees per tick) toward the target. This simulates brief moments of hesitation or pause in human aim. After the duration expires, normal rotation resumes.

| Setting | Type | Default | Range | Description |
|---------|------|---------|-------|-------------|
| Rate | Integer | 3 | 1..25 (%) | The chance each tick that a short stop is triggered. |
| Duration | Integer Range | 1..2 | 1..5 (ticks) | How many ticks the rotation pause lasts. A random value within this range is chosen each time a short stop triggers. |

### Fail *(combat-specific modules only)*

Fail is a toggleable processor (default: off) that acts as a configurable miss rate. When triggered, it intentionally shifts the rotation away from the target for a short duration, simulating a player who occasionally misses. The shift is computed by taking a fraction of the difference between the previous and server rotations and adding a random angular offset. After the transition-in duration expires, normal aiming resumes until the next fail triggers.

| Setting | Type | Default | Range | Description |
|---------|------|---------|-------|-------------|
| Rate | Integer | 3 | 1..100 (%) | The chance each tick that a fail is triggered. |
| Factor | Float | 0.04 | 0.01..0.99 | Multiplier applied to the difference between the previous rotation and the server rotation. Higher values cause a larger drift away from the target during a fail. |
| StrengthHorizontal | Float Range | 5.0..10.0 | 1.0..90.0 (°) | The random yaw offset added during a fail. A random value in this range is chosen, with a random sign (left or right). |
| StrengthVertical | Float Range | 0.0..2.0 | 0.0..90.0 (°) | The random pitch offset added during a fail. A random value in this range is chosen, with a random sign (up or down). |
| TransitionInDuration | Integer Range | 1..4 | 0..20 (ticks) | How many ticks the fail state lasts after being triggered. A random value within this range is chosen each time. |

### MovementCorrection

MovementCorrection determines how the player's movement input is adjusted when the server-side rotation (where the server thinks the player is looking) differs from the client-side camera direction.

**Off** — No movement correction is applied. The player moves exactly as they press the keys relative to their client-side view. This feels the most natural since movement and sprinting are unaffected, but it can be detected by anti-cheats because the movement direction will not match the server-side head rotation.

**Strict** — Corrects movement by changing the yaw used for movement calculations to match the server-side rotation. This makes the player walk in the direction the server thinks they are facing, which is fully legitimate but can feel disorienting since pressing forward may not move the player in the direction they see on screen.

**Silent** — Corrects movement using the server-side yaw like Strict, but also adjusts the keyboard input values to prevent the player's walk direction from changing aggressively. This produces a smoother correction that is less noticeable to the player while still matching server expectations.

**ChangeLook** — Corrects movement by actually changing the player's client-side look direction to match the server-side rotation. The player's camera visually snaps to where the server thinks they are looking. This is the most visually intrusive option but ensures perfect consistency between client and server.

---
*Last updated: 2026-02-13*
