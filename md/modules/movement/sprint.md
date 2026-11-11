## Sprint

Sprint makes you run whenever you walk, so you never need to press the sprint key.

**Category:** Movement
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Choice | Legit | Legit, Omnidirectional, Omnirotational | Legit: sprints only forward, like normal. Omnidirectional: sprints in every direction, also sideways and backwards. Omnirotational: turns your character toward where you walk so you can keep sprinting. |
| Ignore | Multi-Select | None | Blindness, Hunger, Collision | Keeps sprinting even when you are blind, hungry, or bump into something. |
| StopOn | Multi-Select | Ground, Air, Sneaking, UsingItem | Ground, Air, Sneaking, UsingItem | Stops sprinting while you sneak or use an item. Ground and Air stop sprinting on the ground or in the air when another module turns you away from the way you walk. |

To keep sprinting after you hit someone, use [KeepSprint](/docs/modules/combat/keepsprint).

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/ModuleSprint.kt)*
