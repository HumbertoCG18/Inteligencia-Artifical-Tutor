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

A photograph of a large, modern, light-colored building with many windows, likely a university or research facility, set against a clear blue sky. The building is surrounded by green trees and a paved area in the foreground.

<sup>1</sup>Este material não pode ser reproduzido ou utilizado de forma parcial sem a permissão dos autores.

{1}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-5fb340ad68b0c71df0b56698b137e35b_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A photograph of a large, modern, light-colored building with many windows, likely a university or research facility, set against a clear blue sky.
<!-- /IMAGE_DESCRIPTION -->
### Sinopse

- Nesta aula, apresentamos uma **visão geral de algumas medidas para avaliação de algoritmos de aprendizagem - tarefas de classificação e agrupamento.**

{2}------------------------------------------------
### Sumário

1 Medidas de Avaliação para Agrupamento

2 Medidas de Avaliação para Classificação

{3}------------------------------------------------
### Medida SSE

- Medida mais comum para a tarefa de agrupamento é a **Soma dos Erros Quadráticos** (SSE – sum of squared errors) : mede a coesão dos clusters
  - Para cada objeto, o erro é a distância ao grupo mais próximo (distância do objeto ao centróide do seu cluster).
  - Para obter SSE, elevamos os erros ao quadrado e os somamos.

$$\bullet SSE = \sum_{i=1}^k \sum_{x \in C_i} distancia^2(m_i, x)$$

- onde  $k$  é o número de clusters,  $x$  é um objeto do grupo  $C_i$  e  $m_i$  é o centro do grupo  $C_i$  .

{4}------------------------------------------------
### Medida SSE

- Quanto menor o SSE, mais compactos (coesos) são os grupos, pois minimizar o SSE significa minimizar a variância intra-grupo.

The figure shows a 2D scatter plot with x and y axes ranging from 1 to 10. There are two clusters of data points. The first cluster, located on the left (approximately x=2, y=4), has a red centroid and four blue data points. The second cluster, located on the right (approximately x=8, y=7), has a pink centroid and eight blue data points. Dashed lines connect each blue data point to its respective centroid, illustrating the intra-cluster variance (SSE).

A scatter plot illustrating two clusters of data points. The left cluster has a red centroid and four blue points. The right cluster has a pink centroid and eight blue points. Dashed lines connect each point to its centroid, representing the squared error sum (SSE).

{5}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-6de7dcb072cef2388026fb0f504084b2_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A scatter plot illustrating two clusters of data points.
<!-- /IMAGE_DESCRIPTION -->
### Medidas geradas pelo Weka

- Medidas geradas pelo Weka
  - **Correctly Classified Instances:** total de amostras corretamente classificadas e o seu percentual
  - **Incorrectly Classified Instances:** total de amostras incorretamente classificadas e o seu percentual
  - **Kappa statistic:** calcula o índice de concordância no processo de classificação (entre os avaliadores). Valores próximos a 1 indicam concordância, enquanto valores próximos a 0 indicam ausência de concordância além do puro acaso.

|       | Poor | Slight | Fair | Moderate | Substantial | Almost perfect |
|-------|------|--------|------|----------|-------------|----------------|
| Kappa | 0.0  | .20    | .40  | .60      | .80         | 1.0            |

{6}------------------------------------------------
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

|                      |     | Preditor (Máquina) |     |
|----------------------|-----|--------------------|-----|
|                      |     | Classes            | Sim |
| Resultados Esperados | Sim | TP                 | FN  |
|                      | Não | FP                 | TN  |

- TP: Verdadeiro-Positivo** (classificação correta): era da classe esperada e o preditor o classificou nessa classe.
- TN: Verdadeiro-Negativo** (classificação correta): não era da classe e preditor não o classificou nessa classe.
- FP: Falso-positivo** (classificação incorreta): não era da classe esperada e o preditor classificou a amostra nessa classe.
- FN: Falso-negativo** (classificação incorreta): era da classe e o preditor classificou a amostra em outra classe.

{10}------------------------------------------------
#### Classificação: Matriz de Confusão

- **Exemplo:** 120 amostras das classes **Iris-Setosa(a)**, **Iris-Versicolor(b)** e **Iris-Virginica(c)** foram testadas, 40 de cada classe.

=== Confusion Matrix ===

