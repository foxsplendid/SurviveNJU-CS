# 知识表示与处理

*   **课程学分**：3 学分
*   **授课学期**：大三秋季学期
*   **授课教师**：人工智能学院 / 计算机系 Websoft 研究组教师
*   **修读阶段**：人工智能学院选修课 / 计算机系选修课

---

## 🌟 课程简介与地位

在当今以深度学习和连接主义为主流的 AI 浪潮中，《知识表示与处理》（Knowledge Representation and Processing）是**经典的符号主义人工智能（Symbolic AI）的代表性课程**。

本课程聚焦于“如何以结构化、可推理的形式在计算机中表达人类知识”。你将学习到本体论（Ontology）、一阶谓词逻辑、描述逻辑，以及目前在搜索搜索引擎、智能问答和知识问答中被广泛应用的**知识图谱（Knowledge Graph）**和**语义网（Semantic Web）**技术。

---

## 📚 核心内容与期末考点

### 1. 核心理论知识点
*   **一阶逻辑与描述逻辑**：逻辑命题的表示、一阶谓词公式、描述逻辑（Description Logics）的基本算子（如 $\sqcap, \sqcup, \neg, \exists, \forall$）及推理规则。
*   **语义网标准体系**（高频考点）：
    *   **RDF (Resource Description Framework)**：三元组（Subject, Predicate, Object）的图模型。
    *   RDFS 与 **OWL (Web Ontology Language)**：类（Class）、属性（Property）的层次定义，等价、相异等公理的定义。
*   **知识图谱查询：SPARQL 语言**（必考大题）：
    *   手写 SPARQL 查询语句从 RDF 图数据中筛选出满足复杂三元组模式的目标数据。
*   **知识图谱构建与推理**：
    *   信息抽取：命名实体识别（NER）、关系抽取（Relation Extraction）。
    *   知识图谱推理：基于规则的推理（如 Datalog）、基于语义嵌入的表示学习（TransE 系列模型）。

### 2. 课程大作业与实验
通常要求小组合作实现一个完整的知识图谱应用，例如：
*   **垂直领域知识图谱的构建与查询**：选择一个感兴趣的领域（如电影、历史人物、医学），爬取数据，使用 Protégé 软件设计本体模型，将数据导入 Jena、Neo4j 等图数据库，并手写查询接口或问答系统。

---

## 💡 备考与学习攻略

1.  **攻克 SPARQL 语言大题**：
    *   期末试卷中，**手写 SPARQL 查询**占分较高。掌握 SELECT, WHERE, FILTER, OPTIONAL, UNION 等关键字的使用方法。
    *   多做几道往年真题中的 SPARQL 编写，理清图模式（Graph Pattern）的变量匹配逻辑。
2.  **理解描述逻辑的推理机制**：
    *   学会用 Tableaux 算法判定描述逻辑概念的满足性（Satisfiability）。
3.  **与 Websoft 研究组的学术连接**：
    *   南京大学的 **[Websoft 研究团队](https://github.com/nju-websoft)**（由瞿裕忠教授领衔）在知识图谱、语义网和软件工程的结合方向拥有极强的科研实力。这门课也是进入 Websoft 研究组的直通门课，对知识图谱表示学习（如 TransE）感兴趣的同学可以提前阅读他们的相关顶会论文。

---

## 🔗 推荐资源

*   💻 **[nju-websoft 官方 GitHub 组织](https://github.com/nju-websoft)**：收录了南大 Websoft 组在知识图谱、语义集成和多智能体开发方面的开源科研项目。
*   📖 **经典参考书**：《知识图谱：方法、实践与应用》（王昊奋 等著），国内目前最系统介绍知识图谱构建和推理的优秀教材。
*   ⚙️ **本体设计工具：Protégé**（`https://protege.stanford.edu/`）：斯坦福大学开发的经典本体构建软件，大作业设计实体关系类层次的必备利器。
