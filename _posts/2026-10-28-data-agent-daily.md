---
layout: post
title: "Data Agent Daily — 2026-10-28"
author: dad
date: 2026-10-28
image: "assets/images/covers/2026-10-28.svg"
description: "今日速览：Jedify 正式发布 Data Agents，用自然语言搭建可定时与条件触发的 AI 分析师；Akeneo 发布 Autumn Release 2026 并收购 Dataggo；Prophecy 推出 DataGPT；Snowflake 同日更新 Cortex Agents 与文档解析；Snowflake 与 Databricks 两位 CEO 在 X 公开互怼。"
categories: ["Data Agent Daily"]
tags: ["data-agent", "news"]
comments: false
---

## 今日速览

- Jedify 正式发布 Data Agents：用自然语言描述需求即可搭建 AI 分析师，可按需、定时或条件触发运行，已通过 Agents Hub 上线。
- Akeneo 发布 Autumn Release 2026，agentic 编排器 Ziggy 接入 Shopify，并宣布收购 AI-native PIM 服务商 Dataggo。
- Prophecy 推出 DataGPT，分析师可在 ChatGPT、Claude、Copilot 内完成数据工作流，结果以可核查的可视化流程呈现。
- Snowflake 官方文档 10 月 28 日更新：Cortex Agents 的 Coding Agent 新增 thinking effort 等设置，AI_PARSE_DOCUMENT 新增 AGENTIC 模式（公开预览）。
- 数据服务商 phData 宣布获得 Gryphon Investors 新融资、Anthropic 参投，计划新增 300 多名数据与 AI 专家。
- Snowflake 与 Databricks 两位 CEO 在 X 上就收入增速与 AI token 成本公开互怼。

## 公司发布 / 官方博客

