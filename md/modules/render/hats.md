## Hats

Hats puts a shape above your head just for looks. You can pick a cone, a halo, flying orbs, a flower, a star or your own picture, and change its size, colors and spin. It does nothing in the game.

The hat can also show above your friends. It turns red for a moment when the player gets hurt. In first person it stays visible unless you turn off **FirstPersonView**, and it always shows while [FreeLook](/docs/modules/render/freelook) is on. The hat moves up a bit when you wear a helmet. With **HeightOffset** you can make it float up and down.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| HeightOffset | Setting Group | | | Makes the hat float up and down. |
| HeightOffset → Period | Integer | 1000 | 10 to 20000 ms | How long one up-and-down move takes. |
| HeightOffset → Symmetric | Toggle | true | | Makes the way down the same as the way up. |
| HeightOffset → Height | Curve | Flat at 0.2 | Progress 0 to 1, Offset 0 to 2 | How high the hat is at each point of the move. |
| Mode | Mode Selector | Cone | Cone, Halo, Orbs, Flower, Star, Image | Which hat to show. |
| Mode → (all) → FollowRotation | Toggle | false | | Turns the hat with your head. |
| Mode → (all) → EquipmentOffset → ArmorOffset | Decimal | 0.1 | 0.0 to 1.0 | How much higher the hat sits when you wear a helmet. |
| Mode → (all) → ShowDamage | Toggle | true | | Turns the hat red when the player gets hurt. |
| Mode → (all) → FriendsOptions → ViewOnFriend | Toggle | true | | Also shows the hat on your friends. |
| Mode → (all) → FriendsOptions → Distance | Integer | 64 | 8 to 512 blocks | How far away friends still get a hat. |
| Mode → (all) → FirstPersonView | Toggle | true | | Shows your own hat in first person. |
| Mode → Cone → HatSettings → Peak | Decimal | 0.3 | 0.01 to 2.0 | How tall the cone is. |
| Mode → Cone → RadiusSettings → OuterRadius | Decimal | 0.6 | 0.1 to 2.0 | How wide the cone is. |
| Mode → Cone → Colors → SyncColors | Toggle | true | | Uses only the first color instead of mixing both. |
| Mode → Cone → Colors → FirstColor | Color | LiquidBounce blue | | The main color. |
| Mode → Cone → Colors → SecondColor | Color | Light LiquidBounce blue | | The second color, used when SyncColors is off. |
| Mode → Cone → Colors → SpinSpeed | Decimal | 1.0 | 0.0 to 10.0 | How fast the colors move around the hat. |
| Mode → Halo → HatSettings → Radius | Decimal | 0.3 | 0.1 to 2.0 | Size of the ring. |
| Mode → Halo → HatSettings → Thickness | Decimal | 0.05 | 0.01 to 1.0 | How thick the ring is. |
| Mode → Halo → Colors → SyncColors | Toggle | true | | Uses only the first color instead of mixing both. |
| Mode → Halo → Colors → FirstColor | Color | LiquidBounce blue | | The main color. |
| Mode → Halo → Colors → SecondColor | Color | Light LiquidBounce blue | | The second color, used when SyncColors is off. |
| Mode → Halo → Colors → SpinSpeed | Decimal | 1.0 | 0.0 to 10.0 | How fast the colors move around the hat. |
| Mode → Orbs → color | Color | LiquidBounce blue | | Color of the orbs. |
| Mode → Orbs → HatSettings → Radius | Decimal | 0.5 | 0.0 to 2.0 | How far the orbs fly from your head. |
| Mode → Orbs → HatSettings → Speed | Decimal | 0.5 | 0.1 to 10.0 | How fast the orbs fly around. |
| Mode → Orbs → HatSettings → OrbsSize | Decimal | 0.1 | 0.01 to 0.5 | Size of each orb. |
| Mode → Orbs → HatSettings → OrbsCount | Integer | 6 | 1 to 12 | How many orbs there are. |
| Mode → Orbs → HatSettings → SpinSpeed | Decimal | 2.0 | -10.0 to 10.0 | How fast each orb spins. Below 0 it spins the other way. |
| Mode → Orbs → Wave | Toggleable Group | On | | Makes the orbs go up and down as they fly around. |
| Mode → Orbs → Wave → WaveHeight | Decimal | 0.1 | 0.01 to 1.0 | How far up and down they go. |
| Mode → Orbs → Wave → WaveSpeed | Decimal | 2.0 | 0.1 to 10.0 | How fast they go up and down. |
| Mode → Flower → HatSettings → Radius | Decimal | 0.3 | 0.1 to 2.0 | Size of the flower. |
| Mode → Flower → HatSettings → Thickness | Decimal | 0.05 | 0.01 to 1.0 | How thick the flower's line is. |
| Mode → Flower → HatSettings → Sharpness | Decimal | 0.6 | 0.1 to 0.9 | How pointy the petals are. |
| Mode → Flower → HatSettings → PetalCount | Integer | 5 | 5 to 15 | How many petals there are. |
| Mode → Flower → HatSettings → SpinSpeed | Decimal | 1.0 | -10.0 to 10.0 | How fast the flower spins. Below 0 it spins the other way. |
| Mode → Flower → Colors → SyncColors | Toggle | true | | Uses only the first color instead of mixing both. |
| Mode → Flower → Colors → FirstColor | Color | LiquidBounce blue | | The main color. |
| Mode → Flower → Colors → SecondColor | Color | Light LiquidBounce blue | | The second color, used when SyncColors is off. |
| Mode → Flower → Colors → SpinSpeed | Decimal | 1.0 | 0.0 to 10.0 | How fast the colors move around the hat. |
| Mode → Star → HatSettings → Radius | Decimal | 0.3 | 0.1 to 2.0 | Size of the star. |
| Mode → Star → HatSettings → Thickness | Decimal | 0.05 | 0.01 to 1.0 | How thick the star's line is. |
| Mode → Star → HatSettings → Sharpness | Decimal | 0.6 | 0.1 to 0.7 | How pointy the star is. |
| Mode → Star → HatSettings → PointsCount | Integer | 5 | 5 to 15 | How many points the star has. |
| Mode → Star → HatSettings → SpinSpeed | Decimal | 1.0 | -10.0 to 10.0 | How fast the star spins. Below 0 it spins the other way. |
| Mode → Star → Colors → SyncColors | Toggle | true | | Uses only the first color instead of mixing both. |
| Mode → Star → Colors → FirstColor | Color | LiquidBounce blue | | The main color. |
| Mode → Star → Colors → SecondColor | Color | Light LiquidBounce blue | | The second color, used when SyncColors is off. |
| Mode → Star → Colors → SpinSpeed | Decimal | 1.0 | 0.0 to 10.0 | How fast the colors move around the hat. |
| Mode → Image → Image | File | | PNG, JPG | The picture to use as your hat. |
| Mode → Image → ColorModulator | Color | White | | Tints the picture. White keeps its own colors. |
| Mode → Image → Scale | Vector | 1, 1 | | Width and height of the picture. |
| Mode → Image → SpinSpeed | Decimal | 1.0 | -10.0 to 10.0 | How fast the picture spins. Below 0 it spins the other way. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/hats/ModuleHats.kt)*
