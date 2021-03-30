## Using module settings
Often a module must be adapted to different situations. Therefore, in many cases it is highly recommended to add configuration options to the module, which the user can adjust according to his needs. This is done with the help of settings.

### Registering settings with a script module
More information on how to add settings to a script module can be found [here](/docs/ScriptAPI/Creating%20Modules/Overview), more information on how to create a setting [here](/docs/ScriptAPI/Global%20Classes). The following documentation refers to the methods defined on a setting instance.

### Method summary
#### setting.get()
Returns the current value of the setting.

---

#### setting.set(newValue)
Sets the value of the setting to the given one.
List of arguments:
- newValue, the value to set the setting to. Has to be of the correct type.

Example:
```js
module.myBooleanSetting.set(false);
```

#### setting.getName()
Returns the name under which the setting is displayed in the client.
Example:
```js
module.myBooleanSetting.getName(); // "MyBooleanSetting"
```

---

#### setting.getMin()
Returns the smallest possible value the setting can take (only for range settings).

---

#### setting.getMax()
Returns the largest possible value the setting can take (only for range settings).