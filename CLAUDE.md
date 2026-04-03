# Claude Context — Vault Root

This file is automatically loaded by Claude Code at the start of every session.
Keep it concise — every line costs context tokens.

## Vault Overview
This is an Obsidian vault paired with the claude-memory system.

**Folders:**
- `Calendar/` — calendar and scheduling notes
- `Claude/` — Claude's working folder (session logs, knowledge base, scratch)
- `Events/` — events and happenings
- `Projects/` — active and archived projects
- `Research/` — background knowledge, references, reading notes

## Claude's Working Space
- `Claude/Session-Logs/` — write a session summary at the end of each conversation
- `Claude/Knowledge-Base/` — distilled facts, patterns, and reusable insights
- `Claude/Scratch/` — drafts and temporary work in progress

## Session Protocol
**Start:** Read this file (done), then read `Projects/<Name>/Current State.md` for any active project.
**End:** Update `Current State.md`, append a log to `Claude/Session-Logs/YYYY-MM-DD.md`.

## Formatting Conventions
- YAML frontmatter on all notes with `tags`, `created`, `status`
- Headings for structure (not bold text)
- Wikilinks `[[Note Name]]` for internal links
- Callouts `> [!note]` for highlighted info
- Nested tags: `#project/active`, `#status/draft`, `#type/log`

## Authorship
At session start, run `git config user.name` and store the result as the session author.
If the command returns nothing, fall back to `whoami`.
Add an `author` field to the YAML frontmatter of every `.md` file you create or append to.

## Active Projects
<!-- Add your active projects here, e.g.: -->
<!-- - [[Projects/My Project/Current State]] -->
