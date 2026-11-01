---
layout: post
title: "Data Agent Daily — 2026-10-25"
author: dad
date: 2026-10-25
image: "assets/images/covers/2026-10-25.svg"
description: "今日速览：Google Cloud 的 Data Agent Kit 于 10 月 24 日正式 GA，免费开源、含 37 个 skills、连接 15+ 项 Google Data Cloud 服务；Meta 确认收购 AI 分析初创 Sundial，并入其 DATA（Data Analytics Tooling & Agents）部门。"
categories: ["Data Agent Daily"]
tags: ["data-agent", "news"]
comments: false
---

## 今日速览

- Google Cloud 的 Data Agent Kit 于 10 月 24 日正式 GA（general availability）：免费开源，含 37 个 Apache 2.0 skills，经 MCP 连接 15+ 项 Google Data Cloud 服务，GA 版新增 BigQuery Graph、Bigtable 与 Managed Service for Apache Spark 支持。
- Meta 确认收购 AI 数据分析初创 Sundial，收购价未披露；Sundial 累计融资 2,300 万美元，将并入 Meta 新设的 DATA（Data Analytics Tooling & Agents）部门，交易完成后停止服务外部客户。
- 费城联储经济学家 Minchul Shin 的工作论文（WP 26-41，8 月发表）本周末获多家媒体报道：其 AI agent 在多次独立运行中找到了优于原研究基准的预测组合方法，但部分改进未通过留出集（holdout）检验。
- Meta 首席数据官 Alex Schultz 在 LinkedIn 发帖宣布 Sundial 交易，并称 Chandra Narayanan 将负责 Meta 的分析工具与 agents 工作。
- Google Cloud 开发者布道师 Jeff Nelson 在 LinkedIn 回复 Data Agent Kit 的只读隔离问题：用只读服务账号或 IAM deny policy 在平台层拦截写操作工具。

## 公司发布 / 官方博客

