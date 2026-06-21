<!-- EXEC_SUMMARY_START -->
## Sumário
> *Leia antes de varrer o arquivo. Vá direto à seção relevante para a pergunta do aluno.*

- **Aula 29 - Aprendizagem de Máquina: Medidas de Avaliação <sup>1</sup>**
  - Sinopse
  - Sumário
  - Medida SSE
  - Medida SSE
  - Medidas geradas pelo Weka
  - Medidas Usuais para Classificação

<!-- EXEC_SUMMARY_END -->
{0}------------------------------------------------

# Inteligência Artificial
## Aula 29 - Aprendizagem de Máquina: Medidas de Avaliação <sup>1</sup>

Sílvia M.W. Moraes

A large, modern, multi-story building with a distinctive architectural design, featuring a prominent vertical section and a series of windows. The building is surrounded by trees and greenery, and a blue sky is visible in the background.

<sup>1</sup>Este material não pode ser reproduzido ou utilizado de forma parcial sem a permissão dos autores.

{1}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-5fb340ad68b0c71df0b56698b137e35b_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A large, modern, multi-story building with a distinctive architectural design, featuring a prominent vertical section and a series of windows.
<!-- /IMAGE_DESCRIPTION -->
### Sinopse

- Nesta aula, apresentamos uma **visão geral de algumas medidas para avaliação de algoritmos de aprendizagem** - tarefas de **classificação e agrupamento**.

{2}------------------------------------------------
### Sumário

- 1 Medidas de Avaliação para Agrupamento
- 2 Medidas de Avaliação para Classificação

{3}------------------------------------------------
### Medida SSE

- Medida mais comum para a tarefa de agrupamento é a **Soma dos Erros Quadráticos (SSE – sum of squared errors)** : mede a coesão dos clusters
  - Para cada objeto, o erro é a distância ao grupo mais próximo (distância do objeto ao centróide do seu cluster).
  - Para obter SSE, elevamos os erros ao quadrado e os somamos.
    - $$SSE = \sum_{i=1}^k \sum_{x \in C_i} distancia^2(m_i, x)$$
    - onde  $k$  é o número de clusters,  $x$  é um objeto do grupo  $C_i$  e  $m_i$  é o centro do grupo  $C_i$  .

{4}------------------------------------------------
### Medida SSE

- Quanto menor o SSE, mais compactos (coesos) são os grupos, pois minimizar o SSE significa minimizar a variância intra-grupo.

A scatter plot on a 10x10 grid illustrating the Sum of Squared Errors (SSE) for two clusters. The x-axis is labeled 1 to 10, and the y-axis is labeled 1 to 10. Two clusters are shown: a small cluster on the left and a larger cluster on the right. Each cluster has a central point (centroid) and several data points (blue dots) connected to it by dashed lines. The left cluster has a red centroid at (2, 4) and four blue data points at (1, 5), (2, 5), (2, 3), and (3, 4). The right cluster has a pink centroid at (8, 7) and eight blue data points at (7, 9), (8, 9), (8, 7), (8, 6), (8, 4), (9, 8), (9, 6), and (10, 5). The SSE is the sum of the squared distances from each data point to its centroid.

| Cluster       | Centroid (x, y) | Data Points (x, y)                                              |
|---------------|-----------------|-----------------------------------------------------------------|
| Left Cluster  | (2, 4)          | (1, 5), (2, 5), (2, 3), (3, 4)                                  |
| Right Cluster | (8, 7)          | (7, 9), (8, 9), (8, 7), (8, 6), (8, 4), (9, 8), (9, 6), (10, 5) |

Scatter plot illustrating the Sum of Squared Errors (SSE) for two clusters.

{5}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-6de7dcb072cef2388026fb0f504084b2_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Scatter plot illustrating the Sum of Squared Errors (SSE) for two clusters.
<!-- /IMAGE_DESCRIPTION -->
### Medidas geradas pelo Weka

- Medidas geradas pelo Weka
  - **Correctly Classified Instances:** total de amostras corretamente classificadas e o seu percentual
  - **Incorrectly Classified Instances:** total de amostras incorretamente classificadas e o seu percentual
  - **Kappa statistic:** calcula o índice de concordância no processo de classificação (entre os avaliadores). Valores próximos a 1 indicam concordância, enquanto valores próximos a 0 indicam ausência de concordância além do puro acaso.

