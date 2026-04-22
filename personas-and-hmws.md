# Personas & How Might We Statements — Data Engineering Pilipinas Community Hub

## Source Basis
All personas and HMW statements are derived from:
- **DEP State of the Community Survey 2026** (n=1,861 respondents) — https://sandygcabanes.github.io/2025-2026-DEP-State-of-the-Community-Survey-Results/
- **GitHub contributor analysis** — 19 core contributors mapped
- **Community website** dataengineering.ph content structure
- **Empathize research** — /projects/community-hub/empathize-augmented.md

---

## Persona 1: "Maya" — The Student Learner

### Demographics
- **Name:** Maya Santos
- **Age:** 21
- **Location:** Quezon City, Metro Manila
- **Education:** BS Statistics, 3rd year student (89.8% of community hold Bachelor's or above)
- **Device:** Laptop only (84.5% rely on laptop; only 0.8% have workstation access)
- **Salary:** N/A (Student segment — 34.5% of community, n=642)

### Background & Motivations
Maya is a 3rd-year Statistics student who joined the DEP Facebook group after hearing about DataCamp scholarships from a classmate. She's time-rich and highly motivated: **81.6% of Students want upskilling**. She watches YouTube tutorials (65.8% of Students use YouTube) on weekends while balancing coursework. She's the most AI-native segment in the community — she uses ChatGPT (86.6%), Gemini (68.2%), and GitHub Copilot (24.7%) daily for study, not as a cheat but as her primary learning medium.

### Pain Points (Quantified)
- **Resource overload:** Too many links on dataengineering.ph; doesn't know where to start between SQL, Python, Power BI, or cloud platforms
- **DAX knowledge gap:** Only 2.2% of Students use DAX vs 29.1% of DA Professionals — she's missing a high-value upskill
- **Hardware bottleneck:** Her laptop can't run Docker/Spark for DE Zoomcamp projects (DataTalks.Club used by only 1.0%)
- **AI dependency risk:** "I use AI to get answers, not to learn" — she hasn't been taught how to interrogate AI outputs

### Key Behaviors
- Learns through YouTube (65.8%) and DataCamp (49.3%) — mix of video how-to's and hands-on projects
- Over-indexes on GitHub Copilot (24.7% vs 13.6% Seeking work) — uses it for practical coding assistance
- Uses Google Sheets (49.7%) because she doesn't have Excel access — but knows employers expect Excel proficiency

### Quote
> "I watch a lot of YouTube tutorials, but I don't know which ones actually lead to a job. Everyone seems ahead of me."

---

## Persona 2: "Jose" — The Job Seeker

### Demographics
- **Name:** Jose Reyes
- **Age:** 24
- **Location:** Pasig City, Metro Manila
- **Education:** BS Mathematics (graduated 6 months ago)
- **Device:** Laptop only
- **Salary:** N/A or internship stipend (<₱15k — 9.4% of employed are at absolute entry/intern level)

### Background & Motivations
Jose graduated with a Math degree and immediately started looking for data roles. He's actively seeking employment: **86.9% of Job Seekers want upskilling** — the highest motivation-to-enrollment ratio of any segment. He knows LinkedIn is where jobs are found (74.4% of employed use LinkedIn) but his profile is thin on projects and certifications. He's frustrated by the gap between "I know Excel" and "I'm job-ready."

### Pain Points (Quantified)
- **LinkedIn not optional:** 74.4% of professionals use LinkedIn for job discovery — he needs project-rich GitHub + LinkedIn combo but doesn't know how to build it
- **DAX knowledge gap:** Only 2.2% use DAX vs 29.1% of DA Professionals — this signals a high-value upskill opportunity he's missing
- **Under-utilized free resources:** Microsoft Learn at 8.6%, Google Cloud Skills Boost at 2.3%, HackerRank/LeetCode at 5.4% — he doesn't know these exist or how to use them for credentials
- **Portfolio gap:** No clear guidance on what projects actually impress hiring managers

### Key Behaviors
- Applies to jobs blindly, gets ghosted — needs structured portfolio building
- Uses Facebook (27.0%) more than LinkedIn (15.2%) for job discovery — but LinkedIn is where professionals actually find roles
- Wants upskilling (86.9%) but doesn't know which skills have the highest ROI

### Quote
> "I finished my degree but I don't have a portfolio. I apply to jobs on LinkedIn but I keep getting rejected. What projects do they actually want?"

---

## Persona 3: "Lia" — The Career Shifter

### Demographics
- **Name:** Lia Cruz
- **Age:** 28
- **Location:** Cebu City (16.5% of community outside Metro Manila/Luzon)
- **Education:** BA Communication Arts (58.5% have NO computing degree — non-CS backgrounds dominate)
- **Device:** Laptop only (8-16GB RAM, SSD — sufficient for most DA work)
- **Salary:** ₱20k/month (66.5% earn ≤₱35k — disproportionately concentrated at entry floor)

### Background & Motivations
Lia worked in marketing communications for 4 years before realizing she wanted to transition into data. She's still in the "decision to shift" phase: **62.5% of Shifters are actively weighing their shift**. She earns ₱20k/month and wants more but feels trapped at the entry salary level. She has no computing degree (58.5% don't) and feels like a liability to employers. She's motivated by career advancement (86.3% have high motivation to upskill) but is lagging on AI adoption — only 50.2% use AI daily for work vs 65.3% of Professionals.

