# 软件分析

*   **课程学分**：3 学分
*   **授课学期**：大三秋季学期
*   **授课教师**：李樾副教授、谭添助理研究员（PASCAL 科研组）
*   **修读阶段**：软件学院必修课 / 计算机系选修课

---

## 🌟 课程简介与地位

由李樾和谭添老师开设的《软件分析》（Software Analysis）是一门**公认处于国际一流水准的硬核高级课程**。这门课聚焦于**静态程序分析（Static Program Analysis）**领域。

> **“在不实际运行程序的前提下，我们如何通过静态代码推导，证明程序在所有可能的执行路径中都不会发生空指针异常、内存泄漏或安全漏洞？”**

本课程不仅在国内受到了清华、北大等学子的热烈追捧，在国际学术界和自学圈中也极富声誉。其实验体系基于南大自主开发并开源的 **Tai-e (太阿) 静态分析框架**，大作业要求你亲自动手实现从指针分析到安全缺陷检测的各个分析模块。

---

## 📚 核心理论与 Tai-e 实验

### 1. 核心理论知识点
*   **静态分析导论**：声音性（Soundness）、完备性（Completeness）以及不可判定性（Undecidability - 莱斯定理）。
*   **中介表示 (IR)**：三地址码（3AC）与控制流图（CFG）的构建。
*   **数据流分析 (Data Flow Analysis)**（高频考点）：
    *   活跃变量分析 (Active Variables)、常量传播 (Constant Propagation)、可达定义分析 (Reaching Definitions)。
    *   **格理论 (Lattice Theory)** 与不动点（Fixed Point）定理：偏序集、上确界、半格、单调框架（Monotonic Framework）。
*   **过程间分析 (Interprocedural Analysis)**：
    *   调用图构建：CHA (Class Hierarchy Analysis)、RTA (Rapid Type Analysis)。
*   **指针分析 (Pointer Analysis)**（重难点）：
    *   Anderson 指针分析算法原理。
    *   上下文敏感性分析（Context Sensitivity）。

### 2. Tai-e 静态分析实验 (Assignments)
你将在 Java 编写的 **Tai-e 框架** 上完成 8 个逐步深入的实验：
*   **Assignment 1 (Constant Propagation)**：实现控制流图上的常量传播分析。
*   **Assignment 2 (Active Variables & Dead Code Detection)**：实现活跃变量分析并在此基础上检测死代码。
*   **Assignment 7 & 8 (Pointer Analysis)**：实现带有上下文敏感特性的 Anderson 指针分析。

---

## 💡 备考与学习攻略

1.  **课前高强度预习，紧跟课程视频**：
    *   课程的理论深度极大。李樾老师和谭添老师在 Bilibili 上录制了全套配套视频。**强烈建议在每次上课前，先看一遍对应的 B 站视频**，理清基本概念，否则现场听课很容易在“格”和“不动点证明”部分跟丢。
2.  **熟记数学符号与转移方程**：
    *   期末考试包含大量的理论推理与算法推演。你需要熟练手写出数据流分析的转移方程（Transfer Functions）以及格的汇聚操作（Meet Operator）。
3.  **大作业代码重构与调试**：
    *   Tai-e 的代码设计非常优雅，符合极高的面向对象设计模式规范。在写实验前，花时间理清 Tai-e 的类层次结构，理解 `Value`、`Statement`、`Method` 等核心数据类型。

---

## 🔗 推荐资源

*   🌐 **[南大《软件分析》课程官方网站](https://pascal-group.bitbucket.io/pas.html)**：存放全套 Slides 和 Assignment 要求的官网。
*   🖥️ **[Tai-e (太阿) 官方 GitHub 仓库](https://github.com/pascal-lab/Tai-e)**：南大开源的静态程序分析框架。
*   🎥 **[Bilibili 静态程序分析公开课视频](https://search.bilibili.com/all?keyword=南京大学软件分析)**：李樾和谭添老师的录制视频，制作极其精良，被誉为国内最好的静态分析自学课。
