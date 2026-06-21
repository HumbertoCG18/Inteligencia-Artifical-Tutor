<!-- EXEC_SUMMARY_START -->
## Sumário
> *Leia antes de varrer o arquivo. Vá direto à seção relevante para a pergunta do aluno.*

- **Subáreas da Inteligência Artificial**
  - Aprendizado Não Supervisionado
  - Aprendizado Não Supervisionado
  - Agrupamento
  - Agrupamento
  - Agrupamento
- **Recalculando os centróides:**
- **Recalculando os centróides:**
- **k-means: Algoritmo de agrupamento particional**
- **K-Means**
  - `sklearn.cluster.KMeans`
  - K-Means
  - `sklearn.cluster.KMeans`
  - K-Means
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
##### Abstract background with orange and green splattersThe background of the slide is an abstract composition of numerous circular and irregular splatters. On the left side, there are large, overlapping splatters in shades of orange and brown. On the right side, there are large, overlapping splatters in shades of green and yellow. The overall effect is a vibrant, artistic splash of colors against a light, gradient background that transitions from blue on the left to white in the center and then to a light orange on the right.Aprendizado não supervisionado: parte 1

Profa Silvia Moraes

{1}------------------------------------------------
## Subáreas da Inteligência Artificial

The diagram illustrates the subfields of Artificial Intelligence (IA) centered around a hub labeled "Inteligência Artificial (IA)". The subfields are categorized into several groups:

- Aprendizado de Máquina (Machine Learning)** (highlighted in red):
  - Aprendizado Profundo (Deep Learning)
  - Aprendizado Supervisionado
  - Aprendizado Não Supervisionado
  - Aprendizado por Reforço
  - Aprendizado auto-supervisionado
  - Aprendizado semissupervisionado
- Processamento de Linguagem Natural**:
  - Extração de Informações
  - Classificação de Texto
  - Tradução Automática
  - Perguntas e Respostas
  - Geração de Texto
- Raciocínio Automatizado**
- Robótica**
- IA Explicável**
- Visão Computacional**

Diagram showing subfields of Artificial Intelligence (IA) arranged around a central hub.

{2}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-9ba3dc91984c80b96f217fb1bddd5c06_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram showing subfields of Artificial Intelligence (IA) arranged around a central hub.
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

```
graph LR; A[Dataset Sem Anotação] --> B[Algoritmo de Machine Learning Supervisionado]; B --> C[Modelo];
```

The diagram illustrates the supervised learning process. It begins with a 'Dataset Sem Anotação' (Unlabeled Dataset) represented by a collage of various animal images (cats, dogs, chickens). An arrow points from this dataset to a box labeled 'Algoritmo de Machine Learning Supervisionado' (Supervised Machine Learning Algorithm). Below this box is a smaller box labeled 'Treinamento' (Training), which contains a diagram of a neural network. A second arrow points from the 'Algoritmo' box to a final box labeled 'Modelo' (Model), which also contains a neural network diagram.

A collage of various animal images including cats, dogs, and chickens, representing an unlabeled dataset. Diagram of a neural network structure with orange, purple, and grey nodes. Diagram of a neural network structure with orange, purple, and grey nodes.

{3}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-7055f51feb10ea4ea48b27c36f085286_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A collage of various animal images including cats, dogs, and chickens, representing an unlabeled dataset.
<!-- /IMAGE_DESCRIPTION -->
### Aprendizado Não Supervisionado

Executa **tarefas descritivas**: explora ou descreve um conjunto de dados.

- **Agrupamento**: divisão em grupos baseada em alguma regularidade ou similaridade
- **Sumarização**: descrição simples e compacta
- **Associação**: relações frequentes entre dados

A close-up photograph of several apples, showing a mix of red, yellow, and green colors, illustrating the concept of data distribution or clustering.

A close-up photograph of several apples, showing a mix of red, yellow, and green colors, illustrating the concept of data distribution or clustering.

A photograph of many small, identical stuffed monkeys, some purple and some yellow, arranged in rows, illustrating the concept of data similarity or grouping.

A photograph of many small, identical stuffed monkeys, some purple and some yellow, arranged in rows, illustrating the concept of data similarity or grouping.

{4}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-16d86083b7ebdc40c0647a1d3d46ace7_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A close-up photograph of several apples, showing a mix of red, yellow, and green colors, illustrating the concept of data distribution or clustering.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-b615ff07e8a0f467f0a6f4783c4463eb_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A photograph of many small, identical stuffed monkeys, some purple and some yellow, arranged in rows, illustrating the concept of data similarity or grouping.
<!-- /IMAGE_DESCRIPTION -->
### Agrupamento

Organiza dados (não classificados, sem rótulos) em grupos de acordo com alguma medida de similaridade.

**Entrada (x):**  
Imagem ou características

<https://www.pexels.com/>

**Dataset Sem Anotação**

→

**Algoritmo de Machine Learning Supervisionado**

**Generalização**

**Modelo**

→

**Grupos**

```
graph LR; A[Entrada (x): Imagem ou características  
https://www.pexels.com/  
Dataset Sem Anotação] --> B[Algoritmo de Machine Learning Supervisionado  
Generalização  
Modelo]; B --> C((Grupos)); C --> D1((Cat Group)); C --> D2((Chicken Group)); C --> D3((Dog Group));
```

Diagram illustrating the clustering process. It starts with an 'Entrada (x): Imagem ou características' section showing a collage of various animal images (cats, dogs, chickens) with a URL 'https://www.pexels.com/'. This is labeled 'Dataset Sem Anotação'. An arrow points to a central box labeled 'Algoritmo de Machine Learning Supervisionado' and 'Generalização', which contains a neural network icon and the word 'Modelo'. Another arrow points from this box to three circular clusters labeled 'Grupos'. The top cluster contains four cat images. The middle cluster contains two chicken images. The bottom cluster contains three dog images.

{5}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-e394c2b5c61344f6a12397f430086072_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram illustrating the clustering process.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-997233d405f0d4b89ddeb7683e047f66_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Flowchart of the clustering process (Agrupamento).
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-d17f75945bbb3feb84a153ecfedb9b81_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram showing the clustering of text documents.
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
#### - **Etapas:**

- preparação,
- proximidade,
- agrupamento,
- validação e
- interpretação.

