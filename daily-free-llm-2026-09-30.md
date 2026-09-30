# 免费大模型日报 · 2026-09-30（周三）

> 🤖 AI 每日免费情报 · 全网挖掘 · [在线版 HTML](daily-free-llm-2026-09-30.html)

**今日四个关键数字**

| 数字 | 含义 |
| --- | --- |
| **$2 / $10** | OpenAI DevDay 发布 **GPT-6.1 Sol**：能力接近 Astra、**价格只要 1/5**；缓存输入 **$0.10/M（比上代再降一半）**，DeepSWE v1.1 **75%**；**无免费 API 入口**，随 ChatGPT Work / Codex 订阅开放 |
| **$0.25 / 月** | 新免费网关 **Gonka Broker**：DeepSeek V4 Flash / GLM-5.3-Flash / MiniMax M2.7；**免绑卡但必须手机验证（+86 实测被拒）**，免费档 6 RPM 整账户共享 |
| **今天到期** | **Dots3-Note Preview 免费档**与**腾讯混元 Hy3 限免**均在 **9/30 23:59** 结束，9/30 是本月免费权益最密集的一天 |
| **4M / 60s** | **Hetzner Inference API** 实验期免费：Qwen3.6-35B-A3B 与 Qwen3.8-27B、**262K**、免绑卡、按速率给额度 |

---

## 🔥 今日头条 · 三条主线

### ① 新模型 · 行业价格线｜OpenAI 发布 **GPT-6.1 Sol**：**$2 / $10**、缓存 **$0.10**，**近旗舰能力卖 1/5 价**

**今天 OpenAI DevDay 的主场是 GPT-6.1 Sol。它对「免费用户」的意义不在免费本身，而在于——它又把「接近旗舰的能力」往低价档推了一格。**

当地时间 9/29（北京 9/30），OpenAI 在 DevDay 2026 上发布 **GPT-6.1 Sol**，定位是「**接近 Astra 的智力，只要 Astra 五分之一的标准 token 价**」。

**💵 定价：缓存这项尤其狠**

- **输入 $2 / 百万、输出 $10 / 百万**（标准档）；**缓存命中输入 $0.10 / 百万 —— 相当于标准输入价的 5%，比上一代 GPT-6 Sol 的缓存价再便宜一半**；
- **规格：1.05M 上下文 / 128K 最大输出 / reasoning 档位 low→max**；
- 官方说法是「**让 agent 复用上下文、反复迭代、跑更长任务变得更便宜**」——**缓存价砍到 1/20，本质是把「长流程 agent」的成本结构改了**。

**📈 跑分：编码追平，硬推理仍差**

- **DeepSWE v1.1：75%，与 Astra 约 74.8% 基本持平**（比 GPT-6 Sol 的最佳成绩再高 **6.4 个百分点**）；
- **OSWorld 2.0（电脑操作）：距 Astra 的 73.5% 只差 2.1 分，但每任务约 $1.30 vs Astra 的 $9.30**；
- **⚠️ 硬推理不省钱：Terminal-Bench Science 57% @ $5.47 vs Astra 68.1% @ $23.80**——**11 分的差距，科学推理类负载仍该上 Astra**；
- **一句话读法：写代码、跑浏览器 agent 选 Sol；前沿推理还得付 Astra 的钱。**

**🎁 免费入口在哪（关键）**

- **没有任何免费 API 入口。** GPT-6.1 Sol 通过 **ChatGPT Work 与 Codex 对 Plus / Pro / Business / Enterprise / Edu 用户开放**，API 侧走 `gpt-6.1-sol`；
- **也就是说：有 ChatGPT 订阅的人今天就能用，想走 API 必须付费**；
- OpenRouter 同步上架 4 条（`openai/gpt-6.1-sol` ± `pro` ± `:batch`，**全在付费侧**）；OpenCode Zen 上架 `gpt-6.1-sol`（≤272K 档 $2/$10、缓存读 $0.10；>272K 翻倍）；
- **官方预告 Ultrafast 加速档（Codex 内最高 8× 速度）随后上线。**

**⚠️ 同日背景：上一款被自己砍掉了**

- **OpenAI 前一天刚刚放弃 GPT-6.1 Astra 的发布计划**——按外媒说法是「**测试中经常无视指令、表现不可预测**」；
- 而 Sol 这次主打的两条正是「**更透明地说明自身限制**」与「**更可靠地遵守用户意图与安全约束**」，并称在自动化安全审查上「**没有出现任何绕过尝试**」；
- 同场还发布了 **Dots 智能体**（云端 24 小时后台干活）、**ChatGPT Space / Pages**（团队协作）、**Pro 500 套餐（$500/月）**、**Codex 全面支持云端运行**、**Codex Security Cloud**、**Agents API 电脑操作**、**Decisions API**。

