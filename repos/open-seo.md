# OpenSEO

**`every-app/open-seo`** · 8.7k ★ · MIT · TypeScript
<https://github.com/every-app/open-seo>

*Seen on: GitHub (every-app/open-seo), "Open source alternative to Semrush and Ahrefs"*

---

## 🟡 Safety: conditional — "open source" here does not mean free

**The software is free. The data isn't.** That's the condition, and it's the part
worth knowing before you spend an evening installing it.

| Check | Finding |
|---|---|
| **Credentials it wants** | A **DataForSEO API key** — a paid third-party account. Scoped and revocable, but you pay per query, directly to them. |
| **Where your data goes** | Your queries go to DataForSEO. Self-hosted deployment keeps everything else on your infrastructure. |
| **Platform terms** | Compliant — DataForSEO is a legitimate paid data provider, not a scraping workaround. |
| **Legal exposure** | None. |
| **License obligations** | MIT — none. |
| **Maintenance** | Good: ~400 commits, 968 forks, 24 open issues, 32 open PRs. Real adoption. |

### What could go wrong

- **Metered billing surprise.** Pay-as-you-go means an over-broad crawl or a
  scheduled job left running can cost more than you expected. Set spending limits
  on the DataForSEO side before you start.
- **Deploying it internet-facing without thinking.** The project distinguishes
  Docker (personal) from Cloudflare (team/public) deployment for a reason — if you
  expose it, you're exposing an API key that spends money.

### Using it safely

- Set a hard spending cap on the DataForSEO account first.
- Start with the Docker/personal deployment. Only go internet-facing when you
  actually need team access, and put auth in front of it.
- Or skip self-hosting: the hosted version at openseo.so is $10/month.

---

## What it does

A full SEO platform: keyword research, rank tracking, competitor analysis,
backlink audits, site audits, and **AI visibility** (how often your site gets
cited by AI assistants). Includes an MCP integration, so an agent can query it
directly.

The pitch: *"a pay-as-you-go alternative that you actually control"* — you drop
the fixed Semrush/Ahrefs subscription (~$100+/month) and pay only for queries you
actually run.

Stack: TypeScript, Vite, Drizzle ORM, Playwright for tests.

## Requirements

DataForSEO API key. Docker for personal use, or Cloudflare for team deployment.

## Verdict

**Do the arithmetic before installing.** If you already spend on SEO tooling,
this plausibly cuts the bill. If you spend nothing today, it isn't a saving — it's
a new cost plus a system to maintain.

---
*Verified 28 July 2026. Figures are a snapshot from that day, not a quality signal.*
