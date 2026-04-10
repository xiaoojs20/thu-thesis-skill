# Optimization-Planning Model Section Pattern

Use this when the thesis contains a subsection such as:

- `x.x 考虑……协同的……优化规划模型`
- `x.x 考虑……的……优化配置模型`
- `x.x ……协同优化模型`
- `x.x ……扩展规划模型`

This file is not about general model-writing advice. It is about the specific thesis subsection pattern represented by sections like `4.4` in a planning/model chapter.

The key point is:

when the thesis reaches the full optimization/planning model, the writing should become strongly hierarchical and highly formula-structured.

The usual writing layer is:

1. `x.x` full planning-model subsection
2. `x.x.1` objective function
3. `x.x.2`, `x.x.3`, ... major constraint categories
4. inside each major category, use Chinese parenthetical items `（1）`, `（2）`, `（3）` to split the model by physical module
5. inside each `（1）` / `（2）` / `（3）`, write equation group + formula meaning + variable meaning if needed

If the user's thesis contains optimization/planning model writing, this pattern should be treated as the default.

## Plain-Language Summary

Write this kind of subsection in the following way:

first write one full planning-model subsection such as `4.4` or `x.x` to say that the previous models are now assembled into a complete optimization/planning model;
then split it into one `目标函数` subsection and several `……约束` subsections;
inside the `目标函数` subsection, use Chinese parenthetical items `（1）`, `（2）`, `（3）` to introduce each objective block in detail;
inside each `……约束` subsection, again use Chinese parenthetical items `（1）`, `（2）`, `（3）` to introduce each physical constraint block in detail.

The important thing is:

the writing should not stop at the formula itself.

For every objective block and every constraint block, the text should continue to explain:

- what the formula represents
- what engineering meaning it has
- what each important variable means
- what the important subscripts and superscripts mean

That is the real format being imitated here.

## What This Kind Of Subsection Must Achieve

This kind of subsection is not a casual model description.

It must do five things clearly:

1. declare that the previous submodels are now assembled into one optimization/planning problem
2. state the overall objective
3. decompose the objective into several interpretable sub-objectives or cost blocks
4. regroup all constraints into several major categories
5. further split each major category into Chinese-parenthetical physical submodules

In other words:

`大节标题 -> 小节标题 -> 中文括号分点 -> 公式组 -> 公式解释`

This is the real writing rhythm.

## The Strong Default Skeleton

```text
x.x 考虑……协同的……优化规划模型
  opening paragraph
  coupling/framework figure

  x.x.1 目标函数
    （1）……
    （2）……
    （3）……（可选）

  x.x.2 ……运行约束
    （1）……
    （2）……
    （3）……

  x.x.3 ……运行约束
    （1）……
    （2）……
    （3）……
    （4）……
    （5）……

  closing paragraph
```

Do not collapse this into one flat block.

Do not write:

- one giant objective formula with no Chinese-parenthetical decomposition
- one long list of constraints with no major-category split
- one long list of constraints with no `（1）（2）（3）` internal split

## Layer 1: How To Write `x.x` The Full Planning-Model Subsection

At the `x.x` layer, write only a short opening paragraph plus an optional framework figure.

This paragraph should do two jobs:

1. inherit previous modeling work
2. announce that a complete optimization/planning model is now built

Template:

```text
基于上述构建的……模型，本文进一步建立了考虑……协同的……优化规划模型。
该模型综合考虑……、……和……之间的耦合关系，以实现……的协同优化配置。
```

If the planning boundary is complex, insert one figure immediately after this paragraph.

The figure should clarify:

- which subsystems are included
- what the resource inputs are
- what the main conversion devices are
- what the storage units are
- what the network or transport links are
- what loads or demands are served

The function of this figure is not decoration. It prepares the reader to accept the later formulas.

## Layer 2: How To Write `x.x.1 目标函数`

This is where the writing must become very structured.

The correct pattern is:

