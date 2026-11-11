# 免费大模型日报 · 2026-11-11

> 快照 13:10 GMT+8 · 本期主线：**Gemini 4 Carbon 全量开放**（$2/$10 推广价至 11/30、12/1 翻倍，OR/Zen/Nous 三池同上）；**百度 ERNIE 5.5 Flash Preview 出海**（OR+Nous 双池）；**OR 免费池 11/09 后首度缩减**（xing4.0:free 退场）；**GLM-5.3-Flash 价格暴涨全回吐**。

## 今日头条

1. **Gemini 4 Carbon 全量开放：三池同上，推广价仅剩 20 天** — Google 11/10 将最强推理模型 Carbon 正式面向所有付费开发者开放（此前两周仅 Fairwind 网安计划内测）。**$2/$10 推广价至 11/30**，12/1 起翻倍至 $4/$20；`:batch` 档 $1/$5、缓存输入 95% 折扣、1M 上下文、thinking_level 三档可调。官方称 CursorBench 4.0 / WANDR / AutomationBench 三榜第一，单任务成本不足次优外部模型一半；Antigravity 同步预览 `/swarm` 多智能体协作。OR `google/gemini-4-carbon`、Zen（5 折同价）、Nous（含 :batch）三池当日同步上架。免费档暂不可用，但 12/1 前是尝鲜最低价窗口。

2. **百度 ERNIE 5.5 Flash Preview：OR + Nous 双池上架** — 百度 11/10 发布 ERNIE 5.5 Flash Preview：**280B 总参 / 14B 激活**、1M 上下文、生成 >200 tok/s，定价 **$0.28/$1.13**（Qianfan 缓存命中实测输入仅 $0.077）。同场 `ernie-light-dt-1.0-intl` 基于开源 GLM 加自研 BSA 稀疏注意力（1M、$1.13/$3.94）。Base 权重已开源：**年收入 ≤$5000 万商用免许可费**，但 EU/UK/韩国除外且禁用于训练他家模型。两枚模型 OR / Nous 双池当日上架，1M 长文本赛道再添低价选手。

## 接口清点（vs 11-10）

- **OpenRouter**：465 → 469 / 零价 15 / `:free` 12（+6 / −2，免费池 11/09 后首度缩减）。新上架：`google/gemini-4-carbon`（$2/$10、1M）+ `:batch`（$1/$5）、`baidu/ernie-5.5-flash-preview`、`baidu/ernie-light-dt-1.0-intl`、`kt/midm-k-3.0-pro`（韩国 KT，120B/A12B Mamba-MoE、262K、$0.20/$0.80）、`motif-technologies/motif-3`（314B/A13.2B、262K、$0.30/$1.20，英韩双语）。退场：`xingchen-agi/xing4.0-29b-a4b:free`（10/19 上架存活 3 周+）、`qwen/qwen-2.5-7b-instruct`。价格：`glm-5.3-flash` 回落至 **$0.0399/$0.0784**（昨日 4.5×/6× 暴涨几乎全回吐）；`kimi-latest` 输出 $9.34→$11.0（+18%）。
- **OpenCode Zen**：84 → 85 / 免费 ID 12 持平。付费 +`gemini-4-carbon`（5 折 $2/$10，官方注明 11/30 截止）；免费席零进出：`-free` 后缀 11 枚 + big-pickle。官方页 Free 区仍列 14 行（含接口已无的 jev-1.13-free / nemotron-3-ultra-free，滞后），以接口为准。Gemini 3.6/3.7/3.8 Flash 5 折与 Argon 5 折照常。
- **Nous Portal**：396 → 398 / :free 4 → 3。上架 ernie-5.5-flash-preview、ernie-light-dt-1.0-intl、gemini-4-carbon + :batch；退场 `reflection/beam-1.0-501b-a23b:free`（免费券到期，Beam Free 仍在 Zen）与 qwen-2.5-7b。现 `:free` 3 款：longcat-2.5、step-3.7-flash、solar-mini4。
- **其他通道**：freellm.net **532+ / 31 家 / 241 实测**（11/10 更新，NIM GLM-5.3-Flash 90 分居首）。OR 新供应商面孔：韩国电信 KT 与 Motif Technologies 首次进驻。Vercel Security Review 公测免费已如期于 11/10 截止。
- **国内免费额度**：混元 **Hy4 / Hy3 限免至 11/15**（WorkBuddy/CodeBuddy 每日额度）+ TokenHub 刊例 5 折至 12/31；智谱 ZCode 每日 3 亿 GLM-5.3-Flash 照常；美团 LongCat 实名领 1000 万 + Zen 免费席每日 100 次。

## 时间线与前瞻

- **11/10**：Gemini 4 Carbon GA（三池同上）；百度 ERNIE 5.5 Flash 发布并出海；Vercel SR 免费公测截止。
- **本周**：Inkling 2 Small 权重 Apache 2.0 开源（官方「下周」承诺已进入兑现窗口）。
- **11/15**：混元 Hy3 / Hy4 限免截止。
- **11/17**：Google Opal 停用。
- **11/30**：七牛 conatus-free 截止；HeyGen Voice Turbo 截止；**Gemini 4 Carbon / Argon 推广价截止**。
- **12/1**：Kiro 4000 积分截止；商汤小浣熊限免截止；Carbon 价格翻倍生效（$4/$20）。
- **12/3**：Gemini Omni 1.1 请求自动转 1.2。
- **12/31**：Zen Gemini 3.6/3.7/3.8 Flash 5 折截止（2027-01-01 起恢复原价）。

## 口径

脚本清点快照（11/11 13:10 GMT+8）。OR 零价池含无 `:free` 后缀的零价模型；Zen 免费 = `-free`/`:free` 后缀 + big-pickle；Nous 以官方接口为准。隐身/免费期模型（inkling-2-small / iceman / big-pickle）免费期为预览价，数据政策各异，勿放机密数据。
