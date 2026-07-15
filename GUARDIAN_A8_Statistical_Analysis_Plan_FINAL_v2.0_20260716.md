# GUARDIAN-A8 Statistical Analysis Plan

**Version:** FINAL v2.0  
**Date locked:** 2026-07-16  
**Study type:** fixed-corpus, post-hoc exploratory secondary analysis of an already adjudicated GUARDIAN dataset  
**Primary analysis set:** A8 Core, 12 scenarios x 12 models = 144 model-scenario responses  

## Final Statistical Review

This SAP is scientifically feasible for a high-level exploratory secondary analysis, provided the main evidentiary claim is descriptive and calibration-focused rather than causal. The A8 Core dataset is complete and internally linkable, but it is small for complex crossed mixed models: 144 responses, 12 scenario clusters, 12 model clusters, and 32 final failures. Therefore, descriptive estimates, model-level exact permutation, and prespecified sensitivity analyses carry the primary evidentiary weight; cross-classified hierarchical models are exploratory/supportive.

## Data Lock

| Analysis set | Scenarios | Models | Responses | Final failures | Adjudication |
|---|---:|---:|---:|---:|---:|
| Overall GUARDIAN | 53 | 12 | 636 | 196/636 (30.8%; Wilson 95% CI 27.4-34.5%) | 166/636 (26.1%) |
| A8 Core | 12 | 12 | 144 | 32/144 (22.2%; Wilson 95% CI 16.2-29.7%) | 24/144 (16.7%) |
| A8 Extended | 24 | 12 | 288 | 92/288 (31.9%; Wilson 95% CI 26.8-37.5%) | 75/288 (26.0%) |
| Non-A8 comparator | 29 | 12 | 348 | 104/348 (29.9%; Wilson 95% CI 25.3-34.9%) | 91/348 (26.1%) |

## Endpoint Hierarchy

Primary endpoint: expert-final value-boundary miscalibration in A8 Core, derived from the locked final pass/fail decision.

Key secondary endpoints: third-round adjudication requirement, A8 Extended sensitivity result, model-category contrasts, and the distribution of existing failure phenotypes among A8 failures.

Unsupported in current locked data: role_overstep, accountability_abdication, patient_autonomy_violation, qualification_boundary_failure, communication_outsourcing, human_review_preserved, safe_escalation_preserved, and auditability_preserved as newly coded mechanism endpoints. These may be used only in a future independently coded substudy.

## Main Analysis Rules

1. The primary claim will be descriptive: A8 human-oversight and clinical-autonomy boundaries can be externalized, measured, and calibrated in the fixed GUARDIAN corpus.
2. Report n/N, percentage, and Wilson 95% CI for binary endpoints. Exact counts take priority over p values.
3. Model-category contrasts are exploratory because model category is nested within model and there are only 12 model clusters.
4. Use model-level exact permutation as the most transparent model-category sensitivity analysis: aggregate A8 Core failure rates by model, preserve the 4-versus-8 medical/general category split, and enumerate all 495 possible assignments.
5. Use cross-classified hierarchical logistic regression only as a supportive model. If it fails to converge, is singular, or shows quasi-separation, report this and use penalized/Bayesian or model-level analyses instead.
6. Domain-level differences are descriptive only; Recommendation 28 has one scenario and cannot support domain-level inference.
7. No causal language is allowed. The analysis evaluates observed association and value-boundary behavior in a locked benchmark corpus.

## Claim Hierarchy

Allowed primary claim: A8 human-oversight boundary miscalibration is measurable in GUARDIAN and can be summarized with transparent uncertainty.

Allowed exploratory claim: medical vertical systems may show higher observed A8 miscalibration/adjudication burden than general foundation systems, if the prespecified model-level and sensitivity analyses are directionally consistent.

Allowed mechanism-framing claim: A8 failures show a bidirectional pattern using existing failure phenotypes, spanning unsafe accommodation/sycophancy and defensive evasion/mechanical refusal.

Not allowed: claims that medical fine-tuning causes failure, that A8 estimates generalize to all clinical AI deployments, or that newly proposed mechanism variables were measured in the locked dataset.
