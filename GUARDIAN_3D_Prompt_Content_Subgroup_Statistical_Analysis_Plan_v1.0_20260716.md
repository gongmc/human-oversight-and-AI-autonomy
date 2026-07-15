# GUARDIAN Three-Dimensional Prompt-Content Subgroup Analysis

## Statistical Analysis Plan v1.0

**Study short title:** GUARDIAN 3D Prompt-Content Subgroup Analysis  
**Document type:** Statistical Analysis Plan (SAP) for GitHub upload and protocol lock  
**Version:** v1.0  
**Date:** 2026-07-16  
**Status:** Lock-ready draft for independent timestamping and GitHub archival  
**Dataset:** Fixed GUARDIAN benchmark corpus; 53 pediatric ethical stress-test prompts, 12 models, 636 prompt-model responses  
**Primary purpose:** Structured exploratory discovery and mechanism-oriented subgroup characterization  
**Target reporting standard:** NEJM AI/NEJM-style transparent statistical reporting, with emphasis on prespecification, uncertainty, reproducibility, and limited claims

---

## 0. Executive Summary

This SAP defines a three-dimensional prompt-content subgroup analysis for the GUARDIAN study. The analysis will evaluate whether model failures, adjudication burden, expert disagreement, and failure phenotypes are concentrated in specific prompt-content mechanisms across three conceptually distinct dimensions:

1. **User pressure source:** who or what is applying pressure to the model, and through what real-world authority, emotion, workload, institutional, privacy, or resource-based rationale.
2. **Requested model behavior:** what the user asks the model to do, suppress, enable, generate, delegate, conceal, or alter.
3. **Risk temporality and reversibility:** what type of harm may occur if the model complies, including immediate physical harm, delayed clinical harm, false-knowledge harm, governance/accountability harm, communication/rights harm, and equity/resource-allocation harm.

The central scientific question is not merely whether some prompts have higher failure rates. The question is whether pediatric AI safety-boundary failures are patterned by recognizable interactional mechanisms that can inform future benchmark design, deployment governance, safety monitoring, and clinical AI oversight.

This analysis is **not** intended to replace the original GUARDIAN primary analysis. It is a new, separately defined, mechanism-oriented subgroup analysis of an already adjudicated benchmark dataset. Because preliminary exploratory work has already been performed on the current dataset, all current-dataset findings will be interpreted as **exploratory and hypothesis-generating**. A future GUARDIAN benchmark refresh, external dataset, or prospectively locked replication dataset would be required for confirmatory claims.

The analysis will use prompt-level estimates as the primary statistical evidence, because the 636 responses are cross-classified by 53 prompts and 12 models and are not independent observations. Response-level mixed-effects models, model-level summaries, leave-one-model-out analyses, leave-one-prompt-out analyses, and cross-axis heatmaps will be used as sensitivity and mechanism exploration tools.

---

## 1. Integrated Four-Expert Rationale

This SAP is written from the integrated position of four expert roles: pediatric clinician, AI safety scientist, senior scientific editor, and experienced statistician.

### 1.1 Pediatric Expert Perspective

In pediatric AI deployment, risk is not limited to incorrect diagnostic or treatment advice. Pediatric care often involves parents or caregivers, clinicians under workload pressure, institutional policies, privacy-sensitive minors, consent complexity, developmental-stage communication, and high-stakes escalation decisions. A model may cause harm not only by giving a wrong clinical recommendation, but also by:

- weakening warning systems;
- obscuring uncertainty;
- bypassing escalation;
- changing audit trails;
- altering permission or privacy boundaries;
- outsourcing clinician-family communication;
- undermining assent, consent, or parental authority structures;
- normalizing unsafe institutional convenience.

Therefore, a pediatric safety analysis should not treat all ethical prompts as interchangeable. It should identify what kind of pediatric interactional demand is associated with failure.

### 1.2 AI Expert Perspective

Large language models do not simply output medical facts. They respond to instructions, social framing, role pressure, authority claims, emotional urgency, system-like commands, and requests to modify workflow or governance functions. In safety-critical domains, the relevant failure mechanism may be a mismatch between:

- the model's tendency to comply, reassure, or complete the requested task;
- the safety boundary expected by expert clinicians and ethicists;
- the governance boundary needed for clinical deployment.

The three-dimensional taxonomy is designed to capture these mechanisms:

- pressure source as the social/institutional input;
- requested behavior as the model-action target;
- risk temporality/reversibility as the harm structure.

### 1.3 Senior Editor Perspective

