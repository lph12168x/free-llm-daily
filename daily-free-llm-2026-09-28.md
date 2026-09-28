# 免费大模型日报 · 2026-09-28（周一）

> 🤖 AI 每日免费情报 · 全网挖掘 · [在线版 HTML](daily-free-llm-2026-09-28.html)

**今日四个关键数字**

| 数字 | 含义 |
| --- | --- |
| **落锤** | 匿名隐身模型 **Space Bunny Alpha** 身份基本揭晓：**MiniMax 于 9/27 在 MiniMax Code 里静默上线 M3.1-Flash-Preview**——距 stealth 空降仅 4 天，**1M + 五档推理强度 + 无模型卡无定价** |
| **24 → 21** | OpenRouter 零价池**一次性掉 3 条、零补位**：`glm-5.2:free`、`nex-n2.5-mini:free`、`nex-n2.5-pro:free` 同时退场——**免费供给从「停止扩容」转入「开始收缩」** |
| **1.6T / 48B** | 美团 **LongCat 2.5-Preview** 上线：**1.6T 总参 / 约 48B 激活 / 1M 上下文 / 原生多模态**，OpenAI + Anthropic 双协议；**Zen 新增免费档 + 老用户发 500 万 tokens** |
| **10/7** | 智谱双节活动**官方盖章落地**：GLM-5.3-Flash 夜间畅用（23:00–09:00 免费）**从 9/20 延期到 10/7**，且 **9/25–10/7 取消高峰期、全天按五折计费** |

---

## 🔥 今日头条 · 三条主线

### ① 谜底落锤｜**Space Bunny Alpha 的身份基本揭晓**：MiniMax 9/27 静默上线 **M3.1-Flash-Preview**——**匿名跑数据 → 产品内发模型的经典套路**

**四天前我们还写「社区指纹指向 MiniMax M3.1，但官方未确认」。今天这条线索收口了——不过是以最 MiniMax 的方式收的口：不开发布会、不发模型卡、不给跑分、不给价格，直接把模型塞进自家产品。** 9 月 27 日，MiniMax 在 **MiniMax Code**（自家编码 agent 产品）里上线了 **M3.1-Flash-Preview**，开发者比官方公告早一整天就在产品模型选择器里发现了它。

| 项目 | 内容 |
| --- | --- |
| 🧩 时间线本身就是证据 | **9/23** — 匿名模型 `stealth/space-bunny-alpha` 空降 OpenRouter（$0/$0）+ Zen（`space-bunny-free`），**1M 上下文、原生多模态、可调推理强度**。**9/24–26** — 社区做分词器指纹：OpenCode 一项研究给出 **24/24 全匹配** MiniMax 已知模型族，另一套更大范围的测量集给出 **50/50 匹配**。**9/27** — MiniMax 在 MiniMax Code 上线 **M3.1-Flash-Preview**，**1M 上下文、五档推理强度（low / medium / high / xhigh / 新增 max）**。**9/28** — 官方 X 账号确认发布，措辞只有一句：「debuts today on MiniMax Code，built for everyday development, fast, reliable, and ready for real work」 |
| 🎁 顺手发的福利比模型本身更实用 | MiniMax Code 同步推出两项**限时福利（9/28–10/7，UTC+8）**：**① 每日签到领双倍免费积分**，新老用户均可参与；**② 所有用户的 Token Plan 额度立即全员重置**，官方称后续还会继续重置。**积分可用于 M3.1-Flash-Preview，也可用于 H3 与 H3 Max 生成视频**——**纯白送、免绑卡、当天就能用**。⚠️ 注意：这个额度走的是 **MiniMax Code 客户端**，不是开放 API；想直接调 API 的话，MiniMax 开放平台的 M3 / M2 免费试用已**延期到 11/7** |
| 📊 免费档在真金白银的榜上排第 5 | OpenRouter 近 7 天用量榜（截至 9/28）：**Space Bunny Alpha 以 9.87T tokens 排第 5**，它**前面四条全部是付费模型**（DeepSeek V4.1 Flash 18.63T、GLM 5.3 Flash 17.82T、DeepSeek V4 Flash 0731 11.47T、Hy4 preview 10.61T）。**也就是说：一条 $0 的匿名模型，把这周所有付费模型挤到了它后面，只剩四条在它之上。** 同榜另有 `Nemotron 3 Ultra (free)` 5.47T 第 7、`Ling 3.0 Flash Fin (free)` 1.21T 第 22、`Laguna S 2.1 (free)` 1.19T 第 23 |
| 🧭 该怎么理解这件事（以及别踩的坑） | **读法：这是一种新的产品发布策略，而不是一次营销事故。** 西方实验室通常先发模型卡与博客再放人用；**MiniMax 反着来——先匿名放上公开平台收真实世界数据，几天后再在产品里落地，模型卡与定价「以后再说」。** 它换到的是真实负载下的性能数据 + 零营销成本的曝光。**对免费用户的含义：** Space Bunny 这条 $0 通道**已经完成了它的使命**，**「限时免费一周」（9/23 起算，约 9/30 到期）大概率就是终点**。**⚠️ 三条纪律：** ① **不要等最后一天**——stealth 池历史上（ox-alpha 6 天、union-alpha 不到 2 天）经常提前关闭；② **它永远不会变成「长期免费档」**，请把评估结论沉淀下来，别把工作流建在它上面；③ **M3.1-Flash-Preview 目前没有公开 API 与定价**，任何声称「M3.1 API 免费」的说法现在都无从核实 |

**💡 这条为什么值得上头条**：因为它把 **「匿名 stealth → 指纹识别 → 产品内静默发布」这条链路第一次完整走完了**，而且全程只用了 **4 天**。三个月前这套玩法还不存在；现在我们能用它**提前摸到未发布模型**——9/24 那条日报写在 M3.1 正式露面之前，**这就是免费档的真正价值：它是前沿模型的免费试吃窗口。**

**✅ 今天可以做的两件事**：① **去领 MiniMax Code 那笔签到积分**（9/28–10/7 每天双倍，纯白送，可跑 M3.1-Flash / H3 / H3 Max 视频）。② **如果 Space Bunny 还在你的候选里，本周之内跑完它**：OpenRouter 用 `stealth/space-bunny-alpha`（**这条 ID 不带 `:free` 后缀**），Zen 用 `space-bunny-free`。

