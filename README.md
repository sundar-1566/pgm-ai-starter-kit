# PgM AI Starter Kit

Six plain-English skills for program managers running a GTM/CX portfolio. Each one is a recipe an AI assistant follows. Nothing to install, and no code.

## The skills
| Skill | Use it when | Portfolio stage |
|---|---|---|
| `intake-triage` | A new request arrives | Intake & prioritize |
| `status-rollup-qbr` | Weekly status, or the QBR pre-read at quarter end | Weekly governance, exec forums |
| `meeting-to-jira` | Right after a sync or steering meeting | Weekly governance |
| `uat-from-qa-pass` | A story passes QA and needs business testing | Deliver the change |
| `adoption-friction-listener` | 1–8 weeks after any process or tool rollout | Adoption |
| `retro-synthesis` | Project close or quarter end | Close & learn |

## Three ways to use them
1. **Claude Code or Claude Desktop:** put each folder in `~/.claude/skills/`. The assistant picks the right one when you describe the task.
2. **Claude Projects (or any approved AI tool's project or workspace):** paste the SKILL.md text as the project instructions, then paste or attach your inputs.
3. **Any approved chat assistant:** paste the SKILL.md, then your inputs, and say "follow this recipe."

Use only the AI tools and data connections your security team has approved. Start with read-only access.

## Try it in 5 minutes with the sample data
- `sample-data/meeting-notes.txt` → run **meeting-to-jira**
- `sample-data/portfolio.csv` + `meeting-notes.txt` → run **status-rollup-qbr**
- `sample-data/field-feedback.txt` → run **adoption-friction-listener**

All sample data is made up.

## Rollout order that builds trust
1. **Personal helpers first** (weeks 1–4): each PgM uses meeting-to-jira and status-rollup on their own work. Mistakes stay small, and trust builds.
2. **Shared reporting next** (weeks 5–8): the portfolio roll-up and QBR pre-read come from the same data.
3. **Event-triggered agents last** (weeks 9–12): uat-from-qa-pass runs on a Jira trigger, with drafts only and a person approving.

Track: hours returned per PgM each week, the rewrite rate (how much of the draft people change), reports on time, and weekly active users.

Made by Sundar Subramanian · [github.com/sundar-1566](https://github.com/sundar-1566). Issues and suggestions welcome.

## License
[CC BY 4.0](LICENSE): free to use and adapt with credit.
