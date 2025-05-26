# Experimental TypeScript Support

> **⚠️ EXPERIMENTAL FEATURE**  
> TypeScript support is currently experimental and unofficial. Use at your own risk! This feature is not endorsed by Mojang or Fabric developers.

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
        "strict": false
    },
    "include": ["src/**/*"]
}
```

![source-mapping](/images/script-source-mapping-in-debugger.png)
*Working source map, allows you to place breakpoints in typescript source code*

### Step 2: Install Type Definitions

1. Visit the [minecraft-LBNG-types GitHub Actions page](https://github.com/commandblock2/minecraft-LBNG-types/actions)
2. Download the latest `jvm-types` artifact
3. Extract the downloaded zip file to a directory (e.g., `./jvm-types`)
4. Install the type definitions:
```bash
npm install file:./jvm-types --no-save
```

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

2. Your compiled JavaScript files will appear in the `dist` directory (or your configured output directory)
3. Load the scripts in LiquidBounce using `.script reload`

## Hot Reload Development

For faster development cycles, you can enable hot reload:

### Setup Hot Reload

1. Install the development dependency:
```bash
npm install minecraft-lbng-types --save-dev
```

2. Start the hot reload watcher:
```bash
npx lb-hotreload-watch
```

3. Copy the hot reloader script to your LiquidBounce scripts directory:
   - Download [hot-reloader.js](https://github.com/commandblock2/minecraft-LBNG-types/blob/master/LBNG-script/hot-reloader.js)
   - Place it in your `.minecraft/LiquidBounce/scripts` directory

4. Enable the hot reloader module (`.t ScriptHotReloader`) in LiquidBounce after running `.script reload`

5. Start modifying your existing scripts - changes will be automatically reloaded!

**Note:** Hot reload currently works with existing scripts only, not newly created ones. It is almost the same with a `.script reload` on your changed script, with the exception that it will presever the debug options for your script.

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
- **Large codebase performance:** May cause IDE performance issues
- **JVM/TypeScript model differences:** Some Java concepts don't translate perfectly to TypeScript
- **Development environment dependency:** Type definitions must be generated in a development environment

## Getting Help

- **Report issues:** [minecraft-LBNG-types Issues](https://github.com/commandblock2/minecraft-lbng-types/issues)

## Example Scripts

Check out the [LBNG-script directory](https://github.com/commandblock2/minecraft-lbng-types/tree/master/src) in the minecraft-LBNG-types repository for complete example scripts written in TypeScript.

---

> **Remember:** This is an experimental feature. While it greatly enhances the development experience, always test your scripts thoroughly and report any issues you encounter!
