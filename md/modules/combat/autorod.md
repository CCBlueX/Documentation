## AutoRod

AutoRod automatically casts a fishing rod at nearby enemies during combat to knock them back, interrupt their movement, and disrupt their aim — a common tactic on PvP servers for creating distance or breaking an opponent's combo. When a valid target enters your configured range and you're aiming close enough to it, AutoRod selects a fishing rod, casts it, waits for the hook to land or time out, and then reels it back in.

You can choose how it leads the shot with **GravityType**: a simple straight-line aim or a projectile-arc prediction that accounts for the rod bobber's drop, which lands more reliably at longer distances. A set of requirement and ignore conditions lets you keep it from firing at the wrong moments — for example while your inventory is open, while you're eating, or while holding items like a bow or pearl. It also stands down automatically while [Blink](/docs/modules/player/blink), [Scaffold](/docs/modules/world/scaffold), or [Freeze](/docs/modules/movement/freeze) are active.

For finer aim and targeting control, AutoRod shares the standard [Target](/docs/modules/shared-settings/target), [AimPoint](/docs/modules/shared-settings/aim-point), and [Rotations](/docs/modules/shared-settings/rotations) groups, so you can tune which enemies it prefers and how naturally it turns toward them.

**Category:** Combat
**Enabled by default:** Yes

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| GravityType | Choice | Projectile | Linear, Projectile | How the cast is aimed — Linear points straight at the target, Projectile predicts the bobber's arc for more accurate long-range casts. |
| Range | Decimal Range | 3.5..5.0 | 2.0..10.0 | The distance window, in blocks, within which an enemy can be rodded. |
| ScanExtraRange | Decimal Range | 3.0..3.0 | 0.0..5.0 | Extra reach randomly added on top of Range for each cast, varying your effective distance. |
| MaxEnemiesNearby | Integer | 1 | 0..10 | Only act when at most this many enemies are in range (0 means no limit). |
| MinHealth | Decimal | 10.0 | 1.0..20.0 | Won't use the rod while your own health is at or below this value. |
| MinTargetHealth | Decimal | 4.0 | 1.0..20.0 | Only targets enemies with more health than this. |
| Requires | Multi-Select | [] | Click, Weapon, VanillaName, NotBreaking | Conditions that must all be met before AutoRod will fire. |
| Ignore | Multi-Select | [] | OpenInventory, UsingItem, HoldingConsumable | Situations in which AutoRod stays inactive. |
| HoldingItemsForIgnore | Registry List | — | — | Items that, while held in your main hand, prevent the rod from being used. |
| Target | Setting Group | — | — | See [Shared: Target](/docs/modules/shared-settings/target). |
| AimPoint | Setting Group | — | — | See [Shared: AimPoint](/docs/modules/shared-settings/aim-point). |
| Rotations | Setting Group | — | — | See [Shared: Rotations](/docs/modules/shared-settings/rotations). |
| AimOffThreshold | Decimal | 5.0 | 2.0..10.0 | Maximum angle, in degrees, between your aim and the target before the rod is cast. |
| SwingMode | Choice | DoNotHide | DoNotHide, HideForBoth, HideForClient, HideForServer | Controls whether and how the arm swing is shown when using the rod. |
| TargetRendering | Toggleable Group | On | — | See [Shared: TargetRendering](/docs/modules/shared-settings/target-rendering). |
| HitTimeout | Integer | 30 | 5..200 ticks | Maximum time to wait after casting before reeling the rod back in. |
| PullOnOutOfRange | Toggle | true | — | Reel the rod in immediately if the target leaves your range. |
| SlotResetDelay | Integer Range | 0..0 | 0..20 ticks | Delay before switching away from the rod slot after pulling. |
| Cooldown | Integer Range | 4..8 | 1..50 ticks | Wait time between consecutive rod uses. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/ModuleAutoRod.kt)*
