---
name: write-skills
description: Use when creating or improving concise AI skills, agent instructions, reusable workflows, or task-specific operating guides.
---

# Write Skills

Create short, practical skills that teach an AI how to do one kind of work better.

## Goal

A skill should answer:

- When should this be used?
- What should the AI do?
- What should the AI avoid?
- What files, tools, examples, or references matter?

Do not explain obvious things. Assume the AI is capable. Add only the context that changes behavior.

## Shape

Use this structure unless there is a good reason not to:

```md
---
name: short-hyphen-name
description: Use when...
---


## Workflow

1. First action
2. Second action
3. Validation or output step

## Rules

- Strong preference
- Hard constraint
- Common failure to avoid

## Output

Describe the expected final result.
```

## Writing Rules

- Be direct and brief.
- Prefer commands over commentary.
- Prefer bullets over paragraphs.
- Keep examples tiny.
- Remove background unless it changes decisions.
- Do not include setup docs, changelogs, or user-facing README content.
- Put fragile exact steps in numbered lists.
- Put optional judgment in bullets.
- Name files and paths exactly when they matter.
- *Exclude* motivational speech, generic advice, secrets.
- *Include* constraints the AI cannot infer, local conventions, required commands, known failures.

## Good Descriptions

The `description` is the trigger. Make it specific.

Good:

```yaml
description: Use when creating or updating Certbot deploy hooks that reload services and send ntfy notifications.
```

Weak:

```yaml
description: Helps with scripts.
```

## Validation

Before calling a skill done:

- Check the trigger description matches real user phrasing.
- Check every instruction changes behavior.
- Check the skill does not hide essential steps in prose.
- Check paths, commands, and filenames are accurate.
- Delete anything merely nice to know.

## Bias

Short wins. Specific wins. A skill is not documentation; it is operational memory.
