## AsyncUtil

The AsyncUtil class provides various methods for asynchronous tasks with [Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise) in JavaScript.

All handlers of command an module (including `onEnable` and `onDisable`) can be [async function](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/async_function) like following code:

```js
const onEnable = async () => {
  await AsyncUtil.ticks(1);
  Chat.displayChatMessage("Enabled!");
}
```

```js
module.on("chatReceive", async (event) => {
  const message = event.getMessage();
  await AsyncUtil.ticks(3);
  await AsyncUtil.until(() => mc.player.isOnGround());
  await AsyncUtil.conditional(20, mc.player.isOnGround);
});
```

Note: because `Promise` doesn't support cancellation, the async functions already running won't be cancelled if you disable the module.

Unlike **V8** or **Node**, **GraalJS** doesn't have [setTimeout](https://developer.mozilla.org/en-US/docs/Web/API/Window/setTimeout), [setInterval](https://developer.mozilla.org/en-US/docs/Web/API/Window/setInterval) nor [fetch](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API).
On your browser, they are attached on [window object](https://developer.mozilla.org/en-US/docs/Web/API/Window).
We provide functions for delay using promises and the game's render thread event loop.

This class also contains function for HTTP requests using [OkHttp](https://github.com/square/okhttp), wich is used extensively in this mod:

```js
const test = "Guten Tag!";
const sourceLanguage = "de";
const targetLanguage = "en";
/** okhttp3.Response */
const response = await AsyncUtil.request((builder) => {
  builder.url(`https://translate.googleapis.com/translate_a/single?client=gtx&sl=${sourceLanguage}&tl=${targetLanguage}&dt=t&q=${encodeURIComponent(text)}`);
});
const code = response.code(); // No await here!
```

We also provide function to run tasks on given [ExecutorService](https://docs.oracle.com/javase/8/docs/api/?java/util/concurrent/ExecutorService.html) with coroutine-style result:

```js
const result = await AsyncUtil.launch(() => {
  java.lang.Thread.sleep(5000);
  return "task result";
});
Chat.displayChatMessage(result);
```

### Method summary

*All of these methods resolve or reject the Promise on the render thread.*

#### `AsyncUtil.ticks(n: int): Promise<int>`
Creates a `Promise` which will be resolved after `n` tick(s). Its value equals to `n`. <br>
List of parameters:
- *n*, ticks to wait. If `n <= 0`, it returns `Promise.resolve(0)`.

<hr>

#### `AsyncUtil.until(condition: () => boolean): Promise<int>`
Creates a `Promise` which will be resolved when `condition` returns `true`. Its value is ticks during waiting. <br>
List of parameters:
- *condition*, resolve condition. It will be executed every tick.

<hr>

#### `AsyncUtil.conditional(n: int, breakLoop: () => boolean): Promise<int>`
Creates a `Promise` which will be resolved when `breakLoop` returns `true` or it has passed `n` tick(s). Its value is ticks during waiting. <br>
List of parameters:
- *n*, max ticks to be waited.
- *breakLoop*, resolve condition. It will be executed every tick.

<hr>

#### `AsyncUtil.request(block: (Request.Builder) => void): Promise<Response>`
Creates a `Promise` for HTTP request. Its value is the [Response](https://github.com/square/okhttp/blob/master/okhttp/src/commonJvmAndroid/kotlin/okhttp3/Response.kt). <br>
List of parameters:
- *block*, building callback for [Request.Builder](https://github.com/square/okhttp/blob/5eecd519aa1a5100fcca08431bfd9c9b85a465a9/okhttp/src/commonJvmAndroid/kotlin/okhttp3/Request.kt).

<hr>

#### `AsyncUtil.launch<T>(executor: ExecutorService, block: () => T): Promise<T>`
Creates a `Promise` which will be resolved after async task `block` is finished or failed. Its value is the result of `block`. <br>
List of parameters:
- *executor*, optional, the task will run on it. Defaults to Main worker of Minecraft (on 1.21.x).
- *block*, the task callback.
