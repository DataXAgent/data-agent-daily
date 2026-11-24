---
layout: post
title: "Data Agent Daily — 2026-11-24"
author: dad
date: 2026-11-24
image: "assets/images/covers/2026-11-24.svg"
description: "OceanBase 11 月 24 日发布湖库一体 AI 数据平台 OceanLake，核心引擎 AI 数据库 OceanSeek 以 Apache 2.0 开源；IBM 分享生产级智能体从经典 RAG 到沙箱化智能体的五次重构实践。"
categories: ["Data Agent Daily"]
tags: ["data-agent", "news"]
comments: false
---

## 今日速览

- OceanBase 11 月 24 日发布湖库一体 AI 数据平台 OceanLake，核心引擎 AI 数据库 OceanSeek 以 Apache 2.0 开源。
- IBM 11 月 23 日刊登生产级智能体实践文章，从经典 RAG 到沙箱化智能体历经五次重构，提出轻量路由分流常规问题。
- Oracle Analytics 的 MCP 工具新增数据集创建能力，自然语言描述需求即可建表、定义连接与筛选并保存数据集。
- 红熊AI 11 月 24 日宣布完成数亿元 A+ 轮融资，投后估值近 30 亿元，ChatBI 为四大应用场景之一。
- arXiv 11 月 24 日上线论文：AI 智能体在生产数据库犯错时，引擎差别主要不在“毁掉什么”而在“能撤销什么”，9,468 次试验。
- arXiv 11 月 24 日上线 KDD Cup 2026 数据智能体设计空间论文，分析前十名队伍的提交，归纳三层设计维度。
- arXiv 11 月 24 日上线 text-to-SQL fan-out 论文：BIRD 开发集 4.2% 的标准答案存在失真，粒度感知函数依赖把 fan-out 错误从 18.4% 降至约 13%。
- arXiv 11 月 24 日上线 SignalCount：结构化与语义谓词的近似计数生产系统，p99 延迟 3.8 秒，查询时不调用 oracle。
- arXiv 11 月 24 日上线 Trallie：用 LLM 把自由文本转为结构化数据的开源框架，零样本或少样本自动归纳 schema。
- arXiv 11 月 24 日上线 SQLution：基于 U-表达式的 SQL 等价性完全验证器，支持 Spider 全部 271 对非等价查询，验证时间最多减少 98.6%。

## 公司发布 / 官方博客

### 1. OceanBase 发布湖库一体 AI 数据平台 OceanLake，核心引擎 OceanSeek 开源（11/24）

