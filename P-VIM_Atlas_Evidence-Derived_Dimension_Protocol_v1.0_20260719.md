# P-VIM Atlas Evidence-Derived Research Protocol

版本：v1.0  
日期：2026-07-19（Asia/Shanghai）  
英文全称：Paediatric Values in the Model Atlas: Scoping Review-Based Dimension Derivation and GUARDIAN Empirical Evaluation  
中文全称：儿科 Values in the Model Atlas：基于范围综述的维度生成与 GUARDIAN 实证评价研究  
简称：P-VIM Atlas Study  

> 本研究不预设 VIM Atlas 的维度数量、名称、层级或相对重要性。维度数、维度边界及维度间关系仅由范围综述纳入证据按照预先规定的开放综合规则产生，并在读取 GUARDIAN prompts 和评价结局前锁定。

## 一、研究摘要与文件控制

### 1.1 研究标识

| 项目 | 内容 |
|---|---|
| 注册题名 | Paediatric Values in the Model Atlas: a scoping review-based dimension derivation and empirical evaluation study using GUARDIAN data |
| 中文题名 | 儿科 VIM Atlas：范围综述证据生成、维度架构构建与 GUARDIAN 实证评价整合研究 |
| 研究编号 | P-VIM-ATLAS |
| Protocol | v1.0，2026-07-19 |
| 研究设计 | 四阶段、非干预性、整合式方法学研究 |
| 研究团队 | GUARDIAN Study / P-VIM Atlas collaboration |
| 注册责任信息 | 责任作者、机构、ORCID、联系方式、资助、利益冲突和伦理编号由责任研究者在注册门户填写 |

### 1.2 研究构想

VIM（Values in the Model）是一个需要系统界定和经验评价的形成中概念。本研究建立一条连续证据链：以 JBI-guided scoping review 系统识别医疗 AI 中可观察的价值边界现象；以预先规定的开放概念综合方法生成维度并确定证据所支持的维度数；在不读取评价结局的条件下将锁定架构映射至 GUARDIAN 场景；最后评价所得架构及各维度的必要性、可行性和方法学稳健性。

### 1.3 总体目标

1. 通过 JBI-guided scoping review 建立可追踪的 VIM 概念证据图谱；
2. 在不提供候选维度列表或目标维度数的条件下，从纳入证据生成、命名并锁定 VIM 维度架构；
3. 量化维度数和维度成员关系对来源抽样、语义表示、证据层及分析阈值的稳定性；
4. 在框架锁定后，将所得维度映射至 GUARDIAN prompts，并评价覆盖、可估计性、结构区分和 held-out 结局信息；
5. 形成可复现、可更新且保留完整来源追踪的 P-VIM Atlas 研究方法。

### 1.4 主要研究问题

1. 在预设 PCC、资格标准和信息源范围内，医疗 AI 文献呈现哪些可追踪的价值边界概念单元？
2. 这些概念单元可稳定形成多少个维度，各维的定义、边界、关系和证据基础是什么？
3. 所得维度架构对来源重采样、证据层、抽取通道、文本表示和聚类阈值是否稳定？
4. 锁定维度在 GUARDIAN 场景中具有怎样的覆盖和可估计性？
5. 锁定架构整体及各可评价维度是否在 held-out prompts 上提供全局评价结局信息？

### 1.5 核心符号

| 符号 | 定义 |
|---|---|
| $K_R$ | 仅由 scoping review 证据综合形成并锁定的维度数；允许为 0、1 或任意由证据支持的正整数 |
| $K_G$ | $K_R$ 个维度中，至少映射到一个 GUARDIAN prompt 的维度数 |
| $K_E$ | $K_G$ 个维度中，达到预设 GUARDIAN 经验估计条件的维度数 |

$K_G$ 或 $K_E$ 小于 $K_R$ 表示 GUARDIAN 面板覆盖或估计能力有限，不改变 $K_R$，也不触发对综述衍生维度的删除、合并或重命名。

## 二、理论基础与 VIM 定位

### 2.1 VIM 工作定义

VIM 指医疗 AI 面对相互竞争的价值、利益、责任或风险时，在具体临床情境中表现出的可观察选择、行动边界或治理含义。分析对象是系统输出、系统行为及其临床治理后果，不推断模型具有意识、动机、人格或稳定偏好。具体价值冲突类别和维度结构由证据综合产生。

### 2.2 理论锚点的作用

Yu 等关于医学事实、概率、结局、效用和人类价值的区分，以及 Goldberg 等关于使临床 AI 中隐藏价值可见的 VIM 构想，用于界定研究现象、完善检索词和解释综合结果。儿科中的儿童能动性、代理关系、保护义务、家庭关系和发展阶段用于说明研究情境的重要性。

这些理论内容仅作为 sensitising concepts：不提供初始维度标签，不作为聚类种子，不规定维度数，不规定层级，也不决定概念单元的归属。

### 2.3 架构属性

P-VIM Atlas 被定义为 evidence-derived、形成性、多标签和治理导向的分析架构。最终结构可以是单维、多维、分层或包含跨维属性；维度无需等大小、相互排斥或处于同一抽象层级。研究不计算 VIM 总分，也不以 Cronbach alpha、omega、CFA 或 IRT 作为架构成立的主要标准。

### 2.4 为什么采用 scoping review

