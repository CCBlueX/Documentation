## Surround

Surround automatically places explosion-resistant blocks — obsidian by default — around your feet to form a protective shell whenever you enable it. This is a staple of Crystal PvP: the surrounding blocks absorb blast damage from end crystals, making you significantly harder to burst down. When the **Center** feature is selected, the module also snaps you to the centre of your block on activation so the hole aligns perfectly.

The module is designed to stay active only while you are stationary inside your hole. You can configure it to disable itself the moment your Y-level changes (e.g. you get knocked out of the hole), when you drift more than half a block away horizontally, or when your speed exceeds a threshold. The **Extend** feature handles the edge case where an entity is standing in a placement spot — Surround will widen the formation outward to work around it, while **NoWaste** prevents it from building an unnecessarily large formation if you are already safely inside a 1×1 hole.

The **Protect** group adds a reactive layer of defence: it watches for opponents mining your surround blocks and, once the block reaches a configurable break stage, places an extra outward ring on the threatened side so your attacker has to break even more blocks. Combine this with the **AddExtraLayer** key bind to force that extra ring on demand at any time. For block-placement timing and rotation behaviour, refer to the [Shared: Block Placer](/docs/modules/shared-settings/block-placer) settings exposed under **Placing**.

**Category:** World
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Features | Multi-Select | Extend, Down | — | Optional behaviours: **Center** snaps you to the centre of your block on enable; **Extend** widens the surround when an entity blocks a placement spot; **NoWaste** skips building a larger formation if you are already in a completed 1×1 hole; **Down** places an extra block layer below the surround to stop enemies from mining the floor out from under you. |
| DisableOn | Multi-Select | YChange | — | Conditions that auto-disable the module: **YChange** fires when your Y-coordinate changes; **XZMove** fires when you drift more than 0.5 blocks from your starting position; **XZSpeed** fires when your horizontal speed reaches 5 m/s or higher. |
| Instant | Toggle | true | — | Replaces broken surround blocks the moment the block-update packet is received, without waiting for the next game tick. Requires the rotation mode in **Placing** to be set to *None*. |
| AddExtraLayer | Key Bind | — | — | While this key is held, forces the extra protection layer to be built continuously, independent of whether **Protect → ExtraLayer** is triggered by block-break events. |
| Protect | Toggleable Group | on | — | Monitors surround blocks being mined by opponents and reacts to protect them before they are fully broken. |
| Protect → MinDestroyProgress | Integer | 4 | 0–9 stage | The mining stage (0 = just started, 9 = almost broken) at which the module begins taking protective action on a block being broken by an enemy. |
| Protect → ExtraLayer | Toggleable Group | on | — | When a surround block is being mined beyond the threshold, automatically extends the surround one block further outward on the threatened side (and one block upward), forcing the attacker to break additional blocks. |
| Protect → ExtraLayer → Corners | Toggle | false | — | Also fills the diagonal corner positions around the threatened side, turning the cross-shaped extension into a full ring. |
| Filter | Choice | Whitelist | — | Controls how the **Blocks** list is interpreted: *Whitelist* restricts placement to only the listed blocks; *Blacklist* excludes the listed blocks and allows everything else. |
| Blocks | Registry List | — | — | The block types Surround may place (or is forbidden from placing, depending on **Filter**). Defaults to obsidian, ender chest, and crying obsidian. |
| Placing | Setting Group | — | — | See [Shared: Block Placer](/docs/modules/shared-settings/block-placer). |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/ModuleSurround.kt)*
