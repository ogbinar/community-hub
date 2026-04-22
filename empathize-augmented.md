# Empathize Step — Augmented Community Profiles for Data Engineering Pilipinas

## Research Basis

This document augments the original empathy research plan with **real community data** sourced from:

1. **DEP State of the Community Survey 2026** (n=1,861 respondents, 95% confidence, 96.6% Philippines-based) — compiled by Sandy G. Cabanes
2. **GitHub contributors** to the DataEngineeringPilipinas repository (19 core contributors tracked)
3. **Community website** dataengineering.ph (Quarto-built, vetiver theme)
4. **Facebook group** (~40,000+ members)
5. **Discord**, YouTube, and other community channels

---

## Community Snapshot (from 2026 Survey)

| Metric | Value |
|---|---|
| Total respondents | 1,861 |
| Philippines-based | 96.6% |
| Under age 30 | 75% (44% aged 20-24; 29.7% aged 25-29) |
| Metro Manila / Luzon | 83.5% |
| Bachelor's or above | 89.8% |
| Use AI daily/weekly for work | 74.4% |
| Use AI daily/weekly for study | 80.8% |
| Employed earning ≤₱35k/month | 48.3% |
| Engaged with DataCamp scholarship | 89.6% |

---

## Profile 1: Students 🎓

### Demographics (from survey)
- **Share of community:** 34.5% (n=642) — the single largest segment
- **Age:** Predominantly 20-24 (44% of all respondents)
- **Education:** 89.8% Bachelor's level or above overall; students currently enrolled
- **Location:** 83.5% Metro Manila / Luzon

### Real Data Points
- **65.8%** use AI tools daily for study — highest adoption of any segment
- **642** respondents, making them the largest single group
- **Learning tools:** YouTube (65.8%), DataCamp (49.3%), GitHub (37.1%)
- **AI tools used:** ChatGPT (86.6%), Gemini (68.2%), Copilot (45.2%), Claude (42.8%)
- Over-index on GitHub Copilot (24.7% vs 13.6% of those seeking work)
- **Hardware:** 84.5% use laptop as primary; only 0.8% have access to workstation

### Key Motivations
- Upskill acquisition (81.6% want upskilling)
- Career advancement (75.3% overall)
- Continued learning (78.5%)

### Pain Points (Evidence-Backed)
- **Resource gap:** DataTalks.Club DE Zoomcamp used by only 1.0% — high quality but requires cloud resources/powerful machines
- **Hardware bottleneck:** 84.5% rely on laptop; DE workloads need higher RAM and compute
- **DAX knowledge gap:** Only 2.2% of Students use DAX vs 29.1% of DA Professionals — a high-value skill they're missing
- **Google Sheets vs Excel:** 49.7% use Google Sheets, but employers expect Excel proficiency (71.3%)
- **AI dependency risk:** AI is "the medium through which they learn" — need to teach deep learning via AI, not shallow completion

### Community Leaders Who Resonate With This Profile
- **Sandy G. Cabanes** (@SandyGCabanes) — Certified Data Analyst & Associate Data Engineer; runs DEP survey and DE pipeline projects
- **Sandy Lauguico** (@sclauguico) — YouTube content creator, data science educator; 46 GitHub followers, 74 repos
- **Nicksy Molms** (@nextcm) — Civil & Structural Engineer learning Python; documents learning journey publicly

### Empathy Map (Augmented with Data)
| Says | Thinks/Feels | Does |
|---|---|---|
| "YouTube is where I learn" | Overwhelmed by the gap between tutorial and real-world projects | Watches 65.8% of learning content on YouTube passively |
| "Is AI cheating if I use it?" | Anxious about academic integrity vs practical necessity | Uses ChatGPT (86.6%) and Gemini (68.2%) daily for study |
| "I don't have a powerful machine" | Frustrated by hardware limitations blocking DE workloads | Relies on cloud free tiers but doesn't know which ones to use |

---

## Profile 2: Job Seekers 💼

