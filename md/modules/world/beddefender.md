## BedDefender

BedDefender places blocks around a bed in BedWars to cover it up. It fills the open spots next to the bed so enemies have a harder time breaking it.

It uses the strongest full blocks in your hotbar first, so obsidian or end stone goes on before wool. Use SelfBed to tell it which bed is yours. With SelfBed on None, it covers every bed near you.

**Category:** World
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| MaxLayers | Integer | 1 | 1..5 | How many layers of blocks to put around the bed. |
| AllowChests | Toggle | false | | Also lets it use chests as cover blocks. |
| SelfBed | Mode Selector | None | None, Color, SpawnLocation, Manual | How it finds your own bed. None covers every bed. |
| SelfBed → [Color] → Slots | Multi-Select | Head | Feet, Legs, Chest, Head | Which armor pieces are checked. A bed with the same color as your armor is yours. |
| SelfBed → [Color] → Loose | Toggle | false | | Also counts beds with a color close to your armor color. |
| SelfBed → [SpawnLocation] → BedDistance | Decimal | 24.0 | 16.0..48.0 blocks | A bed this close to where you spawned is yours. |
| SelfBed → [Manual] → Track | Key | Numpad + | | Marks a bed as yours. |
| SelfBed → [Manual] → Untrack | Key | Numpad - | | Removes the mark again. |
| Place | Setting Group | | | See [Block Placer](/docs/modules/shared-settings/block-placer). |
| RequiresSneak | Toggle | false | | Only places blocks while you sneak. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/ModuleBedDefender.kt)*
