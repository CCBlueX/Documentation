## CrystalView

CrystalView lets you change how nearby End Crystals are drawn so they're easier to read at a glance — useful in crystal PvP where stacked or oddly placed crystals can clutter your view. You can shrink the model, reposition it, and tone down or speed up its motion to suit your taste.

Lower the **Size** and adjust **YTranslate** to keep crystals from overlapping each other or your aim, and use **SpinSpeed** and **Bounce** to control the spinning and floating animation. This pairs naturally with [CrystalAura](/docs/modules/combat/crystalaura) when you want a cleaner picture of the crystals being placed and broken around you.

This is a purely visual tweak — it changes only how crystals look on your screen and has no effect on hitboxes or gameplay.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
| --- | --- | --- | --- | --- |
| Size | Decimal | 0.3 | 0.1..1.5 | Scales the rendered crystal model larger or smaller. |
| YTranslate | Decimal | -0.5 | -2.0..2.0 | Shifts the crystal up or down from its normal position. |
| SpinSpeed | Decimal | 0.0 | 0.0..5.0 | Controls how fast the crystal spins; set to 0 to stop it spinning entirely. |
| Bounce | Decimal | 0.25 | -1.0..1.0 | Adjusts the up-and-down floating motion of the crystal. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleCrystalView.kt)*
