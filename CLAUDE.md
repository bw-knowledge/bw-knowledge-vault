# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

---

## What This Repo Is

This is a **knowledge capture pipeline** — not a traditional code project. There is no build system, package.json, or test runner. The "code" is an n8n workflow definition and a set of Obsidian vault files (markdown clippings, topic notes, templates, and a database definition).

**Flow:** Telegram URL → n8n Cloud → Firecrawl scrape → Claude Haiku 4.5 summary → GitHub commit → Obsidian Git pull

---

## Repo Structure

```
.code/                        ← automation metadata (not app code)
  Knowledge Hub Capture.json  ← full n8n workflow export (1563 lines)
  sources.json                ← URL→vault-path index (updated by n8n on each capture)
  capture-log.jsonl           ← JSONL append-log of every capture (one entry per line)

Clippings/Telegram/           ← AI-generated clippings (auto-committed by n8n)
Topics/                       ← curated topic notes (hand-maintained)
Templates/                    ← Obsidian Templater scripts + the Claude prompt template
Bases/Articles.base           ← Obsidian database definition with domain-extraction formula
.obsidian/                    ← vault config (gitignored plugin state; core + community plugins tracked)
```

---

## The n8n Workflow

**Workflow ID:** `xo9M1ItRvwkrTRqx` (Knowledge Hub Capture)  
**Workflow definition:** `.code/Knowledge Hub Capture.json`

Node order:
> Telegram Trigger → Session Manager → Route by Action → Extract URL → URL Found? → Immediate Reply → Firecrawl Scrape → GitHub List Topics Capture → Build Anthropic Prompt → Basic LLM Chain (Claude Haiku 4.5) → Build Clipping → Build Filename → Get a File → Resolve Filename → Create a File → **[fan-out]** → Build Success Reply + Build Source Index Update + Build Capture Log Entry → Success Reply / Update Source Index / Append Log Entry

To update the workflow: edit `.code/Knowledge Hub Capture.json` and import it in n8n Cloud, or use the n8n MCP tools available in this session.

---

## Clipping Format

Every file in `Clippings/Telegram/` follows this schema:

```yaml
---
title: "Article Title"
created: YYYY-MM-DD
source: "https://..."
tags:
ContentType: "Article"
captured_via: "Telegram"
captured_at: "ISO 8601 timestamp"
---

In summary, [one declarative sentence].

## Suggested Topics
[1–3 freely proposed topic names]

## Matched Topics
[[Existing vault topics]]

## Headlines
- **Bold headline.** Supporting detail.

## Things
- **People:** ...

---

## Full Article
[Full scraped markdown]
```

---

## Automation Metadata Files

### `.code/sources.json`
A flat JSON object mapping `url → vault_path`. Updated by n8n on each successful capture via the `Build Source Index Update` branch. To manually add/correct an entry, edit this file directly — it's a plain JSON object.

### `.code/capture-log.jsonl`
Append-only JSONL log. One JSON object per line:
```json
{"timestamp":"ISO","chat_id":"...","url":"...","status":"success","vault_path":"..."}
```
**Do not reformat** this file as JSON array — n8n's `Append Log Entry` node reads it as JSONL and appends raw lines. Windows CRLF line endings will cause the append-separator check to fail; always save with LF.

---

## n8n-Specific Gotchas (from live debugging)

- **`Buffer` is not available in n8n expression fields** — only inside Code nodes. Decode/encode in the Code node, pass plain string to `fileContent`.
- **`\\n` in n8n jsCode does not produce a newline at runtime** — use `String.fromCharCode(10)` instead. The JSON→JS escape chain is lossy in n8n's sandbox.
- **GitHub GET file response has multiple shapes** — always handle all four: `json.content` (base64), `json.fileContent` (plain), `json.data` (string), `json.data.content` (base64 nested).
- **`retryOnFail: true` on GitHub append nodes causes duplicate entries** — a SHA conflict on retry writes stale content again. Remove `retryOnFail` from any node that does an append operation.
- **`trimEnd()` before appending** normalises CRLF/trailing whitespace so the separator check is reliable.

---

## Git Workflow

GitHub is the source of truth. Obsidian Git pulls commits automatically into the local vault.

- Automated captures commit directly to `main` (n8n uses the GitHub API)
- For manual changes: `git push origin HEAD:main` directly is fine for this single-contributor project
- To sync when remote has moved ahead (common after automated captures): `git stash → git rebase origin/main → git stash pop`
- To revert: `git revert HEAD` (new commit) — not `git reset --hard` (rewrites history, causes non-fast-forward push rejections)

**Never commit `.claude/settings.local.json`** — treat it the same as `.env.local`. If it's tracked, remove with `git rm --cached .claude/settings.local.json`.

---

## Topics and Wikilinks

`Topics/` notes are hand-curated. The bot's **Suggested Topics** are Claude's unconstrained proposals; **Matched Topics** cross-reference existing `Topics/` notes. Wikilinks (`[[Topic Name]]`) are added manually during reading — the automation never writes wikilinks.

The `Bases/Articles.base` database auto-filters clippings by linked topic using `file.hasLink()` and extracts domains via a regex formula on the `source` field.
