# 24. One-time post check

**What it does:** Runs once, shortly after an important scheduled post goes out, and confirms it published. Tells you only if it failed.
**Schedule:** One time, about 30 minutes after the post's scheduled time.
**Posts:** A short line, or only on failure.
**Connectors:** Your social scheduler (read only).
**Cost:** Very low.
**Lives in:** Whichever channel owns the post.

## The prompt

```
Your watch on {{POST_DESCRIPTION}}. At {{POST_TIME}} on {{POST_DATE}}, these posts were scheduled in {{SCHEDULER}}: {{POST_LIST}}. Use the {{SCHEDULER}} tools to check whether those posts published today (recent posts or post status; posts due earlier today should no longer be in the schedule list). Post only if a post failed, is still stuck, or you can't check, starting with "Your watch on {{POST_DESCRIPTION}}:". If everything published, post one short line saying they went out fine. This is a one-time check. Change nothing in {{SCHEDULER}}.
```

## When to use it

- A client's launch post
- Graphics or carousels (more things can break)
- A post tied to a deadline or an event

Just ask: "Set a one-time check for 30 minutes after tomorrow's 8 AM client posts."
