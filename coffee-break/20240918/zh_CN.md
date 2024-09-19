安记冰室・九月上
=============

<!-- 兜售月饼的 -->

> “豆沙、莲蓉、五仁、火腿、鲜肉和枣泥月饼诶，摆一桌嘞——”

欢迎阅读安同开源社区 (AOSC) 期刊《安记冰室》！本栏目旨在以轻松可及的方式，以图文形式介绍过去两周的开发进展、社区事务与近期社区内外活动资讯。此外，本栏目还用于发布与社团及行业人士及代表的访谈录，以特辑形式发布。本栏目不发表评论性内容。

用户公告
--------

### 速更新！安同 OS 离线安装盘意外安装预制 SSH 主机密钥

![OpenSSH 组件更新时的安全警告示意图](/coffee-break/20240918/imgs/openssh-advisory.png)

由于离线安装盘生成工具中的清理流程设计疏忽，自六月底开始发行的安同 OS 离线安装盘（即文件名由 `aosc-os_installer` 开头的 ISO 镜像）所包含的系统镜像均未正确清理 SSH 主机密钥，致使安装后的系统中亦使用了该主机密钥。

考虑到安同 OS 默认开启 SSH 服务，该疏忽恐严重影响用户安全：这些密钥可能导致其它主机能够冒充您的主机的身份，从而窃取您的登入口令和与主机之间的 SSH 会话的内容。但是，如果您使用 SSH 公钥作为登入凭据，则不受影响。

为此，我们紧急发布了 OpenSSH 更新（版本 `9.8p1-4`）修补这一问题：在匹配到已知泄漏的主机密钥的密码学指纹 (fingerprint) 时，将清理并重新生成系统中的 SSH 主机密钥。**如有可能，请尽快更新安同 OS，以免存留安全隐患。**

**请注意：更新完成后，AOSC OS 将重启 SSH 服务守护程序，但不会影响当前已经建立的 SSH 连接；如果您对外提供 SSH 服务，您的用户在连接受影响的 SSH/SCP/SFTP 服务时可能会遇到连接错误。因此，您可能需要将有关情况告知您的用户，并引导他们删除先前信任的 SSH 主机密钥记录。**

我们为此带来的不便表示歉意。

社区脉动
--------

### 携手社团：秋季安同 “校园行” 活动前瞻

