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
- **Aplicando o Modelo aos Dados de Teste**
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
  - Busca no Espaço de Hipóteses
- **Underfitting and Overfitting**
- **Regressão**
  - Árvores de Decisão para Problemas de Regressão
  - Árvores de Decisão para Problemas de Regressão
  - Exemplo de Árvore de Regressão
  - Exemplo de Árvore de Regressão
  - Exemplo de Árvore Modelo
  - Exemplo de Árvore Modelo
  - Árvores de Decisão para Problemas de Regressão
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

<!-- EXEC_SUMMARY_END -->
<!-- DATALAB_CHUNK 1: pages 1-20 -->

{0}------------------------------------------------

The image is a vertical composition. The top half features a dark blue background with a glowing, stylized brain circuit graphic in purple and blue, surrounded by concentric hexagonal lines and small light points. The bottom half shows a close-up, slightly blurred view of several colorful document folders (red, orange, yellow, green, blue) stacked together, with a bright light source creating a rainbow-like glow on the right side.

A composite image featuring a stylized brain circuit graphic on a dark blue background with glowing lines, and a close-up of colorful, blurred document folders at the bottom.
## Aprendizado Supervisionado Parte 2

Árvores de Decisão

Silvia Moraes

Material elaborado pelo prof. **Duncan Ruiz**

{1}------------------------------------------------
## Roteiro

Relembrando

- Machine Learning: Aprendizado Supervisionado

- Tarefas Preditivas

- Classificação & Regressão

- Árvores de Decisão

{2}------------------------------------------------
## Subáreas da Inteligência Artificial

The diagram illustrates the subfields of Artificial Intelligence (IA) arranged around a central aperture graphic. The central text reads "Inteligência Artificial (IA)".

**Machine Learning (Aprendizado de Máquina)** (highlighted in red):

- Aprendizado Profundo (Deep Learning)
- Aprendizado Supervisionado
- Aprendizado Não Supervisionado
- Aprendizado por Reforço
- Aprendizado auto-supervisionado
- Aprendizado semissupervisionado

**Processamento de Linguagem Natural**:

- Extração de Informações
- Classificação de Texto
- Tradução Automática
- Perguntas e Respostas
- Geração de Texto

**Other Subfields:**

- Raciocínio Automatizado
- Robótica
- IA Explicável
- Visão Computacional

Diagram showing the subfields of Artificial Intelligence (IA) arranged around a central aperture graphic.

{3}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-1b7d539e02a202c2cf2d97698b911447_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram showing the subfields of Artificial Intelligence (IA) arranged around a central aperture graphic.
<!-- /IMAGE_DESCRIPTION -->
### Aprendizado Supervisionado

Exige que os **dados** estejam **rotulados** (anotados com suas respectivas classes/valores de saída)

Os algoritmos que seguem esse tipo de aprendizado recebem pares de valores:

- os dados de entrada ( $x$ ) e
- os valores de saída (rótulos) correspondentes ( $y$ ).

**Saída (y):**  
rótulo/classe/anotação

**Entrada (x):**  
Imagem ou características

The diagram shows three examples of supervised learning data pairs. Each example consists of an input image (x) and a corresponding output label (y) in a blue box. The first example is a cat sitting on a windowsill, labeled 'Gato'. The second example is a dog's face, labeled 'Cachorro'. The third example is a chicken in a farm setting, labeled 'Galinha'. A URL 'https://www.pexels.com/' is visible between the dog and chicken images.

**Gato**

**Cachorro**

**Galinha**

Diagram illustrating supervised learning with three examples: a cat, a dog, and a chicken. Each image is labeled with its class name in a blue box.

**Dataset Anotado**

{4}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-d62e2e2281009c16f4ee61660e716cd9_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram illustrating supervised learning with three examples: a cat, a dog, and a chicken.
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

Three photographs of Iris flowers are shown side-by-side. The first is labeled 'Iris Virginica' and shows a blue and white flower. The second is labeled 'Iris Setosa' and shows a dark blue flower. The third is labeled 'Iris Versicolor' and shows a blue and purple flower.

Three photographs of Iris flowers: Iris Virginica (blue and white), Iris Setosa (dark blue), and Iris Versicolor (blue and purple).

{5}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-764bb8d7c93b090e205d908e1a8cade4_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Three photographs of Iris flowers: Iris Virginica (blue and white), Iris Setosa (dark blue), and Iris Versicolor (blue and purple).
<!-- /IMAGE_DESCRIPTION -->
### Aprendizado Supervisionado

O objetivo é encontrar um modelo capaz de mapear os valores de entrada ( $x$ ) nos valores de saída  $y$ .

Em outras palavras, que aproxime  $f$ , tal que  $f(x) = y$ .

Supervisão: ajuste usando o erro em relação à saída esperada.

The diagram illustrates the supervised learning process. On the left, a 'Dataset Anotado' (Annotated Dataset) is shown with three examples: a cat labeled 'Gato', a dog labeled 'Cachorro', and a chicken labeled 'Galinha'. An arrow points from this dataset to a central box representing the 'Algoritmo de Machine Learning Supervisionado' (Supervised Machine Learning Algorithm). Inside this box, the 'Treinamento' (Training) phase is depicted with a neural network icon. A second arrow points from the algorithm box to a final box labeled 'Modelo' (Model), which also contains a neural network icon.

Diagram of the supervised learning process: Dataset Anotado (Gato, Cachorro, Galinha) -> Algoritmo de Machine Learning Supervisionado (Treinamento) -> Modelo.

{6}------------------------------------------------

A crystal ball on a wooden stand, used as a metaphor for a probabilistic model. The crystal ball is dark and reflective, showing some light reflections. The text 'Modelo Probabilístico' is overlaid on the crystal ball.

Modelo Probabilístico

<!-- IMAGE_DESCRIPTION: datalab-f6d72d7c790e7f585532140f3971639a_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of the supervised learning process: Dataset Anotado (Gato, Cachorro, Galinha) -> Algoritmo de Machine Learning Supervisionado (Treinamento) -> Modelo.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-08a82c22d89d6b027ff69762ad096586_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A crystal ball on a wooden stand, used as a metaphor for a probabilistic model.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-8307f6b04df072c9332f9987e034272c_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of the machine learning workflow showing training and testing phases.
<!-- /IMAGE_DESCRIPTION -->
### Aprendizado Supervisionado

**Tarefa preditiva:** encontra uma função (modelo) a partir dos dados de treino que possa ser usada para prever um rótulo (classe) ou valor de um novo exemplo.

Pode ser:

**classificação** (rótulos discretos)

**regressão** (rótulos contínuos)

{7}------------------------------------------------
### Classificação

The diagram illustrates a supervised machine learning classification workflow. It begins with an input image of a cat, labeled 'Imagem sem rótulo' (Image without label) and 'Entrada' (Input). This image is processed by a 'Generalização' (Generalization) block, which contains an 'Algoritmo de Machine Learning Supervisionado' (Supervised Machine Learning Algorithm) and a 'Modelo' (Model) represented by a neural network icon. The final output is a prediction: 'gato (96%)' (cat (96%)), labeled 'Predição' (Prediction).

Diagram of a supervised machine learning classification process.

É o processo de automaticamente atribuir rótulos a dados.

Pode ser do tipo

- Binária: possui apenas duas classes

- Multiclasse: possui mais de duas classes

Pode atribuir

- Um único rótulo (single label)

- Vários rótulos (multi-label)

A photograph of a tomato sorting machine in operation. Red tomatoes are being processed by a blue mechanical arm. A red banner at the bottom of the image contains the text 'Máquina de triagem de tomate' (Tomato sorting machine).

Tomato sorting machine.

{8}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-2ee59e629035d641140e55f4d215b0d7_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a supervised machine learning classification process.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-89986656b45c3b6896256f1a22f7c186_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Tomato sorting machine.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-daa4a6fa7e2ba1954258f86b4928eb32_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of supervised machine learning generalization.
<!-- /IMAGE_DESCRIPTION -->
### Regressão

É o processo de automaticamente prever novos valores  $y$ .  
Neste caso, os dados são anotados com valores.

A line graph illustrating a regression model. The x-axis represents years from 2015 to 2022. The y-axis is unlabeled. Data points are plotted for years 2015 through 2021, connected by a solid blue line. For the year 2022, a dashed red line extends from the 2021 data point, ending with a red question mark, indicating a prediction.

| Year | Value (approx.) |
|------|-----------------|
| 2015 | 0.5             |
| 2016 | 0.2             |
| 2017 | 1.5             |
| 2018 | 1.8             |
| 2019 | 1.2             |
| 2020 | 2.5             |
| 2021 | 2.2             |
| 2022 | 3.0 (predicted) |

Line graph showing data points from 2015 to 2021 and a dashed red line for 2022 with a question mark.

A scatter plot showing training data points (blue dots) and a fitted regression curve (red line). The x-axis ranges from 0 to 100, and the y-axis ranges from -1 to 4. The data points show a non-linear, wavy pattern, and the red curve represents the model's fit to this data.

| x   | training data (approx.) | regression (approx.) |
|-----|-------------------------|----------------------|
| 0   | 0.5                     | 0.5                  |
| 20  | 1.0                     | 1.0                  |
| 40  | 0.0                     | 0.0                  |
| 60  | 1.5                     | 1.5                  |
| 80  | 3.5                     | 3.5                  |
| 100 | 3.0                     | 3.2                  |

Scatter plot with a fitted regression curve.

{9}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-91be14371a97fb5ce9eeb29ae18d07c3_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Line graph showing data points from 2015 to 2021 and a dashed red line for 2022 with a question mark.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-bedcca5cdf168e3508ef511d94ec514c_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Scatter plot with a fitted regression curve.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-f519a5be118c846f631c992412353fb9_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Scatter plot showing training data points (blue dots) and a fitted regression line (red line).
<!-- /IMAGE_DESCRIPTION -->
### Regressão

![Diagram of supervised machine learning training. A dataset of pairs [x, f(x)] is input into a supervised machine learning algorithm. The algorithm performs training (represented by a neural network icon) to create a model. The model then takes an input x and outputs f(x), with a red x^2 indicating the target function.](f4fdd410cdb84df81274da55721e56fb_img.jpg)

$[x, f(x)]$   
[1, 1]  
[2, 4]  
[3, 9]  
[4, 16]  
[5, 25]

$x$   $\xrightarrow{?}$   $f(x)$

Algoritmo de Machine Learning Supervisionado

Treinamento

Modelo

$x$   $\xrightarrow{x^2}$   $f(x)$

Diagram of supervised machine learning training. A dataset of pairs [x, f(x)] is input into a supervised machine learning algorithm. The algorithm performs training (represented by a neural network icon) to create a model. The model then takes an input x and outputs f(x), with a red x^2 indicating the target function.

Dataset Anotado

training data  
regression

Scatter plot showing training data points (blue dots) and a fitted regression line (red line). The x-axis ranges from 0 to 100, and the y-axis ranges from -1 to 4. The data points follow a parabolic trend, and the regression line fits the data well.

Entrada

Algoritmo de Machine Learning Supervisionado

Generalização

Modelo

$x$   $\xrightarrow{f(x)}$   $x^2$

Diagram of supervised machine learning generalization. An input of 6 is fed into the supervised machine learning algorithm. The algorithm performs generalization (represented by a neural network icon) to create a model. The model then takes an input x and outputs f(x), with a red x^2 indicating the target function.

{10}------------------------------------------------
#### Classificação & Regressão com Árvores de Decisão

```
graph TD; A[Restituição] -- S --> B[N]; A -- N --> C[Status Conjugal]; C -- "Solteiro, Divorc." --> D[Renda]; C -- Casado --> E[N]; D -- "<= 80K" --> F[N]; D -- "> 80K" --> G[S];
```

The diagram illustrates a decision tree structure. The root node is "Restituição" (yellow box). It branches into "S" (left) and "N" (right). The "S" branch leads to a leaf node "N" (blue box). The "N" branch leads to a node "Status Conjugal" (yellow box). From "Status Conjugal", the "Solteiro, Divorc." branch leads to a node "Renda" (yellow box), and the "Casado" branch leads to a leaf node "N" (blue box). The "Renda" node branches into "<= 80K" (left) and "> 80K" (right). The "<= 80K" branch leads to a leaf node "N" (blue box), and the "> 80K" branch leads to a leaf node "S" (blue box).

Decision tree diagram for classification and regression.

{11}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-5b4e774d63e0e0ed73801a9247755e5f_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree diagram for classification and regression.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-3442f31a562d1ef45bfa18b18a6a1ddc_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree for Status Conjugal
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-9cbc1ebd80813fc36e499f7d70ed6881_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree for Renda
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-fd76efce549d3713543bb5ed9b023c2e_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree for Restituição
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-7ed5d5770331f31ade15439a21c31425_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree diagram for classification.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-3337af75dfee8af7687b4f49914d6c93_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree diagram for classification.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-3b281ef3b6cc5f8ba97cbc011bfaac79_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree diagram for Status Conjugal.
<!-- /IMAGE_DESCRIPTION -->
### Classificação

A close-up photograph of many small wooden human figures, often called 'puzzle people'. They are scattered together, some standing upright and others lying down. The figures are made of wood and come in several colors: natural light wood, dark brown, light blue, and orange. The background is a dark, textured surface. The image is positioned on the right side of a dark blue gradient background that features a large, faint circular shape.

A close-up image of numerous wooden human figures in various colors (natural wood, dark brown, light blue, orange) scattered together, symbolizing diversity and classification.

{12}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-2dfa6ac3edfe874f68aa0cbccaa42322_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A composite image featuring a stylized brain circuit graphic on a dark blue background with glowing lines, and a close-up of colorful, blurred document folders at the bottom.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-ec0158057f8ccaf74edba16682ec5444_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A close-up image of numerous wooden human figures in various colors (natural wood, dark brown, light blue, orange) scattered together, symbolizing diversity and classification.
<!-- /IMAGE_DESCRIPTION -->
#### Árvores de Decisão

