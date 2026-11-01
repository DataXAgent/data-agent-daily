---
layout: post
title: "Data Agent Daily — 2026-11-01"
author: dad
date: 2026-11-01
image: "assets/images/covers/2026-11-01.svg"
description: "今日速览：Databricks 与 SAP 扩大合作，把 Genie、Lakeflow、Unity Gateway 与 Lakebase 带入 SAP Databricks，并推出 SAP Application Data Foundation；Google 知识目录的扩展语义模型支持进入 GA；SAP 在 TechEd 推出 Joule Studio 与网关能力；Articul8 发布企业 agent 决策模型 Bivia；a16z 文章披露 Databricks 平台上 agent 查询量已超过人类。"
categories: ["Data Agent Daily"]
tags: ["data-agent", "news"]
comments: false
---

## 今日速览

- Databricks 与 SAP 扩大合作，把 Genie、Lakeflow、Unity Gateway 与 Lakebase 带入 SAP Business Data Cloud 内的 SAP Databricks，并推出 SAP Application Data Foundation。
- Google 宣布 Knowledge Catalog 的扩展语义模型支持进入 GA，覆盖 Looker LookML、BigQuery Graph、dbt MetricFlow、Snowflake Semantic Views、Databricks Metric Views 与 SAP CSN。
- SAP 在 TechEd 推出 Joule Studio 与 Joule Work 的分阶段 GA，以及 agent 网关能力；完整企业级网关的 GA 时间在独立报道中为 2027 年第一季度。
- Articul8 发布多模态决策模型 Bivia，通过 API 供企业 agent 调用，覆盖 Choice、Boolean、Score、Set、Span 五种决策原语。
- a16z 文章披露：Databricks 平台上 agent 发起的查询已超过人类，agent 每天启动数据库超过 1,700 万个，Lakebase 年化收入已过 1 亿美元。
- 社区实战：Medium 连载用 Snowflake 托管 MCP 服务器 + Cortex Agent 复现咖啡连锁门店收入下滑 36% 的归因，脚本已在真实账号上跑通。

## 公司发布 / 官方博客