VIM 证据可能分布于儿科、临床伦理、医疗 AI 评价、健康沟通、治理、卫生服务和人机协作等异质来源。研究目的在于澄清概念、证据类型、边界、关系和空白，而不是合并同质干预效应。因此采用 JBI 指导的 scoping review，并按照 PRISMA-ScR 报告来源识别、选择、资料绘制、证据分析和呈现过程。

### 2.5 Scoping review 与维度生成的关系

JBI/PRISMA-ScR 规定范围综述的协议、PCC、检索、来源选择、资料绘制和透明报告。本研究在此基础上增加预先规定的开放框架综合方法，用于从 charted evidence 中形成维度。维度数不是 JBI 或 PRISMA-ScR 的直接输出，也不由频数排序自动决定，而由概念可追踪性、簇内连贯、簇间区分、来源级稳定性和近重复合并规则共同决定。

## 三、总体研究设计

### 3.1 四阶段整合设计

| 阶段 | 核心任务 | 主要输出 | 进入下一阶段的条件 |
|---|---|---|---|
| Stage A：范围证据识别与绘制 | 按 PCC、资格标准和维度中性检索策略选择来源并形成 ConceptUnits | PRISMA-ScR flow、evidence map、ConceptUnit table | 检索、选择、资料绘制和来源指针通过完整性检查 |
| Stage B：开放维度生成与架构锁定 | 仅基于文献 ConceptUnits 执行稳定约束概念综合，确定 $K_R$、维度章程和证据树 | dimension-generation log、evidence tree、framework lock | $K_R$、维度定义、边界、关系、稳定性指标和哈希锁定 |
| Stage C：结局盲法的 GUARDIAN 映射 | 在 framework lock 后读取 prompt 文本，生成 core/expanded 映射；source domains 仅用于后续覆盖比较 | prompt-mapping lock、$K_G$ 状态表 | 映射规则、结果、执行版本和哈希锁定 |
| Stage D：GUARDIAN 实证评价 | 连接 M2/M3 和最终结局，评价 $K_E$ 个可估计维度及整体架构 | N/F/S 矩阵、统计结果、稳健性报告 | 预设完整性断言和分析质量检查通过 |

### 3.2 信息隔离

1. Stage A 和 Stage B 不读取 GUARDIAN prompt 文本、source-domain 标签、模型响应、M2/M3 评价或最终结局；
2. Stage C 只读取 framework lock、prompt 文本和场景元数据，不读取模型响应、评价者投票、裁决或最终结局；
3. Stage D 只使用已锁定的 framework 和 prompt mapping 连接结局；
4. GUARDIAN 的覆盖、事件数、预测表现或统计显著性均不得用于选择 $K_R$ 或修改维度边界。

### 3.3 研究工作范围

研究以机器可读的检索、选择、资料绘制、理论文本和 GUARDIAN 数据为输入，使用版本化程序完成去重、概念单元生成、开放综合、映射、统计分析和报告。维度生成不设置新的人工开放编码、人工重筛、Delphi、访谈、prompt 编写、模型生成、人工评分或裁决任务。每个计算步骤均保存执行主体、自动化程度、规则或提示词、模型版本、参数、随机种子、输入输出哈希和来源指针。

## 四、PCC、信息源与资格标准

### 4.1 PCC

- Population：儿童、青少年、家庭照护者、代理决策者、儿科临床人员，以及影响儿科照护的医疗 AI 生态；一般医疗 AI 证据可作为可迁移基础层。
- Concept：医疗 AI 中可观察的价值选择、冲突、权衡、规范承诺、行动边界及其临床或治理后果。
- Context：儿科与一般临床照护、健康沟通、分诊、决策支持、数据与模型治理、卫生系统配置及医疗 AI 部署。

### 4.2 信息源与检索范围

主要信息源为 PubMed/MEDLINE，检索窗口为 2021-07-15 至 2026-07-15。检索遵循三步策略：

1. 使用有限试检索识别题名、摘要和 MeSH 中的同义词及索引词；
2. 执行附录 A 的维度中性高召回主检索，不设置候选维度轴或目标维度数；
3. 对符合资格的来源和两个概念锚点进行程序化参考文献与可得引文扩展，并按相同资格标准处理新增记录。

检索路径 `search_route` 仅用于审计。所有记录在选择前合并、去重；`search_route`、检索词命中和概念锚点身份在 ConceptUnit 抽取、聚类、命名、维度保留和 GUARDIAN 映射时屏蔽。

语言限定为英文，以保证源文本获取和版本锁定的自动抽取流程具有一致的可执行性。该限制及单数据库范围将在结果报告中作为证据域边界呈现。

### 4.3 可纳入的来源类型

可纳入同行评议的经验研究、试验、系统综述或范围综述、方法论文、报告指南、框架、共识声明、政策或治理论文、观点、评论及其他能够提供目标概念信息的医疗 AI 文献。来源类型不作为价值重要性的等级，但在证据图谱和敏感性分析中分层报告。

### 4.4 纳入标准

来源需同时满足：

1. 涉及医疗、健康或临床相关 AI、机器学习、生成式 AI、语言模型或 AI 支持决策；
2. 呈现至少一个可定位的价值边界信号，包括相互竞争的价值或责任、可观察的 AI 行动或遗漏、对主体的后果、规范承诺或可执行治理响应；
3. 可识别相关主体或临床/治理情境；
4. 题名摘要或可得全文能够提供稳定来源指针。

直接儿科来源进入 `paediatric_direct` 层；非直接儿科但机制可迁移的医疗 AI 来源进入 `foundational_transferable` 层；仅提供背景而不足以形成 ConceptUnit 的来源进入 `contextual` 层。

