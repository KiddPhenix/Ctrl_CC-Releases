# Changelog

## 0.1.2 - 2026-06-18

### English

#### Features

- Added Local CLI LLM Provider support, allowing Ctrl_CC to use local command-line AI tools such as Codex as an analysis provider.
- Added Settings flows for adding, linking, and preparing local CLI providers without requiring a remote API key.

#### Improvements

- Improved Codex CLI discovery on Windows, including Microsoft Store installs and stable local executable paths.
- Improved Codex execution parameters by using verified arguments and recording the actual invocation details for troubleshooting.

#### Fixes

- Fixed local CLI analysis jobs that could remain stuck in the running state.
- Fixed Codex Store path handling so Ctrl_CC prefers the executable path instead of an unstable package directory.
- Fixed Knowledge item delete confirmation so the action menu keeps the confirmation state visible and resets cleanly.

### 中文

#### 功能

- 新增本地 CLI LLM Provider，Ctrl_CC 可以把 Codex 这类本地命令行 AI 工具作为分析 Provider 使用。
- 在 Settings 中增加本地 CLI Provider 的添加、链接和准备流程，不依赖远程 API Key 也能接入本机 AI 工具。

#### 调整

- 优化 Windows 上的 Codex CLI 检测，兼容 Microsoft Store 安装路径和稳定的本地可执行文件路径。
- 优化 Codex 调用参数，使用已验证的执行参数，并记录实际调用信息，方便排查本地 CLI 问题。

#### 修复

- 修复本地 CLI 分析任务可能一直停留在运行中的问题。
- 修复 Codex Store 路径处理，优先使用可执行文件路径，避免依赖不稳定的包目录。
- 修复 Knowledge 条目删除确认菜单状态，确认按钮能保持可见并在关闭菜单后正确重置。

### Assets

```text
Ctrl_CC-0.1.2-windows-x64.zip
SHA256: 59fb0ea129a04c4675ffb648131cbe3c8409cd5d3802ed8246f3c28e1d6ba59c
```

## 0.1.1 - 2026-06-18

### English

#### Features

- Added built-in update checking from the public release metadata, with an in-app entry that opens the latest GitHub Release when a newer version is available.
- Added an appearance setting with System, Light, and Dark modes.
- Added the new public release metadata and packaging path used by future update checks.
- Added unsigned macOS DMG builds for Apple Silicon and Intel Macs.

#### Improvements

- Redesigned the Todo detail view around execution: editable notes, due date, priority, tags, goal, next steps, completion criteria, and source text are easier to scan and act on.
- Refined capture notifications and item actions so captured content flows more clearly into Knowledge and Todo.
- Improved onboarding/home wording, starter data localization, and app branding copy.

#### Fixes

- Added a Windows clipboard fallback for more reliable global capture.
- Fixed macOS capture support and bundled the macOS key server build path.
- Fixed AI-generated tag language handling so tags better match the captured note language.
- Restored title-bar dragging behavior around the brand area.

#### Signing note

This macOS build is unsigned during the testing period. I have not bought an Apple Developer account yet because the budget is still crying quietly, so macOS may ask you to right-click the app and choose **Open** on first launch.

### 中文

#### 功能

- 增加内置更新检测：从公开发布元数据读取最新版本，发现新版时可在应用内打开对应 GitHub Release。
- 增加外观设置，支持跟随系统、浅色模式和深色模式。
- 建立公开发布元数据和打包发布路径，为后续版本检测和下载入口打基础。
- 新增 Apple Silicon 和 Intel Mac 的未签名 macOS DMG 测试包。

#### 调整

- 优化 Todo 详情执行视图，备注、截止时间、优先级、标签、目标、下一步、完成标准和原始来源更容易查看和处理。
- 优化抓取通知和条目操作，让抓取内容进入 Knowledge / Todo 的过程更清晰。
- 优化首页引导词、初始数据本地化和应用品牌文案。

#### 修复

- 增加 Windows 剪贴板兜底，提高全局抓取稳定性。
- 修复 macOS 抓取支持，并补齐 macOS key server 打包路径。
- 修复 AI 生成标签的语言归属，使标签更符合原始内容语言。
- 恢复品牌栏区域的窗口拖动行为。

#### 签名说明

这个 macOS 版本在测试期暂时未签名。还没有购买 Apple 开发者账户，因为预算目前正在默默哭穷，所以 macOS 首次启动时可能需要右键 App 并选择**打开**。

### Assets

```text
Ctrl_CC-0.1.1-windows-x64.zip
SHA256: 293dad67d1961102f77c5f35d3c17a21d6c306d59ba20e52e78cdf621aa0604d
Ctrl_CC-0.1.1-macos-arm64.dmg
SHA256: bc6687ec0692fa5c631b5efb0165f28e23f2c3edf59a8c5f9c16cf0c1a29b7d6
Ctrl_CC-0.1.1-macos-x64.dmg
SHA256: 95a1cb5034f84e6668fa832fa6bbda244a3f0319b9a3550dea6ae441bed03276
```

## 0.1.0 - 2026-06-17

### English

- Initial public binary release metadata.
- Added the public README and latest-version JSON contract.

### 中文

- 初始化公开二进制发布元数据。
- 增加公开 README 和最新版本 JSON 约定。
