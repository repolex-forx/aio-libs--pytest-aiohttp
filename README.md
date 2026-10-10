# Repolex Knowledge Graph of aio-libs/pytest-aiohttp

RDF knowledge graph data for [aio-libs/pytest-aiohttp](https://github.com/aio-libs/pytest-aiohttp), parsed by [repolex](https://repolex.ai).

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
rlex download aio-libs/pytest-aiohttp
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 5f01c5f3c5f4573df756f6e57fa070b8e0491757
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 5f01c5f3c5f4573df756f6e57fa070b8e0491757
│           └── chunk-001.nq.gz
├── blob
│   ├── 0102b0a974ec49314140d79ae6e34f30b6cb4def.nq.gz
│   ├── 109b60026e9355d6b693658f697ac25a9e3f9aa2.nq.gz
│   ├── 1b48d5afc3d411ebc452bbea172e24c24b9b4e44.nq.gz
│   ├── 320e05a0ef730dd51e38f9d079d295bac7e313f8.nq.gz
│   ├── 375155a1ff4486ad458533a391c6f20784f62a22.nq.gz
│   ├── 3d909caa0b93faa72a79e86a9fc69de5cccd7bcf.nq.gz
│   ├── 47c439ba7ffdf8f10763f1a4f32fd7ffe1c08a3e.nq.gz
│   ├── 4ed00b59535375f6da52cefd9988870ef9e5a047.nq.gz
│   ├── 606849326a4002007fd42060b51e69a19c18675c.nq.gz
│   ├── 8c52f6c493422ed59bdca3089c53a1d440ea7f94.nq.gz
│   ├── 93f9f275b06ce56f3e15dba7398a5e64ad6204cc.nq.gz
│   ├── a333cd2ee0e63414f6de26ab55ef114d01de34a2.nq.gz
│   ├── a9955b7f530e32dce6768f248cc78765d659e1dd.nq.gz
│   ├── ac7cea1e3c6b13be3f1ff94f9638666cb43f90ab.nq.gz
│   ├── bb54c49ab10eb2310cb97dd99f40ff07d7cb823a.nq.gz
│   ├── bd33618136642f1371fef16ee038d684eea6293a.nq.gz
│   ├── c556f28250f7aaa3086bbbfab9bd8b445f944041.nq.gz
│   ├── e01e5f0458efdafc11fce62dd12510d40d5ff4d9.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── f59dd8b2ffdfb9dba0141d636fbe23352b99b4f6.nq.gz
│   ├── fa0147f78dc35223dc45a41bc91b6d71fd3f4e35.nq.gz
│   └── fcbb3002434110c2e42d40296512009fbfeda0e2.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 5f01c5f3c5f4573df756f6e57fa070b8e0491757.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 30 files
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

[aio-libs/pytest-aiohttp](https://github.com/aio-libs/pytest-aiohttp)

---
*Parsed on 2026-10-10 by [repolex](https://repolex.ai)*
