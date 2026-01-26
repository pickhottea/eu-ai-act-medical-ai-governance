# P4 — Human Oversight & Review Triggers

## Purpose
Establish enforceable **human-in-the-loop** requirements
for high-risk medical AI systems, ensuring that model outputs
remain subject to review, override, and accountability.

---

## Human Oversight Principle

The AI system provides **decision support only**.
Human oversight is mandatory and operationally enforceable.

---

## Review Triggers

### Low-Confidence Predictions
Predictions falling within a predefined low-confidence band
must be reviewed by a qualified human reviewer.

Threshold values are governance-controlled
and recorded per model run.

---

### High-Risk Subgroup Signals
Subgroups exhibiting elevated error rates relative
to the global baseline must trigger heightened oversight,
including increased review sampling.

---

## Override Rules

- Human reviewers may override model outputs.
- Overrides must be documented and justified.
- Override frequency is treated as a governance signal.

---

## Audit Logging of Oversight

Each review or override action must be logged with:
- Reviewer role (pseudonymous)
- Timestamp
- Model version and run ID
- Original prediction and final decision
- Short governance-relevant rationale

---

## Governance Escalation

Persistent review triggers or override patterns
must be escalated to governance review
before any technical changes are made.

---

## Relationship to EU AI Act
Supports compliance with:
- **Art. 14** — Human oversight
- **Art. 12** — Record-keeping
- **Art. 13** — Transparency

---

*This policy ensures that human oversight
remains central to system operation.*