**🔍 与 Sonnet 5.5 撞车（最值得记的一条）**

**Anthropic 9/28 发 Sonnet 5.5（$2/$10），OpenAI 9/29 发 GPT-6.1 Sol（$2/$10）——隔一天、同一个价格点、同一套话术：「旗舰八成能力，五分之一价格」。**

这不是巧合，是**两家都在抢「真实生产流量所在的那个价格点」**——当 GPU 产能增速快过需求，头部实验室的必然动作就是**把顶配的高溢价让掉，去占住中段**。

**为什么这条要写进「免费日报」**：近三期两条主线正好互为表里——**一边是免费池连续收缩（零价池 24 → 21 → 20），另一边是低价档快速变便宜**。**结论：平台不是不给便宜模型了，而是把「免费」换成了「便宜」。**

---

### ② 新免费通道 · 两条｜**Gonka Broker**（$0.25/月额度）+ **Hetzner Inference API**（实验期免费）

**今天真正「新挖到」的免费增量，是两条 OpenAI 兼容端点——一条走美元计价的中转，一条是欧洲云厂商的实验产品。**

**🎁 Gonka Broker：把免费额度做成了「$0.25/月」**

- 背景是 **Gonka 去中心化 GPU 网络**，对外以普通美元计价 API 出售（**不用碰加密货币**）；入口 `https://proxy.gonkabroker.com/v1`；
- **免费档三款开源模型**：`deepseek-ai/DeepSeek-V4-Flash-0731`（400K / 输出 16K）、`zai-org/GLM-5.3-Flash`（400K / 16K）、`MiniMaxAI/MiniMax-M2.7`（204.8K / 16K）；另含 embedding `BAAI/bge-m3`；
- **额度口径很特别：不是「多少 token」，而是每月固定约 $0.25 的金额**，按各模型单价换算——**折算约 125 万 DeepSeek / GLM tokens，或 100 万 MiniMax tokens**；**输入输出同价**（这点对长回答有利）。

**⚠️ 两个营销页没写的坑**

- **① 必须手机验证才发额度。** 注册只要邮箱或 Google 账号、**不要信用卡**，但注册后余额是 0、key 显示 BLOCKED，**验证手机号后余额才立刻到账**（一个号码一份免费档）。**实测：中国大陆 +86 号码被拒——「免绑卡」不等于「零门槛」。**
- **② 免费档限速 6 RPM，而且是整账户共享、不分模型。** 官网 key 页写的 600 RPM 是付费档；免费档连续几次请求就会 429，**超限直接 429、不自动转付费**。
- 额度**每月 1 号重置、不按天折算**（9/29 验证时仍是满额，重置日 10/1）。

**🖥️ Hetzner Inference API：实验期完全免费**

- **欧洲云厂商 Hetzner 的 OpenAI 兼容推理端点**：`https://inference.hetzner.com/api/v1`；
- **两款模型**：`Qwen/Qwen3.6-35B-A3B-FP8`（**MoE 35B 总参 / 3B 激活、支持视觉**）与 `Qwen3.8-27B`（稠密），**均 262,144 上下文、文本+图像输入**；
- **限速（按 API key）：每 60 秒 400 万输入 tokens + 10 万输出 tokens，外加每 60 秒 10 次请求**；
- **官方原文：只要 Inference API 仍处于实验状态就免费；状态若变更会提前邮件通知。** 需注册账号取 token，**未见绑卡要求**；**不保证性能与可用性、不面向生产**。

**🧭 该怎么用这两条**

- **① 想「白嫖一批先进开源模型」→ 先试 Hetzner**：免绑卡、额度是「每 60 秒 400 万 tokens」这种**按速率的量**，**比 Gonka 的 $0.25/月宽得多**；
- **② 想跑需要「多模型切换」的实验 → Gonka Broker**：三款模型横跨 DeepSeek / GLM / MiniMax，**但 6 RPM 只能做单用户小工具**，跑不了 agent；
- **③ 无论哪条，都别接生产 key、别传机密数据。**

**📌「免绑卡」这个词，本期被重新定义了一次**

三周来我们反复写「免绑卡」——但 Gonka 这条提醒了一件事：**不绑卡 ≠ 零门槛**。**NVIDIA NIM 要手机验证、Mistral 要手机验证、Gonka 也要手机验证，而且明确拒收 +86。** 建议把「是否需要手机验证」和「是否绑卡」并列成选型条件。

---

