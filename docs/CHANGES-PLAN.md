# Changes Plan: Pareto Improvements for DEP Community Hub MVP

**Date:** 2026-04-23  
**Scope:** All 27 HTML files under `docs/`  
**Goal:** Make the MVP feel complete and functional with the highest-impact, lowest-effort changes

---

## Current State Summary

| Metric | Value |
|---|---|
| Total feature pages | 27 HTML files |
| Pages with JS interactivity | 25 (pathway/index.html, mentorship/index.html have none) |
| Feature pages linked from hub | 4 out of 27 |
| Sign-up form | Non-functional (shows `alert()` on submit) |
| Cross-module navigation | Only sql↔python↔excel chain; no "All Modules" overview |
| Footer consistency | All pages have footer, but missing LinkedIn link and social links vary |

---

## P0 — Navigation & Discoverability

### Change 1: Link all feature pages from the main hub roadmap

**File:** `docs/index.html`  
**Effort:** ~30 minutes  
**Impact:** Critical — currently 80% of content is undiscoverable from the landing page

**What to add:** In the Phase 3 accordion sections (Tier A, B, C), convert each feature name into a clickable link pointing to its corresponding HTML file. For features that don't have their own page, leave as text.

**Mapping table:**

| Feature | Score | File | Already built? |
|---|---|---|---|
| #7 Power BI Gap Closer | 8.8 | `/modules/power-bi-gap.html` | ✅ |
| #8 DAX Portfolio Project | 8.2 | `/modules/dax-portfolio.html` | ✅ |
| #9 AI Workflow Interview Prep | 8.2 | `/modules/ai-interview-prep.html` | ✅ |
| #10 Remote Mentorship Board | 8.2 | `mentorship/index.html` (partial) | ⚠️ |
| #11 DAX Micro-Lessons | 8.0 | `/modules/dax-micro.html` | ✅ |
| #12 Draw.io Templates | 8.0 | `/modules/drawio-templates.html` | ✅ |
| #13 GitHub Portfolio Showcase | 8.0 | (merged into git-guide) | — |
| #14 DAX Signal Gap Course | 8.0 | `/modules/dax-signal.html` | ✅ |
| #15 AI Study Workflow Guide | 7.8 | `/modules/ai-study-workflow.html` | ✅ |
| #16 Portfolio Builder Template | 7.8 | (not built) | ❌ |
| #17 Decision to Shift Framework | 7.8 | `/modules/decision-shift.html` | ✅ |
| #18 Hiring Pipeline Connector | 7.8 | `mentorship/hiring.html` | ✅ |
| #19 Creator Spotlight Platform | 7.8 | `/creator/spotlight.html` | ✅ |
| #20 YouTube Content Calendar | 7.8 | (not built) | ❌ |
| #21 Local to Cloud Bridge | 7.5 | `mentorship/index.html` (partial) | ⚠️ |
| #22 Cloud Deployment Bootcamp | 7.8 | `/modules/cloud-bootcamp.html` | ✅ |
| #23 Cloud Certification Guide | 7.8 | (not built) | ❌ |
| #24 Laptop-Only Projects | 7.5 | `/modules/laptop-projects.html` | ✅ |
| #25 Salary Band Tracker | 7.5 | (merged into fluency-map) | ⚠️ |
| #26 AI-Assisted Coding Toolkit | 7.5 | `/modules/ai-coding-toolkit.html` | ✅ |
| #27 Async Collaboration Tools | 7.5 | `/modules/async-tools.html` | ✅ |
| #28 Language/Cultural Bridge | 7.5 | `/modules/culture-bridge.html` | ✅ |
| #29 Free Credential Tracker | 7.0 | `/modules/credential-tracker.html` | ✅ |
| #30 Content Repurposing Toolkit | 7.0 | `/modules/content-repurpose.html` | ✅ |

**Implementation:** Add `href` to each feature name in the accordion. Use pattern: `<a href="/modules/power-bi-gap.html" class="text-dep-blue hover:text-dep-gold font-semibold text-sm">Power BI Gap Closer</a>` for built features, leave as plain text for unbuilt ones.

---

### Change 2: Add "All Modules" section to hub features area

**File:** `docs/index.html`  
**Effort:** ~15 minutes  
**Impact:** Critical — users landing on individual modules have no way to see the full catalog

**What to add:** Between the Phase 2 section and the How It Works section, insert a new "All Learning Modules" section with a responsive grid of all 18 module cards. Each card links to its page. Keep it compact (3-column grid on desktop).

**Content for each card:**
- Module name as title
- One-line description
- Badge showing phase (Phase 1/2/3)
- Link: "Read →"

