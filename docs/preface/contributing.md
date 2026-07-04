# 贡献指南

SurviveNJU-CS 是一个靠社区共同维护的活文档——它的价值，来自每一位曾在南大读书的同学所带来的真实经验。无论你是大一新生还是博士毕业生，无论贡献大小，我们都热烈欢迎。

这份指南告诉你如何参与进来。

---

## 贡献方式总览

!!! tip "不会用 GitHub 也没关系"
    最推荐的方式是直接提 PR，但如果你不熟悉 Git 操作，把内容发给我们同样非常欢迎！

| 贡献方式 | 适合场景 | 难度 |
|---|---|---|
| **提交 Pull Request** | 修改/新增页面内容 | ⭐⭐（需要 Git 基础） |
| **提交 Issue** | 报告错误、提建议、请求新内容 | ⭐（零门槛） |
| **邮件/私信投稿** | 不熟悉 GitHub，但有内容想分享 | ⭐（零门槛） |

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

在修改内容前，先确保能在本地预览效果：

```bash
# 1. 安装 Python（推荐 3.9+），然后安装 mkdocs-material
pip install mkdocs-material

# 2. 如果项目有额外依赖，一并安装
pip install -r requirements.txt

# 3. 启动本地开发服务器
mkdocs serve
```

启动成功后，在浏览器访问 `http://127.0.0.1:8000` 即可实时预览。每次保存文件，页面会自动刷新。

!!! tip "安装建议"
    推荐使用虚拟环境（`python -m venv .venv`）隔离依赖，避免污染全局 Python 环境。也可以使用 `conda` 或 `uv` 管理环境。

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
   - 如果是经验分享，说明你的身份背景（如"24届保研生"）以增加可信度
5. 提交 PR，等待 maintainer review

!!! tip "PR 被要求修改不要气馁"
    review 过程中提出修改意见是正常的，这是协作的一部分。我们会尽快给出反馈。

---

## 本地开发环境详解

```bash
# 完整的环境搭建流程
python -m venv .venv

# Windows 激活虚拟环境
.venv\Scripts\activate

# macOS/Linux 激活虚拟环境
source .venv/bin/activate

# 安装依赖
pip install mkdocs-material

# 常用命令
mkdocs serve          # 启动本地预览（带热重载）
mkdocs build          # 构建静态文件（提 PR 前可选择运行验证）
mkdocs serve --watch docs/  # 仅监听 docs 目录变化
```

如果你新增了页面，记得同时在 `mkdocs.yml` 的 `nav` 部分添加对应条目，否则页面不会出现在导航栏中。

---

## 内容规范

### 语言约定

- **正文内容**：使用**中文**，语气亲切、peer-to-peer（学长学姐对话学弟学妹的风格）
- **代码、命令、配置文件**：使用英文，放在代码块中
- **专业术语**：首次出现时可以给出英文原文，如"主成分分析（PCA, Principal Component Analysis）"

### 文件结构规范

```
docs/
├── index.md              # 首页
├── preface/              # 前言板块
├── courses/              # 课程资源板块
│   ├── index.md          # 板块总览
│   └── algorithm/        # 某门课
│       ├── index.md      # 课程介绍
│       └── notes.md      # 笔记
└── ...
```

每个文件：
- 以一级标题 `#` 开头
- 标题下方有一段简短的介绍段落
- 使用二级标题 `##` 组织主要内容

### 可以贡献的内容

!!! tip "常见贡献场景"
    - 📝 **课程笔记**：某门课的学习总结、知识点梳理（你自己写的）
    - 🔗 **资源链接**：某个有用的开放仓库、公开课链接、工具推荐
    - 💬 **经验分享**：保研/考研/出国/实习的亲历记录
    - 🐛 **错误修正**：发现内容过时或有误，提交修正
    - 📊 **数据补充**：补充某院校的历年录取数据等（需注明来源）

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

请在 Issue 标题前加上对应标签前缀，方便分类：

| 前缀 | 用途 | 示例标题 |
|---|---|---|
| `[错误]` | 报告内容错误或链接失效 | `[错误] 保研时间线页面中夏令营时间有误` |
| `[建议]` | 提出新内容需求 | `[建议] 希望增加算法竞赛入门指南` |
| `[问题]` | 提问（我们会尽力解答） | `[问题] 关于转专业的条件我不太理解` |
| `[侵权]` | 报告版权问题 | `[侵权] 某页面包含未授权的课件内容` |

---

## 贡献者致谢

所有通过 PR 贡献内容的同学，都将被列入贡献者名单。我们使用 GitHub 的自动贡献者统计，你的 GitHub 头像和用户名会出现在仓库主页的 Contributors 区域。

如果你希望在具体页面署名，可以在内容末尾添加：

```markdown
---
*本节由 [@your_github_id](https://github.com/your_github_id)（届别/专业，可选）撰写，最后更新于 YYYY年MM月。*
```

---

## 如果你完全不会 Git

没关系！把你想分享的内容（Word、Markdown、纯文本都行）发送到以下联系方式，我们的编辑会帮你整理格式并上线，你会在贡献者名单中获得署名：

- **GitHub Issue**：直接在 Issue 中粘贴你的文字内容，标注"[投稿]"
- 我们会在 3 天内回复处理进度

---

感谢你愿意花时间为这本指南做贡献。你的每一份经验，都可能成为某个迷茫的学弟学妹最需要的那盏灯。🙏
