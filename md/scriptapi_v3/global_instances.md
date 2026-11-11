## Global instances

The following instances (variables) are available globally in the script.

## `mc`

Shorthand for *Minecraft.getInstance()*. Contains most methods and fields used to interact with the client; most importantly, *mc.player*.

## `localStorage`

This `localStorage` is different from the `localStorage` of a browser. It's a [ConcurrentHashMap](https://docs.oracle.com/en/java/javase/21/docs/api/java.base/java/util/concurrent/ConcurrentHashMap.html), using `String` as key. You can share variables among scripts with it. There are some points you should know:

- It is not persisted, so if the game is restarted, all content will be lost. Reloading scripts clears it as well.
- It doesn't support `null` keys or values (a ConcurrentHashMap requirement).
- All scripts can write and delete entries in it, so you should choose your keys carefully. We recommend that you use this format: `AuthorName:ScriptName:VariableIdentifier`.

## Preloaded classes

These classes can be used without `Java.type`:

- `Vec3i`, `Vec3`, `Mth`, `BlockPos`, `InteractionHand`, `Axis` and `RenderSystem` from Minecraft
- `Color4b`, LiquidBounce's color class
- `Vec3d`, `MathHelper`, `Hand` and `RotationAxis`, the Yarn names of `Vec3`, `Mth`, `InteractionHand` and `Axis`, for older scripts

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce-Addon-ScriptAPI/blob/143f553/src/main/kotlin/net/ccbluex/liquidbounce/script/bindings/api/ScriptContextProvider.kt)*
