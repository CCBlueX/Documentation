## NoSwing

NoSwing suppresses the hand swing animation that plays whenever you attack, use an item, or interact with the world. With this module enabled, your held item stays perfectly still on screen instead of sweeping through the attack motion, giving you a cleaner, less distracting view during combat or general play.

The **HideFor** setting lets you control exactly where the animation is hidden. Suppressing it for **Client** removes the visual swing from your own screen, so you never see your hand move. Suppressing it for **Server** prevents the swing packet from being sent to the server, meaning other players won't see your hand animate either. Both options are enabled by default, hiding the animation entirely on all sides.

This module pairs well with other visual tweaks such as [Animations](/docs/modules/render/animations) and [NoBob](/docs/modules/render/nobob) if you want a fully clean, static first-person view.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---------|------|---------|-------|-------------|
| HideFor | Multi-Select | Client, Server | Client, Server | Controls where the swing animation is hidden. **Client** hides it on your screen; **Server** hides it from other players by suppressing the swing packet. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleNoSwing.kt)*
