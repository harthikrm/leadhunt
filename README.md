# Lead Hunt — Daily Automated Job Lead Search

## What this does
Runs Claude Code once a day at 12:00pm, has it search for fresh FTE leads 
(AI/ML/Data roles, OPT-friendly, startups through mid-tier enterprises) 
posted in the last 24 hours, and appends results to `leads_log.md` with 
direct links. Never overwrites past runs — it's a running history.

## Files in this folder
- `prompt.md` — the task Claude Code runs each day. Edit this if you want 
  to change role targets, filters, or tiering.
- `leads_log.md` — the actual output. This is what you read every day.
- `run_history.log` — raw stdout/stderr from each run, for debugging if a 
  run fails or produces something odd. Not meant for daily reading.

## One-time setup

1. Make sure Claude Code is installed and you're logged into your 
   subscription plan (not API key billing):
   ```
   claude --version
   ```
   If this fails, install Claude Code first.

2. Open your crontab:
   ```
   crontab -e
   ```

3. Add this line (runs every day at 12:00pm machine time):
   ```
   0 12 * * * cd /full/path/to/leadhunt && claude --print "$(cat prompt.md)" >> run_history.log 2>&1
   ```
   Replace `/full/path/to/leadhunt` with the real path on your machine 
   (e.g. `/Users/harthikmallichetty/leadhunt`).

4. Save and exit. Confirm it's scheduled:
   ```
   crontab -l
   ```

## Important: this only runs if your machine is awake at 12pm
Cron does not wake a sleeping laptop. If your machine is asleep or shut down 
at noon, that day's run is silently skipped — no error, just nothing added 
to the log that day.

- **macOS**: you can allow scheduled wake with `pmset`, e.g.:
  ```
  sudo pmset repeat wakeorpoweron MTWRFSU 11:55:00
  ```
  This wakes the machine at 11:55am daily so the noon cron job has a chance 
  to run. (Test this — behavior varies by Mac model/macOS version.)
- **Linux**: similar capability via `rtcwake` or systemd timers with 
  `WakeSystem=true`, setup varies by distro.
- **Simplest fix**: just leave the machine on and awake (not asleep) around 
  noon each day. If it's a desktop that's normally on, you likely don't 
  need to do anything extra.

## Checking it's working
After the first scheduled run, check:
```
cat run_history.log
```
for errors, and:
```
cat leads_log.md
```
to see if a new `## Run:` entry was appended with today's date.

## Usage / cost note
Each run does multiple web searches and page fetches across several sites — 
this is a moderately expensive session, not a quick chat. Watch your plan's 
usage after the first few runs to confirm daily cadence is sustainable. If 
usage is higher than expected, the easiest lever is narrowing the role list 
or source list in prompt.md, not changing the schedule.

## Adjusting later
- Want a different time? Change `0 12 * * *` (minute hour day month weekday 
  in cron syntax).
- Want to pause? Comment out the line in crontab with a `#` rather than 
  deleting it, so you don't lose the schedule config.
- Want to widen back to a 7-day window instead of 24-hour? Edit the 
  RECENCY section in prompt.md — useful for the very first run, since "last 
  24 hours" on day one means very little has accumulated yet.
