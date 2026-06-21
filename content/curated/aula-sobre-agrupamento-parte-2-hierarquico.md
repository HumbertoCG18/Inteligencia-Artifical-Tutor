<!-- EXEC_SUMMARY_START -->
## Sumário
> *Leia antes de varrer o arquivo. Vá direto à seção relevante para a pergunta do aluno.*

- **Subáreas da Inteligência Artificial**
  - Aprendizado Não Supervisionado
  - Aprendizado Não Supervisionado
  - Agrupamento
  - Agrupamento Hierárquico
  - Agrupamento Hierárquico
  - Agrupamento Hierárquico
  - Agrupamento Hierárquico
  - Agrupamento Hierárquico
  - Agrupamento Hierárquico
  - Agrupamento Hierárquico
  - Agrupamento Hierárquico
  - Agrupamento Hierárquico
  - Agrupamento Hierárquico
  - Agrupamento Hierárquico
  - Agrupamento Hierárquico
  - Agrupamento Hierárquico
  - Agrupamento Hierárquico
  - Agrupamento Hierárquico
- **Agrupamento Hierárquico**
- **Agrupamento Hierárquico**
- **Agrupamento Hierárquico**
- **Agrupamento Hierárquico**
- **Agrupamento Hierárquico**
- **Agrupamento Hierárquico**
- **Agrupamento Hierárquico**
- **Agrupamento Hierárquico**
  - `sklearn.cluster.AgglomerativeClustering`
- **Agrupamento Hierárquico**
  - sklearn.cluster.AgglomerativeClustering
  - `sklearn.cluster.AgglomerativeClustering`
- **Agrupamento Hierárquico**
  - `sklearn.cluster.AgglomerativeClustering`
- **Agrupamento Hierárquico**

<!-- EXEC_SUMMARY_END -->
<!-- DATALAB_CHUNK 1: pages 1-20 -->

{0}------------------------------------------------
##### Abstract background with orange and green splattersThe background is an abstract composition of numerous circular and irregular splatters. On the left, there are large, overlapping splatters in shades of orange and brown. On the right, there are large, overlapping splatters in shades of green and yellow. The overall effect is a vibrant, textured gradient from blue on the left to white and orange on the right.Aprendizado não supervisionado: parte 2

Profa Silvia Moraes

{1}------------------------------------------------
## Subáreas da Inteligência Artificial

The diagram illustrates the subfields of Artificial Intelligence (IA) centered around a hub labeled "Inteligência Artificial (IA)". The subfields are arranged in a circular pattern around the center, with lines connecting them to the central hub. A red segment highlights the "Aprendizado de Máquina (Machine Learning)" subfield.

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

**Inteligência Artificial (IA)**

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

The diagram illustrates the supervised machine learning process. It begins with a 'Dataset Sem Anotação' (Unlabeled Dataset) represented by a collage of images of cats, dogs, and chickens. An arrow points from this dataset to a box labeled 'Algoritmo de Machine Learning Supervisionado' (Supervised Machine Learning Algorithm). Below this box is a 'Treinamento' (Training) box containing a neural network diagram. A second arrow points from the training box to a final box labeled 'Modelo' (Model), which also contains a neural network diagram.

A collage of various images including cats, dogs, and chickens, representing an unlabeled dataset. Diagram of a neural network structure. Diagram of a neural network structure.

{3}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-7055f51feb10ea4ea48b27c36f085286_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A collage of various images including cats, dogs, and chickens, representing an unlabeled dataset.
<!-- /IMAGE_DESCRIPTION -->
### Aprendizado Não Supervisionado

Executa **tarefas descritivas**: explora ou descreve um conjunto de dados.

- **Agrupamento**: divisão em grupos baseada em alguma regularidade ou similaridade
- **Sumarização**: descrição simples e compacta
- **Associação**: relações frequentes entre dados

A close-up photograph of several apples, including red and green varieties, illustrating the concept of data points or clusters.

A close-up photograph of several apples, including red and green varieties, illustrating the concept of data points or clusters.

A photograph of many small, identical purple and yellow teddy bears arranged in rows, illustrating the concept of data points or clusters.

A photograph of many small, identical purple and yellow teddy bears arranged in rows, illustrating the concept of data points or clusters.

{4}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-16d86083b7ebdc40c0647a1d3d46ace7_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A close-up photograph of several apples, including red and green varieties, illustrating the concept of data points or clusters.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-b615ff07e8a0f467f0a6f4783c4463eb_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A photograph of many small, identical purple and yellow teddy bears arranged in rows, illustrating the concept of data points or clusters.
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
### Agrupamento Hierárquico

A glowing lightbulb with a black outline, set against a yellow background with a white, torn-paper-like edge on the left. The lightbulb is illuminated, and its filament is visible. A black cord extends from the base of the bulb towards the bottom right.

A glowing lightbulb with a black outline, set against a yellow background with a white, torn-paper-like edge on the left. The lightbulb is illuminated, and its filament is visible. A black cord extends from the base of the bulb towards the bottom right.

{6}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-afe5eb459b7c9cfe880b067777d876d8_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A glowing lightbulb with a black outline, set against a yellow background with a white, torn-paper-like edge on the left.
<!-- /IMAGE_DESCRIPTION -->
### Agrupamento Hierárquico

- Um algoritmo desse tipo gera a partir de uma matriz de proximidade, uma série de partições aninhadas.
- Pode ser:
  - Aglomerativo
  - Por divisão

O diagrama ilustra um processo de agrupamento hierárquico por divisão (divisivo). No topo, um nó contendo '1,2,3,4,5' representa o conjunto completo. Este nó se divide para dois nós: '1,2' à esquerda e '3,4,5' à direita. O nó '1,2' se divide para os nós individuais '1' e '2'. O nó '3,4,5' se divide para o nó '3' e o nó '4,5'. O nó '4,5' se divide para os nós individuais '4' e '5'. À esquerda do diagrama, uma seta vertical apontando para baixo é rotulada 'Por divisão'. À direita, uma seta vertical apontando para cima é rotulada 'aglomerativo', indicando a direção oposta do processo de construção da árvore.

```
graph TD; A["1,2,3,4,5"] --> B["1,2"]; A --> C["3,4,5"]; B --> D["1"]; B --> E["2"]; C --> F["3"]; C --> G["4,5"]; G --> H["4"]; G --> I["5"];
```

Diagrama de agrupamento hierárquico por divisão (divisivo)

{7}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-a738993919a50143787084ee7ce6e2f2_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de agrupamento hierárquico por divisão (divisivo)
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-042733dc5e8e7f5f30b60adba3266cde_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de agrupamento hierárquico por divisão
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-2cde062fd82833415971a8bd1a2cafab_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de agrupamento hierárquico aglomerativo
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-dfe556fea00682b09a59427aaf72051c_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de agrupamento hierárquico por divisão (divisivo)
<!-- /IMAGE_DESCRIPTION -->
### Agrupamento Hierárquico
#### - **Por Divisão:**

- Inicia com todos os objetos representando um único grupo.
- A cada passo, divide o grupo até que cada grupo contenha um objeto (ou  $k$  grupos) ou algum critério de parada seja atingido.
- Para definir os grupos:
  - usa uma **matriz de similaridade ou distância**.

{8}------------------------------------------------
### Agrupamento Hierárquico

- Por divisão:

A diagram illustrating hierarchical grouping by division. It features a vertical blue arrow pointing downwards, with the text "Por divisão" written vertically along its right side. To the right of the arrow, there is a blue rounded rectangular box containing the numbers "1,2,3,4,5".

Diagram illustrating hierarchical grouping by division.

{9}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-562f471e8153729557e6a4ee6343c32c_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram illustrating hierarchical grouping by division.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-cfda9df1319e04207eb28bcefd1dab7b_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram illustrating hierarchical grouping by division.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-e9314c83043183351ed74908e9bf2f90_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram illustrating hierarchical grouping by division.
<!-- /IMAGE_DESCRIPTION -->
### Agrupamento Hierárquico

- Por divisão:

The diagram illustrates hierarchical grouping by division. On the left, a vertical blue arrow points downwards, with the text "Por divisão" written vertically alongside it. To the right of the arrow is a hierarchical tree structure. The root node is a blue rounded rectangle containing the text "1,2,3,4,5". Two lines descend from this root node to two child nodes, also blue rounded rectangles. The left child node contains the text "1,2" and the right child node contains the text "3, 4,5".

Diagram illustrating hierarchical grouping by division.

{10}------------------------------------------------
### Agrupamento Hierárquico

- Por divisão:

The diagram illustrates a hierarchical grouping structure. On the left, a vertical blue arrow points downwards, with the text "Por divisão" (By division) written vertically next to it. To the right of the arrow is a tree structure of blue rounded rectangular boxes. The root node at the top is labeled "1,2,3,4,5". It branches into two child nodes: "1,2" on the left and "3, 4,5" on the right. The "1,2" node branches into two leaf nodes: "1" and "2". The "3, 4,5" node branches into two leaf nodes: "3" and "4,5".

```
graph TD; A["1,2,3,4,5"] --> B["1,2"]; A --> C["3, 4,5"]; B --> D["1"]; B --> E["2"]; C --> F["3"]; C --> G["4,5"];
```

Diagram illustrating hierarchical grouping by division.

{11}------------------------------------------------
### Agrupamento Hierárquico

- Por divisão:

Diagrama de agrupamento hierárquico por divisão. O processo é ilustrado por uma seta vertical descendente rotulada "Por divisão" e uma estrutura de árvore de nós.

```
graph TD; A["1,2,3,4,5"] --> B["1,2"]; A --> C["3, 4,5"]; B --> D["1"]; B --> E["2"]; C --> F["3"]; C --> G["4,5"]; G --> H["4"]; G --> I["5"];
```

A estrutura de árvore mostra a seguinte hierarquia:

- Nó raiz: 1,2,3,4,5
  - Nó filho esquerdo: 1,2
    - Nó folha esquerdo: 1
    - Nó folha direito: 2
  - Nó filho direito: 3, 4,5
    - Nó folha esquerdo: 3
    - Nó filho direito: 4,5
      - Nó folha esquerdo: 4
      - Nó folha direito: 5

Diagrama de agrupamento hierárquico por divisão

{12}------------------------------------------------
### Agrupamento Hierárquico

- **Aglomerativo:**
  - Inicia com cada objeto representando um grupo individual.
  - A cada passo, combina o par mais próximo de grupos, até que somente um grupo (ou  $k$  grupos) reste ou algum critério de parada seja atingido.
- Para definir os grupos: algoritmos hierárquicos tradicionais usam a **matriz de similaridade ou distância**

{13}------------------------------------------------
### Agrupamento Hierárquico

- Aglomerativo:

The diagram illustrates the agglomerative hierarchical clustering process. At the bottom, five numbered nodes (1, 2, 3, 4, 5) are arranged horizontally. A vertical arrow points upwards from the right side of these nodes, labeled 'aglomerativo', indicating the direction of the clustering process.

Diagram illustrating the agglomerative hierarchical clustering process. Five numbered nodes (1, 2, 3, 4, 5) are shown at the bottom, and a vertical arrow labeled 'aglomerativo' points upwards, indicating the direction of the clustering process.

{14}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-4ee27dbf5ef12e7b58b0ef0937bc5a5e_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram illustrating the agglomerative hierarchical clustering process.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-724c7777b608e53be38b12b6fb3c43bc_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram illustrating hierarchical agglomerative clustering.
<!-- /IMAGE_DESCRIPTION -->
### Agrupamento Hierárquico

