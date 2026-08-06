---
entry_id: "k-nn-para-classificacao-exemplo-cardio"
title: "K-NN para Classificação Exemplo Cardio"
language: "jupyter"
category: "codigo-professor"
unit: ""
source: "raw/code/professor/k-nn-para-classificacao-exemplo-cardio.ipynb"
---
# K-NN para Classificação Exemplo Cardio

> **Linguagem:** jupyter

## Célula 1 — Markdown

**Exemplo do k_NN para Classificação**

Arquivo Cardio

Profa Sílvia Moraes  20/08/2025

## Célula 2 — Código

```python
import pandas as pd
from sklearn import neighbors
from sklearn.model_selection import train_test_split
import matplotlib.pyplot as plt
```

## Célula 3 — Markdown

Carregando o arquivo sobre Cardio

## Célula 4 — Código

```python
cardio = pd.read_csv('cardio_train.csv', sep=";")
cardio.shape
```

**Saída:**

```text
(70000, 13)
```

## Célula 5 — Código

```python
cardio.describe()
```

**Saída:**

```text
id           age        gender        height        weight  \
count  70000.000000  70000.000000  70000.000000  70000.000000  70000.000000   
mean   49972.419900  19468.865814      1.349571    164.359229     74.205690   
std    28851.302323   2467.251667      0.476838      8.210126     14.395757   
min        0.000000  10798.000000      1.000000     55.000000     10.000000   
25%    25006.750000  17664.000000      1.000000    159.000000     65.000000   
50%    50001.500000  19703.000000      1.000000    165.000000     72.000000   
75%    74889.250000  21327.000000      2.000000    170.000000     82.000000   
max    99999.000000  23713.000000      2.000000    250.000000    200.000000   

              ap_hi         ap_lo   cholesterol          gluc         smoke  \
count  70000.000000  70000.000000  70000.000000  70000.000000  70000.000000   
mean     128.817286     96.630414      1.366871      1.226457      0.088129   
std      154.011419    188.472530      0.680250      0.572270      0.283484   
min     -150.000000    -70.000000      1.000000      1.000000      0.000000   
25%      120.000000     80.000000      1.000000      1.000000      0.000000   
50%      120.000000     80.000000      1.000000      1.000000      0.000000   
75%      140.000000     90.000000      2.000000      1.000000      0.000000   
max    16020.000000  11000.000000      3.000000      3.000000      1.000000   

               alco        active        cardio  
count  70000.000000  70000.000000  70000.000000  
mean       0.053771      0.803729      0.499700  
std        0.225568      0.397179      0.500003  
min        0.000000      0.000000      0.000000  
25%        0.000000      1.000000      0.000000  
50%        0.000000      1.000000      0.000000  
75%        0.000000      1.000000      1.000000  
max        1.000000      1.000000      1.000000
```

## Célula 6 — Markdown

Convertendo a idade para anos

## Célula 7 — Código

```python
cardio["idade_anos"] = cardio["age"] // 365
```

## Célula 8 — Markdown

Definindo as features de entrada (X), desprezando as colunas cardio, id e age

## Célula 9 — Código

```python
X = cardio.drop(columns=["cardio","id","age"])
X.head()
```

**Saída:**

```text
gender  height  weight  ap_hi  ap_lo  cholesterol  gluc  smoke  alco  \
0       2     168    62.0    110     80            1     1      0     0   
1       1     156    85.0    140     90            3     1      0     0   
2       1     165    64.0    130     70            3     1      0     0   
3       2     169    82.0    150    100            1     1      0     0   
4       1     156    56.0    100     60            1     1      0     0   

   active  idade_anos  
0       1          50  
1       1          55  
2       0          51  
3       1          48  
4       0          47
```

## Célula 10 — Markdown

Definindo a saida : Classe (y)

## Célula 11 — Código

```python
y = cardio["cardio"].values
print(y)
```

**Saída:**

```text
[0 1 1 ... 1 1 0]
```

## Célula 12 — Markdown

