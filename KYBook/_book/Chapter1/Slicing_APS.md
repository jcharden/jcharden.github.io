# [Abstract Program Slicing: an Abstract Interpretation-based approach to Program Slicing](https://arxiv.org/pdf/1605.05104.pdf)

[pdf](https://arxiv.org/pdf/1605.05104.pdf)

## Abstract

基于传统的slicing提出了抽象slicing，只考虑data的属性而不是准确的值。

## Note

![](https://i.loli.net/2019/09/25/3MmwcfkxKHuPYQB.png)

Program slicing is used for reducing the size of programs to analyze. Nevertheless, sometimes this reduction is not sufficient for really improving an analysis. Suppose that some variables at some point of execution do not have a desired property (for example, that they are different from 0, or from null); in order to understand where the error occurred, it would be useful to find those statements which affect such a property of these variables. **Standard slicing may return too many statements**, making it hard for the programmer to realize which one caused the error.

## Thought

为实现相同功能可能有很多种程序写法，通过抽象可以让程序泛型化，特征表示更精准，可以避免混淆。