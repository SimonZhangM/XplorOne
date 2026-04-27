D:\APP\marketing\github\
├── [✓] README.md                             ← 英文仓库首页；作为 GitHub 首屏产品介绍，优先讲价值、定位、下载入口与反馈入口
├── [✓] README_zh-CN.md                       ← 中文仓库首页；用于中文读者快速理解产品定位、能力边界与主要资料入口
├── [✓] CHANGELOG.md                          ← 根目录英文摘要版变更记录；用于快速查看主要版本变化与关键更新
├── [ ] ROADMAP.md                            ← 公开路线图；用于说明后续方向、阶段性重点与暂不处理的事项
├── [✓] SUPPORT.md                            ← 支持与反馈说明；用于承接用户提问、反馈渠道与基本求助方式
├── [ ] LICENSE                               ← 开源许可证文件；用于明确仓库代码与内容的授权边界
├── [ ] LICENSE-NOTICE.md                     ← 许可证补充说明；用于解释非标准授权、资源归属或商业限制
├── [✓] GITHUB_REPO_MEMORY.md                 ← 仓库工作记忆文件；用于沉淀当前 GitHub 仓库的定位、约束与维护口径
├── [✓] Github_Structure.md                   ← 仓库结构说明；用于记录当前已完成与待补齐的 GitHub 文件布局
├── [✓] .gitignore                            ← Git 忽略规则；用于排除本地生成文件、缓存文件与不应提交的临时内容
├── [ ] .github/                              ← GitHub 仓库自动化与协作配置目录；用于放 issue 模板、PR 模板、Actions 等
│   ├── [ ] ISSUE_TEMPLATE/                   ← Issue 模板目录；用于规范 bug、feature request、question 等提交格式
│   │   └── [ ] bug_report.yml                ← Bug 模板；用于收集复现步骤、环境信息与影响范围
│   ├── [ ] PULL_REQUEST_TEMPLATE.md          ← PR 模板；用于统一变更说明、验证方式与风险提示
│   └── [ ] workflows/                        ← GitHub Actions 工作流目录；用于自动检查、发布或同步任务
├── [✓] docs/                                 ← 长文档目录；用于承接 README 之外的详细说明、功能介绍、版本历史和专题页面
│   ├── [ ] getting-started.md                ← 英文快速开始指南；用于新用户首次下载、安装、上手和基本路径说明
│   ├── [ ] getting-started_zh-CN.md          ← 中文快速开始指南；用于中文用户的首次安装与使用路径说明
│   ├── [✓] feature-overview.md               ← 英文功能总览；用于概览核心能力、产品边界与典型使用方式
│   ├── [✓] feature-overview_zh-CN.md         ← 中文功能总览；用于中文读者快速理解主要能力与使用价值
│   ├── [✓] software-release-history.md       ← 英文详细版用户向 release notes；用于面向真实用户记录版本演进
│   ├── [✓] software-release-history_zh-CN.md ← 中文详细版用户向 release notes；用于中文环境下的版本历史说明
│   ├── [ ] privacy-and-ai-boundaries.md      ← 英文隐私与 AI 边界说明；用于解释本地优先、确认写入与数据边界
│   ├── [ ] privacy-and-ai-boundaries_zh-CN.md← 中文隐私与 AI 边界说明；用于中文读者理解产品信任边界
│   ├── [ ] known-limitations.md              ← 英文已知限制说明；用于说明当前未覆盖的平台、能力边界与注意事项
│   ├── [ ] known-limitations_zh-CN.md        ← 中文已知限制说明；用于减少错误预期并提前解释限制
│   ├── [ ] byok-setup.md                     ← 英文 BYOK 配置指南；用于说明 API Key 配置方式与注意点
│   ├── [ ] byok-setup_zh-CN.md               ← 中文 BYOK 配置指南；用于中文用户理解模型配置方式
│   ├── [ ] faq.md                            ← 英文 FAQ；用于集中回答下载、定位、AI、平台、数据边界等常见问题
│   ├── [ ] faq_zh-CN.md                      ← 中文 FAQ；用于中文环境下的常见问题解释
│   └── [ ] assets/                           ← 文档素材目录；用于放 README、功能页、发布页引用的截图、GIF 和说明图
│      ├── [ ] xplorone-main-screenshot.png   ← 主界面总览图；用于展示工作台第一印象
│      ├── [ ] xplorone-ai-query.png          ← AI 查询界面图；用于展示对话与查询能力
│      ├── [ ] xplorone-reports.png           ← 报表界面图；用于展示图表与经营视角
│      └── [ ] xplorone-budget.png            ← 预算界面图；用于展示分类、预算和秩序感
├── [ ] community/                            ← 社区内容目录；用于放欢迎帖、社区说明和长期讨论入口
│   └── [ ] welcome-to-xplorone.md            ← 社区欢迎帖；用于说明仓库定位、反馈方式与 Discussions 使用规则
└── [ ] releases/                             ← 可选发布素材目录；用于整理 release 文案、截图清单、发布配图或下载说明

说明：

- `[✓]` 表示当前 `github` 目录中已经存在的文件或文件夹
- `[ ]` 表示结构规划里应有、但当前仓库中还未落地的文件或文件夹
- 当前实际已存在、且旧结构文档未覆盖的内容，已补入：
  - `GITHUB_REPO_MEMORY.md`
  - `.gitignore`
  - `docs/feature-overview.md`
  - `docs/feature-overview_zh-CN.md`
- 当前旧结构文档里已出现、但仓库暂未落地的内容，保留为待补齐项：
  - `ROADMAP.md`
  - `LICENSE`
  - `LICENSE-NOTICE.md`
  - `getting-started.*`
  - `privacy-and-ai-boundaries.*`
  - `known-limitations.*`
  - `byok-setup.*`
  - `faq.*`
  - `.github/`
  - `community/`
  - `docs/assets/`
