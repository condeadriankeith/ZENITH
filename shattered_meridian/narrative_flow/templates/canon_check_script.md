# Canon Check Script (PowerShell)

## Canonical Verbatim Strings
Run these commands to verify the presence of non-negotiable canon in your chapter files.

### 1. The Fracture Paragraph
```powershell
$pattern = "In the year 907 of the Reckoning, the Treaty of Three Stones"
Select-String -Path "chapters/*.md" -Pattern $pattern
```

### 2. The Three Laws of Ascension
```powershell
$pattern = "THE THREE LAWS OF ASCENSION"
Select-String -Path "chapters/*.md" -Pattern $pattern
```

### 3. Name-Bleed Sensory
```powershell
$pattern = "Names leak like blood from a wound"
Select-String -Path "chapters/*.md" -Pattern $pattern
```

### 4. Forbidden Terms
```powershell
$forbidden = "magic wand|wizard|mana|computer"
$matches = Select-String -Path "chapters/*.md" -Pattern $forbidden
if ($matches) { Write-Host "CRITICAL: Forbidden terms found in $($matches.Path)" -ForegroundColor Red }
```

### 5. Region Name Verification
```powershell
$regions = "Cyris|Thalen|Virek|Kallum|Eirn|Sahru|Alkyr|Mirel|Nyth|Valen|The Hollow"
# (Manual check recommended for context, but this highlights usage)
Select-String -Path "chapters/*.md" -Pattern $regions
```
