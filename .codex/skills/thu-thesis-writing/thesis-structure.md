# 论文结构

## 全文结构

本文件只描述可复用的结构规律。诸如 `规划`、`风险`、`运行`、`建模`、`实验`、`案例分析` 等章节名称只是结构角色示例，不是必须使用的主题词。

全文应保持单一主问题研究线：

1. front matter
2. Chinese abstract
3. English abstract
4. contents, figure list, table list
5. notation/abbreviation list
6. Chapter 1 introduction
7. Chapter 2 method foundation A
8. Chapter 3 method foundation B or solution framework
9. Chapter 4 core planning/model chapter
10. Chapter 5 risk/extension/evaluation chapter
11. Chapter 6 conclusion
12. references and back matter

这不是“多篇论文拼接式”结构。每一章都应解决同一主问题链条中的一个环节。

在确定最后一章编号前，先判断论文层次：

- master's thesis: the thesis often ends in Chapter 5, so the conclusion is often Chapter 5
- doctoral thesis: the thesis often ends in Chapter 6, so the conclusion is often Chapter 6
- if the thesis level is unknown, keep the conclusion chapter number as a placeholder and do not hard-code it

不要照抄样本论文的章节主题，应改写为用户自己的研究对象，例如：

- `基础理论`
- `方法设计`
- `系统实现`
- `实验验证`
- `扩展分析`

## 章节骨架

### 第 1 章：引言

Use:

1. `1.1 研究概述`
2. `1.2 国内外研究现状`
3. `1.3 研究思路与主要工作`

`1.1` 内部保持：

1. research background
2. key problem
3. research significance

`1.3` 内部保持：

1. research route
2. chapter-by-chapter main work

对硕士论文，第 1 章引言内部建议按编译后 PDF 页数分配：

- `研究背景和意义`: 1-2 页。
- `国内外研究现状`: 7-8 页。
- `研究思路与主要工作`: 3-4 页。

三部分合计优先落在 11-13 页；若达到 14 页或超出分项范围，应记录实际页数、偏离量和原因。

### 技术章节

对结论章之前的技术章节，强制保持以下模式：

1. `x.1 概述`
2. `x.2-x.4 主要内容`
5. `x.5 算例分析`
6. `x.6 本章小结`

这是强约束，不是松散建议。

含义如下：

- `概述`: chapter target, problem, and content map
- `主要内容`: one or more consecutive sections carrying definitions, models, methods, frameworks, constraints, algorithms, or derivations
- `算例分析`: validation through cases, experiments, simulations, or comparative studies
- `本章小结`: chapter-level recap of problem, method chain, and validated result

`主要内容` does not have to appear as a literal section title, but it must occupy the middle block between `概述` and `算例分析`.

`概述` 与 `本章小结` 的篇幅都是强约束：每一节至少应约占编译后 PDF 的 2/3 页。起草时不得把 `概述` 写成一段背景说明，也不得把 `本章小结` 写成一段短总结；若尚未编译 PDF，应按多个完整段落展开，使其在编译后大致达到该版面量。

### 论文层面的结论章

对论文层面的结论章，强制保持以下模式：

1. chapter title only: `第x章 结论`
2. opening summary paragraph
3. numbered main contributions
4. closing paragraph

这同样是强约束。

If the thesis is a master's thesis, `x` is often `5`.

If the thesis is a doctoral thesis, `x` is often `6`.

Do not create `x.1`, `x.2`, `x.3` or any subsection headings inside the conclusion chapter.

## 节内组织顺序

当某一节引入模型时，优先按以下顺序：

1. problem or objective definition
2. variable or notation clarification
3. objective function or main mechanism
4. constraints or submodules
5. modeling implication

当某一节引入实验/算例时，优先按以下顺序：

1. case setting
2. scheme definition
3. parameter or boundary condition
4. result comparison
5. interpretation
6. conclusion

## 常见小节类型

Typical subsection patterns:

1. `定义 / 指标 / 挑战`
2. `模型 / 目标函数 / 约束`
3. `边界条件说明 / 结果对比分析 / 灵敏度分析`

## 章节篇幅建议

根据样本论文提炼出的推荐比例：

- introduction: about 30% of core body
- each major technical chapter: about 15% to 20%
- final conclusion: about 4% to 6%

硕士论文还应执行更具体的编译后篇幅控制：

- 第 1 章引言部分编译后大约控制在 9-13 页，最多不超过 15 页；其中 `研究背景和意义` 建议 1-2 页，`国内外研究现状` 建议 7-8 页，`研究思路与主要工作` 建议 3-4 页，三部分合计优先落在 11-13 页。
- 第 5 章结论部分编译后大约控制在 2-3 页，最多不超过 4 页。
- 这是较强约束；若由于学校模板、图表密度、研究内容或导师要求导致无法满足，应在编译后明确记录实际页数、偏离量和原因。

硕士论文的第 2 章到第 4 章还应执行更具体的编译后篇幅控制：

- 每一章编译后大约控制在 25 页，最多不超过 30 页。
- 每一章中的 `算例分析 + 本章小结` 合计控制在 10-15 页。
- 这是较强约束；若由于图表、公式、学校模板或研究内容差异导致无法满足，应在编译后明确记录实际页数、偏离量和原因。
- 每次完成 LaTeX 编译后，都要检查第 1 章、第 2-4 章、第 5 章总页数，以及第 2-4 章中的 `算例分析 + 本章小结` 页数，而不是只在定稿前检查一次。

## 图表密度建议

- Introduction: few figures and tables; use them for background and framework only.
- Method chapters: highest figure density; use for workflow, topology, and statistical patterns.
- Planning and experiment chapters: more result figures than tables.
- Tables mainly carry:
  - scheme descriptions
  - parameters
  - result comparison

## 可复用提纲骨架

```text
第1章 引言
  1.1 研究概述
    1.1.1 研究背景
    1.1.2 关键问题
    1.1.3 研究意义
  1.2 国内外研究现状
  1.3 研究思路与主要工作

第2章 研究对象分析与基础建模
  2.1 概述
  2.2 对象定义与指标
  2.3 建模方法
  2.4 分模块建模
  2.5 算例分析
  2.6 本章小结

第3章 求解框架或运行模拟方法
第4章 核心模型与优化规划
第5章 风险评估或扩展分析
第x章 结论
```

套用该骨架时，要保留推进顺序和节级逻辑，但章节标题必须完全围绕目标论文主题重写。

对技术章节，不可打破的顺序是：

1. `概述`
2. `主要内容`
3. `算例分析`
4. `本章小结`

对论文层面的结论章，不可打破的规则是：

1. no section headings
2. no subsection headings
3. direct chapter-level prose with numbered contribution items
