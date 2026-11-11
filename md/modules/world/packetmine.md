## PacketMine

PacketMine breaks a block after you click it once. You do not have to hold the mouse button, and you can look away while it mines. It works well together with [AutoTool](/docs/modules/world/autotool).

A yellow box on the block shows how far the breaking is.

**Category:** World
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Choice | Normal | Normal, Immediate, Civ | How it mines. Normal mines like the game does. Immediate tries to break the block right away. Civ is made for CivMC servers. |
| Mode → [Normal] → ClientSideSet | Toggle | false | | Removes the block on your screen right when it finishes, without waiting for the server. |
| Mode → [Normal] → WaitForConfirm | Toggle | true | | Keeps the block selected until the server says it broke. |
| Mode → [Immediate] → WaitForConfirm | Toggle | true | | Keeps the block selected until the server says it broke. |
| Mode → [Civ] → Switch | Toggle | false | | Switches to the right tool when the block needs one to drop. |
| Range | Decimal | 4.5 | 1.0..6.0 blocks | How far away you can mine. |
| WallsRange | Decimal | 4.5 | 0.0..6.0 blocks | How far you can mine blocks you can't see. 0 turns this off. |
| KeepRange | Decimal | 25.0 | 0.0..200.0 blocks | How far you can walk away before the block is let go. |
| Swing | Choice | HideForClient | DoNotHide, HideForBoth, HideForClient, HideForServer | Who sees your hand swing. |
| Switch | Choice | OnStop | Always, PostStart, OnStop, Never | When to switch to the best tool. Always holds it the whole time, PostStart right after starting, OnStop just before the block breaks. |
| Switch → [Always] → AbortOnSwitch | Toggle | true | | Stops mining if your held item changes. |
| Switch → [Always] → CancelAutomaticSwitching | Toggle | true | | Stops other modules from changing your item while mining. |
| Switch → [OnStop] → SwitchMethod | Choice | Normal | Normal, Swap, Pick | How to switch. Pick needs ViaFabricPlus and only works on servers older than 1.21.3. |
| Rotate | Choice | Never | OnStart, OnStop, Both, Always, Never | When to turn toward the block. |
| Rotations | Setting Group | | | See [Rotations](/docs/modules/shared-settings/rotations). |
| IgnoreOpenInventory | Toggle | true | | Still turns toward the block while a screen is open. |
| BreakDamage | Decimal | 1.0 | 0.0..2.0 | How much of the block has to be mined before finishing. 1.0 is a full break. |
| PostBreakDelay | Integer | 6 | 0..10 ticks | Wait after a break before the next block (20 ticks per second). |
| AbortAlwaysDown | Toggle | false | | When it stops mining, it always tells the server the bottom side. |
| SelectDelay | Integer | 200 | 0..400 ms | Time between clicks before you can pick or drop a block. |
| TargetRendering | Toggleable Group | On | | See [Placement Rendering](/docs/modules/shared-settings/placement-rendering). |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/packetmine/ModulePacketMine.kt)*
