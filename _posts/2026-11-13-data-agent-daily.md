---
layout: post
title: "Data Agent Daily — 2026-11-13"
author: dad
date: 2026-11-13
image: "assets/images/covers/2026-11-13.svg"
description: "OpenAI 在 11 月 12 日发布 Amplitude 客户案例：产品智能体 Wave 约 80% 由 OpenAI 模型驱动，Amplitude 估计它能把产品改进周期从约 1 个月压缩到 1–2 天，官网首页个性化提示卡 A/B 测试使卡片带来的消息量一天内提升 160%。"
categories: ["Data Agent Daily"]
tags: ["data-agent", "news"]
comments: false
---

## 今日速览

- OpenAI 在 11 月 12 日发布 Amplitude 客户案例：产品智能体 Wave 约 80% 由 OpenAI 模型驱动，Amplitude 估计它能把产品改进周期从约 1 个月压缩到 1–2 天，官网首页 A/B 测试使卡片带来的消息量一天内提升 160%。
- Google 在 11 月 11 日宣布 BigQuery measures GA：把 BI 度量与知识图谱统一在同一模型里，仪表盘与 AI 智能体共用同一度量定义，Conversational Analytics 与 Data Agent Kit 开箱支持。
- Anthropic 在 11 月 12 日把自托管 Claude Managed Agents 推入私人 beta：企业可在自有云或本地运行整套智能体服务，模型调用仍走所选供应商，接入须经客户团队申请。
- AppsFlyer 在 11 月 13 日扩展 Agent Hub 与 MCP 工具：可按营销工作流自定义智能体、拉取事件级数据并按计划推送洞察，首个可执行智能体为 Apple Ads Share of Voice Agent。
- LangChain 在 11 月 12 日完成 3 亿美元融资、估值 30 亿美元，CapitalG 领投，资金用于扩展智能体监控、评估与部署平台 LangSmith，员工计划从 435 人扩至 850 人。
- arXiv 11 月 12 日上线 FlinkEval：流式 SQL 自然语言接口评测基准，含 3,903 组问答–SQL 对、45 个行业领域，在 Confluent Cloud Apache Flink 上执行验证。
- arXiv 11 月 12 日上线 AgentSSL：研究机器学习工程智能体能否利用无标签数据，12 个设置中 8 个超过最强人工基线、最高提升 21.8%，并发布含 16,977 个程序的 ProgramSelectBench。
- arXiv 11 月 12 日上线 SchemaBridge：902 个 schema 的 Text2Schema 基准，需求欠指定时无一模型参照完整性 F1 超过 0.27，要求完整描述后 GPT-5.4-mini 的参照 F1 从 0.228 升至 0.909。
- arXiv 11 月 12 日上线迁移智能体审计：带证据分级经验记忆的 Oracle→PostgreSQL 迁移智能体在 1,833 组样本上记忆仅带来 0.015 的参照符合度提升，72% 的留出样本存在参考泄露。
- arXiv 11 月 12 日上线 KuaiRecV2：快手面向大规模持续学习、多样性与多任务推荐的新基准，含 30 天长期交互记录与动态视频候选池。
- arXiv 11 月 12 日上线 ReSID：生成式推荐长尾检索方法，宣称达到长尾检索 SOTA，已部署于生产系统服务主流量。
- arXiv 11 月 12 日上线 TriGen：面向触发式推荐的生成式范式，离线评测一致优于基线，六国市场线上 A/B 测试后已全量上线。
- arXiv 11 月 12 日上线 TraGR：行为感知生成式推荐框架，用于用户行为轨迹预测，在 4 个公开数据集上一致优于最强基线。
- arXiv 11 月 12 日上线 Sheaf-LightGCN：层论启发的结构化打分扩展，4 个数据集上排序质量变化小且因数据集而异，作者称实验未证明层几何本身带来因果收益。

## 公司发布 / 官方博客

