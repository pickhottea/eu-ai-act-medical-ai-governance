# P5 — Change Control & Release Governance

## Purpose
Define governance-controlled processes for managing changes
to high-risk medical AI systems, ensuring that modifications
are **intentional, reviewed, documented, and auditable**.

This policy prevents uncontrolled model or system changes
that could undermine safety, accountability, or regulatory compliance.

---

## Scope
Applies to:
- Model updates, retraining, and recalibration
- Data pipeline or feature changes affecting model behavior
- Explainability method changes
- Threshold, policy, or governance parameter changes
- Deployment or operational configuration changes

---

## Core Principle
**Governance precedes model change.**

No model or system modification may be executed
without prior governance review and approval.

---

## Change Classification

### Minor Changes
Examples include:
- Documentation updates
- Visualization or reporting adjustments
- Non-functional code refactoring
- Policy text clarifications

Minor changes require:
- Documentation update
- Version annotation
- No revalidation of model behavior

---

### Material Changes
Examples include:
- Model retraining or recalibration
- Feature engineering changes
- Threshold updates affecting review triggers
- Data source or preprocessing modifications
- Changes to explainability methods
- Changes in intended use or target population

Material changes require:
- Formal governance review
- Impact assessment (risk, bias, explainability)
- Updated evidence artefacts
- Explicit approval prior to release

---

## Change Request & Review Process

1. **Change proposal submitted**  
   Description of change, rationale, and scope

2. **Governance review**  
   Assessment of regulatory, clinical, and governance impact

3. **Evidence update (if required)**  
   Updated explainability, bias, or audit artefacts

4. **Approval or rejection**  
   Decision documented with justification

5. **Controlled release**  
   Versioned release with traceable artefacts

---

## Versioning & Traceability

- Each approved change must result in a new version identifier
- Versions must be linked to:
  - corresponding evidence artefacts
  - audit logs
  - applicable policies
- Previous versions must remain accessible for audit purposes

---

## Emergency Changes
Emergency changes may be applied only when necessary
to mitigate immediate safety or compliance risks.

Emergency actions must:
- be documented retrospectively
- trigger a post-hoc governance review
- result in formal approval or rollback

---

## Relationship to Human Oversight
Change control does **not** replace human oversight.
Instead, it ensures that oversight mechanisms themselves
remain valid and enforceable after changes are introduced.

---

## Relationship to EU AI Act
Supports compliance with:
- **Art. 9** — Risk management
- **Art. 12** — Record-keeping and traceability
- **Art. 14** — Human oversight
- **Art. 15** — Accuracy, robustness, and risk control

---

## Review & Maintenance
- Review cadence: at least annually
- Trigger events:
  - recurring incidents or overrides
  - regulatory updates
  - changes in intended use
  - significant system modifications
- Approval authority: governance lead / compliance function

---

*This policy forms part of the EU AI Act–oriented governance framework
and does not constitute legal advice.*
