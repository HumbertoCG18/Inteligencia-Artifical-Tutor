<!-- EXEC_SUMMARY_START -->
## Sumário
> *Leia antes de varrer o arquivo. Vá direto à seção relevante para a pergunta do aluno.*

- **Subáreas da Inteligência Artificial**
  - Aprendizado Não Supervisionado
  - Aprendizado Não Supervisionado
  - Agrupamento
  - Agrupamento
  - Agrupamento
  - Agrupamento
  - Agrupamento
  - Agrupamento
  - Agrupamento
  - Agrupamento
  - Cluster 1
- **Cluster 2**
  - Cluster 1
  - Cluster 2
  - Cluster 2
  - Cluster 2
  - Cluster 1
  - Cluster 2
- **Cluster 2**
- **Cluster 2**
  - Cluster 2
  - Cluster 2
- **k-means: Algoritmo de agrupamento particional**
- **k-means: Algoritmo de agrupamento particional**
- **K-Means**
  - `sklearn.cluster.KMeans`
- **K-Means**
  - `sklearn.cluster.KMeans`
- **K-Means**
  - K-Means e o método Elbow
  - K-Means e o método Elbow
  - K-Means e o método Elbow
  - K-Means e o método Elbow
  - K-Means e o método Elbow
  - K-Means e o método Elbow
- **Dinâmica**

<!-- EXEC_SUMMARY_END -->
<!-- DATALAB_CHUNK 1: pages 1-20 -->

{0}------------------------------------------------

# Aprendizado não supervisionado: parte 1

Profa Silvia Moraes

{1}------------------------------------------------
## Subáreas da Inteligência Artificial

The diagram illustrates the subareas of Artificial Intelligence (IA) centered around a core concept. At the center is a circular icon with the text "Inteligência Artificial (IA)" surrounded by eight curved segments, one of which is highlighted in red. Six lines radiate from this center to different subareas, each with its own list of components.

**Aprendizado de Máquina (Machine Learning)**

- Aprendizado Profundo (Deep Learning)
- Aprendizado Supervisionado
- Aprendizado Não Supervisionado
- Aprendizado por Reforço
- Aprendizado auto-supervisionado
- Aprendizado semissupervisionado

**Processamento de Linguagem Natural**

- Extração de Informações
- Classificação de Texto
- Tradução Automática
- Perguntas e Respostas
- Geração de Texto

**Raciocínio Automatizado**

**Robótica**

**IA Explicável**

**Visão Computacional**

Diagram of Artificial Intelligence subareas

{2}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-9ba3dc91984c80b96f217fb1bddd5c06_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of Artificial Intelligence subareas
<!-- /IMAGE_DESCRIPTION -->
### Aprendizado Não Supervisionado

- **Não exige** que os **dados** estejam **rotulados**
- Sem crítica, **usa regularidades e propriedades estatísticas** dos dados no processo de aprendizagem.

**Entrada (x):**  
Imagem ou características

<https://www.pexels.com/>

**Dataset Sem Anotação**

→

**Algoritmo de Machine Learning Supervisionado**

**Treinamento**

→

**Modelo**

A collage of images showing various animals including cats, dogs, and chickens, representing an unlabeled dataset. A URL 'https://www.pexels.com/' is visible on one of the images. Icon of a neural network with orange, purple, and grey nodes. Icon of a neural network with orange, purple, and grey nodes.

{3}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-7055f51feb10ea4ea48b27c36f085286_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A collage of images showing various animals including cats, dogs, and chickens, representing an unlabeled dataset.
<!-- /IMAGE_DESCRIPTION -->
### Aprendizado Não Supervisionado

Executa **tarefas descritivas**: explora ou descreve um conjunto de dados.

- **Agrupamento**: divisão em grupos baseada em alguma regularidade ou similaridade
- **Sumarização**: descrição simples e compacta
- **Associação**: relações frequentes entre dados

A close-up photograph of several apples, showing a mix of red and green colors, illustrating data points.

A close-up photograph of several apples, showing a mix of red and green colors, illustrating data points.

A close-up photograph of a large group of plush toys, including purple monkeys and yellow bears, illustrating data points.

A close-up photograph of a large group of plush toys, including purple monkeys and yellow bears, illustrating data points.

{4}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-16d86083b7ebdc40c0647a1d3d46ace7_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A close-up photograph of several apples, showing a mix of red and green colors, illustrating data points.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-b615ff07e8a0f467f0a6f4783c4463eb_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A close-up photograph of a large group of plush toys, including purple monkeys and yellow bears, illustrating data points.
<!-- /IMAGE_DESCRIPTION -->
### Agrupamento

Organiza dados (não classificados, sem rótulos) em grupos de acordo com alguma medida de similaridade.

**Entrada (x):**  
Imagem ou características

<https://www.pexels.com/>

**Dataset Sem Anotação**

**Algoritmo de Machine Learning Supervisionado**

**Generalização**

**Modelo**

**Grupos**

Diagram illustrating the clustering process. On the left, an 'Entrada (x): Imagem ou características' section shows a collage of unlabeled images of cats, dogs, and chickens, labeled as 'Dataset Sem Anotação'. An arrow points to a central box labeled 'Algoritmo de Machine Learning Supervisionado' which includes 'Generalização' and a 'Modelo' icon. Another arrow points to the right, labeled 'Grupos', showing three distinct clusters: one with cats, one with chickens, and one with dogs.

{5}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-e394c2b5c61344f6a12397f430086072_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram illustrating the clustering process.
<!-- /IMAGE_DESCRIPTION -->
### Agrupamento
#### - **Características:**

- Técnica aplicada para organizar os dados quando não há classe para predizer.
- Pode ser usado como uma etapa anterior a alguma tarefa, como por exemplo: sumarização.
- **Grupos:** formados por dados (objetos) que compartilham características (podem ser mais genéricos ou mais especializados, diferentes níveis de refinamento).  
Espera-se:
  - Alta similaridade intra-grupo.
  - Baixa similaridade entre grupos.

{6}------------------------------------------------
### Agrupamento

- **Etapas:**
  - preparação,
  - proximidade,
  - agrupamento,
  - validação e
  - interpretação.

The diagram illustrates the clustering process, starting with **Objetos** (Objects) and **Conhecimento do usuário/especialista** (User/specialist knowledge). The process is contained within a box labeled **Processo de agrupamento** (Clustering process).

The stages are:

- Preparação** (Preparation): Receives input from **Objetos** and **Conhecimento do usuário/especialista**. It outputs **Representação dos objetos** (Representation of objects) to the next stage.
- Proximidade** (Proximity): Receives input from **Preparação** and **Conhecimento do usuário/especialista**. It outputs **Medida de similaridade** (Similarity measure) to the next stage.
- Agrupamento** (Clustering): Receives input from **Preparação**, **Proximidade**, and **Conhecimento do usuário/especialista**. It outputs **Clusters** to the next stage.
- Validação** (Validation): Receives input from **Agrupamento** and **Conhecimento do usuário/especialista**.
- Interpretação** (Interpretation): Receives input from **Validação** and **Conhecimento do usuário/especialista**.

Feedback loops are shown with dashed arrows from **Proximidade**, **Agrupamento**, **Validação**, and **Interpretação** back to **Preparação**. The final outputs are **Clusters validados** (Validated clusters) and **Significados dos clusters** (Cluster meanings).

Diagram of the clustering process showing five stages: Preparação, Proximidade, Agrupamento, Validação, and Interpretação, with feedback loops and user input.

{7}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-a738993919a50143787084ee7ce6e2f2_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of the clustering process showing five stages: Preparação, Proximidade, Agrupamento, Validação, and Interpretação, with feedback loops and user input.
<!-- /IMAGE_DESCRIPTION -->
#### Agrupamento
#### Etapas:

- **Preparação:** inclui pré-processamento (ex: normalizações, conversão de tipos e redução de dimensionalidade) e forma de representação dos dados (ex: matriz de similaridade) para que o algoritmo de agrupamento possa ser usado.
- **Proximidade:** definição de medidas de proximidade apropriadas ao domínio e ao tipo de informação que se deseja extrair dos dados. Existem medidas para atributos quantitativos e qualitativos.

{8}------------------------------------------------
### Agrupamento

Etapas: ...

- **Proximidade:** Medidas para atributos quantitativos e qualitativos.
  - Medidas de Distância: atributos contínuos e racionais:

- Manhattan:  $d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$  (usual para binários)

- Euclidiana:  $d(x_i, x_j) = \sqrt{\sum_{l=1}^d (x_i^l - x_j^l)^2}$

- Chebyshev (ou supremum):  $d(x_i, x_j) = \max_{1 \leq l \leq d} |x_i^l - x_j^l|$

The diagram illustrates three distance metrics on a 2D grid between points  $x_i$  (at the origin) and  $x_j$  (at coordinates (3, 3)).

- Distância de Manhattan:** Represented by a dashed line path that moves vertically from  $x_i$  to (0, 3) and then horizontally to  $x_j$ .
- Distância euclidiana:** Represented by a solid straight line segment connecting  $x_i$  and  $x_j$ .
- Distância de Chebyshev:** Indicated by a dashed horizontal line from  $x_i$  to (3, 0), representing the maximum coordinate difference.

Diagram illustrating distance metrics on a 2D grid. A point x\_i is at the origin, and a point x\_j is at (3, 3). The Manhattan distance is shown as a dashed line path from x\_i to (3, 3) via (0, 3). The Euclidean distance is shown as a solid diagonal line from x\_i to x\_j. The Chebyshev distance is indicated by a dashed horizontal line from x\_i to (3, 0).

{9}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-0f3e3ea50bcceb86f6c524ab2b6f3e7a_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram illustrating distance metrics on a 2D grid.
<!-- /IMAGE_DESCRIPTION -->
### Agrupamento

Etapas: ...

- **Proximidade:** Medidas para Atributos Quantitativos:
  - Medidas de Similaridade:

- Separação angular (cosseno): 
$$\cos(x_i, x_j) = \frac{\sum_{l=1}^d x_l^i x_l^j}{\sqrt{\sum_{l=1}^d x_l^i{}^2 \sum_{l=1}^d x_l^j{}^2}}$$

- Pearson: 
$$p(x_i, x_j) = \frac{\sum_{l=1}^d (x_l^i - \bar{x}_i)(x_l^j - \bar{x}_j)}{\sqrt{\sum_{l=1}^d (x_l^i - \bar{x}_i)^2 \sum_{l=1}^d (x_l^j - \bar{x}_j)^2}}$$
 (quando magnitude não é importante, mas sim o grau de variação. Ex: Bioinformática)

The figure shows a 2D coordinate system with a grid. Two vectors,  $x_i$  and  $x_j$ , originate from the origin. Vector  $x_i$  points into the first quadrant, and vector  $x_j$  points into the fourth quadrant. The angle between  $x_i$  and  $x_j$  is labeled  $\alpha$ . Another vector  $x_i'$  is shown in the second quadrant, and vector  $x_j'$  is in the third quadrant. The angle between  $x_i'$  and  $x_j'$  is labeled  $\beta$ . The word 'cosseno' is written near vector  $x_j$ , and 'irson' is written near vector  $x_j'$ .

Diagram illustrating angular separation (cosseno) between two vectors x\_i and x\_j in a 2D space. The angle between them is labeled alpha. The diagram also shows vectors x\_i' and x\_j' and angles labeled cosseno and irson.

{10}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-8ee3b76dd49f31624d287885bc2c81ee_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram illustrating angular separation (cosseno) between two vectors x_i and x_j in a 2D space.
<!-- /IMAGE_DESCRIPTION -->
### Agrupamento

Etapas: ...

- **Proximidade:** Medidas para Atributos Qualitativos:
  - São obtidas a partir da soma das contribuições individuais de todos os atributos.
  - Para atributos nominais, a distância mais usada é a de Hamming.

$$d(x_i, x_j) = \sum_{l=1}^d a(x_i^l, x_j^l) , \text{ onde } a(x_i^l, x_j^l) = \begin{cases} 1 & \text{se } x_i^l \neq x_j^l \\ 0 & \text{c.c} \end{cases}$$

{11}------------------------------------------------
### Agrupamento
#### Etapas: ...

- **agrupamento:** nessa etapa um ou mais algoritmos de agrupamento são usados para gerar os grupos.
- **validação:** etapa que verifica se os grupos gerados são significativos. Ajuda a determinar o número adequado de
- **grupos:** quando esse número não é conhecido.
- **interpretação:** processo de examinar o grupo em relação aos outros com o objetivo de rotulá-lo, indicando a natureza do grupo.

{12}------------------------------------------------
### Agrupamento
#### Tipos:

The figure illustrates three different clustering paradigms. On the left, partitional clustering is shown with three distinct, non-overlapping groups of data points: blue, red, and yellow. In the center, hierarchical clustering is depicted as a series of nested ellipses, where smaller groups of green points are progressively merged into larger, encompassing ellipses. On the right, fuzzy clustering is represented by a 2D plot where data points (A, B, C, D, E, F) have varying degrees of membership in two overlapping clusters, shown as a light blue and a light yellow ellipse. Below the plot is a dendrogram showing the hierarchical merging of these points, with a red line indicating a specific cut-off level.

Diagram illustrating three types of clustering: Partitional, Hierarchical, and Fuzzy.

- **Agrupamento Particional:** Divisão dos objetos de dados em subconjuntos (grupos) sem sobreposição tal que cada objeto de dados está em exatamente um único grupo.
- **Agrupamento Hierárquico:** Um conjunto de grupos aninhados na forma de uma árvore hierárquica.

{13}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-b05a8a3551db31147979064952179990_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram illustrating three types of clustering: Partitional, Hierarchical, and Fuzzy.
<!-- /IMAGE_DESCRIPTION -->
#### Exemplos de Agrupamento Particional

**Agrupamento produtos**  
de acordo com as suas características.

Diagram showing a pile of mixed potatoes being sorted into three separate groups: red potatoes, yellow potatoes, and purple potatoes, indicated by a green arrow.

**Agrupamento de textos**

Diagram showing a stack of mixed yellow and blue documents being sorted into two separate stacks, one yellow and one blue, indicated by a blue arrow.

**Agrupamento de clientes**  
Identificação de perfil para  
recomendação de  
produtos

Diagram showing a group of people icons, some blue and some green, being sorted into two separate groups: one with all blue icons and another with all green icons, indicated by an orange arrow.

**Agrupamento de dados similares**

