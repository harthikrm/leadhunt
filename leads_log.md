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

## Run: 2026-06-20 18:35 (DEEP BACKFILL — 30 day window)

**SECOND DEEP BACKFILL of the day** (a prior backfill ran 05:21). Same 30-day
window (~May 21 – Jun 20). This pass re-swept the readable trackers for rows the
05:21/12:00 runs did NOT log, and re-attempted every community board. Everything
already logged earlier today is de-duped out below — only **NEW** rows appear.

**Coverage & honesty notes (read before trusting anything below):**
- **Fully covered (readable):** `speedyapply/2026-AI-College-Jobs` →
  `NEW_GRAD_USA.md`, loaded in full via `raw.githubusercontent.com` (117 rows,
  ages 0d–52d). This is the one consistently machine-readable, dated,
  directly-linked source. All NEW leads below come from it unless marked otherwise.
- **Degraded this run:** `jobright-ai/2026-Data-Analysis-New-Grad` README now
  renders only "last 7 days" with **relative/ambiguous dates** (the fetcher read
  them as 2025) — **not usable for new dated rows this run.** No new jobright rows logged.
- **NOT covered / blocked (be explicit):**
  - **Community boards — ALL blocked again:** HN thread 48357725 via Algolia
    items API, Algolia search API, AND `hnrss.org` → all **HTTP 403**.
    `startup.jobs` → 403. Reddit "who is hiring" → web search returned only
    stale/2025 aggregator pages, no current datable thread. **Nothing logged from
    any community board.** Net finding for future daily runs: HN/Reddit/startup.jobs
    remain unreadable by this fetcher — do not budget on them until an
    authenticated/feed path is found.
  - **Individual JD verification — ALL still blocked (HTTP 403):** workday, ashby,
    greenhouse, etc. Every visa bucket below is **inferred from company type + role,
    NOT JD text.** Every "verify" must be opened manually.
  - LinkedIn / Indeed / Glassdoor / Wellfound: aggregator landing pages only;
    LinkedIn `/jobs/view/` URLs are stable but 403 the fetcher (level/visa unread).
    Captured as informal leads with that caveat — not in main tiers.
- **De-dup:** cross-checked against ALL prior runs (12:00, 05:21). Skipped as
  already-logged: Astera Labs, Dealer Tire, Home Depot (Req183993), True Anomaly,
  Snowflake, NVIDIA LLM-Training, BMS, FNBO, Jerry (SF Bay), KeyBank R-40079, PNC,
  Unity, Upgrade, Node, Hitachi, Excellus/Univera, Capital One, USAA, Celonis,
  TreeHouse, Genesis Financial, Marvell, TIFIN, Hyve, Smithfield, GlobalFoundries,
  Oklahoma State, and all defense/federal/research/non-US exclusions (True Anomaly,
  Inversion, Sierra Nevada, A-TEK, Everwatch, Lentech, Booz Allen, Radiance, CMU
  Secure-AI noted below, Boeing, Quantiphi, Edwards/Novartis/Thermo/MSD/Flatiron/Emory).

### Tier 1 — Hot & strong fit
_None clears the Tier-1 bar this run: every JD 403'd (visa unverifiable), and the
genuinely on-profile NEW rows are all at larger banks/enterprises whose immigration
policy must be checked first → they sit in Tier 2. Honesty rule keeps Tier 1 empty._

### Tier 2 — Worth a look (NEW this run; caveat is "visa inferred, JD 403" unless noted)

