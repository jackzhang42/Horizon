---
layout: default
title: "Horizon Summary: 2026-10-19 (ZH)"
date: 2026-10-19
lang: zh
---

> 从 55 条内容中筛选出 13 条重要资讯。

---

1. [系统管理员称 Namecheap 封禁其全部域名，再度引发注册商风险讨论](#item-1) ⭐️ 8.0/10
2. [Citizen Lab：Discover-Tech 利用定向广告投放零点击间谍软件](#item-2) ⭐️ 8.0/10
3. [SGLang v0.5.22 发布：950 个 PR，新增扩散模型与嵌入模型支持](#item-3) ⭐️ 7.0/10
4. [Together Computer 发布 HybridAgent：在潜空间思考、用文本行动的 LLM 智能体](#item-4) ⭐️ 7.0/10
5. [Linear 创始人 Karri Saarinen：好软件留有创造者的印记](#item-5) ⭐️ 7.0/10
6. [RepRapMicron：开源微米级 3D 打印机项目](#item-6) ⭐️ 7.0/10
7. [Java 密封类配合穷尽式 switch 可能破坏二进制兼容性](#item-7) ⭐️ 7.0/10
8. [开源 DIY 微操作平台实现亚微米级三维定位](#item-8) ⭐️ 7.0/10
9. [博客文章提出以“逆向”视角理解借用检查](#item-9) ⭐️ 7.0/10
10. [对 FPU 模拟器做超优化：自动搜索找到巧妙的改写方案](#item-10) ⭐️ 7.0/10
11. [深入 Intel 8087 芯片：微码层面的浮点加减法实现](#item-11) ⭐️ 7.0/10
12. [OOPSLA 2026 论文将高效 E-graph 提取扩展到含副作用的程序](#item-12) ⭐️ 7.0/10
13. [Ghidra 与 CBMC 结合打造汇编模型检查器](#item-13) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [系统管理员称 Namecheap 封禁其全部域名，再度引发注册商风险讨论](https://www.reddit.com/r/sysadmin/comments/1x8cycd/namecheap_just_seized_and_disabled_all_my_domains/) ⭐️ 8.0/10

一位系统管理员在 r/sysadmin 发帖称，Namecheap 在没有任何预警的情况下查封并停用了他的全部域名，该事件迅速传播到 Hacker News，获得 557 分和 287 条评论。讨论随即演变为对域名注册商集中风险的全面反思，并援引了 Namecheap 以往的多起事件，例如将账户交给未经核实的第三方，以及 2013 年暂停 Imgur 域名。 域名注册是每一项在线业务的单点故障，因此一个能在短时间内停用整个账户的注册商，会让生产环境的邮件、DNS 和网站同时陷入风险，且没有技术手段可以绕过。这场讨论的意义在于，它促使团队把注册商当作关键基础设施供应商来评估，而不是当作一次普通采购。 最初的 Reddit 帖子既没有给出处理结果，也没有提供 Namecheap 方面的说法；评论者指出，美国注册商依据服务条款基本可以自由终止服务，言论自由保护并不适用。评论者 ericholscher 描述了类似案例：因未在 48 小时内回复一封钓鱼邮件，其业务域名被关闭，升级处理后又花了六个多小时才恢复。

hackernews · sashk · 10月18日 16:56 · [社区讨论](https://news.ycombinator.com/item?id=50142866)

**背景**: 域名注册商是经 ICANN 认证、持有域名注册记录并控制其指向哪些 nameserver 的公司，这意味着它可以在注册局层面暂停一个域名，无论客户自己的服务器状态如何。注册商受 ICANN 合同和 UDRP 等争议解决政策约束，但这些规则主要处理商标冲突，而非账户层面的停用；美国注册商还可以依据自身条款终止服务。此次讨论的背景是，CVC Capital Partners 于 2025 年 9 月同意收购 Namecheap 的多数股权，含债务估值约 15 亿美元，用户普遍预期这笔交易会带来削减成本以及客服更多依赖自动化。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://webhosting.today/2025/09/12/cvc-acquires-majority-stake-in-namecheap-for-1-5-billion/">CVC acquires majority stake in Namecheap for $1.5 billion</a></li>
<li><a href="https://domaingang.com/domain-news/cvc-secures-1-5-billion-acquisition-of-namecheap/">CVC Secures $1.5 Billion acquisition of Namecheap</a></li>
<li><a href="https://news.ycombinator.com/item?id=17657701">So what happens when a domain registrar seizes your... | Hacker News</a></li>

</ul>
</details>

**社区讨论**: 评论者几乎一致持批评态度，并列举了一系列事件：账户被转给未经核实的第三方、仅因一条只有 6 个赞的含糊推文就封禁域名、2013 年暂停 Imgur；不少人把这些行为与 2025 年的私募股权收购以及 .com 价格上涨联系起来。主流建议是谨慎选择注册商并为其真人客服付费，bluehatbrit 和 teddyh 认为在注册商上省钱是因小失大，并推荐 Mythic Beasts 等小型或本地服务商。

**标签**: `#domains`, `#registrars`, `#namecheap`, `#sysadmin`, `#infrastructure-risk`

---

<a id="item-2"></a>
## [Citizen Lab：Discover-Tech 利用定向广告投放零点击间谍软件](https://citizenlab.ca/research/how-discover-tech-turned-targeted-ads-into-a-pipeline-for-spyware/) ⭐️ 8.0/10

Citizen Lab 与广告安全公司 Confiant 合作发布研究，披露以色列广告公司 Discover-Tech 如何利用其名为 Controlium 的广告平台，在广告渲染的瞬间对设备进行去匿名化、指纹识别并自动植入恶意代码，从而为雇佣式间谍软件合作方实施零点击攻击。Citizen Lab 将这份报告命名为“AdFection”，指出定向广告已成为间谍软件一条真实可用的分发渠道，而非偶然的附带现象。 这一发现把在线广告基础设施本身重新定义为攻击面：任何只是打开一个带有广告位的页面的用户，都可能在毫无点击的情况下被画像甚至被入侵，从而使“不要点可疑链接或附件”这类常规建议失效。它也向广告交易平台、发布商和监管机构提出了尖锐问题：谁有资格购买广告库存，以及夹在中间的广告技术中介究竟受到怎样的审查。 研究指出，Controlium 允许合作厂商利用广告定向信号决定要针对哪些人，随后在广告渲染时自动触发植入过程，因此完全不需要用户进行任何交互。报告点名了 Discover-Tech 及其平台，并把这一做法描述为面向多家雇佣式间谍软件厂商提供的服务，而非单次行动。

rss · Lobsters · 10月18日 20:55

**背景**: 零点击间谍软件是指受害者无需任何操作——不用点链接、不用打开文件——就能被植入的恶意软件，通常依靠利用处理传入数据的软件中的漏洞实现。Citizen Lab 是多伦多大学下属的跨学科研究中心，多年来持续记录针对记者、活动人士和异见者的商业间谍软件与数字监控活动。与此同时，定向广告依赖对每位访客的详细画像与指纹数据运行，而这恰恰是攻击者判断“谁值得下手”所需要的信息。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://citizenlab.ca/research/how-discover-tech-turned-targeted-ads-into-a-pipeline-for-spyware/">Exposing AdFection: How Discover-Tech Turned Targeted Ads ...</a></li>
<li><a href="https://www.theverge.com/tech/1011956/discover-tech-zero-click-ads-spyware">An Israeli firm is sending spyware through online ads ...</a></li>

</ul>
</details>

**标签**: `#spyware`, `#surveillance`, `#targeted-advertising`, `#cybersecurity`, `#privacy`

---

<a id="item-3"></a>
## [SGLang v0.5.22 发布：950 个 PR，新增扩散模型与嵌入模型支持](https://github.com/sgl-project/sglang/releases/tag/v0.5.22) ⭐️ 7.0/10

SGLang v0.5.22 正式发布，包含来自 245 位贡献者的 950 个 PR，新增了对一批 LLM、VLM、嵌入模型和扩散模型的支持，包括 Clef/Clef Flash、PPLX-Decider v1.1、EmbeddingGemma 2、LLaDA2.2、HunyuanImage-3.0-Instruct、Kandinsky 6、Wan-Animate-2、SANA-Video 2.0 以及 LLaDA-Image。该版本还带来了显著的性能提升，例如 DeepSeek-V4.1 在 H200 上单 GPU 吞吐最高提升 2.3 倍，MiMo-V2.6-Pro 在 B300 上借助 DFlash 实现 1.85 倍解码吞吐，全新的 InstantTensor 加载器让模型加载速度提升 10 倍。 SGLang 是目前使用最广泛的开源大模型服务框架之一，因此每次版本更新都会直接影响在 NVIDIA、AMD、Intel 等硬件上部署模型的生产团队的推理成本与延迟。本次更新把能力从自回归文本服务扩展到扩散图像/视频生成与嵌入模型，使团队能够将过去分散的多套服务栈整合到一个引擎中；同时吞吐与模型加载方面的改进无需新增硬件即可降低单请求成本。 SGLang 现在要求 Python 3.11 或更高版本，并提供面向 NVIDIA CUDA 13、AMD MI35x/MI30x、Intel GPU 和 Intel CPU 的预构建 Docker 镜像。其他值得注意的改动包括：PD（预填充-解码）分离在长提示词负载下吞吐最高提升 27% 且 p95 TTFT 减半；HiSparse 支持 EAGLE 与 MTP，并将 KV 缓存放在 CPU 内存中；在 MLX 之外新增基于标准 PyTorch 后端的 Apple Silicon 支持；以及修复了混合线性模型在同时使用投机解码与结构化输出时可能从错误的 mamba 状态恢复的问题。

github · ch-wan · 10月19日 02:55

**背景**: SGLang 是一个面向大语言模型和多模态模型的开源高性能服务框架，最初由加州大学伯克利分校开发、现由 LMSYS 托管；它采用 RadixAttention 实现 KV 缓存自动复用、前缀缓存、多 GPU 并行，并提供兼容 OpenAI 的 API，常被拿来与 vLLM 和 TensorRT-LLM 比较。其发布说明默认读者熟悉预填充-解码分离（把提示词处理与逐 token 生成拆分到不同工作节点）、投机解码（先草拟多个 token 再一次性验证）以及 KV 缓存卸载等概念。本次新增的扩散模型条目——LLaDA 系列离散扩散语言模型，以及 Wan-Animate-2 等视频/图像生成模型——反映了非自回归模型和生成式媒体模型正越来越多地由同一批推理引擎来承载的趋势。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.sglang.io/">SGLang – Fast, Open-Source LLM & Multimodal Serving Framework</a></li>
<li><a href="https://github.com/sgl-project/sglang">GitHub - sgl-project/sglang: SGLang is a high-performance ... vLLM vs SGLang: Inference Engine Comparison 2026 - turion.ai Best LLM Inference Engines (2026): vLLM, SGLang & TensorRT-LLM SGLang: The Complete Guide to High-Performance LLM Inference Welcome to SGLang - SGLang Documentation LLM Inference Engines Compared: vLLM, SGLang, Ollama & llama ...</a></li>
<li><a href="https://arxiv.org/abs/2502.09992">[2502.09992] Large Language Diffusion Models - arXiv.org GitHub - ML-GSAI/LLaDA: Official PyTorch implementation for ... [2512.15745] LLaDA2.0: Scaling Up Diffusion Language Models ... GitHub - inclusionAI/LLaDA2.X: LLaDA2.0 is the diffusion ... LLaDA - Large Language Diffusion Models - ml-gsai.github.io Large Language Diffusion Models - proceedings.neurips.cc LLaDA: The Diffusion Model That Could Redefine Language ...</a></li>

</ul>
</details>

**标签**: `#LLM inference`, `#model serving`, `#release notes`, `#diffusion models`, `#open source`

---

<a id="item-4"></a>
## [Together Computer 发布 HybridAgent：在潜空间思考、用文本行动的 LLM 智能体](https://arxiv.org/abs/2610.18861) ⭐️ 7.0/10

Together Computer 发布了 HybridAgent，这是一个开放的 LLM 智能体框架，能够在连续的潜空间中进行推理，并与常规的文本行动交替进行，同时附带了论文（arXiv:2610.18861）、GitHub 代码和 Hugging Face 模型权重。该框架通过一个名为 HybridLink 的轻量模块，把模型最后一层的隐藏状态映射回输入嵌入空间，使智能体可以先切换到潜空间“思考”模式，再回到文本模式执行工具调用并给出最终答案。 潜空间推理长期被视为比逐 token 的思维链更快的替代方案，但前沿实验室大多回避在这一方向公开发表成果，因为不透明的思考过程更难被监控。此次由知名推理服务商发布带代码和权重的开放、可复现成果，把这一路线带入了公共智能体生态，有望降低智能体任务的推理时间和 token 成本，同时也重新点燃了关于可解释性的争论。 作者称在 11 个基准和 3 种模型规模上进行了评测，结果优于基于文本和基于潜空间推理的智能体基线，同时显著降低了推理时间、token 用量和计算成本。不过，一位早期用户测试社区量化的 8B GGUF 版本（IQ4_XS）时发现，面对“谁是教皇？”这样简单的问题，模型会陷入无休止的思考循环，说明在小规模、低精度条件下仍存在稳健性问题。

hackernews · allinonai · 10月18日 20:48 · [社区讨论](https://news.ycombinator.com/item?id=50145337)

**背景**: 目前大多数 LLM 智能体通过写出思维链文本来进行“推理”：中间步骤以普通 token 的形式生成，过程透明、可审计，但速度慢且消耗大量 token。另一条研究路线（如 Hao 等人的 Coconut 方法）则直接在模型连续的隐藏状态——即“潜空间”——中完成同样的计算，效率更高，但不会产生人类可读的推理痕迹。HybridAgent 试图兼得两者：用快速紧凑的潜空间思考完成内部推演，在需要调用工具或被监控时再输出文本。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/togethercomputer/HybridAgent">GitHub - togethercomputer/HybridAgent</a></li>
<li><a href="https://arxiv.org/html/2610.18861v1">Hybrid Reasoning Agents - arXiv.org</a></li>
<li><a href="https://arxiv.org/pdf/2412.06769">Training Large Language Models to Reason in a Continuous Latent ...</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的评论者主要聚焦安全问题：有人认为潜空间思考会增强模型的欺骗能力、让监控更难，并将其与 OpenAI 在输出思考 token 之前先跑多遍网络的做法相类比；另一位则称潜空间推理之所以近乎禁忌，正是因为可解释性和对齐方面的顾虑。还有用户报告了具体的失败案例——量化后的 8B 模型在简单问题上无限循环；也有人建议更进一步，加宽嵌入层，让潜向量与 token 嵌入始终同时传入模型。

**标签**: `#LLM agents`, `#latent reasoning`, `#AI alignment`, `#interpretability`, `#open-source models`

---

<a id="item-5"></a>
## [Linear 创始人 Karri Saarinen：好软件留有创造者的印记](https://karrisaarinen.com/posts/someone-behind-the-software/) ⭐️ 7.0/10

项目管理工具 Linear 的联合创始人兼 CEO Karri Saarinen 发表了题为《Someone Behind the Software》的文章，主张优秀的软件会清晰地显露出构建者的存在感与价值观。该文在 Hacker News 上获得 417 分和 158 条评论，读者更多是在延伸而非反驳这一观点。 这篇文章出现的时机颇为关键：AI 代码生成正让纯粹的编码实现日益商品化，开发者与产品团队不得不转而依靠品味、产品愿景以及"该做什么"的判断力来证明自身价值。同时，它也把当下的产品设计讨论重新接回了更早的"软件工艺"（software craftsmanship）传统——这一传统一直坚持软件是由匠人塑造的手艺，而非纯粹的工业化产出。 讨论中被引用最多的观点是多萝西·塞耶斯（Dorothy Sayers）提出的创造性活动三阶段——理念、实现与互动，弗雷德里克·布鲁克斯曾在《人月神话》中引用过这一说法；评论者用它来解释为何用户只能接触到第三阶段，因而必须去推测其背后的作者。另有评论者指出，增加新能力远比重新思考已有能力容易，于是产品往往不断堆叠功能，却始终无法形成统一的观点。

hackernews · tosh · 10月18日 16:32 · [社区讨论](https://news.ycombinator.com/item?id=50142573)

**背景**: Linear 是一款面向软件工程团队的项目与问题追踪工具，以速度快、设计精良著称，被 Vercel、OpenAI、Ramp 等公司使用，常被视为"产品形态反映强烈观点"的典型。它所呼应的软件工艺运动源于 1990 至 2000 年代的敏捷开发思潮：Jack W. Reeves 在 1992 年的文章《What Is Software Design?》中提出软件开发既是手艺也是工程学科，2009 年的《软件工艺宣言》则呼吁提升职业开发的水准。讨论中提到的塞耶斯三阶段框架，最经典的出处是弗雷德里克·布鲁克斯 1975 年关于软件项目管理的名著《人月神话》。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://linear.app/">Linear – The system for product development</a></li>
<li><a href="https://en.wikipedia.org/wiki/Software_craftsmanship">Software craftsmanship - Wikipedia</a></li>
<li><a href="https://manifesto.softwarecraftsmanship.org/">Manifesto for Software Craftsmanship</a></li>

</ul>
</details>

**社区讨论**: 整体情绪积极，且以补充延伸为主。一位自称 Linear 粉丝的评论者认为，该公司有一项被低估的优势：它自己就是自己的客户，因此可以直接在 Linear 里追踪 Linear 的开发，而不像多数厂商那样必须在术语不兼容的领域之间翻译需求。一位 SaaS 开发者表示认同，认为如今价值既不在代码、甚至也不在架构（AI 在这些方面正快速追赶），而在于决定该做什么、不该做什么；也有人感慨，大多数产品都在扩张成什么都做的"超级产品"，却难以维持一个自洽的观点。

**标签**: `#software-craft`, `#product-design`, `#engineering-culture`, `#AI-and-development`, `#essay`

---

<a id="item-6"></a>
## [RepRapMicron：开源微米级 3D 打印机项目](https://github.com/VikOlliver/RepRapMicron/wiki) ⭐️ 7.0/10

由 Vik Olliver 主导的 RepRapMicron 项目（又称 μRepRap）发布了一份 wiki 文档，描述了一种三轴 3D 打印机机构，定位精度可达几微米，特征尺寸为 10μm–20μm。该项目设计为可使用标准 3D 打印机与 CNC 控制器，并由普通 3D 打印爱好者用廉价常见零件自行搭建。 如果微米级制造能够做到廉价且可在车库里复现，它将像 RepRap 对桌面 FDM 打印所做的那样改变微纳制造，让爱好者和小型实验室能够实际制作微结构和芯片级设计，而不再只是把设计文件留在电脑里。Hacker News 上那条获得 379 分的讨论帖显示出人们对这一想法的强烈兴趣。 该设计借助显微镜平台技术实现精密运动，目标是几微米的机械精度和 10μm–20μm 的特征尺寸，并刻意保持与现成的 3D 打印机和 CNC 电子器件兼容。它目前仍是一个进行中的 wiki 项目，而非已展示的突破性成果，所谓千分之一比例的自复制也只是推测而非已验证。

hackernews · RobotToaster · 10月18日 13:48 · [社区讨论](https://news.ycombinator.com/item?id=50141076)

**背景**: RepRap（“replicating rapid prototyper”的缩写）是始于 2000 年代中期的开源项目，目标是制造低成本的桌面 3D 打印机，使其能打印自身大部分塑料零件，所有设计均以 GNU GPL 发布。传统微米级三维微纳制造通常依赖专门且昂贵的实验室技术与设备。RepRapMicron 将 RepRap 的自复制理念和低成本路线向下延伸到更小尺度，力图让微米级制造得到广泛普及。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://reprap.org/wiki/RepRapMicron">RepRapMicron - RepRap GitHub - VikOlliver/RepRapMicron: μRepRap - A 3D printer ... RepRapMicron Micron Scale 3D Printer by vik - Thingiverse RepRapMicron V0.04 - micron accurate 3D printer RepRapMicron Micron Scale 3D Printer by vik - Thingiverse RepRapMicron V0.03 - micron accurate 3D printer by Vik ... RepRapMicron - hn.today</a></li>
<li><a href="https://github.com/VikOlliver/RepRapMicron">GitHub - VikOlliver/RepRapMicron: μRepRap - A 3D printer ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/RepRap">RepRap - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者将这一刻类比为 18 世纪 90 年代末：Ramsden（分度机与精密刻度）、Maudslay（螺纹车床）和 Wilkinson（镗床）等先驱把精密加工从手艺活变成了可稳定复制的制造。也有人对廉价、可持续地制造那些目前只存在于软件中的芯片设计充满热情，同时有人质疑一台机器打印出自身千分之一比例版本的可能性。

**标签**: `#3d-printing`, `#reprap`, `#microfabrication`, `#open-hardware`, `#self-replication`

---

<a id="item-7"></a>
## [Java 密封类配合穷尽式 switch 可能破坏二进制兼容性](https://neilmadden.blog/2026/04/24/java-sealed-classes-and-exhaustive-pattern-matching/) ⭐️ 7.0/10

Neil Madden 发表博客文章指出：针对密封类型编写的穷尽式 switch 在编译时能顺利通过，但当拥有该密封类型的库后来新增了一个许可子类、而使用方未重新编译时，这段代码会在运行时抛出 MatchException。他以 JDK 26 的 PEM 编码 API（JEP 542）为例，说明其密封类层次结构恰好暴露了这一风险。 穷尽性检查是密封类最主要的卖点之一，它让开发者可以省去防御性的 default 分支；但本文表明，这一保证只存在于编译期，在库版本升级后会悄然失效。任何对外暴露密封层次结构的 Java 库——包括 JDK 本身——都必须把新增许可子类视为事实上的破坏性变更。 编译器只有在编译使用方代码时才能发现 switch 不穷尽，因此针对旧版 jar 编译的使用方会带着过时的许可子类清单继续运行。此外，密封层次结构要求所有许可子类与密封类位于同一模块（若在未命名模块中则需同一包），这意味着子类集合完全由库作者掌控，而非调用方。

hackernews · hnisjafx40 · 10月18日 14:47 · [社区讨论](https://news.ycombinator.com/item?id=50141579)

**背景**: 密封类（sealed classes）在 Java 17 中正式定稿，允许作者通过 permits 子句精确声明哪些类可以继承某个类型。随后在 Java 21 中定稿的 switch 模式匹配可以对这类类型做穷尽性检查，从而无需 default 分支。JEP 542 在 JDK 26 中引入一套预览 API，用于在 Privacy-Enhanced Mail（PEM）文本格式下编码和解码密码学密钥、证书与 CRL，其 PEM 对象模型正是构建在密封类型层次之上。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openjdk.org/jeps/542">JEP 542: PEM Encodings of Cryptographic Objects - OpenJDK</a></li>
<li><a href="https://docs.oracle.com/en/java/javase/26/docs/api//java.base/java/security/PEMEncoder.html">PEMEncoder (Java SE 26 & JDK 26) - docs.oracle.com</a></li>
<li><a href="https://www.baeldung.com/java-sealed-classes-interfaces">Sealed Classes and Interfaces in Java | Baeldung</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍认为这一行为很危险：misja111 主张新增许可子类应当被视为二进制兼容性破坏，而不应让使用方在替换 jar 后遭遇运行时错误。smarks 确认了上下文是 JDK 26 的 PEM 编码 API，并证实若未来 JDK 新增许可子类确实会带来 MatchException 风险；DimmieMan 则表示相比 C# 的做法，他仍更青睐 Java 的 sealed 关键字与使用体验；还有人提到 TypeScript 的 ts-pattern 库以及 Java 的递归模式与字面量模式。

**标签**: `#java`, `#pattern-matching`, `#sealed-classes`, `#binary-compatibility`, `#language-design`

---

<a id="item-8"></a>
## [开源 DIY 微操作平台实现亚微米级三维定位](https://github.com/0x23/MicroManipulatorStepper) ⭐️ 7.0/10

开发者 0x23 在 GitHub 上发布了 MicroManipulatorStepper，这是一个开源、低成本的电动 XYZ 微操作平台，使用现成的步进电机和自制结构件搭建，据称可实现亚微米级精度，最小步进可达 50 纳米。该项目在 Hacker News 上引发了大量关注，评论者称其为令人印象深刻的 DIY 精密工程作品。 用于探针台和显微操作的商用微操作器通常售价数千美元，因此一个千美元以下级别的开源硬件设计降低了爱好者、小型实验室和开放科学团队的使用门槛。它也壮大了不断发展的开源实验室工具生态，这类廉价可复制的仪器正越来越多地用于光学对准、电子元件探测和显微观察。 该设计依靠普通步进电机配合高比例减速（通过细牙丝杠和齿轮传动），把较粗的电机步距转化为纳米级位移，目标应用包括光学对准、电子元件探测和显微观察。由于它是一套以电机驱动、基本为开环的机械结构，实际精度不仅取决于步距分辨率，还取决于背隙、结构刚度和热漂移。

hackernews · _Microft · 10月18日 11:16 · [社区讨论](https://news.ycombinator.com/item?id=50140001)

**背景**: 微操作器是一种能在微米到纳米尺度上精确移动探针、工具或样品的装置，通常配合显微镜使用，在电生理学、半导体探测和微组装中不可或缺。多数商用系统采用步进电机加精密丝杠或压电驱动器，而压电粘滑式设计能以更高成本实现更细的分辨率。开源硬件项目正越来越多地尝试用 3D 打印件和通用元器件复刻这类实验室设备，使其可以低成本地搭建和维修。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/0x23/MicroManipulatorStepper">GitHub - 0x23/MicroManipulatorStepper: A sub-micrometer 3D ...</a></li>
<li><a href="https://daily.dev/posts/open-micromanipulator-a-sub-micrometer-3d-motion-control-plattform-xceqae2du">Open MicroManipulator – A sub-micrometer 3D motion control ...</a></li>
<li><a href="https://docs.hackerfab.org/home/working-docs/nanopositioner-wip/micromanipulator">Micromanipulator | Hacker Fab</a></li>

</ul>
</details>

**社区讨论**: 评论者整体反应热烈：有人询问能否基于同样的连杆原理做出六自由度/六足版本，并希望给出可预测的工作空间以及刚度、精度数据；也有人指出 RepRap Micron 项目在做类似的事情。还有人称赞作者在 YouTube 上的搭建系列视频，提到引用一篇开源纳米定位论文的自制压电粘滑驱动器能以约 1000 美元实现亚纳米分辨率，并希望作者推出 Kickstarter 产品。

**标签**: `#open-source hardware`, `#precision engineering`, `#micromanipulator`, `#DIY electronics`, `#3D motion control`

---

<a id="item-9"></a>
## [博客文章提出以“逆向”视角理解借用检查](https://verdagon.dev/blog/reverse-borrow-checking) ⭐️ 7.0/10

编程语言博主 Evan Ovadia（verdagon）发表了一篇深入的技术文章，提出借用检查（borrow checking）可以从“逆向”来理解和实现——即从函数结尾向开头回溯，而非从入口点正向推进。文章介绍了他的 Valen 借用检查器如何反向工作，追踪使用、修改与声明，以检测释放后使用（use-after-free）错误，据称在处理循环时尤其简洁。 借用检查是 Rust 内存安全保证背后的核心机制，因此任何对该算法的替代性表述，对编译器开发者和试图以更低阻力构建更安全系统级语言的设计者都具有吸引力。如果一种视角能让循环处理和释放后使用分析变得更简单，就可能降低在 Rust 生态之外的新语言中实现借用检查器的门槛。 文章明确表示这是对借用检查算法的一次深入“底层”剖析，而不是入门科普，作者也说明它面向希望了解算法细节的读者。从结尾到开头的逆向遍历被作为一种替代视角，用来追踪使用、修改与声明，其宣称的优势是能更简单地检测释放后使用错误，尤其是在涉及循环的情况下。

rss · Lobsters · 10月18日 14:29

**背景**: 借用检查是执行 Rust 所有权模型的静态分析：每个值都有唯一的所有者，其他代码只能以不可变（共享读）或可变（独占写）的方式临时“借用”它，编译器会拒绝违反这些规则的程序。经典做法是沿着程序正向推进，追踪在每个程序点上哪些借用仍然存活，而当控制流出现分支和循环时，这一分析会变得相当复杂。正因为这种分析是在没有垃圾回收器的情况下防止释放后使用和数据竞争的关键，编译器研究者一直在探索更易实现、更易推理的替代表述方式。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://verdagon.dev/blog/reverse-borrow-checking">A New Way to Think About Borrow Checking (In Reverse)</a></li>
<li><a href="https://x.com/rustaceans_rs/status/2112028670785102073">Rust Bytes on X: "A New Way to Think About Borrow Checking ...</a></li>
<li><a href="https://rustc-dev-guide.rust-lang.org/borrow-check.html">The borrow checker - Rust Compiler Development Guide</a></li>

</ul>
</details>

**标签**: `#borrow checking`, `#memory management`, `#programming languages`, `#static analysis`, `#Rust`

---

<a id="item-10"></a>
## [对 FPU 模拟器做超优化：自动搜索找到巧妙的改写方案](https://purplesyringa.moe/blog/superoptimizing-an-fpu-emulator/) ⭐️ 7.0/10

purplesyringa 的一篇博客文章介绍了如何将超优化（superoptimization，即自动搜索最优指令序列的技术）应用于一个仍在开发中的浮点运算单元（FPU）模拟器。作者表示，当工具发现了一个出乎意料的巧妙改写时感到“目瞪口呆”，而这段代码如今已被用于该模拟器中。 超优化器通常只在很小的玩具内核或简短的 ALU 指令序列上做演示，因此它在模拟器中的一次真实应用，对任何从事位精确（bit-exact）系统工作的开发者来说都是有价值的参考。这也说明，在浮点模拟这类向来依赖手工调优代码的领域，自动搜索依然能让专家感到意外。 超优化通常只能处理简短的、无循环的指令序列，并且在内存访问和控制流方面表现不佳，因此它更适合针对独立的 FPU 辅助函数，而无法处理整个程序。此外，FPU 模拟要求严格遵循 IEEE-754 语义——包括 NaN 传播、舍入模式和异常标志——所以任何替换后的指令序列都必须对照原始行为进行验证。

rss · Lobsters · 10月18日 23:51

**背景**: 超优化最早由 Henry Massalin 在 1987 年探索，其目标是为一小段代码找到理论上最优的指令序列，常见做法是按代价顺序枚举候选序列，并逐一用规范说明或输入输出样例来检验其正确性。像 LLVM 这样的普通编译器只是逐步改进代码，而超优化器则试图寻找一个可证明等价的规范形式替换方案——Souper 等现代工具已经把优化建议反哺给了 LLVM 和 MSVC。FPU 模拟指的是用软件实现浮点硬件，这在 FPU 为可选或缺失的 CPU 上，以及在必须精确复现目标机器数值行为的模拟器中都是必需的。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://purplesyringa.moe/blog/superoptimizing-an-fpu-emulator/">Superoptimizing an FPU emulator | purplesyringa's blog</a></li>
<li><a href="https://en.wikipedia.org/wiki/Superoptimization">Superoptimization - Wikipedia</a></li>
<li><a href="https://www.embecosm.com/appnotes/ean15/ean15.html">Superoptimization - Embecosm Superoptimization – Embecosm Compiler Optimization via Superoptimization - GitHub Pages CS 6120: Superoptimization: a quest for -O∞ Understanding Superoptimization - bongjunj.github.io SuperCoder: Assembly Program Superoptimization with Large ...</a></li>

</ul>
</details>

**标签**: `#superoptimization`, `#emulation`, `#FPU`, `#performance`, `#compilers`

---

<a id="item-11"></a>
## [深入 Intel 8087 芯片：微码层面的浮点加减法实现](https://www.righto.com/2026/10/8087-addition-subtraction-microcode.html) ⭐️ 7.0/10

Ken Shirriff 在 righto.com 发布的最新深度分析（2026 年 10 月）详细剖析了 Intel 8087 协处理器中实现浮点加法和减法的微码。文章梳理了芯片裸片的布局：中央的矩形微码 ROM 存放着 1648 条微指令，而芯片下半部分则是执行 80 位浮点运算的数据通路。 8087 奠定了 x87 浮点编程模型，深刻影响了几十年来的 PC 数值计算；理解这颗 1980 年代的芯片如何在有限的晶体管预算下满足类 IEEE 754 的精度要求，对研究硬件与软件数值计算的人很有价值。它也具体展示了在专用流水线浮点单元出现之前，微码作为固件层如何让复杂的浮点指令变得可行。 文章将加减法拆解为加法器、移位器（负责对阶与规格化）以及指数转换器各自承担的职责，这些部件都作用于 8087 的 80 位内部数值。8087 与后续 Intel 协处理器不同，它直接挂在 8086 的地址总线和数据总线上，通过监视指令流中以前缀位 "11011" 开头的操作码来识别属于自己的指令。

rss · Lobsters · 10月18日 17:59

**背景**: Intel 8087 于 1980 年前后推出，是 8086/8088 的可选数学协处理器，用硬件实现 80 位扩展精度的浮点运算，取代了缓慢的软件模拟。微码是存放在片上 ROM 中的一层底层指令，通过编排数据通路来完成一条复杂的机器指令；研究微码可以精确揭示芯片如何在速度与精度之间取舍。Ken Shirriff 以这种裸片显微摄影逆向分析而闻名，此前他还发表过对 8087 的 FSCALE 指令微码的类似分析。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.righto.com/2026/10/8087-addition-subtraction-microcode.html">Inside the Intel 8087 chip: floating-point addition and ...</a></li>
<li><a href="https://www.righto.com/2026/09/8087-microcode-reverse-engineering-fscale.html">Microcode in Intel's 8087 floating-point chip: the scale ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Intel_8087">Intel 8087 - Wikipedia</a></li>

</ul>
</details>

**标签**: `#Intel 8087`, `#floating point`, `#microcode`, `#reverse engineering`, `#computer history`

---

<a id="item-12"></a>
## [OOPSLA 2026 论文将高效 E-graph 提取扩展到含副作用的程序](https://ztatlock.net/pubs/2026-oopsla-eggcc/) ⭐️ 7.0/10

一篇被 OOPSLA 2026 接收、由 Oliver Flatt 与另外九位作者合著的论文，提出了一种针对含副作用表达式的 e-graph 的高效提取（extraction）算法——这里的副作用指其内存与 I/O 操作必须彼此保持先后顺序的项。这一工作把此前主要适用于纯项的等价饱和（equality saturation）类 e-graph 技术，扩展到了具有可观察副作用的程序上。 E-graph 近年推动了程序优化、程序合成与程序验证的进展，但由于重写必须保持内存与 I/O 副作用的顺序，它们一直难以应用于真实的命令式代码。让含副作用的 e-graph 提取变得可行，有望使这些技术进入带可变状态和副作用的语言的编译器与合成工具，而不只局限于纯函数式或特定领域场景。 提取——即从 e-graph 所表示的众多等价项中选出代价最低的一个——本身在一般情况下就是 NP 难的，通常用自底向上的代价动态规划求解，而该方法默认子项可以自由重排。副作用引入了顺序约束，打破了这一假设，因此该论文的贡献在于一种在尊重副作用顺序的同时仍保持高效性的提取方法；具体算法细节与评测中的局限性需参阅原文。

rss · Lobsters · 10月19日 04:15

**背景**: E-graph 是一种紧凑地存储某个语言中项之间等价关系的数据结构，它共享公共子项，而不枚举所有等价变体。等价饱和利用 e-graph 以非破坏性的方式应用重写规则，累积所有等价程序而非只选定一个，随后再由提取步骤从这一空间中挑出最优程序。当一个表达式的求值不只是返回一个值，还会写内存、执行 I/O 或以其他方式与外部世界交互时，它就被称为“含副作用的”（effectful），这意味着任何改变这些操作先后次序的重写都不能随意互换。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2609.31887">[2609.31887] Efficient Extraction for Effectful E - Graphs</a></li>
<li><a href="https://ztatlock.net/pubs/2026-oopsla-eggcc/">Efficient Extraction for Effectful E - graphs</a></li>
<li><a href="https://en.wikipedia.org/wiki/E-graph">E-graph - Wikipedia</a></li>

</ul>
</details>

**标签**: `#e-graphs`, `#compiler-optimization`, `#program-synthesis`, `#effect-systems`, `#program-verification`

---

<a id="item-13"></a>
## [Ghidra 与 CBMC 结合打造汇编模型检查器](https://www.philipzucker.com/asmc_cpp/) ⭐️ 7.0/10

一个名为 Assembly Model Checker 的项目将 Ghidra 的反汇编能力与 CBMC 的有界模型检查结合起来，用于验证汇编代码。该发布只做了高层描述，几乎没有提供实现细节。 这有望让缺少源码的二进制程序也能接受形式化验证，对逆向工程、安全审计和底层代码可靠性分析具有潜在价值。它也表明逆向工程工具与软件模型检查之间可能出现更紧密的集成。 目前公开内容非常简略，没有说明 Ghidra 的反汇编结果如何转换为可供 CBMC 检查的模型、支持哪些指令集或性质，也没有给出已演示的验证结果。读者需要查看原始项目或相关讨论才能了解具体技术细节。

rss · Lobsters · 10月18日 16:58

**背景**: Ghidra 是美国国家安全局（NSA）开源的反汇编与逆向工程框架，可分析多种处理器指令集并支持脚本自动化。CBMC 是面向 C/C++ 的有界模型检查器，会在给定边界内探索程序行为，以检查断言、内存安全等性质。有界模型检查已用于 Rust 的 Kani 和 Java 的 JBMC 等工具，但要把这一方法用于原始汇编，需要把反汇编结果转换为可供模型检查器分析的语义表示。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/C_Bounded_Model_Checker">C Bounded Model Checker - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Ghidra">Ghidra - Wikipedia</a></li>
<li><a href="https://github.com/NationalSecurityAgency/ghidra">Ghidra Software Reverse Engineering Framework - GitHub</a></li>

</ul>
</details>

**标签**: `#formal verification`, `#CBMC`, `#Ghidra`, `#reverse engineering`, `#program analysis`

---