## InventoryCleaner

Automatically sorts your inventory and drops unnecessary items.

**Category:** Player  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Constraints (Setting Group)
│   ├── StartDelay (Integer Range | default: 1..2 | range: 0..20 | ticks)
│   ├── ClickDelay (Integer Range | default: 2..4 | range: 0..20 | ticks)
│   ├── CloseDelay (Integer Range | default: 1..2 | range: 0..20 | ticks)
│   ├── MissChance (Integer Range | default: 0..0 | range: 0..100 | %)
│   └── Requires (Multi-Select | options: NoMovement, NoRotation, InventoryOpen)
├── MaximumBlocks (Integer | default: 512 | range: 0..2500)
├── MaximumArrows (Integer | default: 128 | range: 0..2500)
├── MaximumThrowables (Integer | default: 64 | range: 0..600)
├── MaximumFoodPoints (Integer | default: 200 | range: 0..2000)
├── Greedy (Toggle | default: true)
├── OffHandItem (Choice | default: SHIELD | options: Sword, Weapon, Spear, Mace, Bow, Crossbow, Axe, Pickaxe, Shovel, Hoe, Rod, Shield, Water, Lava, Milk, Pearl, Gapple, Food, Potion, Block, Throwables, Ignore, None)
├── SlotItem-1 (Choice | default: WEAPON | options: Sword, Weapon, Spear, Mace, Bow, Crossbow, Axe, Pickaxe, Shovel, Hoe, Rod, Shield, Water, Lava, Milk, Pearl, Gapple, Food, Potion, Block, Throwables, Ignore, None)
├── SlotItem-2 (Choice | default: BOW | options: Sword, Weapon, Spear, Mace, Bow, Crossbow, Axe, Pickaxe, Shovel, Hoe, Rod, Shield, Water, Lava, Milk, Pearl, Gapple, Food, Potion, Block, Throwables, Ignore, None)
├── SlotItem-3 (Choice | default: PICKAXE | options: Sword, Weapon, Spear, Mace, Bow, Crossbow, Axe, Pickaxe, Shovel, Hoe, Rod, Shield, Water, Lava, Milk, Pearl, Gapple, Food, Potion, Block, Throwables, Ignore, None)
├── SlotItem-4 (Choice | default: AXE | options: Sword, Weapon, Spear, Mace, Bow, Crossbow, Axe, Pickaxe, Shovel, Hoe, Rod, Shield, Water, Lava, Milk, Pearl, Gapple, Food, Potion, Block, Throwables, Ignore, None)
├── SlotItem-5 (Choice | default: NONE | options: Sword, Weapon, Spear, Mace, Bow, Crossbow, Axe, Pickaxe, Shovel, Hoe, Rod, Shield, Water, Lava, Milk, Pearl, Gapple, Food, Potion, Block, Throwables, Ignore, None)
├── SlotItem-6 (Choice | default: POTION | options: Sword, Weapon, Spear, Mace, Bow, Crossbow, Axe, Pickaxe, Shovel, Hoe, Rod, Shield, Water, Lava, Milk, Pearl, Gapple, Food, Potion, Block, Throwables, Ignore, None)
├── SlotItem-7 (Choice | default: FOOD | options: Sword, Weapon, Spear, Mace, Bow, Crossbow, Axe, Pickaxe, Shovel, Hoe, Rod, Shield, Water, Lava, Milk, Pearl, Gapple, Food, Potion, Block, Throwables, Ignore, None)
├── SlotItem-8 (Choice | default: BLOCK | options: Sword, Weapon, Spear, Mace, Bow, Crossbow, Axe, Pickaxe, Shovel, Hoe, Rod, Shield, Water, Lava, Milk, Pearl, Gapple, Food, Potion, Block, Throwables, Ignore, None)
└── SlotItem-9 (Choice | default: BLOCK | options: Sword, Weapon, Spear, Mace, Bow, Crossbow, Axe, Pickaxe, Shovel, Hoe, Rod, Shield, Water, Lava, Milk, Pearl, Gapple, Food, Potion, Block, Throwables, Ignore, None)
```

### Settings Details

#### Constraints

A group of related settings.

- **StartDelay** (Integer Range) — default: `1` – `2`; range: `0` – `20`; unit: ticks
- **ClickDelay** (Integer Range) — default: `2` – `4`; range: `0` – `20`; unit: ticks
- **CloseDelay** (Integer Range) — default: `1` – `2`; range: `0` – `20`; unit: ticks
- **MissChance** (Integer Range) — default: `0` – `0`; range: `0` – `100`; unit: %
- **Requires** (Multi-Select) — options: `NoMovement`, `NoRotation`, `InventoryOpen`

- **MaximumBlocks** (Integer) — default: `512`; range: `0` – `2500`
- **MaximumArrows** (Integer) — default: `128`; range: `0` – `2500`
- **MaximumThrowables** (Integer) — default: `64`; range: `0` – `600`
- **MaximumFoodPoints** (Integer) — default: `200`; range: `0` – `2000`
- **Greedy** (Toggle) — default: `true`
- **OffHandItem** (Choice) — default: `SHIELD`; options: `Sword`, `Weapon`, `Spear`, `Mace`, `Bow`, `Crossbow`, `Axe`, `Pickaxe`, `Shovel`, `Hoe`, `Rod`, `Shield`, `Water`, `Lava`, `Milk`, `Pearl`, `Gapple`, `Food`, `Potion`, `Block`, `Throwables`, `Ignore`, `None`
- **SlotItem-1** (Choice) — default: `WEAPON`; options: `Sword`, `Weapon`, `Spear`, `Mace`, `Bow`, `Crossbow`, `Axe`, `Pickaxe`, `Shovel`, `Hoe`, `Rod`, `Shield`, `Water`, `Lava`, `Milk`, `Pearl`, `Gapple`, `Food`, `Potion`, `Block`, `Throwables`, `Ignore`, `None`
- **SlotItem-2** (Choice) — default: `BOW`; options: `Sword`, `Weapon`, `Spear`, `Mace`, `Bow`, `Crossbow`, `Axe`, `Pickaxe`, `Shovel`, `Hoe`, `Rod`, `Shield`, `Water`, `Lava`, `Milk`, `Pearl`, `Gapple`, `Food`, `Potion`, `Block`, `Throwables`, `Ignore`, `None`
- **SlotItem-3** (Choice) — default: `PICKAXE`; options: `Sword`, `Weapon`, `Spear`, `Mace`, `Bow`, `Crossbow`, `Axe`, `Pickaxe`, `Shovel`, `Hoe`, `Rod`, `Shield`, `Water`, `Lava`, `Milk`, `Pearl`, `Gapple`, `Food`, `Potion`, `Block`, `Throwables`, `Ignore`, `None`
- **SlotItem-4** (Choice) — default: `AXE`; options: `Sword`, `Weapon`, `Spear`, `Mace`, `Bow`, `Crossbow`, `Axe`, `Pickaxe`, `Shovel`, `Hoe`, `Rod`, `Shield`, `Water`, `Lava`, `Milk`, `Pearl`, `Gapple`, `Food`, `Potion`, `Block`, `Throwables`, `Ignore`, `None`
- **SlotItem-5** (Choice) — default: `NONE`; options: `Sword`, `Weapon`, `Spear`, `Mace`, `Bow`, `Crossbow`, `Axe`, `Pickaxe`, `Shovel`, `Hoe`, `Rod`, `Shield`, `Water`, `Lava`, `Milk`, `Pearl`, `Gapple`, `Food`, `Potion`, `Block`, `Throwables`, `Ignore`, `None`
- **SlotItem-6** (Choice) — default: `POTION`; options: `Sword`, `Weapon`, `Spear`, `Mace`, `Bow`, `Crossbow`, `Axe`, `Pickaxe`, `Shovel`, `Hoe`, `Rod`, `Shield`, `Water`, `Lava`, `Milk`, `Pearl`, `Gapple`, `Food`, `Potion`, `Block`, `Throwables`, `Ignore`, `None`
- **SlotItem-7** (Choice) — default: `FOOD`; options: `Sword`, `Weapon`, `Spear`, `Mace`, `Bow`, `Crossbow`, `Axe`, `Pickaxe`, `Shovel`, `Hoe`, `Rod`, `Shield`, `Water`, `Lava`, `Milk`, `Pearl`, `Gapple`, `Food`, `Potion`, `Block`, `Throwables`, `Ignore`, `None`
- **SlotItem-8** (Choice) — default: `BLOCK`; options: `Sword`, `Weapon`, `Spear`, `Mace`, `Bow`, `Crossbow`, `Axe`, `Pickaxe`, `Shovel`, `Hoe`, `Rod`, `Shield`, `Water`, `Lava`, `Milk`, `Pearl`, `Gapple`, `Food`, `Potion`, `Block`, `Throwables`, `Ignore`, `None`
- **SlotItem-9** (Choice) — default: `BLOCK`; options: `Sword`, `Weapon`, `Spear`, `Mace`, `Bow`, `Crossbow`, `Axe`, `Pickaxe`, `Shovel`, `Hoe`, `Rod`, `Shield`, `Water`, `Lava`, `Milk`, `Pearl`, `Gapple`, `Food`, `Potion`, `Block`, `Throwables`, `Ignore`, `None`

### Screenshots

*Screenshots for InventoryCleaner will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fplayer%2FModuleInventoryCleaner.kt)*
