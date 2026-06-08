## BlockBounce

BlockBounce gives you extra upward momentum every time you jump off a bouncy block, letting you launch much higher than vanilla mechanics allow. It's useful on parkour servers, bounce-pad maps, or any time you want to reach ledges and gain height quickly from slime, beds, or honey.

The module hooks into your jump and only activates when you're actually standing on a bouncy surface. It checks the block just beneath your hitbox — using a detection box extended slightly below your feet by 0.01 — and counts it as bouncy if it's a [slime block, bed, or honey block](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/ModuleBlockBounce.kt#L47-L54). When that condition is met, it adds the configured **Motion** value straight onto your jump's vertical motion, so a higher Motion means a higher bounce.

**Category:** Movement
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---------|------|---------|-------|-------------|
| Motion | Decimal | 0.42 | 0.2..2.0 | Extra upward motion added to your jump when standing on a bouncy block (slime, bed, or honey). Higher values bounce you higher. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/ModuleBlockBounce.kt)*
