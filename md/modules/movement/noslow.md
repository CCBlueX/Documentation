## NoSlow

NoSlow stops the game from slowing you down while you eat, drink, block with a shield, pull back a bow or sneak. It also works on soul sand, slime, honey, powder snow and in water or lava.

Each kind of slowdown has its own group that you can turn on or off. Some groups have a mode list with bypasses named after anti-cheats (Grim, Intave, AAC). Leave the mode on `None` unless the server you play on needs one. Slowdown while mining is handled by [NoSlowBreak](/docs/modules/world/noslowbreak).

**Category:** Movement
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
| --- | --- | --- | --- | --- |
| Blocking | Toggleable Group | on | | Keeps your speed while blocking with a shield (or a sword on old servers). |
| Blocking → Forward | Decimal | 1.0 | 0.0..1.0 | How much forward and backward speed you keep. 1.0 is full speed. |
| Blocking → Sideways | Decimal | 1.0 | 0.0..1.0 | How much sideways speed you keep. |
| Blocking → OnlySlowOnServerSide | Toggle | false | | Only removes the slowdown when the server thinks you are blocking but your game does not. |
| Blocking → Choice | Mode Selector | None | None, Reuse, Switch, Blink, Interact, Grim-2.3.60, Grim-2.3.64-MC1.8, Grim-2.3.71, InvalidHand, Intave-14.8.4 | Bypass to use while blocking. Blink holds back your movement like [Blink](/docs/modules/player/blink). |
| Blocking → Choice → [Reuse] → Timing | Choice | PreAndPost | PreAndPost, Pre, Post | When in each tick the bypass runs. |
| Blocking → Choice → [Switch] → Timing | Choice | PreAndPost | PreAndPost, Pre, Post | When in each tick the bypass runs. |
| Consume | Toggleable Group | on | | Keeps your speed while eating or drinking. |
| Consume → Forward | Decimal | 1.0 | 0.0..1.0 | How much forward and backward speed you keep. |
| Consume → Sideways | Decimal | 1.0 | 0.0..1.0 | How much sideways speed you keep. |
| Consume → NoBlockInteract | Toggleable Group | on | | Stops clicks on blocks while eating, which some anti-cheats look for. |
| Consume → Mode | Mode Selector | None | None, Grim-2.3.60, Grim-2.3.64-MC1.8, InvalidHand, Grim-2.3.71, Jump, Intave-14.8.4, Release | Bypass to use while eating or drinking. |
| Consume → Mode → [Intave-14.8.4] → Mode | Choice | Release | Release, New | Which version of the Intave bypass to use. |
| Bow | Toggleable Group | on | | Keeps your speed while pulling back a bow, crossbow or trident. |
| Bow → Forward | Decimal | 1.0 | 0.0..1.0 | How much forward and backward speed you keep. |
| Bow → Sideways | Decimal | 1.0 | 0.0..1.0 | How much sideways speed you keep. |
| Bow → Choice | Mode Selector | None | None, Grim-2.3.60, Grim-2.3.64-MC1.8, Grim-2.3.71, InvalidHand | Bypass to use while pulling back. |
| Bow → NoBlockInteract | Toggleable Group | on | | Stops clicks on blocks while pulling back. |
| Bundle | Toggleable Group | on | | Keeps your speed while using a bundle. |
| Bundle → Forward | Decimal | 1.0 | 0.0..1.0 | How much forward and backward speed you keep. |
| Bundle → Sideways | Decimal | 1.0 | 0.0..1.0 | How much sideways speed you keep. |
| Sneaking | Toggleable Group | on | | Makes you walk faster while sneaking. |
| Sneaking → MinMultiplier | Decimal | 1.0 | 0.3..1.0 | Lowest speed you can have while sneaking. 1.0 means no slowdown. |
| Sneaking → Mode | Mode Selector | None | None, Switch, AAC-5 | Bypass for sneaking. Switch and AAC-5 only work on servers older than 1.21.6. |
| Sneaking → Mode → [Switch] → Timing | Choice | PreAndPost | PreAndPost, Pre, Post | When in each tick the bypass runs. |
| Sneaking → Mode → [AAC-5] → Timing | Choice | PreAndPost | PreAndPost, Pre, Post | When in each tick the bypass runs. |
| Soulsand | Toggleable Group | on | | Changes your speed on soul sand. |
| Soulsand → Multiplier | Decimal | 1.0 | 0.4..2.0 | Speed on soul sand. 1.0 is normal speed, higher is faster. |
| SlimeBlock | Toggleable Group | on | | Changes your speed on slime blocks. |
| SlimeBlock → Multiplier | Decimal | 1.0 | 0.4..2.0 | Speed on slime blocks. |
| HoneyBlock | Toggleable Group | on | | Changes your speed on honey blocks. |
| HoneyBlock → Multiplier | Decimal | 1.0 | 0.4..2.0 | Speed on honey blocks. |
| PowderSnow | Toggleable Group | on | | Changes your speed in powder snow. |
| PowderSnow → Multiplier | Decimal | 1.0 | 0.4..2.0 | Speed in powder snow. |
| Fluid | Toggleable Group | on | | Stops water and lava from pushing you around. |
| Fluid → Collision | Toggle | true | | When off, water and lava do not slow you at all. |
| Slowness | Toggleable Group | on | | Weakens the Slowness effect. |
| Slowness → PerLevelMultiplier | Decimal | 0.0 | 0.0..0.15 | How much you slow down per level of Slowness. 0.0 removes it, 0.15 is normal. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/noslow/ModuleNoSlow.kt)*
