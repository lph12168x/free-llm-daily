# 免费大模型日报 · 2026-09-29（周二）

> 🤖 AI 每日免费情报 · 全网挖掘 · [在线版 HTML](daily-free-llm-2026-09-29.html)

**今日四个关键数字**

| 数字 | 含义 |
| --- | --- |
| **$2 / $10** | Anthropic 发布 **Claude Sonnet 5.5**：**比 Sonnet 5 快 30%+、单任务成本最高省 30%**，Terminal-Bench 4.0 **70.6%**（Sonnet 5 仅 10.3%），**并已成为 Claude 免费档模型**（客户端免费用，API 侧全部付费） |
| **21 → 20** | OpenRouter 零价池再减 1：`ling-3.0-flash-fin:free` 退场；**Nex-N2.5 免费版正式 EOL（9/25 弃用），两条付费 SKU 今日回归**——上期「连付费版一起消失」的结论被推翻 |
| **日榜第一** | 匿名免费模型 **Space Bunny Alpha 登顶 OpenRouter 日榜**（4.32T +8%），周榜 13.86T 第 3；**中国模型周调用 62.22 万亿 tokens，连续 22 周超过美国**（14.2 万亿） |
| **82 → 83** | OpenCode Zen 新增付费 `claude-sonnet-5-5`；**免费行仍 10 款、免费 ID 11 个**；`LongCat 2.5 Preview Free` 与 `Space Bunny Free` 均为**零保留条款** |

---

## 🔥 今日头条 · 三条主线

### ① 新模型 · 且直接进免费档｜Anthropic 发布 **Claude Sonnet 5.5**：**$2 / $10**、快 30%+、省 30%，**并成为 Claude 免费档模型**

**今天最值得「免费用户」关注的一条，不是又一个匿名 stealth 模型，而是一家头部实验室把自己的中端旗舰直接放进了免费档。**

当地时间 9/28（北京 9/29），Anthropic 发布 **Claude Sonnet 5.5**——它是 **Claude 5.5 家族的第二款**（第一款是 9/23 的 Opus 5.5）。

**💵 定价：一分没涨，但「实际更便宜」**

- 官方定价**与 Sonnet 5 完全相同**：**输入 $2 / 百万、输出 $10 / 百万、缓存读取 $0.20 / 百万**；
- 但官方强调**因效率提升，执行同一个任务的实际成本最高可降 30%**——**这是「按任务算账」而不是「按 token 标价」的定价话术，也是当前行业最主流的一种隐形降价**；
- OpenRouter 侧同步上架 `anthropic/claude-sonnet-5.5`（$2 / $10，缓存读 $0.20，**1M 上下文**，文本+图像+文件输入）与 `anthropic/claude-sonnet-5.5:batch`（批量再 5 折：**$1 / $5**）。

**📈 跑分：一个「跳变」级别的数字**

- **Terminal-Bench 4.0：Sonnet 5.5 拿到 70.6%，而上一代 Sonnet 5 只有 10.3%**——**六倍多的差距，这一栏几乎是跨代**；
- 官方称它在 **GDPval-AA 上与 Opus 5.5 只差 2 分以内**，定位是「**Opus 5.5 的低成本替代与互补**」；
- 能力表述：**长周期任务、图像理解、知识工作（文档 / 演示 / 表格）均增强**；**首次在 Sonnet 系列引入类似高性能模型的网络安全防护措施**。

**🎁 真正的免费点：它是 Claude 免费档的模型**

- **Sonnet 5.5 现在就是 Claude 免费档（free tier）所用的模型**；
- 也就是说——**你不需要绑卡、不需要 API key，在 claude.ai 网页 / 客户端上就能免费用到 Sonnet 5.5**——**对「量大 + 能用 + 先进」这三个要求，这是今天最直白的一条**；
- **⚠️ 但要说清边界：免费的是「客户端」而不是「API」**。走 API 的入口（OpenRouter、OpenCode Zen、Bedrock、Claude Platform on AWS、AWS GovCloud）**全部是付费的**，不存在 Sonnet 5.5 的免费 API。

**🧭 该拿它做什么**

1. **想白嫖：直接用 claude.ai 免费档**——适合交互式写作、代码调试、表格 / 文档处理。这是今天新增的一条「零成本先进模型」通道；
2. **想接 API：把它当成「比 Opus 5.5 便宜很多、但差距很小」的那一档**——$2/$10 对比 Opus 5.5 的 $4/$20，**价格一半、分差 2 分以内**，是性价比区间里很硬的一条；
3. **Agent / 长任务：Terminal-Bench 4.0 的 70.6% 意味着它在终端类编码任务上已经可用**，配合批量版 5 折，适合放进批量流水线。

> **同时宣布的**：**Haiku 5.5「即将推出」**，官方定位「**面向快速、高吞吐量任务**」——**Claude 5.5 家族的第三款，也是未来最可能落在免费档 / 低价档的一款，值得盯。**
> **为什么这条对「免费日报」也重要**：过去两三周的免费池主线是「**匿名 stealth 模型空降 → 一周后消失**」（ox-alpha 6 天、union-alpha 不到 2 天、Space Bunny 一周）。**Sonnet 5.5 走的是完全相反的路：具名、有官方文档、有长期定价、而且把免费档作为分发入口**——**对使用者而言，「有名有姓、有付费路径」的免费档永远比 stealth 更值得放进生产链路。**

### ② 免费池流水｜OpenRouter 零价池 **21 → 20**：`ling-fin:free` 退场；**Nex-N2.5 免费版正式 EOL，付费版今天回归**

