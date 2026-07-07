# Lead Log — Harthik Royal Mallichetty

This file is append-only. Each daily run adds a new `## Run:` section below 
with that day's findings. Older entries are never deleted or edited — if a 
lead goes stale or gets applied to, note that in a NEW entry rather than 
editing the old one, so the history stays intact.

Every lead row must include a working direct link. If a run reports a lead 
without a link, treat that run's output with suspicion and check it manually.

---

## Run: 2026-06-20 12:00

**First substantive run** (prior log was empty — header only, no leads). One
thorough pass completed.

**Coverage & honesty notes (read before trusting visa buckets):**
- Direct ATS job pages on `job-boards.greenhouse.io`, `*.myworkdayjobs.com`,
  and `simplify.jobs` all returned **HTTP 403** to the fetcher this run, so I
  **could not read the individual JD text** to confirm visa/sponsorship
  language, exact YoE, or clearance requirements. Visa buckets below are
  inferred from company type + role, **not** from the JD — every one marked
  "verify" must be opened manually.
- Recency is taken from the "age" field of two daily-maintained GitHub job
  trackers (`speedyapply/2026-AI-College-Jobs`,
  `jobright-ai/2026-Data-Analysis-New-Grad`), which are the most reliable
  dated, directly-linked sources I could actually load. General web/Indeed/
  Glassdoor/LinkedIn searches returned only aggregator landing pages with no
  per-posting dates or stable direct links, so nothing from those is logged.
- Community boards (Reddit/Discord/Slack): **not checked this run** — no prior
  active-board list exists yet (first run). Building that list is a TODO for
  the next run; flagged here so it isn't silently skipped forever.

### Tier 1 — Hot & strong fit
_None this run that clear the bar (recent ≤24h + low-visa-risk + strong applied-AI fit + JD-verified). The greenhouse/workday 403s prevented JD verification, which by the honesty rule keeps the otherwise-promising ones in Tier 2._

### Tier 2 — Worth a look (good fit, one caveat — almost all caveats are "visa unverified, JD unreadable this run")

| Company | What they do / size | Role | Direct link | Posted (basis) | Visa posture | Fit note | Source |
|---|---|---|---|---|---|---|---|
| Astera Labs | Connectivity semiconductors for AI/cloud infra; public, mid-large (~1k) | Machine Learning Engineer – New College Grad 2026 | https://job-boards.greenhouse.io/asteralabs/jobs/4646633005 | ~Jun 18 ("2d" on tracker) | Silent, larger company — **verify** | New-grad ML role, explicitly 2026; semis is heavier on systems/ML-for-hardware than LLM/RAG — fit is the ML title, gap is the applied-GenAI angle | speedyapply tracker |
| Dealer Tire | Tire distribution/analytics, mid-size; remote-friendly | Associate Data Scientist (Remote) | https://jobright.ai/jobs/info/6a3576567f3fdd180d4cd9c5 | Jun 19 | Silent, larger company — **verify** | Remote, entry "Associate" DS — solid for the analytics/ML side of the profile; gap is it's DS not AI-eng | jobright tracker |
| Home Depot | Big-box retail, large enterprise (non-FAANG) | Associate Data Scientist | https://homedepot.wd5.myworkdayjobs.com/en-US/careerdepot/job/STORE-SUPPORT-CENTER-ATLANTA---9090/Associate-Data-Scientist_Req183993 | ~Jun 19 ("1d") | Silent, larger company — **verify** (large enough to have real immigration policy) | Entry DS at scale; Atlanta; analytics fit, GenAI gap | speedyapply tracker |
| Caterpillar | Heavy equipment, large enterprise | Supply Chain Data Analyst | https://jobright.ai/jobs/info/6a306016afabbe533fb8abcf | Jun 19 | Silent, larger company — **verify** | Data Analyst fit; supply-chain domain; large co immigration policy unknown | jobright tracker |

### Tier 3 — Long shots / needs verification / likely blocked

| Company | What they do | Role | Direct link | Posted | Visa posture | Why Tier 3 | Source |
|---|---|---|---|---|---|---|---|
| True Anomaly | Space/defense (orbital security) startup | Machine Learning Engineer I–III | https://job-boards.greenhouse.io/trueanomalyinc/jobs/5138856007 | ~Jun 19 ("1d") | **Likely blocked** — defense/space → ITAR almost always requires US person | Great role/recency, but ITAR US-person requirement very likely disqualifies F-1 OPT. Confirm before spending effort | speedyapply tracker |
| VHB | Engineering/planning consultancy | Data Scientist | https://jobright.ai/jobs/info/6a357484f6b55d12c791fe2b | Jun 19 | Unclear — **verify** | Consultancy DS; fit is moderate, govt-adjacent work may have citizenship constraints | jobright tracker |
| Snowflake | Data cloud platform, large | AI Research Scientist – New Grad | (Ashby listing — full direct URL not captured this run; search surfaced `jobs.ashbyhq.com` only) | ~Jun 17 ("3d", outside 24h) | Silent, larger company — verify | **Link not captured + outside 24h window + research-not-applied-eng.** Logged honestly without a fabricated URL; not safe to treat as a verified lead | speedyapply tracker |

### Recency unverified (could not confirm ≤24h)
| Company | Role | Direct link | Note |
|---|---|---|---|
| Loop | 2026 New Grad Software Engineer, AI (SF/NYC, in-person 4d) | https://job-boards.greenhouse.io/loop/jobs/5780584004 | Surfaced via search, not the dated trackers — **no confirmed post date**. AI-focused new-grad SWE at a startup; worth checking if still open and when posted |
| NVIDIA | High-Performance LLM Training Engineer – NCG 2026 | nvidia.wd5.myworkdayjobs.com (full direct URL not captured) | Tracker showed "4d" — **outside 24h window**; also systems/training-infra heavy vs applied-AI-product profile |

### Excluded (logged so future runs don't re-surface)
- **Boeing – Associate Data Analyst** (Long Beach, "3d"): defense/aerospace, US-citizenship requirement near-certain. Visa-blocked.
- **Traction Complete – Junior AI Automation Developer** (Vancouver, BC, "2d"): Canada-based; F-1 OPT is US work authorization and does not apply. Out of geography.
- **Edwards Lifesciences – Research Scientist I**, **Exact Sciences – Associate Research Scientist I**, **USC – Research Coordinator I**, **Westat – Research Assistant**: wet-lab/clinical research roles, not applied-AI/data-eng fit.

### Bonus — "consider expanding search to"
- Adjacent title seen repeatedly: **Associate Data Scientist** (entry/new-grad DS). Not on the target list but a clean fit for this profile's analytics + ML side — worth adding as a first-class search term in future runs.

### TODO for next run
- Build the community-board list (subreddits like r/dataengineering, r/MachineLearning "who's hiring", relevant Discords/Slacks) and check which are actually active — none verified yet.
- Try an authenticated/alternate fetch path for greenhouse/workday JDs so visa posture can be read directly instead of inferred.

---

## Run: 2026-06-20 05:21 (DEEP BACKFILL — 30 day window)

**THIS IS A ONE-TIME DEEP BACKFILL, NOT A DAILY PASS.** It uses a **30-day**
recency window (Tier window ≈ posts aged ≤30d, i.e. ~May 21 – Jun 20) instead
of the normal 24h, to establish a baseline. Future daily runs should keep using
24h and treat anything below as already-seen.

**Coverage & honesty notes (read before trusting anything below):**
- **Fully covered (dated, directly-linked GitHub trackers, all loaded via
  `raw.githubusercontent.com` which is NOT blocked):**
  - `speedyapply/2026-AI-College-Jobs` → `NEW_GRAD_USA.md` (FTE AI/ML/Data new-grad list) — read in full.
  - `jobright-ai/2026-Data-Analysis-New-Grad` (`master` branch) — read in full (Jun 13–19 rows).
  - `jobright-ai/2026-Business-Analyst-New-Grad` — data/analytics subset read.
  - `zapplyjobs/New-Grad-Data-Science-Positions` — AI/ML-Engineer FTE subset read.
- **Partially covered:** `SimplifyJobs/New-Grad-Positions` — the "Data Science,
  AI & ML" category (37 roles) sits at the bottom of a very long README and the
  fetcher repeatedly truncated before reaching it; only the SWE section loaded.
  Not usable this run. `speedyapply` **internship** README loaded but is interns,
  not FTE — excluded from tiers.
- **NOT covered / blocked this run (be explicit):**
  - **Individual JD verification — ALL blocked again (HTTP 403):** greenhouse,
    *.myworkdayjobs.com, jobs.ashbyhq.com, Oracle Cloud (Fortinet), simplify.jobs.
    **I could not read a single JD body**, so EVERY visa bucket below is inferred
    from company type + role, NOT from JD text, and every "verify" must be opened
    manually. Same blocker as the 2026-06-20 12:00 run.
  - **Community boards:** HN "Ask HN: Who is hiring? (June 2026)" thread is LIVE
    (`news.ycombinator.com/item?id=48357725`). I tried to read it 3 ways — HN
    Algolia API (`hn.algolia.com/api/v1/items/48357725`), the GitHub-pages mirror
    (`nchelluri.github.io/hnjobs/`), and `workatastartup.com` — **all 403'd**.
    Web-search summary indicates June 2026 was a cyclical low (~359 posts) and did
    include Forward-Deployed-Engineer/Python roles, but I could not extract
    individual companies/links, so **nothing from HN is logged**. For future runs:
    the HN thread ID above + its emilburzo/nchelluri mirrors are the boards to
    target; none could be machine-read today. Reddit/Discord "who's hiring" threads
    did not surface a current datable thread via search.
  - LinkedIn / Indeed / Glassdoor / Wellfound: only aggregator landing pages, no
    per-posting dates or stable direct links — nothing logged (unchanged from prior run).
- **Recency basis:** jobright rows carry explicit calendar dates (Jun 13–19 = all
  within window). speedyapply/zapplyjobs rows carry an "age" field (e.g. "4d",
  "17d"); I treated age relative to the tracker's Jun 20 refresh. zapplyjobs ages
  shown in minutes/hours (e.g. "7h", "14m") are scraper "first-seen" stamps, not
  guaranteed post dates — flagged inline where used.
- De-duped against the 2026-06-20 12:00 run: Astera Labs NCG 2026, Home Depot
  Assoc DS (Req183993), Caterpillar, Dealer Tire, VHB, True Anomaly ML Eng already
  logged → not repeated. (Home Depot has several other open Assoc DS reqs; not
  re-listed individually.)

### Tier 1 — Hot & strong fit
_Visa caveat: all JD pages 403'd, so buckets are inferred, not JD-verified._

| Company | What they do / size | Role | Direct link | Posted (basis) | Visa posture | Fit note | Source |
|---|---|---|---|---|---|---|---|
| Fortinet | Cybersecurity (firewalls/network security); large public (~14k) | Applied AI Engineer, New Grad – AI Agent | https://edel.fa.us2.oraclecloud.com/hcmUI/CandidateExperience/en/sites/CX_2001/job/23077 | ~within 30d ("first-seen" recent; exact date unread, JD 403) | Silent, larger company — **verify** | Exact target title ("Applied AI Engineer") + explicit New Grad + agent work — bullseye on the applied-GenAI profile; gap is large-co immigration policy unknown | zapplyjobs DS tracker |
| Jerry | AI-first car-insurance/finance super-app; growth-stage (~Series-funded) | Associate Data Scientist | Dallas TX: https://jobright.ai/jobs/info/6a303fa189f8f147d3734594 · SF Bay (Ashby): https://jobs.ashbyhq.com/jerry.ai/488c142a-7f78-44be-b358-6c2a91f4df73 | Jun 15 (jobright date) / "4d" (speedyapply) | Silent, growth startup — likely OK | **Dallas, TX role = candidate-local.** Applied DS at an AI-product company; strong stack overlap; gap: DS framing vs pure AI-eng | jobright + speedyapply NEW_GRAD |
| CrowdStrike | Endpoint/cloud cybersecurity; large public | Engineer I – New Grad – Agentic AI (Hybrid) | https://crowdstrike.wd5.myworkdayjobs.com/en-US/crowdstrikecareers/job/USA---Sunnyvale-CA/Engineer-I---New-Grad--Agentic-AI--Hybrid-_R29022 | "8d" (≈Jun 12) | Silent, larger company — **verify** (not defense; generally OPT-OK) | Explicit New Grad + Agentic AI = direct fit for the LangGraph/agent work; gap: large-co policy unread | speedyapply NEW_GRAD |
| T-Mobile | Telecom carrier; large public (non-FAANG) | Associate AI Engineer | https://tmobile.wd1.myworkdayjobs.com/en-US/external/job/Overland-Park-Kansas/Associate-AI-Engineer_REQ357347 | "8d" (≈Jun 12) | Silent, larger company — **verify** | Entry "Associate AI Engineer" title fit; enterprise applied-AI; gap: policy unread | speedyapply NEW_GRAD |
| Unity | Real-time 3D / game engine; mid-large public | Machine Learning Engineer – New Grad / Entry-Level (Recommendation / User Understanding) | Bellevue: https://unity.com/careers/positions/7999717?gh_jid=7999717 · Mountain View (entry): https://unity.com/careers/positions/7947300?gh_jid=7947300 | "4d"–"28d" | Silent, larger company — **verify** | Explicit new-grad ML; gap: recommender-systems focus heavier than RAG/LLM | speedyapply NEW_GRAD |
| Excellus BCBS / Univera Healthcare | Health insurer (NY); mid-large | AI Engineer I/II | https://lthc.wd1.myworkdayjobs.com/en-US/excellusbcbscareers/job/Rochester/AI-Engineer-I-II_JR103556-2 | "10d" (≈Jun 10) | Silent, larger company — **verify** | "AI Engineer I" entry rung, enterprise applied AI; gap: healthcare domain + policy unread | speedyapply NEW_GRAD |
| Genesis Financial Solutions (Concora Credit) | Consumer-credit fintech; mid-size | Associate Data & ML Operations Engineer | https://careers-concoracredit.icims.com/jobs/2990/associate-data-%26-ml-operations-engineer/job | "17d" (≈Jun 3) | Silent, mid-size — verify | **MLOps is on the target list**; entry "Associate" data+ML-ops fit (Airflow/dbt/Docker overlap) | speedyapply NEW_GRAD |
| PTC | Industrial/PLM & IoT software; large public | Junior Data Analyst / Analytics Engineer | https://ptc.wd1.myworkdayjobs.com/en-US/ptc/job/Boston-MA-USA/Junior-Data-Analyst-Analytics-Engineer_JR112320 | "11d" (≈Jun 9) | Silent, larger company — **verify** | "Analytics Engineer" exact target title + Junior; dbt/SQL overlap; gap: policy unread | speedyapply NEW_GRAD |
| Bristol Myers Squibb | Pharma; large public | Associate Engineer – Analytical AI Engineering | https://bristolmyerssquibb.wd5.myworkdayjobs.com/en-US/bms/job/Princeton---NJ---US/Associate-Engineer--Analytical-AI-Engineering_R1603317-1 | "4d" (≈Jun 16) | Silent, larger company — **verify** | Entry "Associate Engineer, AI Engineering"; applied-AI fit; gap: pharma domain + policy unread | speedyapply NEW_GRAD |

### Tier 2 — Worth a look (good fit, one caveat — almost all caveats are "visa unverified, JD 403")

| Company | What they do / size | Role | Direct link | Posted (basis) | Visa posture | Fit note | Source |
|---|---|---|---|---|---|---|---|
| Tanium | Endpoint management/security; large private | Corporate AI Engineer | https://job-boards.greenhouse.io/tanium/jobs/7967943 | "7h" first-seen (recent; exact post date unread) | Silent, larger company — **verify** | **Addison, TX = candidate-local.** Internal applied-AI tooling fit; caveat: seniority not stated ("Corporate AI Engineer" may be mid, not entry) | zapplyjobs DS tracker |
| PNC | Regional bank; large public | Associate Data Scientist – Corporate & Institutional Banking | https://pnc.wd5.myworkdayjobs.com/en-US/external/job/PA---Pittsburgh-15222/Associate-Data-Scientist---Corporate---Institutional-Banking_R224536-1 | "4d" / Jun 16 | Silent, larger company — **verify** | Entry "Associate DS" at scale; analytics/ML fit; gap: bank policy + GenAI angle | speedyapply + jobright |
| USAA | Insurance/banking for military members; large | Data Scientist I | https://usaa.wd1.myworkdayjobs.com/en-US/usaajobswd/job/Charlotte-NC---CENTS/Data-Scientist-I_R0118100 | "12d" (≈Jun 8) | Silent, larger company — **verify** (serves military but hiring usually not citizen-only) | Entry DS I; solid analytics fit; gap: confirm no citizenship clause | speedyapply NEW_GRAD |
| Warner Bros. Discovery | Media/streaming; large public | Machine Learning Engineer I | https://warnerbros.wd5.myworkdayjobs.com/en-US/global/job/NY-New-York-30-Hudson-Yards/Machine-Learning-Engineer-I_R000100421 | "30d" (≈May 21, edge of window) | Silent, larger company — **verify** | "ML Engineer I" entry rung at a non-FAANG large co; gap: recency at window edge + policy | speedyapply NEW_GRAD |
| TIFIN | Wealth/fintech AI studio; growth-stage | Junior Data Scientist | https://tifin.com/careers/apply/?gh_jid=6007230004 | "23d" (≈May 28) | Silent, growth startup — likely OK | AI-first fintech, junior DS; good applied fit; gap: recency mid-window | speedyapply NEW_GRAD |
| Celonis | Process-mining / execution-management; large private (unicorn) | Associate Value Engineer – AI-Driven DS & Analytics (Orbit Program) | https://job-boards.greenhouse.io/celonis/jobs/7627647003?gh_jid=7627647003 | "14d" (≈Jun 6) | Silent, larger company — **verify** | New-grad "Orbit" program, AI/analytics; adjacent to Forward-Deployed/Solutions; gap: value-eng (customer-facing) vs pure build | speedyapply NEW_GRAD |
| Upgrade | Consumer-fintech (credit/banking); growth-stage | Junior Business & Data Analyst (Remote) | https://job-boards.greenhouse.io/upgrade/jobs/4706312005 | "4d" (≈Jun 16) | Silent, growth startup — likely OK | Remote, junior data analyst; SQL/BI fit; gap: BA-leaning | speedyapply NEW_GRAD |
| Hitachi | Industrial/IT conglomerate; large | Data Scientist I or II (MAD-BS-OR) | https://hitachi.wd1.myworkdayjobs.com/en-US/hitachi/job/HTA-NCP-Hillsboro-OR/Data-Scientist-I-or-II--MAD-BS-OR-_R0128931 | "8d" (≈Jun 12) | Silent, larger company — **verify** | Entry DS I; analytics/ML fit; gap: policy unread | speedyapply NEW_GRAD |
| DISH (EchoStar) | Satellite/wireless; large | Data Scientist I – Customer Lifecycle | https://dish.jibeapply.com/jobs/99226 | "16d" (≈Jun 4) | Silent, larger company — **verify** | Entry DS, lifecycle analytics; gap: policy + churn-modeling vs GenAI | speedyapply NEW_GRAD |
| Marvell | Semiconductors; large public | AI Solutions Analyst – Early Career | https://marvell.wd1.myworkdayjobs.com/en-US/marvellcareers/job/Santa-Clara-CA/AI-Solutions-Analyst---Early-Career_2601236 | "23d" (≈May 28) | Silent, larger company — **verify** | Early-career AI-solutions (adjacent to AI Solutions Engineer); gap: semis domain | speedyapply NEW_GRAD |
| TreeHouse Foods | Private-label food mfg; large | Associate Product Data Scientist | https://treehouse.wd1.myworkdayjobs.com/en-US/treehousecareers/job/USA-WI-De-Pere/Associate-Product-Data-Scientist_R30383 | "15d" (≈Jun 5) | Silent, larger company — **verify** | Entry product DS; analytics fit; gap: CPG domain | speedyapply NEW_GRAD |
| Node | Data/AI services; small | Junior AI/ML Engineer | https://apply.workable.com/node/j/20EDF55068/ | "5d" (≈Jun 15) | Silent, small — likely OK | Junior AI/ML eng at a small shop; strong stack fit; gap: Herndon VA may be govt-adjacent — confirm no clearance | speedyapply NEW_GRAD |
| SyntheticFi | Fintech startup (synthetic/AI finance); seed/early | Founding Data Analyst | https://jobright.ai/jobs/info/6a34fdf1ce501060b5cf2f48 | Jun 19 | Silent, small startup — likely OK | Early "founding" data hire, SF; broad ownership fit; gap: title is analyst not eng | jobright DA tracker |
| Quantifind | Risk/fraud analytics (NLP on entities); mid-size | Associate Data Scientist | https://jobright.ai/jobs/info/698aa6d80f6f7e7a2ce5dc4e | Jun 19 (multiple reqs) | Silent, mid-size — verify | Entry DS, NLP/analytics fit; gap: domain-specific (sanctions/risk) | jobright DA tracker |
| FNBO (First National Bank of Omaha) | Regional bank; mid-large | Associate II – AI Adoption & Enablement (Omaha, onsite) | https://firstnational.wd12.myworkdayjobs.com/en-US/fnbocareers/job/Omaha---FN-Tower/Associate-II--AI-Adoption---Enablement--onsite-Omaha--NE-_R-20261028 | "4d" (≈Jun 16) | Silent, larger company — **verify** | Entry AI-enablement (adjacent to Solutions/FDE); gap: enablement vs build, onsite-only | speedyapply NEW_GRAD |
| Quadric | Edge-AI chip startup; small | Data Scientist – New Grad – Model Optimization | https://apply.workable.com/quadric-dot-i-o-inc/j/5A15DE8CCE/ | "30d" (≈May 21, window edge) | Silent, small startup — likely OK | Explicit New Grad DS; model-optimization fit; gap: recency at edge, HW-adjacent | speedyapply NEW_GRAD |
| Capital One | Bank/fintech; large public | Applied Researcher I – AI Foundations (LLM finetuning/agentic) | https://capitalone.wd12.myworkdayjobs.com/en-US/capital_one/job/New-York-NY/Applied-Researcher-I--AI-Foundations-_R237204 | "11d" (≈Jun 9) | **Verify (Cap One historically restrictive on sponsorship — but OPT needs none)** | LLM-finetuning/agentic = very on-profile; gaps: "Researcher" (research-leaning) + Cap One immigration nuances | speedyapply NEW_GRAD |

### Tier 3 — Long shots / needs verification / likely blocked

| Company | What they do | Role | Direct link | Posted | Visa posture | Why Tier 3 | Source |
|---|---|---|---|---|---|---|---|
| NVIDIA | AI/GPU compute; large public (non-FAANG, in scope) | High-Performance LLM Training Engineer – New College Grad 2026 | https://nvidia.wd5.myworkdayjobs.com/en-US/nvidiaexternalcareersite/job/US-CA-Santa-Clara/High-Performance-LLM-Training-Engineer---New-College-Grad-2026_JR2019451-1 | "4d" (≈Jun 16) — now **in-window** (was recency-unverified prior run) | Silent, larger company — **verify** | In scope & recent, but training-infra/systems-heavy vs applied-AI-product profile — fit gap keeps it here | speedyapply NEW_GRAD |
| Snowflake | Data-cloud platform; large public | AI Research Scientist – New Grad – Agents & Reinforcement Learning | https://jobs.ashbyhq.com/snowflake/1bad12df-f443-426f-9d09-e96fc780d698 | "3d" (≈Jun 17) | Silent, larger company — **verify** | **Now has a real direct URL** (prior run logged it without one). Research-not-applied-eng + needs JD/visa check | speedyapply NEW_GRAD |
| Axon | Law-enforcement tech (tasers/body-cams/cloud); large public | AI Scientist I | https://job-boards.greenhouse.io/axon/jobs/7746492003 | "29d" (≈May 22, window edge) | Unclear — **verify** | LE-adjacent → possible background/citizenship constraints; recency at edge | speedyapply NEW_GRAD |
| Allen Control Systems | Counter-drone robotic weapon systems; startup | Computer Vision & Machine Learning – Junior | https://jobs.ashbyhq.com/allen-control-systems/cfb348d0-ab31-4fa5-9bd5-def1de764ca9 | "17d" (≈Jun 3) | **Likely blocked** — defense/weapons → ITAR US-person very likely | Austin, TX & junior CV/ML (appealing) but ITAR almost certainly disqualifies F-1 OPT | speedyapply NEW_GRAD |
| Sierra Nevada Corporation | Aerospace/defense systems; large | AI Agent Developer I | https://snc.wd1.myworkdayjobs.com/en-US/snc_external_career_site/job/Sparks-NV/AI-Agent-Developer-I_R0030085 | "8d" (≈Jun 12) | **Likely blocked** — defense → US-citizen/clearance likely | Great title (Agent Developer I) but defense prime usually citizen-only | speedyapply NEW_GRAD |
| A-TEK | Federal IT/AI contractor | Federal AI Solutions Engineer – Entry Level | https://job-boards.greenhouse.io/atek/jobs/5250419008 | "10d" (≈Jun 10) | **Likely blocked** — "Federal" → clearance/citizenship likely | Entry AI Solutions Engineer fit, but federal contracting usually US-person | speedyapply NEW_GRAD |
| Oklahoma State Government | State govt | Junior Data Scientist | https://okgov.wd1.myworkdayjobs.com/en-US/okgovjobs/job/Oklahoma-County/Junior-Data-Scientist_JR61363 | "4d" (≈Jun 16) | Unclear — **verify** | Public-sector roles often need state residency / work-auth specifics | speedyapply NEW_GRAD |

### Recency unverified (in-window per tracker age but no calendar date confirmable, JD 403)
| Company | Role | Direct link | Note |
|---|---|---|---|
| KeyBank | Quantitative Analytics Associate / – Capital | https://keybank.wd5.myworkdayjobs.com/en-US/external_career_site/job/Brooklyn-OH/Quantitative-Analytics-Associate_R-40079 | Clean fit for **Quantitative Data Analyst (non-trading-floor)** target; "11d"/Jun 15 per trackers but JD/visa unread. Large bank → verify |
| Hyve Solutions (TD Synnex) | Supply Chain AI & Analytics Associate | https://synnex.wd5.myworkdayjobs.com/en-US/hyvecareers/job/Fremont-CA/Supply-Chain-AI---Analytics-Associate_R51695 | "23d", AI+analytics associate; JD unread |
| Smithfield Foods | Associate AI Enablement Analyst | https://smithfieldfoods.wd1.myworkdayjobs.com/en-US/careers/job/Smithfield-VA/Associate-AI-Enablement-Analyst_R-2026-7552 | "12d", AI-enablement (adjacent to Solutions/FDE); JD unread |

### Excluded (logged so future runs don't re-surface)
- **Defense / federal / clearance (US-person almost certain):** True Anomaly (Autonomy Eng, Platform Eng AI), Inversion Space, Raytheon (Algorithm Systems Eng II, Plano TX), Leidos, GDIT, KBR, Booz Allen, Everwatch, Lentech, AITHERAS, Radiance Technologies, Steampunk, Bluehawk, Dynamis, Integral Federal, Applied Information Sciences, Carnegie Mellon **SEI** roles (FFRDC). All visa-blocked or near-certain.
- **Non-US geography (F-1 OPT is US-only):** Boeing Junior Data Scientist (Richmond, CANADA), AlgaeCal & Amexio (Canada), UniHomes (UK), Wistron NeWeb (Taiwan), Renault (Tunisia), TensorOps (EU remote), Quantiphi (Bengaluru, India).
- **Wet-lab / clinical / non-data research (not applied-AI/data-eng):** Edwards Lifesciences, Exact Sciences, Novartis, MSD, Thermo Fisher, Caris Life Sciences, Flatiron Health (Statistical Programming), Precision AQ/Medicine, Lila Sciences (science-research scientist roles), numerous "Research Assistant/Coordinator/Clinical Data Abstractor" rows on jobright.
- **Already logged 2026-06-20 12:00** (not repeated): Astera Labs NCG 2026, Home Depot Assoc DS (Req183993), Caterpillar Supply Chain DA, Dealer Tire Assoc DS, VHB DS, True Anomaly ML Eng.

### Bonus — adjacent titles worth adding to the search vocabulary
- **"Associate Data Scientist" / "Data Scientist I"** — by far the most common entry rung touching this profile (Jerry, PNC, USAA, Hitachi, DISH, TreeHouse, TIFIN, Quantifind…). Confirm as first-class search term (already flagged last run).
- **"AI Solutions Analyst" / "AI Enablement Analyst/Strategist" / "AI Adoption & Enablement Associate"** (Marvell, Smithfield, FNBO, GlobalFoundries, Housecall Pro) — customer/internal applied-AI roles **adjacent to the Forward-Deployed / AI Solutions Engineer** targets. Many are more "enablement/ops" than build — screen the JD.
- **"Associate Value Engineer (AI)"** (Celonis Orbit) — new-grad program, FDE-adjacent.
- **"Quantitative Analytics Associate"** (KeyBank) / **"Client Quantitative Analyst I"** (BofA) — clean matches for the **Quantitative Data Analyst (non-trading-floor)** target.
- **"Applied Researcher I – AI Foundations"** (Capital One) — LLM-finetuning/agentic work that maps to the candidate's QLoRA/Mistral flagship, though research-titled.
- **"Associate Engineer – Analytical AI Engineering"** (BMS) and **"Engineer I – New Grad – Agentic AI"** (CrowdStrike) — confirm "Agentic AI" as a high-signal keyword for this profile.

### TODO for next (daily) run
- Community boards: HN "Who is hiring" thread id **48357725** is the live board to mine, but HN + Algolia API + GitHub-pages mirrors + workatastartup ALL 403'd the fetcher today — find a readable path (e.g. authenticated fetch, or the `hnrss`/`hnjobs.emilburzo.com` feeds) before relying on it.
- JD/visa verification remains the biggest gap: every ATS host (greenhouse/workday/ashby/oracle/simplify) 403s. Until a readable path exists, all visa buckets stay inferred.
- SimplifyJobs DS/AI/ML section (37 roles) went unread due to README truncation — try fetching its raw listings JSON or paginating.

---

## Run: 2026-06-20 18:30

One thorough daily pass, **24h window** (≈Jun 19–20). Read `leads_log.md` in
full first; de-duped against all prior runs.

**Coverage & honesty notes (read before trusting visa buckets):**
- **Sources read successfully (via `raw.githubusercontent.com`, not blocked):**
  `jobright-ai/2026-Data-Analysis-New-Grad`, `jobright-ai/2026-Business-Analyst-New-Grad`,
  `speedyapply/2026-AI-College-Jobs` (NEW_GRAD_USA), `zapplyjobs/New-Grad-Data-Science-Positions`.
  Filtered each to rows aged **0d/1d** or dated **Jun 19–20**.
- **Blocked again (HTTP 403, unchanged from prior runs):** every individual JD/ATS
  host I tried — `*.myworkdayjobs.com` (Morningstar), `jobs.smartrecruiters.com`
  (SBT Global), `careers.draftkings.com`, `greenhouse.io`. **I could not read a
  single JD body**, so every visa bucket below is inferred from company type +
  role, NOT JD text. Each "verify" must be opened manually.
- **Community boards: still unreadable.** HN "Who is hiring" thread `48357725`
  via Algolia API **403'd**, GitHub-pages mirror `hnjobs.emilburzo.com` **403'd**.
  `SimplifyJobs/New-Grad-Positions` README truncated before its AI/ML section
  (same as prior runs); its `listings.json` exceeded the fetcher's 10 MB content
  limit. **Nothing from community boards logged this run** — none could be machine-read.
- **Recency basis:** jobright rows carry calendar dates (Jun 19/20 used directly);
  speedyapply/zapplyjobs rows carry an "age" field (0d/1d) read against the Jun 20
  tracker refresh. DraftKings date/level/salary confirmed via web search (Built In /
  ZipRecruiter / careers page metadata), JD body itself unread.
- **De-duped out as already logged:** Dealer Tire Assoc DS, Home Depot Assoc DS
  (Req183993), True Anomaly ML Eng I–III, Tanium Corporate AI Engineer, Astera Labs —
  all appear again in trackers today but were logged in prior runs; not repeated.

### Tier 1 — Hot & strong fit
_None clear the bar this run. The freshest new rows are analyst/quant-analyst roles (good target-title fits) but JD bodies 403'd so visa/YoE unverified, and none is a strong applied-GenAI-engineering match. Kept honestly in Tier 2._

### Tier 2 — Worth a look (good fit, one caveat — caveat is "visa unverified, JD 403" unless noted)

| Company | What they do / size | Role | Direct link | Posted (basis) | Visa posture | Fit note | Source |
|---|---|---|---|---|---|---|---|
| SBT Global | Tech/IT services & products; small-mid | Junior Data Analyst – Operations / Sales Analytics | https://jobs.smartrecruiters.com/SBTGlobalInc/3743990013715446-junior-data-analyst-operations-sales-analytics- | "0d" (≈Jun 20) | Silent, small/mid — likely OK | "Junior Data Analyst" = exact entry target title; small co lowers visa risk; gap: ops/sales analytics (BI/SQL) not AI-eng, JD 403 so YoE/visa unread | speedyapply NEW_GRAD |
| Morningstar | Independent investment research/data; large public (~10k) | Associate Quantitative Analyst | https://morningstar.wd5.myworkdayjobs.com/en-US/confidential/job/Chicago/Associate-Quantitative-Analyst_REQ-055869 | "1d" (≈Jun 19) | Silent, larger company — **verify** | Clean fit for **Quantitative Data Analyst (non-trading-floor)** target; investment-research not trading-floor; gap: large-co immigration policy + JD 403 | speedyapply NEW_GRAD |
| DraftKings | Digital sports betting / iGaming; large public | Analyst I, Casino Analytics (Hybrid, Boston) | https://careers.draftkings.com/jobs/jr14374/analyst-i-casino-analytics/ | Jun 20 (jobright date; level/salary confirmed via web) | Silent, larger company — **verify**; NOTE regulated-gaming **state gaming license** may be required (licensure, not citizenship — but adds a background-check step) | Junior analytics, $64–80k, reporting/experiment analysis = solid Data Analyst fit; gaps: iGaming domain + gaming-license step + large-co policy | jobright Data-Analysis + web |

