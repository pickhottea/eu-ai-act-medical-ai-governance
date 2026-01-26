# P1 — Roles & Responsibilities (Provider vs Operator)

## Purpose
Clarify accountability and responsibility allocation
for a **high-risk AI system** under the **EU AI Act**,
ensuring that obligations related to oversight, documentation,
and corrective actions are clearly assigned and auditable.

This policy establishes **who is responsible for what**
across the AI system lifecycle and prevents ambiguity
between system provision and operational use.

---

## Scope
This policy applies to:
- AI systems classified as **High-Risk AI** under the EU AI Act (Art. 6, Annex III)
- Medical AI systems used for **clinical decision support**
- EU-only deployment contexts

---

## Roles

### Provider  
**MediFuture GmbH**

The Provider is the legal entity responsible for placing
the AI system on the market or putting it into service.

**Core responsibilities include:**
- System design and overall architecture
- Model development, validation, and versioning
- Definition of **intended purpose**, limitations, and risk boundaries
- Establishment of the governance framework and policies
- Preparation and maintenance of technical documentation
- Support for auditability, traceability, and explainability
- Communication with regulatory authorities when required

The Provider **does not perform clinical decisions**
and does not replace human judgment in medical contexts.

---

### Operator  
**Clinical institutions / hospitals**

The Operator is the organization that deploys and uses
the AI system in a real-world clinical environment.

**Core responsibilities include:**
- Decision to deploy or discontinue system use
- Integration into clinical workflows
- Ensuring **human oversight** during operation
- Review and override of AI outputs where appropriate
- Monitoring operational behavior and anomalies
- Incident reporting, escalation, and cooperation in investigations
- Compliance with local clinical and organizational requirements

The Operator retains **final responsibility for clinical decisions**.

---

## Responsibility Split (RACI-style)

| Activity | Provider | Operator |
|--------|----------|----------|
| Model development & training | R | I |
| Model validation & versioning | R | I |
| Intended purpose definition | R | I |
| System documentation | R | I |
| Deployment decision | C | R |
| Clinical workflow integration | I | R |
| Human review & override | I | R |
| Incident detection & reporting | C | R |
| Corrective action design | R | C |
| Corrective action execution | C | R |
| Regulatory communication | C | R |

*R = Responsible, C = Consulted, I = Informed*

---

## Governance Principles

1. **No Autonomous Clinical Decisions**  
   The AI system provides decision support only.
   Final clinical decisions always remain with qualified professionals.

2. **Human Oversight Is Mandatory**  
   Oversight mechanisms must be operationally enforceable,
   not symbolic or optional.

3. **Governance Before Model Changes**  
   Corrective measures begin with governance review.
   Model changes require explicit governance approval
   and documented justification.

4. **Separation of Concerns**  
   Technical responsibility (Provider) and clinical responsibility (Operator)
   must remain clearly separated to avoid accountability gaps.

---

## Evidence & Documentation Links
This policy is supported by:
- Technical documentation index (P3)
- Human oversight and review triggers (P4)
- Audit logs and traceability artefacts (D-series)
- Incident handling and escalation records

---

## Review & Maintenance
- **Review frequency:** At least annually, or upon major system changes
- **Trigger events:** Regulatory updates, significant incidents,
  changes in intended use, or material model updates
- **Approval authority:** Governance lead / compliance function

---

## Relationship to EU AI Act
This policy supports compliance with:
- **Art. 6** — High-Risk AI classification
- **Art. 12** — Record-keeping and auditability
- **Art. 13** — Transparency obligations
- **Art. 14** — Human oversight requirements

---

*This document is part of the governance framework
for an EU AI Act–oriented medical AI demonstration
and does not constitute legal advice.*
