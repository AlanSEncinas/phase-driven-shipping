# phase-driven-shipping

A universal Claude Code skill for solo operators and small teams who want a disciplined shipping rhythm: morning calls, phase-prefixed commits, idea triage, doubt handling, and same-session doc updates. Acts as a **router** — engineering work hands off to the [superpowers](https://agentskills.io) skill suite (brainstorming, TDD, systematic-debugging, verification-before-completion, etc.) at the right moments, so you only have to think about one skill.

Built while shipping a multi-agent sales orchestrator from concept to production. Refined the whole way.

## Philosophy

**Project docs are the source of truth, not memory.**

- `BUILD_PLAN.md` — forward-looking, live checkboxes by phase
- `CLAUDE.md` — backward-looking architecture reference + dated changelog
- `BACKLOG.md` — destination for ideas not in the current phase

Every session opens with a morning call (where are we, what shipped last, today's next action) and closes with one concrete next action. New ideas get triaged to the backlog instead of opening a second front. Self-doubt gets countered with project metrics, not pep talks. Trigger words (`commit`, `done for today`, `ship it`) open auto-commit mode for the rest of the session — no re-asking each time, just phase-prefixed messages and matching doc updates.

## What you get

| File | Role |
|------|------|
| `SKILL.md` | The skill itself — auto-loads when conditions match |
| `BUILD_PLAN.template.md` | Copy to project root as `BUILD_PLAN.md` |
| `BACKLOG.template.md` | Copy to project root as `BACKLOG.md` |

## Routing table preview

The skill is a front door. Engineering work routes to specialized superpowers skills:

| Situation | Hands off to |
|-----------|--------------|
| New feature, component, or behavior change | `superpowers:brainstorming` |
| Multi-step task with a written spec | `superpowers:writing-plans` |
| Implementing any code | `superpowers:test-driven-development` |
| Bug, test failure, unexpected behavior | `superpowers:systematic-debugging` |
| About to claim work is done | `superpowers:verification-before-completion` |
| Major feature complete | `superpowers:requesting-code-review` |
| Branch ready to integrate | `superpowers:finishing-a-development-branch` |

Session bookends, mid-phase ideas, doubt, and trigger words stay inside this skill.

## Install

Clone into your local Claude Code skills directory.

**macOS / Linux:**
```bash
cd ~/.claude/skills
git clone https://github.com/AlanSEncinas/phase-driven-shipping.git
```

**Windows (PowerShell):**
```powershell
cd "$env:USERPROFILE\.claude\skills"
git clone https://github.com/AlanSEncinas/phase-driven-shipping.git
```

The skill is auto-discovered by Claude Code on next session start.

## Requirements

- **Claude Code** — the CLI, desktop app, web app, or IDE extension
- **superpowers plugin** — the routing table delegates engineering work to the [superpowers](https://agentskills.io) skill suite. Without it, the cross-referenced skills (brainstorming, TDD, debugging, verification, etc.) won't be available and the router has nowhere to hand off to.

## How to use

You don't need to invoke anything manually. The skill triggers automatically when:

- You start a new session
- You say `commit` / `done for today` / `ship it`
- You propose a new idea while in the middle of a phase
- You express doubt about progress
- You signal a session is ending

When engineering work happens (writing code, fixing bugs, planning features), the routing table tells Claude which superpowers skill to invoke. You just talk about the work.

## Adapting it

Fork the repo, edit `SKILL.md` to match your voice or tweak the rules, and reinstall. Common edits people make:

- Add their own trigger words alongside the defaults
- Tighten or relax the layer definitions in `BUILD_PLAN.template.md`
- Add domain-specific routing rows (e.g., for design work, content creation, or data analysis)
- Adjust the doubt-handler examples to match the project's metrics

## Contributing

Issues and PRs welcome. The skill itself is short, opinionated, and pressure-tested in real use. Suggest changes that solve real friction, not theoretical ones.

## License

MIT — see [LICENSE](./LICENSE).
