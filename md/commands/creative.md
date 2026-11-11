## Creative Commands

These commands give you items or change the item in your hand. They only work in Creative mode.

---

### `.give`

Gives you an item.

```
.give <item> [amount]
```

- `item`: the item name, like `diamond_sword` or `golden_apple`.
- `amount`: how many you get, 1 if you leave it out. Bigger amounts fill more than one slot.

```
.give diamond_sword
.give golden_apple 64
```

---

### `.rename`

Renames the item in your hand. You can use color codes with `&`, like `&c` for red.

```
.rename [name]
```

Without a name, the item gets its normal name back.

```
.rename &6Super Sword
.rename
```

---

### `.enchant`

Adds or removes enchantments on the item in your hand.

- `.enchant add <enchantment> [level]`: adds one enchantment.
- `.enchant remove <enchantment>`: removes one enchantment.
- `.enchant clear`: removes all enchantments.
- `.enchant all [level]`: adds every enchantment in the game, even ones that don't fit the item.
- `.enchant all_possible [level]`: adds every enchantment that fits the item.

The level is a number, or `max` for the highest normal level of each enchantment. If you leave it out, you get `max`. A number can go above the normal highest level.

```
.enchant add sharpness
.enchant add protection 4
.enchant remove sharpness
.enchant all_possible max
```

---

### `.skull`

Gives you the head of a player, with their skin.

```
.skull <player>
```

- `player`: the player's name or UUID.

```
.skull Notch
```

---

### `.stack`

Changes how many items are in the stack in your hand.

```
.stack [amount]
```

- `amount`: from 1 to 64. If you leave it out, you get 64.

```
.stack 16
```

---

*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/command/commands/ingame/creative)*
