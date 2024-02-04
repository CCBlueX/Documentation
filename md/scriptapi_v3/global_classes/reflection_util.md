## ReflectionUtil

Since Minecraft's field and method names are obfuscated at runtime, accessing them through reflection would require using obfuscated names. This class provides various reflection related methods which automatically apply mapping to deobfuscate the code.

### Method summary

#### `ReflectionUtil.classByName(name: string): Class`
Returns the class with the given name. <br>
List of parameters:
- *name*, name of the class to get (e.g. `net.minecraft.client.MinecraftClient`).

#### `ReflectionUtil.classByObject(obj: object): Class`
Returns the class of an object. <br>
List of parameters:
- *obj*, the object to return the class of.

#### `ReflectionUtil.newInstance(clazz: Class, ...args: object): object`
Creates a new instance of the given class with the given arguments. <br>
List of parameters:
- *clazz*, the class to create a new instance of.
- *args*, the arguments to pass to the constructor.

#### `ReflectionUtil.newInstanceByName(name: string, ...args: object): object`
Creates a new instance of the class with the given name with the given arguments. <br>
List of parameters:
- *name*, fully-qualified name of the class to create a new instance of.
- *args*, the arguments to pass to the constructor.

#### `ReflectionUtil.newInstanceByObject(obj: object, ...args: object): object`
Creates a new instance of the class of the given object with the given arguments. <br>
List of parameters:
- *obj*, object of whose class to create a new instance of.
- *args*, the arguments to pass to the constructor.

#### `ReflectionUtil.getField(obj: object, name: string): object`
Returns the value of the field with the given name on the given object. <br>
List of parameters:
- *obj*, object of which to get the field.
- *name*, name of the field to get.

#### `ReflectionUtil.getStaticField(clazz: Class, name: string): object`
Returns the value of the static field with the given name on the given class. <br>
List of parameters:
- *clazz*, class of which to get the static field.
- *name*, name of the field to get.

#### `ReflectionUtil.invokeMethod(obj: object, name: string, ...args: object): object`
Invokes the method of the given name on the given object passing the given arguments. Returns the methods return value. <br>
List of parameters:
- *obj*, object on which to invoke the method.
- *name*, name of the method to invoke.
- *args*, arguments to pass to the method.

#### `ReflectionUtil.invokeStaticMethod(clazz: Class, name: string, ...args: object): object`
Invokes the static method of the given name on the given class passing the given arguments. Returns the methods return value. <br>
List of parameters:
- *clazz*, class on which to invoke the static method.
- *name*, name of the method to invoke.
- *args*, arguments to pass to the method.
