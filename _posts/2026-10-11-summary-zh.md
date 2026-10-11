---
layout: default
title: "Horizon Summary: 2026-10-11 (ZH)"
date: 2026-10-11
lang: zh
---

> 从 31 条内容中筛选出 10 条重要资讯。

---

1. [《构建你自己的决策模型》教程引发分类器与 LLM 之争](#item-1) ⭐️ 7.0/10
2. [Unikernel 曾经很难——新工具与 LLM 或将改变这一局面](#item-2) ⭐️ 7.0/10
3. [Standard Bots 的 AI 技术栈：来自工业机器人的可靠执行经验](#item-3) ⭐️ 7.0/10
4. [LineageOS 24.0 发布，成为全新大版本 Android 定制 ROM](#item-4) ⭐️ 7.0/10
5. [揭秘 1980 年代的开关电容滤波芯片内部结构](#item-5) ⭐️ 7.0/10
6. [NumPy 2.5 让 np.searchsorted 提速最高达 25 倍](#item-6) ⭐️ 7.0/10
7. [Logfire 动态 JSON 拆分宣称带来 1000 倍查询加速](#item-7) ⭐️ 7.0/10
8. [Niko Matsakis：外部化证明无法用于循环 trait 实现](#item-8) ⭐️ 7.0/10
9. [字节级 Transformer 在同等参数量下超越子词模型](#item-9) ⭐️ 7.0/10
10. [JSON Tiles 让半结构化 JSON 获得接近列存的查询速度](#item-10) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [《构建你自己的决策模型》教程引发分类器与 LLM 之争](https://nishtahir.com/build-your-own-decision-model/) ⭐️ 7.0/10

nishtahir.com 上的一篇题为《Build your own decision model》的博客文章，手把手教读者构建自己的决策模型，并在 Hacker News 上获得 276 分、64 条评论而登上首页。讨论的焦点在于：所谓“决策模型”是否只是分类器的换名，以及基于 LLM 的零样本分类与传统方法相比究竟孰优孰劣。 这篇文章反映了业界正转向可在本地运行的小型专用模型，而非调用大型云端 API，这对关注延迟、成本和数据隐私的开发者尤为重要。它引发的争论也说明，命名和包装方式会显著影响人们对早已存在的机器学习技术的接受度。 该文属于实操教程而非研究成果，本身并未提供基准测试对比或模型版本信息。评论者补上了这一空缺：有人指出 Qwen 之类的小模型在本地运行时性能并不理想，而一个专门打造的“纯决策模型”据称能在浏览器中于 200 毫秒内返回结果。

hackernews · softwaredoug · 10月10日 22:50 · [社区讨论](https://news.ycombinator.com/item?id=50037949)

**背景**: 分类器是一种经典的机器学习组件，负责把输入归入一组固定类别中的某一类；这类模型已存在数十年，通常体积小、速度快。零样本分类则是较新的思路，即用通用大语言模型把文本归入它从未被专门训练过的类别，以速度与确定性换取便利性。小语言模型通常被定义为参数量少于约 400 亿的模型，小到足以在消费级笔记本和设备上训练或部署，这正是“本地推理”得以实现、无需把数据发送到远端服务器的原因。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Small_language_model">Small language model</a></li>
<li><a href="https://grokipedia.com/page/Lightweight_large_language_models">Lightweight large language models</a></li>
<li><a href="https://encord.com/blog/model-inference-in-machine-learning/">Model Inference in Machine Learning | Encord</a></li>

</ul>
</details>

**社区讨论**: 整体情绪在热情与质疑之间分化：有评论者称这篇教程是很好的起点；一位资深机器学习工程师则抱怨分类器多年来无人问津，如今只是被重新包装成“决策模型”；还有人直言它不过是几十年前就已存在的技术的换名。另一些人则推荐自己构建的更轻量方案，例如可在浏览器运行的纯决策模型 Laya 和可在 CPU 上训练的 Jeffy，反映出对快速端侧推理的真实需求。

**标签**: `#machine-learning`, `#classifiers`, `#llm`, `#decision-models`, `#local-inference`

---

<a id="item-2"></a>
## [Unikernel 曾经很难——新工具与 LLM 或将改变这一局面](https://ghuntley.com/unikernels/) ⭐️ 7.0/10

Geoffrey Huntley 的文章指出，unikernel——即与应用程序一同编译的单用途操作系统镜像——过去一直因构建、调试和运维过于困难而难以被主流采用，但近期工具链的改进以及 LLM 辅助开发可能终于让它变得切实可行。该文在 Hacker News 上引发了实质性讨论（151 分、67 条评论），围绕可观测性、操作系统取舍以及 LLM 能否帮助加固这类极简系统展开辩论。 如果 unikernel 变得切实可用，它们相比通用操作系统或容器能提供大幅缩小的攻击面、更低的内存占用和更快的启动速度，这可能重塑云工作负载与微服务的部署方式。这场讨论也凸显了系统工程的长期矛盾：极简设计能提升安全性与性能，却会剥离运维人员赖以生存的调试与可观测性工具。 评论者对安全性的说法提出强烈反驳，指出更小的攻击面并非非黑即白的胜利，而放弃 strace、eBPF、lsof、ss 等工具会让站点可靠性工程师在故障发生时"无路可走"。也有人提到现有的极简内核项目如 Zephyr，以及社区尝试——例如一个基于自研 BareMetal 内核、以约每小时 0.005 加元提供 4 MiB、无磁盘 VM 的独立云服务。

hackernews · ghuntley · 10月10日 14:27 · [社区讨论](https://news.ycombinator.com/item?id=50033357)

**背景**: unikernel 是一种专用的单用途操作系统镜像：编译器会把应用程序与它实际用到的库操作系统服务链接在一起，生成一个极小的可引导机器镜像。与通用操作系统或共享宿主内核的容器不同，unikernel 直接运行在虚拟机管理程序之上，没有独立的用户态/内核态权限边界，这在占用、性能和理论安全性上带来巨大收益，却也让传统调试工具难以使用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Unikernel">Unikernel - Wikipedia</a></li>
<li><a href="https://ideawell.fly.dev/post/toro-deploy-applications-as-unikernels">Toro: Deploy Applications as Unikernels | IdeaWell HN summary...</a></li>
<li><a href="https://phoenixnap.com/kb/unikernel-vs-container">Unikernel vs. Containers: What's the Difference? | phoenixNAP KB</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论对文章的乐观态度普遍持怀疑：多位评论者认为它低估了完整操作系统的价值，因为 strace、eBPF、lsof 等工具至关重要，而应用崩溃时 unikernel 没有任何退路。也有人认为真正的成本在于加固，并思考 LLM 能否承担这一工作；还有评论者指出，更小的攻击面在实践中并非非黑即白的安全胜利，尽管移除工具确实让横向移动变得更加困难。

**标签**: `#unikernels`, `#operating-systems`, `#virtualization`, `#observability`, `#systems-programming`

---

<a id="item-3"></a>
## [Standard Bots 的 AI 技术栈：来自工业机器人的可靠执行经验](https://www.latent.space/p/standard-bots) ⭐️ 7.0/10

Latent Space 发布了一篇针对 Standard Bots 工业机器人 AI 技术栈的技术深度报道，该技术栈使用预训练模型，先从人类演示中学习工厂任务，再通过真实部署中收集的纠正反馈持续改进。文章将其总结为一套关于如何构建在高风险环境中可靠执行任务的 AI 系统的实践经验。 在工业机器人领域，一次失败的动作就可能导致产线停摆或损坏昂贵硬件，因此用于保证模型可靠性的技术，与快速迭代但容忍出错的消费级 AI 形成了有价值的对照。这对机器人研究者和机器学习从业者都意义重大，因为文中描述的“演示学习加纠正反馈”闭环本质上就是模仿学习结合真实世界反馈，而这一模式在具身智能和通用模型部署中正变得越来越重要。 其核心机制是一个自举式循环：预训练模型先通过专家演示来建立对任务的理解，再利用从实际生产运行中采集的纠正数据进行微调；这种方式很有吸引力，因为它避免了在真实硬件上做纯试错式强化学习的高成本与高风险。但需要注意的是，该方法依赖于从部署中收集高质量、标注良好的纠正数据，这类数据的规模化采集并不容易，而且可能无法完全覆盖罕见的失效模式。

rss · Latent Space · 10月10日 14:04

**背景**: 模仿学习（又称“从演示中学习”）是一种让智能体通过监督学习模仿专家示例、而非依靠奖励驱动反复试错来掌握任务的范式。预训练模型则是先在大规模数据集上训练以捕捉通用模式的深度学习模型，之后再针对具体任务进行适配或微调，相比从零训练可以节省数据与算力。在工厂场景中，这种组合尤其有吸引力，因为由操作员提供演示和纠正，比让机器人在产线上反复失败来学习要便宜得多、也安全得多。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Imitation_learning">Imitation learning</a></li>
<li><a href="https://blogs.nvidia.com/blog/what-is-a-pretrained-ai-model/">What Is a Pretrained AI Model ? | NVIDIA Blog</a></li>

</ul>
</details>

**标签**: `#robotics`, `#AI/ML`, `#industrial-automation`, `#imitation-learning`, `#model-deployment`

---

<a id="item-4"></a>
## [LineageOS 24.0 发布，成为全新大版本 Android 定制 ROM](https://lineageos.org/Changelog-32/) ⭐️ 7.0/10

LineageOS 24.0 已正式发布，项目方通过全新的更新日志（Changelog）页面宣布了这一新版社区构建 Android 发行版。这标志着这个历史最悠久、使用最广泛的 Android 定制 ROM 之一完成了又一次大版本号跃升。 LineageOS 是少数仍在积极维护的大型定制 ROM 项目之一，因此新的大版本发布对于那些仍在使用老旧或已被官方停止支持设备的用户尤为重要，他们依赖它获得持续更新、安全补丁以及摆脱厂商预装软件的自由。在众多同类 ROM 项目相继停止开发的背景下，它也让整个 Android 第三方生态以及基于 AOSP 自行构建系统的实践得以延续。 官方更新日志页面是了解 24.0 具体变更的权威来源，其中通常会列出所基于的 Android 版本、官方支持的设备列表，以及功能、安全与构建系统方面的改动。与所有定制 ROM 一样，安装它一般需要解锁 bootloader 并刷入第三方 Recovery，而且官方构建版本只覆盖有限的一部分机型。

rss · Lobsters · 10月11日 06:21

**背景**: LineageOS 是一个由社区免费构建的 Android 第三方固件发行版，通常被称为定制 ROM，它 fork 自 Android 开源项目（AOSP），目标是相比厂商原厂系统提升性能与稳定性。定制 ROM 是第三方开发者基于 Google 开源代码打造的 Android 操作系统，往往不预装 Google Play 服务，常被用来延长厂商已停止更新机型的可用寿命。尽管多年来随着 Google 不断提高门槛，大多数定制 ROM 项目已经消失，LineageOS 仍是其中最具影响力和活跃度的项目之一。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/List_of_custom_Android_distributions">List of custom Android distributions - Wikipedia</a></li>
<li><a href="https://beebom.com/best-custom-roms-android-phones/">10 Best Custom ROMs for Android You Can Install | Beebom</a></li>
<li><a href="https://d2lvhbqifib4zm.cloudfront.net/blog/ditch-google-and-install-lineageos/">LineageOS setup guide: A powerful alternative to Android</a></li>

</ul>
</details>

**标签**: `#LineageOS`, `#Android`, `#Custom ROM`, `#Mobile OS`, `#Open Source`

---

<a id="item-5"></a>
## [揭秘 1980 年代的开关电容滤波芯片内部结构](http://www.righto.com/2026/10/ML10-switched-capacitor-filter.html) ⭐️ 7.0/10

Ken Shirriff 在其 righto.com 博客上发布了一篇新的技术深度剖析文章，拆解了一颗 1980 年代开关电容滤波芯片的内部工作原理，涵盖其电路设计与模拟信号处理技术。该文属于对老式集成电路的逆向工程／芯片裸片分析，面向对模拟与混合信号硬件感兴趣的读者。 开关电容滤波器是一项关键使能技术，它让芯片设计者可以用微小的开关化 MOS 电容取代笨重的精密电阻与电容，从而使全集成、可由时钟调谐的模拟滤波器在 1980 年代成为现实。理解这类芯片有助于现代硬件爱好者与复古计算爱好者认识模拟滤波如何走向片上集成，以及为何同样的技术在今天的混合信号前端中仍在使用。 开关电容滤波器通过 MOS 开关、精确匹配的片上电容和 MOS 运算放大器，在时钟节拍下把电荷搬入搬出电容，因此滤波器的截止频率由时钟比例精确决定，而不依赖元件容差。例如 LTC1064-1 等商用器件曾被记录为时钟与截止频率之比约为 100:1，可见其频率响应可以被控制得非常精确。

rss · Lobsters · 10月10日 21:28

**背景**: 开关电容滤波器是一种模拟电路，它通过让一个小电容在两个节点之间快速切换来模拟电阻；再配合运算放大器与电容，就能构成特性由时钟频率决定的滤波器。由于开关电容和运放都可以用标准 MOS/CMOS 工艺制造，这类滤波器能够集成在单一芯片上，无需传统模拟滤波器所依赖的大体积、不精确的电阻和电容。正因如此，自 1970 年代后期起，它们被广泛用于通信、抗混叠、音频和仪器仪表等设计中。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://hackaday.io/project/190799-lockdown-an-open-source-analog-lock-in-amplifier/log/219676-how-its-made-1-signal-input">How It's Made 1: Signal Input | Details | Hackaday.io</a></li>
<li><a href="https://static5.arrow.com/pdfs/2012/1/15/7/1/7/568/ltc_/auto/an40f.pdf">AN40 - Take the Mystery Out of the Switched Capacitor Filter</a></li>
<li><a href="https://weishielectronics.com/switched-capacitor/">Switched Capacitor : What It Is and How It Works</a></li>

</ul>
</details>

**标签**: `#hardware`, `#reverse-engineering`, `#analog-electronics`, `#switched-capacitor`, `#vintage-computing`

---

<a id="item-6"></a>
## [NumPy 2.5 让 np.searchsorted 提速最高达 25 倍](https://blog.scientific-python.org/numpy/searchsorted/) ⭐️ 7.0/10

Scientific Python 博客的一篇技术深度文章介绍了 NumPy 的 np.searchsorted 函数如何通过一种向量化算法被重写，其性能超过了 NumPy 2.4 的实现；该改动已合入 NumPy 2.5 版本，在作者的基准测试中带来了最高 25 倍的加速。 np.searchsorted 是科学计算 Python 生态中用于查找、分箱、直方图式统计和区间查询的核心基础函数，因此这种数量级的常数因子提速会无需用户改一行代码地传导到 pandas、scikit-learn、SciPy 以及大量用户脚本中。 该优化通过推导出一种向量化形式的二分查找，使一次能处理大量查询值，而不再是逐个循环比较；25 倍这一数字是最佳情况下的基准测试结果，并非对所有输入规模或数据类型都成立，文章还记录了该算法是如何被回移植进 NumPy 本身的。

rss · Lobsters · 10月10日 23:25

**背景**: NumPy 是 Python 数值计算的基础数组库，np.searchsorted 用于找出应当把某些值插入已排序数组的哪些位置才能保持有序，是二分查找式查询的底层构件。NumPy 2.5 被称为一个过渡性版本：它放弃了对 Python 3.11 的支持、移除了 distutils、让 2.0.x 系列中大量弃用项正式失效，并改进了自由线程（free-threading）支持，同时加入了诸如本次 searchsorted 重写这样的性能改进。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.scientific-python.org/numpy/searchsorted/">Blog - Making np.searchsorted up to 25× Faster in NumPy 2 . 5</a></li>
<li><a href="https://numpy.org/doc/2.2/reference/generated/numpy.searchsorted.html">numpy . searchsorted — NumPy v2.2 Manual</a></li>
<li><a href="https://numpy.org/news/">NumPy - News</a></li>

</ul>
</details>

**标签**: `#numpy`, `#performance-optimization`, `#algorithms`, `#scientific-computing`, `#python`

---

<a id="item-7"></a>
## [Logfire 动态 JSON 拆分宣称带来 1000 倍查询加速](https://pydantic.dev/articles/dynamic-shredding-2026-01-26) ⭐️ 7.0/10

Pydantic 于 2026 年 1 月 26 日发布技术文章，介绍了其可观测性平台 Logfire 中的“动态拆分”（dynamic shredding）优化，用于查询半结构化的 JSON 属性数据，并宣称查询速度最高提升 1000 倍。官方表示该功能将从 2026 年 2 月起开始向所有客户逐步推送。 可观测性后端通常要存储海量的半结构化属性数据（span 标签、日志字段、资源元数据），而查询这些数据历来是整个链路中最慢的环节。如果动态拆分能够通用化，那么对高基数 JSON 做临时过滤与分组在生产规模下将变得可行，这会给面临同样问题的其他可观测性和数据库厂商带来竞争压力。 拆分的原理是把有类型的键和动态键提升为独立列，从而能够使用列式存储与索引，而无需在查询时解析整个 JSON 文档。1000 倍是最好情况下的上限而非普遍结果，这种方案以写入阶段额外的处理和模式管理为代价，换取更快的读取速度。

rss · Lobsters · 10月11日 06:16

**背景**: Pydantic Logfire 是由 Pydantic 校验库团队打造的、基于 OpenTelemetry 的可观测性平台，覆盖 trace、日志和指标，支持 Python、JavaScript/TypeScript、Rust、Go、Java 等兼容 OTel 的语言。由于可观测性数据是半结构化的，而且在不同服务之间结构经常变化，通常以 JSON 形式存储，灵活但过滤和聚合速度很慢。JSON 拆分是一项已有技术——Milvus 提供了 JSON Shredding 功能，SQL Server 则用 OPENJSON 把 JSON“拆分”成行与列——它把 JSON 对象转换成结构化的列，从而在保留无模式灵活性的同时获得列式存储的性能。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://pydantic.dev/articles/dynamic-shredding-2026-01-26">How shredding JSON is giving Logfire 1000x query speedups</a></li>
<li><a href="https://milvus.io/docs/json-shredding.md">JSON Shredding | Milvus Documentation</a></li>
<li><a href="https://pydantic.dev/logfire">Pydantic Logfire : AI Observability for LLMs, Apps & RAG</a></li>

</ul>
</details>

**标签**: `#JSON`, `#Query Optimization`, `#Observability`, `#Databases`, `#Performance`

---

<a id="item-8"></a>
## [Niko Matsakis：外部化证明无法用于循环 trait 实现](https://smallcultfollowing.com/babysteps/blog/2026/10/10/modular-vs-external-proofs/) ⭐️ 7.0/10

在 2026 年 10 月 10 日的一篇博客文章中，Niko Matsakis 论证了“外部化”证明与 Rust 的设计根本不相容，并得出结论：在处理 trait 求解器中的循环 trait 实现时，模块化证明是唯一可行的方案。该文延续了他 2026 年 8 月关于支持循环 trait 实现动机的文章，同时也解释了此语境下“证明”的含义。 这一分析直接影响 Rust 下一代 trait 求解器的设计方向，而该项目明确旨在彻底替换现有负责证明 trait 约束和规范化关联类型的组件。由于循环 trait 实现有望带来表达力更强的泛型代码，如何为这类循环提供证明依据，对 Rust 类型系统具有实质影响。 核心问题在于，外部化证明需要从求解器局部推理上下文之外来论证某个循环 trait 实现的成立，而 Matsakis 认为这一点无法与 Rust 的设计约束（如一致性 coherence，以及只有真正可靠的循环才能被接受这一要求）相协调。文章明确指出，让推理保持在求解上下文内部的模块化证明才是可行的替代方案。

rss · Lobsters · 10月10日 16:56

**背景**: Rust 要求大多数 trait 实现是归纳式的（即非循环的），以便编译器判断某个类型是否满足 trait 约束。某些递归类型会产生真正的循环，即证明某个类型实现了某个 trait，需要先假设它已经实现。trait 求解器是编译器中负责解决这些约束义务的组件，而正在开发的下一代 trait 求解器旨在替换当前实现；这里所说的“证明”，就是求解器对某个 trait 约束成立的论证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://smallcultfollowing.com/babysteps/blog/2026/10/10/modular-vs-external-proofs/">Why ' externalized ' proofs of cyclic trait impls does not work · baby.....</a></li>
<li><a href="https://smallcultfollowing.com/babysteps/blog/2026/08/10/cyclic-trait-solving/">Cylic trait implementations : motivation · baby steps</a></li>
<li><a href="https://rust-lang.github.io/goals/2025h1/next-solver.html">Next-generation trait solver - Rust Project Goals</a></li>

</ul>
</details>

**标签**: `#rust`, `#type-systems`, `#trait-solver`, `#compiler-design`, `#programming-languages`

---

<a id="item-9"></a>
## [字节级 Transformer 在同等参数量下超越子词模型](https://arxiv.org/html/2610.05978v1) ⭐️ 7.0/10

一篇新的 arXiv 论文指出，直接处理原始字节序列的标准扁平 Transformer，在参数量相同的情况下能够取得比子词分词模型更低的最优损失，其做法是借助 token-superposition 训练和哈希嵌入来抵消序列变长带来的开销。字节模型在 CUTE 词语操作任务上取得约 40% 的相对提升，在 OCRBench 上也有 20% 的提升。 如果字节级模型的可扩展性优于子词模型，那么当前几乎所有语言模型都依赖的固定子词词表可能变得不再必要，从而改变分词器、算力预算和序列长度的设计方式。这还可能惠及多模态模型，因为字节表示比任意切分的子词单元更贴近细粒度的视觉特征。 论文认为字节输入的额外序列长度其实是一种优势：典型的子词大约对应四个字节，因此相同参数预算下可获得更多计算量。逐字节损失分析显示方差很大，大部分字节的损失接近零，难点集中在模型学到的局部结构边界处。研究还冻结了最多四分之一的中层，强制它们只处理局部聚合表示，模型无需额外训练便保持了下游性能；此外，字节级草稿模型每次目标前向所接受的 token 数量约为子词版本的 3.4 倍，使投机解码更具吸引力。

rss · Lobsters · 10月10日 22:25

**背景**: 大多数大语言模型并不是逐字符读取文本的，而是先用分词器把文本切分成子词单元，再把每个单元映射为一个嵌入向量。这么做的原因是原始字节或字符序列长得多，长期以来被认为会让训练和推理成本过高，因此子词词表一直被当作必要的效率折中。该论文对这一假设提出挑战，测试扁平 Transformer 能否自行学出内部的切块方式，并借助了 token-superposition 训练（把多个 token 合并为一个嵌入以加速预训练）以及哈希嵌入（通过哈希而非固定查找表把输入映射为向量）等技术。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://nousresearch.com/token-superposition">Efficient pretraining with token superposition - NOUS RESEARCH</a></li>
<li><a href="https://grokipedia.com/page/Token_Superposition_Training">Token Superposition Training</a></li>

</ul>
</details>

**标签**: `#language-models`, `#byte-level-models`, `#tokenization`, `#transformers`, `#scaling-laws`

---

<a id="item-10"></a>
## [JSON Tiles 让半结构化 JSON 获得接近列存的查询速度](https://db.cit.tum.de/~durner/papers/json-tiles-sigmod21.pdf) ⭐️ 7.0/10

一篇 SIGMOD 2021 的研究论文提出了 JSON tiles：这套算法能够自动识别一批 JSON 对象中隐含的共同结构，并把其中最重要的键透明地抽取成类似列的物理布局。由此，关系型数据库可以以原生速度对 JSON 数据做分析查询，扫描性能往往接近列式存储，同时仍能处理异构且不断变化的数据，并为查询优化器自动收集统计信息。 由于开发者更看重灵活性而非预先设计模式，JSON 已成为事实上的交换与存储格式，但关系型引擎长期以来为此付出高昂的解析与扫描代价。若有一种技术能在不牺牲模式灵活性的前提下弥合大部分性能差距，就可能改变数据平台存储与查询半结构化数据的方式，对数据工程师和数据库厂商都有实际意义。 JSON tiles 的设计目标是：即使数据高度异构或结构随时间变化，也能保持稳健，而不是假设存在唯一固定的模式；它还会自动收集统计信息，让优化器能够选出较好的执行计划。论文通过实验与最先进的系统和研究方案进行对比，表明该方法既稳健又高效，不过它面向的是读密集型的分析负载，而非事务型负载。

rss · Lobsters · 10月11日 06:21

**背景**: JSON 这类半结构化数据没有严格预定义的模式，而是靠自描述的标签和分隔符来组织结构，数据模型往往在读取时才被解释。这种灵活性对开发者很友好，却让关系型引擎颇为吃力：通常必须解析每个文档并遍历树状表示才能回答查询。相比之下，列式存储把同一字段的值放在一起，从而支持向量化执行、更好的压缩和快得多的分析扫描——JSON tiles 想要复现的正是这一特性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://cppreference.db.in.tum.de/~durner/papers/json-tiles-sigmod21.pdf">JSON Tiles : Fast Analytics on Semi-Structured Data</a></li>
<li><a href="https://en.wikipedia.org/wiki/Semi-structured_data">Semi-structured data</a></li>
<li><a href="https://motherduck.com/learn/columnar-storage-guide/">What Is Columnar Storage ? Column vs Row Databases Explained</a></li>

</ul>
</details>

**标签**: `#databases`, `#JSON`, `#semi-structured data`, `#query optimization`, `#columnar storage`

---