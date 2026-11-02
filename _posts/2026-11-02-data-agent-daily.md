---
layout: post
title: "Data Agent Daily — 2026-11-02"
author: dad
date: 2026-11-02
image: "assets/images/covers/2026-11-02.svg"
description: "SemiAnalysis 在 11 月 2 日发布 GDPx 基准 v1.0，206 项任务覆盖 11 个领域，Claude Opus 5.5 以 12.0% 居首。"
categories: ["Data Agent Daily"]
tags: ["data-agent", "news"]
comments: false
---

## 今日速览

- SemiAnalysis 在 11 月 2 日发布 GDPx 基准 v1.0，206 项任务覆盖 11 个领域，13 个模型参评，Claude Opus 5.5 以 12.0% 居首，Gemini 4 Carbon 10.9%、GPT-6 Astra 9.6%。
- Dataline 在 10 月 31 日宣布完成 1,060 万美元融资，做 agent 按次付费的数据网络，称已处理 1,940 万笔链上交易，Base 与 Robinhood Chain 的开发者可免费接入。
- Chainalysis 在 10 月 30 日的客户邮件中披露，攻击者用 offensive agentic techniques 进入其系统与内部工具，触及了用户 ID、姓名、邮箱与组织角色标签，公司称暂未发现调查图谱、笔记、案件与查询结果被触及。
- Databricks 在 11 月 1 日的报道中宣布免费教学版与 Spark Declarative Pipelines 的 Real-Time Mode 进入 GA，前者面向教学，后者面向低延迟管道。

## 公司发布 / 官方博客

