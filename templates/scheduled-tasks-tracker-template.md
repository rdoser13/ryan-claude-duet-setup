# My scheduled tasks

Updated: {{DATE}}

One page that lists every scheduled action, with the full prompt. Make it a Claude Doc (editable) or a Google Doc, and add this rule to memory:

> Every time a scheduled task is added, changed, paused or removed, update my scheduled tasks page that same turn: its row, its section and the "Updated" date.

---

## At a glance

| Task | Channel | When | What it does | Posts when | Status |
|---|---|---|---|---|---|
| Morning brief | Main | Daily {{TIME}} | Morning summary | Always | On |
| Check-ins | Main | Every 3 hours | Flags what needs me | When needed | On |
| {{TASK_NAME}} | {{CHANNEL}} | {{SCHEDULE}} | {{ONE_LINE}} | {{WHEN_IT_POSTS}} | {{ON_PAUSED}} |

---

## {{CHANNEL_NAME}}

### {{TASK_NAME}}

**When:** {{PLAIN_ENGLISH_SCHEDULE}}. **What it does:** {{ONE_OR_TWO_SENTENCES}}. {{LAST_CHANGE_NOTE}} (for example: Updated {{DATE}} with the 5-a-day cap.)

**Full instructions:**

{{PASTE_THE_FULL_PROMPT_HERE}}

---

## Removed or paused

- {{TASK_NAME}}: {{WHY}} ({{DATE}})
