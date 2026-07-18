# GUARDIAN Statistical Analysis Plan

## Defining, Measuring, and Calibrating Human Oversight and Clinical Autonomy Boundaries in Pediatric Generative Medical AI

Version: v1.0  
Date: 2026-07-18  
Status: existing-data statistical analysis plan for public registration  
Data status: existing GUARDIAN benchmark outcome data only; no new model responses and no new mechanism-code endpoints are introduced in this SAP

## 1. Purpose and Scientific Rationale

This SAP addresses a single scientific question: whether human oversight and clinical autonomy in pediatric generative medical AI can be defined as an observable decision-power boundary, measured using expert-rated benchmark outcomes, and calibrated through interpretable failure patterns.

The analysis is organized around four linked questions:

1. Necessity: Do serious human oversight and clinical autonomy boundary failures occur in pediatric GMAI responses at a level that justifies dedicated evaluation?
2. Externalization: How can an abstract oversight/autonomy principle be translated into observable model behaviors and testable scenario classes?
3. Measurement: How should boundary failures, boundary instability, uncertainty, clustering, concentration, and failure phenotypes be quantified?
4. Calibration: What do the observed failure distributions imply for future model, interface, and institutional calibration?

This SAP does not replace or modify the previously locked GUARDIAN statistical analysis plan. It defines an existing-data analysis and reporting framework that limits the study conclusions to analyses supportable by the available data and explicitly classifies structurally confounded comparisons as descriptive or exploratory.

## 2. Study Design

The study is a fixed-prompt, fixed-model, expert-rated benchmark evaluation of pediatric GMAI responses. Each response is indexed by scenario and model. The analysis uses locked response-level outcome data generated before this SAP.

The unit of observation is the model-scenario response. Because responses are cross-classified by scenario and model, uncertainty will be reported with explicit attention to clustering by scenario and model.

## 3. Analysis Sets

The analysis will use clearly named analysis sets. Public reporting will use descriptive analysis-set names.

### 3.1 Overall GUARDIAN Benchmark Set

This set includes all locked model-scenario responses in the available GUARDIAN benchmark outcome data: 636 responses from 53 scenarios and 12 models.

Purpose: provide study context, denominator lineage, and broad benchmark background. This set is not the primary evidentiary basis for the human oversight and clinical autonomy conclusion.

### 3.2 Primary Human Oversight and Clinical Autonomy Boundary Set

This is the prespecified primary boundary set: 144 responses from 12 scenarios and 12 models.

Purpose: primary analysis of whether human oversight and clinical autonomy boundary failures occur at a clinically meaningful observed frequency.

### 3.3 Operational Governance Boundary Set

This set contains existing responses from traceability, auditability, shutdown, escalation, or governance-control scenarios that operationalize oversight beyond bedside clinician/patient autonomy. The locked primary analysis set contains 144 such responses from 12 scenarios and 12 models. The broader Values in the Model mapping contains 180 expanded-only responses from 15 scenarios and 12 models.

Purpose: evaluate whether additional boundary failures become visible when oversight is externalized as operational governance control. Because this set differs in scenario content and potentially scenario difficulty from the primary boundary set, comparisons with the primary set will be descriptive and mechanism-generating rather than causal.

### 3.4 Expanded Human-Role and Clinical-Autonomy Values in the Model Mapping

This set uses the Values in the Model human-role and clinical-autonomy dimension mapping. It includes the core 144 responses plus expanded governance-related responses, totaling 324 responses in the existing mapping.

Purpose: evaluate measurement sensitivity to broader externalization of human oversight. Dimension rankings and rank changes will be treated as exploratory because scenario membership and denominators differ across dimensions.

### 3.5 Model Categories

Models are grouped as general foundation models and medical-vertical models according to the existing classification. Because category is nested within model and may be confounded by vendor, base model, training data, deployment channel, and safety middleware, all model-category analyses are exploratory and noncausal.

## 4. Conceptual Externalization Framework

Human oversight and clinical autonomy will be defined as a decision-power boundary involving four observable components.

1. Responsibility boundary: whether the model preserves clinician judgment and accountable medical responsibility rather than substituting for the clinician.
2. Autonomy boundary: whether the model preserves patient, child, caregiver, and clinician rights to be informed, refuse, choose, and deliberate.
3. Qualification boundary: whether the model avoids enabling unqualified or lower-authority users to perform actions outside their role.
4. Operational governance boundary: whether the model preserves escalation, human review, auditability, traceability, and the ability to stop unsafe automation.

This framework is interpretive and measurement-oriented. Mechanism-specific variables such as role overstep, accountability abdication, patient autonomy violation, qualification boundary failure, communication outsourcing, preserved human review, preserved safe escalation, and preserved auditability will not be reported as empirical endpoints unless independently coded by at least two coders with adjudication and reliability analysis.

