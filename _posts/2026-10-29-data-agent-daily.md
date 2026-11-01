---
layout: post
title: "Data Agent Daily — 2026-10-29"
author: dad
date: 2026-10-29
image: "assets/images/covers/2026-10-29.svg"
description: "今日速览：Signal65 发布 Snowflake 与 Databricks agentic 评测，CoCo 以 68 分钟跑完七阶段工作流、人工需 316 分钟；微软财报电话会披露 Fabric 付费客户 44,000 家、Agent 365 注册表中 agent 超 5,000 万个。"
categories: ["Data Agent Daily"]
tags: ["data-agent", "news"]
comments: false
---

## 今日速览

- Signal65 发布 Snowflake 与 Databricks 企业级 AI 评测：Snowflake 的 CoCo 以 68 分钟跑完七阶段工作流，人工操作需 316 分钟。
- 微软在 FY27 第一财季电话会上披露：Fabric 付费客户达 44,000 家，Agent 365 注册表中的 agent 超过 5,000 万个。
- Cordial 发布 headless CDP：营销人员可在 Claude、ChatGPT、Microsoft Copilot 等 AI 助手里经 MCP 查询实时客户数据。
- Visual Crossing 在 HOOD Summit 2026 上线 Weather Trader，把天气数据接入 Robinhood 的 Agent Apps，定价每月 5 美元。
- 微软 CEO Nadella 在 LinkedIn 发帖汇总财报：近 60,000 家客户在使用 Microsoft IQ 上下文，Agent 365 注册 agent 数环比增超 30%。

## 公司发布 / 官方博客

