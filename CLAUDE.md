# CLAUDE.md

This file is the primary memory and instruction set for AI assistants working in this repository.
Keep it up to date as the project evolves — treat it as living documentation.

---

## Project Overview

**Elias-Lilla-Test-grej** is currently a minimal template/placeholder repository used for testing
git workflows. No production application code exists yet.

---

## Repository Structure

```
.
├── .claude/
│   ├── settings.json          # Pre-approved shell commands (no prompts for safe ops)
│   └── commands/
│       ├── code-simplifier.md # /code-simplifier — clean up code after implementation
│       └── verify-app.md      # /verify-app     — end-to-end verification checklist
├── CLAUDE.md                  # This file
└── Elias-testfil.txt          # Original test file
```

---

## Workflow

### Starting a Session

1. Open in **Plan mode** (Shift+Tab twice in Claude Code) for any non-trivial task
2. Discuss and refine the plan before switching to implementation mode
3. Use **auto-accept edits** mode once the plan is solid

### During Implementation

- Run `/verify-app` to confirm the feature works before calling it done
- Run `/code-simplifier` after implementation to clean up any over-engineering

### Finishing a Session

1. Verify all tests pass
2. Run `/code-simplifier` for a final cleanup pass
3. Commit with a clear, descriptive message
4. Push and open a PR

---

## Code Conventions

<!-- TODO: Update this section as conventions are established for your specific project. -->

- **Language**: Currently no source language (add yours here)
- **Formatting**: Use the formatter for your language (Prettier, Black, rustfmt, gofmt, etc.)
- **Commit style**: Concise imperative subject line, e.g. `Add login endpoint`
- **Branch naming**: `feature/<slug>`, `fix/<slug>`, `chore/<slug>`
- **PRs**: Keep them small and focused; one concern per PR

---

## Team Notes & Gotchas

<!-- Add hard-won lessons here. This is the "don't forget" section. -->

- This file should be updated as part of every PR that changes conventions or architecture.
  Tag `@.claude` in code reviews to keep it current automatically.
- Do not use `--dangerously-skip-permissions`; pre-approve safe commands in `.claude/settings.json` instead.

---

*Last updated: 2026-03-15*
