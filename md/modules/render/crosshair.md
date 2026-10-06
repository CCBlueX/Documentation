## Crosshair

Crosshair replaces Minecraft's default crosshair with a custom-drawn one, giving you more control over how the center of your screen looks. Pick between a circular reticle or a CS2-style four-line cross, and tune the size, color, and animation to taste.

Both styles can react to your attack cooldown: as your weapon recharges after a swing, the crosshair temporarily expands and then snaps back as it becomes ready, giving you a quick visual cue for timing your hits. The crosshair hides automatically while you have an inventory or container screen open, and you can choose whether it stays visible in third-person view.

Since this is purely a visual overlay, it works alongside any combat module and is a good companion to setups using modules like [KillAura](/docs/modules/combat/killaura) or [AutoClicker](/docs/modules/combat/autoclicker) where clean hit feedback matters.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | Circle | Circle, CS2 | Chooses the overall crosshair style. |
| Mode → Circle → ShowInThirdPerson | Toggle | true | — | Keeps the crosshair visible while in third-person view. |
| Mode → Circle → Radius | Setting Group | — | — | Controls the size of the circular reticle. |
| Mode → Circle → Radius → Range | Decimal Range | 3.0..5.0 | 0.0..25.0 | Inner and outer radius of the ring; the gap between them sets its thickness. |
| Mode → Circle → Radius → DynamicRadiusMultiplier | Decimal | 1.0 | 0.0..5.0 | How much the ring expands right after an attack while your cooldown recharges. Set to 0 for a fixed size. |
| Mode → Circle → Color | Setting Group | — | — | Color and animation of the circle. |
| Mode → Circle → Color → Sync | Toggle | true | — | Uses only the first color; turn off to blend between the first and second colors. |
| Mode → Circle → Color → FirstColor | Color | — | — | Primary crosshair color. |
| Mode → Circle → Color → SecondColor | Color | — | — | Secondary color used when Sync is off. |
| Mode → Circle → Color → SpinSpeed | Decimal | 4.0 | -10.0..10.0 | Speed of the color animation; negative values reverse the direction, 0 keeps it static. |
| Mode → CS2 → ShowInThirdPerson | Toggle | true | — | Keeps the crosshair visible while in third-person view. |
| Mode → CS2 → Crosshair | Setting Group | — | — | Shape of the four-line cross. |
| Mode → CS2 → Crosshair → Length | Decimal | 5.0 | 1.0..20.0 | Length of each of the four lines. |
| Mode → CS2 → Crosshair → Thickness | Decimal | 1.0 | 0.5..5.0 | Width of each line. |
| Mode → CS2 → Crosshair → Gap | Decimal | 2.0 | 0.0..10.0 | Empty space between the center and the start of each line. |
| Mode → CS2 → Crosshair → DynamicMultiplier | Decimal | 1.0 | 0.0..10.0 | How much the gap widens right after an attack while your cooldown recharges. Set to 0 for a fixed gap. |
| Mode → CS2 → Color | Setting Group | — | — | Color and animation of the cross. |
| Mode → CS2 → Color → Sync | Toggle | true | — | Uses only the first color; turn off to blend between the first and second colors. |
| Mode → CS2 → Color → FirstColor | Color | — | — | Primary crosshair color. |
| Mode → CS2 → Color → SecondColor | Color | — | — | Secondary color used when Sync is off. |
| Mode → CS2 → Color → SpinSpeed | Decimal | 4.0 | -10.0..10.0 | Speed of the color animation; negative values reverse the direction, 0 keeps it static. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/crosshair/ModuleCrosshair.kt)*
