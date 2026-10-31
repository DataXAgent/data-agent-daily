---
layout: post
title: "Data Agent Daily — 2026-10-31"
author: dad
date: 2026-10-31
image: "assets/images/covers/2026-10-31.svg"
description: "本周一句话判断：Data Agent 的竞争点已经从会写 SQL 转到谁有业务上下文——context graph / semantic layer / ontology 本周同时被 Jedify、SAP、Google、Microsoft 押注。"
categories: ["Data Agent Daily"]
tags: ["data-agent", "news"]
comments: false
---


> 本周一句话判断：Data Agent 的竞争点已经从“会写 SQL”转到“谁有业务上下文”——context graph / semantic layer / ontology 本周同时被 Jedify、SAP、Google、Microsoft 押注。

## 公司发布 / 官方博客

### 1. Jedify 发布 Data Agents（10/28）
用自然语言描述就能建一个 autonomous analyst，可按需、定时或条件触发，自动监控指标、调查波动、跑重复分析，结果可推 Slack / 邮件，也可通过 MCP 被 Claude、ChatGPT 调用。核心卖点是 context graph：把指标定义、业务规则、行级权限都建模进去。
- [SiliconANGLE 报道](https://siliconangle.com/2026/10/28/jedify-formally-launches-data-agents-for-building-ai-analysts-in-plain-language/)
- [官方 GlobeNewswire 发布稿](https://www.globenewswire.com/news-release/2026/10/28/3390231/0/en/jedify-launches-data-agents-autonomous-analysts-built-on-its-context-graph.html)

### 2. SAP TechEd 大扩张（10/27）
Joule Studio 支持 no-code + pro-code 建 agent、可选 70+ 模型；Business Data Cloud 新增 Ontology Manager，并深化与 Databricks 的集成（Lakeflow、Agent Bricks、Unity Gateway、Lakebase）；主推 MCP + Agent2Agent 互操作。Enterprise AI Gateway 的 GA 要到 2027 Q1，不要当作已上线。
- [Frontier 分析](https://www.thisisfrontier.ai/news/sap-s-agent-expansion-moves-the-cio-choice-from-ai-tools-to-control-architecture)
- [SAP 官方发布稿转载](https://www.tradingview.com/news/prnewswire:da7283c600ab9:0-sap-empowers-ai-developers-to-build-what-matters-and-turn-intent-into-autonomous-execution/)

### 3. Google Data Agent Kit GA（GA 公告 10/24，本周热议）
免费开源的 MCP 工具集 + 37 个 Apache 2.0 skills，把 15+ Google Data Cloud 服务接到 Claude Code、Codex、Cursor、VS Code、Antigravity。本周讨论焦点是双层护栏：skills 只是“建议”，真正的权限靠 IAM / 只读服务账号强制。
- [GA 深度解读](https://news.lavx.hu/article/google-data-agent-kit-reaches-general-availability-splits-guardrails-between-skills-and-iam)
- [Automater 汇总](https://automater.ai/news/google-data-agent-kit-ga-mcp-tools-data-cloud-coding-agents/)

### 4. Microsoft Fabric：Data Agent 已 GA（社区博客，约 10/27）
Copilot Studio 是对话入口、Foundry 是开发者建 agent、Fabric data agent 是只读分析师（问题转 SQL/DAX/KQL，最多 5 个数据源、按用户权限）、operations agent 盯实时数据主动行动。Data agent 与 Copilot Studio 的集成在 10 月 FabCon 上 GA。
- [Microsoft Fabric Community](https://community.fabric.microsoft.com/blog/fbc_comm_blog/copilot-studio-foundry-fabric-data-agent-or-operations-agent-which-one-to-pick/5377319)

### 5. Databricks Agent Memory（Beta）+ AI Runtime（GA）（10/22，二手报道，待官方核实）
Agent Memory 基于 Lakebase 存可复用的上下文数据集，AI Runtime 提供 serverless GPU、直接跑在受 Unity Catalog 治理的数据上，与 Agent Bricks 打通。
- [Wisevoter](https://wisevoter.com/world/us/2026/10/22/databricks-launches-agent-memory-ai-runtime)

## 新闻网站

### 6. a16z 数据：Databricks 上 agent 查询量已超过人类，每天新建 1700 万个数据库（10/27）
承载它的 Lakebase 已到 $100M 年化收入，但 Databricks 总 run rate 是 $7B，agent 原生产品线还只占约 1.4%——用量爆了，收入还没跟上。注意来源 a16z 是 Databricks 董事/早期投资人，立场不中立。
- [The Inference](https://theinference.org/article/agents-launch-17-million-databases-a-day-on-databricks-the-line-they-feed-makes-100-million)

### 7. Snowflake vs Databricks 新战场：SQL 文档解析
Databricks 在 Agent Bricks 里加了 `ai_parse`；Snowflake 在 Intelligence 平台推 Agentic Document Analytics，一次查上千份文档，做定量/时间维度分析，而不只是 RAG 检索。
- [Databricks fires back at Snowflake](http://en.zicos.com/tech/i32371689-Databricks-fires-back-at-Snowflake-with-SQL-based-AI-document-parsing.html)

### 8. Akeneo 秋季发布（10/28 上线）+ 收购 Dataggo
垂直行业版 data agent：agentic orchestrator Ziggy for Shopify 自动 enrich 上千个商品、接入供应商数据、跨渠道发布，并加了透明 AI 标注（标明哪段是 agent 写的、哪段是人审的）。
- [UK Tech News](https://uktechnews.co.uk/2026/10/30/akeneo-puts-ai-agents-to-work-across-product-data-with-enterprise-control-built-in/)

### 9. 风险面：Agentic AI 安全周报（截至 10/27）
OWASP 更新 Agentic AI Incidents 追踪；FastMCP 爆 OAuth issuer-binding 漏洞（已在 4.1.2 修复），可导致 MCP server 窃取客户端凭据——对所有接 MCP 的 Data Agent 都是直接相关的供应链风险。
- [AI Agent Store 周报](https://aiagentstore.ai/ai-agent-news/topic/data-privacy-security)

## 社交媒体

### 10. Instagram — Google Cloud 官方 Reel（10/30）
讲 Agentic Data Cloud 为什么能破“准确率墙”：Knowledge Catalog（业务定义）、Borderless Lakehouse（零拷贝原地查询）、Smart Storage（把 PDF/图片里的暗数据原地结构化）。
- [Google Cloud Reel](https://www.instagram.com/reel/DfIGKzViEpD/)

### 11. Instagram — Zoho（10/28）
预告 “Meet the next evolution of Zoho Analytics, built for the Agentic era”，中小厂 BI 也在全面 agentic 化。
- [Zoho 帖子](https://www.instagram.com/p/DfCXVSoSXiv/)

### 12. Threads — 数据分析师视角热帖（10/24，约 3K 赞）
资深数据分析师 Stanley Wang 建议同行现在就学 Claude Code / Codex，先从“用 agent 做一个 dashboard”开始；评论区在成功案例与公司禁用、核验成本之间分化。
- [Threads 原帖](https://www.threads.com/@stanleywangg/post/De5GiOniqQI)

### 13. Facebook — Agentic AI 学习笔记帖（10/29，480 赞 / 110 评论）
Ali Data Analytics 发 19 页《Agentic AI: Complete Developer Study Notes》，评论区几乎全是求完整版、私信领取。
- [Facebook 原帖](https://www.facebook.com/alitheanalyst/posts/pfbid0tejP8GF42R92voVD7WYkYFxPec2hificmWz52HhwujP9MaJq9yWGJ8iPQjeDtDsRl)

### 14. LinkedIn — Microsoft CVP Mark Chaban（10/26）
Fabric IQ 已在 Copilot Chat / Cowork GA，答案直接 grounded 在 Power BI semantic model 的可信定义上，且不额外收 AI token 费。
- [LinkedIn 文章](https://www.linkedin.com/pulse/trust-new-competitive-advantage-ai-mark-chaban-msz2e)

## 可直接做内容的选题
- “SQL is the small part”：护城河是 context graph + semantic layer，不是生成 SQL
- 钩子数字：Agents now out-query humans — 17M databases a day
- Google 的护栏拆分：skills 是建议、IAM 才是强制
