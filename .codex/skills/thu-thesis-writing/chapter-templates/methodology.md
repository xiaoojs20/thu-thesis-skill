# 方法章节模板

用于模型、方法、仿真或优化规划类章节。

## 推荐结构

这类章节有一条较强的骨架约束：

1. `概述`
2. `主要内容`
3. `算例分析`
4. `本章小结`

在实际写作中，`主要内容` 通常会展开为 `x.2-x.4` 这样的多个连续小节。

```text
第x章 [方法/模型标题]
x.1 概述
x.2 定义、符号或问题分析（主要内容）
x.3 核心模型或方法（主要内容）
x.4 扩展框架、约束或优化模型（主要内容）
x.5 算例分析
x.6 本章小结
```

## 写作说明

### x.1 概述

建议交代：

1. the chapter target
2. the gap in existing methods
3. what this chapter will build

模板：

```text
针对……问题，现有方法通常难以……。
因此，本章提出……方法/模型。
本章的核心内容包括：……。
```

### x.2 定义、符号或问题分析

这一节属于章节的 `主要内容` 区块，主要用于在公式密集出现前稳定符号空间。

可包含：

- key definitions
- symbol table or notation explanation
- problem decomposition if needed

### x.3 核心模型或方法

这一节同样属于章节的 `主要内容` 区块。

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

这一节是 `主要内容` 区块的最后一部分，用来把前面内容总装成完整框架：

- objective function
- operational constraints
- balance constraints
- framework integration

If this section is an optimization-planning subsection such as `考虑……协同的……优化规划模型`, open `optimization-model-pattern.md` and follow that finer-grained pattern:

1. opening paragraph that inherits earlier submodels
2. one coupling/framework figure when the planning boundary is complex
3. `x.x.1 目标函数`, with `（1）（2）（3）` used to split objective blocks
4. `x.x.2`, `x.x.3` major constraint categories
5. inside each major constraint category, use `（1）（2）（3）` to split physical modules
6. closing paragraph that states the complete model and solver type

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

## 最终检查

- the chapter explicitly follows `概述 -> 主要内容 -> 算例分析 -> 本章小结`
- each model block solves one explicit subproblem
- equations are introduced before appearing
- notation is controlled
- experiment section validates the method rather than only showing numbers
