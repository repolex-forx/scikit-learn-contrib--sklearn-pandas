# Repolex Knowledge Graph of scikit-learn-contrib/sklearn-pandas

RDF knowledge graph data for [scikit-learn-contrib/sklearn-pandas](https://github.com/scikit-learn-contrib/sklearn-pandas), parsed by [repolex](https://repolex.ai).

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
rlex download scikit-learn-contrib/sklearn-pandas
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── c9db2d6dcbf515eade751073f43318e43cae5177
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── c9db2d6dcbf515eade751073f43318e43cae5177
│           └── chunk-001.nq.gz
├── blob
│   ├── 0385fa96df4b0d444af8ee314fcc47cfe563adbf.nq.gz
│   ├── 0691a36304fc8106d0382818a2cc97cd9d1c2b9f.nq.gz
│   ├── 0cd8d0bbe55242b164599511b4d8b1234773c9ca.nq.gz
│   ├── 250c89a4e3b38ac3e00f617df445ec7a61e01cde.nq.gz
│   ├── 27b2f8ed09bcde5b7cc2167150af8607fff7a587.nq.gz
│   ├── 2d089672a3fb0c8118a6563b58fd36cfe1bb881d.nq.gz
│   ├── 378349abc924eee216d800a45813f235f8cf06f4.nq.gz
│   ├── 40184eb1f0dcd9f6a446f6cfe63068cd43e55ef8.nq.gz
│   ├── 535ecf69cd53038812b68e0cbe5fae1b2b1a8d49.nq.gz
│   ├── 630329b1428c8417ad4606dcfc56d85475687601.nq.gz
│   ├── 634e789ad1c46def70510b7873bd3b071a2ca231.nq.gz
│   ├── 77d3e2b6c2b8c5658447c577fa42127aa5168a68.nq.gz
│   ├── 82c0b8d879537bcc0f55e2cda0f6451d5212e70e.nq.gz
│   ├── 8951ea8e619d97d651aa55e8dee549b29b31a746.nq.gz
│   ├── 9d5d250d095009403f66851f48866f5cfe39703b.nq.gz
│   ├── a6920faa953bbce361a8c2b3d548cd87a4bfa951.nq.gz
│   ├── ae693c2187d59a16742d3945213b3cec942f9e18.nq.gz
│   ├── c3cdd854c1c401aa7c49409ccff20543695688ab.nq.gz
│   ├── ca4568e79fa7fe1fb93547a66c5aeefdd3c5481d.nq.gz
│   ├── ce87297f8f4f6ea1b772076f4a44dd5c9b365a05.nq.gz
│   ├── e0127c18370fbcab8bc08e916124c44eeabab02b.nq.gz
│   ├── e5590d0ab72957a85778719f0f4f3418c50e4c7f.nq.gz
│   ├── e8aae87b8a200c211b8b55ad504fa91bf91594b6.nq.gz
│   ├── ee57b572af0516f4382e7ba846536a3c07a3ffcd.nq.gz
│   ├── ee6f1e74a97aeb216446f4260f6cc632e77410df.nq.gz
│   ├── f20683f3c0e15793e9e1422a0cd56530fb800e52.nq.gz
│   ├── fb27143ad859ecc793ea4bf4a25d177309481cec.nq.gz
│   ├── fb5af9887a36d586b8fd24f46f07eaaa6b53ac5d.nq.gz
│   └── fd265ab9a69a9f2b764a7a5c6e1c185fa049214a.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── c9db2d6dcbf515eade751073f43318e43cae5177.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 37 files
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

[scikit-learn-contrib/sklearn-pandas](https://github.com/scikit-learn-contrib/sklearn-pandas)

---
*Parsed on 2026-10-15 by [repolex](https://repolex.ai)*
