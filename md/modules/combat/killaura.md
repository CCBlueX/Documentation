## KillAura

KillAura automatically locks on to nearby enemies and attacks them on every available click according to your [Clicker](/docs/modules/shared-settings/clicker) schedule — without requiring you to click manually. It selects the best target within your configured [Range](/docs/modules/shared-settings/range), adjusts your view using [Rotations](/docs/modules/shared-settings/rotations) and [AimPoint](/docs/modules/shared-settings/aim-point), and fires attacks as fast as your attack cooldown and click settings allow. The **Requires** setting gates activation behind one or more conditions such as holding a weapon or pressing the attack key, giving you precise control over when the aura fires.

Several optional sub-systems extend the base behaviour. **AutoBlocking** makes KillAura shield or sword-block between swings, improving your effective defence. **FailSwing** performs a fake swing when no valid target is in reach, disguising KillAura's idle pattern from anti-cheat systems. **FightBot** (powered by [AutoWalk](/docs/modules/shared-settings/autowalk)) navigates you toward your target automatically, and **RangeIndicator** draws a ground circle showing your current attack radius. For a stronger setup, combine KillAura with [Velocity](/docs/modules/combat/velocity) to reduce incoming knockback and [AutoWeapon](/docs/modules/combat/autoweapon) to automatically switch to the best weapon for each target.

