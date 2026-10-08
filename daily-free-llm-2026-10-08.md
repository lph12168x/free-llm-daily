# 免费大模型日报 · 2026-10-08（周四）

> 🤖 AI 每日免费情报 · 全网挖掘 · [在线版 HTML](daily-free-llm-2026-10-08.html)

**今日四个关键数字**

| 数字 | 含义 |
| --- | --- |
| **$0.10 / $0.50** | Anthropic 发布 **Claude Haiku 5.5**：迄今最便宜最快的小模型，比 Haiku 4.5 便宜约 **75%**；**1M 上下文**；**即日起在所有平台提供，包括免费版 Claude 应用** |
| **1.05T / 49B** | Mistral 发布 **Large 4**：万亿级 MoE（激活 49B）、**1M 上下文**、160+ 语言；预览期 **$0.68 / $2.09**；**承诺月底开源权重** |
| **20 → 20** | OpenRouter 零价池**两进两出**：进 `apodex-1.1-mini:free`、`ling-3.1-flash`；出 `qwen3.8-27b:free`、`stealth/space-bunny-alpha`；Zen **84 → 87**、免费 ID **13 个** |
| **免费 × 1 年** | Anthropic 创业扶持（SF Tech Week）：成立 ≤5 年可 **免费用 Claude Team 一年（5 席）+ $1000 API 额度** |

---

## 🔥 今日头条 · 三条主线

### ① 新模型 · 免费档可用｜Anthropic 发布 **Claude Haiku 5.5**：**免费版 Claude 应用就能用**，**$0.10 / $0.50**

**本期唯一一条「旗舰级新模型直接对免费用户开放」——不是免费 API，而是把 Haiku 级模型放进了免费版 Claude 应用。**

当地时间 10/7，Anthropic 发布 **Claude Haiku 5.5**，是 Claude 5.5 家族的第三款（前有 Opus 5.5 与 Sonnet 5.5）。

**💵 定价与规格**

- **输入 $0.10 / 百万、输出 $0.50 / 百万**（prompt ≤100K）；**>100K 升到 $0.50 / $2.50**；
- **比 Haiku 4.5 便宜约 75%**，官方称「迄今最快的小模型」；
- **1M 上下文 / 128K 最大输出**；Haiku 级**首次支持 effort 档**（自适应思考）；知识截止 2026 年 6 月。

**🎁 免费入口在哪（关键）**

- **官方口径：即日起在「所有平台」提供，包括免费版 Claude 应用（网页与 App）**；
- API 侧同步上架 OpenRouter `anthropic/claude-haiku-5.5`（**1M、$0.10/$0.50**）与 OpenCode Zen `claude-haiku-5-5`；另可在 AWS Bedrock / Google Cloud / Microsoft Foundry 调用；
- **⚠️ 免费只发生在 Claude 应用这一层，API 侧仍按量计费。**

**📈 能力定位**

- **OSWorld 2.1（电脑操作）超 OpenAI GPT-6 Luna**；可作为 **Opus 5.5 / Sonnet 5.5 的子智能体**用于编码；
- 面向：**分类、摘要、抽取、实时客服、语音 agent、应用内助手**——典型「高频、低成本」工作；
- **Anthropic 首个内置「窄域高危网络安全请求」防护的 Haiku；Max / Team 订阅另赠每月 API 额度。**

**⚠️ 迁移注意**

- **为 Haiku 4.5 写的代码在 5.5 上会 break**：手动 extended thinking（`budget_tokens`）返回 400；
- **adaptive thinking 默认开启**，响应可能以 thinking 块开头；相同文本会计入更多 token；
- **一句话：Claude 5.5 三档（Opus → Sonnet → Haiku）到齐，「小模型免费档」这一格由 Haiku 补上。**

---

### ② 新模型 · 开源路线｜Mistral 发布 **Large 4**：**1.05T MoE / 49B 激活 / 1M 上下文**，**月底开源权重**

**欧洲开源路线的旗舰：把万亿级 MoE 的激活压到 49B——意味着「前沿级能力」有机会以「可自托管」的形态落到免费侧。**

当地时间 10/6，Mistral 发布 **Mistral Large 4**（内部代号 ML4），公开预览状态。

**🧬 规格**