| sepal length | sepal width | petal length | petal width |
|--------------|-------------|--------------|-------------|
| 5,1          | 3,5         | 1,4          | 0,2         |
| 4,9          | 3,0         | 1,4          | 0,2         |
| 7,0          | 3,2         | 4,7          | 7,1         |
| 6,4          | 3,2         | 4,5          | 1,5         |
| 6,3          | 3,3         | 6,0          | 2,5         |
| 5,8          | 2,7         | 5,1          | 1,9         |

A red arrow pointing from the data table to the first cluster (Grupo 1).

Diagram showing three clusters of data points from the table above, each enclosed in a light grey oval. Grupo 1 contains the first two rows (petal width 0,2). Grupo 2 contains the third and fourth rows (petal length 4,7 and 4,5). Grupo 3 contains the last three rows (petal length 6,0, 6,0, 5,1).

Grupo 1

|     |     |     |     |
|-----|-----|-----|-----|
| 5,1 | 3,5 | 1,4 | 0,2 |
| 4,9 | 3,0 | 1,4 | 0,2 |

Grupo 2

|     |     |     |     |
|-----|-----|-----|-----|
| 7,0 | 3,2 | 4,7 | 7,1 |
| 6,4 | 3,2 | 4,5 | 1,5 |

Grupo 3

|     |     |     |     |
|-----|-----|-----|-----|
| 6,3 | 3,3 | 6,0 | 2,5 |
| 5,8 | 2,7 | 5,1 | 1,9 |

{14}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-7832324609ad3cc688064e0341612b32_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram showing a pile of mixed potatoes being sorted into three separate groups: red potatoes, yellow potatoes, and purple potatoes, indicated by a green arrow.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-df6babe297323feb1575ba89f5cf3b09_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram showing a stack of mixed yellow and blue documents being sorted into two separate stacks, one yellow and one blue, indicated by a blue arrow.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-3293245c6893d9d49c2c878828423ecd_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram showing a group of people icons, some blue and some green, being sorted into two separate groups: one with all blue icons and another with all green icons, indicated by an orange arrow.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-b77cd8b2f763af8d453537177ac5942f_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A red arrow pointing from the data table to the first cluster (Grupo 1).
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-70f5f44cb855bbb0c203c00187b2113e_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram showing three clusters of data points from the table above, each enclosed in a light grey oval.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-0928cdf6e30b6fef3f510d120adeb39d_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Red arrow pointing to the first column of the table
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-5fb25b0024985e77cd12c62a7255055e_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Red arrow pointing to the last row of the table.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-0f4ae20874db623ff48a27215649ce03_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A blue arrow pointing from the text 'X contém os dados de entrada' to the variable 'X' in the 'kmeanModel.fit(X)' line of code.
<!-- /IMAGE_DESCRIPTION -->
#### Agrupamento Particional

Icon representing unlabeled data, showing three stacked cylinders.

Dados não rotulados

Red arrow pointing from the data icon to the Machine Learning algorithm box.

Algoritmo de Machine Learning

Red arrow pointing from the Machine Learning algorithm box to the Results text.

Resultados

| sepal length | sepal width | petal length | petal width |
|--------------|-------------|--------------|-------------|
| 5,1          | 3,5         | 1,4          | 0,2         |
| 4,9          | 3,0         | 1,4          | 0,2         |
| 7,0          | 3,2         | 4,7          | 7,1         |
| 6,4          | 3,2         | 4,5          | 1,5         |
| 6,3          | 3,3         | 6,0          | 2,5         |
| 5,8          | 2,7         | 5,1          | 1,9         |

Red arrow pointing from the data table to the k-Means algorithm box.

Algoritmo k-Means

Red arrow pointing from the k-Means algorithm box to the grouped data tables.

Tarefa: agrupamento (clustering)

Grupo 1

|     |     |     |     |
|-----|-----|-----|-----|
| 5,1 | 3,5 | 1,4 | 0,2 |
| 4,9 | 3,0 | 1,4 | 0,2 |

Grupo 2

|     |     |     |     |
|-----|-----|-----|-----|
| 7,0 | 3,2 | 4,7 | 7,1 |
| 6,4 | 3,2 | 4,5 | 1,5 |

Grupo 3

|     |     |     |     |
|-----|-----|-----|-----|
| 6,3 | 3,3 | 6,0 | 2,5 |
| 5,8 | 2,7 | 5,1 | 1,9 |

{15}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-589af9a5d6f5bbbdc8f482e364688676_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Icon representing unlabeled data, showing three stacked cylinders.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-0e240e8e4783e664047fbdb5fbd0989f_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Red arrow pointing from the data icon to the Machine Learning algorithm box.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-be217a121b8cc1b82eb1598749372865_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Red arrow pointing from the Machine Learning algorithm box to the Results text.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-15ee1fd7e4011d0d5dcb11b291fb91d7_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Red arrow pointing from the data table to the k-Means algorithm box.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-2224b82995b3ba31aa82f20fb06f4c9c_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Red arrow pointing from the k-Means algorithm box to the grouped data tables.
<!-- /IMAGE_DESCRIPTION -->
##### k-means: Algoritmo de agrupamento particional

- **k-means:** Algoritmo de agrupamento particional.
- Características:
  - Cada grupo está associado a um centroide (objeto central).
  - Cada objeto é atribuído ao grupo com o centroide mais próximo.
  - Número de grupos ( $k$ ) deve ser especificado
  - Centroides iniciais são geralmente aleatórios.
  - Agrupamento varia conforme a inicialização.

{16}------------------------------------------------
##### k-means: Algoritmo de agrupamento particional

- **k-means:** Algoritmo de agrupamento particional.
- Características:
  - Centroides são (tipicamente) a média de todos os objetos do grupo.
  - A medida de distância geralmente empregada é a distância Euclidiana.
  - k-means geralmente converge com poucas iterações.
  - Complexidade é  $O(n.k.i.d)$ , onde
    - $n$  = número de objetos,
    - $k$  = número de grupos,
    - $i$ = número de iterações e
    - $d$ = número de atributos

{17}------------------------------------------------
##### k-means: Algoritmo de agrupamento particional

- **k-means:** Algoritmo de agrupamento particional.
  1. Selecione  $k$  objetos como centroides;
  2. Repita
    1. Calcule a distância de cada objeto em relação ao centroide de cada cluster  $k$
    2. O objeto será atribuído ao cluster  $k$  cujo centroide está mais próximo
    3. Depois de processar todos os dados, recalcule os centroides, considerando os dados em cada cluster  $k$ .
  3. Até que os centroides não mudem mais

{18}------------------------------------------------
##### k-means: Algoritmo de agrupamento particional

- **k-means:** Algoritmo de agrupamento particional. Exemplo:

| Padrão | Peso(Atributo1) | Altura(Atributo2) |
|--------|-----------------|-------------------|
| 1      | 2               | 8                 |
| 2      | 8               | 2                 |
| 3      | 6               | 8                 |
| 4      | 2               | 7                 |
| 5      | 8               | 4                 |
| 6      | 2               | 6                 |

$$\text{Manhattan: } d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$$

{19}------------------------------------------------
##### k-means: Algoritmo de agrupamento particional

- **k-means:** Algoritmo de agrupamento particional. Exemplo:

| Padrão | Peso(Atributo1) | Altura(Atributo2) |
|--------|-----------------|-------------------|
| 1      | 2               | 8                 |
| 2      | 8               | 2                 |
| 3      | 6               | 8                 |
| 4      | 2               | 7                 |
| 5      | 8               | 4                 |
| 6      | 2               | 6                 |

