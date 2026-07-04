# 深度学习

*   **课程学分**：3 学分
*   **授课学期**：大三秋季学期
*   **授课教师**：人工智能学院教师组
*   **修读阶段**：人工智能学院必修课 / 计算机系选修课

---

## 🌟 课程简介与地位

如果说《机器学习导论》是为你讲解传统机器学习算法的经典之美，那么《深度学习》（Deep Learning）则是带你**直接探索现代人工智能的引擎动力**。

本课程紧跟时代步伐，从最初的感知机（Perceptron）出发，层层递进地讲解多层感知机（MLP）、反向传播算法（BP）、卷积神经网络（CNN）、循环神经网络（RNN/LSTM/GRU），直至大模型时代的核心基石——**Transformer 架构与注意力机制（Attention Mechanism）**。

---

## 📚 核心理论与期末考点

### 1. 核心理论知识点
*   **反向传播与链式法则**（必考）：
    *   手写推导简单神经网络（如含有 1 个隐层的 MLP）在特定损失函数下的**梯度反向传播公式**。
    *   梯度消失（Gradient Vanishing）与梯度爆炸（Gradient Exploding）的原因及解决方法（Residual Connection、批归一化 Batch Normalization、激活函数选择如 ReLU）。
*   **卷积神经网络 (CNN)**：
    *   卷积操作的输出尺寸计算公式：$\text{Output} = \lfloor\frac{W - F + 2P}{S}\rfloor + 1$。
    *   经典网络架构：LeNet, AlexNet, VGG, ResNet（残差连接的原理与公式）。
*   **序列模型 (RNN)**：
    *   传统 RNN 随时间反向传播（BPTT）中的梯度问题。
    *   LSTM 的门控机制（输入门、遗忘门、输出门、细胞状态，必考结构图）。
*   **Transformer 与自注意力机制**（重难点）：
    *   **自注意力机制（Self-Attention）公式**（必须熟记）：$\text{Attention}(Q, K, V) = \text{softmax}(\frac{QK^T}{\sqrt{d_k}})V$。
    *   多头注意力（Multi-Head Attention）与位置编码（Positional Encoding）的作用。

### 2. 课程大作业与实验
通常要求基于 Python 与 **PyTorch** 框架独立或合作完成一个综合性的深度学习大作业，如：
*   实现一个基于 CNN 的图像分类/目标检测系统。
*   基于 Transformer 架构手写一个简易的机器翻译模型或文本生成模型。
*   要求进行超参数调优（Learning Rate, Batch Size, Dropout Rate），并撰写详实的实验报告（包含 Loss 曲线和准确率变化图）。

---

## 💡 备考与学习攻略

1.  **熟练掌握 PyTorch 开发**：
    *   不要只停留在理论看公式。平时多在 Jupyter Notebook 里写写 PyTorch 拼装模型的代码。理解 `Dataset`、`DataLoader` 的构建，熟记训练循环（`optimizer.zero_grad()`, `loss.backward()`, `optimizer.step()`）的标准写法。
2.  **公式手推反向传播**：
    *   期末大题经常考对于给定的网络结构和损失函数，求对某个权重矩阵的偏导数。这需要你非常熟练地应用偏导数链式法则，注意矩阵求导时的转置和维度匹配。
3.  **合理利用 GPU 算力**：
    *   大作业在训练深度网络时需要 GPU 算力。尽早向学院或导师申请服务器资源，或者利用 Google Colab、Kaggle Kernels 等免费 GPU 额度，切忌拖延到最后一晚在自己的 CPU 笔记本上跑大作业模型。

---

## 🔗 推荐资源

*   📖 **推荐教材：李沐《动手学深度学习》**（`https://d2l.ai`）：目前国内最火、质量极高的深度学习自学教材。配有完整的 PyTorch/MXNet 实现代码以及视频讲解，非常适合课后巩固。
*   🎥 **经典公开课：CS231n & CS224n**：斯坦福大学的计算机视觉（CS231n）和自然语言处理（CS224n）公开课，其课后作业（Assignments）质量极高，是深度学习领域的工业标准练习。
