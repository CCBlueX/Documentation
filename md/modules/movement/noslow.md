## NoSlow

Cancels slowness effects caused by blocks and using items.

**Category:** Movement  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Blocking (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   ├── Forward (Decimal | default: 1.0 | range: 0.0..1.0)
│   ├── Sideways (Decimal | default: 1.0 | range: 0.0..1.0)
│   ├── OnlySlowOnServerSide (Toggle | default: false)
│   └── Choice (Mode Selector | default: None | modes: None, Reuse, Switch, Blink, Interact, Grim2360, Grim2364-1.8, Grim2371, InvalidHand, Intave14)
│       ├── [Mode: Reuse]
│       │   └── Timing (Choice | default: PRE_POST | options: PreAndPost, Pre, Post)
│       ├── [Mode: Switch]
│       │   └── Timing (Choice | default: PRE_POST | options: PreAndPost, Pre, Post)
├── Consume (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   ├── Forward (Decimal | default: 1.0 | range: 0.0..1.0)
│   ├── Sideways (Decimal | default: 1.0 | range: 0.0..1.0)
│   ├── NoBlockInteract (Toggleable Group | default: on)
│   │   └── Enabled (Toggle | default: true)
│   └── Mode (Mode Selector | default: None | modes: None, Grim2360, Grim2364-1.8, InvalidHand, Grim2371, Intave14, Release)
│       ├── [Mode: Intave14]
│       │   └── Mode (Choice | default: RELEASE | options: Release, New)
├── Bow (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   ├── Forward (Decimal | default: 1.0 | range: 0.0..1.0)
│   ├── Sideways (Decimal | default: 1.0 | range: 0.0..1.0)
│   ├── Choice (Mode Selector | default: None | modes: None, Grim2360, Grim2364-1.8, Grim2371, InvalidHand)
│   └── NoBlockInteract (Toggleable Group | default: on)
│       └── Enabled (Toggle | default: true)
├── Bundle (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   ├── Forward (Decimal | default: 1.0 | range: 0.0..1.0)
│   └── Sideways (Decimal | default: 1.0 | range: 0.0..1.0)
├── Sneaking (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   ├── MinMultiplier (Decimal | default: 1.0 | range: 0.3..1.0)
│   └── Mode (Mode Selector | default: None | modes: None, Switch, AAC5)
│       ├── [Mode: Switch]
│       │   └── Timing (Choice | default: PRE_POST | options: PreAndPost, Pre, Post)
│       └── [Mode: AAC5]
│           └── Timing (Choice | default: PRE_POST | options: PreAndPost, Pre, Post)
├── Soulsand (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   └── Multiplier (Decimal | default: 1.0 | range: 0.4..2.0)
├── SlimeBlock (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   └── Multiplier (Decimal | default: 1.0 | range: 0.4..2.0)
├── HoneyBlock (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   └── Multiplier (Decimal | default: 1.0 | range: 0.4..2.0)
├── PowderSnow (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   └── Multiplier (Decimal | default: 1.0 | range: 0.4..2.0)
├── Fluid (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   └── Collision (Toggle | default: true)
└── Slowness (Toggleable Group | default: on)
    ├── Enabled (Toggle | default: true)
    └── PerLevelMultiplier (Decimal | default: 0.0 | range: 0.0..0.15)
```

### Settings Details

#### Blocking

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Forward** (Decimal) — default: `1.0`; range: `0.0` – `1.0`
- **Sideways** (Decimal) — default: `1.0`; range: `0.0` – `1.0`
- **OnlySlowOnServerSide** (Toggle) — default: `false`
##### Choice

Select a mode for this feature. Available modes: **None**, **Reuse**, **Switch**, **Blink**, **Interact**, **Grim2360**, **Grim2364-1.8**, **Grim2371**, **InvalidHand**, **Intave14**. Default: **None**.

###### Mode: Reuse

- **Timing** (Choice) — default: `PRE_POST`; options: `PreAndPost`, `Pre`, `Post`

###### Mode: Switch

- **Timing** (Choice) — default: `PRE_POST`; options: `PreAndPost`, `Pre`, `Post`


#### Consume

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Forward** (Decimal) — default: `1.0`; range: `0.0` – `1.0`
- **Sideways** (Decimal) — default: `1.0`; range: `0.0` – `1.0`
##### NoBlockInteract

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`

##### Mode

Select a mode for this feature. Available modes: **None**, **Grim2360**, **Grim2364-1.8**, **InvalidHand**, **Grim2371**, **Intave14**, **Release**. Default: **None**.

###### Mode: Intave14

- **Mode** (Choice) — default: `RELEASE`; options: `Release`, `New`


#### Bow

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Forward** (Decimal) — default: `1.0`; range: `0.0` – `1.0`
- **Sideways** (Decimal) — default: `1.0`; range: `0.0` – `1.0`
##### Choice

Select a mode for this feature. Available modes: **None**, **Grim2360**, **Grim2364-1.8**, **Grim2371**, **InvalidHand**. Default: **None**.

##### NoBlockInteract

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`


#### Bundle

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Forward** (Decimal) — default: `1.0`; range: `0.0` – `1.0`
- **Sideways** (Decimal) — default: `1.0`; range: `0.0` – `1.0`

#### Sneaking

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **MinMultiplier** (Decimal) — default: `1.0`; range: `0.3` – `1.0`
##### Mode

Select a mode for this feature. Available modes: **None**, **Switch**, **AAC5**. Default: **None**.

###### Mode: Switch

- **Timing** (Choice) — default: `PRE_POST`; options: `PreAndPost`, `Pre`, `Post`

###### Mode: AAC5

- **Timing** (Choice) — default: `PRE_POST`; options: `PreAndPost`, `Pre`, `Post`


#### Soulsand

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Multiplier** (Decimal) — default: `1.0`; range: `0.4` – `2.0`

#### SlimeBlock

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Multiplier** (Decimal) — default: `1.0`; range: `0.4` – `2.0`

#### HoneyBlock

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Multiplier** (Decimal) — default: `1.0`; range: `0.4` – `2.0`

#### PowderSnow

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Multiplier** (Decimal) — default: `1.0`; range: `0.4` – `2.0`

#### Fluid

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Collision** (Toggle) — default: `true`

#### Slowness

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **PerLevelMultiplier** (Decimal) — default: `0.0`; range: `0.0` – `0.15`


### Screenshots

*Screenshots for NoSlow will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fmovement%2FModuleNoSlow.kt)*