- Aglomerativo:

The diagram illustrates the process of hierarchical agglomerative clustering. It shows five data points (1, 2, 3, 4, 5) at the bottom level. Points 1 and 2 are connected by a line, and points 4 and 5 are connected by a line. Above these connections are two blue boxes labeled '1,2' and '4,5' respectively. A vertical blue arrow on the right side points upwards, labeled 'aglomerativo', indicating the direction of the clustering process.

```
graph BT; 1 --- 12[1,2]; 2 --- 12; 4 --- 45[4,5]; 5 --- 45; 3; style 1 fill:#4a7ebb,color:#fff; style 2 fill:#4a7ebb,color:#fff; style 3 fill:#4a7ebb,color:#fff; style 4 fill:#4a7ebb,color:#fff; style 5 fill:#4a7ebb,color:#fff; style 12 fill:#4a7ebb,color:#fff; style 45 fill:#4a7ebb,color:#fff;
```

Diagram illustrating hierarchical agglomerative clustering.

{15}------------------------------------------------
### Agrupamento Hierárquico

- Aglomerativo:

The diagram illustrates the agglomerative clustering process. It shows a hierarchy of clusters represented by blue rounded rectangles. At the bottom level, there are five individual data points labeled 1, 2, 3, 4, and 5. In the middle level, two clusters are formed: one containing points 1 and 2, and another containing points 3, 4, and 5. At the top level, these two clusters are merged into a single large cluster containing all five points (1, 2, 3, 4, 5). To the right of the diagram, a vertical blue arrow points upwards, labeled 'aglomerativo', indicating the direction of the clustering process.

```
graph BT; 1[1] --- 12[1,2]; 2[2] --- 12; 3[3] --- 345[3,4,5]; 4[4] --- 345; 5[5] --- 345; 12 --- 12345[1,2,3,4,5]; 345 --- 12345;
```

Diagram of hierarchical agglomerative clustering showing the merging of clusters 1,2 and 3,4,5 into a final cluster 1,2,3,4,5.

{16}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-0f985b39edc1d52ba3600c438bc8f0a5_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of hierarchical agglomerative clustering showing the merging of clusters 1,2 and 3,4,5 into a final cluster 1,2,3,4,5.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-b5335262987c819d7f71ce40f99cb71b_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of hierarchical clustering showing the first step where clusters A and B are merged.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-b2f5606b9c7184c1c6070a290080a3e3_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram showing the hierarchical clustering process.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-4ff00a489baaa34a0c01070de1d613db_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Hierarchical clustering diagram showing three clusters merging into a single structure.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-838c31609fac483fa2c01c7896a2fd6d_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Hierarchical clustering diagram showing the merging of clusters C8, C9, and C10 into C11.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-8269648391c59363ea61243864a2adf7_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Hierarchical clustering diagram showing the merging of clusters C8, C9, and C10 into C11.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-cf8bd014a50b7c69435e804f67f9617f_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Hierarchical clustering diagram showing the merging of clusters C8, C9, and C10 into C11.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-f142b022cfc716cd967297f027efe647_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Hierarchical clustering diagram showing the merging of clusters C8, C9, and C10 into C11.
<!-- /IMAGE_DESCRIPTION -->
### Agrupamento Hierárquico
#### - **Aglomerativo:**

Diagrama de agrupamento hierárquico aglomerativo. O diagrama mostra a formação de clusters a partir de elementos individuais. No nível inferior, há cinco elementos: 1, 2, 3, 4 e 5. Os elementos 1 e 2 são combinados em um cluster '1,2'. Os elementos 4 e 5 são combinados em um cluster '4,5'. Em seguida, o elemento 3 é combinado com o cluster '4,5' para formar o cluster '3, 4,5'. Finalmente, o cluster '1,2' é combinado com o cluster '3, 4,5' para formar o cluster final '1,2,3,4,5'. À direita do diagrama, uma seta vertical apontando para cima é rotulada 'aglomerativo', indicando a direção da fusão dos clusters.

```
graph BT; 1 --- 12[1,2]; 2 --- 12; 4 --- 45[4,5]; 5 --- 45; 3 --- 345[3, 4,5]; 45 --- 345; 12 --- 12345[1,2,3,4,5]; 345 --- 12345;
```

Diagrama de agrupamento hierárquico aglomerativo

{17}------------------------------------------------
### Agrupamento Hierárquico

- Um algoritmo desse tipo gera a partir de uma matriz de proximidade, uma série de partições aninhadas.
- Pode ser:
  - Aglomerativo
  - Por divisão

O diagrama ilustra um agrupamento hierárquico por divisão (divisivo). No topo, um nó contendo '1,2,3,4,5' se divide para dois nós: '1,2' à esquerda e '3,4,5' à direita. O nó '1,2' se divide para os nós '1' e '2'. O nó '3,4,5' se divide para os nós '3' e '4,5'. O nó '4,5' se divide para os nós '4' e '5'. À esquerda do diagrama, uma seta vertical apontando para baixo é rotulada 'Por divisão'. À direita, uma seta vertical apontando para cima é rotulada 'aglomerativo', indicando a direção oposta do processo.

```
graph TD; A["1,2,3,4,5"] --> B["1,2"]; A --> C["3,4,5"]; B --> D["1"]; B --> E["2"]; C --> F["3"]; C --> G["4,5"]; G --> H["4"]; G --> I["5"];
```

Diagrama de agrupamento hierárquico por divisão (divisivo)

{18}------------------------------------------------
### Agrupamento Hierárquico

- Produz um conjunto de grupos aninhados, organizados como uma árvore, mostrando partições ou combinações.
- Pode ser visualizado por um dendograma..

```
graph TD; A["1,2,3,4,5,6"] --- B["1,3,2,5,4"]; A --- C["4"]; A --- D["6"]; B --- E["1,3"]; B --- F["2,5,4"]; E --- G["1"]; E --- H["3"]; F --- I["2,5"]; F --- J["4"]; I --- K["2"]; I --- L["5"];
```

A hierarchical tree diagram illustrating the grouping of elements 1 through 6. The root node is labeled "1,2,3,4,5,6". It branches into "1,3,2,5,4" and "4". The "1,3,2,5,4" node further branches into "1,3" and "2,5,4". The "1,3" node branches into "1" and "3". The "2,5,4" node branches into "2,5" and "4". The "2,5" node branches into "2" and "5". The final leaf nodes are "1", "3", "2", "5", "4", and "6".

Hierarchical tree diagram showing the grouping of elements 1 through 6.

A dendrogram illustrating the hierarchical clustering of elements 1 through 6. The x-axis represents the elements in the order 1, 3, 2, 5, 4, 6. The y-axis represents the distance or similarity, ranging from 0 to 0.2. The dendrogram shows the following fusion steps: elements 1 and 3 merge at a distance of approximately 0.05; elements 2 and 5 merge at a distance of approximately 0.07; the cluster {2, 5} merges with element 4 at a distance of approximately 0.17; the cluster {1, 3} merges with the cluster {2, 5, 4} at a distance of approximately 0.18; and finally, the entire group {1, 2, 3, 4, 5, 6} merges with element 6 at a distance of approximately 0.21.

Dendrogram showing the hierarchical clustering of elements 1 through 6.

{19}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-2b3a967f6ce4f23649be995a353e39f8_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Hierarchical tree diagram showing the grouping of elements 1 through 6.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-1c427123350e0e73e2a109b79069314b_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Dendrogram showing the hierarchical clustering of elements 1 through 6.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-0b3d9fe35da3ee0c88f1420bb9ed7a03_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Hierarchical clustering diagram showing the merging of clusters C8, C9, and C10 into a single structure, with leaf nodes C1 through C7.
<!-- /IMAGE_DESCRIPTION -->
### Agrupamento Hierárquico

- **Vantagens desse tipo de agrupamento:**
  - Não é necessário assumir um número particular de grupos
  - Qualquer número de grupos desejado pode ser obtido ao 'cortar' o dendograma no nível apropriado.
  - Podem corresponder a taxonomias úteis. Exemplos em ciências biológicas (e.g., reino animal, reconstrução filogenética, . . . ).

<!-- DATALAB_CHUNK 2: pages 21-40 -->

{20}------------------------------------------------

# Agrupamento Hierárquico

- Similaridade baseada nas distâncias entre os elementos ou centróides dos clusters.
- Em geral usam uma matriz de similaridade/distancia

The diagram shows two irregular, cloud-like shapes representing clusters. Each cluster contains four black dots representing individual data points. A double-headed horizontal arrow connects the two clusters, with the text 'Similaridade?' written above it, indicating a comparison of similarity between the two groups.

Diagram illustrating similarity between two clusters.

|    | p1 | p2 | p3 | p4 | p5 | ... |
|----|----|----|----|----|----|-----|
| p1 |    |    |    |    |    |     |
| p2 |    |    |    |    |    |     |
| p3 |    |    |    |    |    |     |
| p4 |    |    |    |    |    |     |
| p5 |    |    |    |    |    |     |
| .  |    |    |    |    |    |     |

{21}------------------------------------------------

# Agrupamento Hierárquico

- Os algoritmos aglomerativos são mais usados.
- A operação-chave é a distância entre os dois clusters.
- A diferença entre os algoritmos que seguem essa abordagem está justamente no cálculo dessa distância

```
graph TD; Inicio([Inicio]) --> Entrada[/Objetos e seus atributos/]; Entrada --> Calcula[Calcula matriz de distancias]; Calcula --> Seta[Seta Objeto como Cluster]; Seta --> Decisão{Nro de cluster = 1}; Decisão -- Sim --> Fim([Fim]); Decisão -- Nao --> Une[Une dois clusters proximos]; Une --> Atualiza[Atualiza Matriz de distancias]; Atualiza --> Decisão;
```

The flowchart illustrates the hierarchical clustering process. It begins with 'Inicio' (Start), followed by 'Objetos e seus atributos' (Objects and their attributes). The next step is 'Calcula matriz de distancias' (Calculate distance matrix), followed by 'Seta Objeto como Cluster' (Set object as cluster). A decision diamond asks 'Nro de cluster = 1' (Number of clusters = 1). If 'Sim' (Yes), it proceeds to 'Fim' (End). If 'Nao' (No), it proceeds to 'Une dois clusters proximos' (Merge two closest clusters), then 'Atualiza Matriz de distancias' (Update distance matrix), and loops back to the decision diamond.

Flowchart of Hierarchical Clustering process

{22}------------------------------------------------

# Agrupamento Hierárquico

Exemplo:

- Considere os objetos (pontos):

A : (1,1)

B: (2,1)

C: (3,4)

D: (4,6)

E: (5,3)

F: (6,4)

G: (7,3)

```
graph TD; Inicio([Inicio]) --> Entrada[/Objetos e seus atributos/]; Entrada --> SetaObjeto[Seta Objeto como Cluster]; SetaObjeto --> CalculaMatriz[Calcula matriz de distancias]; CalculaMatriz --> Decidao{Nro de cluster = 1}; Decidao -- Sim --> Fim([Fim]); Decidao -- Nao --> UneClusters[Une dois clusters proximos]; UneClusters --> AtualizaMatriz[Atualiza Matriz de distancias]; AtualizaMatriz --> Decidao;
```

