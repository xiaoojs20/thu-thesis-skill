# 论文写作与审阅检查表

以下两种情况使用：

- before returning drafted chapter text
- when reviewing an existing thesis chapter or section

用于审阅时，每一项都要明确标记为：

- pass
- partial
- fail
- not applicable

## 结构

- Does the chapter follow one main problem line?
- Does the section order match the chapter type?
- Is there a chapter-level introduction or overview section near the beginning?
- Is there a chapter-level summary or `本章小结` near the end?
- If it is a technical chapter, does it contain:
  - `概述`
  - `主要内容`
  - `算例分析`
  - `本章小结`
- For a technical chapter, do these four blocks appear in the required order:
  - `概述`
  - `主要内容`
  - `算例分析`
  - `本章小结`
- If any one of the four blocks is missing, is the structure marked `fail` rather than `partial`?

## 节间衔接

- Does each major section connect logically to the previous section?
- Are there explicit transition sentences between background, model, experiment, and summary sections?
- Are `针对 / 首先 / 其次 / 基于此 / 最后` used where the logic needs structural guidance?
- Does the chapter avoid abrupt jumps from one topic to another without explanation?

## 引言

- Does it move from broad background to specific thesis problem?
- Are the subproblems explicit?
- Are the technical difficulties explicit?
- Is the literature review theme-based rather than author-by-author?

## 段落质量

- Does each paragraph do one main job?
- Are claims concrete rather than generic?

## 公式

- Is each equation introduced before appearing?
- If there is an equation group, is each equation’s role explained?
- Is there a `式中：` block when symbol density is high?
- Are key variables explained after the equation instead of being left implicit?
- Is the modeling meaning stated after the formula?

## 优化/规划模型小节

- If the section is a planning-model subsection, does it start with a short inheritance paragraph rather than repeating chapter background?
- Is there a coupling/framework figure when multiple systems, energy forms, or planning objects are involved?
- Does the subsection contain `x.x.1 目标函数`?
- Under `目标函数`, are `（1）（2）（3）` used to split different objective blocks such as investment cost and operating cost?
- Are Chinese-parenthetical sub-items such as `（1）投资成本` and `（2）运行成本` written in bold rather than plain text?
- Does every Chinese-parenthetical sub-item occupy its own line or paragraph, with the explanation starting from the next paragraph rather than the same line?
- Do the explanatory paragraphs under each Chinese-parenthetical sub-item keep first-line indentation instead of being flush left?
- Does each objective block include:
  - formula
  - physical meaning
  - key variable explanation
  - index explanation when notation is dense
- Does the subsection contain `x.x.2`, `x.x.3` style major constraint categories?
- Inside each major constraint category, are `（1）（2）（3）` used to split different physical modules?
- Are previously derived subsystem constraints imported by equation-range reference where appropriate instead of being fully rewritten?
- Are new constraints grouped first by big system category, then by physical module, rather than by arbitrary formula order?
- Does each constraint group have a follow-up sentence explaining what that group accomplishes?
- Does the subsection end by stating that the full optimization model is obtained by jointly enforcing the objective and all constraints?

## 图与表

- Are figure captions noun-based rather than conclusion-based?
- Are inserted figures in PDF format?
- If a figure is not PDF, is that explicitly called out to the user?
- Are tables used for parameters and structured comparisons?
- Are figure/table conclusions explained in the main text instead of the caption?
- Does the text explicitly say `由图可知` or `由表可知` when interpreting results?
- Does every important figure or table have an explicit textual reference and interpretation?

## Experiment Section

- Is the validation goal explicit?
- Are schemes and baselines defined?
- Are boundary conditions or parameters stated?
- Is the experiment section structurally complete:
  - case setting
  - scheme definition
  - parameter or boundary description
  - result comparison
  - interpretation
  - statement of what the experiment proves
- Does the result analysis explain why the difference appears?
- Does the section end with what the comparison proves?

## Abstract

- Does it avoid `第1章……第2章……` narration?
- Does each contribution follow `problem -> method -> effect`?
- Is the ending a true summary rather than repetition?

## Conclusion

- Does it reopen the thesis-level problem?
- Does the thesis-level conclusion avoid all section and subsection headings?
- Are the main contributions numbered cleanly?
- Is every numbered contribution lead sentence bold?
- Is every numbered contribution lead sentence an independent LaTeX paragraph, with the explanation starting in the next paragraph?
- Does each contribution follow `challenge -> method -> result -> value`?
- Are the numbered items rewritten from the full-thesis perspective rather than copied from chapter summaries?
- Does the ending state the overall implication of the thesis?
