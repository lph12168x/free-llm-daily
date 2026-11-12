# 免费大模型日报 · 2026-11-12

> 快照 13:10 GMT+8 · 本期主线：**ERNIE 5.5 Flash Preview 转挂 :free**（发布 2 天即补免费席）；**Mistral 免费档 API 核实关闭**；**Pareto 26.10 复合模型双池上架**；**DS V4.1-Flash 降价**。

## 今日头条

1. **ERNIE 5.5 Flash Preview 转挂 :free：发布仅 2 天即补免费档** — 昨日以 $0.28/$1.13 付费出海的百度 ERNIE 5.5 Flash Preview（280B/A14B、1M、200 tok/s），付费版已从 OR/Nous 撤下，换 `baidu/ernie-5.5-flash-preview:free` 上架——Qianfan 免费托管，实测 P50 吞吐 88 tok/s、延迟 2.4s，限速约 200 req/天。OR 零价池 **15 → 16、:free 12 → 13**。1M 长上下文直接进免费池，是目前免费档里规格最高的中国旗舰之一，注意 Qianfan 结构化输出错误率偏高（实测 ~20%）。

2. **Mistral 免费档 API 确认关闭：聚合站仍在误标「1B token/月」** — 官方文档核实（11/8 口径）：Mistral **Free mode 仅含 Le Chat / Vibe 月度额度，不含 API 访问**——创建 API key 与调用须先激活计费、走 pay-as-you-go。旧 Experiment 档（约 1B token/月）已成历史。freellm.net 等聚合站仍按旧档标注「免费 API」，再次印证**第三方站点普遍滞后，一切以官方接口/定价页为准**。

## 接口清点（vs 11-11）

- **OpenRouter**：469 → 467 / 零价 16 / `:free` 13（免费池回升 +1）。新上架：`baidu/ernie-5.5-flash-preview:free`、`unbiased/pareto-26.10-preview`（复合模型、1M、$0.8/$3.2，BYOK only）；付费退场 3 款：`seed-1.6` / `seed-1.6-flash` / `seed-2.0-code`（seed 系剩 2-1-turbo/2.0-lite/2.0-mini）。价格：`deepseek-v4.1-flash` 降至 **$0.022/$0.40**（输入 −57%/输出 −29%）；`v4.1-flash-1017` 输入 $0.006 → $0.15（限免价恢复，+2400%）；`qwen3.5-9b` 双降 67%；`glm-5.3-flash:batch` 输出 +195%；`granite-4.2-8b` 输出 −40%、`gemma-3-27b` 输出 −22%。
- **OpenCode Zen**：85 / 免费 ID 12 持平，零进出零价格变动（`-free` 11 枚 + big-pickle）。官方页 Free 区列 16 行（含接口已无的 jev-1.13-free 等，滞后），以接口为准。Carbon / Argon 5 折至 11/30、Flash 系 5 折至 12/31 照常。
- **Nous Portal**：398 → 395 / :free 3 持平。+`unbiased/pareto-26.10-preview`（与 OR 同步）、−seed 三款（与 OR 同源退场）。现 `:free`：longcat-2.5、step-3.7-flash、solar-mini4。
- **其他通道**：freellm.net **535+ / 31 家 / 244 实测**（11/11 更新，NIM GLM-5.3-Flash 90 分居首）。Pareto 26.10 为「复合路由」模型：每请求并发多个上游模型择优合成答案，**无单一上游、无公开 benchmark**，适合尝鲜不宜当基准。
- **国内免费额度**：混元 **Hy4 / Hy3 限免至 11/15**（剩 3 天）+ TokenHub 刊例 5 折至 12/31；智谱 ZCode 每日 3 亿 GLM-5.3-Flash 照常；美团 LongCat 实名领 1000 万 + Zen 免费席每日 100 次；腾讯混元新人体验包至 12/31。

## 时间线与前瞻

- **11/11–12**：ERNIE 5.5 Flash :free 上架（发布 2 天补免费席）；Mistral 免费档 API 关闭获官方文档口径确认。
- **本周**：Inkling 2 Small 权重 Apache 2.0 开源（兑现窗口）。
- **11/15**：混元 Hy3 / Hy4 限免截止。
- **11/17**：Google Opal 停用。
- **11/30**：七牛云 conatus-free 截止；HeyGen Voice Turbo 截止；Gemini 4 Carbon / Argon 推广价截止。
- **12/1**：Kiro 4000 积分截止；商汤小浣熊限免截止；Carbon 价格翻倍生效（$4/$20）。
- **12/3**：Gemini Omni 1.1 请求自动转 1.2。
- **12/31**：Zen Gemini 3.6/3.7/3.8 Flash 5 折截止（2027-01-01 起恢复原价）。

---
**口径**：脚本清点快照（11/12 13:10 GMT+8）。OR 零价池含无 `:free` 后缀的零价模型；Zen 免费 = `-free`/`:free` 后缀 + big-pickle；Nous 以官方接口为准。隐身/免费期模型（inkling-2-small / iceman / big-pickle）数据政策各异，勿放机密数据。
