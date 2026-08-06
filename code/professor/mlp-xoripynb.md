---
entry_id: "mlp-xoripynb"
title: "MLP - XOR.ipynb"
language: "jupyter"
category: "codigo-professor"
unit: ""
source: "raw/code/professor/mlp-xoripynb.ipynb"
---
# MLP - XOR.ipynb

> **Linguagem:** jupyter

## Célula 1 — Código

```python
from sklearn.neural_network import MLPClassifier
```

## Célula 2 — Código

```python
X = [[0, 0], [0, 1],[1,0],[1,1]]
y = [[1,0],[0,1],[0,1],[1,0]]
```

## Célula 3 — Código

```python
clf = MLPClassifier(solver='adam', hidden_layer_sizes=(2,), learning_rate_init=0.3, momentum=0.2, verbose=True)
clf.fit(X, y)
```

**Saída:**

```text
Iteration 1, loss = 1.49975253
Iteration 2, loss = 1.41656375
Iteration 3, loss = 1.33923761
Iteration 4, loss = 1.27016748
Iteration 5, loss = 1.22036770
Iteration 6, loss = 1.16742789
Iteration 7, loss = 1.11207224
Iteration 8, loss = 1.05307606
Iteration 9, loss = 0.93646708
Iteration 10, loss = 0.83684891
Iteration 11, loss = 0.72818068
Iteration 12, loss = 0.66626729
Iteration 13, loss = 0.57068094
Iteration 14, loss = 0.51758841
Iteration 15, loss = 0.42057376
Iteration 16, loss = 0.38302895
Iteration 17, loss = 0.31320781
Iteration 18, loss = 0.24406861
Iteration 19, loss = 0.21600395
Iteration 20, loss = 0.18445732
Iteration 21, loss = 0.15270967
Iteration 22, loss = 0.12430715
Iteration 23, loss = 0.10326785
Iteration 24, loss = 0.08496410
Iteration 25, loss = 0.06716929
Iteration 26, loss = 0.05566845
Iteration 27, loss = 0.04870359
Iteration 28, loss = 0.04264643
Iteration 29, loss = 0.03669775
Iteration 30, loss = 0.03133771
Iteration 31, loss = 0.02711277
Iteration 32, loss = 0.02404678
Iteration 33, loss = 0.02230093
Iteration 34, loss = 0.02066206
Iteration 35, loss = 0.01850656
Iteration 36, loss = 0.01623845
Iteration 37, loss = 0.01477934
Iteration 38, loss = 0.01377556
Iteration 39, loss = 0.01297959
Iteration 40, loss = 0.01229444
Iteration 41, loss = 0.01166017
Iteration 42, loss = 0.01105303
Iteration 43, loss = 0.01047504
Iteration 44, loss = 0.00994023
Iteration 45, loss = 0.00946292
Iteration 46, loss = 0.00905106
Iteration 47, loss = 0.00870422
Iteration 48, loss = 0.00841469
Iteration 49, loss = 0.00816989
Iteration 50, loss = 0.00795553
Iteration 51, loss = 0.00775888
Iteration 52, loss = 0.00757137
Iteration 53, loss = 0.00738965
Iteration 54, loss = 0.00721459
Iteration 55, loss = 0.00704922
Iteration 56, loss = 0.00689660
Iteration 57, loss = 0.00675848
Iteration 58, loss = 0.00663498
Iteration 59, loss = 0.00652489
Iteration 60, loss = 0.00642623
Iteration 61, loss = 0.00633670
Iteration 62, loss = 0.00625418
Iteration 63, loss = 0.00617688
Iteration 64, loss = 0.00610349
Iteration 65, loss = 0.00604002
Iteration 66, loss = 0.00598043
Iteration 67, loss = 0.00592348
Iteration 68, loss = 0.00586893
Iteration 69, loss = 0.00581655
Iteration 70, loss = 0.00576658
Training loss did not improve more than tol=0.000100 for 10 consecutive epochs. Stopping.

MLPClassifier(hidden_layer_sizes=(2,), learning_rate_init=0.3, momentum=0.2,
              verbose=True)
```

## Célula 4 — Código

```python
clf.predict(X)
```

**Saída:**

```text
array([[1, 0],
       [0, 1],
       [0, 1],
       [1, 0]])
```

## Célula 5 — Código

```python
print("Classes: ", clf.classes_ )
print("Melhor loss: ", clf.best_loss_)
print(clf.coefs_)
print(clf.intercepts_)
print(clf.get_params)
```

**Saída:**

```text
Classes:  [0 1]
Melhor loss:  0.005766583958948901
[array([[3.82822162, 4.17666043],
       [3.83844673, 4.23667175]]), array([[ 7.6379815 , -7.3627816 ],
       [-3.17664541,  3.05828147]])]
[array([-3.84202347, -0.08340061]), array([ 5.32865473, -5.20663665])]
<bound method BaseEstimator.get_params of MLPClassifier(hidden_layer_sizes=(2,), learning_rate_init=0.3, momentum=0.2,
              verbose=True)>
```
