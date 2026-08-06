---
entry_id: "exemplo-com-k-nn"
title: "Exemplo com k-NN"
language: "jupyter"
category: "codigo-professor"
unit: ""
source: "raw/code/professor/exemplo-com-k-nn.ipynb"
---
# Exemplo com k-NN

> **Linguagem:** jupyter

## Célula 1 — Código

```python
import pandas as pd
from sklearn import neighbors
```

## Célula 2 — Código

```python
#iris = pd.read_csv('IRIS.csv')
iris = pd.read_csv('IRIS_train.csv')
iris.shape
```

**Saída:**

```text
(144, 5)
```

## Célula 3 — Código

```python
iris.describe()
```

**Saída:**

```text
sepal_length  sepal_width  petal_length  petal_width
count    144.000000   144.000000    144.000000   144.000000
mean       5.840278     3.050000      3.754861     1.195139
std        0.831489     0.439166      1.763017     0.759401
min        4.300000     2.000000      1.000000     0.100000
25%        5.100000     2.800000      1.600000     0.300000
50%        5.800000     3.000000      4.300000     1.300000
75%        6.400000     3.300000      5.100000     1.800000
max        7.900000     4.400000      6.900000     2.500000
```

## Célula 4 — Código

```python
iris.groupby
```

**Saída:**

```text
<bound method DataFrame.groupby of      sepal_length  sepal_width  petal_length  petal_width         species
0             4.7          3.2           1.3          0.2     Iris-setosa
1             4.6          3.1           1.5          0.2     Iris-setosa
2             5.0          3.6           1.4          0.2     Iris-setosa
3             5.4          3.9           1.7          0.4     Iris-setosa
4             4.6          3.4           1.4          0.3     Iris-setosa
..            ...          ...           ...          ...             ...
139           6.7          3.0           5.2          2.3  Iris-virginica
140           6.3          2.5           5.0          1.9  Iris-virginica
141           6.5          3.0           5.2          2.0  Iris-virginica
142           6.2          3.4           5.4          2.3  Iris-virginica
143           5.9          3.0           5.1          1.8  Iris-virginica

[144 rows x 5 columns]>
```

## Célula 5 — Código

```python
X = iris.drop(columns=["species"])
X.head()
```

**Saída:**

```text
sepal_length  sepal_width  petal_length  petal_width
0           4.7          3.2           1.3          0.2
1           4.6          3.1           1.5          0.2
2           5.0          3.6           1.4          0.2
3           5.4          3.9           1.7          0.4
4           4.6          3.4           1.4          0.3
```

## Célula 6 — Código

```python
y = iris["species"].values
print(y)
```

**Saída:**

