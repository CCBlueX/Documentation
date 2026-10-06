## AntiAFK

AntiAFK keeps you active in the eyes of the server so you don't get kicked or moved to a lobby for standing still. While it's on, it performs small automatic actions — turning your view, swinging your arm, jumping, or shuffling around — on a repeating timer so the server registers you as a live player.

Pick a behavior with **Mode**. **RandomInteraction** (the default) fires a random mix of the actions you select on a randomized timer, which makes the activity look less robotic. **Old** is a simple fallback that just spins you around and walks forward. **Custom** lets you build your own combination of rotating, swinging, jumping, and walking with individual toggles and delays.

This is handy on servers with strict AFK timers when you need to step away briefly. Keep in mind the movement actions will physically move your character, so only use it somewhere safe where wandering won't get you killed or dropped into a hazard.

**Category:** Player
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
| --- | --- | --- | --- | --- |
| Mode | Mode Selector | RandomInteraction | Old, RandomInteraction, Custom | Chooses how AntiAFK keeps you active. |
| Mode → [RandomInteraction] → Interaction | Multi-Select | SwingHand, Yaw, Pitch | Jump, SwingHand, ChangeSlot, Yaw, Pitch, RandomDirection | Which actions are randomly performed to stay active. |
| Mode → [RandomInteraction] → Delay | Integer Range | 4..7 | 0..20 (ticks) | Random wait between actions, picked from this range. |
| Mode → [Custom] → Rotate | Toggleable Group | On | — | Periodically turns your view to register activity. |
| Mode → [Custom] → Rotate → IgnoreOpenInventory | Toggle | true | — | Keep rotating even while an inventory or other screen is open. |
| Mode → [Custom] → Rotate → Rotations | Setting Group | — | — | See [Shared: Rotations](/docs/modules/shared-settings/rotations). |
| Mode → [Custom] → Rotate → Delay | Integer | 5 | 0..20 (ticks) | Wait between each rotation. |
| Mode → [Custom] → Rotate → Angle | Decimal | 1.0 | -180.0..180.0 | How far your view turns each time. |
| Mode → [Custom] → Swing | Toggleable Group | On | — | Periodically swings your arm. |
| Mode → [Custom] → Swing → Delay | Integer | 5 | 0..20 (ticks) | Wait between each arm swing. |
| Mode → [Custom] → Jump | Toggle | true | — | Jump while idle to register activity. |
| Mode → [Custom] → Move | Toggle | true | — | Walk forward while idle to register activity. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/ModuleAntiAFK.kt)*
