## FreeCam

FreeCam detaches the camera from your character and lets you fly it freely through the world while your player stays exactly where it is. Use it to scout around corners, peek over walls, check what's behind you, or line up a view that your body can't physically reach — all without moving in-game. Steering uses your normal movement keys, with jump and sneak raising and lowering the camera, and the **Speed** setting controls how fast the camera glides.

Because your real position never changes, FreeCam is great for situational awareness, but it can leave you exposed if something happens while you're "away." The **CancelOn** options let it switch itself off automatically when you take damage, get teleported, actually move, or enter liquid, so you snap back to your body when it matters. It also disables itself on world changes so you never get stuck.

With **AllowCameraInteract** turned on you can interact with blocks and entities from the camera's viewpoint — handy for reaching things behind cover, similar to a ghost-hand style reach. **MidClickCameraTeleport** lets you middle-click to jump the camera to whatever it's looking at, and the **Navigation** group can auto-walk the camera toward its aim point while a held key is pressed. For finer control over how aiming behaves while interacting, see the shared [Rotations](/docs/modules/shared-settings/rotations) settings. If you only want to look around without detaching the camera, try [FreeLook](/docs/modules/render/freelook) instead.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Speed | Decimal | 1.0 | 0.1–2.0 | How fast the camera moves when you steer it with your movement keys. |
| CancelOn | Multi-Select | [] | Damage, Teleport, Move, Liquid | Automatically turns FreeCam off when any of the selected events happen, snapping the camera back to your body. |
| MidClickCameraTeleport | Toggle | false | — | Middle-click to teleport the camera to the point it is currently looking at. |
| KeepSneaking | Toggle | false | — | Keeps your character sneaking while the camera is detached. |
| Rotations | Setting Group | — | — | See [Shared: Rotations](/docs/modules/shared-settings/rotations). |
| AllowCameraInteract | Toggleable Group | On | — | Lets you interact with blocks and entities from the camera's perspective, useful for reaching things behind walls or your back. |
| AllowCameraInteract → LookAt | Toggle | true | — | Aims your character at whatever the camera's crosshair is pointing at while interacting. |
| Navigation | Toggleable Group | Off | — | See [Shared: AutoWalk](/docs/modules/shared-settings/autowalk). |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleFreeCam.kt)*
