---
name: "thu-thesis-writing"
description: "Use when writing, outlining, revising, reviewing, or expanding a Chinese engineering thesis, dissertation chapter, abstract, introduction, methodology chapter, experiment section, or conclusion in the structured Tsinghua-style academic pattern: problem-driven introduction, chapter-by-chapter method progression, explicit equation explanations, disciplined figure/table usage, formal experiment analysis, and chapter-level thesis review."
---

# 清华风格工科论文写作

当用户希望论文文本遵循从高质量清华风格工科博士论文中提炼出的结构与语气时，使用本 skill。

本 skill 明确以“写作形式优先”，而不是“样本主题优先”：

- 学习章节组织、段落逻辑、公式叙述、图表规范和实验章节骨架
- 不要继承样本论文的研究主题、领域假设、系统名称、数据集、变量或结论
- 不要把电力系统、能源系统、规划、储能、风险等样本主题词强行带入其他论文

## 本 Skill 强制保持的写法

1. Problem-driven thesis structure rather than article stitching.
2. Strong technical-chapter backbone: `概述 -> 主要内容 -> 算例分析 -> 本章小结`.
3. Formal Chinese engineering-academic prose.
4. Explicit equation explanation style with `式中：`.
5. Clear figure/table division of labor.
6. Reusable experiment-section patterns.
7. Strong introduction and conclusion scaffolding.
8. Chapter-review checks for structural completeness and local logic.
9. Theme isolation: extract writing form, not subject matter.

## 适用场景

Use this skill for:

- Thesis chapter drafting
- Chapter outlining
- Thesis section rewriting
- Thesis chapter review
- Thesis section review
- Abstract writing
- Introduction writing
- Methodology/model chapter writing
- Experiment/case-study section writing
- Conclusion writing
- Converting rough notes into thesis prose

如果目标论文包含优化/规划模型小节，应将 `optimization-model-pattern.md` 视为默认写法，而不是可选参考。

Do not use it for:

- Journal papers with very different target styles
- Informal reports
- Slide decks
- Code or implementation documentation

## 使用流程

1. 先识别目标产出类型：
   - abstract
   - introduction
   - methodology/model chapter
   - experiment section
   - conclusion
   - full chapter outline
   - chapter review
   - section review
2. 先判断论文层次：
   - 硕士论文：结论章通常是第 5 章
   - 博士论文：结论章通常是第 6 章
   - 如果学位层次未知，不要提前写死结论章编号
3. 只读取与当前任务相关的文件：
   - 总体结构 -> `thesis-structure.md`
   - 行文逻辑与语气 -> `writing-patterns.md`
   - 公式、图、表 -> `equation-rules.md`
   - 算例/实验章节 -> `experiment-pattern.md`
   - 优化规划模型小节 -> `optimization-model-pattern.md`
   - LaTeX 编译与清理命令 -> `latex-build-commands.md`
   - 最终自查 -> `checklist.md`
   - 现成模板骨架 -> `chapter-templates/*.md`
4. 如果是起草任务，先列提纲，再写正文。
5. 对技术章节，强制保持以下四段骨架顺序：
   - `概述`
   - `主要内容`
   - `算例分析`
   - `本章小结`
6. 将 `主要内容` 视为章节主体，可展开为定义、模型、约束、框架、算法等多个连续小节，但必须位于 `概述` 与 `算例分析` 之间。
7. 全文默认按“问题 -> 方法 -> 结果”的顺序起草。
8. 如果论文中出现 `考虑……协同的……优化规划模型`、`……优化配置模型` 等“模型总装段”，先读 `optimization-model-pattern.md`，并默认采用该写法。
9. 对论文层面的 `结论` 章，不要再设节或小节；无论结论是第 5 章还是第 6 章，都应写成“章节标题 + 连续段落 + 编号贡献项”。
10. 公式默认按“先说明用途 -> 再给公式 -> 再给 `式中：` -> 再说明建模含义”的顺序解释。
11. 图表标题默认使用名词性表述，核心结论放在正文中说明。
12. LaTeX 工程中的图优先使用 PDF；如果图不是 PDF，要明确提醒用户。
13. 每章技术章节结尾都要有 `本章小结`，并重述：
   - the challenge
   - the method chain
   - what the case study verified
14. 如果是审阅任务，使用 `checklist.md` 作为检查表，并明确指出：
   - missing chapter introduction
   - missing chapter summary
   - missing variable explanations after equations
   - missing or weak figure/table references
   - incomplete experiment structure
   - weak transitions between sections
15. 输出前务必再跑一遍 checklist。

## 主题隔离规则

本 skill 背后的来源材料来自某一篇具体样本论文，但该样本只用于提炼写作形式。

使用本 skill 时：

1. Reuse structure, not the sample thesis topic.
2. Reuse rhetoric, not the sample thesis terminology.
3. Reuse chapter logic, not the sample thesis chapter subjects.
4. Reuse experiment organization, not the sample thesis test systems.
5. If the user's thesis topic differs, rewrite every placeholder around the user's actual research object rather than around the sample thesis object.
6. If the user's topic is unknown, keep placeholders generic and do not invent a domain.

## 文件索引

- `thesis-structure.md`
  Use when deciding chapter order, section layering, and chapter length balance.

- `writing-patterns.md`
  Use when drafting paragraphs, introductions, abstracts, conclusions, and chapter summaries.

