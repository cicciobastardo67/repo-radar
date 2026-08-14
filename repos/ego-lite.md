# ego (lite)

**`citrolabs/ego-lite`** · ~2.5k ★ · **MIT covers only the skill and docs** · macOS only
<https://github.com/citrolabs/ego-lite>

*Seen on: promo page — "#1 Repository Of The Day" on GitHub Trending, "The best browser for both you and your AI agents"*

---

## 🔴 Safety: high risk

**The MIT badge is not on the thing you run.** The repository contains the agent
skill and the documentation. **The browser itself is a separate, closed-source
download.** You cannot read the code of the program that gets your sessions.

| Check | Finding |
|---|---|
| **Credentials it wants** | The premise of the product: it **shares your logged-in browser state — cookies and active sessions — with AI agents**. The pitch names GitHub, Jira, and internal admin panels. |
| **Where your data goes** | Unknown. The binary is closed source, so this cannot be verified — only trusted. |
| **Platform terms** | You're using your own sessions in your own browser, so no third-party breach. |
| **Legal exposure** | None directly. |
| **License obligations** | MIT on the repo — but that covers documentation and a skill file, not the browser. **Check what the license badge actually applies to.** |
| **Maintenance** | Repo created April 2026, ~2.5k stars, 121 forks. Young but popular. |

### What could go wrong

1. **An unauditable binary inherits your live sessions.** Not a throwaway account —
   your real, daily, logged-in profile, including whatever internal tooling you're
   signed into. If it misbehaves, there is no source to check and no way to know.
2. **The trust ask is larger than it looks.** "No passwords, no API keys" sounds
   safer. It isn't: session cookies *are* the credential, and they bypass 2FA.
   Skipping the password is not the same as reducing access.
3. **macOS only.** Apple Silicon and Intel. Windows and Linux are on the roadmap
   with no date. If your team isn't all on Mac, it's not an option anyway.

### Using it safely

- **Not with a work profile.** If you try it, use a clean browser profile signed
  into nothing that matters.
- Treat it exactly like [Agent-Reach](agent-reach.md): the risk is the account,
  not the tool — except here you also can't read the code.

---

## What it does

A Chromium-based desktop browser by Citro Labs that lets AI agents drive a real
browser using your existing logged-in state. Ships with an `ego-browser` skill for
terminal agents — Claude Code, Cursor, Codex. Pitched as zero cost, zero config.

The idea is genuinely useful: agents usually can't reach anything behind a login,
and this removes that wall.

## Verdict

**The problem is not the idea, it's the packaging.** An open-source badge on a
repository of docs, wrapping a closed-source binary that takes your live sessions,
is precisely the pattern this archive exists to catch.

Same lesson as [Eromify](../not-repos/eromify.md), different costume: **check what
the license badge actually covers before treating something as open source.**

---
*Verified 14 August 2026. Figures are a snapshot, not a quality signal.*
