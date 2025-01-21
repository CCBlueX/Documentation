## Theme System
LiquidBounce features a Theme System that allows you to customize the appearance of the client. The theme affects all graphical user interfaces (GUIs) throughout the client, including but not limited to the HUD, ClickGUI, main menu, and any other visual elements.

### LiquidBounce Theme
The default theme of LiquidBounce provides a clean and modern look:

![Default HUD](/images/liquidbounce-hud.png)
![Default ClickGUI](/images/liquidbounce-clickgui.png)
![Default Main Menu](/images/liquidbounce-mainmenu.png)

### Using Themes
You can manage themes using the following commands:

#### `.client theme list`
This command displays all available themes that are installed in your themes directory.

#### `.client theme browse`
Opens your themes directory (shown below) where themes are stored:

![Themes Directory](/images/themes-directory.png)

#### `.client theme set <name>`
Applies the specified theme. For example: `.client theme set jellobounce`

### Custom Themes

<div class="note js-note">
	<span class="note-close js-close">
		<i class="fa fa-times"></i>
	</span>
	<h4 class="note-title"> Note </h4>
	<p class="note-description">Custom Theme support is currently an experimental feature. The Marketplace for Automatic Theme Updates is still in development.</p>
</div>

#### How To Install
You can install custom themes from the community.

1. Visit the releases page of the theme.
2. Download the latest release
3. Extract the content of the ZIP file to your themes folder
4. Start LiquidBounce
5. Type `.client theme set <name>`

#### JelloBounce Theme
Here's how the JelloBounce theme changes the appearance of various GUIs:

![JelloBounce HUD](/images/jellobounce-hud.png)
![JelloBounce ClickGUI](/images/jellobounce-clickgui.png)
![JelloBounce Main Menu](/images/jellobounce-mainmenu.png)

[Releases](https://github.com/larryngton2/jellobounce/releases)

#### Catppuccin Theme
[Releases](https://github.com/liquidsquid1/catppuccin-lb/releases)

For most users, we recommend waiting for the upcoming Marketplace feature which will simplify the theme installation process.