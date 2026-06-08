## Criticals

In vanilla Minecraft a critical hit deals roughly 50% bonus damage, but only when you're falling through the air at the moment you attack — you can't be on the ground, in water, on a ladder, and so on. Criticals takes care of this for you, landing a crit on (almost) every hit instead of only when you happen to be falling. It's a staple companion to melee modules like [KillAura](/docs/modules/combat/killaura) and [AutoClicker](/docs/modules/combat/autoclicker).

The **Mode** setting decides *how* the crit is achieved. Jump physically performs a tiny hop so you're falling when the hit lands. Packet and NoGround instead manipulate your movement packets so the server believes you're in the air without you actually moving much, which makes them far harder to detect — but the right choice depends on the server's anti-cheat. Timer briefly bends game speed to squeeze a fall in before the hit, and Blink holds packets back until a crit is possible. Pick the mode that matches the anti-cheat you're up against; the packet-based options include presets tuned for common systems.

Sprinting normally cancels critical hits, so the **WhenSprinting** group can briefly drop your sprint around an attack to let the crit go through. **Visuals** controls the crit star/particles, letting you show extra effects or even fake them when no real crit happened.

**Category:** Combat
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | Jump | None, Packet, NoGround, Jump, Blink, Timer | Selects the method used to land critical hits. |
| Mode → Packet → Mode | Choice | NoCheatPlus | Vanilla, NoCheatPlus, Falling, Low, Down, Grim, BlocksMC | Anti-cheat preset that shapes the fake movement packets. Choose the one matching the server. |
| Mode → Packet → PacketType | Choice | Full | OnGroundOnly, PositionAndOnGround, LookAndOnGround, Full | Which kind of movement packet is sent. Full carries the most data and works with every preset. |
| Mode → Jump → Height | Decimal | 0.42 | 0.1..0.42 | How high the automatic hop is. Lower values are subtler but still enough to crit. |
| Mode → Jump → Range | Decimal | 1.0 | 1.0..6.0 | Only hops when an enemy is within this distance, so you don't jump for no reason. |
| Mode → Jump → OptimizeForCooldown | Toggle | true | — | Times the hop to your attack cooldown so the crit lands with a fully charged hit. |
| Mode → Jump → CheckKillaura | Toggle | true | — | Only auto-hops while [KillAura](/docs/modules/combat/killaura) is active. |
| Mode → Jump → CheckAutoClicker | Toggle | false | — | Only auto-hops while [AutoClicker](/docs/modules/combat/autoclicker) is active. |
| Mode → Jump → CanBeSeen | Toggle | true | — | Requires line of sight to the enemy before hopping. |
| Mode → Blink → Delay | Integer Range | 50..50 | 0..1000 ms | How long packets are held back while waiting for a crit opportunity. A random value in this range is used each time. |
| Mode → Blink → Range | Decimal | 4.0 | 0.0..10.0 | Only engages when an enemy is within this distance. |
| Mode → Timer → Speed | Decimal | 0.8 | 0.1..1.0 | Game-speed factor applied near an enemy to create a fall window. Lower is slower and more noticeable. |
| Mode → Timer → Range | Decimal | 4.0 | 0.0..10.0 | Only adjusts timer speed when an enemy is within this distance. |
| WhenSprinting | Toggleable Group | On | — | Manages your sprint around attacks so sprinting doesn't cancel the crit. |
| WhenSprinting → StopSprinting | Choice | Legit | None, Legit, OnNetwork, OnAttack | How sprint is dropped: not at all, naturally (Legit), at the network level, or right when you attack. |
| WhenSprinting → Range | Decimal | 4.0 | 0.0..10.0 | Distance at which an enemy counts for the sprint handling. |
| Visuals | Toggleable Group | On | — | Controls the critical-hit particle effects. |
| Visuals → Fake | Toggle | false | — | Shows crit particles even when the hit isn't actually a critical. |
| Visuals → Critical | Integer | 1 | 0..20 | Number of normal crit particle bursts to display per hit. |
| Visuals → Magic | Integer | 0 | 0..20 | Number of enchant/magic crit particle bursts to display per hit. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/criticals/ModuleCriticals.kt)*