|  | a  | b  | c  | <-- classified as   |
|--|----|----|----|---------------------|
|  | 40 | 0  | 0  | a = Iris-setosa     |
|  | 0  | 37 | 3  | b = Iris-versicolor |
|  | 0  | 2  | 38 | c = Iris-virginica  |

- A tabela corresponde a uma matriz quadrada  $3 \times 3$ , onde as linhas correspondem às classes esperadas (conhecidas, que estão no arquivo de teste) e as colunas às classes preditas.
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

|  | a  | b  | c  | <-- classified as   |
|--|----|----|----|---------------------|
|  | 40 | 0  | 0  | a = Iris-setosa     |
|  | 0  | 37 | 3  | b = Iris-versicolor |
|  | 0  | 2  | 38 | c = Iris-virginica  |

- **Atividade I:** Calcule os índices TP, TN, FP e FN para as classes Iris-Virginica e Iris-Setosa

{12}------------------------------------------------
#### Classificação: Matriz de Confusão

- **Exemplo:** 120 amostras das classes **Iris-Setosa(a)**, **Iris-Versicolor(b)** e **Iris-Virginica(c)** foram testadas, 40 de cada classe.

=== Confusion Matrix ===

|  | a  | b  | c  | <-- classified as   |
|--|----|----|----|---------------------|
|  | 40 | 0  | 0  | a = Iris-setosa     |
|  | 0  | 37 | 3  | b = Iris-versicolor |
|  | 0  | 2  | 38 | c = Iris-virginica  |

- **Atividade I:** Calcule os índices TP, TN, FP e FN para as classes Iris-Virginica e Iris-Setosa
- **Resposta:** Para classe Iris-Virginica:
  - TP (Verdadeiro-Positivo): 38
  - TN (Verdadeiro-Negativo): 77
  - FP (Falso-Positivo): 3
  - FN (Falso-Negativo): 2

{13}------------------------------------------------
#### Classificação: Matriz de Confusão

- **Exemplo:** 120 amostras das classes **Iris-Setosa(a)**, **Iris-Versicolor(b)** e **Iris-Virginica(c)** foram testadas, 40 de cada classe.

=== Confusion Matrix ===

|  | a  | b  | c  | <-- classified as   |
|--|----|----|----|---------------------|
|  | 40 | 0  | 0  | a = Iris-setosa     |
|  | 0  | 37 | 3  | b = Iris-versicolor |
|  | 0  | 2  | 38 | c = Iris-virginica  |

- **Atividade I:** Calcule os índices TP, TN, FP e FN para as classes Iris-Virginica e Iris-Setosa
- **Resposta:** Para classe Iris-Setosa:
  - TP (Verdadeiro-Positivo): 40
  - TN (Verdadeiro-Negativo): 75
  - FP (Falso-Positivo): 0
  - FN (Falso-Negativo): 0

{14}------------------------------------------------
#### Classificação: Accuracy

- Acurácia e precisão, embora, muitas vezes, sejam usadas como sinônimos, estatisticamente não são a mesma medida.
- **Accuracy**: corresponde à proporção de acertos do classificador.

|                      |     | Preditor (Máquina) |     |
|----------------------|-----|--------------------|-----|
|                      |     | Classes            | Sim |
| Resultados Esperados | Sim | TP                 | FN  |
|                      | Não | FP                 | TN  |

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
  - **Para classe Iris-Versicolor:**
    - TP (Verdadeiro-Positivo): 37
    - TN (Verdadeiro-Negativo): 78
    - FP (Falso-Positivo): 2
    - FN (Falso-Negativo): 3
  - $Accuracy_{versicolor} = \frac{TP+TN}{TP+TN+FP+FN} = \frac{37+78}{37+78+2+3} = 0,958$

{17}------------------------------------------------
#### Classificação: Accuracy

- **Exemplo:** 120 amostras das classes **Iris-Setosa(a)**, **Iris-Versicolor(b)** e **Iris-Virginica(c)** foram testadas, 40 de cada classe.

=== Confusion Matrix ===

|  | a  | b  | c  | <-- classified as   |
|--|----|----|----|---------------------|
|  | 40 | 0  | 0  | a = Iris-setosa     |
|  | 0  | 37 | 3  | b = Iris-versicolor |
|  | 0  | 2  | 38 | c = Iris-virginica  |

- **Atividade II:** Calcule a accuracy (micro-média) para as classes iris-setosa e iris-virginica. Em seguida, calcula a macro-média de accuracy.

{18}------------------------------------------------
#### Classificação: Accuracy

