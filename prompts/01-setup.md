# Setup prompt: paste this into a new Claude chat

```
Set up my Claude Upgrade Hub. I've duplicated the "Claude Upgrade Hub — Starter Kit" page into my Notion and connected Notion to you.

1. Use the Notion connector to find my page titled "Claude Upgrade Hub — Starter Kit" (if there are several, use the one I most recently edited). Fetch its three databases (Upgrade Radar, Learn Tracker, Weekly Review) and note each one's page URL and data source id (collection://...). If the page or a database is missing, stop and tell me what's missing.

2. Ask me two short questions in one go (a multiple-choice card if you have one):
   a. My time zone. Recommend the one you can infer, if any.
   b. A public YouTube playlist of Claude videos to watch, or "none". Recommend "none" if I'm unsure.

3. Read the three prompt files from this kit:
   https://raw.githubusercontent.com/Mykemiller/claude-upgrade-hub/main/prompts/weekly-scout.md
   https://raw.githubusercontent.com/Mykemiller/claude-upgrade-hub/main/prompts/learn-feed.md
   https://raw.githubusercontent.com/Mykemiller/claude-upgrade-hub/main/prompts/health-check.md
   Use the text inside each file's code block. If you can't fetch them, ask me to paste them.

4. In each prompt, replace the placeholders:
   {{HUB_URL}}     my hub page URL
   {{RADAR_DS}}    the Upgrade Radar data source id
   {{LEARN_DS}}    the Learn Tracker data source id
   {{REVIEW_DS}}   the Weekly Review data source id
   {{TIMEZONE}}    my time zone (IANA name, e.g. America/Chicago)
   {{PLAYLIST}}    my playlist URL, or the word none

5. Create three scheduled tasks with those prompts. Check my existing scheduled tasks first so you don't make duplicates.
   - "Weekly upgrade scout": Sundays at about 4:17 PM my time
   - "Learn feed": weekdays at about 6:43 AM my time
   - "Weekly health check": Mondays at about 7:23 AM my time

6. Run the health check prompt once now, so my first Weekly Review page exists.

7. Tell me in a few lines what you created and when each task runs, and remind me: each Monday, open the newest Weekly Review and pick 1–3 things to try.

Rules: don't install anything, don't sign in to sites, don't send email or messages, and change nothing in Notion except what these steps say.
```
