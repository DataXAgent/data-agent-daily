---
layout: post
title: "Data Agent Daily — 2026-11-15"
author: dad
date: 2026-11-15
image: "assets/images/covers/2026-11-15.svg"
description: "日本 CloudShift 在 11 月 15 日发布 RDB 联动 AI 智能体 DataMind AI：自然语言生成 SELECT 语句查询业务数据库，结果以 Key＆Value 形式交给 AI 分析加工，还可写回数据库形成数据循环。"
categories: ["Data Agent Daily"]
tags: ["data-agent", "news"]
comments: false
---

## 今日速览

- 日本 CloudShift 在 11 月 15 日发布 RDB 联动 AI 智能体 DataMind AI：自然语言生成 SELECT 语句查询业务数据库，结果以 Key＆Value 形式交给 AI 分析加工，还可写回数据库形成数据循环。
- Cube 在 11 月 13 日上线 Cube in ChatGPT：在 ChatGPT 内安装插件、登录 Cube 账号后可用自然语言问数，图表与仪表盘由语义层生成，数字均来自数据模型中的度量并遵循用户自身的 Cube 权限。
- Hex 4.0 在 11 月 10 日进入公开 Beta：项目改为全代码定义，Claude、Codex、Cursor 等外部智能体可直接构建数据应用并推送进 Hex，官方图表显示 4 张内部看板加载比 3.0 快 4–12 倍。
- Strategy 在 11 月 13 日发布 11 月产品更新：Strategy MCP Server 可直接使用已认证的内存型与实时 Intelligent Cubes，无需为每个 cube 单独开启 AI 功能；Mosaic Sentinel Mission Control 新增运行集中视图。
- Cube Core 在 11 月 14–15 日连发三个小版本 v1.8.24、v1.8.25、v1.8.26，均为修复与性能改进，无实质新功能。

## 公司发布 / 官方博客

