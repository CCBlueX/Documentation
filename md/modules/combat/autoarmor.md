## AutoArmor

AutoArmor puts on the best armor in your inventory by itself. When you pick up a better helmet, chestplate, leggings or boots, it swaps them in. It does not take off an Elytra you are wearing.

**Category:** Combat
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Constraints | Setting Group | | | See [Shared: Inventory Constraints](/docs/modules/shared-settings/inventory-constraints). |
| Mode | Choice | Smart | Smart, RawDefense | How to decide which armor is best. Smart counts all protection enchantments. RawDefense only counts how much damage the armor blocks on old 1.8 servers, so Fire or Blast Protection can't make worse armor look better. RawDefense is good for SkyWars and BedWars. |
| Mode → [RawDefense] → ConsiderProjectileProtection | Toggle | true | | Also counts Projectile Protection. Useful when lots of players use bows. |
| Hotbar | Toggleable Group | On | | Puts on armor straight from your hotbar, which is faster. |
| Hotbar → CanSwapArmor | Toggle | false | | Swaps worn armor with armor in your hotbar in one click. Only turn this on if the server is 1.19.4 or newer. |
| SaveArmor | Toggleable Group | On | | Swaps out armor that is about to break for a fresh piece. |
| SaveArmor → DurabilityThreshold | Integer | 24 | 0..100 | When a piece has this much durability left (in percent) or less, it gets swapped. |
| SaveArmor → AutoOpenInventory | Toggle | true | | Opens your inventory by itself to swap the armor, if it needs to. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/autoarmor/ModuleAutoArmor.kt)*
