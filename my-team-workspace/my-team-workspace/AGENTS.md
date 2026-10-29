# Workspace

> **TL;DR:** Shared AI-powered team workspace for Lab 8 / UNA Chat — start here, read `brain/daily-log/status.md`, then descend into the relevant `AGENTS.md`.

This is a shared team workspace designed so AI agents (GitHub Copilot, Claude Code, Cursor, etc.) can navigate efficiently using **progressive disclosure** — reading only what they need, when they need it.

**Official path (do not flatten):** `lab6-paradigma/my-team-workspace/my-team-workspace/`.

These workspace documents (`brain/`, Knowledge, Skills, AGENTS, assistant rules) are versioned from the **parent** repository `lab6-paradigma`. Cloned apps under `Repos/` keep their own Git and are ignored by the parent except `Repos/AGENTS.md`.

## Brain (persistent memory)

> Follow the Obsidian brain instructions merged below. Vault path: [`brain/`](brain/).

At the start of every session, read `brain/daily-log/status.md` and today’s diary under `brain/daily-log/`. Log real work to the diary; put durable findings in topic notes; refresh `status.md` before finishing. Never store secrets in the brain.

UNA Chat code lives in `Repos/lab5-paradigmas/` (own Git). From that clone, the brain is at `../../brain/`.

**Harness:** No se realizará el paso 3 del Laboratorio 8: Preparar y utilizar el harness. Por decisión de alcance, no se instalará ni utilizará rsc-harness.

Cursor may also load project rules under `.cursor/rules/` when present; still treat this `AGENTS.md` and `brain/` as the source of truth for Lab 8 context.

## Structure

- [Knowledge/](Knowledge/AGENTS.md) — Durable reference material, notes, and facts about projects, systems, and domains.
- [Skills/](Skills/AGENTS.md) — Reusable, task-specific playbooks the agent can invoke for known classes of work.
- [Repos/](Repos/AGENTS.md) — Index of cloned source code repositories. Actual repos are **not** tracked here (see `.gitignore`: `/Repos/*` + `!/Repos/AGENTS.md`).
- [brain/](brain/INDEX.md) — Obsidian-style second brain for Lab 8 continuity.
- [Machine/](Machine/AGENTS.md) — This-computer-specific items (startup scripts, local config). **Not** tracked in Git (see `.gitignore`).
- [temp/](temp/AGENTS.md) — Scratch space for transient files, working notes, and intermediate artifacts. Safe to clear at any time.

## How to navigate

Each directory contains its own `AGENTS.md` describing its purpose, conventions, and what to expect inside — read that file before doing deep work in a directory (progressive disclosure). Start here, then descend only into the directory relevant to the current task.

### TL;DR convention

Every `AGENTS.md` starts with a one-line `> **TL;DR:**` blockquote directly under its title. When navigating:

1. Read only the title + TL;DR line first — that's usually enough to decide whether the directory is relevant to the current task.
2. Only read the rest of the file if the TL;DR isn't sufficient (e.g. you need conventions, examples, or the what-belongs/doesn't-belong rules).
3. Do not skip the TL;DR itself — it's the cheapest signal for whether to go deeper.

When adding a new `AGENTS.md`, write its TL;DR last, after the rest of the content is settled, so it accurately compresses the file.

## Getting Started

1. **Clone this repo** to your machine.
2. **Create your personal Knowledge base:** `Knowledge/{YourName}-Brain/` (add it to `.gitignore` if you want it private, or leave it shared).
3. **Link your repos:** Create a junction/symlink at `Repos/` pointing to your local repositories folder, or just use `Repos/AGENTS.md` as an index.
4. **Configure MCP servers:** Edit `.vscode/mcp.json` with the tools this workspace should use.
5. **Add team knowledge:** Document your projects, conventions, and architecture in `Knowledge/`.

## MCP Servers

MCP server configuration lives in [.vscode/mcp.json](.vscode/mcp.json). Add the servers this workspace should use.

## Customization

- **copilot-instructions.md** — Global rules applied to every AI interaction. Edit `.github/copilot-instructions.md` to set team-wide conventions.
- **AGENTS.md in every directory** — Add one to any new folder so agents (and humans) know what it contains.
