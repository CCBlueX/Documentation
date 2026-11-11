## QuickPerspectiveSwap

QuickPerspectiveSwap changes your camera view only while you hold its key. Let go and you are back in the view you had before, so you can take a quick look at yourself or behind you.

From first person it switches to the front view (looking at your face). From the back view it switches to the front view, and from the front view to the back view. It does nothing while [FreeLook](/docs/modules/render/freelook) or [FreeCam](/docs/modules/render/freecam) is on.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| RearView | Toggle | false | | From first person, switch to the back view (behind your character) instead of the front view. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleQuickPerspectiveSwap.kt)*
