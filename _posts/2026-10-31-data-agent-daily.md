---
layout: post
title: "Data Agent Daily — 2026-10-31"
author: dad
date: 2026-10-31
image: "assets/images/covers/2026-10-31.svg"
description: "今日一句话判断：agent 的竞争正在从“会答问题”转向“谁拥有可信、可计价、可治理的上下文”——Hex 为此重写了整个产品，ZoomInfo 把 GTM 上下文接进 Snowflake agent，Dataline 则想给 agent 的每一次数据调用标价。"
categories: ["Data Agent Daily"]
tags: ["data-agent", "news"]
comments: false
---

> 今日一句话判断：agent 的竞争正在从“会答问题”转向“谁拥有可信、可计价、可治理的上下文”——Hex 为此重写了整个产品，ZoomInfo 把 GTM 上下文接进 Snowflake agent，Dataline 则想给 agent 的每一次数据调用标价。

## 公司发布 / 官方博客

### 1. Hex 发布 4.0 并完成 $100M D 轮，估值 $12 亿（10/27）
Hex 宣布从头重写的数据分析平台 Hex 4.0，同时完成 1 亿美元 D 轮融资、估值 12 亿美元，由 Peak XV 与 137 Ventures 领投。CEO Barry McCardel 坦言：旧产品加了四年 AI 也“远非 agent native”——agent 工具箱膨胀到数百个、外部 agent 只能走 MCP、计算引擎不是为高并发 agent 工作流设计的。4.0 的核心假设是“一切皆代码”：项目逻辑与可视化全部由代码文件支撑、而非专有 YAML，同时叠加受治理的上下文与审查工具，让人和 agent 在同一批产物上协作；外部 agent（Claude、Codex、Cursor）也可直接调用 Hex 平台。公司称全球客户超 2,500 家，但 4.0 目前仍处 private beta，定价与 agent 计量细节尚未公布。
- [Hex 官方：Introducing Hex 4.0](https://hex.tech/blog/introducing-hex-4-0/)
- [Hex 官方：$100M 融资公告](https://hex.tech/blog/hex-new-era/)
- [CryptoBriefing 报道](https://cryptobriefing.com/hex-100-million-series-d-ai-agents/)

### 2. ZoomInfo MCP 与 API 上线 Snowflake（10/30）
ZoomInfo 宣布其 MCP 连接器与 API 已进入 Snowflake AI Data Cloud，均经由 GTM.AI（其 headless GTM 上下文层）接入。业务用户可在 Snowflake CoWork 里用自然语言查询 ZoomInfo 数据，经管理员批准后可暴露给 Snowflake Cortex Agents；数据团队则可用 Search、Enrich、Lookup、Bulk、Monitoring 五组端点实时或批量 enrich  Snowflake 表（批量上限为每请求 10,000 条、每查询 200,000 条）。ZoomInfo 称其 GTM Context Graph 覆盖 1 亿+公司、5 亿+联系人及数十亿购买信号；每次调用走 OAuth 2.0 并继承用户在 ZoomInfo 内的角色权限，全部用量记入审计框架——10 月 30 日各家通稿的共同主题正是“agent 能读什么数据、凭什么权限读”。
- [ZoomInfo 官方发布稿](https://www.zoominfo.com/newsroom/press-releases/zoominfo-mcp-api-launch-snowflake)
- [Business Wire 原稿](https://www.businesswire.com/news/home/20261030229214/en/ZoomInfo-launches-New-MCP-Connector-and-API-on-Snowflake)

### 3. dbt Labs 博客：LangChain 如何用分层上下文把自助分析问题量做到 40 倍（10/27）
LangChain 的分析工程团队复盘了他们的 Hex agent 上下文体系：第一层是 dbt 项目本身——表与字段描述同步进 BigQuery，任何读 BigQuery 的 agent 都继承同一套描述；Hex agent 还能直接读 dbt 仓库与 DAG，理解模型上下游与 SQL 逻辑。在此之上再叠三层：写在 dbt 仓库里、经 GitHub Action 导入 Hex 的 workspace guides（业务概念，如 ARR 口径）；代码化的语义层（指标与 join 关系）；以及“背书”机制（只把少数 mart 模型与看板标为可信源，改动需数据团队评审）。结果是自助分析提问量增长 40 倍，数据团队的工作从“代答问题”转为“拥有上下文”。下一步是补 evals 并用 Hex CLI 继续丰富上下文。
- [dbt Labs 博客](https://courses.getdbt.com/blog/langchain-self-serve-analytics-ai-agent-context)
- [LangChain 官方复盘（7 月，佐证 40 倍口径）](https://www.langchain.com/blog/agent-data-stack)

## 新闻网站

### 4. Dataline 宣布 $10.6M 融资，做 agent 可付费的数据层（10/31）
Dataline 宣布 1,060 万美元融资并启动首批 AI Data Launch 合作伙伴，定位是“agent 可付费的数据网络”：任何人可发布数据 feed，任何 agent 可按调用付费（x402），每次 API 响应附带 AI 置信度评分（来源可靠性、新鲜度、一致性），让 agent 在行动前标记或拒绝不可信数据。首批合作方包括 Hyperliquid、Polymarket、Kalshi、Base、Robinhood Chain、BNB、Sui、TON 等，Base 与 Robinhood Chain 上的开发者可免费接入。公司称已支撑 1,940 万笔链上交易、agent 任务成功率 96.4%（均为公司口径，无第三方核验）。注意一个口径差异：The Block 10 月 21 日报道称这轮实际在 4 月就以 SAFE + token warrant 形式签约、未披露估值——10 月 31 日的通稿是正式官宣，而非本周新到账的现金。
- [GlobeNewswire 通稿（转载）](https://portal.sina.com.hk/finance/finance-globenewswire/globenewswire/2026/10/31/1973035/dataline-raises-10-6m-to-give-ai-agents-data-they-can-trust/)
- [The Block 报道（4 月签约口径）](https://www.tradingview.com/news/bloomingbit:7fb207559094b:0-dataline-raises-10-6-million-seed-round-plans-ai-agent-data-network-expansion-and-token-launch/)

### 5. 第三方实测：Snowflake CoCo agent 比人工快 4.6 倍，Databricks Genie Code 未独立跑完全流程（10/29）
Signal65 用同一套真实场景（美国 DOT 航班延误数据集）在 Snowflake 与 Databricks 上各跑两遍：人工与各家 agentic 工具。结果是 Snowflake 的 CoCo agent 以 68 分钟跑完全部七阶段工作流，人工需 316 分钟（4.6 倍）；治理与 PII 保护任务快 32%；且 CoCo 可在平台内与开发者本机直接工作。而 Databricks 的 Genie Code 未能在无人干预下完成全部外部应用工作流，需借助第三方 agent（Claude Code），耗时约 4 倍。提醒：这是单一场景、单家评测机构的结果，可作选型参考，不宜直接外推为全量能力对比。
- [Signal65 评测](https://signal65.com/research/ai/snowflake-vs-databricks-an-ai-and-enterprise-readiness-evaluation/)

## 社交媒体

### 6. X：Snowflake 与 Databricks 两位 CEO 公开互怼（10/28）
Snowflake CEO Sridhar Ramaswamy 在 X 上转发 Ben Horowitz 谈 Databricks 的文章，要求对方“公布全部数字”，质疑 80% 的年收入增速在剔除 pass-through 推理收入后是否只剩 65%，并追问自由现金流、RPO、利润率与稀释情况。Databricks CEO Ali Ghodsi 回应称两家互补，并反讽“既然你们没在做 AI 这件事，不如考虑通过 Databricks 买 AI token”，同时称多数客户近几个月 token 支出下降约 30%（token 用量反而上升）。Ramaswamy 回了一句：“我问的是收入，不是来贡献收入的。”双方说法均为各自立场，token 降本数字为 Databricks 单方口径。
- [Economic Times 报道](https://economictimes.indiatimes.com/tech/artificial-intelligence/snowflake-and-databricks-ceos-debate-growth-and-ai-reactions-follow/articleshow/135296930.cms)
- [Analytics India Magazine 报道](https://analyticsindiamag.com/ai-news/youre-not-doing-this-ai-stuff-databricks-ceo-tells-snowflake)

说明：今日检索未见 Google Cloud、Microsoft、Databricks 官方博客在过去 24 小时内发布新的 Data Agent 专帖，其最新动态已见本刊首期；X / Instagram / LinkedIn / Reddit 今日除上述 CEO 交锋外，未见可核实的新热帖。

## 可直接做内容的选题
- “Agent-native 不是加法，是重写”：用 Hex 4.0 的案例讲为什么在旧产品上贴 agent 贴不住——工具膨胀、MCP 单通道、计算引擎三处旧账，适合做一张“旧架构 vs agent-native 架构”对比图
- “你的 agent 凭什么权限读数据”：以 ZoomInfo × Snowflake 为例，讲 OAuth + 角色权限 + 审计这条线为什么是 10 月 30 日通稿的共同主题，钩子：agent 时代的权限模型就是新的数据治理
- “数据开始按调用卖给 agent”：Dataline 的 x402 + 置信度评分，讲数据产品计价方式的变化——从卖订阅到卖每次调用的可信度，适合接 RecSys 视角：推荐系统早就按 impression 计价，数据层正在跟上
