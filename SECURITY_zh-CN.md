[English](./SECURITY.md) | 简体中文

# 安全说明

最后更新：2026-04-30

这份文档说明如何反馈 XplorOne 的安全敏感问题。

## 支持版本

安全审查和修复优先面向当前公开 Windows 版本和近期公开发布线。

用户应从官方来源下载 XplorOne：

- [GitHub Releases](https://github.com/SimonZhangM/XplorOne/releases)
- 可用时的官方网站

旧版本不一定获得同等程度的审查、文档更新或兼容性修复。

## 反馈安全问题

请不要在公开 GitHub Issues 或 Discussions 中提交安全敏感问题。

安全敏感问题请发送至：

- simonzhang2026@163.com

有帮助的报告通常包括：

- XplorOne 版本
- Windows 版本
- 安装包或更新来源
- 受影响区域
- 复现步骤
- 预期行为
- 实际行为
- 仅在脱敏后提供截图或日志

## 不要公开分享

请不要公开发布：

- 模型 API Key
- 本地 API Token
- MCP Client Token
- 授权码
- 完整本地数据库
- 完整备份
- 含真实数据的账本导出文件
- 未脱敏日志
- 含财务数据或凭据的截图
- 包含 secret token 的本地 endpoint

## 安全范围

安全敏感区域可能包括：

- 安装包和更新行为
- 本地凭据保存
- 模型 API Key 处理
- 本地 API Token 处理
- MCP Client Token 处理
- 本地 API 访问边界
- 只读 MCP / query 行为
- 备份、导出、归档和恢复处理
- 发布打包中误带私有运行时数据的风险
- 涉及敏感财务上下文的 AI 请求边界

## 非安全问题

普通产品反馈、bug、文档问题、功能建议、安装问题或不暴露敏感信息的模型配置问题，请使用 GitHub Issues 或 Discussions。

- [Issues](https://github.com/SimonZhangM/XplorOne/issues)
- [Discussions](https://github.com/SimonZhangM/XplorOne/discussions)
- [支持说明](./SUPPORT_zh-CN.md)