```
graph TD;
    Objetos[Objetos] --> Preparação[Preparação];
    Conhecimento[Conhecimento do usuário/especialista] -.-> Preparação;
    Conhecimento -.-> Proximidade[Proximidade];
    Preparação --> Proximidade;
    Preparação -- "Representação dos objetos" --> Agrupamento[Agrupamento];
    Proximidade -- "Medida de similaridade" --> Agrupamento;
    Agrupamento --> Validação[Validação];
    Conhecimento -.-> Agrupamento;
    Conhecimento -.-> Validação;
    Validação --> Interpretação[Interpretação];
    Conhecimento -.-> Interpretação;
    Validação --> ClustersValidados[Clusters validados];
    Interpretação --> Significados[Significados dos clusters];
```

The diagram illustrates the clustering process (Agrupamento) as a sequence of steps within a larger process box, influenced by external knowledge and feedback loops.

- Objetos** (Objects) feed into **Preparação** (Preparation).
- Conhecimento do usuário/especialista** (User/Expert Knowledge) provides input to **Preparação**, **Proximidade** (Proximity), **Agrupamento**, **Validação** (Validation), and **Interpretação** (Interpretation).
- Preparação** and **Proximidade** are interconnected, with **Preparação** leading to **Proximidade** and vice versa.
- Preparação** outputs **Representação dos objetos** (Object representation) to **Agrupamento**.
- Proximidade** outputs **Medida de similaridade** (Similarity measure) to **Agrupamento**.
- Agrupamento** leads to **Validação**, which then leads to **Interpretação**.
- Validação** outputs **Clusters validados** (Validated clusters).
- Interpretação** outputs **Significados dos clusters** (Cluster meanings).

Flowchart of the clustering process (Agrupamento).

{7}------------------------------------------------
#### Agrupamento
#### Etapas:

- **Preparação:** inclui pré-processamento (ex: normalizações, conversão de tipos e redução de dimensionalidade) e forma de representação dos dados (ex: matriz de similaridade) para que o algoritmo de agrupamento possa ser usado.
- **Proximidade:** definição de medidas de proximidade apropriadas ao domínio e ao tipo de informação que se deseja extrair dos dados. Existem medidas para atributos quantitativos e qualitativos.

{8}------------------------------------------------
#### Agrupamento
##### Etapas: ...

- **Proximidade:** Medidas para atributos quantitativos e qualitativos.
  - Medidas de Distância: atributos contínuos e racionais:

- Manhattan:  $d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$  (usual para binários)

- Euclidiana:  $d(x_i, x_j) = \sqrt{\sum_{l=1}^d (x_i^l - x_j^l)^2}$

- Chebyshev (ou supremum):  $d(x_i, x_j) = \max_{1 \leq l \leq d} |x_i^l - x_j^l|$

The diagram shows a 2D coordinate system with a grid. Two points,  $x_i$  and  $x_j$ , are plotted. Three distances are illustrated:

- Distância de Manhattan:** Represented by a dashed line that moves horizontally and vertically between the two points, following the grid lines.
- Distância euclidiana:** Represented by a solid straight line connecting the two points directly.
- Distância de Chebyshev:** Represented by a dashed line that moves horizontally and vertically, but only the maximum of the horizontal and vertical distances is shown, representing the maximum coordinate difference.

Diagram illustrating three distance metrics between two points x\_i and x\_j on a grid.

{9}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-0f3e3ea50bcceb86f6c524ab2b6f3e7a_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram illustrating three distance metrics between two points x_i and x_j on a grid.
<!-- /IMAGE_DESCRIPTION -->
#### Agrupamento
##### Etapas: ...
##### - **Proximidade:** Medidas para Atributos Quantitativos:

- Medidas de Similaridade:

- Separação angular (cosseno):  $\cos(x_i, x_j) = \frac{\sum_{l=1}^d x_i^l x_j^l}{\sqrt{\sum_{l=1}^d x_i^l{}^2 \sum_{l=1}^d x_j^l{}^2}}$

- Pearson:  $\rho(x_i, x_j) = \frac{\sum_{l=1}^d (x_i^l - \bar{x}_i)(x_j^l - \bar{x}_j)}{\sqrt{\sum_{l=1}^d (x_i^l - \bar{x}_i)^2 \sum_{l=1}^d (x_j^l - \bar{x}_j)^2}}$  (quando magnitude

não é importante, mas sim o grau de variação. Ex: Bioinformática)

Diagrama de um plano cartesiano com eixos x e y. Duas setas, x\_i e x\_j, partem da origem. O ângulo entre elas é rotulado 'cosseno'. Duas outras setas, x\_i' e x\_j', também partem da origem, com o ângulo entre elas rotulado 'Pearson'.

{10}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-7c2f0efb2c5d10a52ce19ba33d9d3cec_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de um plano cartesiano com eixos x e y.
<!-- /IMAGE_DESCRIPTION -->
#### Agrupamento
##### Etapas: ...

- **Proximidade:** Medidas para Atributos Qualitativos:
  - São obtidas a partir da soma das contribuições individuais de todos os atributos.
  - Para atributos nominais, a distância mais usada é a de Hamming.

$$d(x_i, x_j) = \sum_{l=1}^d a(x_i^l, x_j^l) , \text{ onde } a(x_i^l, x_j^l) = \begin{cases} 1 & \text{se } x_i^l \neq x_j^l \\ 0 & \text{c.c} \end{cases}$$

{11}------------------------------------------------
#### Agrupamento
##### Etapas: ...

- **agrupamento:** nessa etapa um ou mais algoritmos de agrupamento são usados para gerar os grupos.
- **validação:** etapa que verifica se os grupos gerados são significativos. Ajuda a determinar o número adequado de
- **grupos:** quando esse número não é conhecido.
- **interpretação:** processo de examinar o grupo em relação aos outros com o objetivo de rotulá-lo, indicando a natureza do grupo.

{12}------------------------------------------------
#### Agrupamento
#### Tipos:

The diagram illustrates two types of clustering. On the left, a vertical line separates two examples of partitional clustering. The left side shows three disjoint groups: a group of four blue dots, a group of three yellow dots, and a group of four red dots. The right side shows two groups of green dots, each enclosed in a circle, which are themselves enclosed in a larger circle. On the right, a 2D plot shows a large gray circle containing two smaller, non-overlapping circles: a blue one labeled 'A' and a yellow one labeled 'F'. A red line connects the centers of these two circles. Below the plot is a dendrogram showing the hierarchical merging of six points labeled A, B, C, D, E, and F. The dendrogram shows a red line connecting A and B, and another red line connecting D and E. These two pairs are then merged into a larger group, which is finally merged with C and F. The labels A, B, C, D, E, and F are listed at the bottom of the dendrogram.

Diagram illustrating two types of clustering: Partitional and Hierarchical.

