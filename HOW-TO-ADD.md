# How to add things (rules for me and for any AI helping me)

This file is the authority on how the repo is maintained. Change the rules freely; keep this file current.

## 1. Pick the type
| I want to record... | Type | Folder |
|---|---|---|
| Something I believe about how systems should be built | principle | `principles/<domain>/` |
| Something I avoid or dislike, and what I do instead | anti-pattern | `anti-patterns/` |
| A repeatable way I do a task | playbook | `playbooks/` |
| A real choice I made on a project, and how it turned out | decision | `decisions/` |
| What a book, paper, talk, incident or project taught me | source | `sources/<kind>/` |
| A technology-specific implementation of a principle | stack note | `stacks/<stack>/` |
| A half-formed thought | raw note | `inbox/` |

If unsure, drop it in `inbox/` and move on. Never block yourself on structure.

## 2. Order of work
1. **Source first.** When something comes from a book, paper, talk, incident or project, create or update its source note (`templates/source.md`).
2. **Then the notes it produced.** Create principles, anti-patterns or playbooks. Each must list its source(s) in `sources:`.
3. **Back-link.** Add the new note to the source's "Led to" section.
4. **Index.** Add one line to the `INDEX.md` of the folder the note lives in.

## 3. Writing a note
- Copy the matching file from `templates/`. Filename: `kebab-case.md`, descriptive, unique across the repo, never renamed (to retire a note, set `status: deprecated`).
- Required frontmatter: `title`, `type`, `summary`, `confidence`, `status`, `updated`. The `summary` is one sentence and is copied into the index line.
- Always fill `applies_when` and `not_when` for principles and anti-patterns. A rule without a scope gets over-applied.
- Write in my own words, in the first person where natural. The first lines of a note must be usable on their own, because an AI may read only those.
- Keep notes under ~300 words. If longer, split into two notes and link them.
- General notes do not depend on a technology. Mention a tool only as an example. Tool-specific detail goes in `stacks/<stack>/` and links up to the principle it implements.

## 4. Links and references
- Use repo-root paths everywhere in frontmatter and body links, for example `sources/books/ddia.md#ch5`. Never use bare titles or chat links.
- A source can feed many notes; a note can cite many sources.
- Weigh evidence by `evidence_type` on the source: `experienced` (I lived it) and `postmortem` outrank `empirical`, which outranks `opinion`.

## 5. Index line format
`- [Title](file.md) — one-sentence summary · confidence · tag, tag`

When an INDEX.md grows past ~25 lines, split by sub-topic into sub-folders and keep a short parent index.

## 6. Confidence and change
- New belief: `hunch`. Used and held up: `working`. Proven through repeated use or an incident: `strong`.
- When new evidence contradicts a note, do not delete. Set the old note to `status: revisiting`, describe the tension in both notes under "Tradeoffs and tensions", and decide later.
- Promote a principle into `AGENTS.md` core principles only when it is `strong` and applies almost everywhere.

## 7. Public-repo safety
- Nothing from an employer or client: no company names, internal systems, customer data, or non-public incidents. Generalize or anonymize first.
- No copy-pasted passages from books or papers. Paraphrase; short quotes only, with a source link.
- No secrets, tokens, hostnames, or internal URLs.

## 8. When an AI helps me write notes
- It follows this file and uses the templates.
- It may draft structure and wording from my raw input, but I review it. It must never invent sources, quotes, page numbers or incidents; missing evidence stays blank.
- It adds the index line and back-links in the same change.
