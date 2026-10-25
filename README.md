<div align="center">

<img src="00%20Meta/Assets/golden-brain-logo.png" alt="Golden Second Brain Logo" width="220" />

# 🧠 GOLDEN SECOND BRAIN 3.0
### The Autonomous, Compounding AI Knowledge Operating System for Obsidian

[![Obsidian](https://img.shields.io/badge/Obsidian-v1.6+-7C3AED?logo=obsidian&logoColor=white)](https://obsidian.md)
[![License: MIT](https://img.shields.io/badge/License-MIT-F59E0B.svg)](LICENSE)
[![Karpathy Wiki Pattern](https://img.shields.io/badge/Pattern-Karpathy%20LLM%20Wiki-10B981)](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f)
[![Kepano OFM Standards](https://img.shields.io/badge/Standards-Kepano%20Obsidian%20Skills-3B82F6)](https://github.com/kepano/obsidian-skills)
[![Multi-Agent Ready](https://img.shields.io/badge/Agents-Universal%20Handover-EC4899)](#-multi-agent-session-handover)

---

**[ 🇮🇩 Baca dalam Bahasa Indonesia ](#-panduan-bahasa-indonesia)** &nbsp;|&nbsp; **[ 🇬🇧 Read in English ](#-english-documentation)**

---

</div>

<br />

<div id="-panduan-bahasa-indonesia"></div>

# 🇮🇩 Panduan Bahasa Indonesia

## 🌟 Tentang Golden Second Brain 3.0

Kebanyakan sistem AI & catatan saat ini menggunakan metode **RAG (Retrieval-Augmented Generation)** biasa: Anda mengunggah file, lalu AI mencari potongan teks setiap kali Anda bertanya. Kelemahannya, **AI tidak pernah benar-benar belajar atau mengumpulkan pengetahuan jangka panjang**. Setiap pertanyaan dijawab dari nol tanpa ada akumulasi wawasan.

**Golden Second Brain 3.0** mengadopsi filosofi revolusioner dari **Andrej Karpathy (Founding Member OpenAI / ex-Tesla AI Director)**:
> *"Obsidian adalah IDE-nya; LLM adalah programmernya; dan Wiki adalah codebase-nya."*

Sistem ini mengubah Obsidian Anda menjadi **basis pengetahuan hidup (living wiki) yang terus bertumbuh dan saling terhubung secara otomatis**:
1. **AI yang Menulis & Merawat:** Anda fokus membaca, mengkurasi sumber, dan berpikir. AI yang meringkas, menghubungkan konsep, mendeteksi kontradiksi, dan merapikan catatan.
2. **Super Hemat Token:** Catatan internal wiki (`03 Wiki/`) ditulis dalam **Bahasa Inggris** (menghemat 50%–70% token BPE pada LLM), sedangkan interaksi komunikasi chat tetap fleksibel menggunakan **Bahasa Indonesia**.
3. **Universal Skills Hub:** Menyimpan backup offline penuh dari kumpulan kemampuan agen AI (*Agent Skills* dari Kepano, CEO Obsidian) agar Anda tidak pernah kehilangan modul saat repo GitHub pihak ketiga dihapus.
4. **Multi-Agent Session Handover:** Anda bisa berganti AI (Antigravity, Claude Code, Cursor, Codex, OpenCode) kapan saja tanpa kehilangan konteks diskusi sebelumnya.

---

## 🏛️ Struktur Direktori Vault

```text
Golden Second Brain 3.0/
├── 00 Meta/                      # Pusat kontrol sistem, aset, dan backup
│   ├── Assets/                   # Logo, visual diagrams, dan banner
│   ├── Chats/                    # 🤝 Arsip sesi diskusi & handover lintas agen AI
│   ├── Skills/                   # 🛡️ Universal Agent Skills Hub (offline mirror)
│   │   ├── Registry.md           # Katalog master skill & jadwal audit berkala
│   │   └── Stored/               # Mirror offline lengkap (termasuk kepano/obsidian-skills)
│   ├── Templates/                # Templat standar (Concept, Entity, Summary, Synthesis)
│   │   └── Web Clipper/          # Panduan & konfigurasi resmi Obsidian Web Clipper
│   ├── Dashboard.md              # Portal utama & navigasi cepat vault
│   ├── Index.md                  # Katalog konten (dibaca AI saat pencarian cepat)
│   └── Log.md                    # Catatan kronologis semua operasi AI di vault
│
├── 01 Inbox/                     # Tempat penampungan file mentah dari luar (PDF, artikel)
│   └── Clippings/                # Target otomatis Obsidian Web Clipper (root tetap bersih)
├── 02 Fleeting/                  # Ide kilat & catatan mentah langsung dari pemikiran Anda
│
├── 03 Wiki/                      # Pengetahuan Inti yang Disintesis & Dirawat oleh AI
│   ├── Concepts/                 # Mental models, pola pikir, teori, prinsip dasar
│   ├── Entities/                 # Tokoh, software, perusahaan, proyek, User Profile
│   ├── Summaries/                # Ekstraksi struktural dari bahan di Inbox
│   └── Synthesis/                # Perbandingan mendalam, analisis silang, esai
│
├── 04 Canvas/                    # Peta visual interaktif (.canvas JSON spec)
├── 05 Archive/YYYY-MM/           # Arsip sumber mentah yang telah selesai diproses
└── _attachments/                 # Folder terpusat untuk semua gambar & media
```

---

## 🚀 Panduan Memulai Cepat

### 1. Buka Vault di Obsidian
1. Download dan buka aplikasi [Obsidian](https://obsidian.md).
2. Pilih **Open folder as vault** (Buka folder sebagai vault).
3. Arahkan ke folder `Golden Second Brain 3.0`.
4. Buka file `00 Meta/Dashboard.md` sebagai beranda utama Anda!

### 2. Onboarding Otomatis dengan AI Agent
Saat pertama kali Anda menghubungkan AI Agent favorit Anda (Claude Code, Gemini/Antigravity, Cursor, dll.):
1. Agen akan mendeteksi status `pending_onboarding` pada file `03 Wiki/Entities/User Profile.md`.
2. Agen akan menyapa dan memandu Anda dalam wawancara singkat 3-4 pertanyaan (nama, fokus keahlian, proyek aktif, dan preferensi komunikasi).
3. Profil Anda langsung terpasang sehingga seluruh jawaban AI ke depan akan selalu relevan dengan konteks hidup dan proyek Anda!

### 3. Perintah Utama AI
- `/ingest` : AI memproses semua dokumen baru di `01 Inbox/`, membuat ringkasan terstruktur di `03 Wiki/Summaries/`, memperbarui konsep terkait di `03 Wiki/Concepts/`, memperbarui `Index.md`, dan memindahkan file asli ke `05 Archive/`.
- `/query <topik>` : AI membaca `Index.md` untuk menemukan catatan yang tepat, lalu memberikan jawaban mendalam yang saling terhubung dengan wikilinks `[[...]]`.
- `/save-session` : AI merangkum percakapan penting dan keputusan arsitektur ke dalam `00 Meta/Chats/` agar agen AI lain bisa melanjutkan pekerjaan tanpa lupa konteks.
- `/lint` : AI melakukan audit kesehatan vault (menemukan broken links, catatan tanpa tautan, dan mendeteksi kontradiksi informasi).

---

<br />
<hr />
<br />

<div id="-english-documentation"></div>

# 🇬🇧 English Documentation

## 🌟 Overview & Paradigm

Most AI knowledge workflows rely on traditional chunk-based **RAG (Retrieval-Augmented Generation)**: documents are split into arbitrary chunks, searched at runtime, and answered on the fly. Knowledge is never truly synthesized, compounded, or connected.

**Golden Second Brain 3.0** implements the **Andrej Karpathy LLM Wiki Architecture**:
> *"Obsidian is the IDE; the LLM is the programmer; the wiki is the codebase."*

Instead of rediscovering facts on every query, the AI agent **incrementally builds, compiles, and maintains a persistent personal wiki**:
- **Compounding Knowledge:** Summaries, entity dossiers, and mental models stay perpetually interlinked and updated.
- **Max Token Efficiency:** Internal wiki notes (`03 Wiki/**`) are maintained in **100% English**, achieving 50%–70% Byte-Pair Encoding (BPE) token density savings and maximizing LLM context window reasoning.
- **Universal Skills Hub:** Vendored offline mirrors of official Agent Skills (featuring Kepano's OFM standards) insulate your workflows against upstream repository removals or breaking changes.
- **Multi-Agent Portability:** Context is decoupled from proprietary chat interfaces and stored inside `00 Meta/Chats/` for seamless handover between Claude, Antigravity, Cursor, and Codex.

---

## 🏛️ Directory Architecture

- **`00 Meta/`**: Orchestration nerve center containing Master Index, Operations Log, Visual Dashboard, and the Universal Skills Hub.
- **`00 Meta/Chats/`**: Curated decision records and high-signal session handover transcripts.
- **`00 Meta/Skills/`**: Fully mirrored offline repositories with an upstream audit protocol.
- **`01 Inbox/`**: Staging area for raw sources (PDFs, papers, web clips via Obsidian Web Clipper).
- **`02 Fleeting/`**: Ephemeral capture lane for the human thinker's spontaneous notes.
- **`03 Wiki/`**: Persistent, AI-maintained knowledge graph divided into `Concepts/`, `Entities/`, `Summaries/`, and `Synthesis/`.
- **`04 Canvas/`**: Native JSON Canvas (`.canvas`) specifications for interactive visual architecture and relationship mapping.
- **`05 Archive/`**: Immutable storage for raw sources post-ingestion (`YYYY-MM/`).
- **`_attachments/`**: Central repository for images, audio, and documents (configured in `.obsidian/app.json`).

---

## ⚡ Core Operational Workflows

### 1. Ingestion (`/ingest`)
Drop web clips, papers, or notes into `01 Inbox/`. The AI agent parses the document, creates an executive extraction in `03 Wiki/Summaries/`, updates associated principles in `03 Wiki/Concepts/`, updates `00 Meta/Index.md`, logs the operation in `00 Meta/Log.md`, and archives the raw source into `05 Archive/YYYY-MM/`.

### 2. Querying & Synthesis (`/query`)
Inquiries consult `00 Meta/Index.md` first, retrieving high-relevance nodes deterministically without brute-force context dumping. Novel syntheses and comparisons are filed back into `03 Wiki/Synthesis/`.

### 3. Session Handover (`/save-session`)
Preserves critical technical breakthroughs and decisions into `00 Meta/Chats/YYYY-MM-DD - <Topic>.md`, allowing any secondary agent to inspect and immediately resume ongoing efforts.

### 4. Skills Hub Audit
Run on a weekly-to-monthly basis. Inspects upstream repositories tracked in `00 Meta/Skills/Registry.md`. Prepares a diff report and requires user authorization before updating local mirrors.

---

## 🛠️ Standards Compliance
- **Obsidian Flavored Markdown (OFM)**: Adheres strictly to [Kepano's Obsidian Skills](https://github.com/kepano/obsidian-skills).
- **JSON Canvas Specification**: Native `.canvas` files compliant with [jsoncanvas.org](https://jsoncanvas.org).
- **Git Hygiene**: Centralized `.gitignore` protecting Obsidian internal cache files while maintaining clean directory trees via `.gitkeep`.

---

## 👤 Author
Crafted with passion by **[Daffa' Avicenna](https://github.com/daffaavicenna)**.  
Licensed under the [MIT License](LICENSE).
