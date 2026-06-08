## Fucker

Fucker automatically destroys (or right-click *uses*) specific blocks near you. Its most common job is breaking enemy **beds** in Bedwars-style games, but it also targets things like dragon eggs out of the box — and you can point it at any block type you like. When enabled, it scans for valid targets within reach, turns toward the closest one, and starts breaking it without you having to aim or click.

It can reach targets you can see directly, and — depending on your settings — work toward targets that are walled off by clearing a path or punching an opening first. It plays nicely with related tools: when [PacketMine](/docs/modules/world/packetmine) is running it hands off the actual mining, it uses [AutoTool](/docs/modules/world/autotool)'s slots to judge mining speed, and it pauses while [Blink](/docs/modules/player/blink) is active.

To keep you from wrecking your own bed, the **SelfBed** option offers several ways to recognize and skip it. You can also let Fucker's aiming take priority over [KillAura](/docs/modules/combat/killaura) so it stays focused on breaking instead of fighting.

**Category:** World
**Enabled by default:** Yes

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Range | Decimal | 4.0 | 1.0–6.0 | How far (in blocks) Fucker will reach to find and break a target you can see. |
| WallRange | Decimal | 0.0 | 0.0–6.0 | Maximum distance for targets you have no direct line of sight to. Left at 0, the module won't break blocks it can't see. Capped to Range. |
| Entrance | Toggleable Group | On | — | Treats a target as reachable if it has any open (air) side, even one you can't see, and breaks it as if it were in plain view. Handy on servers like Hypixel and CubeCraft. |
| Entrance → BreakFree | Toggle | true | — | If the target has no opening, breaks the weakest neighboring block first to create one. |
| Surroundings | Toggle | false | — | Allows breaking blocks that stand in the way in order to clear a path to a hidden target. |
| Targets | Registry List | — | — | The blocks Fucker will break or use. Defaults to all beds and dragon eggs. |
| Delay | Integer | 1 | 0–20 (ticks) | Ticks to wait when switching between targets or after a use action. Higher values slow it down. |
| Action | Choice | Destroy | Destroy, Use | Whether to break the target (Destroy) or right-click interact with it (Use). |
| ForceImmediateBreak | Toggle | false | — | Tries to break the block in a single tick where possible, instead of the normal gradual mining process. |
| IgnoreOpenInventory | Toggle | false | — | Keeps working even while a chest or other inventory screen is open. |
| IgnoreUsingItem | Toggle | true | — | Keeps working while you're using an item (eating, drinking, drawing a bow, etc.). |
| PrioritizeOverKillAura | Toggle | true | — | Gives Fucker's aiming priority over [KillAura](/docs/modules/combat/killaura), so it focuses on breaking rather than attacking. |
| ChestAsFullBlock | Toggle | false | — | Treats chests as a full cube when working out reach and pathing, useful when a chest sits right against the target. |
| SelfBed | Mode Selector | SpawnLocation | None, Color, SpawnLocation, Manual | How your own bed is recognized so it gets left alone. None disables protection, Color matches by armor color, SpawnLocation uses your spawn point, Manual lets you mark beds yourself. |
| SelfBed → [Color] → Slots | Multi-Select | Head | Feet, Legs, Chest, Head | Which armor slots to read the team color from when identifying your bed. |
| SelfBed → [Color] → Loose | Toggle | false | — | Uses looser color matching when deciding which bed is yours. |
| SelfBed → [SpawnLocation] → BedDistance | Decimal | 24.0 | 16.0–48.0 | Maximum distance from your spawn point for a bed to count as yours. |
| SelfBed → [Manual] → Track | Key | — | — | Key to manually mark a bed as your own. |
| SelfBed → [Manual] → Untrack | Key | — | — | Key to remove a manual mark from a bed. |
| Rotations | Setting Group | — | — | See [Shared: Rotations](/docs/modules/shared-settings/rotations). |
| TargetRendering | Toggleable Group | On | — | See [Shared: Placement Rendering](/docs/modules/shared-settings/placement-rendering). |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/fucker/ModuleFucker.kt)*
