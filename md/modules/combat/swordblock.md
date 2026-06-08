## SwordBlock

SwordBlock restores the classic 1.8-style sword blocking mechanic on modern Minecraft servers that use ViaVersion. In Minecraft 1.9 and later, blocking was replaced by the shield system — but many PvP-focused servers run on older combat protocols or use ViaVersion to bridge versions. This module intercepts your right-click action with a sword in hand and redirects it to a blocking packet that the server understands as a block, recreating the damage-reduction behaviour from older versions.

By default the module sends the actual blocking packet to the server so you genuinely reduce incoming damage. If you only want the visual pose without the server-side effect — for example to test animations or on a server where sending the packet would flag anticheat — enable **OnlyVisual**. You can also pair this module with [KillAura](/docs/modules/combat/killaura)'s auto-block feature; SwordBlock handles the visual side of that interaction as well.

The shield-hiding options let you keep the classic look consistent: if you carry a shield in your offhand, it would normally be visible and conflict with the sword-blocking animation. **HideShieldSlot** suppresses it while you're holding a sword, and **AlwaysHideShield** extends that to all situations.

**Category:** Combat
**Enabled by default:** Yes

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| OnlyVisual | Toggle | false | — | When enabled, only plays the sword-blocking animation client-side without sending any blocking packet to the server. |
| FakeOnPressing | Toggle | false | — | Shows the sword-blocking animation whenever you hold the use key, even if no actual block action is in progress. |
| HideShieldSlot | Toggle | false | — | Hides the shield in your offhand slot visually while you are holding a sword, keeping the classic 1.8 look. |
| ApplyToThirdPersonView | Toggle | true | — | Applies the sword-blocking animation when viewed in third-person perspective. |
| AlwaysHideShield | Toggle | false | — | Hides the offhand shield at all times, regardless of what is in your main hand. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/ModuleSwordBlock.kt)*
