# SourcererCC: Scaling Code Clone Detection to Big Code

tags: tokens

[pdf](https://arxiv.org/pdf/1512.06448.pdf)

## Overview

A token-based clone detector that targets three clone types, and exploits an index to achieve scalability to large inter-project repositories using a standard workstation.

![](https://i.loli.net/2019/09/26/oRiwh8eOY76Baj4.png)

## Approach

Two primary stages: (i) partial index creation; and (ii) clone detection.

### Partial index creation

Parses the code blocks from the source files, and tokenizes them with a simple scanner that is aware of token and block semantics of a given language(java c c#). From the code blocks it builds an inverted index mapping tokens to the blocks that contains them. Unlike previous approaches, it does not create an index of all tokens in the code blocks, instead it uses a filtering heuristic to construct a partial index of only a subset of the tokens in each block.

### Clone detection

Iterates through all of the code blocks, retrieves their candidate clone blocks from the index. As per the filtering heuristic, only the tokens within the sub-block are used to query the index, which reduces the number of candidate blocks. After candidates are retrieved, SourcererCC uses another filtering heuristic, which exploits ordering of the tokens in a codeblock to measure a live upper-bound and lower-bound of similarity scores between the query and candidate blocks. Candidates whose upper-bound falls below the similarity threshold are eliminated immediately without further processing. Similarly, candidates are accepted as soon as their lower-bound exceeds the similarity threshold. This is repeated until the clones of every code block are located. SourcererCC exploits symmetry to avoid detecting the same clone twice.
