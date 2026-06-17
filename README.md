# Ctrl_CC

## English

### Download

Open the latest release:

https://github.com/KiddPhenix/Ctrl_CC-Releases/releases/latest

Choose the file for your system:

- Windows x64: `Ctrl_CC-<version>-windows-x64.zip`
- macOS Apple Silicon, when available: `Ctrl_CC-<version>-macos-arm64.dmg`
- macOS Intel, when available: `Ctrl_CC-<version>-macos-x64.dmg`

Older versions are available from:

https://github.com/KiddPhenix/Ctrl_CC-Releases/releases

Release history:

[CHANGELOG.md](CHANGELOG.md)

### Windows

1. Download the Windows zip file from Releases.
2. Extract the zip file to a folder you control, such as `D:\Tools\Ctrl_CC`.
3. Run `Ctrl_CC.exe`.
4. Optional: add the extracted folder to `PATH` if you want to call `Ctrl_CC-CLI.cmd` or `Ctrl_CC-MCP.cmd` from other tools.

Packaged command examples:

```powershell
.\Ctrl_CC-CLI.cmd status
.\Ctrl_CC-CLI.cmd search "project convention"
```

### macOS

1. Download the dmg file for your Mac.
2. Open the dmg file.
3. Drag `Ctrl_CC` to `Applications`.
4. Start `Ctrl_CC` from `Applications`.

Packaged command-line entry points are included in the app bundle when available. If macOS blocks the first launch, open System Settings, allow the app, and launch it again.

### Local Data

Ctrl_CC stores local data on your own machine.

Windows default paths:

```text
%APPDATA%\Ctrl_CC\data\ctrl_cc.sqlite
%APPDATA%\Ctrl_CC\data\settings.json
%APPDATA%\Ctrl_CC\logs\boot.log
%APPDATA%\Ctrl_CC\logs\mcp.log
```

Environment overrides:

```text
CTRL_CC_USER_DATA_DIR
CTRL_CC_DATA_DIR
CTRL_CC_HOME
CTRL_CC_CLI_CMD
CTRL_CC_MCP_CMD
```

### Update Check

The latest-version metadata is published here:

https://raw.githubusercontent.com/KiddPhenix/Ctrl_CC-Releases/main/latest.json

Apps or scripts can read that JSON file, compare the installed version with `latest.version`, then open `latest.releasePage` or download the matching platform asset.

---

## 中文

### 下载

打开最新版本：

https://github.com/KiddPhenix/Ctrl_CC-Releases/releases/latest

按系统选择文件：

- Windows x64：`Ctrl_CC-<version>-windows-x64.zip`
- macOS Apple Silicon，如该版本提供：`Ctrl_CC-<version>-macos-arm64.dmg`
- macOS Intel，如该版本提供：`Ctrl_CC-<version>-macos-x64.dmg`

历史版本在这里：

https://github.com/KiddPhenix/Ctrl_CC-Releases/releases

版本历史：

[CHANGELOG.md](CHANGELOG.md)

### Windows

1. 从 Releases 下载 Windows zip 文件。
2. 解压到你自己管理的目录，例如 `D:\Tools\Ctrl_CC`。
3. 运行 `Ctrl_CC.exe`。
4. 可选：如果希望其他工具直接调用 `Ctrl_CC-CLI.cmd` 或 `Ctrl_CC-MCP.cmd`，把解压目录加入 `PATH`。

打包版命令示例：

```powershell
.\Ctrl_CC-CLI.cmd status
.\Ctrl_CC-CLI.cmd search "project convention"
```

### macOS

1. 下载与你的 Mac 匹配的 dmg 文件。
2. 打开 dmg 文件。
3. 把 `Ctrl_CC` 拖到 `Applications`。
4. 从 `Applications` 启动 `Ctrl_CC`。

打包版命令行入口会随 app bundle 一起提供。首次启动如果被 macOS 拦截，到系统设置里允许该应用，然后重新打开。

### 本地数据

Ctrl_CC 的数据保存在本机。

Windows 默认路径：

```text
%APPDATA%\Ctrl_CC\data\ctrl_cc.sqlite
%APPDATA%\Ctrl_CC\data\settings.json
%APPDATA%\Ctrl_CC\logs\boot.log
%APPDATA%\Ctrl_CC\logs\mcp.log
```

可用环境变量：

```text
CTRL_CC_USER_DATA_DIR
CTRL_CC_DATA_DIR
CTRL_CC_HOME
CTRL_CC_CLI_CMD
CTRL_CC_MCP_CMD
```

### 更新检测

最新版本元数据发布在这里：

https://raw.githubusercontent.com/KiddPhenix/Ctrl_CC-Releases/main/latest.json

App 或脚本可以读取这个 JSON，拿本机版本和 `latest.version` 比较，然后打开 `latest.releasePage`，或下载对应平台的资产。