1. first give one top-level total objective equation
2. then use Chinese parenthetical items `（1）`, `（2）`, `（3）` to expand each major objective block
3. inside each block, explain:
   - the formula
   - the physical meaning
   - the meaning of key variables
   - the meaning of important superscripts/subscripts when needed

This is one of the most important fixed patterns in optimization/planning model writing.

### 2.0 The Correct Feeling Of `目标函数`

`目标函数` in this kind of thesis should feel like a complete mini-section, not a single formula.

That means:

1. first one total objective equation
2. then `（1）`, `（2）`, `（3）` to split the objective
3. under each item, write enough prose so the reader understands the formula without guessing

If `目标函数` only has one formula and no decomposition, it usually looks underwritten.

### 2.1 Top-Level Total Objective

Before the Chinese-parenthetical items, write one aggregated objective equation.

Template:

```text
如式（x.1）所示，目标函数最小化……和……。
min …
```

Typical top-level expressions:

- `min 年化投资成本 + 年运行成本`
- `min 系统总成本`
- `min 建设成本 + 运行成本 + 弃能惩罚成本`

This top formula should stay aggregated.

Do not directly dump every detailed term into the first line.

The reason is simple:

the top equation tells the reader the optimization direction;
the later `（1）（2）（3）` items tell the reader how that direction is mathematically implemented.

### 2.2 Use Chinese Parenthetical Items Under `目标函数`

After the top-level objective, split it with:

- `（1）投资成本`
- `（2）运行成本`
- `（3）弃能/风险/碳排放/惩罚成本` if needed

This is not optional decoration. It is the standard way to make the objective legible.

In practice, the writing should read like:

```text
x.x.1 目标函数
如式（x.1）所示，目标函数最小化……和……。

（1）投资成本
……

（2）运行成本
……
```

This visual structure itself is part of the thesis style.

### 2.3 What Each `（1）` / `（2）` / `（3）` Must Contain

Each item should contain four pieces in order:

1. one lead-in sentence
2. one or several formulas
3. one paragraph explaining what this block physically represents
4. if variable density is high, a `式中：` sentence clarifying symbols, superscripts, and subscripts

The local rhythm should be:

```text
（1）投资成本
如式（x.2）所示，……
……
式（x.2）-（x.4）分别表示……、……和……。
式中：……。
其中，下标……表示……，上标……表示……。
```

This should be understood as a required degree of completeness.

In other words, for each item under `目标函数`, you should normally write:

1. the item name
2. the formula
3. what the formula means physically
4. what the important variables mean
5. what the important indices mean

If these five pieces are missing, the item is usually not complete enough.

### 2.4 What Must Be Explained In Objective Items

#### `（1）投资成本`

Normally explain:

- annualization relationship if used
- initial investment composition
- what assets are included
- which variables are existing capacity and which are expansion capacity

Typical decomposition:

- generation investment
- line/network investment
- storage power investment
- storage energy investment
- conversion-equipment investment

You should not stop at the formula.

You should say explicitly:

- which cost corresponds to which physical equipment
- how capacity variables map to the cost terms
- what the subscripts denote

#### `（2）运行成本`

Normally explain:

- what operational actions create the cost
- how different subsystems contribute to operating cost
- whether the cost is weighted by typical-day coefficients, scenario coefficients, or time-scale weights

Typical decomposition:

- thermal generation cost
- startup/shutdown cost
- transport cost
- storage operation cost
- fuel supply cost
- load shedding penalty

Again, the formula is not enough.

You must say what physical process each cost term represents.

#### `（3）Other Objective Terms`

Use this when the thesis includes:

- curtailment penalty
- carbon-emission cost
- risk cost
- reliability penalty
- renewable-integration penalty

The writing logic is the same:

`lead-in sentence -> formula -> physical meaning -> variable meaning`

### 2.5 On Variable Explanation In Objective Writing

Your point is exactly right:

the objective-function writing in this kind of thesis is usually very explicit about variables, especially when the notation is dense.

