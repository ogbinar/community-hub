# Agent Configuration — Data Engineering Pilipinas (DEP) Community Hub

## Project Overview

Build **real, functional HTML + Tailwind CSS** pages for the DEP Community Hub. This is a static site deployed to GitHub Pages from the `docs/` folder. No backend, no database, no build steps. Every feature must work as pure HTML/CSS/JS — if it needs a live API or server, use an iframe embed or localStorage instead.

All design decisions are grounded in the **DEP State of the Community Survey 2026** (n=1,861 respondents).

---

## Tech Stack

| Component | Implementation |
|---|---|
| HTML | Plain `.html` files, no templates, no build tools |
| CSS | Tailwind CSS via CDN (`https://cdn.tailwindcss.com`) |
| JavaScript | Vanilla JS only, inline `<script>` tags, `localStorage` for persistence |
| Fonts | Google Fonts CDN — Inter family |
| Icons | Inline SVG only (no icon libraries) |
| Embeds | YouTube iframes, Google Forms iframes (allowed external services) |

---

## Design System

### Color Palette

| Token | Hex | Usage |
|---|---|---|
| `--dep-blue` | `#1e3a5f` | Navbar background, hero section, headings, primary text on light backgrounds |
| `--dep-gold` | `#d4910b` | CTA buttons, accent borders (left-border 4px), badges, highlights, active states |
| `--dep-coral` | `#c0392b` | Warning/error callouts, "Where AI gets it wrong" sections, important alerts — used sparingly |
| `--dep-warm` | `#faf8f5` | Page body background (warm white) |
| `--dep-charcoal` | `#2d3748` | Body text color |
| `--dep-lightgold` | `#fef3c7` | Section backgrounds for accent sections, code example backgrounds |
| `--dep-slate` | `#6b7a8d` | Secondary text, muted labels, helper text |

**Tailwind config:**
```js
tailwind.config = {
  theme: {
    extend: {
      colors: {
        'dep-blue': '#1e3a5f',
        'dep-gold': '#d4910b',
        'dep-coral': '#c0392b',
        'dep-warm': '#faf8f5',
        'dep-charcoal': '#2d3748',
        'dep-lightgold': '#fef3c7',
        'dep-slate': '#6b7a8d',
      },
      fontFamily: { 'inter': ['Inter', 'system-ui', 'sans-serif'] },
    },
  },
};
```

### Typography

- **Font family:** `Inter` (Google Fonts CDN)
- **Heading weights:** `font-extrabold` (800) for h1, `font-bold` (700) for h2/h3
- **Body text:** default weight (400), `leading-relaxed` for readability
- **Monospace code:** `Courier New`, monospace fallback

### Philippine Visual Identity

1. **Sun motif** — Subtle SVG watermark in hero/dark sections (~5% opacity). Use the inline SVG from the shared navbar as a background pattern on dark backgrounds.

2. **Banig-inspired weave dividers** — Thin decorative horizontal lines using repeating linear gradient:
   ```css
   .banig-divider {
     height: 8px;
     background-image: repeating-linear-gradient(
       45deg, transparent, transparent 8px,
       rgba(212,145,11,0.2) 8px, rgba(212,145,11,0.2) 16px
     );
   }
   ```

3. **Warm color temperature** — Warm whites and grays throughout. Never use cold corporate blues or stark blacks. The `#faf8f5` warm white is the default page background.

4. **Local microcopy** — Use "₱" for currency, reference local realities (Philippine time zones, local learning platforms like Facebook Groups, Filipino names in examples). Microcopy should feel like it's written by Pinoys for Pinoys.

### Layout & Spacing

- **Max width:** `max-w-[1120px]` centered with `mx-auto`
- **Horizontal padding:** `px-4 sm:px-6 lg:px-8` (responsive)
- **Section spacing:** `mb-12` between major sections, `mb-10` between subsections
- **Card padding:** `p-6` for content cards, `p-4` for smaller elements

### Responsive Design

- Mobile-first approach
- Grid layouts: `grid-cols-1 md:grid-cols-2 lg:grid-cols-3`
- Navbar text hidden on mobile (`hidden sm:inline` for long labels)
- Breakpoints: `sm` (640px), `md` (768px), `lg` (1024px)

---

## Shared Components

### Navbar (Every Page)

```html
<nav class="fixed top-0 left-0 right-0 z-50 bg-dep-blue shadow-md">
  <div class="max-w-[1120px] mx-auto px-4 sm:px-6 lg:px-8">
    <div class="flex items-center justify-between h-16">
      <a href="../docs/index.html" class="flex items-center gap-2 text-white font-bold text-lg">
        <!-- Sun motif SVG icon -->
        <svg class="w-7 h-7 text-dep-gold" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round">
          <circle cx="12" cy="12" r="4"/>
          <line x1="12" y1="1" x2="12" y2="3"/>
          <line x1="12" y1="21" x2="12" y2="23"/>
          <line x1="4.22" y1="4.22" x2="5.64" y2="5.64"/>
          <line x1="18.36" y1="18.36" x2="19.78" y2="19.78"/>
          <line x1="1" y1="12" x2="3" y2="12"/>
          <line x1="21" y1="12" x2="23" y2="12"/>
        </svg>
        <span class="hidden sm:inline">DEP Community Hub</span>
      </a>
      <!-- Nav links: adjust per page -->
    </div>
  </div>
</nav>
```

