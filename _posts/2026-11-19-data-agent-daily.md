---
layout: post
title: "Data Agent Daily — 2026-11-19"
author: dad
date: 2026-11-19
image: "assets/images/covers/2026-11-19.svg"
description: "ThoughtSpot 宣布 Spotter 通过 MCP 连接器接入 Claude Data，Claude 生成的仪表板按受治理的语义层与行级权限解析，Send To ThoughtSpot 一键转为 Liveboard，两项集成即日起向客户开放；Databricks Genie Code CLI 正式 GA，Google 发布 Gemini 4 Neon。"
categories: ["Data Agent Daily"]
tags: ["data-agent", "news"]
comments: false
---

## 今日速览

- ThoughtSpot 宣布两项与 Claude 的集成：Spotter 通过 Spotter MCP 连接器接入 Claude Data，Claude 生成的仪表板按 ThoughtSpot 语义层与行级权限解析；Send To ThoughtSpot 一键把 Claude Data 中的分析产物转为受治理的 Liveboard，两项集成即日起向客户开放。
- ThoughtSpot 推出 Customer Hosted 部署选项，企业可在自有 AWS 账号或 GCP 项目内部署其数据与 AI 平台（含 Spotter），控制面与数据面均不出客户云，可自带私有 LLM。
- Databricks 的 Genie Code CLI 于 11 月 18 日正式 GA，可在终端运行 Genie 编码 agent；同日发博客介绍 11 月 5 日进入 Beta 的 Genie Migrate for Serverless，以可审核 diff 把经典计算任务迁移至 serverless，支持 30 天回滚。
- Databricks 获第二届 A-Team AI in Capital Markets Awards 2026“数据智能与治理最佳 AI 方案”奖，系首次获该奖；RBC Capital Markets 在 Databricks 上构建的 Aiden QuickTakes 智能体自动生成研究报告草稿的速度提升最高达 95%。
- Google 发布 Gemini 4 Neon，定价 $3/$15 每百万 token、100 万 token 上下文，Artificial Analysis 智能指数 61 分排第 3、Coding Agent Index 58.6 分排第 1，Agent Arena 指数排第 2。
- OpenAI 发布内部 agent 报告：其 coding agent 独立完成 2–4 小时研究任务的成功率从 3 月的 23% 升至 10 月的 46%，研究员人均 agent 工作量从每天 0.5 个 agent 工作日升至 5.7 个。
- Oracle 推出面向临床试验运营的 Life Sciences AI Agents，进入早期采用，覆盖组合监控、试验规划与试验执行。
- Google Labs 推出实验性常驻产品 agent Stitch Loop，接入代码库与实时指标持续优化已上线产品，全球候补名单开放。
- Snowflake 称将在 GITEX GLOBAL 2026 展示 CoCo、CoWork 与 Business Ontology 等 AI Data Cloud 能力。
- 按 11 月 16 日公布的计划，Tableau Studio 服务器版定于今日上线，但截至发稿未见官方确认。
- arXiv 11 月 19 日上线 MARS：淘宝多阶段智能体推荐系统，用微调 Qwen3-0.6B 的近线智能体为每个用户生成七维流水线配置，两周 A/B 测试最大提升 V2P +5.22%、GMV +7.34%。
- arXiv 11 月 19 日上线 The Value Semantics Layer：IBM 提出面向智能体 AI 的值语义层，把值语义外化为规划器可见的基础设施。
- arXiv 11 月 19 日上线 ReflectRec：用循环一致性偏好校验改进 LLM 推荐，MovieLens-100K/1M 上比 CoT4Rec-ICL 高 +16.25/+4.46 个百分点 Hit@10。
- arXiv 11 月 19 日上线 CONCORD-Rec：目录条件模态效用的语义 ID 扩散推荐，20 组协议-数据集上 NDCG 平均提升 4%，30% 模态冲突下提升 14.63%。
- arXiv 11 月 19 日上线 Piccolo：阿里 AgentScope 团队用智能体数据工程与递归自改进协同演化决策模型与数据，Piccolo-27B 在 Decision Index Vision Full 榜上得 75.59 分居首。
- arXiv 11 月 19 日上线 CaDO：多智能体框架自动诊断并修复因果推理数据集的标注错误与结构失衡，18 组实验设置的 16 组上胜过最强数据清洗基线。
- arXiv 11 月 19 日上线 Evaluating Governed LLM-Driven ML Experimentation：面向自主跑 ML 实验的智能体的受治理评估框架，6 个 ML 任务、1,445 次试验全部记入只可追加的台账。
- arXiv 11 月 19 日上线 When Do LLMs Model the Right Target?：11 个模型在高风险预测问题建模中不加引导时不可靠地处理决策依赖性，给出目标、假设与估计程序后目标对齐实现率达 99–100%。
- arXiv 11 月 19 日上线 OASIS：面向 LLM 语义过滤的在线自适应框架，在线延迟降低 1.75–5.42 倍，LLM 处理的文档数减少 35%–75%。
- Wren AI 官方 Facebook 11 月 19 日发帖宣传与 Phison 的本地部署 GenBI 合作，模型在客户自有环境内运行，SC26 现场演示。

