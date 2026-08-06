---
entry_id: "k-nn-para-regressao-exemplo-imc"
title: "K-NN para Regressão exemplo IMC"
language: "jupyter"
category: "codigo-professor"
unit: ""
source: "raw/code/professor/k-nn-para-regressao-exemplo-imc.ipynb"
---
# K-NN para Regressão exemplo IMC

> **Linguagem:** jupyter

## Célula 1 — Markdown

**Exemplo de uso do k-NN para regressão**

Predição do IMC

Profa Sílvia Moraes  20/08/2025

## Célula 2 — Código

```python
import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.neighbors import KNeighborsRegressor
from sklearn.metrics import mean_squared_error, r2_score
from sklearn.model_selection import train_test_split
import matplotlib.pyplot as plt
import numpy as np
```

## Célula 3 — Markdown

Carga dos dados do arquivo Cardio

## Célula 4 — Código

```python
cardio = pd.read_csv('cardio_train.csv', sep=";")
cardio.shape
```

**Saída:**

```text
(70000, 13)
```

## Célula 5 — Markdown

Convertendo a idade para anos e criando a coluna imc

## Célula 6 — Código

```python
cardio["idade_anos"] = cardio["age"] // 365
```

## Célula 7 — Código

```python
cardio["imc"] = cardio["weight"] / (cardio["height"] / 100) ** 2
```

## Célula 8 — Markdown

Excluindo colunas desnecessárias

## Célula 9 — Código

```python
X = cardio.drop(columns=["cardio","id","age","active","alco","ap_hi","ap_lo","cholesterol","gluc","smoke","imc"])
X.head()
```

**Saída:**

```text
gender  height  weight  idade_anos
0       2     168    62.0          50
1       1     156    85.0          55
2       1     165    64.0          51
3       2     169    82.0          48
4       1     156    56.0          47
```

## Célula 10 — Código

```python
y = cardio["imc"].values
print(y)
```

**Saída:**

```text
[21.96712018 34.92767916 23.50780533 ... 31.35357879 27.09925101
 24.91349481]
```

## Célula 11 — Markdown

Separando treino e teste

## Célula 12 — Código

```python
X_train, X_test, y_train, y_test = train_test_split(
    X, y,
    test_size=0.01,
    random_state=42
)
```

## Célula 13 — Código

```python
print("X_train:", X_train.shape)
print("X_test:", X_test.shape)
print("y_train:", y_train.shape)
print("y_test:", y_test.shape)
```

**Saída:**

```text
X_train: (69300, 4)
X_test: (700, 4)
y_train: (69300,)
y_test: (700,)
```

## Célula 14 — Markdown

K-NN para Regressão

## Célula 15 — Código

```python
k = 5
clf = KNeighborsRegressor(n_neighbors=k)
clf.fit(X_train, y_train)
```

**Saída:**

```text
KNeighborsRegressor()
```

## Célula 16 — Markdown

Fazendo a predição para o conjunto de teste

## Célula 17 — Código

```python
y_pred = clf.predict(X_test)
```

## Célula 18 — Markdown

O coeficiente de determinação (r^2) mede o quanto do comportamento da variável dependente (alvo) é explicado pelo modelo em relação à média dessa variável. Varia de 0 a 1.
0 → o modelo não explica nada (igual a chutar a média).
1 → o modelo explica perfeitamente os dados (erro zero).
Em alguns casos pode ser negativo, o que significa que o modelo está pior do que simplesmente usar a média como predição.

O Erro Médio Quadrado (em inglês MSE – Mean Squared Error) é uma métrica usada para avaliar a qualidade de um modelo de regressão. O MSE calcula a média dos quadrados das diferenças entre os valores reais e preditos.

## Célula 19 — Markdown

Avaliando o resultado

## Célula 20 — Código

```python
mse = mean_squared_error(y_test, y_pred)
r2 = r2_score(y_test, y_pred)
print(f"Erro Quadrático Médio (MSE): {mse:.4f}")
print(f"Coeficiente de Determinação (R²): {r2:.4f}")
```

**Saída:**

```text
Erro Quadrático Médio (MSE): 0.0185
Coeficiente de Determinação (R²): 0.9993
```

## Célula 21 — Markdown

Alguns gráficos para comparar os resultados

## Célula 22 — Código

```python
plt.figure(figsize=(8,5))
plt.hist(y_test, bins=15, alpha=0.7, label="IMC", color="blue")
plt.hist(y_pred, bins=15, alpha=0.7, label="IMC - predito", color="red")
plt.xlabel("IMC")
plt.ylabel("Frequência")
plt.title("Distribuição ")
plt.legend()
plt.grid(True, linestyle="--", alpha=0.6)
plt.show()
```

**Saída:**

```text
<Figure size 800x500 with 1 Axes>
```

## Célula 23 — Código

```python
plt.figure(figsize=(8,5))
plt.plot(y_test, label="IMC", color="blue", marker="o", linestyle="-")
plt.plot(y_pred, label="IMC pred", color="red", marker="x", linestyle="--")
plt.xlabel("Dados")
plt.ylabel("IMC")
plt.title("Comparação")
plt.legend()
plt.grid(True, linestyle="--", alpha=0.6)
plt.show()
```

**Saída:**

```text
<Figure size 800x500 with 1 Axes>
```

## Célula 24 — Código

```python
plt.figure(figsize=(8,5))
plt.scatter(range(len(y_test)),y_test, label="IMC", color="blue", alpha=0.7, marker="o")
plt.scatter(range(len(y_pred)), y_pred, label="IMC pred", color="red", alpha=0.7, marker="x")
plt.xlabel("Amostras")
plt.ylabel("IMC")
plt.title("Dispersão de IMC")
plt.legend()
plt.grid(True, linestyle="--", alpha=0.6)
plt.show()
```

**Saída:**

```text
<Figure size 800x500 with 1 Axes>
```

> Notebook truncado: exibindo 24 de 25 células.
