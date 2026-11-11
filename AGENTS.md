# AGENTS.md

How pages in this repository are written. File layout, the manifest and redirects are in the
README.

## Readers

- User pages (modules, get started, usage, commands, global settings, servers,
  troubleshooting, premium, LiquidProxy, Baritone, AutoConfig): a 10-year-old who just
  started with the client and knows nothing technical. Short sentences, everyday words. Say
  what it does in the game and when you would turn it on.
- Developer pages (add-on API, script API, theme development): people writing an add-on,
  script or theme. Document what they call and how to use it, not how the client works
  inside.

## What belongs in the docs

Only what the reader of that page needs. Most client changes need no docs change at all.

Update a page when:

- a module, command or setting is added, removed or renamed, or a default or range changes
  (update the settings table)
- something a user sees or does works differently than the page says
- an API that add-ons, scripts or themes call is added, changed or removed

Never add:

- a sentence just so a change leaves a trace in the docs
- notes on a page that is not about that thing (a cosmetics detail in a setup tutorial)
- internal REST routes, packets, class names or implementation details, unless the page
  documents that exact API for developers who must call it
- bug-fix notes, edge-case trivia, history or changelog wording ("now", "no longer", "was
  renamed from", "since version")

If you have to explain why a reader needs a sentence, they do not need it.

## Style

- Timeless present tense, plain and neutral.
- No em dashes. Use periods, commas, colons or parentheses. Leave empty table cells empty.
- No AI tells: marketing words ("seamlessly", "powerful", "quietly"), "not X but Y", lists of
  three by habit, bold labels in front of every line, a closing sentence that repeats the
  point. [Humanizer](https://github.com/blader/humanizer) lists the patterns.
- "LiquidBounce" for the client, "the legacy version" for the old 1.8.9 client. No internal
  branch names such as "Nextgen".
- Links use the manifest URLs in lower case, e.g. `/docs/modules/combat/killaura`. Mixed-case
  paths do not load on the site.
- Never invent behaviour, settings or URLs. Never add personal data, credentials or anything
  about our infrastructure (exit IPs, ISPs, internal limits, hostnames).

## Module pages

Keep the shape:

```markdown
## ModuleName

One to three short sentences: what it does and when to use it.

**Category:** Combat
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Range | Decimal | 4.2 | 1.0..8.0 | How far away a target can be, in blocks. |

---
*Last updated: YYYY-MM-DD, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/<commit>/<path>)*
```

- Names, types, defaults, ranges and modes match the client source exactly. Nested settings
  are written `Group → [Mode] → Setting`.
- Types: Toggle, Integer, Integer Range, Decimal, Decimal Range, Text, Text List, Color, Key,
  Mode Selector, Choice, Multi-Select, Registry List, Editable List, Curve, File, Vector,
  Setting Group, Toggleable Group.
- Settings shared by many modules link to their page under
  `/docs/modules/shared-settings/` instead of being repeated.
- Only AutoConfig and HUD are enabled by default.
