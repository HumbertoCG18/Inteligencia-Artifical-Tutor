---
entry_id: "rede-perceptron-classificacao-planta-iris"
title: "Rede Perceptron - Classificacao - Planta Iris"
language: "jupyter"
category: "codigo-professor"
unit: ""
source: "raw/code/professor/rede-perceptron-classificacao-planta-iris.ipynb"
---
# Rede Perceptron - Classificacao - Planta Iris

> **Linguagem:** jupyter

## Célula 1 — Código

```python
#Algoritmo de Treinamento do Perceptron
import pandas as pd
import numpy as np
import math

#Funcao de ativacao
def funcaoLimiar(v):
  if v>=0: return 1
  else: return 0

def funcaoLogistica(v):
  return 1/(1+ math.exp(-v))

def propagacao(entradaX,pesos):
  X= [1] + entradaX.copy()   #inclui Xo=1 referente ao bias
  v=0
  for i in range(0,len(pesos)):
    v = v + X[i] * pesos[i]
  return v
```

## Célula 2 — Código

```python
def algoritmoTreinamento(dados):
  epoca = 0
  eta = 1
  pesos = [[0,0,0,0,0], [0,0,0,0,0]]  #Sao dois neuronios

  print("Pesos iniciais: ", pesos)

  erroGeral = 1
  while erroGeral!=0 and epoca<=100:
    erroGeral = 0
    epoca = epoca + 1
    print("\n>>>>>>Epoca: ", epoca)

    for tupla in dados:
      entradaX = tupla.copy()
      classeY = entradaX.pop()
      print("Processando - Entrada: ", entradaX, "Classe: ", classeY)

      for j in range(0,len(pesos)):
        v = propagacao(entradaX,pesos[j])
        #y = funcaoLogistica(v)
        y = funcaoLimiar(v)
        erro = classeY[j] - y
        print('Erro neuronio', j,' = ', erro)

        if erro!=0:
          X = [1] + entradaX.copy()
          for i in range(0,len(pesos[j])):
            delta = eta * erro * X[i]
            pesos[j][i] = pesos[j][i] + delta

        print("Neuronio ", j , ":" , pesos[j])

        erroGeral = erroGeral + abs(erro)

    print("Pesos atuais: ", pesos)
    print('Erro Geral: ', erroGeral)

  return pesos
```

## Célula 3 — Código

```python
#Exemplo com a planta Iris
iris = pd.read_csv("IRIS.csv")
X = iris.iloc[:, [0, 1, 2, 3,4]].values
#print(X)
```

## Célula 4 — Código

```python
#Separando dados da planta Iris em Treino/Teste
dadosTreino = []
dadosTeste = []

setosa=[]
virginica = []
versicolor=[]

for tupla in X:
  if tupla[4]=='Iris-setosa':
    classe = [1,0]
    setosa.append([tupla[0],tupla[1],tupla[2],tupla[3],classe])
  else:
    classe = [0,1]
    if tupla[4]=='Iris-versicolor': versicolor.append([tupla[0],tupla[1],tupla[2],tupla[3],classe])
    else: virginica.append([tupla[0],tupla[1],tupla[2],tupla[3],classe])


#print('\nDados Setosa')
#for item in setosa:
#  print(item)

#print('\nDados Versicolor')
#for item in versicolor:
#  print(item)

#print('\nDados Virginica')
#for item in virginica:
#  print(item)

dadosTreino = []
for i in range(0,10):
  dadosTreino.append(setosa[i])
  dadosTreino.append(versicolor[i])
  dadosTreino.append(virginica[i])

dadosTeste = []
for i in range(11,13):
  dadosTeste.append(setosa[i])
  dadosTeste.append(versicolor[i])
  dadosTeste.append(virginica[i])

print('\nDados Treino')
for item in dadosTreino:
  print(item)

print('\nDados Teste')
for item in dadosTeste:
  print(item)
```

**Saída:**

