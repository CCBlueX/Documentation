## Hitbox

Hitbox makes the boxes around enemies bigger, so your hits land even when your aim is a little off. Big values are easy for anticheats to notice.

**Category:** Combat
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Size | Decimal | 0.1 | 0.0..1.0 | How much bigger each side of the enemy's box gets, in blocks. |
| ApplyToDebugHitbox | Toggle | true | | Also makes the hitbox outlines bigger when you show them with F3+B. |
| ApplyToComponent | Toggle | true | | Also uses the bigger box for weapons that have their own attack range, like spears. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/ModuleHitbox.kt)*
