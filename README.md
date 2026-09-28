# Repolex Knowledge Graph of asimov-modules/asimov-mic-module

RDF knowledge graph data for [asimov-modules/asimov-mic-module](https://github.com/asimov-modules/asimov-mic-module), parsed by [repolex](https://repolex.ai).

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
rlex download asimov-modules/asimov-mic-module
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 3bb447c4873980b398fdc1a6d7838999fe6e057e
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 3bb447c4873980b398fdc1a6d7838999fe6e057e.nq.gz
│   └── repolex
│       └── 3bb447c4873980b398fdc1a6d7838999fe6e057e
│           └── chunk-001.nq.gz
├── blob
│   ├── 0faf320ab61483f47f7040f2f4132d61b2b0e756.nq.gz
│   ├── 10b359dd05935c73efb064470f9ecda90f6d28aa.nq.gz
│   ├── 2b0c788e2596d934456a7ce78cc4e7f3fe40e217.nq.gz
│   ├── 75e3b65f99b29f48ab230e3eab3de8d0b7a9229f.nq.gz
│   ├── 8a8466a018d0892660c0b5dd9f37dcd73e9915a6.nq.gz
│   ├── 8acdd82b765e8e0b8cd8787f7f18c7fe2ec52493.nq.gz
│   ├── 9bb0c94968fb34b89b4100cddb084e5a30d2a9c4.nq.gz
│   ├── 9fe50de16e59d550235aa6d7d15ee12ddf054414.nq.gz
│   ├── a760ab06abc51cceb87e4db07cce7e79d1fbe1d0.nq.gz
│   ├── af73f6ba09053af1f21d6315e073a90be75f495f.nq.gz
│   ├── af9908b08f4b33c32a0080af73f53bc0fa0cdce4.nq.gz
│   ├── b66517ed509c3fc1f333655ad8f1352371190b05.nq.gz
│   ├── cf42f6893594e2f8be2b722de51123d65e4d61c4.nq.gz
│   ├── e3e57a8ce4ccbf74759a6df8fa4a3980ff1c9209.nq.gz
│   ├── e8e3b0cf556eabf826e758e3ac76cfbb8b37b7ba.nq.gz
│   ├── efb98088164f5786b17e83ed384971fc3c74f93c.nq.gz
│   ├── fceb23c227d2157f9265d903f38a6b14cdfa3be6.nq.gz
│   └── fe031bc7bfb0b35b6962bd1aea9d7c9cb118537b.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 3bb447c4873980b398fdc1a6d7838999fe6e057e.nq.gz
├── filetree
│   └── 3bb447c4873980b398fdc1a6d7838999fe6e057e.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 26 files
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

[asimov-modules/asimov-mic-module](https://github.com/asimov-modules/asimov-mic-module)

---
*Parsed on 2026-09-28 by [repolex](https://repolex.ai)*
