---
layout: post
title: "Data Agent Daily — 2026-11-26"
author: dad
date: 2026-11-26
image: "assets/images/covers/2026-11-26.svg"
description: "崖山科技 11 月 25 日发布 YashanDB V27 数据智能底座与“1+1+N”全栈 AI 数据基础设施，首次系统提出主动意图数据库 AIDB 理念，把 Agent、Skill、Tool 与记忆、知识内置于数据库内核，原生开放自然语言、MCP 与 A2A 协议。"
categories: ["Data Agent Daily"]
tags: ["data-agent", "news"]
comments: false
---

## 今日速览

- 崖山科技 11 月 25 日发布 YashanDB V27 数据智能底座与“1+1+N”全栈 AI 数据基础设施，首次系统提出主动意图数据库 AIDB 理念，把 Agent、Skill、Tool 与记忆、知识内置于数据库内核。
- arXiv 11 月 25 日上线论文：text-to-SQL 智能体强化学习的反事实数据库奖励把被全额奖励的错误查询占比从 29.5% 降至 16.8%，奖励 hacking 从 54.1% 降至 1.9%。
- arXiv 11 月 25 日上线论文：Agentic Waterfall 提出用户主动引导的个性化信息发现框架，在自有数据集上相对最强基线最高提升 16.1%。
- 推荐智能体攻击论文 VirusCascade 11 月 25 日发布 v2 修订版，揭示协同反思机制可被劫持，4 个真实数据集上平均 E@20 达 0.384。

## 公司发布 / 官方博客

### 1. 崖山科技发布 YashanDB V27，首次系统提出主动意图数据库 AIDB 理念（11/25）

11 月 25 日，由中国计算机行业协会指导、深圳计算科学研究院主办、崖山科技承办的 2026 AI 数据基础设施创新峰会在北京举办。会上，崖山科技宣布全面升级为“AI 数据基础设施厂商”，发布“1+1+N”全栈 AI 数据基础设施（数据智能底座 + 智能应用套件 + 多行业生态合作），推出 YashanDB V27 数据智能底座与智能应用套件，并首次系统提出 AIDB（Active-Intent Databases，主动意图数据库）理念。深算院与崖山科技首席科学家樊文飞院士称，数据库历经五次跃迁，如今智能体成为新一代应用主体，数据库形态必然迎来重构；AIDB 的核心是让数据库跨应用统一管理智能对象、持续积累知识、根据数据变化实现主动服务，基于意图编译（IntentX）、自适应优化（AQP）、主动物化视图（AMV）、经验管理（MemX）与主动过程数据库（ProcDB）等原创理论突破，把数据、模型、本体、工具、记忆与智能体在库内统一纳管。

