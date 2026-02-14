# AXM Protocols

<p align="center">
  <img src="https://raw.githubusercontent.com/axm-protocols/axm-init/main/assets/logo.png" alt="AXM Logo" width="180" />
</p>

<p align="center">
  <strong>AXM · Agent eXecution Model</strong> <em>(pronounced "Axiom")</em><br>
  Structured protocols for AI agents, from scaffolding to execution.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/python-3.12+-blue.svg" alt="Python" />
  <img src="https://img.shields.io/badge/license-Apache%202.0-green.svg" alt="License" />
  <img src="https://img.shields.io/badge/status-active-brightgreen.svg" alt="Status" />
</p>

---

## Why Protocols?

AI agents are increasingly capable, but capability without governance is a liability. Today's agents produce great results, yet their work is hard to audit, reproduce, or certify. When the stakes are high (compliance, security, production code) you need more than "it usually works."

AXM takes a protocol-driven approach: **structured pipelines with validation gates, checkpointed state, and traceable artifacts**. Agents think freely. The server validates every transition.

This philosophy shapes everything we build:

- **Constrained execution**: agents follow structured pipelines, validation gates prevent skipping steps
- **Two-stage validation**: fast structural checks first, semantic evaluation second
- **Session persistence**: execution state is saved and resumable after any interruption
- **Knowledge management**: URI-addressable, lazy-loaded resources for efficient context
- **Provenance tracking**: every artifact carries traceability metadata

---

## 🔧 Open-Source Tools

Production-grade Python tools designed for humans and AI agents alike. Each tool is independent, structured-output-first, and MCP-compatible.

### Core Toolchain

| Package | Description | Links |
|---------|-------------|-------|
| **[axm](https://github.com/axm-protocols/axm)** | Unified CLI shell, autodiscovers installed AXM packages via entry points | [![CI](https://github.com/axm-protocols/axm/actions/workflows/ci.yml/badge.svg)](https://github.com/axm-protocols/axm/actions/workflows/ci.yml) [![PyPI](https://img.shields.io/pypi/v/axm)](https://pypi.org/project/axm/) [![Docs](https://img.shields.io/badge/docs-live-brightgreen)](https://axm-protocols.github.io/axm/) |
| **[axm-init](https://github.com/axm-protocols/axm-init)** | Scaffold, check & govern Python projects (38 quality checks) | [![CI](https://github.com/axm-protocols/axm-init/actions/workflows/ci.yml/badge.svg)](https://github.com/axm-protocols/axm-init/actions/workflows/ci.yml) [![PyPI](https://img.shields.io/pypi/v/axm-init)](https://pypi.org/project/axm-init/) [![Docs](https://img.shields.io/badge/docs-live-brightgreen)](https://axm-protocols.github.io/axm-init/) |
| **[axm-audit](https://github.com/axm-protocols/axm-audit)** | Code quality auditing, 6-category composite scoring on 100pts | [![CI](https://github.com/axm-protocols/axm-audit/actions/workflows/ci.yml/badge.svg)](https://github.com/axm-protocols/axm-audit/actions/workflows/ci.yml) [![PyPI](https://img.shields.io/pypi/v/axm-audit)](https://pypi.org/project/axm-audit/) [![Docs](https://img.shields.io/badge/docs-live-brightgreen)](https://axm-protocols.github.io/axm-audit/) |
| **[axm-bib](https://github.com/axm-protocols/axm-bib)** | Bibliographic toolkit: search papers, resolve DOIs, extract PDFs | [![CI](https://github.com/axm-protocols/axm-bib/actions/workflows/ci.yml/badge.svg)](https://github.com/axm-protocols/axm-bib/actions/workflows/ci.yml) [![PyPI](https://img.shields.io/pypi/v/axm-bib)](https://pypi.org/project/axm-bib/) [![Docs](https://img.shields.io/badge/docs-live-brightgreen)](https://axm-protocols.github.io/axm-bib/) |

### Coming Soon

| Package | Description | Status |
|---------|-------------|--------|
| **axm-mcp** | MCP server exposing all AXM tools to AI agents via Model Context Protocol | 🔜 |
| **axm-ast** | Code intelligence: AST-powered search, impact analysis, dependency graphs via tree-sitter | 🔜 |
| **axm-git** | Git automation: preflight checks, atomic commits, semantic tagging | 🔜 |

```bash
# Install everything
uv add axm[all]

# Or pick what you need
uv add axm-init axm-audit axm-bib
```

---

## ⚙️ Protocol Engine

Behind the open-source tools lies a **protocol execution engine**: the runtime that turns structured YAML protocols into validated, checkpointed agent workflows with server-enforced quality gates.

The engine is currently in private development. If you're interested in structured agent execution for your team, [reach out](mailto:gabriel@axm-protocols.io).

---

## Standards

All AXM repositories follow a shared gold standard enforced by `axm-init check`:

- `src/` layout, PEP 621, `py.typed`
- Ruff + MyPy (strict) + Pytest + Coverage
- GitHub Actions CI with trusted OIDC publishing
- MkDocs Material with Diátaxis documentation
- Pre-commit hooks, Dependabot, conventional commits

---

<p align="center">
  <strong>Apache 2.0</strong> · <a href="https://github.com/axm-protocols">GitHub</a>
</p>
