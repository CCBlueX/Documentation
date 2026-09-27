## Creating Commands

Client commands are [Brigadier](https://github.com/Mojang/brigadier) commands, the same library Minecraft uses for its own. They are typed into the chat with the client's prefix (`.` by default) and are never sent to the server.

### Registering a command

A command is a `CommandRegistrar`, which adds its literal to the dispatcher it is given. The source type is `ClientCommandSource`.

```kotlin
object CommandGreet : CommandRegistrar {

    override fun register(dispatcher: CommandDispatcher<ClientCommandSource>) {
        dispatcher.register("greet", aliases = listOf("hi")) {
            exec {
                chat("Hello!")
                1
            }

            argument("name", StringArgumentType.word(), suggests = onlinePlayers()) { name ->
                optional("times", IntegerArgumentType.integer(1, 5), default = 1) { times ->
                    exec { ctx ->
                        repeat(ctx.get(times)) {
                            chat(regular("Hello, ").append(variable(ctx.get(name))))
                        }
                        1
                    }
                }
            }

            literal("server") {
                requires { it.isIngame }

                argument("greeting", StringArgumentType.word(), suggests = suggestions("Hi", "Hello", "Hey")) { greeting ->
                    exec { ctx ->
                        ClientCommandSource.playerOrNull?.connection?.sendChat(ctx.get(greeting))
                        1
                    }
                }
            }
        }
    }

}
```

This accepts `.greet`, `.greet Steve`, `.greet Steve 3`, `.greet server Hello` and the same with `.hi`. Register it from the add-on's `onInitialize()`:

```kotlin
registerCommand(CommandGreet)
```

Command names are unique regardless of case, and registering a taken one fails the add-on. `CommandManager.isRootTaken(name)` checks first. `CommandManager.execute("greet Steve 2")` runs a command from code, without the prefix.

### Kotlin DSL

`dispatcher.register(name, aliases) { ... }` builds the command with the client's Kotlin DSL:

| Function                                        | Description                                                                                          |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------|
| `literal(name, aliases) { ... }`                | A subcommand.                                                                                        |
| `argument(name, type, suggests) { arg -> ... }` | A required argument of a Brigadier `ArgumentType`. The block continues the chain after it.           |
| `optional(name, type, default, suggests) { arg -> ... }` | An optional argument. `default` is used when it is left out, `null` if none is given. Every argument after it must be optional too. |
| `exec { ctx -> result }`                        | What runs when the input ends here. Returns an `Int`, 1 for success.                                 |
| `execSuspend { ctx -> }`                        | The same as a `suspend` function. The client shows a progress message and, unless `allowParallel` is set, refuses to start the command again before it finished. |
| `requires { source -> allowed }`                | Hides and blocks the literal while the condition is false, for example `it.isIngame`.                |
| `ctx.get(arg)`                                  | Reads the value of an argument, typed.                                                               |
| `t(key, args)`                                  | The translation of `liquidbounce.command.<command>.<key>`.                                          |

A greedy argument, such as `StringArgumentType.greedyString()`, has to be the last in its chain.

`ClientCommandSource` has `playerOrNull`, `levelOrNull` and `isIngame` for commands that need a world.

### Suggestions

`suggests` takes a Brigadier `SuggestionProvider`. The client has a few ready-made ones:

| Function                              | Suggests                                               |
|---------------------------------------|--------------------------------------------------------|
| `suggestions("a", "b")`               | The given strings.                                     |
| `suggestions(iterable)`               | The strings of a collection.                           |
| `suggestions { iterable }`            | Strings computed when the player types.                |
| `onlinePlayers()`                     | The names in the tab list.                             |

### Descriptions and errors

`.help` shows the translation of `liquidbounce.command.<command>.description`, see [Translations](/docs/add-on-api/translations).

An exception thrown by a command typed into the chat is shown there in red. `CommandException(text)` shows just `text`, any other exception its class name and message as well.

### Plain Brigadier

The DSL is optional. Any Brigadier builder with `ClientCommandSource` as source works, which is also how commands are written in [Java](/docs/add-on-api/using-java):

```java
public class CommandHello implements CommandRegistrar {

    @Override
    public void register(CommandDispatcher<ClientCommandSource> dispatcher) {
        dispatcher.register(LiteralArgumentBuilder.<ClientCommandSource>literal("hello")
            .executes(context -> {
                ClientChat.chat("Hello!");
                return 1;
            })
            .then(RequiredArgumentBuilder.<ClientCommandSource, String>argument("name", StringArgumentType.word())
                .executes(context -> {
                    String name = StringArgumentType.getString(context, "name");
                    ClientChat.chat(ClientChat.regular("Hello, ").append(ClientChat.variable(name)));
                    return 1;
                })));
    }

}
```
