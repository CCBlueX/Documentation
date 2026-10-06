## ExtendedFirework

ExtendedFirework boosts the speed you gain while flying with an [elytra](/docs/modules/movement/elytrafly) and a firework rocket. Normally a firework rocket pushes you forward at a fixed rate; this module multiplies that push so each rocket carries you noticeably faster and farther.

Leave it on **Normal** for a balanced, ready-to-go boost. Switch to **Custom** if you want to dial in the exact strength along each axis yourself — handy for fine-tuning your elytra travel speed or staying within what a particular server will tolerate. Because the speed gain is obvious, very high multipliers are easy for anti-cheats to flag, so increase it gradually.

**Category:** Movement
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---------|------|---------|-------|-------------|
| Mode | Mode Selector | Normal | Normal, Custom | Chooses how the firework boost is amplified: a preset Normal strength or a fully Custom one. |
| Mode → Custom → VelocityMultiplier | Vector3_d | (0.1, 1.65, 0.5) | — | The per-axis (X, Y, Z) multiplier applied to the firework boost when Mode is set to Custom. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/exploit/ModuleExtendedFirework.kt)*
