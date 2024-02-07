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

#### `Setting.float(name: string, default: float, min: float, max: float, suffix: string = ""): Value`
Creates a new float setting (a floating-point value between *min* and *max*). <br>
List of parameters:
- *name*, name of the setting.
- *default*, default value of the setting.
- *min*, lowest value the setting can be set to.
- *max*, highest value the setting can be set to.
- *suffix*, displayed next to the current value to describe its unit.

**Example:**
```js
const range = Setting.float("Range", 3.0, 0.5, 8.0, "blocks");
range.value; // 3.0
range.value = 1.2;
```

#### `Setting.floatRange(name: string, lowDefault: float, highDefault: float, min: float, max: float, suffix: String = ""): Value`
Creates a new float setting which has a low and a high value. Intended for choosing values between a set max and min value. <br>
List of parameters:
- *name*, name of the setting.
- *lowDefault*, default low value of the setting.
- *highDefault*, default high value of the setting.
- *min*, lowest value the setting can be set to.
- *max*, highest value the setting can be set to.
- *suffix*, displayed next to the current value to describe its unit.

**Example:**
```js
const randomness = Setting.floatRange("Randomness", 2.3, 7.8, 0.0, 10.0, "jitter");
randomness.lowValue; // 2.3
randomness.highValue; // 7.8
randomness.lowValue = 4.2;
randomness.highValue = 5.12;
```

#### `Setting.int(name: string, default: int, min: int, max: int, suffix: string = ""): Value`
Creates a new integer setting (an integer value between *min* and *max*). <br>
List of parameters:
- *name*, name of the setting.
- *default*, default value of the setting.
- *min*, lowest value the setting can be set to.
- *max*, highest value the setting can be set to.
- *suffix*, displayed next to the current value to describe its unit.

**Example:**
```js
const expand = Setting.int("Expand", 4, 0, 10, "blocks");
expand.value; // 4
expand.value = 7;
```

#### `Setting.intRange(name: string, lowDefault: int, highDefault: int, min: int, max: int, suffix: String = "")`
Creates a new integer setting which has a low and a high value. Intended for choosing values between a set max and min value. <br>
List of parameters:
- *name*, name of the setting.
- *lowDefault*, default low value of the setting.
- *highDefault*, default high value of the setting.
- *min*, lowest value the setting can be set to.
- *max*, highest value the setting can be set to.
- *suffix*, displayed next to the current value to describe its unit.

**Example:**
```js
const cps = Setting.intRange("CPS", 5, 10, 0, 20, "cps");
cps.lowValue; // 5
cps.highValue; // 10
cps.lowValue = 4;
cps.highValue = 17;
```

#### `Setting.key(name: string, default: int): Value`
Creates a keyboard key value. Refer to the [this gist](https://gist.github.com/Mumfrey/5cfc3b7e14fef91b6fa56470dc05218a) for information on key codes. <br>
List of parameters:
- *name*, name of the setting.
- *default*, default value of the setting (key code).

**Example:**
```js
const bind = Setting.key("Bind", 53); // 53 is slash
bind.value; // true
bind.value = 54;
```

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