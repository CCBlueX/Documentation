## TargetLock

TargetLock restricts which players your client will attack, keeping you focused on a single target at a time. This is particularly useful in hectic PvP scenarios — such as faction fights or crystal PvP — where nearby enemies could otherwise steal the targeting focus of modules like [KillAura](/docs/modules/combat/killaura).

**Temporary** mode establishes a lock the first time you attack a player. The lock persists for up to `MaximumTime` seconds and is automatically released if the target moves beyond `MaximumRange` blocks or if you die. The `WhenNoLock` setting controls what happens when no lock is currently active: `AllowAll` lets targeting work normally until you hit someone, while `AllowNone` blocks all attacks until a lock is established — making it a strict single-target mode from the start.

**Filter** mode uses a static username list instead of a combat trigger. Add names to the `Usernames` list and choose `Whitelist` to allow attacking only those players, or `Blacklist` to block attacking them and allow everyone else. The `Combat` toggle, available in both modes, narrows the lock restriction to combat modules only (such as [KillAura](/docs/modules/combat/killaura)) rather than applying it globally across all targeting.

**Category:** Misc  
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | Temporary | — | Selects how the target lock is determined: `Temporary` locks on after you attack a player; `Filter` locks by a static username list. |
| Mode → [Temporary] → MaximumTime | Integer | 30 | 0 – 120 s | How long (in seconds) a temporary lock lasts after attacking a player. Setting this to `0` keeps the lock active until the player moves out of range. |
| Mode → [Temporary] → MaximumRange | Decimal | 20.0 | 8.0 – 40.0 | Maximum distance in blocks at which a temporary lock is maintained. If the locked player moves farther away, the lock is released automatically. |
| Mode → [Temporary] → WhenNoLock | Choice | AllowAll | — | Behaviour when no player is currently locked. `AllowAll` permits attacking any player normally; `AllowNone` blocks all attacks until a lock is first established. |
| Mode → [Filter] → Usernames | Editable List | — | — | The list of player usernames used for filtering. Add one name per entry. |
| Mode → [Filter] → FilterType | Choice | Whitelist | — | `Whitelist` allows attacking only the players in `Usernames`; `Blacklist` blocks attacking those players and permits all others. |
| Combat | Toggle | false | — | When enabled, the lock restriction applies only to combat modules (such as [KillAura](/docs/modules/combat/killaura)); when disabled, it applies globally to all targeting. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/ModuleTargetLock.kt)*
