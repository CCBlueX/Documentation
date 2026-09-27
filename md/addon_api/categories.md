## Categories

Every module belongs to a `ModuleCategory`, which decides the ClickGUI panel it appears in. An add-on can file its modules under the built-in categories or bring its own.

### Built-in categories

`ModuleCategories` holds the built-in ones: `COMBAT`, `PLAYER`, `MOVEMENT`, `RENDER`, `WORLD`, `MISC`, `EXPLOIT` and `FUN`.

```kotlin
object ModuleExample : ClientModule("Example", ModuleCategories.MISC)
```

`ModuleCategories.entries` lists every registered category, `ModuleCategories.byName(name)` finds one regardless of case.

### Custom categories

`ModuleCategory(tag, icon)` takes:

| Property | Description                                                                                          | Required | Type         | Default |
|----------|------------------------------------------------------------------------------------------------------|----------|--------------|---------|
| tag      | Name of the category, shown as the panel title.                                                      | Yes      | `String`     |         |
| icon     | SVG or PNG shown by the ClickGUI, as `namespace:path` for `resources/<namespace>/<path>` in the jar. | No       | `Identifier` | `null`  |

The add-on declares its categories in `categories`:

```kotlin
object ExampleCategories {

    @JvmField
    val EXAMPLE = ModuleCategory("Example", Identifier.fromNamespaceAndPath("example-addon", "clickgui/example.svg"))

}

object ModuleExample : ClientModule("Example", ExampleCategories.EXAMPLE)

class ExampleAddon : LiquidBounceAddon() {

    override val categories = listOf(ExampleCategories.EXAMPLE)

    override fun onInitialize() {
        registerModules(ModuleExample)
    }

}
```

`@JvmField` makes the category a plain static field for Java code.

`categories` is read for every add-on before any `onInitialize()` runs, so add-ons can also file modules under each other's categories. A category that is only known at runtime is registered from `onInitialize()` instead:

```kotlin
val category = registerCategory(ModuleCategory(name))
```

- Category names are unique regardless of case. Registering a name that is taken fails the add-on.
- `registerModules` fails for a module whose category is not registered.
- When an add-on fails, its categories are removed again, unless modules of other add-ons still use them.

### Icons

The icon above resolves to `src/main/resources/resources/example-addon/clickgui/example.svg`. Keep it there and not under Minecraft's `assets/`, see [Resource files](/docs/add-on-api/developers/manifest-and-lifecycle#resource-files). A category without an icon gets the theme's icon for its name, and the client icon if the theme has none.
