## XRay

XRay hides every block except the ones on its list, so you can see ores, chests and other useful blocks through the ground. The list starts with ores, containers, liquids, portals and a few more blocks. Change it with `.xray add <block>` and `.xray remove <block>`.

If you only want to outline some blocks and keep the world normal, use [BlockESP](/docs/modules/render/blockesp).

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| FullBright | Toggle | true | | Lights up the shown blocks fully, so they are easy to see in the dark. |
| ExposedOnly | Toggle | false | | Only shows blocks that touch air or another non-solid block. Fully buried blocks stay hidden. |
| BackgroundOpacity | Integer | 0 | 0 to 255 | Shows the hidden blocks see-through with this opacity. 0 hides them fully. |
| Blocks | Registry List | Ores, containers, liquids, portals and more | | The blocks XRay shows. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleXRay.kt)*
