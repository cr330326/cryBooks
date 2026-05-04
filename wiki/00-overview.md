---
type: synthesis
status: seed
created: 2026-05-04
updated: 2026-05-04
sources:
  - llm-wiki.md
tags:
  - meta/wiki
---

# Reading Knowledge Base Overview

This wiki is the maintained knowledge layer for the reading collection in `raw/`.

The current goal is to turn books, papers, reports, articles, and notes into a persistent, interlinked Markdown wiki. Raw files remain immutable. The agent gradually builds source summaries, concept pages, entity pages, people pages, work pages, question answers, and cross-source syntheses.

## Current Structure

- `raw/` stores source material.
- `raw/_inbox/` stores new material waiting for ingest.
- `wiki/sources/` stores one page per ingested source.
- `wiki/concepts/`, `wiki/entities/`, `wiki/people/`, and `wiki/works/` store reusable knowledge pages.
- `wiki/questions/` stores durable answers to user questions.
- `wiki/syntheses/` stores cross-source analysis.
- `wiki/contradictions/` tracks conflicting claims.
- `wiki/health/` stores maintenance reports.

## Current Status

The wiki scaffold exists, but no raw source has been fully ingested yet.

## Good First Ingests

- A single Markdown article from `raw/AI/Article/`.
- A single AI report or paper from `raw/AI/报告/` or `raw/论文/`.
- One book chapter or extracted note from a larger book.

