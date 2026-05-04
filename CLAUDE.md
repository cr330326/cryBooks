# Personal LLM Wiki Schema

This repository is a personal reading knowledge base based on Andrej Karpathy's LLM Wiki pattern. The agent maintains a persistent, interlinked Markdown wiki from immutable raw sources.

## Operating Principles

- Treat `raw/` as source of truth. Read from it, never rewrite, rename, delete, or annotate raw files unless the user explicitly asks.
- Treat `wiki/` as the maintained knowledge layer. The agent may create and edit wiki pages, indexes, logs, templates, and health reports.
- Prefer durable wiki updates over one-off chat answers. If a query produces reusable synthesis, offer to file it under `wiki/questions/` or `wiki/syntheses/`.
- Every factual claim in the wiki should point back to at least one source page or raw source path.
- Preserve uncertainty. Mark weak evidence, contradictions, stale claims, and open questions explicitly.
- Use Obsidian-style links: `[[Page Name]]`. Use relative Markdown links for files outside normal wiki pages, especially raw source paths.
- Keep filenames readable and stable. Use Chinese titles when the source/domain is Chinese; avoid renaming established pages without user approval.

## Directory Layout

```text
raw/
  _inbox/        New sources waiting to be ingested.
  assets/        Local images and attachments captured from sources.
  ...            Existing curated books, reports, articles, papers.

wiki/
  index.md       Content catalog and main navigation file.
  log.md         Append-only chronological operation log.
  00-overview.md Current high-level map of the knowledge base.
  sources/       One page per ingested source.
  concepts/      Concepts, ideas, theories, methods.
  entities/      Organizations, products, systems, projects.
  people/        Authors, researchers, historical figures.
  works/         Books, papers, reports, courses, talks.
  questions/     Filed answers to user questions.
  syntheses/     Cross-source analysis, comparisons, arguments.
  contradictions/ Explicit conflicts or disputed claims.
  health/        Wiki lint and maintenance reports.
  _templates/    Page templates and workflow scaffolds.
```

## Page Frontmatter

Use YAML frontmatter for wiki pages when creating or substantially revising them:

```yaml
---
type: source|concept|entity|person|work|question|synthesis|contradiction|health
status: seed|draft|reviewed|stale
created: YYYY-MM-DD
updated: YYYY-MM-DD
sources:
  - raw/path/or/wiki/source-page.md
tags:
  - topic/example
---
```

## Source Page Format

Each ingested source gets one page under `wiki/sources/` unless it is a major work that deserves a `wiki/works/` page plus chapter/source pages.

Required sections:

- `# Title`
- `## Source`
- `## One-Line Summary`
- `## Key Ideas`
- `## Useful Details`
- `## Links To Update`
- `## Contradictions Or Tensions`
- `## Open Questions`

## Ingest Workflow

Use this when the user says to ingest, process, summarize into the wiki, or handle files in `raw/_inbox/`.

1. Identify source files and confirm scope if more than 5 sources are involved.
2. Read/extract source content with the best available local tool. For binary files, extract text first; for images, inspect relevant images separately.
3. Decide the wiki targets before editing: source page, related concepts, entities, people, works, syntheses, contradictions.
4. Create or update the source page in `wiki/sources/`.
5. Update existing topic pages touched by the source. Add new concept/entity/person/work pages only when the idea will likely recur.
6. Add backlinks from new pages to related pages using `[[Page Name]]`.
7. Record contradictions in the affected page and, if significant, create/update `wiki/contradictions/<slug>.md`.
8. Update `wiki/index.md` with new or changed pages.
9. Append to `wiki/log.md` using this parseable heading:
   `## [YYYY-MM-DD] ingest | Source Title`
10. End with a concise report: source processed, pages created, pages updated, uncertainties, and suggested next ingest/query.

## Query Workflow

Use this when the user asks a question against the knowledge base.

1. Read `wiki/index.md` first.
2. Search `wiki/` with `rg` for relevant names, phrases, and aliases.
3. Read the most relevant wiki pages before raw files. Use raw files only to verify or deepen a claim.
4. Answer with citations to wiki pages and raw source paths where useful.
5. Distinguish established wiki synthesis from fresh inference made during this answer.
6. If the answer is reusable, create or update a page in `wiki/questions/` or `wiki/syntheses/` after confirming or when the user asks to file it.
7. Append a query entry to `wiki/log.md` when a durable page is created or important synthesis changes:
   `## [YYYY-MM-DD] query | Question`

## Health Check Workflow

Use this when the user asks to lint, audit, check health, clean up, or maintain the wiki.

1. Read `wiki/index.md` and recent entries in `wiki/log.md`.
2. Check for orphan wiki pages with few or no links.
3. Check for pages missing frontmatter, source references, or update dates.
4. Search for markers: `TODO`, `TBD`, `unclear`, `needs source`, `stale`, `contradiction`.
5. Identify important repeated terms that lack pages.
6. Identify contradictions, stale claims, duplicate pages, and broken links.
7. Write a dated report under `wiki/health/YYYY-MM-DD-health-check.md`.
8. Apply low-risk fixes directly: index updates, missing backlinks, obvious template/frontmatter repairs.
9. Ask before broad rewrites, source interpretation changes, or page renames.
10. Append a log entry:
    `## [YYYY-MM-DD] health | Scope`

## Quality Bar

- A useful page is concise, linked, sourced, and easy to revise.
- Prefer synthesis over extractive summaries, but never erase source nuance.
- Do not over-page the wiki. Create pages for durable concepts, entities, people, works, and recurring questions.
- Keep `wiki/index.md` useful at human scale: one-line summaries beat exhaustive metadata.
- Keep `wiki/log.md` append-only. Correct mistakes in a new note instead of rewriting history.