- `equation-rules.md`
  Use when writing model sections, variable definitions, figures, tables, or citations.

- `experiment-pattern.md`
  Use when writing case studies, result analysis, sensitivity analysis, or scheme comparison.

- `optimization-model-pattern.md`
  Use when writing a subsection such as `考虑……协同的……优化规划模型`, especially for objective-function plus grouped-constraint assembly.

- `latex-build-commands.md`
  Use when the user asks how to compile, clean, rebuild, or troubleshoot a ThuThesis LaTeX project.

- `checklist.md`
  Use as the last pass before returning draft text, or as the main rubric when reviewing an existing thesis chapter.

- `chapter-templates/introduction.md`
  Use for Chapter 1 or standalone introduction sections.

- `chapter-templates/methodology.md`
  Use for model, method, or planning chapters.

- `chapter-templates/experiment.md`
  Use for `算例分析` or experimental validation sections.

- `chapter-templates/conclusion.md`
  Use for chapter conclusions or full-thesis conclusions.

## 硬规则

1. Keep one main problem line through the chapter.
2. Do not write thesis text as a list of disconnected papers.
3. Prefer theme-based literature review, not author-by-author listing.
4. Use transition phrases deliberately: `针对`, `首先`, `其次`, `基于此`, `最后`.
5. Every technical chapter must contain `概述 + 主要内容 + 算例分析 + 本章小结` in that order.
6. `主要内容` can be split into multiple consecutive sections, but those sections collectively serve one block: the chapter's main method/model content.
7. If one of the four blocks is missing, do not treat the chapter as structurally complete.
8. Do not put full conclusions into figure captions or table titles.
9. Do not drop equations without explaining what each block does.
10. Do not end experiment sections with raw observations only; state what the comparison proves.
11. Figures should be inserted in PDF format by default.
12. If a proposed or existing figure is not in PDF format, explicitly remind the user rather than silently accepting it.
13. The thesis-level `结论` chapter must not set section or subsection headings, whether it is Chapter 5 or Chapter 6.
14. The thesis-level `结论` chapter should be organized as opening summary paragraph -> numbered contributions -> closing paragraph.
15. Each numbered contribution item in the thesis-level conclusion must use a bold numbered lead sentence as an independent LaTeX paragraph, then continue the explanation in the next paragraph.
16. Write the lead sentence in LaTeX as `\textbf{（n）提出了……}`.
17. Each thesis-level conclusion contribution must follow `challenge -> method -> result/verification -> value`, and must not be a pasted chapter summary.
18. Do not write the abstract as `第1章...第2章...`.
19. When reviewing, judge the chapter against thesis structure and local transitions, not against generic prose preferences.
20. Never import domain-specific nouns from the source thesis unless the user explicitly asks for that exact topic.
21. For optimization-planning subsections, enforce the layer `x.x -> x.x.1/x.x.2/x.x.3 -> （1）（2）（3） -> equation group -> explanation`.
22. Under `目标函数`, use Chinese-parenthetical items such as `（1）投资成本`, `（2）运行成本` to split objective blocks.
23. Under each major constraint subsection, use Chinese-parenthetical items such as `（1）火电机组……约束`, `（2）可再生能源……约束` to split physical modules.
24. Every Chinese-parenthetical sub-item under optimization/planning writing must be written as a bold standalone lead, such as `\textbf{（1）投资成本}` or `\textbf{（2）电力平衡约束}`.
25. After each bold Chinese-parenthetical lead, start the explanation in the next paragraph rather than on the same line; do not write the explanation flush against the lead sentence.
26. The explanatory paragraph after each sub-item must keep first-line indentation, and every subsequent explanatory paragraph under the same sub-item must also keep first-line indentation rather than being flush left.
27. For optimization-planning objectives, explain not only the formula but also the physical meaning of each block and the meaning of key variables, superscripts, and subscripts when needed.
28. For optimization-planning constraints, regroup by big system category at the `x.x.2/x.x.3` layer and by physical module at the `（1）（2）（3）` layer.
29. If the user's thesis includes optimization/planning model writing, default to this pattern unless the user explicitly asks for a different structure.
30. When writing LaTeX displayed equations, do not insert an extra blank line above `\begin{equation}` / `\begin{align}`; the equation environment should follow directly after the lead-in sentence.
31. Always leave one blank line after `\end{equation}` / `\end{align}`; the narration after the equation block must start as a new paragraph and must not begin immediately on the next line.
32. When writing LaTeX citations, explicitly distinguish `inline` and `super` cite styles according to the local sentence pattern.
33. If the citation is preceded by explicit wording such as `文献` or `参考文献`, switch to inline citation style before that citation with `\thusetup{ cite-style = inline }`.
34. If the citation serves as a superscript reference for a statement or clause rather than following explicit wording such as `文献`, switch to superscript citation style before that citation with `\thusetup{ cite-style = super }`.
35. Whenever the required citation style at a location differs from the current local setting, explicitly call `\thusetup{ cite-style = ... }`; do not assume the correct style is already active.

## 输出标准

好的输出应当读起来像规范的工科论文章节：

- clear problem framing
- stable section hierarchy
- dense but controlled technical prose
- explicit equation and notation handling
- disciplined figure/table references
- result interpretation tied back to the thesis objective
