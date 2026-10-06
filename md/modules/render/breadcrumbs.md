## Breadcrumbs

Breadcrumbs draws a continuous trail along the ground that marks where players have walked, like a ribbon following their footsteps. Each game tick the module records a player's position and adds it to that player's trail, then the renderer connects those points into a flat strip (or a thin line when Height is 0). It's a purely cosmetic Render module — handy for visualizing your own movement paths, reviewing routes, or just for the look.

By default it only tracks your own player (OnlyOwn), but you can turn that off to leave trails behind every player in the world. The trail can be a fixed color or a cycling rainbow, and stands up off the ground by the Height value to form a visible wall rather than a flat line. The most recent segment is anchored to the player's smoothly interpolated position, so the trail stays glued to them as they move ([the trail render logic](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleBreadcrumbs.kt#L152-L189)).

With the Temporary group enabled (the default), each trail point expires after the Alive time and is dropped, keeping the trail to a rolling tail behind the player. Disable Temporary to let trails grow indefinitely until you change worlds or disable the module. When Fade is on, points gradually become more transparent as they approach their expiration, so the tail softly disappears at the end ([fade and expiration handling](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleBreadcrumbs.kt#L156-L182)).

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
| --- | --- | --- | --- | --- |
| OnlyOwn | Toggle | true | — | When on, only your own player leaves a trail. Turn off to draw trails for all players in the world. |
| Color | Color | — | — | The color and base opacity of the trail. Ignored while Rainbow is enabled. |
| Rainbow | Toggle | false | — | Cycles the trail through rainbow colors over time instead of using the fixed Color. |
| Height | Decimal | 0.5 | 0.0..2.0 | How tall the trail stands off the ground, in blocks. At 0.0 the trail is drawn as a thin line instead of a filled strip. |
| Temporary | Toggleable Group | on | — | When enabled, trail points expire over time so only a rolling tail is kept. Disable to let trails persist until a world change or the module is turned off. |
| Temporary → Alive | Integer | 900 | 10..10000 (ms) | How long each trail point remains before it is removed, in milliseconds. |
| Temporary → Fade | Toggle | true | — | Fades trail points to fully transparent as they approach the end of their Alive time. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleBreadcrumbs.kt)*
