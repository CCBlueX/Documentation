## Hats

Render a hat above the player's head.

**Category:** Render  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── HeightOffset (Setting Group)
│   ├── Period (Integer | default: 1000 | range: 10..20000 | ms)
│   ├── Symmetric (Toggle | default: true)
│   └── Height (Curve)
└── Mode (Mode Selector | default: Cone | modes: Cone, Halo, Orbs, Flower, Star, Image)
    ├── [Mode: Cone]
    │   ├── FollowRotation (Toggle | default: false)
    │   ├── EquipmentOffset (Setting Group)
    │   │   └── ArmorOffset (Decimal | default: 0.1 | range: 0.0..1.0)
    │   ├── ShowDamage (Toggle | default: true)
    │   ├── FriendsOptions (Setting Group)
    │   │   ├── ViewOnFriend (Toggle | default: true)
    │   │   └── Distance (Integer | default: 64 | range: 8..512 | blocks)
    │   ├── FirstPersonView (Toggle | default: true)
    │   ├── HatSettings (Setting Group)
    │   │   └── Peak (Decimal | default: 0.3 | range: 0.01..2.0)
    │   ├── RadiusSettings (Setting Group)
    │   │   └── OuterRadius (Decimal | default: 0.6 | range: 0.1..2.0)
    │   └── Colors (Setting Group)
    │       ├── SyncColors (Toggle | default: true)
    │       ├── FirstColor (Color)
    │       ├── SecondColor (Color)
    │       └── SpinSpeed (Decimal | default: 1.0 | range: 0.0..10.0)
    ├── [Mode: Halo]
    │   ├── FollowRotation (Toggle | default: false)
    │   ├── EquipmentOffset (Setting Group)
    │   │   └── ArmorOffset (Decimal | default: 0.1 | range: 0.0..1.0)
    │   ├── ShowDamage (Toggle | default: true)
    │   ├── FriendsOptions (Setting Group)
    │   │   ├── ViewOnFriend (Toggle | default: true)
    │   │   └── Distance (Integer | default: 64 | range: 8..512 | blocks)
    │   ├── FirstPersonView (Toggle | default: true)
    │   ├── HatSettings (Setting Group)
    │   │   ├── Radius (Decimal | default: 0.3 | range: 0.1..2.0)
    │   │   └── Thickness (Decimal | default: 0.05 | range: 0.01..1.0)
    │   └── Colors (Setting Group)
    │       ├── SyncColors (Toggle | default: true)
    │       ├── FirstColor (Color)
    │       ├── SecondColor (Color)
    │       └── SpinSpeed (Decimal | default: 1.0 | range: 0.0..10.0)
    ├── [Mode: Orbs]
    │   ├── FollowRotation (Toggle | default: false)
    │   ├── EquipmentOffset (Setting Group)
    │   │   └── ArmorOffset (Decimal | default: 0.1 | range: 0.0..1.0)
    │   ├── ShowDamage (Toggle | default: true)
    │   ├── FriendsOptions (Setting Group)
    │   │   ├── ViewOnFriend (Toggle | default: true)
    │   │   └── Distance (Integer | default: 64 | range: 8..512 | blocks)
    │   ├── FirstPersonView (Toggle | default: true)
    │   ├── color (Color)
    │   ├── HatSettings (Setting Group)
    │   │   ├── Radius (Decimal | default: 0.5 | range: 0.0..2.0)
    │   │   ├── Speed (Decimal | default: 0.5 | range: 0.1..10.0)
    │   │   ├── OrbsSize (Decimal | default: 0.1 | range: 0.01..0.5)
    │   │   ├── OrbsCount (Integer | default: 6 | range: 1..12)
    │   │   └── SpinSpeed (Decimal | default: 2.0 | range: -10.0..10.0)
    │   └── Wave (Toggleable Group | default: on)
    │       ├── Enabled (Toggle | default: true)
    │       ├── WaveHeight (Decimal | default: 0.1 | range: 0.01..1.0)
    │       └── WaveSpeed (Decimal | default: 2.0 | range: 0.1..10.0)
    ├── [Mode: Flower]
    │   ├── FollowRotation (Toggle | default: false)
    │   ├── EquipmentOffset (Setting Group)
    │   │   └── ArmorOffset (Decimal | default: 0.1 | range: 0.0..1.0)
    │   ├── ShowDamage (Toggle | default: true)
    │   ├── FriendsOptions (Setting Group)
    │   │   ├── ViewOnFriend (Toggle | default: true)
    │   │   └── Distance (Integer | default: 64 | range: 8..512 | blocks)
    │   ├── FirstPersonView (Toggle | default: true)
    │   ├── HatSettings (Setting Group)
    │   │   ├── Radius (Decimal | default: 0.3 | range: 0.1..2.0)
    │   │   ├── Thickness (Decimal | default: 0.05 | range: 0.01..1.0)
    │   │   ├── Sharpness (Decimal | default: 0.6 | range: 0.1..0.9)
    │   │   ├── PetalCount (Integer | default: 5 | range: 5..15)
    │   │   └── SpinSpeed (Decimal | default: 1.0 | range: -10.0..10.0)
    │   └── Colors (Setting Group)
    │       ├── SyncColors (Toggle | default: true)
    │       ├── FirstColor (Color)
    │       ├── SecondColor (Color)
    │       └── SpinSpeed (Decimal | default: 1.0 | range: 0.0..10.0)
    ├── [Mode: Star]
    │   ├── FollowRotation (Toggle | default: false)
    │   ├── EquipmentOffset (Setting Group)
    │   │   └── ArmorOffset (Decimal | default: 0.1 | range: 0.0..1.0)
    │   ├── ShowDamage (Toggle | default: true)
    │   ├── FriendsOptions (Setting Group)
    │   │   ├── ViewOnFriend (Toggle | default: true)
    │   │   └── Distance (Integer | default: 64 | range: 8..512 | blocks)
    │   ├── FirstPersonView (Toggle | default: true)
    │   ├── HatSettings (Setting Group)
    │   │   ├── Radius (Decimal | default: 0.3 | range: 0.1..2.0)
    │   │   ├── Thickness (Decimal | default: 0.05 | range: 0.01..1.0)
    │   │   ├── Sharpness (Decimal | default: 0.6 | range: 0.1..0.7)
    │   │   ├── PointsCount (Integer | default: 5 | range: 5..15)
    │   │   └── SpinSpeed (Decimal | default: 1.0 | range: -10.0..10.0)
    │   └── Colors (Setting Group)
    │       ├── SyncColors (Toggle | default: true)
    │       ├── FirstColor (Color)
    │       ├── SecondColor (Color)
    │       └── SpinSpeed (Decimal | default: 1.0 | range: 0.0..10.0)
    └── [Mode: Image]
        ├── FollowRotation (Toggle | default: false)
        ├── EquipmentOffset (Setting Group)
        │   └── ArmorOffset (Decimal | default: 0.1 | range: 0.0..1.0)
        ├── ShowDamage (Toggle | default: true)
        ├── FriendsOptions (Setting Group)
        │   ├── ViewOnFriend (Toggle | default: true)
        │   └── Distance (Integer | default: 64 | range: 8..512 | blocks)
        ├── FirstPersonView (Toggle | default: true)
        ├── Image (File)
        ├── ColorModulator (Color)
        ├── Scale (2D Position)
        └── SpinSpeed (Decimal | default: 1.0 | range: -10.0..10.0)
