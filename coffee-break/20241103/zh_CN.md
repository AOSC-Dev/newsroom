安记冰室・十月下
=============

<!-- 端着甏肉干饭的 -->

> “热乎儿的甏肉干饭，来一碗儿？”

欢迎阅读安同开源社区 (AOSC) 期刊《安记冰室》！本栏目旨在以轻松可及的方式，以图文形式介绍过去两周的开发进展、社区事务与近期社区内外活动资讯。此外，本栏目还用于发布与社团及行业人士及代表的访谈录，以特辑形式发布。本栏目不发表评论性内容。

致歉：休刊说明
-------------

回来了（哈欠）。

放了各位读者朋友两个月的鸽子，实在抱歉。过去近两个月《安记冰室》欠奉的很大一部分的原因来自于节假日、日常工作繁忙和“安同校园行”活动重启前后的诸多工作。当然，不论如何，休刊还是应该说一声的，所以——私密吗喽！

十一月开始，我们会尽力确保《安记冰室》准时发刊。

白铭骢   
2024 年 11 月 2 日

用户公告
--------

<!-- 本节请使用链接形式指向先前发布的公告正文，尽可能缩短篇幅 -->

### CUPS 及相关软件包推送安全更新，修复已公开可利用的高危漏洞

九月底，安全研究员 [evilsocket](https://www.evilsocket.net/2024/09/26/Attacking-UNIX-systems-via-CUPS-Part-I/) 披露了与 CUPS 等软件包相关的四个安全漏洞，CVSS 3.1 评分最高达到 [9.1](https://www.cve.org/CVERecord?id=CVE-2024-47177)。我们已于 2024 年 9 月 27 日推送更新，修复上述安全漏洞。

有关该漏洞的详细波及范围及修复指引，详请见下列公告。

[阅读安全公告 >>](20240927-cups-vulnerability.zh_CN.md)

### NVIDIA 显卡及部分龙架构用户在近期内核更新后可能无法正常启动系统

自 6.10.12（稳定主线/mainline）及 6.6.53（长期支持/longterm) 内核更新以来，我们收到多名用户反馈称其在更新内核后，使用 NVIDIA、龙芯 7A 显卡无法正常启动系统，具体症状为：系统画面卡滞在 GRUB 启动内核的画面，系统实际成功启动（可通过 SSH 访问）后画面亦无变化。

有关该问题的排查结果和解决方法建议，详请见下列公告。

[阅读用户公告 >>](20241008-nvidia-ls7a-simpledrm-performance-notes.zh_CN.md)

### 近期安装的安同 OS 可能无法在部分程序中使用输入法

在九月发布的安装盘中，默认系统配置中设置了错误的输入法模块，导致一部分闭源软件（已知微信及 Steam 受此问题波及）无法正常使用输入法。

有关该问题的排查结果和解决方法建议，详请见下列公告。

[阅读用户公告 >>](20240928-input-method-profile.zh_CN.md)

### 小熊猫包管理 (oma) 安装源签名刷新公告

