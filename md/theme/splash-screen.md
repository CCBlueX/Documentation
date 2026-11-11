## Splash Screen

A theme can bring its own splash screen: the animation that plays while Minecraft loads its resources, while LiquidBounce asks which browser to use on the first start, while it downloads what it needs, on the way into the main menu, and behind the error screen when LiquidBounce runs into an error it cannot recover from. A theme without one gets Minecraft's own loading screen.

The splash screen is a [Lottie](https://lottiefiles.com/what-is-lottie) animation, the JSON format After Effects exports through the Bodymovin plugin and that tools such as LottieFiles and Figma plugins can write. LiquidBounce draws it natively, without a browser, so it is ready from the first frame.

### Files

A splash screen lives in the theme's `public` folder:

```
public/
├── metadata.json
├── splash/
│   ├── animation.json
│   └── images/
│       ├── logo.png
│       └── ...
└── sounds/
    └── splash-hit.ogg
```

The included theme's splash in the [LiquidBounce repository](https://github.com/CCBlueX/LiquidBounce/tree/nextgen/src-theme/public/splash) is a complete example.

Add a `splash` section to `metadata.json`:

```json
{
  "id": "your-custom-id",
  "name": "YourTheme",
  "version": "0.1.0",
  "authors": ["YourName"],
  "splash": {
    "animation": "splash/animation.json",
    "background": "#181a1b",
    "text": "#ffffff",
    "accent": "#4677ff"
  }
}
```

| Field | Meaning |
|---|---|
| `animation` | Path of the Lottie file, relative to `public`. Required. |
| `background` | Color behind the animation. It fills the window around the composition and fades into the menu. Defaults to `#181a1b`. |
| `text` | Color of the client's own text: the download status, the browser choice and the error screen. Defaults to white. |
| `accent` | Color of the selected entry in the browser choice and the error screen. Defaults to `#4677ff`. |

### Making the animation

Design the composition at **1920×1080**. It is scaled to fit the window and centered; on other aspect ratios the `background` color fills the rest. Any frame rate works.

When exporting from After Effects with Bodymovin, keep images as separate files (**Assets: Copy original images**) rather than embedding them, and store them next to `animation.json` under the folder the export names (`images/` by default). Embedded `data:` images also work but make the file larger.

LiquidBounce plays this part of the format:

- **Image layers**, from PNG files up to 2048×2048. Export them at about the size they appear on a 1920×1080 screen.
- **Solid layers** and **null layers**.
- **Precomps**, with their opacity applied to everything inside.
- **Shape layers** with rectangles (including rounded corners), ellipses and fills. Put one fill in each group.
- **Transforms**: anchor point, position (also with separated dimensions), scale, rotation and opacity, with the bezier easing of their keyframes and hold keyframes.
- **Parenting**: a layer follows the transform of its parent, but not its opacity, as in After Effects.
- **Masks** in *Add* mode. A mask clips the layer to the rectangle around it, which covers wipes and reveals.

Text layers, effects, expressions, track mattes, other shapes such as paths and strokes, and subtract or intersect masks are skipped. The client lists what it skipped in its log.

### Phases

The splash screen follows the client through several phases. Mark them with composition markers named like the phase. Each phase plays once and then holds its last frame, or loops the segment of the marker `<phase>-loop` if there is one.

| Marker | When it plays |
|---|---|
| `intro` | When loading starts. Without an `intro` marker, the whole animation is the intro. |
| `choice` | On the first start, while LiquidBounce asks which browser to use. |
| `tasks` | While LiquidBounce downloads or prepares what it needs, after loading. |
| `outro` | When the splash fades into the main menu. The background fades out over one second, so keep the outro at most one second long. |
| `error` | Behind the error screen. Its text and buttons, about 150 GUI pixels tall, are drawn below the `content` layer, so move the logo up and leave room. An error after the splash has ended plays the `intro` first. |

A phase without a marker keeps showing what is on screen. A new phase starts once the current one has played to its end, while a loop is left right away. When loading finishes before the intro does, the rest of the intro plays three times as fast so the client does not wait for it. Loading never waits for the animation.

The marker's duration is the length of its segment, so the markers can sit one after the other on the same timeline.

### Progress and text

Two layer names connect the animation to the client:

- **`progress`**: this layer is stretched horizontally around its anchor point by the loading progress, from 0 to 100%. Put the anchor point at the left edge of your bar. The progress only grows: during the first start, loading and the downloads after it share one bar.
- **`content`**: the anchor point of this layer, usually a null layer, is where the client places its own text. The download status, the browser choice and the error screen are drawn centered below it, in the theme's font (`nativeFont`). Animate it to move the text with your design. The text fades in once the phase has played in, so it does not cross moving parts. Without the layer, the text sits at 70% of the window height.

### Sounds

Add a marker named `sound:<name>` to play `sounds/<name>.ogg` from your theme when the animation passes it. The files are Ogg Vorbis, the same folder the `sounds` field of `metadata.json` uses. Set the loudness of each sound in the file itself; the game's master volume applies on top.

The splash plays its sounds before Minecraft's sound engine is ready, so they do not have to be listed in the `sounds` field.

### Limits

To keep loading fast, a splash screen may have at most 256 layers, PNG images up to 2048×2048, sounds up to about 45 seconds and 16 MiB of files in total. It may only use files inside the theme.

A splash screen that cannot be read, fails to draw, or takes longer than 20 ms per frame for 30 frames in a row is replaced by Minecraft's own loading screen until the theme changes, and the log says why. Loading goes on either way.

### Testing your splash screen

1. Apply your theme with `.client theme set <id>`, or your development server with `.client theme set http://localhost:5173/`.
2. LiquidBounce uses the splash screen of the active theme from the next loading screen on. An installed theme also shows it right at the next start; a development server only while it is applied. Press **F3 + T** to reload resources and watch it, or restart the game.

---

*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/render/splash/Splash.kt)*
