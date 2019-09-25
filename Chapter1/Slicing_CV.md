# [Code Vectors: Understanding Programs Through Embedded Abstracted Symbolic Traces](https://arxiv.org/pdf/1803.06686.pdf)

## Abstract

采用abstractions of traces obtained from symbolic execution of a program来表示程序，将这些traces转化为向量，这些向量即代码的特征表示。

## Note

关键在于如何抽象以及如何做word embedding

- 关于如何做抽象：
  ![](https://i.loli.net/2019/09/25/JafQ68xZEvOIjUR.png)
  ![](https://i.loli.net/2019/09/25/264JMpCwEgOFVhq.png)
  ![](https://i.loli.net/2019/09/25/D3fBOnV92WhAQS4.png)


- 关于如何做word embedding
  ![](https://i.loli.net/2019/09/25/kyGD2X45m7TpofO.png)

## Thought

提供了一个做slice以及word,statement embedding的思路
做slice可以结合符号执行，embedding可以用抽象表示，这样可以减少token的数量，以及删除冗余信息。
