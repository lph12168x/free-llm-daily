# 每日免费大模型日报 · 2026-10-12

> 自动生成 · 在线版：[daily-free-llm-2026-10-12.html](daily-free-llm-2026-10-12.html)
> 仓库：[lph12168x/free-llm-daily](https://github.com/lph12168x/free-llm-daily)

---

> 本期主线是**「免费供给重心换轨」**：接口侧两池同时缩表（OpenRouter 零价连续 3 期零进出、Zen 目录 −5），增量全在**开源权重**侧——Reflection AI **Beam**（501B/23B）发布、Aleph Alpha **Kolibri-1**（78.1B，Apache 2.0）放权重、HAL-X **THX-01**（322M）API 免密钥。

| 数字 | 含义 |
| --- | --- |
| **5010 亿参数** | **Reflection AI 发布 Beam 开放权重模型**：501B 总参 / **23B 激活**稀疏 MoE、**1M 上下文**、52 层；预训练 23.8T tokens、6,144 张 GB300 四周训完。官方称代码/推理**媲美 GLM-5.2（744B/40B）**、Agent 逼近 **Qwen3.8-Max**，**推理算力省 3–4 倍**；Terminal-Bench v2.1 得 **80.1**（落后 DeepSeek V4.1 Flash 90.6、Kimi K3 88.3）。**本月内 Apache 2.0 放权重**，现开 early-access 候补；英伟达已投 8 亿美元（传或进一步增持） |
| **458 / 19 · 82 / 9** | OpenRouter 目录 **458 款**、零价 **19 款**（连续 3 期**零进出**；含无 `:free` 后缀的 `inclusionai/ling-3.1-flash`）、`:free` 15 款；**OpenCode Zen 接口 82 款 / 免费 ID 9 个**（10/10 为 87 / 12，**−5**），**官方定价页 Free 行 13 条为准** |
| **Zen 本周下线** | `exo-free`、`nemotron-3-ultra-free`、`ling-3.0-flash-fin-free`、`deepseek-v4-flash-vision-exp`、`claude-sonnet-4` 五款退出接口目录 |
| **新免费供给 2 条** | **Aleph Alpha `Kolibri-1`**：78.1B 总参 / **3.46B 激活**、德英双语、262K，**Apache 2.0 权重已上 HuggingFace**；⚠️ 主线 llama.cpp / Ollama 尚**不能加载**（需社区补丁），Q4 约 47.5GB；发布方已与 Cohere 签合并协议。**HAL-X `THX-01`**：322M 非自回归**决策模型**（非聊天），**API 免注册免密钥**、约 **10ms**、工单分类准确率 **98.4%**，Apache 2.0 |
| **长期兜底仍在** | **NIM ~1 万请求/日居首**、**Groq 1,000/日**、**Cloudflare 1 万 neurons/日**、**豆包 200 万 tokens/日**、**智谱 GLM-Flash 永久免费**、**OVHcloud 匿名 2 RPM**（8 款免费模型、GDPR 合规） |
| **趋势判断** | 免费供给正从「**送 API 额度**」转向「**放开源权重**」——免费 API 会缩表，权重不会。当下「先进 + 免费」的确定解法是：短期靠 Zen 限时通道冲，长期靠自托管兜底 |

---

### 🏆 **Reflection AI 发布 `Beam`：501B 开放权重，正面对标 GLM-5.2 / 逼近 Qwen3.8-Max**

**今日最大**：布鲁克林初创 **Reflection AI**（前 DeepMind 研究员 Misha Laskin / Ioannis Antonoglou 创立）发布首款开放权重模型 **Beam**。**规格**：**501B 总参 / 23B 激活**稀疏 MoE、**1M 上下文**、52 层、交错局部 + 全局注意力、细粒度路由专家；预训练 **23.8T tokens**，用 **6,144 张 GB300 四周**训完；RL 阶段跑 **1 亿+ rollouts**、约 13 亿 sandbox。**对标**：官方称代码 / 推理**媲美 GLM-5.2（744B/40B）**、Agent 任务**逼近 Qwen3.8-Max**，且**推理算力只要对手 1/3–1/4**；**Terminal-Bench v2.1 得 80.1**，落后 DeepSeek V4.1 Flash（90.6）与 Kimi K3（88.3）——**不是最强，但单位算力效率最高**。**怎么拿到**：**本月内以 Apache 2.0 放出权重 + 技术报告 + 模型卡**，现开 early-access 候补名单，走 HuggingFace 与主流云 / neocloud 分发。**为什么重要**：北美首个正面迎战国产开放权重的旗舰级模型，面向**受监管行业与「AI 工厂」本地部署**——对不能把代码送出境的团队是个新选项。**🖇 背景**：英伟达已投 8 亿美元，FT 报道称其正探讨追加投资或收购。

### 🦜 **Aleph Alpha `Kolibri-1`：欧洲主权牌，78.1B Apache 2.0 已放权重**

**10/3 德国统一日发布**：**78.1B 总参 / 仅 3.46B 激活**，德英双语、**262K 上下文**，权重**已在 HuggingFace 以 Apache 2.0 放出**（可商用），附 189 页技术报告。跑分超 **Nemotron 3 Super** 与 **GPT-OSS 120B**；德国 + 芬兰基建「无外国控制」，主打公共部门 / 工业 / 航空航天。**⚠️ 两个坑**：① 主线 **llama.cpp / Ollama / LM Studio 还加载不了**（需社区补丁，CUDA 未验证），Q4_K_M 约 **47.5GB**；② 发布方 Aleph Alpha 已于 9/16 与 **Cohere 签合并协议**（合并后双总部多伦多 / 柏林），**「主权」的长期维护方未定**。**结论**：已有 64GB+ 显存 / 内存再尝鲜；德语业务可关注，代码任务性价比不如 Qwen3.6-35B-A3B。

### ⚡ **HAL-X `THX-01`：322M 决策模型，API 完全免密钥**

**非自回归**小模型，**322M 参数**、Apache 2.0、权重 + 训练脚本全开；**托管 API 无需注册、无需 API Key**。**不是聊天模型**——做**垃圾邮件判定 / 工单路由 / 发票字段抽取 / 有序打分 / 逐字摘录**，输出带校准概率的结构化答案。**跑分**：2,843 条多语言工单准确率 **98.4%**（Jev 1.13 为 97.4%），延迟 **~10ms vs 331ms**（官方称不同部署，非受控对比），支持 18 种后训练语言，`pip install thx01` 即可，也能跑在手机上。**适合**：要在流水线里塞一个**分类 / 抽取判别器**、又不想为一次分类付大模型钱的团队。

### 🔄 **平台清点：两池同时缩表，OpenRouter 零价连续 3 期零进出**

**OpenRouter**（09:18 快照）：目录 **458 款**（与 10/10 完全一致），零价口径 **19 款**、带 `:free` 后缀 **15 款**，**本期无一进一出**。池内元老：**Nemotron 3 Ultra 550B**（1M）、**Nemotron 3 Super 120B**、**Nemotron 3.5 Lightning**、**Thinking Machines Inkling / Inkling Small**（1M，多模态）、**Gemma 4 31B / 26B**、**Ling 3.1 Flash**（零价但**无 `:free` 后缀**，易漏计）、**Lyria 3 两款**；新面孔：**Poolside Laguna S 2.1 / XS 2.1**、**Cohere North Mini Code**（256K）、**Apodex 1.1 Mini**、**Dots3-Note Preview**（512K）、**LFM2.5-2.6B**。**⚠️ 新入池多为代码 / Agent 小模型（30B–120B），1M 长上下文只剩 NVIDIA 与 Thinking Machines 两家**。**OpenCode Zen**：接口目录 **82 款**（10/10 为 87，**−5**），免费 ID **9 个**，官方定价页 **Free 行 13 条**（含 `big-pickle` 隐身模型）——**以定价页为准**。免费主力：**Step 5 Preview Free**（约一周窗口、ZDR）、**Space Bunny Free**（隐身、ZDR）、**LongCat 2.5 Preview Free**（ZDR）、**Muse Spark 1.3 Contributor Free**（Meta，**换你数据训模型**）、**Jev 1.13 Free**、**MiMo-V2.6-Flash Free**、**Nemotron 3.5 Lightning Free**、**Ling 3.1 Flash Free**、**Big Pickle**。**🔐 条款分层**：ZDR 可用（Space Bunny / LongCat / Step 5 Preview）；**数据可能用于训练**（Big Pickle / Exo / MiMo / Ling / Muse Spark Contributor）；**Nemotron 仅限试用**。

### 🎟️ **「量大能用」免费额度大盘（10/12 复核）**

**国际侧**：🥇 **NVIDIA NIM**——开发者计划成员免费原型访问，手机验证后约 **40 req/min**，**单日量级仍居首**；🥈 **Groq**——免费档 **30 req/min、1,000 req/日、8K tokens/min**（gpt-oss-120b、Qwen3.8 27B）；🥉 **Cloudflare Workers AI**——**10,000 neurons/日**（是额度不是次数）；**OVHcloud AI Endpoints**——**匿名档无需注册**即可发请求（2 RPM），**8 款免费模型**（Qwen3.8-27B、Qwen3.5-397B-A17B、Mistral-Small-3.2、Llama-3.3-70B 等），**GDPR 合规、欧盟机房**。**应用侧**：**ChatGPT 免费档已上 GPT-6 Luna**（10/8 起，含 Intelligent UI 交互式回答）；**Gemini 应用免费档**仍是 Flash-Lite 级。**国内侧（手机号注册即得）**：**智谱 GLM-Flash 永久免费**（另送 2000 万 token）、**火山引擎（豆包）200 万 tokens/日**、**硅基流动 2000 万 token**、**DeepSeek 300 万 token**。**⚠️ 避坑**：聚合网关（one-api 等）渠道类型要选 **type 16**（type 1 会 404）；硅基流动 base_url **不要带 `/v1`**。

### 🧭 **今天怎么选 · 三条路**

**A · 要「最强」不要钱** → Zen 免费池的 **Step 5 Preview Free**（约一周、ZDR）或 **Space Bunny Free**；OpenRouter 侧用 **Nemotron 3 Ultra 550B**（1M）。**窗口短，当冲刺用，别写进架构**。 **B · 要「天天有量」** → 主力挂 **NIM（~1 万/日）**，备用 **Groq（1k/日）** 与 **Cloudflare（1 万 neurons/日）**；国内用 **豆包 200 万 tokens/日** 或 **智谱永久免费档**。**多供应商 fallback 是唯一稳态策略**。 **C · 要「不怕断供」** → **自托管是本期唯一的确定性增量**：Beam（本月 Apache 2.0）、Kolibri-1（已放权重）、THX-01（322M，可跑手机）。**免费 API 会缩表，权重不会**。

### ⏰ **到期 / 波动提醒**

- **本周内** — **Step 5 Preview**（10/8 起约一周）、**Zen 各 Free 通道**均为「limited time」制，随时可能转付费
- **本月内** — **Beam 权重 Apache 2.0 放出**（early-access 候补中）；**Kolibri-1** 已可下载
- **趋势** — 两端接口池**同时缩表**；免费供给重心正从「送 API 额度」转向「放开源权重」

> **口径说明**：本页数字为脚本清点时刻快照（2026-10-12 09:18 GMT+8）。OpenRouter 零价池按 `prompt=='0' and completion=='0'` 统计，「零价但无 `:free` 后缀」的模型也已计入；Zen 以**官方定价页 Free 行为准**。第三方聚合榜与官方目录存在滞后与计数差，请勿单独据其做采购结论。「开源」指权重公开，不代表可自由商用。**Big Pickle / Exo / MiMo / Ling / Muse Spark Contributor / Nemotron Free 等「数据可能用于训练或仅限试用」的通道：不要把机密代码、个人信息或生产客户数据放进去。**

---
