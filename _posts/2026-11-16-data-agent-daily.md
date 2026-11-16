---
layout: post
title: "Data Agent Daily — 2026-11-16"
author: dad
date: 2026-11-16
image: "assets/images/covers/2026-11-16.svg"
description: "Salesforce 在 11 月 16 日宣布 Tableau Studio 在韩国上线：Tableau Agent 用自然语言生成可视化、计算与仪表盘，云版 11 月 17 日、服务器版 11 月 19 日可用。"
categories: ["Data Agent Daily"]
tags: ["data-agent", "news"]
comments: false
---

## 今日速览

- Salesforce 在 11 月 16 日宣布 Tableau Studio 在韩国上线：Tableau Agent 用自然语言生成可视化、计算与仪表盘，云版 11 月 17 日、服务器版 11 月 19 日可用。
- 腾讯云在 11 月 16 日发布首个数据库 Agent 平台 TencentDB Agent：覆盖 MySQL、Redis、MongoDB 等 14 款数据库，主动发现问题、自主诊断并交付结论。
- DataRobot 与戴尔在 11 月 16 日宣布合作：把 Agent Workforce Platform 与 Dell AI Factory 结合，向中东企业提供主权智能体部署。
- dbt 在 11 月 release notes 中列出远程 dbt MCP 服务器的新进展：可接 Gemini Enterprise、已上架 Databricks Marketplace，只读用户可用共享凭证通过 MCP 查询指标。
- Anthropic 在 11 月 10 日推出 Claude Sheets、Claude Whiteboards 与 Claude Data：Sheets 与 Whiteboards 为 Beta 版，Data（原 Dashboards）正式可用；Claude Meetings 于 11 月 12 日进入 Beta。
- Google 在 11 月 12 日发布 Gemini 4 Hydrogen：面向日常编码与智能体工作流，100 万 token 上下文，API 定价为每百万输入 tokens 1.50 美元、输出 7.50 美元。
- arXiv 11 月 13 日上线 LuthorSQL：7B 非自回归 text-to-SQL 模型作智能体的快速前置判断，BIRD 隐藏测试集执行准确率 68.03%，与 Claude Opus 5.5 级联后 API 成本降低 33.3%。
- arXiv 11 月 13 日上线 Bridge：数据库驱动的 text-to-SQL 交互式消歧框架，在 BIRD-dev 上执行准确率较最强基线高 11.60%。
- arXiv 11 月 13 日上线 MEM-SQL：用历史 SQL 记忆增强 text-to-SQL，平均执行准确率从 37.1% 升至 50.0%，输入 tokens 减少 76.6%。
- arXiv 11 月 11 日上线 SimRec：用强化学习训练推荐智能体的完整交互策略，Qwen3-4B 智能体在 ESCI 上 NDCG@100 从 32.23% 升至 35.42%。

## 公司发布 / 官方博客

