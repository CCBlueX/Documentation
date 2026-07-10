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

The newest version of LiquidBounce also includes a visual HUD editor in the ClickGUI. In the editor you can drag components directly on the screen to reposition them, with anchor points and snapping guides helping you align them. A drawer lists the components available in your active theme together with a short description of each, so you can add them to your HUD from there — some components, such as **Text** and **Image**, can be added multiple times. You can also adjust a component's settings directly in the editor.

### Replace scoreboard text

In the newest version of LiquidBounce, the **Scoreboard** component of the default theme can rewrite the text it displays using a regular expression. In the component's settings, enter a pattern in **ReplaceRegex** and the text to insert in **ReplaceWith** — every match in the scoreboard's header, entry names and scores is replaced. If **ReplaceRegex** is empty or not a valid regular expression, the scoreboard is shown unchanged.

### Use a different HUD look

The available HUD components and their look are determined by your active [theme](/docs/theme-system/overview). To change the appearance or add components, switch to a different theme from the [Marketplace](/docs/theme-system/overview#installing-themes-from-marketplace) or create your own following the [theme development guide](/docs/theme-system/overview#creating-your-own-theme).

**LiquidBounce Theme:**
![LiquidBounce HUD](/images/hud/liquidbounce-hud.png)

**JelloBounce Theme:**
![JelloBounce HUD](/images/hud/jello-hud.png)

**BeautifyV2 Theme:**
![BeautifyV2 HUD](/images/hud/beautify-hud.png)