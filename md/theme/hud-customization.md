## HUD Customization

The HUD comes with components that show information on your screen. You can customize which components are visible and where they appear.

### Edit your HUD with the HUD Editor

The HUD Editor lets you put together your HUD visually:

1. Press **RIGHT SHIFT** to open the ClickGUI
2. Select the **HUD Editor** tab at the top of the screen

While the HUD Editor is open, all components become editable.

**Adding components:** Click **Add Component** at the top of the screen to open a drawer listing the components available in your active theme, together with a short description of each. Use the search bar to filter the list and click a component to add it to your HUD. Most components can only be added once, but some, such as **Text** and **Image**, can be added multiple times.

**Moving components:** Drag a component to reposition it. While dragging, a grid is shown and the screen is divided into nine anchor zones. The component is anchored to the zone it is dropped in, so it keeps its position relative to the screen edge or center across different resolutions and GUI scales. Components snap to the grid and align magnetically with nearby components, with guides and the current position shown while you move them.

**Configuring components:** Each component shows its settings right next to it in the editor. To remove a component, click the cross next to its name.

### Configure your HUD Components manually

Components can also be managed through the module settings:

1. Press **RIGHT SHIFT** to open the ClickGUI
2. Navigate to **Render** → **HUD**

![HUD Configuration Small](/images/hud-configuration-small.png)

3. Click on **Themes** → **Name of the Theme** (e.g., LiquidBounce) → **Components**

![HUD Configuration](/images/hud-configuration.png)

From here, you can enable/disable components and adjust their positions.

### Use a different HUD look

The available HUD components and their look are determined by your active [theme](/docs/theme-system/overview). To change the appearance or add components, switch to a different theme from the [Marketplace](/docs/theme-system/overview#installing-themes-from-marketplace) or create your own following the [theme development guide](/docs/theme-system/overview#creating-your-own-theme).

**LiquidBounce Theme:**
![LiquidBounce HUD](/images/hud/liquidbounce-hud.png)

**JelloBounce Theme:**
![JelloBounce HUD](/images/hud/jello-hud.png)

**BeautifyV2 Theme:**
![BeautifyV2 HUD](/images/hud/beautify-hud.png)
