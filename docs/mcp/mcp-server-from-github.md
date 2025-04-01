# 从GitHub仓库构建MCP服务器

本指南提供了使用Cline从GitHub仓库构建现有MCP服务器的分步教程。

## **寻找MCP服务器**

在线有多个地方可以找到MCP服务器：

-   **Cline可以自动将MCP服务器添加到其列表中，然后您可以进行编辑。** Cline可以直接从GitHub克隆仓库并为您构建服务器。
-   **GitHub:** 在GitHub上寻找MCP服务器的两个最常见地方包括：
    -   [官方MCP服务器仓库](https://github.com/modelcontextprotocol/servers)
    -   [Awesome-MCP服务器仓库](https://github.com/punkpeye/awesome-mcp-servers)
-   **在线目录:** 多个网站列出了MCP服务器，包括：

    -   [mcpservers.org](https://mcpservers.org/)
    -   [mcp.so](https://mcp.so/)
    -   [glama.ai/mcp/servers](https://glama.ai/mcp/servers)

    这些目录允许用户根据下载量、日期、星标和使用案例等多种标准对服务器进行排序。每个条目都提供了功能、工具和配置说明等信息。

-   **PulseMCP:** 该网站有一篇博客文章讨论了AI如何使用MCP服务器使网站过时。PulseMCP还包括关于MCP服务器的FAQ部分：[https://www.pulsemcp.com/](https://www.pulsemcp.com/)

## **使用Cline构建**

1.  **启动流程:** 向Cline提供以下信息：
    -   **GitHub仓库URL:** 服务器仓库的URL。
    -   **README.md内容:** 这是可选的，但有助于Cline理解服务器的用途和配置。您可以从GitHub仓库复制README.md文件。
2.  **与Cline的交互示例:**

    ```
    用户: "Cline，我想添加用于Brave浏览器控制的MCP服务器。这是GitHub链接：https://github.com/modelcontextprotocol/servers/tree/main/src/brave-search 你能添加吗？"

    Cline: "好的。正在将仓库克隆到MCP目录。因为它有'package.json'文件，所以需要构建。我应该运行'npm run build'吗？"

    用户: "是的，构建它。"

    Cline: "构建完成。这个服务器需要一个浏览器路径。你的Brave浏览器可执行文件在哪里？"

    用户: "它在'/Applications/Brave Browser.app/Contents/MacOS/Brave Browser'。"

    Cline: "好的。我已经用该路径更新了服务器配置，并将其添加到'cline_mcp_settings.json'。还有其他事情吗？"

    用户: "没有了。我们测试一下吧。"

    Cline: "太好了！正在启动MCP检查器来测试服务器连接。之后，我们可以尝试从Cline控制浏览器。"
    ```

3.  **Cline的操作:** 根据您的指令，Cline将执行以下操作：
    -   **仓库克隆:** Cline会将仓库克隆到您的本地机器，通常在您的配置中指定的目录。
    -   **调整:** 您可以指导Cline修改服务器的配置。例如：
        -   **用户:** "这个服务器需要一个API密钥。你能找到应该添加它的地方吗？"
        -   Cline可能会根据您的指令自动更新`cline_mcp_settings.json`文件或其他相关文件。
    -   **构建服务器:** Cline将运行适当的构建命令，通常是`npm run build`。
    -   **将服务器添加到设置:** Cline会将服务器的配置添加到`cline_mcp_settings.json`文件。

## **测试和故障排除**

1.  **测试服务器:** Cline完成构建过程后，测试服务器以确保其按预期工作。如果遇到任何问题，Cline可以协助您。
2.  **MCP检查器:** 您可以使用MCP检查器来测试服务器的连接和功能。

## **最佳实践**

-   **了解基础知识:** 虽然Cline简化了流程，但基本了解服务器代码、MCP协议()以及如何配置服务器是有益的。这有助于更有效地进行故障排除和定制。
-   **清晰的指令:** 在整个过程中向Cline提供清晰具体的指令。
-   **测试:** 安装和配置后彻底测试服务器以确保其正常运行。
-   **版本控制:** 使用版本控制系统（如Git）跟踪服务器代码的更改。
-   **保持更新:** 保持MCP服务器更新以获取最新功能和安全补丁。