### Footer (Every Page)

```html
<footer class="bg-dep-blue py-8 border-t-2 border-dep-gold/30">
  <div class="max-w-[1120px] mx-auto px-4 sm:px-6 lg:px-8 text-center">
    <p class="text-white/60 text-sm">Built by the Data Engineering Pilipinas community. All tools are free and open-source.</p>
  </div>
</footer>
```

### Card Pattern (Reusable)

```html
<div class="bg-white rounded-xl shadow-md p-6 border-l-4 border-dep-gold card-hover">
  <!-- Card content -->
</div>
```

With hover effect:
```css
.card-hover { transition: transform 0.2s ease, box-shadow 0.2s ease; }
.card-hover:hover { transform: translateY(-4px); box-shadow: 0 12px 25px rgba(30,58,95,0.15); }
```

### Code Block Pattern (Copyable)

```html
<div class="bg-dep-lightgold p-4 rounded-lg border-l-4 border-dep-gold my-4 relative">
  <button onclick="copyCode(this)" class="absolute top-2 right-2 bg-dep-gold text-white text-xs px-3 py-1 rounded hover:bg-yellow-600 transition-colors">Copy</button>
  <pre><code>-- Your code here</code></pre>
</div>
```

With JS helper:
```js
function copyCode(btn) {
  const code = btn.parentElement.querySelector('code').textContent;
  navigator.clipboard.writeText(code).then(() => {
    const original = btn.textContent;
    btn.textContent = 'Copied!';
    setTimeout(() => btn.textContent = original, 1500);
  });
}
```

---

## Page Structure Rules

### Main Hub (`docs/index.html`)

Must include these sections in order:
1. Hero / Header — Title, subtitle, CTA buttons, trust badges
2. Community Snapshot (Trust Bar) — 4 stat cards from survey data
3. Phase 1 Features — 3 cards in a grid
4. Phase 2 Features — 2 cards in a grid
5. How It Works — 6-step timeline
6. Full Roadmap — Expandable accordion (Phase 1 expanded, 2 & 3 collapsible)
7. Sign Up / Join Cohort — Form with name, email, role selector, checkboxes
8. Footer

### Learning Module Pages (`modules/*.html`)

Must follow this structure:
1. **Module Header** — Module number, title, description, YouTube video link (real URL or search link)
2. **Concept Explanation** — Clear explanation of the topic with inline code examples
3. **AI-Generated Answer** — What ChatGPT/Copilot would output for a sample problem
4. **Where AI Gets It Wrong** — Specific bugs/errors AI introduces, explained clearly
5. **Practitioner Validation** — Step-by-step how to verify/correct the AI output
6. **Resources** — Real links (SQLiteOnline.com, GitHub search, etc.) — NO `href="#"`

### Pathway Pages (`pathway/*.html`)

- `index.html` — 8-week timeline with week-by-week assignments, resource links, Discord check-in info
- `checklist.html` — Printable checklist with localStorage progress tracking, progress bar, completion message

### Mentorship Page (`mentorship/index.html`)

- "How It Works" 4-step flow
- Mentor directory cards (real names from survey)
- Session topics grid
- Sign-up CTAs (use real Google Forms or descriptive text — NO `href="#"`)

---

## Implementation Rules

### What's Allowed

| Feature | Implementation |
|---|---|
| Code examples | Inline `<pre><code>` with copy buttons |
| Video delivery | YouTube iframes OR links to YouTube search/results |
| Forms | Google Forms embedded via iframe, or static HTML forms with `mailto:` |
| Progress tracking | `localStorage` (checklists, progress bars) |
| Interactive elements | Vanilla JS for copy-to-clipboard, accordion toggle, checkbox state |
| External resources | Links to real tools: SQLiteOnline.com, GitHub, Canva, etc. |

### What's NOT Allowed

| Pattern | Why | Alternative |
|---|---|---|
| `href="#"` links | Fake navigation — provides no value | Use real URLs, remove the link, or replace with descriptive text |
| Placeholder text like "Coming soon" or "TBD" | Not usable — users can't do anything | Replace with actual instructions or a real resource link |
| Mock data as if it's live | Misleading — no backend exists | Use realistic examples clearly labeled as examples |
| External JS libraries (React, Vue, etc.) | Violates vanilla JS only constraint | Pure Tailwind + inline `<script>` |
| Image files (.jpg, .png) | Not required, increases complexity | Inline SVG icons and CSS patterns instead |

### Code Quality Rules

