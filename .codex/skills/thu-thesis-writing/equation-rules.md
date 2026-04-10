# Equation, Figure, and Table Rules

## Equation Explanation Style

Use this fixed sequence:

1. explain why the equation is needed
2. show the equation or equation group
3. explain the role of each equation if there are multiple equations
4. add `式中：` to define symbols
5. state what the equation block accomplishes in the thesis

## Equation Group Template

```text
……如式（x.1）-（x.4）所示。
式（x.1）描述……，式（x.2）构建……，式（x.3）计算……，式（x.4）给出……。
式中：A 表示……；B 表示……；C 为……。
基于式（x.1）-（x.4）构建的……，实现了……。
```

## `式中：` Rules

1. Start with `式中：`.
2. Follow variable appearance order.
3. Use `；` to separate items.
4. Explain physical meaning first, then role, range, or bound.

Template:

```text
式中：X 表示……；Y 表示……；Z 为……，其上限为……。
```

## What To Explain After Equations

Do not stop at symbol definitions. Also state the modeling function:

- describes uncertainty
- preserves temporal correlation
- quantifies seasonal fluctuation
- defines balance constraints
- reduces computational complexity
- supports later scenario analysis

## Figure Rules

### Function Split

Use figures for:

- background cognition
- research framework
- topology
- workflow
- dynamic process
- balance curve
- sensitivity analysis

### File Format Rule

Prefer inserting figures as PDF files.

Rationale:

- PDF is the default expected figure format for this thesis workflow
- vector PDF usually preserves line art, topology diagrams, and plotted curves better in LaTeX

If the available figure is not PDF, explicitly remind the user that the current skill expects PDF-form figure insertion.

### Caption Style

Keep captions noun-based, not conclusion-based.

Good patterns:

- `某系统拓扑结构`
- `某方法框架`
- `某结果对比分析`
- `某月平衡结果`
- `某灵敏度分析`

Do not put the final conclusion in the caption.

### In-Text Figure Interpretation

Use this pattern:

```text
图 x 展示了……。
由图可知，……。
相较于方案 A，方案 B ……。
```

### Review Rule For Figures

When reviewing figure usage:

1. check whether the inserted figure is PDF
2. if it is not PDF, explicitly flag it to the user
3. do not silently treat non-PDF insertion as fully compliant

## Table Rules

Use tables for:

1. scheme descriptions
2. parameter settings
3. structured result comparison
4. literature summary

Caption style is also noun-based:

- `对比方案描述`
- `关键参数设置`
- `不同方案的优化结果对比分析`

## Figure/Table Division of Labor

- tables carry structured numeric comparison
- figures carry trends, topology, process, and mechanism

Do not use a figure if a compact table expresses the result better.

## Citation Style

Prefer numeric references in engineering-thesis prose:

- `[1]`
- `[2]`
- `[9-10]`

Place citations directly after the technical claim they support.

## LaTeX Conventions

If writing LaTeX-compatible text, assume:

- single equations -> `equation`
- multiline equations -> `align`
- equation reference -> `\eqref{}`
- figures -> `figure`
- tables -> `table`
- labels:
  - `eq:...`
  - `fig:...`
  - `tab:...`
