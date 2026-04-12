# 写作模式

## 核心段落逻辑

本文件控制的是论述节奏与段落推进，而不是论文主题本身。所有名词都应围绕用户自己的研究对象重写。

默认段落推进顺序：

1. state the engineering background or phenomenon
2. state the contradiction, gap, or challenge
3. introduce what this chapter or thesis addresses
4. state the method, effect, or contribution

## 推荐衔接语

这些词要有意识地使用：

- `针对`
- `首先`
- `其次`
- `基于此`
- `最后`
- `由图可知`
- `由表可知`
- `通过上述对比分析`

不要为了“避免重复”而过度乱换说法，导致论文语体失去稳定性。

## 常用句式模板

### 方法引入

```text
针对……问题，本文提出……方法。
首先，……。
其次，……。
基于此，……。
最后，通过……验证……。
```

### 结果解读

```text
如图 x 所示，……。
由图可知，……。
相较于方案 A，方案 B 在……方面……。
通过上述对比分析，证明了……。
```

### 背景铺垫

```text
随着……，研究对象/系统/场景面临……挑战。
一方面，……；另一方面，……。
因此，如何……成为……领域的重要问题。
```

## 引言写法

引言建议按以下顺序展开：

1. macro background
2. concrete system contradiction
3. enabling technology or possible response resource
4. core scientific problem
5. subproblem decomposition
6. technical difficulties
7. significance
8. literature review
9. research route and chapter arrangement

硬规则：

1. Start broad, then narrow to the thesis problem.
2. Split the core problem into 2 to 4 subproblems.
3. For each subproblem, name 1 to 2 technical difficulties.
4. Review literature by topic, not by author order.
5. End with the thesis route and chapter tasks.

## 摘要写法

摘要可按六步展开：

1. background and overall challenge
2. core scientific problem
3. contribution 1
4. contribution 2
5. contribution 3 or 4
6. overall summary and keywords

Hard rules:

1. Do not write `第1章……第2章……`.
2. Do not insert literature review.
3. Keep each contribution to a compressed `problem -> method -> effect` block.
4. End with overall value, not with repetition.

## 结论写法

结论章保持三层结构：

1. opening paragraph:
   - restate the thesis background and overall route
2. numbered contributions:
   - each item should be `challenge -> method -> result -> value`
   - each item starts with a bold numbered lead sentence as an independent LaTeX paragraph
3. closing paragraph:
   - overall finding and broader value

Hard rules:

1. Do not create section headings or subsection headings in the thesis-level conclusion chapter.
2. Do not write `5.1`, `5.2`, `5.3` or `6.1`, `6.2`, `6.3` style structure; keep the rule generic as `x.1`, `x.2`, `x.3` are not used in the thesis-level conclusion chapter.
3. Keep the conclusion as chapter-level prose plus numbered contribution items only.
4. The numbered lead sentence must be bold and must occupy an independent LaTeX paragraph.
5. Put a blank line after the numbered lead sentence; the explanatory text must start in the next paragraph.
6. Write the numbered lead sentence in LaTeX as `\textbf{（n）提出了……}`.
7. Do not copy chapter summaries directly; rewrite each item from the full-thesis perspective.

建议的编号段模板：

```text
\textbf{（n）提出了……}

针对……问题，本文……。
基于……，建立/构建……。
最后通过……验证了……。
```

## 本章小结写法

`本章小结` 的篇幅是强约束：每个技术章节的 `本章小结` 至少应约占编译后 PDF 的 2/3 页。不能只写一段短总结；若暂时无法编译估算，应写成多个完整段落，覆盖问题回扣、方法链条、算例验证和本章对后续章节的支撑作用。

每个 `本章小结` 都应包含：

1. why the chapter was needed
2. what method chain the chapter built
3. what the case study verified

Use:

```text
首先，……。
其次，……。
基于此，……。
最后，通过算例分析证明了……。
```

`概述` 也遵循同等篇幅约束：每个技术章节的 `概述` 至少应约占编译后 PDF 的 2/3 页。写作时应至少交代章节问题来源、上一章或全文主线的承接、本章方法目标、主要内容安排和验证思路，避免只用 3 到 5 句话快速带过。

## 语气控制

应保持正式的中文工科论文语体：

- concise
- analytical
- non-emotional
- result-oriented
- technically explicit

避免：

- rhetorical flourish
- journalistic tone
- exaggerated novelty claims without evidence
- vague praise words like `效果显著` without saying on what metric
- borrowing domain nouns from the source thesis when the user is writing about another topic