### ③ 到期日 · 榜单｜**9/30 一天集中到期**；**Space Bunny Alpha 周榜登顶 23.4T**

**今天是本月免费权益最密集的一天——多条通道同时到期。榜单那边，一条 $0 的匿名模型正式坐上了全站第一。**

**⏰ 今天 9/30 到期（今天就该跑）**

- **① Dots3-Note Preview 免费档**（OpenRouter `dots-studio/dots-3-note-preview:free` + 官方 `studio.dots.ai`；**280B / 激活 16B、512K、图文、tools + structured_outputs**）——**官方标注有效期至 2026-09-30**；
- **② 腾讯混元 Hy3 限免**（官方口径延长至 **2026-09-30 23:59**）；
- **③ 同一批到期的还有**：阿里 Qoder × Qwen3.8-Flash 免费用、百度文心 4.0 全系列免费期、上海电信 AI Store 2500 万额度领取、杭州千问办公 Token 卡现场领、Merge Gateway GLM-5.3-Flash 1 折；
- **④ 另外一条要盯**：Space Bunny Alpha 的「限时免费一周」按 9/23 起算，窗口就在这两天。

**📊 周榜（截至 9/29）：$0 模型第一**

- **① Space Bunny Alpha（$0）23.4T（new）**
- ② DeepSeek V4.1 Flash 22T **+24%**
- ③ GLM 5.3 Flash 11.6T **−37%**
- ④ GPT-5.6 Luna 8.31T −4%
- ⑤ MiMo-V2.6-Flash 8.21T **>999%**
- ⑥ Hy4 preview 8.06T −38%
- ⑦ DeepSeek V4 Flash 0731 7.28T −16%
- ⑧ **Nemotron 3 Ultra (free) 5.86T +15%（前十唯一长期免费条目）**
- **月榜**：GLM 5.3 Flash 57.5T 第一 / Hy4 preview 56T / GPT-5.6 Luna 51.9T / DeepSeek V4.1 Flash 47.9T；Space Bunny 23.4T 第 6、Nemotron 3 Ultra (free) 19T 第 8。

**🐰 Space Bunny 现在有 3 个入口**

- **OpenRouter（`stealth/space-bunny-alpha`，1M、文本+图+视频、可调 reasoning effort）**；
- **OpenCode Zen（`space-bunny-free`，零保留、不用于训练）**；
- **本期新发现：第三方网关 Command Code 也提供零额度访问（约 1049K、免绑卡）**。
- **⚠️ 身份仍未官方确认**——第三方独立测试与分词器指纹**持续指向中国厂商 MiniMax**，但 **MiniMax 与 OpenRouter 都没有正面确认**。**把它当「好用但随时会消失的匿名供应商」对待，永远在配置里留一条备线。**

**⏳ 智谱倒计时：还有 7 天，但每天清零**

- **9/28–10/7 期间，ZCode 每天向全体用户发「1 亿 Token × 10 万份」GLM-5.3-Flash**；
- **⚠️ 关键细节：这是「当天作废的票」，不是一个月白嫖期。** 已有用户实测反馈**额度第二天凌晨清零，且频繁遇到「当前系统繁忙，请切换模型」**；
- **付费用户另得 8 张重置卡**（4 张周额度 + 4 张 5 小时额度，有效期 1 个月）。**读法：把它当每日抽奖，别当稳定额度。**

**📌 stealth 窗口纪律（第三次重申）**

**已记录的实际寿命：ox-alpha 6 天 → union-alpha 不到 2 天 → Space Bunny 已超一周（但公告口径是「限时一周」）→ ling-fin:free 约一周 → nex-n2.5 free 约两周。** **结论不变：不要按公告日期规划，按「今天就能跑完」规划。**

---

## 🌤️ 次要更新 · 值得记一笔

### 🐰 Space Bunny Alpha 扩到第三个平台：Command Code 也提供零额度访问

本期核对到一条新路径：**第三方网关 Command Code 也提供 Space Bunny Alpha 的免费访问（约 1049K 上下文、免绑卡）**。加上原有的 OpenRouter 与 OpenCode Zen，**这条匿名模型现在有三个入口**。

**⚠️ 三个入口的条款不一样，必须分开看**：**Zen 侧写的是「零保留、不用于训练」（最干净）**；**OpenRouter 侧是「匿名第三方可能保留 prompts 与 completions，但不用于训练」**；**Command Code 这条暂未见到同等级别的数据条款说明**。**同样是「免费」，数据对价不同——选入口时先看条款，再看价格。**

**实用提醒**：由于它随时可能转付费或消失，**正确做法是把它写成一个变量而不是常量**——主模型、备用模型各留一个配置项，并现在就定好「什么时候切」的规则。

