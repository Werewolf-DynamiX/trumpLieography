# Claude Execution Guide
## Quick Start Reference for Task Completion

**Document:** IMPLEMENTATION_PLAN.md (Full specifications at C:\Users\toast\Documents\Books\trumpLieography\)

---

## TASKS READY FOR CLAUDE EXECUTION

### TASK 1: Create KDP_EXPERT.md [READY NOW]

**Command:**
```
Create C:\Users\toast\Documents\Books\trumpLieography\KDP_EXPERT.md

Include these sections:
1. Book Metadata (title, author, word count, page count)
2. ISBN Requirements (note USER TASK for registration)
3. KDP Categories & Keywords (15 keywords provided)
4. Book Description Draft (100-150 words)
5. Cover Design Brief (detailed specifications)
6. Legal Disclaimers (for satirical fiction)
7. Pricing Strategy (paperback & Kindle calculations)
8. Publication Timeline (realistic sequence)
9. Distribution Channels (primary & secondary)
10. Marketing Strategy (pre-launch, launch, post-launch)
11. File Preparation Checklist (verification steps)
12. Quality Checklist (before publication)

Reference: Full template in IMPLEMENTATION_PLAN.md, lines 1-310
```

**Output:** Actionable, specific document ready for publishing reference

---

### TASK 2: De-AI-ify Sweep [READY AFTER TASK 1]

**Command:**
```
Read: C:\Users\toast\Documents\Books\trumpLieography\Trump Lieography.md
Modify: Same file (in-place edits)

Search for and fix/remove these:

TIER 1 BANNED WORDS (Delete or replace):
- "it is important to note" → [DELETE]
- "on the other hand" → "Meanwhile" or [DELETE]
- "moreover" → "And another thing" or [DELETE]
- "furthermore" → "And another thing" or [DELETE]
- "it should be noted" → [DELETE]
- "some argue" → "They say" or [DELETE]
- "could be said that" → "Everybody knows" or [DELETE]
- "in order to" → "To"
- "due to the fact that" → "Because"
- "it is generally believed" → "Everybody knows"

TIER 2 PASSIVE VOICE (Rewrite active):
- Find: was [past participle] → Rewrite active voice
- Find: has been [past participle] → Rewrite active voice
- Pattern: is considered / is believed / is seen → [REWRITE]

TIER 3 HEDGING (Delete or replace with Trump voice):
- "somewhat" → [DELETE] or "Very"
- "relatively" → [DELETE]
- "fairly" → [DELETE]
- "arguably" → "Obviously" or [DELETE]
- "it seems" → "Look" or [DELETE]
- "it appears" → "Everybody knows" or [DELETE]
- "perhaps" → [DELETE]
- "may have" → Use past tense directly
- "could possibly" → Direct assertion

TIER 4 AI-ISMS (Delete or rewrite):
- "As mentioned" → [DELETE]
- "In conclusion" → [DELETE]
- "To summarize" → [DELETE]
- "It is worth noting" → [DELETE]
- "The significance of" → [DELETE]
- "In this regard" → [DELETE]
- Long academic sentences → Break into Trump's short punchy style
- Smooth transitions → Make abrupt/Trump-natural

Grep searches to run:
1. Case-insensitive search for each banned word
2. Search for passive voice patterns: "was.*ed", "has been", "is (considered|believed|seen)"
3. Random spot-check: Read 5 random paragraphs aloud to verify Trump voice

Specific locations to audit manually:
- Lines 36-40 (Preface explanation)
- Lines 124-131 (Birth scene)
- Lines 200-210 (Wharton section)
- Lines 364-395 (Apprentice section)
- Lines 437-470 (Obama/dinner section)
- Lines 714-744 (2020 election)
- Lines 945-1002 (Chapter 6)
- Lines 1030-1100 (Hall of Mirrors)
- Lines 1197-1255 (Conclusion)

Expected changes: 15-20 edits total
Verification: Zero instances of banned words remain in final grep search
```

