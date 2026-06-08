## AutoWeapon

AutoWeapon scans your hotbar and silently swaps to the best weapon for the situation right before you hit something, so you don't have to manually juggle slots mid-fight. By default it favors a sword, but it can also react to what your opponent is doing: if a target raises a shield it will reach for an axe to stun them, and if a mace smash is available it will switch to your mace to land the falling-damage bonus. After the hit it switches back to your original slot, keeping the swap invisible to your normal gameplay.

The core of the logic is in [`determineWeaponSlot`](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/ModuleAutoWeapon.kt#L171-L192): it filters your hotbar to weapons, then picks the strongest one for the current case — mace when a smash is possible, axe when the target would block with a shield, otherwise the highest-scoring weapon of your preferred type. The swap itself is performed silently and reverted after the configured number of ticks via [the attack handler](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/ModuleAutoWeapon.kt#L129-L148).

AutoWeapon yields to other actions: if AutoBuff is using your slot or you're eating/drinking a consumable in your main hand, it stays out of the way ([isBusy](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/ModuleAutoWeapon.kt#L84-L89)). You can leave the preferred list empty if you only want the AutoShieldBreak or AutoMace reactions without forcing a normal weapon switch.

**Category:** Combat
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Preferred | Multi-Select | [Sword] | Any, Sword, Axe, Mace, Spear, Pickaxe, Shovel, Hoe, Knockback, FireAspect | Weapon type(s) to switch to when no special case (shield or mace smash) applies. Leave empty to disable normal switching and rely only on AutoShieldBreak / AutoMace. |
| AutoShieldBreak | Toggle | true | — | When the target would block your hit with a shield, switch to an axe instead, since an axe stuns shield users. |
| AutoMace | Toggle | true | — | When a mace smash attack is available (e.g. falling), switch to a mace, whose smash cannot be blocked by a shield. |
| SwitchBack | Integer | 20 | 1..300 | Ticks to wait after the swap before silently switching back to your original slot. |
| ChangeOn | Multi-Select | [OnAttack] | OnAttack, OnTarget | When to perform the swap: OnAttack switches as you attack an entity; OnTarget switches as soon as a target is selected. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/ModuleAutoWeapon.kt)*
