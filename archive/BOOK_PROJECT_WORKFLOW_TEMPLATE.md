# Generic Book-Writing Workflow System

**Version:** 1.0
**Based on:** Analysis of JRock, VGM/Silicon Symphonies, and Tatsuro Yamashita projects
**Authors:** Claude (Prose & Analysis) + Gemini (Architecture & Design)
**Date:** 2026-01-05

---

## Executive Summary

This document provides a reusable, modular workflow template optimized for:

- **Quality:** Academic rigor, multi-agent review, technical accuracy verification
- **Efficiency:** Token optimization, clear handoff protocols, parallel agent work
- **Scalability:** Works for theory books, biographies, technical guides
- **Publication-Ready:** KDP-compliant output structure

### Core Principle: Division of Labor

| Agent | Primary Role | Key Responsibilities |
|-------|-------------|---------------------|
| **Gemini** | Architect & Researcher | Planning, research briefs, technical review, quality assurance |
| **Claude** | Writer & Editor | Prose generation, de-AI-ification, editorial polish, compilation |
| **User** | Director & Asset Creator | Strategic decisions, visual assets, final approval |

---

## A. Directory Structure Template

Create this structure when initializing a new book project:

```
PROJECT_ROOT/
├── GEMINI.md                          # Gemini's operational context
├── CLAUDE.md                          # Claude's writing guidelines
├── TODO.md                            # Shared task tracking with agent ownership
│
├── manuscript/                        # ALL PROSE AND COMPILED OUTPUT
│   ├── 00_master_outline.md          # Full TOC + chapter summaries
│   ├── [BOOK_TITLE]_final.md         # Compiled manuscript (generated)
│   ├── chapters/                     # Individual chapter files
│   │   ├── 01_[chapter_title].md
│   │   ├── 02_[chapter_title].md
│   │   └── ...
│   ├── front_matter/
│   │   ├── 00_copyright.md
│   │   ├── 01_toc.md
│   │   ├── 02_introduction.md
│   │   └── [acknowledgments, dedication].md
│   ├── back_matter/
│   │   ├── appendix_a.md
│   │   ├── glossary.md
│   │   ├── bibliography.md
│   │   └── about_author.md
│   └── drafts/                       # Scratch work, rejected versions
│
├── context/                           # Agent personas and specialized guidance
│   ├── WRITER_VOICE.md               # Writing voice, tone, style examples
│   ├── TECHNICAL_REVIEWER.md         # Subject matter expert persona
│   ├── KDP_EXPERT.md                 # Publishing format/metadata guidance
│   ├── STORY_BIBLE.md               # (Biography only) Character details
│   ├── FACTS_SHEET.md               # Key facts, sources, ban lists
│   └── [CUSTOM_PERSONA].md          # Project-specific reviewer
│
├── research/                         # Gemini's research briefs
│   ├── [topic_1].md                  # Research brief on topic 1
│   ├── [topic_2].md
│   ├── sources/                      # Raw source material
│   └── reviews/                      # Persona-based chapter reviews
│       ├── chapter_01_review.md
│       └── chapter_01_responses.md
│
├── reference/                        # Shared resources
│   ├── editorial_guide.md            # Extended style guide
│   ├── collaboration_workflow.md     # Agent handoff system
│   ├── quality_gates.md              # Review checkpoints
│   ├── tone_examples.md              # Good/bad writing examples
│   ├── art_brief.md                  # Visual asset requirements
│   └── kdp_checklist.md              # KDP formatting requirements
│
├── visuals/                          # Generated images and diagrams
│   ├── figures/
│   ├── diagrams/
│   └── generated/
│
├── .vale/                            # Prose linting (optional)
│   ├── .vale.ini
│   └── styles/
│
└── output/                           # Build artifacts
    ├── [book_title]_final.pdf
    ├── [book_title]_final.epub
    └── kdp_metadata.txt
```

---

## B. Phase-by-Phase Workflow

### PHASE 0: PROJECT INITIALIZATION

**Duration:** 1-2 hours
**Agent:** User + Gemini

**Tasks:**
1. Create directory structure
2. Define project scope (book type, word count, audience, timeline)
3. Populate initial context files:
   - `GEMINI.md` with project identity and core thesis
   - `CLAUDE.md` with voice/tone guidance
   - `context/WRITER_VOICE.md` with specific style examples
   - `context/FACTS_SHEET.md` or `context/STORY_BIBLE.md`
4. Create master outline skeleton in `manuscript/00_master_outline.md`

**Output:** Project initialized; agents understand scope and voice.

---

