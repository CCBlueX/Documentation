# Experimental TypeScript Support

> **⚠️ EXPERIMENTAL FEATURE**  
> TypeScript support is currently experimental and unofficial. Use at your own risk! This feature is not endorsed by Mojang or Fabric developers (ofc it is not).

![Experimental TypeScript Support](/images/script-type-support.png)

TypeScript support for LiquidBounce NextGen allows you to write scripts with type checking(not fully working), autocompletion, and better IDE support. This feature provides automatically generated type definitions for Minecraft, LiquidBounce NextGen, and the entire(almost) JVM environment.

## What's Included

- **Generated TypeScript definitions** for Minecraft (with mods), LiquidBounce NextGen, and JVM classes
- **TypeScript augmentations** for proper type hints and manual enhancements
- **Example scripts** written in TypeScript
- **Hot reload support** for development workflow
- **IDE integration** with autocompletion and type checking

## Important Notes

- The generated definitions are primarily designed for **autocompletion** rather than strict type checking
- You may encounter TypeScript compiler errors that don't affect functionality
- Definitions for mods is limited to those present in the LiquidBounce NextGen development environment

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) installed on your system
- Basic knowledge of TypeScript and npm

### Step 1: Setup TypeScript Project

1. Create a new directory for your TypeScript scripts:
```bash
mkdir lb-typescript-scripts
cd lb-typescript-scripts
```

2. Initialize a new Node.js project:
```bash
npm init -y
```

3. Install TypeScript:
```bash
npm install typescript
```

4. Initialize TypeScript configuration:
```bash
npx tsc --init
```

5. Update your `tsconfig.json` to specify source directory:
```json
{
    "compilerOptions": {
        "target": "es2020",
        "module": "commonjs",
        "outDir": "./dist",
        // strongly recommend to turn on these two
        // if you ever need to connect to the debugger
        "inlineSourceMap": true, 
        "inlineSources": true,
        "strict": false,
        "types": ["jvm-types"] 
        // we explicitly acknoledge that we import global ambient types from jvm-types package
    },
    "include": ["src/**/*"]
}
```

Note: we currently only support commonjs for now, esm support will be added in future.

![source-mapping](/images/script-source-mapping-in-debugger.png)
*Working source map, allows you to place breakpoints in typescript source code*

### Step 2: Install Type Definitions

1. Install the type definitions with npm:
```bash
npm install jvm-types
```
The package is a bit large, around 80M decompressed, it might take a while but by my test it worked.

### Step 3: Configure Output Directory (Optional)

For seamless integration with LiquidBounce, configure the output directory to point to your scripts folder:

```json
{
    "compilerOptions": {
        "outDir": "/path/to/.minecraft/LiquidBounce/scripts"
    }
}
```

**Linux users:** You can create a symbolic link instead of modifying `tsconfig.json`:
```bash
ln -s ./dist /path/to/.minecraft/LiquidBounce/scripts
```

### Step 4: Write Your First TypeScript Script

Create a new file `src/minimal.ts`:

```typescript
import { Matrix2d } from "jvm-types/org/joml/Matrix2d";
// your script should have at least 1 single import or export statement to be recognized as a module or the compiler will treat it as a script instead
// you can also use the `export {}` to make it a module if you want it to be clean
// Those embedded definitions like `registerScript` will be automatically imported by the compiler if your .ts file is treated as a module.

const script = registerScript.apply({
    name: "example-minimal",
    version: "1.0.0",
    authors: ["commandblock2"]
});

script.registerModule({
    name: "example-typescript-module-minimal",
    description: "Ths is an minimal example module generated in ts", 
    category: "Client",

}, (mod) => {
    mod.on("enable", () => {
        Client.displayChatMessage(`Hi, ${mc.player}`)
    })
});
```

### Step 5: Compile and Run

1. Compile your TypeScript code:
```bash
npx tsc --watch
```

