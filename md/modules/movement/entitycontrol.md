## EntityControl

EntityControl lets you steer rideable mobs — like pigs, striders, or horses — even when they aren't properly equipped. Normally a pig needs a saddle (and a carrot on a stick) before it will respond to your movement keys, and a horse needs to be tamed and saddled before it follows your steering. With this module on, you can take direct control of those entities and ride them around without meeting the usual requirements.

The **Enforce** setting decides which restrictions get bypassed. *Saddled* makes the game treat the mount as if it already has a saddle, so it accepts your steering input. *JumpStrength* unlocks the mount's jump charge so rideable mobs that can leap (such as horses) will actually jump when you hold the jump key. You can enable either or both depending on how much control you want.

This is most useful on servers or in situations where you want to commandeer a mount quickly without gathering the right items first. Pair it with movement modules if you want extra speed once you're riding.

**Category:** Movement
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Enforce | Multi-Select | [Saddled, JumpStrength] | Saddled, JumpStrength | Chooses which riding requirements to bypass: *Saddled* makes mounts respond to steering as though saddled, and *JumpStrength* enables jumping on mounts that support it. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/ModuleEntityControl.kt)*
