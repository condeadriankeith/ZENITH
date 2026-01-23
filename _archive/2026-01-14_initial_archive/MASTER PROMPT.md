# MASTER PROMPT — Markdown-only Worldbuilding Package Generator for *The Shattered Meridian*

## Input
- **Canonical source file:** `/mnt/data/shattered_meridian_compendium.md`

## Objective
Using the canonical compendium as the sole source of truth, generate a complete, **markdown-only** worldbuilding package for *The Shattered Meridian*.  
Produce only `.md` files (no PNG, PDF, DOCX, XLSX, CSV, or other binary outputs). All content must be editorially complete, internally consistent, and ready for downstream conversion by humans or tools.

---

## Non-Negotiable Rules

### 1. Originality
- Do **not** reference or reuse names, lore, mechanics, or terminology from any external IP.  
- Use **only** the provided compendium as source material. Expand and formalize; do not import outside lore.

### 2. Canon Enforcement
The following items are canonical and must appear **verbatim** where indicated and consistently across documents:
- **The Great Filter** (primary antagonist) and Meridian Lock mechanics  
- **The Fracture (907 R)** as the canonical origin of the Vanishing (include canonical paragraph)  
- **Ascension — the three immutable laws** (include exact plaque text)  
- **Name-Bleed** sensory Ruination paragraph (use exact text at least once)  
- The Traveler: **nameless**, **left-handed**, pack of knowledge, three emotional anchors (mother’s name traded, failed rescue, lost Archivist)  
- Region names: **Cyris, Thalen, Virek, Kallum, Eirn, Sahru, Alkyr, Mirel, Nyth, Valen, The Hollow**

### 3. Narrative Discipline
- Replace at least **50%** of any long explanatory blocks in the compendium with *in-world artifacts* (ledger excerpts, trial transcripts, marginalia, tavern rhymes, codex epigraphs) when creating chapter/codex-style documents.  
- Avoid encyclopedic dumps in main documents; keep long-form explanation in `lore/` and `systems/` reference files.

### 4. Markdown-only Deliverables
- Produce **only** `.md` files. Where maps, images, spreadsheets or other binaries were originally requested, create **textual equivalents**:
  - `maps/` becomes `maps.md` with ASCII or descriptive map legend and coordinate key.
  - `systems_arcana.md` replaces spreadsheets and must include the entropy model and example calculations as inline preformatted tables/code blocks.
  - `bestiary.md` replaces CSV; include machine-parsable markdown tables.
  - `manifest.md` replaces JSON manifest (human- and tool-friendly table).
  - `validation_report.md`, `changelog.md`, `README.md` are all markdown.
- Do not create or reference any binary files in outputs.

---

## Required Folder Structure (markdown-only)

/shattered_meridian/
├─ manifest.md
├─ README.md
├─ compendium/
│ └─ shattered_meridian_compendium.md # canonical source (input)
├─ atlas/
│ ├─ atlas_master.md
│ ├─ maps.md # textual map descriptions + legend
│ └─ traveler_route.md
├─ codex/
│ ├─ codex_of_realms.md
│ └─ codex_epigraphs.md
├─ systems/
│ ├─ systems_arcana.md # taxonomy, entropy model, example calcs
│ └─ ascension_laws_plaque.md
├─ lore/
│ ├─ lore_compendium.md
│ └─ lore_entries/ # 30+ md files: 01_title.md ... 30_title.md
├─ bestiary/
│ ├─ bestiary.md # table + long entries
│ └─ spirits.md
├─ characters/
│ ├─ characters_index.md
│ └─ archetypes/ # many md files, one per archetype
├─ traveler_archive/
│ ├─ traveler_archive.md
│ └─ traveler_journal_fragments.md
├─ art_and_aesthetics/
│ ├─ color_palettes.md
│ ├─ moodboard_prompts.md # text prompts for artists
│ └─ sound_motifs.md
├─ scenes/
│ ├─ trial_scene_cyris.md
│ ├─ virek_foundry_rupture.md
│ └─ prologue_personalized.md
└─ editorial/
├─ style_guide.md
├─ canon_checklist.md
└─ changelog.md


---

## Document Specifications (content & format rules)

### Atlas (`atlas_master.md`, `maps.md`, `traveler_route.md`)
- `atlas_master.md`: regional pages (topography, climate, signature magic, one vivid daily-life detail). Use headings and subheadings.
- `maps.md`: human-readable map legend and coordinate grid descriptions. Include an ASCII schematic or numbered coordinate markers for major nodes and the Hollow.
- `traveler_route.md`: step-by-step textual travel route with chapter ties and node references.

### Codex of Realms (`codex_of_realms.md`, `codex_epigraphs.md`)
- `codex_of_realms.md`: canonical cosmology, Architects, The Great Filter, The Fracture (include canonical paragraph), Ascension Laws (verbatim plaque), ritual lexicon, governance rules.
- `codex_epigraphs.md`: 40 short epigraphs (one-liners, tavern rhymes, ledger scraps) formatted as bullet list, usable as chapter openers.

