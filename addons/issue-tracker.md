# Add-on: weekly review as a Linear or GitHub issue

Prefer a task tracker to a Notion page? Add this paragraph to the end of your "Weekly health check" scheduled task's prompt (ask Claude to update it):

**Linear**
```
Also: in Linear team "<TEAM KEY>", check for an open issue titled "Claude hub review — week of <Mon D, YYYY>". Update it if it exists, otherwise create it assigned to me, priority Medium, with the same Health, Waiting and 3 picks sections and the checklist, plus a link to this week's Weekly Review page.
```

**GitHub**
```
Also: in my GitHub repo "<owner/repo>", check for an open issue titled "Claude hub review — week of <Mon D, YYYY>". Update it if it exists, otherwise open it with the same sections and checklist and a link to this week's Weekly Review page. Label it "claude-hub".
```

The Notion Weekly Review stays the record either way.
