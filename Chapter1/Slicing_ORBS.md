# [ORBS:Language-Independent Program Slicing]([./pdf/ORBS.pdf](http://www0.cs.ucl.ac.uk/staff/j.krinke/publications/fse14.pdf))

## 1 Abstract

通过删除特定语句，且删除后对于特定输入，依然能得到原来的结果，不断删除。这是一个动态的slicing，需要testcase输入。

## 2 Approach

给了一个slice的定义
![](https://i.loli.net/2019/09/25/P4LxGo2lAp75TE3.png)


## 3 Heuristic

提供了一个slice的思路，通过删除之后而不改变语义的方法。