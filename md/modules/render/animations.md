## Animations

Allows you to modify many of game's animations.

**Category:** Render  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── MainHand (Toggleable Group | default: off)
│   ├── Enabled (Toggle | default: false)
│   ├── ItemScale (Decimal | default: 0.0 | range: -5.0..5.0)
│   ├── X (Decimal | default: 0.0 | range: -5.0..5.0)
│   ├── Y (Decimal | default: 0.0 | range: -5.0..5.0)
│   ├── PositiveRotationX (Decimal | default: 0.0 | range: -50.0..50.0)
│   ├── PositiveRotationY (Decimal | default: 0.0 | range: -50.0..50.0)
│   └── PositiveRotationZ (Decimal | default: 0.0 | range: -50.0..50.0)
├── OffHand (Toggleable Group | default: off)
│   ├── Enabled (Toggle | default: false)
│   ├── ItemScale (Decimal | default: 0.0 | range: -5.0..5.0)
│   ├── X (Decimal | default: 0.0 | range: -1.0..1.0)
│   ├── Y (Decimal | default: 0.0 | range: -1.0..1.0)
│   ├── PositiveRotationX (Decimal | default: 0.0 | range: -50.0..50.0)
│   ├── PositiveRotationY (Decimal | default: 0.0 | range: -50.0..50.0)
│   └── PositiveRotationZ (Decimal | default: 0.0 | range: -50.0..50.0)
├── EquipOffset (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   └── Ignore (Multi-Select | default: [Blocking, Place] | options: Blocking, Place, Amount)
├── SwingDuration (Integer | default: 6 | range: 1..20)
├── BlockingAnimation (Mode Selector | default: 1.7 | modes: 1.7, Pushdown)
│   ├── [Mode: 1.7]
│   │   ├── Y (Decimal | default: 0.1 | range: 0.05..0.3)
│   │   └── SwingScale (Decimal | default: 0.9 | range: 0.1..1.0)
└── AirWalker (Toggle | default: false)
```

### Settings Details

#### MainHand

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false` — Toggles main hand item position and rotation customization.
- **ItemScale** (Decimal) — default: `0.0`; range: `-5.0` – `5.0` — Adjusts the scale of the item held in the main hand.
- **X** (Decimal) — default: `0.0`; range: `-5.0` – `5.0` — Horizontal position offset of the main hand item.
- **Y** (Decimal) — default: `0.0`; range: `-5.0` – `5.0` — Vertical position offset of the main hand item.
- **PositiveRotationX** (Decimal) — default: `0.0`; range: `-50.0` – `50.0` — Rotation offset around the X axis for the main hand item.
- **PositiveRotationY** (Decimal) — default: `0.0`; range: `-50.0` – `50.0` — Rotation offset around the Y axis for the main hand item.
- **PositiveRotationZ** (Decimal) — default: `0.0`; range: `-50.0` – `50.0` — Rotation offset around the Z axis for the main hand item.

#### OffHand

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false` — Toggles off hand item position and rotation customization.
- **ItemScale** (Decimal) — default: `0.0`; range: `-5.0` – `5.0` — Adjusts the scale of the item held in the off hand.
- **X** (Decimal) — default: `0.0`; range: `-1.0` – `1.0` — Horizontal position offset of the off hand item.
- **Y** (Decimal) — default: `0.0`; range: `-1.0` – `1.0` — Vertical position offset of the off hand item.
- **PositiveRotationX** (Decimal) — default: `0.0`; range: `-50.0` – `50.0` — Rotation offset around the X axis for the off hand item.
- **PositiveRotationY** (Decimal) — default: `0.0`; range: `-50.0` – `50.0` — Rotation offset around the Y axis for the off hand item.
- **PositiveRotationZ** (Decimal) — default: `0.0`; range: `-50.0` – `50.0` — Rotation offset around the Z axis for the off hand item.

#### EquipOffset

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true` — Toggles equip animation offset customization.
- **Ignore** (Multi-Select) — default: `Blocking`, `Place`; options: `Blocking`, `Place`, `Amount` — Conditions under which the equip offset animation is skipped.

- **SwingDuration** (Integer) — default: `6`; range: `1` – `20` — Duration of the arm swing animation in ticks.
#### BlockingAnimation

Select a mode for this feature. Available modes: **1.7**, **Pushdown**. Default: **1.7**.

##### Mode: 1.7

- **Y** (Decimal) — default: `0.1`; range: `0.05` – `0.3` — Vertical translation applied during the 1.7-style blocking animation.
- **SwingScale** (Decimal) — default: `0.9`; range: `0.1` – `1.0` — Scale factor for the swing progress during blocking.

- **AirWalker** (Toggle) — default: `false` — Applies the walk animation even while the player is airborne.

### Screenshots

*Screenshots for Animations will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Frender%2FModuleAnimations.kt)*