**上期我们写「nex-n2.5 连付费 SKU 一起整体消失」。今天这条被自己推翻了——付费版回来了，免费版确认永久退场。**

脚本清点：目录 **458 涨到 460 款（+2）**，零价池 **21 掉到 20（−1）**、带 `:free` 后缀 **17 掉到 16（−1）**。

**📤 今天掉的：一条只活了一周的新免费档**

- **`inclusionai/ling-3.0-flash-fin:free`（262K ctx）**退出零价池；
- 它是蚂蚁 inclusionAI 的金融领域版 Flash，**作为免费档存在的时间只有大约一周**（9/22 前后进池、今天出池）；
- **⚠️ 一个容易搞混的点：Zen 侧的同名免费档 `ling-3.0-flash-fin-free` 仍在架**（官方定价页仍是 Free 行）。**所以这是「聚合平台（OpenRouter）侧退出」，不是「模型下线」。**

**📥 今天进的：两条付费 SKU 回归 + Sonnet 5.5**

- ① **`nex-agi/nex-n2.5-mini`（$0.025 / $0.10，缓存 $0.0025）与 `nex-agi/nex-n2.5-pro`（$0.075 / $0.25，缓存 $0.015）双双回归**——**都是付费版，262K ctx，图文输入**；
- ② **`anthropic/claude-sonnet-5.5` + `:batch`**（见头条①）；
- **零价侧今天补位 0 条**；另下架 `deepseek/deepseek-r1-distill-llama-70b`（老蒸馏模型）。

**🔬 Nex-N2.5 的完整生命周期（本期最有价值的复盘）**

| 时间 | 事件 |
| --- | --- |
| **9/9** | `nex-n2.5-mini:free` / `-pro:free` 上线 OpenRouter 免费池（262K、agentic coding、图文） |
| **9/24** | 免费版仍在架，但**付费 SKU 下架**（我们当时写「free 仍在架，非整体消失」） |
| **9/28 上午** | 免费版退场，我们据此写「**连付费 SKU 一起整体消失**」 |
| **9/29（今天）** | **付费 SKU 回来了、免费版确认 EOL**（第三方记录弃用日期为 **2026-09-25**） |

**结论：免费试用期约 2 周 → 免费版永久退场 → 付费版随后回归。这条序列比任何单日快照都更能说明「免费档的真实寿命」。**

**🌐 聚合站滞后：本期又有两个新实证**

- **① freellm.net 的 OpenRouter 免费页仍把 `ling-3.0-flash-fin:free` 标为 Online（21 款）**，而该条今天已从官方目录退出——其页面标注「Last Updated 2026-09-27」，**滞后约 2 天**；
- **② rival.tips 已正确标注** nex-n2.5 mini / pro 的免费版为 **EOL** 并给出弃用日期 **2026-09-25**，**这次它比 freellm.net 更新快**；
- **读法不变：任何「是否还在免费」的判断，一律以官方接口 / 官方定价页为准。**

**零价池近五期流水（脚本口径：输入与输出同时为 $0）**

| 日期 | 目录总量 | 零价池 | 其中 `:free` | 零价净增减 |
| --- | --- | --- | --- | --- |
| 9/22 | 445 | 24 | 21 | — |
| 9/23 | 454 | 24 | 21 | +0 / -0 |
| 9/24 | 457 | 24 | 20 | +1 / -1 |
| 9/28 | 458 | 21 | 17 | +0 / -3 |
| **9/29（今天）** | **460** | **20** | **16** | **+0 / -1** |

**连续两期净减（9/28 −3、9/29 −1），累计已从 24 掉到 20。** 而目录总量五期涨了 **15 款**——**新增能力持续全部放进取费侧，「免费池收缩」已从单日信号变成趋势。**

**1M 上下文且 $0 的条目（今天 7 条，与上期持平）**：`stealth/space-bunny-alpha`（1,000,000）、`nvidia/nemotron-3.5-lightning:free`（1,000,000）、`nvidia/nemotron-3-ultra-550b-a55b:free`（1,000,000）、`thinkingmachines/inkling:free`（1,048,576）、`thinkingmachines/inkling-small:free`（1,048,576）、`google/lyria-3-pro-preview`（1,048,576，输出音频）、`google/lyria-3-clip-preview`（1,048,576，输出音频）。

### ③ 榜单｜**Space Bunny Alpha 登顶 OpenRouter 日榜**：免费模型把付费模型挤到身后——**中国模型连续 22 周领跑全球**

**一条 $0 的匿名模型，昨天成了 OpenRouter 全站调用量第一名。** 这不是营销话术，是榜单事实——也是本期「免费模型到底有多大需求」最直接的证据。

**📊 日榜（截至 9/28）：免费模型第一**

| 排名 | 模型 | 作者 | tokens | 环比 |
| --- | --- | --- | --- | --- |
| 1 | **Space Bunny Alpha（$0）** | stealth | **4.32T** | +8% |
| 2 | DeepSeek V4.1 Flash | deepseek | 3.68T | +7% |
| 3 | MiMo-V2.6-Flash | xiaomi | 1.43T | +16% |
| 4 | GLM 5.3 Flash | z-ai | 1.32T | +29% |
| 5 | GPT-5.6 Luna | openai | 1.29T | +15% |
| 7 | Nemotron 3 Ultra (free) | nvidia | 964B | −4% |

**📈 周榜（截至 9/27）：Space Bunny 第 3**

