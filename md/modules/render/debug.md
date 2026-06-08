## Debug

Debug is a diagnostic overlay aimed squarely at developers and advanced users who want to peek under the hood of the client. When other modules expose internal data — server-sided rotations, hitboxes, target lines, predicted paths and other geometry, plus live parameter values — Debug draws that information into the world and onto your screen so you can see exactly what the client is calculating.

For everyday play there's nothing here to gain; it doesn't give you any in-game advantage. It's most useful when you're testing behavior, reporting a bug, or trying to understand why a feature like [KillAura](/docs/modules/combat/killaura) or [Scaffold](/docs/modules/world/scaffold) is acting a certain way. Captured parameter values are shown in a list that fades out after a set time, and holding the player-list (Tab) key temporarily hides that overlay.

The optional groups add their own visualizations: SimulatedPlayer draws a predicted line showing where your movement is heading over the next several ticks, and Graph renders a small on-screen plot of an editable curve for tuning value mappings.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
| --- | --- | --- | --- | --- |
| Parameters | Toggle | true | — | Shows the on-screen list of captured parameter values reported by other modules. |
| Geometry | Toggle | true | — | Draws debug geometry (lines, boxes, points, triangles) that other modules submit into the world. |
| Expires | Integer | 5 | 1..30 (secs) | How long a captured parameter value stays on screen before fading away. |
| SimulatedPlayer | Toggleable Group | off | — | Draws a line predicting your movement path over the coming ticks. |
| SimulatedPlayer → TicksToPredict | Integer | 20 | 5..100 | How many ticks ahead the predicted movement path is simulated. |
| Graph | Toggleable Group | off | — | Renders an on-screen plot of the editable curve below for visual tuning. |
| Graph → Curve | Curve | — | — | The curve drawn and edited in the on-screen graph. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleDebug.kt)*