```text
Dados Treino
[5.1, 3.5, 1.4, 0.2, [1, 0]]
[7.0, 3.2, 4.7, 1.4, [0, 1]]
[6.3, 3.3, 6.0, 2.5, [0, 1]]
[4.9, 3.0, 1.4, 0.2, [1, 0]]
[6.4, 3.2, 4.5, 1.5, [0, 1]]
[5.8, 2.7, 5.1, 1.9, [0, 1]]
[4.7, 3.2, 1.3, 0.2, [1, 0]]
[6.9, 3.1, 4.9, 1.5, [0, 1]]
[7.1, 3.0, 5.9, 2.1, [0, 1]]
[4.6, 3.1, 1.5, 0.2, [1, 0]]
[5.5, 2.3, 4.0, 1.3, [0, 1]]
[6.3, 2.9, 5.6, 1.8, [0, 1]]
[5.0, 3.6, 1.4, 0.2, [1, 0]]
[6.5, 2.8, 4.6, 1.5, [0, 1]]
[6.5, 3.0, 5.8, 2.2, [0, 1]]
[5.4, 3.9, 1.7, 0.4, [1, 0]]
[5.7, 2.8, 4.5, 1.3, [0, 1]]
[7.6, 3.0, 6.6, 2.1, [0, 1]]
[4.6, 3.4, 1.4, 0.3, [1, 0]]
[6.3, 3.3, 4.7, 1.6, [0, 1]]
[4.9, 2.5, 4.5, 1.7, [0, 1]]
[5.0, 3.4, 1.5, 0.2, [1, 0]]
[4.9, 2.4, 3.3, 1.0, [0, 1]]
[7.3, 2.9, 6.3, 1.8, [0, 1]]
[4.4, 2.9, 1.4, 0.2, [1, 0]]
[6.6, 2.9, 4.6, 1.3, [0, 1]]
[6.7, 2.5, 5.8, 1.8, [0, 1]]
[4.9, 3.1, 1.5, 0.1, [1, 0]]
[5.2, 2.7, 3.9, 1.4, [0, 1]]
[7.2, 3.6, 6.1, 2.5, [0, 1]]

Dados Teste
[4.8, 3.4, 1.6, 0.2, [1, 0]]
[5.9, 3.0, 4.2, 1.5, [0, 1]]
[6.4, 2.7, 5.3, 1.9, [0, 1]]
[4.8, 3.0, 1.4, 0.1, [1, 0]]
[6.0, 2.2, 4.0, 1.0, [0, 1]]
[6.8, 3.0, 5.5, 2.1, [0, 1]]
```

## Célula 5 — Código

```python
#Treinamento
w = algoritmoTreinamento(dadosTreino)
```

**Saída:**