- **1.05T 总参数 / 49B 激活**（约 4.7%）、**1.6B 视觉编码器**、**1M 上下文**；文本 + 图像输入；
- **原生支持 160+ 语言（含全部欧盟官方语言）**；支持函数调用、结构化输出、文档问答、批处理与 Agents / Conversations API；
- 在自有欧洲数据中心的 **3,800 块 NVIDIA Grace Blackwell** 上训练。

**💵 定价**

- **标准 $1.36 / $4.18 per M**（缓存输入 $0.14）；**预览期打折 $0.68 / $2.09、缓存 $0.07**；
- OpenRouter `mistralai/mistral-large-4-0`（**512K、$0.68 / $2.09**），OpenCode Zen `mistral-large-4`（**均付费**）；
- **⚠️ 目前没有任何免费 API 入口。**

**📈 跑分**

- **DeepSWE v1.1 61.7%** / SWE-Atlas-QnA 59.4% / **Terminal-Bench 4 28.3%** / AutomationBench 59.9%；
- **Cybench 网络安全 93%**、AA Cyber Index 82%；Surge AI 编码人工评测 **3.74 / 5**（对比 Opus 5 的 4.22、GLM-5.3 的 3.6）；
- **强项：编码 agent、长终端流程、安全、金融与法律文档。**

**🎁 为什么它对「免费」有意义**

- **官方承诺月底发布权重**（许可证待公布）。参照 **Mistral Large 3 是 Apache-2.0**、长期出现在各类免费托管与自建清单里——**Large 4 若沿用开放许可，月底就会多一条「可自托管的前沿级」选项**；
- **建议：现在把它记进候选清单，10 月底回来核一次许可证。**

---

### ③ 免费池 · 换血｜OpenRouter **20 → 20** 但**两进两出**；Zen 免费 ID **13 个**，新增 3 条

**本期没有「数量变化」的戏剧性，但质地换了一遍——旧的两条先进免费模型下线，新的两条补位；Space Bunny 少了一个入口。**

**🔄 OpenRouter（脚本 10/8 清点）**

- 目录 **464 → 467 款（+3）**，**零价仍 20 款（`:free` 16 款）**；
- **进**：`apodex/apodex-1.1-mini:free`（**262K**、长程研究与预测向）、`inclusionai/ling-3.1-flash`（**560B/25B 激活、262K、混合推理——零价但不带 `:free` 后缀**）；
- **出**：`qwen/qwen3.8-27b:free`（**连续 429、长期探不到，本期下架**）、`stealth/space-bunny-alpha`（**从 OR 撤出**）。

**🖥️ OpenCode Zen**

- `/zen/v1/models` **84 → 87 款**；带免费标记 ID **13 个**：**新增** `exo-free`、`fledge-alpha-free`、`ling-3.1-flash-free`；**移除** `deepseek-v4-flash-free`、`mimo-v2.5-free`；
- 另上架**付费** `claude-haiku-5-5` 与 `mistral-large-4`；
- **⚠️ 条款分三类**：Space Bunny / LongCat 2.5 = 零保留、不用于训练；**Exo / Fledge / Ling / MiMo / Big Pickle = 免费期数据可能用于改进模型**；Nemotron 两条 = NVIDIA 试用端点，**勿传个人 / 机密数据**。

**🐰 Space Bunny 少了一个入口**

- 它在 OR 的零价条目**本期消失**，**但 Zen 侧 `space-bunny-free` 仍在**；三入口（OR / Zen / Command Code）→ 至少 **OR 这一条要打问号**；
- **纪律：把匿名模型写成变量而不是常量。**

**🧭 怎么读这个「20 → 20」**

- **「数量踩住、质地继续换」是近三期的固定模式**：新上架模型越来越先进，**但几乎全部落在付费侧**；
- **免费侧的补给只剩 stealth 与 preview**——来得快、走得更快，**把「今天就能跑完」当成规划单位**；
- **stealth 寿命记录**：ox-alpha 6 天 → union-alpha 不到 2 天 → Space Bunny 约两周 → 本期 exo / fledge / ling-3.1-flash 顶替。

---

## 🌤️ 次要更新 · 值得记一笔