Ubuntu 24.10 更新了 APT [加密签名算法要求](https://discourse.ubuntu.com/t/new-requirements-for-apt-repository-signing-in-24-04/42854)，而我社先前使用的软件源 GPG 公钥算法 (nistp521) 不符合其要求的：

- 2048 位以上的 RSA
- Ed25519
- Ed448

因此，Ubuntu 24.10、deepin V23 及开放麒麟 (openKylin) 2.0 等使用 APT >= 2.8 版本的发行版无法正常使用我社官方源安装 oma。为解决该问题，我们已于 UTC+8 时间 2024 年 10 月 6 日生成算法为 Ed25519 的新软件源签名密钥。

有关本次签名刷新的详情与注意事项，详请见下列公告。

[阅读用户公告 >>](20241006-new-oma-repo-key.zh_CN.md)

社区脉动
--------

### “安同校园行”重启：宁夏理工学院与澳门科技大学活动后记

![宁夏理工学院的同学们围观龙芯 3A6000 台式机的“原神，启动！”](/coffee-break/20241103/imgs/nit-loongson-genshin.jpg)
> 宁夏理工学院的同学们围观龙芯 3A6000 台式机的“原神，启动！”

安同开源社区从校园诞生，校园及草根开源社区和组织的发展也是社区建立时的初心之一。如今，高校社团亦是我社关注和扶持的对象。自 2024 年起，我们与众多高校社团协作，组织“安同校园行”活动，邀请社区贡献者、行业代表等走进校园，分享社区和专业工作经验，让更多学生接触、了解和融入开源社区乃至行业前沿。 

![“安同校园行”澳门科技大学站活动海报](/coffee-break/20241103/imgs/must-lug-poster.jpg)
> “安同校园行”澳门科技大学站活动海报

随着“安同校园行”活动的重启，我们在十月探访了宁夏理工学院和澳门科技大学，与两所学校的学生一同举办了两场趣味横生的活动。我们在两所学校的活动中均按照同学们的期望邀请了社区内外讲者，围绕其感兴趣的课题组织了主旨演讲和分享。在分享环节后，我们背着龙芯 3A6000 台式机，让同学们体验当今主流国产硬件平台的硬件性能与软件功能；此外，我们还组织了安同 OS 安装作坊，由安同 OS 维护者们现场辅导同学们安装安同 OS，在让不少初次接触 Linux 的同学成功“入坑”的同时，也让一些对安同 OS 感到好奇的同学们体验了来自我社的“东方神秘发行版”。

我们衷心希望参加两场活动的同学们在知识与快乐间有所收获。从校园来的安同开源社区也将继续走进校园，努力破除信息隔阂和推行行业知识共享。在今年仅存的两个月中，我们还将前往三所高校协办“安同校园行”活动：

- 11 月 9 或 10 日：兰州大学
- 12 月 8 日：山东大学（青岛分校）
- 12 月（日期待定）：西安电子科技大学

有关“安同校园行”详情及现场体验，请见如下几个链接：

- [“安同校园行”官方介绍](https://aosc.io/events#campus)
- [来自宁夏理工学院学生社团“蜘蛛人网络服务队”的活动回顾](https://mp.weixin.qq.com/s?__biz=MzkwODUyOTQxNw==&mid=2247484777&idx=1&sn=efaf4a36ceac1a1240abf83bbc8d0804&chksm=c0c9df0ff7be56197f3ef0063a4f4273674c570bf549e95c5bad4aaef99a5987c06c2a3a0d71&token=2110527252&lang=zh_CN#rd)
- [“安同校园行”的 Bilibili 直播回放](https://space.bilibili.com/3494371531950426)

### 100% 通过率：社区“开源之夏”实习项目圆满收官

![安同开源社区的“开源之夏”2024 实习项目](/coffee-break/20241103/imgs/aosc-ospp-home.png)
> 安同开源社区的“开源之夏”2024 实习项目

经过三个月的开发及评审周期，我社在本年度的三个“开源之夏”实习项目均成功结项：

- [自由及开源软件简中本地化工作](https://summer-ospp.ac.cn/org/prodetail/24f3e0160)（学生：葛镕锋；导师：白铭骢）
- [设计编写安同 OS 用户手册及编写规范](https://summer-ospp.ac.cn/org/prodetail/24f3e0161)（学生：侯文敏；导师：温柔）
- [为 RISC-V 开发板提供安同 OS 系统镜像](https://summer-ospp.ac.cn/org/prodetail/24f3e0162)（学生：李伽扬；导师：Icenowy Zheng）

恭喜各位学生，期望在社区日后的工作交流中仍能看到各位的身影！在此，也感谢三位导师的辛勤付出和各位社区贡献者与好友对“开源之夏”项目的大力支持。

### 2024 年社区纪念衫（冬装）设计与订购预告

![最新最热安同爆款冬装！](/coffee-break/20241103/imgs/merch-poster-coffee-break.jpg)
> 最新最热安同爆款冬装！

好消息！我们计划开放五款纪念衫的订购，其中包含 AOSCC 2024 设计的再版

由于目前已经入冬，因此我们在复用设计的同时将衣服款式改为了冬装（套头连帽衫）；另外还引入了三款新设计：

- o... oma!（套头连帽衫，左一）
- 安同 OS 提示符（套头连帽衫，左二）
- 安同 OS 提示符（风衣，右一）

我们目前正在积极与供货商议价，价格商议完毕后即开放订购，敬请期待！

### 新一批安同 OS 默认壁纸出炉！

感谢各位踊跃参与廿四年末暨“流浪相机”默认壁纸投票！本次候选壁纸均来自于三月启动的“流浪相机”接龙活动，共有十名社区好友参与，在中国多个地区捕捉美丽风景。

至截止时，我们共收到了 157 份投票，选出默认桌面壁纸及锁屏壁纸如下：

![默认桌面壁纸（作者：椰椰雪球；标题：采芳 / Grazing）](/coffee-break/20241103/imgs/wallpaper-grazing.jpg)
> 默认桌面壁纸（作者：椰椰雪球；标题：采芳 / Grazing）

![默认锁屏壁纸（作者：匿名撰稿人；标题：暗日 / Dark Days）](/coffee-break/20241103/imgs/wallpaper-dark-skies.jpg)
> 默认锁屏壁纸（作者：匿名撰稿人；标题：暗日 / Dark Days）

恭喜二位投稿人，也感谢各位踊跃参与“流浪相机”的朋友们，来年“流浪相机”活动再见！

**推送计划**

新一批“流浪相机”壁纸包将随近期安同 OS 系统更新推送，敬请期待！

### 社区新门户网站上线

![安同开源社区新版主页（冬季配色）](/coffee-break/20241103/imgs/aosc-portal-winter.png)
> 安同开源社区新版主页（冬季配色）

经过逾一年艰难的选型、开发和内容编写，社区的新门户终于竣工，与大家见面了（其实问题还很多，但差不多是时候让年久失修的老门户退休了）！

[一睹为快 >>](https://aosc.io/)

门户网站的主要设计目标是在单屏幕空间中显示尽可能多的有用信息，其主要实现手段是综合使用多列布局及纵横导航部件。此外，新门户网站还尝试摆脱 FOSS 社区网站的一些常见设计导向，采取图文混编、产品导向为主要呈现逻辑，方便新老用户了解社区项目、活动及公告等。

**后续计划**

考虑到新网站上线存在时间及交付压力，我们决定将一部分工作留作上线后的愿望清单。如果您有兴趣参与推进相关工作，欢迎与我们联系。

[上线后迭代愿望清单 >>](https://github.com/AOSC-Dev/website-2023/issues/19)

如果您在浏览社区门户时遇到问题，也欢迎您在社区各群组与我们联系，或在[网站源码仓库](https://github.com/AOSC-Dev/website-2023)提交问题报告。

### Ubuntu 20 周年：生日快乐！

![Ubuntu，生日快乐！](/coffee-break/20241103/imgs/ubuntu-at-20-slim.png)
> Ubuntu，生日快乐！

2004 年 10 月 20 日，Ubuntu 4.10 横空出世。虽说 Ubuntu 无所谓首个“桌面发行版”，但其对易用性和图形化的追求很快使其成为许多 Linux 初心者的首选：一时间，GNOME、APT、“deb 包”成为了许多用户心目中“易用、好用的 Linux 发行版”的黄金标准。

如今，Ubuntu 仍是 Linux 乃至操作系统生态中的一颗耀眼明星。不论 Ubuntu 给我们走向开源世界的启蒙一课和星星之火，还是其给予 Linux 软件生态乃至操作系统业界的诸多启示，Ubuntu 为同为操作系统和基础软件研发同行的我们留下了不可多得的宝贵财富。

安同开源社区贡献者在此恭贺 Ubuntu 24.10 顺利发布，顺祝 Ubuntu 20 岁生日快乐！

系统快讯
--------

### KDE 6 开放测试

![KDE 6 桌面换代更新来了！](/coffee-break/20241103/imgs/kde-6-call-for-testing.png)
> KDE 6 桌面换代更新来了！

KDE 桌面环境作为安同 OS 的默认界面，决定了系统的桌面使用体验。

自年初发布以来，KDE 6 已日趋成熟；为提早排查界面和兼容性等方面可能存在的问题、调整默认桌面配置并尽可能充分地收集用户反馈，我们正式开启了 KDE 6 桌面环境的测试源，供用户朋友测试尝鲜。

**参与测试**

如果您希望参与 KDE 6 的尝鲜测试，请使用如下命令加入测试源：

```bash
oma topics --opt-in kde-6
```

请注意：KDE 6 测试源更新频繁且稳定性未必有保障，请谨慎在主力生产用设备上更新使用。

**关于 Wayland 与 X11**

为继续保障应用兼容性和基础使用体验，KDE 6 周期我们计划继续使用 X11 会话，并提供 Wayland 会话作为可选项。

考虑到 KDE 对 X11 的支持水平和 X11 组件维护活跃度在缓慢下滑，且 Wayland 可以提供 HDR、平板支持等增强特性，我们也认识到支持 Wayland 的重要性。

因此，如果您在使用 Wayland 会话时遇到问题，也欢迎您向我们反馈，我们会尽力尝试解决。

**反馈指引**

我们欢迎您通过任意平台上的社区聊天群组反馈问题；为了提高反馈的响应效率和降低维护者负担，在提供反馈时请注意如下几点：

- 前因后果：请尽可能完整、清晰地描述您遇到问题前后执行过的操作
- 图文并茂：如有可能，请提供问题相关的截图、录像及日志
- 保持耐心：问题调查和修复需要时间，我们会尽力解决您发现的问题和提出的意见；如果我们长时间没有响应您的反馈，请保持善意并提醒我们

### 巩固提升：小熊猫包管理 (oma) 1.12 版发布

![.deb 包管理哪家强？o... oma!](/coffee-break/20241103/imgs/o-oma-slim.png)
> .deb 包管理哪家强？o... oma!

历经一个月的设计、开发与测试，oma 1.12.0 终于与大家见面了！

本次更新包含超过 10 个新特性，让 oma 更好用、更符合安同 OS 用户的需要：其中，我们大幅度增强了软件包与系统特性保护功能、为操作内容阅读器新增了搜索功能、翻修了软件源镜像管理器的界面，还对无用软件包清理、非交互模式界面和诸多 oma 子命令进行了增强和优化。

让我们一起了解本次 oma 特性更新带来的各种新功能和修复吧！

[阅读更新日志 >>](20241031-oma-1.12-relnote.zh_CN.md)

### 安同 OS RISC-V 版首个开发板镜像：赛昉科技 VisionFive 2

![VisionFive 2 图例（图源：赛昉科技）](/coffee-break/20241103/imgs/visionfive-2.jpg)
> VisionFive 2 图例（图源：赛昉科技）

近日，随着[Errant](https://github.com/Errant404)  的“开源之夏 2024”项目[“为 RISC-V 开发板提供安同 OS 系统镜像”](https://summer-ospp.ac.cn/org/prodetail/24f3e0162)顺利结项，[aoscbootstrap](https://github.com/AOSC-Dev/aoscbootstrap) 及 [aosc-mkrawimg](https://github.com/AOSC-Dev/aosc-mkrawimg) 新增了赛昉科技 (StarFive) JH7110 SoC 平台支持。

这意味着我们将于近期发布为 VisionFive 2 量身定做的系统镜像，敬请期待！

开发者角
--------

### Autobuild4 4.4.0 发布

经过数个月的维护，[Autobuild4](https://github.com/AOSC-Dev/autobuild4) 终于迎来了第一个特性更新：4.4.0。

该版主要引入由[杨欣辉](https://github.com/Cyanoxygen)开发的 [Glibc 微架构 HWCAPS](https://hackweek.opensuse.org/projects/support-glibc-hwcaps-and-micro-architecture-package-generation) 打包支持，该特性将为 Core 12 引入 HWCAPS 多运行时提供支持。

有关该新特性的使用方式，请见杨欣辉编写的 [HWCAPS 打包指南](https://wiki.aosc.io/zh/developer/packaging/hwcaps-packaging-guide/)。

### ACBS 及 abbs-update-checksum 引入 pypi:: 源码类型支持

近日，为解决 PyPI 稳定源码链接 (`https://pypi.io/.../`) 高度模式化且不易获取的问题，[Student Main](https://github.com/stdmnpkg) 为 [ACBS](https://github.com/AOSC-Dev/acbs) 实现了 `pypi::` 源码类型，大幅度简化 PyPI 源码配置的编写，如下例中 `lang-python/certifi` 的 `spec` 文件：

```bash
VER=2024.7.4
SRCS="tbl::https://pypi.io/packages/source/c/certifi/certifi-$VER.tar.gz"
CHKSUMS="sha256::5a1e7645bc0ec61a09e26c36f6106dd4cf40c6db3a1fb6352b0244e7fb057c7b"
CHKUPDATE="anitya::id=7995"
```

可改写为：

```bash
VER=2024.7.4
SRCS="pypi::version=$VER::certifi"
CHKSUMS="sha256::5a1e7645bc0ec61a09e26c36f6106dd4cf40c6db3a1fb6352b0244e7fb057c7b"
CHKUPDATE="anitya::id=7995"
```

为适配该新源码类型，[傅孝元](https://github.com/eatradish)发布了包含相关支持的 [abbs-update-checksum](https://github.com/AOSC-Dev/abbs-update-checksum) 0.3.0。

### 断舍离：pkg-prune.rkt 及 dropit 工具

维护发行版仓库，怎能少得了断舍离？

在某个软件失去维护，维护者失去耐心时，安同 OS 往往会选择抛弃某个软件包的维护。那么，要怎样简化“给软件包办退休”的过程呢？[繁杂绪 (OriginCode)](https://github.com/OriginCode) 和[张丙戊](https://github.com/xtexChooser)给出了各自的答案——二者目标一致，但工作模式相反：

- [pkg-prune.rkt](https://github.com/AOSC-Dev/scriptlets/blob/master/pkg-prune.rkt)，使用 Racket 实现；该工具用于在删除某个软件包时，以之作为端点，递归清理因删除该软件包后新增的，无逆向依赖的软件包
- [dropit](https://github.com/AOSC-Dev/scriptlets/tree/master/dropit)，使用 Bash 实现；与 [pkg-prune.rkt](https://github.com/AOSC-Dev/scriptlets/blob/master/pkg-prune.rkt) 相反，该工具在从 [aosc-os-abbs](https://github.com/AOSC-Dev/aosc-os-abbs) 等打包脚本树中删除某个软件包时，同时查询其反向依赖并一并提交删除

爽不？有“断舍离”需求的安同 OS 维护者们不妨一试。

### 打包生成，前进四！Ciel、ACBS 及 aoscbootstrap 默认开启 Unsafe I/O 选项

dpkg 包管理以其对可靠性的重视著称，其中一环便是在安装、卸载和更新软件包时引入大量的文件同步和备份操作。虽然这一设计对用户的系统长久稳定有积极意义，但对于我社数个需要频繁进行大量包管理操作的容器管理、打包和发行版生成工具来说，无疑是徒增了开发者的等待时间。

随着 [oma](https://github.com/AOSC-Dev/oma) 1.12 的发布，[傅孝元](https://github.com/eatradish) 引入了  `--force-unsafe-io` 选项，禁用所有“安全 I/O”功能，可大幅度包管理操作的速度。而后，她为我社的 [Ciel](https://github.com/AOSC-Dev/ciel-rs) 容器管理工具、[ACBS](https://github.com/AOSC-Dev/acbs) 半自动打包工具及 [aoscbootstrap](https://github.com/AOSC-Dev/aoscbootstrap) 发行版生成工具均默认开启了这一选项，相信可大幅度提高上述工具的使用效率。

### 红花榜

感谢在过去一期中参与 AOSC 项目开发和维护工作的各位同事：

- [BC204](https://github.com/BC204)
- [Henry Chen](https://github.com/chenx97)
- [柴天浩](https://github.com/cthbleachbit)
- [杨欣辉](https://github.com/Cyanoxygen)
- [傅孝元](https://github.com/eatradish)
- [Errant](https://github.com/Errant404)
- [Zixuan "Lain" Yang](https://github.com/Fearyncess)
- [德州润华](https://github.com/HouLiXieBuRou)
- [Icenowy Zheng](https://github.com/Icenowy)
- [Ivan Maidanski](https://github.com/ivmai)
- [陈嘉杰 (jiegec)](https://github.com/jiegec)
- [Kexy Biscuit（百合ヶ咲るる）](https://github.com/KexyBiscuit)
- [leavelet](https://github.com/leavelet)
- [刘子兴](https://github.com/liushuyu)
- [白铭骢](https://github.com/MingcongBai)
- [繁杂绪 (OriginCode)](https://github.com/OriginCode)
- [ouankou](https://github.com/ouankou)
- [Outvi V](https://github.com/outloudvi)
- [SignKirigami](https://github.com/prcups)
- [王江津](https://github.com/RedL0tus)
- [Rick Liu](https://github.com/rickliu2000)
- [王邈](https://github.com/shankerwangmiao)
- [Sharelter](https://github.com/Sharelter)
- [shatian114](https://github.com/shatian114)
- [SkyBird233](https://github.com/SkyBird233)
- [Student Main](https://github.com/stdmnpkg)
- [Suyun](https://github.com/Suyun114)
- [张丙戊](https://github.com/xtexChooser)
- [温柔](https://github.com/xunpod)

此外，欢迎新加入我社贡献者行列的新人，愿合作愉快，共同进步：

- [AydenMeng](https://github.com/AydenMeng)
- [black-desk](https://github.com/black-desk)
- [CAB233](https://github.com/CAB233)
- [lunzima](https://github.com/lunzima)
- [Alan Lin](https://github.com/miwu04)
- [pch666777](https://github.com/pch666777)
- [🍉](https://github.com/suica-me)
- [wxiwnd](https://github.com/wxiwnd)

一起吹水
--------

<details>
    <summary>点此查看进群说明，一起吹水玩耍吧~</summary>

互联网是我社的主要活动场所，欢迎来社区各群聊及语音频道交流玩耍：

### 微信群

请扫描此二维码添加好友**并说明来意：申请加入 AOSC 社区频道。**

![wechat](/assets/wechat.png)

### QQ 群

![qq](/assets/qq.jpg)

### Telegram 群组

![telegram](/assets/telegram.png)

### Discord 语音频道

![discord](/assets/discord.png)
</details>

栏目介绍
--------

考虑到社区项目和文化等日趋成熟，我们决定重启外联和宣传工作，在更广阔的天地寻找志同道合的朋友。

您阅读的本期半月刊即是我们外宣工作的一部分，我们的文字宣传栏目如下：

- 安记冰室：社区双周报及访谈栏目
- 聊斋：信创及稀见软硬件专题
- 怀古：古董软硬件专题
- 实况：各类线下活动资讯

其中，《安记冰室》于北京时间 (UTC+8) 每月第二、四个周末发布，其他栏目均视讯息内容及编辑进展发布；发布平台包括：

- 社区门户
- 微信公众号“安同开源”
- Bilibili 帐号“安同开源社区”
- 微博帐号 @安同开源
- Twitter/X @aosc_dev_cn 及 @aosc_dev（英文）

此外，我们正寻求国内开源及 Linux 相关媒体的朋友合作，一起将我社的工作和文化广而告之。