The flowchart illustrates the hierarchical clustering process. It begins with 'Inicio' (Start), followed by 'Objetos e seus atributos' (Objects and their attributes). The process then sets each object as a cluster ('Seta Objeto como Cluster') and calculates a distance matrix ('Calcula matriz de distancias'). A decision is made on whether the number of clusters is 1 ('Nro de cluster = 1'). If 'Sim' (Yes), the process ends ('Fim'). If 'Nao' (No), two closest clusters are merged ('Une dois clusters proximos'), the distance matrix is updated ('Atualiza Matriz de distancias'), and the decision is repeated.

Flowchart of Hierarchical Clustering process

{23}------------------------------------------------

# Agrupamento Hierárquico

Exemplo:

Diagram showing 7 objects (C1 to C7) with their coordinates:

| Object | Coordinates |
|--------|-------------|
| C1     | A(1,1)      |
| C2     | B(2,1)      |
| C3     | C(3,4)      |
| C4     | D(4,6)      |
| C5     | E(5,3)      |
| C6     | F(6,4)      |
| C7     | G(7,3)      |

Diagram showing 7 objects (C1 to C7) with their coordinates.

```
graph TD; Inicio([Inicio]) --> Entrada[/Objetos e seus atributos/]; Entrada --> SetaObjeto[Seta Objeto como Cluster]; SetaObjeto --> CalculaMatriz[Calcula matriz de distancias]; CalculaMatriz --> Decisão{Nro de cluster = 1}; Decisão -- Sim --> Fim([Fim]); Decisão -- Nao --> UneClusters[Une dois clusters proximos]; UneClusters --> AtualizaMatriz[Atualiza Matriz de distancias]; AtualizaMatriz --> Decisão;
```

Flowchart illustrating the Hierarchical Clustering process:

- Inicio
- Objetos e seus atributos
- Seta Objeto como Cluster
- Calcula matriz de distancias
- Decision: Nro de cluster = 1
  - If Sim: Fim
  - If Nao: Une dois clusters proximos
- Atualiza Matriz de distancias
- Loop back to Decision

Flowchart of the Hierarchical Clustering process.

{24}------------------------------------------------

# Agrupamento Hierárquico

Exemplo:

- Considere os objetos (pontos):

A : (1,1), B: (2,1), C: (3,4), D: (4,6), E: (5,3), F: (6,4), G: (7,3),

|    |   | A | B | C | D | E | F | G |
|----|---|---|---|---|---|---|---|---|
| c1 | A | 0 | 1 | 5 | 8 | 6 | 8 | 8 |
| c2 | B | 1 | 0 |   |   |   |   |   |
| c3 | C | 5 |   | 0 |   |   |   |   |
| c4 | D | 8 |   |   | 0 |   |   |   |
| c5 | E | 6 |   |   |   | 0 |   |   |
| c6 | F | 8 |   |   |   |   | 0 |   |
| c7 | G | 8 |   |   |   |   |   | 0 |

$\text{dist}(A,B) = |1-2| + |1-1| = 1$   
 $\text{dist}(A,C) = |1-3| + |1-4| = 5$   
 $\text{dist}(A,D) = |1-4| + |1-6| = 8$   
 $\text{dist}(A,E) = |1-5| + |1-3| = 6$   
 $\text{dist}(A,F) = |1-6| + |1-4| = 8$   
 $\text{dist}(A,G) = |1-7| + |1-3| = 8$

Manhattan: 
$$d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$$

```

graph TD
    Inicio([Inicio]) --> Entrada[/Objetos e seus atributos/]
    Entrada --> SetaObjeto[Seta Objeto como Cluster]
    SetaObjeto --> CalculaMatriz[Calcula matriz de distancias]
    CalculaMatriz --> Decisao{Nro de cluster = 1}
    Decisao -- Sim --> Fim([Fim])
    Decisao -- Nao --> UneClusters[Une dois clusters proximos]
    UneClusters --> AtualizaMatriz[Atualiza Matriz de distancias]
    AtualizaMatriz --> Decisao
  
```

The flowchart illustrates the iterative process of hierarchical clustering. It begins with 'Inicio' (Start), followed by 'Objetos e seus atributos' (Objects and their attributes). The process then sets each object as a cluster ('Seta Objeto como Cluster') and calculates a distance matrix ('Calcula matriz de distancias'). A decision diamond checks if the number of clusters is 1. If 'Sim' (Yes), it ends at 'Fim' (End). If 'Nao' (No), it merges the two closest clusters ('Une dois clusters proximos') and updates the distance matrix ('Atualiza Matriz de distancias'), looping back to the decision point.

Flowchart of Hierarchical Clustering process

{25}------------------------------------------------

# Agrupamento Hierárquico

Exemplo:

- Considere os objetos (pontos):

A : (1,1), B: (2,1), C: (3,4), D: (4,6), E: (5,3), F: (6,4), G: (7,3),

|    |   | A | B | C | D | E | F | G |
|----|---|---|---|---|---|---|---|---|
| C1 | A | 0 | 1 | 5 | 8 | 6 | 8 | 8 |
| C2 | B | 1 | 0 | 4 | 7 | 5 | 7 | 7 |
| C3 | C | 5 | 4 | 0 |   |   |   |   |
| C4 | D | 8 | 7 |   | 0 |   |   |   |
| C5 | E | 6 | 5 |   |   | 0 |   |   |
| C6 | F | 8 | 7 |   |   |   | 0 |   |
| C7 | G | 8 | 7 |   |   |   |   | 0 |

$\text{dist}(B,C) = |2-3| + |1-4| = 4$   
 $\text{dist}(B,D) = |2-4| + |1-6| = 7$   
 $\text{dist}(B,E) = |2-5| + |1-3| = 5$   
 $\text{dist}(B,F) = |2-6| + |1-4| = 7$   
 $\text{dist}(B,G) = |2-7| + |1-3| = 7$

Manhattan: 
$$d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$$

```
graph TD; Inicio([Inicio]) --> Entrada[/Objetos e seus atributos/]; Entrada --> SetaObjeto[Seta Objeto como Cluster]; SetaObjeto --> CalculaMatriz[Calcula matriz de distancias]; CalculaMatriz --> Decisao{Nro de cluster = 1}; Decisao -- Sim --> Fim([Fim]); Decisao -- Nao --> UneClusters[Une dois clusters proximos]; UneClusters --> AtualizaMatriz[Atualiza Matriz de distancias]; AtualizaMatriz --> Decisao;
```

The flowchart illustrates the iterative process of hierarchical clustering. It begins with 'Inicio' (Start), followed by 'Objetos e seus atributos' (Objects and their attributes). The process then sets each object as a cluster ('Seta Objeto como Cluster') and calculates a distance matrix ('Calcula matriz de distancias'). A decision is made on whether the number of clusters is 1. If 'Sim' (Yes), the process ends ('Fim'). If 'Nao' (No), two closest clusters are merged ('Une dois clusters proximos'), the distance matrix is updated ('Atualiza Matriz de distancias'), and the decision is repeated.

Flowchart of Hierarchical Clustering process

{26}------------------------------------------------

# Agrupamento Hierárquico

Exemplo:

- Considere os objetos (pontos):

A : (1,1), B: (2,1), C: (3,4), D: (4,6), E: (5,3), F: (6,4), G: (7,3),

|    |   | A | B | C | D | E | F | G |
|----|---|---|---|---|---|---|---|---|
| C1 | A | 0 | 1 | 5 | 8 | 6 | 8 | 8 |
| C2 | B | 1 | 0 | 4 | 7 | 5 | 7 | 7 |
| C3 | C | 5 | 4 | 0 | 3 | 3 | 3 | 5 |
| C4 | D | 8 | 7 | 3 | 0 |   |   |   |
| C5 | E | 6 | 5 | 3 |   | 0 |   |   |
| C6 | F | 8 | 7 | 3 |   |   | 0 |   |
| C7 | G | 8 | 7 | 5 |   |   |   | 0 |

$$\begin{aligned} \text{dist}(C,D) &= |3-4| + |4-6| = 3 \\ \text{dist}(C,E) &= |3-5| + |4-3| = 3 \\ \text{dist}(C,F) &= |3-6| + |4-4| = 3 \\ \text{dist}(C,G) &= |3-7| + |4-3| = 5 \end{aligned}$$

$$\text{Manhattan: } d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$$

```
graph TD; Inicio([Inicio]) --> Entrada[/Objetos e seus atributos/]; Entrada --> SetaObjeto[Seta Objeto como Cluster]; SetaObjeto --> CalculaMatriz[Calcula matriz de distancias]; CalculaMatriz --> Decisao{Nro de cluster = 1}; Decisao -- Sim --> Fim([Fim]); Decisao -- Nao --> UneClusters[Une dois clusters proximos]; UneClusters --> AtualizaMatriz[Atualiza Matriz de distancias]; AtualizaMatriz --> Decisao;
```

The flowchart illustrates the iterative process of hierarchical clustering. It begins with 'Inicio' (Start), followed by 'Objetos e seus atributos' (Objects and their attributes). The process then sets each object as a cluster ('Seta Objeto como Cluster') and calculates a distance matrix ('Calcula matriz de distancias'). A decision diamond checks if the number of clusters is 1. If 'Sim' (Yes), it ends at 'Fim' (End). If 'Nao' (No), it merges the two closest clusters ('Une dois clusters proximos') and updates the distance matrix ('Atualiza Matriz de distancias'), looping back to the decision point.

Flowchart of Hierarchical Clustering process

{27}------------------------------------------------

# Agrupamento Hierárquico

Exemplo:

- Considere os objetos (pontos):

A : (1,1), B: (2,1), C: (3,4), D: (4,6), E: (5,3), F: (6,4), G: (7,3),

|    |   | A | B | C | D | E | F | G |
|----|---|---|---|---|---|---|---|---|
| c1 | A | 0 | 1 | 5 | 8 | 6 | 8 | 8 |
| c2 | B | 1 | 0 | 4 | 7 | 5 | 7 | 7 |
| c3 | C | 5 | 4 | 0 | 3 | 3 | 3 | 5 |
| c4 | D | 8 | 7 | 3 | 0 | 4 | 4 | 6 |
| c5 | E | 6 | 5 | 3 | 4 | 0 |   |   |
| c6 | F | 8 | 7 | 3 | 4 |   | 0 |   |
| c7 | G | 8 | 7 | 5 | 6 |   |   | 0 |

$$\begin{aligned} \text{dist}(D,E) &= |4-5| + |6-3| = 4 \\ \text{dist}(D,F) &= |4-6| + |6-4| = 4 \\ \text{dist}(D,G) &= |4-7| + |6-3| = 6 \end{aligned}$$

$$\text{Manhattan: } d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$$

```
graph TD; Inicio([Inicio]) --> Entrada[/Objetos e seus atributos/]; Entrada --> SetaObjeto[Seta Objeto como Cluster]; SetaObjeto --> CalculaMatriz[Calcula matriz de distancias]; CalculaMatriz --> Decisão{Nro de cluster = 1}; Decisão -- Sim --> Fim([Fim]); Decisão -- Nao --> UneClusters[Une dois clusters proximos]; UneClusters --> AtualizaMatriz[Atualiza Matriz de distancias]; AtualizaMatriz --> Decisão;
```

