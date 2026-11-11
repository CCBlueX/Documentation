## Setting

The Setting class provides methods for creating module settings. See [Creating Modules](/docs/script-api/creating-modules/overview) for how to add them to a module.

### Method summary

#### `Setting.boolean(options: Object): Value`
Creates a new boolean setting (either on or off). <br>
Parameter properties:

| Property | Description                                | Type    |
|----------|--------------------------------------------|---------|
| name     | Name under which the setting is displayed. | string  |
| default  | The setting's initial value.               | boolean |

**Example:**
```js
const fastSwing = Setting.boolean({
    name: "FastSwing",
    default: true
});
fastSwing.value; // true
fastSwing.value = false;
```

<hr>

#### `Setting.float(options: Object): Value`
Creates a new float setting (a floating-point value between *min* and *max*). <br>
Parameter properties:

| Property | Description                                                          | Type     |
|----------|----------------------------------------------------------------------|----------|
| name     | Name under which the setting is displayed.                           | string   |
| default  | The setting's initial value.                                         | number   |
| range    | Array containing the setting's min and max value.                    | number[] |
| suffix   | Displayed next to the current value to describe its unit. (optional) | string   |

**Example:**
```js
const range = Setting.float({
    name: "Range",
    default: 3.0,
    range: [0.5, 8.0],
    suffix: "blocks"
});
range.value; // 3.0
range.value = 2.3;
```

<hr>

#### `Setting.floatRange(options: Object): Value`
Creates a new float setting which has a low and a high value. Intended for choosing values between a set max and min value. <br>
Parameter properties:

| Property | Description                                                          | Type     |
|----------|----------------------------------------------------------------------|----------|
| name     | Name under which the setting is displayed.                           | string   |
| default  | The setting's initial values.                                        | number[] |
| range    | Array containing the setting's min and max value.                    | number[] |
| suffix   | Displayed next to the current value to describe its unit. (optional) | string   |

**Example:**
```js
const randomness = Setting.floatRange({
    name: "Randomness",
    default: [2.3, 7.8],
    range: [0.0, 10.0],
    suffix: "jitter"
});
randomness.value; // [2.3, 7.8]
randomness.value = [2, 4.34];
```

<hr>

#### `Setting.int(options: Object): Value`
Creates a new integer setting (an integer value between *min* and *max*). <br>
Parameter properties:

| Property | Description                                                          | Type     |
|----------|----------------------------------------------------------------------|----------|
| name     | Name under which the setting is displayed.                           | string   |
| default  | The setting's initial value.                                         | number   |
| range    | Array containing the setting's min and max value.                    | number[] |
| suffix   | Displayed next to the current value to describe its unit. (optional) | string   |

**Example:**
```js
const expand = Setting.int({
    name: "Expand",
    default: 4,
    range: [0, 10],
    suffix: "blocks"
});
expand.value; // 4
expand.value = 7;
```

<hr>

#### `Setting.intRange(options: Object): Value`
Creates a new integer setting which has a low and a high value. Intended for choosing values between a set max and min value. <br>
Parameter properties:

| Property | Description                                                          | Type     |
|----------|----------------------------------------------------------------------|----------|
| name     | Name under which the setting is displayed.                           | string   |
| default  | The setting's initial values.                                        | number[] |
| range    | Array containing the setting's min and max value.                    | number[] |
| suffix   | Displayed next to the current value to describe its unit. (optional) | string   |

**Example:**
```js
const cps = Setting.intRange({
    name: "CPS",
    default: [4, 10],
    range: [0, 20],
    suffix: "cps"
});
cps.value; // [4, 10]
cps.value = [5, 12];
```

<hr>

#### `Setting.key(options: Object): Value`
Creates a key value. Keys are given by name, like Minecraft's key names: `"r"`, `"key.keyboard.r"`, `"left.shift"` or `"key.mouse.left"`. Use `"none"` for no key. Reading `value` returns the key object, use `value.getName()` for its name. <br>
Parameter properties:

| Property | Description                                                          | Type     |
|----------|----------------------------------------------------------------------|----------|
| name     | Name under which the setting is displayed.                           | string   |
| default  | The setting's initial key name.                                      | string   |

**Example:**
```js
const key = Setting.key({
    name: "Key",
    default: "r"
});
key.value.getName(); // "key.keyboard.r"
key.value = "g";
```

<hr>

#### `Setting.text(options: Object): Value`
Creates a text value. <br>
Parameter properties:

| Property | Description                                                          | Type     |
|----------|----------------------------------------------------------------------|----------|
| name     | Name under which the setting is displayed.                           | string   |
| default  | The setting's initial value.                                         | string   |

