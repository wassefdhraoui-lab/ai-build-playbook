# Lessons log

Format for each entry (newest at the bottom):

```
## YYYY-MM-DD | project | short title
- Problem: what went wrong
- Cause: why
- Fix: what solved it
- Rule: the sentence that prevents it next time (also added to the matching doc)
```

When an entry has a general Rule, copy that rule into the right doc (`02-architecture`, `03-security`, `05-web`, ...).

---

## 2026-11-14 | portfolio | Next.js docs differ from memory
- Problem: the agent can write code from outdated Next.js knowledge.
- Cause: the Jari project uses a very new Next.js version, and its own AGENTS.md warns about breaking changes.
- Fix: read `node_modules/next/dist/docs/` before writing framework code.
- Rule: for any fast-moving framework, read the installed version's docs first.