So in the skill, enforce this rule:

after each objective block, explain not only the formula meaning, but also the key variables and, when necessary, the meaning of important upper and lower indices.

Useful template:

```text
式中：……表示……；……表示……；……为……。
其中，下标 r、m、d、t 分别表示区域、月份、日期和时段；上标 Inv、Ope 分别表示投资成本和运行成本。
```

Do not assume the reader will infer index meaning automatically.

This is especially important when the objective contains multi-index variables such as region, month, day, time period, unit type, storage type, scenario, or line index.

When several indices appear together, explain them directly in the prose after the formula instead of leaving them implicit.

## Layer 3: How To Write `x.x.2`, `x.x.3` As Major Constraint Categories

After `目标函数`, the next level should usually be several major constraint categories.

This level should be written as titled subsubsections such as:

- `x.x.2 其他能源供应系统运行约束`
- `x.x.3 电力系统运行约束`
- `x.x.4 风险约束`

This layer is for big categories only.

Each `x.x.2` / `x.x.3` should represent one complete class of constraints.

Do not use this layer for tiny local details.

The reader should understand from the title alone what large subsystem is being constrained.

The visual effect should look like this:

```text
x.x.2 其他能源供应系统运行约束
x.x.3 电力系统运行约束
```

This layer is about large categories.

It should not yet drop to the level of specific devices.

## Layer 4: How To Write Constraints Inside Each Major Category

Inside each constraint category, use Chinese parenthetical items:

- `（1）火电机组快速机组组合约束`
- `（2）可再生能源运行约束`
- `（3）输电线路运行约束`
- `（4）电力网络约束`
- `（5）电化学储能运行约束`

This is the standard pattern.

The principle is:

major titles classify by system;
Chinese-parenthetical items classify by physical module inside that system.

This is how a real planning model becomes readable.

This means the constraint writing has two nested levels:

1. large-system level:
   `x.x.2`, `x.x.3`
2. physical-module level:
   `（1）`, `（2）`, `（3）`

The first level answers `which system is being constrained`;
the second level answers `which module inside that system is being constrained`.

## The Standard Writing Unit For Each Constraint Item

Each `（1）` / `（2）` / `（3）` should normally follow this local structure:

1. item title
2. equation or equation group
3. one paragraph explaining what the equations do
4. if needed, one `式中：` sentence for variables and indices

Template:

```text
（1）……
……
式（x.10）-（x.14）构建了……约束。式（x.10）描述……，式（x.11）设置……，式（x.12）刻画……，式（x.13）保证……，式（x.14）给出……。
式中：……。
```

If the formula group is standard and does not require line-by-line explanation, the compressed version can be:

```text
式（x.10）-（x.14）描述了……的运行特性。
```

But even in the compressed version, the equation group must be followed by a sentence of meaning.

Do not leave the formulas hanging.

This is the most common failure in weak drafts:

they place several formulas under `（1）火电机组约束` and then immediately move on.

The stronger thesis style always adds one explanatory sentence after the formula group.

## How To Write Different Types Of Constraint Items

### `（1）` Controllable Unit Constraints

Typical examples:

- thermal-unit commitment constraints
- conventional generator output constraints
- startup and shutdown constraints
- ramping constraints
- minimum up/down time constraints

What to explain:

- what physical device is controlled
- whether the equations reflect output limits, dynamic limits, or on/off logic
- what the binary or state variables mean

Typical sentence:

```text
式（x.10）-（x.15）基于……约束集，描述了……的运行特性。
```

If necessary, continue with one more sentence clarifying state variables, startup variables, or capacity variables.

### `（2）` Renewable-Energy Constraints

Typical examples:

- wind output limits
- PV output limits
- curtailment bounds

What to explain:

- the resource-dependent upper bound
- whether the installed capacity and resource availability appear separately
- whether curtailment is allowed

Typical sentence:

```text
式（x.16）设置了……机组的出力上下限。
```

