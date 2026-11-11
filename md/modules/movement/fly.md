## Fly

Fly lets you fly in survival mode. There are many modes. A few work anywhere the server doesn't check for flying (Vanilla, Creative, Jetpack and others), and the rest are made for one anti-cheat or server. Pick the mode made for the server you play on, because a mode made for one anti-cheat usually gets caught by another.

Many modes only fly for a short time or distance and then stop. With DisableOnSetback on, Fly turns off when the server pulls you back to where you were, which usually means you got caught. Use [NoFall](/docs/modules/player/nofall) so landing doesn't hurt you.

**Category:** Movement
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | Vanilla | Vanilla, Creative, Jetpack, Enderpearl, AirWalk, Explosion, Fireball, Vulcan-2.7.7, Vulcan-2.8.6-MC1.13, Vulcan-2.8.6-MC1.8, Vulcan-2.8.6-Teleport-MC1.8, Grim-2.3.59, Grim-2.3.73, Spartan-Phase524, CubeCraft-2024-04-20, CubeCraft-2024-01-27, CubeCraft-2024-03-10, CubeCraft-2025-12-26, Verus-b3896-Damage, Verus-b3896-Flat, NcpClip, Hypixel, HypixelFlat, HycraftDamage | How you fly. Modes not listed below have no settings. |
| Mode → [Vanilla] → Glide | Decimal | 0.0 | -1.0..1.0 | How fast you move up or down when you don't press jump or sneak. Negative sinks, positive rises. |
| Mode → [Vanilla] → BypassVanillaCheck | Toggle | true |  | Moves you down a little now and then so the server doesn't kick you for flying. |
| Mode → [Vanilla] → BaseSpeed | Setting Group |  |  | Normal flying speed. |
| Mode → [Vanilla] → BaseSpeed → Horizontal | Decimal | 0.44 | 0.1..10.0 | Speed forward and sideways. |
| Mode → [Vanilla] → BaseSpeed → Vertical | Decimal | 0.44 | 0.1..10.0 | Speed up and down. |
| Mode → [Vanilla] → SprintSpeed | Toggleable Group | On |  | Use other speeds while you sprint. |
| Mode → [Vanilla] → SprintSpeed → Horizontal | Decimal | 1.0 | 0.1..10.0 | Speed forward and sideways while sprinting. |
| Mode → [Vanilla] → SprintSpeed → Vertical | Decimal | 1.0 | 0.1..10.0 | Speed up and down while sprinting. |
| Mode → [Creative] → Speed | Decimal | 0.1 | 0.1..5.0 | Flying speed, like in Creative mode. |
| Mode → [Creative] → SprintSpeed | Toggleable Group | On |  | Use another speed while you sprint. |
| Mode → [Creative] → SprintSpeed → Speed | Decimal | 0.1 | 0.1..5.0 | Flying speed while sprinting. |
| Mode → [Creative] → MaxVelocity | Decimal | 4.0 | 1.0..20.0 | The fastest you can go. |
| Mode → [Creative] → BypassVanillaCheck | Toggle | true |  | Moves you down a little now and then so the server doesn't kick you for flying. |
| Mode → [Creative] → ForceFlight | Toggle | true |  | Keep flying turned on. |
| Mode → [Enderpearl] → Speed | Decimal | 1.0 | 0.5..2.0 | Flying speed after your ender pearl lands. |
| Mode → [Enderpearl] → Rotations | Setting Group |  |  | See [Shared: Rotations](/docs/modules/shared-settings/rotations). |
| Mode → [AirWalk] → OnGround | Toggle | true |  | Tell the server you stand on the ground while you walk on air. |
| Mode → [Explosion] → Vertical | Decimal | 4.0 | 0.0..10.0 | How much an explosion pushes you up. You need to get hit by an explosion first. |
| Mode → [Explosion] → StartStrafe | Decimal | 1.0 | 0.6..4.0 | How fast you go forward right after the explosion. |
| Mode → [Explosion] → StrafeDecrease | Decimal | 0.005 | 0.001..0.1 | How fast that speed goes away. |
| Mode → [Fireball] → Technique | Mode Selector | Legit | Legit, Custom | How the fireball gets thrown. You need fire charges in your hotbar or offhand. |
| Mode → [Fireball] → Technique → [Legit] → Jump | Toggleable Group | On |  | Jump before throwing. |
| Mode → [Fireball] → Technique → [Legit] → Jump → Delay | Integer | 3 | 0..20 ticks | Ticks (20 per second) to wait before jumping. |
| Mode → [Fireball] → Technique → [Legit] → Sprint | Toggle | true |  | Sprint after the throw. |
| Mode → [Fireball] → Technique → [Legit] → StopMove | Toggle | true |  | Stop walking while it works, so you don't fall off edges. |
| Mode → [Fireball] → Technique → [Legit] → Rotations | Setting Group |  |  | See [Shared: Rotations](/docs/modules/shared-settings/rotations). |
| Mode → [Fireball] → Technique → [Legit] → Rotations → Pitch | Decimal | 90.0 | 0.0..90.0 | How far down you look when throwing. |
| Mode → [Fireball] → Technique → [Legit] → Rotations → Backwards | Toggle | true |  | Look backwards when throwing. |
| Mode → [Fireball] → Technique → [Custom] → DisableDelay | Integer | 10 | 0..20 | Ticks to wait after the throw before Fly turns off. |
| Mode → [Fireball] → Technique → [Custom] → ThrowDelay | Integer | 2 | 0..20 | Ticks to wait before throwing. |
| Mode → [Fireball] → Technique → [Custom] → Jump | Toggleable Group | On |  | Jump before throwing. |
| Mode → [Fireball] → Technique → [Custom] → Jump → JumpDelay | Integer | 1 | 0..20 ticks | Ticks to wait before jumping. |
| Mode → [Fireball] → Technique → [Custom] → YVelocity | Toggleable Group | On |  | Set your upward speed after the throw. |
| Mode → [Fireball] → Technique → [Custom] → YVelocity → Velocity | Decimal | 0.0 | -5.0..5.0 | The upward speed to set. |
| Mode → [Fireball] → Technique → [Custom] → YVelocity → Delay | Integer | 0 | 0..20 ticks | Ticks to wait before setting it. |
| Mode → [Fireball] → Technique → [Custom] → Sprint | Toggle | true |  | Sprint after the throw. |
| Mode → [Fireball] → Technique → [Custom] → StopMove | Toggle | true |  | Stop walking while it works, so you don't fall off edges. |
| Mode → [Fireball] → Technique → [Custom] → Rotations | Setting Group |  |  | See [Shared: Rotations](/docs/modules/shared-settings/rotations). |
| Mode → [Fireball] → Technique → [Custom] → Rotations → Pitch | Decimal | 90.0 | 0.0..90.0 | How far down you look when throwing. |
| Mode → [Fireball] → Trigger | Mode Selector | Instant | Instant, OnEdge | When to throw. Instant throws right away, OnEdge waits until you reach the edge of a block. |
| Mode → [Fireball] → Trigger → [OnEdge] → EdgeDistance | Decimal | 0.01 | 0.01..0.5 | How close to the edge you need to be. |
| Mode → [Fireball] → SlotResetDelay | Integer Range | 4..6 | 0..40 ticks | Ticks before your held item switches back after the throw. |
| Mode → [Vulcan-2.8.6-MC1.8] → Timer | Decimal | 2.5 | 1.0..2.5 | How much faster the game runs for you. |
| Mode → [Vulcan-2.8.6-MC1.8] → AutoDisable | Toggle | false |  | Turn Fly off when it stops working. |
| Mode → [Grim-2.3.59] → Toggle | Integer | 0 | 0..100 | Turn Fly off after this many ticks. 0 means never. |
| Mode → [Grim-2.3.59] → Timer | Decimal | 0.446 | 0.1..1.0 | How fast the game runs for you. Below 1 is slower. |
| Mode → [Grim-2.3.73] → AutoLagInAir | Toggle | true |  | Start by itself after you have been in the air for a moment. |
| Mode → [Grim-2.3.73] → AirTick | Integer | 3 | 0..12 ticks | How long you need to be in the air first. |
| Mode → [CubeCraft-2024-04-20] → HorizontalSpeed | Decimal | 3.5 | 0.1..10.0 | Speed forward. |
| Mode → [CubeCraft-2024-04-20] → ConstantSpeed | Toggle | false |  | Keep that speed the whole time. |
| Mode → [CubeCraft-2024-04-20] → VerticalSpeed | Decimal | 0.7 | 0.1..1.0 | Speed up and down when you hold jump or sneak. |
| Mode → [CubeCraft-2024-04-20] → ReboostTicks | Integer | 30 | 10..50 | Ticks between boosts. |
| Mode → [CubeCraft-2024-04-20] → BoostOnce | Toggle | false |  | Boost only once. |
| Mode → [CubeCraft-2024-04-20] → Nostalgia | Toggle | false |  | Also move you up a little on each boost. |
| Mode → [CubeCraft-2024-01-27] → HorizontalSpeed | Decimal Range | 0.33..0.34 | 0.1..1.0 | Speed forward, picked at random from this range. |
| Mode → [CubeCraft-2024-03-10] → Height | Decimal | 0.42 | 0.1..1.0 | How high each boost pushes you. |
| Mode → [CubeCraft-2024-03-10] → Speed | Decimal | 0.35 | 0.1..1.0 | Speed forward. |
| Mode → [CubeCraft-2024-03-10] → Ticks | Integer | 11 | 1..20 | Ticks between boosts. |
| Mode → [CubeCraft-2025-12-26] → HorizontalSpeed | Decimal | 3.5 | 0.1..10.0 | Speed forward. |
| Mode → [CubeCraft-2025-12-26] → VerticalSpeed | Decimal | 0.7 | 0.1..5.0 | Speed up and down when you hold jump or sneak. |
| Mode → [CubeCraft-2025-12-26] → Ticks | Integer | 20 | 10..50 | How long the flight lasts, in ticks. |
| Mode → [CubeCraft-2025-12-26] → Timer | Decimal | 0.5 | 0.1..1.0 | How fast the game runs for you. Below 1 is slower. |
| Mode → [CubeCraft-2025-12-26] → Nostalgia | Toggle | false |  | Also move you up a little on each boost. |
| Mode → [Verus-b3896-Flat] → Timer | Decimal | 5.0 | 1.0..20.0 | How much faster the game runs for you. |
| Mode → [NcpClip] → Speed | Decimal | 7.5 | 2.0..10.0 | Speed forward. |
| Mode → [NcpClip] → AdditionalEntry | Decimal | 2.0 | 0.0..2.0 | Extra speed at the start. |
| Mode → [NcpClip] → Timer | Decimal | 0.4 | 0.1..1.0 | How fast the game runs for you. Below 1 is slower. |
| Mode → [NcpClip] → Strafe | Toggle | true |  | Let you steer while flying. |
| Mode → [NcpClip] → Clipping | Decimal | -0.5 | -1.0..1.0 | How far up or down you get moved at the start. Negative is down. |
| Mode → [NcpClip] → Blink | Toggle | false |  | Hold back your movement from the server while flying. |
| Mode → [NcpClip] → FallDamage | Toggle | false |  | Take fall damage first. |
| Mode → [NcpClip] → MaximumDistance | Decimal | 200.0 | 0.1..500.0 | Turn Fly off after this many blocks. |
| Mode → [Hypixel] → Timer | Decimal | 1.0 | 0.1..1.0 | How fast the game runs for you. Below 1 is slower. |
| Mode → [HypixelFlat] → Timer | Decimal | 1.0 | 0.1..1.0 | How fast the game runs for you. Below 1 is slower. |
| Mode → [HypixelFlat] → Speed | Decimal | 1.66 | 0.8..2.0 | Speed forward. |
| Visuals | Toggleable Group | On |  | Changes how your flying looks. |
| Visuals → Stride | Toggle | true |  | Keep the walking animation small while you fly. |
| DisableOnSetback | Toggle | false |  | Turn Fly off when the server pulls you back. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/fly/ModuleFly.kt)*
