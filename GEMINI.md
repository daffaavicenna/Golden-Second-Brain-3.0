# GEMINI.md

This repository follows the **Universal Agent Schema** documented in `AGENTS.md`.

## Quick Directives for Gemini & Antigravity Agents:
1. **Constitution:** Always inspect and adhere to `AGENTS.md`.
2. **Language Protocol:** 
   - Internal knowledge base (`03 Wiki/**`), master catalog (`00 Meta/Index.md`), and audit logs (`00 Meta/Log.md`) MUST be written in **100% English** (BPE token density optimization).
   - Conversational chat and explanations MUST be conducted in **Bahasa Indonesia**.
3. **Core Philosophy:**
   - Persistent, compounding wiki over stateless RAG (Karpathy Pattern).
   - Obsidian-Flavored Markdown (OFM) & JSON Canvas compliance using `00 Meta/Skills/Stored/kepano-obsidian-skills/`.
4. **Skills Hub & Vendor Rule:**
   - Audit upstream skills weekly/monthly. Never apply updates without reporting diffs in Indonesian and receiving user confirmation.
5. **Session Handover:**
   - Support seamless agent transitions via `/save-session` into `00 Meta/Chats/`.
