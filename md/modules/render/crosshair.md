## Crosshair

Crosshair replaces the normal crosshair with your own. Pick a ring (Circle) or four lines like in Counter-Strike 2 (CS2), then change its size and colors.

After you attack, the crosshair grows for a moment and shrinks back once your weapon is ready again. That helps you time your hits. It is hidden while an inventory or chest is open.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | Circle | Circle, CS2 | Shape of the crosshair. |
| Mode → [Circle] → ShowInThirdPerson | Toggle | true | | Shows the crosshair in third person too. |
| Mode → [Circle] → Radius → Range | Decimal Range | 3.0..5.0 | 0.0..25.0 | Inner and outer size of the ring. |
| Mode → [Circle] → Radius → DynamicRadiusMultiplier | Decimal | 1.0 | 0.0..5.0 | How much the ring grows after you attack. 0 keeps it the same size. |
| Mode → [Circle] → Color → Sync | Toggle | true | | Uses only the first color. Off mixes both colors. |
| Mode → [Circle] → Color → FirstColor | Color | Light blue | | Main color. |
| Mode → [Circle] → Color → SecondColor | Color | Pale blue | | Second color, used when Sync is off. |
| Mode → [Circle] → Color → SpinSpeed | Decimal | 4.0 | -10.0..10.0 | How fast the colors move around. Negative goes the other way, 0 stops it. |
| Mode → [CS2] → ShowInThirdPerson | Toggle | true | | Shows the crosshair in third person too. |
| Mode → [CS2] → Crosshair → Length | Decimal | 5.0 | 1.0..20.0 | Length of each line. |
| Mode → [CS2] → Crosshair → Thickness | Decimal | 1.0 | 0.5..5.0 | Width of each line. |
| Mode → [CS2] → Crosshair → Gap | Decimal | 2.0 | 0.0..10.0 | Space between the middle and the lines. |
| Mode → [CS2] → Crosshair → DynamicMultiplier | Decimal | 1.0 | 0.0..10.0 | How much the gap grows after you attack. 0 keeps it the same. |
| Mode → [CS2] → Color → Sync | Toggle | true | | Uses only the first color. Off mixes both colors. |
| Mode → [CS2] → Color → FirstColor | Color | Light blue | | Main color. |
| Mode → [CS2] → Color → SecondColor | Color | Pale blue | | Second color, used when Sync is off. |
| Mode → [CS2] → Color → SpinSpeed | Decimal | 4.0 | -10.0..10.0 | How fast the colors move around. Negative goes the other way, 0 stops it. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/crosshair/ModuleCrosshair.kt)*