**Example:**
```js
const message = Setting.text({
    name: "Message",
    default: "This is a default message."
});
message.value; // "This is a default message."
message.value = "This is another message";
```

<hr>

#### `Setting.textArray(options: Object): Value`
Creates a list of text values. <br>
Parameter properties:

| Property | Description                                                          | Type     |
|----------|----------------------------------------------------------------------|----------|
| name     | Name under which the setting is displayed.                           | string   |
| default  | The setting's initial values.                                        | string[] |

**Example:**
```js
const messages = Setting.textArray({
    name: "Messages",
    default: ["This is a message", "This is another message"]
});
messages.value; // ["This is a message", "This is another message"]
messages.value = [...messages.value, "This is a third message."];
```

<hr>

#### `Setting.choose(options: Object): Value`
Creates a choose list value (drop down). <br>
Parameter properties:

| Property | Description                                                          | Type     |
|----------|----------------------------------------------------------------------|----------|
| name     | Name under which the setting is displayed.                           | string   |
| default  | The setting's initial value. Must be one of *choices*.               | string   |
| choices  | Possible values.                                                     | string[] |

**Example:**
```js
const animal = Setting.choose({
    name: "Animal",
    default: "Capybara",
    choices: ["Axolotl", "Capybara", "Snek"]
});
animal.value; // Capybara
animal.value = "Axolotl";
```

<hr>

#### `Setting.multiChoose(options: Object): Value`
Creates a list of values the user can turn on and off independently. <br>
Parameter properties:

| Property  | Description                                                          | Type     |
|-----------|----------------------------------------------------------------------|----------|
| name      | Name under which the setting is displayed.                           | string   |
| default   | The values turned on initially. (optional)                           | string[] |
| choices   | Possible values.                                                     | string[] |
| canBeNone | Whether all values may be turned off. Defaults to `true`. (optional) | boolean  |

**Example:**
```js
const targets = Setting.multiChoose({
    name: "Targets",
    default: ["Players"],
    choices: ["Players", "Mobs", "Animals"],
    canBeNone: false
});
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
    fastSwing: Setting.boolean({
      name: "FastSwing",
      default: true
    }),
    range: Setting.float({
      name: "Range",
      default: 3.0,
      range: [0.5, 8.0],
      suffix: "blocks"
    }),
    randomness: Setting.floatRange({
      name: "Randomness",
      default: [2.3, 7.8],
      range: [0.0, 10.0],
      suffix: "jitter"
    }),
    expand: Setting.int({
      name: "Expand",
      default: 4,
      range: [0, 10],
      suffix: "blocks"
    }),
    cps: Setting.intRange({
      name: "CPS",
      default: [4, 10],
      range: [0, 20],
      suffix: "cps"
    }),
    key: Setting.key({
      name: "Key",
      default: "r"
    }),
    message: Setting.text({
      name: "Message",
      default: "This is a default message."
    }),
    messages: Setting.textArray({
      name: "Messages",
      default: ["This is a message", "This is another message"]
    }),
    animal: Setting.choose({
      name: "Animal",
      default: "Capybara",
      choices: ["Axolotl", "Capybara", "Snek"]
    })
  }
}, (mod) => {
  mod.on("enable", () => {
    Client.displayChatMessage(`FastSwing: ${mod.settings.fastSwing.value}`);
    Client.displayChatMessage(`Range: ${mod.settings.range.value}`);
    Client.displayChatMessage(`Randomness: ${mod.settings.randomness.value}`);
    Client.displayChatMessage(`Expand: ${mod.settings.expand.value}`);
    Client.displayChatMessage(`CPS: ${mod.settings.cps.value}`);
    Client.displayChatMessage(`Key: ${mod.settings.key.value.getName()}`);
    Client.displayChatMessage(`Message: ${mod.settings.message.value}`);
    Client.displayChatMessage(`Messages: ${mod.settings.messages.value}`);
    Client.displayChatMessage(`Animal: ${mod.settings.animal.value}`);

    mod.settings.fastSwing.value = false;
    mod.settings.range.value = 2.3;
    mod.settings.randomness.value = [2, 4.34];
    mod.settings.expand.value = 2;
    mod.settings.cps.value = [5, 12];
    mod.settings.key.value = "g";
    mod.settings.message.value = "Axolotls are cool";
    mod.settings.messages.value = ["New message 1", "New message 2"];
    mod.settings.animal.value = "Axolotl";
  });
});
```

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce-Addon-ScriptAPI/blob/143f553/src/main/kotlin/net/ccbluex/liquidbounce/script/bindings/features/ScriptSetting.kt)*
