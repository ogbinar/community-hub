# Prototype Design Plan — Data Engineering Pilipinas Community Hub

## Executive Summary

This document outlines the design plan for the **MVP prototype** of the Data Engineering Pilipinas (DEP) Community Hub. The prototype targets **Students and Job Seekers** (55.7% of community) with three core features designed to narrow the income mobility gap from ₱35k → ₱100k+.

All insights are grounded in the **DEP State of the Community Survey 2026** (n=1,861 respondents, 95% confidence, 96.6% Philippines-based).

---

## 1. Target Audience & Rationale

### Primary Users: Students + Job Seekers (Combined 55.7% of Community)

| Segment | Share | Key Stat | Why They're First |
|---|---|---|---|
| **Students** | 34.5% (n=642) | 81.6% want upskilling; 65.8% use AI daily for study | Largest segment; time-rich; highest motivation-to-enroll ratio |
| **Job Seekers** | 21.2% (n=394) | 86.9% want upskilling — highest of any segment | Second largest; actively seeking employment; need portfolio proof |

### Secondary Users: Career Shifters (18.9%, n=352)
- 58.5% have NO computing degree; 66.5% earn ≤₱35k
- Included in the pathway feature but not the primary launch audience

### Rationale for Targeting Students + Job Seekers First

1. **Largest combined segment:** 55.7% of the entire community — immediate impact on more than half the community
2. **Highest motivation-to-enroll ratio:** 86.9% of Job Seekers and 81.6% of Students want upskilling — highest conversion potential
3. **Lowest switching cost:** Time-rich, lowest opportunity cost — easiest to activate with low-cost programs
4. **AI-native generation:** 65.8% use AI daily for study — they already internalize AI as a learning medium
5. **Survey validation:** "Target Students first (34.5% of community; 81.6% want upskilling). Time-rich, motivation-high, lowest switching cost."

---

## 2. Core Features & Minimal Viable Implementation

### Feature 1: AI-Augmented Learning Modules (Score: 9.3/10)

**What it is:** A series of short, interactive lessons that teach learners how to use AI as a study tool — not for getting answers, but for interrogating them. Each module follows this structure:
- Concept explanation (5-minute YouTube video)
- AI-generated answer example
- "Where AI gets it wrong" breakdown
- How a practitioner validates the answer

**Minimal viable version:**
- 3 modules covering SQL basics, Python fundamentals, and Excel/Power BI intro
- Each module delivered as a 5-minute YouTube video + accompanying GitHub Gist with code examples
- Discord thread for Q&A per module
- No login required — open access to all DEP members

**User experience:**
- Learner watches YouTube video → reads accompanying GitHub Gist → tries exercises in their own laptop → posts questions in Discord thread → gets answered by volunteer mentor within 24 hours
- Feels like a **self-paced bootcamp with human support**, not just passive video watching

### Feature 2: Career Shifter DA/DE Pathway (Score: 9.0/10)

**What it is:** An 8-week structured sprint with clear milestones, designed specifically for career shifters who have no computing degree. The pathway covers:
- Week 1-2: SQL basics + Excel/Power Query
- Week 3-4: Power BI fundamentals + DAX basics
- Week 5-6: Python pandas + data manipulation
- Week 7-8: Cloud deployment basics (AWS/Azure free tier) + GitHub portfolio setup

**Minimal viable version:**
- 8 weekly Discord check-in threads with milestone assignments
- One volunteer mentor per cohort (time-bound commitment: 2 hours/week)
- DEP-branded digital badge for completion (shareable on LinkedIn)
- No paid tools required — all learning uses free/open-source tools

**User experience:**
- Learner joins a cohort → receives weekly assignment via Discord → completes exercise using free tools → posts progress in check-in thread → gets feedback from volunteer mentor → earns DEP-branded badge at completion
- Feels like a **structured, time-bound cohort with accountability**, not an open-ended self-study program

### Feature 3: LinkedIn Profile Optimizer (Score: 8.7/10)

**What it is:** An interactive checklist that walks learners through optimizing their LinkedIn profile for data roles. It includes:
- Project-rich GitHub linking guide
- Certification badge display instructions
- Skill endorsement strategies
- Headline optimization template
- AI-assisted content generation for profile sections (using free Gemini API)

**Minimal viable version:**
- One-page Google Doc checklist with step-by-step instructions
- AI-assisted section writing using free Gemini API (no login required, just copy-paste prompts)
- Before/after LinkedIn profile examples
- Optional: 30-minute Discord office hours for profile review

**User experience:**
- Learner downloads the checklist → follows each step → uses AI prompts to draft profile sections → posts their "before" and "after" LinkedIn profiles in Discord for peer feedback → gets reviewed by volunteer mentor during office hours
- Feels like a **guided, interactive workshop**, not a static PDF

