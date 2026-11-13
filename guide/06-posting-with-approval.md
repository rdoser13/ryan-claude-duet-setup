# Step 6: Posting with approval

The posting workflow is simple: Claude drafts, you pick, Claude schedules. Nothing goes live without you.

## The daily loop

1. **4:17 PM:** the X drafts routine writes 2 to 4 drafts for tomorrow from your own material (videos, blog posts, podcast transcripts, call notes). It emails them to you and posts them in your main chat with a proposed time slot for each.
2. **You reply** with the numbers you want, plus any edits. "Post 1 and 3. Change the hook on 3 to..."
3. **Claude schedules** your picks in your social scheduler at the proposed slots, and logs them.
4. **Monday:** the performance check pulls the numbers and updates your log, so next week's drafts lean into what worked.

## Why it works

**Two log files make it smarter every week:**

- `pick-log.md`: every draft, whether you picked, skipped or rejected it, and your edits. Template in `templates/logs/`.
- `performance-log.md`: what actually performed once posted. Template in `templates/logs/`.

The drafts routine reads both before writing. Over a few weeks, it learns your taste and what your audience rewards.

**A tracker sheet for the big picture.** My setup uses one Google Sheet with tabs for each channel (X picks, X performance, YouTube, Shorts, LinkedIn, newsletter) and a patterns tab. Routines update it weekly. Email and content agents read the patterns tab before drafting.

## Your time slots

Pick 3 or 4 fixed slots a day and save them in memory, for example 9:00 AM, 12:15 PM, 3:30 PM and 7:30 PM. Then "schedule my picks" needs no back and forth. Add the rule "never two posts in the same minute, no two posts on the same topic or format back to back."

## Graphics

Save a graphics style guide with your rules. Mine include: official tool logos, my headshot, my logo on every graphic, no glowing "AI look", interesting backgrounds, always 3 options. Ask for "graphic: receipt" style images for cost breakdowns and "old way vs my way" for swaps.

## Memes on viral news

When AI news goes viral, speed wins. My meme watch runs twice a day, finds the one story everyone is talking about, and makes 3 meme options on famous templates. After my review and pick, Claude posts it. Template in `scheduled-actions/05-viral-news-memes.md`. Style guide in `templates/style-guides/meme-style-guide.md`.

## Cross-posting

Some posts work on LinkedIn too. Tell Claude which ones and ask for them "properly formatted for LinkedIn": shorter lines, no X-only references, a clear first line. Never auto-cross-post everything.

## Quality gates before anything reaches you

Every draft passes through:

1. Your **personal brand skill** (voice rules, banned words, platform limits).
2. An **anti-slop** pass that strips AI fluff.
3. A **critic** pass that judges the hook and topic, not just the wording.

Drafts that still fail get dropped. Getting 3 strong drafts beats getting 4 with a weak one.

## Checklist

- [ ] Time slots saved in memory
- [ ] pick-log.md and performance-log.md created from the templates
- [ ] X drafts routine on
- [ ] Performance check on after the first week of posts
