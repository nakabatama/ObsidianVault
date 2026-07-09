# Concepts 互链审计报告

## 1. 总体结论

当前 vault 中没有字面意义的 `concepts/` 文件夹，实际概念目录是 `03 - concepts/`；课程笔记目录是 `02 - courses/statistical physics of particles_Kardar/`。本报告按实际目录 `03 - concepts/` 审计。

整体来看，概念笔记互链偏克制，不存在明显的过度链接或关键词高亮泛滥。47 个链接出现中，45 个指向概念文件，2 个指向课程章节文件；平均每篇概念笔记 1.74 个出链。多数链接都嵌在定义句、推导句或例子句里，能帮助读者理解关系。

主要问题不是“链接太多”，而是“关系说明还不够结构化”。很多文件只有一两段正文，没有标题、别名、前置概念、相关概念或应用区块。对单个概念来说这很清爽，但对知识网络来说，读者不容易判断某条链接是定义依赖、推导依赖、对比辨析，还是只是一个例子。

当前明显 hub 概念包括 `State Function`、`Reversible Transformation`、`Response Functions`、`Carnot Engine`、`Cyclic Transformation`、`Quasi-static Transformation`。其中 `State Function` 入链最多，但自身没有出链，内容也承担了“状态变量/状态函数/平衡态条件”的多重职责，需要补强。

孤岛或半孤岛概念主要是 `Carnot Cycle`、`Carnot Theorem`、`Clausius Theorem`、`Entropy`、`Perpetual Motion Machines of the First Kind`。这些文件本身并非不重要，而是缺少来自其他概念文件的入链，导致在概念网络中不容易被发现。

## 2. 文件与链接概览

- concepts 文件数量：27 个 Markdown 文件。
- 内部链接总数：47 次链接出现。
- 指向 `03 - concepts/` 内部概念的链接：45 次。
- 指向课程章节的链接：2 次。
- 平均每个文件出链数量：约 1.74。
- 重复链接：未发现同一文件中重复链接同一概念的明显问题。

出链最多的文件：

- `03 - concepts/Response Functions.md`：4 个出链。
- `03 - concepts/Carnot Cycle.md`：3 个出链。
- `03 - concepts/Carnot Engine.md`：3 个出链。
- `03 - concepts/Clausius Theorem.md`：3 个出链。
- `03 - concepts/Entropy.md`：3 个出链。
- `03 - concepts/Kelvin-Planck Statement.md`：3 个出链。
- `03 - concepts/Thermodynamic Temperature.md`：3 个出链。

入链最多的文件：

- `03 - concepts/State Function.md`：6 个入链。
- `03 - concepts/Reversible Transformation.md`：4 个入链。
- `03 - concepts/Carnot Engine.md`：3 个入链。
- `03 - concepts/Cyclic Transformation.md`：3 个入链。
- `03 - concepts/Quasi-static Transformation.md`：3 个入链。
- `03 - concepts/Response Functions.md`：3 个入链。

没有出链的文件：

- `03 - concepts/Clausius Inequality.md`
- `03 - concepts/State Function.md`

没有来自其他概念文件入链的文件：

- `03 - concepts/Carnot Cycle.md`
- `03 - concepts/Carnot Theorem.md`
- `03 - concepts/Clausius Theorem.md`
- `03 - concepts/Entropy.md`
- `03 - concepts/Perpetual Motion Machines of the First Kind.md`

断链或跨目录链接：

- `03 - concepts/Empirical Temperature.md` 中的 `[[1.2 the Zeroth Law|zeroth law]]` 指向课程章节 `02 - courses/.../1.2 the Zeroth Law.md`，不是概念内部链接；在整个 vault 中可解析，但在 concepts 内部图里表现为外部链接。
- `03 - concepts/Perpetual Motion Machines of the First Kind.md` 中的 `[[1.3 the First Law|first law]]` 指向课程章节 `02 - courses/.../1.3 the First Law.md`，同上。

命名约定观察：

- 概念文件统一使用英文 Title Case 文件名。
- 文件名大量使用空格，例如 `Clausius Statement.md`、`Carnot Theorem.md`。
- 未发现 YAML frontmatter、`aliases`、一级标题或统一模板。
- Obsidian 别名主要通过链接显示文本实现，例如 `[[State Function|state variable]]`。

## 3. 高质量链接示例

