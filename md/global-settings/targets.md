## Targets

Chooses which players and mobs count as targets. Combat modules like KillAura only attack targets from the Combat list, and visual modules like ESP only show targets from the Visual list.

You can also switch a target on or off with the [`.targets`](/docs/commands/client) command, for example `.targets combat Passive`.

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Combat | Multi-Select | Players, Hostile, Angerable, WaterCreature, Invisible | Players, Hostile, Angerable, WaterCreature, Passive, ArmorStand, Invisible, Dead, Sleeping, Friends | What combat modules attack. |
| Visual | Multi-Select | Players, Hostile, Angerable, WaterCreature, Invisible | Self, Players, Hostile, Angerable, WaterCreature, Passive, ArmorStand, Invisible, Dead, Sleeping, Friends | What visual modules show. |

### What each target means

| Target | Meaning |
|---|---|
| Self | You. Only shown when you look at yourself in third person, FreeCam or FreeLook. Visual only. |
| Players | Other players. |
| Hostile | Mobs that attack you, like zombies and skeletons. |
| Angerable | Mobs that only attack when you make them angry, like wolves and endermen. |
| WaterCreature | Water animals, like fish, squids and dolphins. |
| Passive | Friendly animals and villagers, like cows, pigs and sheep. |
| ArmorStand | Armor stands. |
| Invisible | Lets players and mobs count even while they are invisible. |
| Dead | Lets players and mobs count while they are dying. |
| Sleeping | Lets players count while they sleep in a bed. |
| Friends | Lets players on your friend list count. Without it, your friends are always left alone. |

Combat modules never attack anything outside the world border, because the server would not allow it.

---

*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/global/GlobalSettingsTarget.kt)*
