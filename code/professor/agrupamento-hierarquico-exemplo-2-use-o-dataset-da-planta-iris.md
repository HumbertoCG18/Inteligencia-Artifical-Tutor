---
entry_id: "agrupamento-hierarquico-exemplo-2-use-o-dataset-da-planta-iris"
title: "agrupamento hierarquico - exemplo 2 (use o dataset da planta IRIS)"
language: "jupyter"
category: "codigo-professor"
unit: ""
source: "raw/code/professor/agrupamento-hierarquico-exemplo-2-use-o-dataset-da-planta-iris.ipynb"
---
# agrupamento hierarquico - exemplo 2 (use o dataset da planta IRIS)

> **Linguagem:** jupyter

## Célula 1 — Markdown

# **Aprendizado não Supervisionado: Agrupamento Hierárquico -Exemplo 2**
Sílvia Moraes
---

Exemplo 2: Neste exemplo, a aplicação de agrupamento hierárquico aglomerativo é feita sobre o **dataset da planta IRIS**. Usamos o pacote Agglomerative Clustering do sklearn na implementação.

## Célula 2 — Código

```python
import pandas as pd
import numpy as np
from matplotlib import pyplot as plt
from sklearn.cluster import AgglomerativeClustering
import scipy.cluster.hierarchy as sch
```

## Célula 3 — Markdown

**Carga do dataset** da planta IRIS sem a classe, ou seja, sem o tipo de planta IRIS.

## Célula 4 — Código

```python
#Exemplo com a planta Iris
iris = pd.read_csv("IRIS.csv")
X = iris.iloc[:, [0, 1, 2, 3]].values
```

## Célula 5 — Markdown

**Agglomerative Clustering**

O algoritmo possui vários parâmetros. Segue aqui alguns que usamos:

*   **n_clusters** : serve para determinar quantos clusters você gostaria. Após alguns testes e visualização do dendograma, você pode estabelecer a quantidade de clusters desejada. O valor default desse parâmetro é 2.

*  **metric** : métrica usada para medir a similaridade (distância) dos clusters ao longo do processo aglomerativo. Pode ser: “euclidean”, “l1”, “l2”, “manhattan”, “cosine”, or “precomputed” (neste caso, é necessário informar na entrada a matriz de distâncias/adjacências já calculada). Se for configurado como None, a métrica padrão é “euclidean”.
*   **linkage**: define o algoritmo aglomerativo que será usado como critério para realizar o merge dos dois clusters próximos. Na prática, o algoritmo determina que pontos de cada um dos clusters sob avaliação serão considerados pela métrica que estabelece similaridade. E ainda, ao confirmar proximidade, o algoritmo realiza a união dos mesmos. Pode ser:"ward", "complete", "average", "single". "ward" é o default.

1.   *ward* : minimiza a variância dos clusters que estão sendo unidos. Só aceita "euclidean" como métrica de distância.
2.   *average* : usa a média das distâncias de cada elemento de um cluster em relação ao outro.
1.   *complete* ou *maximum *: usa a maior distância, ao computar a distância de cada elemento de um cluster em relação ao outro.
2.   *single* ou *minimum* : usa a menor distância, ao computar a distância de cada elemento de um cluster em relação ao outro.

## Célula 6 — Código

```python
#---------------------------------------------------------------------------------------
#Fizemos vários testes de configuração desse algoritmo.
#Para testar, retire os comentários apenas da configuração que você quer estudar.
#Plotamos um dendograma para você conseguir visualizar o resultado
#---------------------------------------------------------------------------------------

#Exemplo 1
#dendrogram = sch.dendrogram(sch.linkage(X, method='ward'))
#model = AgglomerativeClustering(metric='euclidean', linkage='ward')

#Exemplo 2
#dendrogram = sch.dendrogram(sch.linkage(X, method='single'))
#model = AgglomerativeClustering(n_clusters=5, metric='euclidean', linkage='single')

#Exemplo 3
dendrogram = sch.dendrogram(sch.linkage(X, method='complete'))
model = AgglomerativeClustering(n_clusters=3, metric='euclidean', linkage='complete')

#Exemplo 4
#dendrogram = sch.dendrogram(sch.linkage(X, method='average'))
#model = AgglomerativeClustering(n_clusters=3, metric='euclidean', linkage='average')
```

