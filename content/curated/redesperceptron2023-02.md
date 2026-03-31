# Rede Neural Perceptron

Silvia Moraes

![](content/images/redesperceptron2023-02-_page_0_Picture_2.png)

### Roteiro

- Arquiteturas de Rede
- Redes FeedForward
- Revisitando a estrutura de um neurônio artificial
- Algoritmo de Aprendizado de uma rede perceptron
- Passo a passo de execução
- Limitação da rede

![](content/images/redesperceptron2023-02-_page_1_Picture_7.png)

# A arquitetura de uma rede neural define o tipo de tarefa que ela pode executar.

![](content/images/redesperceptron2023-02-_page_2_Picture_1.png)

![](content/images/redesperceptron2023-02-_page_2_Picture_2.png)

![](content/images/redesperceptron2023-02-_page_2_Picture_3.png)

# Redes Feed Forward Tarefas Supervisionadas: classificação o e regressão

![](content/images/redesperceptron2023-02-_page_3_Picture_1.png)

Perceptron

![](content/images/redesperceptron2023-02-_page_3_Picture_3.png)

![](content/images/redesperceptron2023-02-_page_3_Figure_4.png)

https://sites.icmc.usp.br/andre/research/neural/

Propagação: fluxo do sinal sempre para frente

![](content/images/redesperceptron2023-02-_page_4_Picture_0.png)

# Redes Feed Forward Rede Perceptron

- Perceptron é uma rede muito simples.
- Quando constituída de apenas um neurônio é chamada de perceptron elementar.
- Possui apenas uma camada de neurônios.
- Pode ter várias entradas e várias saídas.
- Trabalha com valores discretos e contínuos tanto para as entradas quanto para as saídas.
- Historicamente quando há valores contínuos, as redes com essas características eram chamadas de Adaline.
- <u>Limitação</u>: só consegue resolver problemas linearmente separáveis.

![](content/images/redesperceptron2023-02-_page_5_Picture_0.png)

Como definir a quantidade valores de entrada, de camadas e neurônios da rede?

- Como esta rede tem apenas 1 camada, precisamos apenas definir a os atributos de entrada e quantidade de neurônios desta única camada.
- Normalmente, define-se um neurônio para cada classe esperada.
- Para entender, vamos ver um exemplo...

![](content/images/redesperceptron2023-02-_page_6_Picture_0.png)

| cpf | nome   | renda | dívida | classificação do cliente |  |
|-----|--------|-------|--------|--------------------------|--|
| 111 | João   | 2000  | 1000   | bom                      |  |
| 222 | Maria  | 3000  | 2000   | mau                      |  |
| 333 | Pedro  | 1000  | 500    | mau                      |  |
| 444 | Carlos | 3000  | 1500   | bom                      |  |

Entradas: Quais são atributos podem ser usados como entrada para rede?

Saídas: Em quantas classes do algoritmo deve organizar os clientes?

![](content/images/redesperceptron2023-02-_page_7_Picture_0.png)

|   | cpf | nome         | renda | dívida | classificação do cliente | į |
|---|-----|--------------|-------|--------|--------------------------|---|
| 1 | 11, | loão         | 2000  | 1000   | bom                      |   |
| 2 | 22. | <b>daria</b> | 3000  | 2000   | mau                      |   |
| 3 | 33  | Pedro        | 1000  | 500    | mau                      |   |
| 4 | 44  | Carlos       | 3000  | 1500   | bom                      |   |
|   |     |              |       |        |                          |   |

2 atributos de entrada

Entradas: Quais são atributos podem ser usados como entrada para rede?

Saídas: Em quantas classes do algoritmo deve organizar os clientes?

![](content/images/redesperceptron2023-02-_page_8_Picture_0.png)

| cpf  | nome         | renda | dívida | classificação do cliente |
|------|--------------|-------|--------|--------------------------|
| 111  | oão          | 2000  | 1000   | bom                      |
| 222, | <b>Naria</b> | 3000  | 2000   | mau                      |
| 333  | Pedro        | 1000  | 500    | mau                      |
| 444  | Carlos       | 3000  | 1500   | bom                      |

2 classes como saida

Entradas: Quais são atributos podem ser usados como entrada para rede?

Saídas: Em quantas classes do algoritmo deve organizar os clientes?

#### Lembrando:

Redes neurais **trabalham somente com números**, por isso e comum realizar transformações nos dados.

E funcionam melhor com dados normalizados.

![](content/images/redesperceptron2023-02-_page_9_Picture_3.png)

![](content/images/redesperceptron2023-02-_page_10_Picture_0.png)

| renda dívida |      | classificação do cliente |  |  |
|--------------|------|--------------------------|--|--|
| 0,66         | 0,5  | 1                        |  |  |
| 1            | 1    | 0                        |  |  |
| 0,33         | 0,25 | 0                        |  |  |
| 1            | 0,75 | 1                        |  |  |

![](content/images/redesperceptron2023-02-_page_10_Picture_3.png)

#### Topologia menos usual.

#### Cada neurônio e capaz de decidir entre 2 classes:

- Quando a rede devolve 0, significa que não é um cliente bom.
- Quanto a rede devolve 1, significa que <u>é</u> um cliente bom.

![](content/images/redesperceptron2023-02-_page_11_Picture_0.png)

#### Classificação Cliente

| renda | dívida | D1 | D2 |
|-------|--------|----|----|
| 0,66  | 0,5    | 1  | 0  |
| 1     | 1      | 0  | 1  |
| 0,33  | 0,25   | 0  | 1  |
| 1     | 0,75   | 1  | 0  |

![](content/images/redesperceptron2023-02-_page_11_Picture_4.png)

#### Topologia mais usual.

- Haverá uma saída esperada para cada neurônio.
- A saída da rede é dependente dos vários neurônios.
- Pode ser escolhido aquele de maior valor de saída.

![](content/images/redesperceptron2023-02-_page_12_Picture_0.png)

### Classificação Cliente

| renda | dívida | D1 | D2 |  |
|-------|--------|----|----|--|
| 0,66  | 0,5    | 1  | 0  |  |
| 1     | 1      | 0  | 1  |  |
| 0,33  | 0,25   | 0  | 1  |  |
| 1     | 0,75   | 1  | 0  |  |

