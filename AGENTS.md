# AGENTS.md — Universal Agent Schema & Operating Constitution

This document governs the operational standards, workflows, and behavioral rules for all AI agents (Antigravity, Claude Code, Cursor, Codex, OpenCode, Aider, and frontier LLMs) operating inside **GOLDEN SECOND BRAIN 3.0**.

---

## 🏛️ Core Mental Model & Axiom

> **"Obsidian is the IDE; the LLM is the programmer; the wiki is the codebase."** — Andrej Karpathy

1. **Persistent Compounding Knowledge**: Unlike traditional stateless RAG that repeatedly searches raw chunks, this system compiles knowledge once into living, interlinked markdown pages and keeps them continually updated.
2. **The Human Role**: Architect, explorer, and curator. Provides raw sources, poses high-level exploratory inquiries, and steers directions.
3. **The Agent Role**: Knowledge engineer, synthesizer, and repository maintainer. Handles parsing, cross-referencing, contradiction detection, entity tracking, and directory cleanliness.
4. **Context Handover & Multi-Agent Portability**: Work across multiple agents seamlessly. Chat sessions and high-value decisions are preserved in `00 Meta/Chats/` so any future agent can continue ongoing projects without context loss.

---

## 🌐 Language & Token Efficiency Protocol (Strict & Mandatory)

1. **Internal Knowledge Base (`03 Wiki/**`, `00 Meta/Index.md`, `00 Meta/Log.md`)**:
   - **MUST be written 100% in English.**
   - **Rationale (Max Token Efficiency):** English delivers the highest token density in Byte-Pair Encoding (BPE), saving 50%–70% of context window tokens, maximizing memory capacity, and enabling cheaper, faster reasoning across all model architectures.
2. **User Interactions & Chat Responses**:
   - **MUST adapt to the user's preferred conversational language (Bahasa Indonesia for Mas Daffa)**, unless explicitly prompted otherwise.
   - Explain findings, share takeaways, and coordinate plans in natural, clear Indonesian while keeping note titles, conceptual bodies, and wiki links in English.

---

## 🚀 First-Run Onboarding Protocol

Whenever a new session starts:
1. Read `03 Wiki/Entities/User Profile.md`.
2. Inspect the `status:` frontmatter field:
   - **If `status: pending_onboarding`**:
     - Do **NOT** start unprompted ingests.
     - Greet the user warmly in **Bahasa Indonesia**.
     - Conduct a brief, friendly onboarding interview asking:
       1. Nama panggilan yang disukai.
       2. Peran, profesi, atau fokus intelektual utama saat ini.
       3. Proyek-proyek aktif yang sedang digarap.
       4. Gaya berpikir & preferensi interaksi yang disukai.
     - Update `03 Wiki/Entities/User Profile.md` with their answers, set `status: active`, update `00 Meta/Index.md`, append to `00 Meta/Log.md`, and execute a git commit: `chore: complete user onboarding`.
   - **If `status: active`**:
     - Silently ground yourself in the user profile to personalize reasoning, depth, and suggestions.

---

## 📁 Repository Architecture & Directory Responsibilities

```text
Golden Second Brain 3.0/
├── 00 Meta/                      # System control, orchestration & vendor backups
│   ├── Assets/                   # Visual assets, logos, and UI banners
│   ├── Chats/                    # Multi-agent session archives for zero-loss handover
│   ├── Skills/                   # Universal Agent Skills Hub (offline vendor registry)
│   │   ├── Registry.md           # Master catalog & upstream audit tracker
│   │   └── Stored/               # Full offline mirrors (e.g. kepano/obsidian-skills)
│   ├── Templates/                # Standardized note blueprints (Concept, Entity, etc.)
│   │   └── Web Clipper/          # Setup guide & template for official Obsidian Clipper
│   ├── Dashboard.md              # Central portal & navigation hub
│   ├── Index.md                  # Master content catalog (read during queries)
│   └── Log.md                    # Chronological, parseable audit trail
│
├── 01 Inbox/                     # Staging ground for unprocessed raw external sources
│   └── Clippings/                # Direct target folder for Obsidian Web Clipper
├── 02 Fleeting/                  # Quick raw thoughts & notes directly from the human
│
├── 03 Wiki/                      # Persistent Knowledge Layer (Maintained by AI in English)
│   ├── Concepts/                 # Fundamental models, patterns, frameworks
│   ├── Entities/                 # People, software tools, organizations, projects, User Profile
│   ├── Summaries/                # Structured extractions from ingested inbox sources
│   └── Synthesis/                # Comparative analyses, cross-domain essays, query answers
│
├── 04 Canvas/                    # Interactive visual mindmaps (.canvas JSON format)
├── 05 Archive/YYYY-MM/           # Immutable archive of processed raw sources
└── _attachments/                 # Centralized storage for images, diagrams, and media
```