**Saída:**

```text
<Figure size 640x480 with 1 Axes>
```

## Célula 7 — Markdown

Trecho a seguir que mostra como os dados foram agrupados. Usamos os labels atribuidos pelo algoritmo para mostrar a organização realizada pelo algoritmo.

## Célula 8 — Código

```python
model.fit(X)
labels = model.labels_
numCluster = model.n_clusters
print("Cluster dos dados: ", labels)
print("Numero de clusters: ", numCluster)

for iCluster in range(0,numCluster):
  print("Cluster: ", iCluster)
  for indice in range(0, len(labels)):
    if labels[indice]==iCluster: print(X[indice])

plt.show()
```

**Saída:**

```text
Cluster dos dados:  [1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1
 1 1 1 1 1 1 1 1 1 1 1 1 1 0 0 0 2 0 2 0 2 0 2 2 2 2 0 2 0 2 2 0 2 0 2 0 0
 0 0 0 0 0 2 2 2 2 0 2 0 0 0 2 2 2 0 2 2 2 2 2 0 2 2 0 0 0 0 0 0 2 0 0 0 0
 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
 0 0]
Numero de clusters:  3
Cluster:  0
[7.  3.2 4.7 1.4]
[6.4 3.2 4.5 1.5]
[6.9 3.1 4.9 1.5]
[6.5 2.8 4.6 1.5]
[6.3 3.3 4.7 1.6]
[6.6 2.9 4.6 1.3]
[6.1 2.9 4.7 1.4]
[6.7 3.1 4.4 1.4]
[6.2 2.2 4.5 1.5]
[5.9 3.2 4.8 1.8]
[6.3 2.5 4.9 1.5]
[6.1 2.8 4.7 1.2]
[6.4 2.9 4.3 1.3]
[6.6 3.  4.4 1.4]
[6.8 2.8 4.8 1.4]
[6.7 3.  5.  1.7]
[6.  2.9 4.5 1.5]
[6.  2.7 5.1 1.6]
[6.  3.4 4.5 1.6]
[6.7 3.1 4.7 1.5]
[6.3 2.3 4.4 1.3]
[6.1 3.  4.6 1.4]
[6.2 2.9 4.3 1.3]
[6.3 3.3 6.  2.5]
[5.8 2.7 5.1 1.9]
[7.1 3.  5.9 2.1]
[6.3 2.9 5.6 1.8]
[6.5 3.  5.8 2.2]
[7.6 3.  6.6 2.1]
[7.3 2.9 6.3 1.8]
[6.7 2.5 5.8 1.8]
[7.2 3.6 6.1 2.5]
[6.5 3.2 5.1 2. ]
[6.4 2.7 5.3 1.9]
[6.8 3.  5.5 2.1]
[5.7 2.5 5.  2. ]
[5.8 2.8 5.1 2.4]
[6.4 3.2 5.3 2.3]
[6.5 3.  5.5 1.8]
[7.7 3.8 6.7 2.2]
[7.7 2.6 6.9 2.3]
[6.  2.2 5.  1.5]
[6.9 3.2 5.7 2.3]
[5.6 2.8 4.9 2. ]
[7.7 2.8 6.7 2. ]
[6.3 2.7 4.9 1.8]
[6.7 3.3 5.7 2.1]
[7.2 3.2 6.  1.8]
[6.2 2.8 4.8 1.8]
[6.1 3.  4.9 1.8]
[6.4 2.8 5.6 2.1]
[7.2 3.  5.8 1.6]
[7.4 2.8 6.1 1.9]
[7.9 3.8 6.4 2. ]
[6.4 2.8 5.6 2.2]
[6.3 2.8 5.1 1.5]
[6.1 2.6 5.6 1.4]
[7.7 3.  6.1 2.3]
[6.3 3.4 5.6 2.4]
[6.4 3.1 5.5 1.8]
[6.  3.  4.8 1.8]
[6.9 3.1 5.4 2.1]
[6.7 3.1 5.6 2.4]
[6.9 3.1 5.1 2.3]
[5.8 2.7 5.1 1.9]
[6.8 3.2 5.9 2.3]
[6.7 3.3 5.7 2.5]
[6.7 3.  5.2 2.3]
[6.3 2.5 5.  1.9]
[6.5 3.  5.2 2. ]
[6.2 3.4 5.4 2.3]
[5.9 3.  5.1 1.8]
Cluster:  1
[5.1 3.5 1.4 0.2]
[4.9 3.  1.4 0.2]
[4.7 3.2 1.3 0.2]
[4.6 3.1 1.5 0.2]
[5.  3.6 1.4 0.2]
[5.4 3.9 1.7 0.4]
[4.6 3.4 1.4 0.3]
[5.  3.4 1.5 0.2]
[4.4 2.9 1.4 0.2]
[4.9 3.1 1.5 0.1]
[5.4 3.7 1.5 0.2]
[4.8 3.4 1.6 0.2]
[4.8 3.  1.4 0.1]
[4.3 3.  1.1 0.1]
[5.8 4.  1.2 0.2]
[5.7 4.4 1.5 0.4]
[5.4 3.9 1.3 0.4]
[5.1 3.5 1.4 0.3]
[5.7 3.8 1.7 0.3]
[5.1 3.8 1.5 0.3]
[5.4 3.4 1.7 0.2]
[5.1 3.7 1.5 0.4]
[4.6 3.6 1.  0.2]
[5.1 3.3 1.7 0.5]
[4.8 3.4 1.9 0.2]
[5.  3.  1.6 0.2]
[5.  3.4 1.6 0.4]
[5.2 3.5 1.5 0.2]
[5.2 3.4 1.4 0.2]
[4.7 3.2 1.6 0.2]
[4.8 3.1 1.6 0.2]
[5.4 3.4 1.5 0.4]
[5.2 4.1 1.5 0.1]
[5.5 4.2 1.4 0.2]
[4.9 3.1 1.5 0.1]
[5.  3.2 1.2 0.2]
[5.5 3.5 1.3 0.2]
[4.9 3.1 1.5 0.1]
[4.4 3.  1.3 0.2]
[5.1 3.4 1.5 0.2]
[5.  3.5 1.3 0.3]
[4.5 2.3 1.3 0.3]
[4.4 3.2 1.3 0.2]
[5.  3.5 1.6 0.6]
[5.1 3.8 1.9 0.4]
[4.8 3.  1.4 0.3]
[5.1 3.8 1.6 0.2]
[4.6 3.2 1.4 0.2]
[5.3 3.7 1.5 0.2]
[5.  3.3 1.4 0.2]
Cluster:  2
[5.5 2.3 4.  1.3]
[5.7 2.8 4.5 1.3]
[4.9 2.4 3.3 1. ]
[5.2 2.7 3.9 1.4]
[5.  2.  3.5 1. ]
[5.9 3.  4.2 1.5]
[6.  2.2 4.  1. ]
[5.6 2.9 3.6 1.3]
[5.6 3.  4.5 1.5]
[5.8 2.7 4.1 1. ]
[5.6 2.5 3.9 1.1]
[6.1 2.8 4.  1.3]
[5.7 2.6 3.5 1. ]
[5.5 2.4 3.8 1.1]
[5.5 2.4 3.7 1. ]
[5.8 2.7 3.9 1.2]
[5.4 3.  4.5 1.5]
[5.6 3.  4.1 1.3]
[5.5 2.5 4.  1.3]
[5.5 2.6 4.4 1.2]
[5.8 2.6 4.  1.2]
[5.  2.3 3.3 1. ]
[5.6 2.7 4.2 1.3]
[5.7 3.  4.2 1.2]
[5.7 2.9 4.2 1.3]
[5.1 2.5 3.  1.1]
[5.7 2.8 4.1 1.3]
[4.9 2.5 4.5 1.7]
```
