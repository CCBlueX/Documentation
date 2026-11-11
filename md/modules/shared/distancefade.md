## DistanceFade

DistanceFade makes the boxes and outlines of a module fade out depending on how far away they are. Things very close to you or very far away can slowly disappear, so your screen is less full. With the default values nothing fades.

Used by: [BlockESP](/docs/modules/render/blockesp), [HoleESP](/docs/modules/render/holeesp), [StorageESP](/docs/modules/render/storageesp).

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| NearStart | Decimal | 0.0 | 0.0..512.0 | Things closer than this are hidden, in blocks. |
| NearEnd | Decimal | 0.0 | 0.0..512.0 | Things further than this are fully shown. Between NearStart and NearEnd they fade in. |
| FarStart | Decimal | 512.0 | 0.0..512.0 | Things further than this start to fade out. |
| FarEnd | Decimal | 512.0 | 0.0..512.0 | Things further than this are hidden. |

The four values always stay in this order: NearStart, NearEnd, FarStart, FarEnd. If you move one past another, the other moves along.

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/render/utils/DistanceFadeUniformValueGroup.kt)*
