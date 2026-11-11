## FastUse

FastUse makes eating, drinking and other item use finish faster. It mostly works on old servers that let your client decide how long using an item takes. Newer anticheats often notice it.

Immediate finishes the item right away, ItemUseTime finishes it after a set number of ticks (20 per second), and Crossbow loads crossbows faster. Conditions lets you turn the speed-up off in some situations, like while you are in the air.

**Category:** Player
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | Immediate | Immediate, ItemUseTime, Crossbow | How item use is sped up. |
| Mode → Immediate → Delay | Integer | 0 | 0..10 ticks | How long to wait before finishing the item. |
| Mode → Immediate → Timer | Decimal | 1.0 | 0.1..5.0 | Game speed while finishing the item. Higher is faster. |
| Mode → Immediate → Speed | Integer | 20 | 1..35 packets | How many extra movement packets are sent to finish the item. |
| Mode → ItemUseTime → ConsumeTime | Integer | 15 | 0..20 | Ticks you use the item before it is finished. |
| Mode → ItemUseTime → Speed | Integer | 20 | 1..35 packets | How many extra movement packets are sent to finish the item. |
| Mode → Crossbow → TickCooldown | Integer | 1 | 1..20 | How often, in ticks, the crossbow trick is repeated. |
| Conditions | Multi-Select | NotInTheAir | NotInTheAir, NotDuringMove, NotDuringRegeneration | FastUse does nothing while one of these is true. |
| StopInput | Toggle | Off | | Stops you from walking while you hold the use key. |
| PacketType | Choice | Full | OnGroundOnly, PositionAndOnGround, LookAndOnGround, Full | Which kind of movement packet to send. Full is what a normal client sends. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/ModuleFastUse.kt)*
