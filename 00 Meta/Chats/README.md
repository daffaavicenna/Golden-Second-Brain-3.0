---
type: documentation
title: "Multi-Agent Session Handover System"
updated: 2026-10-25
---

# 🤝 Multi-Agent Session Archive & Context Handover

## Overview
This directory acts as the **Context Bridge** across multiple AI agents (Antigravity, Claude Code, Cursor, Codex, OpenCode, or future frontier models).

### The Core Problem Solved: Context Amnesia & Agent Lock-In
When working across diverse AI tools, context is traditionally fragmented across isolated web interfaces and IDE chat histories. By persisting curated session logs into this directory:
1. **Zero Context Loss:** Any agent can read past session records and immediately resume complex multi-step workflows.
2. **High-Signal Knowledge:** Only pivotal decisions, architectural conclusions, and high-value prompt dialogues are preserved (filtering out conversational fluff, raw token dumps, and transient debugging errors).
3. **Graph Interconnection:** Sessions link directly to permanent concepts in `03 Wiki/Concepts/` and entities in `03 Wiki/Entities/`.

---

## ⚡ How to Trigger Session Backup

You can trigger a session backup at any time with commands such as:
- `/save-session`
- `"Tolong backup / catat sesi diskusi ini ke vault"`
- `"Record this session for handover to another agent"`

### Protocol Followed by the Agent:
1. Read `00 Meta/Chats/_Template - Session.md`.
2. Extract the high-signal executive summary, architecture decisions, and high-value excerpts.
3. Save the note as `00 Meta/Chats/YYYY-MM-DD - <Topic Title>.md`.
4. Add bidirectional links (`[[...]]`) to touched wiki concepts and entities.
5. Log the session creation in `00 Meta/Log.md`.
