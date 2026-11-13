# 13. Client weekly report (advanced)

**Level:** Advanced (extra paid tools, GitHub or a client setup)
**What it does:** Every Monday at 8 AM, refreshes a client's weekly marketing report page and emails the client team a short note with the link. Holds and emails only you if anything goes wrong.
**Schedule:** `0 13,14 * * 1` in UTC, with a time guard (see below)
**Posts:** Emails, not chat posts.
**Connectors:** Gmail, GitHub (a repo with the report code), the data sources your report pulls from, a place to host the page.
**Cost:** Medium to high, depending on the report.
**Lives in:** That client's channel.
**Why advanced:** Needs a small code repo and a hosted page. Ask Claude to build those with you first.

## Why the time guard?

Cron with a time zone isn't available on every routine type. This one fires at both 13:00 and 14:00 UTC. One of those is 8 AM Central in winter, the other in summer. The first step checks the local hour and quits on the wrong run. Swap the hours and time zone for yours.

## The prompt

```
You refresh the {{CLIENT_NAME}} weekly marketing report every Monday at 8 AM {{YOUR_TIMEZONE_NAME}}. Do these steps in order.

Step 0, time guard: run "TZ={{YOUR_TIMEZONE}} date +%H". This routine fires twice so that one run lands on 8 AM local time in both standard and daylight time. If the output is not 08, reply exactly "Not 8 AM, nothing to do." and stop.

Step 1, already done?: check the report's state for this ISO week. If it shows published, reply "Already published this week." and stop.

Step 2, find the code: this session has the repo {{REPORT_REPO}} checked out; find the routine instructions file and work from the repo root. If a needed secret is empty, the report host can't be reached or the repo is missing, send ONE email to {{YOUR_EMAIL}}, subject "HOLD: {{CLIENT_NAME}} report could not start", plain text with the exact error and the most likely fix. Never print or include a secret. Then stop.

Step 3: follow the routine instructions file exactly. Nobody will answer questions: when anything is unclear, fails or is blocked, HOLD as that file says, which always means sending the HOLD email. Do not commit or push anything.

Step 4, notify the client: re-check the state. Only if it shows published AND this run published it AND you sent no HOLD email, send ONE email to {{CLIENT_RECIPIENTS}}, cc {{YOUR_EMAIL}}, subject "Your Updated {{CLIENT_NAME}} Weekly Marketing Report", plain text exactly as below, no additions:

Hi {{CLIENT_TEAM_NAME}}, / Your weekly marketing report is updated. You can view the numbers here: [report link] / As always if you have any questions just reply to this email. / {{YOUR_FIRST_NAME}}

If it is not published, or you sent a HOLD email, send nothing to the client. Never send more than one client email per run. If the client email fails, do not retry; send ONE email to {{YOUR_EMAIL}}, subject "Client was NOT notified: {{CLIENT_NAME}} report", with the error and "The page is updated; forward the link yourself."
```

## Tips

- Set this one up yourself in your routines settings, since it emails your client. You approve the recipients once, in your own words.
- Pair it with the report check (14) so you know by mid-morning if anything slipped.
- Keep the client email boring and identical every week. Clients like predictable.
