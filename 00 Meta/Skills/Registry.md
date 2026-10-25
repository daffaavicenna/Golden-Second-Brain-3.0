---
type: registry
title: "Universal Agent Skills Registry"
updated: 2026-10-25
status: active
---

# 🛡️ Universal Agent Skills Hub & Registry

> **Purpose:** This registry serves as the Single Source of Truth and offline vendor backup for all AI Agent Skills powering **Golden Second Brain 3.0**. 
> All skill repositories stored here are complete offline mirrors (`00 Meta/Skills/Stored/`) to prevent link rot, upstream repository deletions, and unexpected breaking changes.

---

## 📋 Audit & Maintenance Policy

1. **Audit Cadence:**
   - Minimum: **Once every week** (e.g. every Monday).
   - Maximum interval: **Once every month**.
2. **Strict Change Control Protocol:**
   - **Never auto-update or overwrite local skills blindly.**
   - Upon detecting upstream changes, the AI agent **MUST** generate a diff/changelog report.
   - Present the changes to the user in **Bahasa Indonesia**.
   - Only apply updates to `Stored/` after explicit user authorization.
3. **Upstream Disappearance (Dead Repo Mitigation):**
   - If an upstream repository returns `404` or is deleted, update the status to `[UPSTREAM DEAD]`.
   - The offline mirror in `00 Meta/Skills/Stored/` remains 100% functional and preserved.

---

## 📦 Installed & Backed-Up Skills

| Skill Package | Local Path | Upstream URL | Backed Up Commit | Status | Last Audit |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **kepano/obsidian-skills** | `00 Meta/Skills/Stored/kepano-obsidian-skills` | https://github.com/kepano/obsidian-skills | `3ccff53` | `🟢 Active` | 2026-10-25 |

---

## 🛠️ Included Sub-Skills in `kepano-obsidian-skills`

- **`obsidian-markdown`**: Strict Obsidian-Flavored Markdown (OFM) rules, wikilinks, callouts, and frontmatter.
- **`json-canvas`**: Generate native `.canvas` interactive visual mindmaps.
- **`obsidian-bases`**: Syntax and logic for Obsidian Bases (`.base`).
- **`obsidian-cli`**: Headless CLI control for Obsidian vault automation.
- **`defuddle`**: HTML/webpage clutter extractor for clean markdown conversions.
- **`knap`**: Data-to-markdown templating engine.

---

## 🚀 How to Export / Install to External Agents

If you are setting up another AI agent on your system:
- **Claude Code:** Link or copy `00 Meta/Skills/Stored/kepano-obsidian-skills/` into your `~/.claude/` or `.claude/skills/`.
- **OpenCode:** Link to `~/.opencode/skills/`.
- **Codex / OpenClaw:** Reference the local path in agent configuration.
