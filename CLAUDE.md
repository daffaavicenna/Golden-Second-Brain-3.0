# CLAUDE.md

This repository follows the **Universal Agent Schema** documented in `AGENTS.md`.

## Quick Directives for Claude Code:
1. **Constitution:** Always inspect and adhere to `AGENTS.md`.
2. **Language Protocol:** 
   - All internal wiki notes (`03 Wiki/**`), master catalog (`00 Meta/Index.md`), and audit logs (`00 Meta/Log.md`) MUST be written in **100% English** for maximum token efficiency.
   - User chat interactions MUST be conducted in **Bahasa Indonesia** (unless instructed otherwise).
3. **Core Philosophy:**
   - Persistent, compounding wiki over stateless RAG (Karpathy Pattern).
   - Obsidian-Flavored Markdown (OFM) compliance using skills in `00 Meta/Skills/Stored/kepano-obsidian-skills/`.
4. **Skills Hub & Vendor Rule:**
   - Never auto-overwrite skill files in `00 Meta/Skills/Stored/` without presenting a diff report to the user first.
5. **Session Handover:**
   - When requested (`/save-session`), record structured context logs in `00 Meta/Chats/` using `00 Meta/Chats/_Template - Session.md`.
