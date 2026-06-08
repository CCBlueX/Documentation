## DistanceFade

DistanceFade controls how the visuals from a module gently fade in and out based on how far away things are from you. Instead of every box or outline showing at the exact same strength no matter where it is, this group lets you make distant objects (or very close ones) fade away smoothly, so your view stays cleaner and only the things you care about stand out.

It works with two fade zones. The **near** zone fades things in as they move away from you — anything closer than the near range can be faded out, which is handy for clearing clutter right in front of your face. The **far** zone fades things out as they get farther away, so distant objects gradually disappear instead of cluttering the horizon. Between the two fully-visible points, the visuals show at full strength. By default the near values are both `0` and the far values are both `512`, which effectively turns fading off and shows everything at full strength out to the maximum range.

The four values always stay in a sensible order — your near start can't pass your near end, and the far start can't drop below the near end or above the far end — so the fade never overlaps or flips itself the wrong way around.

This setting group is used by the following modules:

- [BlockESP](/docs/modules/render/blockesp)
- [StorageESP](/docs/modules/render/storageesp)

### Settings

| Setting | Type | Default | Range | Description |
| --- | --- | --- | --- | --- |
| NearStart | Decimal | 0.0 | 0.0..512.0 | Distance (in blocks) at which the near fade begins — objects closer than this are fully faded out, fading in as they reach NearEnd. |
| NearEnd | Decimal | 0.0 | 0.0..512.0 | Distance at which the near fade finishes, so objects at or beyond this point are fully visible. |
| FarStart | Decimal | 512.0 | 0.0..512.0 | Distance at which the far fade begins — objects stay fully visible up to here, then start fading out. |
| FarEnd | Decimal | 512.0 | 0.0..512.0 | Distance at which the far fade finishes, so objects farther than this are fully faded out. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/render/utils/DistanceFadeUniformValueGroup.kt)*
