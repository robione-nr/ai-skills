---
name: operational-environment
description: Use when working on Nolan's local/VPS projects, deployment scripts, plain PHP/JS/CSS sites, Python utilities, MySQL work, git workflows, or environment-sensitive tasks.
---

## Environment

Local working directory:

```text
/home/nolan/projects
```

Local:

- Ubuntu 24.04.4
- PHP 8.3.6
- Python 3.12.3
- Apache 2.4.58

VPS:

- Ubuntu 22.04
- PHP 8.1.2
- MySQL Server 8.0.46
- Python 3.10.12
- Apache 2.4.52
- Certbot 5.6.0

VPS access:

- Git global identity is configured.
- GitHub username: `robione-nr`.
- User creates Github repos and sets licenses.
- For privileged VPS details, read `operational-secrets.md` only when the task involves SSH, root ownership, cron, deployment permissions, or remote git auth.

## Filesystem

- Local `VPS` mount uses `sshfs` to remote `/var/www`.
- Only operate on files visible in the workspace.
- Files outside the workspace are out of scope unless the user provides contents or asks for commands.
- I will ask the user for information within these files when it facilitates troubleshooting issues.
- Secret files inside the workspace may be edited when relevant.

Current VPS web layout:

```text
/var/www/[function]/[domain]
```

Planned VPS web layout:

```text
/var/www/[domain]/[function]
```

Do not restructure this layout unless explicitly asked. The user will perform the restructure.

## Python

- Use `python3` and `pip`.
- **Always use `.venv` per project/script.**
- Do not rely on system Python packages for project dependencies.
- Remember VPS Python is 3.10.12; avoid newer-only syntax/APIs unless compatibility is checked.

## Web Code

- No frameworks by default.
- PHP, CSS, ECMAScript is plain.
- Prefer simple, readable files over build systems unless the project already has one.

## Database

- MySQL lives on VPS only.
- The usual pattern is to create SQL/schema changes for the user to execute.
- Do not assume direct DB access.
- After repos and directory layout are ready, use branch-based workflow for all changes, including DB-adjacent files.

## Git

- Use branch workflow when repos are available:
  1. Create a branch.
  2. Make scoped changes.
  3. Validate.
  4. Commit.
  5. Merge as appropriate.
- Include `(Codex)` in commit messages.
- The user handles actions outside accessible files or permissions.
- Known local repo roots:
  - `VPS/repo/portfolio` -> `git@github.com:robione-nr/portfolio.git`
  - `VPS/nolan-robidoux.name/html/endpoint/health` -> `git@github.com:robione-nr/endpoint-biometrics.git`
  - `VPS/scripts/common/python/utility-server` -> `git@github.com:robione-nr/utility-server.git`

Please refer to `operational-secrets.md` for further environmental context.
