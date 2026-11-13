# 23. Weekly meeting notes backup marker

**What it does:** Posts a marker every Friday. Your main chat has a thread copy any new meeting transcripts from your notetaker into a private repo, so you never lose them if you switch tools.
**Schedule:** `CRON_TZ={{YOUR_TIMEZONE}} 43 16 * * 5` (Fridays, 4:43 PM)
**Posts:** One marker line, handled quietly.
**Connectors:** Your meeting notetaker and GitHub, for the thread.
**Cost:** Low.
**Lives in:** Main chat.

## The routine prompt

```
You are the weekly trigger for {{YOUR_NAME}}'s meeting notes backup (Fridays about 4:43pm {{YOUR_TIMEZONE}}). On {{DATE}} they asked: "{{YOUR_WORDS}}" (for example: keep backing up any new meeting notes to this repo). This run can't reach GitHub, so you do not back anything up yourself. The main chat hands the work to a session that has the repo.

Do exactly one thing: post one short message with this text and today's date: "Meeting notes backup marker: time to back up new recaps to {{NOTES_REPO}} (YYYY-MM-DD)."

Read nothing, write no files, start nothing else.
```

## The memory rule

```
Remember: when the "Meeting notes backup marker" appears, hand it to a thread with {{NOTES_REPO}}: back up recaps and transcripts newer than .last-sync, same file naming, skip {{EXCLUDED_MEETINGS}} (for example: calls under NDA), update the index and .last-sync, commit to main. Don't relay the marker. Tell me only if it fails.
```

## First-time setup

Ask once: "Create a private repo {{NOTES_REPO}} and back up ALL of my meeting transcripts so far, with a README, an index file and a .last-sync file. Leave out {{EXCLUDED_MEETINGS}}."
