## AutoLeave

AutoLeave leaves the server when your health gets too low, so you get out before you die. It does nothing in singleplayer, in creative mode, or while you hold a Totem of Undying. After it leaves, it turns itself off.

**Category:** Combat
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Health | Decimal | 8.0 | 0.0..20.0 HP | When your health is below this, AutoLeave gets ready to leave. 20 HP is full health. |
| Delay | Integer Range | 0..0 | 0..60 ticks | How long your health has to stay low before you leave, in ticks (20 per second). A random value from the range is used. If you heal in time, the wait starts over. |
| Mode | Choice | Quit | Quit, InvalidPacket, SelfHurt, IllegalChat, IllegalSwitchitem, IllegalInteract | How you leave. Quit disconnects normally. The other modes do something the server does not allow, so the server kicks you instead. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/ModuleAutoLeave.kt)*
