# 小熊猫包管理（oma）v1.3.34 更新日志

— 修复了使用 oma mirror 添加或删除源时会清空测试源列表的问题，并改进了错误输出
— 修复当元数据缓存中有软件包被删除时 command-not-found 可能会崩溃的问题（感谢 [OriginCode](https://github.com/OriginCode) 提交问题报告！）
— 修复通过 PolicyKit 提权安装本地 .deb 文件时无法将本地包加入缓存的问题（感谢 [白铭骢](https://github.com/MingcongBai) 提交问题报告！）
— 修复 oma topics 会把该不可用的测试源条目写入到 sources.list 的问题
— 改进 date_hack 函数的错误处理逻辑