### Demographics (from survey)
- **Share of community:** 21.2% (n=394) — second largest segment
- **Combined with Students:** 55.7% of the entire community is in the "talent pipeline"
- **Motivation:** 86.9% want upskilling — highest motivation-to-enrollment ratio

### Real Data Points
- **86.9%** want upskilling (highest of any segment)
- Actively seeking jobs; not yet in data roles
- Primary job search platform: LinkedIn (varies by background)

### Key Motivations
- Career advancement (75.3% overall driver)
- Direct path to employment
- Portfolio building and proof of skills

### Pain Points (Evidence-Backed)
- **LinkedIn is not optional:** 74.4% of employed professionals use LinkedIn for job discovery — must build complete, project-rich profiles
- **Portfolio gap:** No clear guidance on what projects actually impress hiring managers
- **DAX knowledge gap:** Only 2.2% of Students use DAX vs 29.1% of DA Professionals — signals a high-value upskill opportunity they're missing
- **Hardware bottleneck:** Same as students; laptop-only limits DE project depth
- **Low awareness of free resources:** DataCamp (49.3%), GitHub (25.8%) — but Microsoft Learn at 8.6%, Google Cloud Skills Boost at 2.3% are severely under-utilized

### Empathy Map (Augmented with Data)
| Says | Thinks/Feels | Does |
|---|---|---|
| "I don't know what projects to build" | Uncertain if their portfolio is competitive | Builds tutorial clones, doesn't know how to make them stand out |
| "LinkedIn is where jobs are found" | Anxious about profile completeness | Applies blindly, gets ghosted; needs project-rich GitHub + LinkedIn combo |

---

## Profile 3: Career Shifters 🔄

### Demographics (from survey)
- **Share of community:** 18.9% (n=352)
- **58.5%** have NO computing degree — non-CS backgrounds dominate
- **66.5%** earn ₱35k or below — disproportionately concentrated at the entry floor

### Real Data Points
- **58.5%** have no computing degree (vs 41.5% who do)
- **66.5%** earn ≤₱35k/month — highest concentration at entry salary level
- **86.3%** with high motivation to upskill
- **62.5%** are still in the "decision to shift" phase — not fully committed yet
- **AI lag:** Only 50.2% use AI daily for work (vs 65.3% Professionals); 15.4% use AI monthly or less; 3.4% say they don't plan to use AI (highest refusal rate)
- **Facebook usage:** 27.0% discover jobs via Facebook vs 15.2% of Professionals

### Key Motivations
- Decision-to-shift support (62.5%) — still weighing the choice
- Upskill acquisition (86.3%)
- Career advancement (75.3%)

### Pain Points (Evidence-Backed)
- **No recognized credential:** Non-CS background feels like a liability to employers
- **Salary trap:** 66.5% earn ≤₱35k; lowest satisfaction profile (72.9% score 1-5 on satisfaction)
- **AI adoption lag:** Significantly behind Professionals and Students in daily AI usage for work
- **Hardware-to-cloud bridge gap:** Learn locally but don't know how to deploy to cloud — need "Local to Cloud Bridge" curriculum
- **GCP vs AWS/Azure mismatch:** 60.7% use GCP (higher than DE Pros at 26.8%) — may be using free tiers but industry expects AWS/Azure

### Empathy Map (Augmented with Data)
| Says | Thinks/Feels | Does |
|---|---|---|
| "I don't have a CS degree" | Imposter syndrome; comparing to computing-degree peers | Spends hours on free resources, feels stuck at entry level |
| "How do I prove I can do this?" | Anxious about job market readiness and salary expectations | Builds tutorials but doesn't know how to showcase them professionally |

---

## Profile 4: Data Professionals 🏢

### Demographics (from survey)
- **Share of community:** 19.6% (n=364)
- **88.4%** hold a Bachelor's degree; 7.4% hold a Master's
- **45.2%** are Data Analysts specifically
- **65.3%** use AI daily for work — highest of any segment

