# Changelog

## 0.1.8 - 2026-06-23

### English

#### Features

- Added Windows automatic update installation from the public release metadata: Ctrl_CC downloads the Windows zip, verifies SHA256, prepares a backup, applies the update, and restarts automatically.
- Added Agent portrait generation through Codex CLI, including Codex CLI discovery, execution logs, usage records, and generated image file handling.

#### Improvements

- Updated the in-app update entry so Windows users can download and install directly, while other platforms still open the release download page.
- Updated Agent portrait errors and copy to guide users toward connecting Codex CLI instead of configuring an OpenAI API key.
- Improved macOS history scanning path support so local history discovery works with more macOS layouts.

#### Fixes

- Added stricter validation for Windows update metadata, asset URL, zip contents, and SHA256 digest before applying an update.
- Improved Agent portrait failure reporting for missing Codex CLI, CLI launch failure, CLI exit failure, timeout, and empty image output.

### 中文

#### 功能

- 新增 Windows 自动更新安装：Ctrl_CC 会从公开发布元数据下载 Windows zip，校验 SHA256，准备备份，应用更新并自动重启。
- 新增通过 Codex CLI 生成 Agent 立绘，包含 Codex CLI 检测、执行日志、用量记录和生成图片落盘处理。

#### 调整

- 更新应用内更新入口，Windows 用户可直接下载并安装，其他平台继续打开 Release 下载页。
- 更新 Agent 立绘生成错误提示和文案，引导用户连接 Codex CLI，而不是配置 OpenAI API Key。
- 优化 macOS 历史扫描路径支持，让本机历史发现兼容更多 macOS 路径布局。

#### 修复

- 增加 Windows 自动更新前的元数据、下载 URL、zip 内容和 SHA256 校验。
- 优化 Agent 立绘失败原因展示，覆盖缺少 Codex CLI、CLI 启动失败、CLI 退出失败、超时和未找到图片输出。

### Assets

```text
Ctrl_CC-0.1.8-windows-x64.zip
SHA256: 393C15BF760FDE5ABF8379402459F9627E5C97FE609ACB4B2DD0416B6A3010E5
```

## 0.1.7 - 2026-06-22

### English

#### Features

- Improved Memories history import so imported local AI history is summarized in smaller batches, with progress updates for processed, imported, and skipped items.
- Added a debug setting to reset the Memories history import cursor, allowing a future import to rescan local history when needed.
- Added a tag-filter delete action for Memories so the current tag search can be cleaned up directly.

#### Improvements

- Strengthened AI summarization rules for imported history so generated Memories include a concrete project/module subject, specific problem, useful tags, and Markdown solution text.
- Made history import safer to retry: failed AI summary batches stop without advancing the cursor, while already imported batches remain recorded.
- Improved import job logs so scan count, imported count, skipped candidates, and retry state are visible.

#### Fixes

- Reduced low-quality generic titles and provenance-only problem text in imported Memories.
- Fixed prompt proposal handling so missing prompt text is surfaced instead of silently writing back an empty proposal.

#### macOS testing build

- Added unsigned macOS DMG builds for Apple Silicon and Intel Macs.

#### Signing note

This macOS build is unsigned during the testing period. I have not bought an Apple Developer account yet because the budget is still crying quietly, so macOS may ask you to right-click the app and choose **Open** on first launch.

### 中文

#### 功能

- 优化 Memories 历史导入，按更小批次总结本地 AI 历史，并显示已处理、已导入、已跳过的进度。
- 新增调试设置，可重置 Memories 历史导入 cursor，必要时让下一次导入重新扫描本机历史。
- 新增按当前 tag 搜索结果删除 Memories 的入口，方便直接清理当前筛选范围。

#### 调整

- 强化历史导入的 AI 总结规则，生成的 Memories 需要包含具体项目/模块、明确问题、有用标签和 Markdown solutionText。
- 提升历史导入的可重试性：AI 总结批次失败时不推进 cursor，已成功导入的批次会保留记录。
- 优化导入任务日志，记录扫描数量、导入数量、跳过候选和可重试状态。

#### 修复

- 减少导入 Memories 中过泛标题和只描述来源、不描述问题的内容。
- 修复提示词草案缺少正文时的处理，避免静默写回空草案。

#### macOS 测试包

- 新增 Apple Silicon 和 Intel Mac 的未签名 macOS DMG 测试包。

#### 签名说明

这个 macOS 版本在测试期暂时未签名。还没有购买 Apple 开发者账户，因为预算目前正在默默哭穷，所以 macOS 首次启动时可能需要右键 App 并选择**打开**。

### Assets

```text
Ctrl_CC-0.1.7-windows-x64.zip
SHA256: E1B74D2FFE32E3B5B386A0E98CE0B6D9B86368A42EBB273C4C1C7B1043E4C360
Ctrl_CC-0.1.7-macos-arm64.dmg
SHA256: 13ab624d8d00b3fbe5b9b952c547d9b79f8486996f4f3d76ba971acc61138285
Ctrl_CC-0.1.7-macos-x64.dmg
SHA256: e2c286233aed17cd267cac8f78ed377a30d4779eef4ba014fc8eae13980ae1f3
```

