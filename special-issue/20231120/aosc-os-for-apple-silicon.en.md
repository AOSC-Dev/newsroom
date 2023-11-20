AOSC OS for Apple Silicon Now Available
====

![AOSC OS at the Apple Startup Manager.](/special-issue/20231120/imgs/apple-silicon.jpg)

AOSC OS for Apple Silicon is now available for most M1 or M2 based Macs. This
round of release will work out of the box on most M1-based systems[^1], with
the exception of OpenGL[^2] and Thunderbolt[^3], the internal storage, ports,
audio, Wi-Fi, and webcam should work out of the box. Support for M2 devices is
currently work-in-progress[^4] and M3 support will be coming soon.

On macOS Ventura (13) or newer, use following command in terminal to install
AOSC OS:

```
curl https://releases.aosc.io/install-asahi | sh
```

Should you run into any issues whilst installing or using AOSC OS, please
[file an issue](https://github.com/AOSC-Dev/aosc-os-abbs/issues/new?assignees=&labels=&projects=&template=bug-report.yml) 
or get in touch with us via the channels listed below.

Get in Touch
----

At AOSC, we strive to provide and maintain a easy and pleasant experience for our users. We welcome you at our community chat groups to share your experience, or to [report problems](https://github.com/AOSC-Dev/aosc-os-abbs/issues/new?assignees=&labels=&projects=&template=bug-report.yml) that you may have experienced while using AOSC OS. 

### Telegram

![telegram](/special-issue/20231120/imgs/telegram.png)

### Discord

![discord](/special-issue/20231120/imgs/discord.png)

### WeChat

Please scan this QR code and note that you would like to join our community chat group.

![wechat](/special-issue/20231120/imgs/wechat.png)

### QQ

![qq](/special-issue/20231120/imgs/qq.jpg)

----

[^1]: Due to [an macOS issue](https://github.com/AsahiLinux/docs/wiki/macOS-Sonoma-Boot-Failures), you may not be able to install AOSC OS on 14" or 16" MacBook Pro models with ProMotion displays.
[^2]: OpenGL support will be added with Mesa 24, this version is expected to be released later this year or in early 2024.
[^3]: Thunderbolt support is not currently planned.
[^4]: To see the progress on M2 support, please refer to Asahi Linux's [project documentation](https://github.com/AsahiLinux/docs/wiki/M2-Series-Feature-Support)。