---

### ② 免费池收缩｜OpenRouter 零价池 **24 → 21**：**一口气掉 3 条、零补位**——**连续多期「零增减」结束了**

**这是本期最硬的一条事实，也是最近一个月里免费池第一次真正意义的缩小。** 脚本清点：目录从 **457 涨到 458 款（+1）**，但**零价池从 24 掉到 21（−3）**、**带 `:free` 后缀从 20 掉到 17（−3）**。**新增的那 1 条在付费侧，零价侧一条都没补。**

| 项目 | 内容 |
| --- | --- |
| 📤 掉的三条，恰好是三种不同的死法 | **① `z-ai/glm-5.2:free`（32,768 ctx）**——**长期在架的老面孔**。它从 9/17 起健康度就在波动（当时 uptime 81.8%），后来恢复到 98.86%，我们也一直把它记在「零价池体检」里。**今天整条消失，不是转付费、是直接下架。** 结合智谱近期把资源全压到 **GLM-4.7-Flash 永久免费档**与 **GLM-5.3-Flash 夜间畅用**上，这是一次**免费资源的内部腾挪**：从「给旧旗舰发免费券」转向「用新一代 Flash 做引流」。**② `nex-agi/nex-n2.5-mini:free` 与 ③ `nex-agi/nex-n2.5-pro:free`**——这两条是**连坐式退场**：9/24 我们写的是「付费 SKU 下架、`:free` 版本仍在架」，**当时把它读作「测试期结束、正式定价未定」；今天的答案是——两周试用期结束，整个 nex-n2.5 系列从 OpenRouter 完全消失**。**这是「新平台试用券」的标准寿命：约 2 周。** |
| 📥 新增的 5 条，全在付费侧 | **零价侧：0 条。** 付费侧新增 **`typesafe/jev-router`**（TypeSafe 把 Jev 包装成路由器）、**`fireworks/ember-1`**、**`perceptron/perceptron-mk1.5`**、**`mistralai/devstral-2512`** 与 **`mistralai/mistral-large-2512`**（**注意：Mistral 这两条是「下架后又回来」，但回来的只是付费版——免费版没跟着回来**）。**本期合计：进 5 条全付费、出 3 条全零价 + 1 条付费（claude-3-haiku）。** **「增量全给付费、存量开始减免费」——这是与过去一个月完全相反的结构。** |
| 🔬 口径必须分清：21 和 17 不是一回事 | 四个数字同时成立、且必须同时说：**① 目录总量 457 → 458（+1）**；**② 零价池（输入输出同时 $0）24 → 21（−3）**；**③ 带 `:free` 后缀 20 → 17（−3）**；**④ 「零价但不带后缀」仍是 4 条**：`stealth/space-bunny-alpha`、`google/lyria-3-pro-preview`、`google/lyria-3-clip-preview`（**后两条输出音频**）、`openrouter/free`（200K 自动路由池）。**本期掉的三条全部带 `:free` 后缀，所以 21 与 17 同步减 3、两者差值不变。** 这个细节很重要：**如果你的监控只盯「零价池总数」，你会看到 −3；但如果你盯「`:free` 后缀项」，你同样看到 −3——本期两个口径第一次完全同步，说明退场的是「正规免费券」而不是「伪装成免费的可转价款」。** |
| 🌐 聚合站又一次落后于官方目录 | 对同一批变动，第三方站点的反映速度差别很大：**freellm.net** 已跟到 **505+ 款 / 31 家平台 / 239 款实时验证 / 417+ 免绑卡**，其 OpenRouter 免费页显示 **21 款**——**与官方脚本口径一致，这次没有滞后**。但 **CostGoat 的 OpenRouter 免费页仍写「19 款」**，**并且把已在 9/24 掉出零价池的 `nex-agi/nex-n2.5-pro:free`、`-mini:free` 继续列在表里**——**滞后约 4 天，属典型。** **本页结论不变：聚合站用来「发现新东西」，官方目录用来「确认还在不在」，两者不可互换。** |

**🆓 零价池近六期流水**（脚本口径：输入与输出同时为 $0）：

| 日期 | 目录总量 | 零价池 | 其中 `:free` | 零价净增减 |
| --- | --- | --- | --- | --- |
| 9/21 | 446 | 24 | 21 | — |
| 9/22 | 445 | 24 | 21 | +0 / -0 |
| 9/23 | 454 | 24 | 21 | +0 / -0 |
| 9/24 | 457 | 24 | 20 | +1 / -1 |
| **9/28（今天）** | **458** | **21** | **17** | **+0 / -3** |

**前五期零价总量纹丝不动，本期一次性减 3，是最近一个月第一次实质收缩。** 同时目录总量六期涨了 **12 款**，而零价池**净减 3 款**——**平台把新增能力全部放进了收费侧。**

**1M 上下文且 $0 的条目（今天是 7 条，与上期持平）**：`stealth/space-bunny-alpha`（1,000,000）、`nvidia/nemotron-3.5-lightning:free`（1,000,000）、`nvidia/nemotron-3-ultra-550b-a55b:free`（1,000,000）、`thinkingmachines/inkling:free`（1,048,576）、`thinkingmachines/inkling-small:free`（1,048,576）、`google/lyria-3-pro-preview`（1,048,576，**音频输出**）、`google/lyria-3-clip-preview`（1,048,576，**音频输出**）。**前五条文本可用，后两条不是——统计 1M 免费时别把音频算进去。**

---

### ③ 国产新面孔｜美团 **LongCat 2.5-Preview** 上线：**1.6T / 48B / 1M / 原生多模态**——**Zen 免费档 + 老用户 500 万 tokens 双通道**

**今天免费池里最值得上手的新模型是这条，而不是那个已经要走的隐身模型。** 美团上线 **LongCat-2.5-Preview**，并做了一件国产厂商里不常见的事——**同时开放官方 API 和第三方免费池两条入口**。