The flowchart illustrates the iterative process of hierarchical clustering. It begins with 'Inicio' (Start), followed by 'Objetos e seus atributos' (Objects and their attributes). The next step is 'Seta Objeto como Cluster' (Set Object as Cluster). Then, 'Calcula matriz de distancias' (Calculate distance matrix) is performed. A decision diamond asks 'Nro de cluster = 1' (Number of clusters = 1). If 'Sim' (Yes), the process ends at 'Fim' (End). If 'Nao' (No), the process proceeds to 'Une dois clusters proximos' (Merge two closest clusters), then 'Atualiza Matriz de distancias' (Update distance matrix), and loops back to the decision diamond.

Flowchart of Hierarchical Clustering process

{28}------------------------------------------------

# Agrupamento Hierárquico

Exemplo:

- Considere os objetos (pontos):

A : (1,1), B: (2,1), C: (3,4), D: (4,6), E: (5,3), F: (6,4), G: (7,3),

|    |   | A | B | C | D | E | F | G |
|----|---|---|---|---|---|---|---|---|
| c1 | A | 0 | 1 | 5 | 8 | 6 | 8 | 8 |
| c2 | B | 1 | 0 | 4 | 7 | 5 | 7 | 7 |
| c3 | C | 5 | 4 | 0 | 3 | 3 | 3 | 5 |
| c4 | D | 8 | 7 | 3 | 0 | 4 | 4 | 6 |
| c5 | E | 6 | 5 | 3 | 4 | 0 | 2 | 2 |
| c6 | F | 8 | 7 | 3 | 4 | 2 | 0 |   |
| c7 | G | 8 | 7 | 5 | 6 | 2 |   | 0 |

$$\begin{aligned} \text{dist}(E,F) &= |5-6| + |3-4| = 2 \\ \text{dist}(E,G) &= |5-7| + |3-3| = 2 \end{aligned}$$

$$\text{Manhattan: } d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$$

```
graph TD; Inicio([Inicio]) --> Entrada[/Objetos e seus atributos/]; Entrada --> Seta[Seta Objeto como Cluster]; Seta --> Calcula[Calcula matriz de distancias]; Calcula --> Decidao{Nro de cluster = 1}; Decidao -- Sim --> Fim([Fim]); Decidao -- Nao --> Une[Une dois clusters proximos]; Une --> Atualiza[Atualiza Matriz de distancias]; Atualiza --> Decidao;
```

The flowchart illustrates the iterative process of hierarchical clustering. It begins with 'Inicio' (Start), followed by 'Objetos e seus atributos' (Objects and their attributes). The next step is 'Seta Objeto como Cluster' (Set object as cluster). Then, 'Calcula matriz de distancias' (Calculate distance matrix) is performed. A decision diamond asks 'Nro de cluster = 1' (Number of clusters = 1). If 'Sim' (Yes), the process ends at 'Fim' (End). If 'Nao' (No), the process proceeds to 'Une dois clusters proximos' (Merge two closest clusters), then 'Atualiza Matriz de distancias' (Update distance matrix), and loops back to the decision diamond.

Flowchart of Hierarchical Clustering process

{29}------------------------------------------------

# Agrupamento Hierárquico

Exemplo:

- Considere os objetos (pontos):

A : (1,1), B: (2,1), C: (3,4), D: (4,6), E: (5,3), F: (6,4), G: (7,3),

|   | A | B | C | D | E | F | G |
|---|---|---|---|---|---|---|---|
| A | 0 | 1 | 5 | 8 | 6 | 8 | 8 |
| B | 1 | 0 | 4 | 7 | 5 | 7 | 7 |
| C | 5 | 4 | 0 | 3 | 3 | 3 | 5 |
| D | 8 | 7 | 3 | 0 | 4 | 4 | 6 |
| E | 6 | 5 | 3 | 4 | 0 | 2 | 2 |
| F | 8 | 7 | 3 | 4 | 2 | 0 | 2 |
| G | 8 | 7 | 5 | 6 | 2 | 2 | 0 |

$$\text{dist}(F,G) = |6-7| + |4-3| = 2$$

$$\text{Manhattan: } d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$$

```
graph TD; Inicio([Inicio]) --> Entrada[/Objetos e seus atributos/]; Entrada --> SetaObjeto[Seta Objeto como Cluster]; SetaObjeto --> CalculaMatriz[Calcula matriz de distancias]; CalculaMatriz --> Decisao{Nro de cluster = 1}; Decisao -- Sim --> Fim([Fim]); Decisao -- Nao --> UneClusters[Une dois clusters proximos]; UneClusters --> AtualizaMatriz[Atualiza Matriz de distancias]; AtualizaMatriz --> Decisao;
```

The flowchart illustrates the iterative process of hierarchical clustering. It begins with 'Inicio' (Start), followed by 'Objetos e seus atributos' (Objects and their attributes). The process then sets each object as a cluster ('Seta Objeto como Cluster') and calculates a distance matrix ('Calcula matriz de distancias'). A decision is made on whether the number of clusters is 1. If 'Sim' (Yes), the process ends at 'Fim' (End). If 'Nao' (No), the two closest clusters are merged ('Une dois clusters proximos'), the distance matrix is updated ('Atualiza Matriz de distancias'), and the decision is repeated.

Flowchart of Hierarchical Clustering process

{30}------------------------------------------------

# Agrupamento Hierárquico

Exemplo:

- Considere os objetos (pontos):

A : (1,1), B: (2,1), C: (3,4), D: (4,6), E: (5,3), F: (6,4), G: (7,3),

|   | A | B | C | D | E | F | G |
|---|---|---|---|---|---|---|---|
| A | 0 | 1 | 5 | 8 | 6 | 8 | 8 |
| B | 1 | 0 | 4 | 7 | 5 | 7 | 7 |
| C | 5 | 4 | 0 | 3 | 3 | 3 | 5 |
| D | 8 | 7 | 3 | 0 | 4 | 4 | 6 |
| E | 6 | 5 | 3 | 4 | 0 | 2 | 2 |
| F | 8 | 7 | 3 | 4 | 2 | 0 | 2 |
| G | 8 | 7 | 5 | 6 | 2 | 2 | 0 |

Manhattan:  $d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$

```
graph TD; Inicio([Inicio]) --> Entrada[/Objetos e seus atributos/]; Entrada --> SetaObjeto[Seta Objeto como Cluster]; SetaObjeto --> CalculaMatriz[Calcula matriz de distancias]; CalculaMatriz --> Decidao{Nro de cluster = 1}; Decidao -- Sim --> Fim([Fim]); Decidao -- Nao --> UneClusters[Une dois clusters proximos]; UneClusters --> AtualizaMatriz[Atualiza Matriz de distancias]; AtualizaMatriz --> Decidao;
```

The flowchart illustrates the iterative process of hierarchical clustering. It begins with 'Inicio' (Start), followed by 'Objetos e seus atributos' (Objects and their attributes). The process then sets each object as a cluster ('Seta Objeto como Cluster') and calculates a distance matrix ('Calcula matriz de distancias'). A decision diamond checks if the number of clusters is 1. If 'Sim' (Yes), it ends at 'Fim' (End). If 'Nao' (No), it merges the two closest clusters ('Une dois clusters proximos') and updates the distance matrix ('Atualiza Matriz de distancias'), looping back to the decision point.

Flowchart of Hierarchical Clustering process

{31}------------------------------------------------

# Agrupamento Hierárquico

Exemplo:

- Considere os objetos (pontos):

A : (1,1), B: (2,1), C: (3,4), D: (4,6), E: (5,3), F: (6,4), G: (7,3),

|   | A | B | C | D | E | F | G |
|---|---|---|---|---|---|---|---|
| A | 0 | 1 | 5 | 8 | 6 | 8 | 8 |
| B | 1 | 0 | 4 | 7 | 5 | 7 | 7 |
| C | 5 | 4 | 0 | 3 | 3 | 3 | 5 |
| D | 8 | 7 | 3 | 0 | 4 | 4 | 6 |
| E | 6 | 5 | 3 | 4 | 0 | 2 | 2 |
| F | 8 | 7 | 3 | 4 | 2 | 0 | 1 |
| G | 8 | 7 | 5 | 6 | 2 | 1 | 0 |

Manhattan:  $d(x_i, x_j) = \sum_{l=1}^d |x_i^l - x_j^l|$

```
graph TD; Inicio([Inicio]) --> Entrada[/Objetos e seus atributos/]; Entrada --> SetaObjeto[Seta Objeto como Cluster]; SetaObjeto --> CalculaMatriz[Calcula matriz de distancias]; CalculaMatriz --> Decisao{Nro de cluster = 1}; Decisao -- Sim --> Fim([Fim]); Decisao -- Nao --> UneClusters[Une dois clusters proximos]; UneClusters --> AtualizaMatriz[Atualiza Matriz de distancias]; AtualizaMatriz --> Decisao;
```

The flowchart illustrates the iterative process of hierarchical clustering. It begins with 'Inicio' (Start), followed by 'Objetos e seus atributos' (Objects and their attributes). The process then sets each object as a cluster ('Seta Objeto como Cluster') and calculates a distance matrix ('Calcula matriz de distancias'). A decision diamond checks if the number of clusters is 1. If 'Sim' (Yes), it ends at 'Fim' (End). If 'Nao' (No), it merges the two closest clusters ('Une dois clusters proximos') and updates the distance matrix ('Atualiza Matriz de distancias'), looping back to the decision diamond.

Flowchart of Hierarchical Clustering process

{32}------------------------------------------------

# Agrupamento Hierárquico

Exemplo:

|   | A | B | C | D | E | F | G |
|---|---|---|---|---|---|---|---|
| A | 0 | 1 | 5 | 8 | 6 | 8 | 8 |
| B | 1 | 0 | 4 | 7 | 5 | 7 | 7 |
| C | 5 | 4 | 0 | 3 | 3 | 3 | 5 |
| D | 8 | 7 | 3 | 0 | 4 | 4 | 6 |
| E | 6 | 5 | 3 | 4 | 0 | 2 | 2 |
| F | 8 | 7 | 3 | 4 | 2 | 0 | 2 |
| G | 8 | 7 | 5 | 6 | 2 | 2 | 0 |

The diagram illustrates the first step of hierarchical clustering. At the bottom, seven individual data points are listed as clusters: C1 (A(1,1)), C2 (B(2,1)), C3 (C(3,4)), C4 (D(4,6)), C5 (E(5,3)), C6 (F(6,4)), and C7 (G(7,3)). Above C1 and C2, a new cluster is formed, represented by a dark blue box containing the coordinates A(1,1), B(2,1). Two lines connect this new cluster box to the boxes for C1 and C2, indicating their merger.

Diagram of hierarchical clustering showing the first step where clusters A and B are merged.

Une dois clusters proximos

A,B -> distancia =1

Metrica de integracao =  
menor distancia

{33}------------------------------------------------

# Agrupamento Hierárquico

Exemplo:

|   | A | B | C | D | E | F | G |
|---|---|---|---|---|---|---|---|
| A | 0 | 1 | 5 | 8 | 6 | 8 | 8 |
| B | 1 | 0 | 4 | 7 | 5 | 7 | 7 |
| C | 5 | 4 | 0 | 3 | 3 | 3 | 5 |
| D | 8 | 7 | 3 | 0 | 4 | 4 | 6 |
| E | 6 | 5 | 3 | 4 | 0 | 2 | 2 |
| F | 8 | 7 | 3 | 4 | 2 | 0 | 2 |
| G | 8 | 7 | 5 | 6 | 2 | 2 | 0 |

Une dois clusters proximos

E,F -> distancia =2

