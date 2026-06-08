## Twerk

Twerk makes your character automatically and repeatedly sneak and unsneak, creating a rhythmic bobbing motion. It works by toggling the sneak input on a fixed cycle every few game ticks, so your character visually crouches and stands back up continuously without any manual input.

This is a purely cosmetic/fun module — great for messing around on servers, showing off to other players, or just leaving your character dancing while you're idle. You can pair it with other fun modules like [Derp](/docs/modules/fun/derp) or [SkinDerp](/docs/modules/fun/skinderp) for extra visual flair.

The **Delay** setting controls how many ticks each sneak and unsneak phase lasts, letting you dial in anything from a rapid vibration to a slow, deliberate crouch rhythm.

**Category:** Fun
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---------|------|---------|-------|-------------|
| Delay | Integer | 2 | 1–20 | Number of ticks each sneak and unsneak phase lasts. Lower values produce faster twerking; higher values slow it down. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/fun/ModuleTwerk.kt)*
