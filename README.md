# Repolex Knowledge Graph of jupyter/sphinxcontrib_github_alt

RDF knowledge graph data for [jupyter/sphinxcontrib_github_alt](https://github.com/jupyter/sphinxcontrib_github_alt), parsed by [repolex](https://repolex.ai).

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
rlex download jupyter/sphinxcontrib_github_alt
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── d53e47dba537ae17ebecd66e1d23ff05ad94cce3
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── d53e47dba537ae17ebecd66e1d23ff05ad94cce3
│           └── chunk-001.nq.gz
├── blob
│   ├── 153c649661d5df79055be0fff5487293b1d886ec.nq.gz
│   ├── 18bb6a146b2c0a3f9b7681321179af5f8898011a.nq.gz
│   ├── 2b20602611ae83f5c91811510f930a4991022024.nq.gz
│   ├── 79217d56311e126134f7115479017384d9d54839.nq.gz
│   ├── 80fbabd9abd682fba75cd4c94d6f8356bf7b6126.nq.gz
│   └── f618a33792e38da2f59364377092da0743eda3bb.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── d53e47dba537ae17ebecd66e1d23ff05ad94cce3.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 14 files
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

[jupyter/sphinxcontrib_github_alt](https://github.com/jupyter/sphinxcontrib_github_alt)

---
*Parsed on 2026-10-21 by [repolex](https://repolex.ai)*
