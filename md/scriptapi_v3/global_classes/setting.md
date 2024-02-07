## Setting

The Setting class provides methods for creating module settings. Refer to [here](#TODO) for information how to integrate them with modules.

### Method summary

#### `Setting.boolean(name: string, default: boolean): Value`
Creates a new boolean setting (either on or off). <br>
List of parameters:
- *name*, name of the setting.
- *default*, default value of the setting.

**Example:**
```js
const fastSwing = Setting.boolean("FastSwing", true);
fastSwing.value; // true
fastSwing.value = false;
```

<hr>

#### `float(name: string, default: float, range: [float], suffix: string = ""): Value`
Creates a new float setting (a floating-point value between *min* and *max*). <br>
List of parameters:
- *name*, name of the setting.
- *default*, default value of the setting.
- *range*, array containing min and max values.
- *suffix*, displayed next to the current value to describe its unit.

**Example:**
```js
const range = Setting.float("Range", 3.0, [0.5, 8.0], "blocks");
range.value; // 3.0
range.value = 2.3;
```

<hr>

#### `Setting.floatRange(name: string, default: [float], range: [float], suffix: String = ""): Value`
Creates a new float setting which has a low and a high value. Intended for choosing values between a set max and min value. <br>
List of parameters:
- *name*, name of the setting.
- *default*, array containing low and high value.
- *range*, array containing min and max values.
- *suffix*, displayed next to the current value to describe its unit.

**Example:**
```js
const randomness = Setting.floatRange("Randomness", [2.3, 7.8], [0.0, 10.0], "jitter");
randomness.value; // [2.3, 7.8]
randomness.value = [2, 4.34];
```

<hr>

#### `Setting.int(name: string, default: int, range: [int], suffix: string = ""): Value`
Creates a new integer setting (an integer value between *min* and *max*). <br>
List of parameters:
- *name*, name of the setting.
- *default*, default value of the setting.
- *range*, array containing min and max values.
- *suffix*, displayed next to the current value to describe its unit.

**Example:**
```js
const expand = Setting.int("Expand", 4, [0, 10], "blocks");
expand.value; // 4
expand.value = 7;
```

<hr>

#### `Setting.intRange(name: string, default: [int], range: [int], suffix: string = "")`
Creates a new integer setting which has a low and a high value. Intended for choosing values between a set max and min value. <br>
List of parameters:
- *name*, name of the setting.
- *default*, array containing low and high value.
- *range*, array containing min and max values.
- *suffix*, displayed next to the current value to describe its unit.

**Example:**
```js
const cps = Setting.intRange("CPS", [4, 10], [0, 20], "cps");
cps.value; // [4, 10]
cps.value = [5, 12];
```

<hr>

#### `Setting.key(name: string, default: int): Value`
Creates a keyboard key value. Refer to the [this gist](https://gist.github.com/Mumfrey/5cfc3b7e14fef91b6fa56470dc05218a) for information on key codes. <br>
List of parameters:
- *name*, name of the setting.
- *default*, default value of the setting (key code).

**Example:**
```js
const bind = Setting.key("Bind", 53); // 53 is slash
bind.value; // 53
bind.value = 54;
```

<hr>

#### `Setting.text(name: String, default: String): Value`
Creates text value. <br>
List of parameters:
- *name*, name of the setting.
- *default*, default value of the setting.

**Example:**
```js
const message = Setting.text("Message", "This is a default message.");
message.value; // "This is a default message."
message.value = "This is another message";
```

<hr>

#### `Setting.textArray(name: string, default: [string]): Value`
Creates text value. <br>
List of parameters:
- *name*, name of the setting.
- *default*, default value of the setting.

**Example:**
```js
const messages = Setting.textArray("Messages", ["This is a message", "This is another message"]);
messages.value; // ["This is a message", "This is another message"]
messages.value = [...message.value, "This is a third message."];
```

### Example script

This script contains all setting types and can be used as a reference.

```js
const script = registerScript({
    name: "MyScript",
    version: "1.0.0",
    authors: ["My Name"]
});

script.registerModule({
    name: "MyModule",
    category: "Misc",
    description: "An example module created with LiquidBounce's script API.",
    settings: {
        fastSwing: Setting.boolean("FastSwing", true),
        range: Setting.float("Range", 3.0, [0.5, 8.0], "blocks"),
        randomness: Setting.floatRange("Randomness", [2.3, 7.8], [0.0, 10.0], "jitter"),
        expand: Setting.int("Expand", 4, [0, 10], "blocks"),
        cps: Setting.intRange("CPS", [5, 10], [0, 20], "cps"),
        bind: Setting.key("Bind", 53),
        message: Setting.text("Message", "This is a default message."),
        messages: Setting.textArray("Messages", ["This is a message", "This is another message"]),
    }
}, (mod) => {
    mod.on("enable", () => {
        Client.displayChatMessage(`FastSwing: ${mod.settings.fastSwing.value}`);
        Client.displayChatMessage(`Range: ${mod.settings.range.value}`);
        Client.displayChatMessage(`Randomness: ${mod.settings.randomness.value}`);
        Client.displayChatMessage(`Expand: ${mod.settings.expand.value}`);
        Client.displayChatMessage(`CPS: ${mod.settings.cps.value}`);
        Client.displayChatMessage(`Bind: ${mod.settings.bind.value}`);
        Client.displayChatMessage(`Message: ${mod.settings.message.value}`);
        Client.displayChatMessage(`Messages: ${mod.settings.messages.value}`);

        mod.settings.fastSwing.value = false;
        mod.settings.range.value = 2.3;
        mod.settings.randomness.value = [2, 4.34];
        mod.settings.expand.value = 2;
        mod.settings.cps.value = [5, 12];
        mod.settings.bind.value = 11;
        mod.settings.message.value = "Axolotls are cool";
        mod.settings.messages.value = ["New message 1", "New message 2"];
    });
});

```