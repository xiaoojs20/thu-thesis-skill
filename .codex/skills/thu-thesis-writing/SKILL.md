---
name: "thu-thesis-writing"
description: "Use when writing, outlining, revising, reviewing, or expanding a Chinese engineering thesis, dissertation chapter, abstract, introduction, methodology chapter, experiment section, or conclusion in the structured Tsinghua-style academic pattern: problem-driven introduction, chapter-by-chapter method progression, explicit equation explanations, disciplined figure/table usage, formal experiment analysis, and chapter-level thesis review."
---

# THU Thesis Writing

Use this skill when the user wants thesis text that should follow the structure and tone extracted from a high-quality Tsinghua-style engineering PhD thesis.

This skill is intentionally format-first and topic-agnostic:

- learn chapter organization, paragraph logic, equation narration, figure/table discipline, and experiment scaffolding
- do not inherit the source thesis topic, domain assumptions, system names, datasets, variables, or conclusions
- do not force power systems, energy systems, planning, storage, risk, or any other sample-theme vocabulary onto a different thesis

## What This Skill Enforces

1. Problem-driven thesis structure rather than article stitching.
2. Strong technical-chapter backbone: `概述 -> 主要内容 -> 算例分析 -> 本章小结`.
3. Formal Chinese engineering-academic prose.
4. Explicit equation explanation style with `式中：`.
5. Clear figure/table division of labor.
6. Reusable experiment-section patterns.
7. Strong introduction and conclusion scaffolding.
8. Chapter-review checks for structural completeness and local logic.
9. Theme isolation: extract writing form, not subject matter.

## When To Use

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

Do not use it for:

- Journal papers with very different target styles
- Informal reports
- Slide decks
- Code or implementation documentation

## Workflow

1. Identify the target deliverable:
   - abstract
   - introduction
   - methodology/model chapter
   - experiment section
   - conclusion
   - full chapter outline
   - chapter review
   - section review
2. Read only the relevant files:
   - overall structure -> `thesis-structure.md`
   - prose and rhetoric -> `writing-patterns.md`
   - equations, figures, tables -> `equation-rules.md`
   - experiment section -> `experiment-pattern.md`
   - LaTeX build and cleanup commands -> `latex-build-commands.md`
   - final self-check -> `checklist.md`
   - ready-made scaffold -> `chapter-templates/*.md`
3. If drafting, build the outline before drafting paragraphs.
4. For technical chapters, enforce the four-part backbone in this order:
   - `概述`
   - `主要内容`
   - `算例分析`
   - `本章小结`
5. Treat `主要内容` as the chapter body, which may expand into multiple sections such as definitions, models, constraints, frameworks, or algorithms, but it must stay between `概述` and `算例分析`.
6. Draft in a problem-to-method-to-result sequence.
7. For the thesis-level `结论` chapter, do not create section or subsection headings; write it as chapter title plus continuous paragraphs with numbered contribution items.
8. For equations, explain purpose first, then formula, then `式中：`, then modeling meaning.
9. For figures/tables, make the caption noun-based and keep conclusions in the main text.
10. Prefer inserting figures as PDF files in the LaTeX project; if a figure is not in PDF format, explicitly remind the user.
11. End each technical chapter with a chapter summary that restates:
   - the challenge
   - the method chain
   - what the case study verified
12. If reviewing, use `checklist.md` as a chapter-review rubric and explicitly report:
   - missing chapter introduction
   - missing chapter summary
   - missing variable explanations after equations
   - missing or weak figure/table references
   - incomplete experiment structure
   - weak transitions between sections
13. Run the checklist before finalizing.

## Theme-Isolation Rule

The source materials behind this skill come from one specific thesis sample, but that sample is only evidence for writing form.

When using this skill:

1. Reuse structure, not the sample thesis topic.
2. Reuse rhetoric, not the sample thesis terminology.
3. Reuse chapter logic, not the sample thesis chapter subjects.
4. Reuse experiment organization, not the sample thesis test systems.
5. If the user's thesis topic differs, rewrite every placeholder around the user's actual research object rather than around the sample thesis object.
6. If the user's topic is unknown, keep placeholders generic and do not invent a domain.

## Reference Map

- `thesis-structure.md`
  Use when deciding chapter order, section layering, and chapter length balance.

- `writing-patterns.md`
  Use when drafting paragraphs, introductions, abstracts, conclusions, and chapter summaries.

- `equation-rules.md`
  Use when writing model sections, variable definitions, figures, tables, or citations.

- `experiment-pattern.md`
  Use when writing case studies, result analysis, sensitivity analysis, or scheme comparison.

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

## Hard Rules

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
13. The thesis-level `结论` chapter must not set section or subsection headings.
14. The thesis-level `结论` chapter should be organized as opening summary paragraph -> numbered contributions -> closing paragraph.
15. Do not write the abstract as `第1章...第2章...`.
16. When reviewing, judge the chapter against thesis structure and local transitions, not against generic prose preferences.
17. Never import domain-specific nouns from the source thesis unless the user explicitly asks for that exact topic.

## Output Standard

A good output from this skill should read like a formal engineering thesis chapter:

- clear problem framing
- stable section hierarchy
- dense but controlled technical prose
- explicit equation and notation handling
- disciplined figure/table references
- result interpretation tied back to the thesis objective