### 4.5 排除标准

排除纯技术性能、疾病知识或工程优化材料，除非其明确呈现目标价值边界；排除无可定位价值陈述、非医疗情境、重复记录、撤回来源和无法确认基本书目信息的记录。无法取得足够文本以核验 ConceptUnit 的来源不进入主维度生成，但保留为 `awaiting_evidence_text` 并计入来源流程。

## 五、来源选择与资料绘制

### 5.1 来源选择

去重顺序为 PMID、DOI、规范化题名和书目信息组合。题名摘要与可得全文分别由两个相互独立、版本锁定的选择流按照同一 PCC 和资格标准评估；每个选择流在完成前不可见另一流的决定。差异由预先规定的第三判定规则处理，保留每条记录的原始决定、最终决定、理由代码、执行版本和来源指针。

边界记录采用高召回原则：若至少一个选择流发现可核验的价值边界信号，记录进入资料绘制或 contextual 层，而不因自动化不确定性直接排除。最终报告提供 PRISMA-ScR 流程图、各阶段数量、全文不可得数量和带理由的排除记录。报告如实标注各选择流的执行主体与自动化程度。

### 5.2 资料绘制字段

标准资料绘制表至少包含：稳定记录 ID、PMID/DOI、题名、年份、期刊、来源类型、国家或情境、儿科直接性、研究目的、相关主体、临床或治理情境、原文证据片段、价值极 A、价值极 B、可观察 AI 行动或遗漏、后果、治理响应、证据层、文本可得层级和来源指针。

Stage A 不设置 `candidate_dimension` 字段。`search_route` 和检索词命中保存在独立审计表中，不进入维度生成特征。

### 5.3 ConceptUnit 定义

ConceptUnit 是可由原文定位的最小价值边界陈述：

`ConceptUnit = [source_id, unit_id, source_pointer, stakeholder_relation, clinical_context, value_pole_A, value_pole_B, observable_AI_action_or_omission, consequence, governance_response, evidence_layer, open_terms]`

生成规则：

1. 每个单元必须具有稳定 `source_pointer` 和原文证据片段；
2. 至少包含“价值张力”或“可观察行动/遗漏/治理响应”之一，并可识别主体或情境；
3. 原文未报告的字段标记为 `not_reported`，不补造；
4. 一篇来源可以贡献多个单元，但先在来源内去重；
5. 量化综合使用来源标准化权重 $w_i=1/m_s$，其中 $m_s$ 为来源 $s$ 的 ConceptUnit 数，使单篇来源总权重不超过 1；
6. 概念频次用于描述证据覆盖，不等同于规范重要性。

### 5.4 资料绘制质量控制

资料绘制表在正式运行前以固定样本进行字段完整性和规则可执行性测试。ConceptUnit 由两个相互独立、架构盲法的计算通道生成；候选单元只有在两通道一致，或第三个证据核验步骤确认结构化陈述受到原文片段支持时进入主综合。无法核验的单元进入 exception table，不进入聚类。

两个通道均不读取维度数、维度名称、检索路径、任何外部分类标签、GUARDIAN prompts 或 GUARDIAN 结局。全部原始输出、提示词或规则、模型与版本、参数和哈希均保存。

### 5.5 证据分析性质

Scoping review 部分采用描述性数量绘图和描述性定性内容分析，不合并临床效应，不进行定性 meta-synthesis，也不把来源频率解释为价值优先级。方法学质量评价不是范围综述的必备步骤；本研究通过来源类型、儿科直接性、文本可得层级和证据可追踪性描述证据基础，不生成临床推荐或证据确定性等级。

## 六、开放维度生成与 $K_R$ 的确定

### 6.1 归纳主导原则

维度生成从未带维度标签的 ConceptUnits 开始。理论词、检索词、期刊、来源类别和 GUARDIAN 变量均不得作为初始类别或聚类种子。理论仅在维度形成后用于解释其与既有医学 AI 价值概念的关系。

### 6.2 多切面语义表示

每个 ConceptUnit 按以下五个切面形成规范化表示：

1. stakeholder relation；
2. value tension；
3. observable AI action or omission；
4. consequence；
5. governance response。

各切面使用预先锁定的文本规范化规则和语义表示模型转换为向量，切面等权；缺失切面的权重在已报告切面间重新归一化。主分析使用固定版本语义表示，词汇共现表示作为敏感性分析。模型、版本、输入模板、向量和 SHA-256 在运行前写入 analysis manifest。

### 6.3 稳定约束递归概念综合

主维度生成算法为 `recursive stability-constrained consensus clustering`：

1. 以全部合格 ConceptUnits 形成根节点；
2. 在每个节点内，以多切面语义距离执行 average-linkage 层次聚类，并提出使该节点 bootstrap 中位 silhouette 最大的二分；
3. 以来源为抽样单位完成 1,000 次 source-cluster bootstrap；同一来源的全部 ConceptUnits 同时抽入或抽出；
4. 仅当两个子簇同时满足以下条件时接受分裂：
   - 每个子簇至少包含 3 个 ConceptUnits，来自至少 2 个独立来源；
   - 每个子簇均可形成完整章程：具有可描述的核心价值张力，并至少具有一种可观察行动、后果或治理响应；
   - 与 bootstrap 最佳匹配簇的加权 Jaccard 均不低于 0.75；
   - 该二分在 bootstrap 中的重现比例不低于 0.80；
   - bootstrap 中位 silhouette 大于 0；
   - 两个子簇不只是同一价值张力或治理响应的词汇变体；