| Company | What they do / size | Role | Direct link | Posted (basis) | Visa posture | Fit note | Source |
|---|---|---|---|---|---|---|---|
| Nevoya | Zero-emission freight/trucking logistics startup; early/growth | AI Operations Associate (Texas) | https://jobs.ashbyhq.com/nevoya/3163e7df-5c59-4b8a-a37a-15caf2e543d5 | "8d" (≈Jun 12) | Silent, startup — likely OK | **Austin, TX = candidate-local.** Applied-AI ops at a startup; gap: "Operations Associate" leans ops/process over pure build (also a CA twin: …/ece297a0-f8f2-47dd-9f1e-395662ea7633) | speedyapply NEW_GRAD |
| Enbridge | Energy/pipeline infrastructure; large | Data Analyst Specialist I – Work Management Technology | https://enbridge.wd3.myworkdayjobs.com/en-US/enbridge_careers/job/Houston-TX-USA/Data-Analyst-Specialist-I--Work-Management-Technology_71806 | "7d" (≈Jun 13) | Silent, larger company — **verify** | **Houston, TX.** Entry Data Analyst; SQL/BI fit; gap: ops-tech domain, large-co policy unread | speedyapply NEW_GRAD |
| Citi | Global bank; large public | Junior Data Services and AI Developer – Officer | https://citi.wd5.myworkdayjobs.com/en-US/2/job/Jersey-City-New-Jersey-United-States/Junior-Data-Services-and-AI-Developer---Officer_26967855 | "15d" (≈Jun 5) | Silent, larger company — **verify** (big bank → real immigration policy) | Explicit "Junior … AI Developer"; data+AI build fit; gap: bank policy unread | speedyapply NEW_GRAD |
| Bank of America | Global bank; large public | Data Scientist I – Fraud Model Governance | https://ghr.wd1.myworkdayjobs.com/en-US/us-emplsv/job/Charlotte/Data-Scientist-I----Fraud-Model-Governance_26019387 | "10d" (≈Jun 10) | Silent, larger company — **verify** | Entry DS I; analytics/ML fit; gap: model-governance (not GenAI build) + bank policy | speedyapply NEW_GRAD |
| Bank of America | Global bank; large public | Client Quantitative Analyst I – Analytics Transformation | https://ghr.wd1.myworkdayjobs.com/en-US/us-emplsv/job/New-York/Client-Quantitative-Analyst-I---Analytics-Transformation_26019832 | "8d" (≈Jun 12) | Silent, larger company — **verify** | Clean **Quantitative Data Analyst (non-trading-floor)** target match; analytics-transformation, not a trading desk; gap: bank policy | speedyapply NEW_GRAD |
| Morningstar | Investment research/data; mid-large public | Associate Quantitative Analyst | https://morningstar.wd5.myworkdayjobs.com/en-US/confidential/job/Chicago/Associate-Quantitative-Analyst_REQ-055869 | "1d" (≈Jun 19) | Silent, larger company — **verify** | **Quantitative Data Analyst (non-trading-floor)** fit at a data/research firm; strong analytics overlap; gap: finance domain | speedyapply NEW_GRAD |
| Cypress Creek Renewables | Solar/renewables developer; mid-size | Junior Engineer – AI Automation | https://ccrenew.com/careers/job-listing/?gh_jid=7948197 | "21d" (≈May 30) | Silent, mid-size — likely OK | "Junior … AI Automation" = build-leaning applied-AI; Python/automation fit; gap: recency mid-window, domain-specific | speedyapply NEW_GRAD |

### Tier 3 — Long shots / needs verification / weaker fit (NEW this run)

