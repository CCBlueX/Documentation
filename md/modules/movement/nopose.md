## NoPose

NoPose prevents your client from sending certain entity pose changes that older server versions or anticheat systems do not recognise. Modern Minecraft introduced poses such as swimming (the horizontal sprint-swim pose) and a shorter crouch stance, which can cause issues on servers running older protocol versions — NoPose lets you suppress these on a per-pose basis.

The **NoSwim** toggle stops your player from entering the flat swimming pose when sprinting underwater, keeping you in the standard upright stance instead. The **SneakHeight** option controls which hitbox height is reported while sneaking: `1.8` matches the pre-1.9 standing-height sneak used on very old servers, `1.9` matches the slightly shorter 1.9–1.14 crouch, and `1.15` matches the current vanilla crouch height. Pick whichever value matches what the target server expects.

This module is most useful on servers that run ViaVersion or similar protocol-translation layers, or on anticheat configurations that flag unexpected pose packets. If you are experiencing movement flags or visual glitches related to swimming or crouching, NoPose is a good first thing to enable.

**Category:** Movement
**Enabled by default:** Yes

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| NoSwim | Toggle | true | — | Prevents your player from entering the horizontal swimming pose while sprinting underwater. |
| SneakHeight | Choice | 1.8 | 1.8, 1.9, 1.15 | Sets the hitbox height used while sneaking. Choose the value that matches the protocol version your server expects. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/ModuleNoPose.kt)*
