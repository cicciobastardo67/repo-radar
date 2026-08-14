# Opencodex

**Opencodex** · 13 ★ · MIT · VS Code extension
*34 installs on the VS Code Marketplace*

*Seen on: promo screenshot — "A free, open-source coding agent inside VS Code"*

---

## 🟡 Safety: conditional — far too new to trust with a codebase

**13 stars. 34 installs.** The idea is fine; the adoption is near zero, and that
matters more than usual for this category.

| Check | Finding |
|---|---|
| **Credentials it wants** | None to start — that's the pitch. Optionally a free provider's key, or local models via Ollama. |
| **Where your data goes** | To whichever free provider you pick. **"Free model" usually means your prompts are training data.** Check each provider's terms — that's your client's code going into someone's training set. |
| **Platform terms** | Depends on the provider you connect. |
| **Legal exposure** | None directly, but see the confidentiality point above — client code under NDA should not go to a free tier you haven't read the terms of. |
| **License obligations** | MIT — none. |
| **Maintenance** | Brand new, essentially unreviewed. |

### What could go wrong

**A coding agent extension is a high-trust install.** It reads your whole
workspace, edits files, and runs commands. With 34 installs, effectively nobody
has audited it. That's not an accusation — it's the base rate: an unvetted
extension with that surface area is a supply-chain risk regardless of intent.

The second issue is quieter and more likely to bite: **free model tiers usually
pay for themselves with your data.** For an agency working under client NDAs,
routing client code through an unread free tier is the actual exposure here, not
the extension itself.

### Using it safely

- **Wait.** Nothing is lost by revisiting in six months.
- If you must try it: a scratch project, never client code.
- If you want local and private, Ollama is the config to use — the models run on
  your machine and nothing leaves.

---

## What it does

A Codex-style coding agent that runs entirely inside VS Code. Pick a provider and
a free model, describe what you want. Presents an ordered plan before working and
keeps it pinned while it runs. No account or API key needed to start.

## Verdict

**Good idea, wrong moment.** The "no account, free models, or local via Ollama"
angle is genuinely attractive. But a coding agent is the last category where you
want to be install number 35.

Revisit when it has real adoption and someone other than the author has read it.

---
*Verified 14 August 2026 from the project's own README. Figures are a snapshot, not a quality signal.*
