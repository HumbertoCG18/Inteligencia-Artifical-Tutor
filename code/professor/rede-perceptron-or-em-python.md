---
entry_id: "rede-perceptron-or-em-python"
title: "Rede Perceptron - OR em Python"
language: "jupyter"
category: "codigo-professor"
unit: ""
source: "raw/code/professor/rede-perceptron-or-em-python.ipynb"
---
# Rede Perceptron - OR em Python

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
#Tabela OR
x1 = [0,0,1,1]
x2 = [0,1,0,1]
d =  [0,1,1,1]

dados = []
print('x1  x2  d')
for i in range(0,len(x1)):
  print(x1[i], ' ', x2[i], ' ', d[i])
  dados.append([x1[i],x2[i],d[i]])
#print(dados)
```

**Saída:**

```text
x1  x2  d
0   0   0
0   1   1
1   0   1
1   1   1
```

## Célula 4 — Código

```python
#Treinamento
w = algoritmoTreinamento(dados)
```

**Saída:**

```text
Pesos iniciais:  [0, 0, 0]

Epoca:  1
Processando:  [0, 0, 0]
Erro =  -1
Pesos atuais:  [-1, 0, 0]
Processando:  [0, 1, 1]
Erro =  1
Pesos atuais:  [0, 0, 1]
Processando:  [1, 0, 1]
Erro =  0
Pesos atuais:  [0, 0, 1]
Processando:  [1, 1, 1]
Erro =  0
Pesos atuais:  [0, 0, 1]

Epoca:  2
Processando:  [0, 0, 0]
Erro =  -1
Pesos atuais:  [-1, 0, 1]
Processando:  [0, 1, 1]
Erro =  0
Pesos atuais:  [-1, 0, 1]
Processando:  [1, 0, 1]
Erro =  1
Pesos atuais:  [0, 1, 1]
Processando:  [1, 1, 1]
Erro =  0
Pesos atuais:  [0, 1, 1]

Epoca:  3
Processando:  [0, 0, 0]
Erro =  -1
Pesos atuais:  [-1, 1, 1]
Processando:  [0, 1, 1]
Erro =  0
Pesos atuais:  [-1, 1, 1]
Processando:  [1, 0, 1]
Erro =  0
Pesos atuais:  [-1, 1, 1]
Processando:  [1, 1, 1]
Erro =  0
Pesos atuais:  [-1, 1, 1]

Epoca:  4
Processando:  [0, 0, 0]
Erro =  0
Pesos atuais:  [-1, 1, 1]
Processando:  [0, 1, 1]
Erro =  0
Pesos atuais:  [-1, 1, 1]
Processando:  [1, 0, 1]
Erro =  0
Pesos atuais:  [-1, 1, 1]
Processando:  [1, 1, 1]
Erro =  0
Pesos atuais:  [-1, 1, 1]
```

## Célula 5 — Código

```python
#Generalizacao

entrada1 = int(input('Informe o valor de x1: '))
entrada2 = int(input('Informe o valor de x2: '))
tuplaEntrada = [entrada1,entrada2]

v = propagacao(tuplaEntrada,w)
y = funcaoLimiar(v)
print('Saida da rede: ', y)
```

**Saída:**

```text
Informe o valor de x1: 1
Informe o valor de x2: 1
Saida da rede:  1
```
