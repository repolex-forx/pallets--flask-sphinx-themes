# Repolex Knowledge Graph of pallets/flask-sphinx-themes

RDF knowledge graph data for [pallets/flask-sphinx-themes](https://github.com/pallets/flask-sphinx-themes), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [rlex](https://github.com/repolex-ai/rlex) query tool:

```bash
cargo install --git https://github.com/repolex-ai/rlex
```

Verify the install:

```bash
rlex --help
```

**rlex is designed to be used primarily by LLMs in a terminal.** Start up your favorite AI assistant and ask it to use rlex. It handles the SPARQL — you just ask questions in plain English.

To load this repo's data:

```bash
rlex download pallets/flask-sphinx-themes
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 3d562d0f6869f4a1845f8c68cdbcd0139d1e0bbf
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 3d562d0f6869f4a1845f8c68cdbcd0139d1e0bbf
│           └── chunk-001.nq.gz
├── blob
│   ├── 0c1b3fdab5deda4275622b2444e253c8a75b6935.nq.gz
│   ├── 2329b0d4774cf8a3ff178e78c4728bf32215f2e5.nq.gz
│   ├── 390e395562392a95e337cf05005eae621b6d710f.nq.gz
│   ├── 6b4c771eeeaa32545931cab1496786626db6bea1.nq.gz
│   ├── 7761bfb43b626cdb9e8690b1386c74de196dce09.nq.gz
│   ├── 8daab7ee6efe3b6f3c2a2594b711e7a9026eb5e2.nq.gz
│   ├── a1ccca7c7b2c781c0fa96338866f9ded386de904.nq.gz
│   ├── b0c226357463ba71fb7cd03627292c9d8bab5400.nq.gz
│   ├── b43b19d54979e0ee95d83b761c905ca489f466d4.nq.gz
│   ├── e38950d572b87fb065d6d5c088e0eb83b4aeaf62.nq.gz
│   ├── f97c9d17db2c60f8b1cdc43753e5568a720c2bc1.nq.gz
│   └── ff6b757f66f7503a6e661e4283592e8d88fb77ae.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 3d562d0f6869f4a1845f8c68cdbcd0139d1e0bbf.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 20 files
```

| Directory | What it contains |
|-----------|-----------------|
| `blob/` | Per-file AST graphs, content-addressed by git blob SHA. Each file in the source repo gets its own graph. |
| `aggregate/ast/` | Combined AST graph per parsed commit. Merges all blob graphs for a snapshot of the entire codebase at that point. |
| `aggregate/lsp/` | Language Server Protocol enrichment: resolved symbols, definitions, references, and type information. |
| `aggregate/dataflow/` | Interprocedural data flow edges between functions and modules. |
| `aggregate/repolex/` | Combined graph (AST + LSP + dataflow) per commit. |
| `commit/` | Git commit metadata (author, date, message, parent links). |
| `branch/` | Branch metadata. |
| `tag/` | Tag metadata. |
| `filetree/` | File tree snapshots per commit (which files existed and their blob SHAs). |
| `audit/` | Code architecture and graph audit reports per commit. |

## Source repository

[pallets/flask-sphinx-themes](https://github.com/pallets/flask-sphinx-themes)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
