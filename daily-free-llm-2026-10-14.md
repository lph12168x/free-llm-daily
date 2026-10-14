# 每日免费大模型日报 · 2026-10-14

> 自动生成 · 在线版：[daily-free-llm-2026-10-14.html](daily-free-llm-2026-10-14.html)
> 仓库：[lph12168x/free-llm-daily](https://github.com/lph12168x/free-llm-daily)

## 📰 今日摘要（2026-10-14）

> 本期主线：**免费池开始收缩**——OpenRouter 零价池 **连续 4 期零进出被打破、两连出（19→17）**；大厂侧 **Gemini 4 Argon 旗舰进聚合渠道**（付费、无免费档）；而真正的重磅在明天——**10/15 Step 5 Preview 开源完整权重**。

| 数字 | 含义 |
| --- | --- |
| **19 → 17** | **OpenRouter 零价池两连出**：`apodex-1.1-mini:free` 整体下架（10/8 上架、**仅存活 6 天**）、免费档智能分第一（41.1）的 `ling-3.1-flash` **转付费**退出零价池；`:free` **15→14**；目录同步移除 ling-3.0-flash-sante / ling-3.0-flash-fin / 旧版 pareto——**蚂蚁 Ling 系在 OR 的免费存在基本清零** |
| **$2 / $10** | **Gemini 4 Argon 上架 OpenRouter（batch 半价 $1/$5）与 Zen（5 折）**：Google 9/30 受控发布的旗舰，**单次输出上限 64K→1M**、DeepSWE v1.1 **77.9% 当前最高**、19 项基准 13 项领先；推广期价格**官方明示后续将涨价**，无免费档 |
| **$0 输出** | **scaledown summarize / extract 上架 OR**：1M 上下文、**输出 $0**、输入仅 $0.04/M——摘要 / 结构化抽取近乎白嫖，「输出免费」赛道继续扩容 |
| **明天 10/15** | **Step 5 Preview 开源完整权重**（600B/27B、1M、文本+视觉）：开源落地 = 免费不再依赖任何限免窗口；WorkBuddy 限免同步进行至 **10/25** |

---

### 📉 **OpenRouter 免费池收缩：连续 4 期零进出被打破**

与 10/13 快照逐条比对：零价池同时出两个——`apodex-1.1-mini:free`（10/8 才上架）整体下架；`inclusionai/ling-3.1-flash` 转付费退出零价池。**聚合榜（modelgrep 等）仍把 ling-3.1-flash 标为免费第一，已滞后**。免费档优先改用：**inkling-small:free**（1M、智能分 25.7）、**nemotron-3.5-lightning:free**（1M、81 t/s）、gemma-4-31b、nemotron-3-ultra-550b（1M）。

### 🌌 **Gemini 4 Argon 进聚合渠道：1M 输出的旗舰，无免费档**

OpenRouter `google/gemini-4-argon` **$2/$10**、batch **$1/$5**；Zen 同步上架并标 5 折。规格：**单次输出上限 64K→1M**（多数前沿模型仅 ~128K）、DeepSWE v1.1 77.9%、Vals Index 企业知识第一、长视频 LVBench 91.7%；缓存输入比标准低 95%。想白嫖同级的仍只有 **AI Studio 免费层的 Flash 系**（10 RPM / 20 RPD，未受 App 砍档影响）。

### 📊 **接口清点（13:11）与隐身扩散**

- **OpenRouter**：目录 **459→462** / 零价 **19→17** / `:free` **14**。新增：gemini-4-argon（+batch）、liquid/lfm-2.5-24b-a2b、unbiased/pareto-26.9（+latest）、**scaledown summarize / extract**（输出 $0）。
- **OpenCode Zen**：接口 **84→86**（+gemini-4-argon 5 折、+内部 test），免费 ID **11 不变**。⚠️ **定价页与接口「打架」**：页面 Free 行仍列 Exo / MiMo-V2.5 / Ling 3.0 Fin / Nemotron 3 Ultra 四条，但 API 已无对应端点——以接口为准，这几条随时可能正式退场。
- **隐身扩散**：Command Code 的 `stealth/glyph-cluster:free`（256K、全档免费、100 请求/日）本周扩散至 **Vercel AI Gateway**——一个隐身模型多渠道铺货。⚠️ 官方标注**不走 ZDR**、数据可能用于训练。Nous Portal `stealth/missingno` 仍在。
- **长期白嫖口**：NVIDIA NIM（GLM-5.3 周 4T tokens）、Groq（1K 请求/日）、Cloudflare（1 万 neurons/日）、豆包 200 万 tokens/日、商汤 Token Plan 不绑卡、讯飞 Spark Lite 永久免费、**OVHcloud 免注册匿名即用**（8 款 Qwen / Mistral / Llama，2 RPM）。

### ⏰ **到期红线**

- **10/15（明天）** — **Step 5 Preview 开源完整权重**（同在 WorkBuddy 限免期内）
- **10 月中旬** — **Kimi K3.1** 传发布（野村消息：Agent 长任务、百万上下文、三档推理强度；未官宣）
- **10/25** — **腾讯 WorkBuddy 独家限免结束**；**本月内** — Beam 权重 Apache 2.0、Mistral Large 4 权重约 10/27
- **趋势** — 免费 API 池开始收缩；增量在**开源权重 + 隐身限免 + 输出免费专用模型**三条线

> **口径说明**：本页数字为脚本清点时刻快照（**2026-10-14 13:11 GMT+8**，与 10/13 快照逐条比对）。OpenRouter 零价池按 `prompt=='0' and completion=='0'` 统计，「零价但无 `:free` 后缀」的模型也已计入；Zen 以**接口免费 ID 数为准**（定价页 Free 行仅作参考，今日两头打架）。第三方聚合榜与官方目录存在滞后与计数差（modelgrep 今日仍把已转付费的 ling-3.1-flash 标为免费第一），请勿单独据其做结论。「开源」指权重公开，不代表可自由商用。**glyph-cluster / missingno 等隐身或「数据可能用于训练 / 仅限试用」的通道：不要把机密代码、个人信息或生产客户数据放进去。**

---