```text
Pesos iniciais:  [[0, 0, 0, 0, 0], [0, 0, 0, 0, 0]]

>>>>>>Epoca:  1
Processando - Entrada:  [5.1, 3.5, 1.4, 0.2] Classe:  [1, 0]
Erro neuronio 0  =  0
Neuronio  0 : [0, 0, 0, 0, 0]
Erro neuronio 1  =  -1
Neuronio  1 : [-1, -5.1, -3.5, -1.4, -0.2]
Processando - Entrada:  [7.0, 3.2, 4.7, 1.4] Classe:  [0, 1]
Erro neuronio 0  =  -1
Neuronio  0 : [-1, -7.0, -3.2, -4.7, -1.4]
Erro neuronio 1  =  1
Neuronio  1 : [0, 1.9000000000000004, -0.2999999999999998, 3.3000000000000003, 1.2]
Processando - Entrada:  [6.3, 3.3, 6.0, 2.5] Classe:  [0, 1]
Erro neuronio 0  =  0
Neuronio  0 : [-1, -7.0, -3.2, -4.7, -1.4]
Erro neuronio 1  =  0
Neuronio  1 : [0, 1.9000000000000004, -0.2999999999999998, 3.3000000000000003, 1.2]
Processando - Entrada:  [4.9, 3.0, 1.4, 0.2] Classe:  [1, 0]
Erro neuronio 0  =  1
Neuronio  0 : [0, -2.0999999999999996, -0.20000000000000018, -3.3000000000000003, -1.2]
Erro neuronio 1  =  -1
Neuronio  1 : [-1, -3.0, -3.3, 1.9000000000000004, 1.0]
Processando - Entrada:  [6.4, 3.2, 4.5, 1.5] Classe:  [0, 1]
Erro neuronio 0  =  0
Neuronio  0 : [0, -2.0999999999999996, -0.20000000000000018, -3.3000000000000003, -1.2]
Erro neuronio 1  =  1
Neuronio  1 : [0, 3.4000000000000004, -0.09999999999999964, 6.4, 2.5]
Processando - Entrada:  [5.8, 2.7, 5.1, 1.9] Classe:  [0, 1]
Erro neuronio 0  =  0
Neuronio  0 : [0, -2.0999999999999996, -0.20000000000000018, -3.3000000000000003, -1.2]
Erro neuronio 1  =  0
Neuronio  1 : [0, 3.4000000000000004, -0.09999999999999964, 6.4, 2.5]
Processando - Entrada:  [4.7, 3.2, 1.3, 0.2] Classe:  [1, 0]
Erro neuronio 0  =  1
Neuronio  0 : [1, 2.6000000000000005, 3.0, -2.0, -1.0]
Erro neuronio 1  =  -1
Neuronio  1 : [-1, -1.2999999999999998, -3.3, 5.1000000000000005, 2.3]
Processando - Entrada:  [6.9, 3.1, 4.9, 1.5] Classe:  [0, 1]
Erro neuronio 0  =  -1
Neuronio  0 : [0, -4.3, -0.10000000000000009, -6.9, -2.5]
Erro neuronio 1  =  0
Neuronio  1 : [-1, -1.2999999999999998, -3.3, 5.1000000000000005, 2.3]
Processando - Entrada:  [7.1, 3.0, 5.9, 2.1] Classe:  [0, 1]
Erro neuronio 0  =  0
Neuronio  0 : [0, -4.3, -0.10000000000000009, -6.9, -2.5]
Erro neuronio 1  =  0
Neuronio  1 : [-1, -1.2999999999999998, -3.3, 5.1000000000000005, 2.3]
Processando - Entrada:  [4.6, 3.1, 1.5, 0.2] Classe:  [1, 0]
Erro neuronio 0  =  1
Neuronio  0 : [1, 0.2999999999999998, 3.0, -5.4, -2.3]
Erro neuronio 1  =  0
Neuronio  1 : [-1, -1.2999999999999998, -3.3, 5.1000000000000005, 2.3]
Processando - Entrada:  [5.5, 2.3, 4.0, 1.3] Classe:  [0, 1]
Erro neuronio 0  =  0
Neuronio  0 : [1, 0.2999999999999998, 3.0, -5.4, -2.3]
Erro neuronio 1  =  0
Neuronio  1 : [-1, -1.2999999999999998, -3.3, 5.1000000000000005, 2.3]
Processando - Entrada:  [6.3, 2.9, 5.6, 1.8] Classe:  [0, 1]
Erro neuronio 0  =  0
Neuronio  0 : [1, 0.2999999999999998, 3.0, -5.4, -2.3]
Erro neuronio 1  =  0
Neuronio  1 : [-1, -1.2999999999999998, -3.3, 5.1000000000000005, 2.3]
Processando - Entrada:  [5.0, 3.6, 1.4, 0.2] Classe:  [1, 0]
Erro neuronio 0  =  0
Neuronio  0 : [1, 0.2999999999999998, 3.0, -5.4, -2.3]
Erro neuronio 1  =  0
Neuronio  1 : [-1, -1.2999999999999998, -3.3, 5.1000000000000005, 2.3]
Processando - Entrada:  [6.5, 2.8, 4.6, 1.5] Classe:  [0, 1]
Erro neuronio 0  =  0
Neuronio  0 : [1, 0.2999999999999998, 3.0, -5.4, -2.3]
Erro neuronio 1  =  0
Neuronio  1 : [-1, -1.2999999999999998, -3.3, 5.1000000000000005, 2.3]
Processando - Entrada:  [6.5, 3.0, 5.8, 2.2] Classe:  [0, 1]
Erro neuronio 0  =  0
Neuronio  0 : [1, 0.2999999999999998, 3.0, -5.4, -2.3]
Erro neuronio 1  =  0
Neuronio  1 : [-1, -1.2999999999999998, -3.3, 5.1000000000000005, 2.3]
Processando - Entrada:  [5.4, 3.9, 1.7, 0.4] Classe:  [1, 0]
Erro neuronio 0  =  0
Neuronio  0 : [1, 0.2999999999999998, 3.0, -5.4, -2.3]
Erro neuronio 1  =  0
Neuronio  1 : [-1, -1.2999999999999998, -3.3, 5.1000000000000005, 2.3]
Processando - Entrada:  [5.7, 2.8, 4.5, 1.3] Classe:  [0, 1]
Erro neuronio 0  =  0
Neuronio  0 : [1, 0.2999999999999998, 3.0, -5.4, -2.3]
Erro neuronio 1  =  0
Neuronio  1 : [-1, -1.2999999999999998, -3.3, 5.1000000000000005, 2.3]
Processando - Entrada:  [7.6, 3.0, 6.6, 2.1] Classe:  [0, 1]
Erro neuronio 0  =  0
Neuronio  0 : [1, 0.2999999999999998, 3.0, -5.4, -2.3]
Erro neuronio 1  =  0
Neuronio  1 : [-1, -1.2999999999999998, -3.3, 5.1000000000000005, 2.3]
Processando - Entrada:  [4.6, 3.4, 1.4, 0.3] Classe:  [1, 0]
Erro neuronio 0  =  0
Neuronio  0 : [1, 0.2999999999999998, 3.0, -5.4, -2.3]
Erro neuronio 1  =  0
Neuronio  1 : [-1, -1.2999999999999998, -3.3, 5.1000000000000005, 2.3]
Processando - Entrada:  [6.3, 3.3, 4.7, 1.6] Classe:  [0, 1]
Erro neuronio 0  =  0
Neuronio  0 : [1, 0.2999999999999998, 3.0, -5.4, -2.3]
Erro neuronio 1  =  0
Neuronio  1 : [-1, -1.2999999999999998, -3.3, 5.1000000000000005, 2.3]
Processando - Entrada:  [4.9, 2.5, 4.5, 1.7] Classe:  [0, 1]
Erro neuronio 0  =  0
Neuronio  0 : [1, 0.2999999999999998, 3.0, -5.4, -2.3]
Erro neuronio 1  =  0
Neuronio  1 : [-1, -1.2999999999999998,
```

## Célula 6 — Código

```python
#Generalizacao

print('Pesos neuronio 0:', w[0][0], w[0][1],w[0][2],w[0][3],w[0][4])
print('Pesos neuronio 1:', w[1][0], w[1][1],w[1][2],w[1][3],w[1][4])

acertos = 0
for tupla in dadosTeste:
  entradaX = tupla.copy()
  classeY = entradaX.pop()
  print("Processando - Entrada: ", entradaX, "Classe Esperada: ", classeY)

  saida = []
  for j in range(0,len(w)):
    v = propagacao(entradaX,w[j])
    y = funcaoLimiar(v)
    print('Saida da rede - predicao Neuronio ',j,':', y)
    saida.append(y)

  if(saida==tupla[4]): acertos = acertos +1

acc = acertos / len(dadosTeste)
print('Acuracia: ', acc)
```

**Saída:**

```text
P
```

## Célula 7 — Código

```python

```
