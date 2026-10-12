# Vault Index

Entry points. Notes live in the subfolders.

- Sources: `sources/`
- Concepts: `concepts/`
- Scratch notes: `scratch-notes/`
- Meeting notes: `meetings/`

## ID scheme
- Sources: citekey `<name><year><title>` (e.g. `bernstein2017pqc`)
- Concepts: kebab-case (e.g. `ml-dsa`), aliases under `aliases`

## Frontmatter
```yaml
---
id: <see ID scheme>
type: "..."
aliases: []
tags: []
cites: [] # ids this note relies on
used_in: [] # ids/chapters that use this note
---
```