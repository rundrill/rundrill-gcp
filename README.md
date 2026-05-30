# RunDrill Google Cloud

Your personal **Google Cloud certification coach** inside your AI agent — prep the whole ladder
(**Foundational → Associate → Professional**) the way the exam actually demands it: by **choosing the
best service under real constraints** and **reviewing real Google Cloud configs for the planted flaw**,
not by memorising service lists or watching the AI design your architecture. Short targeted drills, an
honest picture of your tier, mistake memory that resurfaces what you got wrong, and timed mock exams.
Your tier and progress live on the RunDrill MCP server (`mcp.rundrill.com`), synced across machines —
not in a local file.

**Why this course is different.** Google Cloud exams don't reward recall — they hand you a scenario
with competing constraints (cost, latency, availability, security, data residency, operational
overhead) and several plausible services, and ask which fits BEST. The skill that matters is
*discrimination under constraints*: which service, and **why not** the near-neighbours — Cloud SQL vs
Spanner vs Bigtable vs Firestore, Cloud Run vs GKE vs App Engine vs Functions, Dataflow vs Dataproc vs
Data Fusion. When an AI can draft any architecture or template on demand, the real risk is the
*illusion of competence* — accepting one that reads fine and is quietly wrong: a primitive
`roles/owner` grant, a single-zone "highly available" design, a firewall rule that's wide open, a
read replica mistaken for failover. Every drill is **blended** — an exam-style scenario decision paired
with a hands-on console/`gcloud`/Terraform task you run in your own project — and the **signature drill
hands you a real Google Cloud config with a planted flaw and asks you to find it, like a security
review.** Plus timed, domain-weighted **mock exams** as a per-cert boss battle (timed practice is the
strongest readiness signal).

The course mirrors the Google Cloud certification ladder — **Foundational** (Cloud Digital Leader) →
**Associate** (Cloud Engineer, Data Practitioner, Workspace Administrator) → **Professional** (Cloud
Architect, Developer, DevOps, Security, Network, Data Engineer, Database, Machine Learning). Google
Cloud has **no Specialty tier** — its Professional tier absorbs the security, networking, data, and ML
domains AWS files under Specialty. Pick the certification you're aiming for; the shared Foundational
base and the cross-cutting Core service deep-dives are always in scope.

> **Cost & safety.** Hands-on tasks run in **your own Google Cloud project**. The coach flags anything
> billable, prefers the free tier / Always Free, and reminds you to tear it down.

**Learn in your language.** The Google Cloud exam and console are in English, but you don't have to
study only in English: set your native language and the coach explains in it while giving every Google
Cloud service and term as *native (English original)* — so you reason naturally and still recognise the
official terms on the exam.

## One plugin, three hosts

The coaching skill (`skills/gcp-coach/SKILL.md`) and `.mcp.json` are shared; each host reads its own
manifest and ignores the rest.

| Host | Reads |
|---|---|
| Claude Code / Claude Desktop | `.claude-plugin/plugin.json` + `.mcp.json` |
| OpenAI Codex | `.codex-plugin/plugin.json` + `.mcp.json` |
| Google Antigravity | `plugin.json` + `mcp_config.json` |

The MCP endpoint is `https://mcp.rundrill.com/skills/gcp` — the skills-course host, passing
`subject: "gcp"`. The server routes on the `/skills` segment and ignores the course name; the name
makes Google Cloud register as its own MCP server in your agent. On first use the host opens a browser
tab for the OAuth handshake, then closes it — no API key to paste.

## Install

- **Claude Code / Desktop** — via the RunDrill marketplace:
  ```
  /plugin marketplace add rundrill/rundrill
  /plugin install rundrill-gcp@rundrill
  ```
  Then run `/gcp-coach`.
- **OpenAI Codex** — `codex plugin marketplace add rundrill/rundrill`, then install `rundrill-gcp`.
- **Google Antigravity** — drop this folder into `~/.gemini/config/plugins/rundrill-gcp/` (global) or
  `<workspace>/.agents/plugins/rundrill-gcp/` (workspace-scoped).

## A note on Google Cloud™

This is an independent study aid for learning Google Cloud and preparing for Google Cloud Certification
exams. It is **not** affiliated with, authorized, or endorsed by Google LLC. *Google Cloud™* and the
Google Cloud certification names are trademarks of Google LLC. The course teaches the publicly
documented services and exam domains in our own words; it does not reproduce Google Cloud exam content.
Google changes services, limits, and certifications frequently — always confirm current details against
the official Google Cloud documentation.

## License & attribution

© RunDrill. Licensed under **Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International
(CC BY-NC-ND 4.0)** — full text in [LICENSE](LICENSE). You may view, run, and share this plugin
unchanged, non-commercially, with attribution; you may not use it commercially or publish
modified/derivative versions. For other licensing, contact **hello@rundrill.com**.
