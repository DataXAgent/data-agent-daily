---
layout: post
title: "Data Agent Daily — 2026-11-21"
author: dad
date: 2026-11-21
image: "assets/images/covers/2026-11-21.svg"
description: "Databricks 宣布 Genie Agents 的 MCP 工具正式 GA，作者可为 agent 接入 Unity Gateway 注册的外部 MCP 服务器；Emerson 与 Databricks 合作把工业 OT 数据接入 Databricks 平台；微软推出 Agent Controls 公共预览，Alteryx、Starburst、Qlik、IBM Cognos 等同周发布数据智能体相关更新。"
categories: ["Data Agent Daily"]
tags: ["data-agent", "news"]
comments: false
---

## 今日速览

- Databricks 宣布 Genie Agents 的 MCP 工具正式 GA，作者可为 agent 接入 Unity Gateway 注册的外部 MCP 服务器，Agent mode API 同步支持 MCP 工具。
- Emerson 与 Databricks 合作，把 AspenTech Inmation OT Data Fabric 的原生访问接入 Databricks Data + AI 平台，工业 OT 数据可与业务数据一起用于分析、AI 应用与 agent。
- 微软推出 Agent Controls 公共预览，基于开源 Agent Control Specification 与 Agent Hooks，在运行时集中评估并执行 agent 行为策略。
- Alteryx 推出 VURA 治理体验，把工作流认证、血缘与数据质量等信任信号直接呈现在 OpenAI、Claude 与 Gemini 的对话界面中。
- Starburst 推出 Context Studio 私有预览，从现有目录、BI 工具与指标库中汇聚业务定义，供 AI agent 查询时使用，定义冲突由人工审批解决。
- Qlik Answers 新增自定义技能与高级分析能力，可按企业自有术语与业务规则引导分析，并做排除集、预测、优化与因果分析。
- IBM Cognos Analytics 12.2.0 发布，Query Agent 从预览转为正式可用，内置 MCP 服务器扩至 104 个工具。
- DataSwitch 推出 Mathi，基于专家本体推荐 schema 映射与业务规则，经专家批准后生成数据管道，管道可供 Databricks Genie 与 Snowflake Cortex 使用。
- SAS 与 Posit 合作，把 SAS Viya 与 SAS Clinical Acceleration 同 Posit Workbench、Positron 等工具集成，首批面向临床开发。
- 英伟达在 SC26 发布 Rubin HPC GPU，单卡 CUDA 核心超 5 万个，面向 agent 调用的科学模拟与数据处理，预计 2028 年上市。
- Cube 11 月 20 日更新日志新增 Cube Apps，可在 Cube 内搭建仪表盘、滚动故事与幻灯片。
- 华尔街日报报道，Databricks 正就新一轮融资进行早期谈判，估值约 2,250 亿美元。
- arXiv 11 月 19 日上线 DSFlow：基于 LangGraph 的神经符号数据工作流智能体，以确定性统计诊断护栏校验 LLM 选择的方法。
- arXiv 11 月 20 日上线 Bridging the Discovery Gap in Solid Dataspaces：为 Solid 数据空间提出符合 FAIR 原则的语义数据目录。
- arXiv 11 月 20 日上线 STARR：嵌入模型更换后迁移 HNSW 索引的方法，240 组迁移中位构建提速 16.71 倍、召回中位损失 1 个百分点。
- OpenAI 11 月 20 日在 YouTube 发布《Meet the Data Agent in ChatGPT》，介绍 ChatGPT Data 插件的问数、制图与建仪表盘能力。

## 公司发布 / 官方博客

### 1. Databricks Genie Agents 的 MCP 工具正式 GA（11/20）
Databricks 11 月 20 日在 AI/BI 与 Genie One 发布说明中确认，Genie Agents 的 MCP 工具正式 GA：作者除 Databricks 自带连接器外，还可接入在 Unity Gateway 注册的外部 MCP 服务器，Agent mode API 同步支持 MCP 工具。此前 Genie Agents 的 MCP 连接器处于 Beta，Genie One MCP 服务器已于 9 月 22 日 GA；本次 GA 的是面向 Genie Agents 作者的 MCP 工具接入能力。
- [Databricks 官方发布说明（11/20）](https://docs.databricks.com/gcp/en/ai-bi/release-notes/2026)

### 2. Emerson 与 Databricks 合作，把工业 OT 数据接入企业 AI 平台（11/19）
Emerson 11 月 19 日宣布与 Databricks 合作，把 AspenTech Inmation OT Data Fabric 的原生访问接入 Databricks Data + AI 平台：工业企业可把实时与历史的工厂、资产与运营数据同业务数据结合，用于预测性维护、性能优化、分析、AI 应用与 agent；客户还可在 Databricks 内访问 AspenTech AVA AI 平台与 Inmation 管理的全部上下文数据。Emerson 称，合作要解决的关键障碍是 OT 数据与业务数据之间的 IT/OT 鸿沟。
- [Emerson 官方新闻稿（11/19）](https://www.emerson.com/en/corporate/news/2026/emerson-databricks-bring-industrial-and-enterprise-ai-together)
- [IT Business Today 报道（11/19）](https://itbusinesstoday.com/tech/ai/emerson-and-databricks-join-forces-to-advance-industrial-ai/)

### 3. 微软推出 Agent Controls 公共预览（11/18，补录）
微软 11 月 18 日推出 Agent Controls 公共预览，这是一项 Azure 托管服务，用于集中定义、管理和评估跨框架、平台与云的 AI agent 行为策略。该服务基于微软开源的 Agent Control Specification（ACS）与 Agent Hooks：Agent Hooks 在 agent 生命周期各环节（启动、输入、模型调用、工具调用、输出、关停）设置干预点，ACS 定义评估请求与决策的开放契约；策略可组合内容安全分类器、LLM 评判器与确定性规则（如 Rego），每次评估返回允许、拒绝或转换三类决策，并附带标明所用策略与版本的回执。微软同时说明，服务本身不做沙箱隔离，执行决策仍由宿主负责。
- [微软官方博客（11/18）](https://commandline.microsoft.com/introducing-agent-controls-an-enterprise-control-plane-for-agent-behavior/)

### 4. Alteryx 推出 VURA 治理体验（11/18，补录）
Alteryx 11 月 18 日推出 VURA 治理体验，把其 VURA（可见、可理解、可重复、可审计）框架变为 Alteryx One 内的一项主动治理能力：实时信任信号直接呈现在 OpenAI、Anthropic Claude 与 Google Gemini 的对话界面中，业务用户可在提问时看到工作流认证、数据标签、血缘与数据质量信息，IT 则集中管控权限、版本与上线流程；Alteryx One 还通过 MCP 原生接入企业技术栈，并提供面向 OpenAI、Claude、Gemini、Microsoft Copilot、Databricks Genie 与 Snowflake Cortex 的集成。Alteryx 援引其 2026 年数据分析师现状报告称，43% 的受访组织认为解释 AI 洞察仍是主要挑战。
- [PR Newswire 通稿（11/18）](https://www.prnewswire.com/news-releases/alteryx-introduces-vura-governance-experience-to-help-enterprises-validate-ai-outputs-and-automate-operations-with-greater-trust-and-reliability-302943259.html)
- [TechTarget 报道（11/18）](https://www.techtarget.com/news/alteryx-launches-vura-governance-suite-to-boost-ai-visibility/874985/)

### 5. Starburst 推出 Context Studio 私有预览（11/18，补录）
Starburst 11 月 18 日推出 Context Studio 私有预览，从现有数据目录、BI 工具、指标库与文档中汇聚业务定义，供 AI agent 回答问题时与数据一并使用，以消除不同部门对同一指标定义不一致导致 agent 给出看似合理实则错误的答案。定义冲突由内置审批流解决，agent 提出的改进须经人工批准，再经回归测试检查对既有查询的影响；系统同时记录 agent 访问的数据源、生成的 SQL 与答案依据，便于审计。Context Studio 现为私有预览，公开预览计划于 2027 年 1 月推出，GA 预计 2027 年第一季度；公司未披露准确率或生产力方面的量化证据。
- [SiliconANGLE 报道（11/18）](https://siliconangle.com/2026/11/18/starburst-adds-context-support-to-give-ai-agents-consistent-access-to-business-data-definitions/)

### 6. Qlik Answers 新增自定义技能与高级分析（11/17，补录）
Qlik 11 月 17 日宣布，Qlik Answers 新增自定义技能与高级分析能力，现已可用：企业可用自有术语、业务规则与分析指令定义自定义技能，引导 Qlik Answers 按组织自己的方式调查业务问题；高级分析把 Qlik Analytics Engine 接入对话体验，可做排除集（灰色）分析、预测分析、优化与因果分析，发现初始答案可能遗漏的数据。更新采用以 AWS Bedrock 基础模型驱动推理的简化架构，Qlik 称内部测试显示准确率提升约 15%、响应速度快一倍以上（未提供独立第三方测试结果）。
- [TechTarget 报道（11/17）](https://www.techtarget.com/news/new-qlik-answers-capabilities-improve-ai-fueled-insight-generation/874957/)
- [GlobeNewswire 通稿（11/17）](https://beta.manilatimes.net/2026/11/17/tmt-newswire/globenewswire/qlik-answers-puts-business-expertise-to-work-in-ai-assisted-decisions/2472109/amp)

### 7. IBM Cognos Analytics 12.2.0 发布，Query Agent 正式 GA（11/16，补录）
IBM 11 月 16 日发布 Cognos Analytics 12.2.0，Query Agent 从预览转为正式可用：用户可从报表、仪表盘与数据模块直接用自然语言提问，获得表格、图表与后续追问建议；Premium Kit 内置的 MCP 服务器扩至 104 个工具（新增 40 多个），兼容的 AI 客户端可通过它校验报表、排程任务与监控执行；仪表盘新增导出 PowerPoint 与 Markdown。
- [IBM 官方公告（11/16）](https://www.ibm.com/new/announcements/ibm-cognos-analytics-12-2-0-turns-ai-conversations-into-connected-analytics-workflows)

### 8. DataSwitch 推出 Mathi，把专家知识转为 AI 就绪数据管道（11/16，补录）
DataSwitch 11 月 16 日推出 Mathi，其 Expert-to-Pipeline（E2P）平台背后的 AI 判断引擎：Mathi 基于企业本体推荐 schema 映射与业务规则，并附证据与置信度分数供领域专家审核，批准后生成数据管道、验证测试与血缘；一家全球保险集团正用它把收购业务的遗留保单数据映射进标准模型。Mathi 由 DataSwitch 自研私有小语言模型 Medha 驱动，可在标准 CPU 上气隙运行；经批准的决策指导 AI agent 为 Databricks、Snowflake 与 Microsoft Fabric 构建原生管道，产出数据可供 Databricks Genie 与 Snowflake Cortex 使用。
- [Business Wire 通稿（11/16）](https://www.businesswire.com/news/home/20261113596599/en/DataSwitch-Introduces-Mathi-to-Turn-Enterprise-Expertise-into-AI-Ready-Data-Pipelines)

### 9. SAS 与 Posit 合作，面向受治理的生命科学 AI（11/16，补录）
SAS 11 月 16 日宣布与 Posit PBC 合作，把 SAS Viya 与 SAS Clinical Acceleration 同 Posit Workbench、Positron、Posit Connect 与 Posit Package Manager 集成，首批面向临床开发：程序员可在 Positron 内同一会话中编写 SAS 与 R 代码，SAS Viya 按程序员本人权限执行 SAS 代码；Posit 工具让客户在受管控、有版本的环境中使用开源技术，同时满足监管要求。双方专家于 11 月 15–18 日在格拉斯哥 PHUSE EU Connect 现场展示该集成；未披露财务条款。
- [PR Newswire 通稿（11/16）](https://www.prnewswire.com/news-releases/sas-and-posit-partner-for-governed-ai-in-life-sciences-302939752.html)

### 10. 英伟达在 SC26 发布 Rubin HPC GPU（11/16，补录）
英伟达 11 月 16 日在 SC26 超算大会上发布 Rubin HPC GPU，属 Vera Rubin 平台的新分支，面向科学与工程模拟与数据处理：单卡 CUDA 核心超 5 万个，配稀疏数据加速能力与第七代 NVLink，agent 可调用 CUDA-X 库中的算法做模拟与分析。英伟达称，agent 帮科学家筛选候选材料、分子与设计方案时依赖模拟验证想法，更快的模拟意味着更快的发现；该 GPU 预计 2028 年上市，未公布显存、功耗与定价。
- [HPCwire 报道（11/16）](https://www.hpcwire.com/off-the-wire/nvidia-announces-rubin-hpc-a-new-gpu-to-accelerate-agents-for-science-engineering-and-analytics/)

### 11. Cube 11 月 20 日更新日志新增 Cube Apps（简讯）
Cube 11 月 20 日更新日志新增 Cube Apps，可在 Cube 内搭建打破网格的仪表盘、滚动故事与幻灯片。同日自托管目录显示 Cube Core v1.8.31 发布。
- [Cube 官方更新日志（11/20）](https://cube.dev/changelog)

## 新闻网站

### 12. 华尔街日报：Databricks 正就约 2,250 亿美元估值的新一轮融资谈判（11/20）
《华尔街日报》11 月 20 日报道，Databricks 正就新一轮数十亿美元融资进行早期谈判，估值约 2,250 亿美元；该公司 8 月曾宣布以 1,900 亿美元估值融资 50 亿美元。Databricks 提供帮助企业存储、分析数据与开发 AI 应用的软件，与 Snowflake 竞争，被视为未来上市候选。
- [Channel News Asia 转引华尔街日报（11/20）](https://www.channelnewsasia.com/business/databricks-in-early-talks-raise-funds-225-billion-valuation-wsj-reports-6570836)

## 论文 / arXiv

### 13. DSFlow：带统计诊断护栏的神经符号数据工作流智能体（11/19 上线，补录）
DSFlow: A Neuro-Symbolic Data Workflow Agent with Statistical Diagnostic Guardrails（arXiv:2611.25111，11 月 18 日提交，11 月 19 日上线，作者 Junfeng Nie、Xiaohui Chen）提出基于 LangGraph 的神经符号数据智能体平台，把 LLM 选择的可复用技能与确定性诊断护栏结合：技能提供可扩展的任务知识，符号校验可接受提议方法、要求澄清或重新规划、覆盖不合适的方法，或提供安全兜底；回归与聚类案例展示了 DSFlow 如何用诊断证据纠正方法选择，并在可审计报告中记录决策。
- [arXiv:2611.25111](https://arxiv.org/abs/2611.25111)

### 14. Bridging the Discovery Gap in Solid Dataspaces：面向 Solid 数据空间的语义数据目录（11/20）
Bridging the Discovery Gap in Solid Dataspaces with a Semantic Data Catalog（arXiv:2611.26611，11 月 19 日提交，11 月 20 日上线，作者 Florian Hölken、Alexander Paulus、Tobias Meisen、André Pomp）为去中心化的 Solid 数据空间提出符合 FAIR 原则的数据目录：用语义模型描述各 Solid 服务器与 Pod 中的可用数据源，解决跨多服务器发现与定位数据的难题，以提升数据发现、标准化元数据访问、跨源互操作与复用，面向智慧城市等开放数据生态。
- [arXiv:2611.26611](https://arxiv.org/abs/2611.26611)

### 15. STARR：嵌入模型更换后的 HNSW 索引迁移方法（11/20，简讯）
Standardized Tolerance for Adaptive Reuse and Repair: A Method for HNSW Migration Under Embedding Model Change Scenarios（arXiv:2611.25416，11 月 19 日提交，11 月 20 日上线，作者 Hengzhao Ma、Chenyang Zhu、Bin Wang、Xiaochun Yang）提出 STARR 方法，在嵌入模型更换、同一批对象被重新编码后迁移 HNSW 索引：比较同一源邻居列表在两种嵌入空间中的标准化边长并复用可复用的连接，再做修复 pass 保证每个顶点可达；MS MARCO、Wikipedia 与 CC3M 各百万级对象实验中，240 组有向迁移的中位构建提速 16.71 倍，Recall@10 中位损失 1 个百分点。
- [arXiv:2611.25416](https://arxiv.org/abs/2611.25416)

## 社交媒体

### 16. OpenAI 在 YouTube 发布《Meet the Data Agent in ChatGPT》（11/20）
OpenAI 11 月 20 日在 YouTube 发布视频《Meet the Data Agent in ChatGPT》（1 分 36 秒），作为 Data 插件系列的第一集：介绍如何在插件市场中找到 Data 插件、它如何与文件及已连接工具协同工作，以及数据质量检查、KPI 定义与追踪、产品与业务分析、市场规模测算等内置技能；同日还发布了同系列的《Ask Questions About Your Data in ChatGPT》《Connect Your Team's Data to ChatGPT》等视频。Data Agent 功能本身于 9 月 10 日随 ChatGPT Work 发布，本次为官方介绍视频。
- [YouTube @OpenAI（11/20）](https://www.youtube.com/watch?v=KrlfehIapEA)

本期检索范围内，11 月 16–18 日的 Alteryx、Starburst、Qlik、IBM Cognos、DataSwitch、SAS 与 Posit、英伟达 Rubin HPC、微软 Agent Controls 等发布为 Ignite 当周遗漏的补录条目，此前各期均未收录；ThoughtSpot Customer Hosted 已于 11 月 19 日一期收录，本期不再重复。国内大厂（阿里云、火山引擎、腾讯云、百度智能云、网易智企、华为云、京东云）与国内独立厂商（Aloudata、AskTable、数花智算、数势科技、帆软、思迈特、观远数据、Kyligence、衡石科技）当日均无数据代理相关的新发布；中文媒体 36氪、机器之心、量子位、InfoQ、DataFunTalk、Datawhale、dbaplus、墨天轮、和鲸当日均无数据智能体直接相关的新内容；WrenAI、DB-GPT、Chat2DB、Vanna、Apache Gravitino、Alpha-SQL、ReFoRCE、DeepEye-SQL、LAMBDA、Data Interpreter、DeepAnalyze、DocETL 当日均无新 Release；Spider 2.0、BIRD、DABstep、DAComp 等评测基准原作者团队当日无新动态；Hugging Face Papers 11 月 21 日日榜前列无与数据代理直接相关的论文；Tableau、Snowflake、Hex、Anthropic 当日无可核实的新发布；Workday 拟收购语义层厂商 Honeydew（11 月 18 日宣布）与 LanceDB 5,750 万美元 B 轮（11 月 17 日宣布）均在约 24 小时窗口之外，未作条目。

## 今日回顾

Databricks 宣布 Genie Agents 的 MCP 工具正式 GA；Emerson 与 Databricks 合作把工业 OT 数据接入 Databricks 平台；微软推出 Agent Controls 公共预览；Alteryx 推出 VURA 治理体验；Starburst 推出 Context Studio 私有预览；Qlik Answers 新增自定义技能与高级分析；IBM Cognos 12.2.0 发布、Query Agent 正式 GA；DataSwitch 推出 Mathi；SAS 与 Posit 合作面向受治理的生命科学 AI；英伟达发布 Rubin HPC GPU；Cube 更新日志新增 Cube Apps；华尔街日报报道 Databricks 正就约 2,250 亿美元估值的新一轮融资谈判；arXiv 上线 DSFlow、Solid 语义数据目录与 STARR 三篇论文；OpenAI 在 YouTube 发布介绍 ChatGPT Data Agent 的视频。
