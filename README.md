# my-engineering-brain

Engineering notes for me and AI. How I think about designing, organizing, scaling and securing systems, with the books, papers, incidents and projects behind each belief.

It is built to be navigated, not loaded whole. Start at [AGENTS.md](AGENTS.md).

## Using it with an AI
Point the AI at the entry file. Example prompt:

```
Read https://raw.githubusercontent.com/kevinrawal/my-engineering-brain/main/AGENTS.md
and follow its reading protocol. Then help me with: <task>
```

If the AI cannot browse, paste `AGENTS.md`, `about.md` and the relevant `INDEX.md` files, then paste individual notes when it asks for them.

## Layout
| Folder | What lives there |
|---|---|
| `principles/` | What I believe, by domain, with scope and confidence |
| `anti-patterns/` | Things I avoid or dislike, why, and what I do instead |
| `playbooks/` | How I do recurring things (scaffold a service, lay out a repo) |
| `decisions/` | Real decisions from my projects, with outcomes |
| `sources/` | Evidence: books, papers, talks, incidents, projects (never opinions) |
| `stacks/` | Technology-specific notes that implement the general principles |
| `inbox/` | Raw unprocessed notes (ignored by AI) |
| `templates/` | Copy these to start a note |

To add content, see [HOW-TO-ADD.md](HOW-TO-ADD.md).