## 公司发布 / 官方博客

### 1. ThoughtSpot 深化与 Claude 的集成，Spotter 接入 Claude Data（11/18）
ThoughtSpot 11 月 18 日宣布两项与 Claude 的集成：Spotter 通过 Spotter MCP 连接器接入 Claude Data，Claude 把每个纯文本问题交给 Spotter，在 ThoughtSpot 语义模型上用客户已认证的度量、连接、同义词、业务定义与行级权限解析，Claude 生成的每个仪表板都按同一套受治理的定义落地，同一问题在同一数据上每次返回同一答案；每个结果附带生成它的搜索 token（所用的度量、属性、过滤条件与时间范围），用户可阅读、质疑并重新运行。Send To ThoughtSpot 可一键把 Claude Data 中建好的分析产物转为 ThoughtSpot Liveboard，每个图块已按 Spotter 的搜索 token 接地，无需重建或重新解释；转入后团队可按现有权限与行级安全共享、可验证 Liveboard 版本、可设 KPI 提醒与订阅、可下钻到行级并向 Spotter 追问，还可通过 Google Sheets、Excel、移动应用、Slack、Teams 触达用户或嵌入自有应用。两项集成即日起向 ThoughtSpot 客户开放。
- [GlobeNewswire 通稿（11/18）](https://www.globenewswire.com/news-release/2026/11/18/3405968/0/en/thoughtspot-deepens-integration-with-claude-to-advance-agentic-analytics-for-the-enterprise.html)

### 2. ThoughtSpot 推出 Customer Hosted 部署选项（11/18）
ThoughtSpot 11 月 18 日推出 Customer Hosted 部署选项，企业可在自有 AWS 账号或 GCP 项目内部署其数据与 AI 平台（含 agentic AI 分析师 Spotter），控制面与数据面均在客户云内，以满足数据主权与合规要求，并支持自带私有 LLM。
- [GlobeNewswire 通稿（11/18）](https://www.globenewswire.com/news-release/2026/11/18/3405722/0/en/thoughtspot-introduces-customer-hosted-deployment-giving-enterprises-full-control-of-their-data-and-ai.html)
- [TechTarget 报道（11/18）](https://www.techtarget.com/news/thoughtspot-debuts-customer-hosted-to-address-data-sovereignty/874882/)

### 3. Databricks：Genie Code CLI 正式 GA，Genie Migrate for Serverless 介绍博客（11/18）
Databricks 11 月 18 日宣布 Genie Code CLI 正式 GA，与工作区内的 Genie Code 同一套管理方式：管理员跨 CLI 与工作区统一管理一个 Genie Code 预算，用户每月免费的 Genie 用量同样适用于 CLI，可在终端运行 Genie 编码 agent。同日 Databricks 发博客介绍 11 月 5 日进入 Beta 的 Genie Migrate for Serverless：该 agent 扫描经典计算任务并评估迁移可行性，翻译计算配置与库，把变更以可审核 diff 形式提交、经人工批准后才写入，可 30 天回滚，工作负载代码本身不动，不确定的 Spark 配置会标记出来交由用户决定；可通过 Databricks CLI 的 compute-migrations 命令组批量迁移，也可在 Genie Code 内用 /compute 迁移单个 notebook 或任务；以 Databricks Asset Bundles 或 Git 文件夹为事实来源的任务暂不支持迁移。
- [Databricks 11 月发布说明：Genie Code CLI GA（11/18）](https://docs.databricks.com/gcp/en/release-notes/product/2026/november)
- [Databricks 博客：Introducing Genie Migrate for Serverless（11/18，经转述）](https://engineered.at/articles/introducing-genie-migrate-for-serverless)

### 4. Databricks 获 A-Team 资本市场 AI 奖“数据智能与治理最佳 AI 方案”（11/19）
Databricks 11 月 19 日宣布获第二届 A-Team AI in Capital Markets Awards 2026“Best AI Solution for Data Intelligence & Governance”奖，系首次获该奖，获奖者由资本市场从业者社区投票选出。通稿以 RBC Capital Markets 在 Databricks 上构建的 Aiden QuickTakes 智能体为例：该智能体统一数据摄取、AI 分析与内容生成，自动生成研究报告草稿的速度提升最高达 95%，同时满足受监管资本市场的治理与安全要求；LSEG 与 Databricks 合作把 AI 就绪的金融数据原生接入分析，AI 智能体可用 plain English 查询 35 万多项投资标的。Databricks 称，面向业务用户的 Genie One 是统一前端，管理者、分析师与风控人员用自然语言提问即可得到以 Unity Catalog 为依据的答案；经 MCP，同一受治理层延伸至 Microsoft Teams、Excel 以及 Claude、ChatGPT 等助手，每次请求按 Unity Catalog 权限授权并记录，生成的 SQL 与血缘可检查。
- [Databricks 官方博客（11/19）](https://www.databricks.com/blog/databricks-wins-team-award-ai-capital-markets-0)

### 5. Google 发布 Gemini 4 Neon（11/18）
Google 11 月 18 日推出 Gemini 4 系列新模型 Neon，定位在 Carbon 与 Hydrogen 之间，定价 $3 每百万输入 token（缓存输入 $0.15 每百万 token）、$15 每百万输出 token，100 万 token 上下文窗口，即日起在 Gemini API、Google AI Studio、Antigravity（付费 Pro/Ultra 用户）与 Gemini 应用（Pro/Ultra 用户）中推出。Google 称 Neon 面向长程 agent 工作流与多步骤分析：Artificial Analysis 智能指数 61 分排第 3，Coding Agent Index 58.6 分排第 1，Agent Arena 指数 1336 分排第 2（4,200 多个真实 agent 会话），Vals 指数 70.9% 排第 2；Terminal-Bench 4.1 得 65.2%，Agents' Last Exam v1.1 得 75.8%，Chartography  dense 图表阅读得 73.5%；Zapier AutomationBench 56.3% 排第 1，Andon Labs Vending-Bench 2 得 $16,843 排第 1。Neon 在默认 high 思考级别下每任务成本比 Carbon 低 32%，在高思考级别下比顶级竞品低约 50%–80%。
- [Google 官方博客：Introducing Gemini 4 Neon（11/18）](https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-4-neon/)

### 6. OpenAI 发布内部 agent 报告《Research acceleration: The jagged frontier》（11/18）
OpenAI 11 月 18 日发布内部 agent 使用报告：其 coding agent 独立完成 2–4 小时研究任务的成功率从 3 月的 23% 升至 10 月的 46%；研究员人均 agent 工作量从每天 0.5 个 agent 工作日升至 5.7 个，按 API 价折算人均日花费中位数达 2,400 美元。
- [OpenAI 官方博客（11/18）](https://openai.com/index/research-acceleration-jagged-frontier/)

### 7. Oracle 推出 Life Sciences AI Agents（11/18）
Oracle 11 月 18 日推出面向临床试验运营的 Life Sciences AI Agents，进入早期采用，覆盖组合监控、试验规划与试验执行，整合 Oracle 生命科学应用与第三方数据，发现运营问题并推荐行动供人工审批。
- [Clinical Research News 报道（11/18）](https://www.clinicalresearchnewsonline.com/news/2026/11/18/oracle-launches-ai-agents-for-clinical-trial-teams)

### 8. Google Labs 推出 Stitch Loop（11/18，简讯）
Google Labs 11 月 18 日推出实验性常驻产品 agent Stitch Loop，接入代码库与实时指标持续优化已上线产品，默认含安全、延迟、无障碍三条循环，安全循环结合 Gemini 4 Carbon 与 DeepMind CodeMender，全球候补名单开放，AI Ultra 用户优先。
- [Google 官方博客（11/18）](https://blog.google/innovation-and-ai/models-and-research/google-labs/stitch-loop/)

## 新闻网站

### 9. Snowflake 将在 GITEX GLOBAL 2026 展示 agentic AI（11/19，简讯）
Snowflake 11 月 19 日称将在 GITEX GLOBAL 2026 展示 CoCo（数据团队编码 agent）、CoWork（个人工作 agent）与 Business Ontology 等 AI Data Cloud 能力。
- [GEC Newswire 通稿（11/19）](https://gecnewswire.com/snowflake-to-showcase-agentic-ai-innovations-at-gitex-global-2026/)

### 10. Tableau Studio 服务器版定于今日上线，截至发稿未见官方确认（11/19，简讯）
按 11 月 16 日公布的发布计划，Tableau Studio 服务器版定于 11 月 19 日上线；截至发稿，Salesforce 新闻中心与 Tableau 官方渠道未见上线确认稿。云版已于 11 月 17 日按计划上线。微软 Ignite 2026 第 3 天（11 月 19 日）的报道均为 11 月 17–18 日内容的复述，未见 Fabric、Copilot 或 Microsoft IQ 的新事实增量。
- [首尔经济日报英文版报道（11/17，发布计划）](https://en.sedaily.com/business/2026/11/17/salesforce-launches-tableau-studio-an-ai-agent-for-data)

## 论文 / arXiv

### 11. MARS：淘宝多阶段智能体推荐系统技术报告（11/19）
MARS: Multi-stage Agentic Recommendation System（arXiv:2611.24006，11 月 18 日提交，11 月 19 日上线，作者 Tong Liu、Chaoqun Hou、Longxiang Xiong 等 17 人）把个性化从单阶段预测扩展到整条流水线编排：用微调 Qwen3-0.6B 的近线智能体为每个用户生成七维流水线配置（流水线模式、检索配额、模型选择、融合权重、重排器设置等），配置经校验与缓存后异步消费，级联不等待 LLM 推理；策略经三阶段训练（Confidence-aware SFT、Format-Anchored Preference Optimization、GRPO 沙箱回放）。淘宝五大场景、千万级日活的两周 A/B 测试显示全部关键指标正向，最大提升 V2P +5.22%、GMV +7.34%，约 20% 的请求走轻量 Minimal 模式，平均服务延迟比生产基线低 12ms。
- [arXiv:2611.24006](https://arxiv.org/abs/2611.24006)

### 12. The Value Semantics Layer：面向智能体 AI 的机器可理解数据库语义层（11/19）
The Value Semantics Layer: Enabling Machine-Understandable Databases for Agentic AI（arXiv:2611.23629，11 月 17 日提交，11 月 19 日上线，作者 Jalal Mahmud、Eser Kandogan）指出，随着数据系统同时服务自主 LLM 智能体与人类分析师，需要更丰富的语义基础设施连接分析概念与分析操作；现有元数据系统只暴露 schema、目录、血缘与治理信息，对操作语义的支持有限。论文提出 Value Semantics Layer（VSL），把值语义外化为持久的、规划器可见的基础设施，引入可复用的 Value Semantic Types（VSTs，捕捉分布、关系、过程、定量与策略依据的操作语义断言），让规划器校验分析操作、选择合适算子并引导分析工作流；论文给出动机、形式化、架构与原型实现，并提出面向 AI 原生语义基础设施的研究议程。
- [arXiv:2611.23629](https://arxiv.org/abs/2611.23629)

### 13. ReflectRec：用循环一致性偏好校验改进 LLM 推荐（11/19）
ReflectRec: Cycle-Consistency Preference Verification for LLM-based Recommendation（arXiv:2611.23969，11 月 18 日提交，11 月 19 日上线，作者 Dae Kyoo Kim、Heejung Cho、Sungmoo Hong、Eunil Park），已发表于 EMNLP 2026 主会。CoT 式 LLM 推荐器先生成一段自然语言偏好注释再排序，但该注释未经校验，且排序器不参考行为相似用户；ReflectRec 用偏好到历史的往返校验器为偏好注释打分，可恢复性低时条件再生，并在多轮再生中择优，同时注入行为相似用户未来观看记录作为协同提示。在 MovieLens-100K 与 MovieLens-1M 上，完整管线比 CoT4Rec-ICL 高 +16.25/+4.46 个百分点 Hit@10，三个 LLM 骨干（Qwen3-30B、Qwen2.5-72B、Llama-3.3-70B）上均有正向增益。
- [arXiv:2611.23969](https://arxiv.org/abs/2611.23969)

### 14. CONCORD-Rec：目录条件模态效用的语义 ID 扩散推荐（11/19）
CONCORD-Rec: Catalog-Conditioned Modality Utility for Semantic-ID Diffusion Recommendation（arXiv:2611.23710，11 月 18 日提交，11 月 19 日上线，作者 Haopeng Jin、Bingkang Shi、Tao Yu、Yifei Ma、Hao Liu、Hongzhu Yi、Jinwen Luo）针对多模态生成式推荐：模态缺失、退化或语义冲突时，均匀融合与无约束 token 门控会在迭代去噪中传播误导内容。CONCORD-Rec 用反事实目录划分效用监督可用性掩码的 token 级门控，在固定分词器与部分掩码的语义 ID 状态下评估跨越精确可行目录支撑的异折教师联盟。20 组协议-数据集上 NDCG 平均提升 4%，30% 模态冲突下提升 14.63%，完整 vs 均匀的 T=16 扫描在提升质量 2.00–3.58% 的同时把 p95 延迟最多降低 86.89%。
- [arXiv:2611.23710](https://arxiv.org/abs/2611.23710)

### 15. Piccolo：通过递归自改进协同演化决策模型与数据（11/19）
Piccolo（arXiv:2611.24651，11 月 18 日提交，11 月 19 日上线，作者 Zhenqing Ling、Qirui Jiao 等，含 Bolin Ding、Jingren Zhou，阿里 AgentScope 团队）用智能体数据工程（Agentic Data Engineering）与递归自改进协同演化决策模型与训练数据，Piccolo-27B 在 Decision Index Vision Full 榜上得 75.59 分居首。
- [arXiv:2611.24651](https://arxiv.org/abs/2611.24651)

### 16. CaDO：形式化验证引导的多智能体因果数据集修复与生成框架（11/19）
CaDO（arXiv:2611.24406，11 月 18 日提交，11 月 19 日上线，作者 Songli Yu、Qi Luo）提出多智能体框架自动诊断并修复因果推理数据集的标注错误与结构失衡，在 18 组实验设置的 16 组上胜过最强数据清洗基线，下游模型精度最多提升 9.1%，被标记样本中至少 95% 确有缺陷。
- [arXiv:2611.24406](https://arxiv.org/abs/2611.24406)

### 17. Evaluating Governed LLM-Driven ML Experimentation：受治理的 ML 实验智能体评估（11/19）
Evaluating Governed LLM-Driven ML Experimentation: Lifecycle, Provenance, and Failure Metrics（arXiv:2611.23678，11 月 18 日提交，11 月 19 日上线，作者 Dowling Wong），发表于 KDD 2026 Workshop on Evaluation and Trustworthiness of Agentic AI。自主跑 ML 实验的智能体通常只按达到的最佳分数评判，但分数不说明过程：智能体是否留在允许编辑的文件内、失败试验是保留还是悄悄丢弃、每次保留或丢弃决定能否追溯到证据。论文提出按实验过程与结果一起评估，并构建受治理的 harness：控制面（而非提议变更的 LLM）拥有每次试验的生命周期、检查编辑范围、决定保留或丢弃，并把每条记录追加进只可追加的台账；无效动作率、重复坏提议率、溯源完整性等治理指标均由此台账计算。6 个 ML 任务、1,445 次试验上同一契约不变适用；台账揭出分数掩盖的失败，包括一个 120 次试验全部失败的无记忆臂、一个有界提议耗尽的基准适配器，以及一次由可复现哈希揭出的重置失败；只记录成功试验的对照循环漏记了 50 次试验中的 43 次，而受治理台账记录了全部 50 次；全部 1,445 次试验的台账已公开。
- [arXiv:2611.23678](https://arxiv.org/abs/2611.23678)

### 18. When Do LLMs Model the Right Target?：LLM 在高风险预测问题建模中的目标对齐（11/19）
When Do LLMs Model the Right Target? Problem Formulation in High-Stakes Risk Prediction（arXiv:2611.23638，11 月 18 日提交，11 月 19 日上线，作者 Jennifer Zhang、Amanda Coston）研究 LLM 辅助数据科学时能否正确建模预测问题：聚焦决策依赖性（历史决策影响观测结果）这一有效性挑战，在儿童福利、医疗与就业三个场景、用 11 个 OpenAI 与 Anthropic 模型、7 种提示条件评估 LLM 生成的代码与解释。结果显示，不加引导时 LLM 不可靠地处理决策依赖性；当提示明确目标、估计该目标所需的假设与估计程序时，目标对齐的实现率达 99–100%；在前沿模型上，仅用一句话描述决策如何影响结果已足以引出目标对齐的实现；部分回答在解释中承认了决策依赖性、代码中却未处理。论文提出以有效性为中心的 LLM 辅助预测建模指南。
- [arXiv:2611.23638](https://arxiv.org/abs/2611.23638)

### 19. OASIS：面向 LLM 语义过滤的在线自适应框架（11/19）
Towards Online Adaptive LLM-based Semantic Filtering（arXiv:2611.24518，11 月 18 日提交，11 月 19 日上线，作者 Ziqi Zou、Zhenyan Nie、Kangfei Zhao 等）针对 LLM 在非结构化文档上按自然语言谓词做语义过滤：每篇文档都调一次 oracle LLM 成本过高、在线延迟过大，现有模型级联用轻量代理模型打分、只把不确定的文档交给 oracle，但代理模型泛化有限，且固定采样预算做代理训练与阈值校准，难以适应多样的在线查询。OASIS 结合与查询无关的文档相似性先验与查询自适应的在线学习和采样：离线阶段用文档相似性作先验并在文档嵌入上建图；每个在线查询训练查询条件的图注意力网络得到代理分数，并用密度感知主动学习探索不确定分数区域、选择性标注信息量大的文档、重训代理并在额外标注不太可能改进级联时提前停止；阈值校准阶段按查询的分数分布自适应采样校准集。实验显示，OASIS 在准确率 0.9 下把在线延迟降低 1.75–5.42 倍，LLM 处理的文档数比最强方法减少 35%–75%。
- [arXiv:2611.24518](https://arxiv.org/abs/2611.24518)

## 社交媒体

### 20. Wren AI 官方 Facebook 发布与 Phison 的本地部署 GenBI 合作（11/19）
Wren AI 官方 Facebook 账号 11 月 19 日发帖宣传与 Phison 的合作：把 Wren AI 生成式 BI 集成进 Phison AI Data Platform 本地一体机，模型在客户自有环境内运行、数据不出墙，SC26 Phison 5413 号展位现场演示。实质通稿发布于 11 月 17 日，本条仅为当日社交媒体发帖。
- [Facebook @getwrenai（11/19）](https://www.facebook.com/getwrenai/posts/pfbid026Yx4L1ADJqhhrewUpYRisLJk6zoVz8uoW43HgyyKvJY3m4dT8oG1TJdz1ky8x3Wul)
- [EINPresswire 通稿（11/17）](https://www.einpresswire.com/article/957164436/wren-ai-collaborates-with-phison-on-on-premises-ai-analytics-at-sc26)

本期检索范围内，国内大厂（阿里云、火山引擎、腾讯云、百度智能云、网易智企、华为云、京东云）与国内独立厂商（Aloudata、AskTable、数花智算、数势科技、帆软、思迈特、观远数据、Kyligence、衡石科技）当日均无数据代理相关的新发布；中文媒体 36氪、机器之心、量子位、InfoQ、DataFunTalk、Datawhale、dbaplus、墨天轮、和鲸当日均无数据智能体直接相关的新内容；WrenAI、DB-GPT、Cube Core、Chat2DB、Vanna、Apache Gravitino、Alpha-SQL、ReFoRCE、DeepEye-SQL、LAMBDA、Data Interpreter、DeepAnalyze、DocETL 当日均无新 Release；Hugging Face Papers 11 月 19 日日榜前列除 Piccolo 外无与数据代理直接相关的论文；Spider 2.0、BIRD、DABstep、DAComp 等评测基准原作者团队当日无新动态；Anthropic 11 月 19 日上市属资本新闻，与数据工作无直接关系，未作条目；DeepSeek 第二轮融资落地属泛 AI 融资，未作条目。

## 今日回顾

ThoughtSpot 宣布 Spotter 接入 Claude Data 与 Send To ThoughtSpot 两项集成，即日起向客户开放，并推出 Customer Hosted 部署选项；Databricks 的 Genie Code CLI 正式 GA，同日介绍 11 月 5 日进入 Beta 的 Genie Migrate for Serverless，并获 A-Team 资本市场 AI 奖；Google 发布 Gemini 4 Neon，Coding Agent Index 58.6 分排第 1；OpenAI 发布内部 agent 报告，coding agent 独立完成 2–4 小时研究任务的成功率从 3 月的 23% 升至 10 月的 46%；Oracle 推出 Life Sciences AI Agents；arXiv 同日上线 MARS、Value Semantics Layer、ReflectRec、CONCORD-Rec、Piccolo、CaDO、受治理的 ML 实验智能体评估、When Do LLMs Model the Right Target? 与 OASIS 九篇论文；Tableau Studio 服务器版按计划定于今日上线，截至发稿未见官方确认。
