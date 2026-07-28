# Eromify

**Not a repository.** Closed-source commercial SaaS · <https://eromify.com>

*Seen on: Instagram Reels (Kim in Space), showing `eromify.com/mcp` being added to Claude as a custom connector — gated behind commenting "Claude"*

---

## 🔴 Safety: high risk

**There is no source to read.** The pitch is an open-source-style "add this
connector" demo for a closed commercial product — and approving an MCP connector
is a bigger decision than the video implies.

| Check | Finding |
|---|---|
| **Credentials it wants** | An account, and — the real ask — **approval as a custom MCP connector** inside Claude. |
| **Where your data goes** | Their servers. Anything passing through connector calls leaves your machine. |
| **Platform terms** | Depends where you publish the output. Social and payment platforms differ sharply on synthetic personas and on mandatory disclosure. |
| **Legal exposure** | None from the tool itself. Disclosure obligations for AI-generated personas vary by platform and jurisdiction. |
| **License obligations** | Proprietary. Nothing auditable. |
| **Maintenance** | Unknown — no public repository. |

### What approving an MCP connector actually grants

This is the transferable part, worth more than anything specific to this product.

**A custom MCP connector is not an app you download.** It's a third-party server
you authorize to expose tools inside your conversations. Concretely:

- the server decides **which tools** to offer, and **can change them after you
  approve it**;
- tool descriptions are **text they write** that enters the model's context;
- data flowing through those calls **reaches their servers**.

Claude states it directly in the dialog visible in the screenshot: *"Only use
connectors from developers you trust."* That is not legal boilerplate. The trust
level is comparable to installing a browser extension with broad permissions — not
to visiting a website.

### Using it safely

- Connect MCP connectors only from vendors you'd have paid anyway and would
  vouch for.
- **Never in an account holding personal, work, or client data.** Use a separate
  account to try anything unknown.
- Re-check what a connector exposes periodically — the tool list you approved is
  not necessarily the tool list you have.

---

## What it is

A commercial AI creator platform generating photorealistic "AI influencers" with
consistent identity across images and video — diffusion models (FLUX and others)
plus proprietary identity-lock technology. Credit-based pricing from roughly $5
for 200 credits up to a ~$99/month Creator plan.

A Fanvue tab (subscription adult content platform) was open in the same
screenshot, indicating the intended use case.

### Verification note

`eromify.com/mcp` and a third-party review both returned **HTTP 403** when
checked. The MCP endpoint's documentation and the reviews could not be verified
directly — **feature and pricing details above come from secondary sources.**

## Verdict

Out of category compared to everything else here: not code you can read, but a
paid service promoted through a gated Reel.

If the product is useful to you, evaluate it as you would any SaaS. But treat
**connecting it to Claude as a separate and more serious decision than buying
it** — and one that a 30-second video is not a basis for.

---
*Checked 28 July 2026.*
