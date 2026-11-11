## FakeLag

FakeLag makes you look laggy to other players. It holds back what your client tells the server for a short time and then sends it all at once. Enemies see you where you were a moment ago, so they miss more of their hits.

FakeLag stops lagging for a moment when you take damage or knockback, while you are in water, while a menu is open and while you eat or drink. If [AutoDodge](/docs/modules/combat/autododge) is on too, FakeLag uses it to move out of the way of arrows.

**Category:** Combat
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Range | Decimal Range | 2.0..5.0 | 0.0..10.0 | How close an enemy has to be for Dynamic mode to start lagging, in blocks. |
| Delay | Integer Range | 300..600 | 0..1000 ms | How long to hold things back before sending them. A random value from the range is used each time. |
| RecoilTime | Integer | 250 | 0..1000 ms | How long to wait after sending everything before lagging again. |
| Mode | Choice | Dynamic | Constant, Dynamic | Constant lags all the time. Dynamic only lags when an enemy is in range and lagging keeps you further from them. |
| FlushOn | Multi-Select | EntityInteract, BlockInteract, Action | EntityInteract, BlockInteract, Action | Sends everything right away when you do one of these: hit or use an entity (EntityInteract), use a block (BlockInteract), or mine or drop things (Action). |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/ModuleFakeLag.kt)*
