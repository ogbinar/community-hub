# Implementation Plan: HTML-Only Features for DEP Community Hub

## Constraint Analysis

**What "HTML only" means:** Static HTML + Tailwind CSS (CDN) + vanilla JS. No backend, no database, no API calls, no server-side processing. Everything is pre-rendered content served as static files.

**What this enables:** Readable content pages, interactive checklists (localStorage), calculators (vanilla JS), directories (hardcoded JSON), templates (code blocks), timelines, roadmaps, guides, and reference documents.

**What this excludes:** Real-time booking systems, live dashboards with API feeds, user authentication, dynamic form submissions, real-time chat, video hosting, analytics tracking.

---

## Phase 1: MVP — HTML-Only Features (3 features)

### Feature 1: AI-Augmented Learning Modules (Score: 9.3/10)

**Implements as:** Static lesson pages with pre-written content blocks. Each module is a single HTML file.

**File structure:**
```
/modules/sql-basics.html
/modules/python-fundamentals.html
/modules/excel-powerbi-intro.html
```

**Each page contains:**
- Concept explanation section (written by volunteer)
- "AI-generated answer" example block (pre-written, showing what ChatGPT/Copilot would output)
- "Where AI gets it wrong" breakdown block (highlighted in coral/red)
- "How a practitioner validates it" section (best practices checklist)
- Embedded YouTube video (5-min module) via `<iframe>`
- Link to GitHub Gist for code examples
- Link to Discord Q&A thread

