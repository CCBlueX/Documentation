## SkinChanger

SkinChanger changes the skin of your own player on your screen. Other players still see your real skin unless you turn on **UploadSkin**.

Use **Online** to copy the skin of any Java Edition player by name, or **File** to load a skin image from your computer.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| ForceOverride | Toggle | false | | Turn this on if your new skin does not show up on some servers. |
| UploadSkin | Toggle | false | | Also sets the skin on your Minecraft account, so everyone sees it. Does not work with legacy accounts. |
| Mode | Mode Selector | Online | Online, File | Where the skin comes from. |
| Mode → Online → Username | Text | LiquidBounce | | Name of the player whose skin you want. |
| Mode → File → Image | File | | | A PNG skin image on your computer. |
| Mode → File → Model | Choice | Default | Slim, Default | Arm shape of the skin: **Slim** (thin arms, like Alex) or **Default** (wide arms, like Steve). |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleSkinChanger.kt)*
