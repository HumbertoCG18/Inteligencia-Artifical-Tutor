---
entry_id: "agrupamento-usando-k-means-exemplo-2-ipynb"
title: "agrupamento usando k-Means exemplo 2 (.ipynb)"
language: "jupyter"
category: "codigo-professor"
unit: ""
source: "raw/code/professor/agrupamento-usando-k-means-exemplo-2-ipynb.ipynb"
---
# agrupamento usando k-Means exemplo 2 (.ipynb)

> **Linguagem:** jupyter

## Célula 1 — Markdown

# **Aula 02 - Aprendizado não Supervisionado: agrupamento com k-Means** - Exemplo 2
Sílvia Moraes
---

Exemplo 2: Neste exemplo, a aplicação do algoritmo de agrupamento k-Means é feita sobre o  **dataset da Planta IRIS**. Usamos o pacote KMeans do sklearn na implementação.

## Célula 2 — Código

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
from sklearn.cluster import KMeans
from sklearn.metrics import silhouette_score
from sklearn.preprocessing import MinMaxScaler
```

## Célula 3 — Markdown

Fazendo a carga dos dados da planta IRIS sem a informação de classe.

## Célula 4 — Código

```python
iris = pd.read_csv("IRIS.csv")
x = iris.iloc[:, [0, 1, 2, 3]].values
```

## Célula 5 — Markdown

**Explorando os dados do dataset da Planta IRIS**

Informações sobre atributos e classes.

## Célula 6 — Código

```python
iris.info()
iris[0:10]
```

**Saída:**

```text
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 150 entries, 0 to 149
Data columns (total 5 columns):
 #   Column        Non-Null Count  Dtype  
---  ------        --------------  -----  
 0   sepal_length  150 non-null    float64
 1   sepal_width   150 non-null    float64
 2   petal_length  150 non-null    float64
 3   petal_width   150 non-null    float64
 4   species       150 non-null    object 
dtypes: float64(4), object(1)
memory usage: 6.0+ KB

sepal_length  sepal_width  petal_length  petal_width      species
0           5.1          3.5           1.4          0.2  Iris-setosa
1           4.9          3.0           1.4          0.2  Iris-setosa
2           4.7          3.2           1.3          0.2  Iris-setosa
3           4.6          3.1           1.5          0.2  Iris-setosa
4           5.0          3.6           1.4          0.2  Iris-setosa
5           5.4          3.9           1.7          0.4  Iris-setosa
6           4.6          3.4           1.4          0.3  Iris-setosa
7           5.0          3.4           1.5          0.2  Iris-setosa
8           4.4          2.9           1.4          0.2  Iris-setosa
9           4.9          3.1           1.5          0.1  Iris-setosa
```

## Célula 7 — Markdown

Informações sobre a distribuição das classes:

## Célula 8 — Código

```python
#Distribuição das classes
iris_outcome = pd.crosstab(index=iris["species"],   # Make a crosstab
                              columns="count")      # Name the count column

iris_outcome
```

**Saída:**

```text
col_0            count
species               
Iris-setosa         50
Iris-versicolor     50
Iris-virginica      50
```

## Célula 9 — Markdown

Segmentando os dados por classe para viabilizar a visualização.

## Célula 10 — Código

```python
iris_setosa=iris.loc[iris["species"]=="Iris-setosa"]
iris_virginica=iris.loc[iris["species"]=="Iris-virginica"]
iris_versicolor=iris.loc[iris["species"]=="Iris-versicolor"]
```

## Célula 11 — Markdown

Gráficos para Análise do dataset da planta IRIS.  Análise comparativa por atributos.

## Célula 12 — Código

```python
sns.set_style("whitegrid")
sns.pairplot(iris,hue="species",height=3);
plt.show()
```

**Saída:**

```text
<Figure size 1343x1200 with 20 Axes>
```

## Célula 13 — Markdown

Usando a **Inércia** para estimar o valor de **k** pelo ***método do cotovelo***.

## Célula 14 — Código

```python
#Estimando o valor de k.
wcss = []

for i in range(1, 11):
    kmeans = KMeans(n_clusters = i, init = 'k-means++', max_iter = 300, n_init = 10, random_state = 0)
    kmeans.fit(x)
    wcss.append(kmeans.inertia_)
```

## Célula 15 — Markdown

Plotando os resultados para poder aplicar o método do cotovelo. O melhor valor de k, ele estimou entre 2 e 4, apontando para 3.

## Célula 16 — Código

```python
plt.plot(range(1, 11), wcss)
plt.title('The elbow method (Método do Cotovelo)')
plt.xlabel('Número de Clusters (K)')
plt.ylabel('WCSS') #within cluster sum of squares
plt.show()
```

**Saída:**

```text
<Figure size 640x480 with 1 Axes>
```

## Célula 17 — Markdown

Aplicando kMeans para k=3.

## Célula 18 — Código

```python
kmeans = KMeans(n_clusters = 3, init = 'k-means++', max_iter = 300, n_init = 10, random_state = 0)
y_kmeans = kmeans.fit_predict(x)
```

## Célula 19 — Markdown

Visualizando centróides e labels.

## Célula 20 — Código

```python
C = kmeans.cluster_centers_
labels = kmeans.labels_
print("Centroides:\n", C)
print("Cluster de cada cada:\n", labels)
```

**Saída:**

```text
Centroides:
 [[5.9016129  2.7483871  4.39354839 1.43387097]
 [5.006      3.418      1.464      0.244     ]
 [6.85       3.07368421 5.74210526 2.07105263]]
Cluster de cada cada:
 [1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1
 1 1 1 1 1 1 1 1 1 1 1 1 1 0 0 2 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
 0 0 0 2 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 2 0 2 2 2 2 0 2 2 2 2
 2 2 0 0 2 2 2 2 0 2 0 2 0 2 2 0 0 2 2 2 2 2 0 2 2 2 2 0 2 2 2 0 2 2 2 0 2
 2 0]
