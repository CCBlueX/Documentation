## Sprint

Sprint keeps you running automatically whenever you're moving, so you never have to hold down or tap the sprint key. As long as you have movement input, the client sprints for you, which is convenient for travel, combat, and any movement technique that relies on sustained sprinting.

The **Mode** setting controls how flexible the sprinting is. *Legit* behaves like normal vanilla sprinting (forward movement only) for a natural look. *Omnidirectional* lets you sprint in any direction — including sideways and backwards — which also enables sprint-jump boosts no matter which way you're heading. *Omnirotational* goes a step further by rotating your movement direction so you keep sprinting even when strafing, pairing well with combat and aim-based movement.

Use **Ignore** to keep sprinting in situations that would normally stop vanilla sprint, such as having Blindness, low hunger, or bumping into things. **StopOn** does the opposite: it tells Sprint when to back off, letting you make automatic sprinting look more legitimate (for example, stopping while sneaking or using an item). For keeping your sprint through hits in combat, see [KeepSprint](/docs/modules/combat/keepsprint).

**Category:** Movement
**Enabled by default:** Yes

### Settings

| Setting | Type | Default | Range | Description |
| --- | --- | --- | --- | --- |
| Mode | Choice | Legit | Legit, Omnidirectional, Omnirotational | How sprinting is applied: *Legit* mimics vanilla forward sprinting, *Omnidirectional* sprints in any direction and enables all-direction sprint-jump boosts, and *Omnirotational* rotates your movement so you keep sprinting while strafing. |
| Ignore | Multi-Select | [] | Blindness, Hunger, Collision | Conditions to ignore so sprinting continues anyway: Blindness effect, low hunger, and collisions with blocks or entities. |
| StopOn | Multi-Select | [Ground, Air] | Ground, Air, Sneaking, UsingItem | Situations where automatic sprinting should stop: while on the ground, while in the air, while sneaking, and while using an item. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/ModuleSprint.kt)*
