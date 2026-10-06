## Fly

Fly lets you move freely through the air in survival mode, where the game would normally keep you on the ground. Because flying is one of the most heavily watched-for cheats, Fly ships with a large list of **modes**: some are generic (Vanilla, Creative, Jetpack, Enderpearl, AirWalk, Explosion, Fireball), while most others are hand-tuned to slip past one specific anti-cheat or server — Vulcan, Grim, Spartan, Sentinel, Verus, NCP, Hypixel and Hycraft. Pick the mode that matches where you're playing: a mode built for one anti-cheat will usually flag instantly on another, so the right choice is more important than any single speed value.

Many of these modes rely on tricks like taking a hit, throwing an item, or desyncing your position, so they only fly for a limited time or distance before turning themselves off again. A few — such as Sentinel20thApr and NcpClip — work best with [PingSpoof](/docs/modules/exploit/pingspoof) enabled, and some will switch it on for you automatically. The Sentinel modes also disable [Speed](/docs/modules/movement/speed) while active to avoid conflicts. The Visuals group keeps your movement looking smooth to nearby players.

By default Fly turns itself off the instant the server drags you back to an earlier position (a "setback"), which is a common sign you've been caught — this stops you fighting an anti-cheat that's already onto you. Pair it with [NoFall](/docs/modules/player/nofall) so you don't take damage when you eventually land.