```
graph TD; A1["A(1,1), B(2,1)"] --- A1_1["A(1,1)"]; A1 --- A1_2["B(2,1)"]; E2["E(5,3), F(6,4)"] --- E2_1["E(5,3)"]; E2 --- E2_2["F(6,4)"]; C1["C1"] --- A1_1; C2["C2"] --- A1_2; C3["C3"] --- C3_1["C(3,4)"]; C4["C4"] --- C4_1["D(4,6)"]; C5["C5"] --- E2_1; C6["C6"] --- E2_2; C7["C7"] --- C7_1["G(7,3)"];
```

Diagram of hierarchical clustering showing two clusters being merged. The left cluster contains nodes A(1,1) and B(2,1), which are connected to a parent node labeled A(1,1), B(2,1). The right cluster contains nodes E(5,3) and F(6,4), which are connected to a parent node labeled E(5,3), F(6,4). Below these are seven individual nodes labeled C1 through C7 with coordinates: C1(A(1,1)), C2(B(2,1)), C3(C(3,4)), C4(D(4,6)), C5(E(5,3)), C6(F(6,4)), and C7(G(7,3)).

{34}------------------------------------------------

# Agrupamento Hierárquico

Exemplo:

|   | A | B | C | D | E | F | G |
|---|---|---|---|---|---|---|---|
| A | 0 | 1 | 5 | 8 | 6 | 8 | 8 |
| B | 1 | 0 | 4 | 7 | 5 | 7 | 7 |
| C | 5 | 4 | 0 | 3 | 3 | 3 | 5 |
| D | 8 | 7 | 3 | 0 | 4 | 4 | 6 |
| E | 6 | 5 | 3 | 4 | 0 | 2 | 2 |
| F | 8 | 7 | 3 | 4 | 2 | 0 | 2 |
| G | 8 | 7 | 5 | 6 | 2 | 2 | 0 |

Une dois clusters proximos

G

```
graph TD; AB["A(1,1), B(2,1)"] --- A1["A(1,1)"]; AB --- B1["B(2,1)"]; EF["E(5,3), F(6,4)"] --- E1["E(5,3)"]; EF --- F1["F(6,4)"]; C["C(3,4)"]; D["D(4,6)"]; G["G(7,3)"]; A1 --- C1["C1"]; B1 --- C2["C2"]; E1 --- C5["C5"]; F1 --- C6["C6"]; C --- C3["C3"]; D --- C4["C4"]; G --- C7["C7"];
```

The diagram illustrates a hierarchical clustering process. At the top, two clusters are shown: one containing nodes A(1,1) and B(2,1), and another containing nodes E(5,3) and F(6,4). These clusters are connected to a horizontal line representing the next level of the hierarchy. Below this line, seven individual nodes are listed: A(1,1), B(2,1), C(3,4), D(4,6), E(5,3), F(6,4), and G(7,3). Each node is associated with a label below it: C1, C2, C3, C4, C5, C6, and C7 respectively. The nodes A(1,1) and B(2,1) are connected to C1 and C2. The nodes E(5,3) and F(6,4) are connected to C5 and C6. The nodes C(3,4), D(4,6), and G(7,3) are connected to C3, C4, and C7 respectively.

Hierarchical clustering diagram showing the merging of clusters A and B, and E and F, with individual nodes C, D, and G.

{35}------------------------------------------------

# Agrupamento Hierárquico

Exemplo:

|   | A | B | C | D | E | F | G |
|---|---|---|---|---|---|---|---|
| A | 0 | 1 | 5 | 8 | 6 | 8 | 8 |
| B | 1 | 0 | 4 | 7 | 5 | 7 | 7 |
| C | 5 | 4 | 0 | 3 | 3 | 3 | 5 |
| D | 8 | 7 | 3 | 0 | 4 | 4 | 6 |
| E | 6 | 5 | 3 | 4 | 0 | 2 | 2 |
| F | 8 | 7 | 3 | 4 | 2 | 0 | 2 |
| G | 8 | 7 | 5 | 6 | 2 | 2 | 0 |

Une dois clusters proximos

C,D -> distancia =3

The diagram illustrates the hierarchical clustering process. It shows three clusters at the top, each containing two data points with their coordinates (x,y):

- Cluster 1: A(1,1), B(2,1)
- Cluster 2: C(3,4), D(4,6)
- Cluster 3: E(5,3), F(6,4)

Below each cluster, the individual data points are listed with their coordinates and a label (C1 through C7):

- C1: A(1,1)
- C2: B(2,1)
- C3: C(3,4)
- C4: D(4,6)
- C5: E(5,3)
- C6: F(6,4)
- C7: G(7,3)

Diagram of hierarchical clustering showing three clusters: {A(1,1), B(2,1)}, {C(3,4), D(4,6)}, and {E(5,3), F(6,4)}. Below each cluster are the individual data points with their coordinates, labeled C1 through C7.

{36}------------------------------------------------

# Agrupamento Hierárquico

Exemplo:

$$C8 = ( (1+2)/2, (1+1)/2 ) = (1.5, 1)$$

$$C9 = ( (3+4)/2, (4+6)/2 ) = (3.5, 5)$$

$$C10 = ( (5+6)/2, (3+4)/2 ) = (5.5, 3.5)$$

Diagram illustrating the hierarchical clustering process. The clusters are defined as follows:

- C8 (1.5, 1) contains A(1,1) and B(2,1).
- C9 (3.5, 5) contains C(3,4) and D(4,6).
- C10 (5.5, 3.5) contains E(5,3) and F(6,4).

The objects are labeled C1 through C7, corresponding to A(1,1), B(2,1), C(3,4), D(4,6), E(5,3), F(6,4), and G(7,3) respectively.

Diagram showing the hierarchical clustering process. It starts with three clusters: C8 (1.5, 1) containing A(1,1) and B(2,1); C9 (3.5, 5) containing C(3,4) and D(4,6); and C10 (5.5, 3.5) containing E(5,3) and F(6,4). Below these are the individual objects C1 through C7, with G(7,3) being the remaining unclustered object.

```
graph TD; Inicio([Inicio]) --> Input[/Objetos e seus atributos/]; Input --> SetCluster[Seta Objeto como Cluster]; SetCluster --> CalcDist[Calcula matriz de distancias]; CalcDist --> Decision{Nro de cluster = 1}; Decision -- Sim --> Fim([Fim]); Decision -- Nao --> Merge[Une dois clusters proximos]; Merge --> UpdateDist[Atualiza Matriz de distancias]; UpdateDist --> Decision;
```

Flowchart of the hierarchical clustering algorithm. It starts with 'Inicio', followed by 'Objetos e seus atributos', 'Seta Objeto como Cluster', and 'Calcula matriz de distancias'. A decision diamond asks 'Nro de cluster = 1'. If 'Sim', it goes to 'Fim'. If 'Nao', it goes to 'Une dois clusters proximos', then 'Atualiza Matriz de distancias', and loops back to the decision diamond.

{37}------------------------------------------------

# Agrupamento Hierárquico

Exemplo:

|               | C8 (1.5,1) | C9 (3.5, 5) | C10 (5.5,3.5) | C7 (7,3) |
|---------------|------------|-------------|---------------|----------|
| C8 (1.5,1)    | 0          |             |               |          |
| C9 (3.5, 5)   |            | 0           |               |          |
| C10 (5.5,3.5) |            |             | 0             |          |
| C7 (7,3)      |            |             |               | 0        |

Diagram illustrating the initial clustering of objects into three clusters:

- Cluster C8 (1.5, 1) contains objects A(1,1) and B(2,1).
- Cluster C9 (3.5, 5) contains objects C(3,4) and D(4,6).
- Cluster C10 (5.5, 3.5) contains objects E(5,3) and F(6,4).

Objects A(1,1), B(2,1), C(3,4), D(4,6), E(5,3), F(6,4), and G(7,3) are labeled as C1 through C7 respectively.

Diagram showing the initial clustering of objects into three clusters: C8, C9, and C10. C8 contains A(1,1) and B(2,1). C9 contains C(3,4) and D(4,6). C10 contains E(5,3) and F(6,4). Object G(7,3) is not yet assigned to any cluster.

```
graph TD; Inicio([Inicio]) --> Entrada[/Objetos e seus atributos/]; Entrada --> SetaObjeto[Seta Objeto como Cluster]; SetaObjeto --> CalculaMatriz[Calcula matriz de distancias]; CalculaMatriz --> Decidao{Nro de cluster = 1}; Decidao -- Sim --> Fim([Fim]); Decidao -- Nao --> UneClusters[Une dois clusters proximos]; UneClusters --> AtualizaMatriz[Atualiza Matriz de distancias]; AtualizaMatriz --> Decidao;
```

Flowchart illustrating the hierarchical clustering process:

- Inicio
- Objetos e seus atributos
- Seta Objeto como Cluster
- Calcula matriz de distancias
- Decision: Nro de cluster = 1
  - If Sim: Fim
  - If Nao: Une dois clusters proximos
- Une dois clusters proximos
- Atualiza Matriz de distancias
- Loop back to Decision

Flowchart of the hierarchical clustering algorithm.

{38}------------------------------------------------

# Agrupamento Hierárquico

Exemplo:

$\text{dist}(C8,C9) = |1.5-3.5| + |1-5| = 6$   
 $\text{dist}(C8,C10) = |1.5-5.5| + |1-3.5| = 6.5$   
 $\text{dist}(C8,C7) = |1.5-7| + |1-3| = 7.5$

|               | C8 (1.5,1) | C9 (3.5, 5) | C10 (5.5,3.5) | C7 (7,3) |
|---------------|------------|-------------|---------------|----------|
| C8 (1.5,1)    | 0          | 6           | 6.5           | 7.5      |
| C9 (3.5, 5)   | 6          | 0           |               |          |
| C10 (5.5,3.5) | 6.5        |             | 0             |          |
| C7 (7,3)      | 7.5        |             |               | 0        |

Atualiza Matriz de  
distancias

The diagram illustrates a hierarchical clustering process. At the top, three clusters are shown, each in a blue rounded rectangle:

- Cluster 1: C8 (1.5, 1) containing A(1,1) and B(2,1)
- Cluster 2: C9 (3.5, 5) containing C(3,4) and D(4,6)
- Cluster 3: C10 (5.5, 3.5) containing E(5,3) and F(6,4)

Below these, the individual data points are listed in blue rounded rectangles, each with a label C1 through C7 underneath:

- A(1,1) labeled C1
- B(2,1) labeled C2
- C(3,4) labeled C3
- D(4,6) labeled C4
- E(5,3) labeled C5
- F(6,4) labeled C6
- G(7,3) labeled C7

Blue lines connect the parent clusters to their constituent data points, showing the merging process.

Hierarchical clustering diagram showing three clusters merging into a single structure.

{39}------------------------------------------------

# Agrupamento Hierárquico

Exemplo:

$\text{dist}(C9,C10) = |3.5-5.5| + |5-3.5| = 3.5$   
 $\text{dist}(C9,C7) = |3.5-7| + |5-3| = 5.5$

|               | C8 (1.5,1) | C9 (3.5, 5) | C10 (5.5,3.5) | C7 (7,3) |
|---------------|------------|-------------|---------------|----------|
| C8 (1.5,1)    | 0          | 6           | 6.5           | 7.5      |
| C9 (3.5, 5)   | 6          | 0           | 3.5           | 5.5      |
| C10 (5.5,3.5) | 6.5        | 3.5         | 0             |          |
| C7 (7,3)      | 7.5        | 5.5         |               | 0        |

