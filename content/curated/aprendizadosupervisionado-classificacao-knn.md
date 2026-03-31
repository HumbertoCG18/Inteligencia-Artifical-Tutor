#### Aprendizado Supervisionado Parte 1

Classificação com k-NN

Profa Silvia Moraes

![](content/images/aprendizadosupervisionado-classificacao-knn-_page_0_Picture_3.png)

#### **Roteiro**

- Relembrando
  - Machine Learning: Aprendizado Supervisionado
  - Tarefas Preditivas
- Classificação
  - Classificadores Lineares
  - Algoritmo k-NN

## **Subáreas da Inteligência Artificial**

![](content/images/aprendizadosupervisionado-classificacao-knn-_page_2_Figure_1.png)

#### **Aprendizado Supervisionado**

- Exige que os **dados** estejam **rotulados** (anotados com suas respectivas classes/valores de saída)
- Os algoritmos que seguem esse tipo de aprendizado recebem pares de valores:
  - os dados de entrada (x) e
  - os valores de saída (rótulos) correspondentes (y).

![](content/images/aprendizadosupervisionado-classificacao-knn-_page_3_Picture_5.png)

**DatasetAnotado**

#### **Aprendizado Supervisionado**

#### Em um conjunto de dados (exemplos) rotulado :

• Cada dado corresponde a um indivíduo do domínio e é formado por uma tupla contendo características (features).

**Atributo de entrada** (atributo previsor)

| sepal length | sepal width | petal length | petal width | class           |
|--------------|-------------|--------------|-------------|-----------------|
| 5,1          | 3,5         | 1,4          | 0,2         | Iris-setosa     |
| 4,9          | 3,0         | 1,4          | 0,2         | Iris-setosa     |
| 7,0          | 3,2         | 4,7          | 7,1         | Iris-versicolor |
| 6,4          | 3,2         | 4,5          | 1,5         | Iris-versicolor |
| 6,3          | 3,3         | 6,0          | 2,5         | Iris-virginica  |
| 5,8          | 2,7         | 5,1          | 1,9         | Iris-virginica  |
|              |             |              |             |                 |
|              |             |              |             |                 |

**Atributo de saída** (atributo alvo ou meta)

**Rótulo (Classes)**

![](content/images/aprendizadosupervisionado-classificacao-knn-_page_4_Picture_7.png)

#### **Aprendizado Supervisionado**

- O objetivo é encontrar um modelo capaz de mapear os valores de entrada (x) nos valores de saída y.
- Em outras palavras, que aproxime *f*, tal que *f(x) = y*.
- Supervisão: ajuste usando o erro em relação à saída esperada.

![](content/images/aprendizadosupervisionado-classificacao-knn-_page_5_Figure_4.png)

**DatasetAnotado**

![](content/images/aprendizadosupervisionado-classificacao-knn-_page_6_Picture_0.png)

#### **Aprendizado Supervisionado**

- **Tarefa preditiva**: encontra uma função (modelo) a partir dos dados de treino que possa ser usada para prever um rótulo (classe) ou valor de um novo exemplo.
- Pode ser:
  - **classificação** (rótulos discretos)
  - **regressão** (rótulos contínuos)

![](content/images/aprendizadosupervisionado-classificacao-knn-_page_7_Figure_1.png)

- É o processo de automaticamente atribuir rótulos a dados.
- Pode ser do tipo
  - Binária: possui apenas duas classes
  - Multiclasse: possui mais de duas classes
- Pode atribuir
  - Um único rótulo (single label)
  - Vários rótulos (multi-label)

![](content/images/aprendizadosupervisionado-classificacao-knn-_page_7_Picture_9.png)

#### **Regressão**

- É o processo de automaticamente predizer novos valores y.
- Neste caso, os dados são anotados com valores.

![](content/images/aprendizadosupervisionado-classificacao-knn-_page_8_Figure_3.png)

![](content/images/aprendizadosupervisionado-classificacao-knn-_page_8_Figure_4.png)

#### Regressão

