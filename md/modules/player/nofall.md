## NoFall

NoFall prevents fall damage automatically whenever you land from a height that would normally hurt you. The module is inactive in Creative and Spectator mode, while flying, or while invulnerable, since those states already grant immunity. Use the **Not** setting to further restrict when it runs — for example, selecting **WithMace** lets fall damage remain active while you hold a Mace, preserving its charged smash-attack bonus.

Choosing the right **Mode** for your server is the most important decision. Most modes work by modifying what the client reports to the server — **SpoofGround** and **Packet** tell the server you are on the ground before you actually land, **NoGround** never reports being on the ground (preventing the server from registering a damaging landing), and **Cancel** suppresses movement packets while you fall. Several modes are tuned for specific anti-cheat builds: **HypixelPacket** and **Hypixel** target Hypixel's protection, **Vulcan277** and **VulcanTP288** bypass different versions of Vulcan, **Verus** targets the Verus anti-cheat, **BlocksMC** is designed for BlocksMC's detection, **Grim2371-1.9+** targets GrimAC, and **Spartan524Flag** works around Spartan 524. **Rettungsplatform** is a special mode for GommeHD.net BedWars that activates that server's own rescue-platform item. **ForceJump** makes your character jump at the last moment before landing so you never accumulate enough fall distance to take damage.

Two modes take a more physical approach: **MLG** automatically places a water bucket or other soft-landing block (scaffolding, hay bale, slime block, etc.) beneath you once you exceed **MinFallDistance**, just as a skilled player would — it can also pick up the water afterwards. **Mount** searches for a nearby rideable entity and mounts it during the fall to absorb the impact. The **Blink** mode predicts an upcoming dangerous fall and queues your movement packets rather than sending them, then releases them safely once you land. For any sub-mode that offers a fall-distance selector, **Smart** automatically reads your character's safe-fall-distance attribute (which scales with Feather Falling), while **Constant** uses a fixed threshold you configure.

