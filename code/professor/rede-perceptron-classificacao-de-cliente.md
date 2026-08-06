---
entry_id: "rede-perceptron-classificacao-de-cliente"
title: "Rede Perceptron - Classificacao de Cliente"
language: "jupyter"
category: "codigo-professor"
unit: ""
source: "raw/code/professor/rede-perceptron-classificacao-de-cliente.ipynb"
---
# Rede Perceptron - Classificacao de Cliente

> **Linguagem:** jupyter

## Célula 1 — Código

```python
#Algoritmo de Treinamento do Perceptron

#Funcao de ativacao
def funcaoLimiar(v):
  if v>=0: return 1
  else: return 0

def propagacao(tupla,pesos):
  v = pesos[0] + pesos[1] * tupla[0] + pesos[2] * tupla[1]
  return v
```

## Célula 2 — Código

```python
def algoritmoTreinamento(dados):
  epoca = 0
  eta = 1
  pesos = [0,0,0]
  print("Pesos iniciais: ", pesos)

  erroGeral = 1
  while erroGeral!=0 and epoca<=100:
    erroGeral = 0
    epoca = epoca + 1
    print("\nEpoca: ", epoca)
    for tupla in dados:
      print("Processando: ", tupla)
      v = propagacao(tupla,pesos)
      y = funcaoLimiar(v)
      erro = tupla[2] - y
      print('Erro = ', erro)
      if erro!=0:
        delta = eta * erro
        pesos[0] = pesos[0] + delta
        delta = eta * erro * tupla[0]
        pesos[1] = pesos[1] + delta
        delta = eta * erro * tupla[1]
        pesos[2] = pesos[2] + delta
      print("Pesos atuais: ", pesos)
      erroGeral = erroGeral + abs(erro)

  return pesos
```

## Célula 3 — Código

```python
#Tabela - Dados de Treino
x1 = [2800,1300,1400,500,1100,1800,2400,1950,450,2750,850,1300,2100,900,2700,1600]
x2 = [550,500,80,200,270,450,650,600,70,730,90,200,750,300,250,500]
d =  [1,0,1,0,0,1,1,1,0,1,0,0,1,0,1,0]

maiorRenda = 2800
maiorDivida = 800

print('Dados de Treino:')
dadosTreino = []
#print('x1  x2  d')
for i in range(0,len(x1)):
  #print(x1[i], ' ', x2[i], ' ', d[i])
  dadosTreino.append([x1[i]/maiorRenda,x2[i]/maiorDivida,d[i]])
  #dadosTreino.append([x1[i],x2[i],d[i]])
print(dadosTreino)

#Tabela - Dados de Teste
x1 = [1900,2500,1600,2300,2100]
x2 = [150,800,700,500,250]
d =  [1,1,0,1,1]

print('Dados de Teste:')
dadosTeste = []
#print('x1  x2  d')
for i in range(0,len(x1)):
  #print(x1[i], ' ', x2[i], ' ', d[i])
  dadosTeste.append([x1[i]/maiorRenda,x2[i]/maiorDivida,d[i]])
  #dadosTeste.append([x1[i],x2[i],d[i]])
print(dadosTeste)
```

**Saída:**

```text
Dados de Treino:
[[1.0, 0.6875, 1], [0.4642857142857143, 0.625, 0], [0.5, 0.1, 1], [0.17857142857142858, 0.25, 0], [0.39285714285714285, 0.3375, 0], [0.6428571428571429, 0.5625, 1], [0.8571428571428571, 0.8125, 1], [0.6964285714285714, 0.75, 1], [0.16071428571428573, 0.0875, 0], [0.9821428571428571, 0.9125, 1], [0.30357142857142855, 0.1125, 0], [0.4642857142857143, 0.25, 0], [0.75, 0.9375, 1], [0.32142857142857145, 0.375, 0], [0.9642857142857143, 0.3125, 1], [0.5714285714285714, 0.625, 0]]
Dados de Teste:
[[0.6785714285714286, 0.1875, 1], [0.8928571428571429, 1.0, 1], [0.5714285714285714, 0.875, 0], [0.8214285714285714, 0.625, 1], [0.75, 0.3125, 1]]
```