- **Agrupamento Particional:** Divisão dos objetos de dados em subconjuntos (grupos) sem sobreposição tal que cada objeto de dados está em exatamente um único grupo.
- **Agrupamento Hierárquico:** Um conjunto de grupos aninhados na forma de uma árvore hierárquica.

{13}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-eefe19c5e14dc4d6c316b7f7fbb7d7d7_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram illustrating two types of clustering: Partitional and Hierarchical.
<!-- /IMAGE_DESCRIPTION -->
##### Exemplos de Agrupamento Particional

**Agrupamento produtos**  
de acordo com as suas  
características.

Diagram showing the clustering of potatoes. A large pile of multi-colored potatoes is shown on the left. A green arrow points to three separate piles on the right, each containing potatoes of a single color: red, yellow, and purple.

**Agrupamento de clientes**  
Identificação de perfil para  
recomendação de  
produtos

Diagram showing the clustering of customers. On the left, a group of stylized human icons in blue and green are shown. An orange arrow points to the right, where the icons are organized into two distinct groups: one with all blue icons and another with all green icons.

**Agrupamento de dados similares**

| sepal length | sepal width | petal length | petal width |
|--------------|-------------|--------------|-------------|
| 5,1          | 3,5         | 1,4          | 0,2         |
| 4,9          | 3,0         | 1,4          | 0,2         |
| 7,0          | 3,2         | 4,7          | 7,1         |
| 6,4          | 3,2         | 4,5          | 1,5         |
| 6,3          | 3,3         | 6,0          | 2,5         |
| 5,8          | 2,7         | 5,1          | 1,9         |

A red arrow pointing from the table of data to the grouped clusters.

**Grupo 1**

|     |     |     |     |
|-----|-----|-----|-----|
| 5,1 | 3,5 | 1,4 | 0,2 |
| 4,9 | 3,0 | 1,4 | 0,2 |

**Grupo 2**

|     |     |     |     |
|-----|-----|-----|-----|
| 7,0 | 3,2 | 4,7 | 7,1 |
| 6,4 | 3,2 | 4,5 | 1,5 |

**Grupo 3**

|     |     |     |     |
|-----|-----|-----|-----|
| 6,3 | 3,3 | 6,0 | 2,5 |
| 5,8 | 2,7 | 5,1 | 1,9 |

Diagram showing three groups of data points (flowers) clustered together. Grupo 1 and Grupo 3 are in the foreground, while Grupo 2 is in the background. Each group contains a small table of data.

**Agrupamento  
de textos**

Diagram showing the clustering of text documents. On the left, a stack of documents in blue and yellow is shown. An arrow points to the right, where the documents are organized into two distinct groups: one with all yellow documents and another with all blue documents.

{14}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-4ee27dbf5ef12e7b58b0ef0937bc5a5e_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram showing the clustering of potatoes.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-bd671b21db63e6fdb2196e9b18502aac_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram showing the clustering of customers.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-159f15d60777adb6b16c91d84b32c32f_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A red arrow pointing from the table of data to the grouped clusters.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-f6e8acf9f931452d01688d311b5c0364_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram showing three groups of data points (flowers) clustered together.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-0928cdf6e30b6fef3f510d120adeb39d_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Red arrow pointing to the first column of the table
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-6b410420a4a85fdcd8cce973d3ec037a_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Red arrow pointing to the first column of the table
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-3558a64b4f3d03eb8da8e584c606af39_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A red arrow points to the first column of the table, specifically to the row index 3.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-943b5c4cef256d8e4b32442bab86697f_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Red arrow pointing to Tupla 4 in the table.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-2f98f75750e637aa0f280dbe3d95de6d_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Red arrow pointing to the first column of the table.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-f26317fb2eba3b087764545f1880b42c_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Red arrow pointing right
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-0f4ae20874db623ff48a27215649ce03_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A blue arrow pointing from the text 'X contém os dados de entrada' to the variable 'X' in the code snippet above.
<!-- /IMAGE_DESCRIPTION -->
##### Agrupamento Particional

Icon representing unlabeled data, shown as three yellow cylinders.

Dados não rotulados

| sepal length | sepal width | petal length | petal width |
|--------------|-------------|--------------|-------------|
| 5,1          | 3,5         | 1,4          | 0,2         |
| 4,9          | 3,0         | 1,4          | 0,2         |
| 7,0          | 3,2         | 4,7          | 7,1         |
| 6,4          | 3,2         | 4,5          | 1,5         |
| 6,3          | 3,3         | 6,0          | 2,5         |
| 5,8          | 2,7         | 5,1          | 1,9         |

Algoritmo de  
Machine Learning

Resultados

Algoritmo  
k-Means

Tarefa: agrupamento  
(clustering)

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
> **[Descrição de imagem]** Icon representing unlabeled data, shown as three yellow cylinders.
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
    - $i$  = número de iterações e
    - $d$  = número de atributos

{17}------------------------------------------------
##### k-means: Algoritmo de agrupamento particional

- **k-means:** Algoritmo de agrupamento particional.
  1. Selecione k objetos como centroides;
  2. Repita
    1. Calcule a distância de cada objeto em relação ao centroide de cada cluster k
    2. O objeto será atribuído ao cluster k cujo centroide está mais próximo
    3. Depois de processar todos os dados, recalcule os centroides, considerando os dados em cada cluster k.
  3. Até que os centroides não mudem mais

{18}------------------------------------------------
##### k-means: Algoritmo de agrupamento particional

- k-means: Algoritmo de agrupamento particional. Exemplo:

| Padrão | Peso(Atributo1) | Altura(Atributo2) |
|--------|-----------------|-------------------|
| 1      | 2               | 8                 |
| 2      | 8               | 2                 |
| 3      | 6               | 8                 |
| 4      | 2               | 7                 |
| 5      | 8               | 4                 |
| 6      | 2               | 6                 |

Manhattan: 
$$d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$$

{19}------------------------------------------------
##### k-means: Algoritmo de agrupamento particional

- k-means: Algoritmo de agrupamento particional. Exemplo:

| Padrão | Peso(Atributo1) | Altura(Atributo2) |
|--------|-----------------|-------------------|
| 1      | 2               | 8                 |
| 2      | 8               | 2                 |
| 3      | 6               | 8                 |
| 4      | 2               | 7                 |
| 5      | 8               | 4                 |
| 6      | 2               | 6                 |

Manhattan: 
$$d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$$
##### Cluster 1

Centroide: (2) [8,2]

Tuplas:
##### Cluster 2

Centroide: (6) [2,6]

Tuplas:

<!-- DATALAB_CHUNK 2: pages 21-40 -->

{20}------------------------------------------------

# k-means: Algoritmo de agrupamento particional