Manhattan:  $d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$
##### Cluster 1

Centroide: (2) [8,2]

Tuplas:
##### Cluster 2

Centroide: (6) [2,6]

Tuplas:

<!-- DATALAB_CHUNK 2: pages 21-40 -->

{20}------------------------------------------------

# k-means: Algoritmo de agrupamento particional

- **k-means:** Algoritmo de agrupamento particional. Exemplo:

| Padrão | Peso(Atributo1) | Altura(Atributo2) |
|--------|-----------------|-------------------|
| 1      | 2               | 8                 |
| 2      | 8               | 2                 |
| 3      | 6               | 8                 |
| 4      | 2               | 7                 |
| 5      | 8               | 4                 |
| 6      | 2               | 6                 |

Manhattan:  $d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$
### Cluster 1

Centroide: (2) [8,2]

Tuplas:
## Cluster 2

Centroide: (6) [2,6]

Tuplas:

**Tupla: (1) [2,8]**

Dist(C1,T1)=  $|8-2| + |2-8| = 12$

Dist(C2,T1) =  $|2-2| + |6-8| = 2$

{21}------------------------------------------------

# k-means: Algoritmo de agrupamento particional

- **k-means:** Algoritmo de agrupamento particional. Exemplo:

| Padrão | Peso(Atributo1) | Altura(Atributo2) |
|--------|-----------------|-------------------|
| 1      | 2               | 8                 |
| 2      | 8               | 2                 |
| 3      | 6               | 8                 |
| 4      | 2               | 7                 |
| 5      | 8               | 4                 |
| 6      | 2               | 6                 |

Manhattan:  $d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$
### Cluster 1

Centroide: (2) [8,2]

Tuplas:
### Cluster 2

Centroide: (6) [2,6]

Tuplas: [2,8]

**Tupla: (1) [2,8]**

**Dist(C1,T1) = |8-2| + |2-8| = 12**

**Dist(C2,T1) = |2-2| + |6-8| = 2**

{22}------------------------------------------------

# k-means: Algoritmo de agrupamento particional

- k-means:** Algoritmo de agrupamento particional. Exemplo:

| Padrão | Peso(Atributo1) | Altura(Atributo2) |
|--------|-----------------|-------------------|
| 1      | 2               | 8                 |
| 2      | 8               | 2                 |
| 3      | 6               | 8                 |
| 4      | 2               | 7                 |
| 5      | 8               | 4                 |
| 6      | 2               | 6                 |

Manhattan:  $d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$
#### Cluster 1

Centroide: (2) [8,2]

Tuplas: [8,2]
### Cluster 2

Centroide: (6) [2,6]

Tuplas: [2,8]

**Tupla: (2) [8,2]**

Dist(C1,T2)=  $|8-8| + |2-2| = 0$

Dist(C2,T2) =  $|2-8| + |6-2| = 10$

{23}------------------------------------------------

# k-means: Algoritmo de agrupamento particional

- k-means:** Algoritmo de agrupamento particional. Exemplo:

| Padrão | Peso(Atributo1) | Altura(Atributo2) |
|--------|-----------------|-------------------|
| 1      | 2               | 8                 |
| 2      | 8               | 2                 |
| 3      | 6               | 8                 |
| 4      | 2               | 7                 |
| 5      | 8               | 4                 |
| 6      | 2               | 6                 |

Manhattan:  $d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$
#### Cluster 1

Centroide: (2) [8,2]

Tuplas: [8,2]
### Cluster 2

Centroide: (6) [2,6]

Tuplas: [2,8] [6,8]

**Tupla: (3) [6,8]**

**Dist(C1,T3)= |8-6| + |2-8|=8**

**Dist(C2,T3) = |2-6| + |6-8|=6**

{24}------------------------------------------------

# k-means: Algoritmo de agrupamento particional

- **k-means:** Algoritmo de agrupamento particional. Exemplo:

| Padrão | Peso(Atributo1) | Altura(Atributo2) |
|--------|-----------------|-------------------|
| 1      | 2               | 8                 |
| 2      | 8               | 2                 |
| 3      | 6               | 8                 |
| 4      | 2               | 7                 |
| 5      | 8               | 4                 |
| 6      | 2               | 6                 |

Manhattan:  $d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$
### Cluster 1

Centroide: (2) [8,2]

Tuplas: [8,2]
### Cluster 2

Centroide: (6) [2,6]

Tuplas: [2,8] [6,8] [2,7]

**Tupla: (4) [2,7]**

**Dist(C1,T4) = |8-2| + |2-7| = 11**

**Dist(C2,T4) = |2-2| + |6-7| = 1**

{25}------------------------------------------------

# k-means: Algoritmo de agrupamento particional

- k-means:** Algoritmo de agrupamento particional. Exemplo:

| Padrão | Peso(Atributo1) | Altura(Atributo2) |
|--------|-----------------|-------------------|
| 1      | 2               | 8                 |
| 2      | 8               | 2                 |
| 3      | 6               | 8                 |
| 4      | 2               | 7                 |
| 5      | 8               | 4                 |
| 6      | 2               | 6                 |

Manhattan:  $d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$
#### Cluster 1

Centroide: (2) [8,2]

Tuplas: [8,2], [8,4]
## Cluster 2

Centroide: (6) [2,6]

Tuplas: [2,8] [6,8] [2,7]

**Tupla: (5) [8,4]**

**Dist(C1,T5)= |8-8|+|2-4|=2**

**Dist(C2,T5) = |2-8| + |6-4|=8**

{26}------------------------------------------------

# k-means: Algoritmo de agrupamento particional

- k-means:** Algoritmo de agrupamento particional. Exemplo:

| Padrão | Peso(Atributo1) | Altura(Atributo2) |
|--------|-----------------|-------------------|
| 1      | 2               | 8                 |
| 2      | 8               | 2                 |
| 3      | 6               | 8                 |
| 4      | 2               | 7                 |
| 5      | 8               | 4                 |
| 6      | 2               | 6                 |

Manhattan:  $d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$
#### Cluster 1

Centroide: (2) [8,2]

Tuplas: [8,2], [8,4]
## Cluster 2

Centroide: (6) [2,6]

Tuplas: [2,8] [6,8] [2,7] [2,6]

**Tupla: (6) [2,6]**

**Dist(C1,T6) = |8-2| + |2-6| = 10**

**Dist(C2,T6) = |2-2| + |6-6| = 0**

{27}------------------------------------------------

# k-means: Algoritmo de agrupamento particional

- **k-means:** Algoritmo de agrupamento particional. Exemplo:

| Padrão | Peso(Atributo1) | Altura(Atributo2) |
|--------|-----------------|-------------------|
| 1      | 2               | 8                 |
| 2      | 8               | 2                 |
| 3      | 6               | 8                 |
| 4      | 2               | 7                 |
| 5      | 8               | 4                 |
| 6      | 2               | 6                 |

Manhattan:  $d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$
#### Cluster 1

Centroide: ~~(2) [8,2]~~ [8,3]

Tuplas: [8,2], [8,4]
### Cluster 2

Centroide: (6) [2,6]

Tuplas: [2,8] [6,8] [2,7] [2,6]

Recalculando os centroides:

Cluster1:

$[(8+8)/2, (2+4)/2] = [8,3]$

{28}------------------------------------------------

# k-means: Algoritmo de agrupamento particional

