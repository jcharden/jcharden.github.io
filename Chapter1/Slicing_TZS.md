# [TZSlicer](https://ieeexplore.ieee.org/document/8383886)

[pdf](https://ieeexplore.ieee.org/document/8383886)

## Abstract

针对information leakage的问题，提出了一种能自动识别发生information leakage的代码位置，介绍了slicing的方法。

## Note

### 框架

![](https://i.loli.net/2019/09/25/6EX4aC5GsHflqrO.png)

### Taint analyzer

三个粒度进行taint：

- Method-level Tainting (TZ-M), which taints the program at the function level and generates security sensitive functions and non-sensitive functions;
- Block-level Tainting (TZ-B), which further taints the internal code blocks (e.g., branches) within the functions and generates security sensitive and non-sensitive blocks; and
- Line-level Tainting (TZ-L), in which each line of the program is labeled as either security sensitive or non-sensitive based on the taint propagation.

### Program Slicer & Slice Optimizer

An important design principle of the Program Slicer is to ensure that the sliced programs are functionally equivalent to the original program.

Employ dynamic taint analysis that is dependent upon the specific executions of the sliced programs, which has been shown to achieve significantly smaller slices than static slicing.

- TZ-M Slicing
- TZ-B Slicing
- TZ-L Slicing

## Thought

结合动态的taint analysis可以得到更小而精的slice。