| 项目 | 内容 |
| --- | --- |
| 🐱 规格：参数没变，能力面扩大了 | **延续 LongCat-2.0 的 1.6T 总参 / 约 48B 激活 / 1M token 上下文**（LongCat 2.0 曾在超 5 万张国产芯片上完成 35 万亿 token 预训练），**这一代的关键增量是「原生多模态」**。**最大输出 128K tokens**；官方定位从「代码与工具调用」推进到**终端、浏览器、桌面软件、电子表格、设计工具的长流程任务**——**也就是把 agent 从 CLI 里放出来，去操作真实软件界面**。**⭐ 最实用的一点：官方 API 同时兼容 OpenAI 与 Anthropic 接口**，并**直接给出 Codex、OpenCode、OpenClaw、CatPaw 四家的接入方法**——**现有 agent 工具改个 base_url 就能接。** |
| 🎁 两条免费通道（一条立刻可用） | **① OpenCode Zen：`longcat-2.5-preview-free`**——今天新加入 Zen 免费名单，定价页四列全 Free，**且条款明确写「零保留政策、不使用你的数据训练模型」**（与同页的 Big Pickle / MiMo / Ling 的「免费期数据可能用于改进模型」完全不同）。**这是 Zen 免费名单里数据条款第二干净的一条（仅次于 Space Bunny）。** **② 美团官方：所有老用户发放 500 万免费 tokens** 用于体验新模型，**原有 token 套餐不受影响、可继续使用**。官方平台注册新用户亦有体验额度。**建议：优先走 Zen 那条**——它没有「额度用完」的概念，且零保留条款对代码场景更友好。 |
| ⚠️ 一个必须说清楚的空白 | **官方目前没有公布 LongCat-2.5 的任何 benchmark。** GUI 操作能力、长流程任务完成率**相对 2.0 提升了多少，官方一句都没说，也没有第三方复现数据**。**参数没变、能力面扩大、却不给分数**——合理推测是「先把接口与分发卡住，性能验证后置」，**但作为使用者，你应该把它当成「待验证的新条目」，而不是「已知的强模型」**。**建议的验证方式：拿一个你手头真实的长流程任务（比如「读一个表格 → 改几处在另一张表里 → 输出摘要」）跑一遍，看它能不能不中断地走完。** 这比看任何跑分都直接。 |
| 🧭 为什么这条比 stealth 模型更值得投入 | 把它和头条①放在一起看，对比很鲜明：**Space Bunny Alpha** —— $0、1M、很强，但**匿名、无 SLA、窗口由负载决定、身份刚被揭晓、随时转付费**。**LongCat 2.5-Preview** —— 同样 $0、同样 1M、同样原生多模态，但**具名厂商（美团）、有官方 API 兜底、有明确定价体系（免费期结束后会转付费而非消失）、给出四家 agent 的接入文档、且 Zen 侧是零保留条款**。**结论：同一天的免费档里，优先选「有名有姓、有付费路径」的那条——因为它的免费期结束只是变成付费，而不是断供。** |

---

## 🌤️ 次要更新 · 值得记一笔

### 🇨🇳 上海 AI Lab 开源 Intern-Decision 三款：typed-decision 类别首次支持图像输入

**9 月 26 日，上海人工智能实验室在 40 秒内连建三个 Hugging Face 仓库，随后三小时内把权重全部推完**：**Intern-Decision-0.85B（07:57 UTC）、2.21B（08:14）、4.54B（09:03）**——全部 **Apache-2.0**，基于 **Qwen3.5 基座微调**。

它们属于 **Jev 在 9/15 开创、Laya 在 9/18 跟进的「typed-decision」类别**——**不生成文本，而是接收一个状态 + 一份具名问题 schema + 每题允许的答案集合，返回这些答案上的概率分布**。**Intern-Decision 的三条是这个类别里第一批支持图像输入的开放权重**，用「masked-next-token 决策目标」实现：**一次前向传播就回答 schema 里的所有问题，不做采样、直接校准出 typed JSON**。

**发布包比同类别任何一位都完整**：训练代码 + 两个推理后端 + 打分框架 + **温度拟合脚本**。卡片自评：**4B checkpoint 在七个 suite 上平均 90.02，对 Jev 的 88.74 有过之**，Brier 分数与预期校准误差都更低。**⚠️ 这份排名完全未经独立验证**：数字是实验室自己的，七个 suite 里**五个是公开数据集、且由同一组人挑选**。**当方向看可以，当结论用不行。**

**💡 真正被忽略的发现不在排行榜上**：三个 checkpoint 各自带一个拟合好的校准温度，**且随模型变大单调下降——0.85B 是 2.748、2.21B 是 2.101、4.54B 是 1.992**。温度大于 1 意味着把模型的概率分布「压平」，**压得越多说明原始输出越过度自信**——**所以在这个族里，小模型是更过度自信的那个。** **这是本次发布里最有复用价值的结论，而官方表述里一个字都没提。**

**对免费用户的意义**：这不是给你聊天用的模型，而是**把「分类 / 路由 / 打分 / 门禁」从「让聊天模型拼 JSON」里拆出来**的那一类——**成本能低两三个数量级、延迟低一个数量级，而且能自己跑（Apache-2.0）**。结合 TypeSafe 今天在 OpenRouter 上新的 `typesafe/jev-router`，**这个类别正在从「一家独有」变成「有开源可选项」。**

### 🆕 NaiveAI 开源 Naive-N0.5-Flash：MIT、309B MoE、自带 2122 tok/s 运行时

**MIT 许可的开权重模型，309B 总参 / 仅激活 15.5B 的 MoE，面向编码与 AI 研发任务**，**原生 1M token 上下文**。

**最有意思的不是模型而是配套运行时**：NaiveAI 同时发布了自研推理运行时 **NaiveRT**（自称由 AI 写成），宣称**单机可达 2000 tok/s，八卡峰值 2,122 tok/s**。**⚠️ 这类「自研运行时跑出的吞吐数字」必须与模型能力分开看**——它衡量的是工程优化水平，不是模型聪明程度，且均为厂商自报。**API 定价 $0.10 / $0.40（缓存命中 $0.01）**，处于当前中低价位；**权重 / GitHub / 主页均已公开**。**值得记一笔的原因：又一个「MIT + 大 MoE + 1M」的开放权重选项，而且带完整的推理栈。**

