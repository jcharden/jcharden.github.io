# Section1:Slicing

## [STRUCTURED NEURAL SUMMARIZATION](https://arxiv.org/pdf/1811.01824.pdf)

### Abstract

解决了将富含冗余信息的长文本转化为更精确的短文本抽象，该文章将weakly structured data即text转化为highly structured data即graph，这里保留了文本的上下文关系以及token的long-distance关系，然后结合图神经网络进行学习。

### Note

关键在于如何将text转成graph，这里用一张图来说明：

![](https://i.loli.net/2019/09/25/KAFojNnIVTtCarL.png)


文章用来CoreNLP来得到entity，有三种连接关系，next表示顺序关系，in表示从属关系，ref表示引用关系。

### Heuristic

可以把每一个statement再细分成token，然后用AST或者其他方式组织这些token，这样可以最大程度避免丢失由于长文本导致的statement中token信息丢失的问题，但是得到的图会更大，以及如何用AST去表示每条statement是一个待解决问题。

## [Code Vectors: Understanding Programs Through Embedded Abstracted Symbolic Traces](https://arxiv.org/pdf/1803.06686.pdf)

### Abstract

采用abstractions of traces obtained from symbolic execution of a program来表示程序，将这些traces转化为向量，这些向量即代码的特征表示。

### Note

关键在于如何抽象以及如何做word embedding

- 关于如何做抽象：
  ![](https://i.loli.net/2019/09/25/JafQ68xZEvOIjUR.png)
  ![](https://i.loli.net/2019/09/25/264JMpCwEgOFVhq.png)
  ![](https://i.loli.net/2019/09/25/D3fBOnV92WhAQS4.png)


- 关于如何做word embedding
  ![](https://i.loli.net/2019/09/25/kyGD2X45m7TpofO.png)

### Heuristic

提供了一个做slice以及word,statement embedding的思路
做slice可以结合符号执行，embedding可以用抽象表示，这样可以减少token的数量，以及删除冗余信息。

## [ORBS:Language-Independent Program Slicing]([./pdf/ORBS.pdf](http://www0.cs.ucl.ac.uk/staff/j.krinke/publications/fse14.pdf))

### Abstract

通过删除特定语句，且删除后对于特定输入，依然能得到原来的结果，不断删除。这是一个动态的slicing，需要testcase输入。

### Approach

给了一个slice的定义
![](https://i.loli.net/2019/09/25/P4LxGo2lAp75TE3.png)


### Heuristic

提供了一个slice的思路，通过删除之后而不改变语义的方法。

## [MOBS: Multi-Operator Observation-Based Slicing using Lexical Approximation of Program Dependence](http://www0.cs.ucl.ac.uk/staff/j.krinke/publications/icse18.pdf)

### Abstract

改进了ORBS，通过文本相似度

### Note

通过vsm和lda算法计算和待删除的lines和已经可以确定删除的lines的相似度，如果很相似则删掉。

### Heuristic

可以通过计算相似度的方法来对slice进行一些预处理

## [Abstract Program Slicing: an Abstract Interpretation-based approach to Program Slicing](https://arxiv.org/pdf/1605.05104.pdf)

### Abstract


### Note

![](https://i.loli.net/2019/09/25/3MmwcfkxKHuPYQB.png)

### Heuristic
