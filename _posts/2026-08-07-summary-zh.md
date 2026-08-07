---
layout: default
title: "Horizon Summary: 2026-08-07 (ZH)"
date: 2026-08-07
lang: zh
---

> 从 99 条内容中筛选出 28 条重要资讯。

---

1. [Zapscape：KVM/x86 虚拟机逃逸漏洞](#item-1) ⭐️ 9.0/10
2. [AMD 收购 Taalas，将 AI 模型蚀刻进硅片以提升推理性能](#item-2) ⭐️ 8.0/10
3. [马里奥遇见帕累托：多目标权衡的交互式教程](#item-3) ⭐️ 8.0/10
4. [OpenAI 升级 ChatGPT 中的 GPT-5.6 Sol，免费用户可体验 GPT-5.6 Luna](#item-4) ⭐️ 8.0/10
5. [DeepMind 领导层大调整：四名研究员离职，Demis 任董事长，Koray 任高级副总裁](#item-5) ⭐️ 8.0/10
6. [AI 赋能公民或令英国政府停摆](#item-6) ⭐️ 8.0/10
7. [英国法院被人工智能职场纠纷淹没](#item-7) ⭐️ 8.0/10
8. [AI 实验室是否应像危险动物主人一样承担责任？](#item-8) ⭐️ 8.0/10
9. [中国的 AI 雄心冲击全球最庞大的劳动力](#item-9) ⭐️ 8.0/10
10. [tl;dv 验证缺陷导致 181,874 场会议泄露](#item-10) ⭐️ 8.0/10
11. [schrodingers-toctou：演示 TOCTOU 二进制替换攻击](#item-11) ⭐️ 8.0/10
12. [Futhark 语言新增递归函数，面向 GPU 的函数式编程](#item-12) ⭐️ 8.0/10
13. [AI 设计病毒在实验室中成功杀死耐药大肠杆菌](#item-13) ⭐️ 8.0/10
14. [AI 时代，品味成为最后的差异化优势](#item-14) ⭐️ 7.0/10
15. [尼泊尔政府加入“我已遭入侵”数据泄露查询服务](#item-15) ⭐️ 7.0/10
16. [Herdr 加入 Y Combinator，运行时保持开源](#item-16) ⭐️ 7.0/10
17. [ProvenMetal（YC S26）推出数日内交付的美国本土 PCB 组装服务](#item-17) ⭐️ 7.0/10
18. [Meta 因危害儿童被罚 9.42 亿美元](#item-18) ⭐️ 7.0/10
19. [人类在 AI 智能体命令审批游戏中漏掉了三分之一的威胁](#item-19) ⭐️ 7.0/10
20. [Datasette 1.0a38 修复 SQL 注入安全问题](#item-20) ⭐️ 7.0/10
21. [非洲 AI 先驱倡导高效、任务专用模型](#item-21) ⭐️ 7.0/10
22. [印度 IT 业经历 AI 考验，毕业生就业更难](#item-22) ⭐️ 7.0/10
23. [Zig 的 Io.Threaded：简洁的 I/O 后端设计](#item-23) ⭐️ 7.0/10
24. [Xibalba64 开发记：在 2026 年制作 N64 游戏](#item-24) ⭐️ 7.0/10
25. [celld 推出可自托管的分布式 Durable Objects](#item-25) ⭐️ 7.0/10
26. [Crubit：C++/Rust 双向互操作工具发布](#item-26) ⭐️ 7.0/10
27. [科学家首次让生菜和烟草产生动物肌红蛋白](#item-27) ⭐️ 7.0/10
28. [灵长类大脑增大或由视觉区域驱动，而非额叶](#item-28) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [Zapscape：KVM/x86 虚拟机逃逸漏洞](https://github.com/V4bel/Zapscape) ⭐️ 9.0/10

名为 Zapscape 的公开概念验证程序展示了 KVM/x86 中的一个 guest-to-host 逃逸漏洞，可让特权 L1 用户在宿主机上创建 root 所有的文件。研究人员 Kim 于 8 月 6 日发布了该漏洞利用，目标是 AMD 嵌套 SVM/NPT 及 Linux 7.1.3。 这是一个关键虚拟化安全缺陷，因为 guest 可逃逸出虚拟机并在宿主机上以 root 权限执行代码，影响云服务商和多租户环境。它同时凸显了嵌套虚拟化的风险以及加固 hypervisor 的持续挑战。 该 bug 位于内核内的 KVM 中，独立于 QEMU 的模拟触发，QEMU 本身不受影响。Kim 建议在 QEMU TCG 下安全测试该 PoC，且目前没有在野利用证据。

rss · Lobsters · 8月6日 17:31

**背景**: KVM（Kernel-based Virtual Machine）是 Linux 内核模块，使内核能充当 hypervisor。guest-to-host 逃逸指虚拟机内运行的代码可突破虚拟机并在宿主机操作系统上执行。Zapscape PoC 针对嵌套虚拟化（AMD NPT/SVM），即 guest 虚拟机内再运行另一个 hypervisor 或 VM，从而扩大攻击面。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/V4bel/Zapscape">GitHub - V4bel/Zapscape · GitHub</a></li>
<li><a href="https://thehackernews.com/2026/08/new-zapscape-kvm-flaw-could-let.html">New Zapscape KVM Flaw Could Let Privileged L1 Guest Code Escape to Linux Hosts</a></li>
<li><a href="https://www.phoronix.com/news/Linux-Zapscape-Vulnerability">Zapscape Is The Latest Linux Vulnerability For KVM Guest - To - Host ...</a></li>

</ul>
</details>

**标签**: `#security`, `#virtualization`, `#KVM`, `#exploit`, `#x86`

---

<a id="item-2"></a>
## [AMD 收购 Taalas，将 AI 模型蚀刻进硅片以提升推理性能](https://www.theregister.com/systems/2026/08/06/amd-acquires-ai-chip-startup-taalas-to-boost-inference-performance-by-etching-models-into-silicon/5284344) ⭐️ 8.0/10

2026 年 8 月 6 日，AMD 宣布同意收购总部位于多伦多的 AI 芯片初创公司 Taalas，该公司将 AI 模型权重直接硬连线进硅片。此次收购旨在将推理性能提升一个数量级甚至更多，帮助 AMD 在快速增长的人工智能推理市场中竞争。 此次收购为 AMD 带来了一项差异化技术，可大幅加速特定 AI 模型的推理，挑战英伟达的主导地位和谷歌基于 TPU 的方案。这也标志着行业向模型专用芯片发展的趋势，可能迫使 AI 实验室重新思考如何维持竞争护城河。 Taalas 的加速器为单一 AI 模型定制（即硬连线），以灵活性换取性能，但随着模型演进可能面临过时风险。该初创公司于 2026 年 2 月融资 1.69 亿美元，其技术专注于推理而非训练。

hackernews · itvision · 8月6日 20:23 · [社区讨论](https://news.ycombinator.com/item?id=49201970)

**背景**: AI 推理是运行训练好的模型以进行预测的过程，随着 AI 应用规模化，它变得日益关键。传统 GPU 是通用型的，而将模型'蚀刻'进硅片意味着权重被永久固化到电路中，可大幅降低延迟和功耗，但牺牲了灵活性。AMD 一直在与英伟达竞争 AI 芯片市场份额，此次收购正是针对推理领域、契合其战略的一部分。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.theregister.com/systems/2026/08/06/amd-acquires-ai-chip-startup-taalas-to-boost-inference-performance-by-etching-models-into-silicon/5284344">AMD acquires AI chip startup Taalas to boost inference performance by etching models into silicon</a></li>
<li><a href="https://www.reuters.com/world/asia-pacific/chip-startup-taalas-raises-169-million-help-build-ai-chips-take-nvidia-2026-02-19/">Chip startup Taalas raises $169 million to help build AI chips to take on Nvidia | Reuters</a></li>
<li><a href="https://www.cnbc.com/2026/08/06/amd-buys-taalas-startup-that-hardwires-ai-models-into-its-silicon.html">AMD buys Taalas, startup that hardwires AI models into its silicon</a></li>

</ul>
</details>

**社区讨论**: 评论者对于 OpenAI 和 Anthropic 未率先收购 Taalas 表示惊讶，指出随着中国开放权重模型日益领先，此类收购本可建立护城河。还有人推测涉及内置权重芯片的黑市交易等科幻场景，更有评论者分享了该技术的演示链接。

**标签**: `#AMD`, `#AI hardware`, `#inference`, `#acquisition`, `#silicon`

---

<a id="item-3"></a>
## [马里奥遇见帕累托：多目标权衡的交互式教程](https://www.mayerowitz.io/blog/mario-meets-pareto) ⭐️ 8.0/10

这篇题为《Mario Meets Pareto》的博客文章将帕累托前沿概念应用于《马里奥赛车》的角色选择，通过交互式可视化展示速度与加速之间的权衡。它把多目标优化的核心理念变成了一个可动手操作、基于游戏的教程。 通过将抽象的优化概念植根于流行游戏，这篇文章让广大技术读者更容易理解帕累托效率。社区的热烈反响表明，开发者认为这一概念有助于思考安全、性能和用户体验之间的权衡。 帕累托前沿被定义为多目标优化中非支配解的集合，即没有其他方案在所有目标上都更优。在马里奥赛车的例子中，位于前沿上的角色代表速度与加速的最优权衡，而其他角色至少被一个更优选项所支配。

hackernews · theanonymousone · 8月6日 11:24 · [社区讨论](https://news.ycombinator.com/item?id=49195231)

**背景**: 帕累托效率以经济学家维尔弗雷多·帕累托命名，指的是在不损害其他标准的前提下无法改进任何个体或标准的状态。在多目标优化中，帕累托前沿就是所有高效解的集合；当目标为两个时，通常表现为一条曲线。这一概念广泛应用于工程、经济学和决策领域，用于识别相互冲突目标之间的均衡权衡。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Pareto_front">Pareto front - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Multi-objective_optimization">Multi-objective optimization - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者将这一概念延伸到其他场景：jerf 将其与常见的“安全与用户体验”争论联系起来，指出这种说法只有在处于前沿时才成立；uzerfcwn 描述了在《魔兽世界》装备搭配中类似的基于帕累托的剪枝方法；__s 则提到速通玩家常选择位于前沿边缘的 Bowser。还有人给出轻松的视角，比如爸爸们会选择既能保持竞争力又不会太强、适合陪孩子玩的赛车。

**标签**: `#Pareto front`, `#optimization`, `#data visualization`, `#game design`, `#technical blog`

---

<a id="item-4"></a>
## [OpenAI 升级 ChatGPT 中的 GPT-5.6 Sol，免费用户可体验 GPT-5.6 Luna](https://openai.com/index/improving-gpt-5-6-sol-in-chatgpt/) ⭐️ 8.0/10

OpenAI 宣布改进 ChatGPT 中的 GPT-5.6 Sol，称其在日常对话中准确性和一致性更佳。公司还扩大了 GPT-5.6 Luna 对免费 ChatGPT 用户的开放范围，包括无限制的日常聊天。 将 GPT-5.6 Luna 这类接近前沿的模型开放给免费用户，大幅降低了公众使用先进 AI 的门槛。这可能重塑竞争格局，因为可访问性和价格将变得与基准分数一样重要。 GPT-5.6 按能力从低到高分为 Luna、Terra、Sol 三个版本。此次更新中，免费用户可更广泛使用 Luna，而最强的 Sol 获得质量改进；社区评论还提到免费用户新增了“Think”推理开关。

hackernews · OpenAI Blog · 8月6日 17:02 · [社区讨论](https://news.ycombinator.com/item?id=49199357)

**背景**: GPT-5.6 是 OpenAI 最新的大型语言模型系列，于 2026 年 7 月 9 日公开发布，包含 Luna、Terra 和 Sol 三个版本。OpenAI 通常将最强模型保留给付费用户，免费用户仅能使用较旧或较小的模型，因此将 Luna 开放给免费用户标志着访问策略的显著转变。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/GPT-5.6_Sol">GPT-5.6 Sol</a></li>
<li><a href="https://openai.com/index/previewing-gpt-5-6-sol/">Previewing GPT-5.6 Sol: a next-generation model | OpenAI</a></li>
<li><a href="https://artificialanalysis.ai/articles/gpt-5-6-has-landed">GPT - 5 . 6 benchmarks across Intelligence, Speed and Cost</a></li>

</ul>
</details>

**社区讨论**: 评论者们意见不一：一些人赞赏向免费用户开放推理功能，认为这是重大民主化举措；另一些人则质疑在算力受限且与中国模型竞争的背景下的经济性。还有人批评需要手动选择推理级别带来额外负担，也有人认为 OpenAI 的使命声明隐含着把 ChatGPT 模型视为 AGI。

**标签**: `#OpenAI`, `#GPT-5.6`, `#ChatGPT`, `#AI accessibility`, `#model updates`

---

<a id="item-5"></a>
## [DeepMind 领导层大调整：四名研究员离职，Demis 任董事长，Koray 任高级副总裁](https://www.latent.space/p/ainews-jeff-sanjay-oriol-and-quoc) ⭐️ 8.0/10

DeepMind 正在经历一次重大领导层调整：Jeff、Sanjay、Oriol 和 Quoc 这几位研究员即将离职，Demis 将出任董事长，Koray 将担任高级副总裁。 多位知名研究员从全球顶尖 AI 实验室离职，可能预示着研究方向的转变，并影响人才留存。这还可能对更广泛的 AI 社区产生影响，因为他们往往会创建或加入新的项目。 这篇新闻简报没有披露离职研究员的去向、具体生效日期或改组原因。已公布的人事变动仅为 Demis 出任董事长和 Koray 担任高级副总裁。

rss · Latent Space · 8月6日 04:34

**背景**: DeepMind 是谷歌母公司 Alphabet 旗下的顶尖人工智能研究实验室。顶级 AI 实验室的高层人事变动往往预示着研究重点的变化，并会引发 AI 社区的广泛关注。资深研究员的离职可能对在研项目和未来招聘产生广泛影响。

**标签**: `#DeepMind`, `#AI`, `#leadership`, `#industry news`, `#research`

---

<a id="item-6"></a>
## [AI 赋能公民或令英国政府停摆](https://www.economist.com/leaders/2026/08/06/how-ai-is-breaking-the-british-state) ⭐️ 8.0/10

《经济学人》的一篇社论认为，配备 AI 模型和智能体的公民能够以大规模自动化方式提交异议和投诉，可能使英国政府不堪重负，导致行政运转陷入停顿。 这一设想揭示了一类新型风险：AI 不仅提升行政效率，而且可能被用来对公共机构施加不对称压力，进而迫使政府重新设计其与公民互动的方式。 该文是一篇观点文章而非技术研究，聚焦治理与公务员系统的承受能力。文章指出，AI 虽能提升公共服务效率，但也降低了恶意异议的成本，因此政府需要调整流程和规则。

rss · The Economist · 8月6日 08:34

**背景**: AI 智能体（又称 agentic AI）是构建在大型语言模型之上的系统，能够设定目标、调用工具并以有限的自主性采取行动。它们可以操作网站、填写表格、提交文件，因此普通公民也能将提交规划异议等行政程序自动化。这是这类能力首次便宜到足以被个人大规模使用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/AI_agent">AI agent</a></li>
<li><a href="https://en.wikipedia.org/wiki/Agentic_AI">Agentic AI</a></li>
<li><a href="https://arxiv.org/abs/2503.21460">[2503.21460] Large Language Model Agent: A Survey on Methodology, Applications and Challenges</a></li>

</ul>
</details>

**标签**: `#AI`, `#Government`, `#Society`, `#Agents`, `#Policy`

---

<a id="item-7"></a>
## [英国法院被人工智能职场纠纷淹没](https://www.economist.com/britain/2026/08/06/the-tragedy-of-the-commons-ai-edition) ⭐️ 8.0/10

《经济学人》报道称，英国的就业法庭正在被源于人工智能相关工作场所做法（如算法驱动的招聘、监控和绩效管理）的纠纷淹没。文章指出，法律体系正难以跟上人工智能应用的速度。 这之所以重要，是因为工作场所中人工智能的应用速度已超过法律框架的更新，形成了一种'公地悲剧'：个体纠纷不断累积，而系统性问题却得不到解决。这不仅影响英国的雇主、雇员、法官和政策制定者，也使面临类似压力的其他国家受到波及。 文章借用'公地悲剧'这一隐喻，指出与人工智能相关的损害往往通过个人就业法庭索赔来处理，而非通过集体监管来解决。文章特别关注英国的就业法庭，算法管理、自动化招聘和人工智能驱动的绩效指标正日益成为纠纷的核心。

rss · The Economist · 8月6日 08:26

**背景**: 算法管理指的是使用软件（包括人工智能）部分或完全自动化传统上由人类管理者完成的任务，例如排班、监控和评估员工。用于招聘的人工智能工具也被证明会复制已有的偏见，从而可能引发歧视纠纷。当劳动者对自动化决策提出异议时，举证和裁决的压力往往落在法院和就业法庭身上，而这些机构必须在新的技术背景下解释较为陈旧的法律。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.oecd.org/en/publications/algorithmic-management-in-the-workplace_287c13c4-en.html">Algorithmic management in the workplace | OECD</a></li>
<li><a href="https://www.ilo.org/algorithmic-management-workplace">Algorithmic management in the workplace | International Labour Organization</a></li>
<li><a href="https://hai.stanford.edu/news/ai-hiring-tools-can-yield-racial-bias-and-systemic-rejection">AI Hiring Tools Can Yield Racial Bias and Systemic Rejection</a></li>

</ul>
</details>

**标签**: `#AI regulation`, `#employment law`, `#labor`, `#United Kingdom`, `#society`

---

<a id="item-8"></a>
## [AI 实验室是否应像危险动物主人一样承担责任？](https://www.economist.com/science-and-technology/2026/08/06/should-ai-labs-be-treated-like-the-owners-of-dangerous-animals) ⭐️ 8.0/10

《经济学人》于 2026 年 8 月 6 日发表分析，主张应依据“危险动物”原则让 AI 实验室承担法律责任。文章警告说，自主黑客攻击——即无需人工控制即可发起网络攻击的 AI 代理——已经出现，而各国政府尚未做好准备。 这篇文章为 AI 治理引入了一种新颖的法律责任框架，从自愿性的安全承诺转向严格责任。它可能重塑 AI 开发者、保险公司和政策制定者处理 AI 安全的方式，尤其是当自主黑客攻击带来紧迫的网络安全风险时。 该论点将“危险动物”先例（动物主人对其动物造成的损害承担严格责任）应用于 AI 实验室。文章特别指出自主黑客攻击是一个具体的近期威胁，并称各国政府既缺乏相应的法律框架，也缺乏应对此类系统的技术准备。

rss · The Economist · 8月6日 08:20

**背景**: 自主黑客攻击是进攻性安全的下一次演进，AI 驱动的代理可以在无需人工干预的情况下发起并调整网络攻击。传统法律体系通常将责任归于用户，或让 AI 造成的损害处于灰色地带，这使得“危险动物”原则可能成为严格责任的一个先例。搜索结果指出，自主黑客攻击“不是为了让黑客攻击/渗透测试更容易”，而是从根本上改变网络威胁。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.ampcuscyber.com/blogs/rise-of-autonomous-hacking-bots/">How AI Hacking Bots Outsmart Cyber Defenses</a></li>
<li><a href="https://docs.decepticon.red/en/vision/autonomous-hacking">Autonomous Hacking - Decepticon</a></li>

</ul>
</details>

**标签**: `#AI safety`, `#AI governance`, `#cybersecurity`, `#policy`, `#autonomous systems`

---

<a id="item-9"></a>
## [中国的 AI 雄心冲击全球最庞大的劳动力](https://www.economist.com/briefing/2026/08/06/chinas-ai-drive-threatens-the-worlds-largest-workforce) ⭐️ 8.0/10

《经济学人》2026 年 8 月的简报指出，中国领导人越来越担心，他们大力推动的 AI 技术可能导致大规模劳动者失业。这篇文章揭示了中国 AI 战略核心处的一个迫在眉睫的矛盾。 此事意义重大，因为全球最庞大劳动力群体的大量失业可能在中国引发经济和社会不稳定，并波及全球供应链。北京如何应对 AI 导致的就业替代，将对面临同样挑战的其他经济体具有风向标意义。 这篇文章将问题描述为产业政策与劳动保护之间的矛盾：官员希望中国在 AI 领域领先，但该技术可能削弱制造业和服务业的就业。文中没有给出具体的失业预测数字，而是聚焦于政策制定者日益加剧的不安。

rss · The Economist · 8月6日 08:17

**背景**: 中国长期以来依靠规模庞大且相对廉价的劳动力来支撑其工厂和经济增长。近年来，政府将 AI 列为提升竞争力和国家安全的重要战略方向，并在从工厂到公共服务等各个领域推进应用。自动化淘汰岗位的速度可能快于新岗位的创造，而中国的社会安全网——包括失业保障和再培训计划——仍在发展完善之中。《经济学人》的简报探讨了这些力量如何相互碰撞，以及领导人为何开始感到担忧。

**标签**: `#AI`, `#China`, `#workforce`, `#economics`, `#policy`

---

<a id="item-10"></a>
## [tl;dv 验证缺陷导致 181,874 场会议泄露](https://bobdahacker.com/blog/tldv-hack) ⭐️ 8.0/10

一篇博客文章披露，AI 会议记录工具 tl;dv 因验证缺陷导致 181,874 场会议暴露。该漏洞似乎允许未授权访问会议录音。 tl;dv 被广泛用于录制和转录 Zoom、Google Meet 和 Microsoft Teams 上的会议，因此这次暴露可能导致许多组织的敏感商业讨论外泄。这一发现也凸显了 AI 会议工具日益增长的隐私风险。 据称泄露的数据包括会议录音、转录文本和摘要，根本原因在于应用程序的验证逻辑存在缺陷。博客文章称 181,874 场会议被“完全暴露”，但摘要部分未提供完整的攻击细节。

rss · Lobsters · 8月6日 11:22

**背景**: tl;dv 是一款 AI 驱动的会议记录工具，可自动录制、转录、总结并分享来自 Zoom、Google Meet 和 Microsoft Teams 等平台的在线会议。会议通常包含机密商业信息，因此授权和验证检查对于防止用户访问他人录音至关重要。一旦验证失效，攻击者就可能检索或查看本不应访问的数据。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://tldv.io/">tl;dv - AI Meeting Notetaker for Zoom, Google Meet & Teams</a></li>
<li><a href="https://tldv.io/features/meeting-recordings-transcriptions/">Video Record & Transcribe Google, MS Teams and Zoom Meetings</a></li>

</ul>
</details>

**标签**: `#security`, `#vulnerability`, `#privacy`, `#meeting recordings`, `#tl;dv`

---

<a id="item-11"></a>
## [schrodingers-toctou：演示 TOCTOU 二进制替换攻击](https://github.com/xoreaxeaxeax/schrodingers-toctou) ⭐️ 8.0/10

GitHub 项目`schrodingers-toctou`已发布，提供了一个利用时间检查到使用（TOCTOU）竞态条件的概念验证，使系统执行与预期不同的二进制文件。它挑战了“你运行的二进制文件与你编写的程序相同”这一假设。 这项工作揭示了二进制信任模型中的根本弱点，可能影响安全研究人员、开发者以及任何在执行前依赖文件完整性的系统。它可能促使新的防御技术，并引发对现代软件中 TOCTOU 漏洞的更深入审视。 该项目托管在`https://github.com/xoreaxeaxeax/schrodingers-toctou`，其名称引用薛定谔的猫，说明二进制文件在验证与执行之间的双重状态。由于提供的片段中没有详细的技术说明，确切的利用机制仍需查看仓库文档。

rss · Lobsters · 8月6日 15:47

**背景**: 时间检查到使用（TOCTOU）是一类由竞态条件引起的软件缺陷，在系统安全检查与该检查资源的后续使用之间，系统状态可能发生变化。攻击者利用这一时间间隔替换或修改资源，例如将合法二进制文件换成恶意文件。此类漏洞在文件系统操作中很常见，并且与 LLM 智能体等多步骤流程越来越相关。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Time-of-check_to_time-of-use">Time-of-check to time-of-use - Wikipedia</a></li>

</ul>
</details>

**标签**: `#security`, `#TOCTOU`, `#binary exploitation`, `#research`

---

<a id="item-12"></a>
## [Futhark 语言新增递归函数，面向 GPU 的函数式编程](https://futhark-lang.org/blog/2026-08-05-recursion.html) ⭐️ 8.0/10

Futhark 团队于 2026 年 8 月 5 日宣布，该语言终于开始支持递归函数。这是 Futhark 作为面向 GPU 的纯函数式数据并行数组语言的一项重大特性。 递归函数让更多算法可以直接用 Futhark 表达，减少依赖手工改写成迭代式或显式并行形式。这有望扩大该语言在高性能 GPU 计算中的适用范围，并吸引更多函数式编程开发者。 现有内容未包含实现细节，博客文章主要提供了一个讨论帖链接。Futhark 是一种静态类型、纯函数式、数据并行的 ML 家族数组语言；在 GPU 上支持递归在技术上颇具挑战，因此该公告具有重要意义。

rss · Lobsters · 8月6日 07:10

**背景**: Futhark 是哥本哈根大学计算机科学系（DIKU）开发的一种高级函数式数据并行数组编程语言，旨在编译为可在 GPU 和多核 CPU 上高效运行的并行代码。它深受 NESL 启发，采用扁平化（flattening）变换，但传统上对并行表达方式有所限制，例如不支持不规则的嵌套数据并行。由于在 GPU 上高效实现递归历来困难，因此这一新增特性被视为期待已久的功能。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Futhark_(programming_language)">Futhark (programming language)</a></li>
<li><a href="https://futhark-lang.org/">Why Futhark ?</a></li>

</ul>
</details>

**标签**: `#Futhark`, `#functional programming`, `#GPU`, `#recursion`, `#programming languages`

---

<a id="item-13"></a>
## [AI 设计病毒在实验室中成功杀死耐药大肠杆菌](https://www.reddit.com/r/science/comments/1vhku87/in_lab_tests_aidesigned_viruses_killed_e_coli/) ⭐️ 8.0/10

研究人员首次利用人工智能设计出完全功能性的病毒——即能杀死细菌的噬菌体。在实验室测试中，由这些 AI 设计的噬菌体组成的混合物杀死了对天然噬菌体具有耐药性的大肠杆菌菌株。 这标志着合成生物学的一个里程碑，表明 AI 能够生成具有实际治疗潜力的完整病毒基因组。它可能推动针对抗生素耐药感染的噬菌体疗法，同时作者关于可能出现无法被现有对策控制的病原体的警告，也引发了紧迫的生物安全议题。 这些病毒是仅感染细菌的噬菌体，该研究也是首次通过 AI 成功设计完整基因组。作者在论文中警告说：‘此类基因组可能编码出新病原体，这些病原体无法被现有对策所控制。’

reddit · r/science · /u/mvea · 8月6日 23:55

**背景**: 噬菌体是一类感染并在细菌内部复制的病毒，也是地球上最丰富、最多样的生物实体之一。自 20 世纪 20 年代以来，噬菌体就被用作抗生素的替代品，如今被视为对抗多重耐药菌的可能疗法。在这项研究中，AI 被用来设计全新的病毒基因组，这些基因组功能完整并能在实验室中复制，这是全基因组设计领域的首次突破。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.bbc.com/news/articles/c5y3j3ngevmo">Artificial Intelligence used to design brand new viruses</a></li>
<li><a href="https://www.theguardian.com/science/2026/aug/06/safety-fears-as-scientists-make-first-viruses-designed-by-ai">Safety fears as scientists make first viruses designed by AI | Science | The Guardian</a></li>
<li><a href="https://www.nature.com/articles/d41586-025-03055-y">World’s first AI-designed viruses a step towards AI-generated life | Nature</a></li>

</ul>
</details>

**标签**: `#AI`, `#synthetic biology`, `#bacteriophages`, `#biosecurity`, `#E coli`

---

<a id="item-14"></a>
## [AI 时代，品味成为最后的差异化优势](https://notashelf.dev/posts/taste-is-all-thats-left) ⭐️ 7.0/10

软件工程师 notashelf 在新文章《Taste Is All That's Left》中提出，当 AI 接管更多的技术性工作时，人类的品味和审美判断成为最后的差异化优势。该文迅速引发热议，在社区平台上获得了 268 个点赞和 205 条评论。 这篇文章与行业内关于人类判断力在 AI 辅助开发中的角色的广泛讨论产生了共鸣。随着 AI 工具生成越来越多的代码，辨别设计优劣的能力正成为一项关键技能，可能重塑工程师的评估方式和价值。 这篇文章偏重哲学思辨，而非技术细节，没有提供基准或案例研究。评论区有人反驳说，LLM 在更长的时间尺度上难以产出连贯成果，且 AI 生成的文本往往缺乏信息量；作者则感叹市场未必会回报那些甘愿背负品味“重担”的人。

hackernews · Lobsters · 8月6日 17:01 · [社区讨论](https://news.ycombinator.com/item?id=49199346)

**背景**: 这篇文章涉及软件工程中关于“良好品味”的长期争论——即超越技术技能、对整洁且可维护设计的直觉判断。随着 AI 代码生成器降低了编码门槛，品味可能成为关键的区分因素，这一观点近来重新受到关注。Sean Goedecke 等作者曾探讨技术品味与技能的区别，也有研究者研究机器能否拥有审美判断力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.seangoedecke.com/taste/">What is "good taste " in software engineering ?</a></li>
<li><a href="https://medium.com/data-science-collective/taste-still-matters-why-software-engineers-need-more-than-ai-skills-in-2025-d227add52d36">Taste Still Matters: Why Software Engineers Need More... | Medium</a></li>
<li><a href="https://sites.stat.columbia.edu/gelman/research/unpublished/AI_aesthetic_judgment.pdf">Artificial Intelligence and Aesthetic Judgment Jessica Hullman∗ Ari Holtzman†</a></li>

</ul>
</details>

**社区讨论**: 评论区呈现明显分歧。一些读者深深共鸣，回忆自己是如何通过多年犯错才培养了品味；另一些人则批评文章冗长、语无伦次，甚至像“AI 垃圾内容”，并认为核心论点混淆了市场激励与个人选择。一个反复出现的观点是：LLM 的解决方案表面上不错，但在更大的项目中会逐渐变质。

**标签**: `#AI`, `#software-engineering`, `#taste`, `#essay`, `#philosophy`

---

<a id="item-15"></a>
## [尼泊尔政府加入“我已遭入侵”数据泄露查询服务](https://www.troyhunt.com/welcoming-the-nepalese-government-to-have-i-been-pwned/) ⭐️ 7.0/10

尼泊尔政府已加入由 Troy Hunt 创办的数据泄露通知服务“我已遭入侵”（HIBP）。这一合作使尼泊尔公民能够查询自己的个人信息是否已在已知的数据泄露事件中暴露。 这标志着一个国家政府正式采用第三方泄露通知服务的典型案例，提升了数据泄露透明度，并帮助公民积极应对身份盗窃风险。这可能为其他政府利用 HIBP 服务造福公众开创先例。 公告中并未明确说明合作的具体范围，例如是否包括对政府官方网站的域名级监控。社区评论指出尼泊尔政府 IT 安全薄弱，表明此举是及时但具有挑战性的一步。

hackernews · gnabgib · 8月6日 21:52 · [社区讨论](https://news.ycombinator.com/item?id=49203105)

**背景**: “我已遭入侵”（HIBP）是一项免费服务，它汇集各种来源的泄露数据，让用户查询自己的电子邮件地址或电话号码是否已被泄露。政府可以订阅域名搜索功能，以监控官方域名的数据暴露情况。尼泊尔政府运营的数字服务长期存在安全性和可靠性问题，因此这次采用显得尤为重要。

**社区讨论**: 评论者大多对此消息表示欢迎，但也表达了担忧。有人指出尼泊尔政府网站安全性差，例如缺乏输入消毒和生物识别数据暴露问题。还有人开玩笑说政府数据可能已被泄露。一些人请求改进功能，例如允许更改电子邮件地址；另有人则担心如果政府接管此类服务，可能会被执法机构滥用。

**标签**: `#security`, `#data breach`, `#HIBP`, `#government`, `#Nepal`

---

<a id="item-16"></a>
## [Herdr 加入 Y Combinator，运行时保持开源](https://herdr.dev/blog/herdr-is-joining-y-combinator/) ⭐️ 7.0/10

多智能体编程的开源终端复用器 Herdr 宣布加入 Y Combinator 并获得预种子轮融资。公司重申其运行时将保持开源，并透露近期将许可证从 AGPL 更改为 Apache。 这一公告表明投资者对 AI 编程工具领域的持续兴趣，而该领域已日益拥挤，拥有多个 YC 支持的竞争对手。通过承诺开源运行时并采用宽松的 Apache 许可证，Herdr 旨在实现差异化，并安抚那些对 VC 资助的开源项目持谨慎态度的开发者。 根据社区讨论，Herdr 最近将其许可证从 AGPL 更改为 Apache 2.0，以消除采用障碍。它类似于 tmux，但专为协调多个 AI 编程智能体而设计，并面临来自 Superset 和 cmux 等其他 YC 初创公司的竞争。

hackernews · collinmanderson · 8月6日 19:14 · [社区讨论](https://news.ycombinator.com/item?id=49201003)

**背景**: 终端复用器是一种软件应用，允许用户在单个窗口内管理多个终端会话，并可在进程继续运行时分离和重新附加会话。多智能体编程涉及协调多个 AI 智能体，每个智能体拥有各自的上下文和职责，在同一代码库上并发工作。Herdr 正处于这两个概念的交汇点，提供基于终端的界面来启动、监控和管理 AI 编程智能体。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Terminal_multiplexer">Terminal multiplexer</a></li>
<li><a href="https://addyosmani.com/blog/code-agent-orchestra/">AddyOsmani.com - The Code Agent Orchestra - what makes multi-agent coding work</a></li>

</ul>
</details>

**社区讨论**: 社区反应总体积极但喜忧参半：许多人祝贺创始人 Can 获得预种子轮融资，少数人对 VC 融资和开源可持续性表示怀疑。一位评论者指出 YC 支持的竞争对手市场拥挤，另一位质疑从 AGPL 改为 Apache 的理由，还有一位要求提供 asciinema 演示以便更好地评估 TUI。

**标签**: `#Y Combinator`, `#open source`, `#AI coding`, `#terminal multiplexer`, `#startup`

---

<a id="item-17"></a>
## [ProvenMetal（YC S26）推出数日内交付的美国本土 PCB 组装服务](https://provenmetal.com/) ⭐️ 7.0/10

YC S26 初创公司 ProvenMetal 推出了一项服务，可在数天内交付美国本土组装的 PCB，而传统渠道通常需要数周。该公司自动化了报价、DFM 审查和元器件采购流程，并协调美国合约制造商的网络。 美国在全球 PCB 产量中的份额从 2000 年的 30%下降到如今的 4%，该服务直指电子产品制造回流的关键瓶颈。如果成功，它可能使本土原型制作和小批量生产对初创公司、国防及工业客户更具可行性。 该平台包含 KiCad 和 Altium 插件，可在布局完成前将 BOM 发送给 ProvenMetal，从而提前采购长交期元器件。该公司在旧金山存储元器件，并将成套物料路由至美国小型合约制造商网络。

hackernews · willcarkner · 8月6日 15:59 · [社区讨论](https://news.ycombinator.com/item?id=49198464)

**背景**: 合约制造商（CM）以另一家公司的品牌生产产品，在电子行业中常负责 PCB 组装。制造设计（DFM）审查是在生产前检查电路板在制造、组装和测试方面的问题。许多美国 PCB 组装厂规模小且劳动密集，元器件采购往往是最大瓶颈，因此自动化前台任务可显著缩短交付周期。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Contract_manufacturer">Contract manufacturer - Wikipedia</a></li>
<li><a href="https://www.nod-pcba.com/news/1829-en.html">Tired of Frequent Hardware Design Pitfalls? How DFM Reviews ...</a></li>

</ul>
</details>

**社区讨论**: 评论者持谨慎乐观态度但提出担忧：有人建议提供授信额度以在现金转换周期上取胜，也有人质疑其价格能否与中国竞争，指出美国组装往往更慢更贵。一位硬件老兵认为真正的瓶颈是元器件采购而非组装，还有人批评网站未说明层数、柔性板等制造约束。

**标签**: `#PCB`, `#hardware`, `#manufacturing`, `#supply-chain`, `#startup`

---

<a id="item-18"></a>
## [Meta 因危害儿童被罚 9.42 亿美元](https://www.wsj.com/tech/meta-ordered-to-pay-942-million-to-address-harm-to-kids-from-social-media-8ba5aab7) ⭐️ 7.0/10

新墨西哥州一家法院裁定 Meta 支付 9.42 亿美元，因其违反该州公共妨害法（NMSA 1978 § 30-8-1），对使用 Instagram 和 Facebook 的儿童造成伤害。 这一具有里程碑意义的判决让 Meta 为平台上的儿童安全失职承担经济责任，并可能鼓励其他州对社交媒体公司提起类似的公共妨害诉讼。 该判决源于一项诉讼，指控 Meta 故意设计成瘾性功能伤害未成年人。Meta 预计将提起上诉，这可能推迟任何付款。

hackernews · boplicity · 8月7日 00:06 · [社区讨论](https://news.ycombinator.com/item?id=49204352)

**背景**: 新墨西哥州的公共妨害法（NMSA 1978 § 30-8-1）将公共妨害定义为故意制造或维持任何影响众多公民、损害公共健康、安全、道德或福利的行为。此案是对社交媒体平台在青少年心理健康方面提起诉讼的更广泛浪潮的一部分。

**社区讨论**: 评论者对这笔罚款的影响表示怀疑，称这只是 Meta 的‘经营成本’，并预测上诉可能会拖上数年。还有评论者质疑孩子们从 Instagram 和 Facebook 中究竟能得到什么好处。

**标签**: `#Meta`, `#social-media`, `#regulation`, `#child-safety`, `#legal`

---

<a id="item-19"></a>
## [人类在 AI 智能体命令审批游戏中漏掉了三分之一的威胁](https://scalex.dev/blog/ai-agent-permissions-stats/) ⭐️ 7.0/10

对 AI 智能体权限游戏《Continue? Y/N》4 万次游玩的分析显示，玩家在审批命令时漏掉了三分之一的威胁，该分析基于 40.9 万次决策。作者根据此前 Hacker News 讨论中的反馈更新了游戏后才汇总这些数据。 该结果凸显出，在时间压力和权限疲劳下，人类对 AI 智能体的“人在回路”监督很容易出错。这对正在构建 AI 智能体审批界面的厂商和团队非常重要，因为盲目点击可能成为安全链条中的薄弱环节。 该游戏设有 60 秒倒计时，并且会对误批准和误拒绝都做出惩罚，评论者认为这带来了人为压力。统计数据还显示，玩家通常会忽略‘npm run’命令上方显示的历史日志信息。

hackernews · Wirbelwind · 8月6日 11:58 · [社区讨论](https://news.ycombinator.com/item?id=49195468)

**背景**: AI 智能体经常需要执行修改文件或安装包等命令，开发者依靠权限提示框由人来批准有风险的操作。当用户面对频繁弹窗时会产生‘权限疲劳’，而这个游戏正是为了演示这一问题。有评论者将这种体验比作《Papers, Please》，并指出现有的审批模式与其说是在做安全检查，不如说是在衡量用户对 AI 的信任程度。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://dev.to/soytuber/ghes-key-rotation-bug-bounty-program-refocus-ai-agent-permission-fatigue-d8i">GHES Key Rotation, Bug Bounty Program Refocus, AI Agent ...</a></li>
<li><a href="https://modernorange.io/item/48308376">Show HN: Continue? Y/N: A 60-second game about AI agent ...</a></li>
<li><a href="https://www.libhunt.com/posts/1510934-show-hn-continue-y-n-a-60-second-game-about-ai-agent-permission-fatigue">Show HN: Continue? Y/N: A 60-second game about AI agent ...</a></li>

</ul>
</details>

**社区讨论**: 评论者大多质疑该游戏数据的有效性：有人说提示对真实风险有误导性，也有人认为倒计时和没有实际后果让结论不成立。作者 Wirbelwind 回应称这‘只是个游戏’，但他觉得数据有趣，并且已吸收此前讨论中的反馈。还有人提出更宏观的观点，比如批准弹窗更像是厂商的免责手段，而非真正的安全机制。

**标签**: `#AI safety`, `#human-in-the-loop`, `#permissions`, `#empirical study`, `#Hacker News`

---

<a id="item-20"></a>
## [Datasette 1.0a38 修复 SQL 注入安全问题](https://simonwillison.net/2026/Aug/6/datasette/#atom-everything) ⭐️ 7.0/10

Datasette 1.0a38 修复了一个影响在同一数据库中同时提供公开和私有表的实例的 SQL 注入漏洞。该修复也已反向移植到 Datasette 0.65.3。 此安全修复对于运行混合公开/私有表配置的管理员至关重要，可防止拥有公开表访问权限的认证用户通过原始 SQL 读取私有数据。它突显了在开源数据发布工具中保护数据访问的重要性。 该漏洞允许拥有任何公开表访问权限的用户在执行 SQL 权限受限的情况下发起 SQL 注入攻击，从而获得对私有表的只读访问权限。建议管理员在混合访问的数据库上禁用 execute-sql 权限。

rss · Simon Willison · 8月6日 18:24

**背景**: Datasette 是一个用于探索和发布数据的开源工具，其权限系统控制对表的访问。execute-sql 权限决定用户是否可以运行任意 SQL 查询；禁用时，它会限制对受保护数据的原始 SQL 访问，但此漏洞绕过了这一限制。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://simonwillison.net/2026/Aug/6/datasette/">Release: datasette 1.0a38 | Simon Willison’s Weblog</a></li>
<li><a href="https://docs.datasette.io/en/stable/authentication.html">Authentication and permissions - Datasette documentation</a></li>

</ul>
</details>

**标签**: `#security`, `#sql-injection`, `#datasette`, `#open-source`, `#release`

---

<a id="item-21"></a>
## [非洲 AI 先驱倡导高效、任务专用模型](https://www.economist.com/middle-east-and-africa/2026/08/06/an-african-vision-of-artificial-intelligence) ⭐️ 7.0/10

《经济学人》2026 年 8 月的一篇文章报道，非洲科技先驱们提倡针对特定任务定制、只需极少算力的 AI 模型，与主流追求大规模、高算力 AI 系统的做法形成对比。 这一观点之所以重要，在于它挑战了“AI 发展必须依赖巨大计算资源”的假设，并表明资源受限地区可以提供可持续、易获取的替代方案，可能重塑全球 AI 生态。 该文章着重强调“适合特定任务”且“使用少量算力”的模型，更注重效率而非规模。文章摘要中没有提及具体名称或技术基准。

rss · The Economist · 8月6日 13:00

**背景**: 大型 AI 模型，如支持聊天机器人和图像生成的模型，需要海量数据和能源，且往往集中在发达国家。非洲开发者面临基础设施和资源限制，因此正探索以效率为先的设计，使其能在普通硬件上运行。这种做法与全球关于可持续 AI、降低 AI 环境与财务成本的讨论相契合。

**标签**: `#Artificial Intelligence`, `#Africa`, `#Efficient Computing`, `#Sustainable AI`, `#Task-Specific Models`

---

<a id="item-22"></a>
## [印度 IT 业经历 AI 考验，毕业生就业更难](https://www.economist.com/finance-and-economics/2026/08/06/indias-it-sector-is-surviving-artificial-intelligence) ⭐️ 7.0/10

《经济学人》在 2026 年 8 月 6 日发布的分析中指出，印度的 IT 行业正设法在人工智能的兴起中生存下来，但同样的技术却在恶化许多毕业生的就业前景。 这很重要，因为印度 IT 行业是就业和经济增长的主要来源，而 AI 对其劳动力的影响可能重塑该国的科技经济和高等教育的价值。 文章总结称，虽然该行业正在适应，但这种转变对初级员工几乎没有缓解作用，大学在更新课程方面的压力也在加大。

rss · The Economist · 8月6日 09:22

**背景**: 印度的 IT 服务业长期以来雇佣大量工程专业毕业生从事软件维护、测试和支持等工作。生成式 AI 如今正在自动化许多此类常规任务，减少了对初级员工的需求。该行业正转向 AI 模型开发和数字化转型等高价值工作，这要求比许多毕业生目前拥有的技能更高级。

**标签**: `#Artificial Intelligence`, `#India`, `#IT Sector`, `#Employment`, `#Economics`

---

<a id="item-23"></a>
## [Zig 的 Io.Threaded：简洁的 I/O 后端设计](https://matklad.github.io/2026/08/06/neat-io-threaded.html) ⭐️ 7.0/10

系统程序员 matklad 在 2026 年 8 月 6 日发布的一篇博客文章中剖析了 Zig 新的 Io.Threaded I/O 后端，并称赞其设计“简洁优雅”。文章着重展示了这个基于线程池的 std.Io 接口实现如何为并发提供了一种干净、简单的方案。 这一分析意义重大，因为 Zig 正在 0.16 版本中围绕 std.Io 接口重新设计其标准 I/O，而 Io.Threaded 是开发者将面临选择的两个关键后端之一。理解其设计有助于系统程序员评估 Zig 的并发模型——该模型倾向于用阻塞调用的简洁性取代异步复杂度。 Io.Threaded 是 Zig std.Io 中基于线程池的后端，它使用阻塞式系统调用，与基于异步/io_uring 的 Io.Evented 后端形成对比。std.Io 接口像 Zig 的 Allocator 模式一样作为参数传给函数，从而实现控制反转。

rss · Lobsters · 8月6日 20:12

**背景**: 传统上，Zig 通过 async/await 提供并发能力，但该语言已转向显式的 I/O 接口设计。这个新方案在 2025 年末公布，要求执行 I/O 的函数接受一个 std.Io 实现作为参数，内置选项包括 Io.Threaded 和 Io.Evented。Io.Threaded 将阻塞操作卸载到线程池，简单且可移植；Io.Evented 则利用 Linux io_uring 提供高性能异步 I/O。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://daily.dev/blog/zig-async-io-io-uring-zig-0-16-rethinks-concurrent-programming/">Zig Async I/O with io_uring: How Zig 0.16 Rethinks Concurrent Programming | daily.dev</a></li>
<li><a href="https://lwn.net/Articles/1046084/">Zig's new plan for asynchronous programs [LWN.net]</a></li>

</ul>
</details>

**标签**: `#Zig`, `#I/O`, `#Systems Programming`, `#Concurrency`

---

<a id="item-24"></a>
## [Xibalba64 开发记：在 2026 年制作 N64 游戏](https://phoboslab.org/log/2026/08/xibalba64-making-of) ⭐️ 7.0/10

Phobos Lab 的一篇全新技术向制作札记记录了 Xibalba64 的开发过程，这是一款在 2026 年为任天堂 64 开发的同人游戏。文中详细介绍了用于突破主机硬件限制的现代工具链与巧妙技巧。 这篇文章表明，得益于开源 SDK 和成熟的同人游戏社区，N64 等复古主机在 2026 年依然是游戏开发者面前一项兼具创造性与技术性的挑战。它深入展示了底层游戏编程，并为任何对约束驱动开发感兴趣的人提供了宝贵见解。 文章很可能探讨了开源 N64 SDK libdragon 的实际使用，以及如何通过闪存卡在真实硬件上测试。具体话题可能包括内存限制、RSP（Reality Signal Processor）编程，以及 N64 特有的渲染优化技巧。

rss · Lobsters · 8月6日 13:23

**背景**: 任天堂 64 于 1990 年代中期发售，采用 64 位 MIPS CPU 和基于协处理器的架构，与现代 GPU 截然不同。过去，N64 同人游戏开发非常困难，因为官方 SDK 为专有技术，而开发卡带价格昂贵。如今，libdragon 和 n64chain 等开源项目提供了完整工具链，使开发者能够用 C 语言编写游戏，并通过闪存卡在真实主机上运行。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://libdragon.dev/">Libdragon | Open source library for N 64 development.</a></li>
<li><a href="https://github.com/tj90241/n64chain">GitHub - tj90241/n64chain: A (free) open-source N64 development toolchain. · GitHub</a></li>
<li><a href="https://en.wikipedia.org/wiki/Flash_cartridge">Flash cartridge - Wikipedia</a></li>

</ul>
</details>

**标签**: `#game-development`, `#retro-computing`, `#N64`, `#technical-deep-dive`, `#homebrew`

---

<a id="item-25"></a>
## [celld 推出可自托管的分布式 Durable Objects](https://celld.dev/) ⭐️ 7.0/10

celld 是一个开源守护进程，可以在你自己的机器上运行 Cloudflare Workers 和 Durable Objects，提供一种不依赖云提供商的 Durable Objects 编程模型自托管实现。 这很重要，因为 durable objects 此前是 Cloudflare 的专有功能；celld 将该模型去中心化，让开发者可以控制放置、状态和运维基础设施。这有望减少供应商锁定，并将有状态 serverless 模式扩展到自托管和边缘环境。 celld 由 Deno 组织开发，是一个可以像数据库一样编程的分布式系统，将计算和存储结合在一个守护进程（daemon）中。它在保留熟悉的 Workers 编程模型的同时，实现了 Durable Objects 的自托管。

rss · Lobsters · 8月6日 22:21

**背景**: Durable Objects 是一种特殊的 Cloudflare Worker，它将计算与存储独特地结合在一起，充当处理多个并发请求的有状态 serverless 函数。celld 是一个开源替代方案，将该模型迁移到你选择的基础设施中，使放置、状态和运维证据可以独立于云提供商进行管理。该项目托管在 GitHub 的 denoland/celld 下，并将自己定位为可像数据库一样编程的分布式系统。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://celld.dev/">celld : self-hosted, distributed Durable Objects</a></li>
<li><a href="https://github.com/denoland/celld">GitHub - denoland/ celld : self-hosted, distributed Durable Objects</a></li>
<li><a href="https://developers.cloudflare.com/durable-objects/">Overview · Cloudflare Durable Objects docs</a></li>

</ul>
</details>

**标签**: `#durable objects`, `#self-hosting`, `#distributed systems`, `#serverless`

---

<a id="item-26"></a>
## [Crubit：C++/Rust 双向互操作工具发布](https://crubit.rs/) ⭐️ 7.0/10

Crubit 是一个新的双向绑定生成器，允许 C++ 和 Rust 代码互相调用，旨在整合这两个生态系统。该项目大约在 2022 年 10 月公开讨论。 这对系统编程和混合语言代码库意义重大，因为它是能在大型现有 C++ 代码库中逐步采用 Rust 的途径。这也反映了软件行业向更安全的系统编程发展的趋势。 根据 Reddit 评论，Crubit 优先考虑自动生成绑定，而不是让每种语言都写出地道的代码。其短期重点是那些大致遵循 Google C++ 风格指南的代码库，以提高互操作保真度。

rss · Lobsters · 8月6日 17:47

**背景**: C++ 和 Rust 都是系统编程语言，但它们的类型系统、内存模型和工具链不同，因此直接互操作很困难。此前，开发者使用 cxx 等工具来桥接两种语言，但这些工具通常需要手写包装器，或者更注重地道代码而非自动生成。Crubit 是一个双向绑定生成器，旨在高保真地整合两个生态系统，让 Rust 能与大型现有 C++ 代码库中的 C++ 共存。它由 Google 开发，文档见 crubit.rs。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://crubit.rs/design/design.html">High-level design of C++/Rust interop - Crubit Documentation</a></li>
<li><a href="https://www.reddit.com/r/rust/comments/xxfr4e/crubit_crust_bidirectional_interop_tool/">r/rust on Reddit: Crubit: C++/Rust Bidirectional Interop Tool</a></li>
<li><a href="https://crubit.rs/index.html">Home - Crubit Documentation</a></li>

</ul>
</details>

**社区讨论**: 在 Reddit 上，评论者指出 Crubit 的自动绑定生成与强调地道代码的 cxx 是不同的取舍。有人对是否存在一种适用于所有场景的方法表示怀疑，但也承认前期投入的工作可以防止 C++ 思维渗入 Rust 代码。

**标签**: `#C++`, `#Rust`, `#interop`, `#tools`, `#systems programming`

---

<a id="item-27"></a>
## [科学家首次让生菜和烟草产生动物肌红蛋白](https://www.reddit.com/r/science/comments/1vh0gzd/scientists_have_for_the_first_time_genetically/) ⭐️ 7.0/10

研究人员首次通过基因工程让生菜和烟草植株表达动物肌红蛋白。这种源自植物的蛋白质每公顷蛋白质产量有望与动物农业相当甚至更高，同时大幅降低水资源消耗和温室气体排放。 这一突破可能为生产植物基肉类替代品所需的含血红素蛋白质提供更可持续的途径。若能规模化，它有望降低蛋白质生产的环境足迹，并减少对动物养殖的依赖。 经过基因改造的植物会产生肌红蛋白——一种存在于肌肉组织中的铁和氧结合蛋白，赋予肉类颜色和风味。尽管产量前景可观，但这仍处于早期概念验证阶段，尚需进行食品安全评估和规模化生产。

reddit · r/science · /u/mvea · 8月6日 10:31

**背景**: 肌红蛋白是一种存在于脊椎动物骨骼肌和心肌中的铁氧结合蛋白，使肉类呈现红色，并是一种富含血红素的蛋白质。植物分子农业是此处使用的技术，通过基因工程使作物充当生物反应器，生产有价值的蛋白质或其他分子，这种方法在成本和规模上可能比传统发酵或基于动物的生产方式更具优势。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Myoglobin">Myoglobin</a></li>
<li><a href="https://forwardfooding.com/blog/foodtech-trends-and-insights/plant-molecular-farming-explained/">Unlocking the Potential of Plant Molecular Farming | Forward Fooding</a></li>

</ul>
</details>

**标签**: `#biotechnology`, `#genetic engineering`, `#sustainable food`, `#plant-based protein`, `#agriculture`

---

<a id="item-28"></a>
## [灵长类大脑增大或由视觉区域驱动，而非额叶](https://www.reddit.com/r/science/comments/1vhd4ye/research_suggests_primate_brains_didnt_get_big/) ⭐️ 7.0/10

一项分析跨越 5600 万年化石颅骨的研究发现，从树鼩到人类，额叶占大脑的比例保持恒定，而视觉处理区域则随视神经一起增大。 这项发现挑战了“灵长类大脑增大主要反映以额叶为中心的高级认知能力”的普遍假设，提示感觉处理（尤其是视觉）可能是大脑进化的主要驱动力。 该研究比较了跨越 5600 万年的化石颅骨，发现额叶占总脑容量的比例始终稳定。与此同时，视觉区域与视神经同步增大，表明进化选择主要作用于视觉回路，而非抽象认知。

reddit · r/science · /u/andmario_com · 8月6日 18:51

**背景**: 人们通常认为灵长类演化出较大的大脑是为了复杂的社交和认知能力，额叶被视为计划和决策的关键区域。这项研究提供了另一种视角：视觉系统——本就对灵长类树栖生活至关重要——在大脑增大的过程中可能比以往认为的更为关键。

**标签**: `#neuroscience`, `#evolution`, `#primatology`, `#brain`, `#vision`

---