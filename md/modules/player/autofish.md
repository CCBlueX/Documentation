## AutoFish

AutoFish fishes for you. Hold a fishing rod and cast it: when a fish bites, AutoFish reels it in and throws the line out again. You can leave it running while you are away, together with [AntiAFK](/docs/modules/player/antiafk).

It listens for the splash sound of your bobber. If a server uses its own sound for a bite, add it to **Sounds**.

**Category:** Player
**Enabled by default:** No

### Settings

Delays are in ticks (20 per second).

| Setting | Type | Default | Range | Description |
| --- | --- | --- | --- | --- |
| ReelDelay | Integer Range | 5..8 | 0..20 ticks | Wait after a bite before reeling in. |
| Sounds | Registry List | Fishing Bobber Splash | | Sounds that mean a fish is biting. |
| SoundDistance | Toggleable Group | On | | Only reacts to sounds close to your own bobber, so other players' fishing doesn't trigger it. |
| SoundDistance → MaxDistance | Decimal | 1.0 blocks | 0.0..10.0 | How close to your bobber the sound must be. |
| RecastRod | Toggleable Group | On | | Throws the line out again after a catch. |
| RecastRod → Delay | Integer Range | 15..20 | 10..30 ticks | Wait before throwing the line out again. |
| AutoCastRod | Toggleable Group | Off | | Throws the line out whenever it isn't in the water, so you don't have to cast the first time. |
| AutoCastRod → Delay | Integer Range | 15..20 | 0..30 ticks | Wait before casting. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/ModuleAutoFish.kt)*
