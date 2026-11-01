---
layout: post
title: "Data Agent Daily — 2026-10-27"
author: dad
date: 2026-10-27
image: "assets/images/covers/2026-10-27.svg"
description: "今日速览：Hex 发布从头重写的 4.0 并完成 1 亿美元 D 轮（估值 12 亿美元）；SAP 在 TechEd 发布 Joule Studio/Joule Work 扩展与表格基础模型 SAP-RPT-2.0；a16z 报告称 Databricks 上 agent 查询量已超过人类、每天启动 1,700 万个数据库；dbt Labs 博客复盘 LangChain 分层上下文做法，自助分析提问量增长 40 倍。"
categories: ["Data Agent Daily"]
tags: ["data-agent", "news"]
comments: false
---

## 今日速览

- Hex 发布从头重写的 Hex 4.0，并完成 1 亿美元 D 轮融资、估值 12 亿美元，4.0 目前为 private beta。
- SAP 在柏林 TechEd 大会发布 Joule Studio 与 Joule Work 的扩展：可从 70 多个 AI 模型中选用，配套表格基础模型 SAP-RPT-2.0。
- a16z 发文披露 Databricks 平台数据：agent 发起的查询已多于人类，每天启动超过 1,700 万个数据库，Lakebase 年化收入运行率突破 1 亿美元。
- dbt Labs 博客复盘 LangChain 的分层上下文体系：自助分析提问量增长 40 倍。
- Hex 4.0 的消息登上 Hacker News 并引发讨论，帖子获得 60 条评论。

## 公司发布 / 官方博客

### 1. Hex 发布 4.0 并完成 $100M D 轮，估值 $12 亿（10/27）
Hex 宣布从头重写的数据分析平台 Hex 4.0，同时完成 1 亿美元 D 轮融资、估值 12 亿美元，由 Peak XV 与 137 Ventures 领投，Amplify、Avra、a16z、Redpoint、Sequoia、Zero Prime 等参投。CEO Barry McCardel 称旧产品加了四年 AI 仍“远非 agent native”：agent 工具箱膨胀到数百个、外部 agent 只能走 MCP、计算引擎不是为高并发 agent 工作流设计的。4.0 的做法是让项目逻辑与可视化全部由代码文件支撑（而非专有 YAML），叠加受治理的上下文与审查工具；外部 agent（Claude、Codex、Cursor）可直接调用 Hex 平台；新执行引擎支持并行执行与结果流式返回，官方称内部关键应用全量运行时间大幅缩短。公司称全球客户超 2,500 家，刚录得历史最佳季度；4.0 目前仍处 private beta，定价与 agent 计量细节尚未公布。
- [Hex 官方：Introducing Hex 4.0](https://hex.tech/blog/introducing-hex-4-0/)
- [Hex 官方：$100M 融资公告](https://hex.tech/blog/hex-new-era/)
- [CryptoBriefing 报道](https://cryptobriefing.com/hex-100-million-series-d-ai-agents/)

### 2. SAP TechEd：Joule Studio / Joule Work 扩展与表格基础模型（10/27）
SAP 在柏林举行的 TechEd 大会上发布一系列 AI 更新。Joule Studio 支持无代码与专业代码两种方式构建、扩展 agent，可从 70 多个 AI 模型中选用；早期采用客户可在 Joule Studio 内设计并运行 n8n 工作流，更广泛开放随后跟进；选定客户在 SAP 托管的 Joule Studio runtime 上部署、运行自定义 agent 可免费至 2026 年 12 月。Joule Work 增加可推理、规划并跨 SAP 系统执行多步任务的 agentic 能力，在 Joule Studio 构建的 agent 可部署到其 runtime，并出现在 SAP AI Agent Hub 与 Joule Work 会话中；SAP 还公布了让第三方 agent 经受治理的入口调用 Joule Agents 的网关能力。数据侧，SAP Business Data Cloud 与 SAP Knowledge Graph 为 agent 提供业务数据与上下文；新模型方面，SAP-RPT-2.0 是面向结构化数据的表格基础模型，支持多表异常与离群检测，配套时间序列预测模型 SAP-RPT-TS；SAP 还与 HPE 合作把 SAP-RPT 部署到国际空间站的 Spaceborne Computer-2 上做在轨异常监测。企业 AI 网关（Enterprise AI Gateway）与知识图谱等部分能力计划在 2027 年第一季度推出。
- [SAP 官方发布稿（PRNewswire 转载）](https://www.tradingview.com/news/prnewswire:da7283c600ab9:0-sap-empowers-ai-developers-to-build-what-matters-and-turn-intent-into-autonomous-execution/)
- [ERP Today 报道](https://erp.today/sap-teched-2026-whats-rolling-out-and-whats-planned-through-2027/)

### 3. dbt Labs 博客：LangChain 如何用分层上下文把自助分析问题量做到 40 倍（10/27）
LangChain 的分析工程团队在 dbt Labs 博客复盘其 Hex agent 的上下文体系：第一层是 dbt 项目本身——表与字段描述同步进 BigQuery，任何读 BigQuery 的 agent 都继承同一套描述；Hex agent 还能直接读 dbt 仓库与 DAG，理解模型上下游与 SQL 逻辑。在此之上再叠三层：写在 dbt 仓库里、经 GitHub Action 导入 Hex 的 workspace guides（业务概念，如 ARR 口径）；代码化的语义层（指标与 join 关系）；以及“背书”机制（只把少数 mart 模型与看板标为可信源，改动需数据团队评审）。结果是自助分析提问量增长 40 倍；LangChain 官方口径还提到近 30 天约有 2,200 次 agent 会话。下一步是补 evals 并用 Hex CLI 继续丰富上下文。
- [dbt Labs 博客](https://courses.getdbt.com/blog/langchain-self-serve-analytics-ai-agent-context)
- [LangChain 官方复盘](https://www.langchain.com/blog/agent-data-stack)

## 新闻网站

### 4. a16z 发文披露 Databricks agent 用量：查询量已超人类，每天启动 1,700 万个数据库（10/27）
风险投资机构 a16z 于 10 月 27 日发布 Ben Horowitz 与 Michael McGuiness 合写的《Databricks & the Future of the Firm》，首次披露一组使用量数据：Databricks 平台上 AI agent 发起的查询已经多于人类，每天启动超过 1,700 万个数据库；三年前平台上的交互还全部来自人类。承载这批 agent 活动的 Lakebase（无服务器 Postgres，源于 2025 年 5 月约 10 亿美元收购的 Neon）年化收入运行率已突破 1 亿美元，约占 Databricks 70 亿美元总运行率的 1.4%；Lakehouse 数据仓库线年化收入超过 15 亿美元、同比增长逾 100%。文中还引述 Databricks 内部测试：给 agent 接入公司 ontology 后，回答准确率从约 50% 提升到 84.5%。需注意口径：a16z 是 Databricks 的早期投资方且 Horowitz 任其董事，以上数字为公司自报、未经审计。
- [The Inference 报道与核查](https://theinference.org/article/agents-launch-17-million-databases-a-day-on-databricks-the-line-they-feed-makes-100-million)

## 社交媒体

### 5. Hacker News：Hex 4.0 重写引发开发者讨论（10/27）
Hex “删掉原有代码、从头重写产品并同时完成 1 亿美元融资”的消息 10 月 27 日登上 Hacker News，帖子获得 60 条评论，讨论集中在重写风险与 agent-native 架构的取舍。
- [Hacker News 讨论（镜像页）](https://zeli.app/story/50265413)

说明：今日检索未见 X / Instagram / Facebook / LinkedIn / Reddit 上有其他可核实的 Data Agent 热帖，Google Cloud、Microsoft、Snowflake 官方博客当日亦无新的 Data Agent 专帖。

## 今日回顾

Hex 发布 4.0 并完成 1 亿美元 D 轮（估值 12 亿美元）；SAP 在 TechEd 发布 Joule Studio/Joule Work 扩展、表格模型 SAP-RPT-2.0，并公布 2027 年一季度的网关与知识图谱计划；a16z 披露 Databricks 上 agent 查询量已超人类、每天启动 1,700 万个数据库、Lakebase 年化收入破 1 亿美元；dbt Labs 博客公开 LangChain 分层上下文做法，自助分析提问量增长 40 倍；Hex 4.0 在 Hacker News 获得 60 条评论。
