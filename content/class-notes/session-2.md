---
title: "Session 2 — In-Class Notes"
---

# Session 2 — In-Class Notes

## TED Talk Discussion (Wen vs Harris)

**Core framing:** Anarchy vs dystopia — two failure modes for AI governance.

- **Lock down AI** = techno-feudalism (concentration of power, gatekeeping access)
- **Unlock AI** = wild west (no guardrails, race to the bottom)

**Harris critique:** Still mostly "won't it be nice if we could all get along" — aspirational without a concrete mechanism. Proposes restricting AI access for kids, but positions it right next to surveillance as a solution, which undermines the civil liberties framing.

**Pattern recognition:** People were optimistic about social media, then optimistic about AI — same cycle. The techno-optimism doesn't learn from the previous round.

**Wen vs Harris split:**
- **Wen** says trust yourself — agency is individual, the designer/user has to make the call
- **Harris** says the systems are bigger than individuals — structural forces override personal choice

## Extraction (Capability 1)

**Definition:** The process of existing knowledge flowing from subject matter experts into an AI system.

**Two modes of extracted knowledge:**
- **Procedural skills** — how to do things (e.g., how to program, how to diagnose). Gets codified into the model's weights and architecture through training.
- **Pure information** — facts, dates, text, step-by-step guides. Gets looked up via RAG rather than baked into the model itself.

**Examples of tacit knowledge** (hard to extract, you "just know"):
- Mint's game design intuition — knowing what feels fun without being able to articulate the rules
- Cooking — knowing what a dish needs by taste/smell/texture, not a recipe
- Driving — reading traffic flow, anticipating other drivers
- Child care — reading a child's needs from subtle cues

These are all cases where the knowledge resists codification. You can write a recipe, but the expert cook deviates from it based on something they can't fully explain. Polanyi's point: "we know more than we can tell."

**Extraction tensions around ownership and IP:**
- Capture the ability to do actions — extraction isn't just knowledge, it's capability transfer
- Protect proper nouns and full personal patterns — individual style, voice, and identity need guardrails
- Companies own interfaces and abstracted style/topics — the surface layer is protectable, but the underlying patterns get extracted anyway
- Make sure the designers are on the payroll, not just crawl their sites — extraction without compensation is the core labor issue. If you're training on someone's work, they should be employed, not scraped.

**Group discussion also surfaced:** Extraction via feedback and chat — users shaping the model through RLHF, thumbs up/down, and conversational corrections. A third extraction pathway that's neither training data nor RAG, but ongoing behavioral tuning from use.

The distinction matters: procedural knowledge in the weights is always available but hard to update or audit. Information retrieved via RAG is updatable and traceable but dependent on the retrieval pipeline working correctly.

![xkcd 1683: Digital Data](https://imgs.xkcd.com/comics/digital_data.png)
*[xkcd #1683: "Digital Data"](https://xkcd.com/1683/) — The promise of perfect digital retention vs the reality of lossy compression, re-uploading, and screenshotting. (CC BY-NC 2.5, Randall Munroe)*

**Trademark dilution** — A legal doctrine (Lanham Act § 1125(c)) where a trademark's distinctiveness or reputation is weakened, even without consumer confusion. Two forms: *blurring* (diluting uniqueness) and *tarnishment* (negative associations). Relevant to extraction: when AI reproduces stylistic or brand-associated patterns without attribution, it's a form of knowledge extraction that dilutes the original source's distinctiveness.

---

## Connections to Week 2 Theme

This maps directly to the Week 2 theme: extraction and workflow adaptation both sit on the individual-vs-system fault line. Wen's position aligns with the augmentation side of the spectrum (tools empower individuals), Harris's with the displacement side (systems reshape what individuals can do regardless of intent).