- **Exemplo:** 120 amostras das classes **Iris-Setosa(a)**, **Iris-Versicolor(b)** e **Iris-Virginica(c)** foram testadas, 40 de cada classe.
- **Atividade II:** Calcule a accuracy (micro-média) para as classes iris-setosa e iris-virginica. Em seguida, calcula a macro-média de accuracy.
  - **Resposta:** Para classe **Iris-Virginica:**
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

The diagram consists of two side-by-side Venn diagrams. The left diagram shows two overlapping circles. The left circle is solid yellow and labeled "The set of relevant items in the database". The right circle is blue with diagonal hatching and labeled "The set of items retrieved". The intersection of the two circles is also hatched. The right diagram shows the same two circles. The left circle (relevant items) is divided into two parts: a smaller solid yellow part on the left labeled "Relevant items - retrieved" and a larger hatched part on the right labeled "Relevant items - not retrieved". The right circle (retrieved items) is also divided into two parts: the same hatched intersection part and a larger part on the right labeled "Irrelevant items - retrieved".

Two Venn diagrams illustrating Precision and Recall in classification.

{22}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-e180f2b5fcbe8001554a7c0677cd3f82_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Two Venn diagrams illustrating Precision and Recall in classification.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-eb03559a4d92ea9ebd63ea9be663c50a_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram illustrating Precision with two Venn diagrams.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-dd5771673aececa53d42ece89218299d_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Two Venn diagrams illustrating Recall. The left diagram shows a yellow circle (relevant items) and a blue circle (retrieved items). The intersection is labeled 'Relevant items - retrieved'. The part of the yellow...
<!-- /IMAGE_DESCRIPTION -->
##### Classificação: Precision

- Precision:** é a razão entre número de dados corretamente classificados e o número total dados classificados (corretamente e incorretamente).

Diagram illustrating Precision:

The left diagram shows a Venn diagram with two overlapping circles. The left circle is yellow and labeled "Relevant items - not retrieved". The right circle is blue and labeled "Irrelevant items - retrieved". The intersection is yellow hatched and labeled "Relevant items - retrieved".

The right diagram shows a Venn diagram with two overlapping circles. The left circle is yellow and labeled "A" (No. of relevant records retrieved). The right circle is blue and labeled "C" (No. of irrelevant records retrieved). The intersection is yellow hatched.

PRECISION:  $\frac{A}{A+C} \times 100\%$

Diagram illustrating Precision with two Venn diagrams. The left diagram shows a yellow circle (Relevant items - not retrieved) and a blue circle (Irrelevant items - retrieved) overlapping in a yellow hatched area (Relevant items - retrieved). The right diagram shows a yellow circle labeled 'A' (No. of relevant records retrieved) and a blue circle labeled 'C' (No. of irrelevant records retrieved) overlapping. The formula for Precision is given as A / (A+C) \* 100%.

{23}------------------------------------------------
##### Classificação: Precision

- Precision:** proporção de textos corretamente classificados.

C: No. of irrelevant records retrieved.  
A: No. of relevant records retrieved.

PRECISION:  $\frac{A}{A+C} \times 100\%$

Venn diagram illustrating Precision. A yellow circle labeled 'A' represents relevant records retrieved. A blue circle labeled 'C' represents irrelevant records retrieved. The intersection of the two circles is shaded with diagonal lines. The formula for Precision is given as: PRECISION: \frac{A}{A+C} \times 100%.

|                      |     | Preditor (Máquina) |     |
|----------------------|-----|--------------------|-----|
|                      |     | Classes            | Sim |
| Resultados Esperados | Sim | TP                 | FN  |
|                      | Não | FP                 | TN  |

$$Precision = \frac{TP}{TP+FP}$$

{24}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-ae53f90bb87d6d09e2d6b5278d7c338f_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Venn diagram illustrating Precision. A yellow circle labeled 'A' represents relevant records retrieved. A blue circle labeled 'C' represents irrelevant records retrieved. The intersection of the two circles is shaded...
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
  - **Resposta:** Para classe **Iris-Setosa:**
    - TP (Verdadeiro-Positivo): 40
    - TN (Verdadeiro-Negativo): 75
    - FP (Falso-Positivo): 0
    - FN (Falso-Negativo): 0

$$Precision_{setosa} = \frac{TP}{TP+FP} = \frac{40}{40+0} = 1$$

{27}------------------------------------------------
##### Classificação: Precision

