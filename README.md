# Repolex Knowledge Graph of astropy/extension-helpers

RDF knowledge graph data for [astropy/extension-helpers](https://github.com/astropy/extension-helpers), parsed by [repolex](https://repolex.ai).

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
rlex download astropy/extension-helpers
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── f75d18ad43264117aebf6c1d2c34a6c587e61f60
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── f75d18ad43264117aebf6c1d2c34a6c587e61f60
│           └── chunk-001.nq.gz
├── blob
│   ├── 02f3bfcc087052387375ff9873f15c50a581612c.nq.gz
│   ├── 065b8a5aad7d6c8f4a9235b6fd178800cabdb4a2.nq.gz
│   ├── 067bf5fb517ed39a00f24c92546401fafdec5231.nq.gz
│   ├── 0ba557d18f3bf507d4b645e40a268b0cfcb661ff.nq.gz
│   ├── 0cba5656e5771064cbe5fb5715d2b017ed50f400.nq.gz
│   ├── 0dc2b76d597fa45e6fb026261ac75176715a73ae.nq.gz
│   ├── 10589ece86358e91d72602abb395b42e63cdc4bf.nq.gz
│   ├── 17cd2d65c791dfe3fb9f648931b849b34c1deef3.nq.gz
│   ├── 27f573b87af11e2cbbd9f54eb1ee285a58550146.nq.gz
│   ├── 285c78d440abc04da4565b62953b88c15b976056.nq.gz
│   ├── 2a835e84c07c2b81a0ed5c819a88054a5cb1576f.nq.gz
│   ├── 2dbcadb7432f59b9b75f44dc1c7fcf2739cf1b7b.nq.gz
│   ├── 363294712b10b9190a6b47f32b7bc94a7d069e01.nq.gz
│   ├── 36bc2846f00c093c2f40a035feb9fa361291e3ba.nq.gz
│   ├── 531491300d7a6bcc1849a6cbe801b9c157aad4ea.nq.gz
│   ├── 5b20c2ad4fa081592c2d5864079c1514b7f8441e.nq.gz
│   ├── 5d30be9c60837118f8962ed1d12368b82419cb49.nq.gz
│   ├── 6633a48cee9da736e0ac9b3fa67e00a67094f094.nq.gz
│   ├── 69715bb2bb42139baca0af538761e9a0c6771770.nq.gz
│   ├── 73fec2a01981a00ab86d37187501c5aac407f5bc.nq.gz
│   ├── 7c2cc1ba01a7d7f133616660efd1fcd51cf73664.nq.gz
│   ├── 880a7576dd1fb544ded9ce00a0ee505dcf5e290a.nq.gz
│   ├── 8b0dcebfb4538dbd907387fa011d95534c338ea8.nq.gz
│   ├── 940bb495e89a2570ce46cf9c9e64a04c433f5698.nq.gz
│   ├── 9781722edfa48db54f9916b8d246e3e8695a3b10.nq.gz
│   ├── 985a46f441b546c252b1d81836c714c190696634.nq.gz
│   ├── 9a1c62cdd2fb871363384e25c2dd6bd24537ce8c.nq.gz
│   ├── b5087217ffa597b1f5e87e2b89687f5be65b6f7e.nq.gz
│   ├── bc8b9d12618ca02261849939331b12a941034981.nq.gz
│   ├── c69a25fe6dfcc68efa5ab0d7089412a7b40c37ac.nq.gz
│   ├── e12b62b33aaf6d4fd27a6bbace0f1c7b14e5ba96.nq.gz
│   ├── e2223f823697b14e2386275e0b8b9df2e64bfc8c.nq.gz
│   ├── edefa0d3853d70afa868d8feb0918a3b435b64a4.nq.gz
│   └── ee970a204231f55b163abff601de7a69eadf57ef.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── f75d18ad43264117aebf6c1d2c34a6c587e61f60.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 42 files
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

[astropy/extension-helpers](https://github.com/astropy/extension-helpers)

---
*Parsed on 2026-10-15 by [repolex](https://repolex.ai)*