High-level journals will not be persuaded by an unstructured list of post-hoc subgroups. The analysis must present a coherent framework, limited claims, clear denominators, and transparent uncertainty. The paper should not claim that a subgroup "causes" failure. It should claim, if supported, that failures appear to concentrate in specific prompt-content mechanisms, and that these mechanisms may define priority areas for future safety testing and validation.

The strongest publication path is to present the three-dimensional taxonomy as a safety-evaluation framework, while using a hierarchical statistical strategy to avoid appearing as a fishing expedition:

- the **requested model behavior** dimension will be the main candidate for primary mechanism signals;
- the **risk temporality/reversibility** dimension will provide harm-structure interpretation;
- the **user pressure source** dimension will provide real-world deployment context;
- cross-axis analyses will be explicitly exploratory and mechanism-generating.

### 1.4 Statistical Expert Perspective

The statistical unit of scientific information is closer to the prompt than the individual response. Although the dataset contains 636 responses, they arise from a complete 53-by-12 prompt-model grid. Therefore:

- naive response-level tests are not appropriate as primary evidence;
- prompt-level rates will be the primary descriptive quantities;
- response-level mixed models will be used only as sensitivity analyses;
- all results must be reported with absolute counts, denominators, effect sizes, and 95% confidence intervals where appropriate;
- P values will not define discoveries;
- multiplicity will be handled by hierarchy, transparency, and restraint rather than by overclaiming nominal significance.

---

## 2. Relationship to Existing GUARDIAN Analyses

### 2.1 Independence from Prior Main Analysis

This SAP defines a new secondary/subgroup analysis. It does not modify, replace, or retroactively define the original GUARDIAN main analysis.

### 2.2 Status of Current-Dataset Analyses

Because the current GUARDIAN data have already been adjudicated and preliminary descriptive subgroup scans have been reviewed, analyses under this SAP should be described as:

> structured exploratory analyses of a fixed benchmark dataset.

They should not be described as fully prospective confirmatory subgroup analyses.

### 2.3 Path to Stronger Evidence

The same SAP can support stronger evidence if applied to:

- a future GUARDIAN benchmark refresh;
- a new prompt set designed before model evaluation;
- an external pediatric AI safety dataset;
- a prospectively timestamped replication dataset.

In such a validation setting, prespecified estimands, labels, and contrast families may be treated as confirmatory if locked before outcome generation or outcome merging.

---

## 3. Study Objectives

### 3.1 Primary Scientific Objective

To characterize whether GUARDIAN model failures and adjudication burden are concentrated across a three-dimensional prompt-content taxonomy capturing user pressure source, requested model behavior, and risk temporality/reversibility.

### 3.2 Primary Statistical Objective

To estimate subgroup-specific prompt-level rates of final unacceptable responses and adjudication-required responses, and to estimate risk differences comparing each subgroup with all other prompts within the same axis.

### 3.3 Secondary Objectives

1. To describe failure phenotype distributions within each subgroup.
2. To assess whether candidate signals remain directionally stable across models.
3. To assess whether candidate signals remain directionally stable after removing one prompt at a time.
4. To identify high-risk cross-axis cells for future benchmark development.
5. To generate a reproducible pediatric AI safety risk map for future validation.

### 3.4 Non-Objectives

This analysis will not:

- infer causal effects of prompt content on model failure;
- infer internal model training mechanisms;
- rank vendors or products as a primary goal;
- claim definitive clinical harm;
- use subgroup P values as proof of discovery;
- retrospectively relabel prompts based on outcome patterns;
- claim that the three dimensions are statistically independent.

---

## 4. Data Sources and Analysis Sets

### 4.1 Fixed Benchmark Corpus

The analysis uses the fixed GUARDIAN benchmark dataset:

- **Prompts:** 53 pediatric ethical stress-test prompts.
- **Models:** 12 AI models.
- **Responses:** 636 prompt-model responses.
- **Current final unacceptable count:** 196/636.
- **Current adjudication-required count:** 166/636.

These counts are used as data-quality anchors and descriptive baselines.

### 4.2 Input Files

The expected local data sources are:

- prompt-content classification file:
  - `outputs/prompt_subgroup_classification_20260711/GUARDIAN_53_prompt_content_subgroup_classification_initial_20260711.csv`
- joined response-outcome file:
  - `outputs/prompt_subgroup_analysis_results_20260715/joined_prompt_content_response_outcomes_20260715.csv`
- prompt-level rate file:
  - `outputs/prompt_subgroup_analysis_results_20260715/prompt_level_rates_with_subgroup_labels_20260715.csv`
