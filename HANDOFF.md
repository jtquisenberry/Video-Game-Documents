# AGENT HANDOFF: Video Game Documents Preservation & Web Publishing

> **Project:** Video Game Documents (`Video-Game-Documents`)  
> **Repository Root:** `d:\Development\git\Video-Game-Documents`  
> **Source Staging Root:** `D:\W\VideoGames\GameFAQs`  
> **Deployed Web Host:** GitHub Pages (served from `/docs`)  
> **Production Base URL:** `https://jtquisenberry.github.io/Video-Game-Documents/`  
> **Canonical Raw GitHub Base URL:** `https://raw.githubusercontent.com/jtquisenberry/Video-Game-Documents/main/docs/`  
> **GitHub Blob Base URL:** `https://github.com/jtquisenberry/Video-Game-Documents/blob/main/docs/`  
> **Document Last Updated:** 2026-11-07

---

## 1. Executive Summary & Mission

This repository is curated as an authoritative, human-researched knowledge repository and digital preservation archive for video game strategy guides, technical walkthroughs, moves lists, menu translations, and cartographic references. It is specifically optimized for:
1. **Human Readers:** Delivered via a clean, dark-themed responsive catalog on GitHub Pages (`docs/index.html`) where Jekyll renders source Markdown into clean HTML articles.
2. **AI Search & RAG Grounding (e.g., Google Gemini):** Structured with high-density YAML frontmatter, strict semantic hierarchies, deep mathematical formulas, exhaustive status-effect data, and `llms.txt` discovery manifests.

Any agent resuming this work must maintain **100% stylistic, architectural, and metadata consistency** with the existing repository standards.

---

## 2. Mandatory Synchronization: "The Rule of Five"

Every single game, guide, walkthrough, or media archive added or modified **MUST** update all five integration points before the task is considered complete:

```
[1. Game Document]  docs/<Platform>/<Game>/<Filename>.md (with YAML frontmatter)
       │
       ├──► [2. README.md]           Master Catalog Table row + Architecture directory tree
       ├──► [3. llms.txt]            llms.txt (root: docs/ prefix) & docs/llms.txt (web: no prefix)
       ├──► [4. docs/index.html]     <article class="card"> UI Card + Schema.org JSON-LD hasPart node
       └──► [5. docs/sitemap.xml]    Canonical <url> block pointing to https://jtquisenberry.github.io/.../.html
```

### Detailed Breakdown of The Rule of Five:

1. **The Game Document (`docs/<Platform>/<Game>/<Slug>.md` or `README.md`):**
   - Must reside in a platform-first subfolder: `docs/<Platform>/<Game>/`.
   - Never leave loose documents directly under `docs/` or `docs/<Platform>/`.
   - Must begin with standardized YAML frontmatter (see Template below).
   - Never put version numbers into file extensions (e.g. use `game.md`, never `game_v1.0.md`).

2. **Master Catalog & Directory Tree (`README.md`):**
   - Add/update the entry in the Markdown table under `## Master Document Catalog`. Include Platform, Game Title, Document Title (relative link starting with `docs/`), Type, Key Topics & Search Keywords, Author & Version, and Direct Link.
   - Update the ASCII directory tree under `## Repository Architecture`.

3. **Discovery Manifests (`llms.txt` and `docs/llms.txt`):**
   - **Root `llms.txt`:** Uses repo filesystem paths prefixed with `docs/`:
     ```markdown
     - [Title](docs/<Platform>/<Game>/<File>.md): Concise summary sentence.
     ```
   - **Web `docs/llms.txt`:** Uses relative paths *without* `docs/` because `docs/` is the web root:
     ```markdown
     - [Title](<Platform>/<Game>/<File>.md): Concise summary sentence.
     ```

4. **Web Portal & Structured Data (`docs/index.html`):**
   - **Catalog UI Card:** Add `<article class="card">` inside `<section class="catalog-grid">` matching existing card typography, badges, and action buttons. Update total title counter in `<span class="catalog-section-count">`.
   - **Schema.org JSON-LD:** Add a `TechArticle` / `VideoGame` node inside the `"hasPart"` array. The `"url"` property must point to the canonical GitHub Pages `.html` URL.

5. **Search Engine Index (`docs/sitemap.xml`):**
   - Add `<url>` block with the full canonical `.html` URL, current `<lastmod>` (YYYY-MM-DD), `<changefreq>monthly</changefreq>`, and `<priority>0.8</priority>` (or `0.9` for major guides).

---

## 3. Strict URL Rules (The Jekyll vs. Raw Markdown Rule)

GitHub Pages serves `docs/` as the web root and processes Markdown files through Jekyll into rendered `.html` pages upon deployment.

