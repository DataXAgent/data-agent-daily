---
layout: post
title: "Data Agent Daily — 2026-11-10"
author: dad
date: 2026-11-10
image: "assets/images/covers/2026-11-10.svg"
description: "Zoho 在 11 月 10 日把 Zoho Analytics 升级为 Agentic Analytics 平台，Ask Zia 改为多智能体架构，内置六个数据分析子智能体，并以原生语义层与本体层为智能体提供业务上下文。"
categories: ["Data Agent Daily"]
tags: ["data-agent", "news"]
comments: false
---

## 今日速览

- Zoho 在 11 月 10 日把 Zoho Analytics 升级为 Agentic Analytics 平台，Ask Zia 改为多智能体架构，内置六个数据分析子智能体，并以原生语义层与本体层为智能体提供业务上下文。
- Databricks 在 11 月 10 日宣布未来三年在荷兰投资超 5 亿美元，扩建阿姆斯特丹欧洲最大研发中心，支撑 Lakebase、Genie 与 Unity Gateway 的需求增长。
- Northern Trust 与微软在 11 月 9 日联合部署客户入职 Agent，把多年历史交易数据转为标准报告格式，数据准备时间从约两周半缩至 3 天。
- Meta 在 11 月 9 日发布 Muse 系列最小模型 Ember，专为智能体重复性工作设计，输入与输出定价分别为每百万 tokens 0.10 美元与 0.50 美元。
- Anthropic 在 11 月 9 日发布 Claude Fable 5.2 与 Mythos 5.2，API 定价较 5.1 下调 20%，Fable 5.2 在 FrontierCode 2.0 上得分 49.1%。
- 阿里在 11 月 9 日发布千问办公 2.0，从个人助手升级为面向个人与组织协作的 Team Agent，数字员工“小 Q”可经钉钉派任务做数据分析。
- arXiv 11 月 9 日上线 OGDA：本体驱动的数据代理，用于异构数据湖上的可靠分析，在 KramaBench 与 DiscoveryBench 上较最强基线最高提升 10.82 个百分点。
- arXiv 11 月 9 日上线《面向可验证的数据系统自动研究》，主张以精确可组合的规约锚定自动研究中的搜索，把正确性内建为流程的一部分。
- WrenAI 在 11 月 10 日发布 v0.18.0，通过共享上下文层提供项目绑定的 agent 服务与受治理的 MCP。
- Cube Core 在 11 月 9 日发布 v1.8.21，CubeSQL 的 DataFusion 升级至 Arrow 60；同日发布 v1.4.6 LTS，封堵 api-gateway 成员表达式 SQL 求值的 JS 注入。
- 社交媒体与中文媒体层当日未见可核实的数据智能体新内容。

## 公司发布 / 官方博客

