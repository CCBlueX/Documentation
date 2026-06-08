## FastExp

FastExp automatically repairs your Mending-enchanted gear by tossing experience bottles while you hold the keybind. As long as you have bottles o' enchanting in your hotbar or offhand, it looks down and throws them for you so the released experience orbs flow straight into your damaged armor (and the item in your other hand), saving you from spamming the use key.

By default the module only works when it's worth it: it waits until something is actually worn down before it starts, and it stops once your gear is patched up so you don't burn bottles after every couple of hits. You can also have it briefly hold off during combat and tweak how fast bottles are thrown, making it suitable for both quiet downtime repairs and quick top-ups mid-fight.

Note that FastExp turns itself off when you leave a server, and it only repairs items carrying the Mending enchantment.

**Category:** Player
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Rotate | Toggleable Group | On | — | Looks straight down before throwing so the experience orbs land near you for absorption. |
| Rotate → Rotations | Setting Group | — | — | See [Shared: Rotations](/docs/modules/shared-settings/rotations). |
| NoWaste | Toggleable Group | On | — | Only throws as many bottles as needed to repair your gear, instead of throwing endlessly. |
| NoWaste → MinDurabilityToStartRepair | Integer | 64 | 0..2048 | Starts repairing once at least one item drops to this many durability points or lower. |
| NoWaste → MaxDurabilityToContinueRepair | Integer | 85 | 1..100% | Will resume an interrupted repair only while an item is still at or below this percentage of durability, preventing constant tiny top-ups. |
| ThrowMode | Mode Selector | Normal | Normal, Fast | How quickly experience bottles are thrown. |
| ThrowMode → Normal → TicksPerItem | Decimal Range | 2.0..3.0 | 0.5..10.0 ticks | A bottle is thrown roughly once every this many ticks, picked at random within the range for a more natural pace. |
| ThrowMode → Fast → ItemsPerTick | Decimal Range | 3.0..5.0 | 0.5..16.0 | Throws this many bottles every tick for much faster repairs, picked at random within the range. |
| CombatPauseTime | Integer | 0 | 0..40 ticks | Pauses combat-related actions for this many ticks whenever bottles are thrown. |
| SlotResetDelay | Integer Range | 0..0 | 0..40 ticks | Delay before switching back from the bottle slot after use, randomized within the range. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/ModuleFastExp.kt)*
