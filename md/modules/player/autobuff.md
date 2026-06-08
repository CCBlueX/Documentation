## AutoBuff

AutoBuff keeps you topped up by automatically using or throwing buff items the moment you need them — healing soups, golden apples, enchanted player heads, and potions. Turn on the buff types you want, and it watches your health and surroundings, then drinks, eats, or splashes the right item for the situation without you having to manage your hotbar.

Each buff type is its own toggle with its own trigger conditions. Health-based buffs (Soup, Head, Gapple) only fire once your health drops to the threshold you set, while the potion options (Pot, Drink) react to which effects you're missing. When the needed item isn't in your hotbar, [AutoSwap](#) can silently switch to it, and Refill can quick-move spare buff items up from your main inventory so you never run dry mid-fight.

Use it on Kit-PvP, UHC, or survival servers where staying buffed is the difference in a fight. If you'd rather it back off while you're trading hits, the CombatPauseTime and NotDuringCombat options let you hold buffs until combat settles. For automatic eating to fill your hunger bar instead, see [SmartEat](/docs/modules/player/smarteat).

**Category:** Player
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
| --- | --- | --- | --- | --- |
| Soup | Toggleable Group | Off | — | Heals you by eating mushroom stew when your health is low. |
| Soup → Health | Integer | 40 | 1..100 %HP | Trigger soup once health falls to this percent of your max. |
| Soup → ConsiderAbsorption | Toggle | true | — | Counts absorption (yellow) hearts toward your health when deciding whether to eat. |
| Soup → DropAfterUse | Toggleable Group | On | — | Drops the empty bowl after eating so it doesn't clutter your slot. |
| Soup → DropAfterUse → AssumeEmptyBowl | Toggle | true | — | Drops right away assuming the bowl is now empty, instead of waiting to confirm. |
| Soup → DropAfterUse → Wait | Integer Range | 1..2 | 1..20 ticks | Random delay before dropping the bowl. |
| Head | Toggleable Group | Off | — | Eats a player head for instant healing when your health is low. |
| Head → Health | Integer | 40 | 1..100 %HP | Trigger the head once health falls to this percent of your max. |
| Head → ConsiderAbsorption | Toggle | true | — | Counts absorption (yellow) hearts toward your health when deciding whether to eat. |
| Head → MaxAbsorption | Decimal | 1.0 | 0.0..8.0 | Only eats while your current absorption is at or below this amount. |
| Head → Cooldown | Decimal | 0.0 | 0.0..120.0 s | Minimum wait between eating heads. |
| Pot | Toggleable Group | On | — | Throws splash potions at your feet to apply missing beneficial effects. |
| Pot → Potions | Setting Group | — | — | Choose which effects AutoBuff will splash for. |
| Pot → Potions → Health | Toggleable Group | On | — | Splashes Instant Health when you're hurt. |
| Pot → Potions → Health → Health | Integer | 40 | 1..100 %HP | Trigger a health splash once health falls to this percent of your max. |
| Pot → Potions → Regen | Toggleable Group | On | — | Splashes Regeneration when you're hurt and don't have it. |
| Pot → Potions → Regen → Health | Integer | 40 | 1..100 %HP | Trigger a regen splash once health falls to this percent of your max. |
| Pot → Potions → Strength | Toggleable Group | On | — | Splashes Strength when you don't have the effect. |
| Pot → Potions → Speed | Toggleable Group | On | — | Splashes Speed when you don't have the effect. |
| Pot → Potions → FireResistance | Toggleable Group | On | — | Splashes Fire Resistance when you don't have the effect. |
| Pot → Potions → JumpBoost | Toggleable Group | On | — | Splashes Jump Boost when you don't have the effect. |
| Pot → Potions → WaterBreathing | Toggleable Group | On | — | Splashes Water Breathing when you don't have the effect. |
| Pot → TillGroundDistance | Decimal | 2.0 | 1.0..5.0 | Only throws when you're within this many blocks of the ground, so the splash lands on you. |
| Pot → DoNotBenefitOthers | Toggle | false | — | Holds the throw if a nearby enemy would also catch the effect. |
| Pot → AllowLingering | Toggle | false | — | Also allows lingering potions, not just splash potions. |
| Drink | Toggleable Group | Off | — | Drinks regular (non-splash) potions to apply missing beneficial effects. |
| Drink → Potions | Setting Group | — | — | Choose which effects AutoBuff will drink for. |
| Drink → Potions → Health | Toggleable Group | On | — | Drinks an Instant Health potion when you're hurt. |
| Drink → Potions → Health → Health | Integer | 40 | 1..100 %HP | Trigger a health drink once health falls to this percent of your max. |
| Drink → Potions → Regen | Toggleable Group | On | — | Drinks a Regeneration potion when you're hurt and don't have it. |
| Drink → Potions → Regen → Health | Integer | 40 | 1..100 %HP | Trigger a regen drink once health falls to this percent of your max. |
| Drink → Potions → Strength | Toggleable Group | On | — | Drinks a Strength potion when you don't have the effect. |
| Drink → Potions → Speed | Toggleable Group | On | — | Drinks a Speed potion when you don't have the effect. |
| Drink → Potions → FireResistance | Toggleable Group | On | — | Drinks a Fire Resistance potion when you don't have the effect. |
| Drink → Potions → JumpBoost | Toggleable Group | On | — | Drinks a Jump Boost potion when you don't have the effect. |
| Drink → Potions → WaterBreathing | Toggleable Group | On | — | Drinks a Water Breathing potion when you don't have the effect. |
| Gapple | Toggleable Group | Off | — | Eats a golden apple when your health is low. |
| Gapple → Health | Integer | 40 | 1..100 %HP | Trigger the apple once health falls to this percent of your max. |
| Gapple → ConsiderAbsorption | Toggle | true | — | Counts absorption (yellow) hearts toward your health when deciding whether to eat. |
| Gapple → Enchanted | Toggle | true | — | Also allows enchanted golden apples, not just regular ones. |
| AutoSwap | Toggleable Group | Off | — | Silently switches to the needed buff item if it isn't already selected, then switches back. |
| AutoSwap → DelayIn | Integer Range | 1..1 | 0..20 ticks | Random wait after swapping to the item before using it. |
| AutoSwap → DelayOut | Integer Range | 1..1 | 0..20 ticks | Random wait after using the item before swapping back. |
| Refill | Toggleable Group | On | — | Moves spare buff items from your inventory into the hotbar to keep you stocked. |
| Refill → Constraints | Setting Group | — | — | See [Shared: Inventory Constraints](/docs/modules/shared-settings/inventory-constraints). |
| Rotations | Setting Group | — | — | See [Shared: Rotations](/docs/modules/shared-settings/rotations). |
| CombatPauseTime | Integer | 2 | 0..40 ticks | Pauses combat actions for this long when a buff is used. |
| NotDuringCombat | Toggle | false | — | Stops buffing entirely while you're in combat. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/autobuff/ModuleAutoBuff.kt)*
