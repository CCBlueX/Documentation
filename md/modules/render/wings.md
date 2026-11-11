## Wings

Draws glowing wings on your back. Your friends can get wings too. Only you see them.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Position → Height | Decimal | 0.3 | -1.0..1.0 | Moves the wings up or down. |
| Position → BackOffset | Decimal | 0.25 | 0.0..0.5 | How far behind the back the wings sit. |
| Position → EquipmentOffset | Decimal | 0.1 | 0.0..1.0 | Extra space behind the back when the player wears a chestplate or elytra. |
| Mode | Choice | Lines | Lines | How the wings look. |
| Mode → [Lines] → ShowDamage | Toggle | On | | Turns the wings red while the player is hurt. |
| Mode → [Lines] → ShowInFirstPerson | Toggle | Off | | Shows your own wings in first person too. |
| Mode → [Lines] → FriendsOptions → ViewOnFriend | Toggle | On | | Also draws wings on your friends. |
| Mode → [Lines] → FriendsOptions → Distance | Integer | 64 blocks | 8..512 | How close a friend has to be to get wings. |
| Mode → [Lines] → Length | Decimal | 1.0 | 0.1..2.0 | How long the wings are. |
| Mode → [Lines] → Width | Decimal | 0.05 | 0.01..1.0 | How thick each line is. |
| Mode → [Lines] → FadeStartRatio | Decimal | 0.5 | 0.1..1.0 | Where along the line it starts to fade out. Lower values fade sooner. |
| Mode → [Lines] → LinesCount | Integer | 4 | 1..12 | How many lines each wing has. |
| Mode → [Lines] → Angles | Integer Range | 10..37 | 1..90 | The angles, in degrees, the lines spread between. |
| Mode → [Lines] → Color | Color | LiquidBounce blue | | The color of the wings. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/613dfacc9/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/wings)*
