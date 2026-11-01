---
layout: post
title: "Data Agent Daily — 2026-11-01"
author: dad
date: 2026-11-01
image: "assets/images/covers/2026-11-01.svg"
description: "Databricks 与 SAP 扩大合作，把 Genie、Lakeflow、Unity Gateway 与 Lakebase 带入 SAP Databricks，并推出 SAP Application Data Foundation。"
categories: ["Data Agent Daily"]
tags: ["data-agent", "news"]
comments: false
---

## 今日速览

- Databricks 与 SAP 扩大合作，把 Genie、Lakeflow、Unity Gateway 与 Lakebase 带入 SAP Business Data Cloud 内的 SAP Databricks，并推出 SAP Application Data Foundation。
- Google 宣布 Knowledge Catalog 的扩展语义模型支持进入 GA，覆盖 Looker LookML、BigQuery Graph、dbt MetricFlow、Snowflake Semantic Views、Databricks Metric Views 与 SAP CSN。
- SAP 在 TechEd 推出 Joule Studio 与 Joule Work 的分阶段 GA，以及分层的 agent 网关能力。
- Sema4.ai 发布企业 AI Agent 平台 3.0，新增团队共享工作区与可复用的 Verified Queries、Verified Logic，公司称 Verified Queries 可少用 80% 的 LLM token、快 4 倍。
- Articul8 发布多模态决策模型 Bivia，通过 API 供企业 agent 调用，覆盖 Choice、Boolean、Score、Set、Span 五种决策原语。
- Zoho 把 Zoho Analytics 改为 Agentic Analytics 平台，Ask Zia 成为协调六个专业子 agent 的超级 agent，并内置本体与语义层，定价不变。
- Snowflake 在 10 月 28 日的文档中给 Cortex Agents 的 Coding Agent 增加三项公开控制：推理强度、附加系统指令与 stage 挂载。
- Context Labs 在 11 月 1 日发布 AI Distillery，把企业运营与业务数据转为带可验证 lineage 的、归企业所有的 Context Package，现已在 Microsoft Marketplace 上架。
- a16z 文章披露 Databricks 平台上 agent 发起的查询已超过人类，agent 每天启动数据库超过 1,700 万个；Databricks 首席执行官与 Snowflake 首席执行官随后在 X 上就相关数字公开交锋。
- 社区实战：Medium 连载用 Snowflake 托管 MCP 服务器 + Cortex Agent 复现咖啡连锁门店收入下滑 36% 的归因，脚本已在真实账号上跑通。
- 论文 / 推荐代理：Meta AI 与加州大学圣迭戈分校的 PAMO 方法（arXiv 2610.07588，10 月 6 日首投，10 月 31 日经 X 与媒体报道进入公众视野）称，4B 个人代理用跨平台历史重排 Steam 候选后，top-10 命中率从 40.8% 升至 47.9%。

## 公司发布 / 官方博客

