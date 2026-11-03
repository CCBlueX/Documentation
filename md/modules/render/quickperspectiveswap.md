## QuickPerspectiveSwap

QuickPerspectiveSwap lets you instantly switch your camera perspective while holding the module's keybind. Unlike toggling Minecraft's default perspective with F5, this module is designed to be held — the moment you release the key, your view snaps back to your normal first-person (or whatever perspective you had before). This makes it ideal for quickly peeking behind you mid-fight or while navigating tight spaces without permanently changing your view.

The perspective you get depends on your current view, which the module reads every tick so it stays in sync with the F5 key. From first person, activating the module switches you to third-person front view (facing your character from the front). Enabling **RearView** changes this so that holding the key puts you into third-person back view instead, letting you see what is directly behind your character — useful for checking whether someone is following you. If you are already in third-person back view, the module switches you to third-person front view, and vice versa. The module has no effect while [FreeLook](/docs/modules/render/freelook) or [FreeCam](/docs/modules/render/freecam) is running, as those manage the camera themselves.

This module pairs well with [FreeLook](/docs/modules/render/freelook) if you want full free camera rotation, or [Zoom](/docs/modules/render/zoom) when you need to inspect something at a distance without permanently committing to a different perspective.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---------|------|---------|-------|-------------|
| RearView | Toggle | false | — | When enabled, holding the keybind in first person switches to third-person back view instead of third-person front view. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleQuickPerspectiveSwap.kt)*
