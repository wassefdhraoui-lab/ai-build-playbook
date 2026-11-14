# Master rules (read first, every project)

You are helping me build a small, finished, public project that a visitor can try on their own.

## What to read
1. `PROJECT_BRIEF.md` in the project root (it has a `Category:` line).
2. Everything in `core/` (workflow, architecture, security, quality-checklist, deploy).
3. Only `types/<category>.md` that matches the brief.
   If that file is empty, tell me, ask up to 3 questions, and write down the problems you meet in `LESSONS_NEW.md` so the file can be filled later.
4. Skills: if types/<category>/skills/ exists, pick the skills the brief needs.
   - Before the 5-line plan, write one line: "Skills I will use: X, Y (because ...)". If none apply, say so.
   - Open only the SKILL.md files you picked, and the files inside them that you need.
   - Do not read skills that do not match the idea.
   - If the brief changes later and needs another skill, read it at that point.
## How we work
- If the brief is missing or unclear, ask at most 3 questions, then complete it.
- Before coding, write a 5-line plan and wait for my OK.
- Ask first before: deleting files, adding a dependency, calling an external service, touching secrets or deployment.
- Small steps. Commit after each working step (`feat:`, `fix:`, `docs:`, `chore:`).
- Run lint, typecheck, build and tests yourself. Report the real output. Never claim a check passed if you did not run it.
- Never invent data: no fake reviews, numbers, clients or demo users.
- Prefer the simplest thing that works.

## Lessons loop
When a problem takes more than 10 minutes, or the same mistake happens twice, append an entry to `LESSONS_NEW.md`
in the project using the format in `lessons/LESSONS.md`. Do it right away, not at the end.
