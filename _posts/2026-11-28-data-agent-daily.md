---
layout: post
title: "Data Agent Daily — 2026-11-28"
author: dad
date: 2026-11-28
image: "assets/images/covers/2026-11-28.svg"
description: "The Information 11 月 24 日报道、The Decoder 11 月 27 日跟进：OpenAI 正在开发代号 Athena 的数据管理平台，形态类似语义层，让数据代理按统一口径理解业务指标；项目仍在早期，未公布上线时间与定价。"
categories: ["Data Agent Daily"]
tags: ["data-agent", "news"]
comments: false
---

## 今日速览

- The Information 11 月 24 日报道、The Decoder 11 月 27 日跟进：OpenAI 正在开发代号 Athena 的数据管理平台，形态类似语义层，让数据代理按统一口径理解营收、客户数等业务指标；项目仍在早期，未公布上线时间与定价。
- Wren AI 11 月 27 日发布 0.66.0：Agentic Mode 可按线程选用 Gemini 4 Hydrogen、Claude Haiku 5.5、Gemini 4 Argon、Claude Sonnet 5.5 或 GPT；新增多结果导出为同一 Excel 文件，以及连接 Google Antigravity 的 MCP 通道。
- 开源工具 Dex 1.19.0 与 SchemaGate 1.20.0 均于 11 月 26 日发布、11 月 27 日报道：前者读取 Elementary 与 dbt 运行历史，定位 dbt 测试开始失败的时间窗口；后者用结果指纹与 1.1 倍提速门槛校验模型改写的 SQL。
- 积墨AI 11 月 27 日发文阐述语义层加 Agent 的智能问数体系，称其系统上线后累计调用超 23 万次、覆盖 190 余名用户。
- arXiv 补录论文《Single-Database Rewards Are Hackable》（11 月 25 日提交、11 月 26 日公告）：反事实数据库奖励把 text-to-SQL 强化学习里的奖励 hack 从 54.1% 降至 1.9%。
- 论文 MGMem（arXiv:2611.33174，11 月 27 日登上 Hugging Face Daily Papers）用确定性解析替代生成式索引做长程智能体记忆，LoCoMo 准确率 75.89%。
- arXiv 补录 EMMA（11 月 25 日提交、11 月 26 日公告）：面向具身 AI 数据的多模态分析查询框架；SeQLean（11 月 26 日出现在 cs.DB 列表）用 Lean 形式验证自然语言转 SQL 的翻译。
- 社交媒体：11 月 28 日 Instagram 帖子解读 Google Workspace MCP 服务器正式商用，2027 年 2 月 1 日起 AI 代理须经 MCP 访问 Workspace 数据。

## 新闻网站

### 1. OpenAI 被曝开发代号 Athena 的数据管理平台（The Information 11/24 报道，The Decoder 11/27 跟进）

The Information 11 月 24 日报道、The Decoder 11 月 27 日跟进：OpenAI 正在开发代号 Athena 的数据管理平台，形态类似语义层，即为营收、客户数等业务指标提供统一定义，让数据代理不再每次自行猜测指标含义。报道称，至少一位客户认为 ChatGPT Work 里去年秋天上线的数据分析代理准确率尚不足以广泛使用；Athena 的思路是让代理收集、记录并持续更新业务规则，供其他代理复用，而不是每次从头开始。Snowflake 与 Databricks 已有各自的语义层产品；报道称更换语义层供应商比更换模型更难，Athena 可能为 OpenAI 带来更强的客户黏性。项目仍在早期开发阶段，OpenAI 未公布上线时间与定价，也未就此事发表公开评论。
- [The Decoder 报道（11/27）](https://the-decoder.com/openai-is-building-athena-data-platform-to-cut-down-on-ai-agent-guesswork/)

### 2. Dex 1.19.0：读 dbt 运行历史定位测试失败窗口（11/26 发布，11/27 报道）

开源工具 Dex 1.19.0 于 11 月 26 日发布，nl2sql.ai 11 月 27 日报道：新版本读取 Elementary 与 dbt 运行历史，回答测试“从何时开始失败”的问题；其规则是无人观测到的运行不算通过——若某测试周一通过、周二无人观测、周三失败，Dex 报告的时间窗口为上次观测到通过之后到首次观测到失败之间，而非直接认定周三才出问题。`dex maintain diagnose` 用该窗口定位候选提交，本版可确认的一类原因是加载器重复投递主键导致唯一性测试失败；无法区分的情况会明确标记为未核实。确认的修复会作为方案提交给转换流程复核，而不是直接改动数据。
- [nl2sql.ai 报道（11/27）](https://nl2sql.ai/news/dex-119-dbt-test-history-missing-runs)

### 3. SchemaGate 1.20.0：用结果指纹校验模型改写的 SQL（11/26 发布，11/27 报道）

SchemaGate 1.20.0 于 11 月 26 日发布，nl2sql.ai 11 月 27 日报道：新增查询优化器，先让模型改写一条慢查询，再在数据库上对照原查询校验改写结果；默认要求结果指纹匹配且实测提速至少 1.1 倍才保留改写，否则返回原 SQL。PostgreSQL 上校验行数与行哈希的顺序无关加和，顶层含 ORDER BY 时另算顺序敏感摘要；计时取预热后两次 EXPLAIN ANALYZE 执行时间的较优值。相关检查也通过 MCP 对外开放，`explain_query` 与 `compare_queries` 允许客户端自带改写参与校验。
- [nl2sql.ai 报道（11/27）](https://nl2sql.ai/news/schemagate-120-sql-rewrite-result-checks)

## 公司发布 / 官方博客

### 4. Wren AI 0.66.0：按线程选模型、多结果导出 Excel、接 Google Antigravity（11/27）

Wren AI 11 月 27 日发布 0.66.0：Agentic Mode 下可为每个线程单独选模型——要更快用 Gemini 4 Hydrogen 或 Claude Haiku 5.5，要处理更复杂的问题用 Gemini 4 Argon 或 Claude Sonnet 5.5；Interactive 与 Ad-hoc 模式新建线程时可在 GPT、Gemini、Claude 之间选择。新增一次向代理要多个结果并导出为同一个 Excel 文件（每个结果单独成表），以及连接 Google Antigravity 的 Wren AI MCP 服务器，在编辑器内直接查询公司数据。改进方面，更新 Knowledge 里的业务定义（如活跃客户的口径）后，同线程的下一条提问立即使用新定义；Wren AI 可为项目起草描述，经项目负责人审核后保存，帮助经 MCP 接入的 Claude、ChatGPT 等工具选对项目。
- [Wren AI 0.66.0 发布说明（11/27）](https://docs.getwren.ai/cp/releases/0.66.0)

### 5. 积墨AI：语义层加 Agent 的智能问数体系（11/27）

积墨AI 11 月 27 日发文阐述以语义层为核心的智能问数体系：语义层沉淀指标定义、维度口径与业务对象映射，业务问题经“语义理解→DSL 表达→SQL 执行→结果校验→分析交付”链路变成可审计的结果；文中提出“禁止手写 SQL”的约束，所有指标与维度须经语义层核验、由 DSL2SQL 生成、交只读执行器运行。体系按“能用、好用、持续好用”三步落地，并演化为多 Agent 分工：一个 Agent 管数据资产全生命周期，一个专责语义层与业务口径，一个面向业务完成取数分析与洞察。文中称该系统上线后累计调用量突破 23 万次，覆盖 190 余名用户。
- [积墨AI 文章（11/27）](https://jimo.studio/blog/semantic-layer-meets-agent-a-new-paradigm-for-trustworthy-ai-data-analytics/)

## 论文 / arXiv

### 6. Single-Database Rewards Are Hackable：反事实执行让 text-to-SQL 强化学习奖励更可信（11/25 提交、11/26 公告，补录）

Single-Database Rewards Are Hackable: Counterfactual Execution for Trustworthy Text-to-SQL RL（arXiv:2611.34363，11 月 25 日提交、11 月 26 日公告，上一期未收录，此处补录）指出：text-to-SQL 智能体的强化学习通常只在单个数据库上比对执行结果发奖励，错误的查询可能因数据中缺少能暴露 bug 的行而碰巧匹配。论文提出反事实数据库奖励：把最终查询同时跑在几个隐藏的代码生成数据库副本上，严格形式要求全部匹配才付全额奖励。在 1,302 道合成审计题上，严格形式把被全额奖励的错误查询占比从 29.5% 降至 16.8%，奖励 hack 从 54.1% 降至 1.9%，且 2,847 条正确查询无一被误拒；3.35B 模型上的 GRPO 对照实验显示，该奖励在 Spider 上提升 1.6 个百分点。
- [arXiv:2611.34363](https://arxiv.org/abs/2611.34363)

### 7. MGMem：确定性、无生成式索引的长程智能体记忆（11/27 登上 Hugging Face Daily Papers）

MGMem: An Efficient, Deterministic, and Provenance-Preserving Framework for Long-Horizon Agent Memory（arXiv:2611.33174，作者 Junhong Huang、Xin Tong、Jun Xia，10 月 21 日提交，11 月 27 日登上 Hugging Face Daily Papers）针对长程智能体记忆的索引环节：现有系统常调用生成式大模型把历史改写为摘要、事实或知识图谱，成本高、结果不确定、且丢失原始证据。MGMem 用确定性判别式解析管线替代这一步：跨会话重复出现的提及组织为关联图（incidence graph），提问中的提及经三阶段解析器定位，最后把原始对话片段直接交给阅读器。在英文多会话对话问答基准 LoCoMo 上，MGMem 准确率 75.89%，高于同协议基线 EMem 约 2.60 个百分点；LongMemEval-S 全集上整体有竞争力，单会话题型上领先或持平。
- [arXiv:2611.33174](https://arxiv.org/abs/2611.33174)

### 8. EMMA：面向具身 AI 数据的多模态分析查询框架（11/25 提交、11/26 公告，补录）

EMMA: Efficient and Effective Cooperative Multi-Modal Analytics over Embodied AI Data（arXiv:2611.33765，11 月 25 日提交、11 月 26 日公告，上一期未收录，此处补录）面向自动驾驶车辆与机器人持续采集的视频、激光雷达点云、GPS 轨迹等多模态数据，提出把分析查询编译为可组合算子的查询处理框架：按模态分阶段做谓词求值、选择性合并重叠观测，并用时序共位索引、自适应场景跳过与共享 world store 减少深度模型调用，在保持查询准确率的同时降低执行成本。
- [arXiv:2611.33765](https://arxiv.org/abs/2611.33765)

### 9. SeQLean：用 Lean 形式验证自然语言转 SQL 的翻译（11/26 出现在 cs.DB 列表）

SeQLean: Verifying SQL queries using Lean（arXiv:2611.33181，10 月 25 日提交，11 月 26 日出现在 cs.DB 新论文列表）用 Lean 形式验证提高自然语言转 SQL 的准确率：把 SQL 建模为 Lean 中的关系代数，用“证明挑战”检验翻译的内部一致性——例如为同一问题生成性能优化与可读性优先两个翻译，若二者等价则在任何数据库上答案必相同，该等价性可由 Lean 的证明自动化检验；HTTP 上的 JSON API 可把验证器接入智能体框架。
- [arXiv:2611.33181](https://arxiv.org/abs/2611.33181)

## 社交媒体

### 10. Instagram 帖子解读 Google Workspace MCP 服务器正式商用（11/28）

Instagram 用户 Isaac Munandar（@isaac.munandar）11 月 28 日发帖解读 Google Workspace MCP 服务器正式商用：Google 于 11 月 24 日让 Gmail、Drive、Docs、Sheets、Slides、Calendar、Chat、Tasks 八个应用的 MCP 服务器正式商用；自 2027 年 2 月 1 日起，AI 代理访问 Workspace 数据须经 MCP 服务器或官方命令行工具 gwscli，不再直接调用 REST API，否则将被限流至标准档配额。帖子同时提到代理学习到的数据须在 30 天内删除、不得用于模型训练等附加条款。
- [Instagram 帖子（11/28）](https://www.instagram.com/p/DgRfVn3CbOW/)
- [Google Cloud 官方博客（11/25）](https://cloud.google.com/blog/products/identity-security/deploying-agents-safely-in-your-enterprise)

本期检索范围内，Databricks AI/BI 发布说明最新条目仍为 11 月 26 日，11 月 27 日无新增；Snowflake 11 月的 Cortex AI 更新集中在 11 月 18 日至 20 日（Agent SDK GA 等），11 月 27 日的 Medium 汇总无新事实；Anthropic Skills over MCP 为 11 月 24 日发布，已在上一期说明在窗口之外；HYPR AgentPass 原发为 11 月 18 日，11 月 28 日的中文转载无新事实增量。arXiv cs.DB 列表截至发稿最新批次仍为 11 月 26 日，未见 11 月 27 日批次。开源项目方面，Wren Semantic Core 0.5.2 为 11 月 25 日例行修复、DB-GPT v0.8.3 为 11 月 17 日、Cube 1.8.14 为 10 月 28 日，均无今日新 Release；Hex 4.0 知识引擎为 11 月 19 日、dbt 11 月更新汇总为 11 月 17 日。ThoughtSpot、Sigma、Omni、Alation、Atlan、DataHub、Collibra、Monte Carlo、Salesforce/Tableau、Oracle、SAP、IBM、Palantir 及阿里云、火山引擎、腾讯云、百度智能云、京东云、网易智企、帆软、思迈特、观远数据、Kyligence、衡石科技、Aloudata、AskTable、数花智算、数势科技当日无数据代理相关新发布。中文媒体 36氪、量子位、机器之心、DataFunTalk、Datawhale、dbaplus、墨天轮、和鲸当日无数据代理直接相关的新内容。阿联酋 FedAI、瑞士 AI 代理网络攻击、SAP 安全事件等泛 AI 新闻与数据工作无直接关系，未收录。

## 今日回顾

The Information 11 月 24 日报道、The Decoder 11 月 27 日跟进：OpenAI 正在开发代号 Athena 的数据管理平台，形态类似语义层，让数据代理按统一口径理解业务指标；项目仍在早期，未公布上线时间与定价。Wren AI 11 月 27 日发布 0.66.0，Agentic Mode 可按线程选用 Gemini、Claude 或 GPT 模型，并新增多结果导出 Excel 与 Google Antigravity 的 MCP 连接。Dex 1.19.0 与 SchemaGate 1.20.0 于 11 月 26 日发布：前者用运行历史定位 dbt 测试失败窗口，后者用结果指纹校验模型改写的 SQL。积墨AI 11 月 27 日发文阐述语义层加 Agent 的智能问数体系，称系统累计调用超 23 万次。arXiv 补录两篇论文：反事实数据库奖励把 text-to-SQL 强化学习的奖励 hack 从 54.1% 降至 1.9%；EMMA 面向具身 AI 数据做多模态分析查询；MGMem 以确定性解析做长程智能体记忆，LoCoMo 准确率 75.89%；SeQLean 用 Lean 形式验证自然语言转 SQL。Instagram 11 月 28 日帖子解读 Google Workspace MCP 服务器正式商用，2027 年 2 月 1 日起 AI 代理须经 MCP 访问 Workspace 数据。
