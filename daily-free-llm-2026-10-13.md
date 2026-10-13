# 每日免费大模型日报 · 2026-10-13

> 自动生成 · 在线版：[daily-free-llm-2026-10-13.html](daily-free-llm-2026-10-13.html)
> 仓库：[lph12168x/free-llm-daily](https://github.com/lph12168x/free-llm-daily)

---

> 本期是「**小日子**」：免费 API 池连续 **4 期零进出**，真正的新增只有一条——**Zen 今晨空降隐身免费模型 `cat-jam-free`**（官方定价页都还没挂）。大厂侧的重头是 **Meta 首个前沿闭源模型 Muse Wonder**（付费、无免费入口，但已上 OpenRouter，路线变化值得记一笔）。

| 数字 | 含义 |
| --- | --- |
| **cat-jam-free** | **Zen 第 3 枚玩梗隐身免费模型**（big-pickle → space-bunny → cat-jam）：今晨现身 `/v1/models`，**全档 $0**；底层模型 / 参数 / 上下文 / 截止日**全部未公布**，定价页与文档 13:11 快照时**均未收录** |
| **459 / 19 · 84** | OpenRouter 目录 **458→459**（唯一新增 `meta/muse-wonder`，**付费**）；**零价池 19 连续 4 期零进出**、`:free` 15 不变；Zen 接口 **83→84**（唯一新增即 cat-jam-free），**免费 ID 9→10**，定价页 Free 行 13 |
| **$4 / $20** | **Meta Muse Wonder 发布**：首个前沿闭源系列（内部代号「西瓜」）、1M 上下文 / 943K 输出、全模态输入、强制推理；API **$4/$20 每百万**（对标 Opus 5.5 / GPT-6 Sol），Wonder Full 仅 Muse Code 订阅（至 $200/月）不开放 API；**Meta 正式弃守开源优先** |
| **10/15** | **Step 5 Preview 开源完整权重倒计时 2 天**（腾讯 WorkBuddy 限免同步进行至 **10/25**）——权重到手 = 免费不再依赖限时窗口 |

---

### 🕵️ **Zen 隐身免费模型 `cat-jam-free`：今晨空降，官方文档都还没挂**

**今晨（created 时间戳落在 10/13 凌晨）** Zen 的 `/v1/models` 接口多出 `cat-jam-free`，13:11 快照时**官方定价页与文档均未收录**——延续 Zen 隐身模型的玩梗命名（cat jam 梗图）。**已知**：全档 $0、在官方 API 目录可直接调用。**未知**：底层模型、参数规模、上下文长度、免费截止日——按 big-pickle / space-bunny 的先例（均在数日内揭晓身份），预计一两周内揭盅。**⚠️ 隐身期数据大概率用于训练，别放机密代码**；等定价页更新再确认真实身份与限额。

### 🏢 **Meta Muse Wonder：付费前沿，但必看**

Meta 10/12 发布 **Muse Wonder / Muse Wonder Full**，公司**首个前沿模型系列**，明确转向闭源收费。**规格**：1M 上下文 / 943K 最大输出，输入支持**文本 + 图像 + 视频 + 音频 + PDF**，强制推理（6 档 effort），主打「主动记忆」面向长程个人/专业智能体；设计 Arena 网页类 **Elo 1352、全球第 2**。**价格**：API **$4/$20 每百万**；Wonder Full **仅 Muse Code 订阅、不开放 API**；官方称将逐步下放 Muse 应用免费档。已上 OpenRouter（`meta/muse-wonder`，本期唯一进目录的新面孔）。**读法**：闭源大厂集体转向，「免费」供给只会越来越依赖开源社区与限免营销。

### 📊 **接口清点（13:11）与量大能用白嫖口**

- **OpenRouter**：目录 **459** / 零价 **19**（**连续 4 期零进出**）/ `:free` **15**。免费档「量大能用」排面不变：**Ling 3.1 Flash**（262K、免费档智能分最高 41.1）、**Thinking Machines inkling / inkling-small**（1M 上下文）、**Nemotron 3.5 Lightning / 3 Ultra 550B**（1M 上下文）。
- **OpenCode Zen**：接口 **84** / 免费 ID **10**（+cat-jam-free）；定价页 Free 行 **13**（含 big-pickle、exo-free 等接口侧已不含的旧条目），两头口径照旧有差，以实际调用为准。Step 5 Preview / Space Bunny / LongCat 2.5 Preview Free 均在位且 ZDR。
- **白嫖口**：**NVIDIA NIM**（GLM-5.3 1M/40RPM + GLM-5.3-Flash，freellm.net 周用量 2.2 亿 / **4 万亿** tokens，社区最大免费通道）；**Google AI Studio**（Gemini 3.5–3.8 Flash 免费 10 RPM/20 RPD，App 端砍档不影响）；**Groq**（Qwen3.8-27B 30 RPM/250 RPD）+ **Cloudflare**（1 万 neurons/日）。

### ⏰ **到期红线**

- **10/15** — **Step 5 Preview 开源完整权重**（同在 WorkBuddy 限免期内）
- **10/25** — **腾讯 WorkBuddy 独家限免结束**
- **本月内** — **Beam 权重 Apache 2.0 放出**（early-access 候补中）；**Mistral Large 4 权重约 10/27**
- **趋势** — 免费 API 池连续 4 期零进出；增量在**开源权重**与**隐身限免**

> **口径说明**：本页数字为脚本清点时刻快照（**2026-10-13 13:11 GMT+8**，与 10/12 午后快照逐条比对）。OpenRouter 零价池按 `prompt=='0' and completion=='0'` 统计，「零价但无 `:free` 后缀」的模型也已计入；Zen 以**官方定价页 Free 行为准**。第三方聚合榜与官方目录存在滞后与计数差，请勿单独据其做结论。「开源」指权重公开，不代表可自由商用。**cat-jam-free / Big Pickle / Space Bunny 等隐身或「数据可能用于训练 / 仅限试用」的通道：不要把机密代码、个人信息或生产客户数据放进去。**

---
