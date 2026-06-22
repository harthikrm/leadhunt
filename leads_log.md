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

## Run: 2026-06-22 17:09 (DEEP BACKFILL — 30 day window)

**THIS IS A ONE-TIME DEEP BACKFILL, NOT A DAILY PASS.** Run two days after the
prior three runs (all 2026-06-20). Uses a **30-day** recency window
(~May 23 – Jun 22) instead of the normal 24h, to refresh the baseline. Future
daily runs should keep using 24h and treat everything below as already-seen.
Read `leads_log.md` in full first and de-duped against ALL prior runs (06-20
12:00, 05:21 backfill, 18:30, 18:48 backfill).

**Coverage & honesty notes (read before trusting anything below):**
- **Fully/largely covered (loaded via `raw.githubusercontent.com`, not blocked):**
  - `speedyapply/2026-AI-College-Jobs` → `NEW_GRAD_USA.md` — read; "Other"
    (non-FAANG/non-defense) Data/AI/ML rows pulled.
  - `zapplyjobs/New-Grad-Data-Science-Positions` — read; AI/ML/GenAI/DataEng rows
    pulled. **NEW THIS RUN: this tracker carries a visa column** (✅ Sponsor /
    🏛 H-1B Co. / blank). I have logged that flag inline as "tracker visa flag,"
    but it is a **company-level historical-sponsorship indicator, NOT a
    JD-verified, NOT OPT-specific signal** — every JD body itself remained
    unreadable (see below). Still, it's the only machine-readable visa signal
    obtained in any run so far, and none of the kept leads is flagged "no
    sponsorship."
  - `jobright-ai/2026-Data-Analysis-New-Grad` — read; still capped at "last 7
    days" by the maintainers, so Jun 15–22 rows only (no full 30-day depth).
  - `jobright-ai/2026-Business-Analyst-New-Grad` — read; only one data/DS row in
    window (Ekimetrics), rest are process/requirements BA → not logged.
- **PARTIAL coverage caveat:** the WebFetch summarizer collapses these large
  tables and truncates the long tail, so the lists below are the recent/in-scope
  rows it surfaced, **not a guaranteed-exhaustive dump** of every row. Mid-window
  (~May 23 – Jun 10) depth on speedyapply/zapplyjobs is thinner than the fresh end.
- **NOT covered / blocked this run (be explicit):**
  - **Individual JD verification — STILL 100% blocked (HTTP 403):** greenhouse
    (`job-boards.greenhouse.io`), `jobs.ashbyhq.com`, `*.myworkdayjobs.com`,
    `jobs.smartrecruiters.com`, oracle cloud, **AND `jobright.ai/jobs/info/...`
    posting pages, AND `builtin.com`** all 403'd the fetcher. I could not read a
    single JD body. Every visa bucket below is inferred from company type + role
    (+ the zapplyjobs flag where present), NOT JD text. Every "verify" must be
    opened manually. Same structural blocker as all four prior runs.
  - **Seniority caveat:** because JDs are unreadable, roles not explicitly
    labeled junior/new-grad/associate/entry/"I"/"Officer" have **seniority
    unverified** — flagged inline.
  - **Community boards — still unreadable for direct links.** HN "Who is hiring
    (June 2026)" thread `48357725`: the thread page, the `nchelluri.github.io/hnjobs/`
    GitHub-pages mirror, and `hnhiring.com` all **403'd** direct fetch. A
    `WebSearch` over the thread returned partial text but **no per-comment
    permalinks** — so HN items below are logged honestly as informal/unlinked.
    Reddit/Discord/Slack: not machine-readable (Reddit hard-blocked in prior runs;
    not retried). LinkedIn/Indeed/Glassdoor/Wellfound/Built In: only aggregator
    landing pages, no per-posting dates or stable direct links.
  - **SimplifyJobs** New-Grad-Positions AI/ML category: not attempted this run
    (known README-truncation / >10MB JSON issue).
- **Recency basis:** jobright rows carry calendar dates (used directly).
  speedyapply/zapplyjobs rows carry an "age" field read against each tracker's
  ~Jun 22 refresh; ages shown in minutes/hours (e.g. "14m","1h","3h") are scraper
  **first-seen** stamps, NOT guaranteed post dates — flagged inline where used.
