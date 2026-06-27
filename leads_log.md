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

## Run: 2026-06-27 17:09 (DEEP BACKFILL — 30 day window)

**THIS IS A ONE-TIME DEEP BACKFILL, NOT A DAILY PASS.** Run 2026-06-27 with a
wider budget. Recency window = **last 30 days (~May 28 – Jun 27)** instead of the
normal 24h, to refresh the baseline. Future daily runs should keep using 24h and
treat everything below as already-seen. Read `leads_log.md` in full first and
de-duped against ALL six prior runs (06-20 12:00, 06-20 05:21 backfill,
06-20 18:30, 06-20 18:48 backfill, 06-24 17:09 backfill, 06-25 17:30 backfill).

**Coverage & honesty notes (read before trusting anything below):**
- **METHOD (same as 06-25, which worked):** `curl`-ed the raw markdown trackers
  from `raw.githubusercontent.com` (the ONLY non-blocked host) and parsed them
  locally with Python — avoids the WebFetch small-model truncation that capped
  prior runs at ~60 rows. All six trackers loaded in full this run.
- **Fully covered (curl'd raw + parsed locally):**
  - `speedyapply/2026-AI-College-Jobs` → `NEW_GRAD_USA.md` — read in full.
    Finding: **every in-window entry/new-grad row that fit was already logged** in
    prior runs (speedy is the most-mined source) → 0 net-new from speedy this run.
  - `zapplyjobs/New-Grad-Data-Science-Positions` → `README.md` — read in full
    (Data Scientist/AI-Eng/ML-Eng/Data-Eng/Data-Analyst/FDE sections). Richest
    net-new source this run. Carries a Visa column (`🏛 H-1B Co.` / `✅ Sponsor` /
    blank) — noted per-row; a company-level signal, NOT a per-JD guarantee.
  - `jobright-ai/2026-Engineering-New-Grad` → `README.md` — read in full (1.5 MB;
    AI/ML/Data-Eng new-grad rows live here, calendar-dated).
  - `jobright-ai/2026-Data-Analysis-New-Grad` → `README.md` — read in full, BUT
    still **caps visible rows at "last 7 days" (Jun 20–27 only)** per its stated
    capacity constraint → 30-day depth unavailable there (same as 06-24 / 06-25).
  - `jobright-ai/2026-Business-Analyst-New-Grad` — read; **0 data/analytics-eng
    rows** (only process/requirements BA) → nothing logged from it.
  - `SimplifyJobs/New-Grad-Positions` (`dev` branch) — DS/AI/ML section parsed in
    full. Mostly stale (1mo–7mo); 5 net-new in-window rows surfaced below; for
    several, **Simplify only exposes a `simplify.jobs/c/<company>` redirect — no
    direct ATS URL** (flagged per-row).
- **NOT covered / blocked this run (be explicit) — UNCHANGED structural blockers:**
  - **Individual JD verification — ALL still blocked.** `curl` to greenhouse +
    ashby = **000 (CONNECT tunnel failed, 403 — egress policy)**; `WebFetch` to
    ashby = **403**. **I could not read a single JD body** → EVERY visa bucket
    below is inferred from company type + role + the zapply Visa column, NOT JD
    text. Every "verify" must be opened manually. Seniority for any role NOT
    explicitly labeled new-grad/junior/associate/"I"/"1"/entry/early-career/NCG is
    **unverified** and flagged inline.
  - **Community boards — HN still unreadable by direct fetch.** HN "Who is hiring?"
    is **still the June thread `48357725`** (July's not up yet as of Jun 27 —
    confirmed via WebSearch; watch ~Jul 1). `curl` to `hn.algolia.com/api/v1/items/48357725`
    = **000**. WebSearch *over* HN returned only the thread URL, no per-post links.
    Reddit/Discord/Slack: not machine-readable (hard-blocked prior runs).
  - **WebSearch (web at large) DID surface 2 datable applied-AI leads** with stable
    links (FurtherAI, Domino — see below), but most of LinkedIn/Indeed/Glassdoor/
    Wellfound/startup.jobs are aggregator landing pages with no per-posting date or
    stable direct link. No founder/recruiter LinkedIn post with a datable stable
    link surfaced.
  - **People Analytics / HR Data Analyst** (target titles): searched the open web;
    only aggregator pages (Indeed/ZipRecruiter/Glassdoor/jobgether) returned — **no
    individual posting with a stable direct link + confirmable date** → nothing
    loggable. Coverage attempted, came up empty for stable links.
- **Recency basis:** jobright rows carry calendar dates (Jun 20–27 used directly,
  shown as "(Nd, jobright cal)"). speedyapply rows carry an "age" field read against
  the Jun 27 refresh. zapplyjobs ages in minutes/hours ("12m","2h","19h") are
  scraper **first-seen** stamps, NOT guaranteed post dates → flagged
  "(zapply first-seen)" and treated as "≈within window, exact date unconfirmed."
  Simplify rows carry a "Nd"/"Nmo" age; only "Nd ≤30" kept.
- **De-duped out as already logged** (appear again in trackers but NOT repeated
  below): UST HealthProof Assoc DE (Frisco/Bellevue; new **Seattle** loc link
  `https://jobright.ai/jobs/info/6a3a1470214ae004c7a214f6` noted only), OneStream
  Assoc AI Eng (new **Chicago** loc), Brellium Deployment Assoc, CyberProof Assoc DE,
  CVS Assoc DE, GumGum DS I, SentiLink DS New Grad, Capgemini Jr Power BI (new
  **Westlake TX** loc `https://jobright.ai/jobs/info/6a3e042f122f340d29cf28a0`),
  Innodata Applied/GenAI Associate, iSoftStone Assoc AI/ML, Westinghouse DS NGLP,
  Esri DS I, Jerry Assoc DS, TreeHouse Assoc Product DS, Unity ML New Grad (new
  loc links), NewsBreak Applied AI Eng (new req 4691989006), Citi Gen AI Eng (new
  loc), Brex AI Eng Ecosystem, GlobalFoundries AI/ML Systems NCG, Cox Entry DE,
  AbbVie Assoc DE 1, BCBST Assoc DE 1, blend360 Jr DS, Snowflake FDE (new
  "Forward Deployed Analytics Engineer" variant noted in Tier 3), Fiserv AI Eng,
  Oklahoma State Govt Jr DS, Zoom ML/AI Eng.

### Tier 1 — Hot & strong fit
_Entry-marked, recent (≤~2d calendar-dated), non-defense, non-FAANG, strong
applied-AI/data fit. Visa buckets inferred (JDs all 000/403)._

| Company | What they do / size | Role | Direct link | Posted (basis) | Visa posture | Fit note | Source |
|---|---|---|---|---|---|---|---|
| New York Life | Life insurance; large mutual | Associate - AI Engineer | https://jobright.ai/jobs/info/6a3e3b9b78237a036d5e3960 | Jun 26 (1d, jobright cal) | Silent, larger company — **verify** | **Explicit "Associate" + "AI Engineer"** = exact entry applied-AI rung at a large insurer (distinct from the already-logged NYL "Associate – Data Scientist"); NYC; gap: large-co policy unread | jobright ENG |
| Gen Digital (Norton/Avast/LifeLock) | Consumer cyber-safety software; large public (~3k) | Machine Learning Engineer I | https://jobs.ashbyhq.com/gen-digital/04d8f8b7-135c-4b93-8dbb-f47b9ddb51ea/application | 1d (zapply age) | **✅ Sponsor** (zapply Visa col) → likely OPT-OK, verify | **Explicit "I" entry** ML Engineer + company flagged as an active sponsor; Mountain View; consumer-AI/ML fit; gap: seniority is the only entry marker, JD unread | zapply DS |

### Tier 2 — Worth a look (good fit; caveat = seniority and/or visa unverified, JD 000/403)

| Company | What they do / size | Role | Direct link | Posted (basis) | Visa posture | Fit note | Source |
|---|---|---|---|---|---|---|---|
| Monte Carlo | Data-observability SaaS; growth-stage unicorn | Applied Forward Deployed Engineer (FDE) | https://jobright.ai/jobs/info/6a0b59364d9320363687003c | Jun 24 (3d, jobright cal) | Silent, growth-stage — likely OK (but ~unicorn → verify) | **"Forward Deployed Engineer" = bullseye target title**, and **commercial + Remote US**; data-platform deployment maps to the candidate's data-eng + RAG work; gap: seniority unverified (FDE often wants some customer-facing exp) | jobright ENG |
| Baseten | ML-model inference/deployment platform; growth-stage | Applied AI Inference Engineer · AI Solutions Engineer | https://jobright.ai/jobs/info/69e7db2658811370cb11ec8f (Applied AI Inference, SF) · https://jobright.ai/jobs/info/69e8057e3aa0c4796439d2cb (AI Solutions Eng, NYC) | Jun 23 (4d) / Jun 22 (5d) | Silent, growth-stage — likely OK | **Both are bullseye applied-AI titles** at a model-serving infra startup — direct match to the LLM/RAG-deployment profile; gap: seniority unverified | jobright ENG |
| Ironclad | Contract-lifecycle-management (CLM) AI SaaS; growth-stage unicorn | Finance Systems & AI Engineer | https://jobs.ashbyhq.com/ironcladhq/29f8753e-5ff4-4bfd-9e83-b6ee6c2e8293/application | 1d (zapply age) | **✅ Sponsor** (zapply Visa col) → likely OPT-OK, verify | AI embedded in a business-systems title at an AI-first SaaS; SF; applied-AI + data fit; gap: finance-systems niche + seniority unverified | zapply DS |
| Ro | Telehealth / direct-to-patient healthcare; growth-stage unicorn | AI Engineer | https://jobs.lever.co/ro/0b6ded09-e358-4e39-a428-a2cbf6b15cda/apply | 15h first-seen (≈within window) | **✅ Sponsor** (zapply Visa col) → likely OPT-OK, verify | "AI Engineer" target title at a consumer-health unicorn flagged as a sponsor; NYC; applied-AI fit; gap: seniority unverified, recency is a scraper stamp | zapply DS |
| The Hanover Insurance Group | P&C insurer; large public | Associate Data Engineer (REMOTE) | https://jobright.ai/jobs/info/6a3d74d5122f340d29cf0a72 | Jun 25 (2d, jobright cal) | Silent, larger company — **verify** | **Explicit "Associate" + Remote** Data Engineer — clean dbt/Airflow/SQL entry fit; gap: insurance domain, large-co policy | jobright ENG |
| Brown & Brown Insurance | Insurance brokerage; large public | Junior Data Engineer (Remote, USA) | https://bbinsurance.wd1.myworkdayjobs.com/careers/job/Remote---USA/Junior-Data-Engineer_R26_0000002276 | 1d (zapply age) | Silent, larger company — **verify** | **Explicit "Junior"** Data Engineer (distinct req from the already-logged unmarked Brown & Brown DE R26_0000002275); Remote; dbt/SQL fit | zapply DS |
| Housecall Pro | Field-service-business SaaS; growth-stage | Graduate AI Solutions Analyst | https://jobright.ai/jobs/info/6a0b55a74d9320363686fb4d | Jun 26 (1d, jobright cal) | Silent, growth-stage — likely OK | **"Graduate" + "AI Solutions" = entry Forward-Deployed/AI-Solutions-adjacent** target; Remote; gap: solutions/enablement-leaning vs pure build | jobright ENG |
| SewerAI | Infrastructure-inspection AI (sewer/pipe CV); startup | Junior Analytics Engineer | https://jobright.ai/jobs/info/6a3f101f4d047136e0938af1 | Jun 26 (1d, jobright cal) | Silent, small startup — likely OK | **Explicit "Junior" + "Analytics Engineer" exact target title** at a small AI startup (low visa risk); Walnut Creek CA; dbt/SQL fit | jobright ENG |
| AEG (Anschutz Entertainment Group) | Live-entertainment/sports & venues; large private | Associate Data Scientist | https://jobright.ai/jobs/info/6a3d8ace4d047136e093418a | Jun 25 (2d, jobright cal) | Silent, larger company — **verify** | Entry "Associate" DS; LA; analytics/ML fit; gap: entertainment-ops domain, GenAI angle | jobright DA |
| Teamworks | Sports-team operations SaaS; growth-stage | Data Engineer 1 | https://jobs.ashbyhq.com/teamworks/317433d0-072d-40ac-822f-0e268fa6b4c3/application | 25d (Simplify age) | Silent, growth-stage — likely OK | **Explicit "1" entry** Data Engineer at a SaaS startup (low visa risk); North Carolina; dbt/SQL fit; gap: window-edge recency | Simplify (dev) |
| The Nature Conservancy | Environmental nonprofit; large | Junior Data Analyst/Developer | https://jobright.ai/jobs/info/6a3d85bd882f121f56a37e12 | Jun 25 (2d, jobright cal) | Silent, nonprofit — likely OK | **Explicit "Junior"** Data Analyst/Developer; Arlington VA; SQL/BI fit; gap: nonprofit-ops analytics vs AI-eng | jobright DA |
| Xcel Energy | Electric & gas utility; large public | Associate Data Scientist - Distribution | https://jobright.ai/jobs/info/6a3f0dbe78237a036d5e6679 | Jun 26 (1d, jobright cal) | Silent, larger company — **verify** | Entry "Associate" DS; Twin Cities; grid/asset anomaly-detection = good applied-analytics fit; gap: utility domain, GenAI angle | jobright DA |
| Fieldguide | Audit/advisory-automation AI SaaS; growth-stage | AI Engineer | https://jobright.ai/jobs/info/6a1dca783e538a28c204bdab | Jun 22 (5d, jobright cal) | Silent, growth-stage — likely OK | "AI Engineer" target title at an applied-AI startup; SF; strong stack fit; gap: **seniority unverified** (no entry marker) | jobright ENG |
| AI Fund | Andrew Ng's AI venture studio; small | AI Engineer · Applied AI Engineer | https://jobs.lever.co/AIFund/01654e18-7b7f-4f0d-84b4-9e090fbc73be/apply (Applied AI) · https://jobs.lever.co/AIFund/33bd1d6c-5091-42f8-99c0-6e97292782be/apply (AI Eng) | 19h–1d first-seen (≈within window) | Silent, small — likely OK | **"Applied AI Engineer" exact target title** at a hands-on AI studio; Mountain View; strong stack fit; gap: seniority unverified, studio roles can skew senior | zapply DS |
| PROS Holdings | Pricing/revenue-optimization SaaS; mid-large public | Machine Learning Engineer 1 | https://simplify.jobs/c/PROS-Holdings-Inc (Simplify redirect — **no direct ATS link captured**) | 16d (Simplify age) | Silent, larger company — **verify** | **Explicit "1" entry** ML Engineer; Bangor ME (also remote?); applied-ML fit; gap: no direct ATS link (find before applying) | Simplify (dev) |
| University of Texas at Austin | Public university; large | Data Engineer 1 | https://simplify.jobs/c/University-Of-Texas-Austin (Simplify redirect — **no direct ATS link captured**) | 15d (Simplify age) | Silent, university — likely OK (universities often OPT-friendly) | **Explicit "1" entry** Data Engineer; **Austin TX (≈in-state, near-local)**; dbt/SQL fit; gap: no direct ATS link captured | Simplify (dev) |
| Bonterra | Social-good / nonprofit-CRM software; large private | Data Engineer 1 - Data Services | https://simplify.jobs/c/Bonterra (Simplify redirect — **no direct ATS link captured**) | 15d (Simplify age) | Silent, larger company — **verify** | **Explicit "1" entry** Data Engineer; **Remote (USA)**; dbt/SQL fit; gap: no direct ATS link captured | Simplify (dev) |

### Tier 3 — Long shots / needs verification / seniority or domain risk

| Company | What they do | Role | Direct link | Posted | Visa posture | Why Tier 3 | Source |
|---|---|---|---|---|---|---|---|
| Palantir | Data/AI platforms (Gotham/Foundry); large public | Forward Deployed Software Engineer, New Grad | https://jobs.lever.co/palantir/cbe90327-3e6e-451c-a54c-1d3cbcef5aeb/apply (DC) · NYC variant: https://jobs.lever.co/palantir/d1ac83d0-e923-42a5-8e6d-58dd0cab25ca/apply | 10d (Simplify age) | **Verify — likely restrictive** (heavy USG/defense work → many Palantir FDE roles are US-person/clearance-gated, esp. DC) | **FDE New Grad = bullseye title**, commercial-track exists, BUT Palantir's gov-heavy footprint makes US-person/clearance likely for the DC role; confirm the specific req is commercial before effort | Simplify (dev) |
| Loop | Logistics/freight-audit AI startup | AI Engineer | https://jobright.ai/jobs/info/6a29ff38c07d4b6ae1c43b2d | Jun 26 (1d, jobright cal) | Silent, startup — likely OK | "AI Engineer" at a startup (Loop already logged as new-grad SWE-AI); SF; **seniority unverified** (no entry marker) — parked here pending JD | jobright ENG |
| NOSO Labs (YC S25) | Early-stage YC AI startup | AI Engineer | https://jobright.ai/jobs/info/6a37510e29c90c607e4e63e2 | Jun 20 (7d, jobright cal) | Silent, seed startup — likely OK | YC-S25 seed co (low visa risk) BUT very early → role scope/seniority unclear; SF Bay; "Founding"-ish risk | jobright ENG |
| MeritFirst | AI/recruiting-tech (company opacity); small | AI Engineer | https://jobright.ai/jobs/info/6a38b41929c90c607e4e7ed6 | Jun 24 (3d, jobright cal) | Unclear — **verify** | Entry-plausible AI Eng, **Austin TX (≈in-state)**, but company opacity → confirm it's a direct FTE; seniority unverified | jobright ENG |
| Motorola Solutions | Public-safety comms/tech; large public | AI Solutions Developer | https://jobright.ai/jobs/info/6a3d59e14d047136e09331bb | Jun 24 (3d, jobright cal) | Unclear — **verify** | "AI Solutions" title fit BUT public-safety/LE-adjacent → possible background/citizenship constraints + seniority unverified; IL | jobright ENG |
| Northwestern University | Private university; large | Research Data Analyst Associate (1-year Term) | https://jobright.ai/jobs/info/6a3e845b122f340d29cf36a8 | Jun 26 (1d, jobright cal) | Silent, university — likely OK | Entry analyst (universities often OPT-friendly) BUT **1-year term** (not permanent FTE); Evanston IL; analytics fit | jobright DA |
| BlackRock | Asset management; large public | Associate, Modelling Data Scientist | https://blackrock.wd1.myworkdayjobs.com/blackrock_professional/job/Atlanta-GA/Associate--Modelling-Data-Scientist_R264834 | 2d (zapply age) | 🏛 H-1B Co. (zapply) → likely OPT-OK, verify | "Associate" rung DS (distinct from the several already-logged BlackRock Assoc reqs); Atlanta; modeling-heavy vs applied-GenAI; large-finance policy | zapply DS |
| CATHEXIS | Govt/enterprise data & AI consultancy; mid-size | Associate AI/ML Software Developer (req-261) | https://jobright.ai/jobs/info/6a3ee96c882f121f56a3bf7a | Jun 26 (1d, jobright cal) | Unclear — **verify** (govt consultancy → clearance/US-person plausible) | Entry "Associate AI/ML" title BUT CATHEXIS does federal/govt work (already flagged in prior excludes) → confirm commercial, not clearance-gated; Tysons VA | jobright ENG |

### Recency-unverified (strong fit, but no post date confirmable within 30 days)
_Surfaced via WebSearch; active postings but the listings carry no machine-readable
post date and JD bodies are 403/000, so per the honesty rule they are parked here
rather than placed in the dated tiers._
| Company | Role | Direct link | Note |
|---|---|---|---|
| FurtherAI (YC, a16z-backed) | Forward Deployed Engineer · AI Engineer, Agent Team | https://jobs.ashbyhq.com/furtherai/d2fb3438-c7ca-469a-81c7-d98cea49b0d2 (FDE) · https://www.linkedin.com/jobs/view/ai-engineer-agent-team-at-furtherai-4391525037 (AI Eng, Agent Team) | Insurance-AI-agents startup ($30M+ raised, a16z/YC); **FDE + agent-team AI Eng = near-perfect match** to the candidate's LangGraph/RAG flagship; SF (not remote). **Their "Software/AI Engineer (New Grad)" req was removed Mar 31 2026** (out of window) — these two are the currently-open ones, but neither carries a confirmable ≤30d post date. Strong informal lead; verify recency + visa on the page |

### Excluded (logged so future runs don't re-surface)
- **Stale / out-of-window:** **Domino Data Lab – Forward Deployed Engineer, New Grad 2026** (NYC) — a bullseye title, but it's a **2025 campus-recruiting-cycle posting** (one mirror shows it removed Jan 7 2026); not within the 30-day window. Re-check if Domino reopens it for the next cycle (careerpuck `app.careerpuck.com/job-board/domino-data-lab/job/7275081`).
- **FAANG-tier (referral track):** Amazon/AWS (Applied Scientist I/II/3, Quantum Applied Scientist), Microsoft (Applied Scientist), Google (AI Research Scientist Applied AI), Meta (Data Engineer – University Grad, Research Scientist Intern), TikTok/ByteDance (DS/MLE interns, Benefits Data Analyst), Apple, Netflix.
- **Defense / federal / clearance (US-person near-certain):** Booz Allen (Data Scientist Fort Meade/Arlington, Data Scientist Network Analyst), CACI (Data Scientist Crane IN, Data Analyst Chantilly/DC), Leidos (Transportation/Senior Data Scientist McLean/Springfield), Guidehouse (Data Scientist Huntsville/Arlington, Talent-Mgmt Data Analyst DC), General Atomics (Data Scientist I Charlottesville), Radiance Technologies (ML Engineer Beavercreek), RTX (Agentic AI Engineer Arlington), MetroStar (Associate Data Engineer), ITA International (Junior Data Analyst), MUFG (Global Red Team AI Engineer — security).
- **Non-US geography (F-1 OPT is US-only):** Baker Hughes (Early-Career AI Engineer Trainee, India), SOCAN/Publicis Canada (Jr DE / Jr DA, Canada), Bank of Montreal + TD Bank (Toronto), Bending Spoons (UK), Innodata GenAI Associate (French/Canada variants).
- **Trading-floor quant (profile wants non-trading-floor):** TransMarket Group (Junior Quantitative Trader, Chicago).
- **Annotation / language-gated / wet-lab:** Innodata (Generative AI Annotator, GenAI Red-Team English+French), Arrowhead Pharmaceuticals (Scientist, Computational Chemist & MLOps — wet-lab-adjacent), Thermo Fisher (Scientist II Data Scientist Bioprocess), Vertex/Kaiser research-scientist rows.
- **Senior / II+ / intern / co-op:** Expedia (ML Scientist II), Snap (DS Level 4), Oracle (Applied Scientist 3), Amazon (Applied Scientist II), Disney (DE II — prior run), ServiceNow/Zillow/Motorola/Analog Devices/Zoox ML-Eng (no entry marker, likely mid+), Nokia/TikTok/Tesla/W.R. Berkley/JM Family/Trane/Integra/Nuro/Schweitzer (interns/co-ops).
- **People Analytics / HR Data Analyst:** searched the open web; only aggregator pages (Indeed/ZipRecruiter/Glassdoor/jobgether) — no individual posting with a stable direct link + confirmable date → nothing loggable this run.

### Bonus — adjacent titles worth adding to the search vocabulary
- **"Applied Forward Deployed Engineer (FDE)" (Monte Carlo)** — confirms commercial FDE at a data-observability unicorn (not defense); reinforces FDE as a first-class commercial search term.
- **"Applied AI Inference Engineer" / "AI Solutions Engineer" (Baseten)** — model-serving-infra startup applied-AI titles; high-signal for the LLM/RAG-deployment profile.
- **"Finance Systems & AI Engineer" (Ironclad)** — AI embedded inside a business-systems title; easy to miss with a plain "AI Engineer" search.
- **"Graduate AI Solutions Analyst" (Housecall Pro)** — "Graduate"+"AI Solutions" entry FDE/Solutions-adjacent rung.
- **"Junior Analytics Engineer" (SewerAI) / "Data Engineer 1" (Teamworks, Bonterra, UT Austin) / "Machine Learning Engineer 1" (PROS)** — explicit entry rungs ("1"/"Junior") of exact target titles; keep "Data Engineer 1" and "ML Engineer 1" as search variants alongside "Associate/Junior".
- **✅ Sponsor / 🏛 H-1B Co. (zapply Visa column)** — Gen Digital, Ironclad, Ro all carry a `✅ Sponsor` company-level flag this run = the best authorization signal available given JDs are unreadable; prioritize `✅ Sponsor`-flagged cos when JD verification stays blocked.

### TODO for next (daily) run
- **USE curl + local parse, NOT WebFetch, for the GitHub trackers** (unchanged best practice — read all six in full this run).
- **AI/ML new-grad rows** live in `jobright-ai/2026-Engineering-New-Grad` (1.5 MB; there is NO `2026-AI-Machine-Learning-New-Grad` repo). `jobright-ai/2026-Data-Analysis-New-Grad` still caps at "last 7 days" — fine for a daily run, but for 30-day depth find its full Airtable/export.
- **JD/visa verification** unchanged #1 blocker: every ATS host (greenhouse/ashby/workday/oracle/lever via curl or WebFetch) = 000/403 (egress policy). All visa buckets inferred; lean on the zapply `✅ Sponsor`/`🏛 H-1B Co.` column as the only machine-readable authorization signal.
- **Community:** HN is **still the June thread `48357725`** as of Jun 27 — **the July 2026 "Who is hiring" thread should open ~Jul 1**; check for it next run (Algolia API + hnhiring + nchelluri mirror all still 000/403 to direct fetch — only WebSearch returns text, without per-post links).
- **Web leads to re-verify next run:** FurtherAI (FDE + Agent-team AI Eng — confirm recency/visa) and watch for Domino Data Lab's FDE New-Grad to reopen for the next cycle.

---
