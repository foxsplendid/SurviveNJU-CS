# 实用工具集

「工欲善其事，必先利其器。」在泛CS专业的学习与科研中，合理利用高效的工具能够帮助你省去大量繁琐的机械劳动，把精力集中在核心逻辑上。

本篇指南为你整理了在南大学习生活最常用的软件工具链、开发环境配置及南大专属实用程序。

---

## 🏛️ 1. 南大专属实用工具

作为南大在校生，以下几款由本校同学开发、公开维护或常被同学使用的工具，能减少一些重复操作：

### 📅 课表一键导入日历：nju-schedule-ics & NJU-Calendar-Importer-Flutter
*   **用途**：将教服平台课表导出或转换后导入系统日历，提醒你上课时间与地点。
*   **使用工具**：
    *   👉 **[nju-schedule-ics](https://github.com/SuperKenVery/nju-schedule-ics)**：基于命令行/在线转换，生成标准的 `.ics` 文件，适用于导入 iPhone、安卓或 Outlook 日历。
    *   👉 **[NJU-Calendar-Importer-Flutter](https://github.com/121mc/NJU_Calendar_Importer_Flutter)**：采用 Flutter 编写的跨平台课表导入客户端，可将南大课表解析导入日历。
*   **效果**：可设置上课前日历提醒，部分工具支持显示上课教室和授课教师，减少手动录入。

### 📥 教学立方批量课件下载：PedagogySquare_Downloader
*   **用途**：辅助整理自己已选课程、且教学平台允许访问的资料。
*   **使用边界**：仅应下载你本人有权限访问的课程资料，不得绕过访问控制，不得将教师课件、作业要求、试卷或其他受限资料二次公开传播。
*   **使用方式**：前往 [EricZhu-42/PedagogySquare_Downloader](https://github.com/EricZhu-42/PedagogySquare_Downloader) 查看仓库说明和发布包，按项目文档操作。

### 🔒 南大 VPN 远程接入 (Ivanti / Pulse Secure)
*   **用途**：在校外访问部分校内系统或图书馆订阅数据库时，通常需要连接南大官方 VPN。
*   **配置入口**：访问“南大信息化建设管理服务中心”，在服务指南中搜索“VPN”，根据操作系统下载对应的 Pulse Secure 客户端，并使用校内统一身份认证账号登录。

---

## 💻 2. 个人高效学习工具链

| 工具名称 | 分类 | 主要用途与特色 | 官方链接/获取方式 |
| :--- | :--- | :--- | :--- |
| **Obsidian** | 笔记管理 | 纯文本、本地优先的 Markdown 知识库软件。支持双向链接，适合整理复杂的专业课脑图与知识网络。 | [Obsidian 官网](https://obsidian.md) |
| **Zotero** | 文献检索 | 开源免费的论文管理利器。大二、大三做科研或写毕业设计时，可一键抓取网页端 PDF 和论文元数据。 | [Zotero 官网](https://www.zotero.org) |
| **Anki** | 记忆卡片 | 采用间隔重复（Spaced Repetition）算法。适合期末前高强度记忆公共课概念、Linux 常用命令行及数学公式。 | [Anki 官网](https://apps.ankiweb.net) |
| **Overleaf** | LaTeX 写作 | 在线的 LaTeX 编辑和协作平台，适合与同学合作撰写报告或论文；机构权限情况请以学校当前通知为准。 | [Overleaf 官网](https://www.overleaf.com) |

---

## 🛠️ 3. 开发环境与终端效率配置

### 1. Linux 环境搭建
南大泛CS方向的多门实验课（尤其是系统类课程）通常要求 Linux 或类 Unix 开发环境；具体系统版本和依赖请以课程实验指导为准。常见搭建方案如下：
*   **方案一：WSL2 (Windows Subsystem for Linux)**（最推荐 Windows 用户）：
    *   在 Windows 11 中安装 Ubuntu 子系统。它与 Windows 文件系统互通，方便用 VS Code 编辑和调试代码。
    *   **安装命令**：在 PowerShell 中执行 `wsl --install`。
*   **方案二：双系统 (Dual Boot)**：
    *   如果电脑配置允许，可以直接在电脑上安装 Windows + Ubuntu 双系统，获得最纯粹的 Linux 硬件算力支持。

### 2. VS Code 推荐插件
作为泛CS学生的通用编辑器，VS Code 搭配以下插件能让你事半功倍：
*   **C/C++** (Microsoft)：提供语法高亮、IntelliSense 代码自动补全。
*   **GitLens**：可视化 Git 历史，清晰查看每一行代码是谁在什么时间提交的，团队协作大作业必备。
*   **Remote - WSL**：如果你使用 WSL2，该插件可以让你直接在 Windows 的 VS Code 窗口中编辑、调试 WSL2 内的代码，体验极佳。
*   **Markdown All in One**：完美支持 Markdown 预览与快捷键，编写实验报告（Report）的利器。