- ① DeepSeek V4.1 Flash **19.58T**（连续两周第一）
- ② GLM 5.3 Flash **16.32T**
- ③ **Space Bunny Alpha（$0）13.86T**
- ④ DeepSeek V4 Flash 0731 11.17T
- ⑤ Hy4 preview 9.64T
- ⑥ GPT-5.6 Luna 8.54T
- ⑦ **Nemotron 3 Ultra (free) 5.7T**（**前十唯一「长期免费」条目**）
- ⑧ MiMo-V2.6-Flash 5.51T
- **月榜**：GLM 5.3 Flash 57.5T 第一，Space Bunny Alpha 18.2T 进前十（new）

**🇨🇳 中国模型：连续 22 周超过美国**

- 按 OpenRouter 数据测算（**9/21–9/27**）：**中国大模型周调用量 62.22 万亿 tokens，美国 14.2 万亿 tokens——中国连续 22 周位居全球第一**；
- 上周全球总调用量 **146 万亿 tokens**（环比 +13.18%）；
- **前五里三款是中国模型**（DeepSeek V4.1 Flash、GLM 5.3 Flash、Hy4 preview）；
- **作者份额：DeepSeek 以 24.4% 的文本请求占比领跑**（本周起始 9/21）。

**⏰ 别忘了：这条免费通道本周就到期**

- **Space Bunny Alpha 的「限时免费一周」按 9/23 起算，窗口约在 9/30 结束——今天只剩 1～2 天**；
- **它现在是「日榜第一」但「随时转付费或消失」**——**stealth 类模型的窗口由负载与商业决策决定，不由日历决定（ox-alpha 6 天、union-alpha 不到 2 天）**；
- **要做的事很简单：如果它还在你的评估列表里，今天跑完；不要在 9/30 当天才动手。** Zen 侧入口 `space-bunny-free`，OpenRouter 侧 `stealth/space-bunny-alpha`（**这条 ID 不带 `:free`**）。

> **为什么免费模型能冲到第一**：因为这些流量来自**编码 agent**——Cline、Claude Code、Hermes Agent、Kilo Code 这类工具**单个会话就能消耗几亿 tokens**。**对它们来说，「$0 且 1M 上下文」是唯一能把 agent 长流程跑通的组合。** 免费档不是「试试看」的赠品，**而是正在替一部分真实生产负载承担推理成本**——这也是平台开始收缩免费池的根本原因。

## 🌤️ 次要更新 · 值得记一笔

### 🛡️ NVIDIA 开源 OpenShell 0.1.0 + 推出 Open Agent Safety Platform（100+ 合作方）

**9/28，英伟达正式开源 AI Agent 运行时平台 OpenShell 0.1.0**，核心思路是：**不改 agent 自身代码，在工作负载外部建立安全边界与运行时控制**——用**内核级沙箱 + 形式化策略验证**给 agent 划出「允许做什么」的硬边界。

同一天，英伟达发布 **Open Agent Safety Platform**：**OpenShell 负责运行时 containment 策略，Sentry 在 BlueField-4 DPU 上监控网络流量、拦截越权与横向移动**。**首批已有 100+ 合作方加入**，包括微软、Anthropic、xAI、Perplexity 与 Andrew Ng 的 OpenWorker；英伟达称**该平台能阻止此前 Hugging Face 被攻击的那类事件**。

- **为什么免费日报要记它**：过去一周密集出现「**agent 逃出沙箱、越权访问外部站点、经 DNS 向外传数据**」类事件。**如果你在跑免费模型做 agent，这条是「自己那台机上怎么兜底」的最实用参照——而且是开源的、可自部署的。**
- **连带一条信号**：英伟达董事会批准**把股票回购授权再增 1500 亿美元、总额升至 2350 亿美元**——与「AI 数据中心需求仍在加速」的持续表态一致。

### 🧠 Google 推 Gemma 4 12B：编码器无关架构 + 原生音频，16GB 笔电可跑

**Google 发布 Gemma 4 12B**——定位「**把先进 AI 从云端搬进笔记本**」的中量级多模态模型：

- **「编码器无关（encoder-free）」架构**：**不再为音频、视频各配一个独立编码器**，多模态数据直接喂进主干，**降低延迟与内存占用**；
- **Gemma 家族首个原生支持音频输入的中量级模型**（文本 + 图像 + 视频 + 音频）；
- **约 16GB 内存的笔记本即可本地运行**，面向 agentic 工作流：**函数调用、结构化 JSON 输出、系统指令**全部支持。

**🔗 与免费池的关系**：OpenRouter 免费池里已有 **`google/gemma-4-26b-a4b-it:free` 与 `google/gemma-4-31b-it:free`**（均 262K，图文视频输入）。**Gemma 系列是「可本地跑 + 有免费托管档」少见的双通道开源族**——想省钱又有隐私要求时，这条路很实用。
**⚠️ 提示**：官方给 26B / 31B 明确标注「暂无公开编码 / RAG benchmark」，**能力请以自己实测为准，别把下载量当成分数。**

### 💸 降价二连：DeepSeek V4.1-Flash 谷时输出 $0.60、阿里 Qwen-Audio 语音降价 70–95%

