# GUARDIAN A8 Strengthened Secondary Statistical Analysis Plan (LOCKED v1.0)

Lock date: 2026-07-17

Status: locked for GitHub registration before manuscript-level interpretive updating. This plan does not replace the previously locked A8 primary SAP. It defines a secondary, existing-data-only strengthening analysis focused on the human oversight and clinical-autonomy boundary.

## 1. Scope and claim boundary

This strengthened SAP uses only data already available in the locked GUARDIAN A8 statistical outputs and the existing 8-dimensional VIM response-level mapping. No new DPB mechanism-coding endpoint is analyzed here, because independent DPB coding is incomplete. Empirical claims about role_overstep, accountability_abdication, patient_autonomy_violation, qualification_boundary_failure, communication_outsourcing, human_review_preserved, safe_escalation_preserved, or auditability_preserved remain unauthorized until the two-coder plus adjudication workflow and reliability reporting are complete.

Two analysis sources are explicitly separated:

1. Locked A8 primary analysis set: A8 Core n=144, A8 Extended n=288, A8 Extended-only n=144, Non-A8 comparator n=348.
2. VIM D8 response-level mapping: D8 Core n=144, D8 expanded-only n=180, D8 expanded n=324. This mapping is used for dimension-rank, phenotype-polarization, and boundary-diffusion analyses.

## 2. Objectives

The primary objective of this secondary analysis is to determine whether the human oversight/clinical-autonomy value dimension shows a structural pattern that is not visible in the main descriptive rate alone.

Prespecified secondary questions:

1. Rank inversion: Does D8/A8 appear low risk when narrowly externalized as core clinician/patient autonomy, but higher risk when expanded to traceability, auditability, shutdown, and institutional governance?
2. Governance-extension effect: Does the extended governance boundary have higher failure and adjudication rates than the A8 Core boundary?
3. Boundary diffusion: Does the extended boundary change failure from concentration in a few models to a vulnerability observed across most or all models?
4. Failure phenotype polarization: Among D8 failures, do general foundation and medical-vertical models fail through different observable phenotypes?
5. Adjudication signal: Does third-round adjudication identify a subgroup enriched for final failure?

## 3. Endpoints and estimands

Primary endpoints for this strengthened module are final failure and third-round adjudication. Secondary endpoints are failure phenotype among failed responses and model-level any-failure status.

Estimands:

- Absolute risk with Wilson 95% confidence interval.
- Risk difference, risk ratio, and odds ratio for two-group contrasts.
- Fisher exact two-sided p value for response-level two-by-two contrasts.
- Exact model-label permutation p value for model-category contrasts where model-level summaries are the unit of inference.
- Prompt-cluster and model-cluster bootstrap intervals for D8 governance-extension risk differences.
- Concentration metrics: models with any failure, top-k failure share, Herfindahl-Hirschman index, effective number of contributing models, Gini coefficient, and normalized entropy.
- Dimension rank among the 8 VIM dimensions, with prompt-cluster bootstrap rank uncertainty.

## 4. Multiplicity and interpretation

For dimension-vs-other screening across D1-D8, Benjamini-Hochberg false discovery rate q values are reported separately by set type and endpoint. Other analyses are treated as structured secondary/exploratory analyses and are interpreted by effect size, direction consistency, and sensitivity rather than p values alone.

Strong secondary claims require: consistent direction, clinically/scientifically meaningful effect size, no contradiction under model or prompt clustering, and transparent data-source labeling.

## 5. Sensitivity analyses

The governance-extension effect is assessed with leave-one-model and leave-one-domain sensitivity. Phenotype polarization is assessed with a model-level exact permutation and model-cluster bootstrap. Boundary diffusion is assessed with paired exact McNemar testing of model-level any-failure status.

## 6. Reporting rule

Results from this module may support manuscript language about a decision-power-boundary pattern only at the level of observed A8/D8 outcomes. They may not be described as empirical DPB mechanism-code findings until independent DPB coding and reliability analysis are complete.
