# AWS Certified AI Practitioner (AIF-C01) — Study Set

A complete, self-built study package for the **AWS Certified AI Practitioner (AIF-C01)** exam
(foundational level). Every concept is presented in three layers — **what it is**, **why it works**
(causal mechanism), and **how it's applied** (a realistic scenario) — with the official domain code,
a difficulty tier, and a confidence tag throughout. High-stakes concepts add a **"Fails when"** line.
Depth and question counts are weighted to the official domain blueprint, heaviest domain first.

The material is built to teach the **decision logic the exam actually tests** — scenario stems with a
decisive constraint, the answer-elimination method, and the paired-distractor traps AWS relies on —
rather than flat definitions.

## Contents

| File | Description |
|---|---|
| `AIF-C01_Detailed_Notes.pdf` | 16-page detailed notes across all 5 domains, each concept in the What / Why / Applied (+ Fails-when) model, with "How AWS asks it" tips and exam-trap callouts |
| `AIF-C01_Architectural_Maps.html` | 9 causal-chain / decision diagrams: the AI-ML stack, service-selection tree, RAG data flow, security stack, responsible-AI control placement, inference routing, metric selection, prompt-technique selection, and a paired-distractor reference |
| `AIF-C01_Quiz_Set.pdf` | 30-question tiered quiz (incl. multiple-response), blueprint-weighted, with a full answer key that explains every correct answer and every distractor |
| `AIF-C01_Full_Practice_Exam.pdf` | 65-question, full-length, blueprint-weighted timed simulation with a quick-reference answer grid, detailed explanations, and exam-day framing |

## Domain weighting (matches the exam)

| Domain | Weight | Quiz (of 30) | Exam (of 65) |
|---|---|:--:|:--:|
| D3 — Applications of Foundation Models | 28% | 8 | 18 |
| D2 — Fundamentals of Generative AI | 24% | 7 | 16 |
| D1 — Fundamentals of AI and ML | 20% | 6 | 13 |
| D4 — Guidelines for Responsible AI | 14% | 5 | 9 |
| D5 — Security, Compliance & Governance | 14% | 4 | 9 |

D3 and D2 together are over half the exam — the package weights review accordingly.

## How to study (learn → visualize → test → simulate)

1. **Read the notes**, learning each concept's causal mechanism, not just its definition. Master the
   **managed→custom spectrum** first — most scenario questions resolve to "which tool on that spectrum?"
   then layer the right responsible-AI and security control.
2. **Walk the maps** to internalize service selection, RAG data flow, and where each control attaches.
3. **Take the quiz**, then read every explanation — including why the distractors are wrong.
4. **Sit the full 65-question exam** under time (~90 min), score against 700/1000 (~70%), and revisit
   the domains where you missed most.

## The elimination method (use on every question)

Read the **last sentence first** (the decisive constraint) → classify the task → eliminate
categorically-wrong options → break the tie on the constraint → check the paired-distractor traps
(RAG vs fine-tuning, Bedrock vs SageMaker, Guardrails vs Clarify, CloudTrail vs CloudWatch,
Inspector vs Macie, Kendra vs Bedrock KB, Autopilot vs Canvas, temperature vs top-p).

## Notes

- **Original study material** — no real exam items are reproduced.
- Not affiliated with, authorized, or endorsed by Amazon Web Services.
- Exam facts (verify against current AWS docs): 65 questions (50 scored + 15 unscored), ~90 minutes,
  700/1000 scaled to pass, Pearson VUE (center or online-proctored), valid 3 years.