**Technical approach:**
- 3 separate HTML files, each following the same template structure
- Tailwind CSS via CDN for consistent styling
- Inline SVG icons for section headers
- YouTube embeds use iframe (allowed — it's just an embedded player)
- No interactivity needed beyond smooth scroll and copy-to-clipboard for code blocks

**Content to pre-write:**
- 3 module lesson plans (SQL basics, Python fundamentals, Excel/Power BI intro)
- 12 AI example answers (4 per module: correct answer, wrong answer, validation steps)
- Discord thread URLs (pre-created in the DEP Discord server)
- GitHub Gist links (created by volunteer contributors)

**Deliverable:** 3 HTML pages + 1 landing page linking to them. Total ~150 lines of content per module.

---

### Feature 2: Career Shifter DA/DE Pathway (Score: 9.0/10)

**Implements as:** A single-page roadmap with week-by-week milestones, downloadable checklist, and resource links.

**File structure:**
```
/pathway/index.html          ← Main pathway page
/pathway/checklist.html      ← Printable checklist
```

**Main page contains:**
- 8-week timeline (horizontal on desktop, vertical on mobile)
- Each week: assignment description, learning resources (links to YouTube videos, GitHub repos, free courses), milestone checklist
- Week 1-2: SQL basics + Excel/Power Query
- Week 3-4: Power BI fundamentals + DAX basics
- Week 5-6: Python pandas + data manipulation
- Week 7-8: Cloud deployment basics (AWS/Azure free tier) + GitHub portfolio setup
- Discord check-in thread links for each week
- DEP-branded completion badge SVG (downloadable PNG via Canva free tier link)

**Checklist page contains:**
- Printable checklist with checkboxes (localStorage to track progress)
- Week-by-week completion tracking
- "Post in Discord" reminders
- Export-to-PDF button (browser print function)

**Technical approach:**
- Vanilla JS for localStorage checkbox persistence
- Browser print dialog for PDF export
- YouTube embeds for video resources
- GitHub links for code examples
- No backend needed — all content is pre-written by volunteer mentors

**Content to pre-write:**
- 8 weeks of assignments (descriptions, learning objectives, deliverables)
- Resource links (YouTube videos, GitHub repos, free courses like DataTalks.Club Zoomcamp, SQLBolt, freePython.org)
- Discord check-in thread URLs
- Volunteer mentor assignment list

**Deliverable:** 2 HTML files. ~200 lines of content per week = ~1600 lines total.

---

### Feature 3: Time-Bound Mentorship Matching (Score: 8.7/10)

**Implements as:** A static mentor directory page + sign-up form that sends to Google Forms (free).

**File structure:**
```
/mentorship/index.html       ← Mentor directory + sign-up
```

**Page contains:**
- "How it works" section explaining the ADPList-style model (30-min sessions, specific topics, monthly commitment)
- Mentor directory cards showing: mentor name, expertise area, availability day/time, topics they cover
- Sign-up form for mentees (sends to Google Form embed — free, no backend needed)
- Sign-up form for mentors (same Google Form embed)
- Topic list: Resume Review, Burning Issue at Work, SQL Debugging, DAX Help, Career Advice

**Technical approach:**
- Google Forms embedded via iframe (free, no backend)
- Mentor directory is pre-populated with volunteer data
- No real-time booking — mentees request sessions, mentors confirm via Discord/email
- All mentor info is static HTML (updated monthly by volunteer admin)

**Content to pre-write:**
- Mentor profiles (name, expertise, availability, bio — collected via Google Form)
- Topic descriptions (what each 30-min session covers)
- "How it works" guide

**Deliverable:** 1 HTML file. ~50 mentor profiles max (expandable).

---

## Phase 2: Scale — HTML-Only Features (3 features)

### Feature 4: LinkedIn Profile Optimizer (Score: 8.7/10)

**Implements as:** Interactive checklist page with AI prompt templates and before/after examples.

**File structure:**
```
/linkedin/index.html         ← Main optimizer page
```

**Page contains:**
- Step-by-step checklist (6 steps):
  1. Project-rich GitHub linking guide
  2. Certification badge display instructions
  3. Skill endorsement strategies
  4. Headline optimization template
  5. About section AI prompt templates
  6. Experience section AI prompt templates
- AI-assisted content generation prompts (copy-paste blocks using Gemini free API format)
- Before/after LinkedIn profile screenshots (described in text since no images allowed)
- "Post your before/after in Discord" CTA

**Technical approach:**
- Vanilla JS for checkbox persistence (localStorage)
- Copy-to-clipboard buttons for AI prompt templates
- Collapsible sections for each checklist step
- No actual API calls — prompts are pre-written and ready to copy-paste into Gemini/Copilot

**Content to pre-write:**
- 6 checklist steps with detailed instructions
- 10+ AI prompt templates (headline, about, experience, skills, endorsements)
- Before/after examples (text descriptions of what good vs bad looks like)
- GitHub linking best practices guide

**Deliverable:** 1 HTML file. ~300 lines of content.

---

### Feature 5: Multi-Tool Fluency Map (Score: 8.3/10)

**Implements as:** Visual roadmap page showing tool progression paths with salary band data.

**File structure:**
```
/fluency-map/index.html      ← Tool roadmap visualization
```

**Page contains:**
- Interactive SVG roadmap diagram showing progression:
  - Entry level: Power BI → Excel → SQL
  - Mid level: Looker Studio → Python pandas → Git/GitHub
  - Senior level ($100k+): Tableau + Looker Studio + Python + Cloud (AWS/Azure)
- Salary band comparison table (₱35k, ₱75k–₱100k, ₱100k+) showing tool proficiency at each level
- Tool cards with: name, learning resources (free links), certification paths, salary impact
- "One BI tool" validation section explaining why single-tool advice is correct for entry-level but insufficient at senior level

**Technical approach:**
- SVG roadmap diagram (inline, no images)
- Collapsible accordion for each tool's details
- Tabbed interface for different career paths (DA vs DE)
- Vanilla JS for tab/accordion interactions

**Content to pre-write:**
- Tool progression data (which tools correlate with which salary bands from survey)
- Learning resource links for each tool (free courses, YouTube channels, documentation)
- Salary band comparison data (from DEP Survey 2026)
- "One BI tool" validation explanation

**Deliverable:** 1 HTML file. ~250 lines of content + SVG diagram.

---

### Feature 6: Git/GitHub Adoption Guide (Score: 8.3/10)

**Implements as:** Step-by-step guide with code examples, branching strategy diagrams, and portfolio showcase tips.

**File structure:**
```
/git-guide/index.html        ← Main guide page
```

**Page contains:**
- GitHub basics section (create account, create repo, push first file)
- Branching strategies section (feature branch, GitFlow lite)
- Commit conventions section (conventional commits format)
- PR workflows section (how to submit work for review)
- Portfolio showcase guide (README templates, project organization)
- Code examples in syntax-highlighted blocks

**Technical approach:**
- Tailwind CSS typography classes for code block styling
- Copy-to-clipboard buttons for all code examples
- Collapsible sections for each topic
- No backend needed — all content is pre-written

**Content to pre-write:**
- Step-by-step GitHub setup instructions (with screenshots described in text)
- 5+ code examples (git init, git branch, git commit, git push, PR workflow)
- README template for portfolio projects
- Branching strategy diagrams (ASCII art or SVG)

**Deliverable:** 1 HTML file. ~350 lines of content + code blocks.

---

## Phase 3: Expand — HTML-Only Features (Select subset)

From the 34 remaining features, here are the ones fully implementable as static HTML:

### Fully Implementable (no external services needed)

| # | Feature | Score | Implementation Approach |
|---|---|---|---|
| 7 | Power BI Gap Closer | 8.8 | Static lesson pages (same template as AI-Augmented Learning Modules) |
| 8 | DAX Portfolio Project | 8.2 | Static project template page with code examples |
| 9 | AI Workflow Interview Prep | 8.2 | Static interview prep guide with Q&A pairs and answer templates |
| 10 | Remote Mentorship Board | 8.2 | Static mentor directory (same as Feature 3, expanded) |
| 11 | DAX Micro-Lessons | 8.0 | Bite-sized HTML pages (5-min concept explanations) |
| 12 | Draw.io Architecture Templates | 8.0 | Static page with SVG architecture diagrams + download links to .drawio files |
| 13 | GitHub Portfolio Showcase Guide | 8.0 | README template generator (vanilla JS, generates markdown code block) |
| 14 | DAX Signal Gap Course | 8.0 | Static lesson pages focused on DAX functions |
| 15 | AI Study Workflow Guide | 7.8 | One-page PDF-style HTML guide with workflow diagrams |
| 16 | Portfolio Builder Template | 7.8 | Notion/Google Sites template link + HTML preview of what a good portfolio looks like |
| 17 | "Decision to Shift" Support Framework | 7.8 | Self-assessment quiz (vanilla JS, shows results based on answers) |
| 18 | Hiring Pipeline Connector | 7.8 | Static job board page + employer/mentor sign-up (Google Forms embed) |
| 19 | Creator Spotlight Platform | 7.8 | Monthly featured creator cards with interview Q&A text |
| 20 | YouTube Content Calendar | 7.8 | Static calendar table showing upcoming topics and assigned creators |
| 21 | Local to Cloud Bridge Curriculum | 7.5 | Static lesson pages + cloud deployment checklists |
| 22 | Cloud Deployment Bootcamp | 7.8 | Static bootcamp guide with step-by-step deployment instructions |
| 23 | Cloud Certification Guide | 7.8 | Certification roadmap page with study plans and free resource links |
| 24 | Laptop-Only Project Templates | 7.5 | Pre-written Jupyter notebook examples + Python scripts (embedded code blocks) |
| 25 | Salary Band Progression Tracker | 7.5 | Interactive calculator (vanilla JS: input skills → see salary band recommendations) |
| 26 | AI-Assisted Coding Toolkit | 7.5 | Static guide with Copilot/Cursor/Databricks setup instructions and prompt templates |
| 27 | Async Collaboration Tools | 7.5 | Static guide for async contribution workflows (GitHub Issues, Discord, etc.) |
| 28 | Language/Cultural Bridge Guide | 7.5 | One-page HTML guide with cultural context tips |
| 29 | Free Credential Tracker | 7.0 | Static page listing all free certs with difficulty levels and links |
| 30 | Content Repurposing Toolkit | 7.0 | Templates for YouTube → LinkedIn → GitHub README conversion |
| 31 | Creator Analytics Dashboard | 7.5 | **NOT implementable** — requires API feeds (YouTube, GitHub). Replace with static "Creator Guide" page. |
| 32 | Career Shifter Mentorship Board | 8.5 | Static mentor directory (same as Feature 3) |
| 33 | Cross-Promotion Network | 8.2 | Static creator directory with YouTube/GitHub/LinkedIn links |
| 34 | Structured Giving-Back Framework | 7.5 | One-page HTML guide with time commitment estimates |
| 35 | Overseas Hiring Connector | 7.8 | Static job board + visa/work authorization guide |
| 36 | Global Contributor Network | 7.0 | Static contributor directory (same as Feature 33) |
| 37 | Personalized Learning Path Generator | 6.5 | Interactive tool with vanilla JS decision tree (overlaps with #1) |
| 38 | "Master One BI Tool" Validation Tool | 6.5 | Static comparison page (overlaps with #5) |
| 39 | Mentor Impact Dashboard | 6.5 | **NOT implementable** — requires backend to track session rates. Use GitHub Issues + Discord threads instead. |
| 40 | Job Application Tracker | 7.0 | Interactive tracker with localStorage persistence (overlaps with #4) |

### NOT Implementable as Pure HTML (2 features)

| # | Feature | Score | Why It Doesn't Fit | Alternative |
|---|---|---|---|---|
| 31 | Creator Analytics Dashboard | 7.5 | Requires YouTube/GitHub API feeds for live data | Replace with static "Creator Guide" page |
| 39 | Mentor Impact Dashboard | 6.5 | Requires backend to track session completion rates | Use GitHub Issues + Discord threads (existing tools) |

---

## Detailed Implementation Plan for Each Feature

### Feature 1: AI-Augmented Learning Modules

**File:** `modules/{module-name}.html`
**Template structure:**
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <!-- Tailwind CDN, Inter font -->
</head>
<body class="bg-dep-warm">
  <nav><!-- Shared navbar --></nav>

  <main class="max-w-[1120px] mx-auto px-4 py-16">
    <!-- Hero: Module title + YouTube embed -->
    <section id="concept">
      <h2>Concept Explanation</h2>
      <p>Volunteer-written content...</p>
    </section>

    <section id="ai-answer">
      <h2>AI-Generated Answer</h2>
      <div class="bg-dep-lightgold p-4 rounded-lg border-l-4 border-dep-gold">
        <pre><code>What ChatGPT/Copilot would output...</code></pre>
        <button onclick="copyCode()">Copy</button>
      </div>
    </section>

    <section id="where-ai-wrong">
      <h2>Where AI Gets It Wrong</h2>
      <div class="bg-red-50 p-4 rounded-lg border-l-4 border-dep-coral">
        <ul>
          <li>Misconception 1: explanation</li>
          <li>Misconception 2: explanation</li>
        </ul>
      </div>
    </section>

    <section id="practitioner-validation">
      <h2>How a Practitioner Validates It</h2>
      <ol>
        <li>Check the documentation link</li>
        <li>Run the code in your environment</li>
        <li>Compare output against expected results</li>
      </ol>
    </section>

    <section id="resources">
      <h2>Resources</h2>
      <ul>
        <li><a href="#">YouTube Video (5 min)</a></li>
        <li><a href="#">GitHub Gist (code examples)</a></li>
        <li><a href="#">Discord Q&A Thread</a></li>
      </ul>
    </section>
  </main>

  <footer><!-- Shared footer --></footer>
</body>
</html>
```

**Content checklist:**
- [ ] Write concept explanation for SQL basics
- [ ] Write AI-generated answer example for SQL basics
- [ ] Write "Where AI gets it wrong" breakdown for SQL basics
- [ ] Write practitioner validation steps for SQL basics
- [ ] Repeat for Python fundamentals and Excel/Power BI intro
- [ ] Create YouTube videos (5 min each)
- [ ] Create GitHub Gists with code examples
- [ ] Create Discord Q&A threads

---

### Feature 2: Career Shifter DA/DE Pathway

**File:** `pathway/index.html` + `pathway/checklist.html`

**Main page structure:**
```html
<main class="max-w-[1120px] mx-auto px-4 py-16">
  <h1>Career Shifter DA/DE Pathway</h1>
  <p>8-week structured sprint for career shifters with no computing degree.</p>

  <!-- Week-by-week timeline -->
  <div class="space-y-8">
    <section class="week-card bg-white rounded-xl shadow-md p-6 border-l-4 border-dep-gold">
      <h3>Week 1–2: SQL Basics + Excel/Power Query</h3>
      <ul>
        <li>Learning resources: DataCamp (free), SQLBolt, freePython.org</li>
        <li>Assignment: Write 5 SQL queries against a sample dataset</li>
        <li>Deliverable: GitHub repo with queries + Power Query export</li>
      </ul>
      <a href="#">Discord Check-in Thread →</a>
    </section>

    <!-- Repeat for Weeks 3–8 -->
    <!-- Week 3-4: Power BI + DAX basics -->
    <!-- Week 5-6: Python pandas -->
    <!-- Week 7-8: Cloud deployment + GitHub portfolio -->
  </div>

  <section id="completion-badge">
    <h2>DEP-Branded Completion Badge</h2>
    <p>Share your badge on LinkedIn when you complete all 8 weeks.</p>
    <a href="#">Download Badge (Canva free tier)</a>
  </section>
</main>
```

**Checklist page structure:**
```html
<main class="max-w-[1120px] mx-auto px-4 py-16">
  <h1>Pathway Checklist</h1>
  <p>Track your progress. Your selections are saved locally.</p>

  <div class="space-y-4">
    <label class="flex items-center gap-3 p-3 bg-white rounded-lg shadow-sm">
      <input type="checkbox" class="week-checkbox" data-week="1" onchange="saveProgress()">
      <span>Week 1–2: SQL Basics + Excel/Power Query — Assignment submitted</span>
    </label>
    <!-- Repeat for Weeks 3–8 -->

    <div id="progress-bar" class="mt-6">
      <div class="w-full bg-gray-200 rounded-full h-4">
        <div id="progress-fill" class="bg-dep-gold h-4 rounded-full transition-all" style="width: 0%"></div>
      </div>
      <p class="text-sm text-dep-slate mt-2">Progress: <span id="progress-text">0%</span></p>
    </div>

    <button onclick="window.print()" class="bg-dep-gold text-white px-6 py-2 rounded-lg">
      Export to PDF (Print)
    </button>
  </div>
</main>

<script>
  // localStorage persistence
  function saveProgress() {
    const checks = document.querySelectorAll('.week-checkbox');
    const progress = Array.from(checks).filter(c => c.checked).length / checks.length * 100;
    localStorage.setItem('dep-pathway-progress', JSON.stringify(
      Array.from(checks).map(c => c.checked)
    ));
    document.getElementById('progress-fill').style.width = progress + '%';
    document.getElementById('progress-text').textContent = Math.round(progress) + '%';
  }
  // Load saved progress on page load
  window.onload = () => {
    const saved = JSON.parse(localStorage.getItem('dep-pathway-progress') || '[]');
    const checks = document.querySelectorAll('.week-checkbox');
    checks.forEach((c, i) => { c.checked = saved[i] === true; });
    saveProgress(); // Recalculate progress display
  };
</script>
```

**Content checklist:**
- [ ] Write 8 weeks of assignments (objectives, resources, deliverables)
- [ ] Create Discord check-in thread URLs for each week
- [ ] Create GitHub repo templates for each week's assignment
- [ ] Design DEP-branded completion badge (Canva free tier)
- [ ] Recruit volunteer mentors (Google Form)

---

### Feature 3: Time-Bound Mentorship Matching

**File:** `mentorship/index.html`

**Structure:**
```html
<main class="max-w-[1120px] mx-auto px-4 py-16">
  <h1>Time-Bound Mentorship Matching</h1>
  <p>30-minute sessions on specific topics. No open-ended commitment.</p>

  <!-- How it works -->
  <section class="mb-12">
    <h2>How It Works</h2>
    <ol>
      <li>Mentors commit to one 30-min session per month (e.g., first Thursday)</li>
      <li>Mentees request sessions on specific topics</li>
      <li>Mentor confirms availability via Discord</li>
      <li>Session happens via Discord voice channel or Google Meet</li>
    </ol>
  </section>

  <!-- Mentor directory -->
  <section class="mb-12">
    <h2>Available Mentors</h2>
    <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
      <div class="bg-white rounded-xl shadow-md p-6 border-l-4 border-dep-gold">
        <h3>Mentor Name</h3>
        <p class="text-sm text-dep-slate">Expertise: SQL, Power BI</p>
        <p class="text-sm text-dep-slate">Availability: First Thursday monthly, 7–8 PM PHT</p>
        <p class="text-sm text-dep-slate">Topics: Resume Review, SQL Debugging</p>
      </div>
      <!-- Repeat for each mentor -->
    </div>
  </section>

  <!-- Topics list -->
  <section class="mb-12">
    <h2>Available Session Topics</h2>
    <ul class="grid grid-cols-2 gap-3">
      <li><span class="font-semibold">Resume Review</span> — Get feedback on your resume</li>
      <li><span class="font-semibold">Burning Issue at Work</span> — Debug a real work problem</li>
      <li><span class="font-semibold">SQL Debugging</span> — Fix broken queries</li>
      <li><span class="font-semibold">DAX Help</span> — Understand measures and calculated columns</li>
      <li><span class="font-semibold">Career Advice</span> — Pathway guidance for your situation</li>
    </ul>
  </section>

  <!-- Sign-up forms -->
  <section class="mb-12">
    <h2>Sign Up</h2>
    <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
      <div>
        <h3 class="font-semibold mb-3">I'm a Mentee</h3>
        <iframe src="https://docs.google.com/forms/d/e/YOUR_FORM_LINK/viewform" width="100%" height="400" frameborder="0"></iframe>
      </div>
      <div>
        <h3 class="font-semibold mb-3">I'm a Mentor</h3>
        <iframe src="https://docs.google.com/forms/d/e/YOUR_FORM_LINK/viewform" width="100%" height="400" frameborder="0"></iframe>
      </div>
    </div>
  </section>
</main>
```

**Content checklist:**
- [ ] Create Google Forms for mentee and mentor sign-up
- [ ] Collect mentor profiles (name, expertise, availability, bio)
- [ ] Write topic descriptions
- [ ] Create Discord voice channel structure
- [ ] Set up GitHub Issues template for session tracking

---

### Feature 4: LinkedIn Profile Optimizer

**File:** `linkedin/index.html`

**Structure:**
```html
<main class="max-w-[1120px] mx-auto px-4 py-16">
  <h1>LinkedIn Profile Optimizer</h1>
  <p>Step-by-step checklist to build a project-rich LinkedIn profile that gets interview callbacks.</p>

  <!-- Checklist steps -->
  <section class="space-y-4">
    <details class="bg-white rounded-xl shadow-md overflow-hidden" open>
      <summary class="p-4 font-semibold cursor-pointer flex items-center gap-2">
        Step 1: Project-Rich GitHub Linking
      </summary>
      <div class="p-4 border-t">
        <ol>
          <li>Create a GitHub account (if you don't have one)</li>
          <li>Complete at least 2 projects from the pathway</li>
          <li>Write a README with: project description, tools used, what you learned</li>
          <li>Link your GitHub URL in your LinkedIn "Featured" section</li>
        </ol>
      </div>
    </details>

    <details class="bg-white rounded-xl shadow-md overflow-hidden">
      <summary class="p-4 font-semibold cursor-pointer flex items-center gap-2">
        Step 2: Certification Badge Display
      </summary>
      <div class="p-4 border-t">
        <ol>
          <li>Complete free certifications (Microsoft Learn, Google Analytics)</li>
          <li>Add them to LinkedIn "Licenses & Certifications" section</li>
          <li>Upload your DEP completion badge as an image</li>
        </ol>
      </div>
    </details>

    <!-- Repeat for Steps 3–6 -->
    <!-- Step 3: Skill Endorsement Strategies -->
    <!-- Step 4: Headline Optimization Template -->
    <!-- Step 5: About Section AI Prompts -->
    <!-- Step 6: Experience Section AI Prompts -->
  </section>

  <!-- AI prompt templates -->
  <section class="mt-12">
    <h2>AI-Assisted Content Generation</h2>
    <p>Copy these prompts into Gemini or Copilot to draft your profile sections:</p>

    <div class="space-y-4 mt-4">
      <div class="bg-dep-lightgold p-4 rounded-lg border-l-4 border-dep-gold">
        <h3 class="font-semibold mb-2">Headline Prompt</h3>
        <pre><code class="whitespace-pre-wrap">Write a LinkedIn headline for a data professional transitioning from [current role] to [target role]. Include relevant skills: SQL, Python, Power BI. Keep it under 200 characters.</code></pre>
        <button onclick="copyText(this)" class="mt-2 text-sm text-dep-gold font-semibold">Copy Prompt →</button>
      </div>

      <!-- Repeat for other prompts -->
    </div>
  </section>

  <!-- Before/After examples -->
  <section class="mt-12">
    <h2>Before & After Examples</h2>
    <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
      <div class="bg-gray-50 p-6 rounded-lg border-2 border-red-200">
        <h3 class="font-semibold text-dep-coral mb-3">❌ Before</h3>
        <p class="text-sm">"Looking for a job in data. I know Excel and Power BI."</p>
      </div>
      <div class="bg-green-50 p-6 rounded-lg border-2 border-green-400">
        <h3 class="font-semibold text-green-700 mb-3">✅ After</h3>
        <p class="text-sm">"Data Analyst | SQL, Python, Power BI | Built 3 end-to-end analytics projects | Helping businesses make data-driven decisions"</p>
      </div>
    </div>
  </section>

  <!-- CTA -->
  <section class="mt-12 text-center">
    <p class="text-dep-slate">Post your "before" and "after" LinkedIn profiles in the Discord #linkedin-checks channel for peer feedback.</p>
    <a href="#" class="inline-block mt-4 bg-dep-gold text-white px-6 py-2 rounded-lg font-semibold">Go to Discord →</a>
  </section>
</main>

<script>
  function copyText(btn) {
    const code = btn.previousElementSibling.textContent;
    navigator.clipboard.writeText(code);
    btn.textContent = 'Copied!';
    setTimeout(() => btn.textContent = 'Copy Prompt →', 2000);
  }
</script>
```

**Content checklist:**
- [ ] Write 6 checklist steps with detailed instructions
- [ ] Create 10+ AI prompt templates (headline, about, experience, skills)
- [ ] Write before/after examples for each section
- [ ] GitHub linking best practices guide
- [ ] Certification badge display instructions

---

### Feature 5: Multi-Tool Fluency Map

**File:** `fluency-map/index.html`

**Structure:**
```html
<main class="max-w-[1120px] mx-auto px-4 py-16">
  <h1>Multi-Tool Fluency Map</h1>
  <p>Visual roadmap from entry-level to ₱100k+: what separates high earners and how to get there.</p>

  <!-- Interactive SVG roadmap -->
  <section class="mb-12">
    <h2>Your Progression Path</h2>
    <div class="bg-white rounded-xl shadow-md p-8">
      <!-- SVG diagram: entry → mid → senior -->
      <svg viewBox="0 0 800 300" class="w-full">
        <!-- Entry level box -->
        <rect x="50" y="100" width="200" height="100" rx="8" fill="#fef3c7" stroke="#d4910b" stroke-width="2"/>
        <text x="150" y="140" text-anchor="middle" font-size="14" font-weight="bold">Entry Level</text>
        <text x="150" y="160" text-anchor="middle" font-size="11">Power BI, Excel, SQL</text>

        <!-- Arrow -->
        <path d="M270 150 L300 150" stroke="#d4910b" stroke-width="2" marker-end="url(#arrow)"/>

        <!-- Mid level box -->
        <rect x="350" y="100" width="200" height="100" rx="8" fill="#fef3c7" stroke="#d4910b" stroke-width="2"/>
        <text x="450" y="140" text-anchor="middle" font-size="14" font-weight="bold">Mid Level</text>
        <text x="450" y="160" text-anchor="middle" font-size="11">Looker Studio, Python, Git</text>

        <!-- Arrow -->
        <path d="M570 150 L600 150" stroke="#d4910b" stroke-width="2"/>

        <!-- Senior level box -->
        <rect x="650" y="100" width="100" height="100" rx="8" fill="#1e3a5f" stroke="#d4910b" stroke-width="2"/>
        <text x="700" y="140" text-anchor="middle" font-size="14" font-weight="bold" fill="white">₱100k+</text>
        <text x="700" y="160" text-anchor="middle" font-size="10" fill="white">Multi-tool fluency</text>
      </svg>
    </div>
  </section>

  <!-- Salary band comparison table -->
  <section class="mb-12">
    <h2>Salary Band Comparison</h2>
    <table class="w-full bg-white rounded-xl shadow-md overflow-hidden">
      <thead class="bg-dep-blue text-white">
        <tr>
          <th class="p-3 text-left">Salary Band</th>
          <th class="p-3 text-left">SQL</th>
          <th class="p-3 text-left">Python</th>
          <th class="p-3 text-left">Tableau</th>
          <th class="p-3 text-left">Looker Studio</th>
        </tr>
      </thead>
      <tbody>
        <tr class="border-b"><td class="p-3">₱35k and below</td><td class="p-3">45.2%</td><td class="p-3">38.7%</td><td class="p-3">12.3%</td><td class="p-3">8.1%</td></tr>
        <tr class="border-b bg-dep-lightgold/30"><td class="p-3">₱75k–₱100k</td><td class="p-3">62.1%</td><td class="p-3">55.4%</td><td class="p-3">28.9%</td><td class="p-3">15.7%</td></tr>
        <tr><td class="p-3">₱100k+</td><td class="p-3">76.9%</td><td class="p-3">73.6%</td><td class="p-3">38.0%</td><td class="p-3">17.7%</td></tr>
      </tbody>
    </table>
    <p class="text-xs text-dep-slate mt-2">Source: DEP State of the Community Survey 2026 (n=1,861)</p>
  </section>

  <!-- Tool cards -->
  <section class="mb-12">
    <h2>Tool Deep Dives</h2>
    <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
      <div class="bg-white rounded-xl shadow-md p-6 border-l-4 border-dep-gold">
        <h3 class="font-semibold mb-2">Power BI</h3>
        <p class="text-sm text-dep-slate mb-3">Best for: Entry-level data roles in PH companies</p>
        <a href="#" class="text-dep-gold font-semibold text-sm">Free Resources →</a>
      </div>
      <!-- Repeat for Looker Studio, Python, Tableau -->
    </div>
  </section>

  <!-- "One BI Tool" validation -->
  <section class="mb-12">
    <h2>Why "Master One BI Tool" Is Only Half Right</h2>
    <div class="bg-white rounded-xl shadow-md p-6 border-l-4 border-dep-gold">
      <p class="mb-4">For entry-level positioning, mastering one BI tool (Power BI or Tableau) is correct advice. But the data shows ₱100k+ earners demonstrate multi-tool fluency:</p>
      <ul class="list-disc list-inside space-y-2 text-sm text-dep-slate">
        <li>38.0% of ₱100k+ earners use Tableau (vs 12.3% at entry level)</li>
        <li>17.7% use Looker Studio (vs 8.1% at entry level)</li>
        <li>73.6% use Python tools (vs 38.7% at entry level)</li>
      </ul>
    </div>
  </section>
</main>
```

**Content checklist:**
- [ ] Collect salary band tool proficiency data from survey
- [ ] Create SVG roadmap diagram
- [ ] Write tool deep-dive cards (Power BI, Looker Studio, Python, Tableau)
- [ ] Find free learning resources for each tool
- [ ] Write "one BI tool" validation explanation

---

### Feature 6: Git/GitHub Adoption Guide

**File:** `git-guide/index.html`

**Structure:**
```html
<main class="max-w-[1120px] mx-auto px-4 py-16">
  <h1>Git/GitHub Adoption Guide</h1>
  <p>Step-by-step guide for data engineers to adopt version control (only 48.8% currently use it).</p>

  <!-- GitHub basics -->
  <section class="space-y-6">
    <details class="bg-white rounded-xl shadow-md overflow-hidden" open>
      <summary class="p-4 font-semibold cursor-pointer flex items-center gap-2">
        Step 1: Create Your GitHub Account & First Repo
      </summary>
      <div class="p-4 border-t space-y-4">
        <ol class="list-decimal list-inside space-y-2 text-sm">
          <li>Go to github.com and create a free account</li>
          <li>Click "New Repository" → name it (e.g., my-first-data-project)</li>
          <li>Check "Add a README file" and click "Create repository"</li>
        </ol>

        <div class="bg-dep-lightgold p-4 rounded-lg border-l-4 border-dep-gold">
          <pre><code># My First Data Project<br/>A simple data analysis project using Python and pandas.<br/><br/>## Tools Used<br/>- Python 3.x<br/>- pandas<br/>- Jupyter Notebook</code></pre>
          <button onclick="copyCode(this)" class="mt-2 text-sm text-dep-gold font-semibold">Copy README Template →</button>
        </div>
      </div>
    </details>

    <!-- Repeat for Steps 2–5 -->
    <!-- Step 2: Clone a repo and make changes -->
    <!-- Step 3: Create a branch -->
    <!-- Step 4: Commit and push -->
    <!-- Step 5: Pull requests workflow -->
  </section>

  <!-- Branching strategies -->
  <section class="mt-12">
    <h2>Branching Strategies</h2>
    <div class="bg-white rounded-xl shadow-md p-6 border-l-4 border-dep-gold">
      <pre><code># Feature branch workflow (recommended for beginners)<br/>git checkout -b feature/add-sql-query<br/># make changes<br/>git add .<br/>git commit -m "feat: add customer segmentation query"<br/>git push origin feature/add-sql-query</code></pre>
    </div>
  </section>

  <!-- Commit conventions -->
  <section class="mt-12">
    <h2>Commit Conventions</h2>
    <table class="w-full bg-white rounded-xl shadow-md overflow-hidden">
      <thead class="bg-dep-blue text-white">
        <tr><th class="p-3 text-left">Prefix</th><th class="p-3 text-left">When to Use</th></tr>
      </thead>
      <tbody>
        <tr class="border-b"><td class="p-3 font-mono text-sm">feat:</td><td class="p-3 text-sm">New feature or module</td></tr>
        <tr class="border-b bg-dep-lightgold/30"><td class="p-3 font-mono text-sm">fix:</td><td class="p-3 text-sm">Bug fix or correction</td></tr>
        <tr class="border-b"><td class="p-3 font-mono text-sm">docs:</td><td class="p-3 text-sm">Documentation changes</td></tr>
        <tr><td class="p-3 font-mono text-sm">refactor:</td><td class="p-3 text-sm">Code restructuring without behavior change</td></tr>
      </tbody>
    </table>
  </section>

  <!-- Portfolio showcase guide -->
  <section class="mt-12">
    <h2>Portfolio Showcase Guide</h2>
    <div class="bg-white rounded-xl shadow-md p-6 border-l-4 border-dep-gold">
      <h3 class="font-semibold mb-3">What Makes a Great GitHub Portfolio</h3>
      <ul class="space-y-2 text-sm text-dep-slate">
        <li>✓ Clear README with project description, tools used, and results</li>
        <li>✓ At least 2–3 complete projects (not just tutorials)</li>
        <li>✓ Clean file structure with organized folders</li>
        <li>✓ Code comments explaining key logic</li>
        <li>✓ Link to GitHub in your LinkedIn "Featured" section</li>
      </ul>
    </div>
  </section>
</main>

<script>
  function copyCode(btn) {
    const code = btn.previousElementSibling.textContent;
    navigator.clipboard.writeText(code);
    btn.textContent = 'Copied!';
    setTimeout(() => btn.textContent = 'Copy README Template →', 2000);
  }
</script>
```

**Content checklist:**
- [ ] Write step-by-step GitHub setup instructions
- [ ] Create 5+ code examples (git init, git branch, git commit, git push, PR workflow)
- [ ] Write README template for portfolio projects
- [ ] Create branching strategy diagram
- [ ] Write commit conventions table
- [ ] Write portfolio showcase guide

---

## File Structure After Implementation

```
community-hub/
├── docs/
│   └── index.html              ← Main hub (existing)
├── modules/
│   ├── sql-basics.html         ← AI-Augmented Learning Module 1
│   ├── python-fundamentals.html← AI-Augmented Learning Module 2
│   └── excel-powerbi-intro.html← AI-Augmented Learning Module 3
├── pathway/
│   ├── index.html              ← Career Shifter DA/DE Pathway
│   └── checklist.html          ← Printable checklist with progress tracking
├── mentorship/
│   └── index.html              ← Time-Bound Mentorship Matching
├── linkedin/
│   └── index.html              ← LinkedIn Profile Optimizer
├── fluency-map/
│   └── index.html              ← Multi-Tool Fluency Map
├── git-guide/
│   └── index.html              ← Git/GitHub Adoption Guide
├── SPEC.md                     ← Main specification
└── IMPLEMENTATION-PLAN.md      ← This file
```

**Total files:** 10 HTML files (1 hub + 9 feature pages)
**Total lines of content:** ~5,000–6,000 lines across all files
**External dependencies:** Tailwind CDN + Google Fonts + YouTube iframe embeds + Google Forms embeds

---

## Implementation Timeline (Estimated)

| Week | Feature | Effort |
|---|---|---|
| 1–2 | AI-Augmented Learning Modules (3 pages) | 40 hours (content writing + design) |
| 2–3 | Career Shifter DA/DE Pathway (2 pages) | 30 hours |
| 3–4 | Time-Bound Mentorship Matching (1 page) | 20 hours |
| 4–5 | LinkedIn Profile Optimizer (1 page) | 25 hours |
| 5–6 | Multi-Tool Fluency Map (1 page) | 20 hours |
| 6–7 | Git/GitHub Adoption Guide (1 page) | 25 hours |

**Total: ~7 weeks, ~160 hours across 3–4 volunteer contributors.**
