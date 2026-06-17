# Changelog

## 0.1.1 - 2026-06-18

### English

### Features

- Added built-in update checking from the public release metadata, with an in-app entry that opens the latest GitHub Release when a newer version is available.
- Added an appearance setting with System, Light, and Dark modes.
- Added the new public release metadata and packaging path used by future update checks.

### Improvements

- Redesigned the Todo detail view around execution: editable notes, due date, priority, tags, goal, next steps, completion criteria, and source text are easier to scan and act on.
- Refined capture notifications and item actions so captured content flows more clearly into Knowledge and Todo.
- Improved onboarding/home wording, starter data localization, and app branding copy.

### Fixes

- Added a Windows clipboard fallback for more reliable global capture.
- Fixed macOS capture support and bundled the macOS key server build path.
- Fixed AI-generated tag language handling so tags better match the captured note language.
- Restored title-bar dragging behavior around the brand area.

### 中文

### 功能

- 增加内置更新检测：从公开发布元数据读取最新版本，发现新版时可在应用内打开对应 GitHub Release。
- 增加外观设置，支持跟随系统、浅色模式和深色模式。
- 建立公开发布元数据和打包发布路径，为后续版本检测和下载入口打基础。

### 调整

- 优化 Todo 详情执行视图，备注、截止时间、优先级、标签、目标、下一步、完成标准和原始来源更容易查看和处理。
- 优化抓取通知和条目操作，让抓取内容进入 Knowledge / Todo 的过程更清晰。
- 优化首页引导词、初始数据本地化和应用品牌文案。

### 修复

- 增加 Windows 剪贴板兜底，提高全局抓取稳定性。
- 修复 macOS 抓取支持，并补齐 macOS key server 打包路径。
- 修复 AI 生成标签的语言归属，使标签更符合原始内容语言。
- 恢复品牌栏区域的窗口拖动行为。

### Asset

```text
Ctrl_CC-0.1.1-windows-x64.zip
SHA256: 293dad67d1961102f77c5f35d3c17a21d6c306d59ba20e52e78cdf621aa0604d
```

## 0.1.0 - 2026-06-17

### English

- Initial public binary release metadata.
- Added the public README and latest-version JSON contract.

### 中文

- 初始化公开二进制发布元数据。
- 增加公开 README 和最新版本 JSON 约定。
