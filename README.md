# Claude Interrogate Runtime
Updated: 2026-04-08

This directory is the distribution payload for the installable Claude Code plugin.

Contents:

- `plugins/claude-interrogate/` installable plugin payload
- `runtime/dist/` built MCP server runtime
- `.agents/plugins/marketplace.json` marketplace metadata

Current command surface:

- `/claude-interrogate:interrogate <concept> [docs-dir]`
- `/claude-interrogate:interrogate-easy <concept> [docs-dir]`
- `/claude-interrogate:interrogate-fast <concept> [docs-dir]`
- `/claude-interrogate:interrogate-hard <concept> [docs-dir]`
- `/claude-interrogate:reinterrogate <doc-path> [docs-dir]`
- `/claude-interrogate:distill <concept> [docs-dir]`
- `/claude-interrogate:distill-hard <concept> [docs-dir]`
- `/claude-interrogate:extricate <concept> [docs-dir]`
- `/claude-interrogate:trace <concept> [docs-dir]`
- `/claude-interrogate:convert <source> [docs-dir]`
- `/claude-interrogate:summarize <concept> [docs-dir]`
- `/claude-interrogate:audit-docs [docs-dir]`
- `/claude-interrogate:sync-docs [docs-dir]`

Install from the plugin marketplace inside Claude Code:

```text
/plugin marketplace add michael-tiller/claude-interrogate
/plugin install claude-interrogate
```

Repository:

- https://github.com/michael-tiller/claude-interrogate

Notes:

- `summarize` is read-only and does not interrogate or write.
- `trace` is read-only structural mapping of authority, dependencies, and drift.
- `distill` writes a separate exploratory artifact only when explicitly requested; it does not replace the canonical spec.
- `convert` is for controlled promotion or transformation between doc forms.
- `extricate` is for dependency-aware removal, retirement, or replacement planning.
- `reinterrogate` is for modernizing an existing spec against newer sibling knowledge.