| UI Button / Target | href Target Pattern | Example | Notes |
|---|---|---|---|
| **Card Title Link** | `<Platform>/<Game>/<File>.html` | `PS2/MOTU_Defender_of_Grayskull/MOTU_Defender_of_Grayskull_Cheats.html` | Relative; no `docs/` prefix; must use `.html` |
| **"Read Guide" / "Read Manual" Button** | `<Platform>/<Game>/<File>.html` | `Handheld_LCD/MOTU_Electronic_Game/MOTU_Electronic_Game_Walkthrough.html` | Relative; no `docs/` prefix; must use `.html` |
| **"View Markdown (.md)" Button** | `https://raw.githubusercontent.com/jtquisenberry/Video-Game-Documents/main/docs/<Platform>/<Game>/<File>.md` | `https://raw.githubusercontent.com/jtquisenberry/Video-Game-Documents/main/docs/PS2/...md` | Absolute raw GitHub URL; `docs/` IS required |
| **"GitHub" Source Button** | `https://github.com/jtquisenberry/Video-Game-Documents/blob/main/docs/<Platform>/<Game>/<File>.md` | `https://github.com/jtquisenberry/Video-Game-Documents/blob/main/docs/PS2/...md` | Absolute GitHub blob URL; `docs/` IS required |
| **JSON-LD `"url"` property** | `https://jtquisenberry.github.io/Video-Game-Documents/<Platform>/<Game>/<File>.html` | Full canonical URL; `.html` extension; no `docs/` prefix |
| **Sitemap `<loc>` property** | `https://jtquisenberry.github.io/Video-Game-Documents/<Platform>/<Game>/<File>.html` | Full canonical URL; `.html` extension; no `docs/` prefix |

> [!CAUTION]
> **NEVER link to `https://jtquisenberry.github.io/Video-Game-Documents/<path>.md`**  
> GitHub Pages / Jekyll only publishes the rendered `.html` output, not the raw `.md`. Any `.md` link to the github.io domain produces a **404 Not Found**. Always use the `.html` target for web pages and `raw.githubusercontent.com` for raw Markdown.

---

## 4. Media Accessibility Standard: "No Orphan Media"

Search models and screen readers cannot understand binary images without text. Whenever copying images (`.png`, `.jpg`, `.gif`) into a game folder:
- **Never leave loose, unreferenced media files.**
- Every image must be embedded into the companion Markdown document:
  ```markdown
  ![Detailed alt-text describing the screen, HUD elements, characters, and actions](filename.jpg)

  **Caption:** Full paragraph explanation breaking down every UI element, stat counter, character state, waypoint, or transcript depicted.
  ```
- Maps must include waypoint tables and speedrun routing instructions.
- Packaging / Box Art must include verbatim transcriptions of all printed text, blurbs, barcodes, and specs.

---

## 5. Frontmatter & Component Templates

### A. Markdown YAML Frontmatter Template
```yaml
---
title: "Document Title: Subtitle or Scope"
game: "Official English Game Title"
platform: "Canonical Platform Name" # e.g. PlayStation 2, Android, Game Boy Advance, SNES
alternate_titles:
  - "Japanese or Regional Title"
  - "Common Acronym"
developer: "Original Developer"
publisher: "Original Publisher"
release_year: 2005
document_type: "Strategy Guide" # Strategy Guide | Walkthrough | Translation | Moves List & Reference | Map & Route Guide | Media Archive
author: "Jacob Quisenberry"
version: "1.00"
date: "YYYY-MM-DD"
last_updated: "YYYY-MM-DD"
language: "en"
tags:
  - primary-tag
  - genre-tag
  - platform-tag
summary: "1-2 sentence semantic summary optimized for RAG chunking and LLM search discovery."
---
```

### B. `docs/index.html` Single Card Template
```html
				<!-- Platform: Game Title -->
				<article class="card">
					<div class="card-content">
						<div class="card-header">
							<span class="platform-badge">Platform Name</span>
							<span style="font-size: 0.85rem; color: var(--text-muted);">v1.00 (YYYY-MM-DD)</span>
						</div>
						<h2 class="card-title">
							<a href="Platform_Dir/Game_Dir/Document_Name.html">Document Title</a>
						</h2>
						<p class="card-subtitle">Genre • Focus / Scope Subtitle</p>
						<p class="card-desc">
							Concise 1-2 sentence description highlighting technical depth, formulas, or unique data.
						</p>
						<ul class="highlight-list">
							<li><strong>Key Feature 1:</strong> Specific gameplay mechanics or data documented.</li>
							<li><strong>Key Feature 2:</strong> Additional detail, tables, or screen references.</li>
						</ul>
						<div class="card-actions">
							<a href="Platform_Dir/Game_Dir/Document_Name.html" class="btn-primary">Read Guide</a>
							<a href="https://raw.githubusercontent.com/jtquisenberry/Video-Game-Documents/main/docs/Platform_Dir/Game_Dir/Document_Name.md"
								class="btn-secondary" target="_blank" rel="noopener">View Markdown (.md)</a>
							<a href="https://github.com/jtquisenberry/Video-Game-Documents/blob/main/docs/Platform_Dir/Game_Dir/Document_Name.md"
								class="btn-secondary" target="_blank" rel="noopener">GitHub</a>
						</div>
					</div>
				</article>
```

