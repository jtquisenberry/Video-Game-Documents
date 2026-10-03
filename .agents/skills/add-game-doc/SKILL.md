---
name: add-game-doc
description: >-
  Use this skill whenever adding a new game, guide, walkthrough, moves list, translation, or media archive
  to the Video Game Documents repository. Guides the agent through Markdown formatting, YAML frontmatter creation,
  and executing the mandatory 5-point synchronization across README.md, llms.txt, index.html, and sitemap.xml.
---

# Add Game Document Workflow

Follow this procedure whenever adding or converting a new game document in this repository.

---

## Step 1: Establish Folder & File Structure

1. Determine the canonical platform slug (e.g., `Amazon_Luna`, `AmstradCPC`, `AtariST`, `DSi`, `GBA`, `NES`, `SNES`, `Genesis`, `PlayStation`, `PC_Windows`).
2. Create the game folder: `docs/<Platform>/<Game_Slug>/`.
3. Choose a clean filename:
   - `<Game_Slug>_<Document_Type>.md` (e.g., `MOTU_Power_of_Grayskull_Moves_List.md`) or `README.md`.
   - Never put version numbers in the file extension (e.g., no `.md_v1.0.md`).

---

## Step 2: Format the Markdown Content

1. **YAML Frontmatter (Required):**
   ```yaml
   ---
   title: "Complete Document Title"
   game: "Official English Title"
   platform: "Platform Name"
   alternate_titles:
     - "Alternate/Japanese/Regional Title"
   developer: "Developer Name"
   publisher: "Publisher Name"
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
   summary: "1-2 sentence semantic summary for search and RAG chunking."
   ---
   ```
2. **Body Formatting:**
   - Use strict heading hierarchy (`#`, `##`, `###`).
   - Convert controls, items, or stats into Markdown tables.
   - For images, include descriptive alt-text and complete textual transcriptions/waypoint tables.

---

## Step 3: Execute the Mandatory 5-Point Synchronization

Whenever a document is added or modified, update all five points:

1. **Target Document:** Verify file exists in `docs/<Platform>/<Game>/`.
2. **`README.md`:**
   - Add a row to the **Master Document Catalog** table with clickable relative links.
   - Update the **Repository Architecture** directory tree.
3. **`llms.txt` & `docs/llms.txt`:**
   - Add the document to **Primary Documents & Guides** in both `llms.txt` and `docs/llms.txt`.
4. **`docs/index.html`:**
   - Add a `<article class="card">` under `<section class="catalog-grid">`.
   - Add a `TechArticle` / `VideoGame` node in the Schema.org JSON-LD graph.
5. **`docs/sitemap.xml`:**
   - Add `<url>` block with `https://jtquisenberry.github.io/Video-Game-Documents/<path-to-file>`.

---

## Step 4: Cleanup & Validation

1. Remove any loose temporary or raw source files (e.g., `.txt`) that were converted.
2. Run `Test-Path` in PowerShell on all referenced links in `README.md`, `index.html`, and `sitemap.xml` to ensure zero broken links.
