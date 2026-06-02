# Anything Analyzer v3.6.39

## 修复

- **OpenAI 工具调用参数校验** — 避免非字符串 arguments 被当作工具执行错误吞掉
  - 工具调用入站阶段直接拒绝 arguments 非字符串的畸形 tool_call
  - 新增回归测试覆盖 OpenAI tool_call 参数类型异常路径

## 下载

| 平台 | 文件 |
|------|------|
| Windows | Anything-Analyzer-Setup-3.6.39.exe |
| macOS (Apple Silicon) | Anything-Analyzer-3.6.39-arm64.dmg |
| macOS (Intel) | Anything-Analyzer-3.6.39-x64.dmg |
| Linux | Anything-Analyzer-3.6.39.AppImage |
