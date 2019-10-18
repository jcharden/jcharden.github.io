# Learning-based Recursive Aggregation of Abstract Syntax Trees for Code Clone Detection

[pdf](https://pvs.ifi.uni-heidelberg.de/fileadmin/papers/2019/Buech-Andrzejak-SANER2019.pdf)

tags: ASTs

Implement an AST-based Recursive Neural Network.

## Data preprocessing

![](https://i.loli.net/2019/10/18/Mn3Zbq8NLUPDCFg.png)

## Embedding

Use the word2vec skipgram model and make three modifications. First, we fix the context size and view contexts as ordered tuples, rather than bags of tokens. Second, in the case of node types, we define the context not by a window, but by the local neighborhood of the node (parent, children). That means that there is an ordered context of three elements. In the case of node contents, we use an ordered context of four elements (two preceding and two succeeding tokens). Finally, the total possible number of positive and negative samples is relatively small. Therefore, we consider its entirety, instead of statistical sampling and smoothing w.r.t. the relative frequencies.

Use [Tree-Structured Long Short-Term Memory Networks](https://github.com/stanfordnlp/treelstm)