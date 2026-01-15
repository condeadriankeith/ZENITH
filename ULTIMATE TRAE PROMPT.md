# TRAE TASK PROMPT — Add 25 New Character Archetype Files & Integrate into Project

**Purpose:** Create full, production-ready markdown character files for the 25 original archetypes we designed (10 initial sketches + 15 new sketches), integrate them into the project index and manifest, produce a relationships map, and add scene/beat hooks that link each character into the novel’s three-act plan. All outputs must be **markdown only** and saved under the workspace root below.

**Important rules (non-negotiable):**
- **Do not** change any existing scene files in `/workspace/shattered_meridian/scenes/` or insert character names into scenes. Create character files only under `characters/archetypes/`.
- Preserve the **Maer name policy**: the canonical internal name `Maer` must only appear in metadata/archive files (characters/traveler.md and traveler_archive/*). If `Maer` appears in any other file Trae creates, move it to an archival fragment file and flag in `editorial/changes_proposed.md`.
- **No LoL/Runeterra copyrighted terms.** Run a forbidden-terms scan (see Validation section). If any forbidden-term appears, do not auto-replace in narrative text—log the occurrence and suggested replacement into `editorial/changes_proposed.md` and mark `REQUIRES_HUMAN_REVIEW`.
- Log every change in `editorial/changes_proposed.md`. Any autofix must be labeled `AUTOFIX` with original text and rationale.

---

## WORKSPACE ROOT
All files must be created/updated under:

/workspace/shattered_meridian/


---

## PRIMARY DELIVERABLES (create/update these files)

1. **Character archetype files** — one file per character under:

characters/archetypes/<slug>.md

Create 25 files exactly (use the given slugs below). Each file must include the sections and content specified in the **Character File Spec** below.

2. **Characters index**:

characters/characters_index.md

- A sortable table of all characters (slug, epithet, region, first-appearance chapter, link to archetype file).

3. **Character relationships map**:

characters/relationships.md

- A markdown table mapping relationships (ally/antagonist/neutral/mentor/romantic/owed-debt), brief description (10–20 words), and strength (1–5).

4. **Character beats summary**:


narrative_flow/character_arcs_characters_added.md

- For each character, 3 bullet beats showing how they intersect with Maer in Acts I, II, III (one beat each).

5. **Manifest update**:

narrative_flow/manifest.md

- Add entries for all new files with approximate wordcounts.

6. **Validation report** (append to/update):

narrative_flow/validation_report.md

- Add results of character creation validation (forbidden-term scan, Maer-usage check, file present check).

7. **Editorial log**:

editorial/changes_proposed.md

- Append entries for this task: files created, any autofixes, and any `REQUIRES_HUMAN_REVIEW` items.

---

## CHARACTER LIST (25 files — create these slugs)

Create the following files under `characters/archetypes/`:

**Initial 10 (already sketched earlier):**
1. `sera_of_the_tide.md`  
2. `oren_valis.md`  
3. `coren_astell.md`  
4. `lysa_korr.md`  
5. `toran_ironsund.md`  
6. `neth_chainwarden.md`  
7. `kael_stoneborn.md`  
8. `juno_tick_meri.md`  
9. `rian_mern.md`  
10. `thalens_bellman.md`

**Additional 15 (new sketches):**
11. `edda_wren.md`  
12. `harkan_blythe.md`  
13. `lyra_hal.md`  
14. `sarn_of_the_ash.md`  
15. `isala_apothecary.md`  
16. `varek_ledgerunner.md`  
17. `brune_the_quiet.md`  
18. `sorra_veil.md`  
19. `hella_iron_thumb.md`  
20. `fenn_smallwatch.md`  
21. `marek_toll.md`  
22. `yori_runehound.md`  
23. `alin_ro.md`  
24. `mira_glass.md`  
25. `eldra_voss.md`

---

## CHARACTER FILE SPEC (required structure & content)

Each archetype file must be a Markdown document and include the following sections in this exact order:

1. **Front-matter short header (3 lines)**  

<Display Name> — <Epithet>

Slug: <slug.md>
Region: <RegionName>


2. **One-paragraph elevator pitch (25–40 words)** — cinematic, hook-first.

3. **Appearance & Visual Cue (4–7 lines)** — very concrete, sensory (what the camera sees).

4. **Narrative Role (2–4 lines)** — role in the story (mentor, antagonist, ally, etc).

5. **Signature Motif (2 lines)** — a repeated sensory/cinematic device to use when the character appears (sound, scent, gesture).

6. **Moral Contradiction (2–3 lines)** — a brief internal or social conflict that makes them interesting.

7. **How they intersect with Maer (3 bullets)** — one bullet per act (I/II/III) showing specific, concrete narrative interaction. Each bullet must include a suggested chapter placement (e.g., "Act II — Ch. 10 (Virek Foundry)").

8. **First-appearance scene hook (1–2 paragraphs, 80–160 words)** — a ready-to-drop cinematic scene showing them in action (this should be high-quality prose, usable as-is in a chapter file later).

9. **Sample dialogue snippet (3–6 lines)** — 2-3 short lines of dialogue that capture voice and tone.

10. **Arc note (3–5 lines)** — short note on their trajectory across the novel and how they change.

11. **Tags / metadata (one line)** — comma-separated tags: `ally,mentor,forger,left-hand,spirit-porous` etc.

12. **Wordcount target:** each archetype file should be **~600–900 words** total.

**Formatting rules:**  
- Use blockquotes for any in-world artifacts or ledger text inside the file.  
- Do **not** include LoL/Runeterra names or copyrighted terms.  
- Do **not** place `Maer` inside the first-appearance scene if it would reveal the protagonist’s canonical name in a narrative file; if you need to reference Maer, use the phrase **"the Traveler"** inside character files for scene hooks. If you include a journal fragment that uses `Maer`, put it under a blockquote labeled `ARCHIVAL: signed — Maer` and ensure the file log notes that `Maer` is archival-only.

---

## INTEGRATION SPEC (how to link into the novel)

- **characters/characters_index.md**  
- Add each character as a row with: `Display Name | Epithet | Slug | Region | First Appearance (Chapter) | Role | Tags` and a one-sentence teaser.

- **characters/relationships.md**  
- For each new character, add 3–6 relationship entries that show ties to: Maer (the Traveler), at least one other named archetype, and one institution (Codex, White Hand, Archivum, Virek Forgebrotherhood, etc.). Use the interactions we previously sketched as default mapping.

- **narrative_flow/character_arcs_characters_added.md**  
- For each new character add exactly 3 short beats (Act I, Act II, Act III) stating their function and one concrete line of action they take that affects Maer.

- **manifest.md**  
- Add all new files with approximate wordcounts (Trae must compute).

---

## VALIDATION CHECKS (must run and record results)

Run these checks and append their outputs to `narrative_flow/validation_report.md` (show PASS/FAIL + evidence line numbers):

1. **File presence check** — verify all 25 files created and non-empty.

2. **Forbidden-term scan** — run a repo-wide grep for the forbidden list:

runeterra ryze ionia bard thresh taliyah ekko ornn kindred runic

- If any found: list file, line, and context. For narrative content files (character scene hooks) do **not** auto-edit; log `REQUIRES_HUMAN_REVIEW`. For non-narrative or staging files, Trae may remove and replace with `inspiration-note` and log as `AUTOFIX`.

3. **Maer name-usage check** — ensure `Maer` appears only where allowed (characters/traveler.md and traveler_archive files). If `Maer` appears in character files outside an archival blockquote, replace with "the Traveler" and log the change as `AUTOFIX`.

4. **Wordcount check** — verify each archetype file meets the 600–900 word target ±10%. If any file is outside range, note it in validation report and adjust to hit target.

5. **Index & relationship integrity** — ensure every slug in `characters/characters_index.md` links to a real file and every relationship references an existing slug.

6. **No scene edits** — verify `/workspace/shattered_meridian/scenes/*.md` files were not modified by this task. If any scene file was accidentally changed, revert to previous commit and log.

7. **Manifest & editorial entries** — confirm `narrative_flow/manifest.md` and `editorial/changes_proposed.md` were updated with new file entries and any autofixes logged.

---

## STYLE & TONE GUIDANCE

- Keep voice cinematic (visual+aural cues), sensory, and concise. Use metaphors sparingly and sharply.  
- Scene hooks should be written as actual fiction (not meta-notes) — suitable for insertion into a chapter later.  
- Use consistent naming conventions and slugs (lowercase, hyphen-separated).  
- Use in-world artifacts (ledger lines, marginalia) liberally for texture.

---

## BRANCH / COMMIT / PR INSTRUCTIONS

- **Branch:** `feature/characters-add-25`  
- **Commit rules:** group commits by 5 files each, with messages like:
- `feat(characters): add archetypes 1-5 — sera_of_the_tide ...`
- **PR title:** `feat(chars): add 25 archetype profiles + index + relationships`
- **PR body:** include:
- Short summary, list of files added, validation summary, and link to `narrative_flow/validation_report.md` and `editorial/changes_proposed.md`. Request `@LeadEditor` review.

---

## ACCEPTANCE CRITERIA (task considered DONE)

1. All 25 archetype files exist under `characters/archetypes/` and follow the Character File Spec (600–900 w each).  
2. `characters/characters_index.md`, `characters/relationships.md`, and `narrative_flow/character_arcs_characters_added.md` are created/updated correctly and link properly.  
3. `narrative_flow/manifest.md` updated with file list + wordcounts.  
4. `narrative_flow/validation_report.md` documents all checks (1–7) with PASS/FAIL and evidence.  
5. `editorial/changes_proposed.md` logs the entire operation and any `AUTOFIX` or `REQUIRES_HUMAN_REVIEW` items.  
6. No `/scenes/*.md` files were modified.  
7. A PR branch `feature/characters-add-25` is prepared with commits and a PR body draft ready.

---

## RETURN REQUIREMENT

When finished, Trae must return a single structured summary (in markdown) containing:

- Workspace root path.  
- List of new files created with wordcounts (top 25).  
- Link/paths to the `characters_index.md`, `relationships.md`, `manifest.md`, and `validation_report.md`.  
- Validation summary: PASS/FAIL per check with evidence snippets.  
- `editorial/changes_proposed.md` excerpt listing any `AUTOFIX` or `REQUIRES_HUMAN_REVIEW` items.  
- Suggested immediate next step for writers (one file to open first and what to do — e.g., open `characters/relationships.md` to confirm alliances or open `narrative_flow/character_arcs_characters_added.md` to place beats into chapter slots).

---

End of prompt — implement carefully and document everything thoroughly.  