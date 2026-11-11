## AutoMobHeal

AutoMobHeal heals mobs near you by using the right item on them. It feeds your pets and mounts and repairs iron golems with iron ingots. Turn it on to keep your animals alive in a fight or on a long trip.

It uses up your own items, the same as feeding by hand. Wolves, cats and nautiluses are only healed if they are yours. Rare foods like golden apples are off unless you allow them.

**Category:** World
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Range | Decimal | 4.5 | 1.0..6.0 blocks | How close a mob has to be. |
| Delay | Integer Range | 4..4 | 0..40 ticks | Wait after each heal (20 ticks per second). |
| SlotResetDelay | Integer | 2 | 0..20 ticks | How long the item stays in your hand before switching back. |
| SwingMode | Choice | DoNotHide | DoNotHide, HideForClient | Whether you see your hand swing. |
| IronGolem | Toggleable Group | On | | Repairs iron golems with iron ingots. |
| IronGolem → HealthThreshold | Decimal | 75.0 | 1.0..100.0 % | Heals only when its health is at or below this. |
| Wolf | Toggleable Group | On | | Heals your wolves. |
| Wolf → HealthThreshold | Decimal | 75.0 | 1.0..100.0 % | Heals only when its health is at or below this. |
| Wolf → NoWaste | Toggle | true | | Picks food that does not heal more than needed. |
| Wolf → Armor | Toggleable Group | Off | | Takes care of your wolves' armor. |
| Wolf → Armor → Equip | Toggle | false | | Puts wolf armor on your grown-up wolves that have none. |
| Wolf → Armor → RepairThreshold | Decimal | 87.5 | 1.0..100.0 % | Repairs the armor when it is at or below this much durability. |
| Wolf → Armor → OnlyWhenSitting | Toggle | true | | Repairs only wolves that already sit. When off, it makes the wolf sit first. |
| Cat | Toggleable Group | On | | Heals your cats. |
| Cat → HealthThreshold | Decimal | 75.0 | 1.0..100.0 % | Heals only when its health is at or below this. |
| Cat → NoWaste | Toggle | true | | Picks food that does not heal more than needed. |
| HorseFamily | Toggleable Group | On | | Heals horses, donkeys and mules. |
| HorseFamily → HealthThreshold | Decimal | 75.0 | 1.0..100.0 % | Heals only when its health is at or below this. |
| HorseFamily → NoWaste | Toggle | true | | Picks food that does not heal more than needed. |
| HorseFamily → AllowGoldenCarrot | Toggle | false | | Lets it use golden carrots. |
| HorseFamily → AllowGoldenApple | Toggle | false | | Lets it use golden apples. |
| HorseFamily → AllowEnchantedGoldenApple | Toggle | false | | Lets it use enchanted golden apples. |
| ZombieHorse | Toggleable Group | On | | Heals zombie horses. |
| ZombieHorse → HealthThreshold | Decimal | 75.0 | 1.0..100.0 % | Heals only when its health is at or below this. |
| ZombieHorse → NoWaste | Toggle | true | | Picks food that does not heal more than needed. |
| Llama | Toggleable Group | On | | Heals llamas. |
| Llama → HealthThreshold | Decimal | 75.0 | 1.0..100.0 % | Heals only when its health is at or below this. |
| Llama → NoWaste | Toggle | true | | Picks food that does not heal more than needed. |
| Camel | Toggleable Group | On | | Heals camels. |
| Camel → HealthThreshold | Decimal | 75.0 | 1.0..100.0 % | Heals only when its health is at or below this. |
| Camel → NoWaste | Toggle | true | | Picks food that does not heal more than needed. |
| CamelHusk | Toggleable Group | On | | Heals camel husks. |
| CamelHusk → HealthThreshold | Decimal | 75.0 | 1.0..100.0 % | Heals only when its health is at or below this. |
| CamelHusk → NoWaste | Toggle | true | | Picks food that does not heal more than needed. |
| Nautilus | Toggleable Group | On | | Heals your nautiluses. |
| Nautilus → HealthThreshold | Decimal | 75.0 | 1.0..100.0 % | Heals only when its health is at or below this. |
| Nautilus → NoWaste | Toggle | true | | Picks food that does not heal more than needed. |
| Nautilus → AllowBucketFood | Toggle | false | | Lets it use fish buckets. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/automobheal/AutoMobHeal.kt)*
