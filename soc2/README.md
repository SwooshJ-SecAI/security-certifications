# SOC 2

Study and reference notes on SOC 2 — the audit framework that evaluates how a service organization protects customer data. SOC 2 is defined by the AICPA and is the de facto trust standard for SaaS and cloud service providers.

---

## What SOC 2 Actually Is

SOC 2 is not a checklist of technical controls handed to you. It is a framework for demonstrating, through independent audit, that an organization's controls meet defined criteria over time. The organization chooses its own controls; the audit tests whether those controls exist and operate as claimed. This is why two SOC 2 reports can look very different — the criteria are shared, but the control implementations are not.

---

## The Five Trust Services Criteria

Every SOC 2 engagement covers **Security** at minimum. The other four are included only if relevant to the services offered.

| Criterion | Question it answers | Included |
|:---|:---|:---|
| **Security** (Common Criteria) | Is the system protected against unauthorized access? | Always (mandatory) |
| **Availability** | Is the system available for operation as committed? | If uptime is a commitment |
| **Processing Integrity** | Is processing complete, valid, accurate, timely, authorized? | If data processing accuracy matters |
| **Confidentiality** | Is information designated confidential protected? | If handling confidential data |
| **Privacy** | Is personal information handled per the privacy notice? | If handling personal information |

Security is mandatory because it is foundational — the other four are meaningless if the system can be breached. Security is also called the **Common Criteria (CC)** and maps closely to the COSO internal control framework.

---

## Type I vs Type II

This distinction is the single most important SOC 2 concept.

- **Type I** — evaluates whether controls are *suitably designed* at a single point in time. It answers "do the right controls exist on this date?" It is a snapshot.
- **Type II** — evaluates whether controls are *designed and operating effectively* over a period (typically 3 to 12 months). It answers "did the controls actually work, consistently, over time?"

Type II is far more valuable and far more demanding. Design without operation is theater — a control that exists on paper but is not followed provides no assurance. Type II requires evidence that the control ran every time it was supposed to across the whole period, which is why it demands continuous logging and consistent process.

---

## Common Control Areas and Evidence

Controls cluster into recognizable categories. For each, the audit expects evidence that the control operated throughout the review period, not just that it exists.

| Control Area | Example Controls | Evidence Collected |
|:---|:---|:---|
| Access control | MFA, least privilege, access reviews | Access logs, review records, provisioning tickets |
| Change management | Peer review, testing, approval before deploy | Pull requests, change tickets, deployment logs |
| Risk assessment | Annual risk assessment, treatment plans | Risk register, assessment reports |
| Vendor management | Third-party reviews, right-to-audit | Vendor assessments, contracts |
| Incident response | Documented IR plan, post-incident review | IR tickets, tabletop exercise records |
| Monitoring | Logging, alerting, log review | SIEM exports, alert records, review sign-offs |
| Onboarding/offboarding | Timely provisioning and deprovisioning | HR tickets tied to access changes |

---

## The Mental Model for Study

SOC 2 is fundamentally about the relationship between a **control** and its **evidence**. A control is a claim ("we require MFA"); evidence is the proof the claim held over time (the MFA configuration plus authentication logs across the period). Study SOC 2 by asking, for any control: what artifact would an auditor need to see to believe this operated every day for the past year? If no such artifact exists, the control is not auditable — and an unauditable control is a gap.
