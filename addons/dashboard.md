# Add-on: dashboard with freshness lights and "Tell me 3 new things"

A one-page Claude dashboard (artifact) that reads your hub live from Notion:

- **Freshness tiles:** one for Upgrade Radar and one for Learn Tracker, each with a green/yellow/red light (see STANDARD.md §6), the number of items waiting at New, and the age of the oldest.
- **Tell me 3 new things:** picks 3 New items (one to install, one to learn, one wildcard). Each has **Try** and **Skip** buttons that set its Status in Notion (Try → "Reviewed" or "Try next"; Skip → "Rejected" or "Skipped").
- **This week:** the latest Weekly Review row.

It runs with each viewer's own Notion connection, so share it only with yourself, or give friends this file and let Claude build their own.

Paste into Claude:

```
Build me a dashboard for my Claude Upgrade Hub as a Claude dashboard artifact, reading my Notion live through the Notion connector. Hub page: {{HUB_URL}}. Upgrade Radar: {{RADAR_DS}}. Learn Tracker: {{LEARN_DS}}. Weekly Review: {{REVIEW_DS}}.

Sections:
1. Two freshness tiles (Upgrade Radar, Learn Tracker): green if the newest "Date added" is within 8 days (Radar) or 3 days (Learn), yellow if within twice that or more than 25 rows wait at New, red otherwise. Show New count and oldest New age.
2. "Tell me 3 new things" button: picks 3 Status = New rows (one Radar, one Learn, one wildcard; highest Score or Validity first, then newest), shows Name, Kind and the one-line summary, with Try and Skip buttons. Try sets Status to Reviewed (Radar) or Try next (Learn); Skip sets Rejected or Skipped. Only write to Notion when I press a button, and ask me to approve the exact update call before you store it in the page.
3. "This week": the newest Weekly Review row (Health, New waiting, Picked to try).
Keep it to one page that reads well on a phone.
```
