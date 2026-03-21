# Claude Memory — Obsidian Vault Template

This is the Obsidian vault template for use with [claude-memory](https://github.com/your-org/claude-memory).

## What This Is

A pre-configured Obsidian vault that pairs with claude-memory to give Claude Code
persistent, structured memory across sessions. The vault provides the human-readable
narrative layer; claude-memory provides the deep technical archive.

## Setup

This vault is cloned automatically by `setup-hooks.sh` during claude-memory installation.
You do not need to clone it manually.

If you want to set it up manually:

```bash
git clone <this-repo> ~/code/vault
```

Then open Obsidian → **Open folder as vault** → point to `~/code/vault`.

## Folder Structure

```
vault/
├── Calendar/          # Calendar and scheduling notes
├── Claude/
│   ├── Knowledge-Base/    # Distilled facts, patterns, learnings
│   │   └── Learnings Log.md   # Auto-populated by promote-to-obsidian
│   ├── Scratch/           # Temporary drafts (gitignored)
│   └── Session-Logs/      # Per-session logs (auto-written by agent)
├── Events/            # Events and happenings
├── Projects/          # One subfolder per project
│   └── <Project Name>/
│       ├── Current State.md   # Living project status
│       ├── Decisions Log.md   # Architecture decisions (auto-appended)
│       └── Open Questions.md  # Unresolved questions
├── Research/          # Background knowledge and references
└── CLAUDE.md          # Auto-loaded by Claude Code every session
```

## How It Works

1. **claude-memory** captures every Claude Code session automatically via PreCompact hook
2. After significant sessions, run `promote-to-obsidian.py <snapshot_id>` to write insights here
3. The agent writes: session log, decisions, learnings — based on what the session contains
4. Obsidian becomes a live, auto-populated knowledge base of your development work

## Making It Your Own

- Edit `CLAUDE.md` to add your active projects
- Add `[[Projects/<Name>/Current State]]` links for each project you start
- The vault is a private git repo — push to your own remote to keep it portable

## What Gets Committed

- All `.md` notes
- `.obsidian/` config (plugins, theme, hotkeys) — keeps settings in sync across machines
- `CLAUDE.md`

**Not committed:** `workspace.json` (machine-specific), Scratch/ contents, `.DS_Store`