## 5. Outcomes

### 5.1 Primary Outcome

Final unacceptable response in the primary human oversight and clinical autonomy boundary set.

Definition: a response judged finally unacceptable by the locked expert evaluation process.

Primary estimand: observed final unacceptable rate in the primary boundary set.

Primary reporting: number of failures, denominator, observed percentage, Wilson interval, scenario-cluster bootstrap interval, and model-cluster bootstrap interval. The model-cluster bootstrap interval will be highlighted when discussing generalizability across models because model-level heterogeneity is expected and clinically relevant.

### 5.2 Key Secondary Outcome

Third-round adjudication requirement in the primary human oversight and clinical autonomy boundary set.

Definition: whether the response required third-round adjudication in the locked expert evaluation workflow.

Interpretation: adjudication requirement will be treated as a marker of boundary instability or expert disagreement. It will not be described as an independent predictor of final failure because adjudication is part of the rating workflow that produced the final outcome.

### 5.3 Secondary Descriptive Outcomes

1. Final unacceptable response in the operational governance boundary set.
2. Third-round adjudication requirement in the operational governance boundary set.
3. Final unacceptable response in the expanded Values in the Model human-role and clinical-autonomy mapping.
4. Failure phenotype among failed responses, including sycophancy/empathy misuse and defensive evasion/mechanical refusal.
5. Model-level distribution of failures, including number of models with any failure, top-k failure share, Herfindahl-Hirschman index, effective number of contributing models, Gini coefficient, and normalized entropy.

### 5.4 Exploratory Outcomes

1. Model-category differences in failure rates and failure phenotypes.
2. Values in the Model dimension ranking and rank uncertainty.
3. Governance-expanded versus primary-boundary comparisons.
4. Equal-opportunity or resampling-based sensitivity analyses comparing sets with unequal scenario counts.

Exploratory outcomes may be reported when scientifically useful but will not be placed as headline claims in the abstract or key points unless their limitations are explicitly stated.

## 6. Primary Analysis

The primary analysis will estimate the final unacceptable response rate in the primary human oversight and clinical autonomy boundary set.

Required reporting:

1. Numerator and denominator.
2. Observed percentage.
3. Wilson 95% confidence interval at the response level.
4. Scenario-cluster bootstrap 95% interval.
5. Model-cluster bootstrap 95% interval.
6. Brief interpretation emphasizing both clinical materiality and model-level uncertainty.

Interpretive rule:

The primary result supports the conclusion that serious human oversight and clinical autonomy boundary failures occur in the benchmark and warrant dedicated evaluation. It does not estimate real-world incidence and does not support durable ranking of specific products.

## 7. Boundary Externalization Analysis

This analysis addresses whether different ways of externalizing human oversight reveal different failure patterns.

### 7.1 Primary Versus Operational Governance Boundary

The observed failure and adjudication rates will be reported for:

1. Primary human oversight and clinical autonomy boundary set.
2. Operational governance boundary set.
3. Combined broader oversight/governance set, if used for descriptive context.

Because these are different scenario sets, the comparison will be descriptive. Fisher exact tests or unpaired response-level P values will not be used as headline evidence for a governance-extension effect. Risk differences and risk ratios may be reported as descriptive contrasts only, with clear notation that they are not causal estimates and may reflect scenario difficulty.

Preferred wording:

"When oversight was externalized as operational governance control, additional failures were observed."

Prohibited wording:

Any wording that treats the governance comparison as causal, confirmatory, or proof of a universal model-level phenomenon.

### 7.2 Values in the Model Mapping Sensitivity

The Values in the Model human-role and clinical-autonomy dimension will be analyzed in its core and expanded mappings. Results will include numerator, denominator, rate, bootstrap rank interval, and the denominators used for all dimensions being compared.

Dimension ranking is exploratory. Rank changes will be interpreted as measurement sensitivity to externalization rather than as a definitive hierarchy of value risks.

## 8. Boundary Instability and Adjudication Analysis

Adjudication requirement will be analyzed as a process marker of boundary instability.

Required analyses:

1. Final unacceptable rate among adjudicated responses.
2. Final unacceptable rate among non-adjudicated responses.
3. Risk ratio and odds ratio may be reported descriptively.
4. Positive likelihood ratio will not be emphasized and should be omitted from the main report.

Interpretive rule:

Adjudication enrichment will be described as evidence that expert disagreement clusters around unstable boundary cases. It will not be presented as a deployable prediction rule or independent risk signal.

## 9. Failure Phenotype Analysis

Failure phenotype analysis will be restricted to responses already judged unacceptable. The purpose is to distinguish directions of boundary failure rather than to estimate overall prevalence of each mechanism.

Main phenotype categories:

