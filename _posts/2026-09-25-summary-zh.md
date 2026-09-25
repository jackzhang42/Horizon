---
layout: default
title: "Horizon Summary: 2026-09-25 (ZH)"
date: 2026-09-25
lang: zh
---

> 从 107 条内容中筛选出 18 条重要资讯。

---

1. [F-Droid 2.0 发布：界面大改版并淘汰特权扩展](#item-1) ⭐️ 9.0/10
2. [英国政府命令迫使苹果在英国关闭高级数据保护](#item-2) ⭐️ 9.0/10
3. [研究者在不分解模数的情况下以接近 SNFS 的时间伪造 1024 位 RSA 签名](#item-3) ⭐️ 9.0/10
4. [Whiteboard（YC W26）：面向人机协作软件设计的开源 IDE](#item-4) ⭐️ 8.0/10
5. [谷歌 Project Suncatcher 计划把 TPU 送上轨道测试](#item-5) ⭐️ 8.0/10
6. [Sourcehut 借 ansi2html 构建日志 XSS 实现账户接管](#item-6) ⭐️ 8.0/10
7. [为什么肝脏的再生能力如此奇特？](#item-7) ⭐️ 7.0/10
8. [Runway 的 WorldPrompt 实现世界模型实时可控生成](#item-8) ⭐️ 7.0/10
9. [「铸造厂」对「导航员」：AI 让科学思考变便宜，动手做仍然昂贵](#item-9) ⭐️ 7.0/10
10. [37signals 转向由 AI 智能体编写几乎全部代码](#item-10) ⭐️ 7.0/10
11. [《经济学人》：AI 常常让写作变差，即使表面看起来更好](#item-11) ⭐️ 7.0/10
12. [《经济学人》警告 AI 生成文本正在威胁人类作者身份](#item-12) ⭐️ 7.0/10
13. [博客称 Meta 的 Muse 智能体导出了 6.8 GB 文件系统数据](#item-13) ⭐️ 7.0/10
14. [跨平台侧信道攻击利用操作系统文件通知系统泄露信息](#item-14) ⭐️ 7.0/10
15. [浏览器模拟器可运行苹果未发布的 Copland D11E4](#item-15) ⭐️ 7.0/10
16. [甲骨文裁员 2.1 万人、支付 18 亿美元遣散费，实为 AI 资本开支输血](#item-16) ⭐️ 7.0/10
17. [Augment Code 在生产环境改用扩散 LLM Mercury 2.5，延迟降低 82%](#item-17) ⭐️ 7.0/10
18. [沃顿研究：AI 超大规模厂商需提升 2.7 倍生产率才能支撑 1.1 万亿美元投入](#item-18) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [F-Droid 2.0 发布：界面大改版并淘汰特权扩展](https://f-droid.org/2026/09/24/f-droid-2.0-a-new-chapter-for-android-freedom.html) ⭐️ 9.0/10

F-Droid 于 2026 年 9 月 24 日发布 2.0 版本，对这个开源 Android 应用仓库客户端进行了大规模重新设计与技术重构，客户端使用 Kotlin Compose 从零重写。该版本同时开始淘汰 F-Droid 特权扩展（FPE）——此前实现无人值守安装与更新所需的系统级组件。 F-Droid 是历史最悠久、使用最广的开源 Android 应用商店之一，而这次迟来近十年的大改版回应了长期存在的界面笨重问题——该问题此前已促使许多注重隐私的用户转向 Droid-ify 等第三方客户端。安装流程更顺畅、并淘汰配置繁琐的特权扩展，有望让 F-Droid 成为 GrapheneOS、LineageOS 等定制 ROM 用户更现实的首选。 新客户端改用 Kotlin Compose 重写，这是当前现代 Android 应用的标准工具链，官方称其为该项目十年来最大的一次更新，包含全新界面与更顺畅的应用安装体验。淘汰特权扩展则去掉了历史上需要 root 或刷入系统分区才能使用的组件，而该组件一向以配置困难、容易出问题著称。

hackernews · Lobsters · 9月24日 15:26 · [社区讨论](https://news.ycombinator.com/item?id=49831968)

**背景**: F-Droid 是一个面向 Android 的自由开源应用商店与软件仓库，功能上类似 Google Play 商店，但只收录自由开源软件；用户无需注册账号即可浏览、下载和安装应用，应用页会标注广告、用户追踪、依赖非自由软件等“反特性”。其官网还公开所托管应用的源代码以及 F-Droid 服务端软件，因此任何人都可以自建仓库。F-Droid 特权扩展是随客户端一同安装的独立系统组件，可让安装与更新在后台静默完成。Droid-ify 等第三方客户端之所以存在，正是因为许多用户对官方客户端的界面和更新流程不满意。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arstechnica.com/gadgets/2026/09/f-droid-gets-its-biggest-update-in-a-decade-with-new-ui-and-smoother-app-installs/">F-Droid gets its biggest update in a decade with new UI and smoother ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/F-Droid">F-Droid</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论非常活跃（1166 分、309 条评论），整体对此次大改版尤其是特权扩展的淘汰持支持态度，有用户表示正是因为旧版界面和特权扩展的麻烦才转用了 GrapheneOS 上的 Droid-ify。批评者则认为新设计追随了不划分区块视觉边界、不明确提示可点击与可滚动区域的潮流，另有用户抱怨 F-Droid 缺少应用评价与评分，难以区分好应用与差应用。还有评论者调侃官方截图中出现的文本换行显示故障。

**标签**: `#F-Droid`, `#Android`, `#open-source`, `#app-store`, `#privacy`

---

<a id="item-2"></a>
## [英国政府命令迫使苹果在英国关闭高级数据保护](https://macanorak.com/two-tier-encryption-in-the-uk/) ⭐️ 9.0/10

在英国 Home Office 依据《2016 年调查权力法》发出的技术能力通知（Technical Capability Notice）压力下，苹果撤下了面向英国 iCloud 用户的高级数据保护（ADP）功能，自 2025 年 2 月起英国新用户已无法启用该功能。受影响的英国账户中，iCloud 备份、照片、备忘录和 iCloud Drive 等类别已回退到由苹果持有密钥的“标准数据保护”模式。 这是已知的首个大型平台在面对政府要求时选择直接撤下端到端加密功能、而不是构建后门的案例，可能为其他政府树立先例。它同时造成了事实上的“双层加密”格局：英国用户的云端数据保护水平明显低于其他地区用户，从而削弱了人们对全球云隐私承诺的信任。 ADP 会把端到端加密的范围从默认已加密的 14 类 iCloud 数据（包括 iCloud 钥匙串和健康数据）扩展到共 23 类，因此对英国用户而言，只有新增的那 9 类数据回退到标准数据保护。即便开启 ADP，部分元数据和用量信息仍处于标准数据保护之下；此外该通知据称属于保密性质，这也限制了苹果能够公开说明的内容。

hackernews · Lobsters · 9月24日 10:39 · [社区讨论](https://news.ycombinator.com/item?id=49828731)

**背景**: 高级数据保护（ADP）是苹果推出的一项可选 iCloud 设置，用端到端加密保护大部分 iCloud 数据，使密钥仅掌握在用户自己的设备上，苹果自身也无法读取。英国《2016 年调查权力法》允许内政大臣发出“技术能力通知”，强制服务商维持或构建有助于合法调查的能力，而且这类通知可以带有保密义务。此次苹果选择了第三条路：既不削弱 ADP 的加密架构，也不退出英国市场，而是直接停止向英国用户提供该功能。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://support.apple.com/en-us/108756">How to turn on Advanced Data Protection for iCloud - Apple Support</a></li>
<li><a href="https://support.apple.com/en-us/102651">iCloud data security overview - Apple Support</a></li>
<li><a href="https://cunicula.com/en/articles/uk-apple-adp-technical-capability-notice">Apple Advanced Data Protection and the UK Technical Capability ...</a></li>
<li><a href="https://predaxia.com/glossary/technical-capability-notice/">Technical Capability Notice: UK government order under the ...</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上约 388 条评论总体持批评态度，许多人把苹果 2015 年拒绝为 FBI 开建后门与如今的“让步”作对比，也有人认为撤下 ADP 仍会使英国用户的端到端加密密钥在常见使用场景下暴露。另有评论指出，苹果实际上选择了务实的“第三条路”——不是修改安全架构，而是直接下架该功能，从而在不构建后门的前提下满足了法律要求；还有人呼吁苹果退出英国市场或停止向英国政府机构销售设备。

**标签**: `#encryption`, `#privacy`, `#UK`, `#Apple`, `#security-policy`

---

<a id="item-3"></a>
## [研究者在不分解模数的情况下以接近 SNFS 的时间伪造 1024 位 RSA 签名](https://eprint.iacr.org/2026/2131.pdf) ⭐️ 9.0/10

由 Laura Shea、Miro Haller、Adam Suhl、Nadia Heninger 和 Emmanuel Thomé 组成的研究团队实现了一个长期被忽视的 2007 年算法（Joux、Naccache 与 Thomé 提出），在完全不分解密钥的前提下伪造了 1024 位 RSA 签名，整个攻击耗费 1380 CPU 核心年、历时五个自然月，仅向签名预言机发起了 232 次查询。在预计算阶段完成之后，攻击者可以在离线状态下以约 180 核心年伪造任意选定的签名。 该研究说明，在存在签名预言机的场景下，1024 位至 4096 位 RSA 密钥的实际安全强度比基于因子分解的估算低 15 到 30 比特，即便是 4096 位 RSA 在该攻击模型下也达不到 128 位安全级别，这动摇了密钥长度推荐所依赖的核心假设。它也为在当前后量子迁移过程中彻底放弃 RSA 提供了经典（非量子）密码分析层面的证据。 攻击所针对的签名预言机是一台硬件安全模块（HSM），研究者完全通过黑盒 API 交互就实现了对该 HSM 的冒充，而没有导出其中密钥；盲 RSA 方案同样会暴露这类预言机。1380 核心年中的绝大部分属于预计算，且攻击前提是先获得暂时的预言机访问权限，因此它并非无需任何预言机的远程 RSA 破解。

rss · Lobsters · 9月24日 15:13

**背景**: 传统上认为 RSA 的安全性建立在分解公开模数的困难性之上，1024、2048、4096 比特等密钥长度是通过外推通用数域筛法（GNFS）的开销来选取的。特殊数域筛法（SNFS）是同一类算法中更快的专用变体，但只适用于具有特定代数形式的整数，而普通的 RSA 模数并不具备这种形式。2007 年由 Joux、Naccache 与 Thomé 提出的结果绕开了这一限制：只要攻击者能暂时访问原始的、无填充的 RSA 签名或解密预言机，就能构造出一种类陷门结构，在接近 SNFS 的时间内完成伪造，而完全无需分解 N。未填充的 RSA 签名、PKCS#1 v1.5 加密方案中的解密步骤，以及盲 RSA 签名协议，都会暴露这样的原始预言机。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://eprint.iacr.org/2026/2131.pdf">Forging 1024-bit RSA signatures in nearly SNFS time</a></li>
<li><a href="https://en.wikipedia.org/wiki/Special_number_field_sieve">Special number field sieve - Wikipedia</a></li>
<li><a href="https://hwbusters.com/news/rsa-signature-forgery-on-a-1024-bit-hsm-key-took-1380-core-years-and-nobody-had-to-factor-it/">RSA Signature Forgery on a 1024-Bit HSM Key Took ... - Hardware Busters</a></li>

</ul>
</details>

**标签**: `#cryptography`, `#RSA`, `#cryptanalysis`, `#digital signatures`, `#number field sieve`

---

<a id="item-4"></a>
## [Whiteboard（YC W26）：面向人机协作软件设计的开源 IDE](https://github.com/devdotfast/whiteboard) ⭐️ 8.0/10

四位工程师（Sid、Alex、Ketan 和 Milan）发布了 Whiteboard：一款以 MIT 协议开源、基于桌面端的应用，它为 AI 编码智能体提供 SDK，使其能够在应用内的画布上绘制图表、规格说明和推理轨迹，并与代码并列展示。该项目构建在 Code OSS 之上，内置用 Rust 编写的 AST 感知语义 diff 查看器及 WASM 插件系统，还提供“决策日志”，让智能体把自己的推理轨迹与图表和源码关联起来。 随着智能体编程成为常态，团队不断合并自己从未完整读过的 AI 生成 PR，创始人将由此产生的理解缺失称为“认知债务”；Whiteboard 正是针对这一缺口，把架构与规格层面的评审变成一种可视化的一等公民活动。Salesforce、Modal 等公司已经在用它评审智能体的产出，并且只把需要人类判断的变更升级为白板评审会话，这使它更像是 Greptile 等工具的补充，而非替代品。 由于构建在 Code OSS 之上，点击时序图、ER 图或智能体轨迹中的引用即可直接跳转到对应源码，并开箱即用地获得 VS Code 的快捷键与 LSP 支持。语义 diff 查看器会把新增的大型函数概括为伪代码，默认折叠单元测试和大量文档改动；桌面应用目前仅支持 macOS，且尚不能编辑文件——团队表示会通过 issue 逐步解决，同时计划推出收费的托管网页版，提供轨迹存储与多人协作评审。

hackernews · sidharthkmenon · 9月24日 17:21 · [社区讨论](https://news.ycombinator.com/item?id=49833867)

**背景**: Code OSS 是 Visual Studio Code 的开源核心，也是大多数开发者使用的编辑器，基于它构建让 Whiteboard 免费获得了完整的代码编辑器、语言服务器和快捷键支持。Claude Code（Anthropic）和 Codex（OpenAI）是能够阅读代码库、修改文件并代为执行命令的智能体编程工具，但它们的产出通常只以纯文本 diff 的形式被评审。所谓 AST 感知（语义）diff，是把代码解析成语法树后再比较，从而能按语义（例如“某个函数被重写”）而非逐行来描述改动。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://appimage.github.io/Code_OSS/">Code OSS – AppImages</a></li>
<li><a href="https://en.wikipedia.org/wiki/Claude_Code">Claude Code</a></li>
<li><a href="https://openai-codex.mintlify.app/llms.txt">openai - codex .mintlify.app/llms.txt</a></li>

</ul>
</details>

**社区讨论**: 评论整体偏正面：有人称这种边生成边绘制的“手绘风”流式图表动画将在一年内随处可见，也有人称赞 Rust 实现的语义 diff 显著提升了代码理解效率。主要争议集中在两点：一个无法编辑文件的工具是否配得上“IDE”这一称呼；以及一旦实现开始演进，图表是否会不可避免地与代码逐渐脱节。此外还有评论者指出，仅支持 macOS 这一限制应当在更显眼的位置说明。

**标签**: `#AI agents`, `#developer tools`, `#open-source`, `#software design`, `#IDE`

---

<a id="item-5"></a>
## [谷歌 Project Suncatcher 计划把 TPU 送上轨道测试](https://blog.google/innovation-and-ai/models-and-research/google-research/google-project-suncatcher-facts/) ⭐️ 8.0/10

谷歌公布了名为 Project Suncatcher 的研究项目，计划以小型卫星星座的形式把机器学习算力基础设施送入太空，卫星由太阳能供电并搭载谷歌张量处理单元（TPU）。经过多年内部研究后，该项目已排定首次在轨测试，将发射一颗原型卫星来评估 TPU 在太空环境中的表现。 如果这一设想被证明可行，轨道算力就能绕开日益制约地面 AI 数据中心的土地、电力和散热瓶颈，因此这是针对整个 AI 基础设施成本结构的一次战略押注。正如 Hacker News 上的讨论所示，它也带来了关于信号情报、在轨图像处理等军民两用军事用途的敏感问题。 谷歌在 2025 年 11 月发布的可行性研究把经济性视为核心问题：只有发射价格在 2030 年代中期降至每公斤 200 美元以下，太空算力才具备竞争力。技术难点包括 TPU 的抗辐射加固、真空环境下的散热，以及把计算结果下行传回地球时的带宽限制。

hackernews · xnx · 9月24日 13:53 · [社区讨论](https://news.ycombinator.com/item?id=49830606)

**背景**: 太空数据中心把用于 AI 训练和推理的处理与存储系统放在卫星或轨道平台上，而不是地面机房，这一概念有时被称为轨道计算。谷歌并非唯一的探索者：Starcloud 等初创公司已就其硬件和经济性发布白皮书，并已发射过一个小型验证载荷，美国审计署（GAO）也发布了关于太空数据中心的专题技术报告。其吸引力在于充足且不间断的太阳能，以及不受土地和电网限制；缺点则是发射成本、辐射、热管理和下行带宽受限。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.google/innovation-and-ai/models-and-research/google-research/google-project-suncatcher-facts/">Learn about Google ’s Project Suncatcher to put ML infrastructure in...</a></li>
<li><a href="https://research.google/blog/exploring-a-space-based-scalable-ai-infrastructure-system-design/">Exploring a space-based, scalable AI infrastructure system design</a></li>
<li><a href="https://en.wikipedia.org/wiki/Space-based_data_center">Space-based data center - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论总体偏怀疑：多位评论者认为无论在物理规律还是经济性上，太空数据中心都明显劣于地面机房，有人调侃唯一真正的好处是刚失业、爱扔燃烧瓶的公众够不着。也有人提到 Starcloud 已有的验证载荷，指出 Alphabet 持有大量 SpaceX 股份，并推测该技术与军用信号情报（SIGINT）及在轨图像处理存在重叠，还以 Glomar Explorer 和 Gorgon Stare 作为“昂贵商业项目暗藏国防目的”的先例。

**标签**: `#google`, `#space-computing`, `#ml-infrastructure`, `#data-centers`, `#satellites`

---

<a id="item-6"></a>
## [Sourcehut 借 ansi2html 构建日志 XSS 实现账户接管](https://blog.arusekk.pl/posts/srht-account-takeover/) ⭐️ 8.0/10

一位安全研究者发布了详细分析，说明 ansi2html 库（ansi2html.py）中的一个跨站脚本（XSS）漏洞如何被利用：Sourcehut 使用该库把 ANSI 转义序列渲染成 builds.sr.ht 的构建日志，攻击者因此可以把终端转义序列注入日志，并在任何查看该日志的用户浏览器中执行 JavaScript，最终实现完整的账户接管。文章指出该漏洞具有蠕虫式传播能力，任何能让文本进入构建日志的人都能触发，并被分配了 CVE-2026-92973。 攻击者几乎不需要付出任何成本——只要向开启了持续集成的公共邮件列表发送一个恶意补丁即可触发，这使得整条账户接管攻击链的门槛极低。由于被窃取的凭据包括 builds.sr.ht 存储的部署密钥（在 sr.ht 官方实例上甚至包含用于 sr.ht 自身的密钥），其影响远超单个用户账户，会波及这些密钥所保护的基础设施。 攻击链为：终端转义序列注入 → HTML 注入 → JavaScript 执行。ansi2html 在把 OSC 8 超链接等转义码转换成 HTML 链接时没有正确转义其中的 URL，因此精心构造的序列可以突破生成的标记结构。其实际教训是：在不破坏有用终端格式的前提下彻底净化任意构建输出极为困难，因为合法的构建日志本身就充满了不可信的转义序列。

hackernews · Lobsters · 9月24日 19:54 · [社区讨论](https://news.ycombinator.com/item?id=49835996)

**背景**: ANSI 转义序列是终端用于控制颜色、光标移动和超链接的不可见控制码，其中 OSC 8 用于在终端输出中生成可点击链接。Sourcehut 的 CI 服务 builds.sr.ht 会保存构建日志，并用 ansi2html 将其渲染成带颜色的 HTML 在浏览器中显示；该服务同时保存着可向用户仓库推送代码的部署密钥。跨站脚本（XSS）指把攻击者可控的脚本注入到其他用户浏览的页面中，在本例中该脚本以受害者的已认证会话运行，因此可以读取机密信息或冒用其身份执行操作。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.arusekk.pl/posts/srht-account-takeover/">SourceHut account takeover via build logs (XSS in ansi2html.py) | CVE-2026-92973 | Arusekk blog</a></li>
<li><a href="https://pypi.org/project/ansi2html/">ansi2html - PyPI</a></li>
<li><a href="https://sourcehut.org/">sourcehut - the hacker's forge</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍对漏洞触发的容易程度感到震惊——只需向开启了 CI 的邮件列表发送一个恶意补丁；也对最出人意料的后果感到意外：攻击者可以拿到全部部署密钥，包括 builds.sr.ht 为 sr.ht 自身保存的密钥。多位评论者指出，构建日志本质上就是极具风险的数据面，因为在不破坏有用格式的前提下几乎不可能净化任意构建输出，因此必须始终把输入视为不可信；也有人称赞维护者迅速修复了上游 Python 项目。

**标签**: `#security`, `#xss`, `#ci-cd`, `#vulnerability-disclosure`, `#sourcehut`

---

<a id="item-7"></a>
## [为什么肝脏的再生能力如此奇特？](https://dynomight.substack.com/p/liver) ⭐️ 7.0/10

dynomight 博客的一篇新文章探讨了为什么唯独肝脏具有如此独特的自我再生能力，文章将进化权衡的论点与执业病理学家的专业评论以及移植接受者的亲身经历结合在一起。该文在 Hacker News 上引发了大量关注，获得了 374 个赞和 195 条评论。 肝脏是人体唯一能够重新长出缺失组织质量的主要器官，这一事实使活体供体移植和劈离式肝移植成为可能，也可能为未来的再生医学提供启示。理解进化为何赋予肝脏这种能力——却没有赋予其他器官——涉及生物学与复杂系统中更为广泛的权衡问题。 肝部分切除术后的肝脏再生分为三个阶段——启动期、增殖期和终止期——主要由现有肝细胞的代偿性增生驱动，而非干细胞。关键在于，肝脏只能再生到功能性质量而非原始形状，而且驱动再生的同一批分子通路如果未被关闭，就可能转向纤维化。

hackernews · jbotz · 9月24日 16:23 · [社区讨论](https://news.ycombinator.com/item?id=49832938)

**背景**: 肝脏是人体的主要代谢中心，负责解毒、蛋白质合成、胆汁生成和能量储存。由于远古人类长期面对寄生虫、细菌和腐败食物，这个器官显然需要能够承受并恢复频繁的损伤，这或许能解释其异常的再生能力。科学家通过在动物模型中进行部分肝切除术来研究这一过程，而临床医生则利用它开展活体供体移植，将供体的肝脏劈开，让每一部分重新生长。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Liver_regeneration">Liver regeneration - Wikipedia</a></li>
<li><a href="https://www.nature.com/articles/s41575-020-0342-4">Liver regeneration: biological and pathological mechanisms and implications | Nature Reviews Gastroenterology & Hepatology</a></li>
<li><a href="https://pmc.ncbi.nlm.nih.gov/articles/PMC5749503/">The balancing act of the liver: tissue regeneration versus fibrosis - PMC</a></li>

</ul>
</details>

**社区讨论**: 一位自称病理学家的评论者推荐读者从 Robert Weinberg 的《The Biology of Cancer》入手来了解相关生物学知识。有评论者认为，大多数器官之所以不能再生，只是因为进化压力不足，并指出即便是蝾螈的再生也有局限（已知没有成年蝾螈能再生出完整的眼睛）；另一位则反驳了文章关于人类用肝脏再生换取皮肤和血液修复的说法，认为伤口愈合极其重要，绝非单纯的权衡取舍。一位患有原发性硬化性胆管炎的移植接受者分享了自己的亲身经历：他接受了劈离式肝脏（另一部分给了儿童），几个月内肝脏就重新生长起来。

**标签**: `#biology`, `#liver regeneration`, `#medicine`, `#evolutionary biology`, `#Hacker News`

---

<a id="item-8"></a>
## [Runway 的 WorldPrompt 实现世界模型实时可控生成](https://www.latent.space/p/runway) ⭐️ 7.0/10

Latent Space 的一篇技术深度报道剖析了 Runway 的 GWM Worlds 2 及其新功能 WorldPrompt：这是一个控制层，可以锁定首帧等固定元素，同时通过带时间戳的实时动作来操控角色、镜头和环境。Runway 于 2026 年 9 月公布的 GWM Worlds 2 能实时生成可交互世界，输出连续的 720p、24 fps 视频以及 48,000 Hz 音频，并根据用户输入作出响应，而不再是生成一段固定片段。 如果世界模型能够被实时操控而非提前渲染，生成式视频就会从“出片工具”转变为可交互的媒介，这对游戏原型设计、虚拟制片以及机器人和智能体仿真都意义重大。文章认为，Runway 押注 WorldPrompt 这样的控制层（而非单纯比拼生成质量），正是它与其它实时视频生成产品拉开差距的关键。 WorldPrompt 被明确定义为一种提示机制而非脚本语言：它用于设定环境、主体和视觉风格，并借助持久上下文让状态在帧与帧之间延续，同时以带时间戳的动作改变接下来的发展。需要注意的限制是，720p、24 fps 与 48 kHz 音频仍低于广播或游戏常见的帧率与规格，而且让世界模型持续实时运行依然需要大量算力。

rss · Latent Space · 9月25日 01:30

**背景**: 世界模型是一类学习环境内部表征并预测其演化的 AI 系统，使内容可以被模拟和交互，而不是提前离线渲染。早期的文生视频模型（如 Runway 的 Gen 系列）针对一个提示只生成一段固定片段；而 GWM Worlds 2 构建在 Runway 的基础音视频生成模型之上，使画面与声音能够根据输入逐帧同步合成。WorldPrompt 则是叠加在该模型之上、由用户实际操控的那一层，而实时视频生成整体上是多个实验室正在角逐的新兴方向。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.latent.space/p/runway">Runway’s WorldPrompt and the Engineering of Real-Time Worlds</a></li>
<li><a href="https://runway.com/research/introducing-gwm-worlds-2">Runway Research | Introducing GWM Worlds 2</a></li>
<li><a href="https://spatialinsiders.com/stories/runway-gwm-worlds-2-interactive-worlds">Runway’s New AI Generates Worlds as You Play | Spatial Insider</a></li>

</ul>
</details>

**标签**: `#generative AI`, `#world models`, `#real-time video`, `#Runway`, `#AI video generation`

---

<a id="item-9"></a>
## [「铸造厂」对「导航员」：AI 让科学思考变便宜，动手做仍然昂贵](https://www.latent.space/p/foundries-vs-navigators-lowering) ⭐️ 7.0/10

Latent Space 发布了一篇客座文章，提出 AI 让科学中的「思考」变得廉价，但真正「动手做」科学——运行实验、产生物理数据、验证结果——并没有变便宜。作者把这种不对称视为重塑研究型公司的核心力量，并将其归纳为两种截然不同的运营模式：所谓「铸造厂（foundries）」与「导航员（navigators）」。 如果认知（思考）变得充裕、而执行（动手做）依然稀缺，那么研究中的瓶颈与价值捕获点就会转向那些掌握昂贵物理与算力基础设施的一方，而不是点子最多的一方。这对 AI for Science 初创公司、企业实验室以及科研资助机构的资本配置与团队组织方式都有直接影响。 这篇文章属于概念性评论，而非产品发布或基准测试：它没有引用数据集或指标，也没有提供量化证据，因此其价值在于框架本身而非实证结果。「铸造厂」这一比喻借自半导体产业——少数资本密集的共享设施服务众多设计者；而「导航员」的角色更接近假设生成与实验方向选择，也就是如今 AI 可以廉价完成的那部分工作。

rss · Latent Space · 9月24日 15:03

**背景**: AI for Science 已从单纯的预测模型走向具备代理能力的系统：例如卡内基梅隆大学的 AI Science Foundry 让 AI 智能体利用高端仪器设计并编排实验，而 Owkin 的 K Navigator 则充当生物医学假设探索的智能体副驾驶。大语言模型也被直接用于科研工作流，比如用于循证文献综述的 Elicit。问题在于，这些系统加速的主要是研究中的推理与文献环节，远比湿实验室与仪器环节快，而后者的试剂、机时与验证成本依旧高昂且缓慢。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://ai-science-foundry.cmu.edu/">AI Science Foundry - Carnegie Mellon University</a></li>
<li><a href="https://www.businesswire.com/news/home/20250505282917/en/Owkin-Launches-K-Navigator-a-Ground-breaking-Agentic-Co-pilot-to-Speed-up-Breakthroughs-in-Biomedical-Research-by-20x">Owkin Launches K Navigator , a Ground-breaking Agentic Co-pilot to...</a></li>
<li><a href="https://elicit.com/">Elicit: AI for scientific research</a></li>

</ul>
</details>

**标签**: `#AI for Science`, `#Research Operations`, `#AI Economics`, `#Scientific Discovery`, `#Lab Automation`

---

<a id="item-10"></a>
## [37signals 转向由 AI 智能体编写几乎全部代码](https://newsletter.pragmaticengineer.com/p/the-pulse-end-of-coding-by-hand) ⭐️ 7.0/10

《The Pragmatic Engineer》的 Pulse 通讯报道称，Ruby on Rails 的缔造者 37signals 已转向使用 AI 智能体来生成公司几乎全部的代码。同一期内容还提到 Amazon 和 Meta 在招聘工程师方面遇到困难，并预测传统的人工代码审查可能也会消失。 37signals 是一家深受尊敬、由工程师主导的公司，其鲜明的工程实践影响了一代 Web 开发者，因此它大规模采用 AI 生成代码，为“手写代码是否正在衰落”的争论提供了有力信号。如果代码审查也随之一同淡出，主流软件团队的日常工作流程、招聘画像和技能预期都可能发生实质性变化。 这一说法的关键在于，智能体是“生成几乎全部代码”，而不仅是辅助自动补全，这意味着需求、审查和质量控制的方式都发生了重大转变。该通讯本身属于行业评论而非技术深度解析，而此前关于 AI 辅助开发的报道也指出，交付速度提升的同时可能伴随实质性的质量风险。

rss · The Pragmatic Engineer · 9月24日 16:44

**背景**: Ruby on Rails 是由 David Heinemeier Hansson 所在的 37signals 公司创建的开源 Web 框架，它推广的“约定优于配置”等理念深刻影响了现代 Web 开发。AI 编程智能体是构建在大语言模型之上的工具，能够在较少人工输入的情况下自主编写、调试和测试代码，其应用范围正从生成源代码扩展到文档编写等任务。“手写代码之死”的争论，核心在于人类工程师是否会从逐行写代码转向指挥和审查机器生成的产物。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/AI_coding_agent">AI coding agent</a></li>
<li><a href="https://www.reddit.com/r/ChatGPTCoding/comments/1nhoppq/whats_your_take_on_the_best_ai_coding_agents/">What's your take on the best AI Coding Agents? : r/ChatGPTCoding - Reddit</a></li>

</ul>
</details>

**标签**: `#AI coding agents`, `#software engineering`, `#developer productivity`, `#Ruby on Rails`, `#industry trends`

---

<a id="item-11"></a>
## [《经济学人》：AI 常常让写作变差，即使表面看起来更好](https://www.economist.com/britain/2026/09/24/ai-often-makes-writing-worse-even-if-it-makes-it-better) ⭐️ 7.0/10

《经济学人》发表文章指出，AI 常常会让写作质量下降，即便表面上看起来像是有所提升，而其背后的原因比人们常说的“破折号（em-dash）”这类文风特征要复杂得多。该消息目前只以一句简短引言的形式出现（“原因很复杂，但不是因为那个该死的破折号”），完整论证位于该刊的付费墙之后。 随着大语言模型融入记者、学生、营销人员和开发者的日常写作流程，“AI 辅助究竟是真的提升了文章质量，还是只是让它读起来更顺滑”这一问题，对所有生产或评估文本的人都至关重要。如果表面的精致掩盖了内容、个人声音或准确性的流失，那么采用 AI 写作工具的组织可能在自认为升级的同时，实际上让产出质量下降了。 该引言明确反驳了那种靠破折号之类表面标记来判断文本是否由 AI 生成的做法，暗示真正的问题另有所在——可能在于内容实质、推理、原创性或作者的语感，而非标点风格。由于目前只能看到引言部分，文章的具体论据、案例和所提出的机制无法从现有内容中得到验证。

rss · The Economist · 9月24日 13:22

**背景**: 大语言模型（LLM）是一种神经网络，通常基于 Transformer 架构，在海量文本上训练以预测和生成语言，ChatGPT、Claude、Gemini、DeepSeek 等助手都建立在它们之上。由于模型的优化目标是生成流畅、看似合理的续写内容，其输出往往读起来很顺，这反而可能掩盖事实错误、含糊表达或千篇一律的措辞。文中提到的“破折号”指的是近来网络上流行的一种做法：试图通过少数几个文风特征来判断某段文字是否由 AI 生成。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Large_language_model">Large language model - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Large_language_model_emergent_abilities">Large language model emergent abilities</a></li>
<li><a href="https://www.ibm.com/think/topics/large-language-models">What Are Large Language Models (LLMs)? - IBM</a></li>

</ul>
</details>

**标签**: `#AI writing`, `#LLM`, `#media`, `#productivity`, `#language`

---

<a id="item-12"></a>
## [《经济学人》警告 AI 生成文本正在威胁人类作者身份](https://www.economist.com/leaders/2026/09/24/dont-let-ai-kill-the-author) ⭐️ 7.0/10

《经济学人》发表了一篇题为《别让 AI 杀死作者》的社论，认为机器生成文本的泛滥正在威胁作者身份与创造性表达，并呼吁社会保护人类创作。该文的切入点是“机器制造散文的种种危害”，而非某个具体新模型的发布或技术指标的突破。 随着生成式 AI 让流畅的文章、书籍和剧本可以近乎零边际成本地批量产出，写作的经济逻辑与伦理规范正在被重塑，影响职业作家、记者、出版商以及所有在线阅读文本的人。像《经济学人》这样的主流媒体公开表态，意味着“作者身份”之争正从技术小众圈层进入文化主流视野，并可能影响版权、内容披露与署名方面的政策走向。 该条目本身只提供了标题和副标题“机器制造散文的种种危害”，因此文中的具体论点、所提对策以及引用的案例都无法从现有文本中获知。它的价值主要体现在：一家读者广泛的时事刊物把 AI 生成写作当作一个文化问题而非单纯的技术问题来对待。

rss · The Economist · 9月24日 13:22

**背景**: 生成式 AI 指能够根据用户提示按需生成看似原创的文本、图像或代码的系统，例如大语言模型；在写作领域，它们可以在几秒内起草新闻摘要、营销文案、散文乃至小说。这引发了持续不断的争议：训练数据与版权归属问题、AI 辅助作品是否应当披露或署名、以及读者能否信任可能并非出自人类之手的文字。作为历史悠久、以不署名且立场鲜明的社论著称的英国周刊，《经济学人》常在社论中呼吁具体的政策回应，因此其表态在政策与商业讨论中颇具分量。

**标签**: `#AI`, `#authorship`, `#generative AI`, `#media`, `#writing`

---

<a id="item-13"></a>
## [博客称 Meta 的 Muse 智能体导出了 6.8 GB 文件系统数据](https://mouse.dev/blog/muse-runtime-export/) ⭐️ 7.0/10

mouse.dev 上的一篇博客文章称，作者向 Meta 的个人 AI 智能体 Muse 索取其文件系统时，Muse 返回了约 6.8 GB 的导出数据，作者据此认为这暴露了沙箱或运行时隔离的失效。该内容随后出现在 Lobsters 上，被当作潜在的 AI 安全、隐私与数据外泄问题讨论，而非 Meta 官方确认的漏洞披露。 Muse 是面向消费者的智能体，Meta 宣称它能浏览网页、完成购物、生成文档并连接第三方应用，因此若真能通过普通提问拉取大量运行时文件系统数据，就意味着用户数据、凭据或内部工具可能经由对话泄露。这也凸显出个人 AI 智能体不断扩大的权限范围，正在超过用于约束它们的沙箱与输出过滤机制。 6.8 GB 比任何单次对话回复的合理体积都大出几个数量级，这意味着导出的内容可能打包了缓存用户文件、日志、模型或工具二进制等运行时产物，而不仅仅是泄露了一份文档。该说法并未得到 Meta 证实，摘要也明确指出未获得文章全文，因此目前仍无法判断这属于有意的导出功能、权限配置错误的文件访问工具，还是真正的沙箱逃逸。

rss · Lobsters · 9月24日 14:55

**背景**: Muse 是 Meta 于 2026 年 9 月推出的个人 AI 智能体，基于 Meta Superintelligence Labs 的 Muse 模型系列构建，可代表用户执行任务，并能访问浏览、文件和已连接的服务。由于智能体会执行代码并接触真实数据，它们通常被限制在 AI 沙箱中——一个隔离环境，通过限制文件系统、网络和 API 权限，防止模型触及敏感系统。与此相关的风险类别是提示注入（prompt injection），即精心构造的输入让模型执行攻击者而非开发者的指令；其中的间接注入会把指令藏在智能体阅读的网页或文档里，用来尝试外泄智能体权限范围内的任何数据。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://about.fb.com/news/2026/09/introducing-muse-personal-ai-agent/">Introducing Muse: The World's First Personal AI Agent Built for Everyone</a></li>
<li><a href="https://en.wikipedia.org/wiki/Prompt_injection">Prompt injection - Wikipedia</a></li>
<li><a href="https://blog.securelayer7.net/ai-sandbox/">AI Sandbox : Security Risks, Benefits & Best Practices</a></li>

</ul>
</details>

**标签**: `#AI security`, `#privacy`, `#Meta`, `#prompt injection`, `#data exfiltration`

---

<a id="item-14"></a>
## [跨平台侧信道攻击利用操作系统文件通知系统泄露信息](https://inoti.fyi/) ⭐️ 7.0/10

研究人员发布了一项关于“文件通知攻击”的工作，指出 Linux、Android、Windows 和 macOS 的文件通知系统存在一类侧信道泄露，并提出了一套系统化、半自动的方法来发现并利用这种泄露。研究结果显示，攻击者可以借助这些操作系统沿用数十年的通知事件，推断出文件活动，甚至包括自己并不控制的 Docker 容器内部的文件活动。 文件通知 API 是操作系统的基础原语，被备份工具、IDE、同步客户端和安全软件广泛使用，因此这里的泄露几乎可能影响所有主流消费级与服务器平台，并动摇应用之间、用户之间以及容器之间的隔离假设。作者认为这些缺陷由来已久，现有缓解措施并不充分，这意味着操作系统厂商可能需要重新设计或进一步限制通知接口。 该工作的基础是一套系统化、半自动的技术，用于发现文件通知的侧信道泄露并将其“模板化”，以便攻击者针对目标实例化利用；据报道，其覆盖面还扩展到跨 Docker 容器的文件通知。相关报道称这些缺陷已存在数十年并影响所有主流操作系统，同时指出本条新闻本身只链接到一个讨论帖，而非详细的技术文章。

rss · Lobsters · 9月25日 02:50

**背景**: 文件通知系统是内核级的接口，允许程序订阅文件被创建、修改或删除等事件，而不必反复轮询文件系统；各平台的实现方式不同（例如 Linux 和 Android 上的 inotify、Windows 上的 ReadDirectoryChangesW），并被备份工具、IDE、文件同步客户端和杀毒软件广泛使用。侧信道攻击利用的是系统无意中泄露的信息——例如时间、功耗或活动模式——而不是密码算法本身的缺陷。在这项研究中，泄露通道正是通知事件流本身：事件是否到达、到达的时机乃至事件的缺失，都可能暴露其他程序、用户或容器正在进行的操作。由于这些接口在整个系统范围内共享，它们可能跨越本应相互隔离的边界。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.theregister.com/security/2026/09/24/decades-old-file-security-flaws-found-in-android-linux-macos-and-windows/5298672">Decades-old file security flaws found in Android, Linux, macOS, and...</a></li>
<li><a href="https://inoti.fyi/pubs/file-notification-attacks.pdf">File Notification Attacks :Templating and Exploiting Side-Channel...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Side-channel_attack">Side-channel attack</a></li>

</ul>
</details>

**标签**: `#security`, `#side-channel`, `#file-notification`, `#operating-systems`, `#privacy`

---

<a id="item-15"></a>
## [浏览器模拟器可运行苹果未发布的 Copland D11E4](https://www.pagetable.com/300) ⭐️ 7.0/10

一款基于浏览器的模拟器现在可以让用户直接在网页中启动并体验苹果的 Copland D11E4 版本——这是 1996 年 6 月发布的、原本计划成为 System 8 的系统的“兼容版”（Compatibility Edition），无需在本地安装任何模拟软件。该消息由 PageTable.com 的一篇帖子发布，并链接到了相关讨论帖。 Copland 是计算机历史上最著名的被取消的操作系统项目之一，而把它最后一版可运行的构建放进浏览器，极大降低了复古计算爱好者、操作系统历史研究者和学生了解苹果“下一代 Mac OS”在崩塌前模样的门槛。这也反映出基于浏览器（借助 JavaScript/WebAssembly）的模拟趋势，正让遗留软件和未发布软件只需一个网址即可访问。 D11E4 版本（代号“Spaz”）是目前已知最新的 Copland 构建，仅在 1996 年 8 月苹果取消该项目前约两个月才分发给测试者。由于它属于未完成的测试版软件，用户应当预期到不稳定、功能缺失和子系统不完整，而不会是一个打磨完善的系统体验。

rss · Lobsters · 9月24日 19:24

**背景**: Copland 是苹果在 1994 至 1996 年间试图对老旧的经典 Mac OS 进行现代化改造的项目，目标是在保持对现有 Mac 应用兼容的同时，引入受保护内存、抢占式多任务和微内核。该项目饱受功能蔓延、管理混乱和里程碑屡屡延误之苦，最终于 1996 年 8 月被取消；苹果随后在 1997 年收购 NeXT，并最终于 2001 年推出 Mac OS X。浏览器模拟器利用 JavaScript、WebAssembly、HTML5 和 CSS3 等技术在浏览器中模拟计算机硬件，因此无需本地安装。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Apple_Copland_(operating_system)">Apple Copland (operating system)</a></li>
<li><a href="https://betawiki.net/wiki/Copland_build_D11E4">Copland build D 11 E 4 - BetaWiki</a></li>
<li><a href="https://www.pagetable.com/66">Apple Copland Reference Documentation – pagetable.com</a></li>

</ul>
</details>

**标签**: `#emulation`, `#retrocomputing`, `#Apple Copland`, `#browser`, `#operating systems`

---

<a id="item-16"></a>
## [甲骨文裁员 2.1 万人、支付 18 亿美元遣散费，实为 AI 资本开支输血](https://www.reddit.com/r/artificial/comments/1wpnhzz/oracle_cut_21000_jobs_and_paid_18b_in_severance/) ⭐️ 7.0/10

Reddit 用户 /u/Dapper-Tale-4021 的一篇分析指出，甲骨文今年裁撤 2.1 万个岗位、支付 18 亿美元遣散费，并根据 WARN 申报文件还将在 11 月 13 日再裁 800 人，这些并非 AI 自动化取代岗位的结果，而是一种为创纪录的 AI 数据中心建设腾出资金的现金流手段。该帖将这一现象归结为德意志银行分析师所称的行业普遍模式——"AI 冗余洗白"（AI redundancy washing），即公司在并无实际生产级 AI 部署的情况下，把裁员归因于 AI。 该帖挑战了当前主流叙事，即科技行业大规模裁员是 AI 自动化不可避免的结果，认为实际上员工是被裁掉以腾出资金购买 GPU 和建设数据中心。如果这一判断成立，这一重新定性对投资者、政策制定者和劳动者都意义重大，因为两种解释对公司的估值、以及对被裁员工究竟是技术进步还是资本重新配置赌注的牺牲品，含义完全不同。 该帖引用德意志银行的数据称，2026 年有 41%的裁员事件提及 AI，涉及 17.9 万名员工，而其中相当一部分公司根本拿不出生产环境的 AI 部署；帖子还引用麻省理工学院（MIT）的研究，指出 95%的生成式 AI 试点项目从未走出测试阶段。作者承认自己对这笔基础设施赌注本身是否正确并无定论，并强调"我们实现了这些职能的自动化"听起来像效率提升，而"我们裁员是为了给基础设施融资"听起来像一场赌博——因此受到质疑的不只是裁员，还有其叙事框架。该分析属于个人评论而非经核实的报道，其核心因果关系主张尚未得到甲骨文方面确认。

reddit · r/artificial · /u/Dapper-Tale-4021 · 9月25日 04:59

**背景**: 甲骨文是一家传统企业软件与云服务公司，如今在 AI 算力租赁领域与亚马逊、微软和谷歌竞争，而这块业务需要在数据中心和 GPU 上进行巨额前期资本支出（capex）。在企业财务中，资本支出通常需要与薪酬等运营支出（opex）相平衡，因此裁减人员是释放现金投入基础设施最快的途径之一。WARN 申报文件指的是美国《工人调整与再培训通知法》（WARN Act）要求提交的通知，该法律强制大型雇主在大规模裁员前提前告知；而"AI 洗白"（AI washing）是仿照"漂绿"（greenwashing）造出的说法，指企业夸大自身 AI 能力，或把 AI 当作重组裁员的方便解释。

**标签**: `#AI industry`, `#layoffs`, `#AI infrastructure`, `#cloud economics`, `#tech labor`

---

<a id="item-17"></a>
## [Augment Code 在生产环境改用扩散 LLM Mercury 2.5，延迟降低 82%](https://www.reddit.com/r/artificial/comments/1wplpto/stefano_ermon_autoregressive_inference_is/) ⭐️ 7.0/10

据一篇 Reddit 帖子称，Augment Code 在 9 月将其生产环境的编码智能体后端换成了 Inception Labs 的 Mercury 2.5——一个更小的扩散式 LLM，而非更大的自回归模型，并声称在已上线产品中实现了延迟降低 82%、成本降低 90%。Artificial Analysis 独立测得该模型速度为每秒 770 个 token，而 Inception 自己宣称的数字是每秒 1,107 个 token。 自回归解码一次只生成一个 token，且受内存带宽限制，因此 GPU 在推理循环中大部分时间处于闲置状态；而扩散模型可以并行生成一整块 token，直接针对这一瓶颈。如果这些生产环境数据站得住脚，可能会改变对延迟敏感的智能体工作负载的成本与延迟经济学，并推动更多厂商转向非自回归的文本架构。 独立测得的每秒 770 个 token 明显低于 Inception 宣称的每秒 1,107 个 token，不过两个数字都远高于常见的自回归推理速度；帖子还指出，扩散模型的采样器设置以及在 vLLM 等推理栈中的服务支持仍在快速演进。值得注意的是，这篇 Reddit 帖子把技术评论与商业提案混在一起——它提议做一个开放的、同一硬件条件下的基准测试，让开放权重的 DiffusionGemma 与 Gemma 4 26B-A4B 在租用的 H100 上对比（约每小时 3.41 美元/GPU），并以每月 417 美元的 Optima 席位和基准测试初创公司 Vals 获得的 4000 万美元融资作为周边商业热度的佐证。

reddit · r/artificial · /u/cen6wkf · 9月25日 03:23

**背景**: 自回归语言模型一次只生成一个 token，每一步解码都需要一次完整的前向传播，把模型权重从内存中读取一遍，这使得推理受内存带宽限制，GPU 利用率偏低。扩散语言模型则从噪声出发，并行地对一整块 token 反复去噪，天然更契合 GPU 的并行结构；由于文本是离散的而非连续的，这类模型需要离散扩散或掩码扩散等特殊改造，而不能直接套用标准的高斯噪声。Inception Labs 的 Mercury 2.5 被称为迄今训练过的能力最强、规模最大的扩散语言模型，而 Artificial Analysis 是一家独立基准测试机构，其测量数据甚至常被模型厂商自己引用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.inceptionlabs.ai/blog/introducing-mercury-2-5">Introducing Mercury 2 . 5 – Inception</a></li>
<li><a href="https://artificialanalysis.ai/leaderboards/models">LLM Leaderboard - Comparison of AI models from... | Artificial Analysis</a></li>
<li><a href="https://arxiv.org/abs/2505.15045">Diffusion vs. Autoregressive Language Models: A Text ... - arXiv</a></li>

</ul>
</details>

**标签**: `#AI/ML`, `#Diffusion Models`, `#LLM Inference`, `#GPU Optimization`, `#Production Deployment`

---

<a id="item-18"></a>
## [沃顿研究：AI 超大规模厂商需提升 2.7 倍生产率才能支撑 1.1 万亿美元投入](https://www.reddit.com/r/artificial/comments/1wowoyc/ai_hyperscalers_may_need_to_raise_productivity_27/) ⭐️ 7.0/10

沃顿商学院金融学教授 Jessica Wachter 与其合著者 Jonathan Wachter 的新研究估算，Alphabet、微软、亚马逊、Meta 和 Oracle 需要在 2030 年前将生产率提升 2.7 倍，才能证明到 2027 年约 1.1 万亿美元 AI 基础设施支出是合理的。论文警告称，如果预期的 AI 繁荣未能兑现，这轮建设可能成为“历史上规模最大的资本错配”。 超大规模厂商的 AI 资本支出目前是美国股市估值和 GDP 增长最重要的驱动力之一，因此这项分析为看多 AI 的叙事提供了一个具体的财务层面反证。如果生产率的回报未能如期兑现，投资者、云服务商乃至整体经济都可能承受大规模资产减值和 AI 相关资产的重估。 2.7 倍的生产率数字是在计入资本成本、折旧以及 15% 的预期回报率之后得出的，并且仅基于这五家公司的支出来计算，而非整个科技行业。因此结论对 15% 这一回报门槛，以及 AI 能力转化为可衡量产出增益的速度假设都高度敏感。

reddit · r/artificial · /u/Post-reality · 9月24日 09:07

**背景**: 超大规模厂商（hyperscaler）指 Alphabet、微软、亚马逊、Meta、Oracle 这类大规模云与数据中心运营商，它们建设并运营着远超传统本地数据中心的庞大软硬件基础设施，也是当前 AI 加速器的主要买家。“资本错配”是经济学用语，指资金流向回报低于资本成本的项目，从而拖累整体生产率。对这些公司而言，证明支出合理意味着获得的回报要高于折旧与融资成本，这正是论文设定明确 15% 门槛回报率的原因。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Hyperscale_computing">Hyperscale computing - Wikipedia</a></li>
<li><a href="https://www.denodo.com/en/glossary/hyperscalers-definition-importance-key-providers">Hyperscalers : Definition , Importance, and Key Providers | Denodo</a></li>

</ul>
</details>

**标签**: `#AI economics`, `#AI infrastructure`, `#hyperscalers`, `#productivity`, `#capital allocation`

---