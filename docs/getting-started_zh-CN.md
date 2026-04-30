[English](./getting-started.md) | 简体中文

# XplorOne 快速开始

XplorOne 是一款面向超级个体、自由职业者、一人公司经营者、顾问、独立开发者和小型工作室主理人的本地优先 AI 财务工作台。

这份文档帮助你完成第一次可用的基础流程：

1. 下载并安装 XplorOne
2. 创建或打开账本
3. 理解首页工作台
4. 记下第一笔流水
5. 查看流水记录
6. 打开报表与财务视图
7. 可选启用 AI 功能
8. 可选了解本地 MCP 与外部 agent 连接

这不是完整功能手册。  
如果你想了解 XplorOne 当前有哪些功能，请看：[功能导览](./feature-overview_zh-CN.md)。

## 1. 下载并安装

从 [GitHub Releases](https://github.com/SimonZhangM/XplorOne/releases) 下载最新 Windows 版本。

下载后：

1. 运行安装程序
2. 完成安装
3. 启动 XplorOne

如果 Windows 出现安全提示，请确认安装包来自本仓库的官方 Release 页面。

## 2. 创建或打开第一个账本

账本是 XplorOne 中最主要的财务工作空间。

在一个账本里，你可以管理：

- 账户
- 分类
- 流水
- 报表与财务视图

第一次启动 XplorOne 后，可以先创建一个新账本，或者打开已有账本。

完成这一步不需要 API Key。

## 3. 理解首页工作台

首页是 XplorOne 的财务工作台。

它的作用不是单纯展示数据，而是帮助你快速理解当前财务状态，并进入最常用的操作。

在首页工作台里，你通常可以看到：

- 本月收入与支出
- 资产概览
- 每日收支趋势
- 支出分类排行
- 最近流水
- 快捷操作，例如记一笔、看流水、看报表、问 AI

首页不是装饰性的仪表盘。  
它是你日常财务工作的起点。

## 4. 记下第一笔流水

最简单的开始方式，是先记下一笔流水。

你可以从两个入口开始：

- 左侧边栏的 **记一笔**
- 首页工作台里的 **记一笔** 快捷入口

第一笔流水可以保持简单：

1. 选择流水类型
2. 填写金额
3. 选择账户
4. 选择分类
5. 设置日期
6. 如有需要，补充备注
7. 保存流水

保存后，这笔流水就会进入你的本地账本。

记流水不需要 API Key。

## 5. 查看流水记录

记下第一笔流水后，可以进入流水列表查看记录。

你可以在列表页面查看：

- 流水记录
- 收入与支出流向
- 账户相关活动
- 分类相关活动

这一步可以帮助你确认刚才的记录已经保存成功，也能初步理解 XplorOne 如何组织财务数据。

## 6. 打开报表与财务视图

当你有了一些流水后，可以打开报表与财务视图，更清楚地观察自己的财务状态。

你可以查看：

- 收入与支出
- 现金流
- 资产与负债
- 账户状态
- 分类结构
- 图表与趋势

报表与财务视图属于核心本地功能。  
它们不需要 API Key。

## 7. 可选 — 启用 AI 功能

AI 功能是可选增强，不是使用 XplorOne 的前提。

即使没有 API Key，XplorOne 也依然可以作为本地优先财务工作台使用。  
你仍然可以记账、查看报表、使用本地视图和基础查询。

只有当你需要 AI 助手能力时，才需要配置自己的 API Key：

- 财务分析
- 趋势解释
- 明确进入 AI 工作流时的模型辅助理解
- 启用模型参与时的录入草稿辅助
- 更开放的财务相关对话

在本地内核支持的范围内，本地助手的查询和录入工作流仍然保持本地优先。

AI 助手可以帮助分析和更开放的财务相关对话，但任何写入都需要用户确认。
AI 不会自动写入账本。

配置方式请见：[BYOK 配置说明](./byok-setup_zh-CN.md)。  
隐私与边界说明请见：[隐私与 AI 边界](./privacy-and-ai-boundaries_zh-CN.md)。

## 8. 可选 — 通过本地 MCP 连接外部 agent

本地 MCP 是可选能力，主要面向外部 agent 工作流。

如果你使用 Codex、WorkBuddy 这类工具，XplorOne 可以提供 token 保护的本地只读 MCP / query 路径。

这不是以下操作的前提：

- 本地记账
- 录入流水
- 查看报表
- 基础查询
- 使用 XplorOne 桌面端的常规工作流

当前 MCP 路径只读，并且会经过 XplorOne 受控的本地 API 与查询链路，而不是绕过应用直接读取数据库。

功能层面的介绍可见：[功能导览](./feature-overview_zh-CN.md)。  
数据与集成边界可见：[隐私与 AI 边界](./privacy-and-ai-boundaries_zh-CN.md)。

## 9. 接下来可以看什么

完成第一次使用流程后，你可以继续查看：

- [功能导览](./feature-overview_zh-CN.md) —— 了解 XplorOne 的主要功能区域
- [隐私与 AI 边界](./privacy-and-ai-boundaries_zh-CN.md) —— 了解本地数据、AI 与集成边界
- [数据保存与备份恢复](./data-storage-and-backup_zh-CN.md) —— 理解本地文件、备份、恢复和迁移边界
- [AI 助手行为说明](./ai-assistant-behavior_zh-CN.md) —— 理解本地助手和 AI 助手行为
- [本地 API 与 MCP](./local-api-and-mcp_zh-CN.md) —— 理解外部 agent 集成边界
- [BYOK 配置说明](./byok-setup_zh-CN.md) —— 为 AI 辅助功能配置自己的模型 API Key
- [当前限制说明](./known-limitations_zh-CN.md) —— 了解当前发布范围
- [支持说明](../SUPPORT_zh-CN.md) —— 了解遇到问题时去哪里反馈

## 需要帮助？

你可以使用：

- [Discussions](https://github.com/SimonZhangM/XplorOne/discussions) 提出问题、想法、反馈和产品讨论
- [Issues](https://github.com/SimonZhangM/XplorOne/issues) 提交 bug、安装问题和可明确处理的问题
- [Releases](https://github.com/SimonZhangM/XplorOne/releases) 下载版本与查看更新说明
