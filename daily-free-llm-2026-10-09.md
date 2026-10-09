# 免费大模型日报 · 2026-10-09（周五）

> 🤖 AI 每日免费情报 · 全网挖掘 · [在线版 HTML](daily-free-llm-2026-10-09.html)

**今日四个关键数字**

| 数字 | 含义 |
| --- | --- |
| **免费档 → Flash-Lite** | Google 今日（10/9）起，未订阅 Google AI 的个人账户在 Gemini 应用可用模型由三款缩为**仅 Flash-Lite（32K）**；Flash 移入 $4.99/月 AI Plus，**AI Plus 的 Pro 也被拔除**；**⚠️ AI Studio / API 免费层不受影响** |
| **600B / 27B** | 阶跃 **Step 5 Preview** 免费约一周：600B 总参 / 27B 激活 MoE、**1M 上下文**、文图视频三模态；上线 OpenRouter，并在 OpenCode / Cline / Nous / Kilo 免费开放（OpenCode 侧带 ZDR） |
| **469 / 19 · 87** | OpenRouter 目录 **467 → 469**、零价 **20 → 19**（唯一出池 `ling-3.0-flash-sante:free`，且直接转为付费）；OpenCode Zen **87 款 / 免费 ID 13 个**（+`step-5-preview-free`、−`fledge-alpha-free`） |
| **200 万 / 日** | 国内日额度最大：**火山方舟（豆包）200 万 tokens/日**；**商汤 SenseNova Token Plan 长期免费公测**（不绑卡、每 5 小时刷新） |

---

## 🔥 今日头条 · 三条主线

### ① 免费档收缩｜Google 今日起把 **Gemini 应用免费档砍到只剩 Flash-Lite**——付费档也一起缩

**这是 10 月以来「免费资源」最重要的一次收缩：从今天（10/9）起，没有订阅 Google AI 的个人账户，在 Gemini 应用里能用的模型从 Flash-Lite / Flash / Pro 三款，直接缩到只剩 Flash-Lite 一款。**

依据 Google 帮助页「Changes to Gemini model access and limits」，**付费档也未能幸免——AI Plus 的 Pro 权限同样被拔除。**

**📉 到底改了什么**

- **免费档（$0）→ 仅 Flash-Lite**，上下文缩到 **32K**（约为 1M 的 3%）。
- **Flash 移入 $4.99/月 AI Plus**；**AI Plus 不再含 Pro**。
- **Pro 需 $19.99/月 AI Pro**；Deep Think 与全部模型要 $99.99+ 的 **AI Ultra**。

**⚠️ 关键区分（别误伤自己）**

- 这次动的是 **Gemini 应用（网页 / App）的免费档**，**不是 Google AI Studio / Gemini API 的免费层**（免绑卡、按项目日额度）；
- **用 API 的链路本次并未同步收紧，仍然可用**；
- 断掉的是「**在 App 里免费用 Pro 深度思考**」这条路。

**🧭 替代怎么选**

- **要长上下文 + 多模态又不想付费 → 首选转 Google AI Studio**（免费层仍在），其次 **NVIDIA NIM**（GLM-5.3 / Kimi K3，1M）、**OpenRouter 零价池**；
- **要「最先进又免费」→ 免费版 ChatGPT（GPT-6 Luna）与今天新开的 Step 5 Preview。**

**🧭 怎么读这条**

- **同一天，两条方向相反的动作**：Google **收紧**免费档（只剩 Flash-Lite）——OpenAI **升级**免费档（GPT-6 Luna + 智能界面，10/8 起推送）。
- **对你的实际含义：别把关键工作流绑在单一免费档上，尤其别绑在「应用层的免费旗舰」上——它随时会变。**

---

### ② 先进又免费｜阶跃 **Step 5 Preview**：**600B / 27B 激活、1M 上下文**，免费一周

