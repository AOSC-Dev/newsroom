# 小熊猫包管理（oma）v1.3.31 更新日志

— 添加 oma refresh 执行过程中的读取数据库操作时的进度条
— 添加在 /etc/apt/sources.list 中使用 file:/ 的支持，现在可以使用  file:/ 或 file:/// 指定本地源了
— 修复在 Debian/Ubuntu 及其衍生发行版中打开 multiarch 支持时 oma search 输出中不显示架构名的问题
— 修复在 Debian/Ubuntu 及其衍生发行版中 oma show PKG 中输出 APT-Source 一栏显示不正确的问题
— 修复在 Debian/Ubuntu 及其衍生发行版中，计算出的依赖错误输出中不显示软件包架构的问题
— 修复非 Flat Repo 格式本地软件源的支持