- **① DeepSeek 价格**：**V4.1-Flash 谷时输出降至 $0.60 / 百万 tokens，比 V4-Pro 低约 70%**；同时有报道称 **DeepSeek 年化营收（ARR）已突破 10 亿美元，正筹备科创板（STAR Market）IPO**。**谷时窗口延续到 10/10。**
- **② 阿里 Qwen-Audio 3.1**：**语音 API 全线降价 70–95%**——**中国大模型价格战正式打到「语音」这条线**，此前降价主要发生在文本与多模态上。
- **③ 另外两条**：**Grok 4.7 登陆 Amazon Bedrock**（500K 上下文、low→xhigh 四档推理强度，走 Responses / Chat Completions / Converse 三协议）；**Meta 成立 Meta Enterprise Platform**（前 MongoDB CEO CJ Desai 挂帅，主推 Muse 系列 agent，**官宣阵容里没有 Llama**）。

> **读法：降价 + 开源 + 平台化，这三件事同时发生，意味着「从 $0 到几乎不要钱」的区间正在被迅速填满**——**免费档收缩的另一面，是低价档变得非常便宜。**

### 🧰 两个新免费网关：BazaarLink（2 款免费模型）与 ModelBridge（50 万 tokens/月）

- **① BazaarLink（bazaarlink.ai）**：**2 款启用中的免费模型**——`qwen/qwen3.7-flash` 与 `deepseek/deepseek-v4-flash-0731free`；**免绑卡**；共享额度：**未充值 10 RPM + 50 加权单位/日，充值后 20 RPM + 100 单位/日**，每日 00:00 UTC 重置，**免费账号 2 个并发**。
- **② ModelBridge（aibridge-api.com）**：**免费档 50 万 tokens/月 + 一次性 50 万新客奖励**，**免绑卡**，**港节点，专注中国模型**（DeepSeek / Qwen / GLM / Kimi）。
- **③ 老面孔更新**：**AIHubMix 免费池仍是 60 款 / 16 家作者**，**免卡先送 10 次试用**；**一次性充 $1 后切永久日额度：100 请求/日 + 10 请求/分 + 100 万 tokens/日，每天重置**。

**⚠️ 纪律不变**：这类聚合网关**上游不透明、无 SLA**，只适合试验与个人项目。**额度会互相牵连、随时可改、随时可关**——**不要把带生产 key 的请求发给来路不明的网关。**

### 📈 榜单补充：免费档在 freellm.net 核验榜的位置

**freellm.net 核验榜（更新 2026-09-29）：502+ 款 / 31 家平台 / 235 款实时验证 / 415+ 免绑卡**（较 9/28：505+ → 502+、417+ → 415+，属正常波动）。

- 榜首仍是 **NVIDIA NIM `z-ai/glm-5.3`（96 分，1.3M、40 RPM）**；次席 **`z-ai/glm-5.3-flash`（95 分，周吞吐 271.7B）**；
- **OpenRouter 的 `Ling 3.0 Flash Sante (free)` 95 分第 3（周吞吐 331.3B）**、`Qwen3.8 27B (free)` 93 分第 4、Ollama Cloud `deepseek-v4-pro` 92 分第 5；
- 其后 **NIM `Kimi K3` 90**、**Gemini 3.8 Flash 90**、**Zen `Qwen3.8 Max` 88**、**Zen `GLM-5.3` 87**。
- **⚠️ 滞后实证（本期新增）**：该站的 OpenRouter 免费页**仍把今天已退场的 `ling-3.0-flash-fin:free` 标为 Online（显示 21 款）**，而其页面自身标注「Last Updated 2026-09-27」——**滞后约 2 天**。**把这类站点当「发现新模型」的入口没问题，但「是否仍在免费」必须回官方复核。**

## 🧾 今日免费入口速查 · 先进 + 量大优先

| # | 入口 | 免费额度 | 模型量级 | 状态 / 注意 |
| --- | --- | --- | --- | --- |
| ① | **Claude Sonnet 5.5**（claude.ai 免费档） | **客户端免费用**（免绑卡 · **API 无免费**） | 中端旗舰、**TB 4.0 70.6%** | **今天新增**；免费仅限 claude.ai 客户端，API 侧（OR / Zen）全部付费；比 Opus 5.5 便宜一半、分差 2 分内 |
| ② | **OpenRouter** `nemotron-3-ultra-550b-a55b:free` | $0 / $0（200 请求/日） | 550B / 激活 55B、**1M** | Nvidia 端点；**周榜 5.7T 第 7，前十唯一长期免费**；**勿提交个人 / 机密数据** |
| ③ | **Space Bunny Alpha**（OpenRouter / Zen） | $0 / $0，**约 9/30 到期、剩 1–2 天** | **1M** / 文本+图+视频 | 疑似 MiniMax M3.1 系；**日榜第一（4.32T）**；ID 不带 `:free`；**今天就跑完** |
| ④ | **LongCat 2.5-Preview**（Zen，9/28 新增） | **四列全 Free**（限时） | 1.6T / 激活 48B、**1M + 原生多模态** | **零保留、不用于训练**；美团具名厂商，免费期结束转付费而非断供；官方另送老用户 500 万 tokens |
| ⑤ | **智谱 z.ai**（永久免费档 + 双节活动） | **输入输出全 Free** + 夜免至 10/7 | `GLM-4.7-Flash` 等、国内直连 | **唯一可以写进长期依赖的一类**；9/25–10/7 全天五折 |
| ⑥ | **NVIDIA NIM**（长期兜底） | 40 RPM、**不限调用量** | `glm-5.3`（1.3M）与 Kimi K3（1M） | freellm.net 榜首来源（96 分）；**需手机验证** |
| ⑦ | **Dots3-Note Preview**（9/30 到期，剩 1–2 天） | $0 / $0（至 2026-09-30） | 280B / 激活 16B、512K / 图文 | 支持 tools / structured_outputs；**今天就得跑** |

