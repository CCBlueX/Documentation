## TpAura

TpAura teleports you to enemies far away, hits them, and teleports you back. It finds a way around walls and up or down to reach them. While you teleport, you stay where you are on your own screen.

<video src="/images/modules/tpaura/tpaura.mp4" controls width="600">Your browser does not support the video tag.</video>

**Category:** Combat
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Range | Decimal | 30.0 | 6.0..100.0 blocks | How far away an enemy can be. |
| AfterAttack | Choice | Return | Return, Stay | What to do after hitting. Return teleports you back. Stay keeps you at the enemy. |
| Hold | Integer | 10 | 1..40 ticks | With Return: how long to stay at the enemy waiting for a hit before going back, in ticks (20 per second). |
| Target | Setting Group |  | | See [Shared: Target](/docs/modules/shared-settings/target). |
| Clicker | Setting Group |  | | See [Shared: Clicker](/docs/modules/shared-settings/clicker). |
| Rotations | Setting Group |  | | See [Shared: Rotations](/docs/modules/shared-settings/rotations). |
| Steps | Setting Group | | | How the teleport is split into small jumps. |
| Steps → Length | Decimal | 5.0 | 1.0..9.5 blocks | How long each small jump is. |
| Steps → PerTick | Integer | 3 | 1..5 packets | How many small jumps are sent each tick. |
| Render | Toggleable Group | On | | Draws the way TpAura takes. |
| Render → CanBeCovered | Toggle | false | | Lets blocks hide the drawing. |
| Render → Route | Color | | | Color of the way to the enemy. |
| Render → Search | Color | | | Color shown while it looks for a way. |
| Render → Destination | Color | | | Color of the spot you teleport to. |
| Render → Break | Color | | | Color of blocks that would be broken on the way. |
| Render → Place | Color | | | Color of blocks that would be placed on the way. |
| Render → Target | Color | | | Color of the enemy. |
| Render → Invalid | Color | | | Color used when no way was found. |
| Render → Ghost | Toggle | true | | Shows an outline of you where the server thinks you are. |
| Render → FadeOut | Integer | 800 | 0..3000 ms | How long the drawing takes to fade away. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/tpaura/ModuleTpAura.kt)*
