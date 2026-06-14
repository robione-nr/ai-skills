---
name: write-code
description: Use when writing or editing code and the user asks for good practices, clean implementation, maintainability, conventions, style, or code quality.
---

## Operating Environment
- Refer to `operational-environment.md`.

## Workflow

1. Read nearby code before editing.
2. Follow the project and language conventions already present.
3. Keep changes scoped to the request.
4. Prefer clear, boring code over clever code.
5. Validate with the smallest useful test, compile check, linter, or manual inspection available.

## Rules

- Match the indentation conventions of existing files.
- Indentation in newly created files will be horizontal tabs unless *forbidden* by the language.
- Follow naming conventions by language and project:
  - Python: `snake_case` functions/variables, `PascalCase` classes, `UPPER_SNAKE_CASE` constants.
  - JavaScript/TypeScript: `camelCase` variables/functions, `PascalCase` classes/components/types.
  - Go: `camelCase` or `PascalCase` by export status; short names only when idiomatic.
  - Shell: lower snake case for functions/locals unless existing style differs.
- Prefer existing formatter/linter rules over personal style.
- Inline short functions used once when inlining improves readability.
- Keep helper functions when they remove duplication, clarify a complex step, isolate side effects, or are likely to be reused.
- Use language-native constants instead of magic values.
- Use macros or `#define` only when idiomatic and safer than alternatives.
- Keep functions focused. Split when a function mixes unrelated concerns.
- Group related code into logical units.
- Add one short comment before a non-obvious logical unit.
- Do not comment what a single lines.
- Prefer structured parsing/APIs over ad hoc string manipulation.
- Preserve user changes. Do not rewrite unrelated code.

## Comments

Use comments like signposts:

```python
# Normalize Scweet output before selecting cards.
```

Avoid comments like narration:

```python
# Set x to 1.
```

## Output

Return code that:

- Fits the surrounding style.
- Is easy to scan.
- Has minimal new abstraction.
- Handles expected errors directly.
- Leaves unrelated files and behavior alone.
