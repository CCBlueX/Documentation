## TargetLock

TargetLock makes you fight one player at a time, so modules like [KillAura](/docs/modules/combat/killaura) don't switch to someone else in a big fight.

In Temporary mode, the first player you hit becomes your target. The lock ends after MaximumTime, or when the player gets too far away. In Filter mode, you write a list of names and choose to attack only them (Whitelist) or everyone but them (Blacklist).

**Category:** Misc
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | Temporary | Temporary, Filter | How your target is chosen. |
| Mode → [Temporary] → MaximumTime | Integer | 30 | 0..120 s | How long the lock lasts after you hit a player. |
| Mode → [Temporary] → MaximumRange | Decimal | 20.0 | 8.0..40.0 | The lock ends when the player is farther away than this, in blocks. |
| Mode → [Temporary] → WhenNoLock | Choice | AllowAll | AllowAll, AllowNone | What happens before you hit someone. AllowAll attacks anyone. AllowNone attacks no one. |
| Mode → [Filter] → Usernames | Editable List | Notch | | Player names for the filter. |
| Mode → [Filter] → FilterType | Choice | Whitelist | Whitelist, Blacklist | Whitelist attacks only these players. Blacklist attacks everyone else. |
| Combat | Toggle | false | | On: other players are only skipped as attack targets. Off: they are ignored by every module, for example ESP too. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/ModuleTargetLock.kt)*
