# [STRUCTURED NEURAL SUMMARIZATION](https://arxiv.org/pdf/1811.01824.pdf)

[pdf](http://www0.cs.ucl.ac.uk/staff/j.krinke/publications/fse14.pdf)

## Abstract

解决了将富含冗余信息的长文本转化为更精确的短文本抽象，该文章将weakly structured data即text转化为highly structured data即graph，这里保留了文本的上下文关系以及token的long-distance关系，然后结合图神经网络进行学习。

## Note

关键在于如何将text转成graph，这里用一张图来说明：

![](https://i.loli.net/2019/09/25/KAFojNnIVTtCarL.png)


文章用来CoreNLP来得到entity，有三种连接关系，next表示顺序关系，in表示从属关系，ref表示引用关系。

## Thought

可以把每一个statement再细分成token，然后用AST或者其他方式组织这些token，这样可以最大程度避免丢失由于长文本导致的statement中token信息丢失的问题，但是得到的图会更大，以及如何用AST去表示每条statement是一个待解决问题。