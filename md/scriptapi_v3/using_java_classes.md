## Using Java classes
As established in the [Getting Started Guide](/docs/Script%20API/Getting%20Started), the [GraalJS](https://github.com/oracle/graaljs) JavaScript engine used by LiquidBounce's script API allows easy interoperation with Java code. Classes from the game and the Java standard library can be imported and used similarly to how you would in Java. This functionality greatly facilitates the development of powerful scripts. Basically anything possible by modifying LiquidBounce's source code can also be done using a script.

### Java.type(className : string): Class
Imports a Java class. <br>
List of parameters:
- className, the fully qualified-name of the class to be imported.

#### Using classes from the Java standard library
```js
const File = Java.type("java.io.File");
const FileUtils = Java.type("org.apache.commons.io.FileUtils");
const StandardCharsets = Java.type("java.nio.charset.StandardCharsets");

// Reads a file and returns its contents.
function readFile(path) {
  const file = new File(path);
  return FileUtils.readFileToString(file, StandardCharsets.ISO_8859_1);
}
```

For more information, please check out the [official GraalJS documentation](https://www.graalvm.org/latest/reference-manual/js/JavaInteroperability/#access-java-from-javascript) on the topic. It provides detailed instructions on how to use this functionality including many examples.


