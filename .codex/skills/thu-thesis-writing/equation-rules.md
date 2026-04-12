# 公式、图与表规则

## 公式解释顺序

公式解释优先按以下固定顺序：

1. explain why the equation is needed
2. show the equation or equation group
3. explain the role of each equation if there are multiple equations
4. add `式中：` to define symbols
5. state what the equation block accomplishes in the thesis

## 公式组模板

```text
……如式（x.1）-（x.4）所示。
\begin{align}
  [公式内容]
\label{eq:block}
\end{align}

式（x.1）描述……，式（x.2）构建……，式（x.3）计算……，式（x.4）给出……。
式中：A 表示……；B 表示……；C 为……。
基于式（x.1）-（x.4）构建的……，实现了……。
```

## LaTeX 公式环境空行规则

这是强约束，不是建议：

1. `\begin{equation}`、`\begin{align}` 这类陈列公式环境前不需要额外空行；公式环境应紧接引导句下一行。
2. `\end{equation}`、`\end{align}` 后必须再空一行。
3. 公式块后的解释句必须从新段落开始，不能紧贴在 `\end{...}` 下一行直接顶格续写。
4. 单个公式和公式组都必须遵守这条规则。

正确示例：

```text
……可构建目标函数如下：
\begin{equation}
  [公式内容]
\label{eq:obj}
\end{equation}

式（\ref{eq:obj}）为……
```

错误示例：

```text
……可构建目标函数如下：

\begin{equation}
  [公式内容]
\label{eq:obj}
\end{equation}
式（\ref{eq:obj}）为……
```

## `式中：` 规则

1. Start with `式中：`.
2. Follow variable appearance order.
3. Use `；` to separate items.
4. Explain physical meaning first, then role, range, or bound.

Template:

```text
式中：X 表示……；Y 表示……；Z 为……，其上限为……。
```

## 公式后还需要解释什么

不要只停留在符号定义，还要说明该公式块的建模作用：

- describes uncertainty
- preserves temporal correlation
- quantifies seasonal fluctuation
- defines balance constraints
- reduces computational complexity
- supports later scenario analysis

## 图的规则

### 图的职责

图更适合承载：

- background cognition
- research framework
- topology
- workflow
- dynamic process
- balance curve
- sensitivity analysis

### 文件格式规则

插图优先使用 PDF。

原因：

- PDF is the default expected figure format for this thesis workflow
- vector PDF usually preserves line art, topology diagrams, and plotted curves better in LaTeX

如果现有图不是 PDF，要明确提醒用户本 skill 默认按 PDF 图插入。

### 图题写法

Keep captions noun-based, not conclusion-based.

较好的题注模式：

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

在 ThuThesis 模板中，引用样式需要显式区分 `inline` 和 `super`，并在需要切换时显式调用：

```tex
\thusetup{
  cite-style = inline, % inline super[上标引用]
}
```

强约束如下：

1. 如果 `\cite{...}` 前面有显式的 `文献`、`参考文献` 等字样，使用 `inline` 样式。
2. 如果引用只是给前面的判断、论述或事实陈述加上标参考文献，使用 `super` 样式。
3. 每次到某一处需要和当前样式不同的引用格式时，都要显式写一次 `\thusetup{ cite-style = inline }` 或 `\thusetup{ cite-style = super }`，不要默认沿用。

`inline` 示例：

```tex
\thusetup{ cite-style = inline }
文献\cite{ref1,ref2}针对该问题开展了研究。
```

`super` 示例：

```tex
\thusetup{ cite-style = super }
该方法能够显著降低系统运行成本。\cite{ref3}
```

## LaTeX Conventions

If writing LaTeX-compatible text, assume:

- single equations -> `equation`
- multiline equations -> `align`
- equation reference -> `\eqref{}`
- citations preceded by explicit `文献` wording -> switch to `\thusetup{ cite-style = inline }`
- citations used as superscript support for a statement -> switch to `\thusetup{ cite-style = super }`
- when the local citation style needs to change, explicitly call `\thusetup{ cite-style = ... }`
- do not insert an extra blank line before `\begin{equation}` / `\begin{align}`
- leave one blank line after `\end{equation}` / `\end{align}`
- figures -> `figure`
- tables -> `table`
- labels:
  - `eq:...`
  - `fig:...`
  - `tab:...`
