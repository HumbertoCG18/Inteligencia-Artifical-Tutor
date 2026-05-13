<!-- EXEC_SUMMARY_START -->
## Sumário
> *Leia antes de varrer o arquivo. Vá direto à seção relevante para a pergunta do aluno.*

- **Aprendizado Supervisionado Parte 2**
- **Roteiro**
- **Subáreas da Inteligência Artificial**
  - Aprendizado Supervisionado
  - Aprendizado Supervisionado
  - Aprendizado Supervisionado
  - Aprendizado Supervisionado
  - Classificação
  - Regressão
  - Regressão
  - Classificação
  - Aplicando o Modelo aos Dados de Teste
- **Aplicando o Modelo aos Dados de Teste**
- **Aplicando o Modelo aos Dados de Teste**
- **Aplicando o Modelo aos Dados de Teste**
  - Aplicando o Modelo aos Dados de Teste
- **Aplicando o Modelo aos Dados de Teste**
- **Indução de Árvores de Decisão**
  - Indução Top-Down
  - Algoritmo de Hunt
  - Indução Top-Down
  - Como filtrar os dados com base em um atributo?
  - Indução Top-Down
  - Como escolher o atributo?
- **Medidas para Impureza de Nodos**
- **Índice Gini**
- **Computando uma divisão com o Índice Gini**
  - Computando Índice Gini para Atributos Binários
  - Árvore elementar: Calculando o Índice GINI
  - Induzindo o 2o. Nível da árvore de decisão
  - Induzindo o 3o. Nível da árvore de decisão
- **Conjunto de Treino**
- **Comparação entre os critérios de divisão**
  - Indução Top-Down
  - Critérios de Parada para Indução Top-Down
- **Vantagens e Desvantagens de Árvores de Decisão**
- **Visualização Geométrica de uma Árvore de Decisão**
  - Visualização Geométrica de uma Árvore de Decisão
  - Visualização Geométrica de uma Árvore de Decisão
  - Visualização Geométrica de uma Árvore de Decisão
  - Visualização Geométrica de uma Árvore de Decisão
- **Espaço de Hipóteses**
- **Espaço de Hipóteses**
  - De árvores para regras
- **Busca no Espaço de Hipóteses**
- **Underfitting and Overfitting**
- **Árvores de Decisão para Problemas de Regressão**
- **Árvores de Decisão para Problemas de Regressão**
  - Exemplo de Árvore de Regressão
  - Exemplo de Árvore de Regressão
  - Exemplo de Árvore Modelo
  - Exemplo de Árvore Modelo
- **Árvores de Decisão para Problemas de Regressão**
  - Árvore elementar: Calculando o Índice GINI
  - Exemplo Ilustrativo
  - Exemplo Ilustrativo
  - Exemplo Ilustrativo
- **Exemplo Ilustrativo**
- **Exemplo Ilustrativo**
- **Exemplo Ilustrativo**
- **Exemplo Ilustrativo**
- **Exemplos de Algoritmos**
  - - ID3 (Quinlan 1986)
  - - C4.5 (Quinlan 1993)
- **Exemplos de Algoritmos**
- **Exemplos de Algoritmos**
- **Imagens Curadas**

<!-- EXEC_SUMMARY_END -->
<!-- DATALAB_CHUNK 1: pages 1-20 -->

{0}------------------------------------------------

A collage of two images. The top image shows a stylized, glowing brain composed of circuit board patterns in purple and blue, set against a dark background with faint circuit lines. The bottom image shows a close-up of a computer keyboard with vibrant, multi-colored LED backlighting in shades of red, orange, yellow, green, and blue.
## Aprendizado Supervisionado Parte 2

Árvores de Decisão

---

Silvia Moraes

Material elaborado pelo prof. **Duncan Ruiz**

{1}------------------------------------------------
## Roteiro

Relembrando

Machine Learning: Aprendizado Supervisionado

Tarefas Preditivas

Classificação & Regressão

Árvores de Decisão

{2}------------------------------------------------
## Subáreas da Inteligência Artificial

The diagram illustrates the subareas of Artificial Intelligence (IA) centered around a core concept. At the center is a circular icon with the text "Inteligência Artificial (IA)" surrounded by eight curved segments, one of which is highlighted in red. Six lines radiate from this center to different subareas, each with a corresponding list of topics or applications.

- Aprendizado de Máquina (Machine Learning)**
  - Aprendizado Profundo (Deep Learning)
  - Aprendizado Supervisionado
  - Aprendizado Não Supervisionado
  - Aprendizado por Reforço
  - Aprendizado auto-supervisionado
  - Aprendizado semissupervisionado
- Processamento de Linguagem Natural**
  - Extração de Informações
  - Classificação de Texto
  - Tradução Automática
  - Perguntas e Respostas
  - Geração de Texto
- Raciocínio Automatizado**
- Robótica**
- IA Explicável**
- Visão Computacional**

Diagram of Artificial Intelligence subareas

{3}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-1b7d539e02a202c2cf2d97698b911447_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of Artificial Intelligence subareas
<!-- /IMAGE_DESCRIPTION -->
### Aprendizado Supervisionado

Exige que os **dados** estejam **rotulados** (anotados com suas respectivas classes/valores de saída)

Os algoritmos que seguem esse tipo de aprendizado recebem pares de valores:

- os dados de entrada (x) e
- os valores de saída (rótulos) correspondentes (y).

**Saída (y):**  
rótulo/classe/anotação

**Entrada (x):**  
Imagem ou características

**Gato**

The diagram shows three images with labels: a cat labeled 'Gato', a dog labeled 'Cachorro', and a chicken labeled 'Galinha'. Arrows point from the labels 'Entrada (x)' and 'Saída (y)' to the cat image. A URL 'https://www.pexels.com/' is visible in the bottom right of the cat image.

<https://www.pexels.com/>

**Cachorro**

**Galinha**

Diagram illustrating supervised learning with labeled images of a cat, a dog, and a chicken.

**Dataset Anotado**

{4}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-d62e2e2281009c16f4ee61660e716cd9_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram illustrating supervised learning with labeled images of a cat, a dog, and a chicken.
<!-- /IMAGE_DESCRIPTION -->
### Aprendizado Supervisionado

Em um conjunto de dados (exemplos) rotulado :

- Cada dado corresponde a um indivíduo do domínio e é formado por uma tupla contendo características (features).

**Atributo de entrada**  
(atributo previsor)

| sepal length | sepal width | petal length | petal width | class           |
|--------------|-------------|--------------|-------------|-----------------|
| 5,1          | 3,5         | 1,4          | 0,2         | Iris-setosa     |
| 4,9          | 3,0         | 1,4          | 0,2         | Iris-setosa     |
| 7,0          | 3,2         | 4,7          | 7,1         | Iris-versicolor |
| 6,4          | 3,2         | 4,5          | 1,5         | Iris-versicolor |
| 6,3          | 3,3         | 6,0          | 2,5         | Iris-virginica  |
| 5,8          | 2,7         | 5,1          | 1,9         | Iris-virginica  |

**Atributo de saída**  
(atributo alvo ou meta)

**Rótulo**  
(Classes)

The image shows three distinct Iris flower species side-by-side. From left to right, they are labeled: Iris Virginica (a blue/purple flower with a white center), Iris Setosa (a dark purple flower), and Iris Versicolor (a purple flower with a yellow center). Each image has its label written in small text below it.

Three images of Iris flowers: Iris Virginica, Iris Setosa, and Iris Versicolor.

{5}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-2dfa6ac3edfe874f68aa0cbccaa42322_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A collage of two images. The top image shows a stylized, glowing brain composed of circuit board patterns in purple and blue, set against a dark background with faint circuit lines. The bottom image shows a close-up of...
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-764bb8d7c93b090e205d908e1a8cade4_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Three images of Iris flowers: Iris Virginica, Iris Setosa, and Iris Versicolor.
<!-- /IMAGE_DESCRIPTION -->
### Aprendizado Supervisionado

O objetivo é encontrar um modelo capaz de mapear os valores de entrada ( $x$ ) nos valores de saída  $y$ .

Em outras palavras, que aproxime  $f$ , tal que  $f(x) = y$ .

Supervisão: ajuste usando o erro em relação à saída esperada.

The diagram illustrates the supervised learning process. On the left, a collection of images is shown, each with a label in a blue box: 'Gato' (Cat), 'Cachorro' (Dog), and 'Galinha' (Chicken). Below this collection is the text 'Dataset Anotado' (Annotated Dataset). A large blue arrow points from the dataset to a central green box. This box is labeled 'Algoritmo de Machine Learning Supervisionado' (Supervised Machine Learning Algorithm) and contains a smaller white box labeled 'Treinamento' (Training) which features a small neural network icon. Another large blue arrow points from this central box to a final box on the right labeled 'Modelo' (Model), which also contains a neural network icon.

Diagram illustrating the supervised learning process. It shows an annotated dataset of images (cat, dog, chicken) being processed by a supervised machine learning algorithm for training, resulting in a trained model.

{6}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-f6d72d7c790e7f585532140f3971639a_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram illustrating the supervised learning process.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-9b9d2abd741ed4bafe7f78f89961c663_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of the learning process
<!-- /IMAGE_DESCRIPTION -->
### Aprendizado Supervisionado

**Tarefa preditiva:** encontra uma função (modelo) a partir dos dados de treino que possa ser usada para prever um rótulo (classe) ou valor de um novo exemplo.

Pode ser:

**classificação** (rótulos discretos)

**regressão** (rótulos contínuos)

Modelo Probabilístico

{7}------------------------------------------------
### Classificação

The diagram illustrates the classification process. It starts with an input image of a cat, labeled "Imagem sem rótulo" and "Entrada". A blue arrow points to a green box labeled "Algoritmo de Machine Learning Supervisionado". Inside this box, a smaller white box labeled "Modelo" contains a neural network icon, and the word "Generalização" is written below the algorithm name. Another blue arrow points from the algorithm box to the output "gato (96%)", which is labeled "Predição". The input image has a URL at the bottom: <https://www.pexels.com/>.

Diagram of the classification process

É o processo de automaticamente atribuir rótulos a dados.

Pode ser do tipo

- Binária: possui apenas duas classes

- Multiclasse: possui mais de duas classes

Pode atribuir

- Um único rótulo (single label)

- Vários rótulos (multi-label)

An image showing a tomato sorting machine. A red label at the bottom of the image reads "Máquina de triagem de tomate".

Image of a tomato sorting machine

{8}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-2ee59e629035d641140e55f4d215b0d7_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of the classification process
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-89986656b45c3b6896256f1a22f7c186_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Image of a tomato sorting machine
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-dff659a422a9e5edd8ce41823a863379_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Icon representing regression analysis, showing a bar chart with five bars of varying heights inside a white circle.
<!-- /IMAGE_DESCRIPTION -->
### Regressão

É o processo de automaticamente predizer novos valores y.  
Neste caso, os dados são anotados com valores.

A line graph illustrating regression prediction. The x-axis represents years from 2015 to 2022. The y-axis represents an unlabeled value. Data points are plotted for 2015, 2016, 2017, 2018, 2019, 2020, and 2021. A solid blue line connects these points. For the year 2022, there is a dashed red line extending from the 2021 point, ending with a red question mark, indicating a predicted value.

| Ano  | Valor (aproximado) |
|------|--------------------|
| 2015 | 0.0                |
| 2016 | 0.5                |
| 2017 | 1.5                |
| 2018 | 2.0                |
| 2019 | 1.0                |
| 2020 | 2.5                |
| 2021 | 2.0                |
| 2022 | 3.0 (predito)      |

Line graph showing data points from 2015 to 2021 with a dashed red line and a question mark for 2022, illustrating regression prediction.

A scatter plot showing training data and a regression line. The x-axis ranges from 0 to 100, and the y-axis ranges from -1 to 4. Blue dots represent the training data, which follow a sinusoidal pattern. A solid red line represents the regression model, which is a smooth curve fitted to the training data points. A legend in the top right corner identifies the blue dots as 'training data' and the red line as 'regression'.

| x   | y (training data) |
|-----|-------------------|
| 0   | 0.5               |
| 20  | 1.0               |
| 40  | 0.0               |
| 60  | 1.5               |
| 80  | 3.5               |
| 100 | 3.0               |

Scatter plot with a regression line, showing training data points and a fitted regression curve.

{9}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-91be14371a97fb5ce9eeb29ae18d07c3_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Line graph showing data points from 2015 to 2021 with a dashed red line and a question mark for 2022, illustrating regression prediction.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-bedcca5cdf168e3508ef511d94ec514c_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Scatter plot with a regression line, showing training data points and a fitted regression curve.
<!-- /IMAGE_DESCRIPTION -->
### Regressão