### Pain Points (Quantified)
- **No recognized credential:** Non-CS background feels like a liability — 58.5% have no computing degree
- **Salary trap:** 66.5% earn ≤₱35k; lowest satisfaction profile (72.9% score 1-5 on satisfaction)
- **AI adoption lag:** Only 50.2% use AI daily for work (vs 65.3% Pros); 15.4% use AI monthly or less; 3.4% say they don't plan to use AI (highest refusal rate)
- **Power BI gap:** 25-point gap (69.1% DA Pros vs 43.9% Shifters) — highest ROI upskill
- **DAX gap:** Highest-signal gap (29.1% DA Pros vs 6.2% Shifters) — separates capable Power BI users from experts

### Key Behaviors
- Uses Facebook more than LinkedIn for job discovery (27.0% vs 15.2%) — but LinkedIn is where professionals actually find roles
- Lags on AWS/Azure familiarity (25.8% vs 45.2% Pros) but uses GCP more (60.7% vs 26.8% Pros) — may be using free tiers but industry expects AWS/Azure
- Needs a "Local to Cloud Bridge" curriculum — integrate Cloud and AI as monitoring/deployment layer of local work

### Quote
> "I don't have a CS degree, so I feel like everyone's ahead of me. I'm earning ₱20k and want more, but I don't know what skills will actually get me to ₱50k."

---

## Persona 4: "Rico" — The Data Analyst Professional

### Demographics
- **Name:** Rico Mendoza
- **Age:** 31
- **Location:** Makati City, Metro Manila
- **Education:** BS Statistics (88.4% hold Bachelor's; 7.4% hold Master's)
- **Device:** Laptop + occasional workstation access (11.3% of DA Professionals use workstation)
- **Salary:** ₱55k/month (₱35k-₱75k band — largest band; DA modal range at 38.5%)

### Background & Motivations
Rico is a mid-level Data Analyst working in a corporate BPO. He's been in his current role for 2 years and wants to break through to the ₱100k+ tier. He uses Power BI (69.1% of DAs specifically) daily but feels stuck at the mid-level salary band. He knows AI is important — **65.3% use AI daily for work** (highest of any segment) — but he's not sure how to differentiate himself beyond "I use ChatGPT." He's in the modal salary band (₱35k-₱75k) with only 31.9% satisfaction scores, and he wants more.

### Pain Points (Quantified)
- **The ₱75k-₱100k bottleneck:** Only 9.1% of Professionals sit here — a structural ceiling that requires deliberate upskilling to break through
- **"One BI tool" advice is only half-right:** Correct for entry-level, but ₱100k+ earners show multi-tool fluency (Power BI + Tableau + Looker Studio + Python tools)
- **AI is mainstream, not differentiating:** 65.3% use AI daily — the edge now lies in *how* you use AI (audit outputs, security, accuracy, cost)
- **Tool sophistication at ₱100k+:** SQL (76.9%), Python (73.6%), Tableau (38.0%), Alteryx (10.1%), Qlik Sense (8.9%) — multi-tool fluency separates high earners