- k-means: Algoritmo de agrupamento particional. Exemplo:

| Padrão | Peso(Atributo1) | Altura(Atributo2) |
|--------|-----------------|-------------------|
| 1      | 2               | 8                 |
| 2      | 8               | 2                 |
| 3      | 6               | 8                 |
| 4      | 2               | 7                 |
| 5      | 8               | 4                 |
| 6      | 2               | 6                 |

Manhattan: 
$$d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$$
#### Cluster 1

Centroide: (2) [8,2]

Tuplas:
#### Cluster 2

Centroide: (6) [2,6]

Tuplas:

**Tupla: (1) [2,8]**

**Dist(C1,T1)= |8-2|+|2-8|=12**

**Dist(C2,T1) = |2-2| + |6-8|=2**

{21}------------------------------------------------

# k-means: Algoritmo de agrupamento particional

- k-means: Algoritmo de agrupamento particional. Exemplo:

| Padrão | Peso(Atributo1) | Altura(Atributo2) |
|--------|-----------------|-------------------|
| 1      | 2               | 8                 |
| 2      | 8               | 2                 |
| 3      | 6               | 8                 |
| 4      | 2               | 7                 |
| 5      | 8               | 4                 |
| 6      | 2               | 6                 |

Manhattan: 
$$d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$$
#### Cluster 1

Centroide: (2) [8,2]

Tuplas:
#### Cluster 2

Centroide: (6) [2,6]

Tuplas: [2,8]

**Tupla: (1) [2,8]**

**Dist(C1,T1)= |8-2| + |2-8|=12**

**Dist(C2,T1) = |2-2| + |6-8|=2**

{22}------------------------------------------------

# k-means: Algoritmo de agrupamento particional

- k-means: Algoritmo de agrupamento particional. Exemplo:

| Padrão | Peso(Atributo1) | Altura(Atributo2) |
|--------|-----------------|-------------------|
| 1      | 2               | 8                 |
| 2      | 8               | 2                 |
| 3      | 6               | 8                 |
| 4      | 2               | 7                 |
| 5      | 8               | 4                 |
| 6      | 2               | 6                 |

Manhattan: 
$$d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$$
#### Cluster 1

Centroide: (2) [8,2]

Tuplas: [8,2]
#### Cluster 2

Centroide: (6) [2,6]

Tuplas: [2,8]

**Tupla: (2) [8,2]**

Dist(C1,T2)=  $|8-8| + |2-2|=0$

Dist(C2,T2) =  $|2-8| + |6-2|=10$

{23}------------------------------------------------

# k-means: Algoritmo de agrupamento particional

- k-means: Algoritmo de agrupamento particional. Exemplo:

| Padrão | Peso(Atributo1) | Altura(Atributo2) |
|--------|-----------------|-------------------|
| 1      | 2               | 8                 |
| 2      | 8               | 2                 |
| 3      | 6               | 8                 |
| 4      | 2               | 7                 |
| 5      | 8               | 4                 |
| 6      | 2               | 6                 |

Manhattan: 
$$d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$$
#### Cluster 1

Centroide: (2) [8,2]

Tuplas: [8,2]
#### Cluster 2

Centroide: (6) [2,6]

Tuplas: [2,8] [6,8]

**Tupla: (3) [6,8]**

**Dist(C1,T3)= |8-6| + |2-8|=8**

**Dist(C2,T3) = |2-6| + |6-8|=6**

{24}------------------------------------------------

# k-means: Algoritmo de agrupamento particional

- k-means: Algoritmo de agrupamento particional. Exemplo:

| Padrão | Peso(Atributo1) | Altura(Atributo2) |
|--------|-----------------|-------------------|
| 1      | 2               | 8                 |
| 2      | 8               | 2                 |
| 3      | 6               | 8                 |
| 4      | 2               | 7                 |
| 5      | 8               | 4                 |
| 6      | 2               | 6                 |

Manhattan: 
$$d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$$
#### Cluster 1

Centroide: (2) [8,2]

Tuplas: [8,2]
#### Cluster 2

Centroide: (6) [2,6]

Tuplas: [2,8] [6,8] [2,7]

**Tupla: (4) [2,7]**

**Dist(C1,T4)= |8-2| + |2-7|=11**

**Dist(C2,T4) = |2-2| + |6-7|=1**

{25}------------------------------------------------

# k-means: Algoritmo de agrupamento particional

- k-means: Algoritmo de agrupamento particional. Exemplo:

| Padrão | Peso(Atributo1) | Altura(Atributo2) |
|--------|-----------------|-------------------|
| 1      | 2               | 8                 |
| 2      | 8               | 2                 |
| 3      | 6               | 8                 |
| 4      | 2               | 7                 |
| 5      | 8               | 4                 |
| 6      | 2               | 6                 |

Manhattan: 
$$d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$$
#### Cluster 1

Centroide: (2) [8,2]

Tuplas: [8,2], [8,4]
#### Cluster 2

Centroide: (6) [2,6]

Tuplas: [2,8] [6,8] [2,7]

**Tupla: (5) [8,4]**

**Dist(C1,T5)= |8-8|+|2-4|=2**

**Dist(C2,T5) = |2-8| + |6-4|=8**

{26}------------------------------------------------

# k-means: Algoritmo de agrupamento particional

- k-means: Algoritmo de agrupamento particional. Exemplo:

| Padrão | Peso(Atributo1) | Altura(Atributo2) |
|--------|-----------------|-------------------|
| 1      | 2               | 8                 |
| 2      | 8               | 2                 |
| 3      | 6               | 8                 |
| 4      | 2               | 7                 |
| 5      | 8               | 4                 |
| 6      | 2               | 6                 |

Manhattan: 
$$d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$$
#### Cluster 1

Centroide: (2) [8,2]

Tuplas: [8,2], [8,4]
#### Cluster 2

Centroide: (6) [2,6]

Tuplas: [2,8] [6,8] [2,7] [2,6]

**Tupla: (6) [2,6]**

**Dist(C1,T6)= |8-2| + |2-6|=10**

**Dist(C2,T6) = |2-2| + |6-6|=0**

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

Manhattan: 
$$d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$$
#### Cluster 1

Centroide: ~~(2) [8,2]~~ [8,3]

Tuplas: [8,2], [8,4]
#### Cluster 2

Centroide: (6) [2,6]

Tuplas: [2,8] [6,8] [2,7] [2,6]

Recalculando os centroides:

Cluster1:

$[(8+8)/2, (2+4)/2] = [8,3]$

{28}------------------------------------------------

# k-means: Algoritmo de agrupamento particional

- k-means: Algoritmo de agrupamento particional. Exemplo:

| Padrão | Peso(Atributo1) | Altura(Atributo2) |
|--------|-----------------|-------------------|
| 1      | 2               | 8                 |
| 2      | 8               | 2                 |
| 3      | 6               | 8                 |
| 4      | 2               | 7                 |
| 5      | 8               | 4                 |
| 6      | 2               | 6                 |

Manhattan: 
$$d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$$
#### Cluster 1

Centroide: ~~(2) [8, 2]~~ [8, 3]

Tuplas: [8, 2], [8, 4]
#### Cluster 2

Centroide: ~~(6) [2, 6]~~ [3, 7.25]

Tuplas: [2, 8] [6, 8] [2, 7] [2, 6]

Recalculando os centroides:

Cluster2:

$$[(2+6+2+2)/4, (8+8+7+6)/4] = [3, 7.25]$$

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

- **Dinâmica:** Execute 1 iteração e determine o centróide, considerando que as tuplas 2 e 4 foram escolhidas como centróides:

Manhattan: 
$$d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$$

|   | Atributo 1 | Atributo 2 | Atributo 3 | Atributo 4 |
|---|------------|------------|------------|------------|
| 1 | 5          | 4          | 3          | 1          |
| 2 | 1          | 0          | 1          | 2          |
| 3 | 2          | 1          | 0          | 2          |
| 4 | 6          | 3          | 6          | 1          |
| 5 | 3          | 4          | 2          | 3          |
| 6 | 3          | 3          | 1          | 3          |

Centroide 1 (C1) = [ 1, 0, 1, 2 ] (Tupla 2)

Centroide 2 (C2) = [6, 3, 6, 1 ] (Tupla 4)

{31}------------------------------------------------

# k-means: Algoritmo de agrupamento particional

- **Dinâmica:** Execute 1 iteração e determine o centróide, considerando que as tuplas 2 e 4 foram escolhidas como centróides:

Manhattan: 
$$d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$$

|   | Atributo 1 | Atributo 2 | Atributo 3 | Atributo 4 |
|---|------------|------------|------------|------------|
| 1 | 5          | 4          | 3          | 1          |
| 2 | 1          | 0          | 1          | 2          |
| 3 | 2          | 1          | 0          | 2          |
| 4 | 6          | 3          | 6          | 1          |
| 5 | 3          | 4          | 2          | 3          |
| 6 | 3          | 3          | 1          | 3          |

Centroide 1 (C1) = [ 1, 0, 1, 2 ] (Tupla 2)

- $\text{Dist}(C1, \text{Tupla1}) = |1-5| + |0-4| + |1-3| + |2-1| = 11$
- $\text{Dist}(C1, \text{Tupla2}) = 0$
- $\text{Dist}(C1, \text{Tupla3}) = |1-2| + |0-1| + |1-0| + |2-2| = 3$
- $\text{Dist}(C1, \text{Tupla4}) = |1-6| + |0-3| + |1-6| + |2-1| = 14$
- $\text{Dist}(C1, \text{Tupla5}) = |1-3| + |0-4| + |1-2| + |2-3| = 8$
- $\text{Dist}(C1, \text{Tupla6}) = |1-3| + |0-3| + |1-1| + |2-3| = 6$

Centroide 2 (C2) = [ 6, 3, 6, 1 ] (Tupla 4)

- $\text{Dist}(C2, \text{Tupla1}) = |6-5| + |3-4| + |6-3| + |1-1| = 5$
- $\text{Dist}(C2, \text{Tupla2}) = |6-1| + |3-0| + |6-1| + |1-2| = 14$
- $\text{Dist}(C2, \text{Tupla3}) = |6-2| + |3-1| + |6-0| + |1-2| = 13$
- $\text{Dist}(C2, \text{Tupla4}) = 0$
- $\text{Dist}(C2, \text{Tupla5}) = |6-3| + |3-4| + |6-2| + |1-3| = 10$
- $\text{Dist}(C2, \text{Tupla6}) = |6-3| + |3-3| + |6-1| + |1-3| = 10$

{32}------------------------------------------------

# k-means: Algoritmo de agrupamento particional

- **Dinâmica:** Execute 1 iteração e determine o centróide, considerando que as tuplas 2 e 4 foram escolhidas como centróides:

Manhattan: 
$$d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$$

|   | Atributo 1 | Atributo 2 | Atributo 3 | Atributo 4 |
|---|------------|------------|------------|------------|
| 1 | 5          | 4          | 3          | 1          |
| 2 | 1          | 0          | 1          | 2          |
| 3 | 2          | 1          | 0          | 2          |
| 4 | 6          | 3          | 6          | 1          |
| 5 | 3          | 4          | 2          | 3          |
| 6 | 3          | 3          | 1          | 3          |

**Centroide 1 (C1) = [ 1, 0, 1, 2 ] (Tupla 2)**

- $\text{Dist}(C1, \text{Tupla1}) = |1-5| + |0-4| + |1-3| + |2-1| = 11$
- $\text{Dist}(C1, \text{Tupla2}) = 0$
- $\text{Dist}(C1, \text{Tupla3}) = |1-2| + |0-1| + |1-0| + |2-2| = 3$
- $\text{Dist}(C1, \text{Tupla4}) = |1-6| + |0-3| + |1-6| + |2-1| = 14$
- $\text{Dist}(C1, \text{Tupla5}) = |1-3| + |0-4| + |1-2| + |2-3| = 8$
- $\text{Dist}(C1, \text{Tupla6}) = |1-3| + |0-3| + |1-1| + |2-3| = 6$

**Centroide 2 (C2) = [ 6, 3, 6, 1 ] (Tupla 4)**

- $\text{Dist}(C2, \text{Tupla1}) = |6-5| + |3-4| + |6-3| + |1-1| = 5$
- $\text{Dist}(C2, \text{Tupla2}) = |6-1| + |3-0| + |6-1| + |1-2| = 14$
- $\text{Dist}(C2, \text{Tupla3}) = |6-2| + |3-1| + |6-0| + |1-2| = 13$
- $\text{Dist}(C2, \text{Tupla4}) = 0$
- $\text{Dist}(C2, \text{Tupla5}) = |6-3| + |3-4| + |6-2| + |1-3| = 10$
- $\text{Dist}(C2, \text{Tupla6}) = |6-3| + |3-3| + |6-1| + |1-3| = 10$

{33}------------------------------------------------

# k-means: Algoritmo de agrupamento particional

- **Dinâmica:** Execute 1 iteração e determine o centróide, considerando que as tuplas 2 e 4 foram escolhidas como centróides:

Manhattan: 
$$d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$$

