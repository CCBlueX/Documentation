## Trajectories

Trajectories draws a predicted arc for projectiles — arrows, ender pearls, splash potions, tridents, and more — directly in the 3D world so you can see exactly where they will land before or after they are thrown. It is enabled by default, giving you an immediate visual edge when lining up long-range bow shots, ender pearl teleports, or potion throws.

The module can preview paths for your own held items as well as projectiles already airborne, and can optionally show the same information for other nearby players. The **Show** setting controls which of these scenarios are active: `AlwaysShowBow` lets you see the arrow arc even while your bow is only partially drawn; `OtherPlayers` reveals where nearby players' held throwables are aimed; `ActiveTrajectoryArrow` and `ActiveTrajectoryOther` track arrows and other live projectiles already in flight. Use **TrajectoryTypes** to limit rendering to only the projectile types you care about. Pair Trajectories with [AutoBow](/docs/modules/combat/autobow) or [Aimbot](/docs/modules/combat/aimbot) to get a clearer picture of where your shots will land.

The optional **ShowDetailedInfo** overlay adds an on-screen label beside each trajectory showing flight time, distance to the landing spot, the item icon, and the thrower's name — useful for reading incoming enemy pearl plays or coordinating grenade timing in PvP.

**Category:** Render
**Enabled by default:** Yes

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| MaxSimulatedTicks | Integer | 240 | 1–1000 ticks | How many game ticks ahead the trajectory path is simulated. Higher values extend the visible arc but cover less ground for fast projectiles like arrows. |
| MaxRenderDistance | Integer | 96 | 16–512 m | Maximum distance from your camera at which trajectories are drawn. Projectiles beyond this range are not shown. |
| CullBehindPlayer | Toggle | false | — | When enabled, trajectories located behind you (behind your view direction) are hidden, reducing clutter outside your field of view. |
| ShowMultiShot | Toggle | true | — | When enabled, a separate arc is drawn for each arrow fired by a multi-shot crossbow. Disable to show only the centre shot. |
| TrajectoryTypes | Multi-Select | Arrow, Potion, EnderPearl, FishingBobber, Trident, Snowball, Egg, ExpBottle, Fireball, WindCharge | — | Which projectile types have their paths rendered. Deselect any entry to hide that projectile type entirely. FireworkRocket is available but off by default. |
| Show | Multi-Select | OtherPlayers, ActiveTrajectoryArrow | — | Controls when and for whom trajectories appear. `AlwaysShowBow` previews your bow arc even before it is fully drawn. `OtherPlayers` shows predicted arcs for nearby players' held throwables. `ActiveTrajectoryArrow` tracks arrows already in flight. `ActiveTrajectoryOther` tracks other live projectiles in flight. |
| ShowDetailedInfo | Toggleable Group | Off | — | When enabled, overlays an info label on each trajectory showing flight time, distance, item icon, and owner name. Sub-settings below control what is shown and how it looks. |
| ShowDetailedInfo → ShowAt | Choice | Entity | — | Determines where the info label is anchored in the world: `Owner` places it at the thrower, `Entity` follows the projectile itself, `Landing` pins it at the predicted impact point. |
| ShowDetailedInfo → Item | Toggle | true | — | Show the projectile's item icon in the info overlay. |
| ShowDetailedInfo → OwnerName | Toggle | true | — | Show the name of the player who threw or shot the projectile. |
| ShowDetailedInfo → Distance | Toggle | true | — | Show the distance from your position to the predicted landing point. |
| ShowDetailedInfo → DurationUnit | Choice | Ticks | — | Whether flight time is displayed in game ticks (`Ticks`) or as a decimal seconds value (`Seconds`). |
| ShowDetailedInfo → Color | Color | — | — | Text colour used for the overlay labels. |
| ShowDetailedInfo → Scale | Decimal | 1.0 | 0.25–4.0 | Scale multiplier applied to the overlay text and icon. Values below 1.0 shrink the label; values above 1.0 enlarge it. |
| ShowDetailedInfo → RenderOffset | Vector3_d | — | — | Shifts the label's world anchor position by this (X, Y, Z) offset, allowing fine-tuned placement relative to the chosen `ShowAt` point. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/trajectories/ModuleTrajectories.kt)*
