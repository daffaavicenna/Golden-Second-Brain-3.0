# 🧠 Golden Second Brain 3.0

> An enterprise-grade, persistent AI-augmented knowledge engine built for [Obsidian](https://obsidian.md).
> Combining the **Andrej Karpathy LLM Wiki Pattern**, **Steph Ango (Kepano) Obsidian Skills**, and a **Multi-Agent Session Handover Architecture**.

---

## 🏛️ Philosophy & Architecture

> *"Obsidian is the IDE; the LLM is the programmer; the wiki is the codebase."* — Andrej Karpathy

Most AI knowledge workflows rely on brute-force RAG (retrieval-augmented generation) that recalculates context from scratch on every query. **Golden Second Brain 3.0** compiles insights once into a living, interlinked knowledge network and keeps it continuously up to date.

```text
Golden Second Brain 3.0/
├── 00 Meta/                      # Control center, orchestration & vendor backups
│   ├── Assets/                   # Logos, banners, visual assets
│   ├── Chats/                    # Multi-agent session archives for zero-loss handover
│   ├── Skills/                   # Universal Agent Skills Hub (offline vendor backup)
│   │   ├── Registry.md           # Master catalog & upstream audit tracker
│   │   └── Stored/               # Full offline mirrors (e.g. kepano/obsidian-skills)
│   ├── Templates/                # Standardized note blueprints (Concept, Entity, etc.)
│   │   └── Web Clipper/          # Setup guide & template for official Obsidian Clipper
│   ├── Dashboard.md              # Central portal & navigation hub
│   ├── Index.md                  # Master content catalog (deterministic query index)
│   └── Log.md                    # Chronological, parseable audit trail
│
├── 01 Inbox/                     # Staging ground for unprocessed raw external sources
│   └── Clippings/                # Direct target folder for Obsidian Web Clipper
├── 02 Fleeting/                  # Quick raw thoughts & notes directly from the human
│
├── 03 Wiki/                      # Persistent Knowledge Layer (Maintained by AI in English)
│   ├── Concepts/                 # Fundamental models, patterns, frameworks
│   ├── Entities/                 # People, software tools, organizations, User Profile
│   ├── Summaries/                # Structured extractions from ingested inbox sources
│   └── Synthesis/                # Comparative analyses, cross-domain essays, query answers
│
├── 04 Canvas/                    # Interactive visual mindmaps (.canvas JSON format)
├── 05 Archive/YYYY-MM/           # Immutable archive of processed raw sources
└── _attachments/                 # Centralized storage for images, diagrams, and media
```

---

## ✨ Key Features in Version 3.0

1. **⚡ Super-Efficient Token Protocol**:
   - Internal knowledge base (`03 Wiki/**`) is strictly maintained in **English** (saving 50%–70% BPE tokens, maximizing LLM context windows).
   - Conversational chat automatically adapts to the user's natural language (e.g., **Bahasa Indonesia**).
2. **🛡️ Universal Agent Skills Hub (`00 Meta/Skills/`)**:
   - Stores full offline vendor backups of essential skills (such as `kepano/obsidian-skills`).
   - Mitigates repository deletions and link rot.
   - Built-in audit cadence (weekly to monthly) with strict rule: **Report diffs first before updating**.
3. **🤝 Multi-Agent Session Handover (`00 Meta/Chats/`)**:
   - Record high-signal decision logs and prompts on-demand via `/save-session`.
   - Seamlessly switch between Antigravity, Claude Code, Cursor, Codex, or OpenCode without context amnesia.
4. **🌐 Seamless Obsidian Web Clipper Integration**:
   - Dedicated `01 Inbox/Clippings/` target keeps the root vault completely clean.
   - Automatic routing of web clips into structured summaries and concept graphs.
5. **🎨 Native Obsidian-Flavored Markdown (OFM) & Canvas**:
   - Strictly conforms to official standards from Obsidian's CEO (Kepano).
   - Interactive `.canvas` JSON mindmaps generated on demand.

---

## 🚀 Getting Started

### 1. Open in Obsidian
1. Open **Obsidian**.
2. Select **Open folder as vault**.
3. Choose `Golden Second Brain 3.0`.
4. Open `00 Meta/Dashboard.md` as your home base!

### 2. First-Run Agent Onboarding
When connecting any AI agent (Claude Code, Gemini, Antigravity, Cursor, etc.):
1. The agent inspects `03 Wiki/Entities/User Profile.md`.
2. It guides you through a friendly 3-4 question onboarding interview.
3. Your active projects, roles, and thinking style are personalized into the vault!

### 3. Core Commands
- `/ingest` : Process unhandled sources in `01 Inbox/`, extract concepts, update wiki, and archive raw file.
- `/query <topic>` : Consult `Index.md`, read relevant wiki notes, and synthesize deep answers.
- `/save-session` : Record the current high-signal agent chat session for seamless cross-agent handover.
- `/lint` : Audit knowledge graph health, find orphan pages, and flag conceptual contradictions.

---

## 📄 License
MIT License. Created by [Daffa' Avicenna](https://github.com/daffaavicenna).
