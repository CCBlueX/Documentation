## AutoBow

AutoBow helps you with bows, crossbows and tridents. It can aim at enemies for you, let go of the shot when it is charged, and make your bow charge faster. Each of the three parts can be turned on and off on its own.

**Category:** Combat
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| AutoShoot | Toggleable Group | On | | Lets go of the shot by itself when your weapon is charged and you are aiming at an enemy. |
| AutoShoot → Charged | Integer | 15 | 3..20 ticks | How long to pull the bow before shooting, in ticks (20 per second). Longer means a stronger shot. |
| AutoShoot → ChargedRandom | Decimal Range | 0.0..0.0 | -10.0..10.0 ticks | A random amount added to Charged, so every shot is a bit different. |
| AutoShoot → DelayBetweenShots | Decimal | 0.0 | 0.0..5.0 s | How long to wait after a shot before shooting again. |
| AutoShoot → AimThreshold | Decimal | 1.5 | 1.0..4.0 ° | How close your aim has to be to the enemy before shooting. |
| AutoShoot → RequiresHypotheticalHit | Toggle | false | | Only shoots if the arrow would really hit an enemy. |
| AutoShoot → UsePrechargedCrossbow | Toggle | false | | Also shoots a crossbow that is already loaded. |
| BowAimbot | Toggleable Group | On | | Aims at enemies for you. It aims higher for far enemies, because arrows fall down as they fly. |
| BowAimbot → Target | Setting Group | | | See [Shared: Target](/docs/modules/shared-settings/target). |
| BowAimbot → Rotations | Setting Group | | | See [Shared: Rotations](/docs/modules/shared-settings/rotations). |
| BowAimbot → ThroughWalls | Toggle | true | | Also aims at enemies behind blocks. |
| BowAimbot → TargetRendering | Toggleable Group | On | | See [Shared: TargetRendering](/docs/modules/shared-settings/targetrendering). |
| FastCharge | Toggleable Group | Off | | Makes your bow charge faster. Most anticheats notice this, so it works best on servers without one. |
| FastCharge → Speed | Integer | 20 | 3..20 | How much faster the bow charges. |
| FastCharge → NotInTheAir | Toggle | true | | Does not charge faster while you are in the air. |
| FastCharge → NotDuringMove | Toggle | false | | Does not charge faster while you are moving. |
| FastCharge → NotDuringRegeneration | Toggle | false | | Does not charge faster while you have Regeneration. |
| FastCharge → PacketType | Choice | Full | OnGroundOnly, PositionAndOnGround, LookAndOnGround, Full | What kind of movement message is sent to charge faster. Try another one if a server does not like the current one. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/aimbot/ModuleAutoBow.kt)*
