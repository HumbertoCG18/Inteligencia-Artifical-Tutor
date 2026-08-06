---
entry_id: "rede-perceptron-reconhecendo-letras"
title: "Rede Perceptron - Reconhecendo Letras"
language: "jupyter"
category: "codigo-professor"
unit: ""
source: "raw/code/professor/rede-perceptron-reconhecendo-letras.ipynb"
---
# Rede Perceptron - Reconhecendo Letras

> **Linguagem:** jupyter

## Célula 1 — Código

```python
#Algoritmo de Treinamento do Perceptron
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
  neuronio = [0]*(len(dados[0]))
  pesos =   [neuronio, neuronio.copy()] #Sao dois neuronios

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
#Separando dados da planta Iris em Treino/Teste
letraI = [0,0,1,0,0,
          0,0,1,0,0,
          0,0,1,0,0,
          0,0,1,0,0,
          0,0,1,0,0, [1,0]]
letraO = [1,1,1,1,1,
          1,0,0,0,1,
          1,0,0,0,1,
          1,0,0,0,1,
          1,1,1,1,1, [0,1]]
dadosTreino = [letraI,letraO]


print('\nDados')
for item in dadosTreino:
  print(item)

letraI = [0,0,0,0,0,
          0,0,1,0,0,
          1,0,1,0,0,
          0,0,1,0,0,
          0,0,1,0,0, [1,0]]
letraO = [1,1,1,1,1,
          1,0,0,0,1,
          1,0,0,0,1,
          1,1,0,0,1,
          1,1,0,1,1, [0,1]]
dadosTeste = [letraI,letraO]
```

**Saída:**

```text
Dados
[0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, [1, 0]]
[1, 1, 1, 1, 1, 1, 0, 0, 0, 1, 1, 0, 0, 0, 1, 1, 0, 0, 0, 1, 1, 1, 1, 1, 1, [0, 1]]
```

## Célula 4 — Código

```python
#Treinamento
w = algoritmoTreinamento(dadosTreino)
```

**Saída:**

