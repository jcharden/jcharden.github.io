# [MOBS: Multi-Operator Observation-Based Slicing using Lexical Approximation of Program Dependence](http://www0.cs.ucl.ac.uk/staff/j.krinke/publications/icse18.pdf)

## 1 Abstract

改进了ORBS，通过文本相似度

## 2 Note

通过vsm和lda算法计算和待删除的lines和已经可以确定删除的lines的相似度，如果很相似则删掉。

## 3 Heuristic

可以通过计算相似度的方法来对slice进行一些预处理