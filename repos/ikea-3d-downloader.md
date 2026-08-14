# IKEA 3D Model Downloader

**Tampermonkey userscript** · updated 30 January 2026

*Seen on: promo screenshot — adds a "Download 3D" button to IKEA product pages*

---

## 🟡 Safety: conditional — it works, but the files aren't yours

**Technically trivial and effective.** The constraint is copyright, and for an
agency it's the whole story.

| Check | Finding |
|---|---|
| **Credentials it wants** | None. |
| **Where your data goes** | Nowhere — the download comes straight from IKEA. |
| **Platform terms** | Grey. It saves a file the site already sends your browser, but IKEA's terms don't contemplate you keeping it. |
| **Legal exposure** | **The models are IKEA's intellectual property.** Personal use is one thing; commercial client work is infringement. |
| **License obligations** | The script's licence is irrelevant — the **assets** are what's restricted. |
| **Maintenance** | Last bugfix January 2026. A short script; low maintenance need. |

### How it works

No magic involved. IKEA already serves those `.GLB` models to the browser to power
its own "View in 3D" feature. The script adds a button that saves the file the
page is already sending you, naming it from the product and colour. That's why it
works across IKEA's different language sites.

### What could go wrong

1. **Using IKEA models in client work is copyright infringement.** Renders,
   mockups, visualisations delivered to a client, anything commercial. IKEA is
   exactly the kind of company with a legal department that notices.
2. **Userscripts run with the page's privileges.** It's short — read it before
   installing. That's a thirty-second check, not a hypothetical.

### Using it safely

- Personal use, as the README describes: trying furniture in your own home
  planning software. Fine.
- **For client renders, buy properly licensed models.** Not a technical
  limitation — a licensing one, and the only version that survives a question
  from the client's lawyer.

---

## Verdict

**Fine for you at home, not for KhmerADV deliverables.** The tool does what it
says. The output is someone else's property, and an agency is precisely the actor
that can't plead personal use.

---
*Verified 14 August 2026 from the project's own README.*
