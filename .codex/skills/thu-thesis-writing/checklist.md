# Thesis Writing and Review Checklist

Use this either:

- before returning drafted chapter text
- when reviewing an existing thesis chapter or section

When used for review, explicitly mark each check as:

- pass
- partial
- fail
- not applicable

## Structure

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

## Section Transitions

- Does each major section connect logically to the previous section?
- Are there explicit transition sentences between background, model, experiment, and summary sections?
- Are `针对 / 首先 / 其次 / 基于此 / 最后` used where the logic needs structural guidance?
- Does the chapter avoid abrupt jumps from one topic to another without explanation?

## Introduction

- Does it move from broad background to specific thesis problem?
- Are the subproblems explicit?
- Are the technical difficulties explicit?
- Is the literature review theme-based rather than author-by-author?

## Paragraph Quality

- Does each paragraph do one main job?
- Are claims concrete rather than generic?

## Equations

- Is each equation introduced before appearing?
- If there is an equation group, is each equation’s role explained?
- Is there a `式中：` block when symbol density is high?
- Are key variables explained after the equation instead of being left implicit?
- Is the modeling meaning stated after the formula?

## Optimization-Planning Subsection

- If the section is a planning-model subsection, does it start with a short inheritance paragraph rather than repeating chapter background?
- Is there a coupling/framework figure when multiple systems, energy forms, or planning objects are involved?
- Is the objective written in layers:
  - total objective
  - cost or benefit decomposition
  - prose explanation of each block
- Are previously derived subsystem constraints imported by equation-range reference where appropriate instead of being fully rewritten?
- Are new constraints grouped by physical module or subsystem rather than by arbitrary formula order?
- Does each constraint group have a follow-up sentence explaining what that group accomplishes?
- Does the subsection end by stating that the full optimization model is obtained by jointly enforcing the objective and all constraints?

## Figures and Tables

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
- Does each contribution follow `challenge -> method -> result -> value`?
- Does the ending state the overall implication of the thesis?
