AOSC OS 发布新一批系统发行
====

近日，我们发布了新一批 AOSC OS 系统发行，包含一年以来的系统组件更新，在引入更新和修复系统中存在的问题的同时，还改善了硬件支持。

前往我社下载页面即可获取 AOSC OS：[https://aosc.io/zh-cn/downloads](https://aosc.io/zh-cn/downloads)

![AOSC OS 默认桌面](/special-issue/20231017/imgs/desktop.zh_CN.png)

系统特性
----

本次发行更新囊括许多新特性和使用体验改进，其中最为明显的是新增了社区开发的 [Omakase 软件包管理前端](https://github.com/AOSC-Dev/oma)，改善管理系统组件的易用性和可靠性；更新了内核、图形栈、音频栈等关键硬件支持组件，确保在新硬件上的使用体验；我们也对系统各关键组件进行了修缮和更新，主要的几项有：

- Linux 内核更新至 6.4 分支，同时提供 6.1 长期支持分支，确保新硬件上的系统体验；另有引入一系列针对 Microsoft Surface、华为擎云 W510 和飞腾 D2000/8 系列设备的补丁，改善这些设备上的开箱使用体验
- Core 11.0.1，包含最新核心运行时库及工具链，如包含更多架构支持及指令集优化的 Glibc 2.37 和支持各类最新的语言特性的 GCC 13.2.0
- 引入 OpenSSL 3.1.1 运行时，包含最新的算法库及安全修复
- 更新预装浏览器套件，包括 Mozilla Firefox 117.0.1 及 Thunderbird 115.2.2
- KDE Plasma 桌面套件更新，包含截至 2022 年底的最新版本，对默认使用体验和性能进行了调优
- 增强默认命令提示符功能，如增加 SSH 远程命令行标记、优化 Git 提示符和规范化启动脚本等
- 增强默认编辑器功能，在 GNU Nano 的基础上附加预装 Vim 编辑器

架构支持
----

开放与自由源代码授权大大提升了软件乃至操作系统的可移植性，让这些软件得以运行在许多不同种类、性能各异的硬件上。得益于此，AOSC OS 共支持基于 7 个处理器架构的设备：AMD64/x86-64、AArch64、基于 MIPS 的龙芯三号处理器（1000 ~ 4000 系列）、MIPS64 Release 6、IBM POWER8+、64 位 RISC-V 和龙架构 (LoongArch)。其中，本轮发行中包含两个新架构移植：

- 龙架构 (LoongArch)：目前该架构已完成基本移植，可在搭载“新世界固件”的龙芯 3A5000/3C5000/3C5000L/3A6000 设备上开箱即用；由于该架构较新，该架构系统包含较其他架构版本新的系统组件，在后续几个月中，这些更新将合并到主线架构的稳定源中，成为正式架构
- MIPS64 Release 6：此架构由上海芯联芯智能科技有限公司职工维护，目前在该公司作为基准环境，用于监测 MIPS64 Release 6 软件应用生态支持情况

此外，我们还重启了 IBM POWER8+ 的架构移植，将其基于新浮点二进制接口规范 (IEEE Long Double) 重构，改善应用与后续组件更新的兼容性。

### 架构分类

为确保系统维护效率和更好地引导用户选用 AOSC OS，我们将支持架构分为三个级别：

- 一级架构 (Primary Architecture)：包括 AMD64 和 AArch64，此类架构硬件可用性良好且主线软件支持基本完备
- 二级架构 (Secondary Architecture)：包括基于 MIPS 的龙芯三号处理器（1000 ~ 4000 系列）、MIPS64 Release 6、IBM POWER8+ 和 64 位 RISC-V；此类架构主线软件支持基本满足标准特性要求（必要时有删减），硬件时有可靠性问题且维护算力不足
- 三级架构 (Tertiary Architecture)：目前包括龙架构 (LoongArch)；此类架构属于实验性移植，在维护质量提高和系统使用体验基本稳定后会升格为二级、甚至一级架构

常联系
----

我们十分重视 AOSC OS 的使用体验，欢迎来我社各聊天群组分享使用体验或于我们的源码仓库[报告问题](https://github.com/AOSC-Dev/aosc-os-abbs/issues/new?assignees=&labels=&projects=&template=bug-report.yml)，我们将尽一切努力持续为您营造轻松愉快的使用体验。

### 微信群

请扫描此二维码添加好友并说明来意：申请加入 AOSC 社区频道。

![wechat](/special-issue/20231017/imgs/wechat.png)

### QQ 群

![qq](/special-issue/20231017/imgs/qq.jpg)

### Telegram 群组

![telegram](/special-issue/20231017/imgs/telegram.png)

### Discord 语音频道

![discord](/special-issue/20231017/imgs/discord.png)