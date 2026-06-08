## CheckScreenHandlerType

This shared setting group lets you control which kinds of container screens a module is allowed to act on. In Minecraft, every container you open — chests, double chests, shulker boxes, hoppers, barrels, furnaces, and so on — has its own screen type. This group gives you a list of those types plus a filter mode so you can decide exactly where a module does its work.

The **Types** list is where you pick the container screens you care about, and the **Filter** mode decides how that list is read. With **Whitelist**, the module only acts on the screens you added to the list and ignores everything else. With **Blacklist**, the module acts on every screen *except* the ones you listed. This is handy when, for example, you want [ChestStealer](/docs/modules/player/cheststealer) to empty chests but leave certain menus alone, or you want a module to only trigger inside specific containers.

If you leave the list empty, the filter effectively applies to nothing on the whitelist side (no screens match) or everything on the blacklist side (nothing is excluded), so set the list to match the containers you actually want to target.

This setting group is used by the following modules:
- [AutoF5](/docs/modules/render/autof5)
- [ChestCleaner](/docs/modules/player/chestcleaner)
- [ChestStealer](/docs/modules/player/cheststealer)

### Settings

| Setting | Type | Default | Range | Description |
| --- | --- | --- | --- | --- |
| Types | Registry List | — | — | The list of container screen types this filter applies to. |
| Filter | Choice | Whitelist | Whitelist, Blacklist | How the Types list is used: Whitelist acts only on listed screens, Blacklist acts on everything except listed screens. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2)*