**今天「量大能用的先进模型」这一格，最值得上手的是阶跃星辰的 Step 5 Preview——旗舰级配置，却给了明确的免费窗口。**

**🚀 规格**

- **600B 总参 / 27B 激活**的稀疏 MoE，**1M 上下文**，文本 + 图像 + 视频多模态；
- 官方定位：面向 **金融与编码**的 agentic / 专业任务，用更低的任务成本换旗舰级智能。

**🎁 免费入口（约一周）**

- 10/8 上线 **OpenRouter**，StepFun 同时在 **OpenCode、Cline、Nous Research、Kilo Code** 等平台开放免费约一周（Cline 侧为两周）；
- **OpenCode 侧附带零数据保留（ZDR）承诺**——免费期相对干净的一条。

**📊 跑分与实测**

- 官方称 **DeepSWE 上领先 Kimi K3 与 GLM-5.3**；AA Intelligence Index 约 **44**（与 GLM 5.3 / Kimi K3 同一档）；
- 社区实测约 **115 tokens/s**、首字延迟约 **1.5s**。

**💰 免费期后定价**

- OpenRouter 为 **$1.00 / $2.70 per M**（缓存命中 **$0.05**，上线期五折）；
- **免费窗口就是「把整个仓库塞进去」的最好时机——1M 上下文 + 免费，这种组合不常有。**

**🧭 和 ChatGPT Luna 不是一类**

- **GPT-6 Luna 是「应用里的一次性重活」**（不接 API）；**Step 5 Preview 是「能接进 agent / CLI 的 1M 长上下文」**；
- **建议：趁免费一周，把你最吃上下文的那条链路（整库问答、长文档分析）切到它上面试一次，再决定要不要留。**

---

### ③ 平台清点｜OpenRouter **469 / 零价 19**；Zen **87 / 免费 ID 13**（Step 5 进、Fledge 出）

**本期两家接口都动了，但方向一致：新上的先进模型全在付费侧，免费侧靠 preview 补位。**

**🔄 OpenRouter（脚本清点 10/9）**

- 目录 **469 款（+2）**、**零价 20 → 19 款（−1）**、带 `:free` 后缀 **16 → 15**；
- **唯一出池**：`inclusionai/ling-3.0-flash-sante:free`——同时转为**付费版** `inclusionai/ling-3.0-flash-sante`（**$0.042 / $0.1232 per M**）；
- 新增 3 条全为**付费**：`openai/gpt-6.1-sol:batch`、`gpt-6.1-sol-pro:batch`、`stepfun/step-5-preview`；另移除 `baidu/ernie-4.5-vl-424b-a47b`；
- **注意**：`inclusionai/ling-3.1-flash`（无 `:free` 后缀）**仍为 $0/$0**——「零价但不带后缀」这条口径继续成立。

**🖥️ OpenCode Zen**

- 接口仍 **87 款**，免费标记 ID **13 个（数量不变）**；
- **−`fledge-alpha-free`（匿名 / preview 通道到期）**、**+`step-5-preview-free`**；
- 官方定价页 Free 行共 **13 条**：Big Pickle、Space Bunny、LongCat 2.5 Preview、**Step 5 Preview**、Exo、MiMo-V2.6-Flash、MiMo-V2.5、Ling 3.1 Flash、Ling 3.0 Flash Fin、Nemotron 3 Ultra、Nemotron 3.5 Lightning、Muse Spark 1.3 Contributor、Jev 1.13 Free。

**💰 顺手一条**

- **Mistral Large 4 在 Zen 标 50% off**（$0.68 / $2.09），与预览期折扣一致——「预览期便宜、权重月底才开源」。

**⚠️ 一条纪律**

- **「数量踩住、质地换一遍」继续。** Fledge 这类匿名 / preview 通道的生命周期就是几天到几周；
- **把免费通道当变量、别当常量——写进配置里就要准备好它明天消失。**

---

## 🌤️ 次要更新 · 值得记一笔

