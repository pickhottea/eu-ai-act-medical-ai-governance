# P3 — Record-Keeping & Audit Logging

## Purpose
Define record-keeping and audit logging requirements
to ensure that AI system behavior is **traceable, reconstructable,
and auditable** in accordance with the EU AI Act.

---

## Scope
Applies to:
- Model runs and inference executions
- Human review and override actions
- Governance-relevant decisions and incidents

---

## Audit Logging Principles

Audit logs must be:
- **Append-only**
- **Tamper-resistant**
- **Time-stamped**
- **Linked to a specific model version and run ID**

Logs are treated as **governance artefacts**, not operational telemetry.

---

## Minimum Log Contents

Each audit record must include:
- Model identifier and version
- Run ID and execution timestamp
- Input dataset or data slice identifier
- Output prediction and confidence (where applicable)
- Human review status (reviewed / overridden)
- Reference to explainability artefacts (if used)
- Incident or escalation flag (if applicable)

---

## Data Minimization & Privacy

- Logs must not contain direct personal identifiers.
- Any patient-related references must be pseudonymized.
- Access to logs must be restricted to authorized roles only.

---

## Retention & Availability

- Logs must be retained for a period consistent with
  regulatory and organizational requirements.
- Logs must be retrievable in a format suitable for
  internal review or regulatory inspection.

---

## Relationship to EU AI Act
Supports compliance with:
- **Art. 12** — Record-keeping and logging
- **Art. 9** — Risk management
- **Art. 14** — Human oversight (via traceable review actions)

---

*This policy defines governance expectations for auditability
and does not prescribe a specific logging technology.*
