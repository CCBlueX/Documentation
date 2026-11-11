## AutoBuff

AutoBuff eats, drinks or throws healing and buff items for you when you need them: soup, player heads, splash potions, normal potions and golden apples. It is useful on PvP servers like Kit-PvP or UHC, where you have no time to switch items by hand.

Each item type has its own on/off switch. Soup, heads and golden apples are used when your health gets low. Potions are used when you are missing their effect. For filling your hunger bar, use [SmartEat](/docs/modules/player/smarteat) instead.

**Category:** Player
**Enabled by default:** No

### Settings

Some settings are in ticks (20 per second).

| Setting | Type | Default | Range | Description |
| --- | --- | --- | --- | --- |
| Soup | Toggleable Group | On | | Eats mushroom stew when your health is low. |
| Soup → Health | Integer | 40 | 1..100 %HP | Health (in percent) at or below which it eats soup. |
| Soup → ConsiderAbsorption | Toggle | true | | Counts yellow hearts as health. |
| Soup → AfterUse | Mode Selector | Drop | None, Drop, Stack | What to do with the empty bowl: leave it, drop it, or move it out of the hotbar so the bowls stack in your inventory. Bowls in your offhand are left alone. |
| Soup → AfterUse → [Drop/Stack] → AssumeEmptyBowl | Toggle | true | | Treats the slot as an empty bowl without checking it. |
| Soup → AfterUse → [Drop/Stack] → Wait | Integer Range | 1..2 | 1..20 ticks | Wait before dropping or moving the bowl. |
| Soup → AfterUse → [Stack] → IgnoreInventoryFull | Toggle | true | | Moves the bowl even when your inventory looks full. |
| Soup → AfterUse → [Stack] → Constraints | Setting Group | | | See [Shared: Inventory Constraints](/docs/modules/shared-settings/inventory-constraints). |
| Head | Toggleable Group | On | | Eats a player head when your health is low. |
| Head → Health | Integer | 40 | 1..100 %HP | Health (in percent) at or below which it eats a head. |
| Head → ConsiderAbsorption | Toggle | true | | Counts yellow hearts as health. |
| Head → MaxAbsorption | Decimal | 1.0 | 0.0..8.0 | Only eats while you have this many yellow hearts or fewer. |
| Head → Cooldown | Decimal | 0.0 | 0.0..120.0 s | Time to wait between heads. |
| Pot | Toggleable Group | On | | Throws splash potions at your feet. |
| Pot → Potions | Setting Group | | | Effects it will throw potions for. |
| Pot → Potions → Health | Toggleable Group | On | | Instant Health when you are hurt. |
| Pot → Potions → Health → Health | Integer | 40 | 1..100 %HP | Health (in percent) at or below which it uses Instant Health. |
| Pot → Potions → Regen | Toggleable Group | On | | Regeneration when you are hurt and don't have it yet. |
| Pot → Potions → Regen → Health | Integer | 40 | 1..100 %HP | Health (in percent) at or below which it uses Regeneration. |
| Pot → Potions → Strength | Toggleable Group | On | | Strength when you don't have it. |
| Pot → Potions → Speed | Toggleable Group | On | | Speed when you don't have it. |
| Pot → Potions → FireResistance | Toggleable Group | On | | Fire Resistance when you don't have it. |
| Pot → Potions → JumpBoost | Toggleable Group | On | | Jump Boost when you don't have it. |
| Pot → Potions → WaterBreathing | Toggleable Group | On | | Water Breathing when you don't have it. |
| Pot → TillGroundDistance | Decimal | 2.0 | 1.0..5.0 | Only throws when the ground is this many blocks below you or closer. |
| Pot → DoNotBenefitOthers | Toggle | true | | Doesn't throw if an enemy nearby would get the effect too. |
| Pot → AllowLingering | Toggle | false | | Also uses lingering potions. |
| Drink | Toggleable Group | On | | Drinks normal potions. |
| Drink → Potions | Setting Group | | | Effects it will drink potions for. |
| Drink → Potions → Health | Toggleable Group | On | | Instant Health when you are hurt. |
| Drink → Potions → Health → Health | Integer | 40 | 1..100 %HP | Health (in percent) at or below which it uses Instant Health. |
| Drink → Potions → Regen | Toggleable Group | On | | Regeneration when you are hurt and don't have it yet. |
| Drink → Potions → Regen → Health | Integer | 40 | 1..100 %HP | Health (in percent) at or below which it uses Regeneration. |
| Drink → Potions → Strength | Toggleable Group | On | | Strength when you don't have it. |
| Drink → Potions → Speed | Toggleable Group | On | | Speed when you don't have it. |
| Drink → Potions → FireResistance | Toggleable Group | On | | Fire Resistance when you don't have it. |
| Drink → Potions → JumpBoost | Toggleable Group | On | | Jump Boost when you don't have it. |
| Drink → Potions → WaterBreathing | Toggleable Group | On | | Water Breathing when you don't have it. |
| Gapple | Toggleable Group | On | | Eats a golden apple when your health is low. |
| Gapple → Health | Integer | 40 | 1..100 %HP | Health (in percent) at or below which it eats an apple. |
| Gapple → ConsiderAbsorption | Toggle | true | | Counts yellow hearts as health. |
| Gapple → Enchanted | Toggle | true | | Also eats enchanted golden apples. |
| AutoSwap | Toggleable Group | On | | Switches to the item in your hotbar, uses it, then switches back. |
| AutoSwap → DelayIn | Integer Range | 1..1 | 0..20 ticks | Wait after switching before using the item. |
| AutoSwap → DelayOut | Integer Range | 1..1 | 0..20 ticks | Wait after using the item before switching back. |
| Refill | Toggleable Group | On | | Moves buff items from your inventory into the hotbar. |
| Refill → Constraints | Setting Group | | | See [Shared: Inventory Constraints](/docs/modules/shared-settings/inventory-constraints). |
| Rotations | Setting Group | | | Used for aiming splash potions. See [Shared: Rotations](/docs/modules/shared-settings/rotations). |
| Rotations → RotationTiming | Choice | Normal | Normal, OnTick, OnUse | When to look down for a throw. Normal turns your view first and waits, OnTick and OnUse only aim at the moment of the throw. |
| CombatPauseTime | Integer | 0 | 0..40 ticks | How long to pause attacking after using a buff. |
| NotDuringCombat | Toggle | false | | Doesn't use buffs while you are fighting. |
| IgnoreOpenInventory | Toggle | false | | Keeps using buffs while your inventory is open. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/autobuff/ModuleAutoBuff.kt)*
