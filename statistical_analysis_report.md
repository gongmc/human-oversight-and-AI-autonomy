# PRISMA Extraction and Statistical Analysis Report

Generated: 16 July 2026.

## Data Basis

This report uses the adjudicated title/abstract screening corpus for the Pediatric VIM Atlas. It follows PRISMA-style accounting for identified, screened, excluded, contextual, and core evidence records. Extraction is abstract-level unless a PDF status is explicitly recorded in the high-relevance PDF manifest.

## PRISMA-Style Flow

- Records identified from PubMed/MEDLINE axis searches: 2,770.
- Additional concept-anchor records: 2.
- Records screened at title/abstract level: 2,772.
- Excluded after adjudicated title/abstract screening: 867.
- Contextual evidence retained: 1,373.
- Core evidence included in synthesis: 532.
- Core direct pediatric evidence: 170.
- Core foundational transferable evidence: 362.
- Records requiring third-reviewer adjudication: 1,401.

## Core Evidence Profile

### By Design
- benchmark_or_model_evaluation: 298
- randomized_trial: 65
- systematic_review_or_meta_analysis: 44
- implementation_or_workflow_study: 41
- other_or_unclear: 30
- observational_or_cross_sectional: 23
- framework_guideline_policy: 17
- qualitative_or_survey: 13
- viewpoint_or_commentary: 1

### By Pediatric VIM Axis
- 公平、社会处境与可及性: 428/532 (80.5%)
- 证据边界与认识论责任: 279/532 (52.4%)
- 安全-效用阈值与升级决策: 263/532 (49.4%)
- 同意、隐私、责任与可追溯: 243/532 (45.7%)
- 人机角色边界与临床自主权: 194/532 (36.5%)
- 沟通、共情与非迎合边界: 157/532 (29.5%)
- 资源配置、家庭负担与激励冲突: 138/532 (25.9%)
- 儿童/青少年主体性、代理决策与保密: 74/532 (13.9%)

## Statistically Supported Findings

- LLM/生成式AI信号: core pediatric 31/170 (18.2%) vs foundational 295/362 (81.5%), FDR-adjusted p=2.73e-43.
- 公平、社会处境与可及性: core pediatric 103/170 (60.6%) vs foundational 325/362 (89.8%), FDR-adjusted p=1.34e-14.
- 摘要报告定量统计: core pediatric 133/170 (78.2%) vs foundational 160/362 (44.2%), FDR-adjusted p=6.77e-13.
- 同意、隐私、责任与可追溯: core pediatric 44/170 (25.9%) vs foundational 199/362 (55.0%), FDR-adjusted p=9.25e-10.
- 证据边界与认识论责任: core pediatric 56/170 (32.9%) vs foundational 223/362 (61.6%), FDR-adjusted p=1.48e-09.
- 沟通、共情与非迎合边界: core pediatric 23/170 (13.5%) vs foundational 134/362 (37.0%), FDR-adjusted p=5.59e-08.
- 框架/综述/指南信号: core pediatric 56/170 (32.9%) vs foundational 210/362 (58.0%), FDR-adjusted p=1.09e-07.
- 人机角色边界与临床自主权: core pediatric 37/170 (21.8%) vs foundational 157/362 (43.4%), FDR-adjusted p=1.9e-06.
- 安全-效用阈值与升级决策: core pediatric 66/170 (38.8%) vs foundational 197/362 (54.4%), FDR-adjusted p=0.00097.
- 儿童/青少年主体性、代理决策与保密: core pediatric 33/170 (19.4%) vs foundational 41/362 (11.3%), FDR-adjusted p=0.0132.

## Meta-Analysis Feasibility

- Can a conventional clinical-effect meta-analysis be performed across all 532 core records? No: The corpus mixes pediatric AI applications, adult transferable LLM benchmarks, governance frameworks, observational studies, trials, reviews, and commentaries; PICO, outcomes, comparators, and effect measures are not commensurable.
- Can model-performance metrics be pooled? Not valid at corpus level: AUC, accuracy, sensitivity, specificity, hallucination, unsafe advice, usability, workflow, and governance outcomes refer to different tasks and denominators.
- What quantitative synthesis was performed? Random-effects meta-analysis of evidence-map proportions: Publication-year strata were used to estimate pooled proportions of evidence classes and VIM dimensions among core records; this is a structural evidence meta-analysis, not a pooled clinical treatment or diagnostic accuracy estimate.

## Random-Effects Meta-Analysis of Evidence Proportions

The following analyses pool year-stratified proportions using a DerSimonian-Laird random-effects model on logit-transformed proportions. These are evidence-structure meta-analyses, not pooled clinical efficacy or diagnostic accuracy estimates.

- 核心证据中直接儿科证据比例: pooled random-effects proportion 42.7% (95% CI 28.6-58.2); I2=87.5%.
- 核心证据中LLM/生成式AI比例: pooled random-effects proportion 49.5% (95% CI 32.1-67.1); I2=89.6%.
- 核心证据中摘要报告定量统计比例: pooled random-effects proportion 55.1% (95% CI 50.1-60.0); I2=15.6%.
- 儿童/青少年主体性、代理决策与保密: pooled random-effects proportion 14.4% (95% CI 11.6-17.7); I2=0.0%.
- 安全-效用阈值与升级决策: pooled random-effects proportion 49.4% (95% CI 42.9-56.0); I2=44.0%.
- 证据边界与认识论责任: pooled random-effects proportion 48.7% (95% CI 36.4-61.2); I2=84.1%.
- 公平、社会处境与可及性: pooled random-effects proportion 78.6% (95% CI 71.9-84.1); I2=55.3%.
- 沟通、共情与非迎合边界: pooled random-effects proportion 30.1% (95% CI 25.1-35.6); I2=31.1%.
- 同意、隐私、责任与可追溯: pooled random-effects proportion 45.7% (95% CI 41.3-50.2); I2=5.0%.
- 资源配置、家庭负担与激励冲突: pooled random-effects proportion 26.7% (95% CI 21.5-32.8); I2=41.4%.
- 人机角色边界与临床自主权: pooled random-effects proportion 35.9% (95% CI 30.2-42.0); I2=38.8%.

## Interpretation

The quantitative evidence base supports three high-level findings: first, the direct pediatric medical AI value-boundary literature remains a minority of the core evidence base; second, transferable LLM and broader clinical AI evaluation literature supplies most of the operational measurement machinery; third, equity/context/access, evidence boundaries, safety thresholds, accountability, and human-AI role boundaries dominate the mapped evidence, whereas child agency and resource/incentive conflicts are comparatively underdeveloped.

## Limitations

The extraction is based on title/abstract records and available PDF manifest status. Because outcomes, populations, tasks, and effect measures are heterogeneous, a conventional pooled clinical effect-size meta-analysis is not appropriate at this stage. Full-text extraction and risk-of-bias appraisal remain required before a journal-declared systematic review can claim definitive pooled clinical effects.
