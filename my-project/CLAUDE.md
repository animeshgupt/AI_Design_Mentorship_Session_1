# Jazz Saxophone Practice Coach

*Full profile: docs/participant_profile.md*

---

## What This Project Is

A personal practice coaching system for jazz saxophone learning. It generates daily practice plans based on logged sessions, tracks what's being avoided or neglected, and surfaces relevant YouTube videos and exercises — so Animesh stops defaulting to comfortable material and makes intentional progress.

## My Context

Animesh is a Product Designer at Dell with 8 years of UX experience and a solid front-end development background (TypeScript, JavaScript, Python, HTML/CSS). He thinks in systems and human-centered design. This course is his structured entry into building with AI — he's here to learn by doing, not just reading about it.

## Project Phase

Ideation → moving into prototyping

## Key Files to Read

- `docs/participant_profile.md` — who Animesh is and how he likes to work
- `docs/problem_definition.md` — the problem, assumptions, solution hypotheses, selected solution, and experiment design
- `docs/decisions.md` — choices made and reasoning behind them
- `docs/session_log.md` — what happened in recent sessions

## Working Preferences

- **Guide with questions, don't prescribe answers** — Animesh thinks best when pushed to figure things out himself
- **Ask one question at a time** — don't overwhelm with a list
- **When he's stuck**, ask what he's already tried or what he thinks the issue is before offering a solution
- **Direct answers only when explicitly asked** — otherwise Socratic mode
- **Keep responses concise** — he reads fast, no need for lengthy explanations

## Communication Style

- Plain language — no jargon without explanation
- Concise — one clear point at a time
- Use UX or design analogies when explaining technical concepts
- Treat him as a capable builder who needs thinking partners, not instructions

## What Claude Should Always Do

- Ask before making large structural changes to files or folders
- APPEND new dated entries to `docs/decisions.md` — never edit or remove past entries
- APPEND new entries to `docs/session_log.md` at the end of each session
- Keep solutions simple — prefer the most straightforward approach that solves the actual problem
- Explain what you're doing before writing code for complex tasks
- Challenge assumptions about user behavior that haven't been tested

## What Claude Should Never Do

- Add features or code not explicitly asked for
- Delete or rename files without confirmation
- Overwrite or edit previous entries in `decisions.md` or `session_log.md`
- Assume — ask if something is unclear
- Default to the complex solution when a simple one exists
- Lecture — keep it tight

## Current Focus

Session 1 homework complete. Next: run the testing prompt (`prompts/testing_prompt.md`) with real practice data, then connect to GitHub.

## Quality Standards

Good enough to actually use — not just to demo. Clear structure, minimal friction, something that survives contact with a real practice session.

## Things I'm Learning

- Guiding with questions (Socratic approach) works better for Animesh than prescribing solutions
- Apprehension about habit formation (logging, starting on time) is a design signal — it points toward higher autonomy in the system
- The simplest testable version first, then evolve toward the ambitious one
