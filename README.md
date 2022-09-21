# SEKA : Seeking Knowledge Graph Anomalies

## Introduction

Development is under progress. Expect frequent source code commits.

This repository provides the implementation of an approach to
unsupervised anomaly detection in knowledge graphs. The algorithm
first characterises triples in a directed edge-labelled knowledge
graph using a set of binary features, and then uses a one-class
support vector machine classifier to classify the triples as normal or
abnormal.

## Requirements

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

Download the project:

```bash
git clone git@github.com:AsaraSenaratne/SEKA.git
```

Open a terminal and change directory to the cloned project:

```bash
cd SEKA
```

Install the required packages:

```bash
pip install -r requirements.txt
```

Ensure that the following resources are inside the 'assets'
folder. They should be properly downloaded, and imported.

```
mkdir assets
pushd assets
```

```
wget https://github.com/explosion/spacy-models/releases/download/en_core_web_sm-3.0.0/en_core_web_sm-3.0.0.tar.gz
wget https://nlp.stanford.edu/software/stanford-ner-4.2.0.zip
wget https://yago-knowledge.org/data/yago1/yago-1.0.0-turtle.7z
```

```
tar xvf en_core_web_sm-3.0.0.tar.gz
unzip stanford-ner-4.2.0.zip
7z x yago-1.0.0-turtle.7z
```

```
popd
````

This demo using YAGO requires quite a bit of RAM, over 16GB.

The .py files in the folder run in the following order:

(1) triple_features.py
(2) entity_features.py
(3) svm_training.py

Additionally, if you wish to inject anomalies to the KGs, use the implementation in ink.py.
