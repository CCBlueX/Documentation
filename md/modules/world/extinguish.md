## Extinguish

Extinguish puts out fire on you by placing water at your feet. After that it can pick the water up again with an empty bucket.

You need a water bucket in your hotbar or offhand. It does nothing in the Nether, while you have Fire Resistance, and by default while you are fighting.

**Category:** World
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Cooldown | Decimal | 1.0 | 0.0..20.0 s | Shortest time between two uses. |
| NotDuringCombat | Toggle | true | | Doesn't place water while you are fighting. |
| Pickup | Toggleable Group | On | | Picks the water up again with an empty bucket. |
| Pickup → PickupSpan | Decimal Range | 0.1..10.0 | 0.0..20.0 s | How long after placing the water it may be picked up. |
| Rotations | Setting Group | | | See [Rotations](/docs/modules/shared-settings/rotations). |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/ModuleExtinguish.kt)*
