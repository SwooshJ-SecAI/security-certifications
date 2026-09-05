# ISO/IEC 27001:2022

Study and reference notes on ISO/IEC 27001:2022 — the international standard for an Information Security Management System (ISMS). Where SOC 2 is an audit report, ISO 27001 is a certifiable management system: it defines the repeatable process by which an organization governs security.

---

## The Core Idea: It Is a System, Not a Control List

The most common misunderstanding is treating ISO 27001 as a list of controls to implement. The controls (Annex A) are the smaller part. The heart of the standard is the **ISMS** — the management process in clauses 4 through 10 that makes security a governed, continually improving discipline rather than a one-time project.

The ISMS runs on the Plan-Do-Check-Act cycle:

- **Plan** — establish context, scope, risk assessment, and a risk treatment plan.
- **Do** — implement the selected controls and operate them.
- **Check** — monitor, measure, audit internally, and review with management.
- **Act** — correct nonconformities and improve.

Certification tests whether this cycle genuinely turns, not whether a specific control is present.

---

## Mandatory Clauses (4–10)

These are the non-optional management requirements — the parts that make it an ISMS:

| Clause | Focus |
|:--|:---|
| 4 — Context | Define internal/external issues, interested parties, and ISMS scope |
| 5 — Leadership | Top-management commitment, security policy, roles and responsibilities |
| 6 — Planning | Risk assessment, risk treatment, security objectives |
| 7 — Support | Resources, competence, awareness, documented information |
| 8 — Operation | Execute risk treatment and operate controls |
| 9 — Performance evaluation | Monitoring, internal audit, management review |
| 10 — Improvement | Nonconformity, corrective action, continual improvement |

---

## Annex A Controls (2022 Structure)

The 2022 revision reorganized the controls from 114 across 14 domains into **93 controls across 4 themes**. The consolidation reflects how controls actually group in practice:

| Theme | Controls | What it covers |
|:---|:--:|:---|
| **Organizational** | 37 | Policies, roles, supplier relationships, threat intelligence, cloud service use |
| **People** | 8 | Screening, awareness, responsibilities, remote working |
| **Physical** | 14 | Secure areas, equipment, media handling, environmental protection |
| **Technological** | 34 | Access control, cryptography, logging, secure development, data protection |

The 2022 version also introduced 11 new controls addressing modern needs — including threat intelligence, information security for cloud services, data leakage prevention, and secure coding — reflecting how the threat landscape shifted since the prior revision.

---

## Statement of Applicability (SoA)

The SoA is the pivotal document. It lists every Annex A control and, for each, states whether it is applied, and if not, why it is excluded. This forces a deliberate decision on every control rather than silent omission. An auditor reads the SoA to understand what the organization claims to do; the audit then tests whether reality matches the SoA.

---

## The Certification Process

1. **Stage 1 audit** — documentation review. Does the ISMS exist on paper? Are scope, policy, risk assessment, and SoA in place?
2. **Stage 2 audit** — implementation review. Does the ISMS operate as documented? Evidence of controls running, internal audits performed, management reviews held.
3. **Surveillance audits** — annual checks that the ISMS continues to operate.
4. **Recertification** — full reassessment every three years.

---

## The Mental Model for Study

ISO 27001 rewards thinking in terms of process maturity, not control presence. For any requirement, ask: is this a one-time artifact or a recurring activity? The standard's power is that it demands recurrence — risk assessments repeat, audits repeat, reviews repeat. A control implemented once and never revisited fails the standard even if it technically exists, because the ISMS is defined by the turning of the improvement cycle.
