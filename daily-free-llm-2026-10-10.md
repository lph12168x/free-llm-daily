# 免费大模型日报 · 2026-10-10（周六）

> 🤖 AI 每日免费情报 · 全网挖掘 · [在线版 HTML](daily-free-llm-2026-10-10.html)

**今日四个关键数字**

| 数字 | 含义 |
| --- | --- |
| **登顶双榜** | 阶跃 **Step 5 Preview 登顶 OpenRouter Trending 榜、日榜全球第二**（AA 综合智能指数 **44**、全球开源前三）；600B 总参 / 27B 激活 MoE、**1M 上下文**、原生多模态；免费约一周，**官方确认 10/15 正式开源权重** |
| **458 / 19 · 87** | OpenRouter 目录 **469 → 458（−11）**、零价 **19 款（与昨日完全一致）**、`:free` 15 款；OpenCode Zen **87 款 / 免费 ID 12 个**——**两家清点与昨日完全一致** |
| **今日算力免费** | **Qwen-Image-2.1-Turbo 开源**：7B DiT、**8 步出 2K 图**、原生透明通道；**权重 Qwen Research 许可（商用需另行授权）**，托管 API ¥0.10/张 |
| **长期兜底仍在** | **NIM ~1 万请求/日居首**、**Groq 1,000/日**、**Cloudflare 1 万 neurons/日**、**豆包 200 万 tokens/日**、**智谱 GLM-Flash 永久免费** |

---

## 🔥 今日头条 · 三条主线

### ① 开源旗舰免费冲顶｜阶跃 **Step 5 Preview 登顶 OpenRouter Trending 榜、日榜全球第二**

**今天「先进模型 + 免费」这一格唯一的主角，还是阶跃 Step 5 Preview——上线第二天就冲到 OpenRouter 趋势榜第一、日榜全球第二，官方确认 10 月 15 日正式开源权重。**

**🏆 双榜战绩（10/10）**

- **OpenRouter Trending 榜第 1**、**日榜（按当日 Token 处理量）全球第 2**。
- DAIR.AI 联合创始人 Elvis Saravia 实测评价：**能力可与 GLM-5.3、Kimi K3 媲美，处在成本 / 能力权衡的「帕累托前沿」**。

**🚀 规格（复核）**

- **600B 总参 / 27B 激活**稀疏 MoE、**1M 上下文**、64K 输出上限、原生多模态输入（文本 / 图像 / 视频）。
- **Artificial Analysis 综合智能指数 44 分，位居全球开源前三**；面向 AI 编程、软件工程、专业知识工作与金融场景优化。

**🎁 免费窗口仍在（约一周）**

- 10/8 上线，**OpenRouter + OpenCode + Cline + Nous Research + Kilo Code 免费约一周**（Cline 侧两周）。
- **OpenCode 侧带零数据保留（ZDR）承诺**——本轮免费通道里条款最干净的一条。

**💰 到期后怎么算**

- OpenRouter 定价 **$1.00 / $2.70 per M**（缓存命中 $0.05，上线期五折）。
- **10/15 开源权重后，可自托管 = 脱离「免费档随时消失」的风险**；但许可证与 Model-as-a-Service 条款要逐条核。

> **今天的行动建议**：趁免费一周，把你最吃上下文的真实任务（整库问答 / 长文档 / 多步 Agent）在 Step 5 上跑一遍。**10/15 权重放出后，自托管就多一条不依赖厂商免费档的长期选项——这是本期最值钱的一条路。**

---

### ② 平台清点｜OpenRouter **458 / 零价 19**；Zen **87 / 免费 12**——两家与昨日持平

**本期两家接口都「按兵不动」：昨天的换血完成后，今天没有新增也没有下架，池子数量完全一致。**

**🔄 OpenRouter（脚本清点 10/10）**

- 目录 **458 款（较昨日 −11）**、**零价 19 款（与昨日完全一致）**、带 `:free` 后缀 **15 款**。
- **零价池今日进出均为 0**——昨日 `ling-3.0-flash-sante:free` 出池转付费后，池子稳定在 19。
- **口径提醒**：`inclusionai/ling-3.1-flash`（无 `:free`）**仍为 $0/$0**，「零价但不带后缀」继续成立。

**🖥️ OpenCode Zen**