1. Sycophancy or empathy misuse: the model over-accommodates user pressure, emotional framing, or unsafe preference in ways that displace clinical judgment or patient protection.
2. Defensive evasion or mechanical refusal: the model withdraws, refuses, or issues procedural disclaimers in ways that fail to preserve safe escalation, accountable handoff, or clinical next steps.

Required reporting:

1. Phenotype count among failed responses.
2. Percentage among failed responses.
3. Wilson 95% interval where appropriate.
4. Model-category phenotype contrasts as exploratory only.
5. Model-level permutation or model-cluster bootstrap for exploratory category contrasts when reported.

Interpretive rule:

Phenotype results support the calibration argument that oversight failures have different directions and therefore require more precise calibration than generic refusal tuning.

## 10. Model Heterogeneity and Concentration

Model heterogeneity will be treated as a central feature of the data, not only a nuisance.

Required analyses:

1. Per-model final unacceptable rates in the primary boundary set.
2. Number of models with any failure.
3. Top-1, top-2, and top-3 failure share.
4. Effective number of contributing models.
5. Leave-one-model-out sensitivity for the primary outcome where available.

Interpretive rule:

Model heterogeneity supports the need for model-specific calibration and post-deployment monitoring. It does not support durable public ranking of products or claims about entire model categories.

## 11. Model-Category Analyses

Model-category analyses will be exploratory and noncausal.

Analyses may include:

1. Failure rate by model category in the primary boundary set.
2. Adjudication rate by model category.
3. Failure phenotype distribution by model category among failed responses.
4. Model-level exact permutation or model-cluster bootstrap for robustness.

Required caveat:

Model category is nested within model and confounded by vendor, base model, training procedure, deployment channel, and safety middleware. Category contrasts will not be placed as a primary or headline finding.

## 12. Uncertainty Estimation

Because responses are clustered by both scenario and model, uncertainty reporting will use multiple complementary intervals.

1. Wilson confidence intervals: response-level descriptive intervals.
2. Scenario-cluster bootstrap intervals: sensitivity to scenario sampling.
3. Model-cluster bootstrap intervals: sensitivity to model sampling.
4. Two-way or crossed bootstrap: optional sensitivity if feasible and computationally stable.

Reporting priority:

For the primary outcome, public reporting will include the observed percentage together with the model-cluster bootstrap interval in the abstract or main summary. Wilson intervals may be reported in the table or supplement.

## 13. Multiple Testing

No multiplicity adjustment is required for the single primary outcome.

Exploratory dimension-level or multiple-domain comparisons will use false-discovery adjustment where already specified in the existing analysis. Adjusted and unadjusted P values will not be interpreted as confirmatory evidence if the underlying comparison involves nonexchangeable scenario sets or unequal denominators.

## 14. Sensitivity Analyses

### 14.1 Cluster Sensitivity

The primary result will be compared across Wilson, scenario-cluster bootstrap, and model-cluster bootstrap intervals.

### 14.2 Leave-One-Model-Out Sensitivity

The primary boundary failure rate will be recalculated after excluding one model at a time, if available from existing outputs.

### 14.3 Leave-One-Scenario-Out Sensitivity

The primary boundary failure rate will be recalculated after excluding one scenario at a time, if available or feasible from existing data.

### 14.4 Equal-Opportunity Governance Sensitivity

If comparing primary and operational governance sets with different scenario counts, an equal-scenario resampling analysis may be used. For each iteration, an equal number of scenarios will be sampled from each set, preserving all model responses for selected scenarios. The distribution of failure rates, risk differences, and number of models with any failure will be summarized.

This analysis remains exploratory because scenario content is not exchangeable and difficulty may differ.

### 14.5 Rank Robustness Sensitivity

For Values in the Model dimension ranking, bootstrap rank intervals and denominator tables will be reported. Rank changes will be considered unstable if rank intervals are wide or overlap multiple positions.

## 15. Main Table Plan

The main report will contain one primary results table with statistical values only, without interpretation text.

Recommended rows:

1. Overall GUARDIAN benchmark final unacceptable responses.
2. Primary human oversight and clinical autonomy boundary final unacceptable responses.
3. Primary boundary adjudication requirement.
4. Operational governance boundary final unacceptable responses.
5. Operational governance boundary adjudication requirement.
6. Expanded Values in the Model human-role and clinical-autonomy mapping final unacceptable responses.
7. Adjudicated versus non-adjudicated final unacceptable responses in the primary boundary set.
8. Failure phenotype distribution among primary-boundary failures.
9. Exploratory model-category failure rate, clearly labeled exploratory.
10. Model-cluster bootstrap interval for the primary boundary outcome.

Table columns:

1. Analysis domain.
2. Analysis set.
3. Endpoint.
4. Numerator/denominator.
5. Observed percentage.
6. Response-level 95% CI, if applicable.
7. Cluster-aware interval or robustness statistic.
8. Statistical test, if appropriate.
9. Analysis status: primary, secondary descriptive, or exploratory.

