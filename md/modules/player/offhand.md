## Offhand

Offhand automates what sits in your off-hand slot so you are never caught without the right survival or combat item. You configure independent sub-systems for totems of undying, end crystals, golden apples, strength potions, and building blocks — the module selects whichever is most relevant at any moment and quietly moves it into your off-hand without interrupting your main-hand actions. Each item group has an optional keybind for manual override, and the **Cycle** key lets you step through available modes on the fly.

The Totem sub-system is the most sophisticated: it tracks your current health (including absorption), checks predicted explosion damage from nearby entities (creepers, end crystals), optionally scans for beds and respawn anchors, and simulates incoming fall damage — all before deciding whether a totem is required. When danger passes it can swap back to whatever was in your off-hand before the emergency. The Crystal, Gapple, StrengthPotion, and Block groups add contextual layers on top: for example, you can hold a golden apple only while swinging a sword with [KillAura](/docs/modules/combat/killaura) active, or keep a block ready only while [Scaffold](/docs/modules/world/scaffold) or [Eagle](/docs/modules/player/eagle) is running.

**Category:** Player
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Constraints | Setting Group | — | — | See [Shared: Inventory Constraints](/docs/modules/shared-settings/inventory-constraints). |
| SwitchMode | Choice | Automatic | Smart, Switch, PickUp, Automatic | How items are moved into the off-hand. **Smart** swaps hotbar items directly, sending fewer packets (works on all versions but can trigger kicks on some servers). **Switch** performs a single inventory-swap action — the cleanest method on 1.16+ servers. **PickUp** uses click-to-pick-up actions and works on all versions. **Automatic** chooses between Switch and PickUp based on the detected server version (requires ViaFabricPlus for older servers). |
| SwitchDelay | Integer | 0 | 0..500 ms | Minimum time (ms) to wait between off-hand swaps for all item modes. |
| Cycle | Key | — | — | Key to cycle through available off-hand modes. |
| Totem | Toggleable Group | on | — | Automatically equips a totem of undying when you are in danger. |
| Totem → SwitchDelay | Integer | 0 | 0..500 ms | Delay (ms) specifically before switching to a totem. |
| Totem → SwitchBackDelay | Integer | 40 | 0..500 ms | Delay (ms) to wait before switching back to the previous item once the totem is no longer needed. |
| Totem → Health | Toggleable Group | on | — | Triggers a totem switch when your health drops to or below the configured threshold. |
| Totem → Health → HealthThreshold | Integer | 14 | 0..20 | Health (in half-hearts, counting absorption) at or below which a totem is equipped. |
| Totem → Health → Safety | Toggleable Group | on | — | Uses a lower, separate health threshold while you are inside a hole or burrowed, letting you keep more useful items in your off-hand when you are already protected from most damage. |
| Totem → Health → Safety → SafeHealthThreshold | Integer | 10 | 0..20 | The reduced health threshold (half-hearts) applied instead of HealthThreshold when you are in a hole or burrowed. |
| Totem → Health → SubtractCalculatedDamage | Toggle | false | — | Subtracts predicted incoming damage from your effective health before comparing it to the threshold, making totem switching more proactive. |
| Totem → Health → PredictExplosionDamageEntities | Toggle | true | — | Factors in predicted explosion damage from nearby entities (e.g. end crystals, creepers) when deciding whether a totem is required. |
| Totem → Health → PredictExplosionDamageBlocks | Toggle | false | — | Factors in predicted explosion damage from nearby beds and charged respawn anchors when deciding whether a totem is required. |
| Totem → Health → MissingArmor | Toggle | true | — | Forces a totem into the off-hand whenever any armor slot is empty, regardless of current health. |
| Totem → Health → PredictFallDamage | Toggleable Group | on | — | Simulates your falling trajectory and equips a totem if the calculated fall damage would bring you to or below the threshold. |
| Totem → Health → PredictFallDamage → IgnoreElytra | Toggle | false | — | Skips fall-damage prediction while you are gliding with an elytra. |
| Totem → Health → SwitchBack | Toggle | true | — | After a totem is no longer needed, returns the item that was previously in your off-hand. |
| Totem → SendDirectly | Toggle | false | — | Bypasses the normal inventory scheduling queue and sends totem-swap packets immediately, ignoring active inventory constraints. Use carefully — it can look suspicious on strict servers. |
| Crystal | Toggleable Group | on | — | Keeps an end crystal in your off-hand. |
| Crystal → OnlyWhileCrystalAura | Toggle | false | — | Only equips a crystal while [CrystalAura](/docs/modules/combat/crystalaura) is active. |
| Crystal → WhenNoTotems | Toggle | true | — | Falls back to an end crystal when Totem mode would normally equip a totem but none are available in your inventory. |
| Crystal → CrystalBind | Key | — | — | Key to manually force an end crystal into the off-hand. |
| Gapple | Toggleable Group | on | — | Keeps an enchanted golden apple (or regular golden apple as a fallback) in your off-hand. |
| Gapple → GappleBind | Key | — | — | Key to manually force a golden apple into the off-hand. |
| Gapple → WhileHoldingSword | Toggleable Group | on | — | Only equips a golden apple while you are holding a sword in your main hand. |
| Gapple → WhileHoldingSword → OnlyWhileKillAura | Toggle | true | — | Requires [KillAura](/docs/modules/combat/killaura) to be active before equipping the golden apple. |
| StrengthPotion | Toggleable Group | off | — | Keeps a strength potion in your off-hand so it is ready to drink before or during a fight. |
| StrengthPotion → OnlyWhileHoldingSword | Toggle | true | — | Only equips a strength potion while you are holding a sword. |
| StrengthPotion → OnlyWhileKillAura | Toggle | true | — | Only equips a strength potion while [KillAura](/docs/modules/combat/killaura) is active. |
| StrengthPotion → StrengthBind | Key | — | — | Key to manually force a strength potion into the off-hand. |
| Block | Toggleable Group | off | — | Keeps a placeable block in your off-hand for use alongside building modules. |
| Block → WhileScaffold | Toggle | true | — | Equips a block while [Scaffold](/docs/modules/world/scaffold) is active. |
| Block → WhileEagle | Toggle | true | — | Equips a block while [Eagle](/docs/modules/player/eagle) is active. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/offhand/ModuleOffhand.kt)*