## 0.1.6 - 2026-06-22

### English

#### Features

- Added Agent cards and portrait-driven Agent browsing, with dedicated entries for builders, reviewers, researchers, planners, release work, docs, testing, security, and clipboard workflows.
- Added Agent portrait import surfaces and expanded portrait matching so local AI tools and AGENTS.md-style workflows can be represented more clearly.
- Added Agent history reflection scanning, AI review, and quality-loop records to help turn prior work into reusable Agent memory.
- Added background Agent history scanning so long history analysis can run without blocking the main app flow.
- Added unsigned macOS DMG builds for Apple Silicon and Intel Macs.

#### Improvements

- Improved Agent memory import and optimization flows, including broader history recall and a clearer review path before turning history into reusable cards.
- Improved Agent detail and compact-list behavior, preserving metadata and making section switching work reliably.
- Improved default Agent handling on macOS so the new Agent surfaces start from better cross-platform defaults.

#### Fixes

- Tightened Agent history recall to reduce unrelated or instruction-context content from being pulled into reflections.
- Filtered self-pollution from Agent history review and limited AI review budgets to keep background analysis more predictable.
- Fixed Agent detail section switching and compact-list metadata retention.

#### Signing note

This macOS build is unsigned during the testing period. I have not bought an Apple Developer account yet because the budget is still crying quietly, so macOS may ask you to right-click the app and choose **Open** on first launch.

### 中文

#### 功能

- 新增 Agent 卡片和立绘浏览入口，覆盖构建、评审、研究、规划、发布、文档、测试、安全和剪贴板工作流。
- 新增 Agent 立绘导入界面并扩展立绘候选匹配，让本机 AI 工具和 AGENTS.md 工作流能被更清晰地呈现。
- 新增 Agent 历史反思扫描、AI 复核和质量闭环记录，用于把历史工作沉淀成可复用的 Agent 记忆。
- 新增后台 Agent 历史扫描，长历史分析不再阻塞主界面流程。
- 新增 Apple Silicon 和 Intel Mac 的未签名 macOS DMG 测试包。

#### 调整

- 优化 Agent 记忆导入与优化流程，扩大历史召回范围，并在写入可复用卡片前增加更清楚的复核路径。
- 优化 Agent 详情和紧凑列表行为，保留元信息并修复分区切换体验。
- 优化 macOS 上的默认 Agent 处理，让新的 Agent 界面具备更好的跨平台初始状态。

#### 修复

- 收紧 Agent 历史召回，减少无关内容和指令上下文被带入反思结果。
- 过滤 Agent 历史复核中的自污染内容，并限制 AI 复核预算，让后台分析更可控。
- 修复 Agent 详情分区切换和紧凑列表元信息保留问题。

#### 签名说明

这个 macOS 版本在测试期暂时未签名。还没有购买 Apple 开发者账户，因为预算目前正在默默哭穷，所以 macOS 首次启动时可能需要右键 App 并选择**打开**。

### Assets

```text
Ctrl_CC-0.1.6-windows-x64.zip
SHA256: 4DB4E983C1D4361552B78BEB56DF04A5523B58D2AF8901AD6871DF513D88CDDF
Ctrl_CC-0.1.6-macos-arm64.dmg
SHA256: a1c8e27db2fd1dab3b9b796670ed143640b301b6c0119d9362387ae9c65a482f
Ctrl_CC-0.1.6-macos-x64.dmg
SHA256: a36e8df79e60b68ccf23907645ec9ba6db380779c04b0159a45d24f5ca460bd8
```

## 0.1.5 - 2026-06-19

### English

#### Features

- Added macOS as a Local CLI runtime option in Settings.
- Added macOS Local CLI command discovery for Codex app resource paths, Homebrew paths, and shell PATH lookup.
- Added native macOS Local CLI verification and version detection before treating the provider as ready.
- Added a Step-by-Step release runbook and saved it back into Ctrl_CC Knowledge.
- Added unsigned macOS DMG builds for Apple Silicon and Intel Macs.

#### Improvements

- Updated Local CLI skill injection so native macOS paths use the same managed agent-file flow as other native runtimes.
- Replaced the dev script with a cross-platform Electron launcher.

#### Signing note

This macOS build is unsigned during the testing period. I have not bought an Apple Developer account yet because the budget is still crying quietly, so macOS may ask you to right-click the app and choose **Open** on first launch.

### 中文

#### 功能

- Settings 中新增 macOS 作为本地 CLI 运行环境选项。
- 新增 macOS 本地 CLI 命令检测，覆盖 Codex App 资源路径、Homebrew 路径和 shell PATH 查找。
- 新增 macOS 本地 CLI 验证和版本检测，通过后再视为 Provider 可用。
- 新增 Step by Step 发布手册，并写回 Ctrl_CC Knowledge。
- 新增 Apple Silicon 和 Intel Mac 的未签名 macOS DMG 测试包。

#### 调整

