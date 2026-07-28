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

### 🔴 High risk

| Project | What it does | ★ | Why |
|---|---|---|---|
| [Agent-Reach](repos/agent-reach.md) | Read access to 13 platforms for AI agents | 61.3k | Runs on your session cookies; breaks platform terms |
| [Eromify](not-repos/eromify.md) | AI influencer generator | — | Closed-source MCP connector — nothing to audit |
| [Court of Claude](not-repos/court-of-claude.md) | Unknown | — | No public URL; gated behind a comment |

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
Two of the twelve entries here were gated or closed-source. The genuine, famous
projects in the same feed lend them credibility they haven't earned.

---

## Adding a new entry

Copy [`TEMPLATE.md`](TEMPLATE.md) into `repos/` (or `not-repos/` if it isn't
actually a repository), fill it in, and add a row to the index above.

Fill the safety table first. If you can't answer "what credentials does it want"
and "where does my data go", that's already the finding.