### Real Data Points
- **Salary profile:** Skewed — 31.0% earn ₱15k-₱35k; 38.5% earn ₱35k-₱75k (modal band); 9.1% earn ₱75k-₱100k (thin bottleneck); 21.4% earn ₱100k+
- **Tool sophistication at ₱100k+:** SQL (76.9%), Python (73.6%), Tableau (38.0%), Alteryx (10.1%), Qlik Sense (8.9%) — multi-tool fluency separates high earners
- **Cloud usage:** AWS 45.2%, Azure 49.1% — near-equal dominance
- **Side gig prevalence:** 22.2% had a side gig in past 12 months (~1 in 5)
- **Median tenure at current salary:** 1-2 year band (27.4%)
- **Master's holders:** 4× more common at ₱75k-₱100k (15.4% vs 3.9%); 18.6% at ₱100k+ (vs 4.9% overall) — but 84.6% of ₱100k+ earners do NOT have a Master's

### Key Motivations
- Moving to next salary band (structural bottleneck at ₱75k-₱100k)
- Multi-tool fluency and specialization
- AI workflow optimization (not just using AI, but knowing which tool for which task)

### Pain Points (Evidence-Backed)
- **The ₱75k-₱100k bottleneck:** Only 9.1% of Professionals sit here — a structural ceiling that requires deliberate upskilling to break through
- **"Master one BI tool" advice is only half-right:** Correct for entry-level, but ₱100k+ earners show multi-tool fluency (Power BI + Tableau + Looker Studio + Python tools)
- **AI is mainstream, not differentiating:** 65.3% use AI daily — the edge now lies in *how* you use AI (audit outputs, security, accuracy, cost)
- **Master's degree premium exists but isn't automatic:** Helps at ₱75k-₱100k and above, but only when combined with strong practical skills

### Empathy Map (Augmented with Data)
| Says | Thinks/Feels | Does |
|---|---|---|
| "I know Power BI but what's next?" | Uncertain about career trajectory past entry/mid-level | Watches random tutorials, jumps between topics; needs structured path to ₱100k+ |
| "Everyone uses different tools" | Frustrated by fragmentation (Tableau vs Power BI vs Looker Studio) | Sticks to what they know; needs guidance on which tools differentiate at salary bands |

---

## Profile 5: Data Engineers 🛠️

### Demographics (from survey)
- **Share of community:** ~4.4% (n=82) — smaller but higher-earning segment
- **39.0%** earn ₱100k+ — highest concentration of any role cluster

### Real Data Points
- **39.0%** reach ₱100k+ salary vs 15.5% of Data Analysts — DE pays materially more at every comparable level
- **Driven by:** 24.4% earning ₱125k-₱250k (the premium tier)
- **Core tools:** Python (78.5%), SQL (88.6%) — more heavily used in DE than DA
- **Cloud platforms:** AWS 53.5%, Azure 52.1% — near-mandatory for DE professionals
- **Git/GitHub:** 48.8% use version control
- **AI tools:** GitHub Copilot (16.5%), Cursor (12.7%), Databricks assistant (10.1%) — AI-assisted coding is mainstream in DE work

### Key Motivations
- Premium compensation trajectory (₱100k+ at 39% rate)
- Cloud platform mastery and certification
- Architecture design and documentation skills (Draw.io used by 35.4%)

### Pain Points (Evidence-Backed)
- **Hardware bottleneck for DE workloads:** 19.5% use VMs, 12.2% use workstations — most can't run Docker/Spark locally
- **Portfolio gap:** A portfolio without a cloud project is a "significant gap" per survey data
- **Git/GitHub adoption at 48.8%** — nearly half of DEs don't use version control, a professional expectation
- **Draw.io architecture diagrams** used by only 35.4% — documentation skills are underdeveloped

### Empathy Map (Augmented with Data)
| Says | Thinks/Feels | Does |
|---|---|---|
| "I know Python and SQL but what's next?" | Wants to reach the ₱100k+ tier but unsure of the path | Builds local pipelines; needs cloud deployment guidance (AWS/Azure) |

---

## Profile 6: Content Creators & Educators 🎬

### Demographics (from survey)
- **Share of community:** Only 0.4% are in content-related roles as primary data role
- **7.3%** willing to "regularly post content" as volunteer activity
- **38.8%** willing to share knowledge; 25.9% willing to co-train