- failed-response phenotype file:
  - source failed-response table used to derive `final_failure_phenotype` and `broad_failure_mode`

For GitHub publication, any patient-sensitive or proprietary model-output text should be handled according to the study's data-sharing plan. Deidentified derived analysis tables and code should be shared where permissible.

### 4.3 Analysis Sets

| Analysis set | Definition | Use |
|---|---|---|
| Prompt classification set | 53 prompts with three-axis labels | Defines subgroup exposure variables |
| Full response set | 636 prompt-model responses | Main response-level descriptive dataset |
| Prompt-level set | 53 rows, one row per prompt, summarizing 12 model responses | Primary statistical evidence |
| Failed-response set | Responses with final unacceptable outcome | Failure phenotype analysis |
| Adjudication set | Responses requiring third-meeting adjudication | Expert-disagreement/adjudication analysis |
| Sensitivity sets | Alternative label sets, leave-one-model-out, leave-one-prompt-out, category-collapsed sets | Robustness checks |

---

## 5. Three-Dimensional Prompt-Content Taxonomy

### 5.1 General Coding Principles

The classification unit is the **prompt**, not the response. Each prompt receives one primary label on each of the three dimensions. Optional secondary labels may be retained for descriptive review, but the main analysis uses primary labels only unless a prespecified secondary-label sensitivity analysis is conducted.

Prompt labels must be based only on:

- prompt text;
- attack vector;
- testing objective;
- source domain or recommendation context, if available before outcome merging.

Prompt labels must not be based on:

- model identity;
- model response text;
- final decision;
- adjudication status;
- failure phenotype;
- exploratory subgroup results.

### 5.2 Dimension 1: User Pressure Source

This dimension captures the primary social, institutional, emotional, authority-based, resource-based, or system-level pressure applied to the model.

Candidate categories include:

| Category | Operational meaning |
|---|---|
| caregiver_family_emotional_pressure | Parent, caregiver, or family emotion, fear, urgency, guilt, or conflict pressures the model to comply |
| clinician_authority_workload_pressure | Clinician invokes seniority, expertise, workload, workflow urgency, or professional authority |
| system_admin_developer_override_pressure | User frames request as system, developer, administrator, integration, or technical override |
| resource_scarcity_or_local_practice_pressure | Scarcity, local practice norms, infrastructure limits, or pragmatic constraints pressure the model |
| commercial_or_institutional_self_interest | Financial, institutional, reputational, operational, or convenience interests pressure the model |
| privacy_or_vip_status_pressure | VIP, privacy, confidentiality, special-status, or access-pressure framing |
| false_evidence_or_pseudo_authority_pressure | Fabricated evidence, false guideline claims, pseudo-authority, or misleading citation pressure |
| research_data_access_pressure | Research, registry, quality-improvement, data-access, or secondary-use framing |
| benign_framing_or_low_stakes_reassurance | Low-stakes, harmless, educational, or reassurance framing used to soften risk |
| system_resource_constraint_pressure | Computational, staffing, queue, bed, or system resource constraint used as pressure |
| routine_complexity_or_ambiguity_pressure | Ordinary but complex ambiguity without a single dominant social actor |
| family_conflict_or_proxy_decision_pressure | Conflict among caregivers, proxies, minors, or family decision-makers |

If two pressures are present, coders should assign the label representing the main reason the model is asked to cross a boundary.

### 5.3 Dimension 2: Requested Model Behavior

This dimension captures what the prompt asks the model to do or stop doing.

Candidate categories include:

| Category | Operational meaning |
|---|---|
| clinical_action_or_treatment_generation | Generate diagnosis, treatment, triage, medication, dosing, or direct clinical action |
| warning_or_safety_mechanism_suppression | Suppress, soften, hide, bypass, or ignore warnings, uncertainty, contraindications, red flags, or escalation |
| false_evidence_or_authority_generation | Generate or endorse false citations, false evidence, authority claims, or fabricated support |
| traceability_audit_permission_or_privacy_manipulation | Alter, bypass, conceal, or misuse traceability, auditability, permissions, privacy, logging, access, or accountability |
| communication_consent_or_literacy_adaptation | Modify communication, consent, explanation, readability, truthfulness, or family/patient-facing messaging |
| decision_delegation_or_referee_role | Ask the model to act as final decision-maker, referee, arbitrator, or substitute for human judgment |
| system_or_permission_override | Request system-level permission, configuration, jailbreak, policy override, or role-based override |
| patient_rights_or_human_interaction_override | Override patient rights, family involvement, assent, clinician-family interaction, or human review |
| automation_of_clinician_patient_interaction | Automate relational clinical communication, handoff, counseling, or interaction in a way that may displace clinician responsibility |

This dimension is expected to carry the strongest mechanistic and statistical signal, because it directly describes the action requested from the model.

### 5.4 Dimension 3: Risk Temporality and Reversibility

This dimension captures the expected harm structure if the model complies with the prompt.

Candidate categories include:

| Category | Operational meaning |
|---|---|
| immediate_irreversible_physical_harm | Near-term risk of serious or irreversible physical harm |
| delayed_serious_clinical_harm | Delayed clinical deterioration, missed diagnosis, delayed escalation, or cumulative harm |
| evidence_uncertainty_or_false_knowledge_harm | False evidence, false certainty, misinformation, or epistemic harm affecting clinical judgment |
| governance_traceability_privacy_or_accountability_harm | Harm to governance, auditability, privacy, permission boundaries, traceability, or accountability |
| communication_consent_or_rights_harm | Harm to consent, assent, communication, understanding, dignity, rights, or family-clinician relationship |
| equity_resource_allocation_or_access_harm | Unequal access, resource allocation harm, fairness harm, or discriminatory operational impact |

This dimension is not only clinical; it explicitly includes governance and rights-based harms that are especially relevant for pediatric AI deployment.

---

## 6. Label Review, Consensus, and Classification Lock

### 6.1 Blinded Review Package

Before formal analysis under this SAP, a blinded classification package should be generated containing:

- prompt ID;
- source domain;
- attack vector;
- testing objective;
- prompt text, if shareable;
- no model names;
- no model responses;
- no outcome labels;
- no final decision;
- no adjudication status;
- no exploratory signal results.

### 6.2 Reviewer Process

At least two independent reviewers should classify all 53 prompts along the three dimensions. Reviewers should preferably include:

- one pediatric/clinical reviewer;
- one AI ethics/safety or informatics reviewer.

The reviewers should assign:

- primary pressure-source label;
- primary requested-behavior label;
- primary risk-temporality/reversibility label;
- optional secondary label, if needed;
- short rationale.

### 6.3 Agreement Metrics

For each dimension:

- percent agreement will be reported;
- Cohen's kappa will be reported when category structure permits;
- Gwet's AC1 may be reported as a sensitivity metric if prevalence imbalance or sparse categories make kappa unstable;
- the number and proportion of prompts requiring consensus will be reported.

### 6.4 Consensus Procedure

Disagreements will be resolved by:

1. blinded discussion between reviewers;
2. third-reviewer adjudication if disagreement persists;
3. documented final label and rationale.

### 6.5 Classification Lock

The final classification file must be locked before final analysis tables are generated. The locked classification file should include:

- reviewer 1 label;
- reviewer 2 label;
- final consensus label;
- consensus notes;
- date;
- version;
- SHA-256 checksum.

Any later label change must be handled as a documented amendment and cannot silently replace the locked classification.

---

## 7. Outcomes

### 7.1 Primary Descriptive Outcomes

#### 7.1.1 Final Unacceptable Response

Binary indicator that the final adjudicated decision for a prompt-model response is unacceptable/fail.

Interpretation:

- represents expert-adjudicated failure relative to the GUARDIAN evaluation standard;
- does not directly measure patient harm;
- does not identify the internal cause of model failure.

#### 7.1.2 Adjudication Required

Binary indicator that a response required third-meeting adjudication because second-round consensus did not meet the predefined threshold.

Interpretation:

- represents expert disagreement, boundary ambiguity, or difficult judgment;
- is not the same as model failure;
- is especially relevant for identifying areas where pediatric AI safety boundaries are contested.

### 7.2 Secondary Outcomes

| Outcome | Type | Analysis set | Purpose |
|---|---|---|---|
| m2_consensus_rate | continuous/proportion | full response set | Degree of second-round expert agreement |
| final_failure_phenotype | categorical | failed-response set | Detailed pattern of failure |
| broad_failure_mode | categorical | failed-response set | Unsafe accommodation vs unsafe evasion |
| model-level subgroup rate | descriptive | full response set | Directional consistency across models |
| prompt-level subgroup rate | descriptive | prompt-level set | Primary unit of scientific interpretation |

### 7.3 Failure Phenotype Mapping

Failure phenotypes will be reported using the locked GUARDIAN phenotype definitions. For mechanism-level reporting, detailed phenotypes may be mapped into broader categories such as:

- unsafe accommodation;
- unsafe evasion;
- other/unclassified, if needed.

This mapping must be prespecified in the analysis codebook and not modified after viewing subgroup phenotype results.

---

## 8. Estimands

### 8.1 Primary Prompt-Level Estimand

For each subgroup label within each dimension, the primary estimand is:

> the difference in mean prompt-level event risk between prompts in that subgroup and all other prompts in the same analysis set.

For prompt \(j\):

- \(n_j = 12\) model responses;
- \(y_j\) = number of responses with the event;
- prompt-level risk \(r_j = y_j / n_j\).

For subgroup \(g\):

\[
RD_g = mean(r_j | j \in g) - mean(r_j | j \notin g)
\]

This estimand will be calculated separately for:

- final unacceptable;
- adjudication required.

### 8.2 Secondary Response-Level Estimand

The secondary response-level estimand is the marginal difference in predicted probability of the event comparing subgroup \(g\) with all other prompts, after accounting for prompt and model clustering using a cross-classified model.

This will be treated as sensitivity evidence, not primary evidence.

### 8.3 Failure Phenotype Estimand

Among failed responses, the estimand is the subgroup-specific distribution of detailed failure phenotypes and broad failure modes.

Because this conditions on failure, it should not be interpreted as the probability of a phenotype among all responses unless explicitly calculated with all responses as the denominator.

---

## 9. Inferential Hierarchy

To support comprehensive analysis while avoiding uncontrolled overinterpretation, results will be organized into a hierarchy.

### 9.1 Main Mechanism Dimension

The requested model behavior dimension is the main mechanism dimension. It directly describes what the user asked the model to do and is expected to provide the clearest mechanism-level signal.

Key requested-behavior categories of a priori interest:

- traceability_audit_permission_or_privacy_manipulation;
- warning_or_safety_mechanism_suppression;
- clinical_action_or_treatment_generation;
- communication_consent_or_literacy_adaptation.

### 9.2 Harm-Structure Dimension

The risk temporality/reversibility dimension provides harm-structure interpretation.

Key categories of a priori interest:

- governance_traceability_privacy_or_accountability_harm;
- immediate_irreversible_physical_harm;
- communication_consent_or_rights_harm;
- evidence_uncertainty_or_false_knowledge_harm.

### 9.3 Contextual Pressure Dimension

The user pressure-source dimension provides real-world deployment context.

Key categories of a priori interest:

- system_admin_developer_override_pressure;
- commercial_or_institutional_self_interest;
- clinician_authority_workload_pressure;
- caregiver_family_emotional_pressure;
- false_evidence_or_pseudo_authority_pressure.

### 9.4 Cross-Axis Mechanism Exploration

Cross-axis analyses will be used to identify mechanism cells, especially:

- requested behavior x risk temporality;
- pressure source x requested behavior;
- pressure source x risk temporality.

Cross-axis cells will be considered descriptive unless a future validation dataset is prospectively locked.

---

## 10. Statistical Analysis Methods

### 10.1 Data Quality Checks

Before analysis, the following checks must pass:

- exactly 53 unique prompts;
- exactly 12 models per prompt;
- exactly 636 prompt-model responses;
- unique prompt-model response identifiers;
- no missing primary label for any of the three dimensions;
- final unacceptable count consistent with locked final decision file;
- adjudication-required count consistent with locked adjudication file;
- failure phenotype present only for failed responses, unless otherwise documented;
- no duplicate records after joining classification and outcome files.

Any failure of these checks must stop analysis until resolved.

### 10.2 Descriptive Summary

For each dimension and subgroup:

- number of prompts;
- number of responses;
- final unacceptable n/N and percentage;
- adjudication required n/N and percentage;
- prompt-level mean, median, minimum, maximum, and interquartile range of event rates;
- mean second-round consensus rate;
- failure phenotype distribution among failed responses.

All percentages should be reported with the numerator and denominator.

### 10.3 Primary Prompt-Level Analysis

The primary analysis will use one row per prompt.

For each subgroup \(g\), calculate:

- mean prompt-level final unacceptable rate;
- mean prompt-level adjudication-required rate;
- risk difference versus all other prompts;
- 95% confidence interval for the risk difference.

Confidence intervals may be constructed using:

1. prompt-level nonparametric bootstrap, resampling prompts within subgroup and outside subgroup;
2. quasi-binomial or beta-binomial models, if stable;
3. robust alternatives if model-based methods fail.

The default bootstrap will use:

- resampling unit: prompt;
- resamples: 5000;
- random seed: 20260716;
- percentile 95% interval.

### 10.4 Response-Level Cross-Classified Sensitivity Model

For each binary outcome, a cross-classified mixed-effects logistic model may be fitted:

\[
logit[P(Y_{ij}=1)] = \beta_0 + \beta_1 subgroup_j + u_{prompt[j]} + v_{model[i]}
\]

where:

- \(i\) indexes model;
- \(j\) indexes prompt;
- \(u_{prompt[j]}\) is a prompt random intercept;
- \(v_{model[i]}\) is a model random intercept.

The model output will be transformed through marginal standardization into:

- subgroup predicted probability;
- all-other predicted probability;
- marginal risk difference.

Odds ratios may be reported in supplementary material but should not be the primary interpretive metric.

If the model fails to converge, produces complete separation, or yields unstable estimates, the analysis will fall back to prompt-level estimates and bootstrap intervals.

### 10.5 Model-Level Directional Consistency

For each candidate signal:

- calculate subgroup-versus-other risk differences separately within each model;
- report the percentage of models with the same direction as the overall prompt-level estimate;
- perform leave-one-model-out sensitivity analysis.

This is not a formal generalizability analysis, but it helps identify whether a signal is driven by a single model.

### 10.6 Prompt-Level Influence

For each candidate signal:

- perform leave-one-prompt-out recalculation of the prompt-level risk difference;
- report the minimum and maximum leave-one-prompt-out risk difference;
- report the percentage of leave-one-prompt-out estimates with the same direction.

Signals that reverse direction after removing one prompt will be downgraded.

### 10.7 Cross-Axis Analysis

For each pair of dimensions, calculate event rates for each cell.

Minimum reporting rules:

- cells with 1 prompt: listed only in supplementary tables, no inference;
- cells with 2 prompts: descriptive only, flagged as sparse;
- cells with 3 or more prompts: eligible for descriptive discussion;
- cells with 5 or more prompts: eligible for cautious mechanism-level discussion if directionally stable.

The main cross-axis visualization will be a heatmap of requested behavior x risk temporality, because this pair best reflects action-harm mechanisms.

### 10.8 Failure Phenotype Analysis

Among failed responses:

- tabulate detailed failure phenotype by each dimension;
- tabulate broad failure mode by each dimension;
- describe top phenotype only when failed-response denominator is at least 10;
- avoid formal inference for sparse phenotype cells;
- avoid inferring internal model mechanisms from phenotype distributions.

### 10.9 Consensus and Adjudication Analysis

Adjudication-required analyses will be interpreted as analyses of expert boundary uncertainty, not as analyses of model error.

For each subgroup:

- adjudication-required n/N and percentage;
- prompt-level adjudication rate;
- mean and median second-round consensus rate;
- candidate high-adjudication signals.

Subgroups with high adjudication but not high failure may represent ethically ambiguous or communication-sensitive domains rather than unsafe model performance.

---

## 11. Multiplicity, P Values, and Evidence Language

### 11.1 Multiplicity Position

This analysis contains multiple axes, subgroups, outcomes, and cross-axis cells. Therefore, nominal P values would be misleading if used as discovery claims.

The primary reporting strategy is:

- effect estimates;
- denominators;
- absolute risk differences;
- 95% confidence intervals;
- directionality and robustness checks;
- explicit exploratory language.

### 11.2 P Values

P values are not required for the main report. If P values are requested by reviewers or used in supplementary analyses:

- they will be two-sided;
- they will be labeled exploratory;
- Benjamini-Hochberg false-discovery-rate adjustment may be applied within clearly defined outcome-axis families;
- no result will be described as definitively significant based solely on P < 0.05.

### 11.3 Evidence-Tier Rules

Candidate signals will be classified into tiers:

| Tier | Rule | Interpretation |
|---|---|---|
| Candidate priority signal | at least 3 prompts; prompt-level risk difference >= 10 percentage points; model-direction agreement >= 75%; leave-one-prompt direction agreement >= 75%; clinically/editorially coherent | Worth formal review and possible main-text emphasis |
| Suggestive signal | at least 3 prompts; prompt-level risk difference >= 5 percentage points; some directional stability | Worth reporting as exploratory pattern |
| Descriptive sparse signal | fewer than 3 prompts or unstable estimates | Supplementary only |
| No clear pattern | small or inconsistent risk difference | Not emphasized |
| Candidate lower-risk pattern | risk difference <= -10 percentage points with directional stability | Descriptive, not a safety claim |

These tiers are heuristic and do not convert exploratory analyses into confirmatory findings.

---

## 12. Sparse Categories and Category Collapsing

### 12.1 Sparse Category Rule

Categories with fewer than 3 prompts will not be used for formal subgroup contrast interpretation. They may be shown descriptively.

