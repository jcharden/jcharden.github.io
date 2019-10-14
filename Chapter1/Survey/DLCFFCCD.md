# Deep Learning Code Fragments for Code Clone Detection

[pdf](https://tufanomichele.com/publications/C5.pdf)

tags: ASTs

## Approach

Proposed a learning-based approach for clone detection.

Generally, there are four clone types.
  - Type I: Identical fragments except for variations in comments and layout.
  - Type II: Identical fragments except for variations in identifier names and literal values in addition to Type I differences.
  - Type III: Syntactically similar fragments that differ at the statement level. The fragments have statements added, modified, or removed with respect to each other, in addition to Type II differences - Type IV: Syntactically dissimilar fragments that implement the same functionality.

Type I, II, and III clones indicate textual similarity whereas Type IV clones indicate functional similarity.

![](https://i.loli.net/2019/09/26/IbQPi71VkKFesGx.png)

- The first part we use a particular type of language model, an RtNN, to
map each term in a fragment to an embedding.
- The second part we use the language’s grammar and a recursive learning procedure, implemented as an RvNN, to encode arbitrarily long sequences of embeddings to characterize fragments.

## 拓展

Recently, Language models' effectiveness has suffused SE tasks such as code suggestion , deriving readable string test inputs to reduce human oracle cost , predicting comments to improve search over code bases and code categorization , improving error reporting , generating feasible test cases to improve coverage , improving stylistic consistency to aid readability and maintainability, code migration, synthesizing API completions , code review , fault localization , and suggesting method and class names.