|       | Poor | Slight | Fair | Moderate | Substantial | Almost perfect |
|-------|------|--------|------|----------|-------------|----------------|
| Kappa | 0.0  | .20    | .40  | .60      | .80         | 1.0            |

A horizontal scale for Kappa statistic values. The scale is represented by a horizontal line with an arrow pointing to the right. Above the line, there are six labels: 'Poor', 'Slight', 'Fair', 'Moderate', 'Substantial', and 'Almost perfect'. Below the line, there are six numerical values: '0.0', '.20', '.40', '.60', '.80', and '1.0'. The word 'Kappa' is written to the left of the '0.0' value.

A horizontal scale for Kappa statistic values from 0.0 to 1.0, with qualitative labels above the numbers.

{6}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-46f43cb4ffd47565e7c0ca306d461435_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A horizontal scale for Kappa statistic values from 0.0 to 1.0, with qualitative labels above the numbers.
<!-- /IMAGE_DESCRIPTION -->
#### Medidas geradas pelo Weka

- Medidas geradas pelo Weka
  - **Mean absolute error** (erro absoluto médio): média do valor absoluto dos erros. Erro absoluto corresponde à diferença em módulo entre o valor esperado e sua aproximação.
  - **Root mean squared error** (raiz do erro quadrático médio): raiz da média dos quadrados dos erros. Erro quadrático corresponde ao quadrado da diferença entre o valor esperado e sua aproximação.
  - **Relative absolute error** (erro absoluto relativo) : corresponde à razão entre o erro absoluto e a magnitude do valor esperado.
  - **Root relative squared error** (erro quadrático relativo): corresponde à razão entre o erro quadrático e a magnitude do valor esperado.

{7}------------------------------------------------
### Medidas Usuais para Classificação

- As medidas mais usuais em tarefas de Classificação são
  - Accuracy (Acurácia),
  - Precision (Precisão)
  - Recall (Abrangência)
  - F-Measure (F1)
- São medidas clássicas definidas para a área de Recuperação de Informações.

{8}------------------------------------------------
#### Classificação: Matriz de Confusão

- As medidas usadas para avaliar os resultados da classificação são calculadas a partir de uma **tabela de confusão** (ou de contingência).
- Nessa tabela são confrontados os resultados do preditor com os resultados esperados.
- É sempre uma matriz quadrada:  $nroClasses \times nroClasses$ , onde as linhas representam os resultados esperados e as colunas, os resultados gerados pelo preditor.

{9}------------------------------------------------
#### Classificação: Matriz de Confusão

- As medidas foram originalmente definidas para classificadores binários, ou seja, capazes de classificar dados em apenas 2 classes. Para duas classes *Sim* e *Não*, a matriz seria assim:

|                      |     | Preditor (Máquina) |    |
|----------------------|-----|--------------------|----|
|                      |     | Classes            |    |
| Resultados Esperados | Sim | TP                 | FN |
|                      | Não | FP                 | TN |

- TP: Verdadeiro-Positivo** (classificação correta): era da classe esperada e o preditor o classificou nessa classe.
- TN: Verdadeiro-Negativo** (classificação correta): não era da classe e preditor não o classificou nessa classe.
- FP: Falso-positivo** (classificação incorreta): não era da classe esperada e o preditor classificou a amostra nessa classe.
- FN: Falso-negativo** (classificação incorreta): era da classe e o preditor classificou a amostra em outra classe.

{10}------------------------------------------------
#### Classificação: Matriz de Confusão

- **Exemplo:** 120 amostras das classes **Iris-Setosa(a)**, **Iris-Versicolor(b)** e **Iris-Virginica(c)** foram testadas, 40 de cada classe.

=== Confusion Matrix ===

```

a  b  c  <-- classified as
40  0  0 |  a = Iris-setosa
 0 37  3 |  b = Iris-versicolor
 0  2 38 |  c = Iris-virginica

```

- A tabela corresponde a uma matriz quadrada  $3 \times 3$ , onde as linhas correspondem às classes esperadas (conhecidas, que estão no arquivo de teste) e as colunas às classes previstas.
- A diagonal principal corresponde aos acertos do classificador.
- **Para classe Iris-Versicolor:**
  - TP (Verdadeiro-Positivo): 37
  - TN (Verdadeiro-Negativo): 78
  - FP (Falso-Positivo): 2
  - FN (Falso-Negativo): 3