![](content/images/redesperceptron2023-02-_page_12_Picture_4.png)

#### Topologia mais usual.

- Haverá uma saída esperada para cada neurônio.
- A saída da rede é dependente dos vários neurônios.
- Pode ser escolhido aquele de maior valor de saída.

![](content/images/redesperceptron2023-02-_page_13_Picture_0.png)

### Classificação Cliente

| renda | dívida | D1 | D2 |  |
|-------|--------|----|----|--|
| 0,66  | 0,5    | 1  | 0  |  |
| 1     | 1      | 0  | 1  |  |
| 0,33  | 0,25   | 0  | 1  |  |
| 1     | 0,75   | 1  | 0  |  |

![](content/images/redesperceptron2023-02-_page_13_Picture_4.png)

#### Topologia mais usual.

- Haverá uma saída esperada para cada neurônio.
- A saída da rede é dependente dos vários neurônios.
- Pode ser escolhido aquele de maior valor de saída.

![](content/images/redesperceptron2023-02-_page_14_Picture_0.png)

### Classificação Cliente

| renda | dívida | D1 | D2 |  |
|-------|--------|----|----|--|
| 0,66  | 0,5    | 1  | 0  |  |
| 1     | 1      | 0  | 1  |  |
| 0,33  | 0,25   | 0  | 1  |  |
| 1     | 0,75   | 1  | 0  |  |

![](content/images/redesperceptron2023-02-_page_14_Picture_4.png)

#### Topologia mais usual.

- Haverá uma saída esperada para cada neurônio.
- A saída da rede é dependente dos vários neurônios.
- Pode ser escolhido aquele de maior valor de saída.

![](content/images/redesperceptron2023-02-_page_15_Picture_0.png)

### Classificação Cliente

| renda | dívida | D1 | D2 |  |
|-------|--------|----|----|--|
| 0,66  | 0,5    | 1  | 0  |  |
| 1     | 1      | 0  | 1  |  |
| 0,33  | 0,25   | 0  | 1  |  |
| 1     | 0,75   | 1  | 0  |  |

![](content/images/redesperceptron2023-02-_page_15_Picture_4.png)

#### Topologia mais usual.

- Haverá uma saída esperada para cada neurônio.
- A saída da rede é dependente dos vários neurônios.
- Pode ser escolhido aquele de maior valor de saída.

Mais exemplos de topologia ...

![](content/images/redesperceptron2023-02-_page_16_Picture_1.png)

# **Exemplo 1** – Dados estruturados

![](content/images/redesperceptron2023-02-_page_17_Picture_1.png)

## Planta Iris

![](content/images/redesperceptron2023-02-_page_18_Picture_1.png)

4 atributos de entrada

3 classes: Iris-setosa, Iris-versicolor, Iris-virginica

![](content/images/redesperceptron2023-02-_page_18_Picture_4.png)

|   | sepal_length | sepal_width | petal_length | petal_width | species     |
|---|--------------|-------------|--------------|-------------|-------------|
| 0 | 5.1          | 3.5         | 1.4          | 0.2         | Iris-setosa |
| 1 | 4.9          | 3.0         | 1.4          | 0.2         | Iris-setosa |
| 2 | 4.7          | 3.2         | 1.3          | 0.2         | Iris-setosa |
| 3 | 4.6          | 3.1         | 1.5          | 0.2         | Iris-setosa |
| 4 | 5.0          | 3.6         | 1.4          | 0.2         | Iris-setosa |
| 5 | 5.4          | 3.9         | 1.7          | 0.4         | Iris-setosa |
| 6 | 4.6          | 3.4         | 1.4          | 0.3         | Iris-setosa |
| 7 | 5.0          | 3.4         | 1.5          | 0.2         | Iris-setosa |
| 8 | 4.4          | 2.9         | 1.4          | 0.2         | Iris-setosa |
| 9 | 4.9          | 3.1         | 1.5          | 0.1         | Iris-setosa |

## Planta Iris

Corola (conjunto de pétalas)

Pétalas

Sépalas

Cálice (conjunto de sépalas)

4 atributos de entrada

2 classes: Iris-setosa, Nao Iris-setosa

![](content/images/redesperceptron2023-02-_page_19_Picture_4.png)

|   | sepal_length | sepal_width | petal_length | petal_width | species     |
|---|--------------|-------------|--------------|-------------|-------------|
| 0 | 5.1          | 3.5         | 1.4          | 0.2         | Iris-setosa |
| 1 | 4.9          | 3.0         | 1.4          | 0.2         | Iris-setosa |
| 2 | 4.7          | 3.2         | 1.3          | 0.2         | Iris-setosa |
| 3 | 4.6          | 3.1         | 1.5          | 0.2         | Iris-setosa |
| 4 | 5.0          | 3.6         | 1.4          | 0.2         | Iris-setosa |
| 5 | 5.4          | 3.9         | 1.7          | 0.4         | Iris-setosa |
| 6 | 4.6          | 3.4         | 1.4          | 0.3         | Iris-setosa |
| 7 | 5.0          | 3.4         | 1.5          | 0.2         | Iris-setosa |
| 8 | 4.4          | 2.9         | 1.4          | 0.2         | Iris-setosa |
| 9 | 4.9          | 3.1         | 1.5          | 0.1         | Iris-setosa |

![](content/images/redesperceptron2023-02-_page_20_Figure_0.png)

Atributos dos objetos

Entrada com Dados estruturados

![](content/images/redesperceptron2023-02-_page_21_Figure_0.png)

Atributos dos objetos

Entrada com Dados estruturados

### Planta Iris

# **Topologia para 2 classes**Classificador Binario Neural

Camada de entrada(dados): 4

Camada de saida (neuronios): 2

![](content/images/redesperceptron2023-02-_page_22_Picture_2.png)

Tipo de Planta Iris

| <b>x1</b> | <b>x2</b> | х3  | x4  | d1 | d2 |
|-----------|-----------|-----|-----|----|----|
| 5.1       | 3.5       | 1.4 | 0.2 | 1  | 0  |
| 7         | 3.2       | 4.7 | 1.4 | 0  | 1  |
|           |           |     |     |    |    |

