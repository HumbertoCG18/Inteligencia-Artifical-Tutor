---
entry_id: "mlp-classificacao-inadimplencia-normalizacao-e-gridsearchcv"
title: "MLP Classificação - Inadimplência (normalização e GridSearchCV)"
language: "jupyter"
category: "codigo-professor"
unit: ""
source: "raw/code/professor/mlp-classificacao-inadimplencia-normalizacao-e-gridsearchcv.ipynb"
---
# MLP Classificação - Inadimplência (normalização e GridSearchCV)

> **Linguagem:** jupyter

## Célula 1 — Markdown

# **Redes Neurais: MultiLayer Perceptron (MLP)**
Sílvia Moraes
---
Neste exemplo usamos o **dataset Default of Credit Card Clients**, disponível em https://archive.ics.uci.edu/dataset/350/default+of+credit+card+clients

## Célula 2 — Código

```python
#importando os pacotes usados
import pandas as pd
from sklearn.neural_network import MLPClassifier
from sklearn.model_selection import train_test_split
from sklearn.metrics import confusion_matrix, ConfusionMatrixDisplay
from sklearn.metrics import accuracy_score
from sklearn.metrics import classification_report
from sklearn.preprocessing import MinMaxScaler, StandardScaler
from sklearn.model_selection import GridSearchCV
```

## Célula 3 — Markdown

Fazendo a carga do dataset

## Célula 4 — Código

```python
dados = pd.read_csv("inadimplencia.csv",sep=";")
```

## Célula 5 — Markdown

Selecionando as colunas numéricas para normalização

## Célula 6 — Código

```python
colunas_numericas = dados.select_dtypes(include=['int64', 'float64']).columns
#colunas_numericas = colunas_numericas.drop(["ID","SEX","EDUCATION","MARRIAGE","PAY_0","PAY_2","PAY_3","PAY_4","PAY_5","PAY_6","default payment next month"])
colunas_numericas = colunas_numericas.drop(["ID","default payment next month"])
print(colunas_numericas)
```

**Saída:**

```text
Index(['LIMIT_BAL', 'SEX', 'EDUCATION', 'MARRIAGE', 'AGE', 'PAY_0', 'PAY_2',
       'PAY_3', 'PAY_4', 'PAY_5', 'PAY_6', 'BILL_AMT1', 'BILL_AMT2',
       'BILL_AMT3', 'BILL_AMT4', 'BILL_AMT5', 'BILL_AMT6', 'PAY_AMT1',
       'PAY_AMT2', 'PAY_AMT3', 'PAY_AMT4', 'PAY_AMT5', 'PAY_AMT6'],
      dtype='object')
```

## Célula 7 — Markdown

Normalizando ...

## Célula 8 — Código

```python
scaler = MinMaxScaler()
dados[colunas_numericas] = scaler.fit_transform(dados[colunas_numericas])
dados.head()
```

**Saída:**

```text
ID  LIMIT_BAL  SEX  EDUCATION  MARRIAGE       AGE  PAY_0  PAY_2  PAY_3  \
0   1   0.010101  1.0   0.333333  0.333333  0.051724    0.4    0.4    0.1   
1   2   0.111111  1.0   0.333333  0.666667  0.086207    0.1    0.4    0.2   
2   3   0.080808  1.0   0.333333  0.666667  0.224138    0.2    0.2    0.2   
3   4   0.040404  1.0   0.333333  0.333333  0.275862    0.2    0.2    0.2   
4   5   0.040404  0.0   0.333333  0.333333  0.620690    0.1    0.2    0.1   

   PAY_4  ...  BILL_AMT4  BILL_AMT5  BILL_AMT6  PAY_AMT1  PAY_AMT2  PAY_AMT3  \
0    0.1  ...   0.160138   0.080648   0.260979  0.000000  0.000409  0.000000   
1    0.2  ...   0.163220   0.084074   0.263485  0.000000  0.000594  0.001116   
2    0.2  ...   0.173637   0.095470   0.272928  0.001738  0.000891  0.001116   
3    0.2  ...   0.186809   0.109363   0.283685  0.002290  0.001199  0.001339   
4    0.2  ...   0.179863   0.099633   0.275681  0.002290  0.021779  0.011160   

   PAY_AMT4  PAY_AMT5  PAY_AMT6  default payment next month  
0  0.000000  0.000000  0.000000                           1  
1  0.001610  0.000000  0.003783                           1  
2  0.001610  0.002345  0.009458                           0  
3  0.001771  0.002506  0.001892                           0  
4  0.014493  0.001615  0.001284                           0  

[5 rows x 25 columns]
```

## Célula 9 — Markdown

Separando dados de entrada

## Célula 10 — Código

```python
X = dados.drop(columns=["ID","default payment next month"])
X.head()
```

**Saída:**

