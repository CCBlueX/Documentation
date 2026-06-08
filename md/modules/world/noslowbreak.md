## NoSlowBreak

NoSlowBreak prevents the game's normal mining speed penalties from slowing you down when breaking blocks. Vanilla Minecraft reduces your breaking speed in several situations — when you have the Mining Fatigue effect, when you are not standing on the ground, or when you are underwater. This module cancels those reductions so your blocks break at full speed regardless of your current conditions.

You can choose which situations the module applies to independently. For example, you might only want to counteract Mining Fatigue (common on servers that apply the effect near elder guardians or via plugins) without affecting the physics of mid-air or underwater mining. Enable whichever conditions suit your playstyle or server environment.

This module pairs well with [FastBreak](/docs/modules/world/fastbreak) if you want to mine as quickly as possible overall, and with [NoSlow](/docs/modules/movement/noslow) if you are also looking to remove other speed-reducing effects on your movement.

**Category:** World
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---------|------|---------|-------|-------------|
| When | Multi-Select | MiningFatigue, OnAir | MiningFatigue, OnAir, Underwater | Select which conditions should have their block-breaking speed penalty removed. **MiningFatigue** — negates the penalty from the Mining Fatigue status effect. **OnAir** — negates the penalty for breaking blocks while airborne. **Underwater** — negates the penalty for breaking blocks while submerged. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/ModuleNoSlowBreak.kt)*