**📌 长期兜底组合（无到期日那一类）**

- **智谱 z.ai** — `GLM-4.7-Flash` / `GLM-4.5-Flash` / `GLM-4.6V-Flash` **输入输出全 Free，无到期日**（国内直连）。
- **Claude Sonnet 5.5** — **claude.ai 免费档可用**，无到期表述；**但仅限客户端，无免费 API**。
- **书生 InternLM** — **1.8 亿 tokens/月、免信用卡、无明确到期日**。
- **美团 LongCat** — **每天 5,000 万 token**（官方平台）。
- **Cerebras** — **每天 100 万 token**；**Cloudflare Workers AI** — **每天 1 万 neurons**。
- **OVHcloud AI Endpoints** — **匿名免注册 9 款**，2 RPM。
- **FreeLLMAPI（自托管，MIT）** — **34 家 / 635 端点 / 约 7.4 亿 tokens·月**，一条命令起本地网关。

> **组合建议**：**主力**用一条稳的（NIM / 智谱永久免费档 / claude.ai 免费档），**兜底**用无到期日的（LongCat / InternLM），**试用**用限时券与 stealth（Space Bunny / Dots3 / LongCat 2.5）。免费池已连续收缩两期，**「付费兜底」这一层今年值得认真算一次成本。**

## 🔎 平台盘点 · 今日快照

### 📊 OpenRouter：**460 款中 20 款零价**（`:free` 16 款）

- 脚本清点时刻：**460 款（较 9/28 +2）**，其中**输入与输出同时为 $0 的共 20 款**（较 9/28 **−1**），**带 `:free` 后缀 16 款**（**−1**）。
- **零价池退出一条**：`inclusionai/ling-3.0-flash-fin:free`（**262K，免费档只活了约一周**；**注意 Zen 侧同名免费档仍在架**）。
- **零价池新进 0 条。** 总量新增 **`anthropic/claude-sonnet-5.5` 与 `:batch`、`nex-agi/nex-n2.5-mini`、`nex-agi/nex-n2.5-pro`**（**后两条是付费 SKU 回归**）；下架 `deepseek/deepseek-r1-distill-llama-70b`。
- **四条「零价但不带 `:free`」**：`stealth/space-bunny-alpha`（**1M 三模态**）、`google/lyria-3-pro-preview`、`google/lyria-3-clip-preview`（**后两条输出音频**）、`openrouter/free`（200K 自动路由池）。
- **1M 且 $0 的条目 7 条，与上期持平。**

### 🔧 OpenCode Zen：**82 → 83 款**（+`claude-sonnet-5-5`），免费 ID **11 个**

- `/zen/v1/models` 返回 **83 款**（较 9/28 的 82 款 +1，**零下架**）。新增 **`claude-sonnet-5-5`**（**付费**，对应官方定价页 Claude Sonnet 5 一档 $2.00 / $10.00、缓存读 $0.20）。
- 带免费标记的 ID 仍 **11 个**：`jev-1.13-free`、`deepseek-v4-flash-free`、`muse-spark-1.3-contributor-free`、`muse-spark-1.2-contributor-free`、`mimo-v2.6-flash-free`、`space-bunny-free`、`longcat-2.5-preview-free`、`mimo-v2.5-free`、`ling-3.0-flash-fin-free`、`nemotron-3-ultra-free`、`nemotron-3.5-lightning-free`。
- 官方**定价页 Free 行 10 款**（Big Pickle、Space Bunny、LongCat 2.5 Preview、MiMo-V2.6-Flash、MiMo-V2.5、Ling 3.0 Flash Fin、Nemotron 3 Ultra、Nemotron 3.5 Lightning、Muse Spark 1.3 Contributor、Jev 1.13 Free）。
- 📖 **数据条款三类必须分清**：**Space Bunny / LongCat 2.5 = 零保留、不用于训练**（最干净）；**Big Pickle / MiMo / Ling = 免费期数据可能用于改进模型**；**Nemotron 两条 = NVIDIA 试用端点，明确勿传个人 / 机密数据**。
- ⏰ 旧版下线提醒：**小米 `mimo-v2.5-pro` / `mimo-v2.5` 将于 10/21 10:00 下线**，`mimo-v2.5-free` 受此影响——**尽快切 `mimo-v2.6-flash-free`。**

### 🌐 freellm.net：**502+ 款 / 31 家平台 / 235 款实时验证 / 415+ 免绑卡**

- 核验时间 2026-09-29（较上期：505+ → **502+**、417+ → **415+**，属正常波动）。榜首 **NVIDIA NIM `z-ai/glm-5.3`（96 分）**、次席 **`z-ai/glm-5.3-flash`（95 分）**。
- **OpenRouter 的 `Ling 3.0 Flash Sante (free)` 95 分第 3（周吞吐 331.3B）**、`Qwen3.8 27B (free)` 93 分第 4、Ollama Cloud `deepseek-v4-pro` 92 分第 5、NIM `Kimi K3` 90、Gemini 3.8 Flash 90、Zen `Qwen3.8 Max` 88、Zen `GLM-5.3` 87。
- **⚠️ 滞后实证（本期新增）**：其 OpenRouter 免费页**仍把今天已退场的 `ling-3.0-flash-fin:free` 标为 Online（显示 21 款，官方目录已是 20 款）**，页面自身标注「Last Updated 2026-09-27」——**滞后约 2 天**。同类 **rival.tips 这次更新更快**（已正确标注 nex-n2.5 free 为 EOL）。
- **用法建议**：把它当「**发现新模型与新平台**」的入口（收录广度确实好），**但任何关于「是否还在免费」的判断，一律回官方定价页或官方 API 复核。**

