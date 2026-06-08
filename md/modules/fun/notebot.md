## Notebot

Notebot automatically plays Note Block songs loaded from NBS (Note Block Song) files — the format used by tools like [Note Block Studio](https://opennbs.org/). When enabled, it scans the note blocks within reach, tests each one to discover its current pitch, tunes them to the correct pitches required by the song, and then plays the song by triggering the blocks in sequence. Progress for each stage (testing, tuning, and playing) is reported in chat. The module disables itself once the song finishes or if requirements cannot be met (e.g. not enough note blocks nearby, you are in Creative mode, or [PacketMine](/docs/modules/world/packetmine) is active).

You must be in Survival mode and have enough correctly-typed note blocks within range before enabling the module. The block type underneath each note block determines its instrument, so make sure you have the right blocks placed. With **ReuseBlocks** enabled, only one block per note value is needed (the same block can be struck multiple times per tick), which greatly reduces the number of blocks required at the cost of potentially missing simultaneous identical notes.

Notebot highlights the note blocks it is working with in-world. The highlight color transitions through red (testing), yellow (tuning), and the configured play color as the module progresses through its stages.

**Category:** Fun
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Song | File | — | — | The NBS file to load and play. |
| PianoOnly | Toggle | false | — | When enabled, all instruments are mapped to harp (piano), so only harp-type note blocks are needed regardless of what instruments the song uses. |
| ReuseBlocks | Toggle | false | — | When enabled, a single note block can be reused for the same pitch within a tick, reducing the total number of blocks required. Changing this setting disables the module. |
| Range | Decimal | 6.0 | 1.0–6.0 | Maximum distance (in blocks) from your eyes at which note blocks are detected and interacted with. |
| IgnoreOpenInventory | Toggle | true | — | When enabled, the module continues operating even while an inventory screen is open. |
| StartDelay → Test | Integer | 0 | 0–20 ticks | Delay in ticks before the testing stage begins. |
| StartDelay → Tune | Integer | 0 | 0–20 ticks | Delay in ticks before the tuning stage begins. |
| StartDelay → Play | Integer | 2 | 0–20 ticks | Delay in ticks before playback begins. |
| Render | Toggleable Group | on | — | See [Shared: Placement Rendering](/docs/modules/shared-settings/placement-rendering). |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/fun/notebot/ModuleNotebot.kt)*
