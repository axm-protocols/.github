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
</p>

---

## Philosophy

axm-protocols starts from a simple observation: in agent workflows, **not everything needs to be probabilistic.** LLM generation is inherently non-deterministic — but code analysis, quality checks, and workflow orchestration can be entirely deterministic. AXM builds that deterministic layer.

- **Structured output** — every tool returns JSON, designed for agents that consume data, not parse text
- **AST-powered analysis** — tree-sitter based code intelligence for semantic precision, not grep noise
- **Codified quality gates** — 40+ rules across lint, types, coverage, complexity, security, and governance
- **Reproducible workflows** — conventional commits, pre-commit enforcement, semantic versioning

---

## 🔧 axm-forge — Developer Tools

AST introspection, code auditing, project scaffolding, and git automation.

| Package | Description | Version |
|---|---|---|
| [axm-ast](https://github.com/axm-protocols/axm-forge/tree/main/packages/axm-ast) | Code intelligence via tree-sitter — callers, impact, dependency graphs | [![PyPI](https://img.shields.io/pypi/v/axm-ast)](https://pypi.org/project/axm-ast/) |
| [axm-audit](https://github.com/axm-protocols/axm-forge/tree/main/packages/axm-audit) | Code quality auditing — 6-category composite scoring on 100 pts | [![PyPI](https://img.shields.io/pypi/v/axm-audit)](https://pypi.org/project/axm-audit/) |
| [axm-init](https://github.com/axm-protocols/axm-forge/tree/main/packages/axm-init) | Project scaffolding & 39-check governance gate | [![PyPI](https://img.shields.io/pypi/v/axm-init)](https://pypi.org/project/axm-init/) |
| [axm-git](https://github.com/axm-protocols/axm-forge/tree/main/packages/axm-git) | Structured commits, semantic tagging, preflight checks | [![PyPI](https://img.shields.io/pypi/v/axm-git)](https://pypi.org/project/axm-git/) |

<p>
  <a href="https://github.com/axm-protocols/axm-forge/actions/workflows/ci.yml"><img src="https://github.com/axm-protocols/axm-forge/actions/workflows/ci.yml/badge.svg" alt="CI"></a>
  <a href="https://forge.axm-protocols.io"><img src="https://img.shields.io/badge/docs-live-brightgreen" alt="Docs"></a>
</p>

```bash
uv add axm-ast axm-audit axm-init axm-git
```

---

## 🧠 axm-nexus — Core Runtime

Unified CLI, protocol execution engine, and MCP server. Nexus provides the runtime that turns structured YAML protocols into validated, checkpointed agent workflows.

| Package | Description |
|---|---|
| axm | Unified CLI shell with autodiscovery |
| axm-nexus | Protocol models, loaders, and catalog |
| axm-engine | State machine, orchestrator, and validation |
| axm-mcp | MCP server exposing all AXM tools |

Coming soon — currently in development.

---

## Standards

Every AXM package is measured on two axes:

- **Governance** (`axm-init check`) — `src/` layout, PEP 621, `py.typed`, GitHub Actions CI, MkDocs docs, pre-commit hooks, conventional commits
- **Code quality** (`axm-audit`) — Ruff lint, MyPy strict, test coverage, cyclomatic complexity, security, dead code — composite score on 100 pts

---

<p align="center">
  <strong>Apache 2.0</strong> · <a href="https://github.com/axm-protocols">GitHub</a>
</p>
