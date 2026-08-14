---
layout: default
title: "Horizon Summary: 2026-08-14 (ZH)"
date: 2026-08-14
lang: zh
---

> 从 112 条内容中筛选出 23 条重要资讯。

---

1. [DRAM“意面化”攻击解锁 CPU 隐藏内存](#item-1) ⭐️ 9.0/10
2. [OpenAI 发布 GPT-5.6 构建者指南，助力更快 AI 代理](#item-2) ⭐️ 9.0/10
3. [SvelteKit 3 候选版本发布](#item-3) ⭐️ 9.0/10
4. [Gemini 3.7 Flash 发布：谷歌最强编码与智能体工作流模型](#item-4) ⭐️ 8.0/10
5. [OpenAI 与 Cerebras 宣称 GPT-5.6 Sol Ultrafast 速度提升 7 倍](#item-5) ⭐️ 8.0/10
6. [Bluesky 推出 Jetstream 等新协议服务，降低开发者门槛](#item-6) ⭐️ 8.0/10
7. [DeepSeek 发布 Harness 开发者预览版：插件优先、可追踪的智能体框架](#item-7) ⭐️ 8.0/10
8. [选择无聊的技术：善用有限的创新代币](#item-8) ⭐️ 8.0/10
9. [代码理解成为软件新瓶颈](#item-9) ⭐️ 8.0/10
10. [Pi 中的上下文压缩：面向 LLM 智能体的上下文管理](#item-10) ⭐️ 8.0/10
11. [追踪 65.7 万条链接，探究旧网络为何消失](#item-11) ⭐️ 8.0/10
12. [浙大 PhyEdit 开源：显式 3D 几何约束让平面图像编辑更精准，超越 Nano Banana Pro](#item-12) ⭐️ 8.0/10
13. [白宫科学主管呼吁改革美国科技政策，优先发展 AI 以应对中国](#item-13) ⭐️ 8.0/10
14. [Richard Hipp 2024 年演讲详解 SQLite 工作原理](#item-14) ⭐️ 8.0/10
15. [斯托尔曼论黑客行为是趣味性的巧思](#item-15) ⭐️ 8.0/10
16. [NP 难问题作为实际障碍被高估了](#item-16) ⭐️ 7.0/10
17. [Nine PBS 起诉 Iron Mountain 封锁档案数据访问](#item-17) ⭐️ 7.0/10
18. [单条日志导致 journald 在 ext4/btrfs 上产生 49KB+/110KB+ 写入](#item-18) ⭐️ 7.0/10
19. [SparrowMap 让私人摄像头追踪政府车辆](#item-19) ⭐️ 7.0/10
20. [《经济学人》力挺选择抗病与高智商胚胎](#item-20) ⭐️ 7.0/10
21. [让他们写 RFC：倡导轻量级技术提案](#item-21) ⭐️ 7.0/10
22. [用 Rust 的 Egg 库编写 SQL 优化器教程](#item-22) ⭐️ 7.0/10
23. [天文学家发现新型天体“黑洞星”，或解释宇宙“小红点”](#item-23) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [DRAM“意面化”攻击解锁 CPU 隐藏内存](https://github.com/xoreaxeaxeax/skitter-creek-bath-salts) ⭐️ 9.0/10

安全研究员 Christopher Domas 发布了“skitter-creek-bath-salts”项目，利用 DRAM 地址加扰绕过 CPU 内存保护，访问 PSP 私有内存和 SMRAM 等隐藏区域。这项工作已在 Black Hat 上展示，并在 Hacker News 和 Lobsters 上引发了广泛讨论。 这一攻击表明，DRAM 的物理寻址行为可以绕过复杂的硬件安全防护，直接影响基于 AMD Jaguar 的游戏机等平台。它让拥有 ring-0 权限的攻击者得以进入“负环”区域，动摇了人们对 CPU 隔离和可信执行环境的长期假设。 该项目使用 z3 SMT 求解器逆向 DRAM 加扰变换，生成一个“别名”地址，能在不触发平台安全检查的情况下访问受保护地址。它专门针对 AMD 16h（Jaguar）；README 中指出 Zen 3 使用不同的内存控制器基址，因此对更新 CPU 的适用性尚不明确。

hackernews · Lobsters · 8月13日 14:17 · [社区讨论](https://news.ycombinator.com/item?id=49286341)

**背景**: 现代 CPU 会对发送给 DRAM 的物理地址进行加扰，将访问分散到不同的 bank 和 row，以改善电气特性并增强安全性。这形成了内存的“意面化”视图，与软件通常看到的连贯视图不同。通过逆向加扰函数，攻击者可以找到受保护地址的别名，从而访问被围栏和锁隔开的数据。这项工作建立在 Rowhammer 等先前 DRAM 安全研究的基础上，但针对的是加扰机制本身，而非比特翻转效应。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/xoreaxeaxeax/skitter-creek-bath-salts">GitHub - xoreaxeaxeax/skitter-creek-bath-salts: Unlocking _everything_ on the CPU with DRAM scrambling · GitHub</a></li>
<li><a href="https://news.ycombinator.com/item?id=49286341">Spaghettifying DRAM | Hacker News</a></li>

</ul>
</details>

**社区讨论**: Hacker News 和 Lobsters 上的评论者反应热烈，称赞 Christopher Domas 过去的演讲，并期待 Black Hat 上的展示。一些人担心游戏机安全团队（Xbox、PlayStation）会感到紧张，另一些人则询问哪些更新型号的 CPU 受影响，并指出 README 目前只详细说明了 AMD Jaguar。

**标签**: `#security`, `#DRAM`, `#hardware hacking`, `#exploitation`, `#Black Hat`

---

<a id="item-2"></a>
## [OpenAI 发布 GPT-5.6 构建者指南，助力更快 AI 代理](https://openai.com/index/builders-guide-to-gpt-5-6) ⭐️ 9.0/10

OpenAI 发布了 GPT-5.6 的构建者指南，向初创公司展示如何利用更智能的模型选择和全新的 Responses API 功能来构建更快、更具成本效益的 AI 代理。该指南伴随 2026 年 7 月 9 日发布的 GPT-5.6 模型家族，包含 Luna、Terra 和 Sol 三个版本。 这很重要，因为 GPT-5.6 被定位为智能和效率的新标准，覆盖编码、知识工作、网络安全和科学等领域。初创公司和开发者现在有了具体指南来利用该模型和 Responses API，这可能加速 AI 代理在生产系统中的采用。 GPT-5.6 提供三个版本：Luna、Terra 和 Sol，其中 Sol 能力最强。Responses API 被推荐用于 GPT-5.4 及更新模型，提供统一接口，内置网页搜索、文件搜索、计算机使用和代码解释器等工具，适合构建类代理应用程序。

rss · OpenAI Blog · 8月13日 11:00

**背景**: GPT-5.6 是 OpenAI 开发的大型语言模型，于 2026 年 7 月 9 日发布，包含三个按能力从低到高排列的模型：Luna、Terra 和 Sol。Responses API 是构建类代理应用程序的统一接口，支持多轮交互、内置工具和外部 MCP。该构建者指南旨在帮助初创公司和开发者高效选择合适的模型版本，并利用 API 实现实际的 AI 代理应用场景。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/GPT-5.6">GPT-5.6 - Wikipedia</a></li>
<li><a href="https://openai.com/index/gpt-5-6/">GPT-5.6: Frontier intelligence that scales with your ambition | OpenAI</a></li>
<li><a href="https://developers.openai.com/api/docs/guides/migrate-to-responses">Migrate to the Responses API | OpenAI API</a></li>

</ul>
</details>

**标签**: `#GPT-5.6`, `#OpenAI`, `#AI agents`, `#API`, `#machine learning`

---

<a id="item-3"></a>
## [SvelteKit 3 候选版本发布](https://svelte.dev/blog/sveltekit-3-release-candidate) ⭐️ 9.0/10

SvelteKit 3 候选版本现已发布，标志着该框架的一个重大里程碑。此 RC 版本在稳定版发布之前引入了破坏性变更和新功能。 SvelteKit 是 Svelte 生态中广泛使用的元框架，因此这一 RC 版本对 Svelte 生态系统影响重大。开发者现在可以测试即将推出的更改，并为下一个主要版本做好准备。 作为候选版本，此版本预计接近最终版本，但仍可能有一些额外更改。公告中除了里程碑状态外，没有详细说明具体的破坏性变更和新功能。

rss · Lobsters · 8月13日 19:08

**背景**: Svelte 是一个用于构建用户界面的组件框架，而 SvelteKit 是构建在 Svelte 之上的应用框架，类似于 Next.js 之于 React。SvelteKit 处理路由、服务端渲染和其他全栈问题，是构建 Web 应用的综合性工具。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://svelte.dev/tutorial/kit/introducing-sveltekit">Introduction / What is SvelteKit ? • Svelte Tutorial</a></li>
<li><a href="https://pgm-2425-itexploration.github.io/syllabus/tutorials/full-stack/sveltekit.html">SvelteKit | PGM IT Exploration</a></li>

</ul>
</details>

**标签**: `#Svelte`, `#SvelteKit`, `#JavaScript`, `#Framework`, `#Release`

---

<a id="item-4"></a>
## [Gemini 3.7 Flash 发布：谷歌最强编码与智能体工作流模型](https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-3-7-flash/) ⭐️ 8.0/10

Google DeepMind 发布了 Gemini 3.7 Flash，这是其面向编码和智能体的最强工作流模型，距 3.6 Flash 发布仅三周。该模型具备强大的视觉能力，并提供计划于 2026 年 12 月 31 日翻倍的初始优惠定价。 这一发布对 AI/ML 从业者意义重大，因为它以更低的成本让先进的多模态推理更易用，同时提升了在 DeepSWE 等基准上的性能。它延续了谷歌在竞争激烈的 LLM 市场中快速迭代的节奏，但并非范式转变。 该模型在推理、编码、智能体工具使用、多模态、多语言和长上下文基准上进行了评估。社区测试显示其图像到 HTML 的转换能力很强，但 Opus 5 仍被认为是最佳；评论者还指出 Luna 更便宜，可能会削弱 Flash 的性价比优势。

hackernews · thisisauserid · 8月13日 17:23 · [社区讨论](https://news.ycombinator.com/item?id=49289112)

**背景**: Gemini 是 Google DeepMind 开发的多模态大语言模型家族，于 2023 年 12 月发布。Flash 系列被设计为低成本、高吞吐量的“工作流”型模型，适用于摘要、解析和格式化等任务，强调性价比和速度。Gemini 3.7 Flash 在此基础上增强了推理和智能体能力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-3-7-flash/">Gemini 3 . 7 Flash : our most intelligent workhorse model</a></li>
<li><a href="https://deepmind.google/models/model-cards/gemini-3-7-flash/">Gemini 3 . 7 Flash - Model Card — Google DeepMind</a></li>
<li><a href="https://ai.google.dev/gemini-api/docs/models/gemini-3.7-flash">Gemini 3 . 7 Flash | Gemini API | Google AI for Developers</a></li>

</ul>
</details>

**社区讨论**: 社区成员积极对该模型进行基准测试：一位测试者发现 Gemini 3.7 在图像转 HTML 任务上表现良好，但 Opus 5 仍是最佳；Simon Willison 则指出了将于 2026 年 12 月 31 日翻倍的奇怪定价安排。还有人认为 Luna/Terra 更便宜，削弱了 Flash 的存在意义，并根据 DeepSWE 基准推荐使用 Luna (Xhigh)。

**标签**: `#AI`, `#Google`, `#Gemini`, `#LLM`, `#Models`

---

<a id="item-5"></a>
## [OpenAI 与 Cerebras 宣称 GPT-5.6 Sol Ultrafast 速度提升 7 倍](https://www.cerebras.ai/blog/accelerating-gpt-5-6-sol-ultrafast-with-openai) ⭐️ 8.0/10

OpenAI 与 Cerebras 发布了 GPT-5.6 Sol Ultrafast，这是一个新的服务层级，运行 GPT-5.6 Sol 的速度比标准处理最多快 14 倍。在 Cerebras 的基准测试中，Ultrafast 在 11 小时 11 分钟内回答了全部 2500 道 HLE 问题，而 Claude Fable 5 则需要 78 小时 27 分钟，准确率接近相同，速度快约 7 倍。 这可能使推理速度成为前沿 AI 模型的关键竞争因素，打开更快速的迭代空间，并让法律简报、金融模型和工程报告等具有经济价值的任务能在更短时间内完成。它还表明，OpenAI 与 Cerebras 这类合作能把前沿模型的质量与专用硬件结合起来，改变用户对 API 推理服务的预期。 这一加速由 Cerebras 的晶圆级引擎（wafer-scale engine）驱动，它使用单个大型处理器并具备高片内内存和带宽。OpenAI 的公告称 Ultrafast 将首先在 OpenAI API 中推出，但尚未公布定价细节，而且两篇博文也没有明确确认其在所有基准上都能与标准 GPT-5.6 Sol 保持完全一致的准确率。

hackernews · pr337h4m · 8月13日 18:10 · [社区讨论](https://news.ycombinator.com/item?id=49289844)

**背景**: Cerebras 生产晶圆级引擎（Wafer-Scale Engine）——全球最大的 AI 处理器，为深度学习工作负载提供快速推理与训练。GPT-5.6 Sol 是 OpenAI 面向复杂推理和知识工作的前沿模型，Ultrafast 是一个预览服务层级，其回复生成速度远快于标准处理。HLE 等前沿推理基准通过跨学科的高难度专家级问题来考验模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cerebras.ai/blog/accelerating-gpt-5-6-sol-ultrafast-with-openai">Accelerating GPT-5.6 Sol Ultrafast with OpenAI</a></li>
<li><a href="https://openai.com/index/previewing-ultrafast/">Previewing Ultrafast mode: GPT-5.6 Sol at up to 14X the speed | OpenAI</a></li>
<li><a href="https://en.wikipedia.org/wiki/Cerebras_Systems">Cerebras Systems - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者总体上对加速感到兴奋，但对部分说法持怀疑态度。有人称赞 OpenAI 与 Cerebras 的合作，并认为更快的推理能提升思考质量，因为迭代更快；也有人指出两篇博文都没有明确确认与标准模型性能完全一致，而且缺少定价信息。

**标签**: `#AI`, `#Inference Speed`, `#OpenAI`, `#Cerebras`, `#Benchmarks`

---

<a id="item-6"></a>
## [Bluesky 推出 Jetstream 等新协议服务，降低开发者门槛](https://atproto.com/blog/introducing-bluesky-protocol-services) ⭐️ 8.0/10

Bluesky 宣布推出一套协议服务，其中包括 Jetstream，一种简化 AT Protocol 数据洪流（firehose）访问的新流式消费服务。该公告发布在 AT Protocol 官方博客上，旨在进一步降低开发者基于该协议构建应用的难度。 这一进展显著降低了开发者在 AT Protocol 上构建实时功能（如订阅源生成器、机器人和分析工具）的门槛。通过提供更易用的数据洪流消费方式，Bluesky 强化了其开放生态系统，并鼓励更多第三方创新。 Jetstream 采用 Go 实现，开源且可自托管，它从数据洪流中摄取数据，并将 CBOR 编码的数据块转换为更易处理的轻量 JSON。它附带了官方的 Go 客户端库，并已有社区客户端库；用户甚至可以直接在浏览器中消费该流，无需专用服务器。

hackernews · danabramov · 8月14日 00:14 · [社区讨论](https://news.ycombinator.com/item?id=49293324)

**背景**: AT Protocol 是一种用于构建社交应用的去中心化联合协议，为 Bluesky 提供支持，并支持应用间的账户可迁移性。数据洪流（firehose）是一个经过认证的事件流，包含帖文、点赞、关注、用户名变更等事件，用于在网络中同步用户数据，但直接消费它技术要求较高。Jetstream 通过提供更易用的 JSON 友好接口解决了这一问题，让更广泛的开发者群体能够更轻松地使用实时数据。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.bsky.app/blog/jetstream">Introducing Jetstream | Bluesky</a></li>
<li><a href="https://docs.bsky.app/docs/advanced-guides/firehose">Firehose | Bluesky</a></li>
<li><a href="https://en.wikipedia.org/wiki/AT_Protocol">AT Protocol - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: Simon Willison 称赞了 Jetstream 的简洁性，指出无需服务器即可直接在浏览器中消费，并分享了他更新的演示。其他评论者则讨论了页面所用文档系统等周边话题，还提出了一项雄心勃勃的设想——在 Bluesky 数据洪流之上重建 DNS；同时，也有评论者对近期服务中断及平台在服务状态上的透明度表示担忧。

**标签**: `#atproto`, `#bluesky`, `#decentralized`, `#protocol`, `#firehose`

---

<a id="item-7"></a>
## [DeepSeek 发布 Harness 开发者预览版：插件优先、可追踪的智能体框架](https://deepseek.com/harness/en/) ⭐️ 8.0/10

DeepSeek 在 GitHub 上以 MIT 许可证发布了 DeepSeek Harness 的早期开发者预览版。该 harness 采用由 Cordis 驱动的“一切皆插件”架构，并拥有可追踪的会话日志，记录模型看到的每个事件。 智能体 harness 是将 AI 模型变成实用智能体的关键层，而 DeepSeek Harness 在众多专有智能体模糊其追踪记录的情况下，提供了一个完全开放、可追踪的替代方案。其插件优先的设计可降低开发者自定义智能体行为的“fork 成本”，而社区的高度关注也表明市场对透明智能体基础设施的强烈需求。 该预览版依赖 Cordis v4 插件系统，支持热重载，并在卸载插件时可回滚状态和副作用。会话日志是仅追加的，记录系统提示、推理、工具调用、子智能体调度和上下文注入，并支持在同一事件流上进行恢复、分叉、搜索和重放。

hackernews · bjin · 8月13日 12:58 · [社区讨论](https://news.ycombinator.com/item?id=49285244)

**背景**: AI 智能体 harness 是 AI 模型周围的软件层，它将模型从文本生成器转变为可工作的智能体，负责处理工具、记忆和智能体循环。可追踪的会话日志对于调试和审计智能体行为非常重要。“一切皆插件”意味着从工具到 UI 组件的每项能力都可以在运行时替换或重组，这与单体式智能体框架不同。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.deepseek.com/harness/en/">DeepSeek Harness developer preview: Everything is a plugin</a></li>
<li><a href="https://explainx.ai/blog/deepseek-harness-v0-1-plugin-first-agent-stack-august-2026">DeepSeek Harness v0.1: Run the Plugin-First Stack | explainx.ai</a></li>
<li><a href="https://www.x-cmd.com/install/deepseek-harness/">deepseek - harness : Swap Any Agent... | X-CMD | deepseek - harness</a></li>

</ul>
</details>

**社区讨论**: 社区反应热烈但看法不一。作者表示这是早期预览版，欢迎反馈；一些评论者称赞可追踪的会话日志是“杀手级功能”，认为美国模型不具备这一能力。其他人则对插件方式表示怀疑，提到“插件疲劳”，并争论热重载能力是否真正有用。

**标签**: `#deepseek`, `#agent-harness`, `#ai`, `#open-source`, `#developer-tools`

---

<a id="item-8"></a>
## [选择无聊的技术：善用有限的创新代币](https://mcfunley.com/choose-boring-technology) ⭐️ 8.0/10

Dan McKinley 在 2015 年发表的《选择无聊的技术》一文中提出，公司应默认采用成熟、无聊的技术，并将有限的“创新代币”只花在真正能形成差异化的领域。文章引入了一个概念：每家公司大约只有三枚创新代币可用于尝试新的或未经充分验证的技术。 这篇文章已成为技术战略和工程管理领域的经典参考，帮助团队权衡利弊并向上级和同事解释这些取舍。“创新代币”的框架至今仍被广泛使用，包括在讨论何时采用 AI 智能体等新技术时。 文章并未完全禁止新技术，而是建议新技术在采用前必须通过一系列“考验”标准。“三枚代币”是一个示意性的限制，旨在迫使团队分清主次；这篇文章部分是对 2010 年代初期 JavaScript 框架频繁更迭的回应。

hackernews · tosh · 8月13日 17:48 · [社区讨论](https://news.ycombinator.com/item?id=49289512)

**背景**: “创新代币”是 Dan McKinley 推广的一个比喻：每家公司大约有三枚代币，每当你选择一门新的或非标准的技术，就会花掉一枚。选择“无聊”的技术——即成熟、被广泛采用、理解充分的技术——不需要花费代币，这样你就能把代币留给真正让产品与众不同的地方。这个想法帮助工程师和管理者避免因太多新奇工具而陷入复杂性泥潭。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://mcfunley.com/choose-boring-technology">Dan McKinley :: Choose Boring Technology</a></li>
<li><a href="https://www.lessannoyingbusiness.com/post/innovation-tokens">Innovation Tokens - When to break from the status quo</a></li>
<li><a href="https://jadon.us/posts/notes-on-choose-boring-technology/">Notes on - Choose Boring Technology by Dan McKinley</a></li>

</ul>
</details>

**社区讨论**: 评论区大多对这篇文章表示赞赏，有人称“创新代币”是他职业生涯中最好用的概念之一。也有人提出反驳，认为这个比喻过于随意，工程师应该直接评估风险和需求，而不是用“无聊 vs. 新颖”作为粗略判断标准。还有人指出这篇文章是对 JavaScript 框架更迭潮流的自然回应，并有人将该观点放到 AI 智能体时代重新审视。

**标签**: `#software engineering`, `#technology strategy`, `#innovation`, `#engineering management`

---

<a id="item-9"></a>
## [代码理解成为软件新瓶颈](https://www.geoffreylitt.com/2026/07/02/understanding-is-the-new-bottleneck) ⭐️ 8.0/10

文章指出，随着 LLM 生成更多代码，软件开发的关键瓶颈正从编写代码转向理解代码。它强调人类现在必须理解日益增长的机器编写代码。 这种重新定义很重要，因为它将注意力和投资引向代码理解工具、开发者教育以及支持阅读和推理代码的实践。它影响着工程师、工程领导者以及 AI 辅助开发工具的构建者。 文章据称通过互动测验和示例展示了即使对有经验的工程师来说，代码理解也会多么迅速地失效。它认为这个问题在 LLM 出现之前就已存在，但被 LLM 放大，因为 LLM 生成的代码往往缺乏明确的动机或解释性上下文。

hackernews · sebg · 8月13日 18:47 · [社区讨论](https://news.ycombinator.com/item?id=49290299)

**背景**: 程序理解是计算机科学中研究软件工程师如何维护和扩展现有源代码的领域，包括所涉及的认知过程。阅读代码、构建心智模型和追踪依赖关系是这一过程的核心活动。LLM 通过生成大量看似合理但又不透明的代码加剧了这一挑战，使人类理解成为一种日益关键且稀缺的资源。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Program_comprehension">Program comprehension</a></li>
<li><a href="https://grokipedia.com/page/code_reading">Code Reading</a></li>

</ul>
</details>

**社区讨论**: 评论者意见不一：有人同意理解是瓶颈，而另一些人则认为 LLM 本身才是真正的问题。几位评论者指出，LLM 生成的 PR 描述缺乏动机且不受欢迎，依赖 LLM 来理解代码可能意味着信任错误的解释。另一种观点认为这个问题先于 LLM 存在，本质上是工程管理和程序理解这一长期存在的挑战。

**标签**: `#LLM`, `#software engineering`, `#code understanding`, `#developer tools`, `#program comprehension`

---

<a id="item-10"></a>
## [Pi 中的上下文压缩：面向 LLM 智能体的上下文管理](https://earendil.com/posts/compaction-in-pi/) ⭐️ 8.0/10

EARENDIL 上的一篇技术文章解释了 Pi 中上下文压缩（compaction）的工作原理，详细说明了何时触发压缩以及如何通过摘要（summarization）压缩对话历史。该文章引发了社区关于压缩与剪枝（pruning）、提示缓存（prompt caching）等上下文管理策略的比较讨论。 随着 LLM 智能体处理越来越复杂的任务，高效的上下文管理变得至关重要；Pi 的压缩技术有助于智能体在有限的上下文窗口内运行而不丢失关键信息。围绕剪枝和缓存权衡的讨论，也在塑造构建高性价比、长期运行的智能体工作流的最佳实践。 Pi 中的压缩依赖摘要来降低上下文占用，并在对话接近模型上下文上限时触发。社区成员指出，提示缓存为压缩带来了成本权衡，一些人建议改用剪枝低价值消息，或使用双 KV 缓存（dual KV caches）在生成的同时并行执行摘要。

hackernews · tosh · 8月13日 17:57 · [社区讨论](https://news.ycombinator.com/item?id=49289654)

**背景**: 大型语言模型（LLM）有固定的上下文窗口——即模型在生成回答时能“看到”的文本量。长时间的智能体对话很快会填满这个窗口，因此像 Pi 这样的工具会把较早的消息压缩成摘要，以保留关键信息并腾出空间。提示缓存（prompt caching）是一种相关技术，它存储并复用先前请求的计算来降低延迟和成本，但可能与压缩产生冲突，因为改变提示会破坏缓存。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://earendil.com/posts/compaction-in-pi/">How Compaction Works in Pi | EARENDIL</a></li>
<li><a href="https://outcomeschool.com/blog/how-does-context-compaction-work">How does context compaction work ?</a></li>
<li><a href="https://www.ibm.com/think/topics/prompt-caching">What is Prompt Caching? - IBM</a></li>

</ul>
</details>

**社区讨论**: 评论者围绕压缩的替代方案展开争论：有人倾向于剪枝低价值消息以保留原意，有人建议保持上下文利用率在 30% 以下以从根本上避免压缩，还有人指出提示缓存使激进的压缩成本高昂。一位本地 LLM 用户分享了双 KV 缓存的技巧来并行摘要，另一位评论者则对现有所有方案表示不满。

**标签**: `#LLM`, `#context-management`, `#compaction`, `#AI-agents`, `#prompt-caching`

---

<a id="item-11"></a>
## [追踪 65.7 万条链接，探究旧网络为何消失](https://0.mk/blog/link-rot) ⭐️ 8.0/10

一篇数据驱动的博客文章报道，研究人员追踪了 657,607 个链接，以量化和分析旧网络的消失，为大规模链接腐烂提供了具体证据。这项调查在 Hacker News 上引发了 129 条关于网络历史与衰退的评论。 这很重要，因为它将一种广泛感受到但模糊理解的现象——在线内容的短暂性——转化为硬数据，提高了对数字保存的认识。它影响着依赖网络作为记忆和证据的历史学家、学者以及普通用户，并凸显了网络存档的紧迫性。 该调查专门追踪了 657,607 个链接，以查看有多少已失效或被重定向，得出了链接腐烂率的详细统计。这篇博客文章还引发了一场激烈的辩论，讨论“旧网络”究竟何时结束，评论提出的时间线从 Google 出现之前到短短几年前不等。

hackernews · tdx · 8月13日 17:49 · [社区讨论](https://news.ycombinator.com/item?id=49289532)

**背景**: 链接腐烂是指超链接逐渐无法指向原始目标的现象，因为相关资源被移动或删除，这被视为对数字保存的公认威胁。研究对链接腐烂率的估计差异很大，但这个问题对法律系统、学术研究和历史记录都意义重大。“旧网络”通常指早期去中心化的互联网时代，那时以个人博客和独立网站为主，尚未被大型社交平台统治。这项调查旨在衡量有多少旧网络已经消失。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Link_rot">Link rot</a></li>
<li><a href="https://en.wikipedia.org/wiki/Wikipedia:Link_rot">Wikipedia:Link rot - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者们对“旧网络”给出了不同定义：有人认为它终结于 Facebook 崛起之时，有人以 Google 搜索的出现为分界线，还有人调侃道，称 2009–2014 年为“旧网络”让自己感觉自己老了。一条令人难忘的评论提到了“布兰妮·斯皮尔斯的半导体物理指南”，认为它是那个时代尚存的遗物。整体氛围怀旧且略带反叛，甚至有人提出旧网络或许还会回归。

**标签**: `#link rot`, `#web history`, `#internet archaeology`, `#data analysis`, `#digital preservation`

---

<a id="item-12"></a>
## [浙大 PhyEdit 开源：显式 3D 几何约束让平面图像编辑更精准，超越 Nano Banana Pro](https://mp.weixin.qq.com/s?__biz=MzIzNjc1NzUzMw==&mid=2247912028&idx=4&sn=c106858467e16b7df780265696c61fe3) ⭐️ 8.0/10

浙江大学 ReLER 团队开源了 PhyEdit，该框架已被 ACM MM 2026 接收，利用显式 3D 几何预览来指导基于 DiT 的图像编辑。与 Google DeepMind 的 Nano Banana Pro 相比，PhyEdit 在平面图像编辑任务上的 3D 相关指标更高。 这项工作通过引入显式 3D 几何约束，直接解决了 AI 图像编辑中长期存在的基于文本“盲猜”的瓶颈。它让模型能更好地处理物体远近、尺度、遮挡以及多物体操作，有望惠及学术研究和商业编辑工具。 PhyEdit 将几何运动预览与 Qwen-Image-Edit 相结合，以提高图像编辑过程中的几何准确性和物理一致性。开源代码已发布在 GitHub 上，相关论文已被 ACM MM 2026 接收。

rss · 量子位 · 8月13日 07:38

**背景**: 传统的 AI 图像编辑模型通常在潜在空间中运作，仅依赖文本提示，缺乏显式 3D 理解，导致物体尺度、位置和遮挡容易出错。基于 DiT（Diffusion Transformer）的编辑器提升了语义质量，但仍难以保证几何精度。显式 3D 约束为模型提供了清晰的空间结构，从而支持更可控且物理上合理的编辑。Nano Banana Pro 是 Google DeepMind 推出的 Gemini 3 Pro 图像模型，是图像生成与编辑领域的强大商业基线。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.51cto.com/article/852945.html">ACM MM'26 | 3D指标超过Nano Banana Pro！浙大开源方案让AI在平面图像...</a></li>
<li><a href="https://github.com/nenhang/PhyEdit">GitHub - nenhang/PhyEdit: [ACMMM 2026] PhyEdit: Towards Real ...</a></li>
<li><a href="https://deepmind.google/models/gemini-image/pro/">Gemini 3 Pro Image – Nano Banana Pro — Google DeepMind</a></li>

</ul>
</details>

**标签**: `#AI`, `#image editing`, `#3D reconstruction`, `#computer vision`, `#research`

---

<a id="item-13"></a>
## [白宫科学主管呼吁改革美国科技政策，优先发展 AI 以应对中国](https://www.economist.com/by-invitation/2026/08/13/the-case-for-overhauling-american-science) ⭐️ 8.0/10

2026 年 8 月 13 日，白宫科学主管迈克尔·克拉齐奥斯（Michael Kratsios）在《经济学人》发表的受邀评论文章中主张，美国科学必须进行彻底改革，以优先利用人工智能并在与中国的竞争中胜出。 这篇文章表明，美国科学政策可能将资金和优先事项转向人工智能以及对华地缘政治竞争。研究人员和工程师可能会在科研经费、国家科研议程以及公私研发合作方面感受到变化。 这篇评论是观点性论述而非官方政策宣布，因此没有包含具体的预算、项目或时间表。其核心主张是将美国科研精力集中于人工智能，并以在竞争中胜过中国作为衡量成功的标准。

rss · The Economist · 8月13日 13:12

**背景**: 克拉齐奥斯担任白宫科学主管，这一职位通常与白宫科技政策办公室（OSTP）相关，负责协调联邦研发工作和科学咨询。长期以来，美国科学围绕广泛的基础研究和多样化的机构使命来组织，而这篇文章主张确立更为聚焦的国家方向。这一提议正值美中科技竞争激烈之际，人工智能被视为具有战略关键地位。

**标签**: `#AI`, `#science policy`, `#US-China competition`, `#innovation`, `#research`

---

<a id="item-14"></a>
## [Richard Hipp 2024 年演讲详解 SQLite 工作原理](https://www.youtube.com/watch?v=ZSKLA81tBis) ⭐️ 8.0/10

在 2024 年的一次技术演讲中，SQLite 创始人 Richard Hipp 讲解了 SQLite 的内部工作原理，并提供了配套的幻灯片 PDF 供在线查看。演讲梳理了数据库引擎的核心组件与执行流程。 作为 SQLite 创始人的权威讲解，这场演讲为这个全球部署最广泛的数据库引擎之一提供了难得而深入的洞见。它对软件工程师、系统研究者以及任何需要维护或扩展 SQLite 的人员都很有价值。 演讲涵盖了 SQLite 的虚拟数据库引擎（VDBE）——一个基于寄存器的字节码解释器，负责执行编译后的 SQL 语句——以及负责 I/O 处理的 pager 和页缓存层。演示材料以 PDF 形式发布在 sqlite.org，相关讨论发布在 Lobsters 上。

rss · Lobsters · 8月13日 11:56

**背景**: SQLite 是一款自包含、无服务器、嵌入式的关系型数据库，广泛用于从移动设备到网页浏览器等无数应用中。它的架构将 SQL 编译与执行分离：前端把 SQL 编译成 VDBE 字节码，后端则包含 B-tree、pager 和操作系统接口层。pager 负责页面级 I/O 与缓存管理，而 VDBE 是一个基于寄存器的虚拟机，负责运行生成的字节码。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.sqlite.org/arch.html">Architecture of SQLite</a></li>
<li><a href="https://www.sqlite.org/vdbe.html">The Virtual Database Engine of SQLite</a></li>

</ul>
</details>

**标签**: `#SQLite`, `#databases`, `#database internals`, `#technical talk`, `#software engineering`

---

<a id="item-15"></a>
## [斯托尔曼论黑客行为是趣味性的巧思](https://stallman.org/articles/on-hacking.html) ⭐️ 8.0/10

Lobsters 社区正在讨论理查德·斯托尔曼的文章《On Hacking》。他在文中反思了将黑客行为视为一种趣味性巧思的观点，并探讨了这种心态在编程文化中的伦理维度。该讨论获得了 8.0 的高分，表明程序员群体对此有浓厚兴趣。 斯托尔曼是黑客文化中的奠基性人物，他对黑客行为的诠释影响了许多程序员对这一术语的理解。这场讨论将技术巧思与伦理联系起来，有助于社区区分积极的黑客行为与有害行为。 该新闻条目并未提供文章全文，主要给出了 Lobsters 上关于《On Hacking》的评论讨论串链接。文章被标记为 hacking、programming、ethics 和 hacker-culture，反映了其核心主题。

rss · Lobsters · 8月13日 07:51

**背景**: 在程序员文化中，“hacking”原本指富有趣味性和巧妙的问题解决方式，而非计算机犯罪。理查德·斯托尔曼是 GNU 项目和自由软件运动的创始人，长期以来一直倡导这一正面含义，并强调技术能力伴随的伦理责任。

**标签**: `#hacking`, `#programming`, `#ethics`, `#hacker-culture`, `#stallman`

---

<a id="item-16"></a>
## [NP 难问题作为实际障碍被高估了](https://gruhn.me/blog/2026-08-13/) ⭐️ 7.0/10

一篇博客文章提出，NP 难问题作为实际障碍被高估了，因为现实世界中的实例通常可以通过启发式算法或限制问题空间来解决。 这挑战了 NP 难问题在实践中难以解决的传统观念，鼓励从业者关注实际解决方案而非最坏情况复杂度。它凸显了理论复杂性与现实世界性能之间的差距。 这篇文章可能引用了依赖管理和类型检查等例子，这些通用上属于 NP 难问题，但由于输入受限和启发式方法，在实践中可行。它指出最坏情况实例在典型应用中很少出现。

hackernews · theanonymousone · 8月13日 20:14 · [社区讨论](https://news.ycombinator.com/item?id=49291268)

**背景**: NP 难是一个复杂度类别，指至少与 NP 中最难问题一样难的问题。目前没有已知的多项式时间算法，但这是最坏情况的描述。在实践中，许多 NP 难问题可以通过启发式算法、近似算法或施加额外约束在真实数据上高效求解。理论最坏情况复杂度与实际可解性之间的区别是这篇博客文章的核心。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/NP-hardness">NP-hardness - Wikipedia</a></li>
<li><a href="https://stackoverflow.com/questions/1857244/what-are-the-differences-between-np-np-complete-and-np-hard">What are the differences between NP, NP-Complete and NP-Hard?</a></li>
<li><a href="https://ocw.mit.edu/courses/6-046j-design-and-analysis-of-algorithms-spring-2012/f53967be74f440c4855f9472dff28a63_MIT6.046J_S12_rec10.pdf">6.046J Recitation 10: NP-hardness - MIT OpenCourseWare</a></li>

</ul>
</details>

**社区讨论**: 评论反映了健康的辩论：一些人认为复杂性理论旨在理解计算的极限，而不是劝阻现实世界的问题解决，而另一些人则同意实际实例通常避免指数级爆炸。一位评论者指出，依赖管理器和类型系统通常会消除或限制困难案例，另一位则指出近似解往往足够。

**标签**: `#complexity theory`, `#NP-hard`, `#algorithms`, `#practical computing`, `#programming`

---

<a id="item-17"></a>
## [Nine PBS 起诉 Iron Mountain 封锁档案数据访问](https://current.org/2026/08/nine-pbs-sues-iron-mountain-over-blocked-access-to-archival-data/) ⭐️ 7.0/10

Nine PBS 已对 Iron Mountain 提起诉讼，原因是该公司阻止其访问档案数据，并引发了对数据所有权和备份实践的担忧。 此案凸显了第三方档案存储的法律风险，并提出了关于异地存储数据所有权和控制权的问题。这可能会影响依赖外部供应商进行长期数据保存的公共广播机构和其他组织。 根据社区讨论，该存储系统据说属于 OSS，Iron Mountain 可能需要法院判决才能在避免进一步法律风险的情况下释放数据。最近的听证会涉及服务器设置细节，以及对数据丢失（包括内存中的解密密钥）的担忧。

hackernews · vinayakborkar · 8月13日 13:14 · [社区讨论](https://news.ycombinator.com/item?id=49285418)

**背景**: Iron Mountain 是一家成立于 1951 年的全球企业信息管理公司，提供记录管理、数据备份和异地存储服务。组织通常使用此类服务来保存档案数据，但当供应商的客户关系发生变化或面临破产风险时，可能会因所有权和合同义务产生访问争议。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Iron_Mountain_(company)">Iron Mountain (company) - Wikipedia</a></li>
<li><a href="https://www.ironmountain.com/">Iron Mountain</a></li>

</ul>
</details>

**社区讨论**: 评论者反应不一：有人免费提供存储空间，也有人为 Iron Mountain 辩护，指出其可能需要法院命令以避免法律风险。还有人强调 3-2-1 备份规则的重要性，提及第二家异地供应商的成本，并引用听证会更新，认为内存中的解密密钥可能面临风险。也有人查看后发现存储供应商 OSS 团队规模很小，对其信誉提出质疑。

**标签**: `#data-archival`, `#legal`, `#storage`, `#backup`, `#public-broadcasting`

---

<a id="item-18"></a>
## [单条日志导致 journald 在 ext4/btrfs 上产生 49KB+/110KB+ 写入](https://github.com/systemd/systemd/issues/40262) ⭐️ 7.0/10

systemd 的 GitHub 仓库中新增的 bug 报告显示，systemd-journald 处理单条日志时，在 ext4 上会产生超过 49KB 的磁盘写入，在 btrfs 上则超过 110KB。这表明 journal 文件格式存在严重的写入放大问题。 该问题暴露了 Linux 核心日志组件中的严重存储效率问题，在日志量大的环境下可能导致不必要的 SSD 磨损和磁盘空间浪费。由于 systemd-journald 被几乎所有现代 Linux 发行版使用，影响范围很广。 写入放大源于 journald 的追加式文件格式：每条新日志都会更新头部元数据，即便日志内容很小，也迫使文件系统重写整个块。该问题在 btrfs 上更严重，因为写时复制（CoW）为每次块更新增加了额外开销。

hackernews · ValdikSS · 8月13日 18:41 · [社区讨论](https://news.ycombinator.com/item?id=49290215)

**背景**: systemd-journald 是大多数现代 Linux 发行版使用的日志守护进程，负责将内核、syslog 和应用日志收集到带索引的二进制 journal 文件中。该格式为追求健壮性而设计为只追加，但每次追加都会更新文件头部，迫使文件系统重写受影响的数据块。当日志内容远小于被弄脏的块大小时，这种设计就导致写入放大问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://news.ycombinator.com/item?id=49290215">Single log line is 49KB+ (ext4) / 110KB+ (btrfs) of systemd- journald ...</a></li>
<li><a href="https://www.freedesktop.org/software/systemd/man/latest/systemd-journald.service.html">systemd-journald.service - freedesktop.org</a></li>
<li><a href="https://linuxconfig.org/introduction-to-the-systemd-journal">Configure Systemd Journald on Linux Effectively systemd-journald.service - freedesktop.org systemd/Journal - ArchWiki Configure Persistent Systemd Journal Storage on Linux systemd-journald (8) — Arch manual pages journald.conf (5) - Linux manual page - man7.org Understanding systemd-journald and how logging works with ...</a></li>

</ul>
</details>

**社区讨论**: 评论者强烈批评 journald，指出啰嗦的应用程序会刷爆日志、无法按服务过滤，以及索引性能不佳。有评论指出当前行为与最初的只追加设计意图不符，还有建议仅将 journald 用作转发，把存储交给传统 syslog。

**标签**: `#systemd`, `#journald`, `#logging`, `#storage`, `#linux`

---

<a id="item-19"></a>
## [SparrowMap 让私人摄像头追踪政府车辆](https://sparrowmap.com/) ⭐️ 7.0/10

SparrowMap 是一个由志愿者运营的平台，利用众包私人摄像头拍摄并公开绘制公共道路上的政府车辆位置。该平台会模糊摄像头位置，并在设备上销毁私人车牌以保护旁观者的隐私。 该项目将典型的监视关系颠倒过来，让公民监督政府而非政府监督公民，由此引发关于隐私、信任和警察问责制的尖锐问题。它可能影响围绕自动车牌识别和反监控工具的讨论。 地图仅存储道路和模糊约 60 米的位置点，绝不保留摄像头的精确位置。私人车牌会在摄像头端直接销毁且永远不会存储；该项目在 GitHub 上开源。

hackernews · paulnpace · 8月14日 00:10 · [社区讨论](https://news.ycombinator.com/item?id=49293294)

**背景**: 自动车牌识别系统（ALPR）被警方广泛使用，像 Flock 这样的公司向执法机构出售监控摄像头，从而引发隐私担忧。SparrowMap 的做法正好相反：它让志愿者贡献摄像头画面，建立一份关于公共道路上政府车辆的开放、公开记录。该项目声称会积极匿名化数据：不保存精确地址，不存储私人车牌，只保留经过约 60 米模糊处理的道路级位置信息。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/SparrowMap/sparrowmap">GitHub - SparrowMap/sparrowmap: A system for an open, public ...</a></li>
<li><a href="https://map.sparrowmap.com/app">SparrowMap</a></li>

</ul>
</details>

**社区讨论**: 评论者看法不一：有人建议让 SparrowMap 的创作者也体验 Flock 员工车辆被类似追踪的感觉，以理解隐私侵犯；也有人指出部分城市的警方 GPS 数据已可通过 FOIA 获取。技术上的担忧包括实时地图报错、Windows 可执行文件缺乏可验证的哈希值，以及为何要发送非执法车辆的任何数据。

**标签**: `#privacy`, `#surveillance`, `#government`, `#transparency`, `#ethics`

---

<a id="item-20"></a>
## [《经济学人》力挺选择抗病与高智商胚胎](https://www.economist.com/leaders/2026/08/13/in-praise-of-designer-ish-babies) ⭐️ 7.0/10

《经济学人》在 2026 年 8 月的社论中主张，接受体外受精（IVF）的夫妇应被允许利用多基因评分（PGS）来选择抗病能力更强、智商更高的胚胎。该文章将此视为父母选择与公共政策问题，同时承认相关伦理争议。 这一立场将一项有争议的生物伦理议题带入主流讨论，可能影响胚胎选择的监管与公众舆论。它直接关系到备孕父母、IVF 服务机构、基因检测公司以及正在探索生殖技术边界的政策制定者。 文章区分了抗病能力选择（争议较小）与智商选择（高度争议）。多基因评分的预测并不完美，尤其在不同祖先群体间差异明显，而且只有在可获得多个胚胎时胚胎选择才可行；批评者还指出，该技术已在监管不足的情况下被商业化提供。

rss · The Economist · 8月13日 13:12

**背景**: 多基因评分（PGS）通常基于全基因组关联研究，汇总许多基因变异对某一性状或疾病风险的估计效应。胚胎植入前遗传学诊断（PGD）已能筛查单基因疾病，但为智商等复杂性状进行选择则远不可靠，并引发优生学担忧。目前已有公司开始提供多基因胚胎选择服务，促使各界呼吁加强监管。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.nejm.org/doi/full/10.1056/NEJMsr2105065">Problems with Using Polygenic Scores to Select Embryos</a></li>
<li><a href="https://en.wikipedia.org/wiki/Polygenic_score">Polygenic score - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Preimplantation_genetic_diagnosis">Preimplantation genetic diagnosis</a></li>

</ul>
</details>

**标签**: `#bioethics`, `#genetics`, `#embryo selection`, `#IQ`, `#public policy`

---

<a id="item-21"></a>
## [让他们写 RFC：倡导轻量级技术提案](https://ohadravid.github.io/posts/2026-08-let-them-write-rfcs/) ⭐️ 7.0/10

一篇题为《让他们写 RFC》的博文鼓励软件工程团队采用 RFC（Request for Comments）文档，作为在实施前提出和讨论技术变更的轻量级流程。 采用 RFC 流程有助于团队尽早统一技术决策，改善协作并减少昂贵的返工。它让每位工程师都能在设计讨论中发声，从而带来更好的架构和更强的工程文化。 博文倡导一种轻量、易用的 RFC 格式，鼓励分享尚未成熟的早期想法。它可能将内部 RFC 与正式的标准化组织 RFC 进行对比，强调内部 RFC 应保持简单且便于评审。

rss · Lobsters · 8月13日 10:48

**背景**: RFC（Request for Comments，征求意见稿）最初源于互联网标准社区，是一种概述技术规范和协议的正式文档。在软件工程中，RFC 常被用作讨论框架，让团队在实施前对提议的功能、变更或改进发表意见。编写 RFC 有助于工程师“三思而后行”，确保设计决策经过深思熟虑并留有文档记录。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://hiteksoftware.com.au/blog/what-is-rfc-in-software-development/">What Is RFC in Software Development? A Guide for... - Hitek Software</a></li>
<li><a href="https://www.techtarget.com/whatis/definition/Request-for-Comments-RFC">What is a Request for Comments ( RFC )? | Definition from TechTarget</a></li>
<li><a href="https://philcalcado.com/2018/11/19/a_structured_rfc_process.html">A Structured RFC Process</a></li>

</ul>
</details>

**标签**: `#RFC`, `#software engineering`, `#collaboration`, `#process`, `#technical writing`

---

<a id="item-22"></a>
## [用 Rust 的 Egg 库编写 SQL 优化器教程](https://rustmagazine.org/issue-2/write-a-sql-optimizer-using-egg) ⭐️ 7.0/10

这篇 Rust 杂志教程演示了如何使用 Egg e-graph 库构建 SQL 优化器。它展示了如何利用等价饱和（equality saturation）来探索和重写 SQL 查询计划。 将 e-graph 应用于 SQL 优化是一种新兴技术，可以使查询优化器更具模块化和可扩展性。本教程让 Rust 开发者和数据库爱好者更容易理解这一概念，可能会推动该领域更多的实践探索。 该教程可能涵盖了将 SQL 表达式表示为 e-node、为查询转换定义重写规则，以及使用成本模型来选择最优计划。它与 RisingLight 等相关工作有关，RisingLight 是一个使用 Egg 重写 SQL 优化器并同时支持基于规则和基于成本优化的教学数据库系统。

rss · Lobsters · 8月13日 19:00

**背景**: E-graph（等价图）是一种数据结构，能够紧凑地表示一组等价表达式，从而使工具可以同时处理许多可能的改写。Egg 是一个 Rust 库，提供了 e-graph 和等价饱和（equality saturation）的高效实现，其中重写规则会一直应用直到图不再变化。传统的 SQL 优化器依赖手工编码的启发式规则和搜索策略，而 e-graph 提供了一种更系统的方式来探索等价查询计划的空间。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://deepwiki.com/egraphs-good/egg">egraphs-good/ egg | DeepWiki</a></li>
<li><a href="https://github.com/egraphs-good/egg/discussions/189">Would e-graphs be useful for query optimization + rewrite ...</a></li>
<li><a href="https://pldi23.sigplan.org/details/egraphs-2023-papers/13/Building-an-SQL-Optimizer-with-Egg">Building an SQL Optimizer with Egg (EGRAPHS 2023 - E-Graph ...</a></li>

</ul>
</details>

**标签**: `#rust`, `#egg`, `#sql-optimizer`, `#e-graphs`, `#database`

---

<a id="item-23"></a>
## [天文学家发现新型天体“黑洞星”，或解释宇宙“小红点”](https://www.reddit.com/r/science/comments/1vnm3ca/astronomers_discover_a_brandnew_type_of/) ⭐️ 7.0/10

天文学家发现了一种前所未有的新型天体“黑洞星”。它表现为早期宇宙中一个极其明亮的红点，大小与整个太阳系相当，能量产生方式类似于黑洞。 这一发现可能解释詹姆斯·韦布空间望远镜拍摄的深空图像中反复出现的神秘“小红点”。若得到证实，它将代表一类连接恒星与黑洞行为的新型宇宙天体。 黑洞星的大小与太阳系相当，发出明亮的红光。它看起来像一颗巨大的恒星，但其能量输出更接近黑洞，并且可能解释韦布望远镜观测到的“小红点”。

reddit · r/science · /u/fchung · 8月13日 20:18

**背景**: 詹姆斯·韦布空间望远镜（JWST）在早期宇宙中拍摄到了大量致密而明亮的红色天体，被昵称为“小红点”。它们的真实本质一直不清楚，一些研究者认为它们可能是活跃黑洞或致密的恒星形成星系。新提出的“黑洞星”提供了一种替代解释：一种看起来像大质量恒星但能量产生方式类似黑洞的混合天体。这一发现若得到确认，将为已知的天体家族增加一个新的类别。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://news.mit.edu/2026/astronomers-discover-brand-new-type-astrophysical-object-black-hole-star-0812">Astronomers discover a brand-new type of astrophysical object ...</a></li>
<li><a href="https://www.theguardian.com/science/2026/aug/12/astronomy-discovery-new-cosmic-object-black-hole-star">Astronomers discover a new kind of cosmic object – a black ...</a></li>
<li><a href="https://www.sciencedaily.com/releases/2026/08/260813045538.htm">JWST Spots a Bizarre “Black Hole Star” 100 Billion Times ...</a></li>

</ul>
</details>

**标签**: `#astronomy`, `#astrophysics`, `#black hole`, `#discovery`, `#science`

---