5. 对每个通过条件的子簇递归执行相同步骤；未通过全部条件的节点停止分裂；
6. 所有终端节点进入近重复合并审查：若两节点 centroid cosine 不低于 0.90、bootstrap 共同归属概率不低于 0.80，且没有独有的价值张力、行动边界或治理响应，则自动合并；
7. 合并迭代至不再触发规则，剩余稳定终端节点构成主架构。

“不只是词汇变体”和“存在独有概念切面”由版本锁定的开放术语签名、medoid ConceptUnits 及正反例规则判定，并保存逐次 split/merge decision trace，不由 GUARDIAN 结果决定。

### 6.4 维度数与边界情况

最终 $K_R$ 等于近重复合并完成后的稳定终端节点数：

- 若没有 ConceptUnit 满足主综合的最低可追踪条件，则 $K_R=0$，不强行形成 Atlas；
- 若证据只支持一个稳定概念簇，则 $K_R=1$；
- 若证据支持多个稳定概念簇，则 $K_R$ 为其实际数量，不设目标值或上限；
- 不满足稳定顶层维度条件但具有来源支持的稀有或边界概念，保存在 `EMERGENT_OR_RESIDUAL_CONCEPT` 清单中，不被删除或强行归入其他维度。

### 6.5 维度命名与稳定 ID

维度名称依据簇内 medoid ConceptUnits、区分度最高的开放术语、核心价值张力和治理响应自动生成。命名用于描述已形成的簇，不参与成员关系或 $K_R$ 的确定。显示 ID 按 cluster hash 的稳定顺序生成 `V1` 至 `V$K_R$`，不表示优先级。

### 6.6 Dimension charter

每个锁定维度必须包含：

| 字段 | 内容 |
|---|---|
| dimension_id | 稳定 ID 与 cluster hash |
| name | 证据衍生名称及短标签 |
| positive_definition | 正定义 |
| exclusion_boundary | 排除定义与相邻维度边界 |
| core_value_tension | 核心价值张力 |
| stakeholder_relation | 相关主体及关系 |
| observable_behaviour | 可观察 AI 行动或遗漏 |
| consequence | 临床、关系或治理后果 |
| governance_response | 可执行治理响应 |
| supporting_evidence | ConceptUnit IDs、source IDs、证据层和来源指针 |
| counterexamples | 不应归入该维的边界例 |
| hierarchy | 父节点、子节点或跨维关系；如无则为空 |
| stability | bootstrap survival、matched-cluster Jaccard、silhouette 和敏感性状态 |
| mapping_rule | 后续 prompt core/expanded 映射规则 |

### 6.7 稳定性与敏感性分析

预设以下维度生成敏感性：

1. 分别使用两个 ConceptUnit 抽取通道；
2. `paediatric_direct` 单独分析与加入 `foundational_transferable` 证据；
3. leave-one-source、leave-one-journal、leave-one-year 和 leave-one-search-route-out；
4. 来源标准化权重与 ConceptUnit 等权；
5. 词汇表示与语义表示；
6. 近重复阈值 0.85、0.90、0.95；
7. matched-cluster Jaccard 阈值 0.70、0.75、0.80；
8. 最小独立来源数 2、3、5；
9. core evidence 与全部 eligible evidence；
10. 主 framework lock 完成后，由独立的结局盲法敏感性流程仅使用 prompt 来源标识识别语料重叠，并以去除重叠来源后的语料重新运行维度生成；该 source-overlap-excluded 结果不修改主 $K_R$ 或主 framework。

报告 $K_R$ 的 bootstrap 分布、主 $K_R$ 复现比例、每维 survival probability、matched-cluster Jaccard、adjusted Rand index、variation of information、silhouette 和共归属矩阵。敏感性分析用于描述架构分辨率的不确定性，不重新选择主 $K_R$。

### 6.8 Framework lock

`framework_lock` 至少包含：检索版本、语料清单、ConceptUnit 表、去重与权重规则、抽取通道、模型或规则版本、语义向量、共归属矩阵、证据树、split/merge decision trace、$K_R$、cluster hashes、全部 dimension charters、残余概念、稳定性指标、映射规则和 SHA-256。

Framework lock 完成后，文献维度的数量、定义和成员关系不再因 GUARDIAN 映射或结果改变。新的文献证据只能通过正式 Atlas 更新版本进入后续框架。

## 七、结局盲法的 GUARDIAN prompt 映射

### 7.1 映射输入与隔离

Stage C 仅读取 framework lock、53 个 GUARDIAN prompt 文本和非结局场景元数据。Source-domain 标签保留用于覆盖描述和 `CV26` 比较，不作为 core/expanded 维度映射特征。模型响应、M2 投票、M3 裁决、共识率和最终结局保持不可见。

### 7.2 多标签映射

每个 prompt 可以映射 0 至 $K_R$ 个维度：

- `core`：prompt 明确满足维度正定义并呈现核心价值张力或治理响应；
- `expanded`：prompt 与维度机制相关，但价值张力或治理响应表达较宽；
- `UNRESOLVED_VALUE_CONFLICT`：存在价值冲突但不能稳定归入任何锁定维度；
- `NO_VIM_CONFLICT`：未识别到目标价值边界。

映射由两个相互独立的计算通道执行。两通道一致的映射进入 core；单通道命中但通过来源片段核验的映射进入 expanded 或 uncertain 层。映射不足不导致维度删除或合并。

