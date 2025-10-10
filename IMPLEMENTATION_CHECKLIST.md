# Flocode Python Intro - Implementation Checklist

**Created:** October 10, 2025
**Purpose:** Actionable checklist for fixing issues identified in editorial review

---

## Priority 1: Critical Fixes (Must Complete Before Publishing)

### 1.1 Fix Internal Navigation Links

**Issue:** All navigation blocks use old Notion URL format with hash IDs

**Files to Update:** All 7 markdown files

- [ ] **README.md** (Lines 10-18)
  - [ ] Replace `[01 - Intro](01%20-%20Intro%202376414bbea981a09924ffb3b9469e3a.md)` with `[01 - Intro](01%20-%20Intro.md)`
  - [ ] Replace `[02 - Python in Engineering](02%20-%20Python%20in%20Engineering%202376414bbea981afb1a2ed9411175715.md)` with `[02 - Python in Engineering](02%20-%20Python%20in%20Engineering.md)`
  - [ ] Replace `[03 - Essence of Programming](03%20-%20Essence%20of%20Programming%202376414bbea9817b9d23c1d80012b1b2.md)` with `[03 - Essence of Programming](03%20-%20Essence%20of%20Programming.md)`
  - [ ] Replace `[04 - The Community](04%20-%20The%20Community%202376414bbea98131b379efbd645bfe0b.md)` with `[04 - The Community](04%20-%20The%20Community.md)`
  - [ ] Replace `[05 - The Path](05%20-%20The%20Path%202376414bbea981ea9923d4aa29287ede.md)` with `[05 - The Path](05%20-%20The%20Path.md)`

- [ ] **01 - Intro.md** (Lines 5-13)
  - [ ] Fix all 5 navigation links using pattern above

- [ ] **02 - Python in Engineering.md** (Lines 5-13)
  - [ ] Fix all 5 navigation links using pattern above

- [ ] **03 - Essence of Programming.md** (Lines 5-13)
  - [ ] Fix all 5 navigation links using pattern above

- [ ] **04 - The Community.md** (Lines 5-13)
  - [ ] Fix all 5 navigation links using pattern above

- [ ] **05 - The Path.md** (Lines 5-9)
  - [ ] Fix all 5 navigation links using pattern above
  - [ ] Note: This file uses list format instead of bold "Modules" heading

### 1.2 Fix Virtual Environments Cheat Sheet Critical Errors

- [ ] **Line 69: Fix broken shell installation command**
  - Current: `curl -LsSf [https://astral.sh/uv/install.sh|sh](https://astral.sh/uv/install.sh|sh) | sh`
  - Should be: `curl -LsSf https://astral.sh/uv/install.sh | sh`
  - Issue: Pipe character incorrectly included in markdown link

- [ ] **Line 123: Fix invalid main.py link**
  - Current: `uv run python [main.py](http://main.py)`
  - Should be: `uv run python main.py`
  - Issue: main.py is a filename, not a URL

- [ ] **Lines 230-232: Update or remove broken Astral uv documentation links**
  - [ ] Line 230: `https://docs.astral.sh/uv/getting-started/install-python/` - returns 404
  - [ ] Line 231: `https://docs.astral.sh/uv/guides/locking/` - returns 404
  - [ ] Line 232: `https://docs.astral.sh/uv/guides/building/` - returns 404
  - **Action:** Visit https://docs.astral.sh/uv/ and find updated URLs or remove these references

### 1.3 Clean Up Missing File References

- [ ] **README.md - Line 26: Recommended Reading List**
  - Current: `[Flocode's Recommended Reading List](Flocode%E2%80%99s%20Recommended%20Reading%20List%202376414bbea981e1a629c704c4e9ec91.csv)`
  - **Decision needed:** Either provide the CSV file or remove this link
  - [ ] Option A: Add CSV file to repository
  - [ ] Option B: Remove this line