## Célula 4 — Código

```python
#Treinamento
w = algoritmoTreinamento(dadosTreino)
```

**Saída:**

```text
Pesos iniciais:  [0, 0, 0]

Epoca:  1
Processando:  [1.0, 0.6875, 1]
Erro =  0
Pesos atuais:  [0, 0, 0]
Processando:  [0.4642857142857143, 0.625, 0]
Erro =  -1
Pesos atuais:  [-1, -0.4642857142857143, -0.625]
Processando:  [0.5, 0.1, 1]
Erro =  1
Pesos atuais:  [0, 0.0357142857142857, -0.525]
Processando:  [0.17857142857142858, 0.25, 0]
Erro =  0
Pesos atuais:  [0, 0.0357142857142857, -0.525]
Processando:  [0.39285714285714285, 0.3375, 0]
Erro =  0
Pesos atuais:  [0, 0.0357142857142857, -0.525]
Processando:  [0.6428571428571429, 0.5625, 1]
Erro =  1
Pesos atuais:  [1, 0.6785714285714286, 0.03749999999999998]
Processando:  [0.8571428571428571, 0.8125, 1]
Erro =  0
Pesos atuais:  [1, 0.6785714285714286, 0.03749999999999998]
Processando:  [0.6964285714285714, 0.75, 1]
Erro =  0
Pesos atuais:  [1, 0.6785714285714286, 0.03749999999999998]
Processando:  [0.16071428571428573, 0.0875, 0]
Erro =  -1
Pesos atuais:  [0, 0.5178571428571429, -0.05000000000000002]
Processando:  [0.9821428571428571, 0.9125, 1]
Erro =  0
Pesos atuais:  [0, 0.5178571428571429, -0.05000000000000002]
Processando:  [0.30357142857142855, 0.1125, 0]
Erro =  -1
Pesos atuais:  [-1, 0.21428571428571436, -0.16250000000000003]
Processando:  [0.4642857142857143, 0.25, 0]
Erro =  0
Pesos atuais:  [-1, 0.21428571428571436, -0.16250000000000003]
Processando:  [0.75, 0.9375, 1]
Erro =  1
Pesos atuais:  [0, 0.9642857142857144, 0.7749999999999999]
Processando:  [0.32142857142857145, 0.375, 0]
Erro =  -1
Pesos atuais:  [-1, 0.642857142857143, 0.3999999999999999]
Processando:  [0.9642857142857143, 0.3125, 1]
Erro =  1
Pesos atuais:  [0, 1.6071428571428572, 0.7124999999999999]
Processando:  [0.5714285714285714, 0.625, 0]
Erro =  -1
Pesos atuais:  [-1, 1.0357142857142858, 0.08749999999999991]

Epoca:  2
Processando:  [1.0, 0.6875, 1]
Erro =  0
Pesos atuais:  [-1, 1.0357142857142858, 0.08749999999999991]
Processando:  [0.4642857142857143, 0.625, 0]
Erro =  0
Pesos atuais:  [-1, 1.0357142857142858, 0.08749999999999991]
Processando:  [0.5, 0.1, 1]
Erro =  1
Pesos atuais:  [0, 1.5357142857142858, 0.18749999999999992]
Processando:  [0.17857142857142858, 0.25, 0]
Erro =  -1
Pesos atuais:  [-1, 1.3571428571428572, -0.06250000000000008]
Processando:  [0.39285714285714285, 0.3375, 0]
Erro =  0
Pesos atuais:  [-1, 1.3571428571428572, -0.06250000000000008]
Processando:  [0.6428571428571429, 0.5625, 1]
Erro =  1
Pesos atuais:  [0, 2.0, 0.4999999999999999]
Processando:  [0.8571428571428571, 0.8125, 1]
Erro =  0
Pesos atuais:  [0, 2.0, 0.4999999999999999]
Processando:  [0.6964285714285714, 0.75, 1]
Erro =  0
Pesos atuais:  [0, 2.0, 0.4999999999999999]
Processando:  [0.16071428571428573, 0.0875, 0]
Erro =  -1
Pesos atuais:  [-1, 1.8392857142857142, 0.41249999999999987]
Processando:  [0.9821428571428571, 0.9125, 1]
Erro =  0
Pesos atuais:  [-1, 1.8392857142857142, 0.41249999999999987]
Processando:  [0.30357142857142855, 0.1125, 0]
Erro =  0
Pesos atuais:  [-1, 1.8392857142857142, 0.41249999999999987]
Processando:  [0.4642857142857143, 0.25, 0]
Erro =  0
Pesos atuais:  [-1, 1.8392857142857142, 0.41249999999999987]
Processando:  [0.75, 0.9375, 1]
Erro =  0
Pesos atuais:  [-1, 1.8392857142857142, 0.41249999999999987]
Processando:  [0.32142857142857145, 0.375, 0]
Erro =  0
Pesos atuais:  [-1, 1.8392857142857142, 0.41249999999999987]
Processando:  [0.9642857142857143, 0.3125, 1]
Erro =  0
Pesos atuais:  [-1, 1.8392857142857142, 0.41249999999999987]
Processando:  [0.5714285714285714, 0.625, 0]
Erro =  -1
Pesos atuais:  [-2, 1.2678571428571428, -0.21250000000000013]

Epoca:  3
Processando:  [1.0, 0.6875, 1]
Erro =  1
Pesos atuais:  [-1, 2.267857142857143, 0.47499999999999987]
Processando:  [0.4642857142857143, 0.625, 0]
Erro =  -1
Pesos atuais:  [-2, 1.8035714285714284, -0.15000000000000013]
Processando:  [0.5, 0.1, 1]
Erro =  1
Pesos atuais:  [-1, 2.3035714285714284, -0.05000000000000013]
Processando:  [0.17857142857142858, 0.25, 0]
Erro =  0
Pesos atuais:  [-1, 2.3035714285714284, -0.05000000000000013]
Processando:  [0.39285714285714285, 0.3375, 0]
Erro =  0
Pesos atuais:  [-1, 2.3035714285714284, -0.05000000000000013]
Processando:  [0.6428571428571429, 0.5625, 1]
Erro =  0
Pesos atuais:  [-1, 2.3035714285714284, -0.05000000000000013]
Processando:  [0.8571428571428571, 0.8125, 1]
Erro =  0
Pesos atuais:  [-1, 2.3035714285714284, -0.05000000000000013]
Processando:  [0.6964285714285714, 0.75, 1]
Erro =  0
Pesos atuais:  [-1, 2.3035714285714284, -0.05000000000000013]
Processando:  [0.16071428571428573, 0.0875, 0]
Erro =  0
Pesos atuais:  [-1, 2.3035714285714284, -0.05000000000000013]
Processando:  [0.9821428571428571, 0.9125, 1]
Erro =  0
Pesos atuais:  [-1, 2.3035714285714284, -0.05000000000000013]
Processando:  [0.30357142857142855, 0.1125, 0]
Erro =  0
Pesos atuais:  [-1, 2.3035714285714284, -0.05000000000000013]
Processando:  [0.4642857142857143, 0.25, 0]
Erro =  -1
Pesos atuais:  [-2, 1.839285714285714, -0.30000000000000016]
Processando:  [0.75, 0.9375, 1]
Erro =  1
Pesos atuais:  [-1, 2.589285714285714, 0.6374999999999998]
Processando:  [0.32142857142857145, 0.375, 0]
Erro =  -1
Pesos atuais:  [-2, 2.2678571428571423, 0.26249999999999984]
Processando:  [0.9642857142857143, 0.3125, 1]
Erro =  0
Pesos atuais:  [-2, 2.2678571428571423, 0.26249999999999984]
Processando:  [0.5714285714285714, 0.625, 0]
Erro =  0
Pesos a
```

## Célula 5 — Código

```python
#Generalizacao

acertos = 0
for tupla in dadosTeste:
  v = propagacao(tupla,w)
  y = funcaoLimiar(v)
  print('Saida da rede - predicao: ', y)
  print('Saida esperada ........ : ', tupla[2])
  if y==tupla[2]: acertos = acertos+1

acc = acertos / len(dadosTeste)
print('Acuracia: ', acc)
```
