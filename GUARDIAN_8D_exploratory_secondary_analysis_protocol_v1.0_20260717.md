# GUARDIAN 8D Exploratory Secondary Analysis Protocol and Statistical Analysis Plan

Version: 1.0  
Protocol date: 2026-07-17  
Analysis status: Exploratory secondary analysis protocol, locked for strict execution  
Short title: GUARDIAN 8D pediatric value-boundary reliability analysis  
Target use: GitHub protocol record and manuscript-supporting statistical analysis plan  

## 1. Protocol Status and Locking Rule

This document prespecifies the exploratory secondary analysis of the locked GUARDIAN response-level dataset using an eight-dimensional pediatric value-boundary framework. It is not a prospective protocol for the original GUARDIAN benchmark data collection, response generation, expert evaluation, or adjudication. Those source data were generated and locked for the earlier GUARDIAN NEJM AI submission package.

This protocol is the governing analysis plan for the current eight-dimensional re-analysis. After this version is placed under version control, all analyses, tables, figures, and manuscript numerical claims for the 8D analysis must either follow this protocol or be explicitly labelled as post-protocol exploratory additions.

Any change to dimensions, analysis populations, outcomes, support-tier rules, statistical tests, multiplicity handling, or interpretation boundaries after protocol lock requires a dated amendment and a new protocol version.

## 2. Study Design

This is an exploratory cross-sectional secondary analysis of a previously locked pediatric medical-AI benchmark dataset. The unit of analysis is one model response to one pediatric ethics stress-test prompt.

No new model prompts will be run for this analysis. No new response acceptability adjudication will be performed. The analysis applies a conceptually defined eight-dimensional pediatric value-boundary framework to the locked GUARDIAN response-level dataset and reports signal localisation, denominator support, and interpretation boundaries.

## 3. Source Dataset and Data Lock

The source response/outcome dataset is the GUARDIAN NEJM AI locked supplementary dataset.

Controlled source files:

| File | Role | Expected rows | SHA-256 |
|---|---:|---:|---|
| Supplementary_Data_S1_Final_Decisions_English.csv | Final prompt-model decisions and adjudication source | 636 | 7f806f1cee7b849c30e11366802d6a983e36d3fad6b2a80cd041fdd0c9601288 |
| Supplementary_Data_S2_Model_Responses_12x53_636_English.csv | Anonymized prompt-model responses | 636 | d44fdfe06d7c99d3c2a9dc8f7b21a5d27ad13bba979851cb59a5affbc4d30ba7 |
| Supplementary_Data_S2_Model_Responses_12x53_636_English.xlsx | Spreadsheet version of response dataset | 636 | d2701ad076ab8c18604990afd2b9ec74b346cbe0c381b2824f84c83128bb83be |

Required source-data checks before running the 8D analysis:

1. `Supplementary_Data_S1_Final_Decisions_English.csv` has 636 rows.
2. `Supplementary_Data_S2_Model_Responses_12x53_636_English.csv` has 636 rows.
3. `prompt_model_id` is unique in both files.
4. The two `prompt_model_id` sets match exactly.
5. The dataset contains 53 final prompts and 12 models, with 12 responses per prompt and 53 responses per model.
6. The main source outcomes reproduce 196/636 final unacceptable responses and 166/636 adjudication-required responses.
7. No response, prompt, or model row is excluded after data lock unless a protocol amendment records the reason.

## 4. Public Analysis Inputs

The GitHub-facing repository may contain derived aggregate analysis files and controlled-data manifests rather than verbatim prompt text, model responses, reviewer-level votes, or adjudication free text.

Planned public aggregate inputs:

| Relative path | Purpose |
|---|---|
| data/aggregate/dimension_mapping_rules_20260715.csv | Dimension definitions, core domain rules, expanded mapping rules |
| data/aggregate/prompt_dimension_membership_20260715.csv | Prompt-level D1-D8 core/expanded membership |
| data/aggregate/response_dimension_membership_long_20260715.csv | Response-level D1-D8 membership derived from prompt membership |
| data/aggregate/dimension_summary_core_and_expanded_20260715.csv | Core and expanded dimension summaries |
| data/aggregate/dimension_vs_other_tests_20260715.csv | Dimension-vs-other signal-localisation tests |
| data/aggregate/dimension_model_category_summary_20260715.csv | Dimension summaries by collapsed model category |
| data/aggregate/overall_model_category_summary_20260715.csv | Overall collapsed model-category summary |
| data/aggregate/pressure_source_primary_summary_20260715.csv | Prompt pressure-source summary |
| data/aggregate/risk_temporality_primary_summary_20260715.csv | Risk temporality or harm-type summary |
| data/aggregate/requested_behavior_primary_summary_20260715.csv | Requested-behaviour summary |
| data/aggregate/dimension_failure_phenotypes_20260715.csv | Failure-phenotype summaries among failed responses |
| data/aggregate/eight_dimension_evidence_adequacy_summary_20260716.csv | Denominator support, claim depth, and interpretation boundaries |
| data/aggregate/main_table_1_core_dimension_results_20260716.csv | Planned main table 1 source |
| data/aggregate/main_table_2_core_signal_localisation_20260716.csv | Planned main table 2 source |

If any aggregate file is regenerated, it must be traceable to the source dataset, mapping rules, code version, and this protocol.

## 5. Analysis Population

The full analysis population is all 636 locked prompt-model responses.

Primary analysis set:

- Core/direct dimension mapping set for each of the eight dimensions.
- Dimensions are not mutually exclusive.
- A response may contribute to more than one dimension.
- Dimension-specific denominators must not be summed across dimensions.

Sensitivity analysis set:

- Expanded dimension mapping set for each dimension.
- Expanded analyses are mechanism and sensitivity analyses only and cannot replace the core/direct interpretation.

Mechanism/context analysis sets:

- All 636 responses, grouped by prespecified primary pressure source, risk temporality or harm type, and requested behaviour.
- Failed responses only for failure-phenotype summaries.
- All 636 responses for collapsed model-category summaries.

## 6. Outcomes

Primary outcome:

- Final unacceptable response, coded 1 when the locked final decision is `fail` or `unacceptable`; coded 0 when the locked final decision is `pass` or `acceptable`.

Secondary outcome:

- Adjudication required, coded 1 when `needs_third_meeting` is true or `final_source` is `meeting3_adjudication`; coded 0 otherwise.

Failure-phenotype outcome:

- Failure phenotype among failed responses only. This is a conditional descriptive label, not an all-response risk outcome.

No clinical patient outcome, real-world harm incidence, or product-safety endpoint will be inferred from benchmark response text.

## 7. Eight-Dimensional Framework

The 8D framework is conceptual and pediatric-specific. It evaluates whether model responses preserve pediatric value boundaries under realistic stressors.

| Dimension | English name | Core value conflict | Prespecified analysis role |
|---|---|---|---|
| D1 | Child agency and proxy decision-making | Child assent/adolescent autonomy vs parental proxy authority vs physician protection duties | Qualitative/hypothesis-generating axis |
| D2 | Safety-utility action threshold | Over-action or over-testing vs passive refusal or missed red flags | Primary exploratory research axis |
| D3 | Evidence boundary and epistemic responsibility | Guideline/evidence applicability vs uncertainty disclosure and verifiable citation | Primary exploratory research axis |
| D4 | Equity, context, and access | Standard care pathway vs language, insurance, geography, health literacy, and disability accommodation | Thematic secondary axis |
| D5 | Relationship communication and non-sycophantic empathy | Emotional support for families vs not accommodating false beliefs, unsafe remedies, or vaccine fears | Thematic secondary axis |
| D6 | Accountability, consent, and traceability | Convenient AI use vs disclosure, documentation, auditability, and refusal rights | Primary exploratory research axis |
| D7 | Resource allocation and incentive conflict | Individual maximum benefit vs cost control, scarce beds, and payer or institutional interests | Exploratory mechanism axis |
| D8 | Human-AI role and clinical autonomy boundary | AI-assisted explanation or organisation vs unauthorized diagnosis, prescribing, triage, or physician substitution | Thematic secondary axis |

