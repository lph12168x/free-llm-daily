# 每日免费大模型日报 · 2026-10-15

> 自动生成 · 在线版：[daily-free-llm-2026-10-15.html](daily-free-llm-2026-10-15.html)
> 仓库：[lph12168x/free-llm-daily](https://github.com/lph12168x/free-llm-daily)

---

> 本期主线：**Step 5 Preview 权重今日如期开源**——免费自此不依赖限免窗口；但各渠道限免窗**明天集中关闭**。免费 API 池面继续沉寂：OR **连续 5 期零进出**，Zen 反向挤出 1 款。

| 数字 | 含义 |
| --- | --- |
| **权重落地** | **Step 5 Preview 开源 BF16 + FP8 双版本**，上线 Hugging Face / ModelScope，附技术博客（**92 层窄深架构、Sparse GQA**、百万级可验证环境 + 长程任务强化学习）与部署指南，vLLM / SGLang / Transformers 皆可；600B 总参 / 27B 激活、1M 上下文、原生视觉；OR Token 用量**周榜+日榜全球第二** |
| **明天 10/16** | **Cline / Nous / Kilo 的 Step 5 免费窗关闭**，恢复官方标价 **$1 / $2.7**（OrcaRouter 复核： Nous 窗口本就明示 10/8–10/15）——要薅限免只剩今天 |
| **11 → 10** | **Zen 挤出 `ling-3.1-flash-free`**：接口 86→85、免费 ID 11→10，**蚂蚁 Ling 系在 Zen 免费清零**（昨日刚在 OR 退出）；定价页 Free 行 12 vs 接口 10，滞后照旧 |
| **$0 补贴** | **Grok Bot 免费动态路由 Opus 5.5**（10/8 起）：Cursor 账号登录 PC 端即用，原价 $4/$20 的成本平台补贴，另免费直连 X 数据；业内判断属闪电战策略、清单随时收紧 |

---

### 🏆 **Step 5 Preview 权重今日开源：免费从「限免」变「自部署」**

阶跃星辰 10/15 正式开放权重，**BF16 与 FP8 两个版本**同步上线 Hugging Face 和 ModelScope。技术博客披露 92 层窄深架构、Sparse GQA、训练稳定性优化、**百万级可验证环境**与长程任务强化学习等细节。**部署**：vLLM / SGLang 起兼容 OpenAI 接口的 API 服务，Transformers 可离线推理，多芯片平台有适配。**用量**：OpenRouter 截至 10/15 的 Token 用量**周榜与日榜均为全球第二**——本来就在限免期被薅得飞起，权重落地后自由部署无截止日。

### 🆓 **Grok Bot 补贴白嫖 Opus 5.5：账记在马斯克头上**

10/8 起 Grok Bot PC 端升级**动态路由**：用 Cursor 账号登录即可使用，后台按任务自动调用 **Opus 5.5**（原价 $4/$20 每百万）、Midjourney、Suno 等顶级模型，成本平台承担；同时免 API 费直连 X 数据。团队确认 Bot 本身就直接跑在 Opus 5.5 上、已分批上线。⚠️ **第三方转述信源**，属前期闪电战补贴，后端清单大概率收紧，且走第三方路由**勿放机密数据**。

### 📊 **接口清点（13:10）**

- **OpenRouter**：目录 **462** / 零价 **17**（`：free` 后缀 **14**）——与 10/14 逐条一致，**连续第 5 期零进出**；免费档排面仍是 inkling / inkling-small（1M）、nemotron-3.5-lightning / 3-ultra（1M）、gemma-4-31b 等。
- **OpenCode Zen**：接口 **86→85** / 免费 ID **11→10**（出 `ling-3.1-flash-free`）；定价页 Free 行 **12** 与接口 **10** 两头口径差持续（exo / mimo-v2.5 / nemotron-ultra 页面在列、API 已无），**以接口为准**。
- **隐身免费**：Nous Portal `stealth/missingno` 仍 $0（约 262K 上下文、未公布截止）；Command Code `stealth/glyph-cluster:free`（256K、100 请求/日）仍全档免费并已扩散至 Vercel AI Gateway。
- **月度额度**：Anthropic 按 Max 5x / Max 20x / Team **每月送 $100 / $200 / $500 API 额度**；Vercel AI Gateway 月度免费额度；Hugging Face 免费档仅 $0.10/月路由额度（测试用）。

### ⏰ **到期红线**

- **10/16（明天）** — Cline / Nous / Kilo 的 **Step 5 免费窗关闭**，恢复 $1/$2.7
- **10 月中旬** — **Kimi K3.1** 传发布（野村消息，今日未至）；K4 规划 5–6 万亿参数
- **10/25** — **腾讯 WorkBuddy 独家限免结束**；本月内 Beam 权重 Apache 2.0、Mistral Large 4 权重约 10/27
- **趋势** — 免费重心继续从「送 API 额度」转向「**放开源权重**」：Step 5 今日落地即是样本

> **口径说明**：本页数字为脚本清点时刻快照（**2026-10-15 13:10 GMT+8**，与 10/14 快照逐条比对）。OpenRouter 零价池按 `prompt=='0' and completion=='0'` 统计，「零价但无 `:free` 后缀」的模型也已计入；Zen 以**接口免费 ID 数为准**（定价页 Free 行仅作参考）。第三方聚合榜与官方目录存在滞后与计数差，请勿单独据其做结论。「开源」指权重公开，不代表可自由商用。**glyph-cluster / missingno / Grok Bot 路由等隐身、补贴或「数据可能用于训练」的通道：不要把机密代码、个人信息或生产客户数据放进去。**

---
