## AutoWeapon

AutoWeapon switches to the best weapon in your hotbar when you hit something, then switches back after a while. If the enemy holds up a shield it takes an axe, which breaks through shields. If you are falling and can do a Mace smash attack, it takes your Mace.

**Category:** Combat
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Preferred | Multi-Select | Sword | Any, Sword, Axe, Mace, Spear, Pickaxe, Shovel, Hoe, Knockback, FireAspect | Which kinds of items to switch to. Knockback and FireAspect mean any item with that enchantment. |
| Priority | Choice | Default | Default, Knockback, Damage, AttackSpeed | Which of your preferred items to pick. Default picks the best weapon. Knockback picks the highest Knockback enchantment, Damage the most damage, AttackSpeed the fastest. |
| AutoShieldBreak | Toggle | true | | Switches to an axe when the enemy would block your hit with a shield. |
| AutoMace | Toggle | true | | Switches to a Mace when you can do a smash attack. |
| SwitchBack | Integer | 20 | 1..300 ticks | How long to wait before switching back to your old item, in ticks (20 per second). |
| ChangeOn | Multi-Select | OnAttack | OnAttack, OnTarget | When to switch. OnAttack switches when you hit. OnTarget switches as soon as a module like KillAura picks a target. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/ModuleAutoWeapon.kt)*