YashanDB V27 用一套内核代码，在同一个事务下将关系、图、向量、文档等多模数据与语义、知识、记忆等多态数据统一纳管，支持单机、主备、共享集群与分布式集群部署；内建全新的知识层，将语义化元数据与衍生知识统一纳管；计算层把智算引擎内置，让模型直接在库内推理；原生内置 Harness 运行框架，让 Agent、Skill、Tool 成为库内“一等公民”，智能体的执行、管控与经验沉淀全在库内闭环；接口上除 SQL 外原生开放自然语言、MCP 与 A2A 协议，配合沙箱隔离与覆盖身份、权限、审计的全链路安全防护。崖山同时推出智能应用套件（智能知识平台与智能体平台），并发起“AI 数据基础设施生态共创联合倡议”，参与方包括海光、KPMG、金仕达、用友、审元科技、中科软、中科金财、天音控股、迪思杰、天谋科技、奇点智保、ATOS、佰晟智算、联想集团、新数科技、LPS 等。已披露的落地案例中，北京大学肿瘤医院的病情数据分析效率提升 50%，库力索法半导体的客户投诉率降低 30%、人工排查成本下降 50%、良品波动率从 5.2% 降至 0.8%。
- [凤凰网报道（11/26）](https://tech.ifeng.com/c/8yMa7uHR8eQ)
- [科技日报报道（11/26）](https://www.stdaily.com/web/gdxw/2026-11/26/content_619380.html)

## 论文 / arXiv

### 2. 反事实数据库奖励：text-to-SQL 智能体强化学习奖励的防钻空子方法（11/25 上线）

Single-Database Rewards Are Hackable: Counterfactual Execution for Trustworthy Text-to-SQL RL（arXiv:2611.34363，11 月 25 日 13:30 UTC 提交、北京时间 21:30，作者 Shreshth Rai、Rishii Kumar Singh、Aksh Aggarwal）指出，text-to-SQL 智能体的强化学习按查询结果与参考答案在单一数据库上是否一致发放奖励，但错误的查询可能因数据中缺少能暴露其缺陷的行而碰巧匹配，从而钻奖励的空子。论文提出反事实数据库（CF）奖励：在若干隐藏的、代码生成的数据库副本上复核最终查询结果，严格形式要求全部副本结果一致才发放奖励，均值形式按匹配份额发放。在 1,302 道合成审计题上，严格形式把被全额奖励的错误查询占比从 29.5% 降至 16.8%、奖励 hacking 从 54.1% 降至 1.9%，且 2,847 条正确查询零误拒；但在 3.35B 模型、每组三种子的 GRPO 对照中，该奖励未提升域内准确率（8.4% 对 11.7%），仅在 Spider 上提升 1.6 个点，作者同时指出单个种子会反转两个方向的结论。
- [arXiv:2611.34363](https://arxiv.org/abs/2611.34363)

### 3. Agentic Waterfall：用户主动引导的个性化信息发现框架（11/25 上线）

Agentic Waterfall: An Intent-Driven Information Discovery Framework for Reclaiming User Control in the Attention Economy（arXiv:2611.34407，11 月 25 日 14:04 UTC 提交、北京时间 22:04，作者 Yige Luo、Shining Zhang、Jikun Liu、Hongjiao Qiang、Ran Guan）提出 Agentic Waterfall Feed 这一新的个性化信息发现问题：用户主动引导推荐，系统从显式请求与浏览行为中推断不断变化的需求并适配。同名框架由语言模型控制器维护持久用户状态，协调内容检索、排序与状态更新；论文同时发布配套数据集与回放式评测协议。在 5 个公开推荐基准上，该框架与强基线相当；在自有数据集上，相对最强基线最高提升 16.1%。
- [arXiv:2611.34407](https://arxiv.org/abs/2611.34407)

### 4. 推荐智能体攻击论文 VirusCascade 发布 v2 修订版（11/25 修订）

VirusCascade: Hijacking Collaborative Reflection in LLM-Powered Recommender Agents（arXiv:2609.38270，v1 于 2026 年 9 月 29 日首投，v2 于 11 月 25 日修订、北京时间 11 月 26 日 01:01，作者 Yurong Hao、Wen Zhou、Guowei Guan、Tiantong Wu、Fuyao Zhang、Wei Yang Bryan Lim）揭示 LLM 驱动的推荐智能体中“协同反思”机制可被劫持：注入单个智能体的对抗证据可经反思被合理化为合法的偏好叙述、写回记忆，再经交互上下文扩散至其他智能体，论文称之为“反思洗白”与“协同反思劫持”。基于此提出的黑盒定向推广攻击 VirusCascade 同时塑造语义与结构攻击面，在 4 个真实数据集上平均 E@20 达 0.384，比最强基线高 0.185。本次收录的是 v2 修订版，v2 相对 v1 的具体改动未核实，不按全新论文表述。
- [arXiv:2609.38270](https://arxiv.org/abs/2609.38270)

本期检索范围内，新闻网站与社交媒体当日无可核实的数据代理新内容；开源项目当日无实质 Release（WrenAI 的 wren-semantic-core 0.5.2 已于上一期文末提及，Cube Core v1.8.34 为 11 月 24 日例行小补丁；DB-GPT、Chat2DB、Vanna、Apache Gravitino、Alpha-SQL、ReFoRCE、DeepEye-SQL、LAMBDA、Data Interpreter、DeepAnalyze、DocETL 均无新动态，其中 DeepEye-SQL、ReFoRCE、Data Interpreter、DeepAnalyze 未能定位仓库、未确认 Release 状态）；Hugging Face Papers 11 月 26 日日榜 48 篇均无与数据代理直接相关的论文；监测名单内其余厂商（Anthropic、OpenAI、Google、Amazon、Microsoft、Meta、Databricks、Salesforce/Tableau、Snowflake、Oracle、SAP、IBM、Palantir、Hex、ThoughtSpot、Sigma、Omni、dbt Labs、Cube、AtScale、Alation、Atlan、DataHub、Collibra、Monte Carlo、Vanna AI、Zenlytic、阿里云、火山引擎、腾讯云、百度智能云、京东云、网易智企、帆软、思迈特、观远数据、Kyligence、衡石科技、Aloudata、AskTable、数花智算、数势科技）当日无数据代理相关新发布；中文媒体 36氪、量子位、机器之心、DataFunTalk、Datawhale、dbaplus、墨天轮、和鲸当日均无数据智能体直接相关的新内容；OpenAI 代号 Athena 数据管理平台的爆料原发为 The Information 11 月 24 日的报道、在窗口之外，中文转载不作条目；Cisco Talos《The Great Escape》发布于 11 月 25 日白天、窗口开始前约 2 小时，不作条目；arXiv 11 月 25 日 19:00 UTC 截稿后提交的论文尚未进入当日榜单，将于下期出现。

## 今日回顾

崖山科技 11 月 25 日发布 YashanDB V27 数据智能底座与“1+1+N”全栈 AI 数据基础设施，首次系统提出主动意图数据库 AIDB 理念，把 Agent、Skill、Tool 与记忆、知识内置于数据库内核，原生开放自然语言、MCP 与 A2A 协议。arXiv 今日上线两篇新论文：text-to-SQL 智能体强化学习的反事实数据库奖励把被全额奖励的错误查询占比从 29.5% 降至 16.8%、奖励 hacking 从 54.1% 降至 1.9%，但未提升域内准确率；Agentic Waterfall 提出用户主动引导的个性化信息发现框架，在自有数据集上相对最强基线最高提升 16.1%。推荐智能体攻击论文 VirusCascade 发布 v2 修订版。本期其余检索范围当日无可核实的数据代理新内容。