**Category:** Combat
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Clicker | Setting Group | — | — | See [Shared: Clicker](/docs/modules/shared-settings/clicker). |
| Range | Setting Group | — | — | See [Shared: Range](/docs/modules/shared-settings/range). |
| Target | Setting Group | — | — | See [Shared: Target](/docs/modules/shared-settings/target). |
| Rotations | Setting Group | — | — | See [Shared: Rotations](/docs/modules/shared-settings/rotations). |
| AimPoint | Setting Group | — | — | See [Shared: AimPoint](/docs/modules/shared-settings/aim-point). |
| Requires | Multi-Select | Weapon | Click \| Weapon \| EmptyHand \| VanillaName \| NotBreaking | Conditions that must all be met for KillAura to activate. `Click` requires the attack key to be held or recently pressed; `Weapon` requires a sword, axe, or mace in the main hand; `EmptyHand` requires an empty main hand; `VanillaName` requires no custom item name; `NotBreaking` requires that you are not currently mining a block. |
| Raycast | Choice | Enemy | None \| Enemy \| All | Which entities can obstruct the attack hit-ray. `None` ignores all obstructions; `Enemy` only considers attackable entities; `All` considers any entity including non-targets. |
| Criticals | Choice | Ignore | Smart \| Ignore \| Always | Critical-hit timing mode. `Smart` times attacks to land critical hits when possible; `Ignore` attacks without waiting for crit conditions; `Always` only attacks when a critical hit can be dealt. |
| KeepSprint | Toggle | false | — | When enabled, preserves your sprint momentum after each attack rather than letting it reset. |
| IgnoreOpenInventory | Toggle | true | — | When enabled, KillAura continues targeting and attacking even while your inventory or a container screen is open. |
| SimulateInventoryClosing | Toggle | true | — | Sends a fake inventory-close packet to the server before each attack, allowing hits while the inventory remains open on your client. |
| AutoBlocking | Toggleable Group | On | — | Automatically blocks with your shield or sword between attacks to improve your defence. |
| AutoBlocking → BlockMode | Choice | Fake | Basic \| Interact \| Fake | How the block action is sent. `Basic` uses a plain use-item packet; `Interact` right-clicks the entity or block in your crosshair; `Fake` only shows the blocking animation client-side without actually blocking on the server. |
| AutoBlocking → SimulateVanillaUse | Toggle | true | — | Makes the blocking interaction behave like a vanilla right-click, which is more consistent with normal gameplay and less detectable. |
| AutoBlocking → UnblockMode | Choice | StopUsingItem | StopUsingItem \| ChangeSlot \| SwapHand \| None | How KillAura cancels the block before each attack. `StopUsingItem` sends a release-item packet; `ChangeSlot` briefly switches hotbar slots; `SwapHand` sends two swap-hand packets; `None` keeps the block active during the attack. |
| AutoBlocking → Reblock | Integer Range | 0..0 | 0..3 ticks | Random delay in ticks before re-engaging the block after an attack. |
| AutoBlocking → PauseOnUnblock | Integer Range | 0..0 | 0..3 ticks | Random pause in ticks after unblocking before the next attack is allowed to fire. |
| AutoBlocking → Chance | Decimal | 100.0 | 0.0..100.0 % | Probability that AutoBlocking will attempt to block on each cycle. Lower values make blocking appear more randomised. |
| AutoBlocking → Blink | Integer | 0 | 0..10 ticks | Number of ticks to queue outgoing packets while blocking, simulating a brief connection lag. |
| AutoBlocking → PrioritizeBlocking | Toggle | true | — | Reduces attack rate to ensure a block is fully established before each strike. |
| AutoBlocking → OnScanRange | Toggle | false | — | Starts blocking when a target enters scan range but has not yet reached attack range. |
| AutoBlocking → OnlyWhenInDanger | Toggle | false | — | Restricts AutoBlocking to situations where a target is actively aiming at you. |
| AutoBlocking → AssumeShield | Toggle | false | — | Treats the main-hand item as shield-capable on servers that do not support the 1.9+ offhand protocol, useful for 1.8-based servers. |
| TargetRendering | Toggleable Group | On | — | See [Shared: TargetRendering](/docs/modules/shared-settings/target-rendering). |
| FailSwing | Toggleable Group | Off | — | Performs a fake swing when no valid target is in attack range, disguising KillAura's idle timing pattern from anti-cheat. |
| FailSwing → AdditionalRange | Decimal Range | 2.5..3.0 | 0.0..10.0 | Extra range beyond the normal attack range within which a fake swing can be triggered. |
| FailSwing → NotifyWhenFail | Mode Selector | Box | None \| Box \| Sound | Feedback when a swing misses. `None` gives no feedback; `Box` renders a small indicator at the missed hit position; `Sound` plays an audio click. |
| FailSwing → NotifyWhenFail → [Mode: Box] → Fade | Integer | 4 | 1..10 secs | How long the miss indicator box stays visible before fading out. |
| FailSwing → NotifyWhenFail → [Mode: Box] → Color | Color | — | — | Fill colour of the miss indicator box. |
| FailSwing → NotifyWhenFail → [Mode: Box] → Rainbow | Toggle | false | — | Cycles the miss indicator box through rainbow colours instead of using a fixed colour. |
| FailSwing → NotifyWhenFail → [Mode: Sound] → Volume | Decimal | 50.0 | 0.0..100.0 | Volume of the miss notification sound. |
| FailSwing → NotifyWhenFail → [Mode: Sound] → Pitch | Decimal | 0.8 | 0.0..2.0 | Pitch of the miss notification sound. |
| FightBot | Toggleable Group | Off | — | See [Shared: AutoWalk](/docs/modules/shared-settings/autowalk). |
| RangeIndicator | Toggleable Group | Off | — | Renders a circle on the ground around you visualising your current attack range. |
| RangeIndicator → ColorMode | Choice | Static | Static \| Rainbow \| Distance | Colour scheme for the range circle. `Static` blends between idle and active colours; `Rainbow` cycles through all hues; `Distance` interpolates colour based on how close the current target is. |
| RangeIndicator → IdleColor | Color | — | — | Colour of the range circle when no target is selected. |
| RangeIndicator → ActiveColor | Color | — | — | Colour of the range circle when a target is locked. |
| RangeIndicator → Outline | Toggle | true | — | Draws an outline along the edge of the range circle. |
| RangeIndicator → OutlineColor | Color | — | — | Colour of the range circle outline. |
| RangeIndicator → PulseAnimation | Toggle | false | — | Animates the circle with a rhythmic size pulse. |
| RangeIndicator → PulseSpeed | Decimal | 2.0 | 0.5..5.0 | Frequency of the pulse animation cycle. |
| RangeIndicator → PulseIntensity | Decimal | 0.15 | 0.05..0.5 | Amplitude of the pulse as a fraction of the circle radius. |
| RangeIndicator → FadeAnimation | Toggle | true | — | Smoothly transitions the circle between idle and active colours rather than switching instantly. |
| RangeIndicator → FadeSpeed | Decimal | 0.1 | 0.01..0.5 | Speed of the colour transition between idle and active states. |
| RangeIndicator → WallRangeColor | Color | — | — | Colour of the through-walls range ring. Set alpha to 0 to hide it. |
| RangeIndicator → ScanRangeColor | Color | — | — | Colour of the scan range ring. Set alpha to 0 to hide it. |
| RangeIndicator → OpponentRangeColor | Color | — | — | Colour of the opponent's estimated range ring. Set alpha to 0 to hide it. |
| RangeIndicator → HideWhenDead | Toggle | true | — | Hides the indicator while your character is dead. |
| RangeIndicator → HideWhenSpectator | Toggle | true | — | Hides the indicator while in spectator mode. |
| RangeIndicator → HideInVehicle | Toggle | false | — | Hides the indicator while you are riding a vehicle. |
| RangeIndicator → RespectInventorySetting | Toggle | true | — | Hides the indicator when a container is open and IgnoreOpenInventory is turned off. |
| RangeIndicator → CanBeCovered | Toggle | false | — | Allows blocks and terrain to render on top of the range circle, enabling depth testing. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/killaura/ModuleKillAura.kt)*
