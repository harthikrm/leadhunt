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
