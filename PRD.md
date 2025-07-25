# 产品需求文档 (PRD): "Python与高数之桥"

**版本**: 1.0
**日期**: 2025年7月20日

---

## 1. 产品概述 (Product Overview)

### 1.1. 产品名称
"Python与高数之桥"三周冲刺学习计划

### 1.2. 背景与问题
准计算机科学（CS）大一新生在过渡到大学学习时，普遍面临两大挑战：
1.  **高等数学的抽象性**：微积分中的极限、导数、积分等核心概念高度抽象，仅通过传统课本和公式难以建立直观、深刻的理解。
2.  **编程入门的陡峭曲线**：大学的第一门编程课节奏快，对于零基础的学生来说，很容易在初期就感到挫败和迷茫，从而跟不上进度。

本项目旨在解决这一核心痛点，通过创新的学习路径，帮助学生平滑地度过这一关键时期。

### 1.3. 产品愿景与目标
**愿景**: 改变学生学习数学的方式——从被动接受公式，到主动探索、验证和创造。
**核心目标**: 本计划的根本目标并非培养Python专家或数学家，而是**建立一座坚实的桥梁**，让学生能够熟练运用Python这个强大的工具，去**可视化（Visualize）**和**具象化（Embody）**抽象的数学概念，从而在大学第一学期就建立起在数理和编程领域的双重自信。

---

## 2. 目标用户 (Target Audience)

### 2.1. 用户画像 (Persona)
*   **身份**: 准计算机科学（CS）大一新生。
*   **特质**:
    *   具备良好的高中数学基础和较强的逻辑思维能力。
    *   对技术和编程抱有天然的好奇心和热情。
    *   编程经验为零或非常有限。
*   **痛点与需求**:
    *   渴望在大学开始前抢占先机，为即将到来的学业挑战做好准备。
    *   需要一种更直观、更“动手”的方式来理解抽象的高等数学。
    *   希望在正式开课前，无压力地掌握基础编程技能，避免“入门即劝退”。

---

## 3. 产品需求与功能 (Product Requirements & Features)

### 3.1. 核心交付物 (Key Deliverable)
学生在计划结束时，需独立完成并提交一份名为 **“我的第一个微积分探索笔记本”** 的Jupyter Notebook (`.ipynb`) 文件。这份文件应全面展示其三周的学习成果。

### 3.2. 功能模块 (按学习周划分)

#### 3.2.1. 第一周需求: 奠定基础——从代码到图像
*   **用户故事**: 作为一名新生，我希望能快速搭建好编程环境，并学会用代码绘制出我熟悉的函数图像。
*   **功能点**:
    *   **环境掌握**: 熟练使用Jupyter Notebook，包括创建、保存、运行代码单元和编写Markdown笔记。
    *   **Python基础**: 掌握变量、基本数据类型、数学运算和`print()`函数。
    *   **核心库入门**:
        *   使用`NumPy`的`linspace`生成数据点。
        *   使用`Matplotlib`的`plot`函数绘制2D图像。
        *   能够对图像进行基本美化（标题、坐标轴标签、网格）。
    *   **函数定义**: 学会用`def`定义Python函数，以对应数学中的`f(x)`。
*   **验收标准**: 能独立编写代码，绘制出任意高中阶段常见函数（如二次函数、三角函数、指数函数）的图像。

#### 3.2.2. 第二周需求: 深入核心——可视化微积分概念
*   **用户故事**: 作为一名学生，我希望不仅能看到公式，更能“看到”极限的逼近过程和导数的几何意义。
*   **功能点**:
    *   **极限可视化**:
        *   使用`for`循环或NumPy数组计算并观察数列极限（如 `(1+1/n)^n`）。
        *   通过生成一系列趋近于某点的x值，来验证函数极限（如 `sin(x)/x`）。
    *   **导数可视化**:
        *   编写代码计算函数某点上割线的斜率。
        *   通过动态改变割线的一个点，观察割线斜率如何逼近切线斜率（即导数值）。
        *   在函数图像上，同时绘制出割线与最终的切线，直观对比。
*   **验收标准**: 能用代码和图像，清晰地展示函数极限的收敛过程，以及“切线是割线的极限”这一核心思想。

#### 3.2.3. 第三周需求: 解锁神器——符号计算与积分初步
*   **用户故事**: 作为一名学习者，我希望能用程序帮我解决复杂的符号运算，并理解积分的面积本质。
*   **功能点**:
    *   **符号计算 (SymPy)**:
        *   使用`SymPy`进行符号的定义、求导、积分和求极限。
        *   能够验证手动计算的导数或积分结果是否正确。
        *   掌握`lambdify`，将符号表达式转换为可用于绘图的数值函数。
    *   **积分可视化 (黎曼和)**:
        *   编写代码计算给定函数在某区间上的黎曼和。
        *   使用`Matplotlib`的条形图功能，将黎曼和的矩形绘制在函数曲线下方。
        *   通过增加矩形数量（`n`），动态展示黎曼和如何逼近定积分的精确值。
*   **验收标准**: 能使用`SymPy`自动求解导数和积分，并能用黎曼和的方式，通过代码和图像解释定积分的“曲线下面积”的本质。

### 3.3. 非功能性需求
*   **学习工具**: 必须使用Anaconda发行版，以确保Python环境和核心库（Jupyter, NumPy, Matplotlib）的一致性。
*   **学习理念**: 整个学习过程必须遵循以下原则：
    *   **目标导向**: 以“能用”为目的，不纠结于语法的细枝末节。
    *   **动手实践**: 每一行代码都需亲手实践和修改，鼓励“玩代码”。
    *   **拥抱错误**: 将解决错误信息视为核心学习技能之一。
    *   **建立联系**: 时刻思考编程知识与数学概念之间的关联。

---

## 4. 约束与假设 (Constraints & Assumptions)

### 4.1. 时间约束
*   整个学习计划严格限定在**3周**内完成，总投入时间为**60小时**。
*   这是一个高强度的冲刺计划，要求学习者有集中的时间投入。

### 4.2. 资源与环境假设
*   **自学模式**: 计划为自学者设计，不依赖教师的实时指导。
*   **资源明确**: 所有学习资源和工具都应是免费且易于获取的。
*   **硬件假设**: 学习者拥有一台可以正常安装和运行Anaconda的个人电脑。

---

## 5. 成功衡量指标 (Success Metrics)

### 5.1. 产出指标 (Output Metrics)
*   **完成率**: 学习者成功完成并提交“我的第一个微积分探索笔记本”的比例。
*   **完整性**: 提交的笔记本是否包含了三周所学的所有核心可视化任务。

### 5.2. 能力指标 (Capability Metrics)
*   **独立性**: 学习者是否能脱离教程，独立编写代码来绘制一个新函数的图像。
*   **迁移性**: 学习者是否能举一反三，尝试用所学方法探索课本中遇到的其他数学概念。

### 5.3. 理解指标 (Understanding Metrics)
*   **概念解释**: 通过观察学生的笔记和代码，评估其是否对极限、导数、积分的核心概念建立了更直观、物理的理解，而不仅仅是记忆公式。
*   **学习反馈**: 通过问卷或访谈，收集学生对这种“编程+数学”交叉学习方法的有效性反馈。
