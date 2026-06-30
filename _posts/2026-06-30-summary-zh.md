---
layout: default
title: "Horizon Summary: 2026-06-30 (ZH)"
date: 2026-06-30
lang: zh
---

> 从 72 条内容中筛选出 26 条重要资讯。

---

1. [vLLM v0.24.0 新增 MiniMax-M3 支持，优化 DeepSeek-V4](#item-1) ⭐️ 9.0/10
2. [最高法院裁定地理围栏搜查令需宪法保护](#item-2) ⭐️ 9.0/10
3. [CVE-2026-46817：Oracle EBS 遭积极攻击](#item-3) ⭐️ 9.0/10
4. [Longinus 漏洞一举突破 Chrome 渲染器和 V8 沙箱](#item-4) ⭐️ 9.0/10
5. [IPv6 分片漏洞实现可靠的 Linux 容器逃逸](#item-5) ⭐️ 9.0/10
6. [.self：一个支持自托管的新顶级域名，提供免费子域名](#item-6) ⭐️ 8.0/10
7. [火箭实验室历史性收购铱星公司](#item-7) ⭐️ 8.0/10
8. [Ornith-1.0：自我改进的开源代理编程模型](#item-8) ⭐️ 8.0/10
9. [韩国宣布 1 万亿美元投资内存芯片和人形机器人](#item-9) ⭐️ 8.0/10
10. [深入解析 CUDA 内核启动内部机制](#item-10) ⭐️ 8.0/10
11. [人工智能热潮促使海底电缆绕开中国](#item-11) ⭐️ 8.0/10
12. [AT-URI 语法缺陷曝光](#item-12) ⭐️ 8.0/10
13. [DRM GEM change_handle 释放后重用导致提权至 root](#item-13) ⭐️ 8.0/10
14. [ACM 文章揭穿形式化验证迷思](#item-14) ⭐️ 8.0/10
15. [Qwen 3.6 27B：本地开发的甜蜜点？](#item-15) ⭐️ 7.0/10
16. [提出基于 SSH 的原生图形化 Shell 方案](#item-16) ⭐️ 7.0/10
17. [将 Game Boy 指令 JIT 编译为 WebAssembly 性能超越本地解释器](#item-17) ⭐️ 7.0/10
18. [AI 协作调试的具体案例](#item-18) ⭐️ 7.0/10
19. [日产数据泄露因 Oracle PeopleSoft 漏洞](#item-19) ⭐️ 7.0/10
20. [SimpleHelp 漏洞 CVE-2026-48558 被利用传播 Djinn Stealer](#item-20) ⭐️ 7.0/10
21. [全民新生儿 DNA 测序辩论](#item-21) ⭐️ 7.0/10
22. [用 AI 和 X 射线成像读取赫库兰尼姆卷轴](#item-22) ⭐️ 7.0/10
23. [当性能提升无关紧要时](#item-23) ⭐️ 7.0/10
24. [Rust 中 std::pin::Pin 的用途与使用](#item-24) ⭐️ 7.0/10
25. [重新审视 Yliluoma 有序抖动算法](#item-25) ⭐️ 7.0/10
26. [Typst 关于增量编译的演讲](#item-26) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [vLLM v0.24.0 新增 MiniMax-M3 支持，优化 DeepSeek-V4](https://github.com/vllm-project/vllm/releases/tag/v0.24.0) ⭐️ 9.0/10

vLLM v0.24.0 已发布，新增对 MiniMax-M3 模型的支持，并对 DeepSeek-V4 进行了大量优化，包括 FlashInfer 稀疏索引缓存和预填充分块规划。该版本包含来自 256 位贡献者的 571 次提交。 此版本标志着 vLLM 作为领先的 LLM 推理引擎的重要里程碑，扩大了对 DeepSeek-V4 和 MiniMax-M3 等前沿模型的支持并提升了性能。这些优化将帮助 AI 从业者降低延迟、提高吞吐量，助力大规模部署。 值得注意的技术细节包括：通过 MSA 为 MiniMax-M3 引入 MXFP4 支持，FlashInfer 稀疏索引缓存带来 2-4% 的 TTFT 提升，以及 Model Runner V2 默认支持量化模型。此外，新的流式解析器引擎统一了工具调用/推理解析。

github · khluu · 6月29日 19:41

**背景**: vLLM 是一个开源的高性能大语言模型推理引擎，旨在提供低延迟和高吞吐量。MXFP4 是一种块浮点格式，将 32 个 4 位迷你浮点数分组并共享指数，以减少量化伪影。FlashInfer 是一个用于注意力、GEMM 和 MoE 操作的内核库，在各种 GPU 架构上提供领先性能。TTFT（首 token 时间）衡量模型开始响应提示所需的时间。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/MXFP4">MXFP4</a></li>
<li><a href="https://github.com/flashinfer-ai/flashinfer">GitHub - flashinfer-ai/flashinfer: FlashInfer: Kernel Library ...</a></li>
<li><a href="https://www.ibm.com/think/topics/time-to-first-token">Time to First Token (TTFT) | IBM</a></li>

</ul>
</details>

**标签**: `#vLLM`, `#LLM inference`, `#model optimization`, `#release`, `#AI systems`

---

<a id="item-2"></a>
## [最高法院裁定地理围栏搜查令需宪法保护](https://www.theguardian.com/us-news/2026/jun/29/supreme-court-geofence-warrants-case-decision) ⭐️ 9.0/10

美国最高法院于 2026 年 6 月 29 日裁定，地理围栏搜查令构成第四修正案意义上的搜查，需要宪法隐私保护，多数意见由大法官埃琳娜·卡根撰写。 这一里程碑式的裁决为数字隐私确立了先例，限制了执法机构未经搜查令进行大规模位置数据收集的能力，影响警方监视实践及谷歌等科技公司。 法院认为，个人在公共场所的手机位置数据也享有合理的隐私期待，地理围栏搜查令必须遵守第四修正案的搜查令要求。

hackernews · cdrnsf · 6月29日 15:54 · [社区讨论](https://news.ycombinator.com/item?id=48720924)

**背景**: 地理围栏搜查令是一种法院命令，强制谷歌等技术公司提供特定地理区域和时间范围内所有设备的位置数据。第四修正案保护人民免受不合理的搜查和扣押。此前，下级法院对地理围栏搜查令是否本身违反第四修正案存在分歧，该裁决提供了明确性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.theguardian.com/us-news/2026/jun/29/supreme-court-geofence-warrants-case-decision">US supreme court rules geofence warrants require constitutional privacy protections | US supreme court | The Guardian</a></li>
<li><a href="https://en.wikipedia.org/wiki/Geofence_warrant">Geofence warrant</a></li>

</ul>
</details>

**社区讨论**: 评论者注意到法院意见（有用户提供了链接）引用了事实来源，并引用了通过 IP 地理定位识别葆拉·布罗德威尔的历史案例。一些人讨论了该裁决对 Flock 摄像头等其他监视工具的影响，质疑它们是否现在也需要搜查令。

**标签**: `#law`, `#privacy`, `#supreme-court`, `#surveillance`, `#digital-rights`

---

<a id="item-3"></a>
## [CVE-2026-46817：Oracle EBS 遭积极攻击](https://www.anavem.com/en/news/cybersecurity/cve-2026-46817-oracle-ebs-under-active-attack) ⭐️ 9.0/10

攻击者正在积极利用 CVE-2026-46817，这是 Oracle E-Business Suite 中的一个关键漏洞，威胁全球金融系统。 这一积极利用使金融系统面临风险，因为 Oracle EBS 被广泛部署用于企业资源规划和财务管理。 该漏洞被评为严重级别并在野外被利用；用户应立即应用任何可用的补丁或缓解措施。

rss · Anavem.com · 6月29日 13:46

**背景**: Oracle E-Business Suite (EBS) 是一套集成的业务应用程序套件，用于 ERP、供应链和人力资本管理。Common Vulnerabilities and Exposures (CVE) 是公开已知网络安全漏洞的目录。CVE-2026-46817 是此特定漏洞的唯一标识符。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Oracle_E-Business_Suite">Oracle E-Business Suite</a></li>
<li><a href="https://www.cve.org/">CVE: Common Vulnerabilities and Exposures</a></li>

</ul>
</details>

**标签**: `#cybersecurity`, `#vulnerability`, `#Oracle`, `#CVE`, `#active exploit`

---

<a id="item-4"></a>
## [Longinus 漏洞一举突破 Chrome 渲染器和 V8 沙箱](https://nebusec.ai/research/v8-cve-2026-6307-writeup/) ⭐️ 9.0/10

一个被命名为 Longinus 的新漏洞（CVE-2026-6307）被披露，它能够通过单一利用同时逃逸 Chrome 的渲染器沙箱和 V8 沙箱，这是一项重大的安全发现。 该漏洞绕过了 Chrome 的两层关键安全防护，可能允许攻击者在主机系统上实现完全远程代码执行，影响数十亿依赖 Chrome 沙箱保护的用户。 该利用程序通过单一的漏洞链同时攻击 Chrome 渲染器进程沙箱和 V8 JavaScript 引擎堆沙箱，无需额外漏洞即可从这两个受限制环境中逃脱。

rss · Lobsters · 6月29日 15:00

**背景**: Chrome 使用多层沙箱来隔离渲染器进程与操作系统，限制文件系统访问和其他权限。V8 沙箱进一步限制 JavaScript 引擎内的内存访问，以防止内存破坏漏洞的利用。沙箱逃逸漏洞允许代码突破这些受限环境，在底层系统上执行任意命令。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://chromium.googlesource.com/chromium/src/+/refs/heads/main/docs/design/sandbox_faq.md">Chromium Docs - Sandbox FAQ</a></li>
<li><a href="https://chromium.googlesource.com/chromium/src/+/HEAD/docs/design/sandbox.md">Chromium Docs - Sandbox</a></li>
<li><a href="https://saelo.github.io/presentations/offensivecon_24_the_v8_heap_sandbox.pdf">The V 8 Heap Sandbox - OffensiveCon 2024</a></li>

</ul>
</details>

**标签**: `#security`, `#chrome`, `#v8`, `#cve`, `#sandbox-escape`

---

<a id="item-5"></a>
## [IPv6 分片漏洞实现可靠的 Linux 容器逃逸](https://github.com/sgkdev/ipv6_frag_escape) ⭐️ 9.0/10

sgkdev 在 GitHub 上发布了一个仓库，展示了一项可靠的 Linux 提权与容器逃逸技术，该技术利用了 IPv6 分片包处理中的一个漏洞。 该漏洞意义重大，因为它提供了一种实用且可靠的容器逃逸与获取 root 权限的方法，可能被用于针对容器化环境的真实攻击。它凸显了即使在现代 Linux 内核中，IPv6 处理方面仍存在关键安全缺口。 该漏洞利用 IPv6 分片绕过安全边界实现提权。仓库包含概念验证代码，并声称在较新的 Linux 内核上可靠运行。

rss · Lobsters · 6月29日 17:01

**背景**: IPv6 分片允许将大的数据包拆分成更小的片段。RFC 5722 要求 IPv6 主机静默丢弃重叠片段以防止某些攻击，但一些实现可能仍然存在漏洞。容器逃逸是指突破容器的隔离环境以访问宿主机系统，通常借助内核漏洞实现。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://hackaday.com/2024/08/30/this-week-in-security-the-rest-of-the-ipv6-story-cve-hunting-and-hacking-the-tsa/">This Week In Security: The Rest Of The IPv6 Story, CVE ...</a></li>
<li><a href="https://securelayer7.net/learn/containers/what-is-a-container-escape">What is a Container Escape ? | SecureLayer7</a></li>

</ul>
</details>

**社区讨论**: Lobste.rs 上对该仓库的评论证实了该漏洞的严重性和可靠性，一些用户指出了其对云环境和容器部署的潜在影响。

**标签**: `#security`, `#vulnerability`, `#container-escape`, `#linux`, `#ipv6`

---

<a id="item-6"></a>
## [.self：一个支持自托管的新顶级域名，提供免费子域名](https://hccf.onmy.cloud/2026/06/21/reclaiming-our-digital-selves-hccfs-vision-for-a-human-centered-top-level-domain/) ⭐️ 8.0/10

一项关于新顶级域名“.self”的提案被提出，为每人提供一个免费子域名，以支持自托管并重新掌控数字身份。 如果实施，.self 可以赋予个人托管自己服务的能力，减少对中心化平台的依赖，但必须解决域名抢注、滥用和可持续资金等挑战。 该提案规定每人一个免费子域名，并通过身份验证和事后基于信誉的移除等机制防止抢注和滥用。资金和治理模式尚未明确。

hackernews · HumanCCF · 6月29日 19:49 · [社区讨论](https://news.ycombinator.com/item?id=48724230)

**背景**: 自托管是指在自己的私有服务器上运行网站或服务，而非使用托管平台。顶级域名（TLD）是域名名称的最后一部分（例如.com）。历史上像.tk 这样的免费顶级域名曾因被诈骗者滥用，导致被邮件提供商和杀毒软件屏蔽。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Self-hosting_(network)">Self-hosting (network) - Wikipedia</a></li>
<li><a href="https://github.com/awesome-selfhosted/awesome-selfhosted">GitHub - awesome-selfhosted/awesome-selfhosted: A list of ...</a></li>

</ul>
</details>

**社区讨论**: 评论者对防止抢注和滥用的可行性表示怀疑，并引用了.tk 的前车之鉴。有人建议使用身份证明和信誉系统，也有人提到微软 Vega 以实现隐私保护的身份验证。资金和执行问题也被提出。

**标签**: `#top-level domain`, `#self-hosting`, `#internet governance`, `#DNS`, `#digital identity`

---

<a id="item-7"></a>
## [火箭实验室历史性收购铱星公司](https://investors.rocketlabcorp.com/news-releases/news-release-details/rocket-lab-acquire-iridium-historic-deal-creating-fully) ⭐️ 8.0/10

火箭实验室宣布收购铱星公司，获得铱星盈利的卫星通信业务和宝贵的频谱牌照，打造一家完全一体化的太空公司。 这笔交易标志着火箭实验室向垂直整合发射与卫星运营的战略迈进，类似于 SpaceX 的模式，并为火箭实验室提供了稳定的收入来源和保证的发射需求。 火箭实验室不仅获得铱星卫星星座，还获得其宝贵的频谱权和盈利业务，而铱星股东将获得合并后实体的股票。收购预计将于 2025 年完成。

hackernews · everfrustrated · 6月29日 14:09 · [社区讨论](https://news.ycombinator.com/item?id=48719485)

**背景**: 火箭实验室是一家提供发射服务和建造卫星的太空公司。铱星公司运营全球卫星通信网络。垂直整合使公司能够控制更多供应链环节并降低成本。

**社区讨论**: 评论意见不一；一些人看到了与 SpaceX 的 Starlink 策略的相似之处，指出火箭实验室可以利用铱星来保证发射频率。其他人则对太空垃圾和夜空商业化表示担忧。

**标签**: `#Rocket Lab`, `#Iridium`, `#acquisition`, `#space industry`, `#satellite communications`

---

<a id="item-8"></a>
## [Ornith-1.0：自我改进的开源代理编程模型](https://github.com/deepreinforce-ai/Ornith-1) ⭐️ 8.0/10

Ornith-1.0 是由 DeepReinforce.AI 在 2025 年 6 月发布的一系列开放权重（MIT 许可）的微调 Qwen 模型，专用于代理编程。它利用强化学习自我改进编码工作流程，从而实现了更快的推理速度和有竞争力的性能。 这是首个获得本地 LLM 社区好评的 Qwen 微调模型，表明开源模型在代理编程任务上可以匹敌甚至超越专有模型。其自我改进的训练方法可以减少人工数据整理的需求，为更自主的编程助手铺平道路。 Ornith-1.0 提供 9B Dense、31B Dense、35B MoE 和 397B MoE 四种变体，基于预训练的 Qwen 模型构建。社区测试显示，35B 变体由于更紧凑的思维链，速度比 Qwen-3.6 35B 快 3 倍，在复杂编程任务上表现略优。

hackernews · danboarder · 6月29日 17:16 · [社区讨论](https://news.ycombinator.com/item?id=48722052)

**背景**: 代理编程是指 AI 代理自主执行多步软件开发任务，如代码生成、调试和测试。微调是通过在精选数据集上训练，将预训练的大语言模型（如 Qwen）适配到特定领域。Ornith-1.0 使用强化学习不仅生成解决方案，还学习驱动这些解决方案的脚手架（工作流程），这是一种自我改进的形式。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://medium.com/data-science-in-your-pocket/ornith-1-0-self-learning-llm-for-coding-318c9a830bfc">Ornith 1 . 0 : Self Learning LLM for Coding | by Mehul Gupta | Medium</a></li>
<li><a href="https://github.com/deepreinforce-ai/Ornith-1">GitHub - deepreinforce-ai/ Ornith - 1 · GitHub</a></li>
<li><a href="https://ollama.com/library/ornith">ornith</a></li>

</ul>
</details>

**社区讨论**: 社区反应总体积极；用户注意到 Ornith-1.0 提供了比 Qwen-3.6 35B 更快的推理和创意解决方案。部分用户报告它在某些任务上仍有困难，且在无工具环境下容易产生幻觉，但总体被视为一个扎实的微调模型，是开源代理编程的进步。

**标签**: `#AI`, `#open-source`, `#agentic coding`, `#Qwen`, `#fine-tuning`

---

<a id="item-9"></a>
## [韩国宣布 1 万亿美元投资内存芯片和人形机器人](https://arstechnica.com/ai/2026/06/south-korea-to-spend-1t-on-more-memory-chip-production-and-humanoid-robots/) ⭐️ 8.0/10

韩国宣布了一项 1 万亿美元的投资计划，用于新建内存芯片制造工厂并开发人形机器人，作为其主导半导体和机器人产业战略的一部分。 这项巨额投资可能重塑全球内存芯片供应并加速人形机器人商业化，但也引发了关于内存市场潜在产能过剩的担忧，以及人形形态是否最优的辩论。 该计划专门拨款 5850 亿美元用于新建晶圆厂，其余用于机器人。内存晶圆厂通常需要 5-10 年才能建成投产，而像 ARMAR-6 这样的人形机器人已经在工业领域开发使用。

hackernews · jnord · 6月29日 22:21 · [社区讨论](https://news.ycombinator.com/item?id=48726102)

**背景**: 内存芯片是几乎所有电子设备中使用的关键商品组件，其生产需要造价数十亿美元的专门制造工厂（fab）。人形机器人是模仿人体解剖学设计的机器人，旨在用于工业、医疗和服务等场景——像 NVIDIA 这样的公司正在开发计算平台来支持它们。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/List_of_semiconductor_fabrication_plants">List of semiconductor fabrication plants - Wikipedia</a></li>
<li><a href="https://www.tomshardware.com/news/micron-idaho-memory-fab-ground-breaking">Micron Breaks Ground On $15 Billion Idaho Memory Chip Fab</a></li>
<li><a href="https://en.wikipedia.org/wiki/Humanoid_robot">Humanoid robot - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者提出了几点：担心由于争相建厂导致产能过剩，质疑为何选择人形形态而非潜在更优的设计，对晶圆厂建设周期（5-10 年）的好奇，以及一个比喻将内存芯片比作'杂货'（必需品），将人形机器人比作'舞蹈课'（投机性的未来）。

**标签**: `#semiconductors`, `#robotics`, `#investment`, `#manufacturing`

---

<a id="item-10"></a>
## [深入解析 CUDA 内核启动内部机制](https://fergusfinn.com/blog/what-happens-when-you-run-a-gpu-kernel/) ⭐️ 8.0/10

Fergus Finn 发表了一篇博文，详细介绍了启动 CUDA 内核时从 CPU 到 GPU 的完整路径，涵盖了驱动程序、硬件调度以及门铃寄存器和队列管理描述符等同步机制。 这篇博文填补了 CUDA 教育中常见的空白，解释了从启动语法到实际 GPU 执行之间发生的事情，有助于开发者编写更高效的代码并调试性能问题。 文章特别强调了门铃机制和 QMD 格式的作用，这些在典型教程中往往被一带而过，同时还讨论了默认流中的隐式同步。

hackernews · mezark · 6月29日 13:11 · [社区讨论](https://news.ycombinator.com/item?id=48718863)

**背景**: CUDA 内核启动并非瞬间完成，它涉及多个层次，包括 CUDA 运行时、驱动程序和 GPU 硬件。CPU 将命令写入环形缓冲区，通过门铃通知 GPU，然后 GPU 的工作调度器获取并执行队列管理描述符。理解这一路径对于优化延迟敏感型应用至关重要。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.geeksforgeeks.org/cpp/launching-a-kernel-in-cuda/">Launching a Kernel | CUDA - GeeksforGeeks</a></li>
<li><a href="https://docs.nvidia.com/cuda/cuda-runtime-api/group__CUDART__EXECUTION.html">CUDA Runtime API :: CUDA Toolkit Documentation</a></li>
<li><a href="https://enccs.github.io/cuda/2.02_HelloGPU/">Launching the GPU kernel — CUDA training materials documentation</a></li>

</ul>
</details>

**社区讨论**: 评论高度正面，读者对文章的深度表示赞赏，尤其是门铃和 QMD 部分。有读者指出，CUDA 默认流中的隐式同步与 Vulkan 的显式同步相比更易用。另一位读者提到 NVIDIA 提供了开放的 GPU 文档供进一步阅读。

**标签**: `#CUDA`, `#GPU`, `#HPC`, `#systems`, `#GPU internals`

---

<a id="item-11"></a>
## [人工智能热潮促使海底电缆绕开中国](https://www.economist.com/asia/2026/06/29/the-ai-boom-and-geopolitics-are-rewiring-asias-oceans) ⭐️ 8.0/10

受人工智能热潮和地缘政治紧张局势影响，连接数据中心的新海底电缆正在绕开中国及战略咽喉要道。 这一变化影响着全球互联网流量的骨干网，可能增加 AI 数据传输的延迟和成本，同时增强了某些线路的安全性和韧性。 重新布线旨在避开中国附近及马六甲海峡等咽喉要道的脆弱性，这些区域对超过 99%的洲际数据流量至关重要。

rss · The Economist · 6月29日 17:14

**背景**: 海底电缆承载着全球超过 99%的洲际互联网流量。地缘政治紧张局势和 AI 数据中心的爆发式增长增加了对安全、低延迟连接的需求，促使网络运营商重新考虑传统上经过或靠近中国的路线。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.submarinecablemap.com/">Submarine Cable Map</a></li>
<li><a href="https://www.geocables.com/">GeoCables - Submarine Cable Encyclopedia, Live Routes ...</a></li>
<li><a href="https://resources.telegeography.com/submarine-cable-routing-increasingly-crowded-seafloor">Submarine Cable Routing on an Increasingly Crowded Seafloor</a></li>

</ul>
</details>

**标签**: `#geopolitics`, `#undersea cables`, `#AI infrastructure`, `#data centers`, `#Asia`

---

<a id="item-12"></a>
## [AT-URI 语法缺陷曝光](https://bnewbold.leaflet.pub/3mph4hzvbdc2v) ⭐️ 8.0/10

一篇技术分析揭示了 AT-URI（AT Protocol 的标识符方案）中存在的重大语法问题，指出了不一致性和潜在的互操作性问题。 这些问题至关重要，因为 AT-URI 是 AT Protocol 的基础，而 AT Protocol 旨在为去中心化社交网络提供动力；语法问题可能会阻碍开发者的采用和跨平台兼容性。 该分析突出了诸如基于句柄的 URI 缺乏持久性、解析规则模糊以及偏离 RFC-3986 URI 标准等问题，这可能会影响依赖 AT-URI 的实现。

rss · Lobsters · 6月29日 20:34

**背景**: AT Protocol（认证传输协议）是一个用于社交网络应用的去中心化框架。它使用 DID 作为持久身份标识，AT URI 用于资源标识。AT URI 旨在符合 RFC-3986，但存在特定注意事项，使其成为生态系统中一个复杂的组成部分。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://atproto.com/specs/at-uri-scheme">AT URI scheme (at://) - AT Protocol</a></li>
<li><a href="https://en.wikipedia.org/wiki/AT_Protocol">AT Protocol - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Uniform_Resource_Identifier">Uniform Resource Identifier - Wikipedia</a></li>

</ul>
</details>

**标签**: `#AT Protocol`, `#URI`, `#syntax`, `#technical`, `#discussion`

---

<a id="item-13"></a>
## [DRM GEM change_handle 释放后重用导致提权至 root](https://cyberstan.co.uk/drm-lpe-linux/) ⭐️ 8.0/10

Linux 内核 DRM GEM 子系统的 change_handle ioctl 中存在一个释放后重用漏洞（CVE-2026-46215），允许任意本地非特权用户将权限提升至 root。 这是一个高严重性的 Linux 内核漏洞，可使非特权进程完全控制系统，影响大量使用 DRM 进行图形处理的系统。 该漏洞的产生是因为 drm_gem_change_handle_ioctl 在移动 GEM 对象的句柄时未增加其 handle_count，导致在短时间内对象有两个 IDR 条目但 handle_count 仍为 1，从而产生竞争条件。

rss · Lobsters · 6月29日 18:05

**背景**: 直接渲染管理器（DRM）是 Linux 内核中用于管理图形硬件访问的子系统。图形执行管理器（GEM）是 DRM 内的内存管理器，负责处理缓冲区对象。change_handle ioctl 用于在文件私有表中将 GEM 对象从一个句柄重新分配给另一个句柄。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Direct_Rendering_Manager">Direct Rendering Manager - Wikipedia</a></li>
<li><a href="https://cyberstan.co.uk/drm-lpe-linux/">Unprivileged root via a use-after-free in DRM GEM change ...</a></li>

</ul>
</details>

**标签**: `#linux`, `#kernel`, `#security`, `#vulnerability`, `#drm`

---

<a id="item-14"></a>
## [ACM 文章揭穿形式化验证迷思](https://queue.acm.org/detail.cfm?id=3819084) ⭐️ 8.0/10

ACM Queue 上发表了一篇题为《你对形式化验证一无所知》的文章，探讨并澄清了软件工程中关于形式化验证的常见误解。 形式化验证是确保软件正确性的高价值但常被误解的技术；这篇文章有助于弥合实践工程师的知识差距。 文章可能讨论了诸如形式化验证过于昂贵、仅适用于安全关键系统或需要完整形式化规范等误解。

rss · Lobsters · 6月29日 14:15

**背景**: 形式化验证是一种严格的数学技术，用于证明或证伪系统相对于形式化规范的正确性。它被用于硬件和软件验证，可实现安全认证中的最高评估保证等级（EAL7）。例子包括 CompCert C 编译器和 seL4 微内核。尽管功能强大，形式化验证常被认为过于复杂或不切实际，而这正是文章所挑战的观点。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Formal_verification">Formal verification</a></li>

</ul>
</details>

**标签**: `#formal verification`, `#software engineering`, `#correctness`, `#ACM`

---

<a id="item-15"></a>
## [Qwen 3.6 27B：本地开发的甜蜜点？](https://quesma.com/blog/qwen-36-is-awesome/) ⭐️ 7.0/10

一篇博文展示了 Qwen 3.6 27B 在高端 128GB MacBook Pro 上的运行，但社区评论强烈批评其实用性和成本，认为过于昂贵且噪音大，不适合实际工作。 这场争论凸显了本地隐私与控制优势与运行大型模型的高硬件成本和不便之间的矛盾。它影响着开发者在本地部署和云 API 服务之间的选择。 博文特意使用了 128GB 的 MacBook Pro，起价 6699 美元。Qwen 3.6 27B 是一个 270 亿参数的密集模型，推理需要大量内存。

hackernews · stared · 6月29日 17:05 · [社区讨论](https://news.ycombinator.com/item?id=48721903)

**背景**: Qwen 3.6 是阿里巴巴推出的开源大语言模型系列，其中 27B 版本针对编码任务进行了优化。在本地运行此类模型需要配备大量 RAM/VRAM 的高端硬件，通常花费数千美元。许多开发人员转而使用 OpenRouter 或前沿实验室等云 API。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/Qwen/Qwen3.6-27B">Qwen/Qwen3.6-27B · Hugging Face</a></li>
<li><a href="https://overchat.ai/ai-hub/llm-hardware-requirements">Local LLM Hardware Requirements in 2026 | AI Hub</a></li>

</ul>
</details>

**社区讨论**: 评论基本持批评态度。用户指出所需硬件成本高昂（128GB MacBook Pro 售价 6699 美元），由于散热和噪音问题，在笔记本电脑上运行密集的 LLM 任务不切实际，并且博文的示例并不代表在现有代码库上的实际编码。一些人建议更具成本效益的选择，如 Mac Mini M4 或使用云服务。

**标签**: `#LLM`, `#Qwen`, `#local development`, `#hardware`, `#community discussion`

---

<a id="item-16"></a>
## [提出基于 SSH 的原生图形化 Shell 方案](https://probablymarcus.com/blocks/2026/06/28/native-graphical-shell-for-SSH.html) ⭐️ 7.0/10

一篇博客文章提出了一种基于 SSH 的原生图形化 Shell，旨在改善传统基于 TUI 的终端的远程 GUI 体验。该概念建议将 SSH 用作传输层，转发 GUI 显示层，类似于它如何转发 PTY 用于终端。 该提案挑战了开发者社区中盛行的 TUI 优越性思维，可能扩展 SSH 在现代 GUI 应用中的实用性。如果实现，它可能简化远程图形化开发和管理。 该提案承认了像 X11 转发和 HTML5 Web 应用这样的现有技术，但寻求一种更原生的方法。社区讨论强调了浏览器连接到 Unix 套接字的安全问题。

hackernews · Lobsters · 6月29日 15:42 · [社区讨论](https://news.ycombinator.com/item?id=48720758)

**背景**: SSH（安全外壳）是一种用于远程安全访问系统的协议，传统上用于基于文本的终端模拟器（TUI）。图形化远程访问通过 X11 转发或 VNC 实现，但这些解决方案可能效率低下或不安全。原生图形化 Shell 将直接把 GUI 应用转发集成到 SSH 协议中。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://news.ycombinator.com/item?id=48720758">A native graphical shell for SSH | Hacker News</a></li>
<li><a href="https://github.com/GOODBOY008/r-shell">GitHub - GOODBOY008/r-shell: Lightweight open-source SSH ...</a></li>

</ul>
</details>

**社区讨论**: 评论意见分歧；一些人认为这是在重新发明已有的解决方案如 X11 转发，而另一些人则认为 TUI 并非天生优越，SSH 应该支持 GUI 层。一位评论者指出，出于安全原因，浏览器缺乏原始 Unix 套接字功能。

**标签**: `#SSH`, `#GUI`, `#remote access`, `#terminal`, `#shell`

---

<a id="item-17"></a>
## [将 Game Boy 指令 JIT 编译为 WebAssembly 性能超越本地解释器](https://humphri.es/blog/WATaBoy/) ⭐️ 7.0/10

WATaBoy 项目展示了将 Game Boy 模拟器指令即时编译(JIT)为 WebAssembly，性能优于原生 C++解释器，尤其在允许 WebAssembly JIT 的浏览器中表现突出。 该方法为 iOS 等禁止原生 JIT 但允许浏览器中 WebAssembly JIT 的平台提供了高性能模拟的可行路径，有望在移动设备上解锁强大的模拟器。 该项目使用 WebAssembly 文本格式(WAT)动态生成 Game Boy CPU 指令代码。性能基准测试显示，WASM JIT 优于原生解释器，不过 Firefox 比 Chrome 和 Safari 慢约 25%。

hackernews · Lobsters · 6月29日 15:02 · [社区讨论](https://news.ycombinator.com/item?id=48720190)

**背景**: 模拟器通常通过解释或动态重编译(JIT)来转换客户机指令。Apple 在 iOS 上限制原生 JIT，但允许 WebKit 内 JavaScript 和 WebAssembly 的 JIT，这使得 JIT 到 WASM 的技术具有吸引力。WAT 是 WebAssembly 的人类可读文本格式，旨在让开发者编写或检查 Wasm 模块。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/WebAssembly">WebAssembly - Wikipedia</a></li>
<li><a href="https://developer.mozilla.org/en-US/docs/WebAssembly/Guides/Understanding_the_text_format">Understanding WebAssembly text format - WebAssembly | MDN</a></li>

</ul>
</details>

**社区讨论**: 评论者称赞该项目巧妙利用 WebAssembly JIT 绕过 iOS 限制，并与静态重编译方法进行了比较。有人注意到浏览器间的显著性能差异，推测是浏览器特定优化所致。也有评论对作为本科生项目的复杂性表示赞赏。

**标签**: `#JIT`, `#WebAssembly`, `#emulation`, `#performance`, `#iOS`

---

<a id="item-18"></a>
## [AI 协作调试的具体案例](https://htmx.org/essays/working-with-ai/) ⭐️ 7.0/10

htmx 的创建者 Carson Gross 记录了一个使用 Claude AI 修复 hyperscript 解析 bug 的详细案例，揭示了 AI 在软件开发中的优势与不足。 这一分析为当前 AI 在调试方面的能力提供了实用且细致的见解，对于考虑将 AI 工具整合到工作流中的开发者很有价值。它也引发了关于 LLM 在批判性思维方面根本局限性的讨论。 文章专注于 hyperscript 解析器中的一个普通 bug，与 Claude 的交互表明 AI 擅长分析和样板代码，但在批判性思维和整体设计方面较弱。社区评论指出缺少关于所用 Claude 模型和提示工程方法的细节。

hackernews · comma_at · 6月29日 14:53 · [社区讨论](https://news.ycombinator.com/item?id=48720064)

**背景**: hyperscript 是一种简洁、类自然语言的网页脚本语言，受 Apple HyperTalk 启发。htmx 是一个轻量级库，通过属性扩展 HTML，实现 AJAX 和动态更新而无需页面刷新。Claude 是 Anthropic 开发的大型语言模型，注重 AI 安全和伦理合规。在此上下文中，Claude 被用作 AI 编码助手来调试 hyperscript 解析器的问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Claude_(AI)">Claude (AI) - Wikipedia</a></li>
<li><a href="https://hyperscript.org/">hyperscript</a></li>
<li><a href="https://htmx.org/">htmx - high power tools for html</a></li>

</ul>
</details>

**社区讨论**: 社区成员总体上赞赏这篇诚实的分析，但指出文章缺乏具体细节如使用了哪个 Claude 模型。几位评论者认同 LLM 在批判性思维和设计方面存在困难，认为缺乏世界模型是根本局限。讨论还涉及使用 htmx 与 AI 进行编码的实际经验。

**标签**: `#AI`, `#LLM`, `#software engineering`, `#debugging`, `#htmx`

---

<a id="item-19"></a>
## [日产数据泄露因 Oracle PeopleSoft 漏洞](https://www.anavem.com/en/news/cybersecurity/nissan-data-breach-tied-to-oracle-peoplesoft-flaw) ⭐️ 7.0/10

日产披露了一起数据泄露事件，攻击者利用与 ShinyHunters 勒索组织相关的 Oracle PeopleSoft 关键漏洞（CVE-2026-35273）入侵系统，影响了现任和前任员工。 此事件凸显了未修补企业软件的现实后果，一家大型车企的员工数据遭到泄露。同时，它也强调了 ShinyHunters 等组织针对已知漏洞的活跃威胁。 CVE-2026-35273 是 Oracle PeopleSoft PeopleTools 中的一个严重未认证远程代码执行漏洞，Oracle 已为此发布了带外安全警报。ShinyHunters 一直在利用此漏洞进行大规模数据盗窃活动。

rss · Anavem.com · 6月29日 20:40

**背景**: Oracle PeopleSoft 是一套企业资源规划软件，PeopleTools 是其开发平台。ShinyHunters 是一个以数据盗窃和勒索闻名的臭名昭著的组织。在接到活跃利用报告后，Oracle 为此零日漏洞发布了紧急补丁。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.oracle.com/security-alerts/alert-cve-2026-35273.html">Oracle Security Alert Advisory - CVE-2026-35273</a></li>
<li><a href="https://www.securityweek.com/oracle-addresses-peoplesoft-vulnerability-amid-reports-of-zero-day-attacks/">Oracle Addresses PeopleSoft Vulnerability Amid Reports of Zero-Day Attacks - SecurityWeek</a></li>
<li><a href="https://arcticwolf.com/resources/blog/critical-oracle-peoplesoft-vulnerability-actively-exploited-in-shinyhunters-campaign/">Critical Oracle PeopleSoft Vulnerability Actively Exploited in ShinyHunters Campaign | Arctic Wolf</a></li>

</ul>
</details>

**标签**: `#cybersecurity`, `#data breach`, `#Oracle PeopleSoft`, `#vulnerability`, `#Nissan`

---

<a id="item-20"></a>
## [SimpleHelp 漏洞 CVE-2026-48558 被利用传播 Djinn Stealer](https://www.anavem.com/en/news/cybersecurity/cve-2026-48558-simplehelp-exploited-to-drop-djinn-stealer) ⭐️ 7.0/10

攻击者正在积极利用 SimpleHelp 的严重漏洞 CVE-2026-48558，部署新型跨平台信息窃取恶意软件 Djinn Stealer，该恶意软件针对 Windows、macOS 和 Linux 系统。 这很重要，因为它展示了广泛使用的远程支持软件中严重漏洞的现实世界利用，可能导致跨多个平台的广泛凭据窃取，包括云和 AI 工具凭据。 CVE-2026-48558 是 SimpleHelp 中的身份验证绕过漏洞；Djinn Stealer 是一种此前未知的窃取程序，目标是浏览器凭据、云令牌和 AI 工具密钥。

rss · Anavem.com · 6月29日 14:00

**背景**: SimpleHelp 是一种远程支持和访问软件，供 IT 专业人员和托管服务提供商用于跨平台控制设备和提供支持。Djinn Stealer 是一种新型信息窃取恶意软件，可在 Windows、macOS 和 Linux 上运行，旨在窃取凭据和令牌等敏感信息。漏洞 CVE-2026-48558 允许攻击者绕过 SimpleHelp 的身份验证，从而无需有效凭据即可部署恶意软件。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.bleepingcomputer.com/news/security/hackers-exploit-critical-simplehelp-flaw-deploy-new-djinn-infostealer-taskweaver-malware/">Critical SimpleHelp flaw exploited to deploy new stealer malware</a></li>
<li><a href="https://www.darkreading.com/cyberattacks-data-breaches/djinn-stealer-targets-cloud-ai-credentials">Djinn Stealer Targets Cloud and AI Credentials</a></li>
<li><a href="https://simple-help.com/">SimpleHelp | Remote Support Software by SimpleHelp</a></li>

</ul>
</details>

**标签**: `#cybersecurity`, `#vulnerability`, `#CVE`, `#malware`, `#cross-platform`

---

<a id="item-21"></a>
## [全民新生儿 DNA 测序辩论](https://www.economist.com/science-and-technology/2026/06/29/should-every-babys-dna-be-sequenced) ⭐️ 7.0/10

《经济学人》在一篇新文章中探讨了为每个新生儿进行 DNA 测序的潜在好处和伦理挑战。 这一讨论可能影响未来的新生儿筛查公共卫生政策，并对个性化医疗、隐私和公平性产生影响。 文章可能权衡了早期发现遗传疾病的医学益处与同意、数据隐私和潜在歧视等伦理问题。

rss · The Economist · 6月29日 19:51

**标签**: `#genomics`, `#bioethics`, `#newborn screening`, `#DNA sequencing`, `#public health`

---

<a id="item-22"></a>
## [用 AI 和 X 射线成像读取赫库兰尼姆卷轴](https://www.economist.com/culture/2026/06/29/the-herculaneum-scrolls-are-starting-to-be-read) ⭐️ 7.0/10

研究人员首次完整破译了碳化的赫库兰尼姆卷轴（Pherc. 1667），使用了欧洲同步辐射设施（ESRF）的相位对比 X 射线显微断层扫描和人工智能算法。 这一突破打开了此前被认为无法阅读的数百份古代文本的访问途径，可能改变我们对古典哲学和文学的理解。 该卷轴的扫描分辨率高到足以区分单个碳基墨迹笔画，AI 被训练用于在复杂的分层表面上检测墨水。

rss · The Economist · 6月29日 15:39

**背景**: 赫库兰尼姆卷轴在公元 79 年维苏威火山喷发中被掩埋并碳化。几个世纪以来，它们无法在不破坏的情况下展开。虚拟展开结合了 X 射线显微断层扫描和 AI，以数字方式解开并阅读文本，这一挑战由维苏威挑战赛推动。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Virtual_unfolding">Virtual unfolding - Wikipedia</a></li>
<li><a href="https://scrollprize.org/firstscroll">An entire Herculaneum scroll has been read for the first time</a></li>

</ul>
</details>

**标签**: `#archaeology`, `#AI`, `#imaging`, `#ancient texts`, `#technology`

---

<a id="item-23"></a>
## [当性能提升无关紧要时](https://blog.colinbreck.com/when-impressive-performance-gains-do-not-matter/) ⭐️ 7.0/10

这篇文章指出，令人印象深刻的性能优化在实践中往往无关紧要，因为它们针对的是无关紧要的瓶颈或对实际影响微乎其微。 这挑战了追求微优化而不考虑实际用户体验或系统限制的常见工程文化，鼓励对性能工作采取更务实的态度。 作者可能提供了场景示例，说明优化代码仅带来微不足道的好处，例如当 I/O 或网络延迟占主导时，或者优化在生产中从未被触发。

rss · Lobsters · 6月29日 13:15

**背景**: 性能优化是软件工程中的常见关注点，但工程师经常会过早优化或关注错误的部分。文章强调，了解实际使用模式并测量真正的瓶颈比实现令人印象深刻的微基准测试数字更重要。

**标签**: `#performance`, `#software engineering`, `#optimization`, `#engineering culture`

---

<a id="item-24"></a>
## [Rust 中 std::pin::Pin 的用途与使用](https://vrong.me/blog/what-is-pinning-in-rust/) ⭐️ 7.0/10

这篇博客文章解释了 Rust 中 std::pin::Pin 的用途和使用方法，这是 async/await 和自引用类型的一个关键概念。 Pin 是安全异步 Rust 的基础，因为它确保 future 和其他自引用类型在被固定后不能被移动，从而防止内存不安全。 博客涵盖了栈固定和堆固定，解释了 Pin<&mut T> 和 Pin<Box<T>> 之间的区别，并讨论了 Unpin trait。

rss · Lobsters · 6月29日 16:37

**背景**: 在 Rust 中，async/await 特性使用的 future 可能包含自引用指针。移动这样的 future 会使这些指针失效，导致未定义行为。Pin 提供了值不会被移动的保证，从而支持安全的自引用类型。Unpin trait 表示即使在固定后也能安全移动的类型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://vrong.me/blog/what-is-pinning-in-rust/">What is ` std :: pin :: Pin ` in Rust ? | vrongmeal</a></li>
<li><a href="https://tuttlem.github.io/2025/05/26/understanding-pin-safe-types-in-rust.html">Understanding Pin-safe Types in Rust · Cogs and Levers</a></li>
<li><a href="https://medium.com/@cheneyshyu/why-adopt-pin-unpin-over-relative-pointers-dca2080ccfe4">Why Adopt Pin/Unpin Over Relative Pointers? [ Rust Design...] | Medium</a></li>

</ul>
</details>

**标签**: `#Rust`, `#async`, `#Pin`, `#memory management`

---

<a id="item-25"></a>
## [重新审视 Yliluoma 有序抖动算法](https://30fps.net/pages/revisiting-yliluoma-2/) ⭐️ 7.0/10

30fps.net 上的一篇新文章重新审视了 Yliluoma 的有序抖动算法，可能提出了优化或替代实现，以在有限调色板上获得更好的色彩再现。 这一回顾对复古计算和图形编程社区具有重要意义，因为它可以改善有限色深显示器（如旧硬件或现代低端设备）的图像质量。 Yliluoma 的算法包括多个变体（1、2、3），具有基于 gamma 的混合和 CIE 颜色评估等功能，新文章可能比较它们或引入更新版本。

rss · Lobsters · 6月30日 01:28

**背景**: 有序抖动是一种通过在整个图像上平铺阈值图来在较少颜色的显示器上显示连续色调图像的技术。Yliluoma 的有序抖动算法将其扩展到任意调色板，使用每像素颜色候选数组和高级颜色度量来减少条带效应并产生更平滑的结果。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Ordered_dithering">Ordered dithering</a></li>
<li><a href="https://bisqwit.iki.fi/story/howto/dither/jy/">Arbitrary-palette positional dithering algorithm</a></li>
<li><a href="https://matejlou.blog/2023/12/06/ordered-dithering-for-arbitrary-or-irregular-palettes/">Ordered Dithering with Arbitrary or Irregular Colour Palettes</a></li>

</ul>
</details>

**标签**: `#graphics`, `#dithering`, `#algorithm`, `#retro computing`, `#computer graphics`

---

<a id="item-26"></a>
## [Typst 关于增量编译的演讲](https://youtu.be/yWWVhbyOWWE) ⭐️ 7.0/10

Typst 团队在一个演讲中解释了 Typst 如何通过实现增量编译来快速重新编译文档，从而减少作者的等待时间。 这很重要，因为增量编译是使 Typst 区别于 LaTeX 等传统排版系统的关键特性，有望为大文档提供近乎即时的预览更新。它可以显著改善研究人员、学生和出版商等频繁编辑和重新编译文档的用户的工作流程。 演讲涵盖了设计决策，例如缓存解析后的抽象语法树和增量布局计算，使得只重新计算更改的部分。Typst 的增量系统是内置于核心的，而非事后添加，从而保证了效率。

rss · Lobsters · 6月29日 13:57

**背景**: Typst 是一个现代的、开源的排版系统，被设计为 LaTeX 的替代品，注重易用性和快速编译。增量编译是一种技术，只重新编译文档中更改的部分，而不是整个文档，从而为迭代编辑节省时间。这与 LaTeX 形成对比，后者通常从头开始重新编译整个文档。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Typst">Typst - Wikipedia</a></li>
<li><a href="https://www.researchgate.net/publication/364622490_Fast_Typesetting_with_Incremental_Compilation">(PDF) Fast Typesetting with Incremental Compilation</a></li>
<li><a href="https://github.com/typst/typst">GitHub - typst / typst : A markup-based typesetting system that is...</a></li>

</ul>
</details>

**标签**: `#typst`, `#typesetting`, `#incremental compilation`, `#programming languages`, `#tools`

---