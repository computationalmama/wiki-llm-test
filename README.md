# wiki-llm-test

A persistent, LLM-maintained Markdown wiki for Gooey.AI-related people, projects, and events — built and curated using the Karpathy-style LLM Wiki Builder pattern.

- `raw_sources/` — immutable original materials (bios, notes, event photos/logs)
- `wiki/` — curated Markdown knowledge base (entities, concepts, source map, index)
- `AGENTS.md` — maintenance rules for future agents/maintainers
- `WIKI_SCHEMA.md` — file/naming conventions

Start here: [`wiki/index.md`](wiki/index.md)

## Folder structure

```
wiki-llm-test/
├── AGENTS.md
├── WIKI_SCHEMA.md
├── README.md
│
├── raw_sources/                                  # Immutable original source materials
│   ├── ambika-joshi-bio-context-2026.md          # Self-reported bio/context dump
│   └── realml-event-notes.md                     # RealML event — 4 images logged, written notes pending
│
└── wiki/                                         # Curated LLM-maintained knowledge base
    ├── index.md                                  # Start here — overview + status + open questions
    ├── source-map.md                             # Tracks every raw source, its status & confidence
    │
    ├── entities/                                 # People, orgs, platforms
    │   ├── ambika-joshi.md                       # Head of DevRel, Gooey.AI / "Computational Mama"
    │   ├── gooey-ai.md                            # Open-source AI orchestration platform
    │   └── ajaibghar-cultural-services.md         # Creative tech studio co-founded by Ambika
    │
    └── concepts/                                 # Projects, practices, events
        ├── computational-mama-practice.md         # Art/research practice — code as care, AI & motherhood
        ├── sun-shines-bright-solarpi.md            # Solar-powered portable AI hardware project
        ├── dpga-nomination.md                     # Digital Public Goods Alliance nomination (Gooey.AI)
        └── realml.md                               # RealML event — partial, images logged, notes pending
```

## Navigation tips
- Every wiki page cites its raw source(s) — follow the "Sources" section on any page to see original material.
- Pages marked "Needs verification" or "Not found in sources" indicate known gaps — see each page's "Open questions" section.
- Cross-links use `[[Double Bracket]]` notation to point to related entities/concepts.
