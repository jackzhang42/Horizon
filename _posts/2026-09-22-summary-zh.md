---
layout: default
title: "Horizon Summary: 2026-09-22 (ZH)"
date: 2026-09-22
lang: zh
---

> 从 77 条内容中筛选出 28 条重要资讯。

---

1. [小米 MiMo-V2.6-Pro：训练成本仅 300 万美元的 1T 开放权重模型](#item-1) ⭐️ 9.0/10
2. [vLLM v0.30.0 发布：新增模型支持、持久权重缓存与 HiSparse 分层](#item-2) ⭐️ 8.0/10
3. [你拥有的只有注意力](#item-3) ⭐️ 8.0/10
4. [Bryan Cantrill 复盘 Sun Microsystems 究竟错在哪里](#item-4) ⭐️ 8.0/10
5. [文章主张：LLM 代笔的文字无法实现真正的沟通](#item-5) ⭐️ 8.0/10
6. [Cloudflare Python Workers 结束两年预览正式全面可用](#item-6) ⭐️ 8.0/10
7. [xAI 发布 Grok 4.7：权重增加 40%，价格保持不变](#item-7) ⭐️ 8.0/10
8. [Nathan Lambert 扩展其国会证词，阐述开放模型的权力格局](#item-8) ⭐️ 8.0/10
9. [阿里巴巴在云栖大会正式宣布 Qwen 4](#item-9) ⭐️ 8.0/10
10. [Phantom-KV：注入约 18MB 可热插拔 KV 缓存库即可解除 LLM 拒答](#item-10) ⭐️ 8.0/10
11. [“Spymarks”：隐蔽内容追踪带来的监控威胁](#item-11) ⭐️ 7.0/10
12. [Polo Club 推出交互式 Transformer 讲解器，引发注意力机制教学讨论](#item-12) ⭐️ 7.0/10
13. [AI 编码代理让 CI 成为瓶颈，Linear 重构其流水线](#item-13) ⭐️ 7.0/10
14. [NASA 火星采样返回任务因成本超支而被取消](#item-14) ⭐️ 7.0/10
15. [LWN 展望 Git 2.56 与 3.0，引发 SHA-256 迁移讨论](#item-15) ⭐️ 7.0/10
16. [陶哲轩宣布成立数学与人工智能咨询小组](#item-16) ⭐️ 7.0/10
17. [HERMES 开源短波电台实现远距离数字语音与数据传输](#item-17) ⭐️ 7.0/10
18. [苹果 Copland D11E4 通过 DingusPPC 模拟在浏览器中启动](#item-18) ⭐️ 7.0/10
19. [恶意 npm 包 mathmain 用触发矩阵隐藏加密加载器](#item-19) ⭐️ 7.0/10
20. [TypeSafe AI 发布 Jev：输出概率而非文本的决策模型](#item-20) ⭐️ 7.0/10
21. [OpenAI 呼吁建立全球共享的人工智能安全标准](#item-21) ⭐️ 7.0/10
22. [央行人士主张：数字货币的未来要靠公共货币而非私人货币](#item-22) ⭐️ 7.0/10
23. [书评：并行编程难吗？如果难，又能怎么办？](#item-23) ⭐️ 7.0/10
24. [用同一套代码库同时构建 GBA 与 PC 游戏](#item-24) ⭐️ 7.0/10
25. [阿里巴巴计划打造 5 万亿至 10 万亿参数 AI 模型并发布新芯片](#item-25) ⭐️ 7.0/10
26. [小米将 MiMo-V2.6 蒸馏进 Qwen 9B 模型](#item-26) ⭐️ 7.0/10
27. [Yandex 发布 AliceAI-Foundation-80B-A3B-Base，一款自研架构的俄罗斯 MoE 基础模型](#item-27) ⭐️ 7.0/10
28. [SupraLabs 发布 Supra2-IMG：100M 参数的文本生成图像 DiT 模型，训练不到 10 小时](#item-28) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [小米 MiMo-V2.6-Pro：训练成本仅 300 万美元的 1T 开放权重模型](https://www.latent.space/p/ainews-xiaomi-mimo-v26-pro-1t-a42b) ⭐️ 9.0/10

小米发布了 MiMo-V2.6-Pro，这是一个开放权重的混合专家（MoE）模型，总参数量 1.02T、激活参数 42B，同时还有一个更小的 Flash 版本（总参数 309B、激活 15B），并宣称其登顶开放权重模型榜首。小米表示 Pro 模型的训练成本约为 300 万美元，并公开了一份技术报告以及记录强化学习过程的实时训练看板。 如果约 300 万美元的训练成本属实，这将标志着构建前沿级模型的经济门槛发生质变，使资金充裕的实验室乃至大型高校也能涉足万亿参数级别的训练。同时，这也进一步巩固了中国在开放权重发布上的领先地位，让小米加入 DeepSeek、阿里 Qwen、月之暗面（Moonshot AI）与 Z.ai 的行列，并对坚持闭源的美国实验室形成压力，迫使其为闭源策略给出更有说服力的理由。 该模型采用稀疏架构：1.02T 总参数中每个 token 仅激活 42B，这正是其推理与训练算力远低于同等稠密万亿参数模型的原因。小米还公开了异常详尽的方法论文档，包括实时强化学习看板；社区引用的基准显示，MiMo-V2.6-Pro 在 Terminal Bench 4.0 上得分 34.9，而 GPT 6 Astra 为 59.6，说明它在部分智能体任务上仍落后于最强的闭源系统。

rss · Latent Space · 9月22日 06:30

**背景**: 混合专家（MoE）模型把网络层拆分为许多专门的子网络，即“专家”，并为每个输入 token 只路由到其中少数几个，因此模型可以拥有极大的总容量，却只在很小的一部分激活参数上消耗算力。“开放权重”指训练好的参数可公开下载，但具体能做什么由许可证决定，而未必包含训练数据或源代码，这与完全开源的 AI 有所区别。DeepSeek、阿里云、月之暗面与 Z.ai 等中国实验室已将开放权重发布作为默认策略，而 OpenAI、Anthropic、Google DeepMind 等美国主要实验室则大体上把最大的模型保持闭源。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mixture_of_experts">Mixture of experts - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Open-weight_model">Open-weight model</a></li>
<li><a href="https://huggingface.co/blog/moe">Mixture of Experts Explained</a></li>

</ul>
</details>

**社区讨论**: 评论者称赞小米的透明度，尤其是实时训练看板和详尽的技术报告，同时也提到关于“何为真正开放模型”的持续争论（权重、训练数据与代码之间的区别）。有讨论认为中国凭借电力与电网建设方面的优势，从长期看可能赢得 AI 竞赛；另有用户对基准测试结果持怀疑态度，认为 Terminal Bench 4.0 与 ExploitGym 相对更可信。

**标签**: `#AI`, `#open-weights`, `#LLM`, `#Xiaomi`, `#training-efficiency`

---

<a id="item-2"></a>
## [vLLM v0.30.0 发布：新增模型支持、持久权重缓存与 HiSparse 分层](https://github.com/vllm-project/vllm/releases/tag/v0.30.0) ⭐️ 8.0/10

vLLM 发布了 v0.30.0，该版本包含来自 315 位贡献者（其中 104 位是新贡献者）的 762 次提交，新增了对 DeepSeek-V4.1-Flash、DeepSeek-V4-Flash-Vision-Exp、GLM-5.3-Flash、K2-Horizon、Cohere Compass、Bailing V3 VL、Nanbeige4.2 等模型的支持，并带来了基于 AVX512/AMX 稀疏 MLA 内核的 DeepSeek-V4 CPU 后端。本版本最核心的性能特性是 "Fast Start"：一个常驻的每 GPU 权重缓存守护进程，将量化后、按张量并行切分的权重保留在 GPU 显存中，使重启的引擎可以通过 CUDA IPC 直接映射这些权重（使用 `--load-format ipc_cache`），而无需再从磁盘重新加载。 vLLM 是目前部署最广泛的开源大模型推理服务引擎之一，因此这些改动会直接进入生产推理栈：Fast Start 能显著缩短引擎重启和自动扩缩容的延迟，而新增的 CPU 与 ROCm 后端则把 vLLM 可服务的硬件范围扩展到了 NVIDIA GPU 之外。对最新的前沿模型家族（DeepSeek-V4.x、GLM-5.3、K2-Horizon）提供首日支持，也对需要快速上线这些模型的团队非常重要。 IPC 权重缓存现在也覆盖 FP4 检查点和多节点张量并行；新增的 HiSparse 特性为稀疏 MLA 解码引入了一个驻留主机的存储层级，在 GPU 显存紧张时把 KV 页溢出到锁页主机内存，并通过 `HiSparseConnector` 用每个请求的 GPU 热缓冲区来服务 top-k 未命中。其他值得注意的工程优化包括：在 CUDA 图捕获期间冻结垃圾回收，把捕获时间从 12 秒降到 2 秒（H200 上引擎初始化从 28.9 秒降到 8.2 秒），以及修复了 `--return-sampling-mask` 带来的约 2 倍强化学习步时回归。

github · khluu · 9月22日 05:20

**背景**: vLLM 是一个开源的大语言模型推理服务引擎，它提出了用于高效管理 KV 缓存的 PagedAttention，常被用来在 GPU 集群上运行 DeepSeek、Qwen 等模型。FlashMLA 是 DeepSeek 开源的优化版多头潜在注意力（MLA）解码内核库；本次发布说明中提到，DeepSeek-V4.1-Flash 的 KV 缓存完全以 MXFP8 存储，这是一种 8 位“微缩放”浮点格式，每小组数值共享一个缩放因子。CUDA IPC 是 CUDA 提供的一项能力，允许一个进程把 GPU 显存分配导出为句柄，让同一台机器上的另一个进程直接映射和使用，这正是新的 Fast Start 权重缓存所依赖的机制。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/deepseek-ai/FlashMLA">GitHub - deepseek-ai/ FlashMLA : FlashMLA : Efficient Multi-head...</a></li>
<li><a href="https://docs.nvidia.com/cuda/cuda-programming-guide/04-special-topics/inter-process-communication.html">4.16. Interprocess Communication — CUDA Programming Guide</a></li>
<li><a href="https://vllm.ai/blog/2026-06-12-minimax-m3-vllm">MiniMax M3 in vLLM: Day-0 Serving for 1M-Token Multimodal Reasoning</a></li>

</ul>
</details>

**标签**: `#vLLM`, `#LLM inference`, `#model serving`, `#AI/ML systems`, `#release`

---

<a id="item-3"></a>
## [你拥有的只有注意力](https://alicegg.tech/2026/09/21/attention) ⭐️ 8.0/10

一篇关于在数字时代从社交媒体和无尽刷屏中夺回注意力的文章及 Hacker News 讨论。

hackernews · Lobsters · 9月21日 14:26 · [社区讨论](https://news.ycombinator.com/item?id=49787726)

**标签**: `#attention economy`, `#social media`, `#digital wellbeing`, `#doomscrolling`, `#hacker news`

---

<a id="item-4"></a>
## [Bryan Cantrill 复盘 Sun Microsystems 究竟错在哪里](https://bcantrill.dtrace.org/2026/09/20/what-sun-got-wrong/) ⭐️ 8.0/10

Bryan Cantrill 在其个人博客发表了题为《What Sun got wrong》的文章，剖析了导致 Sun Microsystems 衰落的一系列战略、销售与工程层面的失误。该文迅速登上 Hacker News 首页，获得 568 分和 326 条评论。 Sun 的崩塌是说明「世界级工程能力仍可能败给更擅长销售的公司」的经典案例，至今仍是讨论技术雄心与商业纪律如何取舍时的重要参照。这场讨论在当下尤有共鸣，因为资深工程师从中看到了与当前 AI 时代高估值和厂商锁定争议的相似之处。 评论者列举了若干具体决策，例如 Sun 在 2002 年短暂取消 x86 版 Solaris，他们认为这摧毁了那些不愿被锁定在 SPARC 平台上的客户的信任；另有 2002 年与 Google 的交易告吹，据称原因是 Sun 坚持要知道 Google 拥有多少台服务器。还有人对比了 Sun 繁琐的报价与销售面谈流程和 Dell 的次日送达，也有人回忆自己在 70 美元卖出 Sun 股票，随后股价跌至 7 美元。

hackernews · chmaynard · 9月21日 14:03 · [社区讨论](https://news.ycombinator.com/item?id=49787436)

**背景**: Sun Microsystems 成立于 1982 年，是那个时代最具影响力的计算机公司之一，打造了基于 SPARC 的工作站与服务器、Solaris 操作系统，以及 NFS、Java、ZFS、DTrace 等技术，并于 2010 年被 Oracle 收购。Bryan Cantrill 是一位系统工程师，以在 Sun 联合创造 DTrace 而闻名，此后他任职于 Joyent 并联合创办了 Oxide Computer，这使他既有第一手经验，也以对行业直言不讳的复盘而著称。

**社区讨论**: 评论区以第一手回忆和事后复盘为主，普遍认同 Sun 更在意打造出色的技术，而非经营一家企业。评论者互相补充对 Sun 销售文化和战略失误的具体不满，也有人怀念 Sun 瘦客户机以及 pine、vi 这类工具，还有人将其与如今 Tesla、SpaceX 和 AI 股票的高估值作警示性类比。

**标签**: `#Sun Microsystems`, `#tech history`, `#engineering culture`, `#business strategy`, `#systems`

---

<a id="item-5"></a>
## [文章主张：LLM 代笔的文字无法实现真正的沟通](https://blog.colinbreck.com/i-dont-want-to-read-what-you-didnt-write/) ⭐️ 8.0/10

Colin Breck 发表了一篇题为《I don't want to read what you didn't write》的博客文章，认为由大语言模型生成的文字并非真正的沟通，因为模型无法提供作者真正想表达的含义。该文登上 Hacker News 首页，获得约 591 分和 215 条评论，讨论围绕 AI 撰写的 Pull Request、文档以及人类作者身份的价值展开。 这篇文章集中体现了软件工程领域日益加剧的一种文化张力：AI 生成的 PR 描述、文档和评审意见正变得司空见惯，而评审者越来越觉得自己读到的是填充物而非真实推理。它在 Hacker News 上引发的强烈共鸣表明，关于 AI 辅助写作中真实性与责任归属的争论，已经从一个抽象话题变成了日常工程实践中的现实问题。 讨论中的批评者指出了一个现实中的失败模式：20 行代码改动如今有时会附带数页生成的论证、风险分析和对每项设计决策的辩护，评审者感到不得不读却又并非自己所需。文章的核心论点可以量化——如果作者掌握 1000 比特的语义信息却只交给模型 300 比特，模型无法凭空补足缺失的 700 比特，而它猜对的部分本来也不属于真正的信息。

hackernews · mooreds · 9月21日 22:30 · [社区讨论](https://news.ycombinator.com/item?id=49794330)

**背景**: Pull Request（PR，拉取请求）是 GitHub、GitLab 等工具中向代码库提交改动的标准机制，通常会将代码差异与一段解释意图和风险的文字描述配对呈现。Hacker News 是由 Y Combinator 运营的长期技术创业论坛，以围绕此类话题展开高参与度、技术性扎实的讨论而闻名。自大语言模型广泛普及以来，工程师越来越多地用它们起草这些描述、文档和代码评审意见，而本文及其评论区正是对这一做法提出质疑。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.ibm.com/think/topics/pull-request">What Is a Pull Request? - IBM</a></li>
<li><a href="https://en.wikipedia.org/wiki/Hacker_News">Hacker News - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论区总体上与文章立场一致：有评论者把写作视为字面意义上的信息传递，认为 LLM 无法替作者补全这些信息；也有人描述了真实的痛苦经历——为一个小改动写的 PR 却附带了数页 AI 生成的论证，令人不堪卒读。也有持相反意见的声音（earthnail）认为，LLM 可以作为梳理思路的“陪练”，前提是作者亲自校对并反复重写提示词，直到文字确实有效传达信息、不再有 AI 味。

**标签**: `#ai-writing`, `#llm`, `#software-engineering-culture`, `#code-review`, `#communication`

---

<a id="item-6"></a>
## [Cloudflare Python Workers 结束两年预览正式全面可用](https://blog.cloudflare.com/python-workers-ga/) ⭐️ 8.0/10

Cloudflare 宣布 Python Workers 正式全面可用（GA），在经历约两年的预览期后，Python 成为其无服务器边缘平台上的一等公民语言。此次发布还包含上游 HTTP 客户端支持，使 Requests、urllib3 等库能够在 WebAssembly 环境中直接通过 JavaScript 的 fetch API 发起请求。 这把庞大的 Python 生态带到了 Cloudflare 的全球分布式边缘网络上，为开发者提供了 AWS Lambda、Google Cloud Functions 等传统无服务器 Python 方案之外的厂商选择。这同时表明，基于 WebAssembly 的语言运行时正在成熟为可用于生产环境的服务端基础设施，而不再只是浏览器技术。 Python Workers 通过 Pyodide 运行编译为 WebAssembly 的 CPython，因此只有纯 Python 或已预编译的包才能使用，而打包方案已通过 PEP 783（PyEmscripten）实现标准化。冷启动和启动时间是基于 WASM 方案的已知取舍，新的上游支持依赖 JSPI（JavaScript Promise Integration）来将同步的 Python HTTP 调用与异步的 fetch API 衔接起来。

hackernews · torutofu · 9月21日 13:38 · [社区讨论](https://news.ycombinator.com/item?id=49787142)

**背景**: Pyodide 是把 CPython 移植到 WebAssembly/Emscripten 的成果，使得在受限的运行时环境中安装和运行 Python 包成为可能。Cloudflare Workers 是一个无服务器平台，把代码部署到全球边缘网络以实现低延迟执行。WebAssembly（Wasm）是一种面向栈式虚拟机的二进制指令格式，旨在为网页和非网页环境提供高性能应用支持。三者结合，使 Cloudflare 能在边缘的沙箱化 WASM 隔离环境中运行 Python 代码，而非依赖传统的 Linux 容器。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://pyodide.org/en/stable/?ref=more-than-numbers.ghost.io">Pyodide — Version 0.25.1</a></li>
<li><a href="https://developers.cloudflare.com/workers/">Overview · Cloudflare Workers docs</a></li>
<li><a href="https://en.wikipedia.org/wiki/WebAssembly">WebAssembly - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 讨论整体偏正面但技术性很强：一位 urllib3 维护者澄清，Pyodide/Emscripten 与 JSPI 的贡献早在几年前就已合并，且资金流向了实现这些工作的外部贡献者而非维护者本人；Wasmer 创始人 Syrus Akbary 赞赏其进展与 PEP 783 标准化，但也指出仍存在的架构层面顾虑。其他评论者把它与 2008 年 Google App Engine 的 Python 支持相类比，调侃标题被误读为“用 AI 替换了所有 Python 程序员”，还有人追问冷启动性能究竟表现如何。

**标签**: `#cloudflare`, `#python`, `#webassembly`, `#serverless`, `#pyodide`

---

<a id="item-7"></a>
## [xAI 发布 Grok 4.7：权重增加 40%，价格保持不变](https://x.ai/news/grok-4-7) ⭐️ 8.0/10

xAI 发布了 Grok 4.7，这是一款改进幅度适中的前沿模型，其模型权重比 Grok 4.6 多出约 40%，而 API 价格保持不变，仍为每百万输入 token 收费 2 美元、每百万输出 token 收费 6 美元。该消息发布在 Hacker News 上，获得了 553 分和 472 条评论。 此次发布加剧了前沿模型竞赛，而且它的时间点恰好在传闻中的 Anthropic Opus 5.5 发布前一天，说明 xAI 试图在密集的发布窗口期保持存在感。由于模型规模明显扩大而价格未涨，这也透露出利润空间被压缩，以及 xAI 不得不在能力而非价格上参与竞争的压力。 社区对推理强度（reasoning effort）设置的测试发现了异常行为：low 和 medium 档位消耗的 token 数量相近，而 xhigh 档位使用的 token 反而少于 high 档；测试者最初通过 OpenRouter 调用，之后又直接使用 xAI API 重新验证了这一结果。用户还反馈 Grok 4.7 在实际使用中更慢、更贵，这与单次请求消耗更多推理 token 的模型特征相符。

hackernews · meetpateltech · 9月21日 15:50 · [社区讨论](https://news.ycombinator.com/item?id=49788838)

**背景**: 前沿模型（frontier model）指的是在某一时刻可用的能力最强的通用 AI 系统之一，通常来自主要实验室的最新旗舰产品，这个称谓是相对的而非永久的。模型在训练过程中把学到的内容存储为模型权重——本质上是一大堆数字——因此“权重增加 40%”意味着网络规模显著变大，训练和推理通常也需要更多算力。推理模型在给出答案前会“思考”，产生被称为推理 token 的中间步骤，而这些 token 按输出 token（更贵的一类）计费，所以即使每 token 价格不变，思考更久的模型也可能让单次请求的实际成本悄然上升。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://getmorefromai.com/glossary/frontier-model">Frontier model : Definition , Examples, and Why It... | GetMoreFromAI</a></li>
<li><a href="https://answers.mindstick.com/blog/419/why-do-large-language-models-hallucinate-and-why-model-weights-are-not-enough">Why Do Large Language Models Hallucinate and Why Model ...</a></li>
<li><a href="https://redis.io/blog/token-budget-aware-llm-reasoning/">Token-Budget-Aware LLM Reasoning: Cut Costs in 2026 - Redis</a></li>

</ul>
</details>

**社区讨论**: 整体情绪褒贬不一，且以怀疑为主。有评论者认为，模型规模大得多却价格不变，再加上发布时间比原计划晚了近两周，说明 xAI 对 4.7 的结果并不满意，并预测 Opus 5.5 会在基准测试上将其击败——不过也有人表示自己对基准测试本身已越来越怀疑。simonw 等人则以实证方式深挖了推理 token 的行为；一位认为 Grok 4.6 在编程和智能体工作流中完全不堪使用的用户表示，4.7 更慢、更贵，可能只是为了冲榜而“烧 token”；但仍有多人对今年晚些时候 Grok 5 带来的大幅跃升抱有期待。

**标签**: `#LLM`, `#xAI`, `#Grok`, `#Model Release`, `#AI Industry`

---

<a id="item-8"></a>
## [Nathan Lambert 扩展其国会证词，阐述开放模型的权力格局](https://www.interconnects.ai/p/the-current-balance-of-power-in-open) ⭐️ 8.0/10

Interconnects.ai 通讯作者、研究员 Nathan Lambert 发布了他为美国国会准备的证词的扩展书面版本，主题是当前开放 AI 模型之间的力量格局。这篇文章把他原本简短的现场陈述扩展为一份面向政策制定的更完整分析，讨论开放权重模型在竞争中的位置。 由于作者是开放模型领域被广泛阅读的专家，这份证词式分析会直接进入美国正在进行的政策辩论——即是否以及如何监管开放权重 AI 的发布。它为立法者和产业读者提供了一套关于竞争力、安全与开放性的结构化论证，而这些问题当下正同时影响监管走向和模型发布策略。 这是一篇面向政策的论述文章，而非技术发布，因此其中不含基准测试或代码；它的价值在于把原本作为正式国会证词提交的关于开放模型与闭源模型对比的论点系统化。值得注意的是，发布的版本被描述为“扩展形式”，也就是说它包含了现场听证时间限制下无法展开的推理与细节。

rss · Interconnects · 9月21日 11:56

**背景**: 开放模型（常被称为开放权重模型）是指训练好的参数被公开发布的 AI 系统，任何人都可以下载、运行或微调；与之相对的是只能通过 API 访问的闭源模型。围绕它们的争论通常是创新、透明度与美国竞争力之争，与滥用风险担忧之间的对立，这已成为美国 AI 治理讨论的核心议题。国会证词则是专家向立法与监督程序提交书面证据和论点的正式机制。

**标签**: `#AI policy`, `#open models`, `#AI governance`, `#LLMs`, `#open source AI`

---

<a id="item-9"></a>
## [阿里巴巴在云栖大会正式宣布 Qwen 4](https://www.reddit.com/r/LocalLLaMA/comments/1wmxfjs/qwen_4_announced_at_apsara_conference/) ⭐️ 8.0/10

阿里巴巴在云栖大会（Apsara Conference）上正式宣布了 Qwen 4，标志着其 Qwen 大语言模型家族进入下一个大版本。该消息以 r/LocalLLaMA 上一篇仅有一句话加一张截图的形式出现，发帖时并未披露更多技术细节。 Qwen 是使用最广泛的开源权重模型家族之一，因此新的大版本通常会在社区引发一轮微调、基准测试对比以及下游工具适配的热潮。同时这也具有竞争意义，因为阿里巴巴正将 Qwen 定位为与其他领先的开源及闭源模型家族抗衡的产品。 这次消息本身内容非常单薄：只有一张截图和一句话，因此关于参数量、上下文长度、许可条款、多模态能力乃至实际发布日期都没有任何确认信息。从历史上看，Qwen 各代产品会发布多种不同规模的版本，并采用不同的许可条款，因此这些具体信息是后续值得关注的重点。

reddit · r/LocalLLaMA · /u/Salah_H_Hasan · 9月22日 02:45

**背景**: Qwen 又称通义千问，是阿里云开发的以大语言模型和小语言模型为主、以开放权重为主要形式的模型家族；其第一代于 2023 年 4 月开启测试，同年 12 月开源了 72B 模型的权重。凭借较为宽松的许可证和频繁的小模型发布，它成为社区微调和二次修改模型的常见起点。云栖大会（Apsara Conference）是阿里云的年度旗舰技术大会，在杭州举办，2026 年场次于 9 月 22 日至 24 日举行，主题为“AI for Practical Impact”。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Qwen">Qwen - Wikipedia</a></li>
<li><a href="https://www.alibabacloud.com/apsara-conference/2026-about">2026 About Apsara Conference – Alibaba Cloud</a></li>

</ul>
</details>

**标签**: `#LLM`, `#Qwen`, `#Alibaba`, `#open-source-models`, `#model-release`

---

<a id="item-10"></a>
## [Phantom-KV：注入约 18MB 可热插拔 KV 缓存库即可解除 LLM 拒答](https://www.reddit.com/r/LocalLLaMA/comments/1wms904/uncensor_an_llm_without_touching_weights_inject_a/) ⭐️ 8.0/10

开发者 lordx64 发布开源项目 phantom-kv，它把一小批离线训练好的键/值张量（约 18MB）直接注入大模型的 KV 缓存，注意力机制会把它当作已经存在的上下文来读取。由于完全没有改动模型检查点，“解除审查”变成了按请求生效、可热插拔的能力模式：卸载缓存后，基座模型恢复为字节级完全一致。 此前所有移除拒答的方法都要在某处做出永久性改动：权重空间的 abliteration 会重写检查点（并破坏按量化分发的兼容性），激活空间的投影则要在启动时修补模型的信号通路。phantom-kv 把拒答移除变成一种由部署方控制、可与未修改的受约束权重一同分发的开关，这可能改变本地大模型社区与安全团队看待能力门控的方式。 作者自行审计了局限：用 8B 评判模型审计发现，词汇层面的拒答抑制指标会高估合规程度，因为语义上的拒绝常以换一种说法的方式继续存在；在长会话中该“嫁接”会以约 2–4k token 的半衰期衰减，可通过实测的重注入节奏来缓解。回答仍会带上法律/伦理性质的说明框架，而三种能力模式（受约束、防御向“蓝药丸”、攻击向“红药丸”）据称只相差 129 个缓存槽位，而非不同检查点。

reddit · r/LocalLLaMA · /u/Anony6666 · 9月21日 22:55

**背景**: KV 缓存保存注意力机制为先前 token 已经计算出的键和值张量，避免重复计算；正是它让生产环境的推理速度提升约 10–20 倍，代价是显存/内存随上下文长度线性增长。Abliteration 是流行的“无审查”开源权重模型背后的标准做法：它从权重中删除模型的拒答方向，属于对检查点的永久性修改。激活空间投影则在运行时、按 token、按层，在引擎钩子内部减去拒答方向。phantom-kv 两者都不做——它只通过注意力本来就要消费的输入通道来影响模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://magazine.sebastianraschka.com/p/coding-the-kv-cache-in-llms">Understanding and Coding the KV Cache in LLMs from Scratch</a></li>
<li><a href="https://arxiv.org/abs/2607.17427">[2607.17427] Abliteration Is Not a Scalpel: Off-Target ...</a></li>
<li><a href="https://abliteration.org/wiki/academic-research/">Academic papers on abliteration and refusal removal</a></li>

</ul>
</details>

**标签**: `#LLM`, `#KV-cache`, `#refusal-removal`, `#abliteration`, `#AI-safety`

---

<a id="item-11"></a>
## [“Spymarks”：隐蔽内容追踪带来的监控威胁](https://brand.io/article/spymarks/) ⭐️ 7.0/10

一篇题为《Spymarks, Not Watermarks》的新文章指出，嵌入图像和其他内容中的隐蔽追踪标记构成了一种独立于传统水印、且日益严重的监控威胁。文章用“spymarks”这一新词重新概括了已知的隐写技术，强调它们的功能不仅是声明所有权，还可用于识别、归因和追踪个人。 随着越来越多的内容流经 AI 工具、截屏流程和广告技术系统，隐蔽标记可能让企业或政府得以对泄密者、记者和普通用户进行去匿名化。这使水印议题从版权保护转向隐私与公民自由层面的担忧，波及任何在网上分享图片或文档的人。 这一概念与隐写术高度重叠，但文章以意图加以区分：传统水印通常是可见的或被公开承认的所有权声明，而“spymarks”被设计为不可见，常用于泄密追踪或广告归因。文中强调的一个关键局限是：一般无法证明某个标记“不存在”，只能证明它存在，这使检测与清除成为本质上不对称的防御难题。

hackernews · possibilistic · 9月21日 23:03 · [社区讨论](https://news.ycombinator.com/item?id=49794615)

**背景**: 水印是一种由来已久的做法，通过在媒体中嵌入标识信息来证明版权或追踪保密文件的接收者。隐写术则是更广义的“隐藏通信”技术，把信息藏于另一媒介之中，使其存在对第三方不可见，这也是泄密追踪标记和防篡改方案的基础。C2PA、元数据签名等现代内容溯源机制旨在确认媒体的来源与真实性，但隐私倡导者警告，强制溯源可能与匿名性及创作者的自主权发生冲突。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Steganography">Steganography - Wikipedia</a></li>
<li><a href="https://cdt.org/insights/the-promise-and-risk-of-digital-content-provenance/">The Promise and Risk of Digital Content Provenance</a></li>
<li><a href="https://www.nist.gov/publications/reducing-risks-posed-synthetic-content-overview-technical-approaches-digital-content">Reducing Risks Posed by Synthetic Content An Overview of ...</a></li>

</ul>
</details>

**社区讨论**: 评论者大体认同该概念不过是隐写术的“改头换面”，有人指出企业早已在内部网页背景图中嵌入此类标记，以便从截图中识别泄密者。其他人则担忧通过驱动层像素扫描进行广告归因的滥用，并普遍感到避免被追踪的唯一办法是彻底远离新技术；还有评论者提出一种安全工程式的权衡思路，区分“可证明水印存在”与“无法证明水印不存在”。

**标签**: `#privacy`, `#steganography`, `#surveillance`, `#content-provenance`, `#security`

---

<a id="item-12"></a>
## [Polo Club 推出交互式 Transformer 讲解器，引发注意力机制教学讨论](https://poloclub.github.io/transformer-explainer/) ⭐️ 7.0/10

曾推出 CNN Explainer 和 Diffusion Explainer 的 Polo Club 团队发布了一个可在浏览器中交互操作的 Transformer 注意力机制可视化讲解器（poloclub.github.io/transformer-explainer），读者可以逐步手动操作分词、Q/K/V 计算、多头注意力和 token 采样等过程。该项目登上 Hacker News 首页，获得约 356 分和 55 条实质性评论。 Transformer 几乎是所有现代大语言模型的基础，但其内部机制很难通过静态图理解，因此由知名可视化团队制作的优质交互式讲解器能显著降低学生、工程师和新手的学习门槛。它所引发的讨论也表明，真正决定从业者能否理解注意力机制的，往往不只是架构本身，还有教学方式的呈现。 该讲解器属于纯教育性项目，并非研究成果；社区评论者指出了一些具体的教学呈现问题：Q/K/V 权重矩阵是注意力机制的核心可学习参数，却被放得太靠后；把温度参数描述为“安全与创造力之间的权衡”也被认为具有误导性。评论者还指出，每个注意力头都有自己独立的权重，尽管它们可以被合并为一次大型矩阵运算。

hackernews · aray07 · 9月21日 19:43 · [社区讨论](https://news.ycombinator.com/item?id=49792342)

**背景**: Transformer 是一种基于多头注意力机制的神经网络架构，输入文本先被切分为 token，每个 token 再通过查表转换为向量。注意力机制会计算查询（Q）、键（K）和值（V）矩阵，用缩放点积为每个查询与所有键打分，再用这些分数对值向量做加权求和；多头注意力则用多组不同的可学习投影并行执行这一过程。最终每个 token 都获得一个融入上下文的表示，正是这一机制取代了此前的循环和卷积序列模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Transformer_(deep_learning)">Transformer (deep learning) - Wikipedia</a></li>
<li><a href="https://www.geeksforgeeks.org/nlp/multi-head-attention-mechanism/">Multi-Head Attention Mechanism - GeeksforGeeks</a></li>
<li><a href="https://machinelearningmastery.com/the-transformer-attention-mechanism/">The Transformer Attention Mechanism - MachineLearningMastery.com Transformer (deep learning) - Wikipedia Attention in transformers, step-by-step | Deep ... | 3Blue1Brown Understanding Transformers and Attention Mechanisms: An ... Introduction to Transformers and Attention Mechanisms Transformers in Machine Learning - GeeksforGeeks</a></li>

</ul>
</details>

**社区讨论**: 整体反馈偏正面，有评论者称其为“我见过的最好的可视化之一”；最有分量的讨论认为 Q/K/V 权重应该更靠前呈现，并且应放在“Head N of M”模块内部，因为每个注意力头都有各自独立的权重。一个被广泛认同的洞见是：注意力头的行为就像一个稠密层，只不过它的权重是在推理时根据键和查询动态构造出来的，而这一点在教程中很少被强调；另有评论者反对在温度参数的解释中使用“安全”一词，因为温度为 0 的输出会呈现出一种不自然的“缺乏意外感”。还有人推荐 bbycroft.net/llm 作为补充资源，并追问为何其他架构方案最终未能流行起来。

**标签**: `#transformers`, `#machine-learning`, `#visualization`, `#education`, `#attention-mechanism`

---

<a id="item-13"></a>
## [AI 编码代理让 CI 成为瓶颈，Linear 重构其流水线](https://linear.app/now/ci-bottleneck-reworked) ⭐️ 7.0/10

Linear 发布了一篇工程深度文章，讲述在 AI 编码代理大量涌入代码与流水线任务、使持续集成（CI）成为主要瓶颈之后，公司如何重构其 CI 流水线。Linear 将工作负载从 GitHub Actions 迁移到具备更快 CPU、更高性能存储和更好缓存基础设施的第三方 runner 上，同时也对流水线本身进行了改造。 随着 AI 编码代理产生远超以往的提交、分支和拉取请求，限制软件交付速度的因素已从开发者敲代码的速度转移到 CI 的承载能力，这迫使工程团队重新思考 CI 基础设施与成本模型。任何采用代理式编码工具的工程组织都会受到影响，围绕性能竞争的 CI 厂商与 runner 服务商同样如此。 Linear 的文章指出，最直接的收益来自把同一条流水线放到更快的第三方机器上运行、而非继续使用 GitHub Actions，而不是重写流水线逻辑本身。围绕该话题的讨论也提出了隐忧：更快的流水线并不会自动带来更好的产品，而且即便 CI 提速，人工审查与产品层面的测试仍可能是真正的瓶颈。

hackernews · julian_digital · 9月21日 19:23 · [社区讨论](https://news.ycombinator.com/item?id=49792067)

**背景**: 持续集成（CI）是指开发者频繁地把代码变更合并到共享代码库中，并由自动化系统在每次提交或按计划构建和测试软件的做法；该术语由 Grady Booch 于 1991 年首次提出，后由 Martin Fowler 和极限编程运动推广开来。AI 编码代理（也称代理式编码）利用大语言模型辅助软件开发生命周期的各个环节，从代码生成到调试和测试，这会大幅增加流经 CI 系统的变更数量。Linear 是一家成立于 2019 年的旧金山项目管理软件公司，其客户包括 OpenAI、Salesforce 和 Cursor。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Continuous_integration">Continuous integration</a></li>
<li><a href="https://en.wikipedia.org/wiki/AI_coding_agent">AI coding agent</a></li>
<li><a href="https://en.wikipedia.org/wiki/Linear_(software)">Linear (software)</a></li>

</ul>
</details>

**社区讨论**: 这篇 HN 帖子下积累了 224 条评论，整体对“流水线更快就等于软件更好”持怀疑态度：有评论者质问，如果一切都变得如此之快，为什么新产品和新手机反而功能更少、完成度更低。也有人表示在 CI 费用上涨后自托管 runner 才是出路，认为真正的瓶颈是人工的产品测试而非 CI，并批评在大量由 LLM 生成的 PR 中存在“无用的测试雪崩”，这些测试往往只覆盖琐碎的内置行为。

**标签**: `#CI/CD`, `#AI coding agents`, `#developer productivity`, `#software engineering`, `#testing`

---

<a id="item-14"></a>
## [NASA 火星采样返回任务因成本超支而被取消](https://www.science.org/content/article/nasa-s-mars-sample-return-mission-dead) ⭐️ 7.0/10

《科学》杂志报道，NASA 的火星采样返回任务（MSR）在 2026 年已被实际取消，原因是成本膨胀至约 110 亿美元，且采样返回时间被推迟到 2040 年之后。这一决定使毅力号火星车已在火星上封存的样本管无法取回，也终结了 2022 年正式获批的 NASA 与 ESA 联合计划。 MSR 原本是行星科学的旗舰项目，也是首次由机器人将火星岩石、土壤和大气样本带回地球以确证火星是否曾经孕育生命。它的取消把火星采样返回的主导权让给了中国的天问三号任务——后者计划于 2028 年发射、约 2031 年带回样本，这标志着太空探索领域地缘格局的重大变化。 批评者指出，JPL 领导层围绕 Ariane 64 等传统运载火箭设计任务，而没有采用 Starship 或 New Glenn 等更新、运力更大且成本更低的方案，而且其预计带回的样本仅约 1.1 磅（约 0.5 公斤），而阿波罗登月任务带回了 842 磅月球岩石。返回的火星物质还引发逆向污染担忧，不过对地球生物圈的风险普遍被认为很低。

hackernews · Muhammad523 · 9月21日 19:14 · [社区讨论](https://news.ycombinator.com/item?id=49791939)

**背景**: 火星采样返回是一项由 NASA 与 ESA 合作、2022 年获批的多任务计划，目的是取回 NASA 毅力号火星车自 2021 年以来在火星上采集并封存的岩石、土壤和大气样本。取回这些样本需要另建一系列航天器：采样着陆器、把样本送入火星轨道的上升器，以及捕获并送回地球的返回轨道器。其科学价值在于，地球上的实验室仪器能比任何火星车车载传感器更彻底地分析火星物质，从而直接检验火星过去是否存在生命这一问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mars_sample-return_mission">Mars sample-return mission</a></li>
<li><a href="https://www.notebookcheck.net/China-aims-to-procure-Mars-samples-in-2031-while-NASA-s-mission-remains-in-limbo.1399349.0.html">China aims to procure Mars samples in 2031... - Notebookcheck News</a></li>
<li><a href="https://www.devx.com/daily-news/china-plans-tianwen-3-mars-launch-2028-return-martian-soil-2031/">China plans Mars sample return for 2028</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的评论者提供了内部视角：一位曾参与 ExoMars“罗莎琳德·富兰克林”号火星车的贡献者描述了发射多次推迟至 2028 年的经历，并表示希望采样返回任务将来能够重启。其他人则把 110 亿美元的成本和 2040 年的时间表归咎于 JPL 领导层，并批评其围绕传统火箭而非 Starship 或 New Glenn 进行设计；还有几位提到中国并行的天问三号计划，并质疑为何一篇 2026 年 1 月的文章现在才被翻出来讨论。

**标签**: `#space-exploration`, `#nasa`, `#mars-sample-return`, `#science-policy`, `#industry-news`

---

<a id="item-15"></a>
## [LWN 展望 Git 2.56 与 3.0，引发 SHA-256 迁移讨论](https://lwn.net/SubscriberLink/1094575/2385e98583715c2b/) ⭐️ 7.0/10

LWN 发布了一篇前瞻性综述，介绍了 Git 2.56 以及未来的 Git 3.0 中即将到来的变化，包括新命令、对历史遗留默认行为的清理，以及进展缓慢的 SHA-256 哈希迁移。这篇文章在 Hacker News 上获得了 106 分、43 条评论，讨论集中在各大托管平台对 SHA-256 的支持、Git 的一些不合理默认值，以及更换哈希算法对现有仓库的冲击。 Git 几乎是所有现代软件开发的基础设施，因此它的默认行为和对象格式一旦变化，就会波及每一位开发者、每条 CI 流水线和每个代码托管服务。Git 3.0 正是维护者终于可以实施那些被推迟多年的破坏性兼容修改的里程碑，所以这场路线图讨论的意义远超 Git 自身的贡献者社区。 根据 Git 官方设计文档，SHA-256 迁移被设计为可以逐个仓库进行，且不需要其他相关方采取行动，SHA-256 仓库还能与 SHA-1 仓库互操作。讨论中还提到了一个拟议中的便利命令 `git add --resolved`，以及长期以来用户对 Git 默认配置不合理的抱怨——Git 3.0 或许可以利用其允许破坏性变更的窗口来解决这些问题。

hackernews · Lobsters · 9月21日 23:16 · [社区讨论](https://news.ycombinator.com/item?id=49794736)

**背景**: Git 是一种分布式版本控制系统，其中每个文件、目录和提交都由其内容的密码学哈希值来标识。自 2005 年诞生以来它一直使用 SHA-1，但针对 SHA-1 的实际碰撞攻击（2017 年被公开演示）使得更强算法成为必要，因此该项目一直在推进向 SHA-256 的迁移。由于哈希值遍布提交对象、打包文件和引用之中，这类变更很难在不破坏兼容性的前提下推行，所以它被分多个版本逐步推进，而不是一次性发布。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://git-scm.com/docs/hash-function-transition">hash-function-transition Documentation - Git</a></li>
<li><a href="https://www.kernel.org/pub/software/scm/git/docs/technical/hash-function-transition.html">Git hash function transition - The Linux Kernel Archives</a></li>

</ul>
</details>

**社区讨论**: 评论者对托管平台普遍持怀疑态度：有人指出 Atlassian 的一个尚未关闭的 JIRA 工单显示 Bitbucket 仍不支持 SHA-256，还有人批评 GitHub 拖沓，只在边缘做些小改动。也有人对拟议的 `git add --resolved` 表示欢迎，呼吁 Git 3.0 修复“所有糟糕的默认设置”，并提出担忧：从 SHA-1 切换到 SHA-256 是否需要强制推送并重写全部历史，从而可能带来安全隐患。

**标签**: `#git`, `#version-control`, `#sha256`, `#open-source`, `#software-engineering`

---

<a id="item-16"></a>
## [陶哲轩宣布成立数学与人工智能咨询小组](https://terrytao.wordpress.com/2026/09/21/advisory-group-on-mathematics-and-artificial-intelligence/) ⭐️ 7.0/10

陶哲轩（Terence Tao）在其博客上宣布成立“数学与人工智能咨询小组”，目的是就人工智能公司如何与数学研究及数学界互动提供建议。小组当前的一项具体任务，是就 OpenAI 如何协调发布其内部模型所产生的大量重要数学成果提供咨询。 该小组表明数学家正试图主动为 AI 驱动的数学发现制定规范，而不是在成果公布后再被动回应；同时它把一群声望很高的学者与一家动机正受到公开质疑的商业 AI 实验室放在了一起。这一尝试的结果，可能会影响其他研究领域是否也建立类似的与 AI 公司的咨询关系。 该小组的定位明确是“咨询性”的，因此质疑者指出它无法强迫 OpenAI 改变其行事方式；目前讨论中最具体的交付形式是协调发布问题陈述、解答以及相应的 Lean 证明。Burt Totaro 等批评者认为 OpenAI 是在借用数学家的公信力来抵消负面舆情，另一些人则认为此举不过是学术界的“守门”，除了可验证的证明之外并无额外价值。

hackernews · digital55 · 9月21日 19:17 · [社区讨论](https://news.ycombinator.com/item?id=49791997)

**背景**: 陶哲轩是加州大学洛杉矶分校的数学家、菲尔兹奖得主，他的博客在数学界被广泛阅读，常常成为反思科研实践如何变化的场所。Lean 是一种交互式定理证明器，允许数学家以计算机可机械验证的形式化语言书写证明，这也是评论者把 Lean 证明视为 AI 生成数学成果的“硬证据”的原因。此次公告正值多家 AI 实验室宣称在数学上取得重大进展之际，围绕这类宣称应如何被验证与发布，争论进一步升温。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://terrytao.wordpress.com/2026/09/21/advisory-group-on-mathematics-and-artificial-intelligence/">Announcing the Advisory Group on Mathematics and Artificial Intelligence</a></li>
<li><a href="https://en.wikipedia.org/wiki/Terence_Tao">Terence Tao - Wikipedia</a></li>
<li><a href="https://www.simonsfoundation.org/2026/08/13/fields-medalist-terence-tao-on-artificial-intelligence-and-why-we-do-math/">Watch: Fields Medalist Terence Tao on Artificial Intelligence and Why ...</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍赞赏数学界面对 AI“热潮”时冷静、理性且富有同理心的反应，并将其与其他领域的表现作对比。对于小组本身，讨论则出现分歧：被引用的 Burt Totaro 观点——OpenAI 在利用数学家的信任与声望——获得不少支持，也有人认为这不过是学术界的守门行为，只要直接公布问题陈述、解答和 Lean 证明就足够了。还有一条调侃陶哲轩名气的玩笑缓和了气氛。

**标签**: `#AI`, `#mathematics`, `#OpenAI`, `#research-culture`, `#academia`

---

<a id="item-17"></a>
## [HERMES 开源短波电台实现远距离数字语音与数据传输](https://spectrum.ieee.org/hermes-shortwave-radio-digital-data) ⭐️ 7.0/10

HERMES 是由 Rhizomatica 组织推出的开源短波（HF）无线电系统，可在极远距离上提供数字语音和数据通信。它并非单一设备，而是被描述为一套软件栈——由多个程序协同工作，以便通过短波发送数据。 该项目面向全球南方地区提供具有韧性、对基础设施依赖极低的通信手段，因为那里的传统电信网络往往稀缺或不可靠。它已经过真实紧急情况的验证，据称成功处理了一次 Pan Pan 紧急呼叫，表明开源短波数据链路在生死攸关的场景中确实能发挥作用。 HERMES 通过短波（HF）频段传输，并包含签名与哈希等功能，但在许多国家，对消息内容进行加密在业余无线电中被法律限制。由于短波信号可借助电离层反射实现越地平线传播，该系统能达到远超常规 VHF/UHF 或 Wi-Fi 链路的距离。

hackernews · SamuraiLion · 9月21日 16:14 · [社区讨论](https://news.ycombinator.com/item?id=49789228)

**背景**: 短波即 HF（高频）无线电，使用 3–30 MHz 频段，信号可经电离层反射传播数千公里而无需任何地面基础设施——这一特性长期被海事、航空和业余无线电操作者所用。Rhizomatica 是一家非营利组织，以在墨西哥瓦哈卡等欠发达地区建设社区自营电信网络而闻名。HERMES 属于 WinLink 等无线电消息工具一脉，后者在业余电台上提供类似电子邮件的服务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://spectrum.ieee.org/hermes-shortwave-radio-digital-data">Shortwave Radio Gets a Secure Data Upgrade With HERMES - IEEE ...</a></li>
<li><a href="https://hermes.radio/">hermes.radio</a></li>
<li><a href="https://www.rhizomatica.org/">rhizomatica</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍称赞该项目是向最需要的人群提供韧性通信手段的有前途的方式，并提到它在 Pan Pan 紧急呼叫中的成功应用。主要担忧集中在监管层面：在美国进行发射需要执照，且业余频段通常不允许加密；也有人指出签名与哈希仍然合法。多位读者将 HERMES 与 WinLink、Garmin/Iridium、Zoleo 以及基于 Starlink 的短信等商业替代方案进行比较，用于海上或生死攸关的场景。

**标签**: `#radio`, `#open-source`, `#emergency-communications`, `#networking`, `#telecommunications-policy`

---

<a id="item-18"></a>
## [苹果 Copland D11E4 通过 DingusPPC 模拟在浏览器中启动](https://www.pagetable.com/300) ⭐️ 7.0/10

Michael Steil 在 pagetable.com 上发布了一个页面，可以直接在网页浏览器中启动苹果夭折的 Copland 操作系统——具体是最后一个版本 D11E4——底层运行的是经过改进的 DingusPPC 模拟器。文章指出，Copland 在真实硬件上极难运行，此前也从未被成功模拟过。 Copland 是苹果从未正式发布的下一代 Mac OS，在此之前想要体验它只能依赖稀少且不稳定的真实硬件；如今浏览器版本让任何人都能即时访问这一具有历史意义的被取消系统。这也体现了浏览器端（WebAssembly 风格）模拟技术的成熟，因为一整套经典 Mac OS 现在可以在一个标签页里运行。 D11E4 是 Copland 的最后一个版本，该演示依赖的是对 PowerPC 时代 Mac 模拟器 DingusPPC 的改进，而非任何新的 Copland 代码。曾在同期硬件上运行过 Copland 的评论者回忆说它极不稳定、频繁崩溃，因此模拟体验更像是历史猎奇，而非可用的系统。

hackernews · luu · 9月21日 18:15 · [社区讨论](https://news.ycombinator.com/item?id=49791125)

**背景**: Copland 是苹果在 1994 至 1996 年间开发的系统，原本作为老旧的 System 7 的现代化继任者，计划以 System 8（后来改名为 Mac OS 8）的名义发布，承诺带来内存保护、抢占式多任务等新特性，同时保持对现有 Mac 应用程序的兼容。该项目饱受功能蔓延和进度延误之苦，最终于 1996 年 8 月被取消；苹果转而于 1997 年收购 NeXT，NeXTSTEP 成为 2001 年 Mac OS X 的基础。在此过渡期间，苹果先后发布了更偏传统架构的 Mac OS 8（1997 年）和 Mac OS 9（1999 年）。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.pagetable.com/300">Apple Copland D 11 E 4 booting in your Browser – pagetable.com</a></li>
<li><a href="https://en.wikipedia.org/wiki/Apple_Copland_(operating_system)">Apple Copland (operating system)</a></li>

</ul>
</details>

**社区讨论**: 整体情绪多是终于能亲手体验 Copland 的怀旧喜悦，有评论者称这是自己从未想过能实现的体验。一位曾在同期硬件上运行过 Copland 的评论者用亲身经历泼了冷水，说它不稳定且经常崩溃，认为砍掉它是正确的决定，并推测如果 Copland 成功，苹果可能就不会收购 NeXT，也就不会有 OS X。其他人则惊叹于能在浏览器中运行整台电脑，惋惜 Project Star Trek（苹果更早的 Intel 移植项目）永远无法见到，并指出 UI 的延续性——从沿用至今的单色手表指针光标，到滚动文本区域在拖动滚动条时不重绘文字这类当年留下的取舍。

**标签**: `#emulation`, `#retro-computing`, `#apple`, `#computing-history`, `#webassembly`

---

<a id="item-19"></a>
## [恶意 npm 包 mathmain 用触发矩阵隐藏加密加载器](https://safedep.io/mathmain-encrypted-loader/) ⭐️ 7.0/10

SafeDep 发布了一篇安全分析，剖析了伪装成数学库的恶意 npm 包 mathmain，它内置了一个使用 AES-256-GCM 加密的第二阶段加载器，只有当 lusolve() 函数接收到某个特定的 3x3 矩阵时才会解密。该包及其两个同族包在被发现一个未被调用的函数之前， reportedly 在一周内累计获得了 310 万次下载。 这是一个真实且有据可查的软件供应链攻击案例，攻击者滥用了被广泛信任的 npm 生态和巧妙的混淆手法来绕过自动化扫描器。它凸显了攻击者如何利用看似正常的包和条件触发机制来投放远程访问载荷，这对每一位安装依赖的开发者都构成日益增长的风险。 加密载荷由一个'密码'把关，本质上就是传入数学求解器 lusolve() 例程的一个精确的 3x3 矩阵，因此通用的基于特征码的扫描器根本无法猜中或触发它。调查人员通过发现一个未被调用的函数定位到触发器，JFrog 随后破解了加密密钥；但还原出的第二阶段载荷实际上完全失效，然而该包据报道至今仍挂在 npm 上，没有任何警告提示。

hackernews · abhisek · 9月21日 18:33 · [社区讨论](https://news.ycombinator.com/item?id=49791378)

**背景**: 加载器(loader)是一类专门用于投递额外载荷(如窃密木马或远程访问木马)的恶意软件，而加密器(crypter)或加密加载器则负责把载荷隐藏起来以逃避检测。npm 是 JavaScript/Node.js 的默认包注册中心，任何发布其上的包都可能被成千上万的下游项目引入，因此成为供应链攻击的高价值目标。CommonJS 是较旧的 Node.js 模块格式，它允许动态的 require() 调用，这类调用很难被静态地 grep 或分析，攻击者常借此来掩盖恶意逻辑。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://safedep.io/mathmain-encrypted-loader/">Why Does an npm Math Library Need an Encrypted Loader?</a></li>
<li><a href="https://umesh-malik.com/blog/npm-encrypted-loader-malware-detection">How to Detect npm Encrypted Loader Malware: 3.1M Downloads</a></li>
<li><a href="https://www.npmjs.com/package/mathmain?activeTab=dependencies">mathmain - npm</a></li>

</ul>
</details>

**社区讨论**: 评论者指出，JFrog 破解密码的功劳不容忽视，正是它才让后续分析成为可能；也有读者质疑为何要用某个特定的 3x3 矩阵作为攻击触发器，猜测其目的是针对某类数值分析场景。还有人强调第二阶段载荷其实完全失效，认为 CommonJS 模块格式早该被淘汰，因为 ESM 的动态 import 更容易检测和分析；同时有人发问，执法部门是否会把这些仍挂在 npm 上的后门当作犯罪来追究。

**标签**: `#supply-chain-security`, `#npm`, `#malware-analysis`, `#javascript`, `#cybersecurity`

---

<a id="item-20"></a>
## [TypeSafe AI 发布 Jev：输出概率而非文本的决策模型](https://simonwillison.net/2026/Sep/21/jev/) ⭐️ 7.0/10

成立于 2024 年、在隐身模式下研发两年的旧金山公司 TypeSafe AI 发布了 Jev，这是其称之为“System One 模型”（即决策模型）的新模型类别的首个成员。Jev 不生成文本，而是接收文本或半结构化的“状态”以及一个或多个问题，返回带类型的概率化答案：0 到 1 之间的伯努利式是/否置信度、在给定选项集合上的概率分布，或沿指定数值区间的评分。 Jev 把大语言模型重新定义为分类与决策引擎，而非文本生成器，这可能使垃圾邮件识别、打标签、优先级排序、排名和搜索结果重排等大规模任务变得极其便宜和快速。其每百万输入 token 仅 0.042 美元的定价（输出免费）甚至低于 OpenAI GPT-5 Nano 的每百万 0.05 美元，这暗示面向决策的推理可能成为 AI 技术栈中一个独立且高度商品化的层次。 Jev 支持三类问题：Noul 问题（即伯努利问题，其 CEO 已在 Hacker News 上确认该词源自伯努利分布）、返回置信度加全部选项概率分布的选择题，以及在一组带描述的数值等级上给出浮点评分的打分题。单个 state 可以携带尽可能多地塞进上下文窗口的问题，且问题并行评估，因此增加问题几乎不额外增加耗时；TypeSafe 声称在分类任务上推理速度约为同类大模型的 200 倍、成本低约 400 倍。

rss · Simon Willison · 9月21日 23:09

**背景**: 传统大语言模型按输入和输出 token 计费，其中输出 token 通常单价高得多，因为模型需要逐 token 生成文本；Jev 从不生成文本，从而绕开了这一成本，因此输出可以免费。其“System One”命名借鉴了心理学家 Daniel Kahneman 对快速直觉的“系统 1”思维与缓慢审慎的“系统 2”推理的区分。Simon Willison 认为“决策模型”这一称呼更贴切，因为该模型本质上是一次前沿智能的函数调用：输入非结构化状态，输出带类型的概率化决策。他还给出了一个实用场景：先用 BM25 这类经典词法检索排序算法取出 100 个候选，再用 Jev 对它们相对于原始查询的相关性进行重排打分。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Jev_(AI_model)">Jev (AI model) - Wikipedia</a></li>
<li><a href="https://typesafe.ai/blog/introducing-system-one-models-and-jev">Introducing System One Models & Jev - TypeSafe AI Blog</a></li>
<li><a href="https://www.langchain.com/blog/building-a-harness-with-jev">What Is Jev? A Guide to TypeSafe AI's System One Model - LangChain</a></li>

</ul>
</details>

**标签**: `#LLM`, `#decision models`, `#AI`, `#TypeSafe AI`, `#probabilistic models`

---

<a id="item-21"></a>
## [OpenAI 呼吁建立全球共享的人工智能安全标准](https://openai.com/index/building-standards-next-phase-ai) ⭐️ 7.0/10

OpenAI 发布了一篇题为《为人工智能的下一阶段制定标准》的立场文章，勾勒出通向全球共享人工智能标准的路径，并呼吁通过协调一致的评估、报告与治理机制来提升安全性。 作为最大的前沿模型开发者之一，OpenAI 公开推动协调一致的标准，是一个重要的行业信号，可能影响各国政府和监管机构制定人工智能安全规则的方式，也会给其他竞争实验室带来对齐或回应的压力。 该内容是政策层面的表态，而非技术发布，因此尚未明确具体机制，例如由谁负责评估、适用何种报告门槛、哪些司法辖区参与等；这一操作细节的缺失，很可能是观察者关注的主要空白。

rss · OpenAI Blog · 9月21日 10:00

**背景**: 过去几年，前沿人工智能治理已从抽象讨论走向具体立法，各国人工智能安全研究所、《欧盟人工智能法案》以及一系列国际峰会，都在尝试界定强大模型应如何被测试和报告。第三方评估、透明度报告和事件披露已成为这些努力的核心构件。核心难点在于协调：只有当主要实验室和主要市场采用兼容规则时，标准才能真正奏效，否则开发者将面对彼此不兼容的零散要求。OpenAI 这篇文章意在把自身定位为支持这种趋同，而非抗拒它。

**标签**: `#AI governance`, `#AI safety`, `#standards`, `#policy`, `#OpenAI`

---

<a id="item-22"></a>
## [央行人士主张：数字货币的未来要靠公共货币而非私人货币](https://www.economist.com/by-invitation/2026/09/21/the-future-of-digital-finance-rests-on-public-money-not-private) ⭐️ 7.0/10

2026 年 9 月 21 日，《经济学人》刊发的一篇特邀评论中，资深央行官员皮耶罗·奇波洛内（Piero Cipollone）主张，央行必须继续充当数字金融的锚，以维护公众信任并确保各类支付系统之间的互操作性。他反驳了仅靠私人发行的数字货币就能支撑未来货币体系基础的观点。 这篇文章发表之际，全球正围绕“由谁发行和控制数字货币”展开政策博弈：各国央行在推进 CBDC，而稳定币发行方和商业银行也在扩张自己的代币化支付通道。如果央行“公共货币必须居于核心”的论点占据上风，将直接影响整个支付与金融科技行业的监管规则、竞争格局和消费者获取服务的方式。 这是一篇来自央行内部人士的政策评论，而非技术设计文档，因此它围绕信任与互操作性搭建论点，并未深入讨论零售型与批发型 CBDC、持有上限、隐私模型等具体架构选择。同时，它也带有机构自身立场的色彩——作者所在机构本身就在研发公共数字货币，因此对私人稳定币发行方竞争性主张的回应并不对等。

rss · The Economist · 9月21日 09:34

**背景**: 央行数字货币（CBDC）是由央行直接发行的官方货币的数字形态，属于央行的负债而非私人公司的负债，这一点与比特币等加密货币或私人发行的稳定币不同。此处的“公共货币”指可被公众广泛使用的央行货币，与实物现金和商业银行准备金并列。互操作性指的是不同系统和支付服务商之间能够顺畅通信与结算的能力；若缺少共同的公共锚，相互竞争的私人网络可能会割裂成一个个封闭孤岛。这场争论之所以重要，是因为稳定币和代币化存款正快速增长，央行担心自己会失去作为最终结算层（settlement layer）的地位。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Central_bank_digital_currency">Central bank digital currency - Wikipedia</a></li>
<li><a href="https://www.federalreserve.gov/faqs/what-is-a-central-bank-digital-currency.htm">The Fed - What is a Central Bank Digital Currency?</a></li>
<li><a href="https://www.bcbgroup.com/insights/interoperability-a-prerequisite-for-financial-convergence/">Interoperability: A Prerequisite for Financial Convergence</a></li>

</ul>
</details>

**标签**: `#digital finance`, `#central banking`, `#CBDC`, `#public money`, `#interoperability`

---

<a id="item-23"></a>
## [书评：并行编程难吗？如果难，又能怎么办？](https://ahelwer.ca/post/2026-09-21-concurrency-textbook/) ⭐️ 7.0/10

技术博主 ahelwer 发表了一篇书评，评述 Paul McKenney 的经典并发教材《Is Parallel Programming Hard, And, If So, What Can You Do About It?》，讨论书中提供的洞见以及对实际工程实践的启示。文章还附上了 Lobsters 上关于该书的讨论帖链接。 McKenney 的这本书是为数不多免费公开、且深入底层的并发参考书之一，因此一篇认真的书评能帮助从业者判断它是否比替代资料更值得投入时间。在这样一个大量优质知识散落在内核邮件列表和艰深学术论文中、而非传统教材里的领域，这类书评也起到了筛选和导读的作用。 这本书通常以其项目名 “perfbook” 为人所知，可免费下载，并且是在公开环境下撰写和维护的。其内容范围一般涵盖同步原语、内存屏障与内存模型、加锁与无锁算法，以及压力测试、形式化验证等正确性验证手段。任何书评都必然反映作者个人的关注重点，因此读者应把这些评价视为个人观点，而非对该资料价值的最终定论。

rss · Lobsters · 9月21日 14:28

**背景**: Paul E. McKenney 是一位资深的 Linux 内核开发者，最著名的成就是 Read-Copy-Update（RCU）——一种在内核中被广泛使用的同步机制，他的这本书正是源于这种深入内核的并发实践经验。这个问题之所以困难，是因为现代多核硬件和编译器会对内存操作进行重排序，使得来自单线程代码的直觉常常导致难以察觉的错误程序。因此，书中花了大量篇幅讨论内存序、原子操作，以及推理和测试并发代码的各种方法。该书全文免费发布，这也使它成为系统程序员、内核开发者以及准备并发相关面试或工作的人常用的参考书。

**标签**: `#parallel programming`, `#concurrency`, `#book review`, `#software engineering`, `#computer science`

---

<a id="item-24"></a>
## [用同一套代码库同时构建 GBA 与 PC 游戏](https://mattgreer.dev/blog/making-a-game-for-gba-and-pc/) ⭐️ 7.0/10

开发者 Matt Greer 发布了一篇博客，讲解他如何用同一套共享代码库构建出既能在 Game Boy Advance 上运行、也能在 PC 上运行的游戏。文章重点介绍了让同一份源码树同时编译到 2001 年的掌机平台和现代桌面平台上所需的工程技巧。 在资源极度受限的复古主机与现代 PC 之间做跨平台开发，是对代码可移植性异常严苛的考验，因此这篇文章为自制软件、嵌入式和复古游戏开发者提供了可复用的经验。它也反映出 GBA 自制游戏社区依然活跃——爱好者至今仍在发布可以烧录成卡带的新游戏。 GBA 与 PC 的目标环境差异极大：它没有操作系统，快速 RAM 仅有几十 KB、显存约 96KB，搭载约 16.78 MHz 的 ARM7TDMI 处理器，并且没有浮点运算单元。由于本次未提供文章正文，Greer 具体使用的抽象层、工具链与构建配置无法在此独立核实。

rss · Lobsters · 9月21日 16:02

**背景**: Game Boy Advance 是任天堂 2001 年推出的掌机，基于 32 位 ARM7TDMI CPU，屏幕分辨率为 240x192，并且没有可供依赖的操作系统。自制游戏开发者通常使用 C 或 C++ 编写 GBA 游戏，配合 devkitARM 这类工具链以及 libgba、libtonc 等库，最终产出 .gba ROM 镜像。因此，若要和 PC 版共用同一套代码库，就必须把所有平台相关的工作——渲染、输入、音频、内存管理与时序——都隔离在抽象层之后，因为这两个目标平台在几乎所有硬件细节上都不相同。

**标签**: `#game development`, `#GBA`, `#cross-platform`, `#retro computing`, `#software engineering`

---

<a id="item-25"></a>
## [阿里巴巴计划打造 5 万亿至 10 万亿参数 AI 模型并发布新芯片](https://www.reddit.com/r/LocalLLaMA/comments/1wmyh9z/alibaba_plans_ai_model_with_5_trillion_to_10/) ⭐️ 7.0/10

据 r/LocalLLaMA 社区的一则投稿，阿里巴巴 reportedly 计划打造一个参数规模在 5 万亿到 10 万亿之间的大语言模型，并发布了一款新的 AI 芯片。另有报道指出，这款芯片是新一代 Zhenwu（镇武）处理器，性能约为上一代的三倍。 如果这一计划落地，5 万亿到 10 万亿参数的模型将成为史上规模最大的模型之一，使阿里巴巴跻身美国头部前沿实验室的同一梯队，并进一步加剧全球模型规模的竞赛。将这一目标与自研芯片结合，也凸显出在美国出口管制持续限制获取英伟达尖端硬件背景下，中国推动 AI 算力自主的努力。 该投稿本身几乎没有提供技术细节——没有说明架构（例如是否为混合专家模型）、训练数据、算力预算或时间表，而单看参数量并不能说明实际能力。芯片方面的信息来自其他报道：新款 Zhenwu 芯片声称性能达到上一代的三倍，且阿里巴巴计划到 2032 年将全球数据中心容量扩展到 20 吉瓦以上。

reddit · r/LocalLLaMA · /u/tengo_harambe · 9月22日 03:35

**背景**: 模型的参数量大致相当于其神经网络中可学习权重的数量，而神经缩放定律（scaling law）描述了当参数、训练数据和算力增加时性能通常如何提升。现代混合专家（MoE）架构可以拥有数万亿的总参数，但每个 token 只激活其中一小部分，从而把推理成本控制在可接受范围内。阿里巴巴的芯片由其芯片子公司平头哥（T-Head）设计，Zhenwu 系列用于支撑自建数据中心，这是在中国企业加速开发英伟达硬件国产替代方案的背景下进行的。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.alibabagroup.com/en-US/document-1994119844504535040">Alibaba Unveils New AI Chip, Flagship Model, and Rebuilt Cloud Stack AI for Agentic Era-Alibaba Group</a></li>
<li><a href="https://www.cnbc.com/2026/09/22/alibaba-ai-alibabacloud-zhenwu-v900-.html">Alibaba shares jump as new AI chip, data center buildout plans unveiled</a></li>
<li><a href="https://en.wikipedia.org/wiki/AI_scaling_law">AI scaling law</a></li>

</ul>
</details>

**标签**: `#Alibaba`, `#large language models`, `#AI chips`, `#scaling`, `#hardware`

---

<a id="item-26"></a>
## [小米将 MiMo-V2.6 蒸馏进 Qwen 9B 模型](https://www.reddit.com/r/LocalLLaMA/comments/1wmtjqu/mimov26_distilled_themselves_into_qwen_9b/) ⭐️ 7.0/10

一个名为 MiMo-V2.6-Distill-Qwen-9B 的模型已在 Hugging Face 的 XiaomiMiMo 组织下发布，意味着小米的旗舰模型 MiMo-V2.6 被蒸馏进了一个基于 Qwen 架构的 9B 参数模型中。该消息由 r/LocalLLaMA 上的一则帖子曝光，帖子只包含 Hugging Face 链接，没有任何配套的技术说明。 如果蒸馏效果理想，本地 LLM 社区就获得了一个约 9B 的模型，它继承了规模大得多的前沿 MiMo-V2.6 检查点的能力，同时又能在消费级 GPU 上运行。这也表明小米正积极争取开放权重生态，不只是发布旗舰检查点，还推出更小、更易部署的衍生模型。 模型名称明确把 MiMo-V2.6 作为教师模型，与 Qwen 9B 学生模型配对，而后者的参数量级与支持原生 262,144 token 上下文的稠密模型 Qwen3.5-9B 相同。帖子中没有提供蒸馏数据集、教师检查点版本（Pro 还是 Flash）、评测分数或许可条款等信息，因此该学生模型的实际质量尚待验证。

reddit · r/LocalLLaMA · /u/Beamsters · 9月21日 23:50

**背景**: 知识蒸馏是把大型“教师”模型的行为迁移到较小的“学生”模型中的技术，通常做法是让学生模型在教师模型生成的输出上训练，从而以很低的算力代价保留推理和指令遵循能力。小米的 MiMo 团队一直在发布 MiMo-V2.6 系列，官方称其通过规模化强化学习打造的“全模态”模型，在编码、电脑操作和 3D 推理上更强，并有 Pro 与 Flash 两个版本。Qwen 是阿里巴巴的开放权重模型家族，其 9B 稠密档位因能轻松放进单块高端消费级 GPU 而成为本地推理的热门尺寸。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/XiaomiMiMo/MiMo-V2.6-Pro-RL">XiaomiMiMo/MiMo-V2.6-Pro-RL - Hugging Face</a></li>
<li><a href="https://labs.adaline.ai/p/llm-distillation-explained">LLM Distillation Explained - by Nilesh Barla - Adaline Labs</a></li>
<li><a href="https://huggingface.co/Qwen/Qwen3.5-9B">Qwen/Qwen3.5-9B · Hugging Face</a></li>

</ul>
</details>

**标签**: `#LLM`, `#Model Distillation`, `#Qwen`, `#MiMo`, `#Local AI`

---

<a id="item-27"></a>
## [Yandex 发布 AliceAI-Foundation-80B-A3B-Base，一款自研架构的俄罗斯 MoE 基础模型](https://www.reddit.com/r/LocalLLaMA/comments/1wmmnrt/yandexaliceaifoundation80ba3bbase/) ⭐️ 7.0/10

Yandex 在 Hugging Face 上发布了 AliceAI-Foundation-80B-A3B-Base，这是一个总参数 80B、激活参数 3B 的混合专家（MoE）基础模型，采用了完全自研的架构，而不是对 Qwen3 或其他已有模型系列的微调。该版本仅为预训练基础模型，尚未经过后训练（post-training），目前也还没有 llama.cpp 支持。 这为本地大模型生态又增添了一个公开释放的大规模 MoE 基础模型，而且来自美国和中国主流模型厂商之外的实验室，直接对标 Qwen 35B 与 DeepSeek V4 Flash。与对现有开源模型做微调不同，它是真正自研的架构，这为研究人员和微调者提供了一个架构上独立的新基座用于实验。 该模型总参数约 80B，但每个 token 仅激活 3B，属于稀疏 MoE 设计，即每次前向计算只调用一小部分专家网络，因而实际推理算力远低于参数规模给人的印象。由于它是基础检查点，缺少指令微调与对齐，同时缺少 llama.cpp/GGUF 支持，目前在消费级硬件上便捷地本地推理仍受限。

reddit · r/LocalLLaMA · /u/Iwaku_Real · 9月21日 19:24

**背景**: 混合专家（MoE）是一种把网络拆分为多个“专家”子网络、并为每个输入 token 只路由到其中少数几个的架构，因此模型可以拥有非常大的总参数量，而单 token 的计算量仍然可控。“基础模型”（base model）是大规模文本预训练后的原始产物：它能续写和补全文本，但尚未经过后训练——即监督微调、偏好对齐或面向推理的强化学习——因此还不能直接当作助手使用。llama.cpp 是广泛使用的推理引擎，通过 GGUF 量化格式在本地运行模型；是否获得它的支持，往往决定了某个新架构能否真正跑在笔记本和台式机上。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mixture_of_experts">Mixture of experts - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Post-training_of_large_language_models">Post-training of large language models</a></li>
<li><a href="https://developer.nvidia.com/blog/applying-mixture-of-experts-in-llm-architectures/">Applying Mixture of Experts in LLM Architectures | NVIDIA Technical Blog</a></li>

</ul>
</details>

**标签**: `#LLM`, `#Yandex`, `#Mixture-of-Experts`, `#Custom Architecture`, `#LocalLLaMA`

---

<a id="item-28"></a>
## [SupraLabs 发布 Supra2-IMG：100M 参数的文本生成图像 DiT 模型，训练不到 10 小时](https://www.reddit.com/r/LocalLLaMA/comments/1wmftr3/massive_release_supra2img_a_tiny_100m_texttoimage/) ⭐️ 7.0/10

SupraLabs 发布了 Supra2-IMG，这是一个 100M 参数的扩散 Transformer（DiT）文本生成图像模型，完全从零开始训练，仅在 Runpod 上租用的一块 H100 GPU 上耗时不到 10 小时完成。该模型可生成其团队称为业界领先（SOTA）水平的 256x256 图像，GPU 推理约 2 秒、CPU 推理约 20 秒，权重与推理脚本已在 Hugging Face 上公开。 它表明如今只需一块租用的 GPU、数小时训练，就能从零得到一个可用的文本生成图像模型，并能在普通硬件上本地运行，大幅降低了个人爱好者和小团队的入门门槛。这契合了扩散模型不断小型化的趋势，即用分辨率和规模换取可及性，与大型实验室动辄数十亿参数的系统形成对比。 公布的样例图像使用固定参数生成（seed 0、50 步采样、classifier-free guidance 系数 3.0），作者声称这些样例并未经过挑选。主要局限在于输出分辨率仅为 256x256，且此次发布以推理脚本和权重为主，并未提供完整的可复现训练流程或 FID 等基准指标。

reddit · r/LocalLLaMA · /u/LH-Tech_AI · 9月21日 15:21

**背景**: 扩散 Transformer（DiT）是 Peebles 和 Xie 于 2022 年提出的一类图像生成架构，它用作用于潜空间图像块的纯 Transformer 取代了扩散模型传统的 U-Net 主干，从而提升了可扩展性。文本生成图像的扩散模型通过在多个去噪步骤中把随机噪声逐步转化为图像，并由文本提示和 classifier-free guidance 引导——后者是一种用图像多样性换取更强提示词遵循度的技术。SupraLabs 是一个不定期发布小型开源模型的小团队，而 Runpod 是一个按小时出租 GPU 用于 AI 训练与推理的云平台。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2212.09748">[2212.09748] Scalable Diffusion Models with Transformers</a></li>
<li><a href="https://github.com/facebookresearch/DiT">Scalable Diffusion Models with Transformers (DiT) - GitHub DiT · Hugging Face Scalable Diffusion Models with Transformers Diffusion Transformers Explained: The Beginner’s Guide [2510.11690] Diffusion Transformers with Representation ...</a></li>
<li><a href="https://grokipedia.com/page/runpod">Runpod</a></li>

</ul>
</details>

**标签**: `#text-to-image`, `#diffusion-models`, `#local-ai`, `#open-source`, `#model-release`

---