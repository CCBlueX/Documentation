## Extinguish

Extinguish keeps you from burning to death by automatically placing a water source at your feet the moment you catch fire. As soon as the flames go out, it scoops the water back up so you don't leave a puddle behind or flood the area. This makes it handy on servers where fire, lava splashes, or flint-and-steel traps are common.

To work, you need a water bucket in your hotbar or offhand (and an empty bucket if you want the water cleaned up afterward). The module aims at the placement spot for you, waits out a short cooldown between uses, and won't act if you already have Fire Resistance. Note that it can't place water in dimensions where water evaporates, such as the Nether.

By default it holds off while you're fighting, so it won't interrupt a clutch moment by swapping to a bucket — turn that off if you'd rather always douse the fire immediately.

**Category:** World
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
| --- | --- | --- | --- | --- |
| Cooldown | Decimal | 1.0s | 0.0–20.0s | Minimum delay between extinguish actions, preventing it from placing water too rapidly. |
| NotDuringCombat | Toggle | true | — | Stops the module from acting while you are in combat, so it won't interrupt a fight to grab a bucket. |
| Pickup | Toggleable Group | On | — | After extinguishing, automatically picks the water back up with an empty bucket. |
| Pickup → PickupSpan | Decimal Range | 0.1–10.0s | 0.0–20.0s | The time window after placement during which the water is eligible to be picked back up. |
| Rotations | Setting Group | — | — | See [Shared: Rotations](/docs/modules/shared-settings/rotations). |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/ModuleExtinguish.kt)*