```text
['Iris-setosa' 'Iris-setosa' 'Iris-setosa' 'Iris-setosa' 'Iris-setosa'
 'Iris-setosa' 'Iris-setosa' 'Iris-setosa' 'Iris-setosa' 'Iris-setosa'
 'Iris-setosa' 'Iris-setosa' 'Iris-setosa' 'Iris-setosa' 'Iris-setosa'
 'Iris-setosa' 'Iris-setosa' 'Iris-setosa' 'Iris-setosa' 'Iris-setosa'
 'Iris-setosa' 'Iris-setosa' 'Iris-setosa' 'Iris-setosa' 'Iris-setosa'
 'Iris-setosa' 'Iris-setosa' 'Iris-setosa' 'Iris-setosa' 'Iris-setosa'
 'Iris-setosa' 'Iris-setosa' 'Iris-setosa' 'Iris-setosa' 'Iris-setosa'
 'Iris-setosa' 'Iris-setosa' 'Iris-setosa' 'Iris-setosa' 'Iris-setosa'
 'Iris-setosa' 'Iris-setosa' 'Iris-setosa' 'Iris-setosa' 'Iris-setosa'
 'Iris-setosa' 'Iris-setosa' 'Iris-setosa' 'Iris-versicolor'
 'Iris-versicolor' 'Iris-versicolor' 'Iris-versicolor' 'Iris-versicolor'
 'Iris-versicolor' 'Iris-versicolor' 'Iris-versicolor' 'Iris-versicolor'
 'Iris-versicolor' 'Iris-versicolor' 'Iris-versicolor' 'Iris-versicolor'
 'Iris-versicolor' 'Iris-versicolor' 'Iris-versicolor' 'Iris-versicolor'
 'Iris-versicolor' 'Iris-versicolor' 'Iris-versicolor' 'Iris-versicolor'
 'Iris-versicolor' 'Iris-versicolor' 'Iris-versicolor' 'Iris-versicolor'
 'Iris-versicolor' 'Iris-versicolor' 'Iris-versicolor' 'Iris-versicolor'
 'Iris-versicolor' 'Iris-versicolor' 'Iris-versicolor' 'Iris-versicolor'
 'Iris-versicolor' 'Iris-versicolor' 'Iris-versicolor' 'Iris-versicolor'
 'Iris-versicolor' 'Iris-versicolor' 'Iris-versicolor' 'Iris-versicolor'
 'Iris-versicolor' 'Iris-versicolor' 'Iris-versicolor' 'Iris-versicolor'
 'Iris-versicolor' 'Iris-versicolor' 'Iris-versicolor' 'Iris-virginica'
 'Iris-virginica' 'Iris-virginica' 'Iris-virginica' 'Iris-virginica'
 'Iris-virginica' 'Iris-virginica' 'Iris-virginica' 'Iris-virginica'
 'Iris-virginica' 'Iris-virginica' 'Iris-virginica' 'Iris-virginica'
 'Iris-virginica' 'Iris-virginica' 'Iris-virginica' 'Iris-virginica'
 'Iris-virginica' 'Iris-virginica' 'Iris-virginica' 'Iris-virginica'
 'Iris-virginica' 'Iris-virginica' 'Iris-virginica' 'Iris-virginica'
 'Iris-virginica' 'Iris-virginica' 'Iris-virginica' 'Iris-virginica'
 'Iris-virginica' 'Iris-virginica' 'Iris-virginica' 'Iris-virginica'
 'Iris-virginica' 'Iris-virginica' 'Iris-virginica' 'Iris-virginica'
 'Iris-virginica' 'Iris-virginica' 'Iris-virginica' 'Iris-virginica'
 'Iris-virginica' 'Iris-virginica' 'Iris-virginica' 'Iris-virginica'
 'Iris-virginica' 'Iris-virginica' 'Iris-virginica']
```

## Célula 7 — Código

```python
clf = neighbors.KNeighborsClassifier(n_neighbors=5)

clf.fit(X.values, y)
```

**Saída:**

```text
KNeighborsClassifier()
```

## Célula 8 — Código

```python
#5.1,3.5,1.4,0.2,Iris-setosa
#4.9,3,1.4,0.2,Iris-setosa
#7,3.2,4.7,1.4,Iris-versicolor
#6.4,3.2,4.5,1.5,Iris-versicolor
#6.3,3.3,6,2.5,Iris-virginica
#5.8,2.7,5.1,1.9,Iris-virginica

X_test=[[5.1,3.5,1.4,0.2],
        [4.9,3,1.4,0.2],
        [7,3.2,4.7,1.4],
        [6.4,3.2,4.5,1.5],
        [6.3,3.3,6,2.5],
        [5.8,2.7,5.1,1.9]]

predicao = clf.predict(X_test)

for i in range(0,len(X_test)):
  print(X_test[i], "predicao: ", predicao[i])
```

**Saída:**

```text
[5.1, 3.5, 1.4, 0.2] predicao:  Iris-setosa
[4.9, 3, 1.4, 0.2] predicao:  Iris-setosa
[7, 3.2, 4.7, 1.4] predicao:  Iris-versicolor
[6.4, 3.2, 4.5, 1.5] predicao:  Iris-versicolor
[6.3, 3.3, 6, 2.5] predicao:  Iris-virginica
[5.8, 2.7, 5.1, 1.9] predicao:  Iris-virginica
```

## Célula 9 — Código

```python

```