{11}------------------------------------------------
#### Classificação: Matriz de Confusão

- **Exemplo:** 120 amostras das classes **Iris-Setosa(a)**, **Iris-Versicolor(b)** e **Iris-Virginica(c)** foram testadas, 40 de cada classe.

=== Confusion Matrix ===

```
  a  b  c  <-- classified as
40  0  0 |  a = Iris-setosa
 0 37  3 |  b = Iris-versicolor
 0  2 38 |  c = Iris-virginica
```

- **Atividade I:** Calcule os índices TP, TN, FP e FN para as classe Iris-Virginica e Iris-Setosa

{12}------------------------------------------------
#### Classificação: Matriz de Confusão

- **Exemplo:** 120 amostras das classes **Iris-Setosa(a)**, **Iris-Versicolor(b)** e **Iris-Virginica(c)** foram testadas, 40 de cada classe.

=== Confusion Matrix ===

```
  a  b  c  <-- classified as
40  0  0 |  a = Iris-setosa
 0 37  3 |  b = Iris-versicolor
 0  2 38 |  c = Iris-virginica
```

- **Atividade I:** Calcule os índices TP, TN, FP e FN para as classe Iris-Virginica e Iris-Setosa
- **Resposta:** Para classe **Iris-Virginica**:
  - TP (Verdadeiro-Positivo): 38
  - TN (Verdadeiro-Negativo): 77
  - FP (Falso-Positivo): 3
  - FN (Falso-Negativo): 2

{13}------------------------------------------------
#### Classificação: Matriz de Confusão

- **Exemplo:** 120 amostras das classes **Iris-Setosa(a)**, **Iris-Versicolor(b)** e **Iris-Virginica(c)** foram testadas, 40 de cada classe.

=== Confusion Matrix ===

```
  a  b  c  <-- classified as
40  0  0 |  a = Iris-setosa
 0 37  3 |  b = Iris-versicolor
 0  2 38 |  c = Iris-virginica
```

- **Atividade I:** Calcule os índices TP, TN, FP e FN para as classe Iris-Virginica e Iris-Setosa
- **Resposta:** Para classe **Iris-Setosa**:
  - TP (Verdadeiro-Positivo): 40
  - TN (Verdadeiro-Negativo): 75
  - FP (Falso-Positivo): 0
  - FN (Falso-Negativo): 0

{14}------------------------------------------------
#### Classificação: Accuracy

- Acurácia e precisão, embora, muitas vezes, sejam usadas como sinônimos, estatisticamente não são a mesma medida.
- **Accuracy**: corresponde à proporção de acertos do classificador.

|                      |     | Preditor (Máquina) |           |
|----------------------|-----|--------------------|-----------|
|                      |     | Classes            |           |
| Resultados Esperados | Sim | TP                 | <u>FN</u> |
|                      | Não | FP                 | TN        |

- TP: Verdadeiro-Positivo (classificação correta)
- TN: Verdadeiro-Negativo (classificação correta)
- FP: Falso-positivo (classificação incorreta)
- FN: Falso-negativo (classificação incorreta)
- $Accuracy = \frac{TP+TN}{TP+TN+FP+FN}$

{15}------------------------------------------------
#### Classificação: Accuracy
##### - Micro-médias (por classe)

- $Accuracy_{classe} = \frac{TP+TN}{TP+TN+FP+FN}$
##### - Macro-médias (índices gerais)

- *Accuracy Média*: média aritmética de todas as micro-médias de *accuracy*.

{16}------------------------------------------------
#### Classificação: Accuracy

- **Exemplo:** 120 amostras das classes **Iris-Setosa(a)**, **Iris-Versicolor(b)** e **Iris-Virginica(c)** foram testadas, 40 de cada classe.

- Para classe **Iris-Versicolor**:

- TP (Verdadeiro-Positivo): 37
- TN (Verdadeiro-Negativo): 78
- FP (Falso-Positivo): 2
- FN (Falso-Negativo): 3

- $Accuracy_{versicolor} = \frac{TP+TN}{TP+TN+FP+FN} = \frac{37+78}{37+78+2+3} = 0,958$

{17}------------------------------------------------
#### Classificação: Accuracy

