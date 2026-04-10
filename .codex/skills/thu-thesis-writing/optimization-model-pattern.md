# Optimization-Planning Model Section Pattern

Use this when writing a technical subsection like `x.x 考虑……协同的……优化规划模型` inside the chapter's `主要内容` block.

This pattern is extracted from a strong thesis subsection whose internal motion is highly reusable:

1. one short opening paragraph to declare that the full coupled planning model is now assembled
2. one architecture or coupling figure to show what systems, resources, and links are inside the model
3. `目标函数`
4. `其他系统/前序模块运行约束`
5. `核心系统运行约束`
6. one short closing paragraph that states the final model is obtained by jointly enforcing the objective and all constraints, then names the solver type

This is a high-reuse thesis pattern because it does not try to explain every mechanism from zero. Instead, it performs model assembly:

- inherit component models from the previous subsection
- elevate them into a planning objective
- group constraints by subsystem
- finish by stating the complete optimization model

## What This Subsection Is Supposed To Do

The job of this subsection is not to repeat all earlier modeling details.

Its job is to answer four questions in order:

1. what full planning problem is being solved now
2. what the optimization objective minimizes or maximizes
3. how the already-defined subsystems are coupled into one constraint set
4. what complete mathematical program is finally formed

If these four questions are clear, the subsection usually feels complete.

## Recommended Skeleton

```text
x.x 考虑……协同的……优化规划模型
  opening paragraph
  coupling/framework figure
  x.x.1 目标函数
  x.x.2 [其他能源系统/前序模块/耦合链路]运行约束
  x.x.3 [电力系统/核心系统]运行约束
  closing paragraph
```

Typical title language:

- `考虑多类型储能协同的……优化规划模型`
- `考虑风险约束的……优化配置模型`
- `考虑多能耦合的……协同规划模型`
- `考虑源-网-荷-储协调的……扩展规划模型`

## Section-Level Writing Motion

### 1. Opening Paragraph

Keep this short, usually 1 to 3 sentences.

It should do only two things:

1. explicitly inherit the model foundation from the previous section
2. declare that a full coupled optimization planning model is now constructed

Template:

```text
基于上述构建的……模型，本文进一步建立了考虑……协同的……优化规划模型。
该模型综合考虑……、……与……之间的耦合关系，用于实现……的协同优化配置。
```

Do not start with a long background recap here. The subsection is already deep inside the technical chapter.

### 2. Coupling Figure

Insert one framework or coupling figure immediately after the opening paragraph when the model involves multiple systems, energy forms, or planning objects.

The figure should show:

- resource inputs
- main conversion devices
- network links
- storage units
- demand types

Caption style:

- `……耦合模型`
- `……协同规划框架`
- `……系统能量耦合关系`

In-text sentence:

```text
图 x 展示了……系统的耦合关系。
其中，……作为……，……通过……实现与……的关联。
```

The figure's function is to let the reader accept the model boundary before reading equations.

## Subsection 1: Objective Function

This part usually follows a three-step rhythm:

1. total objective
2. objective decomposition
3. explanation of each cost or benefit block

### Step A: Give the Top-Level Objective First

Start with one sentence and one compact top-level formula.

Template:

```text
如式（x.1）所示，目标函数以……为目标，综合考虑……与……。
min / max …
```

Common objective wording:

- `目标函数最小化年化投资成本和年运行成本`
- `目标函数以系统总成本最小为目标`
- `目标函数综合考虑建设成本、运行成本与弃能惩罚成本`

This first formula should stay abstract and aggregated. Do not pour all detailed sums into the first equation.

### Step B: Split the Objective Into Large Blocks

After the total objective, split it into 2 to 4 large terms.

Typical decomposition:

- investment cost
- operation cost
- maintenance cost
- penalty cost
- emission cost
- risk cost

This is where the source subsection is especially teachable:

it first writes `总目标 = 投资成本 + 运行成本`, then expands each block separately. That creates a clean reading ladder from coarse to fine.

Template:

```text
其中，……包括……和……。
式（x.2）-（x.4）分别给出了……、……与……的计算方法。
```

### Step C: Explain the Cost Blocks In Prose

After each decomposition formula, add 1 to 3 sentences to explain what that block contains.

Good explanation content:

- what assets are included
- which variables are existing capacity and which are expansion capacity
- whether a cost is annualized or initial
- what physical activity generates the operating cost

Template:

```text
式（x.2）给出了……，主要包括……。
其中，……通过……与……的乘积进行表征。
式（x.3）描述了……，反映了……阶段的……成本。
```

The key move is:

do not define every symbol in `式中：` only; also explain the engineering meaning of each cost block in normal prose.

### Detailed Objective Pattern To Mimic

If you are writing an optimization-planning subsection, imitate this order:

1. top-level total objective
2. annualization relationship if investment is annualized
3. investment block decomposition
4. operation block decomposition
5. prose explanation of what each block includes

This order is better than mixing all terms in one giant formula because the reader can follow the planning logic.

## Subsection 2: Other-System Or Previously Built Constraint Block

This block is for constraints that were already modeled earlier, such as:

- hydrogen system
- heat system
- gas system
- risk model
- seasonal storage model
- transportation model
- uncertainty scenario model

When these constraints were fully derived in the previous subsection, do not rewrite them in full unless needed. The strong pattern is:

1. give one heading for the subsystem
2. explicitly state that its constraints are given by earlier equations
3. use an equation-range reference to compress repetition

Template:

```text
……系统运行约束如式（x.a）-（x.b）所示。
（x.a）-（x.b） （x.c）
```

This move matters because it tells the reader:

