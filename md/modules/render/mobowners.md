## MobOwners

MobOwners displays the owner's name above tamed entities and, optionally, projectiles in the world. Whenever you hover near a wolf, cat, horse, or any other tamable creature, you will see a label showing which player claimed it — useful for quickly identifying whether a mob belongs to you, a teammate, or an unknown player.

By default the module only tracks tamed animals. If you also want to know who fired an arrow, threw a trident, or launched another projectile, enable the **Projectiles** toggle. When the owner is already present in your current game session their name appears instantly; if they are not, LiquidBounce queries the Mojang API in the background and shows "Loading…" until the name is resolved.

This module pairs naturally with [ESP](/docs/modules/render/esp) and [Nametags](/docs/modules/render/nametags) if you want a fuller picture of the entities around you.

**Category:** Render
**Enabled by default:** Yes

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Projectiles | Toggle | false | — | When enabled, also shows the owner's name above projectiles (arrows, tridents, etc.) in addition to tamed animals. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleMobOwners.kt)*
