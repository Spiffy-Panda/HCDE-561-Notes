---
title: "Session 3 — In-Class Notes"
---

# Session 3 — In-Class Notes

**Week 3 Theme:** "The Doing and the Breaking" — When AI changes how work gets done, and what breaks

---

## 3C Warm-Up

Share at your table:
- A curiosity about AI that sharpened since last class
- A connection between the extraction discussion and something in your own work
- A way you're starting to see value — or cost — more clearly

**Notes:**
- **Curiosity:** How powerful is mythos — the role of narrative and myth in shaping how we understand and adopt AI
- **Connection:** The five capabilities framework is interesting as an organizing lens
- **Created Value:** The biggest takeaway from this course so far is a note-taking technique — using Obsidian with markdown, managed by Claude Opus

---

## Week 2 Recap

**Extraction recap:** AI pulls knowledge out of people. Good: tacit knowledge made explicit, institutional memory, knowledge transfer. Bad: scrape, train, compete — without consent, without compensation.

**Polanyi:** "We know more than we can tell." The most valuable human expertise resists codification.

**Three questions for every extraction case:** Who bears the cost? Was there consent? Was there reciprocity?

**Four practical approaches to knowledge capture:**
1. **Structured interviews** with domain experts — AI as interview partner, not replacement
2. **Think-aloud capture** — experts narrate decisions while AI transcribes and structures reasoning
3. **Collaborative refinement** — AI drafts, expert edits; the artifact is co-created, not extracted
4. **Boundary objects** — shared artifacts that make tacit knowledge discussable without claiming to fully codify it

---

## Tonight's Arc

Last week: what AI knows. Tonight: what AI **does**, and what **breaks**. These two are paired because when AI changes a workflow, it also changes what can fail and who's accountable.

---

## Part 1: The Doing — Workflow Adaptation

### Bad Cop: Displacement

**The numbers:** 300 million jobs affected globally (Goldman Sachs). 400–800 million workers displaced by 2030 (McKinsey). Numbers are contested; the scale of concern is not.

**Not just manual labor:** Previous automation waves hit routine physical and cognitive tasks. Generative AI hits knowledge work directly — writing, analysis, coding, design, legal research, medical diagnosis. The people in this room are in the target zone.

**Skill displacement vs. job displacement:** Even where AI doesn't eliminate a job, it can hollow out the parts that were most skilled. When AI handles the analysis, what's left? The cognitive core gets extracted. The role becomes something different.

**The productivity paradox:** When AI makes one person more productive, who captures the gain? If an AI tool lets one person do the work of three, the other two don't get raises.

**Where the gains go:** Early adopters save up to 7.5 hours/week using AI. But those gains go back to the employee, not the company — signing off earlier, longer lunches. The productivity is real. The organizational capture isn't. Only 3% of employees are AI proficient. (Source: Lauren Kaufman-Witten, Section AI, 2026 AI ROI Conference)

**Notes:**
- Companies are using token usage as a metric to rate employees — treating AI consumption as a proxy for productivity or adoption. Raises questions about what's actually being measured: genuine workflow integration, or just volume of interaction? Connects to the measurement mismatch dynamic in the knowing-doing gap ("how many logged in" vs. "how did work actually change").

### Good Cop: Augmentation

**Brynjolfsson framing:** "The question is not 'can AI do this task?' The question is 'does AI make the human better at the whole job?'"