- these equations still belong to the final optimization problem
- but their derivation has already been completed above

This is classic thesis writing for assembled models. It keeps the subsection concise and avoids restating the same derivation.

## Subsection 3: Core-System Constraint Block

This is usually the largest block. Its internal rhythm should be:

1. divide by physical module, not by random equation order
2. each module gets a numbered lead-in
3. each numbered item contains an equation group
4. each equation group is followed by a concise explanation sentence

### Preferred Grouping Order

For power-system planning, a very stable order is:

1. dispatchable generation constraints
2. renewable generation constraints
3. transmission constraints
4. network balance constraints
5. short-duration storage constraints

For another domain, keep the same logic:

1. controllable supply
2. uncertain supply
3. transport/network
4. nodal or system balance
5. buffer/storage

### How Each Numbered Constraint Item Should Read

Template:

```text
（1）……
式（x.5）-（x.8）构建了……约束。
式（x.5）描述……，式（x.6）设置……，式（x.7）刻画……，式（x.8）保证……。
```

Or, when the formulas are self-evident and already standard:

```text
式（x.5）-（x.8）描述了……的运行特性。
```

This is another important lesson from the source subsection:

after every constraint group, it adds one sentence saying what the group does. It does not leave the formulas hanging.

### What The Constraint Groups Usually Need To Cover

#### A. Controllable Generation

Typical contents:

- unit aggregation
- output limits
- ramping limits
- startup and shutdown logic
- minimum up/down time

Writing move:

first give the equation group, then summarize with a sentence like `描述……的运行特性`.

#### B. Renewable Generation

Typical contents:

- output upper bound tied to resource availability
- optional curtailment variables

Writing move:

one formula may be enough, but still follow it with a sentence saying it sets the renewable output range.

#### C. Transmission Or Transport Network

Typical contents:

- line flow limits
- transport capacity limits
- existing plus expansion capacity

Writing move:

after the formula, explain the modeling assumption briefly, such as the adopted flow model or the meaning of existing versus candidate capacity.

#### D. Nodal/System Balance

This is usually the conceptual core of the whole assembled model.

Typical contents:

- nodal balance
- conversion device consumption or output
- load shedding bounds
- policy constraints such as renewable penetration

Writing move:

state clearly that the conversion devices enter the balance equation as loads or injections. This is exactly the kind of sentence that prevents a multi-energy model from becoming unreadable.

#### E. Short-Duration Or Auxiliary Storage

Typical contents:

- inter-temporal SOC transition
- charge/discharge bounds
- energy bounds
- cycle-closing constraint

Writing move:

explain the physical meaning of each line in order: state transition, power limits, energy limits, cycle balance.

## Closing Paragraph

End the subsection by explicitly stating that the complete optimization model is obtained by jointly enforcing the objective and all constraints.

Template:

```text
通过联立式（x.1）-（x.n），构建了考虑……协同的……优化规划模型。
该模型属于……规划模型，可通过……求解器进行高效求解。
```

This closing sentence is not optional in this pattern.

It tells the reader three things:

1. the model assembly is finished
2. the mathematical-programming type is clear
3. the next section can move to case studies or algorithms without structural discontinuity

## Paragraph-Level Roles To Mimic

When summarizing a source subsection like this, look for these paragraph jobs:

1. inheritance paragraph:
   says the new model is based on earlier submodels
2. boundary paragraph/figure:
   clarifies what systems are inside the planning boundary
3. objective paragraph:
   gives the top-level optimization target
4. cost-decomposition paragraph:
   expands the objective into interpretable blocks
5. subsystem handoff paragraph:
   imports previously built constraints by reference
6. module constraint paragraphs:
   organize core constraints by physical module
7. solver paragraph:
   closes the full model and names the program type

If your draft contains all seven paragraph jobs, it will usually feel like a mature thesis subsection rather than raw notes.

## Sentence Templates

### Opening

```text
基于上述构建的……模型，本文进一步建立了考虑……协同的……优化规划模型。
```

### Objective Lead-In

```text
如式（x.1）所示，目标函数最小化……和……。
```

### Objective Decomposition

```text
其中，……包括……与……。
式（x.2）和式（x.3）分别给出了……与……的计算方法。
```

### Constraint Handoff

```text
……系统运行约束如式（x.a）-（x.b）所示。
```

### Constraint Group Explanation

```text
式（x.5）-（x.8）描述了……的运行特性。
```

### Network/Balance Explanation

```text
式（x.9）为……平衡约束，其中……作为……参与平衡。
```

### Closing

```text
通过联立式（x.1）-（x.n），构建了……优化规划模型。
该模型为……模型，可通过……求解器求解。
```

## Common Mistakes

Avoid these when writing an optimization-planning subsection:

1. repeating the full derivation of every subsystem instead of importing earlier equations by reference
2. starting directly with dense formulas without one opening sentence stating what full planning problem is being built
3. placing all cost items into one oversized objective formula with no layered decomposition
4. listing constraints in the order they were derived rather than regrouping them by subsystem or physical module
5. giving formulas without one-sentence explanations after each equation group
6. forgetting the final sentence that declares the complete model and solver type
7. explaining only symbols but not the engineering role of each cost block or constraint block

## Fast Self-Check

Before finalizing, verify:

- the subsection starts with `基于上述……模型`
- there is one coupling/framework figure if the system boundary is complex
- the objective is written from total to decomposition, not all at once
- reused subsystem constraints are imported by equation-range reference where appropriate
- core constraints are grouped by module and numbered
- every equation group has at least one interpretation sentence
- the subsection ends with `通过联立式……构建了……优化规划模型`
