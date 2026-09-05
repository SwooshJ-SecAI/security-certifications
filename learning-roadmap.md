# Certification Learning Roadmap

A phased study plan that sequences credentials by dependency: foundations first, then specialization, then governance and architecture. Each phase builds on the vocabulary and mental models established in the phase before it.

---

## Phase 1 — Foundations (Complete)

**CompTIA Security+ (SY0-701)**

The baseline. Security+ establishes the shared vocabulary every later certification assumes: the CIA triad, cryptographic primitives, access control models, network defense, and risk management. Everything downstream reuses these terms. Completing this first means later material can be read at the level of "how does this apply" rather than "what does this word mean."

Outcome: credential earned. Notes in [comptia/](./comptia/).

---

## Phase 2 — Specialization (In Progress)

**CompTIA SecAI+ (CY0-001)** and **AWS Certified AI Practitioner (AIF-C01)**

These run in parallel because they reinforce each other. SecAI+ covers the security side of AI — adversarial machine learning, model supply-chain risk, data poisoning, prompt injection, and governance of AI systems. AIF-C01 covers the foundational mechanics of AI/ML on a cloud platform — model types, training, inference, responsible AI practices, and the managed services that host them.

Studied together, they close the loop: one explains how AI systems work and are operated, the other explains how they fail and are attacked. A security engineer building AI tooling needs both halves.

Sequencing: AIF-C01 first (or slightly ahead) to establish the mechanics, then SecAI+ layers the threat model on top.

---

## Phase 3 — Governance and Audit (Planned)

**ISO 27001 Lead Auditor**

A shift from technical controls to systems of governance. ISO 27001 is about the Information Security Management System (ISMS) — the repeatable process by which an organization identifies risk, selects controls, and demonstrates ongoing management. The Lead Auditor track adds the discipline of evaluating whether an ISMS actually functions as documented.

This phase pairs naturally with practical SOC 2 and HIPAA reference work (see [soc2/](./soc2/) and [hipaa/](./hipaa/)), since all three are exercises in mapping controls to evidence and proving operation over time.

---

## Phase 4 — Architecture and Management (Planned)

**CISSP**

The capstone. CISSP spans eight domains and expects the candidate to think like a security architect and manager, not only a practitioner. It assumes fluency in everything from the earlier phases and adds breadth: security architecture, software development security, and the management judgment to balance risk against business need.

Sequenced last because it rewards accumulated context. Attempting it before the foundational and specialization phases means memorizing what should already be understood.

---

## Guiding Principle

The roadmap is deliberately dependency-ordered rather than difficulty-ordered. Each credential is attempted when its prerequisites are internalized, so study time is spent building on understanding instead of backfilling gaps. The goal is durable knowledge that transfers to real engineering work, with the certification as the checkpoint rather than the objective.