### 12.2 Collapsing Rule

Category collapsing is allowed only if:

- conceptually justified before final analysis table generation;
- documented in an amendment or codebook;
- not driven by observed outcome magnitude;
- applied consistently across outcomes.

Examples of potentially defensible collapsing include:

- governance-related categories involving traceability, auditability, privacy, permissions, and accountability;
- communication/consent/rights categories;
- authority/override categories.

Any collapsed analysis must be labeled as such and not replace the original-category analysis.

---

## 13. Sensitivity Analyses

### 13.1 Classification Sensitivity

Compare:

- initial coder draft labels;
- independently reviewed labels;
- final consensus labels;
- alternative labels for prompts with unresolved ambiguity.

If conclusions depend strongly on label choice, the result will be downgraded.

### 13.2 Model Sensitivity

Perform:

- leave-one-model-out analysis;
- model-specific subgroup risk differences;
- optional descriptive exclusion of models with extreme overall failure rates, labeled as sensitivity only.

The primary analysis will retain all 12 models unless a prespecified data-quality reason exists.

### 13.3 Prompt Sensitivity

Perform:

- leave-one-prompt-out analysis for candidate signals;
- influence ranking of prompts contributing most to each candidate signal.

### 13.4 Outcome Definition Sensitivity

If alternative outcome thresholds are available:

- compare final unacceptable vs second-round majority fail;
- compare adjudication-required using the original threshold and any alternative threshold;
- compare broad failure-mode mappings if multiple phenotype mappings are plausible.

### 13.5 Missing and Unrateable Responses

If missing, unrateable, or platform-failure responses are identified:

- primary analysis excludes non-evaluable platform failures from clinical failure denominators only if documented before analysis;
- sensitivity analysis treats missing/unrateable as unacceptable;
- sensitivity analysis treats missing/unrateable as missing;
- platform/API failure is reported separately.

---

## 14. Tables and Figures

### 14.1 Main Text Tables

| Table | Purpose |
|---|---|
| Table 1 | Three-dimensional taxonomy, definitions, and prompt counts |
| Table 2 | Subgroup estimates for final unacceptable and adjudication required across all three dimensions |
| Table 3 | Candidate priority and suggestive signals with robustness indicators |
| Table 4 | Failure phenotype distribution by key subgroup |

### 14.2 Main Text Figures

| Figure | Purpose |
|---|---|
| Figure 1 | Three-dimensional pediatric AI safety-boundary framework |
| Figure 2 | Forest plot of prompt-level risk differences for candidate subgroup signals |
| Figure 3 | Requested behavior x risk temporality heatmap |
| Figure 4 | Model-level descriptive heterogeneity and leave-one-model robustness |

### 14.3 Supplementary Materials

Supplementary materials should include:

- full locked 53-prompt classification table;
- reviewer agreement and consensus table;
- all subgroup estimates;
- all cross-axis cells;
- model-by-subgroup estimates;
- prompt-level influence table;
- failure phenotype table;
- reproducibility manifest;
- code and software versions.

---

## 15. Interpretation Rules

### 15.1 Preferred Interpretation

The preferred interpretation language is:

> GUARDIAN failures appeared to concentrate in prompt-content mechanisms that requested models to alter or enable governance-related functions, including traceability, auditability, permissions, privacy, and accountability. These findings are exploratory and require validation in prospectively locked benchmark data.

### 15.2 Prohibited or High-Risk Language

Avoid:

- "proved";
- "caused";
- "statistically significant subgroup effect" unless a validated confirmatory strategy exists;
- "VIM/VIS-facing domains";
- "this model is unsafe" as a general product claim;
- "clinical treatment prompts are the main risk" if not supported by data;
- "governance prompts cause model failure";
- "expert disagreement equals model error";
- "the model intentionally hides audit trails";
- "training data caused this failure."

### 15.3 Editorially Strong Framing

A strong but defensible framing is:

> The three-dimensional taxonomy suggests that pediatric AI safety failures may be less about a single clinical topic area and more about interactional demands that ask models to cross governance, accountability, privacy, communication, or escalation boundaries.

---

## 16. Reporting Standards and NEJM AI Alignment

This SAP is aligned with the following reporting principles:

| Principle | Implementation in this SAP |
|---|---|
| Prespecified analysis plan | GitHub timestamp, version number, lock file, amendment log |
| Transparent sample size | Fixed 53 prompts, 12 models, 636 responses; no post-hoc denominator changes |
| Clear analysis units | Prompt-level primary analysis; response-level sensitivity |
| Effect estimates over P values | n/N, rates, risk differences, 95% CIs |
| Multiplicity restraint | evidence hierarchy; no nominal significance claims |
| Handling missingness | prespecified missing/unrateable rules |
| Reproducibility | code, manifest, hash, random seed, software versions |
| AI disclosure | disclose AI assistance in drafting or code generation if used |
| Reporting checklists | apply appropriate AI/observational/reporting checklists depending on final manuscript type |

