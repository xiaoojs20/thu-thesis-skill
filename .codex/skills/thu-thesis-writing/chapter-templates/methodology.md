# Methodology Chapter Template

Use this for a model, method, simulation, or optimization-planning chapter.

## Recommended Structure

```text
第x章 [方法/模型标题]
x.1 概述
x.2 定义、符号或问题分析
x.3 核心模型或方法
x.4 扩展框架、约束或优化模型
x.5 算例分析
x.6 本章小结
```

## Writing Guide

### x.1 概述

State:

1. the chapter target
2. the gap in existing methods
3. what this chapter will build

Template:

```text
针对……问题，现有方法通常难以……。
因此，本章提出……方法/模型。
本章的核心内容包括：……。
```

### x.2 定义、符号或问题分析

Use this section to stabilize the notation space before equations become dense.

Include:

- key definitions
- symbol table or notation explanation
- problem decomposition if needed

### x.3 核心模型或方法

For each subsection:

1. explain why the model block is needed
2. show equations
3. explain equation roles
4. add `式中：`
5. explain what the block achieves

Template:

```text
为描述……，构建如式（x.1）-（x.3）所示的模型。
式（x.1）描述……，式（x.2）定义……，式（x.3）计算……。
式中：……。
基于上述模型，可以实现……。
```

### x.4 扩展框架、约束或优化模型

Use this section to assemble the model into a full framework:

- objective function
- operational constraints
- balance constraints
- framework integration

### x.5 算例分析

Open `experiment.md` and follow that template.

### x.6 本章小结

Template:

```text
首先，本章针对……提出了……。
其次，构建了……。
基于此，建立了……。
最后，通过算例分析验证了……。
```

## Final Check

- each model block solves one explicit subproblem
- equations are introduced before appearing
- notation is controlled
- experiment section validates the method rather than only showing numbers
