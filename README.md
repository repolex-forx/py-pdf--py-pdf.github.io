# Repolex Knowledge Graph of py-pdf/py-pdf.github.io

RDF knowledge graph data for [py-pdf/py-pdf.github.io](https://github.com/py-pdf/py-pdf.github.io), parsed by [repolex](https://repolex.ai).

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
rlex download py-pdf/py-pdf.github.io
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 5aa20d2fcdf6edc65ba142f8554d25865336e174
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 5aa20d2fcdf6edc65ba142f8554d25865336e174
│           └── chunk-001.nq.gz
├── blob
│   ├── 1165a569b7b09b0915ff447c250f6259cd96011b.nq.gz
│   ├── 17185c36f26566d4dc21b76bc2011898860a0155.nq.gz
│   ├── 1ca257ef611a22d906d675dbc0634d8ffa1bfa88.nq.gz
│   ├── 371cfe355dd3e241cbd73707957e299ddef5bc4c.nq.gz
│   ├── 5e3eddef0694c5d6d674cf6219dc0656cfbd2751.nq.gz
│   ├── 69e3d1ebb59a6ba3af066b2ca90d43c0be4865ae.nq.gz
│   ├── 8c7f6c2be44b791e9334a8742844373f4caef713.nq.gz
│   ├── 90f2d78046f66953c8a628a502438075d16125d2.nq.gz
│   ├── 97358baec56d2a0beb8d41a59d2dd078059e401c.nq.gz
│   ├── a4b5d1a6c13e48548115f7dcddfc1c4d93c3bbd9.nq.gz
│   ├── b364f0697ca7aa903f68882dda706e1f8300038c.nq.gz
│   ├── ba210b72b65238f0948659cfdcb4d5ee5cf00a8b.nq.gz
│   ├── c496cade584f6f3716cadbafdc5cf2ef8f296ffd.nq.gz
│   ├── ca765d5a0a7332199f9f7ff196124c760d4c94fe.nq.gz
│   ├── d9690eda455d471ca59e4647960efd00ba4550cc.nq.gz
│   └── f5d8b1401aaebf4965238d767e813f7b72bbd1d2.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 5aa20d2fcdf6edc65ba142f8554d25865336e174.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 24 files
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

[py-pdf/py-pdf.github.io](https://github.com/py-pdf/py-pdf.github.io)

---
*Parsed on 2026-10-21 by [repolex](https://repolex.ai)*
