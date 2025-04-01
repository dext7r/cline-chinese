# Cline 扩展架构

本目录包含 Cline VSCode 扩展的架构文档。

## 扩展架构图

[extension-architecture.mmd](./extension-architecture.mmd) 文件包含一个 Mermaid 图表，展示了 Cline 扩展的高层架构。该图表说明了：

1. **核心扩展**
   - 扩展入口点和主要类
   - 通过 VSCode 全局状态和密钥存储进行状态管理
   - Cline 类中的核心业务逻辑

2. **Webview 用户界面**
   - 基于 React 的用户界面
   - 通过 ExtensionStateContext 进行状态管理
   - 组件层次结构

3. **存储系统**
   - 任务专用的历史记录和状态存储
   - 基于 Git 的文件变更检查点系统

4. **数据流**
   - 核心扩展组件间的数据流
   - Webview 用户界面数据流
   - 核心与 webview 之间的双向通信

## 查看图表

查看图表的步骤：
1. 在 VSCode 中安装 Mermaid 图表查看器扩展
2. 打开 extension-architecture.mmd 文件
3. 使用扩展的预览功能渲染图表

您也可以在 GitHub 上查看该图表，GitHub 内置了 Mermaid 渲染支持。

## 配色方案

图表采用高对比度配色方案以提高可视性：
- 粉色 (#ff0066)：全局状态和密钥存储组件
- 蓝色 (#0066ff)：扩展状态上下文
- 绿色 (#00cc66)：Cline 提供者
- 所有组件均使用白色文字以确保最佳可读性