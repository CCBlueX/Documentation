## ReflectionUtil

This class provides reflection helpers for accessing fields, methods and constructors that are not reachable from a script directly, for example private members. Minecraft is not obfuscated, so names are the Mojang names used in the game's code.

### Method summary

#### `ReflectionUtil.classByName(name: string): Class`
Returns the class with the given name. <br>
List of parameters:
- *name*, name of the class to get (e.g. `net.minecraft.client.Minecraft`). Slashes are accepted in place of dots.

<hr>

#### `ReflectionUtil.newInstance(clazz: Class, ...args: object): object`
Creates a new instance of the given class with the given arguments. Private constructors work too; the constructor is matched by the exact classes of the arguments. <br>
List of parameters:
- *clazz*, the class to create a new instance of.
- *args*, the arguments to pass to the constructor.

<hr>

#### `ReflectionUtil.newInstanceByName(name: string, ...args: object): object`
Creates a new instance of the class with the given name with the given arguments. <br>
List of parameters:
- *name*, fully-qualified name of the class to create a new instance of.
- *args*, the arguments to pass to the constructor.

<hr>

#### `ReflectionUtil.newInstanceByObject(obj: object, ...args: object): object`
Creates a new instance of the class of the given object with the given arguments. <br>
List of parameters:
- *obj*, object of whose class to create a new instance of.
- *args*, the arguments to pass to the constructor.

<hr>

#### `ReflectionUtil.getField(obj: object, name: string): object`
Returns the value of the public field with the given name on the given object. <br>
List of parameters:
- *obj*, object of which to get the field.
- *name*, name of the field to get.

<hr>

#### `ReflectionUtil.getDeclaredField(clazz: Class, name: string): object`
Returns the value of the static field with the given name declared in the given class, including private ones. <br>
List of parameters:
- *clazz*, class of which to get the static field.
- *name*, name of the field to get.

<hr>

#### `ReflectionUtil.invokeMethod(obj: object, name: string, ...args: object): object`
Invokes the public method of the given name on the given object passing the given arguments. Returns the method's return value. Overloads are matched by the number and types of the arguments; `null` arguments are not supported. <br>
List of parameters:
- *obj*, object on which to invoke the method.
- *name*, name of the method to invoke.
- *args*, arguments to pass to the method.

**Example:**

```js
ReflectionUtil.invokeMethod(mc.player, "setSprinting", true);
```

<hr>

#### `ReflectionUtil.invokeDeclaredMethod(clazz: Class, name: string, ...args: object): object`
Invokes the static method of the given name declared in the given class, including private ones. Inherited methods are not found. Returns the method's return value. <br>
List of parameters:
- *clazz*, class on which to invoke the static method.
- *name*, name of the method to invoke.
- *args*, arguments to pass to the method.

<hr>

#### `ReflectionUtil.invalidateCache(): void`
Clears the cache of fields and methods looked up so far.

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce-Addon-ScriptAPI/blob/143f553/src/main/kotlin/net/ccbluex/liquidbounce/script/bindings/api/ScriptReflectionUtil.kt)*
