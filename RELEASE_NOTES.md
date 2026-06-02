# Anything Analyzer v3.6.29

## 修复

- **LLM 非对象 JSON 响应诊断** — 避免兼容服务返回 `null` 等合法但非对象 JSON 时抛出内部属性访问错误
  - `safeParseJson` 现在会将非对象 JSON 归一为空对象，由各调用路径继续给出明确格式错误
  - OpenAI Chat Completions 回归测试覆盖 `null` 响应，确保诊断保持为缺少 `choices` 字段

## 下载

| 平台 | 文件 |
|------|------|
| Windows | Anything-Analyzer-Setup-3.6.29.exe |
| macOS (Apple Silicon) | Anything-Analyzer-3.6.29-arm64.dmg |
| macOS (Intel) | Anything-Analyzer-3.6.29-x64.dmg |
| Linux | Anything-Analyzer-3.6.29.AppImage |
