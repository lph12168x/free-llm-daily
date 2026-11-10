# 免费大模型日报 · 2026-11-10

> 快照 13:10 GMT+8 · 本期主线：**Claude Fable 5.2 发布即三池同步上架**（$8/$40 降 20%、FrontierCode 49.1%）；**Meta Muse Ember** 追平 Haiku 5.5 成本仅 1/3；**Inkling-2-small :free 回归 OR**、Crouton Alpha 三处退场；**Zen 免费席 11→12**。

## 今日头条

1. **Claude Fable 5.2 发布即三池同步上架** — Anthropic 11/10 发布新旗舰 Fable 5.2 / Mythos 5.2（同一底层模型，Fable 面向全员）。FrontierCode 2.0 32.4%→49.1%，超 Opus 5.5（45.5%）与 GPT-6 Astra（42.8%）；输出提速 30%。定价 $8/$40 较上代降 20%，OR `:batch` 档 $4/$20 再半价，可选 fast mode $16/$80（提速 2.5×）。OR / Zen / Nous 三池当日同步上架，`~claude-fable-latest` 动态路由跟随降价。官方案例：千智能体 30 小时形式化费马大定理、8 天搓出操作系统原型。

2. **Meta Muse Ember：追平 Haiku 5.5，成本仅 1/3** — 11/9 发布 Meta 旗下最小最高效模型：$0.10/$0.50（缓存输入 $0.004）、1M 上下文 / 512K 输出、原生多模态（文本/图像/音频/视频/PDF）。AA 智能指数 36 追平 Claude Haiku 5.5 max，单任务成本 $0.14 仅为后者 1/3，定位 agent 高频重复作业。已上 OR `meta/muse-ember`、Zen `muse-ember-1.0`、Nous。同日上架还有 Nex-N2.6（基于 GLM-5.3-Flash 后训的 agentic 模型，321B、$0.12/$0.40）。

## 接口清点（vs 11-09）

- **OpenRouter**：465 / 零价 16 / `:free` 13（+4 / +1）。新上架：`anthropic/claude-fable-5.2`（$8/$40、1M）+ `:batch`（$4/$20）、`meta/muse-ember`、`nex-agi/nex-n2.6`、`qwen3.8-max-0902:batch`；**`inkling-2-small:free` 回归零价池**（昨日转 :batch、今日 :free，1M 上下文）。退场：`stealth/crouton-alpha`（11/3 上架存活 6 天，三处同步撤）、`minimax/minimax-m1`。价格：`glm-5.3-flash` 输入涨 4.5×、输出涨 6×（:batch 档反向半价）；`kimi-k3:batch` 涨 2.5×；`gemma-4-26b` 输出 $0.225→$0.10；`llama-3.3-70b` →$0.71/$0.71。
- **OpenCode Zen**：84 / 免费 ID 12（11→12）。付费 +`claude-fable-5-2`、+`muse-ember-1.0`；免费席 **+`longcat-2.5-free`**（每日限 100 次、零保留、托管于中国）与 **+`minimax-m3.1-flash-free`**（零保留），−`crouton-alpha-free`。官方页 Free 区 14 行仍含接口已无的 jev-1.13-free / nemotron-3-ultra-free（滞后），以接口为准。折扣：**Gemini 3.6/3.7/3.8 Flash 全线 5 折** $0.75/$3.75（12/31 截止、2027-01-01 起恢复原价）；Sonnet 5.5 缓存读取半价 $0.10；Argon 5 折至 11/30。
- **Nous Portal**：396 / `:free` 4 持平。与 OR 同步上架 fable-5.2、muse-ember、nex-n2.6、qwen3.8-max-0902:batch；crouton、minimax-m1 退场。`:free` 4 款不变：longcat-2.5、beam-1.0-501b-a23b、step-3.7-flash、solar-mini4。
- **其他通道**：freellm.net 531+ / 31 家 / 240 实测（11/9 更新，NIM GLM-5.3-Flash 90 居首）；gravity.fast 11/10 实测 OR `:free` 13、最大上下文为 Inkling 2 Small 1M，与本刊口径一致。⚠️ Vercel **Security Review 公测免费今日截止**，之后转按 Token 计费。
- **国内免费额度**：混元 **Hy4 / Hy3 限免至 11/15**（WorkBuddy/CodeBuddy 0 倍率每日额度）；智谱 ZCode 每日 3 亿 GLM-5.3-Flash 照常；美团 LongCat 新户实名领 1000 万，Zen 免费席另享每日 100 次。

## 时间线与前瞻

- **11/10**：Claude Fable 5.2 发布（三池同上）；Vercel SR 公测免费截止；Muse Ember 双池上架。
- **11/9**：Meta Muse Ember 发布；Crouton Alpha 三处同步退场（存活 6 天）。
- **本周**：Inkling 2 Small 权重 Apache 2.0 开源（官方「下周」承诺进入兑现窗口）。
- **11/15**：混元 Hy3 / Hy4 限免截止。
- **11/17**：Google Opal 停用。
- **11/30**：七牛 conatus-free 截止；HeyGen Voice Turbo 截止；Zen Argon 5 折到期。
- **12/1**：Kiro Kiroween 4000 积分申领截止；商汤小浣熊限免截止。
- **12/3**：Gemini Omni 1.1 请求自动转 1.2。
- **12/31**：Zen Gemini 3.6/3.7/3.8 Flash 5 折截止（2027-01-01 起恢复原价）。

## 口径

脚本清点快照（11/10 13:10 GMT+8）。OR 零价池含无 `:free` 后缀的零价模型；Zen 免费 = `-free`/`:free` 后缀 + big-pickle；Nous 以官方接口为准。隐身/免费期模型（inkling-2-small / iceman / big-pickle）免费期为预览价，数据政策各异，勿放机密数据。