### Tier 3 — Long shots / needs verification / likely blocked

| Company | What they do | Role | Direct link | Posted | Visa posture | Why Tier 3 | Source |
|---|---|---|---|---|---|---|---|
| Defense Unicorns | DoD software/platform (mission software for defense/space); growth-stage | Forward Deployed Engineer – Data Engineer – Space (Remote) | https://job-boards.greenhouse.io/defenseunicorns/jobs/5169676007 | "1d" (≈Jun 19) | **Likely blocked** — DoD/space mission software → US-person / clearance very likely | Title is a bullseye (**Forward Deployed + Data Engineer**, both target titles) and remote, but defense/space programs almost always require US-person; confirm before effort | zapplyjobs DS tracker |

### Excluded (logged so future runs don't re-surface)
- **FAANG-tier (handled separately via referral):** Microsoft – Data Engineer II ("1d"), Amazon – Data Engineer, PV Prime Video TV ("1d").
- **Defense / federal / clearance (US-person near-certain):** Boeing – Business Intelligence Analyst Assoc/Mid (Tukwila WA, Jun 20); Booz Allen Hamilton – Cybersecurity AI/ML Engineer (McLean) and AI/ML Engineer (Arlington); General Dynamics IT – Norwegian Analyst (MacDill AFB).
- **Internship, not FTE:** State Street – BestX AI Engineer (Full-time Internship Jul–Dec 2026).
- **Wet-lab / clinical / non-data research (not applied-AI/data-eng fit):** Edwards Lifesciences – Research Scientist I; Thermo Fisher – Associate Research Scientist (Vaccines); GeneDx – Assistant Clinical Analyst I; Eli Lilly – Post-Doctoral Scientist (Human Genomics); Carta Healthcare – Clinical Data Abstractor; Samaritan Daytop Village – Research Associate.
- **Non-target BA / non-technical analyst rows** (jobright Business-Analyst tracker Jun 19–20): Public Consulting Group (IT BA, public sector), Moose Toys (BA), SFPUC / San Francisco PUC (IS BA), Insurify (BA), Optum (BA), Radiant Logistics (BA), Capital One (Business Analyst Associate – Feb 2027) — these are process/requirements BA roles, not data/analytics-engineering; skipped.
- **Already logged in prior runs** (not repeated): Dealer Tire – Associate Data Scientist; Home Depot – Associate Data Scientist (Req183993); True Anomaly – ML Engineer I–III; Tanium – Corporate AI Engineer; Astera Labs roles.

### Bonus — adjacent titles seen this run
- **"Associate Quantitative Analyst"** (Morningstar) — reinforces the **Quantitative Data Analyst (non-trading-floor)** target at a research/data shop (not a trading desk); good keyword.
- **"Forward Deployed Engineer – Data Engineer"** (Defense Unicorns) — confirms FDE+DataEng combo titles exist new-grad-ish, but the live instances this cycle skew defense; broaden the FDE search toward commercial-SaaS employers (Palantir-style FDE roles at non-defense startups).

### TODO for next (daily) run
- Same two structural blockers persist and are the top priority to solve: (1) every ATS/career host 403s the fetcher → all visa buckets remain inferred, not JD-verified; (2) all HN "who's hiring" paths (Algolia API, emilburzo mirror, GitHub-pages mirror, workatastartup) 403 → community boards still uncovered. Find an authenticated/alternate fetch path for at least one of each.
- SimplifyJobs `listings.json` is >10 MB (fetcher cap) and README truncates before the AI/ML table — try a ranged/paginated fetch or the per-category JSON if one exists.

---

## Run: 2026-06-20 18:48 (DEEP BACKFILL — 30 day window)

**THIS IS A ONE-TIME DEEP BACKFILL, NOT A DAILY PASS.** Second backfill of the
day, run with a wider budget. Uses a **30-day** recency window (~May 21 – Jun 20)
instead of the normal 24h. Future daily runs should keep using 24h and treat
everything below as already-seen. Read `leads_log.md` in full first and de-duped
against ALL prior runs (12:00, 05:21 backfill, 18:30).

**Coverage & honesty notes (read before trusting anything below):**
- **Fully covered (loaded via `raw.githubusercontent.com`, not blocked):**
  - `speedyapply/2026-AI-College-Jobs` → `NEW_GRAD_USA.md` — read in full.
  - `zapplyjobs/New-Grad-Data-Science-Positions` — read in full (large; AI/ML/DataEng
    subsets all pulled). This was the richest source this run (~977 listings / 178 cos).
  - `jobright-ai/2026-Data-Analysis-New-Grad` — loaded, but the tracker now states
    **"only jobs posted in the last 7 days are listed due to capacity constraints,"**
    so its 30-day depth was unavailable this run (only Jun 13–20 rows visible).
  - `jobright-ai/2026-Business-Analyst-New-Grad` — loaded; **no data/analytics-eng
    rows**, only process/requirements BA roles → nothing logged from it.
