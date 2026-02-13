## BlinkManager

Controls the global packet queueing system used by the Blink module and other features that need to delay outgoing or incoming packets. The BlinkManager intercepts network packets and can hold them in a queue to be released later.

### Settings

```
├── Esp (Mode Selector | default: Wireframe | modes: Box, Model, Wireframe, None)
└── Line (Color | default: LiquidBounce blue)
```

### Settings Details

- **Esp** (Mode Selector) — default: `Wireframe`; modes: `Box`, `Model`, `Wireframe`, `None` — Selects how the server-side player position is visualized while blinking.
  - **Box** — Renders a simple box at the server-side position.
  - **Model** — Renders a full player model at the server-side position.
  - **Wireframe** — Renders a wireframe outline of the player model.
  - **None** — No ESP visualization.
- **Line** (Color) — default: LiquidBounce blue — The color of the line trail drawn between queued movement positions.

### How It Works

The BlinkManager sits between the client and server, intercepting packets in both directions. Modules like Blink and FakeLag use the BlinkManager to:

1. **Queue outgoing packets** — Movement and action packets are held instead of being sent to the server.
2. **Queue incoming packets** — Server packets can also be delayed for certain bypass techniques.
3. **Flush on demand** — Queued packets are released all at once or in batches.

Certain packets are always allowed through (chat messages, status requests), and the queue is automatically flushed on teleport, disconnect, or death to prevent desyncs.

### Related Modules

- [Blink](/docs/Modules/Player/Blink) — Uses BlinkManager to queue all outgoing movement packets.
- [FakeLag](/docs/Modules/Combat/FakeLag) — Uses BlinkManager to simulate lag by delaying packets.
