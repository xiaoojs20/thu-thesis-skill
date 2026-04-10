# Thesis Structure

## Overall Thesis Shape

Use a single-problem research line:

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

This is not a stitched-paper structure. Each chapter should solve one step of the same main problem.

## Chapter Backbone

### Chapter 1: Introduction

Use:

1. `1.1 研究概述`
2. `1.2 国内外研究现状`
3. `1.3 研究思路与主要工作`

Inside `1.1`, keep:

1. research background
2. key problem
3. research significance

Inside `1.3`, keep:

1. research route
2. chapter-by-chapter main work

### Technical Chapters

For Chapters 2 to 5, prefer this pattern:

1. `x.1 概述`
2. `x.2` definition / symbol table / problem analysis
3. `x.3` core method or model
4. `x.4` expanded framework / constraints / optimization model
5. `x.5 算例分析`
6. `x.6 本章小结`

## Section Organization

When a section introduces a model, use this order:

1. problem or objective definition
2. variable or notation clarification
3. objective function or main mechanism
4. constraints or submodules
5. modeling implication

When a section introduces experiments, use this order:

1. case setting
2. scheme definition
3. parameter or boundary condition
4. result comparison
5. interpretation
6. conclusion

## Common Subsection Types

Typical subsection patterns:

1. `定义 / 指标 / 挑战`
2. `模型 / 目标函数 / 约束`
3. `边界条件说明 / 结果对比分析 / 灵敏度分析`

## Chapter Length Guidance

Recommended balance derived from the source thesis:

- introduction: about 30% of core body
- each major technical chapter: about 15% to 20%
- final conclusion: about 4% to 6%

## Figure/Table Density Guidance

- Introduction: few figures and tables; use them for background and framework only.
- Method chapters: highest figure density; use for workflow, topology, and statistical patterns.
- Planning and experiment chapters: more result figures than tables.
- Tables mainly carry:
  - scheme descriptions
  - parameters
  - result comparison

## Reusable Outline Skeleton

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
第6章 结论
```
