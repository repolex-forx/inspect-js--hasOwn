# Repolex Knowledge Graph of inspect-js/hasOwn

RDF knowledge graph data for [inspect-js/hasOwn](https://github.com/inspect-js/hasOwn), parsed by [repolex](https://repolex.ai).

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
rlex download inspect-js/hasOwn
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 65c9fc9cabca2f10170a5d037d2f7f9f6380e80f
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 65c9fc9cabca2f10170a5d037d2f7f9f6380e80f
│           └── chunk-001.nq.gz
├── blob
│   ├── 0314929078de8a733a0af9c8ba5bc00aca094cc9.nq.gz
│   ├── 10396f1fc042b2465f9999c6c3998ea5c89b54f4.nq.gz
│   ├── 1826526e091b89c896e7099ccd891db79165e329.nq.gz
│   ├── 1c4b85b756a968f4fcad0e76cbf67cad78113510.nq.gz
│   ├── 38fcca3502c885830f22ef4fbccccc15deb97a5c.nq.gz
│   ├── 66c938249bb1fbe2b950464736f5eb2546c636c7.nq.gz
│   ├── 6b71d59cea119f539ebf628eaca95a22f33b30d1.nq.gz
│   ├── 88d49f9bb44f436548a11cfa8ac716f1192f50fe.nq.gz
│   ├── 90a43dc309b047ad27d1efee6c1f08c6d522583f.nq.gz
│   ├── a4cd29e9d87bb5edd1753523fd17e23a90a8dc25.nq.gz
│   ├── aafdf3b2b8f0ef01aa1b3e44596560eee3f38ff7.nq.gz
│   ├── adad47c0774bee306b0c0ee197f7122162d742a2.nq.gz
│   ├── cc80f22fa906221aca36afbea97e39f185d28712.nq.gz
│   ├── d68c8b716ff04186cd4c0ed8f85af474cfbfbc6a.nq.gz
│   ├── dd4af3dead1d0271155176658cf353550949ee18.nq.gz
│   ├── eacea13e1815dd5fe322f64b653bc81eb9924377.nq.gz
│   ├── f25870d366d4d6dc127ec7ff84f3b8a22b85ee00.nq.gz
│   └── f759b8a8396e3993fb7901d7551d38ee2a786b31.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 65c9fc9cabca2f10170a5d037d2f7f9f6380e80f.nq.gz
├── issue
│   └── issue.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 25 files
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

[inspect-js/hasOwn](https://github.com/inspect-js/hasOwn)

---
*Parsed on 2026-11-09 by [repolex](https://repolex.ai)*