![](content/images/aprendizadosupervisionado-classificacao-knn-_page_9_Figure_1.png)

![](content/images/aprendizadosupervisionado-classificacao-knn-_page_9_Figure_2.png)

![](content/images/aprendizadosupervisionado-classificacao-knn-_page_10_Picture_1.png)

![](content/images/aprendizadosupervisionado-classificacao-knn-_page_11_Picture_1.png)

![](content/images/aprendizadosupervisionado-classificacao-knn-_page_11_Picture_2.png)

Como classificar Gafanhotos ?

Se os dados desses insetos fossem estruturados, que atributos/características seriam mais importantes e significativos para a classificação?

![](content/images/aprendizadosupervisionado-classificacao-knn-_page_12_Picture_2.png)

Se os dados desses insetos fossem estruturados, que atributos/características seriam mais importantes e significativos para a classificação?

![](content/images/aprendizadosupervisionado-classificacao-knn-_page_13_Picture_2.png)

![](content/images/aprendizadosupervisionado-classificacao-knn-_page_14_Picture_1.png)

Se tivermos um conjunto de dados anotados com as classes dos gafanhotos, poderemos aplicar um algoritmo de classificação para predizer a classe de novos insetos desse tipo.

| ID | Compr.<br>Abdômen | Compr.<br>Antenas | Classe    | ID | Compr.<br>Abdômen | Compr.<br>Antenas | Classe    |
|----|-------------------|-------------------|-----------|----|-------------------|-------------------|-----------|
| 1  | 2,7               | 5,5               | Gafanhoto | 6  | 2,9               | 1,9               | Gafanhoto |
| 2  | 8,0               | 9,1               | Esperança | 7  | 6,1               | 6,6               | Esperança |
| 3  | 0,9               | 4,7               | Gafanhoto | 8  | 0,5               | 1,0               | Gafanhoto |
| 4  | 1,1               | 3,1               | Gafanhoto | 9  | 8,3               | 6,6               | Esperança |
| 5  | 5,4               | 8,5               | Esperança | 10 | 8,1               | 4,7               | Esperança |

Qual a classe de um inseto com comprimento 5,1 de abdômen e 7,0 mm de antenas?

![](content/images/aprendizadosupervisionado-classificacao-knn-_page_15_Figure_1.png)

Qual a classe de um inseto com comprimento 5,1 de abdômen e 7,0 mm de antenas?

#### **Classificador Linear Simples**

Se o exemplo desconhecido está acima da linha Então a classe é **Esperança** Senão a classe é **Gafanhoto**

![](content/images/aprendizadosupervisionado-classificacao-knn-_page_16_Figure_3.png)

#### **Classificador Linear**

Pode ser usado para mais dimensões.

Nesse caso, a divisão não será por uma reta (linha) mas por um hiperplano .

![](content/images/aprendizadosupervisionado-classificacao-knn-_page_17_Picture_4.png)

#### **Classificador Linear**

Limitação: resolve apenas problemas cujas classes são linearmente separáveis.

![](content/images/aprendizadosupervisionado-classificacao-knn-_page_18_Figure_3.png)

![](content/images/aprendizadosupervisionado-classificacao-knn-_page_18_Figure_5.png)

Classificação Perfeita Classificação Muito Boa Classificação Inútil

![](content/images/aprendizadosupervisionado-classificacao-knn-_page_18_Figure_7.png)

#### **Classificador Linear**

Exemplo: **Planta Iris**

• 150 amostras: Dataset Balanceado

- o 50 Iris Setosa,
- o 50 Iris Virginica e
- o 50 Iris Versicolor

![](content/images/aprendizadosupervisionado-classificacao-knn-_page_19_Figure_7.png)

- Podemos generalizar o classificador para N classes, encontrando N-1 hiperplanos:
  - 1. O primeiro hiperplano separa a Setosa das outras duas Versicolor/Virginica
  - 2. O segundo hiperplano separa Versicolor de Virginica

**K- Nearest Neighbour**: algoritmo dos k vizinhos mais próximos.

