# 论文模板 (LaTeX / Typst)

在南京大学，无论是本科毕业设计（论文），还是硕士、博士学位论文，学校都有着极其严密且复杂的格式规范要求（如页边距、字体大小、参考文献格式等）。如果完全使用 Word 手动调整，常常会因为排版错乱而浪费大量时间。

为了让同学们能够专注于学术内容本身，南大开源社区维护了超高质量的 LaTeX 和 Typst 学位论文模板。

---

## 🖋️ 1. LaTeX 论文模板：NJUThesis (推荐)

**NJUThesis** 是南京大学最知名的开源项目之一，也是目前最推荐使用的学位论文排版模板。

*   **官方仓库**：[nju-lug/NJUThesis](https://github.com/nju-lug/NJUThesis)
*   **维护组织**：南京大学 Linux 用户协会 (NJU-LUG)
*   **支持范围**：完全支持南京大学**学士、硕士、博士**学位论文格式规范。
*   **项目状态**：**已正式收录于 CTAN（TeX 综合档案网）**。如果你的电脑安装了完整的 TeX Live（2021 或更新版本），你可以直接在命令行更新安装，无需单独下载源码包。

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

**Typst** 是近年来风靡全球的下一代排版标记语言。它具有**渲染速度极快（毫秒级）、语法简洁（类似 Markdown）、报错信息极度友好**的特点，被普遍认为是 LaTeX 的强力替代者。

*   **官方仓库**：[nju-lug/modern-nju-thesis](https://github.com/nju-lug/modern-nju-thesis)
*   **维护组织**：南京大学 Linux 用户协会 (NJU-LUG)
*   **推荐理由**：如果你厌烦了 LaTeX 漫长的编译等待和晦涩的排版宏包报错，且学校或导师允许提交 PDF 格式论文，强烈推荐使用该 Typst 模板。

---

## 📄 3. 官方 Word 模板

如果你的导师强烈要求提交 `.docx` 格式文档，或者你对代码类工具感到排斥，你可以直接通过学校官方渠道下载规范：
*   **获取入口**：登录“南京大学教务处官网”，在“实践教学 -> 毕业设计”栏目中下载最新的《南京大学本科生毕业论文（设计）撰写模版与规范》。

---

## 📚 4. LaTeX 与 Typst 入门自学指南

*   **《一份不太简短的 LaTeX2e 介绍》** (lshort-zh)：公认最经典的 LaTeX 中文入门指南，网上可免费下载 PDF，半天即可上手。
*   **Overleaf 中文文档**：Overleaf 提供了非常优质的排版教程，适合随查随用。
*   **Typst 官方文档** (`https://typst.app/docs`)：Typst 官方教程非常现代化，支持在线直接编辑预览。
