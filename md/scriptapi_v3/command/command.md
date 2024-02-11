## Creating Commands

Commands created using the script API behave exactly like builtin commands. In contrast to modules, commands are intended to perform one well-defined action once when they are executed.

### Registering a command

Just like modules, commands have to be registered with the client. This must be done by calling `registerCommand` on your script's instance passing an object containing various options.
```js
script.registerCommand({ option: value });
```

The object passed to `registerCommand` may contain the following options:

| Propery     | Description                                                                 | Required | Type     | Default |
|-------------|-----------------------------------------------------------------------------|----------|----------|---------|
| name        | Primary name of the command.                                                | Yes      | string   |         |
| onExecute   | Function called when the command is executed.                               | Yes      | function |         |
| aliases     | Array containing additional names of the command.                           | No       | array    | []      |
| parameters  | Array containing parameters of the command. Refer to 'Creating parameters'. | No       | array    | []      |
| hub         | Whether this command is a hub command. Hub commands cannot be executed.     | No       | boolean  | false   |
| subcommands | Array containing additional subcommands.                                    | No       | array    | []      |

### Creating parameters

Parameters accept arguments passed in by the user. By default, no validation is performed. Arguments given by the user will be passed to `onExecute` as strings. 

Parameters are created as JavaScript objects and may have the following options:

| Propery        | Description                                                                                      | Required | Type     | Default |
|----------------|--------------------------------------------------------------------------------------------------|----------|----------|---------|
| name           | Name of the parameter.                                                                           | Yes      | string   |         |
| required       | Whether the parameter is required or optional.                                                   | No       | boolean  | false   |
| vararg         | Whether this parameter accept a variable amount of arguments. Only possible with last parameter. | No       | boolean  | false   |
| getCompletions | Function returning completion candidates for partial input.                                      | No       | function |         |
| validate       | Function validating the parameter and possibly applying transformations.                         | No       | function |         |

### Using validators

Validators may be used to ensure an argument provided by the user is of the expected format. They may also be used to perform a parameter transformation substituting the string argument with one that has been processed in some way. To enable parameter validation, set a `validate` function in a parameter's options.

#### Using builtin validators

LiquidBounce's script API provides a set of builtin validators for common use cases. For more information on builtin validators, click [here](#TODO).

**Example:** Command using the built-in *module* validator.
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


#### Writing custom validators

Validators are functions that accept an argument given by the user and validate its integrity. They may also subsitute it with a processed value which will be passed to `onExecute` instead.

Writing a custom validator involves creating a function which accepts the raw string argument as a parameter and returns an object indicating whether the argument has been accepted and either a subsitution value or an error message to display.

If the argument has been accepted, an object of the following structure has to be returned:
```js
{
  accept: true,
  value: processedArgument
}
```

If the argument has been rejected, an object of the following structure has to be returned instead:
```js

{
  accept: false,
  error: "Argument did not fulfill expected criteria"
}
```

**Example:** Implementing an integer validator. Note that the script API offers a built-in validator for this purpose. See [here](#Todo).

```js
script.registerCommand({
  name: "integer",
  parameters: [{
    name: "value",
    required: true,
    validate(arg) {
      const integerRegex = /^-?\d+$/;
      if (integerRegex.test(arg)) {
        return {
          accept: true,
          value: parseInt(arg),
        };
      } else {
        return {
          accept: false,
          error: `'${arg}' is not a valid integer`
        };
      }
    }
  }],
  onExecute(integer) {
    Client.displayChatMessage(`typeof ${integer} is ${typeof integer}`);
  }
});
```

### Using auto completion

Command parameters support tab autocomplete when implemented. To do so, `getCompletions` has a to specified. It expects a function accepting two parameters, the partial input for the current parameter (what the user has entered so far) and an array containing all parameters accepted so far, and returns an array of completion candidates.

**Example:** A command accepting only *Axolotl*, *Capbybara*, and *Snek* as its first parameter.

```js
const acceptedAnimals = ["Axolotl", "Capybara", "Snek"];
script.registerCommand({
  name: "animal",
  parameters: [{
    name: "value",
    required: true,
    validate(arg) {
      if (acceptedAnimals.includes(arg)) {
        return {
          accept: true,
          value: arg,
        };
      } else {
        return {
          accept: false,
          error: `Only the following animals are acceptable: ${acceptedAnimals.join(", ")}`,
        };
      }
    },
    getCompletions(begin, args) {
      return acceptedAnimals.filter(a => a.startsWith(begin));
    }
  }],
  onExecute(animal) {
    Client.displayChatMessage(`Petting the ${animal}`);
  }
});
```

### Complex example

The following example command uses all supported API features. It may be used as a reference when developing.

```js
const acceptedAnimals = ["Axolotl", "Capybara", "Snek"];
script.registerCommand({
  name: "myCommand",
  aliases: ["exampleCommand", "sampleCMD"], // .exampleCommand and .sampleCommand will both work to execute this command.
  hub: true, // .myCommand is not executable directly. It only serves a hub holding subcommands.
  subcommands: [{
      name: "math",
      hub: true,
      subcommands: [{
          name: "div",
          aliases: ["divide"],
          parameters: [{
              name: "x",
              required: true,
              validate: ParameterValidator.integer
            },
            {
              name: "y",
              required: true,
              validate: ParameterValidator.integer
            }
          ],
          onExecute(x, y) {
            Client.displayChatMessage(`${x} divided by ${y} is ${x / y}`);
          }
        },
        {
          name: "sqrt",
          parameters: [{
            name: "x",
            required: true,
            validate: ParameterValidator.positiveInteger
          }],
          onExecute(x) {
            Client.displayChatMessage(`Square root of ${x} is ${Math.sqrt(x)}`);
          }
        },
        {
          name: "sum",
          parameters: [{
            name: "numbers",
            required: true,
            vararg: true,
            validate: ParameterValidator.integer
          }],
          onExecute(args) {
            Client.displayChatMessage(`Sum ${args.join(" + ")} is ${args.reduce((s, a) => s + a, 0)}`);
          }
        }
      ]
    },
    {
      name: "animal",
      parameters: [{
        name: "value",
        required: true,
        validate(arg) {
          if (acceptedAnimals.includes(arg)) {
            return {
              accept: true,
              value: arg,
            };
          } else {
            return {
              accept: false,
              error: `Only the following animals are acceptable: ${acceptedAnimals.join(", ")}`,
            };
          }
        },
        getCompletions(begin, args) {
          return acceptedAnimals.filter(a => a.startsWith(begin));
        }
      }],
      onExecute(animal) {
        Client.displayChatMessage(`Petting the ${animal}`);
      }
    }
  ]
});
```