---
entry_id: "mlp-regressao-cardio"
title: "MLP Regressão - Cardio"
language: "jupyter"
category: "codigo-professor"
unit: ""
source: "raw/code/professor/mlp-regressao-cardio.ipynb"
---
# MLP Regressão - Cardio

> **Linguagem:** jupyter

## Célula 1 — Markdown

**Exemplo de uso do MLP para regressão**

Predição do IMC

Profa Sílvia Moraes  29/08/2025

## Célula 2 — Código

```python
import pandas as pd
from sklearn.neural_network import MLPRegressor
from sklearn.model_selection import train_test_split
from sklearn.metrics import mean_squared_error, r2_score
import matplotlib.pyplot as plt
```

## Célula 3 — Código

```python
cardio = pd.read_csv('cardio_train.csv', sep=";")
cardio.shape
```

**Saída:**

```text
(70000, 13)
```

## Célula 4 — Código

```python
cardio["idade_anos"] = cardio["age"] // 365
cardio["imc"] = cardio["weight"] / (cardio["height"] / 100) ** 2
```

## Célula 5 — Código

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

## Célula 6 — Código

```python
y = cardio["imc"].values
print(y)
```

**Saída:**

```text
[21.96712018 34.92767916 23.50780533 ... 31.35357879 27.09925101
 24.91349481]
```

## Célula 7 — Código

```python
# Dividir os dados em treino e teste
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.01, random_state=42)
```

## Célula 8 — Código

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

## Célula 9 — Código

```python
# Criar o modelo MLP para regressão
mlp = MLPRegressor(hidden_layer_sizes=(10,),
                   activation='logistic',
                   solver='adam',
                   learning_rate_init=0.001,
                   momentum=0.1,
                   max_iter=1000,
                   random_state=42,
                   verbose=True)
```

## Célula 10 — Código

```python
mlp.fit(X_train, y_train)
```

**Saída:**

