---
layout: post
title: "Data Agent Daily — 2026-11-20"
author: dad
date: 2026-11-20
image: "assets/images/covers/2026-11-20.svg"
description: "Tableau 官方确认 Tableau Studio 与 Tableau Data Apps 已在 Tableau Server 与 Cloud 上全面可用，服务器版按 11 月 16 日公布的计划于 11 月 19 日上线；Databricks 自主修数仓管线的 Genie ZeroOps 进入公开 Beta，Snowflake Decision 模型进入公开预览，Hex 推出自学习图谱上下文系统 Knowledge Engine。"
categories: ["Data Agent Daily"]
tags: ["data-agent", "news"]
comments: false
---

## 今日速览

- Tableau 官方确认 Tableau Studio 与 Tableau Data Apps 已在 Tableau Server 与 Cloud 上全面可用，服务器版按 11 月 16 日公布的计划于 11 月 19 日上线。
- Databricks 自主修数仓管线的 agent Genie ZeroOps 进入公开 Beta，私有预览期间观测到 8 万多个真实客户问题，修复须人工批准才进生产。
- Snowflake 的 Decision 模型进入公开预览，可在一条 SQL 内对表做多项独立分类与打分并返回概率与置信度，报价 $0.042/百万 token。
- Hex 推出自学习图谱上下文系统 Knowledge Engine，每夜由策展 agent 归纳当日工作中的新知识并分级，随 Hex 4.0 公开 Beta 推出。
- Informatica 扩大与微软在 Ignite 上的合作，受治理的企业数据进入 Copilot、Foundry 与 Fabric，Copilot 与 Teams 集成已 GA。
- Google 在 Gemini Interactions API 中推出 Tool Retrieval 预览，agent 可把大工具库置于待命状态、仅在需要时按需加载工具参数。
- Collibra 发布 11 月产品上新，Control Tower、Maestro、MCP Governance 等上线，涵盖定时治理检查、无代码构建 AI agent 与 MCP 工具管控。
- OpenAI 的常驻 agent Dots 开始向少量 ChatGPT Plus 用户测试，并即日起向全部 ChatGPT Business Standard 用户开放。
- DataHub 发布补丁版 v1.9.1，修复 OpenSearch 2.x 上多 OR 组语义搜索无结果的问题，服务镜像升级至 OpenJDK 25.0.5.1。
- arXiv 11 月 20 日上线 Cost-Aware Agentic Feature Optimization：LLM 智能体为大规模排序模型做特征优化，生产模型平均 normalized entropy 提升 0.31%、pipeline 成本降低 2.3%。
- arXiv 11 月 20 日上线 GenSPARQL：为 SPARQL 增加 GENOP 算子，让 LLM 在查询求值过程中为变量生成缺失事实值，83% 的 LLM 命名实体被正确映射回图谱。
- arXiv 11 月 20 日上线 Thetis++：面向数据湖探索式表搜索，结合关键词与语义信号，HNSW 预过滤比 LSH 平均快 4.7 倍。
- arXiv 11 月 20 日上线 LINEAGE：面向科研智能体文献检索的实证谱系检索基准，基于 121,048 篇论文构建，含 67,502 个节点与 164,948 条谱系边。
- arXiv 11 月 20 日上线 AutoRAGBench：评测 LLM 智能体自动开发 RAG 系统能力的基准。
- arXiv 11 月 20 日上线 TwinLab-Bench：AI 科学家基准，52 个软件介导实验室任务，33 个缺决定性数据的任务上零预算通过数为 0。
- arXiv 11 月 20 日上线 CompAct-Bench：200 任务基准评测长程智能体工作上下文压缩，压缩后平均准确率跌至 56.7%。
- arXiv 11 月 20 日上线 AppSci-Bench：评测 LLM 构建与改进面向业务的 AI 智能体能力，Claude Opus 5.0 平均-最小分最高，为 59.1%。
- arXiv 11 月 19 日上线 Asking but Missing：自然语言数据查询中的决策覆盖研究，12 个模型在 BIRD-Pandas 上的结论是主要难点是识别出哪些问题需要问。
- arXiv 11 月 19 日上线 Cascadeability and the Realization Gap：LLM 语义过滤代理级联的实证研究，含 10 个真实工作负载。
- Wren AI 官方 Facebook 11 月 19 日发帖宣传与 TrueNAS 的合作，私有 GenBI 运行在用户已有存储上，本地模型、零数据外流。

## 公司发布 / 官方博客

### 1. Tableau Studio 与 Tableau Data Apps 在 Server 与 Cloud 全面 GA（11/19）
Tableau 官方 11 月 19 日发帖确认，Tableau Studio 与 Tableau Data Apps 已在 Tableau Server 与 Cloud 上全面可用；此前按 11 月 16 日公布的计划，云版定于 11 月 17 日上线、服务器版定于 11 月 19 日上线，云版已按计划上线，服务器版至此获得官方确认。Tableau Studio 是对话式编写分析的 agentic 工作区，用 Tableau Agent 与 Tableau Skills 在受治理数据上编写、打磨分析，可随时切回 Tableau 熟悉的编写体验；完整体验需 Creator 许可与 Tableau+、Cloud+ 或 Server+ 版本。Tableau Data Apps 可从任意 agent 对话式构建自定义分析 Web 应用，Tableau 托管每个应用并沿用同一套安全、权限与治理。同日更新的 Tableau 11 月新功能页还列出：Tableau Next 的 Q&A 校准批量回归测试将于 11 月内 GA，Tableau Agent 语义建模进入 Beta。
- [Tableau 官方 Facebook（11/19）](https://www.facebook.com/Tableau/posts/pfbid0LKpjtDDySfp9nA7LhV7N8yGWvqLqjtyFzC8jn4MRrbxpv8YWnbeCep2zCXSdTXtpl)
- [Tableau 11 月新功能页](https://www.tableau.com/products/new-features?field_products_target_id=2068)

### 2. Databricks Genie ZeroOps 进入公开 Beta（11/19）
Databricks 11 月 19 日宣布，自主修数仓管线的 agent Genie ZeroOps 进入公开 Beta，工作区管理员可在 Previews 页开启。该 agent 按检测、调查、验证、通知、修复五步自动处理管线故障与静默数据质量问题：持续监控任务、管线与表，定位根因并在沙箱中用单元测试与 dry run 验证拟议修复，再把摘要与修复建议发至 Slack、Teams 或 PagerDuty，修复以 PR 形式提交；ZeroOps 绝不在未经人工批准的情况下改动生产代码或数据。私有预览期间，ZeroOps 在数百家客户处观测到 8 万多个真实客户问题，超半数问题需要组织专属知识才能正确分诊、排序与解决；Beta 新增共享收件箱、摘要通知、自定义 agent 指令与一键 PR。
- [Databricks 官方博客（11/19）](https://www.databricks.com/blog/genie-zeroops-now-public-beta-autonomous-agent-fixes-data-pipelines-lessons-80000-customer)

### 3. Snowflake Decision 模型进入公开预览（11/20）
Snowflake 文档发布说明 11 月 20 日条目确认，Cortex AI_COMPLETE 开始支持 Snowflake Decision 公开预览。该模型专为大批量分类、打分与决策设计，用户提供评判标准后，可在一条 SQL 内对表做多项独立评估并返回概率与置信度，支持选定类别、按有序量表打分、判断陈述真伪三种问题类型；多个独立评估可共享一次 AI_COMPLETE 请求。Snowflake 报价 $0.042/百万 token、每行约 1.58 毫秒处理时间（厂商说法，未附准确率基准）。该模型 10 月 7 日进入私有预览，本次为可用阶段的变更。
- [Snowflake 官方文档发布说明（11/20）](https://docs.snowflake.com/en/release-notes/all-release-notes)
- [Superpower Daily 报道（11/20）](https://superpowerdaily.com/posts/snowflake-opens-public-preview-of-ai-model-for-classifying-and-scoring-data)

### 4. Hex 推出 Knowledge Engine，随 Hex 4.0 公开 Beta 推出（11/19）
Hex 11 月 19 日在 changelog 中推出自学习图谱上下文系统 Knowledge Engine，随 Hex 4.0 公开 Beta 推出。每夜由后台策展 agent 复核当日工作中的新知识，合并重复项、强化已有知识、标记冲突指引，再按含义与用法分级：Verified（有定义上下文背书）、Supported（有可用上下文佐证）、Learning（agent 自行决定、上下文既不支持也不否定）、Contested（来源不一致）与 Debunked（已证伪、作为警示记录留存）。提问时，agent 先查知识图谱再检索，以减少重复推理与偏离可信逻辑的情况；管理员可在 Context Studio → Knowledge 中复核有争议的知识。
- [Hex 官方 Changelog（11/19）](https://learn.hex.tech/changelog/2026-11-19)

### 5. Informatica 扩大与微软在 Ignite 上的合作（11/19）
Informatica（Salesforce 旗下）11 月 19 日宣布扩大与微软的合作，把受治理的企业数据带入 Copilot、Foundry 与 Fabric：Copilot 与 Teams 集成已 GA，可查询权威业务定义、数据质量与血缘；Foundry 的 Informatica Headless 新增 MCP 治理、身份与管理能力；Fabric 扫描扩展至 notebook 与 pipeline，已 GA；另新增美国东海岸 Azure 交付点。
- [Salesforce 新闻中心（11/19）](https://www.salesforce.com/in/news/stories/informatica-trusted-enterprise-data-microsoft-collaboration/?bc=OTH)

### 6. Google 推出 Gemini API Tool Retrieval 预览版（11/19）
Google 11 月 19 日在 Gemini Interactions API 中推出 Tool Retrieval 预览，agent 可把大工具库置于待命状态、仅在需要时按需加载工具参数 schema，以减少 token 消耗与延迟并提升工具选择准确率；支持 Gemini 3.6 及更新模型（含 Gemini 4 全系），无单独收费。
- [Google 官方博客（11/19）](https://blog.google/innovation-and-ai/technology/developers-tools/gemini-api-tool-retrieval/)

### 7. Collibra 发布 11 月产品上新（11/19）
Collibra 官方 Facebook 11 月 19 日发布“November's Product Drop”：Control Tower（定时治理检查 + 邮件/Slack/Teams 告警）GA；Maestro（在 Collibra 内无代码构建 AI agent，带审批流）；MCP Governance（通过 MCP 网关控制 agent 可用工具）；Governance by Design；Python 脚本血缘（AI 读代码映射列级血缘）。
- [Collibra 官方 Facebook（11/19）](https://www.facebook.com/CollibraInc/posts/pfbid02C86wUw4SCGWQA3S8mEbeMSGAkGwkmQAhv9KipxPvGLS9ULoV9qXpxyG3UBtDES49l)
- [Collibra 官网 innovations 页](https://www.collibra.com/products/innovations)

### 8. DataHub 发布补丁版 v1.9.1（11/19，简讯）
DataHub 11 月 19 日发布 v1.9.1 补丁版：修复 OpenSearch 2.x 上语义搜索在过滤条件含两个及以上 OR 组时无结果的问题；服务镜像升级至 OpenJDK 25.0.5.1 以修复 CVE-2026-114938。
- [DataHub 官方 Release 页（11/19）](https://docs.datahub.com/docs/releases)

## 新闻网站

### 9. OpenAI 把常驻 agent Dots 扩展至 Plus 小范围测试与 Business Standard 全量（11/19 宣布，11/20 报道）
ChatGPT 工程负责人 Thibault Sottiaux 11 月 19 日在 X 上宣布，主动式常驻 agent Dots 开始向少量 ChatGPT Plus（$20/月）用户测试，并即日起向全部 ChatGPT Business Standard 用户开放；Dots 可通过插件生态接入 4,000 多个应用、自主执行任务，现可跑在 GPT-6.1 Terra 上（此前为 GPT-6 Astra）。该条为通用 agent 扩面，与数据工作无专属关系，作简讯收录。
- [Engadget 报道（11/20）](https://www.engadget.com/2322656/openai-is-testing-dots-personal-agents-on-its-20-per-month-plus-tier/)

## 论文 / arXiv

### 10. Cost-Aware Agentic Feature Optimization System for Fleet-Scale Ranking Models（11/20）
Cost-Aware Agentic Feature Optimization System for Fleet-Scale Ranking Models（arXiv:2611.26531，11 月 19 日提交，11 月 20 日上线，作者 Chang Yang、Yao Xuan、Wendan Yan 等）用 LLM 智能体为大规模排序模型 fleet 做特征优化：自动生成交叉特征，Researcher 智能体在成本上限内做 10–25 轮异步试验调优特征选择。生产模型平均 normalized entropy 提升 0.31%，pipeline 成本降低 2.3%，上线后在线 A/B 主指标提升 0.20%。
- [arXiv:2611.26531](https://arxiv.org/abs/2611.26531)

### 11. GenSPARQL：面向不完整知识图谱的 SPARQL 生成式扩展（11/20）
GenSPARQL: A Generative Extension of SPARQL for Incomplete Knowledge Graphs（arXiv:2611.26062，11 月 19 日提交，11 月 20 日上线，作者 Jingcheng Wu、Yi Wang、Hongkuan Zhou、Steffen Staab、Bo Xiong）为 SPARQL 1.1 增加 GENOP 算子，让 LLM 在查询求值过程中为变量生成缺失事实值，再经相似度连接映射回图谱实体；三款开源 LLM 评估中，83% 的 LLM 命名实体被正确映射，仅 1 处错误匹配。
- [arXiv:2611.26062](https://arxiv.org/abs/2611.26062)

### 12. Thetis++：数据湖中的语义表搜索（11/20）
Exploring Semantic Table Search in Data Lakes（arXiv:2611.25691，11 月 19 日提交，11 月 20 日上线，作者 Martin Pekár Christensen、Matteo Lissandrini、Katja Hose）面向数据湖探索式表搜索，提出结合关键词与语义（实体）信号的 Thetis++ 方法；HNSW 预过滤比 LSH 平均快 4.7 倍且保持检索质量。
- [arXiv:2611.25691](https://arxiv.org/abs/2611.25691)

### 13. LINEAGE：面向科研智能体的实证谱系检索基准（11/20）
LINEAGE: A Benchmark for Empirical Lineage Retrieval in AI Scientific Literature（arXiv:2611.25845，11 月 19 日提交，11 月 20 日上线，作者 Pangjing Wu、Xu Yuan、Wenqi Fan、Qing Li）面向科研智能体文献检索的实证谱系检索基准，基于 2018–2025 年 17 个顶会 121,048 篇论文构建，含 67,502 个节点、164,948 条谱系边、80,000 条多面检索查询，评测了 19 个检索系统。
- [arXiv:2611.25845](https://arxiv.org/abs/2611.25845)

### 14. AutoRAGBench：评测 LLM 智能体自动开发 RAG 系统能力的基准（11/20）
AutoRAGBench: A Benchmark for LLM Agents Automating RAG System Development（arXiv:2611.25582，列入 11 月 19 日 agent benchmarks 新榜，作者 Hang Zhang、Yuzhi Pan、Ziyao Zhong 等）评测 LLM 智能体自动开发 RAG 系统的能力；RAG 系统开发需大量工程投入与反复试验，设计选择因场景而异。
- [arXiv:2611.25582](https://arxiv.org/abs/2611.25582)

### 15. TwinLab-Bench：用真实实验室的智能体孪生评测 AI 科学家（11/20）
TwinLab-Bench: Evaluating AI Scientists in Agentic Twins of Real Labs（arXiv:2611.26248，列入 11 月 19 日 agent benchmarks 新榜，作者 Yang Wan、Linchao Zhu）提出 AI 科学家基准，52 个软件介导实验室任务，覆盖执行既定流程、选下一步测量、自主设计实验三层能力；33 个缺决定性数据的任务上零预算通过数为 0。
- [arXiv:2611.26248](https://arxiv.org/abs/2611.26248)

### 16. CompAct-Bench：长程智能体任务的工作上下文压缩基准（11/20）
CompAct-Bench: A Benchmark for Working-Context Compaction in Long-Horizon Agent Tasks（arXiv:2611.25673，列入 11 月 19 日 agent benchmarks 新榜，作者 Jiayi Chen、Lizhe Chen、Yujia Chen 等）为 200 任务基准（BrowseComp 79 + SWE-bench 96 + CompanyBench 25），评测 12 个前沿模型做长程智能体工作上下文压缩；压缩后平均准确率跌至 56.7%，最强的 Claude Opus 5 也仅 68.5%。
- [arXiv:2611.25673](https://arxiv.org/abs/2611.25673)

### 17. AppSci-Bench：LLM 能否构建 AI 智能体并让它们变得更好（11/20）
AppSci-Bench: Can LLMs Build AI Agents and Make Them Better?（arXiv:2611.25360，列入 11 月 19 日 agent benchmarks 新榜，作者 Sanjari Srivastava、Manpreet Kaur、Cheng Chang 等）评测 LLM 构建与改进面向业务的 AI 智能体能力，覆盖 7 个领域、7 个前沿模型；Claude Opus 5.0 在 3 次构建尝试中平均-最小分最高，为 59.1%。
- [arXiv:2611.25360](https://arxiv.org/abs/2611.25360)

### 18. Asking but Missing：自然语言数据查询中的决策覆盖（11/19 上线，补录）
Asking but Missing: Decision Coverage in Natural-Language Data Querying（arXiv:2611.23864，11 月 18 日提交，11 月 19 日上线，作者 Hangle Hu 等）提出 Grounded Code Generation 诊断协议，区分“识别未决决策—用证据解决—翻译为可执行代码”三阶段，在 BIRD-Pandas 上评测 12 个模型；结论是主要难点不是回答澄清问题、而是识别出哪些问题需要问。
- [arXiv:2611.23864](https://arxiv.org/abs/2611.23864)

### 19. Cascadeability and the Realization Gap：LLM 语义过滤代理级联的实证研究（11/19 上线，补录）
Cascadeability and the Realization Gap: An Empirical Study of LLM-Powered Semantic Filtering（arXiv:2611.23898，11 月 18 日提交，11 月 19 日上线，作者 Nan Hou 等）研究 LLM 语义过滤的代理级联（proxy cascade），含 10 个真实工作负载，提出 cascadeability 与 realization gap 诊断量。
- [arXiv:2611.23898](https://arxiv.org/abs/2611.23898)

## 社交媒体

### 20. Wren AI 官方 Facebook 宣传与 TrueNAS 的合作（11/19）
Wren AI 官方 Facebook 账号 11 月 19 日发帖宣传与 TrueNAS 的合作：把 Wren AI 生成式 BI 集成进 TrueNAS，私有 GenBI 运行在用户已有存储上，本地模型、零数据外流、就地查询 20+ 数据源、快照保护上下文层，支持 RLS 与 CLS。
- [Facebook @getwrenai（11/19）](https://www.facebook.com/getwrenai/posts/pfbid0cK8Hqq3EPgpwBAeM5qZc6bbsMoTJnB1hU7MN4tdDQFDsUrZuFrpNEQRFhoVMeRzEl)

本期检索范围内，国内大厂（阿里云、火山引擎、腾讯云、百度智能云、网易智企、华为云、京东云）与国内独立厂商（Aloudata、AskTable、数花智算、数势科技、帆软、思迈特、观远数据、Kyligence、衡石科技）当日均无数据代理相关的新发布；中文媒体 36氪、机器之心、量子位、InfoQ、DataFunTalk、Datawhale、dbaplus、墨天轮、和鲸当日均无数据智能体直接相关的新内容；WrenAI、DB-GPT、Cube Core、Chat2DB、Vanna、Apache Gravitino、Alpha-SQL、ReFoRCE、DeepEye-SQL、LAMBDA、Data Interpreter、DeepAnalyze、DocETL 当日均无新 Release；Spider 2.0、BIRD、DABstep、DAComp 等评测基准原作者团队当日无新动态；Hugging Face Papers 11 月 20 日日榜前列无与数据代理直接相关的论文；ThoughtSpot 11 月 20 日无新发布；Microsoft Ignite 2026 第 4 天未见 Fabric、Copilot 或 Microsoft IQ 的新事实。LanceDB 5,750 万美元 B 轮（11 月 17 日宣布）与 Workday 拟收购语义层厂商 Honeydew（11 月 18 日宣布）均在约 24 小时窗口之外，未作条目；Anthropic 11 月 20 日无可核实的产品新发布。

## 今日回顾

Tableau 官方确认 Tableau Studio 与 Tableau Data Apps 已在 Tableau Server 与 Cloud 上全面可用，服务器版按计划于 11 月 19 日上线；Databricks 的 Genie ZeroOps 进入公开 Beta，私有预览期间观测到 8 万多个真实客户问题；Snowflake Decision 模型进入公开预览；Hex 推出 Knowledge Engine，随 Hex 4.0 公开 Beta 推出；Informatica 扩大与微软的合作；Google 推出 Gemini API Tool Retrieval 预览；Collibra 发布 11 月产品上新；OpenAI 的 Dots 开始向少量 Plus 用户测试；DataHub 发布 v1.9.1；arXiv 同日上线 Cost-Aware Agentic Feature Optimization、GenSPARQL、Thetis++、LINEAGE、AutoRAGBench、TwinLab-Bench、CompAct-Bench 与 AppSci-Bench 八篇论文，另补录 11 月 19 日上线的 Asking but Missing 与 Cascadeability；Wren AI 官方 Facebook 宣传与 TrueNAS 的合作。
