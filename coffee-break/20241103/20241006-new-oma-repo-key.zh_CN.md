小熊猫包管理 (oma) 安装源签名刷新公告
===

Ubuntu 24.10 更新了 APT [加密签名算法要求](https://discourse.ubuntu.com/t/new-requirements-for-apt-repository-signing-in-24-04/42854)，而我社先前使用的软件源 GPG 公钥算法 (nistp521) 不符合其要求的：

- 2048 位以上的 RSA
- Ed25519
- Ed448

因此，Ubuntu 24.10、deepin V23 及开放麒麟 (openKylin) 2.0 等使用 APT >= 2.8 版本的发行版无法正常使用我社官方源安装 oma。

为解决该问题，我们已于 UTC+8 时间 2024 年 10 月 6 日生成算法为 Ed25519 的新软件源签名密钥：

```
pub   ed25519 2024-10-06 [SC]
      F54DE04F93DFEDBA123FC2933AE2C2BE062E9F06
uid   AOSC OS Maintainers <maintainers@aosc.io>
sub   cv25519 2024-10-06 [E]
```

我们计划于 UTC+8 时间 10 月 7 日零时切换该源的签名密钥，如果您先前已配置 oma 安装源，您需要重新执行 oma 安装程序：

```bash 
curl -sSf https://repo.aosc.io/get-oma.sh | sudo sh
```

切换签名密钥后，Ubuntu 24.10、deepin V23 及开放麒麟 (openKylin) 2.0 等发行版将可以正常使用上述命令安装 oma。
