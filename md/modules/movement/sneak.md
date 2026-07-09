## Sneak

Sneak automatically holds the sneak key for you at all times, keeping your character in a crouched state without any manual input. This is useful for preventing accidental falls off edges, staying silent while exploring, or maintaining a sneaking appearance in general gameplay.

Three modes control how the sneak state is communicated to the server. **Legit** overrides the movement input directly, making it behave as close to a real keypress as possible — it also has an optional sub-setting to only activate sneaking when you are standing on magma blocks, protecting you from their damage without crouching everywhere else. **Vanilla** forces the sneak flag inside the outgoing movement packet each tick; on servers running a version earlier than 1.21.6 when connected via ViaFabricPlus, it instead sends the legacy start and stop sneak packets, so it now works on those versions as well. **Switch** uses a legacy packet-based start/stop sneak approach and is only compatible with servers running a version earlier than 1.21.6 when connected via ViaFabricPlus.

The **NotDuringMove** toggle lets you disable automatic sneaking while you are actively walking or running, so the module only crouches when you are standing still — handy if you want edge protection without the movement speed penalty of permanent sneaking.

**Category:** Movement
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | Vanilla | Legit, Vanilla, Switch | Selects how the sneak state is applied. |
| Mode → [Legit] → OnMagmaBlocksOnly | Toggle | false | — | When enabled in Legit mode, sneaking is only applied while you are standing on a magma block, protecting you from its damage. |
| NotDuringMove | Toggle | false | — | When enabled, automatic sneaking is suppressed while you are moving. |

---
*Last updated: 2026-07-09 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/ModuleSneak.kt)*
