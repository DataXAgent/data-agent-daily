---
layout: post
title: "Data Agent Daily — 2026-11-23"
author: dad
date: 2026-11-23
image: "assets/images/covers/2026-11-23.svg"
description: "Sigma Assistant 11 月 22 日上线可追溯答案：回答中的每个数字可追溯到计算过程与数据血缘，全体客户默认开启；Snowflake Cortex Agent SDK 正式 GA，微软 Fabric 数据智能体的高级 NL2SQL 与 DAX 转正。"
categories: ["Data Agent Daily"]
tags: ["data-agent", "news"]
comments: false
---

## 今日速览

- Sigma Assistant 11 月 22 日上线可追溯答案，回答中的每个数字可追溯到计算过程与数据血缘，全体客户默认开启。
- Sigma 11 月 20 日更新日志新增语音输入与工作簿 PDF 附件，语音识别在浏览器本地完成。
- Snowflake Cortex Agent SDK v1.0.0 于 11 月 18 日正式 GA，可在自有应用中运行 Cortex Agent 与 Cortex Code。
- 微软 11 月 17 日发布 Fabric 11 月功能汇总，数据智能体的高级 NL2SQL 与高级 DAX 转正，标准运行时完成 11 月 2–10 日推送。
- dbt Labs 11 月 17 日发布 11 月更新，Wizard Desktop 进入公开 Beta，dbt Charts 进 Claude 与 ChatGPT。
- Oracle 发布 Analytics 11 月更新，Deep Insights Agents 支持多数据集多阶段调查，Data Flow AI Assistant 用自然语言搭建数据流。
- Palantir 11 月 19 日在 Insight 内推出 AIP Insight（beta），用自然语言描述探索内容、由 AIP 搭建 workbook。
- Hex 11 月 18 日刊登 Underdog 客座文章，200 多名员工通过 Hex agent 进行了 1 万多次分析对话，以版本化 dbt 项目为共享上下文层。
- Alteryx 11 月 18 日更新 Agent Studio 发布说明，Alteryx Agents 新增数据集描述，MCP 服务器新增资产摘要与关键词+语义混合搜索。
- 印度数据安全初创 Matters.AI 11 月 23 日宣布完成约 1,200 万美元 Pre-A 轮，融资将用于数据血缘与自主调查研发。
- 火山引擎 11 月 20 日披露与中油共享的智能体合作，内部已运行 18 个智能体，数据型智能体“慧分析”使报告周期缩短 80%。
- 微软 11 月 17 日宣布 Atlan 为首选数据治理合作伙伴，OneLake 目录成为跨 estate 治理的统一基础。
- 微软与甲骨文 11 月 17 日在 Ignite 上宣布一批集成，Foundry agent 可通过托管 MCP 服务器访问 Oracle 数据库。
- arXiv 11 月 23 日上线 AskWise：用执行结果引导文本转 SQL 的澄清提问，只在选项确实改变答案时才提问。
- arXiv 11 月 23 日上线 Decision Columns：用可解释的决策列嵌入做实体匹配与检索，相似度可按问题逐项分解。
- arXiv 11 月 23 日上线 Federated KPI Aggregation：站点 agent 协同 OLAP 汇总粒度，在本地隐私规则下保留全部贡献。

## 公司发布 / 官方博客

### 1. Sigma Assistant 上线可追溯答案，每个数字可追溯到计算与血缘（11/22）

