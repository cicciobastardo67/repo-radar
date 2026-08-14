# Resource2Skill

**`microsoft/Resource2Skill`** · 426 ★ · MIT · Python
<https://github.com/microsoft/Resource2Skill>

*Seen on: Instagram Reels (GithubSignals), "What if an AI agent could watch..."*

---

## 🟡 Safety: conditional — it's a research release, not a product

**426 stars, 9 commits.** Microsoft's official open-source release of an academic
paper (arXiv:2606.29538). Nothing dangerous; nothing finished either.

| Check | Finding |
|---|---|
| **Credentials it wants** | Azure OpenAI or a comparable LLM provider. Scoped, revocable. |
| **Where your data goes** | Your resources and prompts go to whichever LLM you configure. |
| **Platform terms** | N/A. |
| **Legal exposure** | If you feed it third-party tutorial videos or paid courses, the generated skills are derivatives of someone else's material. Keep those private. |
| **License obligations** | MIT — none. |
| **Maintenance** | **9 commits on main.** A paper release, published and largely done. |

### What could go wrong

- **It stops where the paper stopped.** Research code is published to prove a
  result, not to be maintained. Don't build a workflow that must survive.
- Heavy per-domain dependencies: Playwright for web, LibreOffice for PowerPoint,
  fluidsynth plus a soundfont for audio, bpy for Blender. Each one is a thing that
  can break.

### Using it safely

- Treat it as an experiment with a fixed end date. Pin the commit.
- Keep skills built from third-party material out of client deliverables.

---

## What it does

Turns human-created resources — tutorial videos, reference artifacts, articles,
code — into **executable skills that operate real software**. The agent then
browses, composes and runs those skills to produce actual artifacts: web pages,
PowerPoint decks, Excel workbooks, Blender scenes, REAPER-style audio.

## ⚠️ What it is *not*

**It is not a document or knowledge retrieval system.** The repository says so
explicitly. This distinction decides whether it fits a use case:

| | |
|---|---|
| **[book-to-skill](book-to-skill.md)** | *What the document says* — knowledge |
| **Resource2Skill** | *How to produce the artifact* — operating software |
| **Neither** | Professional judgement |

So for a **legal or regulatory agent, this is the wrong tool.** It knows nothing
about laws and doesn't retrieve them. That job belongs to book-to-skill.

For an **auditing workflow** it can fit, but only on the output side: if your
audit deliverables are Excel workbooks or slide decks in a fixed house format,
this is the domain it covers — learning to *produce the deliverable*, not to do
the audit. If your reports are prose documents, it has nothing to offer.

## Requirements

Python 3.11 in a fresh venv, Azure OpenAI or equivalent, plus per-domain system
dependencies.

## Verdict

**Interesting result, wrong shape for knowledge work.** Worth reading the paper.
Not worth building on at 9 commits — and not the answer to "can this be the legal
agent", which it can't.

---
*Verified 14 August 2026. Figures are a snapshot, not a quality signal.*
