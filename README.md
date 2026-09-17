# Repolex Knowledge Graph of rbarrois/confutils

RDF knowledge graph data for [rbarrois/confutils](https://github.com/rbarrois/confutils), parsed by [repolex](https://repolex.ai).

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
lexq download rbarrois/confutils
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── d0f52fd1c057a7c18522e10c32520c9ea3a1a55d
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── d0f52fd1c057a7c18522e10c32520c9ea3a1a55d.nq.gz
│   └── repolex
│       └── d0f52fd1c057a7c18522e10c32520c9ea3a1a55d
│           └── chunk-001.nq.gz
├── blob
│   ├── 01f0fe4408f88ac7d8dd3963d6e54a568ab74a71.nq.gz
│   ├── 100b93820ade4c16225673b4ca62bb3ade63c313.nq.gz
│   ├── 1cd03e189a560b4f83bc5a868a874985fb76c6e5.nq.gz
│   ├── 2bc2c483f0f6230ef096683361b8431cfa31d4a6.nq.gz
│   ├── 3fdb112760debc7366d5fef293b7d4cd76bda8ce.nq.gz
│   ├── 5046a7002fdc8735372ce845c351d1d8c620b18b.nq.gz
│   ├── 504d59e853ff999818257343ec0f659ff637a4b8.nq.gz
│   ├── 64fe2966aba53a86a1293619ca7222e0e2f5fe38.nq.gz
│   ├── 67fdad9dfa1732ff7d9aae34e38e0b06396d417a.nq.gz
│   ├── 6e12217bcdb78c699267249459cbf913606109ec.nq.gz
│   ├── 735fab5c6e7f3d6bb0ac986bb8c525d8161f540e.nq.gz
│   ├── 8b137891791fe96927ad78e64b0aad7bded08bdc.nq.gz
│   ├── 8cfa3ff2a56bd4467f8ded0d02acfba7b47ce496.nq.gz
│   ├── a25c9d0f559a41e5fc3facb3e421f71fab5a632e.nq.gz
│   ├── a2c21cc4bc46b0c483b70b71837a00c3fc92483f.nq.gz
│   ├── a741df7cd5dfe19527cd5f62c733f7257e42a8b8.nq.gz
│   ├── af93217f2a891bcfdf07d4f74ed11cd8c85d5fd6.nq.gz
│   ├── b00503e2c0c385b2d62d59985a1cb67301bfc460.nq.gz
│   ├── d88e214538a71f936762bff41c94a1184c4f63a4.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── ea709b2b77fb095a7cbcd0dea408351035344e80.nq.gz
│   ├── ed05aa5e2def537b6e1103da0ff27e6c9ab13f05.nq.gz
│   ├── f69cb1a8a3b9a6936b577770afc36cd7ebf83702.nq.gz
│   ├── fa2505de8403e7ed8d4f6c784d8ac5cada93c236.nq.gz
│   └── ffbf9e65639e12ae175fbc827131b862aa246943.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── d0f52fd1c057a7c18522e10c32520c9ea3a1a55d.nq.gz
├── filetree
│   └── d0f52fd1c057a7c18522e10c32520c9ea3a1a55d.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 33 files
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

[rbarrois/confutils](https://github.com/rbarrois/confutils)

---
*Parsed on 2026-09-17 by [repolex](https://repolex.ai)*
