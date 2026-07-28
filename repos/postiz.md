# Postiz

**`gitroomhq/postiz-app`** · 33.9k ★ · AGPL-3.0 · TypeScript
<https://github.com/gitroomhq/postiz-app>

*Seen on: Instagram Reels (Wassim younes AI), "AI OPEN SOURCED social media marketing team"*

---

## 🟢 Safety: low risk

**It authenticates the right way.** Official, platform-approved OAuth flows — the
one meaningful difference from tools like [Agent-Reach](agent-reach.md).

| Check | Finding |
|---|---|
| **Credentials it wants** | OAuth authorization per platform, granted through the platform's own consent screen. Revocable from your account settings at any time, scoped to what you approve. The README states it never asks users to paste API keys into the hosted product. |
| **Where your data goes** | Self-host and it stays on your server. The hosted version is the vendor's — your choice which. |
| **Platform terms** | Compliant. This is the sanctioned way to post programmatically. |
| **Legal exposure** | None. |
| **License obligations** | **AGPL-3.0.** Read this before building on it: if you run a modified version as a network-accessible service, you must publish your source. Personal and internal use is unaffected. |
| **Maintenance** | Excellent: 2,720 commits, 6.3k forks, active development. |

### What could go wrong

- **The AGPL, if you're building a product.** Not a security risk, but the most
  likely way this bites someone: you fork it, add features, sell access, and now
  owe the source. Fine if you know; expensive if you find out later.
- Self-hosting means you own the security of the box holding OAuth tokens for
  every connected account. Keep it patched.

### Using it safely

- Nothing special — this is the well-behaved option. Self-host via Docker Compose
  if you want the data on your own machine.
- If commercial use is the goal, read the AGPL properly or contact them about
  licensing first.

---

## What it does

Open source social media scheduling and publishing: Instagram, YouTube, LinkedIn,
Reddit, TikTok, Facebook, Pinterest, Threads, X, Slack, Discord, Mastodon,
Bluesky, Dribbble. Includes analytics, team collaboration, and integrations with
N8N and Make.com. The self-hosted alternative to Buffer/Hootsuite.

The README states there is **no feature difference between the hosted and
self-hosted versions** — nothing held back from the free tier.

## Requirements

pnpm monorepo: NextJS (React), NestJS, Prisma on PostgreSQL, Temporal, Resend for
email. Docker Compose files provided for self-hosting.

## Verdict

**The best usefulness-to-risk ratio in this archive.** Mature, actively developed,
and it does the hard thing correctly rather than the easy thing cheaply.

If you post to social media regularly, this is the one to actually install.

---
*Verified 28 July 2026. Figures are a snapshot from that day, not a quality signal.*
