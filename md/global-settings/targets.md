## Targets

Defines which entity types are considered targets across the entire client. These settings are shared by all combat modules (e.g. KillAura, Aimbot) and visual modules (e.g. ESP, Nametags).

**Aliases:** Enemies

### Settings

```
├── Combat (Multi-Select | default: [Players, Hostile, Angerable, WaterCreature, Invisible] | options: Players, Hostile, Angerable, WaterCreature, Passive, Invisible, Dead, Sleeping, Friends)
└── Visual (Multi-Select | default: [Players, Hostile, Angerable, WaterCreature, Invisible] | options: Self, Players, Hostile, Angerable, WaterCreature, Passive, Invisible, Dead, Sleeping, Friends)
```

### Settings Details

- **Combat** (Multi-Select) — default: `Players`, `Hostile`, `Angerable`, `WaterCreature`, `Invisible`; options: `Players`, `Hostile`, `Angerable`, `WaterCreature`, `Passive`, `Invisible`, `Dead`, `Sleeping`, `Friends` — Determines which entity types combat modules will attack. The `Self` option is excluded from combat targeting.
- **Visual** (Multi-Select) — default: `Players`, `Hostile`, `Angerable`, `WaterCreature`, `Invisible`; options: `Self`, `Players`, `Hostile`, `Angerable`, `WaterCreature`, `Passive`, `Invisible`, `Dead`, `Sleeping`, `Friends` — Determines which entity types visual modules will highlight or display. Includes the `Self` option for rendering your own player in third-person or FreeCam.

### Target Types

| Target | Description |
|---|---|
| Self | Your own player (visual only, shown in third-person/FreeCam) |
| Players | Other player entities |
| Hostile | Hostile mobs (zombies, skeletons, etc.) |
| Angerable | Neutral mobs that can become hostile (wolves, endermen, etc.) |
| WaterCreature | Aquatic mobs (dolphins, fish, etc.) |
| Passive | Passive mobs (cows, pigs, sheep, etc.) |
| Invisible | Entities with the invisibility effect |
| Dead | Entities that are currently dead |
| Sleeping | Players that are sleeping in a bed |
| Friends | Players on your friend list |

> **Tip:** You can also configure targets using the `.targets` command. For example: `.targets combat Players` toggles the Players target for combat.
