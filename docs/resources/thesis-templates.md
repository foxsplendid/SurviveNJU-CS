# 论文模板 (LaTeX / Typst)

在南京大学，无论是本科毕业设计（论文），还是硕士、博士学位论文，学校都有较严格的格式规范要求（如页边距、字体大小、参考文献格式等）。如果完全使用 Word 手动调整，容易因为排版错乱而浪费时间。

为了让同学们能够专注于学术内容本身，南大开源社区维护了一些常用的 LaTeX 和 Typst 学位论文模板。

---

## 🖋️ 1. LaTeX 论文模板：NJUThesis

**NJUThesis** 是南京大学学生和校友社区中较常用的学位论文排版模板之一。

*   **项目仓库**：[nju-lug/NJUThesis](https://github.com/nju-lug/NJUThesis)
*   **维护组织**：南京大学 Linux 用户协会 (NJU-LUG)
*   **支持范围**：目标是支持南京大学**学士、硕士、博士**学位论文格式规范；提交前仍应按学校/院系最新模板和导师要求核对。
*   **安装方式**：请以仓库 README 的最新说明为准；如果项目当前支持 TeX Live/CTAN 安装，可直接通过 TeX Live 工具链安装或升级。

### ⚙️ 快捷使用命令 (TeX Live / MacTeX)
在终端或 PowerShell 中直接执行以下命令安装或升级：
```bash
tlmgr install njuthesis
```

### 📝 极简使用示例
创建一个主 `.tex` 文件，使用 `njuthesis` 文档类：
```latex
\documentclass[type=bachelor]{njuthesis} % type 可选 bachelor, master, doctor

\title{南京大学学位论文 LaTeX 模板使用研究}
\author{张三}
\supervisor{李四~教授}
\department{计算机科学与技术系}
\major{计算机科学与技术}
\date{2026年6月}

\begin{document}

\maketitle
\makeabstract

\chapter{引言}
这是你的第一章正文内容。你可以非常方便地进行数学公式排版：
\begin{equation}
    E = mc^2
\end{equation}

\chapter{系统设计}
这是第二章。

\end{document}
```

---

## ⚡ 2. Typst 论文模板：modern-nju-thesis (现代化选择)

**Typst** 是近年来受到较多关注的新一代排版标记语言。它语法相对简洁、预览速度较快，对不熟悉 LaTeX 宏包生态的同学更容易上手。

*   **项目仓库**：[nju-lug/modern-nju-thesis](https://github.com/nju-lug/modern-nju-thesis)
*   **维护组织**：南京大学 Linux 用户协会 (NJU-LUG)
*   **适用场景**：如果学校、院系和导师允许使用 Typst 生成的 PDF，并且你希望降低排版工具学习成本，可以评估该模板是否适合你的论文。

---

## 📄 3. 官方 Word 模板

如果你的导师强烈要求提交 `.docx` 格式文档，或者你对代码类工具感到排斥，你可以直接通过学校官方渠道下载规范：
*   **获取入口**：登录“南京大学教务处官网”，在“实践教学 -> 毕业设计”栏目中下载最新的《南京大学本科生毕业论文（设计）撰写模版与规范》。

---

## 📚 4. LaTeX 与 Typst 入门自学指南

*   **《一份不太简短的 LaTeX2e 介绍》** (lshort-zh)：常见的 LaTeX 中文入门资料，适合系统了解基础语法和排版概念。
*   **Overleaf 中文文档**：Overleaf 提供了非常优质的排版教程，适合随查随用。
*   **Typst 官方文档** (`https://typst.app/docs`)：Typst 官方教程非常现代化，支持在线直接编辑预览。