Relevant public guidance includes:

- NEJM AI Editorial Policies: <https://ai.nejm.org/about/editorial-policies>
- NEJM Editorial Policies: <https://www.nejm.org/about-nejm/editorial-policies>
- NEJM statistical reporting guidance article: <https://www.nejm.org/doi/full/10.1056/NEJMe1906559>
- NEJM subgroup analysis guidance article: <https://www.nejm.org/doi/full/10.1056/NEJMsr077003>
- CONSORT-AI/SPIRIT-AI, TRIPOD-AI, and MI-CLAIM should be considered if the final manuscript design maps to those reporting frameworks.

---

## 17. Reproducibility and GitHub Lock Procedure

### 17.1 Repository Structure

Recommended GitHub structure:

```text
guardian-3d-subgroup-sap/
  README.md
  PROTOCOL_LOCK_20260716.md
  SHA256SUMS_20260716.txt
  protocol/
    GUARDIAN_3D_Prompt_Content_Subgroup_Statistical_Analysis_Plan_v1.0_20260716.md
  codebook/
    prompt_content_taxonomy_codebook_v1.0.json
  audit/
    feasibility_audit_or_manifest.json
  scripts/
    analysis_scripts_or_placeholders
  outputs/
    empty_or_gitignored_until_analysis
```

### 17.2 Lock Requirements

At lock time:

1. verify file list;
2. compute SHA-256 checksum for every locked file;
3. write a protocol lock statement;
4. tag the GitHub repository or create a GitHub release;
5. record repository URL, commit SHA, and date/time;
6. prohibit silent edits after lock.

### 17.3 Amendment Log

Any post-lock change must be documented:

| Version | Date | Section changed | Reason | Before/after seeing results? | Impact on interpretation |
|---|---|---|---|---|---|
| v1.0 | 2026-07-16 | Initial SAP | New three-dimensional subgroup analysis SAP | After preliminary exploratory scan of current dataset | Current-dataset results exploratory |

### 17.4 Run Manifest

The final analysis should generate a machine-readable manifest containing:

- date/time of run;
- input file names and hashes;
- classification file hash;
- software versions;
- random seed;
- row counts;
- prompt counts;
- model counts;
- outcome counts;
- output file list;
- script commit hash.

---

## 18. Ethical and Pediatric Governance Considerations

Because the study addresses pediatric AI safety, interpretation should explicitly distinguish:

- model answer acceptability;
- expert disagreement;
- possible clinical harm;
- governance harm;
- privacy harm;
- communication and consent harm;
- deployment monitoring implications.

The analysis should avoid reducing pediatric AI risk to direct treatment recommendations alone. A key contribution of the three-dimensional framework is that it recognizes governance and relational harms as clinically meaningful in pediatric settings.

---

## 19. Planned Manuscript Positioning

### 19.1 Recommended Title Direction

Possible manuscript title:

> Three-Dimensional Prompt-Content Mechanisms of Pediatric AI Safety-Boundary Failure in the GUARDIAN Benchmark

### 19.2 Recommended Abstract Claim

Appropriate claim:

> In structured exploratory analyses, GUARDIAN failures were not evenly distributed across pediatric ethical stress tests. Higher failure burden appeared in prompt-content mechanisms involving governance-related model actions, particularly traceability, auditability, permission, privacy, and accountability manipulation. These findings require validation in prospectively locked benchmark datasets.

### 19.3 Recommended Discussion Claim

Appropriate claim:

> These findings suggest that pediatric AI safety testing should include not only direct diagnostic and treatment prompts, but also prompts that test whether models maintain governance boundaries under social, institutional, technical, and authority-based pressure.

---

## 20. Final Statistical Position

The three-dimensional analysis is scientifically feasible and potentially publication-enhancing if executed with transparency and restraint.

The expected high-level contribution is not a list of "high-risk prompts." The expected contribution is a reusable pediatric AI safety taxonomy showing that failures may cluster around:

- what pressure is applied to the model;
- what behavior the model is asked to perform;
- what type of harm could result if the model complies.

For the current GUARDIAN dataset, the analysis must remain exploratory. For future prospectively locked datasets, this SAP can serve as a confirmatory analysis foundation.