## 📅 到期日历 · 别踩空

### 📅 眼前这两天（最密集）

- **约 9/30（剩 1–2 天）** — **Space Bunny Alpha 的「限时免费一周」窗口**（按 9/23 起算）；**stealth 池历史上常提前关闭，今天就该跑完**。
- **9/30（剩 1–2 天）** — **Dots3-Note Preview 免费档到期**；**阿里 Qoder × Qwen3.8-Flash 免费用结束**；**腾讯 Hy3 / 文心 4.0 全系列免费期结束**；**上海电信 AI Store 2500 万额度领取截止**；**杭州千问办公 Token 卡现场领结束**；**Merge Gateway GLM-5.3-Flash 1 折结束**。
- **10/7** — **智谱 GLM-5.3-Flash 夜间畅用 + 全天五折结束**；**MiniMax Code 双倍签到结束**（均有延期可能，以官方为准）。

### 📅 10 月及以后

- **10/10** — **DeepSeek 低谷价窗口结束**；**腾讯混元 Hy4 preview**（老用户夜间免费）结束；unbiased.ai Pareto 正式发布（即 union-alpha 真身）。
- **10/14** — 珠海算力券申报截止（企业向）。
- **10/15** — **阶跃 Step 5 Preview 释放完整 BF16 权重**（许可证待公布）。
- **10/17** — 豆包全用户 30 天订阅（9/24 那轮）截止。
- **10/21（10:00）** — **小米 `mimo-v2.5-pro` / `mimo-v2.5` 正式下线**，Zen 的 `mimo-v2.5-free` 受影响。
- **11/7** — MiniMax 开放平台 M3 / M2 免费试用到期。
- **12/31** — 腾讯云 TokenHub / 华为云码道 / 移动云 MoMA 年度额度截止；微信小程序成长计划二期报名截止。

## 🧭 今天该怎么动

### ① 现在就做（5 分钟内）

**今天有一条「马上能用」的免费新增，和一条「马上要没」的免费存量。**

- **第一件：去 claude.ai 免费档试一下 Sonnet 5.5。** 这是今天唯一一条**「头部实验室先进模型 + 零成本 + 无需绑卡」的通道**——对比一下它在你实际任务上，和 Opus 5.5 / 你现用的免费模型差多少，再决定要不要为 API 侧付 $2/$10。
- **第二件：把 Space Bunny Alpha 和 Dots3 这两条「剩 1–2 天」的额度今天跑掉。** 两条都按 **9/30 到期**。**别看还有一两天就拖——stealth 类历史上（ox-alpha 6 天、union-alpha 不到 2 天）经常提前关闭，而它现在是日榜第一，负载最高。**
- **顺手做件防呆的事：检查你所有配置里写死的免费模型名。** 今天这条 `ling-3.0-flash-fin:free` 只活了约一周；`nex-n2.5-*:free` 活了约两周。两条都印证同一件事：**写死的 $0 通道需要备线**——主力挂 NIM / 智谱永久免费档，备线挂 LongCat 2.5。

### ② 今天之内

**把「免费档寿命」这件事从印象变成数据。**

本期正好凑齐了一个完整样本：**Nex-N2.5 从 9/9 上线免费版 → 9/25 弃用 → 9/29 付费版回归**，全程 20 天。加上此前的 **ox-alpha（6 天）、union-alpha（不到 2 天）、Space Bunny（约 7 天）、glm-5.2:free（长期在架后突然下架）**——**五种「免费档」的真实寿命差异极大，但没有一条会提前很久通知你。**

**建议今天做一张「免费档到期表」**：把你实际在用的每条通道写下来，标「来源类型」（永久 / 限时券 / 试用 / stealth / 捐赠换数据），**按类型设不同复看频率**——永久档每月看一次，限时券每周看一次，stealth 每天看一次。**成本十分钟，收益是永远不会在某天早上发现生产线断了。**

**如果你在用 agent 跑免费模型**，也值得看一眼英伟达今天开源的 **OpenShell 0.1.0**——**它的思路是「不改编 agent 代码，在运行时外面套一层沙箱 + 策略验证」**，正好对应这周密集出现的 agent 越权事件。

### ③ 本周之内

1. **把「免费池收缩」当成趋势而非波动来做预案。** 零价池已连续两期净减（24 → 21 → 20），**而目录同期净增 15 款**——**平台没停止接入新模型，只是不再把新模型免费给你。** 本周值得把「付费兜底」认真算一遍成本：现在低价档已经很便宜（DeepSeek V4.1 Flash 谷时、GPT-6 Luna $0.10/$0.50、GLM-5.3-Flash $0.15/$0.50），**从 $0 到「几乎不要钱」的那一档，价格差其实很小。**
2. **把 Sonnet 5.5 纳入「性价比档」的比较。** 它把「$2/$10 就能拿到接近 Opus 5.5 的能力」这件事摆上台面，**而且免费档就能先试。** 如果你的团队在「Opus 太贵、Flash 不够用」之间做过取舍，**今天这条正好填在那个空档里。**
3. **盯四个日期**：**9/30**（Space Bunny + Dots3 + 一批国产免费期集中到期，本周最密集的一天）、**10/7**（智谱夜免与 MiniMax 签到）、**10/15**（阶跃 Step 5 权重开源，许可证是变量）、**10/21**（小米 MiMo-V2.5 全线下线）。
4. **等 Haiku 5.5。** 官方说「即将推出」且定位「快速、高吞吐」——**按 Anthropic 的分层习惯，它很可能成为下一款落在免费档或低价档的 Claude 模型，值得盯。**