```

### Settings Details

#### HeightOffset

A group of related settings.

- **Period** (Integer) — default: `1000`; range: `10` – `20000`; unit: ms — Duration of one height animation cycle.
- **Symmetric** (Toggle) — default: `true` — Makes the animation play forward then backward.
- **Height** (Curve) — Curve defining the vertical offset over time.

#### Mode

Select a mode for this feature. Available modes: **Cone**, **Halo**, **Orbs**, **Flower**, **Star**, **Image**. Default: **Cone**.

##### Mode: Cone

- **FollowRotation** (Toggle) — default: `false` — Rotates the hat to match the player's head rotation.
###### EquipmentOffset

A group of related settings.

- **ArmorOffset** (Decimal) — default: `0.1`; range: `0.0` – `1.0` — Extra height offset when wearing a helmet.

- **ShowDamage** (Toggle) — default: `true` — Turns the hat red when the player takes damage.
###### FriendsOptions

A group of related settings.

- **ViewOnFriend** (Toggle) — default: `true` — Renders the hat on friend players.
- **Distance** (Integer) — default: `64`; range: `8` – `512`; unit: blocks — Maximum distance to render hats on other players.

- **FirstPersonView** (Toggle) — default: `true` — Shows the hat in first-person perspective.
###### HatSettings

A group of related settings.

- **Peak** (Decimal) — default: `0.3`; range: `0.01` – `2.0` — Height of the cone's tip.

###### RadiusSettings

A group of related settings.

- **OuterRadius** (Decimal) — default: `0.6`; range: `0.1` – `2.0` — Radius of the cone's base.

###### Colors

A group of related settings.

- **SyncColors** (Toggle) — default: `true` — Uses the first color for both gradient endpoints.
- **FirstColor** (Color) — Primary gradient color.
- **SecondColor** (Color) — Secondary gradient color.
- **SpinSpeed** (Decimal) — default: `1.0`; range: `0.0` – `10.0` — Speed of the color rotation animation.


##### Mode: Halo

- **FollowRotation** (Toggle) — default: `false` — Rotates the hat to match the player's head rotation.
###### EquipmentOffset

A group of related settings.

- **ArmorOffset** (Decimal) — default: `0.1`; range: `0.0` – `1.0` — Extra height offset when wearing a helmet.

- **ShowDamage** (Toggle) — default: `true` — Turns the hat red when the player takes damage.
###### FriendsOptions

A group of related settings.

- **ViewOnFriend** (Toggle) — default: `true` — Renders the hat on friend players.
- **Distance** (Integer) — default: `64`; range: `8` – `512`; unit: blocks — Maximum distance to render hats on other players.

- **FirstPersonView** (Toggle) — default: `true` — Shows the hat in first-person perspective.
###### HatSettings

A group of related settings.

- **Radius** (Decimal) — default: `0.3`; range: `0.1` – `2.0` — Radius of the halo ring.
- **Thickness** (Decimal) — default: `0.05`; range: `0.01` – `1.0` — Thickness of the halo tube.

###### Colors

A group of related settings.

- **SyncColors** (Toggle) — default: `true` — Uses the first color for both gradient endpoints.
- **FirstColor** (Color) — Primary gradient color.
- **SecondColor** (Color) — Secondary gradient color.
- **SpinSpeed** (Decimal) — default: `1.0`; range: `0.0` – `10.0` — Speed of the color rotation animation.


##### Mode: Orbs

- **FollowRotation** (Toggle) — default: `false` — Rotates the hat to match the player's head rotation.
###### EquipmentOffset

A group of related settings.

- **ArmorOffset** (Decimal) — default: `0.1`; range: `0.0` – `1.0` — Extra height offset when wearing a helmet.

- **ShowDamage** (Toggle) — default: `true` — Turns the hat red when the player takes damage.
###### FriendsOptions

A group of related settings.

- **ViewOnFriend** (Toggle) — default: `true` — Renders the hat on friend players.
- **Distance** (Integer) — default: `64`; range: `8` – `512`; unit: blocks — Maximum distance to render hats on other players.

- **FirstPersonView** (Toggle) — default: `true` — Shows the hat in first-person perspective.
- **color** (Color) — Color of the orbiting spheres.
###### HatSettings

A group of related settings.

- **Radius** (Decimal) — default: `0.5`; range: `0.0` – `2.0` — Orbit radius of the orbs.
- **Speed** (Decimal) — default: `0.5`; range: `0.1` – `10.0` — Vertical bounce speed of the orbs.
- **OrbsSize** (Decimal) — default: `0.1`; range: `0.01` – `0.5` — Size of each individual orb.
- **OrbsCount** (Integer) — default: `6`; range: `1` – `12` — Number of orbiting orbs.
- **SpinSpeed** (Decimal) — default: `2.0`; range: `-10.0` – `10.0` — Horizontal spin speed of the orbs.

###### Wave

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true` — Toggles a vertical wave animation on the orbs.
- **WaveHeight** (Decimal) — default: `0.1`; range: `0.01` – `1.0` — Amplitude of the wave motion.
- **WaveSpeed** (Decimal) — default: `2.0`; range: `0.1` – `10.0` — Speed of the wave animation.