### 🎁 智谱双节活动官方落地：夜免延至 10/7、取消高峰期、FlashX 两周试用

**此前几天只是自媒体传闻，现在智谱开放平台文档正式上线，确认三件事**：

- **① 夜间畅用延期**：在 **ZCode / AutoClaw** 里调用 **GLM-5.3-Flash**，**每晚 23:00 到次日 09:00 额度消耗为 0（即可畅用）**——原定 9 月 20 日结束，**现延期到 10 月 7 日**。
- **② 取消高峰期**：**9 月 25 日至 10 月 7 日，全天按 50% 积分计费**。平时只有周一至周五 14:00–18:00 算高峰、其余时间半价；**双节期间全天都按半价算**。
- **③ 新上 GLM-5.3-FlashX 滚动开放两周试用**：**最快 200 tokens/s**，但**消耗是普通 Flash 的 2.5 倍**——**适合卡脖子的硬任务，不适合当默认档。**

**⚠️ 三条边界必须看清**：**① 免费只限 ZCode / AutoClaw 里的 Flash**，其他支持的 Agent 只是额度翻倍、不是全免；**② 触到 5 小时 / 周限额仍需等重置**；**③** 对夜猫子开发者来说，**免费窗口等于多送了约 17 天**。

**与它对照的长期兜底仍是那条**：z.ai 的 `GLM-4.7-Flash` / `GLM-4.5-Flash` / `GLM-4.6V-Flash` 输入输出全 Free、无到期日，国内直连——**这是目前少数能写进长期依赖的免费档。**

### 🧰 免费聚合网关集体更新：FreeLLMAPI 扩到 34 家 / 635 端点，另有三个新玩家

- **① FreeLLMAPI（开源，MIT）规模又跳了一档**：从早前的 14 家扩到 **34 家服务商 / 635 个免费模型端点**，聚合免费额度**约 7.4 亿 tokens / 月**，GitHub **28.4k stars**（此前记录是 6k）。能力也补齐了：**6 种路由策略（按实时速度与可靠性打分）、429/5xx 自动 failover（最多重试 20 次）、按「平台+模型+key」追踪 RPM/RPD/TPM/TPD、粘性会话锁定 30 分钟、AES-256-GCM 密钥静态加密、内置 MCP server、React 可视化仪表盘**。**一条命令 Docker 起本地网关，对外只暴露一个 OpenAI 兼容端点。**
- **② Merge Gateway**：**Pro 档每月 $10 免费 LLM credits**（每月 1 号发放、月底过期、需绑卡），一个端点路由所有主流模型。
- **③ ModelBridge**（aibridge-api.com）：**500K tokens/月 + 500K 新客奖励**，**免绑卡**，港节点，专注中国模型（DeepSeek / Qwen / GLM / Kimi）。
- **④ Free.ai**：**注册后 30,000 tokens/日**（匿名仅 6,000），每日重置，**OpenAI 兼容 API（`api.free.ai`）**，账号内 400+ 工具共用同一额度池。

**⚠️ 使用这类聚合网关的三条纪律**：**① 上游不透明、无 SLA，只用于试验与个人项目**；**② 额度会互相牵连**（Free.ai 的 30K/日与站内工具共享）；**③ 别把带 key 的请求发给来路不明的网关**——优先选自托管（FreeLLMAPI）或定位清晰的官方网关。

### 📈 榜单：三条免费档进 OpenRouter 周榜前 23，其中一条直达第 5

**OpenRouter 近 7 天用量榜（截至 9/28）**：**DeepSeek V4.1 Flash 18.63T 第 1**、**GLM 5.3 Flash 17.82T 第 2**、DeepSeek V4 Flash 0731 11.47T 第 3、Hy4 preview 10.61T 第 4、**⭐ Space Bunny Alpha 9.87T 第 5（$0 免费）**、GPT-5.6 Luna 8.64T 第 6、**⭐ Nemotron 3 Ultra (free) 5.47T 第 7**、MiMo-V2.6-Flash 4.28T 第 8、MiMo-V2.5 3.5T 第 9、GLM 5.3 2.89T 第 10、Hy3 2.79T 第 11、GPT-6 Luna 2.28T 第 12、Gemini 3.8 Flash 2.19T 第 13。

**第 15–23 名里另有两条免费档**：**Muse Spark 1.3 Contributor 1.76T 第 15**（以折扣价换 Meta 训练权）、**Ling 3.0 Flash Fin (free) 1.21T 第 22**、**Laguna S 2.1 (free) 1.19T 第 23**。**读法：前 23 名里有 4 条是 $0 或准 $0，其中一条（Space Bunny）进了前五。这解释了为什么平台要收缩免费池——免费模型确实在分流付费模型的用量，而今天那次「一次性减 3」很可能不是巧合。**

**freellm.net 核验榜（9/27 更新）**：**505+ 款 / 31 家平台 / 239 款实时验证 / 417+ 免绑卡**；榜首仍是 **NVIDIA NIM `z-ai/glm-5.3`（96 分，1.3M、40 RPM）**，次席 **`z-ai/glm-5.3-flash`（96 分）**；**OpenRouter 的 `Ling 3.0 Flash Sante (free)` 以 95 分冲到第 3（周吞吐 313.8B）**，`Qwen3.8 27B (free)` 93 分第 4、Ollama Cloud `deepseek-v4-pro` 92 分第 5。**⚠️ 注意：该站榜首分数从 97 微降到 96，属评分口径波动，不必过度解读。**

---

## 🧾 今日免费入口速查 · 先进 + 量大优先

