# Repo Radar

Safety-first notes on GitHub projects I come across — mostly from social media
posts, where the pitch never mentions what the tool actually asks for.

**Every entry answers "what does this want from me?" before "what does it do?"**
That order is deliberate. A tool's usefulness is easy to find out; its cost to
you is not, and it is usually the part the video leaves out.

---

## Risk ratings

| | Meaning |
|---|---|
| 🟢 | Runs on your own machine or with credentials you fully control. No terms-of-service conflict, no legal exposure, permissive or clearly-stated license, actively maintained. |
| 🟡 | Safe, but conditional — needs a paid third-party account, carries copyleft obligations, is barely maintained, or is only legal within a defined scope. Read the condition before using. |
| 🔴 | Wants your session credentials, breaks a platform's terms, exposes you legally, or cannot be audited at all. Use only with throwaway accounts, or not at all. |

A red rating is not "this is malware". It means **the cost to you is real and the
pitch did not mention it.**

---

## Index

### 🟢 Safe to use

| Project | What it does | ★ | License |
|---|---|---|---|
| [Postiz](repos/postiz.md) | Social media scheduling across 14 platforms | 33.9k | AGPL-3.0 |
| [Lightpanda](repos/lightpanda.md) | Headless browser for AI agents, written in Zig | 32.7k | AGPL-3.0 |
| [Neon](repos/neon.md) | Serverless Postgres with git-style branching | 22.7k | Apache-2.0 |
| [book-to-skill](repos/book-to-skill.md) | Compiles a technical book into an agent skill | 10.6k | MIT |
| [CodeFlow](repos/codeflow.md) | Interactive architecture map of any repo | 4.8k | MIT |

### 🟡 Conditional

| Project | What it does | ★ | The condition |
|---|---|---|---|
| [Strix](repos/strix.md) | Autonomous AI penetration testing | 45k | Only against systems you own or are authorized to test |
| [OpenSEO](repos/open-seo.md) | Semrush/Ahrefs alternative | 8.7k | Requires a paid DataForSEO account |
| [Weft](repos/weft.md) | Language for orchestrating AI systems | 1.7k | Self-declared proof of concept |
| [gbro-collage-broll](repos/gbro-collage-broll.md) | Collage-style B-roll from a voiceover line | 831 | 831 stars, 3 commits — effectively unmaintained |
| [Resource2Skill](repos/resource2skill.md) | Distills skills for operating software from tutorials | 426 | 426 stars, 9 commits — a paper release |
| [Opencodex](repos/opencodex.md) | Free coding agent inside VS Code | 13 | 34 installs; a coding agent is the wrong place to be early |
| [IKEA 3D Downloader](repos/ikea-3d-downloader.md) | Saves `.GLB` models from IKEA product pages | — | The models are IKEA's IP — personal use only |

### 🔴 High risk

| Project | What it does | ★ | Why |
|---|---|---|---|
| [Agent-Reach](repos/agent-reach.md) | Read access to 13 platforms for AI agents | 61.3k | Runs on your session cookies; breaks platform terms |
| [ego (lite)](repos/ego-lite.md) | Browser that shares your logged-in sessions with agents | 2.5k | **MIT covers only the docs — the browser is closed source** |
| [watermarks-remover](repos/watermarks-remover.md) | Strips AI provenance marks from text and files | — | Built to defeat provenance detection; a liability if you publish |
| [Eromify](not-repos/eromify.md) | AI influencer generator | — | Closed-source MCP connector — nothing to audit |
| [Court of Claude](not-repos/court-of-claude.md) | Unknown | — | No public URL; gated behind a comment |

---

## Notes

Write-ups that aren't about a single project.

| Note | What it covers |
|---|---|
| [What actually has to be declared as AI](notes/ai-act-marking.md) | EU AI Act Article 50 — who must mark, who must disclose, and why ordinary marketing copy usually needs neither |

---

## What I learned filling this in

**Star counts prove nothing.** The spread in this batch: 831 stars / 3 commits
versus 22.7k stars / 8,474 commits. Four checks separate them in thirty seconds —
**last commit date, commit count, open issues, license.**

**"Free" always has a reason. Find it.** Three different reasons appear here:

- **OpenSEO** is free because you pay DataForSEO for the data.
- **Agent-Reach** is free because it bypasses official APIs using your account's
  cookies — the potential bill is a ban.
- **Postiz** is genuinely free, because the business model is the hosted version
  and the AGPL protects the project.

Only the third is free in the sense you'd assume. The question is never *what does
it cost*, it's **who pays, and how**.

**Installing code and connecting a service are different decisions.** Open source
code can be read, pinned to a version, and sandboxed. An MCP connector or a tool
holding your session cookies is a remote service that can change after you approve
it, while holding access to your accounts. The second deserves far more caution —
and it is the part these posts never mention.

**When a video asks you to comment a word for the link, the link is the product.**
Several entries here were gated or closed-source. The genuine, famous projects in
the same feed lend them credibility they haven't earned.

**Check what the licence badge actually covers.** [ego (lite)](repos/ego-lite.md)
is the sharpest example: an MIT badge on a repository containing documentation and
a skill file, while the browser you actually install — the one that inherits your
logged-in sessions — is a separate closed-source download. The badge was accurate
and the impression it created was wrong. Ask *which artifact* the licence applies
to, not just what the licence is.

---

## Adding a new entry

Copy [`TEMPLATE.md`](TEMPLATE.md) into `repos/` (or `not-repos/` if it isn't
actually a repository), fill it in, and add a row to the index above.

Fill the safety table first. If you can't answer "what credentials does it want"
and "where does my data go", that's already the finding.
