# DECKARD: Scalable and Accurate Tree-based Detection of Code Clones

tags: ASTs

[pdf](https://web.cs.ucdavis.edu/~su/publications/icse07.pdf)

## Overview

Present an efficient algorithm for identifying similar subtrees and apply it to tree representations of source code. Our algorithm is based on a novel characterization of subtrees with numerical vectors in the Euclidean space and an efficient algorithm to cluster these vectors w.r.t. the Euclidean distance metric. Subtrees with vectors in one cluster are considered similar.

## Approach

![](https://i.loli.net/2019/09/26/hLqYkEHe9gQFCcW.png)

- Characteristic Vectors
  The characteristic vector of a subtree is a point <c1, . . . , cni> in the Euclidean space, where each ci represents the count of occurrences of a specific tree pattern in the subtree.

  ![](https://i.loli.net/2019/09/26/tQT2xHL5i8BGl43.png)

- Vector Merging
  Sum up the vectors of certain node sequences. The choice of which nodes in the tree to merge is important; these nodes must make good boundaries among cloned code, while not frequently containing large subtrees.
- Vector Clustering and Post-Processing
   clusters similar characteristic vectors w.r.t. their Euclidean distances to detect cloned code.
