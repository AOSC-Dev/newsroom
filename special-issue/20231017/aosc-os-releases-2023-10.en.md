Now Available: New Wave of AOSC OS System Releases
====

Recently, we released a new wave of AOSC OS system releases. This wave contains a year's worth of component updates, incorporating routine updates, bugfixes, and enhanced hardware support.

You may obtain AOSC OS from our downloads page: [https://aosc.io/downloads](https://aosc.io/downloads)

![AOSC OS Desktop](/special-issue/20231017/imgs/desktop.en.png)

New Features
----

This wave of update includes many new features and improvements to the default user experience. Most notably, all new system releases now come pre-installed with [Omakase](https://github.com/AOSC-Dev/oma), our in-house package management interface which aims to improve ease-of-use and reliability. The Linux Kernel, as well as the graphical and audio stacks also got refreshed to improve user experience on newer hardware. We have also made updates to key system components, most notably:

- Linux Kernel was updated to the 6.4 branch (6.1 longterm versions also available) to ensure a smooth experience on newer hardware. We have also incorporated additional patches to improve out-of-the-box experience on Microsoft Surface devices, as well as Huawei's Kunpeng 920- and Phytium D2000/8-based devices.
- Core was updated to 11.0.1, boasting the newest core runtime libraries and toolchain, such as Glibc 2.37 with new architecture support and instruction set optimisations, and GCC 13.2.0, which provides support for latest programming language features.
- OpenSSL runtime was updated to 3.1.1 with support for latest cryptographic algorithms, as well as key security enhancements.
- The default browsers also saw updates, such as Mozilla Firefox 117.0.1 and Thunderbird 115.2.2.
- The KDE Plasma desktop was updated to contain newest versions from end of 2022, with interface and performance tweaks and optimisations applied by default.
- Enhanced Shell prompt with SSH connection marker, optimised Git status prompts, and standardised profile scripts.
- More powerful editors, with Vim now pre-installed in addition to GNU Nano.

Architecture Support
----

Free and open source software greatly enhanced portability of software applications and operating systems, making it possible to run them on a wide variety of hardware with varying features and performance metrics. AOSC OS benefits from this great ecosystem. So far, we support a wide range of devices built upon seven (7) processor architectures: AMD64/x86-64, AArch64, MIPS-based Loongson 3 processors (1000-4000 series), MIPS64 Release 6, IBM POWER8+, 64-bit RISC-V, and LoongArch.

This wave of updates offers support for two new architectures:

- LoongArch: We have completed a basic port for this architecture and AOSC OS now works out-of-the-box on "New World Firmware" Loongson 3A5000/3C5000/3C5000L/3A6000-based devices. This port requires components newer than our other supported architectures to function correctly on these devices. In the coming months, we will be working on making these changes available as stable updates for all other architectures.
- MIPS64 Release 6: This port is currently maintained by employees at the CIP United Co., Ltd. and is used as its reference system environment for monitoring and testing software application support for the MIPS64 Release 6 architecture.

We have also rebooted the IBM POWER8+ port, rebuilding it against the new floating-point ABI (IEEE Long Double), enhancing compatibility with current applications and future updates.

### Levels of Architectural Support

To help ensure efficient maintenance and to guide prospective users, we classify our architectural ports into three classes:

- Primary Architectures: Includes AMD64 and AArch64; these architectures enjoy good hardware availability and software support.
- Secondary Architectures: Includes AArch64, MIPS-based Loongson 3 processors (1000-4000 series), MIPS64 Release 6, IBM POWER8+, and 64-bit RISC-V; these architectures come with near-complete mainline software support. However, architectures listed under this class suffer from insufficient computing performance for regular maintenance, or less reliable hardware.
- Tertiary Architectures: LoongArch currently falls into this category; support for these architectures are considered experimental, but may be promoted as secondary, or even primary, architectures, should quality of maintenance and user experience improve.

Get in Touch
----

At AOSC, we strive to provide and maintain a easy and pleasant experience for our users. We welcome you at our community chat groups to share your experience, or to [report problems](https://github.com/AOSC-Dev/aosc-os-abbs/issues/new?assignees=&labels=&projects=&template=bug-report.yml) that you may have experienced while using AOSC OS. 

### Telegram

![telegram](/special-issue/20231017/imgs/telegram.png)

### Discord

![discord](/special-issue/20231017/imgs/discord.png)

### WeChat

Please scan this QR code and note that you would like to join our community chat group.

![wechat](/special-issue/20231017/imgs/wechat.png)

### QQ

![qq](/special-issue/20231017/imgs/qq.jpg)