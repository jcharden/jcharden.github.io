# DeepFL: Integrating Multiple Fault Diagnosis Dimensions for Deep Fault Localization

tags: texts, properties, labels

[pdf](https://dl.acm.org/citation.cfm?id=3330574)

Collect various suspiciousness-value-based, fault-proneness-based and
textual-similarity-based features from the fault localization, defect
prediction and information retrieval areas. Working at method level.

- Spectrum-based Suspiciousness

  learn faulty locations based on suspiciousness values computed by 25 traditional spectrum-based fault localization techniques.

- Mutation-based Suspiciousness
- Complexity-based Fault Proneness

  code complexity metrics have been widely used to estimate the fault-proneness of code elements in the field of defect prediction. we collect all the 21 widely-used code complexity metrics (shown in Table 1) for the method level (since DeepFL works at the method level). In addition, we also collect the statistics for each type of Java ASM [67] bytecode instructions shown Table 1. In total, we have 37 complexity-based features.
  ![](https://i.loli.net/2019/09/25/cO8PviS2GapoWhE.png)

- Textual Similarity Information

  We investigate the textual similarity between source code methods and failed test information. Similar with the structured information retrieval work, we also collect different fields for both queries and documents. Query fields come from failed tests, including the name of failed tests, the source code of failed tests and the complete failure message (including exception type, message, and stacktrace). Document fields come from source code methods, including: the full qualified name of the method, accessed classes, method invocations, used variables, and comments. Each field of query can be searched on each field of document, yielding 15 combinations. For each combination, we calculate the similarity score between the query field and the document field by using the popular TF.IDF model. Then, we treat the similarity scores of the 15 combinations as 15 features for our DeepFL.

  ![](https://i.loli.net/2019/09/25/hfq7KwJeIHSY85c.png)

