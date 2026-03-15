# CLAUDE.md

This file is the primary memory and instruction set for AI assistants working in this repository.
Keep it up to date as the project evolves — treat it as living documentation.

---

## Project Overview

<!-- TODO: Replace with a 1–3 sentence description of what this project does and who it's for. -->

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

## Development Commands

<!-- TODO: Fill in the actual commands for this project once a tech stack is chosen. -->

| Task        | Command             |
|-------------|---------------------|
| Install     | `<command>`         |
| Dev server  | `<command>`         |
| Build       | `<command>`         |
| Test        | `<command>`         |
| Lint        | `<command>`         |
| Format      | `<command>`         |
| Type check  | `<command>`         |

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

## Slash Commands

These live in `.claude/commands/` and are available as `/command-name` in Claude Code.

| Command            | Purpose                                                      |
|--------------------|--------------------------------------------------------------|
| `/code-simplifier` | Reviews changed code for over-engineering and cleans it up  |
| `/verify-app`      | Runs a structured end-to-end verification of the app        |

---

## Permissions & Safe Commands

Pre-approved commands (no confirmation prompt) are listed in `.claude/settings.json`.

**Always pre-approved:**
- All `git` operations
- `npm/yarn/pnpm install`, `npm run *`, `npm test`
- `pip install`, `pytest`, `ruff`, `mypy`, `black`
- `cargo build/test/clippy/fmt`
- `go build/test/vet/fmt`
- `make *`, `ls`, `cat`, `echo`, `which`, `pwd`

**Always denied (will always prompt):**
- `rm -rf *` — destructive file removal
- Piping downloads directly into a shell (`curl | bash`)
- `sudo` — privilege escalation
- Writing to `/etc/`

---

## Code Conventions

<!-- TODO: Update this section as conventions are established for your specific project. -->

- **Language**: Currently no source language (add yours here)
- **Formatting**: Use the formatter for your language (Prettier, Black, rustfmt, gofmt, etc.)
- **Commit style**: Concise imperative subject line, e.g. `Add login endpoint`
- **Branch naming**: `feature/<slug>`, `fix/<slug>`, `chore/<slug>`
- **PRs**: Keep them small and focused; one concern per PR

---

## Architecture Notes

<!-- TODO: Describe key architectural decisions, patterns, and constraints once the project grows. -->

*No architecture to document yet.*

---

## External Integrations

<!-- TODO: List MCP tools, APIs, and services Claude can interact with. -->

| Tool    | Purpose          | Config              |
|---------|------------------|---------------------|
| *(none yet)* | —           | —                   |

To add MCP integrations (Slack, Sentry, BigQuery, etc.), add them to `.mcp.json` at the root.

---

## Team Notes & Gotchas

<!-- Add hard-won lessons here. This is the "don't forget" section. -->

- This file should be updated as part of every PR that changes conventions or architecture.
  Tag `@.claude` in code reviews to keep it current automatically.
- Do not use `--dangerously-skip-permissions`; pre-approve safe commands in `.claude/settings.json` instead.

---

*Last updated: 2026-03-15*
