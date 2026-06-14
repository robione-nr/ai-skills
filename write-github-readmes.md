---
name: write-github-readmes
description: Use when creating or improving GitHub repository README.md files for scripts, CLIs, libraries, services, apps, personal utilities, or project portfolios.
---

## Workflow

1. Inspect the repository before writing.
2. Identify what the project actually is: audience, entry points, commands, configuration, tests, deployment, and important files.
3. Decide the README shape from the project, not from a fixed template.
4. Preserve useful existing content when updating a README.
5. Write concrete commands and examples only when supported by the repo.
6. Validate paths, commands, and claims when practical.

## Rules

- Do not invent features, badges, screenshots, install steps, configuration, roadmap items, or support promises.
- Do not force install/configure sections onto personal or one-off repos that are not meant to be drop-in tools.
- Do not add license text or a license section just because READMEs often have one.
- Prefer a short purpose statement near the top.
- Prefer practical commands over prose when commands exist.
- Prefer a lightweight structure for personal scripts, notes, experiments, and internal tools.
- Use fuller onboarding sections only for reusable projects that someone else can install, run, or integrate.
- Mention uncertainty directly when behavior cannot be verified from the repo.
- Keep marketing language out unless the repo is product-facing.

## Shape

Choose only the sections that fit:

- Title
- Short purpose or status
- What it does
- Requirements
- Setup or installation
- Usage
- Configuration
- Examples
- Verification or tests
- Deployment or operations
- Project structure
- Notes, limitations, or maintenance reminders

For personal utilities, prefer:

- What this is
- How I use it
- Important files
- Commands, if any
- Notes or caveats

For reusable tools, prefer:

- What it solves
- Requirements
- Install or setup
- Usage examples
- Configuration
- Tests or verification

## Output

Return a README that:

- Matches the project maturity and intended audience.
- Uses accurate repo-specific details.
- Is easy to scan on GitHub.
- Avoids boilerplate that does not help this repo.
