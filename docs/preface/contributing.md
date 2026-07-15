# 贡献指南

SurviveNJU-CS 是一个社区共同维护的活文档。贡献可以是事实纠错、来源补充、链接维护，也可以是明确标注适用条件的个人经验；贡献者不需要公开真实身份、成绩或其他个人材料。

这份指南告诉你如何参与进来。

---

## 贡献方式总览

!!! tip "两种真实可用的入口"
    能直接修改文档时提交 Pull Request；暂时不会使用 Git 时提交最小化 GitHub Issue。项目当前没有公开的邮件或私信投稿渠道，不要把敏感材料粘贴到公开 Issue。

| 贡献方式 | 适合场景 | 难度 |
|---|---|---|
| **提交 Pull Request** | 修改/新增页面内容 | ⭐⭐（需要 Git 基础） |
| **提交 Issue** | 报告错误、提建议、请求新内容 | ⭐（零门槛） |

---

## PR 完整流程

### 第一步：Fork 仓库

前往 [SurviveNJU-CS 主仓库](https://github.com/foxsplendid/SurviveNJU-CS)，点击右上角 **Fork** 按钮，将仓库 Fork 到你自己的 GitHub 账号下。

### 第二步：Clone 到本地

```bash
# 将 YOUR_USERNAME 替换为你的 GitHub 用户名
git clone https://github.com/YOUR_USERNAME/SurviveNJU-CS.git
cd SurviveNJU-CS
```

### 第三步：新建分支

养成好习惯——永远不要在 `main` 分支上直接修改：

```bash
# 分支名用短横线分隔，简洁描述你在做什么
git checkout -b add-algorithm-notes
# 或者
git checkout -b fix-broken-links-in-career
```

### 第四步：搭建本地预览环境

项目通过 `pyproject.toml` 和 `uv.lock` 固定 Python 3.11、`uv==0.11.16` 及 MkDocs 依赖。先按 [uv 官方安装说明](https://docs.astral.sh/uv/getting-started/installation/)安装对应版本，再在仓库根目录执行：

```bash
# Install the exact locked environment
uv sync --locked

# Start the local preview server
uv run --locked mkdocs serve
```

启动成功后，按终端显示的地址访问；当前配置通常为 `http://127.0.0.1:8000/SurviveNJU-CS/`。保存文件后页面会自动刷新。

!!! warning "不要另建一套未锁定环境"
    仓库没有 `requirements.txt`，也不使用全局 `pip install mkdocs-material` 作为维护流程。未锁定环境可能产生与 CI 不一致的渲染结果。

### 第五步：编写内容

在 `docs/` 目录下找到对应位置，修改或新建 Markdown 文件。详见下方「内容规范」章节。

### 第六步：提交更改

```bash
# 查看修改了哪些文件
git status

# 添加修改
git add docs/courses/algorithm/notes.md   # 精确添加
# 或者
git add .                                  # 添加所有修改（用前先 git status 确认）

# 提交，commit message 用中文简洁描述
git commit -m "添加算法课笔记：排序算法部分"

# 推送到你 fork 的仓库
git push origin add-algorithm-notes
```

### 第七步：创建 Pull Request

1. 打开你 Fork 的仓库页面，GitHub 会提示你创建 Pull Request
2. 点击 **Compare & pull request**
3. 填写 PR 标题（简洁描述修改内容）
4. 在正文中简要说明：
   - 你修改/添加了什么
   - 事实性修改对应的来源、适用年份或学期和核验日期
   - 如果是经验分享，说明样本和适用条件；无需公开真实身份、成绩或录取材料
5. 提交 PR，等待 maintainer review

review 可能要求补充来源、收窄结论或删除存在版权、隐私和学术诚信风险的内容。一般 Issue 和 PR 无法承诺固定回复时限；可定位的侵权与不当链接通知按[声明与免责](disclaimer.md)中的专项时限处理。

---

## 本地开发环境详解

```bash
# Install or refresh the locked environment
uv sync --locked

# Preview with live reload
uv run --locked mkdocs serve

# Required validation before submitting a PR
uv run --locked mkdocs build --strict
```

如果你新增了页面，记得同时在 `mkdocs.yml` 的 `nav` 部分添加对应条目，否则页面不会出现在导航栏中。

---

## 内容规范

### 语言约定

- **正文内容**：使用**中文**和同学之间直接、尊重的语气；事实判断保持克制，不用身份或届别代替证据
- **代码、命令、配置文件**：使用英文，放在代码块中
- **专业术语**：首次出现时可以给出英文原文，如"主成分分析（PCA, Principal Component Analysis）"

### 文件结构规范

```
docs/
├── index.md              # Site home
├── preface/              # Project scope and contribution rules
├── getting-started/      # New-student and major information
├── academics/            # Academic rules and procedures
├── courses/              # Course identities and knowledge maps
├── resources/            # Public-resource indexes
├── career/               # Postgraduate study and careers
├── labs/                 # Research-group navigation
└── campus-life/          # Campus services and safety
```

每个文件：
- 以一级标题 `#` 开头
- 标题下方有一段简短的介绍段落
- 使用二级标题 `##` 组织主要内容

### 可以贡献的内容

!!! tip "常见贡献场景"
    - **事实纠错**：用当前一手来源修正政策、课程、电话、地点或机构信息
    - **课程知识地图**：提交自己撰写的知识结构和学习方法，并与当期考试范围分开
    - **资源链接**：补充开放仓库、公开课或工具，同时标注维护者、许可证和风险
    - **经验分享**：记录推免、考研、出国、科研或实习经历，注明年份、样本和适用条件
    - **链接维护**：报告失效、重定向、内容变更或来源冲突

### 投稿规则与 PR 提交须知

提交 PR 即表示贡献者确认：其提交内容为原创内容、事实性整理或有权使用的材料；未包含未授权教材、课件、试卷、答案、课程录像、商业电子书、他人隐私信息或违反课程学术诚信要求的内容；贡献者同意其原创文字内容按本项目内容许可证发布。维护者有权基于版权、隐私、学术诚信、事实准确性或社区安全原因修改、拒绝或删除相关内容。

### 严格禁止的内容

!!! danger "禁止收录清单（红线，绝对不可触碰）"
    本项目严格不收录以下内容：
    - ❌ 未公开授权的教师 PPT、讲义、试卷、答案、课程录像；
    - ❌ 商业教材 PDF、盗版电子书、网盘合集；
    - ❌ 作业答案、实验完整代码、考试押题资料；
    - ❌ 涉及个人隐私的 GPA、排名、联系方式、申请材料；
    - ❌ 对具体教师、助教、同学的人身评价；
    - ❌ 无来源、无法核验、明显过时的政策信息。

### Markdown 写作规范

- 使用 MkDocs Material 的 admonitions 突出重要信息：

```markdown
!!! note "提示"
    这是一条普通提示。

!!! tip "小技巧"
    这是一条实用技巧。

!!! warning "注意"
    这是一条需要注意的事项。

!!! danger "红线"
    这是绝对不能做的事。
```

- 表格用于对比信息，代码块指定语言高亮
- 内部链接使用相对路径，如 `[贡献指南](../preface/contributing.md)`
- 外部链接写成 `[显示文字](https://example.com)` 的格式

---

## Issue 提交规范

如果你不打算直接修改文件，可以通过 [提交 Issue](https://github.com/foxsplendid/SurviveNJU-CS/issues/new) 来参与：

!!! danger "Issue 内容默认公开"
    不要提交姓名、学号、电话、邮箱、成绩单、排名、申请材料、身份文件、Cookie、Token、内部系统截图，或未公开课程题目与资料。报告问题通常只需要本站页面 URL、错误段落、公开来源和建议修改方向。

请在 Issue 标题前加上对应标签前缀，方便分类：

| 前缀 | 用途 | 示例标题 |
|---|---|---|
| `[错误]` | 报告内容错误或链接失效 | `[错误] 保研时间线页面中夏令营时间有误` |
| `[建议]` | 提出新内容需求 | `[建议] 希望增加算法竞赛入门指南` |
| `[问题]` | 提问（我们会尽力解答） | `[问题] 关于转专业的条件我不太理解` |
| `[侵权]` | 报告版权问题 | `[侵权] 某页面包含未授权的课件内容` |

---

## 贡献者致谢

通过 PR 合入的提交通常会进入 Git 历史，并可能出现在 GitHub 的自动 Contributors 统计中；具体展示受合并方式和 GitHub 统计规则影响，项目不作固定展示承诺。

如果你希望在具体页面署名，可以在内容末尾添加：

```markdown
---
*本节由 [@your_github_id](https://github.com/your_github_id)（届别/专业，可选）撰写，最后更新于 YYYY年MM月。*
```

---

## 如果你完全不会 Git

可以先提交一个最小化 [GitHub Issue](https://github.com/foxsplendid/SurviveNJU-CS/issues/new)，说明希望修正的页面、问题摘要和公开来源。不要在 Issue 中发布完整私人材料；维护者会根据可用时间评估是否转为文档任务，但不能承诺收录或一般问题的固定回复时限。侵权与不当链接通知按[声明与免责](disclaimer.md)中的专项流程处理。

---

感谢你为指南提供可核验、可维护并尊重版权与隐私的贡献。
