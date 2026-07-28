# book-to-skill

**`virgiliojr94/book-to-skill`** · 10.6k ★ · MIT · Python
<https://github.com/virgiliojr94/book-to-skill>

*Seen on: Instagram Reels (Marco Kazandjieff), "Turn any book into an AI agent skill in one command". The username was obscured by the presenter's hand in the video and had to be found by search — the URL shown on screen was not usable.*

---

## 🟢 Safety: low risk

**Local file processing with no credentials and no network dependency.**

| Check | Finding |
|---|---|
| **Credentials it wants** | None of its own. Analysis runs through whichever agent you already use. |
| **Where your data goes** | Your books stay on disk. Extracted text remains local and inspectable — deliberately, so you can verify quotes rather than trust them. |
| **Platform terms** | N/A. |
| **Legal exposure** | One thing to keep in mind: converting a book you own for personal use is ordinary; **redistributing the generated skill files** means redistributing a derivative of copyrighted material. Keep compiled skills from commercial books private. |
| **License obligations** | MIT — none. |
| **Maintenance** | Healthy: 89 commits, 1.3k forks, #10 Python Repository of the Day on Trendshift (May 2026). |

### What could go wrong

- **Sharing the output.** The tool is fine; publishing a skill compiled from a
  copyrighted book is the mistake to avoid.
- Extraction quality varies by source format. PDFs with heavy layout come out
  worse than EPUBs.

### Using it safely

- Keep compiled skills in a private location.
- Spot-check a chapter against the original before trusting it for anything that
  matters — the retained source text is there precisely for that.

---

## What it does

Compiles a technical book — PDF, EPUB, DOCX, HTML, RTF, Markdown,
reStructuredText, AsciiDoc, TXT, MOBI/AZW — into a structured **agent skill**: a
`SKILL.md` plus per-chapter files, a glossary, patterns, and a cheatsheet. The
agent loads only the chapter it needs, when it needs it.

**The token claim, and why it holds up.** The README claims **24×–51× fewer
tokens** than dumping the book into context to answer one question. The mechanism
is sound: navigation cost is paid **once at compile time**, then at runtime you
carry a ~4K-token resident core plus one pre-compiled chapter. No discovery loop,
no compress-to-fit on every turn.

Follows the open Agent Skills standard, so one skill runs on Claude Code, GitHub
Copilot CLI, and Amp.

## Requirements

`pip install book-to-skill`, or clone into your skills folder (`~/.claude/skills/`,
`~/.copilot/skills/`, `~/.agents/skills/`). Format-specific dependencies:
pdftotext or Docling for PDFs, ebooklib for EPUBs, python-docx, beautifulsoup4,
striprtf as needed.

## Verdict

**The most immediately useful thing here if you have technical PDFs you never
read.** Low risk, low effort, and the underlying pattern — precompile structure
once, load on demand — is the right way to give an agent documentation.

---
*Verified 28 July 2026. Figures are a snapshot from that day, not a quality signal.*
