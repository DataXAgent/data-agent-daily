---
layout: post
title: "Data Agent Daily — 2026-11-05"
author: dad
date: 2026-11-05
image: "assets/images/covers/2026-11-05.svg"
description: "Google 在 11 月 4 日更新 Agentic Data Cloud：跨云互联与缓存正式可用，Knowledge Catalog 从 11 月 4 日起默认接入 Gemini 应用，AlloyDB 可直接查询 Iceberg 表。"
categories: ["Data Agent Daily"]
tags: ["data-agent", "news"]
comments: false
---

## 今日速览

- Google 在 11 月 4 日更新 Agentic Data Cloud，跨云互联与缓存正式可用，Knowledge Catalog 从 11 月 4 日起默认接入 Gemini 应用，AlloyDB 可直接查询 Iceberg 表。
- Redis 在 11 月 5 日扩展实时上下文引擎 Iris，新增六项能力，其中 Agent Memory、Intent Router、Agent Playbooks 与 Context Gateway 进入正式可用。
- Dataiku 在 11 月 4 日发布 Headless，把自然语言 agentic 界面 Cobuild 带进 Claude Code、Codex 等编码工具，兼容 Cursor、Snowflake CoCo、GitHub Copilot 与 AWS Kiro。
- Adobe 在 11 月 4 日把 CX Enterprise Coworker 接入 ChatGPT、Claude、Databricks Genie、Gemini 与 Microsoft Copilot，并新增 Databricks Genie 与 Snowflake Cortex AI 等 MCP 连接器。
- Salesforce 在 11 月 4 日宣布 Agentforce Coworker 已有超过 185,000 名用户，三个月内用量增长 21 倍，并新增每用户每月 50 美元的订阅选项。
- Kimi 在 11 月 5 日发布 Kimi Hosted Agents，把 Harness 作为云端服务提供，首批提供 140 多个 Skills、30 多个插件与 8 个金融 Agent 模板。
- GlobalGPT 在 11 月 5 日发布 Yukie for Business 1.0，把业务数据接入 agent，监测数据变化并产出看板、网站、表单与客服机器人。
- ThoughtSpot 11 月版本说明列出新版 Spotter 体验、SpotterViz 文件上传与 Spotter 3 排程进入正式可用。
- Ocient 在 11 月 5 日宣布完成 1 亿美元 C 轮融资，累计融资 2.6 亿美元，用于扩展面向 agent 的 OcientAIQ 解决方案。
- Capgemini 在 11 月 5 日发布《World Cloud Report for Financial Services 2027》，受访金融机构中 59% 正在试点或部署多 agent AI，10% 已实现企业级编排。
- 微软在 11 月 4 日给 Clarity 增加 Agentic Analytics，可查看 AI agent 在网站上的活动并测试其能否完成结账等任务。
- Dialpad 与 Ada 在 11 月 5 日宣布合并，组建统一的 AI 操作系统，融合语音分析与多语言 agent，交易预计 11 月 12 日左右完成。
- ZS 在 11 月 4 日宣布扩展 ZAIDYN 的 agentic AI 能力，覆盖商业、个性化、医学与患者工作流。
- Lovable 的内部数据 agent Lovsight 在 11 月 5 日的报道中披露，9 月完成 167,000 项任务，每天约 500M 事件流入 BigQuery。
- arXiv 11 月 3 日首投的论文评估 agentic AI 完成端到端数据科学项目的能力，七个模型三轮反馈后平均分从 59% 升至 76%。

## 公司发布 / 官方博客

