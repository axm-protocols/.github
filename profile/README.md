# AXM Protocols

<p align="center">
  <img src="https://raw.githubusercontent.com/axm-protocols/axm-forge/main/assets/logo.png" alt="AXM Logo" width="180" />
</p>

<p align="center">
  <strong>A</strong>gent e<strong>X</strong>ecution <strong>M</strong>odel — deterministic tooling and structured <strong>Protocols</strong> for AI agents.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/python-3.12+-blue.svg" alt="Python" />
  <img src="https://img.shields.io/badge/license-Apache%202.0-green.svg" alt="License" />
  <img src="https://img.shields.io/badge/status-active-brightgreen.svg" alt="Status" />
  <a href="https://gabriel.axm-protocols.io"><img src="https://img.shields.io/badge/blog-gabriel.axm--protocols.io-8a5a2b.svg" alt="Blog" /></a>
</p>

---

## Philosophy

Some problems resist determinism by nature — judging an open situation, writing prose,
reasoning over the never-seen. Law met that long ago and did not try to make the judge
deterministic: it accepted a fallible core and built a deterministic *shell* around it —
procedure, rules of evidence, the duty to give reasons. **You do not make the judge
reliable; you make the trial reliable.**

AXM applies the same move to AI agents. LLM generation is irreducibly probabilistic — so
AXM does not fight that, it *frames* it. Code analysis, quality checks, and orchestration
**can** be deterministic, and that is the shell: tight enough that the model's
non-determinism stays confined, framed, justified, and revisable. Not a safer inference —
a tighter procedure around an inference accepted as fallible.

- **Structured output** — every tool returns JSON, designed for agents that consume data, not parse text
- **AST-powered analysis** — tree-sitter based code intelligence for semantic precision, not grep noise
- **Codified quality gates** — 40+ rules across lint, types, coverage, complexity, security, and governance
- **Reproducible workflows** — conventional commits, pre-commit enforcement, semantic versioning

> The thinking behind this — and where the analogy holds, and where it breaks —
> is laid out in [the first post](https://gabriel.axm-protocols.io).

---

## 🔧 [axm-forge](https://github.com/axm-protocols/axm-forge) — Developer Tools

Unified CLI, MCP server, AST introspection, code auditing, project scaffolding, and git automation. Published on PyPI.

| Package | Description | Version |
|---|---|---|
| [axm](https://github.com/axm-protocols/axm-forge/tree/main/packages/axm) | Unified CLI shell with tool autodiscovery | [![PyPI](https://img.shields.io/pypi/v/axm)](https://pypi.org/project/axm/) |
| [axm-mcp](https://github.com/axm-protocols/axm-forge/tree/main/packages/axm-mcp) | MCP server exposing all AXM tools to agents | [![PyPI](https://img.shields.io/pypi/v/axm-mcp)](https://pypi.org/project/axm-mcp/) |
| [axm-ast](https://github.com/axm-protocols/axm-forge/tree/main/packages/axm-ast) | Code intelligence via tree-sitter — callers, impact, dependency graphs | [![PyPI](https://img.shields.io/pypi/v/axm-ast)](https://pypi.org/project/axm-ast/) |
| [axm-audit](https://github.com/axm-protocols/axm-forge/tree/main/packages/axm-audit) | Code quality auditing — composite scoring across lint, types, tests, complexity, security | [![PyPI](https://img.shields.io/pypi/v/axm-audit)](https://pypi.org/project/axm-audit/) |
| [axm-init](https://github.com/axm-protocols/axm-forge/tree/main/packages/axm-init) | Project scaffolding & governance gate | [![PyPI](https://img.shields.io/pypi/v/axm-init)](https://pypi.org/project/axm-init/) |
| [axm-git](https://github.com/axm-protocols/axm-forge/tree/main/packages/axm-git) | Structured commits, semantic tagging, preflight checks | [![PyPI](https://img.shields.io/pypi/v/axm-git)](https://pypi.org/project/axm-git/) |
| [axm-anvil](https://github.com/axm-protocols/axm-forge/tree/main/packages/axm-anvil) | CST-based code transforms and refactors | [![PyPI](https://img.shields.io/pypi/v/axm-anvil)](https://pypi.org/project/axm-anvil/) |
| [axm-edit](https://github.com/axm-protocols/axm-forge/tree/main/packages/axm-edit) | Atomic multi-file batch editing | [![PyPI](https://img.shields.io/pypi/v/axm-edit)](https://pypi.org/project/axm-edit/) |
| [axm-smelt](https://github.com/axm-protocols/axm-forge/tree/main/packages/axm-smelt) | Deterministic token compaction for LLM inputs | [![PyPI](https://img.shields.io/pypi/v/axm-smelt)](https://pypi.org/project/axm-smelt/) |

<p>
  <a href="https://github.com/axm-protocols/axm-forge/actions/workflows/ci.yml"><img src="https://github.com/axm-protocols/axm-forge/actions/workflows/ci.yml/badge.svg" alt="CI"></a>
  <a href="https://forge.axm-protocols.io"><img src="https://img.shields.io/badge/docs-live-brightgreen" alt="Docs"></a>
</p>

```bash
uv add axm axm-mcp axm-ast axm-audit axm-init axm-git axm-anvil axm-edit axm-smelt
```

---

## ✍️ Writing

Notes on agentic AI and how it is built to work — the thinking behind AXM, in long form.

**[gabriel.axm-protocols.io](https://gabriel.axm-protocols.io)** — bilingual (FR/EN), built with Astro, deployed on Cloudflare Pages.

---

## Standards

Every AXM package is measured on two axes:

- **Governance** (`axm-init check`) — `src/` layout, PEP 621, `py.typed`, GitHub Actions CI, MkDocs docs, pre-commit hooks, conventional commits
- **Code quality** (`axm-audit`) — Ruff lint, MyPy strict, test coverage, cyclomatic + cognitive complexity, security, dead code — composite score on 100 pts

---

<p align="center">
  <strong>Apache 2.0</strong> · <a href="https://github.com/axm-protocols">GitHub</a> · <a href="https://gabriel.axm-protocols.io">Blog</a>
</p>
