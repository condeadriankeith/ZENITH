# QA Checks

## Automated Validation Scripts

### 1. Canonical Phrase Verification
```bash
# Check for required canonical phrases in specified files
grep -Rin "Mortals should not meddle with the power of the Gods" scenes/ || echo "MISSING: Canonical refrain not found in scenes/"
grep -Rin "THE THREE LAWS OF ASCENSION" systems/ascension_laws_plaque.md || echo "MISSING: Ascension Laws plaque not found"
grep -Rin "THE THREE LAWS OF ASCENSION" codex/codex_of_realms.md || echo "MISSING: Ascension Laws in codex"
grep -Rin "Name-Bleed" bestiary/bestiary.md || echo "MISSING: Name-Bleed reference in bestiary"
grep -Rin "Name-Bleed" lore/lore_entries/01_fracture.md || echo "MISSING: Name-Bleed reference in lore entry"
```

### 2. Place Name Verification
```bash
# Verify all canonical place names exist in the work
PLACE_NAMES="Cyris Thalen Virek Kallum Eirn Sahru Alkyr Mirel Nyth Valen The Hollow"
for place in $PLACE_NAMES; do
  FOUND=$(grep -r "$place" . --include="*.md" | wc -l)
  if [ $FOUND -lt 1 ]; then
    echo "WARNING: Place name '$place' not found in any document"
  fi
done
```

### 3. Character Constraint Verification
```bash
# Verify Traveler constraints are maintained
grep -ri "nameless" characters/traveler.md || echo "WARNING: 'nameless' trait not found in character file"
grep -ri "left-handed" characters/traveler.md || echo "WARNING: 'left-handed' trait not found in character file"
grep -ri "pack" characters/traveler.md || echo "WARNING: 'pack' reference not found in character file"
```

### 4. Exposition Length Check
```bash
# Check for exposition paragraphs longer than 400 words
# This would require a more complex script to count words between paragraph breaks
echo "Manual check required: Verify no single exposition paragraph exceeds 400 words"
```

## Manual Verification Checklist

### A. Canon Compliance
- [ ] The Fracture (907 R) paragraph appears verbatim in `codex/codex_of_realms.md`
- [ ] The Fracture (907 R) paragraph appears verbatim in `lore/lore_entries/01_fracture.md`
- [ ] THE THREE LAWS OF ASCENSION appear verbatim in `systems/ascension_laws_plaque.md`
- [ ] THE THREE LAWS OF ASCENSION appear verbatim in `codex/codex_of_realms.md`
- [ ] Name-Bleed sensory paragraph appears in `bestiary/bestiary.md`
- [ ] Name-Bleed sensory paragraph appears in at least one lore entry
- [ ] Name-Bleed sensory paragraph appears in at least one scene

### B. Character Constraints
- [ ] Traveler is consistently referred to as nameless
- [ ] Traveler is consistently described as left-handed
- [ ] Traveler carries a pack of knowledge
- [ ] Traveler has three emotional anchors: (a) mother's name traded, (b) failed rescue, (c) lost Archivist mentor
- [ ] Left-hand motif appears consistently throughout

### C. Place Name Accuracy
- [ ] Cyris appears correctly (not Cirus, Siryc, etc.)
- [ ] Thalen appears correctly
- [ ] Virek appears correctly
- [ ] Kallum appears correctly
- [ ] Eirn appears correctly
- [ ] Sahru appears correctly
- [ ] Alkyr appears correctly
- [ ] Mirel appears correctly
- [ ] Nyth appears correctly
- [ ] Valen appears correctly
- [ ] The Hollow appears correctly

### D. World Building Consistency
- [ ] Three Laws of Ascension are respected in all magical workings
- [ ] Magic taxonomy is applied correctly (Spirit, Covenant, Engineered, Tidal, Void-Edge)
- [ ] Left-hand rites and inversion mechanics are used consistently
- [ ] Entropy consequences are tracked and acknowledged
- [ ] Political targeting consequences are shown

