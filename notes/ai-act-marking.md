# What actually has to be declared as AI — EU AI Act, Article 50

*Written 14 August 2026. Article 50 has applied since 2 August 2026, so
enforcement practice is new for everyone. This is a reading of the text, not
legal advice — have a lawyer confirm your review process, since you publish for
clients.*

---

## The mistake everyone makes

There are **two separate obligations**, and they fall on **different parties**.

| | Article 50(2) — **marking** | Article 50(4) — **disclosure** |
|---|---|---|
| **Who** | The **provider** — OpenAI, Anthropic, Google | The **deployer** — you |
| **What** | Mark output machine-readable as artificially generated | Tell people the content is AI-generated |
| **Applies to** | Synthetic audio, image, video **and text** | Deep fakes, and text informing the public on matters of public interest |

**You have no obligation to add markers.** That duty belongs to the model
provider, and it's why those marks exist in the output in the first place.

---

## Does marketing copy need a disclosure?

Generally **no**, for two independent reasons.

**1. It isn't public-interest information.** The text duty in 50(4) covers text
*"published with the purpose of informing the public on matters of public
interest"* — journalism and matters of public concern. Advertising copy is
commercial communication, a different thing.

**2. The editorial exception.** Even where the duty applies, it does not apply
where the content *"has undergone a process of human review or editorial control
and where a natural or legal person holds editorial responsibility for the
publication"*.

So: Reel copy written by AI from a client brief, reviewed by you before
publishing → **no Article 50 disclosure duty on the text.**

### But the review has to be real

The Commission's guidelines are specific, and this is the part that protects you:

- **Human review** means deliberate examination of the *substance* by a person
  with relevant knowledge and professional judgement on the subject matter.
- **Editorial responsibility** means someone holds ultimate legal responsibility
  for publication.
- Checks must be **substantive, not superficial or cursory approval**.

**Write this into your process and record it.** A named reviewer per deliverable
is what turns the exception from an argument into a fact.

---

## Images are less automatic than people assume

The 50(4) duty covers image, audio or video **constituting a deep fake** —
content resembling real persons, objects, places or events, appearing authentic.

An obviously stylised or clearly synthetic illustration isn't automatically a deep
fake. The rule is not "always mark images" either — but this is the area where
getting it wrong is most visible, so it deserves more care than text.

---

## Three things the AI Act does not settle

**1. Platform rules are a separate track.** Meta, TikTok and YouTube require AI
labels by contract. The law not requiring a disclosure doesn't mean the platform
doesn't. Check the platform policy per channel.

**2. Not declaring is not the same as removing.** You have no duty to *add* a
marker. Actively **stripping** a mark the provider was legally required to apply
is a different act — a lawful omission versus an action taken against a
compliance mechanism. See [watermarks-remover](../repos/watermarks-remover.md).

**3. Advertising law still applies.** Rules against misleading commercial
communication predate all of this and are unaffected by it.

---

## Practical summary

| Content | Disclosure duty on you? |
|---|---|
| Marketing copy, reviewed by a named person | **No** |
| Text informing the public on public-interest matters, unreviewed | **Yes** |
| Deep fake — realistic depiction of real people or events | **Yes** |
| Clearly synthetic illustration | Generally no, but judge case by case |
| Anything, where the platform's own policy requires a label | **Yes, by contract** |

**The cheapest insurance is the review record.** Substantive human review with a
named responsible person removes the text obligation and is the thing you'd point
to if anyone asks.

---

## Sources

- [European Commission — FAQ on Article 50 transparency obligations](https://digital-strategy.ec.europa.eu/en/faqs/transparency-obligations-under-article-50-ai-act)
- [Bird & Bird — first impressions of the final Article 50 guidelines](https://www.twobirds.com/en/insights/2026/european-commission-adopts-final-guidelines-on-ai-act-article-50-transparency-obligations-first-impr)
- [Practical guide to Article 50](https://artificialintelligenceact.eu/transparency-rules-article-50/)
