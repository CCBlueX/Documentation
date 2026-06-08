## Animations

Animations gives you control over how your held items look and move on screen. You can resize and reposition the item in your main hand or off hand, tweak the rotation of the model, adjust how long the swing animation lasts, and pick a different blocking animation — all without changing how the game plays for other players. It's purely a visual tweak, so use it to get a viewmodel that feels comfortable to you, whether that's an old-school look or something more compact.

The main-hand and off-hand groups each let you shift the item along the X/Y axes, scale it up or down, and add extra rotation. The EquipOffset group controls the small "raise" animation that plays when you switch or use items, and lets you skip that motion in specific situations. AirWalker keeps your legs moving with the walking animation even while you're off the ground.

The BlockingAnimation setting only takes effect while [SwordBlock](/docs/modules/combat/swordblock) is enabled — it changes how your sword looks when blocking, letting you choose the classic 1.7-style block or a pushdown motion.

**Category:** Render
**Enabled by default:** Yes

### Settings

| Setting | Type | Default | Range | Description |
| --- | --- | --- | --- | --- |
| MainHand | Toggleable Group | On | — | Customizes the position, scale, and rotation of the item held in your main hand. |
| MainHand → ItemScale | Decimal | -1.25 | -5.0..5.0 | Scales the main-hand item model larger or smaller. |
| MainHand → X | Decimal | 0.0 | -5.0..5.0 | Shifts the main-hand item left or right. |
| MainHand → Y | Decimal | 0.0 | -5.0..5.0 | Shifts the main-hand item up or down. |
| MainHand → PositiveRotationX | Decimal | 0.0 | -50.0..50.0 | Adds rotation to the main-hand item around the X axis. |
| MainHand → PositiveRotationY | Decimal | 0.0 | -50.0..50.0 | Adds rotation to the main-hand item around the Y axis. |
| MainHand → PositiveRotationZ | Decimal | 0.0 | -50.0..50.0 | Adds rotation to the main-hand item around the Z axis. |
| OffHand | Toggleable Group | Off | — | Customizes the position, scale, and rotation of the item held in your off hand. |
| OffHand → ItemScale | Decimal | 0.0 | -5.0..5.0 | Scales the off-hand item model larger or smaller. |
| OffHand → X | Decimal | 0.0 | -1.0..1.0 | Shifts the off-hand item left or right. |
| OffHand → Y | Decimal | 0.0 | -1.0..1.0 | Shifts the off-hand item up or down. |
| OffHand → PositiveRotationX | Decimal | 0.0 | -50.0..50.0 | Adds rotation to the off-hand item around the X axis. |
| OffHand → PositiveRotationY | Decimal | 0.0 | -50.0..50.0 | Adds rotation to the off-hand item around the Y axis. |
| OffHand → PositiveRotationZ | Decimal | 0.0 | -50.0..50.0 | Adds rotation to the off-hand item around the Z axis. |
| EquipOffset | Toggleable Group | On | — | Controls the raise/equip motion that plays when switching or using items. |
| EquipOffset → Ignore | Multi-Select | [Blocking, Place] | [Blocking, Place, Amount] | Situations in which the equip motion is skipped. |
| SwingDuration | Integer | 12 | 1..20 | How long the arm swing animation lasts, in ticks — lower is faster. |
| BlockingAnimation | Mode Selector | Pushdown | [1.7, Pushdown] | Animation used while blocking with a sword (only active with SwordBlock enabled). |
| BlockingAnimation → [1.7] → Y | Decimal | 0.1 | 0.05..0.3 | Vertical offset of the item during the 1.7 blocking animation. |
| BlockingAnimation → [1.7] → SwingScale | Decimal | 0.9 | 0.1..1.0 | Scales how strongly the swing motion is applied during the 1.7 animation. |
| AirWalker | Toggle | false | — | Plays the walking leg animation even while you are in the air. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleAnimations.kt)*
