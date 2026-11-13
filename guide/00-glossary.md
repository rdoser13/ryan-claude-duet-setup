# Glossary

Plain meanings for the words used in this repo.

**Claude Duet:** The app. You text Claude like a chief of staff, and it does the work.

**Connector:** An app you link to Claude Duet, like Gmail or Google Calendar. Claude can only see and use what you connect.

**MCP:** Short for Model Context Protocol. It's the plug that lets Claude talk to another app. When a tool says it "has an MCP", Claude can connect to it.

**Main chat:** Your home base in Claude Duet. Every request starts here.

**Channel:** A separate chat for one big area, like a client or your podcast. It has its own memory and tasks, so your main chat stays clean.

**Thread:** A side conversation where Claude does one longer job. It reports back when it's done. You can open it to follow along, but you don't have to.

**Task:** One thing you want done. The Tasks page shows each one as Working, Ready for you, Stopped or Resolved.

**Scheduled action (routine):** A job that runs on a timer, like every Monday at 10 AM. It starts fresh each time, does its job, and messages you only when something needs you. "Scheduled action", "scheduled task" and "routine" all mean the same thing here.

**Memory:** Notes Claude keeps about you, your rules and your work. Every session and every scheduled action reads it. If you want Claude to remember something, say "Remember..."

**Skill:** A saved set of instructions Claude loads before a job, like your writing style or your podcast question template. Skills keep the quality the same every time.

**Placeholder:** A blank in a template, written like `{{YOUR_NAME}}`. Replace it with your own details, or let Claude fill it in.

**Marker:** A one-line message a scheduled action posts to hand work to your main chat. Used when the routine can't reach a tool itself, like GitHub.

**Cron:** The format for a schedule. `CRON_TZ=America/New_York 37 15 * * 5` means "3:37 PM every Friday, New York time." You never have to write it yourself. Just tell Claude the time in plain words.

**Quiet hours:** The hours Claude never messages you.

**Stop condition:** A rule that pauses a scheduled action when it keeps failing or keeps finding nothing. It protects your usage.

**Usage:** How much of your Claude plan you've used. Every scheduled action run uses a little.
