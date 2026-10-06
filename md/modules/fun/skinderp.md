## SkinDerp

SkinDerp randomly toggles the overlay layers of your Minecraft skin on and off every tick, creating a flickering or "derping" visual effect. It works with the standard skin layer system — hat, jacket, sleeves, pants legs, and cape — so it requires a skin that actually uses those second layers to look interesting.

You can control which parts flicker and how fast the toggling happens. When **Sync** is off, each selected part is toggled independently at random, producing a chaotic scrambled look. When **Sync** is on, each part is flipped from its current state in unison, so all selected parts blink together in a coordinated pattern. When you disable the module, your original skin layer settings are automatically restored.

This is a purely cosmetic and fun module. It has no combat or movement effect, but it pairs well with other visual oddities like [Derp](/docs/modules/fun/derp) or [HandDerp](/docs/modules/fun/handderp) if you want a fully chaotic appearance.

**Category:** Fun
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Sync | Toggle | false | — | When enabled, all selected skin parts flip together in sync each tick instead of being toggled independently at random. |
| Delay | Integer | 0 | 0–20 ticks | How many ticks to wait between each toggle cycle. Higher values slow down the flickering effect. |
| Parts | Multi-Select | Hat, Jacket, LeftPants, RightPants, LeftSleeve, RightSleeve, Cape | — | Which skin overlay parts are included in the derp effect. Deselect any parts you want to remain visible. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/fun/ModuleSkinDerp.kt)*
