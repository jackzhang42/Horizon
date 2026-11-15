---
layout: default
title: "Horizon Summary: 2026-11-15 (ZH)"
date: 2026-11-15
lang: zh
---

> 从 39 条内容中筛选出 10 条重要资讯。

---

1. [SpaceX 在第 15 次飞行中成功回收星舰，向完全可复用迈进一步](#item-1) ⭐️ 8.0/10
2. [Lovable 生成的应用因 Supabase RLS 配置薄弱泄露护照信息与逾 20 万条私信](#item-2) ⭐️ 8.0/10
3. [沃兹尼亚克如何在硬件问世前手写并手工汇编出 Apple 1 的 BASIC](#item-3) ⭐️ 7.0/10
4. [PyPI 推出全新项目页面，更清晰地展示安全与来源溯源信息](#item-4) ⭐️ 7.0/10
5. [EFF 要求上诉法院规定车牌识别数据库搜索须持搜查令](#item-5) ⭐️ 7.0/10
6. [约 200 行纯 JAX 代码从零实现 DeepSeek V3 推理](#item-6) ⭐️ 7.0/10
7. [Project Zero 实行 90 天漏洞披露，并计划缩短至 60 天和 30 天](#item-7) ⭐️ 7.0/10
8. [欧盟开源模型 EUROPA 据称目标接近 1 万亿参数](#item-8) ⭐️ 7.0/10
9. [《远程访问安全法》推进，全球 GPU 租赁与开源大模型或受冲击](#item-9) ⭐️ 7.0/10
10. [tiny-voca：450 万参数全开源 TTS 模型，CPU 上以 70 倍实时速度运行](#item-10) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [SpaceX 在第 15 次飞行中成功回收星舰，向完全可复用迈进一步](https://www.spacex.com/launches/starship-flight-15) ⭐️ 8.0/10

SpaceX 在第 15 次飞行结束时，成功用发射塔的机械臂在空中捕获了星舰，延续了以塔臂回收返回硬件、而非让其溅落海面的做法。公司通过官方 X 账号和发射直播公布了这一结果。 将飞行器完整回收而不是一次性消耗，是打造完全可复用发射系统的核心前提；每一次成功捕获，都让星舰更接近“快速复飞、单位公斤成本大幅下降”的目标，而这正是整个项目的立足点。如果这一能力与可复用的热防护盾同时成立，就有可能重塑重型载荷进入近地轨道、月球乃至火星的价格预期。 这次捕获由发射塔的机械臂完成，机械臂必须精确匹配返回飞行器的位置与速度，否则就可能损坏箭体。飞行结束后最主要的工程疑问是：热防护盾能否经受再入考验、做到检修而非整体更换，以及被捕获后的飞行器能多快完成周转并再次飞行。

hackernews · ls612 · 11月14日 21:22 · [社区讨论](https://news.ycombinator.com/item?id=50500963)

**背景**: 星舰（Starship）是 SpaceX 研制的两级完全可复用超重型运载火箭，由“超重型”助推器和星舰上面级组成，在完全可复用构型下设计运力为超过 100 吨进入近地轨道。它被定位为猎鹰 9 号和猎鹰重型火箭的后继者，在得克萨斯州的星际基地（Starbase）制造和发射。与助推器用支腿着陆、上面级则被抛弃的猎鹰 9 号不同，星舰的设计要求两级都被回收：助推器和飞船都由发射塔的机械臂在空中夹住（这套装置常被昵称为“Mechazilla”），以便接受检查、加注燃料并再次飞行。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.m.wikipedia.org/wiki/SpaceX_Starship">SpaceX Starship - Wikipedia</a></li>
<li><a href="https://www.spacex.com/vehicles/starship">Starship - SpaceX</a></li>

</ul>
</details>

**社区讨论**: 评论整体以庆祝为主，称这是“酝酿了十多年的新时代开端”；技术性最强的讨论则集中在热防护盾能否撑住、未来能否实现“助推器与飞船双捕获”并让同一批飞船反复飞行，以及最终入轨质量分数与猎鹰 9 号约 60%可复用（按成本计）的架构相比会如何。还有用户提出疑问：高频次发射产生的二氧化碳排放是否足以对气候变化造成实质影响，并表示这是常听到的说法但自己没有数据判断。

**标签**: `#spacex`, `#starship`, `#reusable-rockets`, `#aerospace`, `#spaceflight`

---

<a id="item-2"></a>
## [Lovable 生成的应用因 Supabase RLS 配置薄弱泄露护照信息与逾 20 万条私信](https://www.crissyfield.de/research/lovable-en/) ⭐️ 8.0/10

Crissy Field 的安全研究人员发布研究指出，使用 AI 应用构建工具 Lovable 结合 Supabase 搭建的应用泄露了包括护照信息和超过 20 万条私信在内的敏感数据，原因是这些应用默认未启用行级安全（Row-Level Security）。报告显示，攻击者只需在浏览器中查看网络请求即可发现这些泄露，无需任何高级黑客技术。 这揭示了快速增长的“氛围编程”（vibe coding）生态中的系统性风险：非技术用户能够发布数据库实际上默认对公网开放的应用，使 AI 生成项目成为数量庞大且易受攻击的目标。同时这也把焦点转向平台责任问题——究竟该由 Lovable、Supabase 还是终端用户为不安全默认配置负责。 当 RLS 未启用时，Supabase 的 PostgREST API 不会做任何行级过滤，而打包进前端的 anon key 本就是公开的，因此任何人调用接口都会拿到全部数据行。Lovable 安全负责人表示，每个应用在发布前都会自动扫描，并提供可选的深度 SAST 扫描，用户可点击“Fix”修复、开启后台自动修复，或在发现问题时阻止发布；Supabase 的一次讨论（supabase/supabase#4547）显示默认配置约在 10 月 30 日被修改，但已有项目可能仍沿用旧行为。

hackernews · armcat · 11月14日 17:43 · [社区讨论](https://news.ycombinator.com/item?id=50499017)

**背景**: Lovable 是一款 AI 应用构建工具，可根据自然语言提示生成包括界面、数据库和后端逻辑在内的完整应用，面向几乎没有编程经验的用户。Supabase 是基于 PostgreSQL 的热门开源后端即服务（BaaS），通过自动生成的 REST API 对外暴露数据表。行级安全（RLS）是 PostgreSQL 的一项功能，用于限制每个用户能读写哪些数据行；在 Supabase 中它默认关闭，因此未启用 RLS 的表对任何持有公开 anon key 的人都是可读的。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://supabase.com/docs/guides/api/securing-your-api">Securing your API | Supabase Docs</a></li>
<li><a href="https://amabrik.com/blog/supabase-row-level-security/">Supabase Row Level Security (RLS) Explained | Amabrik</a></li>
<li><a href="https://lovable.dev/">App & Website Builder | Build Software in Minutes | Lovable</a></li>

</ul>
</details>

**社区讨论**: 评论者大多认可这项发现，但对责任归属存在分歧：有人认为 Supabase 应负主要责任，因为其早年为了降低上手门槛而默认关闭 RLS；Lovable 安全负责人则强调其发布前扫描和一键修复机制。还有人指出这类应用无需任何黑客技能即可攻破，且数量庞大、增长迅速，并呼吁采用默认拒绝的数据库、最小权限 API 和自动化鉴权测试，让不安全部署变得难以发生。

**标签**: `#security`, `#AI-generated apps`, `#Supabase`, `#row-level security`, `#data breach`

---

<a id="item-3"></a>
## [沃兹尼亚克如何在硬件问世前手写并手工汇编出 Apple 1 的 BASIC](https://retrocomputing.stackexchange.com/questions/17957) ⭐️ 7.0/10

Retrocomputing Stack Exchange 上的一篇问答（在 Hacker News 上重新引发热议，获得 222 分和 109 条评论）解释了史蒂夫·沃兹尼亚克如何完全在纸上手写出 Apple 1 的 BASIC 解释器：他先用 6502 汇编语言书写，再自己逐条翻译成机器码操作码，等到硬件成型后才输入机器进行测试。评论者证实，这是当年买不起第二台电脑或汇编器的 8 位 hobbyist 的标准做法。 这则讨论提供了一个罕见而具体的窗口，让人看到在个人电脑还无法承载自身开发工具的时代，软件是如何被生产出来的——早期微型计算机软件实际上是在“程序员脑子里完成编译”的。它也说明汇编器和持久存储的出现如何大幅降低了写软件的门槛，而这一转变塑造了整个从爱好者群体走向产业的进程。 沃兹尼亚克的 Integer BASIC 为了简化只支持整数运算，而在 Apple II 上，其升级版被烧录进 ROM，开机即可使用。评论者指出，6502 常用的操作码只有几十个（大约 30 到 50 个），因此像 LDA 对应 $A9 这样的十六进制机器码可以被记住，这在现代 CPU 上几乎不可能。

hackernews · Skyfall106 · 11月14日 22:22 · [社区讨论](https://news.ycombinator.com/item?id=50501594)

**背景**: MOS Technology 于 1975 年 9 月推出的 6502 是一款廉价的 8 位微处理器，正是它让 Apple 1 这类爱好者电脑变得买得起。那个年代，目标机器上没有任何开发环境：汇编器（把 LDA 这类助记符转换成机器码的工具）本身都是奢侈品，所以程序员只能在纸上写程序清单（有时写在预先印好的编码表格上），再手工翻译成操作码。沃兹尼亚克以几乎并行地设计 Apple 1 的硬件和软件而闻名，这正是为什么 BASIC 解释器在整机完成之前就已经存在于纸上。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://news.ycombinator.com/item?id=50501594">How did Woz write the Apple 1 BASIC before building... | Hacker News</a></li>
<li><a href="https://en.wikipedia.org/wiki/MOS_Technology_6502">MOS Technology 6502 - Wikipedia</a></li>
<li><a href="https://www.apple2history.org/history/ah03/">3 – The Apple II – Apple II History</a></li>

</ul>
</details>

**社区讨论**: 评论者基本一致认为，在纸上手工汇编是 8 位机爱好者的默认做法，因为再买一台机器或一个汇编器都负担不起，而这种缓慢的方式迫使人深思熟虑，往往一次就能写对。不少人分享了自己在 Commodore 64 上背操作码、以及为只能在实验室里接触到的机器在纸上写代码的亲历记忆；也有用户提出了讨论中尚未解答的追问：沃兹尼亚克究竟是怎样把纸上的解释器变成 ROM 的。

**标签**: `#retrocomputing`, `#apple-1`, `#assembly`, `#6502`, `#computing-history`

---

<a id="item-4"></a>
## [PyPI 推出全新项目页面，更清晰地展示安全与来源溯源信息](https://blog.pypi.org/posts/2026-11-06-ui-updates-complete/) ⭐️ 7.0/10

PyPI 已完成新版项目页面的全面上线，现在会更醒目地展示每个发行文件的安全与来源溯源（provenance）信息。新界面让用户一眼就能看出某个分发包是否带有可验证的溯源证明，例如通过 CI/CD 流水线中的 Trusted Publishing 发布。 Python 的包索引是软件供应链最主要的攻击面之一，把溯源信号直接放到项目页面上，可以让下游用户以很低的成本判断某个版本是否真的在其声称的环境中构建。这也会推动维护者采用 Trusted Publishing 和签名证明，使 PyPI 与 npm 等注册表的同类举措保持一致。 这些信号表明某个构件是否带有与其源码仓库和构建过程绑定的溯源证明，但正如评论者指出的，它只能发现原本无害的项目在发布环节或凭据被攻破后的异常，无法识别从一开始就怀有恶意的项目。评论者还提到一些缺口，例如 Trusted Publishing 尚不支持可复用工作流（reusable workflows），以及目前真正发布溯源信息的项目仍属少数（例如 dlt 与 datasette 的对比）。

hackernews · rbanffy · 11月14日 15:40 · [社区讨论](https://news.ycombinator.com/item?id=50497892)

**背景**: 溯源证明（provenance attestation）是一种签名声明，把软件包构件与生成它的源码仓库、提交和构建系统关联起来，使使用者能够验证它确实由预期的流水线构建，而不是在某个人的笔记本上打包。Sigstore 为这类签名提供了底层工具，包括绑定 OIDC 身份的“无密钥”（keyless）短期证书，从而避免使用可能被攻击者窃取的长期私钥。PyPI 的 Trusted Publishing 允许维护者借助同样的短期凭据模型直接从 CI 服务商发布，而这次改版只是把由此产生的证明数据展示在项目页面上。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.sigstore.dev/">sign . verify . protect. Make sure your software is what it claims to be.</a></li>
<li><a href="https://nesbitt.io/2026/10/30/signing-and-attestations-across-package-registries.html">Signing and Attestations Across Package Registries | Andrew Nesbitt</a></li>
<li><a href="https://nhimg.org/glossary/npm-provenance-attestation/">What Is npm Provenance Attestation ? Definition & Examples</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论总体对 PyPI 突出溯源信息表示欢迎，但不少评论者担心这种信任模型过度依赖中心化身份和大型云 CI 服务商，会造成锁定效应，显得不够“Python 风格”。也有人强调该功能的局限——它只能发现合法项目的版本被劫持，而识别不了恶意软件包——并希望后续能支持 GitHub Actions 的可复用工作流，以及让 Sigstore 式无密钥签名在第三方 CI 服务中得到更广泛采用。

**标签**: `#PyPI`, `#supply chain security`, `#provenance`, `#Sigstore`, `#Python packaging`

---

<a id="item-5"></a>
## [EFF 要求上诉法院规定车牌识别数据库搜索须持搜查令](https://www.eff.org/deeplinks/2026/11/were-asking-appeals-court-require-warrant-alpr-searches) ⭐️ 7.0/10

电子前沿基金会（EFF）提交了一份法律意见书，敦促联邦上诉法院裁定：检索全国性的自动车牌识别（ALPR）摄像头网络属于《第四修正案》意义上的“搜查”，因此必须持有搜查令。EFF 认为，这些互联互通、持续追踪全国各地驾驶者的庞大摄像头网络，构成了不能在没有搜查令的情况下进行的大规模监控。 如果法院采纳这一主张，使用 Flock 等系统的警察及其他机构在检索历史车牌位置数据前，就必须取得搜查令或证明存在合理根据，而不能再无限制地无证查询。该案的裁决可能重塑全美执法机构使用大规模监控基础设施的方式，并为其他记录公众移动轨迹的传感器网络立下先例。 ALPR 摄像头会拍下每一辆经过的车辆，存储车牌、品牌、型号、颜色以及凹陷等特征，并附带时间戳和 GPS 位置，这些记录通常被保存数月乃至数年，并在各机构之间共享。这份意见书属于倡导性文件而非判决，因此目前尚未产生新的法律义务；而且下级法院对于“将大量零散的公共场所观察聚合为详细画像是否越过第四修正案红线”仍存在分歧。

hackernews · nobody9999 · 11月15日 02:00 · [社区讨论](https://news.ycombinator.com/item?id=50503255)

**背景**: 自动车牌识别器是安装在灯杆、巡逻车和桥梁上的人工智能摄像头，持续扫描来往车流并记录每个车牌被看到的位置，进而汇入可检索的数据库，使调查人员能够重建某辆车在一段时间内的行驶轨迹。美国《第四修正案》保护人们免受不合理的搜查与扣押，而最高法院 2018 年在“Carpenter 诉美国案”中裁定：获取长时间跨度的手机基站位置记录本身就构成需要搜查令的搜查。EFF 的论点是把这一逻辑延伸到 ALPR 数据库，认为单次扫描或许属于公开信息，但全面聚合的移动记录会暴露一个人生活中的私密细节。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Automatic_number-plate_recognition">Automatic number- plate recognition - Wikipedia</a></li>
<li><a href="https://deflock.org/">DeFlock is an open-source project that maps license plate readers ...</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍同情 EFF，有人称赞其捍卫宪法，也有人认为这是良好的第一步但应走得更远——只允许 ALPR 存储与有效搜查令相关车辆的车牌命中记录。多人以新罕布什尔州法律为范本：禁止批量采集所有车牌、禁止拍摄驾驶员和行人、要求 3 分钟内删除“未命中”图像、禁止将此类图像上传离开设备；不过也有人强调访问数据仍需搜查令。另有评论从受害者权利角度提出反驳，认为既然数据已经存在，就应用于侦破诸如乡村连环入室盗窃之类的案件；并批评“身处公共场所即放弃第四修正案保护”以及公司实体可为盈利而丢弃公民权利的观点。

**标签**: `#privacy`, `#surveillance`, `#ALPR`, `#Fourth Amendment`, `#EFF`

---

<a id="item-6"></a>
## [约 200 行纯 JAX 代码从零实现 DeepSeek V3 推理](https://github.com/Vaibhaav-Tiwari/deepseek-v3-jax) ⭐️ 7.0/10

开发者 Vaibhaav-Tiwari 在 GitHub 上发布了一个 Show HN 项目，用大约 200 行纯 JAX 代码从零重新实现了 DeepSeek V3 的推理流程。该帖子在 Hacker News 上获得 234 分和 22 条评论，读者纷纷称赞其极简、从第一性原理出发的实现方式。 紧凑、可读性强的重实现让开发者更容易理解并修改大语言模型的真实运行方式，而不是把推理当作框架里的黑盒。由于已经有人证明它能在没有 CUDA 的 AMD 硬件上跑通，这也为非 NVIDIA 用户提供了一个切实可行的本地实验起点。 有评论者表示自己在 RX 7600 XT 16GB 上端到端跑通了该项目，但需要先设置 HSA_OVERRIDE_GFX_VERSION=11.0.0 以及另一个环境变量，以绕过 JAX 的 ROCm 插件限制。ZML 团队也指出，只要把 JAX 指向他们的 PJRT Metal 插件，这份代码应该同样能在苹果硬件上运行；该仓库的定位是学习性质的产物，而非经过性能调优的推理引擎。

hackernews · VaibhaavTiwari · 11月14日 15:04 · [社区讨论](https://news.ycombinator.com/item?id=50497589)

**背景**: DeepSeek V3 是中国 AI 公司 DeepSeek 推出的开放权重大语言模型，以其混合专家（MoE）结构和无辅助损失（auxiliary-loss-free）的负载均衡策略著称。JAX 是 Google DeepMind 推出的类 NumPy 数值计算与机器学习库，它通过 XLA 编译 Python 函数，并能借助可插拔的 PJRT 后端面向非 NVIDIA 加速器。ROCm 是 AMD 面向 GPU 计算的开放软件栈，相当于 CUDA 的对应物，而 JAX 的 ROCm 插件成熟度明显较低，这正是消费级 Radeon 显卡经常需要设置环境变量覆盖的原因。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/deepseek-ai/DeepSeek-V3">GitHub - deepseek -ai/ DeepSeek - V 3 · GitHub</a></li>
<li><a href="https://rocm.docs.amd.com/en/latest/about/what-is-rocm.html">What is ROCm ? — AMD ROCm 10.1.0</a></li>
<li><a href="https://www.educative.io/answers/what-is-jax">What is JAX ?</a></li>

</ul>
</details>

**社区讨论**: 讨论整体非常正面，读者谈到从第一性原理重建模型的魅力，并表示这重新点燃了他们对 JAX 的兴趣。最有实用价值的评论来自一位在 AMD RX 7600 XT 上成功端到端运行的用户，他分享了所需的具体环境变量；ZML 团队的一位成员则指出，他们的 PJRT Metal 插件可以让这份实现扩展到苹果硬件上。还有几位经验较少的评论者希望获得学习路线图或相关技巧，使整个讨论带有很强的激励色彩。

**标签**: `#JAX`, `#DeepSeek`, `#LLM inference`, `#minimal implementations`, `#ROCm`

---

<a id="item-7"></a>
## [Project Zero 实行 90 天漏洞披露，并计划缩短至 60 天和 30 天](https://projectzero.google/2026/11/disclosure-policy.html) ⭐️ 7.0/10

Google Project Zero 宣布立即生效的“Full 90”漏洞披露政策，即在向厂商报告漏洞 90 天后公开披露；该团队计划于 2027 年 2 月 2 日缩短至 60 天，并于 2028 年 1 月 3 日缩短至 30 天。 这一路线图为整个漏洞处理生态设定了明确倒计时，迫使厂商、Android 原始设备制造商和 Linux 发行版更快修复并分发补丁；如果它们做不到，用户可能在补丁到达设备之前就得知可利用漏洞的存在。 这一变化是分阶段实施而非立即执行：目前只有 90 天窗口生效，60 天和 30 天期限分别安排在 2027 年和 2028 年，为厂商和下游维护者留出适应时间。讨论还凸显出，披露期限并不保证补丁能到达用户，尤其是在 Android 涉及多方的更新链条以及像 Ubuntu 这样需要回移植修复的发行版中。

hackernews · hacb · 11月14日 11:13 · [社区讨论](https://news.ycombinator.com/item?id=50496051)

**背景**: Google Project Zero 是一支安全研究团队，专门寻找广泛使用软件中的零日漏洞，并推动厂商在细节公开前完成修复。其披露期限属于协调漏洞披露的一种形式，即先私下通知厂商，并给予固定时间制作补丁，之后研究人员再公布技术细节。Android 基于修改过的 Linux 内核，这又增加了一层复杂性：修复需要经过 Google、芯片制造商、设备厂商和运营商，因此补丁可能早已存在，却要很久才能到达大多数手机。Ubuntu 等 Linux 发行版同样需要时间，为众多受支持版本回移植并测试修复。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.ibtimes.com/google-project-zero-security-initiative-wants-hack-planet-1628858">Google Project Zero Security Initiative Wants To Hack The... | IBTimes</a></li>
<li><a href="https://en.wikipedia.org/wiki/Android_(operating_system)">Android (operating system) - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者总体上欢迎更严格的期限，但质疑它们是否符合现实中的补丁分发情况，并指出 Android 存在长期延迟、Ubuntu 需要更多时间。有人认为 30 天仍然太慢，大科技公司应资助更快的修复；还有人抱怨高危漏洞报告已在多次固件更新中修复，却仍未获得漏洞赏金。

**标签**: `#security`, `#vulnerability-disclosure`, `#project-zero`, `#google`, `#open-source`

---

<a id="item-8"></a>
## [欧盟开源模型 EUROPA 据称目标接近 1 万亿参数](https://www.reddit.com/r/LocalLLaMA/comments/1xwr917/europa_the_eus_open_ai_model_is_aiming_for_nearly/) ⭐️ 7.0/10

r/LocalLLaMA 上的一篇帖子指出，欧盟的开源 AI 模型项目 EUROPA 据称目标定在接近 1 万亿参数。如果这一数字属实，那么这个由欧盟支持的开源模型将跻身由美国和中国主要实验室打造的最大前沿模型所在的数量级。 一个由公共资金支持、规模约 1 万亿参数的开源权重模型将成为迄今最大的开源项目之一，并为欧洲的开发者、研究者和监管者提供一个相对于美国和中国前沿模型的本土替代方案。这也表明，欧盟正把“主权 AI 能力”当作战略性基础设施来对待，而不是完全交给私营实验室。 这一说法仅来自 Reddit 上的一条纯链接帖子，没有附带任何文档，因此在模型架构（稠密还是混合专家）、训练 token 规模、算力投入、许可条款和发布时间等方面都没有细节可查。而且参数量本身只是能力的弱指标——稀疏混合专家模型往往达到数千亿乃至上万亿参数，但每个 token 只激活其中很小一部分。

reddit · r/LocalLLaMA · /u/mawcopolow · 11月15日 09:24

**背景**: 参数是神经网络内部习得的权重；参数越多通常意味着吸收知识和技能的容量越大，但训练与推理成本也高得多。所谓“开源”模型通常指开放权重：训练好的权重可以下载，但训练数据和代码未必公开，因此这种开放程度弱于完全的开源软件。要打造接近 1 万亿参数的模型，需要数万块 GPU 和数月训练时间，这也正是欧盟持续资助共享算力和多语种协作模型项目的原因，以避免完全依赖美国和中国的基础模型。

**社区讨论**: 这条帖子下几乎没有实质性讨论：它只是一条纯链接，唯一附带的评论是“One can hope”（但愿如此）。这句简短的话透露出谨慎而带期待的乐观态度，而非任何技术层面的辩论。

**标签**: `#open-source AI`, `#large language models`, `#EU AI policy`, `#foundation models`, `#AI compute`

---

<a id="item-9"></a>
## [《远程访问安全法》推进，全球 GPU 租赁与开源大模型或受冲击](https://www.reddit.com/r/LocalLLaMA/comments/1xwmnkw/rasa_will_cause_total_chaos_to_open_llms_and/) ⭐️ 7.0/10

美国众议院已于 2026 年 1 月通过 H.R.2683《远程访问安全法》（RASA），目前该法案正等待参议院表决。与此同时，美国商务部正着手敲定一项规则，禁止中国 AI 企业租用位于境外的英伟达 GPU。 现行美国出口管制明确限制向中国出售先进 AI 芯片，但对通过云端远程租用同等算力的行为覆盖不清，RASA 意在堵上这一漏洞。由于开源大模型的训练与推理常常依赖租用的云端 GPU 算力，该法案可能重塑远不止中国开发者的算力获取方式。 若正式成为法律，RASA 将扩大美国工业与安全局（BIS）依据《出口管理条例》所拥有的权限，使其能够监管外国人通过互联网或云服务对受管制物项的远程访问。该法案仍需参议院通过并由总统签署，而针对中国企业海外租用 GPU 的商务部规则则是另一项独立的行政举措。

reddit · r/LocalLLaMA · /u/ag789 · 11月15日 04:47

**背景**: 美国出口管制由商务部工业与安全局依据《出口管理条例》（EAR）执行，限制英伟达 AI GPU 等先进芯片向特定国家出货。一个广受关注的问题是，外国公司可以通过向云服务商租用同等芯片来规避这些限制，而不必直接购买。RASA 将把 BIS 的权限延伸至这种远程访问场景，而正在推进的商务部规则则把同样逻辑专门应用于在海外租用 GPU 的中国 AI 企业。开源权重的大模型开发者往往依赖这类租用算力，因此云访问规则的收紧会波及整个社区。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.iaps.ai/research/remote-access-security-act">Remote Access Security Act ( RASA ) — Institute for AI Policy and...</a></li>
<li><a href="https://abhs.in/blog/remote-access-security-act-rasa-ai-chip-export-controls-enterprise-checklist-2026">RASA Bill: Remote GPU Export Ban for US Cloud Buyers Explained</a></li>
<li><a href="https://www.lexology.com/library/detail.aspx?g=9813c777-e72d-4a77-abef-26f35253136c">What the Remote Access Security Act Means for Export... - Lexology</a></li>

</ul>
</details>

**标签**: `#AI policy`, `#export controls`, `#open LLMs`, `#GPU access`, `#Remote Access Security Act`

---

<a id="item-10"></a>
## [tiny-voca：450 万参数全开源 TTS 模型，CPU 上以 70 倍实时速度运行](https://www.reddit.com/r/LocalLLaMA/comments/1xw7zrg/tinyvoca_a_fully_open_45mparameter_tts_code/) ⭐️ 7.0/10

开发者 n4ze3m 发布了 tiny-voca：一个 450 万参数（4,537,291 个参数、约 18 MB）的英语语音合成模型，代码、权重、训练配方、数据集以及自研的音素化工具 dizione 全部公开。该模型在 4 个 CPU 线程上运行速度约为实时的 70 倍，并可通过 ONNX 直接在浏览器中运行，输出 24 kHz 音频，包含一男一女两个固定音色，完全从零训练仅需在一块 RTX 4090 上耗时 7.7 小时。 代码、权重、数据和训练配方全链条开源，加上可在 CPU 级别运行的效率，使该项目成为边缘端与端侧语音合成的可复现参考；而目前大多数高质量 TTS 系统体积庞大、依赖 GPU 且只部分开源。它还证明了用轻量级的源-滤波器合成器替代神经网络声码器，可以在极小的模型体积下实现极高的推理速度。 18 MB 这一数字涵盖了包含波形生成阶段在内的整个模型，因为音频是由一个小型源-滤波器合成器生成的，而非神经网络声码器，这也是速度提升的主要来源。作者也坦率列出了局限：仅支持英语、只有两个音色、不支持声音克隆、外文姓名和生僻拼写经常读错、音色略显机械，而且训练音频本身是由 Qwen3-TTS 生成的，因此模型质量的上限受制于该“教师”模型。

reddit · r/LocalLLaMA · /u/nato_nob · 11月14日 17:26

**背景**: 语音合成流水线通常先用音素化工具（phonemizer）把文本转成音素（一种语言中可区分意义的最小语音单位），再用神经网络预测声学特征，最后把特征转换为波形。在多数现代系统中，最后一步由神经网络声码器完成——它是第二个神经网络，往往比声学模型本身更大、更慢。源-滤波器合成是一种经典的替代方案，它把语音建模为由声源（声带振动）经滤波器（声道）塑形产生的信号，计算开销小得多；而 ONNX 是一种开放的模型导出格式，可让模型脱离 PyTorch，在各类框架乃至浏览器中运行。

**标签**: `#text-to-speech`, `#small-models`, `#open-source`, `#edge-inference`, `#onnx`

---