### 🌏 国内免费额度大盘（截至 10/8）：谁家「送得最多」

- **① 火山方舟（豆包）**：实名后**每天自动发 200 万 tokens**，单模型另给 50 万基础额度——**日额度最大的一家**（需先在控制台手动开通模型）。
- **② 商汤 SenseNova Token Plan**：**长期免费公测、不绑卡不充值，每 5 小时刷新配额**（首月每 5 小时 1500 次）。
- **③ 讯飞星火 Spark Lite**：**永久免费 API**；星辰 MaaS 开源模型 0 元无限量。
- **④ 腾讯混元 Lite**：**长期免费**；TokenHub 新人包每模型 100 万 tokens、可用到 12/31。
- **⑤ 阿里云百炼 / 百度千帆**：新用户每模型送 100 万 tokens（90 天 / 3 个月）；文心 ERNIE-Speed / Lite 长期免费。
- **⑥ 智谱 z.ai**：GLM Flash 系列**永久免费**，新用户另送 2000 万 tokens。
- **⚠️ 两条要记**：**硅基流动「小模型永久免费」已取消**（现仅 embedding / 语音 / OCR / 翻译 / Kolors 免费）；**市面上没有通用「AI 兑换码 / CDKey」，卖码的一律当诈骗。**

### 📈 freellm.net 核验榜（10/8）：NIM 仍居首，但聚合站有滞后

- **499+ 款 / 30 家平台 / 235 款实时 API 验证**；榜首仍是 **NVIDIA NIM `z-ai/glm-5.3`（95 分）**、`z-ai/glm-5.3-flash`（95）；
- 其后 **Ollama Cloud `deepseek-v4-pro`（91）**、**Kilo Code `qwen3.8-27b:free`（91）**、**NIM Kimi K3（90）**；
- **⚠️ 滞后实证（本期继续）**：多个聚合页仍在列 `qwen/qwen3.8-27b:free`、`space-bunny-alpha` 等**已在正式接口里消失**的条目，也把已转付费的模型标成免费——**「是否还在免费」永远回官方接口复核。**

### 🧩 免费入口补充与提醒

- **① Nous Portal**：$0 档仍含一批 `:free` 模型（Ling / LongCat / Laguna / Step 等，免绑卡、标准限速），**是本期 Step 5 免费一周的入口之一**。
- **② Ox Alpha**：`oxalpha.org` 打出「免费 1M 上下文前沿模型」的招牌（`stealth/ox-alpha`，经 OpenRouter 路由）——**属 stealth 自营宣传站，本期并未进入 OR 零价池，当作参考即可。**
- **③ 纪律**：聚合网关（UnoRouter / OrcaRouter / Nous Portal / Kilo 等）**上游不透明、无 SLA**，只做试验与个人项目。
- **④ 「免费期数据可能用于训练」的通道（Exo / Fledge / Muse Spark Contributor 等）：别喂机密代码与个人信息。**

### 🔬 开源侧顺手记：决策模型与极致量化

- **① Cloudflare 首款自研模型 Clef（27B）/ Clef-flash（9B）**：开源权重，**返回每个候选答案的概率**而非自由文本，支持 64K 内图像与视频；兼容 Jev 的 API，**延迟反超 Jev**（209ms / 38.8ms 对 524ms）。
- **② Samsung Labs 开源 LittleBit**：把权重压到 **1.0 → 0.1 bit / 参数**级别，保持原架构推理；支持 OPT / Llama 2·3 / Phi-4 / Qwen2.5·3 / Gemma 2·3。**⚠️ 代码为 CC BY-NC 4.0，商用需另行授权。**
- **③ Google DeepMind EmbeddingGemma 2**：740M 多模态嵌入模型，把文本 / 代码 / 图像 / 音频 / 视频映到同一空间，可跑在手机上。
- **读法**：**带不动大模型时，「小模型 + 极致压缩 + 本地化」是另一条免费的解法。**

