## Global Settings Overview

Global settings belong to the whole client, not to one module. You find them in the ClickGUI (opened with Right Shift) under Settings. You can also change them with the [`.value`](/docs/commands/client) command, using paths that start with `settings.`, like `settings.commands.prefix`.

- [Targets](/docs/global-settings/targets): which players and mobs combat and visual modules care about.
- [Teleport](/docs/global-settings/teleport): how the `.teleport`, `.playerteleport` and `.vclip` commands move you.
- [Client Chat](/docs/global-settings/client-chat): LiquidChat, the chat between LiquidBounce users.
- [Rich Presence](/docs/global-settings/rich-presence): what Discord shows about LiquidBounce on your profile.
- [Auto Translate](/docs/global-settings/auto-translate): which service translates chat messages.
- [Blink Manager](/docs/global-settings/blink-manager): how your held-back position looks while Blink and similar modules are on.
- [Commands](/docs/global-settings/commands): the command prefix and suggestions for mistyped commands.
- [Language](/docs/global-settings/language): the language of the client's menus and messages.
- [Gui Renderer](/docs/global-settings/gui-renderer): how sharp the menus are and which browser draws them.
- [View Model](/docs/global-settings/view-model): how items in your hand look and swing.
- [Rotation Manager](/docs/global-settings/rotation-manager): shows on your character where modules make you look.

---

*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/global/GlobalManager.kt)*
