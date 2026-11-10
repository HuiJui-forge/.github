<div align="center">

<img src="https://raw.githubusercontent.com/HuiJui-forge/.github/main/profile/avatar.png" width="120" alt="HuiJuiSU" />

# huijui forge

**huijui forge** · 作品与模块生态

旗下产品：**HuiJuiSU** —— 基于 KernelSU 的 Android Root 管理器

[![Website](https://img.shields.io/badge/官网-huijuisu--next.github.io-3ee6c4?style=flat-square)](https://huijui-forge.github.io/)
[![Release](https://img.shields.io/github/v/release/HuiJui-forge/HuijuiSU?style=flat-square&label=release)](https://github.com/HuiJui-forge/HuijuiSU/releases/latest)
[![License](https://img.shields.io/github/license/HuiJui-forge/HuijuiSU?style=flat-square)](https://github.com/HuiJui-forge/HuijuiSU/blob/main/LICENSE)
[![Telegram](https://img.shields.io/badge/Telegram-群组-26A5E4?style=flat-square&logo=telegram)](https://t.me/Huijui123)

</div>

---

## 我们在做什么

HuiJuiSU 是 **KernelSU 的下游分支**。保留上游的管理器与内核能力，额外把隐藏模块、检测对抗、热刷入与一批实用工具收进管理器。

| 方向 | 说明 |
|---|---|
| **内置隐藏** | 隐藏所需组件随 APK 分发，首次启动自动部署，不需要用户自己找包、导配置 |
| **真·热刷入** | 接入 Hybrid Mount runtime，纯 VFS 计划的模块装完即挂载 |
| **开机秒激活** | 内置 `huijui_core`，重启后隐藏配置自动生效 |
| **稳定优先** | root 调用多路径回退 + 超时，避免界面卡死；核心模块防误删 |

---

## 项目

| 仓库 | 说明 | 状态 |
|---|---|---|
| [**HuijuiSU**](https://github.com/HuiJui-forge/HuijuiSU) | 管理器与内核（主仓库） | 活跃 |
| [**Snow-love-Module**](https://github.com/HuiJui-forge/Snow-love-Module) | 一键隐藏模块源码（恋雪） | 维护 |
| [**Huijui_Module_Repo**](https://github.com/HuiJui-forge/Huijui_Module_Repo) | 模块仓库索引与更新源 | 维护 |
| [**HuiJui-Toolbox**](https://github.com/HuiJui-forge/HuiJui-Toolbox) | 常用 Root 操作脚本集合 | 维护 |
| [**huijui-forge.github.io**](https://github.com/HuiJui-forge/huijui-forge.github.io) | 官网（GitHub Pages） | 活跃 |

---

## 快速开始

```bash
# 1. 确认内核 KMI
uname -r

# 2. 加载对应 kernelsu.ko（以 android16-6.12 / arm64 为例）
adb push aarch64-android16-6.12_kernelsu.ko /data/local/tmp/
adb shell su -c "ksud insmod /data/local/tmp/aarch64-android16-6.12_kernelsu.ko"

# 3. 安装管理器
adb install HuiJuiSU_NEXT_Ultra_arm64-v8a-release.apk
```

装好后打开 App → 工具箱 → 一键隐藏。

完整步骤见 [安装文档](https://huijui-forge.github.io/install.html)。

---

## 兼容性

| KMI | Android | 方式 |
|---|---|---|
| `android12-5.10` ~ `android17-6.18` | 12 ~ 17 | GKI · LKM |
| 4.x / 非 GKI 魔改内核 | 8 ~ 13 | 内核补丁 |

---

## 技术栈

| 层 | 使用 |
|---|---|
| 管理器 | Kotlin + Jetpack Compose，AGP / Gradle |
| 内核 | C，KernelSU 分支，LKM 与内核补丁双路线 |
| 用户态 | Rust / C（ksud、ksuinit） |
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


---

## Languages · 语言

<details>
<summary><b>简体中文</b></summary>

huijui forge 是一个小型开源团队，专注 Android Root 工具与模块生态。
我们的旗舰产品是 **HuiJuiSU** —— 基于 KernelSU 的 Root 管理器，
内置一键隐藏、真热刷入与开机自动激活。

</details>

<details>
<summary><b>繁體中文</b></summary>

huijui forge 是一個小型開源團隊，專注 Android Root 工具與模組生態。
我們的旗艦產品是 **HuiJuiSU** —— 基於 KernelSU 的 Root 管理器，
內建一鍵隱藏、真熱刷入與開機自動啟用。

</details>

<details>
<summary><b>English</b></summary>

huijui forge is a small open-source team focused on Android root tooling
and module tooling. Our flagship product is **HuiJuiSU**, a KernelSU-based
root manager with built-in hiding, true hot-flash mounting and automatic
activation on boot.

</details>

<details>
<summary><b>日本語</b></summary>

huijui forge は Android の Root ツールとモジュール環境に取り組む
小さなオープンソースチームです。主力製品は **HuiJuiSU** —
KernelSU ベースの Root マネージャーで、ワンクリック隠蔽・
ホットフラッシュ・起動時の自動有効化を備えています。

</details>

<details>
<summary><b>한국어</b></summary>

huijui forge 는 Android 루트 도구와 모듈 생태계에 집중하는
작은 오픈소스 팀입니다. 대표 제품은 **HuiJuiSU** — KernelSU 기반
루트 관리자로, 원클릭 숨김·핫 플래시·부팅 시 자동 활성화를 제공합니다.

</details>

<details>
<summary><b>Русский</b></summary>

huijui forge — небольшая open-source команда, занимающаяся инструментами
root-доступа и модулями для Android. Наш основной продукт — **HuiJuiSU**,
root-менеджер на базе KernelSU со встроенным скрытием, горячей установкой
модулей и автоматической активацией при загрузке.

</details>

---

## 参与

- 提交 Issue：[HuijuiSU/issues](https://github.com/HuiJui-forge/HuijuiSU/issues)
- 讨论：Telegram 群 [@Huijui123](https://t.me/Huijui123)
- 更新通知：Telegram 频道 [@HuijuiSU](https://t.me/HuijuiSU)
- QQ 群：763278354

---

## 许可

各仓库以 **GPL-3.0** 为主，详见对应仓库的 `LICENSE`。

<sub>HuiJuiSU 与 KernelSU 官方无隶属关系；本项目为独立的下游分支。</sub>
