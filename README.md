# Repolex Knowledge Graph of coleifer/django-generic-aggregation

RDF knowledge graph data for [coleifer/django-generic-aggregation](https://github.com/coleifer/django-generic-aggregation), parsed by [repolex](https://repolex.ai).

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
rlex download coleifer/django-generic-aggregation
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 7dc1557ac0a791ccc56278b57ba25d6651d868e0
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 7dc1557ac0a791ccc56278b57ba25d6651d868e0
│           └── chunk-001.nq.gz
├── blob
│   ├── 04292f33b83f44db032689ad527d03ad3a50f9eb.nq.gz
│   ├── 1399fbdc0ea8dd0aa22467f7b1589f1b4ddb8c4f.nq.gz
│   ├── 16b43d8333ee167adcfc837f0b428e60f2989e06.nq.gz
│   ├── 1747311e1499a230eadf20ae30f38d86d14ffb2e.nq.gz
│   ├── 3c360c6f6700bb173b750f2a22a56d9cce2e8bd6.nq.gz
│   ├── 3ccd24e7e9fb50c46df52a4aff21d07d087f9e5b.nq.gz
│   ├── 57e541146ca69ce5383857843aa1d3f93b1f304c.nq.gz
│   ├── 6083b58e9355e3359dc46fd7b850e02c9ec1a653.nq.gz
│   ├── 6a25943939259cc2ad55abf9303ba585af8736e1.nq.gz
│   ├── 841b7cb12e7138a7eb3e4b90e95888e1b0c177c5.nq.gz
│   ├── 850d79c4a18baa2309372d11a4013e14ddc131cc.nq.gz
│   ├── 93120e66c81f4b26c1d40a4b853394b85131e9ed.nq.gz
│   ├── 94b9b5330612c140a924409e181e7744045c64df.nq.gz
│   ├── 95b6cf206360826326e53868e6ba1d28bec0e5b5.nq.gz
│   ├── 999d37e78d5a21cc2be74920f7b8442f6fcd8ea3.nq.gz
│   ├── 9b5c4cea6ff2fa6a12908c0a37497457e95ea657.nq.gz
│   ├── aa872d7e9e50b80891558b61ad1871c80f6c9900.nq.gz
│   ├── b366f7a8b15d08bfe2e703f20a8a363541211233.nq.gz
│   ├── b4c9a61bfe8cba6385ae541f6147fdddc58b2588.nq.gz
│   ├── b857494c632204fc453243523bdee8d94ba3a713.nq.gz
│   ├── bd0816e86c84c19b8216cfc85b654684d9cf8b1f.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── f59843294cd2a8fe389a3bb7667314f38961d3e9.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 7dc1557ac0a791ccc56278b57ba25d6651d868e0.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 31 files
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

[coleifer/django-generic-aggregation](https://github.com/coleifer/django-generic-aggregation)

---
*Parsed on 2026-10-20 by [repolex](https://repolex.ai)*
