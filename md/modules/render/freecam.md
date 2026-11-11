## FreeCam

FreeCam lets your camera leave your body and fly around on its own. Your player stays where it is. Steer the camera with your movement keys, use jump to go up and sneak to go down.

Use it to look around corners or over walls without moving. FreeCam turns off when you change worlds or leave the server. With **CancelOn** you can also make it turn off when you take damage, get teleported, move, or touch water or lava.

With **AllowCameraInteract** on, you can use and hit blocks and entities from where the camera is. **MidClickCameraTeleport** moves the camera to the spot you are looking at when you middle-click. If **Navigation** is on, holding its key (Left Ctrl) makes your player walk to the spot the camera looks at. If you only want to turn the camera around your player, use [FreeLook](/docs/modules/render/freelook).

<video src="/images/modules/freecam/freecam-navigation.mp4" controls width="600">Your browser does not support the video tag.</video>

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Speed | Decimal | 1.0 | 0.1 to 2.0 | How fast the camera flies. |
| CancelOn | Multi-Select | None | Damage, Teleport, Move, Liquid | Turns FreeCam off when one of the picked things happens. |
| AllowCameraInteract | Toggleable Group | On | | Lets you interact with blocks and entities from the camera. |
| AllowCameraInteract → LookAt | Toggle | true | | Turns your player toward what the camera is aiming at when you interact. |
| Navigation | Toggleable Group | Off | | Walks your player to where the camera looks while you hold the key. See [AutoWalk](/docs/modules/shared-settings/autowalk). |
| Navigation → Key | Key | Left Ctrl | | The key to hold so your player walks to the camera's target. |
| MidClickCameraTeleport | Toggle | false | | Middle-click to move the camera to the spot you are looking at. |
| KeepSneaking | Toggle | false | | Keeps your player sneaking while the camera is away. |
| Rotations | Setting Group | | | See [Rotations](/docs/modules/shared-settings/rotations). |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleFreeCam.kt)*
