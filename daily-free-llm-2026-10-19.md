## 📰 今日摘要（2026-10-19）

> 本期主线：**Reflection Beam 1.0 权重开源**（Apache 2.0，501B/23B、1M）——隐身三连揭晓：OpenCode `cat-jam`、Nous `MissingNo` 都是它，免费入口 5 处同时在线；**中国电信 TeleAI Xing4.0** 上 OR 免费档；Zen 空降新隐身 `ll-alpha-free`（仅定价页可见）。

| 数字 | 含义 |
| --- | --- |
| **501B 开源** | **Beam 1.0 权重开源**（10/16）：Apache 2.0、不禁蒸馏；BF16≈934GB / FP8≈469GB / NVFP4≈273GB + DFlash2 投机解码，自部署推荐 4×B300；自报 SWE-bench 81.6%、Terminal-Bench 2.1 80.1%，**AA 30 分＝美国开放权重第二**；OR 走 Nebius **$0.25/$1** |
| **5 处免费** | **Beam 免费入口**：Reflection 官 API **免费公测**、Zen `beam-free`、Vercel AI Gateway `reflection/beam-free`、Nous Portal；⚠️ 限免无截止日、**无 ZDR（30 天留存）**，Zen 侧对中国大陆及港澳不可用 |
| **18 → 19** | **OR 零价池 +1**：+`xingchen-agi/xing4.0-29b-a4b:free`（中国电信 TeleAI，29B/4B、原生 256K、工具调用+结构化输出、**200 请求/日**；权重开源，GGUF **16GB 内存可跑**）；付费新上架 beam-1.0、deepseek-v4.1-flash-1017（$0.30/$1.20）、pareto-26.10、elorian/glimpse、qwen3.7-plus:batch；目录 465→471 |
| **86 → 85** | **Zen 免费 ID 11→10**：+`beam-free`、+`glm-5.3-flash-free` 回归；−`cat-jam-free`（揭晓下架）、−`muse-spark-1.2/1.3-contributor-free`（贡献者免费撤销）；⚠️ 定价页 Free 行 **14** vs 接口 10，**新隐身 `ll-alpha-free`（30 天留存）仅页面可见**，以接口为准 |

---

### 🧠 **Beam 1.0：权重开源落地，隐身谜底一次揭开**

Reflection AI 首个开放权重模型 **Beam 1.0** 10/16 上线 HF：501B 总参 / 23B 激活稀疏 MoE、1M 上下文、256 专家，**Apache 2.0 且明示不禁蒸馏/微调/合并**。自报 SWE-bench Verified 81.6%、TB2.1 80.1%，AA 独立 30 分＝**美国开放权重第二**（仍落后中国第一梯队）。同日 **OpenCode `cat-jam`、Nous `MissingNo` 两个隐身模型揭晓均为 Beam**——隐身试用的标准剧本：匿名收集反馈、揭晓时转正。免费白嫖路径齐全：**Reflection 官 API 免费公测**、Zen `beam-free`、Vercel AI Gateway（可接 Claude Code / Cursor）、Nous Portal；OR 上 Nebius 托管仅 **$0.25/$1**。注意：限免无截止日、**不支持 ZDR**（30 天留存），公司代码别放。

### 🆓 **国产侧：Xing4.0 免费 + Nous 免费档上新**

- **中国电信 TeleAI（星晨）Xing4.0-29B-A4B**：10/16 上 OR 免费档，29B/4B MoE、原生 256K、支持工具调用与结构化输出；权重开源（GitHub/ModelScope），GGUF 后 **16GB 内存笔记本可跑**，繁中写作口碑好、代码推理一般。
- **Nous Portal 免费档扩容**：`stepfun/step-3.7-flash:free`（阶跃 5 月开源的 196B/11B、400 TPS）、`meituan/longcat-2.0:free`（1M）；UnoRouter / ZenMux / Kenari 也有 step-3.7-flash 免费镜像。
- **端侧再下探**：面壁 **MiniCPM-V 4.7**（10/13，35B-A3B 端侧 MoE）在 iPhone 17 Pro Max 上 **3GB 内存 13+ tok/s**。

### 📊 **接口清点（09:36）**

- **OpenRouter**：目录 **465→471** / 零价 **18→19**（仅 +Xing4.0:free，进出集中在付费档）。
- **OpenCode Zen**：接口 **86→85**，免费 ID **11→10**；定价页 Free 行 **14** vs 接口 10——**新隐身 `ll-alpha-free`（30 天留存）及 exo / mimo-v2.5 / nemotron-ultra 免费仅页面可见**，以接口为准。
- **隐身免费未动**：Command Code / Vercel / Kilo 的 `glyph-cluster:free`（$0，CC 档 100 请求/日）、Zen `big-pickle` / `space-bunny-free` 均在。
- **长期白嫖口**：NIM、AI Studio Flash 系、Groq、Cloudflare、豆包 200 万 tokens/日、商汤、讯飞 Spark Lite。

### ⏳ **到期红线**

- **10/27** — **Mistral Large 4 权重开源**（1.05T/49B，Cybench 93%、漏洞复现修补 82% 全场最高；Reuters 口径）
- **10 月内（传闻）** — **Kimi K3.1**（野村传中旬，今日未至）、Fable 5.5、Grok 4.8、GPT-6.1 Sol Ultrafast
- **11/30** — Zen 上 **Gemini 4 Argon 5 折**（$2/$10）截止
- **soon** — **Space Bunny 揭名**（OR 官方口径）；Zen `ll-alpha-free` 身份待揭晓

> **口径说明**：本页数字为脚本清点时刻快照（**2026-10-19 09:36 GMT+8**，与 10/16 快照逐条比对）。OpenRouter 零价池按 `prompt=='0' and completion=='0'` 统计，「零价但无 `:free` 后缀」的模型也已计入；Zen 以**接口免费 ID 数为准**（定价页 Free 行仅作参考）。第三方聚合榜与官方目录存在滞后与计数差，请勿单独据其做结论。「开源」指权重公开，不代表可自由商用。**隐身或「数据可能用于训练」的通道：不要把机密代码、个人信息或生产客户数据放进去。**

---

