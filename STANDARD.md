# Jar Standard v1

A "jar" is any collection that watches public Claude material and helps you adopt the useful parts. Every jar follows the same lifecycle, fields, rhythm and gate rules, so one weekly check can keep them all healthy.

## 1. Lifecycle

```
Sources → Scout → Score and dedupe → Queue (Status = New) → Your review
   → Adopt / Install / Try → Adoption log → Retire when stale
```

Scouts only find and queue. Only you move an item past **New**.

## 2. Two kinds of jar

| Kind | Holds | Database | Status path |
| --- | --- | --- | --- |
| **Install** | Skills, mods, plugins, connectors | Upgrade Radar | New → Reviewed → Installed · Rejected → Retired |
| **Learn** | Tips, videos, release notes | Learn Tracker | New → Try next → Tried · Adopted · Skipped → Retired |

## 3. Fields every database has

| Field | Purpose |
| --- | --- |
| **Key** | Catches duplicates: `owner/repo#name` for things you install, `tip-0001` or `yt-<video id>` for things you learn |
| **Source** + **Source type** | Link, and Official or Community |
| **Date added** / **Last checked** | When it was found, and when it was last checked |
| **Score** | Your own 0–100. Scouts may also set **Validity** |
| **Risk** (install only) | Pass / Warn / Fail / Unreviewed, before install |
| **Status** | See the paths above |
| **What happened** / **Notes** | One line after you try it. This closes the loop |

## 4. Rhythm

| Cadence | What happens | Who |
| --- | --- | --- |
| Weekdays | Learn feed adds New rows | Scheduled task |
| Sunday | Upgrade scout adds New rows | Scheduled task |
| Monday | Health check writes the Weekly Review | Scheduled task |
| Monday, 15–20 min | Clear New rows, pick 1–3 to try | You |
| First Monday of the month | Re-check installed items against their source; drop dead sources | Health check flags it, you decide |
| Quarterly | Retire anything not used or checked in 90 days | You |

## 5. Gate rules

- **Queue:** Validity ≥ 60, Risk ≠ Fail, and a clear use for you.
- **Install:** scan first (`claude plugin validate`, or read `SKILL.md` and any scripts), check what it can reach (files, network, programs), install at user scope, and log the version and date.
- **Adopt:** try it once on real work, then mark Tried or Adopted with one line.
- **Official beats community** when both cover the same thing.

## 6. Freshness lights (used by the dashboard and the health check)

| Light | Meaning |
| --- | --- |
| 🟢 Green | The feeding task ran within its schedule |
| 🟡 Yellow | Late by up to twice its gap, or more than 25 items waiting at New |
| 🔴 Red | The task is paused or failed, or more than twice its gap late |

## 7. Good sources to start with

- Anthropic: anthropic.com/news, docs.claude.com, support.claude.com, code.claude.com
- Skills: github.com/anthropics/skills, plus well-starred community skill collections
- Mods: Anthropic's sample mods (anthropics/claude-code-playground), awesome-claude-code-mods
- Curated indexes: hesreallyhim/awesome-claude-code

Add or drop sources at the monthly check.