### 💰 OpenCode Go 与 Command Code GOAT：$10 套餐里 DeepSeek V4.1 Flash 额度永久提到 $60/月（6×）

两家 AI 编程订阅本周同时加码：继 OpenCode 宣布把 $10/月的 Go 套餐中 **DeepSeek V4.1 Flash 额度永久提升到 $60/月**后，**Command Code 也宣布 $10/月的 GOAT 套餐做同样调整（永久）**。

**口径要读准**：**这是「共享额度池」，不是每个模型各给一份。** OpenCode Go 每月总额度 $60，**DeepSeek V4.1 Flash、GLM-5.3 Flash、Kimi K2.6 等模型共同消耗这份额度**。**Command Code 侧**：GOAT $10/月共享 $70/月额度池（含 Jev），**另有一款 $1/月套餐、约合 $10 等效额度**。

**为什么这条对「免费日报」重要**：$10 换 $60 的额度，**折算下来单位 token 成本已经非常接近 $0**——**它实际上是「免费池收缩」的一种对冲产品。**

### 🧰 免费网关生态快照：AIHubMix 60 款 / LLM7.io / free-llm.com 目录

- **① AIHubMix 免费池维持 60 款 / 16 家作者**（更新 2026-09-28）：**免卡先送 10 次试用；一次性充 $1 后切换永久日额度——100 请求/日 + 10 请求/分 + 100 万 tokens/日，每天重置**；近 30 天该池跑了 **35.1B tokens / 307K 次请求**；
- **② LLM7.io**：**无需注册 30 RPM，用免费邮箱 token 提到 120 RPM，滚动 24 小时内最多约 500 万 tokens**；
- **③ free-llm.com 社区目录**把免费通道分成「永久免费层」与「一次性试用金」两类，**并明确标注哪些需要手机验证**——**这是本期第二条与 Gonka 呼应的经验**。

### 📈 平台口径：OpenRouter 464 款 / 20 零价，Zen 84 款，freellm.net 487+

- **① OpenRouter**：**464 款，其中 20 款零价、16 款带 `:free` 后缀**。今天总量 **+4 条，全部是 GPT-6.1 Sol 系列**，**零价池零进零出**——**近六期第一次「零价池完全不动」，但方向仍是新增全进付费侧**；
- **② OpenCode Zen**：**84 款（+1，新增付费 `gpt-6.1-sol`，零下架）**；**官方定价页 Free 行 10 款**；**⚠️ `muse-spark-1.2-contributor-free` 仍在 `/models` 列表里，但已从定价页 Free 行移除**——**接口列表可能滞后，定价页仍是权威源**；
- **③ freellm.net 核验（2026-09-30）**：**487+ 款 / 30 家平台 / 233 款实时验证**；榜首 **NVIDIA NIM `z-ai/glm-5.3`（96 分）**、`z-ai/glm-5.3-flash`（95 分）、OpenRouter `Qwen3.8 27B (free)`（93 分）、Ollama Cloud `deepseek-v4-pro`（92 分）、NIM `Kimi K3`（90 分）；
- **⚠️ 滞后实证（本期）**：多家聚合站与中文攻略页**仍把 `z-ai/glm-5.2:free` 与 `minimax/minimax-m2.7:free` 列为免费**，而官方目录里这两条**早已变成付费**（现价 $0.25/$3.99 与 $0.21/$0.84）。

### 🔒 智谱 ZCode 补偿落地进展：云端数据已删、上传链路已移除

- **① 已移除「仓库快照上传链路」，事件涉及的全部云端数据已删除，处置结果经第三方核查确认**；
- **② 官方公开承诺：在用户未主动发起相关操作的前提下，任何内容都不会离开用户电脑，代码数据全程保留本地**；此前整改还包括**开源 ZCode、引入第三方安全审计、MaaS 平台上线数据不留存功能**；
- **③ 补偿按两类发放**：付费及一个月内回归的付费用户——**4 张周额度重置卡 + 4 张 5 小时额度重置卡（1 个月有效）**；全体用户——**9/28–10/7 每日「1 亿 Token × 10 万份」**；
- **④ 一句实务提醒**：如果你本地仓库曾走过这类客户端的索引功能，**今天顺手做两件事——轮换一遍仓库里出现过的密钥，检查一下 CI/部署配置里的敏感变量。**

---

## 🧾 今日免费入口速查（先进 + 量大优先）