- 🎁 **Anthropic 创业扶持**：10/6 SF Tech Week 推出——**成立 5 年内或近两年获融资的初创，可免费用 Claude Team 一年（最多 5 席）+ $1000 API 额度**；**本期唯一一条「面向真实项目、可持续一年」的免费额度**。
- 🆓 **OpenCode Zen 一次补进三条免费**：`exo-free`、`fledge-alpha-free`、`ling-3.1-flash-free`，移除 `deepseek-v4-flash-free` 与 `mimo-v2.5-free`（后者原定 10/21 下线、**本期提前移除**）——**「产品下线 → 免费档先撤」通常早于官方日期。**
- 🧾 **免费网关与厂商新条目**：**BazaarLink**（2 款免费模型 `qwen/qwen3.7-flash`、`deepseek/deepseek-v4-flash-0731`；免绑卡，10 RPM + 50 加权单位/日）、**APInex**（`free/` 前缀 9 款 1M 模型）、**Nous Portal**（$0 档 7 款 `:free`：Ling 3.0 Flash Fin / Step 3.7 Flash / LongCat 2.0 & 2.5 Preview / Laguna S 2.1 / Ling 3.0 Flash Sante / Laguna XS 2.1）。
- 📈 **平台口径**：**OpenRouter 467 款 / 20 零价 / 16 `:free`**；新增付款侧含 `anthropic/claude-haiku-5.5`、`mistralai/mistral-large-4-0`、`google/gemini-nano-banana-2.1`、`unbiased/pareto-26.10-preview`、`nvidia/switchyard`（开源路由模型）；**Zen 84 → 87、免费 ID 13 个**；**freellm.net 495+ 款 / 30 家平台 / 231 款实时验证**（榜首 NIM `z-ai/glm-5.3` 96、`z-ai/glm-5.3-flash` 95）。
- ⚠️ **滞后实证（本期）**：**CostGoat 等聚合页仍把已下架的 `qwen/qwen3.8-27b:free` 与 `stealth/space-bunny-alpha` 列为免费 / Online**，而官方接口里已不存在——**「是否还在免费」一律回官方接口复核。**

---

## 🧾 今日免费入口速查（先进 + 量大优先）

| 入口 | 免费额度 | 模型量级 | 状态 / 注意 |
| --- | --- | --- | --- |
| **免费版 Claude 应用** 🔵 新增 | 免费档可用（App / 网页） | **Haiku 5.5**，1M / 128K 输出 | **本期唯一的「旗舰级新模型免费入口」**；无需 key、无需绑卡；API 侧仍计费 |
| **Google AI Studio** | 免绑卡（每项目日额度） | Gemini 3.8 / 3.7 / 3.6 Flash，**1M** | **长期兜底首选**；3.x Pro 不在免费档；输入可能用于改进模型 |
| **NVIDIA NIM** `z-ai/glm-5.3` | **40 RPM**、不限调用量（需手机验证） | 1.3M；榜单 96 分 | 同站 `glm-5.3-flash`（95）与 `Kimi K3`（90）；**须手机验证** |
| **OpenRouter** `nemotron-3-ultra-550b-a55b:free` | $0 / $0（200 请求/日） | 550B / 激活 55B，**1M** | **零价池里量最大、最稳的一条**；NVIDIA 试用端点，勿传机密数据 |
| **OpenCode Zen** `exo-free` / `fledge-alpha-free` 🔵 新增 | 四列全 Free（限时） | 匿名 / 预览类 | **三天前还没有的两条**；免费期数据可能用于改进模型，别喂机密 |
| **Nous Portal** | $0 档含 7 款 `:free` | Ling / Step / LongCat / Laguna | `inference-api.nousresearch.com/v1`；免绑卡、标准限速 |
| **智谱 z.ai** | 输入输出全 Free、无到期日 | `GLM-4.7-Flash` 等，国内直连 | **唯一可以写进长期依赖的一类**；双节活动已结束，永久档仍在 |
| **Mistral Large 4** 🔜 月底开源权重 | 预览期 $0.68 / $2.09（仍付费） | 1.05T / 49B 激活，**1M** | **月底权重放出后可能出现免费托管**，先记进候选 |

**📌 长期兜底组合（无到期日那一类）**