```text
Iteration 1, loss = 347.64242301
Iteration 2, loss = 269.59537737
Iteration 3, loss = 193.01452556
Iteration 4, loss = 139.70132589
Iteration 5, loss = 102.62097562
Iteration 6, loss = 75.22166994
Iteration 7, loss = 55.20774376
Iteration 8, loss = 41.03050078
Iteration 9, loss = 31.31183046
Iteration 10, loss = 24.65166366
Iteration 11, loss = 19.91669969
Iteration 12, loss = 16.50430127
Iteration 13, loss = 14.03782440
Iteration 14, loss = 12.23971862
Iteration 15, loss = 10.93127200
Iteration 16, loss = 10.00656432
Iteration 17, loss = 9.12435721
Iteration 18, loss = 8.16344283
Iteration 19, loss = 7.56827568
Iteration 20, loss = 7.13364871
Iteration 21, loss = 6.81200429
Iteration 22, loss = 6.58070994
Iteration 23, loss = 6.41013764
Iteration 24, loss = 6.27381385
Iteration 25, loss = 5.97342961
Iteration 26, loss = 5.53644610
Iteration 27, loss = 5.31850925
Iteration 28, loss = 5.15832024
Iteration 29, loss = 5.03460776
Iteration 30, loss = 4.93691549
Iteration 31, loss = 4.86003282
Iteration 32, loss = 4.79563693
Iteration 33, loss = 4.71947928
Iteration 34, loss = 4.62715866
Iteration 35, loss = 4.55350731
Iteration 36, loss = 4.48802542
Iteration 37, loss = 4.43035773
Iteration 38, loss = 4.37282481
Iteration 39, loss = 4.31684508
Iteration 40, loss = 4.26440316
Iteration 41, loss = 4.21494577
Iteration 42, loss = 4.16302185
Iteration 43, loss = 4.11713501
Iteration 44, loss = 4.06686063
Iteration 45, loss = 4.01849864
Iteration 46, loss = 3.97421296
Iteration 47, loss = 3.92092846
Iteration 48, loss = 3.87599750
Iteration 49, loss = 3.82738197
Iteration 50, loss = 3.77667348
Iteration 51, loss = 3.72920673
Iteration 52, loss = 3.68072607
Iteration 53, loss = 3.62648891
Iteration 54, loss = 3.57642121
Iteration 55, loss = 3.52212496
Iteration 56, loss = 3.46852675
Iteration 57, loss = 3.42467596
Iteration 58, loss = 3.38641920
Iteration 59, loss = 3.34395111
Iteration 60, loss = 3.31078981
Iteration 61, loss = 3.27501108
Iteration 62, loss = 3.24090093
Iteration 63, loss = 3.20859392
Iteration 64, loss = 3.17618407
Iteration 65, loss = 3.14468116
Iteration 66, loss = 3.11653858
Iteration 67, loss = 3.08657215
Iteration 68, loss = 3.05823258
Iteration 69, loss = 3.03228042
Iteration 70, loss = 3.00306358
Iteration 71, loss = 2.97584293
Iteration 72, loss = 2.94984564
Iteration 73, loss = 2.92355914
Iteration 74, loss = 2.90007282
Iteration 75, loss = 2.87362532
Iteration 76, loss = 2.85033001
Iteration 77, loss = 2.82721210
Iteration 78, loss = 2.80232292
Iteration 79, loss = 2.78093067
Iteration 80, loss = 2.75807153
Iteration 81, loss = 2.73497249
Iteration 82, loss = 2.71371289
Iteration 83, loss = 2.69739048
Iteration 84, loss = 2.67368161
Iteration 85, loss = 2.65215810
Iteration 86, loss = 2.63079954
Iteration 87, loss = 2.61541863
Iteration 88, loss = 2.59260449
Iteration 89, loss = 2.57290795
Iteration 90, loss = 2.55332567
Iteration 91, loss = 2.53650514
Iteration 92, loss = 2.51719435
Iteration 93, loss = 2.49811943
Iteration 94, loss = 2.46924429
Iteration 95, loss = 2.44545274
Iteration 96, loss = 2.42303325
Iteration 97, loss = 2.39933715
Iteration 98, loss = 2.37826735
Iteration 99, loss = 2.35667569
Iteration 100, loss = 2.33453667
Iteration 101, loss = 2.31587276
Iteration 102, loss = 2.29248606
Iteration 103, loss = 2.27502158
Iteration 104, loss = 2.25493458
Iteration 105, loss = 2.23516109
Iteration 106, loss = 2.21499243
Iteration 107, loss = 2.19521840
Iteration 108, loss = 2.17539592
Iteration 109, loss = 2.15829651
Iteration 110, loss = 2.13897826
Iteration 111, loss = 2.12039298
Iteration 112, loss = 2.10570397
Iteration 113, loss = 2.08375070
Iteration 114, loss = 2.06869315
Iteration 115, loss = 2.04755691
Iteration 116, loss = 2.03125698
Iteration 117, loss = 2.01538326
Iteration 118, loss = 1.99722371
Iteration 119, loss = 1.98031249
Iteration 120, loss = 1.96453713
Iteration 121, loss = 1.94609100
Iteration 122, loss = 1.92916378
Iteration 123, loss = 1.91513849
Iteration 124, loss = 1.89805944
Iteration 125, loss = 1.88292579
Iteration 126, loss = 1.86951006
Iteration 127, loss = 1.85150799
Iteration 128, loss = 1.83536471
Iteration 129, loss = 1.81817723
Iteration 130, loss = 1.80490046
Iteration 131, loss = 1.78880344
Iteration 132, loss = 1.77355035
Iteration 133, loss = 1.75959683
Iteration 134, loss = 1.74491968
Iteration 135, loss = 1.73175735
Iteration 136, loss = 1.71497463
Iteration 137, loss = 1.69992059
Iteration 138, loss = 1.68987040
Iteration 139, loss = 1.67365777
Iteration 140, loss = 1.66125105
Iteration 141, loss = 1.64313117
Iteration 142, loss = 1.62966846
Iteration 143, loss = 1.61791420
Iteration 144, loss = 1.60182859
Iteration 145, loss = 1.59244270
Iteration 146, loss = 1.57744315
Iteration 147, loss = 1.56509618
Iteration 148, loss = 1.55038757
Iteration 149, loss = 1.53992968
Iteration 150, loss = 1.52649987
Iteration 151, loss = 1.51466131
Iteration 152, loss = 1.50180286
Iteration 153, loss = 1.48935775
Iteration 154, loss = 1.47699053
Iteration 155, loss = 1.46740581
Iteration 156, loss = 1.45200528
Iteration 157, loss = 1.44213647
Iteration 158, loss = 1.43057390
Iteration 159, loss = 1.41597630
Iteration 160, loss = 1.40814102
Iteration 161, loss = 1.39476784
Iteration 162, loss = 1.38218218
Iteration 163, loss = 1.36924804
Iteration 164, loss = 1.35933394
Iteration 165, loss = 1.34989229
Iteration 166, loss = 1.33960394
Iteration 167, loss = 1.32645629
Iteration 168, loss = 1.32083876
Iteration 169, loss = 1.30953626
Iteration 170, loss = 1.29767263
Iteration 171, loss = 1.28917933
Iteration 172, loss = 1.27582663
Iteration 173, loss = 1.26844
```

## Célula 11 — Código

```python
y_pred = mlp.predict(X_test)
```

## Célula 12 — Código

```python
mse = mean_squared_error(y_test, y_pred)
r2 = r2_score(y_test, y_pred)
print(f"Erro Quadrático Médio (MSE): {mse:.4f}")
print(f"Coeficiente de Determinação (R²): {r2:.4f}")
```

## Célula 13 — Código

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

## Célula 14 — Código

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

## Célula 15 — Código

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

## Célula 16 — Código

```python
# Ver número de camadas e neurônios
print("Camadas ocultas:", mlp.hidden_layer_sizes)
print("Camadas totais (incluindo entrada e saída):", len(mlp.coefs_) + 1)

# Pesos (coefs_) e bias (intercepts_)
for i, (w, b) in enumerate(zip(mlp.coefs_, mlp.intercepts_)):
    print(f"Camada {i} → {i+1}:")
    print(f"  Pesos: {w.shape}")  # shape: (neurônios_entrada, neurônios_saida)
    print(f"  Bias: {b.shape}")
```