| 入口 | 免费额度 | 模型量级 | 状态 / 注意 |
| --- | --- | --- | --- |
| **NVIDIA NIM** `z-ai/glm-5.3` | **40 RPM**、不限调用量、需手机验证 | 1.3M 上下文；freellm.net 96 分榜首 | **长期兜底首选**；同站还有 `glm-5.3-flash`（95）与 `Kimi K3`（90） |
| **OpenRouter** `nemotron-3-ultra-550b-a55b:free` | $0 / $0，200 请求/日 | 550B / 激活 55B、**1M** | 周榜 **5.86T +15%，前十唯一长期免费**；NVIDIA 试用端点，**勿传个人 / 机密数据** |
| **Space Bunny Alpha**（OR / Zen / Command Code） | $0 / $0，限时，窗口就在这两天 | **1M** / 文本+图+视频 | **周榜第一 23.4T**；ID 不带 `:free`；**今天就跑完** |
| **Hetzner Inference API** | **4M 输入 / 60s** + 10 万输出 / 60s、免绑卡 | Qwen3.6-35B-A3B、Qwen3.8-27B、262K | **本期新增**；实验期免费、**不保证 SLA** |
| **Gonka Broker** | ≈ **$0.25 / 月**，每月 1 号重置 | DeepSeek V4 Flash / GLM-5.3-Flash / M2.7 | **免绑卡但要手机验证（+86 被拒）**；**6 RPM 整账户共享** |
| **LongCat 2.5-Preview**（Zen） | **四列全 Free**，限时 | 1.6T / 激活 48B、**1M + 原生多模态** | **零保留、不用于训练**；美团具名厂商，**免费期结束转付费而非断供** |
| **智谱 z.ai**（永久免费档 + 双节活动） | **输入输出全 Free**，夜免至 10/7 | `GLM-4.7-Flash` 等，国内直连 | **唯一可以写进长期依赖的一类**；**ZCode 每日 1 亿券当天作废** |
| **Dots3-Note Preview** 🔴 今天到期 | $0 / $0，至 2026-09-30 | 280B / 激活 16B、512K / 图文 | 支持 tools / structured_outputs；**现在就跑** |

**📌 长期兜底组合（无到期日那一类）**

- **智谱 z.ai** — `GLM-4.7-Flash` / `GLM-4.5-Flash` / `GLM-4.6V-Flash` **输入输出全 Free，无到期日**（国内直连）；
- **NVIDIA NIM** — **40 RPM、不限调用量**，含 `glm-5.3`（1.3M）与 `Kimi K3`（1M）；**需手机验证**；
- **Hetzner Inference API** — **实验期免费、免绑卡**，按速率给额度；**随时可能结束实验期**；
- **书生 InternLM** — **1.8 亿 tokens/月、免信用卡、无明确到期日**；
- **美团 LongCat** — **每天 5,000 万 token**（官方平台）；
- **Cloudflare Workers AI** — **每天 1 万 neurons**；**OVHcloud AI Endpoints** — **匿名免注册 9 款**，2 RPM；
- **FreeLLMAPI（自托管，MIT）** — **34 家 / 635 端点 / 约 7.4 亿 tokens·月**。

**组合建议**：**主力**用一条稳的（NIM / 智谱永久免费档），**兜底**用无到期日的（LongCat / InternLM / Hetzner），**试用**用限时券与 stealth。本期新增的态度是：**「免费」这一层之外，也该把 $10/月级订阅算进来**——OpenCode Go 与 Command Code GOAT 的额度折算后，单位成本已经很接近 $0。

---

## 🔎 平台盘点 · 今日快照

### 📊 OpenRouter：**464 款中 20 款零价**（`:free` 16 款）

- 脚本清点时刻：**464 款（较 9/29 +4）**，其中**输入与输出同时为 $0 的共 20 款**（**持平**），**带 `:free` 后缀 16 款**（**持平**）；
- **今天总量 +4 条，全部是付费**：`openai/gpt-6.1-sol`、`openai/gpt-6.1-sol-pro` 及各自 `:batch`（**均 1.05M ctx、$2/$10、批量版 $1/$5、缓存读 $0.10**）。**零下架**；
- **零价池零进零出**——**近六期里第一次「零价池完全不动」**，但**连续新增仍全部落在付费侧**；
- **四条「零价但不带 `:free`」**：`stealth/space-bunny-alpha`（1M 三模态）、`google/lyria-3-pro-preview`、`google/lyria-3-clip-preview`（后两条输出音频）、`openrouter/free`（200K 自动路由池）；
- **1M 且 $0 的条目 7 条，与上期持平**。

### 🆓 零价池近五期流水（输入与输出同时为 $0 的口径）

