# SPEC: Data Engineering Pilipinas — Community Hub MVP

## Overview

Build a **single-page, HTML + Tailwind CSS** prototype of the DEP Community Hub. The page serves as a landing hub that surfaces three core features for Students and Job Seekers (55.7% of the community), who are the primary launch audience.

The prototype is **not a full application** — it is a static, functional landing page that demonstrates the user experience and structure of the MVP. It should be deployable to GitHub Pages with zero dependencies beyond CDN-hosted Tailwind.

---

## 1. Target Audience

| Segment | Share | Why They're First |
|---|---|---|
| Students | 34.5% (n=642) | 81.6% want upskilling; 65.8% use AI daily for study |
| Job Seekers | 21.2% (n=394) | 86.9% want upskilling — highest motivation-to-enroll ratio |

## 2. Core Features to Surface

### Feature A: AI-Augmented Learning Modules (Score: 9.3/10)
- Three short modules: SQL Basics, Python Fundamentals, Excel/Power BI Intro
- Each module = 5-min YouTube video + GitHub Gist code examples + Discord Q&A thread
- Structure: Concept → AI-generated answer → "Where AI gets it wrong" → Practitioner validation

### Feature B: Career Shifter DA/DE Pathway (Score: 9.0/10)
- 8-week structured sprint with weekly milestones
- Week 1-2: SQL + Excel/Power Query | Week 3-4: Power BI + DAX | Week 5-6: Python pandas | Week 7-8: Cloud deployment + GitHub portfolio
- Discord accountability check-ins; DEP-branded completion badge

### Feature C: LinkedIn Profile Optimizer (Score: 8.7/10)
- Interactive checklist for optimizing LinkedIn profiles for data roles
- AI-assisted section writing prompts (copy-paste, no API needed in MVP)
- Before/after examples + optional Discord office hours

---

## 3. Page Structure & Sections

The single page should contain these sections in order:

### Section 1 — Hero / Header
- Background: deep blue (#1e3a5f) with subtle sun motif watermark (8-ray abstracted SVG, ~5% opacity)
- Title: "Data Engineering Pilipinas — Community Hub"
  - Color: white, large and bold
- Subtitle/tagline: "Free, structured learning for Filipinos transitioning into data careers"
  - Color: warm off-white (#faf8f5) with slightly relaxed line-height
- Primary CTA button: "Join First Cohort" — sun gold background (#d4910b), dark text, rounded corners
  - Hover: slight scale up + shadow increase
- Secondary link: "Explore the Hub →" — white text with underline on hover
  - Scrolls to features section
- Decorative accent: thin sun gold horizontal line beneath title (32px wide)
- Layout: centered vertically and horizontally; text left-aligned on mobile, centered on desktop

### Section 2 — Community Snapshot (Trust Bar)
Background: warm white (#faf8f5) with very light gold wash (#fef3c7 at 15% opacity)
Divider above section: thin decorative line with repeating diamond pattern (banig-inspired weave motif, sun gold at 20% opacity)

A horizontal stat bar of 4 cards in a grid (2x2 on mobile, 4-across on desktop):

**Card 1:** "40,000+" — large number in deep blue (#1e3a5f), label: "Community members"
**Card 2:** "96.6%" — large number in deep blue, label: "Philippines-based"
**Card 3:** "80.8%" — large number in deep blue, label: "Use AI for study weekly"
**Card 4:** "₱35k → ₱100k+" — large number in coral red (#c0392b), label: "The mobility gap we're closing"

Design note: Numbers are extra-large (text-5xl or similar), labels are small and muted. The ₱ symbol is prominent — this is the core problem statement.

### Section 3 — Features (The Three Pillars)
Background: warm white (#faf8f5)
Divider above section: thin decorative line with repeating diamond pattern
Section heading: "Three pillars to close the mobility gap" — deep blue, centered

Three cards in a grid layout (1-col on mobile, 3-col on desktop ≥768px), each representing one core feature:

**Card styling:** White background, rounded corners (rounded-xl), subtle shadow (shadow-md), hover: translateY(-2px) + shadow increase. Left border accent: sun gold (4px solid).

**Card 1: AI-Augmented Learning Modules**
- Icon: Sun gold SVG lightbulb or book icon at top-left of card
- Title: "AI-Augmented Learning Modules" — deep blue, bold
- Description: "Learn SQL, Python, and Power BI through AI-interrogated lessons — not passive videos"
- Three module pills/tags (sun gold background with dark text): "SQL Basics", "Python Fundamentals", "Excel/Power BI Intro"
- CTA button: Sun gold background, white text, rounded, "Start Learning →"

**Card 2: Career Shifter DA/DE Pathway**
- Icon: Sun gold SVG arrows-in-a-circle or roadmap icon
- Title: "Career Shifter DA/DE Pathway" — deep blue, bold
- Description: "8-week structured sprint with weekly milestones, Discord accountability, and a DEP-branded completion badge"
- Timeline pills (deep blue background, white text): "Wk 1-2 SQL", "Wk 3-4 Power BI", "Wk 5-6 Python", "Wk 7-8 Cloud + Portfolio"
- CTA button: Sun gold background, white text, rounded, "Join Cohort →"

**Card 3: LinkedIn Profile Optimizer**
- Icon: Sun gold SVG user-card or profile icon
- Title: "LinkedIn Profile Optimizer" — deep blue, bold
- Description: "Step-by-step checklist to build a project-rich LinkedIn profile that gets interview callbacks"
- Checklist preview items (3 shown with checkmark icons): "Project-rich GitHub linking", "Certification badge display", "Headline optimization"
- CTA button: Sun gold background, white text, rounded, "Get the Checklist →"

### Section 4 — How It Works (User Journey)
Background: deep blue (#1e3a5f) with subtle sun motif watermark (~5% opacity, white)
Divider above section: decorative diamond pattern line
Section heading: "How it works" — white, centered, large

A horizontal timeline (6 steps, displayed as a flow on desktop, vertical stack on mobile):

1. **Watch** — YouTube video (5-min module) — icon: play circle
2. **Read** — GitHub Gist code examples — icon: file code
3. **Try** — Exercises on your laptop — icon: laptop
4. **Ask** — Post questions in Discord thread — icon: chat bubble
5. **Get feedback** — Mentor response within 24 hours — icon: checkmark circle
6. **Earn** — DEP-branded badge at completion — icon: medal/star

Each step: white number circle (sun gold background) as the step indicator, white text description below it. Connector lines between steps in sun gold.

### Section 5 — Sign Up / Join Cohort
Background: warm white (#faf8f5) with very light gold wash
Divider above section: decorative diamond pattern line
Section heading: "Join the first cohort" — deep blue, centered, large
Subheading (warm gray): "Free. No credit card needed. Built by Pinoys, for Pinoys."

A simple form (non-functional, static) with fields:
- Name (text input) — label above field, warm gray text
- Email (email input) — label above field
- Role selector (dropdown): Student / Job Seeker / Career Shifter / Data Professional / Other
- "I want to learn" checkbox group with tag-style checkboxes: SQL / Python / Power BI / DAX / Cloud Deployment
  - Checked boxes: sun gold background, white text
  - Unchecked: light gray border, warm gray text
- Submit button: large, centered, sun gold background (#d4910b), dark text (not white — contrast against gold), rounded, "Join First Cohort"
- Microcopy beneath form: "We'll send you a Discord invite + Week 1 materials within 24 hours"

### Section 6 — Footer
Background: deep blue (#1e3a5f), white text
Layout: 2-column on desktop (links left, credits right), single column on mobile

Left side:
- "Data Engineering Pilipinas" — white, bold
- Links row: YouTube / Discord / GitHub / LinkedIn — sun gold color, hover: white
- Small tagline beneath: "All tools are free and open-source."

Right side:
- "Built by the Data Engineering Pilipinas community"
- Copyright notice: "© 2026 DEP Community. Survey compiled by Sandy G. Cabanes."
- Subtle sun gold horizontal line as top border

---

## 4. Design Requirements

### Visual Identity: Balancing DEP's Technical Cleanliness with Philippine Character

The current DEP website (dataengineering.ph) is a **Quarto/Bootstrap-generated site** with:
- Dark/light mode toggle
- Very clean, academic, minimal aesthetic
- Bootstrap Icons (bi-github, bi-facebook, bi-discord)
- Neutral color treatment — mostly grays and blues from the Quarto theme
- Left sidebar TOC navigation
- No brand personality beyond "technical documentation"

The Community Hub prototype should **preserve the clean technical foundation** while injecting **Philippine visual identity** that signals cultural belonging. The goal: it should feel like it belongs to the same ecosystem as dataengineering.ph, but with warmth and cultural specificity.

### Color Palette
| Role | Hex | Usage |
|---|---|---|
| Deep Blue (primary) | #1e3a5f | Hero background, navbar — replaces navy; inspired by Philippine waters, echoes the blue in the PH flag |
| Sun Gold (accent) | #d4910b | CTA buttons, highlights, active states — warm gold inspired by sun rays of the PH flag |
| Coral Red (secondary accent) | #c0392b | Badge elements, important callouts — subtle nod to the red in the PH flag, used sparingly for emphasis only |
| Warm White | #faf8f5 | Card backgrounds, light sections — slightly warm off-white instead of pure white; feels more inviting |
| Charcoal | #2d3748 | Body text — softer than pure black |
| Light Gold (subtle) | #fef3c7 | Section backgrounds for accent sections — very light gold wash |
| Slate | #6b7a8d | Secondary text, muted labels |

**Design principle:** Philippine colors are used as **accents**, not dominant. The primary visual language stays clean and technical (like dataengineering.ph); the PH elements provide warmth, identity, and emotional resonance.

### Philippine Visual Elements to Incorporate

1. **Sun motif — subtle SVG accent**
   - A simplified 8-ray sun icon used as a decorative element in the hero section background or as a corner accent on feature cards
   - NOT the full national flag emblem — just an abstracted, minimal geometric interpretation (clean lines, no detail)
   - Renders as a very faint watermark pattern (~5-8% opacity) behind the hero section

2. **Lacuna / weave-inspired border patterns**
   - Subtle geometric border or divider between sections inspired by traditional Filipino weave patterns (banig/tapis geometry)
   - Applied as a thin decorative line with repeating diamond/rhombus shapes between major sections
   - Color: sun gold at 20% opacity — barely noticeable but adds texture

3. **Warm color temperature**
   - Avoid cold grays; shift toward warm neutrals (warm white, warm gray text)
   - This small shift makes the page feel more approachable and less "corporate documentation"

4. **Philippine context in microcopy**
   - Use "₱" currency symbol prominently (already in spec)
   - Microcopy that reflects local reality: "built by Pinoys, for Pinoys", "free — no credit card needed"
   - References to local learning realities: "works on your laptop (8GB RAM+)", "no expensive tools required"

### Typography
- Font: Inter (loaded from Google Fonts CDN) as primary; system-ui as fallback
  - Matches the clean, modern feel of dataengineering.ph while being slightly warmer
- Headings: Bold/ExtraBold, 2xl-4xl scale
- Body: Regular, base/sm scale with relaxed line-height (1.65 vs default 1.5) for warmth
- CTAs: Semibold, title case (not all caps — feels more approachable than corporate)
- Accent text (taglines, labels): Medium weight, slightly smaller, uppercase with letter-spacing

### Layout Constraints
- Fully responsive: mobile-first (stack vertically on <640px, grid on ≥640px)
- Max content width: 1120px centered
- Section padding: py-16 md:py-24
- Card gap: gap-6
- No JavaScript frameworks — vanilla HTML only
- Navbar: fixed top, dark blue background with white text (matching dataengineering.ph's dark navbar style)

### Interactivity (Minimal JS)
- Smooth scroll for anchor links (CTA buttons → section targets)
- Mobile hamburger menu toggle (single function, <10 lines)
- Form does not submit anywhere — purely visual prototype
- Hover states on cards: subtle lift effect (translateY(-2px) + shadow increase)

---

## 5. Technical Constraints

- **Single file** (index.html) or at most two files (index.html + tailwind via CDN)
- **Tailwind CSS via CDN** — no build step, no npm, no bundler
- **Google Fonts CDN** — Inter font family loaded from Google Fonts (only dependency beyond Tailwind)
- **No backend** — form is static/visual only
- **No images required** — use inline SVG icons (heroicons or custom sun motif) for visual elements
- **Deployable to GitHub Pages** as a static site

---

## 6. Success Criteria

The MVP prototype should:
1. Render correctly on mobile and desktop
2. Surface all three core features with clear descriptions and CTAs
3. Reflect the survey-grounded design principles (YouTube-first, Discord accountability, DEP branding)
4. Be deployable to GitHub Pages with zero configuration beyond pushing the file
5. Load fast — only Tailwind CDN + Google Fonts as external dependencies
6. Feel visually connected to dataengineering.ph's clean aesthetic while having distinct Philippine warmth and cultural identity

---

## 7. Out of Scope (Explicitly Excluded)

1. No backend, no database, no authentication
2. No actual YouTube/Discord/GitHub integrations
3. No dark/light mode toggle
4. No analytics tracking
5. No multi-page navigation — single page only
6. No animations beyond smooth scroll and hover states
7. No full national flag imagery or political symbolism — Philippine elements are subtle, abstracted, and professional

---

## 8. File Structure

```
community-hub/
├── SPEC.md                    ← this file
├── INDEX.md                   ← project index (existing)
├── ideate-results.md          ← feature prioritization (existing)
├── prototype-design-plan.md   ← design proposal (existing)
└── public/
    └── index.html             ← MVP prototype (to be built)
```