| Company | What they do | Role | Direct link | Posted | Visa posture | Why Tier 3 | Source |
|---|---|---|---|---|---|---|---|
| JustAnswer | Online expert Q&A / AI assistant; mid-size | Associate AI Conversation Designer (Remote) | https://job-boards.greenhouse.io/justanswer/jobs/8587759002 | "8d" (≈Jun 12) (also req …8509749002, "4d") | Silent, mid-size — verify | **Remote** + applied-LLM (conversation/prompt design); adjacent to AI-eng but design-leaning, not core build | speedyapply NEW_GRAD |
| Loop | Logistics/freight-payments software; growth-stage | AI Operations Associate | https://job-boards.greenhouse.io/loop/jobs/5819779004 | "11d" (≈Jun 9) | Silent, growth startup — likely OK | Applied-AI ops at an AI-forward startup; gap: ops-associate, not eng | speedyapply NEW_GRAD |
| MiTek | Building-products / construction tech; large | Supply Chain Data Analyst I | https://mii.wd5.myworkdayjobs.com/en-US/mitek/job/StCharles-MO-USA/Supply-Chain-Data-Analyst-I_R06378 | "9d" (≈Jun 11) | Silent, larger company — **verify** | Entry Data Analyst; SQL/analytics fit; gap: supply-chain domain, no AI angle | speedyapply NEW_GRAD |
| Franklin Templeton | Asset management; large public | Junior Quant Developer | https://franklintempleton.wd5.myworkdayjobs.com/en-US/primary-external-1/job/New-York-New-York-United-States-of-America/Junior-Quant-Developer_868307-1 | "3d" (≈Jun 17) | Silent, larger company — **verify** | Junior quant **developer** (build, not trading desk); Python/SQL fit; gap: finance-quant domain, large-co policy | speedyapply NEW_GRAD |
| Clear Investment Group | Real-estate investment firm; mid-size | AI Associate | http://clearinvestmentgroup.applytojob.com/apply/GhAjTFH6Km/AI-Associate | "10d" (≈Jun 10) | Silent, mid-size — verify | Generalist "AI Associate"; scope vague (could be ops/enablement vs build) — screen JD | speedyapply NEW_GRAD |
| DebtBook | Municipal-finance/debt SaaS fintech; growth-stage | Associate Quantitative Strategist | https://job-boards.greenhouse.io/debtbook/jobs/4698960005 | "24d" (≈May 27) | Silent, growth startup — likely OK | Quant/analytics at a fintech SaaS; gap: recency mid-window, "strategist" framing | speedyapply NEW_GRAD |
| SBT Global | Trading/distribution company; small-mid | Junior Data Analyst – Operations / Sales Analytics | https://jobs.smartrecruiters.com/SBTGlobalInc/3743990013715446-junior-data-analyst-operations-sales-analytics-?oga=true | "0d" (≈Jun 20) | Silent, small — likely OK | Junior DA, ops/sales analytics; SQL/BI fit; gap: small co, no AI angle | speedyapply NEW_GRAD |
| Carnegie Mellon University | University research lab | Associate Machine Learning Engineer – Secure AI Lab | https://cmu.wd5.myworkdayjobs.com/en-US/cmu/job/Pittsburgh-PA/Associate-Machine-Learning-Engineer---Secure-AI-Lab_2024609 | "11d" (≈Jun 9) | Unclear — **verify** | Entry ML Eng (academic; universities often OPT/CPT-friendly), BUT "Secure AI Lab" may carry funding/citizenship constraints — confirm | speedyapply NEW_GRAD |
| WorldQuant | Quant investment-management firm; large | Junior Quantitative Analyst | https://job-boards.greenhouse.io/worldquant/jobs/4616499006 | "11d" (≈Jun 9) | Silent, larger company — **verify** | **Austin, TX** + junior quant analyst; analytics/Python fit; gap: research/alpha (trading-adjacent) borders the "non-trading-floor" exclusion — screen | speedyapply NEW_GRAD |
| KeyBank | Regional bank; large public | Quantitative Analytics Associate – Capital (R-40080) | https://keybank.wd5.myworkdayjobs.com/en-US/external_career_site/job/Brooklyn-OH/Quantitative-Analytics-Associate---Capital_R-40080 | "4d" (≈Jun 16) | Silent, larger company — **verify** | NEW req, distinct from R-40079 logged 05:21; same Quant-Data-Analyst fit; gap: bank policy | speedyapply NEW_GRAD |

### Informal / LinkedIn leads (direct links found, but level + visa UNVERIFIED — LinkedIn 403'd the fetcher)
_Surfaced via web search for founder/recruiter "Applied AI Engineer" posts. Treat as raw leads to open manually; I could not confirm seniority (some may be senior) or sponsorship. Dates are search-reported May 2026 (within 30d for the later ones)._

