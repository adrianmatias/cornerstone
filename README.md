# cornerstone

An **LLM wiki** (Karpathy-style, living research repository) on **the Great Pyramid of Giza** — treated as a cornerstone for engineering, the history of mankind, and the spirit.

This repository is the working session behind the Obsidian vault at `~/Documents/obsidian/cornerstone`. It tracks and deepens the research iteratively: ingestion of source material into `raw/`, synthesis into a backlinked wiki, with contradictions surfaced rather than hidden.

## Structure

```
cornerstone/
├── raw/
│   ├── log.md               # User entrypoint — prompts + source material (chronological)
│   ├── log_hermes.md        # Agent operations log (chronological)
│   └── articles/            # Raw source material / research notes
├── concepts/                # Concept pages (construction, dating, purpose, ...)
├── entities/                # Entity pages (people, structures, sites)
├── index.md                 # Content catalog: every page with a one-line summary
├── SCHEMA.md                # Wiki schema & conventions
├── hermes.md                # Agent's seed document / research history
└── README.md                # This file
```

## Conventions

- **`raw/` is immutable** — original prompts and source material, never edited in place.
- **`concepts/` + `entities/` are synthesis** — distilled, backlinked knowledge derived from the raw layer.
- **Chronological logs**: `raw/log.md` (user) and `raw/log_hermes.md` (agent) accumulate by appending, never by overwriting.
- **`SCHEMA.md`** defines the page taxonomy, frontmatter, provenance markers, and update policy.
- Contradictions are surfaced, not hidden — both positions are presented with dates and sources.

## Guiding research lines

- Block transport via **rolling** (wooden cradles) instead of sledges
- The **Sphinx** and its relationship to the Giza complex; water-weathering erosion ~20,000 BC
- **Tunnels and passages** connecting the Great Pyramid with the Sphinx or the Nile
- Khufu's pyramid as the culmination of an evolving technology (dating implications for other pyramids)
- Recent **SAR claims** by Malanga & Biondi of massive vertical shafts beneath the Khafre Pyramid

See `raw/log.md` for the full history of prompts.
