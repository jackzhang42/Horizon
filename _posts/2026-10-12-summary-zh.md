---
layout: default
title: "Horizon Summary: 2026-10-12 (ZH)"
date: 2026-10-12
lang: zh
---

> 从 51 条内容中筛选出 12 条重要资讯。

---

1. [Zod 4.6.6 提交被发现植入恶意代码，但未发布到 npm](#item-1) ⭐️ 8.0/10
2. [陶哲轩发布《数学 2.0》演讲幻灯片：AI 正在改写数学研究方式](#item-2) ⭐️ 8.0/10
3. [「Passkey 是陷阱」一文引发 Hacker News 激辩](#item-3) ⭐️ 8.0/10
4. [浏览器指纹正在成为新的 Cookie](#item-4) ⭐️ 7.0/10
5. [《横扫千军》被重制以适配现代电脑](#item-5) ⭐️ 7.0/10
6. [朝鲜地图绘制者：为封闭国家制图的志愿者群像](#item-6) ⭐️ 7.0/10
7. [Karpathy 称对 LLM 能力的认知鸿沟正在扩大](#item-7) ⭐️ 7.0/10
8. [Rich Hickey 主张「AI」不是工具](#item-8) ⭐️ 7.0/10
9. [Vale 的 Valen 项目提出用于内存安全的"组借用"机制](#item-9) ⭐️ 7.0/10
10. [开发者成功在 iPhone 11 上启动 Linux](#item-10) ⭐️ 7.0/10
11. [格斗游戏式回滚网络代码被引入《星际争霸：母巢之战》](#item-11) ⭐️ 7.0/10
12. [借助 React Compiler 让 React Context 变得廉价](#item-12) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [Zod 4.6.6 提交被发现植入恶意代码，但未发布到 npm](https://github.com/colinhacks/zod/commit/d821685ea6732436fcdf786a81d076958471e467) ⭐️ 8.0/10

广泛使用的 TypeScript 校验库 Zod 中一个标记为“Fix bugs and improve performance”的可疑提交（d821685）似乎注入了恶意 JavaScript，在包被安装时从一个以太坊智能合约中拉取载荷。社区分析与 GitHub 安全公告均确认，这段被污染的代码从未发布到 npm 注册表，因此使用已发布 4.6.6 版本的用户并未受到影响。 Zod 几乎是 JavaScript 与 TypeScript 生态中人尽皆知的依赖项，因此即便是未发布的供应链污染事件，也足以引发严重警觉：一旦维护者账号或 CI 流水线被攻破，单个恶意提交可能波及数百万下游项目。此事还凸显出攻击者正越来越多地利用区块链智能合约作为抗审查、难以被下线的恶意载荷分发通道。 据报道，恶意改动隐藏在 packages/mini/meta.test.mjs 等文件中，这些文件会在安装时执行，而载荷 URL 则从以太坊智能合约中获取，以规避 npm 对可疑硬编码 URL 或命令的扫描。尽管引发恐慌，该恶意更新从未推送到 npm，因此只有直接从被污染的 Git 提交（而非注册表）安装的人才会受影响。

hackernews · luggage_bazooka · 10月12日 07:47 · [社区讨论](https://news.ycombinator.com/item?id=50052814)

**背景**: Zod 是一个 TypeScript 优先的 schema 校验库，用于定义与校验数据结构，从简单字符串到深层嵌套对象均可覆盖；它每周被下载数百万次，深度存在于许多框架和工具的依赖树中。npm 生态中的供应链攻击通常通过攻破维护者账号、发布恶意版本，或借助安装时执行的生命周期脚本注入代码来实施。以太坊智能合约手法是一种较新的规避方式：由于区块链数据无法被编辑或删除，攻击者可以把恶意 URL 存于链上甚至动态轮换，而扫描工具无法简单地封禁某个固定域名。提交只是其中一步——代码仍需发布到 npm，普通用户才有可能收到。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.csoonline.com/article/4050956/malicious-npm-packages-use-ethereum-blockchain-for-malware-delivery.html">Malicious npm packages use Ethereum blockchain for malware delivery</a></li>
<li><a href="https://zod.dev/">Intro | Zod</a></li>

</ul>
</details>

**社区讨论**: 评论者大体上达成了共识：这段恶意代码从未发布到 npm，有人给出了 GitHub 安全公告链接，也有人附上 Hacker News 讨论帖以确认该更新未进入注册表。另一些人则深挖细节，指出可疑的提交信息以及会在安装时执行的 packages/mini/meta.test.mjs 文件；同时也有实际担忧被提出，即是否应视作“紧急状况（code red）”，以及该如何向客户交代。

**标签**: `#security`, `#supply-chain-attack`, `#zod`, `#javascript`, `#npm`

---

<a id="item-2"></a>
## [陶哲轩发布《数学 2.0》演讲幻灯片：AI 正在改写数学研究方式](https://teorth.github.io/tao-web/slides/math-2-0-caltech-2026.pdf) ⭐️ 8.0/10

菲尔兹奖得主陶哲轩（Terence Tao）公开了其 2026 年 10 月在加州理工学院（Caltech）所做演讲《数学 2.0》的幻灯片，他在其中提出 AI 已经终结了“证明稀缺”的时代，并勾勒出数学界应当如何围绕 AI 工具重新组织自身。他把历史上的“数学 1.0”与未来的“数学 2.0”相对照，主张后者应当淡化对开放问题的自动化求解，转而维系数学共同体以及人类数学理解的作用。 陶哲轩是当今最具影响力的数学家之一，他把 AI 定位为一次结构性冲击而不仅仅是一件工具，这一判断很可能会影响资助机构、期刊和高校院系对数学研究的看法。这场演讲还出现在一个现实争论之中：当 AI 能够批量生成证明时，一个历来以“解决了多少开放问题”来衡量进展的学科，其价值是否会遭到侵蚀。 幻灯片把开放问题比作“灯塔，而非终点”——它们是指向理论“代码库”（定义与证明体系）该往何处扩展的信号；并指出当前数学 AI 并非“好公民”，因为它只针对单个问题提示做优化，而不会贡献优雅且可复用的理论。陶哲轩还借用了医学类比：如果一款由 AI 发现的癌症疗法要注射进人体，你是否希望至少有一位人类研究者理解其作用机理？

hackernews · Anon84 · 10月11日 13:16 · [社区讨论](https://news.ycombinator.com/item?id=50043026)

**背景**: 陶哲轩是菲尔兹奖得主，也是读者最多的数学博主之一，过去几年他一直在公开追踪大语言模型与自动定理证明器在研究级数学上的表现。在他所称的“数学 1.0”传统模式中，学科进展主要靠解决著名开放问题并发表人类可读的证明来衡量；而近期能够提出或补全此类证明的 AI 系统出现后，一种新的可能性浮现出来：解法可能变得极其丰富，却鲜有人理解，也难以融入既有理论。“数学 2.0”正是他给出的应对方案：让 AI 去加固共享的理论体系，而不是去收割孤立的结果。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://terrytao.wordpress.com/2026/10/10/math-2-0/">Math 2.0 | What's new</a></li>
<li><a href="https://officechai.com/ai/terence-tao-math-2-0/">Terence Tao Says 'Math 2.0' Must Move Past Problem-Solving in ...</a></li>
<li><a href="https://community.openai.com/t/terence-tao-on-math-2-0-and-the-need-for-a-holistic-approach/1404266">Terence Tao on "Math 2.0" and the need for a holistic ...</a></li>

</ul>
</details>

**社区讨论**: 评论区对陶哲轩的医学类比提出反驳：一位从事药物研发的读者认为，人类对药物作用机制的理解本就“极其不完整”，多数临床医生也不会因为一款 AI 设计的癌症疗法机理不明而犹豫开处方；另一位则指出，连全身麻醉的机制至今都没有定论。也有人描述了各自领域的情绪冲击——研究者发现 AI 解出了自己钻研多年的问题、刚提交的经费申请不得不重写，甚至形容这像是失去一位老朋友；还有评论用软件术语转述陶哲轩的观点：数学是一套代码库，开放问题是灯塔，而当前的数学 AI 则是一个不会写出优雅代码的贡献者。

**标签**: `#AI`, `#mathematics`, `#Terence Tao`, `#machine learning`, `#research`

---

<a id="item-3"></a>
## [「Passkey 是陷阱」一文引发 Hacker News 激辩](https://nonfunctional.substack.com/p/passkeys-are-a-trap-do-not-use-them) ⭐️ 8.0/10

一篇题为《Passkey 是陷阱》（Passkeys are a trap）的批评性 Substack 文章对 passkey 认证提出质疑，并在 Hacker News 上引发大规模讨论，获得 594 分和 351 条评论。讨论并未形成简单的支持或反对结论，而是围绕 passkey 的安全性、可移植性与可用性权衡展开了一场技术含量很高的辩论。 Google、Apple、微软以及各大网络服务都在力推 passkey，视其为密码的最终替代方案，因此对其设计与锁定风险的批评几乎关系到每一位软件用户。这场讨论的重要性在于，其结果将决定认证是变得更抗钓鱼，还是仅仅把凭证控制权从用户手中转移到少数平台厂商手里。 评论者提出了具体的技术要点：agwa 指出，attestation（证明）只能在凭证注册时要求，登录时无法追溯性强制要求，而且当网站请求 attestation 时浏览器会弹出权限提示。bmitch3020 则反对说，passkey 损害了可移植性与备份能力，因为凭证被绑定到单一设备上，而且指纹解锁的强度可能弱于密码管理器中的长密码。

hackernews · laurex · 10月11日 21:59 · [社区讨论](https://news.ycombinator.com/item?id=50048312)

**背景**: Passkey 建立在 WebAuthn 之上，这是由 W3C 与 FIDO 联盟共同制定的 Web 标准，让网站用公钥密码学而非共享密钥来认证用户。一个 passkey 将认证器（如 Apple Keychain、Android、Windows Hello、硬件安全密钥或密码管理器）持有的私钥与网站保存的公钥配对，由于凭证与特定域名绑定，因此能抵御钓鱼和中间人攻击。该标准刻意没有规定私钥如何存储或同步，这正是平台厂商常常通过自家云服务同步凭证、而跨生态可移植性始终存在争议的原因。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Passkeys">Passkeys</a></li>
<li><a href="https://en.wikipedia.org/wiki/WebAuthn">WebAuthn</a></li>
<li><a href="https://en.wikipedia.org/wiki/FIDO2">FIDO2</a></li>

</ul>
</details>

**社区讨论**: 整体情绪存在分歧但颇具技术深度：alpineman 认为现实中的易用性比理论威胁更重要，并指出过于严苛的安全建议往往适得其反，因为人们最终还是会把密码写下来。也有人反驳文章本身——danpalmer 指出，该文在最后一条脚注中承认作者其实为 passkey 做了有力辩护，甚至遗漏了 passkey 依靠域名绑定来抵御中间人攻击这一重要安全特性。

**标签**: `#security`, `#authentication`, `#passkeys`, `#privacy`, `#web-standards`

---

<a id="item-4"></a>
## [浏览器指纹正在成为新的 Cookie](https://royfish.dev/fingerprints-are-the-new-cookies) ⭐️ 7.0/10

一篇论证浏览器指纹已实际取代 Cookie 成为主流网络追踪手段的博客文章在 Hacker News 上引发了大规模讨论，获得 353 个赞和 168 条评论。文章认为，由于指纹追踪不需要在客户端存储任何东西，围绕第三方 Cookie 争议而诞生的同意横幅和 Cookie 控制手段对用户几乎没有保护作用。 这之所以重要，是因为围绕 Cookie 同意构建的整套监管与浏览器厂商机制——GDPR 同意横幅、Safari 的 ITP、Chrome 一再推迟的 Cookie 淘汰计划——在很大程度上都被指纹追踪绕过了，因为即便用户清除 Cookie 或更换浏览器，指纹仍能识别设备。任何关心网络匿名性的用户，以及依赖跨站追踪的广告主和分析厂商，都会直接受到这一转变的影响。 指纹追踪的原理是把许多看似无害的微小信号——屏幕分辨率、已装字体、时区、语言、GPU/WebGL 渲染特性、音频栈行为等——组合成一个高熵标识符；浏览器 API 中的 NavigatorUAData.getHighEntropyValues() 就是典型例子，其中“熵”指某个值能揭示多少关于用户的信息。即便是普通的 HTTP 请求也会泄露浏览器、语言、操作系统和 IP 地址，因此评论者指出，伪装只能抬高可识别性的下限，而网络延迟和物理规律会让这个下限始终存在。

hackernews · royfish · 10月11日 22:33 · [社区讨论](https://news.ycombinator.com/item?id=50048642)

**背景**: 浏览器指纹是指通过浏览器收集到的、关于设备软硬件配置的信息，可被组合成一个相对稳定的标识符。与存储在浏览器中、可被删除的 Cookie 不同，指纹是服务器端根据浏览器不可避免地暴露出的特征计算得出的，因此即便清除 Cookie、使用隐私模式，甚至在同一台设备上更换浏览器，它有时仍能奏效。这使指纹可用于反欺诈，但同时也让主动规避追踪的用户仍可能被长期记录浏览历史并精准投放广告。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Browser_fingerprinting">Browser fingerprinting</a></li>
<li><a href="https://developer.mozilla.org/en-US/docs/Web/API/NavigatorUAData/getHighEntropyValues">NavigatorUAData: getHighEntropyValues() method - Web APIs - MDN</a></li>
<li><a href="https://amiunique.org/">Check if your browser has a unique fingerprint , how identifiable you...</a></li>

</ul>
</details>

**社区讨论**: 评论区总体上认同 Cookie 同意这一叙事是一种误导，有人指出无论采用何种机制，追踪与画像在法律上都需获得同意，因此指纹追踪并不能规避规则。多人力主把责任归于 JavaScript，认为纯 HTML 只暴露可伪装的 IP 和 User-Agent，而 JS 赋予网页的权力过大；获得最多认同的观点是，最高熵的 API——如音频处理、离屏 WebGL 渲染——应置于浏览器显式同意之后，或改用专门的、用户主动加入的广告定向 API。

**标签**: `#privacy`, `#web tracking`, `#fingerprinting`, `#browser security`, `#consent`

---

<a id="item-5"></a>
## [《横扫千军》被重制以适配现代电脑](https://nanolathe.gg/) ⭐️ 7.0/10

一个托管于 nanolathe.gg 的粉丝项目推出了为现代硬件重制版的经典 RTS 游戏《横扫千军》（Total Annihilation，1997 年发行），目标是在当前系统上流畅运行。此事在 Hacker News 上引发热议，获得 495 分、198 条评论，讨论中将其与其他开源 RTS 重实现项目进行了比较。 这说明即便是一款几十年前的商业 RTS，也能通过志愿者的重实现工作重获新生，同时也把关注度引向 Beyond All Reason、Spring 引擎等更广泛的开源 RTS 生态。这里探索的以性能为核心的重实现技术，也会反哺现代大规模战斗模拟。 并非所有反馈都是正面的：有评论者表示该项目的错误提示和文档极其难用，花了一小时才勉强尝试使用。该项目与一系列衍生自《横扫千军》的成果并存，包括 Spring 引擎以及基于 Recoil 分支的 Beyond All Reason。

hackernews · jttnr · 10月11日 18:04 · [社区讨论](https://news.ycombinator.com/item?id=50045984)

**背景**: 《横扫千军》是 Cavedog Entertainment 于 1997 年 9 月推出的科幻即时战略游戏，其主设计师 Chris Taylor 后来创立 Gas Powered Games 并打造了 2007 年的《最高指挥官》（Supreme Commander），后者被广泛视为其精神续作。为该游戏制作 XTA 模组的创作者们独立开发了开源 3D 游戏引擎 Spring，此后它成为众多受《横扫千军》启发项目的基础。Beyond All Reason 是一款免费开源的 RTS，构建于 Spring 引擎的分支 Recoil 之上，并从《横扫千军》和《最高指挥官》中汲取了大量灵感。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Total_Annihilation">Total Annihilation</a></li>
<li><a href="https://en.wikipedia.org/wiki/Beyond_All_Reason">Beyond All Reason</a></li>
<li><a href="https://springrts.com/">Spring RTS Engine</a></li>

</ul>
</details>

**社区讨论**: 整体情绪偏正面，评论者称赞 Beyond All Reason 是最佳精神续作，认可其打磨程度、便利功能，以及对数万单位乃至 150 人同场对战的支持。也有人将其与已有 20 年历史的 Spring 引擎作比较，质疑这个新项目有何优势；还有一位开发者介绍了自己类似的《最高指挥官》重实现，称可实现 6.4 万单位空战以 60fps 运行。少数用户提出实际顾虑，指出文档和错误提示难用，另有一人提到该网站用 01/02/03 卡片编号的排版很像 AI 生成网站的典型特征。

**标签**: `#game-development`, `#rts`, `#game-engine`, `#open-source`, `#retro-computing`

---

<a id="item-6"></a>
## [朝鲜地图绘制者：为封闭国家制图的志愿者群像](https://cartographers-nk.wonyoung.so/) ⭐️ 7.0/10

麻省理工学院的数据可视化专家 Wonyoung So 发布了《朝鲜地图绘制者》项目，汇总了 OpenStreetMap 上覆盖朝鲜的 324,415 个数据点，并为创建这些数据的志愿贡献者做了人物画像。该项目揭示了这些制图者是谁、他们为何绘制这个国家，以及每一次贡献背后的个人动机。 它把关注点从众包地图的技术产出转向了背后的人，展示了一个志愿项目如何能够为世界上最难进入的国家之一产出细致的地理知识。它也说明 OpenStreetMap 是一种几乎完全建立在无偿且常常不被认可的劳动之上的全球公共产品。 贡献量最高的单一制图者拥有 75,583 次编辑；一位名为 "P791" 的制图者表示，他有意绘制图们江沿线看起来可能成为逃亡路线的区域，重点关注朝鲜一侧和中国一侧的围栏、道路与城镇。由于实地测绘不可能进行，这些数据主要依靠描摹卫星与航拍影像而非实地采集的 GPS 轨迹构建。

hackernews · edent · 10月11日 19:46 · [社区讨论](https://news.ycombinator.com/item?id=50047091)

**背景**: OpenStreetMap 是一个由志愿者维护、以开放许可发布的全球地图数据库，由 Steve Coast 于 2004 年创建，起因是英国地形测量局未以自由许可公开其数据。贡献者通过 GPS 设备实地采集、描摹航拍与卫星影像，或导入其他自由许可的地理数据来添加内容，数据库由非营利组织 OpenStreetMap 基金会托管。朝鲜是世界上最封闭、被测绘程度最低的国家之一，因此当地几乎所有精细细节都来自对遥感影像的描摹，而非实地考察。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://cartographers-nk.wonyoung.so/">Cartographers of North Korea :: 북한의 지도 제작자</a></li>
<li><a href="https://en.wikipedia.org/wiki/OpenStreetMap">OpenStreetMap</a></li>
<li><a href="https://artsandculture.google.com/asset/cartographers-of-north-korea-cra-–-carlo-ratti-associati-scribit-wonyoung-so/KgFK2vNGROkMAQ">Cartographers of North Korea - CRA – Carlo Ratti Associati + Scribit...</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍被深深吸引，有人称 OpenStreetMap 是"我心目中的互联网七大奇迹之一"，也有人惊叹于这类项目背后无偿且不被认可的付出。最引人注目的反应集中在制图者 "P791" 身上，他坦承绘制图们江地区是为了帮助朝鲜人出逃；另有读者提到如今游客已能在朝鲜拍摄视频，也有人希望该项目能做成图文并茂的常规文章形式。

**标签**: `#OpenStreetMap`, `#North Korea`, `#cartography`, `#crowdsourcing`, `#mapping`

---

<a id="item-7"></a>
## [Karpathy 称对 LLM 能力的认知鸿沟正在扩大](https://twitter.com/karpathy/status/2109361546505966046) ⭐️ 7.0/10

Andrej Karpathy 重新翻出四月份的一条推文，指出人们对 LLM 能力的共同认知之间的鸿沟正在「扩大」，并形容这已不再是「两群人各说各话」，而更像一个「陡峭的漏斗」。该推文在 Hacker News 上引发大规模讨论（448 分、639 条评论），聚焦于究竟谁真正理解当前模型能做什么。 这场讨论触及了一个核心问题：前沿模型带来的生产力提升正被极不均衡地吸收，技术娴熟的用户远远领先于那些自以为工作太复杂、不会被自动化的普通白领。这种分化影响的不仅是 AI 实验室，还包括各行各业的招聘、再培训与竞争优势。 评论者提出了具体的反驳与限定条件：一位认为真正的分界线在于「可验证性」，因为 LLM 最适合机器能校验、或根本不需要校验的工作；另一位则指出普通企业在大举投入 agent 或自建前沿模型上仍看不到明确的 ROI。还有人提到，那些一年前只试用过一两次 ChatGPT 的非技术白领，对即将到来的变化几乎毫无概念。

hackernews · albertzeyer · 10月11日 20:20 · [社区讨论](https://news.ycombinator.com/item?id=50047422)

**背景**: Andrej Karpathy 是知名 AI 研究者与教育者、OpenAI 创始成员之一，并曾任特斯拉 AI 总监，他对 LLM 能力的评论广受关注。「验证瓶颈」指的是这样一种观点：当 AI 生成的内容变得廉价而海量时，稀缺资源就转移到了用于确认这些输出正确可信的人工或自动审查环节。Hacker News 是一个以技术为核心的讨论社区，从业者之间的这类辩论常在此长篇展开。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://x.com/karpathy">Andrej Karpathy (@karpathy) / X</a></li>
<li><a href="https://hbr.org/2026/10/ai-is-making-verification-the-bottleneck-for-companies">AI Is Making Verification the Bottleneck for Companies</a></li>
<li><a href="https://medium.com/@sohail8338/the-verification-bottleneck-how-to-scale-agentic-ai-output-4a39ee315d72">The Verification Bottleneck: How to Scale Agentic AI Output</a></li>

</ul>
</details>

**社区讨论**: 整体情绪褒贬不一：许多人认同鸿沟确实存在，尤其是那些认为自己的工作太复杂、不会被自动化的办公室职员；怀疑者则认为 Karpathy 只是泛泛而谈，真正的分界在于可验证性而非能力本身。还有人从经济角度切入，称普通企业在大举投入 AI 上并未看到回报，另有评论者把大多数用户比作欣赏闪亮珠宝、却不了解其来自火山的买主。

**标签**: `#LLM capabilities`, `#AI impact`, `#future of work`, `#Hacker News discussion`, `#AI automation`

---

<a id="item-8"></a>
## [Rich Hickey 主张「AI」不是工具](https://www.linkedin.com/pulse/ai-tool-rich-hickey-kjl8e) ⭐️ 7.0/10

Clojure 编程语言的创造者 Rich Hickey 在 LinkedIn 上发表了一篇题为《「AI」不是工具》的文章，主张把 AI 系统简单描述为「工具」这一流行做法在概念上是错误的。该文被提交到 Lobsters 并引发讨论，不过本次新闻提交本身只包含一个指向这些评论的链接。 「AI 只是工具」这一说法被广泛用来为 AI 产品的构建、宣传与治理方式辩护，因此来自一位备受尊敬的软件思想家的批判，可能会改变开发者和设计者思考 AI 系统中的能动性、责任与设计问题的方式。这也进一步卷入了业界关于大型模型是否应被视作编译器、计算器等中立工具的争论。 由于该提交仅链接到 Lobsters 的评论串，没有提供摘要或讨论文本，Hickey 的具体论证并未在条目中呈现。其价值来自 Hickey 以概念性批判著称的名声——例如他关于「简单性」和「价值之价值」的著名演讲——而非来自任何新产品或新版本发布。

rss · Lobsters · 10月12日 01:18

**背景**: Rich Hickey 是一位资深程序员，最广为人知的成就是创造了运行在 Java 虚拟机上的 Lisp 方言 Clojure，以及设计了 Datomic 数据库。在业界讨论中，AI 模型常被类比为编译器、计算器或搜索引擎之类的工具，这种说法意在强调人类仍然掌控并负有责任。而 AI 哲学领域的争论则质疑这类系统是否真正拥有目标或能动性，以及这对我们设计、部署和监管它们意味着什么。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Rich_Hickey">Rich Hickey - Wikipedia</a></li>
<li><a href="https://grokipedia.com/page/Rich_Hickey">Rich Hickey — Grokipedia</a></li>

</ul>
</details>

**标签**: `#AI`, `#philosophy of AI`, `#Rich Hickey`, `#software design`, `#commentary`

---

<a id="item-9"></a>
## [Vale 的 Valen 项目提出用于内存安全的"组借用"机制](https://verdagon.dev/blog/valen-group-borrowing) ⭐️ 7.0/10

Evan Ovadia（网名 Verdagon）在 verdagon.dev 上发表博客文章，介绍了来自 Vale/Valen 语言项目的"组借用"（group borrowing）——一种有意区别于 Rust 式借用检查的编译期内存安全机制。该文章随后被 Lobste.rs 收录，引发读者讨论。 内存安全是编程语言设计中最活跃的方向之一，而 Rust 的所有权/借用模型虽然成功，却普遍被认为学习曲线陡峭，因此任何可信的替代方案都可能影响未来系统语言处理别名与安全性的方式。如果组借用真能如描述般运作，它或许能为那些觉得 Rust 单一所有者规则过于严苛的语言和项目，提供一条限制更少的编译期安全路径。 Valen 项目自己明确表示，该语言仍处于原型阶段，"几乎才刚刚过了概念验证"，因此组借用应被视为一种研究方向，而非可直接投入生产的功能。这篇博客属于技术深度剖析，也就是说组借用的论据主要建立在设计论述之上，而非经过基准测试、已经落地的实现。

rss · Lobsters · 10月11日 12:23

**背景**: 在 C 和 C++ 这类语言中，内存安全漏洞是安全问题的首要来源之一，因此语言设计者一直在探索不依赖垃圾回收器、在编译期就能防止这类问题的方案。Rust 的借用检查器是最著名的例子：它要求每个值只有一个所有者，且引用必须遵守严格的别名规则，许多开发者觉得这种约束过于严格。组借用正是 Vale 项目在单一所有者模型之外提出的替代思路；Vale 是一门实验性系统语言，其宣称目标是同时做到快速、内存安全、易用且灵活。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/valen-lang/Valen">valen -lang/ Valen : Compiler for the Valen programming language ...</a></li>
<li><a href="https://github.com/Verdagon">Verdagon (Evan Ovadia) · GitHub</a></li>

</ul>
</details>

**标签**: `#memory-safety`, `#borrow-checking`, `#programming-languages`, `#systems-programming`, `#language-design`

---

<a id="item-10"></a>
## [开发者成功在 iPhone 11 上启动 Linux](https://www.patreon.com/partshacker/posts/linux-boots-on-172091834) ⭐️ 7.0/10

一位名为 "partshacker" 的开发者通过 Patreon 发布公告，称已成功在 iPhone 11 上启动 Linux，这意味着开源内核在苹果基于 A13 芯片的硬件上完成了 bring-up。该公告本身只是一条简短的项目进展更新，而非完整的技术文档，相关讨论发生在 Lobsters 社区。 在高度封闭的现代 iPhone 上启动 Linux 内核是一项值得关注的系统级破解里程碑，因为苹果设备是消费电子中限制最严的硬件之一，正常情况下只能运行 iOS。这类成功案例扩大了在苹果移动芯片设备上运行替代操作系统的研究积累，也可能为未来的驱动开发、引导链研究以及设备再利用与延长寿命提供参考。 该帖子内容非常简略，没有说明哪些组件可以工作——显示、触控、蜂窝基带、Wi-Fi 或电源管理支持均未提及，因此无法判断这次移植只是内核启动到控制台，还是已经具备一定可用性。iPhone 11 搭载苹果 A13 Bionic 芯片，其硬件文档未公开，意味着大多数驱动都需要逆向工程，或从 checkm8 时代的既有工作中移植。

rss · Lobsters · 10月12日 08:59

**背景**: 引导加载程序（bootloader）是设备开机后最先运行的小程序，它负责初始化 CPU、内存、存储等核心硬件，然后找到并加载操作系统内核到内存中。在 iPhone 上，这一流程被苹果的安全启动机制严格锁定，只允许经过签名的苹果软件运行，因此要启动其他系统通常需要利用 bootrom 级别的漏洞（例如旧款芯片上的 checkm8）来绕过签名校验。所以把 Linux 移植到手机上，往往意味着要为苹果从未公开文档的硬件编写或适配引导链与设备驱动。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Bootloader">Bootloader</a></li>

</ul>
</details>

**标签**: `#Linux`, `#iPhone`, `#mobile`, `#bootloader`, `#Apple`

---

<a id="item-11"></a>
## [格斗游戏式回滚网络代码被引入《星际争霸：母巢之战》](https://www.youtube.com/watch?v=vIt9xua9bLc) ⭐️ 7.0/10

一段新视频记录了在《星际争霸：母巢之战》(StarCraft: Brood War) 中实现格斗游戏式回滚网络代码(rollback netcode)的过程，目前该技术已在社区对战平台 ShieldBattery 上线。根据相关讨论，玩家如今甚至能以真正的 TR24 Low（或更低）延迟与韩国玩家对战。 自 1998 年以来，《母巢之战》的联机一直依赖确定性的帧同步(lockstep)网络模型，必须靠输入延迟来掩盖网络延迟；回滚技术几乎消除了这种可感知的延迟，有望显著改善跨区域的竞技体验。这也说明，长期被视为格斗游戏专属、被许多竞技社区称作“圣杯”的回滚技术，完全可以被移植到一款已有 28 年历史的即时战略游戏上。 回滚网络代码的原理是：先预测远端玩家的输入并在本地立即模拟，待真实输入到达后再回滚并重新模拟游戏状态——这一技术由 GGPO 推广开来。它要求游戏模拟完全确定性；视频还涉及《母巢之战》在拨号调制解调器、IPX 局域网和 Battle.net 时代的网络历史，以及 OpenBW 用于承载同一命令流的现代 ASIO 传输方式。

rss · Lobsters · 10月12日 08:27

**背景**: 网络代码(netcode)是指网络游戏在玩家之间同步游戏状态的整体方案；一旦实现不佳，玩家就会遇到卡顿、回弹或状态倒退等问题。传统格斗游戏和早期 RTS 多采用基于延迟或帧同步的模型：在推进每一帧之前，所有玩家都要等待其他人的输入，以牺牲响应性换取一致性。回滚网络代码则不同，它在点对点模型下依据预测输入在本地先行推进游戏，事后回滚纠错，从而带来几乎无延迟的手感，代价是额外的 CPU 开销和偶发的画面修正。本次新闻正是把这一思路应用到了联机基础设施可追溯至 1998 年的《母巢之战》上。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Rollback_netcode">Rollback netcode</a></li>
<li><a href="https://en.wikipedia.org/wiki/GGPO">GGPO - Wikipedia</a></li>
<li><a href="https://tl.net/forum/brood-war/646540-rollback-netcode-in-brood-war">Rollback Netcode in Brood War</a></li>

</ul>
</details>

**标签**: `#netcode`, `#game-development`, `#StarCraft`, `#rollback-netcode`, `#retro-gaming`

---

<a id="item-12"></a>
## [借助 React Compiler 让 React Context 变得廉价](https://jjenzz.com/making-react-context-cheap/) ⭐️ 7.0/10

jjenzz.com 上发布了一篇技术深度文章，讲解如何借助 React Compiler 提供的自动记忆化（memoization）能力来降低 React Context 的性能开销，而不再依赖手动编写 useMemo、useCallback 和 React.memo。文章认为，当编译器接管记忆化之后，Context 经典的重渲染代价就不再那么令人担忧。 React Context 是避免“prop drilling”（逐层透传 props）的内置方案，但一旦 context 值变化就会重渲染所有消费者组件，这一直是众所周知的性能痛点，常常迫使团队拆分多个 context，或者改用 Zustand、Jotai、Redux Toolkit 等外部状态管理库。如果 React Compiler 能让 Context 默认就变得廉价，开发者就能保留更简单、无额外依赖的状态共享方式，而不必承担惯常的重渲染成本。 React Compiler 在构建阶段自动插入记忆化逻辑，因此可以稳定那些原本会通过 context provider 触发级联重渲染的引用。需要注意的是，编译器必须能够真正分析到相关组件，这意味着违反 React 规则、或未被纳入编译构建流程的代码，仍会退回到过去那种昂贵的渲染行为。

rss · Lobsters · 10月11日 18:26

**背景**: React Context 允许组件共享数据（例如主题、语言环境或登录状态），而不必把 props 一层层穿过组件树的每一个中间层级。问题在于，当 provider 的值发生变化时，所有消费该 context 的组件都会重渲染，在大型应用中代价可观。React Compiler 是官方推出的构建期工具，会自动完成过去需要开发者手写的记忆化工作，而这篇文章探讨的正是它是如何改变使用 Context 的成本收益的。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://react.dev/learn/react-compiler">React Compiler – React</a></li>
<li><a href="https://codiga.io/blog/react-context-performance/">Improve React Context performance</a></li>
<li><a href="https://clixo.sh/blog/react-context-performance-optimization">React Context Performance Optimization: Stop Your Context from...</a></li>

</ul>
</details>

**标签**: `#React`, `#React Context`, `#React Compiler`, `#Performance`, `#Frontend`

---