No interpretation column will be included in the main table.

## 16. Figure Plan

Figure 1: Study flow and analysis-set lineage. This figure should show the relationship among the overall benchmark set, primary boundary set, operational governance set, expanded mapping set, and non-boundary comparator set.

Figure 2: Primary boundary burden and uncertainty. This figure should show observed failure and adjudication rates with Wilson, scenario-cluster, and model-cluster uncertainty.

Figure 3: Boundary externalization map. This figure should show how the abstract oversight/autonomy principle is externalized into responsibility, autonomy, qualification, and operational governance boundary components, linked to measurable outcomes.

Figure 4: Calibration-oriented failure phenotype figure. This figure should show the distribution of failure phenotypes and model heterogeneity, emphasizing different calibration targets.

## 17. Reporting Rules for Study Claims

### 17.1 Allowed Primary Claim

The benchmark identified measurable and clinically material failures of human oversight and clinical autonomy in pediatric GMAI responses, supporting the need to evaluate this boundary as a dedicated safety domain.

### 17.2 Allowed Externalization Claim

Different externalizations of human oversight identify different failure patterns. Operational governance scenarios make visible failures related to auditability, traceability, escalation, and shutdown that are not captured by narrow bedside autonomy prompts alone.

### 17.3 Allowed Calibration Claim

Observed failures differ in direction, including over-accommodating unsafe user pressure and mechanically withdrawing without preserving safe next steps. Oversight calibration therefore requires preserving the correct distribution of decision authority, not merely increasing refusals or generic disclaimers.

### 17.4 Claims Requiring Downgrade

1. Governance-expanded versus primary-boundary comparisons: descriptive, not causal.
2. Model-category contrasts: exploratory and noncausal.
3. Values in the Model rank changes: measurement-sensitivity findings, not definitive rankings.
4. Adjudication enrichment: process association, not independent prediction.

### 17.5 Claims Not Authorized by Current Data

The study report will not present empirical prevalence or association results for uncompleted mechanism-code endpoints, including role overstep, accountability abdication, patient autonomy violation, qualification boundary failure, communication outsourcing, preserved human review, preserved safe escalation, or preserved auditability.

## 18. Missing Data and Data Integrity

Analyses will use locked complete response-level outcome data. Any missing outcome, missing model identifier, missing scenario identifier, or duplicate response index will be documented before analysis. No imputation will be performed for primary outcomes.

## 19. Software and Reproducibility

Analyses will be performed using scripted, reproducible code. All reported tables will be generated from source data or locked statistical output files and must be traceable to a source table and versioned output.

The public repository or registration package should include:

1. This SAP.
2. The original locked SAP or protocol package.
3. A data lineage table defining all analysis sets.
4. Source data sufficient to reproduce reported tables, subject to any confidentiality limits.
5. Analysis code and session information.
6. A version-controlled change log.

## 20. Article Transparency Statements

The study report should include:

1. Ethics or IRB statement.
2. Data availability statement.
3. Code availability statement.
4. Funding statement.
5. Conflict of interest statement.
6. Author contribution statement.
7. Disclosure of overlap with any prior, submitted, or concurrent GUARDIAN publication or submission using shared benchmark data.

## 21. Planned Reporting Structure

The Results section should follow this order:

1. Analysis-set lineage and data structure.
2. Primary boundary failure burden with cluster-aware uncertainty.
3. Adjudication as boundary instability.
4. Boundary externalization: primary versus operational governance, descriptive only.
5. Failure phenotype and calibration implications.
6. Model heterogeneity and exploratory category findings.
7. Sensitivity analyses and limitations of inference.

The Discussion should be organized around:

1. Human oversight as a measurable decision-power boundary.
2. Why narrow "human-in-the-loop" statements are insufficient.
3. Why calibration must preserve responsibility, autonomy, qualification, and governance pathways.
4. Why pediatric deployment requires special attention to distributed authority among clinicians, children, caregivers, and institutions.
5. Limitations, including benchmark design, clustering, model version instability, noncausal exploratory comparisons, and incomplete mechanism coding.

## 22. Verification Criteria Before Public Release

Before public posting or journal submission, the following checks must pass:

1. All primary results report numerator, denominator, observed percentage, and cluster-aware uncertainty.
2. No unpaired governance comparison is presented as causal or confirmatory.
3. No model-category comparison appears as a headline finding.
4. No Values in the Model rank change is presented without denominator and uncertainty context.
5. No uncompleted mechanism-code endpoint is reported as empirical evidence.
6. Public-facing text uses descriptive analysis-set names.
7. The framework name "Values in the Model" is used correctly.
8. All data overlap with concurrent or prior GUARDIAN reports, publications, or submissions is disclosed.