| 日期 | 目录总量 | 零价池 | 其中 `:free` | 零价净增减 |
| --- | --- | --- | --- | --- |
| 9/23 | 454 | 24 | 21 | — |
| 9/24 | 457 | 24 | 20 | +1 / -1 |
| 9/28 | 458 | 21 | 17 | +0 / -3 |
| 9/29 | 460 | 20 | 16 | +0 / -1 |
| **9/30（今天）** | **464** | **20** | **16** | **+0 / -0** |

今天零价池第一次「踩住刹车」，**但同期目录净增 4 款、全部落在付费侧**。**结构没变：平台继续接新模型，只是不再把新模型做成免费档。**

### 🔧 OpenCode Zen：**83 → 84 款**（+`gpt-6.1-sol`），定价页 Free 行 **10 款**

- `/zen/v1/models` 返回 **84 款**（+1，**零下架**）。新增 **`gpt-6.1-sol`**（**付费**）：**≤272K 档 $2.00 / $10.00、缓存读 $0.10；>272K 档 $4.00 / $15.00、缓存读 $0.20**——**缓存单价是 GPT-6 Sol 的一半**；
- 带免费标记的 ID 仍 **11 个**：`jev-1.13-free`、`deepseek-v4-flash-free`、`muse-spark-1.3-contributor-free`、`muse-spark-1.2-contributor-free`、`mimo-v2.6-flash-free`、`space-bunny-free`、`longcat-2.5-preview-free`、`mimo-v2.5-free`、`ling-3.0-flash-fin-free`、`nemotron-3-ultra-free`、`nemotron-3.5-lightning-free`；
- 官方**定价页 Free 行 10 款**（Big Pickle、Space Bunny、LongCat 2.5 Preview、MiMo-V2.6-Flash、MiMo-V2.5、Ling 3.0 Flash Fin、Nemotron 3 Ultra、Nemotron 3.5 Lightning、Muse Spark 1.3 Contributor、Jev 1.13 Free）；
- **⚠️ 本期新发现一处名单不一致**：`muse-spark-1.2-contributor-free` **仍在 `/models` 返回列表里，但已从官方定价页 Free 行移除**——**定价页是权威源，接口列表可能滞后**；
- **📖 数据条款三类仍要分清**：**Space Bunny / LongCat 2.5 = 零保留、不用于训练**（最干净）；**Big Pickle / MiMo / Ling = 免费期数据可能用于改进模型**；**Nemotron 两条 = NVIDIA 试用端点，明确勿传个人/机密数据**。

### 🌐 freellm.net：**487+ 款 / 30 家平台 / 233 款实时验证**

- 核验时间 2026-09-30。榜首 **NVIDIA NIM `z-ai/glm-5.3`（96 分，1.0M、最多 40 RPM）**、次席 **`z-ai/glm-5.3-flash`（95 分）**；
- **OpenRouter `Qwen3.8 27B (free)` 93 分第 3**、Ollama Cloud `deepseek-v4-pro` 92 分第 4、NIM `Kimi K3` 90 分第 5、Gemini 3.8 Flash 90 分第 6、Zen `Qwen3.8 Max` 88 分第 7、Zen `GLM-5.3` 87 分第 8；
- 榜单里能看到两条我们跟踪的条目：**`Space Bunny Alpha`（71 分，周吞吐 13.9T）**、**`Dots3-Note Preview (free)`（69 分，592.8B）**——**后者今天到期**；
- **⚠️ 滞后实证（本期）**：多家聚合站与中文攻略页**仍把 `z-ai/glm-5.2:free`、`minimax/minimax-m2.7:free` 列为免费**，而官方目录里**这两条早已是付费模型**。

---

## 📅 到期日历 · 别踩空

**今天 9/30（本月最密集的一天）**

- **Dots3-Note Preview 免费档到期**（OpenRouter + 官方 `studio.dots.ai`，官方标注至 2026-09-30）
- **腾讯混元 Hy3 限免结束（9/30 23:59）**
- **Space Bunny Alpha 的「限时免费一周」窗口就在这两天**
- **阿里 Qoder × Qwen3.8-Flash 免费用结束**；**百度文心 4.0 全系列免费期结束**
- **上海电信 AI Store 2500 万额度领取截止**；**杭州千问办公 Token 卡现场领结束**
- **Merge Gateway GLM-5.3-Flash 1 折结束**

**10 月及以后**