```text
Pesos iniciais:  [[0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], [0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0]]

>>>>>>Epoca:  1
Processando - Entrada:  [0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0] Classe:  [1, 0]
Erro neuronio 0  =  0
Neuronio  0 : [0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0]
Erro neuronio 1  =  -1
Neuronio  1 : [-1, 0, 0, -1, 0, 0, 0, 0, -1, 0, 0, 0, 0, -1, 0, 0, 0, 0, -1, 0, 0, 0, 0, -1, 0, 0]
Processando - Entrada:  [1, 1, 1, 1, 1, 1, 0, 0, 0, 1, 1, 0, 0, 0, 1, 1, 0, 0, 0, 1, 1, 1, 1, 1, 1] Classe:  [0, 1]
Erro neuronio 0  =  -1
Neuronio  0 : [-1, -1, -1, -1, -1, -1, -1, 0, 0, 0, -1, -1, 0, 0, 0, -1, -1, 0, 0, 0, -1, -1, -1, -1, -1, -1]
Erro neuronio 1  =  1
Neuronio  1 : [0, 1, 1, 0, 1, 1, 1, 0, -1, 0, 1, 1, 0, -1, 0, 1, 1, 0, -1, 0, 1, 1, 1, 0, 1, 1]
Pesos atuais:  [[-1, -1, -1, -1, -1, -1, -1, 0, 0, 0, -1, -1, 0, 0, 0, -1, -1, 0, 0, 0, -1, -1, -1, -1, -1, -1], [0, 1, 1, 0, 1, 1, 1, 0, -1, 0, 1, 1, 0, -1, 0, 1, 1, 0, -1, 0, 1, 1, 1, 0, 1, 1]]
Erro Geral:  3

>>>>>>Epoca:  2
Processando - Entrada:  [0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0] Classe:  [1, 0]
Erro neuronio 0  =  1
Neuronio  0 : [0, -1, -1, 0, -1, -1, -1, 0, 1, 0, -1, -1, 0, 1, 0, -1, -1, 0, 1, 0, -1, -1, -1, 0, -1, -1]
Erro neuronio 1  =  0
Neuronio  1 : [0, 1, 1, 0, 1, 1, 1, 0, -1, 0, 1, 1, 0, -1, 0, 1, 1, 0, -1, 0, 1, 1, 1, 0, 1, 1]
Processando - Entrada:  [1, 1, 1, 1, 1, 1, 0, 0, 0, 1, 1, 0, 0, 0, 1, 1, 0, 0, 0, 1, 1, 1, 1, 1, 1] Classe:  [0, 1]
Erro neuronio 0  =  0
Neuronio  0 : [0, -1, -1, 0, -1, -1, -1, 0, 1, 0, -1, -1, 0, 1, 0, -1, -1, 0, 1, 0, -1, -1, -1, 0, -1, -1]
Erro neuronio 1  =  0
Neuronio  1 : [0, 1, 1, 0, 1, 1, 1, 0, -1, 0, 1, 1, 0, -1, 0, 1, 1, 0, -1, 0, 1, 1, 1, 0, 1, 1]
Pesos atuais:  [[0, -1, -1, 0, -1, -1, -1, 0, 1, 0, -1, -1, 0, 1, 0, -1, -1, 0, 1, 0, -1, -1, -1, 0, -1, -1], [0, 1, 1, 0, 1, 1, 1, 0, -1, 0, 1, 1, 0, -1, 0, 1, 1, 0, -1, 0, 1, 1, 1, 0, 1, 1]]
Erro Geral:  1

>>>>>>Epoca:  3
Processando - Entrada:  [0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0] Classe:  [1, 0]
Erro neuronio 0  =  0
Neuronio  0 : [0, -1, -1, 0, -1, -1, -1, 0, 1, 0, -1, -1, 0, 1, 0, -1, -1, 0, 1, 0, -1, -1, -1, 0, -1, -1]
Erro neuronio 1  =  0
Neuronio  1 : [0, 1, 1, 0, 1, 1, 1, 0, -1, 0, 1, 1, 0, -1, 0, 1, 1, 0, -1, 0, 1, 1, 1, 0, 1, 1]
Processando - Entrada:  [1, 1, 1, 1, 1, 1, 0, 0, 0, 1, 1, 0, 0, 0, 1, 1, 0, 0, 0, 1, 1, 1, 1, 1, 1] Classe:  [0, 1]
Erro neuronio 0  =  0
Neuronio  0 : [0, -1, -1, 0, -1, -1, -1, 0, 1, 0, -1, -1, 0, 1, 0, -1, -1, 0, 1, 0, -1, -1, -1, 0, -1, -1]
Erro neuronio 1  =  0
Neuronio  1 : [0, 1, 1, 0, 1, 1, 1, 0, -1, 0, 1, 1, 0, -1, 0, 1, 1, 0, -1, 0, 1, 1, 1, 0, 1, 1]
Pesos atuais:  [[0, -1, -1, 0, -1, -1, -1, 0, 1, 0, -1, -1, 0, 1, 0, -1, -1, 0, 1, 0, -1, -1, -1, 0, -1, -1], [0, 1, 1, 0, 1, 1, 1, 0, -1, 0, 1, 1, 0, -1, 0, 1, 1, 0, -1, 0, 1, 1, 1, 0, 1, 1]]
Erro Geral:  0
```

## Célula 5 — Código

```python
#Generalizacao

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

  if(saida==tupla[len(entradaX)]): acertos = acertos +1

acc = acertos / len(dadosTeste)
print('Acuracia: ', acc)
```

**Saída:**

```text
Processando - Entrada:  [0, 0, 0, 0, 0, 0, 0, 1, 0, 0, 1, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0] Classe Esperada:  [1, 0]
Saida da rede - predicao Neuronio  0 : 1
Saida da rede - predicao Neuronio  1 : 0
Processando - Entrada:  [1, 1, 1, 1, 1, 1, 0, 0, 0, 1, 1, 0, 0, 0, 1, 1, 1, 0, 0, 1, 1, 1, 0, 1, 1] Classe Esperada:  [0, 1]
Saida da rede - predicao Neuronio  0 : 0
Saida da rede - predicao Neuronio  1 : 1
Acuracia:  1.0
```

## Célula 6 — Código

```python

```