If curtailment variables are involved, explain whether the available output, dispatched output, and curtailed output are distinguished.

### `（3）` Network Or Transport Constraints

Typical examples:

- transmission-line limits
- pipeline or channel transport limits
- interregional transport limits

What to explain:

- what network model is used
- whether existing capacity and expansion capacity are both included
- how candidate-line investment is represented

Typical sentence:

```text
式（x.17）建立了……的容量上下限约束，其中……和……分别表示已建容量与待建容量。
```

If the network has an assumed flow model, state it briefly after the equation.

### `（4）` System-Balance Constraints

Typical examples:

- nodal power balance
- energy balance
- supply-demand balance
- renewable-penetration constraints
- load-shedding bounds

This is often the conceptual core of the whole model.

What to explain:

- what enters the left-hand side
- what enters the right-hand side
- which conversion devices are modeled as loads or injections
- what policy indicator or planning requirement is enforced

Typical sentence:

```text
式（x.18）为……平衡约束，其中……作为……参与平衡。式（x.19）设置了……上下限。式（x.20）给出了……约束。
```

This kind of sentence is very important in multi-energy models because it tells the reader how cross-system coupling enters the balance relation.

### `（5）` Storage Constraints

Typical examples:

- SOC state transition
- charge/discharge power bounds
- energy-capacity bounds
- cycle-closing constraints
- long-duration storage coupling constraints

What to explain:

- the inter-temporal transition relationship
- the power-capacity and energy-capacity meanings
- whether the storage is day-level or month-level
- whether cycle balance or annual balance is imposed

Typical sentence:

```text
式（x.21）-（x.24）构建了……储能模型。式（x.21）表示……，式（x.22）和式（x.23）分别表示……，式（x.24）表示……。
```

If the thesis contains both short-duration storage and seasonal storage, explicitly distinguish which block belongs to which time scale.

## The Most Important Rule: Distinguish Two Different Uses Of `（1）（2）（3）`

This pattern uses Chinese-parenthetical items in two different ways:

### Use A: under `x.x.1 目标函数`

Here `（1）（2）（3）` means:

- different objective blocks
- different cost-function parts
- different terms inside the objective

Example:

- `（1）投资成本`
- `（2）运行成本`
- `（3）风险成本`

### Use B: under `x.x.2`, `x.x.3` constraints

Here `（1）（2）（3）` means:

- different physical modules inside one major constraint class
- different device/network/balance blocks

Example:

- `（1）火电机组快速机组组合约束`
- `（2）可再生能源运行约束`
- `（3）输电线路运行约束`

Do not mix these two uses.

This distinction should be explicit in the skill.

This is one of the most important format rules:

- under `目标函数`, `（1）（2）（3）` means objective decomposition
- under `……运行约束`, `（1）（2）（3）` means constraint-module decomposition

The same symbol form is used twice, but its structural job is different.

## The Closing Paragraph

At the end of the whole `x.x` subsection, add one short closing paragraph.

This paragraph should state:

1. which equations together form the final planning model
2. what type of optimization model it is
3. what solver or solution method can be used

Template:

```text
通过联立式（x.1）-（x.n），构建了考虑……的……优化规划模型。
该模型为……规划模型，可通过……求解器实现高效求解。
```

This sentence is structurally important.

Without it, the subsection often feels unfinished.

It gives the reader a clear sense that:

the objective has been written,
the constraints have been fully assembled,
and the mathematical model is now closed.

## A More Concrete Reusable Skeleton

