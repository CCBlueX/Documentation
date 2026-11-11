## AsyncUtil

The `AsyncUtil` class offers a set of utilities for handling asynchronous operations using [Promises](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise) in JavaScript.

Module event handlers (including `enable` and `disable`) and command handlers can be written as [async function](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/async_function), like in the following examples:

```js
mod.on("enable", async () => {
  await AsyncUtil.ticks(1);
  Client.displayChatMessage("Enabled!");
});
```

```js
mod.on("chatReceive", async (event) => {
  const message = event.getMessage();
  await AsyncUtil.ticks(3);
  await AsyncUtil.until(() => mc.player.onGround());
  await AsyncUtil.conditional(20, () => mc.player.onGround());
});
```

**Note:** Promises cannot be cancelled, so any async function that has already started will continue running even if the module is disabled.

Unlike browsers or Node.js, GraalJS does not support web APIs such as [setTimeout](https://developer.mozilla.org/en-US/docs/Web/API/Window/setTimeout), [setInterval](https://developer.mozilla.org/en-US/docs/Web/API/Window/setInterval), or [fetch](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API).

Instead, this utility provides delay and timing functions that work within the game's render thread event loop.

Additionally, AsyncUtil includes support for making HTTP requests using [OkHttp](https://github.com/square/okhttp), which LiquidBounce also uses:

```js
const text = "Guten Tag!";
const sourceLanguage = "de";
const targetLanguage = "en";
/** okhttp3.Response */
const response = await AsyncUtil.request((builder) => {
  builder.url(`https://translate.googleapis.com/translate_a/single?client=gtx&sl=${sourceLanguage}&tl=${targetLanguage}&dt=t&q=${encodeURIComponent(text)}`);
});
const code = response.code(); // No await here!
```

You can also run tasks on another thread with `launch` and wait for their result:

```js
const result = await AsyncUtil.launch(() => {
  java.lang.Thread.sleep(5000);
  return "task result";
});
Client.displayChatMessage(result);
```

### Method Summary

*All methods resolve or reject their Promises on the render thread. AsyncUtil only exists in JavaScript scripts. Pending waits are dropped when scripts are reloaded.*

<hr>

#### `AsyncUtil.ticks(n: int): Promise<int>`

Returns a `Promise` that resolves after `n` game ticks. The resolved value is the number of ticks waited.

**Parameters:**

* `n`: Number of ticks to wait. If `n <= 0`, it immediately resolves with `0`.

<hr>

#### `AsyncUtil.until(condition: () => boolean): Promise<int>`

Returns a `Promise` that resolves when the `condition` function returns `true`. The resolved value is the number of ticks waited.

**Parameters:**

* `condition`: A function that is evaluated every tick. When it returns `true`, the promise resolves.

<hr>

#### `AsyncUtil.conditional(n: int, breakLoop: () => boolean): Promise<int>`

Returns a `Promise` that resolves when either the `breakLoop` function returns `true`, or `n` ticks have passed. Whichever comes first. The resolved value is the number of ticks waited.

**Parameters:**

* `n`: Maximum number of ticks to wait.
* `breakLoop`: A condition function evaluated each tick. If it returns `true`, the promise resolves early.

<hr>

#### `AsyncUtil.request(block: (Request.Builder) => void): Promise<Response>`

Creates a `Promise` that performs an HTTP request and resolves with the resulting [Response](https://github.com/square/okhttp/blob/master/okhttp/src/commonJvmAndroid/kotlin/okhttp3/Response.kt).

**Parameters:**

* `block`: A callback function used to configure the [Request.Builder](https://github.com/square/okhttp/blob/5eecd519aa1a5100fcca08431bfd9c9b85a465a9/okhttp/src/commonJvmAndroid/kotlin/okhttp3/Request.kt).

<hr>

#### `AsyncUtil.launch<T>(executor: Executor, block: () => T): Promise<T>`

Runs a task asynchronously on a given [Executor](https://docs.oracle.com/en/java/javase/21/docs/api/java.base/java/util/concurrent/Executor.html), returning a `Promise` that resolves with the result of the task.

**Parameters:**

* `executor`: *(Optional)* The `Executor` to run the task on. Defaults to Minecraft's background worker pool.
* `block`: A function containing the code to execute asynchronously.

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce-Addon-ScriptAPI/blob/143f553/src/main/kotlin/net/ccbluex/liquidbounce/script/bindings/api/ScriptAsyncUtil.kt)*
