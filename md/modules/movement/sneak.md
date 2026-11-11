## Sneak

Sneak keeps you sneaking all the time without holding the key. The mode decides how the sneaking is done.

**Category:** Movement
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | Vanilla | Legit, Vanilla, Switch | Legit: works like holding the Sneak key yourself. Vanilla: tells the server you sneak while you keep walking at normal speed. Switch: quickly switches sneaking on and off; only works on servers older than 1.21.6 when you join through ViaFabricPlus. |
| Mode → Legit → OnMagmaBlocksOnly | Toggle | false |  | Only sneaks when you step on a magma block, so it can't burn you. |
| NotDuringMove | Toggle | false |  | Stops sneaking while you walk. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/ModuleSneak.kt)*