- k-means:** Algoritmo de agrupamento particional. Exemplo:

| Padrão | Peso(Atributo1) | Altura(Atributo2) |
|--------|-----------------|-------------------|
| 1      | 2               | 8                 |
| 2      | 8               | 2                 |
| 3      | 6               | 8                 |
| 4      | 2               | 7                 |
| 5      | 8               | 4                 |
| 6      | 2               | 6                 |

Manhattan:  $d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$
#### Cluster 1

Centroide: ~~(2, 8)~~ ~~(8, 2)~~ [8, 3]

Tuplas: [8, 2], [8, 4]
### Cluster 2

Centroide: ~~(6, 2)~~ ~~(2, 6)~~ [3, 7.25]

Tuplas: [2, 8] [6, 8] [2, 7] [2, 6]

Recalculando os centroides:

Cluster2:

$[(2+6+2+2)/4, (8+8+7+6)/4] = [3, 7.25]$

{29}------------------------------------------------

# k-means: Algoritmo de agrupamento particional

- **Dinâmica:** Execute 1 iteração e determine o centróide, considerando que as tuplas 2 e 4 foram escolhidas como centróides:

|   | Atributo 1 | Atributo 2 | Atributo 3 | Atributo 4 |
|---|------------|------------|------------|------------|
| 1 | 5          | 4          | 3          | 1          |
| 2 | 1          | 0          | 1          | 2          |
| 3 | 2          | 1          | 0          | 2          |
| 4 | 6          | 3          | 6          | 1          |
| 5 | 3          | 4          | 2          | 3          |
| 6 | 3          | 3          | 1          | 3          |

{30}------------------------------------------------

# k-means: Algoritmo de agrupamento particional

- Dinâmica:** Execute 1 iteração e determine o centróide, considerando que as tuplas 2 e 4 foram escolhidas como centróides:

Manhattan:  $d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$

|   | Atributo 1 | Atributo 2 | Atributo 3 | Atributo 4 |
|---|------------|------------|------------|------------|
| 1 | 5          | 4          | 3          | 1          |
| 2 | 1          | 0          | 1          | 2          |
| 3 | 2          | 1          | 0          | 2          |
| 4 | 6          | 3          | 6          | 1          |
| 5 | 3          | 4          | 2          | 3          |
| 6 | 3          | 3          | 1          | 3          |

Centroide 1 (C1) = [ 1, 0, 1, 2 ] (Tupla 2)

Centroide 2 (C2) = [ 6, 3, 6, 1 ] (Tupla 4)

{31}------------------------------------------------

# k-means: Algoritmo de agrupamento particional

- Dinâmica:** Execute 1 iteração e determine o centróide, considerando que as tuplas 2 e 4 foram escolhidas como centróides:

$$\text{Manhattan: } d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$$

|   | Atributo 1 | Atributo 2 | Atributo 3 | Atributo 4 |
|---|------------|------------|------------|------------|
| 1 | 5          | 4          | 3          | 1          |
| 2 | 1          | 0          | 1          | 2          |
| 3 | 2          | 1          | 0          | 2          |
| 4 | 6          | 3          | 6          | 1          |
| 5 | 3          | 4          | 2          | 3          |
| 6 | 3          | 3          | 1          | 3          |

Centroide 1 (C1) = [ 1, 0, 1, 2 ] (Tupla 2)

- Dist(C1, Tupla1) =  $|1-5| + |0-4| + |1-3| + |2-1| = 11$
- Dist(C1, Tupla2) = 0
- Dist(C1, Tupla3) =  $|1-2| + |0-1| + |1-0| + |2-2| = 3$
- Dist(C1, Tupla4) =  $|1-6| + |0-3| + |1-6| + |2-1| = 14$
- Dist(C1, Tupla5) =  $|1-3| + |0-4| + |1-2| + |2-3| = 8$
- Dist(C1, Tupla 6) =  $|1-3| + |0-3| + |1-1| + |2-3| = 6$

Centroide 2 (C2) = [ 6, 3, 6, 1 ] (Tupla 4)

- Dist(C2, Tupla1) =  $|6-5| + |3-4| + |6-3| + |1-1| = 5$
- Dist(C2, Tupla2) =  $|6-1| + |3-0| + |6-1| + |1-2| = 14$
- Dist(C2, Tupla3) =  $|6-2| + |3-1| + |6-0| + |1-2| = 13$
- Dist(C2, Tupla4) = 0
- Dist(C2, Tupla5) =  $|6-3| + |3-4| + |6-2| + |1-3| = 10$
- Dist(C2, Tupla 6) =  $|6-3| + |3-3| + |6-1| + |1-3| = 10$

{32}------------------------------------------------

# k-means: Algoritmo de agrupamento particional

- Dinâmica:** Execute 1 iteração e determine o centróide, considerando que as tuplas 2 e 4 foram escolhidas como centróides:

Manhattan:  $d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$

|   | Atributo 1 | Atributo 2 | Atributo 3 | Atributo 4 |
|---|------------|------------|------------|------------|
| 1 | 5          | 4          | 3          | 1          |
| 2 | 1          | 0          | 1          | 2          |
| 3 | 2          | 1          | 0          | 2          |
| 4 | 6          | 3          | 6          | 1          |
| 5 | 3          | 4          | 2          | 3          |
| 6 | 3          | 3          | 1          | 3          |

Centroide 1 (C1) = [ 1, 0, 1, 2 ] (Tupla 2)

- Dist(C1, Tupla1) =  $|1-5| + |0-4| + |1-3| + |2-1| = 11$
- Dist(C1, Tupla2) = 0
- Dist(C1, Tupla3) =  $|1-2| + |0-1| + |1-0| + |2-2| = 3$
- Dist(C1, Tupla4) =  $|1-6| + |0-3| + |1-6| + |2-1| = 14$
- Dist(C1, Tupla5) =  $|1-3| + |0-4| + |1-2| + |2-3| = 8$
- Dist(C1, Tupla6) =  $|1-3| + |0-3| + |1-1| + |2-3| = 6$

Centroide 2 (C2) = [ 6, 3, 6, 1 ] (Tupla 4)

- Dist(C2, Tupla1)** =  $|6-5| + |3-4| + |6-3| + |1-1| = 5$
- Dist(C2, Tupla2) =  $|6-1| + |3-0| + |6-1| + |1-2| = 14$
- Dist(C2, Tupla3) =  $|6-2| + |3-1| + |6-0| + |1-2| = 13$
- Dist(C2, Tupla4) = 0
- Dist(C2, Tupla5) =  $|6-3| + |3-4| + |6-2| + |1-3| = 10$
- Dist(C2, Tupla6) =  $|6-3| + |3-3| + |6-1| + |1-3| = 10$

{33}------------------------------------------------

# k-means: Algoritmo de agrupamento particional

- Dinâmica:** Execute 1 iteração e determine o centróide, considerando que as tuplas 2 e 4 foram escolhidas como centróides:

Manhattan:  $d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$

|   | Atributo 1 | Atributo 2 | Atributo 3 | Atributo 4 |
|---|------------|------------|------------|------------|
| 1 | 5          | 4          | 3          | 1          |
| 2 | 1          | 0          | 1          | 2          |
| 3 | 2          | 1          | 0          | 2          |
| 4 | 6          | 3          | 6          | 1          |
| 5 | 3          | 4          | 2          | 3          |
| 6 | 3          | 3          | 1          | 3          |

