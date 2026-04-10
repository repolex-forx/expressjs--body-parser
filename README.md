# Repolex Knowledge Graph of expressjs/body-parser

RDF knowledge graph data for [expressjs/body-parser](https://github.com/expressjs/body-parser), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [lexq](https://github.com/repolex-ai/lexq) query tool using [uv](https://docs.astral.sh/uv/getting-started/installation/).

If you have uv installed, just copy/paste this into your terminal:

```bash
uv tool install git+https://github.com/repolex-ai/lexq
```

This installs lexq onto your system, in your user context. Verify the install:

```bash
lexq --help
```

**lexq is designed to be used primarily by LLMs in a terminal.** Start up your favorite LLM and ask it to use the lexq tool. It's that easy!

To load this repo's data:

```bash
lexq download expressjs/body-parser
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 3d248660b2e8b66732b232d7c758517fbf2420a6
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 3d248660b2e8b66732b232d7c758517fbf2420a6.nq.gz
│   └── repolex
│       └── 3d248660b2e8b66732b232d7c758517fbf2420a6
│           └── chunk-001.nq.gz
├── blob
│   ├── 013ce5c4e52555986cb24bb602429ba2e91e1016.nq.gz
│   ├── 02eb542cd0c6903cbe6438b5a33bf4451990d024.nq.gz
│   ├── 033a97cbea5b51e020e847506536afbe1bf85b86.nq.gz
│   ├── 06c9a41a14b034957bb1cbccd149ba0649a833ea.nq.gz
│   ├── 23c73577049e4d754f368b16e4e0e040dbf14c4c.nq.gz
│   ├── 2b67aa9535ea837fc610a091e0dfc42349bed151.nq.gz
│   ├── 364d3838e5b635d237ee6b06849e805de91445fb.nq.gz
│   ├── 386b7b6946e47bc46f8138791049b4e6a7cef889.nq.gz
│   ├── 39d320f55de5640c327991c765af2fc16b9635cb.nq.gz
│   ├── 486878a229317a54594c917437f7ebc9dbf82d37.nq.gz
│   ├── 497306591aad91cf89a35229cd4318303728fbb7.nq.gz
│   ├── 4a3227c1ecba8bb4e5cb2820d11345e9549d64bf.nq.gz
│   ├── 62562b74a3b5a79e82ca417b02e0f597d85f5e2f.nq.gz
│   ├── 7d3eeb62afad950c21a029788b035dc85805864a.nq.gz
│   ├── 9582e7d9b2f3893787185d804c8d71c0c6bd0ce0.nq.gz
│   ├── 9808c3b2b6602da61eb4afcb4caf33368e3e2bd4.nq.gz
│   ├── 9df73be92dcdad3bd64bfd298056bf9b0aa28118.nq.gz
│   ├── a6096a49b45192e7c5ac5f0f2bdcb17d0b18d1b1.nq.gz
│   ├── ad4854dd95860fabad2bce3abf8573c09ff18e0d.nq.gz
│   ├── b6dc0e29a4af4d417dab33298689854b156ca2bd.nq.gz
│   ├── d1f3f48086b669108f9d9398ce7cfbc02ee0db2f.nq.gz
│   ├── e0bf9741edfed571381a3cc4bf82f647889d073e.nq.gz
│   ├── e4f03fba61b0fabdebe763c8ffa6db3fc383ffe9.nq.gz
│   ├── f15b98e249d653f23d7e121037bde0eae1817582.nq.gz
│   └── fcdde650c06429165341b22111b9124defe83388.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 3d248660b2e8b66732b232d7c758517fbf2420a6.nq.gz
├── filetree
│   └── 3d248660b2e8b66732b232d7c758517fbf2420a6.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 35 files
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

## Source repository

[expressjs/body-parser](https://github.com/expressjs/body-parser)

---
*Parsed on 2026-04-10 by [repolex](https://repolex.ai)*
