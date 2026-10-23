## 📰 今日摘要（2026-10-23）

> 本期主线：**Recursive Flint 权重开源（Apache 2.0）**——40B/2.5B 激活 MoE 编码模型，由自动研究系统 Eureka Machine 主导研发、笔记本可跑，OR / Zen 双池免费上架；**MiniMax M3.1 Flash 免费档双池退场**，UnoRouter 补位万亿级 `mistral-large-4:free`。

| 数字 | 含义 |
| --- | --- |
| **40B 开源** | **Recursive Flint（10/21 发布）**：40B 总参 / **2.5B 激活** MoE、262K、**Apache 2.0** 可商用；Recursive（Richard Socher 创立、**田渊栋联合创始**）的自动研究系统 **Eureka Machine** 主导架构搜索 / 4-bit 输出层 / 恢复蒸馏 / 自定义内核，小团队**不到 4 个月**从零训完；自报 SWE-bench Pro v2 **89.7%**（仅次 Qwen3.8）、Verified 74.2%、TB2.1 54.9%，**50B 以下 SWE-bench Verified 第一**（⚠️ 自报待独立复测） |
| **笔记本可跑** | Flint **48GB 内存**即可：M4 Pro 实测 **131 tok/s**（约为 Gemma 4 / Nemotron 3.5 Lightning 的 2 倍）、RTX Spark 155 tok/s；免费入口 **OR `recursive/flint-v1.0:free`**（$0、262K、113 tok/s）+ **Zen `flint-40b-free`**（数据保留 30 天） |
| **顶流退场** | **M3.1 Flash 双池免费下架**：OR 免费档周用量顶流（**11.4T tokens/周**）与 Zen `minimax-m3.1-flash-free` 同日退场，正价 $0.15/$0.60；Zen 同时下架 `longcat-2.5-preview-free`；OR 免费用量第一让位 **Nemotron 3 Ultra**（4.63T/周） |
| **万亿免费** | **UnoRouter 10/22 新上 `mistral-large-4:free`**：1.05T/49B 旗舰直接免费（共享容量 + 按模型限速），:free 池达 **76 款**（GLM-5.3-Flash、Qwen3.8-Max、Kimi K3 等在列）；Nous Portal 免费档 **8 款**（10/21 +`solar-mini-4:free`） |
| **接口清点** | OR **468 / 零价 20 / `:free` 17**（+flint、−m3.1-flash）；Zen **85 / 免费 ID 9**（+flint-40b-free，−m3.1-flash-free、−longcat-2.5-preview-free），⚠️ 定价页 Free 行 **13** vs 接口 9，以接口为准；Zen 折扣：Mistral Large 4 **5 折 $0.68/$2.09**、Gemini 4 Argon 5 折（**11/30 截止**）；⏳ **10/27 Mistral Large 4 权重开源**倒计时 4 天 |

---