- **Exemplo:** 120 amostras das classes **Iris-Setosa(a)**, **Iris-Versicolor(b)** e **Iris-Virginica(c)** foram testadas, 40 de cada classe.

```
=== Confusion Matrix ===
```

```
  a  b  c  <-- classified as
40  0  0 |  a = Iris-setosa
 0 37  3 |  b = Iris-versicolor
 0  2 38 |  c = Iris-virginica
```

- **Atividade II:** Calcule a accuracy (micro-média) para as classes iris-setosa e iris-virginica. Em seguida, calcula a macro-média de accuracy.

{18}------------------------------------------------
#### Classificação: Accuracy

- **Exemplo:** 120 amostras das classes **Iris-Setosa(a)**, **Iris-Versicolor(b)** e **Iris-Virginica(c)** foram testadas, 40 de cada classe.
- **Atividade II:** Calcule a accuracy (micro-média) para as classes iris-setosa e iris-virginica. Em seguida, calcula a macro-média de accuracy.
  - **Resposta:** Para classe Iris-Virginica:
    - TP (Verdadeiro-Positivo): 38
    - TN (Verdadeiro-Negativo): 77
    - FP (Falso-Positivo): 3
    - FN (Falso-Negativo): 2
  - $Accuracy_{virginica} = \frac{TP+TN}{TP+TN+FP+FN} = \frac{38+77}{38+77+3+2} = 0,958$

{19}------------------------------------------------
#### Classificação: Accuracy

- **Exemplo:** 120 amostras das classes **Iris-Setosa(a)**, **Iris-Versicolor(b)** e **Iris-Virginica(c)** foram testadas, 40 de cada classe.
- **Atividade II:** Calcule a accuracy (micro-média) para as classes iris-setosa e iris-virginica. Em seguida, calcula a macro-média de accuracy.
  - **Resposta:** Para classe Iris-Setosa:
    - TP (Verdadeiro-Positivo): 40
    - TN (Verdadeiro-Negativo): 75
    - FP (Falso-Positivo): 0
    - FN (Falso-Negativo): 0
  - $Accuracy_{setosa} = \frac{TP+TN}{TP+TN+FP+FN} = \frac{40+75}{40+75} = 1$

{20}------------------------------------------------
#### Classificação: Accuracy

- **Exemplo:** 120 amostras das classes **Iris-Setosa(a)**, **Iris-Versicolor(b)** e **Iris-Virginica(c)** foram testadas, 40 de cada classe.
- **Atividade II:** Calcule a accuracy (micro-média) para as classes iris-setosa e iris-virginica. Em seguida, calcula a macro-média de accuracy.
  - **Resposta: Macro-Média:**  $Accuracy = \frac{1+0,958+0,958}{3} = 0,972$
  - $Accuracy_{setosa} = 1$
  - $Accuracy_{versicolor} = 0,958$
  - $Accuracy_{virginica} = 0,958$

{21}------------------------------------------------
#### Classificação: Precision e Recall

- Para entender a diferença entre Precision e Recall, considere as imagens abaixo.

The diagram consists of two Venn diagrams. The left diagram shows two overlapping circles: a yellow circle on the left and a blue circle on the right. The intersection is shaded with diagonal lines. Labels with leader lines point to the yellow circle ('The set of relevant items in the database') and the blue circle ('The set of items retrieved'). The right diagram is similar, but the non-overlapping part of the blue circle is labeled 'Irrelevant items - retrieved'. The intersection is labeled 'Relevant items - retrieved', and the non-overlapping part of the yellow circle is labeled 'Relevant items - not retrieved'.

Two Venn diagrams illustrating retrieval results. The left diagram shows the intersection of relevant items and retrieved items. The right diagram shows the intersection of relevant items and retrieved items, with the non-overlapping part of the retrieved set labeled as irrelevant items.

{22}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-e180f2b5fcbe8001554a7c0677cd3f82_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Two Venn diagrams illustrating retrieval results.
<!-- /IMAGE_DESCRIPTION -->
##### Classificação: Precision

- **Precision:** é a razão entre número de dados corretamente classificados e o número total dados classificados (corretamente e incorretamente).

Diagram illustrating Precision in classification:

The diagram shows two overlapping circles representing the sets of relevant and irrelevant items retrieved.

