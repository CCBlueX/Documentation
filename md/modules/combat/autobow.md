## AutoBow

AutoBow takes the manual work out of using a bow. It can aim at nearby enemies for you, decide the perfect moment to release a charged shot, and even speed up how quickly your bow draws. It also understands crossbows (including ones you've pre-charged) and tridents, so it stays useful whatever ranged weapon you're holding.

The module is split into three independent parts. **BowAimbot** lines your shot up with a target, accounting for arrow drop and travel time. **AutoShoot** fires once the weapon is charged enough and your aim is on target. **FastCharge** reduces the time needed to fully draw a bow. You can turn each part on or off separately, so you might use just the aim assist, just the auto-release, or all three together.

Keep in mind that FastCharge relies on packet tricks that work best on vanilla servers — most anti-cheats detect and block faster-than-normal bow drawing, so use it with care.

**Category:** Combat
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| AutoShoot | Toggleable Group | Off | — | Automatically releases your shot once the weapon is charged and your aim meets the conditions below. |
| AutoShoot → Charged | Integer | 20 ticks | 3–20 ticks | How long the bow must be drawn before AutoShoot will fire it. Higher means a more powerful shot. |
| AutoShoot → ChargedRandom | Decimal Range | 0.0–0.0 ticks | -10.0–10.0 ticks | Adds a randomized amount of extra (or reduced) charge time so each shot's timing varies, looking less robotic. |
| AutoShoot → DelayBetweenShots | Decimal | 0.0 s | 0.0–5.0 s | Minimum wait after a shot before the next one is allowed. |
| AutoShoot → AimThreshold | Decimal | 1.5° | 1.0–4.0° | How closely your aim must match the target before firing. Smaller values demand more precise alignment. |
| AutoShoot → RequiresHypotheticalHit | Toggle | false | — | Only fires when a simulated arrow along your current aim would actually strike an enemy. |
| AutoShoot → UsePrechargedCrossbow | Toggle | true | — | Allows firing a crossbow that is already loaded, even if you're not actively drawing it. |
| BowAimbot | Toggleable Group | On | — | Automatically aims at enemies, compensating for arrow drop and flight time. |
| BowAimbot → ThroughWalls | Toggle | true | — | Lets the aim assist target enemies even when there's terrain between you and them. |
| BowAimbot → Target | Setting Group | — | — | See [Shared: Target](/docs/modules/shared-settings/target). |
| BowAimbot → Rotations | Setting Group | — | — | See [Shared: Rotations](/docs/modules/shared-settings/rotations). |
| BowAimbot → TargetRendering | Toggleable Group | On | — | See [Shared: TargetRendering](/docs/modules/shared-settings/target-rendering). |
| FastCharge | Toggleable Group | Off | — | Speeds up how fast the bow charges. Best used only on vanilla servers, as anti-cheats often detect it. |
| FastCharge → Speed | Integer | 20 | 3–20 | How aggressively the charge is sped up each tick — higher draws faster. |
| FastCharge → NotInTheAir | Toggle | true | — | Pauses fast charging while you're off the ground. |
| FastCharge → NotDuringMove | Toggle | false | — | Pauses fast charging while you're moving. |
| FastCharge → NotDuringRegeneration | Toggle | false | — | Pauses fast charging while you have the Regeneration effect. |
| FastCharge → PacketType | Choice | Full | OnGroundOnly, PositionAndOnGround, LookAndOnGround, Full | Which kind of movement packet is used to speed up the charge — change this if a server reacts badly to one type. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/aimbot/ModuleAutoBow.kt)*
