# SEKA : Seeking Knowledge Graph Anomalies

## Introduction
This repository provides the implementation of an approach to unsupervised anomaly detection in knowledge graphs. We first 
characterize triples in a directed edge-labelled knowledge graph using a set of binary features, and then employ a one-class support vector machine classifier to classify these
triples  as normal or abnormal. 

## Technologies
This project is implemented using:
* Python 3.6

Following Python packages are used in the project. 
* pandas v1.3.1
* nltk v3.6.2
* networkx v2.6.2
* numpy v1.21.2
* rdflib v6.0.0
* validators v0.18.2
* matplotlib v3.4.2
* statsmodels v0.13.0
* spacy v3.1.3
* parameters v0.2.1
* python_dateutil v2.8.2
* scikit_learn v1.0


## Execute the project
Download the project from:
```
https://www.dropbox.com/sh/0k59vbce81ya71z/AAAxWoNRAyXDA86-TvhVQU_Aa?dl=0
```

Install the required packages:
```
pip install -r requirements.txt
```

Open a terminal and change directory to the cloned project:
```
cd <path_to_directory>/SEKA

```


Ensure that the following resources are inside the 'assets' folder. They should be properly
downloaded, and imported.
````
en_core_web_sm-3.0.0
Download lilnk: https://github.com/explosion/spacy-models/releases/download/en_core_web_sm-3.0.0/en_core_web_sm-3.0.0.tar.gz

stanford-ner-4.2.0
Download lilnk: https://nlp.stanford.edu/software/stanford-ner-4.2.0.zip

YAGO-1
https://yago-knowledge.org/downloads/yago-1

````


The .py files in the folder runs in the following order:

(1) triple_features.py
(2) entity_features.py
(3) svm_training.py

Additionally, if you wish to inject anomalies to the KGs, use the implementation in ink.py.

For ease of exploring task 2 of our approach, which is target predicate fact anomaly detection, we have used a sample
predicate (http://yago-knowledge.org/resource/bornIn) from YAGO-1 in triple_features.py. We have also provided 
sample_persons.csv for you to explore task 3 of our approach, target type entity anomaly detection. By using these
pre fetched data, you can eliminate the need of populating the graph from a raw file, thus reducing the need of 
having a high performance computer.