- **De-duped out as already logged** (appear again in trackers but NOT repeated
  below): Tanium Corporate AI Eng, NewsBreak Applied AI Eng, Citi *Generative AI
  Engineer Officer* (the *Junior Data Services & AI Developer* below is a DIFFERENT
  Citi req), State Street GenAI Officer + BestX internship, Elevance Gen AI Eng,
  Fiserv ML SWE, CarGurus MLOps, all Astera Labs reqs, DoorDash ML Infra, Snowflake
  AI Research Sci, NVIDIA, CrowdStrike, Zoom ML, Fortinet Applied AI, Tradeweb/ICD,
  SBT Global Jr DA, Dealer Tire, Home Depot Assoc DS, Hitachi DS I/II, PTC Jr
  DA/Analytics Eng, USAA DS I, DraftKings Analyst I, Caterpillar, BofA *Client Quant
  Analyst I* (the *Data Scientist I – Fraud* below is a DIFFERENT BofA req).

### Tier 1 — Hot & strong fit
_Entry-labeled, in-window, non-defense, non-FAANG, strong applied-AI/data fit. Visa buckets inferred (JDs 403)._

| Company | What they do / size | Role | Direct link | Posted (basis) | Visa posture | Fit note | Source |
|---|---|---|---|---|---|---|---|
| Citi | Global bank; large public | Junior Data Services and AI Developer – Officer | https://citi.wd5.myworkdayjobs.com/en-US/2/job/Jersey-City-New-Jersey-United-States/Junior-Data-Services-and-AI-Developer---Officer_26967855 | "16d" (≈Jun 6) | Silent, larger company — **verify** (zapplyjobs flags Citi 🏛 H-1B sponsor — company-level, not JD-verified) | **"Junior" + "AI Developer" + "Officer"** = explicit entry AI-dev rung; Python/AI build fit; gap: large-bank immigration policy + JD 403 | speedyapply NEW_GRAD |
| Paramount Global | Media/streaming; large public (non-FAANG) | Machine Learning Engineer, Entry | https://careers.paramount.com/job/New-York-Machine-Learning-Engineer,-Entry-NY-10036/1389620800/ | scraper first-seen "14m" (just appeared on tracker; calendar post date **unconfirmed** — recency basis is the first-seen stamp, treat as recent-but-unverified) | Silent, larger company — **verify** (no tracker flag) | **Explicit "Entry" ML Engineer** at a large non-FAANG media co (Burbank CA / NYC); clean entry-rung title match; gap: recency is first-seen-not-post-date + JD 403 | zapplyjobs DS |

### Tier 2 — Worth a look (good fit; caveat = seniority and/or visa unverified, JD 403)

| Company | What they do / size | Role | Direct link | Posted (basis) | Visa posture | Fit note | Source |
|---|---|---|---|---|---|---|---|
| Zayo | Fiber/bandwidth-infrastructure provider; large | AI Engineer (US, Remote) | https://zayo.wd1.myworkdayjobs.com/Zayo_Careers/job/United-States/AI-Engineer_R0016139 | "3d" (≈Jun 19) | Silent, larger company — **verify** (zapplyjobs flag 🏛 H-1B Co.) | **Remote** AI Engineer at a large infra co + sponsor-history flag; gap: **seniority unverified** (no junior/I in title) + JD 403 | zapplyjobs DS |
| Harvey | Legal-GenAI startup (LLMs for law firms); growth-stage (well-funded) | Data Scientist, Product | https://jobs.ashbyhq.com/harvey/1321b20d-d6f8-4bdb-b2de-ec33c0948b53/application | "3d" (≈Jun 19) | Silent, growth startup — likely OK (zapplyjobs flag ✅ Sponsor) | **Hot applied-GenAI company** = strong culture/stack fit; gap: DS-product framing (not eng), seniority unverified, JD 403 | zapplyjobs DS |
| GumGum | Contextual-advertising / computer-vision ad-tech; mid-size | Data Scientist I | https://jobright.ai/jobs/info/69e32f6bbe46fa3a4ef5984d (jobright) · https://job-boards.greenhouse.io/gumgum/jobs/7703520003 (greenhouse) | jobright shows **Jun 21**; greenhouse age says **"52d"** (≈early May) — **age conflict**, treat as a repost re-surfaced Jun 21 | Silent, mid-size — likely OK | **"I" = entry** DS at a mid-size ad-tech (CV/NLP); good applied fit; gap: post-date conflict (orig may be ~6wk old) + JD 403 | jobright DA + speedyapply |
| Bank of America | Global bank; large public | Data Scientist I – Fraud Model Governance | https://ghr.wd1.myworkdayjobs.com/en-US/us-emplsv/job/Charlotte/Data-Scientist-I----Fraud-Model-Governance_26019387 | "11d" (≈Jun 11) | Silent, larger company — **verify** | **"I" = entry** DS; fraud-model/analytics fit; gap: large-bank policy + JD 403 (distinct from the already-logged BofA Client Quant Analyst I) | speedyapply NEW_GRAD |
| Enbridge | Energy/pipeline infrastructure; large public | Data Analyst Specialist I – Work Management Technology | https://enbridge.wd3.myworkdayjobs.com/en-US/enbridge_careers/job/Houston-TX-USA/Data-Analyst-Specialist-I--Work-Management-Technology_71806 | "8d" (≈Jun 14) | Silent, larger company — **verify** | **Houston, TX = in-state.** "I" entry analyst; SQL/BI fit; gap: work-mgmt-tech/ops-analytics (not AI-eng) + JD 403 | speedyapply NEW_GRAD |
| GlobalFoundries | Semiconductor foundry; large public | AI Enablement Strategist – New College Graduate | Austin TX: https://globalfoundries.wd1.myworkdayjobs.com/en-US/external/job/USA---Texas---Austin/AI-Enablement-Strategist--New-College-Graduate-_JR-2600367 · Malta NY: https://globalfoundries.wd1.myworkdayjobs.com/en-US/external/job/USA---New-York---Malta/AI-Enablement-Strategist--New-College-Graduate-_JR-2600365 | "18d" (≈Jun 4) | Silent, larger company — **verify** | **Austin, TX = in-state**, explicit **NCG** program; gap: "Enablement Strategist" skews enablement/strategy over build (adjacent to AI Solutions, not core AI-eng) | speedyapply NEW_GRAD |
| Ekimetrics | Data-science / marketing-effectiveness consultancy; mid-size | Business Scientist – Data Science & Marketing Effectiveness | https://jobright.ai/jobs/info/69e28e3a5c44d4710fe25b41 | Jun 21 | Silent, mid-size — verify | Applied DS (marketing-mix / measurement) — Python/SQL/stats fit; gap: marketing-analytics domain + consultancy + seniority unverified | jobright BA |

