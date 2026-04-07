# ui-scout

> A Claude Code skill that requires searching existing component sources before building from scratch.

![Claude Code](https://img.shields.io/badge/Claude_Code-skill-blue)
![License](https://img.shields.io/badge/license-MIT-green)

---

## The Problem

Claude rebuilds components that already exist in better form.

Modals, dropdowns, buttons, date pickers — rebuilt from scratch, without the accessibility work, edge case handling, and browser compatibility that production-grade libraries already provide.

---

## Before / After

**Without ui-scout**
```
You: Add a combobox to the form

Claude: [starts building custom combobox: 200+ lines, basic keyboard support,
no ARIA, no accessibility testing — reinvents what cmdk already does perfectly]
```

**With ui-scout**
```
You: Add a combobox to the form

Claude: Checking sources first...
shadcn/ui has a Combobox built on cmdk — covers 100% of the requirement.
Adapting to match the design system.
[20 lines, full accessibility included]
```

---

## Install

```bash
mkdir -p ~/.claude/skills/ui-scout
curl -o ~/.claude/skills/ui-scout/SKILL.md \
  https://raw.githubusercontent.com/Feli2arias/ui-scout/main/SKILL.md
/ui-scout
```

---

## What It Enforces

| Rule | Why |
|------|-----|
| Search before building: 21st.dev → shadcn → Aceternity → Radix → build | Reuse over rebuild |
| ≥80% match → adapt, don't rebuild | Right threshold |
| Use 21st.dev MCP tools when available | Fastest path to quality |
| Attribution comment when adapting | Traceability |
| Build from scratch only as last resort | Explicit decision |

---

## What It Doesn't Change

Component quality, accessibility, and design fidelity are never compromised.

---

## License

MIT