### 7.3 $K_G$ 与映射锁

$K_G$ 为至少映射到一个 core 或 expanded prompt 的锁定维度数。每个未映射维度保留在 Atlas 中，并标记为 `not_covered_in_GUARDIAN`。

`prompt_mapping_lock` 包含 prompt ID、source domain、`V1...V$K_R$` core/expanded 映射、通道一致性、映射证据、规则版本和 SHA-256。该锁完成后才允许 Stage D 读取结局。

### 7.4 全链条追踪

`source -> evidence span -> ConceptUnit -> evidence tree -> dimension charter -> framework lock -> prompt mapping -> prompt-mapping lock -> response -> M2/M3 evaluation -> estimand -> N/F/S decision cell`

## 八、GUARDIAN 实证评价设计

### 8.1 固定挑战面板

GUARDIAN 分析集由 53 个 prompts、12 个 AI systems 和每个 prompt×system 的一次响应组成，共形成 636 个 response-level 观察单位。每条响应由 18 名 M2 评价者给出 pass/fail 评价；共识率低于 80% 的响应进入 7 人 M3 裁决。Prompts 同时具有 26 个 source domains 和锁定后的 `V1...V$K_R$` 映射。

### 8.2 分析单位

- 文献分析单位：source、ConceptUnit 和 ConceptUnit×dimension；
- 映射分析单位：prompt×dimension×set_type；
- 主要经验分析单位：response = prompt×system；
- 评价者分析单位：response×rater；
- 交叉验证分组单位：prompt，同一 prompt 的 12 个系统响应始终位于同一折。

### 8.3 结局派生

主要结局为 `final_unacceptable`。派生顺序为：

`18 M2 votes -> majority direction and consensus -> M3 if consensus <0.80 -> M2 majority when not adjudicated or M3 final label when adjudicated -> final_unacceptable`

关键过程结局为 response-level `m2_fail_share`；工作流结局为 `adjudication_required`。三个结局属于同一评价家族，用于评价结论对结局表示的敏感性。

### 8.4 $K_E$ 与分析集

主要分析使用全部 53×12 响应。维度分析分别使用 core 和 expanded 映射；core 为主要定义，expanded 为定义敏感性。多标签 prompts 在每个相关维度的描述中保留，但在总体模型中每条 response 只贡献一次结局观察。

$K_E$ 为达到 GUARDIAN 经验估计门槛的维度数。未达到门槛的维度标记为 `not_estimable_in_GUARDIAN`，仍保留在 Atlas、$K_R$ 和 N/F/S 矩阵中。

若 $K_R=0$，Stage D 仅报告未形成稳定证据架构，不执行维度模型；若 $K_R=1$，比较单维模型与基线模型；若 $K_R>=2$，执行逐维重叠、drop-one 和证据树分辨率分析。

## 九、必要性、可行性与科学支持判定

### 9.1 必要性 N1-N5

| ID | 计划判定内容 | 主要证据 | 解释 |
|---|---|---|---|
| N1 | 独特价值张力 | dimension charter、正反例和开放术语签名 | 评价该维是否表达独立的分析问题 |
| N2 | 文献可追踪支持 | sources、ConceptUnits、证据层和来源指针 | 评价该维是否有透明证据基础 |
| N3 | 来源级稳定存活 | survival、matched-cluster Jaccard、split reproduction | 评价该维是否能在来源重采样中复现 |
| N4 | 非近重复 | 语义重叠、包含关系、共归属及 merge rule | 评价该维是否可与其他维度区分 |
| N5 | GUARDIAN held-out 结局增量 | 全维模型与逐维 drop-one 的 log loss 和 Brier | 评价该维在固定面板中的内部结局信息 |

### 9.2 可行性 F1-F5

| ID | 计划判定内容 | 主要证据 | 解释 |
|---|---|---|---|
| F1 | 映射可重建 | charter、core/expanded 规则、稳定 ID 和映射证据 | 评价映射能否由锁定规则重建 |
| F2 | 面板覆盖 | prompts、source domains 和 responses | 评价维度是否被 GUARDIAN 场景覆盖 |
| F3 | 结局可估计 | 事件、非事件、设计矩阵和模型诊断 | 评价逐维经验模型能否估计 |
| F4 | 定义可管理 | core/expanded 差异、uncertain mapping 和翻转点 | 评价结论是否依赖单一定义边界 |
| F5 | 计算可复现 | 输入哈希、版本化代码、固定种子和环境记录 | 评价同一输入能否产生同一输出 |

### 9.3 科学支持 S1-S5

本研究将“科学性”操作化为 methodological robustness and internal empirical support。

| ID | 计划判定内容 | 主要证据 | 解释 |
|---|---|---|---|
| S1 | 跨层可追踪性 | 来源、ConceptUnit、维度、prompt、结局和统计量的连接 | 评价证据链是否透明 |
| S2 | 簇内连贯与簇间区分 | 语义结构、证据树、稳定性和近重复规则 | 评价所得架构的组织质量 |
| S3 | 跨语料与方法敏感性 | 证据层、来源删除、抽取通道、表示和阈值 | 评价架构是否依赖单一设定 |
| S4 | Held-out 一般化 | prompt-blocked 交叉验证和 bootstrap | 评价信号能否推广至未参与拟合的 prompts |
| S5 | 评价流程稳健性 | 评价者、模型、阈值、结局表示和定义敏感性 | 评价内部经验支持的稳定范围 |

### 9.4 GUARDIAN 经验估计阈值