##### Mode: Flower

- **FollowRotation** (Toggle) — default: `false` — Rotates the hat to match the player's head rotation.
###### EquipmentOffset

A group of related settings.

- **ArmorOffset** (Decimal) — default: `0.1`; range: `0.0` – `1.0` — Extra height offset when wearing a helmet.

- **ShowDamage** (Toggle) — default: `true` — Turns the hat red when the player takes damage.
###### FriendsOptions

A group of related settings.

- **ViewOnFriend** (Toggle) — default: `true` — Renders the hat on friend players.
- **Distance** (Integer) — default: `64`; range: `8` – `512`; unit: blocks — Maximum distance to render hats on other players.

- **FirstPersonView** (Toggle) — default: `true` — Shows the hat in first-person perspective.
###### HatSettings

A group of related settings.

- **Radius** (Decimal) — default: `0.3`; range: `0.1` – `2.0` — Radius of the flower shape.
- **Thickness** (Decimal) — default: `0.05`; range: `0.01` – `1.0` — Thickness of the flower petals.
- **Sharpness** (Decimal) — default: `0.6`; range: `0.1` – `0.9` — How pointed the petal tips are.
- **PetalCount** (Integer) — default: `5`; range: `5` – `15` — Number of petals on the flower.
- **SpinSpeed** (Decimal) — default: `1.0`; range: `-10.0` – `10.0` — Rotation speed of the flower.