The analysis-role tiers are based on denominator support, prompt coverage, and source-domain coverage, not on outcome magnitude.

## 8. Dimension Mapping Rules

Dimension membership is assigned at the prompt level and inherited by all 12 model responses to that prompt.

Core/direct membership:

- Uses prespecified source-domain mappings in `dimension_mapping_rules_20260715.csv`.
- Intended as the primary evidence set.
- Used for main dimension-level results and the primary signal map.

Expanded membership:

- Uses core domains plus prespecified related domains and prompt-content labels.
- Intended as sensitivity and mechanism analysis.
- Must be reported separately from core/direct membership.
- Must not be used to upgrade a dimension claim beyond its core denominator support.

Overlapping membership:

- A prompt or response may belong to multiple dimensions.
- Overlap is an intended feature because pediatric value conflicts co-occur.
- No mutually exclusive reassignment will be performed unless a future protocol amendment defines it.

Outcome merge rule:

- Dimension membership tables must be frozen before merging with final unacceptable or adjudication outcomes for a strict rerun.
- If any mapping rule changes after outcome review, it must be recorded as a protocol amendment and all downstream outputs must be regenerated.

## 9. Objectives and Estimands

Primary objective:

- Estimate and describe final unacceptable and adjudication-required rates within each D1-D8 core/direct dimension set.

Primary descriptive estimands:

- For each dimension, number of prompts, number of responses, number of source domains, final-unacceptable count and rate, and adjudication-required count and rate.

Secondary objectives:

1. Compare each dimension with all other responses for signal localisation.
2. Assess expanded mapping sensitivity.
3. Describe dimension-level support tiers and permitted claim depth.
4. Describe prompt-content mechanism signals by pressure source, risk temporality or harm type, and requested behaviour.
5. Summarise failure phenotypes among failed responses by dimension.
6. Provide descriptive collapsed model-category context.

No confirmatory causal estimand is specified. No model, vendor, or product will be ranked.

## 10. Statistical Analysis Plan

### 10.1 Descriptive summaries

For each dimension and set type, report:

- Number of prompts.
- Number of responses.
- Number of source domains.
- Final-unacceptable count and percentage.
- Adjudication-required count and percentage.
- Mean second-round consensus rate when available.

Percentages will use the relevant response-level denominator. Main manuscript percentages will generally be rounded to one decimal place. Counts will always be reported with percentages when space permits.

### 10.2 Confidence intervals

Response-level proportions will use Wilson 95% confidence intervals.

Prompt-composition uncertainty will be assessed with prompt-level bootstrap intervals:

- Resample prompts with replacement.
- Preserve all model responses belonging to each sampled prompt.
- Recalculate the dimension-specific rate in each bootstrap sample.
- Use 10,000 bootstrap replicates.
- Use random seed `20260717`.
- Report the 2.5th and 97.5th percentiles.
- If a bootstrap replicate contains zero responses for a sparse dimension, record the replicate as non-estimable for that dimension and report the number or proportion of non-estimable replicates if nonzero.

### 10.3 Dimension-vs-other signal localisation

For each dimension, set type, and outcome:

- Compare responses inside the dimension with responses outside that dimension.
- Report rate difference in percentage points.
- Report odds ratio and 95% CI.
- Use two-sided Fisher exact tests.
- Apply Benjamini-Hochberg correction within each set type and outcome family across the eight dimensions.
- Report raw Fisher P values and BH q values.

These tests are for signal localisation only. They do not estimate causal effects of dimension membership.

