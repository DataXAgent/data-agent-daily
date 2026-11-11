---
layout: post
title: "Data Agent Daily — 2026-11-11"
author: dad
date: 2026-11-11
image: "assets/images/covers/2026-11-11.svg"
description: "IBM 与微软在 11 月 10 日联合发布行业智能体平台 Imagine Enterprise，IBM Consulting 提供 6,000 多个预建智能体与资产，微软以 Foundry、Copilot Studio 与 Fabric 提供 AI 与数据底座，首批面向金融、保险与零售。"
categories: ["Data Agent Daily"]
tags: ["data-agent", "news"]
comments: false
---

## 今日速览

- IBM 与微软在 11 月 10 日联合发布行业智能体平台 Imagine Enterprise，IBM Consulting 提供 6,000 多个预建智能体与资产，微软以 Foundry、Copilot Studio 与 Fabric 提供 AI 与数据底座，首批面向金融、保险与零售。
- project44 在 11 月 10 日宣布其 AI 供应链分析师 Mo 接入 Snowflake Cortex AI，以约 1 万亿条货运记录的物流本体加语义解析提问，内测 10/10 答对、速度为通用大模型的 2.5 倍，210 家客户已用、累计回答 5 万多个问题。
- Denodo 在 11 月 10 日与 AWS 签署多年战略合作协议，以 Denodo 平台为 AI 数据层，让智能体在 Bedrock AgentCore 与 SageMaker 上零复制访问实时受治理数据，拜耳作物科学称找数据时间减少 80%。
- Google Cloud 在 11 月 10 日发布 Gemini for healthcare 预览版，以通用 Gemini agent 为底座，统一电子病历、理赔与医保数据，执行病历合成、就诊准备与预授权等多步工作流。
- PuppyGraph 在 11 月 10 日宣布完成 1,000 万美元 A 轮融资，累计融资 1,500 万美元，其 1.0 版已 GA，可让 AI 智能体把最多 3,000 张企业表当作统一图谱就地查询、亚秒级返回。
- arXiv 11 月 10 日上线企业分析智能体评估框架比较研究，轨迹法在 72 个已知风险用例上 F1 为 0.90，纯文本法误报多 5 倍，第三阶段发现 24 个新失效。
- arXiv 11 月 10 日上线 FERN：面向 Text-to-SQL 的跨基准表检索，融合三个冻结检索器加 LightGBM 重排、无生成式 LLM，在 Spider 上 complete@5 从 83.9% 提升至 95.6%，单问题中位延迟 208 毫秒。
- arXiv 11 月 10 日上线 NIFT-SQL：面向企业 Text-to-SQL 检索的客户监督表打分，每客户示例问题微调检索器加 560M 交叉编码器打分融合，在 BEAVER、LiveSQLBench 等集上 complete@15 达 69.2%、89.5%、85.6%。
- arXiv 11 月 10 日上线《智能体基准在任务耗尽前就停止区分优劣》，重打 8 个数据科学/ML 工程智能体基准的已发布结果，发现二值通过/失败计分过粗且以参考答案为上限，提出带日期锚点的截断对数比计分加成本单列。
- arXiv 11 月 10 日上线已验证智能体入库研究：窄智能体提议模式、39 类检查的验证器两轮校验、人工审批，在 4 个公开生物医学数据集上 4,510 万个值零对账缺口、每数据集成本不足 0.50 美元。
- arXiv 11 月 10 日上线 SHARP：面向下一兴趣点预测的语义分层智能体推理与动态记忆，在 3 个真实数据集上 Acc@5、Acc@10 平均比最强基线高 5.29 和 4.52 个百分点。
- arXiv 11 月 10 日上线 AutoManifold：基于流形嵌入的数据可视化算法智能体设计，多智能体 LLM 编排从亲和度、代价与优化原语组合生成流形嵌入算法，在真实数据集上优于 t-SNE、UMAP 与 PaCMAP。
- arXiv 11 月 10 日上线 TreeAgent：面向长层级数据的结构感知记忆智能体，在 8K–1M token 的 JSON/HTML/YAML/JS 检索与聚合任务上使 4 类记忆智能体平均提升 3.61%。
- arXiv 11 月 10 日上线《从反事实编辑到人类叙事》：面向推荐系统解释的 LLM 驱动解读，用 LLM 把反事实交互编辑清单概括为自然语言解释并以偏好优化调优，在 MovieLens-1M 上语言质量高。
- MotherDuck 在 11 月 10 日于 LinkedIn 发文称“每个人都应拥有自己的数据代理”，CEO Jordan Tigani 将于 11 月 17 日分享 MotherDuck 下一步动向。

