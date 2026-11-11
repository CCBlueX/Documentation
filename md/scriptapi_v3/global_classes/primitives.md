## Primitives

The `Primitives` object provides utility functions to explicitly convert JavaScript values (strings or numbers) into JVM primitives. JavaScript numbers are doubles, so use these when a Java method or field needs a specific primitive type.

### Method summary

#### `Primitives.boolean(param: string): boolean`

Converts a JavaScript string into a boolean value. The conversion is case-insensitive (`"true"` becomes `true`, any other value becomes `false`). A boolean is passed through.
List of parameters:

* *param*, the string to convert.

<hr>

#### `Primitives.byte(param: string): byte`

Converts a JavaScript string into a JVM byte. Returns `0` if the input is `null`; a string that is not a number throws an error.
List of parameters:

* *param*, the string to convert.

<hr>

#### `Primitives.short(param: string): short`

Converts a JavaScript string into a JVM short. Returns `0` if the input is `null`; a string that is not a number throws an error.
List of parameters:

* *param*, the string to convert.

<hr>

#### `Primitives.char(param: string): char`

Converts the first character of a JavaScript string into a JVM char. Returns the null character (`'\u0000'`) if the string is empty or `null`.
List of parameters:

* *param*, the string to convert.

<hr>

#### `Primitives.int(param: string): int`

Converts a JavaScript string into a JVM int. Returns `0` if the input is `null`; a string that is not a number throws an error.
List of parameters:

* *param*, the string to convert.

<hr>

#### `Primitives.long(param: string): long`

Converts a JavaScript string into a JVM long. Returns `0` if the input is `null`; a string that is not a number throws an error.
List of parameters:

* *param*, the string to convert.

<hr>

#### `Primitives.float(param: string): float`

Converts a JavaScript string into a JVM float. Returns `0.0F` if the input is `null`; a string that is not a number throws an error.
List of parameters:

* *param*, the string to convert.

<hr>

#### `Primitives.double(param: string): double`

Converts a JavaScript string into a JVM double. Returns `0.0` if the input is `null`; a string that is not a number throws an error.
List of parameters:

* *param*, the string to convert.

<hr>

Every method also accepts a number instead of a string, for example `Primitives.float(0.5)` or `Primitives.int(42)`. `byte`, `short`, `int` and `long` take an optional second argument with the radix used to parse a string, for example `Primitives.int("ff", 16)`.

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce-Addon-ScriptAPI/blob/143f553/src/main/kotlin/net/ccbluex/liquidbounce/script/bindings/api/ScriptPrimitives.kt)*
