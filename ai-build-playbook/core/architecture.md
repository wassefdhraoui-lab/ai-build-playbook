# Architecture rules

- TypeScript strict mode everywhere.
- Layers: `data/` (content, config), `lib/` (pure logic, no UI), `components/` (UI), `app/` or `pages/` (routing).
- One responsibility per file. If a file passes ~200 lines, split it.
- Content (texts, lists, links) lives in data files so it can change without touching components.
- No global mutable state unless the project needs it. Prefer passing data down.
- Name things for what they are (`calculateScore`, not `handleStuff`).
- Pure logic gets unit tests. UI gets at least one end-to-end smoke test (page loads, main action works).
- Folder layout for a web project:

```
src/
  app/          routes
  components/   reusable UI
  data/         content and config
  lib/          pure helpers
  styles/       tokens + global css
tests/
public/
```

- Decision log: when a non-obvious choice is made, add one line to `DECISIONS.md` in the project (what, why).
