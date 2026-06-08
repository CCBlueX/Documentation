## Nuker

Nuker automatically breaks blocks in your surrounding area without any manual clicking. When enabled, it continuously scans for valid blocks within range and destroys them one after another — useful for clearing terrain, farming resources, or demolishing structures rapidly. It pairs well with [AutoTool](/docs/modules/world/autotool) to always use the most efficient tool for whatever it is breaking.

There are two breaking modes to choose from. **Legit** mode mimics how a real player mines: it faces the target block, respects normal break timing and reach limits, and can optionally reach through walls via `WallRange`. This is the safer option on servers with anti-cheat. **Instant** mode bypasses break animations entirely and can destroy many blocks per second using raw packets — far faster, but much more detectable. Note that [Blink](/docs/modules/player/blink) will pause Nuker in either mode while it is active.

You can control *which* blocks get broken using the **Filter** and **Blocks** settings. Switch Filter to **Whitelist** and add specific blocks to only break those; leave it on **Blacklist** to break everything *except* the listed blocks. The **AreaMode** setting lets you switch between a **Sphere** (breaks blocks in all directions around you) and a **Floor** region (breaks a flat rectangular area you define by coordinates, useful for clearing a specific plot layer by layer).

**Category:** World
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | Legit | — | Selects the breaking method: **Legit** uses realistic rotation-based mining; **Instant** uses packets to destroy blocks without going through normal break animations. |
| Mode → \[Legit\] → Range | Decimal | 4.0 | 1.0–6.0 | Maximum reach distance when targeting blocks in Legit mode. |
| Mode → \[Legit\] → WallRange | Decimal | 0.0 | 0.0–6.0 | Reach distance for blocks behind walls. Set to `0` to disable through-wall targeting. Cannot exceed Range. |
| Mode → \[Legit\] → ForceImmediateBreak | Toggle | false | — | When enabled, attempts to break the target block immediately on the first tick rather than waiting through the normal mining progress. |
| Mode → \[Legit\] → Rotations | Setting Group | — | — | See [Shared: Rotations](/docs/modules/shared-settings/rotations). |
| Mode → \[Legit\] → SwitchDelay | Integer | 0 | 0–20 | How many ticks to wait before switching focus to a new target block after the previous one is broken. |
| Mode → \[Instant\] → Range | Decimal | 5.0 | 1.0–50.0 | Maximum reach distance when targeting blocks in Instant mode. |
| Mode → \[Instant\] → BPS | Integer Range | 40..50 | 1–200 | Number of blocks broken per second. A random value is chosen from this range each tick for more natural variance. |
| Mode → \[Instant\] → DoNotStop | Toggle | false | — | When enabled, skips sending the stop-breaking packet. May increase throughput on some servers but can cause visual desync. |
| AreaMode | Mode Selector | Sphere | — | Shape of the mining area: **Sphere** scans all blocks around you within the configured radius; **Floor** targets a defined rectangular region. |
| AreaMode → \[Floor\] → RelativeToPlayer | Toggle | true | — | When enabled, `StartPosition` and `EndPosition` are treated as offsets from your current position so the area moves with you. |
| AreaMode → \[Floor\] → StartPosition | Vector3_i | — | — | One corner of the rectangular floor area (X, Y, Z). |
| AreaMode → \[Floor\] → EndPosition | Vector3_i | — | — | Opposite corner of the rectangular floor area (X, Y, Z). |
| AreaMode → \[Floor\] → TopToBottom | Toggle | true | — | When enabled, Nuker clears the highest layer of the defined region first, then works downward. |
| Filter | Choice | Whitelist | — | How the Blocks list is applied: **Whitelist** only breaks blocks on the list; **Blacklist** breaks everything *except* blocks on the list. |
| Blocks | Registry List | — | — | The set of blocks used by the Filter. Add blocks here to whitelist or blacklist them. |
| Swing | Choice | DoNotHide | — | Controls the hand-swing animation visibility: **DoNotHide** shows it normally; **HideForBoth** hides it for you and other players; **HideForClient** hides it only on your screen; **HideForServer** hides it only from the server. |
| IgnoreOpenInventory | Toggle | false | — | When enabled, Nuker keeps breaking blocks even while a container or inventory screen is open. |
| TargetRendering | Toggleable Group | on | — | See [Shared: Placement Rendering](/docs/modules/shared-settings/placement-rendering). |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/nuker/ModuleNuker.kt)*
