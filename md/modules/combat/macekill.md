## MaceKill

MaceKill dramatically amplifies the Mace's fall-damage mechanic by faking a large fall height at the moment you swing it. In vanilla Minecraft, the Mace deals bonus damage based on how far you've fallen before hitting an enemy — MaceKill spoofs that distance on the server so you deal massive, potentially one-shot damage without needing to actually fall from height.

Enable this module whenever you have a Mace in hand and want to delete targets instantly. It activates automatically when you attack with the Mace; no additional setup is required. Keep in mind this relies on a packet-level exploit and may be detectable or blocked on anti-cheat protected servers.

The **FallHeight** setting controls how many blocks of simulated fall the module tries to fake. The actual height used may be slightly lower if blocks above your head would obstruct the teleport path — MaceKill automatically finds the highest unobstructed height up to your configured value.

**Category:** Combat
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| FallHeight | Integer | 22 | 1–170 | The maximum number of blocks of fall height to simulate when attacking with the Mace. Higher values deal more damage; the module automatically reduces this if blocks are in the way. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/ModuleMaceKill.kt)*
