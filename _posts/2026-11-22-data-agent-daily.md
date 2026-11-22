---
layout: post
title: "Data Agent Daily — 2026-11-22"
author: dad
date: 2026-11-22
image: "assets/images/covers/2026-11-22.svg"
description: "AWS Quick 11 月 20 日更新：对话里搭建业务流程、多智能体协同作答、改版 Web 应用与 Meta ads、Amplitude 连接器；Google Cloud 发布数据智能体模拟器与 Managed Airflow 智能体，Vodafone 用数据工程智能体把管线成本降低 30%。"
categories: ["Data Agent Daily"]
tags: ["data-agent", "news"]
comments: false
---

## 今日速览

- AWS 11 月 20 日更新 AWS Quick：对话中搭建 Quick Flows、多智能体协同作答、改版 Web 应用，新增 Meta ads 与 Amplitude 连接器。
- Google Cloud 11 月 21 日介绍内部数据模拟器，用合成数据资产与已验证的 SQL 答案键评测数据智能体，不触碰生产数据。
- Google Cloud 11 月 20 日介绍 Managed Airflow 智能体：控制台智能体排查失败任务，Data Agent Kit 在 IDE 里编写、迁移、部署 DAG，MCP 服务器已 GA。
- Vodafone 捷克 11 月 21 日介绍用 Google 数据工程智能体把 2,000–3,000 行 BigQuery 存储过程迁成 Dataform 管线，执行时间减半、成本降低 30%。
- Databricks 11 月 19 日宣布 Genie Code 的 /importBI 批量迁移正式可用，可一次迁移整文件夹的 Tableau 与 Power BI 报表（补录）。
- 戴尔 11 月 16 日发布 Agentic Data Gateway，为智能体提供统一治理的数据入口，内部测试显示 token 消耗最多降低 76%、答案准确率从 60% 升至 94%（补录）。
- 开源数据智能体框架 DB-GPT 11 月 17 日发布 v0.8.3，新增证据校验与报告恢复、结构化可追溯的数据分析报告、仪表盘工作区与智能体可观测追踪（补录）。
- arXiv 11 月 20 日上线 GenSPARQL：SPARQL 的生成式扩展，让 LLM 在查询求值时为变量绑定生成值。

## 公司发布 / 官方博客

