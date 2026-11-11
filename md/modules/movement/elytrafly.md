## ElytraFly

ElytraFly makes elytra flying easy to control. You can fly up, down and forward with your movement keys, without fireworks. It only works while you wear an elytra, and not in Creative or with Levitation.

The mode decides how flying feels. Static and Vanilla give simple, steady control. Boost builds up speed over time and lets you dive to go faster. Firework uses rockets for you. Pitch40Infinite tilts your view up and down by itself so you can keep flying for a long time. To put on an elytra by itself, use [ElytraSwap](/docs/modules/player/elytraswap).

**Category:** Movement
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Instant | Multi-Select | [Stop] | Start, Stop | Start: open the elytra as soon as you jump. Stop: stop gliding when you sneak on the ground. |
| NotInFluid | Toggle | false |  | Stop gliding when you are in water or lava. |
| DurabilityExploit | Toggle | false |  | Keeps restarting the glide so your elytra doesn't lose durability. |
| Speed | Toggleable Group | On |  | Sets how fast you fly in the modes that use it. |
| Speed → Vertical | Decimal | 0.5 | 0.0..5.0 | How fast you go up or down when you hold jump or sneak. |
| Speed → Horizontal | Decimal | 1.0 | 0.0..8.0 | How fast you fly forward. |
| Mode | Mode Selector | Static | Static, Vanilla, Boost, Firework, Pitch40Infinite | How flying works. |
| Mode → [Static] → DurabilityExploitNotWhileNoMove | Toggle | false |  | Only use DurabilityExploit while you stand still in the air. |
| Mode → [Static] → Glide | Toggleable Group | Off |  | Drift slowly while you don't press any keys. |
| Mode → [Static] → Glide → Vertical | Decimal | 0.01 | 0.0..1.0 | How fast you sink while drifting. |
| Mode → [Static] → Glide → Horizontal | Decimal | 0.0 | 0.0..1.0 | How fast you move forward while drifting. |
| Mode → [Boost] → Speed | Decimal | 0.9 | 0.5..2.0 | The top speed Boost builds up to. |
| Mode → [Boost] → Acceleration | Decimal | 0.01 | 0.005..0.05 | How fast you speed up and slow down. |
| Mode → [Boost] → AutoBoost | Toggle | true |  | Boost by itself, without holding jump. |
| Mode → [Boost] → VerticalControl | Decimal | 0.8 | 0.2..1.0 | How strongly jump and sneak move you up and down. |
| Mode → [Boost] → SmartGroundBehavior | Toggle | true |  | Fly more carefully when you are close to the ground. |
| Mode → [Boost] → GroundDistance | Decimal | 3.0 | 1.5..7.0 | How many blocks above the ground count as close. |
| Mode → [Boost] → DiveMechanics | Toggle | true |  | Gain speed while you dive and keep it when you pull up. |
| Mode → [Boost] → DiveAcceleration | Decimal | 0.05 | 0.01..0.1 | How fast you gain speed while diving. |
| Mode → [Boost] → DiveEfficiency | Decimal | 0.8 | 0.4..1.5 | How much of the dive speed you keep when you pull up. |
| Mode → [Firework] → ConsiderInventory | Toggleable Group | Off |  | Also take rockets from your inventory, not only from the hotbar and offhand. |
| Mode → [Firework] → ConsiderInventory → Constraints | Setting Group |  |  | See [Shared: Inventory Constraints](/docs/modules/shared-settings/inventory-constraints). |
| Mode → [Firework] → Cooldown | Integer Range | 20..20 | 0..300 ticks | Time between rockets, in ticks (20 per second). |
| Mode → [Pitch40Infinite] → MinSpeed | Decimal | 25.0 | 10.0..70.0 | Below this speed (km/h) it tilts up to climb. |
| Mode → [Pitch40Infinite] → MaxSpeed | Decimal | 150.0 | 50.0..170.0 | Above this speed (km/h) it tilts down again. |
| Mode → [Pitch40Infinite] → MaxHeight | Integer | 200 | 50..360 | The height it tries to stay below. |
| Mode → [Pitch40Infinite] → PitchIncrement | Decimal | 3.0 | 1.0..10.0 | How fast it tilts your view. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/elytrafly/ModuleElytraFly.kt)*
