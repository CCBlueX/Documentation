## Breadcrumbs

Breadcrumbs leaves a colored trail behind you as you walk, so you can see where you have been. It can also draw trails for other players.

With Temporary on, the trail slowly disappears behind you. Turn Temporary off to keep the whole trail until you change worlds or turn the module off.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| OnlyOwn | Toggle | true | | Only you leave a trail. Off gives every player a trail. |
| Color | Color | LiquidBounce blue, alpha 120 | | Color of the trail. Not used while Rainbow is on. |
| Rainbow | Toggle | false | | Makes the trail change through rainbow colors. |
| Height | Decimal | 0.5 | 0.0..2.0 | How tall the trail is, in blocks. At 0 it is a thin line. |
| Temporary | Toggleable Group | On | | The trail disappears after a while. |
| Temporary → Alive | Integer | 900 ms | 10..10000 ms | How long each part of the trail stays. |
| Temporary → Fade | Toggle | true | | The trail fades out before it disappears. |
| Render | Choice | Plain | Plain, Shader | **Plain** draws the trail normally. **Shader** draws it with a shader effect, and its **Style** setting picks how that looks. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleBreadcrumbs.kt)*
