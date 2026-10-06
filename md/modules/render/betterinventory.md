## BetterInventory

BetterInventory bundles several quality-of-life visual tweaks for inventory and container screens. Instead of changing how items behave, it adds on-screen information and highlights that make managing your inventory faster and clearer. Each feature is its own toggleable group, so you can enable only the parts you want.

The three features are independent. **HighlightClicked** draws an outline or hotbar-style frame around the slot you last clicked, so it's easy to track which slot you just interacted with — see [the highlight logic](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleBetterInventory.kt#L155-L159). **TextCooldownProgress** prints the remaining cooldown directly on an item (such as an Ender Pearl or Chorus Fruit) as a percentage, in ticks, or in seconds, so you don't have to read the shrinking cooldown overlay; the text only appears while a cooldown is active, as handled in [the cooldown text drawing](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleBetterInventory.kt#L121-L153).

**ContainerItemView** previews the contents of a container item — like a Shulker Box or Bundle — without opening it, by reading its stored items and drawing them next to your cursor when you hover over the stack. You can position the preview relative to the mouse or at a fixed offset, optionally hide empty slots, and scale it to taste, as shown in [the container preview rendering](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleBetterInventory.kt#L161-L196).

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| HighlightClicked | Toggleable Group | on | — | Highlights the slot you last clicked in an inventory screen. |
| HighlightClicked → Mode | Mode Selector | Border | Border, Texture | How the clicked slot is highlighted: a colored border, or the vanilla hotbar selection frame. |
| HighlightClicked → Mode → [Border] → Color | Color | — | — | Color of the border drawn around the clicked slot. |
| TextCooldownProgress | Toggleable Group | on | — | Shows an item's remaining cooldown as text drawn over the item. |
| TextCooldownProgress → Mode | Choice | Percentage | Percentage, DurationTicks, DurationSeconds | Format of the cooldown readout: a percentage, the remaining ticks, or the remaining seconds. |
| TextCooldownProgress → Scale | Decimal | 1.0 | 0.25..4.0 | Size multiplier for the cooldown text. |
| TextCooldownProgress → Color | Color | — | — | Color of the cooldown text. |
| ContainerItemView | Toggleable Group | on | — | Previews the contents of a hovered container item (e.g. Shulker Box, Bundle) next to your cursor. |
| ContainerItemView → SkipEmptyStack | Toggle | false | — | When enabled, empty slots inside the container are omitted from the preview. |
| ContainerItemView → Scale | Decimal | 1.0 | 0.25..4.0 | Size multiplier for the container preview. |
| ContainerItemView → RelativeToMouse | Toggle | true | — | When enabled, the preview follows your cursor; when disabled, it uses a fixed position from the offsets below. |
| ContainerItemView → RenderOffsetX | Decimal | 150.0 | -4096.0..4096.0 | Horizontal offset of the preview, in pixels. |
| ContainerItemView → RenderOffsetY | Decimal | 0.0 | -4096.0..4096.0 | Vertical offset of the preview, in pixels. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleBetterInventory.kt)*