Note: it is expected that the tsc will flush your console output with a bunch of errors, this is due to our imperfect type definitions, we will fix this in future (might not be so soon though).

2. Your compiled JavaScript files will appear in the `dist` directory (or your configured output directory)
3. Load the scripts in LiquidBounce using `.script reload`

## Hot Reload Development (Optional)

For faster development cycles, you can enable hot reload:

### Setup Hot Reload

1. Install the development dependency:
```bash
npm install minecraft-lbng-types --save-dev
```

2. Start the hot reload watcher:
```bash
npx lb-hotreload-watch path/to/your/dist # default to ./dist if you don't specify

```

3. Copy the hot reloader script to your LiquidBounce scripts directory:
   - Download [hot-reloader.js](https://github.com/commandblock2/minecraft-LBNG-types/blob/master/LBNG-script/hot-reloader.js)
   - Place it in your `.minecraft/LiquidBounce/scripts` directory

4. Enable the hot reloader module (`.t ScriptHotReloader`) in LiquidBounce after running `.script reload`

5. Start modifying your existing scripts - changes will be automatically reloaded!

**Note:** Hot reload currently works with existing scripts only, not newly created ones. It is almost the same with a `.script reload` on your changed script, with the exception that it will presever the debug options for your script.

## Use npm ecosystem packages (partially) (Optional)

1. install your dependencies with `npm install <package>`
    - eg. `npm install typscript`
2. write ts scripts with typescript support
    - eg. 
    ```typescript
    import { SyntaxKind, tokenToString } from 'typescript';


    const script = registerScript.apply({
        name: "node-ecosystem-demo",
        version: "1.0.0",
        authors: ["commandblock2"]
    });

    script.registerModule({
        name: "example-node-ecosystem-demo-module",
        description: "Ths is an minimal example module for the node ecosystem demo",
        category: "Client",

    }, (mod) => {
        mod.on("enable", () => {
            Client.displayChatMessage(`All keywords in ts are ${Array.from({ length: SyntaxKind.LastKeyword - SyntaxKind.FirstKeyword + 1 }, (_, i) => tokenToString(SyntaxKind.FirstKeyword + i)).filter(Boolean)}`)
        })
    })
    ```
3. copy the `node_modules` folder into your LiquidBounce source folder or it's parent folder. (Better to link it with symlink if you are on linux, eg `ln -s path/to/your/development/repo/node_modules/ node_modules`,in liquidbounce script folder or liquidbounce folder)
4. it's going to be slow, this specific script is indeed slow (probably slower than nodejs) and most likely many package that uses node.js api(`assert`, `process`) will fail to load. Currently graaljs does not provide these api, so you might have to use a browserfied version if that package ever has one.  

I discovered this when trying to installing `@types/reserved-keywords` and `reserved-keywords`, but it didn't work because `require('assert')` was on the first line of their package, so I just went use `typescript` instead

## IDE Configuration

### Visual Studio Code

For the best TypeScript experience in VS Code:

1. Install the TypeScript extension (usually included by default)
2. Open your project folder in VS Code
3. Start the TypeScript compiler in watch mode: `npx tsc --watch`
4. Enjoy full autocompletion, type checking, and IntelliSense

### Performance Considerations

The TypeScript language server may occasionally struggle with the large JVM codebase. If you experience issues in vscode, try these steps:

- **Reload the window:** `Ctrl+Shift+P` → "Developer: Reload Window"
- **Restart TypeScript server:** `Ctrl+Shift+P` → "TypeScript: Restart TS Server"

There are also other cases where auto-importing might not be able to list that specific type you are trying to import, in that case you might have to import them manually.

## Common TypeScript Issues

### Type Assignment Errors

You may encounter errors like:
```
Type 'ClientPlayerEntity' is not assignable to type 'LivingEntity'
```

On a snippet like:
```typescript
const entity: LivingEntity = mc.player
```

**Temporary Workaround:** Use type assertions when necessary:
```typescript
const entity: LivingEntity = mc.player as unknown as LivingEntity;
```

### Method Overloading Conflicts

Some Java classes have method overloads that conflict with TypeScript's type system. But the compiled JavaScript will work correctly despite TypeScript errors. (Help needed in generating accurate types for these cases)

### Bean Access Naming

GraalJS bean access may have different naming conventions than the TypeScript definitions.

## Current Limitations

- **Type checking accuracy:** Definitions are optimized for autocompletion over strict type checking
- **Auto importing issues:** IDE might have difficulties in auto-importing classes
- **JVM/TypeScript model differences:** Some Java concepts don't translate perfectly to TypeScript (eg. typescript interfaces has NO static methods but java/kt does)
- **Development environment dependency:** Type definitions must be generated in a development environment
- **No async/await support:** No async/await support in the generated typescript files, it instead just generates Promises


## How this is implemented

### Typescript definition generation
It was generated from forked a ts-generator that orignally only works with field generation. And [the fork](https://github.com/commandblock2/ts-generator) is modified to generate both field and method definitions. It uses kotlin reflection api (mostly) to generate typescript definition files, it also uses java reflection sometimes somwhere to check if the names are actually correct (kotlin reflection sometimes see things differently, like `Unit` for kotlin but `void` for java). So it is expected to generate definitions that are not 100% accurate and it some times fails to process some classes (like java.util.Map), but what it generates should be there on jvm (little bit of false negatives but no false positives observed so far).
I do plan to retire this generator and instead use a graaljs based script for fully accurate definitions in the future (which might have even worse performance, current one is already bad enough).

There is also a part of the definitions is maintained manually, like some of `Settings.boolean` and other things that are presented as `org.graalvm.polyglot.Value` for graaljs (which they are actually js objects, and can be properlly represented as typescript type). These (plus embedded variable/class access like `mc`) are implemented with [typescript declaration merging](https://www.typescriptlang.org/docs/handbook/declaration-merging.html#global-augmentation).

### Modifications on LiquidBounce
Mixins for the `require` function was written to inject calls to the require function, this redirects any `require()` call that starts with `jvm-types/` to `Java.type()` call in graaljs (with a additional step replacing '/' to '.'). Your typescript statement  
`import { HttpServer } from "jvm-types/com/sun/net/httpserver/HttpServer";` will be compiled by vanilla typescript compiler to  
`const HttpServer_1 = require("jvm-types/com/sun/net/httpserver/HttpServer");`,  
where the `require` function will see it starts with `jvm-types/` and instead call  
`Java.type(com.sun.net.httpserver.HttpServer)` and return a object  
`{ HttpServer: Java.type("com.sun.net.http.httpserver.HttpServer") }` which can be used like any other object a `require()` call would return.

If it does not start with the prefix, it just goes on and calls the original require function provided by graaljs.

## Why this, not a custom typescript compiler?
Using a custom typescript compiler would indeed be a much cleaner solution to this problem than embedding a snippet to support js compiled from typescript. We actually tried to use a custom typescript compiler at first, but ultimately we found that this approach turned out to be 
- very slow (`tsc --watch` can almost respond in instant now compared to at least 2 seconds if we use a custom compiler script),
- difficult to maintain. (600 lines of code and transformed more than we would like to)
- source mapping unfriendly (so that you can no longer see the typescript in chromium's debugger, or you can see a mismatched one)

However, if you are experienced and you do know how to make things right with a cleaner solution, please feel free to contribute!

## Getting Help

- **Report issues:** [minecraft-LBNG-types Issues](https://github.com/commandblock2/minecraft-lbng-types/issues)

## Example Scripts

Check out the [LBNG-script directory](https://github.com/commandblock2/minecraft-lbng-types/tree/master/src) in the minecraft-LBNG-types repository for complete example scripts written in TypeScript.

---

> **Remember:** This is an experimental feature. While it greatly enhances the development experience, always test your scripts thoroughly and report any issues you encounter!