Corola (conjunto de pétalas)

(conjunto de sépalas)

- Pétalas

Iris-Setosa Nao Iris-Setosa

# Exemplo 2 – Dados desestruturados

![](content/images/redesperceptron2023-02-_page_23_Picture_1.png)

• Considere como entrada de uma imagem de caracteres: 5 x 5.

![](content/images/redesperceptron2023-02-_page_24_Picture_2.png)

 Objetivo: identificar as imagens correspondentes a vogais:

![](content/images/redesperceptron2023-02-_page_24_Picture_4.png)

![](content/images/redesperceptron2023-02-_page_25_Figure_1.png)

Atributos dos objetos

![](content/images/redesperceptron2023-02-_page_26_Figure_1.png)

Atributos dos objetos

![](content/images/redesperceptron2023-02-_page_26_Picture_3.png)

![](content/images/redesperceptron2023-02-_page_27_Figure_1.png)

Topologia: 25 x 5

![](content/images/redesperceptron2023-02-_page_27_Picture_3.png)

| x1,x2,x3,,x25  | d1 | d2 | d3 | d4 | d5 |
|----------------|----|----|----|----|----|
| 1,1,1,1,1,0,   | 1  | 0  | 0  | 0  | 0  |
| 1,1,1,1,1,0,   | 0  | 1  | 0  | 0  | 0  |
| 0,0,1,0,0,0,0, | 0  | 0  | 1  | 0  | 0  |
| 1,1,1,1,1,0,   | 0  | 0  | 0  | 1  | 0  |
| 1,0,0,0,1,1,0, | 0  | 0  | 0  | 0  | 1  |
|                |    |    |    |    |    |

# Exemplo 3 – Dados desestruturados

![](content/images/redesperceptron2023-02-_page_28_Picture_1.png)

# Classificador de sentenças

![](content/images/redesperceptron2023-02-_page_29_Figure_1.png)

## Classificador de sentenças

![](content/images/redesperceptron2023-02-_page_30_Figure_1.png)

## Classificador de sentenças

![](content/images/redesperceptron2023-02-_page_31_Figure_1.png)

Veremos mais detalhes dessa topologia na aula sobre MultiLayer Perceptron.

Tipicamente esse problema não é linearmente separável. Ele precisa de uma rede várias camadas.

# Etapas Básicas de Construção de uma Rede Neural

![](content/images/redesperceptron2023-02-_page_32_Picture_1.png)

• Como já mencionado, essas redes só conseguem resolver problemas linearmente separáveis.

 O algoritmo de aprendizado desse tipo de rede, procura os coeficientes que traçam a reta que separa linearmente os dados de uma classe de outra.

![](content/images/redesperceptron2023-02-_page_33_Figure_3.png)

![](content/images/redesperceptron2023-02-_page_34_Figure_2.png)

$$v_j = w_{0j} + \sum_{i=1}^n (x_i \times w_{ij})$$

$$y_j = f(v_j)$$

![](content/images/redesperceptron2023-02-_page_35_Figure_2.png)

$$v_j = \sum_{i=0}^n (x_i \times w_{ij})$$

$$y_i = f(v_i)$$

- Existem várias funções de ativação para as redes neurais.
- As clássicas são:
  - Limiar ou degrau
  - Linear
  - Sigmoide: logistica ou tangente hiperbolica
- Geralmente o Perceptron usa a função limiar.

![](content/images/redesperceptron2023-02-_page_36_Figure_8.png)

![](content/images/redesperceptron2023-02-_page_37_Figure_2.png)

### Treinamento de Rede Neurais

### Dataset com dados históricos, pre-processado e anotado com classes:

- Divida o dataset (harmonicamente, no caso de classes), em conjuntos disjuntos de:
- treino: usado para o treinamento do modelo;
  - validação: usado para validar o modelo durante o treinamento;
  - teste: usado para verificar a solução, ou seja, a versão final do modelo, após

o treinamento.

![](content/images/redesperceptron2023-02-_page_38_Figure_7.png)

### Treinamento de Redes Neurais

Como os subconjuntos de treino, validação e teste são usados:

![](content/images/redesperceptron2023-02-_page_39_Figure_2.png)

Acurácia = Número de predições corretas

Total de predições

### Treinamento de Redes Neurais

- Os ciclos de treinamento de uma rede são medidos em épocas.
- Uma época corresponde a passagem de todos os dados do conjunto de treino uma vez pela rede.
- Para treinar uma rede são necessárias várias épocas.

## Rede Perceptron - Algoritmo de Treinamento

Algoritmo de Treinamento do Perceptron: usa Regra Delta (correção de erro)

- Sendo X = { (dados1;saidaDesejada1); (dados1;saidaDesejada2),...}
- A taxa de aprendizagem $\eta$ (deve ser positiva).

```
Inicializar todos pesos da rede com zero : wij = 0
Repetir ate encontrar erroGeral=0:
     epocas = epocas + 1
          erroGeral = 0
          Para cada neuronio j: 1 a k da rede :
          vi = 0
          Para cada atributo i: 0 a n dos dados de X :
               vj = vj + xi * wij
          yj = f(vj)
          erroj = dj - yj
          se erroj!=0 entao :
               delta = n * erroj * xi
               wij = wj + delta
     erroGeral = erroGeral + abs(erroj)
```

Qual o objetivo do treinamento de uma rede neural?

O que estamos procurando?

![](content/images/redesperceptron2023-02-_page_42_Picture_2.png)

# Os pesos sinápticos.

São neles que o conhecimento adquirido pela rede fica armazenado.

## Rede Perceptron – Limitações

### Tabela OR

| x1 | x2 | d |
|----|----|---|
| 0  | 0  | 0 |
| 0  | 1  | 1 |
| 1  | 0  | 1 |
| 1  | 1  | 1 |

![](content/images/redesperceptron2023-02-_page_44_Figure_3.png)

## Rede Perceptron – Limitações

### Tabela XOR

| $\times$1 | x2 | d |
|----|----|---|
| 0  | 0  | 0 |
| 0  | 1  | 1 |
| 1  | 0  | 1 |
| 1  | 1  | 0 |

