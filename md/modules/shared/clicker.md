## Clicker

The Clicker settings decide how fast a module clicks for you. Clicks per second (CPS) are clicks in one second. When two modules click the same button, like KillAura and TriggerBot, they share the clicks, so you don't click twice as fast. When you click yourself, your click counts as one of the planned clicks.

The attack cooldown is counted the way the server counts it, so a faster game timer does not let you attack early.

Used by: [KillAura](/docs/modules/combat/killaura), [AutoClicker](/docs/modules/combat/autoclicker), [TriggerBot](/docs/modules/combat/triggerbot), [AutoShoot](/docs/modules/combat/autoshoot), [TpAura](/docs/modules/combat/tpaura), [Scaffold](/docs/modules/world/scaffold), [ProjectilePuncher](/docs/modules/world/projectilepuncher).

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Technique | Choice | Human | Human, Constant | How the time between clicks is picked. Human changes the rhythm like a real hand. Constant clicks at an even pace at the top of the CPS range. |
| CPS | Integer Range | 11..14 | 1..30 clicks | How many clicks per second. Some modules allow more, Scaffold up to 100. |
| MaxPerTick | Integer | 2 | 1..5 clicks | How many clicks can happen in one tick (20 ticks per second). |
| ItemCooldown → Minimum | Decimal Range | 1.0..1.0 | 0.0..2.0 | How charged your attack has to be before clicking. 1.0 is fully charged, higher values wait a bit longer. Only in modules that attack. |
| MissCooldown | Toggle | true | | After you miss, Minecraft makes you wait a moment before you can attack again. This waits for that too. Only for the attack button. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/utils/clicking/Clicker.kt)*
