# 算例与实验章节模式

## 默认实验逻辑

建议按以下顺序：

1. state the validation goal
2. describe the case system or dataset
3. define comparison schemes
4. give parameter or boundary settings
5. present results
6. interpret the mechanism behind the result
7. state what the comparison proves

## 常见结构

### 模式 A：方法验证

适用于新模型或新分解方法：

1. experiment goal
2. data source and computing environment
3. module-by-module result
4. overall reconstruction or final comparison
5. conclusion

### 模式 B：方案对比

适用于优化或仿真框架：

1. scheme setting
2. test system description
3. parameter setting
4. result comparison
5. interpretation
6. conclusion

### 模式 C：风险或鲁棒性分析

适用于不确定性、CVaR 或鲁棒规划问题：

1. scheme setting
2. scenario or uncertainty configuration
3. base results
4. sensitivity analysis
5. larger system verification
6. conclusion

## 可复用章节骨架

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

## 结果分析段模板

```text
表 x 对比了方案 A 和方案 B 的结果。
由表可知，方案 B 在……方面优于方案 A，主要体现在……。
相应地，……由……变化为……。
通过上述对比分析，证明了……。
```

## 图结果解读模板

```text
图 x 展示了……。
由图可知，……。
系统在……阶段表现出……规律。
这说明……。
```

## 图表组织顺序

算例小节内部优先按以下顺序组织：

1. scheme table
2. topology figure
3. parameter table
4. result table
5. dynamic result figures

## 什么算是强实验章节

一个强实验章节应回答：

1. what is being validated
2. against what baseline
3. under what conditions
4. what changed
5. why it changed
6. what this means for the thesis claim
