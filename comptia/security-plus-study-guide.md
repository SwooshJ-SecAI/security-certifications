# Security+ SY0-701 Study Guide

Condensed, high-yield notes organized by exam domain. Each concept is built from its underlying logic: what problem it solves and why it exists, then how it works.

---

## Domain 1 — General Security Concepts (12%)

### The CIA Triad

Every security control ultimately serves one of three goals. This is the root from which everything else grows.

- **Confidentiality** — information is disclosed only to those authorized. Defeated by eavesdropping, theft, weak access control. Enforced by encryption and access control.
- **Integrity** — information is accurate and unaltered except by authorized action. Defeated by tampering, corruption. Enforced by hashing, digital signatures, checksums.
- **Availability** — information and systems are usable when needed. Defeated by denial-of-service, hardware failure, disaster. Enforced by redundancy, backups, capacity planning.

A useful test: for any control, ask which leg of the triad it protects. If it protects none, question why it exists. A common fourth addition is **non-repudiation** — proof that an actor cannot deny an action, achieved through digital signatures and logging.

### Control Types (by function)

Controls are classified by what they do relative to an incident in time:

- **Preventive** — stop an incident before it happens (firewall, access control, encryption).
- **Detective** — identify an incident in progress or after (IDS, log monitoring, cameras).
- **Corrective** — restore after an incident (backups, patching, incident response).
- **Deterrent** — discourage an attempt (warning banners, visible cameras).
- **Compensating** — an alternate control when the primary is not feasible.
- **Directive** — mandate behavior (policies, procedures).

Controls are also classified by **category**: technical (implemented in technology), managerial (policy and process), operational (executed by people), and physical (locks, guards, fences).

### Zero Trust

The mental shift: never trust based on network location. The old model trusted anything inside the perimeter; zero trust assumes breach and verifies every request. Core ideas: verify explicitly, use least-privilege access, and assume the network is hostile. Implemented through a **policy engine** (decides) and **policy enforcement point** (acts), separating the control plane (decisions) from the data plane (traffic).

---

## Domain 2 — Threats, Vulnerabilities, and Mitigations (22%)

### Threat Actors

Understand actors by their **motivation** and **capability**, because those predict behavior:

- **Nation-state** — high capability, high resources, patient. Motivated by espionage, disruption. Advanced Persistent Threat (APT).
- **Organized crime** — financially motivated, professional, ransomware and fraud.
- **Hacktivist** — ideologically motivated, often defacement or leaks.
- **Insider threat** — legitimate access misused; hardest to detect because access is authorized.
- **Unskilled attacker** — uses existing tools; low capability but high volume.

### Common Attack Types

- **Phishing / social engineering** — attacks the human, not the machine. The most common initial access vector because it bypasses technical controls entirely.
- **Malware families** — virus (needs a host and user action), worm (self-propagating), ransomware (encrypts for extortion), trojan (disguised), rootkit (hides at a privileged level), logic bomb (triggers on condition).
- **Injection** — untrusted input treated as code (SQL injection, cross-site scripting). Root cause is failure to separate data from instructions.
- **On-path (formerly man-in-the-middle)** — attacker intercepts communication between two parties.

### Vulnerability Management

The cycle: identify (scanning), analyze (is it real, is it exploitable, what is the risk), prioritize (CVSS score plus business context), remediate (patch, mitigate, or accept), and validate (rescan). CVSS gives a severity number, but prioritization requires pairing it with exposure and asset value — a critical CVE on an isolated test box may matter less than a medium on an internet-facing system.

---

## Domain 3 — Security Architecture (18%)

### Network Segmentation

The logic: limit the blast radius. If everything is flat, one compromised host reaches everything. Segmentation places boundaries so a breach is contained. Techniques include VLANs, subnets, and a **screened subnet (DMZ)** for public-facing services so they never sit alongside internal systems.

### Secure Design Principles