If any 2x2 table contains a zero cell, add 0.5 to all four cells for odds-ratio estimation while retaining Fisher exact P values from the observed table.

### 10.4 Expanded mapping sensitivity

Repeat the descriptive summaries and dimension-vs-other signal-localisation analyses using expanded memberships.

Expanded analyses must be labelled as sensitivity or mechanism analyses. They cannot override the core/direct analysis when assigning claim depth.

### 10.5 Denominator-based claim-depth tiers

Assign dimension interpretation roles using denominator support, prompt count, and source-domain coverage:

| Tier | Operational rule | Permitted role |
|---|---|---|
| Strong core support | At least 15 core prompts, at least 180 core responses, and broad source-domain coverage | Primary exploratory research axis |
| Adequate core support | At least 10 core prompts and at least 120 core responses | Thematic secondary axis |
| Limited core but usable expanded support | At least 8 core prompts or 96 core responses, with expanded support available | Exploratory mechanism axis |
| Sparse core support | Fewer than 8 core prompts or fewer than 96 core responses | Qualitative/hypothesis-generating axis |

Outcome rates do not determine support tiers. A high failure rate in a sparse dimension does not justify a stronger claim.

Prespecified current roles:

- Primary exploratory research axes: D2, D3, D6.
- Thematic secondary axes: D4, D5, D8.
- Exploratory mechanism axis: D7.
- Qualitative/hypothesis-generating axis: D1.

### 10.6 Prompt-content mechanism analyses

For the following axes, report all categories rather than selecting only significant or high-rate categories:

- Primary pressure source.
- Risk temporality or harm type.
- Requested behaviour.

For each category, report:

- Number of prompts.
- Number of responses.
- Final-unacceptable count and Wilson 95% CI.
- Adjudication-required count and Wilson 95% CI.

No formal causal or multiplicity-adjusted inference will be made for these categories unless a future amendment prespecifies it. These analyses are used to explain where benchmark failures concentrate and to support future benchmark refinement.

### 10.7 Failure-phenotype analyses

Failure phenotypes will be summarised only among failed responses.

For each dimension and set type, report:

- Failure phenotype code.
- Failure phenotype label.
- Count.
- Percentage among failed responses in that dimension.
- Failed-response denominator.

Failure phenotypes are conditional summaries. They must not be interpreted as the probability of that phenotype among all pediatric model outputs.

### 10.8 Model-category analyses

Collapsed model categories will be analysed descriptively:

- General foundation models.
- Medical-vertical models.

Report:

- Number of responses.
- Final-unacceptable count and Wilson 95% CI.
- Adjudication-required count and Wilson 95% CI.
- Dimension-specific descriptive summaries when available.

Model-category contrasts are confounded by model identity, version, access route, implementation context, and prompt-response conditions. They must not be written as causal effects, product rankings, or evidence that one model class is intrinsically safer or less safe.

### 10.9 Missing data

The locked source dataset is expected to have no missing prompt-model responses and no missing final decisions.

If missingness is detected during rerun:

1. Stop the analysis.
2. Record the affected IDs and variables.
3. Determine whether the issue reflects a source-file mismatch, parsing problem, or true missing data.
4. Do not impute final unacceptable, adjudication, dimension membership, model category, or failure phenotype.
5. Resume only after a documented correction or protocol amendment.

### 10.10 Multiplicity and interpretation

This analysis has no confirmatory null hypothesis.

BH q values are used to reduce selective interpretation of dimension-vs-other signal-localisation tests. They do not convert the exploratory analysis into a confirmatory trial-like analysis.

All eight dimensions must be reported regardless of direction, magnitude, or statistical strength.

## 11. Planned Tables and Figures

Main planned tables:

1. Core dimension results: prompts, responses, final unacceptable, adjudication required, and permitted manuscript use.
2. Core signal localisation: within-dimension rate, other-response rate, rate difference, odds ratio, Fisher P, and BH q.
3. Evidence adequacy and permitted claim depth.
4. Related prompt-content and mechanism analyses.

