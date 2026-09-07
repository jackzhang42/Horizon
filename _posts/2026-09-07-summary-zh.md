---
layout: default
title: "Horizon Summary: 2026-09-07 (ZH)"
date: 2026-09-07
lang: zh
---

> 从 45 条内容中筛选出 13 条重要资讯。

---

1. [OpenAI 披露 RSI 与智能体驱动的研究加速内幕](#item-1) ⭐️ 9.0/10
2. [《Simple Made Easy》：Rich Hickey 论简单为何胜过容易](#item-2) ⭐️ 9.0/10
3. [Anubis 中的 WebAssembly：耗时一年的向后兼容之路](#item-3) ⭐️ 8.0/10
4. [Asahi Linux 正式支持 Apple M3 芯片](#item-4) ⭐️ 8.0/10
5. [OpenAI《外星心智》：把高级 AI 比作异类智能](#item-5) ⭐️ 8.0/10
6. [《自动化的讽刺》：重温 1983 年经典论文](#item-6) ⭐️ 8.0/10
7. [用 1024 字节的 C 语言写成的 Python 解释器](#item-7) ⭐️ 7.0/10
8. [Nitter 与 XCancel 在法律建议后恢复服务](#item-8) ⭐️ 7.0/10
9. [GrapheneOS 宣布重构默认应用与安全剪贴板](#item-9) ⭐️ 7.0/10
10. [报告：至多 20%的新 gTLD 域名被用于诈骗](#item-10) ⭐️ 7.0/10
11. [从零构建 NetBSD 11 的实用指南](#item-11) ⭐️ 7.0/10
12. [陶哲轩谈纯 AI 方法“过早解决”数学问题的危害](#item-12) ⭐️ 7.0/10
13. [ThreadSanitizer 在 C 和 Go 中检测数据竞争的局限](#item-13) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [OpenAI 披露 RSI 与智能体驱动的研究加速内幕](https://simonwillison.net/2026/Sep/6/research-acceleration-the-view-inside-openai/) ⭐️ 9.0/10

OpenAI 发布了《Research acceleration: The view inside OpenAI》，与首席科学家 Jakub Pachocki 的随笔《An Alien Mind》一起，阐述了其迈向递归自我改进（RSI）和 AGI 的推进。文中还透露，到 2026 年 8 月中旬，按 API 价格计算，OpenAI 研究人员的编码智能体推理支出已超过每人每天 600 美元。 此事意义重大，因为 OpenAI 声称自动化 AI 研究者既能加速能力发展，也能加速安全研究，包括对齐以及抵御危险 AI 智能体的防御手段。公开的内部使用数据还难得地展示出，编码智能体正在成为头部 AI 实验室日常工作中核心且昂贵的基础设施。 文章中的图表显示，OpenAI 每位研究人员的中位每日推理支出从 2026 年 2 月的接近零上升到 8 月底的约 600 美元，并在 7 月下旬出现陡峭拐点。Simon Willison 猜测这一跃升与内部人员获得后来以 GPT-6 Astra 名义发布的模型有关，并指出 OpenAI 使用 RSI 这个缩写时并没有展开解释。

rss · Simon Willison · 9月6日 23:57

**背景**: 递归自我改进（RSI）指的是一种正反馈循环：AI 系统不断提高自身改进能力，从而可能引发加速的智能增长。智能体工程（agentic engineering）由 OpenAI 联合创始人 Andrej Karpathy 在 2026 年初提出，指的是工程师在人类监督下指挥 AI 智能体计划、编写并测试代码的工作方式。编码智能体正迅速从实验室实验发展为日常专业工具，并成为 AI 研发中的核心议题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Recursive_self-improvement">Recursive self-improvement - Wikipedia</a></li>
<li><a href="https://arxiv.org/pdf/2607.07663">Recursive Self-Improvement in AI: From Bounded Self ...</a></li>
<li><a href="https://www.ibm.com/think/topics/agentic-engineering">What is Agentic Engineering? | IBM</a></li>

</ul>
</details>

**社区讨论**: 评论区对推理支出的规模和可持续性感到惊讶，有人说每位研究人员的花费疯狂，还有人质疑这种持续增加的开销如何维持。部分评论者对 OpenAI 将加速 AI 研究包装成应对 AI 风险的必要防御表示不安；Simon Willison 则指出文章使用 RSI 这个缩写时没有为更广泛的读者解释其含义。

**标签**: `#OpenAI`, `#AGI`, `#Recursive Self-Improvement`, `#AI Research`, `#Coding Agents`

---

<a id="item-2"></a>
## [《Simple Made Easy》：Rich Hickey 论简单为何胜过容易](https://www.youtube.com/watch?v=SxdOUGdseq4) ⭐️ 9.0/10

2011 年，Rich Hickey 在 Strange Loop 大会发表了演讲《Simple Made Easy》，区分了“simple”（源自拉丁语 simplex，意为单一折叠或未交织）与“easy”（意为近在手边或熟悉）这两个词。他主张开发者应当有意识地选择简单，即使这条道路并不容易。 这场演讲已成为软件设计领域的重要参考，促使工程师重新权衡易用性与长期复杂度之间的关系。“简单”作为客观属性、“容易”作为主观感受的核心区分，直接影响着当今关于架构、状态管理与函数式编程的讨论。 Hickey 将“simple”追溯为拉丁语“一个折叠”的词根，而“easy”则与邻近和熟悉相关。他认为，常见的“容易”做法——可变状态、继承、副作用——会造成相互缠绕的系统，并推荐使用纯函数、不可变数据和显式组合等构造。

rss · Lobsters · 9月6日 14:25

**背景**: Rich Hickey 是 Clojure 的创造者、Datomic 的设计者。这场演讲于 2011 年在 Strange Loop 大会上发表，Hickey 在演讲中指出不应混淆“简单”与“容易”这两个概念。此后，演讲内容在 GitHub 等平台广泛传播，InfoQ 后来还将其作为“本周经典”推荐。文字稿至今仍常被用于软件设计课程和讨论的学习材料。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.infoq.com/presentations/Simple-Made-Easy/">Simple Made Easy - InfoQ Classic of the Week: Rich Hickey — 'Simple Made Easy' (2011) talk-transcripts/Hickey_Rich/SimpleMadeEasy.md at master ... simple-mindset.md · GitHub Notes: Rich Hickey’s talk Simple Made Easy – Collin K. Berke ... Simple Made Easy - Rich Hickey - by Suyog Kadel Talk Notes: "Simple Made Easy" by Rich Hickey (2011)</a></li>
<li><a href="https://sparsenotes.com/posts/2026/05/2026-05-30-hickey-simple-made-easy-classic/">Classic of the Week: Rich Hickey — 'Simple Made Easy' (2011)</a></li>
<li><a href="https://github.com/matthiasn/talk-transcripts/blob/master/Hickey_Rich/SimpleMadeEasy.md">talk-transcripts/Hickey_Rich/SimpleMadeEasy.md at master ...</a></li>

</ul>
</details>

**标签**: `#simplicity`, `#software design`, `#rich hickey`, `#talk`, `#programming`

---

<a id="item-3"></a>
## [Anubis 中的 WebAssembly：耗时一年的向后兼容之路](https://anubis.techaro.lol/blog/2026/anubis-wasm/) ⭐️ 8.0/10

开源 Web AI 防火墙 Anubis 经过一年的工程努力，终于推出了 WebAssembly 版本，该实现明确支持至 Chrome 66 的旧版浏览器。这篇技术博文详细介绍了其中涉及的详尽向后兼容性工作。 随着 AI 爬虫机器人威胁日益加剧，Anubis 基于挑战的防火墙提供了一种无需用户操作的防御方式，但要求 WebAssembly 可能将旧浏览器或安全设置严格的用户拒之门外。这项工作表明，在不牺牲广泛浏览器支持的前提下也能采用 WebAssembly，为安全和反机器人工具树立了榜样。 如果浏览器缺少 Anubis 依赖的 WebAssembly 功能，挑战会回退到原有的纯 JavaScript 解决方案。兼容性目标据称可回溯到 2018 年发布的 Chrome 66，这就要求避免使用较新的 WASM 指令并仔细进行功能检测。

hackernews · Lobsters · 9月6日 20:32 · [社区讨论](https://news.ycombinator.com/item?id=49590611)

**背景**: Anubis 是一个自称『Web AI 防火墙』的开源项目，它通过向 HTTP 客户端提出谜题或挑战（通常是一种工作量证明计算）来保护网站免受 AI 驱动的爬虫机器人影响。这些挑战在浏览器中静默运行，无需用户交互。WebAssembly（WASM）是一种运行在浏览器中的低级字节码格式，执行速度接近原生，非常适合这类计算密集任务。尽管 WASM 被设计为向后兼容且采用功能测试机制，但浏览器功能仍在不断演进，较旧的浏览器可能不支持较新的 WASM 指令。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/TecharoHQ/anubis">GitHub - TecharoHQ/anubis: Weighs the soul of incoming HTTP ...</a></li>
<li><a href="https://webassembly.org/">WebAssembly</a></li>
<li><a href="https://anubis.techaro.lol/">Anubis: Web AI Firewall Utility | Anubis</a></li>

</ul>
</details>

**社区讨论**: 评论者赞赏作者对向后兼容性的执着，有人称赞文中对开源维护者处境的诙谐语气。另一位出于隐私考虑禁用 WebAssembly 的用户希望，当 WASM 挑战无法运行时能给出明确提示；其他人则推荐了用于检测 WASM 功能支持的工具，并建议使用 Rust 的 wasm32v1-none 目标来构建基线兼容的 WASM。

**标签**: `#webassembly`, `#browser-compatibility`, `#anubis`, `#open-source`, `#software-engineering`

---

<a id="item-4"></a>
## [Asahi Linux 正式支持 Apple M3 芯片](https://asahilinux.org/2026/09/m2-episode-1/) ⭐️ 8.0/10

Asahi Linux 已宣布正式支持 Apple M3 系列芯片，使得 Linux 可以在最新的 Apple Silicon 硬件上运行。这一公告标志着该项目及其社区的一个重要里程碑。 这一进展意义重大，因为 Asahi Linux 是让 Linux 运行于 Apple Silicon 的主要项目，对 M3 的支持将这一能力扩展到最新的 Mac 上。它体现了逆向工程的重大进展，并可能加速 Linux 在 Apple 硬件上的采用。 Apple Silicon 是一个完全未文档化的平台，因此对 M3 的支持需要大量的逆向工程工作。与之前的 Asahi 版本一样，某些硬件功能（如睡眠和 HDMI 输出）在初期可能仍不完善。

hackernews · mdp2021 · 9月6日 14:08 · [社区讨论](https://news.ycombinator.com/item?id=49586698)

**背景**: Asahi Linux 是一个由 Hector Martin 发起的开源项目，旨在 Apple Silicon Mac 上原生运行 Linux。Apple 的 M3 系列于 2023 年底推出，是 Apple 为 Mac 设计的第三代自定义 ARM 处理器。由于 Apple 不公开其硬件细节，Asahi 开发者必须对每一代新芯片进行逆向工程，因此官方支持是一项显著成就。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Asahi_Linux">Asahi Linux - Wikipedia</a></li>
<li><a href="https://asahilinux.org/about/">About - Asahi Linux</a></li>
<li><a href="https://en.wikipedia.org/wiki/Apple_m3_chip,_apple_m3_cpu">Apple m3 chip, apple m3 cpu</a></li>

</ul>
</details>

**社区讨论**: 社区评论大多对开发者的辛勤工作表示赞赏，但也对 Apple 不支持该项目、使得这些努力成为必要而感到沮丧。一些用户指出，AI 辅助的驱动开发可能会加快对未来 M 系列芯片的支持，而另一些用户则指出缺少睡眠和 HDMI 支持是采用的障碍。

**标签**: `#linux`, `#apple-silicon`, `#asahi-linux`, `#open-source`, `#hardware`

---

<a id="item-5"></a>
## [OpenAI《外星心智》：把高级 AI 比作异类智能](https://openai.com/index/an-alien-mind/) ⭐️ 8.0/10

OpenAI 发布了一篇题为《外星心智》（An Alien Mind）的文章，将能力不断增强的 AI 描述为一种外星智能，并探讨其社会与安全影响。据报道，文中承认目前还没有任何实验室能在以最大速度负责任地扩展的同时解决好对齐与监控问题，并表示希望各方自愿放缓速度。 这篇文章之所以重要，是因为它直面 AI 行业的核心战略矛盾：前沿实验室究竟是应该继续扩张规模、在与其它 AI 行为体的防御性竞赛中保持领先，还是应在对齐问题解决之前主动放缓。作为最具影响力的实验室之一 OpenAI 的表态，它很可能会影响监管讨论，以及其它开发者为其训练决策所作的辩护逻辑。 社区讨论中引用的关键段落认为，继续快速训练更聪明模型的最强理由是：需要构建防御系统，以应对其它 AI 可能带来的危险。同一讨论还突出了文中的坦承——目前还没有实验室已把对齐与监控解决到足以负责任地以最大速度继续扩展的程度，文中同时表达了希望各方自愿放缓的愿望。

hackernews · OpenAI Blog · 9月6日 16:27 · [社区讨论](https://news.ycombinator.com/item?id=49588080)

**背景**: AI 对齐是旨在使 AI 系统遵循人类目标与价值观的研究领域；若对齐失败，系统可能去追求非预期甚至有害的目标。超级智能指一种在几乎所有重要领域都大幅超越最优秀人类头脑的假想智能体。OpenAI 的这篇文章参与了一场长期争论：高级 AI 是否会威胁人类文明，以及究竟应依靠技术对齐、行业自愿克制，还是外部监管来确保安全。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/AI_alignment">AI alignment</a></li>
<li><a href="https://en.wikipedia.org/wiki/Superintelligence">Superintelligence</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上 341 条评论的讨论交织着黑色幽默与怀疑情绪。一些评论者把该文斥为配合 OpenAI 上市计划的“IPO 姿态”；另一些人则指出文中论证所隐含的、令人不安的军备竞赛逻辑。有评论者将文章核心概括为“承认对齐仍未解决、需要各方自愿放缓”；还有人用讽刺的口吻设想，未来的观察者将如何看待人类未能停下自己亲手启动的进程。

**标签**: `#AI`, `#OpenAI`, `#alignment`, `#superintelligence`, `#tech ethics`

---

<a id="item-6"></a>
## [《自动化的讽刺》：重温 1983 年经典论文](https://static1.squarespace.com/static/644321e78cd2dd37613af33e/t/6694873f71612132a84371c7/1721009983702/Ironies+of+Automation_Bainbridge_1983.pdf) ⭐️ 8.0/10

这条新闻分享了 Lisanne Bainbridge 于 1983 年发表在期刊《Automatica》上的论文《自动化的讽刺》的 PDF。该链接未提供额外评论，只是分享了这一经典文本。 该论文是人因工程与自动化研究的奠基之作，其洞见对当今关于 AI 与自主系统的讨论依然极具参考价值。它挑战了“自动化只是减轻人类操作员负担”的假设，这对当代安全关键系统的设计至关重要。 这篇论文仅有五页，却指出了一个核心悖论：自动化控制系统通常处理常规操作，而留给人类操作员的都是那些困难、罕见且自动化无法处理的任务。到 2016 年 11 月，该论文已被引用大约 1800 次。

rss · Lobsters · 9月6日 13:40

**背景**: Lisanne Bainbridge 是一位认知心理学家，她的工作推动了认知工程领域的形成。她的论文指出，当设计者将任务自动化时，往往只会移除容易的部分，而那些残余的、难以预料的问题则留给了人类。因此，“讽刺”之处在于：先进的自动化反而让那些原本要取代的人类操作员变得更加重要，并给其带来更高的认知要求。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Ironies_of_Automation">Ironies of Automation - Wikipedia</a></li>
<li><a href="https://medium.com/@craigtrim/the-ironies-of-automation-0f302343bf7d">The Ironies of Automation. In 1983, a cognitive psychologist wrote… | by Craig Trim | Medium</a></li>
<li><a href="https://www.semanticscholar.org/paper/Ironies-of-automation-Bainbridge/0713bb9d9b138e4e0a15406006de9b0cddf68e28">[PDF] Ironies of automation | Semantic Scholar</a></li>

</ul>
</details>

**标签**: `#automation`, `#human-computer interaction`, `#cognitive engineering`, `#systems design`, `#classic paper`

---

<a id="item-7"></a>
## [用 1024 字节的 C 语言写成的 Python 解释器](https://austinhenley.com/blog/python1024.html) ⭐️ 7.0/10

Austin Henley 的博文展示了一个仅用 1024 字节 C 源代码写成的 Python 解释器。该解释器只支持 Python 的一个很小子集，依靠极端的代码高尔夫技巧而非通用解析器。 该项目展示了极端大小限制如何激发富有创意的解释器设计，引发了关于代码高尔夫和极简语言实现的讨论。它也凸显了像 Snek 这类面向资源受限嵌入式系统的实用替代方案。 该解释器只有 1024 字节 C 源码，编译后的二进制文件要大得多，且只支持非常小的 Python 子集。它采用了极端捷径：任何 'f' 都被当作 'for [x] in range[y]'，'w' 当作 'while'，'i' 当作 'if'；循环通过跳回并每次迭代重新解析源码来实现，类似 DOS 的 .bat 处理方式。

hackernews · Lobsters · 9月6日 23:14 · [社区讨论](https://news.ycombinator.com/item?id=49591876)

**背景**: 代码高尔夫是一种休闲编程竞赛，参与者力求用尽可能短的源代码解决特定问题。此前已有像 C4 和 Sector C 这样的极简语言实现先例。深奥编程语言（esolang）同样探索编程语言设计的边界。这类项目往往更看重创意和限制下的巧思，而非实际用途。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Code_golf">Code golf</a></li>
<li><a href="https://en.wikipedia.org/wiki/Esoteric_programming_language">Esoteric programming language</a></li>

</ul>
</details>

**社区讨论**: 评论者称赞该项目的创意，但也批评其“糟糕”的假设：jrdres 指出它假定任何 'f' 都是特定的 for 循环且缺乏错误检查，不像 C4。userbinator 指出 1024 字节的 C 会编译成更大的二进制，且每次迭代重新解析源码类似于 DOS 的 .bat 行为。teddyh 建议在实际生产中使用 Snek，而 marcelo-earth 表示这篇文章让他第一次了解到代码高尔夫。

**标签**: `#python`, `#interpreters`, `#code-golf`, `#programming-languages`, `#esoteric`

---

<a id="item-8"></a>
## [Nitter 与 XCancel 在法律建议后恢复服务](https://github.com/zedeus/nitter/commit/1428b4c2b4246f92a7e5b2673438e5fb39fcc4a3) ⭐️ 7.0/10

根据法律建议，Nitter 与 XCancel 实例已恢复运营，相关消息通过 Nitter 官方仓库的提交及附带链接发布。此前这些项目因法律压力曾暂停或面临不确定性。 对隐私倡导者和自托管用户而言，Nitter 仍是无需追踪或登录即可浏览 X/Twitter 内容的重要工具。它的恢复表明替代前端项目有可能挺过法律挑战，从而惠及依赖隐私保护方式访问 X 的用户。 该公告出现在 Nitter 维护者的提交中，并附有 xcancel.com/cdclegal 的链接，暗示项目方已获得正式法律指导。Nitter 比 Twitter 轻约 15 倍，且无需 JavaScript 即可使用，但仅支持浏览，不能登录或发帖。

hackernews · Lobsters · 9月6日 17:49 · [社区讨论](https://news.ycombinator.com/item?id=49588988)

**背景**: Nitter 是一款免费、开源、面向 X（原 Twitter）的替代前端，注重隐私和性能。XCancel 是 Nitter 的一个热门实例，允许用户无需账号或躲避追踪器即可查看 X 内容。许多类似的替代前端都面临大型平台的法律施压，因此法律意见往往决定它们能否继续运营。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Nitter">Nitter - Wikipedia</a></li>
<li><a href="https://github.com/zedeus/nitter">GitHub - zedeus/nitter: Alternative Twitter front-end · GitHub</a></li>
<li><a href="https://maketecheasier.com/browse-x-anonymously-with-xcancel/">How to Browse X Anonymously With XCancel - Make Tech Easier</a></li>

</ul>
</details>

**社区讨论**: 评论者对该项目的延续表示欣慰和支持，有人指出替代前端在获取 X 上关键信息方面的重要性。也有人谈到用户在平台间迁移的普遍困难，以及小项目对抗资金雄厚的法律团队所承受的经济负担；还有人希望 Instagram 等其他服务也能出现类似工具。

**标签**: `#Nitter`, `#privacy`, `#open-source`, `#Twitter/X`, `#legal`

---

<a id="item-9"></a>
## [GrapheneOS 宣布重构默认应用与安全剪贴板](https://grapheneos.social/@GrapheneOS/117225539756835649) ⭐️ 7.0/10

GrapheneOS 宣布计划彻底改造或完全替换剩余的 AOSP 默认应用，包括过时的图库应用，以及可能包括 AOSP 键盘。它同时表示，长期将加入通过 Messaging Layer Security（MLS）实现端到端加密的原生 RCS 支持，目标是摆脱对 Google Messages 的依赖。 这件事很重要，因为注重隐私的 Android 用户在 GrapheneOS 上目前必须依赖 Google Messages 才能使用加密 RCS，这与该项目核心的隐私目标相冲突。替换过时的 AOSP 应用也让 GrapheneOS 能够加强默认应用的安全性，并减少系统自带组件中的跟踪与数据收集。 通过 MLS 实现端到端加密的原生 RCS 是长期计划，不会立刻发布；目前 GrapheneOS 仍需要依赖 Google Messages 来使用加密 RCS。该团队近期招聘了更多员工以加快开发进度，AOSP 图库将被一个现代应用完全替换，AOSP 键盘也可能采取类似做法。

hackernews · Cider9986 · 9月6日 20:24 · [社区讨论](https://news.ycombinator.com/item?id=49590512)

**背景**: GrapheneOS 是一个开源、注重安全与隐私的移动操作系统，基于 Android 开源项目（AOSP）构建，主要官方支持 Google Pixel 设备。它通过对 Android 组件进行加固并缩减攻击面来提升安全性，同时保持广泛的 Android 应用兼容性。AOSP 应用是 Android 自带的系统应用，替换它们可以让 GrapheneOS 提供更注重隐私、更新更及时的替代品。RCS 是现代短信的继任协议，其标准的端到端加密基于 MLS。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/GrapheneOS">GrapheneOS</a></li>
<li><a href="https://grapheneos.org/">GrapheneOS: the private and secure mobile OS</a></li>

</ul>
</details>

**社区讨论**: 社区成员对非 Google 的 RCS 客户端计划反应积极，有用户表示这将是巨大的进步，因为此前在 Google Messages 上的体验时好时坏。部分用户对公告中提到的“安全剪贴板”功能具体指什么表示困惑，也有人建议用 FUTO 键盘替换 AOSP 键盘，并指出 ReFra 图库应用很可能是系统图库的替代品。

**标签**: `#GrapheneOS`, `#Android security`, `#privacy`, `#mobile OS`, `#RCS`

---

<a id="item-10"></a>
## [报告：至多 20%的新 gTLD 域名被用于诈骗](https://simonwillison.net/2026/Sep/6/the-purpose-of-dns-is-to-spread-scams/) ⭐️ 7.0/10

Terence Eden 引用 Interisle 的报告表示，域名系统（DNS）已成为骗子实施诈骗的巨大渠道。报告发现，2025 年新注册的 8500 万个 gTLD 域名中，截至 2025 年 5 月已有 850 万个被加入阻止列表，实际滥用率可能在 10%到 20%之间。 这些数据表明，每五个新注册的通用顶级域名中就可能有一个与诈骗相关，也凸显了 ICANN 多年来遏制域名滥用努力的明显不足。这会影响普通网民、企业以及整个 DNS 生态系统的可信度。 Interisle 认为 10%的滥用率很可能只是下限，实际情况可能接近 20%，而阻止列表数据只能反映那些已被发现并列入清单的域名。Simon Willison 指出，据称 ICANN 多年来一直在讨论这个问题，但未能解决。

rss · Simon Willison · 9月6日 14:40

**背景**: 域名系统（DNS）将 example.com 等人们易记的域名转换为计算机用来路由流量的数字 IP 地址。通用顶级域名（gTLD）是不与特定国家绑定的域名后缀，例如 .com、.org，以及后来出现的 .xyz、.top 等新后缀。DNS 阻止列表是记录已知或疑似用于垃圾邮件或恶意活动的域名的数据库，DNS 过滤器或邮件服务器会查询这些列表来阻止访问。由于域名注册成本低、可自动化且难以监管，犯罪分子会大规模注册新域名并不断更换，以实施各种诈骗。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Generic_top-level_domain">Generic top-level domain - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Domain_Name_System_blocklist">Domain Name System blocklist - Wikipedia</a></li>
<li><a href="https://www.icann.org/resources/pages/what-2012-02-25-en">What Does ICANN Do? - ICANN</a></li>

</ul>
</details>

**标签**: `#DNS`, `#security`, `#scams`, `#ICANN`, `#domain abuse`

---

<a id="item-11"></a>
## [从零构建 NetBSD 11 的实用指南](https://meanmicio.org/2026/09/06/netbsd-11-from-scratch/) ⭐️ 7.0/10

一篇题为“NetBSD 11 from scratch”的新技术文章描述了从源代码构建 NetBSD 11 的过程。目前已提供的内容摘录仅包含标题和评论链接，并未包含完整的文章正文。 NetBSD 11 是广受欢迎的可移植类 Unix 操作系统的最新大版本，因此从零构建指南对需要自定义配置的开发者和系统管理员很有价值。它也凸显了 NetBSD 在更广泛的 BSD 生态中持续的重要性，以及其构建系统的成熟度。 该文章日期为 2026 年 9 月 6 日，并在 Lobsters 上以 NetBSD、BSD、操作系统、从零构建和教程等标签分享。NetBSD 官方文档指出，完整构建可使用 build.sh 或更高级的 sysbuild 和 sysupgrade 命令完成，但无法根据提供的内容摘要核实该文章中的具体步骤。

rss · Lobsters · 9月6日 13:35

**背景**: NetBSD 是一个免费、开源的类 Unix 操作系统，以在众多硬件平台上的高可移植性而闻名。NetBSD 项目于 2026 年 7 月底前后发布了 NetBSD 11.0；从源代码构建通常需要获取内核和用户态源代码、配置内核，然后运行构建脚本以生成可安装的发行版本。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.netbsd.org/">The NetBSD Project</a></li>
<li><a href="https://en.wikipedia.org/wiki/NetBSD">NetBSD - Wikipedia</a></li>
<li><a href="https://www.netbsd.org/docs/guide/en/chap-updating.html">Chapter 35. Updating an existing system from sources</a></li>

</ul>
</details>

**标签**: `#NetBSD`, `#BSD`, `#operating-system`, `#from-scratch`, `#tutorial`

---

<a id="item-12"></a>
## [陶哲轩谈纯 AI 方法“过早解决”数学问题的危害](https://mathstodon.xyz/@tao/117207856734787448) ⭐️ 7.0/10

陶哲轩在 Mathstodon 上分享了一个讨论串，告诫人们纯 AI 驱动的方法可能“过早地解决”数学问题，并指出同样的情况也适用于编程。这条帖子推荐读者去查看更完整的讨论，并特别指出其中他认为最相关的一段。 随着 AI 辅助发现不断进入数学与软件开发领域，陶哲轩的提醒具有重要意义：它提醒研究者，AI 生成的答案可能看似可信，却缺乏严谨论证。这场讨论关乎“AI 输出何时值得信任”以及“人类验证为何仍然不可或缺”。 帖子本身没有介绍 AI 方法的技术细节，主要是给出 Mathstodon 上一条讨论串的链接，并建议读者阅读完整内容。陶哲轩明确指出，AI 过早给出数学结果与编程中过早“解决”问题具有相似性。

rss · Lobsters · 9月6日 07:45

**背景**: 陶哲轩是著名数学家，以解析数论研究以及积极参与线上数学社群而闻名。在关于 AI 与数学的讨论中，一个常见担忧是：自动化工具可能生成听起来合理的答案，却没有真正的推理或证明支撑，因此过早采信这类答案可能导致错误或无法验证的结论。陶哲轩将此类比到编程：一个看似可行却未被真正理解的“解决方案”，常常会带来隐藏的技术债或脆弱的代码。

**标签**: `#AI`, `#mathematics`, `#programming`, `#research`

---

<a id="item-13"></a>
## [ThreadSanitizer 在 C 和 Go 中检测数据竞争的局限](https://theconsensus.dev/p/2026/09/06/data-races-and-the-limits-of-threadsanitizer-in-c-and-go.html) ⭐️ 7.0/10

一篇新技术文章探讨了在 C 和 Go 中使用 ThreadSanitizer 检测数据竞争时的局限性，指出了该工具可能漏报真实竞争或产生误导性报告的情况。 数据竞争难以复现和调试，因此了解 ThreadSanitizer 的盲区可以帮助开发者避免盲目的安全感。这一讨论对在持续集成或本地测试中依赖 race detector 的 C/C++ 和 Go 程序员尤其有价值。 ThreadSanitizer 将编译期插桩与运行时库结合，通常会让程序变慢约 5 到 15 倍。其检测基于 happens-before 模型，因此涉及不受支持的原语、汇编代码或未插桩的第三方库时，竞争可能无法被检测到。

rss · Lobsters · 9月6日 22:13

**背景**: 数据竞争是指两个线程在没有同步的情况下访问同一内存位置，并且其中至少一个是写操作。ThreadSanitizer 是 LLVM/Clang 中用于 C/C++ 的动态检测工具，通过运行时观察被插桩的内存访问来发现此类问题。Go 也提供了自己的内置数据竞争检测器，其设计理念和实际局限与 ThreadSanitizer 类似。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://clang.llvm.org/docs/ThreadSanitizer.html">ThreadSanitizer — Clang 24.0.0git documentation</a></li>
<li><a href="https://github.com/google/sanitizers/wiki/threadsanitizercppmanual">ThreadSanitizerCppManual · google/sanitizers Wiki · GitHub</a></li>
<li><a href="https://hpc-wiki.info/hpc/ThreadSanitizer">ThreadSanitizer - HPC Wiki</a></li>

</ul>
</details>

**标签**: `#data-races`, `#ThreadSanitizer`, `#Go`, `#C`, `#concurrency`

---