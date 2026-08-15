# Auto-Research 检索与证据审计

## 审计摘要

- 检索截止：2026-08-09
- 最终纳入：48 个去重版本族
- 出版状态：35 项同行评议、12 项预印本、1 项官方报告
- 角色分层：38 项核心、8 项桥接、2 项背景
- 证据等级：A 级 30 项、B 级 7 项、C 级 11 项
- 一手来源：48/48 均指向正式会刊、期刊、arXiv、DOI、官方报告或官方仓库
- 核验深度：46 项全文或完整官方说明核验，2 项正式摘要与元数据核验；48 项均完成逐条主张编码
- 当前覆盖等级：L2。补漏后两个独立收敛家族的去重新增率均为 0%，六条一级路线稳定；严格数据验证、真实 Chrome 浏览器复验与安全扫描均已通过

以上终态统计全部由 `atlas.json` 现场分组计算；筛选、检索和主张账本只用于解释过程，不反向充当终态计数真源。

## 范围、同义词与边界

研究问题：Auto-Research 的发展全貌、主要技术路线、证据边界、关键系统与尚未解决的问题是什么？

核心操作定义：人工智能系统承担至少两个实质科研环节，并产生可由实验、代码、数据溯源、外部评价或同行评议检查的研究产物。定义领域路线、测量真实研究闭环、提供关键负面证据或安全治理框架的工作也可纳入。

检索同义词包括：`Auto-Research`、`autoresearch`、`automated research`、`autonomous research`、`AI scientist`、`research agent`、`scientific discovery agent`、`machine learning experimentation agent`、`self-driving laboratory`、`robot scientist`、`autonomous experimentation`、`automated hypothesis validation`、`research replication benchmark`。

排除：

- 传统 AutoML、神经架构搜索或单一贝叶斯优化，除非工作扩展为具有语义研究决策的多阶段闭环；
- 普通搜索、问答、润色、综述或报告生成；
- 与 `AutoResearch` 只有名称重合的市场研究服务、技能封装和第三方复刻；
- 无法定位方法、评测或一手入口的宣传；
- 被正式版本取代的预印本和同一论文的更正、代码、新闻报道，不重复计数。

## 来源家族与使用规则

发现阶段使用通用网页检索定位候选，但核心主张只接受以下一手入口：

1. Nature Portfolio 正式论文与更正页；
2. PMLR 的 ICML 正式会刊；
3. ICLR 官方论文页；
4. ACL Anthology 正式会刊；
5. NeurIPS 官方论文页；
6. OpenReview 的 TMLR 或正式会议记录；
7. NEJM AI、Science、Royal Society 等 DOI 或出版页；
8. arXiv 预印本原文；
9. 作者或机构官方仓库与白皮书。

新闻、综述、聚合页和搜索摘要只用于发现、外部争议定位或元数据交叉检查，不独立支撑核心能力主张。

## 查询轮次

完整逐行记录位于 [search_ledger.jsonl](../planning/search_ledger.jsonl)。下表是可读摘要；`命中`在搜索服务不提供稳定总数时记为不可获得，`筛选`指实际查看并去重的候选数。

