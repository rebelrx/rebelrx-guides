<!--
Source: privacy/my-setup.md
Last translated: 2026-04
-->

# 🧪 RebelRx 隐私配置方案

这是我自己在真实环境中使用的隐私优先技术栈，专为**控制力、性能和可用性**而设计。

我每天都在使用这套系统，并会随着更优服务的出现持续更新这些内容。

---

## 🧭 理念

该配置围绕以下原则构建：

* **所有权** → 你的数据始终由你掌控
* **实用性** → 工具必须在日常中真正可用
* **可扩展性** → 能随需求增长
* **安全性** → 避免不必要的暴露

> 💡 这不是“极致隐私”的配置，而是一个**平衡且可用的系统**。

---

## 🖥️ 硬件概览

我的系统由**自托管基础设施、专用设备和个人设备**组成，每个设备承担特定角色。

---

## 🧱 核心基础设施

### Minisforum MS-A2（主服务器）

* **操作系统：** Devuan（裸机运行）
* **角色：** 核心 Docker 主机

> 💡 这是整个系统的核心骨干

👉 查看 Minisforum 工作站迷你主机系列：<https://www.minisforum.com/collections/station-mini-series>

---

### QNAP TS-h1277AXU-RP（NAS）

* **角色：** 大容量存储 + 备份
* 存储内容：

  * 媒体库
  * Nextcloud 数据
  * 备份
  * 归档（ROM、文档等）

> 💡 将计算（服务器）与存储（NAS）分离可以提升灵活性和系统韧性

👉 查看 QNAP NAS 产品：<https://www.qnap.com/en-us/product>

---

## 💻 个人设备

### 自定义 Ryzen 9 台式机（Windows 11）

* **角色：** 游戏 + 仅限 Windows 的应用
* 用途：

  * 高性能任务
  * 兼容非 Linux 软件

👉 查看 Micro Center 门店：<https://www.microcenter.com/>

---

### Framework 台式机（Artix Linux）

* **角色：** 次级工作站
* 用途：

  * 日常生产力
  * Linux 优先工作流

👉 查看 Framework 台式机：<https://frame.work/marketplace/desktops>

---

### Framework 13 笔记本（Artix Linux）

* **角色：** 出行 + 开发设备
* 用途：

  * 远程访问（通过 Tailscale）
  * 管理家庭基础设施
  * 轻量生产力

👉 查看 Framework 笔记本：<https://frame.work/marketplace/laptops>

---

## 🎮 游戏与模拟

### Raspberry Pi 5（8GB）

* **操作系统：** Batocera
* **附加：** MiSTer FPGA
* **角色：** 复古游戏 / 模拟

👉 查看 Vilros 的 Raspberry Pi 产品：<https://vilros.com/>

---

## 🏠 专用设备

### Beelink Mini S13

* **角色：** 智能家居自动化
* **操作系统：** Home Assistant OS

👉 查看 Beelink 迷你主机：<https://www.bee-link.com/collections/product>

---

### Umbrel Home

* **角色：** 比特币节点
* 运行：

  * 完整 BTC 节点
  * Lightning 网络

👉 查看 Umbrel 设备：<https://umbrel.com/>

---

### Intel NUC 13

* **角色：** 音频服务器
* **操作系统：** Roon ROCK

👉 查看 B&H 的 NUC 产品：<https://www.bhphotovideo.com/>

---

## 🧠 设计理念

每个设备都有**明确的单一职责**：

* 服务器 → 计算（Docker 工作负载）
* NAS → 存储
* 客户端 → 交互（桌面/笔记本）
* 专用设备 → 专项任务

> 💡 这种分离使系统：
>
> * 更易维护
> * 更具韧性
> * 更易扩展

---

## ✅ 为什么这个配置适合我

* 避免单点故障
* 职责清晰分离
* 每台设备性能最优
* 可以灵活升级各个组件

---

## 🚀 关于硬件的最终思考

但你并不需要这么多硬件才能开始。

这套系统是逐步演进而来的——
从小开始，随着需求增长再扩展。

---

## 🧱 核心架构

* **基于 Docker 的部署**
* **NAS 支持的存储**
* **反向代理（Nginx Proxy Manager）**
* **通过 Tailscale 实现私有访问（无端口转发）**

---

## ☁️ 数据与生产力

