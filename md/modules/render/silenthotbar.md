## SilentHotbar

Several modules in LiquidBounce use a "silent hotbar" mechanic — they temporarily switch your selected hotbar slot server-side to use a specific item (for attacking, building, or other actions) without actually moving your client-side selection. By default, Minecraft would display whichever item is silently selected in your hand, making it visually obvious that your held item is swapping around. SilentHotbar prevents that visual switch from showing, so your hand always displays the item you have genuinely selected on your hotbar.

This module is primarily a cosmetic complement to other modules that rely on silent slot switching, such as [KillAura](/docs/modules/combat/killaura), [AutoTool](/docs/modules/world/autotool), or [Scaffold](/docs/modules/world/scaffold). Enabling it keeps your first-person view clean and less tell-tale during gameplay.

The **NoCooldownProgress** option extends this behaviour to the attack cooldown indicator — when enabled, the cooldown animation will not play for the silently selected item, keeping the visual state consistent with what you are actually holding.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| NoCooldownProgress | Toggle | true | — | Suppresses the attack cooldown progress animation for the silently selected item, so the cooldown overlay matches your visually held item rather than the one being used internally. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleSilentHotbar.kt)*
