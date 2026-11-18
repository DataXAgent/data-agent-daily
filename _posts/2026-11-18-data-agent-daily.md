---
layout: post
title: "Data Agent Daily — 2026-11-18"
author: dad
date: 2026-11-18
image: "assets/images/covers/2026-11-18.svg"
description: "微软在 Ignite 2026 上发布企业上下文管理平台 Microsoft IQ 并与 Salesforce 推出 Copilotforce，Fabric IQ 把受治理的 Power BI 语义模型与数据智能体带入 Copilot，Excel 内问数进入预览。"
categories: ["Data Agent Daily"]
tags: ["data-agent", "news"]
comments: false
---

## 今日速览

- 微软在 Ignite 2026 上发布企业上下文管理平台 Microsoft IQ，Fabric IQ 把受治理的 Power BI 语义模型与数据智能体带入 Copilot，Excel 内问数进入预览；同日与 Salesforce 推出 Copilotforce，Salesforce in Copilot 公开预览、含 38+ 预置销售技能，Data 360 与 Fabric 双向 Zero Copy 集成。
- Wren AI 与 Phison 在 SC26 发布本地部署 GenBI 一体机，自然语言问数、推理跑在企业自有基础设施上。
- Atlan 与微软合作，把跨域血缘与治理扩展到 OneLake 数据资产，Fabric 原生连接器已 GA。
- Alation 连续第二年入选 Gartner 数据与分析治理平台魔力象限领导者。
- Databricks 宣布 Genie Migrate for Lakehouse 正式可用，支持 7 类传统数仓自动迁移，宣称转换准确率 90%+、交付周期快 25%。
- theairankings 更新《Best AI for Data Analysis》指南，Spider 2.0 榜首智能体系统在 Snowflake 集上超 96%、最难的 dbt 集上为 65.6%。
- Tableau Studio 云版 11 月 17 日按计划上线，服务器版定于 11 月 19 日。
- DB-GPT 发布 v0.8.3，新增结构化可追溯的数据分析报告、Next.js 16 仪表盘工作区与 Agent 可观测追踪。
- arXiv 11 月 18 日上线 MoL-SQL：首个可控多语言混合 Text-to-SQL 基准，16,892 条 MoL-Full，存储值语言最多造成 23 个点的精度损失。
- arXiv 11 月 18 日上线 DisGuAD：交互式 Text-to-SQL 的歧义检测框架，关键歧义覆盖率从 48.62% 升至 82.75%。
- arXiv 11 月 18 日上线 GuardAgent：面向 LLM 推荐系统推广型攻击的记忆增强智能体检测框架，WSDM 2027 录用。
- arXiv 11 月 18 日上线 Better Rankers, Worse Retrievers：生成式推荐经 RL 后训练后顶部精度提升、5 个数据集候选召回全部下降。
- arXiv 11 月 18 日上线 VerRec：以文字反馈做生成式推荐的强化学习，3 个 Amazon 数据集上提升推荐精度与排序质量。
- arXiv 11 月 18 日上线 CG2R：簇引导解码的个性化推荐，3 个基准数据集上超过经典、神经与 LLM 基线。
- Databricks 官方 Instagram 发布 OpenAI 总裁 Brockman 与 CEO Ghodsi 对谈，谈 Genie 本体层与企业数据可及性。
- 微软 Agent 365 Business Analytics 仪表盘演示：240 万次已识别用例会话、成本 710 万美元、AI 价值 2,520 万美元。
- 阿里云开发者社区刊登社区投稿，介绍面向非结构化数据的 AI 智能体架构，自动完成合同、报告等文档的信息抽取与结构化输出。

## 公司发布 / 官方博客