- 接口仍 **87 款**、免费标记 ID **12 个**（昨日 13）——差异仅来自命名口径。
- 官方定价页 Free 行 **13 条**：Big Pickle、Space Bunny、LongCat 2.5 Preview、**Step 5 Preview**、Exo、MiMo-V2.6-Flash、MiMo-V2.5、Ling 3.1 Flash、Ling 3.0 Flash Fin、Nemotron 3 Ultra、Nemotron 3.5 Lightning、Muse Spark 1.3 Contributor、Jev 1.13 Free。

**⚠️ Zen 免费池的两条条款**

- **Nemotron 3 Ultra / 3.5 Lightning Free（NVIDIA 免费端点）：仅限试用，勿提交个人或机密数据**，使用会被记录用于改进 NVIDIA 产品。
- **Big Pickle / Space Bunny / LongCat / Step 5 Preview / Exo / MiMo / Ling 系列 Free：免费期内数据「可能用于改进模型」**——别喂生产代码。

**🔓 零价池近六期流水**

| 日期 | 目录总量 | 零价池 | 其中 `:free` | 零价净增减 |
| --- | --- | --- | --- | --- |
| 9/29 | 460 | 20 | 16 | +0 / -1 |
| 9/30 | 464 | 20 | 16 | +0 / -0 |
| 10/8 | 467 | 20 | 16 | +2 / -2 |
| 10/9 | 469 | 19 | 15 | +0 / -1 |
| **10/10（今天）** | **458** | **19** | **15** | **+0 / -0** |

> 零价池连续两期停在 **19**，今日无进出；而**目录总量由 469 回落到 458（−11）**——减少的是付费侧条目。**平台既不加免费供给、也不减，全部变化发生在付费侧。**

---

### ③ 承接昨日｜Google 免费档已切 Flash-Lite；行业侧补位继续

**昨天（10/9）Google 把 Gemini 应用个人免费档砍到只剩 Flash-Lite（32K）；今天没有反转，反而是「谁在补位」开始显现。**

**📉 变化确认**

- **未订阅 Google AI 的个人账户：Gemini 应用可用模型 = 仅 Flash-Lite**。
- **Flash 移入 $4.99/月 AI Plus；AI Plus 不再含 Pro；Pro 需 $19.99/月 AI Pro**；Deep Think 属 AI Ultra。
- **关键：这次动的是应用层免费档，Google AI Studio / Gemini API 免费层本次未同步收紧。**

**🌤️ 谁在补位**

- **① ChatGPT 免费档仍给 GPT-6 Luna**（旗舰级 + 智能交互界面，仅 Chat 体验、不含 API）。
- **② 开源侧：Step 5 Preview 免费一周 + 10/15 开源**，把「免费旗舰」从闭源应用层挪到了可自托管侧。
- **③ Qwen-Image-2.1-Turbo 今日开源**（图像向）。

**🧭 替代顺序不变**：长上下文 + 多模态又不想付费 → **Google AI Studio（免费层仍在）→ NVIDIA NIM（1M）→ OpenRouter 零价池**；要「最先进又免费」→ **免费版 ChatGPT（GPT-6 Luna）或 Step 5 Preview**。

> **一句话总结今天**：昨天是「一收一放」（Google 收、OpenAI 放），今天是「收势确认 + 开源补位」：闭源应用免费档继续缩，开源旗舰（Step 5 / Qwen-Image-2.1-Turbo）继续放，且都给出了「开源权重」这条退路。

---

## 🌤️ 次要更新 · 值得记一笔

### 🧮 开源侧今日两条：图像加速与极致量化

- **① Qwen-Image-2.1-Turbo（阿里通义，10/9）**：7B 视觉生成模型，**去噪从 40 步压到 8 步、原生 2K 出图**，支持多参考图编辑与 **RGBA 透明通道**；托管 API **¥0.10/张（120 RPM）**，Pro 档 ¥0.25/张（20 RPM）。**⚠️ 权重为 Qwen Research License，商用自托管需另行授权**。
- **② NVIDIA Nemotron 3.5 Lightning**：**30B MoE / 30B 激活**的开放模型，面向「始终在线的 agent」中的快速专业任务；**同步在 Zen 与 OpenRouter 提供 Free 端点**。

> **读法**：图像与 agent 两条线都在往「更小步数 / 更小激活 + 开放权重」走——免费能用的门槛继续下降。

