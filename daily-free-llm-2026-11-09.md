# 免费大模型日报 · 2026-11-09

> 快照 09:45 GMT+8 · 本期主线：Inkling 2 Small 发布即上 Zen 免费席；OR 免费池 18→16、Inception Mercury 全系退场；Gemini Omni 1.2 Flash 降价 30%。

## 今日头条

1. **Inkling 2 Small 发布即上 Zen 免费席** — Thinking Machines 11/6 发布第二代开放权重模型：594B/A17B MoE，AA 综合分 13→31、登顶美国开源第一（前三均为中国模型：K3.1 Pro 46 / DS V4.1 Flash 33 / GLM-5.3 32）。发布即隐身上架 Zen `inkling-2-small-free`（与 `iceman-free` 同日入席），官方承诺下周 Apache 2.0 开源权重。代价是「话多」：单任务平均输出约 15 万 token、成本 $1.18、耗时 21 分钟；预训练数据披露采样自 Kimi K3。

2. **OR 免费池 18→16，Inception Mercury 全系退场** — Mercury 2 / 2.5 / 3 三款扩散 LLM 从 OR 与 Nous 双池整体撤下（Mercury 3 上架不足三周）；Inkling 两枚 `:free` 同步撤下转 `:batch` 付费批量档；NVIDIA 内容安全小模型 `:free` 同日退场。唯一进账：`liquid/lfm-3-1.7b:free`（11/6 上架，1.7B/256K、工具调用，数据用于训练）。OR 总目录 455→461，:batch 批量档集中上新 8 款。

## 接口清点（vs 11-04）

- **OpenRouter**：461 / 零价 16 / `:free` 12。新上架：`ricursiveai/ripple-65b-preview`（Apache 2.0、$0.20/$0.60）、Ling-3.0-Tiny、`gemini-omni-1.1/1.2-flash`（视频生成、按分辨率分档计价）、auto-code。价格：`gpt-oss-120b` 输出 $0.09→$0.60（涨回 6.9×）；`glm-5.3` 输出 $3.60→$1.40；`deepseek-v4-pro` 半价 $0.95/$1.90；`v4.1-flash-1017` →$0.01/$0.50；`llama-3.3-70b` 涨 2 倍。
- **OpenCode Zen**：81 / 免费 ID 11（10→11）：+`inkling-2-small-free`、+`iceman-free`，−`pulse-alpha-free`（上架仅 4 天，11/6 弃用）。官方页 Free 区列 14 行（含接口未见的 jev-1.13-free / nemotron-3-ultra-free，页面滞后）——以接口为准。折扣：ML4 5 折、Argon 5 折至 11/30。
- **Nous Portal**：393 / `:free` 4（3→4）：新上 `meituan/longcat-2.5:free`（11/4 上架）；beam-1.0-501b-a23b、step-3.7-flash、solar-mini4 持平；Mercury×3 退场。
- **其他通道**：UnoRouter 11/7-08 连上 5 枚 `:free`（qwen-plus、qwen3-235b、qwen3.7-flash、solar-pro4、lfm3-1.7b）；NVIDIA Build 免费层 62 款（GLM-5.3-Flash、Step 5 Preview、K2.6 在列）；freellm.net 531+ / 31 家 / 240 实测（NIM GLM-5.3-Flash 90 居首）；EdgeOne Makers 新户送 50 万 tokens。
- **国内免费额度**：混元 Hy4 限免至 11/15（WorkBuddy/CodeBuddy 0 倍率每日额度，首日额度遭挤爆已十倍扩容）；Hy3 限免同步延至 11/15；阿里千问双 11 会场 11/5 开场；StepAudio 3 限免 11/8 如期收官；智谱 ZCode 每日 3 亿 GLM-5.3-Flash 照常；美团 LongCat 新户 1000 万。

## 时间线与前瞻

- **11/6**：Inkling 2 Small 发布；Zen pulse 弃用 + iceman-free 上架；LFM3-1.7B 上 OR 免费档。
- **11/5**：Gemini Omni 1.2 Flash 发布（15 秒、720p 降 30%，Arena 文/图生视频双榜首；Google Vids 每月免费 3 条）；百度「词元所」上线；Hy4 十倍扩容公告。
- **11/10**：Vercel Security Review 公测免费截止。
- **11/15**：混元 Hy3 / Hy4 限免截止；商汤小浣熊延至 12/1。
- **下周**：Inkling 2 Small 权重 Apache 2.0 开源（安全测试后）；12/3 起 Omni 1.1 请求自动转 1.2。
- **11/17**：Google Opal 停用。
- **11/30**：七牛云 conatus-free 截止；HeyGen Voice Turbo 免费截止；Zen Argon 5 折到期。
- **12/1**：Kiro Kiroween 积分申领截止；商汤小浣熊限免截止。

## 口径

脚本清点快照（11/09 09:45 GMT+8）。OR 零价池含无 `:free` 后缀的零价模型；Zen 免费 = `-free`/`:free` 后缀 + big-pickle；Nous 以官方接口为准。隐身模型（inkling-2-small / iceman / crouton / big-pickle）免费期为预览价，数据政策各异，勿放机密数据。