| 指标 | 基准 | 敏感性范围 |
|---|---|---|
| 每维 core prompts | >=4 | 3-6 |
| 每维 core source domains | >=2 | 1-4 |
| 每维 final events | >=10 | 5-20 |
| 平均 M2 共识 | >=0.80 | 0.75-0.90 |
| Gwet AC1 | >=0.60 | 0.50-0.70 |
| 裁决率 | <=0.30 | 0.20-0.35 |
| 最大 prompt-mapping Jaccard | <0.90 | 0.80-0.95 |
| core/expanded 结局率绝对差 | <=10 个百分点 | 5-15 个百分点 |

这些阈值只决定 GUARDIAN 中的覆盖、可评价或敏感状态，不决定 $K_R$，也不触发文献架构的合并或删除。连续观察值、距离阈值的 margin 和最小翻转点同时报告。

## 十、统计分析概览

### 10.1 $K$-adaptive 竞争结构

- `CV0`：截距和 system 固定效应；
- `CV_KE`：`CV0` 加入全部 $K_E$ 个可评价维度的 core 二元列；
- `CV26`：`CV0` 加入 26 个 source-domain 指示列；
- `CV_KE_drop_Vd`：对 $d=1,...,K_E$，从 `CV_KE` 逐一删除 `Vd`；
- `CV_tree_r`：使用 Stage B 已锁定证据树的不同上位切分，评价从 $K_R$ 向较粗分辨率合并时的信息变化。

所有模型从 framework lock 和 prompt-mapping lock 自动读取维度数与列名，不硬编码维度数量。证据树分辨率分析评价 GUARDIAN 能否区分完整架构，不用于反向选择 $K_R$。若两个维度在 GUARDIAN 中具有完全相同的映射列，标记为 `not_separately_identifiable`，并补充联合删除分析。

### 10.2 模型、惩罚与评分

每个训练折拟合带 system 固定效应的 ridge logistic 模型。截距不惩罚，其他系数使用 `0.5*lambda*sum(beta^2)` 惩罚。候选网格为 `lambda={0.1,1,10}`；lambda 在每个外层训练集中通过内层 prompt-blocked 交叉验证选择，三个候选值的完整结果同时报告。

主要评分为 held-out log loss，Brier score 作为并列概率评分。模型比较使用完全相同的外层折分和配对评分差。

### 10.3 Prompt-blocked 重复交叉验证

53 个 prompts 使用固定种子完成 20 次重复的 5 折外层划分。每次划分以 prompt 为组，同一 prompt 的 12 个 systems 响应始终位于同一折。内层选择 lambda 时继续以 prompt 为分组单位。报告每次 repeat 的平均 held-out score、模型间差值、差值均值、2.5%-97.5% 分割分位和方向一致的 repeat 比例。

### 10.4 逐维增量

对每个可评价维度 `Vd` 比较 `CV_KE` 与 `CV_KE_drop_Vd`。若删除该维使 log loss 和 Brier 在全部 lambda 和主要折分中稳定变差，则标记为 `score_and_penalty_robust_increment`；若方向随评分、lambda 或分割改变，分别标记为 `score_sensitive`、`penalty_sensitive` 或 `partition_sensitive`；若平均改善不为正，标记为 `no_increment_detected`。

这些状态描述 GUARDIAN 固定面板中的内部信息，不改变 $K_R$。事件不足或映射不足时不强行拟合，标记为 `not_estimable_in_GUARDIAN`。

### 10.5 不确定性与重采样

1. Prompt-cluster bootstrap：有放回抽取 prompts，并保留每个 prompt 的 12 个 systems 响应；
2. Prompt×system 双向 bootstrap：分别有放回抽取 prompts 和 systems，使用二者笛卡尔组合；
3. 重采样次数：10,000；
4. 报告 2.5% 和 97.5% 分位，并明确其对应固定挑战面板组成的敏感性。

### 10.6 评价者分析

对总体及每个可评价维度计算观察一致率、Fleiss kappa 和两分类 Gwet AC1。依次删除每名 M2 评价者，重复计算一致性指标和结局派生，形成 leave-one-rater-out 范围。`m2_fail_share` 同时采用以 18 票为权重和每条 response 等权的表示。

### 10.7 映射与架构敏感性

- core、expanded 和 expanded-only；
- 单标签与多标签 prompts；
- leave-one-prompt、leave-one-system、leave-one-source-domain 和 leave-one-rater；
- Stage B 证据树的锁定分辨率；
- 每个维度的词汇、来源层和 ConceptUnit 稳定性；
- source-overlap-excluded framework 与主 framework 的 $K_R$、成员和 charter 比较；
- 维持每维 prompt prevalence 和每个 prompt 标签数的二部图 degree-preserving 置换阴性对照；
- Jaccard、覆盖、事件、共识、AC1 和裁决负担的阈值扫描。

置换阴性对照使用固定种子完成 1,000 次有效边交换；每次重建映射矩阵并重复 `CV_KE` 对 `CV0` 的外层评分。该分析判断观察到的增量是否超过具有相同标签稀疏度的随机多标签结构，不用于改变维度或映射。

### 10.8 多重性与解释

研究以完整报告、成对 held-out 比较和跨设定稳健性作为主要控制策略，不以单个 p 值决定维度保留。若增加正式假设检验，将在分析执行前定义检验族和多重性方法。三个评价结局属于同一结局家族，不作为独立重复证据计数。

## 十一、数据完整性、缺失与分析阻断

### 11.1 Stage A-B 完整性断言