Sigma 11 月 22 日宣布，Sigma Assistant 的回答现已可追溯：答案中的每个数字都链接到产生它的计算过程与数据血缘，用户可看到数字如何得出。悬停在带下划线的数字上，可看到来源表、过滤器、计算方式与匹配记录；数字来自已定义度量时，Sigma Assistant 会标注为度量并展示定义与公式。点击数字可在侧栏打开完整分析：来源、过滤器、连接与并集以自然语言呈现，并附完整结果表，可进一步查看 SQL 与血缘（Show lineage 映射从源仓库表或数据模型到结果的完整链路，包括过滤器应用位置与新增计算）。悬停后点“Ask in chat”可就该数字继续追问，或分析其他维度。Sigma 称答案遵循现有仓库权限，包括行级安全与列掩码；该功能对全体客户默认开启，需配置 AI 提供方并拥有“Use Assistant”权限。博客同时说明，数字追溯仅在直接与 Sigma Assistant 对话时可用，通过 Sigma Assistant 内选择器进入的仓库 agent 对话中不可用。
- [Sigma 官方博客（11/22）](https://www.sigmacomputing.com/blog/sigma-assistant-traceable-answers)

### 2. Sigma 11 月 20 日更新：语音输入与工作簿 PDF 附件（11/20，补录）

Sigma 11 月 20 日更新日志新增 Sigma Assistant 与 agent 的语音输入：在提示栏点 Dictate，说出请求后点 Stop dictating，可在发送前检查并编辑转写文本。语音识别使用浏览器的语音识别能力，需支持的浏览器与麦克风权限，Sigma 不接收音频，只收到发送的提示文本。同批更新还包括工作簿中 Assistant 构建模式支持 PDF 附件、徽章 API 端点，以及嵌入用户交互功能 GA；以 BigQuery 或 Gemini 为 AI 提供方时，模型改为 Gemini Flash 3.8。
- [Sigma 更新日志（11/20）](https://help.sigmacomputing.com/changelog/2026-11-20)

### 3. Snowflake Cortex Agent SDK v1.0.0 正式 GA（11/18，补录）

Snowflake 官方发布说明记录，Cortex Agent SDK 于 11 月 18 日正式 GA，Python 与 TypeScript 均提供 v1.0.0。SDK 用于构建在自有应用中运行 Cortex Agent 与 Cortex Code 的程序，可流式返回响应、维护对话与线程、重连长任务。该 SDK 于 10 月 13 日进入公开预览，本次为正式可用节点。
- [Snowflake 官方发布说明（11/18）](https://docs.snowflake.com/en/release-notes/all-release-notes)

### 4. 微软发布 Fabric 11 月功能汇总，数据智能体高级 NL2SQL 与 DAX 转正（11/17，补录）

微软 11 月 17 日发布 Fabric 11 月功能汇总，其中数据智能体（Data Agents）的 Advanced NL2SQL 与 Advanced DAX 生成正式 GA。两项能力于 10 月 19 日宣布 GA，11 月 2 日起推送至标准运行时、预计 11 月 10 日完成，同时标准运行时改用 GPT-5.6 Terra：高级 NL2SQL 用子工具探索 schema、测试连接、查找过滤值、修改已批准示例查询、提出澄清问题并检查推理步骤；高级 DAX 生成用多步推理检查模型元数据、消除歧义、复核中间结果并优化查询。微软引用的内部测试显示，SQL 生成准确率从 78.8% 升至 90.9%、P95 延迟从 46.8 秒降至 32.9 秒，DAX 准确率从 89.15% 升至 91.86%、P95 延迟从 97.5 秒降至 34.7 秒（内部测试结果，未提供独立第三方验证）。同批预览内容包括高级 NL2SQL 的日期时间推理改进、SQL 源的多主题指导文件与 schema 对象描述；标准运行时下数据智能体最多返回 1,000 行（预览）。汇总同时记录，Fabric 数据智能体以自定义工具接入 Microsoft Foundry 的旧集成于 11 月 6 日停止支持，需迁移至 Fabric IQ。
- [Microsoft Fabric 社区博客（11/17）](https://community.fabric.microsoft.com/blog/fbc_fabricupdatesblogs/fabric-november-2026-feature-summary/5414311)

### 5. dbt Labs 发布 11 月更新：Wizard Desktop 公开 Beta，dbt Charts 进 Claude 与 ChatGPT（11/17，补录）

dbt Labs 11 月 17 日发布 11 月更新：dbt Wizard Desktop 进入公开 Beta，支持 macOS、Windows 与 Linux，可并行运行多个任务，每个任务在 git 与仓库中隔离，合并前可用可视化 DAG 差异复核每处改动。dbt Charts 进入 Claude 与 ChatGPT（Beta），通过 MCP 连接器（dbtcharts.com/mcp）在聊天应用内直接对话 boards 与仓库，按用户自身权限执行；dbt 称基准测试中 dbt Charts 生成的仪表盘质量更高、token 用量比从头构建少约 20–50%。一键式 dbt MCP 集成新上架 Cursor 与 Databricks 市场（此前已在 Claude 与 ChatGPT 上架，Snowflake、Google Gemini 与 AWS Kiro 正在推进）。同批内容还包括 dbt v2 本地单元测试（Alpha，SQL 转 DuckDB、无需仓库往返）、批量测试 GA（dbt 内部测试称运行时间减少 40%、仓库查询减少 65%），以及 dbt State 新免费计划（自托管与 Developer/Starter 计划每月 1,000 DATT，Enterprise 与 Enterprise+ 每月 2,000 DATT）。
- [dbt Labs 官方博客（11/17）](https://www.getdbt.com/blog/whats-new-in-dbt-november-2026)

### 6. Oracle Analytics 11 月更新：Deep Insights Agents 与 Data Flow AI Assistant（11 月，补录）

Oracle 发布 Analytics Cloud 11 月更新，AI 方面两项内容为重点：Deep Insights Agents 支持需要多阶段分析的业务调查，agent 可跨多个数据集工作，采纳业务指令与 PDF 参考文档，以表格、图表与来源呈现发现；Instant 模式处理聚焦问题，高推理模式处理更广泛的调查，用户可复核 agent 的活动、保存回答共享，并下载执行记录供技术复核。Data Flow AI Assistant 帮助用户用日常语言构建与丰富数据流，可按指定条件添加过滤步骤、在表达式编辑器中为新列生成公式，应用前可检查新增过滤器与生成的公式。同批更新还包括工作簿过滤器值范围粘贴与 trellis 图独立坐标轴刻度。
- [Oracle Analytics 官方博客（11 月）](https://blogs.oracle.com/analytics/explore-the-oracle-analytics-november-2026-update)

### 7. Palantir 在 Insight 内推出 AIP Insight（beta），自然语言描述即建 workbook（11/19，补录）

Palantir 11 月 19 日在 Foundry 公告页宣布，AIP Insight 已在 Insight 内推出（beta），面向全部已启用 AIP 的 enrollment 可用。用户用自然语言描述想探索的内容，AIP 帮助查找相关数据并搭建 workbook 来回答问题；agent 创建的分析步骤在 workbook 中可见、可编辑，用户可检查结果如何产生并自行修改步骤。Beta 阶段可创建与编辑分析路径，表、图与地图布局仍需手动配置，部分 Insight 功能（如接口与派生属性）暂不受 copilot 支持。
- [Palantir Foundry 公告页（11/19）](https://www.palantir.com/docs/foundry/announcements)

### 8. Hex 刊登 Underdog 客座文章：1 万多次分析对话背后的 dbt 上下文层（11/18，补录）

Hex 11 月 18 日刊登体育博彩公司 Underdog 的客座文章：200 多名员工通过 Hex agent 在 Hex、Slack 与 Claude 中进行了 1 万多次分析对话，团队把版本化的 dbt 项目作为共享上下文层，而非另建 AI 专属知识库。dbt 模型定义数据与关系，语义模型定义可信度量与可连接关系，指南（guide）承载不适合塞进指标或维度的判断、注意事项与反向知识（如员工账号应排除在客户分析外、历史问题应使用日快照而非当前状态表）。Hex 会跨对话识别反复出现的歧义并聚合成改进建议，Claude 再通过 Hex CLI 把建议落回 dbt 仓库并提交 PR。团队用 evals 从正确性、一致性、路径（是否用了正确的上下文）三个维度检验 agent 对上下文的使用，目前为临时运行，下一步计划接入 CI。
- [Hex 官方博客（11/18）](https://hex.tech/blog/how-underdog-powers-conversational-analytics-with-dbt-and-hex/)

### 9. Alteryx Agent Studio 发布说明：数据集描述与 MCP 资产摘要（11/18，补录）

Alteryx 11 月 18 日更新 Agent Studio 发布说明：Alteryx Agents 现为每个数据集显示描述，出现在选择数据集对话框的描述列、选中数据集的悬停提示，以及聊天中 Agent Assets 卡片上，AI 生成的描述带有标记；Agents 标签页的 Used Datasets 列改名为 Agent Assets。Alteryx MCP 服务器方面，展示资产卡片的 MCP 客户端现为每个资产显示 AI 生成的摘要（带标记），资产搜索改为关键词与语义混合搜索，agent 可按名称与用途查找资产。
- [Alteryx Agent Studio 发布说明（11/18）](https://help.alteryx.com/aac/en/release-notes/release-notes-for-agent-studio.html)

## 新闻网站

### 10. 印度数据安全初创 Matters.AI 完成约 1,200 万美元 Pre-A 轮（11/23）

Tech in Asia 11 月 23 日报道，总部位于班加罗尔的数据安全初创 Matters.AI 完成约 1,200 万美元 Pre-A 轮，由 Tanglin Venture Partners 领投，IIFL Fintech Fund、Piper Serica 旗下 Bharat Tech Fund、Foster Ventures 与 Tetration Ventures 参投，现有投资方 Kalaari Capital 与 Endiya Partners 跟投；本轮后公司累计融资约 1,825 万美元。Matters.AI 称其软件追踪企业系统中的敏感数据流向（包括共享给生成式 AI 工具的数据），已有 50 多家机构使用；融资将用于研发（包括数据血缘与自主调查）与北美销售团队建设。
- [Tech in Asia 报道（11/23）](https://www.techinasia.com/news/indian-data-security-startup-mattersai-raises-12m)

### 11. 火山引擎与中油共享共建三类智能体，数据型“慧分析”报告周期缩短 80%（11/20，补录）

火山引擎 11 月 20 日披露与中国石油集团共享运营公司（中油共享）的智能体合作细节：双方共建知识、数据、流程三类智能体，目前内部已运行 18 个智能体，覆盖财务、税务、法务、信息技术、客服、人力资源六大场景。知识型“享知道”平台沉淀 10 万多条知识条目，回答准确率超 90%；流程型“易报销”基于 HiAgent 搭建，出差申请效率提升 70%、填单操作减少 95%；数据型“慧分析”基于 DataAgent，报告生成周期缩短 80%、分析效率提升 70%。双方还搭建了低代码智能体开发运营中台，开展 4 期实战培训覆盖 200 多名员工、产出 39 个智能体原型。上述数字为厂商披露，未提供独立验证。
- [AGI Hunt 转述火山引擎微信公众号文章（11/20）](https://agihunt.info/p/1a1f7eb7d1d18a2ed89bb427dfc)

### 12. 微软宣布 Atlan 为首选数据治理合作伙伴，OneLake 目录成统一治理基础（11/17，补录）

微软 11 月 17 日宣布与 Atlan 的战略合作，称 Atlan 为其首选数据治理合作伙伴：OneLake 目录成为在整个数据 estate 内发现、治理与保护数据的统一基础，Purview 数据治理支持于 2027 年 11 月 12 日停止；OneLake 与 Fabric 客户可用 Atlan 把治理延伸至 OneLake 之外，Atlan 的 Migration Studio 承接 Purview 数据治理迁移、把已有元数据带入新环境。Atlan 的 Fabric 连接器把 lakehouse、仓库、语义模型与 Power BI 报告（含列级血缘）纳入 Atlan，agent 通过 Atlan 读取同一套经认证的定义与血缘。
- [Business Wire 通稿（11/17）](https://www.businesswire.com/news/home/20261117903447/en/Atlan-and-Microsoft-Collaborate-to-Extend-OneLake-Governance-Across-the-Data-Estate)

### 13. 微软与甲骨文在 Ignite 上宣布集成，Foundry agent 可经托管 MCP 访问 Oracle 数据库（11/17，补录）

微软与甲骨文 11 月 17 日在 Ignite 上宣布一批基于 Oracle AI Database@Azure 的集成：Oracle AI Database Excel 插件即日起可用，工作表直连 Oracle Database、用 Copilot 在表内分析；Azure Workload Center for Oracle 进入有限预览，把单个工作负载的架构、资源与依赖收进 Workload Virtual Instance 统一视图；开发者可在 Microsoft Foundry 中构建 agent，通过托管 MCP 服务器与 A2A 协议连接 Oracle AI Database（OCI 内或 Azure 内均可），访问限于已批准的 SQL 与 PL/SQL 操作、工具与预定义报告，并以 Microsoft Entra 认证与 Oracle Deep Data Security 执行权限控制、全部调用可审计。Oracle AI Database@Azure 现覆盖 33 个 Azure 区域。
- [微软 Azure 官方博客（11/17）](https://azure.microsoft.com/en-us/blog/microsoft-and-oracle-bring-agentic-ai-into-flow-of-enterprise-work/)

## 论文 / arXiv

### 14. AskWise：用执行结果引导文本转 SQL 的澄清提问（11/23 上线）

AskWise: Execution-Guided Clarification of Intent and Data in Text-to-SQL（arXiv:2611.27474，11 月 20 日提交，11 月 23 日上线，作者 Yuru Liang、Guangyinan Mei、Miles Fan）针对数据库提问中意图与数据歧义的澄清问题：执行候选查询的多种修复组合，只在两个执行结果仅在某一选项上不同、且给出不同答案时，才就该选项提问；一旦全部存活组合给出同一已知答案即返回答案。在 120 个销售任务上，该界限把每轮平均执行次数从 14.88 降至 13.80；在 AmbiQT 上，受控值交换在 1,206 个符合条件的案例中的 424 个里分开了参考查询；在 155 个抽样问题上，对两个数据库状态剪除同一模型候选使参考答案签名的召回率提升 8.71 个百分点（Doubao Lite）与 10.00 个百分点（GPT Sol）。
- [arXiv:2611.27474](https://arxiv.org/abs/2611.27474)

### 15. Decision Columns：可解释的决策列嵌入，用于实体匹配与检索（11/23 上线）

Decision Columns as an Index: Interpretable Embeddings for Explainable Entity Matching and Search（arXiv:2611.27910，11 月 20 日提交，11 月 23 日上线，作者 Aadharsh Kannan、Robert Bruckner、Philip A. Bernstein）提出用决策列构建可解释嵌入：每列存储一个决策模型对一个自然语言问题的校准答案（是、否、未说明），一条记录的嵌入即其在一组有序问题上的答案；相似度可精确分解为每个问题的贡献，新增问题可增加坐标而不改变已有坐标。在公开产品基准上，问题空间检索在检索后验证的实体匹配器中与稠密候选生成统计相当，同时为接受的匹配提供精确解释；由检索失败推导的问题使平均倒数排名提升两倍且无需重编码已有答案；单个小型神经网络可从已有稠密嵌入预测完整可解释向量，成本约为千分之五。
- [arXiv:2611.27910](https://arxiv.org/abs/2611.27910)

### 16. Federated KPI Aggregation：站点 agent 协同 OLAP 汇总粒度（11/23 上线）

Federated KPI Aggregation with Local Privacy Constraints and Coordinated OLAP Roll-Ups（arXiv:2611.26709，11 月 19 日提交，11 月 23 日上线，作者 Felix Härer）研究跨组织 KPI 分析：各站点在本地最小群组规则下发布 KPI，若各自独立执行抑制，合并 KPI 会缺失部分贡献；该方法在发布本地查询结果前协调 OLAP 粒度，选出全部站点接受的最不泛化公共汇总，站点 agent 协调当前能力与已批准的本地执行，隐私检查与聚合计算仍为确定性本地函数。四站点原型中，协调汇总保留了全部贡献，而独立抑制下仅保留 78.3%；能力变更实验显示，使用当前站点 agent 状态后候选检查与回复更少、且无不支持的请求。
- [arXiv:2611.26709](https://arxiv.org/abs/2611.26709)

本期检索范围内，开源项目当日无新 Release（WrenAI 最新仍为 11 月 10 日的 v0.18.0，DB-GPT v0.8.3 已于 11 月 22 日一期收录，Chat2DB、Vanna、Apache Gravitino、Alpha-SQL、ReFoRCE、DeepEye-SQL、LAMBDA、Data Interpreter、DeepAnalyze、DocETL 均无新动态；Cube Core v1.8.32 补丁 11 月 21 日发布，未取得逐条更新说明，本期未作条目）；Spider 2.0、BIRD、DABstep、DAComp 等评测基准原作者团队当日无新动态，Hugging Face Papers 11 月 23 日日榜前列无与数据代理直接相关的论文；ThoughtSpot 26.11 发布说明（含 Spotter on Liveboards GA 等）仍未确认精确发布日期，本期未作条目；国内大厂与国内独立厂商除火山引擎一项外当日无数据代理相关新发布；中文媒体 36氪、机器之心、量子位、InfoQ、DataFunTalk、Datawhale、dbaplus、墨天轮、和鲸当日均无数据智能体直接相关的新内容；社交媒体当日未见可核实的数据代理新线索（所见 Instagram 与 Facebook 帖子均为 11 月 19 日 Genie ZeroOps 公开 Beta 的二次传播）。Databricks Genie 接入微软全家桶的 11 月 18 日博客与 11 月 19 日、11 月 21 日两期已收录的 Genie MCP 延伸内容重叠，本期不再重复；Qlik Answers 与 Cube Apps 已于 11 月 21 日一期收录，本期不再重复。

## 今日回顾

Sigma Assistant 上线可追溯答案，回答中的每个数字可追溯到计算过程与数据血缘，全体客户默认开启；Sigma 同周更新日志新增语音输入与工作簿 PDF 附件。Snowflake Cortex Agent SDK v1.0.0 正式 GA，微软 Fabric 数据智能体的高级 NL2SQL 与高级 DAX 转正并完成标准运行时推送，dbt Wizard Desktop 进入公开 Beta、dbt Charts 进 Claude 与 ChatGPT。Oracle 发布 Analytics 11 月更新，Palantir 在 Insight 内推出 AIP Insight（beta），Hex 刊登 Underdog 的 1 万多次分析对话实践，Alteryx 更新 Agent Studio 发布说明。Matters.AI 完成约 1,200 万美元 Pre-A 轮，火山引擎披露与中油共享的 18 个智能体合作，微软宣布 Atlan 为首选数据治理合作伙伴，微软与甲骨文宣布 Foundry agent 经托管 MCP 访问 Oracle 数据库。arXiv 今日上线 AskWise、Decision Columns 与 Federated KPI Aggregation 三篇论文。