### 1. Google Cloud：Data Agent Kit 正式 GA（10/24）
Google Cloud 产品经理 Arun Nair 与开发者布道师 Jeff Nelson 在官方博客宣布 Data Agent Kit 正式 GA。这是一套免费的 MCP 工具与 Google 官方 agent skills，让用户现有的编程 agent（Antigravity、Claude Code、Codex、Cursor 及 VS Code 兼容编辑器）直接对接 Google Cloud 数据产品，并预装在 Cloud Shell 与 Cloud Workstations 中。工具包经 MCP 服务器连接 15+ 项 Google Data Cloud 服务，附 37 个 Apache 2.0 开源 skills（例如优化 BigQuery SQL、设计 Bigtable row key）；GA 版新增 BigQuery Graph、Bigtable 与 Managed Service for Apache Spark 支持，此前版本为 9 月 29 日的 1.0.0 与 10 月 13 日的 1.1.0。安全护栏分两层：skills 层是建议性的最佳实践（含 accidental-data-loss-prevention，要求 agent 在执行 DROP TABLE、无 WHERE 的 DELETE 等破坏性命令前先取得用户明确同意）；IAM 层是强制执行，可用只读服务账号运行 agent，或用 deny policy 拦截 tool.isReadOnly 为 false 的工具调用。除所用 Google Cloud 服务本身的费用外，工具包不另收费。
- [Google Cloud 官方博客：Data Agent Kit is now GA](https://cloud.google.com/blog/topics/developers-practitioners/data-agent-kit-is-now-ga-bring-google-data-cloud-to-any-coding-agent)
- [TechGig 报道（10/24）](https://techgig.com/amp/news/ai/google-data-agent-kit-now-generally-available-for-coding-agents/135171564)

## 新闻网站

### 2. Meta 收购 AI 分析初创 Sundial，并入 DATA 部门（10/23 确认，10/24 报道）
Meta 发言人向 Axios 确认收购 AI 数据分析平台 Sundial，价格未披露，消息于 10 月 23 日确认、10 月 24 日被多家媒体报道。Sundial 于 2021 年由两位前 Meta 高管 Julie Zhuo 与 Chandra Narayanan 创立，做自然语言自助分析（通过聊天插件把提问转成分析结论），累计融资 2,300 万美元，其中 2025 年 7 月完成由 GPV 的 DJ Patil 领投、Sequoia Capital 参投的 1,600 万美元 A 轮；客户名单包括 OpenAI。Sundial 将并入 Meta 今年 7 月新设的 Data Analytics Tooling & Agents 部门（简称 DATA），由 Meta 首任首席数据官 Alex Schultz 负责；Narayanan 将领导 Meta 的分析工具与 agents 工作，Zhuo 一并加入。交易完成后 Sundial 停止服务外部客户。
- [CryptoBriefing 报道](https://cryptobriefing.com/meta-acquires-ai-data-platform-sundial/)
- [Dealroom 报道](https://dealroom.co/news/165523-meta-buys-ai-analytics-startup-sundial-founded-by-two-of-its-alumni/)

### 3. 媒体报道费城联储 AI agent 研究论文：agent 自主做预测组合研究（10/24–10/25 报道）
多家媒体在本周末报道费城联储高级经济顾问 Minchul Shin 的工作论文 WP 26-41《An Auditable AI Agent Loop for Empirical Economics》（论文本身发表于 2026 年 8 月，此条为 10 月 24–25 日的媒体报道）。该研究把开源 agent-loop 架构改造成可审计的实证经济学研究流程：写入指令契约、固定评估器、单一可编辑脚本与完整实验日志，并增加搜索后的留出集评估。在预测组合（forecast combination）案例中，agent 的多次独立搜索找到了优于原研究基准的方法；但论文同时指出，部分改进在留出集上未能复现，属于对样本的过拟合。报道还引述行业背景称，高盛、摩根大通、花旗与巴克莱等大行已把初级分析师班次削减至多三分之二（此为报道引述口径）。
- [Startup Fortune 报道](https://startupfortune.com/ai-agents-are-starting-to-do-the-work-of-research-economists-on-wall-street/)
- [费城联储：论文原文页](https://www.philadelphiafed.org/the-economy/an-auditable-ai-agent-loop-for-empirical-economics-a-case-study-in-forecast-combination)

## 社交媒体

### 4. LinkedIn：Alex Schultz 发帖宣布 Sundial 加入 Meta DATA 部门（10/23）
Meta 首席数据官 Alex Schultz 在 LinkedIn 发帖公布 Sundial 并入其负责的 DATA 部门，并明确组织安排：Chandra Narayanan 负责 Meta 的 data analytics tooling and agents 工作。帖文内容由 Axios 及后续多家媒体在报道收购时转述。
- [CryptoBriefing 报道（含 LinkedIn 帖文信息）](https://cryptobriefing.com/meta-acquires-ai-data-platform-sundial/)

### 5. LinkedIn：Jeff Nelson 回复 Data Agent Kit 的只读隔离做法（10/24 前后）
Google Cloud 开发者布道师 Jeff Nelson 在 LinkedIn 上被问到 Data Agent Kit 如何把只读调研与能改基础设施的工具隔离开，他回复称这件事在 IAM 层解决、不靠单个 agent 的设置：通过 impersonation 让 agent 以只读服务账号运行，或配置 IAM deny policy，拦截 mcp.googleapis.com/tools.call 中 tool.isReadOnly 为 false 的调用，可在组织、文件夹或项目层级生效。
- [LavX News 报道（转述 LinkedIn 问答）](https://news.lavx.hu/article/google-data-agent-kit-reaches-general-availability-splits-guardrails-between-skills-and-iam)

说明：本期社交媒体可核实内容主要来自 LinkedIn 且多为媒体转述；X、Instagram、Facebook、Reddit 上未检索到 10 月 24 日晚至 10 月 25 日窗口内可核实的 Data Agent 新热帖，故不单列。

## 今日回顾

Google Cloud 的 Data Agent Kit 于 10 月 24 日正式 GA，37 个开源 skills、15+ 项服务接入与 skills+IAM 双层护栏一并落地；Meta 确认收购累计融资 2,300 万美元的 Sundial，并入新设 DATA 部门、由回巢的 Chandra Narayanan 负责分析工具与 agents；费城联储 WP 26-41 的 AI agent 经济学研究在本周末获媒体集中报道，其预测组合改进部分通过、部分未通过留出集检验；社交媒体侧，Alex Schultz 与 Jeff Nelson 的两条 LinkedIn 动态分别对应上述收购与 GA 的组织与技术细节。
