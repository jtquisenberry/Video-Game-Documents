# Video Game Documents – Workspace Rules

You are working in the **Video Game Documents** repository. This repository is curated as an authoritative, human-researched ground truth of video game strategy guides, technical walkthroughs, translations, and cartographic references. It is specifically optimized for both human readers and AI search grounding (such as Google Gemini).

Every agent working in this repository MUST strictly follow the architecture, conventions, and synchronization rules defined below.

---

## 1. Directory Structure Standards

* **Root Directory:** Reserved exclusively for repository-level administrative and discovery files:
  - `README.md` (Master catalog, documentation standards, architecture)
  - `llms.txt` (AI discovery manifest)
  - `LICENSE` (GPL v3)
  - `.gitignore`
  - `GEMINI.md` (Workspace rules)
* **Substantive Content (`docs/`):** All documentation lives under `docs/` using a **Platform-First** two-tier hierarchy:
  `docs/<Platform>/<Game>/`
  - `<Platform>`: Canonical platform name or slug (e.g., `Amazon_Luna`, `AmstradCPC`, `AtariST`, `DSi`, `GBA`, `NES`, `SNES`, `Genesis`, `PlayStation`, `PC_Windows`).
  - `<Game>`: Descriptive folder name matching the game's title or common abbreviation with underscores (e.g., `MOTU_Legends_Unite`, `MOTU_Power_of_Grayskull`, `Dekisugi_Tincle`).
* **Game Folders:** Must contain:
  - The primary document: either `<Game_Slug>_<Document_Type>.md` or `README.md`.
  - Any associated media (maps, box art, screenshots) stored directly alongside the markdown file or in an `assets/` subfolder.
* **No Loose Files:** Never leave raw files (`.txt`, `.doc`, loose images) in `docs/` or directly under `docs/<Platform>/`. Everything must reside inside a dedicated `<Game>` subfolder. Scratch or source files should be converted to Markdown and removed.

---

## 2. Mandatory Synchronization Checklist ("The Rule of Five")

Whenever any document is added, renamed, or substantially revised, you **MUST** update all five integration points:

1. **The Game Document:**
   - Create or update `docs/<Platform>/<Game>/<Filename>.md`.
   - Must include complete, standardized YAML frontmatter (see schema below).
2. **`README.md`:**
   - Add/update the row in the **Master Document Catalog** table (Platform, Game, Document Title, Type, Keywords, Author & Version, Direct Relative Link).
   - Update the **Repository Architecture** directory tree.
3. **`llms.txt` AND `docs/llms.txt`:**
   - Add/update the entry under **Primary Documents & Guides** in both `llms.txt` (root) and `docs/llms.txt` (web root for GitHub Pages).
4. **`docs/index.html`:**
   - Add/update the `<article class="card">` inside `<section class="catalog-grid">` with badges, descriptions, and direct links.
   - Add/update the corresponding `TechArticle` / `VideoGame` node in the embedded **Schema.org JSON-LD** graph (`hasPart` array).
5. **`docs/sitemap.xml`:**
   - Add or update the `<url>` entry with the canonical URL (`https://jtquisenberry.github.io/Video-Game-Documents/...`) and `<lastmod>` date.

---

## 3. Document Frontmatter Specification

Every `.md` document inside `docs/` must begin with this standardized YAML frontmatter block:

```yaml
---
title: "Document Title"
game: "Canonical Game Title"
platform: "Canonical Platform Name"
alternate_titles:
  - "Regional or Japanese Title"
  - "Common Acronym"
developer: "Developing Studio"
publisher: "Publishing Entity"
release_year: 2000
document_type: "Strategy Guide" # Strategy Guide | Walkthrough | Translation | Moves List & Reference | Map & Route Guide | Media Archive
author: "Author Name"
version: "1.00"
date: "YYYY-MM-DD"
last_updated: "YYYY-MM-DD"
language: "en"
tags:
  - tag1
  - tag2
summary: "1-2 sentence semantic summary optimized for RAG chunking and LLM search discovery."
---
```

---

## 4. Media Accessibility Standard ("No Orphan Media")

* **No standalone binary files:** Pure image files (box art, screenshots, maps) cannot be understood by text search models in isolation.
* **Maps:** Must be accompanied by a Markdown document with an exhaustive numbered waypoint legend, sector descriptions, key items/chords list, and step-by-step speedrun or navigation instructions.
* **Box Art / Packaging:** Must include complete transcriptions of all printed text, slogans, compatibility headers, publisher imprints, and descriptive visual breakdowns.
* **Screenshots:** Must include captions describing the displayed UI, HUD, gameplay state, and depicted mechanics.

---

## 5. File Naming Rules

* Use clear, descriptive names: `<Game_Slug>_<Document_Type>.md` (e.g., `Dekisugi_Tincle_walkthrough.md`, `MOTU_Power_of_Grayskull_Moves_List.md`) or `README.md`.
* **Never include version numbers in file extensions** (e.g., do **not** create `.md_v1.0.md`). Store version numbers exclusively in the YAML frontmatter (`version: "1.0"`).
