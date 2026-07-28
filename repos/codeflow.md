# CodeFlow

**`braedonsaunders/codeflow`** · 4.8k ★ · MIT · JavaScript
<https://github.com/braedonsaunders/codeflow>

*Seen on: Instagram Reels (RammCodes), "Turns any GitHub repository into interactive visualizations"*

---

## 🟢 Safety: low risk

**Lowest-friction thing in this archive** — no install, no account, no backend.

| Check | Finding |
|---|---|
| **Credentials it wants** | None. No account, no sign-up. |
| **Where your data goes** | Runs entirely in the browser; the README's claim is *"Your code never leaves your machine."* For public repos it fetches from GitHub client-side. |
| **Platform terms** | N/A. |
| **Legal exposure** | None. |
| **License obligations** | MIT — none. |
| **Maintenance** | Reasonable: 129 commits, 737 forks, only 3 open issues. |

### What could go wrong

- **Verify the privacy claim yourself if you point it at private code.** "Runs in
  your browser" is checkable — open devtools, watch the network tab, confirm
  nothing leaves. It's a single HTML file, so this takes a minute. Worth doing
  once before you trust it with anything proprietary.
- Its security scanning and health scores are heuristics, not an audit. Useful as
  a first look, not as assurance.

### Using it safely

- Public repos: nothing to think about, just use it.
- Private or client code: do the devtools check first, or run the HTML file
  locally offline.

---

## What it does

Paste a GitHub URL, get an interactive architecture map: how files connect, plus
**blast radius analysis** — *if I change this file, what breaks?* Also does
pattern detection, security heuristics, and a code health score. Supports 40+
languages.

Stack: a single HTML file with React 18, D3.js 7 and Babel. 100% browser-based,
no backend. There's also a GitHub Action that keeps a summary card in your README
up to date.

## Requirements

A browser.

## Verdict

**Try it first, because trying it costs nothing.** Genuinely useful when you're
dropped into a codebase you don't know and need to see the shape of it before
reading files.

---
*Verified 28 July 2026. Figures are a snapshot from that day, not a quality signal.*
