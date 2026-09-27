## Project Setup

An add-on is a Gradle project with Fabric Loom and the Kotlin plugin. The [template](https://github.com/CCBlueX/LiquidBounce-Addon-Template) has all of this set up; this page explains what it contains.

### Gradle and JDK

The template's wrapper runs Gradle 9.6.1, the same as LiquidBounce. Minecraft 26.1 and later need Java 25. `jdk` in `gradle/libs.versions.toml` sets the toolchain for Java and Kotlin and the Java release target:

```kotlin
tasks.withType<JavaCompile>().configureEach {
    options.encoding = "UTF-8"
    options.release = libs.versions.jdk.get().toInt()
}

java {
    withSourcesJar()

    toolchain {
        languageVersion = JavaLanguageVersion.of(libs.versions.jdk.get().toInt())
    }
}

kotlin {
    compilerOptions {
        jvmToolchain(libs.versions.jdk.get().toInt())
        freeCompilerArgs.add("-Xskip-prerelease-check")
    }
}
```

LiquidBounce is compiled with Kotlin preview features, which marks its classes as pre-release. Without `-Xskip-prerelease-check`, the Kotlin compiler refuses to compile against them.

### Versions

`gradle/libs.versions.toml` holds every version, library and plugin. Keep the versions in line with the LiquidBounce build the add-on compiles against. A mismatch in `minecraft`, `fabric-loom` or `kotlin` is the usual cause of an add-on that compiles and then crashes at runtime. The catalog for LiquidBounce on Minecraft 26.3:

```toml
[versions]
jdk = "25"

minecraft = "26.3"
fabric-loom = "1.17-SNAPSHOT"
fabric-loader = "0.19.5"
fabric-api = "0.160.5+26.3"

kotlin = "2.4.20"
fabric-kotlin = "1.14.1+kotlin.2.4.20"

liquidbounce = "0.40.1+26.3-SNAPSHOT"

[libraries]
minecraft = { group = "com.mojang", name = "minecraft", version.ref = "minecraft" }
fabric-loader = { group = "net.fabricmc", name = "fabric-loader", version.ref = "fabric-loader" }
fabric-api = { group = "net.fabricmc.fabric-api", name = "fabric-api", version.ref = "fabric-api" }
fabric-kotlin = { group = "net.fabricmc", name = "fabric-language-kotlin", version.ref = "fabric-kotlin" }
liquidbounce = { group = "net.ccbluex", name = "liquidbounce", version.ref = "liquidbounce" }

[plugins]
fabric-loom = { id = "net.fabricmc.fabric-loom", version.ref = "fabric-loom" }
kotlin-jvm = { id = "org.jetbrains.kotlin.jvm", version.ref = "kotlin" }
```

LiquidBounce's own [`gradle/libs.versions.toml`](https://github.com/CCBlueX/LiquidBounce/blob/nextgen/gradle/libs.versions.toml) is the reference for these.

The `liquidbounce` version takes one of three forms:

| Form                            | Example                        | Repository  | Resolves to                                                  |
|---------------------------------|--------------------------------|-------------|--------------------------------------------------------------|
| `<version>+<mc>`                | `0.40.1+26.3`                  | `releases`  | a release                                                    |
| `<version>+<mc>-SNAPSHOT`       | `0.40.1+26.3-SNAPSHOT`         | `snapshots` | the newest development build, moves with every push to `nextgen` |
| `<version>+<mc>-<sha>-SNAPSHOT` | `0.40.1+26.3-cadfef0-SNAPSHOT` | `snapshots` | the development build of one commit                          |

Gradle keeps a resolved snapshot for a day. The template turns that off so `-SNAPSHOT` always means the newest build:

```kotlin
configurations.all {
    resolutionStrategy.cacheChangingModulesFor(0, "seconds")
}
```

### Plugins and repositories

The plugins come from the catalog. Loom itself is resolved from Fabric's Maven, declared in `settings.gradle.kts`:

```kotlin
pluginManagement {
    repositories {
        maven {
            name = "Fabric"
            url = uri("https://maven.fabricmc.net/")
        }
        gradlePluginPortal()
        mavenCentral()
    }
}
```

```kotlin
plugins {
    alias(libs.plugins.fabric.loom)
    alias(libs.plugins.kotlin.jvm)
}
```

LiquidBounce is published to `https://maven.ccbluex.net`, releases and development builds each with a sources jar, which IDEs attach automatically.

```kotlin
repositories {
    mavenCentral()
    mavenLocal()
    maven {
        name = "CCBlueX Releases"
        url = uri("https://maven.ccbluex.net/releases")
    }
    maven {
        name = "CCBlueX Snapshots"
        url = uri("https://maven.ccbluex.net/snapshots")
    }
    maven {
        name = "Fabric"
        url = uri("https://maven.fabricmc.net/")
    }
}
```

### Dependencies

```kotlin
dependencies {
    minecraft(libs.minecraft)

    implementation(libs.fabric.loader)
    implementation(libs.fabric.api)
    implementation(libs.fabric.kotlin)

    implementation(libs.liquidbounce)
}
```

- The dependency is the client itself, `net.ccbluex:liquidbounce`. There is no separate API artifact. Its POM declares no dependencies, so the add-on declares Minecraft, Fabric Loader, Fabric API and Fabric Language Kotlin itself.
- Use `implementation`, not `modImplementation`. For these Minecraft versions Loom has no remapping step, development and production both use Mojang's names, and the `mod*` configurations do not exist.
- Do not add a `mappings(...)` line. LiquidBounce declares none, and Loom defaults to Mojang's official names. A different mapping set produces an add-on that compiles and then fails on every Minecraft call.

### Loom

```kotlin
loom {
    accessWidenerPath = file("src/main/resources/example-addon.accesswidener")
}
```

`accessWidenerPath` points Loom at the add-on's access widener, which it applies to the Minecraft classes the add-on compiles against. The same file is named under `accessWidener` in `fabric.mod.json`, see [Mixins and Access Wideners](/docs/add-on-api/mixins-and-access-wideners#access-wideners). Loom also provides `./gradlew runClient`, which starts the game with LiquidBounce and the add-on. Game tests need more configuration, see [Testing](/docs/add-on-api/testing).

### Add-on version

`gradle.properties` holds the add-on's own coordinates:

```properties
mod_version=1.0.0
maven_group=com.example
archives_base_name=example-addon
```

The Minecraft version goes into the add-on's version:

```kotlin
base {
    archivesName = project.property("archives_base_name") as String
    version = "${project.property("mod_version")}+${libs.versions.minecraft.get()}"
    group = project.property("maven_group") as String
}
```

`./gradlew build` writes `build/libs/example-addon-1.0.0+26.3.jar` and `example-addon-1.0.0+26.3-sources.jar`. The jar carries the project's `LICENSE` as `LICENSE_example-addon`. The same `mod_version` can be released once per Minecraft version, see [Publishing](/docs/add-on-api/publishing).

`processResources` fills these placeholders in `fabric.mod.json`:

| Placeholder                | Value                                                   |
|----------------------------|---------------------------------------------------------|
| `${version}`               | `<mod_version>+<minecraft>`, for example `1.0.0+26.3`   |
| `${minecraft_version}`     | `minecraft` from the catalog                            |
| `${loader_version}`        | `fabric-loader` from the catalog                        |
| `${fabric_kotlin_version}` | `fabric-kotlin` from the catalog                        |

### Building against a local client

To compile against changes that are not published yet, publish a LiquidBounce checkout to the local Maven repository under a version of your own. The checkout needs everything LiquidBounce's own build needs, Node.js included (see its [README](https://github.com/CCBlueX/LiquidBounce#readme)).

```sh
./gradlew publishToMavenLocal -Ppublish.version=0.40.1+26.3-local-SNAPSHOT
```

Then point the add-on at it. `mavenLocal()` is already among the template's repositories.

```toml
liquidbounce = "0.40.1+26.3-local-SNAPSHOT"
```

Without `-Ppublish.version`, the checkout publishes `<mod_version>+<mc>-SNAPSHOT`, the same version as the moving development build. Since `mavenLocal()` comes before the CCBlueX repositories, the add-on then keeps resolving the local build until it is removed from `~/.m2/repository/net/ccbluex/liquidbounce/`.