**Modules list:** `sql-basics`, `python-fundamentals`, `excel-powerbi-intro`, `power-bi-gap`, `dax-portfolio`, `ai-interview-prep`, `dax-micro`, `drawio-templates`, `dax-signal`, `ai-study-workflow`, `decision-shift`, `cloud-bootcamp`, `laptop-projects`, `ai-coding-toolkit`, `async-tools`, `culture-bridge`, `credential-tracker`, `content-repurpose`

---

## P1 — Interactivity Gaps

### Change 3: Add JS interactivity to pathway/index.html

**File:** `docs/pathway/index.html`  
**Effort:** ~45 minutes  
**Impact:** High — this is a core Phase 1 feature page with zero interactivity

**What to add:**
- Convert each week block into a collapsible accordion (click to expand/collapse)
- Add "copy Discord link" button for each week's check-in thread
- Add a simple progress indicator at the top: "Week X of 8" with a mini progress bar that fills as you scroll through sections

**JS needed:** ~30 lines — reuse the accordion pattern already defined in index.html CSS (`.accordion-content`, `.accordion-chevron`) and add a new `toggleAccordion` function or reuse the one from index.html. Since it's a separate file, either inline the JS or copy the shared CSS classes.

---

### Change 4: Add JS interactivity to mentorship/index.html

**File:** `docs/mentorship/index.html`  
**Effort:** ~30 minutes  
**Impact:** High — second core Phase 1 feature page with zero interactivity

**What to add:**
- Add a topic filter input above the mentor cards: as user types "SQL", only mentors covering SQL topics remain visible
- Convert the "How It Works" 4-step grid into collapsible cards (click step to expand details)
- Add "copy Discord invite link" button

**JS needed:** ~25 lines — simple filter function on input event, plus accordion toggle.

---

### Change 5: Replace form alert with localStorage + success message

**File:** `docs/index.html`  
**Effort:** ~15 minutes  
**Impact:** High — removes jarring browser alert, makes CTA feel real

**What to change:**
- Replace `onsubmit="event.preventDefault(); alert('This is a prototype...');"` with:
  - `onsubmit="handleSubmit(event)"`
- Add JS function that:
  - Reads all form fields (name, email, role, selected checkboxes)
  - Saves to `localStorage.setItem('dep-cohort-signup', JSON.stringify(data))`
  - Replaces the form with a success message: "🎉 You're in! Check your inbox for a Discord invite and Week 1 materials."
  - Shows a subtle toast notification

**Success message HTML:**
```html
<div id="signup-success" class="hidden text-center py-8">
  <svg class="w-16 h-16 mx-auto mb-4 text-dep-gold" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M22 11.08V12a10 10 0 1 1-5.35-9.5"/><polyline points="22 4 12 14.01 9 11.01"/></svg>
  <h3 class="text-xl font-bold text-dep-blue mb-2">You're in! 🎉</h3>
  <p class="text-dep-slate">Check your inbox for a Discord invite and Week 1 materials within 24 hours.</p>
  <p class="text-xs text-dep-slate/60 mt-4">Saved locally — data won't persist across browsers.</p>
</div>
```

---

## P2 — Consistency & Polish

### Change 6: Add LinkedIn to all footers + standardize social links

**Files:** All 27 HTML files (or use a shared JS footer partial)  
**Effort:** ~30–60 minutes (30 min if using one JS partial, ~1 hr if editing each file)  
**Impact:** Medium — LinkedIn is critical for the target audience's career-shifting behavior

**Approach:** Use a single inline JS snippet at the bottom of `<body>` on every page that dynamically injects the footer. This way you only edit one location.

**Footer content (identical on all pages):**
```html
<footer id="dep-footer" class="bg-dep-blue py-8 border-t-2 border-dep-gold/30">
  <div class="max-w-[1120px] mx-auto px-4 sm:px-6 lg:px-8">
    <div class="flex flex-col md:flex-row items-center justify-between gap-4">
      <div class="text-center md:text-left">
        <p class="text-white font-semibold mb-1">Data Engineering Pilipinas</p>
        <div class="flex items-center justify-center md:justify-start gap-3">
          <a href="https://youtube.com" target="_blank" rel="noopener" class="text-dep-gold hover:text-white text-xs flex items-center gap-1"><svg class="w-3.5 h-3.5" viewBox="0 0 24 24" fill="currentColor"><!-- YT icon --></svg>YouTube</a>
          <a href="https://discord.gg/buDgydz7J9" target="_blank" rel="noopener" class="text-dep-gold hover:text-white text-xs flex items-center gap-1"><svg class="w-3.5 h-3.5" viewBox="0 0 24 24" fill="currentColor"><!-- Discord icon --></svg>Discord</a>
          <a href="https://github.com/DataEngineeringPilipinas" target="_blank" rel="noopener" class="text-dep-gold hover:text-white text-xs flex items-center gap-1"><svg class="w-3.5 h-3.5" viewBox="0 0 24 24" fill="currentColor"><!-- GitHub icon --></svg>GitHub</a>
          <a href="https://www.linkedin.com/company/data-engineering-pilipinas" target="_blank" rel="noopener" class="text-dep-gold hover:text-white text-xs flex items-center gap-1"><svg class="w-3.5 h-3.5" viewBox="0 0 24 24" fill="currentColor"><!-- LinkedIn icon --></svg>LinkedIn</a>
        </div>
      </div>
      <p class="text-white/50 text-xs">Built by the DEP community · Free & open-source · © 2026</p>
    </div>
  </div>
</footer>
```