| 轮次 | 来源与精确查询主题 | 筛选 | 新纳入 | 边际新增率 | 结果 |
|---|---|---:|---:|---:|---|
| 发现 1 | OpenReview/arXiv/NeurIPS/ACL：`autonomous research agent benchmark AI scientist research paper replication` | 12 | 6 | 50.0% | 建立评测与复现路线 |
| 核验 1 | arXiv/OpenReview/官方项目：`PaperBench RE-Bench CORE-Bench MLAgentBench autonomous research agents` | 14 | 5 | 35.7% | 转到正式会刊核验版本 |
| 反证 1 | arXiv/OpenReview/ACL：`AUTOEXPERIMENT RExBench InquiTree ResearcherBench research agents` | 13 | 4 | 30.8% | 定位自主性退化与长程失败 |
| 构想分支 | ACL/OpenReview：`scientific idea generation LLM novelty feasibility diversity human study` | 16 | 5 | 31.3% | 建立知识与构想路线 |
| 同名项目 | GitHub/arXiv：`AutoResearch autoresearch official GitHub autonomous research agent` | 18 | 5 | 27.8% | 区分 Karpathy 项目、综述和复刻 |
| 端到端分支 | Nature/NEJM AI/ACL：`end-to-end AI research agent scientist literature experiment paper peer review` | 24 | 6 | 25.0% | 核验正式版本族 |
| 机器学习分支 | PMLR/ICLR/OpenReview：`machine learning experimentation agent code search MLE benchmark autonomous research loop` | 31 | 8 | 25.8% | 建立可执行研发闭环 |
| 实体历史 | Nature/Science/Royal Society：`robot scientist autonomous laboratory self-driving laboratory closed-loop experiment discovery` | 29 | 6 | 20.7% | 从 Adam 到 SAMPLE |
| 领域补漏 | Nature/PMLR/OpenReview：`AI agents scientific hypothesis validation nanobody chemistry materials discovery human experiment` | 27 | 7 | 25.9% | 生物、化学、材料与证伪 |
| 安全反证 | Nature 系列：`AI scientist safety laboratory benchmark risk hallucination diversity leakage reproducibility` | 23 | 5 | 21.7% | 安全、认识论与泄漏 |
| 元数据核验 | Science/机构库/DOI：`The automation of science Adam robot scientist Eve drug repositioning DOI` | 12 | 2 | 16.7% | 历史论文交叉核验 |
| 饱和扩展 A | Nature/PMLR/ACL/OpenReview 定向横扫 | 47 | 0 | 0.0% | 无新一级路线、无独立信息增量 |
| 饱和扩展 B | 综述引文/官方仓库/版本追踪 | 61 | 0 | 0.0% | 新结果均为重复、长尾或代表性折叠 |
| 2026 前沿补漏 | arXiv/ACL/官方项目：`AutoResearchBench ResearchClawBench DiscoPER BadScientist PAPERMIND AI evaluate AI scientists` | 9 | 5 | 55.6% | 新增 AutoResearchBench、ResearchClawBench、DiscoPER、BadScientist、PAPERMIND；自动评审循环性预印本折叠 |
| 专业科学补漏 | Nature/预印本/外部基准：`CellVoyager BioMedAgent RoboChem-Flex` | 3 | 1 | 33.3% | 新增 CellVoyager；后两项代表性折叠 |
| 最终收敛 C | Nature/PMLR/ACL/OpenReview 正式出版定向回扫 | 24 | 0 | 0.0% | 复核正式版本和 AgenticSciML、X 射线科学家等折叠项；无新路线 |
| 最终收敛 D | arXiv/GitHub：`2606/2607 scientific research agent benchmark` 与 `autoresearch benchmark scientific agent` | 19 | 0 | 0.0% | EurekAgent、AHOIS 分别折叠到数字环境和实体闭环；无新路线 |

全部 17 轮都保存在机读 [search_ledger.jsonl](../planning/search_ledger.jsonl)，具名纳排和折叠决定另见 [screening.csv](../planning/screening.csv)。

旧版把早期两轮 0% 去重新增率解释为“路线级候选发现饱和”，后续日期特异性补漏新增 6 项，证明旧结论过早。因此以当前 48 项为基线另做两个独立回扫：正式出版家族筛选 24 个去重候选、新近预印本/仓库家族筛选 19 个，均新增 0 项且无第七条一级路线。这支持“截止日的路线级可见候选已收敛”，不等于绝对穷尽未公开系统或未索引长尾。

## 筛选、去重与版本族

最终 48 个纳入版本族以 `atlas.json` 为准；[screening.csv](../planning/screening.csv) 另行记录纳入、排除、合并和候补，不把版本、外部反证或代表性折叠重复计入终态。主要版本决策如下：

