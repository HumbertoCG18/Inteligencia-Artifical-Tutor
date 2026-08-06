---
entry_id: "exemplo-1-arvores-de-decisao-classificacao-planta-iris"
title: "Exemplo 1 - Árvores de Decisão Classificação - Planta Iris"
language: "jupyter"
category: "codigo-professor"
unit: ""
source: "raw/code/professor/exemplo-1-arvores-de-decisao-classificacao-planta-iris.ipynb"
---
# Exemplo 1 - Árvores de Decisão Classificação - Planta Iris

> **Linguagem:** jupyter

## Célula 1 — Markdown

# Machine Learning I
# Aprendizado Supervisionado
## Escrito por Duncan Ruiz

Prática com Decision Tree Classifier e Iris

## Célula 2 — Código

```python
# pacotes básicos
import math
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt

# pacotes do sklearn para acesso a datasets, preparação, modelagem e avaliação
from sklearn import datasets
# pacote pipeline para combinar preparação e modelagem
from sklearn.pipeline import Pipeline, make_pipeline
# arsenal de preparação
from sklearn.preprocessing import MinMaxScaler # rescala em min-max
from sklearn.preprocessing import StandardScaler # padroniza features removendo média e
#     escalando para variância unitária. Também chamado de z-score
#
from sklearn.model_selection import train_test_split as tts
from sklearn.model_selection import StratifiedKFold as skf
from sklearn.model_selection import GridSearchCV as gscv
from sklearn.tree import DecisionTreeClassifier as DTC
from sklearn.tree import plot_tree, export_graphviz, export_text
from sklearn.metrics import accuracy_score as acc_score
from sklearn.metrics import confusion_matrix as cm
from sklearn.metrics import ConfusionMatrixDisplay as CMD

#pacotes para apoio a leitura e gravação de datasets
from pathlib import Path
import csv

#pacotes para visualização e formatação
import pprint
import graphviz
```

## Célula 3 — Código

```python
# carga de dados
iris = datasets.load_iris(as_frame=True)
print(iris.DESCR)
```

## Célula 4 — Código

```python
# separação em features e target
X = iris.data
y = iris.target
iris.frame
```

## Célula 5 — Código

```python
print(X.shape)
print(y.shape)
```

## Célula 6 — Código

```python
# separação em treino e teste, e X e y

treino_X, teste_X, treino_y, teste_y = tts(X, y, random_state=0,test_size=0.3, stratify=y)

print(treino_X.shape)
print(treino_y.shape)
print(teste_X.shape)
print(teste_y.shape)
print(np.stack(np.unique(teste_y, return_counts=True), axis=1))
```

## Célula 7 — Código

```python
teste_X
```

## Célula 8 — Código

```python
# indução do modelo de classificação por árvore de decisão
#ccp_alphas = [0.0, 0.05, 0.1, 0.15, 0.2, 0.25, 0.3, 0.35, 0.4, 0.45, 0.5]
#ccp_alphas = [0.0, 0.005, 0.01, 0.015, 0.02, 0.025, 0.03, 0.04, 0.05, 0.055, 0.06, 0.07, 0.08, 0.09, 0.1]
#ccp_alphas = [0.055]
ccp_alphas = [0.0]

for ccp_i in ccp_alphas:
    modelo = DTC(random_state=0
                ,criterion='entropy'  # 'gini', 'entropy', 'log_loss'
                ,min_samples_split=2  # default 2
                ,min_samples_leaf=1   # default 1
                ,max_leaf_nodes=None  # default None
                ,class_weight=None    # default None. 'balanced' para equilibrar classes
                ,ccp_alpha=ccp_i        # default 0.0 Valores na documentação 0.005 0.01 0.015 0.02 0.025 0.03 0.035
                )
    modelo.fit(treino_X, treino_y)
    teste_pred_y = modelo.predict(teste_X)
    acuracia = acc_score(teste_y, teste_pred_y)
    resultado = cm(teste_y, teste_pred_y)

    #cm_display = CMD(resultado).plot()
    print('Alpha=', ccp_i,' Acuracia=', acuracia)
```

## Célula 9 — Código

```python
# apresentações do modelo
modelo_txt = export_text(modelo, feature_names=iris['feature_names'])
print(modelo_txt)
```

## Célula 10 — Código

```python
# apresentações do modelo
plt.figure(figsize=(10, 10))
plot_tree(modelo, filled=True, rounded=True, feature_names=iris.feature_names, class_names=iris.target_names)
plt.title('Árvore de Decisão treinada no dataset Iris')
plt.show()
```

## Célula 11 — Código

```python

```
