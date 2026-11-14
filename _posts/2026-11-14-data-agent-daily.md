---
layout: post
title: "Data Agent Daily — 2026-11-14"
author: dad
date: 2026-11-14
image: "assets/images/covers/2026-11-14.svg"
description: "Google Cloud 在 11 月 13 日宣布 BigQuery 与 Looker 的 AI 智能体可观测性与治理扩展：对话日志与 Conversational Analytics API 进入 GA，遥测统一落入客户自有 BigQuery 表，ADK 与 LangGraph 自定义智能体可一行 SDK 接入。"
categories: ["Data Agent Daily"]
tags: ["data-agent", "news"]
comments: false
---

## 今日速览

- Google Cloud 在 11 月 13 日宣布 BigQuery 与 Looker 的 AI 智能体可观测性与治理扩展：对话日志与 Conversational Analytics API 进入 GA，遥测统一落入客户自有 BigQuery 表，ADK 与 LangGraph 自定义智能体可一行 SDK 接入。
- Databricks 在 11 月 13 日发布 OpenAI 企业落地三条路径：ChatGPT 经 Genie 插件问数、Codex 经 Unity Gateway 集中治理、自定义智能体经 Model Serving 与 Databricks Apps 交付。
- Databricks 的 Genie ZeroOps 在 11 月 12 日进入 Beta：后台智能体监控 jobs、pipelines 与 tables，查根因并提修复建议，生产变更仍由人工把关。
- digna 在 11 月 13 日发出通稿，介绍 2026.11 版本：digna Agentic 让 Claude 等 AI 智能体经 MCP Server 查数据质量，另新增 Data Reconciliation 与 digna Engine。
- InfoQ 在 11 月 13 日报道 Google 开源的 AQuA：生产智能体故障诊断工具，每轮最多抽样 1,000 段会话，32 段对话受控回放测出 42 项发现、9 个候选问题，验证后留下 6 项确认问题。
- arXiv 11 月 13 日上线 SynthCorp：为数据智能体造基准的平台，生成 7 个数据资产、256 个任务，数据资产最多含 1,000 张运营表，gold 程序经模拟日志因果溯源验证。
- arXiv 11 月 13 日上线 HeriKGQA：文化遗产传感器数据的知识图谱问答，500 个问题上准确率 99.0%，比最强基线高 18.2 个百分点，速度快约 4 倍。
- arXiv 11 月 13 日上线 RMIT-ADM+S 的 TREC RAG 2026 参赛报告：7 个研究智能体 run 中 6 个超过 track 中位数，最佳 run 的 Batch-1 vital 覆盖率 0.892，并列 track 最高。
- arXiv 11 月 13 日上线 CURATOR：微调决策模型为 RAG 做细粒度证据选择，候选数增加时仍保持证据判别力，尤其在上下文有限时提升下游 RAG 表现。
- arXiv 11 月 13 日上线 LAAM：主动学习近似 LLM 排序，详细查询下达到 DeepSeek 重排 87% 的平均 P@10，单查询能耗仅 3.3%。
- arXiv 11 月 13 日上线 CaST：带最优性间隙界的约束向量搜索校准早停，百万级数据集上回放成本至多为同类最优的 1.132 倍。
- arXiv 11 月 13 日上线 HyperPage：从搜索智能体日志学习磁盘向量索引的页布局，7 种缓存预算下比 MARGO 少读 5.2%–21.2% 的页。

## 公司发布 / 官方博客