![](content/images/redesperceptron2023-02-_page_45_Figure_3.png)

- **Pesos** inicializados com zero:  $w_{10} = 0, w_{11} = 0, w_{12} = 0$
- limiar:  $Q(v_k) = \begin{array}{cc} 1 & se \ v_k \geq 0 \\ 0 & caso \ contr \acute{a}rio \end{array}$  , taxa de aprendizagem:  $\eta = 1$

| <b>x1</b> | <b>x2</b> | d | x0 = 1                                    |
|-----------|-----------|---|-------------------------------------------|
| 0         | 0         | 0 | 0 x1 $w11=0.0$ $w10=0.0$                  |
| 0         | 1         | 1 | $0  x2 \qquad 1 \longrightarrow y1 = 1.0$ |
| 1         | 0         | 1 | w12 = 0.0                                 |
| 1         | 1         | 1 | propagação                                |

- $v_1 = x_0 \times w_{10} + x_1 \times w_{11} + x_2 \times w_{12}$
- $v_1 = 1 \times 0 + 0 \times 0 + 0 \times 0 = 0$
- $y_1 = Q(v_1) = Q(0) = 1.0$

- Ajuste dos pesos (Aplicando a regra delta)
  - $erro_1 = d_1 y_1 = 0 1.0 = -1.0$
  - $w_{10} = w_{10} + \eta \times erro_1 \times x_0 = 0.0 + 1 \times -1.0 \times 1 = -1.0$
  - $w_{11} = w_{11} + \eta \times erro_1 \times x_1 = 0.0 + 1 \times -1.0 \times 0 = 0.0$
  - $w_{12} = w_{12} + \eta \times erro_1 \times x_2 = 0.0 + 1 \times -1.0 \times 0 = 0.0$

- Pesos atuais:  $w_{10} = -1.0, w_{11} = 0.0, w_{12} = 0.0$
- limiar:  $Q(v_k) = \begin{array}{ccc} 1 & se \, v_k \geq 0 \\ 0 & caso \, contr \acute{a}rio \end{array}$  , taxa de aprendizagem:  $\eta = 1$

| <b>x1</b> | <b>x2</b> | d | x0 = 1                      |
|-----------|-----------|---|-----------------------------|
| 0         | 0         | 0 | 0 x1 $w11=0.0$ $w10 = -1.0$ |
| 0         | 1         | 1 | 1 $x_2$ 1 $y_1 = 0.0$       |
| 1         | 0         | 1 | w12 = 0.0                   |
| 1         | 1         | 1 | propagação                  |

- $v_1 = x_0 \times w_{10} + x_1 \times w_{11} + x_2 \times w_{12}$
- $v_1 = 1 \times -1.0 + 0 \times 0.0 + 1 \times 0.0 = -1.0$
- $y_1 = Q(v_1) = Q(-1.0) = 0.0$
- Ajuste dos pesos (Aplicando a regra delta)
  - $erro_1 = d_1 y_1 = 1 0.0 = 1.0$
  - $w_{10} = w_{10} + \eta \times erro_1 \times x_0 = -1.0 + 1 \times 1.0 \times 1 = 0.0$
  - $w_{11} = w_{11} + \eta \times erro_1 \times x_1 = 0.0 + 1 \times 1.0 \times 0 = 0.0$
  - $w_{12} = w_{12} + \eta \times erro_1 \times x_2 = 0.0 + 1 \times 1.0 \times 1 = 1.0$

- Pesos atuais:  $w_{10} = 0.0, w_{11} = 0.0, w_{12} = 1.0$
- limiar:  $Q(v_k) = \begin{array}{ccc} 1 & se \, v_k \geq 0 \\ 0 & caso \, contr \acute{a}rio \end{array}$  , taxa de aprendizagem:  $\eta = 1$

| <b>x1</b> | <b>x2</b> | d |   |           |            | x0 = 1              |
|-----------|-----------|---|---|-----------|------------|---------------------|
| 0         | 0         | 0 | 1 | <b>x1</b> | w11=0.0    | W10 = 0.0           |
| 0         | 1         | 1 | 0 | x2        |            | 1 → Y1 = <b>1.0</b> |
| 1         | 0         | 1 |   |           | W12 = 1.0  | 0<br>               |
| 1         | 1         | 1 |   |           | propagação |                     |

- $v_1 = x_0 \times w_{10} + x_1 \times w_{11} + x_2 \times w_{12}$
- $v_1 = 1 \times 0.0 + 1 \times 0.0 + 0 \times 1.0 = 0.0$
- $y_1 = Q(v_1) = Q(0.0) = 1.0$

- Ajuste dos pesos (Aplicando a regra delta)
  - $erro_1 = d_1 y_1 = 1 1.0 = 0.0$ 
    - quando o erro é zero, não há ajuste de pesos.

- Pesos atuais:  $w_{10} = 0.0, w_{11} = 0.0, w_{12} = 1.0$
- limiar:  $Q(v_k) = \begin{array}{ccc} 1 & se \, v_k \geq 0 \\ 0 & caso \, contr \alpha rio \end{array}$  , taxa de aprendizagem:  $\eta = 1$

| <b>x1</b> | <b>x2</b> | d | x0 = 1                   |
|-----------|-----------|---|--------------------------|
| 0         | 0         | 0 | 1 x1 $w11=0.0$ $w10=0.0$ |
| 0         | 1         | 1 | 1 $\times$2 1.0                 |
| 1         | 0         | 1 | W12 = 1.0                |
| 1         | 1         | 1 | propagação               |

- $v_1 = x_0 \times w_{10} + x_1 \times w_{11} + x_2 \times w_{12}$
- $v_1 = 1 \times 0.0 + 1 \times 0.0 + 1 \times 1.0 = 1.0$
- $y_1 = Q(v_1) = Q(1.0) = 1.0$

- Ajuste dos pesos (Aplicando a regra delta)
  - $erro_1 = d_1 y_1 = 1 1.0 = 0.0$ 
    - quando o erro é zero, não há ajuste de pesos.

- Erro Acumulado para época 1 :
  - Erro Geral:
    - $\bullet = abs(erroEntrada1) + abs(erroEntrada2) + abs(erroEntrada3) + abs(erroEntrada4) =$
    - $\bullet = abs(-1.0) + abs(1.0) + abs(0.0) + abs(0.0)$
    - = 2.0