|   | Atributo 1 | Atributo 2 | Atributo 3 | Atributo 4 |
|---|------------|------------|------------|------------|
| 1 | 5          | 4          | 3          | 1          |
| 2 | 1          | 0          | 1          | 2          |
| 3 | 2          | 1          | 0          | 2          |
| 4 | 6          | 3          | 6          | 1          |
| 5 | 3          | 4          | 2          | 3          |
| 6 | 3          | 3          | 1          | 3          |

Centroide 1 (C1) = [ 1, 0, 1, 2 ] (Tupla 2)

- **Dist(C1, Tupla2) = 0**
- Dist(C1, Tupla3) = |1-2| + |0-1| + |1-0| + |2-2| = 3
- Dist(C1, Tupla4) = |1-6| + |0-3| + |1-6| + |2-1| = 14
- Dist(C1, Tupla5) = |1-3| + |0-4| + |1-2| + |2-3| = 8
- Dist(C1, Tupla 6) = |1-3| + |0-3| + |1-1| + |2-3| = 6

Centroide 2 (C2) = [ 6, 3, 6, 1 ] (Tupla 4)

- Dist(C2, Tupla2) = |6-1| + |3-0| + |6-1| + |1-2| = 14
- Dist(C2, Tupla3) = |6-2| + |3-1| + |6-0| + |1-2| = 13
- Dist(C2, Tupla4) = 0
- Dist(C2, Tupla5) = |6-3| + |3-4| + |6-2| + |1-3| = 10
- Dist(C2, Tupla 6) = |6-3| + |3-3| + |6-1| + |1-3| = 10

{34}------------------------------------------------

# k-means: Algoritmo de agrupamento particional

- **Dinâmica:** Execute 1 iteração e determine o centróide, considerando que as tuplas 2 e 4 foram escolhidas como centróides:

Manhattan: 
$$d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$$

|   | Atributo 1 | Atributo 2 | Atributo 3 | Atributo 4 |
|---|------------|------------|------------|------------|
| 1 | 5          | 4          | 3          | 1          |
| 2 | 1          | 0          | 1          | 2          |
| 3 | 2          | 1          | 0          | 2          |
| 4 | 6          | 3          | 6          | 1          |
| 5 | 3          | 4          | 2          | 3          |
| 6 | 3          | 3          | 1          | 3          |

Centroide 1 (C1) = [ 1, 0, 1, 2 ] (Tupla 2)  
[ 1, 0, 1, 2 ]

- **Dist(C1, Tupla3)** = |1-2|+|0-1|+|1-0|+|2-2|= 3
- Dist(C1, Tupla4) = |1-6|+|0-3|+|1-6|+|2-1|= 14
- Dist(C1, Tupla5) = |1-3|+|0-4|+|1-2|+|2-3|= 8
- Dist(C1, Tupla 6) = |1-3|+|0-3|+|1-1|+|2-3|= 6

Centroide 2 (C2) = [ 6, 3, 6, 1 ] (Tupla 4)  
[ 5, 4, 3, 1 ]

- Dist(C2, Tupla3) = |6-2|+|3-1|+|6-0|+|1-2|= 13
- Dist(C2, Tupla4) = 0
- Dist(C2, Tupla5) = |6-3|+|3-4|+|6-2|+|1-3|= 10
- Dist(C2, Tupla 6) = |6-3|+|3-3|+|6-1|+|1-3|= 10

{35}------------------------------------------------

# k-means: Algoritmo de agrupamento particional

- **Dinâmica:** Execute 1 iteração e determine o centróide, considerando que as tuplas 2 e 4 foram escolhidas como centróides:

Manhattan: 
$$d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$$

Centroide 1 (C1) = [ 1, 0, 1, 2 ] (Tupla 2)

[1, 0, 1, 2]

[2, 1, 0, 2]

- $\text{Dist}(C1, \text{Tupla4}) = |1-6| + |0-3| + |1-6| + |2-1| = 14$
- $\text{Dist}(C1, \text{Tupla5}) = |1-3| + |0-4| + |1-2| + |2-3| = 8$
- $\text{Dist}(C1, \text{Tupla6}) = |1-3| + |0-3| + |1-1| + |2-3| = 6$

Centroide 2 (C2) = [6, 3, 6, 1] (Tupla 4)

[ 5, 4, 3, 1 ]

- **$\text{Dist}(C2, \text{Tupla4}) = 0$**
- $\text{Dist}(C2, \text{Tupla5}) = |6-3| + |3-4| + |6-2| + |1-3| = 10$
- $\text{Dist}(C2, \text{Tupla6}) = |6-3| + |3-3| + |6-1| + |1-3| = 10$

|   | Atributo 1 | Atributo 2 | Atributo 3 | Atributo 4 |
|---|------------|------------|------------|------------|
| 1 | 5          | 4          | 3          | 1          |
| 2 | 1          | 0          | 1          | 2          |
| 3 | 2          | 1          | 0          | 2          |
| 4 | 6          | 3          | 6          | 1          |
| 5 | 3          | 4          | 2          | 3          |
| 6 | 3          | 3          | 1          | 3          |

A red arrow pointing to the row for Tupla 4 in the table, which is highlighted with a red border.

Red arrow pointing to Tupla 4 in the table.

{36}------------------------------------------------

# k-means: Algoritmo de agrupamento particional

- **Dinâmica:** Execute 1 iteração e determine o centróide, considerando que as tuplas 2 e 4 foram escolhidas como centróides:

Manhattan: 
$$d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$$

Centroide 1 (C1) = [ 1, 0, 1, 2 ] (Tupla 2)

[1, 0, 1, 2]

[2, 1, 0, 2]

- $\text{Dist}(C1, \text{Tupla5}) = |1-3| + |0-4| + |1-2| + |2-3| = 8$

- $\text{Dist}(C1, \text{Tupla6}) = |1-3| + |0-3| + |1-1| + |2-3| = 6$

Centroide 2 (C2) = [6, 3, 6, 1 ] (Tupla 4)

[ 5, 4, 3, 1 ]

[ 6, 3, 6, 1 ]

- $\text{Dist}(C2, \text{Tupla5}) = |6-3| + |3-4| + |6-2| + |1-3| = 10$

- $\text{Dist}(C2, \text{Tupla6}) = |6-3| + |3-3| + |6-1| + |1-3| = 10$

|   | Atributo 1 | Atributo 2 | Atributo 3 | Atributo 4 |
|---|------------|------------|------------|------------|
| 1 | 5          | 4          | 3          | 1          |
| 2 | 1          | 0          | 1          | 2          |
| 3 | 2          | 1          | 0          | 2          |
| 4 | 6          | 3          | 6          | 1          |
| 5 | 3          | 4          | 2          | 3          |
| 6 | 3          | 3          | 1          | 3          |