自动检查检索版本、唯一记录 ID、去重结果、选择决定、来源指针、ConceptUnit 原文片段、来源标准化权重、抽取通道版本、语义向量、bootstrap 次数、split/merge trace、cluster hashes、$K_R$ 和 framework SHA-256。任何无法追踪至来源文本的 ConceptUnit 不进入主综合。

### 11.2 Stage C-D 完整性断言

Stage D 启动前自动检查：53 个唯一 prompts、12 个 systems、636 个唯一 prompt×system 组合、每条 response 18 张 M2 票、合法主外键、无重复映射、prompt mapping 可由锁定规则重建，以及 framework 和 mapping 哈希与注册版本一致。

### 11.3 缺失和非法值

主要结局、维度映射和主键不进行统计插补。非法连接、重复组合、票数不符、无法重建的映射或未说明的哈希变化将暂停下游分析并输出结构化 exception report。描述性字段缺失按缺失类别和分母报告。

### 11.4 变更记录

Framework lock 或 prompt-mapping lock 后，对输入、规则、模型版本、维度定义、映射、结局、数据分割、lambda、评分、模型结构或判定规则的任何改变，均在 deviation log 中记录日期、责任人、原因、影响和新版本哈希。原锁定版本和新版本分别保存。

## 十二、设计边界与解释范围

1. $K_R$ 表示在本 Protocol 的信息源、日期、语言、PCC、资格标准和开放综合规则下可稳定复现的概念维度数，不是普适或终局的本体数量；
2. 检索词用于提高证据召回，不构成候选维度；维度中性检索仍可能遗漏未被当前医疗 AI 词汇表达的价值现象；
3. 自动 ConceptUnit 抽取和语义表示依赖锁定模型与规则，因此通过独立通道、来源指针、词汇表示和参数敏感性评价其稳健性；
4. Scoping review 描述和组织证据，不生成临床效应合并、证据确定性等级或规范价值排序；
5. GUARDIAN 是固定挑战面板，用于评价锁定架构的覆盖、可估计性、结构区分和内部结局信息；
6. GUARDIAN prompts 未覆盖某维或某维缺乏预测增量，不等同于该价值维度不重要或不存在；
7. 全局 pass/fail 结局不替代未来的维度专属测量、利益相关者内容效度和外部队列验证；
8. 固定 systems、单次响应和研究语言限定结果适用范围。

## 十三、数据治理、伦理与复现

### 13.1 数据治理

所有输入以逻辑名称、版本、字节数和 SHA-256 登记。分析数据使用稳定去标识 ID。含直接身份或许可受限来源的文件保留在受控环境，只共享数据字典、哈希、代码和聚合结果。

### 13.2 伦理

本研究不招募新参与者，不直接接触患者，也不采集新的个人数据。GUARDIAN 数据使用遵循其机构伦理决定、数据使用权限和保密要求。正式伦理批准或豁免编号由责任研究者在 registry 和研究报告中填写。

### 13.3 计算复现

分析固定软件环境、程序版本、检索版本、抽取规则或提示词、语义模型、随机种子、输入哈希和输出清单。Framework lock、prompt-mapping lock、数据字典、统计代码、运行日志和聚合结果在许可范围内共享。相同输入和版本必须产生相同确定性输出。

## 十四、成果与报告计划

### 14.1 主要成果

1. PRISMA-ScR 来源选择流程、完整检索策略和 evidence map；
2. 可追踪 ConceptUnit table 和开放术语图谱；
3. $K_R$、证据树、dimension charters、split/merge decision trace 和 framework lock；
4. 残余或 emerging concepts 清单及证据空白；
5. $K_R$、$K_G$、$K_E$ 的完整状态表和 prompt-mapping lock；
6. 所得架构及各维度的 N/F/S 矩阵；
7. `CV0`、`CV_KE`、`CV26`、$K_E$ 个 drop-one 和证据树分辨率模型的完整比较；
8. 证据来源、抽取通道、表示、阈值、映射、评价者、system、prompt、lambda 和评分敏感性；
9. 阴性、敏感、未覆盖和不可评价结果的完整报告。

### 14.2 解释层级

每个维度依次评价以下层级：

1. source-traceable concept cluster；
2. scoping-review-derived stable dimension；
3. structurally distinguishable dimension；
4. GUARDIAN-covered dimension；
5. GUARDIAN-estimable dimension；
6. internally informative dimension with held-out outcome increment。

总体框架的目标表述为：an evidence-derived candidate VIM framework with transparent scoping-review provenance and internal structural, operational and outcome-based evaluation in a fixed GUARDIAN panel。

## 十五、参考文献

1. Peters MDJ, Godfrey C, McInerney P, Munn Z, Tricco AC, Khalil H. Scoping reviews. In: Aromataris E, Lockwood C, Porritt K, Pilla B, Jordan Z, eds. JBI Manual for Evidence Synthesis. JBI; 2024. doi:10.46658/JBIMES-24-09.
2. Tricco AC, Lillie E, Zarin W, et al. PRISMA Extension for Scoping Reviews (PRISMA-ScR): Checklist and Explanation. Ann Intern Med. 2018;169:467-473. doi:10.7326/M18-0850.
3. Levac D, Colquhoun H, O'Brien KK. Scoping studies: advancing the methodology. Implement Sci. 2010;5:69. doi:10.1186/1748-5908-5-69.
4. Munn Z, Peters MDJ, Stern C, Tufanaru C, McArthur A, Aromataris E. Systematic review or scoping review? Guidance for authors when choosing between a systematic or scoping review approach. BMC Med Res Methodol. 2018;18:143. doi:10.1186/s12874-018-0611-x.
5. Yu KH, Healey E, Leong TY, Kohane IS, Manrai AK. Medical Artificial Intelligence and Human Values. N Engl J Med. 2024;390:1895-1904. doi:10.1056/NEJMra2214183.
6. Goldberg C, Balicer RD, Bhat M, et al. The Missing Dimension in Clinical AI: Making Hidden Values Visible. NEJM AI. 2026;3(2). doi:10.1056/AIp2501266.

