## TpAura

TpAura automatically teleports your character to nearby enemies and attacks them, all without physically moving your visible position. When active, the module finds valid targets around you, packet-teleports to their location to land a hit, and then returns you to your original position — making it appear as though you never moved. A wireframe ghost of your actual network position is rendered in-world so you can track where the server thinks you are.

Two movement strategies are available. **AStar** mode uses pathfinding to navigate around obstacles on the way to the target, sending position packets block-by-block along the calculated route. It respects terrain and can optionally teleport you back to your starting point after the attack. **Immediate** mode skips pathfinding entirely and jumps straight to the nearest target in a single sequence of packets, best suited for open environments where nothing stands between you and the enemy.

Because TpAura relies on sending rapid position packets, servers with strong anti-cheat may issue a setback (a server-side correction). When this happens, a chat message will warn you and the teleport is cancelled automatically. Pairing this module with [AntiBot](/docs/modules/misc/antibot) is recommended to avoid wasting attacks on fake players.

**Category:** Combat
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| AttackRange | Decimal | 4.2 | 3.0–5.0 | Maximum distance from your teleported position at which an enemy can be attacked. |
| Clicker | Setting Group | — | — | See [Shared: Clicker](/docs/modules/shared-settings/clicker). |
| Mode | Mode Selector | AStar | AStar, Immediate | Selects the teleportation strategy used to reach targets. |
| Mode → [AStar] → MaximumDistance | Integer | 95 | 50–250 | Maximum block distance from you within which targets will be considered for pathfinding. |
| Mode → [AStar] → MaximumCost | Integer | 250 | 50–500 | Maximum pathfinding cost allowed; higher values permit longer or more complex routes. |
| Mode → [AStar] → TickDistance | Integer | 3 | 1–7 | Number of path blocks to bundle into a single position packet per step, controlling teleport granularity. |
| Mode → [AStar] → AllowDiagonal | Toggle | false | — | When enabled, the pathfinder may move diagonally between blocks. |
| Mode → [AStar] → TpBack | Toggle | true | — | When enabled, you are teleported back to your original position after the attack. |
| Mode → [AStar] → Stick | Integer | 5 | 1–10 (ticks) | How many ticks to remain at the target's location before returning. |
| Target | Setting Group | — | — | See [Shared: Target](/docs/modules/shared-settings/target). |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/tpaura/ModuleTpAura.kt)*
