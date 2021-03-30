## Java classes
Since, as mentioned in the [introduction](/docs/ScriptAPI/Getting%20Started), Nashorn is able to access Java classes directly, it is possible to solve most problems with the script API almost exactly as one would do in Java. For this purpose, a method is used that is provided by Nashorn itself. It allows the developer to import any Java classes and use them from within JavaScript. This includes classes from JVM as well as classes from Minecraft. This is very useful because it allows doing almost everything with the script API.

The method used for this is defined on the global variable `Java` and is called `Java.type`.

### Java.type(className)
The Java.type method takes a fully qualified class path as parameter and returns the corresponding Java class. This class can then be instantiated in the same way as in Java or static methods and fields can be accessed directly. <br>
List of arguments:
- className, the fully qualified name of the class to be imported.

Examples:
#### Using built-in classes
```js
var File = Java.type("java.io.File");
var FileUtils = Java.type("org.apache.commons.io.FileUtils");
var StandardCharsets = Java.type("java.nio.charset.StandardCharsets");

// Reads a file and returns its contents.
function readFile(path) {
    var file = new File(path);
    return FileUtils.readFileToString(file, StandardCharsets.ISO_8859_1);
}
```

#### Using Minecraft classes
```js
var C00Handshake = Java.type("net.minecraft.network.handshake.client.C00Handshake");

...

module.on("packet", function(eventData) {
    var packet = eventData.getPacket();

    if (packet instanceof C00Handshake) {
        Chat.print("Cancelling handshake.");
        eventData.cancelEvent();
    }
});
```

For more information on `Java.type`, check out the official Nashorn documentation on the topic [here](https://docs.oracle.com/javase/8/docs/technotes/guides/scripting/nashorn/api.html).
