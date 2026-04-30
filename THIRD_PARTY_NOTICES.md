# XplorOne Third-Party Notices

Last Updated: 2026-04-30

This file provides the first notice-and-attribution baseline for third-party software components relevant to XplorOne.

This file is informational only. It does not replace any original third-party license text, and it does not modify the terms of any third-party license.

Methodology:

- This document is based on the current repository dependency tree (`package.json`, `package-lock.json`, and installed packages).
- For desktop releases, the final compliance checkpoint is the actual bundled content present in the shipped Electron desktop artifact.
- This file does not assume that every transitive package must be reproduced in full; it records the materials verified in the current repository and current desktop packaging route.

## 1. How to read this file

For each component, this file records:

- component name and version;
- declared license from the current installed package metadata;
- upstream project URL;
- whether the component is runtime/bundled or build-time/dev-only in the current release model;
- any verified notice or license file already present in the current package or shipped runtime.

Unless otherwise stated, the existence of a component in this file does not itself grant any rights beyond that component's own license.

## 2. Runtime / Bundled Components

The current official product line is the Electron desktop release. The following components are part of, or directly relevant to, the current runtime/bundled distribution path.

| Component | Version | License | Upstream URL | Bundled With Product | Verified Notice / License Material |
|---|---:|---|---|---|---|
| Electron | 41.2.0 | MIT | https://github.com/electron/electron | Yes | `node_modules/electron/dist/LICENSE`; `node_modules/electron/dist/LICENSES.chromium.html` present in Electron runtime |
| React | 18.3.1 | MIT | https://github.com/facebook/react | Yes | `node_modules/react/LICENSE` |
| React DOM | 18.3.1 | MIT | https://github.com/facebook/react | Yes | `node_modules/react-dom/LICENSE` |
| Express | 5.2.1 | MIT | https://expressjs.com/ | Yes | `node_modules/express/LICENSE` |
| better-sqlite3 | 12.8.0 | MIT | http://github.com/WiseLibs/better-sqlite3 | Yes | `node_modules/better-sqlite3/LICENSE` |
| Zod | 3.25.76 | MIT | https://github.com/colinhacks/zod | Yes | `node_modules/zod/LICENSE` |
| @modelcontextprotocol/sdk | 1.29.0 | MIT | https://github.com/modelcontextprotocol/typescript-sdk | Yes | package metadata verified; no separate NOTICE file found at package root |

### Runtime notes

- Electron runtime distribution already includes its own `LICENSE` and `LICENSES.chromium.html`. Those files are the primary verified notice materials for Electron and Chromium-related bundled content in the current desktop runtime.
- XplorOne also ships its own legal materials separately via `resources/legal/` in the desktop package configuration.
- The runtime dependency tree also includes transitive packages through the components above. For this first notice baseline, the components listed here are the major verified runtime packages directly relevant to current desktop distribution.

## 3. Build-Time / Dev-Only Components

The following components are present in the repository build or packaging workflow but are not themselves the current end-user runtime of the desktop product.

| Component | Version | License | Upstream URL | Build-Time Only | Verified Notice / License Material |
|---|---:|---|---|---|---|
| electron-builder | 26.8.1 | MIT | https://github.com/electron-userland/electron-builder | Yes | `node_modules/electron-builder/LICENSE` |
| Vite | 5.4.21 | MIT | https://github.com/vitejs/vite | Yes | `node_modules/vite/LICENSE.md` includes Vite license and bundled dependency license summary |
| TypeScript | 5.9.3 | Apache-2.0 | https://github.com/microsoft/TypeScript | Yes | `node_modules/typescript/LICENSE.txt`; `node_modules/typescript/ThirdPartyNoticeText.txt` |
| @vitejs/plugin-react | 4.7.0 | MIT | https://github.com/vitejs/vite-plugin-react | Yes | package metadata verified; no separate NOTICE file found at package root |

### Build-time notes

- TypeScript includes `ThirdPartyNoticeText.txt` in the installed package. This file is verified in the current repository, but TypeScript itself is build-time/dev-only in the current release route and is not the end-user runtime of the desktop app.
- Vite's `LICENSE.md` explicitly notes bundled dependency licenses inside the published Vite artifact. In the current XplorOne release model, this remains build-time/dev-only rather than a shipped desktop runtime dependency.

## 4. Verified License / Notice Materials

The following verified files exist in the current repository or shipped Electron runtime and are the basis of this first notice baseline:

### 4.1 Electron runtime materials

- `node_modules/electron/dist/LICENSE`
- `node_modules/electron/dist/LICENSES.chromium.html`

### 4.2 TypeScript build-time materials

- `node_modules/typescript/LICENSE.txt`
- `node_modules/typescript/ThirdPartyNoticeText.txt`

### 4.3 Vite build-time materials

- `node_modules/vite/LICENSE.md`

## 5. Exclusions / Notes

- This file is not a statement that every transitive dependency currently requires full-text reproduction in the shipped desktop product.
- The final runtime compliance checkpoint is the actual bundled content included in the desktop release artifact.
- Some transitive dependencies are used only during building, bundling, or development and are not currently shipped as user-facing runtime components.
- If the packaging route changes, especially if new installers, auto-update, web-hosted components, or additional bundled libraries are introduced, this file should be re-verified.

## 6. Maintenance Process

When dependencies or packaging change, update this file by:

1. Re-reading `package.json` and `package-lock.json`
2. Re-checking installed package metadata and verified license/notice files
3. Re-checking actual desktop release contents
4. Updating runtime/bundled vs build-time/dev-only classification
5. Adding any newly verified notice or full-text materials that become relevant

---

# XplorOne 第三方软件声明

最后更新日期：2026.5.1