Atualiza Matriz de  
distancias

The diagram illustrates a hierarchical clustering process. At the top level, three clusters are shown: C8 (1.5, 1), C9 (3.5, 5), and C10 (5.5, 3.5). Each cluster is represented by a blue rounded rectangle containing its coordinates and the coordinates of its constituent points. C8 contains points A(1,1) and B(2,1). C9 contains points C(3,4) and D(4,6). C10 contains points E(5,3) and F(6,4). Below these clusters, the individual points are listed as leaf nodes: C1 (A(1,1)), C2 (B(2,1)), C3 (C(3,4)), C4 (D(4,6)), C5 (E(5,3)), C6 (F(6,4)), and C7 (G(7,3)). Lines connect the parent clusters to their respective leaf nodes, showing the hierarchical structure.

Hierarchical clustering diagram showing the merging of clusters C8, C9, and C10 into a single structure, with leaf nodes C1 through C7.

<!-- DATALAB_CHUNK 3: pages 41-59 -->

{40}------------------------------------------------

# Agrupamento Hierárquico

Exemplo:

$\text{dist}(C_{10}, C_7) = |5.5 - 7| + |3.5 - 3| = 2$

|               | C8 (1.5,1) | C9 (3.5, 5) | C10 (5.5,3.5) | C7 (7,3) |
|---------------|------------|-------------|---------------|----------|
| C8 (1.5,1)    | 0          | 6           | 6.5           | 7.5      |
| C9 (3.5, 5)   | 6          | 0           | 3.5           | 5.5      |
| C10 (5.5,3.5) | 6.5        | 3.5         | 0             | 2        |
| C7 (7,3)      | 7.5        | 5.5         | 2             | 0        |

Atualiza Matriz de  
distancias

The diagram illustrates a hierarchical clustering process. At the top level, three clusters are shown: C8 (1.5, 1), C9 (3.5, 5), and C10 (5.5, 3.5). Each of these clusters is represented by a blue rounded rectangle containing the coordinates of its constituent points. C8 contains A(1,1) and B(2,1); C9 contains C(3,4) and D(4,6); and C10 contains E(5,3) and F(6,4). Lines connect each of these top-level clusters to a corresponding pair of leaf nodes at the bottom. The leaf nodes are labeled C1 through C7. C1 and C2 correspond to A(1,1) and B(2,1) respectively, under the C8 cluster. C3 and C4 correspond to C(3,4) and D(4,6) respectively, under the C9 cluster. C5 and C6 correspond to E(5,3) and F(6,4) respectively, under the C10 cluster. C7 (7,3) is shown as a single leaf node without a parent cluster above it.

Hierarchical clustering diagram showing the merging of clusters C8, C9, and C10 into a larger structure, with C7 remaining separate.

{41}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-c5655e700cc3e9aac7e9f4f07f30264d_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram illustrating similarity between two clusters.
<!-- /IMAGE_DESCRIPTION -->
## Agrupamento Hierárquico

Exemplo:

$$C_{11} = ((5+6+7)/3, (3+4+3)/3) = (6, 3.33)$$

|               | C8 (1.5,1) | C9 (3.5, 5) | C10 (5.5,3.5) | C7 (7,3) |
|---------------|------------|-------------|---------------|----------|
| C8 (1.5,1)    | 0          | 6           | 6.5           | 7.5      |
| C9 (3.5, 5)   | 6          | 0           | 3.5           | 5.5      |
| C10 (5.5,3.5) | 6.5        | 3.5         | 0             | 2        |
| C7 (7,3)      | 7.5        | 5.5         | 2             | 0        |

```

graph TD
    C8["C8 (1.5, 1)  
A(1,1), B(2,1)"] --- C1["C1  
A(1,1)"]
    C8 --- C2["C2  
B(2,1)"]
    C9["C9 (3.5, 5)  
C(3,4), D(4,6)"] --- C3["C3  
C(3,4)"]
    C9 --- C4["C4  
D(4,6)"]
    C10["C10 (5.5, 3.5)  
E(5,3), F(6,4)"] --- C5["C5  
E(5,3)"]
    C10 --- C6["C6  
F(6,4)"]
    C11["C11 (6, 3.33)  
E(5,3), F(6,4), G(7,3)"] --- C5
    C11 --- C6
    C11 --- C7["C7  
G(7,3)"]
  
```

The diagram illustrates the hierarchical clustering process. It shows three main clusters being merged into a final cluster C11. Cluster C8 (1.5, 1) contains points A(1,1) and B(2,1), which are labeled as C1 and C2 respectively. Cluster C9 (3.5, 5) contains points C(3,4) and D(4,6), labeled as C3 and C4. Cluster C10 (5.5, 3.5) contains points E(5,3) and F(6,4), labeled as C5 and C6. The final cluster C11 (6, 3.33) is formed by merging C10 and C7 (7,3), which contains point G(7,3). The diagram shows the parent cluster at the top and its children below it, with lines indicating the merging process.

Hierarchical clustering diagram showing the merging of clusters C8, C9, and C10 into C11.

```

graph TD
    Decision{"Nro de cluster = 1"}
    Decision -- Sim --> Fim[Fim]
    Decision -- Nao --> UneDoisClusters[Une dois clusters proximos]
    UneDoisClusters --> AtualizaMatriz[Atualiza Matriz de distancias]
    AtualizaMatriz --> Decision
  
```

The flowchart describes the iterative process of hierarchical clustering. It starts with a decision diamond: "Nro de cluster = 1". If the answer is "Sim" (Yes), the process ends at "Fim". If the answer is "Nao" (No), the process moves to a green box "Une dois clusters proximos" (Merge two closest clusters), then to another green box "Atualiza Matriz de distancias" (Update distance matrix), and then loops back to the decision diamond.

Flowchart for the hierarchical clustering algorithm.

{42}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-a4b963a07cc368283154762c4b156fe7_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of hierarchical clustering showing two clusters being merged.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-fcbc3c31776721edc98ceb1944ec438f_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of hierarchical clustering showing three clusters: {A(1,1), B(2,1)}, {C(3,4), D(4,6)}, and {E(5,3), F(6,4)}.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-6629e8a87e7552e2454b7c3e9f6d73a0_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram showing the initial clustering of objects into three clusters: C8, C9, and C10.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-34b047489058d6400b412cd0ae2334ba_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Hierarchical clustering diagram showing the merging of clusters C8, C9, and C10 into a larger structure, with C7 remaining separate.
<!-- /IMAGE_DESCRIPTION -->
## Agrupamento Hierárquico

Exemplo:

|             | C8 (1.5,1) | C9 (3.5, 5) | C11 (6,3.3) |
|-------------|------------|-------------|-------------|
| C8 (1.5,1)  | 0          |             |             |
| C9 (3.5, 5) |            | 0           |             |
| C11 (6,3.3) |            |             | 0           |

The diagram illustrates a hierarchical clustering process. At the bottom, seven individual data points are labeled C1 through C7, each with its coordinates: C1(1,1), C2(2,1), C3(3,4), C4(4,6), C5(5,3), C6(6,4), and C7(7,3). Above these, three clusters are shown: C8 (1.5, 1) containing A(1,1) and B(2,1); C9 (3.5, 5) containing C(3,4) and D(4,6); and C10 (5.5, 3.5) containing E(5,3) and F(6,4). At the top, a new cluster C11 (6, 3.33) is formed, which contains the coordinates of C8, C9, and C10, as well as the coordinates of E(5,3), F(6,4), and G(7,3). Lines connect the parent clusters to their constituent data points, and a line connects C11 to its constituent clusters.

Hierarchical clustering diagram showing the merging of clusters C8, C9, and C10 into C11.

Atualiza Matriz de  
distancias

{43}------------------------------------------------

# Agrupamento Hierárquico

Exemplo:

$\text{dist}(C8,C9) = |1.5-3.5| + |1-5| = 6$   
 $\text{dist}(C8,C11)= |1.5-6| + |1-3.33| = 6.83$

|             | C8 (1.5,1) | C9 (3.5, 5) | C11 (6,3.3) |
|-------------|------------|-------------|-------------|
| C8 (1.5,1)  | 0          | 6           | 6.83        |
| C9 (3.5, 5) | 6          | 0           |             |
| C11 (6,3.3) | 6.83       |             | 0           |

The diagram illustrates a hierarchical clustering process. At the bottom, seven individual data points are labeled C1 through C7. C1 is A(1,1) and C2 is B(2,1). C3 is C(3,4) and C4 is D(4,6). C5 is E(5,3), C6 is F(6,4), and C7 is G(7,3). Above these, three clusters are formed: C8 (1.5, 1) containing A(1,1) and B(2,1); C9 (3.5, 5) containing C(3,4) and D(4,6); and C10 (5.5, 3.5) containing E(5,3) and F(6,4). At the top, a new cluster C11 (6, 3.33) is formed by merging C10 and C7. The cluster C11 contains the elements E(5,3), F(6,4), and G(7,3). Lines connect the parent clusters to their constituent data points or sub-clusters.

Hierarchical clustering diagram showing the merging of clusters C8, C9, and C10 into C11.

Atualiza Matriz de  
distancias

{44}------------------------------------------------

# Agrupamento Hierárquico

Exemplo:

$\text{dist}(C9,C11)= |3.5-6| + |5-3.33| = 4.17$

|             | C8 (1.5,1) | C9 (3.5, 5) | C11 (6,3.3) |
|-------------|------------|-------------|-------------|
| C8 (1.5,1)  | 0          | 6           | 6.83        |
| C9 (3.5, 5) | 6          | 0           | 4.17        |
| C11 (6,3.3) | 6.83       | 4.17        | 0           |

The diagram illustrates the hierarchical clustering process. At the bottom, seven individual data points are labeled C1 through C7. C1 (A(1,1)) and C2 (B(2,1)) are merged into cluster C8 (1.5, 1). C3 (C(3,4)) and C4 (D(4,6)) are merged into cluster C9 (3.5, 5). C5 (E(5,3)) and C6 (F(6,4)) are merged into cluster C10 (5.5, 3.5). Finally, cluster C10 is merged with cluster C9 to form the new cluster C11 (6, 3.33), which contains the data points E(5,3), F(6,4), and G(7,3). The labels for the parent clusters (C8, C9, C10, C11) are placed above their respective boxes, while the leaf node labels (C1-C7) are placed below theirs.

Hierarchical clustering diagram showing the merging of clusters C8, C9, and C10 into C11.

Atualiza Matriz de distancias

{45}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-366a77fdefb0097b3289b4a011911390_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram showing 7 objects (C1 to C7) with their coordinates.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-0ee9d674085524d589646a6c3fb21ec3_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Hierarchical clustering diagram showing the merging of clusters A and B, and E and F, with individual nodes C, D, and G.
<!-- /IMAGE_DESCRIPTION -->
## Agrupamento Hierárquico

Exemplo:

$$C12 = ( (3+4+5+6+7)/5, (4+6+3+4+3)/5 ) = (5, 4)$$

|            | C8 (1.5,1) | C12 (5, 4) |
|------------|------------|------------|
| C8 (1.5,1) |            |            |
| C12 (5, 4) |            |            |