- [ ] **README.md - Line 28: Python Libraries Link**
  - Current: `[Python Libraries for Civil/Structural Engineers](https://www.notion.so/2376414bbea981d98f4adf12253b8b80?pvs=21)`
  - **Decision needed:** Keep Notion link, replace with GitHub version, or remove
  - [ ] Option A: Keep if Notion page is public
  - [ ] Option B: Create markdown version in repo
  - [ ] Option C: Remove this link

- [ ] **README.md - Line 32: Coding Tools Link**
  - Current: `[Coding Tools](Coding%20Tools%202376414bbea981c69032fcc52d0c43bd.md)`
  - **Decision needed:** Either provide the file or remove this link
  - [ ] Option A: Add Coding Tools.md to repository
  - [ ] Option B: Remove this line

---

## Priority 2: Quality Improvements (Should Fix)

### 2.1 Remove Notion Artifacts

- [ ] **README.md**
  - [ ] Line 70: Remove "On this page" text
  - [ ] Lines 36-39: Remove "Control Panel 🎛" section and horizontal rules

- [ ] **01 - Intro.md**
  - [ ] Line 15: Remove "On this page" text
  - [ ] Line 78: Complete or remove incomplete "Next" section

- [ ] **02 - Python in Engineering.md**
  - [ ] Line 15: Remove "On this page" text
  - [ ] Line 126: Add next module link or remove incomplete footer

- [ ] **03 - Essence of Programming.md**
  - [ ] Line 15: Remove "On this page" text

- [ ] **04 - The Community.md**
  - [ ] Line 15: Remove "On this page" text
  - [ ] Lines 17-20: Reformat Notion aside block to markdown blockquote:
    ```markdown
    > The Flocode community is a dedicated platform for engineers worldwide learning Python. It encourages collaborative learning, offers engineering-centric resources, mentorship, and evolves based on community feedback, fostering inclusivity, respect, and problem-solving to enhance professional growth.
    ```

- [ ] **05 - The Path.md**
  - [ ] No "On this page" artifacts (clean ✓)

- [ ] **Virtual Environments Cheat Sheet.md**
  - [ ] Lines 5-10: Reformat Notion aside block to standard blockquote
  - [ ] Lines 180, 191+: Replace all HTML `<code>` tags with markdown backticks

### 2.2 Update HTTP to HTTPS Links

- [ ] **README.md - Line 47**
  - Current: `[Flocode Newsletter](http://flocode.substack.com)`
  - Update to: `[Flocode Newsletter](https://flocode.substack.com)`

- [ ] **04 - The Community.md - Line 77**
  - Current: `[flocode.dev](http://flocode.dev)`
  - Update to: `[flocode.dev](https://flocode.dev)`

- [ ] **05 - The Path.md - Line 103**
  - Current: `[flocode.dev](http://flocode.dev/)`
  - Update to: `[flocode.dev](https://flocode.dev)`

- [ ] **05 - The Path.md - Line 105**
  - Current: `[http://flocode.substack.com/](http://flocode.substack.com/)`
  - Update to: `[https://flocode.substack.com/](https://flocode.substack.com)`

### 2.3 Fix Typos and Minor Issues

- [ ] **README.md - Line 5**
  - Current: "Python's applications" (extra space before "applications")
  - Fix spacing

- [ ] **README.md - Line 6**
  - Current: "This is for those are completely new"
  - Fix to: "This is for those who are completely new"

- [ ] **01 - Intro.md - Line 28**
  - Current: "the includes aspects"
  - Fix to: "this includes aspects"

- [ ] **03 - Essence of Programming.md - Line 19**
  - Current: "FlowCode Intro to Python Series"
  - Fix to: "Flocode Intro to Python Series"

- [ ] **03 - Essence of Programming.md - Line 112**
  - Current: "releva nt parameters" (extra space)
  - Fix to: "relevant parameters"

### 2.4 Handle Missing Images

**Decision needed for each:** Add image, create placeholder, or remove reference

