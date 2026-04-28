[English](./SUPPORT.md) | 简体中文

# 支持与反馈

这份文档说明：在使用 XplorOne 时，如果遇到问题、想提建议或需要反馈 bug，应该去哪里、提供哪些信息、哪些内容不要公开发布。

XplorOne 是一款本地优先的桌面财务工作台。它可能涉及财务数据、模型 API Key、本地 token、备份文件和截图。因此，在公开反馈前，请先阅读下面的敏感信息说明。

## 1. 提问前可以先看什么

在新建 Issue 或 Discussion 之前，建议先查看：

- [快速开始](./docs/getting-started_zh-CN.md)
- [功能导览](./docs/feature-overview_zh-CN.md)
- [常见问题](./docs/faq_zh-CN.md)
- [当前限制说明](./docs/known-limitations_zh-CN.md)
- [BYOK 配置说明](./docs/byok-setup_zh-CN.md)
- [隐私与 AI 边界](./docs/privacy-and-ai-boundaries_zh-CN.md)
- [Releases](https://github.com/SimonZhangM/XplorOne/releases)

除非你正在测试旧版本，否则建议先确认自己使用的是当前最新可用版本。

## 2. 不同问题应该去哪里

### 一般问题、想法和使用讨论

请使用 [Discussions](https://github.com/SimonZhangM/XplorOne/discussions) 处理：

- 产品问题
- 使用问题
- 功能想法
- 工作流反馈
- 文档建议
- 早期用户体验反馈

如果问题还在探索阶段，或者不确定是不是 bug，优先放到 Discussions。

### bug 和明确可处理的问题

请使用 [Issues](https://github.com/SimonZhangM/XplorOne/issues) 处理：

- 可复现 bug
- 安装问题
- 崩溃
- 界面异常
- 结果不正确
- 明确的功能缺陷
- 可复现的模型配置问题
- 可清楚描述的 MCP 或本地 API 问题

Issue 最适合提交有复现步骤、环境信息、预期结果和实际结果的问题。

提交 Issue 时，请优先使用仓库提供的 Issue 表单，不要提交空白或一句话问题。

### 安全或敏感问题

请不要公开发布安全敏感信息。

敏感问题请通过邮件联系：

- simonzhang2026@163.com

适合通过私下方式反馈的问题包括：

- token 暴露
- API Key 暴露
- 疑似凭据保存问题
- 私人财务数据暴露
- 与安装或更新相关的安全敏感问题

### 商业、授权、OEM 或合作咨询

如需咨询授权、再分发、集成、OEM、白标或商业合作，请联系：

- simonzhang2026@163.com
- www.xplorone.com

## 3. 哪些内容不要公开发布

请不要在公开 Issues 或 Discussions 中发布：

- 模型 API Key
- 本地 API token
- MCP client token
- 授权码
- 私人财务记录
- 真实银行流水
- 导出的账本文件
- 完整备份文件
- 未脱敏日志
- 含私人财务数据的截图
- 个人身份信息
- 模型服务商账户细节

发布截图或日志前，请先移除敏感信息。

## 4. 提交 bug 时应该包含什么

一份有用的 bug 报告通常包括：

- XplorOne 版本
- Windows 版本
- 问题发生的位置
- 你原本想做什么
- 复现步骤
- 预期结果
- 实际结果
- 必要时的脱敏截图
- 是否涉及 AI、BYOK、本地 API、MCP、导入导出、备份或安装器

建议格式：

```text
XplorOne 版本：
Windows 版本：
页面或功能：
我原本想做什么：
复现步骤：
预期结果：
实际结果：
是否涉及 AI / BYOK / MCP / 导入 / 备份：
截图或日志：
敏感信息是否已移除：是 / 否
```

## 5. 安装或 Windows 版本问题

如果是安装、更新、重装或卸载问题，请提供：

- XplorOne 版本
- 安装包文件名
- 下载来源
- Windows 版本
- 安装包是否来自 GitHub Releases 或官方网站
- 报错信息或截图
- 这是首次安装、更新、重装还是卸载问题

如果安装日志里包含私人路径、token、用户名或其他敏感信息，请先脱敏后再发布。

## 6. AI 或 BYOK 问题

如果是 AI 或 BYOK 配置问题，请提供：

- provider 名称
- base URL 类型，但不要提供 secret 值
- model name
- 测试连接是否通过
- 使用的是哪个助手：
  - 本地助手
  - AI 助手
- 涉及哪种能力：
  - 查询
  - 录入
  - 分析
  - 自由对话
- 输入语言
- 期望回复语言
- 实际回复语言
- 报错信息，如有

请不要提供你的 API Key。

配置说明请见：[BYOK 配置说明](./docs/byok-setup_zh-CN.md)。

## 7. 本地 API 或 MCP 问题

如果是本地 API 或 MCP 相关问题，请提供：

- XplorOne 版本
- 外部客户端名称，例如 Codex 或 WorkBuddy
- 问题发生在本地 API、MCP，还是两者都有
- 尝试调用的工具或查询
- 预期结果
- 实际结果
- 相关错误信息
- 当时 XplorOne 是否正在运行

请不要提供：

- 本地 API token
- MCP client token
- 带有 secret token 的完整 endpoint
- 私人财务查询结果

当前 MCP 路径是只读的，并且会经过 XplorOne 受控的本地 API 与查询链路，不会直接读取数据库。

详细说明请见：[隐私与 AI 边界](./docs/privacy-and-ai-boundaries_zh-CN.md)。

## 8. 导入、导出、备份或数据问题

如果是数据相关问题，请提供：

- XplorOne 版本
- 操作类型：
  - 备份
  - 恢复
  - 导出
  - 导入
  - 归档
  - `.xpl` 工作流
- 来源文件类型
- 是当前账本数据还是归档账本数据
- 你原本预期会发生什么
- 实际发生了什么
- 报错信息，如有

请不要公开上传私人财务文件。

如果需要样例文件，请创建虚构或脱敏样例，不要使用真实财务数据。

## 9. 功能建议

功能建议欢迎放在 [Discussions](https://github.com/SimonZhangM/XplorOne/discussions)。

一条有帮助的功能建议通常会说明：

- 你想解决什么问题
- 现在是怎么绕开的
- 为什么现有工作流不够
- 这是个人、自由职业、工作室还是业务经营场景
- 这个需求和记账、报表、AI、导入导出、MCP 还是设置有关

请尽量避免把功能建议写成“大而全产品需求”。XplorOne 当前有意聚焦于面向超级个体和小型工作室的本地优先财务工作流。

## 10. 回复预期

公开支持会尽量处理，但不承诺即时回复。

清楚、可复现的问题更容易被调查。

如果公开反馈中包含敏感数据，相关内容可能会被编辑、关闭或移除。

商业支持条款如有，将与公开 GitHub 支持分开处理。

## 11. 常用链接

- [README](./README_zh-CN.md)
- [快速开始](./docs/getting-started_zh-CN.md)
- [功能导览](./docs/feature-overview_zh-CN.md)
- [常见问题](./docs/faq_zh-CN.md)
- [当前限制说明](./docs/known-limitations_zh-CN.md)
- [BYOK 配置说明](./docs/byok-setup_zh-CN.md)
- [隐私与 AI 边界](./docs/privacy-and-ai-boundaries_zh-CN.md)
- [Releases](https://github.com/SimonZhangM/XplorOne/releases)
- [Discussions](https://github.com/SimonZhangM/XplorOne/discussions)
- [Issues](https://github.com/SimonZhangM/XplorOne/issues)
