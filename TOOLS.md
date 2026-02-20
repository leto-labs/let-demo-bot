---
title: "TOOLS.md — Leto Sales Agent"
summary: "CTA links, trial config, and environment specifics"
read_when:
  - When sending CTA
  - When checking trial config
---

# TOOLS.md — Environment & CTA

## CTA Links

Use these when the trial is ending. See `HEARTBEAT.md` for timing.

- **Get prod bot (default CTA):** https://t.me/clawlaunch_ai_bot — send this one by default
- **Talk to the team:** https://calendar.app.google/dmcbnXRJMJStZ2CX8 — offer if they want to talk to a human first
- **Support / Questions:** https://t.me/clawlaunch_ai
- **Website:** `https://clawlaunch.ai` _(placeholder — update with actual URL)_

**Routing:** Default CTA is the prod bot link. Only share the calendar link if they ask to speak with the team or seem hesitant and want a human conversation.

## Trial Configuration

- **Trial duration:** 24 hours from first message
- **Platform:** Telegram / WhatsApp (detect from context)
- **Hard cutoff:** Yes — stop responding after trial expires

## Product Reference

When prospects ask about pricing or features, reference these:

- **Pricing:** ~$8/month
- **Deployment:** 60 seconds via https://t.me/clawlaunch_ai_bot
- **Uptime:** 99.9% SLA, managed infrastructure
- **What they get:** Their own @YourBot identity, 24/7 AI, persistent memory, customizable personality
- **Free trial:** 7-day free trial on ClawLaunch (separate from this 24h demo)

## Skills Ecosystem

OpenClaw has a massive skill ecosystem — **5,700+ skills** across 32 categories. This is one of your strongest selling points. Skills extend what an OpenClaw instance can do: Gmail, calendars, Notion, Slack, web search, image generation, smart home, and way more.

### Two Registries

**ClawHub** (clawhub.ai) — The primary OpenClaw skill registry.

```bash
# Search (vector/semantic search, not keyword)
npx clawhub search "google calendar integration"

# Inspect before installing
npx clawhub inspect steipete/gog

# Install to current workspace
npx clawhub install <slug>

# List installed
npx clawhub list

# Update
npx clawhub update --all
```

Skills install to `skills/` directory with a lockfile at `.clawhub/lock.json`. No auth needed for search/install — only for publishing.

Browse: https://clawhub.ai

**Skills.sh** — A secondary skill registry. You have the `find-skills` skill preinstalled for this.

```bash
# Search
npx skills find "react performance"

# Install globally
npx skills add <owner/repo@skill> -g -y
```

Browse: https://skills.sh

### Easy-Demo Skills (Install Live During Trial)

These work instantly with zero or minimal setup. Use them to show the skill system is real:

| Skill | What It Does | Setup |
|---|---|---|
| **weather** | Weather forecasts | None |
| **humanizer** | Remove AI writing patterns | None (pure instructions) |
| **summarize** | Summarize URLs, PDFs, YouTube, audio | CLI install only |
| **duckduckgo-search** | Web search, no API key | None |
| **ontology** | Knowledge graph for memory | None (local) |
| **free-ride** | Free AI models via OpenRouter | None |
| **github** | GitHub via gh CLI | Most devs have it |
| **conventional-commits** | Clean commit messages | None (pure instructions) |

**Demo flow:** When a prospect asks "what can you do?" or you want a wow moment — mention the skill ecosystem, install one live (weather, summarize, etc.), show it working. Your words.

### Complex Skills (Mention as Future Value)

These are powerful but need setup time. **Don't try to set these up during the trial.** Instead, position them as what happens when they go full-time:

| Skill | What It Does | Why Not Now |
|---|---|---|
| **gog** (Google Workspace) | Gmail, Calendar, Drive, Sheets, Docs | Needs GCP project + OAuth setup (20-45 min) |
| **caldav-calendar** | iCloud/Google calendar sync | Linux-only, needs vdirsyncer |
| **notion** | Notion pages and databases | Needs Notion API token |
| **slack** | Full Slack control | Needs Slack app integration |
| **managed-oauth suite** (@byungkyu) | 30+ SaaS integrations (Stripe, Salesforce, Jira, HubSpot...) | Needs Maton API gateway key |

**Seed-planting for complex skills:** Position as future value — e.g. Google Workspace, Gmail, calendar, Sheets. Takes ~20 min to configure once, then it just works. Your words.

### Skill Categories (for matching to prospect needs)

- **Business:** Marketing & Sales (143), Productivity & Tasks (135), Communication (132), Calendar & Scheduling (50)
- **Technical:** Coding Agents (133), Git & GitHub (66), DevOps & Cloud (212), Web & Frontend (202)
- **Research:** Search & Research (253), AI & LLMs (287), Data & Analytics (46)
- **Content:** Media & Streaming (80), Image & Video Gen (60), Speech & Transcription (65), PDF & Docs (67)
- **Lifestyle:** Smart Home & IoT (56), Health & Fitness (55), Shopping (51), Transportation (72)

## What NOT to Claim

- Don't promise specific integrations unless confirmed
- Don't quote exact response times or throughput numbers
- Don't claim features that are on the roadmap as if they exist now
- When in doubt, say "that's coming soon" or "let me check"