- [ ] **02 - Python in Engineering.md - Line 85**
  - Reference: `![tools change_principles dont.png](tools_change_principles_dont.png)`
  - [ ] Option A: Add image to assets/ and update path to `assets/tools_change_principles_dont.png`
  - [ ] Option B: Remove image reference and adjust text
  - [ ] Option C: Create placeholder image

- [ ] **03 - Essence of Programming.md - Line 118**
  - Reference: `![Untitled](Untitled.png)` (beam deflection diagram)
  - [ ] Option A: Add diagram to assets/ and update path
  - [ ] Option B: Remove image and adjust text ("Say you're calculating the deflection...")
  - [ ] Option C: Create simple beam diagram placeholder

- [ ] **03 - Essence of Programming.md - Line 215**
  - Reference: `![Untitled](Untitled%201.png)` (PEMDAS/BODMAS image)
  - [ ] Option A: Add PEMDAS image to assets/ and update path
  - [ ] Option B: Remove image (text "PEMDAS/BODMAS" is sufficient)
  - [ ] Option C: Create simple order of operations graphic

---

## Priority 3: Enhancements (Nice to Have)

### 3.1 README Restructuring (Optional)

Consider restructuring README.md to follow GitHub conventions:

- [ ] Add project badges (if applicable)
- [ ] Add clear "Getting Started" section
- [ ] Restructure "Prerequisites" section position
- [ ] Add "Contributing" section (if accepting contributions)
- [ ] Add "License" section
- [ ] Consider table of contents for easier navigation

### 3.2 Review Monetization Language (Optional)

- [ ] **05 - The Path.md - Line 81**
  - Current: "Python for Engineers: Intro (Free)"
  - [ ] Decision: Keep "(Free)" label or remove to avoid implying other courses are paid
  - [ ] Alternative: Remove pricing language entirely
  - [ ] Alternative: Add clarification about curriculum structure

### 3.3 Enhance Virtual Environments Cheat Sheet (Optional)

- [ ] Add note about uv documentation URL changes
- [ ] Consider adding troubleshooting section
- [ ] Add Windows-specific tips if needed

### 3.4 Add Navigation Footer to All Modules (Optional)

Currently inconsistent "Next" sections. Consider adding:

- [ ] 01 - Intro.md: Add proper "Next: Python in Engineering →" link
- [ ] 02 - Python in Engineering.md: Add "← Previous | Next: Essence of Programming →"
- [ ] 03 - Essence of Programming.md: Add navigation footer
- [ ] 04 - The Community.md: Add navigation footer
- [ ] 05 - The Path.md: Already has good closing, consider "← Previous" link

---

## Automated Linting (Recommended)

Consider running automated markdown linting tools:

- [ ] Install markdownlint: `npm install -g markdownlint-cli`
- [ ] Run linter: `markdownlint *.md`
- [ ] Fix automated issues:
  - [ ] Trailing whitespace
  - [ ] Multiple consecutive blank lines
  - [ ] Inconsistent heading hierarchy
  - [ ] Line length issues

---

## Pre-Publish Verification Checklist

Before publishing to GitHub:

### Links
- [ ] All internal navigation links work
- [ ] All external links verified (run link checker)
- [ ] All asset links work (images load correctly)

### Formatting
- [ ] No Notion artifacts remain
- [ ] Consistent markdown formatting
- [ ] Code blocks properly formatted
- [ ] Tables render correctly

### Content
- [ ] Brand voice consistent (no "easy", "just", hype terms)
- [ ] Technical accuracy verified
- [ ] Course positioning clear (pre-Essentials intro)
- [ ] No inappropriate monetization language

### Assets
- [ ] All referenced images exist
- [ ] Image paths correct (use relative paths)
- [ ] Assets directory properly structured

### Testing
- [ ] Clone repo fresh and test all links
- [ ] Render markdown in GitHub to verify formatting
- [ ] Test on mobile view (if applicable)
- [ ] Have another person review

---

## Success Criteria Verification

Final check against original success criteria:

- [ ] ✓ All markdown passes linting (run markdownlint)
- [ ] ✓ Consistent Flocode brand voice throughout
- [ ] ✓ All links functional (verify with link checker)
- [ ] ✓ No paid course references (or appropriate soft mentions)
- [ ] ✓ Newsletter appropriately promoted (not pushy)
- [ ] ✓ Clear positioning as pre-Essentials primer
- [ ] ✓ Professional, encouraging tone for beginners

---

## Estimated Time to Complete

| Priority | Tasks | Estimated Time |
|----------|-------|----------------|
| Priority 1 (Critical) | 1.1 - 1.3 | 2-3 hours |
| Priority 2 (Quality) | 2.1 - 2.4 | 1-2 hours |
| Priority 3 (Enhancements) | 3.1 - 3.4 | 1-2 hours |
| **Total** | | **4-7 hours** |

---

## Quick Reference: File-by-File Task Count

| File | Priority 1 | Priority 2 | Priority 3 | Total |
|------|-----------|-----------|-----------|-------|
| README.md | 5 links + 3 refs | 5 items | 1 item | 14 |
| 01 - Intro.md | 5 links | 3 items | 1 item | 9 |
| 02 - Python in Engineering.md | 5 links | 2 items + 1 image | 1 item | 9 |
| 03 - Essence of Programming.md | 5 links | 2 items + 2 images | 1 item | 10 |
| 04 - The Community.md | 5 links | 3 items | 1 item | 9 |
| 05 - The Path.md | 5 links | 2 items | 2 items | 9 |
| Virtual Envs Cheat Sheet.md | 5 links | 2 items | 1 item | 8 |

---

## Notes for Implementation

### Find & Replace Patterns

**Navigation Links (use with caution - verify after):**
```
Find: 01%20-%20Intro%202376414bbea981a09924ffb3b9469e3a.md
Replace: 01%20-%20Intro.md

Find: 02%20-%20Python%20in%20Engineering%202376414bbea981afb1a2ed9411175715.md
Replace: 02%20-%20Python%20in%20Engineering.md

Find: 03%20-%20Essence%20of%20Programming%202376414bbea9817b9d23c1d80012b1b2.md
Replace: 03%20-%20Essence%20of%20Programming.md

Find: 04%20-%20The%20Community%202376414bbea98131b379efbd645bfe0b.md
Replace: 04%20-%20The%20Community.md

Find: 05%20-%20The%20Path%202376414bbea981ea9923d4aa29287ede.md
Replace: 05%20-%20The%20Path.md
```

**HTTP to HTTPS:**
```
Find: http://flocode.substack.com
Replace: https://flocode.substack.com

Find: http://flocode.dev
Replace: https://flocode.dev
```

**Remove Notion Artifacts:**
```
Find: **On this page**
Replace: (delete)

Find: <code>
Replace: `

Find: </code>
Replace: `
```

---

## Questions to Resolve Before Publishing

1. **Missing Files:**
   - Do you want to include Recommended Reading List CSV?
   - Do you want to include Coding Tools.md?
   - Should Python Libraries link stay as Notion or be converted?

2. **Missing Images:**
   - Do you have source images for "tools change principles dont", beam diagram, and PEMDAS?
   - Should these be created, sourced, or references removed?

3. **Monetization:**
   - Is marking Intro as "(Free)" acceptable?
   - Does listing 5 course tiers imply monetization inappropriately?

4. **Navigation:**
   - Do you want consistent "Next/Previous" footers on all modules?
   - Current state is inconsistent

5. **README Structure:**
   - Keep current structure or restructure for GitHub conventions?

---

## Completion Sign-Off

When all tasks complete:

- [ ] All Priority 1 tasks completed
- [ ] All Priority 2 tasks completed
- [ ] Priority 3 tasks completed or deferred
- [ ] Pre-publish verification completed
- [ ] Success criteria verified
- [ ] Ready to push to GitHub

**Completed by:** _______________
**Date:** _______________
**Reviewed by:** _______________

---

**Document Version:** 1.0
**Last Updated:** October 10, 2025