- Método para aproximar funções discretas ou contínuas, representadas por meio de um grafo acíclico direcionado, com vértice inicial único
- Tal grafo pode ser representado por um conjunto de regras “SE...ENTÃO” (Compreensibilidade)
- Amplamente utilizado em aplicações práticas, principalmente em problemas de classificação

```
graph TD; A[Restituição] -- S --> B[N]; A -- N --> C[Status Conjugal]; C -- "Solteiro, Divorc." --> D[Renda]; C -- Casado --> E[N]; D -- "<= 80K" --> F[N]; D -- "> 80K" --> G[S];
```

O diagrama ilustra uma árvore de decisão com os seguintes nós e ramificações:

- Nó raiz: **Restituição** (amarelo).
  - Ramificação **S** leva ao nó **N** (azul).
  - Ramificação **N** leva ao nó **Status Conjugal** (amarelo).
- Nó **Status Conjugal** (amarelo).
  - Ramificação **Solteiro, Divorc.** leva ao nó **Renda** (amarelo).
  - Ramificação **Casado** leva ao nó **N** (azul).
- Nó **Renda** (amarelo).
  - Ramificação **<= 80K** leva ao nó **N** (azul).
  - Ramificação **> 80K** leva ao nó **S** (azul).

Diagrama de uma Árvore de Decisão para classificação.

{13}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-eefe19c5e14dc4d6c316b7f7fbb7d7d7_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de uma Árvore de Decisão para classificação.
<!-- /IMAGE_DESCRIPTION -->
##### Exemplo de Árvore de Decisão

catagórico      Categórico      contínuo      classe

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

Atributos Explanatórios

```
graph TD; A[Restituição] -- S --> B[N]; A -- N --> C[Status Conjugal]; C -- "Solteiro, Divorc." --> D[Renda]; C -- Casado --> E[N]; D -- "<= 80K" --> F[N]; D -- "> 80K" --> G[S];
```

The diagram illustrates a decision tree for classifying 'Calote ?' (Class) based on 'Atributos Explanatórios' (Explanatory Attributes). The root node is 'Restituição' (Categorical). If 'Restituição' is 'S', the outcome is 'N'. If 'Restituição' is 'N', the next node is 'Status Conjugal' (Categorical). If 'Status Conjugal' is 'Casado', the outcome is 'N'. If 'Status Conjugal' is 'Solteiro, Divorc.', the next node is 'Renda' (Continuous). If 'Renda' is ' $\leq 80K$ ', the outcome is 'N'. If 'Renda' is ' $> 80K$ ', the outcome is 'S'.

Decision tree diagram showing the classification process for 'Calote ?' based on 'Restituição', 'Status Conjugal', and 'Renda'.

Modelo: Árvore de Decisão

{14}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-a33da0f14e456f92539ce3e9b7d81f9a_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree diagram showing the classification process for 'Calote ?' based on 'Restituição', 'Status Conjugal', and 'Renda'.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-187d05bf7ead21e1394b61320d8b3632_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree diagram showing the induction of the 3rd level.
<!-- /IMAGE_DESCRIPTION -->
##### Exemplo de Árvore de Decisão

*categorico*  
*Categorico*  
*contínuo*  
*classe*

| <i>Tid</i> | Restituição | Status Conjugal | Renda | Calote ? |
|------------|-------------|-----------------|-------|----------|
| 1          | S           | Solteiro        | 125K  | N        |
| 2          | N           | Casado          | 100K  | N        |
| 3          | N           | Solteiro        | 70K   | N        |
| 4          | S           | Casado          | 120K  | N        |
| 5          | N           | Divorc.         | 95K   | S        |
| 6          | N           | Casado          | 60K   | N        |
| 7          | S           | Divorc.         | 220K  | N        |
| 8          | N           | Solteiro        | 85K   | S        |
| 9          | N           | Casado          | 75K   | N        |
| 10         | N           | Solteiro        | 90K   | S        |

Conjunto de Treino

```
graph TD; A[Restituição] -- S --> B[N]; A -- N --> C[Status Conjugal]; C -- "Solteiro, Divorc." --> D[Renda]; C -- Casado --> E[N]; D -- "<= 80K" --> F[N]; D -- "> 80K" --> G[S];
```

The decision tree starts with the root node 'Restituição'. If the answer is 'S', it leads to a leaf node 'N'. If the answer is 'N', it leads to the 'Status Conjugal' node. From 'Status Conjugal', if the status is 'Solteiro, Divorc.', it leads to the 'Renda' node. If the status is 'Casado', it leads to a leaf node 'N'. From the 'Renda' node, if the income is less than or equal to 80K, it leads to a leaf node 'N'. If the income is greater than 80K, it leads to a leaf node 'S'.

Decision tree diagram for predicting 'Calote ?' based on 'Restituição', 'Status Conjugal', and 'Renda'.

Modelo: Árvore de Decisão

{15}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-7efae06af3af43ffe5d4b956a679cf54_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree diagram for predicting 'Calote ?' based on 'Restituição', 'Status Conjugal', and 'Renda'.
<!-- /IMAGE_DESCRIPTION -->
##### Outro exemplo de Árvore de Decisão

*categorico*  
*Categorico*  
*contínuo*  
*classe*

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

```
graph TD; A[Status Conjugal] -- Casado --> B[N]; A -- Solteiro, Divorc. --> C[Restituição]; C -- S --> D[N]; C -- N --> E[Renda]; E -- <= 80K --> F[N]; E -- > 80K --> G[S];
```

Decision tree diagram for the dataset. The root node is 'Status Conjugal'. It splits into 'Casado' (leading to leaf 'N') and 'Solteiro, Divorc.' (leading to 'Restituição'). 'Restituição' splits into 'S' (leading to leaf 'N') and 'N' (leading to 'Renda'). 'Renda' splits into '<= 80K' (leading to leaf 'N') and '> 80K' (leading to leaf 'S').

Pode existir mais de uma árvore de decisão adequada para os mesmos dados!