**If editing individually:** Add LinkedIn link to hub footer (already has YouTube, Discord, GitHub). For individual pages, add the same 4-link row to their existing footers.

---

### Change 7: Add scroll-to-top button

**Files:** All 27 HTML files (or one JS partial)  
**Effort:** ~15–30 minutes  
**Impact:** Medium — expected UX on content-heavy pages

**Implementation:** Add this single script block to the bottom of every page (before `</body>`):
```html
<script>
  // Scroll-to-top button
  const btn = document.createElement('button');
  btn.innerHTML = '↑';
  btn.className = 'fixed bottom-6 right-6 w-10 h-10 rounded-full bg-dep-gold text-white shadow-lg opacity-0 transition-opacity duration-300 hover:bg-yellow-600 z-50 focus:outline-none';
  btn.setAttribute('aria-label', 'Back to top');
  document.body.appendChild(btn);
  window.addEventListener('scroll', () => {
    btn.style.opacity = window.scrollY > 400 ? '1' : '0';
  });
  btn.addEventListener('click', () => window.scrollTo({ top: 0, behavior: 'smooth' }));
</script>
```

**Alternative:** Add to just `index.html` and the 6 core feature pages (pathway, mentorship, linkedin, fluency-map, git-guide, modules/*). Skip for less-visited Phase 3 pages.

---

## P3 — Nice-to-Have Polish

### Change 8: Add favicon + Open Graph meta tags to all pages

**Files:** All 27 HTML files (or one partial)  
**Effort:** ~20 minutes  
**Impact:** Low-medium — professional polish for social sharing

**Implementation:** In every `<head>`, after the title tag, add:
```html
<!-- Favicon: sun icon as inline SVG data URI -->
<link rel="icon" href="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'%3E%3Ccircle cx='50' cy='50' r='20' fill='%23d4910b'/%3E%3Cline x1='50' y1='10' x2='50' y2='25' stroke='%23d4910b' stroke-width='6'/%3E%3Cline x1='50' y1='75' x2='50' y2='90' stroke='%23d4910b' stroke-width='6'/%3E%3Cline x1='10' y1='50' x2='25' y2='50' stroke='%23d4910b' stroke-width='6'/%3E%3Cline x1='75' y1='50' x2='90' y2='50' stroke='%23d4910b' stroke-width='6'/%3E%3C/svg%3E" type="image/svg+xml">
<!-- Open Graph -->
<meta property="og:title" content="DEP Community Hub — Free Data Career Learning for Pinoys">
<meta property="og:description" content="Structured, free learning paths for Filipinos transitioning into data careers. SQL, Python, Power BI, and more.">
<meta property="og:type" content="website">
<meta property="og:locale" content="en_PH">
```

---

## Implementation Order & Dependencies

| Step | Change | Depends On | Time |
|------|--------|-----------|------|
| 1 | Change 2 (All Modules section on hub) | — | 15 min |
| 2 | Change 1 (Cross-links in roadmap accordion) | — | 30 min |
| 3 | Change 5 (Sign-up form → localStorage) | — | 15 min |
| 4 | Change 3 (pathway/index.html interactivity) | — | 45 min |
| 5 | Change 4 (mentorship/index.html interactivity) | — | 30 min |
| 6 | Change 7 (scroll-to-top button) | — | 20 min |
| 7 | Change 6 (LinkedIn in footers) | — | 30–60 min |
| 8 | Change 8 (favicon + OG tags) | — | 20 min |

**Total estimated effort:** ~3 hours  
**Files requiring changes:** All 27 HTML files, but most changes touch only `index.html` (changes 1, 2, 5) plus 2 files (changes 3, 4). Changes 6, 7, 8 are bulk operations across all files.

---

## Not Implemented (Out of Scope)

| Feature | Reason |
|---------|--------|
| New feature pages (#16, #20, #23) | Would require new HTML files; scope is Pareto improvements to existing pages |
| Google Forms integration for sign-up | Requires external service setup; localStorage is sufficient for MVP prototype |
| Real mentor booking system | Out of scope for HTML-only MVP; Discord handles this |