Centroide 1 (C1) = [ 1, 0, 1, 2 ] (Tupla 2)

- Dist(C1, Tupla2) = 0**
- Dist(C1, Tupla3) =  $|1-2| + |0-1| + |1-0| + |2-2| = 3$
- Dist(C1, Tupla4) =  $|1-6| + |0-3| + |1-6| + |2-1| = 14$
- Dist(C1, Tupla5) =  $|1-3| + |0-4| + |1-2| + |2-3| = 8$
- Dist(C1, Tupla 6) =  $|1-3| + |0-3| + |1-1| + |2-3| = 6$

Centroide 2 (C2) = [ 6, 3, 6, 1 ] (Tupla 4)

[ 5, 4, 3, 1 ]

- Dist(C2, Tupla2) =  $|6-1| + |3-0| + |6-1| + |1-2| = 14$
- Dist(C2, Tupla3) =  $|6-2| + |3-1| + |6-0| + |1-2| = 13$
- Dist(C2, Tupla4) = 0
- Dist(C2, Tupla5) =  $|6-3| + |3-4| + |6-2| + |1-3| = 10$
- Dist(C2, Tupla 6) =  $|6-3| + |3-3| + |6-1| + |1-3| = 10$

{34}------------------------------------------------

# k-means: Algoritmo de agrupamento particional

- Dinâmica:** Execute 1 iteração e determine o centróide, considerando que as tuplas 2 e 4 foram escolhidas como centróides:

Manhattan:  $d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$

|   | Atributo 1 | Atributo 2 | Atributo 3 | Atributo 4 |
|---|------------|------------|------------|------------|
| 1 | 5          | 4          | 3          | 1          |
| 2 | 1          | 0          | 1          | 2          |
| 3 | 2          | 1          | 0          | 2          |
| 4 | 6          | 3          | 6          | 1          |
| 5 | 3          | 4          | 2          | 3          |
| 6 | 3          | 3          | 1          | 3          |

Centroide 1 (C1) = [ 1, 0, 1, 2 ] (Tupla 2)  
[1, 0, 1, 2]

- Dist(C1, Tupla3) =  $|1-2| + |0-1| + |1-0| + |2-2| = 3$
- Dist(C1, Tupla4) =  $|1-6| + |0-3| + |1-6| + |2-1| = 14$
- Dist(C1, Tupla5) =  $|1-3| + |0-4| + |1-2| + |2-3| = 8$
- Dist(C1, Tupla 6) =  $|1-3| + |0-3| + |1-1| + |2-3| = 6$

Centroide 2 (C2) = [ 6, 3, 6, 1 ] (Tupla 4)  
[ 5, 4, 3, 1 ]

- Dist(C2, Tupla3) =  $|6-2| + |3-1| + |6-0| + |1-2| = 13$
- Dist(C2, Tupla4) = 0
- Dist(C2, Tupla5) =  $|6-3| + |3-4| + |6-2| + |1-3| = 10$
- Dist(C2, Tupla 6) =  $|6-3| + |3-3| + |6-1| + |1-3| = 10$

{35}------------------------------------------------

# k-means: Algoritmo de agrupamento particional

- Dinâmica:** Execute 1 iteração e determine o centróide, considerando que as tuplas 2 e 4 foram escolhidas como centróides:

Manhattan:  $d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$

|   | Atributo 1 | Atributo 2 | Atributo 3 | Atributo 4 |
|---|------------|------------|------------|------------|
| 1 | 5          | 4          | 3          | 1          |
| 2 | 1          | 0          | 1          | 2          |
| 3 | 2          | 1          | 0          | 2          |
| 4 | 6          | 3          | 6          | 1          |
| 5 | 3          | 4          | 2          | 3          |
| 6 | 3          | 3          | 1          | 3          |

Centroide 1 (C1) = [ 1, 0, 1, 2 ] (Tupla 2)

[1, 0, 1, 2]

[2, 1, 0, 2]

- Dist(C1, Tupla4) =  $|1-6| + |0-3| + |1-6| + |2-1| = 14$
- Dist(C1, Tupla5) =  $|1-3| + |0-4| + |1-2| + |2-3| = 8$
- Dist(C1, Tupla 6) =  $|1-3| + |0-3| + |1-1| + |2-3| = 6$

Centroide 2 (C2) = [ 6, 3, 6, 1 ] (Tupla 4)

[ 5, 4, 3, 1 ]

- Dist(C2, Tupla4) = 0**
- Dist(C2, Tupla5) =  $|6-3| + |3-4| + |6-2| + |1-3| = 10$
- Dist(C2, Tupla 6) =  $|6-3| + |3-3| + |6-1| + |1-3| = 10$

{36}------------------------------------------------

# k-means: Algoritmo de agrupamento particional

- Dinâmica:** Execute 1 iteração e determine o centróide, considerando que as tuplas 2 e 4 foram escolhidas como centróides:

Manhattan:  $d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$

|   | Atributo 1 | Atributo 2 | Atributo 3 | Atributo 4 |
|---|------------|------------|------------|------------|
| 1 | 5          | 4          | 3          | 1          |
| 2 | 1          | 0          | 1          | 2          |
| 3 | 2          | 1          | 0          | 2          |
| 4 | 6          | 3          | 6          | 1          |
| 5 | 3          | 4          | 2          | 3          |
| 6 | 3          | 3          | 1          | 3          |

Centroide 1 (C1) = [ 1, 0, 1, 2 ] (Tupla 2)

[1, 0, 1, 2]

[2, 1, 0, 2]

- Dist(C1, Tupla5) =  $|1-3| + |0-4| + |1-2| + |2-3| = 8$

- Dist(C1, Tupla 6) =  $|1-3| + |0-3| + |1-1| + |2-3| = 6$

Centroide 2 (C2) = [ 6, 3, 6, 1 ] (Tupla 4)

[ 5, 4, 3, 1 ]

[ 6, 3, 6, 1 ]

- Dist(C2, Tupla5) =  $|6-3| + |3-4| + |6-2| + |1-3| = 10$

- Dist(C2, Tupla 6) =  $|6-3| + |3-3| + |6-1| + |1-3| = 10$

{37}------------------------------------------------

# k-means: Algoritmo de agrupamento particional

- Dinâmica:** Execute 1 iteração e determine o centróide, considerando que as tuplas 2 e 4 foram escolhidas como centróides:

Manhattan:  $d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$

|   | Atributo 1 | Atributo 2 | Atributo 3 | Atributo 4 |
|---|------------|------------|------------|------------|
| 1 | 5          | 4          | 3          | 1          |
| 2 | 1          | 0          | 1          | 2          |
| 3 | 2          | 1          | 0          | 2          |
| 4 | 6          | 3          | 6          | 1          |
| 5 | 3          | 4          | 2          | 3          |
| 6 | 3          | 3          | 1          | 3          |

Centroide 1 (C1) = [ 1, 0, 1, 2 ] (Tupla 2)

[1, 0, 1, 2]

[2, 1, 0, 2]

[3, 4, 2, 3]

- Dist(C1, Tupla 6) =  $|1-3| + |0-3| + |1-1| + |2-3| = 6$

Centroide 2 (C2) = [ 6, 3, 6, 1 ] (Tupla 4)

[5, 4, 3, 1]

[6, 3, 6, 1]