```text
x.x 考虑……协同的……优化规划模型
基于上述构建的……模型，本文进一步建立了考虑……协同的……优化规划模型。
图 x 展示了……系统的耦合关系。

x.x.1 目标函数
如式（x.1）所示，目标函数最小化……和……。

（1）投资成本
如式（x.2）-（x.4）所示，……
式（x.2）表示……，式（x.3）表示……，式（x.4）表示……。
式中：……。
其中，下标……表示……，上标……表示……。

（2）运行成本
如式（x.5）-（x.6）所示，……
式（x.5）表示……，式（x.6）表示……。
式中：……。

x.x.2 其他系统运行约束
……系统运行约束构建如式（x.7）-（x.12）所示。

x.x.3 核心系统运行约束
（1）……
……
式（x.13）-（x.18）描述了……的运行特性。

（2）……
……
式（x.19）设置了……上下限。

（3）……
……
式（x.20）建立了……约束。

（4）……
……
式（x.21）为……平衡约束，其中……作为……参与平衡。

（5）……
……
式（x.22）-（x.25）构建了……模型。

通过联立式（x.1）-（x.25），构建了……优化规划模型。
该模型为……模型，可通过……求解。
```

## A More Detailed Natural-Language Writing Guide

If you were to explain the format in plain Chinese, it should read roughly like this:

first, write a subsection like `x.x 考虑……的……优化规划模型`, and use one short paragraph to say that based on the previous model, a complete optimization/planning model is now established.
Then, if needed, place a framework figure to show the coupling relationship.

After that, write `x.x.1 目标函数`.
Inside `x.x.1`, do not write only one total formula and stop.
You should first give the total objective, and then use `（1）投资成本`, `（2）运行成本`, `（3）其他成本` to explain each objective term separately.
For each item, you should explain the formula itself, what physical meaning it has, what each important variable means, and what important subscripts/superscripts mean.

Then continue with `x.x.2` and `x.x.3` style constraint subsections.
Each of these should represent one large class of constraints, such as another energy system, the core power system, or a risk module.
Inside each large class, use `（1）`, `（2）`, `（3）` to continue splitting by physical module.
For example, one item may be thermal-unit constraints, another may be renewable-energy constraints, another may be network constraints, and another may be storage constraints.

For each such item, write the formula group first, and then immediately explain what those formulas mean.
If the notation is dense, continue with `式中：` and explain variables and indices.

Finally, at the end of the full subsection, add one sentence saying that by jointly enforcing the objective and all constraints, the full optimization/planning model is obtained, and mention what type of solver can be used.

## Hard Rules

1. If the thesis is writing a planning-model subsection, keep the layer `x.x -> x.x.1/x.x.2/x.x.3 -> （1）（2）（3） -> equation group -> meaning explanation`.
2. Under `目标函数`, use Chinese-parenthetical items to split major objective blocks.
3. Under each major constraint subsection, use Chinese-parenthetical items to split physical modules.
4. Each objective block must explain formula meaning and key variable meaning.
5. Each constraint item must be followed by at least one sentence explaining what the equation group does.
6. When notation is dense, explain the meaning of important indices, not just the main variable names.
7. Major constraint subsections must classify by big system category, not by tiny local details.
8. Do not merge objective writing and constraint writing into one continuous flat section.
9. End the subsection with a sentence declaring the final model and its solution type.

## Common Mistakes

Avoid these:

1. writing `x.x.1 目标函数` without `（1）投资成本` / `（2）运行成本` style decomposition
2. writing a full objective with no Chinese-parenthetical expansion
3. writing `x.x.2` or `x.x.3` as a flat list of formulas without `（1）（2）（3）`
4. failing to explain what variables or indices mean after a dense formula
5. mixing subsystem-level headings and Chinese-parenthetical module headings
6. putting all constraints into one subsection instead of separating them into `x.x.2`, `x.x.3`, ...
7. ending the subsection without a final sentence that closes the model

## Fast Self-Check

Before finalizing, verify:

- does the subsection have `x.x.1 目标函数`?
- under `目标函数`, are there `（1）（2）（3）` items for different objective blocks?
- does each objective item include formula + physical meaning + variable explanation?
- does the subsection have `x.x.2`, `x.x.3` style major constraint categories?
- inside each major constraint category, are there `（1）（2）（3）` items for physical modules?
- does each constraint item have formula meaning after the equations?
- does the subsection end with `通过联立式……构建了……优化规划模型`?
