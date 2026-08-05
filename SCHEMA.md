# Wiki Schema

## Domain
The Great Pyramid of Giza as a cornerstone for engineering, the history of mankind, and the spirit. Covers construction techniques, dating, purpose, internal structure, the Giza complex (pyramids, Sphinx, temples), geological context, astronomical/ritual function, occult and esoteric traditions, and the evolution of pyramid technology across dynasties.

## Conventions
- File names: lowercase, hyphens, no spaces (e.g., `construction-methods.md`)
- Every wiki page starts with YAML frontmatter (see below)
- Use `[[wikilinks]]` to link between pages (minimum 2 outbound links per page)
- When updating a page, always bump the `updated` date
- Every new page must be added to `index.md` under the correct section
- Every action must be appended to `log.md` (user entrypoint) and `log_hermes.md` (agent log)
- **Provenance markers:** On pages that synthesize 3+ sources, append `^[raw/articles/source-file.md]` at the end of paragraphs whose claims come from a specific source.
- Contradictions are surfaced, not hidden. When two sources conflict, both positions are presented with dates and sources.

## Frontmatter
```yaml
---
title: Page Title
created: YYYY-MM-DD
updated: YYYY-MM-DD
type: entity | concept | comparison | query | summary
tags: [from taxonomy below]
sources: [raw/articles/source-name.md]
confidence: high | medium | low
contested: true
contradictions: [other-page-slug]
---
```

## Tag Taxonomy
- Construction: construction-methods, ramp-theory, geopolymer, transport, quarrying, casing
- Structure: internal-structure, chambers, shafts, voids, grand-gallery, relieving-chambers
- Dating: radiocarbon, osl-dating, chronology, old-wood-problem, astronomical-dating
- Geology: bedrock, nile-branch, erosion, plateau-geology
- Astronomy: stellar-alignment, shaft-alignments, precession, solar-function
- Complex: sphinx, khafre-pyramid, menkaure-pyramid, causeway, boat-pits, osiris-shaft
- Traditions: hermetic, occult, arabic-medieval, initiation
- People: khufu, snefru, hemiunu, lehner, houdin, davidovits, gantenbrink, malanga-biondi
- Technology: muon-tomography, sar-radar, gravimetry, gpr
- Meta: controversy, evidence-summary, open-questions, evolution-timeline

## Page Thresholds
- **Create a page** when an entity/concept appears in 2+ sources OR is central to one source
- **Add to existing page** when a source mentions something already covered
- **DON'T create a page** for passing mentions, minor details, or things outside the domain
- **Split a page** when it exceeds ~200 lines — break into sub-topics with cross-links
- **Archive a page** when content is fully superseded — move to `_archive/`, remove from index

## Entity Pages
One page per notable entity (person, structure, site). Include overview, key facts/dates, relationships via [[wikilinks]], source references.

## Concept Pages
One page per concept or topic. Include definition, current state of knowledge, open questions, related concepts via [[wikilinks]].

## Comparison Pages
Side-by-side analyses. Include what is compared and why, dimensions (table format preferred), verdict/synthesis, sources.

## Update Policy
When new information conflicts with existing content:
1. Check dates — newer sources generally supersede older ones
2. If genuinely contradictory, note both positions with dates and sources
3. Mark contradiction in frontmatter: `contradictions: [page-name]`
4. Flag for user review in the lint report
