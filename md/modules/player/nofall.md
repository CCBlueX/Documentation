## NoFall

NoFall stops you from taking fall damage. Each mode does this in a different way, so pick the one that works on your server. It does nothing in Creative or Spectator mode, while you fly, or while you can't take damage.

Most modes change what your client tells the server about landing, for example by saying you are already on the ground. Some modes are made for one anticheat or server, and their name says which one. MLG places a water bucket or another soft block under you before you land, like a skilled player would. Mount jumps onto a nearby rideable mob while you fall. Rettungsplatform uses the rescue platform item (blaze rod or magma cream) from BedWars on GommeHD.

By default NoFall pauses while you glide with an elytra and while you hold a mace, so mace smash attacks still deal their bonus damage. Change this with Not.

**Category:** Player
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | SpoofGround | SpoofGround, SpoofLanding, NoGround, Packet, PacketJump, MLG, Mount, Rettungsplatform, Spartan-Phase524, Vulcan-2.7.7, Vulcan-2.8.8, Verus-b3896, ForceJump, Cancel, Blink, HypixelPacket, Hypixel, BlocksMC, Grim-2.3.71-MC1.9 | How fall damage is avoided. Pick the one that works on your server. |
| Mode → SpoofGround → FallDistance | Mode Selector | Smart | Smart, Constant | Smart works out from your character when a fall starts to hurt (Feather Falling counts). Constant uses the Value below. |
| Mode → SpoofGround → FallDistance → Constant → Value | Decimal | 1.7 | 0.0..5.0 | Fall distance in blocks at which NoFall starts working. |
| Mode → SpoofGround → ResetFallDistance | Toggle | On | | Resets how far the client thinks you have fallen. |
| Mode → SpoofLanding → Modification | Vector | 1337, 0, 1337 | | Position change sent with the landing. |
| Mode → Packet → PacketType | Choice | Full | OnGroundOnly, PositionAndOnGround, LookAndOnGround, Full | Which kind of movement packet to send. |
| Mode → Packet → Filter | Mode Selector | FallDistance | FallDistance, Always | Send the packet only after falling far enough, or all the time. |
| Mode → Packet → Filter → FallDistance → Distance | Mode Selector | Smart | Smart, Constant | Smart works out when a fall starts to hurt. Constant uses the Value below. |
| Mode → Packet → Filter → FallDistance → Distance → Constant → Value | Decimal | 2.0 | 0.0..5.0 | Fall distance in blocks at which the packet is sent. |
| Mode → Packet → Filter → FallDistance → ResetFallDistance | Toggle | On | | Resets how far the client thinks you have fallen. |
| Mode → PacketJump → PacketType | Choice | Full | PositionAndOnGround, Full | Which kind of movement packet to send. |
| Mode → PacketJump → FallDistance | Mode Selector | Smart | Smart, Constant | Smart works out when a fall starts to hurt. Constant uses the Value below. |
| Mode → PacketJump → FallDistance → Constant → Value | Decimal | 3.0 | 0.0..5.0 | Fall distance in blocks at which PacketJump works. |
| Mode → PacketJump → Timing | Mode Selector | Landing | Landing, Falling | Send the jump right before you land, or while you are still falling. |
| Mode → PacketJump → Timing → Falling → ResetFallDistance | Toggle | On | | Resets how far the client thinks you have fallen. |
| Mode → MLG → MinFallDistance | Decimal | 5.0 | 2.0..50.0 | How far you have to fall before a block is placed. |
| Mode → MLG → Rotations | Setting Group | | | See [Rotations](/docs/modules/shared-settings/rotations). |
| Mode → MLG → PickUpWater | Toggleable Group | On | | Picks the water back up after landing. |
| Mode → MLG → PickUpWater → PickupSpan | Integer Range | 200..1000 | 0..10000 ms | How long after placing it the water gets picked up. |
| Mode → Mount → MinFallDistance | Decimal | 5.0 | 2.0..50.0 | How far you have to fall before NoFall tries to mount. |
| Mode → Mount → SearchRange | Decimal | 4.5 | 1.0..8.0 | How far away, in blocks, a mob to ride can be. |
| Mode → Mount → RetryDelay | Integer | 2 | 0..20 ticks | Ticks (20 per second) to wait before trying again. |
| Mode → Mount → SwingMode | Choice | DoNotHide | DoNotHide, HideForBoth, HideForClient, HideForServer | Whether your arm swing is shown when you mount. |
| Mode → Mount → AutoDismount | Toggleable Group | Off | | Gets off the mob again after landing. |
| Mode → Mount → AutoDismount → Delay | Integer Range | 0..0 | 0..20 ticks | How long to wait before getting off. |
| Mode → Vulcan-2.8.8 → VoidLevel | Integer | 0 | -256..0 | The mode only works if there is ground under you above this height. |
| Mode → ForceJump → BlockDistance | Decimal | 1.0 | 0.1..5.0 | How close the ground has to be before the jump. |
| Mode → ForceJump → FallDistance | Decimal | 3.35 | 3.35..10.0 | How far you have to fall before the jump. |
| Mode → ForceJump → JumpHeight | Decimal | 0.42 | 0.1..0.42 | How strong the jump is. |
| Mode → Cancel → FallDistance | Mode Selector | Smart | Smart, Constant | Smart works out when a fall starts to hurt. Constant uses the Value below. |
| Mode → Cancel → FallDistance → Constant → Value | Decimal | 1.7 | 0.0..5.0 | Fall distance in blocks at which NoFall starts working. |
| Mode → Cancel → ResetFallDistance | Toggle | On | | Resets how far the client thinks you have fallen. |
| Mode → Cancel → CancelSetbackPacket | Toggle | Off | | Also ignores the server pulling you back. |
| Mode → Blink → TriggerFallDistance | Decimal | 2.5 | 0.5..3.0 | Blink starts holding back your movement once it predicts you will fall farther than this. |
| Mode → Blink → MaximumFallDistance | Decimal | 20.0 | 2.0..50.0 | If you fall farther than this, the held-back movement is sent right away. |
| Mode → HypixelPacket → OverVoid | Toggle | Off | | Also works when there is no ground under you. |
| Not | Multi-Select | WhileGliding, WithMace | WhileGliding, WithMace | NoFall pauses while one of these is true. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/nofall/ModuleNoFall.kt)*
