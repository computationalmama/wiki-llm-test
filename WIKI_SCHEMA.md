# WIKI_SCHEMA.md — Structural Conventions

## Directory layout
```
raw_sources/            Immutable original materials
wiki/
  index.md              Top-level entry point and navigation
  source-map.md          Registry of all raw sources + derived pages
  entities/
    <slug>.md            People, organizations, products
  concepts/
    <slug>.md            Ideas, projects, ongoing initiatives, events
AGENTS.md               Maintenance rules for agents
WIKI_SCHEMA.md          This file
```

## Entity page template
```markdown
# <Entity Name>

## Summary
One to three sentence overview.

## Details
Structured facts, grouped by theme.

## Related
- [[Other Entity]]
- [[Related Concept]]

## Sources
- `raw_sources/<file>` — description

## Open questions
- Explicit list of unknowns / needs verification
```

## Concept/project page template
```markdown
# <Concept/Project Name>

## Summary
What it is, in 1-3 sentences.

## Key facts
- Bullet list of concrete, sourced facts

## Timeline (if applicable)
- Date — event

## Related
- [[Entity]]
- [[Other Concept]]

## Sources
- `raw_sources/<file>`

## Open questions
- Explicit list of unknowns
```

## Cross-linking
- Use `[[Concept Name]]` or `[[Entity Name]]` inline to reference other pages by their human-readable title.
- Keep filenames stable and lowercase-hyphenated even if the display title changes.

## Uncertainty markers
- `Unknown` — genuinely not knowable from context
- `Not found in sources` — could exist but hasn't been provided yet
- `Needs verification` — stated but not confirmed, or ambiguous/conflicting
