# Repolex Knowledge Graph of NousResearch/hermes-agent-self-evolution

RDF knowledge graph data for [NousResearch/hermes-agent-self-evolution](https://github.com/NousResearch/hermes-agent-self-evolution), parsed by [repolex](https://repolex.ai).

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
rlex download NousResearch/hermes-agent-self-evolution
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 0a929e3aa20e15cf04dc7c28492a7d41a5139125
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 0a929e3aa20e15cf04dc7c28492a7d41a5139125.nq.gz
│   └── repolex
│       └── 0a929e3aa20e15cf04dc7c28492a7d41a5139125
│           └── chunk-001.nq.gz
├── blob
│   ├── 04f2c78b03587507978806894fbc0aa40f2a512e.nq.gz
│   ├── 0e8396a99d9e5ead7d2a66a8fc511e679072e4e2.nq.gz
│   ├── 179064e1058eb9b0ef28a7f1ae75da15d5c5afed.nq.gz
│   ├── 2a79a670aaa632fe720b2fef0fc9ce62ee7d281f.nq.gz
│   ├── 33d91b6cfeed442b6c825b1ae37c64ada564e7eb.nq.gz
│   ├── 3a430ce13d550f14ae2cf7efa8e89b5efbe625b7.nq.gz
│   ├── 48f9ef147e5b47d3d24d712d5360f41d31340ce6.nq.gz
│   ├── 546086da7bdd3f8308b9c5643f8a17001cc78dea.nq.gz
│   ├── 65fe0aaa4dd131f9dd7166fb402bd242a1ffe3d4.nq.gz
│   ├── 6d4d22ed3a5c54f4060e50174357ec2a3655c6fd.nq.gz
│   ├── 85704c8356d9aa73dcdeb95f70432083956b8550.nq.gz
│   ├── 88e3aaa39e715eb594d58a04bd74cb08dbc9d3c8.nq.gz
│   ├── 9de3fe470543996822d694154d9cbc22ff6e01b0.nq.gz
│   ├── ac2b8a29ed1ba19a528c235a6d3365a5b553a55d.nq.gz
│   ├── adfacc079decf4b5392064aac24a238578b33f9d.nq.gz
│   ├── b7c7521e3e548b83cd30e35d6f0e66b4b5519930.nq.gz
│   ├── baedbb49a40d9454b382820acf5535995cf35235.nq.gz
│   ├── c59f9a6a57e36edbc2aae6b76aeee2e4878e63a8.nq.gz
│   ├── d221b8e0884e5dd8f5fd808c39c1ab418a93502e.nq.gz
│   ├── d6b13459d4da382e87b1dc7e8c79d7d80a9233ef.nq.gz
│   ├── d7e062b5f087a7289b6e409e0aa3816d6ee5ad3b.nq.gz
│   ├── d90162c593cc0aac80f16bd60077e1f26e407269.nq.gz
│   ├── dae7f461bd5a0d2eb30bad1fa1aac612d5ecedb4.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── f4ad3c2c52b3ca8cf71858220609cc3cf7271518.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 0a929e3aa20e15cf04dc7c28492a7d41a5139125.nq.gz
├── filetree
│   └── 0a929e3aa20e15cf04dc7c28492a7d41a5139125.nq.gz
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
| `audit/` | Code architecture and graph audit reports per commit. |

## Source repository

[NousResearch/hermes-agent-self-evolution](https://github.com/NousResearch/hermes-agent-self-evolution)

---
*Parsed on 2026-10-01 by [repolex](https://repolex.ai)*