---

## 🧾 今日免费入口速查（先进 + 量大优先）

| 入口 | 免费额度 | 模型量级 | 状态 / 注意 |
| --- | --- | --- | --- |
| **阶跃 Step 5 Preview** 🟣 本期新增 | 免费约一周（OpenRouter / OpenCode / Cline / Nous / Kilo） | **600B / 27B 激活**，1M · 多模态 | **今天先进 + 免费的最佳组合**；DeepSWE 超 Kimi K3 / GLM-5.3；OpenCode 侧带 ZDR |
| **NVIDIA NIM** `z-ai/glm-5.3` | **40 RPM**（约 1 万请求/日） | GLM-5.3 / Kimi K3，**1M** | **量最大、最稳的一档**；**须手机验证**；勿传机密数据 |
| **Groq** | **30 RPM · 1,000 请求/日** | gpt-oss-120b / Qwen3.8 27B | **免绑卡、最快（LPU）**；限额按组织计 |
| **Google AI Studio** | 免绑卡（每项目日额度） | Gemini 3.x Flash，**1M · 多模态** | **⚠️ App 免费档今日收紧，但 AI Studio 免费层不受影响**——长上下文兜底首选 |
| **免费版 ChatGPT** | 免费档可用（App / 网页） | **GPT-6 Luna**（旗舰级 + 交互界面） | **旗舰模型免费**；无需 key / 绑卡；仅 Chat 体验，API 侧不变 |
| **OpenRouter** `nemotron-3-ultra-550b-a55b:free` | **50 请求/日**（充 $10 → 1,000） | 550B / 激活 55B，**1M** | **零价池里量最大、最稳的一条**；NVIDIA 试用端点 |
| **OpenCode Zen** `step-5-preview-free` | 四列全 Free（限时） | Step 5 / Exo 等 | **本期免费池「一进一出」**；免费期数据条款各异，别喂机密 |
| **智谱 z.ai** | 输入输出全 Free、无到期日 | `GLM-Flash` 等，国内直连 | **唯一可写进长期依赖的一类**；永久档仍在 |

---

## 🔎 平台盘点 · 今日快照

**OpenRouter：469 款中 19 款零价（`:free` 15 款）**

- 清点时刻：**469 款**，**输入与输出同时为 $0 的共 19 款**，**带 `:free` 后缀 15 款**；
- **本期唯一出池**：`inclusionai/ling-3.0-flash-sante:free` → 转为付费 `inclusionai/ling-3.0-flash-sante`（$0.042 / $0.1232）；
- **四条「零价但不带 `:free`」**：`ling-3.1-flash`（560B/25B）、`lyria-3-pro-preview`、`lyria-3-clip-preview`（后两条输出音频）、`openrouter/free`（200K 自动路由池）；
- **1M 且 $0 的条目 5 条**：nemotron-3.5-lightning:free、nemotron-3-ultra-550b-a55b:free、inkling:free、inkling-small:free、lyria-3-pro / clip-preview。

**零价池近六期流水（输入与输出同时为 $0 的口径）**

| 日期 | 目录总量 | 零价池 | 其中 `:free` | 零价净增减 |
| --- | --- | --- | --- | --- |
| 9/28 | 458 | 21 | 17 | +0 / -3 |
| 9/29 | 460 | 20 | 16 | +0 / -1 |
| 9/30 | 464 | 20 | 16 | +0 / -0 |
| 10/8 | 467 | 20 | 16 | +2 / -2 |
| **10/9（今天）** | **469** | **19** | **15** | **+0 / -1** |

零价池在 20 款附近连站四期后本期 **−1**，且**换出的那条直接转付费**。**结构非常稳定：平台继续接新模型（本期 +2），只是不再把新模型做成免费档。** 今天唯一的「逆势」来自 preview：**Step 5 Preview 的免费一周。**

---

## 📅 到期日历 · 别踩空

