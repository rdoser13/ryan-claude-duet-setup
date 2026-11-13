# 22. Daily GitHub backup marker

**Level:** Advanced (extra paid tools, GitHub or a client setup)
**What it does:** Posts one marker line each night. Your main chat sees it and has a thread with GitHub access write the day's log and back up your setup to your private repo.
**Schedule:** `CRON_TZ={{YOUR_TIMEZONE}} 17 20 * * *` (daily, 8:17 PM)
**Posts:** One marker line. Your main chat handles it without bothering you.
**Connectors:** None for the routine. GitHub for the thread that does the work.
**Cost:** Very low for the marker. Low to medium for the backup itself.
**Lives in:** Main chat.

## The routine prompt

```
You are the nightly trigger for {{YOUR_NAME}}'s Claude Duet daily work log (about 8:17pm {{YOUR_TIMEZONE}}). They asked for a daily log in the repo {{REPO}} on {{DATE}}. This run can't reach GitHub, so you do not write the log yourself. The main chat hands the writing and the commit to a session that has the repo.

Do exactly one thing: post one short message in this channel with this text and today's date in place of YYYY-MM-DD: "Daily log marker: time to write and commit duet-daily-logs/YYYY-MM-DD.md."

Read nothing, write no files, start nothing else. If posting fails, end the run.
```

## The memory rule that makes it work

Paste this into your main chat so it knows what to do when the marker appears:

```
Remember: when the "Daily log marker" post appears, export my scheduled tasks tracker, then hand the backup to a thread that has {{REPO}}: write today's log in the CHECKED / INFERRED / UNKNOWN format, add up to 5 KB edits to queue/KB-EDITS.md, refresh scheduled-tasks/, copy my memory with contact emails stripped to duet-memory/, copy notes files that changed today, and commit to main. No secrets, codes, account numbers, contact details, health details or client data under NDA. Don't relay the marker. Tell me only if the commit fails.
```

## Tips

- See guide step 7 for the full backup setup and the log format.