### Nextcloud AIO

* 文件
* 日历（CalDAV）
* 联系人（CardDAV）
* NAS 支持的存储

### 云存储（托管）

* pCloud.com

---

## 📧 邮箱

* Proton Mail

---

## 📸 照片

### Immich

* 替代 Google Photos
* 快速、现代化界面
* 完全自托管

---

## 📝 办公

### ONLYOFFICE

* 替代 Microsoft Office 365
* 完整办公套件（文档、表格、演示、PDF、表单）
* 免费且开源

---

## 📄 PDF 与文档

* Sumatra PDF（轻量阅读器）
* BentoPDF（PDF 工具）
* Paperless-ngx（文档归档）

---

## 📝 笔记与知识管理

### Joplin

* 基于 Markdown
* 跨平台
* 通过 Nextcloud 同步

### Paperless-ngx

* 文档管理系统
* OCR + 标签
* 替代纸质文件

---

## 🔐 安全与身份

### 密码管理器

* Proton Pass（托管方案）

### 双重认证（2FA）

* 所有服务均启用
* 支持 Passkeys 时优先使用

---

## 🌍 网络与隐私层

### DNS 屏蔽

* AdGuard Home
* 全网络广告与追踪拦截

### VPN

* Mullvad（隐私优先 VPN）

### 私有访问

* Tailscale
* 安全远程访问服务
* 无开放端口

---

## 🌐 浏览器

* Brave

  * 内置广告/追踪拦截
  * 几乎无需扩展

---

## 🎥 媒体与娱乐

### Jellyfin

* 自托管流媒体
* 替代 Netflix / HBO 等服务

### Arr 套件

* Sonarr
* Radarr
* Prowlarr
* 自动化媒体管理

---

## 📚 书籍与音频

### Calibre-Web / Kavita

* 电子书库

### Audiobookshelf

* 有声书 + 播客
* 完全自托管

---

## 💰 财务

### Actual Budget

* 自托管预算工具
* 替代 Mint / YNAB

---

## 🧰 开发与基础设施

### Git

* Forgejo（自托管 Git 服务）

### 编辑器

* VSCodium（无遥测 VS Code）

---

## 🌐 网络工具

* LibreSpeed
* Speedtest-tracker

自托管网络测速，无跟踪。

---

## 🔁 替代关系

| 大型科技服务           | 替代方案                           |
| ---------------- | ------------------------------ |
| Google Drive     | Nextcloud                      |
| Google Photos    | Immich                         |
| Google 日历        | Nextcloud                      |
| Google 联系人       | Nextcloud                      |
| Gmail            | Proton Mail / Tuta             |
| Chrome 密码管理      | Vaultwarden / Proton Pass      |
| Chrome           | Brave                          |
| Google Docs（部分）  | Nextcloud + Joplin             |
| Netflix / HBO    | Jellyfin + Arr 套件              |
| Kindle / Audible | Calibre-Web / Audiobookshelf   |
| Adobe Acrobat    | Sumatra PDF / BentoPDF         |
| Mint / YNAB      | Actual Budget                  |
| GitHub           | Forgejo                        |
| ISP DNS          | AdGuard Home / Pi-hole         |
| Speedtest.net    | LibreSpeed / Speedtest-tracker |

---

## 🧠 设计原则

### 1. 尽可能本地优先

数据存储在：

* 你的服务器
* 你的 NAS

---

### 2. 在有价值时才自托管

并非所有内容都需要自托管。

平衡策略：

* 自托管 → 核心数据（文件、照片、密码）
* 托管 → 便利性（如邮箱）

---

### 3. 默认安全

* 无开放端口
* 仅通过 Tailscale 访问
* 使用反向代理进行内部路由

---

### 4. 保持可维护性

* 基于 Docker 的服务
* 清晰的目录结构
* 配置版本控制（Forgejo）

---

## ⚖️ 为什么这个配置有效

* 对数据拥有高度控制
* 持续成本低
* 架构可扩展
* 安全的远程访问
* 跨设备可用

---

## 🚀 关于基础设施的最终思考

这不是唯一的方案，也绝非完美！

但它是一个**经过实战验证的真实配置**，在以下方面取得平衡：

* 隐私
* 可用性
* 可靠性

> 🧠 目标不是完美，而是在**无摩擦的前提下实现控制力**。