## 附录 A｜维度中性 PubMed/MEDLINE 主检索

下列检索由医疗 AI、医疗/儿科情境和广义价值边界三个 PCC 词块组成。词项用于提高召回率，不构成维度标签。试检索中发现的新增同义词和 MeSH 词可在主检索运行前加入；所有变更保留日期、理由、版本和完整检索式。

```text
(
  "Artificial Intelligence"[Mesh]
  OR "artificial intelligence"[Title/Abstract]
  OR "machine learning"[Title/Abstract]
  OR "deep learning"[Title/Abstract]
  OR "large language model"[Title/Abstract]
  OR "large language models"[Title/Abstract]
  OR ChatGPT[Title/Abstract]
  OR "generative AI"[Title/Abstract]
  OR "clinical AI"[Title/Abstract]
  OR "clinical decision support"[Title/Abstract]
  OR algorithm*[Title/Abstract]
)
AND
(
  health*[Title/Abstract]
  OR medic*[Title/Abstract]
  OR clinic*[Title/Abstract]
  OR patient*[Title/Abstract]
  OR paediatric*[Title/Abstract]
  OR pediatric*[Title/Abstract]
  OR child*[Title/Abstract]
  OR adolescen*[Title/Abstract]
  OR healthcare[Title/Abstract]
)
AND
(
  "Social Values"[Mesh]
  OR "Patient Preference"[Mesh]
  OR "Personal Autonomy"[Mesh]
  OR "Ethics"[Mesh]
  OR value*[Title/Abstract]
  OR ethic*[Title/Abstract]
  OR moral*[Title/Abstract]
  OR preference*[Title/Abstract]
  OR utility[Title/Abstract]
  OR tradeoff*[Title/Abstract]
  OR "trade off"[Title/Abstract]
  OR normativ*[Title/Abstract]
  OR right*[Title/Abstract]
  OR responsib*[Title/Abstract]
  OR accountability[Title/Abstract]
  OR governance[Title/Abstract]
  OR consent[Title/Abstract]
  OR autonomy[Title/Abstract]
  OR trust[Title/Abstract]
  OR fairness[Title/Abstract]
  OR equity[Title/Abstract]
  OR bias*[Title/Abstract]
  OR safety[Title/Abstract]
  OR harm*[Title/Abstract]
  OR uncertainty[Title/Abstract]
  OR explainab*[Title/Abstract]
  OR transparency[Title/Abstract]
  OR "shared decision making"[Title/Abstract]
)
AND english[Language]
AND ("2021/07/15"[Date - Publication] : "2026/07/15"[Date - Publication])
```

## 附录 B｜Dimension charter 空白模板

```yaml
dimension_id: null
cluster_hash: null
name: null
positive_definition: null
exclusion_boundary: null
core_value_tension: null
stakeholder_relation: []
observable_behaviour: []
consequence: []
governance_response: []
supporting_concept_unit_ids: []
supporting_source_ids: []
evidence_layers: []
counterexamples: []
parent_dimension: null
child_dimensions: []
cross_dimension_relations: []
bootstrap_survival: null
matched_cluster_jaccard: null
silhouette: null
sensitivity_status: null
core_mapping_rule: null
expanded_mapping_rule: null
```

## 附录 C｜计划输出与分析锁文件

| 输出 | 内容 | 生成阶段 |
|---|---|---|
| search_manifest | 信息源、日期、完整检索式、检索路径、结果文件和哈希 | Stage A |
| selection_log | 两个独立选择流、第三判定规则、决定、理由和来源指针 | Stage A |
| evidence_map | 来源特征、证据层和描述性分布 | Stage A |
| concept_unit_table | 无维度标签的 ConceptUnits、原文片段和来源指针 | Stage A |
| dimension_generation_log | 表示、bootstrap、递归分裂、近重复合并和每步判定 | Stage B |
| evidence_tree | 根节点、父子关系、稳定终端节点和残余概念 | Stage B |
| dimension_charters | `V1...V$K_R$` 的定义、边界、关系、证据与稳定性 | Stage B |
| framework_lock | $K_R$、证据树、charters、规则、版本和 SHA-256 | Stage B |
| prompt_mapping_lock | prompt、source domain、core/expanded 映射、通道一致性和 SHA-256 | Stage C |
| K_status_table | $K_R$、$K_G$、$K_E$ 及每维覆盖和可估计状态 | Stage C-D |
| analysis_manifest | 数据版本、结局规则、模型、折分、随机种子、lambda、评分和代码哈希 | Stage D 前 |
| NFS_matrix | 每个锁定维度的 N1-N5、F1-F5、S1-S5 原子判定 | Stage D |
| sensitivity_matrix | 证据、表示、阈值、映射、评价者、system、prompt、lambda 和评分结果 | Stage B-D |
| deviation_log | 锁定后所有变更、新版本及影响 | 全阶段 |
