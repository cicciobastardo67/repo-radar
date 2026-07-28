# Strix

**`usestrix/strix`** · 45k ★ · Apache-2.0 · Python
<https://github.com/usestrix/strix>

*Seen on: Instagram Reels (Carter Perez) — showed 41.3k stars, gated behind commenting "GUIDE"*

---

## 🟡 Safety: conditional — the condition is legal, not technical

**The tool is well built and safe to run. Pointing it at the wrong target is a
crime.** That is the whole rating.

| Check | Finding |
|---|---|
| **Credentials it wants** | An LLM API key (OpenAI, Anthropic, Google, others) via `LLM_API_KEY`, stored in `~/.strix/cli-config.json`. Scoped, revocable — the good kind. |
| **Where your data goes** | Your target's responses and your prompts go to whichever LLM provider you configure. Relevant if you're testing something confidential. Execution is sandboxed in Docker. |
| **Platform terms** | N/A — but see legal exposure. |
| **Legal exposure** | **This is the point.** Strix runs live exploit attempts. Doing that against a system you don't own or aren't authorized to test is a criminal offence in most jurisdictions — in Italy, art. 615-ter of the penal code and following. Being open source, well-intentioned, or "just testing" changes nothing. |
| **License obligations** | Apache-2.0 — permissive. |
| **Maintenance** | Strong: 638 commits, 4.7k forks, 45k stars. |

### What could go wrong

1. **You point it at something that isn't yours.** The legal line between a
   penetration test and an attack is **written authorization from the system's
   owner**, with a defined scope. Nothing else.
2. **Scope creep during a real engagement.** An autonomous agent following links
   can wander outside the agreed perimeter. Constrain the target list explicitly.
3. **Confidential data reaching your LLM provider** during testing of sensitive
   systems. Pick the provider accordingly.

### Using it safely

Legitimate targets, in plain terms:

- Applications you own.
- Your company's staging environments, with sign-off.
- Purpose-built labs — HackTheBox, TryHackMe, deliberately vulnerable apps.
- Clients who have given you a **written mandate with a defined scope**.

The README says it plainly: *"Only test apps you own or have permission to test.
You are responsible for using Strix ethically and legally."*

---

## What it does

Autonomous AI penetration testing agents: reconnaissance, exploitation attempts,
and validation of findings with **working proofs-of-concept**. Not static
analysis — it runs your code dynamically and tries to break it, which is why it
produces far fewer false positives. If it reports something, it has a
demonstration.

Stack: Python with LiteLLM, the Caido HTTP proxy, Playwright, and the Textual CLI
framework. Interactive mode or headless for CI/CD.

## Requirements

Docker running (pulls its sandbox image on first run), plus an LLM API key.
Configured via `STRIX_LLM` and `LLM_API_KEY`.

## Verdict

**A serious, well-engineered tool.** The highest-value use is continuous: wire it
into CI so every build gets a real security pass on **your own** code.

The condition isn't bureaucratic caution — it's the difference between a
professional practice and a criminal charge.

---
*Verified 28 July 2026. Figures are a snapshot from that day, not a quality signal.*
