## SmartEat

SmartEat picks food from your hotbar and offhand and eats it for you. AutoEat eats when your hunger gets low. SilentOffhand lets you right-click with a tool in your hand to eat the best food without switching slots yourself.

When your health is low, it prefers golden apples, enchanted golden apples or healing potions, depending on the health thresholds below. Otherwise it eats the food that fills the most hunger. Health is counted in half hearts, so 20 is full health.

**Category:** Player
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| SwapBackDelay | Integer | 5 | 1..20 | Ticks (20 per second) to wait before switching back to your slot after eating. |
| PreferGappleHealthThreshold | Decimal | 9.0 | 0.0..20.0 | At or below this health, healing potions come before normal food. |
| PreferNotchAppleHealthThreshold | Decimal | 2.0 | 0.0..20.0 | At or below this health, enchanted golden apples come first. |
| PreferHealthPotHealthThreshold | Decimal | 12.0 | 0.0..20.0 | At or below this health, golden apples come before normal food. |
| CombatPauseTime | Integer | 0 | 0..40 ticks | Pauses combat modules for this long when SmartEat starts eating. |
| NotDuringCombat | Toggle | Off | | Does not eat while you are fighting. |
| SilentOffhand | Toggleable Group | On | | Right-click while holding a tool to eat the best food without changing your slot. |
| SilentOffhand → RenderSlot | Toggleable Group | On | | Shows the food that would be eaten in an extra slot next to your hotbar. |
| SilentOffhand → RenderSlot → Offset | Integer | 40 | 30..70 | How far left of the hotbar that slot is drawn. |
| AutoEat | Toggleable Group | On | | Eats on its own when your hunger is low. |
| AutoEat → MinHunger | Integer | 15 | 0..20 | Starts eating when your hunger is below this (20 is full). |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/ModuleSmartEat.kt)*
