# 小熊猫包管理 (oma) v1.3.29 更新日志

- 使用了新版 oma-apt (Rust apt binding），更加多的 C++ 空指针检查，减少崩溃几率
- 修复了当历史数据库存在 oma undo 条目时，再执行 oma undo 会发生 undo 列表错位的问题（感谢 [@GGN_2015](https://t.me/GGN_2015) 提交 Bug！）
