[jeffbai]: https://github.com/MingcongBai
[cyanoxygen]: https://github.com/Cyanoxygen
[ggn_2015]: https://github.com/GGN-2015

# 小熊猫包管理（oma）v1.3.32 更新日志

— 修复了 oma topics 命令修改过后的 atm.list 文件头注释末尾不带换行符的问题（感谢 [@JeffBai][jeffbai] 修复！）
— 修复了 oma refresh 刷新非安同 OS 源时刷新信息显示不正确的问题
— 修复了仅 Release 源不指定 trusted=yes ，也能刷新成功的问题
— 修复了当使用 oma install 安装软件包时，若指定软件包不存在只打印错误信息，oma 仍继续执行的问题（感谢 [@GGN_2015][ggn_2015] 提交的 Bug！）
— 调整了 oma topics 列表的输出格式与颜色，让界面更加简洁明了（感谢 [@JeffBai][jeffbai] 修复！）
— 修复了在 Wayland 环境下审阅界面不提示可以用鼠标滚动的问题（感谢 [@Smasnug][cyanoxygen] 修复！）
