---
layout: default
title: "Horizon Summary: 2026-09-30 (ZH)"
date: 2026-09-30
lang: zh
---

> 从 66 条内容中筛选出 19 条重要资讯。

---

1. [OpenAI 发布 GPT-6.1 Sol：以五分之一价格提供接近 Astra 的智能](#item-1) ⭐️ 9.0/10
2. [OpenAI DevDay 2026：GPT-6 系列模型、Decisions 与 Agents API、Spaces 及 Marketplace](#item-2) ⭐️ 9.0/10
3. [OpenAI 推出 Dots：ChatGPT 中的常驻自主智能体](#item-3) ⭐️ 8.0/10
4. [浏览器实时太阳系可视化：渲染 52.6 万颗小行星与全部在轨追踪卫星](#item-4) ⭐️ 8.0/10
5. [Raschka 梳理文本分类演进：从词袋模型到 Jev](#item-5) ⭐️ 8.0/10
6. [PS5 Relapse 漏洞利用公开：覆盖 7.00–13.60 固件的 WebKit 越狱](#item-6) ⭐️ 8.0/10
7. [研究人员从未受信任应用实现 OnePlus 15 的 root 提权](#item-7) ⭐️ 8.0/10
8. [Livenerf：用于检测 LLM “暗削”的开源工具引发热议](#item-8) ⭐️ 7.0/10
9. [佛蒙特州以家庭电池网络取代调峰电厂](#item-9) ⭐️ 7.0/10
10. [NASA 被曝请前 SR-71 机组协助秘密重启黑鸟](#item-10) ⭐️ 7.0/10
11. [America.gov 上线：由 Gemini 驱动的美国政府公共服务门户](#item-11) ⭐️ 7.0/10
12. [德里将电网电力损耗从 50%降至 5%](#item-12) ⭐️ 7.0/10
13. [Anthropic：GLM-5.3 与 Claude Mythos Preview 首次实现控制流劫持](#item-13) ⭐️ 7.0/10
14. [Shopify 弃用 React Native：一年前还曾大力称赞，如今转向 AI 战略](#item-14) ⭐️ 7.0/10
15. [加密支付卡或让中国绕过管制购买美国 AI 模型](#item-15) ⭐️ 7.0/10
16. [Nura（postmarketOS）公布通向日常可用主线内核手机的路线图](#item-16) ⭐️ 7.0/10
17. [CACM 评论：AI 没有让编程变简单，只是改变了难点的性质](#item-17) ⭐️ 7.0/10
18. [ESP-SDR：原始 IQ 采集让 ESP32 芯片变身低成本 SDR](#item-18) ⭐️ 7.0/10
19. [免费开源新书：从芯片到智能体的机器学习性能工程指南](#item-19) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [OpenAI 发布 GPT-6.1 Sol：以五分之一价格提供接近 Astra 的智能](https://openai.com/index/introducing-gpt-6-1-sol/) ⭐️ 9.0/10

OpenAI 发布了 GPT-6.1 Sol，这是 GPT-6 Sol 的升级版本，定位略低于旗舰型号 GPT-6 Astra，标准 API 价格为每百万输入 token 2 美元、每百万缓存输入 token 0.10 美元、每百万输出 token 10 美元。其缓存输入价格比标准输入价格低 95%，比 GPT-6 Sol 的缓存输入价格便宜 50%，开发者可通过 API 以 gpt-6.1-sol 的名称调用，但目前尚未在 ChatGPT 中上线。 此次发布让 token 价格成为前沿实验室竞争的主战场，进一步印证了「模型能力正在快速商品化」的判断，也压缩了所有出售原始推理能力厂商的利润空间。对于运行大量智能体或编程工作负载的开发者而言，缓存成本减半意味着同样的预算可以支撑多得多的调用量；而对 Anthropic 等竞争对手来说，这加大了定价与商业模式上的压力。 OpenAI 会对 1024 个 token 及以上的提示词自动缓存，但 GPT-6.1 Sol 对每次缓存提示词都会收取缓存写入费用，无论该缓存前缀之后是否被再次读取，因此实际节省幅度取决于复用模式。第三方早期数据颇为亮眼：在 Devin 中，低推理强度下 GPT-6.1 Sol 以每任务 0.21 美元的成本取得 58.1% 的成绩，而同样设置下的 GPT-6 Sol 为 50.5%，这一成绩也是每任务成本低于 0.30 美元的模型中最高分。

hackernews · OpenAI Blog · 9月29日 17:06 · [社区讨论](https://news.ycombinator.com/item?id=49896586)

**背景**: OpenAI 的 GPT-6 系列中，GPT-6 Astra 是旗舰前沿模型，GPT-6 Sol 则是其下更便宜的一档，因此「near-Astra（接近 Astra）」意味着这款低价模型被宣称能在低得多的价格下逼近旗舰级能力。提示词缓存（prompt caching）是一种让服务商存储提示词中重复前缀（例如很长的系统指令或代码库上下文）以避免重复处理的技术，服务商通常会对缓存输入 token 给出大幅折扣。由于 Codex、Devin 这类智能体编程工具每一轮都会重发体量庞大且大体相同的上下文，缓存输入定价往往决定了它们的真实使用成本。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/introducing-gpt-6-1-sol/">Introducing GPT - 6 . 1 Sol | OpenAI</a></li>
<li><a href="https://openrouter.ai/openai/gpt-6.1-sol">GPT - 6 . 1 Sol - API Pricing & Providers | OpenRouter</a></li>
<li><a href="https://devin.ai/blog/gpt-6-1-sol">GPT - 6 . 1 Sol is now available in Devin | Devin</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的评论者普遍认为真正的头条是缓存输入降价而非模型本身，有人指出缓存便宜 50% 会让 Codex 的「续航」大幅提升。不少读者将此举视为 AI 模型缺乏真正护城河、正陷入价格战式商品化的证据，有人据此推测这正是 Anthropic 今年寻求 IPO 的原因；也有人对模型质量持怀疑态度，称 GPT-6 Sol 相比上一代是明显退步、自己已转投 Opus 5.5，并质疑 6.1 会不会有实质区别。

**标签**: `#OpenAI`, `#GPT-6.1`, `#LLM`, `#AI pricing`, `#Hacker News`

---

<a id="item-2"></a>
## [OpenAI DevDay 2026：GPT-6 系列模型、Decisions 与 Agents API、Spaces 及 Marketplace](https://www.latent.space/p/ainews-openai-devday-2026-dots-61) ⭐️ 9.0/10

在 DevDay 2026 上，OpenAI 发布了 20 多项公告，包括 GPT-6 系列模型（Astra、Sol 与 Luna）、名为“Ultrafast”的超低延迟服务、Decisions API 与 Agents API、Spaces 以及 Marketplace，同时公布 ChatGPT 周活跃用户达到 12 亿。根据 OpenAI 自己的回顾，Decisions API 将 Luna 的智能聚焦于一组由用户定义的、答案有限的封闭式问题上。 这些发布表明 OpenAI 正在把自己定位为全栈平台，而不仅仅是模型供应商——它把模型、智能体基础设施、分发渠道（Marketplace）以及终端用户产品（Spaces、ChatGPT）打包进同一个生态。尤其是 Agents API，使 OpenAI 直接与第三方智能体框架展开竞争；而据报道 12 亿的 ChatGPT 周活跃用户数，将使其以巨大优势成为最大的消费级 AI 入口。 Decisions API 以限量预览形式推出，面向分类与路由等受限任务而非开放式生成，并支持以文本或图像作为上下文。Agents API 是构建在 Codex harness 之上的托管服务，由平台负责编排，并提供自动上下文压缩、多智能体编排、程序化工具调用与 MCP 支持，其核心概念包括 Agent、Environment、Session 与 Event。

rss · Latent Space · 9月30日 05:53

**背景**: DevDay 是 OpenAI 面向开发者的年度大会，历史上通常在此发布新模型与新的 API 能力。GPT-6 是 OpenAI 的大语言模型系列：据公开资料，GPT-6 Astra 于 2026 年 9 月 4 日面向公众发布，GPT-6 Sol 与 GPT-6 Luna 则于 2026 年 9 月 22 日推出。这里的“API”指开发者可在自己的软件中调用的编程接口；“智能体（agent）”指能够借助工具进行规划并执行多步操作的 AI 系统，而不仅仅是回答单次提示；MCP（Model Context Protocol）则是此类智能体连接外部工具与数据的标准方式。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/devday-2026-recap/">DevDay 2026 Recap - OpenAI</a></li>
<li><a href="https://en.wikipedia.org/wiki/GPT-6_Astra">GPT-6 Astra</a></li>
<li><a href="https://openai.com/index/introducing-the-agents-api/">Introducing the Agents API | OpenAI</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#DevDay`, `#AI Agents`, `#LLM`, `#Product Launch`

---

<a id="item-3"></a>
## [OpenAI 推出 Dots：ChatGPT 中的常驻自主智能体](https://openai.com/index/introducing-dots/) ⭐️ 8.0/10

OpenAI 在旧金山举办的 DevDay 2026 大会上发布了 Dots，这是一组常驻于 ChatGPT 内部的智能体，拥有独立的云端计算机，可以主动替用户完成多步骤任务。这些智能体由 GPT-6 Astra 驱动，可被个性化设定为小小的团状形象，并能通过插件接入 4000 多个应用；Pro 和 Business Premium 订阅用户可包含一个 Dots 智能体。 这是 OpenAI 迄今最明确的一次转型：从被动响应的聊天机器人走向无需提示即可自主行动的常驻智能体，这一转变可能重新定义人们向 AI 委派工作的方式，也会影响 Grok Bot、Meta 的 Muse 等竞品在智能体产品上的定位。它还加深了 OpenAI 各条产品线——Codex、ChatGPT Work 以及如今的 Dots——之间的重叠，迫使用户重新思考应该把工作流建立在哪个入口之上。 每个 Dots 智能体都拥有独立的沙箱云端计算机、长期记忆与插件访问权限，其设计目标是承接持续性的多步骤项目，而非一次性提问；该功能明确不面向欧洲经济区、瑞士和英国开放，且仅随 Pro 与 Business Premium 套餐附带一个 Dots 智能体，并未作为独立产品单独售卖。

hackernews · alvis · 9月29日 17:07 · [社区讨论](https://news.ycombinator.com/item?id=49896604)

**背景**: 自主智能体与传统聊天机器人的区别在于，它们整合了身份设定、记忆、规划与执行四类能力，因此能够跨会话持续工作，而不是每次对话结束就遗忘。所谓“常驻”智能体更进一步：它们在后台持续运行——通常处于自己独立的云端环境中——并会主动发起任务，这也带来了关于信任、成本以及用户保留多少监督权的新问题。OpenAI 的 Dots 是在 Grok Bot、Meta 的 Muse 等更早的智能体产品之后推出的，同时也处于整个行业向多智能体编排演进的浪潮之中。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.wired.com/story/openai-dots-always-on-ai-agents-that-proactively-help/">OpenAI ’s Dots Are Always - On AI Agents —and Its Answer... | WIRED</a></li>
<li><a href="https://www.datacamp.com/blog/openai-dots">OpenAI Dots : Always - On Agents in ChatGPT, Explained | DataCamp</a></li>
<li><a href="https://guptadeepak.com/the-rise-of-autonomous-ai-agents-a-comprehensive-guide-to-their-architecture-applications-and-impact/">Autonomous AI Agents: Architecture, Applications, Impact, guptadeepak.com</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的反应褒贬不一：一位 Grok Bot 重度用户认为，常驻智能体之间的协作非常强大，因为领域专属的智能体既能避免单个上下文窗口过载，又形成了一道有用的信任边界；但也有人表示自己对“过夜运行”的智能体需求很小，因为自身产出速度受限于人工审核与批准。还有多位评论者抱怨 Codex、ChatGPT Work 与 Dots 之间的界限越来越模糊，其中一人表示自己仍更看好 Meta 的 Muse 作为消费级产品，另有人指出该功能不向欧洲经济区、瑞士和英国开放。

**标签**: `#AI agents`, `#OpenAI`, `#autonomous agents`, `#product announcement`, `#Hacker News`

---

<a id="item-4"></a>
## [浏览器实时太阳系可视化：渲染 52.6 万颗小行星与全部在轨追踪卫星](https://space.bl2.net/) ⭐️ 8.0/10

一位开发者发布了 space.bl2.net，这是一个在浏览器中按真实比例实时呈现太阳系的可视化项目，可渲染约 52.6 万颗小行星以及 CelesTrak 目录中的全部卫星。它整合了 CelesTrak 的 TLE 数据、JPL 小天体数据库（SBDB）中的小行星与彗星，以及 JPL Horizons 的航天器位置，数据每日更新，并提供可正向和反向拖动的时间滑块，卫星会随发射日期出现或消失。 它展示了普通网页图形能力和免费公开天文数据已发展到何种程度：一台普通笔记本就能在浏览器标签页里以 60 帧以上的速度处理 50 万个轨道天体。它还说明，如今构建这类工具的主要门槛是结构化、公开可获取的数据集，而不只是渲染技术本身——评论区把这一点直接与 LLM 辅助开发联系起来。 轨道传播基于 CelesTrak 的 TLE 数据并使用 SGP4 算法，在 Web Worker 中运行，渲染则使用 WebGL2；约 30MB 的小行星数据集在后台加载，因此页面仍可交互。精度受制于源数据本身：JPL SBDB 的轨道通常为二体解，约每半年重新计算一次，误差以 1σ给出，而由 TLE 推算的位置也会随时间推移而变差。

hackernews · wanick · 9月29日 19:08 · [社区讨论](https://news.ycombinator.com/item?id=49898778)

**背景**: WebGL2 是一套 JavaScript API，可利用 GPU 在浏览器中渲染交互式 3D 图形，无需插件即可实现 GPU 加速的物理运算与特效。CelesTrak 是一家发布及时轨道数据的非营利机构，其数据以 TLE（两行轨道根数）形式发布，再通过 SGP4 模型推算卫星位置。NASA 喷气推进实验室（JPL）维护着小天体数据库（SBDB），收录所有已知小行星及多颗彗星的轨道与物理数据，并通过 Horizons 系统提供航天器与行星的高精度星历。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://celestrak.org/">CelesTrak</a></li>
<li><a href="https://en.wikipedia.org/wiki/JPL_Small-Body_Database">JPL Small-Body Database</a></li>
<li><a href="https://en.wikipedia.org/wiki/WebGL">WebGL</a></li>

</ul>
</details>

**社区讨论**: 评论区总体非常热情，有人感叹从当年在 486DX 上为约 30 个天体做轨道计算、勉强跑到 30 帧，到今天在浏览器里以 60 帧以上处理 50 万个天体，代际进步巨大。有用户认为如今借助 LLM 构建这类可视化已很容易，真正的瓶颈是结构化的公开数据；也有人提出如何在夜空中辨认卫星的实用问题，还有人半开玩笑地建议做个“小行星人气投票”的淘汰赛。

**标签**: `#WebGL`, `#astronomy`, `#visualization`, `#open-data`, `#real-time`

---

<a id="item-5"></a>
## [Raschka 梳理文本分类演进：从词袋模型到 Jev](https://magazine.sebastianraschka.com/p/classifier-history-and-jev) ⭐️ 8.0/10

Sebastian Raschka 发表了一篇长文，梳理文本分类技术从词袋模型（bag-of-words）经 RNN、CNN、Transformer 一路演进到 Jev 的历史脉络。Jev 是由 OpenAI 前成员 Diogo Almeida 创办的 TypeSafe AI 推出的专有通用分类模型。文章配有可视化图解，并通过动手实验对比了准确率与效率，尤其重点讨论了概率校准（calibration）与生产环境中的权衡。 文章把 Jev 视为分类领域的潜在“ChatGPT 时刻”——单个模型就能低成本地对任意文本输入进行分类，无需为每个任务单独微调专用分类器，这可能重塑团队构建邮件路由、内容审核等流水线的方式。文章同时把校准问题置于核心位置，反对仅凭整体准确率来评判分类器的常见做法，这一区分对任何要上线“置信度阈值”系统的团队都至关重要。 Jev 属于专有模型，根据 Raschka 引用的 TypeSafe AI 博客基准，它在决策类任务上大致可与 GPT-5.6 Luna 持平，但速度快、成本低若干个数量级；其发布后很快涌现出大量开源复刻版本。文章关于校准的讨论引用了著名的 Guo et al. 研究结论：现代神经网络往往系统性地过度自信，这意味着一个准确率 96% 但概率不可信的模型，在生产环境中可能反而不如一个准确率 94% 但概率诚实的模型。

hackernews · Sebastian Raschka · 9月29日 11:06 · [社区讨论](https://news.ycombinator.com/item?id=49891203)

**背景**: 词袋模型是经典的基线方法，它把一篇文档仅仅表示为其词汇的计数或频率，丢弃了语序和上下文信息；后来它逐渐被 RNN、CNN、Transformer 等能学习上下文表示的神经架构取代。Jev 代表了一类较新的“系统一（System One）”式模型：只专注于一件很窄的事——接收一段文本和一个带预设选项的问题——但做得极快、极便宜，位置介于任务专用分类器和完整的通用大语言模型之间。校准指的是模型预测的概率是否与真实世界中的频率相符：如果一个模型在大量预测中声称“90% 置信度”，那么大约应有 90% 是正确的，这正是置信度阈值策略能够可靠工作的前提。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://magazine.sebastianraschka.com/p/classifier-history-and-jev">Language Models for Text Classification: From Bag-of-Words to Jev</a></li>
<li><a href="https://www.deeplearning.ai/the-batch/models-built-to-do-one-thing-well">Jev, A Classification Model, Takes the Developer World By Storm, Spawns Imitators</a></li>
<li><a href="https://rockyshikoku.medium.com/jev-style-text-classification-system-one-run-locally-how-accurate-can-it-get-57f30ed3594a">Jev-style text classification (System One), run locally. How accurate can it get? | by Daisuke Majima (MLBoy) | Sep, 2026 | Medium</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍称赞这篇文章。nzoschke 表示自己一直在比较各种邮件分类策略，认为 Jev 很有前景，并呼应了 Raschka 将其视为分类领域“ChatGPT 时刻”的说法。aidiscoverywire 认为校准部分是整篇文章中对真正要上线分类器的人最重要的内容，指出生产环境的路由通常基于置信度设置阈值，而一个准确率 96% 却输出过度自信的模型，在实际运营中不如一个准确率 94% 但概率诚实的模型。Moon_Y 则赞赏文章的历史梳理，并表示通用性、速度与成本之间的权衡，以及 Jev 在任务专用分类器与完整 LLM 之间的定位，是最有意思的部分。

**标签**: `#text-classification`, `#language-models`, `#calibration`, `#NLP`, `#LLM`

---

<a id="item-6"></a>
## [PS5 Relapse 漏洞利用公开：覆盖 7.00–13.60 固件的 WebKit 越狱](https://github.com/ntfargo/Relapse-Exploit) ⭐️ 8.0/10

安全研究者 ntfargo 在 GitHub 上公开了名为 Relapse 的 PS5 漏洞利用链，支持 7.00 至 13.60 版本的固件，并利用的是 WebKit 中 JavaScriptCore 引擎的一个漏洞。该利用属于“需重新触发的”（tethered）内核漏洞，可运行 Kstuff、Shadow Mount Plus 和 ETA-HEN 等自制软件工具。 由于该漏洞覆盖了直到近期几乎所有已售出的主机固件，大量现存 PS5 硬件如今都可能被越狱，这将迫使索尼尽快修补，并可能影响处于可破解固件版本的二手主机价格。这也再次引发了关于主机安全模型的公开讨论，尤其是启用了 JIT 的 JavaScript 引擎作为长期攻击面的问题。 该利用属于 tethered（非持久化）类型，每次重启后都需要重新触发，而非一劳永逸；仓库声明其仅用于教育和安全研究目的。值得注意的是，目前最新固件版本已是 14.00，因此出厂即为更新版本或已升级到 13.60 以上的主机并不在该利用链的覆盖范围内。

hackernews · therepanic · 9月29日 15:44 · [社区讨论](https://news.ycombinator.com/item?id=49895304)

**背景**: PS5 的系统软件中包含基于 WebKit 的浏览器组件，而 WebKit 的 JavaScriptCore 引擎使用 JIT（即时编译）来执行 JavaScript，这是一个庞大且经常被攻击的目标——JavaScriptCore 也被 Bun 使用，而 Node.js 和 Chromium 则使用 V8。PlayStation 主机上的越狱通常先用浏览器或 WebKit 漏洞获得代码执行，再用内核漏洞突破沙箱，从而运行未签名的自制程序。另一个长期存在的用户不满是，PS5 禁止把游戏存档复制到用户自己的 USB 存储设备，必须订阅 PlayStation Plus 并按每个用户档案单独开启云备份，这与 PS1 至 PS4 时代截然不同。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/ntfargo/Relapse-Exploit">GitHub - ntfargo/ Relapse - Exploit : Exploit chain for PS 5 7.00 - 13.60</a></li>
<li><a href="https://gbatemp.net/threads/relapse-ps5-kernel-exploit-brings-homebrew-to-firmware-7-00-13-60.684829/">Relapse PS 5 kernel exploit brings homebrew to... | GBAtemp.net</a></li>
<li><a href="https://www.playstation.com/en-us/support/hardware/back-up-ps5-data-USB/">How to back up and restore PS5 console data - PlayStation</a></li>

</ul>
</details>

**社区讨论**: 评论者的关注点更多在现实影响而非漏洞本身：有用户询问它是否能终于实现 USB 存档备份——他因数据损坏损失了一年的 Minecraft 进度，并抱怨如今必须订阅 PS Plus。其他人则讨论了越狱社区囤积零日漏洞与 bootloader 突破线索的现象，推测索尼可能会关闭 JavaScriptCore 的 JIT 以缩小攻击面；还有人表达了矛盾心态——有人希望该发布能等到 GTA 6 之后再出现，也有人期待它最终能让 PS5 运行 Steam 上的 PC 游戏。

**标签**: `#PS5`, `#security-exploit`, `#jailbreak`, `#WebKit-JavaScriptCore`, `#console-hacking`

---

<a id="item-7"></a>
## [研究人员从未受信任应用实现 OnePlus 15 的 root 提权](https://blog.nns.ee/2026/09/24/oneplus-root/) ⭐️ 8.0/10

一名安全研究人员在 blog.nns.ee 上发布文章，演示了如何从一个未受信任的普通 Android 应用出发，最终在 OnePlus 15 上获得 root 权限。文章完整地展示了一条移动端提权利用链，使攻击者能够从被沙箱隔离的应用上下文一路提升到设备的最高权限级别。 这表明即便有 Android 的多层防御机制——按应用划分的 UID、SELinux 强制访问控制以及 untrusted_app 沙箱——精心串联起来的多个漏洞依然可以在当代旗舰手机上拿到完整的 root 权限。这类研究对 OnePlus 15 用户、Android 平台防御方以及所有依赖应用隔离作为安全边界的人都至关重要，同时也提升了利用链对攻击者与渗透测试人员的价值。 目前公开的材料只是一篇研究员博客，外加一个指向 Lobste.rs 讨论的链接，摘要中并未披露 CVE 编号、具体存在漏洞的组件、受影响的固件/OxygenOS 版本，也未说明一加是否已修复其中任何一个问题。从 untrusted_app 域提升到 root 通常需要串联多个不同的弱点，例如一个有漏洞的内核驱动或厂商组件，再配合某种绕过 SELinux 限制的手法。

rss · Lobsters · 9月29日 17:25

**背景**: Android 会把每个第三方应用隔离在独立的 Linux UID 和独立的 SELinux 域中；默认情况下，应用进程的类型为 untrusted_app，平台的 SELinux 策略拒绝其访问系统数据、内核接口以及其他应用的文件。正是由于这种强制访问控制，在 Android 上获取 root 很少能靠单个漏洞完成，通常需要串联应用沙箱逃逸、进入更高权限上下文，最后实施内核级利用。root 是设备上的最高权限级别，可以以超级用户身份执行任意代码，因此攻击者和刷机/渗透测试社区都对此趋之若鹜。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://source.android.com/docs/security/features/selinux/concepts">SELinux concepts | Android Open Source Project</a></li>
<li><a href="https://codelucky.com/android-security-model/">Android Security Model: Complete Guide to Permission System and Sandboxing - CodeLucky</a></li>
<li><a href="https://android.googlesource.com/platform/external/sepolicy/+/57531cacb40682be4b1189c721fd1e7f25bf3786/untrusted_app.te">untrusted_app.te - platform/external/sepolicy - Git at Google</a></li>

</ul>
</details>

**标签**: `#security`, `#android`, `#exploit`, `#privilege-escalation`, `#mobile-security`

---

<a id="item-8"></a>
## [Livenerf：用于检测 LLM “暗削”的开源工具引发热议](https://github.com/ninjahawk/livenerf) ⭐️ 7.0/10

一位开发者发布了 livenerf，这是一个小型、只追加记录、尽可能确定性的基准测试，通过对 Opus 5.5 等前沿模型反复运行固定提示集，来检测模型在发布后是否被悄悄削弱。该仓库会记录输出长度、事实准确率和拒答率等指标，并在 Hacker News 上引发了 559 分、239 条评论的热议，讨论所谓“暗削（nerf）”是否真实存在。 如果服务商确实会在发布后悄悄降低模型质量，这将损害人们对付费 API 的信任，并影响所有基于这些模型构建产品的开发者，而此前并没有公开工具系统地长期追踪这类变化。这场讨论之所以重要，是因为它让用户的主观体验与统计测量形成对立，也涉及 AI 厂商应如何为无声的后端变更负责。 据相关报道，livenerf 每天运行约 200 条固定提示集，并被设计成确定性的、只追加记录，以免结果被事后篡改。一篇关于检测模型退化的统计论文称，其框架能识别低至 0.3% 的准确率下降，这说明有意义的性能回退可能非常细微，难以与噪声区分。

hackernews · bryan0 · 9月29日 22:36 · [社区讨论](https://news.ycombinator.com/item?id=49901736)

**背景**: LLM“暗削（nerf）”指的是这样一种怀疑：服务商在不告知用户的情况下，通过后端调整、量化、路由或安全微调等方式，悄悄让已部署的模型变差。由于用户看不到模型权重或服务基础设施，只能从行为表现反推变化，因此很难区分真实的性能回退与正常波动、上下文窗口限制或心理上的“蜜月期”效应。livenerf 和 Nerf Bench 这类工具正是试图通过将模型输出与其发布当日的基线进行对比来填补这一空白。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/ninjahawk/livenerf">GitHub - ninjahawk/livenerf: Benchmark for tracking model capability after release. · GitHub</a></li>
<li><a href="https://www.promptzone.com/miles_dvorak/livenerf-tracking-opus-55-nerfs-via-hn-data-1bgi">Livenerf: Tracking Opus 5.5 Nerfs via HN Data - PromptZone</a></li>
<li><a href="https://arxiv.org/html/2602.10144v1">When LLMs get significantly worse: A statistical approach to detect model degradations</a></li>

</ul>
</details>

**社区讨论**: 评论者意见严重分化：johnfn 等人认为在绝大多数被报告的情况下“暗削”并不存在，用户只是在对噪声进行模式匹配或撞上了复杂度上限；而 sheepscreek 等人则认为，庞大基础设施中持续累积的细微变更很可能是暂时性回退的成因。jug 提到了竞品 Nerf Bench，它曾检测出 Anthropic 后来承认的 Opus 4.6 性能退化；msejas 则分享了一段轶事——在提交反馈后感觉质量立刻下降，并猜测可能存在按会话（per-session）的削弱。

**标签**: `#LLM`, `#benchmarks`, `#model-degradation`, `#AI-tooling`, `#community-discussion`

---

<a id="item-9"></a>
## [佛蒙特州以家庭电池网络取代调峰电厂](https://www.bbc.com/future/article/20260928-a-virtual-power-plant-hidden-in-vermont-homes-is-keeping-the-lights-on-during-storms) ⭐️ 7.0/10

据相关报道，佛蒙特州的虚拟电厂（由软件协调的家庭电池网络）已成为该州最大的单一能源来源，并已促成两座调峰电厂关停。报道描述的方案中，参与家庭每月支付约 55 美元即可获得两块 Tesla Powerwall，并根据其在停电和用电高峰时段同意向电网回馈的容量获得电费减免。 这是一个真实落地的案例，表明分布式家庭电池能够在相当规模上取代化石燃料调峰电厂，为其他州和国家提供了一条无需新建发电机组即可增加电网容量的路径。与此同时，它也把“谁为该分布式基础设施付费、谁从中获利”——是电价用户、房主还是公用事业公司——这一经济问题推到了公众讨论的中心。 据报道，该计划为每户提供两块 Tesla Powerwall，月费约 55 美元，电费抵扣额度取决于房主允许公用事业公司在停电期间调用多少电量。批评者指出，电池本质上是电力的净消费者而非发电设备，存在充放电往返损耗和容量衰减，而且用储能替代发电只有在峰值容量本就过剩时才最合理。

hackernews · devonnull · 9月29日 18:19 · [社区讨论](https://news.ycombinator.com/item?id=49897993)

**背景**: 虚拟电厂（VPP）是将成百上千个小型的分布式设备——家庭电池、太阳能板、智能恒温器、电动车充电桩——通过软件连接起来，使其能够像一个统一电源那样被统一调度，从而提供满足高峰负荷、维持电网频率等服务。调峰电厂是通常只在用电需求激增时才运行的发电厂；由于运行时间很短，其发电成本高昂，且多以天然气为燃料。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Virtual_power_plant">Virtual power plant - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Peaking_power_plant">Peaking power plant - Wikipedia</a></li>
<li><a href="https://www.tesla.com/learn/what-is-a-virtual-power-plant">What Is a Virtual Power Plant? - Tesla</a></li>

</ul>
</details>

**社区讨论**: 评论意见分歧明显：一位澳大利亚用户表示自己在政府补贴下自购了太阳能和电池，乐于让虚拟电厂在需求高峰时向外输出电力，因为这在电价上对自己有利；而另一些人则认为佛蒙特的方案是公用事业公司转嫁成本的把戏，让家庭为并不属于自己所有的电池支付数千美元，理应反过来为承载电网设施付费。还有人从技术角度提出，电池消耗而非生产电力，只有在峰值容量过剩时才能真正替代发电。

**标签**: `#energy`, `#virtual-power-plant`, `#batteries`, `#grid-infrastructure`, `#climate-tech`

---

<a id="item-10"></a>
## [NASA 被曝请前 SR-71 机组协助秘密重启黑鸟](https://aviationweek.com/defense/aircraft-propulsion/nasa-asked-several-former-sr-71a-staffers-help-secret-restart) ⭐️ 7.0/10

据《航空周刊》(Aviation Week) 报道，NASA 曾邀请数名曾参与 SR-71A 工作的前工作人员，协助一项秘密行动，试图让已退役的“黑鸟”重新恢复可飞或可用状态。报道未披露公开的时间表、预算或官方任务理由，NASA 也未确认该计划的具体范围。 重启一架已退役数十年的 Mach 3 以上侦察机，令人质疑当今的卫星、无人机和高超音速项目是否在高速、高空侦察能力上仍存在缺口。同时，这也凸显了国防工业基础的脆弱性——当年黑鸟退役后，工装、备件和专用燃料供应链被有意拆除。 有评论者指出，NASA 据称选中的是最后一架下线的机身 SN 61-7980，但它长期停放在爱德华兹空军基地的露天环境，而非博物馆内；相比之下，SN 61-7964 一直存放于战略空军司令部博物馆的室内。美国空军和 NASA 在 2007 年销毁了价值约 6 亿美元的黑鸟备件，而且只有 SR-71 使用的 JP-7 燃料已不再生产，这意味着加油机也需重新改装才能加注该燃料。

hackernews · ilamont · 9月29日 10:10 · [社区讨论](https://news.ycombinator.com/item?id=49890733)

**背景**: 洛克希德 SR-71“黑鸟”是臭鼬工厂（Skunk Works）研制的高空、Mach 3 以上侦察机，机体约 85% 为钛合金，配备两台 J58 加力涡喷发动机。其油箱设计为仅在高温下密封，因此飞机在地面时会故意渗漏 JP-7 燃料，直到高速飞行时的热膨胀把缝隙封住。美国空军于 1998 年将 SR-71 退役，NASA 也在 1999 年结束最后的黑鸟飞行任务；此后洛克希德·马丁曾公开宣传高超音速的 SR-72“暗星”作为概念上的后继机型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://theaviationgeekclub.com/jp-7-the-fuel-that-powered-the-sr-71-blackbird-caused-a-nationwide-shortage-of-bug-spray-heres-why/">JP - 7 , the fuel that powered the SR - 71 Blackbird caused a nationwide...</a></li>
<li><a href="https://nationalsecurityjournal.org/85-of-the-sr-71-blackbirds-airframe-was-built-from-russian-titanium-that-the-cia-secretly-bought-through-shell-companies/">85% of the SR - 71 Blackbird's Airframe Was... - National Security Journal</a></li>
<li><a href="https://www.airforce-technology.com/features/feature-lockheed-martin-unveils-sr-72-successor-sr-71-spy-plane/">Lockheed Martin unveils SR - 72 as successor to... - Airforce Technology</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的整体情绪以怀疑和怀旧为主：多位评论者质疑重启 60 年前的技术是否合理，并将其与今年的蒸汽弹射器争议相提并论；另一些人则认为已有更快、很可能是无人驾驶的机密机型在服役（提及 RQ-180 和 Polecat）。还有人关注实际问题——机身选择、被销毁的备件以及 JP-7 停产——并有人强烈推荐本·里奇的回忆录《臭鼬工厂》(Skunk Works)。

**标签**: `#aerospace`, `#SR-71`, `#NASA`, `#defense`, `#engineering`

---

<a id="item-11"></a>
## [America.gov 上线：由 Gemini 驱动的美国政府公共服务门户](https://america.gov/) ⭐️ 7.0/10

美国政府推出了全新的公共服务门户 America.gov，目标是帮助超过 1 亿人找到并获取各类公共服务；Google 表示自己是该计划的技术合作伙伴，使用 Gemini 为大模型驱动的体验提供支持。该消息迅速在 Hacker News 上引发热议，获得 535 分和 445 条评论。 这是大型语言模型在国家政府面向公民的服务中最受瞩目的落地案例之一，可能为其他政府机构采用 AI 提供公共服务的做法树立先例。如果成功，它能显著降低民众判断自己能申请哪些福利和服务的门槛，但同时也把隐私、安全和可访问性问题直接推到公众视野中。 Google 表示该计划使用 Gemini 帮助人们“更快、更轻松地”获取关键公共资源；有评论者将该实现方式概括为“Gemini + 护栏（guardrails）”，即模型输出受到安全和政策过滤器的约束。批评者还指出了具体的界面问题，例如一个指纹/隐私图标覆盖在关于保护隐私的段落上且无法关闭，以及对极老旧浏览器兼容性的担忧。

hackernews · plesiv · 9月29日 14:04 · [社区讨论](https://news.ycombinator.com/item?id=49893509)

**背景**: Gemini 是 Google 的大语言模型系列，也是其对话式助手背后的技术，这类助手用自然语言直接生成答案，而不是返回一串链接。“护栏（guardrails）”指的是围绕模型设置的安全层与政策约束，使其拒绝或改答有害、跑题或存在法律风险的请求——对一个不能给出错误资格建议的政府服务来说，这是关键的设计选择。办理政府事务向来困难，因为各种福利分散在规则各异的多个机构中，这正是聊天机器人常被宣传能解决的“大海捞针”式问题。钓鱼攻击（伪造官方网站或消息）则是与之密切相关的风险，因为搜索政府帮助信息的民众正是攻击者的重点目标。

**社区讨论**: 评论情绪褒贬不一：有几位评论者认为这个想法本身很有价值，指出在繁杂的政府服务中找到正确的办事路径，正是精心设计的聊天机器人能够真正发挥作用的“大海捞针”场景。怀疑者则警告钓鱼风险，建议只在沙箱中打开该链接，批评无法关闭的隐私图标设计糟糕，并深入讨论了该系统“Gemini + 护栏”的技术实现方式。

**标签**: `#government-tech`, `#AI/ML`, `#Gemini`, `#public-services`, `#privacy-security`

---

<a id="item-12"></a>
## [德里将电网电力损耗从 50%降至 5%](https://spectrum.ieee.org/delhi-electricity-loss) ⭐️ 7.0/10

IEEE Spectrum 发表了一篇深度报道，讲述德里如何把电力输配损耗——其中很大一部分源于猖獗的窃电——从大约 50%降到约 5%。这篇报道在 Hacker News 上获得 510 分、286 条评论，文中把这一转变归因于绝缘架空集束电缆、更完善的计量等一系列反窃电措施的组合，而非某一项单一的技术突破。 如此大幅度地降低损耗说明，在许多发展中国家，电网损耗与其说是工程问题，不如说是商业与治理问题；而解决它可以把一家濒临破产、依赖补贴的电力公司变成一家可持续经营的企业。如果这种经验可以复制，就能释放出用于增长的发电容量，并使太阳能、储能和电气化投资对数以亿计的用户而言变得可负担得多。 这些干预措施不仅是硬件改造，更是威慑手段：用架空集束电缆把配电线路绝缘起来既能防止非法搭接，又——正如一位评论者所观察到的——顺带让猴子可以安全地沿着电线在社区之间穿行。文章强调，窃电者既有权贵也有平民——商户、居民用户，甚至包括有利益关联的电力公司员工——他们从路灯和邻近配电线上盗接电力，而电力公司过去既缺乏资源去识别，也无力去处罚。

hackernews · rbanffy · 9月29日 12:43 · [社区讨论](https://news.ycombinator.com/item?id=49892245)

**背景**: 电力公司通常用“综合技术与商业损耗”（AT&C losses）来衡量绩效，它由技术损耗（变压器和导线发热造成的损失）和商业损耗（窃电、未计量用电和计费失败）两部分组成；在印度许多邦，这一数字曾经高达 40%~50%。与之相关的另一个现象是“拉闸限电”（load shedding），即电力公司在供不应求时主动实施的轮流停电。解决该问题的两项关键技术是：架空集束电缆（ABC）——把绝缘相导线紧密捆扎在一起、而不是用空气间隙隔开的架空线路；以及高级计量基础设施（AMI）——能够双向通信的智能电表，可让电力公司获取实时用电数据，并使窃电篡改更容易被发现。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Aerial_bundled_cable">Aerial bundled cable</a></li>
<li><a href="https://anyline.com/news/atc-losses-facts-and-solutions">AT & C Losses : Key Facts and Solutions for the Utility Industry</a></li>
<li><a href="https://electricalampere.com/at-and-c-losses/">AT & C Losses | Meaning, Formula, Causes & Best Practices</a></li>

</ul>
</details>

**社区讨论**: 评论者大体上认同，标题中的数字低估了这件事对人的影响：他们认为真正具有革命性的是消除了非计划性拉闸限电——过去一天可能停电好几次，逼得家庭不得不拔掉电器插头以免复电时的电压冲击。也有人指出了一些意想不到的后果，比如绝缘电线让猴子可以安全地在社区之间“开辟道路”，并把太阳能加电池、屋顶乃至垂直光伏面板、社区级 BESS 视为印度充沛日照下的自然下一步。还有人强调窃电是系统性的，权势者与普通人都参与其中，而电力公司根本没有手段去发现或处罚。

**标签**: `#energy-infrastructure`, `#electrical-grid`, `#india`, `#sustainability`, `#systems-engineering`

---

<a id="item-13"></a>
## [Anthropic：GLM-5.3 与 Claude Mythos Preview 首次实现控制流劫持](https://simonwillison.net/2026/Sep/29/anthropic-frontier-red-team/) ⭐️ 7.0/10

Anthropic 的 Frontier Red Team 在其内部二进制漏洞利用（Binary Exploitation）基准中随机抽取 100 个任务评测多个模型，发现 GLM-5.3 在 4% 的试验中实现了完整的控制流劫持，Claude Mythos Preview 则为 6%。而更早的模型，如 Claude Opus 4.6 和 GLM-5.2，在这些试验中一次都没有成功。 这标志着一条能力门槛被明确跨越：过去得分为零的模型如今能够自主产出可用的漏洞利用程序，这对 AI 网络能力预测、安全政策以及两用风险都有直接影响，因为高级攻击能力正从少数前沿实验室向外扩散。由于 GLM-5.3 并非美国实验室的模型，这一结果也加剧了关于开放权重与国际网络能力扩散的争论。 这些数字虽小但非零——在 100 个内部基准任务的随机样本上分别为 4% 和 6%——且该评测使用的是 Anthropic 自有的内部基准，被引用的段落并未公开说明任务内容、评分标准和提示方式。Simon Willison 的帖子本身只是对该结论的简短引用，没有附带分析，因此应将其视为一个高信号的数据点，而非经过同行评审的测量结果。

rss · Simon Willison · 9月29日 22:20

**背景**: 控制流劫持（control flow hijack）是一类漏洞利用方式：攻击者取得程序指令指针的控制权——通常借助缓冲区溢出或格式化字符串漏洞——使程序执行攻击者选定的代码，而非原本的逻辑。二进制漏洞利用（binary exploitation）则是安全领域的一门技术，指在没有源代码的情况下，从已编译的可执行文件中发现并武器化此类内存安全缺陷。此前，完整地跑通这种多步推理与调试链条被认为超出了 LLM 智能体的能力范围，因此即便是个位数的成功率，非零也意义重大。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://nhimg.org/glossary/control-flow-hijacking/">What Is Control - Flow Hijacking ? Definition & Examples</a></li>
<li><a href="https://kam.mff.cuni.cz/pitfalls/06-pwn/">Binary exploitation | Pitfalls of Computer Security</a></li>
<li><a href="https://medium.com/@kvsivabharath/binary-exploitation-buffer-overflow-7f1b0a527ac0">Binary Exploitation. Buffer Overflow | by Sivabharath K | Medium</a></li>

</ul>
</details>

**标签**: `#ai-security`, `#ai-safety`, `#cyber-capabilities`, `#llm-evaluation`, `#anthropic`

---

<a id="item-14"></a>
## [Shopify 弃用 React Native：一年前还曾大力称赞，如今转向 AI 战略](https://newsletter.pragmaticengineer.com/p/shopify-native-mobile) ⭐️ 7.0/10

据 The Pragmatic Engineer 简报报道，Shopify 正在放弃在其移动应用中使用 React Native——而就在大约一年前，该公司还公开表示对该框架非常满意。报道称此次转向的原因是 AI 相关的战略考量，而非单纯的技术缺陷。 Shopify 是公开力挺 React Native 的最知名企业之一，因此它的转向对整个跨平台移动开发生态、以及正在做类似技术选型的工程负责人来说都是一个重要信号。这也说明 AI 优先的战略正在越来越多地重塑大型产品公司的基础工程决策。 目前可获得的摘要并未说明 Shopify 将改用何种技术替代、迁移时间表如何，也未说明受影响的移动端代码规模有多大，因此这次变更的技术范围仍不明确。官方给出的理由是战略性和 AI 驱动的，这意味着该决定可能更多取决于组织与工具链方向，而非单纯的框架性能。

rss · The Pragmatic Engineer · 9月29日 15:53

**背景**: React Native 是由 Meta（原 Facebook）开发的开源 UI 框架，允许开发者用同一套 JavaScript 与 React 代码库构建 iOS 和 Android 应用，其组件会直接映射到各平台的原生 UI 构建块。它的核心卖点是以“学一次，随处编写”的方式实现跨平台开发，同时保持接近原生的性能，因此拥有大型移动团队的公司常常采用它。Shopify 先公开称赞、随后又弃用的过程，体现了业界一个反复出现的矛盾：共享代码库能加快交付，但当 AI 驱动的开发工具等新的战略优先级出现时，团队可能会重新倾向于完全原生的代码。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/React_Native">React Native - Wikipedia</a></li>
<li><a href="https://reactnative.dev/">React Native · Learn once, write anywhere</a></li>

</ul>
</details>

**标签**: `#React Native`, `#Shopify`, `#Mobile Development`, `#AI`, `#Software Engineering`

---

<a id="item-15"></a>
## [加密支付卡或让中国绕过管制购买美国 AI 模型](https://www.economist.com/finance-and-economics/2026/09/29/the-ai-boom-meets-a-new-kind-of-crypto-scam) ⭐️ 7.0/10

《经济学人》发表分析文章指出，与加密货币账户绑定的支付卡可能让中国用户得以付费使用美国 AI 模型，从而绕过美国的出口管制。该文于 2026 年 9 月 29 日发布，将这一现象描述为在 AI 热潮与加密支付通道交汇处出现的一种新型规避监管手段。 美国对先进 AI 硬件和模型的出口管制是中美科技竞争的核心杠杆，而能够掩盖真实付款方及其所在地的支付通道，会让这些管制措施的执行难度大幅上升。如果加密支付卡真能被用来购买模型访问权限，那么 AI 企业、支付服务商以及美国工业与安全局（BIS）等监管机构可能都需要建立新的合规与筛查机制。 加密支付卡允许持有人像使用普通借记卡一样消费其稳定币或加密货币余额，而且其身份审核通常比直接使用银行账户或企业电汇更为宽松。不过目前可获得的摘要非常简短，因此文章关于具体涉及哪些发卡机构、哪些模型或交易规模，以及这一漏洞实际有多大的证据仍不明确。

rss · The Economist · 9月29日 16:05

**背景**: 美国出口管制由工业与安全局（BIS）依据《出口管理条例》（EAR）执行，限制最先进半导体以及用于训练前沿 AI 的算力的出口，并日益扩展到 AI 模型权重和输出内容。通过托管的 API 访问前沿模型属于灰色地带：模型本身并未离开美国服务器，但其能力实际上跨越了国界，监管机构已开始把模型输出视为受管制对象。与此同时，以稳定币或加密货币余额而非银行账户作为资金来源的加密支付卡，作为一种零售支付渠道不断增长，部分原因在于其发行速度快、与传统银行身份的关联度低。《经济学人》的论点正是把这两种趋势结合起来：一种难以追踪的支付方式，加上一项按国籍受限的服务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://cset.georgetown.edu/article/dont-forget-the-catch-all-basics-ai-export-controls/">For Export Controls on AI, Don’t Forget the “Catch-All” Basics</a></li>
<li><a href="https://www.justsecurity.org/126643/ai-model-outputs-export-control/">AI Model Outputs Demand the Attention of Export Control Agencies</a></li>
<li><a href="https://www.pionex.com/blog/crypto-cards-with-yield/">Crypto Cards With Yield: How They Work & Compare (2026)</a></li>

</ul>
</details>

**标签**: `#AI policy`, `#crypto scams`, `#export controls`, `#geopolitics`, `#fintech`

---

<a id="item-16"></a>
## [Nura（postmarketOS）公布通向日常可用主线内核手机的路线图](https://postmarketos.org/blog/2026/09/29/road-to-main-category/) ⭐️ 7.0/10

Nura（原 postmarketOS）发布了一篇日期为 2026-09-29 的博客文章《The road to daily-drivable mainline phones》，阐述了将设备推进到 wiki 中「main」分类的路线图，该分类专门收录最接近日常可用水平的手机。这篇文章是一份路线图与设备分类规划更新，而非某个单一新功能或新版本的发布公告。 「能否日常使用」一直是开源移动 Linux 项目与主流 Android/iOS 设备之间的核心差距，因此一份面向「main」层级的正式路线图，意味着生态正从技术演示转向可靠性目标。这对 Linux 手机用户和维护者影响最大，因为设备分类决定了新手被推荐购买哪些机型，以及哪些移植版本能获得持续维护。 该路线图围绕设备分类展开，其中「main」指被认为最接近日常主力机水准的机型；在这一生态中，这一标准通常意味着使用主线 Linux 内核并让绝大多数硬件组件可用。由于所提供的条目仅包含一个 Lobste.rs 讨论链接而没有评论正文，文章中的具体里程碑以及可能附带的设备清单在此无法核实。

rss · Lobsters · 9月29日 19:20

**背景**: Nura 原名 postmarketOS（pmOS），是一个面向智能手机和平板电脑的自由开源操作系统，基于轻量的 Alpine Linux 发行版，自 2016 年开始开发、2017 年正式发布。与 Android 依赖厂商定制、往往陈旧的私有内核不同，这类项目力求运行上游「主线」（mainline）Linux 内核，使设备能持续获得安全修复与驱动改进，以支撑该项目提出的手机十年生命周期目标。它可运行 Plasma Mobile、GNOME、Phosh、MATE、XFCE 等多种用户界面，早期的里程碑常以手机成功启动主线内核的照片来庆祝。所谓「日常可用」，指的是手机在通话、消息、续航和拍照等方面足够可靠，而不仅仅是能开机或跑个演示。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/PostmarketOS">postmarketOS - Wikipedia</a></li>
<li><a href="https://postmarketos.org/">postmarketOS // real Linux distribution for phones</a></li>
<li><a href="https://lwn.net/Articles/772298/">Running Android devices on mainline kernels [LWN.net]</a></li>

</ul>
</details>

**标签**: `#postmarketOS`, `#Linux mobile`, `#mainline kernel`, `#open-source smartphones`, `#mobile Linux`

---

<a id="item-17"></a>
## [CACM 评论：AI 没有让编程变简单，只是改变了难点的性质](https://cacm.acm.org/opinion/ai-didnt-make-programming-easier-it-just-made-it-differently-difficult/) ⭐️ 7.0/10

《Communications of the ACM》（CACM）发表的一篇评论文章提出，AI 编程工具并没有让编程整体上变得更简单，而是把编程的难点换了个地方——旧障碍被替代，却出现了新的、性质不同的障碍。文章明确针对“AI 让软件开发变简单”这一流行说法提出反论。 这一论点之所以重要，是因为它直接挑战了当前推动大量 AI 编程助手投资的生产力叙事，以及团队衡量开发者产出的方式。如果 AI 只是把难点转移了位置——比如从编写语法转向审查、调试和信任生成的代码——那么工具、培训和工程流程都需要重新设计，而不是单纯提速。 这是一篇观点／评论文章，而非实证研究，因此其论断基于论证与经验，而不是量化基准测试。文章聚焦软件工程实践和基于大语言模型（LLM）的开发工具；相关社区讨论托管在 Lobste.rs 上，但评论文本并未包含在素材中。

rss · Lobsters · 9月29日 09:40

**背景**: 《Communications of the ACM》是美国计算机学会（ACM）的旗舰月刊，既发表同行评审研究，也刊载从业者的观点文章。GitHub Copilot 等 AI 编程助手以及基于对话的大语言模型已在专业开发中广泛使用，厂商往往宣称带来巨大的生产力提升。本文参与的正是这场持续争论：这些提升是否真实，以及 AI 工具实际上对程序员提出了什么样的技能与判断要求。

**标签**: `#AI`, `#software engineering`, `#programming`, `#developer productivity`, `#LLM`

---

<a id="item-18"></a>
## [ESP-SDR：原始 IQ 采集让 ESP32 芯片变身低成本 SDR](https://espargos.net/espsdr/) ⭐️ 7.0/10

ESPARGOS 项目发布了 ESP-SDR，它利用乐鑫 ESP32 系列芯片中一项未公开的原始 IQ 基带采集功能，让固件绕过固定功能调制解调器，把这款微控制器当作软件定义无线电接收机使用。团队表示该功能是过去几个月借助大语言模型（LLM）发现的，并且 ESP32-C61 甚至能采到超出官方支持调谐范围的信号，最高可达 2.7 GHz。 ESP32 芯片售价仅几美元，且已广泛用于业余爱好者和嵌入式项目，因此把它改造为 SDR 接收机可能大幅降低射频实验和无线研究的成本门槛。这也暗示其他通用 Wi-Fi 或蓝牙 SoC 可能同样隐藏着厂商从未公开的原始采样能力。 该 SDR 功能被描述为低占空比，主要覆盖 2.4 GHz 频段，ESP32-C5 还支持 5 GHz；由于它依赖未公开的硬件行为而非官方 API，因此可能对芯片版本和固件变化较为敏感，宽带宽或持续性流式采集并非其预期用途。

rss · Lobsters · 9月29日 22:13

**背景**: ESP32 是乐鑫（Espressif）推出的低成本、低功耗 Wi-Fi 与蓝牙微控制器系列，广泛用于物联网和业余电子制作；其射频部分通常由固定功能的硬件调制解调器驱动，只向软件暴露处理完成的报文。而软件定义无线电（SDR）则直接暴露原始基带采样，即原始 IQ（同相/正交）数据，使调制、解调和协议解析都由软件完成，这正是 RTL-SDR、Airspy 等专用设备所提供的能力。IQ 采集就是指记录这些未经处理的采样数据，而 ESP-SDR 的技巧在于，在厂商原本无意暴露原始采样流的芯片内部把它挖了出来。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://espargos.net/espsdr/">ESPARGOS - ESP-SDR: Raw IQ Capture with Espressif's ESP32 Chips</a></li>
<li><a href="https://github.com/ESPARGOS/esp-sdr">GitHub - ESPARGOS / esp - sdr : ESP - SDR uses the undocumented raw...</a></li>

</ul>
</details>

**标签**: `#SDR`, `#ESP32`, `#embedded`, `#wireless`, `#IQ capture`

---

<a id="item-19"></a>
## [免费开源新书：从芯片到智能体的机器学习性能工程指南](https://www.reddit.com/r/MachineLearning/comments/1wt6ns4/i_wrote_a_free_opensource_book_on_making_ml/) ⭐️ 7.0/10

一位开发者发布了一本名为《How to Make Your Model Fast: A Systems View of Efficient Machine Learning, from Silicon to Agents》的免费开源书籍，源码托管在 GitHub 的 usamahz/make-your-model-fast 仓库中。全书从 roofline 分析和硬件基础讲起，逐步延伸到 kernel、编译器、量化、剪枝、视觉、端侧 LLM、机器人、性能剖析、服务化，最后落到智能体系统。 大多数机器学习优化资料只关注减少 FLOPs 之类的孤立技巧，而这本书把性能问题放在“系统瓶颈”的框架下讨论，恰好是实践者判断量化、剪枝或 kernel 优化是否值得做的关键直觉。随着端侧 LLM 与智能体负载向边缘硬件扩散，一份免费开源、贯通芯片层分析与上层智能体服务化的参考资料，正好填补了 ML 系统、推理与编译器工程师的真实需求空白。 该书的核心论点是：减少 FLOPs 并不必然让模型变快——在动手优化之前，必须先判断负载究竟是受计算、带宽、内存还是系统瓶颈限制。全书完全免费开源，作者也明确邀请从事 ML 系统、推理、编译器、边缘 AI 与性能工程的人士提供反馈和贡献。

reddit · r/MachineLearning · /u/SoloTiger_ · 9月29日 10:35

**背景**: Roofline 分析最早在 2008 年一篇针对 AMD Opteron CPU 的论文中提出，它是一种可视化性能模型：把工作负载的运算强度与硬件可达到的计算和内存带宽画在一起，从而看出某个 kernel 撞上的是哪一条“屋顶”。ML 性能工程在此基础上进一步区分“计算受限”和“内存受限”的工作，这也解释了为什么量化、剪枝、算子融合和编译优化在不同硬件上的收益差别巨大。端侧 LLM 推理——即在资源受限设备上运行通常小于 4GB 的模型——正是这些权衡最突出的应用场景之一，尤其受功耗与内存限制影响。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://nersc.gitlab.io/tools/performance/roofline/">Roofline Performance Model - NERSC Documentation</a></li>
<li><a href="https://v-chandra.github.io/on-device-llms/">On-Device LLMs: State of the Union, 2026</a></li>
<li><a href="https://grokipedia.com/page/Lightweight_open-source_LLMs_for_Android">Lightweight open-source LLMs for Android</a></li>

</ul>
</details>

**标签**: `#machine learning`, `#performance engineering`, `#systems`, `#optimization`, `#open source`

---