- 文件：`03 - concepts/Adiabatic Transformation.md`
- 链接：`[[Adiabatic Transformation]] -> [[Internal Energy]]`
- 判断：建议保留
- 理由：该链接表达了第一定律语境下内能构造的定义依赖：绝热过程中做功只依赖初末态，从而可构造内能。不是关键词高亮。

- 文件：`03 - concepts/Internal Energy.md`
- 链接：`[[Internal Energy]] -> [[Adiabatic Transformation]]`
- 判断：建议保留
- 理由：反向链接也有意义，因为内能笔记直接用绝热过程中的功来定义能量差，属于定义依赖。

- 文件：`03 - concepts/Reversible Transformation.md`
- 链接：`[[Reversible Transformation]] -> [[Quasi-static Transformation]]`
- 判断：建议保留
- 理由：正文明确说明“可逆过程必须准静态，但准静态不一定可逆”，这是典型的前置概念和对比辨析关系。

- 文件：`03 - concepts/Generalized Forces.md`
- 链接：`[[Generalized Forces]] -> [[Generalized Displacements]]`
- 判断：建议保留
- 理由：广义力和广义位移是共轭变量，正文也通过功项公式说明了配对关系。

- 文件：`03 - concepts/Kelvin-Planck Statement.md`
- 链接：`[[Kelvin-Planck Statement]] -> [[Clausius Statement]]`
- 判断：建议保留
- 理由：两个表述在第二定律中等价，正文明确写出等价关系，属于高价值对比/等价链接。

- 文件：`03 - concepts/Entropy.md`
- 链接：`[[Entropy]] -> [[Clausius Inequality]]`
- 判断：建议保留
- 理由：熵的定义和 Clausius 不等式之间存在推导关系，当前正文给出了公式上下文。

- 文件：`03 - concepts/Thermodynamic Temperature.md`
- 链接：`[[Thermodynamic Temperature]] -> [[Carnot Relation]]`
- 判断：建议保留
- 理由：热力学温标通过可逆热机普适效率建立，Carnot relation 是核心表达式。

## 4. 低价值或可疑链接

整体没有发现需要高置信度删除的链接；当前问题更多是“说明不足”而非“链接噪音”。以下链接建议弱化、改写或补强。

- *文件：`03 - concepts/Empirical Temperature.md`*
- *链接：`[[Empirical Temperature]] -> [[State Function|state variable]]`*
- *判断：建议弱化 / 需要人工确认*
- *理由：链接显示文本是 `state variable`，但目标文件是 `State Function.md`。在热力学语境中状态变量和状态函数高度相关，但二者不完全等同；当前 `State Function.md` 又同时列举 pressure、volume 等变量，边界略混。*
- *建议修改：如果你希望保留一个宽义节点，可把 `State Function.md` 扩展为“state variables and state functions”；否则建议新增 `State Variable.md`，或把此处改为普通文本 `state variable`，避免概念混淆。*
==修改建议：增加state variable的词条与state function辨析，此处改为链接到state variable==

- 文件：`03 - concepts/Heat Capacities.md`
- 链接：`[[Heat Capacities]] -> [[State Function|state function]]`
- 判断：建议补强，不建议删除
- 理由：这条链接的语义是“heat is not a state function”，本身很重要；但目标文件 `State Function.md` 没有解释 path function / 非状态函数，因此读者点过去后支撑不足。
- 建议修改：在 `State Function.md` 中补一小段“与路径量的区别”，再保留该链接。
==修改建议：增加path function的词条与state function辨析，此处改为链接到path function==

- 文件：`03 - concepts/Response Functions.md`
- 链接：`[[Response Functions]] -> [[Heat Capacities]]`、`[[Isothermal Compressibility]]`、`[[Magnetic Susceptibility]]`、`[[Thermal Expansion Coefficient]]`
- 判断：建议移到结构化“例子/子类”区，或补一句分类说明
- 理由：这些链接是合理的例子关系，但当前是一个列表句。随着响应函数例子增加，这个句子会变成简单枚举。
- 建议修改：改为“常见例子”区块，说明每个例子响应的外部变量。

- 文件：`03 - concepts/Thermodynamic Temperature.md`
- 链接：`[[Thermodynamic Temperature]] -> [[Carnot Engine|reversible heat engines]]`
- 判断：建议改写
- 理由：显示文本是复数的 reversible heat engines，但目标是 `Carnot Engine.md`。热力学温标依赖“所有可逆热机的普适效率”，其理论支点更接近 `Carnot Theorem`。
- ==建议修改：在定义句后同时引入 `[[Carnot Theorem]]`，把现有链接改成更精确的 `[[Carnot Engine|Carnot engines]]`。==

