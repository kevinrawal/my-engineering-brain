# AGENTS.md — read this first

This repo holds the author's engineering thinking: how they design, organize, scale and secure systems, what they prefer, what they reject, and the evidence behind it. It is written to be read by any AI (assistant, agent, or code editor).

It is deliberately **not** meant to be read in full. Navigate it.

## Reading protocol
1. Read this file and `about.md` (author context and default assumptions).
2. Use the routing table below to pick the 1–2 folders relevant to the task.
3. Open that folder's `INDEX.md`. Each line is: title — summary · confidence · tags.
4. Open only the notes whose summaries match the task (usually 2–6). Follow `sources:` or `related:` links only when you need the evidence or a conflicting view.
5. Do not open `inbox/` (raw, unreviewed). Open `sources/` only when you need evidence for a claim.
6. If nothing relevant exists, say so, answer from general knowledge, and label it as not coming from the author's notes.

## Routing table
| If the task is... | Read |
|---|---|
| Designing a new system or service | principles/architecture, principles/data, playbooks |
| Organizing a codebase, repo or modules | principles/codebase-organization, playbooks |
| Designing APIs, contracts, integrations | principles/api-and-contracts |
| Scaling, performance, failure handling | principles/scaling-and-reliability |
| Auth, multi-tenancy, threat modeling, data protection | principles/security |
| LLM, RAG or agent systems | principles/ai-systems |
| Deploy, observability, incidents, on-call | principles/operations, sources/incidents |
| Choosing a technology or approach | decisions, anti-patterns, then principles |
| Anything specific to one technology | stacks/<name> |
| "Why does the author believe X?" | the note's `sources:` → sources/ |

## How to treat the content
- These are one engineer's opinions, not universal truths. Use them as defaults, not laws.
- `confidence`: `strong` = follow unless there is a clear reason not to; `working` = lean toward it and mention alternatives; `hunch` = a hypothesis, do not enforce.
- Respect `applies_when` and `not_when`. If the task is outside that scope, say so instead of forcing the note.
- `status: revisiting` means the author is unsure; `deprecated` means ignore it.
- If a note conflicts with the user's current request or constraints, say so openly and let the user decide. Do not silently override either side.
- When you use a note, name it by path so the author can trace the advice.
- Never invent notes, sources, quotes or citations. Never edit this repo unless asked; when asked to add content, follow `HOW-TO-ADD.md`.

## Core principles (the few that always apply; keep to 10 or fewer)
_Empty. The author adds a line here when a principle reaches `strong` and applies almost everywhere._

## Map
`principles/` · `anti-patterns/` · `playbooks/` · `decisions/` · `sources/` · `stacks/` · `inbox/` · `templates/` · `glossary.md` · `about.md` · `HOW-TO-ADD.md`
