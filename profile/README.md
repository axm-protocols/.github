<p align="center">
  <img src="https://raw.githubusercontent.com/axm-protocols/axm-forge/main/assets/logo.png" alt="AXM Logo" width="180" />
</p>

<h1 align="center">AXM Protocols</h1>

<p align="center">
  <strong>A</strong>gent e<strong>X</strong>ecution <strong>M</strong>odel — governed execution, built around the problem to solve.
</p>

<p align="center">
  <a href="https://github.com/axm-protocols/axm-forge/actions/workflows/ci.yml"><img src="https://github.com/axm-protocols/axm-forge/actions/workflows/ci.yml/badge.svg" alt="Forge CI" /></a>
  <img src="https://img.shields.io/badge/python-3.12%2B-blue" alt="Python 3.12+" />
  <a href="https://github.com/axm-protocols/axm-forge/blob/main/LICENSE"><img src="https://img.shields.io/badge/Forge_license-Apache%202.0-green" alt="Forge license: Apache 2.0" /></a>
  <a href="https://forge.axm-protocols.io/"><img src="https://img.shields.io/badge/docs-Forge-brightgreen" alt="Forge documentation" /></a>
  <a href="https://gabriel.axm-protocols.io/"><img src="https://img.shields.io/badge/blog-gabriel.axm--protocols.io-8a5a2b.svg" alt="Blog" /></a>
</p>

---

AXM develops an execution model for work carried out by AI agents, software
and people. It starts with the problem, the result expected and the conditions
for accepting it. The public starting point is
**[AXM Forge](https://github.com/axm-protocols/axm-forge)**, a Python developer
toolchain available through MCP, a shared CLI and Python libraries.

## The idea

Think of commissioning a piece of work in a workshop. The brief and acceptance
criteria remain attached to the job as different specialists contribute.
Changing who does the work need not change what counts as an acceptable result.

AXM applies that separation to execution. The problem and its progress persist
across attempts. A **contract** describes what an acceptable result must satisfy;
an **evaluation policy** describes how to assess it; an **executor** attempts
the work. Evaluation can combine automated checks, model judgment and human
review, according to the task.

The design principle is to make the decision to accept a proposed change
explicit and inspectable. This lets the means of execution evolve while keeping
the requirements visible. The strength of an acceptance decision depends on the
checks and evidence behind it.

The [blog](https://gabriel.axm-protocols.io/) explores the ideas behind this
approach: constraints within autonomous loops, bounded execution and the
difference between a convincing result and a justified one.

## Start with Forge

Forge provides tools for understanding and changing code:

- **Code intelligence** — structural analysis, symbol search and dependency exploration.
- **Quality checks** — lint, types, tests, coverage, security and project conventions.
- **Editing and refactoring** — batch edits with validation and rollback support,
  plus Python symbol refactoring.
- **Developer workflows** — scaffolding, Git operations and text compaction.

Tools return structured results with a compact text representation for agent
clients. Install the providers you need; the available catalog depends on
the server environment.

For MCP, start with the
[installation and first-call guide](https://forge.axm-protocols.io/axm-mcp/tutorials/quickstart/).
It covers a client-managed **stdio** process and a persistent
**Streamable HTTP** server. For individual tools and Python libraries, browse
the [package catalog](https://forge.axm-protocols.io/packages/).

## Beyond the public tools

Private development explores how to carry that model through complex work:
compose units of work, recover from failed attempts and bring unresolved
decisions back to a person. The aim is to reduce the attention needed to
supervise execution while preserving a clear account of its progress.

Those components are not offered here as public packages. This profile
introduces the direction; the public repositories and their documentation
define what is available to use today.

## Quality and openness

Forge includes tooling to check both code quality and project conventions.
Its [CI](https://github.com/axm-protocols/axm-forge/actions/workflows/ci.yml)
and package documentation expose the relevant checks and usage limits.

Forge is licensed under
[Apache 2.0](https://github.com/axm-protocols/axm-forge/blob/main/LICENSE).
Licensing and availability are specific to each repository; private development
is not a commitment to a public release.

---

<p align="center">
  <a href="https://github.com/axm-protocols/axm-forge">Explore Forge</a> ·
  <a href="https://forge.axm-protocols.io/">Documentation</a> ·
  <a href="https://gabriel.axm-protocols.io/">Blog</a>
</p>