Considera os objetos mais próximos com características semelhantes para predizer a classe de um novo dado.

![](content/images/aprendizadosupervisionado-classificacao-knn-_page_20_Picture_3.png)

- Algoritmo baseado em memória (Lazy)
  - oEtapa de Treinamento:
    - **Não gera modelo**: apenas memorização dos dados rotulados
  - oEtapa de Generalização:
    - Classifica um novo dado levando em consideração os k vizinhos mais próximos.
    - Usa uma medida de distância para calcular a proximidade dos dados vizinhos (distância euclidiana é bem usual).
    - Cada vizinho k próximo ao dado vota em uma classe.
    - A classe mais votada passa a ser a da novo dado.

![](content/images/aprendizadosupervisionado-classificacao-knn-_page_22_Figure_2.png)

#### Exemplo:

| ID | Atributo1 | Atributo2 | Classe |
|----|-----------|-----------|--------|
| 1  | 5         | 9         | A      |
| 2  | 7         | 9         | A      |
| 3  | 8         | 9         | A      |
| 4  | 9         | 8         | A      |
| 5  | 2         | 5         | B      |
| 6  | 4         | 4         | B      |
| 7  | 1         | 3         | B      |
| 8  | 2         | 3         | B      |
| 9  | 5         | 2         | ?      |

- Aplicar o algoritmo para k=3
- Usar distância de Manhattan (para simplificar o cálculo)

![](content/images/aprendizadosupervisionado-classificacao-knn-_page_23_Figure_5.png)

#### Exemplo:

| ID | Atributo1 | Atributo2 | Classe | Amostra, Dado Novo | Distancia | Valor Distância |
|----|-----------|-----------|--------|--------------------|-----------|-----------------|
| 1  | 5         | 9         | Α      | 1,9                | 5-5 + 9-2 | 7               |
| 2  | 7         | 9         | Α      | 2,9                | 7-5 + 9-2 | 9               |
| 3  | 8         | 9         | Α      | 3,9                | 8-5 + 9-2 | 10              |
| 4  | 9         | 8         | Α      | 4,9                | 9-5 + 8-2 | 10              |
| 5  | 2         | 5         | В      | 5,9                | 2-5 + 5-2 | 6               |
| 6  | 4         | 4         | В      | 6,9                | 4-5 + 4-2 | 3               |
| 7  | 1         | 3         | В      | 7,9                | 1-5 + 3-2 | 5               |
| 8  | 2         | 3         | В      | 8,9                | 2-5 + 3-2 | 4               |
| 9  | 5         | 2         | ?      |                    |           |                 |

- Aplicar o algoritmo para k=3
- Usar distância de Manhattan (para simplificar o cálculo)

#### Exemplo:

|  | B | B é classe predominante dos 3 |  |  |
|--|---|-------------------------------|--|--|

vizinhos mais próximos

- Aplicar o algoritmo para k=3
- Usar distância de Manhattan (para simplificar o cálculo)

#### • **Aspectos Positivos**

- Treinamento é simples (apenas armazenamento dos objetos rotulados);
- Constrói aproximações locais da função objetivo, pois são diferentes para cada objeto novo que foi classificado;
- Aplicável mesmo em problemas complexos;
- Incremental (quando novas amostras de treinamento estão disponíveis, basta memorizá-las).

#### • **Aspectos Negativos**

- Não gera um modelo
- Dependente da medida de distância (importante normalizar os dados)
- Predição pode ser custosa para muito objetos
- Alta dimensionalidade dos atributos afeta negativamente os algoritmos baseados em distância (quanto maior o número de atributos mais a distância do mais próximo aproxima-se do mais distante).

### **Referências**

Este material foi construído com base no material sobre DataMining dos professores Eamonn Keogh(University of California), Rodrigos Barros, Duncan e Renata de Paris e também nos capítulos:

- 4 InteligênciaArticial: Uma abordagem de Aprendizagem de Máquina: Facelli e outros.
- 18 do livro Articial Intelligence a Modern Approach: Russel & Norvig
