---
layout: post
title: "Data Agent Daily — 2026-11-12"
author: dad
date: 2026-11-12
image: "assets/images/covers/2026-11-12.svg"
description: "Databricks 在 11 月 11 日发布第二代 Always-on Genie，把 Genie 从问答助手改为常驻自主智能体，Genie Ontology 已 GA，Genie Search 覆盖 100 多个企业数据源，官方基准称任务正确率 91%。"
categories: ["Data Agent Daily"]
tags: ["data-agent", "news"]
comments: false
---

## 今日速览

- Databricks 在 11 月 11 日发布第二代 Always-on Genie，把 Genie 从问答助手改为常驻自主智能体，Genie Ontology 已 GA，Genie Search 覆盖 100 多个企业数据源，官方基准称任务正确率 91%。
- Databricks 在 11 月 12 日把 Genie ZeroOps 推入 Beta，在后台监控作业、流水线与表，检测故障与数据质量问题并给出修复建议；Pages 于 11 月 11 日 GA，Genie 插件同日接通 ChatGPT、Claude 与 Grok Bot/Cursor。
- Google 在 11 月 11 日发布 Gemini Decisions API，单次请求可对同一多模态输入评估最多 1,000 个问题，端到端延迟约 150–250 毫秒，每百万输入 token 收费 0.10 美元、不收输出 token 费。
- Cube Core 在 11 月 11 日发布 v1.8.22 补丁版本，含 CubeSQL 的 TRIM 与 SPLIT_PART 下推、CubeStore 多架构 Docker 镜像发布等。
- Rubrik 在 11 月 11 日宣布 BigQuery 无代理不可变备份 GA，支持整数据集或单表恢复、跨项目与跨区恢复及无限期保留，Google Cloud Storage 保护扩展预计未来数月 GA。
- arXiv 11 月 11 日上线 TIGA：用工具接地的 LLM 智能体做受控分类体系构建，在 4 个基准分类体系、两种 LLM 骨干上多数配置取得最强结构质量，但 token 与调用成本显著更高。
- arXiv 11 月 11 日上线 DocFS：把文件系统作为多模态文档问答的智能体推理环境，配 Qwen3.5-Plus 在 MMLongBench-Doc 与 FinRAGBench-V 上分别比最强基线高 2.9 和 4.3 个百分点，推理最快 10.3 倍、token 最多省 10.1 倍。
- arXiv 11 月 11 日上线 ARoute：面向批处理与流式的任务对齐模型路由，在 15 个任务-成本设定中同等成本下平均准确率全部最高，比最强基线平均高 4.1 个百分点，批处理速度比级联方法最快 2.8 倍。
- arXiv 11 月 11 日上线《Beyond the Document》：提出便携智能体格式 PAF 包，托管受治理阅读器在 400 个冻结问题上成功率 96%，高于指令加原始文件检索的 86%。

## 公司发布 / 官方博客

