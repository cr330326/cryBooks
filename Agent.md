# Personal LLM Wiki Agent Schema

This file is the agent-facing entrypoint for the personal LLM Wiki in this folder.

Follow the full schema in `CLAUDE.md`. It defines the directory layout, page conventions, and the required workflows for:

- ingesting new raw sources into the persistent wiki,
- answering questions from the accumulated wiki,
- running health checks and maintenance passes.

## Quick Start

1. Read `CLAUDE.md`.
2. Read `wiki/index.md`.
3. Read recent activity with:
   `rg "^## \\[" wiki/log.md | tail -10`
4. For new sources, start from `raw/_inbox/` unless the user names a specific file.
5. Never modify `raw/` unless the user explicitly asks.
6. Maintain `wiki/index.md` and `wiki/log.md` whenever wiki content changes.

## Agent Defaults

- Use `rg` for search.
- Use Obsidian links for wiki pages: `[[Page Name]]`.
- Cite sources with wiki page links and raw file paths.
- Prefer small, incremental wiki edits that compound over time.
- When uncertain, write the uncertainty down rather than hiding it.

