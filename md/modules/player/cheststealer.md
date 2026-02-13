## ChestStealer

Automatically steals all items from a chest.

**Category:** Player  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Constraints (Setting Group)
│   ├── StartDelay (Integer Range | default: 1..2 | range: 0..20 | ticks)
│   ├── ClickDelay (Integer Range | default: 2..4 | range: 0..20 | ticks)
│   ├── CloseDelay (Integer Range | default: 1..2 | range: 0..20 | ticks)
│   ├── MissChance (Integer Range | default: 0..0 | range: 0..100 | %)
│   └── Requires (Multi-Select | options: NoMovement, NoRotation)
├── AutoClose (Toggle | default: true)
├── SelectionMode (Choice | default: DISTANCE | options: Distance, Index, Random)
├── MoveMode (Choice | default: QUICK_MOVE | options: QuickMove, DragAndDrop)
├── QuickSwaps (Toggle | default: true)
├── OnFull (Choice | default: THROW | options: None, Throw)
├── CheckScreenHandlerType (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   ├── Types (Registry List)
│   └── Filter (Choice | default: WHITELIST | options: Whitelist, Blacklist)
├── CheckScreenTitle (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   ├── Titles (Multi-Select | default: [Barrel, Chest, LargeChest, ShulkerBox, ChestMinecart] | options: Barrel, Beacon, BlastFurnace, BrewingStand, Chest, LargeChest, Dispenser, Dropper, EnderChest, Furnace, Hopper, ShulkerBox, Smoker, ChestMinecart, HopperMinecart)
│   ├── Custom (Editable List)
│   └── Filter (Choice | default: WHITELIST | options: Whitelist, Blacklist)
├── Aura (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   ├── Range (Decimal | default: 3.0 | range: 1.0..6.0)
│   ├── WallRange (Decimal | default: 0.0 | range: 0.0..6.0)
│   ├── Delay (Integer | default: 5 | range: 1..80 | ticks)
│   ├── VisualSwing (Toggle | default: true)
│   ├── NotDuringCombat (Toggle | default: true)
│   ├── TrackManualInteractions (Toggle | default: true)
│   ├── PauseOn (Multi-Select | options: Combat, UsingItem)
│   ├── ValidStorageBlocks (Registry List)
│   ├── AwaitContainer (Toggleable Group | default: on)
│   │   ├── Enabled (Toggle | default: true)
│   │   ├── Timeout (Integer | default: 10 | range: 1..80 | ticks)
│   │   └── MaxRetries (Integer | default: 4 | range: 1..10)
│   └── Rotations (Setting Group)
│       ├── AngleSmooth (Mode Selector | default: Linear | modes: Linear, Sigmoid, Acceleration)
│       │   ├── [Mode: Linear]
│       │   │   ├── HorizontalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│       │   │   └── VerticalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│       │   ├── [Mode: Sigmoid]
│       │   │   ├── HorizontalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│       │   │   ├── VerticalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│       │   │   ├── Steepness (Decimal | default: 10.0 | range: 0.0..20.0)
│       │   │   └── Midpoint (Decimal | default: 0.3 | range: 0.0..1.0)
│       │   └── [Mode: Acceleration]
│       │       ├── YawAcceleration (Decimal Range | default: 20.0..25.0 | range: 1.0..180.0)
│       │       ├── PitchAcceleration (Decimal Range | default: 20.0..25.0 | range: 1.0..180.0)
│       │       ├── DynamicAccel (Toggleable Group | default: off)
│       │       │   ├── Enabled (Toggle | default: false)
│       │       │   ├── CoefDistance (Decimal | default: -1.393 | range: -2.0..2.0)
│       │       │   ├── YawCrosshairAccel (Decimal Range | default: 17.0..20.0 | range: 1.0..180.0)
│       │       │   └── PitchCrosshairAccel (Decimal Range | default: 17.0..20.0 | range: 1.0..180.0)
│       │       ├── AccelerationError (Toggleable Group | default: on)
│       │       │   ├── Enabled (Toggle | default: true)
│       │       │   ├── YawAccelError (Decimal | default: 0.1 | range: 0.01..1.0)
│       │       │   └── PitchAccelError (Decimal | default: 0.1 | range: 0.01..1.0)
│       │       ├── ConstantError (Toggleable Group | default: on)
│       │       │   ├── Enabled (Toggle | default: true)
│       │       │   ├── YawConstantError (Decimal | default: 0.1 | range: 0.01..1.0)
│       │       │   └── PitchConstantError (Decimal | default: 0.1 | range: 0.01..1.0)
│       │       └── SigmoidDeceleration (Toggleable Group | default: off)
│       │           ├── Enabled (Toggle | default: false)
│       │           ├── Steepness (Decimal | default: 10.0 | range: 0.0..20.0)
│       │           └── Midpoint (Decimal | default: 0.3 | range: 0.0..1.0)
│       ├── MovementCorrection (Choice | default: SILENT | options: Off, Strict, Silent, ChangeLook)
│       ├── ResetThreshold (Decimal | default: 2.0 | range: 1.0..180.0)
│       └── TicksUntilReset (Integer | default: 5 | range: 1..30 | ticks)
└── SilentScreen (Toggleable Group | default: off)
    ├── Enabled (Toggle | default: false)
    ├── UnlockCursor (Toggle | default: false)
    └── DrawInventoryTag (Toggleable Group | default: on)
        ├── Enabled (Toggle | default: true)
        ├── Background (Mode Selector | default: Rect | modes: Rect, Texture)
        │   ├── [Mode: Rect]
        │   │   ├── Color (Color)
        │   │   ├── OutlineColor (Color)
        │   │   └── Margin (Decimal | default: 2.0 | range: 0.0..100.0)
        ├── Scale (Decimal | default: 1.5 | range: 0.25..4.0)
        ├── RenderOffset (3D Position)
        └── ShowTitle (Toggle | default: false)
```

### Settings Details

#### Constraints

A group of related settings.

- **StartDelay** (Integer Range) — default: `1` – `2`; range: `0` – `20`; unit: ticks
- **ClickDelay** (Integer Range) — default: `2` – `4`; range: `0` – `20`; unit: ticks
- **CloseDelay** (Integer Range) — default: `1` – `2`; range: `0` – `20`; unit: ticks
- **MissChance** (Integer Range) — default: `0` – `0`; range: `0` – `100`; unit: %
- **Requires** (Multi-Select) — options: `NoMovement`, `NoRotation`

- **AutoClose** (Toggle) — default: `true`
- **SelectionMode** (Choice) — default: `DISTANCE`; options: `Distance`, `Index`, `Random`
- **MoveMode** (Choice) — default: `QUICK_MOVE`; options: `QuickMove`, `DragAndDrop`
- **QuickSwaps** (Toggle) — default: `true`
- **OnFull** (Choice) — default: `THROW`; options: `None`, `Throw`
#### CheckScreenHandlerType

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Types** (Registry List)
- **Filter** (Choice) — default: `WHITELIST`; options: `Whitelist`, `Blacklist`

#### CheckScreenTitle

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Titles** (Multi-Select) — default: `Barrel`, `Chest`, `LargeChest`, `ShulkerBox`, `ChestMinecart`; options: `Barrel`, `Beacon`, `BlastFurnace`, `BrewingStand`, `Chest`, `LargeChest`, `Dispenser`, `Dropper`, `EnderChest`, `Furnace`, `Hopper`, `ShulkerBox`, `Smoker`, `ChestMinecart`, `HopperMinecart`
- **Custom** (Editable List)
- **Filter** (Choice) — default: `WHITELIST`; options: `Whitelist`, `Blacklist`

#### Aura

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Range** (Decimal) — default: `3.0`; range: `1.0` – `6.0`
- **WallRange** (Decimal) — default: `0.0`; range: `0.0` – `6.0`
- **Delay** (Integer) — default: `5`; range: `1` – `80`; unit: ticks
- **VisualSwing** (Toggle) — default: `true`
- **NotDuringCombat** (Toggle) — default: `true`
- **TrackManualInteractions** (Toggle) — default: `true`
- **PauseOn** (Multi-Select) — options: `Combat`, `UsingItem`
- **ValidStorageBlocks** (Registry List)
##### AwaitContainer

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Timeout** (Integer) — default: `10`; range: `1` – `80`; unit: ticks
- **MaxRetries** (Integer) — default: `4`; range: `1` – `10`

##### Rotations

A group of related settings.

###### AngleSmooth

Select a mode for this feature. Available modes: **Linear**, **Sigmoid**, **Acceleration**. Default: **Linear**.

###### Mode: Linear

- **HorizontalTurnSpeed** (Decimal Range) — default: `180.0` – `180.0`; range: `0.0` – `180.0`
- **VerticalTurnSpeed** (Decimal Range) — default: `180.0` – `180.0`; range: `0.0` – `180.0`

###### Mode: Sigmoid

- **HorizontalTurnSpeed** (Decimal Range) — default: `180.0` – `180.0`; range: `0.0` – `180.0`
- **VerticalTurnSpeed** (Decimal Range) — default: `180.0` – `180.0`; range: `0.0` – `180.0`
- **Steepness** (Decimal) — default: `10.0`; range: `0.0` – `20.0`
- **Midpoint** (Decimal) — default: `0.3`; range: `0.0` – `1.0`

###### Mode: Acceleration

- **YawAcceleration** (Decimal Range) — default: `20.0` – `25.0`; range: `1.0` – `180.0`
- **PitchAcceleration** (Decimal Range) — default: `20.0` – `25.0`; range: `1.0` – `180.0`
###### DynamicAccel

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
- **CoefDistance** (Decimal) — default: `-1.393`; range: `-2.0` – `2.0`
- **YawCrosshairAccel** (Decimal Range) — default: `17.0` – `20.0`; range: `1.0` – `180.0`
- **PitchCrosshairAccel** (Decimal Range) — default: `17.0` – `20.0`; range: `1.0` – `180.0`

###### AccelerationError

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **YawAccelError** (Decimal) — default: `0.1`; range: `0.01` – `1.0`
- **PitchAccelError** (Decimal) — default: `0.1`; range: `0.01` – `1.0`

###### ConstantError

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **YawConstantError** (Decimal) — default: `0.1`; range: `0.01` – `1.0`
- **PitchConstantError** (Decimal) — default: `0.1`; range: `0.01` – `1.0`

###### SigmoidDeceleration

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
- **Steepness** (Decimal) — default: `10.0`; range: `0.0` – `20.0`
- **Midpoint** (Decimal) — default: `0.3`; range: `0.0` – `1.0`


- **MovementCorrection** (Choice) — default: `SILENT`; options: `Off`, `Strict`, `Silent`, `ChangeLook`
- **ResetThreshold** (Decimal) — default: `2.0`; range: `1.0` – `180.0`
- **TicksUntilReset** (Integer) — default: `5`; range: `1` – `30`; unit: ticks


#### SilentScreen

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
- **UnlockCursor** (Toggle) — default: `false`
##### DrawInventoryTag

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
###### Background

Select a mode for this feature. Available modes: **Rect**, **Texture**. Default: **Rect**.

###### Mode: Rect

- **Color** (Color)
- **OutlineColor** (Color)
- **Margin** (Decimal) — default: `2.0`; range: `0.0` – `100.0`

- **Scale** (Decimal) — default: `1.5`; range: `0.25` – `4.0`
- **RenderOffset** (3D Position)
- **ShowTitle** (Toggle) — default: `false`



### Screenshots

*Screenshots for ChestStealer will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fplayer%2FModuleChestStealer.kt)*
