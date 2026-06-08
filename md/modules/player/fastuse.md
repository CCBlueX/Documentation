## FastUse

FastUse speeds up how quickly you can use right-click items — eating food, drinking potions, firing a bow or crossbow, and similar consumables. Normally these actions take a fixed amount of time, but on many servers the server trusts your client to report how long you've been using an item. FastUse takes advantage of this by telling the server you've finished sooner, so the item activates almost instantly.

This is mainly useful on legacy or loosely-protected servers; modern anticheats may flag or block the speed-up. The **Mode** you pick decides the technique: **Immediate** releases the item right away (with an optional game-speed boost), **ItemUseTime** waits until you've used it for a set number of ticks before finishing, and **Crossbow** is a dedicated option for loading crossbows quickly. Use the **Conditions** to hold off in situations where the acceleration would look suspicious or get in your way.

If you mainly want smarter automatic food handling rather than raw speed, consider pairing this with [SmartEat](/docs/modules/player/smarteat).

**Category:** Player
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
| --- | --- | --- | --- | --- |
| Mode | Mode Selector | ItemUseTime | Immediate, ItemUseTime, Crossbow | Chooses which technique is used to speed up item usage. |
| Mode → Immediate → Delay | Integer | 10 | 0–10 ticks | How long to wait before releasing the item, in ticks. |
| Mode → Immediate → Timer | Decimal | 1.0 | 0.1–5.0 | Temporarily adjusts game speed while finishing the item; higher is faster. |
| Mode → Immediate → Speed | Integer | 10 | 1–35 packets | How many movement packets are sent at once to simulate faster use. |
| Mode → ItemUseTime → ConsumeTime | Integer | 17 | 0–20 | Number of ticks you must use the item before it is released. |
| Mode → ItemUseTime → Speed | Integer | 5 | 1–35 packets | How many movement packets are sent at once to simulate faster use. |
| Mode → Crossbow → TickCooldown | Integer | 1 | 1–20 | How often (in ticks) the crossbow reload action is repeated. |
| Conditions | Multi-Select | NotInTheAir | NotInTheAir, NotDuringMove, NotDuringRegeneration | Situations in which FastUse will pause and not accelerate item usage. |
| StopInput | Toggle | false | — | Cancels your movement input while you hold the use key. |
| PacketType | Choice | Full | OnGroundOnly, PositionAndOnGround, LookAndOnGround, Full | Which kind of movement packet to send; Full most closely matches a vanilla client. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/ModuleFastUse.kt)*