- Como ainda há erro, o algoritmo prossegue ...

- Pesos atuais:  $w_{10} = 0.0, w_{11} = 0.0, w_{12} = 1.0$
- $\bullet$  limiar:  $Q(v_k)=\begin{array}{ccc} 1 & se \, v_k \geq 0 \ 0 & caso \, contr \alpha rio \end{array}$  , taxa de aprendizagem:  $\eta=1$

| <b>x1</b> | <b>x2</b> | d |   |           |            | x0 = 1       |
|-----------|-----------|---|---|-----------|------------|--------------|
| 0         | 0         | 0 | 0 | <b>x1</b> | w11=0.0    | W10 = 0.0    |
| 0         | 1         | 1 | 0 | x2        |            | 1 > Y1 = 1.0 |
| 1         | 0         | 1 |   |           | W12 = 1.0  |              |
| 1         | 1         | 1 |   |           | propagação |              |

- $v_1 = x_0 \times w_{10} + x_1 \times w_{11} + x_2 \times w_{12}$
- $v_1 = 0 \times 0.0 + 0 \times 1.0 + 1 \times 0.0 = 0.0$
- $y_1 = Q(v_1) = Q(0.0) = 1.0$

- Ajuste dos pesos (Aplicando a regra delta)
  - $erro_1 = d_1 y_1 = 0 1.0 = -1.0$
  - $w_{10} = w_{10} + \eta \times erro_1 \times x_0 = 0.0 + 1 \times -1.0 \times 1 = -1.0$
  - $w_{11} = w_{11} + \eta \times erro_1 \times x_1 = 0.0 + 1 \times -1.0 \times 0 = 0.0$
  - $w_{12} = w_{12} + \eta \times erro_1 \times x_2 = 1.0 + 1 \times -1.0 \times 0 = 1.0$

- Pesos atuais:  $w_{10} = -1.0, w_{11} = 0.0, w_{12} = 1.0$
- limiar:  $Q(v_k) = \begin{array}{ccc} 1 & se \ v_k \geq 0 \\ 0 & caso \ contr \'ario \end{array}$  , taxa de aprendizagem:  $\eta = 1$

| <b>x1</b> | <b>x2</b> | d |   |    |            | x0 = 1              |
|-----------|-----------|---|---|----|------------|---------------------|
| 0         | 0         | 0 | 0 | x1 | w11=0.0    | W10 = -1.0          |
| 0         | 1         | 1 | 1 | x2 |            | 1 → Y1 = <b>1.0</b> |
| 1         | 0         | 1 |   |    | W12 = 1.0  | 0<br><b></b>        |
| 1         | 1         | 1 |   | ķ  | oropagação | 0                   |

- $v_1 = x_0 \times w_{10} + x_1 \times w_{11} + x_2 \times w_{12}$
- $v_1 = 1 \times -1.0 + 0 \times 0.0 + 1 \times 1.0 = 0.0$
- $y_1 = Q(v_1) = Q(0.0) = 1.0$

- Ajuste dos pesos (Aplicando a regra delta)
  - $erro_1 = d_1 y_1 = 1 1.0 = 0.0$ 
    - quando o erro é zero, não há ajuste de pesos.

- Pesos atuais:  $w_{10} = -1.0, w_{11} = 0.0, w_{12} = 1.0$
- limiar:  $Q(v_k) = \begin{array}{ccc} 1 & se \, v_k \geq 0 \\ 0 & caso \, contr \acute{a}rio \end{array}$  , taxa de aprendizagem:  $\eta = 1$

| <b>x1</b> | <b>x2</b> | d | x0 = 1                      |
|-----------|-----------|---|-----------------------------|
| 0         | 0         | 0 | 1 x1 $w11=0.0$ $w10 = -1.0$ |
| 0         | 1         | 1 | 0 X2 Y1 = 0.0               |
| 1         | 0         | 1 | W12 = 1.0                   |
| 1         | 1         | 1 | propagação                  |

- $v_1 = x_0 \times w_{10} + x_1 \times w_{11} + x_2 \times w_{12}$
- .0  $v_1 = 1 \times -1.0 + 1 \times 0.0 + 0 \times 1.0 = -1.0$ 
  - $y_1 = Q(v_1) = Q(-1.0) = 0.0$
- Ajuste dos pesos (Aplicando a regra delta)
  - $erro_1 = d_1 y_1 = 1 0.0 = 1.0$
  - $w_{10} = w_{10} + \eta \times erro_1 \times x_0 = -1.0 + 1 \times 1.0 \times 1 = 0.0$
  - $w_{11} = w_{11} + \eta \times erro_1 \times x_1 = 0.0 + 1 \times 1.0 \times 1 = 1.0$
  - $w_{12} = w_{12} + \eta \times erro_1 \times x_2 = 1.0 + 1 \times 1.0 \times 0 = 1.0$

- Pesos atuais:  $w_{10} = 0.0, w_{11} = 1.0, w_{12} = 1.0$
- limiar:  $Q(v_k) = \begin{array}{ccc} 1 & se \, v_k \geq 0 \\ 0 & caso \, contr \acute{a}rio \end{array}$  , taxa de aprendizagem:  $\eta = 1$

| <b>x1</b> | <b>x2</b> | d | x0 = 1                   |
|-----------|-----------|---|--------------------------|
| 0         | 0         | 0 | 1 x1 $w11=1.0$ $w10=0.0$ |
| 0         | 1         | 1 | 1 $\times$2 1.0                 |
| 1         | 0         | 1 | w12 = 1.0                |
| 1         | 1         | 1 | propagação               |

- $v_1 = x_0 \times w_{10} + x_1 \times w_{11} + x_2 \times w_{12}$
- $v_1 = 1 \times 0.0 + 1 \times 1.0 + 1 \times 1.0 = 2.0$
- $y_1 = Q(v_1) = Q(2.0) = 1.0$

- Ajuste dos pesos (Aplicando a regra delta)
  - $erro_1 = d_1 y_1 = 1 1.0 = 0.0$ 
    - quando o erro é zero, não há ajuste de pesos.