### 1. Databricks 与 SAP 扩大合作：Genie、Lakeflow、Unity Gateway、Lakebase 进入 SAP Databricks（10/30）
Databricks 在 10 月 30 日宣布扩大与 SAP 的合作，把 Genie、Lakeflow、Unity Gateway 与 Lakebase 带入 SAP Business Data Cloud 内的 SAP Databricks，同时推出新的 SAP Application Data Foundation，用于访问 SAP 应用数据。Databricks 的说法是：业务上下文大多存在于 SAP 系统中（其称 90% 以上的财富 500 强使用 SAP 方案），而过去访问 SAP 应用数据往往意味着自建抽取管道、复制数据并丢失业务语义；新基金会改走 SAP BDC Connect 的零拷贝共享，数据工程师可直接在 SAP 的语义基础上建模。Genie 被描述为带企业上下文的 AI 助手，计划与 SAP 的 Joule 做双向连接；Lakeflow 负责 SAP 数据与 IoT、CRM 等来源的摄取与编排；Unity Gateway 提供跨 agent、工具、模型与 MCP 的治理与成本控制；Lakebase 则是面向 AI 应用与 agent 的 serverless Postgres。SAP 在 10 月 29 日 TechEd 期间也发布了自己的版本，口径基本一致，另提到 Agent Bricks。已上线的客户案例包括 SAF-Holland：其用 SAP Databricks 统一了 1 亿多条客户、交付与物料记录，Databricks 称其分析速度比传统报表快 5 倍。注意口径：扩展能力多为“计划带入”，Databricks 指引客户向 SAP 或 Databricks 客户团队咨询新基金会与扩展能力的可用情况，未给出统一的上线日期。
- [Unite.AI 报道](https://www.unite.ai/databricks-expands-sap-partnership-with-genie-lakeflow-and-lakebase/)
- [Superpower Daily 报道（10/30，含“未给发布日期”的提醒）](https://superpowerdaily.com/posts/sap-and-databricks-extend-partnership-to-bring-more-ai-tools-to-business-data)

### 2. Google：Knowledge Catalog 扩展语义模型支持 GA，agent 可直接读业务指标定义（10/30）
Google 在 10 月 30 日宣布 Knowledge Catalog 的扩展语义模型支持进入 GA：目录除原有技术元数据外，现可摄入 Looker LookML、BigQuery Graph、dbt MetricFlow、Snowflake Semantic Views、Databricks Metric Views 与 SAP CSN 的业务定义，并连成上下文图谱。Google 官方博客同步说明了其中最关键的一块：LookML 语义索引 GA 后，模型、Explore、视图、字段、看板与 lineage 自动同步进 Knowledge Catalog，Gemini Enterprise 与自定义 agent 无需另写代码即可调用；同步默认常开，生产 LookML 的更新接近实时反映。Google 举的例子是净收入这类指标：没有语义层时 agent 会自行拼 SQL 公式、漏掉 order_status = 'Complete' 之类的口径条件，还可能因多粒度 join 导致行数膨胀；有了索引后，agent 查到指标的同时就拿到它的精确定义、join 路径与 lineage。冲突处理上也有明确做法：同一指标在不同系统定义不一致时，目录同时展示两份定义与来源，由数据负责人裁决，而非静默取其一。
- [Google Cloud 官方博客：LookML 索引 GA](https://cloud.google.com/blog/products/business-intelligence/lookml-metadata-indexing-in-knowledge-catalog-is-now-ga)
- [Medium 综述：10 月 24–30 日平台动态中的 Google 部分](https://medium.com/@chameleon13/data-platforms-are-becoming-smarter-and-more-connected-but-are-they-making-business-simpler-a8183a145ca9)

### 3. SAP TechEd：Joule Studio 与 Joule Work 分阶段 GA，agent 网关分两层上线（10/27–10/30）
SAP 在 10 月 27 日柏林 TechEd 上推出一揽子企业 AI 能力：Joule Work 与 Joule Studio 开始分阶段 GA，Joule Studio 支持无代码与专业代码两种开发方式、可调用 70 多个 AI 模型，并新增 Process Consulting Agent，用表格模型 SAP-RPT-1 读取客户已有流程数据、自动给出 agent 配置建议——SAP 开发者 keynote 的说法是把约 80% 的手工配置工作压缩，典型搭建时间从 13 小时降到 2.5 小时（公司口径）。网关部分要分清两层：已有的 Agent Gateway 的入站 Agent2Agent 互通在 10 月 GA，第三方 agent 可经此调用 SAP agent；而新宣布的 SAP Enterprise AI Gateway（集中认证、策略、路由、用量与审计）按独立报道与德国 SAP 用户组 DSAG 的说法要到 2027 年第一季度才 GA，TechTimes 则称其在 2026 年第四季度 GA——两份独立报道的时间口径不一致，以 SAP 官方创新指南的分阶段表述为准更稳妥。此外，Business Data Cloud Ontology Manager（为 SAP Knowledge Graph 做领域视图）目前为 beta，Joule Studio 直连 Business Data Cloud 数据产品、经 n8n 的工作流编排等能力也排在 2027 年第一季度。
- [Frontier 分析：SAP agent 扩展与网关时间口径辨析](https://www.thisisfrontier.ai/news/sap-s-agent-expansion-moves-the-cio-choice-from-ai-tools-to-control-architecture)
- [ERP Today：TechEd 2026 上线与排期梳理](https://erp.today/sap-teched-2026-whats-rolling-out-and-whats-planned-through-2027/)

### 4. Articul8 发布 Bivia：不为每个判断都调用生成式模型的企业 agent 决策层（10/28）
Articul8 在 10 月 28 日发布多模态决策模型 Bivia，通过 API 提供给企业 agent 使用，定位是决策层而非生成层：agent 在执行任务中反复遇到的判断（选工具、核对事实、确认任务完成、校验文档是否符合 schema、图片是否通过检查）可直接由 Bivia 处理，而不必每次都调用生成式模型。Bivia 覆盖文本、图像、视频、表格与图表，支持 Choice、Boolean、Score、Set、Span 五种决策原语与 Fast、Fast+think、Deep 三档运行模式，并可按企业的行业知识、政策与流程定制。公司称 Bivia 建立在其平台内数十亿次决策之上，内部测试中在特定能源与硬件设计（Verilog）任务上达到 100% 准确率——该数字为公司内部测试口径，未经第三方核验，不宜外推到其他行业。Bivia 可独立以 API 形式使用，也可作为 Articul8 企业 AI 平台的一部分，公司点名的已有客户包括 Hitachi Energy、CTC、AZing 与 Megazone。
- [GlobeNewswire 通稿](https://www.globenewswire.com/news-release/2026/10/28/3390832/0/en/articul8-launches-bivia-to-bring-domain-specific-decision-intelligence-to-enterprise-ai-agents.html)
- [TechGig 报道](https://techgig.com/news/ai/articul8-launches-bivia-for-enterprise-ai-agent-decision-intelligence/135291818)

## 新闻网站

### 5. a16z 文章披露 Databricks 平台数据：agent 查询量已超人类，每天启动数据库超 1,700 万个（10/27）
a16z 在 10 月 27 日发表《Databricks & the Future of the Firm》，首次披露了 Databricks 平台的 agent 用量数字：agent 发起的查询已超过人类，agent 每天启动数据库超过 1,700 万个，而三年前平台上的全部交互都来自人类。文章称 agent 活动 feeding 的产品线是 Lakebase（随 2025 年 5 月约 10 亿美元收购 Neon 而来），其年化收入已过 1 亿美元，约占 Databricks 70 亿美元总年化收入的 1.4%；Lakehouse 仓储线年化收入已过 15 亿美元、年增速超 100%。另据文章引用的 Databricks 自述，基于企业本体做 grounding 后，回答准确率在其自有测试中从约 50% 提升到 84.5%。提醒：a16z 是 Databricks 的早期投资方（领投了 2013 年 A 轮）且作者 Ben Horowitz 担任 Databricks 董事，数字为利益相关方披露，未经审计；Databricks 8 月融资时估值为 1,900 亿美元，年化收入 70 亿美元。
- [The Inference 报道](https://theinference.org/article/agents-launch-17-million-databases-a-day-on-databricks-the-line-they-feed-makes-100-million)

## 社交媒体

### 6. Medium 连载：用 Snowflake 托管 MCP 服务器 + Cortex Agent 做门店归因，脚本真实跑通（10/31–11/1）
Pranav Katyayen 在 Medium 上线的 Snowflake AI 实战连载首集，用一个 SQL 脚本搭起 Snowflake 托管 MCP 服务器，让 Claude 与 Cursor 经 Cortex Agent 查询受治理的数据并做归因：案例是 Snowbrew Coffee 涩谷门店 9 月收入下滑 36%，agent 先从销售数据取数，再读日文客户投诉找原因。作者称全部脚本已在真实 Snowflake 账号上多次端到端跑通，并如实记录了踩坑点：新账号会屏蔽旧版 Cortex 函数、OAuth 拒绝 ACCOUNTADMIN、新建 Streamlit 应用默认的运行时与文档不一致。连载定位是“每个实验都真实跑通”，下一集计划让 agent 在 Snowflake 内写代码、跑代码并部署应用，且每次改动前都会征求许可。
- [Medium 首集](https://medium.com/@katyayen.pranav/i-asked-claude-why-our-coffee-sales-crashed-it-answered-from-snowflake-with-zero-backend-code-d5ab12b753ea)
- [Medium 连载总览](https://medium.com/@katyayen.pranav/snowflake-ai-hands-on-a-series-where-every-lab-actually-runs-2998ded73055)

说明：今日检索未见 Microsoft、Snowflake、dbt Labs 官方博客在过去 24 小时内发布新的 Data Agent 专帖；X / Instagram / LinkedIn / Reddit 今日除上述内容外，未见可核实的新热帖。Databricks 10 月 31 日博客《Lakebase branching for CI/CD》为工程实践帖，未列入本期头条序列。

## 今日回顾

Databricks 与 SAP 扩大合作，把 Genie、Lakeflow、Unity Gateway 与 Lakebase 带入 SAP Databricks，并推出 SAP Application Data Foundation；Google 知识目录的扩展语义模型支持进入 GA；SAP 在 TechEd 推出 Joule Studio 与网关能力；Articul8 发布企业 agent 决策模型 Bivia；a16z 文章披露 Databricks 平台上 agent 查询量已超过人类；社区实战连载用 Snowflake 托管 MCP 服务器完成门店归因。