| 入口 | 免费额度 | 模型量级 | 状态 / 注意 |
| --- | --- | --- | --- |
| **LongCat 2.5-Preview** · OpenCode Zen（今日新增） | **四列全 Free**（限时） | 1.6T / 激活 48B，**1M + 原生多模态** | **零保留、不用于训练**；美团具名厂商，免费期结束会转付费而非断供；**官方另有 500 万 tokens 送给老用户** |
| **MiniMax Code** · 9/28–10/7 | **每日签到双倍积分** + Token Plan 全员重置 | M3.1-Flash-Preview，**1M / 五档推理强度** | **纯白送、免绑卡**；积分可跑 M3.1-Flash 与 **H3 / H3 Max 视频**；**仅限客户端，非 API** |
| **Space Bunny Alpha** · OpenRouter / Zen | $0 / $0，**约 9/30 到期、剩 2 天** | **1M** / 文本+图+视频 | 已确认为 MiniMax M3.1 系；**周榜 9.87T 第 5（前五唯一免费）**；ID 不带 `:free`；**本周内跑完评估** |
| **OpenRouter** `nemotron-3-ultra-550b-a55b:free` | $0 / $0（200 请求/日） | 550B / 激活 55B，**1M** | Nvidia 端点；**周榜 5.47T 第 7，前十唯一免费**；**勿提交个人 / 机密数据** |
| **Dots3-Note Preview** · **9/30 到期，剩 2 天** | $0 / $0（至 2026-09-30） | 280B / 激活 16B，512K / 图文 | 支持 tools / structured_outputs；**只剩两天，今天就得跑** |
| **智谱 z.ai** · 永久免费档 + 双节活动 | **输入输出全 Free** + 夜免至 10/7 | `GLM-4.7-Flash` 等，国内直连 | **唯一可以写进长期依赖的一类**；9/25–10/7 全天五折 |
| **NVIDIA NIM** · 长期兜底 | 40 RPM，**不限调用量** | 含 `glm-5.3` 1.3M 与 Kimi K3 1M | freellm.net 榜首来源（96 分）；**需手机验证** |

**📌 长期兜底组合（无到期日那一类）**

- **智谱 z.ai** — `GLM-4.7-Flash` / `GLM-4.5-Flash` / `GLM-4.6V-Flash` **输入输出全 Free，无到期日**（国内直连）。
- **书生 InternLM** — **1.8 亿 tokens/月、免信用卡、无明确到期日**。
- **美团 LongCat** — **每天 5,000 万 token**（官方平台）。
- **Cerebras** — **每天 100 万 token**；**Cloudflare Workers AI** — **每天 1 万 neurons**。
- **OVHcloud AI Endpoints** — **匿名免注册 9 款**，2 RPM。
- **FreeLLMAPI（自托管，MIT）** — **34 家 / 635 端点 / 约 7.4 亿 tokens·月**，一条命令起本地网关。
- **Pollinations** — **免 key 即用**，适合临时脚本。

**组合建议**：**主力**用一条稳的（NIM / 智谱永久免费档），**兜底**用无到期日的（LongCat / InternLM），**试用**用限时券与 stealth（LongCat 2.5 / Space Bunny / Dots3），**临时**用免 key 的（Pollinations）。**四类分开管理，别混在一条配置里。**

---

## 🔎 平台盘点 · 今日快照

### 📊 OpenRouter：**458 款中 21 款零价**（`:free` 17 款）

- 脚本清点时刻：**458 款（较 9/24 +1）**，其中**输入与输出同时为 $0 的共 21 款**（较 9/24 **−3**），**带 `:free` 后缀 17 款**（**−3**）。
- **零价池退出三条**：`z-ai/glm-5.2:free`（**32,768 ctx，长期在架，直接下架非转付费**）、`nex-agi/nex-n2.5-mini:free`、`nex-agi/nex-n2.5-pro:free`（**该系列连付费 SKU 一起整体退场，试用期约 2 周**）。
- **零价池新进 0 条。** 付费侧新增五条：`typesafe/jev-router`、`fireworks/ember-1`、`perceptron/perceptron-mk1.5`、`mistralai/devstral-2512`、`mistralai/mistral-large-2512`（**后两条是下架后回归，但只回付费版**）。
- **四条「零价但不带 `:free`」**：`stealth/space-bunny-alpha`（**1M 三模态**）、`google/lyria-3-pro-preview`、`google/lyria-3-clip-preview`（**后两条输出音频**）、`openrouter/free`（200K **自动路由池**）。**写代码漏写 `/free` 会按付费价扣款；这四条则相反，随时可能直接转付费价。**
- 另下架 `anthropic/claude-3-haiku`。**1M 且 $0 的条目 7 条，与上期持平。**

### 🔧 OpenCode Zen：**80 → 82 款**（+`longcat-2.5-preview-free`、+`qwen3.8-max`），免费 ID **11 个**

- `/zen/v1/models` 返回 **82 款**（较 9/24 的 80 款 +2，**零下架**）。新增两条：**`longcat-2.5-preview-free`**（**免费**）与 **`qwen3.8-max`**（**付费，$2/$6**）。
- 带免费标记的 ID 仍 **11 个**：`big-pickle`、`space-bunny-free`、`jev-1.13-free`、`deepseek-v4-flash-free`、`mimo-v2.6-flash-free`、`mimo-v2.5-free`、`ling-3.0-flash-fin-free`、`nemotron-3-ultra-free`、`nemotron-3.5-lightning-free`、`muse-spark-1.3-contributor-free`、`muse-spark-1.2-contributor-free`。
- 官方**定价页 Free 行 10 款**（Big Pickle、Space Bunny、**LongCat 2.5 Preview**、MiMo-V2.6-Flash、MiMo-V2.5、Ling 3.0 Flash Fin、Nemotron 3 Ultra、Nemotron 3.5 Lightning、Muse Spark 1.3 Contributor、Jev 1.13 Free）。**接口名单比定价页多 `deepseek-v4-flash-free` 与 `muse-spark-1.2-contributor-free`，按惯例以定价页为准。**
- 📖 **数据条款三类必须分清**：**Space Bunny / LongCat 2.5 = 零保留、不用于训练**（最干净）；**Big Pickle / MiMo / Ling = 免费期数据可能用于改进模型**；**Nemotron 两条 = NVIDIA 试用端点，勿提交个人或机密数据**。**控制台的「启用计费」按钮不要点。**
- ⏰ 旧版下线提醒：**小米 `mimo-v2.5-pro` / `mimo-v2.5` 将于 10/21 10:00 下线**，`mimo-v2.5-free` 受此影响——**尽快切 `mimo-v2.6-flash-free`**。