### Tier 3 — Long shots / needs verification / seniority or domain risk

| Company | What they do | Role | Direct link | Posted | Visa posture | Why Tier 3 | Source |
|---|---|---|---|---|---|---|---|
| CVS Health | Health services/pharmacy; large public | Data Scientist (multiple reqs) | https://jobright.ai/jobs/info/6a36c5aca0f3e56e86d6bdc7 (RI) · https://jobright.ai/jobs/info/6a36c5a929c90c607e4e58f8 (NY) | Jun 22 | Silent, larger company — **verify** | Entry-ness unverified (no "I"/junior in title) + healthcare domain + JD 403; distinct from prior CVS *Data Engineer* (Irving). Several near-duplicate reqs (RI Woonsocket / NY) | jobright DA |
| Etched | Transformer-ASIC (AI chip) startup; growth-stage | Applied AI Engineer, Silicon Engineering | https://jobs.ashbyhq.com/etched/831bfa22-d883-450b-9b10-2a16421525a0/application | "18h" (≈Jun 21) | Silent, startup — likely OK (zapplyjobs flag 🏛 H-1B Co.) | Target title BUT **"Silicon Engineering"** = chip/hardware focus, not applied-GenAI-product; seniority unverified | zapplyjobs DS |
| Reddit | Social platform; large private (non-FAANG, in scope) | Machine Learning Engineer | https://job-boards.greenhouse.io/reddit/jobs/8014401 (NYC) · https://job-boards.greenhouse.io/reddit/jobs/8014436 (SF) | "3h" first-seen (≈Jun 22, scraper stamp) | Silent, larger company — **verify** (zapplyjobs flag ✅ Sponsor) | Good ML fit + sponsor flag, but **seniority unverified (likely mid/not entry)** + JD 403 | zapplyjobs DS |
| Plaid | Fintech data-infrastructure; mid-large private | Machine Learning Engineer – Embedded · ML Engineer (Research Science) | https://jobs.ashbyhq.com/plaid/50d40e3b-ed34-470d-b094-71e1555c6f1e/application · https://jobs.ashbyhq.com/plaid/95ccc1d4-39ad-467f-8d65-63227d943313/application | "3d" (≈Jun 19) | Silent, larger company — **verify** (flag ✅ Sponsor) | Strong fintech-infra fit; gap: seniority unverified + "embedded/research-science" specializations + JD 403 | zapplyjobs DS |
| Motional | Autonomous-vehicle tech (Hyundai/Aptiv JV); large | Machine Learning Engineer, Data Mining | https://motional.com/open-positions/?gh_jid=7780008003 (Pittsburgh) · https://motional.com/open-positions/?gh_jid=7779985003 (Boston) | "1h" first-seen (≈Jun 22, scraper stamp) | Silent, larger company — **verify** (flag ✅ Sponsor) | ML fit + sponsor flag; gap: AV/robotics domain (vs applied-GenAI) + seniority unverified | zapplyjobs DS |
| CyberProof (a UST company) | Cybersecurity managed-services; mid-large | Business Systems & Data Analytics Associate | https://jobright.ai/jobs/info/6a394f22f6b55d12c79272f7 | Jun 22 | Silent, larger company — **verify** | "Associate" entry rung BUT business-systems/analytics-ops leaning (not AI-eng) + JD 403 | jobright DA |
| Verde Farms | Organic-beef CPG brand; small-mid | Analyst – Category & Commercial Analytics (Remote) | https://jobright.ai/jobs/info/6a36f408649fdf16292fc7ec | Jun 20 | Silent, small/mid — likely OK | **Remote** analyst; SQL/BI fit; gap: category/commercial-analytics is BA-leaning (not AI/eng) | jobright DA |
| Chicago Trading Company | Proprietary trading firm; mid-size | Market Data Analyst | https://jobright.ai/jobs/info/69cdd6c2891d7b11cfcc06e0 | Jun 22 | Silent, mid-size — verify | NOT the "Quantitative Data Analyst" target — "Market Data Analyst" at a prop shop is typically **market-data-feed/vendor ops**, not quant modeling; on-site Chicago; several duplicate reqs | jobright DA |
| Beth Israel Lahey Health | Hospital system; large non-profit | Healthcare Data Analyst (OBGYN Quality) · Data Scientist | https://jobright.ai/jobs/info/6a394fe806a4fd4b1fab9506 (analyst) · https://jobright.ai/jobs/info/6a393398f6b55d12c7926ae5 (DS) | Jun 22 | Silent, larger company — **verify** | Clinical/healthcare-analytics domain (vs applied-AI/data-eng); Boston on-site; JD 403 | jobright DA |