## 5. 建议补充说明的链接

- 文件：`03 - concepts/State Function.md`
- 当前写法：文件没有出链，但承担 6 个入链；正文提到 examples、equilibrium、laws of thermodynamics。
- 问题：作为 hub，它没有把 `Internal Energy`、`Entropy`、`Empirical Temperature`、`Cyclic Transformation` 等入链概念组织起来。
- ==建议写法：增加一段：==
  ```markdown
  Common thermodynamic state functions include [[Internal Energy|internal energy]] and [[Entropy|entropy]]. In a [[Cyclic Transformation|cyclic transformation]], the net change of any state function is zero.
  ```

- 文件：`03 - concepts/Clausius Inequality.md`
- 当前写法：给出不等式和不可逆过程中的熵变关系，但没有任何链接。
- 问题：它是 `Clausius Theorem` 和 `Entropy` 的桥梁，却在图中没有出链。
- ==建议写法：开头改为：==
  ```markdown
  The Clausius inequality, stated in [[Clausius Theorem]], constrains heat exchange over a cycle:
  ```
  ==在第二个公式前增加：==
  ```markdown
  This inequality motivates the irreversible-process relation for [[Entropy|entropy]].
  ```

- 文件：`03 - concepts/Carnot Engine.md`
- 当前写法：定义了 Carnot engine，可逆、循环、两热源，并说可反向作为 refrigerator。
- 问题：没有链接到 `Carnot Cycle`，但 Carnot engine 的运行路径正是 Carnot cycle；这导致 `Carnot Cycle.md` 没有任何概念入链。
- ==建议写法：在第一段后增加：==
  ```markdown
  The path followed by such an engine is the [[Carnot Cycle|Carnot cycle]].
  ```

- 文件：`03 - concepts/Carnot Theorem.md`
- 当前写法：只链接到 Carnot engine。
- 问题：定理的后果“所有可逆热机同效率”是建立 `Thermodynamic Temperature` 和 `Carnot Relation` 的关键，但当前没有显式桥接。
- ==建议写法：末尾增加：==
  ```markdown
  This universality is what makes it possible to define [[Thermodynamic Temperature|thermodynamic temperature]] and derive the [[Carnot Relation|Carnot relation]].
  ```

- 文件：`03 - concepts/Response Functions.md`
- 当前写法：把四个例子放在一个 examples 句子中。
- 问题：链接真实，但没有说明每个例子的响应变量。
- 建议写法：
  ```markdown
  Common response functions include [[Heat Capacities|heat capacities]] for thermal response, [[Isothermal Compressibility|isothermal compressibility]] for volume response to pressure, [[Thermal Expansion Coefficient|thermal expansion coefficient]] for volume response to temperature, and [[Magnetic Susceptibility|magnetic susceptibility]] for magnetic response.
  ```













20260706晚审核至此














## 6. 建议新增的链接

- 文件：`03 - concepts/Carnot Engine.md`
- 建议新增链接：`[[Carnot Cycle]]`
- 关系类型：定义依赖 / 应用关系
- 理由：Carnot engine 的定义不仅是“可逆热机”，还包括它执行的具体循环路径。当前 `Carnot Cycle.md` 是孤岛，应从 engine 链回。
- 建议插入位置：正文定义段后。

- 文件：`03 - concepts/Carnot Theorem.md`
- 建议新增链接：`[[Thermodynamic Temperature]]`
- 关系类型：推导依赖 / 跨章节桥梁
- 理由：Carnot 定理给出可逆热机效率的普适性，这是热力学温标构造的理论依据。
- 建议插入位置：正文末尾。

- 文件：`03 - concepts/Carnot Theorem.md`
- 建议新增链接：`[[Carnot Relation]]`
- 关系类型：推导依赖
- 理由：Carnot relation 是普适效率进一步写成温度比后的表达。
- 建议插入位置：正文末尾，与热力学温度同句。

- 文件：`03 - concepts/Clausius Inequality.md`
- 建议新增链接：`[[Clausius Theorem]]`
- 关系类型：推导依赖
- 理由：当前不等式本身来自 Clausius theorem；新增链接可把 theorem 文件从孤岛中拉回核心链路。
- 建议插入位置：开头定义句。

- 文件：`03 - concepts/Clausius Inequality.md`
- 建议新增链接：`[[Entropy]]`
- 关系类型：推导依赖 / 应用关系
- 理由：第二个公式已经使用 `S(B)-S(A)`，本质是在说明熵对不可逆过程的约束。
- 建议插入位置：第二个公式前后。

