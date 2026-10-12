# 每日免费大模型日报 · 2026-10-12

> 自动生成 · 在线版：[daily-free-llm-2026-10-12.html](daily-free-llm-2026-10-12.html)
> 仓库：[lph12168x/free-llm-daily](https://github.com/lph12168x/free-llm-daily)

---

> 午后复检结论：**两家接口日内基本按兵不动**（OpenRouter 458 / 19 与上午 09:18 逐条一致；Zen 仅多一条非免费备份端点），真正的新增全在**「今天就能用的免费入口」**——阶跃 **Step 5 Preview 上线腾讯 WorkBuddy 独家限免（10/12–10/25）**，外加**决策模型「输出免费」**与**第二批隐身免费模型**两股新风。

| 数字 | 含义 |
| --- | --- |
| **10/12–10/25** | **阶跃 Step 5 Preview 上线腾讯 WorkBuddy 独家限免**：**600B 总参 / 27B 激活**稀疏 MoE、**1M 上下文**、原生**文本 + 视觉**输入；面向 AI 编程 / 软件工程 / 专业知识工作 / 金融；官方确认 **10/15 开源完整权重** |
| **458 / 19 · 83** | **午后复检：OpenRouter 目录 458、零价 19、`:free` 15——与上午 09:18 完全一致（日内零变动）**；OpenCode Zen 接口 **82 → 83**（仅 +`claude-opus-5-5-backup`，非免费），免费 ID 仍 **9 个** |
| **输出 $0** | **决策模型「输出免费」成新赛道**：Microsoft **Decision-1**（Qwen3.5-9B 后训）**$0.042 / 百万输入、输出免费**、32K、中位 85ms；同赛道还有 Cloudflare **Clef-omni**（开放权重、音视频）、Liquid **d1-3B**（开源权重）、Nace.AI **Drex 1.5**、TypeSafe **Jev**（A 轮 **$8.7 亿**、估值 **75 亿**） |
| **2 枚隐身** | **Nous Portal `stealth/missingno`**（10/10 起 **$0 / 百万**）、**Command Code `stealth/glyph-cluster:free`**（**256K**、全档免费）——**规模、权重、截止日全部未公布，随时下线，别投生产** |
| **国内侧** | 智谱「回工三连」：**10/12 登录送 1 亿 tokens、10/13–16 每天补发 800 万（五天累计 1.32 亿）**；官方**永久免费 API** 实为 `GLM-4.7-Flash`（200K，**并发仅 1**） |
| **趋势判断** | 免费 API 两端**同时缩表**；增量在**开源权重**与**新品类（决策模型输出免费）**——前者不会断供，后者把单位成本压到近零 |

---

### 🎯 **阶跃 `Step 5 Preview` × 腾讯 WorkBuddy：10/12–10/25 独家限免**

**今日新增的「最能用的免费入口」**：阶跃 StepFun 于 **10/12 12:58** 宣布 Step 5 Preview 上线腾讯 WorkBuddy，**2026-10-12 至 10-25 独家限免**。**规格**：**600B 总参 / 27B 激活**稀疏 MoE、**1M 上下文**、原生**文本 + 视觉**输入，面向 AI 编程、软件工程、专业知识工作、金融等真实 Agentic 任务。**与上午那条的关系**：上午写的是 OpenRouter / OpenCode / Cline / Nous / Kilo 的「免费约一周」，本条是**官方合作渠道**——日期明确、覆盖到 10/25，且 **10/15 将开源完整权重**，到期后仍可自托管。**🧭 行动建议**：今天就把最吃上下文的自有任务（整库问答 / 长文档 / 多步 Agent）在 Step 5 上跑一遍；**10/15 再用同一批任务对比自托管权重**，决定是否写进架构。**⚠️ 限免通道的数据条款以各平台为准，别把限免期当 SLA。**

### 🧮 **今日第二主线：决策模型「输出免费」——大厂一周内扎堆进场**

**判定正在变成一种廉价零件**。决策模型不生成文本，而是**一次前向**读入「状态 + 固定选项」、直接回**校准概率**，因此可以**输出 0 计费**：

- **Microsoft `Decision-1`（10/9）**：**Qwen3.5-9B** 后训，在 **Foundry 与 OpenRouter** 上线，**输入 $0.042 / 百万 tokens、输出免费**、**32,768 上下文**、中位 **85ms**（p95 125ms）；官方 36 基准 147,137 题准确率 **83.5%**。用于工单路由、事故分级、内容过滤、给 Agent 的下一步打分。**⚠️ 口径核实**：官网已列 OpenRouter，但 **OpenRouter 的 `/models` 接口今日仍未收录**（458 条里查无此条）——以官方页为准。
- **Cloudflare `Clef-omni`**：**开放权重**，音 / 视频 / 图 / 文一次调用打分（基于 Qwen3-Omni-30B-A3B，去掉语音生成）。
- **Liquid `d1-3B`（10/8）**：**开放权重**、单次前向出类型化答案、**零输出 token**，已上 HuggingFace。
- **Nace.AI `Drex 1.5`**：9B 决策模型，Decision Index 0.3.1 得 **58.08**；权重在 HF、托管在 OpenRouter。
- **TypeSafe `Jev`**：凭决策模型拿到 **A 轮 8.7 亿美元、估值 75 亿美元**（约 1/3 的财富 500 强在用）。

**给你的用法**：Agent 里高频、重复的**确定性判定**（路由 / 门控 / 打分）从「让聊天模型写理由再解析」换成「**一次前向拿概率**」，成本与延迟都塌一个量级。

### 🕵️ **第二批「隐身免费」：MISSINGNO 与 Glyph Cluster**

- **Nous Portal `stealth/missingno`（10/10 起）**：Nous Research 称其为「**高 token 效率的编码与 Agent 推理模型**，限时免费」，Portal 目录标 **$0.00 / 百万**，可在 Hermes Agent 直接用。**已知**：编码 + Agent 方向、自称 token 高效（无数字佐证）。**未公布**：参数量、上下文、跑分、权重是否开放、截止日与之后价格。
- **Command Code `stealth/glyph-cluster:free`**：新增隐身**推理**模型，**256K 上下文**，**对所有档位免费**（含 $1 入门档），调用 `cmd --model stealth/glyph-cluster:free`。这是 Command Code **连续第三个**隐身免费模型（前有 Space Bunny Alpha、Pixel Canary）——**「隐身 + 全档免费」已成招商标准动作**。

**⚠️ 共同风险**：条款不透明、随时下线、**很可能用你的数据**；只做试验，不投生产。

### 🔄 **接口清点（13:15 复检）：两家日内按兵不动**

- **OpenRouter**：目录 **458 款**、零价 **19 款**、带 `:free` 后缀 **15 款**——与上午 09:18 快照**无一条进出**。零价池里量最大的仍是 **Nemotron 3 Ultra 550B**（1M）与 **Nemotron 3 Super 120B**；**Thinking Machines Inkling / Inkling Small**（1M、多模态）紧随。易漏计：`inclusionai/ling-3.1-flash` **零价但不带 `:free` 后缀**。
- **OpenCode Zen**：接口 **82 → 83**，唯一新增为 `claude-opus-5-5-backup`（**备份端点，非免费**）；**免费 ID 仍 9 个**（含隐身 `big-pickle`），官方定价页 **Free 行 13 条为准**。免费主力：**Step 5 Preview Free**、**Space Bunny Free**、**LongCat 2.5 Preview Free**（三者 ZDR）、**Muse Spark 1.3 Contributor Free**（Meta，换数据训模型）、**Jev 1.13 Free**、**MiMo-V2.6-Flash Free**、**Nemotron 3.5 Lightning Free**、**Ling 3.1 Flash Free**、**Big Pickle**。

**读法**：免费 API 两端**同时缩表**且日内停滞；**增量已不在「送 API 额度」，而在「开源权重」与「新品类便宜入口」**。

### 🇨🇳 **国内侧：智谱「回工三连」+ 永久免费口径澄清**

- **发放节奏**：**10/12 登录直发 1 亿** tokens；**10/13–10/16 每天补发 800 万**；五天累计约 **1.32 亿**，零门槛。
- **⚠️ 别被「4 亿」带跑**：网传「普通用户最高 4 亿」是第三方按**非高峰半价 + 98% 缓存命中**估出的**等效量，不是发放额度**；按真实直发量（约 1.9 亿）安排任务。
- **永久免费那条**：官方定价页底部问答里的**永久免费 API** 是 `GLM-4.7-Flash`（200K）与 `GLM-4.6V-Flash`，输入 / 输出 / 缓存三项全免，但**并发仅 1 条**——低频兜底可以，并发不行。
- **五折**：`GLM-5.3-Flash` 输入限时五折至 **0.4 元 / 百万 token**（Batch 同折）。

### 🧭 **今天怎么动 · 三条路**

**A · 要最强且免费** → **Step 5 Preview × WorkBuddy（10/12–10/25）**；或 Zen 的 **Step 5 Preview Free / Space Bunny Free**。**窗口短，当冲刺，不写进架构。** **B · 要天天有量** → 主力 **NIM（~1 万请求/日）**，备用 **Groq 1,000/日**、**Cloudflare 1 万 neurons/日**；国内用 **豆包 200 万 tokens/日** 或智谱永久档。**C · 要把判定做便宜** → 用**决策模型**替掉高频路由 / 门控 / 打分：**Decision-1（输出免费）**、**Clef-omni / d1-3B（开放权重）**现在就能试。

### ⏰ **到期 / 波动提醒**

- **本周内** — **Step 5 Preview** 各处免费窗口约一周；**Zen 各 Free 通道均为 limited time**，随时转付费
- **10/15** — **Step 5 Preview 开源完整权重**（同在 WorkBuddy 限免期内）
- **10/25** — **腾讯 WorkBuddy 独家限免结束**
- **本月内** — **Beam 权重 Apache 2.0 放出**（early-access 候补中）；**Mistral Large 4 开源权重约 10/27**
- **趋势** — 免费 API 两端同时缩表；增量在**开源权重**与**新品类（决策模型输出免费）**

> **口径说明**：本页数字为脚本清点时刻快照（**2026-10-12 13:15 GMT+8 午后复检**，与当日 09:18 上午快照逐条比对）。OpenRouter 零价池按 `prompt=='0' and completion=='0'` 统计，「零价但无 `:free` 后缀」的模型也已计入；Zen 以**官方定价页 Free 行为准**。第三方聚合榜与官方目录存在滞后与计数差（本期实证：**Microsoft-Decision-1 官网已列 OpenRouter，但 OpenRouter 的 `/models` 接口尚未收录**），请勿单独据其做结论。「开源」指权重公开，不代表可自由商用。**Big Pickle / Exo / MiMo / Ling / Muse Spark Contributor / Nemotron Free、以及 MISSINGNO / Glyph Cluster 等隐身或「数据可能用于训练 / 仅限试用」的通道：不要把机密代码、个人信息或生产客户数据放进去。**

---