- **Exemplo:** 120 amostras das classes **Iris-Setosa(a)**, **Iris-Versicolor(b)** e **Iris-Virginica(c)** foram testadas, 40 de cada classe.
  - **Atividade III:** Calcule a precision (micro-média) para as classes iris-setosa e iris-virginica. Em seguida, calcula a macro-média de precision.
  - **Resposta:** Para classe **Iris-Virginica:**
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

Diagram illustrating Recall using Venn diagrams.

The left diagram shows two overlapping circles. The yellow circle represents relevant items, and the blue circle represents retrieved items. The intersection is labeled "Relevant items - retrieved". The part of the yellow circle not in the intersection is labeled "Relevant items - not retrieved". The part of the blue circle not in the intersection is labeled "Irrelevant items - retrieved".

The right diagram shows a yellow circle divided into two parts: B (Number of relevant records not retrieved) and A (Number of relevant records retrieved). The formula for Recall is:

$$\text{RECALL: } \frac{A}{A+B} \times 100\%$$

Two Venn diagrams illustrating Recall. The left diagram shows a yellow circle (relevant items) and a blue circle (retrieved items). The intersection is labeled 'Relevant items - retrieved'. The part of the yellow circle not in the intersection is labeled 'Relevant items - not retrieved'. The part of the blue circle not in the intersection is labeled 'Irrelevant items - retrieved'. The right diagram shows a yellow circle divided into two parts: a larger part labeled 'B' (Number of relevant records not retrieved) and a smaller part labeled 'A' (Number of relevant records retrieved). Below the diagram, the formula for Recall is given as RECALL: \frac{A}{A+B} \times 100%.

{30}------------------------------------------------
##### Classificação: Recall

- **Recall:** proporção de textos que deveriam ter sido corretamente classificados.

B: Number of relevant records not retrieved.  
A: Number of relevant records retrieved.  
 $RECALL: \frac{A}{A+B} \times 100\%$

Venn diagram illustrating Recall. A yellow circle is divided into two parts: A (hatched, representing retrieved relevant records) and B (solid yellow, representing not retrieved relevant records).

|                      |     | Preditor (Máquina) |     |
|----------------------|-----|--------------------|-----|
|                      |     | Classes            | Sim |
| Resultados Esperados | Sim | TP                 | FN  |
|                      | Não | FP                 | TN  |

$$Recall = \frac{TP}{TP+FN}$$

{31}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-00504fc688ebcf131ccbeff94dfc9939_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Venn diagram illustrating Recall. A yellow circle is divided into two parts: A (hatched, representing retrieved relevant records) and B (solid yellow, representing not retrieved relevant records).
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
  - **Resposta:** Para classe Iris-Virginica:
    - TP (Verdadeiro-Positivo): 38
    - TN (Verdadeiro-Negativo): 77
    - FP (Falso-Positivo): 3
    - FN (Falso-Negativo): 2

$$Recall_{virginica} = \frac{TP}{TP+FN} = \frac{38}{38+2} = 0,95$$

{34}------------------------------------------------
##### Classificação: Recall

- **Exemplo:** 120 amostras das classes **Iris-Setosa(a)**, **Iris-Versicolor(b)** e **Iris-Virginica(c)** foram testadas, 40 de cada classe.
  - **Atividade IV:** Calcule o recall (micro-média) para as classes iris-setosa e iris-virginica. Em seguida, calcula a macro-média de recall.
  - **Resposta:** Para classe **Iris-Setosa**:
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
    - $Recall_{versicolor} = \frac{TP}{TP+FN} = \frac{37}{37+3} = 0,925$

{36}------------------------------------------------
##### Classificação: F-Measure

- Média Harmônica das medidas Precision e Recall

$$F1 = \frac{2 \times Precision \times Recall}{Precision + Recall}$$

- **Exemplo:** 120 amostras das classes **Iris-Setosa(a)**, **Iris-Versicolor(b)** e **Iris-Virginica(c)** foram testadas, 40 de cada classe.

- $F - Measure_{versicolor} = \frac{2 \times 0,9487 \times 0,925}{0,9487 + 0,925} = 0,9367$
- $F - Measure_{setosa} = \frac{2 \times 1 \times 1}{1 + 1} = 1$
- $F - Measure_{virginica} = \frac{2 \times 0,9268 \times 0,95}{0,9268 + 0,95} = 0,9382$
- Macro-Média:  $F - Measure = \frac{0,9367 + 1 + 0,9382}{3} = 0,9583$
