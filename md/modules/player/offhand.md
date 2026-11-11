## Offhand

Offhand puts the right item in your offhand for you: a totem of undying, end crystal, golden apple, strength potion or block. It picks whichever one fits the moment. Each item can also have its own key to force it into your offhand, and the Cycle key steps through them.

The totem has the most checks. It goes in when your health (with absorption) gets low, when an explosion or a fall would hurt you a lot, or when a piece of armor is missing. When you are safe again, Offhand can put your old item back.

**Category:** Player
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Constraints | Setting Group | | | See [Inventory Constraints](/docs/modules/shared-settings/inventory-constraints). |
| SwitchMode | Choice | Switch | Smart, Switch, PickUp, Automatic | How items are moved into your offhand. Switch works best on 1.16 and newer servers. PickUp works on every version. Smart sends fewer clicks but some servers kick for it. Automatic picks Switch or PickUp from the server version and is the default when ViaFabricPlus is installed. |
| SwitchDelay | Integer | 0 | 0..500 ms | Time to wait between offhand swaps. |
| Cycle | Key | H | | Steps through the offhand items. |
| Totem | Toggleable Group | On | | Puts a totem in your offhand when you are in danger. |
| Totem → SwitchDelay | Integer | 0 | 0..500 ms | Time to wait before switching to a totem. |
| Totem → SwitchBackDelay | Integer | 40 | 0..500 ms | Time to wait before putting the old item back. |
| Totem → Health | Toggleable Group | On | | Uses a totem when your health is low. |
| Totem → Health → HealthThreshold | Integer | 14 | 0..20 | Health in half hearts, with absorption, at which the totem goes in. |
| Totem → Health → Safety | Toggleable Group | On | | Uses a lower health limit while you stand in a hole or are burrowed, where explosions hurt less. |
| Totem → Health → Safety → SafeHealthThreshold | Integer | 10 | 0..20 | Health limit used while you are in a hole or burrowed. |
| Totem → Health → SubtractCalculatedDamage | Toggle | Off | | Takes expected damage off your health before checking the limit, so the totem goes in earlier. |
| Totem → Health → PredictExplosionDamageEntities | Toggle | On | | Counts damage from nearby end crystals and creepers that could explode. |
| Totem → Health → PredictExplosionDamageBlocks | Toggle | Off | | Counts damage from nearby beds and respawn anchors that could explode. |
| Totem → Health → MissingArmor | Toggle | On | | Always holds a totem while a piece of armor is missing. |
| Totem → Health → PredictFallDamage | Toggleable Group | On | | Holds a totem if your fall would take you below the health limit. |
| Totem → Health → PredictFallDamage → IgnoreElytra | Toggle | Off | | Skips the fall check while you fly with an elytra. |
| Totem → Health → SwitchBack | Toggle | On | | Puts your old item back once you no longer need the totem. |
| Totem → SendDirectly | Toggle | Off | | Swaps in the totem right away and ignores the inventory constraints. Strict servers may notice this. |
| Crystal | Toggleable Group | On | | Keeps an end crystal in your offhand. |
| Crystal → OnlyWhileCrystalAura | Toggle | Off | | Only while [CrystalAura](/docs/modules/combat/crystalaura) is on. |
| Crystal → WhenNoTotems | Toggle | On | | Uses a crystal when you need a totem but have none. |
| Crystal → CrystalBind | Key | None | | Key that puts a crystal in your offhand. |
| Gapple | Toggleable Group | On | | Keeps an enchanted golden apple, or a normal one, in your offhand. |
| Gapple → GappleBind | Key | None | | Key that puts a golden apple in your offhand. |
| Gapple → WhileHoldingSword | Toggleable Group | On | | Only while you hold a sword. |
| Gapple → WhileHoldingSword → OnlyWhileKillAura | Toggle | On | | Only while [KillAura](/docs/modules/combat/killaura) is on. |
| StrengthPotion | Toggleable Group | Off | | Keeps a strength potion in your offhand. |
| StrengthPotion → OnlyWhileHoldingSword | Toggle | On | | Only while you hold a sword. |
| StrengthPotion → OnlyWhileKillAura | Toggle | On | | Only while [KillAura](/docs/modules/combat/killaura) is on. |
| StrengthPotion → StrengthBind | Key | None | | Key that puts a strength potion in your offhand. |
| Block | Toggleable Group | Off | | Keeps blocks in your offhand for building. |
| Block → WhileScaffold | Toggle | On | | While [Scaffold](/docs/modules/world/scaffold) is on. |
| Block → WhileEagle | Toggle | On | | While [Eagle](/docs/modules/player/eagle) is on. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/offhand/ModuleOffhand.kt)*