### C. `docs/index.html` Multi-Document Hub Card Template (for Games with Multiple Docs)
```html
				<!-- Multi-Document: Game Title -->
				<article class="card">
					<div class="card-content">
						<div class="card-header">
							<span class="platform-badge">Platform Name</span>
							<span class="card-meta">Year • Publisher • Version</span>
						</div>
						<h2 class="card-title">
							<a href="Platform_Dir/Game_Dir/Primary_Doc.html">Game Title</a>
						</h2>
						<p class="card-subtitle">Overview subtitle</p>
						<p class="card-desc">Overall game summary description.</p>
						<div class="doc-hub">
							<h3 class="doc-hub-title">Available Guides &amp; References</h3>
							<!-- Sub-Item 1 -->
							<div class="doc-item">
								<div class="doc-item-body">
									<div class="doc-item-header">
										<span class="doc-type-badge">Walkthrough</span>
										<a href="Platform_Dir/Game_Dir/Doc1.html" class="doc-item-title">Title 1</a>
									</div>
									<p class="doc-item-desc">Description of doc 1.</p>
								</div>
								<div class="doc-item-actions">
									<a href="Platform_Dir/Game_Dir/Doc1.html" class="btn-sm-primary">Read Guide</a>
									<a href="https://raw.githubusercontent.com/jtquisenberry/Video-Game-Documents/main/docs/Platform_Dir/Game_Dir/Doc1.md" class="btn-sm-secondary" target="_blank" rel="noopener">Markdown (.md)</a>
								</div>
							</div>
						</div>
					</div>
				</article>
```

---

## 6. Current Repository Status & Immediate Tasks

### State as of Git Commit `3f1af26` ("Multiple pages added"):
The following 10 Masters of the Universe titles have been converted, their media copied and captioned, and their entries recorded in `README.md`, `llms.txt`, and `docs/llms.txt`:
1. `docs/PS2/MOTU_Defender_of_Grayskull/MOTU_Defender_of_Grayskull_Cheats.md`
2. `docs/Web_Browser/MOTU_Courage_of_Adam/README.md`
3. `docs/Web_Browser/MOTU_Lair_of_the_Slime_Mutant/README.md`
4. `docs/Roblox/MOTU_Battle_for_Grayskull/README.md` (+ 10 screenshots)
5. `docs/Android/MOTU_Combat_Simulator/README.md` (+ 8 screenshots)
6. `docs/Android/MOTU_Guardians_of_Grayskull/README.md` (+ 2 screenshots)
7. `docs/Android/MOTU_He-Man_Heroes/README.md` (+ 2 screenshots)
8. `docs/Android/MOTU_Skeletor/README.md` (+ 4 screenshots)
9. `docs/Android/He-Man_Tappers_of_Grayskull/README.md`
10. `docs/Android/MOTU_VR/README.md`

### ⚠️ IMMEDIATE PENDING WORK:
Complete points 4 and 5 of The Rule of Five for the 10 titles above:
1. **Update `docs/index.html`:**
   - Add the 10 `<article class="card">` elements under `<section class="catalog-grid">` (or organize them into appropriate subsections).
   - Add the 10 `TechArticle` / `VideoGame` items inside the JSON-LD `"hasPart"` array.
   - Update the total titles count badge in `docs/index.html`.
2. **Update `docs/sitemap.xml`:**
   - Add the 10 `<url>` blocks using canonical `.html` URLs:
     - `https://jtquisenberry.github.io/Video-Game-Documents/PS2/MOTU_Defender_of_Grayskull/MOTU_Defender_of_Grayskull_Cheats.html`
     - `https://jtquisenberry.github.io/Video-Game-Documents/Web_Browser/MOTU_Courage_of_Adam/README.html`
     - `https://jtquisenberry.github.io/Video-Game-Documents/Web_Browser/MOTU_Lair_of_the_Slime_Mutant/README.html`
     - `https://jtquisenberry.github.io/Video-Game-Documents/Roblox/MOTU_Battle_for_Grayskull/README.html`
     - `https://jtquisenberry.github.io/Video-Game-Documents/Android/MOTU_Combat_Simulator/README.html`
     - `https://jtquisenberry.github.io/Video-Game-Documents/Android/MOTU_Guardians_of_Grayskull/README.html`
     - `https://jtquisenberry.github.io/Video-Game-Documents/Android/MOTU_He-Man_Heroes/README.html`
     - `https://jtquisenberry.github.io/Video-Game-Documents/Android/MOTU_Skeletor/README.html`
     - `https://jtquisenberry.github.io/Video-Game-Documents/Android/He-Man_Tappers_of_Grayskull/README.html`
     - `https://jtquisenberry.github.io/Video-Game-Documents/Android/MOTU_VR/README.html`