### Key Behaviors
- Conducts quiet market check at 18-month mark (median tenure at current salary is 1-2 year band)
- Uses Power BI across all bands — it is not a differentiator in itself
- Wants to move from ₱55k to ₱100k+ but doesn't know which skills differentiate between bands

### Quote
> "I've been using Power BI for 2 years and I'm comfortable, but I'm stuck at ₱55k. I see people earning ₱100k+ — what do they know that I don't?"

---

## Persona 5: "Kai" — The Data Engineer

### Demographics
- **Name:** Kai Tan
- **Age:** 29
- **Location:** Taguig City, Metro Manila
- **Education:** BS Computer Science (4.4% of community are DEs, n=82)
- **Device:** Laptop + cloud VM access (19.5% use VMs; 12.2% use workstations)
- **Salary:** ₱120k/month (39.0% reach ₱100k+ — highest concentration of any role cluster)

### Background & Motivations
Kai is a mid-level Data Engineer who made the switch from software development. He's in the premium compensation tier: **39.0% earn ₱100k+** (vs 15.5% of DA). He uses Python (78.5%), SQL (88.6%), and cloud platforms (AWS 53.5%, Azure 52.1%) daily. But he's frustrated by the Git/GitHub adoption gap — nearly half of DEs don't use version control, a professional expectation. He also knows Draw.io architecture diagrams are used by only 35.4% of DEs — documentation skills are underdeveloped.

### Pain Points (Quantified)
- **Git/GitHub adoption at 48.8%** — nearly half of DEs don't use version control, a professional expectation
- **Draw.io architecture diagrams used by only 35.4%** — documentation skills are underdeveloped
- **Hardware for DE workloads:** 19.5% use VMs, 12.2% use workstations. Most can't run Docker/Spark locally
- **Portfolio gap:** A portfolio without a cloud project is a "significant gap" per survey data

### Key Behaviors
- Uses GitHub Copilot (16.5%) and Cursor (12.7%) — AI-assisted coding is mainstream in DE work
- Databricks assistant (10.1%) emerging as specialized DE AI tool
- Wants to advance to senior/architect level but needs cloud deployment guidance (AWS/Azure)

### Quote
> "I know Python and SQL, and I've built pipelines on AWS, but I don't use GitHub properly. My portfolio looks messy. How do I get to Senior DE?"

---

## Persona 6: "Sandy" — The Content Creator & Educator

### Demographics
- **Name:** Sandy Lauguico (real community member)
- **Age:** Late 20s/Early 30s
- **Location:** Manila, Philippines
- **Education:** Self-taught + DataCamp certifications
- **Device:** Laptop
- **Salary:** N/A (Content creation is not a primary career path)

### Background & Motivations
Sandy is a YouTube educator and data science content creator who contributes to the DEP community. She's part of the 0.4% in content-related roles as a primary data role, but she's willing to volunteer: **7.3% willing to "regularly post content"** and **38.8% willing to share knowledge**. She creates YouTube tutorials (65.8% of community learns via YouTube) and has built an audience through consistent content creation. She wants more visibility for her work but doesn't know how to reach people beyond organic social media posting.

### Pain Points (Quantified)
- **YouTube awareness at 24.6%** — massive under-indexing given that 65.8% of community learns via YouTube
- **No collaboration infrastructure:** Creators don't know each other's work; siloed content production
- **No tracking/recognition system:** No way to measure who contributed what or get visibility
- **Content creation is not a core skill** for DA/DE roles, but monthly LinkedIn posts and portfolio showcases are sufficient professional visibility

### Key Behaviors
- Posts on social media, hopes for organic reach
- Creates solo content, rarely cross-promotes with other creators
- Wants recognition for contributions but has no platform to showcase them

### Quote
> "I made this video tutorial but I don't know how many people watched it. I wish other creators would collaborate instead of working in silos."

---

## Persona 7: "David" — The Corporate Data Manager

### Demographics
- **Name:** David Lim
- **Age:** 35
- **Location:** Makati City, Metro Manila
- **Education:** BS IT + Master's in Data Science (4× more common at ₱75k-₱100k; 18.6% at ₱100k+)
- **Device:** Workstation (11.3% of DA Professionals use workstation)
- **Salary:** ₱150k/month (Senior DE: 39.0% are here)