- **智谱 z.ai** — `GLM-4.7-Flash` / `GLM-4.5-Flash` / `GLM-4.6V-Flash` **输入输出全 Free，无到期日**（国内直连）；
- **Google AI Studio** — **Gemini 3.x Flash 免绑卡**，每项目按日额度；
- **NVIDIA NIM** — **40 RPM、不限调用量**，含 `glm-5.3`（1.3M）与 `Kimi K3`（1M）；**需手机验证**；
- **Groq** — **30 RPM / 1,000 请求/日**（`gpt-oss-120b` 等）；**已从免费档下掉 Llama 系**；
- **美团 LongCat** — **每天 5,000 万 token**（官方平台）；
- **Cloudflare Workers AI** — **每天 1 万 neurons**；**OVHcloud AI Endpoints** — **匿名免注册 9 款**，2 RPM；
- **FreeLLMAPI（自托管，MIT）** — **34 家 / 635 端点 / 约 7.4 亿 tokens·月**。

> 组合建议：**主力**用一条稳的（NIM / 智谱永久免费档 / Google AI Studio），**兜底**用无到期日的（LongCat / InternLM），**试用**用限时券与 stealth（exo-free / fledge-alpha-free / LongCat 2.5）。本期的态度不变：**「免费」这一层之外，把 $10/月级订阅的门槛也算进来。**

---

## 🔎 平台盘点 · 今日快照

**📊 OpenRouter：467 款中 20 款零价（`:free` 16 款）**

- 脚本清点时刻：**467 款（较 9/30 +3）**，其中**输入与输出同时为 $0 的共 20 款**（持平），**带 `:free` 后缀 16 款**（持平）；
- **本期零价池「两进两出」**：进 `apodex/apodex-1.1-mini:free`、`inclusionai/ling-3.1-flash`；出 `qwen/qwen3.8-27b:free`、`stealth/space-bunny-alpha`；
- **四条「零价但不带 `:free`」**：`inclusionai/ling-3.1-flash`、`google/lyria-3-pro/clip-preview`（输出音频）、`openrouter/free`（200K 自动路由池）；
- **1M 且 $0 的条目 6 条**：nemotron-3.5-lightning:free、nemotron-3-ultra-550b-a55b:free、inkling:free、inkling-small:free、lyria-3-pro/clip-preview。

**🆓 零价池近六期流水（输入与输出同时为 $0 的口径）**

| 日期 | 目录总量 | 零价池 | 其中 `:free` | 零价净增减 |
| --- | --- | --- | --- | --- |
| 9/24 | 457 | 24 | 20 | +1 / -1 |
| 9/28 | 458 | 21 | 17 | +0 / -3 |
| 9/29 | 460 | 20 | 16 | +0 / -1 |
| 9/30 | 464 | 20 | 16 | +0 / -0 |
| **10/8（今天）** | **467** | **20** | **16** | **+2 / -2** |

**🔧 OpenCode Zen：84 → 87 款，免费 ID 13 个**

- `/zen/v1/models` 返回 **87 款**（较 9/30 的 84 款 +3）；**新增五条**：免费 `exo-free`、`fledge-alpha-free`、`ling-3.1-flash-free`，付费 `claude-haiku-5-5`、`mistral-large-4`；**下架两条**：`deepseek-v4-flash-free`、`mimo-v2.5-free`；
- 带免费标记的 ID 共 **13 个**；⚠️ 官方定价页 Free 行仍列 `mimo-v2.5-free`，而接口已移除——**以接口与实际调用为准**；
- 📖 **数据条款三类**：Space Bunny / LongCat 2.5 = 零保留、不用于训练（最干净）；Exo / Fledge / Ling / MiMo / Big Pickle = 免费期数据可能用于改进模型；Nemotron 两条 = NVIDIA 试用端点，勿传个人 / 机密数据。

**🌐 freellm.net：495+ 款 / 30 家平台 / 231 款实时验证（2026-10-07）**

- 榜首 **NVIDIA NIM `z-ai/glm-5.3`（96 分，1.0M、最多 40 RPM）**、次席 **`z-ai/glm-5.3-flash`（95 分，1.0M）**；
- **Ollama Cloud `deepseek-v4-pro`（91）**、**Kilo Code `qwen3.8-27b:free`（91）**、NIM `Kimi K3`（90）、Gemini 3.8 Flash（90）、LLM7.io `GLM-5.3-Flash`（89）、OVHcloud `Qwen3.8-27B`（89）、OpenRouter `Ling 3.1 Flash`（88）；
- **用法建议**：把它当「发现新模型与新平台」的入口，**但「是否还在免费」一律回官方定价页或官方 API 复核。**