### 1. Google Cloud 宣布 BigQuery 与 Looker 的 AI 智能体可观测性与治理扩展（11/13）
Google Cloud 在 11 月 13 日宣布扩展 Google Data Cloud 的 AI 智能体可观测性与评估能力：统一遥测框架覆盖自家 Conversational Analytics 数据智能体与 ADK 或 LangGraph 构建的自定义智能体，遥测统一落入客户自有 BigQuery 表。开箱即用的 Conversational Analytics 智能体自动发出遥测，经 Gemini Enterprise 的 agent-to-agent（A2A）工作流（现 GA）路由到 BigQuery 数据智能体的查询会发送 Cloud Monitoring 指标、Cloud Trace spans 与 BigQuery 对话日志；ADK 或 LangGraph 自定义智能体可通过一行 SDK 接入流式传输同样的结构化遥测。对话日志进 BigQuery（GA）、Conversational Analytics API（GA，含常开管理审计日志与可选数据读取审计日志）、BigQuery Studio 预置看板（GA，跟踪用量、活跃会话、热门知识源与延迟）与 Looker System Activity 看板（GA，跟踪参与度与 token 用量）均已进入 GA，用户评分与查询回顾仍为 preview。运营遥测与对话内容分离管理：运营指标与脱敏后的 trace span 不含用户提示、模型回复、内部思考与生成 SQL；需要逐字审计时，智能体负责人可按智能体 opt-in 对话日志，由 Google 托管服务智能体经 BigQuery Storage Write API 把提示、回复与逐轮遥测写入客户自有 `agent_events` 表，知识源使用行级安全、列级策略标签或动态脱敏时触发 fail-closed 检查跳过记录。成本侧，每轮对话日志记录输入、输出、思考、缓存与总 token 数及总延迟；可配置每查询 BigQuery 字节扫描上限（`big_query_max_billed_bytes`，用 dry-run 估算拦截超大查询），每日输入输出 token 配额为 preview。评估侧，开源评测工具 Prism 可测试以 BigQuery 表或 Looker Explores 为依据的 Conversational Analytics 智能体，评测结果可流入按日分区的 BigQuery 表；BigQuery 内一手智能体评测以 API 与 Colab 笔记本形式提供 preview。
- [Google Cloud 官方博客（11/13）](https://cloud.google.com/blog/products/data-analytics/enterprise-ai-agent-observability-with-bigquery-and-looker)

### 2. Databricks 发布 OpenAI 企业落地三条路径：ChatGPT 问数、Codex 集中治理、自定义智能体（11/13）
Databricks 在 11 月 13 日发布 OpenAI 企业落地指南，说明在受治理的公司数据上使用 OpenAI 工具的三条路径。路径一面向业务用户：经 Databricks Genie 插件在 ChatGPT 里用自然语言问数，Genie Ontology 提供经批准的度量定义，查询在 Databricks 内运行、返回图表并附来源链接，答案只限用户已有权限的数据；SAP ERP 数据也可经此插件进 ChatGPT，Databricks 在 11 月 11 日 release notes 中列出该插件，ChatGPT 经 MCP 把问题发给 Genie One。路径二面向工程师：Codex 不直连 OpenAI，改为经 Unity Gateway 集中治理，安装 Unity Gateway CLI 后运行 `ug codex`，OpenAI key 留在网关内、请求按团队记账；Unity Gateway 本身 GA，文档中的 SQL、沙箱与联网搜索工具及 Unity Gateway skills 仍为 beta。路径三面向自定义智能体：Model Serving 在受治理数据旁运行 OpenAI 模型、无需外部 API key，可用 Agent Bricks 搭建或用 OpenAI Agents SDK 以 Databricks Apps 交付，Lakebase 保存记忆与状态。背景为双方 2025 年 9 月 25 日宣布的多年合作协议，价值 1 亿美元，原生 OpenAI 模型覆盖 2 万多名 Databricks 客户。
- [Databricks 官方博客（11/13）](https://www.databricks.com/blog/openai-and-databricks-enterprise-ai-your-governed-data)
- [ERP News：Genie 插件把 SAP ERP 数据带入 ChatGPT（11/13）](https://erpnews.com/databricks-genie-sap-erp-data-chatgpt/)

### 3. Databricks Genie ZeroOps 进入 Beta：后台智能体盯着数据管道（11/12）
Databricks 在 11 月 12 日把 Genie ZeroOps 推入 Beta：后台智能体监控所选 jobs、pipelines 与 tables，检测失败与数据质量问题、调查根因并提出修复建议，生产变更仍由人工把关。ZeroOps 的概念在 6 月 16 日首次公布，本次 Beta 是可用性节点而非首次发布。Beta 需工作区管理员在 Previews 页开启，仅在单个工作区内运行，监控对象限操作者拥有 OWNER、CAN MANAGE 或 CAN VIEW 权限的资产；表数据质量检测需另行计费的数据质量监控；Beta 不检测成本或性能回归，不监控模型与应用等其他资产类型，且不符合 HIPAA。
- [Databricks 官方 release notes（11/12）](https://docs.databricks.com/aws/en/release-notes/product/2026/november)
- [Databricks Genie ZeroOps 官方文档](https://docs.databricks.com/aws/en/zeroops/)

### 4. digna 发布 2026.11：digna Agentic 让 AI 智能体经 MCP 查数据质量（11/13）
digna 在 11 月 13 日发出通稿，介绍 2026.11 版本的三项新能力。digna Agentic 让 Claude 等 AI 智能体经 digna MCP Server 与 digna 协作：智能体可管理项目、数据源、规则、检查计划与订阅，把检查状态读到单条检查，并沿告警追到数据源、片段与背后的具体数值；经 MCP Server 可接入 ChatGPT、Claude、Gemini 与开源模型，员工可直接向熟悉的 AI 助手提问已监控的数据质量。同版新增 digna Data Reconciliation（检查目标表是否仍与源头一致）与 digna Engine（按连接设定 profiling 位置），并为数据验证带来跨连接参照完整性检查。三项能力即日起向现有客户提供，支持 Teradata、Snowflake、Databricks、Oracle、SQL Server、PostgreSQL 与 BigQuery。
- [digna 官方博客](https://www.digna.ai/digna-release-2026-11-agentic-data-reconciliation-engine)
- [MENAFN 通稿（11/14）](https://menafn.com/1111960839/digna-introduces-agentic-AI-to-make-enterprise-data-easier-to-understand)

## 新闻网站

### 5. InfoQ 报道 Google 开源 AQuA：给生产智能体做故障诊断（11/13）
InfoQ 在 11 月 13 日报道 Google 开源的 AQuA（Ambient Quality Agent）：以 ADK 构建的开源参考实现，并行运行于受观测智能体之外、不插入用户请求处理路径，读取 Cloud Trace、Cloud Logging 或 BigQuery 遥测，每轮最多抽样 1,000 段近期会话，经抽样、评审、聚类、验证、跟踪五阶段处理。AQuA 针对传统基础设施监控漏掉的静默质量回归，例如智能体忽略用户偏好、跳过必需工具调用却返回成功响应；发现按 NEW、RECURRING 或 14 天未见自动 RESOLVED 跟踪，根因分析对照部署时冻结的代码快照、可定位到文件行号；AQuA 不自动修复、不开 PR。Google 用多智能体旅行应用的 32 段对话做受控回放测试：42 项发现归为 9 个候选问题，验证后排除 3 组、留下 6 项确认问题，包括跳过座位可用性检查、交接任务时丢失旅客的纯素偏好；作者注明这是受控回放结果、非正式流量。AQuA 最早于 10 月 8 日随 google/adk-recipes 首次发布，10 月 26 日并入约 3.5 万行的 v0.2.0 更新。
- [InfoQ 报道转载（11/13，作者 Leela Kumili）](https://news.lavx.hu/article/google-open-sources-aqua-to-diagnose-production-ai-agent-failures)
- [TechToDaily 中文报道（11/14）](https://techtodaily.com/news-infoq-e47175ce70/)

## 论文 / arXiv

arXiv 11 月 14 日（周六）无新上线，以下论文出自 11 月 13 日一期。

### 6. SynthCorp：为数据智能体造基准的平台（arXiv 11/13 上线，11/10 提交）
arXiv 11 月 13 日上线的论文《SynthCorp: A Platform for Creating Benchmarks for Data Agents》（arXiv:2611.14765，11 月 10 日提交，Jiani Zhang、Manav Garg、Eugenie Lai、Cheng Zhen、Eva Sharma、Yang Pan、Yaming Lin、Alon Halevy 等）针对 LLM 数据智能体基准快速饱和、无法定向测能力的问题，提出用模拟业务事件随时间产生并修改企业数据来合成可定制数据资产与基准：每个数据资产含关系数据库、文档库与数据目录，配评估任务与可执行 gold 程序。论文用 SynthCorp 生成首批基准：7 个数据资产（最多 1,000 张运营表）、256 个任务、5 个领域；数据资产通过确定性管道检查（外键违规、未声明写入、循环违规、数据库执行失败），错误率近零；用模拟日志中的因果溯源审计候选查询、无需人工标注验证 gold 程序。评测 3 个模型 × 4 种数据上下文设置，基准能区分数据上下文与模型档位；多事件复合任务暴露了 SOTA 智能体的推理失败。SynthCorp v1.0，基准即将发布。
- [arXiv:2611.14765](https://arxiv.org/abs/2611.14765)

### 7. HeriKGQA：文化遗产传感器数据的知识图谱问答（arXiv 11/13 上线，11/11 提交）
arXiv 11 月 13 日上线的论文《HeriKGQA: Grounded Knowledge-Graph Question Answering over Cultural Heritage Sensor Data》（arXiv:2611.15904，11 月 11 日提交）针对文化遗产地传感器数据查询需要数据库专业知识的问题，提出 HeriKGQA：LLM 只负责理解问题与组织答案，计算交给 SPARQL 与确定性代码；问题解析为受遗产本体（W3C SOSA/SSN 对齐 CIDOC-CRM）约束的意图，配时间、空间与异常事实的 grounding 层，LLM 每步加纠错。5 个遗产地的真实数据、500 个问题上，HeriKGQA 准确率 99.0%，比使用同一 LLM、同一异常规则与答案约定的最强基线高 18.2 个百分点，速度快约 4 倍；去掉 grounding 后准确率降 12.2 点，异常问题从 99% 降至 66%。论文报告了开发经验与实际部署情况，已投 NAACL 2027 industry track。
- [arXiv:2611.15904](https://arxiv.org/abs/2611.15904)

### 8. RMIT-ADM+S 参加 TREC RAG 2026：研究智能体、检索消融与开源权重复现（arXiv 11/13 上线，11/12 提交）
arXiv 11 月 13 日上线的论文《RMIT-ADM+S at TREC RAG 2026: Research Agents, Retriever Ablations, and Open-Weight Replication》（arXiv:2611.16425，11 月 12 日提交）报告 RMIT-ADM+S 队参加 TREC 2026 RAG track 的情况：用 ClimbMix 语料提交 7 个研究智能体 run（专有 OpenAI 与开源权重模型），探索检索策略、写作模型与智能体工作流；预提交消融显示写作模型选择与相邻 chunk 扩展是答案质量的主要因素。NIST 官方评测中，7 个 run 有 6 个在全部三套 rubric/nugget 集合上超过 track 中位数；最佳 run brief-hybrid 的全项覆盖率居队内最高，并列 Batch-1 vital 覆盖率 track 最高（0.892）；人工并排偏好因批次而异：开源权重 owa-glm5 在 Batch 1 领先，sol-research-first 在 Batch 2 领先。
- [arXiv:2611.16425](https://arxiv.org/abs/2611.16425)

### 9. CURATOR：用决策模型为 RAG 做细粒度证据选择（arXiv 11/13 上线，11/12 提交）
arXiv 11 月 13 日上线的论文《CURATOR: Scalable Fine-grained Evidence Selection for Retrieval-Augmented Generation using Decision Models》（arXiv:2611.16366，11 月 12 日提交）针对 RAG 把整段检索文本交给 LLM、但只有少数片段含证据的问题，提出 CURATOR：微调决策模型，从大候选池中选取不同数量的支撑片段；逐片段判断需反复处理同一文本、成本高，预训练决策模型可一次评估多个片段，但候选一多判别力下降。CURATOR 在候选数增加时仍保持较强的证据判别力，跨任务与文档域泛化，尤其在上下文有限时提升下游 RAG 表现。
- [arXiv:2611.16366](https://arxiv.org/abs/2611.16366)

### 10. LAAM：用主动学习近似 LLM 排序，节能检索长查询（arXiv 11/13 上线，11/12 提交）
arXiv 11 月 13 日上线的论文《LAAM: Active Learning of Approximate LLM Ranking for Energy-Efficient Retrieval of Long Queries》（arXiv:2611.16488，11 月 12 日提交）针对词汇检索快而省电、LLM 懂长查询语义但推理成本与能耗高的问题，提出 LAAM：在语义检索与 LLM 检索之间加轻量学习预测器，主动学习循环只让 LLM 标注信息量最大的文档。TREC Robust 2004 上用 Lucene BM25 检索与 DeepSeek v3 作 LLM：详细查询下，LAAM 达到 DeepSeek 重排 87% 的平均 P@10（0.459 对 0.526），单查询能耗仅 3.3%；平均精度上与 DeepSeek 无统计差异，MAP 上仍有差距。
- [arXiv:2611.16488](https://arxiv.org/abs/2611.16488)

### 11. CaST：带最优性间隙界的约束向量搜索校准早停（arXiv 11/13 上线，11/12 提交）
arXiv 11 月 13 日上线的论文《Calibrated Early Termination with Bounded Optimality Gaps for Constrained Vector Search》（arXiv:2611.16148，11 月 12 日提交）针对向量搜索作为推荐与 RAG 的检索层、且许多应用限制每个类别可贡献的答案数的问题，研究带约束的 k 近邻查询早停：图索引 best-first 遍历的停止点决定成本与答案是否精确，已有学习型早停只优化平均召回、不保证精确答案。CaST 把风险约束停止化为序多面体上的线性规划，用拉格朗日对偶给出同风险水平下最优规则的下界；固定序列二项检验校准，失败概率至多 ε、置信度 1−δ。百万级两个数据集上回放成本至多为同类最优的 1.132 倍（风险 0.03–0.10，95% 联合置信度）；同风险目标下比其余校准规则快 4.8%–45.5%。
- [arXiv:2611.16148](https://arxiv.org/abs/2611.16148)

### 12. HyperPage：从搜索智能体日志学习磁盘向量索引的页布局（arXiv 11/13 上线，11/12 提交）
arXiv 11 月 13 日上线的论文《HyperPage: Learned Page Layouts for Disk-Resident Graph Vector Indexes》（arXiv:2611.16149，11 月 12 日提交）针对 DiskANN 类磁盘图索引把向量与边存为 SSD 页记录、搜索的页读取量取决于页布局的问题，提出 HyperPage：强化学习训练的搜索智能体反复查询同一索引，每次图遍历可记录展开的记录；HyperPage 用已完成一次运行的日志为声明的内存预算重排页布局，让后续运行少读页。在 1M 与 21M 通道上，7 种缓存预算下 HyperPage 比 MARGO 少读 5.2%–21.2% 的页；1M 索引、缓存为 1% 时 MARGO 需近 3 倍预算才读同样少的页；21M 索引上每步搜索时间最多降 10.4%；结果在第二种智能体模型与第二个语料上同样成立。
- [arXiv:2611.16149](https://arxiv.org/abs/2611.16149)

本期检索范围内，社交媒体当日未见可核实的数据智能体新内容，多为 11 月 11 日 Genie 发布与 11 月 12 日 ZeroOps beta 的转载与解读；中文媒体层当日未见可核实的数据智能体新内容（AQuA 的中文报道见新闻网站一节）；Genie ZeroOps（11/12）为昨日未收录的补录条目；监测名单内其余厂商、研究团队与评测基准机构在过去 24 小时内未见可核实的新动态；监测名单内其余开源项目当日未见实质 Release。

## 今日回顾

Google Cloud 在 11 月 13 日宣布 BigQuery 与 Looker 的 AI 智能体可观测性与治理扩展，对话日志与 Conversational Analytics API 进入 GA，遥测统一落入客户自有 BigQuery 表；Databricks 在 11 月 13 日发布 OpenAI 企业落地三条路径，ChatGPT 经 Genie 插件问数、Codex 经 Unity Gateway 集中治理、自定义智能体经 Model Serving 与 Databricks Apps 交付，Genie ZeroOps 在 11 月 12 日进入 Beta；digna 在 11 月 13 日发出通稿介绍 2026.11 版本，digna Agentic 让 AI 智能体经 MCP Server 查数据质量；InfoQ 在 11 月 13 日报道 Google 开源的 AQuA，生产智能体故障诊断每轮最多抽样 1,000 段会话；arXiv 11 月 13 日一期上线 7 篇直接相关论文，涵盖数据智能体基准平台（SynthCorp）、知识图谱问答（HeriKGQA）、TREC RAG 研究智能体、RAG 证据选择（CURATOR）、节能 LLM 排序（LAAM）与向量检索层优化（CaST、HyperPage）；社交媒体与中文媒体层当日未见可核实的数据智能体新内容。