- The AI Scientist 的 2024 初版、2025 v2 与 2026 Nature 正式论文合并为 `ai-scientist-nature`；正式版本优先，早期差异写入机制和限制。
- Agent Laboratory 使用 Findings of EMNLP 2025 正式版本，早期 arXiv 不重复计数。
- Google Co-Scientist 使用 2026 Nature 正式版本，早期预印本合并。
- MOOSE-Chem 以 ICLR 2025 主会论文为规范版本；后续 AI4X 2025 页面只作版本关联。
- A-Lab 的正式论文、Nature 出版更正与 PRX Energy 同行评议反证视为同一证据版本族；地图采用更正后 36/57 口径，并把“新”限定为平台此前未见。
- ERA 正式论文与 2026-08-06 的独立数据泄漏复核是不同研究问题和不同团队，分别纳入并相互关联。
- Karpathy `autoresearch`、专长代理和双层 AutoResearch 有不同机制与实证，分别纳入；大量第三方技能、复刻和营销页排除。
- FunSearch 作为可验证算法搜索前驱，由机制更广的 AlphaEvolve 代表，不再单列。
- AutoResearchBench 以 `arXiv:2604.25256v1` 为当前规范版本；完整 1,000 题与昂贵端到端系统的随机 50 题子集分别记分母，GPT Deep Research 的 11/50 不能写成 11%。
- ResearchClawBench 以 `arXiv:2606.07591v5` 为当前规范版本；只引用 40 题全覆盖的单系统均值，并保留“7 个代理家族/8 个配置”和 frontier mean 24.6/25.8 的正文冲突。
- DiscoPER 以 `arXiv:2607.01131v1` 为当前规范版本；support rate 不是独立发现数，Sonnet 4.6/4.5 的模型版本冲突未擅自消解。
- BadScientist 使用 ACL 2026 正式会刊版本；名义设计为 600 次生成，但结构检查后的逐策略有效稿数未披露，因此 82.0% 不反推为 82/100。
- PAPERMIND 使用 Findings of ACL 2026 正式版本，`arXiv:2604.21304v2` 合并到同一版本族。它测给定论文后的理解、证据推理和批判，与 TACL 反事实推理反证、BadScientist 的完整性红队各有独立信息增量，不互相折叠。
- CellVoyager 使用 Nature Methods 正式版本；作者 bioRxiv 稿只提供连续正文位置，HeurekaBench 是独立但移除了假设提议阶段的外部评测，不能合并为原系统的同任务复现。
- `Can AI Evaluate AI Scientists?` 仅有 `arXiv:2607.28631` 预印本，没有人类评审金标准；模型间一致性与包含相同模型的合成分存在机械循环，因此折叠到 BadScientist/自动评审限制，不独立计数。

## 分类轴的反证过程

最初候选第二轴是泛化“自治等级”。样本核验后将其改为“科研闭环覆盖深度”，理由如下：

- Google Co-Scientist、Virtual Lab 和 Robin 都有现实实验结果，但实验由人类执行；若只看结果是否来自湿实验，会错误标成实体自治。
- Coscientist 虽能生成并执行部分机器人协议，但测量结果没有驱动下一轮实体实验；反应优化循环主要发生在既有数据集，因此归为数字闭环 L2。
- PaperBench、RExBench 和 AUTOEXPERIMENT 是评价论文，不是研究系统；其层级应表示实际测量的闭环深度。
- A-Lab 和 SAMPLE 的实体闭环深度很高，但这不自动提高新颖性、外部复现和安全证据。
- SciMON 与构想盲评只覆盖单环节，即使模型产出的想法看起来“像研究”，也不能上调为端到端。

最终四级轴因此只回答“实际闭合了多少研究环节”，证据质量另以 A/B/C 和 V/D/P/Q 表达。

## 证据编码

### A/B/C 展示等级

- A：正式同行评议且有可定位实验、基准或系统证据；共 30 项。
- B：官方代码、官方报告或同行评议观点，信息可靠但缺少完整能力验证；共 7 项。
- C：预印本或尚无独立复核的前沿结果；共 11 项。

### V/D/P/Q 审计向量

- V：来源核验深度，V0–V4；本地图核心项均至少核验一手摘要，关键争议项检查全文或完整官方说明。
- D：验证独立性，D0–D3；独立复核如 ERA 数据泄漏使用 D3，作者内部留出与对照通常为 D2。
- P：出版与系统证据状态，P1 为非同行评议来源、P2 为同行评议、P3 为更高层系统证据，PX 表示撤稿或重大争议；“官方”不是自动升档理由。
- Q：主张置信度，Q0–Q3；单基准前沿预印本通常不高于 Q2，观点框架通常为 Q1。

48 条代表性主张、证据位置、向量和限制逐行记录在 [claim_ledger.csv](../planning/claim_ledger.csv)。

## 关键反证和冲突处理

