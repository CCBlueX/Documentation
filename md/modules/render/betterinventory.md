## BetterInventory

BetterInventory adds helpful extras to inventory screens. It marks the slot you clicked last, shows item cooldowns as text, and lets you see what is inside a shulker box or bundle by hovering over it.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| HighlightClicked | Toggleable Group | On | | Marks the slot you clicked last. |
| HighlightClicked → Mode | Mode Selector | Border | Border, Texture | Border draws a colored frame, Texture uses the hotbar selection frame. |
| HighlightClicked → Mode → [Border] → Color | Color | | | Color of the frame. |
| TextCooldownProgress | Toggleable Group | On | | Shows how long an item's cooldown has left, for example on ender pearls. |
| TextCooldownProgress → Mode | Choice | Percentage | Percentage, DurationTicks, DurationSeconds | Show it as a percent, in ticks (20 per second) or in seconds. |
| TextCooldownProgress → Scale | Decimal | 1.0 | 0.25..4.0 | Size of the text. |
| TextCooldownProgress → Color | Color | White | | Color of the text. |
| ContainerItemView | Toggleable Group | On | | Shows the items inside a shulker box or bundle when you hover over it. |
| ContainerItemView → SkipEmptyStack | Toggle | false | | Leaves out empty slots. |
| ContainerItemView → Scale | Decimal | 1.0 | 0.25..4.0 | Size of the preview. |
| ContainerItemView → RelativeToMouse | Toggle | true | | The preview follows your mouse. Off uses a fixed spot. |
| ContainerItemView → RenderOffsetX | Decimal | 150.0 | -4096.0..4096.0 | Moves the preview left or right. |
| ContainerItemView → RenderOffsetY | Decimal | 0.0 | -4096.0..4096.0 | Moves the preview up or down. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleBetterInventory.kt)*
