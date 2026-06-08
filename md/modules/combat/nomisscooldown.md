## NoMissCooldown

NoMissCooldown gives you finer control over what happens when you swing and miss an attack in Minecraft 1.9+ combat. Normally, missing a hit triggers a brief cooldown before you can deal full damage again — this module lets you suppress that penalty or stop the swing packet from being sent in the first place.

The two settings work independently and can be combined. **Remove Attack Cooldown** prevents the miss from resetting your attack cooldown timer, so your weapon stays at full charge and you can immediately land a full-damage hit on your next swing. **Cancel Attack On Miss** takes a different approach: instead of ignoring the cooldown penalty, it suppresses the attack packet entirely when no target is hit, meaning the server never sees the wasted swing at all. This can be useful for reducing detection surface on servers that flag excessive miss rates.

Both options are most effective alongside modules that help you land hits reliably, such as [KillAura](/docs/modules/combat/killaura), [Reach](/docs/modules/player/reach), or [Criticals](/docs/modules/combat/criticals).

**Category:** Combat
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| RemoveAttackCooldown | Toggle | false | — | When enabled, missing an attack does not trigger the 10-tick attack cooldown reset, keeping your weapon at full charge. |
| CancelAttackOnMiss | Toggle | true | — | When enabled, swings that do not connect with a target are cancelled entirely and not sent to the server. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/ModuleNoMissCooldown.kt)*