**今天 / 刚过去**

- **10/9（今天）** — **Google Gemini 应用免费档收紧为 Flash-Lite**，Flash / Pro 转付费（⚠️ AI Studio 免费层不受影响）。
- **10/8** — OpenAI GPT-6 向 Free / Go 推送（GPT-6 Luna），分阶段进行中。
- **10/8** — Step 5 Preview 免费一周开始（OpenRouter / OpenCode / Cline / Nous / Kilo）。

**10 月中下旬及以后**

- **10/10** — DeepSeek 低谷价窗口结束；腾讯混元 Hy4 preview 结束。
- **10/15** — 阶跃 Step 5 Preview 释放完整 BF16 权重（许可证待公布）。
- **10/17** — 豆包全用户 30 天订阅截止；**10/21** — 小米 `mimo-v2.5-pro` / `mimo-v2.5` 正式下线。
- **10/31** — **Mistral Large 4 发布开源权重**；DeepSeek ZDR 协议续期截止。
- **11/7** — MiniMax 开放平台 M3 / M2 免费试用到期。**12/31** — 腾讯云 TokenHub / 华为云码道 / 移动云 MoMA 年度额度截止。

---

## 🧭 今天该怎么动

**① 现在就做（10 分钟内）**

- **把「Gemini 免费档」这条依赖从你的方案里摘出来**——今天起免费档只剩 **Flash-Lite（32K）**；若有脚本 / 工作流依赖 App 端免费 Flash 或 Pro，**今天就会失效**。替代顺序：**Google AI Studio → NVIDIA NIM → OpenRouter 零价池**；
- **趁免费窗口试一次 Step 5 Preview**——**1M 上下文 + 免费一周**，最适合把最吃上下文的真实任务（整库问答 / 长文档分析）跑一遍。

**② 今天之内**

- **把「量大能用」的两条接进备用链**——**NVIDIA NIM（约 1 万请求/日）打头，Groq（1,000/日）居中，OpenRouter（50/日）垫底**；关键是把 `max_retries=0`，让 429 直接切下家；
- **顺手清一次写死的免费模型名**——`inclusionai/ling-3.0-flash-sante:free` **已转付费并出池**，换成 `inclusionai/ling-3.1-flash`（仍 $0/$0）。

**③ 本周之内**

- **重新评估「应用层免费旗舰」的权重**——**Google 今天收、OpenAI 昨天放**；真正的底座要放在**有明确条款的 API 免费层**（AI Studio / NIM / 智谱永久免费档）上；
- **给免费通道按可靠性分层**——永久免费档（智谱 / AI Studio）→ 厂商试用端点（NIM）→ 免费应用层（GPT-6 Luna）→ 预览期免费（Step 5）→ stealth；**生产链路只用前两层**；
- **盯三个日期**——**10/10**（DeepSeek 谷时价、腾讯 Hy4 preview）、**10/15**（Step 5 权重）、**10/31**（Mistral Large 4 开源权重）；
- **留意一条「还没落地的预期」**——**Step 5 免费一周到期后，官方会不会把它做成长期免费档。**

---

> ⚠️ 免费额度可能随时调整，请以各平台官网最新政策为准。本页所有「免费」判定均以官方接口或官方定价页为准。OpenRouter 免费池日内会波动，469 款 / 19 款零价 / 15 款 `:free` 是脚本清点时刻的快照。
> **「Gemini 免费档收紧」指 Gemini 应用（网页 / App）的个人免费账户；Google AI Studio / Gemini API 的免费层本次未同步调整。** Step 5 Preview 的「免费」为限时（各平台窗口不同），到期后按各平台定价计费。
> 第三方聚合榜与官方目录存在滞后与计数差，请勿单独据其做采购或宣传结论。「开源」指权重公开，不代表可自由商用，商用前请逐条核对许可证。
> 📅 生成时间：2026-10-09 · 本页由自动化任务每日生成。
