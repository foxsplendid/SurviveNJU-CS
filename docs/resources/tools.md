# 实用工具集

「工欲善其事，必先利其器。」在泛CS专业的学习与科研中，合理利用高效的工具能够帮助你省去大量繁琐的机械劳动，把精力集中在核心逻辑上。

本篇指南为你整理了在南大学习生活最常用的软件工具链、开发环境配置及南大专属实用程序。

---

## 🏛️ 1. 南大专属实用工具

作为南大在校生，以下几款由本校同学开发或官方提供的工具能大幅提升你的日常效率：

### 📅 课表一键导入日历：nju-schedule-ics
*   **用途**：将教服平台杂乱的课表，一键导出为标准的 `.ics` 文件，直接导入 iPhone、安卓或 Outlook 日历。
*   **使用方式**：访问 [SuperKenVery/nju-schedule-ics](https://github.com/SuperKenVery/nju-schedule-ics) 克隆代码，或使用基于网页的在线转换工具。
*   **效果**：实现上课前 15 分钟日历弹窗自动提醒，支持显示上课教室和授课教师。

### 📥 教学立方批量课件下载：PedagogySquare_Downloader
*   **用途**：期末复习时，一页一页下载教学立方上的 PPT 课件极其繁琐。该工具支持一键批量抓取下载。
*   **使用方式**：前往 [EricZhu-42/PedagogySquare_Downloader](https://github.com/EricZhu-42/PedagogySquare_Downloader) 释放页面下载运行包，输入教学立方账号即可批量导出。

### 🔒 南大 VPN 远程接入 (Ivanti / Pulse Secure)
*   **用途**：在寒暑假离校、或在宿舍区连接非校园网时，必须连接南大官方 VPN 才能访问教服平台、教学立方或通过图书馆免费使用 IEEE Xplore 等数据库。
*   **配置入口**：访问“南大信息化建设管理服务中心”，在服务指南中搜索“VPN”，根据操作系统下载对应的 Pulse Secure 客户端，并使用校内统一身份认证账号登录。

---

## 💻 2. 个人高效学习工具链

| 工具名称 | 分类 | 主要用途与特色 | 官方链接/获取方式 |
| :--- | :--- | :--- | :--- |
| **Obsidian** | 笔记管理 | 纯文本、本地优先的 Markdown 知识库软件。支持双向链接，适合整理复杂的专业课脑图与知识网络。 | [Obsidian 官网](https://obsidian.md) |
| **Zotero** | 文献检索 | 开源免费的论文管理利器。大二、大三做科研或写毕业设计时，可一键抓取网页端 PDF 和论文元数据。 | [Zotero 官网](https://www.zotero.org) |
| **Anki** | 记忆卡片 | 采用间隔重复（Spaced Repetition）算法。适合期末前高强度记忆公共课概念、Linux 常用命令行及数学公式。 | [Anki 官网](https://apps.ankiweb.net) |
| **Overleaf** | LaTeX 写作 | 在线的 LaTeX 编辑和协作平台。南大提供部分收费账户权限，适合与同学合作撰写报告或论文。 | [Overleaf 官网](https://www.overleaf.com) |

---

## 🛠️ 3. 开发环境与终端效率配置

### 1. Linux 环境搭建
南大计算机系和软件学院的必修实验课（尤其是 ICS PA 和 操作系统 OSLab）**必须在 Linux 环境下完成**。我们强烈推荐以下搭建方案：
*   **方案一：WSL2 (Windows Subsystem for Linux)**（最推荐 Windows 用户）：
    *   在 Windows 11 中一键安装 Ubuntu 子系统。它拥有极接近原生的运行效率，且可以直接与 Windows 的文件系统无缝互通，方便用 VS Code 直接编辑代码。
    *   **安装命令**：在 PowerShell 中执行 `wsl --install`。
*   **方案二：双系统 (Dual Boot)**：
    *   如果电脑配置允许，可以直接在电脑上安装 Windows + Ubuntu 双系统，获得最纯粹的 Linux 硬件算力支持。

### 2. VS Code 推荐插件
作为泛CS学生的通用编辑器，VS Code 搭配以下插件能让你事半功倍：
*   **C/C++** (Microsoft)：提供语法高亮、IntelliSense 代码自动补全。
*   **GitLens**：可视化 Git 历史，清晰查看每一行代码是谁在什么时间提交的，团队协作大作业必备。
*   **Remote - WSL**：如果你使用 WSL2，该插件可以让你直接在 Windows 的 VS Code 窗口中编辑、调试 WSL2 内的代码，体验极佳。
*   **Markdown All in One**：完美支持 Markdown 预览与快捷键，编写实验报告（Report）的利器。
