# gbro-collage-broll

**`pyang5166/gbro-collage-broll`** · 831 ★ · MIT · Python
<https://github.com/pyang5166/gbro-collage-broll>

*Seen on: Instagram Reels (GithubSignals), "A smart three-step"*

---

## 🟡 Safety: conditional — effectively unmaintained

**831 stars, 3 commits.** That gap is the finding, and it's the clearest example
in this archive of why star counts mean nothing.

| Check | Finding |
|---|---|
| **Credentials it wants** | A `GEMINI_API_KEY` from Google AI Studio. Scoped and revocable — fine. |
| **Where your data goes** | Your prompts and generated frames go to Google's Gemini API. Normal for the task. |
| **Platform terms** | Compliant — official API, paid properly. |
| **Legal exposure** | None. |
| **License obligations** | MIT — none. |
| **Maintenance** | **3 commits on main.** This is a well-documented script, not a maintained project. If it breaks when the Gemini model changes, nobody is fixing it. |

### What could go wrong

- **Model deprecation kills it.** It pins `gemini-omni-flash-preview` — a preview
  model. Preview models get retired. With three commits of history, don't expect
  an update.
- **Video generation costs add up fast** if you bypass the approval gates.

### Using it safely

- Set a billing cap on the Google AI Studio key.
- Read `SKILL.md` before running it — that's where the actual logic lives.
- Treat it as a script you'll maintain yourself, not a dependency.

---

## What it does

Turns a ~5-second voiceover line into an editorial halftone paper-collage B-roll
clip, assembling elements from an empty scene with a stop-motion feel.

### The genuinely good idea: three approval gates

Video API calls are expensive, so each stage is approved before the next:

| Gate | Stage | Cost of a redo |
|---|---|---|
| 1 | Confirm the visual metaphor | **Free** — it's text |
| 2 | Review the static frame | Cheap — one image |
| 3 | Generate the video | Expensive |

As the README puts it: regenerating one frame costs far less than re-running a
video. **This pattern is the real takeaway** and it transfers to any expensive AI
pipeline — put human approval *before* the costly operation, not after.

## Requirements

Python 3.10+, FFmpeg/FFprobe, YAML config, `google-genai >= 2.10.0`, and a Gemini
API key.

## Verdict

**Useful only if you produce social video in this exact aesthetic.** Otherwise
take the three-gate pattern and leave the code.

---
*Verified 28 July 2026. Figures are a snapshot from that day, not a quality signal.*