### 1. Google 更新 Agentic Data Cloud：跨云 Lakehouse 与 Knowledge Catalog 进入 agent 工作流（11/04）
Google 在 11 月 4 日发布 Agentic Data Cloud 的一批更新，核心是让 agent 直接使用跨云数据与业务上下文。Borderless Lakehouse 方面，面向 AWS 与 Azure 的跨云互联与缓存进入正式可用，可跨云查询数据且不产生可变出口费用；Gemini 现在可直接在 Borderless Lakehouse 上用自然语言查询跨云记录；Lakehouse 与 Knowledge Catalog 直接集成，自动索引云存储中的分布式与非结构化数据。AlloyDB 新增与 Borderless Lakehouse 的集成，可用标准 PostgreSQL 查询直接查询云存储中的 Iceberg 表，无需 ETL 搬运，并可在一条查询中连接实时运营数据与历史湖仓数据，按 Google 的说法，AlloyDB 直接访问 Iceberg 的聚合查询速度比亚马逊同类 PostgreSQL 兼容服务快至多 7 倍；Spanner Omni 进入正式可用，把多模型能力带到本地、边缘与多云环境。Knowledge Catalog 方面，自学习 enrichment 进入预览，扫描 Google Workspace、Jira、SharePoint 与 GitHub 中的非结构化数据，把运营知识转成 Open Knowledge Format 上下文集，另有 Knowledge Studio 进入预览，供团队检查与批准建议的上下文更新；Knowledge Catalog 从 11 月 4 日起在 Gemini 应用中默认启用，在把用户请求转成 SQL 之前先解析业务指标定义与访问控制。同批内容还包括 Data Agent Kit 进入正式可用、AlloyDB Express 扩大预览、AlloyDB 内面向 agent 的 PostgreSQL（按 Google 的说法可处理每秒 300 万次查询），以及 TimesFM 3.0 预测模型与 TabFM 预测分析模型进入预览。Google 在博客中引用客户 Delivery Hero 旗下 talabat 的说法，称通过跨云 Lakehouse 联邦单份 Iceberg 数据，数据移动成本降低约 40%。
- [SiliconANGLE 报道（11/04）](https://siliconangle.com/2026/11/04/google-fine-tunes-its-agentic-data-cloud-to-support-highly-scalable-autonomous-ai-workers/)
- [TechTarget 报道（11/04）](https://www.techtarget.com/news/google-targets-agentic-ai-accuracy-with-latest-flurry-of-features/873687/)
- [Google 官方博客转载（11/04）](https://gixtools.net/2026/11/new-capabilities-to-power-agents-at-scale-with-googles-agentic-data-cloud/)

### 2. Redis 扩展 Iris：六项 agent 记忆、上下文与消息能力，四项进入正式可用（11/05）
Redis 在 11 月 5 日宣布实时上下文引擎 Redis Iris 的下一阶段，新增六项可组合使用的能力：Intent Router、Agent Playbooks、Agent Memory、Context Gateway、Redis Lens 与 Agent Mesh。其中 Intent Router、Agent Playbooks、Agent Memory 与 Context Gateway 进入正式可用，Lens 与 Agent Mesh 处于 beta。按通稿口径，Agent Memory 通过 MemoryETL 从用户操作、文档与其他半结构化数据中构建记忆，以层级结构组织以便精细控制，并提供检查、审计与来源追溯；Context Gateway 与 Lens、Agent Mesh 分别覆盖 agent 的上下文接入、观测与 agent 间消息。Redis 称 Iris 自 2026 年 5 月首次发布以来已有客户在生产中使用，Iris 从即日起可用；Redis 将在 11 月 12 日（美洲）与 11 月 17 日（欧洲、中东与非洲）做面向工程师的直播演示。
- [Tribune India 转载 PRNewswire 通稿（11/05）](https://www.tribuneindia.com/news/business/redis-expands-redis-iris-to-give-ai-agents-the-memory-context-and-messaging-they-need-to-get-to-production/)
- [Lokmat Times 报道（11/05）](https://www.lokmattimes.com/business/redis-enhances-iris-for-ai-agents-better-memory-context-and-communication-for-real-world-use-a001-w01/)

### 3. Dataiku 发布 Headless：Cobuild 进入 Claude Code 与 Codex 等编码工具（11/04）
Dataiku 在年度 Succeed 大会上发布 Dataiku Headless，把自然语言 agentic 界面 Cobuild 带进技术团队日常使用的编码工具。Headless 是编码 agent 检查与操作 Dataiku 的控制面，在需要创建或修改项目时调用 Cobuild，用自然语言创建与修改数据管道、模型、看板与 agent。Headless 以插件形式上架 Claude Code 与 Codex 市场，兼容 Cursor、Snowflake CoCo、GitHub Copilot、AWS Kiro 与其他 agentic 编码工具。按通稿口径，开发者可在编码 agent 中让 Cobuild 把 Excel 工作簿或 Alteryx 工作流重建为可检查的、受治理的 Dataiku 可视化项目。
- [Dataiku 官方博客](https://www.dataiku.com/blog/dataiku-headless)
- [Saudi Tech Post 报道（11/05）](https://sauditechpost.com/2026/11/05/dataiku-introduces-headless-to-bring-governed-data-and-ai-work-to-agentic-coding-tools/)

### 4. Adobe 把 CX Enterprise Coworker 接入 ChatGPT、Claude、Databricks Genie、Gemini 与 Copilot（11/04）
Adobe 在 11 月 4 日宣布，CX Enterprise Coworker 现已接入 ChatGPT（插件形式）、Claude、Databricks Genie、Gemini for business 与 Microsoft Copilot，Amazon Quick、IBM 与 Snowflake 的接入随后推出。该产品是 Adobe 面向客户体验编排的 agentic 队友。同批内容包括新的 MCP 连接器，提供与 Amazon Ads、Databricks Genie、Demandbase、Meta 广告、Microsoft Work IQ、RainFocus 与 Snowflake Cortex AI 等生态伙伴的预建集成。Adobe 同时称 WPP、Omnicom 与 Publicis 等代理集团支持该产品。
- [The Agile Brand Guide 报道（11/05）](https://agilebrandguide.com/adobe-integrates-agentic-cx-enterprise-coworker-into-ai-platforms-from-anthropic-google-microsoft-openai-and-more/)
- [B&T 报道（11/04）](https://www.bandt.com.au/adobe-takes-agentic-ai-into-chatgpt-claude-gemini-with-major-agency-backing/)

### 5. Salesforce：Agentforce Coworker 超过 185,000 名用户，新增每用户每月 50 美元选项（11/04）
Salesforce 在 11 月 4 日宣布，Agentforce Coworker 已有超过 185,000 名用户使用，三个月内用量增长 21 倍，上述数字为 Salesforce 自报口径。本次扩展新增每用户每月 50 美元的订阅选项、可复用的 Skills 与 Conversation History（均已可用），以及与 Google Workspace 和 Microsoft 365 的连接；Microsoft Teams 支持与 iOS、Mac、Windows 应用计划于本月内正式可用，定时任务与 Daily Digest 预计 12 月推出。Salesforce 列出 Adecco Group、Fulton Bank 与 BACA Systems 为扩大采用的客户，并称 Coworker 基于 Salesforce 记录、业务元数据与通过 Data 360 连接的数据提供受信上下文。
- [The Agent Times 报道（11/04）](https://theagenttimes.com/articles/salesforce-says-agentforce-coworker-surpassed-185-000-users--6bfc5c91)
- [Technobezz 报道（11/04）](https://www.technobezz.com/news/salesforce-agentforce-coworker-adds-monthly-user-option)

### 6. Kimi 发布 Kimi Hosted Agents：Harness 作为云端服务，首批 8 个金融 Agent 模板（11/05）
Kimi 在 11 月 5 日宣布推出 Kimi Hosted Agents（托管智能体），把支撑 Agent 运行的 Harness 作为云端服务提供。首批提供 140 多个 Skills 与 30 多个插件，覆盖联网检索、专业数据查询、办公文档处理与内容生成等任务，开发者可按需调用，企业也可接入自有工具与数据源。安全方面，Kimi Hosted Agents 可结合开放平台的独立安全组件 Kimi Inference Hook，在每次模型推理前检查任务输入与工具返回内容。首批提供 8 个金融 Agent 模板，覆盖投研建模、深度研究、晨报生成、IPO 跟踪、持仓监控等任务，支持在托管环境中持续运行。定价方面，总费用为沙箱运行时长（小时）× 0.072 元/小时 + 模型推理费用 + 插件调用次数 × 插件单价。
- [新浪科技转载 IT 之家报道（11/05）](https://finance.sina.com.cn/tech/digi/2026-11-05/doc-inixrytw8950784.shtml)

### 7. GlobalGPT 发布 Yukie for Business 1.0：连接业务数据并监测变化的 agent（11/05）
GlobalGPT 在 11 月 5 日发布 Yukie for Business 1.0，定位为面向小企业主、独立经营者与专业团队的业务 AI agent。按通稿口径，该 agent 连接企业数据、监测数据变化，并把日常工作推进为成品结果，包括跟进看板、网站、表单与客服聊天机器人；邮件、会议记录与团队消息用于提示待办事项。Yukie for Business 即日起在 glbgpt.com 提供。GlobalGPT 称其平台累计用户超过 400 万。
- [Economy Lane 报道（11/05）](https://www.economylane.com/2026/11/05/globalgpt-launches-yukie-for-business-1-0-an-ai-agent-that-monitors-data-and-builds-tools/)

### 8. ThoughtSpot 11 月版本：新版 Spotter 体验、SpotterViz 文件上传与 Spotter 3 排程进入正式可用（11 月）
ThoughtSpot 11 月版本说明（Cloud 26.11.0.cl）列出三项进入正式可用的内容：新版 Spotter 体验，包括 Liveboards 上的 Spotter；SpotterViz 文件上传，可上传 Tableau 工作簿（.twb、.twbx）或图片、PDF 等文件并指示 agent 据此创建 Liveboard；Spotter 3 排程。另有模型保存时自动生成 AI Context 进入早期体验。本期按 11 月版本说明记录，不把四 agent 套件（SpotterViz、SpotterModel、SpotterCode、Spotter 3）重复计为新发布——该套件的发布日期为 2025 年 12 月 10 日。
- [ThoughtSpot 开发者版本说明（11 月）](https://developers.thoughtspot.com/docs/whats-new)

## 新闻网站

### 9. Ocient 完成 1 亿美元 C 轮融资，扩展面向 agent 的分析业务（11/05）
Ocient 在 11 月 5 日宣布完成 1 亿美元 C 轮融资，用于扩展其 agentic AI 分析业务，本轮之后累计融资达到 2.6 亿美元。按公司口径，本财年（截至明年 1 月）收入预计增长两倍以上，上一年收入翻倍；新资金将加速交付 OcientAIQ 解决方案，让 AI agent 与人类分析师查询 PB 级数据集。Ocient 称需求来自国家安全机构与电信运营商等客户，这些客户需要在不抽样的情况下分析海量数据集，越来越多由软件 agent 而非人类分析师查询其系统。OcientAIQ 统一数据平台组合数据接入、分析、治理与 agent 编排。
- [SiliconANGLE 报道（11/05）](https://siliconangle.com/2026/11/05/ocient-raises-100-million-as-agentic-ai-drives-growth-in-large-scale-analytics/)

### 10. Capgemini 报告：59% 的金融机构正在试点或部署多 agent AI，10% 实现企业级编排（11/05）
Capgemini 研究院在 11 月 5 日发布《World Cloud Report for Financial Services 2027》，称金融机构正从孤立的 agentic AI 实验走向跨核心银行与保险工作流的多 agent AI。报告给出的数字为：59% 的企业正在试点或部署多 agent AI 系统，10% 已实现跨企业的企业级编排；90% 的企业正在使用或计划采用智能模型路由以优化性能与 token 成本；52% 的银行与保险公司把 hyperscaler 作为治理多 agent 部署的首选云合作方。报告基于 2026 年 6 月至 7 月进行的全球金融服务高管调查，覆盖 14 个市场的 1,100 名金融服务领导者。
- [Manila Times 转载 GlobeNewswire 通稿（11/05）](https://www.manilatimes.net/2026/11/05/tmt-newswire/globenewswire/financial-institutions-accelerate-transition-to-multi-agent-ai-in-drive-for-bottom-line-value/2462456)

### 11. 微软 Clarity 增加 Agentic Analytics：查看 AI agent 在网站上的活动（11/04）
微软在 11 月 4 日为网站与应用分析工具 Clarity 增加三项功能，其中 Agentic Analytics 让网站所有者查看哪些 AI agent 访问网站、做了什么，并测试 agent 能否完成结账等关键任务。微软称 AI agent 数量在三周内接近翻倍，达到近 200 万。另两项为 Ask Clarity（向 Clarity 提问网站使用情况并获得以真实会话证据支持的答案，目前面向零售商封闭测试）与 Brand Agents 扩展（帮助产品在 Microsoft Copilot、Bing 与 MSN 中被发现，并帮助本地商家获取线索与预约）。
- [PYMNTS 报道（11/04）](https://www.pymnts.com/news/artificial-intelligence/2026/microsoft-clarity-helps-merchants-welcome-ai-shopping-agents/)
- [Search Engine Roundtable 报道（11/04）](https://www.seroundtable.com/microsoft-clarity-gains-agentic-analytics-and-ask-clarity-42449.html)

### 12. Dialpad 与 Ada 合并，组建融合语音分析与多语言 agent 的统一 AI 操作系统（11/05）
Dialpad 与 Ada 在 11 月 5 日宣布合并，组建一家公司，目标是打造融合语音、数据与 AI agent 的统一 agentic 操作系统。按报道口径，Dialpad 自 2018 年以来已分析超过 140 亿分钟的商业通话；Ada 已在生产中部署 500 多个 AI agent，覆盖语音、消息、邮件与社交渠道，支持 130 多种语言。合并后的公司由 Dialpad 联合创始人兼 CEO Craig Walker 担任 CEO，Ada CEO Mike Murchison 担任首席 AI 官；交易预计 11 月 12 日左右完成。
- [openaimpact.com 报道（11/05）](https://openaimpact.com/news/dialpad-ada-agentic-operating-system-customer-work/)

### 13. ZS 扩展 ZAIDYN 的 agentic AI 能力，覆盖生命科学商业、医学与患者工作流（11/04）
ZS 在 11 月 4 日宣布扩展 ZAIDYN 的 agentic AI 能力，新的 agent 覆盖商业、个性化、医学与患者工作流。按通稿口径，agent 感知信号、分析信息、生成洞察、推荐行动，并在既定护栏内自动执行已批准的活动；各应用协同数据、洞察、决策与行动。ZS 称 ZAIDYN 已被 80% 的头部 20 家生命科学公司使用，覆盖 100 多个国家，包含 30 多个模块，上述采用数字为公司自报口径；Everest Group 在 2026 Innovation Watch 中将 ZS 列为 Luminary。
- [WiseVoter 报道（11/04）](https://wisevoter.com/world/2026/11/04/zs-expands-agentic-ai-zaidyn-life-sciences)

### 14. Lovable 内部数据 agent Lovsight：9 月完成 167,000 项任务（11/05 报道）
瑞典科技媒体在 11 月 5 日报道 Lovable 的内部 AI agent Lovsight，该 agent 按既定流程自主开展调研：接收问题、汇总提示、让模型推理、选择工具并检查结果。按报道口径，Lovable 每天约 500M 事件流入 BigQuery，数据环境每天处理约 100,000 次查询，其中大部分来自 agent 与自动化工作流；Lovsight 在 9 月完成 167,000 项任务，调用语言模型超过 200,000 次。Lovable 另有一个内部 agent Company Brain，负责掌握公司的整体上下文与知识。
- [Techtidningen 报道（11/05，瑞典语）](https://techtidningen.se/lovable-ai-agent-gor-en-dags-analysarbete-pa-nagra-minuter/)

## 论文 / arXiv

### 15. arXiv 论文评估 agentic AI 完成端到端数据科学项目的能力：三轮反馈后平均分 59% 升至 76%（11/03 首投）
Rohan Alexander 在 arXiv 上发表论文《Iterated creation, grading, and revision of data science projects by language models》（arXiv:2611.05548，11 月 3 日提交），评估 agentic AI 模型完成端到端数据科学项目的能力及其随反馈的改进。实验中一个带专用工具的 writer 模型完成数据科学项目，包括下载、清洗与分析数据集并撰写短论文；grader 模型评分后 writer 修订，共进行三轮。实验覆盖来自 Anthropic、OpenAI、Google、DeepSeek 与 z.ai 的七个模型，每个模型同时担任 writer 与 grader，共 49 组 writer-grader 配对，每组运行三次。147 份初始提交中 107 份可运行并渲染；三轮反馈后平均分从 59% 升至 76%。按 writer 划分，提升幅度为 Anthropic Opus 5.5 的 3 个百分点至 Anthropic Haiku 4.5 的 46 个百分点；模型给自己的评分平均比其他模型给它的评分高约 9 个百分点；约一半的轮次间差异在 grader 自身噪声范围内。
- [arXiv:2611.05548](https://arxiv.org/abs/2611.05548)

本期检索范围内，除上述论文外，arXiv 与 Hugging Face Papers 未见 11 月 5 日当天首投的、与数据代理直接相关的其他新论文；清华等团队的《Data Agents: Agentic Data Systems》（arXiv:2609.24137）为 9 月首投的论文，本期不重复计为当日新论文。

## 开源项目

本期检索范围内，监测名单内的开源项目在过去 24 小时内未见实质 Release：Wren AI 最新稳定版 v0.17.1 发布于 10 月 30 日；DB-GPT、Vanna 等项目未见当日新版本。

## 社交媒体

本期检索范围内，未见监测名单主体在过去 24 小时内发布新的 Data Agent 专帖；11 月 5 日的社交讨论多为对 Google Agentic Data Cloud 更新、Redis Iris 与 Kimi Hosted Agents 的转述。ClickHouse 10 月 27 日的 Jev 相关帖子为 10 月内容，本期不重复计入。

## 今日回顾

Google 在 11 月 4 日更新 Agentic Data Cloud，跨云互联与缓存正式可用，Knowledge Catalog 从 11 月 4 日起默认接入 Gemini 应用，AlloyDB 可直接查询 Iceberg 表；Redis 在 11 月 5 日扩展 Iris，Agent Memory 等四项能力进入正式可用；Dataiku 在 11 月 4 日发布 Headless，把 Cobuild 带进 Claude Code 与 Codex 等编码工具；Adobe 在 11 月 4 日把 CX Enterprise Coworker 接入 ChatGPT、Claude、Databricks Genie、Gemini 与 Copilot；Salesforce 在 11 月 4 日宣布 Agentforce Coworker 超过 185,000 名用户并新增每用户每月 50 美元选项；Kimi 在 11 月 5 日发布 Kimi Hosted Agents，首批提供 8 个金融 Agent 模板；Ocient 在 11 月 5 日完成 1 亿美元 C 轮融资；Capgemini 在 11 月 5 日的报告中披露 59% 的金融机构正在试点或部署多 agent AI；arXiv 11 月 3 日首投的论文显示 agentic AI 在三轮反馈后把端到端数据科学项目的平均分从 59% 提升至 76%；本期检索范围内未见监测开源项目当日的新 Release，也未见监测名单主体过去 24 小时内的新 Data Agent 专帖。
