## Freeze

Freeze stops you in place. The game around you stops moving for you until you turn it off, and the mode decides what the server sees in the meantime.

**Category:** Movement
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | Stationary | Queue, Cancel, Stationary, TickMovement | How Freeze holds you in place. |
| Mode → Queue → Origin | Multi-Select | Outgoing | Incoming, Outgoing | Which data is held back and sent all at once when Freeze turns off. This works like [Blink](/docs/modules/player/blink). |
| Mode → Cancel → Origin | Multi-Select | Outgoing | Incoming, Outgoing | Which data is thrown away while frozen. |
| Mode → Stationary → CancelC0B | Toggle | true |  | Holds back replies to the server's connection checks. Helps on stricter servers. |
| Mode → TickMovement → Interval | Integer Range | 20..20 | 1..200 | How many ticks (20 per second) you wait between each single step of movement. |
| DisableOn | Multi-Select | Flag | Flag, OnGround, OnMovementInput, InLiquid, Void, OnUseItem | Turns Freeze off when one of these happens: the server pulls you back (Flag), you touch the ground, you press a walk key, you are in water or lava, you fall below the world (Void), or you use an item. |
| Notification | Toggle | false |  | Shows a message that says why Freeze turned itself off. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/ModuleFreeze.kt)*
