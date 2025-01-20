# Script Debugging in LiquidBounce

LiquidBounce's script API leverages GraalVM's powerful debugging capabilities to help developers troubleshoot and optimize their scripts. The debugging interface supports two protocols: Chrome DevTools Protocol (Inspect) and Debug Adapter Protocol (DAP), allowing developers to use their preferred debugging tools.

## Using the Debug Command

The script debugging feature can be accessed using the following command:

```
.script debug <name> [protocol] [suspendOnStart] [inspectInternals] [port]
```

### Parameters

- `name`: (Required) The name of the script file to debug
- `protocol`: (Optional) The debugging protocol to use - either `INSPECT` (Chrome DevTools) or `DAP` (Debug Adapter Protocol)
- `suspendOnStart`: (Optional) If true, execution will pause when debugging begins
- `inspectInternals`: (Optional) If true, allows inspection of internal JavaScript engine state
- `port`: (Optional) The port number to use for the debug server

## Debugging with Chrome DevTools

Chrome DevTools provides a familiar and feature-rich debugging environment for JavaScript developers.

### Setting Up Chrome DevTools Debugging

1. Start debugging with the Inspect protocol:
```
.script debug myscript INSPECT true false 9229
```

2. When the command is executed, LiquidBounce will provide a DevTools URL in the chat. It will look something like:
```
devtools://devtools/bundled/js_app.html?ws=127.0.0.1:9229/myscript.js
```

3. Copy this URL and paste it into Chrome's address bar to open the DevTools interface.

### Features Available in Chrome DevTools

- Breakpoint placement and management
- Variable inspection
- Call stack examination
- Live code modification
- Console interaction for real-time script manipulation

## Debugging with Debug Adapter Protocol (DAP)

DAP enables integration with various IDEs and editors that support the protocol, such as Visual Studio Code.

### Setting Up DAP Debugging

1. Start the debug server with DAP protocol:
```
.script debug myscript DAP true false 9229
```

2. Configure your IDE to connect to the debug server:
   - Protocol: Debug Adapter Protocol
   - Host: localhost
   - Port: 9229 (or your specified port)

### IDE Integration

Most modern IDEs support DAP debugging. Here's how to set it up in Visual Studio Code:

1. Create a `.vscode/launch.json` configuration:
```json
{
    "version": "0.2.0",
    "configurations": [
        {
            "type": "graaljs",
            "request": "attach",
            "name": "Attach to LiquidBounce Script",
            "port": 9229
        }
    ]
}
```

2. Use the IDE's debugging interface to:
   - Set breakpoints
   - Step through code
   - Inspect variables
   - Monitor the call stack

## Best Practices

1. **Port Management**
   - Choose an available port that doesn't conflict with other services
   - The default debug port is typically 9229
   - Ensure the port isn't being used by other debugging sessions

2. **Suspend on Start**
   - Use `suspendOnStart` when you need to debug initialization code
   - Be aware that this will pause script execution immediately

3. **Internal Inspection**
   - Only enable `inspectInternals` when needed for deep debugging
   - This option may impact performance

4. **Error Handling**
   - The debugger will provide detailed stack traces for errors
   - Use breakpoints around error-prone code sections
   - Monitor the console for runtime errors

## Troubleshooting

Common issues and their solutions:

1. **Port Already in Use**
   - Error: "Debug port [PORT] already in use"
   - Solution: Choose a different port or close other debugging sessions

2. **Connection Failed**
   - Verify the port is correct and available
   - Check if any firewall rules are blocking the connection
   - Ensure the script is properly loaded before starting debug session

3. **Breakpoints Not Hitting**
   - Verify the source map is properly loaded
   - Check if the script path matches exactly
   - Ensure the breakpoint is set in the correct location

4. **Performance Issues**
   - Disable `inspectInternals` when not needed
   - Remove unnecessary breakpoints
   - Close unused debug sessions

## Example Debugging Session

Here's a complete example of debugging a script:

1. Create a test script (`test.js`):
```javascript
const script = registerScript({
    name: "DebugTest",
    version: "1.0.0",
    authors: ["Developer"]
});

script.registerModule({
    name: "DebugModule",
    category: "Client",
    description: "Testing debug functionality"
}, (mod) => {
    mod.on("enable", () => {
        // Set a breakpoint here
        let x = 10;
        let y = 20;
        Client.displayChatMessage(`Result: ${x + y}`);
    });
});
```

2. Start debugging:
```
.script debug test INSPECT true false 9229
```

3. Open the DevTools URL provided in chat

4. Set breakpoints and begin debugging

This setup allows you to step through the code, inspect variables, and understand the script's execution flow.