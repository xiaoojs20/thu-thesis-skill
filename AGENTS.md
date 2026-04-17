# AGENTS.md

## Project Context

This repository contains thesis-writing analysis materials and a reusable Codex skill for Chinese engineering thesis drafting:

- source thesis analysis in `docs/`
- reusable skill in `.codex/skills/thu-thesis-writing/`

The repository is for thesis-writing support, not general software development. When the task is about thesis text, chapter organization, equation explanation, figure/table narration, or experiment-section writing, agents should treat this repository as a thesis-writing workspace.

The repository contains patterns extracted from one sample thesis, but agents must treat that sample only as a source of writing form. Do not transfer the sample thesis topic, terminology, case systems, or technical claims into a user's thesis unless the user is explicitly working on that same topic.

## Required Skill

For thesis writing tasks, agents must use the `thu-thesis-writing` skill:

- skill entry: `.codex/skills/thu-thesis-writing/SKILL.md`
- chapter templates: `.codex/skills/thu-thesis-writing/chapter-templates/`

Do not draft thesis chapters in an ad hoc style when this skill applies.

## When To Use The Skill

Use `thu-thesis-writing` whenever the task involves:

- writing or expanding thesis chapters
- outlining thesis sections
- rewriting thesis prose
- writing abstracts, introductions, methodology chapters, experiment sections, or conclusions
- reviewing thesis structure or rhetorical flow
- organizing experiment/case-study sections

## Guidance For Agents

### Writing Thesis Chapters

Before drafting, read the relevant skill files and template for the target chapter type.

Minimum guidance:

- use `thesis-structure.md` for chapter and section layout
- use `writing-patterns.md` for paragraph logic and thesis tone
- use `equation-rules.md` for equations, figures, tables, and citations
- use the matching file in `chapter-templates/` as the starting scaffold
- keep all topic nouns aligned to the user's own research subject; if the subject is unknown, stay generic rather than borrowing from the sample thesis

### Reviewing Thesis Sections

When reviewing thesis text, review against the skill rather than against generic writing preferences.

Check for:

- problem-driven structure
- clear section hierarchy
- explicit equation explanation with `式中：` where needed
- figure/table captions that stay descriptive rather than conclusion-heavy
- conclusion and chapter-summary sections that restate method and verified result
- no accidental borrowing of the sample thesis topic, systems, assumptions, or conclusions

Use `.codex/skills/thu-thesis-writing/checklist.md` for the final pass.

### Structuring Experiments

When writing or revising `算例分析` or experimental sections:

- use `.codex/skills/thu-thesis-writing/experiment-pattern.md`
- define validation goal, scheme settings, parameters, comparison results, interpretation, and what the experiment proves
- separate tables for schemes/parameters from figures for trends, topology, and dynamic behavior
- organize each `算例分析` section into at most five direct subsections: if the section is `x.y 算例分析`, arrange the content within `x.y.1` through `x.y.5` by merging related analyses or moving detail into lower paragraph levels

## Default Rule

If the user asks for thesis-related writing and no other style is explicitly requested, default to the `thu-thesis-writing` skill.