- Dist(C2, Tupla 6) =  $|6-3| + |3-3| + |6-1| + |1-3| = 10$

Red arrow pointing to the last row of the table.

{38}------------------------------------------------

# k-means: Algoritmo de agrupamento particional

- Dinâmica:** Execute 1 iteração e determine o centróide, considerando que as tuplas 2 e 4 foram escolhidas como centróides:

Manhattan:  $d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$

|   | Atributo 1 | Atributo 2 | Atributo 3 | Atributo 4 |
|---|------------|------------|------------|------------|
| 1 | 5          | 4          | 3          | 1          |
| 2 | 1          | 0          | 1          | 2          |
| 3 | 2          | 1          | 0          | 2          |
| 4 | 6          | 3          | 6          | 1          |
| 5 | 3          | 4          | 2          | 3          |
| 6 | 3          | 3          | 1          | 3          |

Centroide 1 (C1) = [ 1, 0, 1, 2 ] (Tupla 2)

[1, 0, 1, 2]

[2, 1, 0, 2]

[3, 4, 2, 3]

[3, 3, 1, 3]

Centroide 2 (C2) = [ 6, 3, 6, 1 ] (Tupla 4)

[ 5, 4, 3, 1]

[ 6, 3, 6, 1]

{39}------------------------------------------------

# k-means: Algoritmo de agrupamento particional

- Dinâmica:** Execute 1 iteração e determine o centróide, considerando que as tuplas 2 e 4 foram escolhidas como centróides:

Manhattan:  $d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$

**Recalculando os centróides:**

Centroide 1 (C1) = [ 1, 0, 1, 2 ] (Tupla 2)

[1, 0, 1, 2]

[2, 1, 0, 2]

[3, 4, 2, 3]

[3, 3, 1, 3]

$[(1+2+3+3)/4, (0+1+4+3)/4, (1+0+2+1)/4, (3+3+1+3)/4] =$

$[9/4, 8/4, 4/4, 10/4] = [2.25, 2, 1, 2.5]$

Centroide 2 (C2) = [6, 3, 6, 1] (Tupla 4)

[5, 4, 3, 1]

[6, 3, 6, 1]

|   | Atributo 1 | Atributo 2 | Atributo 3 | Atributo 4 |
|---|------------|------------|------------|------------|
| 1 | 5          | 4          | 3          | 1          |
| 2 | 1          | 0          | 1          | 2          |
| 3 | 2          | 1          | 0          | 2          |
| 4 | 6          | 3          | 6          | 1          |
| 5 | 3          | 4          | 2          | 3          |
| 6 | 3          | 3          | 1          | 3          |

<!-- DATALAB_CHUNK 3: pages 41-53 -->

{40}------------------------------------------------
## k-means: Algoritmo de agrupamento particional

- Dinâmica:** Execute 1 iteração e determine o centróide, considerando que as tuplas 2 e 4 foram escolhidas como centróides:

Manhattan:  $d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$

**Recalculando os centróides:**

|   | Atributo 1 | Atributo 2 | Atributo 3 | Atributo 4 |
|---|------------|------------|------------|------------|
| 1 | 5          | 4          | 3          | 1          |
| 2 | 1          | 0          | 1          | 2          |
| 3 | 2          | 1          | 0          | 2          |
| 4 | 6          | 3          | 6          | 1          |
| 5 | 3          | 4          | 2          | 3          |
| 6 | 3          | 3          | 1          | 3          |

Centroide 1 (C1) = ~~{1, 0, 1, 2} (Tupla 2)~~ [2.25, 2, 1, 2.5 ]

[1, 0, 1, 2]

[2, 1, 0, 2]

[3, 4, 2, 3]

[3, 3, 1, 3]

Centroide 2 (C2) = [6, 3, 6, 1] (Tupla 4)

[5, 4, 3, 1]

[6, 3, 6, 1]

$$[(5+6)/2, (4+3)/2, (3+6)/2, (1+1)/2] = [11/2, 7/2, 9/2, 2/2] \\ = [5.5, 3.5, 4.5, 1]$$

{41}------------------------------------------------
## k-means: Algoritmo de agrupamento particional

- Dinâmica:** Execute 1 iteração e determine o centróide, considerando que as tuplas 2 e 4 foram escolhidas como centróides:

Manhattan:  $d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$

**Recalculando os centróides:**

Centroide 1 (C1) = ~~{1, 0, 1, 2} (Tupla 2)~~ [2.25, 2, 1, 2.5 ]

[1, 0, 1, 2]

[2, 1, 0, 2]

[3, 4, 2, 3]

[3, 3, 1, 3]

Centroide 2 (C2) = ~~{6, 3, 6, 1} (Tupla 4)~~ [5.5, 3.5, 4.5, 1]

[5, 4, 3, 1]

[6, 3, 6, 1]

|   | Atributo 1 | Atributo 2 | Atributo 3 | Atributo 4 |
|---|------------|------------|------------|------------|
| 1 | 5          | 4          | 3          | 1          |
| 2 | 1          | 0          | 1          | 2          |
| 3 | 2          | 1          | 0          | 2          |
| 4 | 6          | 3          | 6          | 1          |
| 5 | 3          | 4          | 2          | 3          |
| 6 | 3          | 3          | 1          | 3          |

{42}------------------------------------------------
## K-Means
### `sklearn.cluster.KMeans`

```
class sklearn.cluster.KMeans(n_clusters=8, *, init='k-means++', n_init='warn', max_iter=300, tol=0.0001, verbose=0, random_state=None, copy_x=True, algorithm='lloyd')
```