```

graph TD
    C1["C1  
A(1,1)"] --- C8["C8 (1.5, 1)  
A(1,1), B(2,1)"]
    C2["C2  
B(2,1)"] --- C8
    C3["C3  
C(3,4)"] --- C9["C9 (3.5, 5)  
C(3,4), D(4,6)"]
    C4["C4  
D(4,6)"] --- C9
    C5["C5  
E(5,3)"] --- C10["C10 (5.5, 3.5)  
E(5,3), F(6,4)"]
    C6["C6  
F(6,4)"] --- C10
    C7["C7  
G(7,3)"] --- C11["C11 (6, 3.33)  
E(5,3), F(6,4), G(7,3)"]
    C10 --- C11
    C8 --- C12["C12 (5, 4)  
C(3,4), D(4,6), E(5,3), F(6,4), G(7,3)"]
    C9 --- C12
    C11 --- C12
  
```

The diagram illustrates a hierarchical clustering process. At the bottom, individual data points are grouped into clusters C1 through C7. C1 and C2 merge into C8 (centroid 1.5, 1). C3 and C4 merge into C9 (centroid 3.5, 5). C5 and C6 merge into C10 (centroid 5.5, 3.5). C10 and C7 merge into C11 (centroid 6, 3.33). Finally, C8, C9, and C11 merge into the root cluster C12 (centroid 5, 4). Each cluster node contains the coordinates of its members.

Hierarchical clustering dendrogram showing the merging of clusters C1 through C7 into C12.

```

graph TD
    Decision{"Nro de cluster = 1"}
    Decision -- Sim --> Fim["Fim"]
    Decision -- Nao --> UneDoisClusters["Une dois clusters proximos"]
    UneDoisClusters --> AtualizaMatriz["Atualiza Matriz de distancias"]
    AtualizaMatriz --> Decision
  
```

The flowchart describes the iterative process of hierarchical clustering. It starts with a decision diamond: "Nro de cluster = 1". If the answer is "Sim" (Yes), the process ends at "Fim". If the answer is "Nao" (No), the process moves to a green box "Une dois clusters proximos" (Merge two closest clusters), then to another green box "Atualiza Matriz de distancias" (Update distance matrix), and loops back to the decision diamond.

Flowchart for the hierarchical clustering algorithm.

{46}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-d53cd0fd1cf896a9353fd63de1505ba2_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Flowchart of Hierarchical Clustering process
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-f0b7aaa539a2f77c98d53ed6c1c2366b_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Flowchart of Hierarchical Clustering process
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-ae53f90bb87d6d09e2d6b5278d7c338f_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Flowchart of the Hierarchical Clustering process.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-8d325fc12b494e42c9ea7ed2a7f327a6_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Flowchart of Hierarchical Clustering process
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-20136850feb70fd71c7d41cdae203ebb_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Flowchart of Hierarchical Clustering process
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-e29665b8abcea967ef289c6aff07ae4c_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Flowchart of Hierarchical Clustering process
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-805c475f0859e607af0530ba43194bf1_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Flowchart of Hierarchical Clustering process
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-55136bc716146672fc680fa05989f1d2_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Flowchart of Hierarchical Clustering process
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-24c9e038a791677ed33100667b64f7e6_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Flowchart of Hierarchical Clustering process
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-98e54d5540b2efe3e24af3cf936bc4ea_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Flowchart of Hierarchical Clustering process
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-a05e675f8651ae7ccea1d0d68691d1a9_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Flowchart of Hierarchical Clustering process
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-fb18a83d10ebdad8e3e5ea2e86b36136_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Flowchart of the hierarchical clustering algorithm.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-04cfca33e3fc26513abe649d7474f733_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Flowchart of the hierarchical clustering algorithm.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-e05122559f56af5699789b7118d8fe87_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Flowchart for the hierarchical clustering algorithm.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-a161a2bbb4d830e847ccb4f44b7e41a9_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Hierarchical clustering dendrogram showing the merging of clusters C1 through C7 into C12.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-b44f89b176c971c7dd264c07bfef2c2a_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Flowchart for the hierarchical clustering algorithm.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-41aef1f5efab13d4f38f69e86c726062_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Hierarchical clustering dendrogram showing the merging of clusters C1 through C7 into C13.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-683f755e8456c884716de4fce48c7e63_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Flowchart for the hierarchical clustering algorithm.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-b4b7023ccc81c5f4ebfd3ccb58361529_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Dendrogram showing hierarchical clustering of 7 data points.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-056f93110af61f80a3f9526f06423d44_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Dendrogram showing hierarchical clustering of 7 data points.
<!-- /IMAGE_DESCRIPTION -->
## Agrupamento Hierárquico

Exemplo:

```

graph TD
    C1["C1  
A(1,1)"] --- C8["C8 (1.5, 1)  
A(1,1), B(2,1)"]
    C2["C2  
B(2,1)"] --- C8
    C8 --- C13["C13 (4, 3.14)  
C(3,4), D(4,6), E(5,3), F(6,4), G(7,3)"]
    C3["C3  
C(3,4)"] --- C9["C9 (3.5, 5)  
C(3,4), D(4,6)"]
    C4["C4  
D(4,6)"] --- C9
    C9 --- C12["C12 (5, 4)  
C(3,4), D(4,6), E(5,3), F(6,4), G(7,3)"]
    C5["C5  
E(5,3)"] --- C10["C10 (5.5, 3.5)  
E(5,3), F(6,4)"]
    C6["C6  
F(6,4)"] --- C10
    C10 --- C11["C11 (6, 3.33)  
E(5,3), F(6,4), G(7,3)"]
    C7["C7  
G(7,3)"] --- C11
    C11 --- C12
    C12 --- C13
    
```

The diagram illustrates a hierarchical clustering process. It starts with seven individual data points (C1 to C7) at the bottom. C1 and C2 merge into cluster C8 (centroid 1.5, 1). C3 and C4 merge into cluster C9 (centroid 3.5, 5). C5 and C6 merge into cluster C10 (centroid 5.5, 3.5). Then, C8 and C9 merge into cluster C12 (centroid 5, 4). Next, C10 and C7 merge into cluster C11 (centroid 6, 3.33). Finally, C12 and C11 merge into the root cluster C13 (centroid 4, 3.14), which contains all seven data points.

Hierarchical clustering dendrogram showing the merging of clusters C1 through C7 into C13.

|            | C8 (1.5,1) | C12 (5, 4) |
|------------|------------|------------|
| C8 (1.5,1) | 0          | 6.5        |
| C12 (5, 4) | 6.5        | 0          |

$$\text{dist}(C8, C12) = |1.5 - 5| + |1 - 4| = 6.5$$

$$C13 = (28/7, 22/7) = (4, 3.14)$$

```

graph TD
    Decision{"Nro de cluster = 1"}
    Decision -- Sim --> Fim[Fim]
    Decision -- Nao --> Step1[Une dois clusters proximos]
    Step1 --> Step2[Atualiza Matriz de distancias]
    Step2 --> Decision
    
```

The flowchart describes the iterative process of hierarchical clustering. It begins with a decision diamond asking if the number of clusters is 1. If 'Sim' (Yes), the process ends at 'Fim'. If 'Nao' (No), it proceeds to a box labeled 'Une dois clusters proximos' (Merge two closest clusters), then to 'Atualiza Matriz de distancias' (Update distance matrix), and loops back to the decision diamond.

Flowchart for the hierarchical clustering algorithm.

{47}------------------------------------------------
## Agrupamento Hierárquico
#### Alguns algoritmos:

- **Single-link** : baseado na menor distância entre dois clusters  $C1$  e  $C2$  (usa os dados mais próximos, um de cada cluster)
- **Complete-Link**: baseado na maior distância entre dois clusters  $C1$  e  $C2$  (usa os dados mais afastados, um de cada cluster).

Diagram illustrating Single-link clustering. Two clusters, represented as irregular shapes, are shown. A yellow arrow connects the closest point in the left cluster to the closest point in the right cluster, indicating that the distance between these two points determines when the clusters merge.

Diagram illustrating Complete-link clustering. Two clusters, represented as irregular shapes, are shown. A yellow arrow connects the furthest point in the left cluster to the furthest point in the right cluster, indicating that the distance between these two points determines when the clusters merge.

{48}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-a003ffe7299e0a48bceb7f1e45a4f1a3_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram illustrating Single-link clustering.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-7fe5741e83bc9702d1b1d7585ddf66bd_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram illustrating Complete-link clustering.
<!-- /IMAGE_DESCRIPTION -->
## Agrupamento Hierárquico
#### Alguns algoritmos:

- **Average-link:** baseado na distância média entre dois clusters  $C1$  e  $C2$ .
- **Distance Between Centroids:** baseado na distância entre os centróides de dois clusters  $C1$  e  $C2$ .

The diagram shows two clusters, each represented by an irregular cloud shape containing several black dots representing data points. Numerous yellow lines connect every point in the left cluster to every point in the right cluster, forming a complete bipartite graph. This visualizes the calculation of the average distance between all pairs of points from the two clusters.

Diagram illustrating Average-link clustering.

The diagram shows two clusters, each represented by an irregular cloud shape containing several black dots. In the center of each cluster, there is a red 'x' mark representing the centroid. A single yellow line connects the two red 'x' marks, representing the distance between the centroids of the two clusters.

Diagram illustrating Distance Between Centroids clustering.

{49}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-8d66c9c295023a1380f9986d3663bb1e_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram illustrating Average-link clustering.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-0f1767577a073167eb9628d72034e083_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram illustrating Distance Between Centroids clustering.
<!-- /IMAGE_DESCRIPTION -->
## Agrupamento Hierárquico

Em geral, algoritmos hierárquicos não lidam bem com outliers e ruídos.
#### Analisando os algoritmos:

- **Single-link :**
  - Indicado para formas não elípticas
  - Sensível a ruídos e outliers
  - Favorece clusters finos e alongados.
- **Complete-Link:**
  - Menos suscetível a ruídos e outliers
  - Tende a quebrar clusters grandes
  - Tem problemas com formas convexas
  - Favorece clusters esféricos.

{50}------------------------------------------------
## Agrupamento Hierárquico

- **Scki-learn** : <https://scikit-learn.org/stable/modules/generated/sklearn.cluster.AgglomerativeClustering.html>
### `sklearn.cluster.AgglomerativeClustering`

```
class sklearn.cluster.AgglomerativeClustering(n_clusters=2, *, affinity='deprecated', metric=None, memory=None, connectivity=None, compute_full_tree='auto', linkage='ward', distance_threshold=None, compute_distances=False) \[source\]
```

Agglomerative Clustering.

Recursively merges pair of clusters of sample data; uses linkage distance.

