# Per-Project Volta Catalog

Per Round 2 M3, the Volta catalog moved from `~/.volta/` (user-global) to `<project>/.volta/` (per-project).

## Status
🟡 **Placeholder** — directory exists; the actual catalog migration (execution-path item 4) is pending in Volta.

## Expected layout (when migration ships)
```
.volta/
├── catalog.db          # SQLite — assets, dependencies, approvals, cost telemetry
├── cache/              # gitignored — Meshy / ComfyUI / mesh outputs
├── renders/            # gitignored — preview MP4s, turntables
└── manifest.json       # human-readable catalog summary
```

## Volta init (when wired)
```
volta init           # bootstraps .volta/ in cwd
volta import-references  # ingests ../concept/inventory.json as REFERENCE-tier
```
