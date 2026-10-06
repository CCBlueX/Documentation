## Primitives

The `Primitives` object provides utility functions to explicitly convert JavaScript values (strings or numbers) into JVM primitives. Since JavaScript represents all numbers as doubles and lacks strict typing, these functions ensure proper and safe interoperation with JVM-based code by enforcing correct primitive types.

### Method summary

#### `Primitives.boolean(param: string): boolean`

Converts a JavaScript string into a boolean value. The conversion is case-insensitive (`"true"` becomes `true`, any other value becomes `false`).
List of parameters:

* *param*, the string to convert.

<hr>

#### `Primitives.byte(param: string): byte`

Converts a JavaScript string into a JVM byte. Returns `0` if parsing fails or if the input is `null`.
List of parameters:

* *param*, the string to convert.

<hr>

#### `Primitives.short(param: string): short`

Converts a JavaScript string into a JVM short. Returns `0` if parsing fails or if the input is `null`.
List of parameters:

* *param*, the string to convert.

<hr>

#### `Primitives.char(param: string): char`

Converts the first character of a JavaScript string into a JVM char. Returns the null character (`'\u0000'`) if the string is empty or `null`.
List of parameters:

* *param*, the string to convert.

<hr>

#### `Primitives.int(param: string): int`

Converts a JavaScript string into a JVM int. Returns `0` if parsing fails or if the input is `null`.
List of parameters:

* *param*, the string to convert.

<hr>

#### `Primitives.long(param: string): long`

Converts a JavaScript string into a JVM long. Returns `0` if parsing fails or if the input is `null`.
List of parameters:

* *param*, the string to convert.

<hr>

#### `Primitives.float(param: string): float`

Converts a JavaScript string into a JVM float. Returns `0.0F` if parsing fails or if the input is `null`.
List of parameters:

* *param*, the string to convert.

<hr>

#### `Primitives.double(param: string): double`

Converts a JavaScript string into a JVM double. Returns `0.0` if parsing fails or if the input is `null`.
List of parameters:

* *param*, the string to convert.

---

If you'd like, I can add usage examples similar to those in the `ParameterValidator` docs.