### 1. Salesforce 在韩国上线 Tableau Studio：Tableau Agent 用自然语言做分析，云版 11 月 17 日、服务器版 11 月 19 日可用（11/16）
Salesforce 在 11 月 16 日宣布在韩国推出 Tableau Studio：用户用自然语言向 Tableau Agent 下达分析任务，Agent 依据当前工作簿所连数据生成与修改可视化、计算、工作表与仪表盘。配套的 Tableau Skills 是可复用的分析指南库，覆盖数据质量检查、仪表盘设计、计算编写与调试、性能分析等任务，首批 50 多个 Skills 经 Tableau Exchange 分发，来源包括 Salesforce 自身与获批合作伙伴；Tableau Data Apps 可把分析结果做成面向具体业务用途的交互式应用。Tableau 官方新功能页称 Studio 将于 2026 年 11 月在 Tableau Cloud 与 Tableau Server 全面可用，完整体验需要持有 Creator 许可证的 Tableau+、Cloud+ 或 Server+ 版本，也可在 Tableau Cloud 试用版中体验。同批 2026 年 11 月新功能还包括 Tableau Data Apps 全面可用、Tableau Next 的 Q&A Calibration 批量回归测试、Metrics MCP（Claude 等外部智能体可直接查询 Tableau Next 的受治理指标）、Headless Auto Calibration（经 MCP 自动诊断并批量修正语义模型）与 Support for Agentic Flows。
- [Chosun Biz 报道（11/16）](https://biz.chosun.com/en/en-it/2026/11/16/3U76D6KLBVCGBBYF2ZD6PI6BDY/)
- [Tableau 官方 2026 年 11 月新功能页](https://www.tableau.com/products/new-features)

### 2. 腾讯云发布首个数据库 Agent 平台 TencentDB Agent：主动诊断、自主执行，覆盖 14 款数据库（11/16）
腾讯云在 11 月 16 日正式推出首个数据库 Agent 平台 TencentDB Agent。按发布方说法，它不是问答助手，而是能主动发现问题、自主完成诊断、交付确定性结论的生产级 AI Agent：DBA 十余年的一线经验被封装为可调用、可组合、可复用的 Skill。平台覆盖 MySQL、Redis、MongoDB 等 14 款数据库，慢 SQL 分析、容量预测、HA 切换分析由一个 Agent 完成；「腾讯云数据库专家」同步上线 WorkBuddy 专家入口。发布方给出的演示为：对广州地域 41 个 MySQL 实例完成巡检，输出首屏风险 5 条（P0–P2）。计费采用积分制：体验版免费开通，企业版按包年包月计费；网页、企业微信、钉钉、飞书均可接入。11 月 9 日腾讯云全球数字生态大会上已提及 TencentDB Agent，本次为正式发布。
- [腾讯新闻（11/16 11:30）](https://news.qq.com/rain/a/20261116A06M1B00)
- [腾讯云官方产品文档](https://cloud.tencent.com/document/product/1813/130681)

### 3. DataRobot 与戴尔合作，向中东企业提供主权智能体部署（11/16）
DataRobot 在 11 月 16 日宣布与戴尔科技合作，帮助中东企业在主权、本机、私有云与混合云环境内部署智能体，同时保有对 AI 运行位置、智能体治理方式与成本的控制。合作把 Dell AI Factory with NVIDIA 与 DataRobot Agent Workforce Platform 结合，DataRobot 的新蓝图可经 Dell Automation Platform 获取；发布方称初期聚焦金融服务与物流两个行业。DataRobot 援引的研究称，阿联酋与沙特各有 38% 的组织已在生产环境运行智能体 AI；其援引的 IDC 研究称 96% 的组织表示部署生成式 AI 的成本高于预期。DataRobot 以 AI 赞助商身份参加了在迪拜举行的 Dell Technologies Forum，平台在会上展示。已披露的客户为阿联酋电信 Etisalat UAE：双方在 10 月 14 日宣布多年协议，由 Etisalat 在自有数据中心托管 Agent Workforce Platform。
- [Al Bawaba 新闻稿转载（11/16）](https://www.albawaba.com/business/pr/datarobot-collaborates-dell-technologies-1641433?overridden_route_name=entity.node.canonical&base_route_name=entity.node.canonical&page_manager_page=node_view&page_manager_page_variant=node_view-panels_variant-0&page_manager_page_variant_weight=0)

### 4. dbt 11 月 release notes：远程 dbt MCP 服务器接 Gemini Enterprise、上架 Databricks Marketplace（11 月）
dbt 在 11 月 release notes 中列出远程 dbt MCP 服务器的一批新进展：可连接 Gemini Enterprise，用自然语言探索 dbt 项目；远程 dbt MCP 服务器已上架 Databricks Marketplace，可从 Databricks 使用 dbt 项目；只读用户可用管理员配置的共享分析凭证通过远程 MCP 查询指标；远程 MCP 现按每次工具调用检查其针对的项目、环境、任务或运行的权限，服务 token 可用 `text_to_sql` 生成 SQL，但执行 SQL 仍需 OAuth 或个人访问 token。同批还包括 dbt Wizard 可经 Databricks 使用 Claude Haiku 5.5 与 Claude Sonnet 5.5，以及当 AI 模型供应商（OpenAI、Anthropic 或 Fireworks）中断时自动切换至 AWS Bedrock。
- [dbt 官方 release notes](https://docs.getdbt.com/docs/dbt-versions/release-notes)

### 5. Anthropic 推出 Claude Sheets、Claude Whiteboards 与 Claude Data，Meetings 进入 Beta（11/10，补录）
Anthropic 在 11 月 10 日推出 Claude Sheets、Claude Whiteboards 与 Claude Data，并于 11 月 12 日让 Claude Meetings 进入 Beta。本期此前未收录，现补录。Claude Sheets 为 Beta 版：Claude 按一句话请求生成带多标签页、公式、格式与下拉菜单的电子表格，团队可与 Claude 共同编辑，导出为 .xlsx 或 CSV；Claude Whiteboards 为 Beta 版：把讨论整理为带时间线、负责人与日期的共享白板；Claude Data 为原 Claude Dashboards 的新名，现已正式可用：连接 Snowflake、BigQuery、Redshift、Salesforce 等数据源后生成仪表盘、数据故事与旁白视频，以经认证的指标定义作答，认证查询与实时分享仍为 Beta。Sheets、Whiteboards 与 Data 均面向全部付费计划，在网页、桌面与移动端可用；Team 计划默认全部开启，Enterprise 计划中 Sheets 与 Whiteboards 默认关闭、Claude Data 于 11 月 19 日默认开启。Claude Meetings 为 Beta 版，面向 Team 与 Enterprise 计划，首批仅支持 Google Meet，Claude 以可见参会者身份加入会议、做笔记并更新团队文档。同期还推出交互式连接器（基于 MCP Apps）：Adobe、Atlassian、Box、HubSpot 等合作方应用可在 Claude 内直接打开使用；Sheets 一侧的合作方包括 Airtable、Asana、monday.com 与 Smartsheet。
- [CocoLoop 报道（11/11）](https://news.cocoloop.cn/en/2026/11/claude-sheets-whiteboards-beta/)

### 6. Google 发布 Gemini 4 Hydrogen：面向日常编码与智能体工作流的快速模型（11/12，补录）
Google 在 11 月 12 日发布 Gemini 4 Hydrogen，定位为 Gemini 4 家族中面向日常编码与智能体工作流的快速执行模型，本期此前未收录，现补录。模型支持 100 万 token 上下文（输入与输出合计），最长可输出 100 万 tokens；API 定价在整个上下文窗口内统一为每百万输入 tokens 1.50 美元、每百万输出 tokens 7.50 美元。Google 称，默认 high 思考级别下 Hydrogen 在 Artificial Analysis 智能指数上得 51 分，高于 Argon 的 50 分，最高 xhigh 级别达 54 分；在 Agent Arena 上排名第 5；与 Gemini 3.8 Flash 相比，默认设置下速度快 2.5 倍，智能体越权行为减少最高 81%、服务不足减少最高 79%。模型在发布当日即向 Gemini API、Google AI Studio、Gemini for business、Gemini 应用、Google Search 与 Google Antigravity（付费 Pro 与 Ultra 用户）全球推出；11 月 13 日起又在 GitHub Copilot 中全面可用。
- [Google 官方博客（11/12）](https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-4-hydrogen/)

## 开源项目

Cube Core 自 11 月 15 日 v1.8.26 后无新版本（GitHub Releases 已核实），当日无实质 Release；NVIDIA auto-ontology 无新 Release（星标增长不作新闻）；WrenAI、DB-GPT、Chat2DB、DocETL、Apache Gravitino 等监测名单内开源项目当日无实质 Release。

## 论文 / arXiv

### 7. LuthorSQL：7B 非自回归 text-to-SQL 模型作智能体的快速前置判断，BIRD 隐藏测试集 68.03%（11/13）
LuthorSQL（arXiv:2611.17780，11 月 13 日提交）针对用工具查库的前沿 LLM 智能体速度慢、成本高、且把敏感查询暴露给外部 API 的问题，提出一个 7B 非自回归 text-to-SQL 模型作快速 System 1 前置判断，仅在不确定时升级给较慢的 LLM 智能体（System 2）。模型单次前向传播预测有界文法上的槽位分数，编译并运行最多 32 个候选查询计划，再以训练好的验证器选出答案。单独使用时，LuthorSQL 在 BIRD 隐藏测试集上执行准确率为 68.03%，单块 GPU 上每问题 0.84 秒，8 位量化权重下 9 GB 显存即可运行；零样本迁移至 Snowflake、BigQuery、MySQL、PostgreSQL 与 DuckDB 时，准确率与其原生 SQLite 水平相差在 3.1 个百分点以内。与 Claude Opus 5.5 的预注册置信级联实验中，LuthorSQL 在本地回答了近半数问题，在同等准确率下 API 成本降低 33.3%。论文另做污染探测：Opus 在未见 schema 时仍能逐字复现 48–92% 的公开基准标准查询，但在重命名 schema 与截止后数据库上，其工具辅助准确率保持在 95.6–97.4%。
- [arXiv:2611.17780](https://arxiv.org/abs/2611.17780)

### 8. Bridge：数据库驱动的 text-to-SQL 交互式消歧，BIRD-dev 执行准确率较最强基线高 11.60%（11/13）
Bridge（arXiv:2611.17770，11 月 13 日提交）针对 text-to-SQL 中提问欠明确、可对应多个 SQL 解读的问题，提出数据库驱动的消歧框架：离线用数据库自身的信号找出可能存在歧义的列对，经 LLM 验证后建成列歧义图；在线以上一轮错误 SQL 中提到的列与值为锚点，从列歧义图与离线值相似度索引中检索候选，再剪枝整合进后续歧义检测。论文称，在不使用基准提供的 evidence 的 BIRD-dev 上，同等 LLM 成本下 Bridge 的执行准确率较最强基线高 11.60%，最终 SQL 的列使用召回率与精确率分别提升 5.25 与 12.37 个百分点。
- [arXiv:2611.17770](https://arxiv.org/abs/2611.17770)

### 9. MEM-SQL：用历史 SQL 记忆增强 text-to-SQL，执行准确率 37.1% 升至 50.0%（11/13）
MEM-SQL（arXiv:2611.18338，11 月 13 日提交）指出现有基准按问题独立评测，忽略了同一数据库上的历史查询可为新问题提供连接与计算；论文引入 HARE（History-AwaRe Text-to-SQL Benchmark），含 1,600 个请求，源自 823 条已验证查询、覆盖 4 个数据集，标注每个请求保留与改动的部分。方法 MEM-SQL 存储整查询模板、可复用 SQL 片段与领域概念到 schema 元素的映射，按层取用，仅当某层全部需求匹配度达标才使用该层；配合按需 schema 链接（OSL），仅在无层可用或生成器判定证据不足时才查 schema。在 6 个语言模型上，MEM-SQL 的平均执行准确率从无历史的直接生成的 37.1% 升至 50.0%，输入 tokens 平均减少 76.6%、延迟降低 68.8%。论文同时指出，复用多个已验证查询的请求仍是瓶颈，准确率从 56.7% 跌至 29.7%。该论文亦登上 Hugging Face Papers 11 月 16 日日榜。
- [arXiv:2611.18338](https://arxiv.org/abs/2611.18338)
- [Hugging Face Papers 日榜（11/16）](https://huggingface.co/papers)

### 10. SimRec：用强化学习训练推荐智能体的完整交互策略（11/11，补录）
SimRec（arXiv:2611.15426，11 月 11 日提交）提出训练工具集成型推荐智能体完整交互策略的强化学习框架：以任务为锚的用户模拟器对每次推荐给出反馈，模拟器可为外部 LLM 或推荐器自身的自博弈。实验称，在 ESCI 上，Qwen3-4B 智能体的 NDCG@100 从 32.23% 升至 35.42%；在 Amazon C4 上从 22.94% 升至 24.72%，优于更大底座的无训练智能体与任务对齐基线。
- [arXiv:2611.15426](https://arxiv.org/abs/2611.15426)

## 新闻网站

Tableau Studio 韩国上线由 Chosun Biz 于 11 月 16 日报道（已并入第 1 条）；腾讯云 TencentDB Agent 由腾讯新闻于 11 月 16 日报道（已并入第 2 条）；除此之外，新闻网站当日未见其他可核实的数据智能体新内容。

## 社交媒体

Instagram 当日出现第三方账号 @aicoreupdates 发布的 Tableau Studio 解说短视频（11/16），介绍其定价层级，属评论而非新闻；Tableau 官方账号当日无新帖；中文媒体层除腾讯新闻的 TencentDB Agent 报道外未见可核实的新内容；其余社交媒体当日未见可核实的数据智能体新内容。
- [Instagram 第三方解说短视频（11/16）](https://www.instagram.com/reel/Dfy8JvWjqIC/)

本期检索范围内，监测名单内其余厂商、研究团队与开源项目在过去 24 小时内未见可核实的新动态；arXiv cs.DB 11 月 16 日新论文中其余 3 篇与数据代理无直接关系，cs.IR 新论文中无与数据代理直接相关者；Spider 2.0、BIRD、DABstep、DAComp 等评测基准当日无原作者团队新动态；CB Insights「Team of Agents」今日重现的转载实为 2025 年 6 月的旧新闻稿，未收录。

## 今日回顾

Salesforce 在 11 月 16 日宣布 Tableau Studio 在韩国上线，Tableau Agent 用自然语言生成可视化、计算与仪表盘，云版 11 月 17 日、服务器版 11 月 19 日可用；腾讯云同日发布首个数据库 Agent 平台 TencentDB Agent，覆盖 14 款数据库，主动发现问题、自主诊断并交付结论；DataRobot 与戴尔同日宣布合作，向中东企业提供主权智能体部署；dbt 在 11 月 release notes 中列出远程 dbt MCP 服务器的新进展；Anthropic 在 11 月 10 日推出 Claude Sheets、Claude Whiteboards 与 Claude Data，Meetings 于 11 月 12 日进入 Beta；Google 在 11 月 12 日发布 Gemini 4 Hydrogen；arXiv 11 月 13 日上线 LuthorSQL、Bridge 与 MEM-SQL 三篇 text-to-SQL 论文，11 月 11 日上线推荐智能体强化学习框架 SimRec；Cube Core 当日无新版本。
