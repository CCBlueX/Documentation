## NoRotateSet

NoRotateSet prevents the server from forcibly rotating your head. Normally, certain server-side events — such as getting hit, mounting an entity, or specific plugin actions — can snap your view to a new direction without your input. With this module active, those forced rotations are suppressed, keeping your aim and perspective under your control at all times.

The module offers two approaches. **SilentAccept** (the default) quietly acknowledges the server's rotation packets without actually applying them to your view, which is the least detectable option. **ResetRotation** instead resets your head back to where it was immediately after any forced rotation is applied; this mode exposes additional [Rotations](/docs/modules/shared-settings/rotations) settings so you can fine-tune how smoothly and accurately the counter-rotation is performed.

This module pairs well with combat modules such as [KillAura](/docs/modules/combat/killaura) or [Aimbot](/docs/modules/combat/aimbot), where a sudden server-imposed rotation could otherwise throw off your aim mid-fight.

**Category:** Player
**Enabled by default:** Yes

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | SilentAccept | — | Controls how forced server rotations are handled. `SilentAccept` acknowledges them silently without moving your view; `ResetRotation` snaps your view back after a forced rotation is applied. |
| Mode → [ResetRotation] → Rotations | Setting Group | — | — | See [Shared: Rotations](/docs/modules/shared-settings/rotations). |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/ModuleNoRotateSet.kt)*