### 🌐 freellm.net：**505+ 款 / 31 家平台 / 239 款实时验证 / 417+ 免绑卡**

- 核验时间 2026-09-27（较上期：502+ → **505+**、416+ → **417+**）。榜首 **NVIDIA NIM `z-ai/glm-5.3`（96 分）**、次席 **`z-ai/glm-5.3-flash`（96 分）**。
- **OpenRouter 的 `Ling 3.0 Flash Sante (free)` 以 95 分冲到第 3（周吞吐 313.8B）**，`Qwen3.8 27B (free)` 93 分第 4、Ollama Cloud `deepseek-v4-pro` 92 分第 5、NIM `Kimi K3` 91 分第 6。
- **✅ 本期它跟上了官方目录**：其 OpenRouter 免费页已显示 **21 款**，与我们的脚本口径一致，**未出现上期的滞后**。**但同类的 CostGoat 仍写 19 款，并把已退出的 `nex-n2.5-pro:free` / `-mini:free` 继续列出，滞后约 4 天。**
- **用法建议**：把它当「**发现新模型与新平台**」的入口（收录广度确实是全网最好的之一），**但任何关于「是否还在免费」的判断，一律回官方定价页或官方 API 复核**——本页累计记录的多处滞后实例里，这是第一次它「跟上了」，值得记一笔。

---

## 📅 到期日历 · 别踩空

**眼前这一周**

- **9/28（今天）** — **MiniMax Code 双倍签到 + Token Plan 重置开始（至 10/7）**：**今天就能领**。
- **约 9/30（剩 2 天）** — **Space Bunny Alpha 的「限时免费一周」窗口**（按 9/23 起算）；**stealth 池历史上常提前关闭，不要等最后一天**。
- **9/30（剩 2 天）** — **Dots3-Note Preview 免费档到期**；**阿里 Qoder × Qwen3.8-Flash 免费用结束**；**腾讯 Hy3 / 文心 4.0 全系列免费期结束**；**上海电信 AI Store 2500 万额度领取截止**；**杭州千问办公 Token 卡现场领截止**；Merge Gateway GLM-5.3-Flash 1 折结束。
- **10/7** — **智谱 GLM-5.3-Flash 夜间畅用 + 全天五折结束**；**MiniMax Code 双倍签到结束**。

**10 月及以后**

- **10/10** — **DeepSeek 低谷价窗口结束**；**腾讯混元 Hy4 preview**（老用户夜间免费）结束；unbiased.ai Pareto 正式发布（即 union-alpha 的真身）。
- **10/14** — 珠海算力券申报截止（企业向）。
- **10/15** — **阶跃 Step 5 Preview 释放完整 BF16 权重**（许可证待公布）。
- **10/17** — 豆包全用户 30 天订阅（9/24 那轮）截止。
- **10/21（10:00）** — **小米 `mimo-v2.5-pro` / `mimo-v2.5` 正式下线**，Zen 的 `mimo-v2.5-free` 受影响。
- **11/7** — MiniMax 开放平台 M3 / M2 免费试用到期。
- **12/31** — 腾讯云 TokenHub / 华为云码道 / 移动云 MoMA 年度额度截止；微信小程序成长计划二期报名截止。

---

## 🧭 今天该怎么动

### ① 现在就做（5 分钟内）

**今天有两件事必须今天做，因为它们都有明确的时间窗。**

**第一件：去领 MiniMax Code 那笔签到积分。** 9/28–10/7 每天双倍，**纯白送、免绑卡**，积分可跑 **M3.1-Flash-Preview**，也能拿去跑 **H3 / H3 Max 生成视频**——**这是本期性价比最高的一条，不领就浪费了**。

**第二件：把 Space Bunny 和 Dots3 这两个「剩 2 天」的额度今天跑掉。** 两条都按 **9/30 到期**（Space Bunny 按 9/23 起算的一周窗口，Dots3 官方明确标 9/30）。**别看还有两天就拖——stealth 类历史上（ox-alpha 6 天、union-alpha 不到 2 天）经常提前关闭，等最后一天的风险完全不成比例。**

**顺手做一件防呆的事：检查你所有配置里写死的免费模型名。** 今天这次收缩给了一个很干净的教材——`z-ai/glm-5.2:free` 是**长期在架的老面孔**，`nex-n2.5-*:free` 也才上架两周，**三条在同一天一起消失**。**如果你的生产链路里有任何一条写死的 $0 通道，今天就是加备线的好日子：主力挂 NIM 或智谱永久免费档，备线挂 LongCat 2.5。**

### ② 今天之内

**把「免费档会消失」这件事从意外变成预期。** 今天这 3 条退场，恰好覆盖了三种典型死法：**① 老旗舰的免费券被厂商主动收回**（glm-5.2，资源转向新一代 Flash）；**② 新平台的试用期自然到期**（nex-n2.5，约 2 周）；**③ 匿名 stealth 窗口关闭**（Space Bunny，疑似身份揭晓后收摊）。**三种死法的时间尺度完全不同，但共同点是——没有一条会提前很久通知你。**

**建议今天做一张「免费档到期表」**：把你实际在用的每一条免费通道写下来，标上「来源类型」（永久 / 限时券 / 试用 / stealth / 捐赠换数据），**然后按类型设不同的复看频率**——永久档每月看一次，限时券每周看一次，stealth 每天看一次。**这张表的成本是十分钟，收益是永远不会在某天早上发现生产线断了。**

**如果你的任务对延迟不敏感**，今天也适合把 **LongCat 2.5-Preview** 接进来做一次真实评测：**挑一个你手头的长流程任务（读表 → 改数据 → 出摘要），跑一遍看能不能不中断走完**。它官方没给任何 benchmark，**所以你的实测结果本身就是当下唯一可信的数据。**

### ③ 本周之内

