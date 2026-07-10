# Course Notes 与 Concepts 链接整理方案

## 目标

当前知识库有两套并行结构：

- `02 - courses`：按照教材和课程顺序组织，负责叙述路径。
- `03 - concepts`：按照概念实体组织，每个重要概念单独成页。

问题在于课程章节和概念页可能重名或近似重名，例如：

- `02 - courses/.../1.6 Entropy.md`
- `03 - concepts/Entropy.md`

这会让 Obsidian 的链接、补全、图谱和反向链接变得混乱。整理目标是：

> 课程笔记是叙述线，concepts 是概念节点。正文中谈概念时链接到 concept；concept 中记录它第一次从哪一处课程笔记被引入。

---

## 核心原则

### 1. 课程文件与概念文件不共享同一命名空间

课程文件名应带有来源与章节编号，例如：

```text
Kardar - 1.6 Entropy.md
Kardar - 1.4 The Second Law.md
```

概念文件名保持干净的概念名，例如：

```text
Entropy.md
Second Law of Thermodynamics.md
```

也就是说：

- `Entropy.md` 表示概念。
- `Kardar - 1.6 Entropy.md` 表示课程章节。

不要让课程章节文件直接占用概念名。

### 2. 语义链接指向 concepts

课程正文中，如果链接的语义是“这个物理/数学概念”，应链接到 `03 - concepts`。

推荐写法：

```md
**[[Entropy|entropy]]**
```

而不是：

```md
**[[Kardar - 1.6 Entropy|entropy]]**
```

后者会把“概念”误指向“章节”。

### 3. 来源链接指向 courses

concept 文件中保留来源信息，指回课程笔记中第一次引入该概念的位置。

基础写法：

```md
First introduced in [[Kardar - 1.6 Entropy]].
```

更推荐的精确写法：

```md
First introduced at [[Kardar - 1.6 Entropy#^entropy-intro|Kardar §1.6]].
```

对应地，在课程原文第一次加粗引入处添加 block id：

```md
The **[[Entropy|entropy]]** is a state function ... ^entropy-intro
```

### 4. 不给课程文件设置概念 alias

concept 文件可以有自然语言 alias，例如：

```yaml
---
aliases:
  - entropy
---
```

但课程文件不应设置这类 alias：

```yaml
---
aliases:
  - Entropy
---
```

否则 Obsidian 补全时会重新出现“章节”和“概念”抢同一个名字的问题。

---

## 推荐的重命名

将 Kardar 课程笔记统一加上课程前缀：

```text
1.2 the Zeroth Law.md
→ Kardar - 1.2 The Zeroth Law.md

1.3 the First Law.md
→ Kardar - 1.3 The First Law.md

1.4 the Second Law.md
→ Kardar - 1.4 The Second Law.md

1.5 Carnot Engines.md
→ Kardar - 1.5 Carnot Engines.md

1.6 Entropy.md
→ Kardar - 1.6 Entropy.md

1.7 Approach to Equilibrium and the Thermodynamic Potentials.md
→ Kardar - 1.7 Approach to Equilibrium and the Thermodynamic Potentials.md
```

注意：如果不是在 Obsidian UI 中重命名，就不能依赖 Obsidian 自动更新链接。需要全库手动修复旧链接。

---

## 需要补齐的核心 concepts

至少建议新增：

```text
Zeroth Law of Thermodynamics.md
First Law of Thermodynamics.md
Second Law of Thermodynamics.md
Perpetual Motion Machines of the Second Kind.md
```

其中 `Second Law of Thermodynamics.md` 可以使用：

```yaml
---
aliases:
  - Second Law
  - the Second Law
  - second law
---
```

对应原则：

- `Second Law of Thermodynamics.md` 是概念页。
- `Kardar - 1.4 The Second Law.md` 是课程章节。

---

## 链接改写规则

### 课程正文中的概念性链接

如果原文是在谈概念，应改为 concept 链接。

例：

```md
[[1.4 the Second Law|second law]]
```

改为：

```md
[[Second Law of Thermodynamics|second law]]
```

如果同时需要引用章节来源，可以写成：

```md
[[Second Law of Thermodynamics|second law]] discussed in [[Kardar - 1.4 The Second Law|Kardar §1.4]]
```

### 课程导航或章节引用

如果链接的语义是“跳转到某一节课程笔记”，则保留 course 链接。

例：

```md
See [[Kardar - 1.6 Entropy|Kardar §1.6]].
```

### concept 文件中的来源句

当前形式：

```md
First introduced in [[Kardar - 1.6 Entropy]].
```

推荐升级为：

```md
First introduced at [[Kardar - 1.6 Entropy#^entropy-intro|Kardar §1.6]].
```

---

## Block id 命名建议

block id 用于标记课程笔记中第一次加粗引入概念的位置。

推荐格式：

```text
^concept-name-intro
```

例：

```text
^entropy-intro
^second-law-intro
^gibbs-free-energy-intro
^chemical-potential-intro
```

原则：

- 全小写。
- 单词之间用连字符。
- 以 `-intro` 结尾。
- 尽量稳定，不随句子改写而改变。

---

## 建议执行顺序

1. 记录当前 git 状态，确认哪些文件已有未提交修改。
2. 重命名课程文件，给 Kardar 章节加统一前缀。
3. 全库修复旧课程文件名链接。
4. 新建缺失 concept 文件。
5. 把课程正文里的概念性链接改到 concepts。
6. 给每个 concept 的第一次加粗引入处添加 block id。
7. 把 concept 文件中的来源句统一改成 `First introduced at ...`。
8. 检查课程文件是否误用了概念 alias。
9. 检查是否仍有 course 与 concept 同名或近似重名导致歧义。
10. 做一次全库链接审计。

---

## 审计清单

执行完成后应检查：

- [ ] 是否还存在旧课程文件名链接，例如 `[[1.6 Entropy]]`。
- [ ] 是否还存在 course 与 concept 完全同名文件。
- [ ] 所有 concept 是否都有 `First introduced at ...` 来源句。
- [ ] 所有 `First introduced at ...` 是否能解析到课程文件。
- [ ] 所有 concept 来源链接是否尽量指向第一次加粗引入处。
- [ ] 课程正文中谈概念的链接是否都指向 concepts。
- [ ] 课程导航和章节引用是否仍指向 courses。
- [ ] 课程文件是否没有抢占概念 alias。
- [ ] Markdown wikilink 格式是否正常。

---

## 最终预期结构

```text
02 - courses/
└── statistical physics of particles_Kardar/
    ├── Kardar - 1.2 The Zeroth Law.md
    ├── Kardar - 1.3 The First Law.md
    ├── Kardar - 1.4 The Second Law.md
    ├── Kardar - 1.5 Carnot Engines.md
    ├── Kardar - 1.6 Entropy.md
    └── Kardar - 1.7 Approach to Equilibrium and the Thermodynamic Potentials.md

03 - concepts/
├── Entropy.md
├── First Law of Thermodynamics.md
├── Second Law of Thermodynamics.md
├── Zeroth Law of Thermodynamics.md
└── ...
```

核心关系：

```text
course note body
  → concept page

concept page
  → first introduced location in course note
```

例：

```md
<!-- course -->
The **[[Entropy|entropy]]** is a state function ... ^entropy-intro

<!-- concept -->
First introduced at [[Kardar - 1.6 Entropy#^entropy-intro|Kardar §1.6]].
```