---

## 7. Inventory of Remaining Unconverted Sources (`D:\W\VideoGames\GameFAQs`)

Once the immediate sync above is completed, proceed to convert the remaining game folders from `D:\W\VideoGames\GameFAQs`:

| Source Folder | Platform / System | Game / Content Description | Target Folder |
|---|---|---|---|
| `intv_super_masters` | Intellivision | *Masters of the Universe* / *Intellivision Lives* / *Super Masters* screen and packaging archive (7 images) | `docs/Intellivision/MOTU_Super_Masters/` |
| `Barcode_Battler_II` | Dedicated Handheld / Epoch | Barcode Battler II documentation, barcode cards, interface mechanics | `docs/Handheld/Barcode_Battler_II/` |
| `Dragon_Edge_Pinball` | Pinball / Mobile / Arcade | Dragon's Edge Pinball rule sheet, table mechanics, scoring strategies | `docs/<Platform>/Dragon_Edge_Pinball/` |
| `Dungeons_and_Dragons_LCD` | Handheld LCD | Mattel / Tiger Dungeons & Dragons LCD handheld game manual and maze reference | `docs/Handheld_LCD/Dungeons_and_Dragons/` |
| `GBA_Tactics_Ogre_KOL` | Game Boy Advance | *Tactics Ogre: The Knight of Lodis* comprehensive guide / mechanics | `docs/GBA/Tactics_Ogre_KOL/` |
| `Might_and_Magic` | PC / Multi-platform | *Might and Magic* walkthrough / spell tables / maps | `docs/PC/Might_and_Magic/` |
| `PC_Toy_Soldiers_WC` | PC (Windows) | *Toy Soldiers: War Chest* unit stats, survival guide, hero tactics | `docs/PC_Windows/Toy_Soldiers_War_Chest/` |
| `SNES_Final_Fantasy_II` | Super Nintendo (SNES) | *Final Fantasy II* (FFIV) walkthrough, boss tactics, item tables | `docs/SNES/Final_Fantasy_II/` |
| `Tingle_Rupeeland_DS` | Nintendo DS | *Freshly-Picked Tingle's Rosy Rupeeland* walkthrough, negotiation formula, recipe translation | `docs/DS/Tingle_Rupeeland/` |
| `Zelda_Game_and_ Watch` / `Zelda_Game_Watch` | Nintendo Game & Watch | *The Legend of Zelda* dual-screen Game & Watch walkthrough, 8-chamber dungeon maps, scoring rules | `docs/Game_and_Watch/Zelda/` |

---

## 8. Validation Commands (PowerShell)

Before committing any batch of changes, run these verification steps:

```powershell
# 1. Verify all markdown file paths in README.md exist locally
Get-Content README.md | Select-String -Pattern 'docs/[^)\s]+' -AllMatches | ForEach-Object { $_.Matches } | ForEach-Object { $_.Value } | Sort-Object -Unique | ForEach-Object {
    $exists = Test-Path $_
    [PSCustomObject]@{ Path = $_; Exists = $exists }
} | Where-Object { -not $_.Exists }

# 2. Verify all image references in docs/*.md exist on disk
Get-ChildItem -Recurse -Filter *.md docs | ForEach-Object {
    $doc = $_
    $content = Get-Content $doc.FullName
    $matches = [regex]::Matches($content, '!\[.*?\]\((.*?)\)')
    foreach ($m in $matches) {
        $imgPath = Join-Path $doc.DirectoryName $m.Groups[1].Value
        if (-not (Test-Path $imgPath)) {
            Write-Warning "Broken image in $($doc.FullName): $($m.Groups[1].Value)"
        }
    }
}

# 3. Ensure no illegal github.io/*.md links exist in index.html
$badLinks = Select-String -Path 'docs/index.html' -Pattern 'https://jtquisenberry\.github\.io/Video-Game-Documents/.*\.md'
if ($badLinks) {
    Write-Error "Found illegal .md link on GitHub Pages domain: $badLinks"
} else {
    Write-Host "URL Validation Passed: Zero .md links on GitHub Pages domain."
}
```