### 🎟️ 「量大能用」免费额度大盘（10/10 复核）

- **NVIDIA NIM**：**约 40 RPM / 无明确日上限**（官方口径「约 1 万请求/日」），含 `glm-5.3`、`Kimi K3`（均 1M）；**需手机验证**，仅限开发测试、勿传机密数据。
- **Groq**：**30 RPM / 1,000 请求·日 / 8K TPM**（`gpt-oss-120b`、`qwen3.8-27b`，免绑卡）。
- **Google AI Studio**：**Flash-Lite 约 500 请求·日**，免绑卡；**⚠️ 免费档输入可能用于改进产品**（EEA / 瑞士 / 英国除外）。
- **Mistral**：**每模型 1 次/秒、每月约 10 亿 tokens**（免费档默认用于训练，可申请退出）。
- **Cloudflare Workers AI**：**每天 1 万 neurons**；**Cohere**：20 RPM / 1,000 次·月。
- **⚠️ 三条要记**：**GitHub Models 已于 7/30 关停**；**Cerebras 免费档已改为 $5 一次性额度（需绑卡）**；**Hugging Face 仅 $0.10/月额度**。

### 📈 freellm.net 核验榜（10/9）：NIM 仍居首，聚合站滞后继续

榜首仍是 **NVIDIA NIM `z-ai/glm-5.3`（95 分，81.8M 周调用）**、`z-ai/glm-5.3-flash`（95，3.3T 周调用）；其后 **Ollama Cloud `deepseek-v4-pro`（91）**、**Kilo Code `qwen3.8-27b:free`（91）**、**NIM Kimi K3（90）**。

**⚠️ 滞后实证（继续）**：多个聚合页仍在列 `qwen/qwen3.8-27b:free`、`space-bunny-alpha` 等**已在正式接口里消失**的条目，也把已转付费的模型标成免费。**结论不变：「是否还在免费」永远回官方接口复核。**

---

## 🎟️ 今日免费入口速查 · 先进 + 量大优先

| 入口 | 免费额度 | 模型量级 | 状态 / 注意 |
| --- | --- | --- | --- |
| **阶跃 Step 5 Preview** 🟣 | 免费约一周（OpenRouter / OpenCode / Cline / Nous / Kilo） | **600B / 27B 激活** · 1M · 多模态 | 今天先进 + 免费的最佳组合；**双榜登顶**；AA 44 分；OpenCode 侧带 ZDR |
| **NVIDIA NIM** `z-ai/glm-5.3` | **40 RPM**（约 1 万请求/日 · 无日 token 上限） | GLM-5.3 / Kimi K3 · 1M | **量最大、最稳的一档（连续两期榜首）**；须手机验证；勿传机密 |
| **Groq** | **30 RPM · 1,000 请求/日** | gpt-oss-120b · Qwen3.8 27B | 免绑卡、最快（LPU）；8K TPM，长输入要节制 |
| **Google AI Studio** | 免绑卡（Flash-Lite ~500 请求/日） | Gemini 3.x Flash · 1M · 多模态 | **⚠️ App 免费档已收紧，但 AI Studio 免费层不受影响**——长上下文兜底首选 |
| **免费版 ChatGPT** | 免费档可用（App / 网页） | **GPT-6 Luna** | 旗舰模型免费；无需 key / 绑卡；仅 Chat 体验，API 侧不变 |
| **OpenRouter** `nemotron-3-ultra-550b-a55b:free` | **50 请求/日**（充 $10 → 1,000） | 550B / 激活 55B · 1M | **零价池里量最大、最稳的一条**；NVIDIA 试用端点 |
| **OpenCode Zen** `step-5-preview-free` | 四列全 Free（限时） | Step 5 / Exo 等 | 免费池本期进出均为 0；免费期数据条款各异，别喂机密 |
| **智谱 z.ai** | 输入输出全 Free（无到期日） | `GLM-Flash` 等 · 国内直连 | **唯一可写进长期依赖的一类**；永久档仍在 |

**📌 长期兜底组合（无到期日那一类）**：智谱 z.ai（GLM Flash 永久免费）· Google AI Studio（免绑卡、按项目日额度）· NVIDIA NIM（40 RPM）· Groq（1,000/日）· 火山方舟豆包（200 万 tokens/日）· 商汤 SenseNova Token Plan（每 5 小时刷新）· Cloudflare Workers AI（1 万 neurons/日）。

