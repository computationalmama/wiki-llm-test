# AGENTS.md — Maintenance Rules for This Wiki

This file defines how any LLM agent (or human) should read, extend, and edit this wiki going forward.

## Core model
- `raw_sources/` holds **immutable** original materials (pasted text, transcripts, documents). Never edit these after creation — if a source needs correction, add a new dated raw source and note the supersession in `wiki/source-map.md`.
- `wiki/` holds **curated, maintained** Markdown pages: entities, concepts, comparisons, timelines, open questions, and the source map.
- Every non-trivial factual claim in `wiki/` should be traceable to a raw source. If it isn't, mark it `Needs verification` or `Not found in sources`.

## Before editing
1. Always read `wiki/index.md` and `wiki/source-map.md` first.
2. Read the specific concept/entity page(s) you're about to touch in full before editing.
3. Check `raw_sources/` for the original material backing any claim you're changing.

## When ingesting new material
1. Add the raw source verbatim (or as a faithful transcript) to `raw_sources/` with a descriptive, dated filename.
2. Add a row to `wiki/source-map.md`.
3. Update or create entity/concept pages, cross-linking with `[[Double Bracket Names]]`.
4. Update `wiki/index.md` if new top-level entities/concepts are added.
5. Never invent facts. Use `Unknown`, `Not found in sources`, or `Needs verification` explicitly when information is missing or ambiguous.

## When editing existing pages
- Prefer additive, precise edits over rewriting whole pages.
- Preserve prior facts unless a newer, more reliable source contradicts them — in that case, note the contradiction and cite both sources rather than silently overwriting.
- Show Before/After or patch-style summaries when reporting edits back to the user.

## Sensitive/out-of-scope content
- This wiki curates factual, source-grounded knowledge. Requests for generated content outside that scope (e.g., astrological/horoscope predictions, speculative financial advice) should be **logged as a factual record of the request** (e.g., "user requested X") but the actual generated content should **not** be fabricated or included as wiki fact.

## File naming
- Entities: `wiki/entities/<slug>.md`
- Concepts/projects: `wiki/concepts/<slug>.md`
- Slugs: lowercase, hyphen-separated, stable once created (do not rename without updating all cross-links).

## Commit hygiene
- Use atomic multi-file commits for related changes.
- Commit messages should describe the source or update driving the change, e.g. `Update LLM wiki from Gooey`.
- Never commit empty files or placeholder content.
