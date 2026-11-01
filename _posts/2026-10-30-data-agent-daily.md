---
layout: post
title: "Data Agent Daily — 2026-10-30"
author: dad
date: 2026-10-30
image: "assets/images/covers/2026-10-30.svg"
description: "今日速览：ZoomInfo 的 MCP 连接器与 API 上线 Snowflake；Databricks 与 SAP 扩展合作，Genie、Lakeflow、Unity Gateway、Lakebase 将进入 SAP Databricks；雅诗兰黛与微软宣布多年战略合作，Copilot 已扩至 14,000 多名员工。"
categories: ["Data Agent Daily"]
tags: ["data-agent", "news"]
comments: false
---

## 今日速览

- ZoomInfo 的 MCP 连接器与 API 上线 Snowflake：业务用户可在 Snowflake CoWork 里用自然语言查询 ZoomInfo 数据，调用走 OAuth 2.0 并继承用户角色权限。
- Databricks 与 SAP 在 TechEd 上扩展合作：Genie、Lakeflow、Unity Gateway、Lakebase 将进入 SAP Databricks，并推出 SAP Application Data Foundation，双方未给出上线日期。
- 雅诗兰黛与微软宣布多年战略合作：推进 Unified Data Platform、投资 Unified Consumer Data Platform，Copilot 已扩至全球 14,000 多名办公室员工。
- Google Cloud 10 月 30 日发布说明：Knowledge Catalog 现可发现授权视图、逻辑视图与连续物化视图，该集成为正式可用（GA）。
- Databricks 10 月 30 日产品更新：Unity Gateway Skills 的使用可通过审计日志与用量看板追踪（Beta）；Unity Catalog 指标视图之间可记录连接关系（Beta）。

## 公司发布 / 官方博客

