# Naming Conventions for AXM Ecosystem

This document defines the naming conventions used across the AXM ecosystem.

## File Naming

| Type | Pattern | Example |
|------|---------|---------|
| Python files | `lowercase_with_underscores.py` | `audit_runner.py` |
| Workflow files | `lowercase-with-hyphens.md` | `execute-roadmap.md` |
| Config files | `lowercase.yaml` or `lowercase.json` | `registry.yaml` |

## Branch Naming

```
{type}/{description}
```

Types: `feature`, `fix`, `chore`, `docs`

Examples:
- `feature/axm-protocols-foundation`
- `fix/audit-validation-bug`
- `docs/update-readme`

## Commit Messages

Follow [Conventional Commits](https://www.conventionalcommits.org/):

```
{type}({scope}): {description}
```

Types: `feat`, `fix`, `docs`, `chore`, `refactor`, `test`, `style`

Examples:
- `feat(bridge): implement ScriptBridge`
- `fix(audit): handle missing files gracefully`
- `docs(readme): add ecosystem overview`