### Real Data Points (GitHub contributors)
- **Sandy Lauguico** (@sclauguico) — 46 GitHub followers, 74 repos; portfolio site; ETL geospatial projects; ecommerce modern data stack (13 stars); YouTube educator
- **Nicksy Molms** (@nextcm) — Civil & Structural Engineer documenting Python learning journey; IT curriculum guide; public repo "learnpython"
- **Joseph Beltran** (@ProfBelts) — Web Developer aspiring to be Senior Developer; 68 public repos; builds full-stack apps (C#, Ruby, TypeScript)

### Key Motivations
- Sharing knowledge with community (38.8% willing)
- Recognition and visibility for contributions
- Collaboration opportunities with other creators

### Pain Points (Evidence-Backed)
- **YouTube is dominant learning channel** (65.8%) but DEP YouTube channel awareness is only 24.6% — massive under-indexing given the overlap
- **No collaboration infrastructure:** Creators don't know each other's work; siloed content production
- **No tracking/recognition system:** No way to measure who contributed what or get visibility
- **Content creation is not a core skill** for DA/DE roles, but monthly LinkedIn posts and portfolio showcases are sufficient professional visibility

### Empathy Map (Augmented with Data)
| Says | Thinks/Feels | Does |
|---|---|---|
| "I made this video but who watched it?" | Uncertain about impact; wants recognition | Posts on social media, hopes for organic reach; YouTube awareness at 24.6% |

---

## Profile 7: Corporate / Mid-Senior Professionals 🏛️

### Demographics (from survey)
- **Share of community:** ~5.9% "Freelance / Gov / Volunteer" + subset of the 19.6% Professionals
- **88.4%** hold Bachelor's; 7.4% hold Master's — higher education concentration
- **Team size** and **remote work** identified as job satisfaction drivers (from ML analysis)

### Real Data Points (GitHub contributors)
- **Scott Lee Chua** (@scottleechua) — "Econs | Comics | Games"; Manila-based; 19 GitHub followers, 16 repos; builds Telegram bots, data viz apps, personal website
- **Wrenczar Ramos** (@Crocsover) — Cloud Data Engineer; Python interview questions repo; ETL pipelines; Webscraping projects

### Key Motivations
- Hiring qualified local talent (frustration with hiring pipeline)
- Staying current on industry trends and tool sophistication
- Giving back through mentoring (15.1% of Professionals willing to mentor)

### Pain Points (Evidence-Backed)
- **Hiring friction:** Can't find qualified local talent; 48.3% of employed members earn ≤₱35k
- **Mentorship commitment ambiguity:** "I'd love to help but I'm busy" — need structured, time-bound mentoring (e.g., ADPList-style booking)
- **No structured way to give back beyond occasional Facebook comments**

### Empathy Map (Augmented with Data)
| Says | Thinks/Feels | Does |
|---|---|---|
| "I need good data talent" | Frustrated by hiring pipeline; sees salary gap | Posts job requests in Facebook group occasionally; 15.1% willing to mentor |

---

## Profile 8: Overseas Filipinos & International Members 🌏

### Demographics (from survey)
- **96.6%** Philippines-based — very small overseas minority
- Mentoring program FAQ explicitly says "Can I participate if I'm not from the Philippines? Yes."

### Key Motivations
- Staying connected to Philippine data community while abroad
- Remote mentoring, hiring, or collaboration opportunities
- Contributing to local tech ecosystem from diaspora

### Pain Points (Evidence-Backed)
- **Geographic mismatch:** PH-focused events don't align with timezone
- **Limited remote contribution pathways** — unclear how overseas members can participate meaningfully
- **Language/cultural gap:** Some content may be English-heavy or Taglish

---

## Community Leaders & Their Roles (Augmented from GitHub + Survey)

| Name | GitHub Handle | Role/Expertise | Key Projects |
|---|---|---|---|
| **Myk Ogbinar** | @ogbinar | Community founder; Website, Learn Data Pilipinas, Community Leadership | DataEngineeringPilipinas (233⭐), property-pi, py-sdg-eda-workshop |
| **Sandy G. Cabanes** | @SandyGCabanes | Survey analyst; Mentorship program lead; DE pipeline projects | DEP-Survey-Data-Pipeline, 2025-2026 State of Community Survey, ECommerce Analytics |
| **Sandy Lauguico** | @sclauguico | YouTube educator; Data science content creator | portfolio, etl-geospatial (3⭐), ecommerce-modern-data-stack (13⭐) |
| **Michael Angelo Bellen** | @MikeBellen | Data Scientist; DataCamp Donates scholarship lead | Amazon Product Recommendation, Predicting Customers, Foodhub Analysis |
| **Wrenczar Ramos** | @Crocsover | Cloud Data Engineer | ETL-Pipelines (2⭐), Python interview questions, Data-Engineer projects |
| **Katherine Bulac** | @gkate78 | Community leadership; "Learn, lead, build." | bps, meetup-dashboard, pythonasia2026 workshop |
| **Nicksy Molms** | @nextcm | Civil & Structural Engineer learning DE; DataCamp roadmaps | Project-Portfolio, IT-curriculum-guide, learnpython |
| **Gino Freud Hobayan** | @Gino-Freud-Hobayan | Hardware/embedded systems; Arduino; personal website | Arduino-Tx-Rx, hackathon-crud, personal-website |
| **Joseph Beltran** | @ProfBelts | Web Developer → Senior Developer aspirant | full-stack-evaluator (.NET 9), Collab-Text-Editor, broadcast-api |
| **Dan Arnaiz** | @dan-arnaiz | "Conflicted contradiction"; MDG-SMS (scholarship system); DeepSeek-V3 | mdg-cnn-tsa, Ryujinx (Nintendo emulator), DeepSeek-V3 |
| **Scott Lee Chua** | @scottleechua | Econ + Comics + Games; Manila-based developer | spam-of-the-times (3⭐), tele-post-formatter, googleform-to-rabbitsign |
| **komiwalnut** | @komiwalnut | Accenture; Data Science & ML; "I want my own Neuro-sama" | portfolio (1⭐), wild-forest-community, Haroval flashcard app, bettergov.ph |

---

## Research Methods & Timeline (Updated)

### Phase 1: Quantitative (Already Done) ✅
- **DEP Survey 2026** — 1,861 responses; already published by Sandy G. Cabanes
- **GitHub contributor analysis** — 19 core contributors mapped with repos and expertise
- **Community website content audit** — all 7+ pages scraped and analyzed

### Phase 2: Qualitative (To Execute)
- **1-on-1 Interviews** — 5-8 per profile (40-56 total); use survey segments as sampling frame
- **Focus Groups** — 2 groups: (1) Students + Career Shifters; (2) Senior Professionals + Content Creators
- **Discord/Facebook observation** — monitor natural behavior patterns, question frequency, pain point emergence

### Phase 3: Synthesis (Deliverables)
1. **Empathy Maps** — for all 8 profiles (above)
2. **User Personas** — detailed character sketches with quotes and goals
3. **Journey Maps** — how each profile interacts with community over time
4. **Pain Point Matrix** — prioritized by frequency, severity, and survey evidence
5. **"How Might We" Statements** — ready for Ideate stage

---

## Key Strategic Insights (from Survey Data)

1. **The community's primary value is access** — to tools, credentials, hardware, and networks that accelerate the transition from ₱35k floor to ₱100k+ ceiling
2. **Every DEP initiative may be evaluated against this question:** Does it narrow the income mobility gap?
3. **YouTube-first + Discord accountability + DEP certification** = highest probability of sustained enrollment and completion for self-paced learning
4. **AI is mainstream, not optional** — 80.8% use AI weekly for study; curriculum must assume AI-assisted workflows
5. **DataCamp scholarship (89.6% awareness) is the anchor program** — everything else should build on or complement this trust asset
6. **DE pays materially more than DA** — 39% of DEs reach ₱100k+ vs 15.5% of DAs; students who develop DE skills alongside DA fundamentals position for structurally higher earnings