### Community / informal leads (HN "Who is hiring (June 2026)", thread 48357725)
_Surfaced only via `WebSearch` over the thread (the HN page, `nchelluri.github.io/hnjobs/` mirror, and `hnhiring.com` ALL 403'd direct fetch). **No per-comment permalinks were obtainable**, so these are logged honestly as unlinked/unverified — do NOT treat as confirmed without finding the original comment._
- **Comvex.ai** — "Forward Deployment Engineer" (+ other roles), flexible hours but FDE role needs availability through a standard EST business day. Apply: email **peter.lever@comvex.ai** with role + CV. FDE is a target title; seniority/location/visa **unstated** in the snippet. **No direct link captured.**
- **Stealth property-management AI-agents startup** — "Forward Deployed Engineer (backend, Python)," fully remote (UTC−3 to +3), building AI agents that run real operations. Apply: email **mercedes@kinxshn.com**, subject "HN - Forward Deployed Engineer," + CV + salary expectation. **Flagged as likely a stretch:** snippet describes a "senior backend engineer to own a client-facing use case end-to-end" → **senior**, and remote-global (not US-specific). **No direct link captured.**
- **EXCLUDED from tiers:** EggAI (AI Engineer — remote **EU/Switzerland/Norway**, non-US geography); Railtown AI (Head of Developer Relations — senior, non-eng).

### Excluded (logged so future runs don't re-surface)
- **FAANG-tier / FAANG-adjacent (referral track or out of scope):** Google (RTL/Cloud/Applied AI Eng rows), Microsoft (Applied Scientist / Applied Scientist II Bing), Meta (Research Scientist Intern), Amazon (Data Scientist I NY), TikTok + ByteDance + joinbytedance (all ML/Research roles — handled as FAANG-adjacent per prior runs), OpenAI (Research Engineer/Scientist — research + senior, not entry applied-eng).
- **Defense / federal / clearance (US-person near-certain):** Anduril (Data Engineer, Quality Intelligence — Costa Mesa), Booz Allen Hamilton (Data Scientist ×many — Fort Meade / Annapolis Junction / Stafford / Atlanta / DC), General Dynamics IT (Norwegian Analyst — MacDill AFB), Boeing (Associate Data Analyst — Long Beach; Junior Data Scientist — Richmond CANADA), Defense Unicorns FDE DE (already logged).
- **Non-US geography (F-1 OPT is US-only):** TMX Group (Toronto, contract), Exiger (Vancouver/Toronto ×many), ERCO Worldwide (Gatineau QC), EggAI (EU/Switzerland/Norway).
- **Wet-lab / clinical / non-data research (not applied-AI/data-eng):** Yale Research Assistant 1, Henry M. Jackson Foundation Research Assistant I, University of Rochester Bioinformatics Analyst I, Fred Hutch (Clinical Research Coordinator I / Post-Doc Biostatistics), Boehringer Ingelheim (Fall Co-Op Clinical Data Science), Carta Healthcare (Clinical Data Abstractor), GeneDx (Assistant Clinical Analyst I), Pfizer (AI/ML Eng — Vaccine Research), Lila Sciences (ML co-op, Digital Therapeutics), Doctors Without Borders (Data Science Intern), SLAS (Research Assistant), Samaritan Daytop Village (Research Associate), Applecart (Research Specialist), City of Baltimore / Sidley Austin / Neuberger / Exiger research-analyst rows (records/conflicts/RFP research, not data-eng).
- **Intern-only / co-op (candidate graduates May 2026 → student-internship timing is a weak fit; "Intern" is in target type but these read as in-school terms):** Tesla (ML/AI/Applied-AI/ML-Platform Interns), d-Matrix (Applied AI Eng Intern), Workato (AI Eng Intern), Human Computer Lab (SW/ML Intern), State Street (BestX AI Engineer Internship — already logged). Listed so they aren't re-surfaced as "new FTE."
- **Senior/staff:** Salesforce (Senior Staff SWE, ML Infrastructure — Slack), Intuitive ML Engineer (seniority unverified, SF — low priority), Fiserv "AI Engineer" Columbus (= Data Scientist, Cybersecurity AI — domain/seniority unclear, lower priority).
- **Retail/merch data-collector & non-target rows:** Tyson Foods (Data Collector), The Retail Odyssey Company (Retail Data Collector), SAS Retail Services (Coordinator), Kiss Beauty (Sales Data Mgmt Specialist), East Side Union HSD (Data Reporting Specialist), Verde-style category-analytics kept in Tier 3 only.
- **Test/junk rows seen in jobright DA (ignore):** The D. E. Shaw Group "ViduZZZi Test 3/4/5", "AgneZZZ Test" — these are tracker test artifacts, not real postings.

### Bonus — adjacent titles worth adding to the search vocabulary
- **"Junior Data Services and AI Developer (Officer)"** (Citi) — reinforces "Officer" as a bank entry rung AND that "AI Developer" is a high-signal entry title.
- **"Machine Learning Engineer, Entry"** (Paramount) — the literal "Entry" suffix is a useful keyword to catch entry roles that omit "new grad/junior."
- **"AI Enablement Strategist – New College Graduate"** (GlobalFoundries) — reinforces the AI-enablement adjacency (Marvell/Smithfield/FNBO family), NCG-labeled; skews strategy/enablement over build.
- **"Business Scientist"** (Ekimetrics) — a data-science role under a non-obvious title; worth adding to catch DS roles that hide behind "scientist/analyst" labels.
- **CAUTION keyword — "Market Data Analyst"** (Chicago Trading Co): looks like a Quant-Data-Analyst match but is usually **market-data-feed/vendor ops** at trading firms, NOT quant modeling — screen before treating as a target-title hit.

### New capability discovered this run (use in future runs)
- **`zapplyjobs/New-Grad-Data-Science-Positions` exposes a visa column** (✅ Sponsor / 🏛 H-1B Co. / blank). It's a **company-level historical-sponsorship flag, not JD-verified and not OPT-specific**, but it's the first machine-readable visa signal any run has obtained — use it as a coarse prioritization aid (none of the kept leads carried a "no sponsorship" marker).

### TODO for next (daily) run
- **JD/visa verification is still the #1 unsolved blocker** — EVERY host 403s now,
  including `jobright.ai/jobs/info/...` and `builtin.com` (previously untested),
  on top of greenhouse/ashby/workday/smartrecruiters/oracle. Until a readable path
  exists (authenticated fetch / MCP fetch / alternate mirror), all visa buckets
  stay inferred. The zapplyjobs visa-flag column is the best partial workaround so far.
- **Community boards** remain link-blind: HN thread `48357725` + `nchelluri.github.io`
  mirror + `hnhiring.com` all 403; only WebSearch snippets (no permalinks) get through.
  Reddit hard-blocked. Finding ONE readable community path is the highest-leverage
  unlock for the "informal founder/recruiter post" part of the brief.
- **jobright Data-Analysis** is capped at "last 7 days"; for 30-day depth a future
  backfill needs its full Airtable/listings export.
- **SimplifyJobs** AI/ML category still unread (truncation / >10MB JSON) — try a
  ranged/paginated fetch or the per-category JSON.

---
