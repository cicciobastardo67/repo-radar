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
| **Credentials it wants** | Twitter/X cookie, Reddit login, browser session for Facebook/Instagram, cookie for XiaoHongShu. Session cookies are equivalent to passwords — they grant full account access and bypass 2FA. **Stored correctly**, though — see the code review. |
| **Where your data goes** | Local, and there is no telemetry. **One exception:** the generic web channel proxies every URL through the third-party `r.jina.ai`. See the code review. |
| **Platform terms** | Breaches the terms of service of most platforms it supports. Automated access via a user session is exactly what those clauses prohibit. |
| **Legal exposure** | Low for reading public content; the realistic penalty is account-level, not legal. |
| **License obligations** | MIT — none. |
| **Maintenance** | Excellent: 334 commits, very active, 61.3k stars (was ~31k mid-2026). |

### What could go wrong

1. **The account you authenticate gets banned.** Not hypothetical — this is the
   normal outcome when platforms detect automated session use. This is the whole
   reason for the red rating.
2. **Any URL you read through the generic web channel is disclosed to Jina AI.**
   Matters if you read client staging sites or unpublished pages.
3. **It breaks constantly.** The project's headline feature is multi-backend
   routing with automatic fallback — "preferred + alternate" per platform. That
   exists *because* platforms actively close these access paths. Good engineering,
   but it tells you the ground is always moving.

### Using it safely

- **Throwaway accounts only.** Never your main account, never a work account,
  never one tied to a client or to anything you'd mind losing.
- Don't build anything that must keep working on top of it. Treat it as a
  research tool, not infrastructure.
- For anything confidential, avoid the generic web channel — it goes through
  Jina. Use a site-specific channel, or fetch it yourself.

---

## Code review

Read at commit level on 9 August 2026. **This section corrects an earlier claim in
this file** that cookies sat unprotected on disk — that was inferred from the
README and is wrong.

### Credential handling is better than average

```python
os.fchmod(fd, stat.S_IRUSR | stat.S_IWUSR)   # 0600, on the open descriptor
target.mkdir(mode=0o700, parents=True, exist_ok=True)
```

It uses `fchmod` on an already-open descriptor rather than `open()` then
`chmod()`. The second form leaves a window where the file exists with permissive
modes. Choosing the first is a deliberate, informed decision.

Also present:

- Secret redaction in output — tokens, keys, passwords, cookies, signatures
- An explicit warning that passing secrets as CLI arguments leaks them into shell
  history
- `doctor` checks config file permissions and tells you how to fix them
- **Five dedicated security test files**: `test_cookie_security.py`,
  `test_private_file_writes.py`, `test_home_isolation.py`,
  `test_doctor_credential_boundaries.py`, `test_cookie_extract_perms.py`
- SSRF protection in `normalize_public_http_url` — rejects non-public targets,
  control characters, backslashes, malformed authorities
- A response size cap on fetches
- **No telemetry.** Egress reaches only the platforms themselves plus three named
  services (Jina, Exa, Groq)

### The undocumented finding: everything falls back through Jina

```python
def can_handle(self, url: str) -> bool:
    return True  # Fallback — handles any URL

def read(self, url: str) -> str:
    jina_url = f"https://r.jina.ai/{url}"
```

`can_handle` always returns `True`, so the generic web channel is the catch-all
for any URL without a dedicated channel. **The URL and its content pass through a
third party.** This is not stated prominently anywhere in the documentation.

### Smaller findings

| | |
|---|---|
| **Chinese-language output** | Error messages, `doctor` output and channel descriptions are in Chinese. When something breaks, the diagnostic may be in a language your team cannot read. |
| **`cli.py` is 2,350 lines** | 41 functions in one file. Not a bug, but it's where maintenance pain will concentrate. |
| **Minimal lint rules** | `ruff` enables only `E, F, I`. For a project handling credentials, subprocesses and network I/O, the `S` (security) ruleset would be appropriate. |

### What this changes

The rating stays 🔴, but the reason narrows to one thing: **using session cookies
breaches platform terms and gets accounts banned.** Not because the code is
careless — it isn't. Someone competent wrote this.

"Well-built tool, unavoidable access model" is a different warning from "sloppy
tool", and it's the accurate one.

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
*Verified 28 July 2026; source code reviewed 9 August 2026. Figures are a snapshot, not a quality signal.*
