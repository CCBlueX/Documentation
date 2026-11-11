## AutoWalk

These settings control how a module walks you somewhere by itself. It finds a way to the goal and walks, jumps, swims or even flies there for you. When there is no goal, you stop.

Used by: [KillAura](/docs/modules/combat/killaura) (FightBot), [FreeCam](/docs/modules/render/freecam) (Navigation), [AutoFarm](/docs/modules/world/autofarm), [Fucker](/docs/modules/world/fucker).

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| AllowBreak | Toggle | depends on the module | | May break blocks that are in the way. On in FreeCam and Fucker, off in the others. |
| AllowPlace | Toggle | depends on the module | | May place blocks from your hotbar to build a way. On in FreeCam and Fucker, off in the others. |
| AllowParkour | Toggle | true | | May jump over gaps. |
| RiskyJumps | Toggle | false | | Also tries jumps that can go wrong. Only with AllowParkour. |
| MaxFall | Integer | 3 | 0..20 blocks | How far you may drop down. Feather Falling and similar effects add to this. |
| PathRange | Integer | 64 | 16..128 blocks | How long a way it looks for at most. |
| AllowFly | Toggle | true | | May fly when you are able to, for example in creative mode. |
| AllowElytra | Toggle | true | | May glide with an elytra you are wearing. |
| ElytraRockets | Toggle | true | | May use firework rockets while gliding. |
| Render | Toggleable Group | depends on the module | | Draws the way it is walking. Off for KillAura's FightBot, on for the others. |
| Render → CanBeCovered | Toggle | false | | Lets blocks hide the drawing. |
| Render → Route | Color | | | Color of the way. |
| Render → Search | Color | | | Color shown while it looks for a way. |
| Render → Destination | Color | | | Color of the goal. |
| Render → Break | Color | | | Color of blocks it will break. |
| Render → Place | Color | | | Color of blocks it will place. |
| Render → Target | Color | | | Color of the target. |
| Render → Invalid | Color | | | Color used when no way was found. |
| Render → Ghost | Toggle | true | | Shows an outline of you where the server thinks you are. |
| Render → FadeOut | Integer | 800 | 0..3000 ms | How long the drawing takes to fade away. |

The modules add their own settings to this group, for example AutoFarm's ToPlant and ToItems. Those are explained on the module's page.

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/utils/navigation/walk/WalkSettings.kt)*