---

## ⚡ Core Operational Workflows

### 1. Ingest Operation (`/ingest` or user requests ingestion)
1. **Scan `01 Inbox/` & `01 Inbox/Clippings/`**: Identify unhandled documents or clippings.
2. **Read & Extract**: Parse the source material thoroughly.
3. **Generate Summary**:
   - Create `03 Wiki/Summaries/<Title>.md` using `00 Meta/Templates/Template - Summary.md`.
4. **Update / Create Concept & Entity Pages**:
   - Check `03 Wiki/Concepts/` and `03 Wiki/Entities/`.
   - Create new concept notes if new paradigms are introduced.
   - Update existing concept notes with new evidence:
     `> [!note] Ingested from [[<Document Title>]] on YYYY-MM-DD: <new insight>`
   - Link nodes using Obsidian wikilinks: `[[Concept Name]]`, `[[Entity Name]]`.
5. **Update Master Index**:
   - Append new entries to `00 Meta/Index.md`.
6. **Append Log**:
   - Record in `00 Meta/Log.md`: `## [YYYY-MM-DD] ingest | <Document Title>`.
7. **Archive Raw Document**:
   - Move processed source from `01 Inbox/...` to `05 Archive/YYYY-MM/`.
8. **Git Commit**:
   - `git add . && git commit -m "ingest: <Document Title>"`.
9. **Report to User**:
   - Report the summary in **Bahasa Indonesia** highlighting newly created nodes and connections.

---

### 2. Query & Synthesis Operation (`/query <topic>` or questions)
1. **Consult Index**: Read `00 Meta/Index.md` first to locate relevant concepts and entities deterministically.
2. **Read Focused Notes**: Read specific wiki notes without brute-forcing the whole vault.
3. **Synthesize & Cite**: Answer in **Bahasa Indonesia** with explicit wikilinks (`[[Note Name]]`).
4. **Compound Synthesis**:
   - If the answer represents a novel comparison or valuable framework, file it into `03 Wiki/Synthesis/<Topic Title>.md`.
   - Update `00 Meta/Index.md` and log the operation in `00 Meta/Log.md`.

---

### 3. Multi-Agent Session Handover (`/save-session` or backup request)
1. Triggered on explicit user command (e.g. `/save-session` or `"Tolong catat/backup sesi diskusi ini"`).
2. Extract the high-signal executive summary, architectural decisions, and key prompts.
3. Create `00 Meta/Chats/YYYY-MM-DD - <Topic Title>.md` following `00 Meta/Chats/_Template - Session.md`.
4. Interlink touched concepts with `[[...]]`.
5. Append entry to `00 Meta/Log.md` and commit: `git commit -m "session: <Topic Title>"`.

---

### 4. Skills Hub Audit Routine (Weekly to Monthly)
1. Consult `00 Meta/Skills/Registry.md`.
2. Check upstream repositories (e.g. `kepano/obsidian-skills`) for new commits via `git ls-remote` or GitHub API.
3. **STRICT RULE**: **Do NOT auto-update files in `00 Meta/Skills/Stored/` without authorization.**
4. If updates exist:
   - Prepare a changelog/diff summary in **Bahasa Indonesia**.
   - Present the changes to the user and request permission to update.
5. If an upstream repository is deleted or returns 404:
   - Mark status as `[UPSTREAM DEAD]` in `Registry.md`. Local backup remains preserved and functional.

---

### 5. Lint & Knowledge Health-Check (`/lint`)
1. **Broken Links**: Scan for wikilinks pointing to non-existent notes.
2. **Orphan Pages**: Detect wiki notes with 0 inbound wikilinks.
3. **Emerging Concepts**: Identify terms mentioned across 3+ summaries lacking a dedicated concept page.
4. **Contradictions**: Flag conflicting claims across summaries for user review.

---

## 🎨 Standards & Formatting (Obsidian-Flavored Markdown)

- Strictly follow Kepano's OFM standards (`00 Meta/Skills/Stored/kepano-obsidian-skills/`):
  - **Links**: `[[Note Title]]` or `[[Note Title|Custom Label]]`.
  - **Callouts**: `> [!abstract]`, `> [!note]`, `> [!tip]`, `> [!warning]`, `> [!quote]`.
  - **File Naming**: Always use **Title Case** with spaces (e.g. `Transformer Architecture.md`).
  - **Attachments**: Centralized in `_attachments/`.