### E. Thematic Consistency
- [ ] Prismatic/oil-on-water imagery used for magical manifestations
- [ ] Name importance and identity themes explored
- [ ] Sacrifice and cost themes present
- [ ] Balance vs. progress themes explored

## Scene-Specific Checks

### For Prologue Scene
- [ ] Contains canonical refrain verbatim: "Mortals should not meddle with the power of the Gods"
- [ ] Left-hand motif present
- [ ] Name-Bleed sensory hint present
- [ ] Traveler's emotional anchors referenced
- [ ] Proper personalization paragraph included

### For All Scenes
- [ ] No single exposition paragraph exceeds 400 words
- [ ] Magic system rules followed consistently
- [ ] Character traits maintained
- [ ] Canonical phrases preserved
- [ ] Thematic elements integrated

## Validation Output Log

### Results Template
```
VALIDATION RESULTS - $(date)
==========================

Automated Checks:
- Canonical phrases: [PASS/FAIL/MANUAL REVIEW]
- Place names: [PASS/FAIL/MANUAL REVIEW] 
- Character constraints: [PASS/FAIL/MANUAL REVIEW]
- File structure: [PASS/FAIL/MANUAL REVIEW]

Manual Checks:
- Canon compliance: [PASS/FAIL/MANUAL REVIEW]
- Character consistency: [PASS/FAIL/MANUAL REVIEW]
- World building: [PASS/FAIL/MANUAL REVIEW]
- Thematic integration: [PASS/FAIL/MANUAL REVIEW]

Issues Found:
- [List any specific issues discovered]

Recommended Actions:
- [List any required fixes or changes]
```

## Continuous Integration Commands

### Quick Validation Command
```bash
echo "Running Shattered Meridian validation suite..."
echo "Checking canonical phrases..."
grep -r "Mortals should not meddle with the power of the Gods" . --include="*.md" | wc -l
echo "Checking place names..."
grep -r "Cyris\|Thalen\|Virek\|Kallum\|Eirn\|Sahru\|Alkyr\|Mirel\|Nyth\|Valen" . --include="*.md" | wc -l
echo "Validation complete."
```

### Comprehensive Validation Command
```bash
#!/bin/bash
# Run comprehensive validation of all canonical elements

echo "=== SHATTERED MERIDIAN COMPREHENSIVE VALIDATION ==="
echo ""

# Check for canonical refrain
echo "Checking for canonical refrain..."
REFRAIN_COUNT=$(grep -r "Mortals should not meddle with the power of the Gods" . --include="*.md" | wc -l)
echo "Found refrain in $REFRAIN_COUNT location(s)"

# Check for ascension laws
echo "Checking for ascension laws..."
LAWS_COUNT=$(grep -r "THE THREE LAWS OF ASCENSION" . --include="*.md" | wc -l)
echo "Found ascension laws in $LAWS_COUNT location(s)"

# Check for name-bleed
echo "Checking for name-bleed references..."
BLEED_COUNT=$(grep -ri "Name-Bleed\|names leak like blood" . --include="*.md" | wc -l)
echo "Found name-bleed references in $BLEED_COUNT location(s)"

# Check for place names
echo "Checking for place names..."
PLACE_COUNT=$(grep -r "Cyris\|Thalen\|Virek\|Kallum\|Eirn\|Sahru\|Alkyr\|Mirel\|Nyth\|Valen\|The Hollow" . --include="*.md" | wc -l)
echo "Found place names referenced $PLACE_COUNT times"

# Check for character constraints
echo "Checking for Traveler constraints..."
NAMELESS_COUNT=$(grep -ri "nameless" characters/traveler.md | wc -l)
LEFTHAND_COUNT=$(grep -ri "left-handed" characters/traveler.md | wc -l)
PACK_COUNT=$(grep -ri "pack" characters/traveler.md | wc -l)
echo "Found 'nameless': $NAMELESS_COUNT, 'left-handed': $LEFTHAND_COUNT, 'pack': $PACK_COUNT"

echo ""
echo "=== VALIDATION COMPLETE ==="
```