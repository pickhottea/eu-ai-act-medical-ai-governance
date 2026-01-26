# Project 1 — End-to-End Governance Evidence for High-Risk AI (EU AI Act)

AI-assisted diagram (ChatGPT)

![Project 1 Governance Overview](docs/project1_governance_overview.png)

---

## Overview

This repository documents **Project 1** of an EU AI Act–focused portfolio.

The project demonstrates how a **high-risk AI system** can be documented,
audited, and governed in line with the *spirit and structure* of the EU AI Act —
with emphasis on **evidence generation**, not model optimisation.

The core objective is to show how **technical artefacts**
(models, metrics, explainability outputs)
are translated into **audit-ready governance evidence**.

---

## Company Context & High-Risk Positioning

This project is framed in the context of **MediFuture GmbH**, a consulting-oriented
AI solutions provider specialised in **high-risk medical AI systems**.

MediFuture supports hospitals and clinical operators in:
- designing AI-assisted decision-support systems,
- establishing audit-ready governance structures,
- and preparing for regulatory compliance under the EU AI Act.

The demonstrated system (Thorax X-ray analysis) falls into a **medical context**
and is therefore considered **high-risk AI** under the EU AI Act,
subject to strict governance, documentation, and oversight requirements.

---

## High-Risk Classification & Regulatory Mapping

| Dimension | Project Positioning |
|--------|--------------------|
| Sector | Healthcare / Medical AI |
| Intended Purpose | Clinical decision support (alerting, not autonomous diagnosis) |
| EU AI Act Risk Class | High-Risk AI (medical context, Annex III) |
| Human Oversight | Mandatory (radiologist review, override possible) |
| Deployment Mode | Decision support only |
| Data Sensitivity | Medical imaging / clinical data |
| Consequence of Error | Potential impact on health and safety |

---

## Scope & Datasets

Project 1 intentionally combines **three datasets** and **three analysis paradigms**,
each with a clearly defined role:

| Dataset | Modality | Role in Project 1 | Explainability |
|------|--------|------------------|----------------|
| Pneumonia (Chest X-ray) | Medical images (CNN) | **Primary high-risk SaMD-style demo** | CAM / Grad-CAM |
| Stroke dataset | Tabular (clinical) | Explainability & bias *method demo* | SHAP |
| Breast cancer dataset | Tabular (diagnostic) | Explainability *method demo* | SHAP |

Only the **Pneumonia CNN** represents an end-to-end medical AI workflow.
The Stroke and Breast datasets are explicitly **method demonstrations**
and do **not** constitute medical performance claims.

---

## Analysis Methods

### 1) CNN-based Medical Image Analysis (Pneumonia)

- Model: ResNet-18 (transfer learning)
- Task: Binary classification (NORMAL vs. PNEUMONIA)

**Explainability**

CAM-based visual explainability (implemented via **Grad-CAM / Grad-CAM++**)
is used to highlight image regions contributing to model decisions.

Stored artefacts include:
- One **True Positive** Grad-CAM example
- One **False Positive** Grad-CAM example

**Interpretation note**

Grad-CAM heatmaps indicate which image regions contributed most to the model’s decision.
They are intended to support human review, not to replace clinical judgement.

In false positive cases, highlighted regions may correspond to artefacts
or non-pathological patterns, reinforcing the need for expert override.

---

### 2) Tabular Models (Stroke & Breast)

- Stroke: XGBoost classifier (gradient-boosted decision trees)
- Breast: Logistic Regression (linear baseline)
- Purpose: Demonstrate explainability and bias analysis techniques

**Explainability**

SHAP is used for:
- Global explanations (summary plots)
- Local explanations (case-level waterfall plots)

**Bias / Robustness Signals**

Proxy-based subgroup slicing (e.g. age buckets, feature thresholds)
is applied to identify **reliability gaps**.

These analyses are framed as **robustness signals**, not fairness claims.

---

## Governance Policies & Operating Procedures

Project 1 is supported by a set of **explicit governance policies**
that operationalise EU AI Act requirements.

| ID | Policy | Scope |
|----|------|------|
| P1 | Roles & Responsibilities (Provider vs Operator) | Accountability & RACI |
| P2 | High-Risk Classification & Intended Purpose | Risk positioning (Annex III) |
| P3 | Technical Documentation Index | Required artefacts & versioning |
| P4 | Post-Market Monitoring & Continuous Improvement | KPIs, frequency, ownership |
| P5 | Incident Response & Corrective Measures | Stop, override, rollback |
| P6 | Change Control & Release Governance (QMS-lite) | Controlled updates |


See `docs/policies/` for full policy texts.

## Governance & Audit Evidence

Project 1 follows an **audit-first design**.

The notebooks act as **evidence generators**, not analytical reports.
Key governance artefacts include:

- **Model performance evidence** (confusion matrices)
- **Explainability artefacts** (CAM & SHAP)
- **Bias / robustness indicators**
- **Human review policies**
- **Append-only audit logging**

All artefacts are mapped to EU AI Act–style evidence categories (A–D).

---

## Record-Keeping (Art. 12 Spirit)

Each run appends a machine-readable audit record capturing:
- dataset and split identifiers
- model version and configuration
- evaluation metrics
- explainability artefact references
- review and override indicators

---

## Continuous Improvement & Post-Market Perspective

This project is designed as an **iterative governance setup**, not a one-off demo.

Continuous improvement is addressed through:

- **Post-Market Monitoring**  
  Regular review of performance, robustness, and bias signals
  (e.g. error rates, proxy-based slicing, drift indicators).

- **Corrective Measures**  
  Identified issues trigger documented actions such as:
  preprocessing adjustments, data review, recalibration, or retraining.

- **Conformity Maintenance**  
  Governance artefacts (logs, policies, evidence) are reviewed and updated
  whenever:
  - the model changes,
  - the data distribution shifts,
  - or regulatory interpretations evolve.

This reflects the EU AI Act expectation that compliance is a **continuous process**,
not a static certification state.

---

## Regulatory Alignment (Contextual)

Beyond the EU AI Act, medical AI systems operate within a broader regulatory landscape.

This project acknowledges alignment with:
- **Medical Device Regulation (MDR / IVDR)** for AI-based medical software (SaMD),
- **GDPR** with respect to sensitive health data and auditability,
- **Data Act** regarding data access and governance,
- **Digital Services Act (DSA)** where applicable to AI-enabled digital services.

For medical AI applications in Germany, oversight by
**BfArM (Bundesinstitut für Arzneimittel und Medizinprodukte)**
is recognised as a relevant supervisory context.

The project also follows international best-practice principles,
such as those described in **ISO/IEC 42001** for AI management systems.