## 公司发布 / 官方博客

### 1. IBM 与微软联合发布 Imagine Enterprise 行业智能体平台（11/10）
IBM 与微软在 11 月 10 日联合发布 Imagine Enterprise，一个面向行业场景的智能体平台，帮助企业构建、运行与治理执行行业特定流程的 AI 智能体。IBM Consulting 提供 6,000 多个预建智能体与资产及行业经验，微软提供 AI、数据、云与安全底座：Microsoft Foundry、GitHub Copilot 与 Microsoft Copilot Studio 协调智能体与企业系统，Microsoft Fabric、Microsoft 365 基础设施、Microsoft Entra、Microsoft Purview、Microsoft Defender 与 Microsoft Azure 提供数据、身份、AI 治理、安全与云基础；IBM Consulting Advantage 的 Process Studio、Context Studio 与 Advantage Core 帮助设计、部署与治理定制智能体。平台首批行业框架覆盖金融服务、保险与零售，另有前置部署工程师支持。金融科技公司 SEI 正在与 IBM Consulting 及微软探索以该平台推进企业转型。
- [微软官方新闻中心（11/10）](https://news.microsoft.com/source/2026/11/10/ibm-and-microsoft-announce-a-new-ai-agent-platform-designed-for-industry-specific-transformation/)

### 2. project44 的 AI 供应链分析师 Mo 接入 Snowflake Cortex AI（11/10）
project44 在 11 月 10 日宣布其 AI 供应链分析师 Mo 与 Snowflake 集成：以 project44 约 1 万亿条十年货运记录的物流本体与语义解析问题，Snowflake Cortex Analyst 把问题转成 SQL 取数。Mo 的核心是一套 AI 智能体约束机制（guardrails、工作流与执行能力），让智能体在供应链任务上采取行动，而不只是回答提示。内测中，Mo 在 10 道已验证测试题上 10/10 答对、10 次回答全部一致，通用大模型分别为 2/10 与 2/10；Mo 的响应速度为通用大模型的 2.5 倍。210 家客户已在使用 Mo，累计回答 5 万多个问题；个别企业客户在滞期费与滞箱费上单项减少 600 万美元敞口，在单个问题上释放 20 万美元营运资金。
- [GlobeNewswire 通稿（11/10）](https://www.globenewswire.com/news-release/2026/11/10/3399562/0/en/project44-turns-supply-chain-data-into-ai-powered-decisions-with-snowflake.html)

### 3. Denodo 与 AWS 签署多年战略合作协议：为智能体提供可信数据访问（11/10）
Denodo 在 11 月 10 日宣布与 AWS 签署多年战略合作协议，以 Denodo 平台为 AI 数据层，帮助企业在实时受治理数据的基础上开发与规模化智能体。合作内容包括联合研讨会、联合营销、现场协同销售、商业激励与系统集成商方案，覆盖银行反欺诈、保险理赔与制造预测性维护等场景。Denodo 平台把 Bedrock AgentCore、Amazon Quick 与 SageMaker 等 AWS 服务扩展到分布在本地、SaaS 与多云环境中的企业数据，智能体以零复制方式访问受治理的业务上下文，复用同一批受治理数据产品、语义定义与访问策略。拜耳作物科学称，借助 Denodo 的 AI 数据层与 AWS 方案，团队找数据的时间减少 80%，自主客服与跟踪智能体已投入生产。
- [GlobeNewswire 通稿经 Medianet 转载（11/10）](https://newshub.medianet.com.au/2026/11/denodo-signs-strategic-collaboration-agreement-with-aws-to-accelerate-trusted-data-access-for-agentic-ai/181048/)

### 4. Google Cloud 发布 Gemini for healthcare 预览版（11/10）
Google Cloud 在 11 月 10 日发布 Gemini for healthcare 预览版：以通用 Gemini agent 为底座的行业方案，把分散在各系统的病历、理赔与医保数据统一起来，执行病历合成、就诊准备、覆盖核查与预授权等多步工作流，全程保留人工监督。方案由四部分组成：医疗技能（专家编写的多步指令，如病历合成、就诊前准备、覆盖与保单审核、 payer 福利判定）、连接器库（Epic 电子病历只读接入、Oracle Health 电子病历只读接入、InterSystems FHIR MCP Server、Verato 身份解析、Keragon 400 多个医疗应用接入等）、开放合作伙伴生态，以及支持 HIPAA 合规的安全受治理平台与开放模型选择。Google 称，临床医生每周约花 28 小时手动核对信息；HCA Healthcare、Highmark Health 与 Northwell Health 等机构已在参与 shaping 该方案。
- [Google Cloud 官方博客（11/10）](https://cloud.google.com/blog/products/ai-machine-learning/gemini-for-healthcare)

## 新闻网站

### 5. PuppyGraph 完成 1,000 万美元 A 轮融资，1.0 版已 GA：智能体可就地查询 3,000 张表（11/10）
图查询引擎公司 PuppyGraph 在 11 月 10 日宣布完成 1,000 万美元 A 轮融资，由 Particle Future 与 defy.vc 领投，累计融资 1,500 万美元；其 PuppyGraph 1.0 刚进入 GA。1.0 版把图计算直接带到 Apache Iceberg、Databricks、Snowflake、ClickHouse、DuckDB、PostgreSQL、Microsoft Fabric 与 Apache Hudi 等数据源，让 AI 智能体把最多 3,000 张企业表当作统一图谱就地查询、亚秒级返回，无需把数据搬进图数据库；4 台机器集群上一次跨数十亿边的 10 跳查询用时 2.26 秒。内置 AI 智能体或经 MCP 连接的外部工具可用自然语言查询，查询引擎会拒绝未定义的关系引用并返回可供智能体纠错的反馈。公司称过去一年年度经常性收入增长 7 倍，客户包括 AMD、Palo Alto Networks、Datadog、Coinbase 与 Trend Micro。
- [BusinessWire 通稿（11/10）](https://www.businesswire.com/news/home/20261110709159/en/PuppyGraph-Raises-%2410M-Series-A-to-Help-Enterprises-Build-AI-Agents-That-Query-3000-Tables-in-Subseconds)

## 论文 / arXiv

### 6. 企业分析智能体评估框架比较：轨迹法 F1 为 0.90，纯文本法误报多 5 倍（arXiv 11/10 上线，11/10 提交）
arXiv 11 月 10 日上线的论文《Comparative Analysis of Agent Evaluation Frameworks: Stability, Detection, and Discovery in Enterprise Analytics Agents》（arXiv:2611.14493，11 月 10 日提交）对三种评估范式做三阶段比较：基于轨迹的 LLM 评审、纯文本 LLM 评审加红队、确定性启发式，对象为两个企业分析智能体。第一阶段测评估框架稳定性，97% 的配置达到稳定性阈值；第二阶段在 72 个已知风险用例上测已知风险检出，轨迹法精确率与召回率平衡最优（F1=0.90），纯文本法召回率相当但误报多 5 倍；第三阶段测未知风险发现，找出 24 个新失效，功能测试与安全红队之间零重叠。论文建议双框架策略：轨迹评估用于功能评估，对抗红队用于安全验证。
- [arXiv:2611.14493](https://arxiv.org/abs/2611.14493)

### 7. FERN：面向 Text-to-SQL 的跨基准表检索，无生成式 LLM（arXiv 11/10 上线，11/10 提交）
arXiv 11 月 10 日上线的论文《FERN: Cross-Benchmark Table Retrieval for Text-to-SQL with Frozen Retrievers and Learned Ranking》（arXiv:2611.14477，11 月 10 日提交）针对大 pooled catalog 上的 Text-to-SQL 表检索：融合三个冻结检索器得到 100 个候选表，每表以最多 120 个特征描述，再用在 BIRD 训练问题上拟合一次的 LightGBM 排序器重排，全程不用生成式 LLM。在 Spider 上，complete@5（前 5 个表包含全部 gold 表的问题占比）从 83.9% 提升至 95.6%；在 BIRD 有证据提示时 top-5 召回为 96.6%；单问题中位延迟为 208 毫秒（单张 A100，无托管模型调用）。
- [arXiv:2611.14477](https://arxiv.org/abs/2611.14477)

### 8. NIFT-SQL：面向企业 Text-to-SQL 检索的客户监督表打分（arXiv 11/10 上线，11/09 提交）
arXiv 11 月 10 日上线的论文《NIFT-SQL: Customer-Supervised Table Scoring for Enterprise Text-to-SQL Retrieval》（arXiv:2611.12731，11 月 9 日提交）针对企业 Text-to-SQL：用每客户的示例问题微调检索器，再以 560M 交叉编码器对每张表打分（判断查询是否需要该表），经逻辑回归融合。在 BEAVER、LiveSQLBench 与 LiveSQLBench-Large（244 至 971 张表）上，complete@15 分别为 69.2%、89.5% 与 85.6%，高于混合检索基线的 30.4%、41.0% 与 21.8%，也高于同标签微调检索器的 61.1%、81.7% 与 70.4%；加入零样本 8B 重排器的高精度模式分别达到 72.4%、92.5% 与 88.6%。
- [arXiv:2611.12731](https://arxiv.org/abs/2611.12731)

### 9. 智能体基准在任务耗尽前就停止区分优劣：二值计分过粗且以参考答案为上限（arXiv 11/10 上线，11/10 提交）
arXiv 11 月 10 日上线的论文《Agent Benchmarks Stop Ranking Before They Run Out of Tasks》（arXiv:2611.13541，11 月 10 日提交）重打 8 个数据科学/ML 工程智能体基准的已发布结果，包括 MLE-bench、ALE-Bench、SWE-bench Verified 与 Terminal-Bench。论文发现，饱和大多来自度量本身而非任务：多数智能体基准把一次运行归约为一个通过/失败二值，过粗——SWE-bench Verified 前十相邻模型的差距小于测试本身的误差；且以参考答案为上限——ALE-Bench 前十按竞赛分数分开，但按人类中位数评分时打成平手，尽管近半数运行超过该人类水平。论文提出带日期锚点的截断对数比计分，并把成本作为单独一轴；在一次 Terminal-Bench 重跑中，通过/失败打平的模型在测试丢弃的数量指标上相差十倍以上。
- [arXiv:2611.13541](https://arxiv.org/abs/2611.13541)

### 10. 已验证智能体入库：智能体提议、代码验证、人类拍板（arXiv 11/10 上线，11/08 提交）
arXiv 11 月 10 日上线的论文《Agents Propose, Code Verifies, Humans Decide: Verified Agentic Ingestion of Heterogeneous Scientific Tables into Relational Databases》（arXiv:2611.11045，11 月 8 日提交）针对异构科学表格入库：窄智能体提议模式，39 类检查的验证器做两轮校验，人工审批后入库。在 4 个公开生物医学数据集上，4,510 万个值零对账缺口，每数据集成本不足 0.50 美元。
- [arXiv:2611.11045](https://arxiv.org/abs/2611.11045)

### 11. SHARP：面向下一兴趣点预测的语义分层智能体推理与动态记忆（arXiv 11/10 上线，11/10 提交）
arXiv 11 月 10 日上线的论文《SHARP: Semantic Hierarchical Agentic Reasoning for Next POI Prediction with Dynamic Memory》（arXiv:2611.14220，11 月 10 日提交）结合轨迹记忆智能体、多粒度时感知类别转移图与类别引导的 POI 预测器，在 3 个真实数据集上，Acc@5 与 Acc@10 平均比最强基线高 5.29 和 4.52 个百分点。
- [arXiv:2611.14220](https://arxiv.org/abs/2611.14220)

### 12. AutoManifold：基于流形嵌入的数据可视化算法智能体设计（arXiv 11/10 上线，11/10 提交）
arXiv 11 月 10 日上线的论文《AutoManifold: Agentic Design of Data Visualisation Algorithms via Manifold Embedding》（arXiv:2611.13710，11 月 10 日提交）用多智能体 LLM 编排，从亲和度、代价与优化原语组合生成流形嵌入算法，按用户结构保留偏好迭代优化，在真实数据集上优于 t-SNE、UMAP 与 PaCMAP。
- [arXiv:2611.13710](https://arxiv.org/abs/2611.13710)

### 13. TreeAgent：面向长层级数据的结构感知记忆智能体（arXiv 11/10 上线，11/10 提交）
arXiv 11 月 10 日上线的论文《TreeAgent: Structure-Aware Memory Agent for Processing Long Hierarchical Data》（arXiv:2611.13946，11 月 10 日提交）按输入层级切分子树片段并附加结构路径与残差记忆链接，在 8K–1M token 的 JSON/HTML/YAML/JS 检索与聚合任务上，使 4 类记忆智能体平均提升 3.61%。
- [arXiv:2611.13946](https://arxiv.org/abs/2611.13946)

### 14. 从反事实编辑到人类叙事：面向推荐系统解释的 LLM 驱动解读（arXiv 11/10 上线，11/10 提交）
arXiv 11 月 10 日上线的论文《From Counterfactual Edits to Human Narratives: LLM-Driven Interpretations for Recommender System Explanations》（arXiv:2611.13914，11 月 10 日提交）用 LLM 把反事实交互编辑清单概括为自然语言解释，并以偏好优化调优，在 MovieLens-1M 上语言质量高，直接偏好优化在几乎所有设置下提升语义指标。
- [arXiv:2611.13914](https://arxiv.org/abs/2611.13914)

## 社交媒体

### 15. MotherDuck 在 LinkedIn 发文：每个人都应拥有自己的数据代理（11/10）
MotherDuck 在 11 月 10 日于 LinkedIn 官方账号发文称“每个人都应拥有自己的数据代理”，CEO Jordan Tigani 将于 11 月 17 日分享 MotherDuck 下一步动向，并回顾 10 月“Ducktober”8 天 8 个发布（含 Agent Chat）。
- [MotherDuck LinkedIn 官方账号（11/10）](https://www.linkedin.com/company/motherduck)

本期检索范围内，中文媒体层当日未见可核实的数据智能体新内容；监测名单内其余厂商、研究团队与评测基准机构在过去 24 小时内未见可核实的新动态；监测名单内其余开源项目当日未见实质 Release。

## 今日回顾

IBM 与微软在 11 月 10 日联合发布行业智能体平台 Imagine Enterprise，IBM Consulting 提供 6,000 多个预建智能体与资产，微软以 Foundry、Copilot Studio 与 Fabric 提供 AI 与数据底座，首批面向金融、保险与零售；project44 在 11 月 10 日宣布其 AI 供应链分析师 Mo 接入 Snowflake Cortex AI，内测 10/10 答对、速度为通用大模型的 2.5 倍；Denodo 在 11 月 10 日与 AWS 签署多年战略合作协议，拜耳作物科学称找数据时间减少 80%；Google Cloud 在 11 月 10 日发布 Gemini for healthcare 预览版，统一电子病历、理赔与医保数据；PuppyGraph 在 11 月 10 日宣布完成 1,000 万美元 A 轮融资，1.0 版已 GA；arXiv 11 月 10 日上线 9 篇论文，涵盖企业分析智能体评估、Text-to-SQL 表检索（FERN、NIFT-SQL）、智能体基准饱和、已验证智能体入库、兴趣点预测、可视化算法智能体、长层级数据记忆智能体与推荐解释；MotherDuck 在 11 月 10 日于 LinkedIn 发文称每个人都应拥有自己的数据代理；中文媒体层当日未见可核实的数据智能体新内容。
