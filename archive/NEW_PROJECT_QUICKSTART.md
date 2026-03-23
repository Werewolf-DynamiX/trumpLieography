# New Book Project Quick Start Guide

This guide walks you through initializing a new book project using the workflow template.

---

## Step 1: Create Project Folder

```powershell
# Replace PROJECT_NAME with your project folder name
$PROJECT = "MyNewBook"
$BASE = "C:\Users\toast\Documents\Books"

# Create directory structure
New-Item -ItemType Directory -Path "$BASE\$PROJECT" -Force
Set-Location "$BASE\$PROJECT"

# Create subdirectories
@(
    "manuscript",
    "manuscript\chapters",
    "manuscript\front_matter",
    "manuscript\back_matter",
    "manuscript\drafts",
    "context",
    "research",
    "research\sources",
    "research\reviews",
    "reference",
    "visuals",
    "visuals\figures",
    "visuals\diagrams",
    "visuals\generated",
    "output"
) | ForEach-Object { New-Item -ItemType Directory -Path $_ -Force }

Write-Host "Project structure created at: $BASE\$PROJECT"
```

---

## Step 2: Copy Template Files

Copy these from the template:

```powershell
# Copy from template (adjust paths as needed)
Copy-Item "$BASE\BOOK_PROJECT_WORKFLOW_TEMPLATE.md" -Destination ".\reference\workflow_reference.md"
```

---

## Step 3: Initialize Core Files

### 3A: Create GEMINI.md

```powershell
@"
# GEMINI.md - Research, Planning & Quality Assurance

**Project:** [PROJECT TITLE]
**Role:** Architect & Researcher
**Current Phase:** Phase 0: Initialization

---

## 1. Project Identity

### Thesis Statement
[What is this book arguing or teaching?]

### Target Audience
[Who is reading this? What problem does it solve?]

### Strategic Pillars
1. [Pillar 1]
2. [Pillar 2]
3. [Pillar 3]

---

## 2. Scope & Constraints

- **Word Count Target:** [e.g., 50,000]
- **Chapter Count:** [e.g., 10-12]
- **Timeline:** [Start date] - [Target publication]
- **Visual Asset Budget:** [Number of figures/diagrams]

---

## 3. Ban List (AI-isms to Avoid)

- delve, tapestry, landscape, realm, testament
- utilize, leverage, facilitate, embark
- arguably, notably, interestingly, crucially
- it's important to note, in conclusion

---

## 4. Operational Protocol

### When Starting a Session
1. Read this file for context
2. Read TODO.md for pending tasks
3. Check research/ for gap areas

### Creating Research Briefs
- Location: research/[topic_name].md
- Format: Structured facts, NOT prose

---

## 5. Session History

### [DATE]: Project Initialization
- **Actions:** Created project structure
- **Current State:** Ready for Phase 1
- **Next Steps:** Begin research and outlining
"@ | Set-Content "GEMINI.md"
```

### 3B: Create CLAUDE.md

```powershell
@"
# CLAUDE.md - Prose Writing & Editorial Guidance

**Project:** [PROJECT TITLE]
**Your Role:** Lead Writer & Editor

---

## 1. Role Definition

**You are the writer and editor.** Transform research briefs into polished prose.

### Core Responsibilities
1. Draft and revise chapters based on outlines
2. Apply De-AI-ify protocol
3. Maintain manuscript compilation
4. Respond to persona reviews

---

## 2. Writing Style & Tone

### Established Voice
[Describe the voice in 2-3 sentences]

**Characteristics:**
- [Tone trait 1]
- [Tone trait 2]
- [Tone trait 3]

---

## 3. Banned Words (De-AI-ify)

**MUST REMOVE:**
- delve, dive deep, tapestry, landscape
- testament to, undeniable, crucially
- it's important to note, seamlessly
- utilize, leverage, facilitate

**MUST REDUCE:**
- however, therefore, it is
- very, quite, rather, somewhat
- arguably, notably, interestingly

---

## 4. Content Validation Checklist

Before marking prose complete:
- [ ] Voice consistent with established tone
- [ ] De-AI-ify pass completed
- [ ] Technical claims verified against research
- [ ] Citations in APA format
- [ ] Read aloud for flow

---

## 5. What Claude Does NOT Do

- Update GEMINI.md
- Conduct web research (request a brief instead)
- Change chapter structure without proposal
- Make strategic scope decisions
"@ | Set-Content "CLAUDE.md"
```

