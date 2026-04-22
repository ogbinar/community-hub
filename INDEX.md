# Data Engineering Pilipinas — Community Hub Project Index

## Project Overview

This project documents the **Design Thinking process** for building a Community Hub for **Data Engineering Pilipinas (DEP)**, the Philippines' largest data community (~40,000+ Facebook members).

All insights are grounded in the **DEP State of the Community Survey 2026** (n=1,861 respondents, 95% confidence, 96.6% Philippines-based).

---

## Document Map

| Stage | Document | Description |
|---|---|---|
| **Empathize** | [empathize-plan.md](./empathize-plan.md) | Original research plan with interview guides and survey frameworks for all 8 profiles |
| **Empathize** | [empathize-augmented.md](./empathize-augmented.md) | Augmented empathy research with real community data from GitHub, survey results, and website analysis |
| **Define** | [personas-and-hmws.md](./personas-and-hmws.md) | Master personas document with 8 user personas and corresponding "How Might We" statements |
| **Define** | [personas/README.md](./personas/README.md) | Quick reference index linking to all 8 individual persona documents |
| **Define** | [personas/01-student-learner.md](./personas/01-student-learner.md) | Maya (Student) — 34.5% of community; 65.8% use AI daily for study |
| **Define** | [personas/02-job-seeker.md](./personas/02-job-seeker.md) | Jose (Job Seeker) — 21.2% of community; 86.9% want upskilling |
| **Define** | [personas/03-career-shifter.md](./personas/03-career-shifter.md) | Lia (Career Shifter) — 18.9% of community; 58.5% have NO computing degree |
| **Define** | [personas/04-data-analyst-professional.md](./personas/04-data-analyst-professional.md) | Rico (Data Analyst) — ₱75k-₱100k bottleneck at 9.1%; multi-tool fluency needed |
| **Define** | [personas/05-data-engineer.md](./personas/05-data-engineer.md) | Kai (Data Engineer) — 39% earn ₱100k+; Git/GitHub only 48.8% adoption |
| **Define** | [personas/06-content-creator.md](./personas/06-content-creator.md) | Sandy (Creator) — YouTube awareness at 24.6% vs 65.8% learn via YouTube |
| **Define** | [personas/07-corporate-manager.md](./personas/07-corporate-manager.md) | David (Corporate Pro) — 15.1% willing to mentor; team size + remote work = satisfaction drivers |
| **Define** | [personas/08-overseas-filipino.md](./personas/08-overseas-filipino.md) | Ana (Overseas Filipino) — 96.6% Philippines-based; 83.5% Metro Manila/Luzon concentrated |
| **Define** | [profile-insights-alignment.md](./profile-insights-alignment.md) | Direct alignment between survey data and profile assumptions; gap analysis |
| **Ideate** | [ideate-results.md](./ideate-results.md) | 40+ feature ideas across all 8 personas, Pareto-ranked (top 20% = 8 features), open-source/reframed versions included |

---

## Key Findings Summary

### Community Composition
- **Students** (34.5%, n=642) — Largest segment; 65.8% use AI daily for study
- **Job Seekers** (21.2%, n=394) — 86.9% want upskilling; highest motivation-to-enroll ratio
- **Career Shifters** (18.9%, n=352) — 58.5% have NO computing degree; 66.5% earn ≤₱35k
- **Data Professionals** (19.6%, n=364) — 65.3% use AI daily for work; ₱75k-₱100k bottleneck at 9.1%
- **Freelance/Gov/Volunteer** (5.9%, n=109) — Niche segment including community contributors

### Core Pain Points (Quantified)
1. **Resource overload:** Students learn via YouTube (65.8%), DataCamp (49.3%), GitHub (37.1%) — but no clear path
2. **Salary bottleneck:** Only 9.1% of Professionals earn ₱75k-₱100k; structural ceiling requiring deliberate upskilling
3. **AI adoption gap:** Career Shifters only 50.2% use AI daily for work (vs 65.3% Professionals)
4. **Portfolio gap:** No clear guidance on what projects actually impress hiring managers
5. **DAX knowledge gap:** Only 2.2% of Students use DAX vs 29.1% of DA Professionals

### Top 8 MVP Features (Pareto: 20% of features → 80% of impact)
1. **AI-Augmented Learning Modules** (9.3/10) — YouTube-first; Discord Q&A threads
2. **Career Shifter DA/DE Pathway** (9.0/10) — 8-week sprint; volunteer-taught live sessions
3. **Power BI Gap Closer** (8.8/10) — Targeted module closing the 25-point gap
4. **Time-Bound Mentorship Matching** (8.7/10) — ADPList-style booking system
5. **LinkedIn Profile Optimizer** (8.7/10) — Interactive checklist + AI-assisted content generation
6. **Multi-Tool Fluency Map** (8.3/10) — Visual roadmap for ₱75k-₱100k bottleneck
7. **Git/GitHub Adoption Guide** (8.3/10) — Step-by-step guide to close 48.8% gap
8. **Cross-Promotion Network** (8.2/10) — Directory of creators with links to YouTube/GitHub/LinkedIn

### Key Design Principles (From Survey Data)
1. **YouTube-First Delivery** — "65.8% learn via YouTube; host modules as YouTube content, Discord threads for Q&A"
2. **Discord Accountability Cohorts** — "46.9% use Discord; weekly check-ins are zero-cost, high-impact for completion"
3. **DEP-Branded Certification** — "Shareable on LinkedIn; directly activates career advancement motivation (75.3%)"
4. **8-Week Sprint Format** — "Reduces drop-off risk; creates bounded milestones; makes volunteer teaching sustainable"
5. **AI as Co-Creator in Curriculum** — "Teach learners how to use AI as a study tool — not for answers, but to interrogate them"

---

## Data Sources

1. **DEP State of the Community Survey 2026** (n=1,861) — https://sandygcabanes.github.io/2025-2026-DEP-State-of-the-Community-Survey-Results/
2. **GitHub API** — 19 core contributors mapped with repos, stars, languages, and expertise areas
3. **Community website** dataengineering.ph — full content structure and programs analyzed
4. **Empathize research** — Interview guides, survey frameworks, empathy maps for all 8 profiles

---

## Next Steps

1. **Prototype stage** — Build low-fidelity versions of the top 5 MVP features:
   - Figma wireframe of AI-Augmented Learning Modules page
   - Notion template for Career Shifter DA/DE Pathway
   - Discord bot prototype for Time-Bound Mentorship Matching
   - Google Form mockup for LinkedIn Profile Optimizer checklist
   - GitHub README template for Git/GitHub Adoption Guide

2. **Test with real users** — Put prototypes in front of Maya, Jose, Lia, Rico, and Kai from the community
3. **Iterate** — Gather feedback, refine features, rebuild, retest

---

## Contact

Project maintained by the Data Engineering Pilipinas community leadership team.  
Survey compiled by: [Sandy G. Cabanes](https://www.linkedin.com/in/sandygcabanes)  
Community founder: [Myk Ogbinar](https://github.com/ogbinar)