### PHASE 1: RESEARCH & OUTLINING

**Duration:** 2-4 weeks
**Primary Agent:** Gemini

**Tasks:**
1. **Deep Research:** Conduct web research, read source materials
2. **Research Briefs:** Create structured briefs in `research/[topic].md`
3. **Outlining:** Update `00_master_outline.md` with detailed chapter summaries
4. **Content Planning:** Define strategic pillars, visual requirements

**Output:** Comprehensive outline, 15-30 research briefs, bibliography skeleton

---

### PHASE 2: INITIAL PROSE DRAFTING

**Duration:** 3-8 weeks
**Primary Agent:** Claude

**Tasks:**
1. Read chapter summaries and research briefs
2. Draft chapter prose in `manuscript/chapters/`
3. Apply voice guidance from `CLAUDE.md`
4. First-pass De-AI-ify (remove banned words, passive voice)
5. Add citations (APA format)

**Output:** Draft chapters marked `[DRAFT]` in TODO.md

---

### PHASE 3: TECHNICAL REVIEW & ACCURACY PASS

**Duration:** 1-3 weeks
**Primary Agent:** Gemini

**Tasks:**
1. Verify factual claims against research briefs
2. Check bibliography citations
3. Flag incomplete technical details
4. Create review documents in `research/reviews/`

**Output:** Review documents; chapters marked `[REVIEW READY]`

---

### PHASE 4: PERSONA-BASED REVIEW

**Duration:** 1-2 weeks
**Primary Agent:** Gemini (creates reviews) + Claude (responds)

**The 6 Review Personas:**

| Persona | Focus |
|---------|-------|
| Developmental Editor | Structure, pacing, engagement |
| Copy Editor | Grammar, consistency, sentence variety |
| KDP Expert | Market viability, metadata, formatting |
| SME 1 (Subject Matter) | Technical accuracy, depth |
| SME 2 (Domain-Specific) | Project-specific expertise |
| Target Reader | Accessibility, practical value |

**Process:**
1. Gemini generates persona feedback → `research/reviews/chapter_X_personas.md`
2. Claude responds with AGREED/DISAGREED/NEEDS DISCUSSION
3. Implement agreed items; escalate disputes to user

**Output:** Updated chapters with agreed changes; `[PERSONA REVIEW COMPLETE]`

---

### PHASE 5: COMPREHENSIVE EDITORIAL PASS

**Duration:** 2-4 weeks
**Primary Agent:** Claude

**Tasks:**
1. **De-AI-ify Protocol:** Run Vale linting, remove all banned words
2. **Consistency Pass:** Verify terms, names, dates, cross-references
3. **Voice Consistency:** Read-aloud test
4. **Final Proofread:** Typos, formatting

**Output:** Polished chapters with all Vale errors fixed; `[EDITORIAL COMPLETE]`

---

### PHASE 6: COMPILATION & INTEGRATION

**Duration:** 1 week
**Primary Agent:** Claude

**Tasks:**
1. Assemble front matter (copyright, TOC, introduction)
2. Compile full manuscript (use PowerShell/bash script)
3. Verify all cross-references work
4. Final integrated review for flow

**Output:** Single compiled manuscript file

---

### PHASE 7: VISUAL PRODUCTION

**Duration:** 2-4 weeks
**Agent:** User (with Gemini guidance)

**Tasks:**
1. Generate visual assets from `reference/art_brief.md`
2. Insert image references into manuscript
3. Re-compile with images embedded

**Output:** Final manuscript with all visuals integrated

---

### PHASE 8: KDP FORMATTING & PUBLICATION PREP

**Duration:** 1-2 weeks
**Agent:** User

**Tasks:**
1. Create KDP metadata (title, description, keywords)
2. Convert to PDF/ePub
3. Final checklist verification
4. Both agents sign-off in TODO.md

**Output:** KDP-ready files in `output/`

---

### PHASE 9: PUBLICATION & LAUNCH

**Duration:** 1 week
**Agent:** User

Upload to KDP, set launch date, marketing.

---

## C. File Templates

### Template 1: GEMINI.md

