## SkinChanger

SkinChanger replaces the skin your client displays for your own player model without touching your real Mojang account. The change is purely visual on your end by default — other players still see your actual skin. This makes it handy for recording videos or streaming when you want a specific look without permanently altering your profile.

You can pull a skin straight from any Java Edition account using the **Online** mode (just supply that player's username), or use **File** mode to load any custom PNG skin texture from your computer. When **File** mode is selected you also choose between the classic wide ("Default") and slim arm model types to match your skin artwork. If you want to go further and actually change the skin on your Mojang account at the same time, enable **UploadSkin** — note this requires a non-legacy Mojang account authenticated through the standard Mojang/Microsoft login, and will be silently skipped if you are using a custom authentication service.

On certain servers the standard skin-lookup path can be bypassed or ignored, causing the replaced skin not to appear on your own model. Enable **ForceOverride** to work around this — it hooks deeper into the player rendering pipeline to ensure your chosen skin is always rendered for your character.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| ForceOverride | Toggle | false | — | Forces the skin override through a lower-level render hook. Enable if your chosen skin does not appear on your own player model on some servers. |
| UploadSkin | Toggle | false | — | Also uploads the chosen skin to your Mojang account, making it visible to other players. Requires a non-legacy Mojang account using standard authentication. |
| Mode | Mode Selector | Online | Online, File | Selects the source for the replacement skin: fetch by player username (Online) or load a local image file (File). |
| Mode → [Online] → Username | Text | — | — | The Java Edition username whose skin will be fetched and applied to your player model. |
| Mode → [File] → Image | File | — | — | Path to a local PNG skin texture to use as your player skin. |
| Mode → [File] → Model | Choice | Default | Slim, Default | The arm model type that matches your skin artwork — slim (Alex-style) or default (Steve-style wide arms). |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleSkinChanger.kt)*
