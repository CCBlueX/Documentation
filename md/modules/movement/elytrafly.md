## ElytraFly

ElytraFly takes the fiddliness out of elytra flight. Instead of relying on fireworks and careful pitch control, it lets you steer smoothly, hold your altitude, climb, and dive using simple key inputs. It only kicks in when you're actually wearing an elytra (and not in Creative or under Levitation), so you can leave it bound and forget about it until you take off.

Pick a **Mode** to decide how flight feels: *Vanilla* and *Static* give you straightforward, controllable gliding; *Boost* adds momentum, dive-and-pull-up speed, and ground-aware handling; *Firework* automatically fires rockets for you as you fly; and *Pitch40Infinite* automatically oscillates your pitch to keep you airborne indefinitely. The **Speed** group sets how much vertical and horizontal control you get in the modes that use it.

Handy extras include **Instant**, which can auto-start a glide the moment you jump and stop it again when you crouch on the ground, and **DurabilityExploit**, which rapidly re-triggers gliding to avoid spending elytra durability. If you want to swap into an elytra automatically, pair this with [ElytraSwap](/docs/modules/player/elytraswap), and see [ExtendedFirework](/docs/modules/movement/extendedfirework) for more firework-focused flight.

**Category:** Movement
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Instant | Multi-Select | [Stop] | — | When to automatically begin or end a glide: *Start* launches you when you jump, *Stop* lands you when you crouch on the ground. |
| NotInFluid | Toggle | false | — | Automatically stops gliding when you enter water or other liquids. |
| DurabilityExploit | Toggle | false | — | Constantly re-triggers gliding so the elytra never actually wears down, saving durability. |
| Speed | Toggleable Group | On | — | Controls how fast you move while flying. |
| Speed → Vertical | Decimal | 0.5 | 0.0..5.0 | How fast you climb or descend when holding jump or crouch. |
| Speed → Horizontal | Decimal | 1.0 | 0.0..8.0 | How fast you move forward while flying. |
| Mode | Mode Selector | Vanilla | Static, Vanilla, Boost, Firework, Pitch40Infinite | Chooses the overall flight behavior and handling style. |
| Mode → [Static] → DurabilityExploitNotWhileNoMove | Toggle | false | — | Only runs the durability exploit while you're standing still, which can avoid detection on some servers. |
| Mode → [Static] → Glide | Toggleable Group | Off | — | Adds a gentle drifting glide while you aren't actively moving, helping avoid "flying is not enabled" kicks. |
| Mode → [Static] → Glide → Vertical | Decimal | 0.01 | 0.0..1.0 | How quickly you sink during the idle glide. |
| Mode → [Static] → Glide → Horizontal | Decimal | 0.0 | 0.0..1.0 | How much you drift forward during the idle glide. |
| Mode → [Boost] → Speed | Decimal | 0.9 | 0.5..2.0 | The maximum boost speed this mode builds up to. |
| Mode → [Boost] → Acceleration | Decimal | 0.01 | 0.005..0.05 | How quickly the boost ramps up and bleeds off. |
| Mode → [Boost] → AutoBoost | Toggle | true | — | Automatically boosts when you angle upward, without needing to hold jump. |
| Mode → [Boost] → VerticalControl | Decimal | 0.8 | 0.2..1.0 | How strongly jump and crouch raise or lower you. |
| Mode → [Boost] → SmartGroundBehavior | Toggle | true | — | Adjusts handling when you fly close to the ground for safer low passes. |
| Mode → [Boost] → GroundDistance | Decimal | 3.0 | 1.5..7.0 | How close to the ground counts as "near ground" for the smart behavior. |
| Mode → [Boost] → DiveMechanics | Toggle | true | — | Builds up speed while diving that carries into a faster pull-up. |
| Mode → [Boost] → DiveAcceleration | Decimal | 0.05 | 0.01..0.1 | How quickly dive speed accumulates while pointing down. |
| Mode → [Boost] → DiveEfficiency | Decimal | 0.8 | 0.4..1.5 | How much of your built-up dive speed converts into a boost on pull-up. |
| Mode → [Firework] → ConsiderInventory | Toggleable Group | Off | — | Also pulls fireworks from your main inventory, not just the hotbar and offhand. |
| Mode → [Firework] → ConsiderInventory → Constraints | Setting Group | — | — | See [Shared: Inventory Constraints](/docs/modules/shared-settings/inventory-constraints). |
| Mode → [Firework] → Cooldown | Integer Range | 20..20 ticks | 0..300 | How long to wait between automatically firing rockets, picked randomly within this range. |
| Mode → [Pitch40Infinite] → MinSpeed | Decimal | 25.0 | 10.0..70.0 | Speed (km/h) below which the mode tilts up to gain height again. |
| Mode → [Pitch40Infinite] → MaxSpeed | Decimal | 150.0 | 50.0..170.0 | Speed (km/h) above which the mode tilts down to keep diving. |
| Mode → [Pitch40Infinite] → MaxHeight | Integer | 200 | 50..360 | Altitude the mode tries to stay under; flying lower triggers a low-altitude warning. |
| Mode → [Pitch40Infinite] → PitchIncrement | Decimal | 3.0 | 1.0..10.0 | How sharply the pitch swings each tick while oscillating. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/elytrafly/ModuleElytraFly.kt)*