### 1. ZoomInfo MCP 与 API 上线 Snowflake（10/30）
ZoomInfo 宣布其 MCP 连接器与 API 已进入 Snowflake AI Data Cloud，均经由 GTM.AI（其 headless GTM 上下文层）接入。业务用户可在 Snowflake CoWork 里用自然语言查询 ZoomInfo 数据，经管理员批准后可暴露给 Snowflake Cortex Agents，agent 可检索其 GTM Context Graph（公司称覆盖 1 亿+公司、5 亿+联系人及数十亿购买信号）；数据团队则可用 Search、Enrich、Lookup、Bulk、Monitoring 五组端点实时或批量 enrich Snowflake 表，批量上限为每请求 10,000 条、每查询 200,000 条。每次调用走 OAuth 2.0 并继承用户在 ZoomInfo 内的角色权限，全部用量记入审计框架。连接器现已可用，需同时持有 Snowflake 账号与 ZoomInfo 订阅，价格未披露。
- [ZoomInfo 官方发布稿](https://www.zoominfo.com/newsroom/press-releases/zoominfo-mcp-api-launch-snowflake)

### 2. 雅诗兰黛与微软宣布多年战略合作，Copilot 扩至 14,000+ 员工（10/30）
雅诗兰黛公司与微软宣布扩大多年合作，内容包括云与数据基础建设和全公司范围的 AI 采用，围绕三项优先事项：新能力与增长、决策智能、生产力与自动化。数据侧的核心是基于微软技术建设的 Unified Data Platform，连接其各品牌、地区、渠道与职能的数据（公司称业务覆盖 24 个品牌、约 150 个国家和地区）；同时投资 Unified Consumer Data Platform，用于加深消费者洞察并支持从发现到购买的个性化体验。员工工具侧，Microsoft Copilot 已扩展到其全球办公室员工，使用人数超过 14,000。双方未披露财务条款与上线时间表。
- [Microsoft Source 报道](https://news.microsoft.com/source/features/digital-transformation/estee-lauder-expands-ai-across-beauty-business/)
- [Business Wire 发布稿（转载）](https://www.bastillepost.com/global/article/6309060-the-estee-lauder-companies-and-microsoft-announce-a-new-strategic-partnership-to-power-enterprise-efficiency-and-consumer-centric-growth)

### 3. Google Cloud 发布说明：Knowledge Catalog 可发现更多视图类资产（10/30）
Google Cloud 10 月 30 日的发布说明记载：用户现可使用 Knowledge Catalog 发现授权视图（authorized views）、逻辑视图与连续物化视图，并与 Bigtable 实例和表等细粒度数据资产一同检索，该集成为正式可用（GA）。
- [Google Cloud 发布说明](https://docs.cloud.google.com/release-notes)

### 4. Databricks 10 月 30 日产品更新：Unity Gateway Skills 审计与指标视图关系（10/30）
Databricks 10 月产品发布说明中，10 月 30 日条目包括：Unity Gateway Skills（Beta）的使用现可追踪，审计日志记录技能的列出、加载与文件获取事件（服务名 aiGatewaySkills），用量看板的 Skills 标签页按用户展示下载与加载活动；Unity Catalog 指标视图之间可通过 ALTER VIEW ... ADD CONSTRAINT ... RELATIONSHIP 记录连接关系（Beta），供 AI 助手与 BI 工具选择连接路径；Lakeflow Connect 新增 Microsoft Graph Logs 托管连接器（Beta），可接入 Microsoft Defender XDR、Sentinel 等安全产品的日志。
- [Databricks on AWS 2026 年 10 月发布说明](https://docs.databricks.com/aws/en/release-notes/product/2026/october)

## 新闻网站

### 5. Databricks 与 SAP 扩展合作，Genie 等四项能力将进入 SAP Databricks（10/30）
多家科技媒体 10 月 30 日报道，Databricks 与 SAP 在柏林 SAP TechEd 上宣布扩展合作（SAP 方面已于 10 月 29 日由其数据与分析总裁 Irfan Khan 发文介绍）：Genie、Lakeflow、Unity Gateway 与 Lakebase 将进入 SAP Business Data Cloud 内的 SAP Databricks；新推出 SAP Application Data Foundation，用于简化对云端与本地 SAP 应用数据的访问，并可通过 SAP BDC Connect 零拷贝使用。同时计划打通 Genie 与 SAP Joule 的双向集成，把 Genie 的回答与操作带入 SAP 界面。两家均未给出上述能力的上线日期。
- [Unite.AI 报道](https://www.unite.ai/databricks-expands-sap-partnership-with-genie-lakeflow-and-lakebase/)
- [Superpower Daily 报道](https://superpowerdaily.com/posts/sap-and-databricks-extend-partnership-to-bring-more-ai-tools-to-business-data)
- [Techseen 报道](https://techseen.com/story/databricks-and-sap-unleash-end-to-end-data-ai-capabilities-to-level-up-d90c79f)

## 社交媒体

### 6. Databricks 在 X 发帖介绍与 SAP 的扩展合作（10/30）
Databricks 官方 X 账号发帖称：「我们很高兴本周在 #SAPTechEd 上扩展与 @SAP 的合作！AI 需要业务上下文，而大量上下文就存在于 SAP 系统中。新的 SAP Application Data Foundation 简化了在 SAP Databricks 中对云端与本地应用数据的访问，减少定制工作……」（Techseen 的报道转引了该帖）。
- [Techseen 报道（含该帖转引）](https://techseen.com/story/databricks-and-sap-unleash-end-to-end-data-ai-capabilities-to-level-up-d90c79f)

说明：本次检索未在 Instagram、Facebook、LinkedIn、Reddit 上找到可核实的 2026-10-30 当天 Data Agent 新帖，上述 X 发帖为当天能核实到的主要社交动态。

## 今日回顾

ZoomInfo 的 MCP 与 API 于 10 月 30 日上线 Snowflake，上下文图谱数据可经 OAuth 权限控制供 Cortex Agents 调用；Databricks 与 SAP 同日宣布扩展合作，四项能力将进入 SAP Databricks；雅诗兰黛与微软宣布多年合作并把 Copilot 扩至 14,000 多名员工；Google Cloud 与 Databricks 各自在当天的发布说明中更新了 Knowledge Catalog 资产发现与 Unity Gateway Skills 审计等功能。
