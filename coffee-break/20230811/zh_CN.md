安记冰室·创刊号
================

“你地饮滴咩呀——”

欢迎阅读安同开源社区 (AOSC) 双周报《安记冰室》的创刊号！《安记冰室》旨在以轻松可及的方式，以图文形式介绍过去两周的开发进展、社区事务与近期社区内外活动资讯。此外，本栏目还用于发布与社团及行业人士及代表的访谈录，以特辑形式发布。本栏目不发表评论性内容。

AOSC OS 快讯
------------

在过去两周中，社区开发者们除继续对 [AOSC OS](https://aosc.io/zh-cn/downloads) 进行日常维护外，还为系统引入了许多更新、修复，推进了系统周边组件的开发，希望这些工作能为您的工作与娱乐生活带来便利。

### 初识 Omakase

我们为 AOSC OS 量身定做的包管理前端 [Omakase](https://github.com/AOSC-Dev/oma) 正式进入主源，并将跟随 `admin-base`（管理套件）软件包的更新自动安装。Omakase 的主要设计目标有：

- **改善 APT 的界面：**让界面指引、报错及操作逻辑更为简洁易懂
- **增强防呆机制：**通过清晰的指引和操作撤销等机制，助您避免因粗心或其他原因造成系统故障，进而浪费时间和精力
- **优化网络性能：**使用 HTTP/2 和多线程下载等技术，大幅度加快软件包安装与更新
- **提升使用效率：**优化子命令布局，增强搜索功能，让您的系统管理体验更轻松明晰

![oma-screenshot](/coffee-break/20230811/imgs/omakase.png)

快更新系统，输入 `oma` 命令体验 AOSC OS 的全新包管理吧！Omakase 目前处在 1.0 的初期开发阶段，有许多[新特性与设计](https://repo.aosc.io/aosc-documentation/aoscc-2023/magmell/omakase.pdf) 仍在规划当中，欢迎您就使用体验或问题，向我们提出批评建议或[提交问题报告](https://github.com/AOSC-Dev/oma/issues/new)！

Omakase 基于来自 Debian 的 [APT](https://wiki.debian.org/zh_CN/Apt) 开发，并保持与 AOSC OS 先前使用的 APT 功能与行为兼容。为照顾 AOSC OS 老用户的使用习惯，我们将继续在系统中预装 APT，与 Omakase 共存。

### LiveKit 尺寸优化

虽说 AOSC OS 的丰满尺寸早已臭名昭著，但除了确保系统特性齐全和组件简化外，优化系统尺寸亦是改善用户体验的重要一环。

月初，杨欣辉 (GitHub: [@Cyanoxygen](https://github.com/Cyanoxygen)) 针对 LiveKit（AOSC OS 标准启动与安装环境）的生成脚本[提交了一项改进](https://github.com/AOSC-Dev/aosc-mklive/commit/8339e1879cfe113bedcc3b30539057be50315677)，删除不常用字体和文档数据。通过此项改进，后续发布的 LiveKit 镜像将减重约 200~300MiB。

![livekit-screenshot](/coffee-break/20230811/imgs/livekit.png)

### AOSC OS/Retro 系统发布

如果您手上还有舍不得扔掉的古董电脑，我们针对老旧设备优化的 AOSC OS/Retro 系统可助您重新为这些设备“续命”，找到新的用途。七月底，我们发布了 AOSC OS/Retro 的正式版，目前支持 32 位 x86 设备。只需 128MiB 内存、3GiB 硬盘空间和 VGA 显示卡，您就可以享受完整的 AOSC OS/Retro 体验（小声说一句：如果您愿意手动安装基本系统，AOSC OS/Retro 在搭载 32MiB 内存、500MiB 硬盘的 486 机器上就能运行）！

![retro-screenshot](/coffee-break/20230811/imgs/retro.png)

兼容其他架构的 AOSC OS/Retro 将于今年内陆续发布，为您手上的各类稀奇古怪设备提供持续软件支持，敬请期待！

### 更新速览

过去两周中我们为 AOSC OS 推送了许多更新，这里简要介绍其中几项：

- Neofetch 更新至 7.3.9，修复了 AArch64 设备上处理器型号错误显示为“Yes”的问题
- 修复了 WPS Office 在 AArch64 设备上无法启动的问题
- 修复了中州韵 (RIME) 输入法在 AArch64 设备上无法使用的问题
- 修复了 htop 无法正确处理 CPU 核心下线状态的问题
- Fcitx 的萌娘百科词库 ([fcitx-pinyin-moegirl](https://github.com/outloudvi/mw2fcitx)) 更新至 20230714，引入许多新词
- FeelUOwn 播放器更新至 3.8.13，引入 Bilibili 搜索与播放插件
- Blender 更新至 3.6，包含大量用户界面与新功能
- 新增 [Ouch](https://github.com/ouch-org/ouch)，一站式命令行压缩包管理工具

### 尝鲜预报

为更好地测试我们的系统更新，我们为不同类别的更新打开相应的测试源，供用户与贡献者测试。本周，我们新增了如下几个测试源：

- **AOSC OS Core 11 (`core-k`)：**更新系统核心运行时，将 Glibc 更新至 2.37，GCC 更新至 13.2.0，Linux API 头更新至 6.4.7，Zstd 更新至 1.5.5
- **Linux Kernel 6.4 (`linux-6.4.x`)：**将 Linux 内核更新至 6.4，改进硬件支持；其中，此更新还修复了 12 代 Intel/NVIDIA 双显卡无法启动图形界面的问题，并改善了对华为擎云系列台式机的兼容性
- **LLVM 16 与 Rust 1.71 (`llvm-16.0.4`)：**引入 LLVM 16 和 Rust 1.71 及其众多新特性，修缮了龙芯 1000~4000 系列支持，并为 IBM POWER 架构新增了 D 语言支持
- **OpenSSL 3.1.1 (`openssl-3.1.1`)：**引入 OpenSSL 3.1.1 以替代老旧的 OpenSSL 1.1 运行时

这些测试源也将同步至我们的龙架构 (LoongArch) 前沿分支，并为将龙架构引入作为 AOSC OS 正式支持的架构作准备。

输入如下命令随时加入或退出测试源：

```
sudo oma topics
```

如果您在使用如上测试源的过程中遇到问题，请随时联系我们，我们将尽力协助您修复问题。

社区快讯
--------


招工启示
--------


一起吹水
--------