---

## 3. User Experience Design

### Core Experience Principles (From Survey Data)

1. **YouTube-first delivery:** "65.8% of community learns via YouTube. Host modules as YouTube content; Discord threads for Q&A."
2. **Discord accountability cohorts:** "46.9% use Discord; 66.2% of Students (56.7% JobSeekers, 16.2% Professionals, 35.1% Career Shifters). Weekly Discord check-ins are zero-cost, high-impact for completion."
3. **DEP-branded certification:** "DEP-branded certification: shareable on LinkedIn. Directly activates career advancement motivation (75.3%)."
4. **8-week sprint format:** "Reduces drop-off risk for career-motivated learners (75.3%) by creating bounded milestones."
5. **AI as co-creator in curriculum:** "DEP should be ready to leverage AI as a co-creator in the curriculum, not just a topic within it."

### User Journey: "Maya" the Student Learner

**Week 1: Onboarding**
- Maya sees a post in the DEP Facebook group about the new "AI-Augmented Learning Modules"
- She clicks the link → goes to YouTube → watches the first 5-minute SQL basics video
- She reads the accompanying GitHub Gist → tries the exercises on her laptop
- She posts her question in the Discord thread → gets answered by a volunteer mentor within 2 hours
- **Feels like:** "Finally, someone explained this in a way I understand. And there's a real person helping me!"

**Week 2-3: Building Momentum**
- Maya watches the Python fundamentals video → tries exercises → posts questions in Discord
- She joins the Career Shifter DA/DE Pathway cohort (she identifies as a career shifter)
- She receives her Week 1 assignment via Discord → completes it → posts progress in check-in thread
- She gets feedback from her volunteer mentor → feels encouraged
- **Feels like:** "I'm actually making progress. The weekly check-ins keep me accountable."

**Week 4-6: Portfolio Building**
- Maya watches the Power BI + DAX basics videos → builds a small dashboard using Google Sheets data
- She uses the LinkedIn Profile Optimizer checklist → updates her profile with her new projects
- She posts her "before" and "after" LinkedIn profiles in Discord → gets peer feedback
- **Feels like:** "I have something tangible to show employers. My LinkedIn finally looks professional."

**Week 7-8: Completion & Recognition**
- Maya completes the 8-week sprint → earns her DEP-branded digital badge
- She shares it on LinkedIn → gets her first interview callback
- **Feels like:** "I did it. I have a credential, a portfolio, and a job interview. This program actually works."

### User Journey: "Jose" the Job Seeker

**Week 1: Onboarding**
- Jose sees the LinkedIn Profile Optimizer checklist → downloads it immediately
- He follows each step → uses AI prompts to draft his profile sections
- He posts his "before" and "after" profiles in Discord → gets reviewed by a volunteer mentor
- **Feels like:** "My LinkedIn finally looks like someone who knows what they're doing."

