---
entry_id: "exemplo-2-arvores-de-decisao-regressao-diabetes"
title: "Exemplo 2 - Arvores de Decisão - Regressão - Diabetes"
language: "jupyter"
category: "codigo-professor"
unit: ""
source: "raw/code/professor/exemplo-2-arvores-de-decisao-regressao-diabetes.ipynb"
---
# Exemplo 2 - Arvores de Decisão - Regressão - Diabetes

> **Linguagem:** jupyter

## Célula 1 — Markdown

# Machine Learning I
# Aprendizado Supervisionado
## Escrito por Duncan Ruiz

Prática com Decision Tree Regressor e Diabetes

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
from sklearn.tree import DecisionTreeRegressor as DTR
from sklearn.tree import plot_tree, export_graphviz, export_text
from sklearn.metrics import mean_absolute_error as mae
from sklearn.metrics import mean_squared_error as mse

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
diabetes = datasets.load_diabetes(as_frame=True)
print(diabetes.DESCR)
```

## Célula 4 — Código

```python
# separação em features e target
X = diabetes.data
y = diabetes.target
diabetes.frame
```

## Célula 5 — Código

```python
# separação em treino e teste, e X e y

treino_X, teste_X, treino_y, teste_y = tts(X, y, test_size=0.3)

print(treino_X.shape)
print(treino_y.shape)
print(teste_X.shape)
print(teste_y.shape)
```

## Célula 6 — Código

```python
# indução do modelo de classificação por árvore de decisão para regressão
ccp_alphas = [0.0, 0.05, 0.1, 0.15, 0.2, 0.25, 0.3, 0.35, 0.4, 0.45, 0.5, 0.6, 0.7, 0.8, 0.9, 1.0, 2.0, 3.0, 5.0, 10.0, 100.0]
#ccp_alphas = [0.0, 0.005, 0.01, 0.015, 0.02, 0.025, 0.03, 0.04, 0.05, 0.055, 0.06, 0.07, 0.08, 0.09, 0.1]
#ccp_alphas = [0.08]
#ccp_alphas = [0.005]
#ccp_alphas = [1.0]

for ccp_i in ccp_alphas:
    modelo = DTR(random_state=0
                ,criterion="squared_error"  # 'squared_error', 'friedman_mse', 'absolute_error', 'poisson'
                ,min_samples_split=66  # default 2
                ,min_samples_leaf=50   # default 1
                ,max_leaf_nodes=None  # default None
                ,ccp_alpha=ccp_i        # default 0.0 Valores na documentação 0.005 0.01 0.015 0.02 0.025 0.03 0.035
                )
    modelo.fit(treino_X, treino_y)
    teste_pred_y = modelo.predict(teste_X)

    MAE = mae(teste_y, teste_pred_y)
    RMSE = mse(teste_y, teste_pred_y, squared=False)
    print('Alpha=', ccp_i,'  MAE=', MAE, '  RMSE=', RMSE)
```

## Célula 7 — Código

```python
# apresentações do modelo
modelo_txt = export_text(modelo, feature_names=diabetes['feature_names'])
print(modelo_txt)
```

## Célula 8 — Código

```python
# apresentações do modelo
plt.figure(figsize=(15, 15))
plot_tree(modelo, filled=True, rounded=True, feature_names=diabetes.feature_names)
plt.title('Árvore de Decisão treinada no dataset Diabetes')
plt.show()
```

## Célula 9 — Código

```python

```
