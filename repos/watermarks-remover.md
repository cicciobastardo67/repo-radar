# watermarks-remover

**`guillaumemeyer/watermarks-remover`** · v0.3.0 · MIT · Python
<https://github.com/guillaumemeyer/watermarks-remover>

*Seen on: promo screenshot — "strip multi-vendor AI provenance marks from text and files"*

---

## 🔴 Safety: high risk — for the business, not the machine

**The code is harmless. Using it is the problem.** It does exactly one thing:
makes AI-generated content stop looking AI-generated.

| Check | Finding |
|---|---|
| **Credentials it wants** | None. Stdlib Python scripts plus an agent skill. |
| **Where your data goes** | Local. |
| **Platform terms** | **Meta, TikTok and YouTube require AI-content labels.** Stripping provenance to avoid them breaches those policies. |
| **Legal exposure** | **The real issue — see below.** |
| **License obligations** | MIT — none. |
| **Maintenance** | CI passing, v0.3.0, 50 forks. Technically fine. |

### What it removes

| Layer | Target |
|---|---|
| A | Invisible Unicode, exotic spaces, bidi and tag characters |
| B | Statistical token-sampling text watermarks, via agent rewrite |
| Files | C2PA / EXIF / XMP / document properties — PNG, JPEG, SVG, PDF, DOCX, ODT, HTML, Markdown |

Vendors targeted by class: Claude, Gemini / SynthID-Text, OpenAI provenance
surfaces, open-LLM Kirchenbauer-style marks.

The README frames this as *"privacy and hygiene on content you own"*. Stripping
EXIF from your own photos before publishing is a real and legitimate need. But
layers A and B are not about EXIF — they exist to defeat AI provenance detection.

### Why this is a problem for an agency specifically

**EU AI Act Article 50** has applied since **2 August 2026**:

- **50(2)** puts a machine-readable marking duty on the **provider** — OpenAI,
  Anthropic, Google. Those marks exist to satisfy a legal obligation.
- **50(4)** puts a disclosure duty on the **deployer**, for deep fakes and for
  text informing the public on matters of public interest.

You have no duty to *add* markers. But **removing a mark the provider was legally
required to apply is a different act from simply not adding one.** The first is a
lawful omission; the second is an action taken to defeat a compliance mechanism.

Add to that: platform policies requiring AI labels, and the contractual and
reputational damage if a client discovers that provenance was stripped from work
delivered as original.

### If you have a legitimate need

Metadata hygiene is real — EXIF often carries GPS coordinates, device IDs and
names you don't want published. **Use a plain EXIF stripper for that.** A tool
built to defeat multi-vendor AI provenance detection is not the right instrument
for "remove the GPS tag", and choosing it is hard to explain later.

---

## Verdict

**Keep it out of the agency workflow.** Not a moral position — a liability one.
Whoever publishes carries the responsibility, and this tool's whole purpose is to
remove the evidence that would otherwise be there.

See [the note on Article 50](../notes/ai-act-marking.md) for what you actually
have to declare — which for ordinary marketing copy is less than most people
assume.

---
*Verified 14 August 2026 from the project's own README.*
