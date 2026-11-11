## Module Commands

These commands give a few modules extra controls that are easier to use from chat.

---

### `.xray`

Chooses which blocks [XRay](/docs/modules/render/xray) shows.

- `.xray add <block>`: adds a block.
- `.xray remove <block>`: removes a block.
- `.xray list [page]`: lists the blocks XRay shows.
- `.xray clear`: removes all blocks.
- `.xray reset`: goes back to the default block list.

```
.xray add diamond_ore
.xray add ancient_debris
.xray remove iron_ore
.xray reset
```

---

### `.autodisable`

Chooses which modules [AutoDisable](/docs/modules/world/autodisable) turns off for you, for example when you die or change worlds.

- `.autodisable add <modules>`: adds one or more modules. Separate them with commas, like `KillAura,Speed`.
- `.autodisable remove <modules>`: removes them again.
- `.autodisable list [page]`: lists the modules on the list.
- `.autodisable clear`: empties the list.

```
.autodisable add KillAura,Speed
.autodisable list
```

---

### `.autoaccount`

Runs [AutoAccount](/docs/modules/misc/autoaccount) by hand, for servers where you have to register and log in with a password.

- `.autoaccount register`: registers you on the server.
- `.autoaccount login`: logs you in.

---

### `.invsee`

Opens another player's inventory so you can look at it. It shows what you can see the player holding and wearing, and what [InventoryTracker](/docs/modules/world/inventorytracker) has seen them use.

```
.invsee <player>
```

```
.invsee Steve
```

---

### `.models`

Trains the AI models that the AI aim smoothing uses to move your aim like a person. The training uses fights you recorded with [DebugRecorder](/docs/modules/misc/debugrecorder) in its Combat or CombatTrainer mode.

- `.models create <name>`: trains a new model. The name may only use letters, numbers and `-`.
- `.models improve <name>`: trains an existing model more with your recordings.
- `.models delete <name>`: deletes a model you made.
- `.models reload`: loads all models again.
- `.models browse`: opens the models folder.

If one of your models has the same name as a model that comes with LiquidBounce, yours is used.

```
.models create my-aim
.models improve my-aim
```

---

*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/command/commands/module)*