Dividindo o dataset em treino e teste

## Célula 13 — Código

```python
X_train, X_test, y_train, y_test = train_test_split(
    X, y,
    test_size=0.2,          # 20% para teste e 80% para treino
    stratify=y,             # garante estratificação: garante proporção
    random_state=42         # reprodutibilidade: garante a mesma divisão a cada execução
)
```

## Célula 14 — Markdown

Verificando as quantidades/distribuição

## Célula 15 — Código

```python
print(X_train.shape)
print(X_test.shape)
print(y_train.shape)
print(y_test.shape)
```

**Saída:**

```text
(56000, 11)
(14000, 11)
(56000,)
(14000,)
```

## Célula 16 — Markdown

Dando uma olhada no subset de treino

## Célula 17 — Código

```python
print(X_train.head())
print(y_train)
```

**Saída:**

```text
gender  height  weight  ap_hi  ap_lo  cholesterol  gluc  smoke  alco  \
58394       2     162    83.0    120     80            1     1      0     0   
60371       1     158    64.0    120     80            1     1      0     0   
41399       1     165    95.0    160    100            2     1      0     0   
11468       1     164    83.0    150    100            1     1      0     0   
20650       1     156    52.0    100     67            1     1      0     0   

       active  idade_anos  
58394       0          52  
60371       1          47  
41399       1          52  
11468       1          55  
20650       0          49  
[1 0 1 ... 1 1 1]
```

## Célula 18 — Markdown

Dando uma olhada no subset de teste

## Célula 19 — Código

```python
print(X_test.head())
print(y_test)
```

**Saída:**

```text
gender  height  weight  ap_hi  ap_lo  cholesterol  gluc  smoke  alco  \
18682       1     155    59.5    120     85            1     1      0     0   
40992       1     160    59.0    130     90            1     1      0     0   
38068       2     175    88.0    120     80            2     1      0     0   
12096       2     177    62.0    120     90            1     1      0     0   
17791       1     167    81.0    120     80            1     1      0     0   

       active  idade_anos  
18682       1          53  
40992       1          57  
38068       1          41  
12096       1          51  
17791       1          49  
[0 0 0 ... 0 1 1]
```

## Célula 20 — Markdown

Procurando o melhor valor de k para o algoritmo k-NN.
Usando a medida de acurácia. Ela mede a proporção de previsões corretas feitas pelo modelo em relação ao total de previsões.

## Célula 21 — Código

```python
k_values = []
accuracies = []
maior = 0
melhor_k = 2
for k in range(2, 30):
  clf = neighbors.KNeighborsClassifier(n_neighbors=k)
  clf.fit(X_train.values, y_train)
  print("k = ", k, "acuracia = ", clf.score(X_test.values, y_test))

  acertos = 0
  for i in range(0,len(X_test)):
    predicao = clf.predict([X_test.values[i]])
    #print(X_test.values[i], "predicao: ", predicao)
    if predicao == y_test[i]:
      acertos += 1
  acc = acertos / len(X_test)
  print("Acertos: ", acertos)
  print("Erros: ", len(X_test) - acertos)
  print("Acuracia: ", acc)
  k_values.append(k)
  accuracies.append(acc)
  if acc > maior:
    maior = acc
    melhor_k = k
print("Melhor k: ", melhor_k)
print("Maior acuracia: ", maior)
```

**Saída:**

```text
k =  2 acuracia =  0.6396428571428572
Acertos:  8955
Erros:  5045
Acuracia:  0.6396428571428572
k =  3 acuracia =  0.6742142857142858
```

## Célula 22 — Markdown

Plotando o valor do k e a acurácia correspondente

## Célula 23 — Código

```python
plt.plot(k_values, accuracies, marker="o")
plt.xlabel("Valor de k")
plt.ylabel("Acurácia")
plt.title("Acurácia x Valor de k (k-NN)")
plt.grid(True)
plt.show()
```

**Saída:**

```text
<Figure size 640x480 with 1 Axes>
```
