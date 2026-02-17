## ItemTags

Display icons and quantities labels for dropped items.

**Category:** Render  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Filter (Choice | default: BLACKLIST | options: Whitelist, Blacklist)
├── Items (Registry List)
├── BackgroundColor (Color)
├── Scale (Curve)
├── RenderOffset (3D Position)
├── RowLength (Integer | default: 100 | range: 1..100)
├── PreventOverlap (Toggle | default: true)
├── ClusterEntities (Curve)
├── MergeMode (Choice | default: BY_COMPONENTS | options: None, ByItem, ByComponents)
└── Shulker (Toggleable Group | default: off)
    ├── Enabled (Toggle | default: false)
    ├── MergeStacks (Toggle | default: true)
    └── ShowTitle (Toggle | default: true)
```

### Settings Details

- **Filter** (Choice) — default: `BLACKLIST`; options: `Whitelist`, `Blacklist` — Whether the item list acts as a whitelist or blacklist.
- **Items** (Registry List) — List of items to include or exclude.
- **BackgroundColor** (Color) — Background color of the item tag label.
- **Scale** (Curve) — Curve mapping distance to tag display scale.
- **RenderOffset** (3D Position) — Positional offset for the item tag label.
- **RowLength** (Integer) — default: `100`; range: `1` – `100` — Maximum items per row in the tag display.
- **PreventOverlap** (Toggle) — default: `true` — Prevents item tags from overlapping each other.
- **ClusterEntities** (Curve) — Curve mapping distance to cluster grouping radius.
- **MergeMode** (Choice) — default: `BY_COMPONENTS`; options: `None`, `ByItem`, `ByComponents` — How duplicate item stacks are merged together.
#### Shulker

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false` — Toggles display of shulker box contents.
- **MergeStacks** (Toggle) — default: `true` — Merges stacks inside shulker boxes.
- **ShowTitle** (Toggle) — default: `true` — Shows the shulker box name above its contents.


### Screenshots

*Screenshots for ItemTags will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Frender%2FModuleItemTags.kt)*