### Background & Motivations
David is a Data Manager at a mid-sized tech company. He's in the ₱100k+ tier and wants to give back to the community but doesn't know how beyond occasional Facebook comments. **15.1% of Professionals are willing to mentor** — he's one of them but finds the commitment ambiguous. He's frustrated by hiring friction: he can't find qualified local talent and wants to help build the pipeline. He values structured, time-bound mentoring (e.g., every first Thursday of the month) rather than indefinite commitments.

### Pain Points (Quantified)
- **Hiring friction:** Can't find qualified local talent; 48.3% of employed members earn ≤₱35k
- **Mentorship commitment ambiguity:** "I'd love to help but I'm busy" — needs structured, time-bound mentoring
- **No structured way to give back beyond occasional Facebook comments**

### Key Behaviors
- Posts job requests in Facebook group occasionally
- Willing to mentor (15.1%) but doesn't know how to structure it
- Values team size and remote work as satisfaction drivers (from ML analysis)

### Quote
> "I want to help the community, but I'm busy with my own team. If there was a structured way to mentor — maybe just 2 hours a month — I'd sign up tomorrow."

---

## Persona 8: "Ana" — The Overseas Filipino Professional

### Demographics
- **Name:** Ana Reyes (fictional composite)
- **Age:** 30
- **Location:** Dubai, UAE (3.4% of community outside Philippines)
- **Education:** BS Computer Science
- **Device:** Laptop + cloud access
- **Salary:** Equivalent to ₱100k+ in PH terms

### Background & Motivations
Ana is a Filipino professional working abroad who joined the DEP Facebook group to stay connected with the Philippine data community. She's part of the 3.4% outside Philippines and wants to contribute remotely — mentor junior Filipinos, hire locally, or collaborate on projects. But she faces timezone and cultural barriers to participation. The mentoring program FAQ explicitly says "Can I participate if I'm not from the Philippines? Yes" but there's no clear pathway for overseas members to engage meaningfully.

### Pain Points (Quantified)
- **Geographic mismatch:** 83.5% concentrated in Metro Manila/Luzon — events don't align with her timezone
- **Limited remote contribution pathways:** Unclear how overseas members can participate meaningfully
- **Language/cultural gap:** Some content may be English-heavy or Taglish

### Key Behaviors
- Lurks in Facebook group, rarely engages due to timezone mismatch
- Occasionally shares resources but hopes for more structured remote roles
- Wants to mentor or hire locally but doesn't know how to connect with candidates

### Quote
> "I'm Filipino but I'm overseas. I want to help the community, but I don't know how to participate when everyone's in Manila."

---

## How Might We Statements — By Profile

### Profile 1: Students (Maya)
**How might we help Maya navigate the overwhelming amount of free resources and find a clear, personalized learning path?**

- HMW 1: *How might we help Maya use AI as a study tool — not to get answers, but to interrogate them?*
- HMW 2: *How might we help Maya build portfolio projects that work on a laptop without Docker/Spark?*
- HMW 3: *How might we help Maya learn DAX (only 2.2% use it) as a high-value upskill opportunity?*

### Profile 2: Job Seekers (Jose)
**How might we help Jose build a project-rich LinkedIn profile that actually gets him interviews?**

- HMW 1: *How might we help Jose understand which free resources (Microsoft Learn, Google Cloud, HackerRank) have the highest credential ROI?*
- HMW 2: *How might we help Jose learn DAX (only 2.2% of Students use it vs 29.1% Pros) as a differentiator?*
- HMW 3: *How might we help Jose transition from Facebook job discovery (27.0%) to LinkedIn (74.4%) where professionals actually find roles?*

### Profile 3: Career Shifters (Lia)
**How might we help Lia bridge the gap between her non-CS background and data engineering requirements?**

- HMW 1: *How might we help Lia adopt AI tools daily for work (only 50.2% vs 65.3% Pros) as a skill, not a crutch?*
- HMW 2: *How might we help Lia close the Power BI gap (25-point gap) and DAX gap (highest-signal gap) with targeted learning?*
- HMW 3: *How might we help Lia build a "Local to Cloud Bridge" curriculum that integrates Cloud and AI as monitoring/deployment layer of local work?*

### Profile 4: Data Analysts (Rico)
**How might we help Rico break through the ₱75k-₱100k salary bottleneck?**