- Erro Acumulado para época 2 :
  - Erro Geral:
    - = abs(erroEntrada1) + abs(erroEntrada2) + abs(erroEntrada3) + abs(erroEntrada4) =
    - $\bullet = abs(-1.0) + abs(0.0) + abs(1.0) + abs(0.0)$
    - $\bullet = 2.0$
- Como ainda há erro, o algoritmo prossegue ...

- Pesos atuais:  $w_{10} = 0.0, w_{11} = 1.0, w_{12} = 1.0$
- $\bullet$  limiar:  $Q(v_k)=\begin{array}{ccc} 1 & se \, v_k \geq 0 \ 0 & caso \, contr \alpha rio \end{array}$  , taxa de aprendizagem:  $\eta=1$

| <b>x1</b> | <b>x2</b> | d | x0 = 1                                    |
|-----------|-----------|---|-------------------------------------------|
| 0         | 0         | 0 | 0 x1 $w11=1.0$ $w10=0.0$                  |
| 0         | 1         | 1 | $0  X2 \qquad 1 \longrightarrow Y1 = 1.0$ |
| 1         | 0         | 1 | w12 = 1.0                                 |
| 1         | 1         | 1 | propagação                                |

- $v_1 = x_0 \times w_{10} + x_1 \times w_{11} + x_2 \times w_{12}$
- $v_1 = 1 \times 0.0 + 0 \times 1.0 + 0 \times 1.0 = 0.0$ 
  - $y_1 = Q(v_1) = Q(0.0) = 1.0$

- Ajuste dos pesos (Aplicando a regra delta)
  - $erro_1 = d_1 y_1 = 0 1.0 = -1.0$
  - $w_{10} = w_{10} + \eta \times erro_1 \times x_0 = 0.0 + 1 \times -1.0 \times 1 = -1.0$
  - $w_{11} = w_{11} + \eta \times erro_1 \times x_1 = 1.0 + 1 \times -1.0 \times 0 = 1.0$
  - $w_{12} = w_{12} + \eta \times erro_1 \times x_2 = 1.0 + 1 \times -1.0 \times 0 = 1.0$

- Pesos atuais:  $w_{10} = -1.0, w_{11} = 1.0, w_{12} = 1.0$
- limiar:  $Q(v_k) = \begin{array}{ccc} 1 & se \, v_k \geq 0 \\ 0 & caso \, contr \acute{a}rio \end{array}$  , taxa de aprendizagem:  $\eta = 1$

| <b>x1</b> | <b>x2</b> | d |      | x0 = 1                 |
|-----------|-----------|---|------|------------------------|
| 0         | 0         | 0 | 0 x1 | w11 = 1.0 $w10 = -1.0$ |
| 0         | 1         | 1 | 1 X  | 1 Y1 = 1.0             |
| 1         | 0         | 1 |      | w12 = 1.0              |
| 1         | 1         | 1 |      | propagação             |

- $v_1 = x_0 \times w_{10} + x_1 \times w_{11} + x_2 \times w_{12}$
- $v_1 = 1 \times -1.0 + 0 \times 1.0 + 1 \times 1.0 = 0.0$
- $y_1 = Q(v_1) = Q(0.0) = 1.0$

- Ajuste dos pesos (Aplicando a regra delta)
  - $erro_1 = d_1 y_1 = 1 1.0 = 0.0$ 
    - quando o erro é zero, não há ajuste de pesos.

- Pesos atuais:  $w_{10} = -1.0, w_{11} = 1.0, w_{12} = 1.0$
- limiar:  $Q(v_k) = \begin{array}{ccc} 1 & se \, v_k \geq 0 \\ 0 & caso \, contr \acute{a}rio \end{array}$  , taxa de aprendizagem:  $\eta = 1$

| <b>x1</b> | <b>x2</b> | d |      | x0 = 1             |
|-----------|-----------|---|------|--------------------|
| 0         | 0         | 0 | 1 x1 | w11=1.0 $w10=-1.0$ |
| 0         | 1         | 1 | 0 x2 | 1 Y1 = 1.0         |
| 1         | 0         | 1 |      | w12 = 1.0          |
| 1         | 1         | 1 | 1    | oropagação         |

- $v_1 = x_0 \times w_{10} + x_1 \times w_{11} + x_2 \times w_{12}$
- $v_1 = 1 \times -1.0 + 1 \times 1.0 + 0 \times 1.0 = 0.0$
- $y_1 = Q(v_1) = Q(0.0) = 1.0$

- Ajuste dos pesos (Aplicando a regra delta)
  - $erro_1 = d_1 y_1 = 1 1.0 = 0.0$ 
    - quando o erro é zero, não há ajuste de pesos.

- Pesos atuais:  $w_{10} = -1.0, w_{11} = 1.0, w_{12} = 1.0$
- limiar:  $Q(v_k) = \begin{array}{ccc} 1 & se \ v_k \geq 0 \\ 0 & caso \ contr \acute{a}rio \end{array}$  , taxa de aprendizagem:  $\eta = 1$

| <b>x1</b> | <b>x2</b> | d | x0 = 1                    |
|-----------|-----------|---|---------------------------|
| 0         | 0         | 0 | 1 x1 $w11=1.0$ $w10=-1.0$ |
| 0         | 1         | 1 | 1 $\times$2 1.0                  |
| 1         | 0         | 1 | w12 = 1.0                 |
| 1         | 1         | 1 | propagação                |

- $v_1 = x_0 \times w_{10} + x_1 \times w_{11} + x_2 \times w_{12}$
- $v_1 = 1 \times -1.0 + 1 \times 1.0 + 1 \times 1.0 = 1.0$
- $y_1 = Q(v_1) = Q(1.0) = 1.0$

- Ajuste dos pesos (Aplicando a regra delta)
  - $erro_1 = d_1 y_1 = 1 1.0 = 0.0$ 
    - quando o erro é zero, não há ajuste de pesos.

- Erro Acumulado para época 3 :
  - Erro Geral:
    - = abs(erroEntrada1) + abs(erroEntrada2) + abs(erroEntrada3) + abs(erroEntrada4) =
    - = abs(-1.0) + abs(0.0) + abs(0.0) + abs(0.0)
    - $\bullet = 1.0$