- **Defense in depth** — layered controls, so no single failure is catastrophic.
- **Least privilege** — grant the minimum access required for a role. Limits both accident and abuse.
- **Fail secure vs fail open** — decide, per control, whether a failure should deny or allow. A door lock might fail open for life safety; a firewall should fail secure.

### Data Protection

Know the three states and the control appropriate to each:

- **At rest** — stored data. Protected by disk and database encryption.
- **In transit** — moving over a network. Protected by TLS.
- **In use** — actively processed in memory. Hardest to protect; addressed by techniques such as confidential computing.

Supporting concepts: **tokenization** (replace sensitive data with a non-sensitive token), **masking** (hide portions of data), and **data classification** (label by sensitivity so controls can be applied proportionally).

---

## Domain 4 — Security Operations (28%)

### Identity and Access Management (IAM)

The largest operational surface. Built from four ideas in sequence:

1. **Identification** — claiming an identity (username).
2. **Authentication** — proving it. Factors: something you know (password), something you have (token), something you are (biometric). **Multifactor authentication (MFA)** combines factors from different categories, which is why two passwords is not MFA.
3. **Authorization** — what the proven identity may do. Models: role-based (RBAC, by job function), attribute-based (ABAC, by attributes/context), mandatory (MAC, by classification labels), discretionary (DAC, owner decides).
4. **Accounting** — logging what was done, enabling non-repudiation and audit.

Federation and single sign-on (SSO) extend identity across systems using standards such as SAML and OpenID Connect.

### Cryptography Applied

- **Symmetric** — one shared key, fast, used for bulk data (AES). Problem: key distribution.
- **Asymmetric** — public/private key pair, solves key distribution, slower (RSA, ECC). Used to exchange symmetric keys and to sign.
- **Hashing** — one-way function producing a fixed digest (SHA-2). Verifies integrity; not reversible. Passwords are hashed with a **salt** (random per-value) to defeat precomputed-table attacks.
- **Digital signature** — hash the message, encrypt the hash with the sender's private key. Proves integrity and authenticity, and provides non-repudiation.
- **PKI** — the trust framework binding public keys to identities through certificate authorities.

### Monitoring and Response

- **SIEM** — aggregates and correlates logs across sources to surface incidents.
- **Incident response lifecycle** — preparation, identification, containment, eradication, recovery, lessons learned. The order matters: contain before eradicating, or the threat spreads while you clean.

---

## Domain 5 — Security Program Management and Oversight (20%)

### Risk Management

Risk is not eliminated; it is managed. The vocabulary:

- **Risk** = likelihood x impact. Both must be considered; a high-impact, near-impossible event may rank below a moderate, frequent one.
- **Risk responses** — accept (tolerate it), avoid (stop the activity), transfer (insurance, outsourcing), mitigate (reduce likelihood or impact with controls).
- **Quantitative vs qualitative** — quantitative assigns dollar values (SLE, ARO, ALE); qualitative uses relative ratings (high/medium/low) when precise numbers are unavailable.

Key quantitative formulas: **SLE** (single loss expectancy) = asset value x exposure factor. **ALE** (annualized loss expectancy) = SLE x **ARO** (annualized rate of occurrence). ALE justifies control spending — a control is worth deploying if it costs less than the ALE it removes.

### Governance and Compliance

- **Policies, standards, procedures, guidelines** — a hierarchy from high-level intent (policy) to mandatory specifics (standard) to step-by-step instructions (procedure) to optional advice (guideline).
- **Third-party risk** — vendors extend the attack surface; managed through assessments, right-to-audit clauses, and service-level agreements.
- **Frameworks** — structured control sets (NIST CSF, ISO 27001) that provide a common language and a checklist for coverage.

---

## Quick-Reference Anchors

- Every control maps to confidentiality, integrity, or availability.
- Every threat should be studied alongside its mitigation.
- MFA requires factors from different categories, not repeated factors.
- Symmetric for speed, asymmetric for key exchange and signing, hashing for integrity.
- Risk = likelihood x impact; ALE justifies spend.
- Contain before you eradicate.