> **组合建议**：**主力**用一条稳的（NIM / 智谱永久免费档 / Google AI Studio），**兜底**用无到期日的（豆包 / 商汤 / Cloudflare），**试用**用限时与 preview（Step 5 Preview / Exo）。**本期的态度：昨天的「收势」今天得到确认，但开源侧在补位**——把「今天就能跑完」当成规划单位，把「能不能自托管」当成长期退路。

---

## ⏰ 到期日历 · 别踩空

**📅 今天 / 刚过去**

- **10/10（今天）** — **DeepSeek 低谷价窗口结束**；**腾讯混元 Hy4 preview（老用户夜间免费）结束**
- **10/9** — Google Gemini 应用免费档收紧为 Flash-Lite（⚠️ AI Studio 免费层不受影响）；Qwen-Image-2.1-Turbo 开源权重发布
- **10/8** — Step 5 Preview 免费一周开始（OpenRouter / OpenCode / Cline / Nous / Kilo）

**📅 10 月中下旬及以后**

- **10/15** — **阶跃 Step 5 Preview 释放完整 BF16 权重**（许可证待公布）；NVIDIA 中国开发者日（苏州，10/15–16）
- **10/17** — 豆包全用户 30 天订阅（9/24 那轮）截止
- **10/21** — **小米 `mimo-v2.5-pro` / `mimo-v2.5` 正式下线**
- **10/31** — **Mistral Large 4 发布开源权重**；**DeepSeek ZDR 协议本月续期截止**
- **11/7** — MiniMax 开放平台 M3 / M2 免费试用到期
- **12/31** — 腾讯云 TokenHub / 华为云码道 / 移动云 MoMA 年度额度截止

---

## 🧭 今天该怎么动

### ① 现在就做（10 分钟内）

- **第一件：趁免费窗口把 Step 5 Preview 跑一次真实任务。** 它今天登顶 OpenRouter 双榜，是当前「先进 + 免费 + 可接 CLI」三条同时满足的唯一选手。用你最吃上下文的活（整库问答 / 长文档 / 多步 Agent）实测一遍，**免费期约一周，过了就按 $1.00 / $2.70 计费**。
- **第二件：如果你有脚本依赖 Gemini 应用的免费 Flash / Pro，昨天就已经失效。** 换成 **Google AI Studio（免费层仍在）→ NIM（1M）→ OpenRouter 零价池**。

### ② 今天之内

- **把「量大能用」的三条接进备用链**：**NVIDIA NIM（约 1 万请求/日）打头，Groq（1,000/日）居中，OpenRouter（50/日）垫底**——三者都兼容 OpenAI SDK。**关键是把 `max_retries=0`，让 429 直接切下家。**
- **顺手核对配置里有没有已失效的免费模型名**：本期零价池无进出，但**目录总量减少 11 条**——定期 diff `or_models` 快照，比盯聚合站靠谱。

### ③ 本周之内

- **为 10/15 做一次准备：把「Step 5 自托管」列成备选。** 权重放出后，它就从「限时免费」变成「永久免费 + 可私有化」——这是本周最值钱的一条路。
- **把免费通道按可靠性分层，而不是按额度排序**：**永久免费档（智谱 / AI Studio）→ 厂商试用端点（NIM）→ 免费应用层（GPT-6 Luna）→ 预览期免费（Step 5）→ stealth**。越往后越便宜也越短命；生产链路只用前两层。
- **盯三个日期**：**10/15**（Step 5 权重 + NVIDIA 中国开发者日）、**10/21**（MiMo-V2.5 下线）、**10/31**（Mistral Large 4 开源权重）。
- **留意一条「还没落地的预期」**：Step 5 免费一周到期后，官方会不会把它做成长期免费档——如果权重如期开源，答案就已经有了。

---

> ⚠️ 免费额度可能随时调整，请以各平台官网最新政策为准。开放数据：OpenRouter `/api/v1/models`（10/10 清点：**458 款中 19 款 $0、其中 15 款带 `:free` 后缀**）、OpenCode Zen `/zen/v1/models` + 官方定价页（10/10：**接口 87 款、免费标记 ID 12 个**）。OpenRouter 免费池日内会波动，以上为**脚本清点时刻的快照**。
> 📅 生成时间：2026-10-10 · 本页由自动化任务每日生成
