## AutoDodge

AutoDodge watches for incoming projectiles — arrows, spectral arrows, and thrown tridents — and automatically steers you out of their path before they hit. It predicts where each projectile is heading, works out whether your current course would put you in its line of fire, and nudges your movement sideways so the shot misses. Use it when you're fighting bow users or trident throwers and want to avoid chip damage without manually strafing every shot.

When a simple sidestep isn't enough to clear the danger in time, AutoDodge can escalate: with the right options enabled it will also turn you toward the safest spot, jump for extra momentum, and briefly speed up your movement to get clear before impact. By default it stays subtle and only adjusts your movement input, leaving your aim alone.

To avoid interfering with other things you might be doing, AutoDodge holds back in certain situations — for example while you have a menu open or are using an item — and you can fine-tune those exceptions with the Ignore setting. It also steps aside automatically while [Blink](/docs/modules/player/blink) is active, since your real position there isn't where the game shows you.

**Category:** Combat
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
| --- | --- | --- | --- | --- |
| Ignore | Multi-Select | OpenInventory, UsingItem | OpenInventory, UsingItem, UsingScaffold | Situations in which AutoDodge stays inactive so it doesn't get in your way. With OpenInventory it won't dodge while a menu or container is open, with UsingItem it pauses while you're eating, drinking, or holding a bow, and with UsingScaffold it stands down while [Scaffold](/docs/modules/world/scaffold) is running. |
| AllowRotationChange | Toggleable Group | Off | — | Allows AutoDodge to also turn your view toward the safest direction when a plain sidestep won't clear the projectile in time. This makes evasions more effective but is more noticeable to others. |
| AllowRotationChange → AllowJump | Toggle | false | — | When rotation changes are allowed, lets AutoDodge jump as well to gain extra momentum and reach safety faster, used only when it would actually help. |
| AllowTimer | Toggleable Group | Off | — | Allows AutoDodge to briefly speed up the game tick rate when an evasion is too tight to make on normal movement alone, buying you the extra distance needed to get clear. |
| AllowTimer → TimerSpeed | Decimal | 1.4 | 1.0..10.0 | How much faster than normal time runs during an emergency dodge. Higher values clear danger quicker but are more conspicuous and more likely to be flagged. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/autododge/ModuleAutoDodge.kt)*
