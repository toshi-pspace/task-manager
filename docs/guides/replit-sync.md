# Replit ↔ Local Sync (Git/GitHub)

Goal: one GitHub repo is the shared brain. Replit, Claude Code, Codex, and
Antigravity all read/write the same `.agent/` memory through it.

## One-time setup
1. **Create the GitHub repo** (empty) for the project.
2. **Local:** copy this template into `1-Projects/<name>/`, then:
   ```
   cd "1-Projects/<name>"
   git init
   git add .
   git commit -m "Init from PARA template"
   git remote add origin git@github.com:<you>/<repo>.git
   git push -u origin main
   ```
3. **Replit:** create the Repl by importing from that GitHub repo
   (or in an existing Repl: Tools → Git → connect to the repo).

## Daily rhythm
- **Start of session (any tool):** `git pull` first — get the latest `.agent/STATE.md`.
- **End of session:** the agent updates `.agent/STATE.md`, then:
  ```
  git add -A && git commit -m "<what changed>" && git push
  ```
- On Replit, use the Git pane's Pull / Commit / Push buttons — same effect.

## Why this delivers cross-tool memory
`.agent/STATE.md` is committed to the repo. Whoever pulls next — Replit's agent
in the cloud, or Claude Code on your Mac — reads exactly where the last session
left off. The repo, not any single tool, holds the memory.

## Gotchas
- **Never gitignore `.agent/`.** The template's `.gitignore` has `!.agent/` to force-track it. If memory isn't syncing, check this first.
- **Pull before you start** to avoid merge conflicts on `STATE.md`.
- If two tools edit simultaneously and conflict, `STATE.md` is plain Markdown — resolve by hand, keep both sets of notes.
