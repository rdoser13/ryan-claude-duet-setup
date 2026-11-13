# Step 7: Backups to GitHub

Your setup lives in chats, memory and routine prompts. If you ever need to rebuild, move to another tool or hand it to a teammate, you want it all in one place you own. A private GitHub repo is that place.

## What gets backed up

| Folder in your backup repo | What goes in it | How often |
|---|---|---|
| `duet-daily-logs/` | One log per day: what got done, with evidence | Daily |
| `scheduled-tasks/` | A copy of your scheduled tasks tracker doc | Every time it changes, plus daily |
| `duet-memory/` | A copy of your main chat memory, with contact details stripped | Daily |
| `notes/` | Working files that changed that day (style guides, logs) | Daily |
| `queue/` | Your to-do queues, like KB-EDITS (fixes for your knowledge base) | Daily |

## Step by step

1. **Create a private repo** on GitHub. Call it something like `{{YOUR_NAME}}-duet-backup`.
2. **Connect GitHub** in Claude Duet and make sure the Claude GitHub App is installed on that repo.
3. **Ask the main chat to set it up:**

```
Set up {{REPO}} as my command center. Create a README, the folders duet-daily-logs, scheduled-tasks, duet-memory, notes and queue, and an EXCLUDED.md that lists what never gets backed up. Commit to main.
```

4. **Add the marker routine** (template: `scheduled-actions/22-daily-github-backup-marker.md`). It posts one line each night.
5. **Save the standing rule in memory** so your main chat knows what to do when the marker shows up:

```
Remember: when the "Daily log marker" post appears, hand the backup to a thread that has {{REPO}}. It writes today's log, refreshes scheduled-tasks/ from my tracker doc, copies my memory with contact emails removed, copies notes files that changed today, and commits to main. No secrets, codes, account numbers, contact details, health details or client data under NDA. Don't tell me about the marker. Tell me only if the commit fails.
```

## Why a marker?

Scheduled routines can't reach GitHub directly. So the routine just posts a short marker line. The main chat sees it and hands the real work to a thread that does have GitHub. Same trick works for any tool a routine can't reach.

## The daily log format

Ask for logs in a format that separates proof from guesses:

```
# Claude Duet daily log: {{DATE}}
Timezone: {{YOUR_TIMEZONE}}
Coverage: main chat, threads and channels active today
Purpose: a record of what got done, for audits and rebuilding

## Evidence standard
CHECKED = seen done in a tool or page. INFERRED = likely, not verified. UNKNOWN = couldn't tell.

## Completed outcomes
- CHECKED: Scheduled 2 X posts for tomorrow at 9:00 AM and 3:30 PM.
- INFERRED: Weekly report email reached the client team (sent mail shows it, no reply yet).

## Open items
- ...

## Changes to scheduled tasks
- ...
```

## The KB edits queue

Every day, Claude notices things in your knowledge base or skills that are wrong or out of date. Instead of fixing them silently, it queues them for you in `queue/KB-EDITS.md`, up to 5 a day:

```
- [ ] KB-001 · {{DATE}} · skills/x-posts · says 4 slots, actually 3 · change to 3 · pick-log shows 3 slots used all month · open
```

You review the queue weekly and say which to apply.

## Backing up meeting notes

If you use a meeting notetaker (I use Calendly's), back up the recaps to a second private repo on a weekly marker. Then you can leave that tool without losing a single transcript. Template: `scheduled-actions/23-weekly-meeting-notes-backup-marker.md`. Keep a `.last-sync` file in that repo so each run only grabs what's new.

## What never gets backed up

Write these into `EXCLUDED.md` and into the standing rule:

- Passwords, API keys, tokens, sign-in codes
- Card numbers, bank or account numbers
- Email addresses and phone numbers of other people
- Health details
- Any client data under NDA. Name the clients and the people whose calls stay out.

## Checklist

- [ ] Private backup repo created and connected
- [ ] Daily marker routine on
- [ ] Standing rule saved in memory
- [ ] EXCLUDED.md written
- [ ] First daily log committed
