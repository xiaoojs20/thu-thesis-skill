# 结论章节模板

用于论文层面的结论章，或某一章的章末结论。

## 论文层面结论章结构

强约束：

- do not set section headings
- do not set subsection headings
- do not write `x.1`, `x.2`, `x.3`
- keep the whole chapter under the chapter title `第x章 结论`
- organize the body as continuous paragraphs plus numbered contribution items only
- each numbered contribution lead sentence must be bold and form an independent LaTeX paragraph
- the explanation after each numbered lead sentence must start in the next paragraph

```text
第x章 结论
1. opening summary paragraph
2. numbered main contributions
3. overall implication paragraph
```

先根据学位层次确定 `x`：

- master's thesis: `x` is often `5`
- doctoral thesis: `x` is often `6`
- if unknown, keep `x` as a placeholder until the thesis structure is confirmed

## 开头总述段

需要重述：

1. the thesis background
2. the overall contradiction or challenge
3. the thesis route
4. the overall objective

Template:

```text
随着……，系统面临……挑战。
因此，面向……的研究需要……。
本文围绕……，分别从……、……、……和……展开研究。
```

## 编号贡献项模板

每一项贡献都写成：

1. challenge
2. method
3. result
4. value

Template:

```text
\textbf{（1）提出了……}

针对……问题，本文……。
基于……，建立/构建……。
最后通过……验证了……，说明……。
```

一般重复 3 到 5 项。

## 收束段

用论文层面的发现与价值收束：

```text
本文研究表明，……。
本文的工作为……提供了……方法与分析基础。
从……角度看，本文可为……提供支撑。
```

## 章末结论变体

如果这里只是某一章的章末结论，可压缩成：

1. chapter challenge
2. chapter method chain
3. chapter validation result

Template:

```text
首先，本章针对……提出了……。
其次，构建了……。
基于此，实现了……。
最后，通过算例分析验证了……。
```

## 最终检查

- the thesis-level conclusion has no section headings or subsection headings
- every numbered contribution lead sentence is bold
- every numbered contribution lead sentence is an independent LaTeX paragraph
- conclusion is not a copy-paste of section summaries
- each contribution is thesis-level, not minor detail-level
- wording is precise and restrained
- final paragraph states real value, not generic praise
