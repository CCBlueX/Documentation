## SmartEat

SmartEat automatically manages food consumption so you can focus on playing without manually swapping items. It has two complementary systems: **AutoEat** silently selects and eats a food item whenever your hunger bar drops too low, and **SilentOffhand** lets you right-click to eat while holding a tool — without visibly changing your hotbar slot on your own screen or the server's.

The module is also smart about *what* it eats. Rather than blindly picking the nearest food, it prioritises high-value items when your health is critically low. Enchanted golden apples (Notch apples) are preferred below one threshold, golden apples below another, and instant-health potions below a third. Outside those thresholds it falls back to regular food, choosing whichever option restores the most hunger. This tiered priority system can make the difference in a tough combat scenario where every half-heart counts.

SmartEat integrates with the combat management system so eating does not interfere with your fighting rhythm. The **NotDuringCombat** toggle prevents any eating while you are actively in combat, and **CombatPauseTime** briefly suspends combat tracking each time a food item is consumed. For a fuller automated survival setup, consider pairing SmartEat with [AutoBuff](/docs/modules/player/autobuff) or [AutoArmor](/docs/modules/combat/autoarmor).

**Category:** Player
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| SwapBackDelay | Integer | 5 | 1–20 | Number of ticks to wait before silently returning the hotbar selection to your original slot after eating. |
| PreferGappleHealthThreshold | Decimal | 9.0 | 0.0–20.0 | Health (in half-hearts) at or below which golden apples are preferred over ordinary food. |
| PreferNotchAppleHealthThreshold | Decimal | 2.0 | 0.0–20.0 | Health (in half-hearts) at or below which enchanted golden apples are preferred over other food. |
| PreferHealthPotHealthThreshold | Decimal | 12.0 | 0.0–20.0 | Health (in half-hearts) at or below which instant-health potions are preferred over food. |
| CombatPauseTime | Integer | 0 | 0–40 ticks | How long to pause combat tracking (in ticks) each time SmartEat begins consuming an item. |
| NotDuringCombat | Toggle | false | — | When enabled, SmartEat will not eat or swap food while you are in active combat. |
| SilentOffhand | Toggleable Group | On | — | When you right-click while holding a tool, silently swaps the best food item into your hand server-side so you can eat without interrupting your workflow. |
| SilentOffhand → RenderSlot | Toggleable Group | On | — | Renders a ghost offhand slot in the HUD showing which food item SmartEat would use next. |
| SilentOffhand → RenderSlot → Offset | Integer | 26 | 30–70 | Horizontal pixel offset for the ghost offhand slot indicator in the HUD. |
| AutoEat | Toggleable Group | On | — | Automatically eats the best available food item whenever your hunger drops below MinHunger. |
| AutoEat → MinHunger | Integer | 15 | 0–20 | Hunger level (out of 20) that triggers automatic eating. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/ModuleSmartEat.kt)*
