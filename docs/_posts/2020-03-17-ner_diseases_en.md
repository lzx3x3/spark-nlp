---
layout: model
title: Ner DL Model Diseases
author: John Snow Labs
name: ner_diseases
class: NerDLModel
language: en
repository: clinical/models
date: 2020-03-17
tags: [clinical,ner,en]
article_header:
   type: cover
use_language_switcher: "Python-Scala-Java"
---

{:.h2_title}
## Description
Named Entity recognition annotator allows for a generic model to be trained by utilizing a deep learning algorithm (Char CNNs - BiLSTM - CRF - word embeddings) inspired on a former state of the art model for NER: Chiu & Nicols, Named Entity Recognition with Bidirectional LSTM,CNN.
Pretrained named entity recognition deep learning model for diseases.

## Predicted Entities 
Disease

{:.btn-box}
<button class="button button-orange" disabled>Live Demo</button>
[Open in Colab](https://colab.research.google.com/github/JohnSnowLabs/spark-nlp-workshop/blob/master/tutorials/Certification_Trainings/Healthcare/1.Clinical_Named_Entity_Recognition_Model.ipynb){:.button.button-orange.button-orange-trans.co.button-icon}[Download](https://s3.amazonaws.com/auxdata.johnsnowlabs.com/clinical/models/ner_diseases_en_2.4.4_2.4_1584452534235.zip){:.button.button-orange.button-orange-trans.arr.button-icon}
{:.h2_title}
## How to use 
<div class="tabs-box" markdown="1">

{% include programmingLanguageSelectScalaPython.html %}

```python
model = NerDLModel.pretrained("ner_diseases","en","clinical/models")
	.setInputCols("sentence","token","word_embeddings")
	.setOutputCol("ner")
```

```scala
val model = NerDLModel.pretrained("ner_diseases","en","clinical/models")
	.setInputCols("sentence","token","word_embeddings")
	.setOutputCol("ner")
```
</div>

{:.model-param}
## Model Information

{:.table-model}
|----------------|----------------------------------|
| Name:           | ner_diseases                     |
| Type:    | NerDLModel                       |
| Compatibility:  | Spark NLP 2.4.4 +                           |
| License:        | Licensed                         |
|Edition:|Official|                       |
|Input labels:         | [sentence, token, word_embeddings] |
|Output labels:        | [ner]                              |
| Language:       | en                               |
| Case sensitive: | False                            |
| Dependencies:  | embeddings_clinical              |

{:.h2_title}
## Data Source
Trained on i2b2 with `embeddings_clinical`.