```text
LIMIT_BAL  SEX  EDUCATION  MARRIAGE       AGE  PAY_0  PAY_2  PAY_3  PAY_4  \
0   0.010101  1.0   0.333333  0.333333  0.051724    0.4    0.4    0.1    0.1   
1   0.111111  1.0   0.333333  0.666667  0.086207    0.1    0.4    0.2    0.2   
2   0.080808  1.0   0.333333  0.666667  0.224138    0.2    0.2    0.2    0.2   
3   0.040404  1.0   0.333333  0.333333  0.275862    0.2    0.2    0.2    0.2   
4   0.040404  0.0   0.333333  0.333333  0.620690    0.1    0.2    0.1    0.2   

   PAY_5  ...  BILL_AMT3  BILL_AMT4  BILL_AMT5  BILL_AMT6  PAY_AMT1  PAY_AMT2  \
0    0.0  ...   0.086723   0.160138   0.080648   0.260979  0.000000  0.000409   
1    0.2  ...   0.087817   0.163220   0.084074   0.263485  0.000000  0.000594   
2    0.2  ...   0.093789   0.173637   0.095470   0.272928  0.001738  0.000891   
3    0.2  ...   0.113407   0.186809   0.109363   0.283685  0.002290  0.001199   
4    0.2  ...   0.106020   0.179863   0.099633   0.275681  0.002290  0.021779   

   PAY_AMT3  PAY_AMT4  PAY_AMT5  PAY_AMT6  
0  0.000000  0.000000  0.000000  0.000000  
1  0.001116  0.001610  0.000000  0.003783  
2  0.001116  0.001610  0.002345  0.009458  
3  0.001339  0.001771  0.002506  0.001892  
4  0.011160  0.014493  0.001615  0.001284  

[5 rows x 23 columns]
```

## Célula 11 — Markdown

Separando dados de saida

## Célula 12 — Código

```python
y = dados["default payment next month"].values
print(y)
```

**Saída:**

```text
[1 1 0 ... 1 1 1]
```

## Célula 13 — Markdown

Distribuição por classes

## Célula 14 — Código

```python
qtd = dados.groupby('default payment next month').size()
print("Total de amostras: ", len(dados))
print("Possibilidade de Inadimplência:  1 - Sim / 0 - Não")
print("Quantidade de amostras por classe:")
print(qtd)
```

**Saída:**

```text
Total de amostras:  30000
Possibilidade de Inadimplência:  1 - Sim / 0 - Não
Quantidade de amostras por classe:
default payment next month
0    23364
1     6636
dtype: int64
```

## Célula 15 — Markdown

Divisão dos conjuntos de treino e teste usando o método train_test_split. O conjunto de treino ficou com 80% dos dados e o restante, 20%, ficou para o conjunto de teste.

## Célula 16 — Código

```python
X_train, X_test, y_train, y_test = train_test_split(X, y, train_size=0.90, stratify=y, random_state=42)
print(X_train.shape, X_test.shape, y_train.shape, y_test.shape)
```

**Saída:**

```text
(27000, 23) (3000, 23) (27000,) (3000,)
```

## Célula 17 — Markdown

O GridSearchCV vai:


*   Treinar o mlp com todas as combinações de parâmetros.
*   Avaliar cada uma com validação cruzada (n vezes).

*   Armazenar os resultados.
*   Selecionar a melhor combinação de hiperparâmetros com base na métrica escolhida.

Parâmetros a serem testados:

## Célula 18 — Código

```python
param_grid = {
    'hidden_layer_sizes': [(5,), (10,), (15,)],
    'alpha': [0.001, 0.01],      # parâmetro de regularização L2 (evita overfitting penalizando pesos grandes).
    'learning_rate_init': [0.1, 0.2, 0.01]
}
```

## Célula 19 — Código

```python
mlp = MLPClassifier(solver='adam',hidden_layer_sizes= 10, random_state=42, verbose=True)
grid = GridSearchCV(mlp, param_grid, scoring='neg_mean_squared_error', cv=5)
grid.fit(X_train, y_train)
```

**Saída:**

