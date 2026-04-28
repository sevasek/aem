# Automatic Email Manager (AEM)

**Intelligent n8n-powered inbox automation that classifies emails, extracts actionable tasks, generates style-consistent drafts, and delivers daily digests — turning hours of manual triage into structured productivity.**

![License](https://img.shields.io/badge/license-Proprietary-blue.svg)
![n8n](https://img.shields.io/badge/automation-n8n-FF6A00.svg)
![Docker](https://img.shields.io/badge/containerized-Docker-2496ED.svg)
![OpenAI](https://img.shields.io/badge/AI-OpenAI-412991.svg)
![Gmail](https://img.shields.io/badge/integrations-Gmail-4285F4.svg)
![TypeScript](https://img.shields.io/badge/code-JavaScript-F7DF1E.svg)

## About

AEM is a robust, self-hosted automation system built in **n8n** that intelligently manages high-volume Gmail inboxes. It combines rule-based logic, defensive JavaScript Code nodes, and OpenAI agents to classify emails, surface action items, convert them into structured Vikunja tasks, route summaries to Discord, and support context-aware reply drafting.

Designed and implemented by a Site Pastor managing complex ministry, family, and operational responsibilities, AEM demonstrates production-grade automation architecture that solves real-world overload while maintaining full user control and security.

### Business Value Delivered
- **8–12 hours saved per week** on manual email triage
- Dramatically reduced response fatigue and missed follow-ups
- Consistent, high-quality task extraction with SMART criteria
- Scalable foundation for multi-account and advanced AI workflows

**Target Audience**: Busy professionals, pastors, and small-team operators who need reliable, private automation without SaaS lock-in.

## Key Features

- **Hierarchical AI Classification** — Multi-label system (AEM/Action Required → Needs Reply, Newsletter, Meeting, Finance, FYI) with Eisenhower + domain MVV prioritisation
- **Actionable Task Extraction** — Full thread summarisation → SMART Vikunja tasks with HTML descriptions and approval workflows
- **Daily Discord Digests** — Length-controlled summaries with emojis, links, and clean formatting
- **Smart Unsubscribe & Archiving** — RFC 2047 decoding, one-click List-Unsubscribe, and `ready_to_archive` logic
- **Defensive Engineering** — Robust JSON repair, label diffing, batch processing, and error-resilient data handoff
- **Style-Consistent Drafting** — Ready for OpenAI generation in Christ-centred, professional pastoral tone (core loop operational)

## Tech Stack

- **Core**: n8n (main workflows + advanced Code nodes)
- **AI**: OpenAI Chat Completions (gpt-4o-mini and equivalents)
- **Integrations**: Gmail API, Vikunja, Discord, Google Drive/Calendar
- **Infrastructure**: Docker + Docker Compose, self-hosted VPS (Ubuntu)
- **Prompt Engineering**: Markdown-based living prompts and reusable logic

## Screenshots & Demo

<div align="center">

![Workflow Overview](docs/screenshots/aem-workflow-overview.png)
*End-to-end Gmail → Classification → Task → Digest flow*

![Label Overview](docs/screenshots/label-report.png)
*Simple daily summaries of emails sorted and processed*

![Discord Digest Example](docs/screenshots/discord-daily-digest.png)
*Clean, scannable daily summaries of News and FYI emails*

![Discord Action Required Example](docs/screenshots/discord-action-required.png)
*Clean, scannable daily summaries of action emails*

![Vikunja Task Creation](docs/screenshots/vikunja-task-example.png)
*AI-generated tasks with full context*

</div>

## Installation (Self-Hosted)

### Prerequisites
- Ubuntu 24.04 VPS (or equivalent)
- Docker & Docker Compose
- n8n license (or community edition)
- API keys: OpenAI, Gmail (OAuth), Vikunja, Discord