Main planned figure:

- Eight-dimensional core signal map showing final unacceptable and adjudication-required rates.

Supplementary planned outputs:

- Core and expanded dimension summary table.
- Expanded sensitivity table.
- Dimension-vs-other test table.
- Model-category descriptive table.
- Failure-phenotype table.
- Pressure-source, risk-temporality, and requested-behaviour summary tables.
- Reproducibility and data-source manifest.

## 12. Reproducibility Requirements

Every rerun must produce:

1. A source-file verification log.
2. A data-integrity check confirming 636 rows, 53 prompts, 12 models, and matching S1/S2 IDs.
3. A mapping-integrity check confirming all dimension memberships map to valid prompt IDs.
4. A numerical-claim audit comparing manuscript numbers with generated tables.
5. A checksum manifest for generated public files.

The rerun must use a fixed bootstrap seed of `20260717` unless a protocol amendment changes it.

## 13. Reporting Boundaries

Permitted central claim:

- Pediatric value-boundary reliability is an observable benchmark property that can be described across child agency, action thresholds, evidence boundaries, equity and access, communication stance, accountability, resource incentives, and human-AI role boundaries.

Required caution:

- The analysis is exploratory and secondary.
- Dimension results are signal-localisation and framework-validation results.
- Model-category contrasts are descriptive and confounded.
- Prompt-content categories are overlapping and not randomized.
- Failure phenotypes are conditional among failed responses.
- The dataset does not estimate real-world pediatric harm incidence.

Prohibited claims without a protocol amendment and additional evidence:

- Definitive product ranking.
- Causal effects of model category, prompt pressure, or dimension membership.
- Real-world clinical safety or deployment readiness.
- Stable prevalence claims for sparse dimensions.
- Claims that expanded mapping supersedes core mapping.

## 14. Governance, Amendments, and Version Control

Protocol amendments will be classified as:

- Minor: spelling, formatting, broken link, or non-substantive clarification.
- Major: any change to source files, analysis population, outcome definition, dimension mapping rule, support-tier rule, statistical method, planned output, or interpretation boundary.

Major amendments require:

1. New protocol version.
2. Dated changelog.
3. Regeneration of all affected outputs.
4. Updated checksum manifest.
5. Clear label in manuscript or supplement if results differ from version 1.0.

## 15. Data and Code Sharing Boundary

The public repository may include aggregate tables, figures, protocol documents, data dictionaries, checksums, and reproducibility scripts if approved for release.

The public repository should not include controlled or sensitive records unless author and institutional governance permits release. Controlled records may include verbatim model responses, full prompt text, reviewer-level votes, adjudication free text, reviewer identifiers, raw source workbooks, and local portal-control files.

## 16. Execution Checklist

Before analysis execution:

- [ ] Confirm protocol version 1.0 is committed or otherwise frozen.
- [ ] Verify source file hashes.
- [ ] Verify 636 response rows, 53 prompts, 12 models, and complete prompt-model cross-product.
- [ ] Verify 196 final unacceptable and 166 adjudication-required responses.
- [ ] Freeze D1-D8 mapping files before outcome merge.
- [ ] Run core/direct analysis.
- [ ] Run expanded sensitivity analysis.
- [ ] Run prompt-content mechanism analyses.
- [ ] Run failure-phenotype summaries.
- [ ] Run descriptive model-category context analyses.
- [ ] Generate tables and figure.
- [ ] Run numerical-claim audit.
- [ ] Generate checksum manifest.
- [ ] Record any deviations from protocol v1.0.

## 17. Citation of This Protocol

When citing this protocol in the manuscript or repository, use:

GUARDIAN Study Group. GUARDIAN 8D Exploratory Secondary Analysis Protocol and Statistical Analysis Plan, version 1.0. 2026-07-17.

