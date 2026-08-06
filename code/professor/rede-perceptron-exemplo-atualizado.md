---
entry_id: "rede-perceptron-exemplo-atualizado"
title: "Rede Perceptron - Exemplo Atualizado"
language: "jupyter"
category: "codigo-professor"
unit: ""
source: "raw/code/professor/rede-perceptron-exemplo-atualizado.ipynb"
---
# Rede Perceptron - Exemplo Atualizado

> **Linguagem:** jupyter

## Célula 1 — Markdown

## **Rede Perceptron**

Profa Sílvia Moraes - Agosto/2025

## Célula 2 — Código

```python
import matplotlib.pyplot as plt
import numpy as np
```

## Célula 3 — Markdown

Fuções de ativação e propagação do sinal

## Célula 4 — Código

```python
#Funcao de ativacao
def funcaoLimiar(v):
  if v>=0: return 1
  else: return 0

#Método de propagação
def propagacao(tupla,pesos):
  v = pesos[0] + pesos[1] * tupla[0] + pesos[2] * tupla[1]
  return v
```

## Célula 5 — Markdown

Algoritmo de Treinamento: Regra Delta

## Célula 6 — Código

```python
def algoritmoTreinamento(dados):
  epoca = 0
  eta = 1   #Learning rate = taxa de aprendizado
  pesos = [0,0,0]  #Pesos de apenas 1 neurônio
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

## Célula 7 — Markdown

Dados de entrada

## Célula 8 — Código

```python
#Tabela OR
x1_vals = [0,0,1,1]
x2_vals = [0,1,0,1]
d_vals =  [0,1,1,1]

dados = []
print('x1  x2  d')
for i in range(0,len(x1_vals)):
  print(x1_vals[i], ' ', x2_vals[i], ' ', d_vals[i])
  dados.append([x1_vals[i],x2_vals[i],d_vals[i]])
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

## Célula 9 — Markdown

Etapa de Treinamento da rede

## Célula 10 — Código

```python
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

## Célula 11 — Markdown

Gera reta a partir da equação: x1*w11 + x2*w12 + w10 = 0

## Célula 12 — Código

```python
w10 = w[0]     # Peso bias
w11 = w[1]     # Peso de x1
w12 = w[2]     # Peso de x2

x1_d0 = [x1 for x1, d in zip(x1_vals, d_vals) if d == 0]
x2_d0 = [x2 for x2, d in zip(x2_vals, d_vals) if d == 0]
x1_d1 = [x1 for x1, d in zip(x1_vals, d_vals) if d == 1]
x2_d1 = [x2 for x2, d in zip(x2_vals, d_vals) if d == 1]

x = np.linspace(-0.2, 1.2, 100)

# Evitar divisão por zero
if w12 != 0:
    y = (-w10 - w11 * x) / w12
else:
    y = np.full_like(x, np.nan)  # não plota nada se divisão por zero

# Plot
plt.figure(figsize=(6, 6))
plt.plot(x, y, 'k--', label=f'{w11}·x1 + {w12}·x2 + {w10} = 0')

plt.scatter(x1_d0, x2_d0, color='red', label='d = 0')
plt.scatter(x1_d1, x2_d1, color='green', label='d = 1')

plt.xlim(-0.2, 1.2)
plt.ylim(-0.2, 1.2)
plt.xlabel('x1')
plt.ylabel('x2')
plt.title('Reta de separação com pesos personalizados')
plt.axhline(0, color='gray', lw=0.5)
plt.axvline(0, color='gray', lw=0.5)
plt.grid(True, linestyle='--', alpha=0.5)
plt.legend()
plt.gca().set_aspect('equal', adjustable='box')
plt.show()
```

**Saída:**

```text
<Figure size 600x600 with 1 Axes>
```

## Célula 13 — Markdown

Etapa de Generalização

## Célula 14 — Código

```python
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
Informe o valor de x2: 0
Saida da rede:  1
```
