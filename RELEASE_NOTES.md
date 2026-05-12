# Anything Analyzer v3.6.9

## 修复

- **手机端 CA 证书安装后 HTTPS 仍报错** — 修复移动设备安装 CA 证书后进行网络请求仍提示证书不正确的问题
	- `.cer` 证书文件改为 DER 二进制格式（此前错误地返回 PEM 文本格式，iOS/Android 可能无法正确识别）
	- 叶证书添加 `authorityKeyIdentifier` 和 `subjectKeyIdentifier` 扩展，满足移动端 TLS 栈的严格校验
	- TLS 握手时发送完整证书链（叶证书 + CA 证书），确保客户端可完整验证信任路径
	- `.cer` / `.crt` / `.pem` 端点分别返回正确的 Content-Type（`application/x-x509-ca-cert` / `application/x-pem-file`）

## 改进

- **证书安装教程大幅完善** — 证书下载页面新增详细的分步操作指南
	- iOS：10 步完整流程（代理配置 → Safari 下载 → 描述文件安装 → 证书信任设置），附常见问题解答
	- Android：8 步安装流程 + 验证方法 + 小米/华为/OPPO/vivo/三星/Pixel 六大品牌的设置路径指引
	- 补充 Android 7+ 用户 CA 限制说明、Root/Magisk 方案、锁屏要求等特别说明
	- 桌面端补充 Windows 信任存储和 macOS 钥匙串信任设置说明

## 下载

| 平台 | 文件 |
|------|------|
| Windows | Anything-Analyzer-Setup-3.6.9.exe |
| macOS (Apple Silicon) | Anything-Analyzer-3.6.9-arm64.dmg |
| macOS (Intel) | Anything-Analyzer-3.6.9-x64.dmg |
| Linux | Anything-Analyzer-3.6.9.AppImage |
