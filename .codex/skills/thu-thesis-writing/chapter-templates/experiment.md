# Experiment Section Template

Use this for `算例分析`, case studies, validation sections, or result-analysis sections.

## Recommended Structure

```text
x.5 算例分析
x.5.1 算例设置
  （1）测试系统说明
  （2）方案定义
  （3）参数设置
x.5.2 基础结果对比
x.5.3 运行过程或平衡特性分析
x.5.4 灵敏度分析（可选）
x.5.5 大规模系统验证（可选）
```

## Writing Guide

### Opening Paragraph

```text
本节基于……系统进行算例分析，以验证……。
共考虑……组方案，具体设置如表 x 所示。
所有算例通过……实现，并在……环境下测试。
```

### （1）测试系统说明

State:

1. what system is used
2. what components are included
3. why this system is suitable for validation

### （2）方案定义

Use a table when there are multiple schemes.

Keep the differences explicit:

- baseline
- proposed method
- ablation or variant
- risk-aware or storage-aware extension

### （3）参数设置

Use a table for:

- cost parameters
- efficiency parameters
- penetration assumptions
- confidence level or risk weight if relevant

### Result Comparison Paragraph

```text
表 x 对比了方案 A 和方案 B 的结果。
由表可知，方案 B 在……方面优于方案 A，主要体现在……。
相应地，……由……变化为……。
通过上述对比分析，证明了……。
```

### Dynamic Figure Interpretation Paragraph

```text
图 x 展示了……。
由图可知，系统在……阶段表现出……规律。
相较于方案 A，方案 B ……。
这说明……。
```

### Sensitivity Analysis Paragraph

```text
为进一步分析……对结果的影响，本节开展灵敏度分析。
由图可知，随着……增加/降低，……呈现……趋势。
这说明……对系统……具有重要影响。
```

## Final Check

- validation target is explicit
- baseline is explicit
- table/figure order is clean
- result interpretation includes mechanism, not just observation
- ending states what the experiment proves for the thesis claim
