## PacketMine

PacketMine lets you target a block with a single left-click and then automatically handles the entire mining sequence — sending the necessary network packets to start and finish the break — without you holding the mouse button down. This is useful for breaking specific blocks quickly and precisely, and pairs especially well with [AutoTool](/docs/modules/world/autotool), which will automatically equip the best tool for each block before the break completes.

Three mining modes cover different use-cases. **Normal** follows standard Minecraft mining behavior by sending a start packet and a stop packet once enough break progress has accumulated, making it the safest and most compatible choice for most servers. **Immediate** fires both the start and stop packets at the same time for an effectively instant break request, which is faster but may flag stricter anticheats. **Civ** is designed for CivMC-style servers and spams stop packets after the initial start, exploiting a chained-break mechanic to break blocks rapidly.

While a break is in progress, a yellow highlight shrinks around the target block to show how close it is to breaking. The module also exposes per-mode tool-switching behaviour, optional server-side rotation spoofing, and a configurable keep-range so you can wander a short distance without losing your target.

**Category:** World
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | Normal | — | Mining algorithm to use. **Normal** sends standard start/stop break packets. **Immediate** sends both packets simultaneously for an instant break attempt. **Civ** is tailored for CivMC-style servers and repeatedly issues stop packets after the initial start. |
| Mode → [Normal] → ClientSideSet | Toggle | false | — | When enabled, the block is removed on your client as soon as the stop packet is sent, without waiting for server confirmation. |
| Mode → [Normal] → WaitForConfirm | Toggle | true | — | Keep the current target until the server confirms the block actually broke before clearing it. Disable to clear the target immediately after sending the stop packet. |
| Mode → [Immediate] → WaitForConfirm | Toggle | true | — | Keep the current target until the server confirms the block broke before clearing it. |
| Mode → [Civ] → Switch | Toggle | false | — | Automatically switch to the correct tool when the target block requires a specific tool to drop items. |
| Range | Decimal | 4.5 | 1.0–6.0 | Maximum reach distance for selecting and mining a block. |
| WallsRange | Decimal | 4.5 | 0.0–6.0 | Maximum reach when the target block is not directly visible (e.g. mining through a wall). Set to 0 to disable wall-mining entirely. |
| KeepRange | Decimal | 25.0 | 0.0–200.0 | Maximum distance you can move from the target before the module drops it. Higher values let you wander further while still maintaining the break. |
| Swing | Choice | HideForClient | — | Controls where the hand-swing animation plays. **DoNotHide** shows it normally; **HideForClient** hides it only on your screen; **HideForServer** hides it from other players; **HideForBoth** hides it everywhere. |
| Switch | Mode Selector | OnStop | — | When to switch to the best tool for the target block. **Always** holds the tool for the full break duration; **PostStart** switches right after the start packet; **OnStop** switches only when the finish packet is about to be sent; **Never** performs no tool switching. |
| Switch → [Always] → AbortOnSwitch | Toggle | true | — | Cancels the current mining target if the held slot is changed away from the mining tool during a break, whether by the server or the client. |
| Switch → [Always] → CancelAutomaticSwitching | Toggle | true | — | Prevents other modules (other than [AutoTool](/docs/modules/world/autotool) and PacketMine itself) from silently changing your hotbar slot while a break is active, keeping the correct tool held. |
| Switch → [OnStop] → SwitchMethod | Choice | Normal | — | How to perform the slot switch when the finish packet is ready. **Normal** uses a silent hotbar switch; **Swap** physically swaps items in your inventory; **Pick** uses a legacy ViaFabricPlus packet (requires ViaFabricPlus; only works on pre-1.21.3 servers). |
| Rotate | Choice | Never | — | When to rotate your view toward the target block. **OnStart** rotates when beginning a break; **OnStop** rotates when sending the finish packet; **Both** rotates at both points; **Always** rotates continuously; **Never** does not rotate. |
| Rotations | Setting Group | — | — | See [Shared: Rotations](/docs/modules/shared-settings/rotations). |
| IgnoreOpenInventory | Toggle | true | — | When enabled, rotation requests are still applied even while an inventory or other screen is open. |
| BreakDamage | Decimal | 1.0 | 0.0–2.0 | How much break progress must accumulate (relative to a full break) before the stop packet is sent. At 1.0 the block is fully mined before finishing; lower values send the stop packet earlier. |
| PostBreakDelay | Integer | 6 | 0–10 ticks | Extra ticks to wait after finishing a break before targeting the next block. Helps avoid anticheat flags from instant chained breaks. |
| AbortAlwaysDown | Toggle | false | — | When aborting a mining action, always report the block face as downward instead of the actual face that was being mined. |
| SelectDelay | Integer | 200 | 0–400 ms | Minimum time between left-clicks before a new block can be selected or the current target deselected. |
| TargetRendering | Toggleable Group | on | — | See [Shared: Placement Rendering](/docs/modules/shared-settings/placement-rendering). |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/packetmine/ModulePacketMine.kt)*