**Week 2-3: Learning Pathway**
- Jose joins the Career Shifter DA/DE Pathway cohort (he's actively seeking employment)
- He completes Week 1 SQL assignment → posts progress in Discord check-in thread
- He gets feedback from his volunteer mentor → feels motivated to continue
- **Feels like:** "I'm not just watching videos anymore. I'm actually building skills."

**Week 4-6: Portfolio Development**
- Jose builds a small SQL + Python project using free tools (SQLite, pandas, GitHub)
- He uses the AI-Augmented Learning Modules to debug his code → learns how to interrogate AI outputs
- He adds the project to his GitHub → links it from his LinkedIn profile
- **Feels like:** "I have a real project on my portfolio. This is what employers want to see."

**Week 7-8: Job Application**
- Jose completes the 8-week sprint → earns his DEP-branded digital badge
- He updates his LinkedIn with the new credential → starts applying to jobs
- He uses the GitHub Portfolio Showcase Guide to structure his repo properly
- **Feels like:** "I'm finally ready to apply. I have a portfolio, a credential, and a clear path forward."

---

## 4. Technical Architecture & Stack

### Core Stack (All Free/Open-Source)

| Component | Tool | Cost | Rationale |
|---|---|---|---|
| **Video Delivery** | YouTube | Free | 65.8% of community learns via YouTube |
| **Code Examples** | GitHub Gists | Free | Open-source, version-controlled, easy to share |
| **Community & Q&A** | Discord | Free (free tier) | 46.9% use Discord; 66.2% of Students use it |
| **Scheduling** | Google Calendar | Free | No paid calendar tools required |
| **Checklist/Docs** | Google Docs | Free | Collaborative, shareable, zero cost |
| **AI Assistance** | Gemini API (free tier) | Free | No paid AI tools required |
| **Badge/Certification** | Canva (free tier) + GitHub Pages | Free | Shareable on LinkedIn, no login required |
| **Tracking** | GitHub Issues | Free | Zero-cost issue tracking for volunteer mentors |

### User Flow Diagram

```
Facebook Group Post
       ↓
YouTube Video (5-min module)
       ↓
GitHub Gist (code examples)
       ↓
Discord Thread (Q&A + check-ins)
       ↓
Volunteer Mentor Feedback (24-48 hours)
       ↓
DEP-Branded Badge (completion)
       ↓
LinkedIn Share (career advancement)
```

### Volunteer Mentor Flow

```
Sign Up (Google Form)
       ↓
Assign Cohort (GitHub Issues)
       ↓
Weekly Check-in (Discord Thread)
       ↓
Review Submissions (GitHub Gists)
       ↓
Provide Feedback (Discord Comments)
       ↓
Track Progress (GitHub Issues)
```

---

## 5. Success Metrics & Measurement

Based on survey data, here are the measurable targets:

| Metric | Target | Measurement Method |
|---|---|---|
| **Module completion rate** | 70%+ of enrolled Students/Job Seekers complete all 3 AI modules | Discord check-in participation + GitHub submission tracking |
| **Pathway completion rate** | 60%+ of Career Shifters complete the 8-week sprint | Discord check-in participation + badge issuance tracking |
| **LinkedIn profile optimization** | 50%+ of Job Seekers optimize their LinkedIn profiles within first 2 weeks | Self-reported in Discord office hours + peer review submissions |
| **Volunteer mentor retention** | 80%+ of volunteer mentors complete at least one cohort cycle | GitHub Issues tracking + Discord participation |
| **Job application success rate** | 20%+ improvement in interview callback rate for participants | Survey follow-up at 3 months post-completion |

---

## 6. Out of Scope (Explicitly Excluded)

To keep the MVP lean and sustainable, these features are explicitly excluded from the first prototype:

1. **Complex dashboards** — No custom-built analytics dashboards; use GitHub Issues + Discord threads for tracking
2. **Paid AI tools** — No ChatGPT Plus, no Copilot subscriptions; use free Gemini API tier
3. **Enterprise BI tools** — No Tableau, no Alteryx; use Power BI Desktop (free) + Looker Studio (free)
4. **Cloud infrastructure costs** — No AWS/Azure/GCP paid tiers; use free tiers only ($100/$200/$300 credits)
5. **Custom web application** — No React/Next.js app; use existing platforms (YouTube, Discord, GitHub, Google Docs)

---

## 7. Implementation Timeline & Next Steps

### Phase 1: Build Assets (Weeks 1-4)
1. Create 3 AI-Augmented Learning Modules (SQL, Python, Excel/Power BI) as YouTube videos + GitHub Gists
2. Set up Discord server with cohort channels, check-in threads, and mentor assignment workflows
3. Build LinkedIn Profile Optimizer checklist as a Google Doc with AI-assisted prompts
4. Recruit 5 volunteer mentors via Google Form + GitHub Issues tracking

### Phase 2: Launch First Cohort (Weeks 5-8)
1. Announce launch in DEP Facebook group + Discord
2. Onboard first cohort of Students + Job Seekers
3. Begin Week 1 assignments + check-ins
4. Monitor participation + feedback daily

### Phase 3: Iterate & Scale (Weeks 9-12)
1. Collect completion data + participant feedback
2. Refine modules based on Q&A patterns in Discord
3. Adjust mentor assignments + check-in workflows
4. Prepare for second cohort expansion

---

## 8. Key Design Principles Summary

1. **YouTube-first delivery** — "65.8% learn via YouTube; host modules as YouTube content, Discord threads for Q&A"
2. **Discord accountability cohorts** — "46.9% use Discord; weekly check-ins are zero-cost, high-impact for completion"
3. **DEP-branded certification** — "Shareable on LinkedIn; directly activates career advancement motivation (75.3%)"
4. **8-week sprint format** — "Reduces drop-off risk; creates bounded milestones; makes volunteer teaching sustainable"
5. **AI as co-creator in curriculum** — "Teach learners how to use AI as a study tool — not for answers, but to interrogate them"

---

## Next Steps

1. **Create the 3 AI-Augmented Learning Modules** (YouTube videos + GitHub Gists)
2. **Set up the Discord server structure** (cohort channels, check-in threads, mentor workflows)
3. **Build the LinkedIn Profile Optimizer checklist** (Google Doc + AI prompts)
4. **Recruit volunteer mentors** (Google Form + GitHub Issues tracking)
5. **Launch first cohort** → track completion rates in Discord/GitHub

Would you like to proceed with building the actual prototype assets?