**Category:** Player  
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | HypixelPacket | SpoofGround, SpoofLanding, NoGround, Packet, PacketJump, MLG, Mount, Rettungsplatform, Spartan524Flag, Vulcan277, VulcanTP288, Verus, ForceJump, Cancel, Blink, HypixelPacket, Hypixel, BlocksMC, Grim2371-1.9+ | The bypass technique to use. Pick the mode that matches your server's anti-cheat. |
| Mode → [SpoofGround] → FallDistance | Mode Selector | Smart | Smart, Constant | Whether to derive the trigger threshold from your safe-fall attribute (Smart) or use a fixed value (Constant). |
| Mode → [SpoofGround] → FallDistance → [Constant] → Value | Decimal | 1.7 | 0.0..5.0 | Fixed fall distance (blocks) at which ground spoofing begins. |
| Mode → [SpoofGround] → ResetFallDistance | Toggle | true | — | Resets the client-side fall-distance counter after spoofing so it does not accumulate. |
| Mode → [SpoofLanding] → Modification | Vector3_d | — | — | X/Y/Z position offset applied to the landing packet to prevent the server from registering fall damage. |
| Mode → [Packet] → PacketType | Choice | Full | OnGroundOnly, PositionAndOnGround, LookAndOnGround, Full | Format of the extra movement packet sent with the on-ground flag set. |
| Mode → [Packet] → Filter | Mode Selector | FallDistance | FallDistance, Always | When to send the on-ground packet — only when falling far enough, or on every tick. |
| Mode → [Packet] → Filter → [FallDistance] → Distance | Mode Selector | Smart | Smart, Constant | How the trigger distance is determined in FallDistance filter mode. |
| Mode → [Packet] → Filter → [FallDistance] → Distance → [Constant] → Value | Decimal | 2.0 | 0.0..5.0 | Fixed fall-distance threshold for the FallDistance filter. |
| Mode → [Packet] → Filter → [FallDistance] → ResetFallDistance | Toggle | true | — | Resets the client-side fall-distance counter each time the packet fires. |
| Mode → [PacketJump] → PacketType | Choice | Full | PositionAndOnGround, Full | Format of the virtual-jump packet sent to the server. |
| Mode → [PacketJump] → FallDistance | Mode Selector | Smart | Smart, Constant | How the trigger fall distance is determined. |
| Mode → [PacketJump] → FallDistance → [Constant] → Value | Decimal | 3.0 | 0.0..5.0 | Fixed fall distance at which PacketJump activates. |
| Mode → [PacketJump] → Timing | Mode Selector | Landing | Landing, Falling | When to send the jump packet — just as you land (Landing) or repeatedly while you are still airborne (Falling). |
| Mode → [PacketJump] → Timing → [Falling] → ResetFallDistance | Toggle | true | — | Resets the fall-distance counter each tick while you are falling. |
| Mode → [MLG] → MinFallDistance | Decimal | 5.0 | 2.0..50.0 | Minimum fall distance (blocks) before an MLG item placement is attempted. |
| Mode → [MLG] → Rotations | Setting Group | — | — | See [Shared: Rotations](/docs/modules/shared-settings/rotations). |
| Mode → [MLG] → PickUpWater | Toggleable Group | on | — | Automatically picks up water placed during an MLG save. |
| Mode → [MLG] → PickUpWater → PickupSpan | Integer Range | 200..1000 | 0..10000 ms | Time window (ms) after placement during which placed water will be collected. |
| Mode → [Mount] → MinFallDistance | Decimal | 5.0 | 2.0..50.0 | Minimum fall distance before a mount attempt is made. |
| Mode → [Mount] → SearchRange | Decimal | 4.5 | 1.0..8.0 | Radius (blocks) around you to search for a rideable entity. |
| Mode → [Mount] → RetryDelay | Integer | 2 | 0..20 ticks | Ticks to wait before retrying if the first mount attempt fails. |
| Mode → [Mount] → SwingMode | Choice | DoNotHide | DoNotHide, HideForBoth, HideForClient, HideForServer | Controls whether the hand-swing animation from interacting with the entity is hidden. |
| Mode → [Mount] → AutoDismount | Toggleable Group | off | — | When enabled, automatically dismounts after the configured delay following a successful mount. |
| Mode → [Mount] → AutoDismount → Delay | Integer Range | 0..0 | 0..20 ticks | Random delay range (ticks) to wait before dismounting. |
| Mode → [VulcanTP288] → VoidLevel | Integer | 0 | -256..0 | Y coordinate below which the void-detection check is considered active. |
| Mode → [ForceJump] → BlockDistance | Decimal | 0.76 | 0.1..5.0 | Distance below your feet at which a block is detected, triggering the forced jump. |
| Mode → [ForceJump] → FallDistance | Decimal | 3.35 | 3.35..10.0 | Minimum fall distance before a force jump is attempted. |
| Mode → [ForceJump] → JumpHeight | Decimal | 0.11 | 0.1..0.42 | Upward velocity applied during the forced jump. |
| Mode → [Cancel] → FallDistance | Mode Selector | Smart | Smart, Constant | How the trigger fall distance is determined. |
| Mode → [Cancel] → FallDistance → [Constant] → Value | Decimal | 1.7 | 0.0..5.0 | Fixed fall distance at which movement packets are suppressed. |
| Mode → [Cancel] → ResetFallDistance | Toggle | true | — | Resets the client-side fall-distance counter after cancelling packets. |
| Mode → [Cancel] → CancelSetbackPacket | Toggle | false | — | Also suppresses server-issued position-correction (setback) packets. |
| Mode → [Blink] → TriggerFallDistance | Decimal | 2.5 | 0.5..3.0 | Predicted fall distance (simulated ahead) at which packet queuing starts. |
| Mode → [Blink] → MaximumFallDistance | Decimal | 20.0 | 2.0..50.0 | If your actual fall distance exceeds this value, queued packets are flushed immediately. |
| Mode → [HypixelPacket] → OverVoid | Toggle | false | — | Allows the mode to activate even when there is no ground block below (over the void). |
| Not | Multi-Select | (none) | WhileGliding, WithMace | Suspend NoFall while any of the selected conditions are true (e.g. gliding with an Elytra, or holding a Mace). |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/nofall/ModuleNoFall.kt)*
