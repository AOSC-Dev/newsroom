[arkadijs]: https://github.com/arkadijs
[ziyao233]: https://github.com/ziyao233

# 小熊猫包管理（oma）v.1.3.33 更新日志

— 添加使用 SHA-512/MD5 校验的 APT 软件源支持，oma 可搭配更多第三方源使用了
— 添加 sources.list 中使用 $(ARCH) 变量的支持（感谢 [Arkadi Shishlov][arkadijs] 的特性请求！）
— 修复 oma list 输出给 less 时，如输出未完成时中途退出 less 界面则 oma 会崩溃的问题（感谢 [Arkadi Shishlov][arkadijs] 的问题报告！）
— 在无图形环境的情况下禁用 PolicyKit 交互提权，以适应 TTY/SSH/WSL 等环境下 pkexec 无法提权的问题（感谢 [ziyao233][ziyao233] 的问题报告！）
— 修复 oma topics 界面的样式（1.3.32 调整样式时未给分支名加括号）
