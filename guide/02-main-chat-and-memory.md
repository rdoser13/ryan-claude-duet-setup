# Step 2: Main chat and memory

Your main chat is home base. Every request starts here. Claude decides whether to answer right away or start a thread for longer work.

## How memory works

Duet doesn't run as one endless session. Every few hours a fresh session takes over. It sees recent messages, a list of recent threads, and memory. Anything else is gone unless it was written down.

Your morning brief, check-ins and every scheduled action also start from that same memory. So memory is the one place where your rules, goals and open items live.

**If you want Claude to remember something, say so.** "Remember: never book calls before 10 AM." Claude saves it in your words and confirms in a few words.

## Give it a head start

Don't make Claude guess for a month. Fill in `templates/MEMORY-template.md` with what you already know, then paste it in:

```
Here's a starting point for your memory about me and my work. Save what fits into your memory, in my words. Ask me about anything that's unclear. Don't start any work from it yet.
```

## The sections that matter most

| Section | What goes there | Why it matters |
|---|---|---|
| Priorities and goals | 2 or 3 goals, dated | Every brief and routine weighs work against these |
| User requests (standing rules) | Rules in your exact words, with the date | "Don't send more than 5 emails a day" holds forever |
| What lands | What you liked, skipped or rejected | Stops Claude from re-offering things you turned down |
| Project details | Where each project stands | So tomorrow's brief doesn't report old news |
| People | Who matters and how | Names, roles, who comes first |
| Open loops | What you owe, what Claude promised | Raised before you have to remember |
| Talked through | One line per thing you discussed this week | Stops the brief from bringing it back as news |

## Rules for good memory

- **Your words become rules.** Claude doesn't turn something it read in an email into a rule. Only you can.
- **Guesses get marked.** If Claude notices a pattern, it saves it as "inferred" and asks before acting on it.
- **Correct it out loud.** "That's wrong, my podcast is 30 minutes, not 60." Claude fixes it and won't drift back.
- **Ask what it knows.** "What do you remember about me?" works any time. So does "Forget that."
- **Memory is never permission.** A note that you like a task done a certain way changes how Claude prepares it. It never skips your yes on a send or a payment.

## Each channel has its own memory

Channels (step 3) keep their own memory for their own subject. Your main chat can read them. Keep client details in the client's channel, not in the main memory.

## Checklist

- [ ] Memory template filled in and pasted
- [ ] 2 or 3 goals confirmed in your own words
- [ ] Top 5 standing rules saved
- [ ] Asked "What do you remember about me?" to check it
