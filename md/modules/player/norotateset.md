## NoRotateSet

NoRotateSet keeps the server from turning your view. When the server sets where you look, for example after a teleport, your camera stays where it was.

SilentAccept tells the server you accepted its new direction while your camera does not move. ResetRotation also keeps your camera, then turns you back smoothly for the server using its Rotations settings.

**Category:** Player
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | SilentAccept | SilentAccept, ResetRotation | How forced turns from the server are handled. |
| Mode → ResetRotation → Rotations | Setting Group | | | See [Rotations](/docs/modules/shared-settings/rotations). |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/ModuleNoRotateSet.kt)*