1. **评审分数不是正式接收。** The AI Scientist 的三篇投稿均在正式决定前按预注册方案撤回；其中一篇得分高于该工作坊通常接收阈值，组织者认为很可能获接收，但地图不把反事实判断写成接收事实。
2. **验证提升不等于测试迁移。** 分子 Auto Research 的验证—测试崩塌与材料版本的积极留出迁移同时纳入，不做单向结论。
3. **ERA 疫情案例有数据修订争议。** 独立复核只否定原回顾设计中的部分归因；其对后续前瞻系统的积极观察也保留。
4. **A-Lab 的合成数与新颖性不同。** 353 次实验和更正后 36/57 合成事实，与材料是否科学上首次发现、结构判定及四个不确定目标分开陈述。
5. **多智能体不等于多样性。** ResearchAgent 和 Co-Scientist 的协作收益，与 Diversity Collapse 的结构耦合风险并列。
6. **人类执行实验不等于实体自治。** Virtual Lab、Co-Scientist 和 Robin 均归为多环节人审工作流；Coscientist 因缺少实体反馈到下一轮的闭环而归 L2，不因能调用设备就升为 L3。
7. **完整集、子集和有效稿是不同分母。** AutoResearchBench 的 1,000 题完整基准与 50 题昂贵系统子集分开；BadScientist 的 600 次名义生成与未披露的结构有效稿数分开；百分比不跨分母重算。
8. **固定留出通过不等于独立发现。** DiscoPER 在 100 轮中重复使用同一留出集，support rate 只描述作者定义的通过比例；没有最终封存集和多重比较校正时，不把它写成发现数量。
9. **任务改造后的外部结果不等于原流程复现。** CellVoyager 的 HeurekaBench 外部评测移除了假设提议阶段；其低分是重要反向证据，但不能与原作者完整工作流结果直接排名。
10. **论文理解、错误检出和评审抗攻击不可混为一项。** PAPERMIND、TACL 反事实评审研究和 BadScientist 分别测给定论文后的理解、对逻辑错误的敏感性和对蓄意不可靠稿件的鲁棒性；共同使用模型裁判也不使三者成为同一指标。

## 五道覆盖闸门

### 1. 来源覆盖：通过

九类一手来源家族均有记录，核心结论不依赖聚合页。所有 48 项均有稳定主入口。

### 2. 分支代表性：通过

六条路线按知识综合与构想、范式与端到端编排、机器学习研发闭环、领域科学发现、实体自驱实验室、评测复现与治理的顺序，分别有 5、4、6、9、6、18 项。每条路线至少包含奠基或代表工作、当前前沿，以及评测、反证或明确限制。

### 3. 边际新增率：通过

以补漏后 48 项为基线，正式出版家族与新近预印本/仓库家族两轮分别筛选 24 与 19 个去重候选，均新增 0 项、边际新增率 0%，且未出现新一级路线。EurekAgent 和 AHOIS 作为新预印本代表性折叠进入筛选账本，不伪装为“未发现”。

### 4. 逐篇证据核验：通过 L2 要求

48 项均完成一手入口和元数据核验；46 项检查全文或完整官方说明，2 项检查正式摘要与元数据。38 项核心记录全部写有机制、直接证据、至少一项限制、适用含义和 V/D/P/Q；保留为摘要核验的 AlphaEvolve 与 MOOSE-Chem 使用 V2，不以 V3 伪装全文阅读。没有将搜索摘要作为最终证据。

### 5. 主张审计：通过

48 条代表性主张全部进入主张账本；高风险数字均限定适用范围。除既有 ERA、A-Lab、The AI Scientist、分子/材料 Auto Research 与长程基准外，六项新增工作也记录了分母、裁判、版本冲突、任务改造或外部验证边界。

五道覆盖闸门全部通过；严格数据验证、真实 Chrome 桌面/手机/`file://`/键盘/200% 缩放/无脚本回归及安全扫描也全部通过，因此终态覆盖等级为 L2。

## 失败入口与覆盖限制

- 某些出版社全文需要订阅；此时使用正式摘要、开放补充材料、DOI 元数据和作者项目交叉核验，并降低核验深度标记。
- GitHub 星标、产品榜单和市场宣传没有作为能力证据。
- 搜索服务不稳定提供总命中数，因此审计记录实际筛选的去重候选数，不伪造命中总量。
- 中文检索主要用于术语和交付；核心学术文献以英文为主，可能漏掉未进入主流索引的非英语研究。
- 未公开企业系统、内部实验、无稳定入口的演示以及截止日之后的更正无法纳入。
- 2026 年条目更新快；预印本一旦出现正式版本、撤稿或独立复现，应按版本族规则更新。

## 可复核资产

- 单一数据真源：[atlas.json](../atlas.json)
- 检索账本：[search_ledger.jsonl](../planning/search_ledger.jsonl)
- 纳排与版本账本：[screening.csv](../planning/screening.csv)
- 主张证据账本：[claim_ledger.csv](../planning/claim_ledger.csv)
- 综合报告：[REPORT.md](REPORT.md)
- 编译导出：[papers.json](../data/papers.json)、[papers.csv](../data/papers.csv)、[references.bib](../data/references.bib)
