# ZENITH Manifest: The Living Archive

## Project Information Architecture

The ZENITH repository follows a hierarchical flow of information from canonical sources to narrative output:

```
Canon Source (compendium/) 
├──> World Rules (systems/, world_bible/)
├──> Story Elements (characters/, locations/, organizations/)
└──> Narrative Output (manuscript/, narrative_flow/)
```

## Directory Structure & Purpose

| Directory | Purpose |
|-----------|---------|
| `manuscript/` | **Single Source of Truth** for the book. Contains the Prologue and Frontmatter. |
| `archiva/` | Integrated lore repository: Historical records, technical manuals, and God-Shard artifacts. |
| `systems/` | Mechanics: Magic systems, The 3 Laws, The Great Filter. |
| `characters/` | Profiles: The Traveler (Maer), The 25 Archetypes, and Relationships. |
| `locations/` | Geographic and political contexts for episodic quest structure. |
| `organizations/` | Factions and power structures that shape the world's conflicts. |
| `narrative_flow/` | Planning: Outline, Beat Sheets, and Story Architecture. |
| `_archive/` | Organized historical concepts and non-active drafts. |
| `art_and_aesthetics/` | Visual and auditory inspiration/motifs. |
| `compendium/` | Consolidated canonical reference materials. |
| `editorial/` | Style guides, checklists, and validation reports. |
| `templates/` | Standardized structures for consistent content creation. |

## Cross-Reference Guide

When developing content in one area, consider the following connections:

- **New Location Creation:** When creating a new location in `/locations/`, update `/organizations/` to note which faction controls it, and consider if a new God-Shard artifact needs an entry in `/archiva/artifacts/`.

- **Character Development:** When expanding a character in `/characters/`, check `/organizations/` for affiliations and `/locations/` for significant places in their history.

- **God-Shard Integration:** Each God-Shard in `/archiva/artifacts/` should connect to specific locations, characters, and system mechanics.

- **System Mechanics:** New magic systems in `/systems/` should be reflected in character abilities and location-specific phenomena.

## Key Files

- `manuscript/00_prologue.md`: The only active story draft.
- `manuscript/frontmatter.md`: Title, Dedication, and Blurb.
- `compendium/zenith_compendium.md`: The canonical source of all lore, names, rules, tone, and constraints.
- `archiva/artifacts/god_shards_catalog.md`: Master catalog of all God-Shard artifacts.
- `archiva/historical/genesis_record.md`: The canonical creation account.
- `archiva/technical/magic_protocols.md`: The fundamental rules governing magical systems.
- `STYLE_GUIDE.md`: The "Writing Constitution" for the project.
- `NARRATIVE_PROTOCOL.md`: Rulebook for all story decisions.
- `MANIFEST.md`: This file.
- `README.md`: Project overview and setup.

## Status: Fundamentals First
The repository is currently optimized for worldbuilding and character development. Active chapter writing (Book One) is deferred until fundamentals are finalized.
