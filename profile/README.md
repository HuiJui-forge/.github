<div align="center">

<img src="https://raw.githubusercontent.com/HuiJui-forge/.github/main/profile/avatar.png" width="120" alt="huijui forge" />

# huijui forge

**Android Root 工具与模块生态**

[![Website](https://img.shields.io/badge/官网-huijui--forge.github.io-3ee6c4?style=flat-square)](https://huijui-forge.github.io/)
[![Release](https://img.shields.io/github/v/release/HuiJui-forge/HuijuiSU?style=flat-square&label=release)](https://github.com/HuiJui-forge/HuijuiSU/releases/latest)
[![License](https://img.shields.io/github/license/HuiJui-forge/HuijuiSU?style=flat-square)](https://github.com/HuiJui-forge/HuijuiSU/blob/main/LICENSE)
[![Telegram](https://img.shields.io/badge/Telegram-群组-26A5E4?style=flat-square&logo=telegram)](https://t.me/Huijui123)

</div>

---

huijui forge 是一个小型开源团队，专注 **Android Root 工具链与模块生态**。

我们做的不是单个 App，而是一套能互相配合的东西：管理器、隐藏模块、模块仓库、工具箱、官网。
每个项目单独可用，组合起来才是一套完整方案。

---

## 项目总览

| 项目 | 一句话 | 类型 |
|---|---|---|
| [**HuiJuiSU**](#huijuisu) | 基于 KernelSU 的 Root 管理器 | Android App + 内核 |
| [**Snow-love-Module**](#snow-love-module) | 一键隐藏模块（恋雪） | Magisk/KSU 模块 |
| [**Huijui_Module_Repo**](#huijui_module_repo) | 模块索引与更新源 | 数据仓库 |
| [**HuiJui-Toolbox**](#huijui-toolbox) | 常用 Root 操作脚本集合 | Shell 脚本 |
| [**huijui-forge.github.io**](#官网) | 项目官网与文档 | 静态站点 |

---

## HuiJuiSU

> 基于 KernelSU 的 Root 管理器，把隐藏这件事整个收进来。

**它能做什么**

| 能力 | 说明 |
|---|---|
| 内置一键隐藏 | 隐藏所需的 5 个模块随 APK 分发，首次启动自动部署 |
| 真·热刷入 | 接入 Hybrid Mount runtime，纯 VFS 计划的模块装完即挂载 |
| 开机秒激活 | `huijui_core` 在开机过程中完成配置，重启后自动生效 |
| 极客工具箱 | 12 张卡片：boot 备份、SystemUI 重启、缓存清理、Evil 自查、春秋修复等 |
| 核心防误删 | 内置隐藏模块禁止卸载与停用 |
| 稳定性 | root 调用多路径回退 + 超时，不再卡死 |

**适合谁**

- 想要「刷完就能用」的 KernelSU 用户
- 被检测困扰，但不想手动装五个模块、导配置、写名单的人
- 需要 GKI LKM 与内核补丁两种路线的设备

**链接**：[仓库](https://github.com/HuiJui-forge/HuijuiSU) · [下载](https://github.com/HuiJui-forge/HuijuiSU/releases/latest) · [安装文档](https://huijui-forge.github.io/install.html)

---

## Snow-love-Module

> 一键隐藏模块（78 整合 · 恋雪），HuiJuiSU 内置的那一个就是它。

**包含什么**

| 组件 | 作用 |
|---|---|
| Zygisk Next 1.5.2 | Zygisk 运行环境 |
| LSPosed | 模块框架 |
| HMA-OSS UID3.1 | 隐藏应用列表 |
| OhMyKeymint | 提供 keybox |
| PIF-Dates | Play Integrity 修复 |

外带 HMA 管理端、预置 HMA 配置、预置 keybox、春秋修复等脚本，
以及一个可视化 WebUI：补装、重扫名单、换 keybox、导入配置、查日志。

**适合谁**

- 想单独刷隐藏模块、不用完整管理器的用户
- 想改脚本、换配置、自己二次开发的人
- 需要看源码确认行为的人

**链接**：[仓库](https://github.com/HuiJui-forge/Snow-love-Module) · [Release v1.4](https://github.com/HuiJui-forge/Snow-love-Module/releases/tag/v1.4)

---

## Huijui_Module_Repo

> 模块索引与更新源：管理器里浏览模块、检查更新都走它。

**做什么**

- 维护模块清单（id、名称、版本、下载地址、更新 JSON）
- 提供管理器可读的索引格式
- 模块作者提交新版本时更新条目

**适合谁**

- 想在管理器内直接浏览/安装模块的用户
- 想把自己模块收录进来的开发者

**链接**：[仓库](https://github.com/HuiJui-forge/Huijui_Module_Repo)

---

## HuiJui-Toolbox

> 常用 Root 操作脚本集合，给不想记命令的人。

**包含**

| 脚本 | 用途 |
|---|---|
| 备份 boot | `dd` 导出 boot 分区到 Download |
| 重启 SystemUI | 状态栏卡死时自救 |
| 清理缓存 | `drop_caches` 释放内存 |
| 清理临时文件 | `/data/local/tmp` 与安装残留 |
| Evil Service 自查 | 扫描可疑服务 |
| 春秋词条修复 | 系统属性异常修复 |

**适合谁**

- 常在终端里敲命令的玩机用户
- 想把这些操作固化成脚本的人

**链接**：[仓库](https://github.com/HuiJui-forge/HuiJui-Toolbox)

---

## 官网

> 项目文档站，六语言，纯静态。

**有什么**

- 功能详情（每张卡片可展开）
- 安装步骤（LKM 与内核补丁两条路线）
- 兼容性表（8 个 KMI）
- FAQ、关于、更新日志
- 六语言切换：简中 / 繁中 / 英 / 日 / 韩 / 俄

**链接**：[网站](https://huijui-forge.github.io/) · [源码](https://github.com/HuiJui-forge/huijui-forge.github.io)

---

## 技术栈

| 层 | 使用 |
|---|---|
| 管理器 | Kotlin + Jetpack Compose，AGP / Gradle |
| 内核 | C，KernelSU 分支，LKM 与内核补丁双路线 |
| 用户态 | Rust / C（ksud、ksuinit） |
| 模块脚本 | Shell，Magisk/KSU 模块规范 |
| 官网 | 原生 HTML / CSS / JS，零依赖，GitHub Pages |
| 构建 | GitHub Actions，多 ABI + 多 KMI 矩阵 |

---

## 路线

| 阶段 | 目标 | 状态 |
|---|---|---|
| 5.0 | 内置资源、热刷入、工具箱、稳定化 | ✅ 已完成 |
| 5.1 | 一键隐藏全流程自动化、模块仓库接入 | 进行中 |
| 5.2 | 多设备兼容性扩展、错误自诊断 | 计划中 |

---

## 安全

- 核心模块禁止卸载与停用，避免误操作破坏隐藏链路
- 所有 root 调用带超时与多路径回退，不会无限阻塞
- 漏洞报告请走 [SECURITY.md](SECURITY.md)，不要公开 Issue

---

## Languages · 语言

<details>
<summary><b>简体中文</b></summary>

huijui forge 是一个小型开源团队，专注 Android Root 工具与模块生态。
我们维护五个项目：Root 管理器 HuiJuiSU、隐藏模块 Snow-love-Module、
模块仓库 Huijui_Module_Repo、工具脚本 HuiJui-Toolbox，以及官网。

</details>

<details>
<summary><b>繁體中文</b></summary>

huijui forge 是一個小型開源團隊，專注 Android Root 工具與模組生態。
我們維護五個專案：Root 管理器 HuiJuiSU、隱藏模組 Snow-love-Module、
模組倉庫 Huijui_Module_Repo、工具腳本 HuiJui-Toolbox，以及官網。

</details>

<details>
<summary><b>English</b></summary>

huijui forge is a small open-source team focused on Android root tooling
and module tooling. We maintain five projects: the HuiJuiSU root manager,
the Snow-love-Module hiding module, the Huijui_Module_Repo module index,
the HuiJui-Toolbox script collection, and the documentation site.

</details>

<details>
<summary><b>日本語</b></summary>

huijui forge は Android の Root ツールとモジュール環境に取り組む小さな
オープンソースチームです。5 つのプロジェクトを維持しています：
HuiJuiSU（Root マネージャー）、Snow-love-Module（隠蔽モジュール）、
Huijui_Module_Repo（モジュール索引）、HuiJui-Toolbox（スクリプト集）、
そしてドキュメントサイトです。

</details>

<details>
<summary><b>한국어</b></summary>

huijui forge 는 Android 루트 도구와 모듈 생태계에 집중하는 작은 오픈소스
팀입니다. 다섯 개의 프로젝트를 운영합니다: HuiJuiSU(루트 관리자),
Snow-love-Module(숨김 모듈), Huijui_Module_Repo(모듈 색인),
HuiJui-Toolbox(스크립트 모음), 그리고 문서 사이트입니다.

</details>

<details>
<summary><b>Русский</b></summary>

huijui forge — небольшая open-source команда, занимающаяся инструментами
root-доступа и модулями для Android. Мы поддерживаем пять проектов:
root-менеджер HuiJuiSU, модуль скрытия Snow-love-Module, индекс модулей
Huijui_Module_Repo, набор скриптов HuiJui-Toolbox и сайт документации.

</details>

---

## 参与

- 提交 Issue：对应仓库的 Issues
- 讨论：Telegram 群 [@Huijui123](https://t.me/Huijui123)
- 更新通知：Telegram 频道 [@HuijuiSU](https://t.me/HuijuiSU)
- QQ 群：763278354
- 贡献前请读 [CONTRIBUTING.md](CONTRIBUTING.md) 与 [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md)

---

## 许可

各仓库以 **GPL-3.0** 为主，详见对应仓库的 `LICENSE`。

<sub>huijui forge 与 KernelSU 官方无隶属关系；HuiJuiSU 为独立的下游分支。</sub>