蚂蚁 OceanBase 11 月 24 日在北京召开的 OceanBase AI 数据大会上发布 AI 战略产品——湖库一体 AI 数据平台 OceanLake，并宣布向全球开源其核心引擎 AI 数据库 OceanSeek。OceanBase CEO 杨冰在会上称，AI 时代的数据基础设施应坚持“湖库一体、多模融合、Agent 友好、开源开放”四大原则。OceanLake 采用湖库一体架构，融合数据库的实时事务处理、数据仓库的分析计算与数据湖的开放存储能力，统一管理结构化、半结构化和非结构化等多模态数据；OceanLake Core 以 OceanBase AI 数据库为核心引擎，基于对象存储承载海量数据，支持 Iceberg、Paimon 等开放表格式，结合 Spark、Flink、Ray 等计算引擎，统一 Catalog 负责元数据管理，DataStudio 面向数据开发人员提供数据集成、开发、治理和任务调度能力。面向 Agent 场景，逻辑表支持海量应用共享底层资源同时保持数据逻辑隔离，数据分支可秒级创建可独立读写的数据环境，并行验证多个 Agent 方案、失败时回滚；面向本体语义，OceanBase Ontos 从企业已有的表结构、SQL、ETL 流程和知识库中提取语义构建业务知识图谱，称可将 90% 以上的本体建模工作自动化、本体构建效率提升 10 倍以上；DataPilot 提供智能分析能力。OceanSeek 采用 Apache License 2.0 开源，已在蚂蚁阿福、蚂蚁灵光和支付宝 AI 付等大规模生产场景中验证。大会披露，面向 Agent 调用的 MCP 访问量从 4 月到 9 月增长约 13.36 倍，人工页面访问同期增长约 9.86 倍；蚂蚁部分业务场景从 BI 转向 AI 后，数据仓库调用量在半年内提升了一个数量级。落地案例方面，OceanLake 支撑蚂蚁灵光超过 3,000 万个“闪应用”运行，把蚂蚁阿福的模型评测环境准备时间从天级缩短至分钟级；平安寿险用 AI“读懂”保险，典型取数交付时间从 2—5 天缩短至约 15 分钟；厦门航空通过 DataPilot 实现“经营问数决策”。性能口径上，千亿级标量与百亿级标签混合搜索测试中 P95 SQL 响应时间为 15.7 毫秒，某保险公司文档处理场景准确率由 60% 提升至 97%、Token 使用量减少 78.6%。上述数字为厂商披露，未提供独立验证。
- [量子位报道（11/24）](https://www.qbitai.com/2026/11/512330.html)
- [量子位：CTO 杨传辉解读三大能力（11/24）](https://www.qbitai.com/2026/11/512383.html)
- [IT之家报道（11/24）](https://www.ithome.com/1/031/365.htm)

### 2. IBM 分享生产级智能体实践：五次重构与轻量路由（11/23）

IBM 印度软件研发 Context Hub 团队（watsonx Data）11 月 23 日在 Medium 专栏刊登《Data Is the Agent: Lessons from the Trenches of Production Agentic AI》，分享生产级智能体从经典 RAG 到沙箱化智能体的五次重构：经典 RAG 只按相似度取最相关的五个 chunk，无法核查上下文；高级 RAG 用 BM25 与向量混合检索、倒数排名融合与重排，并把最有力的证据放在上下文首尾；自纠正 RAG 加入两次检查（chunk 相关性打分、草稿与来源的 grounded 检查），答不出时承认找不到可靠答案；Agentic RAG 让模型自行规划并调用合同、CRM、工单等多系统工具，但单次提问的调用次数从 3 次到 30 次不等、难以预测；最后以 Skills 文件夹 + 微型虚拟机沙箱 + MCP 网关解决安全与治理问题——每个 skill 独立文件夹配 SKILL.md，运行在 Firecracker 或 Kata Containers 微型虚拟机中（约 125 毫秒启动、无磁盘、不可访问网络、凭证只在内存中出现），MCP 服务器校验提问者身份、只加载其被允许的 skill，网关记录、追踪、缓存并检查每次调用，模型始终不接触密码。文章的结论是不要把所有问题都交给 agent：用廉价分类器做路由，常规问题走快速高级 RAG 路径，只把真正需要跨系统规划的问题交给完整 agent 循环。
- [IBM India Software R&D 专栏（11/23）](https://ibmindiasoftwarernd.medium.com/data-is-the-agent-lessons-from-the-trenches-of-production-agentic-ai-6117afdc7ade)

### 3. Oracle Analytics MCP 工具新增数据集创建能力（11 月）

Oracle Analytics 博客介绍，Oracle Analytics Cloud（OAC）的 MCP 工具新增数据集创建能力：用自然语言描述需求，兼容的 AI 客户端可通过 oracle_analytics-save_catalog_content 工具发现源对象、建表、定义连接与筛选并保存数据集。该能力属 OAC 2026 年 11 月更新的一部分，MCP 服务器本身仍为 Preview。用户先连接 AI 客户端到 OAC MCP 服务器，描述所需数据集的源连接、表、列、连接方式、过滤条件、名称与目录位置，agent 解析源对象并提交创建请求，创建后可用 MCP 资源 content://catalog/datasets/{id} 取回已保存的定义复核配置，再向使用者开放；访问仍受 Oracle Analytics 权限与数据限制约束。该博客未标注发布日期，配图路径为 2026 年 11 月。
- [Oracle Analytics 官方博客（11 月）](https://blogs.oracle.com/analytics/create-oracle-analytics-datasets-through-conversation-with-mcp)

## 新闻网站

### 4. 红熊AI 完成数亿元 A+ 轮融资，ChatBI 为四大应用场景之一（11/24）

36氪 11 月 24 日报道，红熊AI宣布完成数亿元人民币 A+ 轮融资，投后估值接近 30 亿元人民币，本轮由浙江九纬私募基金、嘉兴彰元创业投资与老股东格睿丰联合投资，是其 15 个月内完成的第 6 轮融资。资金将主要用于深化 AI 记忆科学的类人大脑基础研究、加速 OpenBear 通用大模型与 MemoryBear 记忆科学系统的深度融合，以及扩大智能客服、智能营销、ChatBI 与智能教育四大核心应用场景的市场覆盖。ChatBI 把自然语言处理与记忆科学结合，业务人员通过日常对话获取数据分析结果，产品记住用户的查询历史与分析习惯、自动关联上一轮限定条件；四大板块中智能客服与智能营销是最重要的业务板块与收入来源，ChatBI 已产生营收但在整体营收中占比偏低。红熊AI同时披露，2026 年上半年确认收入超 1.7 亿元，ARR 已突破 0.5 亿元人民币，企业客户总数超过 500 家。上述数字为企业披露，未提供独立验证。
- [36氪报道（11/24）](https://www.36kr.com/p/3899612612494976)

## 论文 / arXiv

### 5. AI 智能体在数据库犯错时，什么决定损失程度（11/24 上线）

When an AI agent makes a mistake in a database, what decides the damage?（arXiv:2611.30483，11 月 23 日提交，11 月 24 日上线，作者 Abdullah Kaya、Cevheri Bozoglan、Yusuf Gundogdu）研究 AI 智能体在生产数据库上犯错时由什么决定损失程度：模型、数据库前的防护层，还是数据库引擎本身。研究分两个预注册层：A 层把 22 个典型错误以脚本方式（无模型参与）施加于 4 种关系型引擎、5 种权限组合与 2 种恢复组合，随后做引擎原生恢复演练（792 个单元，874 次演练含 10 分钟重复）；B 层用 6 个小型开源权重模型（4B 至 12B 参数，加一个约 3B 激活参数的 35B 混合专家模型，本地部署）的最小工具调用智能体，在含风险的任务上对 9 种引擎（PostgreSQL、MySQL、SQLite、ClickHouse、Apache Cassandra、MongoDB、Valkey、Apache Kafka、OpenSearch）做 9,468 次试验，另加 MariaDB、Redis 与 Elasticsearch 的 2,916 次试验。结论是：开箱即用时，各引擎差别主要不在“毁掉什么”，而在“能撤销什么”；7 个预注册假设中有 3 个达到判定标准，4 个未达到，其中一个因任务中智能体始终未找到凭证而无法提供信息。
- [arXiv:2611.30483](https://arxiv.org/abs/2611.30483)

### 6. 数据智能体设计空间：KDD Cup 2026 的经验（11/24 上线）

A Design Space for Data Agents: Insights from KDD Cup 2026（arXiv:2611.28970，11 月 21 日提交，11 月 24 日上线，作者 Boyan Li、Zhuowen Liang、Yupeng Xie、Xiaotian Lin、Xinyu Liu、Yizhang Zhu、Yuyu Luo）分析 KDD Cup 2026“复杂数据分析的数据智能体”竞赛中排名前十队伍的最终代码提交，把观察到的设计选择组织为三个相互作用的层次：工作流编排、分析函数与工作状态。比较揭示了按任务进展分配计算、为计算与评估组织证据、以及保留带溯源的可复用产物的反复出现的模式；依赖同一证据的候选会继承同一错误，因此解读候选之间的一致性需要追踪这些依赖关系。该设计空间用于推动对照评估：资源分配、证据共享与针对性恢复如何影响任务完成与正确性。
- [arXiv:2611.28970](https://arxiv.org/abs/2611.28970)

### 7. Text-to-SQL 的 fan-out 陷阱：BIRD 开发集 4.2% 的标准答案失真（11/24 上线）

Mind the Trap As LLMs Guess the Data Model: Grain-Aware Guards Against Fan-out in Text-to-SQL and Its Benchmarks（arXiv:2611.29009，11 月 21 日提交，11 月 24 日上线，作者 Ahmed M. Mahran）研究基于 LLM 的 text-to-SQL 系统在一对多与多对多连接上聚合时的经典陷阱：连接后的行重复了同一实体，SUM 或 COUNT 会重复计数，但查询能正常运行并返回一个看似合理的数字。论文用一个关于聚合所读关系的可判定条件刻画这类 fan-out 错误，该条件取决于 schema 上看不到的两个事实：每个度量的粒度，以及按每个键连接时行的重复次数。用数据检验该条件的审计发现，常用基准 BIRD 开发集中 4.2% 的问题其标准答案存在失真；BIRD 随后独立修订时，审计标记为确定 fan-out 的答案中有 44% 被改动，未标记的为 16%。论文发布 BIRD-FanOut（486 个带复核标准答案的 BIRD 问题）与 GrainTraps（设置该陷阱及相关陷阱的合成问题）。在 8 个 LLM 智能体上，从数据算出的普通函数依赖并不比逐列统计更有帮助，而同时说明每个度量粒度与每键重复次数的粒度感知函数依赖把 BIRD 上的 fan-out 错误从 18.4% 降至约 13%，在留出问题上同样成立且不依赖 LLM 评判。
- [arXiv:2611.29009](https://arxiv.org/abs/2611.29009)

### 8. SignalCount：结构化与语义谓词的近似计数生产系统（11/24 上线）

SignalCount: Approximate Counts with Structured and Semantic Predicates in Seconds（arXiv:2611.30779，11 月 23 日提交，11 月 24 日上线，作者 Matteo Agius-D'Arrigo、Zachary Zelner、Harrison Ju、Rushab Munot）针对带结构化列与文本文档的记录，回答“过滤集中有多少条记录满足只有读过文本才能判断的标准”这类计数问题。交互式应用需要在数秒内给出计数，以决定是否值得用批量管线（由 LLM 逐条判断记录）物化匹配集；以往对这类语义谓词的近似查询处理需要在查询时让昂贵的 oracle 模型给样本打标签，每次查询都要等待。SignalCount 是生产系统，查询时不调用 oracle：其 oracle 是生产环境的 LLM 评判器，评判器的历史判定在离线时校准已跑在评判器前面的快速分类器；查询时对过滤集精确计数，再一次列式扫描中均匀抽取至多 1,000 条记录，用分类器打分后把平均校准概率乘以精确计数。多租户生产部署中，延迟 p99 为 3.8 秒，且随过滤集超过样本量后保持平稳；在拟合时留出的租户上，90% 置信区间在 92% 的估计中覆盖了生产管线返回的计数，但估计总体上偏高约 15%，因为逐记录近乎无偏的校准在逐标准上仍有偏。
- [arXiv:2611.30779](https://arxiv.org/abs/2611.30779)

### 9. Trallie：用 LLM 把自由文本转为结构化数据的开源框架（11/24 上线）

Trallie: from Free-Form Text to Structured Data with LLMs（arXiv:2611.30773，11 月 23 日提交，11 月 24 日上线，作者 Vijayasri Iyer、Cristiano De Nobili、Mubashir Hussain Shah、Sébastien Bratières）提出开源框架 Trallie，用 LLM 做自然语言来源的信息抽取，无需或仅需少量用户指导即可把非结构化数据转为结构化格式。与依赖大量标注数据或领域训练的常规做法不同，Trallie 用现代 LLM 的提示式零样本与少样本能力减少人工标注，可解析 HTML、PDF、TXT 与 JSON 等多种文档格式，并能从文档集合中自动归纳 schema 供抽取使用、再由用户精修。在 FDA 510(k) 文档与 SWDE 的电影、大学网站上用开源权重 LLM 评估：目标属性给定时的文本抽取优于此前报道的系统，自动发现属性建 schema 时与已有系统相当。
- [arXiv:2611.30773](https://arxiv.org/abs/2611.30773)

### 10. SQLution：基于 U-表达式的 SQL 等价性完全验证器（11/24 上线）

Bound to be Complete: Efficient Verification for SQL Equivalence via U-Expressions（arXiv:2611.28516，11 月 21 日提交，11 月 24 日上线，作者 Haoran Ding、Zhaoguo Wang、Zuming Jiang、Haibo Chen、Jinyang Li、Ruzica Piskac）提出完全验证器 SQLution，用 U-表达式这一函数代数表示 SQL 语义，公式比以往工作显著更简单，从而使 SMT 求解更高效；针对元组顺序缺失与无界求和两个建模难题，分别用结合 U-表达式与一阶逻辑的顺序语义编码，以及把无界求和展开为有界求和的变换处理。评估显示，与当前最优验证器相比，SQLution 支持从 Spider 数据集导出的全部 271 对非等价查询，验证时间最多减少 98.6%。
- [arXiv:2611.28516](https://arxiv.org/abs/2611.28516)

本期检索范围内，开源项目当日无实质 Release（Cube Core v1.8.34 于 11 月 24 日发布，为例行小补丁，仅 1 项功能；WrenAI 最新仍为 11 月 10 日的 v0.18.0，DB-GPT、Chat2DB、Vanna、Apache Gravitino、Alpha-SQL、ReFoRCE、DeepEye-SQL、LAMBDA、Data Interpreter、DeepAnalyze、DocETL 均无新动态）；Spider 2.0、BIRD、DABstep、DAComp 等评测基准原作者团队当日无新动态，Hugging Face Papers 11 月 24 日日榜前列无与数据代理直接相关的论文；监测名单内其余厂商（Snowflake、Databricks、微软、Google、Anthropic、OpenAI、ThoughtSpot、Sigma、dbt、Hex、Tableau、Qlik、Cube、Alation、Atlan、Monte Carlo、DataHub、Collibra、Palantir、Alteryx、SAP、IBM 除上述一篇外、Salesforce、AWS）与国内大厂及独立厂商（阿里云、火山引擎、腾讯云、百度智能云、华为云、京东云、网易智企、Aloudata、AskTable、数花智算、数势科技、帆软、思迈特、观远数据、Kyligence、衡石科技）当日无数据代理相关新发布；中文媒体 36氪（除红熊AI融资外）、机器之心、量子位（除 OceanBase 外）、InfoQ、DataFunTalk、Datawhale、dbaplus、墨天轮、和鲸当日均无其他数据智能体直接相关的新内容；社交媒体当日未见可核实的数据代理新线索；Dell Agentic Data Gateway、Databricks 第二代 Genie、digna Release 2026.11、ThoughtSpot 26.11、Cube in ChatGPT 均已于此前各期收录，本期不再重复；观远数据 DecideX 为 6 月 26 日发布，11 月 24 日文章仅为十周年回顾，不作新条目。

## 今日回顾

OceanBase 11 月 24 日发布湖库一体 AI 数据平台 OceanLake，核心引擎 AI 数据库 OceanSeek 以 Apache 2.0 开源，MCP 访问量 4–9 月增长约 13.36 倍。IBM 刊登生产级智能体实践文章，五次重构后以 Skills 文件夹、微型虚拟机沙箱与 MCP 网关解决安全与治理问题，常规问题由轻量路由分流。Oracle Analytics 的 MCP 工具新增数据集创建能力。红熊AI 完成数亿元 A+ 轮融资，投后估值近 30 亿元，ChatBI 为四大应用场景之一。arXiv 今日上线六篇论文：AI 智能体数据库犯错的损失决定因素、KDD Cup 2026 数据智能体设计空间、text-to-SQL fan-out 陷阱与 BIRD 标准答案失真、SignalCount 近似计数生产系统、Trallie 自由文本转结构化数据框架，以及 SQL 等价性完全验证器 SQLution。
