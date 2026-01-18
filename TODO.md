# Project TODO List

## Task Ownership Legend
- `[GEMINI]` - Research, planning, QA
- `[CLAUDE]` - Prose writing, editorial
- `[USER]` - Human decisions, asset creation
- `[HANDOFF]` - Ready for other agent
- `[x]` - Completed

---

## CURRENT PHASE: Phase 5 - Editorial Review & Quality Audit

**STATUS:** IN PROGRESS

---

## CRITICAL

- [ ] `[GEMINI]` **Full File Audit:** Review all project files for completeness and consistency
- [ ] `[GEMINI]` **Unbiased Manuscript Review:** Comprehensive quality assessment of the draft
- [ ] `[CLAUDE]` **De-AI-ify Final Pass:** Remove all banned words and AI-isms from manuscript

## HIGH PRIORITY

- [ ] `[CLAUDE]` **Word Count Reduction:** Cut from ~14,000 to target 10,000-12,000 words
- [ ] `[GEMINI]` **Persona Review:** Generate feedback from all 6 review personas
- [ ] `[CLAUDE]` **Voice Consistency Audit:** Verify Trump voice throughout all chapters
- [ ] `[USER]` **Legal Review Decision:** Confirm Michelle Obama foreword framing is sufficient

## MEDIUM PRIORITY

- [ ] `[GEMINI]` **Migrate Content:** Move manuscript sections to `manuscript/chapters/` structure
- [ ] `[CLAUDE]` **Motif Capping:** Limit "crying strong men" gag to 3-4 instances
- [ ] `[CLAUDE]` **Superlative Audit:** Vary "tremendous" with alternatives
- [ ] `[GEMINI]` **Form Variation:** Identify opportunities for fake tweets, memos, letters

## LOW PRIORITY

- [ ] `[USER]` **KDP Metadata:** Prepare title, description, keywords, categories
- [ ] `[USER]` **Cover Design:** Commission or create book cover
- [ ] `[CLAUDE]` **Final Formatting:** Apply KDP paragraph rules

---

## HANDOFF READY

- [ ] `[HANDOFF to GEMINI]` Draft manuscript ready for comprehensive review
- [ ] `[HANDOFF to CLAUDE]` After Gemini audit, implement recommended changes

---

## COMPLETED

### Phase 0 - Project Initialization (2024-12-24)
- [x] `[USER]` Initial project setup - Done 2024-12-24
- [x] `[CLAUDE]` Draft full manuscript - Done 2024-12-24

### Phase 2 - Initial Drafting (2024-12-24)
- [x] `[CLAUDE]` Write Publisher's Note - Done 2024-12-24
- [x] `[CLAUDE]` Write Author's Preface - Done 2024-12-24
- [x] `[CLAUDE]` Write Michelle Obama Foreword - Done 2024-12-24
- [x] `[CLAUDE]` Write Chapter 1: Genesis of Greatness - Done 2024-12-24
- [x] `[CLAUDE]` Write Chapter 2: Manhattan Conquest - Done 2024-12-24
- [x] `[CLAUDE]` Write Chapter 3: Reality Era - Done 2024-12-24
- [x] `[CLAUDE]` Write Chapter 4: Political Paradox Pt 1 - Done 2024-12-24
- [x] `[CLAUDE]` Write Chapter 5: Political Paradox Pt 2 - Done 2024-12-24
- [x] `[CLAUDE]` Write Chapter 6: The Restoration - Done 2024-12-24
- [x] `[CLAUDE]` Write Hall of Mirrors - Done 2024-12-24
- [x] `[CLAUDE]` Write Afterword & Acknowledgments - Done 2024-12-24

### Phase 4 - Persona Review (2024-12-25)
- [x] `[GEMINI]` Generate initial persona reviews - Done 2024-12-25
- [x] `[GEMINI]` Generate additional persona reviews - Done 2024-12-25
- [x] `[GEMINI]` Generate internal feedback reviews - Done 2024-12-25

### Phase 5 - Editorial (2024-12-26)
- [x] `[CLAUDE]` De-polishing pass (remove AI formality) - Done 2024-12-26
- [x] `[USER]` Generate draft PDF - Done 2024-12-27

### Workflow Standardization (2026-01-06)
- [x] `[USER]` Create new directory structure - Done 2026-01-06
- [x] `[CLAUDE]` Update GEMINI.md to template format - Done 2026-01-06
- [x] `[CLAUDE]` Update CLAUDE.md to template format - Done 2026-01-06
- [x] `[CLAUDE]` Restructure TODO.md - Done 2026-01-06

---

## BLOCKING ISSUES

*None currently*

---

## DECISIONS NEEDED

1. **Word Count Target:**
   - Current: ~14,000 words
   - Option A: Cut to 8,000-10,000 (lean satire pamphlet)
   - Option B: Keep 12,000-15,000 (short book)
   - **Status:** Awaiting user decision

2. **Chapter Structure:**
   - Chapter 4 currently covers 2015-2019
   - Chapter 5 currently covers 2019-2024
   - Option: Split differently for pacing?
   - **Status:** Pending Gemini review recommendation

---

## NOTES

- Draft PDF exists at: `The_Definitive_Fictional_Lieography_FINAL.pdf`
- Original reviews preserved in: `PERSONA_REVIEWS.md`, `ADDITIONAL_PERSONA_REVIEWS.md`, `INTERNAL_FEEDBACK_REVIEWS.md`
- Voice guidelines detailed in: `CLAUDE.md` Section 2
- Master outline in: `MANUSCRIPT_PLAN.md`
