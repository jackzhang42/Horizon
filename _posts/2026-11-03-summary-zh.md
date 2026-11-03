---
layout: default
title: "Horizon Summary: 2026-11-03 (ZH)"
date: 2026-11-03
lang: zh
---

> 从 80 条内容中筛选出 21 条重要资讯。

---

1. [GPT-6 Astra 直接编辑 Qwen 权重引发争论](#item-1) ⭐️ 8.0/10
2. [Subvocal 发布射频感知智能眼镜，可将无声口型转为文字](#item-2) ⭐️ 8.0/10
3. [陶哲轩探讨 AI 时代的“无我数学”](#item-3) ⭐️ 8.0/10
4. [Ubuntu LTS 内核近三周仍未修复严重的 Linux 零日 RCE 漏洞](#item-4) ⭐️ 8.0/10
5. [飞机背景噪声可暴露视频的精确拍摄位置](#item-5) ⭐️ 8.0/10
6. [SGLang v0.5.23 发布：1007 个 PR，新增大量模型支持并大幅提升 MoE 推理性能](#item-6) ⭐️ 7.0/10
7. [DiscImageStudio 可将可见图像直接“烧”在 CD、DVD 和蓝光盘面上](#item-7) ⭐️ 7.0/10
8. [博主呼吁亲手备份网站，引发关于链接腐烂的讨论](#item-8) ⭐️ 7.0/10
9. [Show HN：华沙市中心被做成可交互的体素 3D 地图](#item-9) ⭐️ 7.0/10
10. [OpenAI 详解如何为庞大且快速增长的 monorepo 扩展 Git](#item-10) ⭐️ 7.0/10
11. [Polyend 开源 Tracker 硬件固件，并为刷坏的设备提供付费维修](#item-11) ⭐️ 7.0/10
12. [美国人口普查局 AI 采用数据现按“超级智能”行政令发布](#item-12) ⭐️ 7.0/10
13. [Legora CTO 谈无追踪评估、百万单元格表格审查与计费小时的松动](#item-13) ⭐️ 7.0/10
14. [只为改个时间：作者越狱雷诺车载导航系统](#item-14) ⭐️ 7.0/10
15. [USENIX 文章解析 GEFS 背后的 Bε 树技术](#item-15) ⭐️ 7.0/10
16. [PostHog 宣布将其数据仓库从 DuckDB 迁移出去](#item-16) ⭐️ 7.0/10
17. [WiKey 研究表明 WiFi 信号可识别击键，引发侧信道隐私担忧](#item-17) ⭐️ 7.0/10
18. [PlanetScale 详解如何设计低干扰的数据库计划内切换](#item-18) ⭐️ 7.0/10
19. [OpenAI 下调融资目标，投资者对 AI 的热情降温](#item-19) ⭐️ 7.0/10
20. [英国高等法院判决书中出现不存在的判例引注](#item-20) ⭐️ 7.0/10
21. [Apple Intelligence 12 月登陆中国，阿里 Qwen 取代 ChatGPT](#item-21) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [GPT-6 Astra 直接编辑 Qwen 权重引发争论](https://rikiyat.github.io/blog/weight-space-programming/) ⭐️ 8.0/10

一篇博客文章及随后的讨论描述了 MIT CSAIL 研究人员如何用 GPT-6 Astra 进行“权重空间编程”：在不训练、不做梯度下降的情况下读取并改写 Qwen3.5-0.8B 的内部权重。在一项报道的实验中，Astra 仅编辑了约 0.016% 的权重，就把该模型在 MATH-500 上的准确率从 7.9% 提升到 48.1%。 如果结果可复现，直接编辑权重可能为 AI 系统提供检查、调试和修复模型的新途径，并可能改变可解释性、安全审计和能力调优的做法。它也加剧了关于递归自我改进的猜测，但目前还不能算已经验证的范式转变。 据报道，Astra 触及了 131,072 个权重条目，约占该模型名义上 8 亿参数的 0.016%；它用 Python 计算替换值，然后提交编辑后的张量进行测试。该演示针对的是小型 Qwen 模型，并修复了特定层中的重复循环；据称它还修复了一个驾驶策略，但这些说法基于较窄的基准测试，且正受到质疑。

hackernews · Lobsters · 11月2日 18:21 · [社区讨论](https://news.ycombinator.com/item?id=50341174)

**背景**: 权重空间编程是指用一个通用语言模型读取另一个神经网络的原始数值权重，推断这些权重如何产生行为，并直接编辑张量，而不经过通常的微调或梯度下降。传统上，模型行为通过训练、微调或提示词来改变，因为权重是高维且难以解释的。Qwen 是阿里云推出的开放权重语言模型系列，因此很适合作为此类实验的对象。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://elsolitario.org/en/2026/11/02/mit-csail-astra-edits-0-016-of-qwen3-weights/">Weight-Space Programming: How Astra Edits Weights</a></li>
<li><a href="https://kingy.ai/blog/weight-space-programming-ai-agent-model-weights/">Weight-Space Programming: GPT-6 Astra Edits Qwen - kingy.ai</a></li>
<li><a href="https://en.wikipedia.org/wiki/Qwen">Qwen - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的评论者分歧明显：一些人称这一结果“疯狂”，并对大语言模型可能天生理解另一个网络权重的想法感到震惊；另一些人则呼吁先读论文，认为博客夸大了新颖性。多位评论者指出，权重空间学习和权重编辑已是既有研究领域，还有人猜测 Astra 可能接受过神经权重数据的训练，作为迈向递归自我改进的一步。

**标签**: `#LLM weight editing`, `#model interpretability`, `#Qwen`, `#weight-space learning`, `#AI research`

---

<a id="item-2"></a>
## [Subvocal 发布射频感知智能眼镜，可将无声口型转为文字](https://news.ycombinator.com/item?id=50340088) ⭐️ 8.0/10

YC F26 创业公司 The Subvocal Company 由佐治亚理工学院的 Aarush 和 Arnav 创立，他们展示了这款智能眼镜：利用射频传感将无声口型（包括完全闭唇的“内部言语”）解码为文字，速度接近正常语速。团队今年 2 月在斯坦福 TreeHacks 黑客松上用贴在脸上的肌电（EMG）电极做出最初原型，后因出汗、电干扰和电极位置不稳定等问题改用射频方案，如今把天线嵌入眼镜镜架之中。 无声语音接口有望让用户在图书馆、开放式办公室和公共场所实现免手输入——这些场景下 Wispr Flow 之类的听写工具根本无法使用；对手部劳损或腕管综合征而无法打字的用户来说，这也可能是一条出路。该 Show HN 帖子获得 704 分和 342 条评论，多位评论者表示这正是他们寻找多年的产品。 眼镜发射类似蓝牙的无线电波穿过面部，在无声口型动作中由舌头、嘴唇和软腭调制，随后用基础模型在这些扰动信号上训练以输出文字。创始人指出，最难的工程问题包括构建极低噪声的射频传感栈、让天线场与发音器官最大程度重叠，以及实现跨用户泛化——因为每个人的面部解剖结构和由此产生的射频信号模式差异极大。

hackernews · aarushyadav · 11月2日 17:16

**背景**: 无声语音接口是一个研究已久的领域：它不依赖声音，而是从肌肉活动、舌头与嘴唇运动或脑活动等非听觉信号推断说话意图。创始人提到的 MIT 媒体实验室 AlterEgo 项目，就是用下颌和面部的表面肌电电极识别无声说出的词；NASA 艾姆斯实验室做过早期默读（subvocalization）研究，脑机接口研究者近来也从运动皮层信号中解码内部言语。Subvocal 的创新在于用穿透面部的射频传感取代电极，并封装成可穿戴的眼镜形态。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Subvocal_recognition">Subvocal recognition - Wikipedia</a></li>
<li><a href="https://www.nature.com/articles/s44460-025-00010-2">Sensing technologies for silent speech interfaces - Nature</a></li>
<li><a href="https://www.nih.gov/news-events/nih-research-matters/decoding-inner-speech-brain-signals">Decoding inner speech from brain signals | National ...</a></li>

</ul>
</details>

**社区讨论**: 评论者总体热情但关注实际问题：一位已预订、鼻梁较高的用户恳请团队保留可调节的金属鼻托；另一位双手严重劳损、即将接受双侧腕管手术的用户称自己正是目标人群，并询问是否发货到欧洲；还有人询问是否支持阿拉伯语、信号处理是在眼镜端还是 App 中完成，以及能否推出可夹在现有近视眼镜上的版本。此外，多位评论者建议团队把帖子中的技术说明放到官网上。

**标签**: `#accessibility`, `#wearables`, `#speech-recognition`, `#HCI`, `#hardware`

---

<a id="item-3"></a>
## [陶哲轩探讨 AI 时代的“无我数学”](https://terrytao.wordpress.com/2026/11/02/egoless-mathematics-in-the-ai-era/) ⭐️ 8.0/10

陶哲轩发表了题为《AI 时代的无我数学》的博客文章，探讨人工智能可能如何重塑数学实践与价值观，并引发 Hacker News 上的大量讨论。 由于陶哲轩是知名数学家，他的反思在关于数学真理是否独立于人类数学家、以及 AI 可能如何改变这一职业及其使命感的讨论中具有分量。 这是一篇哲学性随笔和评论，而非技术成果；Hacker News 讨论获得 164 分和 121 条评论，显示人们对其中文化和职业影响有浓厚兴趣。

hackernews · smilelamp · 11月2日 18:54 · [社区讨论](https://news.ycombinator.com/item?id=50341736)

**背景**: 陶哲轩是澳裔美国数学家、加州大学洛杉矶分校教授，因其在数学多个领域的重要工作以及广受阅读的数学实践评论而知名。“无我数学”并非标准技术术语；在此语境中，它指为真理或集体知识而从事数学，而非为个人功劳或自我。该文加入了关于 AI 可能如何改变数学家的日常工作及其价值评估方式的更广泛讨论。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Terence_Tao">Terence Tao - Wikipedia</a></li>
<li><a href="https://news.ycombinator.com/item?id=50341736">Egoless Mathematics in the AI Era | Hacker News</a></li>

</ul>
</details>

**社区讨论**: 评论者意见不一：一些人赞赏陶哲轩坦诚面对传统数学家身份的失落并重新界定价值所在，另一些人则担心文章暗示人本身不重要、只有数学真理重要。还有人关注这一职业将如何演变，其中一位评论者用“喜欢做、擅长做、有人付费让你做”的维恩图来追问数学家还剩下什么。

**标签**: `#AI`, `#mathematics`, `#philosophy`, `#future of work`, `#Terry Tao`

---

<a id="item-4"></a>
## [Ubuntu LTS 内核近三周仍未修复严重的 Linux 零日 RCE 漏洞](https://freenode.net/article/ubuntu-lts-kernels-still-unfixed-for-critical-cve-2026-98432) ⭐️ 8.0/10

据一篇在 Hacker News 上引发大量关注的报道，Ubuntu 的 LTS 内核在近三周时间里仍未修复一个被编号为 CVE-2026-98432 的严重 Linux 内核零日远程代码执行漏洞。相关讨论（超过 520 分、约 150 条评论）主要聚焦于 Canonical 响应迟缓，而非漏洞本身的新技术细节。 Ubuntu LTS 是服务器和云环境中部署最广泛的操作系统之一，因此一个未修复的内核级远程代码执行漏洞会让庞大的用户群体处于风险之中，除非管理员自行采取缓解措施。这一事件还引发了更广泛的质疑：资源充足的企业厂商在核心安全维护上是否跟得上由志愿者运营的发行版。 有评论者指出，在 iptables 的 raw 表 PREROUTING 链中使用 u32 匹配（或等效的 nftables 规则）可以在流量到达内核漏洞触发点之前将其丢弃，但 Ubuntu 并未发布这类缓解指引；相比之下，Red Hat 发布了公告，不过其声称该缓解措施只能降低而不能完全阻止暴露风险。Ubuntu 确实提供 Livepatch，可在系统运行中打内核补丁而无需重启，但该机制的前提是补丁已经存在。

hackernews · majorchord · 11月2日 18:39 · [社区讨论](https://news.ycombinator.com/item?id=50341462)

**背景**: Ubuntu LTS 版本会获得长达数年的安全维护，内核修复通常以更新后的内核软件包形式发布，需要重启才能生效，或者通过 Canonical 的 Livepatch 服务在内存中为运行中的内核打补丁。“零日”指的是在厂商补丁可用之前漏洞就已被公开（或已被利用）。内核远程代码执行漏洞尤其严重，因为一旦利用成功，攻击者就能在最高权限层级执行代码，绕过所有应用层防护。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://ubuntu.com/kernel/lifecycle">Ubuntu kernel lifecycle and enablement stack | Ubuntu</a></li>
<li><a href="https://ubuntu.com/security/livepatch">Livepatch | Security | Ubuntu</a></li>
<li><a href="https://en.wikipedia.org/wiki/Linux_kernel_version_history">Linux kernel version history - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 讨论情绪对 Canonical 明显持批评态度：一位评论者表示，仅这一漏洞未能修复就足以让他把 Ubuntu 排除在可选发行版之外，并指出志愿者运营的发行版都能完成此类修复，而这家公司有充足的时间却未做到。其他人则要求官方给出延迟原因而非猜测，并批评 Ubuntu 缺乏像 Red Hat 那样的缓解说明；还有评论者把担忧扩展到运行 Linux 内核的消费级路由器和无线接入点，认为它们似乎从未获得过安全更新。

**标签**: `#linux`, `#ubuntu`, `#security`, `#kernel`, `#vulnerability`

---

<a id="item-5"></a>
## [飞机背景噪声可暴露视频的精确拍摄位置](https://simonwillison.net/2026/Nov/3/a-sound-that-leaks-your-exact-location/) ⭐️ 8.0/10

OSINT 研究者 Colsto 发布了一段 YouTube 演示，展示如何从视频音轨中提取几乎听不见的飞机噪声，将其转化为多普勒曲线，再与 ADS-B 航班数据进行比对，从而精确定位视频的拍摄地点。该方法结合每架飞机的速度、距离以及前后航班之间的时间间隔，把录音位置缩小到一个精确的点。 这是一次震撼性的隐私警示：任何发布带环境音视频的人，都可能在不知情中公开了一个地理定位信标，因为航班追踪数据是公开且免费的。它把 OSINT 地理定位手段从视觉地标大大拓展到音频层面，对记者、活动人士以及普通内容创作者都构成新的风险。 该方法依赖于从音轨中提取极其微弱的低频飞机噪声，估算飞机飞过头顶时的多普勒频移，再将这些曲线与历史 ADS-B 记录相关联——这些记录约每秒广播一次飞机身份、GPS 位置、高度、速度和航向。由于它依靠多次飞越的几何关系而非单一声音，可识别的飞机数量越多、录音时间越长，定位精度就越高。

rss · Simon Willison · 11月3日 05:32

**背景**: ADS-B（自动相关监视—广播）是一种航空监视技术，飞机通过卫星导航确定自身位置并定期广播，正因如此，众包航班追踪平台才能近乎实时地显示成千上万架飞机。多普勒效应是指声源靠近或远离听者时感知频率发生偏移的现象，当飞机飞过头顶时会产生典型的先升后降曲线。OSINT（开源情报）指对公开可用信息的分析，此前已有 DOPPLERGEIST 等工具探索过通过飞机多普勒分析进行声学定位。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Automatic_Dependent_Surveillance–Broadcast">Automatic Dependent Surveillance–Broadcast - Wikipedia</a></li>
<li><a href="https://nearestplane.com/learn/how-flight-tracking-works/">How Does Flight Tracking Work? ADS-B Explained | NearestPlane</a></li>
<li><a href="https://github.com/1337isnot1337/DOPPLERGEIST">GitHub - 1337isnot1337/DOPPLERGEIST: A tool to geolocate audio ...</a></li>

</ul>
</details>

**标签**: `#privacy`, `#OSINT`, `#geolocation`, `#audio-analysis`, `#ADS-B`

---

<a id="item-6"></a>
## [SGLang v0.5.23 发布：1007 个 PR，新增大量模型支持并大幅提升 MoE 推理性能](https://github.com/sgl-project/sglang/releases/tag/v0.5.23) ⭐️ 7.0/10

SGLang 发布 v0.5.23，这是一个由 257 位贡献者提交的 1007 个 PR 构成的增量版本，新增了对 Muse Spark Open、Beam-1.0、MiniMax-M3.1-Flash、MiniCPM-V 4.7、FLUX.3 Image Klein、MOSS-Image 等大语言模型、视觉语言模型和扩散模型的支持。该版本还引入了可选的低延迟模式（基于 NVIDIA megakernel 与 AMD monokernel 插件）、能让超出显存容量的 MoE 模型运行的 Paged Experts 功能，以及可在 FP8 和 NVFP4 量化 MoE 模型上服务 LoRA 适配器的新 LoRA 引擎。 SGLang 是用于 LLM 与多模态推理的最主流开源服务框架之一，因此每次发布都会直接影响开发者将模型部署到生产环境的方式，以及新开源模型能以多快速度在大规模场景中可用。本次的性能改进——DeepSeek-V4.1 在 GB300 上最高 1.5 倍的 prefill 吞吐、H200 上 MoE 模型首 token 延迟降低 30%–58%、超出显存的模型比 CPU offload 快最高 30 倍——正针对实际推理负载中最主要的成本与延迟瓶颈。 亮点细节包括：DeepSeek-V4.1 在 GB300 上处理 32K–64K 提示时首 token 延迟降低约 28%；低延迟 megakernel/monokernel 模式使单用户解码在 GB300 上最高快 44%、在 MI350X 上最高快 75%；使用解码上下文并行的 DeepSeek 式 MLA 模型可将其前缀缓存保存在 HiCache 基于文件的 L3 存储中。安装时需要加上 --prerelease=allow 参数，官方还提供了面向 NVIDIA CUDA 13、AMD MI35x/MI30x、Intel GPU 与 CPU 以及通过独立 SGLang-TorchTPU 插件支持的 Google TPU7x 的镜像。

github · Fridge003 · 11月2日 22:14

**背景**: SGLang（Structured Generation Language）是一个开源的高性能推理与服务框架，支持大语言模型、视觉语言模型和扩散模型，并针对智能体工作负载、大规模服务以及强化学习 rollout 进行了优化。它与 vLLM、TensorRT-LLM 处于同一赛道，因为常常较早上线针对新模型架构的优化，其版本演进备受 LLM 基础设施团队关注。本版本涉及的关键概念包括：混合专家（MoE）模型——每个 token 只激活部分参数；以及投机解码——用小规模草稿模型提出候选 token 再由大模型验证，两者都旨在不牺牲输出质量的前提下提升吞吐。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/sgl-project/sglang">sgl-project/ sglang : SGLang is a high-performance serving framework ...</a></li>
<li><a href="https://docs.sglang.io/">Welcome to SGLang - SGLang Documentation</a></li>
<li><a href="https://grokipedia.com/page/SGLang">SGLang</a></li>

</ul>
</details>

**标签**: `#SGLang`, `#LLM inference`, `#model serving`, `#release notes`, `#diffusion models`

---

<a id="item-7"></a>
## [DiscImageStudio 可将可见图像直接“烧”在 CD、DVD 和蓝光盘面上](https://github.com/JiaFeiMiao-K-Cat/DiscImageStudio) ⭐️ 7.0/10

开发者 JiaFeiMiao-K-Cat 发布了开源工具 DiscImageStudio，这是一个基于 Windows .NET 9 的程序，可把普通图片转换成光盘数据，使烧录后的 CD、DVD 或蓝光光盘的记录面上呈现出可见图像。项目提供 ISO/RAW 导出以及实验性的流式刻录模式，并内置辅助标定流程，作者称其可将可确定的盘面物理数据精度从约 10^-6 提升到 10^-14。 这款工具把光驱工程中一个冷门的角落——精确控制写入激光在染料层或相变层上留下暗点的位置与方式——变成了普通用户可以动手尝试的东西，并公开讲解了 DVD 的信号调制、蓝光的纠错扇区布局以及亚微米级的螺旋轨道跟踪。这既让它成为一件延续 LightScribe 精神的创意作品，也使其成为理解光盘究竟如何编码数据的学习资源。 使用流程是一个基于工程的图形界面：先选择 CD、DVD 或蓝光并指定输出位置，在 Design 页面导入图片并支持图层排版，然后在 Tone 面板中调节抖动、伽马、亮度和灰度级，最后导出 ISO/RAW 或尝试流式刻录。由于结果本质上依赖具体光驱与盘片，才有了辅助标定这一步——也正因如此，同一张图在不同刻录机上的可复现性是一个需要注意的限制。

hackernews · bpierre · 11月3日 01:33 · [社区讨论](https://news.ycombinator.com/item?id=50346849)

**背景**: 可记录光盘把数据存成一条由微小标记组成的螺旋轨道，读取激光依据这些标记反射率的差异将其解读为比特；在 CD-R/DVD-R 上写入激光会烧灼染料层，而可重写光盘和蓝光则使用相变合金。由于这些标记在合适的光照下肉眼可见，只要刻意选择哪些区域被写入，为数据而刻出的坑点图案本身就能充当一幅图像。DiscImageStudio 正是把这一反向过程自动化：计算出刻录后标记图案恰好构成目标画作的那份光盘镜像。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/JiaFeiMiao-K-Cat/DiscImageStudio">GitHub - JiaFeiMiao-K-Cat/DiscImageStudio</a></li>
<li><a href="https://github.com/JiaFeiMiao-K-Cat/DiscImageStudio/blob/main/README.en.md">DiscImageStudio/README.en.md at main...</a></li>
<li><a href="https://elsolitario.org/en/2026/11/02/discimagestudio-visible-art-on-cd-dvd-and-blu-ray/">Visible Disc Image: What Is DiscImageStudio - elsolitario.org</a></li>

</ul>
</details>

**社区讨论**: 评论区充满热情与怀旧气息：有人提到自己为 BSidesSF CTF 出过一道题，把一段原始 CDDA 音频烧录到 CD-RW 上便会显现出旗帜图案，而选手被期望用软件模拟烧录结果，而不是去猜具体的刻录机型号。其他人则回忆起 LightScribe 光雕刻录机和 Neato 的可打印光盘贴纸，并指出早前 arduinocelentano 的 cdimage 项目是类似的先例。

**标签**: `#optical media`, `#CD/DVD burning`, `#disc art`, `#hardware hacking`, `#reverse engineering`

---

<a id="item-8"></a>
## [博主呼吁亲手备份网站，引发关于链接腐烂的讨论](https://blog.mistys-internet.website/post/2026/10/29/if-you-love-a-website-back-it-up/) ⭐️ 7.0/10

一篇题为《如果你爱一个网站，就把它备份下来》的短文主张，个人应当亲自归档自己珍视的网站，而不是指望它们永远留在线上；该帖在 Hacker News 上获得 555 次点赞和 124 条评论。讨论很快从最初的呼吁扩展到链接腐烂、论坛在从未被爬取的情况下消失，以及用 ArchiveWeb、SingleFile 等工具进行本地抓取保存等话题。 这场讨论揭示了开放网络的一个结构性弱点：没有被任何人主动保存的内容往往会消失，而 Wayback Machine 这类集中式存档也并非无所不包。对于依赖旧文档、论坛和博客的研究者、开发者以及普通读者来说，这一点尤为重要——这些东西可能在人们察觉之前就已不复存在。 评论者特别推荐了 ArchiveWeb，因为它能在抓取时自行挑选要保存的页面和页面元素；也推荐了 SingleFile，它能快速把一个页面连同媒体资源打包成单个自包含的 HTML 文件。讨论还指出一个硬性限制：AI 工具可以从残存的碎片重建网站，但无法找回真正已经消失的数据。

hackernews · ingve · 11月2日 13:25 · [社区讨论](https://news.ycombinator.com/item?id=50336518)

**背景**: 链接腐烂（link rot）指的是超链接随着目标页面被迁移、改写或下线而逐渐失效，产生人们熟悉的“404 Not Found”错误。网页归档工具通过保存页面快照来应对这一问题：既可以像互联网档案馆的 Wayback Machine 那样集中保存，也可以用 WARC 或单文件 HTML 等格式保存在用户自己的机器上。数字保存（digital preservation）作为一个研究领域，关注的是如何在存储介质失效和技术变迁的情况下，让原生数字内容持续可访问，而个人归档正是这一实践的大众版本。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Link_rot">Link rot - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Digital_preservation">Digital preservation - Wikipedia</a></li>
<li><a href="https://websitedownloader.org/blog/website-archiver-guide-2026/">Website Archiver : How to Archive Any Website in 2026</a></li>

</ul>
</details>

**社区讨论**: 整体情绪是支持中带着惋惜：一位评论者说自己眼看着书签逐渐腐烂，几年前的重要资源如今只剩 404，而且常常在 Archive.org 上也找不到副本。有人警告说，五年之内集中化的云端大模型可能取代开放互联网成为信息源，并拥有改写过去的能力，因此呼吁大家购买纸质书、归档重要网站；还有用户讲述自己手工扫描的照片随着一个维持了二十年的 Angelfire 网站悄然消失而丢失，网页存档里只剩下“骨架”。

**标签**: `#digital-preservation`, `#web-archiving`, `#link-rot`, `#open-web`, `#tools`

---

<a id="item-9"></a>
## [Show HN：华沙市中心被做成可交互的体素 3D 地图](https://p.migdal.pl/warsaw-vibe-voxel/) ⭐️ 7.0/10

开发者 Piotr Migdał（stared）发布了“Warsaw in voxels”，这是一个在浏览器中运行的华沙市中心可交互 3D 体素地图，开源实现，数据融合了 OpenStreetMap、波兰 GUGiK/Geoportal 的 LiDAR 与航拍影像，以及华沙官方的城市树木数据库。该演示允许用户切换日期、时间与天气，并可点击行人直接操控其行走（灵感来自《Minecraft》和《地下城守护者》），完整源码已在 GitHub 上公开。 这个项目很好地展示了开放地理空间数据结合 WebGL 能达到的效果：一名开发者无需专有数据或商业引擎，就能把真实城市在三维空间中重建出来，还带有季节性植被和动态光照。它也为任何基于公共数据集构建城市级可视化、模拟或游戏的人提供了一个可复用的参考实现。 建筑高度和树木位置来自 LiDAR 点云，颜色取自航拍影像，而按树种记录的官方树木数据则用于驱动季节性叶色变化；作者提醒首次加载可能较慢，并且桌面端体验最佳。评论者报告了严重的性能问题：尽管性能分析器显示更新逻辑很快，但在 Linux 上的 Firefox 中帧率低于 1 FPS，在 Windows 11 上用 Chrome 搭配移动版 RTX 3080 Ti 时单帧耗时约 120 毫秒。

hackernews · stared · 11月2日 16:25 · [社区讨论](https://news.ycombinator.com/item?id=50339221)

**背景**: 体素（voxel）是像素在三维空间中的对应物：它是规则三维网格上的一个小立方体，携带颜色或材质信息，因而非常便于拼出《Minecraft》那种方块风格的场景。LiDAR（激光探测与测距）通过发射激光脉冲并测量反射所需时间来计算距离，生成稠密点云，从中可以提取精确的建筑高度和地形。由波兰测绘与制图总局（GUGiK）运营的 Geoportal.gov.pl 是这类空间数据的国家级入口，其中相当一部分以开放数据形式发布，任何人都可以下载和再利用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.megavoxels.com/learn/what-is-a-voxel/">What is a voxel ? - Mega Voxels</a></li>
<li><a href="https://en.wikipedia.org/wiki/Lidar">Lidar - Wikipedia</a></li>
<li><a href="https://www.gov.pl/web/gugik-en/geoportal">Geoportal - Head Office of Geodesy and Cartography ( GUGiK )</a></li>

</ul>
</details>

**社区讨论**: 评论者称赞项目“非常精巧”，但讨论主要集中在其性能上：有人报告在 Linux 上的 Firefox 中帧率不足 1 FPS，也有人表示在配备 RTX 3080 Ti 的笔记本上几乎无法使用，并指出性能分析器显示更新逻辑本身其实很快。作者则提到了“Streets of Prague”等基于真实数据的同类城市项目，另一些讨论则转向了旅行见闻，比如华沙的“腊肠犬”建筑和华沙起义博物馆。

**标签**: `#3D visualization`, `#open data`, `#OpenStreetMap`, `#web graphics`, `#Show HN`

---

<a id="item-10"></a>
## [OpenAI 详解如何为庞大且快速增长的 monorepo 扩展 Git](https://openai.com/index/scaling-git-at-openai/) ⭐️ 7.0/10

OpenAI 发布了一篇工程博客《Scaling Git at OpenAI》，介绍其如何改造 Git 基础设施，以支撑规模庞大且快速增长的 monorepo，其中还提到了一套名为 Pando 的内部系统。据一位 Hacker News 评论者统计，这是近期同类文章中第五篇重要文章，此前 Cursor、GitHub（两篇）和 Anthropic 都发过类似内容。 AI 实验室的代码库规模正在超出传统版本控制系统的设计承载能力，因此这些实验室摸索出的技术方案以及自建或改造的工具，很可能会影响未来大型工程组织管理版本控制的方式。这篇文章也为 AI 公司日渐流行的基础设施写作增添了又一个以具体数据为支撑的案例研究。 这篇文章的突出之处在于几乎没有宣传炒作，而是用数字、图表和可视化来支撑论述。不过有评论者指出，文章并未给出硬性的运维基准数据，例如系统每秒能处理多少次 push，或支持多少个并发推送者。

hackernews · OpenAI Blog · 11月2日 23:47 · [社区讨论](https://news.ycombinator.com/item?id=50345924)

**背景**: monorepo 是一种把多个项目放在同一个代码仓库里的版本控制组织方式，它简化了依赖共享和跨项目修改，但会让仓库变得非常庞大。随着仓库规模增长，clone、checkout、fetch、status 等标准 Git 操作会明显变慢，因此出现了 Scalar（用于优化大型仓库中 Git 性能的工具）和 Git LFS 等方案，通过减少网络传输的数据量来维持可用性能。OpenAI 的这篇文章讲的正是当这些常规手段也不够用时所需要做的内部工程改造。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://monorepo.tools/">Everything you need to know about monorepos , and the tools to build...</a></li>
<li><a href="https://git-scm.com/docs/scalar">Git - scalar Documentation</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论（232 分、145 条评论）整体对文章质量给予好评，有评论者称赞它细节丰富、没有炒作，是一群工程师用自己的口吻配着数字和图表讲述的深度内容。但也有人持怀疑态度：多位评论者追问代码量指数级增长究竟在做什么，认为原始提交数量并不能说明产品价值，更多只是反映了更细粒度的变更集或把提交信息当文档的习惯，并指出文章缺少基准测试数据。

**标签**: `#git`, `#version-control`, `#monorepo`, `#engineering-infrastructure`, `#scaling`

---

<a id="item-11"></a>
## [Polyend 开源 Tracker 硬件固件，并为刷坏的设备提供付费维修](https://polyend.com/whats-up/tracker-the-biggest-update-yet/) ⭐️ 7.0/10

Polyend 在号称“史上最大更新”的发布中公开了 Tracker 硬件固件的源代码，使设备拥有者和外部开发者都能自行编译并刷入自定义固件。与此同时，Polyend 明确表示自定义固件不在标准保修范围内，但公司仍会为出现问题的设备提供付费维修服务。 在商业音乐硬件上开源固件仍属罕见，这为 Tracker 带来了一个模改社区，使其功能与生命周期可以远超官方更新所能提供的范围。此举也会给其他硬件厂商带来压力，尤其是 M-VAVE FM-1 这类可改造设备的走红表明，开放本身就能带动销量。 Polyend 明确指出自定义固件存在变砖风险且会使标准保修失效，但承诺提供保外维修，避免用户面对彻底报废的设备。与大多数嵌入式产品一样，固件中可能仍有专有组件或专有工具链，从而限制外部开发者实际能够重新构建的范围。

hackernews · austinallegro · 11月2日 17:20 · [社区讨论](https://news.ycombinator.com/item?id=50340159)

**背景**: 音乐 tracker 是一种音序器界面，音符以纵向时间轴的形式排列在若干编号通道中，这一风格可追溯到 Amiga 时代的软件 tracker；Polyend Tracker 作为首款专用硬件 tracker，将这种工作流带入了独立硬件设备。固件是嵌入在设备中、直接控制硬件的底层软件，因此自定义固件指的是第三方替换版本，而非官方更新。过去厂商通常以保修、技术支持负担和知识产权为由封闭这类代码。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://polyend.com/tracker/">Tracker • Polyend</a></li>
<li><a href="https://en.wikipedia.org/wiki/Music_tracker">Music tracker - Wikipedia</a></li>
<li><a href="https://grokipedia.com/page/Custom_firmware">Custom firmware — Grokipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者将此次开源与 M-VAVE FM-1 的爆红联系起来，认为后者的人气很大程度上来自其开放固件和逆向工程社区。不少人对 Polyend 坦承变砖风险并仍提供付费维修表示赞赏；一位用户分享了自己借助 AI 提示为 Modal Cobalt8 添加 Curtis 风格、303 和 Steiner-Parker 滤波器以及额外振荡器的经历，也有人讨论在存在专有组件、且音乐人对 AI 态度分歧的情况下，还会有多少厂商跟进。

**标签**: `#open-source`, `#firmware`, `#embedded-systems`, `#music-hardware`, `#reverse-engineering`

---

<a id="item-12"></a>
## [美国人口普查局 AI 采用数据现按“超级智能”行政令发布](https://simonwillison.net/2026/Nov/2/census-bureau-super-intelligence/) ⭐️ 7.0/10

Simon Willison 利用美国人口普查局 2026 年 10 月 22 日发布的《商业趋势与展望调查》（BTOS）数据，重新绘制了 Apollo Global Management 的 AI 采用率图表，并在此过程中发现该局如今的数据是“依据第 14434 号行政令”发布的——即 2026 年 9 月 29 日签署、被称为“超级智能”行政令的那份文件。新图表显示，在“任何业务环节使用 AI”的口径下，250 人以上企业的采用率为 40.7%，100–249 人企业为 33.5%，而 50 人以下企业大致在 21%–24%之间。 BTOS 是美国企业 AI 采用情况最受关注的公开指标之一，因此强制性的术语变更会直接影响研究人员、记者和投资者引用官方统计数据时的表述方式。这件事也说明，一份覆盖面很广的行政令可以渗透到看似不起眼的统计产品中，并使这一被广泛引用的数据集在年度对比时变得更加复杂。 除术语变化外，调查本身也在 2025 年 11 月做了调整：问题从“在生产商品或服务中使用 AI”改为“在任何业务环节中使用 AI”，因此两组数据序列明确不可直接比较，Willison 的图表在两者之间留出一段未做衔接的空白，涵盖 2025 年政府停摆以及等待新问法积累六次观测的时期。BTOS 每两周对 120 万家企业中的 20 万家进行轮换抽样，单家企业每十二周才被调查一次，结果在隔周的周四上午 10 点发布。

rss · Simon Willison · 11月2日 13:31

**背景**: 《商业趋势与展望调查》（BTOS）是人口普查局的一项高频调查，自 2024 年起加入 AI 采用情况附卷，因而成为追踪美国企业实际使用 AI 情况的重要数据来源。2026 年 9 月 29 日签署的第 14434 号行政令要求行政机构在官方函件、网站、报告及其他非 statutory 文件中，以“超级智能”（Super Intelligence，简称 SI）取代“人工智能”（AI），同时将该新术语定义为与现有法律定义中 AI 所指的技术相同。Simon Willison 是一位高产的开发者与写作者，经常拿公开数据集作为测试 AI 编程与数据分析工具的基准。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.whitehouse.gov/presidential-actions/2026/09/inaugurating-the-era-of-super-intelligence/">Inaugurating The Era Of Super Intelligence – The White House</a></li>
<li><a href="https://public-inspection.federalregister.gov/2026-20321.pdf">EXECUTIVE ORDER 14434 - - - - - - - Constitution and the laws ...</a></li>
<li><a href="https://www.census.gov/hfp/btos/">Business Trends and Outlook Survey - Census.gov</a></li>

</ul>
</details>

**标签**: `#AI policy`, `#government data`, `#AI adoption`, `#data analysis`, `#executive order`

---

<a id="item-13"></a>
## [Legora CTO 谈无追踪评估、百万单元格表格审查与计费小时的松动](https://latent.space/p/building-ai-for-lawyers-jacob-lauritzen-cto-of-legora/) ⭐️ 7.0/10

在 Latent Space 的一期访谈中，Legora 首席技术官 Jacob Lauritzen 介绍了这家法律 AI 初创公司如何为律师打造 AI 产品，内容涵盖不依赖详细执行追踪（traces）的评估方法、规模可达数百万单元格的表格化审查，以及律所按小时计费商业模式所承受的日益增大的压力。这场讨论更偏向从业者层面的深度对谈，而非产品发布公告。 法律工作是应用型大语言模型价值最高的领域之一，而 Legora 的经验表明，垂直领域的 AI 必须采用与通用聊天机器人基准不同的方式进行验证。如果 AI 能够可靠地完成大规模文档审查，它将直接侵蚀按小时计费的商业逻辑，而这一模式正是大多数律所收入的根基。 访谈强调了“无追踪评估”（evals without traces）——即在无法记录模型完整推理路径的情况下进行评测的方法，这在对保密性敏感的法律工作流中十分常见。访谈还涉及达到数百万单元格规模的表格化审查：每份文档成为一行，每个问题成为一列；August 和 Vecflow 等其他法律 AI 工具也采用类似模式，并让每个答案都能回溯到原文以便核验。

rss · Latent Space · 11月2日 23:01

**背景**: Legora 是一家为律师构建 AI 助手的法律科技初创公司，与 Harvey、August 等工具同台竞争。“Evals”（评估）是团队用来衡量大语言模型系统输出是否正确的测试集，通常基于真实使用过程中的追踪数据（traces）构建，从而把失败案例转化为回归测试。“表格化审查”是一种法律工作流：将大量合同或文档抽取到电子表格式的网格中，让律师可以一次比较数百份文件中的条款与事实。按小时计费则是指传统的按投入时间向客户收费的做法，而 AI 带来的效率提升正在对这一模式构成压力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://hamel.dev/blog/posts/evals-faq/">AI Evals: Everything You Need to Know – Hamel’s Blog</a></li>
<li><a href="https://www.august.law/product/tabular-review">August Tabular Review</a></li>
<li><a href="https://www.vecflow.ai/news/introducing-tabular-review">Introducing Tabular Review : A New Era of Document Analysis</a></li>

</ul>
</details>

**标签**: `#AI applications`, `#legal tech`, `#evals`, `#LLM systems`, `#startups`

---

<a id="item-14"></a>
## [只为改个时间：作者越狱雷诺车载导航系统](https://blog.nns.ee/2026/11/02/renault-hack/) ⭐️ 7.0/10

一位开发者发布了一篇详细的实践记录，讲述自己如何越狱（jailbreak）雷诺汽车上的导航/信息娱乐主机，目的仅仅是为了能够修改系统时间。文章完整梳理了绕过该主机限制所需的嵌入式系统逆向工程过程，而不是接受出厂锁定、无法更改的时钟设置。 这是一个具体而真实的案例，说明个人研究者可以如何破解封闭的汽车主机，也印证了现代汽车中信息娱乐系统属于防护相对薄弱的攻击面这一担忧。对于那些被“只能去 4S 店设置”或网络锁定设置困扰的车主来说，它也说明这类限制往往只是技术性门槛，而非真正无法绕过。 作者的目标其实很小——只是设置时间——但要实现它却需要动用完整的嵌入式逆向工程手段：分析固件与板级元件，弄清主机是如何实施限制的。与大多数主机改装一样，该过程高度依赖具体车型与固件版本，并伴随把主机变砖、失去保修，或影响车辆所依赖功能等风险。

rss · Lobsters · 11月2日 16:30

**背景**: 车载主机（head unit）是位于中控台的计算机，为汽车的娱乐与信息功能提供用户界面，包括收音机、USB 媒体、蓝牙、GNSS 导航，乃至越来越多的车辆设置项。由于这类主机运行嵌入式操作系统，并配有锁定的引导程序与签名固件，想改动厂商未开放的任何内容，通常都需要对固件和硬件进行逆向工程。嵌入式逆向工程指的是通过分析固件、微控制器逻辑与板级元件来理解其功能或发现漏洞，安全研究者审计汽车信息娱乐系统时用的正是这套技能。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Automotive_head_unit">Automotive head unit - Wikipedia</a></li>
<li><a href="https://voidstarsec.com/blog/intro-to-embedded-part-1">Intro to Embedded Reverse Engineering: Tools and Series ...</a></li>
<li><a href="https://hackaday.com/2023/06/27/honda-headunit-reverse-engineering-and-the-dismal-state-of-infotainment-systems/">Honda Headunit Reverse Engineering , And The Dismal... | Hackaday</a></li>

</ul>
</details>

**标签**: `#reverse engineering`, `#embedded systems`, `#car infotainment`, `#jailbreaking`, `#security`

---

<a id="item-15"></a>
## [USENIX 文章解析 GEFS 背后的 Bε 树技术](https://www.usenix.org/publications/login/oct15/bender) ⭐️ 7.0/10

一篇由 Michael Bender 撰写、发表在 USENIX ;login: 上的文章介绍了 Bε 树与写优化数据结构，它被重新提出来作为刚发布的 Plan 9 文件系统 GEFS（“足够好的文件系统”）的理论基础。该提交本质上只是指向文章和此前讨论帖的链接，没有附加更多评论。 像 Bε 树这样的写优化结构可以让插入速度比经典 B 树快上几个数量级，同时保持相当的点查询性能，这对任何写入负载较重的存储系统都很重要。由于 GEFS 在 9p 接口之下构建了一片写时复制的 Bε 树森林，理解这一数据结构是评估该文件系统崩溃安全性与快照设计的关键。 Bε 树在每个内部节点中维护一个待写入更新缓冲区，因此写操作会被批量合并，并以大块顺序 I/O 写入磁盘，而不是分散的随机写；Bender 的工作显示其插入速度比 B 树快 10 到 100 倍，而点查询开销相近。代价是范围查询和扫描会变慢，而且该结构假设的代价模型是数据以块为单位在内存与磁盘之间传输。

rss · Lobsters · 11月2日 20:26

**背景**: B 树是磁盘上标准的索引结构，但每次更新都需要对叶节点进行一次缓慢的随机写。写优化数据结构则先将更新缓冲起来，再以大块顺序方式刷写，从而以部分读取代价换来大幅降低的写成本。Bε 树中的“ε”是一个可调参数，用来控制内部节点分配多少缓冲空间，使设计者可以调整读写放大之间的平衡。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://orib.dev/gefs.pdf">GEFS, A Good Enough File System</a></li>
<li><a href="https://www.cs.williams.edu/~jannen/teaching/s19/cs333/meetings/betrees-slides.pdf">betrees-slides</a></li>

</ul>
</details>

**标签**: `#B-epsilon trees`, `#write optimization`, `#file systems`, `#storage`, `#GEFS`

---

<a id="item-16"></a>
## [PostHog 宣布将其数据仓库从 DuckDB 迁移出去](https://posthog.com/blog/moving-off-duckdb) ⭐️ 7.0/10

PostHog 发布了一篇题为《Why we're moving our warehouse off DuckDB》的工程博客，宣布其数据仓库产品（即 PostHog 基于 DuckDB 引擎构建的分析能力）将迁移到其他后端。文章以解释这次生产环境迁移背后的原因为主线，并在 Lobsters 上引发了讨论。 DuckDB 已成为快速、嵌入式分析负载的默认选择之一，因此一家知名产品分析公司在仓库规模上公开“掉头”，对正在权衡 DuckDB 与服务器型数据仓库的分析与数据基础设施团队来说是很有价值的信号。它也勾勒出 DuckDB 的适用边界：单机、进程内分析是它的强项，而多租户、高并发的生产级数据仓库则另有要求。 这篇博文更像是一份实践经验报告而非基准测试论文，因此具体的失效模式、迁移目标以及性能数据都写在正文中，而本摘要所能获得的片段里并未包含。评估这一取舍的读者应注意，PostHog 的负载是多租户的产品分析仓库、并发用户众多，这与 DuckDB 最常被称道的“单个分析师查询本地文件”场景有显著差异。

rss · Lobsters · 11月3日 07:33

**背景**: DuckDB 是由 Hannes Mühleisen 和 Mark Raasveldt 创建的开源进程内列式分析数据库，于 2019 年首次发布；它像 SQLite 一样嵌入在应用进程中运行，但针对 OLAP 类扫描做了优化，并可直接查询 Parquet 和 CSV 文件。PostHog 是一个产品分析平台，把事件、会话回放、错误和日志统一摄取到一处供查询，同时还提供数据仓库产品，用于在查询产品数据的同时查询外部数据源。在仓库规模上“换掉”一个数据库引擎，通常意味着重新设计摄取、存储布局和查询执行，这也是这类迁移备受其他工程团队关注的原因。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://motherduck.com/learn/what-is-duckdb/">What is DuckDB ? | MotherDuck</a></li>
<li><a href="https://hightouch.com/blog/duckdb">What is DuckDB and why it's the new tool for a data analyst. | Hightouch</a></li>
<li><a href="https://posthog.com/">PostHog – Your product’s context layer</a></li>

</ul>
</details>

**标签**: `#DuckDB`, `#data warehouse`, `#analytics`, `#PostHog`, `#engineering`

---

<a id="item-17"></a>
## [WiKey 研究表明 WiFi 信号可识别击键，引发侧信道隐私担忧](https://ieeexplore.ieee.org/document/7875144) ⭐️ 7.0/10

IEEE 论文《Keystroke Recognition Using WiFi Signals》（WiKey，由 Kamran Ali 等人完成）首次证明，普通商用 WiFi 设备可以通过分析手部与手指动作引起的信道状态信息（CSI）变化，识别用户正在输入的内容。该系统使用搭载 Intel 5300 网卡的现成硬件，在没有任何摄像头、键盘记录器或物理接触设备的情况下，即可检测单次击键并还原出完整单词。 WiFi 已普遍存在于家庭、办公室和公共场所，因此如果仅凭 CSI 就能推断出输入内容，那么每一台无线路由器都可能成为泄露密码、消息等敏感输入的侧信道。该研究既是 WiFi 感知领域的基础性文献，也是无线安全领域的重要参考，并为此后针对 WiFi 感知系统的窃听与对抗攻击研究奠定了基础。 WiKey 依赖 OFDM 各子载波上细粒度的 CSI 幅度与相位测量，以捕捉击键动作引起的细微信道扰动；作者报告在受控环境下针对有限词表可达到约 93.5% 的整词识别准确率，但在打字风格、距离和坐姿多变的真实环境中，准确率会明显下降。该系统还需要针对每位用户和每种键盘位置进行带标签样本的训练阶段，并且在打字区域与收发设备之间保持良好视距时效果最佳。

rss · Lobsters · 11月2日 14:43

**背景**: 信道状态信息（CSI）是许多 WiFi 网卡（如 Intel 5300 和 Atheros 9390）可获取的物理层测量值，用于描述无线信道对各 OFDM 子载波在幅度和相位上的畸变。由于 CSI 比粗糙的 RSSI 信号强度值精细得多，研究者已将其用于人体活动识别、跌倒检测、步态识别和手势感知，甚至可穿墙、在黑暗中工作。WiKey 把这一研究方向从大幅度的身体动作，推进到了键盘上手指与手掌的毫米级微小动作。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://paper.bobylive.com/Hardware/Keystroke_Recognition_Using_WiFi_Signals.pdf">Keystroke Recognition Using WiFi Signals</a></li>
<li><a href="https://scispace.com/papers/keystroke-recognition-using-wifi-signals-3tjd1by223">(PDF) Keystroke Recognition Using WiFi Signals (2015) | Kamran Ali</a></li>
<li><a href="https://arxiv.org/pdf/2404.15587">Security Analysis of WiFi-based Sensing Systems: Threats from ...</a></li>

</ul>
</details>

**标签**: `#WiFi sensing`, `#keystroke recognition`, `#privacy`, `#side-channel attacks`, `#wireless security`

---

<a id="item-18"></a>
## [PlanetScale 详解如何设计低干扰的数据库计划内切换](https://planetscale.com/blog/designing-a-planned-switchover-for-minimum-disruption) ⭐️ 7.0/10

PlanetScale 发布了一篇工程博客文章，介绍如何设计计划内的数据库切换，以将日常维护和拓扑变更对应用造成的干扰降到最低。 计划内切换对高可用数据库运维至关重要，因为它让团队能够在不使服务离线的情况下执行维护、升级或故障转移演练。 该文章是一篇面向运行 MySQL 兼容系统的团队的技术深度文章；提供的摘录仅包含评论链接，因此无法在此核实文章中的具体机制和注意事项。

rss · Lobsters · 11月3日 08:20

**背景**: PlanetScale 是一个关系型数据库平台，提供 Vitess、Neki 和 PostgreSQL 集群，注重扩展性和可靠性。在数据库高可用领域，switchover（计划内切换）是由运维人员主动发起的主库到备库的切换，区别于通常由非计划故障触发的 failover（故障转移）。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://planetscale.com/docs">PlanetScale - PlanetScale</a></li>
<li><a href="https://learn.microsoft.com/en-us/exchange/high-availability/manage-ha/switchovers-and-failovers">Switchovers and failovers | Microsoft Learn</a></li>

</ul>
</details>

**标签**: `#databases`, `#high-availability`, `#PlanetScale`, `#MySQL`, `#zero-downtime`

---

<a id="item-19"></a>
## [OpenAI 下调融资目标，投资者对 AI 的热情降温](https://www.reddit.com/r/artificial/comments/1xm7eyb/openai_lowers_funding_goals_as_investors_cool_on/) ⭐️ 7.0/10

Reddit 的 r/artificial 板块一则链接帖报道称，OpenAI 已在投资者对 AI 热情减弱的情况下下调了融资目标。报道将此描述为这家被视为生成式 AI 热潮领军者的公司，相比此前更激进的募资计划有所收缩。 OpenAI 是生成式 AI 热潮的风向标，因此融资目标的下调可能意味着 AI 资本市场正在转向，进而影响到竞争的大模型开发商、依赖风险投资的 AI 初创公司，以及支撑它们的算力与云服务交易。如果市场顶端的投资者热情都在降温，后期阶段和规模较小的 AI 公司可能面临更苛刻的条款和对营收更严格的审视。 该帖本身只是一个链接帖，没有正文内容，也没有具体金额、估值条款或时间表，同时没有可见的评论讨论，因此仅凭这一条目无法核实融资下调的具体规模以及涉及哪些投资者。因此在看到原始报道之前，这一说法应被视为标题层面的市场信号。

reddit · r/artificial · /u/LinkedInNews · 11月2日 19:47

**背景**: OpenAI 是 ChatGPT 和 GPT 系列模型的开发者，近年来已从微软等投资者和多家大型风险基金处筹集了数十亿美元资金。这些融资被用于支付巨额算力采购、数据中心容量和人才开支，使该公司成为衡量资本市场是否愿意支持昂贵的前沿 AI 研究的代表性指标。自 2022 年底 ChatGPT 发布后，AI 领域的风险投资大幅增长，因此任何情绪降温的迹象都会被视为整个行业的重要指标而受到密切关注。

**标签**: `#OpenAI`, `#AI funding`, `#venture capital`, `#AI industry`, `#investor sentiment`

---

<a id="item-20"></a>
## [英国高等法院判决书中出现不存在的判例引注](https://www.reddit.com/r/artificial/comments/1xmn0l8/uk_high_court_records_a_nonexistent_case_citation/) ⭐️ 7.0/10

英国高等法院 [2026] EWHC 2778 (Admin) 号判决书载明，高级皇家检察官 Ravinder Dhillon 援引了一个名为“R v J”的判例，而法院认定该判例并不存在；她随后解释称自己本意是指另一项真实存在的裁决。据《卫报》报道，该引注来自一次网络搜索中的 AI 回答，不过判决书本身并未认定是 AI 造成了这一引注。 这是一个有据可查的具体案例：疑似由 AI 生成的引注进入了官方法院记录，这加深了人们对大语言模型在法律检索与文书起草中可靠性的担忧。它也给法院、检察机关和律所带来现实压力，要求它们必须对照原始来源核实每一项引证，而不能轻信生成式文本。 法院认为 Dhillon 的解释“令人不满意”，但认定这一虚构引注并未影响继续起诉之异议的结果，因此该错误没有产生实质性的法律后果。值得注意的是，判决书并未将错误归因于 AI，因此“AI 致错”目前只是媒体报道，而非司法认定。

reddit · r/artificial · /u/andrewaltair · 11月3日 07:53

**背景**: 自 2001 至 2002 年起，英国法院开始使用“中性引注”（neutral citation），它指向判决书本身而非某一公开判例汇编，格式为年份＋法院缩写＋案件编号，因此出现了 [2026] EWHC 2778 (Admin) 这样的写法，其中 EWHC 指英格兰及威尔士高等法院，Admin 指行政法庭。AI“幻觉”指模型把虚假或误导性内容当作事实输出，而法律检索恰恰是风险极高的领域，因为看似合理的案件名称和引注很难与真实引注区分。斯坦福 HAI 的基准测试发现，法律类 AI 工具在约六分之一甚至更多查询中会产生幻觉，监管机构和法院也日益强调，引用未经核实的 AI 输出属于职业能力问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Hallucination_(artificial_intelligence)">Hallucination (artificial intelligence) - Wikipedia</a></li>
<li><a href="https://hai.stanford.edu/news/ai-trial-legal-models-hallucinate-1-out-6-or-more-benchmarking-queries">AI on Trial: Legal Models Hallucinate in 1 out of 6 (or...) | Stanford HAI</a></li>
<li><a href="https://www.innertemplelibrary.org.uk/research-and-training/guide-to-neutral-citations/">Guide to Neutral Citations - The Inner Temple Library</a></li>

</ul>
</details>

**标签**: `#AI hallucination`, `#legal tech`, `#LLM reliability`, `#AI risks`, `#law`

---

<a id="item-21"></a>
## [Apple Intelligence 12 月登陆中国，阿里 Qwen 取代 ChatGPT](https://www.reddit.com/r/artificial/comments/1xmf3on/apple_intelligence_is_finally_coming_to_china_in/) ⭐️ 7.0/10

苹果于 10 月 31 日确认，Apple Intelligence 将于 12 月随 iOS 27.3 登陆中国大陆，开发者测试版将于 11 月 4 日启动。在中国，Siri、Writing Tools 和 Visual Intelligence 将调用阿里巴巴的 Qwen，而非 ChatGPT，以完成文本与图像理解及内容生成。 这使苹果成为最新一家采用区域性 AI 模型合作伙伴的西方科技巨头，进一步凸显全球 AI 生态因监管和地缘政治而走向分化。它还可能为其他严格监管市场如何本地化 AI 功能提供一个可复制的模板。 适用机型包括 iPhone 15 Pro 及后续机型，以及 iPhone Air 和 iPhone Duo，且设备需在中国购买，或设备定位与 Apple Account 地区均设为中国；该功能采用选择加入机制，阿里巴巴表示用户请求和生成回复不会用于模型训练。此次上线是部分功能，不包括 WWDC 2026 上宣布的新一代 Siri AI 及其他下一代功能。

reddit · r/artificial · /u/winer666 · 11月3日 00:58

**背景**: Apple Intelligence 是苹果的个人智能系统，在中国以外市场，其部分 Siri 和写作任务依赖 OpenAI 的 ChatGPT。中国要求生成式 AI 服务遵守本地内容与数据规则，这促使外国公司与获批的国内模型提供商合作。Qwen 是阿里巴巴的大语言模型和多模态模型系列，而 Visual Intelligence 是苹果基于摄像头的功能，用于识别并处理物体与文本。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.apple.com/apple-intelligence/">Apple Intelligence and Siri - Apple</a></li>
<li><a href="https://www.alibabacloud.com/en/solutions/generative-ai/qwen?_p_lc=1">Qwen - Alibaba Cloud</a></li>
<li><a href="https://www.coderhouse.com/en/articles/apple-intelligence-china-alibaba-qwen-hybrid-model">Apple Intelligence in China with Alibaba Qwen | Coderhouse</a></li>

</ul>
</details>

**标签**: `#Apple Intelligence`, `#Alibaba Qwen`, `#AI geopolitics`, `#LLM partnerships`, `#China tech market`

---