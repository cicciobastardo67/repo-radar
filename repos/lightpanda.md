# Lightpanda Browser

**`lightpanda-io/browser`** · 32.7k ★ · AGPL-3.0 · Zig
<https://github.com/lightpanda-io/browser>

*Seen on: Instagram Reels (Marco Kazandjieff), "Stop running full Chrome just to scrape the web"*

---

## 🟢 Safety: low risk

**Nothing to hand over.** It runs locally and asks for no credentials.

| Check | Finding |
|---|---|
| **Credentials it wants** | None. It's a browser binary you run yourself. |
| **Where your data goes** | Nowhere — local process. Supports proxies and network interception if you want control over egress. |
| **Platform terms** | Neutral. It respects `robots.txt`. What you scrape with it is your responsibility, as with any browser. |
| **Legal exposure** | None from the tool. Scraping law depends entirely on target and jurisdiction. |
| **License obligations** | **AGPL-3.0.** Embed it in a network-accessible service and you owe your source. A commercial cloud offering exists as the alternative path. |
| **Maintenance** | Active, well-staffed. |

### What could go wrong

- **It's beta and says so.** The README: *"You may still encounter errors or
  crashes."* Hundreds of Web APIs are unimplemented. Complex sites can fail where
  Chrome succeeds — a reliability risk, not a security one.
- **The AGPL** is the real trap for commercial use. Same shape as
  [Postiz](postiz.md).

### Using it safely

- Keep a Chrome/Chromium fallback path in any pipeline that must not break.
- Check the license question before it's load-bearing in a product.

---

## What it does

A headless browser written from scratch for AI agents and automation — not a
Chromium fork. Exposes a Chrome DevTools Protocol server, so Puppeteer and
Playwright connect to it as if it were Chrome.

Claimed gains over headless Chrome, on 100 pages:

| | Lightpanda | Headless Chrome |
|---|---|---|
| Memory | ~123 MB | ~2 GB |
| Time | ~5 s | ~46 s |

Stack: Zig 0.15.2, V8 for JavaScript, `html5ever` for parsing, libcurl for HTTP.
Supports DOM, XHR/Fetch, cookies, proxies, network interception.

## Requirements

Homebrew, nightly binaries, or build from source.

```bash
./lightpanda fetch <url>   # dump a page
./lightpanda serve         # CDP server for Puppeteer/Playwright
./lightpanda agent         # AI-driven browsing in plain English
```

## Verdict

If you do web automation at volume, the RAM and time savings are real and
measurable. Worth adopting **with a Chrome fallback**, and with the AGPL settled
before it matters.

---
*Verified 28 July 2026. Figures are a snapshot from that day, not a quality signal.*
