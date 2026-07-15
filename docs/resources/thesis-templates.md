# 论文模板 (LaTeX / Typst)

本科毕业论文和研究生学位论文分别受学校、院系、培养层次和当届通知约束。封面、声明、摘要、参考文献、签字和归档格式应逐项核对适用于本人的正式要求。

社区维护的 LaTeX 和 Typst 模板可以辅助排版，但不构成学校审核或格式合规证明。

---

## 🖋️ 1. LaTeX 论文模板：NJUThesis

**NJUThesis** 是面向南京大学学位论文排版的社区模板。

*   **项目仓库**：[nju-lug/NJUThesis](https://github.com/nju-lug/NJUThesis)
*   **维护组织**：南京大学 Linux 用户协会 (NJU-LUG)
*   **支持范围**：目标是支持南京大学**学士、硕士、博士**学位论文格式规范；提交前仍应按学校/院系最新模板和导师要求核对。
*   **安装方式**：请以仓库 README 的最新说明为准；如果项目当前支持 TeX Live/CTAN 安装，可直接通过 TeX Live 工具链安装或升级。

### ⚙️ 快速开始 (TeX Live / MacTeX)
安装方式和最低 TeX Live 版本可能随项目更新。先阅读仓库当前 README 和发布包中的用户手册；如果当前版本支持通过 CTAN 安装，可使用：
```bash
tlmgr install njuthesis
```

### 📝 当前项目的基本结构
NJUThesis 当前 README 使用 `\documentclass{njuthesis}` 和 `\njusetup{}`。下面只展示主文件结构，不替代发布包中的 `njuthesis-sample.tex`：
```latex
\documentclass{njuthesis}
\njusetup{
  % Copy metadata fields from njuthesis-sample.tex.
}

\begin{document}
\maketitle
\tableofcontents
\mainmatter
\chapter{Introduction}
Thesis content.
\printbibliography
\end{document}
```

学位类型、院系、作者、导师和中英文摘要等字段应直接从所用版本的示例文件复制，再按用户手册填写；不要沿用网上旧示例中的类选项或命令。

---

## ⚡ 2. Typst 论文模板：modern-nju-thesis

**Typst** 是另一种排版系统。其语法、工具链和模板成熟度与 LaTeX 不同，是否适用取决于当届格式要求、导师意见和归档流程。

*   **项目仓库**：[nju-lug/modern-nju-thesis](https://github.com/nju-lug/modern-nju-thesis)
*   **维护组织**：南京大学 Linux 用户协会 (NJU-LUG)
*   **适用场景**：该项目 README 明确说明它不是学校官方模板。如果学校、院系和导师允许使用 Typst 生成的 PDF，并且你希望降低排版工具学习成本，可以评估该模板是否适合你的论文。

---

## 📄 3. 2026 届本科官方规范与 Word 模板

本科毕业论文应先查看教务处发布的 [《关于做好 2026 届本科毕业论文（设计）工作的通知》](https://jw.nju.edu.cn/3f/59/c26263a802649/page.htm) 及其附件。该官方页面集中提供当届工作手册、论文撰写与存档要求、Word 参考模板，以及生成式人工智能使用指引、使用情况说明材料等文件。

!!! important "模板不等于合规确认"
    官方通知说明学校 Word 模板供参考，具体要求以院系规定为准。NJUThesis 与 modern-nju-thesis 均为社区维护项目，不代表学校或院系已经审核其当前输出；提交前应逐项对照 2026 届通知、所在院系要求和导师意见，尤其核对封面、声明、摘要、参考文献、签名及存档格式。

---

## 📚 4. LaTeX 与 Typst 入门自学指南

*   **[《一份不太简短的 LaTeX2e 介绍》](https://github.com/CTeX-org/lshort-zh-cn)** (lshort-zh-cn)：常见的 LaTeX 中文入门资料，适合系统了解基础语法和排版概念。
*   **[Overleaf 文档](https://www.overleaf.com/learn)**：在线 LaTeX 编辑器的使用文档；向云端上传论文前应确认研究数据、未公开成果和个人信息是否适合由第三方平台处理。
*   **[Typst 官方文档](https://typst.app/docs)**：Typst 语法和工具链文档。
