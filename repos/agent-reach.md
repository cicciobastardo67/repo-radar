# Agent-Reach

**`Panniantong/Agent-Reach`** · 61.3k ★ · MIT · Python
<https://github.com/Panniantong/Agent-Reach>

*Seen on: Instagram Reels (Wassim younes AI), "Twitter API costs $200/month" — gated behind commenting "REACH"*

---

## 🔴 Safety: high risk

**It is free because it doesn't use the official APIs — it uses your logged-in
session cookies.** That is the entire trade, and the post doesn't mention it.

| Check | Finding |
|---|---|
| **Credentials it wants** | Twitter/X cookie, Reddit login, browser session for Facebook/Instagram, cookie for XiaoHongShu. Session cookies are equivalent to passwords — they grant full account access and bypass 2FA. |
| **Where your data goes** | Runs locally, so no vendor server is involved. The exposure is that the tool holds live credentials to your accounts. |
| **Platform terms** | Breaches the terms of service of most platforms it supports. Automated access via a user session is exactly what those clauses prohibit. |
| **Legal exposure** | Low for reading public content; the realistic penalty is account-level, not legal. |
| **License obligations** | MIT — none. |
| **Maintenance** | Excellent: 334 commits, very active, 61.3k stars (was ~31k mid-2026). |

### What could go wrong

1. **The account you authenticate gets banned.** Not hypothetical — this is the
   normal outcome when platforms detect automated session use.
2. **Your cookies sit in a config on disk**, readable by anything else running as
   your user.
3. **It breaks constantly.** The project's headline feature is multi-backend
   routing with automatic fallback — "preferred + alternate" per platform. That
   exists *because* platforms actively close these access paths. Good engineering,
   but it tells you the ground is always moving.

### Using it safely

- **Throwaway accounts only.** Never your main account, never a work account,
  never one tied to a client or to anything you'd mind losing.
- Don't build anything that must keep working on top of it. Treat it as a
  research tool, not infrastructure.
- Run it under a separate OS user or container so the cookie store isn't sitting
  next to everything else.

---

## What it does

A Python CLI that gives an AI agent read and search access to 13 platforms:
Twitter/X, Reddit, YouTube, GitHub, Bilibili, XiaoHongShu, Facebook, Instagram and
others. Works with any agent that can run shell commands — Claude Code, Cursor,
Windsurf.

Genuinely well built: per-platform ranked backend lists with transparent failover,
plus an `agent-reach doctor` command for diagnosing what's broken.

## Requirements

Python 3.10+. Uses yt-dlp, twitter-cli, bili-cli, feedparser, MCP integration.
GitHub works unauthenticated for public repos. Optional Exa API for semantic
search.

## Verdict

Technically impressive and genuinely useful — and the highest-risk thing in this
archive, because the risk is invisible in the pitch. The value is real if you
accept the terms: **a disposable account, and nothing important built on top.**

If you need reliable social posting rather than reading, use
[Postiz](postiz.md) instead — it does the opposite thing correctly, via official
OAuth.

---
*Verified 28 July 2026. Figures are a snapshot from that day, not a quality signal.*
