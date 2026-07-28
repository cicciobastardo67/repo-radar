# Weft

**`WeaveMindAI/weft`** · 1.7k ★ · O'Saasy License · Rust + SvelteKit
<https://github.com/WeaveMindAI/weft>

*Seen on: Instagram Reels (Esserci), "reso gratis per tutti" — gated behind commenting "LINGUA"*

---

## 🟡 Safety: conditional — it isn't finished, and says so

**No security concern. The condition is maturity and an unusual license.**

| Check | Finding |
|---|---|
| **Credentials it wants** | Whatever your workflows need (LLM keys, database, Discord/Slack tokens). Nothing unusual for an orchestration tool. |
| **Where your data goes** | Self-hosted — your infrastructure. |
| **Platform terms** | N/A. |
| **Legal exposure** | None. |
| **License obligations** | **"O'Saasy License"** — MIT plus a restriction on reselling it as a SaaS. A non-standard license, which means no established legal reading. If commercial use is the plan, read the actual text rather than assuming it behaves like MIT. |
| **Maintenance** | **The problem.** `main` is inactive; real work happens on the `mvp` branch, with an August 2026 release planned. |

### What could go wrong

- **You build on a moving foundation.** The README's own warning: treat it as
  *"a foundation to build on, not a finished product."* Pre-1.0 with an inactive
  default branch means breaking changes without notice.
- **The license is untested.** "MIT except SaaS" restrictions are common in
  spirit and inconsistent in wording. Don't assume you know what it permits.

### Using it safely

- Experiment on the `mvp` branch, pin a commit, expect to rewrite.
- Don't put anything production-critical on it before the August 2026 release.

---

## What it does

A programming language for orchestrating AI systems, where LLMs, humans, APIs and
infrastructure are **native language primitives**. The interesting ideas:

- **Humans as a first-class type.** Execution pauses, sends a form to a person,
  and resumes days later.
- **Durable execution.** Programs survive crashes, via Restate.
- **End-to-end typing.** The compiler validates connections before runtime.
- **Dual views.** The same program is both code and an editable visual graph.

Stack: Rust + Restate + PostgreSQL backend, SvelteKit/Svelte 5 frontend, Docker
and optional Kubernetes.

The framing from the README: *"In 2026, real software calls LLMs, spins up
databases, waits for humans, browses the web, coordinates agents. Where are those
primitives?"*

## Requirements

```bash
git clone https://github.com/WeaveMindAI/weft.git
cd weft && cp .env.example .env
./dev.sh server      # terminal 1
./dev.sh dashboard   # terminal 2
# http://localhost:5173
```

## Verdict

**Genuinely interesting ideas, near-zero practical use today.** Worth a look after
the August 2026 MVP lands. Not worth building on before then.

---
*Verified 28 July 2026. Figures are a snapshot from that day, not a quality signal.*
