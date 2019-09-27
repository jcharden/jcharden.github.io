# Automatically Learning Semantic Features for Defect Prediction

tags: ASTs

[pdf](https://ece.uwaterloo.ca/~lintan/publications/deeplearn-icse16.pdf)

Leverage Deep Belief Network (**DBN**) to automatically learn semantic features from token vectors extracted from programs’ Abstract Syntax Trees (**ASTs**).

## Motivating example

![](https://i.loli.net/2019/09/25/kur9RjVgcZP2Js3.png)

## Prediction process

1) nodes of method invocations and class instance creations
2) declaration nodes, i.e., method declarations, type declarations, and enum declarations, and
3) control-flow nodes such as while statements, catch clauses, if statements, throw statements.

![](https://i.loli.net/2019/09/25/duC6mnSi8aZcXjx.png)

![](https://i.loli.net/2019/09/25/Odjflb4Su965QCn.png)