### Systems & Mechanics (`systems_arcana.md`, `ascension_laws_plaque.md`)
- `systems_arcana.md` must include:
  - **Magic taxonomy** as markdown table.
  - **Leyline and node registry** as a table (NodeID, Region, Bandwidth, Entropy estimate, Last noted activation).
  - **Entropy model**: show narrative formula and at least two worked examples as code blocks with numeric steps.
  - **Ascension checklist**: step-by-step process and failure modes.
- `ascension_laws_plaque.md`: exact three-law plaque text, suitable for quoting in scenes.

### Lore Compendium (`lore_compendium.md` + `lore_entries/`)
- `lore_compendium.md` contains an index and 15–20 long entries (700–1,200 words each) integrated into the document.
- `lore_entries/` contains 30+ separate `.md` files (numbered) for modular use.

### Bestiary (`bestiary.md`, `spirits.md`)
- `bestiary.md`: machine-parsable markdown table (id, common_name, category, region, description, danger_level, narrative_hook).
- After the table, include long-form writeups for 12 flagship creatures.
- `spirits.md`: ecology, interaction mechanics, narrative hooks.

### Characters (`characters_index.md`, `archetypes/*.md`)
- `characters_index.md`: overview of archetypes, usage notes, and crosslinks.
- `archetypes/` folder: one `.md` per archetype with appearance, speech samples, signature magic, moral contradictions, arc beats.

### Traveler Archive (`traveler_archive.md`, `traveler_journal_fragments.md`)
- Polished journal fragments and map notes. Include the prologue personalization paragraph within `traveler_archive.md`.

### Art & Aesthetics (`color_palettes.md`, `moodboard_prompts.md`, `sound_motifs.md`)
- `color_palettes.md`: hex codes and short notes for each region.
- `moodboard_prompts.md`: carefully worded prompts for artists (text only).
- `sound_motifs.md`: descriptive motifs for composers.

### Scenes (`trial_scene_cyris.md`, `virek_foundry_rupture.md`, `prologue_personalized.md`)
- Fully polished narrative scenes (wordcounts as previously specified). No placeholders.

### Editorial (`style_guide.md`, `canon_checklist.md`, `changelog.md`)
- `style_guide.md`: voice, motif reuse, banned references, show-don’t-tell rule.
- `canon_checklist.md`: explicit checklist that programmatically ensures canonical items appear.
- `changelog.md`: record every editorial change and reasoning.

---

## Validation & Manifest (markdown)

- **manifest.md**: table listing every generated file, word counts, and a SHA-256 checksum placeholder column (compute if environment allows; otherwise leave `TBD` but list files).
- **validation_report.md**: run checks and output as markdown:
  - Verify canonical texts (Fracture paragraph, Ascension plaque, Name-Bleed) appear verbatim in required places.
  - Confirm no binary files were produced.
  - Flag any newly introduced proper names or contradictions.

---

## Programmatic & Editorial Checks (run and fix iteratively)

1. All place-names must match canonical list. Flag any variations.  
2. Ascension Laws text must be identical in `codex_of_realms.md`, `systems_arcana.md`, and `ascension_laws_plaque.md`.  
3. The Fracture canonical paragraph must appear in `codex_of_realms.md` and in one `lore_entries/` file.  
4. Name-Bleed paragraph must appear in `bestiary.md`, at least one `lore_entries/` file, and in one scene.  
5. At least 50% of long explanatory blocks in source compendium must be converted to in-world artifacts in the generated files (report exact percent).  
6. Scenes must be polished (no "[INSERT]" or TODO markers).

---

## Execution Instructions

1. **Parse** `/mnt/data/shattered_meridian_compendium.md` strictly as the canon source.  
2. **Create** the folder structure above under `/workspace/shattered_meridian/` (or current workspace) and populate with `.md` files only.  
3. **Expand** where required to meet wordcount and content specifications; log all expansions in `changelog.md`.  
4. **Run validation** checks and produce `validation_report.md`. Fix critical issues until no critical flags remain.  
5. **Produce `manifest.md`** summarizing files and basic metadata.  
6. **Produce `README.md`** with quickstart guidelines for writers/designers and instructions on how to convert markdown to other formats if desired.

---

## Completion Criteria

- All files in the markdown-only folder structure exist and are non-empty `.md`.  
- `manifest.md` and `validation_report.md` are present.  
- No critical validation errors remain (canon mismatches, missing required canonical texts, or binary artifacts created).  
- Scenes and lore entries meet specified wordcounts and are editorially polished (no placeholder text).  
- A final short summary (3–6 lines) is written in `README.md` describing what was generated and where to find the canonical pieces.

---

## Final Response Format (what the system should return)

Upon successful completion, return a single markdown-formatted message containing:

1. Path to the markdown package root (e.g., `/workspace/shattered_meridian/`)  
2. A brief `manifest.md` summary (top 12 files and their wordcounts) inline.  
3. A short excerpt from `validation_report.md` showing zero critical failures.  
4. If blocked, an explicit error list with remediation steps.

---

**End of Master Prompt**