### 1. OpenAI 发布 Amplitude 客户案例：产品智能体 Wave 约 80% 由 OpenAI 模型驱动（11/12）
OpenAI 在 11 月 12 日发布 Amplitude 客户案例：Amplitude 的主动式产品智能体 Wave 约 80% 由 OpenAI 模型驱动。团队向 Wave 交代一个产品方向与要改进的目标和指标，Wave 综合 Amplitude 产品分析数据、会话回放、客户反馈与代码，识别并排序改进机会、起草技术方案，交由 Codex 等编码智能体执行，随后度量改动效果。模型按任务分工：GPT-6.1 Sol 负责机会管理与深入代码和数据的调查，GPT-6 Luna 处理扫描代码与小型评估等高频低成本任务，GPT-Image-2.5 Flare 用会话回放截图作参考生成产品线框图。Amplitude 估计，Wave 能把产品改进周期从约 1 个月压缩到 1–2 天；已上线的改动中，四分之一在 Wave 发现机会当天上线，一半在 4 天内、三分之二在一周内上线。Amplitude 自家官网的例子：100 次会话回放样本中，80 名用户直接输入问题、仅 12 人点了通用提示卡；Wave 建议按用户近期的图表、仪表盘或来源页面个性化提示卡，A/B 测试后经提示卡发送的消息一天内比对照组提升 160%——Amplitude 博客注明，这是 7 月实验的初步读数（个性化卡片每 100 次曝光 2.43 次发送、通用卡片 0.94 次），仍需进一步验证。Wave 目前处于 beta，客户可自选自动化程度：多数团队把 bug 修复直接交给编码智能体，新功能与较大改动仍经人工审核。Amplitude 的内部评估中，GPT-6.1 Sol 在机会调查器上得 4.06/5，高于三个未具名对照模型的 3.62、3.52 与 2.94，中位调查时间 54 分钟；在数据科学智能体评估中得 67.5/100，略低于另一领先模型的 69.3，但单次派发平均模型成本为 1.28 美元、对 2.63 美元。
- [OpenAI 客户案例（11/12）](https://openai.com/index/amplitude)
- [Amplitude 官方博客（11/12 更新）](https://corpsite.amplitude.com/blog/wave-product-improvements)

### 2. Google 宣布 BigQuery measures GA：BI 度量与知识图谱统一在同一模型里（11/11）
Google 在 11 月 11 日宣布 BigQuery measures GA：度量直接定义在 BigQuery Graph 的图实体上，BI 仪表盘与 AI 智能体共用同一套受治理的度量定义。GA 新增复合与派生度量（MEASURE() 与 AGG() 组合）、跨多事实表查询（GRAPH_EXPAND 的 start_node 参数隔离各事实表、避免交叉相乘膨胀）以及“粒度锁定”度量；度量定义可用 OPTIONS 子句附带业务描述、同义词与自定义元数据；图与度量元数据自动进入 Knowledge Catalog，可用 BQ.SHOW_GRAPH_EXPAND_SCHEMA 在运行时把图 schema 以 JSON 形式暴露给智能体。Looker 的 LookML 模型可编译为原生 BigQuery Graph 模型，Conversational Analytics 与 Data Agent Kit 对统一后的图与度量定义开箱支持。
- [Google Cloud 官方博客（11/11）](https://cloud.google.com/blog/products/data-analytics/bigquery-measures-ga-unifying-bi-metrics-and-knowledge-graphs)

### 3. Anthropic 自托管 Claude Managed Agents 进入私人 beta（11/12）
Anthropic 在 11 月 12 日宣布自托管 Claude Managed Agents 进入私人 beta：企业可在自有云或本地运行整套 Managed Agents 服务，包括智能体编排服务（cma-server）、沙箱、凭证与会话历史，持久化存储需 PostgreSQL 16 或更高版本；服务器提供与托管版相同的 Managed Agents API，Claude SDK 与 ant CLI 可直接连接。模型本身不搬进企业内网：每次模型调用仍发往客户选定的供应商，默认为 Anthropic，也可选 Amazon Bedrock、Google Cloud、Microsoft Foundry 或自有网关。部分托管功能暂缺，包括定时部署、webhook、dreams、Files API 与云环境；接入仅限符合条件的组织，须经 Anthropic 客户团队申请，未公布价格与 GA 日期。
- [CellCog 深度解析（11/12，依据 Anthropic 公告与官方文档）](https://cellcog.ai/blog/claude-managed-agents-self-hosted/)

### 4. AppsFlyer 扩展 Agent Hub 与 MCP 工具：营销智能体可拉取事件级数据并执行操作（11/13）
AppsFlyer 在 11 月 13 日宣布扩展 Agent Hub 与 MCP 工具：Agent Hub 现可按营销工作流自定义智能体，智能体拉取事件级数据、分析后按设定计划把洞察推送到 Slack 或邮件，也可做根因分析并推荐下一步行动；首个可执行智能体为 Apple Ads Share of Voice Agent，按关键词与地区估算声量份额、偏离目标时推荐出价调整，经批准后直接在 Apple Ads 执行改动，目前处于内测、须经客户成功经理开通。MCP 方面，Protect360 数据、创意级花费与转化留存数据、OneLink 创建与合作伙伴集成配置现可接入自有 AI 工具。
- [MarTech Series 通稿（11/13）](https://martechseries.com/sales-marketing/marketing-automation/appsflyer-expands-agentic-ai-and-mcp-tools-to-empower-marketers-with-trusted-automation/)

## 新闻网站

### 5. LangChain 融资 3 亿美元、估值 30 亿美元（11/12）
LangChain 在 11 月 12 日完成 3 亿美元融资、估值 30 亿美元，由 Alphabet 增长基金 CapitalG 领投，IVP、Sapphire Ventures 跟投，GIC 与 DFJ Growth 新加入；估值约为 2025 年 10 月 B 轮 12.5 亿美元的 2.4 倍。资金用于扩展智能体监控、评估与部署平台 LangSmith 并招聘，员工计划从 435 人扩至 850 人（2027 年底前）。该消息由《华尔街日报》首报。
- [Dealroom 报道（11/12）](https://dealroom.co/news/172300-langchain-raises-300m-tripling-its-valuation-to-3b/)

## 论文 / arXiv

### 6. FlinkEval：流式 SQL 自然语言接口评测基准（arXiv 11/12 上线，11/12 提交）
arXiv 11 月 12 日上线的论文《FlinkEval: A Synthetic Corpus for Evaluating Natural Language Interfaces to Streaming SQL》（arXiv:2611.17093，11 月 12 日提交，IBM Research 团队）针对流式 SQL 的自然语言接口提出执行验证的合成基准：3,903 组问答–SQL 对、45 个行业领域与 45 个语义标签，在 Confluent Cloud Apache Flink 上执行验证，覆盖窗口、时序连接、模式匹配、嵌套类型与数据操作；另设七级问题表述阶梯，考察语义保持的改写与欠指定请求。基线评测显示，模型在模式组合与需求表述上仍有困难。
- [arXiv:2611.17093](https://arxiv.org/abs/2611.17093)

### 7. AgentSSL：机器学习工程智能体能否利用无标签数据（arXiv 11/12 上线，11/12 提交）
arXiv 11 月 12 日上线的论文《AgentSSL: Can MLE Agents Leverage Unlabeled Data?》（arXiv:2611.17323，11 月 12 日提交）把半监督学习建模为程序搜索问题：智能体在弱反馈与同等算力下合成结合已有半监督技术的代码，在 12 个设置中的 8 个上超过最强人工基线、最高提升 21.8%；但程序选择是关键瓶颈，按智能体反馈指标选择时性能最多下降 47%。论文同时发布 ProgramSelectBench 基准，含 16,977 个智能体生成与人工编写的半监督程序，并在真实生态检测任务上验证。
- [arXiv:2611.17323](https://arxiv.org/abs/2611.17323)

### 8. SchemaBridge：LLM 能否从自然语言需求设计关系 schema（arXiv 11/12 上线，11/12 提交）
arXiv 11 月 12 日上线的论文《[Experiment, Analysis, and Benchmark] How well do LLMs comprehend and design relational database schemata?》（arXiv:2611.17044，11 月 12 日提交）提出 SchemaBridge 基准：902 个 schema，评测 LLM 从自然语言需求设计关系 schema（Text2Schema）、口头化 schema 与往返保真度。评测 6 个模型后发现：人工需求普遍欠指定，无一模型的参照完整性 F1 超过 0.27；要求模型给出完整描述后，GPT-5.4-mini 的参照 F1 从 0.228 升至 0.909。
- [arXiv:2611.17044](https://arxiv.org/abs/2611.17044)

### 9. 迁移智能体审计：经验记忆是否让 Oracle→PostgreSQL 迁移智能体真正学习（arXiv 11/12 上线，11/12 提交）
arXiv 11 月 12 日上线的论文《Does a Self-Learning Migration Agent Learn? An Audited Evaluation of Evidence-Graded Experience Memory for Oracle-to-PostgreSQL Migration》（arXiv:2611.16143，11 月 12 日提交）审计带证据分级经验记忆的迁移智能体是否真正从经验中学习：在 1,833 组文档衍生样本上，记忆仅带来 0.015 的参照符合度提升；审计发现 367 个留出样本中有 264 个（72%）与训练共享了 PostgreSQL 参考，去泄露后记忆效应降至 0.002、统计上不显著；一个无模型的最近邻复制基线（参照符合度 0.222）反而优于所有 LLM 系统（最高 0.163）。人工把关的修复循环把可证明正确的单元从 98/216 提升到 167/224。
- [arXiv:2611.16143](https://arxiv.org/abs/2611.16143)

### 10. KuaiRecV2：面向大规模持续学习、多样性与多任务推荐的新基准（arXiv 11/12 上线，11/12 提交）
arXiv 11 月 12 日上线的论文《KuaiRecV2: Benchmarking Large-Scale Continual Learning for Diversified and Multi-task Recommendation》（arXiv:2611.16795，11 月 12 日提交，快手团队，已被 NeurIPS 2026 接收）针对离线评测与线上效果不一致的三个成因（动态物品池下的持续学习、准确率–多样性权衡、多任务奖励平衡）设计评测：提供百万级多模态物品信息与 30 天长期交互记录的工业级数据集与动态视频候选池，评测把检索准确率、多样性与多任务表现纳入同一评分体系，仅当全部指标都提升时才算有效改进。
- [arXiv:2611.16795](https://arxiv.org/abs/2611.16795)

### 11. ReSID：生成式推荐中的长尾检索（arXiv 11/12 上线，11/12 提交）
arXiv 11 月 12 日上线的论文《ReSID: Rethinking Long-Tail Retrieval in Generative Recommendation through Item Reachability》（arXiv:2611.16404，11 月 12 日提交）首次系统研究生成式推荐全流程中的长尾可达性，提出 ReSID：并行长语义 ID、去流行度偏差的束搜索与部分语义 ID 匹配恢复；在保持整体准确率与更低延迟的同时达到长尾检索的 SOTA。论文称该方法已部署于生产系统、服务主流量，并公开了完整代码与模型检查点。
- [arXiv:2611.16404](https://arxiv.org/abs/2611.16404)

### 12. TriGen：面向触发式推荐的生成式范式（arXiv 11/12 上线，11/12 提交）
arXiv 11 月 12 日上线的论文《TriGen: A Generative Paradigm for Trigger-Induced Recommendation》（arXiv:2611.16395，11 月 12 日提交）针对“用户一次点击触发即时推荐”的触发式推荐场景提出生成式范式 TriGen：通过校准尾部注入、动态门控与位置特异变换，协调长期偏好与即时触发意图；离线评测一致优于基线，六个国家市场的线上 A/B 测试录得收入与 GMV 提升后已全量上线。
- [arXiv:2611.16395](https://arxiv.org/abs/2611.16395)

### 13. TraGR：面向用户行为轨迹预测的行为感知生成式推荐（arXiv 11/12 上线，11/12 提交）
arXiv 11 月 12 日上线的论文《From Tokens to Behaviors: Rethinking Generative Recommendation for User Trajectory Prediction》（arXiv:2611.16159，11 月 12 日提交）提出行为感知生成式推荐框架 TraGR：以行为级并行解码语义 ID、循环状态建模行为转移，并用概率反馈与关系感知轨迹学习缓解生成式推荐的训练–推理差距，用于用户行为轨迹预测；在 4 个公开数据集上，TraGR 在不同预测跨度上一致优于最强基线。
- [arXiv:2611.16159](https://arxiv.org/abs/2611.16159)

### 14. Sheaf-LightGCN：层论启发的结构化打分扩展（arXiv 11/12 上线，11/12 提交）
arXiv 11 月 12 日上线的论文《Sheaf-Inspired Structured Scoring Extensions of LightGCN for Collaborative Filtering》（arXiv:2611.17226，11 月 12 日提交）在三层 LightGCN 骨干上加层论启发的结构化打分扩展（对角、低秩、全矩阵残差打分器），在 Amazon-Book、Gowalla、MovieLens-1M、Yelp2018 上测试：排序质量变化小且因数据集而异，覆盖度有时显著变化；作者明确说明，实验未证明层几何本身带来因果收益。
- [arXiv:2611.17226](https://arxiv.org/abs/2611.17226)

本期检索范围内，社交媒体与中文媒体层当日未见可核实的数据智能体新内容；监测名单内其余厂商、研究团队与评测基准机构在过去 24 小时内未见可核实的新动态；监测名单内其余开源项目当日未见实质 Release。

## 今日回顾

OpenAI 在 11 月 12 日发布 Amplitude 客户案例：产品智能体 Wave 约 80% 由 OpenAI 模型驱动，Amplitude 估计产品改进周期从约 1 个月压缩到 1–2 天，官网首页 A/B 测试使卡片消息量一天内提升 160%；Google 在 11 月 11 日宣布 BigQuery measures GA，BI 度量与知识图谱统一在同一模型里；Anthropic 在 11 月 12 日把自托管 Claude Managed Agents 推入私人 beta；AppsFlyer 在 11 月 13 日扩展 Agent Hub 与 MCP 工具；LangChain 在 11 月 12 日完成 3 亿美元融资、估值 30 亿美元；arXiv 11 月 12 日上线 9 篇论文，涵盖流式 SQL 评测基准（FlinkEval）、机器学习工程智能体半监督学习（AgentSSL）、Text2Schema 基准（SchemaBridge）、迁移智能体审计，以及 KuaiRecV2、ReSID、TriGen、TraGR 与 Sheaf-LightGCN 五篇推荐相关论文；社交媒体与中文媒体层当日未见可核实的数据智能体新内容。