###### Colors

A group of related settings.

- **SyncColors** (Toggle) — default: `true` — Uses the first color for both gradient endpoints.
- **FirstColor** (Color) — Primary gradient color.
- **SecondColor** (Color) — Secondary gradient color.
- **SpinSpeed** (Decimal) — default: `1.0`; range: `0.0` – `10.0` — Speed of the color rotation animation.


##### Mode: Star

- **FollowRotation** (Toggle) — default: `false` — Rotates the hat to match the player's head rotation.
###### EquipmentOffset

A group of related settings.

- **ArmorOffset** (Decimal) — default: `0.1`; range: `0.0` – `1.0` — Extra height offset when wearing a helmet.

- **ShowDamage** (Toggle) — default: `true` — Turns the hat red when the player takes damage.
###### FriendsOptions

A group of related settings.

- **ViewOnFriend** (Toggle) — default: `true` — Renders the hat on friend players.
- **Distance** (Integer) — default: `64`; range: `8` – `512`; unit: blocks — Maximum distance to render hats on other players.

- **FirstPersonView** (Toggle) — default: `true` — Shows the hat in first-person perspective.
###### HatSettings

A group of related settings.

- **Radius** (Decimal) — default: `0.3`; range: `0.1` – `2.0` — Radius of the star shape.
- **Thickness** (Decimal) — default: `0.05`; range: `0.01` – `1.0` — Thickness of the star arms.
- **Sharpness** (Decimal) — default: `0.6`; range: `0.1` – `0.7` — How pointed the star tips are.
- **PointsCount** (Integer) — default: `5`; range: `5` – `15` — Number of points on the star.
- **SpinSpeed** (Decimal) — default: `1.0`; range: `-10.0` – `10.0` — Rotation speed of the star.

###### Colors

A group of related settings.

- **SyncColors** (Toggle) — default: `true` — Uses the first color for both gradient endpoints.
- **FirstColor** (Color) — Primary gradient color.
- **SecondColor** (Color) — Secondary gradient color.
- **SpinSpeed** (Decimal) — default: `1.0`; range: `0.0` – `10.0` — Speed of the color rotation animation.


##### Mode: Image

- **FollowRotation** (Toggle) — default: `false` — Rotates the hat to match the player's head rotation.
###### EquipmentOffset

A group of related settings.

- **ArmorOffset** (Decimal) — default: `0.1`; range: `0.0` – `1.0` — Extra height offset when wearing a helmet.

- **ShowDamage** (Toggle) — default: `true` — Turns the hat red when the player takes damage.
###### FriendsOptions

A group of related settings.

- **ViewOnFriend** (Toggle) — default: `true` — Renders the hat on friend players.
- **Distance** (Integer) — default: `64`; range: `8` – `512`; unit: blocks — Maximum distance to render hats on other players.

- **FirstPersonView** (Toggle) — default: `true` — Shows the hat in first-person perspective.
- **Image** (File) — Image file to render as the hat.
- **ColorModulator** (Color) — Tint color applied to the image.
- **Scale** (2D Position) — Width and height scale of the image.
- **SpinSpeed** (Decimal) — default: `1.0`; range: `-10.0` – `10.0` — Rotation speed of the image.


### Screenshots

*Screenshots for Hats will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Frender%2Fhats%2FModuleHats.kt)*
