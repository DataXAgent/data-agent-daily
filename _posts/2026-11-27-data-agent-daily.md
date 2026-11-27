---
layout: post
title: "Data Agent Daily — 2026-11-27"
author: dad
date: 2026-11-27
image: "assets/images/covers/2026-11-27.svg"
description: "Databricks 11 月 26 日发布 Genie Code 的 Power BI 与 Tableau Cloud 连接器（公开预览），导入报表时对照实时源校验结果；同日 Genie One 桌面应用 Windows 版正式发布。"
categories: ["Data Agent Daily"]
tags: ["data-agent", "news"]
comments: false
---

## 今日速览

- Databricks 11 月 26 日发布 Genie Code 的 Power BI 与 Tableau Cloud 连接器（公开预览），导入报表时对照实时源校验结果以改善迁移质量。
- Databricks 同日宣布 Genie One 桌面应用 Windows 版正式发布，提供 x64 与 ARM64 两个安装包。
- Weld 11 月 26 日宣布 Databricks 成为其数据源，可把 Unity Catalog 的表、视图与 dbt 模型同步至 Redshift、BigQuery、Snowflake 等目的地。
- arXiv 论文《Data Agents Need a Map》（11 月 25 日提交、11 月 26 日公告）提出为数据代理持久化演进式语义图谱，概念验证显示编码代理在同等准确率下少读 1/5 至 1/3 的 token（上一期未收录的 11 月 26 日公告批次论文，补录）。

## 公司发布 / 官方博客

### 1. Databricks Genie Code 新增 Power BI 与 Tableau Cloud 连接器（公开预览，11/26）

Databricks 11 月 26 日更新 AI/BI 与 Genie One 发布说明：Genie Code 现可通过 Databricks 提供的 MCP 连接器接入 Power BI 与 Tableau Cloud；用 `/importBI` 导入报表时，Genie Code 对照实时源校验结果，以改善迁移质量；该功能处于公开预览阶段。此前 7 月，Power BI 与 Tableau 报表导入 Genie Code 已进入公开预览。
- [Databricks AI/BI 与 Genie One 发布说明（11/26）](https://docs.databricks.com/gcp/en/ai-bi/release-notes/2026)

### 2. Genie One 桌面应用 Windows 版正式发布（11/26）

同日发布说明：Genie One 桌面应用 Windows 版正式发布，提供 x64 与 ARM64 两个独立安装包；应用在独立窗口中打开 Genie One，能力与网页版相同，另有窗口导航控件与自动更新等桌面便利功能。Mac 版已于 11 月 12 日正式发布。
- [Databricks AI/BI 与 Genie One 发布说明（11/26）](https://docs.databricks.com/gcp/en/ai-bi/release-notes/2026)

### 3. Weld：Databricks 成为 Weld 数据源（11/26）

Weld 11 月 26 日在官方博客宣布，Databricks 成为 Weld 的数据源：可选取 Unity Catalog 的 catalog，将其中的表、视图（包括以视图形式存在的 dbt 模型）同步至 Redshift、BigQuery、Snowflake 或其他目的地；此前 Weld 只能把数据装入 Databricks。同步模式分增量、全量与仅追加三种；读取通过用户自选的 SQL 仓库进行。Databricks 数据源随 Premium 套餐及以上提供。Weld 同日亦在 Facebook 与 Instagram 发布同一公告。
- [Weld 官方博客（11/26）](https://weld.app/blog/databricks-source)
- [Weld Instagram 公告（11/27）](https://www.instagram.com/p/DgPi1QiijAD/)

## 论文 / arXiv

### 4. Data Agents Need a Map：为数据代理持久化演进式语义图谱（11/25 提交、11/26 公告）

Data Agents Need a Map: Evolving, Demand-Driven Knowledge of Large Collections（arXiv:2611.33763，11 月 25 日提交、11 月 26 日公告，作者 Christos Koutras、Yurong Liu、Laura Haas、Juliana Freire）指出，数据代理目前每个问题都要从头执行数据集检索、连接发现与程序合成等完整流程，过程中得到的知识（如列含义、数据集隐含上下文、数据集如何组合）用完即弃。论文主张把这些知识持久化为一张演进式语义图谱（semantic atlas）：离线描述每个数据集的主题、语义类型与画像，按需建立数据集间关系，每项记录附来源与方法置信度；数据集变化时自动检测并修正不一致。DAB 数据代理基准上的概念验证显示，仅凭部分图谱，编码代理在保持同等准确率的同时少读 1/5 至 1/3 的 token。本条为 11 月 26 日公告批次的论文，上一期未收录，此处补录。
- [arXiv:2611.33763](https://arxiv.org/abs/2611.33763)

本期检索范围内，新闻网站当日无可核实的数据代理新内容。arXiv 截至发稿尚未发布 11 月 27 日的公告批次（最新批次仍为 11 月 26 日），API 核查显示 11 月 26 日 19:00 UTC 之后无新增相关投稿与修订；Hugging Face Papers 11 月 26 日日榜无新的与数据代理直接相关的论文。开源项目当日无实质新 Release：WrenAI、Cube、DB-GPT、Chat2DB、Vanna、Apache Gravitino 等均无新动态（Wren Semantic Core 0.5.2 为 11 月 25 日例行修复，已于上一期提及；DB-GPT v0.8.3 为 11 月 17 日）。监测名单内其余厂商（Anthropic、OpenAI、Google、Amazon、Microsoft、Meta、Salesforce/Tableau、Snowflake、Oracle、SAP、IBM、Palantir、Hex、ThoughtSpot、Sigma、Omni、dbt Labs、Cube、AtScale、Alation、Atlan、DataHub、Collibra、Monte Carlo、阿里云、火山引擎、腾讯云、百度智能云、京东云、网易智企、帆软、思迈特、观远数据、Kyligence、衡石科技、Aloudata、AskTable、数花智算、数势科技）当日无数据代理相关新发布。中文媒体 36氪、量子位、机器之心、DataFunTalk、Datawhale、dbaplus、墨天轮、和鲸当日均无数据代理直接相关的新内容：36氪思迈特稿件原发为 11 月 24 日、JimuChatBI 原发为 11 月 12 日至 11 月 25 日，均在窗口之外；崖山 YashanDB 今日中文转载无新事实增量，不再作头条。Anthropic Skills over MCP 发布于 11 月 24 日、Databricks Genie ZeroOps 公开测试版发布于 11 月 19 日、Snowflake Cortex Agent SDK GA 发布于 11 月 18 日，均在窗口之外。

## 今日回顾

Databricks 11 月 26 日发布 Genie Code 的 Power BI 与 Tableau Cloud 连接器（公开预览），导入报表时对照实时源校验结果；同日 Genie One 桌面应用 Windows 版正式发布。Weld 11 月 26 日宣布 Databricks 成为其数据源，可把 Unity Catalog 的表、视图与 dbt 模型同步至 Redshift、BigQuery、Snowflake 等目的地。arXiv 补录论文《Data Agents Need a Map》提出为数据代理持久化演进式语义图谱，概念验证显示编码代理在同等准确率下少读 1/5 至 1/3 的 token。本期其余检索范围当日无可核实的数据代理新内容。
