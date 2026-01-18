# Quality Gates - Trump Lieography

## Phase-End Quality Gates

### End of Phase 2 (Initial Drafting)
- [ ] All chapters drafted
- [ ] Word count within 20% of target
- [ ] Voice consistent throughout
- [ ] Front and back matter complete

### End of Phase 3 (Technical Review)
- [ ] All factual claims verified against FACTS_SHEET.md
- [ ] No accidental defamation
- [ ] Timeline consistency checked
- [ ] Real names/dates accurate

### End of Phase 4 (Persona Review)
- [ ] All 6 personas provided feedback
- [ ] Claude responded to each item (AGREED/DISAGREED)
- [ ] Agreed items implemented
- [ ] Disputes resolved or escalated

### End of Phase 5 (Editorial) - CURRENT
- [ ] Vale lint: 0 errors (if configured)
- [ ] De-AI-ify: 0 banned words
- [ ] Passive voice: < 5% of sentences
- [ ] Average sentence length: < 12 words
- [ ] Superlatives: 3+ per page
- [ ] "People are saying" variants: 1+ per major section
- [ ] All names/dates/references verified
- [ ] 0 typos
- [ ] Read-aloud test passed

### End of Phase 8 (Pre-Publication)
- [ ] PDF generates without errors
- [ ] ePub generates without errors
- [ ] Table of contents accurate
- [ ] Page breaks appropriate
- [ ] KDP metadata complete
- [ ] Both agents signed off
- [ ] User final approval

---

## Critical Errors (STOP and Fix)

These errors MUST be fixed before proceeding:

1. **Typo in title or chapter heading**
2. **Factual error that could be defamatory**
3. **Banned word in Trump voice sections**
4. **Broken cross-reference or link**
5. **Missing referenced content**
6. **Inconsistent terminology (same thing called different names)**
7. **Date/timeline contradiction**
8. **Legal red flag (potential libel, incitement)**

---

## Voice Quality Checklist

Run this checklist on every chapter:

### Sentence Structure
- [ ] 70%+ sentences under 10 words
- [ ] No sentences over 25 words
- [ ] Fragments used for emphasis
- [ ] No academic transition phrases

### Trump-isms
- [ ] At least 3 different superlatives per page
- [ ] "Tremendous" varied with alternatives
- [ ] At least 1 "people are saying" per section
- [ ] At least 1 third-person "Trump" reference per chapter
- [ ] All failures reframed as victories or persecution

### Satirical Distance
- [ ] Absurdity escalates through the book
- [ ] Straight-man elements preserved (Michelle, Publisher)
- [ ] "Clever-stupid" moments included
- [ ] Fiction clearly signaled in early pages

---

## De-AI-ify Verification

### Banned Word Search
Run grep for each of these. Result must be 0:
```
delve|tapestry|landscape|realm|testament|undeniable|invaluable|crucially|seamlessly|utilize|leverage|embark|facilitate|nuanced|multifaceted|pivotal|underscores|noteworthy
```

### Reduce-Use Word Check
These should appear rarely (< 3 per chapter):
```
however|therefore|moreover|furthermore|indeed|arguably|notably|importantly
```

### Passive Voice Check
Search for passive constructions. Convert to active Trump voice:
- "was done" → "I did it"
- "was built" → "I built it"
- "were fired" → "I fired them"

---

## Sign-Off Template

```markdown
## Publication Sign-Off

**Gemini Sign-Off:**
[x] GEMINI Final QA Pass — [Date]
    All factual claims verified. No legal red flags.
    De-AI-ify compliance verified.
    Signature: Gemini

**Claude Sign-Off:**
[x] CLAUDE Final Editorial Pass — [Date]
    All prose polished. Voice consistent.
    Quality gates passed.
    Signature: Claude

**User Sign-Off:**
[x] USER Final Approval — [Date]
    Reviewed all phases. Authorizing publication.
    Signature: [User]
```
