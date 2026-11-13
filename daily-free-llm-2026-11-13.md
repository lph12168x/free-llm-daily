# 免费大模型日报 · 2026-11-13

> 快照 13:10 GMT+8 · 本期主线：**Gemini 4 Hydrogen 发布并三池同上**（Gemini 4 系首次进消费免费档）；**OR 免费池单日 +2**；**DS V4.1-Flash 限免价结束**；**K3.1 Pro 输入 −88%**。

## 今日头条

1. **Gemini 4 Hydrogen 发布：Gemini 4 系首次进消费免费档，三池同上** — 谷歌 11/12 发布 Gemini 4 系第三款模型 Hydrogen，主打快速执行与日常编码/Agent 工作流：**$1.5/$7.5 全 1M 统一价、batch 半价 $0.75/$3.75、1M 输入/输出、四档思考（low~xhigh）**。AA 智能指数 high 档 51、xhigh 54，超过 Argon 的 50；幻觉率仅 8%（Sonnet 5.5 为 43%）。免费用户经 Gemini App 自动模型选择即可用上。OR `google/gemini-4-hydrogen`（付费）+ `:batch`、Zen、Nous 三池同步上架；Antigravity 新增 Orchestrator（Carbon 规划 + Hydrogen 执行，配额 −24%、提速 19%）。云端 only、无开源权重。

2. **OR 免费池单日 +2：新供应商 Apodex + Particle 补免费席** — OR 目录 467→475（单日 +8 为近期最大扩容），零价 16→18、**:free 13→15**：`apodex/apodex-1.1-mini:free`——**新供应商 Apodex**，35B 开源（Apache 2.0）、262K、Novita 托管，长程 research/forecasting 推理向；`particle-ai/particle-1:free`——Particle AI 的 agentic coding 模型（DS V4.1 Flash 后训、1M、图文输入），付费版 $0.05/$0.50 同在。另有 Inkling 2 Small 付费版 $0.30/$1.00 上架 OR+Nous（权重开源进入兑现窗口）、Ling 3.0 Flash Fin/Sante 金融/医疗特化版双池上架（124B/A5.1B、262K、$0.042/$0.1232）。

## 接口清点（vs 11-12）

- **OpenRouter**：467 → 475 / 零价 18 / `:free` 15（单日 +8：hydrogen 付费+batch、inkling-2-small 付费、ling-fin/sante、kimi-k3.1-pro:batch、apodex :free、particle-1 :free）。价格地震：`deepseek-v4.1-flash` $0.022/$0.40 → **$0.30/$1.20**（输入 13.6×/输出 3×，限免价结束，`~flash-latest` 跟随涨至 $0.038/$0.50）；`kimi-k3.1-pro` 输入 $2 → **$0.2375**（−88%）、输出 $8.41（−16%）并新增 :batch $0.70/$6；`glm-5.3` 输出回升 $1.40→$3.60；`gemini-flash-latest` 恢复原价（2×）；`gemma-4-26b` 输出 +155%；`mimo-v2.5-pro` 输出 −52%；`glm-5.2:batch` 输入 −15%。
- **OpenCode Zen**：85 → 86（+gemini-4-hydrogen 付费）/ **免费席 12 持平**（beam / big-pickle / ds-v4.1-flash / glm-5.3-flash / iceman / inkling-2-small / longcat-2.5 / minimax-m3.1-flash / flint-40b / mimo-v2.6-flash / nemotron-3.5-lightning / nemotron-3.5-super-vl）。官方页 Free 区列 17 行仍滞后（含接口已无的 jev-1.13-free），以接口为准。折扣：Carbon/Argon 5 折至 11/30、Flash 系 5 折至 12/31、Mistral Large 4 5 折。
- **Nous Portal**：395 → 400 / :free 3 持平。+gemini-4-hydrogen(+batch)、+ling-3.0-flash-fin/sante、+inkling-2-small（与 OR 同步）、+llama-3.1-70b-instruct（经典回归）；−deepseek-v4.1-flash-1017:batch。现 `:free`：longcat-2.5、step-3.7-flash、solar-mini4。
- **其他通道**：freellm.net **536+ / 31 家 / 245 实测**（11/12 更新，NIM GLM-5.3-Flash 90 分居首，LLM7 DS-V4-Flash-0731 85、Gemini 3.8 Flash 84 次之）。免费榜前十里中国开源模型占 6 席。
- **国内免费额度**：混元 **Hy4 / Hy3 限免至 11/15 23:59**（剩 2 天，WorkBuddy/CodeBuddy 0 倍率）+ TokenHub 刊例 5 折至 12/31；**智谱 ZCode 新用户体验档改版**：5 天 × 每日 800 万（GLM-5.3 300 万 + GLM-5.3-Flash 500 万，取代旧 500 万档）；ZCode 蹬蹬卡邀新活动 **11/13 截止**；七牛云 conatus-free 每日 1 亿至 11/30；美团 LongCat 实名领 1000 万。

## 时间线与前瞻

- **11/12–13**：Gemini 4 Hydrogen 发布并三池同上；OR 免费池单日 +2（Apodex / Particle）；DS V4.1-Flash 限免价结束；K3.1 Pro 输入价 −88%。
- **11/13**：智谱 ZCode 蹬蹬卡邀新活动截止。
- **本周**：Inkling 2 Small 权重 Apache 2.0 开源（付费 API 版已先行上架）。
- **11/15**：混元 Hy3 / Hy4 限免截止（23:59，剩 2 天）。
- **11/17**：Google Opal 停用。
- **11/30**：七牛云 conatus-free 截止；HeyGen Voice Turbo 截止；Gemini 4 Carbon / Argon 推广价截止（12/1 翻倍 $4/$20）。
- **12/1**：Kiro 4000 积分截止；商汤小浣熊限免截止。
- **12/31**：Zen Gemini 3.6/3.7/3.8 Flash 5 折截止（2027-01-01 恢复原价）；腾讯云 TokenHub 5 折截止。

---
**口径**：脚本清点快照（11/13 13:10 GMT+8）。OR 零价池含无 `:free` 后缀的零价模型；Zen 免费 = `-free`/`:free` 后缀 + big-pickle；Nous 以官方接口为准。隐身/免费期模型（inkling-2-small / iceman / big-pickle）数据政策各异，勿放机密数据。
