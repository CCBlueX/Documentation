## AntiBot

Some servers spawn fake players ("bots") to catch cheaters. AntiBot spots these bots so that combat modules like [KillAura](/docs/modules/combat/killaura) and [Aimbot](/docs/modules/combat/aimbot) leave them alone.

Pick the mode that fits your server. The Matrix, Intave and Horizon modes are made for those anti-cheats and need no setup. Custom lets you choose the checks yourself. Strict Custom checks can sometimes mark a real player as a bot.

**Category:** Misc
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | Custom | Custom, Matrix-2021-10-18, Intave-2022-07-28, Horizon-2021-10-18 | Which way of finding bots to use. |
| Mode → [Custom] → InvalidGround | Toggleable Group | On | | Marks players who say they stand on the ground while they float. |
| Mode → [Custom] → InvalidGround → VLToConsiderAsBot | Integer | 10 | 1..50 flags | How many times a player has to do this before they count as a bot. |
| Mode → [Custom] → Conditions | Multi-Select | NoGameMode, IllegalPitch, FakeEntityID | Duplicate, NoGameMode, IllegalPitch, FakeEntityID, NeedHit, IllegalHealth, Swung, Critted, Attributes, IllegalScale | Extra checks. A player who fails any selected check counts as a bot. |
| Mode → [Custom] → AlwaysInRadius | Toggleable Group | Off | | Marks players who never leave the area around you. |
| Mode → [Custom] → AlwaysInRadius → AlwaysInRadiusRange | Decimal | 20.0 | 5.0..30.0 | Size of that area in blocks. |
| Mode → [Custom] → Age | Toggleable Group | Off | | Marks players who only just appeared. |
| Mode → [Custom] → Age → Minimum | Integer | 20 | 0..120 ticks | How long a player has to be around before they are trusted, in ticks (20 per second). |
| Mode → [Custom] → Armor | Toggleable Group | Off | | Marks players whose armor is not in the lists below. |
| Mode → [Custom] → Armor → Helmet | Multi-Select | Nothing | Nothing, Leather, Chain, Iron, Gold, Diamond, Netherite, TurtleScute, Pumpkin, Skull | Helmets a real player may wear. |
| Mode → [Custom] → Armor → Chestplate | Multi-Select | Nothing | Nothing, Leather, Chain, Iron, Gold, Diamond, Netherite, Elytra | Chestplates a real player may wear. |
| Mode → [Custom] → Armor → Leggings | Multi-Select | Nothing | Nothing, Leather, Chain, Iron, Gold, Diamond, Netherite | Leggings a real player may wear. |
| Mode → [Custom] → Armor → Boots | Multi-Select | Nothing | Nothing, Leather, Chain, Iron, Gold, Diamond, Netherite | Boots a real player may wear. |
| Mode → [Custom] → Name | Toggleable Group | On | | Marks players whose name could not belong to a real account. |
| Mode → [Custom] → Name → Length | Integer Range | 3..16 | 1..32 | How long a real name can be. |
| Mode → [Custom] → Name → ValidateChars | Multi-Select | Vanilla | Vanilla, Cyrillic, CJKUnifiedIdeographs | Letters a real name may use. |
| LiteralNPC | Toggle | false | | Treats players who are missing from the server's player list as bots. Works in every mode. |
| NotInTabList | Toggle | false | | Treats players who are missing from the tab list as bots. Works in every mode. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/antibot/ModuleAntiBot.kt)*
