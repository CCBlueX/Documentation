## Global instances

The following instances (variables) are available globally in the script.

## `mc`

Shorthand for *Minecraft.getInstance()*. Contains most methods and fields used to interact with the client; most importantly, *mc.player*.

## `localStorage`

This `localStorage` is different from browser environment `localStorage` like Chrome. It's a [ConcurrentHashMap](https://docs.oracle.com/en/java/javase/21/docs/api/java.base/java/util/concurrent/ConcurrentHashMap.html), using `String` as key. You can share variables among scripts with it. There are some points you should know:

- It is not persisted, so if the game is restarted, all content will be lost.
- It doesn't support `null` key or values. (ConcurrentHashMap requirement)
- All scripts can write and delete entires from it, so you should choose your keys carefully. We recommend that you use this format: `AuthorName:ScriptName:VariableIdentifier`.
  