- **NOT covered / blocked this run (be explicit):**
  - **Individual JD verification — ALL blocked again (HTTP 403):** every ATS host
    (`*.myworkdayjobs.com`, greenhouse, `jobs.ashbyhq.com`, oracle cloud,
    `jobs.smartrecruiters.com`). **I could not read a single JD body**, so EVERY
    visa bucket below is inferred from company type + role, NOT JD text. Every
    "verify" must be opened manually. Same structural blocker as all prior runs.
  - **Seniority caveat:** because JDs are unreadable, roles NOT explicitly labeled
    new-grad/junior/associate-I/"I"/"Officer"/"Launch Program" have **seniority
    unverified** — flagged inline. Several applied-AI titles below could be mid-level.
  - **Community boards — still largely unreadable, but new findings:**
    - HN "Who is hiring (June 2026)" thread `48357725`: HN Algolia items API,
      Algolia search API, `hnrss.org`, and the **`hnhiring.com/june-2026` mirror all
      403'd the fetcher.** A `WebSearch` *over* `hnhiring.com` DID return partial
      text (see Community section) but **no per-post direct links** — so HN leads are
      logged only as informal/no-link items, honestly flagged.
    - **`hnhiring.com` is confirmed to exist and mirrors the thread by month/tech/
      location** (e.g. `/june-2026`, `/locations/remote`, `/technologies/python`).
      It 403s a direct fetch but is searchable. Flag for future runs: try its API or
      an authenticated path.
    - Reddit (`r/dataengineering` search JSON) — **fetch blocked entirely** ("unable
      to fetch from www.reddit.com"). No Discord/Slack boards machine-readable.
  - LinkedIn / Indeed / Glassdoor / Wellfound / startup.jobs: only aggregator landing
    pages or 403s, no per-posting dates or stable direct links — nothing logged from them.
- **Recency basis:** speedyapply/zapplyjobs carry an "age" field (e.g. "2d","5d","30d")
  read against the Jun 20 tracker refresh; zapplyjobs ages in minutes/hours ("14m","2h",
  "7h") are scraper **first-seen** stamps, NOT guaranteed post dates — flagged inline.
  jobright rows carry calendar dates.
- **De-duped out as already logged** (appear again in trackers but NOT repeated below):
  Astera Labs ML NCG (4646633005), Home Depot Assoc DS, Dealer Tire Assoc DS, Caterpillar
  Supply Chain DA, True Anomaly ML, Snowflake AI Research Sci, NVIDIA LLM Training NCG,
  Jerry Assoc DS, CrowdStrike Engineer I Agentic AI, Fortinet Applied AI New Grad (23077),
  Tanium Corporate AI Eng, Capital One Applied Researcher I, KeyBank Quant Analytics Assoc,
  Defense Unicorns FDE Data Eng, SBT Global Jr DA, Morningstar Assoc Quant, DraftKings,
  Unity ML new-grad. (Bank of America Client Quant Analyst I was previously only a *bonus*
  mention — it is logged as a proper row below.)

### Tier 1 — Hot & strong fit
_All entry/early-labeled, recent, non-defense, non-FAANG. Visa buckets inferred (JDs 403)._

| Company | What they do / size | Role | Direct link | Posted (basis) | Visa posture | Fit note | Source |
|---|---|---|---|---|---|---|---|
| AbbVie | Biopharma; large public (~50k) | Associate Data Engineer I | https://jobs.smartrecruiters.com/AbbVie/3743990013652366 | "3d" (≈Jun 17) | Silent, larger company — **verify** | **Explicitly entry ("Associate…I")** Data Engineer — clean fit for the dbt/Airflow/SQL side; gap: pharma domain + large-co policy unread | zapplyjobs DS |
| SS&C Technologies | FinTech/fund-admin software; large public (~27k) | Software & Data Engineer – Financial Technology (Launch Program) | https://ssctech.wd1.myworkdayjobs.com/ssctechnologies/job/Union-NJ/Software---Data-Engineer---Financial-Technology---Launch-Program_R42203 | "2d" (≈Jun 18) | Silent, larger company — **verify** | **"Launch Program" = new-grad track**; data+software eng at a fintech; strong stack overlap; gap: large-co policy unread | zapplyjobs DS |
| Caterpillar | Heavy equipment; large enterprise (non-FAANG) | Data Engineer, Cat Digital Data & AI | https://cat.wd5.myworkdayjobs.com/caterpillarcareers/job/Irving-Texas/Data-Engineer--Cat-Digital-Data---AI_R0000377847 | "2h" first-seen (≈Jun 20) | Silent, larger company — **verify** | **Irving, TX = DFW-local.** Data Eng on a Data & AI team — target title + commute fit; gap: **seniority unverified** (JD 403) + large-co policy | zapplyjobs DS |

### Tier 2 — Worth a look (good fit; caveat = seniority and/or visa unverified, JD 403)

| Company | What they do / size | Role | Direct link | Posted (basis) | Visa posture | Fit note | Source |
|---|---|---|---|---|---|---|---|
| NewsBreak | Local-news/content app w/ ad-AI; growth-stage | Applied AI Engineer, Advertising Agents | https://job-boards.greenhouse.io/newsbreak/jobs/4690262006 | "2d" (≈Jun 18) | Silent, growth-stage — likely OK | **Exact target title** + agentic ad work = bullseye for LangGraph/agent flagship; gap: seniority unverified | zapplyjobs DS |
| State Street | Custody bank / asset servicing; large public | AI Engineer – GenAI & Agentic Systems (Officer) | https://statestreet.wd1.myworkdayjobs.com/Global/job/Quincy-Massachusetts/AI-Engineer---GenAI---Agentic-Systems--Officer-_R-792531 | "3d" (≈Jun 17) | Silent, larger company — **verify** | GenAI + **agentic** = direct match; "Officer" is an entry-professional rung; gap: large-bank policy + Officer≠guaranteed-junior | zapplyjobs DS |
| Citi | Global bank; large public | Generative AI Engineer (Officer) | https://citi.wd5.myworkdayjobs.com/2/job/Jacksonville-Florida-United-States/Generative-AI-Engineer--Officer_26964480-1 | "2d" (≈Jun 18) | Silent, larger company — **verify** | GenAI target title; "Officer" entry rung; gap: large-bank immigration policy unread | zapplyjobs DS |
| Docker | Dev-tools / containers; mid-size private | Machine Learning Engineer | https://jobs.ashbyhq.com/docker/29af4c7f-6c9b-4bb4-a5fa-4950fa292be4/application | "5d" (≈Jun 15) | Silent, mid-size — likely OK | Strong stack-culture fit (Python/Docker-native); mid-size lowers visa risk; gap: seniority unverified | zapplyjobs DS |
| CarGurus | Auto-marketplace; mid-large public | Machine Learning Operations Engineer | https://careers.cargurus.com/us/en/job/8009102?gh_jid=8009102 | "4d" (≈Jun 16) | Silent, larger company — **verify** | **MLOps is a target title**; Airflow/Docker/deploy overlap; gap: seniority unverified | zapplyjobs DS |
| BlackRock | Asset management; large public | Applied AI Engineer – Fundamental Equity Tech | https://blackrock.wd1.myworkdayjobs.com/blackrock_professional/job/San-Francisco-CA/Applied-AI-Engineer---Fundamental-Equity-Tech-Investing-Team_R263834 | "5d" (≈Jun 15) | Silent, larger company — **verify** | Applied-AI target title in an investing-tech team; gap: seniority unverified + large-finance policy | zapplyjobs DS |
| Bank of America | Global bank; large public | Client Quantitative Analyst I – Analytics Transformation | https://ghr.wd1.myworkdayjobs.com/en-US/us-emplsv/job/New-York/Client-Quantitative-Analyst-I---Analytics-Transformation_26019832 | "8d" (≈Jun 12) | Silent, larger company — **verify** | **"I" = entry**; clean fit for the Quantitative Data Analyst (non-trading-floor) target; gap: large-bank policy | speedyapply NEW_GRAD |
| Franklin Templeton | Asset management; large public | Junior Quant Developer | https://franklintempleton.wd5.myworkdayjobs.com/en-US/primary-external-1/job/New-York-New-York-United-States-of-America/Junior-Quant-Developer_868307-1 | "3d" (≈Jun 17) | Silent, larger company — **verify** | **"Junior"** quant dev; Python/SQL fit, quant-analyst-adjacent; gap: large-finance policy | speedyapply NEW_GRAD |
| BlackRock | Asset management; large public | Quantitative Modeler, Associate – QMR | https://blackrock.wd1.myworkdayjobs.com/en-US/blackrock_professional/job/New-York-NY/Quantitative-Modeler--Associate---QMR_R264630-1 | "4d" (≈Jun 16) | Silent, larger company — **verify** | "Associate" rung, quant-modeling; analytics/ML fit; gap: more modeling-heavy than applied-GenAI | speedyapply NEW_GRAD |
| Cape | Privacy-first mobile carrier; startup | Data Engineer | https://jobs.ashbyhq.com/cape/4b93114b-59c0-4f15-91f8-843083b28c3c/application | "2d" (≈Jun 18) | Silent, small startup — likely OK | Startup Data Eng (broad ownership); low visa risk; gap: seniority unverified, NYC onsite likely | zapplyjobs DS |
| AbbVie | Biopharma; large public | Associate Data Engineer II | https://jobs.smartrecruiters.com/AbbVie/3743990013651001 | "3d" (≈Jun 17) | Silent, larger company — **verify** | Same team as the Tier-1 "I" row, one rung up; data-eng fit; gap: "II" may want ~2 yrs | zapplyjobs DS |
| CVS Health | Health services/pharmacy; large public | Data Engineer | https://cvshealth.wd1.myworkdayjobs.com/CVS_Health_Careers/job/TX---Irving/Data-Engineer_R0942270 | "1h" first-seen (≈Jun 20) | Silent, larger company — **verify** | **Irving, TX = DFW-local.** Data-eng fit + commute; gap: seniority unverified + large-co policy | zapplyjobs DS |
| Elevance Health | Health insurer (formerly Anthem); large public | Gen AI Engineer | https://elevancehealth.wd1.myworkdayjobs.com/ANT/job/GA-ATLANTA-740-W-PEACHTREE-ST-NW/Gen-AI-Engineer_JR197275 | "2d" (≈Jun 18) | Silent, larger company — **verify** | GenAI target title; multiple locations; gap: seniority unverified + healthcare-payer policy | zapplyjobs DS |
| Cardinal Health | Healthcare services/distribution; large public | Data/AI Engineer | https://cardinalhealth.wd1.myworkdayjobs.com/EXT/job/US-Nationwide-FIELD/Data-AI-Engineer_20182288 | "5d" (≈Jun 15) | Silent, larger company — **verify** | Data+AI eng, **nationwide/remote-friendly**; stack fit; gap: seniority unverified | zapplyjobs DS |

### Tier 3 — Long shots / needs verification / seniority or domain risk

| Company | What they do | Role | Direct link | Posted | Visa posture | Why Tier 3 | Source |
|---|---|---|---|---|---|---|---|
| Westinghouse Electric | Nuclear power tech; large | Data Scientist – New Grad Leadership Program | https://jobright.ai/jobs/info/6a111f6983d714428982aa0a | Jun 19 | Unclear — **verify** | Explicit new-grad program (appealing) BUT **nuclear → export-control/US-person restrictions plausible**; confirm before effort | jobright DA |
| Zoom | Video/collab SaaS; large public | Machine Learning Engineer | https://zoom.wd5.myworkdayjobs.com/zoom/job/Seattle-WA/Machine-Learning-Engineer_R19190 | "7h" first-seen (≈Jun 20) | Silent, larger company — **verify** | Good ML fit but **seniority unverified** (likely mid); JD 403 | zapplyjobs DS |
| KLA | Semiconductor process control; large public | AI/ML Engineer – Systems | https://kla.wd1.myworkdayjobs.com/Search/job/Ann-Arbor-MI/AI-ML-Engineer---Systems_2635516-1 | "2d" (≈Jun 18) | Silent, larger company — **verify** | Semis/systems-ML heavier than applied-GenAI; seniority unverified | zapplyjobs DS |
| DoorDash | Food delivery; large public (non-FAANG) | Software Engineer, Machine Learning Infrastructure | https://job-boards.greenhouse.io/doordashusa/jobs/8013249 | "2d" (≈Jun 18) | Silent, larger company — **verify** | ML-infra heavy vs applied-AI-product; seniority unverified | zapplyjobs DS |
| Fiserv | Payments/fintech; large public | Machine Learning Software Engineer (AI) | https://fiserv.wd5.myworkdayjobs.com/ext/job/Alpharetta-Georgia/Software-Development-Engineer--AI---ML-_R-10373747 | "6d" (≈Jun 14) | Silent, larger company — **verify** | ML/AI SWE fit; seniority unverified; large-co policy | zapplyjobs DS |
| Tradeweb / ICD | Fixed-income trading-tech / treasury; mid-large | AI Engineer | https://ecnf.fa.us2.oraclecloud.com/hcmUI/CandidateExperience/en/sites/CX/job/301803 | "3d" (≈Jun 17) | Silent, larger company — **verify** | AI Engineer target title at a fintech; **link resolves to a shared Oracle req (Tradeweb/ICD ambiguous)** + seniority unverified | zapplyjobs DS |
| ICF | Consulting (incl. govt clients); large public | Data Engineer (Databricks) – Remote USA | https://icf.wd5.myworkdayjobs.com/ICFExternal_Career_Site/job/Reston-VA/Data-Engineer--Databricks----Remote-USA_R2602105 | "4d" (≈Jun 16) | Unclear — **verify** | Remote + Databricks fit, BUT ICF does federal work → some roles need clearance/US-person; confirm this one is commercial | zapplyjobs DS |
| Astera Labs | Connectivity semis for AI infra; mid-large public | AI/ML Engineer · ML Infrastructure Engineer | https://job-boards.greenhouse.io/asteralabs/jobs/4706552005 · https://job-boards.greenhouse.io/asteralabs/jobs/4706340005 | "4d" (≈Jun 16) | Silent, larger company — **verify** | Additional Astera reqs beyond the logged NCG; ML-for-hardware/infra heavier than RAG/LLM; seniority unverified | zapplyjobs DS |
| Tesla | EV/energy/AI; large (non-FAANG, in scope) | AI Engineer Intern · Applied AI Engineer Intern (AI HW) · ML Platform Intern · Data Engineer Intern | https://www.tesla.com/careers/search/job/259784 · /262946 · /269812 · /269828 | "14m" first-seen — **recency UNVERIFIED** (scraper stamp) | Silent, larger company — **verify** | Target type includes "Intern", but these read as **student internships** and candidate graduates May 2026 → weak timing fit; recency unconfirmed | zapplyjobs DS |

### Community / informal leads (HN "Who is hiring (June 2026)")
_Surfaced only via a `WebSearch` over `hnhiring.com` (the page itself + HN/Algolia APIs all 403'd). **No per-post direct links were obtainable**, so these are logged honestly as unlinked and unverified — do NOT treat as confirmed without finding the original comment._
- **Emergences Labs** — "AI / Systems Engineer," **Remote (US)**, ~$120–150k + equity, building "NeoHuman" (eval-infra desktop product). Stack/role plausibly a strong applied-AI fit. **No direct link captured.**
- **Unnamed early-stage AI fintech** — "Junior Full-Stack Engineer" (web/mobile/AI features, work directly with CEO/CTO). Junior + AI + startup = on-profile, but **no company name or link captured.**
- **Unnamed company** — "Data Engineer (Remote)" building a transformation pipeline on **Snowflake + dbt + Airflow** — near-exact stack match, but **no company name or link captured.**
- **Capital Technology Group** — Senior AI/ML Engineer, Remote US, $150–200k — **EXCLUDED**: senior + explicitly "federal clients" (US-person likely).

### Excluded (logged so future runs don't re-surface)
- **FAANG-tier (referral track):** Microsoft (Data Engineer / Data Engineer II), Amazon/AWS (Data Engineer SCOT-Inbound, PV Prime Video, IAM & Abuse, WW Ops Finance, Decision Intelligence), ByteDance/TikTok interns.
- **Defense / federal / clearance (US-person near-certain):** Booz Allen Hamilton (AI/ML Eng Arlington, Cybersecurity AI/ML McLean, Special Missions DE Fort Benning, Azure DE McLean), GDIT (Agentic AI Eng Falls Church, DE-Junior Camp Smith), Leidos (Computer Vision AI/ML Huntsville, CMDB DE Tampa), KBR (TAGM DE Redstone Arsenal), Guidehouse (DE San Antonio, Palantir DE McLean), Amentum (DE Mid Pearl Harbor), Anduril (DE Quality Intelligence Costa Mesa), Defense Unicorns (FDE DE Space — already logged), Capital Technology Group (federal, from HN).
- **PhD-required / pure research:** Figma (DS Core Data PhD 2026), Citadel Securities (ML Researcher PhD), NVIDIA (Research Scientist Efficient DL NCG; Systems Perf Eng Agentic AI Workloads; Deep Learning Computer Architect — systems/HW), DoorDash (AI Research Fellowship — fellowship + 50d, out of window).
- **Senior/manager/director:** Morgan Stanley (Data AI Engineer, Dir P4), Mastercard (Manager, Data Engineering), Comcast (Data Engineer 3).
- **Wet-lab / clinical:** Carta Healthcare (Clinical Data Abstractor), Edwards Lifesciences (Research Scientist I).
- **Non-target / co-op:** TD Bank (2026 Fall Co-op DE — co-op/student), jobright Business-Analyst tracker rows (process/requirements BA, not data-eng).
- **Generic large-co Data Engineer rows not individually listed** (seniority unverified, lower priority, captured here so they aren't re-surfaced as "new"): Cisco (RTP NC ×2), The Hartford (Charlotte), RELX/LexisNexis (DE II Alpharetta), Vanguard (DE Specialist Wayne PA), Q2 (DE Cary NC), Astreya (Santa Clara), Caterpillar (DE Peoria IL — non-local), Zoom (additional ML reqs R19271/R17822).

### Bonus — adjacent titles worth adding to the search vocabulary
- **"Officer" (Citi/State Street)** — at big banks this is an entry-to-early professional rung; a high-signal keyword for entry-level GenAI/AI-engineer roles that don't say "junior."
- **"Launch Program" / "Leadership Program" (SS&C, Westinghouse)** — new-grad rotational tracks; good keywords to catch entry roles that omit "new grad" in the title.
- **"Associate Data Engineer I/II" (AbbVie)** — explicit entry data-eng rung; add alongside the already-tracked "Associate Data Scientist."
- **"Quant Developer (Junior)" / "Quantitative Modeler, Associate" / "Client Quantitative Analyst I"** (Franklin Templeton, BlackRock, BofA) — reinforce the Quantitative Data Analyst (non-trading-floor) target at asset-managers/banks.
- **"Machine Learning Operations Engineer" (CarGurus)** — confirms MLOps appears as a standalone commercial title (not just at defense/federal shops).
- **"Gen AI Engineer" / "Generative AI Engineer"** (Elevance, Citi) and **"Data/AI Engineer"** (Cardinal Health) — high-signal applied-GenAI keywords at non-tech enterprises.

### TODO for next (daily) run
- **Community boards:** `hnhiring.com` is confirmed to exist and is *searchable* (WebSearch returned text) even though direct fetch + HN/Algolia APIs all 403. Next: try `hnhiring.com`'s JSON/API endpoint or an authenticated fetch to recover per-post links for the June thread (id `48357725`). Reddit fetch is hard-blocked ("unable to fetch from www.reddit.com").
- **jobright Data-Analysis tracker** now caps visible rows at "last 7 days" — for 30-day depth, find its full Airtable/listings export.
- **JD/visa verification** remains the #1 unsolved blocker: every ATS host (workday/greenhouse/ashby/oracle/smartrecruiters) 403s. Until a readable path exists, all visa buckets stay inferred and all "seniority unverified" flags stand.
- **SimplifyJobs** AI/ML category (37 roles) still truncates before loading — try the `dev`-branch raw or a ranged fetch.

---

## Run: 2026-06-24 17:09 (DEEP BACKFILL — 30 day window)

**THIS IS A ONE-TIME DEEP BACKFILL, NOT A DAILY PASS.** Run 2026-06-24 with a
wider budget. Recency window = **last 30 days (~May 25 – Jun 24)** instead of the
normal 24h, to refresh the baseline. Future daily runs should keep using 24h and
treat everything below as already-seen. Read `leads_log.md` in full first and
de-duped against ALL four prior runs (06-20 12:00, 06-20 05:21 backfill,
06-20 18:30, 06-20 18:48 backfill).

**Coverage & honesty notes (read before trusting anything below):**
- **Fully / well covered (loaded via `raw.githubusercontent.com`, not blocked):**
  - `speedyapply/2026-AI-College-Jobs` → `NEW_GRAD_USA.md` — loaded, but the fetcher
    **truncated after ~the first 60 rows** ("200+ additional positions" not rendered),
    so this source is **PARTIAL** this run. FAANG+/Quant/"Other" sections read; the
    long tail of Data/Analytics/ML rows was cut off. Flagged so it isn't treated as complete.
  - `jobright-ai/2026-Data-Analysis-New-Grad` (`master`) — read in full, BUT the tracker
    still **caps visible rows at "last 7 days" (Jun 17–24 only)** due to its stated capacity
    constraint. So its 30-day depth was again unavailable; only Jun 17–24 rows seen.
  - `zapplyjobs/New-Grad-Data-Science-Positions` — read; AI-Engineer / ML-Engineer /
    Data-Engineer / FDE / Analytics-Engineer / Data-Analyst sections pulled (917 listings /
    186 cos claimed). Richest source this run, same as the 06-20 18:48 backfill.
- **NOT covered / blocked this run (be explicit):**
  - **`jobright-ai/2026-AI-Machine-Learning-New-Grad`** — the `master/README.md` path
    **404'd** (repo/branch name likely changed). Did NOT recover an AI/ML-specific jobright
    tracker this run → AI/ML-engineer depth came only from speedyapply (partial) + zapplyjobs.
  - **Individual JD verification — ALL blocked again (HTTP 403):** every ATS host
    (`*.myworkdayjobs.com`, greenhouse, `jobs.ashbyhq.com`, oracle cloud, smartrecruiters).
    **I could not read a single JD body**, so EVERY visa bucket below is inferred from
    company type + role, NOT JD text. Every "verify" must be opened manually. Same
    structural blocker as all four prior runs — unchanged.
  - **Seniority caveat:** because JDs are unreadable, roles NOT explicitly labeled
    new-grad/junior/associate/"I"/"Officer"/"Entry"/"NCG"/"Launch Program" have
    **seniority unverified** — flagged inline.
  - **Community boards — still unreadable by direct fetch (same as every prior run):**
    HN "Who is hiring? (June 2026)" thread is the SAME id **`48357725`** as the 06-20 runs
    (it's still June's thread; July's isn't up yet). I tried 4 paths this run —
    `hn.algolia.com/api/v1/items/48357725` (**403**), `hnhiring.com/june-2026` (**403**),
    `hnhiring.com` remote view (**403**), `nchelluri.github.io/hnjobs/` (**403**). A
    `WebSearch` *over* `hnhiring.com` again returned partial text but **no per-post direct
    links** → HN leads logged below only as informal/unlinked (see Community section).
    Reddit/Discord/Slack: not machine-readable (hard-blocked in prior runs); not re-attempted.
  - LinkedIn / Indeed / Glassdoor / Wellfound / Built In / topstartups: only aggregator
    landing pages, no per-posting dates or stable direct links — nothing logged from them.
    No founder/recruiter LinkedIn post with a stable direct link surfaced this run.
- **Recency basis:** jobright rows carry calendar dates (Jun 17–24 used directly).
  speedyapply rows carry an "age" field ("0d","1d","8d","15d") read against the Jun 24
  refresh. zapplyjobs ages in minutes/hours ("11m","14m","2h","17h","23h") are scraper
  **first-seen** stamps, NOT guaranteed post dates → those rows are flagged
  **recency-unverified** and kept out of the dated tiers where the stamp is sub-day.
- **De-duped out as already logged** (appear again in trackers but NOT repeated below):
  Jerry Assoc DS (now expanded to many NEW US cities incl. **Austin TX**
  `https://jobright.ai/jobs/info/6a39798e06a4fd4b1faba373` & **Remote**
  `https://jobs.ashbyhq.com/jerry.ai/839c4677-34e6-4ba2-ade2-6e4c4fba0414` — company+role
  already logged, new-location links noted here only), Astera Labs ML NCG (4646633005),
  CrowdStrike Engineer I Agentic AI, Capital One Applied Researcher I, NewsBreak Applied AI Eng,
  Elevance Gen AI Eng, Fortinet Applied AI New Grad (23077), Tanium Corporate AI Eng,
  Defense Unicorns FDE DE-Space, Caterpillar DE Cat-Digital Irving (R0000377847), CVS Data Eng
  Irving (R0942279 ≈ prior R0942270), Franklin Templeton Jr Quant Dev, BlackRock Quant Modeler,
  Bank of America Client Quant Analyst I, KeyBank Quant Analytics Assoc, Westinghouse DS NGLP,
  Quantifind Assoc DS, SyntheticFi Founding DA, Caterpillar Supply Chain DA, DraftKings Analyst I
  Casino, Fiserv ML SWE, DoorDash ML-Infra SWE, ICF DE, Cape DE, Snowflake AI Research Sci,
  NVIDIA LLM Training NCG, Quadric DS Model-Opt, Warner Bros ML Eng I.

### Tier 1 — Hot & strong fit
_Entry/new-grad-labeled or exact-target-title, recent (≤~5d), non-defense, non-FAANG. Visa buckets inferred (JDs 403); seniority noted where unverified._

| Company | What they do / size | Role | Direct link | Posted (basis) | Visa posture | Fit note | Source |
|---|---|---|---|---|---|---|---|
| GlobalFoundries | Semiconductor foundry (chip mfg); large public (~13k) | AI/ML Systems Engineer – 2026 New College Graduate | https://globalfoundries.wd1.myworkdayjobs.com/en-US/external/job/USA---Texas---Richardson/AI-ML-Systems-Engineer---2026-New-College-Graduate-_JR-2602829 | 1d (≈Jun 23) | Silent, larger company — **verify** (commercial foundry generally OPT-OK; confirm no export-control clause) | **Richardson, TX = candidate's exact city** + explicit **NCG 2026** + AI/ML title = best authorization×recency×local combo this run; gap: systems/HW-ML heavier than RAG/LLM | speedyapply NEW_GRAD |
| Ramp | Fintech — corporate cards / spend management; growth-stage unicorn (~1k+) | Applied AI Engineer, Fullstack | https://jobs.ashbyhq.com/ramp/6a7e382f-240a-4952-b9e5-7fe2b3856bc9/application | "2h" first-seen (≈Jun 24; recency-unverified scraper stamp) | Silent, growth startup — likely OK (but Ramp is large-ish → verify) | **Exact target title "Applied AI Engineer"** + **Fullstack** = direct match to the ship-end-to-end profile; NYC; gap: seniority unverified (JD 403), recency is a first-seen stamp | zapplyjobs DS |
| Snowflake | Data-cloud platform; large public | Forward Deployed Engineer – Data Engineering | https://jobs.ashbyhq.com/snowflake/9bbafaf2-240d-4cfb-8e95-b289f0350be5/application | 1d (≈Jun 23) | Silent, larger company — **verify** | **FDE + Data Engineering = two bullseye target titles**, and **commercial** (not the defense FDEs seen before); Menlo Park; gap: FDE often expects some customer-facing exp + seniority unverified | zapplyjobs DS |

### Tier 2 — Worth a look (good fit; caveat = seniority and/or visa unverified, JD 403)

| Company | What they do / size | Role | Direct link | Posted (basis) | Visa posture | Fit note | Source |
|---|---|---|---|---|---|---|---|
| Brellium | Healthcare-AI startup (automated clinical chart audit); seed/early | Deployment Associate – AI Solutions | https://jobs.ashbyhq.com/brellium/65f55c9f-4614-4b41-a64b-0cdb6a55792e | 1d (≈Jun 23) | Silent, small startup — likely OK | **"AI Solutions" + entry "Associate" + deployment = Forward-Deployed/AI-Solutions-adjacent** target; startup lowers visa risk; gap: NYC onsite-leaning, deploy/customer-facing vs pure build | speedyapply NEW_GRAD |
| Snowflake | Data-cloud platform; large public | Forward Deployed Engineer – Finance AI | https://jobs.ashbyhq.com/snowflake/9cf335c9-f99d-4ddb-b307-0dcd3a162a09/application | 3d (≈Jun 21) | Silent, larger company — **verify** | Second commercial FDE req (Finance-AI flavor) — fintech-RAG adjacent; gap: seniority unverified | zapplyjobs DS |
| SoFi | Consumer fintech (lending/banking); large public | Associate AI Financial Planning Analyst | https://sofi.com/careers/job/7781335003?gh_jid=7781335003 | "0d" (≈Jun 24) | Silent, larger company — **verify** | Entry "Associate" + applied-AI in fintech; analytics+LLM fit; gap: analyst-leaning vs eng, large-co policy | speedyapply NEW_GRAD |
| GM Financial | Auto-finance arm of GM; large | Data Engineer – Adobe Experience Platform | https://fa-exvu-saasfaprod1.fa.ocs.oraclecloud.com/hcmUI/CandidateExperience/en/sites/CX_1/job/260399 | "17h" first-seen (≈Jun 23; recency-unverified) | Silent, larger company — **verify** | **Irving, TX = DFW-local** + Data-Eng target title; gap: AEP/martech-data niche, seniority unverified | zapplyjobs DS |
| Cox | Telecom/automotive conglomerate; large private | Data Engineer I (Entry Level) | https://cox.wd1.myworkdayjobs.com/Cox_External_Career_Site_1/job/Atlanta-GA/Data-Engineer-I---11361_R202678512 | "14m" first-seen (recency-unverified) | Silent, larger company — **verify** | **Explicitly "Entry Level / Data Engineer I"** — clean dbt/Airflow/SQL fit; gap: recency is a scraper stamp (re-confirm date), large-co policy | zapplyjobs DS |
| BlackRock | Asset management; large public | Associate – Data Engineering | https://blackrock.wd1.myworkdayjobs.com/blackrock_professional/job/Atlanta-GA/Associate---Data-Engineering_R263649-1 | 2d (≈Jun 22) | Silent, larger company — **verify** | **"Associate" entry rung** data-eng; Atlanta; stack fit; gap: large-finance policy | zapplyjobs DS |
| CVS Health | Health services/pharmacy; large public | Associate Data Engineer | https://cvshealth.wd1.myworkdayjobs.com/CVS_Health_Careers/job/RI---Woonsocket/Associate-Data-Engineer_R0942229 | 3d (≈Jun 21) | Silent, larger company — **verify** | **"Associate"** entry data-eng (distinct from the already-logged Irving DE); stack fit; gap: healthcare domain + policy | zapplyjobs DS |
| EquipmentShare | Construction-tech / equipment rental platform; growth-stage | Analytics Engineer | https://www.equipmentshare.com/careers/openings/?gh_jid=8003299 | "14m" first-seen (recency-unverified) | Silent, growth-stage — likely OK | **"Analytics Engineer" exact target title**; dbt/SQL fit; growth-co lowers visa risk; gap: recency is a scraper stamp, seniority unverified | zapplyjobs DS |
| Reach Financial | Consumer-lending fintech; growth-stage | Data Engineer (Remote) | https://job-boards.greenhouse.io/reach/jobs/8597878002 | 2d (≈Jun 22) | Silent, growth startup — likely OK | **Remote** Data-Eng at a fintech; broad-ownership fit; gap: seniority unverified | zapplyjobs DS |
| Zayo | Fiber/network infrastructure; large private | AI Engineer (Remote, US) | https://zayo.wd1.myworkdayjobs.com/Zayo_Careers/job/United-States/AI-Engineer_R0016139 | 5d (≈Jun 19) | Silent, larger company — **verify** | AI-Engineer target title + **US-remote**; gap: seniority unverified (could be mid), infra domain | zapplyjobs DS |
| Qlarant | Healthcare quality / program-integrity analytics; mid-size nonprofit | Data Scientist I | https://jobright.ai/jobs/info/6a3abc3106a4fd4b1fabe9cd | Jun 23 | Silent, mid-size — verify | **Dallas, TX = candidate-local** + entry "DS I"; analytics/anomaly-detection fit; gap: healthcare-integrity domain, GenAI angle | jobright DA |
| GumGum | Contextual-AI ad-tech; mid-size | Data Scientist I | https://jobright.ai/jobs/info/69e32f6bbe46fa3a4ef5984d | Jun 21 | Silent, mid-size — likely OK | Entry "DS I" at an AI-first ad-tech (contextual NLP/CV); good applied fit; gap: ad-tech domain | jobright DA |
| PIMCO | Fixed-income asset manager; large | Quantitative Research Analyst – Client Solutions & Analytics | https://jobright.ai/jobs/info/6a3a60fbdbedbf5680c6f785 | Jun 23 | Silent, larger company — **verify** | **Clean Quantitative Data Analyst (non-trading-floor) fit** — client-solutions analytics, not a trading desk; Python/SQL fit; gap: large-finance policy | jobright DA |
| Capital Group | Asset management (American Funds); large | Quantitative Research Associate – Systematic Portfolio Construction | https://capgroup.wd1.myworkdayjobs.com/en-US/capitalgroupcareers/job/Los-Angeles/Quantitative-Research-Associate---Systematic-Portfolio-Construction_JR6787 | 1d (≈Jun 23) | Silent, larger company — **verify** | "Associate" rung quant-research at an asset manager (non-trading-floor); analytics/ML fit; gap: modeling-heavy, large-finance policy | speedyapply NEW_GRAD |
| American Electric Power | Electric utility; large public | Data Scientist – Associate (Transmission Systems & Asset Health) | https://aep.wd1.myworkdayjobs.com/en-US/aepcareersite/job/New-Albany-OH/Data-Scientist--Associate---Mid----TRANSMISSION-Systems---Asset-Health_R16709-1 | "0d" / Jun 23–24 | Silent, larger company — **verify** | Entry "Associate" DS; anomaly-detection/asset-health = good applied-analytics fit; gap: title says "Associate–Mid" (may want some exp), utility domain | speedyapply + jobright |
| Molina Healthcare | Medicaid/Medicare managed care; large public | Analyst, Finance & Analytics (Advanced SQL / Large-Scale Data) | https://jobright.ai/jobs/info/6a34e09af6b55d12c791e4d7 | Jun 18 | Silent, larger company — **verify** | **Remote** + heavy-SQL analytics; BI/SQL fit; gap: finance-analytics not AI-eng, seniority unverified | jobright DA |
| TRC Companies | Engineering/environmental consultancy; large | Data Analyst – Entry Level | https://jobright.ai/jobs/info/6a3a9f5f06a4fd4b1fabe0bd | Jun 23 | Unclear — **verify** (consultancy may do some govt work) | **Explicit "Entry Level" Data Analyst** in **Houston, TX**; SQL/BI fit; gap: consultancy domain, confirm no govt/clearance scope | jobright DA |
| University of Notre Dame | Private university; large | Data Science Associate | https://jobs.smartrecruiters.com/UniversityOfNotreDame/3743990013754636-data-science-associate?oga=true | "0d" (≈Jun 24) | Silent, university — likely OK (universities often OPT-friendly) | Entry "DS Associate"; broad analytics/ML fit; gap: academic-support data work vs product AI | speedyapply NEW_GRAD |

### Tier 3 — Long shots / needs verification / seniority or domain risk

| Company | What they do | Role | Direct link | Posted | Visa posture | Why Tier 3 | Source |
|---|---|---|---|---|---|---|---|
| Carnegie Mellon University | Private university research; large | Associate Machine Learning Engineer – Secure AI Lab | https://cmu.wd5.myworkdayjobs.com/en-US/cmu/job/Pittsburgh-PA/Associate-Machine-Learning-Engineer---Secure-AI-Lab_2024609 | 15d (≈Jun 9) | Unclear — **verify** | Good entry "Associate MLE" title, BUT **"Secure AI Lab"** + CMU's defense/SEI ties → possible clearance/US-person; confirm this is the open commercial campus role, not SEI/FFRDC | speedyapply NEW_GRAD |
| Hunt Oil Company | Private oil & gas exploration/production; mid-large | AI Engineer | https://fa-eqcd-saasfaprod1.fa.ocs.oraclecloud.com/hcmUI/CandidateExperience/en/sites/CX_1/job/839 | "14m" first-seen (recency-unverified) | Silent, larger company — **verify** | **Dallas, TX = candidate-local** + AI-Engineer title (appealing), BUT **seniority unverified** (likely not entry at a small AI team) + recency is a scraper stamp | zapplyjobs DS |
| F5 | Networking / app-security; large public | AI Engineer | https://ffive.wd5.myworkdayjobs.com/f5jobs/job/Seattle/AI-Engineer_RP1037922 | "11m" first-seen (recency-unverified) | Silent, larger company — **verify** | AI-Engineer title fit but **seniority almost certainly mid+** (no entry marker) + recency is a scraper stamp | zapplyjobs DS |
| Bank of America | Global bank; large public | Associate – Quant | https://ghr.wd1.myworkdayjobs.com/en-US/us-emplsv/job/New-York/Associate---Quant_26020172-1 | 13d (≈Jun 11) | Silent, larger company — **verify** | Quant "Associate" (distinct from the logged Client Quant Analyst I); fit for quant-analyst target; gap: could be markets/trading-floor — JD 403 so unconfirmed | speedyapply NEW_GRAD |
| Disney | Media/streaming; large public (non-FAANG) | Data Engineer II | https://disney.wd5.myworkdayjobs.com/disneycareer/job/New-York-NY-USA/Data-Engineer-II_10154071 | 2d (≈Jun 22) | Silent, larger company — **verify** | Data-Eng fit, but **"II"** likely wants ~2 yrs; seniority risk | zapplyjobs DS |
| FanDuel | Sports betting / iGaming; large | Data Scientist | https://jobright.ai/jobs/info/6a395e80f6b55d12c7927740 | Jun 22 | Silent, larger company — **verify**; regulated-gaming **state license** step possible | DS fit, but seniority unverified + gaming-license background step (licensure, not citizenship) | jobright DA |
| AQR Capital | Quant hedge fund / systematic asset mgmt; large | Quantitative Research Associate | https://careers.aqr.com/jobs?gh_jid=8023897 | "0d" (≈Jun 24) | Silent, larger company — **verify** | On-target quant title BUT AQR is a **systematic-trading shop** (borderline "trading-floor") with a very high research/PhD bar; long shot for this profile | speedyapply NEW_GRAD |

### Recency unverified (in-window per scraper "first-seen" stamp, but no calendar date confirmable; JD 403)
_zapplyjobs minute/hour "first-seen" stamps are NOT post dates — listed separately per the honesty rule. Several already appear in tiers above with the caveat; the ones below are lower-priority or seniority-unclear and parked here._
| Company | Role | Direct link | Note |
|---|---|---|---|
| Esri | Technical Consultant – Enterprise Data | https://www.esri.com/careers/5171874007?gh_jid=5171874007 (Vienna VA; also St Louis 5171873007, Redlands 5171882007) | GIS/enterprise-data consultant; dbt/SQL-adjacent; "23h" first-seen, seniority unverified |
| Uncountable | Scientific Data Engineer (Remote US) | https://jobs.ashbyhq.com/uncountable/48cbdfbc-c377-49bd-b39b-4c2d77357135/application | R&D-data SaaS startup; data-eng fit; "14m" first-seen, seniority unverified |
| Zoetis | Data Engineer | https://zoetis.wd5.myworkdayjobs.com/zoetis/job/Parsippany/Data-Engineer_JR00020850 | Animal-health; data-eng fit; "2d" but JD 403, seniority unverified |
| Procter & Gamble | Data Scientist | https://jobright.ai/jobs/info/68cc1b0b128dc347fd91f322 | Large CPG; DS fit; Jun 19 jobright date but seniority unverified |
| DraftKings | Customer Experience AI Associate | https://draftkings.wd1.myworkdayjobs.com/en-US/employee_referral_portal/job/Boston-MA/Customer-Experience-AI-Associate_JR14486 | Applied-AI "Associate"; **NOTE link is the employee_referral_portal** (may require referral) — find the external-portal URL before applying; "0d" |

### Community / informal leads (HN "Who is hiring? (June 2026)", thread id 48357725)
_Direct fetch 403 on all 4 paths (Algolia API, hnhiring.com, hnhiring remote view, nchelluri mirror) — SAME blocker as every prior run. Surfaced only via `WebSearch` over `hnhiring.com`; **no per-post direct links obtainable**, so logged honestly as unlinked/unverified — do NOT treat as confirmed without finding the original comment._
- **Cora AI** — "Founding Full Stack / **Applied AI Engineer**," Remote (US only, LA/SF pref), ~$190–250k + early equity. Stack = **voice agents, multi-agent orchestration, RAG pipelines, evals** = near-perfect match to the candidate's RAG/LangGraph flagship. **But "Founding" + comp band ⇒ senior-leaning** and "shipped LLMs in production" expected → likely above a new-grad rung. No direct link captured. Informal/long-shot.
- **EggAI** — AI Engineer / Tech Lead, remote **EU / Switzerland / Norway** — **EXCLUDED** (F-1 OPT is US-only; out of geography).
- **L2 Labs** — "Founding Senior SWE," applied-AI lab for data integration — **EXCLUDED** (senior).
- **Quin** — "Founding Engineer (CTO for the right person)," agentic personal-finance, remote US-pref — **EXCLUDED** (founding/exec seniority).
- **Deep Core Technology** — Founding Engineer, **Canada** (CAD comp) — **EXCLUDED** (geography + seniority).

### Excluded (logged so future runs don't re-surface)
- **FAANG-tier (referral track):** Amazon/AWS (Data Engineer I AFT BI, Data Engineer II IAM & Abuse, Data Engineer PV Prime Video, Data Scientist I SCOT-Inbound, Programmer/Analyst Relay, Data Analyst IAG1), Microsoft (Data Engineer II Getting-Customers, Data Engineer II ×1), TikTok/ByteDance (many ML/Applied-Scientist + Data Engineer/Scientist rows), Disney is non-FAANG (kept in Tier 3).
- **Defense / federal / clearance (US-person near-certain):** General Atomics Aeronautical (Data Scientist I, Charlottesville), CACI (Systems Data Eng Integrator + Data Scientist w/ "Clearance Sponsorship"), Booz Allen Hamilton (Data Scientist ×many Fort Meade/Annapolis Jct/Springfield/DC/Stafford/Atlanta; Data Engineer Arlington/McLean/Fayetteville; AI&ML Engineer Chantilly/McLean/Dayton), GDIT (Data Engineer Falls Church; Data Scientist-Junior Jacksonville NC; Norwegian Analyst Tampa/MacDill), KBR (Data Engineer DC-Metro), Guidehouse (Data Engineer Arlington), Command Holdings (Data Analyst "Cleared" El Paso), SAIC (TSA On-Call Data Collector), ECS (Junior Imagery Analyst Fairfax), Accenture Federal (Data Visualization Specialist Suitland), Global Engineering & Technology (Declassification Analyst Entry, College Park/Hyattsville), August Schell (Splunk Eng "Secret"), JP Morgan ML CoE (kept off — large bank, but listed as referral-adjacent), Morgan Stanley AI/ML Eng (PT-JR, senior).
- **Non-US geography (F-1 OPT is US-only):** RBC, Manulife (GRO Toronto/Montreal), Bending Spoons (UK ×3), TMX Group (Toronto), Dalhousie Univ (Halifax), University Health Network (Toronto), WorkSafeBC (Richmond BC), PepsiCo Canada IT co-op, GXO (UK), GCHQ (UK), Aspire Defence (UK), Sureserve (UK), Government of Alberta, Starcom/Kekst/Publicis "Coordinator Applied DS&ML" (Toronto), Exiger (Toronto/Vancouver), CROSSMARK (QC), Explorer Research (Ontario), St. Boniface/WRHA/CancerCare Manitoba (Statistical Programmer, Winnipeg), The Harris Poll (London).
- **Intern / co-op / part-time student (candidate grads May 2026; student programs are weak-fit):** Tesla (AI/Applied-AI/Data-Eng/ML-Platform interns), JM Family (Business Data Eng Intern), Campbell Soup (DE DA&AI / Operational-Support / Agentic-AI-MLOps Co-ops, Camden), Nokia (Data Science Co-op), John Deere (Part-Time Student DS&A ×2), Marmon (DE Intern/Co-op), Sunwater Capital (Fall DE Intern), PlusAI (SWE Intern Data-Infra), Blackstone ("2024" Data Engineer Analyst — stale year tag), Boehringer Ingelheim (Fall Co-Op Clinical DS), Morrison Foerster (Scientific Analyst Intern), Cornerstone Research (Winter Analyst, Dartmouth-only).
- **Senior / staff / lead / PhD-required / pure research:** Salesforce (Data Engineer SMTS/LMTS ×2 — senior), HNTB (Data Engineer III), Comcast (Data Engineer 2 Freewheel), Citadel & Citadel Securities (Quant Researcher / ML Researcher — PhD), NVIDIA (Research Scientist Efficient DL; GenAI-for-Physical-AI PhD; Deep-Learning Computer Architect — systems/HW), Figma (DS Core Data — PhD 2026), D.E. Shaw (AI Strategy & Ops Associate; "ViduZZZi/AgneZZZ" test posts — junk rows), AQR Quant Research Assoc (kept in Tier 3 as long-shot).
- **Wet-lab / clinical / non-data research (not applied-AI/data-eng):** Carta Healthcare (TVT/LAAO, STS, VQI Clinical Data Abstractors), Fred Hutch (Clinical Research Coord, Post-Doc Biostat, Graduate RA, Bioinformatics Analyst I/II), Mayo Clinic (Clinical Data Associate ×several), GeneDx (Assistant Clinical Analyst I), Charles River Labs (Research Analyst I), Weill Cornell / Yale / Tufts / MelroseWakefield / Beth Israel Lahey / Drexel / USC / U Rochester / Dana-Farber / Sarah Cannon / CAMH (Research Assistant/Coordinator/Data Specialist roles), numerous jobright "Research Analyst I / Research Associate / Statistical Programmer / GIS Steward / Sports Data Collector (Genius Sports ×30+) / Field Data Collector / Declassification Analyst" rows.
- **Already logged in prior runs** (appear again; not repeated): Jerry Assoc DS (new-city links noted above), Astera Labs ML NCG, CrowdStrike Engineer I Agentic AI, Capital One Applied Researcher I, NewsBreak Applied AI Eng, Elevance Gen AI Eng, Fortinet Applied AI New Grad, Tanium Corporate AI Eng, Defense Unicorns FDE DE-Space, Caterpillar (Cat-Digital Irving), CVS DE Irving, Franklin Templeton Jr Quant, BlackRock Quant Modeler, BofA Client Quant Analyst I, KeyBank Quant Analytics Assoc, Westinghouse DS NGLP, Quantifind Assoc DS, SyntheticFi Founding DA, DraftKings Analyst I Casino, Fiserv ML SWE, DoorDash ML-Infra, ICF DE, Cape DE, Snowflake AI Research Sci, NVIDIA LLM Training NCG, Quadric DS, Warner Bros ML Eng I.

### Bonus — adjacent titles worth adding to the search vocabulary
- **"Forward Deployed Engineer – Data Engineering / Finance AI" (Snowflake, COMMERCIAL)** — confirms FDE roles exist at a major non-defense data-cloud co (prior FDE sightings were all defense). Add "Forward Deployed Engineer" as a first-class commercial search term, not just defense.
- **"Deployment Associate – AI Solutions" (Brellium)** — entry-level Forward-Deployed/AI-Solutions title at a startup; high-signal for the candidate's FDE/Solutions target.
- **"Associate AI Financial Planning Analyst" (SoFi) / "Customer Experience AI Associate" (DraftKings)** — applied-AI "Associate analyst" titles in consumer fintech/gaming; entry rungs that hide the AI work behind an "Analyst/Associate" label.
- **"Quantitative Research Analyst – Client Solutions" (PIMCO) / "Quantitative Research Associate" (Capital Group, AQR)** — reinforce the **Quantitative Data Analyst (non-trading-floor)** target at asset managers (client-solutions/portfolio-construction, not a trading desk).
- **"Data Engineer I (Entry Level)" (Cox) / "Associate – Data Engineering" (BlackRock) / "Associate Data Engineer" (CVS)** — explicit entry data-eng rungs; keep alongside the already-tracked "Associate Data Scientist."
- **"AI/ML Systems Engineer – New College Graduate" (GlobalFoundries, Richardson TX)** — local DFW new-grad AI/ML title at a semiconductor foundry; note the DFW-local cluster this run: GlobalFoundries (Richardson), GM Financial + Caterpillar Cat-Digital (Irving), Hunt Oil + Jerry Assoc DS (Dallas), Qlarant (Dallas).

### TODO for next (daily) run
- **speedyapply NEW_GRAD_USA fetch truncated** after ~60 rows this run (the long Data/Analytics/ML tail didn't render) — next time fetch in ranged chunks or target the section anchors so the full list loads.
- **jobright AI/ML-New-Grad tracker `master/README.md` 404'd** — find its current repo/branch name (it likely renamed); without it, AI/ML-engineer depth leans entirely on zapplyjobs + the partial speedyapply.
- **Community boards:** unchanged blocker — HN thread `48357725` (still June) + Algolia API + hnhiring + nchelluri mirror ALL 403 direct fetch; only `WebSearch`-over-hnhiring returns text, and **without per-post links**. Still the #1 unsolved community gap. Watch for the **July 2026** "Who is hiring" thread to open (~Jul 1).
- **JD/visa verification** remains the #1 structural blocker: every ATS host (workday/greenhouse/ashby/oracle/smartrecruiters) 403s → all visa buckets inferred, all "seniority unverified" flags stand.

---

## Run: 2026-06-25 17:30 (DEEP BACKFILL — 30 day window)

**THIS IS A ONE-TIME DEEP BACKFILL, NOT A DAILY PASS.** Run 2026-06-25 with a
wider budget. Recency window = **last 30 days (~May 26 – Jun 25)** instead of the
normal 24h, to refresh the baseline. Future daily runs should keep using 24h and
treat everything below as already-seen. Read `leads_log.md` in full first and
de-duped against ALL five prior runs (06-20 12:00, 06-20 05:21 backfill,
06-20 18:30, 06-20 18:48 backfill, 06-24 17:09 backfill).

**Coverage & honesty notes (read before trusting anything below):**
- **METHOD CHANGE that worked this run:** instead of `WebFetch` (which runs a
  small model that truncated the trackers after ~60 rows on every prior run), I
  **`curl`-ed the raw markdown files directly** (raw.githubusercontent.com is NOT
  blocked) and parsed them locally with Python. This let me read sources **in
  full** for the first time, including the SimplifyJobs DS/AI/ML section that
  truncated on all 5 prior runs. **Recommend all future runs use curl+local-parse,
  not WebFetch, for the trackers.**
- **Fully covered (curl'd raw + parsed locally):**
  - `speedyapply/2026-AI-College-Jobs` → `NEW_GRAD_USA.md` — read in full (246
    rows; FAANG+/Quant/Other sections all parsed; 125 rows ≤30d). No truncation
    this run.
  - `zapplyjobs/New-Grad-Data-Science-Positions` → `README.md` — read in full
    (339 apply-rows across Data Scientist/AI-Eng/ML-Eng/Data-Eng/Data-Analyst/FDE).
  - `jobright-ai/2026-Engineering-New-Grad` → `README.md` — read in full (6,106
    rows; this is where AI/ML-Engineer new-grad rows live — the old
    `2026-AI-Machine-Learning-New-Grad` repo that 404'd last run **does not exist**;
    AI/ML roles are under the Engineering repo). Calendar-dated.
  - `jobright-ai/2026-Data-Analysis-New-Grad` → `README.md` — read in full, BUT
    the tracker still **caps visible rows at "last 7 days" (Jun 17–25 only)** per
    its stated capacity constraint, so 30-day depth unavailable (same as 06-24).
  - `jobright-ai/2026-Business-Analyst-New-Grad` — read; **0 data/analytics-eng
    rows** (only process/requirements BA) → nothing logged from it.
  - `SimplifyJobs/New-Grad-Positions` (`dev` branch) — **DS/AI/ML section read IN
    FULL for the first time** (lines 10224–12389). Finding: Simplify's list is
    mostly **stale** — almost all DS/AI/ML rows are aged 1mo–7mo (outside window);
    only 3 in-window net-new rows (BCBST, blend360, Murj — see Recency-unverified).
    So Simplify adds little for a 30-day window; useful mainly as a backstop.
- **NOT covered / blocked this run (be explicit) — UNCHANGED structural blockers:**
  - **Individual JD verification — ALL still blocked.** Tested this run:
    `curl` to greenhouse + jobright.ai both returned **000 (CONNECT denied by
    egress policy)**; `WebFetch` to jobright.ai returned **403**. So I **could not
    read a single JD body** — EVERY visa bucket below is inferred from company type
    + role, NOT JD text. Every "verify" must be opened manually. Seniority for any
    role NOT explicitly labeled new-grad/junior/associate/"I"/entry/NCG is
    **unverified** and flagged inline.
  - **Community boards — HN still unreadable by direct fetch.** HN "Who is hiring?
    (June 2026)" is the SAME thread id **`48357725`** (June thread still current;
    July's not up yet — watch ~Jul 1). `curl` to `hn.algolia.com/api/v1/items/48357725`
    = **000**. Only a `WebSearch` *over* HN/hnhiring returned partial text with
    **no per-post direct links** → HN leads logged below as informal/unlinked.
    Reddit/Discord/Slack not machine-readable (hard-blocked prior runs).
  - LinkedIn / Indeed / Glassdoor / Wellfound / startup.jobs: only aggregator
    landing pages, no per-posting dates or stable direct links — nothing logged.
    No founder/recruiter post with a stable direct link surfaced this run.
- **Recency basis:** jobright rows carry calendar dates (Jun 17–25 used directly).
  speedyapply rows carry an "age" field ("0d".."30d") read against the Jun 25
  refresh — reliable to the day. zapplyjobs ages in minutes/hours ("10m","14m","1h",
  "19h") are scraper **first-seen** stamps, NOT guaranteed post dates → those rows
  are flagged **recency-unverified** inline and the sub-day ones are treated as
  "≈within window, exact date unconfirmed."
- **Useful new signal:** zapplyjobs now carries a **Visa column** — `🏛 H-1B Co.`
  (company is a known H-1B sponsor → generally OPT-friendly) / `✅ Sponsor` /
  blank (unknown). Noted per-row below where present. This is a *company-level*
  sponsorship signal, NOT a per-JD guarantee — still verify.
- **De-duped out as already logged** (appear again in trackers but NOT repeated
  below): GlobalFoundries AI/ML Systems NCG (Richardson), Ramp Applied AI Eng,
  Snowflake FDE, Brellium Deployment Assoc, SoFi, GM Financial, Cox DE I (Atlanta),
  BlackRock (Quant Modeler QMR/Securitized/Aladdin + Assoc Data Eng), CVS, Caterpillar,
  Home Depot Assoc DS, KeyBank Quant Analytics Assoc, Franklin Templeton Jr Quant,
  Bank of America (Client Quant Analyst I / Assoc-Quant), Hitachi DS I/II, USAA DS I,
  Marvell AI Solutions Analyst, TreeHouse Assoc Product DS, A-TEK Federal AI Solutions,
  Excellus/Univera AI Eng I/II, Node Jr AI/ML, PNC Assoc DS, Unity ML NewGrad,
  Upgrade Jr B&D Analyst, PTC Jr DA/Analytics Eng, Capital Group Quant Research Assoc,
  Carnegie Mellon Assoc MLE (Secure AI Lab), TRC Data Analyst Entry (Houston),
  Westinghouse DS NGLP, AQR Quant Research Assoc, Jerry Assoc DS (NY/Remote new-loc
  links only), Qlarant/GumGum/PIMCO/SyntheticFi, Esri Technical Consultant (Esri
  **Data Scientist I** is NEW and logged below).
- **Excluded as out-of-scope** (logged so future runs don't re-surface):
  - **FAANG-tier (referral track):** Amazon/AWS (Data Engineer I/II, Applied/Quantum
    Applied Scientist, Annapurna Labs), Microsoft, Adobe University-Grad ML (kept in
    Tier 3 — Adobe is non-FAANG, in scope), TikTok/ByteDance (many), Meta, Apple, Google.
  - **Defense / federal / clearance (US-person near-certain):** Booz Allen (AI/ML Eng
    Arlington/Chantilly/Hampton, DS Junior Springfield), GDIT (DS-Junior Jacksonville),
    Guidehouse (DS/DA/DE DC/Houston/McLean/Arlington), General Atomics (DS I
    Charlottesville), Radiance (DS Dahlgren, Jr DA), Everwatch (AI/ML Jr Annapolis Jct),
    Lentech (Jr DS Fort Meade), Peraton (GenAI Eng Intern), AMERICAN SYSTEMS (DE Jr
    Quantico), SMX (DE Jr TS/SCI Fort Belvoir), Columbia Technology Partners (SIGDEV
    Annapolis Jct), ITA International (Jr DA), CATHEXIS (Assoc AI/ML — govt consultancy,
    verify), LMI/MetroStar (govt). Simple Technology Solutions kept in Tier 3 (verify
    federal scope).
  - **Non-US geography (F-1 OPT is US-only):** SOCAN + RBC + WPP Media + PepsiCo +
    Open Farm (Canada), Bending Spoons + Howden + Ekimetrics + Alpha FMC + Goodnotes +
    Sonos + Unison + WPP (UK), TrendAI (Ottawa), Baker Hughes (India), HP AI Lab (Spain).
  - **Wet-lab / clinical / pure-research:** Revolution Medicines (Quant Systems
    Pharmacologist), Thermo Fisher (Scientist II/III Bioprocess), Elanco (Research
    Scientist), Carle Health (Research Data Fellow), Joslin Diabetes (DA Vascular Cell
    Bio), Brookhaven (Postdoc ML X-Ray), MatX (ML Researcher 2025-dated).
  - **Trading-floor quant / PhD-required (profile wants non-trading-floor only):**
    Citadel Securities (Quant Researcher PhD), Hudson River Trading (Jr Treasury/Latency
    Quant), AllianceBernstein/Stevens Capital/Vanguard Quant-MBS (Quant Researcher),
    Old Mission/Galaxy/Morgan Stanley (Quant Trader/Desk Strategist), MFS Quant Research
    Assoc, Trexquant.
  - **Senior / II+ / intern / co-op / part-time:** PwC AI Eng "Experienced Associate",
    Snap (Level 4/5), Adobe Applied Scientist, Qualtrics Applied Scientist II, Spotify
    DS, Arrive Logistics DS II, Travelers DE II, Rocket Companies DA II, Anthropic
    Manager Applied AI, Nelnet/Tesla/d-Matrix/Campbell Soup/IDEXX/JM Family/Nuro
    (interns/co-ops), Aptura (part-time AI residency).

### Tier 1 — Hot & strong fit
_Entry/new-grad-labeled or exact-target-title, recent (≤5d where calendar-dated),
non-defense, non-FAANG. Visa buckets inferred (JDs all 403/000); seniority noted._

| Company | What they do / size | Role | Direct link | Posted (basis) | Visa posture | Fit note | Source |
|---|---|---|---|---|---|---|---|
| UST HealthProof | Healthcare-admin/claims platform (UST subsidiary); mid-large | Associate Data Engineer (Early Career Talent) | https://jobright.ai/jobs/info/6a3a1470214ae004c7a214f7 (Frisco TX) · https://jobright.ai/jobs/info/6a394f81649fdf1629300301 (Bellevue WA) | Jun 22 (3d, jobright cal.) | Silent, mid-large — verify | **Frisco, TX = DFW-LOCAL** + explicit "Associate / Early Career" Data Engineer = clean dbt/Airflow/SQL entry fit; gap: healthcare-claims domain | jobright ENG |
| WelbeHealth | Value-based senior care (PACE) provider; growth-stage (~1k) | AI Engineer I | https://job-boards.greenhouse.io/welbehealth/jobs/8599687002 (jobright: https://jobright.ai/jobs/info/6a3c6637122f340d29cedd06) | Jun 24 (1d jobright / 0d speedy) | Silent, growth-stage — likely OK | **Explicit "AI Engineer I" entry rung** — exact target title at the lowest level; LA; gap: healthcare-ops domain, JD/visa unread | jobright ENG + speedy |
| SentiLink | Fraud/identity-verification fintech; growth-stage startup | Data Scientist, New Grad | https://jobs.ashbyhq.com/sentilink/3cb2885e-7a58-4a14-94d5-b7b851053408/application (jobright: https://jobright.ai/jobs/info/69e8bc1f7820c036924e28f5) | Jun 24 (1d) | Silent, growth startup — likely OK | **Explicit "New Grad"** DS at a startup (low visa risk); fraud/anomaly-detection ML maps to the candidate's anomaly-detection work; Chicago/remote | jobright ENG + Simplify |
| Oscar Health | Health-insurance tech ("Hyperion" platform); large public | Analytics Engineer I | http://www.hioscar.com/careers/7872595?gh_jid=7872595 (jobright: https://jobright.ai/jobs/info/6a07085324dcb03739f1f0d0) | Jun 20 (5d) | Silent, larger company — **verify** | **"Analytics Engineer I" = exact target title + explicit "I" entry**; dbt/SQL fit; NYC; gap: large-co immigration policy unread | jobright ENG + Simplify |
| OneStream Software | Corporate-performance-management (EPM) SaaS; large private | Associate AI Engineer | https://jobright.ai/jobs/info/6a39bba0649fdf1629302ad2 | Jun 23 (2d) | Silent, larger company — **verify** | **Explicit "Associate AI Engineer"** entry rung at a finance-software co; applied-AI fit; Birmingham MI; gap: policy unread | jobright ENG |

### Tier 2 — Worth a look (good fit; caveat = seniority and/or visa unverified, JD 403/000)

| Company | What they do / size | Role | Direct link | Posted (basis) | Visa posture | Fit note | Source |
|---|---|---|---|---|---|---|---|
| Capgemini | IT/consulting services; large public | Junior Power BI Developer | https://jobright.ai/jobs/info/6a3a47281232144fb156e44a | Jun 24 (1d) | Silent, larger company — **verify** (consultancy; some govt work) | **Dallas, TX = LOCAL** + **"BI Developer" = exact target title** + "Junior"; SQL/BI fit; gap: consultancy may staff govt accounts | jobright DA |
| SCP Health | Clinical/hospital-medicine management; mid-large | Business Data Analyst I | https://jobright.ai/jobs/info/6a3cb118d261407de97fe594 | Jun 24 (1d) | Silent, mid-large — verify | **Dallas, TX = LOCAL** + entry "Data Analyst I"; SQL/BI fit; gap: healthcare-ops analytics vs AI-eng | jobright DA |
| Paramount Global | Media/streaming; large public (non-FAANG) | Machine Learning Engineer, Entry | https://careers.paramount.com/job/New-York-Machine-Learning-Engineer,-Entry-NY-10036/1389620800/?ats=successfactors | "14m" first-seen (≈within window, exact date unconfirmed) | Silent, larger company — **verify** | **Explicit "Entry" ML Engineer** at a major media co; applied-ML fit; Burbank/NY; gap: large-co policy, recency is a scraper stamp | zapplyjobs |
| LabCorp | Clinical-lab diagnostics; large public | Associate Data Scientist | https://labcorp.wd1.myworkdayjobs.com/external/job/USA---NC---Durham---10-Moore-Drive/Associate-Data-Scientist_2612605 | "12m" first-seen (recency-unverified) | Silent, larger company — **verify** | Entry "Associate" DS (data role, not wet-lab); Durham NC; analytics/ML fit; gap: large-co policy + recency stamp | zapplyjobs |
| UL Solutions | Safety-science testing/certification; large public | Associate Data Scientist · Associate Business Data Analyst | https://jobright.ai/jobs/info/6a362e85ce501060b5cf669c (DS, Northbrook IL) · https://jobright.ai/jobs/info/6a365faa649fdf16292fb61e (BDA, Raleigh NC) | Jun 25 (0d) / Jun 19 (6d) | Silent, larger company — **verify** | Two explicit "Associate" entry rows (DS + Business DA); analytics fit; gap: large-co policy | jobright ENG + DA |
| New York Life | Life insurance; large mutual | Associate - Data Scientist | https://jobright.ai/jobs/info/6a0851f1a203b1052e443bd8 | Jun 20 (5d) | Silent, larger company — **verify** | Entry "Associate" DS at an insurer; analytics/ML fit; NYC; gap: policy unread | jobright ENG |
| CBTS | IT services/managed-tech (Cincinnati Bell sub); mid-large | Data Engineer I (W2 only, no third-party) | https://jobright.ai/jobs/info/6a2c15a3a1d15e3c552f9f43 | Jun 24 (1d) | Silent, mid-large — verify (W2-only note suggests no-C2C, OPT generally fine) | Explicit "Data Engineer I" entry; dbt/SQL fit; Cincinnati OH; gap: IT-services domain | jobright ENG |
| Innodata Inc. | Data-engineering / data-for-AI (LLM data, annotation); small-mid public | Applied AI Associate · Generative AI Associate | https://jobright.ai/jobs/info/6a291bb31dbd8437bebcefae (Applied AI, Remote-RI) · https://jobright.ai/jobs/info/6a3201265958816970017e14 (GenAI, Remote-NH) | Jun 24 (1d) | Silent, small-mid — likely OK | **Remote** + entry "Associate" applied/gen-AI at a data-for-LLM company = strong stack fit (RAG/LLM data); gap: annotation-ops vs pure build (Turkish-speaking GenAI variant excluded — language req) | jobright ENG |
| XiFin, Inc. | Healthcare revenue-cycle / lab-billing SaaS; mid-size | Associate Machine Learning Engineer | https://jobright.ai/jobs/info/6a37bfdace501060b5cf8cdf | Jun 21 (4d) | Silent, mid-size — verify | Explicit "Associate ML Engineer" entry; San Diego; applied-ML fit; gap: healthcare-billing domain | jobright ENG |
| Wonderschool | Childcare-marketplace / ops SaaS; growth-stage startup | Early Career Software Engineer – Applied AI | https://jobright.ai/jobs/info/6a369d4329c90c607e4e549a | Jun 20 (5d) | Silent, growth startup — likely OK | **"Early Career" + "Applied AI"** at a startup (low visa risk); SF; ship-end-to-end fit; gap: SWE-leaning, onsite-likely | jobright ENG |
| CyberProof (UST) | Managed cybersecurity services; mid-large | Associate Data Engineer (Early Career Talent) | https://jobright.ai/jobs/info/6a394f01f6b55d12c79272e2 | Jun 22 (3d) | Silent, mid-large — verify | Explicit "Associate / Early Career" DE; Seattle/Bellevue; dbt/SQL fit; gap: security-services domain | jobright ENG |
| Allstate | Insurance; large public | Applied Machine Learning Engineer (All Levels) | https://allstate.wd5.myworkdayjobs.com/allstate_careers/job/USA---IL-Remote/Applied-Machine-Learning-Engineer--All-Levels-_R27180-1 | "28m" first-seen (recency-unverified) | Silent, larger company — **verify** | "**All Levels**" explicitly includes entry; **IL-Remote**; applied-ML fit; gap: large-co policy + recency stamp | zapplyjobs |
| DHL Supply Chain | Logistics/supply-chain; large | Business Data Analyst I | https://jobright.ai/jobs/info/6a3ce4668bfad862bc99b682 | Jun 25 (0d) | Silent, larger company — **verify** | Entry "Data Analyst I"; supply-chain analytics; Mechanicsburg PA; SQL/BI fit | jobright DA |
| Bread Financial | Consumer-credit fintech; large public | Data Scientist | https://alliancedata.wd5.myworkdayjobs.com/breadfinancial_us/job/Columbus-OH/Data-Scientist_R1012772 | "2d" first-seen (≈within window) | Silent, larger company — **verify** | DS at a fintech; analytics/ML fit; Columbus OH; gap: **seniority unverified** (no entry marker) | zapplyjobs |
| Coca-Cola | Beverages; large public | Data Analyst (Data Solutions) | https://coke.wd1.myworkdayjobs.com/coca-cola-careers/job/US---GA---Atlanta/Data-Analyst--Data-Solutions-_R-142380 | "10m" first-seen (recency-unverified) | Silent, larger company — **verify** | Data-Analyst target title; Atlanta; SQL/BI fit; gap: seniority unverified, recency stamp | zapplyjobs |
| Brown & Brown Insurance | Insurance brokerage; large public | Data Engineer (Remote, USA) | https://bbinsurance.wd1.myworkdayjobs.com/careers/job/Remote---USA/Data-Engineer_R26_0000002275 | "1h" first-seen (recency-unverified) | Silent, larger company — **verify** | **Remote** Data Eng; dbt/SQL fit; gap: seniority unverified, recency stamp | zapplyjobs |
| RELX (LexisNexis) | Data/analytics & risk info; large public | AI Data Analyst | https://relx.wd3.myworkdayjobs.com/relx/job/Alpharetta-GA/AI-Data-Analyst_R113755-1 | "3d" first-seen | 🏛 H-1B Co. (zapply) → likely OPT-OK, verify | Adjacent "AI Data Analyst" title; Alpharetta GA; analytics+AI fit; gap: seniority unverified | zapplyjobs |
| TD Synnex | IT distribution/services; large public | Physical AI Engineer – Simulation & Synthetic | https://synnex.wd5.myworkdayjobs.com/tdsynnexcareers/job/Clearwater-Florida-United-States/Physical-AI-Engineer_R50658 | "25m" first-seen (recency-unverified) | 🏛 H-1B Co. (zapply) → likely OPT-OK, verify | Novel "Physical AI Engineer" title (sim/synthetic-data); applied-AI fit; Clearwater FL; gap: seniority unverified | zapplyjobs |
| Cushman & Wakefield | Commercial real-estate services; large public | Junior Data Scientist | https://cw.wd1.myworkdayjobs.com/en-US/external/job/Chicago-Illinois-USA/Junior-Data-Scientist_R325784 | "1d" (speedy age) | Silent, larger company — **verify** | Explicit "Junior" DS; Chicago; analytics/ML fit; gap: CRE domain, policy | speedy |
| Truist Bank | Regional bank; large public | Data Scientist, Level I / Level II | https://truist.wd1.myworkdayjobs.com/en-US/careers/job/Charlotte-NC/Data-Scientist--Level-I---Level-II-_R0116103-1 | "2d" (speedy age) | Silent, larger company — **verify** | Entry "Level I" rung available; Charlotte NC; analytics/ML fit; gap: bank policy | speedy |
| Careerswift | AI-recruiting/matching platform; small startup | Data Analyst (Junior/Mid) | https://jobs.ashbyhq.com/careerswift.ai/2f78c5da-f74e-4bf2-8b8d-c092c6d4a8d7 | "9d" (speedy age) | Silent, small startup — likely OK | Junior DA at a small AI startup (low visa risk); SF; SQL/BI fit; gap: tiny co, role scope unclear | speedy |

### Tier 3 — Long shots / needs verification / seniority or domain risk

| Company | What they do | Role | Direct link | Posted | Visa posture | Why Tier 3 | Source |
|---|---|---|---|---|---|---|---|
| Adobe | Creative/doc software; large public (non-FAANG, in scope) | 2026 University Graduate – Machine Learning Engineer | https://jobright.ai/jobs/info/6a200346902d19201c7afec9 | Jun 22 (3d) | Silent, larger company — **verify** | In-scope new-grad ML, but very competitive + large-co immigration policy; Seattle | jobright ENG |
| Qualcomm | Semiconductors / wireless; large public | Machine Learning Engineer – College Graduate | https://jobright.ai/jobs/info/6a0fa3f580bf0430c76357ef | Jun 22 (3d) | Silent, larger company — **verify** | New-grad ML, but semis/edge-ML heavier than applied-GenAI; San Diego | jobright ENG |
| Esri | GIS/mapping software; large private | Data Scientist I | https://www.esri.com/careers/5173232007?gh_jid=5173232007 | "0d" (speedy age) | Silent, larger company — **verify** | Entry "DS I" (Esri previously logged only as Tech Consultant); St Louis MO; GIS-data domain | speedy |
| iSoftStone | IT services/consulting & staffing; large | Associate AI/ML Developer | https://jobright.ai/jobs/info/6a2f28a1d3ec94183f4c19be | Jun 24 (1d) | Unclear — **verify** | Entry AI/ML title but staffing/consultancy → confirm it's a direct FTE, not bench/C2C; NY hybrid | jobright ENG |
| EITACIES Inc. | IT consultancy / staffing; small | Junior AI Engineer (Entry-Level, Freshers Welcome) | https://jobright.ai/jobs/info/6a3ab12006a4fd4b1fabe557 | Jun 23 (2d) | Unclear — **verify** | "Freshers welcome" entry AI Eng but staffing-flavored → verify direct-hire/visa; Santa Clara/remote | jobright ENG |
| Digital United | Digital/AI solutions agency; small-mid | AI Solutions Associate | https://jobright.ai/jobs/info/6a05f921320bff2205ea6886 | Jun 22 (3d) | Unclear — **verify** | Entry "AI Solutions Associate" (FDE/Solutions-adjacent) but company opacity → verify; US (remote?) | jobright ENG |
| Ursa Space Systems | Satellite-data / geospatial-intelligence analytics; startup | Jr. AI Engineer | https://jobright.ai/jobs/info/6a3990b01232144fb156c00c | Jun 22 (3d) | Unclear — **verify** | Entry AI Eng at a commercial space-analytics co, BUT geospatial-intel may carry export-control/US-person constraints; Ithaca NY | jobright ENG |
| Brex | Corporate-card/spend fintech; growth unicorn | AI Engineer, Ecosystem · AI Engineer, Product | https://www.brex.com/careers/8606890002?gh_jid=8606890002 (Ecosystem) · https://www.brex.com/careers/8606845002?gh_jid=8606845002 (Product) | "19h" first-seen (recency-unverified) | 🏛 H-1B Co. (zapply) → likely OPT-OK | Exact "AI Engineer" title at a strong fintech, BUT **no entry marker → seniority likely mid+**; SF/Seattle | zapplyjobs |
| WorldQuant | Quant asset manager; large | Junior Quantitative Analyst | https://job-boards.greenhouse.io/worldquant/jobs/4616499006 | "16d" (speedy age) | Silent, larger company — **verify** | "Junior" quant analyst, **Austin TX (≈local)**, BUT WorldQuant is a systematic-trading shop (borderline trading-floor) with a high research bar | speedy |
| Cross River Bank | Banking-as-a-service fintech; mid-large | Associate/AVP – Quantitative Strategies Group | https://www.crossriver.com/greenhouse?gh_jid=7770430003 | "13d" (speedy age) | Silent, mid-large — verify | "Associate" rung quant at a fintech bank (non-trading-floor); Fort Lee NJ; gap: title spans up to AVP (seniority range) | speedy |
| Corgi Insurance | Insurtech startup; early/seed | Quantitative Associate | https://jobs.ashbyhq.com/corgi/2eace392-9380-4a81-837a-3e4e8e3d1f69 | "19d" (speedy age) | Silent, small startup — likely OK | Entry quant at an insurtech startup (low visa risk); Chicago; gap: small co, role scope unclear | speedy |
| RA Capital | Life-sciences investment firm; mid-size | Quantitative Research & Strategy – Healthcare AI Associate | https://job-boards.greenhouse.io/racapitalmanagementllc/jobs/5192268008 | "22d" (speedy age) | Silent, mid-size — verify | "Associate" quant/AI (non-trading-floor research); Boston; gap: heavy bio/healthcare-domain bar | speedy |
| DebtBook | Muni/government-finance fintech SaaS; growth-stage | Associate Quantitative Strategist | https://job-boards.greenhouse.io/debtbook/jobs/4698960005 | "29d" (speedy age) | Silent, growth-stage — likely OK | Entry "Associate" quant at a fintech (non-trading-floor); Charlotte; window edge | speedy |
| MiTek | Building-products / construction-tech; large private | Supply Chain Data Analyst I | https://mii.wd5.myworkdayjobs.com/en-US/mitek/job/StCharles-MO-USA/Supply-Chain-Data-Analyst-I_R06378 | "14d" (speedy age) | Silent, larger company — **verify** | Entry "Data Analyst I"; supply-chain analytics; St Charles MO; SQL/BI fit | speedy |
| Simple Technology Solutions | IT/cloud services; small-mid | AI & Data Engineering Apprentice | https://job-boards.greenhouse.io/simpletechnologysolutions/jobs/6099047004 | "2d" first-seen | Unclear — **verify** | Entry "Apprentice" AI/Data Eng, **Remote**, BUT STS does federal/govt work → confirm this role is commercial, not clearance-gated | zapplyjobs |
| Texas Dept. of Transportation | State government | Data Analyst I, II, or III – TPP Division | https://jobright.ai/jobs/info/6a3ad99edd879c60912b0bec | Jun 23 (2d) | Unclear — **verify** | Entry "DA I", **Austin TX (≈local)**, BUT public-sector roles often need state residency / specific work-auth | jobright DA |
| Yale University | Private university; large | Data Scientist – New Grad Leadership Program | https://jobright.ai/jobs/info/69fd082a5cff890b03f35650 | Jun 19 (6d) | Silent, university — likely OK | New-grad DS program (universities often OPT-friendly), BUT jobright location field shows "Cranberry Township" (Westinghouse's HQ) → **possible data error / mislisted employer**; verify it's actually Yale | jobright DA |

### Recency-unverified (in-window per tracker but no direct ATS link captured)
_Simplify DS/AI/ML section: these 3 are the only net-new in-window rows; Simplify
only exposed a `simplify.jobs/c/<company>` redirect (no direct ATS URL parsed)._
| Company | Role | Best-available link | Note |
|---|---|---|---|
| BlueCross BlueShield of TN (BCBST) | Associate Data Engineer 1 | https://simplify.jobs/c/6624eec0-5300-4435-a8f4-e88cda773305 (Simplify redirect) | Chattanooga TN; "22d" Simplify age; entry DE fit; **no direct ATS link captured — find before applying** |
| blend360 | Junior Data Scientist | https://simplify.jobs/c/ca86fdf5-6866-42d6-ab98-efbef6cf7861 (Simplify redirect) | Atlanta GA; "22d"; data/AI consultancy; **no direct ATS link captured** |
| Murj | Data Analyst (Entry Level) | https://simplify.jobs/c/Murj (Simplify redirect) | Remote USA; "29d" (window edge); cardiac-device health-tech; **no direct ATS link captured** |

### Community / informal leads (HN "Who is hiring? (June 2026)", thread id 48357725)
_Direct fetch still 403/000 on all paths (Algolia API, hnhiring, nchelluri mirror) —
SAME blocker as every prior run. Surfaced only via `WebSearch` over HN/hnhiring;
**no per-post direct links obtainable**, so logged honestly as unlinked/unverified —
do NOT treat as confirmed without finding the original comment._
- **Riot IQ** — hiring "**AI-native fresh grads**" (software / full-stack / AI roles),
  **US-based remote**, online IQ-testing platform startup. **Strong fresh-grad + AI +
  US-remote fit on paper.** No direct link captured (web search collided with "Riot
  Games" — could not isolate Riot IQ's own posting). Informal/unverified.
- **Runway** — Engineering & Research roles, **remote (global)**; generative-video AI
  company (non-FAANG, in scope). Seniority unclear (likely competitive). No per-post link.
- **EXCLUDED:** EggAI (remote EU/Switzerland/Norway), Memora (founding eng, remote EU) —
  geography/seniority. Riot Games intern roles (interns, not FTE).

### Bonus — adjacent titles worth adding to the search vocabulary
- **"Physical AI Engineer" (TD Synnex)** — sim/synthetic-data AI; new high-signal title.
- **"Applied AI Associate" / "Generative AI Associate" (Innodata)** — entry applied/gen-AI
  rungs at a data-for-LLM company; "Associate" hides the AI work behind an analyst-style label.
- **"AI Data Analyst" (RELX)** — analyst title with explicit AI scope.
- **"Early Career Software Engineer – Applied AI" (Wonderschool)** — "Early Career"+"Applied AI"
  combo catches entry applied-AI roles that omit "new grad".
- **"AI Solutions Associate" (Digital United) / "Associate AI/ML Developer" (iSoftStone)** —
  Forward-Deployed/AI-Solutions-adjacent entry titles (screen for staffing/bench).
- **"Analytics Engineer I" (Oscar Health)** — explicit entry rung of the exact target title.
- Confirmed the **"Associate / Early Career Talent" Data Engineer** pattern at UST-family cos
  (UST HealthProof, CyberProof) — good keyword for entry DE.

### TODO for next (daily) run
- **USE curl + local parse, NOT WebFetch, for the GitHub trackers** — this run read every
  tracker (incl. the long Simplify DS/AI/ML table) in full for the first time by curling
  the raw markdown and parsing with Python. WebFetch's small-model truncation (the
  recurring "~60 rows" problem) is avoided entirely this way.
- **jobright AI/ML repo:** there is NO `2026-AI-Machine-Learning-New-Grad` repo (the 404
  last run was real — it doesn't exist). AI/ML-Engineer new-grad rows live in
  `jobright-ai/2026-Engineering-New-Grad` (6,100+ rows) — use that going forward.
- **jobright Data-Analysis** still caps at "last 7 days" — fine for a daily run, but for
  30-day depth find its Airtable/full export.
- **JD/visa verification** unchanged #1 blocker: greenhouse/jobright/workday/ashby all
  403 (WebFetch) or 000 (curl CONNECT denied by egress policy). All visa buckets inferred.
- **Community:** HN thread `48357725` (still June) + Algolia + hnhiring + nchelluri mirror
  all blocked to direct fetch; only WebSearch-over-HN returns text without per-post links.
  Watch for the **July 2026** "Who is hiring" thread (~Jul 1). Riot IQ + Runway are the two
  in-scope informal leads this run — try to recover Riot IQ's direct posting next run.

---

## Run: 2026-06-29 17:10 (DEEP BACKFILL — 30 day window)

**THIS IS A ONE-TIME DEEP BACKFILL, NOT A DAILY PASS.** Run 2026-06-29 with a
wider budget. Recency window = **last 30 days (~May 30 – Jun 29)** instead of the
normal 24h, to refresh the baseline. Future daily runs should keep using 24h and
treat everything below as already-seen. Read `leads_log.md` in full first and
de-duped against ALL six prior runs (06-20 12:00, 06-20 05:21 backfill,
06-20 18:30, 06-20 18:48 backfill, 06-24 17:09 backfill, 06-25 17:30 backfill).

**Coverage & honesty notes (read before trusting anything below):**
- **Method (unchanged, works):** `curl`-ed the raw markdown trackers from
  `raw.githubusercontent.com` (NOT blocked) and parsed locally with Python — avoids
  the WebFetch small-model truncation. All four trackers read **in full** this run.
- **Fully covered (curl'd raw + parsed locally):**
  - `speedyapply/2026-AI-College-Jobs` → `NEW_GRAD_USA.md` — 244 rows parsed
    (FAANG+/Quant/Other all read); ~95 rows ≤30d after filtering.
  - `zapplyjobs/New-Grad-Data-Science-Positions` → `README.md` — 324 apply-rows
    parsed across DS/AI-Eng/ML-Eng/Data-Eng/Data-Analyst/FDE (954 listings claimed).
  - `jobright-ai/2026-Engineering-New-Grad` → `README.md` — read in full (6,432
    data rows; AI/ML-Engineer new-grad rows live here). Calendar-dated **Jun 22–29**.
  - `jobright-ai/2026-Data-Analysis-New-Grad` → `README.md` — read in full, BUT the
    tracker still **caps visible rows at "last 7 days" (Jun 22–29 only)** per its
    capacity constraint, so 30-day depth unavailable (same cap as 06-24 / 06-25).
- **NEW community source this run — partial win:** a `WebSearch` over Y Combinator's
  Work-at-a-Startup board surfaced **real direct `ycombinator.com/companies/.../jobs/`
  URLs** for FDE / Applied-AI roles (logged in the Community section). The **JD bodies
  403** (could not read seniority/visa/post-date), so they're logged as informal/
  unverified — but the links are real, unlike the HN leads of prior runs. Worth mining
  YC WaaS via WebSearch every run.
- **NOT covered / blocked this run (be explicit) — UNCHANGED structural blockers:**
  - **Individual JD verification — ALL still blocked.** Tested this run: `curl` to
    greenhouse + jobright.ai + workday all returned **403 (CONNECT tunnel failed,
    egress policy)**; **WebFetch** to greenhouse + welbehealth + two YC pages also
    **403**. So I **could not read a single JD body** — EVERY visa bucket below is
    inferred from company type + role, NOT JD text. Every "verify" must be opened
    manually. Seniority for any role NOT explicitly labeled
    new-grad/junior/associate/"I"/entry/NCG is **unverified** and flagged inline.
  - **Community boards — HN still unreadable, and the July thread isn't up yet.**
    Today is Jun 29; the **July 2026 "Who is hiring"** thread opens ~Jul 1 (watch for
    it — daily runs should grab it). The **June** thread is still the same id
    **`48357725`**; `curl` to `hn.algolia.com/api/v1/search` = **403/000**, and the
    `nchelluri.github.io/hnjobs/` mirror **403'd via WebFetch**. No per-post HN links
    obtainable → no HN leads logged this run.
  - **SimplifyJobs** — NOT re-pulled this run (budget; prior 06-25 run read its full
    DS/AI/ML section and found it almost entirely stale — only 3 in-window rows for a
    30-day window, all already logged). Skipped knowingly, not silently.
  - Reddit / Discord / Slack — not machine-readable (hard-blocked every prior run).
  - LinkedIn / Indeed / Glassdoor / Wellfound — only aggregator landing pages, no
    per-posting dates or stable direct links — nothing logged. No founder/recruiter
    LinkedIn post with a stable direct link surfaced this run.
- **Recency basis:** jobright rows carry calendar dates (Jun 22–29 used directly).
  speedyapply rows carry an "age" field ("4d".."20d") read against the Jun 29 refresh
  — reliable to the day. zapplyjobs ages in minutes/hours ("17h","28m","14m") are
  scraper **first-seen** stamps, NOT post dates → flagged **recency-unverified** inline.
- **De-duped out as already logged** (appear again in trackers, NOT repeated below):
  Excellus BCBS AI Engineer I/II (JR103556-2), Texas DOT Data Analyst I (06-25 Tier 3),
  General Atomics DS I, GDIT DS-Junior, Jerry / Snowflake FDE / Ramp / GlobalFoundries /
  Brellium / Oscar / WelbeHealth / SentiLink and the rest of the 06-24 & 06-25 tiers.

### Tier 1 — Hot & strong fit
_Entry-labeled or exact-target-title, recent, US-based, non-defense, non-FAANG.
Visa buckets inferred (JDs all 403); seniority noted where unverified._

| Company | What they do / size | Role | Direct link | Posted (basis) | Visa posture | Fit note | Source |
|---|---|---|---|---|---|---|---|
| AI Fund | Andrew Ng's AI venture studio (builds + staffs AI startups); growth-stage | Applied AI Engineer · AI Engineer | https://jobs.lever.co/AIFund/01654e18-7b7f-4f0d-84b4-9e090fbc73be/apply (Applied AI) · https://jobs.lever.co/AIFund/33bd1d6c-5091-42f8-99c0-6e97292782be/apply (AI Eng) | 2–3d (≈Jun 26–27; zapply first-seen, ≈in-window) | Silent, growth startup — likely OK | **Exact target title "Applied AI Engineer"** at an AI-builder studio; Mountain View; ship-end-to-end profile match; gap: seniority unverified (JD 403) | zapplyjobs |
| Monte Carlo | Data-observability / data-reliability SaaS; growth-stage unicorn | Applied Forward Deployed Engineer (FDE) | https://jobright.ai/jobs/info/6a0b59364d9320363687003c | Jun 24 (5d) | Silent, growth startup — likely OK | **FDE = bullseye target title, COMMERCIAL + Remote-US**; data-platform domain fits the dbt/Airflow/pipeline side; gap: FDE usually wants some customer-facing exp + seniority unverified | jobright ENG |
| Frontier Medicines | Precision-medicine biotech (covalent drug discovery + ML); growth-stage | AI Engineer I | https://apply.workable.com/frontier-medicines/j/5E53E8D60C/ | 5d (≈Jun 24) | Silent, growth-stage — likely OK | **Explicit "AI Engineer I" entry rung** — exact target title at the lowest level; South SF; gap: drug-discovery domain | speedyapply |
| The Hanover Insurance Group | P&C insurance carrier; large public | Associate Data Engineer (REMOTE) | https://jobright.ai/jobs/info/6a3d74d5122f340d29cf0a72 | Jun 25 (4d) | Silent, larger company — **verify** | **Explicit "Associate" + REMOTE** Data Engineer = clean dbt/Airflow/SQL entry fit; gap: insurance domain, large-co policy | jobright ENG |
| SewerAI | Infrastructure-inspection AI (sewer/pipe CV + analytics); startup | Junior Analytics Engineer | https://jobright.ai/jobs/info/6a3f101f4d047136e0938af1 | Jun 26 (3d) | Silent, small startup — likely OK | **Explicit "Junior" + "Analytics Engineer" exact target title** at a startup (low visa risk); dbt/SQL fit; Walnut Creek CA | jobright ENG |
| Gen Digital | Consumer cyber-safety (Norton, Avast, LifeLock); large public | Machine Learning Engineer I | https://jobs.ashbyhq.com/gen-digital/04d8f8b7-135c-4b93-8dbb-f47b9ddb51ea/application | 3d (≈Jun 26; zapply first-seen) | Silent, larger company — **verify** | **Explicit "MLE I" entry rung**; Mountain View; applied-ML fit; gap: large-co policy, recency is a first-seen stamp | zapplyjobs |

### Tier 2 — Worth a look (good fit; caveat = seniority and/or visa unverified, JD 403)

| Company | What they do / size | Role | Direct link | Posted (basis) | Visa posture | Fit note | Source |
|---|---|---|---|---|---|---|---|
| Baseten | ML model-deployment / inference infra; growth-stage startup | Applied AI Inference Engineer | https://jobright.ai/jobs/info/69e7db2658811370cb11ec8f | Jun 23 (6d) | Silent, growth startup — likely OK | **"Applied AI" + inference-infra** at a hot ML-infra startup; strong stack-culture fit; gap: inference-infra heavier than RAG/product, seniority unverified | jobright ENG |
| Royal Bank of Canada (RBC) | Global bank — **US/NYC office**; large public | AI Engineer I | https://rbc.wd3.myworkdayjobs.com/en-US/rbcglobal1/job/New-York-New-York-United-States-of-America/AI-Engineer-I_R-0000178591-1 | 4d (≈Jun 25) | Silent, larger company — **verify** | **Role is New York, NY (US-based) + explicit "AI Engineer I"** entry; gap: large-bank immigration policy | speedyapply |
| Ironclad | AI contract-lifecycle / legal-tech SaaS; growth-stage unicorn | Finance Systems & AI Engineer | https://jobs.ashbyhq.com/ironcladhq/29f8753e-5ff4-4bfd-9e83-b6ee6c2e8293/application | 3d (≈Jun 26; first-seen) | Silent, growth startup — likely OK | AI-Engineer title at a strong AI-native startup; SF; gap: finance-systems niche, **seniority unverified** (no entry marker), recency stamp | zapplyjobs |
| ServiceNow | Enterprise workflow/automation SaaS; large public | Machine Learning Engineer, Agentic Apps | https://jobs.smartrecruiters.com/ServiceNow/744000134357159 | 3d (≈Jun 26; first-seen) | Silent, larger company — **verify** | **"Agentic"** = direct match to the LangGraph/agent flagship; Mountain View; gap: seniority unverified, large-co policy | zapplyjobs |
| JPMorgan Chase | Global bank; large public (non-FAANG, referral-adjacent) | AI/ML Engineering Analyst | https://jpmc.fa.oraclecloud.com/hcmUI/CandidateExperience/en/sites/CX_1/job/210745706 | 4d (≈Jun 25) | Silent, larger company — **verify** | **"Analyst" = entry rung** at a big bank; Jersey City; applied-ML fit; gap: large-bank policy. (NOTE: their "AI Engineer – Software Engineer III" req is **III/senior** — excluded) | zapplyjobs |
| DreamWorks Animation | Film/animation studio (NBCU/Universal); large | Analytics Engineer | https://jobright.ai/jobs/info/6a4289c26c326942b4e83369 | Jun 29 (0d) | Silent, larger company — **verify** | **"Analytics Engineer" exact target title**; NYC; dbt/SQL fit; gap: seniority unverified, media domain | jobright ENG |
| NBCUniversal | Media/streaming conglomerate; large public (non-FAANG) | Analytics Engineer | https://jobright.ai/jobs/info/6a4284f46c326942b4e8323e | Jun 29 (0d) | Silent, larger company — **verify** | Exact target title; NYC; SQL/dbt fit; gap: seniority unverified, large-co policy | jobright ENG |
| Xcel Energy | Electric & gas utility; large public | Associate Data Scientist – Distribution | https://jobright.ai/jobs/info/6a3f0dbe78237a036d5e6679 | Jun 26 (3d) | Silent, larger company — **verify** | **Explicit "Associate" DS**; grid/asset analytics = good applied-analytics/anomaly fit; Twin Cities; gap: utility domain | jobright DA |
| Reynolds Consumer Products | CPG (Reynolds Wrap, Hefty); large public | AI Solutions Analyst | https://jobright.ai/jobs/info/6a085024403fc339507ecdda | Jun 29 (0d) | Silent, larger company — **verify** | **"AI Solutions" (FDE/Solutions-adjacent)** entry-ish title; Lake Forest IL; applied-AI fit; gap: "Analyst" framing, seniority unverified | jobright ENG |
| Motorola Solutions | Public-safety comms / enterprise security; large public | AI Solutions Developer · Machine Learning Engineer | https://jobright.ai/jobs/info/6a3d59e14d047136e09331bb (AI Solutions Dev) · https://motorolasolutions.wd5.myworkdayjobs.com/Careers/job/Los-Angeles-CA/Machine-Learning-Engineer_R64440 (MLE) | Jun 24 (5d) / 4d | Silent, larger company — **verify** (some public-safety/gov-adjacent work — confirm role is commercial) | AI-Solutions / ML titles fit; gap: seniority unverified + Motorola does law-enforcement work (screen for clearance/US-person on specific teams) | jobright ENG + zapply |
| Texas Tech University | Public university; large | Business Intelligence Developer | https://jobright.ai/jobs/info/6a3fe35b3bfa967791ebf957 | Jun 27 (2d) | Silent, university — likely OK (universities often OPT-friendly) | **"BI Developer" exact target title + Texas (≈in-state)**; SQL/BI fit; gap: academic-IT BI vs product analytics | jobright DA |
| Safety National | Workers'-comp / specialty reinsurance; mid-large | BI Data Analyst | https://jobright.ai/jobs/info/69cad8baaa3c2c1995e30b15 | Jun 25 (4d) | Silent, mid-large — verify | BI/Data-Analyst target title; St Louis; SQL/BI fit; gap: insurance domain, seniority unverified | jobright DA |
| Clear Investment Group | Real-estate investment / multifamily; mid-size | AI Associate | https://jobright.ai/jobs/info/6a41f0929dd7f954cafe9790 | Jun 28 (1d) | Silent, mid-size — verify | Entry "AI Associate" (applied-AI/ops); Chicago; broad-ownership fit; gap: small AI footprint, role scope unclear | jobright ENG |
| AIG | Insurance (P&C / life); large public | Business Data Analyst | https://aig.wd1.myworkdayjobs.com/AIG/job/NJ-Jersey-City/Business-Data-Analyst_JR2601725 | 4d (≈Jun 25) | Silent, larger company — **verify** | Business/Data-Analyst target title; Jersey City; SQL/BI fit; gap: seniority unverified, insurance domain | zapplyjobs |
| bet365 | Online sports-betting / iGaming — **US (Denver) office**; large private | Junior Data Scientist | https://jobright.ai/jobs/info/6a4257bf557b3862f15e0dac | Jun 29 (0d) | Silent, larger company — **verify**; regulated-gaming **state license** step possible | **Explicit "Junior" DS**, Denver CO (US); analytics/ML fit; gap: iGaming domain + gaming-license background step (licensure, not citizenship) | jobright DA |
| Solace | Healthcare patient-advocacy marketplace; growth-stage startup | People Operations & AI Associate | https://jobs.ashbyhq.com/solace/10e59c85-4919-46b7-85bc-cb7c59657584 | 17d (≈Jun 12) | Silent, growth startup — likely OK | **Maps to the People Analytics / HR Data target** + AI scope; remote-US; gap: HR-ops-leaning vs pure data-eng | speedyapply |
| The Nature Conservancy | Environmental nonprofit; large | Junior Data Analyst / Developer | https://nature.wd108.myworkdayjobs.com/en-US/externalcareers/job/Arlington-Virginia/Junior-Data-Analyst-Developer_JR103288 | 5d (≈Jun 24) | Silent, nonprofit — likely OK | **Explicit "Junior"** DA/dev; Arlington VA; SQL/BI + light-dev fit; gap: nonprofit-IT domain | speedyapply |
| WebFX | Digital-marketing agency / martech; mid-size | Jr. Business Data Analyst | https://jobright.ai/jobs/info/68974d2373b3a600fe8967eb | Jun 28 (1d) | Silent, mid-size — likely OK | Explicit "Jr." Business Data Analyst; Harrisburg PA; SQL/BI fit; gap: marketing-analytics vs AI-eng | jobright DA |
| Illumina | Genomics sequencing hardware/software; large public | AI Engineer | https://jobright.ai/jobs/info/6a3ee7d5122f340d29cf5271 | Jun 26 (3d) | Silent, larger company — **verify** | AI-Engineer target title; San Diego; applied-AI fit; gap: **seniority unverified** (no entry marker), genomics domain | jobright ENG |

### Tier 3 — Long shots / needs verification / seniority or domain risk

| Company | What they do | Role | Direct link | Posted | Visa posture | Why Tier 3 | Source |
|---|---|---|---|---|---|---|---|
| xAI | Frontier-LLM lab (Grok); large private (non-FAANG, in scope) | Data Engineer | https://jobright.ai/jobs/info/6a40ff5a16b1493953283c9f | Jun 28 (1d) | Silent, larger company — **verify** | In-scope Data-Eng at a frontier lab, but **very competitive + seniority unverified**; Palo Alto | jobright ENG |
| Scale AI | Data-labeling / AI-data platform; large private | Machine Learning Research Engineer, Agents – Enterprise | https://jobright.ai/jobs/info/69054219122e8474c78d7e70 | Jun 28 (1d) | Silent, larger company — **verify** | "Agents" = on-profile, but **research-eng + high bar + seniority unverified**; SF Bay | jobright ENG |
| Etsy | E-commerce marketplace; large public (non-FAANG) | Data Scientist, Product Analytics | https://etsy.wd5.myworkdayjobs.com/Etsy_Careers/job/Brooklyn-New-York/Data-Scientist--Product-Analytics_JR5568-1 | 4d (≈Jun 25) | Silent, larger company — **verify** | Product-analytics DS fit, but **seniority unverified** (likely mid); Brooklyn | zapplyjobs |
| Centific | AI-data / digital-transformation services; mid-large | Data Scientist | https://centific.wd1.myworkdayjobs.com/Centific_Global/job/Redmond-Washington/Data-Scientist_JR107660-1 | 2d (≈Jun 27; first-seen) | Silent, mid-large — verify | DS fit, but services/staffing-flavored + **seniority unverified**; Redmond WA | zapplyjobs |
| General Motors | Auto OEM; large public | Data Engineer | https://generalmotors.wd5.myworkdayjobs.com/Careers_GM/job/Warren-Michigan-United-States-of-America/Data-Engineer_JR-202612597 | 6d (≈Jun 23) | Silent, larger company — **verify** | Data-Eng fit, but **seniority unverified** + large-co policy; Warren MI | zapplyjobs |
| Johnson & Johnson | Healthcare/pharma/medtech; large public | Digital Engineering Data & AI Engineer | https://jj.wd5.myworkdayjobs.com/jj/job/New-Brunswick-New-Jersey-United-States-of-America/Digital-Engineering-Data---AI-Engineer_R-084235-1 | 3d (≈Jun 26; first-seen) | Silent, larger company — **verify** | Data+AI Eng fit, but **seniority unverified**; New Brunswick NJ | zapplyjobs |
| Quantcast | Ad-tech / audience AI; mid-large | Machine Learning Engineer | https://jobright.ai/jobs/info/6a39b13d6484fb75f2b33376 | Jun 26 (3d) | Silent, larger company — **verify** | ML-Eng fit, but **seniority unverified**; ad-tech domain; SF | jobright ENG |
| Applied Materials | Semiconductor equipment; large public | Machine Learning Engineer (Generative AI) | https://jobright.ai/jobs/info/6a3ab822797099171917b43a | Jun 23 (6d) | Silent, larger company — **verify** | **GenAI** title (appealing), but semis domain + **seniority unverified**; Santa Clara | jobright ENG |
| CoreWeave | GPU/AI cloud provider; large public | Software Engineer, Inference AI/ML | https://jobright.ai/jobs/info/692111b100c9ee50eaecb67c | Jun 25 (4d) | Silent, larger company — **verify** | Inference AI/ML fit, but infra-heavy + **seniority unverified**; Sunnyvale | jobright ENG |
| MeritFirst | AI startup (small); early | AI Engineer | https://jobright.ai/jobs/info/6a38b41a29c90c607e4e7ed7 | Jun 27 (2d) | Silent, small startup — likely OK | AI-Engineer at a small startup (low visa risk), but company opacity + **seniority/scope unclear**; SF | jobright ENG |
| Locus Robotics | Warehouse-fulfillment robotics; growth-stage | Deployment Engineer, North America | https://jobright.ai/jobs/info/6a3d89da8bfad862bc99d963 | Jun 25 (4d) | Silent, growth-stage — likely OK | **Deployment Engineer (FDE-adjacent)** target; US; gap: ops/field-deploy vs build, **seniority unverified** | jobright ENG |
| Tyler Technologies | Public-sector software (govtech) for state/local; large public | Deployment Engineer – ERP | https://jobright.ai/jobs/info/6a31cc82c477a5075f48f543 | Jun 23 (6d) | Unclear — **verify** | Deployment-Engineer (FDE-adjacent) title, but **govtech** customer base → confirm no public-sector background/clearance step; Yarmouth ME | jobright ENG |
| The Talent Co-op | Talent-network / staffing for AI roles | AI Engineering Roles — Backend / Full-Stack / ML / Applied | https://jobright.ai/jobs/info/6a4236ac1afc66714d3cc16d | Jun 29 (0d) | Unclear — **verify** | Umbrella "AI engineering roles" posting via a **talent network** (not a direct employer) → confirm it routes to a real FTE, not a bench/pipeline; SF Bay | jobright ENG |
| Point72 | Multi-strat hedge fund; large | Data Scientist, Proprietary Research | https://jobright.ai/jobs/info/67842232892d69f5bd6249b9 | Jun 25 (4d) | Silent, larger company — **verify** | DS title, but **proprietary-research = trading-floor-adjacent** + very high bar; profile wants non-trading-floor; NYC | jobright DA |
| The Voleon Group | Systematic / ML quant hedge fund; large | Data Scientist | https://jobright.ai/jobs/info/6a2703fa7d827633afff8006 | Jun 29 (0d) | Silent, larger company — **verify** | ML-quant DS (appealing on paper), but **systematic-trading shop with a PhD-heavy bar**; Berkeley | jobright DA |
| Aquatic Capital Management | Quant trading / systematic asset mgmt; growth | Quantitative Researcher, Early Career | https://jobright.ai/jobs/info/69f397c858b23a2329da62ad | Jun 25 (4d) | Silent, larger company — **verify** | "Early Career" quant (appealing rung), but **trading-floor quant + high research bar**; profile prefers non-trading-floor; Chicago | jobright DA |
| Arrowhead Pharmaceuticals | RNAi drug-discovery biotech; large | Scientist, Computational Chemist & MLOps Engineer | https://jobright.ai/jobs/info/6a3c1d54882f121f56a336c0 | Jun 24 (5d) | Silent, larger company — **verify** | **MLOps is a target title**, but bundled with computational-chemistry / wet-lab-adjacent domain bar; Madison WI | jobright ENG |

### Community / informal leads (Y Combinator Work-at-a-Startup — surfaced via WebSearch)
_NEW source this run. These are **real direct YC job-board URLs**, but the **JD bodies
403'd** (could not read seniority, exact post date, or visa language). Logged honestly
as informal/unverified — open each to confirm it's entry-level and US-eligible before
applying. All are seed/early YC startups (visa: silent, small startup → OPT needs no
sponsorship, generally OK; but tiny startups sometimes can't accommodate — verify)._
- **FurtherAI** — Forward Deployed Engineer (AI agents for insurance workflows); search snippet says **open to recent CS grads** — strong FDE fit. https://www.ycombinator.com/companies/furtherai/jobs/2uFhWmi-forward-deployed-engineer
- **Maywood** — Applied AI Engineer (LLMs, code-gen, agents embedded in CI/CD & dev tooling) — near-exact applied-AI match. https://www.ycombinator.com/companies/maywood/jobs/DV7GBKh-applied-ai-engineer
- **Contrario** — Applied AI Engineer (AI-native recruiting marketplace; ML matching/search) — applied-AI fit. https://www.ycombinator.com/companies/contrario/jobs/UXt8I3L-applied-ai-engineer
- **Soff** — AI-Native Forward Deployed Engineer (AI-agent workforce for industrial execution) — FDE fit. https://www.ycombinator.com/companies/soff/jobs/OTA9QxR-ai-native-forward-deployed-engineer
- **Clarion** — Forward Deployed Engineer. https://www.ycombinator.com/companies/clarion/jobs/mVHG3z1-forward-deployed-engineer
- **CollectWise** — Forward Deployed Engineer. https://www.ycombinator.com/companies/collectwise/jobs/tv3ufcc-forward-deployed-engineer
- **Synthio Labs** — Forward Deployed Engineer – Tech. https://www.ycombinator.com/companies/synthio-labs/jobs/L76r1Yr-forward-deployed-engineer-tech
- **EXCLUDED:** Arist & Avallon AI ("**Founding** Forward Deployed Engineer" — founding/senior); **telli** ("Forward Deployed Engineer (AI)" — company is Berlin/Germany-based per "Cherry" pre-seed → F-1 OPT is US-only, geography risk; verify US-eligibility before applying).

### Excluded (logged so future runs don't re-surface)
- **FAANG-tier / FAANG-owned (referral track):** Amazon/AWS, Microsoft, Google, Meta, Apple, **NVIDIA** (LLM Training NCG, Research Scientist Efficient-DL/Physical-AI, AI Chip Design — all NCG but FAANG+), **TikTok/ByteDance** (many ML/Applied-Scientist PhD rows), **PayPal** (MLE Austin), **Roblox** (SWE Data Eng), **Zoox** (MLE Simulation — Amazon-owned).
- **Defense / federal / clearance (US-person near-certain):** Accenture Federal Services (Jr Data Engineer Chantilly; Forward Deployed Data Engineer DC), Lockheed Martin (Systems/Data Engineer Sunnyvale; A/AI ML Engineer Early-Career), General Atomics Aeronautical (Data Scientist I Charlottesville), GDIT (Data Scientist-Junior Jacksonville NC), MANTECH (Agentic AI Developer Remote), Noblis (Data Analyst – Network Security, Atlantic City), SpaceX (Forward Deployed Engineer, Mission Systems – **Starshield** = defense/ITAR), RTX (Agentic AI Engineer Arlington), Aspire Defence (Apprentice DA — UK defense).
- **Non-US geography (F-1 OPT is US-only):** CIBC (Montreal), Connor Clark & Lunn (DS + Quantitative Data Analyst, Vancouver), Lyft (DA Toronto), mthree (Jr DS Canada), Publicis Canada / ANZ / Toronto (DA ×several), ICBC (DE North Vancouver), Zurich Canada (DE Toronto), RTX (DS/ML Researcher Manchester UK), INRIX (Data Solutions Eng, Birmingham UK), Thomson Reuters (Applied Scientist Toronto), Amphenol (Co-Op Markham ON), FluidAI Medical (Co-op Kitchener ON), SIA Innovations (Agentic AI Eng Montréal), University of Toronto (Sessional Lecturer), Dialpad (Analytics Eng Vancouver).
- **Intern / co-op for currently-enrolled students (candidate grads May 2026 — weak timing fit):** SharkNinja (SharkByte Applied AI & Analytics Co-op, Fall 2026), Hill's Pet Nutrition (CS&L DA Co-Op Aug 2026–May 2027), Volvo Group (BI Co-Op Fall 2026), Marmon Holdings (DE Intern/Co-Op), Great Question / Workato / Human Computer Lab / Integra FEC / Trane / W.R. Berkley / Schweitzer Engineering / Stevens Capital (AI/Data/Quant interns).
- **Senior / II+ / manager (seniority excludes):** Realtor.com (Mgr, Data Engineering), Becton Dickinson (Product Data Analyst III), Thermo Fisher (Data Analyst III), Applied Materials (M4 Manager IV, BI Analyst), JPMorgan (AI Engineer – Software Engineer III).
- **Wet-lab / clinical / lab-bench (not applied-AI/data-eng):** Joslin Diabetes Center (DA I – Vascular Cell Biology), Pace Analytical (Chromatography Data Analyst), Oregon Health Authority (Health Cost DA – RA3), NYC DOHMH (Chronic Disease DA), NewYork-Presbyterian (Population Health DA; BI – Epic EHR — clinical-ops, low fit). Veolia (Meter Data Analyst, Hackensack NJ — utility-meter ops, low fit) noted/skipped.
- **Already logged in prior runs** (appear again; not repeated): Excellus BCBS AI Engineer I/II, Texas DOT Data Analyst I, plus the full 06-24 & 06-25 tier rows (Jerry, Snowflake FDE, Ramp, GlobalFoundries, Brellium, Oscar, WelbeHealth, SentiLink, etc.).

### Bonus — adjacent titles worth adding to the search vocabulary
- **"Applied Forward Deployed Engineer (FDE)" (Monte Carlo)** + the **YC FDE cluster** (FurtherAI, Soff, Clarion, CollectWise, Synthio) — confirms a **wave of COMMERCIAL FDE roles at seed/early startups**, several recent-grad-friendly. Mine YC Work-at-a-Startup via WebSearch for "Forward Deployed Engineer" / "Applied AI Engineer" every run.
- **"AI Solutions Analyst / AI Solutions Developer / AI Associate" (Reynolds, Motorola, Clear Investment)** — entry applied-AI/FDE-adjacent titles that hide the AI work behind an "Analyst/Associate/Developer" label.
- **"People Operations & AI Associate" (Solace)** — a real hit on the **People Analytics / HR Data Analyst** target (rare for this profile); add "People Operations AI" / "People Analytics" as explicit terms.
- **"AI Engineer I" / "MLE I" / "Associate Data Engineer" / "Junior Analytics Engineer"** (Frontier Medicines, RBC, Gen Digital, Hanover, SewerAI) — explicit entry rungs of the exact target titles; keep prioritizing the "I" / "Junior" / "Associate" suffix.
- **"Analytics Engineer" at big media (DreamWorks, NBCUniversal)** — the exact target title is now appearing at large media employers, not just data-startups.

### TODO for next (daily) run
- **Watch for the JULY 2026 HN "Who is hiring" thread (~Jul 1)** — June thread `48357725`
  + Algolia API + nchelluri mirror still all 403/000. The July thread is the single
  biggest community-board opportunity and should be grabbed the day it opens.
- **NEW working community path: WebSearch over Y Combinator Work-at-a-Startup** returns
  real direct YC job URLs (the YC pages themselves 403, but the links are valid). Run a
  WebSearch for the target titles + "site:ycombinator.com" each pass.
- **JD/visa verification** unchanged #1 blocker: greenhouse/jobright/workday/ashby/oracle/
  smartrecruiters all 403 (WebFetch) or 403/000 (curl egress). All visa buckets inferred,
  all "seniority unverified" flags stand.
- **jobright Data-Analysis** still caps at "last 7 days"; **speedyapply + zapplyjobs +
  jobright-Engineering** remain the reliable curl+parse trio. SimplifyJobs is mostly stale
  for a 30-day window (skip unless a daily run wants the backstop).

---

## Run: 2026-07-03 17:15 (DEEP BACKFILL — 30 day window)

**THIS IS A ONE-TIME DEEP BACKFILL, NOT A DAILY PASS.** Run 2026-07-03 with a
wider budget. Recency window = **last 30 days (~Jun 3 – Jul 3)** instead of the
normal 24h, to refresh the baseline. Future daily runs should keep using 24h and
treat everything below as already-seen. Read `leads_log.md` in full first and
de-duped against ALL seven prior runs (06-20 12:00, 06-20 05:21 backfill,
06-20 18:30, 06-20 18:48 backfill, 06-24 17:09 backfill, 06-25 17:30 backfill,
06-29 17:10 backfill).

**Coverage & honesty notes (read before trusting anything below):**
- **Method (unchanged, works):** `curl`-ed the raw markdown trackers from
  `raw.githubusercontent.com` (NOT blocked) and parsed locally with Python —
  avoids the WebFetch small-model truncation. All four trackers read **in full**.
- **Fully covered (curl'd raw + parsed locally):**
  - `speedyapply/2026-AI-College-Jobs` → `NEW_GRAD_USA.md` — 247 rows parsed
    (FAANG+/Quant/**Other** all read; fixed a parser bug so the 5-column "Other"
    table now parses — this is the non-FAANG section with the best net-new rows).
    ~40 title-matching US rows ≤30d after filtering.
  - `zapplyjobs/New-Grad-Data-Science-Positions` → `README.md` — parsed in full
    (962 listings claimed / 197 cos across DS/AI-Eng/ML-Eng/Data-Eng/Data-Analyst/
    FDE). **Caveat:** the overwhelming majority of zapply rows this run carry
    minute/hour "first-seen" scraper stamps (12m–1h) that are NOT post dates → most
    are logged as **recency-unverified**, and a large share are interns/defense/
    FAANG/dupes filtered out.
  - `jobright-ai/2026-Engineering-New-Grad` → `README.md` — read in full (~6,400
    data rows; AI/ML-Engineer new-grad rows live here). Calendar-dated **Jun 26 – Jul 3**.
  - `jobright-ai/2026-Data-Analysis-New-Grad` → `README.md` — read in full, BUT the
    tracker still **caps visible rows at "last 7 days" (Jun 26 – Jul 3 only)** per its
    capacity constraint, so 30-day depth unavailable (same cap as 06-24/06-25/06-29).
- **NEW this run — the JULY 2026 HN thread is LIVE but still unreadable:**
  - "Ask HN: Who is hiring? (**July 2026**)" = thread id **`48747976`** (posted
    ~Jul 2, ~13h before this run). Companion "Who wants to be hired?" = `48747975`.
  - **Every read path 403'd again**, exactly as every prior run: `curl` to
    `hn.algolia.com/api/v1/search` = **000 (CONNECT tunnel failed, egress policy)**;
    `hnrss.org` = **000**; **WebFetch** to `hnhiring.com/july-2026`,
    `hnjobs.emilburzo.com`, and `nchelluri.github.io/hnjobs/` all = **403**. Only a
    `WebSearch` *over* those mirrors returned partial snippets with **no per-post
    direct links** → the only July-thread items surfaced were EU/senior (EggAI —
    remote EU; Ojin — CET±2h; plus several "5+ years" roles), so **nothing US-based
    and entry-level from HN could be logged with a link this run.** The July thread
    remains the single biggest un-mined community opportunity; a readable path is
    still unsolved.
- **YC Work-at-a-Startup (via WebSearch) — WORKS, real direct links (JD bodies 403):**
  same partial-win as 06-29 — `WebSearch` returns real `ycombinator.com/companies/
  .../jobs/` URLs even though the pages themselves 403. Fresh FDE/Applied-AI cluster
  logged in the Community section (open each to confirm entry-level + US-eligible).
- **NOT covered / blocked (unchanged structural blockers):**
  - **Individual JD verification — ALL still blocked** (greenhouse/jobright/workday/
    ashby/oracle/smartrecruiters → 403 WebFetch or 000 curl-egress). **No JD body
    read** → EVERY visa bucket below is inferred from company type + role, NOT JD
    text; every "verify" must be opened manually. Seniority for any role NOT
    explicitly labeled new-grad/junior/associate/"I"/entry/NCG/"program" is
    **unverified** and flagged inline.
  - Reddit / Discord / Slack — not machine-readable (hard-blocked every prior run).
  - LinkedIn / Indeed / Glassdoor / Wellfound — only aggregator landing pages, no
    per-posting dates or stable direct links — nothing logged. No founder/recruiter
    LinkedIn post with a stable direct link surfaced.
  - **SimplifyJobs** — not re-pulled (06-25 read its full DS/AI/ML section and found
    it almost entirely stale for a 30-day window; skipped knowingly, not silently).
- **Recency basis:** jobright rows carry calendar dates (Jun 26 – Jul 3 used
  directly). speedyapply rows carry a reliable-to-the-day "age" ("1d".."30d").
  zapplyjobs minute/hour stamps are scraper first-seen, NOT post dates → those are
  parked in **Recency-unverified**. zapply Visa column (`🏛 H-1B Co.` / `✅ Sponsor`)
  is a *company-level* sponsorship signal (generally OPT-friendly), NOT a per-JD
  guarantee — still verify.
- **De-duped out as already logged** (appear again in trackers, NOT repeated below):
  UST HealthProof Assoc DE (Frisco), XiFin Assoc MLE, Reynolds AI Solutions Analyst,
  NBCUniversal + DreamWorks Analytics Eng, Innodata GenAI/Applied Associate, CBTS
  Jr/Data Engineer, Clear Investment AI Associate, Scale AI ML Research Eng (Agents),
  xAI DE, MeritFirst AI Eng, Motorola AI Solutions Dev, The Talent Co-op, iSoftStone
  Assoc AI Dev, Adobe Univ-Grad MLE, Qualcomm MLE College-Grad, Esri DS I, RBC AI
  Engineer I, Frontier Medicines AI Engineer I, GlobalFoundries NCG (Richardson),
  Brellium, Solace People-Ops & AI, MiTek DA I, Home Depot Assoc DS, Upgrade Jr B&D
  Analyst, PNC Assoc DS (C&IB), SBT Global Jr DA, Careerswift, Cushman & Wakefield Jr
  DS, DraftKings CX AI Associate, Truist DS I, Labcorp Assoc DS, Gen Digital MLE I,
  PTC Jr DA/Analytics Eng, AI Fund Applied AI Eng, YC: Maywood / FurtherAI / Soff /
  telli (already logged 06-29). SpaceX Starshield FDE, MANTECH, Lockheed, GDIT,
  Booz Allen, Noblis, CACI, KBR = defense/federal (excluded, see below).

### Tier 1 — Hot & strong fit
_Entry-labeled or exact-target-title, recent (≤~3d), US-based, non-defense,
non-FAANG. Visa buckets inferred (JDs all 403); seniority noted where unverified._

| Company | What they do / size | Role | Direct link | Posted (basis) | Visa posture | Fit note | Source |
|---|---|---|---|---|---|---|---|
| Northern Trust | Custody bank / wealth & asset servicing; large public | Associate AI Engineer | https://ntrs.wd1.myworkdayjobs.com/en-US/northerntrust/job/Chicago-IL/Associate-AI-Engineer_R156480 | 2d (≈Jul 1) | Silent, larger company — **verify** | **Explicit "Associate AI Engineer"** entry rung at a big bank; Chicago; applied-AI fit; gap: large-bank immigration policy | speedyapply Other |
| AssetMark | Wealth-management tech platform for advisors; large public | Associate Data Engineer | https://assetmark.wd5.myworkdayjobs.com/AssetMark_Careers/job/Charlotte-NC/Associate-Data-Engineer_Req-003889 | Jul 2 (1–2d; jobright cal + zapply 2h) | Silent, larger company — **verify** | **Explicit "Associate" Data Engineer** — clean dbt/Airflow/SQL entry fit; Charlotte NC; gap: fintech-platform policy | jobright ENG + zapply |
| FIS | FinTech / payments & banking software; large public (~55k) | Data Scientist I – FIS University Program | https://fis.wd5.myworkdayjobs.com/en-US/searchjobs/job/US-GA-ATL-201-STE-900/Data-Scientist-I--FIS-University-Program_JR0307349 | 3d (≈Jun 30) | Silent, larger company — **verify** | **"DS I" + explicit "University Program" (new-grad track)** = double entry signal; Atlanta; analytics/ML fit; gap: large-co policy | speedyapply Other |
| Together AI | Open-model AI cloud / inference & training infra; growth-stage unicorn | Analytics Engineer — Data Warehouse | https://jobright.ai/jobs/info/69d58593706f771673ba3d4c | Jul 3 (0d) | Silent, growth startup — likely OK | **"Analytics Engineer" exact target title** at a hot AI-infra startup; SF; dbt/SQL/warehouse fit; gap: **seniority unverified** (JD 403) | jobright ENG |
| Phenom | HR-tech / talent-experience AI platform; growth-stage (~1.5k) | Associate Data Engineer | https://jobright.ai/jobs/info/6a29abb2d3ec8317fe13fbdb | Jul 2 (1d) | Silent, larger company — **verify** | **Explicit "Associate" DE** at a people/talent-analytics platform (adjacent to the People-Analytics target); Ambler PA; dbt/SQL fit | jobright ENG |

### Tier 2 — Worth a look (good fit; caveat = seniority and/or visa unverified, JD 403)

| Company | What they do / size | Role | Direct link | Posted (basis) | Visa posture | Fit note | Source |
|---|---|---|---|---|---|---|---|
| Travelers | P&C insurance carrier; large public | Engineering Development Program (EDP) – Data Engineering | https://jobright.ai/jobs/info/6a4734fe0dd56c76cc2fc44b | Jul 2 (1d) | Silent, larger company — **verify** | **EDP = new-grad rotational program** + Data-Engineering track; Hartford CT; dbt/SQL fit; gap: insurance domain (NOTE: Travelers DE II was excluded prior as senior — this is the entry program) | jobright ENG |
| Travelers | P&C insurance carrier; large public | Data Science Leadership Development Program (DSLDP) – Associate Data Scientist | https://jobright.ai/jobs/info/6a4734fd0dd56c76cc2fc44a | Jul 2 (1d) | Silent, larger company — **verify** | **New-grad "Leadership Development Program" + "Associate" DS**; Hartford CT; analytics/ML fit | jobright DA |
| Billtrust | AR / order-to-cash fintech SaaS; mid-size | Associate Data Scientist | https://www.billtrust.com/careers/job-openings/?gh_jid=7790504003 (jobright: https://jobright.ai/jobs/info/6a4422ccef17a815538a3064) | 2d (≈Jul 1) | Silent, mid-size — likely OK | **Explicit "Associate" DS** at a fintech SaaS; Hamilton NJ; analytics/ML fit | speedyapply Other + jobright |
| Scopely | Mobile-games publisher (Monopoly GO); large private | Associate Data Scientist | https://job-boards.greenhouse.io/scopely/jobs/5284874008?gh_jid=5284874008 | 2d (≈Jul 1) | Silent, larger company — **verify** | Explicit "Associate" DS; Sunnyvale; games-analytics/ML fit | speedyapply Other + jobright |
| BlackRock | Asset management; large public | Associate – Modelling Data Scientist | https://blackrock.wd1.myworkdayjobs.com/en-US/blackrock_professional/job/Atlanta-GA/Associate--Modelling-Data-Scientist_R264834 | 7d (≈Jun 26) | Silent, larger company — **verify** | "Associate" rung modelling DS (distinct from prior BlackRock rows); Atlanta; analytics/ML fit; gap: large-finance policy | speedyapply Other |
| AEG | Live-entertainment / sports & venues; large private | Associate Data Scientist | https://job-boards.greenhouse.io/aegworldwide/jobs/8589068002 | 7d (≈Jun 26) | Silent, larger company — **verify** | Explicit "Associate" DS; Los Angeles; analytics/ML fit; gap: entertainment domain | speedyapply Other |
| Berkley Insurance (W.R. Berkley) | Commercial P&C insurance; large public | Junior Data Scientist | https://careers-berkley.icims.com/jobs/13854/junior-data-scientist/job | 1d (≈Jul 2) | Silent, larger company — **verify** | **Explicit "Junior" DS + Houston, TX** (in-state); analytics/ML fit; gap: insurance domain | speedyapply Other |
| PNC | Regional bank; large public | Associate Data Scientist – Anti-Money-Laundering Analytics & Modeling | https://pnc.wd5.myworkdayjobs.com/en-US/external/job/PA---Pittsburgh-15222/Associate-Data-Scientist---Anti-Money-Laundering-Analytics---Modeling_R226285-1 | 7d (≈Jun 26) | Silent, larger company — **verify** | Entry "Associate" DS (distinct from the already-logged C&IB req); Pittsburgh; AML anomaly-detection maps to candidate's anomaly work | speedyapply Other |
| NFI Industries | 3PL / supply-chain logistics; large private | Data Engineer I | https://jobright.ai/jobs/info/6a46a4950dd56c76cc2fa468 | Jul 2 (1d) | Silent, larger company — **verify** | **Explicit "Data Engineer I"** entry rung; Camden NJ; dbt/SQL fit; gap: logistics domain | jobright ENG |
| CRISP DC | Regional health-information exchange (health-data nonprofit); mid-size | Data Engineer Associate | https://jobright.ai/jobs/info/6a46b3f1c2d11a6a466702db | Jul 2 (1d) | Unclear — **verify** (DC-area health-data, possible public-sector scope) | **Explicit "Associate" DE**; Columbia MD; dbt/SQL fit; gap: confirm not gov/public-sector gated | jobright ENG |
| Portico PM | Property-management services; mid-size | Analytics Engineer, Automation & AI | https://jobright.ai/jobs/info/6a4330fde09ecb4959643026 | Jun 29 (4d) | Silent, mid-size — likely OK | **"Analytics Engineer" exact target title + Katy, TX** (in-state); dbt/SQL + automation fit; gap: seniority unverified, PM domain | jobright ENG |
| Simulmedia | TV / streaming advertising analytics; mid-size | Generative AI Analyst | https://jobright.ai/jobs/info/69d4015a54f00230c6d2d4ab | Jul 2 (1d) | Silent, mid-size — likely OK | GenAI-analyst (applied-AI + analytics); NYC; adtech domain; gap: seniority unverified | jobright ENG |
| MyAdvice | Digital-marketing SaaS for professional practices; small-mid | AI Engineer I (Generative AI) | https://jobright.ai/jobs/info/6a33b203649fdf16292f2998 | Jul 2 (1d) | Silent, small-mid — likely OK | **"AI Engineer I" entry rung + Remote + GenAI** = strong on-profile; gap: small-co role scope | jobright ENG |
| Amigo | AI-agent startup; seed/early | Applied AI Engineer | https://jobright.ai/jobs/info/6a45ab500dd56c76cc2f4108 | Jul 1 (2d) | Silent, small startup — likely OK | **"Applied AI Engineer" exact target title** at an agent startup (LangGraph/agent flagship fit); SF; gap: tiny-co scope, seniority unverified | jobright ENG |
| Taktile | Automated credit/risk decisioning fintech; growth-stage | Forward Deployed Engineer (Ops) | https://jobright.ai/jobs/info/6a443e0357ffc22029406ca1 | Jun 30 (3d) | Silent, growth startup — likely OK | **FDE target title, COMMERCIAL**; NYC; fintech-decisioning fit; gap: FDE usually wants some customer-facing exp, seniority unverified | jobright ENG |
| Sieve (via David Joseph & Co) | Video/multimodal-AI API platform; startup | Forward Deployed Engineer | https://jobright.ai/jobs/info/6a44806565e80d3c99f2cc21 | Jun 30 (3d) | Silent, small startup — likely OK | FDE at a multimodal-AI-infra startup; SF; ship-end-to-end fit; gap: seniority unverified | jobright ENG |
| Markel | Specialty insurance carrier; large public | Associate AI Business Partner | https://markelcorp.wd5.myworkdayjobs.com/en-US/globalcareers/job/Richmond-VA/Associate-AI-Business-Partner-AI-Business-Partner_R0023422 | 3d (≈Jun 30) | Silent, larger company — **verify** | Entry "Associate" AI role (FDE/Solutions-adjacent — internal AI enablement); Richmond VA; gap: "Business Partner" = enablement-leaning vs pure build | speedyapply Other |
| Providence / Pacific Medical Centers | Health system; large nonprofit | Associate Business Intelligence Analyst | https://jobright.ai/jobs/info/6a46fb538204a812e98cab18 | Jul 2 (1d) | Silent, larger company — **verify** | **Explicit "Associate" BI Analyst**; Renton WA; SQL/BI fit; gap: healthcare-ops domain | jobright DA |
| Steve Madden | Footwear/fashion retail; large public | Junior Business Intelligence Analyst – Digital | https://jobright.ai/jobs/info/6a458a9a48d2f00f2a86de8c | Jul 1 (2d) | Silent, larger company — **verify** | **Explicit "Junior" BI Analyst**; NYC; SQL/BI + e-commerce analytics fit | jobright DA |
| CharterUP | Group-charter bus marketplace; growth-stage | Data Analyst | https://jobright.ai/jobs/info/6a29a8aec07d4b6ae1c4203e (Austin) · https://jobright.ai/jobs/info/6a2999a10c4972328e7e4726 (Denver) | Jul 2 (1d) | Silent, growth startup — likely OK | Data-Analyst target title; **Austin, TX** option (≈in-state); SQL/BI fit; gap: seniority unverified | jobright DA |
| Miller Kaplan | Accounting / advisory firm; mid-size | Junior Data Analyst | https://jobright.ai/jobs/info/6a42d3ad6c326942b4e844d6 | Jun 29 (4d) | Silent, mid-size — likely OK | **Explicit "Junior" DA**; Burbank CA; SQL/BI fit; gap: accounting-advisory domain | jobright DA |
| DataVisor | Fraud-detection / anti-money-laundering AI; mid-size | Data Scientist, AI Solutions | https://jobright.ai/jobs/info/6a276c2c7d827633afffa951 | Jun 29 (4d) | Silent, mid-size — likely OK | DS + **AI-Solutions** (FDE-adjacent) at a fraud-AI co; **anomaly-detection maps to candidate's work**; Mountain View; gap: seniority unverified | jobright ENG |
| iFIT | Connected-fitness software/hardware; mid-large | Junior Salesforce AI Engineer | https://jobright.ai/jobs/info/6a2b32772cde2824469c59b1 | Jul 2 (1d) | Silent, mid-large — likely OK | **Explicit "Junior" AI Engineer + Remote**; gap: Salesforce/CRM-AI niche vs general applied-AI | jobright ENG |

### Tier 3 — Long shots / needs verification / seniority or domain risk

| Company | What they do | Role | Direct link | Posted | Visa posture | Why Tier 3 | Source |
|---|---|---|---|---|---|---|---|
| Ericsson | Telecom-network equipment; large public | Baseband Test AI Developer (Entry Level) | https://jobright.ai/jobs/info/6a47c77bf9cbb100d1ab0f00 | Jul 3 (0d) | Silent, larger company — **verify** | Explicit "Entry Level" + **Austin TX** (appealing), but **baseband/telecom-HW test** domain is far from applied-GenAI/data-eng | jobright ENG |
| The Nuclear Company | Nuclear-power development; growth-stage | AI Engineer 1 – Platform Integration & AI/Data | https://jobright.ai/jobs/info/6a42b3366c326942b4e83c2a | Jun 29–30 (3–4d) | Unclear — **verify** | Explicit "AI Engineer 1" entry + platform/data (appealing), BUT **nuclear → export-control/US-person restrictions plausible**; DC | jobright ENG |
| BMW Group | Auto OEM; large | Machine Learning Engineer | https://jobright.ai/jobs/info/6a477599971cd25b06f92104 | Jul 3 (0d) | Silent, larger company — **verify** | ML-Eng fit, but **seniority unverified** (no entry marker); Mountain View | jobright ENG |
| Chime | Consumer-fintech (neobank); large private | AI/ML Engineer | https://jobright.ai/jobs/info/6a26e9e212f02023422612f6 | Jun 30 (3d) | Silent, larger company — **verify** | AI/ML fit at a strong fintech, but **seniority unverified**; SF | jobright ENG |
| Target | Big-box retail; large public | Data Analyst – Digital & E-commerce (ML / Math-Stats) | https://jobright.ai/jobs/info/6a461bae971cd25b06f8b5a1 | Jun 30 (3d) | Silent, larger company — **verify** | Data-Analyst + experimentation/ML fit, but **seniority unverified**; Minneapolis | jobright ENG |
| Tiki AI | AI-data startup; seed/early | AI Data Software Engineer | https://jobright.ai/jobs/info/6a47016c3dbab558e29a97b0 | Jul 2 (1d) | Silent, small startup — likely OK | AI-data eng at a startup (low visa risk), but company opacity + **scope/seniority unclear**; SF | jobright ENG |
| Together AI | AI cloud / inference infra; growth unicorn | Backend Software Engineer — Data Platform & AI Data Products | https://jobright.ai/jobs/info/69b21a3565de58104c718af6 | Jun 27 (6d) | Silent, growth startup — likely OK | Data-platform fit, but **backend-SWE-leaning** + seniority unverified; SF | jobright ENG |
| RWS Group | Localization / language & content services; large | AI Data Specialist – Texas | https://jobright.ai/jobs/info/6a34af7c1232144fb1560f6d | Jul 2 (1d) | Silent, larger company — **verify** | Texas + AI-data title (appealing), but likely **annotation/localization-ops** vs build; seniority unverified | jobright ENG |
| Tata Consultancy Services | IT services / consulting & staffing; large public | Junior AI/ML Engineer | https://jobright.ai/jobs/info/6a4796a14f64ba41dcb57179 | Jul 3 (0d) | Unclear — **verify** | Explicit "Junior" AI/ML, but **staffing/consultancy → confirm direct FTE, not bench/C2C**; Atlanta | jobright ENG |
| CapTech | IT/management consultancy; large private | Data Engineer (AWS, Azure, GCP) | https://jobright.ai/jobs/info/69b9cedb56973837413f5e12 | Jul 3 (0d) | Unclear — **verify** | DE stack fit, but consultancy (may staff client/gov accounts) + **seniority unverified**; Chicago | jobright ENG |

### Recency-unverified (real links, but zapply "first-seen" minute/hour stamp — NOT a confirmed post date; JD 403)
_Parked separately per the honesty rule. zapply Visa column noted where present (company-level H-1B/sponsor signal, not a per-JD guarantee)._
| Company | Role | Direct link | Note |
|---|---|---|---|
| SWBC | AI Engineer | https://swbc.wd1.myworkdayjobs.com/swbccareers/job/San-Antonio-TX/AI-Engineer_R0015130-1 | Financial-services co; **San Antonio TX** (in-state); AI-Engineer title; "12m" first-seen, seniority unverified |
| VSP Vision | Data Engineer (Snowflake/DataStage) | https://vsp.wd1.myworkdayjobs.com/vspvisioncareers/job/Remote-US/Data-Engineer--Snowflake-DataStage-_R-9701 | **Remote-US**; Snowflake/ETL DE fit; "42m" first-seen, seniority unverified |
| Contoro Robotics | Data Engineer, Cloud Platform | https://jobs.ashbyhq.com/contoro/82ee31ed-0418-4fc9-a07b-ebc5998bf5a1/application | Warehouse-robotics startup; **Austin TX** (in-state); ✅ Sponsor (zapply); "21h" first-seen |
| Affirm | AI Solutions Engineer | https://job-boards.greenhouse.io/affirm/jobs/7778204003 | BNPL fintech; **Remote-US**; **"AI Solutions Engineer" target title**; ✅ Sponsor; "1d" first-seen, seniority unverified |
| Stripe | AI Engineer | https://stripe.com/jobs/search?gh_jid=8044460 | Payments; Chicago; AI-Engineer title; ✅ Sponsor; "4h" first-seen, **seniority unverified** (Stripe AI Eng usually mid+) |
| Centerfield | Data Engineer | https://jobs.ashbyhq.com/centerfield/63b6469a-64cb-4c8f-bf80-80c6dbe0f1bc/application | Digital-marketing/ad-tech; Los Angeles; ✅ Sponsor; "1d" first-seen, seniority unverified |

### Community / informal leads (YC Work-at-a-Startup — surfaced via WebSearch; HN July thread unreadable)
_**HN July 2026 thread `48747976` is LIVE but every read path 403'd** (Algolia/hnrss = 000; hnhiring/emilburzo/nchelluri mirrors = 403). WebSearch-over-mirrors returned only EU/senior snippets (EggAI remote-EU, Ojin CET±2h, plus "5+ years" roles) with no per-post links → **no US entry-level HN lead could be logged with a link this run.**_
_The YC links below are **real direct URLs** (the pages themselves 403, so JD bodies — seniority, exact post date, visa language — are UNVERIFIED). All are YC seed/early startups (visa: silent, small startup → OPT needs no sponsorship, generally OK; tiny startups sometimes can't accommodate — verify). Open each to confirm entry-level + US-eligibility before applying._
- **StackAI** — Forward Deployed AI Engineer (enterprise RAG pipelines + LLM workflows) — **strong RAG/LLM fit**. https://www.ycombinator.com/companies/stackai/jobs/uRDrhI2-forward-deployed-ai-engineer
- **Luminai** — Forward Deployed Engineer (embed with customers to deploy AI solutions; San Mateo hybrid). https://www.ycombinator.com/companies/luminai/jobs/9s487sF-forward-deployed-engineer
- **Automat** — Forward Deployed Engineer (customer-facing automation/efficiency). https://www.ycombinator.com/companies/automat/jobs/QfHWU1w-forward-deployed-engineer
- **Amigo** — (also in Tier 2 via jobright) Applied AI Engineer. https://jobright.ai/jobs/info/6a45ab500dd56c76cc2f4108
- **Model ML** — Applied AI Engineer (AI-native workspace for IB/PE/asset-mgmt) — **verify seniority** (serial-founder team, production deployments → may skew mid). https://www.ycombinator.com/companies/model-ml/jobs/XKYq3QI-applied-ai-engineer
- **Firstbase.io** — Applied AI Engineer (remote-work infra SaaS). https://www.ycombinator.com/companies/firstbase-io/jobs/AqftNFh-applied-ai-engineer
- **DeepAware AI** — AI/ML Engineer (RL for data-center infra optimization + anomaly detection — **anomaly-detection fit**). https://www.ycombinator.com/companies/deepaware-ai/jobs/2x0wzJp-ai-ml-engineer
- **Karumi** — AI/ML Applied Engineer (voice AI + browser automation + LLM agents). https://www.ycombinator.com/companies/karumi/jobs/Ht5Bs00-ai-ml-applied-engineer
- **AfterQuery** — Software Engineer – Applied AI / Platform. https://www.ycombinator.com/companies/afterquery/jobs/7tsT0ks-software-engineer-applied-ai-platform
- **Confido** — **New Grad Software Engineer** (ML/AI highly preferred; ≥1 SWE internship; NYC; ~$150k + bonus + equity) — **explicit new-grad**. https://www.ycombinator.com/companies/confido/jobs/qA04RvS-new-grad-software-engineer
- **Artisan** — Data Engineer (Remote-US, $150–220k; "first Data Engineer" on team) — **verify seniority** ("first DE" can skew senior despite no label). https://www.ycombinator.com/companies/artisan/jobs/cWH5YZe-data-engineer
- **SpruceID** — Full-Stack Software Engineer (**New Grad**) – Remote — SWE-leaning but explicit new-grad + remote. https://www.ycombinator.com/companies/spruceid/jobs/xscY5WF-full-stack-software-engineer-new-grad-remote
- **EXCLUDED:** Arist & Dataland ("**Founding** FDE"), Misprint ("**Lead**/Founding ML & Data Eng"), Retell AI ("**Senior** FDE"), Acely/Handle/Instrumentl (**Sr** Data Eng) — seniority; **telli** (FDE-AI, **Germany**) & **Prembly** (DA+ML, **Nigeria**-based identity co) — geography (F-1 OPT is US-only); Paragon (FDE **Intern**), Surface Labs (AI GTM **Intern**) — interns.

### Excluded (logged so future runs don't re-surface)
- **FAANG-tier / FAANG-owned (referral track):** Amazon/AWS (Data Engineer WWGS, DE Ads-Science ASAT), Meta (Data Engineer University Grad), PayPal (MLE Chicago/Austin), Roblox (SWE Data Eng), NVIDIA (Applied MLE Circuit-Design NCG — but NCG/FAANG+), TikTok/ByteDance (many ML/Applied-Scientist/DE — mostly PhD/2027), Intel/Adobe/Zoom/Visa/Etsy (Machine Learning/Data Scientist rows in zapply — non-FAANG but either logged, minute-stamp recency-unverified, or seniority-unverified; kept out of tiers).
- **Defense / federal / clearance (US-person near-certain):** Booz Allen Hamilton (Training-Equipment DS Pensacola, DS Arlington/Chantilly, AI/ML Eng Arlington, AI Engineer Arlington, AWS Streaming DE Springfield, DS-Junior Springfield), GDIT (DS Fort-Bragg-Mid, DS-Junior Jacksonville), CACI (Data-Access-Layer DE ×2, DE/Software-Integrator Denver, AI/ML Eng Co-op, DS-for-Analytics Norco), KBR (TAGM DE Redstone), Leidos (DS McLean), Noblis (DA Network-Security Atlantic City), Systems Planning & Analysis (Jr DS Alexandria), A-TEK (Health-IT DA I; Federal AI Solutions Eng — federal), SpaceX (FDE Mission-Systems **Starshield**), MANTECH (Agentic AI Dev), Lockheed Martin (A/AI MLE Early-Career), Boeing (Experienced/Full-Stack DS), Peraton (GenAI Eng Intern), DeVine Consulting (Atmospheric-Science ML — gov-adjacent), National Laboratory of the Rockies (Postdoc ML — FFRDC).
- **Non-US geography (F-1 OPT is US-only):** telli (Germany), Prembly (Nigeria), EggAI (remote EU/Switzerland/Norway — from HN), Ojin (CET±2h — from HN), Canadian Chamber of Commerce (Ottawa), plus intl tracker rows.
- **Intern / co-op / part-time / residency (candidate grads May 2026 — weak timing fit):** Tesla (Software-ML / Applied-AI-HW / ML-Platform / Data-Engineer / Data-Analyst / People-Analytics interns), TikTok/ByteDance/Integra FEC (DS/DA/DE interns), Nokia (Compliance DS Co-op), John Deere (Part-Time Student DE), Trane / W.R. Berkley / Bosch / Intel (BI/DTCO interns), SharkNinja (Applied-AI & Analytics Co-op Fall-2026), Paragon (FDE Intern), Surface Labs (AI GTM Intern), Aptura (AI Residency — **part-time**, ×5 IB/finance-flavored), IMC Trading (ML Research Intern).
- **Senior / II+ / lead / founding / PhD / trading-floor-quant:** Socratix (**Founding** Full-Stack AI Eng), Arist/Dataland/Misprint (Founding/Lead FDE-ML), Retell (Senior FDE), Acely/Handle/Instrumentl/Artisan? (Sr Data Eng — Artisan kept in Community with a verify flag), PwC (CTIO AI Eng — **Experienced** Associate), Toyota Research Institute (ML Research Scientist), Scale AI (ML **Research** Eng — high bar), The Voleon Group / Point72 (systematic/prop-research DS — trading-floor-adjacent), Hudson River Trading / Optiver / Akuna / D.E. Shaw (Quant Researcher — PhD/trading-floor), Kroenke Sports (DS **Contract**, Colorado Avalanche).
- **Wet-lab / clinical / non-data research (not applied-AI/data-eng):** Emory (Assoc Academic Research Scientist – Pathology), Mass General Brigham (Research DA), University of Rochester Advancement (DS — fundraising-ops), Corning (QA DA), Aptiv (QLIK/Quality DA), Symbotic (DA-Quality), RELX (DA Drug-Product-Content), plus jobright "Research/Clinical Data" rows.
- **Public-sector / residency-gated:** CalPERS, California Correctional Health Care Services, Sacramento Steps Forward, Turning Point Community Programs, WaFd Bank BI (kept out — commercial but seniority-unverified), Civic Nation / Consumer Reports (limited-duration).

### Bonus — adjacent titles worth adding to the search vocabulary
- **"Associate AI Engineer" (Northern Trust) / "AI Engineer I" (MyAdvice) / "AI Engineer 1" (Nuclear Co)** — explicit entry rungs of the exact target title at banks/SaaS; keep prioritizing the "Associate/I/1" suffix.
- **"Data Scientist I – University Program" (FIS) / "Engineering Development Program – Data Engineering" (Travelers) / "Data Science Leadership Development Program" (Travelers)** — **named new-grad rotational programs** are a high-signal way to catch entry roles whose titles omit "new grad"; add "University Program" / "Development Program" / "Leadership Program" as explicit search terms (reinforces SS&C "Launch Program", Westinghouse "NGLP" from prior runs).
- **"Associate AI Business Partner" (Markel) / "Generative AI Analyst" (Simulmedia) / "Data Scientist, AI Solutions" (DataVisor)** — applied-AI/FDE-adjacent titles that hide the AI work behind an "Analyst/Business-Partner/Solutions" label.
- **"Associate Data Engineer" at HR-tech (Phenom)** — a people/talent-analytics platform hiring entry DE = a back-door onto the **People-Analytics / HR-Data** target.
- **YC "Forward Deployed (AI) Engineer" cluster keeps growing** (StackAI, Luminai, Automat this run; FurtherAI/Soff/Maywood prior) — WebSearch over `site:ycombinator.com/companies … jobs` for "Forward Deployed Engineer" / "Applied AI Engineer" remains the most productive community channel; run it every pass.

### TODO for next (daily) run
- **JULY 2026 HN thread `48747976` is LIVE** but still 403 on every read path (Algolia
  API / hnrss = 000 egress; hnhiring / emilburzo / nchelluri mirrors = 403 WebFetch).
  It's the #1 un-mined community opportunity — a readable path (authenticated fetch, or
  a mirror that serves per-post links) is the single highest-value unsolved item. The
  companion "Who wants to be hired?" is `48747975`.
- **WebSearch over YC Work-at-a-Startup** remains the one working community channel
  (real direct links, JD bodies 403). Run it every pass for the target titles.
- **JD/visa verification** unchanged #1 structural blocker: greenhouse/jobright/workday/
  ashby/oracle/smartrecruiters all 403 (WebFetch) or 000 (curl egress) → all visa buckets
  inferred, all "seniority unverified" flags stand.
- **speedy parser bug fixed this run** (the 5-column "Other" table now parses — it had
  been under-read on prior runs because the parser assumed the 6-column FAANG/Quant
  layout). Keep the width-detecting parser.
- **jobright Data-Analysis** still caps at "last 7 days"; **speedyapply + zapplyjobs +
  jobright-Engineering** remain the reliable curl+parse trio.

---

## Run: 2026-07-04 17:12 (DEEP BACKFILL — 30 day window)

**THIS IS A ONE-TIME DEEP BACKFILL, NOT A DAILY PASS.** Run 2026-07-04, 30-day
window (~Jun 4 – Jul 4). Future daily runs should keep using 24h and treat everything
below as already-seen.

**⚠️ CONCURRENCY / DE-DUP NOTE (read first — this shapes the whole entry):** When this
run started, the local checkout was stale at the **06-25** commit, so I initially
de-duped against runs through 06-25. While I was working, **two more backfills landed
on `main`: 06-29 17:10 and 07-03 17:15** — and the 07-03 run (just one day before this
one) used the same 30-day window and the same sources, so it already logged the large
majority of what this run's sources surfaced. Before committing, I fetched, re-based on
the updated `main`, and **re-de-duped every candidate against the 06-29 and 07-03 runs.**
Result: most of my raw findings were exact repeats (same company+role, often same link)
and have been dropped per the append-only skip-exact-repeats rule. **Only the genuinely
net-new leads (not in any prior run, including 06-29/07-03) are logged below** — a short,
honest list rather than a padded one that re-surfaces yesterday's rows.

Examples of raw hits DROPPED as already logged in 06-29/07-03: Affirm (AI Solutions Eng,
same greenhouse link), MyAdvice (AI Engineer I GenAI), Together AI (Analytics Eng — Data
Warehouse), Scopely, DataVisor, AssetMark, NBCUniversal, Target, Simulmedia, NFI, CRISP DC,
Phenom, Amigo, Taktile, Reynolds, Chime, iFIT, Billtrust, Providence/Pacific Medical,
Steve Madden, Sieve, MeritFirst, Stripe, SWBC, BMW, xAI, Scale AI, Contoro, Motorola,
The Nuclear Company, Tata Consultancy, Clear Investment, Centerfield, VSP Vision, Ericsson.

**Coverage & honesty notes:**
- **METHOD (worked again):** `curl`-ed the raw markdown trackers from
  `raw.githubusercontent.com` (NOT egress-blocked; all four returned HTTP 200) and parsed
  locally with Python. Keep using curl+local-parse, not WebFetch, for the trackers.
- **Fully covered (curl'd raw + parsed locally):**
  - `speedyapply/2026-AI-College-Jobs` → `NEW_GRAD_USA.md` (233 rows) — read in full;
    **mostly STALE this run** (age distribution dominated by 50–110d rows; only a few
    in-window, nearly all already logged). Low net-new yield.
  - `zapplyjobs/New-Grad-Data-Science-Positions` (913 jobs / 186 cos) — read in full;
    richest source. Carries a Visa column (`🏛 H-1B Co.` / `✅ Sponsor` / blank), noted
    per row (company-level signal, NOT a per-JD guarantee).
  - `jobright-ai/2026-Engineering-New-Grad` (1.58 MB) — read in full; calendar-dated.
    In-window target rows span **Jun 27 – Jul 4** only (older target rows aged off).
  - `jobright-ai/2026-Data-Analysis-New-Grad` — read in full, still **caps at "last ~7
    days" (Jun 28 – Jul 4)**; 30-day depth unavailable (same as prior runs).
- **NOT covered / blocked — UNCHANGED structural blockers:**
  - **Individual JD verification — ALL still blocked.** `curl` to greenhouse/ashby/workday
    = **HTTP 000 (CONNECT denied by egress policy)**; `WebFetch` to greenhouse = **403**.
    Could not read a single JD body → EVERY visa bucket is inferred from company type +
    role (+ zapply's H-1B column where present), NOT JD text. Every "verify" must be opened
    manually. Seniority for any role not explicitly labeled entry/junior/associate/"I"/"1"
    is **unverified** and flagged.
  - **Community boards — HN STILL unreadable.** The **July 2026 "Ask HN: Who is hiring?"
    thread is LIVE: id `48747976`** (June was `48357725`). All four machine-read paths
    403'd: `hn.algolia.com/api/v1/search`, `hn.algolia.com/api/v1/items/48747976`,
    `news.ycombinator.com/item?id=48747976`, `hnrss.org/item?id=48747976`. WebSearch
    confirmed the thread exists but returned only aggregator landing pages
    (Glassdoor/Indeed/Wellfound/BuiltIn/ZipRecruiter) with **no per-post direct links**.
    → Nothing from HN logged. Reddit still hard-blocked.
  - LinkedIn / Indeed / Glassdoor / Wellfound / Built In: only aggregator landing pages,
    no per-posting dates or stable direct links — nothing logged. No founder/recruiter
    post with a stable direct link surfaced.
- **Recency basis:** jobright rows = calendar dates (Jun 27 – Jul 4). speedyapply = "age"
  field vs Jul 4 refresh. zapplyjobs minute/hour stamps ("13m","2h") are scraper
  **first-seen** stamps, NOT post dates → flagged recency-unverified.

### Tier 1 — Hot & strong fit (net-new only)
_Entry-labeled + exact-target-title, recent, non-defense, non-FAANG. Visa inferred (JDs 403/000)._

| Company | What they do / size | Role | Direct link | Posted (basis) | Visa posture | Fit note | Source |
|---|---|---|---|---|---|---|---|
| Giga | AI startup (voice/agent infra); early/growth | Forward Deployed Engineer I/II | https://jobright.ai/jobs/info/6a2c669ed3ec94183f4bcafa | Jul 4 (0d) | Silent, small startup — likely OK | **"Forward Deployed Engineer I/II" = exact target title with an explicit entry rung**, commercial (not defense); SF; gap: FDE expects some customer-facing polish | jobright ENG |
| Penumbra | Medical-device (neuro/vascular) w/ software; large public | Associate Forward Deployed Engineer | https://jobright.ai/jobs/info/6a484dfc971cd25b06f940b3 | Jul 3 (1d) | Silent, larger company — **verify** | **Explicit "Associate" FDE** = entry rung of a bullseye target title; Alameda CA; gap: med-device domain + large-co policy | jobright ENG |

### Tier 2 — Worth a look (net-new; caveat = seniority and/or visa unverified, JD 403/000)

| Company | What they do / size | Role | Direct link | Posted (basis) | Visa posture | Fit note | Source |
|---|---|---|---|---|---|---|---|
| Snowflake | Data-cloud platform; large public | Analytics Engineer | https://jobs.ashbyhq.com/snowflake/41d8e346-2919-40bf-b5f3-22e3b34ed34c/application | "3d" first-seen (≈Jul 1) | ✅ Sponsor (zapply) → likely OPT-OK, **verify** | **Analytics Engineer exact target title** (distinct from the already-logged Snowflake FDE roles); Menlo Park; dbt/SQL fit; gap: seniority unverified | zapplyjobs |
| CoreWeave | AI/GPU cloud infrastructure; large public (non-FAANG) | Data Scientist | https://coreweave.com/careers/job?4694223006&board=coreweave&gh_jid=4694223006 | "1d" first-seen (≈Jul 3) | ✅ Sponsor (zapply) → likely OPT-OK, **verify** | DS at a fast-growing AI-infra co (distinct from the "SWE Inference AI/ML" role logged 07-03); NYC; analytics/ML fit; gap: seniority unverified | zapplyjobs |
| Torc Robotics | Autonomous-trucking (Daimler Truck); growth-stage | Software Engineer, I – Data Engineering | https://jobright.ai/jobs/info/6a3e6a5178237a036d5e3e86 | Jul 4 (0d) | Silent, larger company — **verify** | **Explicit "I" entry** Data-Engineering SWE; Ann Arbor MI; dbt/SQL/Airflow fit; commercial (not defense); gap: AV domain | jobright ENG |
| CNN (Warner Bros. Discovery) | Media/news; large public (non-FAANG) | Machine Learning Engineer I | https://jobright.ai/jobs/info/6a0e3cf483d71442898176dc | Jul 3 (1d) | Silent, larger company — **verify** | **Explicit "I" entry** ML Engineer; NYC; applied-ML fit; gap: media domain + large-co policy | jobright ENG |
| Becton Dickinson (BD) | Medical-device / diagnostics; large public (~70k) | Commercial Analytics Engineer (Go-To-Market / Business Decision Intelligence) | https://jobright.ai/jobs/info/6a48d667971cd25b06f94b37 (ATS: https://bdx.wd1.myworkdayjobs.com/EXTERNAL_CAREER_SITE_USA/job/USA-NJ---Franklin-Lakes/Commercial-Analytics-Engineer---Go-To-Market-Analytics_R-548948-1) | Jul 3–4 (0–1d) | 🏛 H-1B Co. (zapply) → likely OPT-OK, **verify** | **Analytics Engineer target title**; Franklin Lakes NJ; SQL/BI fit; gap: seniority unverified, med-device domain | jobright DA + zapplyjobs |
| Commonfund | Nonprofit-focused asset manager; mid-large | AI/ML Development Analyst | https://jobright.ai/jobs/info/6a2484edd46c0f799608720c | Jul 3 (1d) | Silent, mid-large — verify | Entry-flavored "AI/ML Development Analyst"; Norwalk CT; applied-ML+analytics fit; gap: analyst-leaning, finance domain | jobright ENG |
| Nanonets | Document-AI / IDP startup; growth-stage | Forward Deployed Engineer | https://jobright.ai/jobs/info/6a4885fa971cd25b06f944f6 | Jul 3 (1d) | Silent, growth startup — likely OK | **FDE target title** at a doc-AI/LLM startup (strong stack fit); Palo Alto; gap: seniority unverified | jobright ENG |
| Upstart | AI-lending fintech; large public | Data Analyst, Home Lending (HMDA), Remote US | https://careers.upstart.com/jobs?gh_jid=8038452 | "4d" first-seen (≈Jun 30) | ✅ Sponsor (zapply) → likely OPT-OK, **verify** | **Remote** Data-Analyst at an AI-first fintech; SQL/BI fit; gap: HMDA/lending-compliance niche, seniority unverified | zapplyjobs |
| Eversource Energy | Electric/gas utility; large public | IT Associate Data Analyst | https://eversource.wd1.myworkdayjobs.com/ExternalSite/job/Westwood-MA/IT-Associate-Data-Analyst_R-030512 | "2h" first-seen (recency-unverified) | 🏛 H-1B Co. (zapply) → likely OPT-OK, **verify** | **Explicit "Associate" entry** DA; Westwood MA; SQL/BI fit; gap: utility-IT domain, recency is a scraper stamp | zapplyjobs |

### Tier 3 — Long shots / needs verification / seniority or domain risk (net-new)

| Company | What they do | Role | Direct link | Posted | Visa posture | Why Tier 3 | Source |
|---|---|---|---|---|---|---|---|
| PayPal | Payments fintech; large public (non-FAANG) | Machine Learning Engineer | https://jobright.ai/jobs/info/6a079994403fc339507e6589 | Jul 2 (2d) | Silent, larger company — **verify** | ML-Engineer fit but **no entry marker → likely mid+**; Chicago | jobright ENG |
| Bot Auto | Autonomous-trucking startup; growth | Machine Learning / Deep Learning Engineer | https://job-boards.greenhouse.io/botauto/jobs/5290395008 | "1d" first-seen (≈Jul 3, Spon) | Silent, growth startup — likely OK | ML/DL Engineer, **Houston TX or SF**; applied-ML fit; gap: seniority unverified, AV domain | zapplyjobs |
| Ludo Robotics | Robotics/AI startup; early | ML/AI Engineer | https://jobright.ai/jobs/info/69ba0cac06c1ba00c54c2c35 | Jul 1 (3d) | Silent, small startup — likely OK | ML/AI-Engineer title at a robotics startup; SF; gap: seniority unverified, tiny co | jobright ENG |
| Rolls-Royce | Aerospace/defense propulsion; large | Junior Machine Learning Engineer | https://jobright.ai/jobs/info/6a46d7908204a812e98ca303 | Jul 2 (2d) | **Likely restricted** — aerospace/defense → export-control/US-person plausible | Explicit "Junior" MLE (appealing), Indianapolis, but defense-adjacent export-control risk | jobright ENG |
| iSpot | TV-ad measurement analytics; mid-size | Research Data Scientist 1 | https://jobright.ai/jobs/info/6a16550b1935fa61b3c70d1f | Jul 3 (1d) | Silent, mid-size — verify | Entry "1" DS (research-titled), Bellevue WA; measurement-analytics fit; gap: research-leaning | jobright DA |
| Xometry | On-demand manufacturing marketplace; mid-large public | Analytics Engineer II | https://job-boards.greenhouse.io/xometry/jobs/5179344007 | "1d" first-seen (≈Jul 3, Spon) | Silent, larger company — **verify** | Analytics-Engineer target title, Waltham MA, BUT **"II" likely wants ~2 yrs** | zapplyjobs |
| MassMutual | Life insurance; large mutual | Quantitative Developer | https://jobright.ai/jobs/info/6a46166f3dbab558e29a38c5 | Jul 3 (1d) | Silent, larger company — **verify** | Quant-developer (non-trading-floor, insurance) — Quant-Analyst-adjacent target; NYC; gap: seniority unverified | jobright DA |
| Netrolynx AI | Small AI services co (opaque); small | Data Analyst | https://jobright.ai/jobs/info/6a4917065d7b097d2df3ac21 | Jul 4 (0d) | Unclear — **verify** | Data-Analyst title at an opaque small AI co, US-remote; verify legitimacy/scope before effort | jobright DA |

### Recency-unverified (net-new; in-window per zapply scraper first-seen stamp; JD 403)
| Company | Role | Direct link | Note |
|---|---|---|---|
| ResMed | Data Engineer | https://resmed.wd3.myworkdayjobs.com/ResMed_External_Careers/job/San-Diego-CA-United-States/Data-Engineer_JR_052285 | "4d" first-seen; San Diego med-device; seniority unverified |
| Nissan | Data Engineer | https://alliance.wd3.myworkdayjobs.com/nissanjobs/job/Franklin-Tennessee---United-States-of-America/Data-Engineer_R00205289-1 | "5d" first-seen; Franklin TN; seniority unverified |

### Community / informal leads
_**Nothing logged.** July 2026 HN "Who is hiring?" thread (id `48747976`) is LIVE but 403'd
on all four machine-read paths; WebSearch returned only aggregator landing pages with no
per-post links. No founder/recruiter post with a stable direct link surfaced. Same blocker
as all prior runs._

### Excluded (net-new sightings this run, logged so future runs don't re-surface)
- **FAANG-tier (referral track):** Amazon/AWS (Applied Scientist II, Data Engineer ASAT/Ads, Data Scientist II MOI), Meta (Data Engineer Product Analytics Univ Grad), Google (AI Research Scientist Applied AI), TikTok/ByteDance (many ML/Applied-Scientist graduate rows), Roblox (SWE Data Engineering — non-FAANG but seniority unverified).
- **Defense / federal / clearance / export-control (US-person near-certain):** SpaceX (AI Engineer Special Programs "Top Secret", Platform Infra Special Programs, FDE Mission Systems Starshield, ML Surrogate Modeling), Innovative Defense Technologies (Associate AI Engineer), Booz Allen (Data Scientist ×many, AI Engineer, AI/ML Engineer, AWS Streaming DE, DE Fort Meade/Honolulu), CACI (Data Scientist/SWE ×several, DE Denver/Kafka, Data Analyst Chantilly), KBR (Data Scientist I/II, TAGM DE Redstone), Leidos (Data Scientist McLean), GDIT (Data Scientist Mid Fort Bragg), RTX (Data Scientist "Top Secret" Plano), Guidehouse (Data Scientist Arlington), Anduril (Security/Product DE), Accenture Federal (Data Analyst "Secret"), Radiance/Noblis (Data Analyst), Blue Origin (BI Analyst II).
- **Non-US geography (F-1 OPT is US-only):** Connor Clark & Lunn / NumerixS / Canadian Chamber / mthree / Flight Centre (Canada), Caterpillar (Peterborough UK), Islington Council / Xantium (UK), Thumbtack (Remote Ontario).
- **Trading-floor quant / PhD-required (profile wants non-trading-floor):** The Voleon Group (DS — systematic hedge fund), Two Sigma / Susquehanna (SIG) / IMC Trading / Edgehog / Virtu Financial (Quant Researcher/Trader).
- **Senior / II+ / intern / co-op / research-lab:** NVIDIA (Applied ML Circuit Design NCG, Research Scientist Gen-AI NCG, Document-AI DE), Nokia (Compliance DS Co-op), John Deere (Part-Time Student DE), Kaiser Permanente (R/Python Programmer — clinical), HPE (DS / DS-Agentic-AI), Intel/Cisco/Comcast/Honeywell/J&J (ML/DS — seniority unverified mid+), Federal Reserve (ML Research Assistant), D.E. Shaw (Applied AI Engineer / ML Researcher — quant firm high bar).
- **Already logged in 06-29/07-03 (dropped as exact repeats):** see the ⚠️ concurrency note above for the full list (Affirm, MyAdvice, Together AI, Scopely, DataVisor, AssetMark, NBCUniversal, Target, Simulmedia, NFI, CRISP DC, Phenom, Amigo, Taktile, Reynolds, Chime, iFIT, Billtrust, Providence, Steve Madden, Sieve, MeritFirst, Stripe, SWBC, BMW, xAI, Scale AI, Contoro, Motorola, The Nuclear Company, Tata Consultancy, Clear Investment, Centerfield, VSP Vision, Ericsson).

### Bonus — adjacent titles worth adding to the search vocabulary
- **"Forward Deployed Engineer I/II" (Giga) / "Associate Forward Deployed Engineer" (Penumbra)** — the FDE target has **explicit entry rungs at commercial (non-defense) employers**; add "Associate/I/II FDE" as first-class entry keywords (reinforces the same finding from the 07-03 run's Monte Carlo/Sieve/Taktile FDE sightings).
- **"AI/ML Development Analyst" (Commonfund)** — applied-ML work behind an "Analyst" label at an asset manager.
- **"Commercial Analytics Engineer" (BD)** — Analytics-Engineer target title with a go-to-market/BI flavor.
- **TX geo net still worth keeping:** Bot Auto (Houston/SF); prior-run TX rows (MeritFirst/Contoro Austin, Hunt Oil Dallas) already logged.

### TODO for next (daily) run
- **CONCURRENCY:** multiple backfills are now landing on `main` within days of each other
  (06-25, 06-29, 07-03, 07-04). Always `git fetch origin main` and read the LATEST log
  before de-duping — a stale local checkout caused most of this run's raw hits to be repeats.
- **Keep curl + local Python parse, NOT WebFetch, for the trackers** (worked again).
- **Community:** July HN thread id `48747976`; all machine-read paths still 403/000. #1
  unsolved community gap. Reddit still hard-blocked.
- **JD/visa verification** unchanged #1 structural blocker: greenhouse/ashby/workday 403
  (WebFetch) / 000 (curl egress-denied). All visa buckets inferred; zapply's H-1B column
  is the only per-company signal.
- **speedyapply NEW_GRAD_USA is going stale** (50–110d-dominated) — lean on zapply + jobright ENG.

---

## Run: 2026-07-05 17:14 (DEEP BACKFILL — 30 day window)

**THIS IS A ONE-TIME DEEP BACKFILL, NOT A DAILY PASS.** Run 2026-07-05, 30-day
window (~Jun 5 – Jul 5). Future daily runs should keep using 24h and treat everything
below as already-seen. Read `leads_log.md` in full first and de-duped against ALL nine
prior runs — **including yesterday's 07-04 backfill and the 07-03 backfill, which used
this same 30-day window and the same sources one day apart.** As a result the large
majority of what this run's trackers surfaced was already logged; **only genuinely
net-new leads (not in any prior run) appear below** — a deliberately short, honest list
rather than a padded one re-surfacing yesterday's rows.

**Coverage summary (what was covered fully / partially / not at all):**
- **FULLY COVERED (curl'd raw markdown from `raw.githubusercontent.com`, HTTP 200, parsed
  locally with Python — the proven method; NOT WebFetch):**
  - `speedyapply/2026-AI-College-Jobs` → `NEW_GRAD_USA.md` (78 KB, 246 positions) — read in
    full. **Continuing to go stale** (age distribution dominated by 20–70d rows); low net-new
    yield, ~2 net-new after de-dup.
  - `zapplyjobs/New-Grad-Data-Science-Positions` (85 KB, 902 jobs / 183 cos) — read in full;
    richest source. Carries a Visa column (`🏛 H-1B Co.` / `✅ Sponsor` / blank) = **company-level**
    sponsorship signal (generally OPT-friendly), NOT a per-JD guarantee. ~79 target-title rows
    after filtering, most already-logged / FAANG / defense / senior / research / intern.
  - `jobright-ai/2026-Engineering-New-Grad` (1.59 MB) — read in full; calendar-dated. In-window
    target rows span **Jun 29 – Jul 05** (older target rows have aged off the visible list).
  - `jobright-ai/2026-Data-Analysis-New-Grad` (60 KB) — read in full, still **caps at "last ~7
    days" (Jun 29 – Jul 05)** per its capacity constraint; 30-day depth unavailable (same cap
    every prior run).
- **PARTIALLY COVERED (WebSearch works, but underlying pages 403 so bodies unverified):**
  - **YC Work-at-a-Startup** — `WebSearch` over `site:ycombinator.com/companies … jobs` returns
    real direct `ycombinator.com/companies/.../jobs/` URLs (the one reliable community channel).
    JD pages themselves 403, so seniority / exact post date / visa language are UNVERIFIED. Fresh
    net-new FDE cluster logged in the Community section.
  - **HN July 2026 mirrors** — `WebSearch` over the mirrors surfaced *named* companies this run
    (Prior Labs, Puntt AI, August Health, Tenera, Prolific) but **no per-post direct links**; see
    the HN note below.
- **NOT COVERED / BLOCKED (unchanged structural blockers, re-confirmed this run):**
  - **Individual JD verification — ALL still blocked.** `WebFetch` to greenhouse (NewsBreak JD)
    = **403**; every prior run's greenhouse/ashby/workday/oracle/smartrecruiters = 403/000. **No
    JD body read** → EVERY visa bucket below is inferred from company type + role (+ zapply's
    H-1B column where present), NOT JD text. Every "verify" must be opened manually. Seniority
    for any role not explicitly labeled entry/junior/associate/"I"/"1"/new-grad/program is
    **unverified** and flagged inline.
  - **HN "Ask HN: Who is hiring? (July 2026)" thread `48747976` — LIVE but every machine-read
    path 403'd AGAIN:** `hn.algolia.com/api/v1/items/48747976` = **403**; `hnhiring.com/search`
    = **403**; `nchelluri.github.io/hnjobs/` = **403**. Companion "Who wants to be hired?" =
    `48747975`. `WebSearch`-over-mirrors named a few cos (Prior Labs FDE-ML — likely EU/Freiburg;
    Puntt AI — see Community; August Health — Applied-AI, but its only open AI role is *Senior*;
    Tenera — new-grads-welcome but likely EU construction-tech; Prolific — AI Solutions Eng, UK)
    with **no stable per-post direct links** → no *additional* US entry-level HN lead could be
    logged with a real link. This remains the #1 un-mined community gap.
  - **Reddit / Discord / Slack** — not machine-readable (hard-blocked every prior run). No active
    datable "who's hiring" thread surfaced with per-post links.
  - **LinkedIn / Indeed / Glassdoor / Wellfound / Built In** — only aggregator landing pages, no
    per-posting dates or stable direct links → nothing logged. No founder/recruiter post with a
    stable direct link surfaced this run.
- **Recency basis:** jobright rows = calendar dates (Jun 29 – Jul 05, used directly). speedyapply
  = "age" field vs the Jul-5 refresh (reliable to the day). **zapplyjobs minute/hour/day stamps
  ("14m", "1h", "3d"–"6d") are scraper FIRST-SEEN stamps, NOT confirmed post dates** — but for a
  30-DAY window even a "6d first-seen" comfortably falls inside the window, so zapply day-stamped
  net-new rows are tiered here (with the first-seen caveat noted), and only minute/hour-stamped
  ones are parked in Recency-unverified.
- **De-duped OUT as already logged** (surfaced again this run, NOT repeated below): NewsBreak
  Applied AI Eng, Quantifind Assoc DS, Bank of America Client-Quant-Analyst-I / Associate-Quant,
  Jerry Assoc DS (new NY/Remote ashby links noted but company+role logged 06-20+), Scopely Assoc
  DS, Esri DS I, PTC Jr DA/Analytics Eng, iSpot Research DS 1, BD Commercial Analytics Eng,
  UST + UST HealthProof Assoc DE, Tata Consultancy Jr AI/ML + Jr DE, CNN MLE I, AssetMark Assoc DE,
  Phenom Assoc DE, XiFin Assoc MLE, The Nuclear Company AI Eng 1, Innodata GenAI Associate, CBTS
  Jr DE, MeritFirst AI Eng, Simulmedia GenAI Analyst, Motorola AI Solutions Dev, Amigo Applied AI
  Eng, Reynolds AI Solutions Analyst, PayPal MLE, Together AI Analytics Eng, iFIT Jr Salesforce AI
  Eng, Unity MLE, CVS Health DE, Voleon DS, WaFd BI, Symbotic DA, HPE DS, Home Depot Assoc DS
  (new req), Labcorp Assoc DS, Truist DS I, SBT Global Jr DA, Gen Digital MLE I.

### Tier 1 — Hot & strong fit (net-new)
_Entry-labeled + low-visa-risk + on-target-title + in-window. Visa inferred (JDs all 403/000)._

| Company | What they do / size | Role | Direct link | Posted (basis) | Visa posture | Fit note | Source |
|---|---|---|---|---|---|---|---|
| Hays Electrical Services | Electrical contracting / field-services firm; mid-size private | Data Analyst I | http://hayselectricalservices.applytojob.com/apply/gCUJCjoH7Z/Data-Analyst-I | ≈Jun 26 (speedy "9d") | Silent, small/mid — likely OK | **Explicit "I" entry + Houston, TX (in-state)**; clean Data-Analyst target with a small employer (low formal-immigration-policy risk); gap: ops/field-services analytics domain, not applied-AI | speedyapply Other |

### Tier 2 — Worth a look (net-new; caveat = seniority and/or visa unverified, JD 403/000)

| Company | What they do / size | Role | Direct link | Posted (basis) | Visa posture | Fit note | Source |
|---|---|---|---|---|---|---|---|
| Bank of America | Global bank; large public | Data Scientist I – Fraud Model Governance | https://ghr.wd1.myworkdayjobs.com/en-US/us-emplsv/job/Charlotte/Data-Scientist-I----Fraud-Model-Governance_26019387 | ≈Jun 10 (speedy "25d") | Silent, larger company — **verify** | **Explicit "I" entry** (distinct from prior BofA Client-Quant-Analyst-I / Associate-Quant rows); **fraud/anomaly modeling maps to candidate's anomaly-detection work**; Charlotte; gap: large-bank immigration policy | speedyapply Other |
| Traba | Labor-marketplace startup (light-industrial staffing); growth-stage | Software Engineer (Applied AI) | https://jobright.ai/jobs/info/6a427c0a6c326942b4e82ff3 | Jun 29 (jobright) | Silent, growth startup — likely OK | Applied-AI SWE at a fast-growing startup; NYC; ship-end-to-end fit; gap: SWE-leaning + seniority unverified | jobright ENG |
| Gravie | Health-benefits / insurance tech; growth-stage | Data Analyst | https://jobright.ai/jobs/info/6a2c1505fc06447490548170 | Jul 4 (jobright) | Silent, growth — likely OK | Data-Analyst target at a benefits-tech startup; Minneapolis; SQL/BI fit; gap: seniority unverified, benefits domain | jobright DA |
| University of Texas at Austin | Public R1 university; very large | Data Engineer I | https://utaustin.wd1.myworkdayjobs.com/UTstaff/job/AUSTIN-TX/Data-Engineer-I_R_00045134 | zapply "14m" first-seen (in 30-d window; recency = scraper stamp) | Likely OPT-friendly (universities are cap-exempt and routinely hire OPT) | **Explicit "I" entry + Austin, TX (in-state)**; dbt/SQL/ETL fit; gap: public-university IT domain; recency is a first-seen scraper stamp not a post date | zapplyjobs |
| GM Financial | Auto-finance arm of GM; large | Data Analyst 1 – Model Management | https://fa-exvu-saasfaprod1.fa.ocs.oraclecloud.com/hcmUI/CandidateExperience/en/sites/CX_1/job/2194 | zapply "14m" first-seen | Silent, larger company — **verify** | **Explicit "1" entry DA + "Model Management" (MLOps/model-governance-adjacent)**; Detroit; SQL/BI fit; gap: auto-finance domain, recency scraper stamp | zapplyjobs |
| Plaid | Fintech data-network / API platform; large private | Machine Learning Engineer (Payments Risk) | https://jobs.ashbyhq.com/plaid/50d40e3b-ed34-470d-b094-71e1555c6f1e/application | zapply "3d" first-seen | ✅ Sponsor (zapply) → likely OPT-OK, **verify** | MLE at a strong fintech; SF; applied-ML fit; gap: seniority unverified, payments-risk niche | zapplyjobs |
| Mercor | AI data-labeling / talent-matching startup; growth-stage | Machine Learning Engineer, Marketplace | https://jobs.ashbyhq.com/mercor/7cee578f-799c-46ad-8951-cb0b724d619a/application | zapply "4d" first-seen | Silent, growth startup — likely OK | MLE at a hot AI-data startup; SF; applied-ML fit; gap: seniority unverified | zapplyjobs |

### Tier 3 — Long shots / needs verification / seniority or domain risk (net-new)

| Company | What they do | Role | Direct link | Posted | Visa posture | Why Tier 3 | Source |
|---|---|---|---|---|---|---|---|
| Rocket Companies (Quicken Loans) | Mortgage / fintech; large public | Machine Learning Engineer | https://quickenloans.wd5.myworkdayjobs.com/rocket_careers/job/Detroit-MI/Machine-Learning-Engineer_R-081566 | Jun 30 (jobright) / zapply "5d" | Silent, larger company — **verify** | ML-Engineer fit but **no entry marker → likely mid+**; Detroit (distinct from prior "Rocket Companies DA II") | jobright ENG + zapplyjobs |
| Lincoln Financial | Life insurance / annuities; large public | Specialist, Actuarial Data Engineer | https://jobright.ai/jobs/info/6a0cd5f04d9320363687c925 | Jul 2 (jobright) | Silent, larger company — **verify** | DE stack fit; Charlotte; gap: **"Specialist" seniority unclear** + actuarial domain | jobright ENG |
| TSMC | Semiconductor foundry; large public | Data Engineer | https://jobright.ai/jobs/info/6a4628104f64ba41dcb50dc4 | Jul 2 (jobright) | Silent, larger company — **verify** | DE fit; San Jose; gap: seniority unverified, semiconductor domain | jobright ENG |
| UnitedHealth Group | Health insurer / Optum; large public (non-FAANG) | Data Engineer | https://jobright.ai/jobs/info/6a46c7cf0dd56c76cc2fadb9 | Jun 29 (jobright) | Silent, larger company — **verify** | DE fit; Eden Prairie MN; gap: seniority unverified, healthcare domain | jobright ENG |
| ETAP Software | Electrical power-systems simulation software; mid-size | Power Systems AI/ML Engineer | https://jobright.ai/jobs/info/6a2376c3dedf78312c7ac4d7 | Jun 29 (jobright) | Silent, mid-size — verify | AI/ML title; Irvine CA; gap: **power-grid-simulation niche far from LLM/RAG**, seniority unverified | jobright ENG |
| Costco Wholesale | Big-box retail; large public (non-FAANG) | Data Analyst – Asset Reporting | https://jobright.ai/jobs/info/6a0ba07f4d93203636872ec5 | Jul 1 (jobright) | Silent, larger company — **verify** | DA target title; Issaquah/Seattle WA; gap: asset-reporting niche + seniority unverified | jobright DA |
| Core Specialty Insurance | Specialty P&C insurer; mid-large | Actuarial Data Analyst | https://jobright.ai/jobs/info/69f3d8ec461b9b613a624616 | Jul 4 (jobright) | Silent, larger company — **verify** | DA fit; Cincinnati; gap: actuarial-insurance niche, seniority unverified | jobright DA |
| Blue River Technology (John Deere) | Ag-robotics / computer vision; mid-size | CVML Engineer, See & Spray | https://jobright.ai/jobs/info/6a3b202306a4fd4b1fac072c | Jul 4 (jobright) | Silent, larger-parent — **verify** | Applied-CV/ML at ag-robotics; Remote-US; gap: **computer-vision focus vs LLM/RAG**, seniority unverified | jobright ENG |
| Rivian | EV maker; large public | Durability Data Analytics Engineer | https://jobright.ai/jobs/info/6a1ac3f2c2a87d6cd3e012aa | Jul 4 (jobright) | Silent, larger company — **verify** | Analytics-Engineer-adjacent; Irvine CA; gap: vehicle-durability-testing niche, seniority unverified | jobright DA |
| XPENG | EV / robotics (China-HQ, US R&D); large | Machine Learning Engineer, Robotics | https://jobright.ai/jobs/info/66ce760fcd91241dd6020b99 | Jun 30 (jobright) | Unclear — **verify** | ML title; Santa Clara; gap: robotics focus, **China-HQ export/policy uncertainty**, seniority unverified | jobright ENG |
| JPMorgan Chase | Global bank; large public | Data Engineer (Multiple Positions) | https://jpmc.fa.oraclecloud.com/hcmUI/CandidateExperience/en/sites/CX_1/job/210762627 | zapply "5d" first-seen | 🏛 H-1B Co. (zapply) → likely OPT-OK, **verify** | DE at scale + **Plano, TX (in-state)**; dbt/SQL fit; gap: seniority unverified, big-bank policy, recency scraper stamp | zapplyjobs |
| Blueprint Technologies | Data / AI consultancy; mid-size | AI Engineer – Automation/Robotics | https://job-boards.greenhouse.io/bpcs/jobs/8037005 | zapply "5d" first-seen | ✅ Sponsor (zapply) → likely OPT-OK, **verify** | AI-Engineer title; Redmond WA; gap: consultancy (may staff client accounts) + automation/robotics focus, seniority unverified | zapplyjobs |

### Recency-unverified (net-new; zapply first-seen minute/hour stamp — NOT a confirmed post date; JD 403)
| Company | Role | Direct link | Note |
|---|---|---|---|
| Micron Technology | Product Yield & Analytics (PYAi) Engineer | https://micron.wd1.myworkdayjobs.com/external/job/Boise-ID---Main-Site/Product-Yield---Analytics-PYAi-Engineer_JR99163-1 | Boise ID; 🏛 H-1B Co.; "5d" first-seen; semiconductor-yield analytics; seniority unverified |
| Vanguard | Data Analyst, Specialist | https://vanguard.wd5.myworkdayjobs.com/vanguard_external/job/Charlotte-NC/Data-Analyst--Specialist_176118-1 | Charlotte NC; 🏛 H-1B Co.; "4d"; "Specialist" seniority unclear |
| Crane Co. | Salesforce Data Analyst | https://cranecompany.wd5.myworkdayjobs.com/Careers/job/The-Woodlands-Texas/Salesforce-Data-Analyst_JR102045 | The Woodlands, TX (in-state); "4d"; Salesforce-CRM niche; Crane is industrial (some defense components → verify) |
| Schweitzer Engineering Laboratories | Data Engineer | https://selinc.wd1.myworkdayjobs.com/SEL/job/Washington---Pullman/Data-Engineer_2026-20940-1 | Pullman WA; 🏛 H-1B Co.; "1h"; power-grid-protection (critical-infra); seniority unverified |
| Coca-Cola | Data Scientist | https://coke.wd1.myworkdayjobs.com/coca-cola-careers/job/US---GA---Atlanta/Data-Scientist_R-139580 | Atlanta GA; "4d"; large CPG; seniority unverified |
| Dell Technologies | Consultant, Machine Learning & Knowledge | https://iawmqy.fa.ocs.oraclecloud.com/hcmUI/CandidateExperience/en/sites/CX_1001/job/293104 | Round Rock, TX (in-state); 🏛 H-1B Co.; "3d"; "Consultant" seniority unclear |

### Community / informal leads (YC Work-at-a-Startup — real direct links; JD pages 403 → bodies unverified)
_All are YC seed/early startups → visa: silent, small startup (OPT needs no sponsorship, generally OK; tiny startups sometimes can't accommodate — verify). Open each to confirm entry-level + US-eligibility before applying. Net-new only (StackAI, Luminai, Automat, Amigo, Model ML, Firstbase, DeepAware, Karumi, AfterQuery, Confido, Artisan, SpruceID, FurtherAI, Soff already logged in prior runs)._
- **Zymbly** — Forward Deployed Engineer (AI-native OS for airline operations / maintenance). https://www.ycombinator.com/companies/zymbly/jobs/ueWPYCh-forward-deployed-engineer
- **Bretton AI** — Forward Deployed Engineer (deploy & integrate the platform directly with customers). https://www.ycombinator.com/companies/bretton-ai/jobs/E8Bd0s3-forward-deployed-engineer
- **Cekura** — Forward Deployed Engineer (**US**) (voice-AI testing/observability; customer-facing). https://www.ycombinator.com/companies/cekura-ai/jobs/AiWwUxI-forward-deployed-engineer-us
- **Puntt AI** — Forward Deployed Engineer ($190k + equity; enterprise marketing-compliance AI agents; Danone/Nestlé/Kenvue live; SF hybrid) — **seniority-unverified**; its companion Applied-AI role is *Senior/Founding* → excluded. Careers via Wellfound: https://wellfound.com/company/punttai/jobs (surfaced from HN thread submission `48398390`).
- **EXCLUDED (seniority/geo):** August Health (only open AI role = *Senior* SWE-AI, Ashby), Avallon AI (*Founding* FDE Solutions Eng), Arist (*Founding* FDE), telli (FDE-AI — **Germany**), Prior Labs (FDE-ML from HN — likely **EU/Freiburg**), Prolific (AI Solutions Eng — **UK**), Anthropic / Palantir (FDE Applied AI — senior/clearance high bar; Anthropic not FAANG-tier but role skews senior).

### Excluded (net-new sightings this run, logged so future runs don't re-surface)
- **FAANG-tier / near-FAANG (referral track):** Tesla (Software ML Engineer), Snap (MLE Causal Inference L5), Reddit (MLE), Adobe (MLE), Intel (MLE), Cisco (MLE), NVIDIA (Data Engineer Document-AI Finance; Applied ML Circuit-Design NCG), TikTok/ByteDance (many ML/DE/DS graduate + intern rows), Zoom (MLE / AI-Engineer-Agent / Video-AI — non-FAANG but seniority-unverified mid+).
- **Defense / federal / clearance / export-control / space:** Boeing (Full-Stack DS Seattle, Experienced DS Herndon), Axiom Space (Enterprise DE Houston), Nasdaq (Investigative DS/AI Eng DC — regulatory/investigative), Radiance Technologies (DA Huntsville), Eagle Harbor LLC (Jr DA — Alaska-Native gov contractor), AST (BI Analyst Tacoma — near JBLM, gov-adjacent), CapTech Consulting (ML/DS Eng + DE, VA — consultancy may staff gov/client accounts).
- **Trading-floor quant / PhD-research (profile wants non-trading-floor, applied not research):** D.E. Shaw (ML Researcher; Applied AI Engineer — quant high bar), IMC Trading (Graduate ML Researcher), State Street (ML Quantitative Research Analyst), ASML (Physics-Informed ML Scientist), Hitachi (ML/CV Research Scientist), InterDigital (Research Engineer/Scientist Wireless+AI/ML).
- **Senior / II+ / intern / co-op / clinical / public-sector / niche-QA:** PwC (CTIO AI Eng — Experienced Associate), Novaflow / Swif.ai / 14.ai / Fresco (Summer-2026 interns — weak timing for a May-2026 grad), John Deere (Part-Time Student DE), Kaiser Permanente (R/Python Programmer — clinical), Johnson & Johnson (DS + App Developer), Caterpillar (Python Dev/AI & Analytics Eng ×2, BI Analyst — seniority unverified), Symbotic (DA-Quality), Aptiv / RELX / Veolia / LG (QLIK/Meter/Material/Drug-content DA niches), Goldman Sachs (Compliance Assoc DE), Barclays (Compliance DS), JPMorgan (ML Center-of-Excellence — seniority unverified), Fiserv (10x Java/AI Eng), HPE (DS / Agentic-AI DS), plus Data-Analysis research/public-sector rows (Mass General Brigham, U-Rochester Advancement, Civic Nation, Sacramento Steps Forward, CA Correctional Health Care, Consumer Reports, Turning Point, Kroenke Sports contract).

### Bonus — adjacent titles worth adding to the search vocabulary
- **"Data Scientist I – Fraud Model Governance" (BofA) / "Data Analyst 1 – Model Management" (GM Financial)** — fraud/model-governance & model-management are **MLOps / anomaly-detection-adjacent** work hidden behind entry DS-I / DA-1 labels; add "model governance" / "model management" as search terms.
- **"Power Systems AI/ML Engineer" (ETAP) / "Durability Data Analytics Engineer" (Rivian) / "Product Yield & Analytics (PYAi) Engineer" (Micron)** — domain-specific "AI/Analytics Engineer" variants that a plain title search misses.
- **"CVML Engineer" (Blue River)** — computer-vision-ML variant of the ML-Engineer target.
- **YC "Forward Deployed Engineer" cluster keeps refilling** (Zymbly / Bretton AI / Cekura / Puntt this run) — `WebSearch` over `site:ycombinator.com/companies … jobs "Forward Deployed Engineer"` remains the single most productive community channel; run it every pass. The YC intern search (`"Machine Learning Engineer Intern Summer 2026"`) is NOT useful for a May-2026 grad.
- **TX geo net (in-state, worth prioritizing):** Hays Electrical (Houston), UT Austin (Austin), JPMorgan (Plano), Crane Co. (The Woodlands), Dell (Round Rock) surfaced this run.

### TODO for next (daily) run
- **CONCURRENCY:** backfills are landing on `main` within a day of each other (07-03, 07-04, 07-05).
  Always `git fetch origin main` and read the LATEST log before de-duping — one-day-apart 30-day
  backfills over the same sources are ~90% overlap, so expect a short net-new list and don't pad it.
- **Sources going stale:** speedyapply NEW_GRAD_USA is now 20–70d-dominated (low net-new). Lean on
  **zapply + jobright ENG** (jobright DA still caps at ~7 days). Keep curl + local Python parse.
- **HN July thread `48747976`** still 403 on every machine-read path (Algolia items / hnhiring /
  nchelluri). WebSearch-over-mirrors now surfaces company *names* but no per-post links — a readable
  path (or converting HN mentions to careers-page links via targeted WebSearch, as done this run for
  August Health / Puntt) is the highest-value unsolved community item. Reddit still hard-blocked.
- **JD/visa verification** unchanged #1 structural blocker: greenhouse/ashby/workday/oracle 403
  (WebFetch) / 000 (curl egress-denied). All visa buckets inferred; zapply's H-1B/Sponsor column is
  the only per-company signal.

---

---

## Run: 2026-07-06 17:20 (DEEP BACKFILL — 30 day window)

**THIS IS A ONE-TIME DEEP BACKFILL, NOT A DAILY PASS.** Run 2026-07-06, 30-day
window (~Jun 6 – Jul 6). Future daily runs should keep using 24h and treat everything
below as already-seen. Read `leads_log.md` in full first and de-duped against ALL ten
prior runs — **including the 07-03, 07-04 and 07-05 backfills, which used this same
30-day window and the same sources within days of this one.** As expected for
same-window one-day-apart passes, the large majority of what the trackers surfaced was
already logged; **only genuinely net-new leads (not in any prior run) appear below** — a
deliberately short, honest list rather than a padded one re-surfacing prior rows.

**Coverage summary (what was covered fully / partially / not at all):**
- **FULLY COVERED (curl'd raw markdown from `raw.githubusercontent.com`, all HTTP 200,
  parsed locally with Python — the proven method; NOT WebFetch):**
  - `speedyapply/2026-AI-College-Jobs` → `NEW_GRAD_USA.md` (78 KB, 232 target-parseable
    rows) — read in full. **Continuing to go stale** (age distribution dominated by
    10–110d rows; most in-window rows already logged). ~1 net-new after de-dup.
  - `zapplyjobs/New-Grad-Data-Science-Positions` (81 KB, 301 rows / 154 cos) — read in
    full; richest source. Carries a Visa column (`🏛 H-1B Co.` / `✅ Sponsor` / blank) =
    **company-level** sponsorship signal (generally OPT-friendly), NOT a per-JD guarantee.
    After target-title + entry + non-defense + non-FAANG + dedup filtering, nearly all
    remaining rows were defense/federal, senior, co-op, or already logged.
  - `jobright-ai/2026-Engineering-New-Grad` (1.55 MB, 6283 rows) — read in full;
    calendar-dated. In-window target rows span **Jun 30 – Jul 06**.
  - `jobright-ai/2026-Data-Analysis-New-Grad` (60 KB, 254 rows) — read in full, still
    **caps at "last ~7 days" (Jun 29 – Jul 06)** per its capacity constraint; 30-day depth
    unavailable (same cap every prior run).
  - `jobright-ai/2026-Business-Analyst-New-Grad` (15 KB, 53 rows) — read in full; no
    net-new in-window target rows after dedup.
- **PARTIALLY COVERED (WebSearch works; underlying JD pages 403 so bodies/seniority
  UNVERIFIED):**
  - **YC Work-at-a-Startup** — `WebSearch` over `site:ycombinator.com/companies … jobs`
    returned real direct `ycombinator.com/companies/.../jobs/` URLs (the one reliable
    community channel). Net-new FDE + Applied-AI cluster logged in the Community section.
    JD pages themselves 403, so seniority / exact post date / visa language are UNVERIFIED.
- **NOT COVERED / BLOCKED (unchanged structural blockers, re-confirmed this run):**
  - **Individual JD verification — ALL still blocked.** `curl` to greenhouse/ashby/
    workday/oracle/rippling/smartrecruiters = **HTTP 000 (CONNECT tunnel 403, egress
    policy)**; prior runs' `WebFetch` to the same = 403. **No JD body read** → EVERY visa
    bucket below is inferred from company type + role (+ zapply's H-1B column where
    present), NOT JD text. Every "verify" must be opened manually. Seniority for any role
    not explicitly labeled entry/junior/associate/"I"/"1"/new-grad is **unverified** and
    flagged inline.
  - **HN "Ask HN: Who is hiring? (July 2026)" thread `48747976` — LIVE but every
    machine-read path 403'd AGAIN** (re-tested this run): `hn.algolia.com/api/v1/items/
    48747976` = **000/403**, `hn.algolia.com/api/v1/search` = **000/403**,
    `nchelluri.github.io/hnjobs/` = **000/403**. Same blocker as every prior run. Nothing
    from HN logged. Remains the #1 un-mined community gap.
  - **Reddit / Discord / Slack** — not machine-readable (hard-blocked every prior run). No
    active datable "who's hiring" thread surfaced with per-post links.
  - **LinkedIn / Indeed / Glassdoor / Wellfound / Built In** — only aggregator landing
    pages, no per-posting dates or stable direct links → nothing logged. No founder/
    recruiter post with a stable direct link surfaced this run.
- **Recency basis:** jobright rows = calendar dates (Jun 30 – Jul 06, used directly).
  speedyapply = "age" field vs the Jul-6 refresh. **zapplyjobs day-stamps ("3d"–"6d") are
  scraper FIRST-SEEN stamps, NOT confirmed post dates** — but for a 30-DAY window even a
  "6d first-seen" comfortably falls inside the window, so zapply day-stamped net-new rows
  are tiered here with the first-seen caveat noted.
- **De-duped OUT as already logged** (surfaced again this run, NOT repeated below): Gen
  Digital (MLE I), CNN (MLE I — Atlanta variant of the NYC role logged 07-04), Rocket
  Companies (MLE Detroit — logged 07-05), BD (Commercial Analytics Eng — new jobright id,
  same role logged 07-04), Core Specialty (Actuarial DA — Chicago variant of Cincinnati
  role logged 07-05), Pacific Medical Centers / Providence (Assoc BI Analyst), WaFd Bank
  (BI Analyst — logged 07-05), JPMorgan (DE Plano — same oracle link logged 07-05), HPE
  (DS — sighted/excluded 07-04 & 07-05; see note in Tier 3), AST (BI Analyst Tacoma —
  excluded 07-05).

### Tier 1 — Hot & strong fit (net-new)
_Entry-labeled + on-target-title + in-window + commercial (non-defense, non-FAANG). Visa inferred (JDs all 403/000)._

| Company | What they do / size | Role | Direct link | Posted (basis) | Visa posture | Fit note | Source |
|---|---|---|---|---|---|---|---|
| Navistar (International Motors) | Commercial trucks / engines / buses manufacturer; large (~13k, TRATON/VW group), non-FAANG | Junior AI/ML Engineer | https://jobright.ai/jobs/info/6a4bb193c2d11a6a4667848d | Jul 06 (0d) | Silent, larger company — **verify** | **Explicit "Junior" + AI/ML-Engineer target title**, Lisle IL, commercial (non-defense); applied-ML at an industrial manufacturer maps to candidate's ship-real-systems profile; gap: automotive/manufacturing domain + large-co immigration policy unread | jobright ENG |
| Adelaide (Adelaide Metrics) | Attention-measurement ad-tech ("AU" metric; ~40% of Fortune-50 brands); growth-stage startup | Associate Data Scientist (Attention Metrics & Ad Tech, Remote US) | jobright: https://jobright.ai/jobs/info/6a4bbc804f64ba41dcb5cec5 · **direct ATS**: https://ats.rippling.com/adelaide/jobs/92517973-affd-4dfb-9536-3d1d200e898c | Jul 06 (0d) | Silent, growth startup — likely OK | **Remote-US + "Associate" DS** at an AI/measurement startup; JD = "train/iterate models, improve codebase & pipelines over hundreds of millions of data points/day" = squarely applied-DS/ML fit; gap: ATS title reads plain "Data Scientist" (seniority slightly ambiguous), ad-tech domain | jobright DA + company ATS |

### Tier 2 — Worth a look (net-new; caveat = seniority and/or visa unverified, JD 403/000)

| Company | What they do / size | Role | Direct link | Posted (basis) | Visa posture | Fit note | Source |
|---|---|---|---|---|---|---|---|
| iHeartMedia | Broadcast radio / digital audio media; large public (non-FAANG) | Digital Data Analyst | San Antonio TX: https://jobright.ai/jobs/info/6a0b739c963f7a67d95cfe23 · NYC: https://jobright.ai/jobs/info/6a0b739b963f7a67d95cfe20 | Jul 02 (4d) | Silent, larger company — **verify** | **San Antonio, TX = in-state option**; DA target title; media/digital-analytics fit (SQL/BI); gap: no explicit entry marker → seniority unverified, media domain | jobright DA |
| A.P. Moller – Maersk | Global shipping / logistics; very large (non-FAANG) | Data Analyst | https://jobright.ai/jobs/info/6a470671971cd25b06f910b7 | Jul 02 (4d) | Silent, larger company — **verify** | DA target at a global logistics leader; Hopedale MA; SQL/BI + supply-chain-analytics fit; gap: seniority unverified, large-co policy | jobright DA |
| Fanatics | Sports-merchandise / licensed-goods e-commerce; large growth-stage (private, ~$30B val) | Data Scientist | https://jobright.ai/jobs/info/6a4b2d715d7b097d2df3cd5a | Jun 30 (6d) | Silent, larger/growth — **verify** | DS target at a fast-scaling commerce co; NYC; analytics/ML fit; gap: seniority unverified (no entry marker) | jobright DA |
| Gallup | Analytics / polling / workplace-consulting firm; mid-large private | Data Analyst | https://jobright.ai/jobs/info/6a4ab8cb3dbab558e29af3f0 | Jul 05 (1d) | Silent, mid-large — **verify** | DA target at a data-first research firm (people-analytics-adjacent — on the profile's target list); Omaha NE; SQL/BI/statistics fit; gap: seniority unverified | jobright DA |
| UST | IT services / digital-transformation firm; large | Associate Data Engineer | https://jobright.ai/jobs/info/6a444ca065e80d3c99f2c553 | Jul 04 (2d) | Silent, larger company — **verify** | **Explicit "Associate" DE + Frisco, TX (in-state)**; dbt/SQL/Airflow fit; **CAVEAT: UST DE variants (UST HealthProof / CyberProof Assoc DE) were logged in prior runs — this Frisco role has a distinct jobright id but may be the same req; verify it isn't a repeat before spending effort** | jobright ENG |

### Tier 3 — Long shots / needs verification / seniority or domain risk (net-new)

| Company | What they do | Role | Direct link | Posted | Visa posture | Why Tier 3 | Source |
|---|---|---|---|---|---|---|---|
| BMO (Bank of Montreal) | Commercial/retail bank (Canadian parent, US role); large | Data Engineer | https://bmo.wd3.myworkdayjobs.com/External/job/Chicago-IL-USA/Data-Engineer_R260019331 | zapply "3d" first-seen (≈Jul 3) | Silent, larger company — **verify** | DE stack fit; Chicago IL; gap: **no entry marker → seniority unverified**, big-bank immigration policy, recency is a scraper stamp | zapplyjobs |
| HPE (Hewlett Packard Enterprise) | Enterprise IT / hybrid-cloud / servers; large public (non-FAANG) | Data Scientist | https://hpe.wd5.myworkdayjobs.com/Jobsathpe/job/Spring-Texas-United-States-of-America/Data-Scientist_1207756-1 | zapply "4d" first-seen (≈Jul 2) | 🏛 H-1B Co. (zapply) → likely OPT-OK, **verify** | DS at scale + **Spring, TX (in-state)**; **CAVEAT: HPE DS was already sighted/excluded in the 07-04 & 07-05 runs — logged here only because it's an in-state TX option with a concrete link; likely not truly net-new**, seniority unverified | zapplyjobs |
| Thumbtack | Home-services marketplace; large growth-stage | Software Engineer, AI/ML Infrastructure (US-Based) | https://jobright.ai/jobs/info/6a0612556c07461fe171bec8 | Jul 05 (1d) | Silent, larger company — **verify** | AI/ML-infra SWE, Remote-US (distinct from the Remote-**Ontario** Thumbtack role excluded 07-04); gap: **no entry marker → likely mid+**, SWE/infra-leaning vs applied-GenAI | jobright ENG |
| Langan Engineering & Environmental Services | Civil/environmental engineering consultancy; mid-large | Environmental Data Analyst | https://jobright.ai/jobs/info/6a0d99e483d714428981101d | Jul 02 (4d) | Silent, larger company — **verify** | DA target title; NYC; SQL/BI fit; gap: environmental-data niche far from AI/RAG, seniority unverified | jobright ENG |
| Capstone Energy+ | Energy / power services; mid-size | Data Analyst | https://jobright.ai/jobs/info/6a35e4e8ce501060b5cf5fea | Jul 03 (3d) | Silent, mid-size — verify | DA target; Van Nuys CA; SQL/BI fit; gap: energy-ops niche, seniority unverified | jobright DA |
| Gotion Inc. | EV-battery manufacturer (China-linked parent, US plant); mid-large | Data Analyst | https://jobright.ai/jobs/info/6a273dc3ca77fd3096d2648d | Jul 03 (3d) | Unclear — **verify** | DA target; Manteno IL; gap: **China-parent → export/policy uncertainty**, manufacturing domain, seniority unverified | jobright DA |
| MRM (McCann/IPG) | Marketing / CRM agency; large (holding-co subsidiary) | Data Analyst | https://jobright.ai/jobs/info/6a297791d3ec8317fe13e24a | Jul 02 (4d) | Silent, larger company — **verify** | DA target; NYC; marketing-analytics fit; gap: agency (may staff client accounts), seniority unverified | jobright DA |
| Ascend Schools | K-12 charter-school network; mid-size nonprofit-adjacent | Data Analyst | https://jobright.ai/jobs/info/6a4b9814971cd25b06f97b81 | Jul 06 (0d) | Silent, mid-size — verify | DA target; Brooklyn NY; SQL/BI fit; gap: education domain, seniority unverified | jobright DA |
| AgileGrid Solutions | Small/opaque IT-services co; small | Data Scientist | https://jobright.ai/jobs/info/6a4baebf5d7b097d2df3dc0a | Jul 06 (0d) | Unclear — **verify** | DS title at an opaque small vendor, US-remote; **verify legitimacy/scope before effort** (staffing-shop risk) | jobright ENG |

### Community / informal leads (YC Work-at-a-Startup — real direct links; JD pages 403 → seniority/visa UNVERIFIED)
_All are YC seed/early startups → visa: silent, small startup (OPT needs no sponsorship, generally OK; tiny startups sometimes can't accommodate — verify). Open each to confirm entry-level + US-eligibility before applying. Net-new only (StackAI, Luminai, Automat, Amigo, Model ML, Firstbase, DeepAware, Karumi, AfterQuery, Confido, Artisan, SpruceID, FurtherAI, Soff, Zymbly, Bretton AI, Cekura, Puntt already logged in prior runs)._
- **Maywood** — Applied AI Engineer (LLMs + intelligent agents for **code delivery / testing / deployment**). https://www.ycombinator.com/companies/maywood/jobs/DV7GBKh-applied-ai-engineer — **strongest community fit this run: directly maps to the candidate's fine-tuned code-review LLM flagship.** Seniority unverified.
- **HackerRank** — Forward Deployed Engineer (onsite customer-facing technical lead on engagements). https://www.ycombinator.com/companies/hackerrank/jobs/PUBbnNs-forward-deployed-engineer — established co; FDE target title; seniority unverified.
- **Nixo** — Forward Deployed Engineer (early AI startup). https://www.ycombinator.com/companies/nixo/jobs/nI0YNNA-forward-deployed-engineer — seniority unverified.
- **Aravolta** — Forward Deployed Engineer (customer-facing in complex **data-center** environments). https://www.ycombinator.com/companies/aravolta/jobs/F5owCzV-forward-deployed-engineer — seniority unverified.
- **Terrakotta** — Forward Deployed Engineer. https://www.ycombinator.com/companies/terrakotta/jobs/Wh899KZ-forward-deployed-engineer — seniority unverified.
- **EXCLUDED (seniority/geo/intern):** Retell AI (*Senior* FDE), Operon (*Founding* FDE), Saphira AI (*Founding* Applied-AI Eng), Weave (*Founding* AI Eng), Peakflo (FDE — **India/Remote**), Crustdata / Paragon / Dex / Great Question (Summer-2026 **interns** — weak timing for a May-2026 grad).

### Recency note
All tiered jobright rows carry calendar post dates (Jun 30 – Jul 06), comfortably inside the 30-day window. BMO/HPE carry zapply first-seen day-stamps (3–4d), also inside window but the stamp is scraper-first-seen, not a confirmed post date (flagged inline). No separate "Recency unverified" section needed this run — every net-new tiered lead is datable within the window.

### Excluded (net-new sightings this run, logged so future runs don't re-surface)
- **Defense / federal / clearance / space (US-person near-certain):** Clarity Innovations (DS Fort Bragg, DA MacDill AFB), Guidehouse (DS Arlington + DS Huntsville), Boeing (Full-Stack DS Seattle, Experienced DS Herndon), Noblis (DA Network Security, Atlantic City), Systems Planning & Analysis (Jr DS Alexandria), Eagle Harbor LLC (Jr DA — gov contractor), PLATEAU GRP (BI Analyst Assoc, Virginia Beach), Axiom Space (Enterprise DE, Houston — space).
- **FAANG-adjacent / large already-seen / senior:** Intel (MLE Santa Clara — seen prior runs), Cisco (MLE Seattle — seen prior runs), PwC (CTIO AI Eng — *Experienced Associate* = senior), Royal Bank of Canada (AI Engineer I NYC — RBC logged prior), Milwaukee Tool (MLE I — but 112d, outside window).
- **Trading-floor quant / high-bar research (profile wants non-trading-floor, applied not research):** D. E. Shaw (Applied AI Engineer — quant high bar), Brookhaven National Laboratory (Postdoc AI/ML), Senseye/Siemens (Research Data Analyst).
- **Non-US geography (F-1 OPT is US-only):** Baker Hughes (AI Engineer — Haryana, India), Canadian Chamber of Commerce (DS — Ottawa), Peakflo (FDE — India), TensorOps (Jr AI/ML — EU greenhouse).
- **Co-op / intern / clinical / public-sector / niche-QA:** Campbell Soup (DE Co-op + DE Agentic-AI/ML-Ops Co-op — both explicitly co-op), Volvo Group (BI — "Fall 2026" program), Beth Israel Lahey (Healthcare DA — clinical/OBGYN), Penn State (DS Hawaii — student-jobs board), Corning (QA DA), Aptiv (QLIK/Quality DA), RELX (Drug-Product-Content DA), Symbotic (DA-Quality), LG Electronics (Material DA), Veolia (Meter DA + DE), CapTech (DE AWS/Azure/GCP — consultancy may staff client accounts), plus DA public-sector/nonprofit rows (California Correctional Health Care, Sacramento Steps Forward, Civic Nation, Consumer Reports [limited-duration], Turning Point Community Programs, University of Rochester Advancement, Kroenke Sports [DS contract], Joslin Diabetes [DA — clinical], OneRail, Blackstone [DA-Associate PE/RE Tech — large PE, seniority unverified]).

### Bonus — adjacent titles worth adding to the search vocabulary
- **"Junior AI/ML Engineer" at heavy-industry manufacturers (Navistar/International)** — applied-ML behind an explicit entry title at a commercial (non-defense) industrial employer; a plain "AI Engineer" search misses the "AI/ML Engineer" hyphenated variant.
- **"Digital Data Analyst" (iHeartMedia)** — media-analytics DA variant, often entry-level, that a bare "Data Analyst" search still catches but the "Digital" qualifier signals ad/audience-analytics.
- **Maywood's "Applied AI Engineer" for code-delivery/testing agents** — the single best community match to the candidate's fine-tuned **code-review LLM** flagship; worth prioritizing.
- **TX in-state net this run:** Navistar (Lisle IL — not TX, Midwest), iHeartMedia (San Antonio), UST (Frisco), HPE (Spring). San Antonio + Frisco + Spring are all Texas-metro options.

### TODO for next (daily) run
- **CONCURRENCY:** backfills continue landing on `main` within a day of each other (07-03 → 07-06). Always `git fetch origin main` and read the LATEST log before de-duping — same-window one-day-apart passes over the same sources are ~90% overlap; expect a short net-new list and don't pad it.
- **Sources going stale:** speedyapply NEW_GRAD_USA is now 10–110d-dominated (near-zero net-new). Lean on **zapply + jobright ENG** (jobright DA still caps at ~7 days; jobright BA thin). Keep curl + local Python parse, NOT WebFetch, for the trackers (worked again, all HTTP 200).
- **HN July thread `48747976`** still 403/000 on every machine-read path (Algolia items/search, nchelluri mirror) — re-confirmed this run. Highest-value unsolved community item; converting HN company *names* to careers-page links via targeted WebSearch remains the only workaround. Reddit/Discord still hard-blocked.
- **JD/visa verification** unchanged #1 structural blocker: greenhouse/ashby/workday/oracle/rippling/smartrecruiters = 403 (WebFetch) / 000 (curl egress-denied). All visa buckets inferred; zapply's H-1B/Sponsor column is the only per-company signal.
- **YC `site:ycombinator.com/companies … "Forward Deployed Engineer" / "Applied AI Engineer"`** remains the single most productive community channel — run both queries every pass. The FDE cluster keeps refilling (Maywood/HackerRank/Nixo/Aravolta/Terrakotta net-new this run).

---

## Run: 2026-07-07 17:06 (DEEP BACKFILL — 30 day window)

**THIS IS A ONE-TIME DEEP BACKFILL, NOT A DAILY PASS.** Run 2026-07-07, 30-day
window (~Jun 7 – Jul 7). Future daily runs should keep using 24h and treat
everything below as already-seen. Read `leads_log.md` in full first and de-duped
against ALL eleven prior runs — **including the 07-03 → 07-06 backfills, which
used this same 30-day window and the same sources within days of this one.** As
expected for same-window one-day-apart passes, the large majority of what the
trackers surfaced was already logged; **only genuinely net-new leads (not in any
prior run) appear below** — a deliberately short, honest list, not a padded one.

**Coverage summary (fully / partially / not at all):**
- **FULLY COVERED (curl'd raw markdown from `raw.githubusercontent.com`, all HTTP
  200, parsed locally with Python — the proven method; NOT WebFetch):**
  - `speedyapply/2026-AI-College-Jobs` → `NEW_GRAD_USA.md` (78 KB) — read in full.
    **Now effectively dead for net-new:** only **5** in-window (≤30d) target-title
    rows survived parsing and **all 5 were already logged/excluded → 0 net-new.**
    Age distribution is 20–110d-dominated. Recommend demoting to a spot-check.
  - `zapplyjobs/New-Grad-Data-Science-Positions` (80 KB, 296 parseable rows) —
    read in full; richest source again. Carries a Visa column (`🏛 H-1B Co.` /
    `✅ Sponsor` / blank) = **company-level** sponsorship signal (generally
    OPT-friendly), NOT a per-JD guarantee. 21 net-new-by-company after target +
    non-senior + non-defense + non-FAANG filtering; 6 tiered + 2 intern/co-op
    after manual review (rest were senior-II/trading-floor/gov/co-op/already-logged).
  - `jobright-ai/2026-Engineering-New-Grad` (1.50 MB, 6371 rows across ENG+DA+BA
    parsed) — read in full; calendar-dated. In-window target rows span **Jul 01
    – Jul 07**.
  - `jobright-ai/2026-Data-Analysis-New-Grad` (60 KB) — read in full, still
    **caps at "last ~7 days" (Jun 30 – Jul 07)** per its capacity constraint;
    30-day depth unavailable (same cap every prior run).
  - `jobright-ai/2026-Business-Analyst-New-Grad` (16 KB) — read in full; no
    net-new in-window target rows after dedup.
- **PARTIALLY COVERED (WebSearch works; underlying JD pages 403 → bodies /
  seniority / exact post date / visa language UNVERIFIED):**
  - **YC Work-at-a-Startup** — `WebSearch` over `site:ycombinator.com/companies …
    "Forward Deployed Engineer"` and `… "Applied AI Engineer"` returned real
    direct `ycombinator.com/companies/.../jobs/` URLs (the one reliable community
    channel). Net-new FDE + Applied-AI cluster logged in the Community section.
- **NOT COVERED / BLOCKED (unchanged structural blockers, re-confirmed this run):**
  - **Individual JD verification — ALL still blocked.** `curl` to greenhouse /
    ashby / workday / oracle / smartrecruiters / jobright = **HTTP 000 (egress
    tunnel denied)**; `WebFetch` to the same = **403**. **No JD body read** →
    EVERY visa bucket below is inferred from company type + role (+ zapply's H-1B
    column where present), NOT JD text. Every "verify" must be opened manually.
    Seniority for any role not explicitly labeled entry/junior/associate/"I"/"1"/
    new-grad is **unverified** and flagged inline.
  - **HN "Ask HN: Who is hiring? (July 2026)" thread `48747976` — LIVE but every
    machine-read path blocked AGAIN** (re-tested this run): `hn.algolia.com/api/v1/
    items/48747976` = **000 (curl) / 403 (WebFetch)**; `hn.algolia.com/api/v1/
    search` = **000**; `hnhiring.com/search` = **403**; `nchelluri.github.io/hnjobs`
    surfaced via WebSearch but not machine-readable. WebSearch-over-mirrors returned
    only **anonymous email-application FDE posts** (e.g. `mercedes@kinxshn.com`,
    `k@lunt.co`) with **no stable per-post direct links and no clear entry-level
    signal** → nothing loggable from HN. Remains the #1 un-mined community gap.
  - **Reddit / Discord / Slack** — not machine-readable (hard-blocked every prior
    run). No active datable "who's hiring" thread surfaced with per-post links.
  - **LinkedIn / Indeed / Glassdoor / Wellfound / Built In** — only aggregator
    landing pages, no per-posting dates or stable direct links → nothing logged.
    No founder/recruiter post with a stable direct link surfaced this run.
- **Recency basis:** jobright rows = calendar dates (Jul 01 – Jul 07, used
  directly). speedyapply = "age" field (all in-window rows already logged).
  **zapplyjobs minute/hour/day stamps ("13m","20h","5d") are scraper FIRST-SEEN
  stamps, NOT confirmed post dates** — but for a 30-DAY window even a "6d
  first-seen" comfortably falls inside the window, so zapply day-stamped net-new
  rows are tiered here with the first-seen caveat noted. YC community rows have
  **no verifiable post date** (JD 403) → flagged recency-unverified.
- **De-duped OUT as already logged** (surfaced again this run, NOT repeated
  below): UST HealthProof (Assoc DE), Novartis (Scientific DE), SEL (Assoc SWE
  AI/ML), Capgemini (Jr DE ×3), NewsBreak (Applied AI Eng), Tata Consultancy (Jr
  DE), Unity (MLE ×2), CNN (MLE I — Atlanta), Together AI (Analytics Eng),
  MeritFirst (AI Eng ×2), AssetMark (Assoc DE), Lincoln Financial (Actuarial DE),
  iFIT (Jr Salesforce AI Eng), PayPal (MLE ×2 — Austin), Phenom (Assoc DE), XiFin
  (Assoc MLE), AMIGO (Applied AI Eng), Ludo Robotics (ML/AI Eng), BD (Commercial
  Analytics Eng), HPE (DS — Spring TX; incl. zapply "HPE University" dup), Esri
  (DS I), Quantifind (Assoc DS ×3), Rivian (Durability Analytics Eng), Civic
  Nation, CharterUP, MRM, Kroenke Sports, Veolia (Meter DA / DE), Costco (DA
  Asset Reporting), Harris (Facility DA), Turning Point (DA I), Core Specialty
  (Actuarial DA — Chicago variant logged 07-06).

### Tier 1 — Hot & strong fit (net-new)
_None this run clear the full bar (explicit-entry + on-target-title + in-window +
low-visa-risk + strong applied-AI fit + non-gov/non-niche). The genuinely
entry-labeled net-new rows are all Data-Analyst/DE at niche or public-sector
employers (Tier 2/3); the strongest applied-AI matches are YC startups with
unverified seniority (Community). Honest result of an 11th same-window pass — the
high-fit rows have all been logged in prior backfills._

### Tier 2 — Worth a look (net-new; caveat = seniority and/or visa unverified, JD 403/000)

| Company | What they do / size | Role | Direct link | Posted (basis) | Visa posture | Fit note | Source |
|---|---|---|---|---|---|---|---|
| Raymond James Financial | Wealth-management / financial-services firm; large public (non-FAANG, non-trading-floor) | People Analytics Analyst – Qlik Sense (Remote) | https://raymondjames.wd1.myworkdayjobs.com/RaymondJamesCareers/job/Remote-Illinois---United-States/People-Analytics-Analyst---Qlik-Sense_R-0011894 | zapply "40m" first-seen (in-window; scraper stamp) | Silent, larger company — **verify** | **"People Analytics Analyst" = exact target-list title + Remote**; SQL/BI/Qlik fit; HR-analytics is on the profile's target list; gap: seniority unverified, Qlik-specific | zapplyjobs |
| Hinge Health | Digital MSK / physical-therapy health platform; large growth-stage (public) | Data Analyst (Remote US) | https://jobs.ashbyhq.com/hinge-health/7cc944a7-d01b-4700-a744-6ad846fcb966/application | zapply "20h" first-seen | ✅ Sponsor (zapply) → likely OPT-OK, **verify** | **Remote-US DA at a health-tech co that sponsors**; SQL/BI + product-analytics fit; gap: seniority unverified, healthcare domain | zapplyjobs |
| Workday, Inc. | HR / finance enterprise SaaS; large public (non-FAANG) | People Analytics Analyst | https://workday.wd5.myworkdayjobs.com/Workday/job/USA-CA-Pleasanton/People-Analytics-Analyst_JR-0108449-1 | zapply "1d" first-seen | 🏛 H-1B Co. (zapply) → likely OPT-OK, **verify** | **"People Analytics Analyst" target-list title** at an HR-software leader (people-analytics is exactly their product domain); Pleasanton CA; SQL/BI fit; gap: seniority unverified | zapplyjobs |
| Fidelity Investments | Financial-services / asset management; very large private (non-FAANG) | Data Engineer | https://fmr.wd1.myworkdayjobs.com/fidelitycareers/job/Westlake-TX/Data-Engineer_2124554-1 | zapply "27m" first-seen | 🏛 H-1B Co. (zapply) → likely OPT-OK, **verify** | **Westlake, TX = in-state (DFW-metro)**; dbt/SQL/Airflow DE fit at a large sponsor; gap: no entry marker → seniority unverified, big-finance policy | zapplyjobs |
| Bloomerang | Nonprofit donor-management / fundraising CRM SaaS; mid-size (Indianapolis) | Associate Conversion Data Analyst (Remote US) | https://jobright.ai/jobs/info/6a4c607a6189f64e437f1dab | Jul 06 (jobright) | Silent, mid-size — likely OK | **Explicit "Associate" + Remote-US**; conversion/growth-analytics DA; SQL/BI fit; small-mid co = lower formal-immigration-policy risk; gap: SaaS-growth-analytics niche, not applied-AI | jobright DA |
| PrizePicks | Daily-fantasy-sports / gaming platform; growth-stage private | Data Engineer (Atlanta / Remote) | https://jobright.ai/jobs/info/6a4bd26dc2d11a6a46678cf8 | Jul 06 (jobright) | Silent, growth-stage — likely OK | DE at a fast-scaling consumer-gaming co; Atlanta-pref/Remote; dbt/SQL/Airflow fit; gap: no entry marker → seniority unverified | jobright ENG |
| Louisiana Economic Development | State economic-development agency (delivery / "Client Innovation Center"); public-sector | Associate Data Engineer – Client Innovation Center (Entry Level) | https://jobright.ai/jobs/info/6a4d13e10209ea6fd6850c04 | Jul 07 (jobright) | Silent, public-sector — **verify** (state agency may prefer work-auth w/o sponsorship) | **Explicit "Associate" + "Entry Level"**; Baton Rouge LA; DE stack fit; gap: state-government/delivery-center domain, public-sector roles sometimes restrict to citizens/PR — verify eligibility before effort | jobright ENG |

### Tier 3 — Long shots / needs verification / seniority or domain risk (net-new)

| Company | What they do | Role | Direct link | Posted | Visa posture | Why Tier 3 | Source |
|---|---|---|---|---|---|---|---|
| Danaher | Life-sciences / diagnostics conglomerate; very large public (non-FAANG) | Data Analyst, Global Trade Compliance | https://jobright.ai/jobs/info/6a4cfdf235e45603c4bb21f3 | Jul 07 (jobright) | Silent, larger company — **verify** | DA target title; Washington DC; SQL/BI fit; gap: trade-compliance niche + no entry marker → seniority unverified + large-co policy | jobright DA |
| Hologic | Medical-device / women's-health diagnostics; large public | Business Intelligence Development Analyst | https://ebwb.fa.us2.oraclecloud.com/hcmUI/CandidateExperience/en/sites/CX/job/11925 | zapply "17h" first-seen | 🏛 H-1B Co. (zapply) → likely OPT-OK, **verify** | **BI target title** (BI-Developer variant); Marlborough MA; SQL/BI fit; gap: med-device domain, seniority unverified | zapplyjobs |
| Bloom Energy | Clean-energy / solid-oxide fuel-cell manufacturer; large public | Equipment Maintenance Data Analyst | https://bloomenergy.wd1.myworkdayjobs.com/bloomenergycareers/job/Fremont-California/Equipment-Maintenance-Data-Analyst_JR-23323 | zapply "1d" first-seen | 🏛 H-1B Co. (zapply) → likely OPT-OK, **verify** | DA target title; Fremont CA; SQL/BI fit; gap: equipment-maintenance-ops niche (far from AI/RAG), seniority unverified | zapplyjobs |
| SCS Engineers | Environmental consulting / engineering firm; mid-large | Data Analyst | https://jobright.ai/jobs/info/6a4c16876189f64e437f114a | Jul 06 (jobright) | Silent, mid-large — verify | DA target; Atlanta GA; SQL/BI fit; gap: environmental-consulting niche far from applied-AI, seniority unverified | jobright DA |
| Petco | Pet-retail / Petco Love foundation arm; large public | Data Analyst (Petco Love) | https://jobright.ai/jobs/info/6a4c18914f64ba41dcb5e81e | Jul 06 (jobright) | Silent, larger company — verify | DA target; San Diego CA; SQL/BI fit; gap: nonprofit-foundation/retail niche, seniority unverified | jobright DA |
| Liberty University | Private Christian university; large (education) | Business Data Analyst I | https://jobright.ai/jobs/info/6a4c2f8b6189f64e437f1759 | Jul 06 (jobright) | Likely OPT-friendly (universities are cap-exempt & routinely hire OPT), **verify** | **Explicit "I" entry**; Lynchburg VA; SQL/BI fit; gap: higher-ed-IT domain (may have faith-statement/residency preferences — verify) | jobright DA |
| St. Louis County, MN | County government; public-sector | Data Analyst | https://jobright.ai/jobs/info/6a4d0bdac643fd23fed3b67e | Jul 06 (jobright) | **Likely restricted** — county-government roles commonly require citizenship/PR + residency | DA target; Duluth MN; SQL/BI fit but **public-sector work-auth restriction very plausible** → confirm F-1-OPT eligibility before any effort | jobright DA |
| McCorquodale Transfer, LLC | Small moving / relocation-logistics company; small | Data Analyst (100% onsite, no remote) | https://jobright.ai/jobs/info/6a3962fa6484fb75f2b312f5 | Jul 06 (jobright) | Silent, small — likely OK | DA target at a small logistics co; **onsite-only West Palm Beach FL** (no remote / relocation required); SQL/BI fit; gap: tiny employer, onsite-only, small-shop-analytics scope | jobright DA |

### Intern / Co-op (in-scope per this run's brief, but timing-flagged for a May-2026 grad → OPT starts Jul 13 2026)
_Prompt lists Intern/Contract as in-scope. These are the only net-new intern rows that aren't co-ops at already-logged employers. A **Fall-2026 internship conflicts with a new-grad FTE search** and would consume OPT time on an intern rung — listed for completeness, not recommended over FTE._

| Company | Role | Direct link | Posted | Visa | Note |
|---|---|---|---|---|---|
| Cloudflare | Data Engineer Intern (Fall 2026) | https://boards.greenhouse.io/cloudflare/jobs/8047201?gh_jid=8047201 | zapply "20h" first-seen | ✅ Sponsor | **Austin, TX (in-state)** + strong infra co; but Fall-2026 intern timing is off for a May-2026 grad on OPT |
| Eurofins | Business Intelligence Intern | https://jobs.smartrecruiters.com/Eurofins/744000131132249 | zapply "4w" first-seen | 🏛 H-1B Co. | Lancaster PA; bio-testing lab; intern rung + niche |

### Community / informal leads (YC Work-at-a-Startup — real direct links; JD pages 403 → seniority/visa/post-date UNVERIFIED)
_All are YC seed/early startups → visa: silent, small startup (OPT needs no sponsorship, generally OK; tiny startups sometimes can't accommodate — verify). Open each to confirm entry-level + US-eligibility before applying. Net-new only (StackAI, Luminai, Automat, Amigo, Model ML, Firstbase, DeepAware, Karumi, AfterQuery, Confido, Artisan, SpruceID, FurtherAI, Soff, Zymbly, Bretton AI, Cekura, Puntt, Maywood, HackerRank, Nixo, Aravolta, Terrakotta, Peakflo already logged/excluded in prior runs)._
- **Delve** — Applied AI Engineer (AI-native compliance platform; "fastest-growing compliance company"). https://www.ycombinator.com/companies/delve/jobs/u6ggqYv-applied-ai-engineer — **strong fit: applied-AI + fast-growing SaaS.** Seniority unverified.
- **PermitFlow** — Applied AI Engineer (construction-permitting software; $31M Series A). https://www.ycombinator.com/companies/permitflow/jobs/W67Dl1F-applied-ai-engineer — Applied-AI target title, funded growth-stage. Seniority unverified.
- **Terra API** — AI Engineer (health / wearable-data API platform). https://www.ycombinator.com/companies/terra-api/jobs/0f5CP0r-ai-engineer — AI-Engineer target title; API/data-integration fit. Seniority unverified.
- **Gem** — AI Product Engineer (AI-first recruiting platform; $150k–260k+equity). https://www.ycombinator.com/companies/gem/jobs/4Uathaz-ai-product-engineer-san-francisco — Applied-AI-adjacent ("AI Product Engineer"); SF. Seniority unverified (comp range spans levels).
- **ClaimSorted** — Forward Deployed Engineer (insurtech; build/deliver onboarding systems for insurers). https://www.ycombinator.com/companies/claimsorted/jobs/8N1SLMl-forward-deployed-engineer — FDE target title at an insurtech startup. Seniority unverified.
- **Quindar** — Forward Deployed (Product) Engineer (satellite-operations software platform). https://www.ycombinator.com/companies/quindar/jobs/pfKZs3i-forward-deployed-engineer — FDE target title, BUT **satellite/space domain → possible ITAR/US-person requirement; verify before effort.** Seniority unverified.
- **EXCLUDED (seniority/geo/intern):** Paragon (Founding FDE + FDE Intern), Weave (FD Engineering *Manager*), Saphira AI (Founding Applied-AI, 5+ yrs), Bild AI (Founding Eng Applied-AI), Kastle (Founding Applied-AI), Peakflo (FDE — **India/Remote**).

### Excluded (net-new sightings this run, logged so future runs don't re-surface)
- **Defense / federal / clearance / gov (US-person near-certain):** Innovative Defense Technologies (Associate AI Engineer — Mount Laurel NJ + Arlington VA), Parsons (Data Analyst DC + AI/ML Engineer — **Aberdeen MD = Aberdeen Proving Ground**), Lentech (Junior Data Scientist — **Fort Meade MD**), California Correctional Health Care Services (Data Analyst / Research Data Analyst I — state corrections).
- **FAANG-tier / near-FAANG / trading-floor (referral or out-of-scope):** NVIDIA (Applied ML Engineer Circuit-Design NCG 2026 ×2), Tesla (AI Engineer — Optimus Whole-Body-Controls), **Jane Street (Machine Learning Engineer — prop-trading/quant, profile wants non-trading-floor)**, Centene (Data Scientist **II** — mid), Capital One (Data Analyst Associate — **2027 start, too far out**).
- **Research / clinical / public-sector / education / student-board:** Penn State (Data Scientist — Hawaii, student-jobs board), Beth Israel Lahey (Healthcare Data Analyst — OBGYN/clinical), Senseye/Siemens (Research Data Analyst), Ensign College (Student-Employee Data Analyst), Consumer Reports (Data Analyst — limited-duration), University of Rochester Advancement (Data Scientist), Corning (QA Data Analyst), Volvo Group (BI — Fall-2026 program), Danaher/Harris/etc. niche rows noted inline.
- **Co-op (explicitly co-op, weak timing for May-2026 grad):** Campbell Soup (Data Engineer DA&AI Co-Op, Data Engineer Operational-Support Co-op, Data Engineer Agentic-AI & ML-Ops Co-op, Agentic AI Engineer Co-Op ×2).

### Bonus — adjacent titles worth adding to the search vocabulary
- **"People Analytics Analyst" (Raymond James — Qlik Sense; Workday — Pleasanton)** — the profile's **People-Analytics / HR-Data-Analyst** target surfaces under this exact title at financial-services + HR-SaaS employers; add `"People Analytics Analyst"` (and the `Qlik Sense` qualifier) as a first-class search term — a bare "Data Analyst" search under-weights it.
- **"Associate Conversion Data Analyst" (Bloomerang)** — growth/conversion-analytics DA variant with an explicit entry rung.
- **"Business Intelligence Development Analyst" (Hologic)** — BI-Developer target variant behind a longer title.
- **"AI Product Engineer" (Gem)** — product-flavored Applied-AI title a plain "AI Engineer" search misses.
- **TX in-state net this run:** Fidelity (Westlake — DFW-metro), Cloudflare intern (Austin). PayPal/MeritFirst (Austin) + Tata (Plano) already logged.

### TODO for next (daily) run
- **CONCURRENCY:** this is the 6th backfill on `main` in ~5 days (07-03 → 07-07). Always
  `git fetch origin main` and read the LATEST log before de-duping — same-window
  one-day-apart passes over the same sources are now ~90%+ overlap; expect a short
  net-new list and DO NOT pad it. Tier 1 was legitimately empty this run.
- **Source health:** `speedyapply/NEW_GRAD_USA` is now effectively **dead for net-new**
  (0 this run; 20–110d-dominated) — demote to a quick spot-check. **`zapply` + `jobright
  ENG`** remain the only productive trackers (jobright DA caps at ~7 days; jobright BA
  thin). Keep **curl + local Python parse, NOT WebFetch**, for the trackers (all HTTP 200).
- **HN July thread `48747976`** still 000/403 on every machine-read path (Algolia
  items/search, hnhiring, nchelluri) — re-confirmed. WebSearch-over-mirrors now returns
  mostly **anonymous email-application posts** (no stable links). Highest-value unsolved
  community item; Reddit/Discord still hard-blocked.
- **JD/visa verification** unchanged #1 structural blocker: greenhouse/ashby/workday/
  oracle/smartrecruiters/jobright = 403 (WebFetch) / 000 (curl egress-denied). All visa
  buckets inferred; zapply's H-1B/Sponsor column is the only per-company signal.
- **YC `site:ycombinator.com/companies … "Forward Deployed Engineer" / "Applied AI
  Engineer"`** remains the single most productive community channel — run both queries
  every pass (net-new this run: Delve, PermitFlow, Terra API, Gem, ClaimSorted, Quindar).
