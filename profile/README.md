# AXM Protocols

<p align="center">
  <img src="https://raw.githubusercontent.com/axm-protocols/axm-forge/main/assets/logo.png" alt="AXM Logo" width="180" />
</p>

<p align="center">
  <strong>A</strong>gent e<strong>X</strong>ecution <strong>M</strong>odel — a deterministic shell for non-deterministic agents.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/python-3.12+-blue.svg" alt="Python" />
  <img src="https://img.shields.io/badge/license-Apache%202.0-green.svg" alt="License" />
  <a href="https://gabriel.axm-protocols.io"><img src="https://img.shields.io/badge/blog-gabriel.axm--protocols.io-8a5a2b.svg" alt="Blog" /></a>
</p>

---

## The idea

Some problems resist determinism by nature — judging an open situation, writing
prose, reasoning over the never-seen. Law met that long ago and didn't try to make
the judge deterministic: it accepted a fallible core and built a deterministic
*shell* around it — procedure, rules of evidence, the duty to give reasons. **You
don't make the judge infallible; you make the trial reliable.**

AXM applies the same move to AI agents. LLM generation is irreducibly probabilistic,
so AXM doesn't fight it — it *frames* it. Analysis, quality gates, and orchestration
**can** be deterministic, and that's the shell: tight enough that the model's
non-determinism stays confined, framed, justified, and revisable.

> Where this idea comes from — and where it breaks — is in [the first post](https://gabriel.axm-protocols.io).

---

## What's here

**🔧 [axm-forge](https://github.com/axm-protocols/axm-forge) — the developer toolchain.**
Nine packages on PyPI: a unified CLI, an MCP server, tree-sitter code intelligence,
quality auditing, scaffolding, git automation, atomic editing, CST refactoring, and
token compaction. Every tool returns a structured result with a compact text view —
built for agents that consume data, not parse prose.

```bash
claude mcp add --scope user axm-mcp -- uvx --python 3.12 --from "axm-mcp[all]@latest" axm-mcp
```

`--scope user` installs it globally (available in every session). Drop it to enable AXM per-project instead — the server then loads only in the directory where you run the command.

This wires `verify`, `audit`, the `ast_*` family, `git_commit`, `batch_edit` and the
rest into your MCP client. Each package also ships standalone (`uv add axm-audit`).

<p>
  <a href="https://github.com/axm-protocols/axm-forge/actions/workflows/ci.yml"><img src="https://github.com/axm-protocols/axm-forge/actions/workflows/ci.yml/badge.svg" alt="CI"></a>
  <a href="https://forge.axm-protocols.io"><img src="https://img.shields.io/badge/docs-live-brightgreen" alt="Docs"></a>
</p>

---

## Coming next

The toolchain is the shell's *foundation*. The runtime is what comes next: turning
agent work into something you can structure, gate, and replay.

- **Deterministic orchestration (loom-DAG).** Agent workflows as graphs — phases,
  quality gates, and bounded repair loops — where the orchestration is structural
  and observable, and the LLM is the oracle inside it, never the thing in charge.
- **Ticket-driven execution.** A feature lifecycle from idea → spec → ticket → done,
  each transition carried by a workflow rather than by discipline. The agent picks
  up a ticket and runs it through the gates; nothing mediocre passes.

The shell is what makes the autonomy safe. That's the whole bet.

---

## Standards

Every AXM package is measured on two axes:

- **Governance** (`axm-init check`) — `src/` layout, PEP 621, `py.typed`, CI, MkDocs docs, prek, conventional commits.
- **Code quality** (`axm-audit`) — Ruff, MyPy strict, coverage, cyclomatic + cognitive complexity, security, dead code — composite score on 100 pts.

---

<p align="center">
  <strong>Apache 2.0</strong> · <a href="https://github.com/axm-protocols">GitHub</a> · <a href="https://gabriel.axm-protocols.io">Blog</a>
</p>
