## CrystalView

CrystalView changes how End Crystals look on your screen. You can make them smaller, move them down, and change how they spin and bounce. This helps in crystal PvP, for example with [CrystalAura](/docs/modules/combat/crystalaura). Hitboxes stay the same.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Size | Decimal | 0.3 | 0.1..1.5 | Size of the crystal. |
| YTranslate | Decimal | -0.5 | -2.0..2.0 | Moves the crystal up or down. |
| SpinSpeed | Decimal | 0.0 | 0.0..5.0 | How fast the crystal spins. 0 stops it. |
| Bounce | Decimal | 0.25 | -1.0..1.0 | How much the crystal floats up and down. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleCrystalView.kt)*
