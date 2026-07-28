# Neon

**`neondatabase/neon`** · 22.7k ★ · Apache-2.0 · Rust
<https://github.com/neondatabase/neon>

*Seen on: Instagram Reels (AI Agent News), "Open source projects you should know"*

---

## 🟢 Safety: low risk

**The most conventional, best-governed project in this archive**, and the only one
with a fully permissive license.

| Check | Finding |
|---|---|
| **Credentials it wants** | None for the open source code. The managed service uses a normal account. |
| **Where your data goes** | Self-hosted: your servers. Managed: theirs, like any database provider — evaluate as you would AWS RDS. |
| **Platform terms** | N/A. |
| **Legal exposure** | None. |
| **License obligations** | **Apache-2.0** — permissive, no copyleft. Use it commercially, closed source, however you like. The cleanest license here. |
| **Maintenance** | The strongest signal in the set: **8,474 commits**, 1.0k forks, backed by a funded company. |

### What could go wrong

- **Self-hosting complexity is the real risk.** Three distributed components —
  Pageserver (storage), Safekeepers (WAL redundancy), stateless compute nodes.
  Build requires protobuf 3.15+, the Rust toolchain, several system libraries, and
  build paths cannot contain spaces. Running this yourself means owning the
  operational burden of a distributed storage system. Most people should not.
- Standard managed-service considerations otherwise: pricing at scale, egress,
  region choice.

### Using it safely

- **Use the managed service.** There's a free tier. The value of the open source
  code here is that you can't be locked in — not that you should be running it.

---

## What it does

Serverless Postgres. Separates storage from compute, which enables autoscaling,
scale-to-zero when idle, and the headline feature: **git-style database
branching.** Branch the database, test a schema migration or a feature, throw the
branch away if it breaks. Excellent for staging environments and per-PR previews.

## Requirements

Managed: a browser. Self-hosted: see the complexity note above.

## Verdict

**If you need a database for a new project, start here.** Database branching pays
for itself the first time a migration goes wrong.

Take it as a service, not as a self-hosting project.

---
*Verified 28 July 2026. Figures are a snapshot from that day, not a quality signal.*
