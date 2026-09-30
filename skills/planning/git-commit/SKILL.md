---
name: git-commit
description: Prepare focused Git commits using Conventional Commit messages. Use when the user asks to stage or commit work, split changes into commits, or choose a commit message; do not push, amend, or rewrite history unless explicitly requested.
---

# Git Commit

Create an accurate, reviewable commit that reflects the user's intended scope. First inspect the working tree, staged diff, branch, and relevant recent commit style. Identify unrelated, generated, or pre-existing changes and preserve them unless the user includes them.

Group changes by independently understandable purpose. If the requested scope contains unrelated work, propose separate commits. Do not split a tightly coupled change merely to make commits smaller.

Use Conventional Commit subjects:

```text
type(optional-scope): imperative summary
```

Choose the narrowest accurate type: `feat`, `fix`, `docs`, `test`, `refactor`, `chore`, `ci`, or `build`. Keep the subject concise and imperative. Add a body only when the why, trade-offs, migration, compatibility, or breaking behavior needs durable context.

Before committing:

1. Stage only the files in the approved logical change.
2. Inspect the staged diff and verify that no secrets, generated output, or unrelated edits are included.
3. Run relevant lightweight validation when it is available and proportionate to the change.

Report the commit hash, subject, changed files, and validation status after committing. Do not push, amend, force-push, reset, rebase, or discard changes unless the user explicitly authorizes that action.
