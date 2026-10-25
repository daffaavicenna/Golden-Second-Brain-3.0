# 🌐 Recommended Configuration for Obsidian Web Clipper

To ensure all web clippings seamlessly integrate with **Golden Second Brain 3.0** without creating clutter in your root vault:

## 1. Extension Download
Install the official browser extension from: [https://obsidian.md/clipper](https://obsidian.md/clipper)

---

## 2. Vault Settings (Inside Web Clipper Settings)
Configure the extension settings as follows:

| Setting Field | Recommended Value | Explanation |
| :--- | :--- | :--- |
| **Vault Name** | `Golden Second Brain 3.0` | Exact name of your Obsidian vault |
| **Default Location / Note Folder** | `01 Inbox/Clippings` | Keeps root directory clean and stages clips for AI ingest |
| **Save Attachments Locally** | `Enabled (Checked)` | Downloads images/media locally |
| **Attachment Folder Path** | `_attachments` | Keeps all media organized in the central vault attachments folder |

---

## 3. Recommended Clipping Template (Markdown Frontmatter)

Copy and paste this into your default template inside the Web Clipper extension:

```markdown
---
type: raw-source
source_type: web-clip
title: "{{title}}"
url: "{{url}}"
author: "{{author}}"
published: {{published}}
clipped_date: {{date}}
tags:
  - source/web
  - status/unprocessed
---

# {{title}}

> [!info] Source Metadata
> - **URL:** {{url}}
> - **Author:** {{author}}
> - **Clipped Date:** {{date}}

---

{{content}}
```

---

## 4. Processing Flow by AI Agents
Once a page is clipped:
1. It lands in `01 Inbox/Clippings/<Article Title>.md`.
2. When you request `/ingest`, the AI agent parses the clipping, generates a structured summary in `03 Wiki/Summaries/`, cross-links concepts in `03 Wiki/Concepts/`, and moves the original clipping to `05 Archive/YYYY-MM/`.