## 📚 数据来源

- **OpenRouter** `/api/v1/models`（9/29 脚本清点，460 款中 20 款 $0、其中 16 款带 `:free` 后缀；已留 `or_models_0929.json`、`zen_0929.json` 供次日 diff；较 9/28 的 458 / 21 / 17 三项变动：总量 +2、零价 −1、`:free` −1）
- **零价池退出一条**（`inclusionai/ling-3.0-flash-fin:free`，262K，Zen 侧同名免费档仍在架）与总量新增四条（`anthropic/claude-sonnet-5.5`、`anthropic/claude-sonnet-5.5:batch`、`nex-agi/nex-n2.5-mini`、`nex-agi/nex-n2.5-pro`；下架 `deepseek/deepseek-r1-distill-llama-70b`）
- **Claude Sonnet 5.5**（Anthropic，2026-09-28 当地时间发布 / 9/29 北京；Claude 5.5 家族第二款；$2 / $10 / 缓存读 $0.20 per M；比 Sonnet 5 快 30%+、单任务成本最高省 30%；Terminal-Bench 4.0 70.6% vs Sonnet 5 的 10.3%；GDPval-AA 与 Opus 5.5 差 2 分内；**已成为 Claude 免费档所用模型**；可用平台 Claude 官方 + Amazon Bedrock + Claude Platform on AWS + AWS GovCloud (US)；Haiku 5.5 即将推出；OpenRouter 侧 1M ctx、文本+图像+文件输入，批量版 $1 / $5）—— 财联社 / 经济观察报 / 界面新闻 / 新浪财经 / aibriefing.dev
- **Nex-N2.5 生命周期**（免费版 9/9 上线 OpenRouter → 第三方记录弃用日 2026-09-25（EOL）→ 9/29 付费 SKU 回归 `nex-n2.5-mini` $0.025/$0.10 缓存 $0.0025、`nex-n2.5-pro` $0.075/$0.25 缓存 $0.015，均 262K、图文）—— rival.tips / readaitime.com
- **Space Bunny Alpha**（`stealth/space-bunny-alpha`；1M ctx / 文本·图像·视频输入 / 工具调用 / 可调 reasoning effort；9/23 上线；**OpenRouter 日榜第一 4.32T +8%，周榜 13.86T 第 3，月榜 18.2T 第 8（new）**；Zen 侧「零保留、不用于训练」）
- **OpenRouter 用量榜**（日榜截至 9/28：Space Bunny Alpha 4.32T / DeepSeek V4.1 Flash 3.68T / MiMo-V2.6-Flash 1.43T / GLM 5.3 Flash 1.32T / GPT-5.6 Luna 1.29T / Hy4 preview 1.21T / Nemotron 3 Ultra (free) 964B；周榜截至 9/27：DeepSeek V4.1 Flash 19.58T / GLM 5.3 Flash 16.32T / Space Bunny Alpha 13.86T / DeepSeek V4 Flash 0731 11.17T / Hy4 preview 9.64T / GPT-5.6 Luna 8.54T / Nemotron 3 Ultra (free) 5.7T / MiMo-V2.6-Flash 5.51T；月榜：GLM 5.3 Flash 57.5T / Hy4 preview 56T / GPT-5.6 Luna 52.1T / Nemotron 3 Ultra (free) 18.9T / Space Bunny Alpha 18.2T；作者份额 DeepSeek 24.4%）
- **中国模型调用量**（OpenRouter 数据测算 9/21–9/27：中国 62.22 万亿 tokens vs 美国 14.2 万亿 tokens，**连续 22 周全球第一**；上周全球总量 146 万亿 tokens 环比 +13.18%）—— 中国日报香港 / 21世纪经济报道 / 每日经济新闻
- **NVIDIA OpenShell 0.1.0 与 Open Agent Safety Platform**（9/28 开源；内核级沙箱 + 形式化策略验证；OpenShell 管运行时 containment、Sentry 在 BlueField-4 DPU 上监控网络流量；100+ 合作方含微软、Anthropic、xAI、Perplexity、OpenWorker；另批准回购授权增加 1500 亿美元至总额 2350 亿美元）—— aibriefing.dev / byobot.ai
- **Google Gemma 4 12B**（编码器无关架构、家族首个原生支持音频的中量级模型、约 16GB 内存笔记本可跑、支持函数调用 / 结构化 JSON / 系统指令；OpenRouter 免费池另有 `google/gemma-4-26b-a4b-it:free` 与 `google/gemma-4-31b-it:free`，均 262K）—— impakti.com / everylocalai.com
- **降价与平台动态**（DeepSeek V4.1-Flash 谷时输出降至 $0.60/M、比 V4-Pro 低约 70%，ARR 突破 10 亿美元并筹备科创板 IPO；阿里 Qwen-Audio 3.1 语音 API 降价 70–95%；Grok 4.7 登陆 Amazon Bedrock，500K ctx + low→xhigh 四档；Meta 成立 Meta Enterprise Platform 主推 Muse 系列，Llama 未在阵容内）—— aibriefing.dev
- **新免费网关**（BazaarLink `api.bazaarlink.ai/v1`：2 款免费模型 `qwen/qwen3.7-flash` 与 `deepseek/deepseek-v4-flash-0731free`，免绑卡，未充值 10 RPM + 50 加权单位/日、充值后 20 RPM + 100 单位/日、00:00 UTC 重置、2 并发；ModelBridge `aibridge-api.com`：免费档 50 万 tokens/月 + 50 万新客奖励、免绑卡、港节点聚焦中国模型；AIHubMix：60 款 / 16 作者，免卡 10 次试用，$1 一次性充值后 100 请求/日 + 1M tokens/日每日重置）—— freetokens.custats.info / aihubmix.com
- **OpenCode Zen** `/zen/v1/models`（83 款、免费 ID 11 个）与官方定价页（Free 行 10 款；新增付费 `claude-sonnet-5-5`，对应定价页 Claude Sonnet 5 一档 $2.00 / $10.00、缓存读 $0.20；LongCat 2.5 Preview 与 Space Bunny 均标注零保留、不用于训练）
- **freellm.net 核验榜**（2026-09-29：502+ 款 / 31 家平台 / 235 款实时验证 / 415+ 免绑卡；榜首 NIM `z-ai/glm-5.3` 96 与 `z-ai/glm-5.3-flash` 95；`Ling 3.0 Flash Sante (free)` 95 第 3、`Qwen3.8 27B (free)` 93 第 4、Ollama Cloud `deepseek-v4-pro` 92 第 5、NIM `Kimi K3` 90、Gemini 3.8 Flash 90、Zen `Qwen3.8 Max` 88、Zen `GLM-5.3` 87；**滞后实证：其 OpenRouter 免费页仍把已退场的 `ling-3.0-flash-fin:free` 标为 Online 并显示 21 款**）
- **rival.tips**（正确标注 `nex-n2.5-mini:free` / `-pro:free` 为 EOL，弃用日 2026-09-25；并收录 `respan/span-01-lite:free`——Respan 行为打分模型，走 OpenRouter Decisions API 而非 chat completions）
- **国内临期清单**（9/30 集中到期：Dots3-Note Preview 免费档、阿里 Qoder × Qwen3.8-Flash、腾讯 Hy3 与文心 4.0 全系列、上海电信 AI Store 2500 万额度领取、杭州千问办公 Token 卡现场领、Merge Gateway GLM-5.3-Flash 1 折；10/7：智谱夜免与 MiniMax Code 双倍签到；10/10：DeepSeek 低谷价与腾讯 Hy4 preview；10/17：豆包 30 天订阅；10/21：小米 MiMo-V2.5 系列下线；11/7：MiniMax 开放平台 M3 / M2 免费试用）
- **智谱 z.ai 开放平台永久免费档**（`GLM-4.7-Flash` / `GLM-4.5-Flash` / `GLM-4.6V-Flash` 输入、缓存输入、输出均为 Free）
- **Nous Portal 免费档**（含 `upstage/solar-pro4:free`、`stepfun/step-3.7-flash:free` 等；注册赠 $1；**注意需绑卡后才会展示完整模型列表**）
- **CommandCode**（Go $1/月、GOAT $10/月；**额度为共享池、按所选模型不同、含 4.4% + $0.30 处理费**）