- HMW 1: *How might we help Rico develop multi-tool fluency (Tableau + Looker Studio + Python tools) that separates ₱100k+ earners?*
- HMW 2: *How might we help Rico articulate his AI workflow in interviews — "I use Copilot for query generation, Claude for documentation review" — rather than just "yes, I use AI"?*
- HMW 3: *How might we help Rico identify which skills differentiate between salary bands (SQL 76.9%, Python 73.6% at ₱100k+ vs lower bands)?*

### Profile 5: Data Engineers (Kai)
**How might we help Kai advance to Senior DE with proper documentation and cloud deployment skills?**

- HMW 1: *How might we help Kai adopt Git/GitHub properly (only 48.8% of DEs use it, a professional expectation)?*
- HMW 2: *How might we help Kai learn Draw.io architecture diagrams (used by only 35.4% of DEs) to document and communicate system design?*
- HMW 3: *How might we help Kai build cloud deployment skills (AWS 53.5%, Azure 52.1%) that are near-mandatory for DE professionals?*

### Profile 6: Content Creators (Sandy)
**How might we help Sandy and other creators get better visibility and collaboration opportunities?**

- HMW 1: *How might we amplify YouTube content (65.8% learn via YouTube) when only 24.6% awareness of DEP YouTube channel?*
- HMW 2: *How might we create a collaboration infrastructure so creators know each other's work instead of working in silos?*
- HMW 3: *How might we build a tracking/recognition system that measures who contributed what and gives visibility to contributors?*

### Profile 7: Corporate Professionals (David)
**How might we help David structure his mentoring commitment without overwhelming his schedule?**

- HMW 1: *How might we help David mentor with specific time-bookings (e.g., every first Thursday of the month) instead of indefinite commitments?*
- HMW 2: *How might we help David connect with qualified local talent to solve his hiring friction?*
- HMW 3: *How might we help David give back through structured channels beyond occasional Facebook comments?*

### Profile 8: Overseas Filipinos (Ana)
**How might we help Ana participate meaningfully in the Philippine data community from overseas?**

- HMW 1: *How might we create remote contribution pathways for overseas members who face timezone and geographic barriers?*
- HMW 2: *How might we help Ana mentor or hire locally when 83.5% of the community is concentrated in Metro Manila/Luzon?*
- HMW 3: *How might we bridge the language/cultural gap for overseas members engaging with English-heavy or Taglish content?*

---

## Summary Table: Personas → HMWs → Community Hub Features

| Persona | Primary Pain Point | Key HMW | Potential Community Hub Feature |
|---|---|---|---|
| **Maya (Student)** | Resource overload, AI dependency | Help Maya use AI as study tool | AI-augmented learning modules with "interrogate the answer" exercises |
| **Jose (Job Seeker)** | Portfolio gap, LinkedIn optimization | Build project-rich LinkedIn profile | Portfolio builder + LinkedIn profile optimizer tool |
| **Lia (Career Shifter)** | No CS degree, salary trap | Close Power BI/DAX gaps with targeted learning | Career Shifter DA/DE pathway with mentorship matching |
| **Rico (Data Analyst)** | ₱75k-₱100k bottleneck | Develop multi-tool fluency | Salary band progression tracker + skill gap analyzer |
| **Kai (Data Engineer)** | Git/GitHub adoption, documentation | Adopt proper version control + architecture docs | GitHub integration guide + Draw.io template library |
| **Sandy (Creator)** | Visibility, collaboration | Amplify YouTube content + create collaboration infrastructure | Creator spotlight platform + cross-promotion network |
| **David (Corporate Pro)** | Structured mentoring | Mentor with time-bookings instead of indefinite commitments | Time-bound mentorship matching (ADPList-style) |
| **Ana (Overseas Filipino)** | Geographic mismatch, remote barriers | Create remote contribution pathways | Remote mentorship board + async collaboration tools |

---

## Next Steps: From Personas to Prototype

The personas and HMW statements above are grounded in hard survey data. The next step is to move to the **Ideate stage** — brainstorming specific Community Hub features that address each HMW, then prototyping the highest-impact ones based on:

1. **Impact on income mobility gap** (₱35k → ₱100k+ as the core value proposition)
2. **Community adoption probability** (YouTube-first + Discord accountability + DEP certification)
3. **Volunteer sustainability** (AI tools can reduce content production effort by 5-10×)

Would you like to proceed to the Ideate stage?
