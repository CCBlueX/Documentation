## Trajectories

Trajectories draws the path that an arrow, ender pearl, potion or other thrown item will fly, so you can see where it lands before you throw. It can also show the paths of things already flying and of items other players hold.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| MaxSimulatedTicks | Integer | 240 | 1 to 1000 ticks | How far ahead the path is worked out, in ticks (20 per second). |
| MaxRenderDistance | Integer | 96 | 16 to 512 m | Paths farther away than this are not drawn. |
| CullBehindPlayer | Toggle | false | | Hides paths behind you. |
| ShowMultiShot | Toggle | true | | Draws one path per arrow for a crossbow with Multishot. Higher Multishot levels add more arrows and a wider spread, up to 16 paths. |
| LineWidth | Decimal | 1.0 | 1.0 to 16.0 | Thickness of the paths for items you or other players hold. |
| ActiveLineWidth | Decimal | 2.0 | 1.0 to 16.0 | Thickness of the paths for things already flying. |
| TrajectoryTypes | Multi-Select | All | Arrow, Potion, EnderPearl, FishingBobber, Trident, Snowball, Egg, ExpBottle, FireworkRocket, Fireball, WindCharge | Which kinds of projectiles get a path. At least one must stay on. |
| Show | Multi-Select | OtherPlayers, ActiveTrajectoryArrow | AlwaysShowBow, OtherPlayers, ActiveTrajectoryArrow, ActiveTrajectoryOther | **AlwaysShowBow** shows a fully drawn shot for a bow you hold even when you are not drawing it. **OtherPlayers** shows paths for items other players hold. **ActiveTrajectoryArrow** shows paths of arrows already flying. **ActiveTrajectoryOther** does the same for other flying projectiles. |
| ShowDetailedInfo | Toggleable Group | off | | Adds a label to each path with the flight time, distance, item and thrower. |
| ShowDetailedInfo → ShowAt | Choice | Entity | Owner, Entity, Landing | Where the label sits: at the thrower, at the projectile, or where it will land. |
| ShowDetailedInfo → Item | Toggle | true | | Shows the item icon. |
| ShowDetailedInfo → OwnerName | Toggle | true | | Shows who threw or shot it. |
| ShowDetailedInfo → Distance | Toggle | true | | Shows how far away the landing spot is. |
| ShowDetailedInfo → TimeUnit | Choice | Ticks | Ticks, Seconds | Shows the flight time in ticks or seconds. |
| ShowDetailedInfo → Color | Color | White | | Text color of the label. |
| ShowDetailedInfo → Scale | Curve | | Distance 0 to 200, Scale 0.25 to 4 | Size of the label at each distance. |
| ShowDetailedInfo → RenderOffset | Vector | 0, 0, 0 | | Moves the label by this many blocks (X, Y, Z). |
| ShowDetailedInfo → RenderOffscreen | Toggleable Group | on | | Keeps labels of off-screen paths at the screen edge with an arrow pointing to them. |
| ShowDetailedInfo → RenderOffscreen → EdgeInset | Decimal | 0.0 | 0.0 to 0.9 | Moves those labels inward from the screen border. 0.1 keeps them 10% away from each edge. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/trajectories/ModuleTrajectories.kt)*