---

## 📅 到期日历 · 别踩空

**刚过去（10/7 前后，如未续期）**：智谱 GLM-5.3-Flash 夜间畅用 + 全天五折结束、**ZCode 每日 1 亿 Token 券发放结束**（永久免费档不受影响）、MiniMax Code 双倍签到结束。

**10 月中下旬及以后**

- **10/10** — DeepSeek 低谷价窗口结束；腾讯混元 Hy4 preview（老用户夜间免费）结束；
- **10/15** — **阶跃 Step 5 Preview 释放完整 BF16 权重**（许可证待公布）；
- **10/17** — 豆包全用户 30 天订阅（9/24 那轮）截止；
- **10/21** — **小米 `mimo-v2.5-pro` / `mimo-v2.5` 正式下线**（Zen 侧 `mimo-v2.5-free` **本期已提前移除**）；
- **10/31（月底）** — **Mistral Large 4 发布开源权重**（许可证与托管渠道届时见分晓）；
- **11/7** — MiniMax 开放平台 M3 / M2 免费试用到期；
- **12/31** — 腾讯云 TokenHub / 华为云码道 / 移动云 MoMA 年度额度截止。

---

## 🧭 今天该怎么动

**① 现在就做（10 分钟内）**

- **打开免费版 Claude 应用，试一遍 Haiku 5.5**——本期唯一「旗舰级新模型直接对免费用户开放」的入口；**用真实「分类 / 摘要 / 抽取」任务测，而不是 hello world**；
- **注册 Nous Portal 或翻一遍 OpenCode Zen**——Zen 本期新进三条免费（`exo-free`、`fledge-alpha-free`、`ling-3.1-flash-free`），**三天前还没有，当天跑完评估**；
- **翻一遍配置里写死的免费模型名**——`qwen/qwen3.8-27b:free` 已下架、`stealth/space-bunny-alpha` 已从 OR 撤出，**请求会直接失败**。

**② 今天之内**

- **把零价池里「1M 上下文」的那几条跑一遍**——本期还剩 **6 条**，其中 **`nemotron-3-ultra-550b-a55b:free` 是「量大 + 长期在线」的那一条**，先用它把长文档任务跑通；
- **把 Mistral Large 4 记进候选清单**——**1.05T / 49B 激活、1M、DeepSWE 61.7%**，现在只有付费入口，**但官方承诺月底放出权重**。

**③ 本周之内**

- **盘点一次「你还有资格领的免费额度」**——尤其 **Anthropic 创业扶持（免费 Claude Team 一年 + $1000 API 额度）**，符合条件的团队去核一次资质；
- **给免费通道按可靠性分层**——永久免费档（智谱 Flash / Google AI Studio）→ 厂商试用端点（NIM）→ 免费应用层（Claude 免费版）→ 限时券（exo / fledge / LongCat 2.5）→ stealth（Space Bunny）；**生产链路只用前两层**；
- **盯三个日期**——**10/10**（DeepSeek 谷时价、腾讯 Hy4 preview）、**10/21**（小米 MiMo-V2.5 全线下线）、**10/31**（Mistral Large 4 开源权重）；
- **留意两条「还没落地的预期」**——**Claude Haiku 5.5** 会不会进一步下探到免费 API 侧；**Mistral Large 4 的许可证**是 Apache-2.0 还是更严。

---

> ⚠️ 免费额度可能随时调整，请以各平台官网最新政策为准。本页所有「免费」判定均以官方接口或官方定价页为准。OpenRouter 免费池日内会波动，467 款 / 20 款零价 / 16 款 `:free` 是脚本清点时刻的快照。
> **Claude Haiku 5.5 的「免费」指免费版 Claude 应用 / 网页可用；API 侧仍按量计费。** Mistral Large 4 当前仅有付费入口，「月底开源权重」为官方公告，许可证类型待公布。
> 📅 生成时间：2026-10-08 · 本页由自动化任务每日生成。
