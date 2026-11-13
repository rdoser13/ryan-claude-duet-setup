# Step 9: Make it yours

Every template in this repo has `{{PLACEHOLDERS}}`. Fill them with your details, then paste.

## The placeholder list

| Placeholder | What to put |
|---|---|
| `{{YOUR_NAME}}` | Your name |
| `{{YOUR_TIMEZONE}}` | Your time zone, like America/New_York |
| `{{YOUR_EMAIL}}` | The address drafts should come from |
| `{{PERSONAL_EMAIL}}` | Where routines email you drafts and reminders |
| `{{X_HANDLE}}` | Your X handle |
| `{{SCHEDULER}}` | Your social scheduler (I use Blotato) |
| `{{SCHEDULER_ACCOUNT}}` | Which account in the scheduler to use. Have Claude list your accounts and pick. |
| `{{TRACKER_SHEET}}` | The name of your tracker Google Sheet |
| `{{REPO}}` | Your private backup repo |
| `{{WEBSITE}}` | Your site |
| `{{YOUTUBE_CHANNEL}}` | Your channel URL |
| `{{PODCAST_NAME}}` | Your podcast |
| `{{STUDIO}}` | Your recording studio (Riverside, etc.) |
| `{{COMMUNITY}}` | Your paid community, if any |
| `{{TOPICS}}` | 5 to 8 topics you're known for |
| `{{OFFERS}}` | What you sell |
| `{{CREDIBILITY_LINE}}` | One line of proof, checked against your about page |
| `{{SIGNATURE}}` | Your email signature |
| `{{CLIENT_NAME}}` | A client's name, for client routines |
| `{{SLOTS}}` | Your daily posting times |
| `{{DATE}}` and `{{YOUR_WORDS}}` | The date you asked, and what you said. Quote yourself. |

## Let Claude fill them in

The fastest way:

```
Here's a scheduled action template. Fill in every {{PLACEHOLDER}} from what you know about me. List any you can't fill and ask me for them. Don't create anything until I say yes.

[paste the template]
```

## Rename, drop and add

- **Rename freely.** "AI news memes" can become "industry news memes" or "funny takes on today's trend".
- **Drop what doesn't fit.** No podcast? Skip the guest prep. No clients? Skip the client folder.
- **Add your own.** Use the anatomy in step 5 and the shape of any template here.

## Using another agent?

The ideas here work beyond Claude Duet. Dots, Grok, Muse and most agent apps have some mix of memory, schedules and connectors. Map them like this:

| This repo says | Look for |
|---|---|
| Main chat | Your agent's main conversation |
| Channel | Projects, spaces or workspaces |
| Memory | Memory, custom instructions or a knowledge file |
| Scheduled action | Scheduled tasks, automations, cron jobs |
| Connector | Integrations, MCP servers, plugins |
| Skill | Skills, saved prompts, custom GPT instructions |
| post_message | However the agent messages you |

The prompts are plain English. Most of them work anywhere with small edits.
