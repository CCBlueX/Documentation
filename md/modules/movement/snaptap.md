## SnapTap

SnapTap resolves conflicting movement inputs by always prioritising the most recently pressed key on each axis. In standard Minecraft, pressing both Left and Right simultaneously causes your character to stop moving horizontally — the two inputs cancel each other out. With SnapTap enabled, the client detects which of the two opposing keys was pressed last and registers only that one, so you keep moving in whichever direction you most recently chose.

This applies independently to both the horizontal axis (Left/Right) and the vertical axis (Forward/Back). Whether you tap a strafe key while already holding the opposite key, or quickly reverse your walking direction, your movement responds immediately to your last input rather than locking up. This behaviour is sometimes called SOCD (Simultaneous Opposite Cardinal Directions) cleaning, and it is commonly used to make strafing and direction changes feel more responsive during PvP and parkour.

SnapTap works alongside [InventoryMove](/docs/modules/movement/inventorymove): when InventoryMove is active, SnapTap continues to apply its key-priority logic even while a screen or inventory is open.

**Category:** Movement
**Enabled by default:** No

### Settings

This module has no configurable settings.

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/ModuleSnapTap.kt)*
