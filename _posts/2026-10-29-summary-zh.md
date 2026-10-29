---
layout: default
title: "Horizon Summary: 2026-10-29 (ZH)"
date: 2026-10-29
lang: zh
---

> 从 82 条内容中筛选出 20 条重要资讯。

---

1. [谷歌发布 Gemini 4 Carbon，主打网络安全的前沿模型](#item-1) ⭐️ 9.0/10
2. [Orange Tsai 仅用逻辑漏洞打造 Edge 完整攻击链](#item-2) ⭐️ 9.0/10
3. [反 LLM 指纹脚本意外触发大模型生物武器安全过滤](#item-3) ⭐️ 8.0/10
4. [Claude Code 被曝静默将每个后台智能体的完整对话记录发送给模型](#item-4) ⭐️ 8.0/10
5. [苹果发布带触控屏与 PROLED XDR OLED 显示屏的 MacBook Pro](#item-5) ⭐️ 8.0/10
6. [苹果自带的 git 与 curl 仍信任已被攻破的 eMudhra 证书](#item-6) ⭐️ 8.0/10
7. [一条畸形 WAP Push 短信即可让 Android 电话进程崩溃并中断通话](#item-7) ⭐️ 8.0/10
8. [Linux 内核模块解除 RTX 3090 张量核心限速，ComfyUI 出图快 55%](#item-8) ⭐️ 8.0/10
9. [Qwenputer：在 Qwen3.5 内部运行的确定性 RISC-V CPU](#item-9) ⭐️ 7.0/10
10. [Stack Overflow 每月提问量已跌破 1000 条](#item-10) ⭐️ 7.0/10
11. [Alpine Linux 披露针对 GitLab 的 Ruby 正则漏洞利用尝试](#item-11) ⭐️ 7.0/10
12. [Surge AI 发布 DAYJOB: Tax 基准：最强 AI 代理仅通过 10.8% 的真实税务任务](#item-12) ⭐️ 7.0/10
13. [Simon Willison：2026 年 10 月是“氛围编程”游戏的分水岭](#item-13) ⭐️ 7.0/10
14. [Supabase 将自身定位为 AI 智能体的后端基础设施](#item-14) ⭐️ 7.0/10
15. [Nathan Lambert 探讨 AI 基准测试与“基准测试者困境”](#item-15) ⭐️ 7.0/10
16. [《经济学人》刊文：AI 是荷马史诗的技术版本](#item-16) ⭐️ 7.0/10
17. [Yoshua Wuyts 指出 Rust 的 Future trait 缺少一个状态](#item-17) ⭐️ 7.0/10
18. [Daniel Lemire 展示 C++ 中每秒十亿次查询的查找表](#item-18) ⭐️ 7.0/10
19. [HP 论文称 ACL 无法处理多主体交互，助长点击劫持与 CSRF](#item-19) ⭐️ 7.0/10
20. [SpEdE：开源 ComfyUI 工具包支持点击编辑高斯泼溅场景](#item-20) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [谷歌发布 Gemini 4 Carbon，主打网络安全的前沿模型](https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-4-carbon/) ⭐️ 9.0/10

谷歌发布了 Gemini 4 Carbon，称其是面向网络安全和长周期智能体任务的最强模型，并表示其在独立评测中处于领先地位。该模型目前仅向经过审核的“可信防御方”开放，尚未向所有用户普遍提供。 此次发布把谷歌的前沿模型推向安全敏感领域，强大的攻防网络能力带来双重用途风险，也使受限访问成为合理选择。同时，这也加剧了顶级实验室在智能体能力、基准测试领先地位和企业级安全保障上的竞争。 据报道，Gemini 4 Carbon 沿用了此前 Argon 模型的多层安全与防护体系，融合了训练阶段的安全措施、实时滥用防御以及抗提示注入能力。第三方追踪网站显示其高配版本价格约为每百万输入 token 4 美元、每百万输出 token 20 美元，但公开可用的时间仍不明确。

hackernews · acossta · 10月28日 17:01 · [社区讨论](https://news.ycombinator.com/item?id=50276792)

**背景**: Gemini 是谷歌 DeepMind 推出的多模态大语言模型系列，谷歌通常按 Ultra、Pro、Flash、Lite 等能力层级发布，并常使用 Argon 之类的内部代号。各大实验室一般会在发布时公布基准测试表格，而具备潜在危险网络能力的模型往往会先开放给一小批可信测试者，再全面上线。独立排行榜和第三方评测机构会汇总厂商公布的这些分数，因此模型何时真正向公众开放显得尤为关键。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-4-carbon/">Introducing Gemini 4 Carbon</a></li>
<li><a href="https://artificialanalysis.ai/models/gemini-4-carbon">Gemini 4 Carbon (high) - Intelligence, Performance... | Artificial Analysis</a></li>
<li><a href="https://theresanaiforthat.com/model/gemini-4-carbon/">Gemini 4 Carbon | AI Model | There's An AI For That</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的评论者普遍持怀疑态度：许多人抱怨 Gemini 的代号和层级（Argon、Carbon、“3.8 Pro”、Ultra）让人几乎无法判断自己实际使用的是哪个模型，也不知道如何升级。另一些人认为，在如此快速变化的领域里，公布基准分数却不开放模型毫无意义，并指出此前的 Argon 模型在正式上线前很久就已公布。

**标签**: `#Gemini`, `#Google`, `#LLM`, `#AI models`, `#Hacker News`

---

<a id="item-2"></a>
## [Orange Tsai 仅用逻辑漏洞打造 Edge 完整攻击链](https://blog.orange.tw/posts/2026-10-the-last-proof-of-human-craft-browser-full-chain/) ⭐️ 9.0/10

2026 年 10 月 28 日，DEVCORE 的 Orange Tsai 公开了一条完整攻击链的技术细节：无需任何内存破坏漏洞，仅凭逻辑缺陷就能把恶意网页变成在 Microsoft Edge 沙箱之外执行的 Windows 代码。该攻击链最早于五个月前的 Pwn2Own Berlin 上演示，赢得 17.5 万美元奖金，微软随后已修复相关漏洞。 这项研究表明，多年来在内存安全加固、沙箱隔离和模糊测试上的投入，依然挡不住以“非预期方式”滥用合法浏览器特性的攻击者，这对所有浏览器厂商和企业防御方都是一个严肃信号。逻辑漏洞无法靠让程序崩溃来发现，只能通过阅读代码、理解语义来推理，因此极难自动化挖掘，却同样能构成完整攻击链并实现完全控制。 据已公开的报道，这条攻击链把大约四到五个逻辑漏洞与两个 Windows 特性结合起来突破沙箱，用户除了访问一个精心构造的页面之外无需任何交互。Tsai 特意等到微软发布修复补丁之后才公开细节，因此此次披露侧重于方法论，而非仍在利用中的零日漏洞。

rss · Lobsters · 10月28日 13:34

**背景**: 现代浏览器被拆分为负责解析不可信网页内容的沙箱化渲染进程，以及权限更高的代理进程；攻击者即便攻陷渲染进程，还必须再找到一个漏洞来逃逸沙箱、触达操作系统。因此经典的浏览器攻击链通常由释放后重用（use-after-free）等内存破坏漏洞构成，而厂商用 ASLR、CFG、堆隔离等缓解措施来削弱这类攻击。逻辑漏洞则不同：它滥用的是“按设计正常工作”的功能，只是这些功能隐含了错误的安全假设，所以内存安全缓解措施和模糊测试基本抓不到它。Pwn2Own 是最知名的漏洞利用竞赛，研究者会在全补丁浏览器上演示此类完整攻击链以赢取奖金。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://thehackernews.com/2026/10/researcher-reveals-how-logic-bugs-alone.html">Researcher Reveals How Logic Bugs Alone Cracked Microsoft ...</a></li>
<li><a href="https://cybersecuritynews.com/microsoft-edge-zero-click-exploit/">Microsoft Edge 0-Click Exploit Chains Five Flaws to Execute ...</a></li>
<li><a href="https://www.darknavy.org/blog/patch_in_exploit_out_how_deepsec_reconstructed_the_pwn2own_microsoft_edge_sandbox_escape/">Patch In, Exploit Out: How deepsec Reconstructed... | DARKNAVY Blog</a></li>

</ul>
</details>

**标签**: `#browser security`, `#Microsoft Edge`, `#exploit chain`, `#logic bugs`, `#vulnerability research`

---

<a id="item-3"></a>
## [反 LLM 指纹脚本意外触发大模型生物武器安全过滤](https://nullpt.rs/fingerprinting-bioweapons) ⭐️ 8.0/10

nullpt.rs 上的一篇分析文章追踪了一个由 servicepipe.tech 部署的网页指纹脚本：该脚本内嵌了大量混淆的、故意制造刺激性的载荷，其中包含伪造的生物武器合成说明和政治雷区，结果让大模型的安全分类器把这段本身无害的反爬虫代码判定为生物武器相关内容。作者是在抓取约一万个网站时发现该脚本的，文章在 Hacker News 上获得超过 1200 分和 230 条评论。 这一事件表明，反爬虫混淆技术与 AI 爬虫之间的猫鼠游戏如今已经延伸到大模型的安全层，导致无害代码可能被服务商的安全护栏隔离或拒答。它凸显了安全分类器的误报如何打断合法的自动化分析流程，也引发了关于网络究竟能承受多少由混淆带来的摩擦的更大讨论。 这些载荷是作者所称“反 LLM”混淆的早期形态：它们被设计成看似违禁内容，诱导 AI 助手拒绝解混淆，从而阻止自动化抓取和分析。该手法只是概率性的，并不保证奏效；评论者指出，同样的提示词在 GLM 等部分模型上能够被顺利执行，而一线商业 API 则会直接拦截。

hackernews · Lobsters · 10月28日 17:13 · [社区讨论](https://news.ycombinator.com/item?id=50276998)

**背景**: 网页指纹脚本会收集浏览器与设备信号，帮助网站区分真人和爬虫，因此通常经过重度混淆以抵抗逆向分析。随着 AI 智能体越来越多地代替用户阅读并解混淆页面 JavaScript，网站运营方开始加入专门针对大模型的、类似提示注入的雷区。与此同时，模型服务商会运行安全分类器，扫描输入输出中是否包含大规模杀伤性武器等类别，并拒绝匹配的请求。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://sitem.co/public/summary/5732/why-is-this-fingerprinting-script-creating-bioweapons">Why Is This Fingerprinting Script Creating Bioweapons? - SiteM</a></li>
<li><a href="https://docs.apify.com/academy/anti-scraping/techniques/fingerprinting">Fingerprinting | Academy | Apify Documentation</a></li>
<li><a href="https://en.wikipedia.org/wiki/Prompt_injection">Prompt injection - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者对此十分着迷，称其为一场“分形”式的军备竞赛，混淆方实际上是在针对大模型爬虫进行训练。多位评论者分享了类似经历：有人描述文档因遗留水印而被静默隔离，还有人指出某 Hacker News 用户主页也包含反 LLM 咒语；另一些人则指出 GLM 等开放模型乐于分析一线 API 拒绝处理的攻击载荷，从而引发了对过滤能力差异的质疑。

**标签**: `#LLM safety filters`, `#web fingerprinting`, `#obfuscation`, `#AI crawlers`, `#prompt injection`

---

<a id="item-4"></a>
## [Claude Code 被曝静默将每个后台智能体的完整对话记录发送给模型](https://gist.github.com/flamerix-ai/c3905705cc4205e5de3011fa2e74efce) ⭐️ 8.0/10

开发者 flamerix-ai 发布的一份公开 gist 分析了 Claude Code 的行为，指出该工具会定期把每个后台智能体的完整对话记录发送回模型进行摘要，从而产生用户从未主动请求的额外模型调用。这些摘要与状态标签请求不会出现在用户可见的会话记录中，却会消耗与正常工作相同的 token 配额。 Claude Code 是目前使用最广泛的 AI 编程智能体之一，这种隐性且持续发生的 token 开销会影响大量按额度计费的开发者，并削弱用户对用量统计透明度的信任。它同时引发了关于对话记录内容为何、以及如何离开本机的隐私与透明度质疑，也让人们开始审视模型厂商自建客户端工具背后的动机。 由于这些请求本身不出现在对话记录中，gist 作者与评论者是根据约 30 秒一次的摘要节奏反推出这些额外调用的；一位用户估算隐藏的状态标签调用约占其每周约 1970 美元 API 等价开销中的 380 美元，即真实总量的 16%。讨论中也有人提出反驳：如果每次都重发完整记录，其中大部分 token 应属于提示缓存命中，实际成本会比表面数字低得多。

hackernews · NikZaal · 10月29日 03:33 · [社区讨论](https://news.ycombinator.com/item?id=50284255)

**背景**: Claude Code 是 Anthropic 推出的终端内 AI 编程智能体，其后台智能体功能（约在 v2.0.60 引入）允许开发者把子任务分派给子智能体在后台运行，同时在前台继续其他工作，完成后回报结果。由于这类智能体运行时间长且无人值守，客户端会定期压缩其对话记录，以便父会话展示简短状态，这就需要额外的模型调用。这些调用与普通提示共享同一用量限额，而提示缓存机制——重复的上下文前缀按更低价格计费——决定了这种重发记录的实际成本高低。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://claudelog.com/faqs/what-are-background-agents/">What are Background Agents in Claude Code | ClaudeLog</a></li>
<li><a href="https://vsits.co/invisible-tax/">The Invisible Tax: Hidden Quota Burns and Phantom Rate Limits in...</a></li>

</ul>
</details>

**社区讨论**: 该讨论（358 分、116 条评论）整体持怀疑态度：一位评论者量化出隐藏开销约占其 Max 套餐每周支出的 16%，另一位则认为重复发送完整记录大部分应命中缓存、成本并不高，还有人质疑模型厂商为何要提供这种无谓消耗 token 的客户端工具。用户还分享了应对办法，尤其是一个可以移除 Anthropic 写入系统提示中的账号邮箱的插件，同时有人表示近日的配额消耗似乎已明显下降。

**标签**: `#Claude Code`, `#AI coding agents`, `#token usage`, `#privacy`, `#developer tools`

---

<a id="item-5"></a>
## [苹果发布带触控屏与 PROLED XDR OLED 显示屏的 MacBook Pro](https://www.apple.com/macbook-pro/proled-xdr-display/) ⭐️ 8.0/10

苹果发布了新款 MacBook Pro（2026 年 10 月），首次在 Mac 笔记本上引入触控屏，并搭载全新的“PROLED XDR”显示屏，这也是 Mac 产品线首次采用 OLED 面板技术。14 英寸机型重量从 3.5 磅（1.59 千克）降至 3.0 磅（1.36 千克），16 英寸从 4.7 磅（2.13 千克）降至 4.0 磅（1.81 千克），约减轻 15%，机身厚度也减少了近 1 毫米。 在 Mac 上加入触控，打破了数十年来“仅限鼠标与键盘”的设计前提，这意味着 macOS 的界面规范以及所有第三方 Mac 应用的点击区域与手势交互都需要重新考量。转向 OLED 也标志着 Mac 产品线 LCD 背光时代的终结，同时让苹果的笔记本设计方向成为开发者和专业用户关注的焦点。 “PROLED XDR”是苹果为双层串联 OLED（tandem OLED）面板起的营销名称，其底层技术与 iPad Pro 上名为“Ultra Retina XDR”的屏幕相同；它采用自发光的像素、无需背光且层数更少，这正是重量大幅下降的主要原因。据报道，macOS 并未为触控从零重构，而是在原有基础上做了适配，批评者指出现有的 macOS 控件在物理尺寸上太小，用手指难以准确点按。

hackernews · etothet · 10月28日 17:10 · [社区讨论](https://news.ycombinator.com/item?id=50276940)

**背景**: OLED（有机发光二极管）显示屏与 LCD 的区别在于每个像素自行发光，而不依赖单独的背光源，因此能实现更深的黑色、更薄的面板与更轻的整机结构；“双层串联 OLED”（tandem OLED）通过叠加两层发光层来提升亮度和使用寿命。苹果长期拒绝在 Mac 上加入触控，将 iPad 定位为触控计算设备，并让 macOS 明确围绕指针输入来设计，而 Windows 笔记本提供触控屏已有约十年时间。此次命名值得关注，是因为苹果此前曾在 mini-LED 与 Pro Display 显示器上使用“XDR”（极致动态范围）这一名称，因此“PROLED XDR”是 OLED 时代的新标签，而非旧有 mini-LED 面板的延续。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.apple.com/macbook-pro/proled-xdr-display/pdf/PROLED_XDR_Display_Technical_Paper.pdf">PROLED XDR DISPLAY Technology Overview</a></li>
<li><a href="https://www.techradar.com/computing/macbooks/whats-the-tech-inside-the-touchscreen-macbook-pros-proled-xdr-screen-heres-why-the-tandem-oled-panel-is-important">What's the tech inside the touchscreen MacBook Pro 's ' PROLED XDR ....</a></li>
<li><a href="https://gizmodo.com/macos-touchscreen-macbook-pro-2000831715">Thank God, Touchscreen macOS Isn't Remotely Close to Windows 8</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的评论分歧明显：一位高赞用户认为触控 Mac 对 Mac 爱好者而言是糟糕的发展，因为面向用户的触控支持会带来大量界面缺陷反馈——控件对于手指来说太小；另一位用户则更赞赏取消 LCD 背光所带来的约 15% 减重。也有人质疑在笔记本上是否真有人需要触控，毕竟鼠标更精准、屏幕还会留下指纹；还有评论者认为，与当年的 Apple Pencil 相比，这次发布显示出苹果“越来越不用心”。

**标签**: `#Apple`, `#MacBook Pro`, `#touchscreen`, `#display technology`, `#hardware`

---

<a id="item-6"></a>
## [苹果自带的 git 与 curl 仍信任已被攻破的 eMudhra 证书](https://emudhra.we-have-a-problem.com/apple.html) ⭐️ 8.0/10

苹果于 2026 年 10 月 17 日就收到了 eMudhra 证书颁发机构事件的通知，但截至 10 月 28 日，macOS 随系统附带的开发者工具（包括 git、curl 和 python3）仍然信任这八张已被攻破的 eMudhra 中间证书。苹果公布的唯一缓解措施要求用户手动修改证书链，并且苹果提示后续的系统更新可能会覆盖这些修改，从而使漏洞重新出现。 任何依赖系统自带 git、curl 或 python3 访问 HTTPS 服务的 macOS 开发者，都可能暴露在利用伪造证书实施的中间人攻击之下，而这正是攻击者窃取凭据和源代码时最想要的立足点。该事件还凸显了各操作系统之间证书信任管理的割裂现状，以及薄弱的厂商修复指引如何让一套被广泛使用的工具链在超过一周的时间里处于无保护状态。 根本原因是密钥生成环节的缺陷——按社区分析是一起 wrap/unwrap 密钥生成事故——攻击者有可能据此还原八张 eMudhra 中间 CA 证书的私钥，这也是 Cloudflare 和 Cisco Talos 推动客户端更新的原因，而不是仅依赖简单的吊销。值得注意的是，使用基于钥匙串（Keychain）的系统信任存储的 macOS 程序不受影响；问题集中在读取独立的 /etc/ssl 证书包的工具上，而由于苹果的手动修复正是修改该文件，常规系统更新可能会将其覆盖。

hackernews · Lobsters · 10月28日 11:03 · [社区讨论](https://news.ycombinator.com/item?id=50271640)

**背景**: 证书颁发机构签发的中间证书位于受信任的根证书与网站使用的叶证书之间，因此一旦中间证书的私钥可被还原，攻击者无需触碰根证书就能为任意域名伪造出看似合法的证书。浏览器和命令行工具会依据本地信任存储校验这些证书链；macOS 至少维护两套存储——Safari 和大多数图形界面程序使用的钥匙串存储，以及命令行工具读取的 /etc/ssl 下的 OpenSSL 风格证书包。当某个 CA 被攻破时，所有仍包含其证书的信任存储都必须更新，这也是为什么响应工作需要通过协调一致的客户端补丁来完成，而不是在服务端做一次改动就能解决。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://emudhra.we-have-a-problem.com/apple.html">Apple's git still trusts the compromised eMudhra certificates</a></li>
<li><a href="https://blog.cloudflare.com/emudhra-certificate-compromise">8 eMudhra certificates are compromised. Here's what you need ...</a></li>
<li><a href="https://blog.talosintelligence.com/compromised-intermediate-certificates/">Compromised eMudhra intermediate certificates</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍认为问题远不止于 git，而是波及所有读取系统证书包的自带工具；许多人对苹果给出的修复方案极为不满——手动修改证书链，而且系统更新可能悄悄将其还原，一位读者直呼离谱，另一位则质疑：对一家以安全为卖点的公司来说，从 /etc/ssl 中移除已吊销的 CA 证书难道不该是件轻而易举的系统更新吗？也有人指出通过 Homebrew 安装的工具和使用钥匙串存储的应用可能不受影响，还有一位评论者在缺乏证据的情况下推测，这次弱密钥生成事件或许是蓄意为之，以便为情报机构制造可乘之机。

**标签**: `#security`, `#macOS`, `#TLS certificates`, `#git`, `#supply chain`

---

<a id="item-7"></a>
## [一条畸形 WAP Push 短信即可让 Android 电话进程崩溃并中断通话](https://smsofdeath.com/) ⭐️ 8.0/10

一项新公布的概念验证显示，只需发送一条构造畸形的 WAP Push 短信，就能让 Android 上的 com.android.phone 进程崩溃，从而导致正在进行中的通话被中断，其中也包括拨打紧急号码的通话。该披露将此定性为 Android 核心电话栈中可远程触发的拒绝服务漏洞，因为攻击者只需向受害者号码发送一条短信即可。 由于 com.android.phone 承载着管理通话状态的核心电话服务，该进程崩溃会直接中断正在进行的通话，而不只是影响某个用户可见的应用；再加上会导致紧急呼叫中断，其严重性远超一般的骚扰性缺陷。任何会接收 WAP Push 消息的 Android 设备都可能被攻击，既无需安装应用，也无需点击链接或进行任何用户操作。 WAP Push 是一种特殊编码的短信，正常用途是携带一个指向 WAP 网址的链接，因此畸形载荷攻击的是电话栈中短信/WAP Push 的解析与分发路径，而非浏览器组件。实际受影响程度取决于设备与厂商定制版本，因为 WAP Push 的处理方式和电话进程的构成在不同 Android 版本和各家 ROM 中存在差异；此外，这份公开披露主要着眼于演示崩溃效果，并未给出补丁或受影响版本清单。

rss · Lobsters · 10月29日 07:22

**背景**: WAP Push 随无线应用协议（WAP）一同引入，目的是让内容能在用户几乎不干预的情况下推送到手机上：它是一条特殊格式的短信，内含一个 WAP 地址链接，手机会以提示形式呈现，并让用户选择是否打开该网址。在 Android 上，com.android.phone 是 AOSP 电话应用的进程名，该进程同时承载电话服务以及应用访问射频与通话状态所用的 android.telephony Java API。由于通话处理逻辑就运行在这个进程里，任何导致其终止的因素——包括收到消息触发的解析器崩溃——都会使电话栈重启，并中断它正在管理的通话。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Wireless_Application_Protocol">Wireless Application Protocol - Wikipedia</a></li>
<li><a href="https://nowsms.com/doc/submitting-sms-messages/sending-wap-push-messages">Sending WAP Push Messages - NowSMS</a></li>
<li><a href="https://stackoverflow.com/questions/5270059/android-telephony-stack-and-dalvik-process-contexts">Android Telephony Stack and Dalvik process... - Stack Overflow</a></li>

</ul>
</details>

**标签**: `#android`, `#security`, `#vulnerability`, `#sms`, `#denial-of-service`

---

<a id="item-8"></a>
## [Linux 内核模块解除 RTX 3090 张量核心限速，ComfyUI 出图快 55%](https://www.reddit.com/r/StableDiffusion/comments/1xi1pzo/a_free_kernel_module_made_my_rtx_3090_generate/) ⭐️ 8.0/10

一位 Reddit 用户（esequiel378）发布了 ComfyUI 基准测试，显示 gpu-unlock 这个 Linux 内核模块（用于解除 RTX 30 系列 GeForce 显卡 FP16/BF16 张量核心限速）可将 Z-Image Turbo BF16、1024²、8 步的出图时间从 7.46 秒/张降至 4.95 秒/张（+51%），叠加降压后为 4.82 秒/张（+55%）。SD 1.5 FP16、1024²、30 步则从 6.40 秒/张提升到 4.64 秒/张（+38%）和 4.52 秒/张（+41%），且在固定种子下每张输出像素的 SHA-256 与原始状态完全一致，其中还包含连续 540 批次、长达 2 小时的稳定性压测。 这让本地生成式 AI 用户在现有硬件上就能获得约 40%–55% 的吞吐提升，并且每张图的能耗下降约 40%（2,369 焦耳 → 1,410 焦耳），而输出像素丝毫不受影响。它也印证了长期以来被怀疑的产品分级做法：NVIDIA 在 GeForce 显卡上把同一块芯片的 FP16/BF16（FP32 累加）速率限制为专业级 RTX A 系列的一半。 有两个实用注意事项值得关注：一是必须避免使用 ComfyUI 的 --fast 参数，因为它会把矩阵乘法切换到 FP16 累加，而这一路径本来就没有被限速，因此性能收益会消失；二是该解锁仅支持 Linux，且只能通过完全断电来恢复。另一个反直觉的发现是：降压在原始状态下反而让显卡变慢，但解锁后却让它变快，因为解锁后的显卡会撞上功耗墙，更低的电压便换回了频率空间。

reddit · r/StableDiffusion · /u/esequiel378 · 10月28日 21:52

**背景**: NVIDIA 在 GeForce 显卡上把用于 FP16、BF16 和 TF32（FP32 累加）运算的张量核心限制在大约一半的速度，而这恰恰是大多数 AI 训练和非量化推理所使用的精度；相比之下，以 RTX A 系列专业卡名义出售的同一块芯片则以全速运行。gpu-unlock 内核模块的绕过方式是：在开机时、NVIDIA 驱动绑定显卡之前先行运行，写入速度选择寄存器（例如 SS0 0x88888888）并执行一次 FLR 复位，之后未经修改的驱动便能让显卡以完整张量核心速率运行。ComfyUI 是一个基于节点图的扩散模型前端，而 Z-Image Turbo 是一个蒸馏版 60 亿参数文生图模型，可在 16 GB 显存内以 8 步完成出图，因此很适合作为衡量单张图片加速比的低延迟测试用例。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/Zagitta/gpu-unlock">GitHub - Zagitta/gpu-unlock: Your GeForce runs AI at half ...</a></li>
<li><a href="https://cldnavi.com/en/blog/rtx3090-gpu-unlock-guide-2026/">gpu-unlock doubles FP16/BF16 on RTX 30-series, but only the ...</a></li>
<li><a href="https://docs.comfy.org/tutorials/image/z-image/z-image-turbo">Z-Image-Turbo in ComfyUI: 8-Step Text-to-Image - ComfyUI</a></li>

</ul>
</details>

**标签**: `#GPU performance`, `#Stable Diffusion`, `#Linux kernel module`, `#hardware throttling`, `#energy efficiency`

---

<a id="item-9"></a>
## [Qwenputer：在 Qwen3.5 内部运行的确定性 RISC-V CPU](https://divagr.com/blog/qwenputer) ⭐️ 7.0/10

一位开发者发布了名为 Qwenputer 的项目，完全在 Qwen3.5 大语言模型内部实现了一颗可运行且确定性的 RISC-V CPU，还顺带实现了一个小型文件系统。它并非让模型“描述”指令执行过程，而是让模型的前向计算本身一步步地完成运算。 这是“模型内计算”的一个引人注目的演示：神经网络表现得像一台小巧而可靠的机器，而不只是一个概率式文本生成器，这也让“记忆”与“真正的计算”在大模型内部的分界线变得更加值得追问。目前它更像一个令人惊喜的奇观而非实用工具，但也暗示了由智能体驱动的系统未来可能如何利用自包含的计算基底。 强调“确定性”意味着相同的输入状态总是产生相同的下一状态，也就是说 CPU 在执行指令时不依赖采样的随机性。作者之所以还要加一个文件系统，是因为“光有一颗 CPU 显然还不够邪门”；而在实际开销上，这种方案几乎必然极其缓慢——它是概念验证，而不是可用的模拟器。

hackernews · csmantle · 10月29日 00:25 · [社区讨论](https://news.ycombinator.com/item?id=50282838)

**背景**: RISC-V 是一套开放、免版税的指令集架构；与大多数 RISC 设计一样，它采用加载—存储（load–store）架构，指令只对寄存器寻址，由独立的加载/存储指令在内存与寄存器之间搬运数据。大语言模型通常是在文本上训练出的下一词元预测器，而非解释器。“模型内计算”指的是通过精心安排 Transformer 的权重、注意力模式和解码流程，使一次前向计算表现得像一段固定算法——在这个例子里，就是一颗执行 RISC-V 指令的 CPU。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/RISC-V">RISC-V - Wikipedia</a></li>
<li><a href="https://github.com/QwenLM/Qwen3">GitHub - QwenLM/Qwen3: Qwen3 is the large language model ...</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论整体相当欢乐：有人调侃这是生物计算机的前奏，有人担心追求回形针最大化的智能体会发现这颗 CPU 并滥用它，还有人表示想让那个臭名昭著的“邪恶 Qwen”人格来当自己的处理器。除了这些玩梗，也有评论者给出了真正有价值的线索——percepta.ai 此前曾用类似 CPU 解码的方式在 Transformer 内实现过 WASM。

**标签**: `#LLM`, `#RISC-V`, `#emulation`, `#AI research`, `#Hacker News`

---

<a id="item-10"></a>
## [Stack Overflow 每月提问量已跌破 1000 条](https://data.stackexchange.com/stackoverflow/query/1926661#graph?t=1) ⭐️ 7.0/10

Stack Exchange Data Explorer 上的一项查询显示，Stack Overflow 目前每月新增提问已不足 1000 条，有评论者指出，这一数字甚至低于该网站诞生最初几个月的水平。该数据在 Hacker News 上广泛传播（437 分、363 条评论），凸显出一场早在生成式 AI 出现之前就已开始的衰退。 十多年来，Stack Overflow 实际上一直是专业编程的公共知识库；它的衰落意味着由同行评审、可公开检索的开发者问答层正在被大模型回答所取代，而这些回答通常不会被归档、未经核验，也难以被搜索引擎索引。这一转变将影响开发者学习与调试的方式、文档空白的填补方式，以及企业从社区平台获取训练数据授权的商业模式。 评论者强调，这一趋势早于 AI：提问量在 2014 年前后已经趋于平缓，2017 年起持续下滑，在 2022 年 11 月 ChatGPT 发布之前就已从 2020 年 6 月前后的局部峰值下跌近 50%，而 ChatGPT 只是完成了最后一击。这一时间线之所以重要，是因为它用既有社区与治理问题的证据，打破了"AI 杀死了 Stack Overflow"这种过于简化的叙事。

hackernews · babelfish · 10月28日 23:35 · [社区讨论](https://news.ycombinator.com/item?id=50282454)

**背景**: Stack Overflow 是 2008 年上线的问答网站，开发者在上面发布编程问题，其他人给出答案并通过投票排序，其内容库权威到大多数关于某个编程报错的搜索都会指向它。自 2022 年底以来，ChatGPT、GitHub Copilot 等工具让开发者无需发帖就能直接得到可用的答案，从而抽掉了多数人访问该网站的主要动机。此次所用的 Data Explorer 是 Stack Exchange 提供的公共接口，可对定期刷新的站点数据副本执行 SQL 查询。

**社区讨论**: 主流观点认为 AI 只是加速而非造成了这场衰退：一些多年积累高声誉的老贡献者表示，他们早在数年前就被不友好的做法赶走了，包括草率地将带有真实细微差别的问题标记为重复、大幅改写用户原帖，以及整体上不欢迎新人的氛围。多位评论者认为，Stack Overflow 作为社区实际上已经名存实亡，只要其历史内容对 AI 训练数据授权仍有价值，它就会继续运营下去。

**标签**: `#stack-overflow`, `#developer-community`, `#ai-impact`, `#moderation`, `#industry-trends`

---

<a id="item-11"></a>
## [Alpine Linux 披露针对 GitLab 的 Ruby 正则漏洞利用尝试](https://alpinelinux.org/posts/GitLab-security-incident-CVE-2026-97229.html) ⭐️ 7.0/10

Alpine Linux 发布了一份安全事件报告，描述了针对其 GitLab 基础设施的 CVE-2026-97229 漏洞利用尝试，并发现使用上游标准 Ruby 重新构建 alpinelinux/gitlab:19.3.6 容器镜像后，修复补丁并未被包含进去。该项目于 10 月 27 日重新发布了 19.3.6 镜像并内置 Ruby 3.3.13，同时警告在此日期之前拉取的任何 19.3.6 镜像以及所有更旧标签的镜像都存在漏洞。 该事件表明，当修复只存在于厂商自己打补丁的运行时之中时，下游的重新构建可能会被悄悄漏掉，使得基于源码构建或第三方镜像构建者在“升级”到号称已修复的版本之后仍然暴露在风险中。对于任何维护打包软件容器镜像的人，尤其是以安全见长的发行版而言，这是一堂具体的供应链课程。 根本原因在于 Ruby 内置的正则表达式引擎 Onigmo：区间重复次数以有符号短整型（MemNumType）存储，传给 Regexp.new 的精心构造的模式会使其溢出，进而破坏内存并导致远程代码执行。由于 GitLab 会编译用户提供的正则表达式（例如 CI 配置中的模式），该漏洞可在未认证情况下被触发；而上游 Ruby 直到 10 月 23 日才在 Ruby 3.3.13、3.4.12 和 4.0.9 中发布修复，远晚于 GitLab 10 月 12 日的版本发布。此外，Alpine 是在已发布的版本标签下重新发布镜像，而非发布新版本号，这让用户很难区分已修复与仍脆弱的 19.3.6 镜像。

hackernews · Lobsters · 10月28日 23:45 · [社区讨论](https://news.ycombinator.com/item?id=50282544)

**背景**: CVE-2026-97229 是一个严重的 GitLab CE/EE 远程代码执行漏洞，影响 19.2.8、19.3.5 和 19.4.2 之前的版本；未认证攻击者可通过在 CI/CD 配置中提供精心构造的正则表达式，在 GitLab 服务器上执行任意代码。值得注意的是，修复并不在 GitLab 自身代码中，而是在 GitLab 官方软件包和镜像所捆绑的 Ruby 解释器的一组补丁里。Alpine Linux 维护着自己基于 Alpine 的 GitLab 容器镜像，它构建在发行版标准的 Ruby 软件包之上，因此不会自动获得 GitLab 私有的 Ruby 补丁。Onigmo 是 Ruby 自 1.9 起使用的正则表达式库（Oniguruma 的一个分支），任何会用不可信输入编译正则表达式的程序都可能受到影响，而不仅仅是 GitLab。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://alpinelinux.org/posts/GitLab-security-incident-CVE-2026-97229.html">GitLab security incident: attempted exploitation of... | Alpine Linux</a></li>
<li><a href="https://nvd.nist.gov/vuln/detail/cve-2026-97229">NVD-CVE-2026-97229</a></li>
<li><a href="https://app.opencve.io/cve/CVE-2026-97229">CVE-2026-97229 - Vulnerability Details - OpenCVE</a></li>

</ul>
</details>

**社区讨论**: 评论者称赞这份报告罕见地坦诚，明确说明了未知之处，包括攻击若成功会泄露哪些数据，并希望补充所用哈希类型等细节。最强烈的批评指向在同一 19.3.6 标签下重新发布已修复镜像而不提升版本号，因为该标签此前的拉取结果仍然存在漏洞。其他人则表达了对内存不安全的 C 库再次引发 RCE 的普遍不满，以及对持续打补丁给源码构建者带来负担的抱怨，其中一位建议 Alpine 改用像 Forgejo 这样更小、可审计的代码托管平台，而不是 GitLab。

**标签**: `#security`, `#gitlab`, `#ruby`, `#vulnerability`, `#supply-chain`

---

<a id="item-12"></a>
## [Surge AI 发布 DAYJOB: Tax 基准：最强 AI 代理仅通过 10.8% 的真实税务任务](https://surgehq.ai/blog/dayjob-tax) ⭐️ 7.0/10

Surge AI 发布了 DAYJOB: Tax 基准，包含 50 项专业税务任务，这些任务取材于真实的客户资料夹（共 1,789 个文件），覆盖税务实践的八个领域，并按高达 95% 的严格评分标准判定是否通过。表现最好的 Claude Sonnet 5.5 仅通过了 10.8% 的任务，GPT-6 Astra 为 4.8%，Gemini 4 Argon 为 3.2%，Surge 由此得出结论：“AI 代理尚未通过审计”。 税务申报是一个高风险、极度注重细节的专业领域，一个填错的数字就可能造成真实的金钱损失，因此不足 11% 的通过率对于那些认为 AI 代理已可胜任面向客户的会计工作的人来说是一个清醒的警示。同时，这一基准也把评测从整齐的选择题式题目推向杂乱、多文件、指令不完备的真实工作场景——而这正是大多数企业级代理部署最终要接受的检验环境。 这些任务刻意包含初始指令中并未完全说明的决策点，而 95% 的评分门槛意味着“差一点”也会被判为失败，而非给予部分分数。DAYJOB: Tax 是 Surge 专业工作基准系列的第三弹，此前已发布医疗（Healthcare）与金融（Finance）两个版本。

hackernews · landonxi · 10月28日 15:46 · [社区讨论](https://news.ycombinator.com/item?id=50275626)

**背景**: 传统上，AI 代理基准测试衡量的是数学题或编程题这类定义明确的任务，因为正确答案可以被自动、容易地检验。而专业服务工作则完全不同：代理需要打开一个装满客户文档的文件夹，判断哪些内容相关，套用特定司法辖区的规则，并产出执业人士愿意签字的成果。DAYJOB 正是 Surge AI 试图大规模构建这类环境的尝试，而偏低的得分恰恰反映出当前代理距离在这类岗位上无监督独立工作还有多远。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://surgehq.ai/blog/dayjob-tax">DAYJOB: Tax — Benchmarking AI Agents on Professional Tax Work</a></li>
<li><a href="https://explainx.ai/blog/surge-ai-dayjob-tax-benchmark-50-tax-assignments-sonnet-5-5-10-8-percent-hn-2026">Dayjob: Tax Benchmark: Best AI Agent Passes 10.8% - explainx.ai</a></li>
<li><a href="https://ai-tldr.dev/releases/surge-dayjob-tax-benchmark/">DAYJOB: Tax — best AI agent passes only 10.8% of… | AI/TLDR</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的评论者分成了两派：一派有亲身实践带来的乐观，另一派则是吃过亏后的谨慎。多位开发者表示自己用 Claude 或 Codex 搭建了报税工具，分别处理美国和南非的税务并取得成功，其中一位还分享了在 GitHub 上把 IRS 表格与工作表形式化的项目，称已覆盖约 60% 的美国联邦税务情形；也有人讲述相反的经历，一位用户发现经会计师协助生成的申报表错误百出，退税额被少算了近 2000 美元。讨论中反复出现的观点是：当人类本身足够懂这一领域、能够发现错误时，大模型非常强大；反之则风险很高。

**标签**: `#AI agents`, `#LLM evaluation`, `#tax preparation`, `#professional services`, `#benchmarks`

---

<a id="item-13"></a>
## [Simon Willison：2026 年 10 月是“氛围编程”游戏的分水岭](https://simonwillison.net/2026/Oct/28/vibe-game-development/) ⭐️ 7.0/10

在 2026 年 10 月 28 日的一篇博客文章中，Simon Willison 提出 2026 年 10 月是“氛围编程”游戏的分水岭，其意义堪比 2025 年 11 月 Opus 4.5 与 GPT-5.1 让编程智能体成为可靠日常工具的那次转折。他特别称赞 Claude Opus 5.5 在 3D 建模、音乐生成，以及最重要的游戏设计方面取得实质性进步，并列举了他完全不看代码就做出来的四款纯浏览器 HTML/JavaScript 游戏——Tree Appreciator、Emberwick、Battle Drones 和 Pumpkin Farmer（又名 Quarter Sun Cove）——这些游戏他是真心觉得好玩。 这一论断把讨论的焦点从“大模型能否生成看起来像游戏的东西”转向“能否做出真正好玩的游戏”，而后者正是 Willison 本人曾怀疑模型不具备的能力。如果他的判断成立，游戏原型制作将对非程序员敞开大门，瓶颈将从实现转向构思新颖有趣的创意；同时也会加剧本已紧张的关于游戏中 AI 生成美术、音乐与代码的争论。 Willison 称自己的做法属于“经典意义上”的氛围编程——完全不看代码——并提到在 Battle Drones 的 v4 更新中，他只是让 Opus 5.5 “把它做得有趣得多”（Make it a LOT more fun），游戏品质就明显提升。他还表示，据他观察 GPT-6 Astra 完全能做出游戏，但对“好玩”的把握尚不及 Opus 5.5，预计 OpenAI 会在年底前追上；四款示例游戏全部基于 HTML 与 JavaScript 在浏览器中运行，其中最简单的 Tree Appreciator 甚至无需 Claude Code，直接用普通 Claude 聊天界面就完成了。

rss · Simon Willison · 10月28日 13:55

**背景**: 氛围编程（vibe coding）指用自然语言描述需求、让大语言模型自动生成代码的开发方式，这一说法在 2025 年初流行开来，通常还意味着开发者根本不去阅读生成的代码。AI 编程智能体比代码补全更进一步：给定一个目标后，它会读取代码仓库、规划跨文件改动、运行构建与测试，并不断迭代直到任务完成。长期关注开发者工具的 Willison 此前曾把 2025 年 11 月认定为这类智能体对专业工程师变得可靠的时刻；这篇新文章把同一分析框架套用到游戏开发上，而这里此前缺的不是写代码的能力，而是设计品味。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://simonwillison.net/2026/Oct/28/vibe-game-development/">The October inflection point for vibe game development</a></li>
<li><a href="https://en.wikipedia.org/wiki/Vibe_coding">Vibe coding - Wikipedia</a></li>
<li><a href="https://agentic.ai/best/coding-agents">30 Best AI Coding Agents in 2026 — Agentic.ai</a></li>

</ul>
</details>

**标签**: `#vibe-coding`, `#AI-coding-agents`, `#game-development`, `#LLMs`, `#Simon-Willison`

---

<a id="item-14"></a>
## [Supabase 将自身定位为 AI 智能体的后端基础设施](https://latent.space/p/supabase/) ⭐️ 7.0/10

在 Latent Space 的一期访谈中，Supabase 创始人 Paul Copplestone 和 Ant Wilson 讨论了公司如何专门为 AI 智能体构建后端基础设施，把记忆、工具和数据整合到同一个平台中。此前 Supabase 已在 Select 2026 大会上宣布支持 MCP 服务器，该公司称这使其成为首个将智能体视为一等基础设施消费方的重大后端即服务（BaaS）平台。 目前智能体开发者往往需要为记忆、工具调用和数据存储拼接多个独立服务，而一个统一的、基于 Postgres 的后端有望大幅简化智能体架构并降低集成成本。如果智能体成为后端服务的主要消费方，这将使 Supabase 这类数据库平台从被动存储转变为 AI 应用技术栈的核心。 Supabase 通过 MCP 的工具边界向智能体开放数据库创建、Edge Functions 和长时间运行的计算任务，同时提供可复用的 Agent Skills 指令集以及一步式插件包。该平台底层仍是常规的 PostgreSQL 数据库，配合认证、存储、实时订阅和边缘函数，因此所谓的“智能体能力”主要是把既有基础能力暴露给模型，而非全新的引擎。

rss · Latent Space · 10月28日 19:48

**背景**: Supabase 是 Firebase 的开源替代方案，将 PostgreSQL 数据库与认证、文件存储、实时订阅和边缘函数打包为单一托管服务。AI 智能体是由大语言模型驱动的程序，能够自主调用工具并保存状态，因此需要可靠的记忆、安全的工具访问和结构化数据。MCP（模型上下文协议）是一种让智能体发现并调用外部工具的标准接口，已成为服务向模型暴露能力的常见方式。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://supabase.com/solutions/agents">Supabase for Agents</a></li>
<li><a href="https://www.mech.app/articles/supabase-mcp-server-how-backend-as-a-service-becomes-agent-as-a-service/">Supabase MCP Server: How Backend-as-a-Service Becomes Agent ...</a></li>
<li><a href="https://supabase.com/docs/guides/ai-tools">AI Tools | Supabase Docs</a></li>

</ul>
</details>

**标签**: `#Supabase`, `#AI agents`, `#backend infrastructure`, `#Postgres`, `#developer tools`

---

<a id="item-15"></a>
## [Nathan Lambert 探讨 AI 基准测试与“基准测试者困境”](https://www.interconnects.ai/p/artificial-analysis-v5-and-the-benchmarkers) ⭐️ 7.0/10

Nathan Lambert 在 Interconnects 发表文章，回顾 AI 基准测试行业，并以 Artificial Analysis v5 和“基准测试者困境”为框架，讨论当前基准测试遗漏了什么。 基准测试会影响企业采用哪些模型、外界如何判断研究进展，以及开发者把优化重点放在哪里，因此基准测试的盲点或失真可能影响整个 AI 生态。 标题中提到的 Artificial Analysis v5 指的是 Intelligence Index v5.0，这是一个聚合九项高难度评测的复合基准，覆盖知识工作、编程、科学和常识；目前可见的摘录很短，因此文章的具体批评应阅读全文。

rss · Interconnects · 10月28日 12:58

**背景**: 基准测试是标准化评测，用于比较 AI 模型在推理、编程和事实知识等能力上的表现。像 Artificial Analysis Intelligence Index 这样的复合指数会把多项评测合并成一个总分，以概括模型的整体能力。随着模型不断进步，基准测试可能饱和——顶尖分数集中在接近上限的位置——或成为被针对性优化的目标，从而使其衡量真实进展的能力变得复杂。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://artificialanalysis.ai/evaluations/artificial-analysis-intelligence-index">Artificial Analysis Intelligence Index v5.0</a></li>
<li><a href="https://www.vellum.ai/blog/llm-benchmarks-overview-limits-and-model-comparison">LLM Benchmarks in 2024: Overview, Limits and Model Comparison</a></li>

</ul>
</details>

**标签**: `#AI benchmarking`, `#LLM evaluation`, `#model evaluation`, `#AI industry`, `#benchmark design`

---

<a id="item-16"></a>
## [《经济学人》刊文：AI 是荷马史诗的技术版本](https://www.economist.com/by-invitation/2026/10/28/ai-is-a-technological-version-of-the-homeric-songs) ⭐️ 7.0/10

2026 年 10 月 28 日，《经济学人》刊出由 Henry Farrell 与 Cosma Shalizi 撰写的特约文章，主张 AI 智能体“不只是随机鹦鹉，也比机器神祇更奇特”。两位作者既反对把模型贬低为纯粹统计式文本模仿，也不认同将其视为初生的超级智能，而是提出用古希腊口传传统中的荷马史诗作类比来理解它们。 围绕 AI 的讨论如今已两极分化：一边是带有贬义色彩的“随机鹦鹉”批评，另一边是近乎宗教式的“机器神祇”叙事，而这两种说法都在影响公众、监管者和投资者对 AI 能力与风险的判断。这一历史类比把 AI 的输出视为在文化中传承、被反复重新组合的素材，有望让关于作者身份、原创性与责任归属的讨论不再局限于“是否像人脑”这一框架。 公开可见的内容只有一句导语，完整论证位于《经济学人》的付费墙之后，且属于概念性推演而非新的实证成果。其学术背景是“口头程式理论”：吟诵者并非逐字复述，而是在表演过程中动态调用记忆中的程式化短语，从而在传承中产生变化与创新。

rss · The Economist · 10月28日 10:33

**背景**: “随机鹦鹉”这一说法源自 Emily Bender 等人 2021 年的论文，认为大语言模型只是在按统计概率拼接词序列，并不真正理解语义。与之对立的“机器神祇”视角则把 AI 描绘成即将到来的、带有近乎魔法般能力的超级智能。荷马类比依托的是数十年的学术研究，尤其是 Milman Parry 与 Albert Lord 的成果：他们证明《伊利亚特》和《奥德赛》诞生于活态口传传统，诗人是在表演中现场创作，而非背诵固定的书面文本。而 AI 智能体则是能够代表用户进行规划、调用工具并带有一定自主性地追求目标的软件系统。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.economist.com/by-invitation/2026/10/28/ai-is-a-technological-version-of-the-homeric-songs">AI is a technological version of the Homeric songs</a></li>
<li><a href="https://en.wikipedia.org/wiki/Stochastic_parrot">Stochastic parrot - Wikipedia</a></li>
<li><a href="https://adrianlerer.substack.com/p/odysseus-homer-and-artificial-intelligence">Odysseus, Homer, and Artificial Intelligence</a></li>

</ul>
</details>

**标签**: `#AI`, `#philosophy`, `#technology and society`, `#commentary`, `#analogy`

---

<a id="item-17"></a>
## [Yoshua Wuyts 指出 Rust 的 Future trait 缺少一个状态](https://blog.yoshuawuyts.com/the-future-trait-has-a-missing-state) ⭐️ 7.0/10

在题为《The Future Trait Has A Missing State》的新博文中，Rust 异步生态作者 Yoshua Wuyts 指出，Rust 的 `Future` trait 所描述的异步计算模型并不完整，存在一个当前设计未能表达的状态。文章进一步分析了这一缺失对 async Rust 语义以及相关语言设计决策意味着什么。 `Future` trait 是整个 async Rust 的基础抽象，因此“其核心模型缺少一个状态”这一论点，对所有编写异步库或异步应用的开发者、以及考虑未来 trait 演进的语言设计者都具有意义。由于执行器、运行时以及编译器对 `async`/`await` 的脱糖展开都依赖同一套 trait 契约，即便是概念层面的缺口也可能在整个生态中产生连锁影响。 这篇博文属于设计层面的分析，而非已被接受的提案：它并没有宣布新的 RFC、已稳定化的特性，也没有公布将进入标准库的具体改动。文章的相关讨论托管在 Lobsters 上，而那里正是 Rust 社区进行偏设计向辩论的常见场所。

rss · Lobsters · 10月29日 04:24

**背景**: 在 Rust 中，`async fn` 与 `async` 块会被编译成实现了 `Future` trait 的状态机；对 future 调用 `.await` 实际上会反复调用它的 `poll` 方法，当值就绪时返回 `Poll::Ready(value)`，否则返回 `Poll::Pending`。future 是惰性的——不被轮询就不会执行——而当它返回 `Pending` 时会注册一个 `Waker`，让执行器知道在可以推进时再次轮询它。此外，Rust 并没有独立的取消机制：丢弃一个 future 就等同于停止它，这也是“一个 future 究竟可能处于哪些状态”会成为异步设计讨论中反复出现的话题的原因之一。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://rust-lang.github.io/async-book/01_getting_started/04_async_await_primer.html">async /.await Primer - Asynchronous Programming in Rust</a></li>
<li><a href="https://hightechmind.io/rust/322-future-trait.html">Example 322: 322: The Future Trait and Poll | Functional Rust</a></li>
<li><a href="https://arcmutex.com/content/async-trait-object-safety">How does ` async _ trait ` work around the limitation that... | ArcMutex</a></li>

</ul>
</details>

**标签**: `#Rust`, `#async`, `#Future trait`, `#language design`, `#concurrency`

---

<a id="item-18"></a>
## [Daniel Lemire 展示 C++ 中每秒十亿次查询的查找表](https://lemire.me/blog/2026/10/26/billion-query-per-second-lookup-tables-in-c/) ⭐️ 7.0/10

Daniel Lemire 发表了一篇 C++ 性能工程文章，介绍能够达到每秒约十亿次查询量级的查找表实现，该文章随后被提交到 Lobsters 上讨论。当前提供的正文里只有一个指向评论区的链接，因此具体的实现技巧与基准测试数字并未包含在给定内容中。 查找表是解析器、哈希索引、数据库引擎、编码校验器与网络报文分类器的核心构件，因此每秒十亿次的吞吐量把一个“廉价但缓慢”的技巧重新定义为真正的高性能原语。对于构建延迟敏感系统的工程师而言，这类结果表明：只要围绕内存层级来设计数据布局与分支行为，而非完全交给编译器，仍有大量性能空间可以挖掘。 这个量级意味着每条查询的预算只有几纳秒：在约 3 GHz 的 CPU 上，每次查找必须在约三个时钟周期内完成，只有表驻留在 L1/L2 缓存中、且每条查询都避开不可预测的分支和长依赖加载链时才可能实现。因此达到该速率通常需要紧凑编码、缓存行友好的布局、批量或向量化查询以及软件预取；并且这类数字一般来自合成的均匀分布或批处理负载，而非真实环境中大量缓存未命中的访问模式。

rss · Lobsters · 10月28日 09:47

**背景**: 查找表用内存访问替代计算：程序不再计算某个值，而是索引到预先算好的数组中，这是 CRC 表、字符分类、Huffman 与区间解码器以及完美哈希中常见的“以空间换时间”策略。现代 CPU 让这一权衡远比看上去复杂，因为一次主存访问的开销约为 80 至 100 纳秒，比一次 L1 缓存命中高约两百倍。因此查找表的性能主要不取决于算术运算，而取决于表位于缓存层级的哪一层、访问下标是否可预测，以及处理器能否并行重叠大量相互独立的查找。Daniel Lemire 是一位计算机科学教授，以在 C++ 和 Java 中讨论这类微架构现实问题而闻名。

**标签**: `#C++`, `#performance`, `#lookup tables`, `#optimization`, `#benchmarking`

---

<a id="item-19"></a>
## [HP 论文称 ACL 无法处理多主体交互，助长点击劫持与 CSRF](https://shiftleft.com/mirrors/www.hpl.hp.com/techreports/2009/HPL-2009-20.pdf) ⭐️ 7.0/10

一份 2009 年的 HP Labs 技术报告（HPL-2009-20）指出，ACL 访问控制模型无法为涉及两个以上主体的交互做出正确授权决定，因为所需信息不会在消息发送过程中被保留。该论文称，这一逻辑错误被影响许多 Web 应用的点击劫持和 CSRF 攻击所利用。 这一批评的重要性在于，它把 CSRF 和点击劫持不只视为实现缺陷，而是 ACL 授权模型与多主体 Web 交互之间根本性不匹配的症状。为现代 Web 应用设计授权机制的开发者和安全架构师，在仅依赖 ACL 式检查时应当理解这一局限。 该报告是一项概念性安全分析，而非新的漏洞披露，并指出这一缺陷早已被文献记录，但仍未被广泛理解。其论点核心在于：当一个主体促使另一个主体发送请求时，发起主体的上下文会丢失，而这正是 CSRF 和点击劫持所滥用的一种间接性。

rss · Lobsters · 10月29日 04:13

**背景**: 访问控制列表（ACL）是一种常见安全模型，它把主体（如用户或进程）映射到资源上的权限，ACL 检查通常询问请求主体是否被允许执行某个操作。点击劫持通过覆盖或隐藏界面元素，诱使用户点击与其感知不同的内容；跨站请求伪造（CSRF）则让已登录用户的浏览器发送由攻击者选定的已认证请求。这两种攻击都利用了一种情况：使用其凭据的一方并非实际发起操作的一方。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Clickjacking">Clickjacking - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Cross-site_request_forgery">Cross - site request forgery - Wikipedia</a></li>
<li><a href="https://mobidev.biz/blog/access-control-models-explained-acl-vs-rbac-vs-abac">Access Control Security Models Explained: ACL vs RBAC vs ABAC</a></li>

</ul>
</details>

**标签**: `#security`, `#access-control`, `#web-security`, `#CSRF`, `#ACL`

---

<a id="item-20"></a>
## [SpEdE：开源 ComfyUI 工具包支持点击编辑高斯泼溅场景](https://www.reddit.com/r/StableDiffusion/comments/1xidz0n/splat_edit_engine_opensource_toolkit_for/) ⭐️ 7.0/10

SpEdE（Splat Edit Engine）是一个以 AGPL 协议开源的 ComfyUI 工具包，作为 #OpenSourceHiggsfield 竞赛作品发布：用户载入高斯泼溅场景后点击某个物体，即可将其删除、按文本提示（可选配参考图）替换，或提取为独立的干净 PLY 文件。整个流程在本地以开放权重运行——SAM 3.1 负责选取、Qwen-Image 2.1 负责绘制替换内容、MoGe-3 负责几何估计、TripoSplat 负责把图像转成高斯点，并附带一个简易 Web UI，用户无需手动连线搭建节点图。 高斯泼溅场景的编辑此前基本局限于研究代码和定制脚本，因此一个点击式、完全本地运行并集成进 ComfyUI 的流水线，显著降低了艺术家和爱好者的使用门槛。其删除模式会针对所有拍摄相机重新拟合真实高斯点来填补空洞，解决了简单删除最明显的缺陷——一旦环绕视角，空洞就会崩坏。 作者仅在单台 Ubuntu + RTX 5090 机器上测试过：Windows 尚未验证，gsplat 通常需针对本地 torch/CUDA 版本编译（最可能卡住的一步），而在显存低于 32 GB 的显卡上工作流大概需要调参。这些注意事项都已写入 GitHub 仓库 Burgstall-labs/ComfyUI-SpEdE 的 README。

reddit · r/StableDiffusion · /u/Burgstall · 10月29日 08:07

**背景**: 3D 高斯泼溅（Gaussian Splatting）把照片中的场景重建为数百万个带方向的三维高斯点，通过快速光栅化渲染，而不是用网格或表面表示；gsplat 是一个开源库，提供 PyTorch 绑定和高度优化的 CUDA 内核用于训练与渲染这类场景。SpEdE 把多个开放模型串联起来：SAM 分割出被点击的物体，MoGe 估计单目几何以便把新物体贴合到原有表面，Qwen-Image 生成或编辑替换图像，TripoSplat 再把单张图像转成高斯点。ComfyUI 是一个基于节点的本地生成模型编排界面，这也是整条编辑流水线能在用户自己的 GPU 上离线运行的原因。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/html/2409.06765v1">gsplat : An Open-Source Library for Gaussian Splatting</a></li>
<li><a href="https://comfyui-wiki.com/en/models/moge/moge">MoGe : Monocular Geometry Estimation | ComfyUI Wiki</a></li>
<li><a href="https://triposplat.app/">TripoSplat - Triposplat AI 3D Gaussian Generator</a></li>

</ul>
</details>

**标签**: `#Gaussian Splatting`, `#3D Scene Editing`, `#ComfyUI`, `#Open Source`, `#Generative 3D`

---