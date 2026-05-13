## Overview

Knowledge Hub is a knowledge capture pipeline. You send a link to a Telegram bot, and within ~30 seconds a structured clipping appears in your Obsidian vault — fully formatted, AI-summarised, and version-controlled in GitHub.

---

## The Stack

| Layer | Tool |
|---|---|
| Capture interface | Telegram bot (`bwclipper_bot`) |
| Workflow engine | n8n Cloud |
| Web scraping | Firecrawl (community node) |
| AI summarisation | Claude Haiku 4.5 (via Anthropic + LangChain) |
| Storage | GitHub (`bw-knowledge/bw-knowledge-vault`) |
| Local sync | Obsidian + Obsidian Git plugin |

---

## How It Works

1. **You send a URL** to the Telegram bot — either paste it directly or forward a message containing a link.
2. **Session Manager** routes the message: capture, `/list_topics`, `/help`, `/cancel`, or fallback.
3. **Firecrawl** scrapes the article and returns clean markdown.
4. **GitHub List Topics** reads your `Topics/` folder so Claude knows what topic notes already exist.
5. **Claude Haiku 4.5** produces a structured summary with five sections:
   - *In summary* — one declarative sentence capturing the most interesting finding
   - *Suggested Topics* — 1–3 topic names Claude freely proposes (unconstrained, best fit for the article)
   - *Matched Topics* — which existing `Topics/` notes apply (only present when vault topics exist; omitted if the vault is empty)
   - *Headlines* — 3–5 bold, declarative bullets with supporting detail
   - *Things* — People, Places, Numbers, Things, Concepts
6. **Build Clipping** assembles the full markdown file: frontmatter + AI summary + full article text.
7. **GitHub Create File** commits the clipping to `Clippings/Telegram/` with a dated filename.
8. **Obsidian Git** auto-pulls the commit into your local vault.
9. **Telegram** sends a success message with the summary, suggested topics, and vault path.

---

## Clipping Format

Each clipping follows this structure:

```
---
title: "Article Title"
created: YYYY-MM-DD
source: "https://..."
tags:
ContentType: "Article"
captured_via: "Telegram"
captured_at: "ISO timestamp"
---

In summary, [declarative statement about the most interesting finding].

## Suggested Topics

[1–3 topic names freely suggested by Claude — unconstrained]

## Matched Topics

[Existing vault topics that apply — omitted if vault has no topics yet]

## Headlines

- **Headline.** Supporting detail.

## Things

- **People:** ...
- **Places:** ...
- **Numbers:** ...
- **Things:** ...
- **Concepts:** ...

---

## Full Article

[Full scraped markdown]
```

---

## Bot Commands

| Command | Action |
|---|---|
| Paste or forward a URL | Captures and summarises the article |
| `/list_topics` | Lists all notes in your `Topics/` folder |
| `/help` | Shows command reference |
| `/cancel` / `/reset` | Clears the current session |

---

## Vault Structure

```
Knowledge Hub/
├── Clippings/
│   └── Telegram/
│       └── YYYY-MM-DD Article Title.md
├── Topics/
│   └── Topic Name.md      ← curated by hand; bot suggests but you link
├── AI Summaries/
└── Knowledge Hub — What We've Built.md
```

---

## Design Decisions

- **Suggested Topics and Matched Topics are separate concerns.** Suggested Topics are Claude's unconstrained recommendations — the best names for this article regardless of what's in the vault. Matched Topics cross-references your existing `Topics/` notes and only appears when vault topics exist. You add `[[wikilinks]]` during reading. This keeps taxonomy suggestions creative while linking stays intentional.
- **Full article is preserved.** The scraped markdown is appended after the AI summary so nothing is lost.
- **GitHub is the source of truth.** Obsidian Git pulls from GitHub, so the vault works across devices and is ready for team sharing.
- **Session management** uses n8n static data with a 30-minute TTL, namespaced under `knowledgeHubSessions`.
- **Group chat support** is enabled: the bot strips `@botname` suffixes from commands and BotFather privacy mode is disabled so it receives plain messages in groups.

---

## n8n Workflow

**Workflow ID:** `xo9M1ItRvwkrTRqx` — Knowledge Hub Capture

Key nodes in order: Telegram Trigger → Session Manager → Route by Action → Extract URL → URL Found? → Immediate Reply → Firecrawl Scrape → GitHub List Topics Capture → Build Anthropic Prompt → Basic LLM Chain (Claude Haiku 4.5) → Build Clipping → Build Filename → Get a File → Resolve Filename → Create a File → Build Success Reply → Success Reply
