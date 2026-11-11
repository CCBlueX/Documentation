## MaceKill

MaceKill makes the server think you fell from high up when you hit someone with a Mace. The Mace does more damage the further you fall, so your hit does a lot of damage without a real fall. It only works while you hold a Mace, and servers with an anticheat may block it.

**Category:** Combat
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| FallHeight | Integer | 22 | 1..170 | How many blocks of falling to fake. More blocks means more damage. If blocks above you are in the way, a lower height is used. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/ModuleMaceKill.kt)*
