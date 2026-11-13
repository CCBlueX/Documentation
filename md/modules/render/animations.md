## ViewModel

ViewModel changes how the item in your hand looks on your own screen. You can move, resize and turn the item in each hand, change how fast your arm swings, and pick a different look for swinging and sword blocking. Other players do not see any of this.

BlockingAnimation is used whenever your sword is shown blocking, for example with [SwordBlock](/docs/modules/combat/swordblock) or on a 1.8 server. While a blocking animation is showing, it is used instead of SwingAnimation.

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| MainHand | Toggleable Group | Off | | Changes the item in your main hand. |
| MainHand → ItemScale | Decimal | 0.0 | -5.0..5.0 | Makes the item bigger or smaller. |
| MainHand → X | Decimal | 0.0 | -5.0..5.0 | Moves the item left or right. |
| MainHand → Y | Decimal | 0.0 | -5.0..5.0 | Moves the item up or down. |
| MainHand → PositiveRotationX | Decimal | 0.0 | -50.0..50.0 | Tilts the item forward or back. |
| MainHand → PositiveRotationY | Decimal | 0.0 | -50.0..50.0 | Turns the item left or right. |
| MainHand → PositiveRotationZ | Decimal | 0.0 | -50.0..50.0 | Rolls the item sideways. |
| OffHand | Toggleable Group | Off | | Changes the item in your off hand. |
| OffHand → ItemScale | Decimal | 0.0 | -5.0..5.0 | Makes the item bigger or smaller. |
| OffHand → X | Decimal | 0.0 | -1.0..1.0 | Moves the item left or right. |
| OffHand → Y | Decimal | 0.0 | -1.0..1.0 | Moves the item up or down. |
| OffHand → PositiveRotationX | Decimal | 0.0 | -50.0..50.0 | Tilts the item forward or back. |
| OffHand → PositiveRotationY | Decimal | 0.0 | -50.0..50.0 | Turns the item left or right. |
| OffHand → PositiveRotationZ | Decimal | 0.0 | -50.0..50.0 | Rolls the item sideways. |
| EquipOffset | Toggleable Group | On | | Plays the small raise animation when you switch or use items. |
| EquipOffset → Ignore | Multi-Select | | Blocking, Place, Amount | Skips the raise animation when you block, place a block, or when only the stack size changes. |
| SwingDuration | Toggleable Group | Off | | Changes how long your arm swing takes. |
| SwingDuration → Multiplier | Decimal | 1.0 | 0.1..3.0x | Lower numbers make the swing faster, higher numbers slower. |
| SwingDuration → Ignore | Multi-Select | | Item, Haste, MiningFatigue | These no longer change your swing speed: the held item, Haste, or Mining Fatigue. |
| SwingAnimation | Mode Selector | None | None, Swipe, Spin, Hook, Dash, Tap, Inject, Slap, Akrien, Smooth, Power, Feast | The arm swing you see when you hit. None keeps the normal swing. |
| BlockingAnimation | Mode Selector | 1.7 | None, 1.7, Pushdown, Sigma, Exhibition, Avatar, Dortware | How your sword looks while blocking. None keeps the normal blocking look of the game. |
| BlockingAnimation → [1.7] → Y | Decimal | 0.1 | 0.05..0.3 | Moves the sword up or down while blocking. |
| BlockingAnimation → [1.7] → SwingScale | Decimal | 0.9 | 0.1..1.0 | How much the sword moves when you swing while blocking. |
| BlockingAnimation → [Sigma] → Y | Decimal | 0.1 | 0.05..0.3 | Moves the sword up or down while blocking. |
| BlockingAnimation → [Exhibition] → Y | Decimal | 0.1 | 0.05..0.3 | Moves the sword up or down while blocking. |
| BlockingAnimation → [Avatar] → Y | Decimal | 0.1 | 0.05..0.3 | Moves the sword up or down while blocking. |
| BlockingAnimation → [Dortware] → Y | Decimal | 0.1 | 0.05..0.3 | Moves the sword up or down while blocking. |
| AirWalker | Toggle | false | | Your legs keep their walking animation while you are in the air. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/global/viewmodel/GlobalSettingsViewModel.kt)*
