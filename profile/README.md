<div align="center">

<img src="https://raw.githubusercontent.com/HuijuiSU-NEXT/.github/main/profile/avatar.png" width="120" alt="HuiJuiSU" />

# huijui forge

**huijui forge** · 作品与模块生态

旗下产品：**HuiJuiSU** —— 基于 KernelSU 的 Android Root 管理器

[![Website](https://img.shields.io/badge/官网-huijuisu--next.github.io-3ee6c4?style=flat-square)](https://huijuisu-next.github.io/)
[![Release](https://img.shields.io/github/v/release/HuijuiSU-NEXT/HuijuiSU?style=flat-square&label=release)](https://github.com/HuijuiSU-NEXT/HuijuiSU/releases/latest)
[![License](https://img.shields.io/github/license/HuijuiSU-NEXT/HuijuiSU?style=flat-square)](https://github.com/HuijuiSU-NEXT/HuijuiSU/blob/main/LICENSE)
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
| [**HuijuiSU**](https://github.com/HuijuiSU-NEXT/HuijuiSU) | 管理器与内核（主仓库） | 活跃 |
| [**Snow-love-Module**](https://github.com/HuijuiSU-NEXT/Snow-love-Module) | 一键隐藏模块源码（恋雪） | 维护 |
| [**Huijui_Module_Repo**](https://github.com/HuijuiSU-NEXT/Huijui_Module_Repo) | 模块仓库索引与更新源 | 维护 |
| [**HuiJui-Toolbox**](https://github.com/HuijuiSU-NEXT/HuiJui-Toolbox) | 常用 Root 操作脚本集合 | 维护 |
| [**huijuisu-next.github.io**](https://github.com/HuijuiSU-NEXT/huijuisu-next.github.io) | 官网（GitHub Pages） | 活跃 |

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

完整步骤见 [安装文档](https://huijuisu-next.github.io/install.html)。

---

## 兼容性

| KMI | Android | 方式 |
|---|---|---|
| `android12-5.10` ~ `android17-6.18` | 12 ~ 17 | GKI · LKM |
| 4.x / 非 GKI 魔改内核 | 8 ~ 13 | 内核补丁 |

---

## 参与

- 提交 Issue：[HuijuiSU/issues](https://github.com/HuijuiSU-NEXT/HuijuiSU/issues)
- 讨论：Telegram 群 [@Huijui123](https://t.me/Huijui123)
- 更新通知：Telegram 频道 [@HuijuiSU](https://t.me/HuijuiSU)
- QQ 群：763278354

---

## 许可

各仓库以 **GPL-3.0** 为主，详见对应仓库的 `LICENSE`。

<sub>HuiJuiSU 与 KernelSU 官方无隶属关系；本项目为独立的下游分支。</sub>