Read more in the [User Guide](#).
#### Parameters:

**n\_clusters** : *int or None, default=2*

The number of clusters to find. It must be `None` if `distance_threshold` is not `None`.

**affinity** : *str or callable, default='euclidean'*

The metric to use when calculating distance between instances in a feature array. If metric is a string or callable, it must be one of the options allowed by `sklearn.metrics.pairwise_distances` for its metric parameter. If linkage is "ward", only "euclidean" is accepted. If "precomputed", a distance matrix (instead of a similarity matrix) is needed as input for the fit method.

*Deprecated since version 1.2:* `affinity` was deprecated in version 1.2 and will be renamed to `metric` in 1.4.

**metric** : *str or callable, default=None*

Metric used to compute the linkage. Can be "euclidean", "l1", "l2", "manhattan", "cosine", or "precomputed". If set to `None` then "euclidean" is used. If linkage is "ward", only "euclidean" is accepted. If "precomputed", a distance matrix is needed as input for the fit method.
#### Comentando alguns **parâmetros**:

- **n\_cluster**: valor inteiro (int) ou None (nenhum). Número de clusters a encontrar. O valor padrão é 2.
- **affinity**: não usar mais
- **metric**: str ou callable. Corresponde a métrica para calcular a distância entre os clusters. Pode ser: "euclidian", "manhattan", "cosine" e outros. Quando está como None, a distância "euclidian" é usada como padrão.

{51}------------------------------------------------
## Agrupamento Hierárquico

- **Scki-learn** : <https://scikit-learn.org/stable/modules/generated/sklearn.cluster.AgglomerativeClustering.html>
### sklearn.cluster.AgglomerativeClustering

```
class sklearn.cluster.AgglomerativeClustering(n_clusters=2, *, affinity='deprecated', metric=None, memory=None, connectivity=None, compute_full_tree='auto', linkage='ward', distance_threshold=None, compute_distances=False) \[source\]
```

Agglomerative Clustering.

Recursively merges pair of clusters of sample data; uses linkage distance.

Read more in the [User Guide](#).
#### Parameters:

**linkage** : {'ward', 'complete', 'average', 'single'}, default='ward'

Which linkage criterion to use. The linkage criterion determines which distance to use between sets of observation. The algorithm will merge the pairs of cluster that minimize this criterion.

- 'ward' minimizes the variance of the clusters being merged.
- 'average' uses the average of the distances of each observation of the two sets.
- 'complete' or 'maximum' linkage uses the maximum distances between all observations of the two sets.
- 'single' uses the minimum of the distances between all observations of the two sets.

*New in version 0.20:* Added the 'single' option

**distance\_threshold** : float, default=None

The linkage distance threshold at or above which clusters will not be merged. If not None, `n_clusters` must be None and `compute_full_tree` must be True.

*New in version 0.21.*
#### Comentando alguns parâmetros:

- **linkage**: determina o critério para a união dos clusters.
  - **ward** :minimiza a variância dos clusters que estão sendo mesclados. (Padrão)
  - **average**: usa a média das distâncias de cada observação dos dois conjuntos
  - **complete**: utiliza as distâncias máximas entre todas as observações dos dois conjuntos
  - **single**: utiliza as distâncias mínimas entre todas as observações dos dois conjuntos

{52}------------------------------------------------

# Agrupamento Hierárquico

- **Scki-learn** : <https://scikit-learn.org/stable/modules/generated/sklearn.cluster.AgglomerativeClustering.html>
### `sklearn.cluster.AgglomerativeClustering`

```
class sklearn.cluster.AgglomerativeClustering(n_clusters=2, *, affinity='deprecated', metric=None, memory=None, connectivity=None, compute_full_tree='auto', linkage='ward', distance_threshold=None, compute_distances=False) \[source\]
```

Agglomerative Clustering.

Recursively merges pair of clusters of sample data; uses linkage distance.

Read more in the [User Guide](#).
#### Parameters:

**linkage** : {'ward', 'complete', 'average', 'single'}, default='ward'

Which linkage criterion to use. The linkage criterion determines which distance to use between sets of observation. The algorithm will merge the pairs of cluster that minimize this criterion.

- 'ward' minimizes the variance of the clusters being merged.
- 'average' uses the average of the distances of each observation of the two sets.
- 'complete' or 'maximum' linkage uses the maximum distances between all observations of the two sets.
- 'single' uses the minimum of the distances between all observations of the two sets.

*New in version 0.20:* Added the 'single' option

**distance\_threshold** : float, default=None

The linkage distance threshold at or above which clusters will not be merged. If not None, `n_clusters` must be None and `compute_full_tree` must be True.

*New in version 0.21.*
#### Comentando alguns parâmetros:

- **distance\_threshold**: float ou None – valor limite definido para a distância entre o clusters. Acima desse valor, os clusters não serão unidos.

{53}------------------------------------------------
## Agrupamento Hierárquico

- **Scki-learn** : <https://scikit-learn.org/stable/modules/generated/sklearn.cluster.AgglomerativeClustering.html>
### `sklearn.cluster.AgglomerativeClustering`

```
class sklearn.cluster.AgglomerativeClustering(n_clusters=2, *, affinity='deprecated', metric=None, memory=None, connectivity=None, compute_full_tree='auto', linkage='ward', distance_threshold=None, compute_distances=False) \[source\]
```

Agglomerative Clustering.

Recursively merges pair of clusters of sample data; uses linkage distance.

Read more in the [User Guide](#).

|             |                                                                                                                                                                                                                              |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Attributes: | <b>n_clusters_ : int</b><br>The number of clusters found by the algorithm. If <code>distance_threshold=None</code> , it will be equal to the given <code>n_clusters</code> .                                                 |
|             | <b>labels_ : ndarray of shape (n_samples)</b><br>Cluster labels for each point.                                                                                                                                              |
|             | <b>n_leaves_ : int</b><br>Number of leaves in the hierarchical tree.                                                                                                                                                         |
|             | <b>n_connected_components_ : int</b><br>The estimated number of connected components in the graph.<br><br><i>New in version 0.21:</i> <code>n_connected_components_</code> was added to replace <code>n_components_</code> . |
|             | <b>n_features_in_ : int</b><br>Number of features seen during fit.<br><br><i>New in version 0.24.</i>                                                                                                                        |
|             |                                                                                                                                                                                                                              |
#### Comentando alguns atributos:

- **n\_clusters:** int – número de clusters encontrados pelo algoritmo.
- **labels:** lista correspondente à entrada com os rótulos numéricos atribuídos aos dados.

{54}------------------------------------------------

# Agrupamento Hierárquico

```
[ ] import pandas as pd
import numpy as np
from matplotlib import pyplot as plt
from sklearn.cluster import AgglomerativeClustering
import scipy.cluster.hierarchy as sch

# Usando pontos como exemplo
x1 = [1,2,3,4,5,6,7]
x2 = [1,1,4,6,3,4,3]
```

```
▶ X = []
for i in range(0,len(x1)):
    X.append([x1[i],x2[i]])
print("Lista de pontos:\n", X , "\n")
```

Lista de pontos:  
[[1, 1], [2, 1], [3, 4], [4, 6], [5, 3], [6, 4], [7, 3]]

Pontos

The scatter plot displays seven data points on a coordinate system where the horizontal axis is labeled 'x1' (ranging from 0 to 8) and the vertical axis is labeled 'x2' (ranging from 0 to 7). The points are plotted as blue dots at the following coordinates: (1, 1), (2, 1), (3, 4), (4, 6), (5, 3), (6, 4), and (7, 3). A light gray grid is visible in the background.

| x1 | x2 |
|----|----|
| 1  | 1  |
| 2  | 1  |
| 3  | 4  |
| 4  | 6  |
| 5  | 3  |
| 6  | 4  |
| 7  | 3  |

Scatter plot titled 'Pontos' showing 7 data points on a 2D plane with axes x1 and x2. The points are located at (1,1), (2,1), (3,4), (4,6), (5,3), (6,4), and (7,3).

{55}------------------------------------------------

# Agrupamento Hierárquico

```
▶ dendrogram = sch.dendrogram(sch.linkage(X, method='average'))  
model = AgglomerativeClustering(n_clusters=5, metric='euclidean', linkage='average')  
  
model.fit(X)  
labels = model.labels_  
numCluster = model.n_clusters  
print("Cluster dos dados: ", labels)  
print("Numero de clusters: ", numCluster)
```

Cluster dos dados: [1 1 3 2 0 0 4]  
Numero de clusters: 5

A dendrogram illustrating hierarchical clustering. The x-axis represents 7 data points, labeled 0, 1, 6, 4, 5, 2, and 3. The y-axis represents the distance, ranging from 0 to 5. The dendrogram shows the following merging process: points 0 and 1 merge at distance 1 (orange line); points 6 and 4 merge at distance ~1.7 (green line); points 4 and 5 merge at distance ~1.4 (green line); points 2 and 3 merge at distance ~2.2 (green line); the cluster {4, 5} merges with point 6 at distance ~3.2 (green line); the cluster {0, 1} merges with the cluster {6, 4, 5} at distance ~4.8 (blue line). The final structure shows 5 clusters: {0, 1}, {6, 4, 5}, {2, 3}, and two singletons (likely 2 and 3 if the labels are misinterpreted, but based on the image, it's {0,1}, {6,4,5}, {2,3} and two singletons).

Dendrogram showing hierarchical clustering of 7 data points.

{56}------------------------------------------------

# Agrupamento Hierárquico

```
[ ] for iCluster in range(0,numCluster):  
    print("Cluster: ", iCluster)  
    for indice in range(0, len(labels)):  
        if labels[indice]==iCluster: print(X[indice])  
  
plt.show()
```

---

```
Cluster:  0  
[5, 3]  
[6, 4]  
Cluster:  1  
[1, 1]  
[2, 1]  
Cluster:  2  
[4, 6]  
Cluster:  3  
[3, 4]  
Cluster:  4  
[7, 3]
```

{57}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-91f1a66918183ac1f85c438198c09376_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Scatter plot titled 'Pontos' showing 7 data points on a 2D plane with axes x1 and x2.
<!-- /IMAGE_DESCRIPTION -->
## Agrupamento Hierárquico

```
▶ dendrogram = sch.dendrogram(sch.linkage(X, method='average'))
model = AgglomerativeClustering(metric='euclidean', linkage='average')

model.fit(X)
labels = model.labels_
numCluster = model.n_clusters
print("Cluster dos dados: ", labels)
print("Numero de clusters: ", numCluster)
```

Omitindo a quantidade desejada de clusters

```
Cluster dos dados: [1 1 0 0 0 0 0]
Numero de clusters: 2
```

Dendrogram illustrating hierarchical clustering. The x-axis represents data points (0, 1, 6, 4, 5, 2, 3) and the y-axis represents distance (0 to 5). The dendrogram shows the merging of clusters: points 0 and 1 merge at distance 1; points 6 and 4 merge at distance ~1.7, and 4 and 5 merge at distance ~1.4; points 2 and 3 merge at distance ~2.2; the cluster {2, 3} merges with {4, 5} at distance ~3.2; finally, the cluster {0, 1} merges with the larger cluster {2, 3, 4, 5, 6} at distance ~4.8.

Dendrogram showing hierarchical clustering of 7 data points. The x-axis is labeled with indices 0, 1, 6, 4, 5, 2, 3. The y-axis represents distance from 0 to 5. A blue line connects point 0 to point 1 at distance 1. A green line connects point 6 to point 4 at distance ~1.7, and point 4 to point 5 at distance ~1.4. Another green line connects point 2 to point 3 at distance ~2.2. A final green line connects the group (2, 3) to the group (4, 5) at distance ~3.2. A large blue line connects the cluster {0, 1} to the cluster {2, 3, 4, 5, 6} at distance ~4.8.

```
[4] for iCluster in range(0, numCluster):
    print("Cluster: ", iCluster)
    for indice in range(0, len(labels)):
        if labels[indice] == iCluster: print(X[indice])

plt.show()
```

```
Cluster: 0
[3, 4]
[4, 6]
[5, 3]
[6, 4]
[7, 3]
Cluster: 1
[1, 1]
[2, 1]
```

{58}------------------------------------------------

# Dinâmica

- Testando e exemplificando o uso do agrupamento hierárquico aglomerativo.
