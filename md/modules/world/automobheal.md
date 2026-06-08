## AutoMobHeal

AutoMobHeal automatically tends to nearby vanilla mobs that can be healed, restoring their health by feeding them the right item or, in the Iron Golem's case, repairing them with an iron ingot. It looks for the closest valid mob within reach that has line of sight, picks a suitable item from your hotbar or offhand, and interacts with it — no manual right-clicking required. This is handy when you're keeping pets, golems, or mounts alive during a fight or on a long journey.

Each animal type has its own toggle and its own health threshold, so you control exactly which mobs get healed and how hurt they need to be before the module steps in. Tamed-only creatures (wolves, cats, nautilus) are only healed when they belong to you, and the module respects sneaking so it won't interfere when you're trying to ride or interact with a mount yourself. For most food-eating mobs, the **NoWaste** option keeps it from overfeeding — it avoids items that would heal more than the mob is missing and prefers the closest-matching food.

Because the module uses your own items, it will consume them from your inventory just like manual feeding would. Special high-value foods (golden carrots, golden/enchanted golden apples for horses, fish buckets for nautilus) are opt-in so you don't burn through rare items by accident.

**Category:** World
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Range | Decimal | 4.5 | 1.0..6.0 | How close (in blocks) a mob must be before it gets healed. Capped by your actual entity reach. |
| Delay | Integer Range | 4..4 | 0..40 ticks | Wait time after a successful heal before acting again. A range adds randomization between the two values. |
| SlotResetDelay | Integer | 2 | 0..20 ticks | How long the chosen hotbar slot stays selected before switching back to your previous slot. |
| SwingMode | Choice | DoNotHide | — | Controls whether the hand-swing animation is shown. Options: DoNotHide, HideForBoth, HideForClient, HideForServer. |
| IronGolem | Toggleable Group | On | — | Repairs iron golems using iron ingots. |
| IronGolem → HealthThreshold | Decimal | 75.0 | 1.0..100.0 % | Only heal an iron golem once its health drops to or below this percentage. |
| Wolf | Toggleable Group | On | — | Feeds your tamed wolves to heal them. |
| Wolf → HealthThreshold | Decimal | 75.0 | 1.0..100.0 % | Only heal a wolf once its health drops to or below this percentage. |
| Wolf → NoWaste | Toggle | true | — | Avoid using food that would heal more than the wolf is missing. |
| Cat | Toggleable Group | On | — | Feeds your tamed cats to heal them. |
| Cat → HealthThreshold | Decimal | 75.0 | 1.0..100.0 % | Only heal a cat once its health drops to or below this percentage. |
| Cat → NoWaste | Toggle | true | — | Avoid using food that would heal more than the cat is missing. |
| HorseFamily | Toggleable Group | On | — | Feeds horses and donkeys to heal them. |
| HorseFamily → HealthThreshold | Decimal | 75.0 | 1.0..100.0 % | Only heal a horse once its health drops to or below this percentage. |
| HorseFamily → NoWaste | Toggle | true | — | Avoid using food that would heal more than the horse is missing. |
| HorseFamily → AllowGoldenCarrot | Toggle | false | — | Allow golden carrots to be used as healing food. |
| HorseFamily → AllowGoldenApple | Toggle | false | — | Allow golden apples to be used as healing food. |
| HorseFamily → AllowEnchantedGoldenApple | Toggle | false | — | Allow enchanted golden apples to be used as healing food. |
| ZombieHorse | Toggleable Group | On | — | Feeds zombie horses to heal them. |
| ZombieHorse → HealthThreshold | Decimal | 75.0 | 1.0..100.0 % | Only heal a zombie horse once its health drops to or below this percentage. |
| ZombieHorse → NoWaste | Toggle | true | — | Avoid using food that would heal more than the zombie horse is missing. |
| Llama | Toggleable Group | On | — | Feeds llamas (and trader llamas) to heal them. |
| Llama → HealthThreshold | Decimal | 75.0 | 1.0..100.0 % | Only heal a llama once its health drops to or below this percentage. |
| Llama → NoWaste | Toggle | true | — | Avoid using food that would heal more than the llama is missing. |
| Camel | Toggleable Group | On | — | Feeds camels to heal them. |
| Camel → HealthThreshold | Decimal | 75.0 | 1.0..100.0 % | Only heal a camel once its health drops to or below this percentage. |
| Camel → NoWaste | Toggle | true | — | Avoid using food that would heal more than the camel is missing. |
| CamelHusk | Toggleable Group | On | — | Feeds camel husks to heal them. |
| CamelHusk → HealthThreshold | Decimal | 75.0 | 1.0..100.0 % | Only heal a camel husk once its health drops to or below this percentage. |
| CamelHusk → NoWaste | Toggle | true | — | Avoid using food that would heal more than the camel husk is missing. |
| Nautilus | Toggleable Group | On | — | Feeds your tamed adult nautilus to heal them. |
| Nautilus → HealthThreshold | Decimal | 75.0 | 1.0..100.0 % | Only heal a nautilus once its health drops to or below this percentage. |
| Nautilus → NoWaste | Toggle | true | — | Avoid using food that would heal more than the nautilus is missing. |
| Nautilus → AllowBucketFood | Toggle | false | — | Allow fish buckets to be used as healing food. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/automobheal/AutoMobHeal.kt)*