1. **Every HTML file must be a complete, standalone page** — includes `<html>`, `<head>`, `<body>`, navbar, footer
2. **No orphaned links** — every `href` must point to something real or be removed
3. **Copy buttons must work** — the `copyCode()` function is available on every page
4. **localStorage keys must be namespaced** — use `dep-*` prefix (e.g., `dep-pathway-progress`, `dep-checklist-state`)
5. **All forms must have a real destination** — Google Forms iframe, `mailto:`, or descriptive text explaining next steps
6. **No external CSS files** — all styles inline in `<style>` tags or via Tailwind utility classes
7. **Semantic HTML** — use `<section>`, `<article>`, `<nav>`, `<main>`, `<header>`, `<footer>` appropriately

---

## File Organization

```
docs/                          # GitHub Pages source folder (deployed)
  index.html                   # Main hub / landing page

modules/                       # AI-Augmented Learning Modules
  sql-basics.html              # Module 1: SQL basics + AI pitfalls
  python-fundamentals.html     # Module 2: Python/pandas + AI pitfalls
  excel-powerbi-intro.html     # Module 3: Excel/Power BI + AI pitfalls

pathway/                       # Career Shifter DA/DE Pathway
  index.html                   # 8-week timeline overview
  checklist.html               # Printable checklist with progress tracking

mentorship/                    # Time-Bound Mentorship Matching
  index.html                   # Mentor directory + session topics + sign-up

linkedin/                      # LinkedIn Profile Optimizer (Phase 2)
  index.html                   # Interactive checklist + AI prompt templates

fluency-map/                   # Multi-Tool Fluency Map (Phase 2)
  index.html                   # Visual roadmap + salary comparison table

git-guide/                     # Git/GitHub Adoption Guide (Phase 2)
  index.html                   # Step-by-step guide with code blocks
```

### Navigation Between Pages

- Each page's navbar links should point to sibling pages using relative paths (`../pathway/index.html`)
- The main hub (`docs/index.html`) is the entry point — all internal pages link back to it
- Learning modules have prev/next navigation at the bottom (Module 1 → Module 2 → Module 3)

---

## Design Principles Summary

1. **YouTube-first delivery** — Modules are video lessons with accompanying written guides
2. **Discord accountability cohorts** — Weekly check-ins keep learners on track
3. **DEP-branded certification** — Completion badges shareable on LinkedIn
4. **8-week sprint format** — Bounded milestones reduce drop-off risk
5. **AI as co-creator in curriculum** — Teach learners to interrogate AI, not just accept answers
6. **Real, functional HTML** — Every link works, every button does something, no placeholders
7. **Warm Philippine identity** — Sun motif, banig patterns, warm colors, local microcopy

---

## Survey Data Quick Reference

Key stats to reference in copy:

| Stat | Context |
|---|---|
| 96.6% PH-based | Community is overwhelmingly Filipino |
| 80.8% use AI for study weekly | AI-native learners — they already use it |
| ₱35k → ₱100k+ mobility gap | Primary motivation: income advancement |
| 58.5% have NO computing degree | Career shifters need structured guidance |
| 66.5% earn ≤₱35k | Financial bottleneck — pathway addresses this |
| 86.3% want to upskill | High demand for learning programs |
| 75.3% motivated by career advancement | LinkedIn badge directly activates this |
| 62.5% actively weighing their shift | Need "decision support" tools |
| 48.8% use version control | Git/GitHub guide addresses this gap |
| 15.1% of Professionals willing to mentor | Mentor pool — time-bound sessions work |

---

## Agent Workflow

When implementing new pages or features:

1. **Read `SPEC.md`** for feature requirements and roadmap context
2. **Read existing pages** in the same directory for consistent patterns
3. **Follow shared components** (navbar, footer, card pattern, code blocks) exactly
4. **Use real URLs** — no `href="#"`, no placeholder links
5. **Add to navigation** — every new page needs a link from its sibling pages and the main hub
6. **Test copy/paste** — ensure all code examples are valid and copy buttons work
7. **Commit with descriptive message** — include feature name, file count, line count

---

## Known Constraints & Trade-offs

### localStorage Limitations
- Data is browser-specific (clearing cache = lost progress)
- No sync across devices or browsers
- Mitigation: Provide print/PDF button for checklists so users can save offline

### No Backend
- Cannot validate form submissions server-side
- Mitigation: Use Google Forms iframe for real data collection, or `mailto:` for simple forms

### YouTube Dependency
- Videos must be hosted on DEP's YouTube channel (not yet created)
- Mitigation: Link to YouTube search results with relevant queries until videos exist

### Discord Dependency
- Q&A happens in Discord threads (external platform)
- Mitigation: Provide clear instructions on how to join and participate

---

## Quick Start Checklist for New Pages

- [ ] Include shared Tailwind config in `<head>`
- [ ] Include Google Fonts Inter link in `<head>`
- [ ] Include `<style>` with `body` font-family, `html` scroll-behavior, `.card-hover`, `.banig-divider`
- [ ] Include shared navbar with sun motif SVG
- [ ] Include shared footer
- [ ] Use `max-w-[1120px] mx-auto px-4 sm:px-6 lg:px-8` for main content
- [ ] Every `<a>` has a real `href` (not `#`)
- [ ] Code blocks have copy buttons with working `copyCode()` function
- [ ] localStorage keys use `dep-` prefix
- [ ] Page links back to `../docs/index.html` (main hub)
