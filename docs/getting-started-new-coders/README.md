# Cline 入门指南 | 新手程序员

欢迎使用 Cline！本指南将帮助您完成设置并开始使用 Cline 构建第一个项目。

## 准备工作

开始前请确保您已准备好以下内容：

-   **VS Code:** 一款免费且强大的代码编辑器。
    -   [下载 VS Code](https://code.visualstudio.com/)
-   **开发工具:** 编程必备软件（Homebrew、Node.js、Git 等）。
    -   按照我们的[安装基础开发工具](installing-dev-essentials.md)指南进行设置（完成本指南后）
    -   Cline 会引导您安装所有需要的工具
-   **Cline 项目文件夹:** 专门用于存放所有 Cline 项目的文件夹。
    -   macOS 系统：在"文稿"文件夹中创建名为"Cline"的文件夹
        -   路径：`/Users/[您的用户名]/Documents/Cline`
    -   Windows 系统：在"文档"文件夹中创建名为"Cline"的文件夹
        -   路径：`C:\Users\[您的用户名]\Documents\Cline`
    -   在此 Cline 文件夹内，为每个项目创建单独的子文件夹
        -   示例：`Documents/Cline/workout-app` 用于健身追踪应用
        -   示例：`Documents/Cline/portfolio-website` 用于个人作品集网站
-   **VS Code 中的 Cline 扩展:** 在 VS Code 中安装 Cline 扩展。

-   这里有一个[视频教程](https://www.youtube.com/watch?v=N4td-fKhsOQ)介绍入门所需的一切。

## 分步设置指南

按照以下步骤启动并运行 Cline：

1. **打开 VS Code:** 启动 VS Code 应用程序。如果 VS Code 显示"正在运行的扩展可能..."，请点击"允许"。

2. **打开您的 Cline 文件夹:** 在 VS Code 中打开您在文档中创建的 Cline 文件夹。

3. **导航至扩展:** 点击 VS Code 侧边活动栏中的扩展图标。

4. **搜索'Cline':** 在扩展搜索栏中输入"Cline"。

5. **安装扩展:** 点击 Cline 扩展旁边的"安装"按钮。

6. **打开 Cline:** 安装完成后，您可以通过以下方式打开 Cline：
    - 点击活动栏中的 Cline 图标。
    - 使用命令面板（`CMD/CTRL + Shift + P`）并输入"Cline: Open In New Tab"将 Cline 作为标签页打开。推荐使用此方式以获得更好的视图。
    - **故障排除:** 如果看不到 Cline 图标，请尝试重启 VS Code。
    - **您将看到:** Cline 聊天窗口会出现在您的 VS Code 编辑器中。

![gettingStartedVsCodeCline](https://github.com/user-attachments/assets/622b4bb7-859b-4c2e-b87b-c12e3eabefb8)

## 设置 OpenRouter API 密钥

安装好 Cline 后，您需要设置 OpenRouter API 密钥以使用 Cline 的全部功能。

1.  **获取 OpenRouter API 密钥:**
    -   [获取 OpenRouter API 密钥](https://openrouter.ai/)
2.  **输入您的 OpenRouter API 密钥:**
    -   导航至 Cline 扩展中的设置按钮。
    -   输入您的 OpenRouter API 密钥。
    -   选择您偏好的 API 模型。
        -   **编程推荐模型:**
            -   `anthropic/claude-3.5-sonnet`: 最常用于编程任务。
            -   `google/gemini-2.0-flash-exp:free`: 免费的编程选项。
            -   `deepseek/deepseek-chat`: 价格极低，性能接近 3.5 sonnet
        -   [OpenRouter 模型排名](https://openrouter.ai/rankings/programming)

## 与 Cline 的首次互动

现在您可以开始使用 Cline 进行开发了。让我们创建第一个项目文件夹并构建一些内容！将以下提示复制粘贴到 Cline 聊天窗口：

```
嘿 Cline！你能帮我在 Cline 目录下创建一个名为"hello-world"的新项目文件夹，并制作一个显示"Hello World"蓝色大字体的简单网页吗？
```

**您将看到:** Cline 会帮助您创建项目文件夹并设置第一个网页。

## 使用 Cline 的技巧

-   **随时提问:** 如果有任何不确定的地方，尽管向 Cline 提问！
-   **使用截图:** Cline 可以理解图片，所以随时可以使用截图展示您的工作内容。
-   **复制粘贴错误信息:** 如果遇到错误，将错误信息复制粘贴到 Cline 聊天窗口。这将帮助 Cline 理解问题并提供解决方案。
-   **使用自然语言:** Cline 设计用于理解普通的非技术语言。您可以自由地用自己习惯的方式描述想法，Cline 会将其转化为代码。

## 常见问题

-   **什么是终端？** 终端是基于文本的计算机交互界面。它允许您运行命令来执行各种任务，如安装软件包、运行脚本和管理文件。Cline 使用终端执行命令并与您的开发环境交互。
-   **代码库如何工作？** (本节将根据新手程序员的常见问题进行扩展)

## 仍有困难？

随时联系我，我会帮助您开始使用 Cline。

nick | 608-558-2410

加入我们的 Discord 社区：[https://discord.gg/cline](https://discord.gg/cline)