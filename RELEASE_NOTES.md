# Anything Analyzer v3.6.18

## 修复

- **Responses API 流式失败信息更准确** — 修复 `response.failed` SSE 将嵌套错误消息显示为 `Unknown stream error` 的问题
  - 兼容 `response.error.message` 结构，保留现有顶层 `message` 和 `error.message` 处理
  - 增加嵌套失败事件回归测试，确保模型过载等错误能直接反馈给调用方

## 下载

| 平台 | 文件 |
|------|------|
| Windows | Anything-Analyzer-Setup-3.6.18.exe |
| macOS (Apple Silicon) | Anything-Analyzer-3.6.18-arm64.dmg |
| macOS (Intel) | Anything-Analyzer-3.6.18-x64.dmg |
| Linux | Anything-Analyzer-3.6.18.AppImage |
