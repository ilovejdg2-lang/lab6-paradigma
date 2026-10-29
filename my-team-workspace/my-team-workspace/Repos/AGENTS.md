# Repos

> **TL;DR:** Index of independently versioned project clones. Only this file is tracked by the workspace Git; each project under `Repos/` keeps its own repository and history.

## Purpose

`Repos/` holds cloned source repositories used from this team workspace. The workspace repository does **not** incorporate project contents or their Git histories.

## Rules

1. Each project under `Repos/<name>/` maintains its **own** version control (its own `.git`).
2. Before working in a clone, read that repository’s root `AGENTS.md` (and OpenSpec / tests if present).
3. Do not commit project files into the workspace parent repository; they are ignored via:

   ```gitignore
   /Repos/*
   !/Repos/AGENTS.md
   ```

4. Durable project facts (architecture, Auth0, deploy status) live in the workspace memory at `../brain/` — never store secrets, tokens, or `.env` values there.
5. The parent repo `lab6-paradigma` versions this `Repos/AGENTS.md` and the rest of the workspace docs; it does **not** version clone contents under `Repos/<project>/`.

## Clones in this workspace

| Folder | Product | Remote (verified) | Notes |
|--------|---------|-------------------|-------|
| [lab5-paradigmas/](lab5-paradigmas/) | UNA Chat (Laboratorio 5 → Lab 8 US-01) | `https://github.com/ilovejdg2-lang/lab5-paradigmas.git` | Express + Socket.IO + HTML/jQuery. Open this folder when working on the chat. Memory for the lab is at `../../brain/` relative to the clone (i.e. workspace `brain/`). |

## Memory reference

- Workspace brain: `../brain/` (from this file) or `my-team-workspace/my-team-workspace/brain/` from the Cursor multi-root layout.
- Start of session: read `../brain/daily-log/status.md` and today’s diary under `../brain/daily-log/`.