① **为「免费池收缩」做些预案。** 本期是最近一个月里零价池第一次实质缩小（24 → 21），同时目录还在涨（+1）——**也就是说平台没有停止接入新模型，只是不再把新模型免费给你**。**这是个趋势信号，不是单日波动。** 如果你的免费策略建立在「反正总有免费档」之上，**本周值得把「付费兜底」这一层认真算一遍成本**——现在中低价位已经很便宜（DeepSeek V4.1 Flash 谷时、GPT-6 Luna $0.10/$0.50、GLM-5.3-Flash $0.15/$0.50），**从 $0 到「几乎不要钱」的那一档，价格差其实很小。**

② **把 typed-decision 这类模型纳入评估。** 上海 AI Lab 开源 Intern-Decision 三款（Apache-2.0、可自部署）+ TypeSafe 在 OpenRouter 上新的 `jev-router`，**意味着「分类 / 路由 / 打分 / 门禁」这类任务第一次有了「便宜、快、有开源替代」的完整选项**。如果你现在的 agent 里有任何一步是「让大模型输出一个 JSON 决策」，**把它拆出来单独评测，很可能省下两三个数量级的成本。**

③ **盯四个日期**：**9/30**（Space Bunny + Dots3 + 一批国产免费期集中到期，本周最密集的一天）、**10/7**（智谱夜免与 MiniMax 签到双双结束）、**10/15**（阶跃 Step 5 权重开源，许可证是变量）、**10/21**（小米 MiMo-V2.5 全线下线）。

④ **留意 M3.1 与 LongCat 2.5 的正式版**：前者今天只在自家产品里、无 API 无定价；后者有 API 但无 benchmark。**两个都值得先把评估框架准备好，等正式信息落地时立刻能出结论。**

---

## 📚 数据来源

- **OpenRouter** `/api/v1/models`（9/28 脚本清点，458 款中 21 款 $0、其中 17 款带 `:free` 后缀；已留 `or_models_0928.json`、`zen_0928.json` 供次日 diff；较 9/24 的 457 / 24 / 20 三项变动：总量 +1、零价 −3、`:free` −3）
- **零价池退场三条**（`z-ai/glm-5.2:free` 32,768 ctx 直接下架；`nex-agi/nex-n2.5-mini:free` 与 `-pro:free` 连同付费 SKU 整体退场）与付费侧新增五条（`typesafe/jev-router`、`fireworks/ember-1`、`perceptron/perceptron-mk1.5`、`mistralai/devstral-2512`、`mistralai/mistral-large-2512`）；另下架 `anthropic/claude-3-haiku`
- **Space Bunny Alpha**（`stealth/space-bunny-alpha`；1,000,000 ctx / 524,288 最大输出 / 文本·图像·视频输入 / 工具调用 / 可调 reasoning effort；9/23 上线；OpenRouter 侧「可保留但不用于训练」、Zen 侧「零保留、不用于训练」；周吞吐 9.87T 排第 5）
- **MiniMax M3.1-Flash-Preview**（9/27 上线 MiniMax Code；1M ctx；五档推理强度 low / medium / high / xhigh / max；**无模型卡、无 benchmark、无公开定价、API endpoint 受限**；MiniMax Code 9/28–10/7 每日签到双倍积分 + 全员 Token Plan 额度重置，积分可用于 M3.1-Flash-Preview 与 H3 / H3 Max 视频；Annual Plus / Max / Ultra 为 $220 / $550 / $1,320，约 1.7B / 5.1B / 12.5B M3 tokens 每月，余额不结转）
- **身份指纹交叉验证**（OpenCode 一项研究 24/24 匹配 MiniMax 已知模型族，另一套更广测量集 50/50；MiniMax Code 仓库提前出现 `MiniMax-M3.1` 且测试代码含 1M 上下文与 low/high/max 三档；Adam Holter 等公开表态为 M3.1；**MiniMax 未正面确认身份映射**）—— StartupFortune / The Neuron / Web Pulse / BlockBeats
- **LongCat-2.5-Preview**（1.6T 总参 / 约 48B 激活 / 1M token ctx / 最大输出 128K / 原生多模态 / 兼容 OpenAI 与 Anthropic 接口 / 官方给出 Codex、OpenCode、OpenClaw、CatPaw 接入方法 / 老用户 500 万免费 tokens / **未公布 benchmark**）—— 美团 LongCat 官方 / BlockBeats / 鉅亨網
- **Intern-Decision 三款**（上海 AI Lab，Apache-2.0，0.85B / 2.21B / 4.54B，基于 Qwen3.5 微调，9/26 07:57–09:03 UTC 三个 Hugging Face 仓库陆续发布；typed-decision 类别首批支持图像输入；masked-next-token 决策目标、一次前向传播回答 schema 全部问题；自评七 suite 平均 4B 为 90.02 vs Jev 88.74，**未经独立验证、七项里五项为公开数据集且由同组挑选**；**校准温度随规模单调下降：0.85B 2.748 / 2.21B 2.101 / 4.54B 1.992**）
- **Naive-N0.5-Flash**（NaiveAI，MIT，309B MoE / 激活 15.5B，原生 1M ctx，自研运行时 NaiveRT 宣称单机 2000 tok/s、八卡峰值 2,122 tok/s，API $0.10 / $0.40、缓存 $0.01；权重 / GitHub / 主页公开）
- **智谱双节活动**（ZCode / AutoClaw 内 GLM-5.3-Flash 每晚 23:00–09:00 额度消耗为 0，由 9/20 **延期至 10/7**；9/25–10/7 取消高峰期、全天按 50% 积分计费；GLM-5.3-FlashX 滚动开放两周试用、最快 200 tokens/s、消耗为普通 Flash 的 2.5 倍；免费仅限 ZCode / AutoClaw 内的 Flash，其他 Agent 仅额度翻倍，仍受 5 小时 / 周限额约束）—— 智谱开放平台文档 / GLM Coding Plan FAQ
- **免费聚合网关**（**FreeLLMAPI**：MIT 自托管，34 家服务商 / 635 个免费模型端点 / 约 7.4 亿 tokens·月 / GitHub 28.4k stars，6 种路由策略、429 与 5xx 自动 failover（最多 20 次）、按平台+模型+key 追踪 RPM/RPD/TPM/TPD、30 分钟粘性会话、AES-256-GCM 密钥静态加密、内置 MCP server；**Merge Gateway** Pro 档每月 $10 免费 credits（每月 1 号发、月底过期、需绑卡）；**ModelBridge** 500K tokens·月 + 500K 新客奖励、免绑卡、港节点、专注中国模型；**Free.ai** 注册后 30,000 tokens·日（匿名 6,000）、每日重置、OpenAI 兼容 API）
- **OpenCode Zen** `/zen/v1/models`（82 款、免费 ID 11 个）与官方定价页（Free 行 10 款；新增 `longcat-2.5-preview-free` 与付费 `qwen3.8-max` $2/$6；LongCat 2.5 Preview 与 Space Bunny 均标注零保留、不用于训练）
- **freellm.net 核验榜**（2026-09-27：505+ 款 / 31 家平台 / 239 款实时验证 / 417+ 免绑卡；榜首 NIM `z-ai/glm-5.3` 96 与 `z-ai/glm-5.3-flash` 96；`Ling 3.0 Flash Sante (free)` 95 第 3、`Qwen3.8 27B (free)` 93 第 4、Ollama Cloud `deepseek-v4-pro` 92 第 5、NIM `Kimi K3` 91 第 6；**本期其 OpenRouter 免费页已显示 21 款，与官方口径一致**）
- **OpenRouter 用量榜**（近 7 天，截至 9/28）：DeepSeek V4.1 Flash 18.63T / GLM 5.3 Flash 17.82T / DeepSeek V4 Flash 0731 11.47T / Hy4 preview 10.61T / **Space Bunny Alpha 9.87T（Free）** / GPT-5.6 Luna 8.64T / **Nemotron 3 Ultra (free) 5.47T** / MiMo-V2.6-Flash 4.28T / MiMo-V2.5 3.5T / GLM 5.3 2.89T / Hy3 2.79T / GPT-6 Luna 2.28T / Gemini 3.8 Flash 2.19T / DeepSeek V4 Pro 0813 1.78T / **Muse Spark 1.3 Contributor 1.76T** / Solar Pro 4 1.68T / GPT-5.6 Sol 1.66T / GLM 5.2 1.62T / Claude Sonnet 5 (batch) 1.45T / MiniMax M3 1.37T / Kimi K3 1.36T / **Ling 3.0 Flash Fin (free) 1.21T** / **Laguna S 2.1 (free) 1.19T**
- **CostGoat OpenRouter 免费页**（滞后实证：仍写 19 款并列出已退出的 `nex-n2.5-pro:free` / `-mini:free`，滞后约 4 天）
- **国内临期清单**（9/30 集中到期：Dots3-Note Preview 免费档、阿里 Qoder × Qwen3.8-Flash、腾讯 Hy3 与文心 4.0 全系列、上海电信 AI Store 2500 万额度领取、杭州千问办公 Token 卡现场领、Merge Gateway GLM-5.3-Flash 1 折；10/7：智谱夜免与 MiniMax Code 双倍签到；10/10：DeepSeek 低谷价与腾讯 Hy4 preview；10/17：豆包 30 天订阅；10/21：小米 MiMo-V2.5 系列下线；11/7：MiniMax 开放平台 M3 / M2 免费试用）
- **智谱 z.ai 开放平台永久免费档**（`GLM-4.7-Flash` / `GLM-4.5-Flash` / `GLM-4.6V-Flash` 输入、缓存输入、输出均为 Free）
- **Nous Portal 免费档**（约 7 款，含 `upstage/solar-pro4:free`、`stepfun/step-3.7-flash:free`；注册赠 $1；**注意需绑卡后才会展示完整模型列表**）
- **CommandCode**（Go $1/月、GOAT $10/月；**额度为共享池、按所选模型不同、含 4.4% + $0.30 处理费**，官方文档口径：约 33% 的 read-tool 流量与 30% 的 shell 流量属可去除浪费）