```

## Célula 21 — Markdown

Visualizando os dados por cluster.

## Célula 22 — Código

```python
k=3
for iCluster in range(0, k):
  print("Cluster: ", iCluster)
  print("Centroide: ", C[iCluster])
  for indice in range(0, len(labels)):
    if(iCluster==labels[indice]):
      print(x[indice])
```

**Saída:**

```text
Cluster:  0
Centroide:  [5.9016129  2.7483871  4.39354839 1.43387097]
[7.  3.2 4.7 1.4]
[6.4 3.2 4.5 1.5]
[5.5 2.3 4.  1.3]
[6.5 2.8 4.6 1.5]
[5.7 2.8 4.5 1.3]
[6.3 3.3 4.7 1.6]
[4.9 2.4 3.3 1. ]
[6.6 2.9 4.6 1.3]
[5.2 2.7 3.9 1.4]
[5.  2.  3.5 1. ]
[5.9 3.  4.2 1.5]
[6.  2.2 4.  1. ]
[6.1 2.9 4.7 1.4]
[5.6 2.9 3.6 1.3]
[6.7 3.1 4.4 1.4]
[5.6 3.  4.5 1.5]
[5.8 2.7 4.1 1. ]
[6.2 2.2 4.5 1.5]
[5.6 2.5 3.9 1.1]
[5.9 3.2 4.8 1.8]
[6.1 2.8 4.  1.3]
[6.3 2.5 4.9 1.5]
[6.1 2.8 4.7 1.2]
[6.4 2.9 4.3 1.3]
[6.6 3.  4.4 1.4]
[6.8 2.8 4.8 1.4]
[6.  2.9 4.5 1.5]
[5.7 2.6 3.5 1. ]
[5.5 2.4 3.8 1.1]
[5.5 2.4 3.7 1. ]
[5.8 2.7 3.9 1.2]
[6.  2.7 5.1 1.6]
[5.4 3.  4.5 1.5]
[6.  3.4 4.5 1.6]
[6.7 3.1 4.7 1.5]
[6.3 2.3 4.4 1.3]
[5.6 3.  4.1 1.3]
[5.5 2.5 4.  1.3]
[5.5 2.6 4.4 1.2]
[6.1 3.  4.6 1.4]
[5.8 2.6 4.  1.2]
[5.  2.3 3.3 1. ]
[5.6 2.7 4.2 1.3]
[5.7 3.  4.2 1.2]
[5.7 2.9 4.2 1.3]
[6.2 2.9 4.3 1.3]
[5.1 2.5 3.  1.1]
[5.7 2.8 4.1 1.3]
[5.8 2.7 5.1 1.9]
[4.9 2.5 4.5 1.7]
[5.7 2.5 5.  2. ]
[5.8 2.8 5.1 2.4]
[6.  2.2 5.  1.5]
[5.6 2.8 4.9 2. ]
[6.3 2.7 4.9 1.8]
[6.2 2.8 4.8 1.8]
[6.1 3.  4.9 1.8]
[6.3 2.8 5.1 1.5]
[6.  3.  4.8 1.8]
[5.8 2.7 5.1 1.9]
[6.3 2.5 5.  1.9]
[5.9 3.  5.1 1.8]
Cluster:  1
Centroide:  [5.006 3.418 1.464 0.244]
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
Centroide:  [6.85       3.07368421 5.74210526 2.07105263]
[6.9 3.1 4.9 1.5]
[6.7 3.  5.  1.7]
[6.3 3.3 6.  2.5]
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
[6.4 3.2 5.3 2.3]
[6.5 3.  5.5 1.8]
[7.7 3.8 6.7 2.2]
[7.7 2.6 6.9 2.3]
[6.9 3.2 5.7 2.3]
[7.7 2.8 6.7 2. ]
[6.7 3.3 5.7 2.1]
[7.2 3.2 6.  1.8]
[6.4 2.8 5.6 2.1]
[7.2 3.  5.8 1.6]
[7.4 2.8 6.1 1.9]
[7.9 3.8 6.4 2. ]
[6.4 2.8 5.6 2.2]
[6.1 2.6 5.6 1.4]
[7.7 3.  6.1 2.3]
[6.3 3.4 5.6 2.4]
[6.4 3.1 5.5 1.8]
[6.9 3.1 5.4 2.1]
[6.7 3.1 5.6 2.4]
[6.9 3.1 5.1 2.3]
[6.8 3.2 5.9 2.3]
[6.7 3.3 5.7 2.5]
[6.7 3.  5.2 2.3]
[6.5 3.  5.2 2. ]
[6.2 3.4 5.4 2.3]
```

## Célula 23 — Markdown

Plotando os grupos e os centróides.

## Célula 24 — Código

```python
#Visualising the clusters
plt.scatter(x[y_kmeans == 0, 0], x[y_kmeans == 0, 1], s = 100, c = 'purple', label = 'Iris-setosa')
plt.scatter(x[y_kmeans == 1, 0], x[y_kmeans == 1, 1], s = 100, c = 'orange', label = 'Iris-versicolour')
plt.scatter(x[y_kmeans == 2, 0], x[y_kmeans == 2, 1], s = 100, c = 'green', label = 'Iris-virginica')

#Plotting the centroids of the clusters
plt.scatter(kmeans.cluster_centers_[:, 0], kmeans.cluster_centers_[:,1], s = 100, c = 'red', label = 'Centroids')
plt.legend()
```

**Saída:**

```text
<matplotlib.legend.Legend at 0x7c391e52d210>

<Figure size 640x480 with 1 Axes>
```
