# Build Plan — phase-driven-shipping

> Forward-looking source of truth for what ships next on the skill itself. Update checkboxes in the same commit as the work. See `CLAUDE.md` §5 for backward-looking changelog. See `BACKLOG.md` for ideas not in the current layer.

**Current phase:** Layer 2 — Stability & Adoption
**Today's next action:** User tests fresh-session auto-fire (commit `db092b8`). If it fires → mark below. If not → escalate description.

---

## Layer 1 — Foundation (SHIPPED)

**Done when:** Public repo exists, skill installs cleanly via `git clone`, skill auto-fires on session start in a real project.

- [x] Write SKILL.md v1 (routing table, morning call, idea triage, doubt handler, commit discipline, red flags) — `20f4708`
- [x] Write BUILD_PLAN.template.md + BACKLOG.template.md — `20f4708`
- [x] Write README.md (philosophy, install, requirements) — `20f4708`
- [x] MIT LICENSE — `20f4708`
- [x] `git init` + first commit on `main` — `20f4708`
- [x] Fix README install URL (correct GitHub username) — `2913e9b`
- [x] Push to public repo at github.com/AlanSEncinas/phase-driven-shipping — pushed at session 1
- [x] Tighten description for reliable auto-fire — `db092b8`
- [ ] **User-verified:** auto-fire works in a fresh session ← BLOCKING Layer 2

---

## Layer 2 — Stability & Adoption (current)

**Done when:** Skill fires reliably across cold and warm starts, has been tested by at least one user other than the author, has a clear demo/example showing the morning-call flow.

- [ ] Confirm auto-fire works after the description fix (manual test by Alan)
- [ ] If auto-fire still fails: escalate to "MUST invoke before any other tool call" language and re-test
- [ ] Add a "Quickstart" section to README with a real example session (operator types → skill responds with morning call → operator types "commit" → skill commits + updates docs)
- [ ] Add screenshots or a short asciinema-style transcript to README so the experience is visible before install
- [ ] Get one external user to install and run a session — collect feedback on (a) does it fire, (b) is the morning call valuable, (c) any friction points
- [ ] Address top friction point from external feedback

---

## Layer 3 — Community & Multi-Domain (later)

**Done when:** Skill is discoverable, has community input, supports more than just code projects.

- [ ] Submit to a Claude Code skill marketplace if one exists by then
- [ ] Add domain variants or routing rules for non-code work (writing, design, data analysis, content)
- [ ] Add an `examples/` folder with sample BUILD_PLAN.md / BACKLOG.md for different project types (web app, ML project, blog, ops runbook)
- [ ] Set up an issue template / contribution guide
- [ ] Write a short post/announcement (X / r/ClaudeAI / LinkedIn) to gather initial users
- [ ] Hit 10+ stars on GitHub (loose marker that it's reaching real people)

---

## Demo Status

> Per the skill's own demo-always principle: a working version of the user-facing artifact must exist at every layer.

- **Current demo:** Install via `git clone https://github.com/AlanSEncinas/phase-driven-shipping.git` into `~/.claude/skills/`, restart Claude Code, observe the skill firing. README routing-table + philosophy section is the static demo.
- **Last verified working:** 2026-05-01 (Layer 1 install + push verified end-to-end; auto-fire pending user test post-`db092b8`)
- **Gap:** No video / asciinema / animated GIF showing the experience. Layer 2 task.

---

## Phase History

> One-line summary when a layer fully ships. Detail moves to `CLAUDE.md` §5.

- _Layer 1 in progress — pending final auto-fire verification._
