# Notion template (build by hand or ask Claude)

If you don't have the duplicate link, paste this into Claude with the Notion connector on:

> Create a private Notion page titled "Claude Upgrade Hub — Starter Kit" with a one-paragraph intro, and inside it these three databases, exactly as specified. Then add the 14 starter tips at the bottom of this file to Learn Tracker with Status = New.

## Upgrade Radar
| Property | Type | Options |
| --- | --- | --- |
| Name | Title | |
| Key | Text | owner/repo#name |
| Kind | Select | Skill, Mod, Plugin, Connector |
| What it does | Text | |
| Install | Text | exact command or steps from its README |
| Source | URL | |
| Source type | Select | Official, Community |
| Validity | Number | scout score 0–100 |
| Risk | Select | Pass, Warn, Fail, Unreviewed |
| Score | Number | your score 0–100 |
| Status | Status | New · Reviewed · Installed · Rejected · Retired |
| Date added, Last checked | Date | |
| Notes | Text | |

## Learn Tracker
| Property | Type | Options |
| --- | --- | --- |
| Name | Title | |
| Key | Text | tip-0001, yt-<video id> |
| Kind | Select | Tip, Video, Release note |
| Product | Select | Claude app, Claude Code, Claude Duet, API |
| Topic | Select | Prompting, Projects, Skills, Mods, Connectors, Artifacts, Memory, Automation, Models, Safety, Setup |
| Summary | Text | |
| Source | URL | |
| Source type | Select | Official, Community |
| Score | Number | |
| Status | Status | New · Try next · Tried · Adopted · Skipped · Retired |
| What happened | Text | |
| Date added, Last checked | Date | |

## Weekly Review
| Property | Type |
| --- | --- |
| Week | Title ("Week of Mon D, YYYY") |
| Date | Date |
| Health | Select: Green, Yellow, Red |
| New waiting | Number |
| Added this week | Number |
| Picked to try | Text |
| Flags | Text |
| Done | Checkbox |

## Starter tips
1. Write a brief, not a prompt: goal, audience, what done looks like, what to avoid.
2. Give Claude a yes/no "done" check at the end of a request.
3. Fix the first message instead of arguing: edit and resend.
4. Use a Project for repeat work.
5. Turn a correction you repeat into a skill.
6. Connect the apps you already use.
7. Ask for a doc, deck or dashboard, not just a reply.
8. Tell Claude what to remember, and "forget that" to remove it.
9. Put a weekly ask on a schedule.
10. Match the effort level to the job.
11. Use a second session to review important work.
12. Keep CLAUDE.md and project instructions short.
13. In Claude Code, `/rewind` undoes recent turns and edits.
14. Run `claude plugin validate` on a mod before installing it.