- 更新本地 CLI skill 写入逻辑，让 macOS 原生路径使用和其他原生运行时一致的 agent file 写入流程。
- 将 dev 脚本替换为跨平台 Electron 启动器。

#### 签名说明

这个 macOS 版本在测试期暂时未签名。还没有购买 Apple 开发者账户，因为预算目前正在默默哭穷，所以 macOS 首次启动时可能需要右键 App 并选择**打开**。

### Assets

```text
Ctrl_CC-0.1.5-macos-arm64.dmg
SHA256: b04315cb939e9485a78c75c2b00824fc4244a8cfa44e3fb511bd62ef697b4c55
Ctrl_CC-0.1.5-macos-x64.dmg
SHA256: d3cb457d32bea9a9edf305592bbce8609a3f62033544de7d3ff59e58e5f7eb6d
```

## 0.1.4 - 2026-06-18

### English

#### Features

- Added a guided Local CLI setup flow in Settings, covering command detection, tool selection, command configuration, authorization, skill injection, and final verification.
- Added desktop analysis verification for Local CLI providers, checking that the configured CLI can return parseable Knowledge/Todo JSON before treating the setup as ready.
- Added unsigned macOS DMG builds for Apple Silicon and Intel Macs.

#### Improvements

- Improved Local CLI setup wording and progress states so the difference between command authorization and real desktop-analysis readiness is clearer.
- Hid the manual test-entry hint from the main setup path, keeping the guide focused on the real verification flow.
- Updated the built-in Ctrl_CC skill text so Knowledge, Todo, Capture, and job-log writebacks follow the user's current language.

#### Fixes

- Reduced the chance of Local CLI setup appearing successful before the provider has passed a real analysis-format check.

#### Signing note

This macOS build is unsigned during the testing period. I have not bought an Apple Developer account yet because the budget is still crying quietly, so macOS may ask you to right-click the app and choose **Open** on first launch.

### 中文

#### 功能

- Settings 中新增本地 CLI 配置向导，串起命令检测、工具选择、命令配置、授权、写入规则和最终验证。
- 新增本地 CLI 桌面分析验证，确认配置后的 CLI 能返回可解析的 Knowledge/Todo JSON 后，再视为配置可用。
- 新增 Apple Silicon 和 Intel Mac 的未签名 macOS DMG 测试包。

#### 调整

- 优化本地 CLI 配置文案和进度状态，更清楚地区分“命令已授权”和“桌面分析链路已可用”。
- 隐藏主流程里的手动测试入口提示，让向导聚焦真实验证流程。
- 更新内置 Ctrl_CC skill 文案，要求 Knowledge、Todo、Capture 和 job log 写回时跟随用户当前语言。

#### 修复

- 降低本地 CLI 只完成授权但尚未通过真实分析格式验证时，被误判为已经可用的概率。

#### 签名说明

这个 macOS 版本在测试期暂时未签名。还没有购买 Apple 开发者账户，因为预算目前正在默默哭穷，所以 macOS 首次启动时可能需要右键 App 并选择**打开**。

### Assets

```text
Ctrl_CC-0.1.4-windows-x64.zip
SHA256: C1D5123C42E71E0274DA3989830A76A2AC5E0A053FF4615D63783CA61CD328AB
Ctrl_CC-0.1.4-macos-arm64.dmg
SHA256: 41685314b9d99fa89e04e888dface597f97883f304aecd21013268fa7fb7af74
Ctrl_CC-0.1.4-macos-x64.dmg
SHA256: 433702f4aab51865ca0fc8d5446c6b940e20c5e241c2bd80cc71f7ead15d46d8
```

## 0.1.3 - 2026-06-18

### English

#### Improvements

- Polished the Memory and navigation UI so Knowledge, Todo, Vault, and related views are easier to scan and switch between.
- Improved local CLI provider settings and runtime state display, making provider setup and troubleshooting clearer.
- Improved local CLI analysis prompting so generated Knowledge drafts use a more consistent Markdown solution format.

#### Fixes

- Fixed Todo editing flows so task detail changes are saved and reflected more reliably.
- Fixed local CLI settings edge cases around provider configuration and status handling.
- Tightened local CLI result handling to reduce malformed analysis output from breaking the expected response format.

### 中文

#### 调整

- 优化 Memory 和导航界面，Knowledge、Todo、Vault 等视图之间更容易浏览和切换。
- 优化本地 CLI Provider 的设置和运行状态展示，Provider 配置和问题排查更清晰。
- 优化本地 CLI 分析提示词，让生成的 Knowledge 草稿更稳定地使用 Markdown solution 格式。

#### 修复

- 修复 Todo 编辑流程，详情页中的任务修改能更可靠地保存并反馈到界面。
- 修复本地 CLI 设置中的 Provider 配置和状态处理边界问题。
- 收紧本地 CLI 分析结果格式处理，降低异常输出破坏预期响应格式的概率。

### Assets

```text
Ctrl_CC-0.1.3-windows-x64.zip
SHA256: AD3B8DE6E9D94BA06E314B46376DA6DEAAAEA8D7EE76EBF7F36A5E9F8C63EAEB
```

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