Red arrow pointing to the first column of the table.

{37}------------------------------------------------

# k-means: Algoritmo de agrupamento particional

- **Dinâmica:** Execute 1 iteração e determine o centróide, considerando que as tuplas 2 e 4 foram escolhidas como centróides:

Manhattan: 
$$d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$$

|   | Atributo 1 | Atributo 2 | Atributo 3 | Atributo 4 |
|---|------------|------------|------------|------------|
| 1 | 5          | 4          | 3          | 1          |
| 2 | 1          | 0          | 1          | 2          |
| 3 | 2          | 1          | 0          | 2          |
| 4 | 6          | 3          | 6          | 1          |
| 5 | 3          | 4          | 2          | 3          |
| 6 | 3          | 3          | 1          | 3          |

Red arrow pointing right

Centroide 1 (C1) = [ 1, 0, 1, 2 ] (Tupla 2)

[1, 0, 1, 2]

[2, 1, 0, 2]

[3, 4, 2, 3]

- **Dist(C1, Tupla 6) = |1-3|+|0-3|+|1-1|+|2-3|= 6**

Centroide 2 (C2) = [6, 3, 6, 1 ] (Tupla 4)

[ 5, 4, 3, 1 ]

[ 6, 3, 6, 1 ]

- **Dist(C2, Tupla 6) = |6-3|+|3-3|+|6-1|+|1-3|= 10**

{38}------------------------------------------------

# k-means: Algoritmo de agrupamento particional

- **Dinâmica:** Execute 1 iteração e determine o centróide, considerando que as tuplas 2 e 4 foram escolhidas como centróides:

Manhattan: 
$$d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$$

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

Centroide 2 (C2) = [6, 3, 6, 1 ] (Tupla 4)

[ 5, 4, 3, 1]

[ 6, 3, 6, 1]

{39}------------------------------------------------

# k-means: Algoritmo de agrupamento particional

- **Dinâmica:** Execute 1 iteração e determine o centróide, considerando que as tuplas 2 e 4 foram escolhidas como centróides:

Manhattan: 
$$d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$$
## Recalculando os centróides:

Centroide 1 (C1) = [ 1, 0, 1, 2 ] (Tupla 2)

[1, 0, 1, 2]

[2, 1, 0, 2]

[3, 4, 2, 3]

[3, 3, 1, 3]

[ (1+2+3+3)/4, (0+1+4+3)/4, (1+0+2+1)/4, (3+3+1+3)/4 ] =

[ 9/4, 8/4, 4/4, 10/4 ] = [2.25, 2, 1, 2.5 ]

Centroide 2 (C2) = [6, 3, 6, 1 ] (Tupla 4)

[ 5, 4, 3, 1]

[ 6, 3, 6, 1]

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

# k-means: Algoritmo de agrupamento particional

- **Dinâmica:** Execute 1 iteração e determine o centróide, considerando que as tuplas 2 e 4 foram escolhidas como centróides:

Manhattan: 
$$d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$$
## Recalculando os centróides:

Centroide 1 (C1) = ~~[1, 0, 1, 2]~~ (Tupla 2) **[2.25, 2, 1, 2.5]**

[1, 0, 1, 2]

[2, 1, 0, 2]

[3, 4, 2, 3]

[3, 3, 1, 3]

Centroide 2 (C2) = **[6, 3, 6, 1]** (Tupla 4)

[5, 4, 3, 1]

[6, 3, 6, 1]

$[(5+6)/2, (4+3)/2, (3+6)/2, (1+1)/2] = [11/2, 7/2, 9/2, 2/2]$   
**= [5.5, 3.5, 4.5, 1]**

|   | Atributo 1 | Atributo 2 | Atributo 3 | Atributo 4 |
|---|------------|------------|------------|------------|
| 1 | 5          | 4          | 3          | 1          |
| 2 | 1          | 0          | 1          | 2          |
| 3 | 2          | 1          | 0          | 2          |
| 4 | 6          | 3          | 6          | 1          |
| 5 | 3          | 4          | 2          | 3          |
| 6 | 3          | 3          | 1          | 3          |

{41}------------------------------------------------
## k-means: Algoritmo de agrupamento particional

- **Dinâmica:** Execute 1 iteração e determine o centróide, considerando que as tuplas 2 e 4 foram escolhidas como centróides:

Manhattan: 
$$d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$$

**Recalculando os centróides:**

Centroide 1 (C1) = ~~[1, 0, 1, 2]~~ (Tupla 2) **[2.25, 2, 1, 2.5]**

[1, 0, 1, 2]

[2, 1, 0, 2]

[3, 4, 2, 3]

[3, 3, 1, 3]

Centroide 2 (C2) = ~~[6, 3, 6, 1]~~ (Tupla 4) **[5.5, 3.5, 4.5, 1]**

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
### K-Means
### `sklearn.cluster.KMeans`

```
class sklearn.cluster.KMeans(n_clusters=8, *, init='k-means++', n_init='warn', max_iter=300, tol=0.0001, verbose=0, random_state=None, copy_x=True, algorithm='lloyd')
```