在今年开春的甲辰烙饼会上，社区提出了安同 “校园行” 活动的设想：深入大学校园，通过学生社团为大学学生和行业上的一线开发者、社区贡献者之间建立沟通的桥梁，埋下参与社区与开源软件贡献的种子。今年三月，社区成功在曲阜师范大学举办了[第一次安同 “校园行”](https://website-2023.aosc.io/news/detail/2024-03-20-qfnu-computing-evolved.zh-cn.md)活动。

“校园行”成功迈出的第一步激起了一批院校的兴趣。因此，安同 “校园行” 活动计划将在十月国庆假期后重启，让更多高校学生接触社区、了解开源和融入贡献者群体。国庆假期后的第一次 “校园行” 活动预计在宁夏理工学院举办，届时将邀请社区贡献者及行业一线工作者前往与社团学生们互动。

至截稿时，兰州大学、山东大学与南阳理工学院等院校的开源与计算机社团们也表达了承办 “校园行” 的意愿。同时，我们也诚邀国内各个院校的计算机社团与我们一起举办 “校园行” 活动。

“校园行” 活动为志愿性质且活动形式灵活，因此社团无需提供资金方面的支持，也可根据需要提出活动形式及演讲主题等。如果您是社团负责人且有意承办“校园行”活动，欢迎[与我们联系](https://website-2023.aosc.io/contact)！

系统快讯
--------

### 集社区之精华：安同 OS 发布九月发行更新

![庆中秋，安同 OS 发布九月发行更新](/coffee-break/20240918/mid-autumn-aosc-os.png)

新一批安同 OS 系统发行更新来啦！

本批发行更新包含自 8 月初以来的各类系统组件更新及安全修复，亦包括针对 Hyper-V、VMware 及 VirtualBox 等虚拟化平台、较新 x86 设备及龙架构平台的功能及支持优化；我们还针对系统安装体验和可靠性进行了大量调优和修复

#### 下载系统

新网站上线在即，我们将完整的发行注记随新的下载页面一同发布，来一睹为快吧~

- [下载安同 OS](https://website-2023.aosc.io/download)
- [查阅发行注记（2024 年 9 月）](https://website-2023.aosc.io/aosc-os/relnote)

### 界面再升级：小熊猫包管理 oma 发布 1.10 

![轻松管，轻松用：oma 助您便捷完成系统组件管理](/coffee-break/20240918/imgs/oma-comic-slim.png)

日前，[傅孝元](https://github.com/eatradish)发布了小熊猫包管理 (oma) 的 1.10 。

本次更新着重对小熊猫包管理的确认界面、表格排版等逻辑进行了优化，在各种不同的终端环境中界面更清晰、好用。“找不到命令 (command-not-found)”界面的设计也进行了调整，在结果较多时对搜索候选的数量进行限制，并引导用户查阅完整列表。

此外，本版还针对 Debian/Ubuntu 用户使用过程中遇到的性能及界面问题进行了针对性调优：如根据这些发行版软件仓库较大的情况，降低了软件包搜索功能的索引复杂度，也对其他需要等待的界面添加了等待提示

oma 1.10 是基于 1.10 RC1 测试后发布的，相对于 1.9 还包含许多细节修复与调整。欢迎各位查阅 [1.10 RC1 的测试公告](1.10-rc1-relnote.md) ，了解 1.10 新特性与修复的技术细节。

#### 安装指南

oma 1.10 已推送安同 OS 稳定源，更新系统即可获取 oma 1.10 ；我们亦同步将 oma 更新推送到了我们的 Debian/Ubuntu 软件源中

运行如下命令即可配置软件源并自动安装 oma，后续可通过更新系统自动获取 oma 更新：

```bash
curl -sSf https://repo.aosc.io/get-oma.sh | sudo sh
```

oma 目前支持的 Debian 及 Ubuntu 版本如下：

- Debian 12
- Debian 11
- Ubuntu 24.04 LTS
- Ubuntu 22.04 LTS
- Ubuntu 20.04 LTS

### 新增 glibc 2.40 及 Linux 6.11 支持：libLoL 0.1.6 发布

![libLoL 持续助力龙架构新世界生态迁移！](/coffee-break/20240918/imgs/liblol.png)

近日，[王邈](https://github.com/shankerwangmiao)发布了安同 OS 龙架构新旧世界兼容框架 libLoL 的 0.1.6 版本。该版本更新顺应了 Debian 的 Glibc 更新和新的内核版本。本次更新主要包含如下内容：

- 适配 glibc 2.40，以应对来自 Debian 的更新需求
- 适配 Linux 6.11，同时将 `lxstat64()` 系统调用的实现切换至基于 `statx()` 调用的实现。

有关更多信息，请参考 [libLoL 0.1.6 更新日志](https://github.com/AOSC-Dev/liblol-website/commit/a7eaead08a52e3cc586973e313da0a50e976d0c9)。

### 改善多媒体支持：FFmpeg 7.0 更新开放测试

由于维护人力不足且部分应用程序的 FFmpeg 特性升级迁移困难较大，安同 OS 的多媒体编解码库 FFmpeg 依旧处于 4.4 版本。该版本距今已经有三年历史，许多媒体格式的编解码器功能、性能及硬件支持上的短板日益凸显。

由于保持旧版 FFmpeg 使得大部分多媒体软件更新日益困难，社区近日将 FFmpeg 更新到了 7.0 版本，相信能够显著提高 AV1 等新兴多媒体格式及各类新硬件的支持水平。您可以通过在小熊猫包管理器中打开 `ffmpeg-7.0` 测试源以尝鲜本次 FFmpeg 大翻修：

```
oma topics --opt-in ffmpeg-7.0
```

如果您在加入本测试源后遇到了问题，欢迎通过文末的各联系方式与我们联系！
 
### WSL 安同 OS 发布 11.5.2 版更新

近日，[Kexy Biscuit](https://github.com/KexyBiscuit) 发布了 WSL 安同 OS 的 11.5.2 版，包含近期发布的各类系统更新与修复（详细变更可参阅本期“集社区之精华：安同 OS 发布九月发行更新”一节的内容）。

如果您日常使用 Windows 工作，相信安同 OS 能为您的生产力环境添彩。

开发者角
--------

### aosc-mklive 更新：离线安装盘支持、综合修复及安全性优化

由于安同 OS “不拆包” 的特性，安同 OS 的安装盘体积过于庞大，且没有包含系统包，常受用户诟病。数月前，[白铭骢](https://github.com/MingcongBai)提出利用分层文件系统 OverlayFS 实现集成系统包的安装介质的构想，[杨欣辉](https://github.com/Cyanoxygen)随后开始探索其实现，[Kexy Biscuit](https://github.com/KexyBiscuit) 在此期间积极测试并提供了诸多反馈。

经过三个月的开发及测试，安同 OS 安装盘生成套件 [aosc-mklive](https://github.com/AOSC-Dev/aosc-mklive) 终于迎来了集成系统包的离线安装盘支持，同时正式发布第一批安同 OS 离线安装盘。新的安装盘利用 OverlayFS 的叠加机制，尽可能抽离了共用的系统组件，并利用 SquashFS 实现较高的压缩率，提高发行空间效率。与此同时，基于 EROFS 文件系统的安装盘也在积极开发及测试中，预计基于 EROFS 的安装盘相对于 SquashFS 启动、安装速度更快，使用体验更佳。

发布前夕，[Kexy Biscuit](https://github.com/KexyBiscuit) 在测试安装盘时发现大量可用性及安全性问题，其中包括前文提到的 SSH 主机密钥问题。自上次发布的 20240801 版安装盘以来，本次发布的安装盘主要包含如下变更：

- 支持龙架构旧世界固件引导安同 OS 安装盘
- 修复带有 Optimus 功能的多显卡设备支持
- 以基于新 DeployKit 后端编写的新命令行安装程序 [dkcli](https://github.com/AOSC-Dev/dkcli) 取代旧的命令行安装程序
- 为安装及试用环境禁用屏幕节电及自动睡眠等电源功能，避免产生意外故障
- 采取措施避免生成安装盘时预生成 SSH 主机密钥
- 删除预设的 `live` 用户密码
- 将内存检测工具 Memtest86+ 升级至 7.00 
- 新增救援与修复控制台（命令行安装环境）说明文字的简体中文翻译

### Ciel 3.4.3 发布：默认使用小熊猫包管理 (oma)

作为安同 OS 的默认包管理功能，小熊猫包管理 (oma) 颇受用户青睐，并已经支持其他基于 dpkg 及 APT 包管理体系的发行版。然而，安同 OS 打包容器管理器 Ciel 依旧在使用 APT 安装依赖。为了让 Ciel 也能享受到 oma 支持多线程下载且性能较好的特性，[傅孝元](https://github.com/eatradish)近日将 Ciel 使用的默认包管理器由 APT 切换到 oma。为了确保打包的可靠性，本项特性没有应用到 RISC-V 及 QEMU 用户态模拟等已知会出现稳定性问题的平台。

如有必要，各位开发者依旧可以通过 `force_use_apt` 配置项或指定 `--force-use-apt` 参数临时将默认包管理器切换为 APT。

### BuildIt! 功能性修复一览

作为安同 OS 自动化维护设施的核心组件，[BuildIt!](https://github.com/AOSC-Dev/buildit) 的使用体验及功能颇受贡献者关注。

日前，[Kexy Biscuit](https://github.com/KexyBiscuit) 修复了几个参数名冲突的问题，[傅孝元](https://github.com/eatradish)通过增加进程锁修复了 `/openpr` 命令执行时的潜在竞态条件，并更新 `abbs-update-checksum` 组件，修复了多源码配置的解析（`/bump` 功能）。此外，根据贡献者请求，[白铭骢](https://github.com/MingcongBai)根据 Git 分支及引用名规则，将 `_` 字符加入了分支名字符白名单中。

### p-vector-rs 0.6.0 发布：改善 Debian 源支持、新增 Zstd 元数据压缩支持

在搭建 oma 的 Debian/Ubuntu 更新源的过程中，安同 OS 维护者发现了数个 [p-vector-rs](https://github.com/AOSC-Dev/p-vector-rs)（APT 软件源刷新与发布工具）中的兼容性问题。为此，[傅孝元](https://github.com/eatradish)与[刘子兴](https://github.com/liushuyu)提交数个补丁，修复了 Debian 软件包元数据文件（如 `control`）不在 `DEBIAN/` 子目录下时刷新出错及部分文件没有记录 UID/GID 时无法完成刷新的问题。

作为 0.6.0 版更新的一部分，[傅孝元](https://github.com/eatradish)还为 `Contents` 元数据文件（软件包内容数据库）引入了 Zstd 压缩支持，可显著降低用户刷新软件源数据的耗时。

### aoscbootstrap 0.7.3 发布：细节修缮

针对本次系统发行更新发布前遇到的问题，我们为 [aoscbootstrap](https://github.com/AOSC-Dev/aoscbootstrap)（安同 OS 系统根及发行包生成工具集）提交了数个修复，并发布了 0.7.3 版。

其中，[Kexy Biscuit](https://github.com/KexyBiscuit) 修缮了 `.sha256sum` 文件的写入逻辑，使其内容与 GNU Coreutils 中对应工具生成的内容一致（先前无法使用 `sha256sum -c` 命令直接进行校验）；[白铭骢](https://github.com/MingcongBai)为清理脚本新增了 SSH 主机密钥的清理逻辑，解决前文提到的密钥泄漏问题。

### abbs-update-checksum 0.2.2 发布：修复多源码配置解析、优化 spec 查询逻辑

[abbs-update-checksum](https://github.com/AOSC-Dev/abbs-update-checksum) 作为安同 OS 自动化设施的一部分，协助 [BuildIt!](https://github.com/AOSC-Dev/buildit) 在 `/bump` 命令过程中刷新源码校验和（亦可直接作为工具使用）。

日前，[张丙戊](https://github.com/xtexChooser)及[傅孝元](https://github.com/eatradish)为该工具提交了数个修复和优化：

- 在软件包树找到第一个匹配 `spec` 时便停止遍历，改善工具响应速度
- 修复刷新多源码 `spec` 时未正确写入对应校验和的问题
- 修复 `-t` (`--tree`) 和 `-t` (`--threads`) 段参数名冲突的问题，新版中 `-t` 为 `--tree` 的别名

### 红花榜

感谢在过去一期中参与 AOSC 项目开发和维护工作的各位同事：

- [salieri](https://github.com/BC204)
- [Henry Chen](https://github.com/chenx97)
- [柴天浩](https://github.com/cthbleachbit)
- [杨欣辉](https://github.com/Cyanoxygen)
- [傅孝元](https://github.com/eatradish)
- [Zixuan "Lain" Yang](https://github.com/Fearyncess)
- [Glenn Strauss](https://github.com/gstrauss)
- [Harry Chen](https://github.com/Harry-Chen)
- [德州润华](https://github.com/HouLiXieBuRou)
- [Icenowy Zheng](https://github.com/Icenowy)
- [Ivan Maidanski](https://github.com/ivmai)
- [陈嘉杰 (jiegec)](https://github.com/jiegec)
- [王翔 (KatyushaScarlet)](https://github.com/KatyushaScarlet)
- [Kexy Biscuit](https://github.com/KexyBiscuit)
- [leavelet](https://github.com/leavelet)
- [刘子兴](https://github.com/liushuyu)
- [lwzhenglittle](https://github.com/lwzhenglittle)
- [白铭骢](https://github.com/MingcongBai)
- [千须末 (OriginCode)](https://github.com/OriginCode)
- [ouankou](https://github.com/ouankou)
- [Outvi V](https://github.com/outloudvi)
- [bubu](https://github.com/p3psi-boo)
- [日落果](https://github.com/purofle)
- [Rick Liu](https://github.com/rickliu2000)
- [王邈](https://github.com/shankerwangmiao)
- [shatian114](https://github.com/shatian114)
- [skybird](https://github.com/SkyBird233)
- [Student Main](https://github.com/stdmnpkg)
- [Suyun](https://github.com/Suyun114)
- [张丙戊](https://github.com/xtexChooser)
- [温柔](https://github.com/xunpod)

此外，欢迎新加入我社贡献者行列的新人，愿合作愉快，共同进步：

- [Errant](https://github.com/Errant404)

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
- 知乎帐号“安同开源社区”
- 微博帐号 @安同开源
- Twitter/X @aosc_dev_cn 及 @aosc_dev（英文）

此外，我们正寻求国内开源及 Linux 相关媒体的朋友合作，一起将我社的工作和文化广而告之。
