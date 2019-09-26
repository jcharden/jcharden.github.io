# A Novel Neural Source Code Representation based on Abstract Syntax Tree

tags: ASTs

[pdf](http://xuwang.tech/paper/astnn_icse2019.pdf)

## Overview

Propose a novel AST-based Neural Network (ASTNN) for source code
representation.

- An example of AST Statement nodes (marked in red)

![Figure 1](https://i.loli.net/2019/09/25/mKRJpCDcZu7bG14.png)

## Approach

![](https://i.loli.net/2019/09/25/PFWhzAdqYB9Tbcw.png)

First, we parse a source code fragment into an AST, and design a preorder traversal algorithm to split each AST to a sequence of statement trees (ST-trees, which are trees consisting of statement nodes as roots and corresponding AST nodes of the statements), as illustrated in Figure 1. All ST-trees are encoded by the Statement Encoder to vectors, denoted as e1, · · · , et.(preorder travel+word2vec+mp) We then use Bidirectional Gated Recurrent Unit (Bi-GRU), to model the naturalness of the statements. The hidden states of Bi-GRU are sampled into a single vector by pooling, which is the representation of the code fragment.