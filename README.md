# Repolex Knowledge Graph of svetlyak40wt/python-repr

RDF knowledge graph data for [svetlyak40wt/python-repr](https://github.com/svetlyak40wt/python-repr), parsed by [repolex](https://repolex.ai).

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
lexq download svetlyak40wt/python-repr
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 56f6a5a3a8f9a2b9e0e028b7992a086e9b42ed4d
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 56f6a5a3a8f9a2b9e0e028b7992a086e9b42ed4d.nq.gz
│   └── repolex
│       └── 56f6a5a3a8f9a2b9e0e028b7992a086e9b42ed4d
│           └── chunk-001.nq.gz
├── blob
│   ├── 28caa1bfe75a9bbf8f7d4030ec54439775a57b3a.nq.gz
│   ├── 3b6796673f88c023d36bf24a60684304c3c7f8ef.nq.gz
│   ├── 4000618e99f9c8ad55aaf9fbbc9057794bfc1252.nq.gz
│   ├── 547dfeecccae7f174170e20f441eead81b5eed19.nq.gz
│   ├── 54a5178587eb3c3c84d3adea87d6e3f0f18e786d.nq.gz
│   ├── 565b0521d0c2cdbfe493d19765b04d5c119fa7eb.nq.gz
│   ├── 72a33558153fb57def85612b021ec596ef2a51b9.nq.gz
│   ├── 772866d2223c1df6c476d2eee7b71be23e60a923.nq.gz
│   ├── 823edd8f8078643dc3a4c2f5bf75afd6235f90cd.nq.gz
│   ├── 85d7778e3aa11d9dbc56624b6406ba4225c156b4.nq.gz
│   ├── 899afee06e265da92482aed3d287e9376d8c9370.nq.gz
│   ├── 8eae14956066132afd629f66458e317dc10d00cc.nq.gz
│   ├── 92351c4f048b8f735f71d3b815917ca906f702f7.nq.gz
│   ├── 9e2742189f65ea34df7e814476bef5ba6c50eb66.nq.gz
│   ├── a71c7bdd52e7e4d6b6116c42e09539d045b3a5ce.nq.gz
│   ├── ae1997adeef763ce4beccd0468cba11286c8c55a.nq.gz
│   ├── c943692424dc37e591a23659bf8417ad091e37d2.nq.gz
│   ├── caf3c9caad9184b457808f05cf628b14314993f7.nq.gz
│   ├── ccd855ce7d7a1375b1914a5ce03ccfa84fb0b6fa.nq.gz
│   ├── d2b3746dc937e3f9d37ccb5392e38ff6de6271ef.nq.gz
│   ├── d9a8ab91d1902e77fd307223f2961ccb286a5b76.nq.gz
│   ├── e0d17494c30025be52f149fdd64135a330297a7a.nq.gz
│   ├── e122f914a87b277e565fc9567af1a7545ec9872b.nq.gz
│   ├── e582053ea018c369be05aae96cf730744f1dc616.nq.gz
│   ├── ef4a013cd0042083f2644ef153ea1bc856354a56.nq.gz
│   ├── f674986acbd603c061b317d61ec8e65284f88199.nq.gz
│   ├── f6cd4be2f75952456cb72c9bee63e4873187a3d1.nq.gz
│   ├── f95eb78d8a603b0fe5d17560d0dd04877d55c71c.nq.gz
│   ├── fdfbaf6ce4d88f51a40cceacdc0d7dd43edfc818.nq.gz
│   └── fe6b7a6d46747bbbb60a852c22460c578c5f0558.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 56f6a5a3a8f9a2b9e0e028b7992a086e9b42ed4d.nq.gz
├── filetree
│   └── 56f6a5a3a8f9a2b9e0e028b7992a086e9b42ed4d.nq.gz
├── issue
│   └── issue.nq.gz
└── tag
    └── tag.nq.gz

14 directories, 39 files
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

[svetlyak40wt/python-repr](https://github.com/svetlyak40wt/python-repr)

---
*Parsed on 2026-04-09 by [repolex](https://repolex.ai)*