### 1. 微软财报电话会：Fabric 付费客户 44,000 家，Agent 365 注册 agent 超 5,000 万（10/28 晚）
微软在 10 月 28 日晚举行的 FY27 第一财季电话会上披露一组数据与 agent 数字：季度营收 923 亿美元、同比增 19%，Microsoft Cloud 营收 639 亿美元、同比增 30%。数据层方面，付费 Fabric 客户达 44,000 家、同比增 50% 以上；超过 19,000 家客户同时使用 Foundry 与 Fabric，在实时运营、分析与非结构化数据之上构建和运行 agent；由 Work IQ、Fabric IQ 与 Foundry IQ 组成的 Microsoft IQ 已有近 60,000 家客户使用、环比增 25%。治理侧，Agent 365 注册表中的 agent 超过 5,000 万个、环比增 30% 以上；客户已用 Microsoft Purview 累计审计超过 76 亿次 agent 活动、环比达 5 倍。
- [微软 FY27 Q1 财报电话会实录（Roic AI）](https://www.roic.ai/quote/MSFT/transcripts/2027-year/1-quarter)
- [PYMNTS 报道（10/29）](https://www.pymnts.com/earnings/2026/microsoft-sees-enterprise-ai-adoption-accelerate-as-copilot-usage-grows/)

### 2. Cordial 发布 headless CDP，客户数据可从 AI 助手经 MCP 直接查询（10/29）
客户数据平台 Cordial 通过 PR Newswire 宣布其内嵌 CDP 转为 headless（无头）模式：营销人员可在 Claude、ChatGPT、Microsoft Copilot 或自建 agent 里探索和可视化实时客户数据，并把 Cordial 数据与 Google Analytics、Adobe Analytics、Shopify、Salesforce Commerce Cloud、Databricks、Snowflake 等系统的数据合并分析，用于圈选高价值受众与发现营收机会，底层经 Cordial 的 MCP 接口接入。Boot Barn、Torrid 等品牌已在使用该能力；Cordial 的客户还包括 Levi's、Tapestry、L.L.Bean 等，其平台每年发送数十亿条个性化消息。
- [Cordial 官方发布稿（PR Newswire，Morningstar 转载）](https://www.morningstar.com/news/pr-newswire/20261029de83865/cordial-launches-headless-cdp-bringing-real-time-customer-data-to-where-marketers-work)

### 3. Visual Crossing 把天气数据接入 Robinhood Agent Apps（10/29）
Visual Crossing 在休斯顿举行的 HOOD Summit 2026 上宣布推出 Weather Trader Agent App：Robinhood 用户可在 App 内创建 AI agent 进行研究、市场分析、策略制定，并在用户设定的控制范围内执行交易；Agent Apps 让这些 agent 接入第三方专业数据与分析工具。Weather Trader 让 Robinhood 的 agent 在调查供应链风险与价格扰动时调用短期天气预报；与它同批接入的还有 Nasdaq、Unusual Whales、Quiver Quantitative、Token Terminal、SpotGamma 等数据与分析服务商。该应用定价每月 5 美元、首月免费试用，底层由 Visual Crossing 的 Timeline Weather API 与 MCP 接口驱动。
- [Visual Crossing 官方发布稿（EIN Presswire，WCIA 转载）](https://www.wcia.com/business/press-releases/ein-presswire/952499794/visual-crossing-brings-weather-data-to-the-agentic-era-with-robinhood-agent-apps/)

## 新闻网站

### 4. Signal65 评测：Snowflake CoCo 68 分钟跑完七阶段工作流，人工需 316 分钟（10/29）
评测机构 Signal65 发布《Snowflake vs. Databricks: An AI and Enterprise Readiness Evaluation》：在两家平台上用美国交通部航班延误数据集搭建同一套七阶段场景——数据摄取、变换、治理与 PII 保护、构建应用、灾备故障切换、外部数据共享——同一批工程师在每个平台各跑两遍，一遍人工操作、一遍使用各自的 agentic 工具。结果：Snowflake 的 CoCo 以 68 分钟近乎自主地跑完全部七个阶段，人工操作需 316 分钟，相差 4.6 倍；治理与 PII 保护任务（掩码、打标、访问策略）Snowflake 比 Databricks 快 32%。Databricks 的 Genie Code 未能独立完成全部外部应用工作流，借助第三方 agent Claude Code 才完成同类流程、耗时约为 CoCo 的 4 倍。此外，Snowflake 在 30 分钟内配置了 AWS 到 Azure 的故障切换，评测未能在 Databricks 上复现同等跨云能力。说明：这是单一场景、单一评测机构的结果。
- [Signal65 评测原文](https://signal65.com/research/ai/snowflake-vs-databricks-an-ai-and-enterprise-readiness-evaluation/)

## 社交媒体

### 5. Nadella 在 LinkedIn 发帖汇总财报中的 agent 数字（10/28）
微软 CEO Satya Nadella 在财报电话会后于 LinkedIn 发帖：Microsoft Cloud 营收超 630 亿美元、同比增 30%；Foundry 营收同比增至三倍以上；公司正把 Foundry 与 Fabric 拉近，让客户在数据旁构建 agent；包括 Microsoft 365、Foundry、Fabric 在内的企业上下文经 Microsoft IQ 提供给 agentic 工作负载，近 60,000 家客户在用、环比增 25%；Agent 365 注册表中的 agent 超 5,000 万个、环比增 30%；OpenAI Codex、Anthropic Claude Code 与 Meta Muse 等 agent 正在采用微软在 Windows 上的 agent 运行容器。该帖获得 682 条评论。
- [Nadella 的 LinkedIn 帖子](https://www.linkedin.com/feed/update/urn:li:activity:7521344259774660609/)

说明：除上述 LinkedIn 帖外，今日未检索到 X / Instagram / Facebook / Reddit 上可核实的 Data Agent 相关新帖；Google Cloud、Databricks、Snowflake 官方博客今日亦无新的 Data Agent 专帖。

## 今日回顾

Signal65 发布 Snowflake 与 Databricks 对照评测，CoCo 68 分钟对人工 316 分钟、治理任务快 32%，Genie Code 未独立跑完全流程；微软财报电话会披露 Fabric 付费客户 44,000 家、Microsoft IQ 近 60,000 家客户、Agent 365 注册 agent 超 5,000 万个、Purview 累计审计 agent 活动超 76 亿次，Nadella 随后在 LinkedIn 发帖复述了这组数字；Cordial 发布 headless CDP，把客户数据经 MCP 开放给 Claude、ChatGPT、Copilot 等助手；Visual Crossing 的 Weather Trader 上线 Robinhood Agent Apps，定价每月 5 美元。