```markdown
# GEMINI.md - Research, Planning & Quality Assurance

**Project:** [Project Name]
**Role:** Architect & Researcher
**Current Phase:** [PHASE]

---

## 1. Project Identity

### Thesis Statement
[One paragraph: What is this book arguing?]

### Target Audience
[Who is reading this?]

### Strategic Pillars
1. [Pillar 1]
2. [Pillar 2]
3. [Pillar 3]

---

## 2. Scope & Constraints

- **Word Count Target:** [e.g., 60,000]
- **Chapter Count:** [e.g., 12 + appendix]
- **Timeline:** [Start - Publication target]
- **Visual Asset Budget:** [Number]

---

## 3. Verified Research Findings

### Key Sources
- [Source 1]
- [Source 2]

### Technical Foundations
[Core technical knowledge to prevent hallucinations]

### Ban List (Avoid These Claims)
- [Claim to avoid 1]

---

## 4. Operational Protocol

### When Starting a Session
1. Read this file for context
2. Read TODO.md for pending tasks
3. Check research/ for gap areas
4. Review Claude's latest prose for accuracy

### Creating Research Briefs
- Location: `research/[topic_name].md`
- Format: Structured facts, citations—NOT prose paragraphs
- Include: Sources, dates, confidence level

---

## 5. Session History

### [Date]: [Session Title]
- **Actions:** [What was done]
- **Current State:** [Where project stands]
- **Next Steps:** [What's next]
- **Handoffs to Claude:** [Specific items]
```

---

### Template 2: CLAUDE.md

```markdown
# CLAUDE.md - Prose Writing & Editorial Guidance

**Project:** [Project Name]
**Your Role:** Lead Writer & Editor

---

## 1. Role Definition

**You are the writer and editor.** Transform research briefs into polished prose.

### Core Responsibilities
1. Prose Writing (draft/revise based on outlines and briefs)
2. Editorial Execution (De-AI-ify, style guide enforcement)
3. Manuscript Compilation (maintain final manuscript)
4. Persona Review Collaboration (respond to Gemini's feedback)

---

## 2. Writing Style & Tone

### Established Voice
[2-3 sentences describing the voice]

**Characteristics:**
- [Trait 1]
- [Trait 2]

### Example of Good Voice
> [Good example]

### Example of Bad Voice
> [Bad example]

---

## 3. Banned Words & Phrases (De-AI-ify)

**MUST REMOVE:**
- delve, dive deep, tapestry, landscape, realm
- testament to, undeniable, invaluable, crucially
- it's important to note, seamlessly, utilize, leverage

**MUST REDUCE:**
- however, it is, very, quite, arguably, notably

---

## 4. De-AI-ify Protocol

Before marking prose complete:
1. Banned Word Grep
2. Vale Lint (if configured)
3. Passive Voice Check
4. Read-Aloud Test
5. Specificity Check

---

## 5. Content Validation Checklist

- [ ] Aligns with strategic pillar
- [ ] Voice consistent
- [ ] De-AI-ify complete
- [ ] Technical claims verified
- [ ] Citations in APA format
- [ ] Bibliography updated

---

## 6. What Claude Does NOT Do

- Update GEMINI.md
- Conduct web research
- Change chapter structure/outline
- Make strategic scope decisions
```

---

### Template 3: TODO.md

```markdown
# Project TODO List

## Task Ownership Legend
- `[GEMINI]` — Research, planning, QA
- `[CLAUDE]` — Prose writing, editorial
- `[USER]` — Human decisions, asset creation
- `[HANDOFF]` — Ready for other agent
- `[x]` — Completed

---

## CURRENT PHASE: [Phase Name]

**STATUS:** [ON TRACK / BLOCKED / NEEDS DECISION]

### CRITICAL
- [ ] `[OWNER]` **Task**: Description

### HIGH PRIORITY
- [ ] `[OWNER]` **Task**: Description

### MEDIUM PRIORITY
- [ ] `[OWNER]` **Task**: Description

---

## HANDOFF READY

- [ ] `[HANDOFF to CLAUDE]` [Description]
- [ ] `[HANDOFF to GEMINI]` [Description]

---

## COMPLETED

### Phase X — Completed [Date]
- [x] `[OWNER]` Task — Done [Date]
```

---

### Template 4: context/WRITER_VOICE.md

```markdown
# WRITER VOICE GUIDE

## Target Voice: [e.g., "Expert Enthusiast"]

### Voice Inspirations
- [Author 1]: [Why]
- [Author 2]: [Why]

---

## Tone Characteristics

**DO:**
- [Trait 1] - [Example]

**DON'T:**
- [Trap 1] - [Bad example]

---

## Technical Integration

How to weave technical details naturally:
- [Pattern] - [Example]

---

## Voice Checklist

- [ ] Would I say this to a friend?
- [ ] Does it sound like me?
- [ ] Is technical detail integrated, not bolted-on?
```

---

## D. Quality Assurance System

### Persona Review Process

1. **Gemini Creates Review:** Generate feedback from all 6 personas
   - File: `research/reviews/chapter_X_personas.md`

