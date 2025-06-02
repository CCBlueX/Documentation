## Primitives

Minecraft runs on JVM. In JVM, [Primitive types](https://www.w3schools.com/java/java_data_types.asp) are fundamental data types that represent simple values rather than objects.
The JVM supports **8** primitive types: boolean, byte, short, char, int, long, float, and double.

Scripting languages like JavaScript often have broader or dynamically-typed number systems.

> For example, JavaScript represents all numbers as 64-bit floating-point values (`Double` in Java/Kotlin),
which can lead to precision loss or type mismatch issues when interoperating with JVM code.

The ScriptPrimitives util addresses these challenges by providing explicit conversion functions to map script numbers or strings to their corresponding JVM primitive types.

### Available Conversion Methods
The ScriptPrimitives object offers the following methods to convert values to JVM primitives:

#### Boolean Conversions:
- `boolean(boolean: Boolean)`: Identity function for Boolean values.
- `boolean(string: String?)`: Converts a string to a Boolean (e.g., "true" → true).

#### Byte Conversions:
- `byte(byte: Byte)`: Identity function for Byte values.
- `byte(long: Long)`: Converts a Long to a Byte (truncates if out of range).
- `byte(string: String?)`: Converts a string to a Byte (returns 0 if null or invalid).

#### Short Conversions:
- `short(short: Short)`: Identity function for Short values.
- `short(long: Long)`: Converts a Long to a Short (truncates if out of range).
- `short(string: String?)`: Converts a string to a Short (returns 0 if null or invalid).

#### Char Conversions:
- `char(char: Char)`: Identity function for Char values.
- `char(long: Long)`: Converts a Long to a Char via Int truncation.
- `char(string: String?)`: Returns the first character of a string (or '\u0000' if null/empty).

#### Int Conversions:
- `int(int: Int)`: Identity function for Int values.
- `int(long: Long)`: Converts a Long to an Int (truncates if out of range).
- `int(string: String?)`: Converts a string to an Int (returns 0 if null or invalid).

#### Long Conversions:
- `long(long: Long)`: Identity function for Long values.
- `long(string: String?)`: Converts a string to a Long (returns 0L if null or invalid).

#### Float Conversions:
- `float(float: Float)`: Identity function for Float values.
- `float(double: Double)`: Converts a Double to a Float (may lose precision).
- `float(string: String?)`: Converts a string to a Float (returns 0F if null or invalid).

#### Double Conversions:
- `double(double: Double)`: Identity function for Double values.
- `double(string: String?)`: Converts a string to a Double (returns 0.0 if null or invalid).

Each method ensures safe conversion by handling null inputs and providing default values where necessary, making it robust for interoperability scenarios between dynamically-typed scripts and statically-typed JVM languages.