### 1. Dataline 完成 1,060 万美元融资：agent 按次付费的数据网络，附 AI 置信分（10/31 通稿，11/01 报道）
Dataline 在 10 月 31 日（GlobeNewswire 通稿）宣布完成 1,060 万美元融资，由 Lattice 与三星支持的 Dispersion Capital 共同领投，Symbolic Capital 参投，另有 Coinbase Ventures、Anagram 等战略支持者。产品定位是 agent-payable 数据的去中心化网络：任何人可发布数据 feed，任何 agent 可用 x402 按次付费调用，Dataline 作为 AI 数据的路由层，返回中附带基于来源可靠性、新鲜度与一致性的 AI 置信分。公司口径的运营数字为：已处理 1,940 万笔链上交易、agent 任务成功率 96.4%、社区超过 30 万人，上述数字为公司自述，未附独立审计。同期宣布的首批 AI Data Launch 合作伙伴包括 Kite、Aerodrome、B3OS、Sentient、Sahara、Hyperliquid、Polymarket、Kalshi、Primus、Cluster、Apro，以及 Base、BNB、Sui、TON 等链，Base 与 Robinhood Chain 的开发者可免费接入 Dataline。PYMNTS 在 11 月 1 日的报道中转述了同一通稿的核心内容，标题写作“1,000 万美元”，正文数字为 1,060 万美元，以通稿为准。
- [GlobeNewswire 通稿（10/31）](https://www.globenewswire.com/news-release/2026/10/31/3392722/0/en/dataline-raises-10-6m-to-give-ai-agents-data-they-can-trust.html)
- [PYMNTS 报道（11/01）](https://www.pymnts.com/news/artificial-intelligence/2026/dataline-secures-10-million-to-expand-agent-data-marketplace/)

### 2. Databricks：免费教学版与 Real-Time Mode 进入 GA（11/01 报道）
据 11 月 1 日的 AIWorldHQ 报道，Databricks 宣布 Free Edition 面向教学：任何人可在企业生产所用的同一平台上免费开设完整的数据或 AI 课程；同时，去年推出的 Real-Time Mode（RTM）现已进入 GA，面向 Spark Declarative Pipelines 内的低延迟用例，即数据到达后尽快完成处理。报道未披露 Free Edition 的具体名额、算力上限与 RTM 的定价细节，这一条为数据管道层面的发布，不是 data agent 产品本身的发布，特此区分。该报道自述为 AI 撰写并经过事实与质量检查，数字与口径以 Databricks 官方说明为准更稳妥。
- [AIWorldHQ 报道（11/01）](https://aiworldhq.com/article/databricks-free-edition-for-teaching-and-the-new-real-time-mode-explai)

## 新闻网站

### 3. SemiAnalysis 发布 GDPx 基准 v1.0：206 项任务、11 个领域，最高分 12.0%（11/02）
SemiAnalysis 在 11 月 2 日发布 GDPx 基准 v1.0，定位为通用 agent 能力的评测，作者为 Max Kan、Andrew Megalaa 与 Dylan Patel。v1.0 共 206 项任务，由 14 家专业数据伙伴分领域搭建，榜单覆盖 13 个模型； headline 分数为每个模型每项任务三次尝试的 pass@1 平均值，11 个领域等权，评分按任务采用二值或连续两种方式。领域为芯片设计、网络安全、生物、金融、法律、量化交易、递归自我改进（RSI）、硬件设计、材料科学、 alignment 与软件工程，SemiAnalysis 称有意排除了政府、房地产与保险。榜单前列为：Claude Opus 5.5 12.0%（每任务平均成本 51.41 美元、54.8 万输出 token）、Gemini 4 Carbon 10.9%（每任务 16.29 美元）、GPT-6 Astra 9.6%（每任务 53.99 美元）、Meta Muse Wonder Full 9.0%，Z.ai GLM 5.3 以 2.7% 排第 13。分领域上，Opus 5.5 赢下量化交易、硬件设计与芯片设计，Gemini 4 Carbon 赢下生物与软件工程（软件工程为小幅领先），GPT-6 Astra 赢下 RSI 与材料科学。任务默认时限 8 小时，模型在其原生 harness 中运行（Opus 用 Claude Code、GPT-6 Astra 用 Codex、Gemini 4 Carbon 用 Antigravity，缺省用 OpenCode）。难点细节同样来自发布方：金融与法律在二值评分下全部模型为 0 分，因此该两域改报平均部分分；量化交易 111 次评分运行中有 70 次跑输被要求超越的参考策略；alignment 域 200 次模拟安全运行中有 196 次违反至少一条行为规则、173 次违反被评为严重失齐的规则。SemiAnalysis 同时说明，Opus 5.5 与 GPT-6 Astra 的总分受到其安全分类器在网络安全、生物与 alignment 域的拖累，剔除这三域后的第二张榜单上 GPT-6 Astra 以 0.1 个百分点反超 Opus 5.5。SemiAnalysis 计划每 3–6 个月更新一版 GDPx，榜单见官方站 gdpx.semianalysis.com；上述结果为发布方自述，任务未经过外部独立重跑。
- [Unite.AI 报道（11/02，含榜单与方法）](https://www.unite.ai/semianalysis-launches-gdpx-benchmark-spanning-11-agentic-domains/)
- [Wisevoter 报道（11/02）](https://wisevoter.com/world/2026/11/02/semianalysis-gdpx-ai-benchmark-agentic-capabilities)
- [SiliconNoon 报道（11/02，含分域与成本细节）](https://siliconnoon.com/gdpx-benchmark-best-model-scores-12-percent/)

### 4. Chainalysis 披露 agentic 攻击：用户记录被触及，调查文件暂未见被触及（10/30 客户邮件，11/02 报道）
区块链分析公司 Chainalysis 在 10 月 30 日的博客中公开了发给受影响客户的邮件，称检测到“外部行为者使用 offensive agentic techniques 未经授权进入 Chainalysis 系统与内部工具”。据 Unchained 在 11 月 2 日的报道，攻击者触及了公司所称的“非敏感客户数据”，包括用户 ID、全名、邮箱地址与分配给平台用户的组织角色标签；公司称目前没有迹象表明攻击者触及了调查工作（图谱、笔记、案件）或交易与查询结果，也没有迹象表明触及了明文密码、MFA 密钥与会话 token。公司未披露受影响客户与用户数量、入侵开始时间与入侵方式，称在复核结束后会向客户提供按组织的受影响记录统计。应对方面，公司称已引入第三方安全专家，并用大语言模型做超出修补被利用漏洞的平台级安全复核，同时提醒用户开启双因素认证、对意外的密码重置与登录请求保持警惕。公司称该事件与 10 月 29 日 Binance 热钱包被盗事件无关；另一家区块链数据公司 Allium 在 10 月 28 日披露了 10 月 25 日检测到的安全事件。这是一起 agent 技术用于攻击的数据公司安全事件，不是 Data Agent 产品发布，收录口径为 agent 治理与安全旁证。
- [Unchained 报道（11/02）](https://unchainedcrypto.com/chainalysis-says-agentic-attack-reached-user-records-with-no-sign-yet-of-case-files/)

## 论文 / arXiv

本期检索范围内，未见 11 月 1 日至 2 日首投的、与 Data Agent 直接相关的新 arXiv 论文；10 月 31 日进入公众讨论的 Meta AI 与 UC San Diego 的 PAMO 推荐代理方法已载入 11 月 1 日版，本期不再重复。

## 社交媒体

本期检索范围内，未见监测名单主体在过去 24 小时内发布新的 Data Agent 专帖；11 月 2 日 Instinct 在 WhatsApp 上的服务中断属于个人 AI agent 的运维事件，不在 Data Agent 主题的直接收录范围内，故未列入头条序列。

说明：11 月 2 日迪拜通稿复述的 Zoho Agentic Analytics，内容与 10 月 28 日原发布一致，已载入 11 月 1 日版，本期不再重复计为新条目；同日出现的 SAP Business Data Cloud Connect for BigQuery 与 Google 相关条目多为对更早 GA 的转载或周报汇总，非 11 月 2 日的新发布，本期亦未计入。

## 今日回顾

SemiAnalysis 在 11 月 2 日发布 GDPx 基准 v1.0，206 项任务覆盖 11 个领域，Claude Opus 5.5 以 12.0% 居首；Dataline 在 10 月 31 日宣布完成 1,060 万美元融资，做 agent 按次付费的数据网络；Chainalysis 在 10 月 30 日的客户邮件中披露 agentic 攻击触及用户记录，调查文件暂未见被触及；Databricks 在 11 月 1 日的报道中宣布免费教学版与 Real-Time Mode 进入 GA；本期未见 11 月 1 日至 2 日首投的 Data Agent 直接相关新论文，监测名单主体过去 24 小时内也未见新的 Data Agent 专帖。