- **10/7** — **智谱 GLM-5.3-Flash 夜间畅用 + 全天五折结束**；**ZCode 每日 1 亿 Token 券发放结束**；**MiniMax Code 双倍签到结束**
- **10/10** — **DeepSeek 低谷价窗口结束**；**腾讯混元 Hy4 preview**（老用户夜间免费）结束
- **10/14** — 珠海算力券申报截止（企业向）
- **10/15** — **阶跃 Step 5 Preview 释放完整 BF16 权重**（许可证待公布）
- **10/17** — 豆包全用户 30 天订阅（9/24 那轮）截止
- **10/21（10:00）** — **小米 `mimo-v2.5-pro` / `mimo-v2.5` 正式下线**，Zen 的 `mimo-v2.5-free` 受影响
- **11/7** — MiniMax 开放平台 M3 / M2 免费试用到期
- **12/31** — 腾讯云 TokenHub / 华为云码道 / 移动云 MoMA 年度额度截止

---

## 🧭 今天该怎么动

**① 现在就做（10 分钟内）**

- **第一件（最紧急）：把 Dots3-Note Preview 的活跑掉。** 它是本期唯一一条**「有明确到期日 + 就是今天 + 还有 512K 长上下文」**的免费档。**用你手上最真实的一个长文档任务去测它，别用 hello world。**
- **第二件：Space Bunny Alpha 也今天跑完。** 它现在是**周榜第一**、负载最高，而 stealth 类的历史规律是**「负载打满就提前关」**。
- **第三件：注册一个 Hetzner 账号试试那条实验端点。** 免绑卡、额度按速率给，**这是今天新增的免费通道里门槛最低的一条。**
- **顺手做件防呆的事：翻一遍你所有配置里写死的免费模型名。** 今天确认 `glm-5.2:free` 与 `minimax-m2.7:free` **早已变成付费**，而很多攻略页还在教人用它们——**如果你的脚本里还写着这两条 ID，扣的就是真金白银。**

**② 今天之内**

- **把「免费 vs $10 订阅」这笔账算一次。** 本期最反直觉的一条是：**免费池连续收缩的同时，$10/月的订阅把额度提到了 $60。** 建议把你的实际月消耗估一下（看 Usage 面板就行），然后对着这两家的额度表比一次。
- **把 GPT-6.1 Sol 放进你的「性价比档」备选。** **$2/$10、缓存 $0.10、1.05M、DeepSWE 75%**——**如果你的工作以写代码和跑 agent 为主，这条今天的定位是「值得认真比价」。** 想让硬推理省钱就别选它，**但编码与电脑操作用它，成本结构是真的变了。**

**③ 本周之内**

- **把「是否需要手机验证」加进你的选型表。** Gonka 免绑卡但拒收 +86 号码，NVIDIA NIM 与 Mistral 也都要手机验证；
- **把「免费通道」按可靠性分层，而不是按额度大小排序**：**永久免费档（智谱 Flash 系）→ 厂商实验端点（Hetzner / NIM）→ 订阅折算（OpenCode Go / Command Code）→ 限时券（Dots3 / LongCat 2.5）→ stealth（Space Bunny）**。**越往后越便宜、也越短命。生产链路只用前两层。**
- **盯三个日期**：**10/7**（智谱夜免与每日券、MiniMax 签到）、**10/10**（DeepSeek 谷时价、腾讯 Hy4 preview）、**10/21**（小米 MiMo-V2.5 全线下线）；
- **留意两个「还没开的口子」**：OpenAI 的 **Ultrafast 加速档**（Codex 内最高 8×）；**Anthropic 的 Haiku 5.5**（官方称「即将推出」、定位快速高吞吐），**按分层习惯很可能是下一款落进免费档或低价档的 Claude 模型。**

---

## 📚 数据来源

