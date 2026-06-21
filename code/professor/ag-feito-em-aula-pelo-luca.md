---
entry_id: "ag-feito-em-aula-pelo-luca"
title: "AG feito em aula pelo Luca"
language: "python"
category: "codigo-professor"
unit: ""
source: "raw/code/professor/ag-feito-em-aula-pelo-luca.py"
---
# AG feito em aula pelo Luca

> **Linguagem:** python

```python


import random

linhas = 11

lista = [5, 10, 15, 3, 10, 5, 2, 16, 9, 7, 5, 10, 15, 3, 10, 5, 2, 16, 9, 7, 5, 10, 15, 3, 10, 5, 2, 16, 9, 7]
lista = lista + lista

matriz = [[0] * (len(lista)+1) for i in range(linhas)]
matriz_inter = [[0] * (len(lista)+1) for i in range(linhas)]

for i in range(11):
    for j in range((len(lista))):
        matriz[i][j] = random.randint(0,1)

def aptidao(pesos, vetor):
    grupo0 = 0
    grupo1 = 0
    for i in range(len(pesos)):
        if vetor[i] == 0:
            grupo0+=pesos[i]
        else:
            grupo1+=pesos[i]

    resultado = abs(grupo0 - grupo1)
    vetor[-1] = resultado
    return resultado

def elitismo(matriz):
    val, index = 1000000, 0
    for i in range(linhas):
        if matriz[i][-1] < val:
            val = matriz[i][-1]
            index = i

    return index

def torneio(valores):
    index1 = random.randint(0, linhas-1)
    index2 = random.randint(0, linhas-1)

    val1, val2 = valores[index1][-1], valores[index2][-1]
    if val1 > val2:
        return index2
    else:
        return index1

def crossover(valores):
    pai = torneio(valores)
    mae = torneio(valores)

    metade = linhas//2

    filho1 = valores[pai][:metade].copy() + valores[mae][metade:].copy()
    filho2 = valores[mae][:metade].copy() + valores[pai][metade:].copy()
    return filho1, filho2

def mutacao(valores):
    for i in range(random.randint(1,8)):
        index_linha = random.randint(1,linhas-1)
        index_coluna = random.randint(0, len(lista) - 1)

        if valores[index_linha][index_coluna]:
            valores[index_linha][index_coluna] = 0
        else:
            valores[index_linha][index_coluna] = 1

controle = False
for geracao in range(50):
    
    print("Geração: ", geracao)  
    for i in range(linhas):
        val = aptidao(lista, matriz[i])
        if val == 0:
            controle = True

    for i in range(linhas):
        print(matriz[i])

    if controle:
        print("Achei")
        break


    index = elitismo(matriz)

    matriz_inter[0] = matriz[index].copy()

    for i in range(1, linhas, 2):
        filho1, filho2 = crossover(matriz)
        matriz_inter[i] = filho1
        matriz_inter[i+1] = filho2

    matriz = matriz_inter

    if random.randint(0,10) > 3:
        print("Mutação")
        mutacao(matriz)



```