---

## ⚠️ 免责声明

⚠️ 免费额度可能随时调整，请以各平台官网最新政策为准。本页所有「免费」判定均以官方接口或官方定价页为准；涉及额度的具体数字请自行调用官方 Usage API 或查看控制台确认。OpenRouter 免费池日内会波动，460 款 / 20 款零价 / 16 款 `:free` 是脚本清点时刻的快照，不代表全天稳定值。

**`stealth/space-bunny-alpha`（Zen 侧 `space-bunny-free`）为匿名第三方供应商运营，OpenRouter 与 OpenCode 仅负责路由，不承担其开发者/所有者/运营者角色；其「限时免费一周」是当前公告而非承诺，且本周即将到期；stealth 类模型历史窗口常因负载提前关闭，请勿作为长期依赖。其与 MiniMax M3.1 的对应关系基于社区分词器指纹与发布时间线推断，MiniMax 未正面确认该映射。**

**Claude Sonnet 5.5 的「免费」仅指 Claude 官方客户端（claude.ai）的免费档可用，其 API 入口（OpenRouter / OpenCode Zen / Bedrock 等）均为付费；本页不对「免费档的速率与配额」做承诺，请以 Anthropic 官方说明为准。**

**`longcat-2.5-preview-free`（美团 LongCat 2.5-Preview）官方未公布任何 benchmark，本页不对其能力做强弱结论；「零保留」为其在 OpenCode Zen 侧的条款表述，走官方 API 时请另行核对服务条款。**

**第三方聚合榜（freellm.net / rival.tips / AIHubMix / llmpricing.dev 等）与官方目录存在滞后与计数差，本页已记录多处实证（下架模型仍标 Online、已停用模型仍标 New、免费范围变更未反映），请勿单独据其做采购或宣传结论。**

「开源」指权重公开，不代表可自由商用，商用前请逐条核对许可证（尤其 Kimi、GLM、Qwen、MiniMax、Step、MiMo、Gemma 系列的 Model-as-a-Service 与许可条款）。**Contributor / 试用 / 训练条款类免费档：不要把机密代码、个人信息或生产客户数据放进去。** 本页提到的 Aggregate Gateway（FreeLLMAPI / Merge / ModelBridge / BazaarLink / Free.ai 等）上游不透明、无 SLA，仅建议用于试验与个人项目，请勿把长期密钥或生产数据接入来路不明的网关。

📅 生成时间：2026-09-29 · 本页由自动化任务每日生成
