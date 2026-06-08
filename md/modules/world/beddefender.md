## BedDefender

BedDefender keeps your bed alive in BedWars by automatically placing blocks over it the moment it becomes exposed. When the module is on, it constantly scans the area around you for your own bed, works out which surrounding faces are uncovered, and queues block placements to seal them back up — letting you focus on fighting or bridging while your defense maintains itself.

You decide how thick the wall should be with **MaxLayers** (1–5 layers of blocks around the bed), and which blocks it's allowed to use: by default it only consumes full solid blocks, picking the hardest, most blast-resistant ones first via [the block-slot comparator](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/ModuleBedDefender.kt#L57-L70), so obsidian or end stone is preferred over wool. Because a bed may already be partially covered, it searches a slightly larger area than its reach so it can still find and finish the job — see [the bed search and placement logic](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/ModuleBedDefender.kt#L97-L139).

Crucially, BedDefender only acts on *your* bed, decided by the **SelfBed** mode. Leave it on **None** and it won't defend anything; pick **Color** to identify your bed by the dyed blocks (e.g. armor of a matching color) around it, **SpawnLocation** to treat the nearest bed within a distance of your spawn as yours, or **Manual** to bind keys that mark and unmark a specific bed yourself. Placements are ordered innermost layer first, closest gaps prioritized, so the holes nearest the bed get plugged first.

**Category:** World
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| MaxLayers | Integer | 1 | 1..5 | How many layers of blocks to wrap around the bed. Higher values build a thicker, harder-to-break shell. |
| AllowChests | Toggle | false | — | When on, chests may also be used as defense blocks, not just full solid blocks. |
| SelfBed | Mode Selector | None | None, Color, SpawnLocation, Manual | How the module decides which bed counts as yours and should be defended. None disables defending. |
| SelfBed → [Color] → Slots | Multi-Select | [Head] | Feet, Legs, Chest, Head | Which armor/equipment slots are checked to match your team color when identifying your bed. |
| SelfBed → [Color] → Loose | Toggle | false | — | When on, color matching is more lenient when deciding whether a bed belongs to your team. |
| SelfBed → [SpawnLocation] → BedDistance | Decimal | 24.0 | 16.0..48.0 | Maximum distance from your spawn point within which a bed is considered your own. |
| SelfBed → [Manual] → Track | Key | — | — | Key that marks the bed you are looking at / nearest as the one to defend. |
| SelfBed → [Manual] → Untrack | Key | — | — | Key that removes a previously marked bed from defense tracking. |
| Place | Setting Group | — | — | See [Shared: Block Placer](/docs/modules/shared-settings/block-placer). |
| RequiresSneak | Toggle | false | — | When on, blocks are only placed while you are holding sneak, giving you manual control over when defending happens. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/ModuleBedDefender.kt)*
