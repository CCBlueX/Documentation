## ParameterValidator

The ParameterValidator class contains various builtin validation methods for client command parameters. A validation function ensures the given parameter satisfies its requirements and can also perform a parameter transformation. For example, `ParameterValidator.module` ensures the given parameter is the name of an existing module and passes the modules instance to `onExecute` in place of the string provided by the user.

### Method summary

#### `ParameterValidator.string(param: string): ValidationResult`
Does not perform any validation and simply passes param as a string to `onExecute`. This is the default validator. <br>
List of parameters:
- *param*, the parameter to validate.

<hr>

#### `ParameterValidator.module(param: string): ValidationResult`
Ensures *param* is the name of an existing module and passes its instance to `onExecute`. <br>
List of parameters:
- *param*, the parameter to validate.

**Example:**

```js
script.registerCommand({
  name: "description",
  parameters: [{
    name: "module",
    required: true,
    validate: ParameterValidator.module,
  }],
  onExecute(mod) {
    Client.displayChatMessage(`Description of module ${mod.name} is '${mod.description}'`);
  }
});
```

<hr>

#### `ParameterValidator.integer(param: string): ValidationResult`
Ensures *param* is a valid integer and passes the parsed number to `onExecute`. <br>
List of parameters:
- *param*, the parameter to validate.

**Example:**

```js
script.registerCommand({
  name: "addition",
  aliases: ["add"],
  parameters: [{
      name: "a",
      required: true,
      validate: ParameterValidator.integer
    },
    {
      name: "b",
      required: true,
      validate: ParameterValidator.integer
    }
  ],
  onExecute(arg1, arg2) {
    Client.displayChatMessage(`Result of ${arg1} + ${arg2} is ${arg1 + arg2}`);
  }
});
```

<hr>

#### `ParameterValidator.positiveInteger(param: string): ValidationResult`
Ensures *param* is a valid positive integer and passes the parsed number to `onExecute`. <br>
List of parameters:
- *param*, the parameter to validate.