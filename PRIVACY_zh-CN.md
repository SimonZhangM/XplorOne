[English](./PRIVACY.md) | 简体中文

# 隐私说明

最后更新：2026-04-30

这份文档说明 XplorOne 桌面产品、GitHub 仓库、下载、支持和公开材料中的隐私处理口径。

XplorOne 被设计为本地优先的桌面财务工作台。本文件用于帮助用户理解产品边界和公开信任基础，不替代适用的 EULA、第三方服务条款或当地法律要求。

## 默认本地数据

XplorOne 的核心财务工作流围绕本地应用数据设计。

默认情况下，你的账本、账户、分类、流水、报表、预算、本地设置和相关工作区数据保存在你自己的桌面环境中。

核心记账、报表、财务视图和受支持的本地查询不需要模型 API Key。

XplorOne 不以默认上传完整本地数据库到云端会计系统为前提。

## 可选 AI 与模型服务商

AI 辅助能力是可选的。

当你使用 AI 辅助工作流时，XplorOne 可能会把完成当前任务所需的相关上下文发送给你自行配置的模型服务。

根据具体工作流，可能包括：

- 当前问题或指令
- 当前任务所需的结构化财务上下文
- 选定的报表或查询上下文
- 录入草稿上下文
- 最近对话上下文
- 与当前回复语言匹配的 AI 个性化摘要，仅在你启用个性化时使用

XplorOne 的目标是发送与任务相关的上下文，而不是默认发送整个本地数据库。

模型服务商可能会按照其自身条款和隐私实践处理数据。用户应选择自己信任的服务商。

## API Key 与本地 Token

XplorOne 可能处理几类凭据：

- **模型 API Key**：用于连接用户选择的模型服务。
- **本地 API Token**：用于保护本地 HTTP API 访问。
- **MCP Client Token**：用于授权外部 agent 使用本地只读 MCP / query 路径。

这些凭据类型不同，作用也不同。

模型 API Key 和 MCP Client Token 会被视为敏感的本地凭据。XplorOne 的设计目标是在可用时通过 Electron `safeStorage` 或等效的系统级本地凭据保护机制保存受保护凭据。

用户不应公开分享 API Key、本地 API Token、MCP Token、授权码、包含密钥的本地 endpoint、暴露凭据的截图或未脱敏日志。

## 备份、导出、日志和支持材料

备份、导出、归档包、日志、截图和 issue 附件可能包含敏感财务信息或本地环境信息。

公开分享前，请移除：

- 私人财务记录
- 模型 API Key
- 本地 API Token
- MCP Client Token
- 授权码
- 完整数据库文件
- 完整备份
- 含真实数据的账本导出文件
- 个人身份信息
- 本地用户名、私人路径或服务商账户细节

如果需要样例，请使用虚构或脱敏数据。

## GitHub、官网、下载与邮件支持

GitHub、官网、下载页、Release 页面、Discussions、Issues 和邮件支持等公开渠道可能涉及用户主动提供的有限信息。

这可能包括：

- GitHub 用户名和公开评论
- issue 或 discussion 内容
- GitHub 或托管服务可见的下载相关上下文
- 联系支持时的邮箱地址和邮件内容
- 用户提供的脱敏截图、日志或示例

请不要在公开 GitHub Issues 或 Discussions 中提交敏感财务数据。

安全敏感或隐私问题请通过邮件联系：

- simonzhang2026@163.com

## 第三方服务

XplorOne 可能依赖第三方系统完成分发、托管、GitHub 仓库功能、模型服务连接、操作系统服务和软件组件打包。

第三方组件和服务仍受其自身条款和隐私实践约束。

第三方组件说明见 [THIRD_PARTY_NOTICES.md](./THIRD_PARTY_NOTICES.md)。

## 用户责任

本地优先软件仍需要用户谨慎处理数据。

用户需要负责：

- 保护自己的电脑账户
- 选择可信任的模型服务商
- 妥善保存备份和导出文件
- 在凭据暴露时轮换 key 或 token
- 在采取行动前审阅 AI 输出
- 在账本写入前确认相关操作

## 相关文档

- [隐私与 AI 边界](./docs/privacy-and-ai-boundaries_zh-CN.md)
- [数据保存与备份](./docs/data-storage-and-backup_zh-CN.md)
- [BYOK 配置说明](./docs/byok-setup_zh-CN.md)
- [安全说明](./SECURITY_zh-CN.md)
- [支持说明](./SUPPORT_zh-CN.md)

