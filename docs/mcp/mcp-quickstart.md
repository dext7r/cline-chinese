# 🚀 MCP 快速入门指南

## ❓ 什么是 MCP 服务器？

把 MCP 服务器想象成给 Cline 提供超能力的特殊助手！它们能让 Cline 完成很酷的任务，比如获取网页内容或操作您的文件。

## ⚠️ 重要：系统要求

请停下！在继续之前，您必须确认满足以下要求：

### 必备软件

-   ✅ 最新版 Node.js (v18 或更高版本)

    -   检查方法：运行 `node --version`
    -   安装地址：<https://nodejs.org/>

-   ✅ 最新版 Python (v3.8 或更高版本)

    -   检查方法：运行 `python --version`
    -   安装地址：<https://python.org/>

-   ✅ UV 包管理器
    -   安装 Python 后运行：`pip install uv`
    -   验证方法：`uv --version`

❗ 如果以上任何命令失败或显示旧版本，请先安装/更新再继续！

⚠️ 如果遇到其他错误，请查看下方的"故障排除"部分。

## 🎯 快速步骤（仅在满足要求后执行！）

### 1. 🛠️ 安装您的第一个 MCP 服务器

1. 在 Cline 扩展中，点击 `MCP Server` 标签页
1. 点击 `Edit MCP Settings` 按钮

 <img src="https://github.com/user-attachments/assets/abf908b1-be98-4894-8dc7-ef3d27943a47" alt="MCP 服务器面板" width="400" />

1. MCP 设置文件将在 VS Code 的标签页中显示
1. 将文件内容替换为以下代码：

Windows 系统：

```json
{
	"mcpServers": {
		"mcp-installer": {
			"command": "cmd.exe",
			"args": ["/c", "npx", "-y", "@anaisbetts/mcp-installer"]
		}
	}
}
```

Mac 和 Linux 系统：

```json
{
	"mcpServers": {
		"mcp-installer": {
			"command": "npx",
			"args": ["@anaisbetts/mcp-installer"]
		}
	}
}
```

保存文件后：

1. Cline 会自动检测变更
2. MCP 安装程序将被下载并安装
3. Cline 将启动 MCP 安装程序
4. 您将在 Cline 的 MCP 设置界面看到服务器状态：

<img src="https://github.com/user-attachments/assets/2abbb3de-e902-4ec2-a5e5-9418ed34684e" alt="带安装程序的 MCP 服务器面板" width="400" />

## 🤔 接下来做什么？

现在您已经有了 MCP 安装程序，可以要求 Cline 从以下位置添加更多服务器：

1. NPM 仓库：<https://www.npmjs.com/search?q=%40modelcontextprotocol>
2. Python 包索引：<https://pypi.org/search/?q=mcp+server-&o=>

例如，您可以要求 Cline 安装 Python 包索引中的 `mcp-server-fetch` 包：

```bash
"安装名为 `mcp-server-fetch` 的 MCP 服务器
- 确保更新 mcp 设置
- 使用 uvx 或 python 运行服务器"
```

您将看到 Cline：

1. 安装 `mcp-server-fetch` python 包
1. 更新 mcp 设置 json 文件
1. 启动服务器

此时 mcp 设置文件应如下所示：

Windows 系统：

```json
{
	"mcpServers": {
		"mcp-installer": {
			"command": "cmd.exe",
			"args": ["/c", "npx", "-y", "@anaisbetts/mcp-installer"]
		},
		"mcp-server-fetch": {
			"command": "uvx",
			"args": ["mcp-server-fetch"]
		}
	}
}
```

您随时可以通过访问客户端的 MCP 服务器标签页来检查服务器状态。参见上图。

就是这样！🎉 您刚刚赋予了 Cline 一些强大的新能力！

## 📝 故障排除

### 1. 使用 `asdf` 时出现"unknown command: npx"错误

有个不太好的消息。除非 MCP 服务器打包方式有所改进，否则您需要手动完成更多工作才能使其正常运行。一个选择是卸载 `asdf`，但我们假设您不想这么做。

相反，您需要按照上述说明"编辑 MCP 设置"。然后，如[这篇文章](https://dev.to/cojiroooo/mcp-using-node-on-asdf-382n)所述，您需要为每个服务器配置添加"env"条目。

```json
"env": {
        "PATH": "/Users/<用户名>/.asdf/shims:/usr/bin:/bin",
        "ASDF_DIR": "<asdf_bin目录路径>",
        "ASDF_DATA_DIR": "/Users/<用户名>/.asdf",
        "ASDF_NODEJS_VERSION": "<您的node版本>"
      }
```

`asdf_bin目录路径`通常可以在您的 shell 配置文件中找到（如 `.zshrc`）。如果使用 Homebrew，可以运行 `echo ${HOMEBREW_PREFIX}` 查找目录起始位置，然后追加 `/opt/asdf/libexec`。

现在有个好消息。虽然不完美，但对于后续服务器安装，您可以相当可靠地让 Cline 自动完成此操作。在 Cline 设置的"自定义指令"中添加以下内容（右上角工具栏按钮）：

> 当安装 MCP 服务器并编辑 cline_mcp_settings.json 时，如果服务器需要使用 `npx` 作为命令，您必须从"mcp-installer"条目中复制"env"条目并添加到新条目中。这对服务器正常使用至关重要。

### 2. 运行 MCP 安装程序时仍然报错

如果运行 MCP 安装程序时仍然报错，可以尝试以下方法：

-   检查 MCP 设置文件是否有错误
-   阅读 MCP 服务器文档，确保 MCP 设置文件使用了正确的命令和参数 👈
-   在终端中直接运行带参数的命令。这样您就能看到 Cline 遇到的相同错误。