# Pull Request Template

## PR Title
```
feat/chore/fix(scene-number): brief description of changes
```

## Description
Provide a brief explanation of the changes in this pull request:

### Scenes Updated
- [List the scene files modified]

### Beats Implemented
- [List which beats from narrative_flow/beat_sheets/ were implemented]

### Artifacts Inserted
- [List any new names, concepts, or lore elements introduced]

### Unresolved Issues
- [Tag @LeadEditor for any lore questions or unresolved canonical issues]

## Validation Checklist

### Pre-Merge Requirements
- [ ] Follows `templates/scene_template.md`
- [ ] Contains prologue personalization paragraph (the one in compendium / earlier)
- [ ] Contains canonical refrain line: "Mortals should not meddle with the power of the Gods"
- [ ] Left-hand motif present at least once
- [ ] Name-Bleed sensory hint present
- [ ] No exposition > 400 words

### Automated Checks Passed
- [ ] Ran canonical line check: `grep -Rin "Mortals should not meddle with the power of the Gods" scenes/[scene-file].md || true`
- [ ] Verified no single exposition paragraph > 400 words

## Reviewer Actions
- [ ] Reviewer runs `narrative_flow/qa_checks.md` scripts (grep canonical lines and place-name check)
- [ ] Approve or request changes
- [ ] If changing canon, file entry in `editorial/changes_proposed.md`

## Additional Notes
[Any additional context or notes for reviewers]