### 1. 日本 CloudShift 发布 RDB 联动 AI 智能体 DataMind AI（11/15）
日本株式会社云端移转（CloudShift）在 11 月 15 日发布 RDB 联动型 AI 智能体 DataMind AI，以 TEXT to SQL 方式连接企业业务系统与 CMS 的关系型数据库，做业务数据的分析、加工、可视化与格式转换。DataMind AI 从自然语言生成 SELECT 语句抽取所需信息，再以 Key＆Value 形式作为上下文交给 AI，发布方称这种方式比 RAG 在数据精度与提示传达力上更优；AI 的回答可写回另一数据库或表再作上下文，发布方把这种用法称为「数据循环」。检索—加工—登记可注册为任务，提示词中设变量后可以网站登记为触发批量处理，或按月改写多条记录。当面对应数据库为 MySQL 与 Oracle，简易用途可用 SQLite；对应 LLM 为 ChatGPT 与 Azure OpenAI，Gemini 与 Claude 正在动作验证中。后续计划以 MCP 连接外部云服务并对应 RAG、扩展 CMS 联动。展开分两阶段：先以 SI 服务积累事例，第二阶段再提供云服务；同时招募 SI 与 IT 咨询合作伙伴。
- [atpress 新闻稿（StartHome 转载，11/15，JST 12:12）](https://home.kingsoft.jp/news/pr/atpress/435486.html)

### 2. Cube in ChatGPT 上线：语义层问数进对话（11/13，补录）
Cube 在 11 月 13 日的 changelog 中宣布 Cube in ChatGPT 上线：在 ChatGPT 内安装 Cube 插件、登录 Cube 账号后可用自然语言问数，Cube 按语义层返回图表与仪表盘，数字均来自数据模型中的度量，并遵循用户自身的 Cube 权限。Cube 在对话中以完整应用运行：可浏览 Workspace 的仪表盘、工作簿与探索，选中图表追问；要求新建仪表盘时由 Cube 搭建、改动以草稿待审核发布；Cube Home 按每个视图推荐问题；图表可全屏打开或下载 PDF。同批 changelog 还包括日期筛选器改进（Presets、Relative、Fixed 三个页签的单弹窗）与 /v1/cubesql 支持 `:name` 参数。
- [Cube 官方 changelog（11/13）](https://cube.dev/changelog)

### 3. Hex 4.0 进入公开 Beta：项目全代码定义，外部智能体可直接构建应用（11/10，补录）
Hex 在 11 月 10 日的官方 changelog 中宣布 Hex 4.0 进入公开 Beta，面向全部合同客户开放，自助计划需邮件 beta@hex.tech 开通。项目改为全代码定义，Claude、Codex、Cursor 等外部智能体可直接构建数据应用并推送进 Hex，纳入治理、权限与用量日志；也可把现有 Hex 应用拉回外部智能体继续改。Context Studio 把 ChatGPT、Slack、Claude 等外部智能体的交互与 Hex 内活动统一可观测。新 UI 以审查为中心，点击任意数字或图表可 Inspect 查看背后逻辑与所用语义模型。换全新执行引擎与计算架构，官方图表显示 4 张内部看板的加载时间比 3.0 快 4–12 倍（EPD KPIs 2 分 24 秒→35 秒、PLG Metrics 3 分 0 秒→16 秒、Agent Usage 2 分 23 秒→12 秒、CFO Dashboard 30 秒→6 秒）。Hex 4.0 在 10 月 27 日首次发布时为私有 Beta，同步宣布 1 亿美元 D 轮融资、估值 12 亿美元（Peak XV 与 137 Ventures 领投）。现有项目不受影响、不自动迁移；4.0 暂缺部分功能。
- [Hex 官方 changelog（11/10）](https://learn.hex.tech/changelog/2026-11-10)
- [Cooley：Hex 1 亿美元 D 轮融资（10/27）](https://www.cooley.com/news/coverage/2026/2026-10-30-hex-raises-100-million-series-d-at-1-2b-valuation)

### 4. Strategy 11 月产品更新：MCP 直用已认证 Cubes，新增 Mosaic 运行监控（11/13，补录）
Strategy 在 11 月 13 日的官方博客中发布 11 月产品更新。Strategy MCP Server 现可直接使用已认证的内存型与实时 Intelligent Cubes，无需为每个 cube 单独开启 AI 功能（内存型 cube 仍需发布，实时 cube 无此要求）；博客注明 MCP 访问 cube 本身不是新功能，本次扩大了可用范围。Auto Dashboard 2.0 改进 HTML 布局导入与批量改名，Auto Summary 与 Auto Narratives 覆盖分层页面。Mosaic Sentinel Mission Control 新增集中视图，汇总风险、审计活动、用量、成本与性能并提示值得调查的变化，不自动修复。Mosaic Studio 数据准备支持 unions；Workstation 支持以 Python 脚本作可复用度量函数。
- [Strategy 官方博客（11/13）](https://employee.microstrategy.com/blog/november-2026-product-updates)

## 开源项目

### 5. Cube Core 连发三个小版本：修复与性能改进（11/14–11/15）
Cube Core 在 11 月 14 日发布 v1.8.24 与 v1.8.25，11 月 15 日发布 v1.8.26，均为修复与性能改进，无实质新功能：v1.8.24 让 server-core 每请求最多运行一次 context 函数；v1.8.25 让 tesseract 在多阶段度量间共享扫描并融合计算；v1.8.26 把 LIMIT 下推到 cubestore 的无 ORDER BY/GROUP BY 查询，并修复 tesseract 预聚合连接路径匹配。
- [Cube GitHub Releases](https://github.com/cube-js/cube/releases)

## 论文 / arXiv

arXiv 11 月 14–15 日为周末，无新论文列表，四分类列表页仍停在 11 月 13 日星期五一期；Hugging Face Papers 无 11 月 14–15 日的日榜；Spider 2.0、BIRD、DABstep、DAComp 等评测基准当日无原作者团队新动态。

## 社交媒体

社交媒体当日未见可核实的数据智能体新内容，多为 11 月 11–13 日 Databricks Genie 发布的转载与解读；中文媒体层当日未见可核实的数据智能体新内容；新闻网站当日未见可核实的数据智能体新内容。

本期检索范围内，监测名单内其余厂商、研究团队与开源项目在过去 24 小时内未见可核实的新动态；Cube v1.8.24/v1.8.26 为补丁版本、内容已在上文核实说明。

## 今日回顾

日本 CloudShift 在 11 月 15 日发布 RDB 联动 AI 智能体 DataMind AI，自然语言生成 SELECT 语句查询业务数据库，结果以 Key＆Value 形式交给 AI 分析加工，还可写回数据库形成数据循环；Cube 在 11 月 13 日上线 Cube in ChatGPT，语义层问数进对话，数字均来自数据模型中的度量并遵循用户自身的 Cube 权限，Cube Core 同期连发 v1.8.24、v1.8.25、v1.8.26 三个修复与性能改进小版本；Hex 4.0 在 11 月 10 日进入公开 Beta，项目全代码定义，外部智能体可直接构建数据应用并推送进 Hex，内部看板加载比 3.0 快 4–12 倍；Strategy 在 11 月 13 日发布 11 月产品更新，MCP Server 可直用已认证的 Intelligent Cubes，Mosaic Sentinel Mission Control 新增运行集中视图；arXiv 周末无新列表，社交媒体与中文媒体层当日未见可核实的数据智能体新内容。