### 1. 微软在 Ignite 2026 发布 Microsoft IQ，并与 Salesforce 推出 Copilotforce（11/17）
微软 11 月 17 日在 Ignite 2026 上宣布企业上下文管理平台 Microsoft IQ 全面可用：汇聚 Work IQ、Fabric IQ、Foundry IQ、Web IQ 四层上下文与 350 多个第三方连接器，让智能体复用企业自身的业务知识、数据、技能与工具；新推出的业务插件（business plugins）把经治理的上下文、技能与权威来源打包，供 Copilot、GitHub Copilot、Foundry（经 MCP）及 ChatGPT、Claude 应用市场中的智能体复用。Fabric IQ 方面，Power BI 语义模型已在 Microsoft Copilot 中全面可用，Fabric 数据智能体即将进入 Copilot、全面可用在即；Excel 内“Edit with Copilot”的 Fabric IQ 进入预览，用户可对受治理的 Power BI 语义模型提问并生成实时连接的透视表；面向 ChatGPT 与 Claude 的 Fabric IQ 连接器、GitHub Copilot 中的 Fabric IQ 本体、Fabric 应用均进入预览。Work IQ 方面，业务应用、Retrieve、实时会议上下文、长时任务与智能体间协作、细粒度 MCP 策略、OpenAI 与 Anthropic 插件均已全面可用。微软同时以澳大利亚电网运营商 AEMO 为例：双方不到 12 周联合开发的 NEM-GEM 运行智能以 Microsoft IQ 为底座。同日，微软与 Salesforce 宣布 Copilotforce 合作：Salesforce in Copilot 插件公开预览，含 38+ 预置销售技能；Salesforce Data 360 与 Microsoft Fabric 之间双向 Zero Copy 集成，OneLake 数据联邦查询已在 Data 360 内全面可用，Data 360 数据共享进 OneLake 为公开预览；Sales Cloud in Teams 进入试点。埃森哲为设计与实施合作伙伴及试点客户，其内部已部署 Copilot 给 74 万多人、Salesforce 用户 5.5 万人。
- [微软官方博客：Microsoft IQ（11/17）](https://azure.microsoft.com/en-us/blog/introducing-the-new-microsoft-iq-putting-your-organizations-intelligence-to-work-in-every-agent/)
- [Microsoft News Center：Copilotforce（11/17）](https://news.microsoft.com/source/2026/11/17/microsoft-and-salesforce-announce-copilotforce-bringing-trusted-customer-context-and-action-into-microsoft-ai-experiences/)
- [Instagram @microsoftcloud 介绍短片（11/18）](https://www.instagram.com/reel/Df2r33GjydP/)

### 2. Wren AI 与 Phison 在 SC26 发布本地部署 GenBI 一体机（11/17）
Wren AI 11 月 17 日在 SC26（芝加哥）宣布与 Phison 合作推出本地部署 AI 分析一体机：Wren AI 生成式 BI 平台结合 Phison AI Data Platform、NVIDIA GPU 与 Pascari aiDAPTIV，团队可用自然语言问数、得到受治理的 SQL、图表与仪表盘，推理跑在企业自有基础设施上，Wren AI 提供统一语义层。Wren AI 官方 Facebook 同期发布 Agentic GenBI 演示视频：一句自然语言自动查数、建图并生成“客户与产品总览”仪表盘，技术要点为统一业务上下文层、可复用的 Skills and Memory，以及数据库行列级权限治理。
- [EINPresswire 通稿（11/17）](https://www.einpresswire.com/article/957164436/wren-ai-collaborates-with-phison-on-on-premises-ai-analytics-at-sc26)
- [Wren AI 官方 Facebook 演示视频（11/17）](https://www.facebook.com/reel/1120238314171894/)

### 3. Atlan 与微软合作，把跨域血缘与治理扩展到 OneLake 数据资产（11/17）
Atlan 11 月 17 日宣布与微软合作：Atlan 的跨域血缘与治理能力与 OneLake 目录协同，覆盖 Fabric 内外的数据资产；Atlan 的 Fabric 原生连接器已全面可用，可将 Lakehouse、仓库、语义模型、Power BI 报表编目到列级，并覆盖 120 多个其他数据源。
- [BusinessWire 通稿（11/17，经转载）](https://markets.financialcontent.com/malvern-online/article/bizwire-2026-11-17-atlan-and-microsoft-collaborate-to-extend-onelake-governance-across-the-data-estate)

### 4. Alation 连续第二年入选 Gartner 数据与分析治理平台魔力象限领导者（11/17）
Alation 11 月 17 日宣布，在 2026 年 Gartner 数据与分析治理平台魔力象限中连续第二年被评为领导者；Gartner 该报告评估了 16 家厂商，报告作者为 Anurag Raj 等，日期为 2026 年 11 月 12 日。
- [GlobeNewswire 通稿（11/17）](https://www.globenewswire.com/news-release/2026/11/17/3405001/0/en/alation-named-a-leader-in-the-gartner-magic-quadrant-for-data-and-analytics-governance-platforms-for-the-second-year-in-a-row.html)

## 新闻网站

### 5. theairankings 更新《Best AI for Data Analysis》指南：分析已走向智能体化，榜首均为智能体系统（11/18 更新）
theairankings 在 11 月 18 日更新的《Best AI for Data Analysis》指南称，数据分析已从“写一条公式”走向“端到端分析一个数据集”，工具按通用聊天模型、专用分析师、电子表格 Copilot 与仓库原生智能体四类划分，首选为 ChatGPT 高级数据分析、Claude for Excel、Julius AI、Gemini 数据科学智能体与 Microsoft Copilot。指南复核的基准数字与昨日 MMNTM 文章一致：Spider 2.0 榜首智能体系统在 Snowflake 集上超 96%，最难的 dbt 集上为 65.6%；2026 年 1 月的审计称 Spider 2.0-Snow 标注错误率为 62.8%、BIRD Mini-Dev 为 52.8%；DABstep 困难任务上发布论文中的最佳智能体仅 14.55%；研究框架发现 Gemini 在最难的多步分析任务上最强。
- [theairankings 指南（11/18 更新）](https://theairankings.com/best-ai-for-data-analysis/)

### 6. Tableau Studio 云版 11 月 17 日按计划上线，服务器版 11 月 19 日跟进（11/17，简讯）
按 11 月 16 日已宣布的发布计划，Tableau Studio 云版于 11 月 17 日上线，服务器版 11 月 19 日跟进；今日未检索到上线后的新细节或新事实增量，按防重复规则仅作一句简讯，不再作头条。
- [首尔经济日报英文版报道（11/17）](https://en.sedaily.com/business/2026/11/17/salesforce-launches-tableau-studio-an-ai-agent-for-data)

### 7. 阿里云开发者社区刊登非结构化数据 AI 智能体架构投稿（11/18）
阿里云开发者社区 11 月 18 日刊登社区用户投稿，介绍面向非结构化数据的 AI 智能体方案，采用感知-认知-执行三层架构（OCR 与版面解析 + RAG 与知识图谱 + LLM 与 ReAct 工具调用），自动完成合同、报告等文档的信息抽取、校验与 JSON 结构化输出。本条为社区投稿、非官方发布，与 ChatBI、text-to-SQL 的直接相关性较弱。
- [阿里云开发者社区文章（11/18）](https://developer.aliyun.com/article/1785188)

## 开源项目

### 8. DB-GPT 发布 v0.8.3：结构化可追溯的数据分析报告与 Agent 可观测追踪（11/17）
DB-GPT 在 11 月 17 日 23:31（北京时间）发布 v0.8.3，新增结构化可追溯的数据分析报告、Next.js 16 仪表盘工作区、Agent 可观测追踪，并加固 Agent 工具调用与报告生成、提升证据验证与报告恢复能力。Cube Core v1.8.27 发布于 11 月 17 日 20:45，在本期检索窗口开始前 15 分钟，不计入本期；WrenAI 最新仍为 11 月 10 日的 v0.18.0；Vanna、Apache Gravitino、DocETL、Chat2DB、DeepEye-SQL、Alpha-SQL、ReFoRCE、LAMBDA、Data Interpreter 当日均无新 Release。
- [DB-GPT v0.8.3 Release](https://github.com/eosphoros-ai/DB-GPT/releases/tag/v0.8.3)

## 论文 / arXiv

### 9. MoL-SQL：首个可控多语言混合 Text-to-SQL 基准，存储值语言最多造成 23 个点的精度损失（11/18）
MoL-SQL: A Controlled Benchmark for Mixture-of-Language Text-to-SQL（arXiv:2611.22333，11 月 17 日提交，11 月 18 日上线，作者 Tianqi Luo、Boyan Li、Yuyu Luo）提出首个可控的多语言混合 Text-to-SQL 基准：问题、schema 与存储值三者的语言可独立切换；MoL-Full 16,892 条、MoL-Cube 3,840 条覆盖全部语言组合。8 个 LLM 与 4 类方法的实验显示，存储值语言最多造成 23 个点的精度损失，问题翻译与额外推理无法缩小该差距。
- [arXiv:2611.22333](https://arxiv.org/abs/2611.22333)

### 10. DisGuAD：交互式 Text-to-SQL 的歧义检测框架，关键歧义覆盖率从 48.62% 升至 82.75%（11/18）
Asking What Matters: Disagreement-Guided Ambiguity Detection for Interactive Text-to-SQL（arXiv:2611.21645，初投 2026 年 10 月 14 日，11 月 18 日列入 cs.DB 上线列表，作者 Su Dong、Jiayan Lin、Yujia Liu、Zijin Hong、Qinggang Zhang、Feiran Huang、Xiao Huang）针对交互式 Text-to-SQL 的澄清目标选择：用候选 SQL 之间的分歧定位对最终查询有影响的歧义。在 BIRD-Interact Lite 与 Full 上，相对原交互策略归一化 Reward 提升 4.40–8.97 点，关键歧义覆盖率从 48.62% 升至 82.75%（Lite）、从 45.76% 升至 85.14%（Full）。
- [arXiv:2611.21645](https://arxiv.org/abs/2611.21645)

### 11. GuardAgent：面向 LLM 推荐系统推广型攻击的记忆增强智能体检测框架（11/18）
GuardAgent: A Memory-Augmented Agentic Framework for Adaptive Detection of Adversarial Promotions in LLM-Based Recommendation（arXiv:2611.22274，11 月 17 日提交，11 月 18 日上线，作者 Shiyi Yang、Xinshu Li、Chen Wang、Xiwei Xu、Liming Zhu、Lina Yao），已被 WSDM 2027 录用。论文称其为首个系统研究针对 LLM 推荐系统的推广型攻击（adversarial promotion）检测的工作，提出感知-行动-反思-记忆循环的记忆增强 agentic 检测框架，在真实数据集上达到最优泛化性能（摘要未给出具体数字）。
- [arXiv:2611.22274](https://arxiv.org/abs/2611.22274)

### 12. Better Rankers, Worse Retrievers：生成式推荐经 RL 后训练后顶部精度提升、候选召回全部下降（11/18）
Better Rankers, Worse Retrievers: The Hidden Cost of RL Post-Training in Generative Recommendation（arXiv:2611.22838，11 月 17 日提交，11 月 18 日上线，作者 Yuheng Chen、Fan Zhang、Yixuan Xu、Chao Yang、Yang Xiang、Can Yang）发现，生成式推荐器经 RL 后训练后顶部精度提升，但 5 个数据集上候选列表召回（数百量级的 hit@K）全部下降；根因是每用户仅一条正样本，导致 RL 把其他合理候选当作错误惩罚；提出的 out-of-rollout anchoring 单一附加损失项可在保留顶部增益的同时把召回恢复到 SFT 水平。
- [arXiv:2611.22838](https://arxiv.org/abs/2611.22838)

### 13. VerRec：以文字反馈做生成式推荐的强化学习（11/18）
More Than a Score: Reinforcement Learning with Verbalized Feedback for Generative Recommendation（arXiv:2611.22410，11 月 17 日提交，11 月 18 日上线，作者 Zipeng Chen、Xinyu Lin、Yuliang Sun、Sheng Zhang、Zeyu Wang、Xiaowen Shi、Junwei Pan、Chengguo Yin）用用户模拟器生成个性化文字反馈指导生成式推荐的强化学习（GRPO 联合优化原始与精炼候选），在 3 个 Amazon 数据集与 2 个生成式推荐骨干上均提升推荐精度与排序质量，文字反馈还促进了候选多样性探索。
- [arXiv:2611.22410](https://arxiv.org/abs/2611.22410)

### 14. CG2R：簇引导解码的个性化推荐，3 个基准数据集上超过经典、神经与 LLM 基线（11/18）
Cluster-Guided Decoding with Trust-Region Constraints for Personalized Recommendation（arXiv:2611.22163，11 月 17 日提交，11 月 18 日上线，作者 Gezheng Wen、Chao Shen、Raviteja Anantha、Tan Shen、Cliff Chung、Layne C. Price）学习语义簇层次结构并把簇级先验直接加入物品打分规则，在 3 个基准数据集上 Recall 与 nDCG 超过经典、神经与 LLM 基线，冷启动用户仍可用，毫秒级在线服务。
- [arXiv:2611.22163](https://arxiv.org/abs/2611.22163)

## 社交媒体

### 15. Databricks 宣布 Genie Migrate for Lakehouse 正式可用（11/17）
Databricks 官方 Facebook 发布产品视频，宣布 Genie Migrate for Lakehouse 正式可用，可将 Teradata、Oracle、BigQuery、SQL Server、Redshift、Snowflake、Azure Synapse 七类传统数仓自动迁移至 Lakehouse，宣称转换准确率 90%+、交付周期快 25%。
- [Facebook Databricks 官方账号视频（11/17）](https://www.facebook.com/reel/1599234818675079/)

### 16. Databricks：OpenAI 总裁 Brockman 对话 CEO Ghodsi，谈 Genie 本体层与企业数据可及性（11/18）
Databricks 官方 Instagram 发布 DATA+AI LIVE 现场对谈片段，Ghodsi 介绍 Genie 本体层（ontology）与 ChatGPT、Astra 的集成，让企业数据可供 Codex 等工具使用；两人一致认为未来数月企业的主要瓶颈是让数据以受治理的方式可供智能体访问。
- [Instagram @databricksinc（11/18）](https://www.instagram.com/reel/Df2xHohFNE9/)

### 17. 微软 Agent 365 Business Analytics 仪表盘演示（11/18）
Microsoft Mechanics 官方 Threads 发布 Agent 365 Business Analytics 仪表盘演示，按业务域、类别与用例分层统计智能体使用情况，展示指标为 240 万次已识别用例会话、成本 710 万美元、AI 价值 2,520 万美元。
- [Threads @msftmechanics（11/18）](https://www.threads.com/@msftmechanics/post/Df3ayrxBGyF)

本期检索范围内，中文媒体 36氪、机器之心、量子位、InfoQ、DataFunTalk、Datawhale、dbaplus、墨天轮、和鲸当日均无数据智能体直接相关的新内容；Hugging Face Papers 11 月 18 日日榜前列无与数据代理直接相关的论文；Spider 2.0、BIRD、DABstep、DAComp 等评测基准原作者团队当日无新动态；OpenAI 11 月 17 日发布 GPT-6.2 Astra 与 Sol 通用基座模型，BenchLM 称 Sol 在数据分析智能体基准 AA-AnalystAgent 上得 53.8 分，按通用基座模型先例未作条目；柏川数据 11 月 18 日完成 5,000 万元 Pre-A 轮融资，面向具身智能数据，未作条目。

## 今日回顾

微软在 Ignite 2026 上发布企业上下文管理平台 Microsoft IQ，Fabric IQ 把受治理的 Power BI 语义模型与数据智能体带入 Copilot，Excel 内问数进入预览；同日与 Salesforce 推出 Copilotforce，Salesforce in Copilot 公开预览、含 38+ 预置销售技能，Data 360 与 Fabric 双向 Zero Copy 集成；Wren AI 与 Phison 发布本地部署 GenBI 一体机；Atlan 与微软把治理扩展到 OneLake；Alation 连续第二年入选 Gartner 治理平台魔力象限领导者；Databricks 宣布 Genie Migrate for Lakehouse 正式可用；DB-GPT 发布 v0.8.3；arXiv 同日上线 MoL-SQL、DisGuAD、GuardAgent、Better Rankers, Worse Retrievers、VerRec 与 CG2R 六篇论文；Tableau Studio 云版按计划上线。
