## QuickPerspectiveSwap

QuickPerspectiveSwap lets you instantly switch your camera perspective while holding the module's keybind. Unlike toggling Minecraft's default perspective with F5, this module is designed to be held — the moment you release the key, your view snaps back to your normal first-person (or whatever perspective you had before). This makes it ideal for quickly peeking behind you mid-fight or while navigating tight spaces without permanently changing your view.

By default, activating the module switches you to third-person front view (facing your character from the front). Enabling **RearView** changes this so that holding the key puts you into third-person back view instead, letting you see what is directly behind your character — useful for checking whether someone is following you.

This module pairs well with [FreeLook](/docs/modules/render/freelook) if you want full free camera rotation, or [Zoom](/docs/modules/render/zoom) when you need to inspect something at a distance without permanently committing to a different perspective.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---------|------|---------|-------|-------------|
| RearView | Toggle | false | — | When enabled, holding the keybind switches to third-person back view instead of third-person front view. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleQuickPerspectiveSwap.kt)*
