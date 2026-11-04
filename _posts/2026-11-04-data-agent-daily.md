---
layout: post
title: "Data Agent Daily — 2026-11-04"
author: dad
date: 2026-11-04
image: "assets/images/covers/2026-11-04.svg"
description: "Snowflake 在 11 月 3 日 Expedition 2026 上发布 Business Ontology 与 Cortex AI Gateway，为 agent 提供经审批的业务定义与统一管控入口。"
categories: ["Data Agent Daily"]
tags: ["data-agent", "news"]
comments: false
---

## 今日速览

- Snowflake 在 11 月 3 日 Expedition 2026 上发布 Business Ontology 与 Cortex AI Gateway，前者记录经审批的业务概念定义，后者作为 agent 访问模型与数据的统一管控入口。
- Oracle 官方博客宣布 Data Science Agent 已在 Oracle Autonomous AI Database Serverless 26ai 上正式可用，对话式完成数据画像、特征准备、模型训练、评估与推理 SQL 生成。
- MariaDB 在 11 月 4 日发布 Enterprise Platform 2027，峰值吞吐较上一大版本高 56%，并加入 Agent Memory、Semantic Cache 与把自然语言问题转成只读 SQL 的 AI Retrieval。
- NVIDIA 的开源项目 Auto Ontology 在 11 月 3 日的报道中披露，该项目在企业元数据上构建语义层并通过 MCP 提供给 agent，报道时仓库约有 1,100 个 star。
- Zoho Analytics 在 10 月 28 日发布的版本中把 Ask Zia 改为协调六个专业 agent 的多 agent 架构，11 月 4 日的报道披露其连接器库在 500 个以上的基础上新增 30 多个。
- MIT Technology Review Insights 与 Snowflake 合作的报告在 11 月 2 日的报道中披露，受访企业中 agent 生成的洞察平均 48% 转化为业务改进行动，一年前为 37%。

## 公司发布 / 官方博客

### 1. Snowflake 发布 Business Ontology 与 Cortex AI Gateway，CoCo 与 CoWork 增加自动化能力（11/03）
Snowflake 在 11 月 3 日 Expedition 2026 上宣布一批 agent 相关能力，核心为 Horizon Catalog 内的两项内容。Business Ontology 是 Horizon Context 的新增能力，尚未进入公开预览，定位为记录业务概念官方含义的治理层：团队可审批“净收入”等核心概念的定义并将其与语义视图、表和视图连接，Cortex Sense 负责从已有上下文中发现定义、提出建议，人工负责人决定是否将其定为官方定义，获批定义优先于推断结果。Cortex AI Gateway 已进入公开预览，是 agent 访问模型与数据的集中入口，对跨云、跨框架、跨 AI 提供商的 agent 连接执行同一套策略，MCP 工具调用以最终用户身份认证并在执行前接受策略检查，Cortex AI Guardrails（公开预览）提供针对提示注入与越狱的运行时防护，可观测能力（正式可用）把每次模型调用、工具调用、推理步骤与护栏决策记录在客户自己的 Snowflake 账户内，成本治理能力（正式可用）可按团队、部门、agent 或应用归属 AI 花费并执行硬性预算上限，Dynamic Model Routing（私有预览）在内部测试中较纯前沿模型路径的 token 效率高出至多 3 倍。同批内容还包括 CoCo Automations（数据团队可配置由 agent 自主执行的 recurring 工作流）与 CoWork Bots（在团队已用工具中后台持续工作、仅在需要决策或签字时找人确认）。Snowflake 在通稿中引用 MIT Technology Review Insights 的调查口径：55% 的高管把缺乏业务上下文列为 agent 洞察质量低的首要原因，数据分散或不可达以 45% 居第二，上述调查为 Snowflake 赞助的研究。
- [Snowflake 官方博客（11/03）](https://www.snowflake.com/en/blog/ai-agents-governance-ai-security-cost-control/)
- [Business Wire 通稿（11/03，经 Bastille Post 转载）](https://www.bastillepost.com/global/article/6321117-snowflake-helps-enterprises-deploy-ai-agents-with-trusted-business-context-and-built-in-controls)

### 2. Oracle Data Science Agent 在 Autonomous AI Database Serverless 26ai 上正式可用（11/03 博客）
Oracle 官方开发者博客宣布，Data Science Agent 已在 Oracle Autonomous AI Database Serverless 26ai 上正式可用。该 agent 内嵌于 Oracle Machine Learning，以对话形式覆盖数据科学生命周期：发现并画像数据集、评估完整性与分布、整理数据与准备特征、计算相关性与筛选预测变量、训练库内分类与回归模型、评估并比较模型表现、解释指标与结果、生成用于评分与推理的 SQL。工作全程在库内运行，访问权限受用户在 Autonomous AI Database 中的角色与权限控制，可用 Conversation Objects 目录限定 agent 可见的表、视图与模型，日志、生成的 SQL、执行细节与对话历史用于追溯与复现。编排层使用 Oracle Select AI Agent 框架，模块化工具分别负责画像、数据准备与模型训练，SQL 生成由 Select AI 提供，模型方面包括 26ai 中的 XGBoost、支持向量机与广义线性模型等库内算法。使用前提为启用 Oracle Machine Learning 的 Autonomous AI Database Serverless 26ai 实例，并通过 DBMS_CLOUD 配置 LLM 凭证与 AI profile。
- [Oracle 官方博客](https://blogs.oracle.com/developers/oracle-data-science-agent-conversational-machine-learning-in-autonomous-ai-database)

### 3. MariaDB 发布 Enterprise Platform 2027：Agent Memory 与 Semantic Cache 进入平台（11/04）
MariaDB plc 在 11 月 4 日发布 MariaDB Enterprise Platform 2027，同时启用新的品牌标识。按通稿口径，该版本峰值吞吐较上一大版本高 56%，该数字来自 McKnight Consulting Group 2026 年 10 月的 HammerDB TPROC-C 测试（MariaDB Enterprise Server 12.3.3-0 对 11.8.3-1，Google Cloud 环境，MariaDB 赞助，非官方 TPC-C 结果）。与 agent 直接相关的四项内容为：AI Retrieval 通过一个托管服务把文档与实时运营数据作为 agent 的检索依据，并把自然语言问题转成只读 SQL；AI 插件把 MariaDB 知识带入 Claude Code 与 Codex 等 coding agent；Agent Memory 为 agent 提供跨会话共享的持久内存存储；Semantic Cache 对换一种表述的已问问题返回已存答案，以减少响应时间与 token 成本。平台其余内容包括在实时运营数据上做分析的 MariaDB Exa、原生向量搜索（较上一大版本每秒查询数高出至多 30%）、Raft 集群与多区域冲突检测及解决、统一的基于角色的访问控制、Bring Your Own Cloud 与 FIPS 140-3。通稿引用的 IDC 口径为：到 2027 年，G2000 企业 agent 使用量将增长十倍，token 与 API 调用负载增长一千倍。
- [Interface 报道（11/04）](https://interface.media/blog/2026/11/04/mariadb-launches-into-the-agentic-era-with-an-agent-ready-platform-and-a-bold-new-brand/)

### 4. Zoho Analytics 把 Ask Zia 改为六 agent 架构，连接器库新增 30 多个（10/28 发布，11/04 报道）
Zoho 在 10 月 28 日发布的 Zoho Analytics 新版本中，把对话式 BI 入口 Ask Zia 改为协调六个专业 agent 的多 agent 架构，六个 agent 分别覆盖数据分析、看板可视化、数据准备、公式创建、SQL 与数据科学或机器学习任务。按 11 月 4 日的报道口径，新版本的核心还有语义层与本体层：语义层与本体层内置于 Zoho Analytics，用于让 agent 使用经定义的业务含义。连接器方面，Zoho Analytics 在已有 500 多个连接器的基础上新增 30 多个。定价方面，Basic 套餐按年付费为每月 R336（南非兰特），覆盖 2 名用户、50 万行数据与 10,000 个 Zoho LLM 积分，云端更新已上线，部分功能在未来四到八周内向全球预览推出，本地部署版本预计 2027 年第一季度推出。Zoho Analytics 称全球每天有 100,000 家企业使用该平台。上述发布日期为 10 月 28 日，本期按“10 月 28 日发布、11 月 4 日报道”记录，不计为 11 月 4 日新发布。
- [Tech Nation 报道（11/04）](https://technation.news/zoho-analytics-adds-agentic-ai/)
- [8digits 报道（11/02）](https://8digits.net/news/zoho-analytics-six-ai-agents-ask-zia-revenue-test/)

## 新闻网站

### 5. MIT Technology Review Insights 报告：agent 洞察平均 48% 转化为业务改进行动（11/02 报道）
MIT Technology Review Insights 与 Snowflake 合作的报告在 11 月 2 日的报道中披露一组调查数字：受访企业中，分析 agent 生成的洞察平均 48% 转化为改进业务的行动，一年前同一批口径为 37%，其余 52% 未产生收入、成本规避或风险缓解方面的回报；55% 的高管把缺乏业务上下文列为 agent 洞察质量低的首要原因，数据分散或不可达以 45% 居第二。报道同时注明，该报告由 MIT Technology Review 的赞助内容部门制作、Snowflake 为商业合作方，报告未公开受访企业名单与抽样方法细节，数字为市场基准口径而非独立审计结果。本期把该报告列为与 Snowflake 11 月 3 日发布同一主题的配套调查口径，不把赞助方调查数字写成独立第三方审计结论。
- [iMasters 报道（11/02）](https://imasters.com/tecnologia/ai-agents-in-analytics-still-get-more-than-half-of-insights-wrong)

## 论文 / arXiv

本期检索范围内，arXiv 与 Hugging Face Papers 未见 11 月 4 日当天首投的、与数据代理直接相关的新论文；11 月 2 日至 5 日在底特律举行的 UIST 2026 上展示的 MUSE（arXiv:2608.16181，首投于 8 月 17 日）为数据科学 agent 的交互式元 agent 研究，本期不把 8 月首投的论文重复计为当日新论文。

## 开源项目

### 6. NVIDIA Auto Ontology：开源语义层通过 MCP 提供给 agent（11/03 报道）
NVIDIA 的开源项目 Auto Ontology 在 11 月 3 日的报道中披露，该项目以 Apache-2.0 协议开源，用 Python 与 TypeScript 实现，在企业元数据上构建语义图谱与目录，再通过 MCP、命令行与 API 提供给 agent 使用，默认模型为 Nemotron 3 Nano 30B A3B、Nemotron 3 Embed 1B 与 Llama Nemotron Rerank VL 1B v2，均经 NVIDIA NIM 调用，支持的数据源包括 Databricks、Postgres、Snowflake 与 DuckDB。报道时仓库约有 1,100 个 star 与 112 个 fork，并于 11 月 3 日当天出现在 Hacker News。按报道口径，完整 text-to-SQL agent 执行通常需要数十秒，返回结果分为答案、SQL 与数据行三个字段，agent 可直接复用 SQL 而无需解析自然语言文本。本期收录依据为 11 月 3 日的独立报道与仓库公开信息，未把 star 数写成项目质量结论。
- [ExplainX 报道（11/03）](https://explainx.ai/blog/nvidia-auto-ontology-open-source-context-layer-agents-mcp-text-to-sql-2026)

## 社交媒体

本期检索范围内，未见监测名单主体在过去 24 小时内发布新的 Data Agent 专帖；11 月 2 日发布的 SemiAnalysis GDPx 基准（206 项任务、Claude Opus 5.5 以 12.0% 居首）已载入 11 月 2 日版，11 月 4 日的讨论多为对该基准的复述，未见新的榜单或分数，本期不再重复计入。

## 今日回顾

Snowflake 在 11 月 3 日 Expedition 2026 上发布 Business Ontology 与 Cortex AI Gateway，为 agent 提供经审批的业务定义与统一管控入口；Oracle Data Science Agent 在 Autonomous AI Database Serverless 26ai 上正式可用，对话式覆盖画像、特征准备、建模、评估与推理 SQL 生成；MariaDB 在 11 月 4 日发布 Enterprise Platform 2027，峰值吞吐较上一大版本高 56%，并加入 Agent Memory 与 Semantic Cache；NVIDIA 开源项目 Auto Ontology 在 11 月 3 日的报道中披露其语义层通过 MCP 提供给 agent；Zoho Analytics 在 10 月 28 日发布的版本中把 Ask Zia 改为六 agent 架构；MIT Technology Review Insights 与 Snowflake 合作的报告在 11 月 2 日的报道中披露 agent 洞察平均 48% 转化为业务改进行动；本期检索范围内未见监测名单主体过去 24 小时内的新 Data Agent 专帖，arXiv 当天亦未见与主题直接相关的新首投论文。
