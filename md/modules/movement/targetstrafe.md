## TargetStrafe

Automatically strafes around enemies targeted by KillAura.

**Category:** Movement  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Mode (Mode Selector | default: Motion | modes: Motion, Input)
│   └── [Mode: Motion]
│       └── Hypixel (Toggle | default: false)
├── Range (Decimal | default: 2.95 | range: 0.0..8.0)
├── FollowRange (Decimal | default: 4.0 | range: 0.0..10.0)
├── Requirements (Multi-Select | options: Space, Speed, KillAura, Ground)
├── Planner (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   ├── ControlDirection (Toggle | default: true)
│   ├── Validation (Toggleable Group | default: on)
│   │   ├── Enabled (Toggle | default: true)
│   │   ├── EdgeCheck (Toggleable Group | default: on)
│   │   │   ├── Enabled (Toggle | default: true)
│   │   │   └── MaxFallHeight (Decimal | default: 1.2 | range: 0.1..4.0)
│   │   └── VoidCheck (Toggleable Group | default: on)
│   │       ├── Enabled (Toggle | default: true)
│   │       └── SafetyExpand (Decimal | default: 0.1 | range: 0.0..5.0)
│   └── AdaptiveRange (Toggleable Group | default: off)
│       ├── Enabled (Toggle | default: false)
│       ├── MaxRange (Decimal | default: 4.0 | range: 1.0..5.0)
│       └── RangeStep (Decimal | default: 0.5 | range: 0.1..1.0)
└── Visuals (Toggleable Group | default: on)
    ├── Enabled (Toggle | default: true)
    ├── Width (Decimal | default: 0.12 | range: 0.01..1.0)
    ├── HeightOffset (Decimal | default: 0.05 | range: -1.0..1.0)
    ├── OuterColor (Color)
    ├── InnerColor (Color)
    ├── OutlineColor (Color)
    ├── ShowNextPoint (Toggle | default: true)
    ├── PointRadius (Decimal | default: 0.18 | range: 0.05..1.0)
    ├── PointColor (Color)
    ├── PointOutlineColor (Color)
    ├── InvalidPointColor (Color)
    └── InvalidPointOutlineColor (Color)
```

### Settings Details

#### Mode

Select how the strafe is applied. Available modes: **Motion**, **Input**. Default: **Motion**.

##### Mode: Motion

Directly overrides your movement vector to orbit the target — strongest, but more obvious server-side.

- **Hypixel** (Toggle) — default: `false` — Applies Hypixel-specific speed adjustments while strafing (works together with Speed).

##### Mode: Input

Steers by rewriting your movement keys instead of the motion vector — looks more legit at the cost of precision.

- **Range** (Decimal) — default: `2.95`; range: `0.0` – `8.0` — Orbit radius the strafe tries to keep around the target.
- **FollowRange** (Decimal) — default: `4.0`; range: `0.0` – `10.0` — Maximum distance to keep following and strafing around a target.
- **Requirements** (Multi-Select) — options: `Space`, `Speed`, `KillAura`, `Ground` — Conditions that must all be met for strafing to activate.

#### Planner

A toggleable group of settings (default: enabled). Plans the next safe strafe position.

- **Enabled** (Toggle) — default: `true`
- **ControlDirection** (Toggle) — default: `true` — Lets your left/right keys choose which way to orbit.
##### Validation

A toggleable group of settings (default: enabled). Rejects strafe positions that are unsafe to step onto.

- **Enabled** (Toggle) — default: `true`
###### EdgeCheck

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true` — Prevents strafing off ledges.
- **MaxFallHeight** (Decimal) — default: `1.2`; range: `0.1` – `4.0` — Maximum drop height still considered safe.

###### VoidCheck

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true` — Prevents strafing into the void.
- **SafetyExpand** (Decimal) — default: `0.1`; range: `0.0` – `5.0` — Extra margin added to the void safety check.

##### AdaptiveRange

A toggleable group of settings (default: disabled). Shrinks the orbit radius when the planned position is blocked.

- **Enabled** (Toggle) — default: `false`
- **MaxRange** (Decimal) — default: `4.0`; range: `1.0` – `5.0` — Largest radius tried when adapting.
- **RangeStep** (Decimal) — default: `0.5`; range: `0.1` – `1.0` — Step size between radius attempts.

#### Visuals

A toggleable group of settings (default: enabled). Draws the orbit circle and the next-point marker.

- **Enabled** (Toggle) — default: `true`
- **Width** (Decimal) — default: `0.12`; range: `0.01` – `1.0` — Thickness of the orbit ring.
- **HeightOffset** (Decimal) — default: `0.05`; range: `-1.0` – `1.0` — Vertical offset of the visuals.
- **OuterColor** (Color) — Outer fill color of the orbit ring.
- **InnerColor** (Color) — Inner fill color of the orbit ring.
- **OutlineColor** (Color) — Outline color of the orbit ring.
- **ShowNextPoint** (Toggle) — default: `true` — Draws a marker at the next planned strafe position.
- **PointRadius** (Decimal) — default: `0.18`; range: `0.05` – `1.0` — Size of the next-point marker.
- **PointColor** (Color) — Fill color when the next point is valid.
- **PointOutlineColor** (Color) — Outline color when the next point is valid.
- **InvalidPointColor** (Color) — Fill color when the next point is unsafe.
- **InvalidPointOutlineColor** (Color) — Outline color when the next point is unsafe.

### Screenshots

*Screenshots for TargetStrafe will be added in a future update.*

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfc/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fmovement%2FModuleTargetStrafe.kt)*