- Como ainda há erro, o algoritmo prossegue ...

- Pesos atuais:  $w_{10} = -1.0, w_{11} = 1.0, w_{12} = 1.0$
- limiar:  $Q(v_k) = \begin{pmatrix} 1 & se \ v_k \geq 0 \\ 0 & caso \ contr \'ario \end{pmatrix}$  , taxa de aprendizagem:  $\eta = 1$

| <b>x1</b> | <b>x2</b> | d | x0 = 1                                |
|-----------|-----------|---|---------------------------------------|
| 0         | 0         | 0 | 0 x1 $w11=1.0$ $w10=-1.0$             |
| 0         | 1         | 1 | $0  X2 \qquad 1 \rightarrow Y1 = 0.0$ |
| 1         | 0         | 1 | w12 = 1.0                             |
| 1         | 1         | 1 | propagação                            |

- $v_1 = x_0 \times w_{10} + x_1 \times w_{11} + x_2 \times w_{12}$
- $v_1 = 1 \times -1.0 + 0 \times 1.0 + 0 \times 1.0 = -1.0$
- $y_1 = Q(v_1) = Q(-1.0) = 0.0$
- Ajuste dos pesos (Aplicando a regra delta)
  - $erro_1 = d_1 y_1 = 0 0.0 = 0.0$ 
    - quando o erro é zero, não há ajuste de pesos.

- Pesos atuais:  $w_{10} = -1.0, w_{11} = 1.0, w_{12} = 1.0$
- limiar:  $Q(v_k) = \begin{pmatrix} 1 & se \ v_k \geq 0 \\ 0 & caso \ contr \acute{a}rio \end{pmatrix}$ , taxa de aprendizagem:  $\eta = 1$

| <b>x1</b> | <b>x2</b> | d |   |           | x0 = 1             |     |
|-----------|-----------|---|---|-----------|--------------------|-----|
| 0         | 0         | 0 | 0 | <b>x1</b> | w11=1.0 $w10=-1.0$ |     |
| 0         | 1         | 1 | 1 | x2        | 1 Y1 = 1           | L.0 |
| 1         | 0         | 1 |   |           | w12 = 1.0          |     |
| 1         | 1         | 1 |   |           | propagação         |     |

- $v_1 = x_0 \times w_{10} + x_1 \times w_{11} + x_2 \times w_{12}$
- $v_1 = 1 \times -1.0 + 0 \times 1.0 + 1 \times 1.0 = 0.0$ 
  - $y_1 = Q(v_1) = Q(0.0) = 1.0$

- Ajuste dos pesos (Aplicando a regra delta)
  - $erro_1 = d_1 y_1 = 1 1.0 = 0.0$ 
    - quando o erro é zero, não há ajuste de pesos.

- Pesos atuais:  $w_{10} = -1.0, w_{11} = 1.0, w_{12} = 1.0$
- limiar:  $Q(v_k) = \begin{array}{ccc} 1 & se \, v_k \geq 0 \\ 0 & caso \, contr \acute{a}rio \end{array}$  , taxa de aprendizagem:  $\eta = 1$

| <b>x1</b> | <b>x2</b> | d |   |           | ;          | x0 = 1     |
|-----------|-----------|---|---|-----------|------------|------------|
| 0         | 0         | 0 | 1 | <b>x1</b> | w11= 1.0   | w10 = -1.0 |
| 0         | 1         | 1 | 0 | x2        |            | 1 Y1 = 1.0 |
| 1         | 0         | 1 |   |           | w12 = 1.0  |            |
| 1         | 1         | 1 |   |           | propagação |            |

- $v_1 = x_0 \times w_{10} + x_1 \times w_{11} + x_2 \times w_{12}$
- $v_1 = 1 \times -1.0 + 1 \times 1.0 + 0 \times 1.0 = 0.0$
- $y_1 = Q(v_1) = Q(0.0) = 1.0$

- Ajuste dos pesos (Aplicando a regra delta)
  - $erro_1 = d_1 y_1 = 1 1.0 = 0.0$ 
    - quando o erro é zero, não há ajuste de pesos.

- Pesos atuais:  $w_{10} = -1.0, w_{11} = 1.0, w_{12} = 1.0$
- limiar:  $Q(v_k) = \begin{array}{ccc} 1 & se \ v_k \geq 0 \\ 0 & caso \ contr \'ario \end{array}$  , taxa de aprendizagem:  $\eta = 1$

| <b>x1</b> | <b>x2</b> | d |      | x0 = 1             |
|-----------|-----------|---|------|--------------------|
| 0         | 0         | 0 | 1 x1 | w11=1.0 $w10=-1.0$ |
| 0         | 1         | 1 | 1 x2 | 1 Y1 = 1.0         |
| 1         | 0         | 1 |      | w12 = 1.0          |
| 1         | 1         | 1 | 1    | oropagação         |

- $v_1 = x_0 \times w_{10} + x_1 \times w_{11} + x_2 \times w_{12}$
- $v_1 = 1 \times -1.0 + 1 \times 1.0 + 1 \times 1.0 = 1.0$
- $y_1 = Q(v_1) = Q(1.0) = 1.0$

- Ajuste dos pesos (Aplicando a regra delta)
  - $erro_1 = d_1 y_1 = 1 1.0 = 0.0$ 
    - quando o erro é zero, não há ajuste de pesos.

- Erro Acumulado para época 4 :
  - Erro Geral:
    - $\bullet$  = abs(erroEntrada1) + abs(erroEntrada2) + <math>abs(erroEntrada3) + abs(erroEntrada4) =
    - $\bullet = abs(0.0) + abs(0.0) + abs(0.0) + abs(0.0)$
    - $\bullet = 0.0$
  - O algoritmo pára.
- Resultado:
  - O algoritmo encontrou os pesos adequados:

$$w_{10} = -1.0, w_{11} = 1.0, w_{12} = 1.0$$

A rede está pronta para ser testada (ou usada).

Carrega-se, na topologia da rede, os pesos encontrados na fase de treinamento.

![](content/images/redesperceptron2023-02-_page_66_Figure_3.png)

