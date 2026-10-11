# Repolex Knowledge Graph of litestar-org/litestar-oidc

RDF knowledge graph data for [litestar-org/litestar-oidc](https://github.com/litestar-org/litestar-oidc), parsed by [repolex](https://repolex.ai).

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
rlex download litestar-org/litestar-oidc
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── a8604405f4f05ab61936d8ae3ee9afd655264ccf
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── a8604405f4f05ab61936d8ae3ee9afd655264ccf
│           └── chunk-001.nq.gz
├── blob
│   ├── 02b4dd0c499a3222d225dfda03ac6177d984b8c6.nq.gz
│   ├── 03f3f04af6d73bde44f84ef6d345d8bfe9c661de.nq.gz
│   ├── 09be58d0d57bd662a62973861cc0c0fbbdbebf44.nq.gz
│   ├── 123014908bebbfb7ecfa1d15daaceb272fabe05b.nq.gz
│   ├── 1d27fd298befe01c50206e70480a41bdad0b8269.nq.gz
│   ├── 21cb5c8cc362ae3042299e607ae5cce77f3e2a02.nq.gz
│   ├── 37d8731ad036726a8d0854b9d2959139516de927.nq.gz
│   ├── 39c55e6275faa5d695d8699272cd62225b352440.nq.gz
│   ├── 3ba13e0cec6cbbfd462e9ebf529dd2093148cd69.nq.gz
│   ├── 44636503252c3dbb474ad9efc7017ae8667b382e.nq.gz
│   ├── 4e58f77a5603d469b738db232743e40442dbc96d.nq.gz
│   ├── 5b0078495f326f864ae663a42f825f6aebce88a4.nq.gz
│   ├── 7941f6aa65c2fcc73500e7bb900931f8a4844173.nq.gz
│   ├── 89dd14e8fc61ecd03c0747ec394c0a00b99129b4.nq.gz
│   ├── 8a104b3053cd4501513a4670147050214fb4d457.nq.gz
│   ├── 8eb633c4984b85532f5330531bc2032f813a41cc.nq.gz
│   ├── 90446afc3da119a8cdeadaee892c7a70768b84d9.nq.gz
│   ├── 9a60dc628cbf9520330a57545b9e5c3df68ecb7a.nq.gz
│   ├── 9e40d54d95b4a331e2bd06351bdffa1c44fcebf6.nq.gz
│   ├── 9e8af479a967b3b385ef6ab1a8f0fa26a98cbb09.nq.gz
│   ├── a3c98e09941b3fc870e0c688d587ebf091e272ba.nq.gz
│   ├── a54c038818b3185dbdd4ec0366dbcbe6b6a1c8bd.nq.gz
│   ├── a9c36f957b9d4d21b690882de464cf5b0477c535.nq.gz
│   ├── b3450b821343219962b2637be932b53a1dc02c25.nq.gz
│   ├── b405d343e241eae142d070fe29ed394a7ffb6759.nq.gz
│   ├── b666f2cc0226e12e2944bf775ab50a0d7487a096.nq.gz
│   ├── bc7095d8f454a7279fb9d13050d592077d1a0a87.nq.gz
│   ├── cb35a11f555532b0a858cc96a08d5bfed092328b.nq.gz
│   ├── d0a7a44246b5cc4cf8de4f32577c5cfa91cc11e8.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e7b666c4aae34385192884d45b02f2c3d4121efd.nq.gz
│   ├── f586c9dee723feefec873e756a88fd40d7a28c61.nq.gz
│   ├── f793fe9e80d1fcb978fe1001c0d58f8de163dd35.nq.gz
│   └── fe913e87fa1830aa54557cbf8ba51f7bdb8d13a0.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── a8604405f4f05ab61936d8ae3ee9afd655264ccf.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 41 files
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

[litestar-org/litestar-oidc](https://github.com/litestar-org/litestar-oidc)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