| Company | Role | Direct link | Note |
|---|---|---|---|
| Vi Labs (vi.co) | Applied AI Engineer – Wellness (Remote) | https://vi.co/careers/applied-ai-engineer-wellness/58.860/ | Real direct careers link. Search indicates Vi's open AI roles skew **Senior/Principal** → likely above target level; also a "Life Sciences & Healthcare" variant exists (only on aggregators remoterocketship/jobgether, no clean direct link). Verify level before applying. |
| Blossom | Applied AI Software Engineer (All Levels) | https://www.linkedin.com/jobs/view/applied-ai-software-engineer-all-levels-at-blossom-4416493233 | "All Levels" → entry plausibly in scope; LinkedIn page unread |
| RS Global Services | Applied AI Engineer (Onsite SF/NY) | https://www.linkedin.com/jobs/view/applied-ai-engineer-onsite-sf-ny-at-rs-global-services-4415884394 | ~May 18; onsite; level/visa unread |
| Fortegra | Applied AI Engineer (Iselin, NJ) | https://www.linkedin.com/jobs/view/applied-ai-engineer-at-fortegra-4402810009 | Insurance/specialty-finance; level/visa unread |
| Landair Advisors | Applied AI Engineer (New York, NY) | https://www.linkedin.com/jobs/view/applied-ai-engineer-at-landair-advisors-4417382496 | ~May 20; level/visa unread |

### Adjacent titles encountered (NEW this run) — worth adding to search vocabulary
- **"AI Operations Associate"** (Nevoya, Loop) — applied-AI at startups, but ops/process-leaning vs build. Screen for how much is hands-on engineering.
- **"Junior … AI Developer / AI Automation Engineer"** (Citi, Cypress Creek) — build-leaning entry AI roles outside the usual "ML Engineer" title; good additions.
- **"Associate AI Conversation Designer"** (JustAnswer) — applied-LLM/prompt role; design-leaning.
- Reconfirmed strong quant-analyst targets (non-trading-floor): **"Client Quantitative Analyst I"** (BofA), **"Associate Quantitative Analyst"** (Morningstar), **"Junior Quant Developer"** (Franklin Templeton).

### Excluded this run (logged so future runs don't re-surface)
- **Quant TRADING-floor / markets-desk (out of scope per "non-trading-floor"):** BlackRock (Quant Modeler ×3), Morgan Stanley (Quant Desk Strategist), AQR (Quant Front Office Eng), Galaxy (Quant Trader – Onchain), Old Mission Capital (Jr Quant Trader), Akuna Capital (Jr Quant Researcher – also >30d at 52d), Cross River Bank (Quant Strategies AVP), Corgi Insurance (Quant Associate), Bank of America "Associate – Quant", Hudson River Trading (Jr Quant Latency Eng), RA Capital (Healthcare AI quant). Trading/alpha desks — excluded; reconsider only the explicitly "analytics"/"developer" titled ones above.
- **Defense / federal / clearance (US-person near-certain):** already-excluded set unchanged (True Anomaly, Inversion, Sierra Nevada, A-TEK, Everwatch, Lentech, Booz Allen, Radiance, SteerBridge/Yuma).
- **Research / wet-lab / non-applied-eng:** Edwards, Novartis, Thermo Fisher, MSD, Flatiron, Emory, Illinois/Iowa State, Joslin Diabetes, Revolution Medicines, CLO Virtual Fashion (R&D Research Scientist), Proxima (ICML AI Scientist – conference/research), Figma (Data Scientist – PhD), NVIDIA Research-Scientist roles, DoorDash AI Research Fellowship.
- **Non-US geography:** Boeing (Richmond, Canada), Amexio (Canada), Quantiphi (India), ZOLL (Israel).
- **Sales/GTM/legal/hardware (not the target build profile):** Encord (Commercial Associate), Lumenci (CS & GTM Associate), BIP Ventures (Product Owner), CIG Communities (AI Innovation Associate – vague), Astreya (AI Infra DC Design – datacenter hardware), HPE (Electrical HW Eng), Booz Allen (AI Privacy Associate General Counsel), Aptura (IB Associate – AI Residency, part-time, finance).

### Net new this run
**7 Tier-2 + 10 Tier-3 + 5 informal/LinkedIn = 22 NEW leads** not in any prior run.
Strongest Texas-local / on-profile picks: **Nevoya (Austin)**, **Enbridge (Houston)**,
**Bank of America Client Quant Analyst I**, **Morningstar Assoc Quant Analyst**.
No source beyond the speedyapply tracker was machine-readable this run — community
boards and JD pages remain fully blocked, so this backfill is **tracker-only coverage**.

---