2. **Claude Responds:** Mark each item as:
   - `AGREED` — Will implement
   - `DISAGREED` — Will not implement (with reason)
   - `NEEDS DISCUSSION` — Wants to discuss

3. **Consensus Rules:**
   - AGREED items: Implement immediately
   - DISAGREED items: Document reason; no action
   - NEEDS DISCUSSION: Both agents reply; user arbitrates if no consensus

---

### Quality Gates Checklist

**End of Phase 5 (Editorial):**
- [ ] Vale: 0 errors
- [ ] De-AI-ify: 0 banned words
- [ ] Passive voice: < 5% of sentences
- [ ] All names/dates/refs verified
- [ ] 0 typos

**End of Phase 8 (Pre-Publication):**
- [ ] PDF generates without errors
- [ ] Metadata complete
- [ ] Both agents signed off

---

### Critical Errors (STOP and Fix)

- Typo in title/chapter heading
- Wrong citation date
- Broken cross-reference
- Missing referenced image
- Inconsistent terminology
- Unfixed Vale error

---

## E. Efficiency Recommendations

### Token Optimization Strategies

| Strategy | Description |
|----------|-------------|
| **Parallel Work** | Gemini researches while Claude drafts previous chapter |
| **Structured Briefs** | Gemini provides facts, not prose; Claude converts to narrative |
| **Reusable Briefs** | Create once, reference multiple times |
| **Batch Similar Tasks** | All De-AI-ify passes in one session |
| **Clear Handoffs** | Eliminate ambiguity; include all required files |
| **Phase Boundaries** | Clear handoffs prevent half-done rework |

### Research Brief Efficiency

**Good (Token-Efficient):**
```
## Key Facts
- YM2612: 6 FM channels + 1 DAC
- Ladder Effect distortion
- Max polyphony: 16 notes
```

**Bad (Token-Heavy):**
```
The YM2612 chip represents a significant evolution in FM synthesis,
featuring six FM channels alongside a single DAC channel...
```

---

## F. Communication Protocol

### Handoff Format in TODO.md

```
- [ ] `[HANDOFF to CLAUDE]` Chapter 3 draft + research brief ready
      - Input: research/chapter_3_context.md
      - Output: manuscript/chapters/03_[title].md
      - Prerequisites: Chapter 2 complete
```

### File Ownership Matrix

| File | Gemini Writes | Claude Writes |
|------|---------------|---------------|
| `GEMINI.md` | Yes | No |
| `CLAUDE.md` | No | Yes |
| `TODO.md` | Yes | Yes |
| `manuscript/chapters/` | No | Yes |
| `manuscript/00_master_outline.md` | Yes | No |
| `research/` | Yes | No |
| `research/reviews/` | Yes | Yes (responses) |

---

## G. Session Wrap-Up Protocol

### Gemini (in GEMINI.md Session History)
```
### [Date]: [Session Title]
- **Actions:** [What was done]
- **Current State:** [Project status]
- **Next Steps:** [What's next]
- **Handoffs to Claude:** [Items ready]
```

### Claude (in TODO.md)
```
## Session: [Date] Claude [Phase]
- [x] `[CLAUDE]` [Task] (Done [Date])
- [ ] `[HANDOFF to GEMINI]` [Task ready]
```

---

## H. Project Initialization Checklist

When starting a new book project:

1. [ ] Create directory structure (Section A)
2. [ ] Customize GEMINI.md with project identity
3. [ ] Customize CLAUDE.md with voice/tone
4. [ ] Create context/WRITER_VOICE.md with examples
5. [ ] Create context/FACTS_SHEET.md or STORY_BIBLE.md
6. [ ] Initialize TODO.md with Phase 1 tasks
7. [ ] Create manuscript/00_master_outline.md skeleton
8. [ ] (Optional) Set up Vale linting
9. [ ] (Optional) Initialize git repository

---

## Final Sign-Off Template

```markdown
## Publication Sign-Off

**Gemini Sign-Off:**
[x] GEMINI Final QA Pass — [Date]
    All technical facts verified. No factual errors.
    Signature: Gemini

**Claude Sign-Off:**
[x] CLAUDE Final Editorial Pass — [Date]
    All prose polished. De-AI-ify complete.
    Signature: Claude

**User Sign-Off:**
[x] USER Final Approval — [Date]
    Reviewed all phases. Authorizing publication.
    Signature: [User]
```

---

*This template is designed to be copied and customized for each new book project. The structural system remains constant; voice, personas, and content adapt to each project's needs.*
