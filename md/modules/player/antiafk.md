## AntiAFK

AntiAFK makes small moves for you, like turning, swinging your arm or jumping, so the server does not kick you or send you to the lobby for standing still. Turn it on when you need to step away from the keyboard for a bit.

Some modes walk your character around, so use it in a safe spot where you can't fall or get hurt.

**Mode** picks what it does:

- **RandomInteraction** picks a random action from the ones you selected, then waits a random time before the next one.
- **Old** walks forward and turns you around every half second.
- **Custom** lets you switch turning, swinging, jumping and walking on or off yourself.

**Category:** Player
**Enabled by default:** No

### Settings

Delays are in ticks (20 per second).

| Setting | Type | Default | Range | Description |
| --- | --- | --- | --- | --- |
| Mode | Mode Selector | RandomInteraction | Old, RandomInteraction, Custom | What AntiAFK does to keep you active. |
| Mode → [RandomInteraction] → Interaction | Multi-Select | Yaw, Pitch, SwingHand | Jump, SwingHand, ChangeSlot, Yaw, Pitch, RandomDirection | Actions it can pick from. Yaw turns you left or right, Pitch looks up or down a little, ChangeSlot picks a random hotbar slot, RandomDirection walks a random way for a moment. |
| Mode → [RandomInteraction] → Delay | Integer Range | 4..7 | 0..20 ticks | Wait between actions. |
| Mode → [Custom] → Rotate | Toggleable Group | On | | Turns your view now and then. |
| Mode → [Custom] → Rotate → IgnoreOpenInventory | Toggle | true | | Keeps turning while an inventory is open. |
| Mode → [Custom] → Rotate → Rotations | Setting Group | | | See [Shared: Rotations](/docs/modules/shared-settings/rotations). |
| Mode → [Custom] → Rotate → Delay | Integer | 5 | 0..20 ticks | Wait between turns. |
| Mode → [Custom] → Rotate → Angle | Decimal | 1.0 | -180.0..180.0 | How far you turn each time. |
| Mode → [Custom] → Swing | Toggleable Group | On | | Swings your arm now and then. |
| Mode → [Custom] → Swing → Delay | Integer | 5 | 0..20 ticks | Wait between swings. |
| Mode → [Custom] → Jump | Toggle | true | | Keeps jumping. |
| Mode → [Custom] → Move | Toggle | true | | Keeps walking forward. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/ModuleAntiAFK.kt)*
