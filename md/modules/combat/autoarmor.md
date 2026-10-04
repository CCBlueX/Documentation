## AutoArmor

AutoArmor keeps you geared up without any manual sorting. As soon as it finds better armor anywhere in your inventory, it equips it for you — picking the strongest available helmet, chestplate, leggings, and boots automatically. This is handy in fast-paced PvP or kit-based games where stopping to drag armor into place can get you killed.

By default it can equip pieces straight from your hotbar as well as from your main inventory, and it will make room in an armor slot (or throw out the old piece if your inventory is full) when needed. It won't touch an equipped Elytra, so your gliding setup stays intact.

The **Mode** setting decides how two pieces are ranked against each other. *Smart* uses the modern, toughness-aware damage formula and weighs every damage-reduction enchantment (Protection, Projectile, Fire and Blast Protection) into one value. *RawDefense* instead ranks by the real damage reduction under the 1.8 armor model, where each armor point is a flat 4% and toughness does not exist — only Protection (and optionally Projectile Protection) counts, so niche enchantments can never make the module prefer iron with high Fire Protection over plain diamond. That makes it the better pick for SkyWars and BedWars.

The optional **SaveArmor** feature watches the durability of the armor you're wearing and swaps in fresh pieces before your current ones break, opening your inventory on its own if that's what it takes to get the replacement on in time.

**Category:** Combat
**Enabled by default:** Yes

### Settings

| Setting | Type | Default | Range | Description |
| --- | --- | --- | --- | --- |
| Constraints | Setting Group | — | — | See [Shared: Inventory Constraints](/docs/modules/shared-settings/inventory-constraints). |
| Mode | Choice | Smart | Smart, RawDefense | How armor pieces are ranked. *Smart* weighs all protection enchantments into the modern damage formula. *RawDefense* ranks by the real damage reduction under the 1.8 armor model and ignores enchantments that don't add actual defense. |
| Mode → RawDefense → ConsiderProjectileProtection | Toggle | true | — | Let Projectile Protection influence the ranking as a deciding argument, which helps on archer-heavy servers. When off, it only matters if everything else is equal. |
| Hotbar | Toggleable Group | On | — | Allow equipping armor by clicking pieces in your hotbar, which is faster than moving items inside the inventory. When off, armor is equipped using inventory moves only. |
| Hotbar → CanSwapArmor | Toggle | false | — | Use the direct armor-swap (Minecraft 1.19.4+) to switch a worn piece for a hotbar piece in one click. Leave off on servers that don't support it. |
| SaveArmor | Toggleable Group | Off | — | Watch the durability of your equipped armor and replace worn-out pieces before they break. |
| SaveArmor → DurabilityThreshold | Integer | 24 | 0–100 | Durability percentage at or below which a worn piece is treated as used up and swapped for a fresh replacement. |
| SaveArmor → AutoOpenInventory | Toggle | true | — | Automatically open your inventory when needed to swap in a replacement piece, even if it means closing another open screen first. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/autoarmor/ModuleAutoArmor.kt)*
