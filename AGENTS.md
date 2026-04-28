# AGENTS.md

This file applies to `repositories/Personal/free-code`.

## Shared Agent Rules

- Start from the smallest useful context and avoid broad scans unless the task requires them.
- Prefer official documentation and primary sources for research; use secondary sources only when official sources are insufficient.
- Prefer small, targeted, verifiable changes; do not assume tooling from another repo applies here.
- Prefer committed scripts and documented commands; inspect README or manifests only when needed to discover commands.
- Do not commit, push, amend, run destructive git commands, or revert user changes unless explicitly requested.
- Avoid touching secrets, credentials, generated files, vendor code, caches, or virtual environments unless the task requires it.
- Use the narrowest verification command that proves the change.
- Prefer Docker or the documented container runtime for verification; for Python repos with a repo-managed `.venv`, use that `.venv` instead of system Python or system `pip`.
- Never install libraries, packages, or dependencies on the host machine just to test or verify.
- Do not fall back to host-side tests or typechecks; if no supported container/runtime or repo-managed `.venv` exists, stop and report the blocker.
- For docs-only changes, inspect the file and diff instead of inventing tests.
- For script changes, validate syntax before behavior checks.
- When fixing a bug, add or run the narrowest practical regression test.
- Default to ASCII, match surrounding style, and avoid repo-wide formatting in focused tasks.
- Add comments only when intent is not obvious, use clear stable names, validate external input at boundaries, fail fast with specific errors, and never log secrets.
- Keep documentation concise and update local rules/docs when adding commands or tools.

## Maintenance

- Replace this minimal guide with repo-specific command, test, and architecture guidance when needed.
- Keep any tool-specific adapters aligned with this file instead of duplicating divergent rules.