### 1. Databricks 发布第二代 Always-on Genie：从问答助手到常驻自主智能体（11/11）
Databricks 在 11 月 11 日于 Data + AI Live 发布第二代 Genie，把 Genie 从问答助手改为常驻自主智能体：接管长时任务、委派子智能体、追踪进度、追问缺失输入，并通过优先收件箱与邮件主动推送待决策事项。Genie 可经 Genie One、邮件、Slack 与 Microsoft Teams 使用，能监控保险理赔中的欺诈模式、持续管理营销活动并按周提议预算调整，也能按日程或指标触发条件运行。Genie Ontology 为智能体提供企业业务地图（定义、指标、关系与组织知识），由智能体自动构建、由人治理；Genie Search 把湖仓与 Google Drive、Jira、Confluence、Workday、SharePoint 等 100 多个企业数据源的搜索统一起来；Genie Agents 面向市场、销售、财务与运营等团队提供专业能力；Genie 插件把同一业务上下文带入 ChatGPT、Claude、Copilot 与 Grok Bot；Unity Catalog 与 Unity Gateway 在现有权限与策略内治理 Genie 的行动、用量与成本。Databricks 称，Genie 与 Genie Ontology 已向全部客户 GA，Genie Search、Ontology Manager 与新的 always-on 模式将进入 preview 与 beta；数千客户已在生产中使用 Genie，包括 Zillow、Unilever、adidas、Atlassian 与 AstraZeneca。在与 Turing 共建的基准测试中，Genie 任务正确率为 91%，为更强前沿智能体的 1.6 倍，token 用量不到一半。
- [Databricks 官方新闻稿（11/11）](https://www.databricks.com/company/newsroom/press-releases/databricks-launches-new-always-genie-autonomous-ai-complex)
- [Databricks 官方博客（11/11）](https://www.databricks.com/blog/new-genie-autonomous-ai-complex-enterprise-work)

### 2. Databricks 11 月发布说明：Genie ZeroOps 进 Beta，Pages GA、Genie 插件接通 ChatGPT 与 Claude（11/11–11/12）
Databricks 官方 11 月发布说明记录：Genie ZeroOps 于 11 月 12 日进入 Beta，在后台监控作业、流水线与表，检测故障与数据质量问题、调查根因并给出修复建议。Pages 于 11 月 11 日 GA，以业务域组织经治理的业务概念定义，可认证与废弃。Genie 插件于 11 月 11 日接通 ChatGPT、Claude 与 Grok Bot/Cursor，用户可在这些工具内经 Genie One MCP 问数；Genie One Windows 桌面应用同日进入 Beta。
- [Databricks 官方文档 11 月发布说明](https://docs.databricks.com/gcp/en/release-notes/product/2026/november)

### 3. Google 发布 Gemini Decisions API：单次请求评估最多 1,000 个问题（11/11）
Google 在 11 月 11 日发布 Gemini Decisions API，由新模型 Gemini Decision 1 驱动：单次请求可对同一多模态输入（文本、图像、音频、视频与 PDF，至多 256K token）评估最多 1,000 个独立问题，返回概率与校准置信度，端到端延迟约 150–250 毫秒，每百万输入 token 收费 0.10 美元、不收输出 token 费。API 提供三类决策原语：是否判断、多选与有序量表评分，面向工具选择、策略检查、模型路由与上下文评分等有界决策。Google 称，内部已用该 API 做 NotebookLM 的动态模型路由（日常查询延迟最多降低 40%）与 Search 的 MCP 工具安全层；在共享基准套件上，其成本约为 Gemini 3.5 Flash-Lite 加 Interactions API 的五分之一。
- [Google 官方博客（11/11）](https://blog.google/innovation-and-ai/technology/developers-tools/gemini-decisions-api/)

### 4. Cube Core 发布 v1.8.22 补丁版本（11/11）
Cube Core 在 11 月 11 日发布 v1.8.22 补丁版本：CubeSQL 新增 TRIM 与 SPLIT_PART 下推、DuckDB 的 DATEDIFF 下推，CubeStore 开始发布多架构 Docker 镜像，model-schema 包改为随每次发布一并发布；另含多项修复，包括 Oracle 驱动的库内预聚合构建与跨数据源 originalSql 连接的栈溢出修复。
- [GitHub Releases（11/11）](https://github.com/cube-js/cube/releases/tag/v1.8.22)

## 新闻网站

### 5. Rubrik：BigQuery 无代理不可变备份 GA，Google Cloud 保护扩展至 GCS（11/11）
Rubrik 在 11 月 11 日宣布把 Google Cloud 数据保护扩展至 Google Cloud Storage，并使 BigQuery 的无代理不可变备份 GA：支持整数据集或单表恢复（含视图与例程，PB 级），可就地恢复或导出至另一项目或区域，备份可存于客户自己的 Google Cloud Storage 桶或 Rubrik Cloud Vault，保留期不限（相对原生 7 天时间旅行上限）。Rubrik 称，随着智能体从试点走向生产，BigQuery 已成为智能体推理与行动所依赖的数据层；Google Cloud Storage 保护扩展预计未来数月 GA。
- [BigDATAwire 通稿（11/11）](https://www.hpcwire.com/bigdatawire/this-just-in/rubrik-extends-protection-to-google-bigquery-and-google-cloud-storage/)

## 论文 / arXiv

### 6. TIGA：用工具接地的 LLM 智能体做受控分类体系构建（arXiv 11/11 上线，11/10 提交）
arXiv 11 月 11 日上线的论文《Controlled Knowledge Engineering for Taxonomy Induction with Tool-Grounded LLM Agents and Runtime-Adaptive Policies》（arXiv:2611.13966，11 月 10 日提交）把分类体系构建建模为带显式状态与受限动作空间的迭代决策过程：智能体用可执行分类体系编辑工具、记录工具调用与理由的交互记忆，以及推理中修订的运行时自适应组织策略，另有可选全局评审器对照候选实体集与现行策略评估结果。在 4 个基准分类体系、两种 LLM 骨干上，TIGA 在多数配置中取得最强结构质量，但并非每项精度指标都占优；收益伴随 token 消耗、API 调用量与推理时间显著上升。
- [arXiv:2611.13966](https://arxiv.org/abs/2611.13966)

### 7. DocFS：把文件系统作为多模态文档问答的智能体推理环境（arXiv 11/11 上线，11/07 提交）
arXiv 11 月 11 日上线的论文《DocFS: File Systems as Agentic Reasoning Environments for Complex Multimodal Document Question Answering》（arXiv:2611.12957，11 月 7 日提交）把原始文档重组为文件系统：目录映射章节层级，显式链接连接文本与图表公式，智能体用导航、搜索与读取等文件系统工具迭代探索文档结构、定位证据。配 Qwen3.5-Plus，DocFS 在 MMLongBench-Doc 与 FinRAGBench-V 上分别比最强基线高 2.9 和 4.3 个百分点，推理速度最高快 10.3 倍、token 最多省 10.1 倍。
- [arXiv:2611.12957](https://arxiv.org/abs/2611.12957)

### 8. ARoute：面向批处理与流式的任务对齐模型路由（arXiv 11/11 上线，11/09 提交）
arXiv 11 月 11 日上线的论文《ARoute: Task-Aligned Batch and Streaming Model Routing》（arXiv:2611.13209，11 月 9 日提交）针对语义数据处理与智能体工作流的模型路由：在用户指定的成本预算下，按任务自身的正确性标准为每个请求选模型，批处理版把预期收益最大的请求路由给更强模型，流式版用小验证集校准的阈值满足成本配额并随预算消耗动态调整。在 MMLU-Pro、LiveCodeBench、SuperGPQA 与两个基于 SWAN 语义查询基准的值填充任务上，同等成本下 ARoute-Batch 在全部 15 个任务-成本设定中平均准确率最高，比最强基线平均高 4.1 个百分点、最高 11.9 个百分点；批处理完成速度比级联方法最高快 2.8 倍。
- [arXiv:2611.13209](https://arxiv.org/abs/2611.13209)

### 9. Beyond the Document：面向任意工作产品的编译上下文与受治理智能体（arXiv 11/11 上线，11/09 提交）
arXiv 11 月 11 日上线的论文《Beyond the Document: Compiled Context and Governed Agents for Any Work Product》（arXiv:2611.13055，11 月 9 日提交）提出 Portable Agent Format（PAF）包：把工作产品与编译上下文、证据、溯源及后续交互规则一并交付。在 4 个新包（投资建议、基金研究、财务报表分析、工程事故复盘）、400 个冻结问题与 12,000 条评估回答上，托管受治理阅读器成功率为 96%，高于指令加原始文件检索的 86%；在每条件 260 个可回答问题上为 94% 对 79%。论文同时指出，一处失败仍未解决：离线检索在某财务数据包的 40 个历史记录问题上全部未答出。
- [arXiv:2611.13055](https://arxiv.org/abs/2611.13055)

本期检索范围内，社交媒体与中文媒体层当日未见可核实的数据智能体新内容；监测名单内其余厂商、研究团队与评测基准机构在过去 24 小时内未见可核实的新动态；监测名单内其余开源项目当日未见实质 Release。

## 今日回顾

Databricks 在 11 月 11 日发布第二代 Always-on Genie，把 Genie 从问答助手改为常驻自主智能体，Genie Ontology 已 GA，Genie Search 覆盖 100 多个企业数据源，官方基准称任务正确率 91%；Databricks 在 11 月 12 日把 Genie ZeroOps 推入 Beta，Pages 于 11 月 11 日 GA，Genie 插件同日接通 ChatGPT、Claude 与 Grok Bot/Cursor；Google 在 11 月 11 日发布 Gemini Decisions API，单次请求可评估最多 1,000 个问题，端到端延迟约 150–250 毫秒；Cube Core 在 11 月 11 日发布 v1.8.22 补丁版本；Rubrik 在 11 月 11 日宣布 BigQuery 无代理不可变备份 GA；arXiv 11 月 11 日上线 4 篇论文，涵盖受控分类体系构建智能体（TIGA）、文件系统文档问答智能体（DocFS）、任务对齐模型路由（ARoute）与便携智能体格式（PAF）；社交媒体与中文媒体层当日未见可核实的数据智能体新内容。
