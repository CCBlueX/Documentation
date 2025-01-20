# Script Debugging

LiquidBounce supports script debugging using GraalVM's debugging capabilities through either Chrome DevTools Protocol (Inspect) or Debug Adapter Protocol (DAP).

## Debug Command

```
.script debug <name> [protocol] [suspendOnStart] [inspectInternals] [port]
```

Parameters:
- `name`: Script file to debug
- `protocol`: `INSPECT` (Chrome DevTools) or `DAP`
- `suspendOnStart`: Pause execution when debugging begins
- `inspectInternals`: Allow inspection of internal engine state
- `port`: Debug server port number

## Using Chrome DevTools

1. Start debugging:
```
.script debug myscript.js INSPECT true false 9229
```

2. LiquidBounce will provide a DevTools URL in chat. Click it or copy to Chrome:
```
devtools://devtools/bundled/js_app.html?ws=127.0.0.1:9229/myscript.js
```

![Chrome DevTools Interface](/images/script-devtools.png)

## Using Debug Adapter Protocol (DAP)

For IDE integration (like VS Code):

1. Start debugging:
```
.script debug myscript DAP true false 9229
```

2. Configure your IDE to connect to localhost:9229

## Troubleshooting

- "Debug port already in use": Choose a different port
- Connection failed: Verify port availability and firewall settings
- Breakpoints not working: Check if script is properly loaded