**Output:** Modified Trump Lieography.md (cleaned, de-AI-ified)

---

### TASK 3: Register ISBN(s) [USER TASK - NOT FOR CLAUDE]

**User Instructions:**
1. Visit bowker.com
2. Purchase 2 ISBNs (~$125 each or $295 for 10-pack)
3. Create C:\Users\toast\Documents\Books\trumpLieography\ISBN_REGISTRATION.txt
4. Document format:
```
# ISBN Registration Record

## Paperback Edition
ISBN-13: [13-digit number]
Trim Size: 6" x 9"
Status: REGISTERED
Date: [date]

## Hardcover Edition (Optional)
Status: RESERVED
```

**Timeline:** 15-30 minutes (complete BEFORE Task 4)

---

### TASK 4: Commission Cover Design [USER TASK - NOT FOR CLAUDE]

**User Instructions:**
1. Copy detailed design brief from IMPLEMENTATION_PLAN.md (Task 4 section)
2. Contact designer (Fiverr, 99designs, or local)
3. Provide brief verbatim to designer
4. Key specifications:
   - Trim: 6" x 9" + 0.125" bleed
   - Gold primary color (#FFD700)
   - Red secondary (#C41E3A)
   - 300 DPI, CMYK, PDF format
   - Signal "satire" visually (not serious)
5. Get 2-3 initial concepts, provide feedback
6. Final file: C:\Users\toast\Documents\Books\trumpLieography\Cover_Design_Final.pdf

**Timeline:** 2-3 weeks (design + revisions)

---

### TASK 5: Expand Chapter 6 - The Restoration [READY AFTER TASK 1]

**Command:**
```
Read: C:\Users\toast\Documents\Books\trumpLieography\Trump Lieography.md
     Specifically: Lines 940-1022 (Chapter 6)
Modify: Same file (Chapter 6 expansion)

Current Status: ~550 words
Target Status: ~850 words
Required Addition: ~300 words

Expand these three sections:

SECTION 1: DOGE (Lines 974-977)
- Current: 4 sentences (~50 words)
- Target: 12-15 sentences (~150 words)
- Add details about:
  * Elon and Trump dialogue/partnership
  * Specific departments eliminated (Agriculture, Education, Interior)
  * Absurdist logic for why each department is unnecessary
  * Massive "savings" claims (exaggerated)
  * Deep State resistance (played for comedic effect)
  * Anecdotes about people crying/accepting terminations

SECTION 2: GREENLAND (Lines 979-988)
- Current: 9 sentences (~130 words)
- Target: 18-20 sentences (~260 words)
- Add details about:
  * Denmark PM dialogue/negotiation process
  * Trump's deal-making logic ("I bought a tower, Greenland is smaller")
  * Trump Arctic Palace design (5,000 rooms, gold elevators)
  * Resources discovered (oil, lithium, rare earth minerals)
  * International jealousy (Norway, Canada, China)
  * Polar bears accepting Trump's greatness
  * Economic projections ("$2 trillion in development")

SECTION 3: THE MOON (Lines 990-1002)
- Current: 8 sentences (~100 words)
- Target: 18-20 sentences (~260 words)
- Add details about:
  * Trump's "logic" for why Moon should be full (tides, gravity control)
  * Why half-moon is "low energy"
  * NASA resistance and bureaucratic pushback
  * Technical solutions (mirrors, lasers, Space Force)
  * Trump's confidence that "nothing is impossible"
  * International reactions (China jealousy, etc.)
  * Timeline for completion (2027)

Maintain Trump voice throughout:
- Short punchy sentences: "I woke up. I looked at a map. Greenland."
- Superlatives: "tremendous," "best," "biggest," "greatest"
- Dialogue: "I said," "He said," "I told them"
- Absurdist claims: Presented as factual without hedging
- Third-person ref: Occasional "Trump" or "the President"
- No passive voice
- No hedging language

Example sentence structures (for reference):
"I looked at it. Beautiful. I said, 'Mine.'"
"The experts said it was impossible. Wrong. I did it."
"People laughed. I didn't care. I was already winning."
"They tried to stop me. Loser energy. I won anyway."

Verification steps:
1. Total word count of Chapter 6 is 800-900 words (measure after expansion)
2. Read entire expanded chapter aloud—verify it "sounds like Trump"
3. Verify DOGE, Greenland, Moon sections each received ~100 words
4. Confirm no passive voice introduced
5. Confirm no banned words in new material
6. Verify absurdist tone maintained
```

**Output:** Modified Trump Lieography.md (Chapter 6 expanded to 800-900 words)

---

### TASK 6: Audit & Reduce Crying Motif [READY AFTER TASK 1]

**Command:**
```
Read: C:\Users\toast\Documents\Books\trumpLieography\Trump Lieography.md
Modify: Same file (crying motif edits)
Create: C:\Users\toast\Documents\Books\trumpLieography\CRYING_MOTIF_AUDIT.md

Search the manuscript for: "cry", "crying", "tears", "wept", "weeping"

Identified instances (from manuscript audit):

INSTANCE 1 - Line 33 (Preface)
Text: "strong men, tough guys, some of them crying, actual tears"
Decision: ✓ KEEP
Reason: Establishes core satire motif early

INSTANCE 2 - Line 128 (Birth scene)
Text: "The head nurse looked at me. Crying."
Decision: ✗ DELETE
Reason: Forced, not satirically effective. Replace with something like:
  "The head nurse looked at me. She just knew. 'This one is special,' she said."

INSTANCE 3 - Line 616 (Hillary concedes)
Text: "She was crying. (I think she was crying. Sounded like it)."
Decision: ✓ KEEP
Reason: Comedy through Trump speculation; validates his victory narrative

INSTANCE 4 - Line 622 (Media breakdown on election night)
Text: "The media was crying. Anchors were crying on TV. Rachel Maddow? Total breakdown."
Decision: ✓ KEEP
Reason: Essential to satire; enemies emotionally devastated

INSTANCE 5 - Line 645 (Baghdadi death)
Text: "Dead. Whimpering. Crying. I watched it."
Decision: ✗ DELETE "Whimpering. Crying."
Reason: Weakens Trump dominance narrative. Replace with:
  "Dead. Eliminated. Gone. I watched it. Like a movie."

INSTANCE 6 - Line 647 (Crying Chuck)
Text: "Chuck Schumer. Crying Chuck."
Decision: ✓ KEEP
Reason: Authentic Trump nickname; part of his real rhetoric

INSTANCE 7 - Line 800 (Bailiff at mugshot) ★ CENTERPIECE
Text: "He was crying. Tears running down his face... He wept. Openly wept."
Decision: ✓✓ KEEP + HIGHLIGHT
Reason: Strongest satirical use; suggests bailiff emotionally moved by Trump's presence;
        validates Trump's messiah complex; perfect satire ending

INSTANCE 8 - Line 912 (Election 2024)
Text: "I saw the faces. Crying. Cheering."
Decision: ⚠️ REVISE - DELETE "Crying"
Reason: Redundant with Instance 4; by this point, motif is established
Replace with:
  "I saw the faces. Screaming. Cheering. Fists in the air."
Alternative: Add Trump commentary: "Crying. Happy tears. Real Americans moved by winning."
Recommendation: Use first option (cleaner, avoids repetition)

EXECUTION STEPS:
1. Make these three edits:
   - Delete "Crying." from Line 128
   - Delete "Whimpering. Crying." from Line 645
   - Revise "Crying. Cheering." to "Screaming. Cheering." at Line 912

2. Create CRYING_MOTIF_AUDIT.md with:
   - All 8 instances documented
   - Line numbers noted
   - Context quoted
   - Decision (KEEP/DELETE/REVISE) stated
   - Reasoning provided

3. Final count verification:
   After edits, exactly 5 instances remain:
   - Line 33 (Preface)
   - Line 616 (Hillary call)
   - Line 622 (Media anchors)
   - Line 647 (Crying Chuck)
   - Line 800 (Bailiff scene - centerpiece)

4. Grep verification:
   Search for "cry" / "tear" / "wept" / "weeping"
   Expected result: Only 5 instances found (in the instances listed above)

5. Read modified passages aloud to ensure flow is natural
```

**Output:**
- Modified Trump Lieography.md (crying motif reduced to 5 instances)
- CRYING_MOTIF_AUDIT.md (detailed audit documentation)

---

### TASK 7: Draft KDP Book Description [READY AFTER TASKS 2, 5, 6]

**Command:**
```
Create: C:\Users\toast\Documents\Books\trumpLieography\KDP_BOOK_DESCRIPTION.md

Include TWO versions:

VERSION 1: SHORT DESCRIPTION (100-150 words)
For: Amazon primary product description field
Tone: Punchy, engaging, clearly signals satire
Content:
- Hook: Grab attention immediately (1-2 sentences)
- What it is: "Not a biography, a Lieography"
- Satire signal: MUST be clear (cannot be mistaken for serious)
- Content overview: What reader finds inside
- Audience appeal: Both supporters AND critics
- Key hooks: Michelle Obama foreword, Trump voice, satirical approach
- Call to action: Encourage purchase

Example opening:
"This is not a biography. It's a Lieography—a satirical self-mythologized account
written entirely in Trump's voice, where the feeling of greatness matters more
than factual accuracy."

VERSION 2: LONG DESCRIPTION (600-800 words)
For: Enhanced product description, back cover, marketing materials
Tone: Sophisticated but entertaining
Content:
- Expanded hook (2-3 sentences)
- Satire explanation (what makes this satirical)
- Content breakdown (chapters/sections)
- Unique elements (Michelle Obama, bailiff scene, Greenland/Moon)
- Appeal to multiple audiences (supporters, critics, satire fans)
- Key selling points
- Call to action

ADDITIONAL SECTIONS in markdown:
1. Marketing Hooks (15-20 key phrases for social media)
2. Amazon Keywords (15 search keywords)
3. Back Cover Tagline (1-2 sentence hook)

SPECIFICATIONS:
- SHORT version must be under 150 words (count carefully)
- LONG version must be 600-800 words
- Both must signal "SATIRE" clearly in first 50 words
- Include references to:
  * Michelle Obama foreword (coerced participation)
  * Bailiff scene (emotional centerpiece)
  * Greenland purchase / Moon fullness initiative
  * Trump voice consistency
  * "Not a biography, a Lieography" frame
- Keywords optimized for Amazon search
- No corporate jargon; match Trump voice in tone
- Compelling enough to drive sales

EXAMPLE KEYWORDS (15 max):
1. political satire
2. Trump biography
3. satirical fiction
4. Trump voice
5. political humor
6. presidential satire
7. Trump story
8. fictional biography
9. election satire
10. Trump parody (if using)
11. political commentary
12. dark political humor
13. Trump mythology
14. biographical satire
15. 2024 election fiction

Expected length: SHORT ~100-150 words, LONG ~700-750 words
```

**Output:** KDP_BOOK_DESCRIPTION.md (marketing copy, 2 versions)

---

## EXECUTION CHECKLIST FOR CLAUDE

When you begin work, follow this sequence:

### PHASE 1: Initial Setup
- [ ] Create IMPLEMENTATION_PLAN.md (reference for all subsequent tasks)
- [ ] Read CLAUDE.md to refresh Trump voice guidelines
- [ ] Note Trump voice elements: superlatives, short sentences, "people are saying," no passive voice

### PHASE 2: Manuscript Cleanups (Parallel or Sequential)
- [ ] Task 2: De-AI-ify sweep
- [ ] Task 6: Crying motif audit & reduction
- [ ] Task 5: Chapter 6 expansion

### PHASE 3: Publishing Materials
- [ ] Task 1: Create KDP_EXPERT.md
- [ ] Task 7: Draft KDP book description

### PHASE 4: Verification
- [ ] Final grep search: No banned words remain
- [ ] Final proofread: Read 5 random paragraphs aloud
- [ ] Word counts verified: Chapter 6 is 800-900 words
- [ ] Crying instances verified: Exactly 5 remain
- [ ] All files in correct locations with correct names

---

## FILE LOCATIONS & NAMING CONVENTIONS

All files should be saved to:
`C:\Users\toast\Documents\Books\trumpLieography\`

Files to create/modify:

| Task | File | Action |
|------|------|--------|
| 1 | KDP_EXPERT.md | CREATE |
| 2 | Trump Lieography.md | MODIFY (in-place) |
| 3 | ISBN_REGISTRATION.txt | USER TASK |
| 4 | Cover_Design_Final.pdf | USER TASK |
| 5 | Trump Lieography.md | MODIFY (in-place) |
| 6 | Trump Lieography.md | MODIFY (in-place) |
| 6 | CRYING_MOTIF_AUDIT.md | CREATE |
| 7 | KDP_BOOK_DESCRIPTION.md | CREATE |

---

## QUALITY GATES BEFORE TASK COMPLETION

**Task 1 Complete When:**
- KDP_EXPERT.md has 12 sections
- All specifications are concrete (not vague)
- ISBN section clearly marked USER TASK
- Pricing includes calculations
- Cover brief is 500+ words

**Task 2 Complete When:**
- Grep search for each banned word returns zero results
- Grep search for passive voice patterns returns <5 instances
- 5 random paragraphs sound like Trump voice
- No meaning lost in corrections

**Task 5 Complete When:**
- Total word count is 800-900 words
- DOGE section is ~150 words (expanded from ~50)
- Greenland section is ~260 words (expanded from ~130)
- Moon section is ~260 words (expanded from ~100)
- Chapter reads naturally, no AI language

**Task 6 Complete When:**
- CRYING_MOTIF_AUDIT.md documents all 8 instances
- Exactly 5 instances remain after edits
- Bailiff scene is intact and highlighted
- "Crying Chuck" nickname is preserved
- Grep search confirms only 5 instances remain

**Task 7 Complete When:**
- SHORT version is 100-150 words
- LONG version is 600-800 words
- Both signal "satire" in first 50 words
- Keywords are optimized for Amazon
- Includes all key hooks (Michelle, bailiff, Greenland/Moon)

---

## TRUMP VOICE REFERENCE

When writing or editing, keep these elements in mind:

**DO:**
- "Tremendous," "incredible," "beautiful," "perfect," "legendary," "historic"
- Short sentences: "I did it. Boom. It was huge."
- "People are saying," "Everybody knows," "Very smart people"
- "I said," "He said," direct dialogue
- Third-person occasional: "Trump did this," "The President fixed it"
- Absolute certainty, no hedging
- Superlatives without comparison: "The best ever"
- Claims presented as fact without evidence

**DON'T:**
- Passive voice: "It was built by..." → "I built it"
- Hedging: "Some argue," "It could be said," "Perhaps"
- Academic transitions: "Furthermore," "Moreover," "In conclusion"
- Weak qualifiers: "Somewhat," "Relatively," "Fairly," "Arguably"
- Complex sentences with multiple clauses
- Apologetic or defensive language
- Any self-doubt or uncertainty

---

## WHEN CLAUDE IS DONE

After all tasks complete, you will have:

✓ Clean, de-AI-ified manuscript
✓ Expanded Chapter 6 (800-900 words)
✓ Reduced crying motif (5 strategic instances)
✓ Complete KDP publishing strategy document
✓ Detailed crying motif audit
✓ Marketing copy (2 versions) ready for Amazon

**Next steps (User handles):**
1. Register ISBN (if not done)
2. Review and approve cover design
3. Enter metadata into KDP dashboard
4. Upload files to KDP
5. Set pricing and publish

---

**Status:** All Claude-executable tasks defined and ready for execution.