**Category:** Movement
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | HypixelFlat | Vanilla, Creative, Jetpack, Enderpearl, AirWalk, Explosion, Fireball, Vulcan277, Vulcan286-113, Vulcan286-18, Vulcan286-Teleport-18, Grim2859-V, Grim2373Jan15, Spartan524, Sentinel20thApr, Sentinel27thJan, Sentinel10thMar, Sentinel26thDec, VerusB3896Damage, VerusB3896Flat, NcpClip, Hypixel, HypixelFlat, HycraftDamage | Which flight method to use. Choose the one made for your server or anti-cheat. |
| Mode → [Vanilla] → Glide | Decimal | 0.0 | -1.0..1.0 | Vertical drift when you aren't pressing jump or sneak — negative sinks, positive rises. |
| Mode → [Vanilla] → BypassVanillaCheck | Toggle | false | — | Periodically nudges you downward to avoid the vanilla flight kick. |
| Mode → [Vanilla] → BaseSpeed | Setting Group | — | — | Base horizontal and vertical fly speed. |
| Mode → [Vanilla] → BaseSpeed → Horizontal | Decimal | 3.0 | 0.1..10.0 | Forward/sideways fly speed. |
| Mode → [Vanilla] → BaseSpeed → Vertical | Decimal | 2.93 | 0.1..10.0 | Up/down fly speed when ascending or descending. |
| Mode → [Vanilla] → SprintSpeed | Toggleable Group | On | — | Applies a different speed while holding sprint. |
| Mode → [Vanilla] → SprintSpeed → Horizontal | Decimal | 1.0 | 0.1..10.0 | Forward/sideways speed while sprinting. |
| Mode → [Vanilla] → SprintSpeed → Vertical | Decimal | 1.0 | 0.1..10.0 | Up/down speed while sprinting. |
| Mode → [Creative] → Speed | Decimal | 0.1 | 0.1..5.0 | Flight speed using creative-style abilities. |
| Mode → [Creative] → SprintSpeed | Toggleable Group | On | — | Uses a different speed while holding sprint. |
| Mode → [Creative] → SprintSpeed → Speed | Decimal | 0.1 | 0.1..5.0 | Flight speed while sprinting. |
| Mode → [Creative] → MaxVelocity | Decimal | 4.0 | 1.0..20.0 | Caps your overall movement speed. |
| Mode → [Creative] → BypassVanillaCheck | Toggle | true | — | Sends occasional downward movement to dodge the vanilla check. |
| Mode → [Creative] → ForceFlight | Toggle | true | — | Keeps the flying ability forced on. |
| Mode → [Enderpearl] → Speed | Decimal | 1.0 | 0.5..2.0 | Fly speed after the thrown pearl lands. |
| Mode → [Enderpearl] → Rotations | Setting Group | — | — | See [Shared: Rotations](/docs/modules/shared-settings/rotations). |
| Mode → [AirWalk] → OnGround | Toggle | false | — | Whether to tell the server you're on the ground while walking on air. |
| Mode → [Explosion] → Vertical | Decimal | 1.2 | 0.0..10.0 | Multiplies the upward velocity gained from explosion knockback. |
| Mode → [Explosion] → StartStrafe | Decimal | 1.0 | 0.6..4.0 | Initial horizontal boost right after the explosion. |
| Mode → [Explosion] → StrafeDecrease | Decimal | 0.01 | 0.001..0.1 | How quickly that horizontal boost fades each tick. |
| Mode → [Fireball] → Technique | Mode Selector | Custom | Legit, Custom | How the fireball launch is performed. |
| Mode → [Fireball] → Technique → [Legit] → Sprint | Toggle | true | — | Start sprinting after the fireball is thrown. |
| Mode → [Fireball] → Technique → [Legit] → StopMove | Toggle | false | — | Stops you walking while active so you don't fall off edges. |
| Mode → [Fireball] → Technique → [Legit] → Jump | Toggleable Group | On | — | Jump before launching. |
| Mode → [Fireball] → Technique → [Legit] → Jump → Delay | Integer | 0 | 0..20 ticks | Ticks to wait before jumping. |
| Mode → [Fireball] → Technique → [Legit] → Rotations | Setting Group | — | — | See [Shared: Rotations](/docs/modules/shared-settings/rotations). |
| Mode → [Fireball] → Technique → [Custom] → DisableDelay | Integer | 10 | 0..20 | Ticks to wait after the throw before turning Fly off. |
| Mode → [Fireball] → Technique → [Custom] → ThrowDelay | Integer | 1 | 0..20 | Ticks to wait before throwing the fireball. |
| Mode → [Fireball] → Technique → [Custom] → Sprint | Toggle | true | — | Start sprinting after the fireball is thrown. |
| Mode → [Fireball] → Technique → [Custom] → StopMove | Toggle | false | — | Stops you walking while active so you don't fall off edges. |
| Mode → [Fireball] → Technique → [Custom] → Jump | Toggleable Group | Off | — | Jump before launching. |
| Mode → [Fireball] → Technique → [Custom] → Jump → JumpDelay | Integer | 1 | 0..20 ticks | Ticks to wait before jumping. |
| Mode → [Fireball] → Technique → [Custom] → YVelocity | Toggleable Group | On | — | Applies a set vertical velocity after launching. |
| Mode → [Fireball] → Technique → [Custom] → YVelocity → Velocity | Decimal | 0.45 | -5.0..5.0 | Vertical velocity applied after launch. |
| Mode → [Fireball] → Technique → [Custom] → YVelocity → Delay | Integer | 5 | 0..20 ticks | Ticks to wait before applying that velocity. |
| Mode → [Fireball] → Technique → [Custom] → Rotations | Setting Group | — | — | See [Shared: Rotations](/docs/modules/shared-settings/rotations). |
| Mode → [Fireball] → Trigger | Mode Selector | Instant | Instant, OnEdge | When the fireball launch is triggered. |
| Mode → [Fireball] → Trigger → [OnEdge] → EdgeDistance | Decimal | 0.01 | 0.01..0.5 | How close to a block edge you must be before it triggers. |
| Mode → [Fireball] → SlotResetDelay | Integer Range | 4..6 | 0..40 ticks | Ticks before your hotbar slot is silently restored after grabbing the fireball. |
| Mode → [Vulcan286-18] → Timer | Decimal | 2.5 | 1.0..2.5 | Game-speed multiplier while desynced. |
| Mode → [Vulcan286-18] → AutoDisable | Toggle | false | — | Turn off automatically when the desync state breaks. |
| Mode → [Grim2859-V] → Toggle | Integer | 0 | 0..100 | Auto-disable after this many ticks (0 removes the limit). |
| Mode → [Grim2859-V] → Timer | Decimal | 0.446 | 0.1..1.0 | Game-speed multiplier during the boost. |
| Mode → [Grim2373Jan15] → AutoLagInAir | Toggle | true | — | Automatically start the fly once you've been airborne long enough. |
| Mode → [Grim2373Jan15] → AirTick | Integer | 3 | 0..12 ticks | Air time in ticks before it activates. |
| Mode → [Sentinel20thApr] → HorizontalSpeed | Decimal | 2.36 | 0.1..10.0 | Horizontal fly speed. |
| Mode → [Sentinel20thApr] → ConstantSpeed | Toggle | true | — | Keep applying the horizontal speed every tick. |
| Mode → [Sentinel20thApr] → VerticalSpeed | Decimal | 0.7 | 0.1..1.0 | Up/down speed when pressing jump or sneak. |
| Mode → [Sentinel20thApr] → ReboostTicks | Integer | 30 | 10..50 | Ticks between each re-boost. |
| Mode → [Sentinel20thApr] → BoostOnce | Toggle | false | — | Boost a single time, then turn off. |
| Mode → [Sentinel20thApr] → Nostalgia | Toggle | false | — | Adds a small upward teleport on boost (older behaviour). |
| Mode → [Sentinel27thJan] → HorizontalSpeed | Decimal Range | 0.33..0.34 | 0.1..1.0 | Random horizontal speed picked from this range each cycle. |
| Mode → [Sentinel10thMar] → Height | Decimal | 0.42 | 0.1..1.0 | Upward velocity applied each cycle. |
| Mode → [Sentinel10thMar] → Speed | Decimal | 0.35 | 0.1..1.0 | Horizontal speed. |
| Mode → [Sentinel10thMar] → Ticks | Integer | 11 | 1..20 | Ticks between each boost. |
| Mode → [Sentinel26thDec] → HorizontalSpeed | Decimal | 3.5 | 0.1..10.0 | Horizontal fly speed. |
| Mode → [Sentinel26thDec] → VerticalSpeed | Decimal | 0.7 | 0.1..5.0 | Up/down speed when pressing jump or sneak. |
| Mode → [Sentinel26thDec] → Ticks | Integer | 20 | 10..50 | How long the flight lasts before turning off. |
| Mode → [Sentinel26thDec] → Timer | Decimal | 0.5 | 0.1..1.0 | Game-speed multiplier during flight. |
| Mode → [Sentinel26thDec] → Nostalgia | Toggle | false | — | Adds a small upward teleport on boost (older behaviour). |
| Mode → [VerusB3896Flat] → Timer | Decimal | 5.0 | 1.0..20.0 | Game-speed multiplier while flat-flying. |
| Mode → [NcpClip] → Speed | Decimal | 7.5 | 2.0..10.0 | Horizontal fly speed. |
| Mode → [NcpClip] → AdditionalEntry | Decimal | 2.0 | 0.0..2.0 | Extra speed added to the initial launch. |
| Mode → [NcpClip] → Timer | Decimal | 0.4 | 0.1..1.0 | Game-speed multiplier during flight. |
| Mode → [NcpClip] → Strafe | Toggle | true | — | Allows steering while flying. |
| Mode → [NcpClip] → Clipping | Decimal | -0.5 | -1.0..1.0 | Vertical offset used to clip through the floor (negative goes down). |
| Mode → [NcpClip] → Blink | Toggle | false | — | Holds back packets so you can recover if something goes wrong. |
| Mode → [NcpClip] → FallDamage | Toggle | false | — | Take fall damage first, which some setups require. |
| Mode → [NcpClip] → MaximumDistance | Decimal | 60.0 | 0.1..500.0 | Auto-disable after travelling this many blocks. |
| Mode → [Hypixel] → Timer | Decimal | 0.73 | 0.1..1.0 | Game-speed multiplier during the flight. |
| Mode → [HypixelFlat] → Timer | Decimal | 1.0 | 0.1..1.0 | Game-speed multiplier during the flight. |
| Mode → [HypixelFlat] → Speed | Decimal | 1.66 | 0.8..2.0 | Horizontal fly speed. |
| Visuals | Toggleable Group | On | — | Visual tweaks that keep your flight looking natural to others. |
| Visuals → Stride | Toggle | true | — | Smooths your stride animation so movement appears normal. |
| DisableOnSetback | Toggle | true | — | Turns Fly off when the server teleports you back, a sign you've been flagged. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/fly/ModuleFly.kt)*
