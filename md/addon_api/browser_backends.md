## Browser Backends

LiquidBounce shows its interface (ClickGUI, HUD, menus) as web pages, rendered by a browser backend. The client comes with a backend that opens pages in the system's browser (`external`), and with an add-on of its own that offers Chromium (`cef`). An add-on can offer another one, as [LiquidBounce-Addon-Wry](https://github.com/CCBlueX/LiquidBounce-Addon-Wry) does with the web view built into the operating system.

### Registering a backend

```kotlin
class ExampleAddon : LiquidBounceAddon() {

    override fun onInitialize() {
        registerBrowserBackend(
            BrowserBackendProvider(
                "example-system",
                "System browser",
                "Opens the client's pages in your default browser.",
            ) { SystemBrowserBackend() }
        )
    }

}
```

`BrowserBackendProvider` takes:

| Property    | Description                                                                                 | Required | Type                   | Default |
|-------------|---------------------------------------------------------------------------------------------|----------|------------------------|---------|
| id          | Unique id, accepted by `LB_BROWSER_BACKEND`.                                                | Yes      | `String`               |         |
| name        | Shown on the selection screen and stored as the value of the **Backend** setting.           | Yes      | `String`               |         |
| description | Shown below the name.                                                                       | Yes      | `String`               |         |
| selectable  | Whether the selection screen offers it. When false, only `LB_BROWSER_BACKEND` picks it.     | No       | `Boolean`              | `true`  |
| create      | Creates the backend. Only called for the backend that is used.                              | Yes      | `() -> BrowserBackend` |         |

Registering an id that is taken fails the add-on.

### Choosing a backend

The client picks the backend while it starts, after every add-on's `onInitialize()`:

- `LB_BROWSER_BACKEND=<id>` as environment variable, or `-Dnet.ccbluex.liquidbounce.browser.backend=<id>`, uses that backend. `none` starts without one.
- With only one selectable backend, that one is used.
- Otherwise the **Backend** setting decides. It offers every selectable backend and defaults to **Ask**, which lets a screen ask the player at startup and stores the picked backend in the setting. While **SHIFT** is held during startup, that screen asks again.

### Implementing a backend

A backend implements `BrowserBackend`, its pages implement `Browser`. The smallest complete backend hands every page to the system browser, as the client's own `external` backend does:

```kotlin
class SystemBrowserBackend : BrowserBackend {

    override val isInitialized = true
    override val browsers = mutableListOf<SystemBrowser>()
    override val supportsIncognito = false

    override fun makeDependenciesAvailable(taskManager: TaskManager, whenAvailable: () -> Unit) = whenAvailable()

    override fun start() = Unit

    override fun stop() = browsers.clear()

    override fun update() = Unit

    override fun createBrowser(
        url: String,
        position: BrowserViewport,
        settings: BrowserSettings,
        priority: Short,
        incognito: Boolean,
        inputAcceptor: InputAcceptor?,
    ) = SystemBrowser(this, url, position, priority).also { browsers += it }

}

class SystemBrowser(
    private val backend: SystemBrowserBackend,
    url: String,
    override var viewport: BrowserViewport,
    override var priority: Short,
) : Browser {

    override val isInitialized = true
    override val isIncognito = false
    override val state: BrowserState = BrowserState.Stateless
    override var visible = true
    override val texture: BrowserTexture? = null

    override var url = url
        set(value) {
            field = value
            Blaze3D.openUri(URI(value))
        }

    init {
        Blaze3D.openUri(URI(url))
    }

    override fun forceReload() = Unit
    override fun reload() = Unit
    override fun goForward() = Unit
    override fun goBack() = Unit
    override fun invalidate() = Unit

    override fun update(width: Int, height: Int) {
        viewport = viewport.copy(width = width, height = height)
    }

    override fun close() {
        backend.browsers.remove(this)
    }

    override fun toString() = "SystemBrowser($url)"

}
```

#### `BrowserBackend`

| Member                                          | Description                                                                                         |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| `makeDependenciesAvailable(taskManager, whenAvailable)` | Called first, on the render thread at startup. Download or unpack what the backend needs, then call `whenAvailable` on the render thread, from a background task with `mc.execute(whenAvailable)`. Work launched on `taskManager` is shown in the client's progress screen until it finishes. |
| `start()`                                       | Called on the render thread once `whenAvailable` was called.                                        |
| `update()`                                      | Called every frame on the render thread while `isInitialized` is true.                              |
| `stop()`                                        | Called when the game shuts down.                                                                    |
| `createBrowser(url, position, settings, priority, incognito, inputAcceptor)` | Opens a page and returns its `Browser`.                            |
| `isInitialized`                                 | Whether `start()` has finished.                                                                     |
| `browsers`                                      | The open pages.                                                                                     |
| `supportsIncognito`                             | Whether a page can get cookies and storage of its own, kept in memory only.                         |

`createBrowser` gets the page's `url`, its `position` on screen as a `BrowserViewport` (`BrowserViewport.fullscreen()` for the whole window), `settings` with the frame rate limit, a `priority`, whether the page should be `incognito`, and an `inputAcceptor` that tells when the page may take mouse and keyboard input.

#### `Browser`

| Member                                     | Description                                                                                  |
|--------------------------------------------|----------------------------------------------------------------------------------------------|
| `texture`                                  | The page's current frame as a `BrowserTexture`, or `null`. The client draws it in `viewport` while `visible`. |
| `viewport`, `visible`, `priority`          | Where the page is, whether it is shown, and the priority it was created with.|
| `url`                                      | The current page. Setting it navigates.                                                      |
| `state`                                    | `Idle`, `Loading`, `Success(httpStatusCode)`, `Failure(errorCode, errorText, failedUrl)` or `Stateless`. |
| `update(width, height)`                    | The window was resized.                                                                      |
| `reload()`, `forceReload()`, `goBack()`, `goForward()` | Navigation; `forceReload()` ignores the cache.                                   |
| `invalidate()`                             | Redraw the page.                                                                             |
| `close()`                                  | The page is no longer needed.                                                                |

`BrowserTexture` wraps Minecraft's `TextureSetup` with the texture's size, whether its pixels are BGRA instead of RGBA, and `u1`, `v1`, `u2`, `v2` for the part of the texture that holds the page.

The client does not pass input to pages. A backend whose pages take input listens for it itself, for example with a handler for `MouseButtonEvent` and `KeyboardKeyEvent`, and only acts while the `inputAcceptor` accepts it.
