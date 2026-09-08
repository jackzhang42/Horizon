---
layout: default
title: "Horizon Summary: 2026-09-08 (ZH)"
date: 2026-09-08
lang: zh
---

> 从 60 条内容中筛选出 22 条重要资讯。

---

1. [《数据流模型》作者十一年后复盘自评](#item-1) ⭐️ 9.0/10
2. [Mistral 融资 30 亿欧元，推动主权开放权重 AI 迈向技术前沿](#item-2) ⭐️ 8.0/10
3. [我们只剩一年修复安全以抵御 AI 漏洞利用](#item-3) ⭐️ 8.0/10
4. [数学家指控 OpenAI 压抑 Navier-Stokes 研究](#item-4) ⭐️ 8.0/10
5. [用消费级 GPU 破解 90 年代证书颁发机构的 RSA 密钥](#item-5) ⭐️ 8.0/10
6. [Jellyfin 12.0 发布，赢得大众好评，成为 Plex 的有力替代品](#item-6) ⭐️ 8.0/10
7. [英伟达重注，延续 AI 热潮](#item-7) ⭐️ 8.0/10
8. [Rich Hickey 2010 年演讲：善用潜意识深度解决问题](#item-8) ⭐️ 8.0/10
9. [LLM 引导的程序进化刷新 10 项圆填充最优解](#item-9) ⭐️ 8.0/10
10. [Yandex 研究员提出将 KV 缓存用作智能体运行时](#item-10) ⭐️ 8.0/10
11. [通过 31,352 次重复基准测量评估 LLM 性能漂移](#item-11) ⭐️ 8.0/10
12. [D2 的高级布局引擎 TALA 现已开源](#item-12) ⭐️ 7.0/10
13. [交互式地图一览洛杉矶百年建造史（1880–2026）](#item-13) ⭐️ 7.0/10
14. [博通下架 VDDK 下载，使迁出 VMware 更难](#item-14) ⭐️ 7.0/10
15. [滥用爬虫在 git.kernel.org 上消耗的 CPU 超过所有合法 git 流量](#item-15) ⭐️ 7.0/10
16. [Rust 2026 年调试调查结果发布](#item-16) ⭐️ 7.0/10
17. [Dan Luu 剖析 AI 智能体使用测试与验证技术的情况](#item-17) ⭐️ 7.0/10
18. [类型推断为何带来可用性问题（2019）](#item-18) ⭐️ 7.0/10
19. [在新硬件平台上启动 Linux 内核的指南](#item-19) ⭐️ 7.0/10
20. [中国基因治疗儿童死亡引发透明度呼吁](#item-20) ⭐️ 7.0/10
21. [实验室发布 EmbedFlow 实现嵌入模型无停机迁移](#item-21) ⭐️ 7.0/10
22. [Rustuna：高性能 Rust 版 Optuna](#item-22) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [《数据流模型》作者十一年后复盘自评](https://www.vldb.org/pvldb/vol19/p4953-fernandez-moctezuma.pdf) ⭐️ 9.0/10

具有开创性意义的《数据流模型》论文作者在获得 VLDB Test of Time 奖之际发布了回顾文章，为他们那篇关于流式分析的原创工作打分。他们认为核心基础——事件时间、拒绝等待数据完整以及强一致性——经受住了时间考验，同时承认窗口与触发器的论述篇幅过大，且触发器是过度设计的产物。 由于《数据流模型》深刻影响了 Apache Beam、Flink 与 Kafka Streams 等现代流处理系统，这种诚实的自我评价为领域指出了未来方向。作者认为流式复杂性应被 SQL 与物化视图隐藏，这意味着流处理正与经典数据库思想走向融合。 回顾指出三处具体不足：窗口与触发器的语义和运维关注纠缠；触发器为一个用户本不该面对的问题提供了过度设计的回答；以流为中心的世界观忽略了流和表本质是同一对象在不同访问语义下的两种表示。文章还追溯了完整性原则如何分化为水位线与快照一致性刷新，并采纳了“留什么、排除什么、再用力推进什么”的自我审视框架。

rss · Lobsters · 9月7日 17:11

**背景**: 《数据流模型》论文于 2015 年由 Google 及其合作研究人员发表于 VLDB，提出了同时面向批处理与流数据的统一编程模型。它推广了事件时间窗口与水位线（watermark）等概念——水位线是事件时间上的动态阈值，用于告知流引擎何时可以安全地确定某个事件时间窗口的结果。这些思想如今支撑着多个广泛使用的开源引擎。在这篇回顾中，作者主张领域应超越底层的流式机制，转向数据库社区长期研究的声明式 SQL 与增量视图维护方法。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.systemoverflow.com/learn/stream-processing-architectures/watermarking-late-data/what-is-watermarking-in-stream-processing">What is Watermarking in Stream Processing?</a></li>
<li><a href="https://developer.confluent.io/patterns/stream-processing/event-time-processing/">Event-Time Processing</a></li>
<li><a href="https://docs.databricks.com/aws/en/structured-streaming/watermarks">Apply watermarks to control data processing thresholds - Databricks</a></li>

</ul>
</details>

**标签**: `#Dataflow Model`, `#Streaming Analytics`, `#A Retrospective`, `#VLDB Test of Time Award`, `#Distributed Systems`

---

<a id="item-2"></a>
## [Mistral 融资 30 亿欧元，推动主权开放权重 AI 迈向技术前沿](https://mistral.ai/news/mistral-makes-sovereign-open-weight-ai-to-frontier/) ⭐️ 8.0/10

Mistral AI 已筹集 30 亿欧元，用以推进其构建主权、开放权重 AI 模型的使命。这使 Mistral 成为欧洲对抗美国和中国主要 AI 实验室的主力替代选择。 这是迄今欧洲 AI 领域规模最大的融资之一，反映出欧洲争取技术自主的决心。希望将数据和模型控制权留在国内的政府与企业，或能从 Mistral 的主权开放权重模式中受益。 开放权重模型会公开训练所得的网络权重，开发者可以下载、本地运行和微调，但并不包含真正的开源 AI 所需的完整训练代码与数据。这笔 30 亿欧元融资旨在将主权 AI 战略与开放权重分发模式结合，使之走向 AI 技术前沿。

hackernews · kuberwastaken · 9月8日 05:06 · [社区讨论](https://news.ycombinator.com/item?id=49605767)

**背景**: 主权 AI 指一个国家利用自己的数据、基础设施和人才来开发、训练和部署 AI 模型的能力。开放权重 AI 会发布训练中产生的数值参数（权重），它与封闭专有系统不同，但也不等同于完整开放源代码的 AI。当前全球前沿 AI 竞赛主要由美国和中国企业推动，这促使欧洲寻求 Mistral 这样本土成长起来的替代解决方案。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://logicity.in/en/blog/mistral-ai-pitches-india-on-sovereign-ai-after-modi-meeting">Mistral AI pitches India on sovereign AI after Modi meeting | Logicity</a></li>
<li><a href="https://www.remio.ai/post/open-weight-ai-gives-users-control-but-open-source-sets-a-higher-bar">Open - Weight AI Gives Users Control, but Open Source Sets a Higher...</a></li>
<li><a href="https://www.cloudmagazin.com/en/2026/06/01/sovereign-ai-as-an-infrastructure-issue-why-open-source-decides-on-sovereignty/">Sovereign AI as an Infrastructure Issue: Why Open Source Decides on...</a></li>

</ul>
</details>

**社区讨论**: 评论意见分歧：有人称赞 Mistral 的另类战略及其在 RAG 和 OCR 场景中的实用价值，也有人怀疑在营收远小于 Anthropic 等对手的情况下它是否有能力资助前沿研究。此外，一些评论对投资方 a16z 抱有反感，也有人主张即便 Mistral 在基准测试中不拔尖，欧洲独特的价值观也足以支持其自主发展 AI。

**标签**: `#AI`, `#Funding`, `#Mistral`, `#Open-weight`, `#Europe`

---

<a id="item-3"></a>
## [我们只剩一年修复安全以抵御 AI 漏洞利用](https://jyn.dev/a-year-to-fix-security/) ⭐️ 8.0/10

文章指出，AI 驱动的漏洞发现技术发展极快，软件行业大约只剩一年时间修复安全问题，否则漏洞将被大规模利用。文中强调，现有大型语言模型（LLM）在识别漏洞方面已极其出色，因此发出紧急行动呼吁。 这之所以重要，是因为 AI 大幅降低了发现和利用软件漏洞所需的时间和技能，使安全态势向攻击者倾斜。如果现在不优先处理安全问题，即使是维护良好的项目也可能被自动化漏洞发现和大规模利用所击溃。 作者具体说明了当前的安全挑战，包括 LLM 在漏洞检测上的进步；社区评论者补充说，多智能体渗透测试框架和租用的 GPU 集群可以快速将攻击规模化。然而误报仍是问题；例如有报告指出，AI 上报的 curl 项目五个漏洞中仅一个被确认为有效 CVE，其余为误报或非安全问题。

hackernews · saikatsg · 9月8日 04:48 · [社区讨论](https://news.ycombinator.com/item?id=49605691)

**背景**: 以 GPT-4 为代表的大型语言模型（LLM）展现了强大的代码理解能力，研究者正将它们用作自主智能体来审查代码并发现安全漏洞。与此同时，攻击者已开始利用 AI 进行漏洞利用和自动化渗透测试，把漏洞利用的开发周期从数周压缩到数小时。低成本算力加上先进的 AI 工具使大规模漏洞发现成为可能，这也是文章提出“一年修复窗口”的原因。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.vulncheck.com/blog/ai-assisted-vulnerability-discovery">The First CVE Wave: Signs That AI-Assisted Vulnerability Discovery Is Reshaping Disclosure Volumes | Blog | VulnCheck</a></li>
<li><a href="https://cloudsecurityalliance.org/artifacts/the-ai-vulnerability-storm">AI Vulnerability: Security Program Guide for CISOs | CSA</a></li>
<li><a href="https://cloud.google.com/blog/topics/threat-intelligence/ai-vulnerability-exploitation-initial-access">Adversaries Leverage AI for Vulnerability Exploitation, Augmented Operations, and Initial Access | Google Cloud Blog</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍认同威胁非常紧迫，Simon Willison 表示“我认为我们连一年时间都没有”，aenis 指出主要限制是运行此类攻击活动的成本。一些怀疑者如 sho 质疑作者关于在 Mac 上快速运行 LLM 的示例，而 pmlnr 则建议简化软件技术栈并遵循“保持简单”原则来提升安全性。

**标签**: `#security`, `#AI`, `#LLMs`, `#vulnerability discovery`, `#software engineering`

---

<a id="item-4"></a>
## [数学家指控 OpenAI 压抑 Navier-Stokes 研究](https://cims.nyu.edu/~tristanb/statement.pdf) ⭐️ 8.0/10

纽约大学 Courant 研究所数学家 Tristan Buckmaster 发表声明，指控 OpenAI 试图压制或收编他关于 Navier-Stokes 方程的研究，甚至在他拒绝后威胁其职业生涯。该声明在 Hacker News 上引发了关于前沿 AI 公司对学术研究影响力的激烈辩论。 Navier-Stokes 解的存在性与光滑性问题是 Clay 研究所七大千禧年难题之一，因此任何与此相关的企业干预指控都关涉到数学中最著名未解问题的学术诚信。这起争议还凸显了人们越来越多的担忧：AI 实验室如何处理研究者的私人数据，以及它们是否会为了利益左右基础科学。 根据 Hacker News 讨论串中的评论，Buckmaster 与在 Anthropic 工作的合作者 Alpöge 过去一年一直使用 AI 工具研究流体动力学问题，OpenAI 涉嫌查看了他们的用户数据并试图左右研究结论。陶哲轩发布了一份数学上的背景解释，Buckmaster 也在 mathstodon.xyz 发布了更详细描述；该 PDF 本身尚未得到独立验证。

hackernews · procedurecall · 9月8日 05:42 · [社区讨论](https://news.ycombinator.com/item?id=49605915)

**背景**: Navier-Stokes 方程是描述粘性流体运动的偏微分方程，是流体力学的基础。在三维空间中，给定初始条件下，是否存在始终光滑的全局解尚未被证明，这被称为 Navier-Stokes 解的存在性与光滑性问题。Clay 数学研究所在 2000 年将它列为千禧年难题之一，并为证明或反例悬赏一百万美元。若能得到确切答案，将标志着数学和物理学的一项历史性进展。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Navier–Stokes_equations">Navier – Stokes equations - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Navier-Stokes_existence_and_smoothness_problem">Navier-Stokes existence and smoothness problem</a></li>
<li><a href="https://www.claymath.org/wp-content/uploads/2022/06/navierstokes.pdf">Existence and smoothness of</a></li>

</ul>
</details>

**社区讨论**: 评论者对 OpenAI 表达了愤怒和怀疑，指责其滥用用户数据窃取并威胁研究人员。一些人讽刺地预测，OpenAI 会归咎于自家模型突破了内部管控并访问了私人聊天记录，另一些人则警告前沿 AI 实验室的“自负”正在膨胀。多位用户分享了 Buckmaster 的更长帖子以及陶哲轩的数学解释链接。

**标签**: `#Navier-Stokes`, `#OpenAI`, `#academic ethics`, `#AI research`, `#mathematical physics`

---

<a id="item-5"></a>
## [用消费级 GPU 破解 90 年代证书颁发机构的 RSA 密钥](https://mcpherrin.ca/2026/09/07/rsa.html) ⭐️ 8.0/10

在一篇新的博客文章中，作者报告称，他用一块消费级 GPU 在大约两天内成功分解了一个 1990 年代证书颁发机构（CA）的 RSA 私钥。这些密钥属于 512 位 RSA；这种强度在当年被视为相当可靠，但现在普通硬件就能破解。 这一实例具体地证明，90 年代的老式加密已不再能保证机密性，因为任何曾用这类密钥保护的数据都可以在事后被还原。它也提醒人们，对需要长期保密的数据而言，更长的密钥和前向保密仍然至关重要。 据评论区介绍，该项目还涉及一个自定义 TLS 实现，因为 Go 的 crypto/tls 已移除对 SSLv3 的支持，而目标客户端是 Netscape Communicator 4.51（系统时钟被设为 2000 年）。也有评论者提醒，文章部分内容由 LLM 生成，因此一些细节仍需核实。

hackernews · Lobsters · 9月8日 01:16 · [社区讨论](https://news.ycombinator.com/item?id=49604637)

**背景**: RSA 的安全性依赖于“分解两个大素数乘积”这一问题的实际难度。对于一般整数，目前最有效的经典算法是普通数域筛法（GNFS）；随着算法和硬件多年进步，它才逐步能够处理 512 位密钥。如今，借助 GPU 上的并行实现，这种分解比上世纪 90 年代便宜得多，因此当年用于真实 TLS 证书的密钥现在可以很快被破解。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/General_number_field_sieve">General number field sieve</a></li>
<li><a href="https://mathworld.wolfram.com/NumberFieldSieve.html">Number Field Sieve -- from Wolfram MathWorld</a></li>

</ul>
</details>

**社区讨论**: 评论区的讨论很活跃，但态度谨慎。有评论者认为，文章把许多有趣的技术细节“留给了 AI”处理，实在可惜；还有人强调，LLM 的输出必须核验，因为“看起来很合理”正是这类模型的强项。更广泛的讨论围绕“两天内破解 512 位证书”这一事实，以及它对于存量加密流量的长期保密性意味着什么。

**标签**: `#RSA`, `#cryptography`, `#security`, `#certificate authority`, `#GPU cracking`

---

<a id="item-6"></a>
## [Jellyfin 12.0 发布，赢得大众好评，成为 Plex 的有力替代品](https://jellyfin.org/posts/jellyfin-release-12.0/) ⭐️ 8.0/10

开源媒体服务器 Jellyfin 发布了最新主版本 12.0。该版本发布后已获得用户好评，尤其是升级过程非常顺畅。 此版本巩固了 Jellyfin 作为 Plex 的开源替代品的地位，对担心 Plex 商业行为的用户尤为关键。对于希望完全掌控媒体、无需订阅费用或外部依赖的自托管爱好者来说，这一发布也很重要。 早期社区反馈表明，从旧版本升级到 12.0 的过程快速且无痛，不过部分媒体条目会暂时消失，直到重新扫描资料库才恢复。值得注意的是，一些因 10.11 性能问题而跳过的用户发现，直接升级到 12.0 非常顺畅。

hackernews · Lobsters · 9月8日 01:56 · [社区讨论](https://news.ycombinator.com/item?id=49604861)

**背景**: Jellyfin 是一个自由开源的媒体系统，采用客户端-服务器架构，让用户能够从自己的服务器向任意设备流式传输媒体。它是 Emby 的一个分支，定位为 Plex 等专有平台的开源替代品，没有订阅费用，也不要求外部连接。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Jellyfin">Jellyfin - Wikipedia</a></li>
<li><a href="https://jellyfin.org/docs/general/about/">About Jellyfin | Jellyfin</a></li>

</ul>
</details>

**社区讨论**: 评论区的整体情绪非常积极，用户形容升级快速无痛，并称赞 Jellyfin 的持续进步。一些持有 Plex 终身通行证的用户表示，他们正密切关注 Jellyfin，视其为 Plex 变得过于强势时的潜在退路。也有少数遗留痛点被提及，例如 Android 客户端的外挂字幕问题，以及三星 Tizen 端选择次要音轨会导致重混流的问题，有用户建议改用 AVPlay 播放器来规避。

**标签**: `#jellyfin`, `#media-server`, `#open-source`, `#self-hosted`, `#release`

---

<a id="item-7"></a>
## [英伟达重注，延续 AI 热潮](https://www.economist.com/podcasts/2026/09/07/nvidias-big-bets-to-fuel-the-ai-boom) ⭐️ 8.0/10

2026 年 9 月 7 日，《经济学人》发布了一期播客，主题是英伟达为助推 AI 热潮而下出的几场大赌注。本期节目将当期刊物中的一篇精选文章转为音频，探讨该公司将如何继续站在快速增长的 AI 行业中心。 这期节目之所以重要，是因为英伟达的战略与 AI 热潮本身密不可分：扩展 Blackwell GPU、NVLink 互联和 CUDA 软件，会直接影响整个 AI 行业的供给、成本与开发者粘性。投资者、观察者与工程师可以借此判断这轮热潮还能维持多久。 这一播客源自《经济学人》的一篇精选文章朗读，代表的是杂志的编辑观点而非技术发布会。其重点是，英伟达的赌注不仅覆盖 GPU 芯片，更覆盖整个生态，从高速 NVLink 互连（每 GPU 3.6 TB/s）到经年累月的 CUDA 开发者生态锁定。

rss · The Economist · 9月7日 09:13

**背景**: 英伟达因 AI 而崛起的路径，是把图形芯片与 CUDA 绑定：CUDA 是公司 2007 年首发的专有并行计算平台，能让 C++、Python、Julia 等语言在 GPU 上高效运行。2024 年发布并持续更新的 Blackwell 架构，正在驱动新一代生成式 AI 数据中心系统。NVLink 这种高速直连技术让每块 GPU 拥有最高 3.6 TB/s 双向带宽，让 GB200 NVL72 等系统可以像一台巨型处理器一样运转。因此，英伟达在 AI 领域的地位建立在硬件与软件环环相扣的投资之上，这正是“大赌注”一词所指的含义。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Nvidia_CUDA">Nvidia CUDA</a></li>
<li><a href="https://www.tomshardware.com/pc-components/gpus/nvidia-blackwell-architecture-deep-dive-a-closer-look-at-the-upgrades-coming-with-rtx-50-series-gpus">Nvidia Blackwell architecture deep dive: A closer... | Tom's Hardware</a></li>
<li><a href="https://www.nvidia.com/en-us/data-center/nvlink/">NVLink & NVLink Switch: Fastest HPC Data Center Platform | NVIDIA</a></li>

</ul>
</details>

**标签**: `#Nvidia`, `#AI`, `#GPU`, `#Hardware`, `#Semiconductors`

---

<a id="item-8"></a>
## [Rich Hickey 2010 年演讲：善用潜意识深度解决问题](https://youtu.be/f84n5oFoZBc) ⭐️ 8.0/10

Lobsters 上有人分享了 Rich Hickey 于 2010 年发表的演讲《Hammock Driven Development》，该演讲主张暂时放下代码，让潜意识去解决难题。这个帖子说明这段经典演讲至今仍能引起开发者共鸣。 这段演讲反对一上来就写代码的压力，影响了许多软件工程师对设计、深度工作与生产力的看法。它至今仍被广泛传播，说明行业依然看重深思熟虑的解决问题方式，而不只是快速迭代。 该视频是 Clojure 编程语言作者 Rich Hickey 在 2010 年所作演讲的录像。分享页面附有指向 Lobsters 讨论帖的链接，但这条新闻本身没有包含讨论内容。

rss · Lobsters · 9月7日 08:31

**背景**: Rich Hickey 在软件界因创造 Clojure 而广为人知，这是一种运行在 JVM 上的函数式 Lisp 方言。他在演讲中建议开发者去散步或坐在吊床上，让潜意识在后台处理难题，并在灵感出现时及时记录下来。

**标签**: `#software engineering`, `#productivity`, `#problem solving`, `#thinking`, `#talk`

---

<a id="item-9"></a>
## [LLM 引导的程序进化刷新 10 项圆填充最优解](https://www.reddit.com/r/MachineLearning/comments/1w9xlyi/llmguided_program_evolution_improves_10_bestknown/) ⭐️ 8.0/10

作者使用 LLM 引导的程序进化，改进了 Packomania csqv 圆填充基准中 N=101–114 的 10 项最佳已知结果，将半径和提高了 2.4%–5.4%，仅用 15 次迭代。总 LLM 成本为 27.72 美元，且 Packomania 独立接受了这些结果。 这项工作表明，LLM 引导的程序进化能够在既定基准上以极低的计算成本超越人类设计的优化算法。它提出了一种可扩展的范式——由 LLM 提出算法改进并交由自动验证器决定取舍，可能加速 AI for science 和数值优化领域的进展。 该方法从一个简单的种子求解器出发，由 LLM 根据结果计分板和失败历史迭代提出算法修改方案，每个候选方案都经过独立验证器评分，只保留改进。作者表示最希望就平台期检测停止规则（plateau-detection stopping rule）获得技术意见；代码、求解结果和论文可在 GitHub 和 arXiv 上获取。

reddit · r/MachineLearning · /u/SIGH_I_CALL · 9月7日 16:54

**背景**: 圆填充问题（circle packing）研究如何将互不重叠的圆放入给定容器内，并优化总面积、半径和等目标。Packomania 托管了多组基准实例，其中 csqv 变体要求在单位正方形内放置 N 个半径可变的圆，使半径之和最大。LLM 引导的程序进化是一种较新的技术：在进化循环中由 LLM 提出代码改动，并由外部评分取代传统适应度函数。先前研究如 Guided Evolution 框架已证明这类通用方法的可行性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/html/2609.05093">LLM-Guided Program Evolution for Circle Packing :Breaking 10...</a></li>
<li><a href="https://packomania.com/">Packomania (52C17)</a></li>
<li><a href="https://en.wikipedia.org/wiki/Packing_problems">Packing problems - Wikipedia</a></li>

</ul>
</details>

**标签**: `#LLM program evolution`, `#optimization`, `#circle packing`, `#AI for science`, `#benchmark results`

---

<a id="item-10"></a>
## [Yandex 研究员提出将 KV 缓存用作智能体运行时](https://www.reddit.com/r/MachineLearning/comments/1w9myqc/kv_cache_as_an_agent_runtime_r/) ⭐️ 8.0/10

Yandex 的研究人员发布了一篇博客文章，提出可以将 Transformer 的 KV 缓存视为智能体运行时，这一思路建立在他们此前 Hogwild! Inference 和 AsyncReasoning 工作的基础之上。文中还预览了一个使用类似技术交互式玩 DOOM 环境的 Qwen3.8-27B 智能体。 这项工作把模型推理与运行时设计重新定义为智能体能力中一条未被充分探索的轴，类似于模型架构和外部 harness 所扮演的角色。如果该方向取得成功，这类技术有望让基于 LLM 的助手响应更快、更具交互性，并能实时适应新信息。 其核心思想是，对注意力缓存的并发访问可以成为一种通用机制：Hogwild! Inference 允许多个并行工作线程共享同一个缓存，而 AsyncReasoning 则是一种无需训练的、在思考的同时进行响应和调整的方法。由于这篇博文只是研究预览而非同行评审论文，DOOM 演示的技术细节仍然有限。

reddit · r/MachineLearning · /u/_puhsu · 9月7日 09:03

**背景**: 在 Transformer 推理中，每个生成的 token 都需要关注之前所有的 token，因此模型会反复计算已见 token 的 key 和 value 向量。KV 缓存将这些向量保存下来以避免重复计算，不过它通常只属于单次生成过程。Hogwild! Inference 和 AsyncReasoning 等研究则把这种推理状态看作可操作、可共享的资源：多个模型实例可以写入同一个缓存，或在新输入到达时继续完成推理。该方向实际上是把 LLM 的内部记忆重新定义为智能体行为的交互式基质，而不仅仅是一种效率优化。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.f22labs.com/blogs/normal-inference-vs-kvcache-vs-lmcache/">Normal Inference Vs Kvcache Vs Lmcache</a></li>
<li><a href="https://arxiv.org/abs/2504.06261">[2504.06261] Hogwild! Inference: Parallel LLM Generation via Concurrent Attention</a></li>
<li><a href="https://arxiv.org/abs/2512.10931">[2512.10931] Asynchronous Reasoning: Training-Free Interactive Thinking LLMs</a></li>

</ul>
</details>

**标签**: `#KV cache`, `#LLM inference`, `#AI agents`, `#interactive systems`, `#research`

---

<a id="item-11"></a>
## [通过 31,352 次重复基准测量评估 LLM 性能漂移](https://www.reddit.com/r/MachineLearning/comments/1w9llr4/measuring_llm_performance_drift_observations_and/) ⭐️ 8.0/10

作者提出了一种纵向基准测试方法论，并基于对 49 个模型进行的 31,352 次重复评分观察进行了分析。结果显示日内评分的标准差为 2.80 分，日间每日中位数的标准差为 8.43 分，表明 LLM 评估存在显著的时间变异性。 这项工作推动领域从静态排行榜快照转向纵向评估，这一点至关重要，因为通过 API 提供的模型可能在公开版本未变的情况下改变行为。依赖基准分数的实践者和研究者需要方法来区分真实的模型漂移与正常变异及基础设施效应。 该方法论使用版本化的基准配置，采用基于重复执行的评估而非 LLM 评判，将可用性故障与有效任务结果分开处理，并在可能时跟踪服务/版本元数据。该文还讨论了基准污染问题，并故意不公布完整的实时任务库以保持测量的完整性。

reddit · r/MachineLearning · /u/ionutvi · 9月7日 07:44

**背景**: 在 LLM 生产系统中，漂移指模型性能随时间逐渐下降，通常由数据分布、用户行为或服务基础设施的变化引起。传统基准测试是静态快照，但通过 API 提供的模型可能每天都在改变行为，即使模型名称不变。纵向基准测试将评估视为时间序列测量问题，将一个模型与其自身先前基线进行比较，而不仅仅是与其他模型比较。作者的平台 AI Stupid Level 在编码、多轮推理和工具使用方面进行持续评估，并以更高频率运行轻量级探针。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.aws.amazon.com/prescriptive-guidance/latest/gen-ai-lifecycle-operational-excellence/prod-monitoring-drift.html">Detecting drift in production applications - AWS Prescriptive Guidance</a></li>
<li><a href="https://medium.com/@tsiciliani/drift-detection-in-large-language-models-a-practical-guide-3f54d783792c">Drift Detection in Large Language Models: A Practical Guide | by Tony Siciliani | Medium</a></li>
<li><a href="https://www.together.ai/blog/evaluate-and-benchmark-llms">How to evaluate and benchmark Large Language Models (LLMs)</a></li>

</ul>
</details>

**标签**: `#LLM evaluation`, `#benchmarking`, `#model drift`, `#performance measurement`

---

<a id="item-12"></a>
## [D2 的高级布局引擎 TALA 现已开源](https://d2lang.com/blog/tala-is-open-source/) ⭐️ 7.0/10

Terrastruct 已将 D2 图表语言的高级布局引擎 TALA 开源，结束了其作为专有付费附加组件的状态，使任何人都可以使用并为该引擎做出贡献。 开源 TALA 使得专注于软件架构的优质图表布局能力对更广泛的 D2 生态免费开放。这降低了个体开发者和爱好者的经济门槛，并为社区驱动的改进打开了大门。 TALA 是一个从零构建且零依赖的图表布局引擎，专门为软件架构图而设计。该项目现已在 GitHub 上可用，而 D2 本身仍保持 100%免费开源；此前 TALA 作为独立安装包以保持这一区分。

hackernews · alixanderwang · 9月7日 23:37 · [社区讨论](https://news.ycombinator.com/item?id=49604150)

**背景**: D2 是一种从声明式文本生成图表的现代文本转图表语言。布局引擎自动定位节点和边，但 D2 的默认引擎因在某些图类型上表现不佳而受到批评，ELK 等替代方案通常效果更好。TALA（Terrastruct 的自动布局方法）由 Terrastruct 打造，是一个带有精细启发式规则、面向架构图的专有引擎。将其开源消除了用户此前采用它时的费用障碍。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/terrastruct/TALA">GitHub - terrastruct/TALA: A diagram layout engine designed specifically for software architecture diagrams · GitHub</a></li>
<li><a href="https://terrastruct.com/tala/">TALA | Terrastruct's AutoLayout Approach</a></li>
<li><a href="https://d2lang.com/tour/tala/">TALA | D2 Documentation</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的评论者普遍欢迎这一开源举措，但对 TALA 的效果评价不一。一些人认为其布局在许多情况下明显更整洁，也有读者指出在一张 Go 队列图中，TALA 使结构看起来比替代方案更复杂。还有人询问其背后的启发式规则，称赞 TALA 相对 ELK 和默认引擎的改进，也有评论抱怨网站在旧版 iOS Safari 上的 CSS 渲染问题。

**标签**: `#open-source`, `#d2`, `#graph-layout`, `#diagramming`, `#devtools`

---

<a id="item-13"></a>
## [交互式地图一览洛杉矶百年建造史（1880–2026）](https://lax-skyline.parcelscope.net/) ⭐️ 7.0/10

ParcelScope 发布了交互式地图 lax-skyline.parcelscope.net，让用户能够查看洛杉矶从 1880 年到 2026 年的建筑建造历史。该地图按建造年代为各地块着色，并在网上引发了关于城市规划与住房政策的广泛讨论。 这个可视化让数十年的城市发展历程变得直观可见，并引发了公众对分区制度、住房可负担性以及洛杉矶原有庞大轨道交通网络被拆除等话题的热烈讨论。通过展示现存建筑的建造年代，它为讨论城市增长与土地利用提供了基于数据的依据。 该地图基于洛杉矶县税务评估官的地块数据，因此只显示仍然存在的建筑。正如评论者所指出的，那些原始建筑已被拆除的老街区会显得稀疏或暗淡，这使一些早期时期看起来远比实际开发程度低。

hackernews · rustywasm · 9月7日 18:52 · [社区讨论](https://news.ycombinator.com/item?id=49601655)

**背景**: 19 世纪末至 20 世纪初，洛杉矶随着有轨电车郊区沿电气化铁路向外扩展而迅速发展。绰号为“红车”的太平洋电气铁路在 20 世纪 20 年代是世界上最大的电气化铁路系统，连接了南加州的众多社区。此后的高速公路建设以及 1980 年代的分区下调等政策变化，深刻改变了该市住房建设的地点与方式。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Pacific_Electric_Railway">Pacific Electric Railway</a></li>
<li><a href="https://en.wikipedia.org/wiki/Streetcar_suburb">Streetcar suburb</a></li>

</ul>
</details>

**社区讨论**: 评论者称赞了该地图，但也提醒说它只显示现存建筑，因此被拆除的老街区不会出现，使早期洛杉矶看起来远比实际情况空旷。还有人借此批评 1980 年代的分区下调加剧了住房成本问题，并对太平洋电气铁路约 1300 英里轨道网络的拆除表示惋惜。

**标签**: `#visualization`, `#urban planning`, `#housing`, `#data analysis`, `#Los Angeles`

---

<a id="item-14"></a>
## [博通下架 VDDK 下载，使迁出 VMware 更难](https://www.virtualizationhowto.com/2026/09/leaving-vmware-just-got-harder-after-broadcom-pulled-vddk-downloads/) ⭐️ 7.0/10

博通已下架 Virtual Disk Development Kit (VDDK) 的下载。VDDK 是备份与迁移工具读写 VMware 虚拟磁盘所依赖的 SDK，因此这次下架给计划迁离 VMware 的组织带来了新的障碍。 VDDK 是许多第三方备份、灾难恢复和迁移产品的基础，因此下架该 SDK 可能会限制 VMware 客户可用的工具。这可能会加深供应商锁定，并加大迁出 VMware 的难度，进而影响企业和整个虚拟化生态。 社区讨论指出，VMware 到 Proxmox 的迁移不受影响，只需将 ESXi 作为存储挂载并复制数据即可；但依赖 VDDK 功能（如更改块跟踪 CBT、HotAdd 和直接 SAN 访问）的企业备份产品可能面临严重问题。收购 VMware 的博通现在管理着 VDDK 及其下载基础设施。

hackernews · josephcsible · 9月7日 20:32 · [社区讨论](https://news.ycombinator.com/item?id=49602699)

**背景**: VMware 曾是应用最广泛的虚拟化平台之一，在 2023 年 11 月被博通收购后，伴随而来的是剧烈的许可调整与大规模产品线精简。Virtual Disk Development Kit (VDDK) 是一套提供库函数的 SDK，用于访问 vSphere、Workstation 和 Fusion 的虚拟磁盘，也是 vSphere Storage APIs for Data Protection (VADP) 的核心组件。Veeam 等备份工具依赖 VDDK 实现高效的虚拟机级备份，因此对众多 VMware 环境的基础设施至关重要。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://techdocs.broadcom.com/us/en/vmware-cis/vsphere/vsphere-sdks-tools/8-0/an-introduction-getting-started-with-vsphere-apis-and-sdks-8-0/example-use-cases-for-vsphere-apis/virtual-disk-api-use-cases.html">Virtual Disk Development Kit - Broadcom TechDocs</a></li>
<li><a href="https://www.vinchin.com/vm-tips/vmware-vadp.html">What Is VMware VADP and How It Helps Backup VM ? | Vinchin Backup</a></li>
<li><a href="https://helpcenter.veeam.com/docs/vbr/userguide/direct_san_access.html">Direct SAN Access - Veeam Backup & Replication User Guide</a></li>

</ul>
</details>

**社区讨论**: 评论普遍对 VMware 的没落感到惋惜，一名前工程师称博通似乎是要在价值归零前榨取利润。也有用户分享了实际迁移经验：一位从 Hyper-V 迁到 VMware 又迁回的人抱怨 Hyper-V 像拼凑起来的工具，另一位则表示从 VMware 迁到 Proxmox 很轻松。还有人半开玩笑地建议保存 VMware 源码以备将来“复活”。

**标签**: `#VMware`, `#Broadcom`, `#VDDK`, `#Virtualization`, `#Migration`

---

<a id="item-15"></a>
## [滥用爬虫在 git.kernel.org 上消耗的 CPU 超过所有合法 git 流量](https://simonwillison.net/2026/Sep/7/creepy-crawlies/) ⭐️ 7.0/10

Konstantin Ryabitsev 报告称，git.kernel.org 上滥用型爬虫消耗的 CPU 已超过包括 git 克隆在内的所有合法访问总和。在任一时刻，五个地理分布式节点中共有 14 个 CPU 核心专门用于为爬虫渲染 git 提交的 HTML。 这突显出滥用爬虫给公共网络服务带来的沉重运维负担，就连 Linux 内核官方 Git 托管这样的旗舰基础设施也不例外。它引发了业界对可持续性以及更好爬虫管理需求的担忧。 渲染工作由 git.kernel.org 使用的 Web 界面 cgit 完成，它把纯 Git 提交转换成 HTML 页面。Simon Willison 表示，他担心 Datasette 也面临同样的问题，因为它提供了大量可被爬取页面。

rss · Simon Willison · 9月7日 23:08

**背景**: git.kernel.org 是 Linux 内核的官方公共 Git 仓库托管地，而 cgit 是一种将仓库和提交呈现为可浏览 HTML 的快速 Web 界面。此类站点的合法流量包括直接 Git 克隆和 API 访问，但越来越多 Web 请求来自自动化爬虫或 AI 爬虫。这篇文章将此持续存在的低级别请求量称为“背景辐射”，不断消耗服务器资源。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://wiki.archlinux.org/title/Cgit">cgit - ArchWiki</a></li>

</ul>
</details>

**标签**: `#crawling`, `#web scraping`, `#git.kernel.org`, `#operations`, `#linux kernel`

---

<a id="item-16"></a>
## [Rust 2026 年调试调查结果发布](https://blog.rust-lang.org/2026/09/07/rust-debugging-survey-2026-results/) ⭐️ 7.0/10

Rust 团队于 2026 年 9 月 7 日在官方博客上发布了 2026 年调试调查的结果。该文章总结了社区对调试工具与实践的反馈。 调试仍然是 Rust 开发者常见的痛点，因此这项调查有助于确定工具改进的优先级，并为编译器或调试器相关的工作提供方向。该结果对 Rust 开发者、工具链维护者以及所有关注 Rust 生态的人尤其重要。 该公告的日期为 2026 年 9 月 7 日，但所提供材料中并未包含完整报告内容，仅附有一个外部的 Lobsters 讨论链接。如需查看详细结论和建议，读者应访问该讨论或完整的博客文章。

rss · Lobsters · 9月7日 17:00

**背景**: Rust 是一种系统编程语言，可靠调试需要编译器与 GDB、LLDB 等外部调试器之间的良好配合。长期以来，Rust 开发者曾遇到变量检查不友好、优化后的 release 构建中难以诊断 panic 等问题。此类官方调查是 Rust 项目收集真实开发者体验、指导未来工具链优先事项的一种方式。

**标签**: `#Rust`, `#debugging`, `#survey`, `#developer tools`

---

<a id="item-17"></a>
## [Dan Luu 剖析 AI 智能体使用测试与验证技术的情况](https://danluu.com/agentic-testing/) ⭐️ 7.0/10

Dan Luu 发表了一篇分析文章，考察 AI 智能体在软件工作流中实际运用测试与验证技术的表现。文章似乎提供了基于事实且细致入微的观察，而非对智能体能力的空泛断言。 随着 AI 编程智能体被越来越广泛地采用，了解它们是否真正运用测试与验证技术对软件可靠性至关重要。这篇分析有助于开发者与工程团队判断哪些环节可以信任智能体，哪些环节仍需人工监督。 所提供的新闻条目中未包含文章正文，因此无法提供具体案例或数据点。该条目附有一个 Lobsters 讨论帖链接，供社区评论和补充背景信息。

rss · Lobsters · 9月7日 16:17

**背景**: 编写代码的 AI 智能体通常以生成代码是否正确为评估标准，但较少有人关注它们是否会主动运行测试、编写测试用例或使用验证工具。Dan Luu 是一名软件工程师与作者，以对工程实践进行细致、基于证据的分析而闻名。这篇文章很可能正是通过考察智能体实际使用测试与验证技术时的行为，来探讨这一空白。

**标签**: `#AI agents`, `#software testing`, `#verification`, `#AI/ML`

---

<a id="item-18"></a>
## [类型推断为何带来可用性问题（2019）](https://austinhenley.com/blog/typeinference.html) ⭐️ 7.0/10

这篇由 Austin Henley 于 2019 年撰写的博文指出，类型推断存在可用性问题，并分析了隐式类型给程序员带来的负面影响。文中附有 Lobsters 讨论链接，以便读者参与社区反馈。 类型推断是许多编程语言的核心特性，因此其可用性缺陷会影响大量开发者。这篇文章为编程语言设计以及工具如何更好地呈现推断类型信息的讨论提供了有价值的视角。 该文章发布于 2019 年，位于 Austin Henley 的博客上；本新闻条目中仅包含评论链接，没有详细摘录。文章主要讨论推断类型在开发者体验上造成的权衡。

rss · Lobsters · 9月8日 06:36

**背景**: 类型推断是指编译器或解释器自动检测表达式类型的过程，通常允许程序员省略显式类型标注。这种特性常见于 ML、Haskell 等函数式语言以及许多主流语言，但移除可见的类型信息也可能使代码更难理解或导航。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Type_inference">Type inference - Wikipedia</a></li>

</ul>
</details>

**标签**: `#type inference`, `#programming languages`, `#developer tools`, `#usability`

---

<a id="item-19"></a>
## [在新硬件平台上启动 Linux 内核的指南](https://werwolv.net/posts/linux_bringup/) ⭐️ 7.0/10

werwolv.net 发表了一篇技术指南，介绍如何让 Linux 内核在一个新的硬件平台上启动（bring-up）。该文章被标记为 Linux、内核、嵌入式、平台启动（platform bring-up）相关主题，并附有 Lobsters 讨论帖链接。 内核启动（kernel bring-up）对于希望在新板卡上启用 Linux 的嵌入式开发者来说是关键一步，也常常成为硬件产品开发的瓶颈。一份清晰实用的指南可以帮助工程师缩短从拿到首批硬件到系统成功启动所需的时间。 这篇文章被定位为针对小众但重要主题的技术深度文章，而非具有突破性的新闻；其提供的正文摘要中只包含指向 Lobsters 讨论帖的链接。成功的 bring-up 过程通常依赖于板级文档以及针对启动失败的反复调试。

rss · Lobsters · 9月7日 21:22

**背景**: 在嵌入式 Linux 开发中，内核 bring-up 指的是让 Linux 在新的或修改过的硬件上启动并运行，通常涉及引导加载程序、内核配置和根文件系统。这一过程常常依赖设备树（device tree），设备树用数据结构描述开发板的 CPU、内存、中断线和外设，使内核无需大量改写代码即可支持新硬件。板级支持包（BSP）则记录特定板卡的硬件连接方式，并支持面向多个目标的开发。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://embear.ch/posts/from-hardware-to-linux/">A Guide to Embedded Linux Bring - up - embear GmbH</a></li>
<li><a href="https://docs.kernel.org/devicetree/usage-model.html">Linux and the Devicetree — The Linux Kernel documentation</a></li>
<li><a href="https://en.wikipedia.org/wiki/Devicetree">Devicetree - Wikipedia</a></li>

</ul>
</details>

**标签**: `#Linux`, `#Kernel`, `#Embedded`, `#Platform Bring-up`, `#Hardware`

---

<a id="item-20"></a>
## [中国基因治疗儿童死亡引发透明度呼吁](https://www.nature.com/articles/d41586-026-02497-2) ⭐️ 7.0/10

在中国，两名儿童因基因治疗而死亡，Nature 就此事件发文，呼吁加强信息披露法律。这篇于 2026 年 9 月 8 日在线发表的文章警告称，中国在基因治疗研究领域的声誉正面临风险。 这一事件凸显了在全球基因治疗快速发展中安全与透明的重要性。如果披露机制得不到加强，可能会削弱全球对基因治疗研究的信任，并延缓各国的监管进程。 这篇 Nature 新闻稿的 DOI 为 10.1038/d41586-026-02497-2。文中特别指出，加强相关法律应有助于确保未来发生死亡事件时迅速向公众披露，同时也警示中国科研界的声誉风险。

rss · Nature · 9月8日 00:00

**背景**: 基因治疗是一种通过改变人体基因来治疗或治愈疾病的实验性医疗手段，而中国已成为基因治疗临床试验的重要地区。然而，该领域仍在发展中，患者死亡等严重不良事件引发了关于试验监管和患者安全的紧迫问题。要求加强披露法律的呼声反映出，临床研究中致命结果需要及时向公众通报。这一事件可能促使国际社会更广泛地审视基因治疗试验的开展与监管方式，尤其是在生物技术产业迅速扩张的国家。

**标签**: `#gene therapy`, `#biotech`, `#regulatory`, `#safety`, `#China`

---

<a id="item-21"></a>
## [实验室发布 EmbedFlow 实现嵌入模型无停机迁移](https://www.reddit.com/r/MachineLearning/comments/1wabmm7/my_lab_found_a_way_to_migrate_between_embedding/) ⭐️ 7.0/10

Reddit 用户 u/Potential_Low_1183 宣布了 EmbedFlow，这是一种基于重排序的嵌入模型迁移方法，无需重新嵌入整个语料库。据称，在多达 100 万篇文档的 63 次迁移测试中，该方法能达到与原生检索相同的质量，其中将 Qwen 4B 升级到 8B 时仅需重排 50 篇文档。 在 H100 上重新嵌入 10 亿文档大约需要 108 天，这使得大规模 RAG 系统升级嵌入模型变得很不现实。EmbedFlow 的重排序方法可以让团队以接近零停机的时间和更低的算力成本采用更新的嵌入模型。 该方法先从旧索引中取回候选文档，再用新模型对候选文档进行重排序，而确定足够的 K 值是难点所在。这个包兼容 Qdrant，可以通过 pip install embedflow 安装，其源代码已在 GitHub 上开源。

reddit · r/MachineLearning · /u/Potential_Low_1183 · 9月8日 02:16

**背景**: 嵌入模型会将文档和查询映射为向量，使 RAG 系统能够进行语义相似性搜索；但切换到新模型并不是简单替换，因为不同模型会生成互不兼容的向量空间。传统迁移方法需要将整个语料库重新嵌入到新索引中，这在十亿级文档规模下成本高昂，而且往往会造成停机。重排序是一种两阶段检索技术，先用旧索引返回候选结果，再用更强的模型对候选结果重新评分。EmbedFlow 正是利用这一思路：在旧索引的候选结果上直接提供新模型的检索效果，同时渐进式地生成目标模型的文档向量。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://pypi.org/project/embedflow/">embedflow · PyPI</a></li>
<li><a href="https://qdrant.tech/documentation/tutorials-operations/embedding-model-migration/">Migrate to a New Embedding Model - Qdrant</a></li>
<li><a href="https://medium.com/google-cloud/migrating-vector-embeddings-in-production-without-downtime-8a0464af6f55">Migrating vector embeddings in production without downtime | by Remigiusz Samborski | Google Cloud - Community | Apr, 2026 | Medium</a></li>

</ul>
</details>

**标签**: `#embedding models`, `#RAG`, `#vector search`, `#model migration`, `#reranking`

---

<a id="item-22"></a>
## [Rustuna：高性能 Rust 版 Optuna](https://www.reddit.com/r/MachineLearning/comments/1w9nyhz/rustuna_a_highperformance_rust_implementation_of/) ⭐️ 7.0/10

Optuna 团队发布了 Rustuna，这是一个用 Rust 编写的高性能、内存高效的 Optuna 实现。它在保留 Optuna 熟悉的 API 和概念的同时，彻底移除了对 Python 的依赖。 由于机器学习中的超参数优化常常受 Python 运行开销和依赖相关供应链风险的影响，Rustuna 的发布因此具有重要意义。更低的内存占用有望让大规模调参变得更实用，也反映出机器学习工具链向 Rust 原生实现发展的趋势。 Rustuna 托管在 github.com/optuna/rustuna，相关介绍发布在 Medium 的 Optuna 专栏博客中。它采用与 Optuna 兼容的设计，并利用 Rust 原生优化的内存管理来实现更低的内存占用。

reddit · r/MachineLearning · /u/c-bata · 9月7日 10:01

**背景**: 超参数是在训练开始前设置的参数，用于控制学习过程，例如学习率和批量大小；超参数优化则是选择一组超参数，使模型在给定数据集上的损失函数最小化。Optuna 是一个专为机器学习设计的自动超参数优化框架，其标志性特点是命令式的“define-by-run” API。Rustuna 的目标是让用户沿用这套熟悉的 Optuna 工作流，同时获得 Rust 实现带来的性能和内存优势。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://optuna.org/">Optuna - A hyperparameter optimization framework</a></li>
<li><a href="https://en.wikipedia.org/wiki/Hyperparameter_optimization">Hyperparameter optimization - Wikipedia</a></li>

</ul>
</details>

**标签**: `#Rust`, `#Optuna`, `#Hyperparameter Optimization`, `#Machine Learning`, `#Library`

---