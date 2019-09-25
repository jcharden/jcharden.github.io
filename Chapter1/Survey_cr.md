# Code representation

## [A Novel Neural Source Code Representation based on Abstract Syntax Tree](http://xuwang.tech/paper/astnn_icse2019.pdf)

[pdf](http://xuwang.tech/paper/astnn_icse2019.pdf)

Propose a novel AST-based Neural Network (ASTNN) for source code
representation.

- An example of AST Statement nodes (marked in red)

![](https://i.loli.net/2019/09/25/mKRJpCDcZu7bG14.png)

- Overview

![](https://i.loli.net/2019/09/25/PFWhzAdqYB9Tbcw.png)

First, we parse a source code fragment into an AST, and design a preorder traversal algorithm to split each AST to a sequence of statement trees (ST-trees, which are trees consisting of statement nodes as roots and corresponding AST nodes of the statements), as illustrated in Figure 1. All ST-trees are encoded by the Statement Encoder to vectors, denoted as e1, · · · , et. We then use Bidirectional Gated Recurrent Unit [35] (Bi-GRU), to model the naturalness of the statements. The hidden states of Bi-GRU are sampled into a single vector by pooling, which is the representation of the code fragment.


## [Code Vectors: Understanding Programs Through Embedded Abstracted Symbolic Traces](https://arxiv.org/pdf/1803.06686.pdf)

[pdf](https://arxiv.org/pdf/1803.06686.pdf)

采用abstractions of traces obtained from symbolic execution of a program来表示程序，将这些traces转化为向量，这些向量即代码的特征表示。

关键在于如何抽象以及如何做word embedding

- 关于如何做抽象：
  ![](https://i.loli.net/2019/09/25/JafQ68xZEvOIjUR.png)
  ![](https://i.loli.net/2019/09/25/264JMpCwEgOFVhq.png)
  ![](https://i.loli.net/2019/09/25/D3fBOnV92WhAQS4.png)


- 关于如何做word embedding
  ![](https://i.loli.net/2019/09/25/kyGD2X45m7TpofO.png)
