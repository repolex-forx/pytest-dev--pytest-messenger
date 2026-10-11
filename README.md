# Repolex Knowledge Graph of pytest-dev/pytest-messenger

RDF knowledge graph data for [pytest-dev/pytest-messenger](https://github.com/pytest-dev/pytest-messenger), parsed by [repolex](https://repolex.ai).

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
rlex download pytest-dev/pytest-messenger
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── f91694959e7d53f2e52b2babb8e265d3c4cac0e6
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── f91694959e7d53f2e52b2babb8e265d3c4cac0e6
│           └── chunk-001.nq.gz
├── blob
│   ├── 0ffe5062612725dd5e0de75d030b81097810dc5d.nq.gz
│   ├── 12610da1802b3b59c259485274d76e815a53d2ea.nq.gz
│   ├── 1ba24b2aa7c8ccf04b8b8abf9cbbbcd2564d703f.nq.gz
│   ├── 1befc1935fd429faed4778fc6db1ba52830dcf64.nq.gz
│   ├── 1db9e77dec7410735d7f858367b0873ec7ad9b22.nq.gz
│   ├── 21e53820423b522dc062c7c11fb603c66fe96fe2.nq.gz
│   ├── 22ef2844f6c7425fa4ee66ea632326aefc3007dd.nq.gz
│   ├── 250649964bbc36f4bec2942f69238aa6f7c02c1a.nq.gz
│   ├── 281d084136b5f47459236392078f35f634df50d3.nq.gz
│   ├── 2834cab62caab863048e8294a60e4a5c18db3a71.nq.gz
│   ├── 2f15eaad9e6d78e4e61c89addf4be77ea57882a0.nq.gz
│   ├── 3547f78998dd26284f519149d562a9bc167d38ee.nq.gz
│   ├── 36b4c4892893685ec1cdc2de69c06a9b73eb33f0.nq.gz
│   ├── 4b915ef090505eda463b0322f84f0fb8aa3243b8.nq.gz
│   ├── 4ba73af5c945ab00357dcd3b24a9e50522cedca7.nq.gz
│   ├── 536e102c12f3165589eedf6c6574971c8e1a8a9f.nq.gz
│   ├── 5dc6fdbe0506f8d4a7e2b7d0ea754aaacbe769dc.nq.gz
│   ├── 65cd51bb5dd58e8af77295a85f3dd8a035a59db2.nq.gz
│   ├── 6a157dcb255afd701e704442115ec915ec8c4498.nq.gz
│   ├── 71973dc9ea884287869cde9fc4780e8bd52ffae3.nq.gz
│   ├── 72a33558153fb57def85612b021ec596ef2a51b9.nq.gz
│   ├── 894a44cc066a027465cd26d634948d56d13af9af.nq.gz
│   ├── 8b41335daf14cca39938b123687a0187bc31b65a.nq.gz
│   ├── 93b8076e736b976bc067a7d6eeac565710d9a7c1.nq.gz
│   ├── 965b2dda7db7c49f68857dc3aea9af37e30a745e.nq.gz
│   ├── 9daa4361b780c3bb3e1700a4187531f6173bde68.nq.gz
│   ├── a12ea577cc23a6ed8d3f4f632c7c2b543b9465ab.nq.gz
│   ├── a446c19c9531264912ae11fed9272f40fda85ba6.nq.gz
│   ├── a60b5be87f97cef216ce91314a29ab1e0378b810.nq.gz
│   ├── b143a530985d6f3e2727a0b70dafe5bc99cfd610.nq.gz
│   ├── b3cbae3a3903d5f364a557b173d2321d2694257c.nq.gz
│   ├── d4a2c4405ec2e962c521a13af91bf5f7098a62a8.nq.gz
│   ├── d600ea190a4f0282a89b30c63a3b25938fa2351a.nq.gz
│   ├── e582053ea018c369be05aae96cf730744f1dc616.nq.gz
│   ├── ee5eb0db543b57796931ee6b065fd607eb30ac68.nq.gz
│   ├── f1e3bf91d41776875f9ea0918cf7880f04bd6a76.nq.gz
│   ├── f39804488c76d45ca4768ddc311b2e132753ea2e.nq.gz
│   ├── f9eec76b55dadd6b7e902e07f9730fb97bd13f74.nq.gz
│   ├── fb3ea898dfc945e6d9462711790bd4f245c0e9ee.nq.gz
│   └── fd9cc4894d6e65343cee2c5445d56cf99a5d45a4.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── f91694959e7d53f2e52b2babb8e265d3c4cac0e6.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 48 files
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

[pytest-dev/pytest-messenger](https://github.com/pytest-dev/pytest-messenger)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