Left Diagram Labels:

- Yellow circle: Relevant items - not retrieved
- Intersection: Relevant items - retrieved
- Blue circle: Irrelevant items - retrieved

Right Diagram Labels:

- Yellow circle (A): A: No. of relevant records retrieved
- Blue circle (C): C: No. of irrelevant records retrieved

PRECISION:  $\frac{A}{A+C} \times 100\%$

Diagram illustrating Precision in classification. It shows two Venn diagrams. The left diagram shows a yellow circle (relevant items) and a blue circle (irrelevant items) with their intersection shaded. Labels point to the yellow-only area (Relevant items - not retrieved), the intersection (Relevant items - retrieved), and the blue-only area (Irrelevant items - retrieved). The right diagram shows a yellow circle (A) and a blue circle (C) with their intersection shaded. Labels point to the yellow-only area (A: No. of relevant records retrieved) and the blue-only area (C: No. of irrelevant records retrieved). Below the right diagram is the formula: PRECISION: A / (A + C) x 100%.

{23}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-eb03559a4d92ea9ebd63ea9be663c50a_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram illustrating Precision in classification.
<!-- /IMAGE_DESCRIPTION -->
##### Classificação: Precision

- **Precision:** proporção de textos corretamente classificados.

C: No. of irrelevant records retrieved.

A: No. of relevant records retrieved.

PRECISION:  $\frac{A}{A+C} \times 100\%$

Venn diagram illustrating Precision. A circle is divided into two regions: A (relevant records retrieved, shaded yellow) and C (irrelevant records retrieved, shaded blue). The formula for Precision is given as A / (A + C) \* 100%.

|                      |     | Preditor (Máquina) |     |
|----------------------|-----|--------------------|-----|
| Classes              |     | Sim                | Não |
| Resultados Esperados | Sim | TP                 | FN  |
|                      | Não | FP                 | TN  |

$$Precision = \frac{TP}{TP+FP}$$

