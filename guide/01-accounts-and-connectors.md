# Step 1: Accounts and connectors

Claude Duet can only help with what it can see. Connectors are the apps you link to your account. Start small, then add more as your routines need them.

## The core 5 (connect these first)

| Connector | What it unlocks |
|---|---|
| Gmail | Morning brief, check-ins, reply drafts, receipt saving, reporter scans |
| Google Calendar | Call prep, podcast prep, week in review, "what's next" in check-ins |
| Google Drive | Saving files, reading call notes, receipts folder |
| Google Docs and Sheets | Prep docs, content runs, trackers and scorecards |
| Claude Docs | Living docs Claude writes and updates in place (your tracker page lives here) |

With just these, the morning brief, check-ins, call prep and week in review all work.

## Add as you grow

| Connector | Used by | Notes |
|---|---|---|
| Social scheduler with an MCP (I use Blotato) | X drafts, performance check, client social routines | Claude reads and schedules. You approve every post |
| Email platform (I use Kit) | Newsletter scorecard, email drafts | Keep it read-only in routines |
| Podcast studio (I use Riverside) | Guest prep, transcripts for content | Never let a routine send guest invites |
| Scheduling tool (I use Calendly) | Call recaps, transcript backups | Notetaker recaps are great content fuel |
| Mention monitoring (I use AlertMouse) | Brand mentions scan | Set up alerts in the tool first |
| SEO data (I use DataForSEO) | SERP and YouTube checks | Pay per call, so keep queries tight |
| Web scraping (Firecrawl, Apify) | Pages that normal fetch can't read | Use only when web fetch fails. Credits go fast |
| GitHub | Backups, skill files, code projects | Routines can't reach it directly (see step 7) |
| Accounting (QuickBooks) | Bookkeeping help | Read first. Make changes only on your word |

## Setup tips that saved me hours

**Set your sending address once.** If you send from a business domain through Gmail, make it Gmail's default "Send mail as" address. Then tell Duet: "My business email should always be the one used for outreach." Drafts will come from the right address every time.

**Say no to connectors you won't use.** When Duet offers a connector you don't need, tell it "Don't use a connector for this." It will stop offering.

**Protect your scraping credits.** Add a standing rule: "Use web fetch and web search first. Only use Firecrawl when a page can't be read any other way." Put the same line in every routine that browses.

**Give Gmail permission to change mail** if you want routines to archive or label. Without it, reads work but archiving fails.

**Media for social posts from the cloud.** Cloud sessions can't upload a local file to most schedulers. What works: save the image to Google Drive, share it as "anyone with the link can view", and pass that link to the scheduler, which copies it in. Unshare the folder once posts go out.

## Your always-on machine (optional, advanced)

Some jobs need your own computer: your signed-in browser, big video files, local tools like ffmpeg. An old laptop or a Mac mini that stays on can serve those through Remote Control or Claude in Chrome. Skip this until a routine actually needs it.

## Checklist

- [ ] Core 5 connected
- [ ] Sending address set in Gmail
- [ ] Scraping credits rule saved
- [ ] One connector added per routine that needs it, not before
