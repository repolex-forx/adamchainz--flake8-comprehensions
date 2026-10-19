# Repolex Knowledge Graph of adamchainz/flake8-comprehensions

RDF knowledge graph data for [adamchainz/flake8-comprehensions](https://github.com/adamchainz/flake8-comprehensions), parsed by [repolex](https://repolex.ai).

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
rlex download adamchainz/flake8-comprehensions
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 164a53196801719ef6312e4a3d915d374335dea7
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 164a53196801719ef6312e4a3d915d374335dea7
│           └── chunk-001.nq.gz
├── blob
│   ├── 0cb99b58a5cf1c096d8e348c925a729b53e3f93b.nq.gz
│   ├── 205ab9ad9df4ab629d1b7b8d8a72b41f44d8824c.nq.gz
│   ├── 22ddbb118475b52ce8ecba56d9ec45009923da58.nq.gz
│   ├── 274956a3849bc0d348cac58c82ee7ed0e002125b.nq.gz
│   ├── 27beaea176e4f83d524e0e09dd1e32214163ab31.nq.gz
│   ├── 2a7f84f54867d02714727f82eef95d3be939d666.nq.gz
│   ├── 3843b6e6e15b50610a170ae20c22de27fc55c811.nq.gz
│   ├── 3ba13e0cec6cbbfd462e9ebf529dd2093148cd69.nq.gz
│   ├── 40c1340c5e19a33ea6030dd19e4c417b1989b762.nq.gz
│   ├── 40f4ac757715bb1a8c355eda9124141fdda3aeff.nq.gz
│   ├── 573d0696b1c0d0269724d9d30b85987e0b63efc7.nq.gz
│   ├── 663d6b920407c6318f1222445b39e30e44afa9d3.nq.gz
│   ├── 6951b1c616b2dfc10c77b06d2c32fd9613f9a7ad.nq.gz
│   ├── 7f1d007c01048570d774e58f46203d3e92056c39.nq.gz
│   ├── 93acb639926ccf42e9a2f76f02419eeaf0405c3a.nq.gz
│   ├── a3f492f58bbca6b2089ac28abffa649564941aa0.nq.gz
│   ├── cf4bca22e6d1dd6e79d5c283f94302e5483a0068.nq.gz
│   ├── e206832662feb020452d0f4ca332125bf43d699a.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e8f5f5e2770eefd3fe9eabb8bd68cd60100cea85.nq.gz
│   └── f0a2abfa16717167b289159a2f38a41fde8a3457.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 164a53196801719ef6312e4a3d915d374335dea7.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 29 files
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

[adamchainz/flake8-comprehensions](https://github.com/adamchainz/flake8-comprehensions)

---
*Parsed on 2026-10-19 by [repolex](https://repolex.ai)*