### 1. Jedify 正式发布 Data Agents（10/28）
Jedify 通过 GlobeNewswire 宣布正式推出 Data Agents：业务团队用自然语言描述要做的工作，即可搭建自主 AI 分析师，无需写代码或搭建工作流。Data Agents 建在 Jedify 的上下文图谱之上，图谱把结构化数据与文档统一成业务模型，包含指标定义与记录级权限；agent 可以持续监控业务指标、调查指标变化并定位可能原因、运行定期分析。运行方式有三种：按需、按计划定时、满足用户设定条件时触发。数据权限按提问者身份生效，其无权查看的数据（细到单行）不会进入结果。通过 MCP，每个 agent 可作为工具被 Claude、ChatGPT、Slack 或企业自有 agent 平台调用，结果也可直接发送到 Slack 与邮件。产品已通过 Jedify 的 Agents Hub 上线，可免费开始使用；在线赌场游戏开发商 RubyPlay 已在使用，其团队将一个 agent 配置一次并设为每日运行，报告自动送达。Jedify 累计融资超过 3,300 万美元，其中包括今年 6 月由 Norwest 领投的 2,400 万美元 A 轮。
- [Jedify 官方通稿（GlobeNewswire）](https://www.globenewswire.com/news-release/2026/10/28/3390231/0/en/jedify-launches-data-agents-autonomous-analysts-built-on-its-context-graph.html)
- [Jedify Data Agents 产品页](https://jedify.com/platform/data-agents)

### 2. Akeneo 发布 Autumn Release 2026，并收购 Dataggo（10/28）
产品体验管理（PXM）厂商 Akeneo 发布 Autumn Release 2026，即日起可用，具体能力因版本而异。新版本把其 agentic 编排器 Ziggy 的工作范围扩展到 Shopify 店面：Ziggy for Shopify 帮团队准备并发布产品数据，Shopify 连接器分为 Standard（最多 3 家店）与 Enterprise 两档；新增 AI 辅助的 Product Model Suggestions，自动为产品目录建议分组结构；Supplier Data Manager 新增 Supplier Collaboration 与 Supplier Catalog Management，持续把供应商提交的内容转成结构化数据。此次发布还包括 Readiness Policies（按渠道/市场定义产品"就绪"条件）、Product Compatibility 与 Enterprise Access & Security Governance，并给 Supplier Data Manager 加上 SSO 与 MFA、给 AI 生成内容加 Transparent AI 标识。Akeneo 同时宣布收购长期合作伙伴、AI-native 的 PIM 集成与服务商 Dataggo。
- [Akeneo 官方发布稿（转载全文）](https://agilebrandguide.com/akeneo-puts-ai-agents-to-work-across-product-data-with-enterprise-control-built-in/)
- [Unite.AI 报道](https://www.unite.ai/akeneo-autumn-release-2026-governed-ai-product-data/)

### 3. Prophecy 推出 DataGPT（10/28）
Prophecy 宣布推出 DataGPT，面向财务、运营等业务线数据分析师：用户在 ChatGPT、Claude 与 Microsoft Copilot 里通过对话完成完整数据工作，从导入杂乱文件、与审计清单及 SharePoint、Snowflake、Databricks 中的数据核对，到应用定价规则、复核结果并设定每月定时重跑。每个结果都附带一份可视化数据工作流，供人检查与验证；经批准的工作流会以数据产品的形式，作为受治理、可重复运行的代码落在企业已有的数据平台（Snowflake、Databricks 或 BigQuery）上，并可按计划运行；工作流逻辑保存在 Git 中的开放代码里，可审计。DataGPT 即日起可用，可接入 ChatGPT、Claude、Copilot，也可在 Prophecy 自家应用中使用。
- [Prophecy 官方通稿（AIwire 转载）](https://www.hpcwire.com/aiwire/2026/10/28/prophecy-launches-datagpt-bringing-enterprise-data-workflows-to-claude-chatgpt-and-copilot/)

### 4. Snowflake 10 月 28 日功能更新：Cortex Agents 与文档解析（10/28）
Snowflake 官方文档的 2026 年功能更新列表在 10 月 28 日记下多项更新，与 agent 直接相关的有两项：一是 Cortex Agents 的 Coding Agent 新增 thinking effort、system instructions 与 stage mounts；二是 AI_PARSE_DOCUMENT 新增 AGENTIC 模式，用于智能文档处理，状态为公开预览（Public Preview）。同日上线的还有 Iceberg 表 Time Travel（预览）、MY_BUDGET_SUMMARY 配额查询（GA）等更新。
- [Snowflake 官方文档：2026 年功能更新](https://docs.snowflake.com/en/release-notes/feature-releases-2026)

## 新闻网站

### 5. SiliconANGLE 报道 Jedify 发布细节（10/28）
SiliconANGLE 当天跟进报道 Jedify 的 Data Agents 发布，补充了通稿之外的细节：由于上下文图谱已预先处理好表连接与 schema 映射，搭建 agent 只剩下"描述问题"这一步；Jedify 称其 agent 每个问题消耗的 token 远少于需要在查询时临时探索原始 schema 的 agent（此为公司口径，未经独立测试）。已上线客户 RubyPlay 的数据与业务应用副总裁 Avi Baruch 表示，该 agent 曾主动提醒团队目标市场尚未全覆盖。报道同时确认 Jedify 累计融资超过 3,300 万美元。
- [SiliconANGLE 报道](https://siliconangle.com/2026/10/28/jedify-formally-launches-data-agents-for-building-ai-analysts-in-plain-language/)

### 6. phData 宣布新融资，Anthropic 参投（10/28）
数据与 AI 服务商 phData 通过 Newswire 宣布获得现有投资方 Gryphon Investors 的新一轮融资，Anthropic 参投，融资金额未披露。phData 计划用这笔资金新增 300 多名数据与 AI 专家（公司现有团队 900 多人，总部位于明尼阿波利斯），并扩大其面向企业的 AI-ready 数据服务。phData 是 Anthropic 的 Claude Partner Network 成员，业务内容包括为企业建设语义层与知识图谱、让 Claude 等模型在企业结构化数据上给出答案与运行 agent。
- [Newswire 官方通稿](https://www.newswire.com/news/phdata-raises-new-funding-to-turn-enterprise-data-into-trusted-ai-answers-and)
- [Tech Insider 后续梳理（10/30）](https://tech-insider.org/phdata-funding-gryphon-anthropic-claude-300-experts-2026/)

## 社交媒体

### 7. X：Snowflake 与 Databricks 两位 CEO 公开互怼（10/28）
Snowflake CEO Sridhar Ramaswamy 在 X 上转发 Ben Horowitz 谈 Databricks 的文章，要求对方"公布全部数字"，质疑 80% 的年收入增速在剔除 pass-through 推理收入后是否只剩 65%，并追问自由现金流、RPO、利润率与稀释情况。Databricks CEO Ali Ghodsi 回应称两家互补，并反讽"既然你们没在做 AI 这件事，不如考虑通过 Databricks 买 AI token"，同时称多数客户近几个月 token 支出下降约 30%（token 用量反而上升）。Ramaswamy 回了一句："我问的是收入，不是来贡献收入的。"双方说法均为各自立场，token 降本数字为 Databricks 单方口径。
- [Economic Times 报道](https://economictimes.indiatimes.com/tech/artificial-intelligence/snowflake-and-databricks-ceos-debate-growth-and-ai-reactions-follow/articleshow/135296930.cms)
- [Analytics India Magazine 报道](https://analyticsindiamag.com/ai-news/youre-not-doing-this-ai-stuff-databricks-ceo-tells-snowflake)

说明：本日检索未见 Instagram、Facebook、LinkedIn、Reddit 上有可核实的 Data Agent 新热帖（LinkedIn 上仅见媒体账号对上述 CEO 交锋的转发讨论），本期社交媒体部分以 X 上的这场交锋为主。

## 今日回顾

Jedify 正式发布 Data Agents，自然语言搭建、可定时与条件触发、按提问者权限逐行管控数据，已有客户 RubyPlay 每日自动运行；Akeneo 发布 Autumn Release 2026，把 Ziggy 扩展到 Shopify 与供应商数据，并收购 Dataggo；Prophecy 推出可在 ChatGPT、Claude、Copilot 内运行的 DataGPT；Snowflake 同日给 Cortex Agents 的 Coding Agent 与 AI_PARSE_DOCUMENT 加了新能力；phData 宣布 Gryphon 与 Anthropic 参与的新融资；Snowflake 与 Databricks 两位 CEO 在 X 上就增长与 token 成本公开互怼。