- 文件：`03 - concepts/Entropy.md`
- 建议新增链接：`[[Clausius Theorem]]`
- 关系类型：推导依赖
- 理由：课程笔记 `1.6 Entropy.md` 中，熵从 Clausius theorem 和路径无关性导出；概念笔记中可显式保留该推导桥梁。
- 建议插入位置：定义段第一句或公式前。

- 文件：`03 - concepts/State Function.md`
- 建议新增链接：`[[Internal Energy]]`、`[[Entropy]]`、`[[Cyclic Transformation]]`
- 关系类型：例子 / 应用关系
- 理由：该文件是入链 hub，但没有把典型状态函数和循环过程中的性质组织出来。
- 建议插入位置：新增“Examples”和“Useful property”小段。

- 文件：`03 - concepts/Thermodynamic Temperature.md`
- 建议新增链接：`[[Carnot Theorem]]`
- 关系类型：前置知识 / 推导依赖
- 理由：热力学温度依赖可逆热机效率的普适性；这正是 Carnot theorem 的后果。
- 建议插入位置：第一段定义句后。

- 文件：`03 - concepts/Perpetual Motion Machines of the First Kind.md`
- 建议新增链接：不建议强行新增概念内链；建议考虑新增 `First Law of Thermodynamics.md` 后再链接。
- 关系类型：前置知识
- 理由：它当前只依赖课程章节 `[[1.3 the First Law|first law]]`。如果概念层需要自洽，第一定律应成为概念文件；否则保留课程链接即可。
- 建议插入位置：暂不修改，先决定是否新建 First Law 概念。

## 7. 文件层面的重构建议

- 建议补强：`03 - concepts/State Function.md`
  - 原因：入链最多，但没有出链，也没有明确区分 state variable、state function、path-dependent quantity。
  - 建议：增加“Definition”“Examples”“Contrast with path functions”“Cyclic transformations”四个小段。

- 建议补强：`03 - concepts/Clausius Inequality.md`
  - 原因：内容重要但无出链；应连接 `Clausius Theorem` 与 `Entropy`。
  - 建议：保留短笔记形式，但加两句关系说明即可。

- 建议补强：`03 - concepts/Carnot Theorem.md`
  - 原因：无入链，但它是 `Thermodynamic Temperature` 和 `Carnot Relation` 的理论前置。
  - 建议：从 `Thermodynamic Temperature.md` 或 `Carnot Engine.md` 链入它。

- 建议补强：`03 - concepts/Entropy.md`
  - 原因：无入链，但它是第一、第二定律后续应用的核心概念。
  - 建议：从 `Clausius Inequality.md` 链入；后续如新增 `First Law of Thermodynamics.md`，可加入热力学基本关系。

- 建议暂不合并：`Generalized Forces.md` 与 `Generalized Displacements.md`
  - 原因：虽然高度配对，但一个是 intensive conjugate variable，一个是 extensive displacement；分开有助于辨析。

- 建议暂不合并：`Kelvin-Planck Statement.md` 与 `Clausius Statement.md`
  - 原因：二者等价但分别刻画热机和制冷机的禁忌形式，分开能保留第二定律两种表述的对照。

- 可考虑合并或降级：`Carnot Relation.md`
  - 原因：当前内容较薄，完全依赖 `Thermodynamic Temperature.md` 和 Carnot engine 公式。
  - 建议：如果后续不会单独展开推导，可把它作为 `Thermodynamic Temperature.md` 的小节；如果会在熵、Carnot 定理中多次引用，则保留独立文件。

- 可考虑新增：`First Law of Thermodynamics.md`
  - 原因：当前 `Perpetual Motion Machines of the First Kind.md` 和 `Internal Energy.md` 都依赖第一定律，但概念层没有第一定律节点。
  - 建议：如果 concepts 目录要形成自洽概念网络，第一、第二、零定律都适合进入概念层；如果课程章节已足够，则不必新增。

## 8. 推荐的概念笔记模板

不建议给每个文件机械填满模板。对于当前这种短概念笔记，推荐使用轻量模板，只在确实需要时保留相关区块：

```markdown
# 概念名

一句话定义。

## Definition / Core Idea

用 1-3 段说明概念本身。正文中的链接只放定义依赖、推导依赖或必须马上理解的概念。

## Key Relation

必要公式、等价表述或核心性质。

## Related Concepts

- Prerequisite: [[...]]，说明为什么是前置概念。
- Paired concept: [[...]]，说明配对关系。
- Contrast: [[...]]，说明容易混淆处。
- Application: [[...]]，说明它用于哪里。
```