### 3C: Create TODO.md

```powershell
@"
# Project TODO List

## Task Ownership Legend
- [GEMINI] - Research, planning, QA
- [CLAUDE] - Prose writing, editorial
- [USER] - Decisions, asset creation
- [HANDOFF] - Ready for other agent
- [x] - Completed

---

## CURRENT PHASE: Phase 1 - Research & Outlining

**STATUS:** STARTING

### HIGH PRIORITY

- [ ] [GEMINI] Define project scope in GEMINI.md
- [ ] [GEMINI] Create master outline in manuscript/00_master_outline.md
- [ ] [GEMINI] Research brief: [Topic 1]
- [ ] [GEMINI] Research brief: [Topic 2]
- [ ] [USER] Provide source materials in research/sources/

### MEDIUM PRIORITY

- [ ] [GEMINI] Create context/WRITER_VOICE.md with examples
- [ ] [GEMINI] Create context/FACTS_SHEET.md
- [ ] [GEMINI] Define visual asset requirements

---

## HANDOFF READY

(Items ready for handoff appear here)

---

## COMPLETED

### Phase 0 - Initialization
- [x] [USER] Create project directory structure - Done [DATE]
- [x] [USER] Initialize core files - Done [DATE]
"@ | Set-Content "TODO.md"
```

### 3D: Create Master Outline Skeleton

```powershell
@"
# Master Outline: [BOOK TITLE]

**Status:** Draft
**Last Updated:** [DATE]

---

## Front Matter

### Introduction
- **Purpose:** [Why this book exists]
- **Key Points:** [What reader will learn]

---

## Part I: [Section Title]

### Chapter 1: [Title]
- **Thematic Purpose:** [So what?]
- **Key Sections:**
  1. [Section A]
  2. [Section B]
- **Visual Assets:** [Diagrams needed]
- **Research Briefs:** [research/chapter_1_*.md]

### Chapter 2: [Title]
- **Thematic Purpose:** [So what?]
- **Key Sections:**
  1. [Section A]
  2. [Section B]

---

## Part II: [Section Title]

### Chapter 3: [Title]
[Continue pattern...]

---

## Back Matter

### Glossary
Key terms to define: [List]

### Bibliography
Initial sources: [List]

### Appendices
- Appendix A: [Topic]
- Appendix B: [Topic]
"@ | Set-Content "manuscript\00_master_outline.md"
```

---

## Step 4: Begin Phase 1

1. **Gemini Session:** Read GEMINI.md, begin research
2. **Update TODO.md** with specific research tasks
3. **Create research briefs** as topics are researched
4. **Refine outline** in `manuscript/00_master_outline.md`

---

## Compilation Command Template

When ready to compile the full manuscript:

```powershell
# Adjust file list to match your actual chapters
Get-Content "manuscript/front_matter/00_copyright.md",
            "manuscript/front_matter/01_toc.md",
            "manuscript/front_matter/02_introduction.md",
            "manuscript/chapters/01_*.md",
            "manuscript/chapters/02_*.md",
            "manuscript/chapters/03_*.md",
            # ... continue for all chapters ...
            "manuscript/back_matter/glossary.md",
            "manuscript/back_matter/bibliography.md",
            "manuscript/back_matter/about_author.md" |
Set-Content "manuscript/[BOOK_TITLE]_final.md"
```

---

## Quality Gates Reminder

Before publication:
- [ ] 0 Vale errors (if configured)
- [ ] 0 banned words
- [ ] All citations verified
- [ ] All cross-references accurate
- [ ] All images in place
- [ ] Both agents signed off
- [ ] PDF generates without errors

---

## Need Help?

- **Workflow Reference:** `reference/workflow_reference.md`
- **Full Template:** `C:\Users\toast\Documents\Books\BOOK_PROJECT_WORKFLOW_TEMPLATE.md`
