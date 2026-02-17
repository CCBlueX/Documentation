## Target

The Target setting group controls how a module selects which entity to target. It filters entities from the world based on field of view and hurt time, checks whether each entity is within range (if a range value is provided by the module), verifies the entity should be attacked using the global target settings, and then sorts valid targets using a configurable priority chain. The result is an ordered list of entities, with the most preferred target first.

The Target setting group appears in the following modules:
- [KillAura](/docs/modules/combat/killaura) (adds IgnoreShield)
- [Aimbot](/docs/modules/combat/aimbot) (adds Range)
- [AutoShoot](/docs/modules/combat/autoshoot) (adds Range)
- [AutoRod](/docs/modules/combat/autorod)
- [CrystalAura](/docs/modules/combat/crystalaura) (adds Range)
- [ElytraTarget](/docs/modules/combat/elytra-target)
- [TpAura](/docs/modules/combat/tpaura)
- [BlockTrap](/docs/modules/world/blocktrap) (adds Range)
- [AutoTrap](/docs/modules/world/autotrap) (adds Range)

### Settings

| Setting | Type | Default | Range | Description |
|---------|------|---------|-------|-------------|
| FOV | Float | 180.0 | 0.0..180.0 | Maximum angle in degrees between the player's crosshair direction and an entity for it to be considered a valid target. At 180.0 all entities in front and behind the player are included. Lower values restrict targeting to entities closer to the center of the screen. |
| HurtTime | Integer | 10 | 0..10 | Maximum hurt time an entity can have to be considered a valid target. Entities with a hurt time above this value are excluded. Since hurt time counts down from 10 after being hit, a value of 10 allows targeting entities regardless of their hurt state, while 0 only allows targeting entities that are not in a hurt animation. |
| Priority | Multi-Select | Type, *then module default* | Type, Health, Distance, Direction, HurtTime, Age | An ordered list of comparators used to sort valid targets. Targets are sorted by the first priority, then ties are broken by the second, and so on. Cannot be empty. The default always starts with Type, followed by a second priority that depends on the module (e.g. Health for KillAura, Distance for AutoShoot, Direction for Aimbot). |

### Priority Options

**Type** — Sorts targets by entity type. Players are prioritized first, then hostile mobs, then neutral mobs that are angry at the player, and all other entities last. This ensures players are always targeted before other entity types when this priority is active.

**Health** — Sorts targets by their actual health (absorption hearts included) in ascending order. Entities with the lowest health are prioritized first, making it easier to secure kills on weakened targets.

**Distance** — Sorts targets by their squared boxed distance to the player in ascending order. The closest entities are prioritized first.

**Direction** — Sorts targets by the angle between the player's crosshair and the entity in ascending order. Entities closest to where the player is already looking are prioritized first. This is useful for aim-assist style modules where targeting the entity requiring the least rotation is preferred.

**HurtTime** — Sorts targets by their current hurt time in ascending order. Entities with the lowest hurt time (those not currently in a hurt animation or closest to recovering) are prioritized first. This helps avoid wasting hits on entities that are still in their invulnerability frames.

**Age** — Sorts targets by their tick count in descending order. Entities that have existed in the world the longest are prioritized first. This can help prioritize real players over recently spawned entities such as bots.

### Module-Specific Additions

Some modules extend the Target group with additional settings that are not part of the base configuration:

- **Range** — Many modules provide a range value (float or float range) that restricts targeting to entities within a certain distance from the player. The range check uses squared boxed distance and supports both single-value ranges (maximum distance only) and min–max ranges (entities must be between the two distances). The specific default and bounds depend on the module.
- **IgnoreShield** — KillAura adds this boolean (default: true) to control whether entities holding a shield that would block the attack are excluded from targeting. When enabled, shielding entities are still valid targets. When disabled, entities that would block the hit are skipped unless the player is holding an axe or AutoWeapon will switch to one.

---
*Last updated: 2026-02-13*
