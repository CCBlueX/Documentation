## AntiBot

AntiBot keeps you from wasting hits on fake players. Many anti-cheats spawn invisible or decoy "bots" to bait you into attacking something no legitimate player would, then flag you for it. When AntiBot recognizes one of these entities, it tells the rest of the client to ignore it — so combat modules like [KillAura](/docs/modules/combat/killaura) and [Aimbot](/docs/modules/combat/aimbot) won't target it, and it won't appear as a valid target.

Pick a **Mode** that matches where you're playing. *Matrix*, *IntaveHeavy*, and *Horizon* are tuned to the quirks of those specific anti-cheats and need no setup. *Custom* lets you build your own detection by combining checks — useful when you know exactly how a server's bots behave (odd names, never-moving entities, impossible armor, and so on).

The two toggles at the bottom work in every mode: they flag any player that the server never properly added to the online player list or tab list, a common giveaway for client-side fakes. Leave AntiBot on for general play, but be aware that aggressive Custom checks can occasionally mistake a real player for a bot.

**Category:** Misc
**Enabled by default:** Yes

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | Custom | Custom, Matrix, IntaveHeavy, Horizon | Which detection profile to use. Custom is fully configurable; the others are presets tuned for those anti-cheats. |
| Mode → [Custom] → Conditions | Multi-Select | NoGameMode, IllegalPitch, FakeEntityID | Duplicate, NoGameMode, IllegalPitch, FakeEntityID, NeedHit, IllegalHealth, Swung, Critted, Attributes, IllegalScale | Individual giveaway checks; a player matching any selected one is treated as a bot. |
| Mode → [Custom] → InvalidGround | Toggleable Group | Off | — | Flags players whose movement claims they're standing on the ground while clearly floating. |
| Mode → [Custom] → InvalidGround → VLToConsiderAsBot | Integer | 10 | 1..50 (flags) | How many violations a player must rack up before being marked as a bot. |
| Mode → [Custom] → AlwaysInRadius | Toggleable Group | Off | — | Flags players who never leave a set distance around you, as bots often stay glued to you. |
| Mode → [Custom] → AlwaysInRadius → AlwaysInRadiusRange | Decimal | 20.0 | 5.0..30.0 | The radius, in blocks, a player must stay within to be considered suspicious. |
| Mode → [Custom] → Age | Toggleable Group | Off | — | Flags players that have only just appeared, since freshly spawned bots haven't existed long. |
| Mode → [Custom] → Age → Minimum | Integer | 20 | 0..120 (ticks) | Minimum number of ticks a player must have existed before they're trusted. |
| Mode → [Custom] → Armor | Toggleable Group | Off | — | Flags players wearing armor that doesn't match the legitimate sets you allow below. |
| Mode → [Custom] → Armor → Helmet | Multi-Select | None | Nothing, Leather, Chain, Iron, Gold, Diamond, Netherite, TurtleScute, Pumpkin, Skull | Allowed helmet items; leave empty to skip checking this slot. |
| Mode → [Custom] → Armor → Chestplate | Multi-Select | None | Nothing, Leather, Chain, Iron, Gold, Diamond, Netherite, Elytra | Allowed chestplate items; leave empty to skip checking this slot. |
| Mode → [Custom] → Armor → Leggings | Multi-Select | None | Nothing, Leather, Chain, Iron, Gold, Diamond, Netherite | Allowed leggings items; leave empty to skip checking this slot. |
| Mode → [Custom] → Armor → Boots | Multi-Select | None | Nothing, Leather, Chain, Iron, Gold, Diamond, Netherite | Allowed boots items; leave empty to skip checking this slot. |
| Mode → [Custom] → Name | Toggleable Group | On | — | Flags players whose name length or characters look invalid for a real account. |
| Mode → [Custom] → Name → Length | Integer Range | 3..16 | 1..32 | Allowed range for a player's name length; names outside it count as bots. |
| Mode → [Custom] → Name → ValidateChars | Multi-Select | None | Vanilla, Cyrillic, CJKUnifiedIdeographs | Which character sets a name may contain; a name using anything outside the selected sets is flagged. |
| LiteralNPC | Toggle | true | — | Treats any player missing from the online player list as a bot. |
| NotInTabList | Toggle | false | — | Treats any player missing from the tab list as a bot. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/antibot/ModuleAntiBot.kt)*
