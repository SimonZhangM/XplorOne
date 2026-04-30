[English](./local-api-and-mcp.md) | 简体中文

# 本地 API 与 MCP

这份文档说明 XplorOne 面向外部 agent 和工具的本地集成路径。

它适合想理解 Local API / MCP 和软件内助手有什么区别的用户。

## 这里的 MCP 是什么

MCP 是 Model Context Protocol 的缩写。

在 XplorOne 中，MCP 是一个可选的本地集成路径，让外部 agent 工具可以通过 XplorOne 受控的本地接口查询结构化财务信息。

当前公开边界是：

- 本地运行
- 通过 token 保护
- 只读
- 围绕当前激活账本
- 经过 XplorOne 的本地 API 与查询层
- 不直接读取数据库

## 和软件内 AI 有什么不同

XplorOne 同时有软件内助手和本地集成路径。

它们有关联，但不是同一件事。

| 区域 | 软件内本地助手 | 软件内 AI 助手 | Local API / MCP |
|---|---|---|---|
| 主要用途 | 本地查询和录入工作流 | 分析和更开放的财务对话 | 外部 agent 只读查询 |
| 是否需要模型 | 受支持的本地流程不需要 | AI 工作流需要 | 外部客户端可能使用自己的模型 |
| 写入能力 | 草稿需用户确认 | 写入需用户确认 | 当前 MCP 路径只读 |
| 作用范围 | 当前应用工作流 | 当前应用工作流 | 当前激活账本查询路径 |
| 数据库访问 | 经过应用服务 | 经过应用服务和选定上下文 | 经过受控 Local API / query 层 |

## 外部 Agent 可以做什么

Codex、WorkBuddy 或类似 agent 客户端，可以通过只读 MCP / query 路径询问：

- 查询本月支出最高的分类
- 总结最近收入与支出变化
- 列出预算超支项
- 查看最近现金流变化
- 基于结构化结果比较不同期间

外部 agent 接收 XplorOne 返回的结构化结果，并由外部 agent 自己负责解释和组织回答。

## 不适合做什么

当前 Local API / MCP 路径不应被当作：

- 自动记账写入器
- 删除或编辑工具
- 直接 SQLite 读取入口
- 公开 Web API
- 面向其他用户的托管服务
- 会计、税务、审计或法律决策引擎
- 绕过 XplorOne 写入确认边界的方式

## Token 与本地访问

本地 API 和 MCP 访问通过本地 token 保护。

Token 边界包括：

- Local API token 用于保护本地 HTTP 访问。
- MCP client token 用于授权外部 agent 客户端。
- Token 应被视为 secret。
- 不应把 token 粘贴到公开 issue、日志、截图或共享 prompt 中。
- 在支持范围内，token 应可以从应用设置中移除、重置或重新生成。

MCP client token 会被视为受保护的本地凭据，在可用时应通过 Electron `safeStorage` 或等效的系统级本地机制保存。

## 当前激活账本范围

当前 MCP / query 路径围绕当前激活账本设计。

用户不应默认 MCP 可以查询所有归档账本、所有备份或当前应用范围外的所有账户。

如果问题依赖特定账本，请先在 XplorOne 中打开或激活对应账本。

## 隐私与安全提示

只读不代表不敏感。

查询结果仍可能包含私人财务信息。除非已经脱敏，否则不要把 MCP 输出粘贴到公开 issue 或第三方系统。

更多说明见：

- [隐私说明](../PRIVACY_zh-CN.md)
- [隐私与 AI 边界](./privacy-and-ai-boundaries_zh-CN.md)
- [安全说明](../SECURITY_zh-CN.md)

