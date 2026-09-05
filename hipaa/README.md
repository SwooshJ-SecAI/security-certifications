# HIPAA

Study and reference notes on HIPAA — the U.S. law governing the protection of health information. For a security engineer, the relevant parts are the Security Rule, the Privacy Rule, and the Breach Notification Rule.

---

## Scope: Who and What

HIPAA applies to **covered entities** (health plans, healthcare clearinghouses, and providers who transmit health data electronically) and their **business associates** (vendors that handle protected health information on their behalf). A business associate is bound through a Business Associate Agreement (BAA) — the contract that extends HIPAA obligations down the supply chain.

The protected asset is **PHI** (Protected Health Information) — individually identifiable health information. In electronic form it is **ePHI**, which is what the Security Rule specifically governs.

---

## The Security Rule

The Security Rule protects ePHI through three categories of safeguards. The structure is deliberate: technology alone is insufficient, so the rule mandates people and process controls alongside technical ones.

### Administrative Safeguards (the largest category)

The policies and processes that govern security. These exist because most breaches trace to human and process failures, not technical ones.

- Security management process (risk analysis and risk management)
- Assigned security responsibility (a named security official)
- Workforce security and information access management (least privilege)
- Security awareness and training
- Contingency planning (data backup, disaster recovery, emergency mode)
- Periodic evaluation

### Physical Safeguards

Protection of the physical systems and facilities holding ePHI.

- Facility access controls
- Workstation use and security
- Device and media controls (disposal, reuse, accountability, backup)

### Technical Safeguards

The technology controls applied to ePHI itself.

- Access control (unique user identification, emergency access, automatic logoff, encryption)
- Audit controls (logging of activity on systems with ePHI)
- Integrity controls (protect ePHI from improper alteration or destruction)
- Transmission security (protect ePHI moving over networks)

### Required vs Addressable

A defining nuance: each safeguard is either **required** (must implement) or **addressable**. Addressable does not mean optional — it means the entity must implement it, or document why it is not reasonable and implement an equivalent alternative. Skipping an addressable control without justification is a violation.

---

## The Privacy Rule

Where the Security Rule governs ePHI specifically, the Privacy Rule governs all PHI in any form and sets the rules for use and disclosure.

- **Minimum necessary** — use or disclose only the least PHI needed for the purpose. The direct analog of least privilege, applied to information sharing.
- **Permitted uses** — treatment, payment, and healthcare operations do not require separate authorization; most other uses do.
- **Individual rights** — patients may access their records, request amendments, and receive an accounting of disclosures.

---

## The Breach Notification Rule

When unsecured PHI is compromised, notification is mandatory and time-bound:

- **Individuals** — notified without unreasonable delay, no later than 60 days from discovery.
- **HHS** — notified; breaches affecting 500 or more individuals are reported without delay, smaller breaches annually.
- **Media** — for breaches affecting 500 or more residents of a state or jurisdiction.

Critically, encryption is a safe harbor: properly encrypted PHI that is lost or stolen is generally not considered a reportable breach, because the data remains unreadable. This is the direct operational incentive to encrypt ePHI everywhere.

---

## The Mental Model for Study

HIPAA is best understood as risk analysis made mandatory. The Security Rule does not dictate specific technologies — it requires the entity to assess its own risks to ePHI and implement reasonable safeguards across administrative, physical, and technical dimensions. Study it by mapping each safeguard to the failure it prevents, and remember that "addressable" is a documentation obligation, not permission to skip.