{24}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-ae53f90bb87d6d09e2d6b5278d7c338f_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Venn diagram illustrating Precision. A circle is divided into two regions: A (relevant records retrieved, shaded yellow) and C (irrelevant records retrieved, shaded blue). The formula for Precision is given as A / (A +...
<!-- /IMAGE_DESCRIPTION -->
##### Classificação: Precision

- **Exemplo:** 120 amostras das classes **Iris-Setosa(a)**, **Iris-Versicolor(b)** e **Iris-Virginica(c)** foram testadas, 40 de cada classe.
  - Para classe **Iris-Versicolor**:
    - TP (Verdadeiro-Positivo): 37
    - TN (Verdadeiro-Negativo): 78
    - FP (Falso-Positivo): 2
    - FN (Falso-Negativo): 3

$$Precision_{versicolor} = \frac{TP}{TP+FP} = \frac{37}{37+2} = 0,9487$$

{25}------------------------------------------------
##### Classificação: Precision

- **Exemplo:** 120 amostras das classes **Iris-Setosa(a)**, **Iris-Versicolor(b)** e **Iris-Virginica(c)** foram testadas, 40 de cada classe.
  - **Atividade III:** Calcule a precision (micro-média) para as classes iris-setosa e iris-virginica. Em seguida, calcula a macro-média de precision.

$$Precision = \frac{TP}{TP+FP}$$

{26}------------------------------------------------
##### Classificação: Precision

- **Exemplo:** 120 amostras das classes **Iris-Setosa(a)**, **Iris-Versicolor(b)** e **Iris-Virginica(c)** foram testadas, 40 de cada classe.
  - **Atividade III:** Calcule a precision (micro-média) para as classes iris-setosa e iris-virginica. Em seguida, calcula a macro-média de precision.
  - **Resposta:** Para classe **Iris-Setosa**:
    - TP (Verdadeiro-Positivo): 40
    - TN (Verdadeiro-Negativo): 75
    - FP (Falso-Positivo): 0
    - FN (Falso-Negativo): 0

$$Precision_{setosa} = \frac{TP}{TP+FP} = \frac{40}{40+0} = 1$$

{27}------------------------------------------------
##### Classificação: Precision

- **Exemplo:** 120 amostras das classes **Iris-Setosa(a)**, **Iris-Versicolor(b)** e **Iris-Virginica(c)** foram testadas, 40 de cada classe.
  - **Atividade III:** Calcule a precision (micro-média) para as classes iris-setosa e iris-virginica. Em seguida, calcula a macro-média de precision.
  - **Resposta:** Para classe **Iris-Virginica**:
    - TP (Verdadeiro-Positivo): 38
    - TN (Verdadeiro-Negativo): 77
    - FP (Falso-Positivo): 3
    - FN (Falso-Negativo): 2

$$Precision_{virginica} = \frac{TP}{TP+FP} = \frac{38}{38+3} = 0,9268$$

{28}------------------------------------------------
##### Classificação: Precision

- **Exemplo:** 120 amostras das classes **Iris-Setosa(a)**, **Iris-Versicolor(b)** e **Iris-Virginica(c)** foram testadas, 40 de cada classe.
  - **Atividade III:** Calcule a precision (micro-média) para as classes iris-setosa e iris-virginica. Em seguida, calcula a macro-média de precision.
  - **Resposta: Macro-Média:**  $Precision = \frac{1+0,9268+0,9487}{3} = 0,9585$ 
    - $Precision_{setosa} = \frac{TP}{TP+FP} = \frac{40}{40+0} = 1$
    - $Precision_{virginica} = \frac{TP}{TP+FP} = \frac{38}{38+3} = 0,9268$
    - $Precision_{versicolor} = \frac{TP}{TP+FP} = \frac{37}{37+2} = 0,9487$

{29}------------------------------------------------
##### Classificação: Recall

- **Recall:** corresponde à razão entre de dados classificados corretamente (relevantes) sobre o número total de classificações definidas como corretas.

Diagram illustrating Recall in classification:

The diagram shows two overlapping circles. The left circle is yellow and labeled "Relevant items - not retrieved". The right circle is blue with diagonal lines and labeled "Irrelevant items - retrieved". The intersection of the two circles is yellow with diagonal lines and labeled "Relevant items - retrieved".

Below the diagram, the formula for Recall is given:

$$\text{RECALL: } \frac{A}{A+B} \times 100\%$$

Where:

- B: Number of relevant records not retrieved.
- A: Number of relevant records retrieved.

Diagram illustrating Recall in classification. It consists of two parts. The left part shows a Venn diagram with two overlapping circles. The left circle is yellow and labeled 'Relevant items - not retrieved'. The right circle is blue with diagonal lines and labeled 'Irrelevant items - retrieved'. The intersection of the two circles is yellow with diagonal lines and labeled 'Relevant items - retrieved'. The right part shows a Venn diagram with two overlapping circles. The left circle is yellow and labeled 'B: Number of relevant records not retrieved.' The right circle is blue with diagonal lines and labeled 'A: Number of relevant records retrieved.' Below this diagram is the formula: RECALL: \frac{A}{A+B} \times 100\%.

{30}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-dd5771673aececa53d42ece89218299d_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram illustrating Recall in classification.
<!-- /IMAGE_DESCRIPTION -->
##### Classificação: Recall

- **Recall**: proporção de textos que deveriam ter sido corretamente classificados.

B: Number of relevant records not retrieved.

A: Number of relevant records retrieved.

RECALL:  $\frac{A}{A+B} \times 100\%$

Venn diagram illustrating Recall. Two overlapping circles, A and B, are shown. Circle A is shaded yellow and represents 'Number of relevant records retrieved'. Circle B is shaded with diagonal lines and represents 'Number of relevant records not retrieved'. The formula for Recall is given as: RECALL: \frac{A}{A+B} \times 100\%.

|                      |     | Preditor (Máquina) |     |
|----------------------|-----|--------------------|-----|
| Classes              |     | Sim                | Não |
| Resultados Esperados | Sim | TP                 | FN  |
|                      | Não | FP                 | TN  |

$$Recall = \frac{TP}{TP+FN}$$

{31}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-00504fc688ebcf131ccbeff94dfc9939_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Venn diagram illustrating Recall. Two overlapping circles, A and B, are shown. Circle A is shaded yellow and represents 'Number of relevant records retrieved'. Circle B is shaded with diagonal lines and represents...
<!-- /IMAGE_DESCRIPTION -->
##### Classificação: Recall

- **Exemplo:** 120 amostras das classes **Iris-Setosa(a)**, **Iris-Versicolor(b)** e **Iris-Virginica(c)** foram testadas, 40 de cada classe.
  - Para classe **Iris-Versicolor**:
    - TP (Verdadeiro-Positivo): 37
    - TN (Verdadeiro-Negativo): 78
    - FP (Falso-Positivo): 2
    - FN (Falso-Negativo): 3

$$Recall_{Versicolor} = \frac{TP}{TP+FN} = \frac{37}{37+3} = 0,925$$

{32}------------------------------------------------
##### Classificação: Recall

- **Exemplo:** 120 amostras das classes **Iris-Setosa(a)**, **Iris-Versicolor(b)** e **Iris-Virginica(c)** foram testadas, 40 de cada classe.
  - **Atividade IV:** Calcule o recall (micro-média) para as classes iris-setosa e iris-virginica. Em seguida, calcula a macro-média de recall.

$$Recall = \frac{TP}{TP+FN}$$

{33}------------------------------------------------
##### Classificação: Recall

- **Exemplo:** 120 amostras das classes **Iris-Setosa(a)**, **Iris-Versicolor(b)** e **Iris-Virginica(c)** foram testadas, 40 de cada classe.
  - **Atividade IV:** Calcule o recall (micro-média) para as classes iris-setosa e iris-virginica. Em seguida, calcula a macro-média de recall.
  - **Resposta:** Para classe **Iris-Virginica**:
    - TP (Verdadeiro-Positivo): 38
    - TN (Verdadeiro-Negativo): 77
    - FP (Falso-Positivo): 3
    - FN (Falso-Negativo): 2

$$Recall_{virginica} = \frac{TP}{TP+FN} = \frac{38}{38+2} = 0,95$$

{34}------------------------------------------------
##### Classificação: Recall

- **Exemplo:** 120 amostras das classes **Iris-Setosa(a)**, **Iris-Versicolor(b)** e **Iris-Virginica(c)** foram testadas, 40 de cada classe.
  - **Atividade IV:** Calcule o recall (micro-média) para as classes iris-setosa e iris-virginica. Em seguida, calcula a macro-média de recall.
  - **Resposta:** Para classe Iris-Setosa:
    - TP (Verdadeiro-Positivo): 40
    - TN (Verdadeiro-Negativo): 75
    - FP (Falso-Positivo): 0
    - FN (Falso-Negativo): 0

$$Recall_{setosa} = \frac{TP}{TP+FN} = \frac{40}{40+0} = 1$$

{35}------------------------------------------------
##### Classificação: Recall

- **Exemplo:** 120 amostras das classes **Iris-Setosa(a)**, **Iris-Versicolor(b)** e **Iris-Virginica(c)** foram testadas, 40 de cada classe.
  - **Atividade IV:** Calcule o recall (micro-média) para as classes iris-setosa e iris-virginica. Em seguida, calcula a macro-média de recall.
  - **Resposta: Macro-Média:**  $Recall = \frac{1+0,95+0,925}{3} = 0,9583$ 
    - $Recall_{setosa} = \frac{TP}{TP+FN} = \frac{40}{40+0} = 1$
    - $Recall_{virginica} = \frac{TP}{TP+FN} = \frac{38}{38+2} = 0,95$
    - $Recall_{Versicolor} = \frac{TP}{TP+FN} = \frac{37}{37+3} = 0,925$

{36}------------------------------------------------
##### Classificação: F-Measure

- Média Harmônica das medidas Precision e Recall

$$F1 = \frac{2 \times \text{Precision} \times \text{Recall}}{\text{Precision} + \text{Recall}}$$

- **Exemplo:** 120 amostras das classes **Iris-Setosa(a)**, **Iris-Versicolor(b)** e **Iris-Virginica(c)** foram testadas, 40 de cada classe.

- $F - \text{Measure}_{\text{versicolor}} = \frac{2 \times 0,9487 \times 0,925}{0,9487 + 0,925} = 0,9367$

- $F - \text{Measure}_{\text{setosa}} = \frac{2 \times 1 \times 1}{1 + 1} = 1$

- $F - \text{Measure}_{\text{virginica}} = \frac{2 \times 0,9268 \times 0,95}{0,9268 + 0,95} = 0,9382$

- Macro-Média:  $F - \text{Measure} = \frac{0,9367 + 1 + 0,9382}{3} = 0,9583$
