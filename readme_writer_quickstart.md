# Writer Quickstart Guide

Welcome to the ZENITH writing project! This guide will help you begin writing officially.

## Getting Started

### 1. Open Required Files
- Open `narrative_flow/beat_sheets/00_prologue.md` to understand the prologue structure
- Open `templates/scene_template.md` to reference the scene construction guidelines

### 2. Duplicate Template to Create Scene
- Copy `templates/scene_template.md` to create `scenes/00_prologue_draft.md`
- The prologue scene has already been seeded with the polished cinematic draft, but you can use this process for future scenes

### 3. Naming & Branch Convention
- Create a branch: `feature/prologue-00`
- Commit your draft to that branch with message: `feat(prologue): first draft`

### 4. Local Checks Before PR
Before submitting your work, run these checks:

Ensure the canonical line exists:
```bash
grep -Rin "Mortals should not meddle with the power of the Gods" scenes/00_prologue_draft.md || true
```

Ensure no single exposition paragraph > 400 words (heuristic). If the environment supports `awk` or `python`, run a paragraph-length check; otherwise mentally split long paragraphs.

### 5. Open Pull Request
- Use `templates/pr_template.md` to structure your pull request
- In PR body include:
  - Beats implemented from `narrative_flow/beat_sheets/00_prologue.md`
  - Artifacts inserted (names/filenames)
  - Any unresolved lore questions (tag `@LeadEditor`)

### 6. Editorial Checklist (PR checklist)
- [ ] Follows `templates/scene_template.md`
- [ ] Contains prologue personalization paragraph (the one in compendium / earlier)
- [ ] Contains canonical refrain line: "Mortals should not meddle with the power of the Gods"
- [ ] Left-hand motif present at least once
- [ ] Name-Bleed sensory hint present
- [ ] No exposition > 400 words

### 7. Reviewer Actions
- Reviewer runs `narrative_flow/qa_checks.md` scripts (grep canonical lines and place-name check)
- Approve or request changes; if changing canon, file entry in `editorial/changes_proposed.md`

## Writing Guidelines

### Style & Tone
- Keep prose cinematic, sensory, and lean (avoid purple prose)
- Use the left-hand motif and prismatic / oil-on-water imagery consistently
- Do not invent new region/place names outside canonical list
- Document every expansion beyond the compendium in `editorial/changes_proposed.md`

### Canonical Requirements
- Always verify canonical phrases appear verbatim
- Maintain character constraints (nameless, left-handed, pack-carrying Traveler)
- Respect the Three Laws of Ascension in all magical workings
- Use only canonical place names: Cyris, Thalen, Virek, Kallum, Eirn, Sahru, Alkyr, Mirel, Nyth, Valen, The Hollow

### Thematic Elements
- Integrate prismatic/oil-on-water imagery for magical manifestations
- Maintain the left-hand motif for bindings and inversions
- Include appropriate sensory details (metallic tang, reedy tones, etc.)
- Reference the Name-Bleed phenomenon where appropriate

## File Organization

### Core Directories
- `scenes/` - Scene drafts and chapters
- `lore/` - Background information and history
- `characters/` - Character development materials
- `codex/` - In-world documents and lore
- `systems/` - Magic systems and mechanical rules
- `narrative_flow/` - Story planning and structure

### Reference Materials
- `compendium/zenith_compendium.md` - Canonical source reference
- `narrative_flow/narrative_master.md` - Overall story structure
- `characters/traveler.md` - Character constraints and details

## Next Steps

1. Begin editing the seeded prologue draft in `scenes/00_prologue_draft.md`
2. Create your feature branch following the naming convention
3. Make your commits and prepare your PR using the template
4. Submit for review following the checklist requirements

Happy writing!