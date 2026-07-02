# Anything Analyzer v3.6.51

## 修复

- **macOS Intel 打包架构** — 修复 x64 包内 `better-sqlite3` 原生模块被打成 arm64 的问题
  - macOS x64 与 arm64 现在分别在对应 runner 上构建，避免原生依赖交叉污染
  - 发布前会校验 `better_sqlite3.node` 的实际 Mach-O 架构，架构不匹配时阻断 Release

## 下载

| 平台 | 文件 |
|------|------|
| Windows | Anything-Analyzer-Setup-3.6.51.exe |
| macOS (Apple Silicon) | Anything-Analyzer-3.6.51-arm64.dmg |
| macOS (Intel) | Anything-Analyzer-3.6.51-x64.dmg |
| Linux | Anything-Analyzer-3.6.51.AppImage |