### 1. AWS Quick 更新：对话建流程、多智能体协同作答（11/20）
AWS 11 月 20 日在机器学习博客发布 AWS Quick 更新：用户可在对话中描述业务流程，由 Quick 建成可编排 agent、技能、工具与数据的 Quick Flow，并在同一对话中运行、测试与优化，对话旁有步骤图供核对；新增确定性步骤（固定计算与检查），流程可处理更长运行与更大数据量。新增多智能体编排：一个请求可同时调用多个专业 agent，各自保留自己的指令、知识与上下文，再合并为一份注明各自贡献的回答；AWS 的示例是预测 agent（规划数据）与采购 agent（供应商合同）共同解释某区域运输成本上涨。改版后的 Web 应用在首页呈现待处理事项与每日简报，可起草待审回复；任务在关闭浏览器后继续运行，等待中的 agent 集中在 Mission Control；Library 汇总近期工作，对话、agent 与文件在 web、桌面与移动端同步。新增 Meta ads 连接器（经 Meta ads MCP 服务器，自然语言创建、管理、分析广告系列，写操作前征求许可）与 Amplitude 连接器（产品用量、用户行为与转化）。技能现可在 Web 应用中浏览、安装、创建与管理；提示词护栏进入预览，可过滤内容、屏蔽拒绝主题与词汇、检测提示词攻击、保护选定个人信息，可先以仅检测模式测试，适用于 Professional 与 Enterprise 计划；管理员还可按群组分配权限与用量上限、控制可添加的数据源类型。新增日语、德语、简体与繁体中文、越南语。AWS 引用 Pomelo（拉美金融科技公司）数据负责人的说法：每月使用数据的人数增加近 4 倍而团队未扩大，单个用例每月节省 80 小时工作（客户自述）。更新在 AWS Quick 已覆盖的全部区域可用。
- [AWS 机器学习博客（11/20）](https://aws.amazon.com/blogs/machine-learning/new-in-aws-quick-more-capable-flows-an-updated-web-experience-and-agents-that-work-together/)

### 2. Google Cloud 发布数据智能体模拟器，用合成数据资产做“风洞”评测（11/21）
Google Cloud 11 月 21 日在官方博客介绍内部数据模拟器，把它比作数据智能体的“风洞”：生成与真实组织结构、因果行为相同的合成数据资产（数据库、文档、聊天记录），所有名称、数字与文档均为合成，用于在不触碰生产数据的情况下评测企业数据智能体。管线分四阶段：① Compile blueprint，用 LLM 把简短的英文模式描述编成冻结蓝图，固定公司的系统、人员、指标与个体信念（可故意埋入错误信念）；② Simulate & build tables，按蓝图与随机种子确定性生成表与 SQL 答案；③ Render documents，把事实写成备忘与聊天记录；④ Evaluate agent，在只读工具上测试智能体。基准的校验包括：每道定量题附带算出金答案的 SQL，并以诱饵 SQL 验证掉入常见陷阱会得到不同数字；无法验证的题直接丢弃；另设幻觉哨兵，如提问虚构指标“Basalt Velocity Ratio”，可靠的智能体应报告该指标不存在。真实性检验分三层：统计特性报告（join fan-out、key skew、Benford 定律等）、领域专家评审、100 多项独立校准检查；Google 称内部评估显示，能力升级在合成资产与人工基准上移动方向与排序一致。多智能体在成对真实与合成客户资产上的对照研究正在进行。Google 同时指出合成评测的两项风险：对模拟器模式的过拟合，以及业务演变带来的漂移。
- [Google Cloud 官方博客（11/21）](https://cloud.google.com/blog/products/data-analytics/a-data-simulator-to-test-agents)

### 3. Google Cloud 介绍 Managed Airflow 智能体：排查失败任务、写 DAG、检升级 readiness（11/20）
Google Cloud 11 月 20 日在官方博客介绍 Managed Service for Apache Airflow（原 Cloud Composer）的智能体能力：控制台内的 Managed Airflow Agent 排查失败任务、建议环境改进、检查 DAG 是否可升级到新版 Airflow；IDE 或编码智能体中的 Data Agent Kit 编写、迁移、部署 DAG；Managed Airflow MCP 服务器已 GA，任何兼容 MCP 的 agent 可管理环境、列出与触发 DAG、检查运行状态；Apache Airflow Common AI provider 可在 Airflow 3 DAG 内运行 LLM 驱动的步骤，如基于 LLM 的分支、区分 transient 错误与坏输入的智能重试、schema drift 检测。博客以虚构公司 Cymbal Shops 的演示串起功能：点击流小时批处理因流量增长内存溢出，控制台智能体诊断后建议 worker 内存从 4GB 升至 8GB，并指出数据库 retention 未启用、环境非高可用、无定时快照三处缺口，智能体只读、改动由人执行；随后 Data Agent Kit 的迁移技能把 DAG 迁到 Airflow 3 事件驱动调度，8 倍峰值流量负载测试下单任务内存保持在 1GB 以下，点击到 BigQuery 的延迟从 1 小时以上降至几分钟。
- [Google Cloud 官方博客（11/20）](https://cloud.google.com/blog/products/data-analytics/scaling-airflow-pipelines-with-ai-agents-on-managed-airflow)

### 4. Vodafone 用 Google 数据工程智能体迁移 BigQuery 存储过程，成本降低 30%（11/21）
Google Cloud 11 月 21 日发布与 Vodafone 捷克合写的案例：Vodafone 用 Gemini 驱动的数据工程智能体（位于 BigQuery pipelines 与 Dataform 内），在 Dataform 中把 2,000–3,000 行的 BigQuery 存储过程迁移为模块化 Dataform 管线。智能体把代码拆为可并行的独立步骤，识别表间依赖，并用 BigQuery 物化视图缓存中间表；Vodafone 称新管线执行时间减半、成本降低 30%、迁移时间比人工方式减少 90%，迁移后的存储过程与原有逻辑 1:1 等价。案例也记录了一个教训：并行化会抵消 BigQuery 对基础表的缓存、导致成本上升，改用物化视图恢复缓存后才拿到 30% 的成本下降。Vodafone 计划把这一做法推广到罗马尼亚、爱尔兰、德国与英国市场，建立 Dataform 模板库，并迁移 SAS 代码、BTEQ 脚本与 MicroStrategy 工作负载。上述数字为企业自述，未提供独立基准与工作负载规模。
- [Google Cloud 官方博客（11/21）](https://cloud.google.com/blog/products/data-analytics/vodafone-cuts-data-pipeline-costs-30-via-data-engineeringagent/)

### 5. Databricks Genie Code 批量迁移仪表盘正式可用（11/19，补录）
Databricks 11 月 19 日在官方博客宣布，Genie Code 的 /importBI 批量迁移正式可用：把命令指向 Unity Catalog volume 中的一个目录，即可一次把整文件夹的 Tableau 与 Power BI 报表转为 AI/BI 仪表盘，不再逐份迁移。支持 .twb、.twbx、.tds、.tdsx、.pbit 与 .tmdl 文件；迁移 agent 自动把 Tableau workbook 与其数据源文件配对，配对不明时向用户确认；每份报告经过规划、语义层评审、度量视图创建、仪表盘构建与验证，各自作为后台作业运行，状态卡显示 Queued、Running 或 Completed；也可直接用自然语言下达迁移请求，或点名迁移个别文件。
- [Databricks 官方博客（11/19）](https://www.databricks.com/blog/bulk-migrate-your-dashboards-aibi-genie-code)

### 6. 戴尔发布 Agentic Data Gateway，为智能体提供统一治理的数据入口（11/16，补录）
戴尔 11 月 16 日在 SC26 上宣布 Dell AI Factory with NVIDIA 的一批更新，其中 Dell AI Data Platform 新增 Agentic Data Gateway：为每个智能体提供一条受治理的企业数据与上下文访问路径，背后由 MCP 服务器支撑，团队一次接入后无需为每个连接重写；戴尔称内部测试显示复用上下文使 token 消耗最多降低 76%、答案准确率从 60% 升至 94%（脚注说明测试基于 20 道题、6 类工作负载的合成收费站运营语料）。同批更新还包括混合数据管线编排（管线在数据所在位置运行）、与 LangChain、OpenAI、Codex、Unstructured.io 的集成，以及 Storage Intelligence 与 Data Intelligence。Dell AI Data Platform 的更新自 2026 年 12 月起可用。
- [Business Wire 通稿（11/16）](https://www.businesswire.com/news/home/20261116099303/en/Dell-Technologies-Delivers-the-Trusted-Data-and-AI-Infrastructure-Foundation-Needed-to-Scale-Agentic-Enterprise-AI)

## 开源项目

### 7. DB-GPT v0.8.3 发布（11/17，补录）
开源数据智能体框架 DB-GPT 11 月 17 日发布 v0.8.3：新增证据校验与报告恢复改进、结构化可追溯的数据分析报告、仪表盘工作区（Next.js 16 工具链升级）、Keenable Search MCP 连接器模板、LLM wiki 索引与 agent 可观测追踪；修复包括 agent 工具调用与报告生成加固、路径遍历与 SQL 注入漏洞修补、技能上传与知识空间权限收紧等。
- [DB-GPT GitHub Releases（11/17）](https://github.com/eosphoros-ai/DB-GPT/releases/tag/v0.8.3)

## 论文 / arXiv

### 8. GenSPARQL：SPARQL 的生成式扩展，让 LLM 在查询求值时生成值（11/20）
GenSPARQL: A Generative Extension of SPARQL for Incomplete Knowledge Graphs（arXiv:2611.26062，11 月 19 日提交，11 月 20 日上线，作者 Jingcheng Wu、Yi Wang、Hongkuan Zhou、Steffen Staab、Bo Xiong）为 SPARQL 1.1 增加生成式扩展：新增 GENOP 算子，在查询求值过程中把 LLM 生成的值绑定到查询变量；相似度连接把 LLM 生成的名称映射到知识图谱中的实体；查询规划器仅对其他图模式与过滤器选出的绑定调用 LLM。在三模型评估中，嵌入相似度映射了 LLM 提及实体的 83%，仅出现一处错误匹配。
- [arXiv:2611.26062](https://arxiv.org/abs/2611.26062)

本期检索范围内，Anthropic 11 月 20 日在纳斯达克上市（36 氪等报道，IPO 募资约 813 亿美元、另有 260 亿美元私募配售，首日收盘市值 1.27 万亿美元）与数据工作无直接关联，未收录；Google 11 月 22 日介绍 Duplex 接入 Gemini App 的 Tasks、可代用户致电商家，属通用智能体能力，与数据工作无直接关联，未收录；蚂蚁 OceanBase 团队 11 月 20 日开源跨对话 Agent 记忆服务 PowerContext，属通用智能体记忆基础设施，未收录；ThoughtSpot 26.11 版本（含 Spotter on Liveboards GA 等）仍在官方文档“即将推出”页，未确认已发布，未收录。国内大厂（阿里云、火山引擎、腾讯云、百度智能云、网易智企、华为云、京东云）与国内独立厂商（Aloudata、AskTable、数花智算、数势科技、帆软、思迈特、观远数据、Kyligence、衡石科技）当日均无数据代理相关的新发布；中文媒体 36 氪、机器之心、量子位、InfoQ 当日均无数据智能体直接相关的新内容；WrenAI、Chat2DB、Vanna、Apache Gravitino 等开源项目当日无新 Release；Cube 更新日志最新仍为 11 月 20 日的 Cube Apps；arXiv 周末无新列表（最新为 11 月 20 日）；Hugging Face Papers 11 月 22 日日榜前列无与数据代理直接相关的论文；Snowflake、Tableau、Hex、Microsoft、OpenAI 当日无可核实的新发布；Databricks 11 月 19 日的 Genie Migrate for Serverless 与 11 月 20 日的 Genie Agents MCP 工具 GA 已分别于 11 月 18 日、11 月 21 日两期收录，本期不再重复。

## 今日回顾

AWS 更新 AWS Quick，对话建流程、多智能体协同作答；Google Cloud 发布数据智能体模拟器与 Managed Airflow 智能体，Vodafone 用数据工程智能体把管线成本降低 30%；Databricks Genie Code 批量迁移仪表盘正式可用；戴尔发布 Agentic Data Gateway；DB-GPT 发布 v0.8.3；arXiv 上线 GenSPARQL。
