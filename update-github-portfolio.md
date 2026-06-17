---
name: update-github-portfolio
description: Use when updating Nolan's GitHub portfolio repo with project cards, public repository links, private-project detail pages, screenshots, videos, or GitHub-flavored Markdown project summaries.
---

## Workflow

1. Inspect `VPS/repo/portfolio` before editing.
2. Follow the repo's existing Markdown, asset, and naming patterns.
3. If the repo is blank or thin, use a GitHub-native structure:
   - `README.md` for the portfolio index.
   - `projects/[app].md` for private or larger project detail pages.
   - `assets/[app]/` for screenshots, thumbnails, and media assets.
4. Classify each project as public or private.
5. Match the amount of detail to project scope, maturity, and visibility.
6. Place true flagship work in `Featured Projects`.
7. Place useful recent work that is not flagship-level in `Recent Work`.
8. Validate links, image paths, headings, and Markdown rendering assumptions.

## Rules

- Use GitHub-flavored Markdown unless the repo already uses another system.
- Use small amounts of GitHub-supported HTML only when it improves screenshots, grids, collapsible details, or linked media.
- Use shields.io badges for compact visibility and status labels when the portfolio already uses badges.
- Avoid red badges; use orange only for caution/warning states.
- Do not add a framework, build system, or renderer unless the user asks.
- Do not duplicate full public repo READMEs in the portfolio.
- Do not expose secrets, private URLs, client names, operational details, or sensitive screenshots.
- Prefer concise portfolio copy over implementation documentation.
- Preserve the user's voice: practical, direct, personal, not corporate.
- Keep project names, slugs, image paths, and links stable.
- Track dates when useful for ordering and recency.
- Do not add status lines unless they explain something useful.

## Ordering

- Use `Featured Projects` for significant or flagship work.
- Use `Recent Work` for new, useful, or active projects that are not necessarily significant.
- Put new projects in `Featured Projects` only when they already show likely flagship potential.
- Keep a compact `Project Index` for completeness.
- A project may appear in a section card and in the index.
- Prefer significance over chronology inside `Featured Projects`.
- Prefer recency inside `Recent Work`.
- Include a date field or visible date only when the portfolio structure needs it.
- If adding dates, prefer stable project metadata:
  - `created`
  - `updated`
  - `featured`
  - `status`
- Do not let old but important projects sink below minor recent work.

## Status Labels

- Include a compact `Status` column in project index tables.
- Keep status labels very short so tables stay readable.
- Use labels such as:
  - M.V.P.
  - Stable
  - W.I.P.
  - Paused
  - Archive
  - Demo
- Do not label a project significant just because it is useful or recent.

## Public Projects

- Add or update a card in the portfolio index.
- Link the card to the public GitHub repo.
- Include a one- or two-sentence summary focused on what the project is and why it matters.
- Include a screenshot only if it clarifies the project quickly.
- Create a detail page only if the user requests one or the project needs portfolio-specific context.
- Put public projects in `Recent Work` when they are useful and current but not flagship work.

## Private Projects

- Add or update a card in the portfolio index.
- Create or update `projects/[app].md`.
- Link the card to the local detail page.
- Explain enough for a visitor who cannot access the repo:
  - what it is
  - who it is for
  - what problem it solves
  - notable workflows, architecture, or tradeoffs
  - screenshots or video links when useful
- Keep implementation detail high-level unless the user asks for depth.

## Bigger Projects

Use richer detail pages when the project warrants it:

- Overview
- Problem or motivation
- Features
- Screenshots
- Demo video or linked thumbnail
- Architecture or workflow notes
- Tradeoffs
- Status or next steps

For screenshot grids, prefer simple Markdown images first. Use an HTML table only when a grid is clearer.

## Output

Return portfolio updates that:

- Render cleanly on GitHub.
- Make public projects easy to open on GitHub.
- Make private projects understandable without repo access.
- Keep assets organized under `assets/[app]/`.
- Leave unrelated portfolio content alone.
