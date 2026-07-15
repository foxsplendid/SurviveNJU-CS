# SurviveNJU-CS | 南京大学泛 CS 学习与校园生存指南

<p align="center">
  <strong>南京大学泛 CS 方向的非官方学习、办事与发展指南</strong>
</p>

<p align="center">
  <a href="https://creativecommons.org/licenses/by-nc-sa/4.0/deed.zh-hans">
    <img src="https://img.shields.io/badge/license-CC%20BY--NC--SA%204.0-blue.svg" alt="License">
  </a>
  <a href="https://github.com/foxsplendid/SurviveNJU-CS/pulls">
    <img src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg" alt="PRs Welcome">
  </a>
</p>

---

## 📖 关于本项目

本项目受 [上海交通大学生存手册（SurviveSJTU）](https://github.com/SurviveSJTU/SurviveSJTUManual) 启发，面向南京大学计算机科学与技术、人工智能、软件工程及相关方向的同学，持续整理课程学习、学业规则、升学就业、研究资源与校园生活信息。

**SurviveNJU-CS 是一个非官方、公益、非营利的学习资源索引与经验共建项目。** 本站不重新分发受版权保护的试卷原题、教师课件、教材电子版等文件；涉及第三方仓库和课程资料时，只提供公开链接索引、风险提示和使用边界说明。

所有涉及培养方案、选课、转专业、推免、处分、医疗和紧急求助等会影响个人权益或安全的信息，都应回到南京大学相关部门、院系和课程当期发布的一手信息。本项目帮助定位来源和理解背景，不替代官方文件、专业判断或现场指挥。

## 核验原则

本站按“零信任”原则维护内容：公开可访问不等于内容正确，GitHub 仓库公开不等于其中每个文件都可再分发，往届经验也不等于现行规则。

- **规则性事实**：优先引用南京大学及所属部门、院系发布的现行文件，并标明适用年份或核验日期。
- **课程实施**：区分稳定知识结构与教师、学分、作业、考试等年份敏感信息；后者以当期教务系统和课程通知为准。
- **第三方资料**：说明其社区或个人属性，不把收录表述为学校背书，并单独核对许可证、凭证安全与学术诚信风险。
- **冲突信息**：不擅自选择看似更新的一方作为事实；保留冲突来源并给出电话或发布部门等复核路径。
- **经验建议**：使用条件化表述，不承诺成绩、录取、竞赛回报或就业结果。

本轮系统审查批次日期为 **2026-07-14**，不代表所有条目在同一天重新发布或永久有效。具体事实以对应页面、表格或来源旁标注的适用版本和核验日期为准；时效性内容使用时仍需重新打开原始来源。

## 🌟 内容概览

| 板块 | 内容 |
|------|------|
| **新生入门** | 泛 CS 专业概览、转专业指南、学习方法与节奏、信息素养 |
| **学业规则** | 选课策略、GPA 解读、学籍与学业程序、期末备考、学术诚信 |
| **课程指南** | 计算机、人工智能、软件工程课程的知识结构，以及苏州校区三个泛 CS 相关学院的官方入口、版本差异与诚信边界 |
| **资源导航** | GitHub 公开资源索引、在线课程、实用工具、推荐书单、往年考试与复习资源、论文模板 |
| **升学与就业** | 考研、推免、境外升学与申请、实习求职、科研入门 |
| **研究与实验室** | 研究组、课程项目与学生技术组织的分类索引，申请前回到院系和团队主页核验 |
| **校园生活** | 紧急求助、校医院、心理支持、校园办事、社团与竞赛入口 |

## 📚 在线阅读

👉 **[点击此处在线阅读](https://foxsplendid.github.io/SurviveNJU-CS/)**

本站使用 MkDocs Material 构建，并通过 GitHub Actions 发布到 GitHub Pages。若线上页面短暂未更新，请查看仓库 Actions 中的 `Deploy MkDocs to GitHub Pages` 工作流状态。

## 🤝 如何贡献

我们欢迎所有南京大学在读及已毕业的同学贡献内容！

### 贡献方式

1. **提交 Pull Request**：Fork 本仓库，修改或新增内容后提交 PR
2. **提交 Issue**：对内容有疑问、建议或发现错误，请在 [Issue 区](https://github.com/foxsplendid/SurviveNJU-CS/issues) 提出；Issue 默认公开，请勿提交个人信息、内部材料或账号凭证
3. **投稿经验分享**：如果你希望分享课程攻略、转专业经验、升学/求职经验等，请参考 [贡献指南](docs/preface/contributing.md)

### 本地开发

```bash
# 克隆仓库
git clone https://github.com/foxsplendid/SurviveNJU-CS.git
cd SurviveNJU-CS

# 安装依赖
uv sync --locked

# 本地预览
uv run --locked mkdocs serve

# 访问 http://127.0.0.1:8000/SurviveNJU-CS/
```

## ⚖️ 版权声明

- 贡献者有权授权的本站原创文字内容采用 [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.zh-hans)；引用内容、第三方材料及贡献者无权许可的其他内容不在此许可范围内
- 本项目作为资源索引平台，所引用的外部仓库和资源版权、许可和访问规则均以原页面为准
- 本站不托管或重新分发受版权保护的课程资料；如有链接索引不当，请通过公开 Issue 提交足以定位争议内容的最小信息，不要发布身份材料、私人联系方式或未公开课程内容
- 详细声明请参阅 [声明与免责](docs/preface/disclaimer.md)

## 🙏 致谢

- 感谢 [SurviveSJTU](https://github.com/SurviveSJTU/SurviveSJTUManual) 项目的启发
- 感谢所有被本项目收录的开源仓库的作者与贡献者
- 感谢南京大学每一位无私分享学习资料的同学和老师
- 感谢 [csdiy.wiki](https://csdiy.wiki) 对CS自学社区的贡献

---

<p align="center">
  <em>「在南大，没有人是一座孤岛。」</em>
</p>