---

## ⚠️ 免责声明

⚠️ 免费额度可能随时调整，请以各平台官网最新政策为准。本页所有「免费」判定均以官方接口或官方定价页为准；涉及额度的具体数字请自行调用官方 Usage API 或查看控制台确认。OpenRouter 免费池日内会波动，458 款 / 21 款零价 / 17 款 `:free` 是脚本清点时刻的快照，不代表全天稳定值。

**`stealth/space-bunny-alpha`（Zen 侧 `space-bunny-free`）为匿名第三方供应商运营，OpenRouter 与 OpenCode 仅负责路由，不承担其开发者/所有者/运营者角色；其「限时免费一周」是当前公告而非承诺，stealth 类模型历史窗口常因负载提前关闭，请勿作为长期依赖。其与 MiniMax M3.1 的对应关系基于社区分词器指纹与发布时间线推断，MiniMax 未正面确认该映射。**

**`longcat-2.5-preview-free`（美团 LongCat 2.5-Preview）官方未公布任何 benchmark，本页不对其能力做强弱结论；「零保留」为其在 OpenCode Zen 侧的条款表述，走官方 API 时请另行核对服务条款。**

**MiniMax M3.1-Flash-Preview 目前无公开 API 与定价，其免费额度仅在 MiniMax Code 客户端内有效（9/28–10/7）；任何声称可直接调用 M3.1 API 或宣称其 API 免费的说法，均无法通过官方渠道核实。**

**第三方聚合榜（freellm.net / CostGoat / AIHubMix / llmpricing.dev 等）与官方目录存在滞后与计数差，本页已记录多处实证（下架模型仍标 Online、已停用模型仍标 New、免费范围变更未反映），请勿单独据其做采购或宣传结论。**

「开源」指权重公开，不代表可自由商用，商用前请逐条核对许可证（尤其 Kimi、GLM、Qwen、MiniMax、Step、MiMo 系列的 Model-as-a-Service 与许可条款）。**Contributor / 试用 / 训练条款类免费档：不要把机密代码、个人信息或生产客户数据放进去。** 本页提到的 Aggregate Gateway（FreeLLMAPI / Merge / ModelBridge / Free.ai 等）上游不透明、无 SLA，仅建议用于试验与个人项目，请勿把长期密钥或生产数据接入来路不明的网关。

📅 生成时间：2026-09-28 · 本页由自动化任务每日生成
