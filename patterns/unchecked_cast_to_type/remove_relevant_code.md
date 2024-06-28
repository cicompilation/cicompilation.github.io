---
layout: page
---
## KBNLresearch/europeananp-ner 137.1

### Warning Message

---------------------

```java
/home/travis/build/KBMLresearch/europeananp-ner/sre/ain/java/nl/kbresearch/europeana_newspapers/ner/alto/Altoprocessor.java:[100,17]unchecked cast
required:edu.stanford.nlp.ie.crf.CRFClassifier<edu.stanford.nlp.util.CoreMap>
found:edu.stanford.nlp.ie.crf.CRFClassifier<capture#1 of ?>

```

### Code Change

---------------------

***src/main/java/nl/kbresearch/europeana_newspapers/ner/alto/AltoProcessor.java***

```diff
- CRFClassifier<CoreMap> classifier_alto = (CRFClassifier<CoreMap>) NERClassifiers.getCRFClassifierForLanguage(lang);
```