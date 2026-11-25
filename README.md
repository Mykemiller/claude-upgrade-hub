# 🧭 Claude Upgrade Hub

A simple, repeatable way to keep your Claude setup getting better.

Claude scouts new **skills, mods, plugins, tips and videos** on a schedule and drops them into your Notion as **New**. Once a week you spend 15–20 minutes deciding what to try. Nothing is ever installed unless you say so.

**You need:** a Claude plan with scheduled tasks, and the Notion connector. GitHub is only where this kit lives. No Linear, no code, no servers.

```
Sources ─▶ Scheduled scout ─▶ New rows in Notion ─▶ You review ─▶ Try / Install ─▶ Log ─▶ Retire
```

---

## Setup (about 15 minutes)

1. **Duplicate the Notion template.** Open the [Claude Upgrade Hub — Starter Kit](https://viridian-trader-1fe.notion.site/Claude-Upgrade-Hub-Starter-Kit-42389a0c16808146b226ee5df3764968) and click **Duplicate** (top right). You get three databases: **Upgrade Radar** (things you install), **Learn Tracker** (things you learn) and **Weekly Review**.
   *Don't have the link? Ask Claude to build the page from [`notion/TEMPLATE.md`](notion/TEMPLATE.md).*
2. **Connect Notion to Claude.** In Claude: Settings → Connectors → Notion. Give it access to your new page.
3. **Run the setup prompt.** Open a new Claude chat, paste [`prompts/01-setup.md`](prompts/01-setup.md), and answer its two questions (your time zone, and an optional YouTube playlist). Claude finds your page and creates three scheduled tasks:

   | Scheduled task | When | What it does |
   | --- | --- | --- |
   | Weekly upgrade scout | Sunday | Finds new skills, mods and plugins → **Upgrade Radar** |
   | Learn feed | Weekdays | Finds new tips, release notes and videos → **Learn Tracker** |
   | Weekly health check | Monday | Writes this week's **Weekly Review** page |

4. **Each Monday**, open the newest Weekly Review, clear the New rows, and pick 1–3 things to try. When you try something, set its Status and add one line under **What happened**.

## Optional add-ons

| Add-on | File | Needs |
| --- | --- | --- |
| Dashboard with freshness lights and a **Tell me 3 new things** button | [`addons/dashboard.md`](addons/dashboard.md) | Claude artifacts |
| 1-minute daily video of the day's finds | [`addons/heygen-video.md`](addons/heygen-video.md) | HeyGen connector |
| Weekly review as a Linear or GitHub issue | [`addons/issue-tracker.md`](addons/issue-tracker.md) | Linear or GitHub connector |

## The rules

1. **Scouts only find and queue.** They never install, run or mark anything done.
2. **Only you move an item past New.**
3. **Anything you install gets a safety check first.** For mods, run `claude plugin validate ./<folder>`. For skills, read the `SKILL.md` and any scripts before you install.
4. **Retire what you stop using.** Stale skills and tips cost context and give wrong advice.

The full method is in [`STANDARD.md`](STANDARD.md).

## Files

```
README.md               this page
STANDARD.md             Jar Standard v1: lifecycle, fields, rhythm, gate rules
notion/TEMPLATE.md      the Notion page and database schemas, if you build it by hand
prompts/01-setup.md     paste into Claude once
prompts/weekly-scout.md
prompts/learn-feed.md
prompts/health-check.md
addons/                 dashboard, HeyGen video, issue tracker
```

MIT licensed. Made by Myke Miller. Share it freely.
