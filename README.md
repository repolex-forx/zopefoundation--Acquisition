# Repolex Knowledge Graph of zopefoundation/Acquisition

RDF knowledge graph data for [zopefoundation/Acquisition](https://github.com/zopefoundation/Acquisition), parsed by [repolex](https://repolex.ai).

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
rlex download zopefoundation/Acquisition
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 206990050ded1991313f57fe970be97ce2461502
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 206990050ded1991313f57fe970be97ce2461502
│           └── chunk-001.nq.gz
├── blob
│   ├── 13b1e926a742cf6016aec705384fa0a2f78c7efd.nq.gz
│   ├── 2468ec9ed8681abdc60aec462d6e248e8768ad73.nq.gz
│   ├── 26da37b5d00ed852033bae7aeae0a809dc21821c.nq.gz
│   ├── 34901cb2b67271a1d562089ed2b58c3da1d947b3.nq.gz
│   ├── 4ae5fe5212dc949517f543fce248e1104e91b810.nq.gz
│   ├── 4b7e84d4189385d5b6e4f9f483836836c7d6b1e7.nq.gz
│   ├── 57dd8a4bfaa6a6926253e3211fd3d37aeb9dc274.nq.gz
│   ├── 5f8762ce6bcae6179d297847042fdda8f7dfe0d2.nq.gz
│   ├── 7010753170dcfcc2a2baba59de5c8b3abe41a554.nq.gz
│   ├── 77f3c744e601e8cdd746df3914bf9c9c8ea5365f.nq.gz
│   ├── 78609a5f5a06dd7d09bef2926810c672a193b0a1.nq.gz
│   ├── 80c2223bbbecdb4bf4dfa7f1f92d52b98910b68b.nq.gz
│   ├── 9249333346e259aa52316f1516fb64b419e70a71.nq.gz
│   ├── b76a9ca112b222058eae4a5fd825430b498e8834.nq.gz
│   ├── b8581dd898cbb33e63961b4d181ff0ffbe5d03ee.nq.gz
│   ├── bab7f94be5ef86cce49612e6cdab326a57143d7d.nq.gz
│   ├── c8316863a8cee55bd76bff933a86f8ae1ba707c8.nq.gz
│   ├── cdae4959a51d977f3cc4382471db947ae0448551.nq.gz
│   ├── d7d7f2cd2ccf035e03755915027d5a23a1574379.nq.gz
│   ├── e1f9ad7b3b48377bfbfaa1b380c384ddea24060f.nq.gz
│   ├── e62eec2685820226d926dae3ba92518b526a522e.nq.gz
│   ├── ec366595459ca9ea3ebb11cd95aa867a7482aaef.nq.gz
│   ├── ef395e2d6b4ac8d3c55e77c97c8cbe86ada55a41.nq.gz
│   ├── f462388e0a3f3ec27198330de555de9ceecc15f8.nq.gz
│   ├── fdafa384691cf7210c388eca5b4069293bc7e205.nq.gz
│   └── ffee6a163301e8ce55668b2a9bbe412f51a594fd.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 206990050ded1991313f57fe970be97ce2461502.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 34 files
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

[zopefoundation/Acquisition](https://github.com/zopefoundation/Acquisition)

---
*Parsed on 2026-11-02 by [repolex](https://repolex.ai)*