[\[source\]](#)

- **n\_clusters** : numero de grupos, padrao=8
- **init**{'k-means++', 'random'}: metodo de inicializacao dos centroides: k-means++ (padrao) faz a escolha baseado em distribuicao.
- **n\_init** 'auto' ou int, padrão = 10 : Número de vezes que o algoritmo k-means é executado com sementes para centróides diferentes.
- **max\_iter** int, padrão=300 : Número máximo de iterações do algoritmo k-means para uma única execução.

{43}------------------------------------------------
## K-Means
### `sklearn.cluster.KMeans`

```
class sklearn.cluster.KMeans(n_clusters=8, *, init='k-means++', n_init='warn', max_iter=300, tol=0.0001, verbose=0, random_state=None, copy_x=True, algorithm='lloyd')
```

[\[source\]](#)

- **tolfloat**, padrão = 1e-4 : Tolerância relativa em relação à norma de Frobenius da diferença nos centros do cluster de duas iterações consecutivas para declarar convergência.
- **algorithm**{"lloyd", "elkan"}, default="lloyd". O algoritmo clássico do estilo EM é "lloyd". A variação "elkan" pode ser mais eficiente em alguns conjuntos de dados com clusters bem definidos. No entanto, consome mais memória devido à alocação de uma matriz extra de forma (n\_samples, n\_clusters).

{44}------------------------------------------------
## K-Means

```
# Executando o k-Means para cada valor de k
kmeanModel = KMeans(n_clusters=k,n_init='auto')
kmeanModel.fit(X)
```

X contém os dados de entrada

{45}------------------------------------------------

A network graph with nodes represented by colored pushpins (red, green, white, yellow, blue) connected by a web of black lines, illustrating a complex network structure.

A network graph with nodes represented by colored pushpins (red, green, white, yellow, blue) connected by a web of black lines, illustrating a complex network structure.

Como determinar a  
quantidade de clusters?  
Qual o melhor  $k$ ?

{46}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-dda713db72e22e546d6192afe545bbe0_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A network graph with nodes represented by colored pushpins (red, green, white, yellow, blue) connected by a web of black lines, illustrating a complex network structure.
<!-- /IMAGE_DESCRIPTION -->
### K-Means e o método Elbow

- O método elbow é conhecido como método do cotovelo. Basicamente o que o método faz é **testar a variância dos dados em relação os centroides dos clusters**.
- Neste método, para determinar o valor  $k$ ,
  - Iteramos continuamente de  $k = 1$  a  $k = n$  (aqui  $n$  é o hiperparâmetro que escolhemos de acordo com nossos requisitos).
  - Para cada valor de  $k$ , calculamos o valor da soma dos quadrados dentro do cluster (WCSS).
    - WCSS – Mede a coesão. É a soma das distâncias quadradas entre o centróide e cada objeto do cluster.

{47}------------------------------------------------
### K-Means e o método Elbow

No sklearn, usamos a **Distortion** e **Inertia** para medir a relação intracluster e extracluster.

- **Distorção:** É calculada como a média das distâncias quadradas dos centroides até cada objeto do cluster. Normalmente, usa como métrica a distância euclidiana.

```
Distortion = 1/n * $\Sigma$(distance(point, centroid)^2)
```

{48}------------------------------------------------
### K-Means e o método Elbow

- Inércia: É a soma das distâncias quadradas das amostras ao centro do cluster mais próximo.

```
Inertia =  $\sum(\text{distance}(\text{point}, \text{centroid})^2)$ 
```

- Para determinar o número ideal de clusters, temos que selecionar o valor de k no “cotovelo”, ou seja, o ponto após o qual a distorção/inércia começa a diminuir de forma linear.

{49}------------------------------------------------
### K-Means e o método Elbow

- Exemplo:

Dataset de Pontos

A scatter plot titled "Dataset de Pontos" showing a dataset of points. The plot has a white background with a black border. The x-axis and y-axis both range from -10.0 to 10.0, with major tick marks every 2.5 units. The data points are represented by blue dots and are clustered into four distinct groups. The top-left cluster is centered around (-4, 5) and contains 6 points. The top-right cluster is centered around (4, 5) and contains 6 points. The bottom-left cluster is centered around (-5, -5) and contains 3 points. The bottom-right cluster is centered around (5, -5) and contains 6 points. The overall distribution suggests a dataset with four well-separated clusters, making it a good candidate for K-Means clustering with K=4.

| Cluster | X    | Y    |
|---------|------|------|
| 1       | -6.0 | 4.0  |
| 1       | -5.0 | 4.0  |
| 1       | -4.0 | 4.0  |
| 1       | -4.0 | 7.0  |
| 1       | -4.0 | 6.0  |
| 1       | -4.0 | 4.0  |
| 2       | 2.0  | 7.0  |
| 2       | 3.0  | 6.0  |
| 2       | 4.0  | 5.0  |
| 2       | 3.0  | 4.0  |
| 2       | 3.0  | 3.0  |
| 2       | 3.0  | 4.0  |
| 3       | -6.0 | -4.0 |
| 3       | -5.0 | -5.0 |
| 3       | -4.0 | -4.0 |
| 4       | 2.0  | -5.0 |
| 4       | 3.0  | -5.0 |
| 4       | 4.0  | -4.0 |
| 4       | 5.0  | -3.0 |
| 4       | 5.0  | -5.0 |
| 4       | 5.0  | -6.0 |

Scatter plot showing a dataset of points with four distinct clusters, suitable for K-Means clustering.

{50}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-7e2465b81aed11b2e58575a811424b75_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Scatter plot showing a dataset of points with four distinct clusters, suitable for K-Means clustering.
<!-- /IMAGE_DESCRIPTION -->
### K-Means e o método Elbow

- Exemplo:

Metodo do cotovelo usando Distorcao

| Valores de K | Distorcao |
|--------------|-----------|
| 2            | 3.8       |
| 3            | 2.3       |
| 4            | 1.4       |
| 5            | 1.2       |
| 6            | 1.0       |
| 7            | 0.8       |
| 8            | 0.7       |
| 9            | 0.6       |

Gráfico do método do cotovelo usando distorção. O eixo X mostra valores de K de 2 a 9. O eixo Y mostra a distorção, que diminui à medida que K aumenta. Há uma mudança acentuada entre K=3 e K=4, formando um 'cotovelo'.

Metodo do cotovelo usando a inercia

| Valores de K | Inercia |
|--------------|---------|
| 2            | 550     |
| 3            | 180     |
| 4            | 50      |
| 5            | 40      |
| 6            | 35      |
| 7            | 25      |
| 8            | 15      |
| 9            | 10      |

Gráfico do método do cotovelo usando inércia. O eixo X mostra valores de K de 2 a 9. O eixo Y mostra a inércia, que diminui à medida que K aumenta. Há uma mudança acentuada entre K=3 e K=4, formando um 'cotovelo'.

Dataset de Pontos

| Cluster            | Centro Aproximado (X, Y) |
|--------------------|--------------------------|
| 1 (Topo Esquerda)  | (-4.5, 5.5)              |
| 2 (Baixo Esquerda) | (-5.5, -4.5)             |
| 3 (Topo Direita)   | (3.5, 5.0)               |
| 4 (Baixo Direita)  | (4.5, -4.5)              |

Gráfico de dispersão do dataset de pontos. Os pontos estão agrupados em quatro clusters distintos: dois no lado esquerdo (um superior e um inferior) e dois no lado direito (um superior e um inferior).

Observando os gráficos, concluímos que o número ideal de clusters para os dados é 4.

{51}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-242fdee4611b447a4206005652ea3c19_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Gráfico do método do cotovelo usando distorção.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-2d62ff2bded0c21414a0f40fdf8fd537_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Gráfico do método do cotovelo usando inércia.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-6dda36bad0978e272ca0420b0902b73a_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Gráfico de dispersão do dataset de pontos.
<!-- /IMAGE_DESCRIPTION -->
### K-Means e o método Elbow

- Exemplo:

The figure consists of two side-by-side scatter plots, both titled "Dataset de Pontos". Both plots have x and y axes ranging from -10.0 to 10.0 with major ticks every 2.5 units.

The left plot shows a dataset of points without any clustering. The points are clustered into four distinct groups: a top-left group (around x=-4, y=5), a top-right group (around x=3, y=5), a bottom-left group (around x=-5, y=-5), and a bottom-right group (around x=4, y=-5).

The right plot shows the same dataset with 4 clusters identified. The clusters are color-coded: blue (top-left and top-right), green (bottom-left), red (bottom-right), and orange (a single point in the top-right cluster). Centroids are marked with colored dots: blue for the top clusters, green for the bottom-left, red for the bottom-right, and orange for the centroid of the top-right cluster.

Two scatter plots illustrating K-Means clustering. The left plot shows a dataset of points without clusters. The right plot shows the same dataset with 4 clusters identified by different colors (blue, green, red, orange) and centroids marked by colored dots.

Observando os gráficos, concluímos que o número ideal de clusters para os dados é 4.

{52}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-4666738057044ad78ced4dbbc0c1bfb3_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Two scatter plots illustrating K-Means clustering.
<!-- /IMAGE_DESCRIPTION -->
## Dinâmica

- Exemplos de uso do k-Means