Modelo = Corresponde a uma instancia do Algoritmo de IA gerada a partir dos dados de treinamento

Esta fase implementa apenas a propagação. Informa-se novos valores para as entradas e a rede gera a saída correspondente.

#### Testando o modelo:

| x1 | x2 |  |
|----|----|--|
| 0  | 0  |  |
| 0  | 1  |  |
| 1  | 0  |  |
| 1  | 1  |  |

![](content/images/redesperceptron2023-02-_page_67_Figure_3.png)

$$v_{j} = \sum_{i=0}^{n} (x_{i} \times w_{ij})$$
$$y_{j} = f(v_{j})$$

Função de ativação-Limiar
$$f(v_j) = \begin{cases} 1 \text{ se } v_j \ge 0 \\ 0 \text{ se } v_j < 0 \end{cases}$$

#### Testando o modelo:

![](content/images/redesperceptron2023-02-_page_68_Picture_2.png)

![](content/images/redesperceptron2023-02-_page_68_Figure_3.png)

$$v1 = 1 \times -1.0 + 0 \times 1.0 + 0 \times 1.0 = -1$$

$$v1 = Q(-1) = \mathbf{0}$$

$$v_j = \sum_{i=0}^n (x_i \times w_{ij})$$

$$y_j = f(v_j)$$

$$f(v_j) = \begin{cases} 1 \text{ se } v_j \ge 0\\ 0 \text{ se } v_j < 0 \end{cases}$$

#### Testando o modelo:

![](content/images/redesperceptron2023-02-_page_69_Picture_2.png)

![](content/images/redesperceptron2023-02-_page_69_Figure_3.png)

$$v1 = 1 \times -1.0 + 0 \times 1.0 + 0 \times 1.0 = 0$$

$$1 \times 1.0 = 0$$

$$Y1 = Q(0) = 1$$

$$v_j = \sum_{i=0}^n (x_i \times w_{ij})$$

$$y_j = f(v_j)$$

$$f(v_j) = \begin{cases} 1 \text{ se } v_j \ge 0\\ 0 \text{ se } v_j < 0 \end{cases}$$

#### Testando o modelo:

![](content/images/redesperceptron2023-02-_page_70_Figure_2.png)

![](content/images/redesperceptron2023-02-_page_70_Figure_3.png)

$$v1 = 1 \times -1.0 +$$
 $1 \times 1.0$ 
 $0 \times 1.0$ 
 $= 0$ 
 $Y1 = Q(0) = 1$ 

$$v_j = \sum_{i=0}^n (x_i \times w_{ij})$$

$$y_j = f(v_j)$$

$$f(v_j) = \begin{cases} 1 \text{ se } v_j \ge 0\\ 0 \text{ se } v_j < 0 \end{cases}$$

#### Testando o modelo:

| $\times$1 | x2 |  |
|----|----|--|
| 0  | 0  |  |
| 0  | 1  |  |
| 1  | 0  |  |
| 1  | 1  |  |

![](content/images/redesperceptron2023-02-_page_71_Figure_3.png)

$$v1 = 1 \times -1.0 + 1 \times 1.0 + 1 \times 1.0 = 1$$

$$v1 = 1 \times 1.0 = 1$$

$$v1 = Q(1) = 1$$

$$v_j = \sum_{i=0}^n (x_i \times w_{ij})$$

$$y_j = f(v_j)$$

$$f(v_j) = \begin{cases} 1 \text{ se } v_j \ge 0\\ 0 \text{ se } v_j < 0 \end{cases}$$

- Atividade 1: Implemente em Python o algoritmo de treinamento da rede Perceptron para as tabelas:
  - OR
  - AND
  - XOR

 Atividade 2: Considere os dados da tabela, selecione os atributos mais adequados, faca o pre-processamento. E, a seguir, use uma rede perceptron para classificar os clientes. Use a mesma topologia da atividade anterior.

| Cliente | Renda | Dívida | Classe |  |
|---------|-------|--------|--------|--|
| 101     | 2800  | 550    | bom    |  |
| 102     | 1300  | 500    | mau    |  |
| 103     | 1400  | 80     | bom    |  |
| 104     | 500   | 200    | mau    |  |
| 105     | 1100  | 270    | mau    |  |
| 106     | 1800  | 450    | bom    |  |
| 107     | 2400  | 650    | bom    |  |
| 108     | 1950  | 600    | bom    |  |
| 109     | 450   | 70     | mau    |  |
| 110     | 2750  | 730    | bom    |  |
| 111     | 850   | 90     | mau    |  |
| 112     | 1300  | 200    | mau    |  |
| 113     | 2100  | 750    | bom    |  |
| 114     | 900   | 300    | mau    |  |
| 115     | 2700  | 250    | bom    |  |
| 116     | 1600  | 500    | mau    |  |
| 117     | 1900  | 150    | bom    |  |
| 118     | 2500  | 800    | bom    |  |
| 119     | 1600  | 700    | mau    |  |
| 120     | 2300  | 500    | bom    |  |
| 121     | 2100  | 250    | bom    |  |

• Atividade 3: Implemente em Python o algoritmo de treinamento da rede Perceptron como classificador binário para Planta Iris. Calcule também a acurácia.

### Planta Iris

# **Topologia para 2 classes**Classificador Binario Neural

Camada de entrada(dados): 4

Camada de saida (neuronios): 2

![](content/images/redesperceptron2023-02-_page_75_Picture_2.png)

Tipo de Planta Iris

| <b>x1</b> | <b>x2</b> | х3  | x4  | d1 | d2 |
|-----------|-----------|-----|-----|----|----|
| 5.1       | 3.5       | 1.4 | 0.2 | 1  | 0  |
| 7         | 3.2       | 4.7 | 1.4 | 0  | 1  |
|           |           |     |     |    |    |

Corola (conjunto de pétalas)

(conjunto de sépalas)

- Pétalas

Iris-Setosa Nao Iris-Setosa

• Atividade 4: Implemente em Python o algoritmo de treinamento da rede Perceptron para reconhecer as letras. Teste usando letras com ruido.

![](content/images/redesperceptron2023-02-_page_76_Figure_2.png)

Atributos dos objetos Topologia: 25 x 2
