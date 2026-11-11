## Criticals

A critical hit does extra damage, but normally only when you are falling while you hit. Criticals makes more of your hits critical, either by doing a tiny jump for you or by making the server think you are in the air. Which mode works best depends on the server's anticheat.

**Category:** Combat
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Choice | Packet | None, Packet, NoGround, Jump, Blink, Timer | How critical hits are made. Packet and NoGround make the server think you are in the air. Jump does a small jump before you hit. Blink holds back your movement until a critical hit is possible. Timer slows the game down near enemies so you fall longer. |
| Mode → [Packet] → Mode | Choice | NCP-2024-01-25 | Vanilla, NCP-2024-01-25, Falling, Low, Down, Grim-2.3.59, BlocksMC | Which anticheat to work against. Pick the one the server uses. |
| Mode → [Packet] → PacketType | Choice | Full | OnGroundOnly, PositionAndOnGround, LookAndOnGround, Full | What kind of movement message is sent. |
| Mode → [Jump] → Height | Decimal | 0.42 | 0.1..0.42 | How high the small jump is. |
| Mode → [Jump] → Range | Decimal | 4.0 | 1.0..6.0 | Only jumps when an enemy is this close, in blocks. |
| Mode → [Jump] → OptimizeForCooldown | Toggle | true | | Times the jump so you land the hit when your attack is fully charged. |
| Mode → [Jump] → CheckKillaura | Toggle | false | | Only jumps while [KillAura](/docs/modules/combat/killaura) is on. |
| Mode → [Jump] → CheckAutoClicker | Toggle | false | | Only jumps while [AutoClicker](/docs/modules/combat/autoclicker) is on. |
| Mode → [Jump] → CheckTriggerBot | Toggle | false | | Only jumps while [TriggerBot](/docs/modules/combat/triggerbot) is on. |
| Mode → [Jump] → CanBeSeen | Toggle | true | | Only jumps when you can see the enemy. |
| Mode → [Blink] → Delay | Integer Range | 300..600 | 0..1000 ms | How long your movement is held back. A random value from the range is used. |
| Mode → [Blink] → Range | Decimal | 4.0 | 0.0..10.0 | Only works when an enemy is this close, in blocks. |
| Mode → [Timer] → Speed | Decimal | 0.8 | 0.1..1.0 | How fast the game runs near enemies. 1.0 is normal speed. |
| Mode → [Timer] → Range | Decimal | 4.0 | 0.0..10.0 | Only works when an enemy is this close, in blocks. |
| WhenSprinting | Toggleable Group | Off | | Sprinting stops critical hits. This stops your sprint when you are about to hit, so the hit can be critical. |
| WhenSprinting → StopSprinting | Choice | Legit | None, Legit, OnNetwork, OnAttack | How your sprint is stopped. None keeps sprinting. Legit stops sprinting like a player would. OnNetwork only tells the server you stopped. OnAttack stops it right when you hit. |
| WhenSprinting → Range | Decimal | 4.0 | 0.0..10.0 | Only works when an enemy is this close, in blocks. |
| Visuals | Toggleable Group | Off | | Shows extra critical hit particles. |
| Visuals → Fake | Toggle | false | | Shows the particles on every hit, even ones that are not critical. |
| Visuals → Critical | Integer | 1 | 0..20 | How many critical hit particle bursts to show. |
| Visuals → Magic | Integer | 0 | 0..20 | How many enchanted hit particle bursts to show. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/criticals/ModuleCriticals.kt)*
