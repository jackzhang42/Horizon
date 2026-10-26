---
layout: default
title: "Horizon Summary: 2026-10-26 (ZH)"
date: 2026-10-26
lang: zh
---

> 从 52 条内容中筛选出 11 条重要资讯。

---

1. [llama.cpp Pocket-TTS 越界写入漏洞 CVE 公开，b11796 已修复](#item-1) ⭐️ 8.0/10
2. [IBM CEO 称开源权重模型已足够好用且便宜，可落地本地部署](#item-2) ⭐️ 7.0/10
3. [F-Zero X 3DS 移植复盘：约 5000 美元 LLM 成本](#item-3) ⭐️ 7.0/10
4. [上下文工程超越长度限制：记忆架构与策略性遗忘](#item-4) ⭐️ 7.0/10
5. [OpenAI 与 Anthropic 最高降价 80%，LLM 价格战为何升级？](#item-5) ⭐️ 7.0/10
6. [《经济学人》：中国 AI 进步日益依赖蒸馏美国模型](#item-6) ⭐️ 7.0/10
7. [OpenLDK 将 Java JIT 与运行时引入 Common Lisp](#item-7) ⭐️ 7.0/10
8. [在 2 美元的 ESP32 级微控制器上用 SIMD 加速运行计算机视觉](#item-8) ⭐️ 7.0/10
9. [斯坦福与 UC Berkeley 的 TokenGate 将长上下文预填充提速至多 11.3 倍](#item-9) ⭐️ 7.0/10
10. [三元 1.58-bit Nemotron 30B-A3B MoE 发布 GGUF，可在 12 GB 显卡上运行](#item-10) ⭐️ 7.0/10
11. [RTX 3080 20GB 解锁 ReBAR 与 P2P，张量并行预填充最高提速 115%](#item-11) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [llama.cpp Pocket-TTS 越界写入漏洞 CVE 公开，b11796 已修复](https://www.reddit.com/r/LocalLLaMA/comments/1xfizft/psa_llamacpp_cve2026116096/) ⭐️ 8.0/10

公开的 CVE-2026-116096 指出，llama.cpp 中 tools/mtmd/models/pockettts-gen.cpp 的 list_pockettts_state_slots 函数存在越界写入问题，攻击者可通过恶意 mmproj 参数在 Pocket-TTS 路径上触发该漏洞。该问题已在版本 b11796 中通过补丁 0a1ef309cdbb9f2024f58a38fb4c42352c5db569 修复；在当前 master 和最新版本 b11871 上，恶意 mmproj 会触发发布版本中生效的 GGML_ASSERT 并中止，而不再造成静默的堆写入。 llama.cpp 是使用最广泛的本机 LLM 运行时之一，因此带有公开利用代码的内存安全公告会影响所有加载不受信任模型或 mmproj 文件的用户。运行多模态或 TTS 工具的用户应尽快升级，因为该问题仅需加载精心构造的投影器文件即可触发，而不需要远程交互。 利用该漏洞需要本地访问权限，但利用代码已公开并可能被用于攻击；升级到 b11796 或更高版本可解决所报告的具体问题。提交者建议的按构造修复方案 PR #29360（“prevent OOB accesses from malformed mmproj files”）仍未合并，因此当前根因只是被检测并中止，而非在设计上被阻止。

reddit · r/LocalLLaMA · /u/Bulky-Priority6824 · 10月26日 00:53

**背景**: llama.cpp 是一个用 C/C++ 编写的推理引擎，用于在本机运行大语言模型，并通过与主模型一起加载的 mmproj（多模态投影器）文件来支持多模态模型。Pocket-TTS 是一个紧凑的文本转语音模型，已集成到 llama.cpp 的 TTS/多模态工具中。GGML_ASSERT 是底层 ggml 张量库中的断言宏，当内部不变量被破坏时会中止执行，因此恶意输入现在会导致崩溃，而不是静默的越界写入。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://cvefeed.io/vuln/detail/CVE-2026-116096">CVE-2026-116096 - ggml-org llama.cpp Pocket-TTS pockettts-gen ...</a></li>
<li><a href="https://github.com/ggml-org/llama.cpp/blob/master/docs/multimodal.md">llama.cpp/docs/multimodal.md at master · ggml-org/llama.cpp</a></li>
<li><a href="https://github.com/kyutai-labs/pocket-tts">GitHub - kyutai-labs/pocket-tts: A TTS that fits in your CPU ...</a></li>

</ul>
</details>

**标签**: `#llama.cpp`, `#security`, `#CVE`, `#memory-safety`, `#local-llm`

---

<a id="item-2"></a>
## [IBM CEO 称开源权重模型已足够好用且便宜，可落地本地部署](https://www.theregister.com/systems/2026/10/22/ibm-ceo-says-open-weight-models-are-now-irresistibly-good-and-cheap-on-prem/5304640) ⭐️ 7.0/10

据《The Register》2026 年 10 月 22 日报道，IBM CEO 公开表示开源权重 AI 模型如今在质量和成本上都已经达到可以在本地（on-prem）部署的水平，对企业而言几乎具有不可抗拒的吸引力。这一表态把自托管大模型从“预算妥协方案”重新定位为许多场景下的可信默认选项。 当一家大型企业级厂商的 CEO 公开为开源权重的本地部署背书时，意味着数据主权与成本可控这两大诉求正从少数人的顾虑变成主流的采购逻辑。这会把竞争压力转移给闭源 API 提供商——当接近前沿水平的开源模型可以跑在企业自有硬件上时，它们必须为高价找到理由。 这一论点的核心有两点：一是开源权重发布（许多来自 DeepSeek、Qwen、Moonshot AI 等中国实验室，以及 Nvidia 的 Nemotron 和 Mistral）已大幅缩小了质量差距；二是一旦企业已拥有 GPU，自托管推理的总拥有成本会显著下降。但仍存在需要注意的地方：许可证条款从宽松的 Apache/MIT 到限制商用不等，此外 GPU 容量规划、量化以及 vLLM 之类的推理服务栈也带来运维负担。

hackernews · Betelbuddy · 10月26日 01:47 · [社区讨论](https://news.ycombinator.com/item?id=50238088)

**背景**: 开源权重模型是指训练好的参数（权重与偏置）被公开发布的 AI 模型，其他人可以下载并在本地运行；这与开源 AI 不同，后者还意味着公开源代码、训练数据和文档。由于这些权重可以在企业自有网络内运行，它们对有敏感数据、无法送往第三方 API 的组织很有吸引力。本地部署（on-premises）指的是在组织自有或可控的基础设施上安装并运行模型，而不是把它当作云服务来消费。来自 OpenAI、Anthropic 和 Google 的付费前沿模型在困难基准上通常仍然领先，因此实际问题在于：某项具体任务是否真的需要最先进的能力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Open-weight_model">Open-weight model</a></li>
<li><a href="https://iternal.ai/how-to-deploy-llm-on-premise">On-Prem LLM Deployment (2026): GPU Sizing, vLLM & Air-Gapped</a></li>
<li><a href="https://deepsense.ai/blog/llm-inference-as-a-service-vs-self-hosted-which-is-right-for-your-business/">LLM Inference as a Service vs. Self - Hosted | Decision Guide</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的评论者总体上表示认同：有人称自己已数月未使用付费模型，靠一台 8 卡 GPU 主机和两台 DGX Spark 完成工作，虽然结果略弱但可接受，因为人仍在回路中纠正，而且隐私得以保留。也有人表示 GLM 5.2/5.3 这类接近前沿的开源模型、甚至把 Gemini Flash 当作日常主力，已足以交付代码，并指出借助 OpenRouter 这类服务无需购买 GPU 就能试用开源模型。还有不少人对 IBM 的动机持怀疑态度——硬件和大型机正是它卖的——但仍认为一个有资源、有分量的老牌厂商来制衡几家 AI 实验室是件好事。

**标签**: `#open-weight-models`, `#on-prem-ai`, `#llm-deployment`, `#ai-infrastructure`, `#hackernews-discussion`

---

<a id="item-3"></a>
## [F-Zero X 3DS 移植复盘：约 5000 美元 LLM 成本](https://hypnotize.works/gdx-3ds/postmortem/index.html) ⭐️ 7.0/10

一位爱好者开发者发布了将《F-Zero X》移植到 Nintendo 3DS 的详细复盘，并披露了约 5,000 美元的 AI/LLM API 成本明细。作者估算，这笔支出相当于约 25 万至 40 万美元的人类工程工作量。 这一案例表明，LLM 辅助开发可能大幅降低复杂逆向工程和游戏移植的成本与门槛。它对复古游戏自制软件、反编译社区以及使用 AI 编程工具的独立开发者都有直接影响。 约 5,000 美元是按 API 标价计算的，评论者指出订阅套餐或多个账号可能让实际支出大不相同。作者还预告即将加入原版 3DS 上的 64DD 内容、本地与在线多人模式，以及自定义赛道的 QR 码分享。

hackernews · bpierre · 10月25日 23:27 · [社区讨论](https://news.ycombinator.com/item?id=50237078)

**背景**: 《F-Zero X》是 1998 年登陆 Nintendo 64 的未来竞速游戏。自制软件（homebrew）指爱好者为 Nintendo 3DS 等封闭游戏机制作的非官方软件，3DS 拥有活跃的 homebrew 社区。将 N64 游戏移植到 3DS 通常需要逆向分析游戏逻辑与资源，反编译项目会从 ROM 重建 C 源代码来辅助这一过程。如今 LLM 也被用于加速汇编分析、代码转换和调试。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Nintendo_3DS_homebrew">Nintendo 3DS homebrew</a></li>
<li><a href="https://deepwiki.com/inspectredc/fzerox">inspectredc/fzerox | DeepWiki</a></li>
<li><a href="https://github.com/BttrDrgn/f-zerox">GitHub - BttrDrgn/ f - zerox : F - Zero X Decompilation · GitHub</a></li>

</ul>
</details>

**社区讨论**: 评论者感谢作者公开成本明细，并追问 API 标价与订阅价格哪一个更能反映真实支出。作者本人参与讨论并预告了即将发布的 64DD 支持、多人模式和 QR 码赛道分享更新；也有人好奇为什么性能更强的 Switch 没有成为《Melee》和《F-Zero X》等移植的首选，反而是 3DS 成了热门目标。

**标签**: `#retro-gaming`, `#homebrew`, `#nintendo-3ds`, `#ai-assisted-development`, `#game-porting`

---

<a id="item-4"></a>
## [上下文工程超越长度限制：记忆架构与策略性遗忘](https://www.dbreunig.com/2026/10/24/the-state-of-context-engineering.html) ⭐️ 7.0/10

2026 年 10 月 24 日发布的新文章《The State of Context Engineering》指出，上下文工程不只是把更多 token 塞进 LLM 上下文窗口，而是围绕信息组织、记忆架构设计以及对陈旧或冲突细节的策略性遗忘展开。该文在 Hacker News 引发了实质性讨论，涉及依赖长度、分层摘要，以及如何区分上下文问题与模型权重问题。 随着越来越多团队构建 LLM 智能体和长时运行工作流，瓶颈正从原始上下文窗口大小转向信息如何被选择、组织、摘要并随时间丢弃。该讨论为开发者提供了实用词汇，用来理解单纯升级“更长上下文”无法解决的可靠性与成本问题。 评论者强调依赖长度（dependency length）——让相关概念在文本中彼此靠近——并提到 VictorTaelin 的 UniiChat 思路：把每条消息摘要成一行，再构建分层二叉树，智能体可通过“缩放”工具按需查看细节。讨论还强调对混乱、冲突记忆进行策略性遗忘，但也有人反驳说，文中 FireRed 泡茶任务的例子实际是模型权重层面的问题，而非上下文污染。

hackernews · pchristensen · 10月25日 20:32 · [社区讨论](https://news.ycombinator.com/item?id=50235780)

**背景**: LLM 只能基于有限的上下文窗口生成回答，窗口内所有内容都会竞争模型的注意力。提示工程主要关注如何写指令，而上下文工程把范围扩大到生成前提供的全部信息：文档、工具输出、历史对话和记忆。智能体要跨多轮交互持续工作，就需要在保留有用记忆与控制上下文规模之间权衡。策略性遗忘是相关研究方向，研究如何按效用动态保留或删除记忆，而不是无限积累。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.promptingguide.ai/guides/context-engineering-guide">Context Engineering Guide | Prompt Engineering Guide</a></li>
<li><a href="https://arxiv.org/pdf/2607.22562">SF-AMS: Strategic Forgetting for Structured Memory in LLM Agent</a></li>
<li><a href="https://arxiv.org/abs/2605.08538">Human-Inspired Memory Architecture for LLM Agents</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍欢迎文章不再把“上下文太长”当作替罪羊，并提出了一些具体技术：按依赖长度排序、UniiChat 式分层摘要，以及类似人类的策略性遗忘。讨论在术语上存在分歧，尤其是 FireRed 泡茶例子究竟属于上下文污染还是模型权重问题。还有评论者把实践挑战概括为：应用框架应在何时保持确定性、何时交给模型驱动。

**标签**: `#context engineering`, `#LLMs`, `#AI agents`, `#memory management`, `#prompt engineering`

---

<a id="item-5"></a>
## [OpenAI 与 Anthropic 最高降价 80%，LLM 价格战为何升级？](https://minimaxir.com/2026/10/cheap-llms/) ⭐️ 7.0/10

一篇被广泛讨论的分析称，OpenAI 与 Anthropic 在短短数月内将大语言模型 API 价格最高下调了 80%。 这轮降价表明，前沿模型的价格正被竞争压低，尤其是来自中国厂商和开放权重模型的低价冲击，这将影响开发者的供应商选择以及构建 AI 产品的成本结构。 原始信息缺少逐模型的价格数据，但社区评论提到 Kimi、GLM 和 DeepSeek 等更便宜的替代方案，并质疑降价究竟来自推理效率提升还是利润让渡。评论还引用 DeepSeek 所称 Flash V4 每 GPU 每小时约 38 美元的收入，作为低价词元仍能对应可观硬件收入的例子。

hackernews · minimaxir · 10月25日 21:11 · [社区讨论](https://news.ycombinator.com/item?id=50236102)

**背景**: 大语言模型通常按词元计费，而推理——即运行模型来回答请求——是持续发生的主要成本，与一次性训练成本不同。随着硬件利用、批处理、模型架构优化以及开放权重模型的竞争加剧，服务商会不断下调每词元价格。不过，单价下降不一定意味着总账单下降，因为智能体式应用完成一个任务可能发起数十到数百次模型调用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://a16z.com/llmflation-llm-inference-cost/">Welcome to LLMflation - LLM inference cost is going down fast</a></li>
<li><a href="https://www.institutepm.com/knowledge-hub/ai-inference-cost-paradox">The AI Inference Cost Paradox: Why Your Bill Keeps Rising as Token ...</a></li>
<li><a href="https://benchlm.ai/llm-pricing-trends">LLM API Pricing Trends & Updates (October 2026) | BenchLM.ai</a></li>

</ul>
</details>

**社区讨论**: 评论者意见分歧：有人表示在遭遇 OpenAI 与 Anthropic 的“网络安全”拒答后转向更便宜的 Kimi 和 GLM 模型；也有人认为这是不可持续的“向下竞底”，甚至可能预示又一轮 AI 寒冬。一个反复出现的观点是，监管压力与中国开放模型的竞争是这场价格战的核心。

**标签**: `#LLM pricing`, `#AI industry`, `#inference economics`, `#competition`, `#Hacker News`

---

<a id="item-6"></a>
## [《经济学人》：中国 AI 进步日益依赖蒸馏美国模型](https://www.economist.com/science-and-technology/2026/10/25/china-increasingly-depends-on-copying-american-ai) ⭐️ 7.0/10

《经济学人》科技版于 2026 年 10 月 25 日刊文指出，中国 AI 实验室正越来越依赖模型蒸馏——即利用从美国领先模型处获取的输出结果来训练自身系统——而非进行原创性研究。文章认为，这种依赖既可能招致美国的政治与监管反弹，也会同时限制中国模型依靠自身所能达到的上限。 蒸馏正处于不断升级的 AI 竞争核心：OpenAI、Anthropic 等美国实验室已公开指责中国开发者挖掘其模型输出以打造更廉价的竞品，这为收紧 API 访问规则与出口管制提供了更多理由。如果文章论点成立，中国从模仿中获得的短期收益可能以牺牲长期自主创新为代价，并影响两国政府在前沿 AI 政策上的取向。 蒸馏技术将大型"教师"模型的行为迁移到更小、更廉价的"学生"模型中；由于它依赖查询模型的输出结果，在技术上很难被检测或彻底封堵。这种方法还存在结构性天花板：学生模型通常只能逼近、而难以超越其训练所依据的教师模型的能力。

rss · The Economist · 10月25日 17:44

**背景**: 知识蒸馏由 Geoffrey Hinton 等人在 2015 年一篇被广泛引用的论文中提出，最初用于将大型神经网络压缩为运行成本更低的小模型，学生模型学习模仿教师模型的输出概率分布，而不仅仅是硬标签。在大语言模型时代，这一技术被赋予了新用途：开发者可以通过 API 从前沿模型处收集大量回复，作为训练自身系统的数据，从而在拿不到权重和训练代码的情况下实质上复制其能力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Model_distillation">Model distillation</a></li>
<li><a href="https://www.scientificamerican.com/article/what-is-ai-model-distillation-and-why-is-it-so-hard-to-stop/">What is AI model distillation , and why is it so... | Scientific American</a></li>
<li><a href="https://arxiv.org/abs/1503.02531">[1503.02531] Distilling the Knowledge in a Neural Network Knowledge Distillation Tutorial [2503.12067] A Comprehensive Survey on Knowledge Distillation A novel knowledge distillation method for graph neural ... Knowledge Distillation in Neural Network Optimization</a></li>

</ul>
</details>

**标签**: `#AI`, `#China`, `#model distillation`, `#geopolitics`, `#LLMs`

---

<a id="item-7"></a>
## [OpenLDK 将 Java JIT 与运行时引入 Common Lisp](https://atgreen.github.io/repl-yell/posts/openldk-java-in-common-lisp/) ⭐️ 7.0/10

OpenLDK 是一个用 Common Lisp 实现 Java JIT 编译器与运行时的项目，使 Java 库可以在 Lisp 环境中使用。它把 Java 类映射为 CLOS 类，并借助 GNU Classpath Exception 使用 OpenJDK 的核心运行时库。 这为 Common Lisp 开发者提供了一条直接利用庞大 Java 生态的途径，无需离开自己的语言或运行独立的 JVM 进程，可简化需要特定 Java 库的 Lisp 应用集成。它也是一个不同寻常的互操作实验，可能引起两个语言社区的关注。 该项目是一个聚焦互操作的方案，而不是传统 JVM 的完整替代品；搜索结果提醒，若重视隔离性、广泛的 JVM 兼容性和成熟的 Java 运行时行为，应将其与独立的 Java 服务或进程边界方案进行评估比较。搜索结果显示其 GitHub 仓库当时约有 271 颗星。

rss · Lobsters · 10月26日 06:15

**背景**: Common Lisp 是一种标准化的 Lisp 方言，以其宏系统和 CLOS 对象系统著称。Java 程序通常运行在 JVM 上，由 JVM 执行字节码并提供核心库；JIT 编译器会在运行时把字节码翻译成本地代码。OpenLDK 在 Common Lisp 内部重新实现了这一 Java 执行层，并在 GNU Classpath Exception 下使用 OpenJDK 的库，该例外条款允许以不同许可证的代码与这些库链接。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/atgreen/openldk">A JIT Compiler and Runtime for Java in Common Lisp - GitHub</a></li>
<li><a href="https://reporank.net/en/repo/atgreen-openldk.html">OpenLDK: Java JIT and Runtime for Common Lisp</a></li>
<li><a href="https://open-awesome.com/projects/openldk">open-ldk — Java JIT Compiler in Lisp | Open Awesome</a></li>

</ul>
</details>

**标签**: `#Common Lisp`, `#Java`, `#JVM`, `#interoperability`, `#OpenLDK`

---

<a id="item-8"></a>
## [在 2 美元的 ESP32 级微控制器上用 SIMD 加速运行计算机视觉](https://shraiwi.com/blog/simd-fast-esp32s3/) ⭐️ 7.0/10

shraiwi.com 上的一篇新博文展示了如何利用 SIMD（单指令多数据）加速，在一颗价格约 2 美元的 ESP32 级微控制器上运行计算机视觉负载。文章详细讲解了在这颗超低成本芯片上的优化思路，说明通常需要更强硬件才能完成的视觉任务，可以被下放到成本极低的设备上运行。 边缘 AI 和嵌入式开发者一直在寻找无需增加树莓派、GPU 或云端往返就能在本地运行感知任务的方法，而把视觉任务压缩到一颗 2 美元的 MCU 上，可能大幅降低智能摄像头、机器人和物联网传感器的成本与功耗预算。这也是一个很有价值的案例，说明手工调优的 SIMD 优化能把有限的微控制器硬件性能挖掘到什么程度。 该工作面向 ESP32 系列，其中较新的型号（如 ESP32-S3）带有 PIE 向量扩展，可提供 32 位和 128 位 SIMD 操作，非常适合像素填充、alpha 运算以及音频/DSP 类负载。与任何 SIMD 移植一样，性能收益高度依赖数据布局以及内层循环能否有效映射到宽寄存器上，因此实际加速比是因负载而异的，并非普遍适用。

rss · Lobsters · 10月25日 14:57

**背景**: SIMD 是一种并行计算技术，单条指令可同时作用于多个数据元素，这些元素通常被打包进 128 位或更宽的寄存器中；它是加速图像与信号处理中重复性算术运算最有效的手段之一。ESP32 是由乐鑫科技（Espressif Systems）设计、台积电以 40 纳米工艺制造的一系列低成本低功耗微控制器，广泛用于物联网设备；其较新的型号加入了向量指令，使得类 DSP 负载在一颗仅售几美元的芯片上也能实用化。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Single_instruction,_multiple_data">Single instruction, multiple data - Wikipedia</a></li>
<li><a href="https://zbotic.in/esp32-s3-ai-camera-tinyml-object-detection-on-device/">ESP 32 - S 3 AI Camera: TinyML Object Detection On-Device - Zbotic</a></li>
<li><a href="https://en.wikipedia.org/wiki/ESP32">ESP32 - Wikipedia</a></li>

</ul>
</details>

**标签**: `#embedded systems`, `#SIMD`, `#computer vision`, `#ESP32`, `#performance optimization`

---

<a id="item-9"></a>
## [斯坦福与 UC Berkeley 的 TokenGate 将长上下文预填充提速至多 11.3 倍](https://www.reddit.com/r/LocalLLaMA/comments/1xfovxr/researchers_from_stanford_and_uc_berkeley/) ⭐️ 7.0/10

斯坦福大学和 UC Berkeley 的研究人员推出了 TokenGate，这是一种轻量级可学习的 token 剪枝模块，利用 token 门控注意力将 Transformer 大模型的长上下文预填充加速至多 11.3 倍。该工作发表于 arXiv 论文 2610.26754，并在 r/LocalLLaMA 上引发关注。 当大模型处理超长提示词时，预填充往往是主要开销，因此大幅提速可能让长文档分析、检索增强生成和智能体工作负载更便宜、更迅捷。如果所声称的收益能够泛化，这项技术可能影响推理系统的设计与部署方式。 由于 Top-K token 选择不可微，TokenGate 借用了混合专家（MoE）风格的技巧：token 重要性分数会在门控之上重新加权注意力 logits，为评分器提供梯度回传路径，同时使用可学习的逐头增益和温度参数。作为一种剪枝方法，它必然以牺牲部分 token 信息来换取速度，因此其对准确率的影响以及在不同模型和任务上的表现，是需要对照论文重点验证的问题。

reddit · r/LocalLLaMA · /u/MundanePercentage674 · 10月26日 06:06

**背景**: 长上下文大模型推理主要有两个阶段：预填充阶段处理完整输入提示并构建 KV cache，解码阶段则逐个生成输出 token。由于自注意力会让每个 token 与许多其他 token 交互，预填充成本会随输入长度增长，因此研究者采用稀疏注意力和 token 剪枝来跳过不太重要的交互。TokenGate 引入可学习的门控，使 token 剪枝能够端到端训练，而不是作为固定启发式规则使用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2610.26754">[2610.26754] TokenGate: Adapting LLMs for Fast and Memory ...</a></li>
<li><a href="https://www.marktechpost.com/2026/10/25/stanford-berkeley-tokengate-learned-token-pruning-llm-prefill/">Researchers from Stanford and UC Berkeley Introduce TokenGate ...</a></li>
<li><a href="https://huggingface.co/papers/2610.26754">Paper page - TokenGate : Adapting LLMs for Fast and...</a></li>

</ul>
</details>

**标签**: `#long-context`, `#attention-mechanism`, `#LLM-inference`, `#efficiency`, `#research-paper`

---

<a id="item-10"></a>
## [三元 1.58-bit Nemotron 30B-A3B MoE 发布 GGUF，可在 12 GB 显卡上运行](https://www.reddit.com/r/LocalLLaMA/comments/1xfqi2d/boro64ternarynemotron35lightning30ba3bgguf/) ⭐️ 7.0/10

在 r/LocalLLaMA 上公布的 Hugging Face 仓库（boro64/Ternary-Nemotron-3.5-Lightning-30B-A3B-GGUF）将基于 Nemotron 的三元（1.58-bit）量化 30B-A3B 混合专家模型打包成单个 GGUF 文件，可在 12 GB 显卡上以 368K 上下文运行。作者报告解码速度 172 tok/s、预填充 7000+ tok/s，并已在原版 llama.cpp 的 b11555+ 与 b11796 构建以及 PrismML/Bonsai 分支的 b10793 构建上完成验证。 这是本地推理的一个实用里程碑：极低比特的三元权重叠加 MoE 稀疏激活，使得一个 30B 级别的模型可以舒适地装进消费级 12 GB 显卡，同时保留超长上下文。更关键的是，它是继 maple-preview 之后第二个能在上游 llama.cpp 上运行的三元 MoE，意味着用户不再必须依赖实验性分支才能尝试这类模型。 该发布是同一个文件即可在两种引擎中运行，作者明确说明它是继 maple-preview 之后第二个兼容原版 llama.cpp 的三元 MoE；所报告的吞吐数据并未附上测试方法，而且作者仍在向社区征集纯 CPU 以及约 10 GB 显存下的基准数据。与所有 1.58-bit 模型一样，相对全精度基线的质量损失才是真正的悬念，而这些跑分并未回答这一点。

reddit · r/LocalLLaMA · /u/pmttyji · 10月26日 07:49

**背景**: 三元（1.58-bit）量化将每个权重大致约束为 {-1, 0, +1} 再配合一个共享缩放因子，相比 FP16 可将显存占用降低一个数量级；但与 Q4 这类训练后量化不同，三元化通常必须在训练阶段就固化下来，不能随意把任意一个检查点直接三元化。“30B-A3B”这种写法指的是混合专家（MoE）模型：总参数约 300 亿，但每个 token 只激活约 30 亿参数，因此它既存下了大量知识，又只需约 3B 模型的计算量，生成速度很快。GGUF 是 llama.cpp 的单文件模型格式，而 llama.cpp 是当前主流的开源 C/C++ 推理引擎，可在消费级显卡、CPU 与 Apple 芯片上运行量化模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://runaihome.com/blog/ternary-llm-1-58-bit-quantization-home-lab-2026/">Breaking the 1 . 58 - Bit Barrier: What Ternary LLM Quantization Means...</a></li>
<li><a href="https://bestllmfor.com/guide/moe-mixture-experts-explique/">MoE explained: why a 30B-A3B runs like a small model model</a></li>
<li><a href="https://docs.prismml.com/run/llamacpp">llama.cpp - Bonsai - docs.prismml.com</a></li>

</ul>
</details>

**社区讨论**: r/LocalLLaMA 的讨论帖偏向实用而非技术辩论：评论者主要索要纯 CPU 的基准数据，以及约 10 GB 这种极小显存配置下的跑分，作者本人也在帖中重复了这一请求。关于三元方法本身几乎没有争论，讨论焦点在于在更多硬件配置上验证那些亮眼的速度与显存数据。

**标签**: `#local-llm`, `#quantization`, `#mixture-of-experts`, `#llama.cpp`, `#low-vram-inference`

---

<a id="item-11"></a>
## [RTX 3080 20GB 解锁 ReBAR 与 P2P，张量并行预填充最高提速 115%](https://www.reddit.com/r/LocalLLaMA/comments/1xf9kmd/rtx_3080_20gb_got_rebar_and_p2p_unlock_70_prompt/) ⭐️ 7.0/10

r/LocalLLaMA 上的一篇社区报告（原作者为 u/nathannguyennng）显示，在一对改装版 20GB RTX 3080 上同时解锁 GPU-unlock、Resizable BAR（ReBAR）与点对点（P2P）通信后，vLLM 张量并行模式下的提示词处理速度相比原始状态提升了 70% 至 115%。在测试中，8K token 的预填充从 967 tok/s 提升到 2080 tok/s，261,900 token 的超长用例从 562 tok/s 提升到 961.6 tok/s，而 token 生成速度基本没有变化，波动处于噪声范围内。 张量并行是本地 LLM 用户运行超出单卡显存模型的主要手段，而 GPU 间通信通常是预填充阶段的瓶颈，因此一个几乎让提示词处理速度翻倍的固件/驱动层面免费解锁，对双 3080/3090 平台来说收益很大。这一改进对长上下文和智能体编程类负载尤为重要——等待 26 万 token 的提示词处理正是主要耗时所在，同时也说明已被停产的消费级架构仍有未被挖掘的潜力。 测试环境为 Proxmox VE 9.2.21、内核 6.14.11-9-pve、驱动 615.71.09，平台是 X399 Zenith Extreme 主板上的 Threadripper 1920X，两张显卡均插在 PCIe 3.0 x16 插槽并限制在 240W 功耗，vLLM 0.32.0 部署 27B AWQ INT4 模型，启用 FP8 KV 缓存、分块预填充、前缀缓存以及 MTP 投机解码。关键在于，加速幅度随提示词长度变化（8K 时 115%，262K 时 71%），解码阶段的 token 间延迟没有稳定改善，而且结果依赖于非官方的 20GB 改装卡与社区解锁工具，并非任何官方支持的配置。

reddit · r/LocalLLaMA · /u/No-Refrigerator-1672 · 10月25日 18:16

**背景**: Resizable BAR（ReBAR，AMD 称之为 Smart Access Memory）是一项可选的 PCIe 特性，允许 CPU 一次性映射 GPU 的全部显存，而不是沿用传统的 256MB 窗口，从而改善主机与设备之间的数据传输效率。点对点（P2P）属于 NVIDIA GPUDirect 体系，可让一块 GPU 通过 PCIe 或 NVLink 直接读写另一块 GPU 的显存，无需经由系统内存中转。张量并行把模型各层切分到多块 GPU 上，因此每一层都需要卡间进行 all-reduce 通信，卡间链路越快，预填充速度就越快。RTX 3080 20GB 并非 NVIDIA 官方型号，而是把公版 10GB 显存翻倍的改装卡（多来自矿卡时期的产线）。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.intel.com/content/www/us/en/support/articles/000090831/graphics.html">What Is Resizable BAR and How Do I Enable It? - Intel</a></li>
<li><a href="https://developer.nvidia.com/gpudirect">GPUDirect | NVIDIA Developer</a></li>
<li><a href="https://docs.vllm.ai/en/latest/serving/parallelism_scaling/">Parallelism and Scaling - vLLM</a></li>

</ul>
</details>

**标签**: `#LocalLLaMA`, `#GPU`, `#tensor-parallel`, `#vLLM`, `#hardware-modding`

---