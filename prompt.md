You are running an autonomous, time-boxed job-lead sourcing pass for Harthik 
Royal Mallichetty. This is a RECURRING daily run. Before doing anything else, 
read leads_log.md in this same folder in full — it contains every lead found 
in all prior runs. Do not re-surface anything already logged there with the 
same company + role + link.

GOAL: Find fresh full-time (FTE) job leads posted in the last 24 hours that 
fit the candidate profile below. Do one thorough pass across your sources, 
then stop and log. Do not run indefinitely — a complete pass is the success 
condition, not a time limit.

=== CANDIDATE PROFILE ===
- MS Business Analytics & AI, UT Dallas (May 2026, GPA 3.81). BTech Computer Science.
- Work authorization: F-1 OPT, valid 36 months starting July 13, 2026 — 
  requires NO employer sponsorship during that window. This is the single 
  most important filter, detailed below.
- Core stack: Python, RAG pipelines, LangGraph/LangChain, LLM fine-tuning 
  (QLoRA, Mistral-7B), pgvector/vector search, dbt, Airflow, FastAPI, GCP, 
  SQL, TypeScript/React, Docker.
- Flagship work: a live production RAG/financial-intelligence platform with 
  real users, and a fine-tuned open-source LLM for code review (QLoRA on 
  Mistral-7B, benchmarked against GPT-4o-mini). Also solo-built production 
  ML deployed at a prior employer (still in use 2 years later), plus data 
  engineering/analytics projects (dbt, Airflow, anomaly detection, BI 
  dashboards).
- Profile skews toward applied AI engineering — shipping real end-to-end 
  systems — not pure research, not pure backend.
- Location: Richardson, TX. Open to remote and to relocation for strong roles.

=== TARGET ROLE TITLES — search for ALL of these ===
AI Engineer · ML Engineer · GenAI Engineer / LLM Engineer · Applied AI 
Engineer · Applied Scientist (new grad/entry-level) · Data Engineer · 
Analytics Engineer · Data Analyst · BI Engineer / BI Developer · MLOps 
Engineer (entry-level) · Forward Deployed Engineer / Forward Deployed AI 
Engineer · AI Solutions Engineer · Machine Learning Engineer, New Grad · 
Quantitative Data Analyst (non-trading-floor) · People Analytics / HR Data 
Analyst

Entry-level / new-grad / junior only — 0-2 years experience asked for. 
Exclude senior/staff/lead/principal.

=== HARD FILTERS — apply during the search ===

1. VISA — the critical filter. Exclude any posting with "must be authorized 
   without sponsorship," "no sponsorship now or future," "US citizen/GC 
   required," clearance requirements, or equivalent. For every lead 
   returned, classify visa posture as one of:
   - OPT-friendly (explicit) — JD or company page says they sponsor/support 
     OPT or visa transfers
   - Silent, small/startup (treat as likely OK) — no mention, company small 
     enough that formal immigration policy is unlikely to be a blocker
   - Silent, larger company (verify before applying) — no mention, but 
     company is large/established enough to likely have a real immigration 
     policy not stated in the JD — flag for manual check, don't assume green
   - Unclear/conflicting

2. COMPANY STAGE — widened. Include seed through growth-stage startups AND 
   established mid-tier-to-large enterprises, excluding only FAANG-tier 
   companies (Google, Meta, Amazon, Apple, Microsoft, Netflix), which are 
   handled separately via referral. Everything else is in scope.

3. RECENCY — tight window. Only include leads posted/reposted within the 
   last 24 hours. State the post date/time or your best-evidence estimate 
   for each. Anything you can't verify as this recent goes in a separate 
   "Recency unverified" section, not the main tiers.

=== WHAT TO RETURN FOR EACH LEAD (non-negotiable fields) ===
- Company name, one line on what they do, size/stage if findable
- Role title
- DIRECT LINK to the posting (the actual URL — never paraphrase a link or 
  say "found on LinkedIn" without the real URL; if you cannot find a stable 
  direct link, say so explicitly rather than omitting the link silently)
- Post date/time (or estimate + basis)
- Visa posture bucket
- One-line fit note (why it matches, and the most obvious gap if any)
- Source (LinkedIn / Indeed / Reddit / HN / Wellfound / company site / 
  community board / other)

=== TIERS ===
- Tier 1 — Hot & strong fit: recent, OPT-friendly or low-risk-silent, 
  strong stack/role match
- Tier 2 — Worth a look: good fit with one caveat (visa needs verifying, 
  slight stack mismatch, recency fuzzy)
- Tier 3 — Long shots / needs verification

=== COMMUNITY BOARDS ===
Check whichever subreddits/Discord/Slack communities/forums you've 
identified as currently active in prior runs (see leads_log.md history). If 
this is your first run or the prior list seems stale, do a quick check of 
which are still active (real posts/engagement in the last 1-2 weeks) before 
relying on them, and note any that have gone dead so future runs skip them.

Also capture informal leads: LinkedIn posts from founders/hiring 
managers/recruiters announcing they're hiring (not formal listings), and 
forum/Discord posts where someone is directly asking for an FTE hire 
matching this profile. Capture poster name/title and the direct link.

Flag any adjacent role titles encountered that aren't on the list above but 
plausibly fit this background, as a bonus "consider expanding search to" note.

=== HONESTY REQUIREMENT ===
If a site blocks or rate-limits you, say so explicitly and state what you 
couldn't cover. Do not invent postings, links, or dates. If unsure whether a 
lead is real/current, put it in Tier 3 with a reason. A smaller list of 
verified leads with working links beats a long padded one.

=== LOGGING — READ CAREFULLY ===
1. Cross-check every candidate lead against the FULL contents of 
   leads_log.md (all prior runs) before including it. Skip exact repeats 
   (same company + role + link).
2. Append your findings to leads_log.md under a new header in this exact 
   format:

## Run: YYYY-MM-DD HH:MM

Then your tiered findings as a markdown table per tier, each row containing 
all the non-negotiable fields above, link included as a markdown link.

3. Do NOT overwrite or delete any prior run's content in leads_log.md. 
   Append only.
4. If a full pass turns up nothing new since the last run, append a short 
   entry saying so explicitly (with what you checked) rather than 
   padding the log with repeats.
5. End your turn cleanly once the pass is complete and logged to 
   leads_log.md. Do not start additional search cycles beyond one 
   thorough pass.