- **OpenRouter** `/api/v1/models`（9/30 脚本清点，464 款中 20 款 $0、其中 16 款带 `:free` 后缀；已留 `or_models_0930.json`、`zen_0930.json` 供次日 diff；较 9/29 的 460 / 20 / 16：总量 +4、零价 0、`:free` 0）
- **GPT-6.1 Sol**（OpenAI，DevDay 2026，当地时间 2026-09-29 / 北京 9-30；$2/$10、缓存 $0.10；1.05M / 128K；DeepSWE v1.1 75%；OSWorld 2.0 差 Astra 2.1 分、每任务 $1.30 vs $9.30；Terminal-Bench Science 57% vs 68.1%；无免费 API；GPT-6.1 Astra 已放弃；同场 Dots / Space / Pro 500 / Codex 云 / Codex Security Cloud / Agents API / Decisions API）—— Hindustan Times · The Hindu · Startup Fortune · SignalDesk · 上游新闻
- **Gonka Broker**（三款开源模型、约 $0.25/月额度、每月 1 号重置、免绑卡但须手机验证且 +86 被拒、6 RPM 整账户共享）—— toolfreebie.com（2026-09-29~30 实测）
- **Hetzner Inference API**（`inference.hetzner.com/api/v1`；Qwen3.6-35B-A3B-FP8 与 Qwen3.8-27B；262,144 ctx；每 60 秒 4M 输入 + 10 万输出、10 请求/60s；实验期免费）—— freetokens.custats.info · GitHub nejib1/Free-LLM
- **OpenRouter 用量榜**（周榜截至 9/29：Space Bunny Alpha 23.4T（new）/ DeepSeek V4.1 Flash 22T +24% / GLM 5.3 Flash 11.6T −37% / GPT-5.6 Luna 8.31T / MiMo-V2.6-Flash 8.21T / Hy4 preview 8.06T / DeepSeek V4 Flash 0731 7.28T / Nemotron 3 Ultra (free) 5.86T）
- **中国模型调用量**（9/21–9/27：中国 62.22 万亿 vs 美国 14.2 万亿，连续 22 周全球第一）—— China Daily Asia
- **Space Bunny Alpha 三入口**（OR / Zen / Command Code；Zen 侧零保留、不用于训练；身份社区指纹指向 MiniMax，未获官方确认）—— freeaiapi.org · Hugging Face blog
- **OpenCode Go 与 Command Code GOAT**（均 $10/月，DeepSeek V4.1 Flash 额度永久提至 $60/月；共享额度池；GOAT 共享 $70/月池含 Jev，另有 $1/月套餐）—— 小众软件 appinn.com
- **免费网关生态**（AIHubMix 60 款 / 16 作者、更新 2026-09-28；LLM7.io 30→120 RPM、滚动 24h 约 500 万 tokens；FreeLLMAPI 34 家 / 635 端点）—— aihubmix.com · GitHub nejib1/Free-LLM
- **智谱 ZCode 补偿与整改**（9/28 10:30 生效；付费用户 4+4 张重置卡；9/28–10/7 每日「1 亿 Token × 10 万份」当日作废；仓库快照上传链路已移除、云端数据已删除并经第三方核查确认）—— 腾讯新闻 · 红星资本局 · 什么值得买
- **OpenCode Zen** `/zen/v1/models`（84 款、免费 ID 11 个）与官方定价页（Free 行 10 款；新增付费 `gpt-6.1-sol`；`muse-spark-1.2-contributor-free` 仍在接口列表但已从定价页移除）
- **freellm.net 核验榜**（2026-09-30：487+ 款 / 30 家平台 / 233 款实时验证；榜首 NIM `z-ai/glm-5.3` 96；滞后实证：仍把已完成付费化的 `glm-5.2:free` 与 `minimax-m2.7:free` 列为免费）
- **国内临期清单**（9/30 集中到期；10/7；10/10；10/17；10/21；11/7）

---

⚠️ 免费额度可能随时调整，请以各平台官网最新政策为准。本页所有「免费」判定均以官方接口或官方定价页为准；涉及额度的具体数字请自行调用官方 Usage API 或查看控制台确认。OpenRouter 免费池日内会波动，**464 款 / 20 款零价 / 16 款 `:free` 是脚本清点时刻的快照**，不代表全天稳定值。

`stealth/space-bunny-alpha`（Zen 侧 `space-bunny-free`、Command Code 侧同名）为匿名第三方供应商运营，其「限时免费一周」是当前公告而非承诺；stealth 类模型历史窗口常因负载提前关闭，请勿作为长期依赖。其与 MiniMax 的对应关系基于社区分词器指纹与发布时间线推断，MiniMax 未正面确认该映射。

`dots-studio/dots-3-note-preview:free` 免费档官方标注有效期至 **2026-09-30**，到期后可能转付费或下架；腾讯混元 Hy3 限免为 **2026-09-30 23:59** 截止。

**GPT-6.1 Sol 无免费 API 入口**，其「可用」范围指 ChatGPT Work / Codex 对相应订阅档开放。

**Gonka Broker 与 Hetzner Inference API 均为第三方端点**，上游不透明、无 SLA、额度可随时变更；Hetzner 明确标注实验期免费、不面向生产。请勿提交个人数据、机密代码或生产客户数据。

`z-ai/glm-5.2:free`、`minimax/minimax-m2.7:free` 在官方目录中**已为付费条目**（现价 $0.25/$3.99 与 $0.21/$0.84），请勿再按旧攻略当作免费模型调用。

第三方聚合榜与官方目录存在滞后与计数差，请勿单独据其做采购或宣传结论。「开源」指权重公开，不代表可自由商用。**Contributor / 试用 / 训练条款类免费档：不要把机密代码、个人信息或生产客户数据放进去。**

📅 生成时间：2026-09-30 · 本页由自动化任务每日生成
