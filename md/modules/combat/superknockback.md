## SuperKnockback

SuperKnockback maximises the knockback you deal when hitting enemies. In vanilla Minecraft, sprint-attacking an entity only applies extra knockback if the game registers you as actively sprinting at the moment of impact. This module manipulates your sprint state around each hit so that the knockback bonus is consistently applied, even against targets that would otherwise be invulnerable to it due to their hurt timer.

Three modes are available. **Packet** sends sprint-state packets in quick succession at the moment of attack, instantly toggling sprint off and back on at the network level without visibly interrupting your movement. **SprintTap** briefly suppresses your sprint in-game after a hit and re-enables it after a short configurable delay, mimicking the manual "sprint-tap" technique. **WTap** instead momentarily blocks your forward movement input after a hit — similar to the classic "w-tap" PvP technique — which resets your sprint and re-applies the knockback boost.

You can limit when the module activates using the **Conditions** filter (e.g. only fire while not in water, only while you are facing the target, or only while on the ground) and the **OnlyOnMove** group, which prevents the module from triggering when you are standing still. The **HurtTime** threshold lets you skip hits on enemies that were hit too recently to receive full knockback, and **Chance** lets you apply the effect only a percentage of the time for a more natural appearance.

**Category:** Combat
**Enabled by default:** Yes

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | SprintTap | Packet, SprintTap, WTap | The technique used to boost knockback on hit. |
| Mode → [SprintTap] → ReSprint | Integer Range | 0..1 | 0..10 ticks | How many ticks to wait before re-enabling sprint after a hit. |
| Mode → [WTap] → UntilMovementBlock | Integer Range | 1..1 | 0..10 ticks | Ticks to wait after a hit before blocking forward movement. |
| Mode → [WTap] → UntilAllowedMovement | Integer Range | 1..1 | 0..10 ticks | Ticks to wait after movement is blocked before restoring it. |
| HurtTime | Integer | 4 | 0..10 | Only applies the knockback boost if the target's hurt timer is at or below this value. |
| Chance | Decimal | 100.0 | 0.0..100.0 % | Probability (in percent) that the knockback boost fires on any given hit. |
| Conditions | Multi-Select | NotInWater | OnlyFacing, OnlyOnGround, NotInWater | Extra conditions that must all be met for the module to act. |
| OnlyOnMove | Toggleable Group | on | — | Only activate when you are moving. |
| OnlyOnMove → OnlyForward | Toggle | true | — | When enabled, the module also requires you to be moving forward (not just sideways). |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/ModuleSuperKnockback.kt)*
