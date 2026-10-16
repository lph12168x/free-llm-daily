# 每日免费大模型日报 · 2026-10-16

> 自动生成 · 在线版：[daily-free-llm-2026-10-16.html](daily-free-llm-2026-10-16.html)
> 仓库：[lph12168x/free-llm-daily](https://github.com/lph12168x/free-llm-daily)

## 📰 今日摘要（2026-10-16）

> 本期主线：**Meta 重返开放权重**——**Muse Spark Open**（816B/42B 激活、1M、原生多模态）发布，号称"迄今美国最强开放权重模型"，还与苹果合作让两台 Mac Studio 即可本地跑；同时 **Step 5 免费窗如期关闭**，白嫖余温只剩 NIM 与自部署。

| 数字 | 含义 |
| --- | --- |
| **816B / 42B** | **Meta Muse Spark Open 开放权重**：1M 上下文、原生多模态（文/图/视频/音频）、主攻编码与 Agent；API **$1.25/$4.25** 上 OpenRouter 等 7 平台，权重上 HF / SageMaker / GCP / Foundry（Muse Model License 有限商用）；**与苹果合作 MLX 优化，两台 M5 Ultra Mac Studio（约 1TB 统一内存）本地可跑**；工具调用 6 项测试第一，但终端编程 / 长周期 SWE **仍落后 Kimi K3、GLM-5.3**，最强 Muse Wonder 维持闭源 |
| **$1 / $2.7** | **Step 5 Preview 免费窗如期关闭**（预测兑现）：Zen 已下架 `step-5-preview-free`，Cline / Nous / Kilo 10/15–16 恢复标价——免费一周烧掉 **12.1T tokens**（OR 周榜第二）；余温：**NVIDIA NIM 仍免费**（40 RPM）+ 10/15 权重已开源可自部署 |
| **17 → 18** | **OR 零价池转增**：**+`nemotron-3.5-super-vl:free`**（120B/12B 激活多模态、1M，Zen 同步上免费端点）、+meta/muse-spark-open、+moondream3 / moondream3.1（9B/2B VLM，$0.30/$2.50）；−claude-sonnet-4、−pareto-26.10-preview；目录 462→465 |
| **85 → 86** | **Zen 免费 ID 10**：进 `deepseek-v4.1-flash-free`（回归）与 `nemotron-3.5-super-vl-free`，出 `step-5-preview-free`；定价页 Free 行 13 vs 接口 10，以接口为准 |

---

### 🦙 **Meta Muse Spark Open：重返开放权重 + 携手苹果**

Meta 在 10/15（美东周四）发布开放权重模型 **Muse Spark Open**，自评"迄今美国能力最强的开放权重模型"。要点：**816B 总参 / 42B 激活稀疏 MoE、1M 上下文、原生多模态**，专为长周期 Agent 任务与复杂软件工程优化。权重上 Hugging Face / SageMaker / Google Cloud Model Garden / Foundry（**Muse Model License、有限商用**）；API 走 Baseten、Fireworks、Groq、Modal、Nebius、**OpenRouter**、Together。最大看点是与**苹果合作**：MLX 优化后**两台 M5 Ultra Mac Studio（各 512GB 统一内存，协同约 1TB）即可本地运行**。跑分方面工具调用 6 项测试第一，但**终端编程 / 长周期 SWE / GDPVal-AA 落后 Kimi K3 与 GLM-5.3**；首席 AI 官汪滔明说"最强模型通常不开源"——Muse Wonder 维持闭源，分层策略 = 开放权重铺生态、闭源保前沿。

### ⏰ **Step 5 免费窗关闭：营销窗口的完整生命周期**

上期预测今日兑现：Zen 下架免费档，Cline / Nous / Kilo 三处恢复 **$1/$2.7** 标价。复盘：免费一周贡献 **12.1T tokens**（OR 周榜全球第二），但 Arena 综合仅 83 名、输出又冗长——"免费榜排名" ≠ 真实口碑。白嫖不中断的两条路：**NVIDIA NIM 的 step-5-preview 仍免费**（40 RPM），**10/15 权重已开源**（BF16+FP8 上 HF/ModelScope），自部署随时可跑。

### 💻 **本地白嫖大扩容：Nemotron 3.5 Bolt + Moondream 3.1**

- **Nemotron 3.5 Bolt 74B-A9B**（10/15 全开源，权重+数据+配方）：2-bit 量化感知训练把 74B/9B 激活压进 **24GB**，llama.cpp / vLLM / Ollama / LM Studio 首日支持——单卡/笔记本本地 Agent 新选项。
- **Moondream 3.1**（9B/2B 激活 VLM）：开源小视觉模型，同步上架 OR（$0.30/$2.50）。
- 加上 Step 5 权重落地，**「自部署免费」供给线本周明显强于「限免 API」**。

### 📊 **接口清点（13:11）**

- **OpenRouter**：目录 **462→465** / 零价 **17→18** / `:free` **15**。进出见上表。
- **OpenCode Zen**：接口 **85→86**，免费 ID **10**；定价页 Free 行 13 与接口 10 口径差持续（exo / mimo-v2.5 / nemotron-3-ultra 页面在列、API 已无），**以接口为准**。
- **隐身免费未动**：Zen `cat-jam-free` / `big-pickle` / `space-bunny-free`、Nous `stealth/missingno`、Command Code `glyph-cluster:free` 均在。
- **长期白嫖口**：NIM（GLM-5.3、Step 5）、AI Studio Flash 系、Groq、Cloudflare、豆包 200 万 tokens/日、商汤、讯飞 Spark Lite。

### ⏳ **到期红线**

- **10 月内（传闻）** — **Fable 5.5、Grok 4.8、Kimi K3.1、GPT-6.1 Sol Ultrafast** 均传 10 月发布
- **10/31** — **Mistral Large 4 权重**（1.05T/49B）开源
- **soon** — **Space Bunny 揭名**（OR 官方口径，社区最猜 MiniMax M3.1-Flash-Preview）

> **口径说明**：本页数字为脚本清点时刻快照（**2026-10-16 13:11 GMT+8**，与 10/15 快照逐条比对）。OpenRouter 零价池按 `prompt=='0' and completion=='0'` 统计，「零价但无 `:free` 后缀」的模型也已计入；Zen 以**接口免费 ID 数为准**（定价页 Free 行仅作参考，两头长期打架）。第三方聚合榜与官方目录存在滞后与计数差，请勿单独据其做结论。「开源」指权重公开，不代表可自由商用。**隐身或「数据可能用于训练」的通道：不要把机密代码、个人信息或生产客户数据放进去。**

---