### 1. Databricks 与 SAP 扩大合作：Genie、Lakeflow、Unity Gateway、Lakebase 进入 SAP Databricks（10/30）
Databricks 在 10 月 30 日宣布扩大与 SAP 的合作，把 Genie、Lakeflow、Unity Gateway 与 Lakebase 带入 SAP Business Data Cloud 内的 SAP Databricks，同时推出新的 SAP Application Data Foundation，用于访问 SAP 应用数据。Databricks 的说法是：业务上下文大多存在于 SAP 系统中（其称 90% 以上的财富 500 强使用 SAP 方案），而过去访问 SAP 应用数据往往意味着自建抽取管道、复制数据并丢失业务语义；新基金会改走 SAP BDC Connect 的零拷贝共享，数据工程师可直接在 SAP 的语义基础上建模。Genie 被描述为带企业上下文的 AI 助手，计划与 SAP 的 Joule 做双向连接；Lakeflow 负责 SAP 数据与 IoT、CRM 等来源的摄取与编排；Unity Gateway 提供跨 agent、工具、模型与 MCP 的治理与成本控制；Lakebase 则是面向 AI 应用与 agent 的 serverless Postgres。SAP 在 10 月 29 日 TechEd 期间也发布了自己的版本，口径基本一致，另提到 Agent Bricks。已上线的客户案例包括 SAF-Holland：其用 SAP Databricks 统一了 1 亿多条客户、交付与物料记录，Databricks 称其分析速度比传统报表快 5 倍。注意口径：扩展能力多为“计划带入”，Databricks 指引客户向 SAP 或 Databricks 客户团队咨询新基金会与扩展能力的可用情况，未给出统一的上线日期。
- [Unite.AI 报道](https://www.unite.ai/databricks-expands-sap-partnership-with-genie-lakeflow-and-lakebase/)
- [Superpower Daily 报道（10/30，含“未给发布日期”的提醒）](https://superpowerdaily.com/posts/sap-and-databricks-extend-partnership-to-bring-more-ai-tools-to-business-data)

### 2. Google：Knowledge Catalog 扩展语义模型支持 GA，agent 可直接读业务指标定义（10/30）
Google 在 10 月 30 日宣布 Knowledge Catalog 的扩展语义模型支持进入 GA：目录除原有技术元数据外，现可摄入 Looker LookML、BigQuery Graph、dbt MetricFlow、Snowflake Semantic Views、Databricks Metric Views 与 SAP CSN 的业务定义，并连成上下文图谱。Google 官方博客同步说明了其中最关键的一块：LookML 语义索引 GA 后，模型、Explore、视图、字段、看板与 lineage 自动同步进 Knowledge Catalog，Gemini Enterprise 与自定义 agent 无需另写代码即可调用；同步默认常开，生产 LookML 的更新接近实时反映。Google 举的例子是净收入这类指标：没有语义层时 agent 会自行拼 SQL 公式、漏掉 order_status = 'Complete' 之类的口径条件，还可能因多粒度 join 导致行数膨胀；有了索引后，agent 查到指标的同时就拿到它的精确定义、join 路径与 lineage。冲突处理上也有明确做法：同一指标在不同系统定义不一致时，目录同时展示两份定义与来源，由数据负责人裁决，而非静默取其一。
- [Google Cloud 官方博客：LookML 索引 GA](https://cloud.google.com/blog/products/business-intelligence/lookml-metadata-indexing-in-knowledge-catalog-is-now-ga)
- [Medium 综述：10 月 24–30 日平台动态中的 Google 部分](https://medium.com/@chameleon13/data-platforms-are-becoming-smarter-and-more-connected-but-are-they-making-business-simpler-a8183a145ca9)

### 3. SAP TechEd：Joule Studio 与 Joule Work 分阶段 GA，agent 网关分两层上线（10/27–10/30）
SAP 在 10 月 27 日柏林 TechEd 上推出一揽子企业 AI 能力：Joule Work 与 Joule Studio 开始分阶段 GA，Joule Studio 支持无代码与专业代码两种开发方式、可调用 70 多个 AI 模型，并新增 Process Consulting Agent，用表格模型 SAP-RPT-1 读取客户已有流程数据、自动给出 agent 配置建议——SAP 开发者 keynote 的说法是把约 80% 的手工配置工作压缩，典型搭建时间从 13 小时降到 2.5 小时（公司口径）。网关部分要分清两层：已有的 Agent Gateway 的入站 Agent2Agent 互通在 10 月 GA，第三方 agent 可经此调用 SAP agent；而新宣布的 SAP Enterprise AI Gateway（集中认证、策略、路由、用量与审计）按独立报道与德国 SAP 用户组 DSAG 的说法要到 2027 年第一季度才 GA，TechTimes 则称其在 2026 年第四季度 GA——两份独立报道的时间口径不一致，以 SAP 官方创新指南的分阶段表述为准更稳妥。此外，Business Data Cloud Ontology Manager（为 SAP Knowledge Graph 做领域视图）目前为 beta，Joule Studio 直连 Business Data Cloud 数据产品、经 n8n 的工作流编排等能力也排在 2027 年第一季度。
- [Frontier 分析：SAP agent 扩展与网关时间口径辨析](https://www.thisisfrontier.ai/news/sap-s-agent-expansion-moves-the-cio-choice-from-ai-tools-to-control-architecture)
- [ERP Today：TechEd 2026 上线与排期梳理](https://erp.today/sap-teched-2026-whats-rolling-out-and-whats-planned-through-2027/)

### 4. Sema4.ai 发布企业 AI Agent 平台 3.0：团队共享工作区 + 可复用已验证查询与逻辑（10/29 宣布，10/31 仍在被报道）
Sema4.ai 在 10 月 29 日宣布企业 AI Agent 平台 3.0，新增团队共享工作区：团队可在受治理的工作区内共同管理 agent、技能、记忆、数据与文件。版本的核心做法是把重复性 agent 工作从每次都由模型重新生成，改为复用客户已审核批准的代码：Verified Queries 复用已批准的数据访问模式，公司称比重复生成查询少用 80% 的 LLM token、快 4 倍；Verified Logic 复用已批准的计算、校验与转换，公司称对重复任务少用 50% 的 token、快 30%。此外，3.0 加入法务审计报告（记录每个 agent 步骤的操作前后变化）、DataFrames 大结构化数据集内存计算（不把每一行都过模型上下文）、Agent Inbox，以及与 Claude Cowork、Microsoft Copilot 的互通和 Microsoft Fabric 支持。上述提速与省 token 数字均为公司口径，未附独立测试细节。
- [Sema4.ai 官方新闻稿（10/29）](https://sema4.ai/newsroom/sema4ai-enterprise-ai-agent-platform-team-based-work-token-reduction/)
- [WebWire 通稿转载（10/29）](http://www.webwire.com/ViewPressRel.asp?aId=363502)

### 5. Articul8 发布 Bivia：不为每个判断都调用生成式模型的企业 agent 决策层（10/28）
Articul8 在 10 月 28 日发布多模态决策模型 Bivia，通过 API 提供给企业 agent 使用，定位是决策层而非生成层：agent 在执行任务中反复遇到的判断（选工具、核对事实、确认任务完成、校验文档是否符合 schema、图片是否通过检查）可直接由 Bivia 处理，而不必每次都调用生成式模型。Bivia 覆盖文本、图像、视频、表格与图表，支持 Choice、Boolean、Score、Set、Span 五种决策原语与 Fast、Fast+think、Deep 三档运行模式，并可按企业的行业知识、政策与流程定制。公司称 Bivia 建立在其平台内数十亿次决策之上，内部测试中在特定能源与硬件设计（Verilog）任务上达到 100% 准确率——该数字为公司内部测试口径，未经第三方核验，不宜外推到其他行业。Bivia 可独立以 API 形式使用，也可作为 Articul8 企业 AI 平台的一部分，公司点名的已有客户包括 Hitachi Energy、CTC、AZing 与 Megazone。
- [GlobeNewswire 通稿](https://www.globenewswire.com/news-release/2026/10/28/3390832/0/en/articul8-launches-bivia-to-bring-domain-specific-decision-intelligence-to-enterprise-ai-agents.html)
- [TechGig 报道](https://techgig.com/news/ai/articul8-launches-bivia-for-enterprise-ai-agent-decision-intelligence/135291818)

### 6. Zoho 把 Zoho Analytics 改为 Agentic Analytics 平台：Ask Zia 协调六个子 agent，本体与语义层内置（10/28）
Zoho 在 10 月 28 日宣布把 Zoho Analytics 从自助 BI 平台改为 Agentic Analytics 平台。Ask Zia 现为超级 agent，协调六个专业子 agent：数据分析、数据可视化、数据准备、公式、DSML 编码与 SQL，六个 agent 共用同一语义层、本体与对话上下文；数据分析 agent 给出描述性、诊断性与规范性三类洞察，公式 agent 把口径写成可复用指标，DSML 编码 agent 在 Code Studio 里训练与运行分类、回归、预测等模型。平台内置两层上下文：本体层映射客户、订单、产品、供应商等业务实体及其关系，语义层为每个指标与字段写描述、同义词与使用说明，另有 Scoping 把 agent 的取数范围限定在指定数据与看板内。外部接入方面，Zoho Analytics MCP 服务器提供本地与远程两种部署，另有 Claude 连接器与插件、命令行界面与可嵌入自有应用的 agent；团队也可自建自定义 agent，接入 MCP 服务器与网络搜索，并设指令与护栏。治理方面包括数据目录、沙箱与部署管理、表列行三级数据策略与 AI 可观测性（记录哪些 agent 运行、谁使用、访问了什么、如何作答）。新增 30 多个连接器，连接器总数超过 500 个，新增 SAP S/4HANA Cloud、PayPal、Adobe Commerce、Notion、Supabase 等；定价不变，每档计划新增每月 Zoho LLM 额度。云端已上线，本体与语义模型的预览按独立报道在未来 4–8 周内逐步覆盖各区域，本地部署版本排在 2027 年第一季度。
- [Zoho 官方博客](https://www.zoho.com/blog/analytics/new-zoho-analytics-agentic-analytics.html)
- [Frontier 分析](https://www.thisisfrontier.ai/news/zoho-turns-analytics-into-an-agent-context-layer-moving-enterprise-ai-control-beyond-the-model)

### 7. Snowflake：Cortex Agents Coding Agent 新增推理强度、附加系统指令与 stage 挂载三项控制（10/28 文档）
Snowflake 在 10 月 28 日的发布说明中给 Cortex Agents 的 Coding Agent 增加三项公开控制，均作用于包含 code_toolset_all 工具的 agent:run 请求。thinking_effort 设定编排模型的推理强度，可选 minimal、low、medium、high、xhigh、max，各模型只接受其中一部分，超出部分会降到该模型接受的最高档；instructions.system 是附加在受管编码 agent 提示词之上的额外系统指令，不替换沙箱、工具与技能指令；stage_mounts 把 Snowflake stage 或版本化 stage 挂载进沙箱，版本化 stage 包括 notebook、Streamlit 应用、工作区与 agent，workspace_mounts 保持不变，仍挂载可写工作区 live 版本。这三项是编码 agent 的生产控制项，不是新产品发布。
- [Snowflake 官方文档（10/28）](https://docs.snowflake.com/en/release-notes/2026/other/2026-10-28-cortex-agents-coding-agent-thinking-effort-stage-mounts)

### 8. Context Labs 在 11 月 1 日发布 AI Distillery：企业数据转为归企业所有的 Context Package（11/01）
Context Labs 在 11 月 1 日（阿布扎比，PR Newswire 通稿）发布 AI Distillery，定位为面向可信主权 AI 的 Context Engine：把企业的运营与业务数据转为受治理的 Context Package，归企业所有，并附可验证的 lineage。平台把结构化与非结构化数据映射到行业本体，Context Package 中的每个答案可追溯回源记录，平台在模型进入生产前先用企业自身记录校验答案；客户可自选前沿模型或开源权重模型，运行在自有数据中心或自选云上。产品现已通过 Microsoft Marketplace 上架，每个企业许可附带一个行业 starter kit；公司正在 ADIPEC 2026 上用能源场景演示，Context Agent 回答运营问题时每个数字追溯到工厂记录。通稿未披露定价与已签约客户，准确率与处理吞吐量也未公布基准数字。
- [PR Newswire 通稿（11/01）](https://www.prnewswire.co.uk/news-releases/context-labs-ai-distillery-lets-enterprises-run-sovereign-ai-on-data-they-own-302925657.html)
- [Wisevoter 报道（11/01）](https://wisevoter.com/world/2026/11/01/context-labs-launches-ai-distillery)

## 新闻网站

### 9. a16z 文章披露 Databricks 平台数据：agent 查询量已超人类，每天启动数据库超 1,700 万个；两家 CEO 随后在 X 上交锋（10/27 文章，10/29 交锋）
a16z 在 10 月 27 日发表《Databricks & the Future of the Firm》，首次披露了 Databricks 平台的 agent 用量数字：agent 发起的查询已超过人类，agent 每天启动数据库超过 1,700 万个，而三年前平台上的全部交互都来自人类。文章称 agent 活动 feeding 的产品线是 Lakebase（随 2025 年 5 月约 10 亿美元收购 Neon 而来），其年化收入已过 1 亿美元，约占 Databricks 70 亿美元总年化收入的 1.4%；Lakehouse 仓储线年化收入已过 15 亿美元、年增速超 100%。另据文章引用的 Databricks 自述，基于企业本体做 grounding 后，回答准确率在其自有测试中从约 50% 提升到 84.5%。提醒：a16z 是 Databricks 的早期投资方（领投了 2013 年 A 轮）且作者 Ben Horowitz 担任 Databricks 董事，数字为利益相关方披露，未经审计；Databricks 8 月融资时估值为 1,900 亿美元，年化收入 70 亿美元。10 月 29 日，Snowflake 首席执行官 Sridhar Ramaswamy 在 X 上引用该文要求 Databricks“公布全部数字”，并质疑剔除透传推理收入后 80% 的年增速是否会降至 65%；Databricks 首席执行官 Ali Ghodsi 回应称两家公司互补，并称使用 Unity Gateway 的客户近几个月 token 支出减少约 30%，同时 token 总量上升。
- [The Inference 报道](https://theinference.org/article/agents-launch-17-million-databases-a-day-on-databricks-the-line-they-feed-makes-100-million)
- [Analytics India Magazine：两家 CEO 的 X 交锋（10/29）](https://analyticsindiamag.com/ai-news/youre-not-doing-this-ai-stuff-databricks-ceo-tells-snowflake)

## 社交媒体

### 10. Medium 连载：用 Snowflake 托管 MCP 服务器 + Cortex Agent 做门店归因，脚本真实跑通（10/31–11/1）
Pranav Katyayen 在 Medium 上线的 Snowflake AI 实战连载首集，用一个 SQL 脚本搭起 Snowflake 托管 MCP 服务器，让 Claude 与 Cursor 经 Cortex Agent 查询受治理的数据并做归因：案例是 Snowbrew Coffee 涩谷门店 9 月收入下滑 36%，agent 先从销售数据取数，再读日文客户投诉找原因。作者称全部脚本已在真实 Snowflake 账号上多次端到端跑通，并如实记录了踩坑点：新账号会屏蔽旧版 Cortex 函数、OAuth 拒绝 ACCOUNTADMIN、新建 Streamlit 应用默认的运行时与文档不一致。连载定位是“每个实验都真实跑通”，下一集计划让 agent 在 Snowflake 内写代码、跑代码并部署应用，且每次改动前都会征求许可。
- [Medium 首集](https://medium.com/@katyayen.pranav/i-asked-claude-why-our-coffee-sales-crashed-it-answered-from-snowflake-with-zero-backend-code-d5ab12b753ea)
- [Medium 连载总览](https://medium.com/@katyayen.pranav/snowflake-ai-hands-on-a-series-where-every-lab-actually-runs-2998ded73055)

## 论文 / arXiv

### 11. 推荐代理：Meta AI 与 UC San Diego 的 PAMO，4B 个人代理用跨平台历史重排推荐（论文 10/6 首投，10/31 进入公众讨论）
Meta AI 与加州大学圣迭戈分校的研究者提出的个人代理中介推荐方法 PAMO，在 10 月 31 日经 X 帖子与 FourWeekMBA 报道进入公众讨论；论文本身首投于 10 月 6 日（arXiv 2610.07588），标题为《Personal-Agent Mediated Recommendation with Cross-Platform User History》。方法设定是：平台先用自有数据做排序，用户的个人代理再用用户授权的跨平台历史对排序做编辑，PAMO 在训练中遮蔽跨平台历史以判断哪些回答真正依赖它，只在排序质量不下降时给这类回答更高奖励。在真实跨平台 Steam 测试（645 名用户，目标平台为 Steam，跨平台历史来自 Nintendo 与 Xbox）中，基于 Qwen3-4B-Instruct 的 PAMO 代理 top-10 命中率 47.9%，高于平台排序的 40.8% 与 Claude Opus 4.6 的 45.4%；有害覆盖率 6.0%，低于 Claude Opus 4.6 的 9.0%。限制同样写在报道里：测试只覆盖 645 名用户与 Steam 一个目标平台，平台排序为研究者自建而非 Steam 真实推荐器，论文未说明 Meta 有产品在使用该方法；论文为预印本，未经同行评审。
- [FourWeekMBA 报道（10/31，含论文数据与限制）](https://fourweekmba.com/ai-meta-paper-a-4b-personal-agent-lifted-game-picks-to-47-9/)
- [arXiv 论文页](https://arxiv.org/abs/2610.07588)

说明：本期为 11 月 1 日晚间更新重发版，新增第 6、7、8 条（Zoho、Snowflake Cortex Agents 控制、Context Labs），其余条目与首发版一致。本次扩充检索覆盖了 watchlist 监测名单主体、arXiv 与 Hugging Face Papers 方向及新增关键词。10 月 31 日 DeepSeek Harness 团队发布的 Super-agent 为编码 agent 原型（MIT 许可的 dsh-superagent-prototype），不在 Data Agent 主题的直接收录范围内，故未列入本期头条序列；本次检索范围内未见 10 月 31 日至 11 月 1 日首投的、与 Data Agent 直接相关的新 arXiv 论文，上述 PAMO 一条以 10 月 31 日的公开讨论为收录依据、论文首投日期已如实标注。今日检索未见 Microsoft、dbt Labs、Hex、ThoughtSpot、Wren AI 官方博客在过去 24 小时内发布新的 Data Agent 专帖。

## 今日回顾

Databricks 与 SAP 扩大合作，把 Genie、Lakeflow、Unity Gateway 与 Lakebase 带入 SAP Databricks，并推出 SAP Application Data Foundation；Google 知识目录的扩展语义模型支持进入 GA；SAP 在 TechEd 推出 Joule Studio 与网关能力；Sema4.ai 发布企业 AI Agent 平台 3.0；Articul8 发布企业 agent 决策模型 Bivia；Zoho 把 Zoho Analytics 改为 Agentic Analytics 平台，Ask Zia 协调六个子 agent；Snowflake 给 Cortex Agents 的 Coding Agent 增加三项公开控制；Context Labs 在 11 月 1 日发布 AI Distillery；a16z 文章披露 Databricks 平台上 agent 查询量已超过人类，两家 CEO 随后在 X 上交锋；社区实战连载用 Snowflake 托管 MCP 服务器完成门店归因；Meta AI 与 UC San Diego 的 PAMO 推荐代理方法在 10 月 31 日进入公众讨论。