[\[source\]](#)

- **tolfloat**, padrão = 1e-4 : Tolerância relativa em relação à norma de Frobenius da diferença nos centros do cluster de duas iterações consecutivas para declarar convergência.
- **algorithm**{“lloyd”, “elkan”}, default=”lloyd”. O algoritmo clássico do estilo EM é “lloyd”. A variação “elkan” pode ser mais eficiente em alguns conjuntos de dados com clusters bem definidos. No entanto, consome mais memória devido à alocação de uma matriz extra de forma (n\_samples, n\_clusters).

{44}------------------------------------------------
### K-Means

```
# Executando o k-Means para cada valor de k  
kmeanModel = KMeans(n_clusters=k,n_init='auto')  
kmeanModel.fit(X)
```

X contém os dados de entrada

{45}------------------------------------------------

A network graph visualization using pushpins and string. The pushpins, representing nodes, are colored red, white, green, yellow, and blue. They are interconnected by a dense web of black string, representing edges. The nodes are distributed across the frame, with a high concentration of connections in the lower-left and central areas.

A network graph visualization using pushpins and string.

Como determinar a  
quantidade de clusters?  
Qual o melhor  $k$ ?

{46}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-0a42e05c07941450f34e4f7117725834_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A network graph visualization using pushpins and string.
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

$$\text{Distortion} = 1/n * \sum(\text{distance}(\text{point}, \text{centroid})^2)$$

{48}------------------------------------------------
### K-Means e o método Elbow

- Inércia: É a soma das distâncias quadradas das amostras ao centro do cluster mais próximo.

$$\text{Inertia} = \sum (\text{distance}(\text{point}, \text{centroid})^2)$$

- Para determinar o número ideal de clusters, temos que selecionar o valor de k no “cotovelo”, ou seja, o ponto após o qual a distorção/inércia começa a diminuir de forma linear.

{49}------------------------------------------------
### K-Means e o método Elbow

- Exemplo:

Dataset de Pontos

| x    | y    |
|------|------|
| -6.0 | 4.0  |
| -5.0 | 4.0  |
| -4.0 | 4.0  |
| -4.0 | 6.0  |
| -4.0 | 7.0  |
| 2.0  | 7.0  |
| 3.0  | 6.0  |
| 3.0  | 4.0  |
| 3.0  | 3.0  |
| 4.0  | 5.0  |
| 4.0  | 4.0  |
| 5.0  | 6.0  |
| -6.0 | -4.0 |
| -5.0 | -5.0 |
| 2.0  | -5.0 |
| 3.0  | -5.0 |
| 5.0  | -3.0 |
| 5.0  | -5.0 |
| 5.0  | -6.0 |

Scatter plot titled 'Dataset de Pontos' showing 20 data points on a 2D plane. The x-axis and y-axis both range from -10.0 to 10.0 with major ticks every 2.5 units. The points are clustered into three groups: a group of 5 points in the upper-left quadrant (approx. x: -6 to -4, y: 4 to 7), a group of 10 points in the upper-right quadrant (approx. x: 2 to 5, y: 3 to 7), and a group of 5 points in the lower-right quadrant (approx. x: 2 to 5, y: -5 to -3).

{50}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-7e2465b81aed11b2e58575a811424b75_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Scatter plot titled 'Dataset de Pontos' showing 20 data points on a 2D plane.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-242fdee4611b447a4206005652ea3c19_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Scatter plot of a dataset with 15 points.
<!-- /IMAGE_DESCRIPTION -->
### K-Means e o método Elbow

- Exemplo:

Dataset de Pontos

| Cluster | X    | Y    |
|---------|------|------|
| 1       | -6.0 | 4.0  |
| 1       | -5.0 | 4.0  |
| 1       | -4.0 | 4.0  |
| 1       | -4.0 | 6.0  |
| 2       | 2.0  | 6.0  |
| 2       | 3.0  | 4.0  |
| 2       | 3.0  | 5.0  |
| 2       | 4.0  | 4.0  |
| 2       | 4.0  | 5.0  |
| 2       | 5.0  | 5.0  |
| 3       | -6.0 | -4.0 |
| 3       | -5.0 | -5.0 |
| 4       | 2.0  | -5.0 |
| 4       | 3.0  | -5.0 |
| 4       | 5.0  | -5.0 |
| 4       | 5.0  | -6.0 |
| 4       | 5.0  | -7.0 |

Scatter plot of a dataset with 15 points. The points are clustered into four groups: a top-left cluster of 4 points, a top-right cluster of 5 points, a bottom-left cluster of 3 points, and a bottom-right cluster of 3 points. The axes range from -10.0 to 10.0.

Metodo do cotovelo usando Distorca

| Valores de K | Distorcao |
|--------------|-----------|
| 2            | 3.8       |
| 3            | 2.3       |
| 4            | 1.4       |
| 5            | 1.2       |
| 6            | 1.0       |
| 7            | 0.8       |
| 8            | 0.75      |
| 9            | 0.65      |

Line graph showing the distortion metric versus the number of clusters (K). The distortion decreases sharply from K=2 to K=4 and then levels off.

Metodo do cotovelo usando a inercia

| Valores de K | Inercia |
|--------------|---------|
| 2            | 550     |
| 3            | 180     |
| 4            | 50      |
| 5            | 40      |
| 6            | 35      |
| 7            | 30      |
| 8            | 25      |
| 9            | 20      |

Line graph showing the inertia metric versus the number of clusters (K). The inertia decreases sharply from K=2 to K=4 and then levels off.

Observando os gráficos, concluímos que o número ideal de clusters para os dados é 4.

{51}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-2d62ff2bded0c21414a0f40fdf8fd537_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Line graph showing the distortion metric versus the number of clusters (K).
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-6dda36bad0978e272ca0420b0902b73a_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Line graph showing the inertia metric versus the number of clusters (K).
<!-- /IMAGE_DESCRIPTION -->
### K-Means e o método Elbow

- Exemplo:

The figure consists of two side-by-side scatter plots, both titled "Dataset de Pontos". Both plots have x and y axes ranging from -10.0 to 10.0 with major ticks every 2.5 units. The left plot shows 15 blue data points distributed in four distinct groups. The right plot shows the same 15 data points, but with four additional colored dots representing cluster centroids: a purple dot at approximately (-4.5, 5.0), an orange dot at approximately (3.5, 5.0), a green dot at approximately (-5.5, -4.5), and a red dot at approximately (4.0, -5.0). The data points are colored blue, except for those near the centroids, which are colored to match their assigned cluster.

| Cluster    | Centroid (x, y) | Data Points (x, y)                                                                        |
|------------|-----------------|-------------------------------------------------------------------------------------------|
| 1 (Purple) | (-4.5, 5.0)     | (-6.0, 4.0), (-5.0, 4.0), (-4.0, 4.0), (-4.0, 6.0), (-4.0, 7.0)                           |
| 2 (Orange) | (3.5, 5.0)      | (2.0, 7.0), (3.0, 6.0), (4.0, 5.0), (5.0, 6.0), (3.0, 4.0), (4.0, 4.0), (3.0, 3.0)        |
| 3 (Green)  | (-5.5, -4.5)    | (-6.0, -4.0), (-5.0, -5.0), (-4.0, -5.0)                                                  |
| 4 (Red)    | (4.0, -5.0)     | (2.0, -5.0), (3.0, -5.0), (4.0, -5.0), (5.0, -5.0), (5.0, -6.0), (5.0, -7.0), (5.0, -2.0) |

Two scatter plots titled 'Dataset de Pontos' showing data points and their assignment to 4 clusters.

Observando os gráficos, concluímos que o número ideal de clusters para os dados é 4.

{52}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-4666738057044ad78ced4dbbc0c1bfb3_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Two scatter plots titled 'Dataset de Pontos' showing data points and their assignment to 4 clusters.
<!-- /IMAGE_DESCRIPTION -->
## Dinâmica

- Exemplos de uso do k-Means
