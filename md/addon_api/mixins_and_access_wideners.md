## Mixins and Access Wideners

Add-ons are Fabric mods, so they can change Minecraft's code, and LiquidBounce's, with [Mixins](https://wiki.fabricmc.net/tutorial:mixin_introduction), and open up private members with an access widener.

### Mixins

Mixins are Java classes listed in a Mixin config, which `fabric.mod.json` names under `mixins`:

```json
{
  "required": true,
  "minVersion": "0.8",
  "package": "com.example.addon.mixin",
  "compatibilityLevel": "JAVA_25",
  "client": [
    "MixinExampleTitleScreen"
  ],
  "injectors": {
    "defaultRequire": 1
  }
}
```

A Mixin into a Minecraft class targets Mojang's names, as everything else in the add-on does:

```java
@Mixin(TitleScreen.class)
public class MixinExampleTitleScreen {

    @Inject(method = "init", at = @At("RETURN"))
    private void onInit(CallbackInfo info) {
        System.out.println("[ExampleAddon] Title screen initialised");
    }

}
```

Mixins are always Java, also in a Kotlin add-on.

### Into LiquidBounce

LiquidBounce's classes are targeted like any other. They have no mappings, so these Mixins set `remap = false`:

```java
@Mixin(value = CommandManager.class, remap = false)
public class MixinCommandManager {

    @Inject(method = "execute", at = @At("HEAD"))
    private void onExecute(String command, CallbackInfo ci) {
        System.out.println("[ExampleAddon] ." + command);
    }

}
```

A Kotlin `object` like `CommandManager` compiles to a class with the same name and its functions as instance methods. The [Script API add-on](https://github.com/CCBlueX/LiquidBounce-Addon-ScriptAPI) mixes into `ModuleManager` and `Value` this way.

Code reached only through a Mixin is not part of the [stable API](/docs/add-on-api/developers/stable-api) and can change in any build.

### Priority

Mixins into the same class are applied in order of their priority, lowest first, and a higher priority wins where two Mixins conflict. LiquidBounce's Mixin config uses priority 1337 for its own Mixins into Minecraft, the default is 1000. A Mixin that has to be applied after LiquidBounce's, for example to see or override what LiquidBounce changed in the same class, needs a priority above 1337:

```java
@Mixin(value = LocalPlayer.class, priority = 1500)
public class MixinLocalPlayer {

    @Inject(method = "tick", at = @At("HEAD"))
    private void onTick(CallbackInfo ci) {
    }

}
```

`"mixinPriority"` in the Mixin config sets the default for all of the add-on's Mixins.

### Access wideners

An access widener makes private or final members of Minecraft accessible. `fabric.mod.json` names it under `accessWidener`, and `build.gradle.kts` points Loom at it so the add-on compiles against the widened classes:

```kotlin
loom {
    accessWidenerPath = file("src/main/resources/example-addon.accesswidener")
}
```

```
accessWidener	v1	official

accessible field net/minecraft/client/gui/screens/inventory/AbstractSignEditScreen sign Lnet/minecraft/world/level/block/entity/SignBlockEntity;
```

The header is separated by tabs and uses the `official` namespace, Mojang's names. `./gradlew build` checks every entry against Minecraft and fails on members that do not exist.

LiquidBounce's own access widener does not carry over. Its entries are plain `accessible` and `mutable`, not `transitive-`, so Loom does not apply them when the add-on compiles. Widen everything the add-on uses in its own file, even members LiquidBounce has widened already.