```text
Iteration 1, loss = 0.48554761
Iteration 2, loss = 0.46966379
Iteration 3, loss = 0.46587343
Iteration 4, loss = 0.46669152
Iteration 5, loss = 0.46595454
Iteration 6, loss = 0.46493273
Iteration 7, loss = 0.46687396
Iteration 8, loss = 0.46474370
Iteration 9, loss = 0.46848392
Iteration 10, loss = 0.46546773
Iteration 11, loss = 0.46658255
Iteration 12, loss = 0.46586889
Iteration 13, loss = 0.46422831
Iteration 14, loss = 0.46523772
Iteration 15, loss = 0.46715033
Iteration 16, loss = 0.46775066
Iteration 17, loss = 0.46163545
Iteration 18, loss = 0.45550804
Iteration 19, loss = 0.45284540
Iteration 20, loss = 0.45277545
Iteration 21, loss = 0.44724175
Iteration 22, loss = 0.44910621
Iteration 23, loss = 0.44800361
Iteration 24, loss = 0.44874611
Iteration 25, loss = 0.44708379
Iteration 26, loss = 0.44699288
Iteration 27, loss = 0.44597520
Iteration 28, loss = 0.44585173
Iteration 29, loss = 0.44559097
Iteration 30, loss = 0.44745635
Iteration 31, loss = 0.44402695
Iteration 32, loss = 0.44468646
Iteration 33, loss = 0.44821879
Iteration 34, loss = 0.44804971
Iteration 35, loss = 0.44548803
Iteration 36, loss = 0.44505555
Iteration 37, loss = 0.44525153
Iteration 38, loss = 0.44538439
Iteration 39, loss = 0.44596218
Iteration 40, loss = 0.44456294
Iteration 41, loss = 0.44631260
Iteration 42, loss = 0.44603631
Training loss did not improve more than tol=0.000100 for 10 consecutive epochs. Stopping.
Iteration 1, loss = 0.48930021
Iteration 2, loss = 0.46861916
Iteration 3, loss = 0.46554358
Iteration 4, loss = 0.47003454
Iteration 5, loss = 0.46517905
Iteration 6, loss = 0.46579387
Iteration 7, loss = 0.46547849
Iteration 8, loss = 0.46541943
Iteration 9, loss = 0.46567943
Iteration 10, loss = 0.46542973
Iteration 11, loss = 0.46754602
Iteration 12, loss = 0.46495858
Iteration 13, loss = 0.46380115
Iteration 14, loss = 0.46485568
Iteration 15, loss = 0.46679729
Iteration 16, loss = 0.46912604
Iteration 17, loss = 0.46636804
Iteration 18, loss = 0.46652502
Iteration 19, loss = 0.46468237
Iteration 20, loss = 0.46629855
Iteration 21, loss = 0.46616924
Iteration 22, loss = 0.46555465
Iteration 23, loss = 0.46591632
Iteration 24, loss = 0.46775794
Training loss did not improve more than tol=0.000100 for 10 consecutive epochs. Stopping.
Iteration 1, loss = 0.48950341
Iteration 2, loss = 0.47029030
Iteration 3, loss = 0.46886695
Iteration 4, loss = 0.47127519
Iteration 5, loss = 0.46816006
Iteration 6, loss = 0.46753985
Iteration 7, loss = 0.46890553
Iteration 8, loss = 0.46749861
Iteration 9, loss = 0.46855377
Iteration 10, loss = 0.46654268
Iteration 11, loss = 0.47318634
Iteration 12, loss = 0.46762933
Iteration 13, loss = 0.46751481
Iteration 14, loss = 0.46738996
Iteration 15, loss = 0.46856894
Iteration 16, loss = 0.47212384
Iteration 17, loss = 0.46786714
Iteration 18, loss = 0.47198283
Iteration 19, loss = 0.46696145
Iterat
```

## Célula 20 — Código

```python
print("Melhor configuração:", grid.best_params_)
print("Melhor acurácia:", grid.best_score_)
```

## Célula 21 — Código

```python
melhor_modelo = grid.best_estimator_
y_predicao = melhor_modelo.predict(X_train)


print("Possibilidade de Inadimplência:  1 - Sim / 0 - Não")
nomes_classes = ["Não","Sim"]
cm = confusion_matrix(y_train, y_predicao)
disp = ConfusionMatrixDisplay(confusion_matrix=cm)
disp = ConfusionMatrixDisplay(confusion_matrix=cm, display_labels=nomes_classes)
disp.plot(cmap='Blues')
```

## Célula 22 — Código

```python
melhor_modelo = grid.best_estimator_
y_predicao = melhor_modelo.predict(X_test)


print("Possibilidade de Inadimplência:  1 - Sim / 0 - Não")
nomes_classes = ["Não","Sim"]
cm = confusion_matrix(y_test, y_predicao)
disp = ConfusionMatrixDisplay(confusion_matrix=cm)
disp = ConfusionMatrixDisplay(confusion_matrix=cm, display_labels=nomes_classes)
disp.plot(cmap='Blues')
```

## Célula 23 — Markdown

No trecho abaixo, mostramos a forma de cálculo da acurácia. E também executamos o método accuracy_score que igualmente calcula a acurácia. Executando ainda o método classification_report que calcula as métricas conhecidas precision, recall e f-measure.

## Célula 24 — Código

```python
acerto = 0
for i in range(0, len(y_predicao)):
  if y_predicao[i]==y_test[i]: acerto = acerto + 1

print("Acuracia: ", acerto/len(y_predicao))
print(accuracy_score(y_test, y_predicao))
print(classification_report(y_test, y_predicao))
```

> Notebook truncado: exibindo 24 de 26 células.
