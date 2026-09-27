---
layout: default
title: "Horizon Summary: 2026-09-27 (ZH)"
date: 2026-09-27
lang: zh
---

> 从 40 条内容中筛选出 10 条重要资讯。

---

1. [DeepSeek 发布 DSec：可在 160 个节点上运行 38 万个并发沙箱](#item-1) ⭐️ 8.0/10
2. [逆向工程揭示 Intel 8087 正切算法：不止于 CORDIC](#item-2) ⭐️ 8.0/10
3. [十五年后再看 Apple Cards：被它「Sherlock」的那家创业公司](#item-3) ⭐️ 7.0/10
4. [Drawgent：直接在实时 Excalidraw 画布上绘图的编码智能体](#item-4) ⭐️ 7.0/10
5. [Haskell 文章探讨 LLM 时代如何保持编程乐趣并引发热议](#item-5) ⭐️ 7.0/10
6. [NixOS 被移植到 Valve 的 Steam Link 串流盒上](#item-6) ⭐️ 7.0/10
7. [Valve 在 Steam 测试版中引入低延迟视频编解码器 Pyrowave](#item-7) ⭐️ 7.0/10
8. [p5.js 引入计算着色器，用于教授 GPU 编程](#item-8) ⭐️ 7.0/10
9. [2026 年 Rust 中 SIMD 的现状](#item-9) ⭐️ 7.0/10
10. [GitHub 通过刻意增加 CSS 体积来提升站点性能](#item-10) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [DeepSeek 发布 DSec：可在 160 个节点上运行 38 万个并发沙箱](https://arxiv.org/abs/2609.22978) ⭐️ 8.0/10

DeepSeek 在 arXiv 上发表论文，介绍了面向大规模智能体（agent）训练的沙箱基础设施 DSec（DeepSeek Elastic Compute），能够在 160 个 AMD EPYC 服务器节点上运行 38 万个并发沙箱。从 DeepSeek-V4.1 开始，DeepSeek 将 rollout 执行迁移到 DSec 上，并拆分为两部分：承载 scaffold（如 DeepSeek Harness）及其工具的 agent 沙箱，以及负责管理沙箱、提供与 scaffold 无关的控制层的 worker 容器。 智能体强化学习的瓶颈之一在于能并行运行多少个隔离环境，因此把沙箱密度提升到几十万级别、且只依赖相对普通的 CPU 集群，能直接提高智能体训练的吞吐。如果这一方案可被推广，可能会重塑 AI 实验室在可抢占的 GPU 训练与有状态环境执行之间的架构划分，而这正是 Google 的 ax 项目同样在竞争的领域。 DSec 与 DeepSeek 的强化学习框架协同设计：它将有状态的 rollout 执行与可抢占的 GPU 训练解耦，并让沙箱生命周期与训练过程相协调，从而在回收空闲资源的同时保留 rollout 状态。由此推算的密度约为每节点 2300 个沙箱（约合每个硬件线程十几个），这也带来了值得关注的问题：其中有多少沙箱处于空闲状态，以及 CPU 密集与网络等待等不可预测的混合负载该如何调度。

hackernews · shenli3514 · 9月26日 18:22 · [社区讨论](https://news.ycombinator.com/item?id=49859112)

**背景**: 用强化学习训练智能体模型，需要同时运行大量相互隔离的环境（即沙箱），让模型在其中尝试任务并获取反馈；每个沙箱本质上是一个带有独立文件系统、工具和网络访问权限的容器或轻量级虚拟机。过去这类 rollout 工作往往与训练争用同一批 GPU 服务器，而沙箱执行通常是 CPU 和 I/O 密集、而非 GPU 密集的，因此这种占用并不经济。EPYC 是 AMD 的服务器 CPU 产品线，论文选择纯 CPU 节点正体现了这种分离思路；Google 开源的 ax 项目则是提供类似智能体沙箱层的同类尝试。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2609.22978">[2609.22978] DeepSeek Elastic Compute (DSec): A Sandbox Infrastructure for Effective Agentic Training at Scale</a></li>
<li><a href="https://arxiv.org/html/2609.22978v1">DeepSeek Elastic Compute (DSec): A Sandbox Infrastructure for Effective Agentic Training at Scale</a></li>
<li><a href="https://technode.com/2026/09/23/deepseek-dsec-agent-training-sandbox-infrastructure/">DeepSeek details DSec sandbox infrastructure for agent training · TechNode</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍对规模感到震撼，有人称在 160 个 EPYC 节点上运行 38 万个并发沙箱“太疯狂了”。也有人对资源分配提出技术质疑：每个核心 12 个沙箱似乎过于极端，好奇其中有多少处于空闲，并指出从 PDF 转换到简单问答等不同任务的 CPU 与网络占用差异极大。还有人将其与 Google 的 ax 项目相比较；另一个反复出现的话题是论文的作者名单（131 位作者，还有 31 位甚至没列出），有评论者推测这是一种“资产保护”策略，避免竞争对手识别出具体工程师并挖走他们。

**标签**: `#DeepSeek`, `#sandboxing`, `#cloud-infrastructure`, `#distributed-systems`, `#AI/ML-infrastructure`

---

<a id="item-2"></a>
## [逆向工程揭示 Intel 8087 正切算法：不止于 CORDIC](http://www.righto.com/2026/09/8087-tangent-cordic.html) ⭐️ 8.0/10

Ken Shirriff 发表了一篇新的技术深度分析文章，通过逆向工程揭示了老式 Intel 8087 浮点协处理器计算正切函数的具体实现方式，并指出它并不只依赖人们通常认为的 CORDIC 算法。该分析深入到芯片实际的微代码与算术例程，而不是仅仅依据文档或二手资料。 这项工作的意义在于，它纠正了人们对早期浮点硬件如何实现超越函数的一个广为流传的假设，并罕见地展示了最早一批大规模商用浮点运算单元在微代码层面的设计取舍。这些发现既对计算历史研究者有价值，也对关心浮点运算在严苛硬件限制下如何真正实现的工程师有帮助。 Intel 8087 于 1980 年发布，是 8086 系列微处理器的首款浮点协处理器；而 CORDIC 是一种逐位运算的移位-相加算法，仅用加法、减法、位移和查找表即可计算三角函数等函数，通常不需要硬件乘法器。Shirriff 的考察表明，8087 的正切例程混合使用了多种技术，而非遵循纯粹的 CORDIC，这反映了在受限的硅片面积下实现高精度超越函数运算时的取舍。

rss · Lobsters · 9月26日 19:01

**背景**: Intel 8087 是 8086 微处理器系列的首款浮点协处理器，于 1980 年发布，它把加、减、乘、除和开方等浮点运算从主 CPU 中分担出来；其指令集后来演变为至今仍存在于现代 x86 芯片中的 x87 标准。CORDIC（坐标旋转数字计算机），又称 Volder 算法，是一种经典的逐位方法，仅靠移位、加法和少量查找表就能计算三角函数、双曲函数、指数和对数函数，因此对缺乏快速乘法器的早期硬件极具吸引力。由于 CORDIC 与前乘法器时代的硬件联系如此紧密，许多人想当然地认为 8087 这类芯片的所有超越函数都采用它，而这正是这篇逆向工程文章所要检验的假设。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Intel_8087">Intel 8087 - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/CORDIC_algorithm">CORDIC algorithm</a></li>
<li><a href="https://en.wikipedia.org/wiki/X87">x87 - Wikipedia</a></li>

</ul>
</details>

**标签**: `#reverse-engineering`, `#hardware`, `#floating-point`, `#intel-8087`, `#cordic`

---

<a id="item-3"></a>
## [十五年后再看 Apple Cards：被它「Sherlock」的那家创业公司](https://lexontech.org/fifteen-years-later-the-apple-cards-origin-story) ⭐️ 7.0/10

lexontech.org 发表了一篇回顾文章，重新讲述了 Apple Cards 应用的前世今生：这款「从 iPhone 打印贺卡」的服务于 2011 年与 iPhone 4S 一同发布，并在 2013 年 9 月 10 日停止运营。文中既有 Sincerely 联合创始人 Matt Brezina 的第一手叙述——他做的 Postagram 和 Sincerely Ink 才是同类应用的先行者——也披露了 Apple 如何说服美国邮政（USPS）扫描信封上仅在紫外线下可见的隐形条码来完成物流追踪。 这是「Sherlocking」（Apple 把第三方小众应用的功能直接整合进系统或自家应用）的典型案例，至今仍是独立开发者最大的恐惧之一——自己辛苦做出来的功能，Apple 可能一句话就原地复制。文章同时揭示了看似简单的消费级功能背后，隐藏着鲜为人知的印刷供应链与邮政物流改造工作。 Apple 坚持不在信封上印刷可见条码，于是与印刷合作方共同开发出一种只在特定紫外线下可见的隐形条码喷涂工艺，USPS 也同意在寄出、分拣处理和投递各环节扫描信封。文章还讨论了凸版印刷（letterpress）的细节：传统凸版追求的是轻触纸面的「kiss impression」，而 Martha Stewart 推广的压凹（debossing）之所以流行，只是因为它让消费者「看起来像」凸版印刷。

hackernews · ksec · 9月26日 09:13 · [社区讨论](https://news.ycombinator.com/item?id=49854693)

**背景**: 「Sherlocking」一词源自 Apple 的搜索工具 Sherlock：2002 年的 Sherlock 3 吸收了第三方工具 Karelia Software 的 Watson 的功能，此后这个词便泛指 Apple 在系统里内置某项功能、令原有第三方应用变得多余。Apple Cards 是一款生命周期很短的 iOS 应用，用户挑选模板、添加照片后，Apple 会代为印刷并寄出实体贺卡，该服务于 2013 年停运。Sincerely 则是位于旧金山、开发同类应用 Postagram 和 Sincerely Ink 的创业公司，其联合创始人 Matt Brezina 曾公开表示，看到 Apple 发布 Cards 时自己既恐惧又愤怒。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cnet.com/tech/services-and-software/mobile-postcard-startup-sincerely-finally-hot-now-that-apple-is-a-rival/">Mobile postcard startup Sincerely finally hot, now that Apple ... - CNET</a></li>
<li><a href="https://apple.fandom.com/wiki/Cards">Cards | Apple Wiki</a></li>
<li><a href="https://thehustle.co/sherlocking-explained">When it comes to Apple , Sherlocking is a nail-biter for app developers.</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的评论基本认可文章的「被 Sherlock」叙事——Sincerely 联合创始人 solfox 回忆 2011 年那场发布会时说自己既恐惧又愤怒，觉得 Apple 是在用自身影响力抢走他们的创意；也有人（jasongi）借机吐槽「创始人主导」公司被过度美化的叙事与创业牺牲。读者还热衷于其中的技术冷知识，称赞那个隐形条码与 USPS 的细节，争论凸版印刷与压凹的审美差异，并怀念 Cards 是给不上网的老年亲戚随手寄度假照片的顺滑体验。

**标签**: `#Apple`, `#product history`, `#startups`, `#Sherlocked`, `#Hacker News`

---

<a id="item-4"></a>
## [Drawgent：直接在实时 Excalidraw 画布上绘图的编码智能体](https://tangled.org/yanndegat.tngl.sh/drawgent) ⭐️ 7.0/10

Drawgent 是一个新的编码智能体，它可以直接在实时的 Excalidraw 画布上绘制并操作图形，也就是说智能体的修改会以画布元素的形式呈现，而不是导出成静态图片。该项目发布在 Tangled 上，很快获得关注，在开发者社区中拿到 143 分和约 40 条评论。 它处在两股快速发展潮流的交汇处——能够操作真实工具的 AI 智能体，以及共享的可视化工作空间——并表明智能体可以成为人类正在编辑的同一块画布上的实时协作者。这对进行架构设计、白板讨论和文档编写的工程团队很有意义，因为图往往正是大家一起推演的核心产物。 关键的技术差异在于 Drawgent 操作的是实时画布，而不是只输出文件或图片，因此可以做到增量式、交互式的修改；讨论中提到 Excalidraw 本身已经提供了官方开源的 MCP 端点和服务器，这意味着智能体可以直接接入这一标准接口，而不必重新实现。与任何由智能体驱动的绘图一样，输出质量仍取决于所用模型以及如何提示和约束智能体。

hackernews · parasitid · 9月26日 15:56 · [社区讨论](https://news.ycombinator.com/item?id=49857729)

**背景**: Excalidraw 是一款开源、基于浏览器的虚拟白板，以手绘风格、实时多人协作和端到端加密会话著称。MCP（Model Context Protocol，模型上下文协议）是 Anthropic 推出的开放标准，用于通过统一接口把 LLM 应用连接到外部数据源和工具，取代各自为政的碎片化集成。Mermaid 则是一种竞争路线：它从纯文本描述生成图表，而非在画布上自由操作，一些开发者认为这种形式更容易让智能体稳定产出结果。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Excalidraw">Excalidraw</a></li>
<li><a href="https://en.wikipedia.org/wiki/Model_Context_Protocol">Model Context Protocol - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Mermaid_(software)">Mermaid (software) - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 整体情绪积极但务实：有评论者指出 Excalidraw 已经提供了官方开源的 MCP 端点和服务器；也有人认为较新的 Claude 模型（通过 Claude Code 或 Obsidian 的 Excalidraw 插件）无需额外工具就能生成 Excalidraw 图。一位持批评态度的评论者表示，在尝试过多种白板集成方案以协作处理架构之后，包括 Excalidraw 在内的方案都不够理想，最终认为 Mermaid 才是对智能体最友好的媒介。最尖锐的质疑是：画图的价值来自它迫使人类进行的思考，而不是最终产物本身，这就让人怀疑智能体自动生成的图究竟能带来多少真正价值。

**标签**: `#ai-agents`, `#excalidraw`, `#mcp`, `#diagramming`, `#developer-tools`

---

<a id="item-5"></a>
## [Haskell 文章探讨 LLM 时代如何保持编程乐趣并引发热议](https://discourse.haskell.org/t/how-to-keep-enjoying-programming-in-a-world-of-llms/14705) ⭐️ 7.0/10

一篇发表在 Haskell Discourse 上的文章《How to keep enjoying programming in a world of LLMs》引发了 Hacker News 讨论，获得 215 分和 263 条评论。讨论围绕 LLM 辅助工作流究竟是保留还是侵蚀编程的技艺、乐趣与技能展开。 它捕捉到了软件开发中日益增长的文化张力：LLM 能为常规或已有解决方案的问题提升效率，但许多开发者担心失去亲手实践的精通感与编码的内在满足感。这会影响个人职业选择、团队实践，以及编程社区在 AI 辅助时代如何界定技艺。 Hacker News 讨论中包含将手工工具修车爱好者与软件调校爱好者类比的比喻，警告将任务推给 LLM 会导致技能萎缩，以及主张效率优先于手工编码的反驳观点。原始内容并非技术突破，而是一篇观点文章，其价值来自讨论的广度与平衡性。

hackernews · signa11 · 9月26日 09:41 · [社区讨论](https://news.ycombinator.com/item?id=49854875)

**背景**: Haskell 是一种通用、静态类型、纯函数式编程语言，具有类型推断和惰性求值，以类型类和单子 I/O 等特性闻名。该文章发表在 Discourse 上；Discourse 是一个开源论坛平台，被许多开发者社区使用，包括 discourse.haskell.org 上的 Haskell 社区。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Haskell_programming_language">Haskell programming language</a></li>
<li><a href="https://en.wikipedia.org/wiki/Discourse_(software)">Discourse (software) - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者意见分化：chicken-stew 将 LLM 编码比作现代汽车调校，并称生成代码常有缺陷或浪费时间；beej71 警告把任何任务推给 LLM 都会导致技能萎缩，并举例说自己连小项目的规划都变得困难。jstrebel 主张效率优先，乐于用 LLM 处理已有解法的问题；trashface 则表示在 18 年职业生涯后准备离开编程，反映出更广泛的倦怠与幻灭。

**标签**: `#LLMs`, `#software-craftsmanship`, `#AI-assisted-development`, `#programming-culture`, `#developer-productivity`

---

<a id="item-6"></a>
## [NixOS 被移植到 Valve 的 Steam Link 串流盒上](https://feyor.sh/blog/infecting-the-steam-link-with-nixos/) ⭐️ 7.0/10

feyor.sh 上的一篇博客文章介绍了如何把 NixOS 安装到 Valve 的 Steam Link 上，用通用型 Linux 系统取代设备原有的串流固件，使其不再只是专用的游戏串流客户端，而成为一台可正常使用的 NixOS 机器。 这说明那些被锁定、已经停产的消费级硬件也能被改造成可复现、以声明式方式管理的 Linux 系统，而这类廉价二手设备正是 NixOS 与嵌入式 Linux 爱好者最喜欢“复活”的目标。这类项目同时也检验了 NixOS 及其交叉编译工具链在面对官方从未支持的硬件时究竟能走多远。 由于 Steam Link 是一台性能较弱、资源受限的设备，内存与 eMMC/闪存容量都很有限，因此这类移植通常需要自定义内核或引导程序并使用交叉编译的软件包，而不是现成的 NixOS 镜像；NixOS 官方也没有为该设备提供支持或安装镜像。NixOS 的原子升级与回滚能力在这里是一大优势，因为在嵌入式设备上一次错误的配置改动否则可能直接让系统变砖。

rss · Lobsters · 9月26日 13:45

**背景**: NixOS 是一个以 Nix 包管理器为核心的 Linux 发行版，采用纯函数式的方法：整个系统都在用 Nix 表达式语言编写的配置文件中声明，NixOS 再据此生成完整的系统配置档。这样可以实现可复现的部署、原子升级与便捷回滚，其软件包来自 Nixpkgs 仓库。Steam Link 则是 Valve 推出的小型机顶盒，用于把主机 PC 上的游戏串流到电视上；Valve 后来已停产该硬件，转而引导用户使用移动端串流应用，因此二手市场上仍有大量廉价设备可淘。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/NixOS">NixOS</a></li>
<li><a href="https://en.wikipedia.org/wiki/Steam_Link">Steam Link - Wikipedia</a></li>

</ul>
</details>

**标签**: `#NixOS`, `#Steam Link`, `#embedded Linux`, `#hardware hacking`, `#homebrew`

---

<a id="item-7"></a>
## [Valve 在 Steam 测试版中引入低延迟视频编解码器 Pyrowave](https://www.phoronix.com/news/Valve-Steam-Beta-Pyrowave) ⭐️ 7.0/10

Valve 在 Steam 客户端测试版中引入了 Pyrowave，这是一个实验性视频编解码器，专为高带宽、低延迟的视频串流而设计，主要面向 Steam 远程同乐（Remote Play）。它目前只是测试版中的一个可选实验项，而非默认的编码选项。 游戏串流对延迟极为敏感，而 H.264、HEVC、AV1 等主流编解码器更注重压缩率而非端到端延迟，因此一个专门为快速编解码而设计的方案有望明显改善 Steam 远程同乐和 Steam Deck 用户的响应体验。如果 Pyrowave 能从测试阶段走向成熟，还可能影响 Valve 在云游戏和家庭内串流上的技术路线，与 NVIDIA 等厂商的专有串流方案形成对照。 Pyrowave 有意避开了现代编解码器中常见的延迟来源，例如 B 帧和灵活的码率控制，以牺牲压缩效率来换取速度，因此需要明显更高的带宽。它目前仍处于实验阶段，需要在 Steam 客户端测试版中手动启用，而且这次公告本身几乎没有提供性能基准或硬件支持方面的细节。

rss · Lobsters · 9月27日 03:41

**背景**: 视频编解码器通过压缩每一帧（以及帧与帧之间的差异）来高效地传输或存储视频；H.264、HEVC、AV1 等编解码器之所以能达到很高的压缩率，部分原因是使用了前向预测、B 帧和自适应码率控制，而这些技术都会带来延迟。在游戏串流中，一帧画面需要在几毫秒内完成采集、编码、传输、解码和显示，因此低延迟比文件体积更重要。Pyrowave 正是为这一场景而生，由开源图形开发者 themaister 设计，他于 2025 年中期发布了关于该编解码器的详细技术文章。Steam 远程同乐允许玩家把一台 PC 上运行的游戏串流到另一台设备，包括手机或 Steam Deck。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://themaister.net/blog/2025/06/16/i-designed-my-own-ridiculously-fast-game-streaming-video-codec-pyrowave/">I designed my own ridiculously fast game streaming video codec ...</a></li>
<li><a href="https://www.phoronix.com/news/Valve-Steam-Beta-Pyrowave">Valve Introduces Pyrowave Video Codec In Beta For Low... - Phoronix</a></li>
<li><a href="https://www.gamingonlinux.com/2026/09/steam-beta-adds-experimental-new-pyrowave-video-codec-for-remote-play/">Steam Beta adds experimental new Pyrowave video codec for...</a></li>

</ul>
</details>

**标签**: `#Valve`, `#video codec`, `#low latency streaming`, `#Steam`, `#beta`

---

<a id="item-8"></a>
## [p5.js 引入计算着色器，用于教授 GPU 编程](https://www.davepagurek.com/blog/p5-compute-shaders/) ⭐️ 7.0/10

Dave Pagurek 发布的一篇新博客文章介绍了如何借助计算着色器在 p5.js 中教授 GPU 编程，把这一面向初学者的创意编程库从传统的绘图与动画 API 扩展到通用 GPU 计算领域。文章建立在 p5.js 已有的 WebGPU 支持工作之上，展示如何通过学生已经熟悉的 sketch 工作流来使用计算着色器。 计算着色器过去通常需要 OpenGL、Vulkan 或 CUDA 等底层图形 API，对课堂教学而言门槛过高；而通过 p5.js 开放这些能力可以降低门槛，让学生无需先掌握完整图形管线就能学习 GPU 并行思维。这也表明 WebGPU 正逐渐成熟到足以支撑浏览器端创意编程进行真正的 GPGPU 计算，可能会改变 GPU 与数据并行计算的教学方式。 该方案依赖 WebGPU 后端而非较旧的 WebGL 渲染器，因为计算着色器是 WebGPU 的特性，WebGL 并不提供；读者需注意各浏览器对 WebGPU 的支持仍不均衡，因此课堂使用依赖较新版本的 Chrome、Edge 或其他支持该特性的浏览器。由于这是博客文章而非正式的功能发布公告，它更像是一份面向教学的教程，可能会随着 p5.js 官方 API 的演进而落后。

rss · Lobsters · 9月27日 00:28

**背景**: p5.js 是一个免费开源的 JavaScript 库，用于在网页上绘图、素描和制作动画，因其把大部分底层细节隐藏在 setup()、draw() 等简单函数之后，被广泛用于学校教育和艺术编程社区。计算着色器是一种在常规渲染管线之外运行于 GPU 上的程序，可让开发者在数千个 GPU 核心上同时执行大规模并行的通用算法。WebGPU 是继 WebGL 之后更新的 Web API，让浏览器能够使用包括计算着色器在内的现代 GPU 特性，并且既可用于 JavaScript，也可用于 Rust、C++ 等原生语言。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/WebGPU">WebGPU - Wikipedia</a></li>
<li><a href="https://developer.mozilla.org/en-US/docs/Web/API/WebGPU_API">WebGPU API - MDN Web Docs - Mozilla</a></li>
<li><a href="https://docs.unity3d.com/530/Documentation/Manual/ComputeShaders.html">Compute Shaders - Unity - Manual</a></li>

</ul>
</details>

**标签**: `#GPU programming`, `#p5.js`, `#compute shaders`, `#WebGPU`, `#creative coding`

---

<a id="item-9"></a>
## [2026 年 Rust 中 SIMD 的现状](https://shnatsel.github.io/state-of-simd-rust-2026/) ⭐️ 7.0/10

Sergey "Shnatsel" Davidoff 发布了题为《2026 年 Rust 中 SIMD 的现状》的综述文章，梳理了 Rust 生态中 SIMD 支持、工具链与最佳实践的演进情况。文章认为 Rust 的 SIMD 支持已经大幅成熟，但可移植 SIMD（std::simd）在 Rust 1.97.1 中仍属于 nightly 专属的实验性 API（feature portable_simd，issue #86656）。 SIMD 是系统编程中提升性能的核心手段，因此厘清当前工具链现状，能帮助性能与系统工程师判断该使用厂商 intrinsics、依赖自动向量化，还是押注可移植 SIMD。std::simd 历经多年仍未稳定，也意味着库作者短期内难以确定其稳定时间表，这直接影响当下 crate 如何设计各自的 SIMD 后端。 除 std::simd 与编译器自动向量化之外，Rust 中几乎所有 SIMD 代码都建立在 SIMD intrinsics 之上，这类 intrinsic 被设计为清晰对应特定的 CPU 指令；而 std::simd 提供的是不绑定任何特定硬件架构的可移植抽象，但需要 nightly 编译器。在 aarch64、arm、thumb 等 ARM 系列目标上，neon 特性通常默认不启用，除非显式写入 target 字符串，因此开发者必须主动开启才能获得 SIMD 能力。

rss · Lobsters · 9月26日 08:28

**背景**: SIMD（单指令多数据）让一条 CPU 指令同时处理多个数值，因此被广泛用于编解码、密码学、数值计算与解析类库中。Rust 提供三条主要使用路径：通过 core::arch 模块暴露的厂商 intrinsics、编译器对普通循环自动进行的自动向量化，以及由 rust-lang portable-simd 工作组开发、以 std::simd 形式提供的可移植 SIMD。可移植 SIMD 的目标是让同一份源码在多种架构上编译出高效的向量指令，而不必强迫开发者编写特定架构的 intrinsic 代码。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://shnatsel.github.io/state-of-simd-rust-2026/">The state of SIMD in Rust in 2026 | Sergey "Shnatsel" Davidoff</a></li>
<li><a href="https://doc.rust-lang.org/std/simd/index.html">std::simd - Rust</a></li>
<li><a href="https://github.com/rust-lang/portable-simd">GitHub - rust-lang/portable-simd: The testing ground for the future of portable SIMD in Rust · GitHub</a></li>

</ul>
</details>

**标签**: `#Rust`, `#SIMD`, `#performance`, `#systems programming`, `#programming languages`

---

<a id="item-10"></a>
## [GitHub 通过刻意增加 CSS 体积来提升站点性能](https://github.blog/engineering/architecture-optimization/improving-site-performance-by-shipping-more-css/) ⭐️ 7.0/10

GitHub 工程博客在 2026 年 9 月下旬发布了一篇文章，介绍团队如何通过刻意增加 CSS 体积（而不是一味地精简它）来提升站点性能。根据聚合站点摘要，这次优化针对的是大型 Pull Request 页面——对多数用户而言体验很快，但在查看超大 PR 时性能会明显下降。 这一做法与前端领域长期以来的共识——CSS 越少站点越快——正好相反，因此可能促使其他工程团队重新审视关于阻塞渲染样式表和资源体积的假设。由于 GitHub 拥有庞大的开发者用户群，它在高流量页面上验证过的技术往往会影响其他 Web 应用的优化方式。 这种反直觉的结果很可能源于字节数之外的权衡：更大的样式表可以消除昂贵的运行时工作，例如由 JavaScript 驱动的样式计算、反复的样式重算，或交互过程中的布局抖动。该文章属于 GitHub 架构与优化方向的一篇深度案例研究，因此具体机制与限制条件应以原文为准，而不应凭猜测。

rss · Lobsters · 9月27日 07:15

**背景**: 浏览器会把 CSS 视为阻塞渲染的资源：在绘制页面之前必须先下载样式表，因为没有样式的页面几乎无法使用，这也是“把关键 CSS 内联到文档头部、其余样式延后或精简”这一常见建议的由来。通常所说的 CSS 优化，是指删除未使用的规则，以减少阻塞渲染的时间并尽可能降低浏览器重排的次数。GitHub 的文章表明，在某些复杂且高度交互的应用中，提前增加 CSS 可以把工作从关键交互路径上移走，从而获得净收益。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://web.dev/articles/critical-rendering-path/render-blocking-css">Render-blocking CSS | Articles | web.dev</a></li>
<li><a href="https://developer.mozilla.org/en-US/docs/Learn_web_development/Extensions/Performance/CSS">CSS performance optimization - Learn web development | MDN</a></li>
<li><a href="https://techreport.ngo/performance/improving-site-performance-by-shipping-more-css/">Improving site performance by shipping more CSS | Tech Report</a></li>

</ul>
</details>

**标签**: `#web performance`, `#CSS`, `#frontend`, `#optimization`, `#GitHub`

---