# Writing Patterns

## Core Paragraph Logic

This file controls rhetoric and paragraph motion, not thesis subject matter. All nouns should be rewritten around the user's topic.

Default paragraph progression:

1. state the engineering background or phenomenon
2. state the contradiction, gap, or challenge
3. introduce what this chapter or thesis addresses
4. state the method, effect, or contribution

## Preferred Transition Language

Use these deliberately:

- `针对`
- `首先`
- `其次`
- `基于此`
- `最后`
- `由图可知`
- `由表可知`
- `通过上述对比分析`

Do not over-randomize wording if the text loses thesis discipline.

## Sentence Templates

### Method Introduction

```text
针对……问题，本文提出……方法。
首先，……。
其次，……。
基于此，……。
最后，通过……验证……。
```

### Result Interpretation

```text
如图 x 所示，……。
由图可知，……。
相较于方案 A，方案 B 在……方面……。
通过上述对比分析，证明了……。
```

### Background Setup

```text
随着……，研究对象/系统/场景面临……挑战。
一方面，……；另一方面，……。
因此，如何……成为……领域的重要问题。
```

## Introduction Style

Build the introduction in this sequence:

1. macro background
2. concrete system contradiction
3. enabling technology or possible response resource
4. core scientific problem
5. subproblem decomposition
6. technical difficulties
7. significance
8. literature review
9. research route and chapter arrangement

Hard rules:

1. Start broad, then narrow to the thesis problem.
2. Split the core problem into 2 to 4 subproblems.
3. For each subproblem, name 1 to 2 technical difficulties.
4. Review literature by topic, not by author order.
5. End with the thesis route and chapter tasks.

## Abstract Style

Use six moves:

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

## Conclusion Style

Use three layers:

1. opening paragraph:
   - restate the thesis background and overall route
2. numbered contributions:
   - each item should be `challenge -> method -> result -> value`
   - each item starts with a bold numbered lead sentence as an independent LaTeX paragraph
3. closing paragraph:
   - overall finding and broader value

Hard rules:

1. Do not create section headings or subsection headings in the thesis-level conclusion chapter.
2. Do not write `6.1`, `6.2`, `6.3` style structure.
3. Keep the conclusion as chapter-level prose plus numbered contribution items only.
4. The numbered lead sentence must be bold and must occupy an independent LaTeX paragraph.
5. Put a blank line after the numbered lead sentence; the explanatory text must start in the next paragraph.
6. Write the numbered lead sentence in LaTeX as `\textbf{（n）提出了……}`.
7. Do not copy chapter summaries directly; rewrite each item from the full-thesis perspective.

Suggested numbered paragraph template:

```text
\textbf{（n）提出了……}

针对……问题，本文……。
基于……，建立/构建……。
最后通过……验证了……。
```

## Chapter Summary Style

Each chapter summary should include:

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

## Tone Control

Write in a formal Chinese engineering style:

- concise
- analytical
- non-emotional
- result-oriented
- technically explicit

Avoid:

- rhetorical flourish
- journalistic tone
- exaggerated novelty claims without evidence
- vague praise words like `效果显著` without saying on what metric
- borrowing domain nouns from the source thesis when the user is writing about another topic
