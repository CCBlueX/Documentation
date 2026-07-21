## HUD Customization

The HUD comes with componenents that show information on your screen. You can customize which components are visible and where they appear.

### Configure your HUD Components

1. Press **RIGHT SHIFT** to open the ClickGUI
2. Navigate to **Render** → **HUD**

![HUD Configuration Small](/images/hud-configuration-small.png)

3. Click on **Themes** → **Name of the Theme** (e.g., LiquidBounce) → **Components**

![HUD Configuration](/images/hud-configuration.png)

From here, you can enable/disable components and adjust their positions.

### Edit your HUD visually

The newest version of LiquidBounce also includes a visual HUD editor in the ClickGUI. In the editor you can drag components directly on the screen to reposition them, with anchor points and snapping guides helping you align them. A drawer lists the components available in your active theme together with a short description of each, so you can add them to your HUD from there — some components, such as **Text** and **Image**, can be added multiple times. You can also adjust a component's settings directly in the editor. When components overlap, clicking one in the editor brings it in front of the others; this stacking order is saved with your config.

### Replace scoreboard text

In the newest version of LiquidBounce, the **Scoreboard** component of the default theme can rewrite the text it displays using a regular expression. In the component's settings, enter a pattern in **ReplaceRegex** and the text to insert in **ReplaceWith** — every match in the scoreboard's header, entry names and scores is replaced. If **ReplaceRegex** is empty or not a valid regular expression, the scoreboard is shown unchanged.

### Adjust an image's opacity

The **Image** component of the default theme can display a picture either from a web address or from a file on your computer. Its **Source** setting chooses between the two: with **URL** selected you enter the image's address, and with **File** selected you pick a local file (PNG, JPG, JPEG, WEBP, GIF or SVG). It also has an **Opacity** setting that controls how see-through the displayed picture is, from 0% (fully transparent) to 100% (fully opaque, the default). Large images are automatically limited in height so they do not cover the whole screen.

### Show Minecraft's closed captions

The default theme includes a **ClosedCaptions** component that shows Minecraft's closed captions (Settings → Accessibility Settings → Closed Captions) on the HUD. Captions keep the text and background colors of the vanilla subtitles, and an arrow next to a caption points in the direction the sound came from. While the component is shown, the vanilla subtitle overlay is hidden so captions do not appear twice. The component is disabled by default and can only be added to the HUD once.

### Use a different HUD look

The available HUD components and their look are determined by your active [theme](/docs/theme-system/overview). To change the appearance or add components, switch to a different theme from the [Marketplace](/docs/theme-system/overview#installing-themes-from-marketplace) or create your own following the [theme development guide](/docs/theme-system/overview#creating-your-own-theme).

**LiquidBounce Theme:**
![LiquidBounce HUD](/images/hud/liquidbounce-hud.png)

**JelloBounce Theme:**
![JelloBounce HUD](/images/hud/jello-hud.png)

**BeautifyV2 Theme:**
![BeautifyV2 HUD](/images/hud/beautify-hud.png)