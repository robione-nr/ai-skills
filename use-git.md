---
name: use-git
description: Use when working with git repositories, including status checks, init, clone, remotes, fetch, pull, rebase, merge conflicts, commits, pushes, tags, or preserving local work.
---

## Workflow

1. Run `git status --short --branch` before changing git state.
2. Identify the repo root with `git rev-parse --show-toplevel` when path scope is unclear.
3. Inspect remotes with `git remote -v` before fetch, pull, or push.
4. Fetch before integrating remote history.
5. Prefer local commits before rebasing or merging unrelated remote history.
6. Resolve conflicts by editing files, then `git add` and `git rebase --continue` or `git merge --continue`.
7. Run `git status --short --branch` before final push or final instructions.

## Rules

- Preserve local work.
- Do not run destructive commands unless the user explicitly asks.
- Do not use `git reset --hard`, `git checkout --`, or `git clean` casually.
- Prefer `git fetch` before `git pull`.
- Prefer rebase for a local-first repo when adding work on top of a small existing remote.
- Use merge when preserving branch topology matters.
- Keep commits focused and messages clear.
- Include required user-requested message tags exactly.
- Check ignored files before committing secrets, local config, virtualenvs, caches, or logs.
- Treat push failures as information: fetch, inspect, integrate, then push.

## Common Commands

```bash
git status --short --branch
git remote -v
git fetch origin
git log --oneline --decorate --all --max-count=10
git diff --stat
git add .
git commit -m "Message"
git pull --rebase origin main --allow-unrelated-histories
git push -u origin main
```

## Conflict Handling

1. Run `git status`.
2. Open each conflicted file.
3. Remove conflict markers: `<<<<<<<`, `=======`, `>>>>>>>`.
4. Keep the intended final content.
5. Run `git add <file>`.
6. Continue with `git rebase --continue` or `git merge --continue`.
7. Push only after the rebase or merge finishes.

## Output

Return:

- Current branch and remote state.
- Commit hash and message when a commit is made.
- Push result when a push is made.
- Any files that need user action.
