# AXM Protocols

<p align="center">
  <img src="https://raw.githubusercontent.com/axm-protocols/axm-init/main/assets/logo.png" alt="AXM Logo" width="180" />
</p>

<p align="center">
  <strong>Open-source tools for Python engineering excellence.</strong><br>
  <em>Scaffolding · Quality Checks · Bibliographic Research</em>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/python-3.12+-blue.svg" alt="Python" />
  <img src="https://img.shields.io/badge/license-Apache%202.0-green.svg" alt="License" />
  <img src="https://img.shields.io/badge/status-active-brightgreen.svg" alt="Status" />
</p>

---

## Packages

| Package | Description | Links |
|---------|-------------|-------|
| **[axm-init](https://github.com/axm-protocols/axm-init)** | Scaffold, check & govern Python projects | [![CI](https://github.com/axm-protocols/axm-init/actions/workflows/ci.yml/badge.svg)](https://github.com/axm-protocols/axm-init/actions/workflows/ci.yml) [![PyPI](https://img.shields.io/pypi/v/axm-init)](https://pypi.org/project/axm-init/) [![Docs](https://img.shields.io/badge/docs-live-brightgreen)](https://axm-protocols.github.io/axm-init/) |
| **[axm-bib](https://github.com/axm-protocols/axm-bib)** | Search papers, resolve DOIs, download & extract PDFs | [![CI](https://github.com/axm-protocols/axm-bib/actions/workflows/ci.yml/badge.svg)](https://github.com/axm-protocols/axm-bib/actions/workflows/ci.yml) [![PyPI](https://img.shields.io/pypi/v/axm-bib)](https://pypi.org/project/axm-bib/) [![Docs](https://img.shields.io/badge/docs-live-brightgreen)](https://axm-protocols.github.io/axm-bib/) |

---

## Quick Start

```bash
# Install
uv add axm-init axm-bib

# Scaffold a production-grade Python project
axm-init init my-project --org my-org --author "Name" --email "e@e.com"

# Check any project against the AXM gold standard (38 checks)
axm-init check
# Score: 100/100 — Grade A 🏆

# Search papers and download PDFs
axm-bib search "attention is all you need"
axm-bib pdf 10.48550/arXiv.1706.03762
```

---

## What We Build

**axm-init** scaffolds Python projects with everything pre-configured — CI/CD, linting, typing, testing, docs, and a check system that scores projects against 38 quality checks. Every scaffolded project starts at 100/100.

**axm-bib** is a bibliographic toolkit: search papers across Semantic Scholar and CrossRef, resolve DOIs to BibTeX, and download PDFs with automatic content extraction to Markdown.

Both tools are designed for **AI agent integration** — structured JSON output, MCP-compatible tools, and deterministic workflows that agents can orchestrate.

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
