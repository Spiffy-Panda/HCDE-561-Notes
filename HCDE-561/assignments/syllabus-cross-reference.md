---
title: "Syllabus Cross-Reference"
---

# Syllabus Cross-Reference: Points of Attention

Cross-referencing the Version 0.7 course materials against past conversations and ongoing projects. Ordered from most actionable to least.

---

## 1. The Bioponic System IS a Use Case Project (Weeks 5-8)

The RAINPOINT bioponic monitor project hits all five capabilities simultaneously:

- **Extraction:** Codifying KNF/JADAM knowledge into an expert system
- **Workflow Adaptation:** The hybrid PLC + LLM architecture (deterministic expert system for routine sensing, Sonnet for automated monitoring, Opus for planning sessions)
- **Compliance/Safety:** Sensor drift, anaerobic crash detection, the interpretive gap between bioponic readings and actionable alerts
- **Model Operations:** The Sonnet-for-monitoring vs Opus-for-planning tiering is literally a model ops decision — cost, capability, latency tradeoffs baked into the architecture
- **Functional Replacement:** The system eventually substituting for human monitoring judgment; the secondary notification system for Mint reframes the human-in-the-loop question entirely

The syllabus explicitly says use cases should be "real, rich, buildable, and different." This project is all four. Strongly consider this as **Use Case 1**.

---

## 2. The BT Evolution Gym Is a Natural Use Case 2

The behavior tree AI gym covers different capability tensions than the bioponic system:

- **Extraction:** The LLM reading scouting reports to understand tacit fighting strategy — pattern recognition from replay logs that would otherwise require a human game designer's intuition
- **Functional Replacement:** LLM replacing a human game designer's balancing intuition through the Improve/Mutate/Crossbreed operations
- **Model Operations:** The ~12-14 LLM calls per season budget is a real cost/capability tradeoff; the prompt templates are themselves a model ops artifact

The adversarial stress-testing in **Week 7** maps perfectly onto the stagnation detection and wildcard injection mechanisms already designed into the gym.

---

## 3. The Anthropic-DoD Thread Is Directly Relevant to Week 3 (Compliance/Safety)

Already led this class discussion in HCDE 560. The 561 syllabus cites Perrow's Normal Accidents and Vaughan's normalization of deviance — the Anthropic-DoD case is a live example of both:

- Anthropic's progressive loosening of its AUP from 2023-2025 (broad prohibition to nuanced usage policy to Palantir partnership to Claude Gov to $1 government offer) is **textbook normalization of deviance**
- The Pentagon's subsequent designation of Anthropic as a supply chain risk after they maintained two narrow red lines illustrates **Perrow's point** that adding safety constraints to complex tightly-coupled systems creates new categories of failure

Worth referencing in a Week 3 artifact.

---

## 4. LLM-Modifying-Lower-Level-Logic Research Maps to Capabilities 4 and 5

The deep dive on LLMs as meta-controllers — the five-level taxonomy from one-shot generation to recursive self-modification — is exactly the kind of "moving target" the syllabus warns about in **Model Operations** (Capability 4). Key tensions:

- The safety/verification concerns (IEC 61508 Edition 3, EU AI Act implications) feed directly into **Week 3** material
- The Godel Agent and self-modifying system research raises the **Functional Replacement** question at its sharpest: when the LLM is modifying the control logic that governs physical systems, "who is accountable when things go wrong?" becomes non-trivial
- The bioponic system itself uses this pattern (LLM modifying expert system rules), so this research is also background for Use Case 1

---

## 5. Hutchins' Distributed Cognition (Week 4) Connects to the Autonome System

The Autonome utility AI framework — authority DAGs, data-driven aggregation, unified entity concept, Bezier response curves — is essentially a formalization of distributed cognition for NPCs. The irreversibility point Hutchins makes (you can't reconstruct distributed cognitive systems by rehiring) has a design corollary: if your Autonome agents develop emergent coordination patterns through the authority DAG, removing or replacing one agent doesn't just lose that agent — it loses the relational structure.

---

## 6. Accessibility Is Underserved by This Syllabus

The YouTube epilepsy detection gap, subvocalization-to-text research, and software-enabled accessibility as a vital AI application — none of this appears in the five-capability framework or the reading list. The syllabus has a **blind spot around disability and accessibility as a strategic AI concern**.

Specific gaps:

- No reading on AI accessibility applications or disability justice perspectives
- The five capabilities don't explicitly address who is *excluded* by AI adoption, only who is displaced or extracted from
- Functional replacement discussions focus on job loss but not on the inverse: AI *creating* capability for people who previously lacked access

This could be strong feedback to surface in **Week 9's framework reflection**.

---

## 7. Polanyi's Tacit Knowledge (Week 2) Is the Theoretical Backbone of the Bioponic System's Hardest Problem

The bioponic system's "composting/bioreactor consultant" role is an attempt to use AI extraction to bridge a tacit knowledge gap. Polanyi would say this is the exact case where extraction fails — the knowledge resists codification.

This also connects to the Week 2 Matt Beane TED talk on "shadow learning" — essentially trying to apprentice to an AI that learned from other people's expertise, which is the exact pipeline disruption Beane documents in surgery.