使用原则：

- 正文链接：放“读到这里必须理解”的概念，例如定义依赖、公式推导依赖。
- Related Concepts 区块：放“读完后值得横向跳转”的概念，例如对比、例子、应用。
- 不要求每篇都有 Related Concepts；只有当出链超过 3 个，或概念关系类型不明显时再加。

适合做 hub note / MOC 的主题：

- `Response Functions`：已经天然承担响应函数家族的索引。
- `State Function`：适合做状态量、路径量、循环过程性质的中心节点，但需要补强。
- 建议新增 MOC：`Thermodynamic Transformations`，组织 `Quasi-static Transformation`、`Reversible Transformation`、`Cyclic Transformation`、`Adiabatic Transformation`。
- 建议新增 MOC：`Second Law of Thermodynamics`，组织 `Idealized Heat Engine`、`Idealized Refrigerator`、`Kelvin-Planck Statement`、`Clausius Statement`、`Carnot Engine`、`Carnot Theorem`、`Clausius Theorem`、`Entropy`。

## 9. 优先级修改清单

### P0：最应该先改

- 在 `Clausius Inequality.md` 增加到 `Clausius Theorem` 和 `Entropy` 的链接说明。
- 在 `Carnot Engine.md` 增加到 `Carnot Cycle` 的链接说明。
- 在 `Carnot Theorem.md` 增加到 `Thermodynamic Temperature` 和 `Carnot Relation` 的桥梁句。
- 补强 `State Function.md`，至少加入 `Internal Energy`、`Entropy`、`Cyclic Transformation` 的说明性链接。

### P1：值得改

- 在 `Thermodynamic Temperature.md` 增加 `Carnot Theorem`，并把“reversible heat engines”与 `Carnot Engine` 的关系说得更精确。
- 把 `Response Functions.md` 中的例子列表改成带关系说明的“common response functions”句子或小列表。
- 决定是否新增 `First Law of Thermodynamics.md`，用来承接 `Internal Energy` 和 `Perpetual Motion Machines of the First Kind`。

### P2：有时间再优化

- 为核心 hub 文件增加一级标题和轻量模板。
- 考虑新增 `Thermodynamic Transformations` 与 `Second Law of Thermodynamics` 两个 MOC。
- 评估 `Carnot Relation.md` 是否继续独立，还是并入 `Thermodynamic Temperature.md`。

## 10. 可选自动修改建议

以下是低风险建议 diff，仅供确认后手动或半自动应用；本次审计没有直接修改原始概念笔记。

```diff
diff --git a/03 - concepts/Carnot Engine.md b/03 - concepts/Carnot Engine.md
@@
 A Carnot engine is a [[Reversible Transformation|reversible]] engine that runs in a [[Cyclic Transformation|cycle]] and exchanges heat only with a source at temperature $T_H$ and a sink at temperature $T_C$.
+
+The path followed by such an engine is the [[Carnot Cycle|Carnot cycle]].
```

```diff
diff --git a/03 - concepts/Clausius Inequality.md b/03 - concepts/Clausius Inequality.md
@@
-The Clausius inequality states that
+The Clausius inequality, stated in [[Clausius Theorem]], constrains heat exchange over a cycle:
@@
-For an irreversible transformation from $A$ to $B$, it implies
+For an irreversible transformation from $A$ to $B$, it implies a constraint on [[Entropy|entropy]]:
```

```diff
diff --git a/03 - concepts/Carnot Theorem.md b/03 - concepts/Carnot Theorem.md
@@
 As a result, all reversible engines operating between the same two reservoirs have the same efficiency.
+
+This universality makes it possible to define [[Thermodynamic Temperature|thermodynamic temperature]] and derive the [[Carnot Relation|Carnot relation]].
```

```diff
diff --git a/03 - concepts/State Function.md b/03 - concepts/State Function.md
@@
 The state functions are only well defined when the system is in equilibrium. That is the system does not appreciably change with time over the observation times.
+
+Common thermodynamic state functions include [[Internal Energy|internal energy]] and [[Entropy|entropy]]. In a [[Cyclic Transformation|cyclic transformation]], the net change of any state function is zero.
```

未保留辅助脚本。本报告使用一次性命令统计链接和上下文，没有向仓库写入脚本文件。