本文件为 XplorOne 第三方软件组件的第一版声明与归属清单。

本文件仅用于信息说明，不替代任何第三方许可证原文，也不改变任何第三方许可证的原始条款。

编制方法：

- 本文件以当前仓库依赖树（`package.json`、`package-lock.json` 及已安装依赖）为基础；
- 对于桌面正式发布，最终核验标准以实际被打进 Electron 桌面发布产物的 bundled contents 为准；
- 本文件不预设“所有传递依赖都必须全文复制”，而是记录当前仓库中已核验到的许可证与 notice 材料。

## 1. 阅读方式

本文件为每个组件记录：

- 组件名称与版本；
- 当前已安装包元数据中的许可证声明；
- 上游项目地址；
- 在当前发布模型下属于 runtime/bundled 还是 build-time/dev-only；
- 当前仓库或运行时中已核验到的 notice / license 文件。

除非另有说明，列出组件并不代表其许可证之外的任何额外授权。

## 2. Runtime / Bundled Components

当前官方产品线为 Electron 桌面版。以下组件属于当前运行时或与当前桌面分发路径直接相关的组件。

| 组件 | 版本 | 许可证 | 上游地址 | 是否随产品分发 | 已核验材料 |
|---|---:|---|---|---|---|
| Electron | 41.2.0 | MIT | https://github.com/electron/electron | 是 | `node_modules/electron/dist/LICENSE`；`node_modules/electron/dist/LICENSES.chromium.html` |
| React | 18.3.1 | MIT | https://github.com/facebook/react | 是 | `node_modules/react/LICENSE` |
| React DOM | 18.3.1 | MIT | https://github.com/facebook/react | 是 | `node_modules/react-dom/LICENSE` |
| Express | 5.2.1 | MIT | https://expressjs.com/ | 是 | `node_modules/express/LICENSE` |
| better-sqlite3 | 12.8.0 | MIT | http://github.com/WiseLibs/better-sqlite3 | 是 | `node_modules/better-sqlite3/LICENSE` |
| Zod | 3.25.76 | MIT | https://github.com/colinhacks/zod | 是 | `node_modules/zod/LICENSE` |
| @modelcontextprotocol/sdk | 1.29.0 | MIT | https://github.com/modelcontextprotocol/typescript-sdk | 是 | 已核验包元数据；包根目录未发现单独 NOTICE 文件 |

### 运行时说明

- Electron 运行时分发中已自带 `LICENSE` 与 `LICENSES.chromium.html`，这是当前桌面运行时下 Electron / Chromium 相关内容的主要已核验 notice 材料。
- XplorOne 另外会通过 `resources/legal/` 路径附带自身法律文件。
- 上述组件仍可能带有传递依赖；本第一版文件主要覆盖当前桌面分发中最重要且已核验的主要组件。

## 3. Build-Time / Dev-Only Components

以下组件存在于当前仓库的构建、打包或开发链路中，但并非最终用户运行桌面产品时的主运行时。

| 组件 | 版本 | 许可证 | 上游地址 | 是否仅构建期 | 已核验材料 |
|---|---:|---|---|---|---|
| electron-builder | 26.8.1 | MIT | https://github.com/electron-userland/electron-builder | 是 | `node_modules/electron-builder/LICENSE` |
| Vite | 5.4.21 | MIT | https://github.com/vitejs/vite | 是 | `node_modules/vite/LICENSE.md`，含 Vite 自身及其 bundled dependency 的许可证摘要 |
| TypeScript | 5.9.3 | Apache-2.0 | https://github.com/microsoft/TypeScript | 是 | `node_modules/typescript/LICENSE.txt`；`node_modules/typescript/ThirdPartyNoticeText.txt` |
| @vitejs/plugin-react | 4.7.0 | MIT | https://github.com/vitejs/vite-plugin-react | 是 | 已核验包元数据；包根目录未发现单独 NOTICE 文件 |

### 构建期说明

- TypeScript 安装包中包含 `ThirdPartyNoticeText.txt`。该文件已在当前仓库中核验到，但 TypeScript 在当前发布方式下属于 build-time/dev-only，而非最终桌面产品运行时。
- Vite 的 `LICENSE.md` 明确包含其 bundled dependency 的许可证摘要，但在当前 XplorOne 发布模型中，Vite 仍属构建期组件。

## 4. 已核验的许可证 / Notice 材料

以下文件已在当前仓库或 Electron 运行时中核验到，是本第一版声明的事实基础：

### 4.1 Electron 运行时材料

- `node_modules/electron/dist/LICENSE`
- `node_modules/electron/dist/LICENSES.chromium.html`

### 4.2 TypeScript 构建期材料

- `node_modules/typescript/LICENSE.txt`
- `node_modules/typescript/ThirdPartyNoticeText.txt`

### 4.3 Vite 构建期材料

- `node_modules/vite/LICENSE.md`

## 5. 排除与说明

- 本文件并不表示当前所有传递依赖都必须在最终桌面产品中逐项全文复制。
- 最终运行时合规核验应以实际桌面发布产物中包含的 bundled contents 为准。
- 某些传递依赖仅用于构建、打包或开发，在当前产品形态下并不会作为最终用户运行时组件被分发。
- 如果未来引入安装器、自动更新、额外 bundled 库或新的分发方式，应重新核验本文件。

## 6. 维护流程

当依赖或打包方式发生变化时，应按以下步骤更新本文件：

1. 重新读取 `package.json` 与 `package-lock.json`
2. 重新核验已安装包元数据与许可证/notice 文件
3. 重新检查实际桌面发布产物中的内容
4. 重新确认 runtime/bundled 与 build-time/dev-only 的分类
5. 将新增或变化的 notice / full-text 材料补入本文件