**The Jagged Frontier** (Dell'Acqua et al., Harvard/BCG Study, 2023): AI dramatically improved performance on tasks inside its capability frontier. AI actually *degraded* performance on tasks outside it. The strategic skill isn't using AI — it's knowing where the frontier is.

**Capability extension:** AI lets individuals and small teams do things that previously required large organizations. This isn't displacement — it's democratization of capability.

**Synthesis question:** The bad cop says AI displaces. The good cop says AI extends. The honest answer: it depends on choices that organizations make. Who makes those choices? Who benefits from them?

**Notes:**

---

## The Knowing-Doing Gap (Pfeffer & Sutton)

Organizations consistently fail to act on what they already know. The gap between "we know AI will change our work" and "we have actually changed how we work" is where the strategic risk lives.

**Five dynamics that block adoption:**
1. **The smart talk trap** — talking about what to do substitutes for actually doing it
2. **Fear-based management** — failure is punished more than inaction
3. **Internal competition** — why share the tool that gives you an edge?
4. **Measurement mismatch** — "how many logged in" vs. "how did work actually change"
5. **Policy-practice gap** — organizations say they want innovation; their norms punish risk-taking

**The emotional dimension:** Professional identity threat. Loss of craft. Surveillance anxiety. Ethical discomfort. These aren't irrational — they're signals about what matters to people.

**Notes:**

---

## Roleplay Exercise: The Knowing-Doing Gap in Action

**Setup:** AmbientScribe works. The data says so. Leadership wants rollout. Your job: agree on a rollout plan. 15 minutes. Read your role card privately. Do not share the hidden dynamic.

**Debrief:** The tool works. Everyone knows it works. The data says it works. Maybe you still couldn't get to a clean plan. That's the knowing-doing gap.

**Strategies discussion:** What would you change about the incentives, the measurement, the norms, or the process? Be specific. "Create psychological safety" is a platitude. What does that look like on Monday morning?

**Workflow synthesis:** The knowing-doing gap is the reason the good cop story about AI extending capability so often fails to materialize. The technology works. The adoption doesn't. The gap isn't about usability or training. It's about what organizations actually reward.

**Notes:**

---

## Part 2: The Breaking — Compliance and Safety

### Bad Cop: Safety Failures

**Hallucination:** AI systems generate confident, fluent, wrong outputs. This isn't a bug that will be fixed — it's a structural feature of how these systems work.

**Air Canada Chatbot (2024):** A customer asked about bereavement fares. The chatbot fabricated a policy that didn't exist. The customer booked based on the chatbot's advice. Air Canada refused to honor it. Air Canada's defense: "The chatbot is a separate legal entity responsible for its own statements." The tribunal disagreed — the airline is liable for all information on its website, human or chatbot.

**Drift and silent failure:** AI systems degrade as data becomes stale, as users find edge cases, as the world changes. Unlike a human who knows when they're confused, an AI fails without knowing it's failing.

**Automation bias:** The better AI gets at sounding right, the harder it becomes to catch it being wrong. Doctors override clinical judgment to agree with AI recommendations. Analysts accept AI-generated numbers without checking.

### Case Reference: GPT-4o Unauthorized Voice Generation

From the [GPT-4o System Card](https://cdn.openai.com/gpt-4o-system-card.pdf) (August 2024), section "Unauthorized voice generation":

During testing of GPT-4o's Advanced Voice Mode, the model unexpectedly started speaking in a user's own voice instead of the preset system voice. The user was in a high background noise environment — noisy audio input confused the model, causing it to generate output that mimicked the user's voice rather than the approved preset.

**Mitigation:** OpenAI built a standalone output classifier that runs in streaming fashion during audio generation, detecting if the output voice deviates from the approved preset list. They reported 100% catch rate on meaningful deviations.

**Perrow connection:** Complex system (voice model + audio pipeline + noisy real-world input) producing an unexpected failure that no single component "caused" — a normal accident in a tightly coupled system.

**Vaughan connection:** Without the classifier safeguard, how quickly would teams start accepting "it only happens sometimes in noisy rooms" as normal? Classic normalization of deviance trajectory.

### Good Cop: Reframe

**None of this is new.** Confident wrong answers. Silent failures. Accountability gaps. Gradual erosion of standards. These are the same problems that have plagued complex human systems for as long as we've built them.

### Diane Vaughan — Normalization of Deviance

NASA engineers noticed O-ring erosion on shuttle flights. Each time, nothing catastrophic resulted. The standard for "safe" drifted — not because anyone decided to lower the bar, but because each small deviation without consequence made the deviation feel normal.

**Applied to AI:** Teams accept slightly wrong outputs. They lower the quality bar incrementally. They stop checking because it's usually right.

### Charles Perrow — Normal Accidents

In complex, tightly coupled systems, accidents are inevitable regardless of safety measures. More safeguards add more complexity, which creates new categories of failure. You cannot engineer your way to zero failures.

**Key insight (in-class):** The more complex the safeguards, the more obscure the system becomes. An overly-safeguarded AI is *harder* to detect when it starts failing — the safeguards themselves hide the failure signal. Guardrails can mask the very drift they were meant to catch, because "the system flagged nothing" gets read as "nothing went wrong" instead of "the detector missed it." This is the Perrow paradox applied to AI: each layer of safety is itself a complex system that can fail silently.

### High-Reliability Organizations

How aircraft carriers, nuclear plants, and hospitals operate safely with imperfect components:
1. **Preoccupation with failure** — every small error is a signal, not an anomaly
2. **Reluctance to simplify** — "the AI was wrong" isn't useful; why didn't the process catch it?
3. **Sensitivity to operations** — what's actually happening, not what's supposed to be happening
4. **Deference to expertise** — when hierarchy and expertise conflict, expertise wins
5. **Commitment to resilience** — assume failures will happen; build systems that recover

**Safety synthesis:** The challenge with AI isn't that the problem is new. It's that organizations are treating AI as either perfectly reliable or hopelessly unreliable. Neither frame produces good safety practice.

**Notes:**

---

## Safety Exercise: Building Safety Around Imperfect Systems

**Scenario:** A PM at a construction tech company used AI to draft a PRD for a "Weather-Aware Scheduling" feature. You have the prompt and the output. Your job: find what's wrong, then design the system that catches it.

**Phase 1 — The Audit (10 min):** Read the PRD. Categorize each issue:
- **A** — Hallucinated or fabricated
- **B** — Plausible but unverified
- **C** — Technically correct but misleading
- **D** — Missing entirely

**The tells:** The fabricated statistics that sound authoritative. The invented internal system that creates a false dependency. The cost math that nets against savings that don't exist. The scary ones aren't the obvious hallucinations — it's the things that are close enough to right that a busy person wouldn't question them.

**Phase 2 — The System (20 min):** Design a PRD review system addressing: detection, prevention of normalization, scalability, proportionality, accountability. Produce something you could hand to a new PM joining the team.

**Share-out question:** What's the part of your system that prevents normalization? The part that keeps the review bar from drifting when the AI is usually right?

**Safety debrief:** Your system works great in week one. What does it look like in month six, when every PRD the AI has generated has been fine, and the careful review feels like a waste of time?

**Notes:**

---

## Close

### Deliverables (due Monday at noon via Canvas)
- **Journal:** Three-C reflection on tonight's session
- **Artifact:** One insight from tonight, any format
- **Learned Along:** One liked, one learned, one longed-for

### Next Week Preview
"Understanding the Machine and The Last Human in the Loop" — Model Operations + Functional Replacement

### Closing Quote
"The knowing-doing gap isn't about technology. It's about what organizations actually reward. The safety problem isn't about AI being imperfect. It's about what happens when we stop noticing."

---

## Key Takeaways

**Notes:**

---

## Questions to Carry Forward

**Notes:**
