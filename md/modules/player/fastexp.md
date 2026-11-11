## FastExp

FastExp throws bottles o' enchanting at your feet to repair your gear with Mending. It works while you hold its key and uses bottles from your hotbar or offhand.

It repairs your armor and the item in your other hand, but only items with Mending. With NoWaste on, it waits until something is worn down, throws about as many bottles as you need, and then stops.

**Category:** Player
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Rotate | Toggleable Group | On | | Looks straight down before throwing, so the experience lands on you. |
| Rotate → Rotations | Setting Group | | | See [Rotations](/docs/modules/shared-settings/rotations). |
| NoWaste | Toggleable Group | On | | Only throws the bottles needed to repair your gear. |
| NoWaste → MinDurabilityToStartRepair | Integer | 64 | 0..2048 | Starts repairing when an item has this much durability left or less. |
| NoWaste → MaxDurabilityToContinueRepair | Integer | 85 | 1..100 % | Finishes an unfinished repair only while an item is at or below this percent of its durability. |
| ThrowMode | Mode Selector | Normal | Normal, Fast | How fast bottles are thrown. |
| ThrowMode → Normal → TicksPerItem | Decimal Range | 2.0..3.0 | 0.5..10.0 ticks | Throws one bottle every this many ticks (20 per second), picked at random in the range. |
| ThrowMode → Fast → ItemsPerTick | Decimal Range | 3.0..5.0 | 0.5..16.0 | Throws this many bottles every tick, picked at random in the range. |
| CombatPauseTime | Integer | 0 | 0..40 ticks | Pauses combat modules for this long while throwing. |
| SlotResetDelay | Integer Range | 0..0 | 0..40 ticks | How long to wait before switching back from the bottle slot. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/ModuleFastExp.kt)*