### 1. Zoho 把 Zoho Analytics 升级为 Agentic Analytics 平台：Ask Zia 改为多智能体架构（11/10）
Zoho 在 11 月 10 日宣布把 Zoho Analytics 升级为 Agentic Analytics 平台，以可信智能层把数据、业务上下文、分析与 AI 智能体连接起来。Ask Zia 采用多智能体架构，内置六个子智能体，分别负责数据分析、可视化、数据准备、建模、编码与 SQL 生成，由中央智能体编排，共享同一语义层、本体与对话上下文；用户可自建数据智能体，经 MCP 连接外部工具与系统。平台的语义层与本体层均为原生能力：语义层为 AI 提供业务术语、指标与同义词的标准定义，本体层建模业务实体及其关系；兼容 Apache Ossie 规范，定义可在平台间携带。Headless BI 方面，开发者与智能体可经 Zoho Analytics MCP 服务器（远程与本地两种部署）构建智能体方案，另有命令行工具与 Claude 插件。平台新增 30 多个数据连接器，连接器总数超过 500 个；除智能体功能外还新增 50 多项能力，包括 10 多种可视化、场景分析、相关矩阵、VARX 预测模型与带 Jupyter Notebook 的 Data Science Studio。Zoho Analytics 每日服务 10 万家企业，定价不变，Basic 套餐为每月 24 美元（按年计费）；云端更新即日可用，本体与语义模型的预览版在未来四到八周内全球 rollout，本地部署版将于 2027 年第一季度提供。
- [The Manila Times 转载 Media OutReach Newswire 通稿（11/10）](https://www.manilatimes.net/2026/11/10/tmt-newswire/media-outreach-newswire/zoho-brings-trusted-business-intelligence-to-ai-agents-in-zoho-analytics-platform-evolution-connecting-data-business-context-insights-and-action/2465925)
- [Zoho Analytics 官方更新页](https://www.zoho.com/analytics/whats-new.html)

### 2. Databricks 宣布未来三年在荷兰投资超 5 亿美元，加码数据 Agent 平台（11/10）
Databricks 在 11 月 10 日宣布未来三年在荷兰投资超 5 亿美元，扩建其位于阿姆斯特丹的欧洲最大研发中心，支撑 Lakebase、Genie 与 Unity Gateway 的需求增长，并计划把荷兰本地团队规模翻倍。公司同时启用了位于 The Rock 大厦的 13,000 平米、11 层新办公室，并设定到 2030 年培训超 4 万人掌握数据与 AI 技能的目标。通稿点名阿姆斯特丹团队在研的 Genie ZeroOps：一个监控生产工作负载、定位问题并建议修复的 AI Agent；阿姆斯特丹团队还负责 Databricks Apps 与面向工程师的内部智能体系统。Databricks 称，ABN Amro、AkzoNobel、Heineken、PostNL、Shell 与 UMC Utrecht 等荷兰客户已在用其平台规模化落地数据与 AI；AkzoNobel 首席信息官在通稿中称，公司用 Genie 触发智能体响应，筛选超 1.2 亿个分子寻找水性替代配方。
- [Databricks 官方通稿全文转载（11/10）](https://bitcomme.com/databricks-to-invest-more-than-500m-in-the-netherlands-to-accelerate-enterprise-data-ai/)

### 3. Northern Trust 与微软联合部署客户入职 Agent，数据准备时间缩短 83%（11/09）
Northern Trust 与微软在 11 月 9 日宣布联合开发的客户入职 Agent：把多年历史交易数据转为 Northern Trust 的标准报告格式，数据准备时间从约两周半缩短至 3 天，降幅 83%。在 7 个真实匿名历史交易案例的受控测试中，Agent 的首过质量分为 96.5% F1。微软的报道称，57% 的资产所有者把多源数据整合列为最大挑战；Northern Trust 截至 2026 年 9 月 30 日的托管资产为 19.9 万亿美元、管理资产为 2.0 万亿美元。Agent 基于 Azure 与 Microsoft Foundry 构建，集成 Excel 与 SharePoint，全程保留人工审核。
- [微软官方新闻中心（11/09）](https://news.microsoft.com/source/2026/11/09/northern-trust-and-microsoft-frontier-company-collaborate-to-transform-client-onboarding-through-ai/)

### 4. Meta 发布 Muse Ember：面向 Agent 重复性工作的最小、最便宜模型（11/09）
Meta 在 11 月 9 日发布 Muse 系列最小模型 Ember，专为智能体每天重复的工作设计，包括工具调用、编码子任务、路由、信息抽取与长文档解析。定价为每百万输入 tokens 0.10 美元、每百万输出 tokens 0.50 美元，缓存输入为每百万 tokens 0.004 美元；上下文为 1M tokens，最高输出 512K tokens。Meta 称，Ember 在 Artificial Analysis Intelligence Index 上得分 36，与 Claude Haiku 5.5 持平，单任务成本约 0.14 美元（Haiku 约 0.41 美元）。模型 ID 为 muse-ember-1.0，已上线 Meta Model API 与 Muse Code；首批合作方包括 Box、Cline、Oracle、Cloudflare 与 You.com。
- [Meta 官方博客（11/09）](https://research.meta.ai/blog/muse-ember)

## 新闻网站

### 5. Anthropic 发布 Claude Fable 5.2 与 Mythos 5.2，API 降价 20%（11/09）
Anthropic 在 11 月 9 日发布面向高难度技术任务的新旗舰模型 Fable 5.2（公开版）与 Mythos 5.2（受限版），定价较 5.1 下调 20%，为每百万输入 tokens 8 美元、每百万输出 tokens 40 美元（5.1 为 10 美元与 50 美元）；输出速度较 5.1 最高快 30%。Fable 5.2 在 FrontierCode 2.0 上得分 49.1%，Opus 5.5 为 45.5%；Anthropic 自报的对比表中，Fable 5.2 在 15 项中有 13 项领先。Mythos 5.2 仅限通过验证的网络安全与生命科学机构使用。
- [VentureBeat 报道（11/09）](https://venturebeat.com/technology/anthropic-releases-claude-fable-5-2-and-mythos-5-2-pairing-new-record-high-benchmarks-with-20-api-cost-reduction)

### 6. 阿里发布千问办公 2.0，定位升级为 Team Agent（11/09）
阿里在 11 月 9 日发布千问办公 2.0，从个人助手升级为面向个人与组织协作的 Team Agent，是上线 3 个月以来的最大一次升级。2.0 新增「协作」「人机共创」「资料空间」「自动任务」「三端互联」，推出行业首个支持多人与 Agent 协作的功能：数字员工“小 Q”可通过钉钉直接派任务，负责整理数据、跟进进度、设待办；多个 Agent 可分工协作，一个做 PPT、一个做数据分析、一个写周报。千问办公上线 30 天用户突破 3,000 万。
- [凤凰网科技报道（11/09，据钉钉官方消息）](https://tech.ifeng.com/c/8xukDVObSZt)

## 论文 / arXiv

### 7. OGDA：面向异构数据湖的本体驱动数据代理（arXiv 11/09 上线，11/09 提交）
arXiv 11 月 9 日上线的论文《OGDA: Ontology-Grounded Data Agents for Reliable Analysis over Heterogeneous Data Lakes》（arXiv:2611.12114，11 月 9 日提交）针对真实数据湖上的全流程数据分析：已有数据代理按任务探索会在海量表上耗尽上下文，进而定位错误数据文件并把错误带入最终答案。OGDA 用紧凑本体降低探索开销并约束数据处理，通过提议者—验证者智能体假设检验从原始数据源构建本体，任务执行中所有数据处理动作受任务图约束。实验在 KramaBench 与 DiscoveryBench 上、用 3 个 LLM 主干进行，与最强基线相比最高提升 10.82 个百分点。
- [arXiv:2611.12114](https://arxiv.org/abs/2611.12114)

### 8. 面向可验证的数据系统自动研究（arXiv 11/09 上线，11/09 提交）
arXiv 11 月 9 日上线的论文《Toward Verifiable Auto-Research for Data Systems》（arXiv:2611.12063，11 月 9 日提交）是一篇愿景型论文：AI 自动研究可为特定负载与硬件定制键值存储、索引、查询引擎等数据系统，但智能体只优化可度量的目标，自然语言需求留有规约博弈空间，可能在基准上表现亮眼却静默丢失更新或违反一致性，且一次完整验证可拖长至数周。论文主张以精确可组合的规约锚定搜索、用轻量性能评审剪除死胡同、用证伪与演绎验证把正确性内建为流程的一部分，并把正确性、性能、研究时间与 token 成本作为同等重要的目标。
- [arXiv:2611.12063](https://arxiv.org/abs/2611.12063)

## 开源项目

### 9. WrenAI 发布 v0.18.0：项目绑定的 agent 服务与受治理的 MCP（11/10）
WrenAI 在 11 月 10 日发布 v0.18.0，新增“通过共享上下文层提供项目绑定的 agent 服务与受治理的 MCP”，另含 JSON 同名列保留、Ossie 导入导出物理列重命名保留、CTE 可见性等 5 项修复。
- [WrenAI GitHub Releases（11/10）](https://github.com/Canner/WrenAI/releases/tag/wren-v0.18.0)

### 10. Cube Core 发布 v1.8.21 与 v1.4.6 LTS（11/09）
Cube Core 在 11 月 9 日发布 v1.8.21：CubeSQL 将 DataFusion 升级至 Arrow 60，pyo3 升级至 0.29，并修复 Tesseract 滚动窗口规划问题。同日发布的 v1.4.6 LTS 为安全修复合集：封堵 api-gateway 成员表达式 SQL 求值的 JS 注入、收紧成员表达式校验、转义 SQL 标识符引号，并将 tzdb 更新至 2026e。
- [Cube Core v1.8.21（11/09）](https://github.com/cube-js/cube/releases/tag/v1.8.21)
- [Cube Core v1.4.6 LTS（11/09）](https://github.com/cube-js/cube/releases/tag/v1.4.6)

## 社交媒体

本期检索范围内，社交媒体（X / LinkedIn / Reddit）当日未见与数据代理直接相关的厂商或研究者帖文的可核实原文。

本期检索范围内，中文媒体层当日未见可核实的数据智能体新内容；除上述条目外，监测名单内的其他厂商、研究团队与评测基准机构在过去 24 小时内未见可核实的新动态；监测名单内其余开源项目当日未见实质 Release。

## 今日回顾

Zoho 在 11 月 10 日把 Zoho Analytics 升级为 Agentic Analytics 平台，Ask Zia 改为多智能体架构，内置六个数据分析子智能体，并以原生语义层与本体层为智能体提供业务上下文；Databricks 在 11 月 10 日宣布未来三年在荷兰投资超 5 亿美元，扩建阿姆斯特丹欧洲最大研发中心，支撑 Lakebase、Genie 与 Unity Gateway 的需求增长；Northern Trust 与微软在 11 月 9 日联合部署客户入职 Agent，数据准备时间从约两周半缩至 3 天；Meta 在 11 月 9 日发布 Muse 系列最小模型 Ember，输入与输出定价分别为每百万 tokens 0.10 美元与 0.50 美元；Anthropic 在 11 月 9 日发布 Claude Fable 5.2 与 Mythos 5.2，API 定价较 5.1 下调 20%；阿里在 11 月 9 日发布千问办公 2.0，定位升级为 Team Agent；arXiv 11 月 9 日上线 OGDA 与《面向可验证的数据系统自动研究》两篇论文；WrenAI 在 11 月 10 日发布 v0.18.0，Cube Core 在 11 月 9 日发布 v1.8.21 与 v1.4.6 LTS；社交媒体与中文媒体层当日未见可核实的数据智能体新内容。