{16}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-0f985b39edc1d52ba3600c438bc8f0a5_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree diagram for the dataset. The root node is 'Status Conjugal'. It splits into 'Casado' (leading to leaf 'N') and 'Solteiro, Divorc.' (leading to 'Restituição'). 'Restituição' splits into 'S' (leading to...
<!-- /IMAGE_DESCRIPTION -->
##### Exemplo de Classificação

| Tid | Restituição | Status Conjugal | Renda | Calote ? |
|-----|-------------|-----------------|-------|----------|
|     |             |                 |       | classe   |
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

| Restituição | Status Conjugal | Renda | Calote ? |
|-------------|-----------------|-------|----------|
| N           | Solteiro        | 75K   | ?        |
| S           | Casado          | 50K   | ?        |
| N           | Casado          | 150K  | ?        |
| S           | Divorc.         | 90K   | ?        |
| N           | Solteiro        | 40K   | ?        |
| N           | Casado          | 80K   | ?        |

```
graph LR; A[Conjunto de Treino] --> B[Classificador]; B --> C[Modelo]; D[Conjunto de Teste] --> C;
```

The diagram illustrates the machine learning workflow. It starts with a training set (Conjunto de Treino) and a test set (Conjunto de Teste). The training set is used to train a classifier (Classificador), which produces a model (Modelo). The test set is then used to evaluate the model.

Diagram of the machine learning workflow showing training and testing phases.

{17}------------------------------------------------
##### Exemplo de Classificação

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

Treino

Indução

Algoritmo de  
Indução de  
Árvore de  
Decisão

Aprendizado

Modelo

Aplicação

Dedução

Teste

| Restitui<br>ção | Status<br>Conjugal | Renda | Calote<br>? |
|-----------------|--------------------|-------|-------------|
| N               | Solteiro           | 75K   | ?           |
| S               | Casado             | 50K   | ?           |
| N               | Casado             | 150K  | ?           |
| S               | Divorc.            | 90K   | ?           |
| N               | Solteiro           | 40K   | ?           |
| N               | Casado             | 80K   | ?           |

{18}------------------------------------------------
##### Exemplo de Classificação

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

Treino

Indução

Algoritmo de  
Indução de  
Árvore de  
Decisão

Aprendizado

Modelo

Aplicação

Dedução

Teste

| Restitui<br>ção | Status<br>Conjugal | Renda | Calote<br>? |
|-----------------|--------------------|-------|-------------|
| N               | Solteiro           | 75K   | ?           |
| S               | Casado             | 50K   | ?           |
| N               | Casado             | 150K  | ?           |
| S               | Divorc.            | 90K   | ?           |
| N               | Solteiro           | 40K   | ?           |
| N               | Casado             | 80K   | ?           |

{19}------------------------------------------------
### Aplicando o Modelo aos Dados de Teste

Dados de Teste

| Restituição | Status Conjugal | Renda | Calote ? |
|-------------|-----------------|-------|----------|
| N           | Casado          | 80K   | ?        |

Início na raiz da árvore.

```
graph TD; Root[Restituição] -- S --> LeafN1[N]; Root -- N --> StatusConjugal[Status Conjugal]; StatusConjugal -- "Solteiro, Divorc." --> Renda[Renda]; StatusConjugal -- Casado --> LeafN2[N]; Renda -- "<= 80K" --> LeafN3[N]; Renda -- "> 80K" --> LeafS[S];
```

Decision tree diagram for credit assessment. The root node is 'Restituição' (yellow). It has two branches: 'S' leading to a leaf 'N' (blue), and 'N' leading to the next internal node 'Status Conjugal' (yellow). 'Status Conjugal' has two branches: 'Solteiro, Divorc.' leading to the next internal node 'Renda' (yellow), and 'Casado' leading to a leaf 'N' (blue). 'Renda' has two branches: '<= 80K' leading to a leaf 'N' (blue), and '> 80K' leading to a leaf 'S' (blue).

<!-- DATALAB_CHUNK 2: pages 21-40 -->

{20}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-81a4cbf0b3c4cbc065efdf8f800dadde_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree diagram for credit assessment.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-ae53f90bb87d6d09e2d6b5278d7c338f_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree diagram for credit assessment.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-26d664119ad25250780f554633444e54_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree diagram for credit assessment.
<!-- /IMAGE_DESCRIPTION -->
## Aplicando o Modelo aos Dados de Teste

Dados de Teste

| Restituição | Status Conjugal | Renda | Calote ? |
|-------------|-----------------|-------|----------|
| N           | Casado          | 80K   | ?        |

```
graph TD; A[Restituição] -- S --> B[N]; A -- N --> C[Status Conjugal]; C -- "Solteiro, Divorc." --> D[Renda]; C -- Casado --> E[N]; D -- "<= 80K" --> F[N]; D -- "> 80K" --> G[S];
```

The diagram is a decision tree. The root node is 'Restituição' (yellow box). It has two branches: 'S' leading to a leaf node 'N' (blue box), and 'N' leading to the 'Status Conjugal' node (yellow box). The 'Status Conjugal' node has two branches: 'Solteiro, Divorc.' leading to the 'Renda' node (yellow box), and 'Casado' leading to a leaf node 'N' (blue box). The 'Renda' node has two branches: '<= 80K' leading to a leaf node 'N' (blue box), and '> 80K' leading to a leaf node 'S' (blue box). A red dashed arrow points from the 'Restituição' node to the 'Restituição' column of the test data table.

Decision tree diagram for credit assessment based on Restituição, Status Conjugal, and Renda.

{21}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-79e1709a7317ead45379cbb8ff3ba802_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree diagram for credit assessment based on Restituição, Status Conjugal, and Renda.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-eb03559a4d92ea9ebd63ea9be663c50a_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree diagram for credit assessment based on Restituição, Status Conjugal, and Renda.
<!-- /IMAGE_DESCRIPTION -->
## Aplicando o Modelo aos Dados de Teste

Dados de Teste

| Restituição | Status Conjugal | Renda | Calote ? |
|-------------|-----------------|-------|----------|
| N           | Casado          | 80K   | ?        |

```
graph TD; Restituição[Restituição] -- S --> N1[N]; Restituição -- N --> StatusConjugal[Status Conjugal]; StatusConjugal -- "Solteiro, Divorc." --> Renda[Renda]; StatusConjugal -- Casado --> N2[N]; Renda -- "<= 80K" --> N3[N]; Renda -- "> 80K" --> S[S];
```

The diagram illustrates a decision tree model. The root node is 'Restituição' (yellow box). It has two branches: 'S' leading to a leaf node 'N' (blue box), and 'N' leading to 'Status Conjugal' (yellow box). A red dashed arrow points from the 'N' branch of 'Restituição' to the 'Restituição' column of the test data table. The 'Status Conjugal' node has two branches: 'Solteiro, Divorc.' leading to 'Renda' (yellow box), and 'Casado' leading to a leaf node 'N' (blue box). The 'Renda' node has two branches: '<= 80K' leading to a leaf node 'N' (blue box), and '> 80K' leading to a leaf node 'S' (blue box).

Decision tree diagram showing the flow from Restituição to Status Conjugal and then to Renda, with leaf nodes indicating 'N' or 'S'.

{22}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-e180f2b5fcbe8001554a7c0677cd3f82_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree diagram showing the flow from Restituição to Status Conjugal and then to Renda, with leaf nodes indicating 'N' or 'S'.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-1316d63eca7b84e13c27f55f0027b7b5_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree diagram for Status Conjugal with two branches: Solteiro, Divorc.
<!-- /IMAGE_DESCRIPTION -->
## Aplicando o Modelo aos Dados de Teste

Dados de Teste

| Restitui<br>ção | Status<br>Conjugal | Renda | Calote<br>? |
|-----------------|--------------------|-------|-------------|
| N               | Casado             | 80K   | ?           |

```
graph TD; A[Restituição] -- S --> B[N]; A -- N --> C[Status Conjugal]; C -- "Solteiro, Divorc." --> D[Renda]; C -- Casado --> E[N]; D -- "<= 80K" --> F[N]; D -- "> 80K" --> G[S];
```

The diagram illustrates a decision tree model for credit assessment. The root node is 'Restituição' (Restitution). If the answer is 'S' (Yes), the path leads to a leaf node 'N' (No). If the answer is 'N' (No), the path leads to the 'Status Conjugal' (Marital Status) node. From 'Status Conjugal', if the status is 'Solteiro, Divorc.' (Single, Divorced), the path leads to the 'Renda' (Income) node. If the status is 'Casado' (Married), the path leads to a leaf node 'N'. From the 'Renda' node, if the income is '<= 80K', the path leads to a leaf node 'N'. If the income is '> 80K', the path leads to a leaf node 'S' (Yes).

Decision tree diagram for credit assessment based on Restituição, Status Conjugal, and Renda.

{23}------------------------------------------------
## Aplicando o Modelo aos Dados de Teste

Dados de Teste

| Restituição | Status Conjugal | Renda | Calote ? |
|-------------|-----------------|-------|----------|
| N           | Casado          | 80K   | ?        |

```
graph TD; A[Restituição] -- S --> B[N]; A -- N --> C[Status Conjugal]; C -- "Solteiro, Divorc." --> D[Renda]; C -- Casado --> E[N]; D -- "<= 80K" --> F[N]; D -- "> 80K" --> G[S];
```

Decision tree diagram illustrating the model's logic for credit assessment:

- Restituição** (Yellow box):
  - If **S** (black arrow), leads to **N** (blue box).
  - If **N** (red arrow), leads to **Status Conjugal** (Yellow box).
- Status Conjugal** (Yellow box):
  - If **Solteiro, Divorc.** (black arrow), leads to **Renda** (Yellow box).
  - If **Casado** (red arrow), leads to **N** (blue box).
- Renda** (Yellow box):
  - If **<= 80K** (black arrow), leads to **N** (blue box).
  - If **> 80K** (black arrow), leads to **S** (blue box).

Decision tree diagram for credit assessment.

{24}------------------------------------------------
## Aplicando o Modelo aos Dados de Teste

Dados de Teste

| Restituição | Status Conjugal | Renda | Calote ? |
|-------------|-----------------|-------|----------|
| N           | Casado          | 80K   | ?        |

```
graph TD; Restituição[Restituição] -- S --> N1[N]; Restituição -- N --> StatusConjugal[Status Conjugal]; StatusConjugal -- "Solteiro, Divorc." --> Renda[Renda]; StatusConjugal -- Casado --> N2[N]; Renda -- "<= 80K" --> N3[N]; Renda -- "> 80K" --> S[S];
```

Decision tree diagram for credit assessment. The root node is 'Restituição' (yellow). It has two branches: 'S' (black arrow) leading to a leaf node 'N' (blue), and 'N' (red arrow) leading to a node 'Status Conjugal' (yellow). 'Status Conjugal' has two branches: 'Solteiro, Divorc.' (black arrow) leading to a node 'Renda' (yellow), and 'Casado' (red arrow) leading to a leaf node 'N' (blue). 'Renda' has two branches: '<= 80K' (black arrow) leading to a leaf node 'N' (blue), and '> 80K' (black arrow) leading to a leaf node 'S' (blue).

Atribuir "N" para Calote

{25}------------------------------------------------
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

graph TD
    N1[N] --> S1[S]
    N1 --> N1a[N]
    
    Restituição1[Restituição] -- S --> N2[N]
    Restituição1 -- N --> S2[S]
    
    Restituição2[Restituição] -- S --> N3[N]
    Restituição2 -- N --> StatusConjugal1[Status Conjugal]
    StatusConjugal1 -- "Solteiro, Divorc." --> S3[S]
    StatusConjugal1 -- Casado --> N4[N]
    
    Restituição3[Restituição] -- S --> N5[N]
    Restituição3 -- N --> StatusConjugal2[Status Conjugal]
    StatusConjugal2 -- "Solteiro, Divorc." --> Renda[Renda]
    StatusConjugal2 -- Casado --> N6[N]
    Renda -- "<= 80K" --> N7[N]
    Renda -- "> 80K" --> S4[S]
  
```

Diagram illustrating the Hunt algorithm for classification. It shows three stages of a decision tree: 1. A single node 'N' branching into 'S' and 'N'. 2. A node 'Restituição' branching into 'N' (S) and 'Status Conjugal' (N). 3. A node 'Restituição' branching into 'N' (S) and 'Status Conjugal' (N), which further branches into 'Solteiro, Divorc.' (S) and 'Casado' (N). 4. A node 'Restituição' branching into 'N' (S) and 'Status Conjugal' (N), which further branches into 'Renda' (Solteiro, Divorc.) and 'N' (Casado). 5. A node 'Renda' branching into 'N' (<= 80K) and 'S' (> 80K).

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
> **[Descrição de imagem]** Diagram illustrating the Hunt algorithm for classification.
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

Diagrama de divisão múltipla para o atributo "Tipo de Carro". O atributo é representado por um retângulo amarelo no topo. Três setas descendentes o dividem em três categorias: "Família" à esquerda, "Esportivo" no centro e "Luxo" à direita.

Diagrama de divisão múltipla para o atributo 'Tipo de Carro'.

- **Binária:** agregar categorias em dois sub-conjuntos. Necessário encontrar a divisão ótima.

Diagrama de divisão binária para o atributo "Tipo de Carro". O atributo é representado por um retângulo amarelo no topo. Duas setas descendentes o dividem em dois sub-conjuntos: "{Família, Esportivo}" à esquerda e "{Luxo}" à direita.

Diagrama de divisão binária para o atributo 'Tipo de Carro'.

OU

Diagrama de divisão binária alternativa para o atributo "Tipo de Carro". O atributo é representado por um retângulo amarelo no topo. Duas setas descendentes o dividem em dois sub-conjuntos: "{Família, Luxo}" à esquerda e "{Esportivo}" à direita.

Diagrama de divisão binária alternativa para o atributo 'Tipo de Carro'.

OU ...

{31}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-dcf37c460c66ec011dbe6ca08de44ff9_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de divisão múltipla para o atributo 'Tipo de Carro'.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-4f148853ae68fdcf5e43f7604cab457d_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de divisão binária para o atributo 'Tipo de Carro'.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-98e54d5540b2efe3e24af3cf936bc4ea_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de divisão binária alternativa para o atributo 'Tipo de Carro'.
<!-- /IMAGE_DESCRIPTION -->
#### Divisão para atributos categóricos ordinais

- Múltipla: dividir com base no número de categorias

```
graph TD; Tamanho[Tamanho] --> Pequeno[Pequeno]; Tamanho --> Medio[Médio]; Tamanho --> Grande[Grande];
```

Diagram showing a single split for the 'Tamanho' attribute into three categories: Pequeno, Médio, and Grande.

- Binária: agregar categorias em dois sub-conjuntos. Necessário encontrar a divisão ótima.

```
graph TD; Tamanho[Tamanho] --> L["{Pequeno, Médio}"]; Tamanho --> R["{Grande}"];
```

Diagram showing a binary split for 'Tamanho' into {Pequeno, Médio} and {Grande}.

OU

```
graph TD; Tamanho[Tamanho] --> L["{Pequeno}"]; Tamanho --> R["{Médio, Grande}"];
```

Diagram showing a binary split for 'Tamanho' into {Pequeno} and {Médio, Grande}.

- E esta divisão?

```
graph TD; Tamanho[Tamanho] --> L["{Pequeno, Grande}"]; Tamanho --> R["{Médio}"];
```

Diagram showing a binary split for 'Tamanho' into {Pequeno, Grande} and {Médio}.

{32}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-14252bcd35912bd656e98b16b2ee51c0_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram showing a single split for the 'Tamanho' attribute into three categories: Pequeno, Médio, and Grande.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-9f9386d5b3d6cbeb1ed104a799320ebf_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram showing a binary split for 'Tamanho' into {Pequeno, Médio} and {Grande}.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-a05e675f8651ae7ccea1d0d68691d1a9_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram showing a binary split for 'Tamanho' into {Pequeno} and {Médio, Grande}.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-f0b7abcb093621bb310bf61fbe0f0d2d_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram showing a binary split for 'Tamanho' into {Pequeno, Grande} and {Médio}.
<!-- /IMAGE_DESCRIPTION -->
#### Divisão para atributos contínuos

- **Múltipla:** discretizar os valores em intervalos

A diagram illustrating multiple discretization of a continuous attribute. At the top, a yellow rectangular box labeled "Renda" has five arrows pointing downwards to five different labels. From left to right, these labels are: " $\leq 10K$ ", "[10k,30k)", "[30k,50k)", "[50k,80k]", and " $> 80K$ ".

Diagram illustrating multiple discretization of income (Renda) into five intervals.

- **Binária:** definir ponto de divisão

A diagram illustrating binary discretization of a continuous attribute. At the top, a yellow rectangular box labeled "Renda" has two arrows pointing downwards to two labels. The left arrow points to " $\leq 80K$ " and the right arrow points to " $> 80K$ ".

Diagram illustrating binary discretization of income (Renda) at a threshold of 80K.

{33}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-318886a86a1dcc59e1fc83db6f157c60_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram illustrating multiple discretization of income (Renda) into five intervals.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-3e2a8dc8c5537dbe703cdcb0e21e4e1b_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram illustrating binary discretization of income (Renda) at a threshold of 80K.
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

The diagram illustrates three potential splits for a decision tree based on the attribute 'Carro próprio?':

- Carro próprio?** (Yellow box)
  - S**: Leaf node with  $C0:6$  and  $C1:4$ .
  - N**: Leaf node with  $C0:4$  and  $C1:6$ .
- Tipo de Carro** (Yellow box)
  - Família**: Leaf node with  $C0:1$  and  $C1:3$ .
  - Esportivo**: Leaf node with  $C0:8$  and  $C1:0$ .
  - Luxo**: Leaf node with  $C0:1$  and  $C1:7$ .
- Matricula Estudante** (Yellow box)
  - 21101234: Leaf node with  $C0:1$  and  $C1:0$ .
  - ... (Ellipsis)
  - 21102345: Leaf node with  $C0:1$  and  $C1:0$ .
  - 21101234: Leaf node with  $C0:0$  and  $C1:1$ .
  - ... (Ellipsis)
  - 22203456: Leaf node with  $C0:0$  and  $C1:1$ .

Three decision tree splits illustrating attribute selection: 'Carro próprio?', 'Tipo de Carro', and 'Matricula Estudante'.

Qual atributo é melhor para dividir os dados?

{35}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-dcc2d5a5b39f780e7a224bb01ba1ef6e_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Three decision tree splits illustrating attribute selection: 'Carro próprio?', 'Tipo de Carro', and 'Matricula Estudante'.
<!-- /IMAGE_DESCRIPTION -->
#### Como escolher o atributo?

- Estratégia gulosa
  - Dar preferência a nós com distribuição de classe **homogênea**
  - Para tanto, precisamos de uma medida para quantificar **impureza**!

The diagram illustrates two different splits of a dataset into two classes (red and blue) to demonstrate the greedy strategy for attribute selection. Each split is shown as a tree structure starting from a root node and branching into two child nodes.

**Left Split:** The root node contains 10 points (5 red, 5 blue). The left child node contains 4 points (3 red, 1 blue), and the right child node contains 6 points (2 red, 4 blue). This split results in two child nodes that are not homogeneous.

**Right Split:** The root node contains 10 points (5 red, 5 blue). The left child node contains 5 points (4 red, 1 blue), and the right child node contains 5 points (1 red, 4 blue). This split also results in two child nodes that are not homogeneous.

Diagram illustrating two different splits of a dataset into two classes (red and blue) to demonstrate the greedy strategy for attribute selection.

{36}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-1142ba0197b158bb198186fe8baccc32_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram illustrating two different splits of a dataset into two classes (red and blue) to demonstrate the greedy strategy for attribute selection.
<!-- /IMAGE_DESCRIPTION -->
#### Qual o melhor atributo?

*categorico*  
*Categorico*  
*contínuo*  
*classe*

| <i>Tid</i> | Restituição | Status Conjugal | Renda | Calote ? |
|------------|-------------|-----------------|-------|----------|
| 1          | S           | Solteiro        | 125K  | N        |
| 2          | N           | Casado          | 100K  | N        |
| 3          | N           | Solteiro        | 70K   | N        |
| 4          | S           | Casado          | 120K  | N        |
| 5          | N           | Divorc.         | 95K   | S        |
| 6          | N           | Casado          | 60K   | N        |
| 7          | S           | Divorc.         | 220K  | N        |
| 8          | N           | Solteiro        | 85K   | S        |
| 9          | N           | Casado          | 75K   | N        |
| 10         | N           | Solteiro        | 90K   | S        |

```
graph TD; A[Restituição] -- S --> B[N]; A -- N --> C[S]; B --- D["Acertos = 3<br/>Erros = 0"]; C --- E["Acertos = 3<br/>Erros = 4"];
```

60%

Decision tree diagram for the 'Restituição' attribute. The root node is 'Restituição' (yellow). It splits into two branches: 'S' (left) and 'N' (right). The 'S' branch leads to a leaf node 'N' (blue) with 'Acertos = 3' and 'Erros = 0'. The 'N' branch leads to a leaf node 'S' (blue) with 'Acertos = 3' and 'Erros = 4'. The overall accuracy is 60%.

Conjunto de Treino

{37}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-145d00f59802048185303f15937ea65c_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree diagram for the 'Restituição' attribute.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-4e85fe330de2c4f5eea6de4b2a53c77f_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree diagram for the 'Restituição' attribute.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-0931f3e098bd4539041de11c50cec2d2_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree diagram for the 'Restituição' attribute.
<!-- /IMAGE_DESCRIPTION -->
#### Qual o melhor atributo?

*categorico*  
*Categorico*  
*contínuo*  
*classe*

| <i>Tid</i> | Restituição | Status Conjugal | Rendim. Tributáveis | Calote ? |
|------------|-------------|-----------------|---------------------|----------|
| 1          | S           | Solteiro        | 125K                | N        |
| 2          | N           | Casado          | 100K                | N        |
| 3          | N           | Solteiro        | 70K                 | N        |
| 4          | S           | Casado          | 120K                | N        |
| 5          | N           | Divorc.         | 95K                 | S        |
| 6          | N           | Casado          | 60K                 | N        |
| 7          | S           | Divorc.         | 220K                | N        |
| 8          | N           | Solteiro        | 85K                 | S        |
| 9          | N           | Casado          | 75K                 | N        |
| 10         | N           | Solteiro        | 90K                 | S        |

Conjunto de Treino

Diagrama de árvore de decisão baseado no atributo Status Conjugal:

```
graph TD; A[Status Conjugal] -- Solteiro --> B[S]; A -- Casado --> C[N]; A -- Divorc. --> D[S];
```

Resultados para o nó Solteiro (S): Acertos = 2, Erros = 2

Resultados para o nó Casado (N): Acertos = 4, Erros = 0

Resultados para o nó Divorc. (S): Acertos = 1, Erros = 1

70%

Diagrama de árvore de decisão baseado no atributo Status Conjugal (alternativa):

```
graph TD; A[Status Conjugal] -- Solteiro, Divorc. --> B[S]; A -- Casado --> C[N];
```

Resultados para o nó Solteiro, Divorc. (S): Acertos = 3, Erros = 3

Resultados para o nó Casado (N): Acertos = 4, Erros = 0

70%

{38}------------------------------------------------
#### Qual o melhor atributo?

*categorico*  
*Categorico*  
*contínuo*  
*classe*

| <i>Tid</i> | Restituição | Status Conjugal | Rendim. Tributáveis | Calote ? |
|------------|-------------|-----------------|---------------------|----------|
| 1          | S           | Solteiro        | 125K                | N        |
| 2          | N           | Casado          | 100K                | N        |
| 3          | N           | Solteiro        | 70K                 | N        |
| 4          | S           | Casado          | 120K                | N        |
| 5          | N           | Divorc.         | 95K                 | S        |
| 6          | N           | Casado          | 60K                 | N        |
| 7          | S           | Divorc.         | 220K                | N        |
| 8          | N           | Solteiro        | 85K                 | S        |
| 9          | N           | Casado          | 75K                 | N        |
| 10         | N           | Solteiro        | 90K                 | S        |

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

Renda

$\leq$ 80K → N  
Acertos = 3  
Erros = 0

> 80K → S  
Acertos = 3  
Erros = 4

60%

Renda

$\leq$ 97K → S  
Acertos = 3  
Erros = 3

> 97K → N  
Acertos = 4  
Erros = 0

70%

Conjunto de Treino

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

- Índice Gini para um nó  $t$ :

$$GINI(t) = 1 - \sum_j [p(j|t)]^2$$

$p(j|t)$  é a frequência relativa da classe  $j$  no nó  $t$

- Valor máximo:  $1 - \frac{1}{c}$  (quando classes forem equiprováveis)
- Valor mínimo:  $0$  (quando todas instâncias pertencem à mesma classe)

|                   |          |
|-------------------|----------|
| C1                | <b>0</b> |
| C2                | <b>6</b> |
| <b>Gini=0.000</b> |          |

|                   |          |
|-------------------|----------|
| C1                | <b>1</b> |
| C2                | <b>5</b> |
| <b>Gini=0.278</b> |          |

|                   |          |
|-------------------|----------|
| C1                | <b>2</b> |
| C2                | <b>4</b> |
| <b>Gini=0.444</b> |          |

|                   |          |
|-------------------|----------|
| C1                | <b>3</b> |
| C2                | <b>3</b> |
| <b>Gini=0.500</b> |          |

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

Decision tree diagram for attribute B. The root node is an oval labeled 'B?'. It branches into 'Sim' (Yes) leading to 'Nó N1' and 'Não' (No) leading to 'Nó N2'.

|              | Pai |
|--------------|-----|
| C1           | 6   |
| C2           | 6   |
| Gini = 0.500 |     |

$$Gini(N1) = 1 - [(5/7)^2 + (2/7)^2] = 0.4082$$

|    | N1 | N2 |
|----|----|----|
| C1 | 5  | 1  |
| C2 | 2  | 4  |

$$Gini(N2) = 1 - [(1/5)^2 + (4/5)^2] = 0.32$$

$$GINI_{split} = \sum_{i=1}^k \frac{n_i}{n} GINI(i)$$

$$Gini(divisão) = [(7/12) * 0.4082] + [(5/12) * 0.32] = 0.37145$$

{44}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-f5a5f52bc25d95a7f616290c99e88ae6_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree diagram for attribute B. The root node is an oval labeled 'B?'. It branches into 'Sim' (Yes) leading to 'Nó N1' and 'Não' (No) leading to 'Nó N2'.
<!-- /IMAGE_DESCRIPTION -->
### Árvore elementar: Calculando o Índice GINI

| Tid | Restituição | Status Conjugual | Renda | Calote ? |
|-----|-------------|------------------|-------|----------|
|     |             |                  |       |          |
| 1   | S           | Solteiro         | 125K  | N        |
| 2   | N           | Casado           | 100K  | N        |
| 3   | N           | Solteiro         | 70K   | N        |
| 4   | S           | Casado           | 120K  | N        |
| 5   | N           | Divorc.          | 95K   | S        |
| 6   | N           | Casado           | 60K   | N        |
| 7   | S           | Divorc.          | 220K  | N        |
| 8   | N           | Solteiro         | 85K   | S        |
| 9   | N           | Casado           | 75K   | N        |
| 10  | N           | Solteiro         | 90K   | S        |

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

categórico  
Categórico  
contínuo  
classe

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

graph TD
    A[Restituição] -- S --> B[N]
    A -- N --> C[S]
    
```

Decision tree diagram for the 'Restituição' attribute. The root node is 'Restituição' (yellow). It splits into two branches: 'S' (left) and 'N' (right). The 'S' branch leads to a leaf node 'N' (blue), and the 'N' branch leads to a leaf node 'S' (blue).

Acertos = 3  
Erros = 0

Acertos = 3  
Erros = 4

$$\text{Gini} = 1 - (3/3)^2 - (0/3)^2$$

60%

$$\text{Gini} = 1 - (3/7)^2 - (4/7)^2$$

$$\text{Gini} = 1 - 1 - 0$$

$$\text{Gini} = 1 - 9/49 - 16/49$$

$$\text{Gini} = 0,0$$

$$\text{Gini} = (49 - 9 - 16)/49$$

$$\text{Gini} = 0,49$$

$$\text{Gini}_{\text{split}} = (3/10) * 0,0 + (7/10) * 0,49$$

$$\text{Gini}_{\text{split}} = 0 + 0,34$$

$$\text{Gini}_{\text{split}} = 0,34$$

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

|      | TipoVeículo           |            |      | TipoVeículo |                     |
|------|-----------------------|------------|------|-------------|---------------------|
|      | {Esportivo<br>, Luxo} | {Familiar} |      | {Esportivo} | {Familiar<br>,Luxo} |
| C1   | 3                     | 1          | C1   | 2           | 2                   |
| C2   | 2                     | 4          | C2   | 1           | 5                   |
| Gini | 0.400                 |            | Gini | 0.419       |                     |

{47}------------------------------------------------
#### Atributos Categóricos: Calculando o Índice GINI

*categórico*  
*Categórico*  
*contínuo*  
*classe*

| <i>Tid</i> | Restituição | Status Conjugal | Renda | Calote ? |
|------------|-------------|-----------------|-------|----------|
| 1          | S           | Solteiro        | 125K  | N        |
| 2          | N           | Casado          | 100K  | N        |
| 3          | N           | Solteiro        | 70K   | N        |
| 4          | S           | Casado          | 120K  | N        |
| 5          | N           | Divorc.         | 95K   | S        |
| 6          | N           | Casado          | 60K   | N        |
| 7          | S           | Divorc.         | 220K  | N        |
| 8          | N           | Solteiro        | 85K   | S        |
| 9          | N           | Casado          | 75K   | N        |
| 10         | N           | Solteiro        | 90K   | S        |

Conjunto de Treino

$Gini_{split} = 0,3$

$Gini_{split} = 0,3$

```

graph TD
    A[Status Conjugal] -- Solteiro --> B[S]
    A -- Casado --> C[N]
    A -- Divorc. --> D[S]
    
```

Solteiro: Acertos = 2, Erros = 2  
 Casado: Acertos = 4, Erros = 0  
 Divorc.: Acertos = 1, Erros = 1

Decision tree diagram for Status Conjugal with three branches: Solteiro, Casado, and Divorc. Each branch leads to a leaf node with classification results.

70%

```

graph TD
    A[Status Conjugal] -- Solteiro, Divorc. --> B[S]
    A -- Casado --> C[N]
    
```

Solteiro, Divorc.: Acertos = 3, Erros = 3  
 Casado: Acertos = 4, Erros = 0

Decision tree diagram for Status Conjugal with two branches: Solteiro, Divorc. and Casado. Each branch leads to a leaf node with classification results.

70%

{48}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-73b28b0f5e3be628bb5a3d6bd1d79d21_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree diagram for Status Conjugal with three branches: Solteiro, Casado, and Divorc.
<!-- /IMAGE_DESCRIPTION -->
#### Atributos Contínuos: Calculando o Índice GINI

- Para a eficiência computacional: para cada atributo,
  - Classificar valores existentes
  - Pesquisar linearmente estes valores, apurando a população envolvida, e calculando o índice GINI
  - Escolher a posição de particionamento que apresenta o menor índice GINI

| Calote            |  | N     |   | N     |   | N     |   | S     |   | S     |   | S     |   | N            |   | N     |   | N     |   | N     |   |       |   |
|-------------------|--|-------|---|-------|---|-------|---|-------|---|-------|---|-------|---|--------------|---|-------|---|-------|---|-------|---|-------|---|
|                   |  | Renda |   |       |   |       |   |       |   |       |   |       |   |              |   |       |   |       |   |       |   |       |   |
| Valores Ordenados |  | 60    |   | 70    |   | 75    |   | 85    |   | 90    |   | 95    |   | 100          |   | 120   |   | 125   |   | 220   |   |       |   |
| Posições de       |  | 55    |   | 65    |   | 72    |   | 80    |   | 87    |   | 92    |   | 97           |   | 110   |   | 122   |   | 172   |   | 230   |   |
| Particionamento   |  | <=    | > | <=    | > | <=    | > | <=    | > | <=    | > | <=    | > | <=           | > | <=    | > | <=    | > | <=    | > | <=    | > |
| S                 |  | 0     | 3 | 0     | 3 | 0     | 3 | 0     | 3 | 1     | 2 | 2     | 1 | 3            | 0 | 3     | 0 | 3     | 0 | 3     | 0 | 3     | 0 |
| N                 |  | 0     | 7 | 1     | 6 | 2     | 5 | 3     | 4 | 3     | 4 | 3     | 4 | 3            | 4 | 4     | 3 | 5     | 2 | 6     | 1 | 7     | 0 |
| Gini              |  | 0.420 |   | 0.400 |   | 0.375 |   | 0.343 |   | 0.417 |   | 0.400 |   | <u>0.300</u> |   | 0.343 |   | 0.375 |   | 0.400 |   | 0.420 |   |

{49}------------------------------------------------
### Induzindo o 2o. Nível da árvore de decisão

*categorico*  
*Categorico*  
*contínuo*  
*classe*

| <i>Tid</i> | Restitui<br>ção | Status<br>Conjugal | Renda | Calote<br>? |
|------------|-----------------|--------------------|-------|-------------|
| 1          | S               | Solteiro           | 125K  | N           |
| 2          | N               | Casado             | 100K  | N           |
| 3          | N               | Solteiro           | 70K   | N           |
| 4          | S               | Casado             | 120K  | N           |
| 5          | N               | Divorc.            | 95K   | S           |
| 6          | N               | Casado             | 80K   | N           |
| 7          | S               | Divorc.            | 220K  | N           |
| 8          | N               | Solteiro           | 85K   | S           |
| 9          | N               | Casado             | 75K   | N           |
| 10         | N               | Solteiro           | 90K   | S           |

Conjunto de Treino

```

graph TD
    A[Status Conjugal] -->|Solteiro, Divorc.| B[S]
    A -->|Casado| C[N]
    B --- D["Acertos = 3  
Erros = 3"]
    C --- E["Acertos = 4  
Erros = 0"]
    
```

Acertos = 3  
Erros = 3

Acertos = 4  
Erros = 0

Decision tree for Status Conjugal

Aqui parou.

```

graph TD
    A[Renda] -->|<= 97K| B[S]
    A -->|> 97K| C[N]
    B --- D["Acertos = 3  
Erros = 1"]
    C --- E["Acertos = 2  
Erros = 0"]
    
```

Acertos = 3  
Erros = 1

Acertos = 2  
Erros = 0

Decision tree for Renda

Ginisplit = 0,25

```

graph TD
    A[Restituição] -->|S| B[N]
    A -->|N| C[S]
    B --- D["Acertos = 2  
Erros = 0"]
    C --- E["Acertos = 3  
Erros = 1"]
    
```

Acertos = 2  
Erros = 0

Acertos = 3  
Erros = 1

Decision tree for Restituição

Ginisplit = 0,25

{50}------------------------------------------------
### Induzindo o 3o. Nível da árvore de decisão

categórico  
Categórico  
contínuo  
classe

| Tid | Restitui<br>ção | Status<br>Conjugal | Rendim.<br>Tributáv<br>eis | Calote<br>? |
|-----|-----------------|--------------------|----------------------------|-------------|
| 1   | S               | Solteiro           | 125K                       | N           |
| 2   | N               | Casado             | 100K                       | N           |
| 3   | N               | Solteiro           | 70K                        | N           |
| 4   | S               | Casado             | 120K                       | N           |
| 5   | N               | Divorc.            | 95K                        | S           |
| 6   | N               | Casado             | 60K                        | N           |
| 7   | S               | Divorc.            | 220K                       | N           |
| 8   | N               | Solteiro           | 85K                        | S           |
| 9   | N               | Casado             | 75K                        | N           |
| 10  | N               | Solteiro           | 90K                        | S           |

Conjunto de Treino

```

graph TD
    A[Status Conjugal] --> B[Solteiro, Divorc.]
    A --> C[Casado]
    C --> D[N]
    D --- E[Acertos = 4<br/>Erros = 0]
    B --> F[Restituição]
    F --> G[N]
    F --> H[S]
    H --> I[N]
    I --- J[Acertos = 2<br/>Erros = 0]
    G --> K[Renda]
    K --> L["<= 80K"]
    K --> M["> 80K"]
    L --> N[N]
    N --- O[Acertos = 1<br/>Erros = 0]
    M --> P[S]
    P --- Q[Acertos = 3<br/>Erros = 0]
    
```

Decision tree diagram showing the induction of the 3rd level. The root node is 'Status Conjugal' (yellow), which splits into 'Solteiro, Divorc.' and 'Casado'. The 'Casado' branch leads to a leaf node 'N' (blue) with 'Acertos = 4' and 'Erros = 0'. The 'Solteiro, Divorc.' branch leads to a node 'Restituição' (yellow), which splits into 'N' and 'S'. The 'S' branch leads to a leaf node 'N' (blue) with 'Acertos = 2' and 'Erros = 0'. The 'N' branch leads to a node 'Renda' (yellow), which splits into '<= 80K' and '> 80K'. The '<= 80K' branch leads to a leaf node 'N' (blue) with 'Acertos = 1' and 'Erros = 0'. The '> 80K' branch leads to a leaf node 'S' (blue) with 'Acertos = 3' and 'Erros = 0'.

Ginisplit = 0,0

{51}------------------------------------------------
## Comparação entre os critérios de divisão

Para um problema de 2 classes:

O gráfico mostra a comparação entre três critérios de divisão para um problema de 2 classes, em função da proporção  $p$  da classe positiva (onde  $p$  varia de 0 a 1). O eixo vertical representa o valor do critério, variando de 0 a 1.

- Entropy (vermelha):** Representa a entropia, que é simétrica em relação a  $p=0.5$  e atinge seu valor máximo de 1 quando  $p=0.5$ .
- Gini (azul):** Representa o índice de Gini, também simétrico em relação a  $p=0.5$ , com um valor máximo de 0.5 quando  $p=0.5$ .
- Misclassification error (preta):** Representa o erro de classificação, que é linear e atinge seu valor máximo de 0.5 quando  $p=0.5$ .

Embora todos os critérios sejam maximizados em  $p=0.5$ , a Entropy é o critério mais conservador, seguido pelo Gini, e o Misclassification error é o menos conservador.

| $p$ | Entropy | Gini  | Misclassification error |
|-----|---------|-------|-------------------------|
| 0.0 | 0.000   | 0.000 | 0.000                   |
| 0.1 | 0.471   | 0.180 | 0.100                   |
| 0.2 | 0.721   | 0.320 | 0.200                   |
| 0.3 | 0.918   | 0.420 | 0.300                   |
| 0.4 | 0.993   | 0.480 | 0.400                   |
| 0.5 | 1.000   | 0.500 | 0.500                   |
| 0.6 | 0.993   | 0.480 | 0.400                   |
| 0.7 | 0.918   | 0.420 | 0.300                   |
| 0.8 | 0.721   | 0.320 | 0.200                   |
| 0.9 | 0.471   | 0.180 | 0.100                   |
| 1.0 | 0.000   | 0.000 | 0.000                   |

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
  - Atingir profundidade máxima (parâmetro)
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
  - Sujeitas a **overfitting** (super-ajuste aos dados)
  - Geram apenas hiperplanos paralelos aos eixos
    - Logo, não lidam bem com atributos correlacionados (por quê?)
  - Solução localmente ótima pode estar longe do ótimo global

{55}------------------------------------------------
## Visualização Geométrica de uma Árvore de Decisão

Objeto a ser classificado

A scatter plot illustrating the geometric visualization of a decision tree. The plot shows two classes of data points in a 2D space defined by Atributo 1 (horizontal axis) and Atributo 2 (vertical axis). The blue circles represent one class, and the red squares represent the other. A purple diamond, labeled 'Objeto a ser classificado', is positioned at approximately (4.5, 5.5) and is being pointed to by an arrow from the text 'Objeto a ser classificado'.

| Atributo 1 | Atributo 2 | Class          |
|------------|------------|----------------|
| 1.0        | 1.0        | Blue Circle    |
| 1.0        | 1.5        | Blue Circle    |
| 1.0        | 2.8        | Blue Circle    |
| 1.0        | 4.0        | Blue Circle    |
| 1.0        | 5.0        | Blue Circle    |
| 1.0        | 6.0        | Blue Circle    |
| 1.5        | 1.8        | Blue Circle    |
| 1.5        | 2.5        | Blue Circle    |
| 1.5        | 3.5        | Blue Circle    |
| 1.5        | 4.0        | Blue Circle    |
| 1.5        | 4.5        | Blue Circle    |
| 1.5        | 5.2        | Blue Circle    |
| 2.0        | 4.5        | Blue Circle    |
| 2.0        | 5.2        | Blue Circle    |
| 2.5        | 1.5        | Blue Circle    |
| 2.5        | 4.0        | Blue Circle    |
| 2.5        | 5.2        | Blue Circle    |
| 2.5        | 5.8        | Blue Circle    |
| 3.0        | 2.2        | Blue Circle    |
| 3.0        | 3.2        | Blue Circle    |
| 3.0        | 3.8        | Blue Circle    |
| 3.0        | 5.2        | Blue Circle    |
| 3.5        | 1.3        | Blue Circle    |
| 3.5        | 5.4        | Blue Circle    |
| 4.0        | 2.4        | Blue Circle    |
| 4.0        | 4.4        | Blue Circle    |
| 4.0        | 5.4        | Blue Circle    |
| 4.5        | 3.2        | Blue Circle    |
| 4.5        | 3.8        | Blue Circle    |
| 4.5        | 5.5        | Purple Diamond |
| 5.0        | 1.6        | Blue Circle    |
| 5.5        | 1.9        | Blue Circle    |
| 5.5        | 3.2        | Blue Circle    |
| 6.0        | 1.7        | Blue Circle    |
| 6.5        | 6.5        | Red Square     |
| 6.5        | 7.2        | Red Square     |
| 6.5        | 8.0        | Red Square     |
| 6.5        | 8.8        | Red Square     |
| 7.0        | 6.8        | Red Square     |
| 7.0        | 7.5        | Red Square     |
| 7.0        | 8.2        | Red Square     |
| 7.0        | 8.8        | Red Square     |
| 7.0        | 9.8        | Red Square     |
| 7.5        | 6.8        | Red Square     |
| 7.5        | 7.5        | Red Square     |
| 7.5        | 8.2        | Red Square     |
| 7.5        | 8.8        | Red Square     |
| 7.5        | 9.2        | Red Square     |
| 8.0        | 5.0        | Red Square     |
| 8.0        | 5.5        | Red Square     |
| 8.0        | 6.2        | Red Square     |
| 8.0        | 6.8        | Red Square     |
| 8.0        | 7.5        | Red Square     |
| 8.0        | 8.2        | Red Square     |
| 8.0        | 8.8        | Red Square     |
| 8.0        | 9.5        | Red Square     |
| 8.5        | 5.2        | Red Square     |
| 8.5        | 5.8        | Red Square     |
| 8.5        | 6.5        | Red Square     |
| 8.5        | 7.2        | Red Square     |
| 8.5        | 7.8        | Red Square     |
| 8.5        | 8.5        | Red Square     |
| 8.5        | 9.2        | Red Square     |
| 9.0        | 5.5        | Red Square     |
| 9.0        | 6.2        | Red Square     |
| 9.0        | 6.8        | Red Square     |
| 9.0        | 7.5        | Red Square     |
| 9.0        | 8.2        | Red Square     |
| 9.0        | 8.8        | Red Square     |
| 9.5        | 4.8        | Red Square     |
| 9.5        | 5.8        | Red Square     |
| 9.5        | 6.5        | Red Square     |
| 9.5        | 7.2        | Red Square     |
| 9.5        | 7.8        | Red Square     |
| 9.5        | 8.2        | Red Square     |
| 9.5        | 8.8        | Red Square     |
| 9.5        | 9.8        | Red Square     |

Scatter plot showing two classes of data points (blue circles and red squares) in a 2D space defined by Atributo 1 and Atributo 2. A purple diamond represents an object to be classified, located at approximately (4.5, 5.5).

{56}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-6fd373b1aea8f583da362efa5e3710df_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Scatter plot showing two classes of data points (blue circles and red squares) in a 2D space defined by Atributo 1 and Atributo 2.
<!-- /IMAGE_DESCRIPTION -->
### Visualização Geométrica de uma Árvore de Decisão

Objeto a ser classificado

A scatter plot with 'Atributo 1' on the x-axis and 'Atributo 2' on the y-axis, both ranging from 1 to 10. The plot contains three types of data points: blue circles, red squares with diagonal stripes, and a single purple square. The blue circles are clustered in the lower-left region (Atributo 1 < 5, Atributo 2 < 6). The red squares are clustered in the upper-right region (Atributo 1 > 5, Atributo 2 > 6). The purple square is located at approximately (4.5, 5.5). An arrow points from the text 'Objeto a ser classificado' to this purple square.

Scatter plot showing data points and a decision boundary.

```
graph TD; A[Atributo 1] -- "$\leq$ 7" --> B[Atributo 2]; A -- "> 7" --> C[ ]; B -- "$\leq$ 6" --> D[ ]; B -- "> 6" --> E[ ]; C --> F[ ]; D --> G[ ]; E --> H[ ]; F --> I[ ]; G --> J[ ]; H --> K[ ]; I --> L[ ]; J --> M[ ]; K --> N[ ]; L --> O[ ]; M --> P[ ]; N --> Q[ ]; O --> R[ ]; P --> S[ ]; Q --> T[ ]; R --> U[ ]; S --> V[ ]; T --> W[ ]; U --> X[ ]; V --> Y[ ]; W --> Z[ ]; X --> AA[ ]; Y --> AB[ ]; Z --> AC[ ];
```

A decision tree diagram illustrating the classification process. The root node is 'Atributo 1'. If the value is  $\leq 7$ , it leads to a node for 'Atributo 2'. If the value is  $> 7$ , it leads to a leaf node containing a red square. The 'Atributo 2' node branches into two paths:  $\leq 6$  and  $> 6$ . The  $\leq 6$  path leads to a leaf node containing a blue circle, and the  $> 6$  path leads to a leaf node containing a red square.

Decision tree diagram for classification.

{57}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-03afcee7dbcfc0af9eae2f7bf5eb6712_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Scatter plot showing data points and a decision boundary.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-e9bc763ebea46fe89aede23775517f44_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Scatter plot showing data points and a classification boundary.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-4c547ec1af44f8fcdc8b1d67662ac30a_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Scatter plot showing data points for a decision tree.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-b34c69e1ec326b01c3a485b27b1df5f6_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree diagram for the scatter plot.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-5000e9028ee2990f6242b2c0a952010d_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Scatter plot showing data points and a decision boundary.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-65e8c0628536d6d4245e9ab46ba070c3_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree diagram corresponding to the scatter plot.
<!-- /IMAGE_DESCRIPTION -->
### Visualização Geométrica de uma Árvore de Decisão

Objeto a ser classificado

A scatter plot with 'Atributo 1' on the x-axis and 'Atributo 2' on the y-axis, both ranging from 1 to 10. The plot contains two main groups of data points: blue circles and red squares with diagonal stripes. A purple diamond, representing the object to be classified, is located at approximately (4.5, 5.5). An arrow points from the text 'Objeto a ser classificado' to this purple diamond. The data points are distributed such that blue circles are generally in the lower-left region and red squares are in the upper-right region, with some overlap.

Scatter plot showing data points and a classification boundary.

```
graph TD; A[Atributo 1] -- "$\leq$ 7" --> B[Atributo 2]; A -- "> 7" --> C[ ]; B -- "$\leq$ 6" --> D[ ]; B -- "> 6" --> E[ ]; C --> F[ ]; D --> G[ ]; E --> H[ ]; F --> I[ ]; G --> J[ ]; H --> K[ ]; I --> L[ ]; J --> M[ ]; K --> N[ ]; L --> O[ ]; M --> P[ ]; N --> Q[ ]; O --> R[ ]; P --> S[ ]; Q --> T[ ]; R --> U[ ]; S --> V[ ]; T --> W[ ]; U --> X[ ]; V --> Y[ ]; W --> Z[ ]; X --> AA[ ]; Y --> AB[ ]; Z --> AC[ ];
```

A decision tree diagram illustrating the classification process. The root node is 'Atributo 1'. It splits into two branches:  $\leq 7$  and  $> 7$ . The  $> 7$  branch leads to a leaf node containing a red square. The  $\leq 7$  branch leads to a node labeled 'Atributo 2'. This node splits into two branches:  $\leq 6$  and  $> 6$ . The  $\leq 6$  branch leads to a leaf node containing a blue circle. The  $> 6$  branch leads to a leaf node containing a red square.

Decision tree diagram for classification.

{58}------------------------------------------------
### Visualização Geométrica de uma Árvore de Decisão

Objeto a ser classificado

Scatter plot showing data points for a decision tree. The x-axis is labeled 'Atributo 1' and the y-axis is labeled 'Atributo 2'. Both axes range from 1 to 10. Blue circles represent one class, and red squares with diagonal lines represent another. A vertical orange line is drawn at Atributo 1 = 7. A purple diamond, representing the object to be classified, is located at approximately (4.5, 5.5). An arrow points from the text 'Objeto a ser classificado' to this purple diamond.

Scatter plot showing data points for a decision tree. The x-axis is labeled 'Atributo 1' and the y-axis is labeled 'Atributo 2'. Both axes range from 1 to 10. Blue circles represent one class, and red squares with diagonal lines represent another. A vertical orange line is drawn at Atributo 1 = 7. A purple diamond, representing the object to be classified, is located at approximately (4.5, 5.5). An arrow points from the text 'Objeto a ser classificado' to this purple diamond.

```
graph TD; A[Atributo 1] -- "$\leq$ 7" --> B[Atributo 2]; A -- "> 7" --> C[Red Square]; B -- "$\leq$ 6" --> D[Blue Circle]; B -- "> 6" --> E[Red Square];
```

Decision tree diagram. The root node is 'Atributo 1' with a split at  $\leq 7$  and  $> 7$ . The  $\leq 7$  branch leads to a node 'Atributo 2' with a split at  $\leq 6$  and  $> 6$ . The  $> 7$  branch leads to a leaf node containing a red square. The  $\leq 6$  branch leads to a leaf node containing a blue circle. The  $> 6$  branch leads to a leaf node containing a red square.

Decision tree diagram. The root node is 'Atributo 1' with a split at $\leq$ 7 and > 7. The $\leq$ 7 branch leads to a node 'Atributo 2' with a split at $\leq$ 6 and > 6. The > 7 branch leads to a leaf node containing a red square. The $\leq$ 6 branch leads to a leaf node containing a blue circle. The > 6 branch leads to a leaf node containing a red square.

{59}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-9b1ec0090070bdf52ea28763b8d52477_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree diagram. The root node is 'Atributo 1' with a split at ≤ 7 and > 7. The ≤ 7 branch leads to a node 'Atributo 2' with a split at ≤ 6 and > 6. The > 7 branch leads to a leaf node containing a red square....
<!-- /IMAGE_DESCRIPTION -->
### Visualização Geométrica de uma Árvore de Decisão

Objeto a ser classificado

A scatter plot with 'Atributo 1' on the x-axis and 'Atributo 2' on the y-axis, both ranging from 1 to 10. The plot contains three types of data points: blue circles, red squares with diagonal stripes, and a single purple diamond. A vertical orange line is drawn at Atributo 1 = 7. An arrow points from the text 'Objeto a ser classificado' to the purple diamond, which is located at approximately (4.5, 5.5).

Scatter plot showing data points for classification based on two attributes.

```
graph TD; A[Atributo 1] -- "$\leq$ 7" --> B[Atributo 2]; A -- "> 7" --> C[Red Striped Square]; B -- "$\leq$ 6" --> D[Blue Circle]; B -- "> 6" --> E[Red Striped Square];
```

A decision tree diagram illustrating the classification logic. The root node is 'Atributo 1'. If the value is less than or equal to 7 ($\leq$ 7), it branches to a node for 'Atributo 2'. If the value is greater than 7 (> 7), it leads to a leaf node containing a red striped square. The 'Atributo 2' node further branches: if the value is less than or equal to 6 ($\leq$ 6), it leads to a leaf node containing a blue circle; if the value is greater than 6 (> 6), it leads to a leaf node containing a red striped square.

Decision tree diagram for the scatter plot.

<!-- DATALAB_CHUNK 4: pages 61-80 -->

{60}------------------------------------------------

# Visualização Geométrica de uma Árvore de Decisão

Objeto a ser classificado

A scatter plot with 'Atributo 1' on the x-axis and 'Atributo 2' on the y-axis, both ranging from 1 to 10. The plot shows two classes of data points: blue circles and red squares with diagonal stripes. A vertical orange line is drawn at Atributo 1 = 7, and a horizontal orange line is drawn at Atributo 2 = 6.5. These lines intersect at (7, 6.5). A purple diamond-shaped object is located at approximately (4.5, 5.5), with an arrow pointing to it from the text 'Objeto a ser classificado'.

Scatter plot showing data points and a decision boundary.

```
graph TD; A[Atributo 1] -- "$\leq$ 7" --> B[Atributo 2]; A -- "> 7" --> C[Red Square]; B -- "$\leq$ 6" --> D[Blue Circle]; B -- "> 6" --> E[Red Square];
```

A decision tree diagram illustrating the classification logic. The root node is 'Atributo 1'. If the value is less than or equal to 7 ($\leq$ 7), the tree proceeds to a node for 'Atributo 2'. If the value is greater than 7 (> 7), it leads to a leaf node containing a red square. The 'Atributo 2' node further splits: if the value is less than or equal to 6 ($\leq$ 6), it leads to a leaf node with a blue circle; if greater than 6 (> 6), it leads to a leaf node with a red square. The area under the '$\leq$ 7' branch is shaded brown, representing the region where Atributo 1 $\leq$ 7.

Decision tree diagram corresponding to the scatter plot.

{61}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-9fe11419dec507724d0362eb31c7b217_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Scatter plot showing data points for classification based on two attributes.
<!-- /IMAGE_DESCRIPTION -->
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

A decision tree diagram illustrating a hypothesis space. The root node is a green square labeled  $A$ . It splits into two branches:  $\leq a_1$  (left) and  $> a_1$  (right). The left branch leads to a green square labeled  $B$ , which splits into  $\leq b_2$  (left) and  $> b_2$  (right). The  $\leq b_2$  branch leads to a red square, and the  $> b_2$  branch leads to a green square labeled  $A$ . This  $A$  node splits into  $\leq a_4$  (left) and  $> a_4$  (right), leading to a gray square and a cyan square, respectively. The right branch from the root  $A$  leads to a green square labeled  $B$ , which splits into  $\leq b_3$  (left) and  $> b_3$  (right). The  $\leq b_3$  branch leads to a purple square, and the  $> b_3$  branch leads to a yellow square.

Decision tree diagram showing splits on variables A and B.

A 2D plot illustrating the hypothesis space in the  $A$ - $B$  plane. The horizontal axis is labeled  $A$  and the vertical axis is labeled  $B$ . The space is partitioned into six regions by vertical lines at  $a_4$  and  $a_1$  on the  $A$ -axis, and horizontal lines at  $b_2$  and  $b_3$  on the  $B$ -axis. The regions are colored as follows: a gray region for  $A \leq a_4$  and  $B > b_2$ ; a red region for  $A \leq a_4$  and  $B \leq b_2$ ; a cyan region for  $a_4 < A \leq a_1$  and  $B > b_2$ ; a purple region for  $a_4 < A \leq a_1$  and  $B \leq b_3$ ; a yellow region for  $A > a_1$  and  $B > b_3$ ; and a cyan region for  $A > a_1$  and  $B \leq b_3$ .

2D plot of the hypothesis space in the A-B plane.

{63}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-feae5a5b6e128162dbced0860fd97b9b_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree diagram showing splits on variables A and B.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-e91d950121dbb814d5c91603c7cd146e_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** 2D plot of the hypothesis space in the A-B plane.
<!-- /IMAGE_DESCRIPTION -->
### De árvores para regras

Regras: disjunções de conjunções lógicas

1. **Se**  $A \leq a_1$  **E**  $B \leq b_2$  **Então** Classe = Vermelha  
**OU**
2. **Se**  $A > a_1$  **E**  $B \leq b_3$  **Então** Classe = Laranja  
**OU**
- ...

```
graph TD; A1[A] -- "$\leq$ a₁" --> B1[B]; A1 -- "> a₁" --> B2[B]; B1 -- "$\leq$ b₂" --> R[Red]; B1 -- "> b₂" --> A2[A]; B2 -- "$\leq$ b₃" --> O[Orange]; B2 -- "> b₃" --> L[Light Green]; A2 -- "$\leq$ a₄" --> G[Dark Grey]; A2 -- "> a₄" --> C[Cyan];
```

The diagram illustrates a decision tree structure. The root node is a green square labeled 'A'. It splits into two branches based on the condition  $A \leq a_1$ . The left branch leads to a green square labeled 'B', and the right branch leads to another green square labeled 'B'. The left 'B' node splits into two branches based on the condition  $B \leq b_2$ : the left branch leads to a red square, and the right branch leads to a green square labeled 'A'. The right 'B' node splits into two branches based on the condition  $B \leq b_3$ : the left branch leads to an orange square, and the right branch leads to a light green square. The green 'A' node under the left 'B' node splits into two branches based on the condition  $A \leq a_4$ : the left branch leads to a dark grey square, and the right branch leads to a cyan square.

Decision tree diagram showing splits on variables A and B, leading to leaf nodes with different colors.

Exercício: complete as regras !

{64}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-575d7d345b3ec04393bb2ec720ebabca_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree diagram showing splits on variables A and B, leading to leaf nodes with different colors.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-f06d7a2fad72d80fe12fca1b65fc805b_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree diagram for 'Rendim. Tributáveis'. The root node is a yellow box labeled 'Rendim. Tributáveis'. It splits into two branches: one for values greater than 97.5K leading to leaf node LM1, and another for...
<!-- /IMAGE_DESCRIPTION -->
### Busca no Espaço de Hipóteses

- Não há **backtracking**
  - Impureza é minimizada localmente em cada nó!
    - Suposição: soma dos ótimos locais aproxima bem o ótimo global
- Espaço de hipóteses completo
  - A função objetivo certamente está contida nele
  - Sem *bias* de restrição
    - Proporcionando chances de *overfitting*
  - Com *bias de busca* (preferência)
    - Árvores com atributos que geram maior redução de impureza estão acima na árvore
    - Tal *bias* implica em tendência para árvores mais curtas

{65}------------------------------------------------
## Underfitting and Overfitting

The graph illustrates the relationship between the number of nodes in a model and the error rates on training and test sets. The x-axis represents the 'Number of nodes' from 0 to 300, and the y-axis represents the 'Error (%)' from 5 to 45. A solid red line shows the training set error, which decreases as the number of nodes increases. A dashed blue line shows the test set error, which initially decreases and then increases after a certain point. A vertical dashed red line at approximately 180 nodes marks the onset of overfitting, where the test set error begins to rise significantly while the training set error continues to fall.

| Number of nodes | Training set Error (%) | Test set Error (%) |
|-----------------|------------------------|--------------------|
| 10              | 38                     | 43                 |
| 50              | 28                     | 35                 |
| 100             | 22                     | 32                 |
| 150             | 16                     | 33                 |
| 180             | 14                     | 33                 |
| 200             | 12                     | 35                 |
| 250             | 9                      | 38                 |

Line graph showing Error (%) vs Number of nodes for Training and Test sets, illustrating overfitting.

Underfitting: quando o modelo é simples demais, ambos erros, de treino e de teste, são grandes.

{66}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-2865fd60541ac34a704bc9e7af1041f7_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Line graph showing Error (%) vs Number of nodes for Training and Test sets, illustrating overfitting.
<!-- /IMAGE_DESCRIPTION -->
## Regressão

A blue bar chart icon is centered within a white circle. The bar chart consists of four vertical bars of varying heights, with the second bar from the left being the tallest. The bars are set against a white background within the circle, and the circle itself is set against a dark blue background.

| Bar Index | Relative Height |
|-----------|-----------------|
| 1         | Medium          |
| 2         | Tallest         |
| 3         | Medium          |
| 4         | Shortest        |

Bar chart icon inside a white circle.

{67}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-dff659a422a9e5edd8ce41823a863379_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Bar chart icon inside a white circle.
<!-- /IMAGE_DESCRIPTION -->
### Árvores de Decisão para Problemas de Regressão

- Árvores de Regressão
  - Folha contém **média dos valores** do atributo alvo dos exemplos de treino que chegam até lá

```
graph TD; CHMIN((CHMIN)) -- "$\leq$ 7.5" --> CACH1((CACH)); CHMIN -- "> 7.5" --> MMAX1((MMAX)); CACH1 -- "$\leq$ 8.5" --> MMAX2((MMAX)); CACH1 -- "(8.5, 28]" --> Leaf1["64.6  
(24/19.2%)"]; MMAX1 -- "$\leq$ 28000" --> Leaf2["157  
(21/73.7%)"]; MMAX1 -- "> 28000" --> CHMAX((CHMAX)); MMAX2 -- "$\leq$ 2500" --> Leaf3["19.3  
(28/8.7%)"]; MMAX2 -- "(2500, 4250]" --> Leaf4["29.8  
(37/8.18%)"]; MMAX2 -- "> 4250" --> CACH2((CACH)); CACH2 -- "$\leq$ 0.5" --> MYCT((MYCT)); CACH2 -- "(0.5, 8.5]" --> Leaf5["59.3  
(24/16.9%)"]; MYCT -- "$\leq$ 550" --> Leaf6["37.3  
(19/11.3%)"]; MYCT -- "> 550" --> Leaf7["18.3  
(7/3.83%)"]; CHMAX -- "$\leq$ 58" --> MMIN((MMIN)); CHMAX -- "> 58" --> Leaf8["783  
(5/359%)"]; MMIN -- "$\leq$ 12000" --> Leaf9["281  
(11/56%)"]; MMIN -- "> 12000" --> Leaf10["492  
(7/53.9%)"]; CACH2 -- "$\leq$ 10000" --> Leaf11["75.7  
(10/24.6%)"]; CACH2 -- "> 10000" --> Leaf12["133  
(16/28.8%)"];
```

The diagram illustrates a decision tree for regression problems. The root node is CHMIN. It splits on the attribute CHMIN into two branches: $\leq$ 7.5 and > 7.5. The left branch leads to node CACH, which splits on CACH into $\leq$ 8.5 and (8.5, 28]. The right branch leads to node MMAX, which splits on MMAX into $\leq$ 28000 and > 28000. The left branch of MMAX leads to a leaf node with mean value 157 and count (21/73.7%). The right branch leads to node CHMAX, which splits on CHMAX into $\leq$ 58 and > 58. The left branch of CHMAX leads to node MMIN, which splits on MMIN into $\leq$ 12000 and > 12000. The right branch of CHMAX leads to a leaf node with mean value 783 and count (5/359%). The left branch of MMIN leads to a leaf node with mean value 281 and count (11/56%). The right branch of MMIN leads to a leaf node with mean value 492 and count (7/53.9%). The left branch of CACH leads to node MMAX, which splits on MMAX into $\leq$ 2500 and (2500, 4250]. The right branch of CACH leads to node CACH, which splits on CACH into $\leq$ 0.5 and (0.5, 8.5]. The left branch of MMAX leads to a leaf node with mean value 19.3 and count (28/8.7%). The right branch of MMAX leads to a leaf node with mean value 29.8 and count (37/8.18%). The left branch of CACH leads to node MYCT, which splits on MYCT into $\leq$ 550 and > 550. The right branch of CACH leads to a leaf node with mean value 59.3 and count (24/16.9%). The left branch of MYCT leads to a leaf node with mean value 37.3 and count (19/11.3%). The right branch of MYCT leads to a leaf node with mean value 18.3 and count (7/3.83%). The left branch of CACH leads to a leaf node with mean value 64.6 and count (24/19.2%). The right branch of CACH leads to a leaf node with mean value 75.7 and count (10/24.6%). The right branch of CACH leads to a leaf node with mean value 133 and count (16/28.8%).

Decision tree diagram for regression problems, showing splits on attributes CHMIN, CACH, MMAX, CHMAX, MMIN, MYCT, and leaf nodes with mean values and counts.

{68}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-27788c2a26d9641e68232a4eff1299b9_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree diagram for regression problems, showing splits on attributes CHMIN, CACH, MMAX, CHMAX, MMIN, MYCT, and leaf nodes with mean values and counts.
<!-- /IMAGE_DESCRIPTION -->
### Árvores de Decisão para Problemas de Regressão

- Árvores de Modelos
  - Folha contém **função de regressão (não-)linear** calculada sobre as instâncias que chegam até lá

![Decision tree diagram for regression problems. The root node is CHMIN. It splits into CACH ($\leq$ 7.5) and MMAX (> 7.5). CACH splits into MMAX ($\leq$ 8.5) and LM4 (50/22.1%) (> 8.5). MMAX splits into LM1 (65/7.32%) ($\leq$ 4250) and CACH (> 4250). CACH splits into LM2 (26/6.37%) ($\leq$ 0.5) and LM3 (24/14.5%) (0.5, 8.5]. MMAX splits into LM5 (21/45.5%) ($\leq$ 28000) and LM6 (23/63.5%) (> 28000).](e2b7490a3455c66c85db12872c78fcc3_img.jpg)

```
graph TD; CHMIN([CHMIN]) -- "$\leq$ 7.5" --> CACH1([CACH]); CHMIN -- "> 7.5" --> MMAX1([MMAX]); CACH1 -- "$\leq$ 8.5" --> MMAX2([MMAX]); CACH1 -- "> 8.5" --> LM4[LM4  
(50/22.1%)]; MMAX2 -- "$\leq$ 4250" --> LM1[LM1  
(65/7.32%)]; MMAX2 -- "> 4250" --> CACH2([CACH]); CACH2 -- "$\leq$ 0.5" --> LM2[LM2  
(26/6.37%)]; CACH2 -- "(0.5, 8.5]" --> LM3[LM3  
(24/14.5%)]; MMAX1 -- "$\leq$ 28000" --> LM5[LM5  
(21/45.5%)]; MMAX1 -- "> 28000" --> LM6[LM6  
(23/63.5%)];
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

Decision tree diagram for regression problems. The root node is CHMIN. It splits into CACH ($\leq$ 7.5) and MMAX (> 7.5). CACH splits into MMAX ($\leq$ 8.5) and LM4 (50/22.1%) (> 8.5). MMAX splits into LM1 (65/7.32%) ($\leq$ 4250) and CACH (> 4250). CACH splits into LM2 (26/6.37%) ($\leq$ 0.5) and LM3 (24/14.5%) (0.5, 8.5]. MMAX splits into LM5 (21/45.5%) ($\leq$ 28000) and LM6 (23/63.5%) (> 28000).

{69}------------------------------------------------
### Exemplo de Árvore de Regressão

catégorico      Catégorico      contínuo      alvo

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

Atributos Explanatórios

```
graph TD; Renda[Renda] -- "> 97.5K" --> Plus1[+1]; Renda -- "<= 97.5K" --> StatusConjugal[Status Conjugal]; StatusConjugal -- "Solteiro" --> Plus30[+30]; StatusConjugal -- "Casado" --> Plus3[+3];
```

Decision tree diagram for regression. The root node is 'Renda' (yellow). A red dashed arrow points to it from the label 'Atributos Explanatórios'. It splits into two branches: '> 97.5K' leading to a leaf node '+1' (blue), and '<= 97.5K' leading to a node 'Status Conjugal' (yellow). A red dashed arrow also points to 'Status Conjugal' from the label 'Atributos Explanatórios'. 'Status Conjugal' splits into two branches: 'Solteiro' leading to a leaf node '+30' (blue), and 'Casado' leading to a leaf node '+3' (blue). A large red arrow points from the training set table to the decision tree.

Conjunto de Treino

Modelo: Árvore de Regressão

{70}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-b35ea3e304aad7d350a9902270413930_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree diagram for regression. The root node is 'Renda' (yellow). A red dashed arrow points to it from the label 'Atributos Explanatórios'. It splits into two branches: '> 97.5K' leading to a leaf node '+1'...
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

| <i>Tid</i> | <i>Restituição</i> | <i>Status Conjugual</i> | <i>Rendim. Tributáveis</i> | <i>Atraso</i> |
|------------|--------------------|-------------------------|----------------------------|---------------|
| 1          | S                  | Solteiro                | 125K                       | 0             |
| 2          | N                  | Casado                  | 100K                       | 1             |
| 3          | N                  | Solteiro                | 70K                        | 30            |
| 4          | S                  | Casado                  | 120K                       | 2             |
| 5          | N                  | Solteiro                | 95K                        | 24            |
| 6          | N                  | Casado                  | 60K                        | 3             |
| 7          | S                  | Solteiro                | 220K                       | 1             |
| 8          | N                  | Solteiro                | 85K                        | 36            |
| 9          | N                  | Casado                  | 75K                        | 3             |
| 10         | N                  | Solteiro                | 90K                        | 30            |

categorico

Categorico

contínuo

alvo

Red arrow pointing from the training set table to the decision tree model.

*Atributo Explanatório*

```
graph TD; A[Rendim. Tributáveis] -- "> 97.5K" --> B[LM1]; A -- "<= 97.5K" --> C[LM2];
```

Decision tree diagram for 'Rendim. Tributáveis'. The root node is a yellow box labeled 'Rendim. Tributáveis'. It splits into two branches: one for values greater than 97.5K leading to leaf node LM1, and another for values less than or equal to 97.5K leading to leaf node LM2. A red dashed arrow points to the root node with the label 'Atributo Explanatório'.

LM num: 1

Delay =

$$18.2396 * \text{Status Conjugual}=\text{Solteiro} \\ - 0.1611 * \text{Rendim. Tributáveis} \\ + 16.2853$$

LM num: 2

Delay =

$$24.2168 * \text{Status Conjugual}=\text{Solteiro} \\ - 0.1458 * \text{Rendim. Tributáveis} \\ + 15.401$$

Conjunto de Treino

Modelo: Árvore de Regressão

{72}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-32b975e5eaf1c7bf9a072bf8b7f3aaad_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Red arrow pointing from the training set table to the decision tree model.
<!-- /IMAGE_DESCRIPTION -->
### Exemplo de Árvore Modelo

| <i>Tid</i> | Restitui<br>ção | Status<br>Conjugal | Renda | Atraso | Atraso<br>Predito | Diferen<br>ça |
|------------|-----------------|--------------------|-------|--------|-------------------|---------------|
| 1          | S               | Solteiro           | 125K  | 0      | 14,3874           | 14,3874       |
| 2          | N               | Casado             | 100K  | 1      | 0,1753            | 0,8247        |
| 3          | N               | Solteiro           | 70K   | 30     | 29,4118           | 0,5882        |
| 4          | S               | Casado             | 120K  | 2      | -3,0467           | 5,0467        |
| 5          | N               | Solteiro           | 95K   | 24     | 25,7668           | 1,7668        |
| 6          | N               | Casado             | 60K   | 3      | 6,653             | 3,653         |
| 7          | S               | Solteiro           | 220K  | 1      | -0,9171           | 1,9171        |
| 8          | N               | Solteiro           | 85K   | 36     | 27,2248           | 8,7752        |
| 9          | N               | Casado             | 75K   | 3      | 4,466             | 1,466         |
| 10         | N               | Solteiro           | 90K   | 30     | 26,4958           | 3,5042        |

Erro médio absoluto:  
4,193

Raiz do erro médio  
quadrático: 5,874

{73}------------------------------------------------
### Árvores de Decisão para Problemas de Regressão

- Principal mudança: medida de divisão de nós
  - Exemplo: standard deviation reduction (SDR)
    - Mesma fórmula genérica do “ganho”
    - Em vez de entropia ou Gini, apenas calcular o desvio padrão do atributo alvo para as instâncias de cada nó e ponderá-las pelas frequências

$$SDR = SD(v_{pai}) - \sum_{t=1}^k \frac{N(v_t)}{N} SD(v_t)$$

{74}------------------------------------------------
#### Árvore elementar: Calculando o Índice GINI

|     |             |                 |       |        | categorico |  |  |  |  | Categorico |  |  |  |  | continuo |  |  |  |  | alvo |  |  |  |  |
|-----|-------------|-----------------|-------|--------|------------|--|--|--|--|------------|--|--|--|--|----------|--|--|--|--|------|--|--|--|--|
| Tid | Restituição | Status Conjugal | Renda | Atraso |            |  |  |  |  |            |  |  |  |  |          |  |  |  |  |      |  |  |  |  |
| 1   | S           | Solteiro        | 125K  | 0      |            |  |  |  |  |            |  |  |  |  |          |  |  |  |  |      |  |  |  |  |
| 2   | N           | Casado          | 100K  | 1      |            |  |  |  |  |            |  |  |  |  |          |  |  |  |  |      |  |  |  |  |
| 3   | N           | Solteiro        | 70K   | 30     |            |  |  |  |  |            |  |  |  |  |          |  |  |  |  |      |  |  |  |  |
| 4   | S           | Casado          | 120K  | 2      |            |  |  |  |  |            |  |  |  |  |          |  |  |  |  |      |  |  |  |  |
| 5   | N           | Solteiro        | 95K   | 24     |            |  |  |  |  |            |  |  |  |  |          |  |  |  |  |      |  |  |  |  |
| 6   | N           | Casado          | 60K   | 3      |            |  |  |  |  |            |  |  |  |  |          |  |  |  |  |      |  |  |  |  |
| 7   | S           | Solteiro        | 220K  | 1      |            |  |  |  |  |            |  |  |  |  |          |  |  |  |  |      |  |  |  |  |
| 8   | N           | Solteiro        | 85K   | 36     |            |  |  |  |  |            |  |  |  |  |          |  |  |  |  |      |  |  |  |  |
| 9   | N           | Casado          | 75K   | 3      |            |  |  |  |  |            |  |  |  |  |          |  |  |  |  |      |  |  |  |  |
| 10  | N           | Solteiro        | 90K   | 30     |            |  |  |  |  |            |  |  |  |  |          |  |  |  |  |      |  |  |  |  |

|               |       |
|---------------|-------|
| Média         | 13,00 |
| Desvio Padrão | 14,93 |

Conjunto de Treino

{75}------------------------------------------------
#### Atributos Categóricos: Calculando o Índice GINI

*categórico*  
*Categórico*  
*contínuo*  
*alvo*

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

```

graph TD
    A[Restituição] -- S --> B[1]
    A -- N --> C[18,14]
    
```

Decision tree diagram for the 'Restituição' attribute. The root node is 'Restituição' (yellow box). It branches into two child nodes: 'S' (left, blue box with value 1) and 'N' (right, blue box with value 18,14).

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

*categorico*  
*Categorico*  
*contínuo*  
*alvo*

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

```

graph TD
    A[Status Conjugal] --> B[Solteiro]
    A --> C[Casado]
    B --> D[20,17]
    C --> E[2,25]
    
```

Decision tree diagram for Status Conjugal. The root node is 'Status Conjugal' (yellow box). It branches into 'Solteiro' (left) and 'Casado' (right). The 'Solteiro' branch leads to a leaf node with value '20,17' (blue box). The 'Casado' branch leads to a leaf node with value '2,25' (blue box).

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

Conjunto de Treino

{77}------------------------------------------------
### Exemplo Ilustrativo

Considere a seguinte árvore de regressão e a tabela logo a seguir, cujo atributo alvo é Rendimento\_Anual.

1: Preencha os valores para os nodos folha da árvore, a partir da tabela abaixo.

Image: Screenshot of Weka Classifier Tree Visualizer and Viewer showing a decision tree and a data table.

The image shows two windows from the Weka software. The top window, 'Weka Classifier Tree Visualizer', displays a decision tree. The root node is 'Restitucao=' with branches 'NAO' and 'SIM'. The 'NAO' branch leads to a node 'Calote=' with branches 'SIM' and 'NAO'. The 'SIM' branch leads to a leaf node containing the value '95.0'. The 'NAO' branch leads to a node 'Estado\_Civil=' with branches 'SOLTEIRO' and 'CASADO, DIVORCIADO'. The 'SIM' branch from the root leads to a node 'Estado\_Civil=' with branches 'SOLTEIRO, CASADO' and 'DIVORCIADO'. The bottom window, 'Viewer', shows a table with 7 rows and 6 columns. A red arrow points from the '95.0' value in the tree to the 'Rendimento\_Anual' column of the table. Another red arrow points from the '95.0' value in the table to the 'Rendimento\_Anual' column of the table.

Tree View

Restitucao=

NAO

SIM

Calote=

SIM

95.0

NAO

Estado\_Civil=

SOLTEIRO

CASADO, DIVORCIADO

Estado\_Civil=

SOLTEIRO, CASADO

DIVORCIADO

Viewer

Relation: TAN\_DecisionTree-weka.filters.unsupervised.attribute.Remove-R1

| No. | Restitucao<br>Nominal | Estado_Civil<br>Nominal | Calote<br>Nominal | Rendimento_Anual<br>Numeric | Rend_Anual Predito<br>Numeric |
|-----|-----------------------|-------------------------|-------------------|-----------------------------|-------------------------------|
| 1   | SIM                   | Solteiro                | NAO               | 125.0                       |                               |
| 2   | NAO                   | Casado                  | NAO               | 100.0                       |                               |
| 3   | NAO                   | Solteiro                | NAO               | 70.0                        |                               |
| 4   | SIM                   | Casado                  | NAO               | 120.0                       |                               |
| 5   | NAO                   | Divorciado              | SIM               | 95.0                        |                               |
| 6   | NAO                   | Casado                  | NAO               | 60.0                        |                               |
| 7   | SIM                   | Divorciado              | NAO               | 220.0                       |                               |

ERRO

$\Sigma$

{78}------------------------------------------------
### Exemplo Ilustrativo

Considere a seguinte árvore de regressão e a tabela logo a seguir, cujo atributo alvo é Rendimento\_Anual.

1: Preencha os valores para os nodos folha da árvore, a partir da tabela abaixo.

```
graph TD; A[Restituicao=] -- NAO --> B[Calote=]; A -- SIM --> C[Estado_Civil=]; B -- SIM --> D[95.0]; B -- NAO --> E[Estado_Civil=]; C -- SOLTEIRO, CASADO --> F[ ]; C -- DIVORCIADO --> G[ ]; E -- SOLTEIRO --> H[70.0]; E -- CASADO, DIVORCIADO --> I[ ];
```

Decision tree diagram showing splits on Restituicao, Calote, and Estado\_Civil attributes.

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

Undo OK Cancel

ERRO

|  |
|--|
|  |
|  |
|  |
|  |
|  |

$\Sigma$

|  |
|--|
|  |
|--|

{79}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-3198cdf0dbe501c46fe0e4073c7d8451_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree diagram showing splits on Restituicao, Calote, and Estado_Civil attributes.
<!-- /IMAGE_DESCRIPTION -->
### Exemplo Ilustrativo

Considere a seguinte árvore de regressão e a tabela logo a seguir, cujo atributo alvo é `Rendimento_Anual`.

1: Preencha os valores para os nodos folha da árvore, a partir da tabela abaixo.

```
graph TD;
    A[Restituicao=] -- NAO --> B[Calote=];
    A -- SIM --> C[Estado_Civil=];
    B -- SIM --> D[95.0];
    B -- NAO --> E[Estado_Civil=];
    E -- SOLTEIRO --> F[70.0];
    E -- CASADO, DIVORCIADO --> G[80.0];
    C -- SOLTEIRO, CASADO --> H[ ];
    C -- DIVORCIADO --> I[ ];
```

Decision tree diagram showing splits on 'Restituicao', 'Calote', and 'Estado\_Civil' attributes, leading to leaf nodes with predicted values 95.0, 70.0, and 80.0.

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

Undo OK Cancel

ERRO

|  |
|--|
|  |
|  |
|  |
|  |
|  |

$\Sigma$

|  |
|--|
|  |
|--|

<!-- DATALAB_CHUNK 5: pages 81-88 -->

{80}------------------------------------------------

# Exemplo Ilustrativo

Considere a seguinte árvore de regressão e a tabela logo a seguir, cujo atributo alvo é `Rendimento_Anual`.

1: Preencha os valores para os nodos folha da árvore, a partir da tabela abaixo.

```
graph TD; A[Restituicao=] -- NAO --> B[Calote=]; A -- SIM --> C[Estado_Civil=]; B -- SIM --> D[95.0]; B -- NAO --> E[Estado_Civil=]; E -- SOLTEIRO --> F[70.0]; E -- CASADO, DIVORCIADO --> G[80.0]; C -- SOLTEIRO, CASADO --> H[122.5]; C -- DIVORCIADO --> I[ ];
```

Decision tree diagram showing splits on Restituicao, Calote, and Estado\_Civil, leading to leaf nodes with predicted values 95.0, 70.0, 80.0, and 122.5.

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

Undo OK Cancel

ERRO

|  |
|--|
|  |
|  |
|  |
|  |
|  |

$\Sigma$

|  |
|--|
|  |
|--|

{81}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-18bb06865e2dada3656ea3d57f290f7f_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree diagram showing splits on 'Restituicao', 'Calote', and 'Estado_Civil' attributes, leading to leaf nodes with predicted values 95.0, 70.0, and 80.0.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-2f587210e4f97c32758c5972e2e83d20_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree diagram showing splits on Restituicao, Calote, and Estado_Civil, leading to leaf nodes with predicted values 95.0, 70.0, 80.0, and 122.5.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-dbd4bab54b57e8d1abf80e3de6471130_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree diagram showing splits on Restituicao, Calote, and Estado_Civil, leading to leaf nodes with predicted values.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-4806f9f95fff13a30d6523bd6ffeac63_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree diagram showing splits on 'Restituicao', 'Calote', and 'Estado_Civil' attributes, leading to leaf nodes with predicted values.
<!-- /IMAGE_DESCRIPTION -->
## Exemplo Ilustrativo

Considere a seguinte árvore de regressão e a tabela logo a seguir, cujo atributo alvo é Rendimento\_Anual.

1: Preencha os valores para os nodos folha da árvore, a partir da tabela abaixo.

Image: Weka Classifier Tree Visualizer and Viewer showing a regression tree and its training data.

The image displays two windows from the Weka software. The top window, 'Weka Classifier Tree Visualizer', shows a decision tree for predicting 'Rendimento\_Anual'. The tree structure is as follows:

- Root Node: Restituicao=
  - NAO branch: Calote=
    - SIM leaf: 95.0
    - NAO branch: Estado\_Civil=
      - SOLTEIRO leaf: 70.0
      - CASADO, DIVORCIADO leaf: 80.0
  - SIM branch: Estado\_Civil=
    - SOLTEIRO, CASADO leaf: 122.5
    - DIVORCIADO leaf: 220.0

The bottom window, 'Viewer', shows the training data table. The last row is highlighted in red, and its 'Rendimento\_Anual' value (220.0) is circled in red. A red arrow points from this value to the '220.0' leaf node in the tree.

| No. | Restituicao<br>Nominal | Estado_Civil<br>Nominal | Calote<br>Nominal | Rendimento_Anual<br>Numeric | Rend_Anual Predito<br>Numeric |
|-----|------------------------|-------------------------|-------------------|-----------------------------|-------------------------------|
| 1   | SIM                    | Solteiro                | NAO               | 125.0                       |                               |
| 2   | NAO                    | Casado                  | NAO               | 100.0                       |                               |
| 3   | NAO                    | Solteiro                | NAO               | 70.0                        |                               |
| 4   | SIM                    | Casado                  | NAO               | 120.0                       |                               |
| 5   | NAO                    | Divorciado              | SIM               | 95.0                        |                               |
| 6   | NAO                    | Casado                  | NAO               | 60.0                        |                               |
| 7   | SIM                    | Divorciado              | NAO               | 220.0                       |                               |

Below the table, there is a section for error calculation:

ERRO

|  |
|--|
|  |
|  |
|  |
|  |
|  |
|  |

$\Sigma$

{82}------------------------------------------------
## Exemplo Ilustrativo

Considere a seguinte árvore de regressão e a tabela logo a seguir, cujo atributo alvo é Rendimento\_Anual.

1: Preencha os valores para os nodos folha da árvore, a partir da tabela abaixo.

```
graph TD; A[Restituicao=] -- NAO --> B[Calote=]; A -- SIM --> C[Estado_Civil=]; B -- SIM --> D[95.0]; B -- NAO --> E[Estado_Civil=]; C -- SOLTEIRO, CASADO --> F[122.5]; C -- DIVORCIADO --> G[220.0]; E -- SOLTEIRO --> H[70.0]; E -- CASADO, DIVORCIADO --> I[80.0];
```

Decision tree diagram showing splits on Restituicao, Calote, and Estado\_Civil, leading to leaf nodes with predicted values.

Viewer

Relation: TAN\_DecisionTree-weka.filters.unsupervised.attribute.Remove-R1

| No. | Restituicao<br>Nominal | Estado_Civil<br>Nominal | Calote<br>Nominal | Rendimento_Anual<br>Numeric | Rend_Anual Predito<br>Numeric |
|-----|------------------------|-------------------------|-------------------|-----------------------------|-------------------------------|
| 1   | SIM                    | Solteiro                | NAO               | 125.0                       | 122.5                         |
| 2   | NAO                    | Casado                  | NAO               | 100.0                       |                               |
| 3   | NAO                    | Solteiro                | NAO               | 70.0                        |                               |
| 4   | SIM                    | Casado                  | NAO               | 120.0                       |                               |
| 5   | NAO                    | Divorciado              | SIM               | 95.0                        |                               |
| 6   | NAO                    | Casado                  | NAO               | 60.0                        |                               |
| 7   | SIM                    | Divorciado              | NAO               | 220.0                       |                               |

Undo OK Cancel

ERRO

|  |
|--|
|  |
|  |
|  |
|  |
|  |

$\Sigma$

|  |
|--|
|  |
|--|

{83}------------------------------------------------
## Exemplo Ilustrativo

Considere a seguinte árvore de regressão e a tabela logo a seguir, cujo atributo alvo é `Rendimento_Anual`.

1: Preencha os valores para os nodos folha da árvore, a partir da tabela abaixo.

```
graph TD; A[Restituicao=] -- NAO --> B[Calote=]; A -- SIM --> C[Estado_Civil=]; B -- SIM --> D[95.0]; B -- NAO --> E[Estado_Civil=]; C -- SOLTEIRO, CASADO --> F[122.5]; C -- DIVORCIADO --> G[220.0]; E -- SOLTEIRO --> H[70.0]; E -- CASADO, DIVORCIADO --> I[80.0];
```

Decision tree diagram showing splits on 'Restituicao', 'Calote', and 'Estado\_Civil' attributes, leading to leaf nodes with predicted values.

Viewer

Relation: TAN\_DecisionTree-weka.filters.unsupervised.attribute.Remove-R1

| No. | Restituicao<br>Nominal | Estado_Civil<br>Nominal | Calote<br>Nominal | Rendimento_Anual<br>Numeric | Rend_Anual Predito<br>Numeric |
|-----|------------------------|-------------------------|-------------------|-----------------------------|-------------------------------|
| 1   | SIM                    | Solteiro                | NAO               | 125.0                       | 122.5                         |
| 2   | NAO                    | Casado                  | NAO               | 100.0                       | 80.0                          |
| 3   | NAO                    | Solteiro                | NAO               | 70.0                        | 70.0                          |
| 4   | SIM                    | Casado                  | NAO               | 120.0                       | 122.5                         |
| 5   | NAO                    | Divorciado              | SIM               | 95.0                        | 95.0                          |
| 6   | NAO                    | Casado                  | NAO               | 60.0                        | 80.0                          |
| 7   | SIM                    | Divorciado              | NAO               | 220.0                       | 220.0                         |

Undo OK Cancel

ERRO

|  |
|--|
|  |
|  |
|  |
|  |
|  |
|  |

$\Sigma$

|  |
|--|
|  |
|--|

{84}------------------------------------------------
## Exemplo Ilustrativo

Considere a seguinte árvore de regressão e a tabela logo a seguir, cujo atributo alvo é Rendimento\_Anual.

1: Preencha os valores para os nodos folha da árvore, a partir da tabela abaixo.

```
graph TD; A[Restitucao=] -- NAO --> B[Calote=]; A -- SIM --> C[Estado_Civil=]; B -- SIM --> D[95.0]; B -- NAO --> E[Estado_Civil=]; C -- SOLTEIRO, CASADO --> F[122.5]; C -- DIVORCIADO --> G[220.0]; E -- SOLTEIRO --> H[70.0]; E -- CASADO, DIVORCIADO --> I[80.0];
```

Decision tree diagram showing splits on Restitucao, Calote, and Estado\_Civil, leading to predicted values.

Relation: TAN\_DecisionTree-weka.filters.unsupervised.attribute.Remove-R1

| No. | Restitucao<br>Nominal | Estado_Civil<br>Nominal | Calote<br>Nominal | Rendimento_Anual<br>Numeric | Rend_Anual Predito<br>Numeric |
|-----|-----------------------|-------------------------|-------------------|-----------------------------|-------------------------------|
| 1   | SIM                   | Solteiro                | NAO               | 125.0                       | 122.5                         |
| 2   | NAO                   | Casado                  | NAO               | 100.0                       | 80.0                          |
| 3   | NAO                   | Solteiro                | NAO               | 70.0                        | 70.0                          |
| 4   | SIM                   | Casado                  | NAO               | 120.0                       | 122.5                         |
| 5   | NAO                   | Divorciado              | SIM               | 95.0                        | 95.0                          |
| 6   | NAO                   | Casado                  | NAO               | 60.0                        | 80.0                          |
| 7   | SIM                   | Divorciado              | NAO               | 220.0                       | 220.0                         |

Undo OK Cancel

ERRO

|      |
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

Atenção! Erro é sempre Positivo!!!

{85}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-c07e21a8d65991db04263322f859c94f_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decision tree diagram showing splits on Restitucao, Calote, and Estado_Civil, leading to predicted values.
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
