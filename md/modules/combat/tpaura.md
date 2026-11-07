## TpAura

TpAura automatically teleports your character to nearby enemies and attacks them, all without physically moving your visible position. When active, the module finds valid targets around you, packet-teleports to their location to land a hit, and then returns you to your original position — making it appear as though you never moved.

The route to the target comes from LiquidBounce's shared pathfinder, so TpAura reaches enemies around obstacles, below overhangs and up on raised platforms, and comes back the same way.

Because TpAura relies on sending rapid position packets, servers with strong anti-cheat may issue a setback (a server-side correction). When this happens, a chat message will warn you and the teleport is cancelled automatically. Pairing this module with [AntiBot](/docs/modules/misc/antibot) is recommended to avoid wasting attacks on fake players.

**Category:** Combat
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| AttackRange | Decimal | 4.2 | 3.0–5.0 | Maximum distance from your teleported position at which an enemy can be attacked. |
| Clicker | Setting Group | — | — | See [Shared: Clicker](/docs/modules/shared-settings/clicker). |
| Target | Setting Group | — | — | See [Shared: Target](/docs/modules/shared-settings/target). |

---
*Last updated: 2026-11-07 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/nextgen/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/tpaura/ModuleTpAura.kt)*
