## Hats

Hats is a purely cosmetic render feature that floats a decorative shape above a player's head. Pick from six styles — a spinning cone, a glowing halo, orbiting orbs, a flower, a star, or your own custom image — and tweak its size, colors, and spin to make it your own.

By default the hat only appears over your own head. You can also choose to show it above friends within a set distance. The hat normally hides while you're in first person, but you can keep it visible there, and it stays visible whenever [FreeLook](/docs/modules/render/freelook) is active so you can admire it. A height-offset curve lets the hat gently bob up and down over time, and an equipment offset nudges it upward when you're wearing a helmet so it doesn't clip into your gear. When a player takes damage, the hat can briefly flash red.

This is a visual-only module — it has no effect on gameplay and is purely for style.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| HeightOffset | Setting Group | — | — | Controls how the hat floats and bobs above the head over time. |
| HeightOffset → Period | Integer | 1000 | 10..20000 ms | Length of one full bob cycle. |
| HeightOffset → Symmetric | Toggle | true | — | Makes the up-and-down motion mirror evenly across the cycle. |
| HeightOffset → Height | Curve | — | — | The animation curve that shapes the height offset over the cycle. |
| Mode | Mode Selector | Image | — | The hat style to display: Cone, Halo, Orbs, Flower, Star, or Image. |
| Mode → [Cone] → FollowRotation | Toggle | false | — | Rotates the hat to face the same direction as the player. |
| Mode → [Cone] → EquipmentOffset | Setting Group | — | — | Raises the hat when a helmet is worn so it clears your gear. |
| Mode → [Cone] → EquipmentOffset → ArmorOffset | Decimal | 0.1 | 0.0..1.0 | Extra height added while a helmet is equipped. |
| Mode → [Cone] → ShowDamage | Toggle | true | — | Flashes the hat red when the player is hurt. |
| Mode → [Cone] → FriendsOptions | Setting Group | — | — | Controls showing the hat above friends. |
| Mode → [Cone] → FriendsOptions → ViewOnFriend | Toggle | true | — | Shows the hat above friends as well as yourself. |
| Mode → [Cone] → FriendsOptions → Distance | Integer | 64 | 8..512 blocks | Maximum distance at which a friend's hat is drawn. |
| Mode → [Cone] → FirstPersonView | Toggle | true | — | Keeps your own hat visible while in first person. |
| Mode → [Cone] → HatSettings | Setting Group | — | — | Shape settings for the Cone style. |
| Mode → [Cone] → HatSettings → Peak | Decimal | 0.3 | 0.01..2.0 | Height of the cone's point. |
| Mode → [Cone] → RadiusSettings | Setting Group | — | — | Size settings for the Cone style. |
| Mode → [Cone] → RadiusSettings → OuterRadius | Decimal | 0.6 | 0.1..2.0 | Width of the cone's base. |
| Mode → [Cone] → Colors | Setting Group | — | — | Color and color-spin settings for the hat. |
| Mode → [Cone] → Colors → SyncColors | Toggle | true | — | Uses a single color instead of blending between two. |
| Mode → [Cone] → Colors → FirstColor | Color | — | — | Primary hat color. |
| Mode → [Cone] → Colors → SecondColor | Color | — | — | Secondary color used when blending is enabled. |
| Mode → [Cone] → Colors → SpinSpeed | Decimal | 1.0 | 0.0..10.0 | How fast the colors cycle around the hat. |
| Mode → [Halo] → FollowRotation | Toggle | false | — | Rotates the hat to face the same direction as the player. |
| Mode → [Halo] → EquipmentOffset | Setting Group | — | — | Raises the hat when a helmet is worn so it clears your gear. |
| Mode → [Halo] → EquipmentOffset → ArmorOffset | Decimal | 0.1 | 0.0..1.0 | Extra height added while a helmet is equipped. |
| Mode → [Halo] → ShowDamage | Toggle | true | — | Flashes the hat red when the player is hurt. |
| Mode → [Halo] → FriendsOptions | Setting Group | — | — | Controls showing the hat above friends. |
| Mode → [Halo] → FriendsOptions → ViewOnFriend | Toggle | true | — | Shows the hat above friends as well as yourself. |
| Mode → [Halo] → FriendsOptions → Distance | Integer | 64 | 8..512 blocks | Maximum distance at which a friend's hat is drawn. |
| Mode → [Halo] → FirstPersonView | Toggle | true | — | Keeps your own hat visible while in first person. |
| Mode → [Halo] → HatSettings | Setting Group | — | — | Shape settings for the Halo style. |
| Mode → [Halo] → HatSettings → Radius | Decimal | 0.3 | 0.1..2.0 | Size of the halo ring. |
| Mode → [Halo] → HatSettings → Thickness | Decimal | 0.05 | 0.01..1.0 | Thickness of the halo ring. |
| Mode → [Halo] → Colors | Setting Group | — | — | Color and color-spin settings for the hat. |
| Mode → [Halo] → Colors → SyncColors | Toggle | true | — | Uses a single color instead of blending between two. |
| Mode → [Halo] → Colors → FirstColor | Color | — | — | Primary hat color. |
| Mode → [Halo] → Colors → SecondColor | Color | — | — | Secondary color used when blending is enabled. |
| Mode → [Halo] → Colors → SpinSpeed | Decimal | 1.0 | 0.0..10.0 | How fast the colors cycle around the hat. |
| Mode → [Orbs] → FollowRotation | Toggle | false | — | Rotates the hat to face the same direction as the player. |
| Mode → [Orbs] → EquipmentOffset | Setting Group | — | — | Raises the hat when a helmet is worn so it clears your gear. |
| Mode → [Orbs] → EquipmentOffset → ArmorOffset | Decimal | 0.1 | 0.0..1.0 | Extra height added while a helmet is equipped. |
| Mode → [Orbs] → ShowDamage | Toggle | true | — | Flashes the hat red when the player is hurt. |
| Mode → [Orbs] → FriendsOptions | Setting Group | — | — | Controls showing the hat above friends. |
| Mode → [Orbs] → FriendsOptions → ViewOnFriend | Toggle | true | — | Shows the hat above friends as well as yourself. |
| Mode → [Orbs] → FriendsOptions → Distance | Integer | 64 | 8..512 blocks | Maximum distance at which a friend's hat is drawn. |
| Mode → [Orbs] → FirstPersonView | Toggle | true | — | Keeps your own hat visible while in first person. |
| Mode → [Orbs] → color | Color | — | — | Color of the orbiting orbs. |
| Mode → [Orbs] → HatSettings | Setting Group | — | — | Shape and motion settings for the Orbs style. |
| Mode → [Orbs] → HatSettings → Radius | Decimal | 0.5 | 0.0..2.0 | Distance of the orbs from the center. |
| Mode → [Orbs] → HatSettings → Speed | Decimal | 0.5 | 0.1..10.0 | How fast the orbs orbit around the head. |
| Mode → [Orbs] → HatSettings → OrbsSize | Decimal | 0.1 | 0.01..0.5 | Size of each orb. |
| Mode → [Orbs] → HatSettings → OrbsCount | Integer | 6 | 1..12 | Number of orbs. |
| Mode → [Orbs] → HatSettings → SpinSpeed | Decimal | 2.0 | -10.0..10.0 | How fast each orb spins on itself; negative reverses direction. |
| Mode → [Orbs] → Wave | Toggleable Group | On | — | Makes the orbs rise and fall in a wave as they orbit. |
| Mode → [Orbs] → Wave → WaveHeight | Decimal | 0.1 | 0.01..1.0 | How high the orbs rise and fall. |
| Mode → [Orbs] → Wave → WaveSpeed | Decimal | 2.0 | 0.1..10.0 | How fast the wave motion moves. |
| Mode → [Flower] → FollowRotation | Toggle | false | — | Rotates the hat to face the same direction as the player. |
| Mode → [Flower] → EquipmentOffset | Setting Group | — | — | Raises the hat when a helmet is worn so it clears your gear. |
| Mode → [Flower] → EquipmentOffset → ArmorOffset | Decimal | 0.1 | 0.0..1.0 | Extra height added while a helmet is equipped. |
| Mode → [Flower] → ShowDamage | Toggle | true | — | Flashes the hat red when the player is hurt. |
| Mode → [Flower] → FriendsOptions | Setting Group | — | — | Controls showing the hat above friends. |
| Mode → [Flower] → FriendsOptions → ViewOnFriend | Toggle | true | — | Shows the hat above friends as well as yourself. |
| Mode → [Flower] → FriendsOptions → Distance | Integer | 64 | 8..512 blocks | Maximum distance at which a friend's hat is drawn. |
| Mode → [Flower] → FirstPersonView | Toggle | true | — | Keeps your own hat visible while in first person. |
| Mode → [Flower] → HatSettings | Setting Group | — | — | Shape settings for the Flower style. |
| Mode → [Flower] → HatSettings → Radius | Decimal | 0.3 | 0.1..2.0 | Overall size of the flower. |
| Mode → [Flower] → HatSettings → Thickness | Decimal | 0.05 | 0.01..1.0 | Thickness of the flower's outline. |
| Mode → [Flower] → HatSettings → Sharpness | Decimal | 0.6 | 0.1..0.9 | How pointed the petals are. |
| Mode → [Flower] → HatSettings → PetalCount | Integer | 5 | 5..15 | Number of petals. |
| Mode → [Flower] → HatSettings → SpinSpeed | Decimal | 1.0 | -10.0..10.0 | How fast the flower rotates; negative reverses direction. |
| Mode → [Flower] → Colors | Setting Group | — | — | Color and color-spin settings for the hat. |
| Mode → [Flower] → Colors → SyncColors | Toggle | true | — | Uses a single color instead of blending between two. |
| Mode → [Flower] → Colors → FirstColor | Color | — | — | Primary hat color. |
| Mode → [Flower] → Colors → SecondColor | Color | — | — | Secondary color used when blending is enabled. |
| Mode → [Flower] → Colors → SpinSpeed | Decimal | 1.0 | 0.0..10.0 | How fast the colors cycle around the hat. |
| Mode → [Star] → FollowRotation | Toggle | false | — | Rotates the hat to face the same direction as the player. |
| Mode → [Star] → EquipmentOffset | Setting Group | — | — | Raises the hat when a helmet is worn so it clears your gear. |
| Mode → [Star] → EquipmentOffset → ArmorOffset | Decimal | 0.1 | 0.0..1.0 | Extra height added while a helmet is equipped. |
| Mode → [Star] → ShowDamage | Toggle | true | — | Flashes the hat red when the player is hurt. |
| Mode → [Star] → FriendsOptions | Setting Group | — | — | Controls showing the hat above friends. |
| Mode → [Star] → FriendsOptions → ViewOnFriend | Toggle | true | — | Shows the hat above friends as well as yourself. |
| Mode → [Star] → FriendsOptions → Distance | Integer | 64 | 8..512 blocks | Maximum distance at which a friend's hat is drawn. |
| Mode → [Star] → FirstPersonView | Toggle | true | — | Keeps your own hat visible while in first person. |
| Mode → [Star] → HatSettings | Setting Group | — | — | Shape settings for the Star style. |
| Mode → [Star] → HatSettings → Radius | Decimal | 0.3 | 0.1..2.0 | Overall size of the star. |
| Mode → [Star] → HatSettings → Thickness | Decimal | 0.05 | 0.01..1.0 | Thickness of the star's outline. |
| Mode → [Star] → HatSettings → Sharpness | Decimal | 0.6 | 0.1..0.7 | How pointed the star's points are. |
| Mode → [Star] → HatSettings → PointsCount | Integer | 5 | 5..15 | Number of points on the star. |
| Mode → [Star] → HatSettings → SpinSpeed | Decimal | 1.0 | -10.0..10.0 | How fast the star rotates; negative reverses direction. |
| Mode → [Star] → Colors | Setting Group | — | — | Color and color-spin settings for the hat. |
| Mode → [Star] → Colors → SyncColors | Toggle | true | — | Uses a single color instead of blending between two. |
| Mode → [Star] → Colors → FirstColor | Color | — | — | Primary hat color. |
| Mode → [Star] → Colors → SecondColor | Color | — | — | Secondary color used when blending is enabled. |
| Mode → [Star] → Colors → SpinSpeed | Decimal | 1.0 | 0.0..10.0 | How fast the colors cycle around the hat. |
| Mode → [Image] → FollowRotation | Toggle | false | — | Rotates the hat to face the same direction as the player. |
| Mode → [Image] → EquipmentOffset | Setting Group | — | — | Raises the hat when a helmet is worn so it clears your gear. |
| Mode → [Image] → EquipmentOffset → ArmorOffset | Decimal | 0.1 | 0.0..1.0 | Extra height added while a helmet is equipped. |
| Mode → [Image] → ShowDamage | Toggle | true | — | Flashes the hat red when the player is hurt. |
| Mode → [Image] → FriendsOptions | Setting Group | — | — | Controls showing the hat above friends. |
| Mode → [Image] → FriendsOptions → ViewOnFriend | Toggle | true | — | Shows the hat above friends as well as yourself. |
| Mode → [Image] → FriendsOptions → Distance | Integer | 64 | 8..512 blocks | Maximum distance at which a friend's hat is drawn. |
| Mode → [Image] → FirstPersonView | Toggle | true | — | Keeps your own hat visible while in first person. |
| Mode → [Image] → Image | File | — | — | The image file used as the hat. |
| Mode → [Image] → ColorModulator | Color | — | — | Tints the image; leave white to keep original colors. |
| Mode → [Image] → Scale | Vector2_f | — | — | Width and height scaling of the image. |
| Mode → [Image] → SpinSpeed | Decimal | 1.0 | -10.0..10.0 | How fast the image spins; negative reverses direction. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/hats/ModuleHats.kt)*
