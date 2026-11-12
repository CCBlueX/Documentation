## AntiVoid

AntiVoid saves you when you are about to fall into the void. It looks a short moment ahead, and if there is nothing under you all the way down, it catches you and shows a notification. Turn it on for maps with void edges, like Bedwars or Skywars, where a knockback hit can throw you off.

It does nothing while [Fly](/docs/modules/movement/fly) is on or while [Clutch](/docs/modules/world/clutch) is catching a fall. Blink mode also waits while [Scaffold](/docs/modules/world/scaffold) is on.

**Mode** picks how it saves you:

- **GhostBlock** puts a fake block under you that only you can stand on.
- **Flag** pushes you up a little.
- **Blink** holds back your movement (like [Blink](/docs/modules/player/blink)) and then sends you back to where you were safe.
- **UseItem** uses an item from your hotbar or offhand, for servers where an item saves you from the void.

**Category:** Player
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
| --- | --- | --- | --- | --- |
| Mode | Mode Selector | GhostBlock | GhostBlock, Flag, Blink, UseItem | How AntiVoid saves you. |
| Mode → [Flag] → FallDistance | Decimal | 0.5 | 0.0..6.0 | How far you must have fallen before it pushes you up. |
| Mode → [Flag] → Height | Decimal | 0.42 | 0.01..10.0 | How far up it pushes you. |
| Mode → [Flag] → Silent | Toggle | false | | Only tells the server you moved up, without moving you on your screen. |
| Mode → [UseItem] → YMotionThreshold | Decimal | -0.5 | -1.0..-0.1 | How fast you must be falling before it uses the item. Lower means faster. |
| Mode → [UseItem] → SlotResetDelay | Integer Range | 4..6 | 0..40 ticks | How long to hold the item before switching back, in ticks (20 per second). |
| Mode → [UseItem] → Items | Registry List | Magma Cream | | Items it may use. |
| VoidLevel | Integer | 0 | -256..0 | The height where the void starts. If there is no block between you and this height, you count as falling into the void. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/antivoid/ModuleAntiVoid.kt)*