![Diagram illustrating the supervised machine learning regression process. On the left, an 'Annotated Dataset' [x, f(x)] with points [1, 1], [2, 4], [3, 9], [4, 16], [5, 25] is input to a 'Supervised Machine Learning Algorithm'. The algorithm uses 'Training' data to build a 'Model'. An input x is shown with a red question mark, and the model outputs f(x). A red x^2 is shown above the model's output f(x), indicating the target function.](f4fdd410cdb84df81274da55721e56fb_img.jpg)

[x, f(x)]  
[1, 1]  
[2, 4]  
[3, 9]  
[4, 16]  
[5, 25]

x **?**  $f(x)$

Algoritmo de Machine Learning Supervisionado

Treinamento

x  **$x^2$**   $f(x)$

Modelo

Diagram illustrating the supervised machine learning regression process. On the left, an 'Annotated Dataset' [x, f(x)] with points [1, 1], [2, 4], [3, 9], [4, 16], [5, 25] is input to a 'Supervised Machine Learning Algorithm'. The algorithm uses 'Training' data to build a 'Model'. An input x is shown with a red question mark, and the model outputs f(x). A red x^2 is shown above the model's output f(x), indicating the target function.

Dataset Anotado

training data  
regression

A scatter plot showing training data points (blue dots) and a regression line (red curve) that fits the data. The x-axis ranges from 0 to 100, and the y-axis ranges from -1 to 4. The legend indicates 'training data' and 'regression'.

Entrada

Algoritmo de Machine Learning Supervisionado

Generalização

x  **$x^2$**   $f(x)$

Modelo

Diagram illustrating the generalization process. An input '6' is shown entering a 'Supervised Machine Learning Algorithm' block. The algorithm uses 'Generalization' to build a 'Model'. The model takes an input x and outputs f(x). A red x^2 is shown above the model's output f(x), indicating the target function.

{10}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-f519a5be118c846f631c992412353fb9_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A scatter plot showing training data points (blue dots) and a regression line (red curve) that fits the data.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-daa4a6fa7e2ba1954258f86b4928eb32_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram illustrating the generalization process.
<!-- /IMAGE_DESCRIPTION -->
#### Classificação & Regressão com Árvores de Decisão

```
graph TD; A[Restituição] -- S --> B[N]; A -- N --> C[Status Conjugal]; C -- "Solteiro, Divorc." --> D[Renda]; C -- Casado --> E[N]; D -- "<= 80K" --> F[N]; D -- "> 80K" --> G[S];
```

A decision tree diagram illustrating a classification process. The root node is 'Restituição' (Refund). If 'S' (Yes), the outcome is 'N' (No). If 'N' (No), the next node is 'Status Conjugal' (Marital Status). If 'Solteiro, Divorc.' (Single, Divorced), the next node is 'Renda' (Income). If 'Casado' (Married), the outcome is 'N' (No). For 'Renda', if '<= 80K' (Less than or equal to 80K), the outcome is 'N' (No). If '> 80K' (Greater than 80K), the outcome is 'S' (Yes).

Decision tree diagram for classification based on tax refund, marital status, and income.

{11}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-5b4e774d63e0e0ed73801a9247755e5f_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree diagram for classification based on tax refund, marital status, and income.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-8307f6b04df072c9332f9987e034272c_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram illustrating the classification process.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-9b1ec0090070bdf52ea28763b8d52477_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree diagram.
<!-- /IMAGE_DESCRIPTION -->
### Classificação

A close-up photograph of numerous interlocking wooden gears in various colors including natural wood, black, red, orange, and teal, set against a dark background.

A close-up photograph of numerous interlocking wooden gears in various colors including natural wood, black, red, orange, and teal, set against a dark background.

{12}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-ec0158057f8ccaf74edba16682ec5444_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A close-up photograph of numerous interlocking wooden gears in various colors including natural wood, black, red, orange, and teal, set against a dark background.
<!-- /IMAGE_DESCRIPTION -->
#### Árvores de Decisão

- Método para aproximar funções discretas ou contínuas, representadas por meio de um grafo acíclico direcionado, com vértice inicial único
- Tal grafo pode ser representado por um conjunto de regras “SE...ENTÃO” (Compreensibilidade)
- Amplamente utilizado em aplicações práticas, principalmente em problemas de classificação

```
graph TD; A[Restituição] -- S --> B[N]; A -- N --> C[Status Conjugal]; C -- "Solteiro, Divorc." --> D[Renda]; C -- Casado --> E[N]; D -- "<= 80K" --> F[N]; D -- "> 80K" --> G[S];
```

O diagrama mostra uma árvore de decisão com o seguinte fluxo:

- O nó inicial é **Restituição**.
- Se **S** (Sim), o resultado é **N**.
- Se **N** (Não), o fluxo vai para o nó **Status Conjugal**.
- Do **Status Conjugal**, se **Solteiro, Divorc.**, o fluxo vai para o nó **Renda**.
- Se **Casado**, o resultado é **N**.
- Do **Renda**, se **<= 80K**, o resultado é **N**.
- Se **> 80K**, o resultado é **S**.

Diagrama de uma Árvore de Decisão

{13}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-eefe19c5e14dc4d6c316b7f7fbb7d7d7_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de uma Árvore de Decisão
<!-- /IMAGE_DESCRIPTION -->
##### Exemplo de Árvore de Decisão

*categórico* *Categórico* *contínuo* *classe*

| Tid | Restituição | Status Conjugal | Renda | Calote ? |
|-----|-------------|-----------------|-------|----------|
| 1   | S           | Solteiro        | 125K  | N        |
| 2   | N           | Casado          | 100K  | N        |
| 3   | N           | Solteiro        | 70K   | N        |
| 4   | S           | Casado          | 120K  | N        |
| 5   | N           | Divorc.         | 95K   | S        |
| 6   | N           | Casado          | 60K   | N        |
| 7   | S           | Divorc.         | 220K  | N        |
| 8   | N           | Solteiro        | 85K   | S        |
| 9   | N           | Casado          | 75K   | N        |
| 10  | N           | Solteiro        | 90K   | S        |

Conjunto de Treino

*Atributos Explanatórios*

```
graph TD; A[Restituição] -- S --> B[N]; A -- N --> C[Status Conjugal]; C -- "Solteiro, Divorc." --> D[Renda]; C -- Casado --> E[N]; D -- "<= 80K" --> F[N]; D -- "> 80K" --> G[S];
```

The decision tree starts with 'Restituição' as the root node. A 'S' (Yes) branch leads to a leaf node 'N' (No). A 'N' (No) branch leads to a node 'Status Conjugal'. From 'Status Conjugal', a 'Casado' (Married) branch leads to a leaf node 'N'. A 'Solteiro, Divorc.' (Single, Divorced) branch leads to a node 'Renda'. From 'Renda', a '<= 80K' branch leads to a leaf node 'N', and a '> 80K' branch leads to a leaf node 'S' (Yes). Red dashed arrows from the text 'Atributos Explanatórios' point to the 'Restituição', 'Status Conjugal', and 'Renda' nodes.

Decision tree diagram showing splits on Restituição, Status Conjugal, and Renda.

Modelo: Árvore de Decisão

{14}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-a33da0f14e456f92539ce3e9b7d81f9a_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree diagram showing splits on Restituição, Status Conjugal, and Renda.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-7efae06af3af43ffe5d4b956a679cf54_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree diagram showing splits on Restituição, Status Conjugal, and Renda.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-187d05bf7ead21e1394b61320d8b3632_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree diagram showing splits on Status Conjugal, Restituição, and Renda.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-0931f3e098bd4539041de11c50cec2d2_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree diagram showing 'Restituição' as the root node.
<!-- /IMAGE_DESCRIPTION -->
##### Exemplo de Árvore de Decisão

*categórico* *Categórico* *contínuo* *classe*

| Tid | Restituição | Status Conjugal | Renda | Calote ? |
|-----|-------------|-----------------|-------|----------|
| 1   | S           | Solteiro        | 125K  | N        |
| 2   | N           | Casado          | 100K  | N        |
| 3   | N           | Solteiro        | 70K   | N        |
| 4   | S           | Casado          | 120K  | N        |
| 5   | N           | Divorc.         | 95K   | S        |
| 6   | N           | Casado          | 60K   | N        |
| 7   | S           | Divorc.         | 220K  | N        |
| 8   | N           | Solteiro        | 85K   | S        |
| 9   | N           | Casado          | 75K   | N        |
| 10  | N           | Solteiro        | 90K   | S        |

Conjunto de Treino

```
graph TD; A[Restituição] -- S --> B[N]; A -- N --> C[Status Conjugal]; C -- "Solteiro, Divorc." --> D[Renda]; C -- Casado --> E[N]; D -- "<= 80K" --> F[N]; D -- "> 80K" --> G[S];
```

The decision tree starts with 'Restituição' as the root node. A 'S' (Sim) branch leads to a leaf node 'N'. A 'N' (Não) branch leads to a 'Status Conjugal' node. From 'Status Conjugal', a 'Casado' branch leads to a leaf node 'N', and a 'Solteiro, Divorc.' branch leads to a 'Renda' node. From 'Renda', a '<= 80K' branch leads to a leaf node 'N', and a '> 80K' branch leads to a leaf node 'S'.

Decision tree diagram showing splits on Restituição, Status Conjugal, and Renda.

Modelo: Árvore de Decisão

{15}------------------------------------------------
##### Outro exemplo de Árvore de Decisão

| <i>Tid</i> | <i>Restituição</i> | <i>Status Conjugal</i> | <i>Renda</i> | <i>Calote ?</i> |
|------------|--------------------|------------------------|--------------|-----------------|
| 1          | S                  | Solteiro               | 125K         | N               |
| 2          | N                  | Casado                 | 100K         | N               |
| 3          | N                  | Solteiro               | 70K          | N               |
| 4          | S                  | Casado                 | 120K         | N               |
| 5          | N                  | Divorc.                | 95K          | S               |
| 6          | N                  | Casado                 | 60K          | N               |
| 7          | S                  | Divorc.                | 220K         | N               |
| 8          | N                  | Solteiro               | 85K          | S               |
| 9          | N                  | Casado                 | 75K          | N               |
| 10         | N                  | Solteiro               | 90K          | S               |

*categórico* *Categórico* *contínuo* *classe*

```
graph TD; A[Status Conjugal] -- Casado --> B[N]; A -- "Solteiro, Divorc." --> C[Restituição]; C -- S --> D[N]; C -- N --> E[Renda]; E -- "<= 80K" --> F[N]; E -- "> 80K" --> G[S];
```

Árvore de decisão baseada nos dados da tabela. A raiz é 'Status Conjugal'. Se 'Casado', a decisão é 'N'. Se 'Solteiro, Divorc.', a decisão vai para 'Restituição'. Se 'S', a decisão é 'N'. Se 'N', a decisão vai para 'Renda'. Se 'Renda' <= 80K, a decisão é 'N'. Se 'Renda' > 80K, a decisão é 'S'.

Pode existir mais de uma árvore de decisão adequada para os mesmos dados!

{16}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-0f985b39edc1d52ba3600c438bc8f0a5_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Árvore de decisão baseada nos dados da tabela.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-4e85fe330de2c4f5eea6de4b2a53c77f_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de árvore de decisão com nó raiz 'Restituição' (amarelo).
<!-- /IMAGE_DESCRIPTION -->
##### Exemplo de Classificação

*categórico* *Categórico* *contínuo* *classe*

| Tid | Restitui<br>ção | Status<br>Conjugal | Renda | Calote<br>? |
|-----|-----------------|--------------------|-------|-------------|
| 1   | S               | Solteiro           | 125K  | N           |
| 2   | N               | Casado             | 100K  | N           |
| 3   | N               | Solteiro           | 70K   | N           |
| 4   | S               | Casado             | 120K  | N           |
| 5   | N               | Divorc.            | 95K   | S           |
| 6   | N               | Casado             | 60K   | N           |
| 7   | S               | Divorc.            | 220K  | N           |
| 8   | N               | Solteiro           | 85K   | S           |
| 9   | N               | Casado             | 75K   | N           |
| 10  | N               | Solteiro           | 90K   | S           |

| Restitui<br>ção | Status<br>Conjugal | Renda | Calote<br>? |
|-----------------|--------------------|-------|-------------|
| N               | Solteiro           | 75K   | ?           |
| S               | Casado             | 50K   | ?           |
| N               | Casado             | 150K  | ?           |
| S               | Divorc.            | 90K   | ?           |
| N               | Solteiro           | 40K   | ?           |
| N               | Casado             | 80K   | ?           |

```
graph LR; A[Conjunto de Treino] --> B[Classificador]; B --> C[Modelo]; D[Conjunto de Teste] --> C;
```

Diagram illustrating the classification process. A 'Conjunto de Treino' (Training Set) is input to a 'Classificador' (Classifier), which outputs a 'Modelo' (Model). A 'Conjunto de Teste' (Test Set) is also input to the 'Modelo'.

{17}------------------------------------------------
##### Exemplo de Classificação

| Tid | Restituição | Status Conjugal | Renda | Calote ? |
|-----|-------------|-----------------|-------|----------|
| 1   | S           | Solteiro        | 125K  | N        |
| 2   | N           | Casado          | 100K  | N        |
| 3   | N           | Solteiro        | 70K   | N        |
| 4   | S           | Casado          | 120K  | N        |
| 5   | N           | Divorc.         | 95K   | S        |
| 6   | N           | Casado          | 60K   | N        |
| 7   | S           | Divorc.         | 220K  | N        |
| 8   | N           | Solteiro        | 85K   | S        |
| 9   | N           | Casado          | 75K   | N        |
| 10  | N           | Solteiro        | 90K   | S        |

Treino

Indução

A diagram showing the learning process. It consists of a red-bordered box containing two stacked 3D-style boxes. The top box is light green and labeled "Algoritmo de Indução de Árvore de Decisão". The bottom box is grey and labeled "Aprendizado". A red arrow points to the top box from the top right. A dark green arrow labeled "Indução" points from the training table to the bottom box.

Diagram of the learning process

Modelo

Aplicação

Dedução

| Restituição | Status Conjugal | Renda | Calote ? |
|-------------|-----------------|-------|----------|
| N           | Solteiro        | 75K   | ?        |
| S           | Casado          | 50K   | ?        |
| N           | Casado          | 150K  | ?        |
| S           | Divorc.         | 90K   | ?        |
| N           | Solteiro        | 40K   | ?        |
| N           | Casado          | 80K   | ?        |

Teste

{18}------------------------------------------------
##### Exemplo de Classificação

| Tid | Restituição | Status Conjugal | Renda | Calote ? |
|-----|-------------|-----------------|-------|----------|
| 1   | S           | Solteiro        | 125K  | N        |
| 2   | N           | Casado          | 100K  | N        |
| 3   | N           | Solteiro        | 70K   | N        |
| 4   | S           | Casado          | 120K  | N        |
| 5   | N           | Divorc.         | 95K   | S        |
| 6   | N           | Casado          | 60K   | N        |
| 7   | S           | Divorc.         | 220K  | N        |
| 8   | N           | Solteiro        | 85K   | S        |
| 9   | N           | Casado          | 75K   | N        |
| 10  | N           | Solteiro        | 90K   | S        |

Treino

Indução

Algoritmo de Indução de Árvore de Decisão

Aprendizado

Modelo

Aplicação

Dedução

Teste

| Restituição | Status Conjugal | Renda | Calote ? |
|-------------|-----------------|-------|----------|
| N           | Solteiro        | 75K   | ?        |
| S           | Casado          | 50K   | ?        |
| N           | Casado          | 150K  | ?        |
| S           | Divorc.         | 90K   | ?        |
| N           | Solteiro        | 40K   | ?        |
| N           | Casado          | 80K   | ?        |

{19}------------------------------------------------
### Aplicando o Modelo aos Dados de Teste

Dados de Teste

| Restituição | Status Conjugal | Renda | Calote ? |
|-------------|-----------------|-------|----------|
| N           | Casado          | 80K   | ?        |

Início na raiz da árvore.

```
graph TD; Root[Restituição] -- S --> LeafN1[N]; Root -- N --> NodeStatus[Status Conjugal]; NodeStatus -- "Solteiro, Divorc." --> NodeRenda[Renda]; NodeStatus -- Casado --> LeafN2[N]; NodeRenda -- "<= 80K" --> LeafN3[N]; NodeRenda -- "> 80K" --> LeafS[S];
```

Decision tree diagram showing the classification process for the test data. The root node is 'Restituição'. A red dashed arrow points to it. The tree has two main branches: 'S' (Sim) leading to a leaf node 'N' (Não), and 'N' (Não) leading to a node 'Status Conjugal'. From 'Status Conjugal', there are two branches: 'Solteiro, Divorc.' leading to a node 'Renda', and 'Casado' leading to a leaf node 'N'. From 'Renda', there are two branches: '<= 80K' leading to a leaf node 'N', and '> 80K' leading to a leaf node 'S' (Sim).

<!-- DATALAB_CHUNK 2: pages 21-40 -->

{20}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-81a4cbf0b3c4cbc065efdf8f800dadde_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree diagram showing the classification process for the test data.
<!-- /IMAGE_DESCRIPTION -->
## Aplicando o Modelo aos Dados de Teste

Dados de Teste

The diagram illustrates a decision tree model for classification. The root node is 'Restituição' (Refund), which branches into 'S' (Yes) leading to a leaf node 'N' (No) and 'N' (No) leading to a node 'Status Conjugal' (Marital Status). 'Status Conjugal' branches into 'Solteiro, Divorc.' (Single, Divorced) leading to a node 'Renda' (Income) and 'Casado' (Married) leading to a leaf node 'N' (No). 'Renda' branches into '<= 80K' leading to a leaf node 'N' (No) and '> 80K' leading to a leaf node 'S' (Yes). A red dashed arrow points from the 'Restituição' node to a table titled 'Dados de Teste' (Test Data).

| Restituição | Status Conjugal | Renda | Calote ? |
|-------------|-----------------|-------|----------|
| N           | Casado          | 80K   | ?        |

Decision tree diagram and a test data table.

{21}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-c5655e700cc3e9aac7e9f4f07f30264d_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree diagram and a test data table.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-d53cd0fd1cf896a9353fd63de1505ba2_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree diagram and test data table.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-73b5cce955ba9415a98791db7b0080ad_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree diagram and a test data table.
<!-- /IMAGE_DESCRIPTION -->
## Aplicando o Modelo aos Dados de Teste

Dados de Teste

```
graph TD; A[Restituição] -- S --> B(N); A -- N --> C[Status Conjugal]; C -- "Solteiro, Divorc." --> D[Renda]; C -- Casado --> E(N); D -- "<= 80K" --> F(N); D -- "> 80K" --> G(S);
```

| Restituição | Status Conjugal | Renda | Calote ? |
|-------------|-----------------|-------|----------|
| N           | Casado          | 80K   | ?        |

Decision tree diagram and test data table. The tree starts with 'Restituição' (S leads to 'N', N leads to 'Status Conjugal'). 'Status Conjugal' (Solteiro/Divorc. leads to 'Renda', Casado leads to 'N'). 'Renda' (<= 80K leads to 'N', > 80K leads to 'S'). A red dashed arrow points from the test data row to the 'N' branch of 'Restituição'.

{22}------------------------------------------------
## Aplicando o Modelo aos Dados de Teste

Dados de Teste

The diagram illustrates a decision tree model and a test data table. The decision tree starts with 'Restituição' (Refund) as the root node. A solid black arrow labeled 'S' (Yes) leads to a leaf node 'N' (No). A solid red arrow labeled 'N' (No) leads to a node 'Status Conjugal' (Marital Status). From 'Status Conjugal', a solid black arrow labeled 'Solteiro, Divorc.' (Single, Divorced) leads to a node 'Renda' (Income), and a solid black arrow labeled 'Casado' (Married) leads to a leaf node 'N'. From 'Renda', a solid black arrow labeled '<= 80K' leads to a leaf node 'N', and a solid black arrow labeled '> 80K' leads to a leaf node 'S' (Yes). To the right, a table titled 'Dados de Teste' contains one row of data: 'Restituição' (N), 'Status Conjugal' (Casado), 'Renda' (80K), and 'Calote ?' (?). A dashed red arrow points from the 'N' in the 'Restituição' column to the 'N' branch of the 'Restituição' node in the decision tree.

| Restituição | Status Conjugal | Renda | Calote ? |
|-------------|-----------------|-------|----------|
| N           | Casado          | 80K   | ?        |

Decision tree diagram and test data table showing the application of a model to test data.

{23}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-d734a6ea1b381280f043fcf70391b6db_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree diagram and test data table showing the application of a model to test data.
<!-- /IMAGE_DESCRIPTION -->
### Aplicando o Modelo aos Dados de Teste

Dados de Teste

```
graph TD; A[Restituição] -- S --> B[N]; A -- N --> C[Status Conjugal]; C -- "Solteiro, Divorc." --> D[Renda]; C -- Casado --> E[N]; D -- "<= 80K" --> F[N]; D -- "> 80K" --> G[S];
```

| Restituição | Status Conjugal | Renda | Calote ? |
|-------------|-----------------|-------|----------|
| N           | Casado          | 80K   | ?        |

Decision tree diagram and a test data table. The tree starts with 'Restituição' (S leads to N, N leads to 'Status Conjugal'). 'Status Conjugal' (Solteiro, Divorc. leads to 'Renda', Casado leads to N). 'Renda' (<= 80K leads to N, > 80K leads to S). A dashed red arrow points from the test data row to the 'Status Conjugal' node.

{24}------------------------------------------------
## Aplicando o Modelo aos Dados de Teste

Dados de Teste

| Restituição | Status Conjugal | Renda | Calote ? |
|-------------|-----------------|-------|----------|
| N           | Casado          | 80K   | ?        |

```
graph TD; A[Restituição] -- S --> B[N]; A -- N --> C[Status Conjugal]; C -- "Solteiro, Divorc." --> D[Renda]; C -- Casado --> E[N]; D -- "<= 80K" --> F[N]; D -- "> 80K" --> G[S];
```

Decision tree structure:

- Root node: **Restituição**
  - Branch **S** leads to leaf node **N**.
  - Branch **N** leads to node **Status Conjugal**.
    - Branch **Solteiro, Divorc.** leads to node **Renda**.
      - Branch **<= 80K** leads to leaf node **N**.
      - Branch **> 80K** leads to leaf node **S**.
    - Branch **Casado** leads to leaf node **N**.

Decision tree diagram for predicting 'Calote ?' based on 'Restituição', 'Status Conjugal', and 'Renda'.

Atribuir "N" para Calote

{25}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-26d664119ad25250780f554633444e54_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree diagram for predicting 'Calote ?' based on 'Restituição', 'Status Conjugal', and 'Renda'.
<!-- /IMAGE_DESCRIPTION -->
## Indução de Árvores de Decisão

- Descobrir “árvore ótima” é problema NP-Difícil
- Muitas heurísticas para gerar árvores
  - Top-Down
  - Bottom-Up
  - Híbrida
  - Algoritmos Evolutivos
  - etc.

{26}------------------------------------------------
### Indução Top-Down
#### - Algoritmo de Hunt

- Assuma que  $D_t$  é o conjunto de exemplos de treino que chega ao nó  $t$
- Assuma que  $y = \{y_1, \dots, y_c\}$  são os rótulos das classes
- Passo 1:
  - Se todas instâncias em  $D_t$  pertencem a mesma classe  $y_t$ , então  $t$  é um nó folha rotulado como  $y_t$
- Passo 2:
  - Se  $D_t$  contém instâncias de mais de uma classe, **um teste sobre determinado atributo** é selecionado para particionar os registros em sub-conjuntos menores. Um nó é criado para cada resultado do teste e as instâncias em  $D_t$  são distribuídas por estes nós de acordo com os resultados. Aplicar algoritmo **recursivamente para cada nó gerado**.

{27}------------------------------------------------
### Algoritmo de Hunt

```
graph TD; N1[N] --> R1[Restituição]; R1 -- S --> N2[N]; R1 -- N --> S1[S]; N2 --> R2[Restituição]; R2 -- S --> N3[N]; R2 -- N --> SC[Status Conjugal]; SC -- "Solteiro, Divorc." --> S2[S]; SC -- Casado --> N4[N]; N4 --> R3[Renda]; R3 -- "<= 80K" --> N5[N]; R3 -- "> 80K" --> S3[S];
```

Diagram illustrating the Hunt algorithm for decision tree construction. It shows three stages of tree growth: 1. Initial state: A single blue node 'N'. 2. First split: A yellow node 'Restituição' with 'S' (Yes) leading to blue node 'N' and 'N' (No) leading to blue node 'S'. 3. Further splits: The 'N' branch from 'Restituição' leads to another yellow node 'Status Conjugal', which splits into 'S' (Yes) leading to blue node 'S' and 'Casado' (Married) leading to blue node 'N'. The 'Casado' branch then leads to a yellow node 'Renda', which splits into '<= 80K' leading to blue node 'N' and '> 80K' leading to blue node 'S'. Red arrows indicate the sequence of splits.

| Tid | Restituição | Status Conjugal | Renda | Calote ? |
|-----|-------------|-----------------|-------|----------|
| 1   | S           | Solteiro        | 125K  | N        |
| 2   | N           | Casado          | 100K  | N        |
| 3   | N           | Solteiro        | 70K   | N        |
| 4   | S           | Casado          | 120K  | N        |
| 5   | N           | Divorc.         | 95K   | S        |
| 6   | N           | Casado          | 60K   | N        |
| 7   | S           | Divorc.         | 220K  | N        |
| 8   | N           | Solteiro        | 85K   | S        |
| 9   | N           | Casado          | 75K   | N        |
| 10  | N           | Solteiro        | 90K   | S        |

{28}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-d17aa1fcc3b86503ad1dd0717a6c34c2_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram illustrating the Hunt algorithm for decision tree construction.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-73b28b0f5e3be628bb5a3d6bd1d79d21_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Two decision tree diagrams illustrating Gini split calculations for the 'Status Conjugal' attribute.
<!-- /IMAGE_DESCRIPTION -->
### Indução Top-Down

- Estratégia Recursiva
- Estratégia Gulosa (*greedy*)
  - Divide os registros com base em teste sobre atributo que otimiza localmente determinado critério
- Questões de Projeto
  - Determinar como particionar os dados
    - Como filtrar os dados com base em um atributo?
    - Como escolher o atributo a ser utilizado?
  - Determinar quando parar de particionar

{29}------------------------------------------------
### Como filtrar os dados com base em um atributo?

- Depende do tipo de atributo
  - Nominal
  - Ordinal
  - Contínuo
- Depende do número de divisões desejado
  - Binária
  - Múltipla

{30}------------------------------------------------
#### Divisão para atributos categóricos nominais

- **Múltipla:** dividir com base no número de categorias

```
graph TD; A[Tipo de Carro] --> B[Família]; A --> C[Esportivo]; A --> D[Luxo];
```

Diagrama de divisão múltipla para o atributo "Tipo de Carro". O nó "Tipo de Carro" (amarelo) é dividido em três categorias: "Família", "Esportivo" e "Luxo".

Diagrama de divisão múltipla para o atributo 'Tipo de Carro'

- **Binária:** agregar categorias em dois sub-conjuntos. Necessário encontrar a divisão ótima.

```
graph TD; A1[Tipo de Carro] --> B1["{Família, Esportivo}"]; A1 --> C1["{Luxo}"]; A2[Tipo de Carro] --> B2["{Família, Luxo}"]; A2 --> C2["{Esportivo}"]; A3[Tipo de Carro] --> B3["{Família, Esportivo}"]; A3 --> C3["{Luxo}"]; A4[Tipo de Carro] --> B4["{Família, Luxo}"]; A4 --> C4["{Esportivo}"]; A5[Tipo de Carro] --> B5["{Esportivo, Luxo}"]; A5 --> C5["{Família}"]; A6[Tipo de Carro] --> B6["{Esportivo, Luxo}"]; A6 --> C6["{Família}"];
```

Diagrama de divisão binária para o atributo "Tipo de Carro". O nó "Tipo de Carro" (amarelo) é dividido em dois sub-conjuntos. As opções mostradas são:

- 1. {Família, Esportivo} e {Luxo}
- 2. {Família, Luxo} e {Esportivo}
- 3. {Família, Esportivo} e {Luxo}
- 4. {Família, Luxo} e {Esportivo}
- 5. {Esportivo, Luxo} e {Família}
- 6. {Esportivo, Luxo} e {Família}

O texto "OU" aparece entre as opções 1 e 2, e "OU ...." aparece entre as opções 4 e 5.

Diagrama de divisão binária para o atributo 'Tipo de Carro'

{31}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-dcf37c460c66ec011dbe6ca08de44ff9_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de divisão múltipla para o atributo 'Tipo de Carro'
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-4f148853ae68fdcf5e43f7604cab457d_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de divisão binária para o atributo 'Tipo de Carro'
<!-- /IMAGE_DESCRIPTION -->
#### Divisão para atributos categóricos ordinais

- **Múltipla:** dividir com base no número de categorias

```
graph TD; Tamanho[Tamanho] --> Pequeno[Pequeno]; Tamanho --> Médio[Médio]; Tamanho --> Grande[Grande];
```

Diagrama de divisão múltipla para o atributo Tamanho. O nó Tamanho (amarelo) é dividido em três categorias: Pequeno, Médio e Grande.

Diagrama de divisão múltipla para o atributo Tamanho

- **Binária:** agregar categorias em dois sub-conjuntos. Necessário encontrar a divisão ótima.

```
graph TD; subgraph Option1; Tamanho1[Tamanho] --> P1["{Pequeno, Médio}"]; Tamanho1 --> G1["{Grande}"]; end; OU[OU]; subgraph Option2; Tamanho2[Tamanho] --> P2["{Pequeno}"]; Tamanho2 --> MG2["{Médio, Grande}"]; end;
```

Diagramas de divisão binária para o atributo Tamanho. O nó Tamanho (amarelo) é dividido em dois sub-conjuntos. A primeira opção divide em {Pequeno, Médio} e {Grande}. A segunda opção divide em {Pequeno} e {Médio, Grande}. O texto "OU" indica as duas opções possíveis.

Diagramas de divisão binária para o atributo Tamanho

- E esta divisão?

```
graph TD; Tamanho[Tamanho] --> PG["{Pequeno, Grande}"]; Tamanho --> M["{Médio}"];
```

Diagrama de divisão binária para o atributo Tamanho. O nó Tamanho (amarelo) é dividido em dois sub-conjuntos: {Pequeno, Grande} e {Médio}.

Diagrama de divisão binária para o atributo Tamanho

{32}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-14252bcd35912bd656e98b16b2ee51c0_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de divisão múltipla para o atributo Tamanho
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-9f9386d5b3d6cbeb1ed104a799320ebf_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagramas de divisão binária para o atributo Tamanho
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-a05e675f8651ae7ccea1d0d68691d1a9_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de divisão binária para o atributo Tamanho
<!-- /IMAGE_DESCRIPTION -->
#### Divisão para atributos contínuos

- **Múltipla:** discretizar os valores em intervalos

```
graph TD; Renda[Renda] --> L1["<= 10K"]; Renda --> L2["[10k,30k)"]; Renda --> L3["[30k,50k)"]; Renda --> L4["[50k,80k)"]; Renda --> L5["> 80K"];
```

A diagram showing a yellow rectangular node labeled "Renda". Five arrows point downwards from this node to five labels: "<= 10K", "[10k,30k)", "[30k,50k)", "[50k,80k)", and "> 80K".

Diagram illustrating multiple intervals for income discretization.

- **Binária:** definir ponto de divisão

```
graph TD; Renda[Renda] --> L1["<= 80K"]; Renda --> L2["> 80K"];
```

A diagram showing a yellow rectangular node labeled "Renda". Two arrows point downwards from this node to two labels: "<= 80K" and "> 80K".

Diagram illustrating binary division for income discretization.

{33}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-318886a86a1dcc59e1fc83db6f157c60_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram illustrating multiple intervals for income discretization.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-3e2a8dc8c5537dbe703cdcb0e21e4e1b_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram illustrating binary division for income discretization.
<!-- /IMAGE_DESCRIPTION -->
### Indução Top-Down

- Estratégia Recursiva
- Estratégia Gulosa (*greedy*)
  - Divide os registros com base em teste sobre atributo que otimiza localmente determinado critério
- Questões de Projeto
  - Determinar como particionar os dados
    - Como filtrar os dados com base em um atributo?
    - Como escolher o atributo a ser utilizado?
  - Determinar quando parar de particionar

{34}------------------------------------------------
### Como escolher o atributo?

Antes da divisão: 10 exemplos da classe 0  
10 exemplos da classe 1

Diagram illustrating three potential split attributes for a dataset:

- Carro próprio?** (Own car?):
  - S (Sim/Yes): C0:6, C1:4
  - N (Não/No): C0:4, C1:6
- Tipo de Carro** (Car Type):
  - Família (Family): C0:1, C1:3
  - Esportivo (Sports): C0:8, C1:0
  - Luxo (Luxury): C0:1, C1:7
- Matrícula Estudante** (Student ID):
  - 21101234: C0:1, C1:0
  - 21102345: C0:1, C1:0
  - 22101234: C0:0, C1:1
  - 22203456: C0:0, C1:1

Diagram showing three potential split attributes for a dataset. 'Carro próprio?' splits into two nodes: S (C0:6, C1:4) and N (C0:4, C1:6). 'Tipo de Carro' splits into three nodes: Família (C0:1, C1:3), Esportivo (C0:8, C1:0), and Luxo (C0:1, C1:7). 'Matrícula Estudante' splits into four nodes: 21101234 (C0:1, C1:0), 21102345 (C0:1, C1:0), 22101234 (C0:0, C1:1), and 22203456 (C0:0, C1:1), with ellipses between them.

Qual atributo é melhor para dividir os dados?

{35}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-dcc2d5a5b39f780e7a224bb01ba1ef6e_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram showing three potential split attributes for a dataset.
<!-- /IMAGE_DESCRIPTION -->
#### Como escolher o atributo?

- Estratégia gulosa
  - Dar preferência a nós com distribuição de classe **homogênea**
  - Para tanto, precisamos de uma medida para quantificar **impureza!**

The diagram illustrates two examples of node splitting in a decision tree. Each example shows a root node with a mix of red and blue dots, which splits into two child nodes. The left example shows a split that results in two child nodes with mixed classes. The right example shows a split that results in two child nodes that are perfectly separated by class (one with only red dots, one with only blue dots), indicating a better split for classification.

Diagram illustrating two examples of node splitting in a decision tree. Each example shows a root node with a mix of red and blue dots, which splits into two child nodes. The left example shows a split that results in two child nodes with mixed classes. The right example shows a split that results in two child nodes that are perfectly separated by class (one with only red dots, one with only blue dots), indicating a better split for classification.

{36}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-1142ba0197b158bb198186fe8baccc32_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram illustrating two examples of node splitting in a decision tree.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-3337af75dfee8af7687b4f49914d6c93_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree diagram showing splits on Atributo 1 and Atributo 2.
<!-- /IMAGE_DESCRIPTION -->
#### Qual o melhor atributo?

| <i>Tid</i> | <i>Restituição</i> | <i>Status Conjugal</i> | <i>Renda</i> | <i>Calote ?</i> |
|------------|--------------------|------------------------|--------------|-----------------|
| 1          | S                  | Solteiro               | 125K         | N               |
| 2          | N                  | Casado                 | 100K         | N               |
| 3          | N                  | Solteiro               | 70K          | N               |
| 4          | S                  | Casado                 | 120K         | N               |
| 5          | N                  | Divorc.                | 95K          | S               |
| 6          | N                  | Casado                 | 60K          | N               |
| 7          | S                  | Divorc.                | 220K         | N               |
| 8          | N                  | Solteiro               | 85K          | S               |
| 9          | N                  | Casado                 | 75K          | N               |
| 10         | N                  | Solteiro               | 90K          | S               |

*categorico*

*Categorico*

*contínuo*

*classe*

```

graph TD
    Root[Restituição] -- S --> LeafN[N]
    Root -- N --> LeafS[S]
    LeafN --- StatsN["Acertos = 3  
Erros = 0"]
    LeafS --- StatsS["Acertos = 3  
Erros = 4"]
    StatsN --- Accuracy["60%"]
    StatsS --- Accuracy
  
```

Decision tree diagram showing 'Restituição' as the root node with two branches: 'S' leading to a leaf node 'N' (Acertos = 3, Erros = 0) and 'N' leading to a leaf node 'S' (Acertos = 3, Erros = 4). The overall accuracy is 60%.

Conjunto de Treino

{37}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-fb18a83d10ebdad8e3e5ea2e86b36136_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree diagram showing 'Restituição' as the root node with two branches: 'S' leading to a leaf node 'N' (Acertos = 3, Erros = 0) and 'N' leading to a leaf node 'S' (Acertos = 3, Erros = 4).
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-f5a5f52bc25d95a7f616290c99e88ae6_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree diagram showing a root node 'B?' with two branches: 'Sim' leading to 'Nó N1' and 'Não' leading to 'Nó N2'.
<!-- /IMAGE_DESCRIPTION -->
#### Qual o melhor atributo?

| Tid | Restituição | Status Conjugal | Rendim. Tributáveis | Calote ? |
|-----|-------------|-----------------|---------------------|----------|
| 1   | S           | Solteiro        | 125K                | N        |
| 2   | N           | Casado          | 100K                | N        |
| 3   | N           | Solteiro        | 70K                 | N        |
| 4   | S           | Casado          | 120K                | N        |
| 5   | N           | Divorc.         | 95K                 | S        |
| 6   | N           | Casado          | 60K                 | N        |
| 7   | S           | Divorc.         | 220K                | N        |
| 8   | N           | Solteiro        | 85K                 | S        |
| 9   | N           | Casado          | 75K                 | N        |
| 10  | N           | Solteiro        | 90K                 | S        |

Conjunto de Treino

**Árvore 1:**

- Root: Status Conjugal
- Branches: Solteiro, Casado, Divorc.
- Leaf nodes: S, N, S
- Performance:
  - Solteiro: Acertos = 2, Erros = 2
  - Casado: Acertos = 4, Erros = 0
  - Divorc.: Acertos = 1, Erros = 1
  - Overall: 70%

**Árvore 2:**

- Root: Status Conjugal
- Branches: Solteiro, Divorc., Casado
- Leaf nodes: S, N
- Performance:
  - Solteiro, Divorc.: Acertos = 3, Erros = 3
  - Casado: Acertos = 4, Erros = 0
  - Overall: 70%

Two decision trees showing the performance of 'Status Conjugal' as a split attribute. The first tree splits into three leaf nodes: Solteiro (S), Casado (N), and Divorc. (S). The second tree splits into two leaf nodes: Solteiro, Divorc. (S) and Casado (N). Both trees show 70% accuracy.

{38}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-6629e8a87e7552e2454b7c3e9f6d73a0_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Two decision trees showing the performance of 'Status Conjugal' as a split attribute.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-b58cedaf15ad4f0edee5621820865ccc_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Two decision trees showing splits on 'Renda' attribute.
<!-- /IMAGE_DESCRIPTION -->
#### Qual o melhor atributo?

*categórico* *Categórico* *contínuo* *classe*

| Tid | Restituição | Status Conjugal | Rendim. Tributáveis | Calote ? |
|-----|-------------|-----------------|---------------------|----------|
| 1   | S           | Solteiro        | 125K                | N        |
| 2   | N           | Casado          | 100K                | N        |
| 3   | N           | Solteiro        | 70K                 | N        |
| 4   | S           | Casado          | 120K                | N        |
| 5   | N           | Divorc.         | 95K                 | S        |
| 6   | N           | Casado          | 60K                 | N        |
| 7   | S           | Divorc.         | 220K                | N        |
| 8   | N           | Solteiro        | 85K                 | S        |
| 9   | N           | Casado          | 75K                 | N        |
| 10  | N           | Solteiro        | 90K                 | S        |

| Rendim. Tributáveis | Calote ? |
|---------------------|----------|
| 60K                 | N        |
| 70K                 | N        |
| 75K                 | N        |
| 85K                 | S        |
| 90K                 | S        |
| 95K                 | S        |
| 100K                | N        |
| 120K                | N        |
| 125K                | N        |
| 220K                | N        |

← 80K

← 97K

Conjunto de Treino

**Tree 1 (Split at 80K):**

- Root: Renda
  - Left branch:  $\leq 80K$  → Leaf N (Acertos = 3, Erros = 0)
  - Right branch:  $> 80K$  → Leaf S (Acertos = 3, Erros = 4)
- Overall Accuracy: 60%

**Tree 2 (Split at 97K):**

- Root: Renda
  - Left branch:  $\leq 97K$  → Leaf S (Acertos = 3, Erros = 3)
  - Right branch:  $> 97K$  → Leaf N (Acertos = 4, Erros = 0)
- Overall Accuracy: 70%

Two decision trees showing splits on 'Renda' attribute. The first tree splits at 80K, and the second tree splits at 97K. Both show accuracy and error counts for each leaf node.

{39}------------------------------------------------
## Medidas para Impureza de Nodos

- Índice Gini

$$GINI(t) = 1 - \sum_j [p(j | t)]^2$$

$$GINI_{split} = \sum_{i=1}^k \frac{n_i}{n} GINI(i)$$

- Entropia

$$Entropy(t) = -\sum_j p(j | t) \log p(j | t)$$

- Erros de classificação

$$Error(t) = 1 - \max_i P(i | t)$$

<!-- DATALAB_CHUNK 3: pages 41-60 -->

{40}------------------------------------------------

# Índice Gini

- Índice Gini para um nó  $t$ :  $GINI(t) = 1 - \sum_j [p(j | t)]^2$

$p(j | t)$  é a frequência relativa da classe  $j$  no nó  $t$

- Valor máximo:  $1 - \frac{1}{c}$  (quando classes forem equiprováveis)
- Valor mínimo:  $0$  (quando todas instâncias pertencem à mesma classe)

|                   |   |
|-------------------|---|
| C1                | 0 |
| C2                | 6 |
| <b>Gini=0.000</b> |   |

|                   |   |
|-------------------|---|
| C1                | 1 |
| C2                | 5 |
| <b>Gini=0.278</b> |   |

|                   |   |
|-------------------|---|
| C1                | 2 |
| C2                | 4 |
| <b>Gini=0.444</b> |   |

|                   |   |
|-------------------|---|
| C1                | 3 |
| C2                | 3 |
| <b>Gini=0.500</b> |   |

{41}------------------------------------------------
## Índice Gini

$$GINI(t) = 1 - \sum_j [p(j|t)]^2$$

|    |          |
|----|----------|
| C1 | <b>0</b> |
| C2 | <b>6</b> |

$$P(C1) = 0/6 = 0 \quad P(C2) = 6/6 = 1$$

$$Gini = 1 - P(C1)^2 - P(C2)^2 = 1 - 0 - 1 = 0$$

|    |          |
|----|----------|
| C1 | <b>1</b> |
| C2 | <b>5</b> |

$$P(C1) = 1/6 \quad P(C2) = 5/6$$

$$Gini = 1 - (1/6)^2 - (5/6)^2 = 0.278$$

|    |          |
|----|----------|
| C1 | <b>2</b> |
| C2 | <b>4</b> |

$$P(C1) = 2/6 \quad P(C2) = 4/6$$

$$Gini = 1 - (2/6)^2 - (4/6)^2 = 0.444$$

{42}------------------------------------------------
## Computando uma divisão com o Índice Gini

- Quando um nó  $p$  é dividido em  $k$  partições (filhos), a qualidade dessa divisão é dada por:

$$GINI_{split} = \sum_{i=1}^k \frac{n_i}{n} GINI(i)$$

onde,

$n_i$  = número de exemplos no filho  $i$

$n$  = número de exemplos no nó pai  $p$

{43}------------------------------------------------
### Computando Índice Gini para Atributos Binários

$$GINI(t) = 1 - \sum_j [p(j|t)]^2$$

```

graph TD
    B((B?)) -- Sim --> N1[Nó N1]
    B -- Não --> N2[Nó N2]
  
```

Decision tree diagram showing a root node 'B?' with two branches: 'Sim' leading to 'Nó N1' and 'Não' leading to 'Nó N2'.

|                     | Pai |
|---------------------|-----|
| C1                  | 6   |
| C2                  | 6   |
| <b>Gini = 0.500</b> |     |

$$Gini(N1) = 1 - [(5/7)^2 + (2/7)^2] = 0.4082$$

|    | N1 | N2 |
|----|----|----|
| C1 | 5  | 1  |
| C2 | 2  | 4  |

$$Gini(N2) = 1 - [(1/5)^2 + (4/5)^2] = 0.32$$

$$GINI_{split} = \sum_{i=1}^k \frac{n_i}{n} GINI(i)$$

$$Gini(divisão) = [(7/12) * 0.4082] + [(5/12) * 0.32] = 0.37145$$

{44}------------------------------------------------
### Árvore elementar: Calculando o Índice GINI

| <i>Tid</i> | <i>Restitui<br/>ção</i> | <i>Status<br/>Conjugal</i> | <i>Renda</i> | <i>Calote<br/>?</i> |
|------------|-------------------------|----------------------------|--------------|---------------------|
| 1          | S                       | Solteiro                   | 125K         | N                   |
| 2          | N                       | Casado                     | 100K         | N                   |
| 3          | N                       | Solteiro                   | 70K          | N                   |
| 4          | S                       | Casado                     | 120K         | N                   |
| 5          | N                       | Divorc.                    | 95K          | S                   |
| 6          | N                       | Casado                     | 60K          | N                   |
| 7          | S                       | Divorc.                    | 220K         | N                   |
| 8          | N                       | Solteiro                   | 85K          | S                   |
| 9          | N                       | Casado                     | 75K          | N                   |
| 10         | N                       | Solteiro                   | 90K          | S                   |

*categórico*

*Categórico*

*contínuo*

*classe*

N

Acertos = 7  
Erros = 3

70%

$$\text{Gini} = 1 - (7/10)^2 - (3/10)^2$$

$$\text{Gini} = 1 - 49/100 - 9/100$$

$$\text{Gini} = (100 - 49 - 9)/100$$

$$\text{Gini} = 0,42$$

Conjunto de Treino

{45}------------------------------------------------
#### Atributos Categóricos: Calculando o Índice GINI

| <i>Tid</i> | <i>categórico</i><br>Restituição | <i>Categórico</i><br>Status Conjugal | <i>contínuo</i><br>Renda | <i>classe</i><br>Calote ? |
|------------|----------------------------------|--------------------------------------|--------------------------|---------------------------|
| 1          | S                                | Solteiro                             | 125K                     | N                         |
| 2          | N                                | Casado                               | 100K                     | N                         |
| 3          | N                                | Solteiro                             | 70K                      | N                         |
| 4          | S                                | Casado                               | 120K                     | N                         |
| 5          | N                                | Divorc.                              | 95K                      | S                         |
| 6          | N                                | Casado                               | 60K                      | N                         |
| 7          | S                                | Divorc.                              | 220K                     | N                         |
| 8          | N                                | Solteiro                             | 85K                      | S                         |
| 9          | N                                | Casado                               | 75K                      | N                         |
| 10         | N                                | Solteiro                             | 90K                      | S                         |

Conjunto de Treino

```

graph TD
    Restituição[Restituição] -- S --> N1[N]
    Restituição -- N --> S1[S]
    style Restituição fill:#ffff00,stroke:#000
    style N1 fill:#007bff,stroke:#000
    style S1 fill:#007bff,stroke:#000
  
```

Diagrama de árvore de decisão com nó raiz 'Restituição' (amarelo). O nó raiz tem duas saídas: 'S' para um nó folha 'N' (azul) e 'N' para um nó folha 'S' (azul).

Acertos = 3  
Erros = 0

$$Gini = 1 - (3/3)^2 - (0/3)^2$$

$$Gini = 1 - 1 - 0$$

$$Gini = 0,0$$

60%

Acertos = 3  
Erros = 4

$$Gini = 1 - (3/7)^2 - (4/7)^2$$

$$Gini = 1 - 9/49 - 16/49$$

$$Gini = (49 - 9 - 16)/49$$

$$Gini = 0,49$$

$$Gini_{split} = (3/10) * 0,0 + (7/10) * 0,49$$

$$Gini_{split} = 0 + 0,34$$

$$Gini_{split} = 0,34$$

{46}------------------------------------------------
#### Atributos Categóricos: Calculando Índice GINI

- Para cada valor distinto, apurar população para cada classe do conjunto de dados
- Usar a matriz com populações para tomar a decisão

Particionamento em n ramos

|      | TipoVeículo |           |      |
|------|-------------|-----------|------|
|      | Familiar    | Esportivo | Luxo |
| C1   | 1           | 2         | 1    |
| C2   | 4           | 1         | 1    |
| Gini | 0.393       |           |      |

Particionamento em 2 ramos  
(busca pela melhor divisão de valores)

|      | TipoVeículo        |            |      | TipoVeículo |                  |
|------|--------------------|------------|------|-------------|------------------|
|      | {Esportivo , Luxo} | {Familiar} |      | {Esportivo} | {Familiar ,Luxo} |
| C1   | 3                  | 1          | C1   | 2           | 2                |
| C2   | 2                  | 4          | C2   | 1           | 5                |
| Gini | 0.400              |            | Gini | 0.419       |                  |

{47}------------------------------------------------
#### Atributos Categóricos: Calculando o Índice GINI

| <i>Tid</i> | <i>Restitui<br/>ção</i> | <i>Status<br/>Conjugal</i> | <i>Renda</i> | <i>Calote<br/>?</i> |
|------------|-------------------------|----------------------------|--------------|---------------------|
| 1          | S                       | Solteiro                   | 125K         | N                   |
| 2          | N                       | Casado                     | 100K         | N                   |
| 3          | N                       | Solteiro                   | 70K          | N                   |
| 4          | S                       | Casado                     | 120K         | N                   |
| 5          | N                       | Divorc.                    | 95K          | S                   |
| 6          | N                       | Casado                     | 60K          | N                   |
| 7          | S                       | Divorc.                    | 220K         | N                   |
| 8          | N                       | Solteiro                   | 85K          | S                   |
| 9          | N                       | Casado                     | 75K          | N                   |
| 10         | N                       | Solteiro                   | 90K          | S                   |

Conjunto de Treino

Gini<sub>split</sub> = 0,3

Gini<sub>split</sub> = 0,3

**Diagrama 1:**

- Root: Status Conjugal
- Branches: Solteiro, Casado, Divorc.
- Leaf nodes: S, N, S
- Statistics for Solteiro (S): Acertos = 2, Erros = 2
- Statistics for Casado (N): Acertos = 4, Erros = 0
- Statistics for Divorc. (S): Acertos = 1, Erros = 1
- Weighted average: 70%

**Diagrama 2:**

- Root: Status Conjugal
- Branches: Solteiro, Divorc., Casado
- Leaf nodes: S, N
- Statistics for Solteiro, Divorc. (S): Acertos = 3, Erros = 3
- Statistics for Casado (N): Acertos = 4, Erros = 0
- Weighted average: 70%

Two decision tree diagrams illustrating Gini split calculations for the 'Status Conjugal' attribute. The first tree splits into three leaf nodes: Solteiro (S), Casado (N), and Divorc. (S). The second tree splits into two leaf nodes: Solteiro, Divorc. (S) and Casado (N).

{48}------------------------------------------------
#### Atributos Contínuos: Calculando o Índice GINI

- Para a eficiência computacional: para cada atributo,
  - Classificar valores existentes
  - Pesquisar linearmente estes valores, apurando a população envolvida, e calculando o índice GINI
  - Escolher a posição de particionamento que apresenta o menor índice GINI

| Calote                      | Renda |       |       |       |       |       |              |       |       |       |
|-----------------------------|-------|-------|-------|-------|-------|-------|--------------|-------|-------|-------|
|                             | 60    |       | 70    |       | 75    |       | 85           |       | 90    |       |
|                             | 95    |       | 100   |       | 120   |       | 125          |       | 220   |       |
|                             | 55    | 65    | 72    | 80    | 87    | 92    | 97           | 110   | 122   | 172   |
| Valores Ordenados           | <=    | >     | <=    | >     | <=    | >     | <=           | >     | <=    | >     |
| Posições de Particionamento | <=    | >     | <=    | >     | <=    | >     | <=           | >     | <=    | >     |
| S                           | 0     | 3     | 0     | 3     | 0     | 3     | 0            | 3     | 1     | 2     |
| N                           | 0     | 7     | 1     | 6     | 2     | 5     | 3            | 4     | 3     | 4     |
| Gini                        | 0.420 | 0.400 | 0.375 | 0.343 | 0.417 | 0.400 | <u>0.300</u> | 0.343 | 0.375 | 0.400 |

{49}------------------------------------------------
### Induzindo o 2o. Nível da árvore de decisão

*categórico*  
*Categórico*  
*contínuo*  
*classe*

| Tid | Restituição | Status Conjugal | Renda | Calote ? |
|-----|-------------|-----------------|-------|----------|
| 1   | S           | Solteiro        | 125K  | N        |
| 2   | N           | Casado          | 100K  | N        |
| 3   | N           | Solteiro        | 70K   | N        |
| 4   | S           | Casado          | 120K  | N        |
| 5   | N           | Divorc.         | 95K   | S        |
| 6   | N           | Casado          | 60K   | N        |
| 7   | S           | Divorc.         | 220K  | N        |
| 8   | N           | Solteiro        | 85K   | S        |
| 9   | N           | Casado          | 75K   | N        |
| 10  | N           | Solteiro        | 90K   | S        |

Conjunto de Treino

**Status Conjugal**

Solteiro, Divorc. → **S**  
Acertos = 3  
Erros = 3

Casado → **N**  
Acertos = 4  
Erros = 0

Aqui parou.

**Renda**

<= 97K → **S**  
Acertos = 3  
Erros = 1

> 97K → **N**  
Acertos = 2  
Erros = 0

Ginisplit = 0,25

**Restituição**

S → **N**  
Acertos = 2  
Erros = 0

N → **S**  
Acertos = 3  
Erros = 1

Ginisplit = 0,25

Decision tree diagram showing the induction of the second level. The root node is 'Status Conjugal' with branches 'Solteiro, Divorc.' leading to leaf 'S' (Acertos = 3, Erros = 3) and 'Casado' leading to leaf 'N' (Acertos = 4, Erros = 0). A text 'Aqui parou.' is next to the 'Casado' branch. Below, two potential split nodes are shown: 'Renda' with branches '<= 97K' leading to leaf 'S' (Acertos = 3, Erros = 1) and '> 97K' leading to leaf 'N' (Acertos = 2, Erros = 0); and 'Restituição' with branches 'S' leading to leaf 'N' (Acertos = 2, Erros = 0) and 'N' leading to leaf 'S' (Acertos = 3, Erros = 1). Both potential splits have a box below them containing 'Ginisplit = 0,25'.

{50}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-3442f31a562d1ef45bfa18b18a6a1ddc_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree diagram showing the induction of the second level.
<!-- /IMAGE_DESCRIPTION -->
### Induzindo o 3o. Nível da árvore de decisão

| <i>Tid</i> | <i>Restituição</i> | <i>Status Conjugal</i> | <i>Rendim. Tributáveis</i> | <i>Calote ?</i> |
|------------|--------------------|------------------------|----------------------------|-----------------|
| 1          | S                  | Solteiro               | 125K                       | N               |
| 2          | N                  | Casado                 | 100K                       | N               |
| 3          | N                  | Solteiro               | 70K                        | N               |
| 4          | S                  | Casado                 | 120K                       | N               |
| 5          | N                  | Divorc.                | 95K                        | S               |
| 6          | N                  | Casado                 | 60K                        | N               |
| 7          | S                  | Divorc.                | 220K                       | N               |
| 8          | N                  | Solteiro               | 85K                        | S               |
| 9          | N                  | Casado                 | 75K                        | N               |
| 10         | N                  | Solteiro               | 90K                        | S               |
## Conjunto de Treino

```
graph TD; A[Status Conjugal] -- "Solteiro, Divorc." --> B[Restituição]; A -- "Casado" --> C[N]; B -- "N" --> D[Renda]; B -- "S" --> E[N]; D -- "<= 80K" --> F[N]; D -- "> 80K" --> G[S];
```

Acertos = 1  
Erros = 0

Acertos = 3  
Erros = 0

Acertos = 2  
Erros = 0

Acertos = 4  
Erros = 0

Decision tree diagram showing splits on Status Conjugal, Restituição, and Renda.

$$\text{Gini}_{\text{split}} = 0,0$$

{51}------------------------------------------------
## Comparação entre os critérios de divisão

Para um problema de 2 classes:

O gráfico mostra a relação entre a probabilidade  $p$  (eixo x) e o valor de três critérios de divisão (eixo y) para um problema de 2 classes. O eixo x varia de 0 a 1, e o eixo y varia de 0 a 1. As três curvas são:

- Entropy** (curva vermelha): Representa a entropia de Shannon,  $H(p) = -p \log_2 p - (1-p) \log_2 (1-p)$ . É a curva mais alta, atingindo 1 no ponto  $p = 0.5$ .
- Gini** (curva azul): Representa o índice de Gini,  $G(p) = 1 - p^2 - (1-p)^2 = 2p(1-p)$ . É uma parábola com vértice em  $(0.5, 0.5)$ .
- Misclassification error** (curva preta): Representa o erro de classificação,  $E(p) = \min(p, 1-p)$ . É uma função triangular com vértice em  $(0.5, 0.5)$ .

| p   | Entropy | Gini | Misclassification error |
|-----|---------|------|-------------------------|
| 0.0 | 0.00    | 0.00 | 0.00                    |
| 0.1 | 0.46    | 0.18 | 0.10                    |
| 0.2 | 0.72    | 0.32 | 0.20                    |
| 0.3 | 0.88    | 0.42 | 0.30                    |
| 0.4 | 0.97    | 0.48 | 0.40                    |
| 0.5 | 1.00    | 0.50 | 0.50                    |
| 0.6 | 0.97    | 0.48 | 0.40                    |
| 0.7 | 0.88    | 0.42 | 0.30                    |
| 0.8 | 0.72    | 0.32 | 0.20                    |
| 0.9 | 0.46    | 0.18 | 0.10                    |
| 1.0 | 0.00    | 0.00 | 0.00                    |

Gráfico comparando Entropy, Gini e Misclassification error para um problema de 2 classes.

{52}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-4666738057044ad78ced4dbbc0c1bfb3_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Gráfico comparando Entropy, Gini e Misclassification error para um problema de 2 classes.
<!-- /IMAGE_DESCRIPTION -->
### Indução Top-Down

- Estratégia Recursiva
- Estratégia Gulosa (*greedy*)
  - Divide os registros com base em teste sobre atributo que otimiza localmente determinado critério
- Questões de Projeto
  - Determinar como particionar os dados
    - Como filtrar os dados com base em um atributo?
    - Como escolher o atributo a ser utilizado?
  - Determinar quando parar de particionar

{53}------------------------------------------------
### Critérios de Parada para Indução Top-Down

- Parar de expandir nós quando:
  - Todas instâncias forem da mesma classe (**homogeneidade de classe**)
  - Todos valores de atributos forem iguais (**homogeneidade de instâncias**)
  - Atingir **valor satisfatório do critério de divisão** (parâmetro)
  - Atingir **profundidade máxima** (parâmetro)
  - ...

{54}------------------------------------------------
## Vantagens e Desvantagens de Árvores de Decisão

- Vantagens:
  - Fácil de compreender (muito utilizadas por médicos!)
  - Possível gerar regras com base nas árvores
  - Custo baixo de geração do modelo:  $O(m' N \log N)$
  - Extremamente rápida para classificar novas instâncias
- Desvantagens:
  - Podem tornar-se **muito grandes**
  - Sujeitas a ***overfitting*** (super-ajuste aos dados)
  - Geram apenas hiperplanos paralelos aos eixos
    - Logo, não lidam bem com atributos correlacionados (por quê?)
  - Solução localmente ótima pode estar longe do ótimo global

{55}------------------------------------------------
## Visualização Geométrica de uma Árvore de Decisão

Objeto a ser classificado

A scatter plot illustrating the geometric visualization of a decision tree. The horizontal axis is labeled 'Atributo 1' and the vertical axis is labeled 'Atributo 2', both ranging from 1 to 10. The plot shows two classes of data points: blue circles (representing one class) and red squares with diagonal stripes (representing the other class). A purple diamond, labeled 'Objeto a ser classificado', is located at coordinates (4.5, 5.5). An arrow points from the text 'Objeto a ser classificado' to this diamond. The data points are distributed across the grid, with blue circles generally in the lower-left region and red squares in the upper-right region, though there is some overlap.

| Atributo 1 | Atributo 2 | Class                                    |
|------------|------------|------------------------------------------|
| 1          | 1          | Blue Circle                              |
| 1          | 2          | Blue Circle                              |
| 1          | 3          | Blue Circle                              |
| 1          | 4          | Blue Circle                              |
| 1          | 5          | Blue Circle                              |
| 1          | 6          | Blue Circle                              |
| 2          | 1          | Blue Circle                              |
| 2          | 2          | Blue Circle                              |
| 2          | 3          | Blue Circle                              |
| 2          | 4          | Blue Circle                              |
| 2          | 5          | Blue Circle                              |
| 2          | 6          | Blue Circle                              |
| 3          | 1          | Blue Circle                              |
| 3          | 2          | Blue Circle                              |
| 3          | 3          | Blue Circle                              |
| 3          | 4          | Blue Circle                              |
| 3          | 5          | Blue Circle                              |
| 3          | 6          | Blue Circle                              |
| 4          | 1          | Blue Circle                              |
| 4          | 2          | Blue Circle                              |
| 4          | 3          | Blue Circle                              |
| 4          | 4          | Blue Circle                              |
| 4          | 5          | Blue Circle                              |
| 4          | 6          | Blue Circle                              |
| 5          | 1          | Blue Circle                              |
| 5          | 2          | Blue Circle                              |
| 5          | 3          | Blue Circle                              |
| 5          | 4          | Blue Circle                              |
| 5          | 5          | Blue Circle                              |
| 5          | 6          | Blue Circle                              |
| 6          | 1          | Blue Circle                              |
| 6          | 2          | Blue Circle                              |
| 6          | 3          | Blue Circle                              |
| 6          | 4          | Blue Circle                              |
| 6          | 5          | Blue Circle                              |
| 6          | 6          | Blue Circle                              |
| 7          | 1          | Blue Circle                              |
| 7          | 2          | Blue Circle                              |
| 7          | 3          | Blue Circle                              |
| 7          | 4          | Blue Circle                              |
| 7          | 5          | Blue Circle                              |
| 7          | 6          | Blue Circle                              |
| 8          | 1          | Blue Circle                              |
| 8          | 2          | Blue Circle                              |
| 8          | 3          | Blue Circle                              |
| 8          | 4          | Blue Circle                              |
| 8          | 5          | Blue Circle                              |
| 8          | 6          | Blue Circle                              |
| 9          | 1          | Blue Circle                              |
| 9          | 2          | Blue Circle                              |
| 9          | 3          | Blue Circle                              |
| 9          | 4          | Blue Circle                              |
| 9          | 5          | Blue Circle                              |
| 9          | 6          | Blue Circle                              |
| 10         | 1          | Blue Circle                              |
| 10         | 2          | Blue Circle                              |
| 10         | 3          | Blue Circle                              |
| 10         | 4          | Blue Circle                              |
| 10         | 5          | Blue Circle                              |
| 10         | 6          | Blue Circle                              |
| 5          | 7          | Red Square                               |
| 6          | 7          | Red Square                               |
| 7          | 7          | Red Square                               |
| 8          | 7          | Red Square                               |
| 9          | 7          | Red Square                               |
| 10         | 7          | Red Square                               |
| 6          | 8          | Red Square                               |
| 7          | 8          | Red Square                               |
| 8          | 8          | Red Square                               |
| 9          | 8          | Red Square                               |
| 10         | 8          | Red Square                               |
| 7          | 9          | Red Square                               |
| 8          | 9          | Red Square                               |
| 9          | 9          | Red Square                               |
| 10         | 9          | Red Square                               |
| 8          | 10         | Red Square                               |
| 9          | 10         | Red Square                               |
| 10         | 10         | Red Square                               |
| 4.5        | 5.5        | Purple Diamond (Object to be classified) |

Scatter plot showing two classes of data points (blue circles and red squares) and a decision boundary. A purple diamond represents the object to be classified, located at (4.5, 5.5). An arrow points from the text 'Objeto a ser classificado' to this diamond.

{56}------------------------------------------------
### Visualização Geométrica de uma Árvore de Decisão

Objeto a ser classificado

The figure illustrates the geometric visualization of a decision tree. On the left, a scatter plot shows data points for two attributes, Atributo 1 (x-axis) and Atributo 2 (y-axis), both ranging from 1 to 10. The plot contains blue circles and red squares with diagonal stripes. A purple diamond, labeled 'Objeto a ser classificado', is located at coordinates (4.5, 5.5). An arrow points from this label to the diamond. On the right, a decision tree diagram shows the classification logic. The root node is 'Atributo 1'. It has two branches:  $\leq 7$  leading to a node 'Atributo 2', and  $> 7$  leading to a leaf node containing a red square. The 'Atributo 2' node has two branches:  $\leq 6$  leading to a leaf node containing a blue circle, and  $> 6$  leading to a leaf node containing a red square. This tree structure corresponds to the regions in the scatter plot: points with Atributo 1 > 7 are red squares; points with Atributo 1 $\leq$ 7 and Atributo 2 > 6 are red squares; points with Atributo 1 $\leq$ 7 and Atributo 2 $\leq$ 6 are blue circles. The purple diamond at (4.5, 5.5) falls into the blue circle region.

```
graph TD; A[Atributo 1] -- "$\leq$ 7" --> B[Atributo 2]; A -- "> 7" --> C[Red Square]; B -- "$\leq$ 6" --> D[Blue Circle]; B -- "> 6" --> E[Red Square]; style C fill:#ccc; style D fill:#ccc; style E fill:#ccc;
```

Scatter plot and decision tree diagram illustrating geometric visualization of a decision tree.

{57}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-ed0b26302ff3a12af19932430728ba03_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Scatter plot and decision tree diagram illustrating geometric visualization of a decision tree.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-99ff399927193b5527d8283e2a74747b_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A scatter plot and a decision tree diagram illustrating the geometric visualization of a decision tree.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-9996a51651209af4c8adad41ffe45393_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A scatter plot and a decision tree diagram illustrating the geometric visualization of a decision tree.
<!-- /IMAGE_DESCRIPTION -->
### Visualização Geométrica de uma Árvore de Decisão

Objeto a ser classificado

A scatter plot illustrating the geometric representation of a decision tree. The x-axis is labeled 'Atributo 1' and the y-axis is labeled 'Atributo 2', both ranging from 1 to 10. The plot shows two classes of data points: blue circles (representing one class) and red squares with diagonal stripes (representing another class). A purple diamond, labeled 'Objeto a ser classificado', is located at coordinates (4.5, 5.5). The data points are scattered across the plot, with blue circles generally in the lower-left region and red squares in the upper-right region.

Scatter plot showing data points for two classes (blue circles and red squares) and a decision boundary. A purple diamond represents the object to be classified.

A decision tree diagram illustrating the classification process. The root node is 'Atributo 1', which splits into two branches:  $\leq 7$  (left) and  $> 7$  (right). The  $\leq 7$  branch leads to a node 'Atributo 2', which further splits into two branches:  $\leq 6$  (left) and  $> 6$  (right). The  $\leq 6$  branch leads to a leaf node containing a blue circle, and the  $> 6$  branch leads to a leaf node containing a red square. The  $> 7$  branch from the root leads directly to a leaf node containing a red square.

Decision tree diagram showing splits on Atributo 1 and Atributo 2.

{58}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-d5c71a9a4fb2ffa3da1aa89ccbcf195e_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Scatter plot showing two classes of data points (blue circles and red squares) and a decision boundary.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-e9bc763ebea46fe89aede23775517f44_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Scatter plot showing data points for two classes (blue circles and red squares) and a decision boundary.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-4c547ec1af44f8fcdc8b1d67662ac30a_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Scatter plot showing data points and a decision boundary.
<!-- /IMAGE_DESCRIPTION -->
### Visualização Geométrica de uma Árvore de Decisão

Objeto a ser classificado

A scatter plot illustrating the geometric representation of a decision tree. The x-axis is labeled 'Atributo 1' and the y-axis is labeled 'Atributo 2', both ranging from 1 to 10. The plot contains blue circles and red squares with diagonal stripes. A vertical orange line at x=7 acts as a decision boundary. A purple diamond, labeled 'Objeto a ser classificado', is located at coordinates (4.5, 5.5) and has an arrow pointing to it from the text label.

Scatter plot showing data points and a decision boundary.

A decision tree diagram corresponding to the scatter plot. The root node is a brown rectangle labeled 'Atributo 1'. It has two branches: ' $\leq 7$ ' leading to a white rectangle labeled 'Atributo 2', and ' $> 7$ ' leading to a grey rectangle containing a red square with diagonal stripes. The 'Atributo 2' node has two branches: ' $\leq 6$ ' leading to a grey rectangle containing a blue circle, and ' $> 6$ ' leading to a grey rectangle containing a red square with diagonal stripes.

Decision tree diagram.

{59}------------------------------------------------
### Visualização Geométrica de uma Árvore de Decisão

Objeto a ser classificado

The figure illustrates the geometric visualization of a decision tree. On the left, a scatter plot shows data points for two classes (blue circles and red squares) on a 2D grid of Atributo 1 (x-axis) and Atributo 2 (y-axis). A vertical orange line at Atributo 1 = 7 separates the two classes. A purple diamond, labeled "Objeto a ser classificado", is located at (4.5, 5.5). On the right, a decision tree diagram shows "Atributo 1" as the root node. It branches into two paths:  $\leq 7$  and  $> 7$ . The  $\leq 7$  path leads to a node "Atributo 2", which further branches into  $\leq 6$  and  $> 6$ . The  $\leq 6$  path leads to a leaf node containing a blue circle, and the  $> 6$  path leads to a leaf node containing a red square. The  $> 7$  path from the root leads to a leaf node containing a red square.

A scatter plot and a decision tree diagram illustrating the geometric visualization of a decision tree. The scatter plot shows data points for two classes (blue circles and red squares) on a 2D grid of Atributo 1 and Atributo 2. A vertical orange line at Atributo 1 = 7 separates the two classes. A purple diamond, labeled 'Objeto a ser classificado', is located at (4.5, 5.5). The decision tree on the right shows 'Atributo 1' as the root node with branches '$\leq$ 7' and '> 7'. The '$\leq$ 7' branch leads to a node 'Atributo 2', which has branches '$\leq$ 6' and '> 6'. The '$\leq$ 6' branch leads to a leaf node containing a blue circle, and the '> 6' branch leads to a leaf node containing a red square. The '> 7' branch from the root leads to a leaf node containing a red square.

<!-- DATALAB_CHUNK 4: pages 61-80 -->

{60}------------------------------------------------

# Visualização Geométrica de uma Árvore de Decisão

Objeto a ser classificado

The figure illustrates the geometric visualization of a decision tree. On the left, a scatter plot shows data points (blue circles and red squares) in a 2D space defined by 'Atributo 1' (x-axis) and 'Atributo 2' (y-axis). The plot is partitioned by a vertical line at x=7 and a horizontal line at y=6. A purple diamond, labeled 'Objeto a ser classificado', is located at (4.5, 5.5). On the right, the decision tree diagram shows 'Atributo 1' as the root node, branching into 'Atributo 2' for the left branch ($\leq$ 7) and a leaf node for the right branch (> 7). 'Atributo 2' further branches into two leaf nodes: one for the left branch ($\leq$ 6) containing a blue circle, and one for the right branch (> 6) containing a red square.

```
graph TD; A[Atributo 1] -- "$\leq$ 7" --> B[Atributo 2]; A -- "> 7" --> C[Red Square]; B -- "$\leq$ 6" --> D[Blue Circle]; B -- "> 6" --> E[Red Square];
```

A scatter plot and a decision tree diagram illustrating the geometric visualization of a decision tree. The scatter plot shows data points (blue circles and red squares) in a 2D space defined by 'Atributo 1' (x-axis) and 'Atributo 2' (y-axis). The plot is partitioned by a vertical line at x=7 and a horizontal line at y=6. A purple diamond, labeled 'Objeto a ser classificado', is located at (4.5, 5.5). The decision tree diagram shows 'Atributo 1' as the root node, branching into 'Atributo 2' for the left branch ($\leq$ 7) and a leaf node for the right branch (> 7). 'Atributo 2' further branches into two leaf nodes: one for the left branch ($\leq$ 6) containing a blue circle, and one for the right branch (> 6) containing a red square.

{61}------------------------------------------------
## Espaço de Hipóteses

- Cada percurso da raiz até o nó folha representa uma **regra de classificação**
- Cada nó folha
  - Está associado a uma classe
  - Corresponde a **uma região do domínio dos atributos**
    - **Hiper-retângulo**
    - Intersecção de hiper-retângulos é vazia
    - União é o espaço total

{62}------------------------------------------------
## Espaço de Hipóteses

The diagram illustrates a decision tree and its corresponding hypothesis space plot.

**Decision Tree:**

- The root node is a green rectangle labeled  $A$ .
- From  $A$ , two branches emerge:  $\leq a_1$  (left) and  $> a_1$  (right).
- Both branches lead to green rectangles labeled  $B$ .
- From the left  $B$  node, two branches emerge:  $\leq b_2$  (left) leading to a red rectangle, and  $> b_2$  (right) leading to a green rectangle labeled  $A$ .
- From the right  $B$  node, two branches emerge:  $\leq b_3$  (left) leading to a purple rectangle, and  $> b_3$  (right) leading to a yellow rectangle.
- From the middle  $A$  node, two branches emerge:  $\leq a_4$  (left) leading to a dark gray rectangle, and  $> a_4$  (right) leading to a cyan rectangle.

**Hypothesis Space Plot:**

- The horizontal axis is labeled  $A$  and has tick marks at  $a_4$  and  $a_1$ .
- The vertical axis is labeled  $B$  and has tick marks at  $b_2$  and  $b_3$ .
- The plot is divided into several colored regions representing different hypotheses:
  - A dark gray region is at the top left, bounded by  $A \leq a_4$  and  $B \geq b_2$ .
  - A cyan region is to the right of the gray region, bounded by  $a_4 < A \leq a_1$  and  $B \geq b_2$ .
  - A yellow region is at the top right, bounded by  $A > a_1$  and  $B \geq b_3$ .
  - A large red region is at the bottom left, bounded by  $A \leq a_1$  and  $B < b_2$ .
  - A purple region is at the bottom right, bounded by  $A > a_1$  and  $B < b_3$ .

Decision tree and its corresponding hypothesis space plot.

{63}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-feae5a5b6e128162dbced0860fd97b9b_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree and its corresponding hypothesis space plot.
<!-- /IMAGE_DESCRIPTION -->
### De árvores para regras

```
graph TD; A1[A] -- "$\leq$ a1" --> B1[B]; A1 -- "> a1" --> B2[B]; B1 -- "$\leq$ b2" --> L1[Red]; B1 -- "> b2" --> A2[A]; A2 -- "$\leq$ a4" --> L2[Gray]; A2 -- "> a4" --> L3[Cyan]; B2 -- "$\leq$ b3" --> L4[Orange]; B2 -- "> b3" --> L5[Yellow];
```

A decision tree diagram illustrating the conversion of tree structures into logical rules. The tree starts with a root node 'A' (green rectangle). It branches into two nodes 'B' (green rectangles) based on the condition  $\leq a_1$  (left) and  $> a_1$  (right). The left 'B' node branches into a red leaf (labeled  $\leq b_2$ ) and another 'A' node (green rectangle) based on  $\leq b_2$  and  $> b_2$ . The right 'A' node branches into a gray leaf (labeled  $\leq a_4$ ) and a cyan leaf (labeled  $> a_4$ ). The right 'B' node branches into an orange leaf (labeled  $\leq b_3$ ) and a yellow leaf (labeled  $> b_3$ ).

Decision tree diagram showing splits on attributes A and B leading to colored leaf nodes.

Regras: disjunções de conjunções lógicas

1. **Se**  $A \leq a_1$  **E**  $B \leq b_2$  **Então** Classe = Vermelha  
**OU**
2. **Se**  $A > a_1$  **E**  $B \leq b_3$  **Então** Classe = Laranja  
**OU**
- ...

Exercício: complete as regras !

{64}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-0897c77315bfe37a098f6b4ea39570d2_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree diagram showing splits on attributes A and B leading to colored leaf nodes.
<!-- /IMAGE_DESCRIPTION -->
## Busca no Espaço de Hipóteses

- Não há **backtracking**
  - Impureza é minimizada localmente em cada nó!
    - Suposição: soma dos ótimos locais aproxima bem o ótimo global
- Espaço de hipóteses completo
  - A função objetivo certamente está contida nele
  - Sem *bias* de restrição
    - Proporcionando chances de *overfitting*
  - Com *bias* de busca (preferência)
    - Árvores com atributos que geram maior redução de impureza estão acima na árvore
    - Tal *bias* implica em tendência para árvores mais curtas

{65}------------------------------------------------
## Underfitting and Overfitting

The graph illustrates the relationship between the number of nodes and the error rate for both training and test sets. The x-axis represents the 'Number of nodes' from 0 to 300, and the y-axis represents the 'Error (%)' from 5 to 45. A vertical dashed red line at approximately 180 nodes marks the point of overfitting. To the right of this line, the label 'Overfitting' is present. The legend indicates that the solid red line represents the 'Training set' and the dashed blue line represents the 'Test set'.

| Number of nodes | Training set Error (%) | Test set Error (%) |
|-----------------|------------------------|--------------------|
| 0               | 38                     | 43                 |
| 50              | 28                     | 35                 |
| 100             | 22                     | 32                 |
| 150             | 16                     | 33                 |
| 180             | 14                     | 33                 |
| 200             | 12                     | 35                 |
| 250             | 9                      | 38                 |
| 260             | 9                      | 38                 |

Line graph showing Error (%) vs Number of nodes. The training set error (solid red line) decreases as nodes increase, while the test set error (dashed blue line) initially decreases then increases, indicating overfitting after approximately 180 nodes.

Underfitting: quando o modelo é simples demais, ambos erros, de treino e de teste, são grandes.

{66}------------------------------------------------

# Regressão

A blue icon representing a bar chart, consisting of five vertical bars of varying heights, positioned inside a white circle. The bars are arranged from left to right, with heights approximately 1.5, 2.5, 3.5, 2.5, and 1.5 units. The icon is centered within a white circle, which is set against a dark blue background.

Icon representing regression analysis, showing a bar chart with five bars of varying heights inside a white circle.

{67}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-2865fd60541ac34a704bc9e7af1041f7_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Line graph showing Error (%) vs Number of nodes.
<!-- /IMAGE_DESCRIPTION -->
## Árvores de Decisão para Problemas de Regressão

- Árvores de Regressão
  - Folha contém **média dos valores** do atributo alvo dos exemplos de treino que chegam até lá

```
graph TD; CHMIN((CHMIN)) -- "$\leq$ 7.5" --> CACH((CACH)); CHMIN -- "> 7.5" --> MMAX1((MMAX)); CACH -- "$\leq$ 8.5" --> MMAX2((MMAX)); CACH -- "(8.5, 28]" --> L1["64.6 (24/19.2%)"]; CACH -- "> 28" --> MMAX3((MMAX)); MMAX1 -- "$\leq$ 28000" --> L2["157 (21/73.7%)"]; MMAX1 -- "> 28000" --> CHMAX((CHMAX)); MMAX2 -- "$\leq$ 2500" --> L3["19.3 (28/8.7%)"]; MMAX2 -- "(2500, 4250]" --> L4["29.8 (37/8.18%)"]; MMAX2 -- "> 4250" --> CACH2((CACH)); MMAX3 -- "$\leq$ 10000" --> L5["75.7 (10/24.6%)"]; MMAX3 -- "> 10000" --> L6["133 (16/28.8%)"]; CHMAX -- "$\leq$ 58" --> MMIN((MMIN)); CHMAX -- "> 58" --> L7["783 (5/35.9%)"]; CACH2 -- "$\leq$ 0.5" --> MYCT((MYCT)); CACH2 -- "(0.5, 8.5]" --> L8["59.3 (24/16.9%)"]; MMIN -- "$\leq$ 12000" --> L9["281 (11/56%)"]; MMIN -- "> 12000" --> L10["492 (7/53.9%)"]; MYCT -- "$\leq$ 550" --> L11["37.3 (19/11.3%)"]; MYCT -- "> 550" --> L12["18.3 (7/3.83%)"];
```

Diagrama de uma Árvore de Regressão. O nó raiz é CHMIN. As folhas contêm a média dos valores do atributo alvo e a proporção de exemplos de treino que chegam até lá.

- CHMIN (Raiz)
  - $\leq$ 7.5: CACH
    - $\leq$ 8.5: MMAX
      - $\leq$ 2500: 19.3 (28/8.7%)
      - (2500, 4250]: 29.8 (37/8.18%)
      - > 4250: CACH
        - $\leq$ 0.5: MYCT
          - $\leq$ 550: 37.3 (19/11.3%)
          - > 550: 18.3 (7/3.83%)
        - (0.5, 8.5]: 59.3 (24/16.9%)
    - (8.5, 28]: 64.6 (24/19.2%)
    - > 28: MMAX
      - $\leq$ 10000: 75.7 (10/24.6%)
      - > 10000: 133 (16/28.8%)
  - > 7.5: MMAX
    - $\leq$ 28000: 157 (21/73.7%)
    - > 28000: CHMAX
      - $\leq$ 58: MMIN
        - $\leq$ 12000: 281 (11/56%)
        - > 12000: 492 (7/53.9%)
      - > 58: 783 (5/35.9%)

Diagrama de uma Árvore de Regressão com o nó raiz CHMIN.

{68}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-27788c2a26d9641e68232a4eff1299b9_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de uma Árvore de Regressão com o nó raiz CHMIN.
<!-- /IMAGE_DESCRIPTION -->
## Árvores de Decisão para Problemas de Regressão

- Árvores de Modelos
  - Folha contém **função de regressão (não-)linear** calculada sobre as instâncias que chegam até lá

![Diagrama de uma árvore de decisão para regressão. A raiz é CHMIN. Se CHMIN $\leq$ 7.5, vai para CACH. Se CHMIN > 7.5, vai para MMAX. De CACH, se $\leq$ 8.5, vai para MMAX; se > 8.5, vai para LM4 (50/22.1%). De MMAX (à esquerda), se $\leq$ 4250, vai para LM1 (65/7.32%); se > 4250, vai para CACH. De CACH (à esquerda), se $\leq$ 0.5, vai para LM2 (26/6.37%); se (0.5, 8.5], vai para LM3 (24/14.5%). De MMAX (à direita), se $\leq$ 28000, vai para LM5 (21/45.5%); se > 28000, vai para LM6 (23/63.5%). À direita do diagrama estão as fórmulas de regressão para cada folha.](e2b7490a3455c66c85db12872c78fcc3_img.jpg)

```
graph TD; CHMIN((CHMIN)) -- "$\leq$ 7.5" --> CACH1((CACH)); CHMIN -- "> 7.5" --> MMAX1((MMAX)); CACH1 -- "$\leq$ 8.5" --> MMAX2((MMAX)); CACH1 -- "> 8.5" --> LM4["LM4 (50/22.1%)"]; MMAX2 -- "$\leq$ 4250" --> LM1["LM1 (65/7.32%)"]; MMAX2 -- "> 4250" --> CACH2((CACH)); CACH2 -- "$\leq$ 0.5" --> LM2["LM2 (26/6.37%)"]; CACH2 -- "(0.5, 8.5]" --> LM3["LM3 (24/14.5%)"]; MMAX1 -- "$\leq$ 28000" --> LM5["LM5 (21/45.5%)"]; MMAX1 -- "> 28000" --> LM6["LM6 (23/63.5%)"];
```

LM1 PRP=8.29+0.004 MMAX+2.77 CHMIN  
LM2 PRP=20.3+0.004 MMIN-3.99 CHMIN  
+0.946 CHMAX  
LM3 PRP=38.1+0.012 MMIN  
LM4 PRP=19.5+0.002 MMAX+0.698 CACH  
+0.969 CHMAX  
LM5 PRP=285-1.46 MYCT+1.02 CACH  
-9.39 CHMIN  
LM6 PRP=-65.8+0.03 MMIN-2.94 CHMIN  
+4.98 CHMAX

Diagrama de uma árvore de decisão para regressão. A raiz é CHMIN. Se CHMIN $\leq$ 7.5, vai para CACH. Se CHMIN > 7.5, vai para MMAX. De CACH, se $\leq$ 8.5, vai para MMAX; se > 8.5, vai para LM4 (50/22.1%). De MMAX (à esquerda), se $\leq$ 4250, vai para LM1 (65/7.32%); se > 4250, vai para CACH. De CACH (à esquerda), se $\leq$ 0.5, vai para LM2 (26/6.37%); se (0.5, 8.5], vai para LM3 (24/14.5%). De MMAX (à direita), se $\leq$ 28000, vai para LM5 (21/45.5%); se > 28000, vai para LM6 (23/63.5%). À direita do diagrama estão as fórmulas de regressão para cada folha.

{69}------------------------------------------------
### Exemplo de Árvore de Regressão

*categórico* *Categórico* *contínuo* *alvo*

| Tid | Restituição | Status Conjugal | Renda | Atraso |
|-----|-------------|-----------------|-------|--------|
| 1   | S           | Solteiro        | 125K  | 0      |
| 2   | N           | Casado          | 100K  | 1      |
| 3   | N           | Solteiro        | 70K   | 30     |
| 4   | S           | Casado          | 120K  | 2      |
| 5   | N           | Solteiro        | 95K   | 24     |
| 6   | N           | Casado          | 60K   | 3      |
| 7   | S           | Solteiro        | 220K  | 1      |
| 8   | N           | Solteiro        | 85K   | 36     |
| 9   | N           | Casado          | 75K   | 3      |
| 10  | N           | Solteiro        | 90K   | 30     |

Conjunto de Treino

*Atributos Explanatórios*

```
graph TD; Renda[Renda] -- "> 97.5K" --> L1["+1"]; Renda -- "<= 97.5K" --> StatusConjugal[Status Conjugal]; StatusConjugal -- Solteiro --> L2["+30"]; StatusConjugal -- Casado --> L3["+3"];
```

Diagrama de uma Árvore de Regressão baseada no conjunto de dados de treinamento. A árvore começa com a Renda no nó raiz. Se a Renda for maior que 97.5K, o valor de saída é +1. Se a Renda for menor ou igual a 97.5K, a árvore avança para o Status Conjugal. Se o Status Conjugal for Solteiro, o valor de saída é +30. Se o Status Conjugal for Casado, o valor de saída é +3.

Modelo: Árvore de Regressão

{70}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-0f6e3cdce0f01d6ccceabcced508bb5b_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de uma Árvore de Regressão baseada no conjunto de dados de treinamento.
<!-- /IMAGE_DESCRIPTION -->
### Exemplo de Árvore de Regressão

| Tid | Restituição | Status Conjugal | Renda | Atraso | Atraso Predito | Diferença |
|-----|-------------|-----------------|-------|--------|----------------|-----------|
| 1   | S           | Solteiro        | 125K  | 0      | 1              | 1         |
| 2   | N           | Casado          | 100K  | 1      | 1              | 0         |
| 3   | N           | Solteiro        | 70K   | 30     | 30             | 0         |
| 4   | S           | Casado          | 120K  | 2      | 1              | 1         |
| 5   | N           | Solteiro        | 95K   | 24     | 30             | 6         |
| 6   | N           | Casado          | 60K   | 3      | 3              | 0         |
| 7   | S           | Solteiro        | 220K  | 1      | 1              | 0         |
| 8   | N           | Solteiro        | 85K   | 36     | 30             | 6         |
| 9   | N           | Casado          | 75K   | 3      | 3              | 0         |
| 10  | N           | Solteiro        | 90K   | 30     | 30             | 0         |

Erro médio absoluto:

$$(1 + 1 + 6 + 6)/10 = 1,4$$

Raiz do erro médio quadrático:

$$\text{SQRT}((1+1+36+36)/10) = 2,72$$

{71}------------------------------------------------
### Exemplo de Árvore Modelo

categórico      Categorical      contínuo      alvo

| Tid | Restituição | Status Conjugal | Rendim. Tributáveis | Atraso |
|-----|-------------|-----------------|---------------------|--------|
| 1   | S           | Solteiro        | 125K                | 0      |
| 2   | N           | Casado          | 100K                | 1      |
| 3   | N           | Solteiro        | 70K                 | 30     |
| 4   | S           | Casado          | 120K                | 2      |
| 5   | N           | Solteiro        | 95K                 | 24     |
| 6   | N           | Casado          | 60K                 | 3      |
| 7   | S           | Solteiro        | 220K                | 1      |
| 8   | N           | Solteiro        | 85K                 | 36     |
| 9   | N           | Casado          | 75K                 | 3      |
| 10  | N           | Solteiro        | 90K                 | 30     |

Conjunto de Treino

Red arrow pointing from the training set to the model tree.

Atributo Explanatório

```

graph TD
    A[Rendim. Tributáveis] -- "> 97.5K" --> B[LM1]
    A -- "<= 97.5K" --> C[LM2]
    style A fill:#ffff00,stroke:#0000ff
    style B fill:#00bfff,stroke:#0000ff
    style C fill:#00bfff,stroke:#0000ff
  
```

LM num: 1  
 Delay =  

$$18.2396 * \text{Status Conjugal=Solteiro} - 0.1611 * \text{Rendim. Tributáveis} + 16.2853$$

LM num: 2  
 Delay =  

$$24.2168 * \text{Status Conjugal=Solteiro} - 0.1458 * \text{Rendim. Tributáveis} + 15.401$$

Modelo: Árvore de Regressão

{72}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-98987d547cba17427b4265c243e4ffbf_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Red arrow pointing from the training set to the model tree.
<!-- /IMAGE_DESCRIPTION -->
### Exemplo de Árvore Modelo

| Tid | Restituição | Status Conjugal | Renda | Atraso | Atraso Predito | Diferença |
|-----|-------------|-----------------|-------|--------|----------------|-----------|
| 1   | S           | Solteiro        | 125K  | 0      | 14,3874        | 14,3874   |
| 2   | N           | Casado          | 100K  | 1      | 0,1753         | 0,8247    |
| 3   | N           | Solteiro        | 70K   | 30     | 29,4118        | 0,5882    |
| 4   | S           | Casado          | 120K  | 2      | -3,0467        | 5,0467    |
| 5   | N           | Solteiro        | 95K   | 24     | 25,7668        | 1,7668    |
| 6   | N           | Casado          | 60K   | 3      | 6,653          | 3,653     |
| 7   | S           | Solteiro        | 220K  | 1      | -0,9171        | 1,9171    |
| 8   | N           | Solteiro        | 85K   | 36     | 27,2248        | 8,7752    |
| 9   | N           | Casado          | 75K   | 3      | 4,466          | 1,466     |
| 10  | N           | Solteiro        | 90K   | 30     | 26,4958        | 3,5042    |

Erro médio absoluto:  
4,193

Raiz do erro médio  
quadrático: 5,874

{73}------------------------------------------------
## Árvores de Decisão para Problemas de Regressão

- Principal mudança: medida de divisão de nós
  - Exemplo: standard deviation reduction (SDR)
    - Mesma fórmula genérica do “ganho”
    - Em vez de entropia ou Gini, apenas calcular o desvio padrão do atributo alvo para as instâncias de cada nó e ponderá-las pelas frequências

$$SDR = SD(v_{pai}) - \sum_{t=1}^k \frac{N(v_t)}{N} SD(v_t)$$

{74}------------------------------------------------
### Árvore elementar: Calculando o Índice GINI

| Tid | Restituição | Status Conjugal | Renda | Atraso |
|-----|-------------|-----------------|-------|--------|
| 1   | S           | Solteiro        | 125K  | 0      |
| 2   | N           | Casado          | 100K  | 1      |
| 3   | N           | Solteiro        | 70K   | 30     |
| 4   | S           | Casado          | 120K  | 2      |
| 5   | N           | Solteiro        | 95K   | 24     |
| 6   | N           | Casado          | 60K   | 3      |
| 7   | S           | Solteiro        | 220K  | 1      |
| 8   | N           | Solteiro        | 85K   | 36     |
| 9   | N           | Casado          | 75K   | 3      |
| 10  | N           | Solteiro        | 90K   | 30     |

*categórico* *Categórico* *contínuo* *alvo*

|               |       |
|---------------|-------|
| Média         | 13,00 |
| Desvio Padrão | 14,93 |

Conjunto de Treino

{75}------------------------------------------------
#### Atributos Categóricos: Calculando o Índice GINI

| <i>Tid</i> | <i>categórico</i><br>Restituição | <i>Categórico</i><br>Status Conjugal | <i>contínuo</i><br>Renda | <i>alvo</i><br>Atraso |
|------------|----------------------------------|--------------------------------------|--------------------------|-----------------------|
| 1          | S                                | Solteiro                             | 125K                     | 0                     |
| 2          | N                                | Casado                               | 100K                     | 1                     |
| 3          | N                                | Solteiro                             | 70K                      | 30                    |
| 4          | S                                | Casado                               | 120K                     | 2                     |
| 5          | N                                | Solteiro                             | 95K                      | 24                    |
| 6          | N                                | Casado                               | 60K                      | 3                     |
| 7          | S                                | Solteiro                             | 220K                     | 1                     |
| 8          | N                                | Solteiro                             | 85K                      | 36                    |
| 9          | N                                | Casado                               | 75K                      | 3                     |
| 10         | N                                | Solteiro                             | 90K                      | 30                    |

Conjunto de Treino

```

graph TD
    Root[Restituição] -- S --> Leaf1[1]
    Root -- N --> Leaf2[18,14]
  
```

Decision tree diagram showing 'Restituição' as the root node. It branches into two leaf nodes: 'S' leading to '1' and 'N' leading to '18,14'.

|                |      |
|----------------|------|
| Média          | 1,00 |
| Desvio Padrão  | 1,00 |
| Número valores | 3    |

|                |       |
|----------------|-------|
| Média          | 18,14 |
| Desvio Padrão  | 15,20 |
| Número valores | 7     |

$$SDR = 14,93 - 3/10 * 1,0 - 7/10 * 15,2$$

$$SDR = 14,93 - 0,3 - 10,64$$

$$SDR = 3,99$$

{76}------------------------------------------------
#### Atributos Categóricos: Calculando o Índice GINI

| <i>Tid</i> | <i>Restituição</i> | <i>Status Conjugal</i> | <i>Renda</i> | <i>Atraso</i> |
|------------|--------------------|------------------------|--------------|---------------|
| 1          | S                  | Solteiro               | 125K         | 0             |
| 2          | N                  | Casado                 | 100K         | 1             |
| 3          | N                  | Solteiro               | 70K          | 30            |
| 4          | S                  | Casado                 | 120K         | 2             |
| 5          | N                  | Solteiro               | 95K          | 24            |
| 6          | N                  | Casado                 | 60K          | 3             |
| 7          | S                  | Solteiro               | 220K         | 1             |
| 8          | N                  | Solteiro               | 85K          | 36            |
| 9          | N                  | Casado                 | 75K          | 3             |
| 10         | N                  | Solteiro               | 90K          | 30            |

*categórico*

*Categórico*

*contínuo*

*alvo*

Conjunto de Treino

```

graph TD
    A[Status Conjugal] -- Solteiro --> B[20,17]
    A -- Casado --> C[2,25]
    style A fill:#ffff00,stroke:#000
    style B fill:#00aaff,stroke:#000
    style C fill:#00aaff,stroke:#000
  
```

Diagrama de árvore de decisão com a raiz 'Status Conjugal' (amarela) dividindo para 'Solteiro' (média 20,17) e 'Casado' (média 2,25).

|                |       |
|----------------|-------|
| Média          | 20,17 |
| Desvio Padrão  | 15,70 |
| Número valores | 6     |

|                |      |
|----------------|------|
| Média          | 2,25 |
| Desvio Padrão  | 0,96 |
| Número valores | 4    |

$$SDR = 14,93 - 6/10 * 15,7 - 4/10 * 0,96$$

$$SDR = 14,93 - 9,42 - 0,38$$

$$SDR = 5,13$$

{77}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-91c33f8e1713989e8192322ec2d1212b_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de árvore de decisão com a raiz 'Status Conjugal' (amarela) dividindo para 'Solteiro' (média 20,17) e 'Casado' (média 2,25).
<!-- /IMAGE_DESCRIPTION -->
### Exemplo Ilustrativo

Considere a seguinte árvore de regressão e a tabela logo a seguir, cujo atributo alvo é Rendimiento\_Anual.

1: Preencha os valores para os nodos folha da árvore, a partir da tabela abaixo.

Weka Classifier Tree Visualizer: 15:17:43 - trees.M5P (TAN\_DecisionTree-weka.filters.unsupervised.attribute.Remove-R1)

Tree View

```
graph TD; A[Restitucao=] -- NAO --> B[Calote=]; A -- SIM --> C[Estado_Civil=]; B -- SIM --> D[95.0]; B -- NAO --> E[Estado_Civil=]; E -- SOLTEIRO --> F[ ]; E -- CASADO, DIVORCIADO --> G[ ]; C -- SOLTEIRO, CASADO --> H[ ]; C -- DIVORCIADO --> I[ ]
```

Viewer

Relation: TAN\_DecisionTree-weka.filters.unsupervised.attribute.Remove-R1

| No. | Restitucao<br>Nominal | Estado_Civil<br>Nominal | Calote<br>Nominal | Rendimiento_Anual<br>Numeric | Rend_Anual Predito<br>Numeric |
|-----|-----------------------|-------------------------|-------------------|------------------------------|-------------------------------|
| 1   | SIM                   | Solteiro                | NAO               | 125.0                        |                               |
| 2   | NAO                   | Casado                  | NAO               | 100.0                        |                               |
| 3   | NAO                   | Solteiro                | NAO               | 70.0                         |                               |
| 4   | SIM                   | Casado                  | NAO               | 120.0                        |                               |
| 5   | NAO                   | Divorciado              | SIM               | 95.0                         |                               |
| 6   | NAO                   | Casado                  | NAO               | 60.0                         |                               |
| 7   | SIM                   | Divorciado              | NAO               | 220.0                        |                               |

ERRO

$\Sigma$

Screenshot of Weka Classifier Tree Visualizer and a data table. The tree diagram shows a regression tree with splits on Restitucao, Calote, and Estado\_Civil. The table below shows 7 rows of data with columns for No., Restitucao, Estado\_Civil, Calote, Rendimiento\_Anual, and Rend\_Anual Predito. A red arrow points from the leaf node '95.0' in the tree to the value '95.0' in row 5 of the table.

{78}------------------------------------------------
### Exemplo Ilustrativo

Considere a seguinte árvore de regressão e a tabela logo a seguir, cujo atributo alvo é Rendimento\_Anual.

1: Preencha os valores para os nodos folha da árvore, a partir da tabela abaixo.

Weka Classifier Tree Visualizer: 15:17:43 - trees.M5P (TAN\_DecisionTree-weka.filters.unsupervised.attribute.Remove-R1)

Tree View

```
graph TD
    Root((Restituicao=)) -- NAO --> Calote((Calote=))
    Root -- SIM --> Estado_Civil1((Estado_Civil=))
    Calote -- SIM --> Leaf1[95.0]
    Calote -- NAO --> Estado_Civil2((Estado_Civil=))
    Estado_Civil2 -- SOLTEIRO --> Leaf2[70.0]
    Estado_Civil2 -- CASADO, DIVORCIADO --> Leaf3[ ]
    Estado_Civil1 -- SOLTEIRO, CASADO --> Leaf4[ ]
    Estado_Civil1 -- DIVORCIADO --> Leaf5[ ]
```

Viewer

Relation: TAN\_DecisionTree-weka.filters.unsupervised.attribute.Remove-R1

| No. | Restituicao<br>Nominal | Estado_Civil<br>Nominal | Calote<br>Nominal | Rendimento_Anual<br>Numeric | Rend_Anual Predito<br>Numeric |
|-----|------------------------|-------------------------|-------------------|-----------------------------|-------------------------------|
| 1   | SIM                    | Solteiro                | NAO               | 125.0                       |                               |
| 2   | NAO                    | Casado                  | NAO               | 100.0                       |                               |
| 3   | NAO                    | Solteiro                | NAO               | 70.0                        |                               |
| 4   | SIM                    | Casado                  | NAO               | 120.0                       |                               |
| 5   | NAO                    | Divorciado              | SIM               | 95.0                        |                               |
| 6   | NAO                    | Casado                  | NAO               | 60.0                        |                               |
| 7   | SIM                    | Divorciado              | NAO               | 220.0                       |                               |

ERRO

$\Sigma$

Weka Classifier Tree Visualizer showing a regression tree and a data table. The tree has a root node 'Restituicao=' with branches 'NAO' and 'SIM'. The 'NAO' branch leads to a node 'Calote=' with branches 'SIM' (leaf 95.0) and 'NAO' (node 'Estado\_Civil=' with branches 'SOLTEIRO' (leaf 70.0) and 'CASADO, DIVORCIADO' (empty box)). The 'SIM' branch leads to a node 'Estado\_Civil=' with branches 'SOLTEIRO, CASADO' (empty box) and 'DIVORCIADO' (empty box). The table below shows 7 rows of data with columns: No., Restituicao, Estado\_Civil, Calote, Rendimento\_Anual, and Rend\_Anual Predito. A red arrow points from the circled value 70.0 in the table to the circled leaf node 70.0 in the tree.

{79}------------------------------------------------
### Exemplo Ilustrativo

Considere a seguinte árvore de regressão e a tabela logo a seguir, cujo atributo alvo é Rendimento\_Anual.

1: Preencha os valores para os nodos folha da árvore, a partir da tabela abaixo.

The figure displays a Weka Classifier Tree Visualizer window showing a regression tree and a data table. The tree structure is as follows:

- Root node: Restituicao=
  - Branch NAO: Calote=
    - Branch SIM: Leaf node 95.0
    - Branch NAO: Estado\_Civil=
      - Branch SOLTEIRO: Leaf node 70.0
      - Branch CASADO, DIVORCIADO: Leaf node 80.0 (circled in red)
  - Branch SIM: Estado\_Civil=
    - Branch SOLTEIRO, CASADO: Leaf node (empty)
    - Branch DIVORCIADO: Leaf node (empty)

The data table below shows the following information:

| No. | Restituicao Nominal | Estado_Civil Nominal | Calote Nominal | Rendimento_Anual Numeric | Rend_Anual Predito Numeric |
|-----|---------------------|----------------------|----------------|--------------------------|----------------------------|
| 1   | SIM                 | Solteiro             | NAO            | 125.0                    |                            |
| 2   | NAO                 | Casado               | NAO            | 100.0 (circled in red)   |                            |
| 3   | NAO                 | Solteiro             | NAO            | 70.0                     |                            |
| 4   | SIM                 | Casado               | NAO            | 120.0                    |                            |
| 5   | NAO                 | Divorciado           | SIM            | 95.0                     |                            |
| 6   | NAO                 | Casado               | NAO            | 60.0 (circled in red)    |                            |
| 7   | SIM                 | Divorciado           | NAO            | 220.0                    |                            |

Red arrows from the tree's leaf nodes point to the corresponding rows in the table: the leaf node '95.0' points to row 5, the leaf node '70.0' points to row 3, and the circled leaf node '80.0' points to row 6. The circled values '100.0' and '60.0' in the table are also highlighted.

Weka Classifier Tree Visualizer showing a regression tree and a data table.

ERRO

$\Sigma$

<!-- DATALAB_CHUNK 5: pages 81-88 -->

{80}------------------------------------------------

# Exemplo Ilustrativo

Considere a seguinte árvore de regressão e a tabela logo a seguir, cujo atributo alvo é Rendimento\_Anual.

1: Preencha os valores para os nodos folha da árvore, a partir da tabela abaixo.

The figure displays a Weka Classifier Tree Visualizer window showing a regression tree and a data table. The tree structure is as follows:

- Root node: Restituicao=
  - Branch NAO: Calote=
    - Branch SIM: Leaf node 95.0
    - Branch NAO: Estado\_Civil=
      - Branch SOLTEIRO: Leaf node 70.0
      - Branch CASADO, DIVORCIADO: Leaf node 80.0
  - Branch SIM: Estado\_Civil=
    - Branch SOLTEIRO, CASADO: Leaf node 122.5 (circled in red)
    - Branch DIVORCIADO: Leaf node (empty)

The data table below shows the following information:

| No. | Restituicao Nominal | Estado_Civil Nominal | Calote Nominal | Rendimento_Anual Numeric | Rend. Anual Predito Numeric |
|-----|---------------------|----------------------|----------------|--------------------------|-----------------------------|
| 1   | SIM                 | Solteiro             | NAO            | 125.0 (circled in red)   |                             |
| 2   | NAO                 | Casado               | NAO            | 100.0                    |                             |
| 3   | NAO                 | Solteiro             | NAO            | 70.0                     |                             |
| 4   | SIM                 | Casado               | NAO            | 120.0 (circled in red)   |                             |
| 5   | NAO                 | Divorciado           | SIM            | 95.0                     |                             |
| 6   | NAO                 | Casado               | NAO            | 60.0                     |                             |
| 7   | SIM                 | Divorciado           | NAO            | 220.0                    |                             |

Red arrows indicate the mapping of data rows to leaf nodes: Row 1 (Rendimento\_Anual 125.0) and Row 4 (Rendimento\_Anual 120.0) both point to the leaf node 122.5. Row 3 (Rendimento\_Anual 70.0) points to the leaf node 70.0. Row 2 (Rendimento\_Anual 100.0) points to the leaf node 80.0. Row 5 (Rendimento\_Anual 95.0) points to the leaf node 95.0. Row 6 (Rendimento\_Anual 60.0) points to the empty leaf node under DIVORCIADO. Row 7 (Rendimento\_Anual 220.0) points to the leaf node 122.5.

Weka Classifier Tree Visualizer showing a regression tree and a data table.

ERRO

$\Sigma$

{81}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-92f8a2dda0aa6e2c03e3fe24131ab6fe_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Screenshot of Weka Classifier Tree Visualizer and a data table.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-b11f4bc2bbfc46968de10a8ad2a8902f_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Weka Classifier Tree Visualizer showing a regression tree and a data table.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-8e21461e0c9384ec60322bedb1b1ab17_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Weka Classifier Tree Visualizer showing a regression tree and a data table.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-e466e4c4fb08567a109bb959a765225c_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Weka Classifier Tree Visualizer showing a regression tree and a data table.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-f68421f5d184c116a7061977a9057e63_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Weka Classifier Tree Visualizer showing a regression tree and a data table.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-5e7b93195badf89e1fb645ae53d619bb_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Weka Classifier Tree Visualizer showing a regression tree and a data table.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-d461c6341beba90844ef785469cd757f_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Weka Classifier Tree Visualizer showing a regression tree and a data table.
<!-- /IMAGE_DESCRIPTION -->
## Exemplo Ilustrativo

Considere a seguinte árvore de regressão e a tabela logo a seguir, cujo atributo alvo é Rendimento\_Anual.

1: Preencha os valores para os nodos folha da árvore, a partir da tabela abaixo.

Weka Classifier Tree Visualizer: 15:17:43 - trees.M5P (TAN\_DecisionTree-weka.filters.unsupervised.attribute.Remove-R1)

Tree View

```
graph TD
    Restituicao((Restituicao=)) -- NAO --> Calote((Calote=))
    Restituicao -- SIM --> Estado_Civil((Estado_Civil=))
    Calote -- SIM --> Leaf1[95.0]
    Calote -- NAO --> Estado_Civil2((Estado_Civil=))
    Estado_Civil2 -- SOLTEIRO --> Leaf2[70.0]
    Estado_Civil2 -- CASADO, DIVORCIADO --> Leaf3[80.0]
    Estado_Civil -- SOLTEIRO, CASADO --> Leaf4[122.5]
    Estado_Civil -- DIVORCIADO --> Leaf5[220.0]
```

Viewer

Relation: TAN\_DecisionTree-weka.filters.unsupervised.attribute.Remove-R1

| No. | Restituicao<br>Nominal | Estado_Civil<br>Nominal | Calote<br>Nominal | Rendimento_Anual<br>Numeric | Rend_Anual Predito<br>Numeric |
|-----|------------------------|-------------------------|-------------------|-----------------------------|-------------------------------|
| 1   | SIM                    | Solteiro                | NAO               | 125.0                       |                               |
| 2   | NAO                    | Casado                  | NAO               | 100.0                       |                               |
| 3   | NAO                    | Solteiro                | NAO               | 70.0                        |                               |
| 4   | SIM                    | Casado                  | NAO               | 120.0                       |                               |
| 5   | NAO                    | Divorciado              | SIM               | 95.0                        |                               |
| 6   | NAO                    | Casado                  | NAO               | 60.0                        |                               |
| 7   | SIM                    | Divorciado              | NAO               | 220.0                       |                               |

$\Sigma$

Weka Classifier Tree Visualizer showing a regression tree and a data table. The tree has nodes for Restituicao, Calote, and Estado\_Civil. The table has columns for No., Restituicao, Estado\_Civil, Calote, Rendimento\_Anual, and Rend\_Anual Predito. A red arrow points from the circled value 220.0 in the table to the circled value 220.0 in the tree.

{82}------------------------------------------------
## Exemplo Ilustrativo

Considere a seguinte árvore de regressão e a tabela logo a seguir, cujo atributo alvo é Rendimento\_Anual.

1: Preencha os valores para os nodos folha da árvore, a partir da tabela abaixo.

The figure displays a Weka Classifier Tree Visualizer window showing a regression tree and a data table. The tree structure is as follows:

- Root node: Restituicao=
  - Branch NAO: Node Calote=
    - Branch SIM: Leaf 95.0
    - Branch NAO: Node Estado\_Civil=
      - Branch SOLTEIRO: Leaf 70.0
      - Branch CASADO, DIVORCIADO: Leaf 80.0
  - Branch SIM: Node Estado\_Civil=
    - Branch SOLTEIRO, CASADO: Leaf 122.5
    - Branch DIVORCIADO: Leaf 220.0

The data table below shows the original data and the predicted values from the tree. A red arrow points from the leaf node '122.5' in the tree to the value '122.5' in the 'Rend\_Anual Predito' column of the table.

| No. | Restituicao Nominal | Estado_Civil Nominal | Calote Nominal | Rendimento_Anual Numeric | Rend_Anual Predito Numeric |
|-----|---------------------|----------------------|----------------|--------------------------|----------------------------|
| 1   | SIM                 | Solteiro             | NAO            | 125.0                    | 122.5                      |
| 2   | NAO                 | Casado               | NAO            | 100.0                    |                            |
| 3   | NAO                 | Solteiro             | NAO            | 70.0                     |                            |
| 4   | SIM                 | Casado               | NAO            | 120.0                    |                            |
| 5   | NAO                 | Divorciado           | SIM            | 95.0                     |                            |
| 6   | NAO                 | Casado               | NAO            | 60.0                     |                            |
| 7   | SIM                 | Divorciado           | NAO            | 220.0                    |                            |

Weka Classifier Tree Visualizer showing a regression tree and a data table.

ERRO

$\Sigma$

{83}------------------------------------------------
## Exemplo Ilustrativo

Considere a seguinte árvore de regressão e a tabela logo a seguir, cujo atributo alvo é Rendimiento\_Anual.

1: Preencha os valores para os nodos folha da árvore, a partir da tabela abaixo.

The figure displays a Weka Classifier Tree Visualizer window showing a regression tree and a data table. The tree structure is as follows:

```

graph TD
    Root((Restitucao=)) -- NAO --> Calote((Calote=))
    Root -- SIM --> Estado_Civil((Estado_Civil=))
    Calote -- SIM --> Leaf1[95.0]
    Calote -- NAO --> Estado_Civil2((Estado_Civil=))
    Estado_Civil2 -- SOLTEIRO --> Leaf2[70.0]
    Estado_Civil2 -- CASADO, DIVORCIADO --> Leaf3[80.0]
    Estado_Civil -- SOLTEIRO, CASADO --> Leaf4[122.5]
    Estado_Civil -- DIVORCIADO --> Leaf5[220.0]
  
```

The data table below provides the actual and predicted values for each instance:

| No. | Restitucao<br>Nominal | Estado_Civil<br>Nominal | Calote<br>Nominal | Rendimento_Anual<br>Numeric | Rend_Anual Predito<br>Numeric |
|-----|-----------------------|-------------------------|-------------------|-----------------------------|-------------------------------|
| 1   | SIM                   | Solteiro                | NAO               | 125.0                       | 122.5                         |
| 2   | NAO                   | Casado                  | NAO               | 100.0                       | 80.0                          |
| 3   | NAO                   | Solteiro                | NAO               | 70.0                        | 70.0                          |
| 4   | SIM                   | Casado                  | NAO               | 120.0                       | 122.5                         |
| 5   | NAO                   | Divorciado              | SIM               | 95.0                        | 95.0                          |
| 6   | NAO                   | Casado                  | NAO               | 60.0                        | 80.0                          |
| 7   | SIM                   | Divorciado              | NAO               | 220.0                       | 220.0                         |

Weka Classifier Tree Visualizer showing a regression tree and a data table.

ERRO

$\Sigma$

{84}------------------------------------------------
## Exemplo Ilustrativo

Considere a seguinte árvore de regressão e a tabela logo a seguir, cujo atributo alvo é Rendimiento\_Anual.

1: Preencha os valores para os nodos folha da árvore, a partir da tabela abaixo.

The figure displays a Weka Classifier Tree Visualizer window showing a regression tree and a data viewer window showing a table of data. The tree structure is as follows:

```

    graph TD
      Root((Restituicao=)) -- NAO --> Calote((Calote=))
      Root -- SIM --> Estado_Civil((Estado_Civil=))
      Calote -- SIM --> Leaf1[95.0]
      Calote -- NAO --> Estado_Civil2((Estado_Civil=))
      Estado_Civil2 -- SOLTEIRO --> Leaf2[70.0]
      Estado_Civil2 -- CASADO, DIVORCIADO --> Leaf3[80.0]
      Estado_Civil -- SOLTEIRO, CASADO --> Leaf4[122.5]
      Estado_Civil -- DIVORCIADO --> Leaf5[220.0]
  
```

The data viewer window shows the following table:

| No. | Restituicao Nominal | Estado_Civil Nominal | Calote Nominal | Rendimento_Anual Numeric | Rend_Anual Predito Numeric |
|-----|---------------------|----------------------|----------------|--------------------------|----------------------------|
| 1   | SIM                 | Solteiro             | NAO            | 125.0                    | 122.5                      |
| 2   | NAO                 | Casado               | NAO            | 100.0                    | 80.0                       |
| 3   | NAO                 | Solteiro             | NAO            | 70.0                     | 70.0                       |
| 4   | SIM                 | Casado               | NAO            | 120.0                    | 122.5                      |
| 5   | NAO                 | Divorciado           | SIM            | 95.0                     | 95.0                       |
| 6   | NAO                 | Casado               | NAO            | 60.0                     | 80.0                       |
| 7   | SIM                 | Divorciado           | NAO            | 220.0                    | 220.0                      |

Weka Classifier Tree Visualizer showing a regression tree and a data viewer table.

Atenção! Erro é sempre Positivo!!!

| ERRO |
|------|
| 2.5  |
| 20.0 |
| 0.0  |
| 2.5  |
| 0.0  |
| 20.0 |
| 0.0  |

$\Sigma$

6.43

45 / 7

{85}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-57261b803cf2db0e8feca169cb2c416b_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Weka Classifier Tree Visualizer showing a regression tree and a data viewer table.
<!-- /IMAGE_DESCRIPTION -->
## Exemplos de Algoritmos
### - ID3 (Quinlan 1986)

- Iterative Dichotomiser 3
- Lida apenas com atributos nominais
- Medida de impureza: ganho de informação
- Tipo de poda: pré-poda (limite de instâncias)
### - C4.5 (Quinlan 1993)

- J48 (Weka), C5.0 (comercial)
- Atributos discretos e contínuos
- Medida de impureza: gain ratio
- Tipo de poda: pós-poda (error-based pruning)

{86}------------------------------------------------
## Exemplos de Algoritmos

- CART (Breiman et al. 1984)
  - Classification and Regression Trees
  - Árvores de Classificação e Regressão
  - Atributos discretos e contínuos
  - Divisões sempre binárias (agrega categorias)
  - Medida de impureza: índice Gini / twoing / sum of squares
  - Tipo de poda: pós-poda (cost-complexity pruning)

{87}------------------------------------------------
## Exemplos de Algoritmos

- M5 (Quinlan 1992)
  - M5P (Weka)
  - Árvores de Regressão e Árvores de Modelos
  - Atributos discretos e contínuos
  - Medida de impureza: SDR
  - Tipo de poda: erro corrigido (leva em conta o número de parâmetros dos modelos lineares)

<!-- IMAGE_DESCRIPTION_ORPHANS -->
## Imagens Curadas

Descrições preservadas para imagens detectadas no documento, mas sem referência markdown compatível no corpo principal.

<!-- IMAGE_DESCRIPTION: datalab-83f22ed94ec5517769dd76d702c6bfd8_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A crystal ball on a wooden stand, symbolizing a probabilistic model.
<!-- /IMAGE_DESCRIPTION -->
<!-- /IMAGE_DESCRIPTION_ORPHANS -->
