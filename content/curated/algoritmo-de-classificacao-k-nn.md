<!-- EXEC_SUMMARY_START -->
## Sumário
> *Leia antes de varrer o arquivo. Vá direto à seção relevante para a pergunta do aluno.*

- **Classificação com k-NN**
- **Roteiro**
- **Subáreas da Inteligência Artificial**
- **Aprendizado Supervisionado**
- **Aprendizado Supervisionado**
- **Aprendizado Supervisionado**
- **Aprendizado Supervisionado**
  - Classificação
  - Regressão
  - Regressão
  - Classificação
  - Classificação
  - Classificação
  - Classificação
  - Classificação
  - Classificação
  - Classificação
  - Classificador Linear Simples
  - Classificação
  - Classificador Linear
  - Classificação
  - Classificador Linear
  - Classificação
  - Classificador Linear
  - Algoritmo k-NN
  - Algoritmo k-NN
  - Algoritmo k-NN
  - Algoritmo k-NN
  - Algoritmo k-NN
  - Algoritmo k-NN
  - Algoritmo k-NN
  - Algoritmo k-NN
- **Referências**
- **Imagens Curadas**

<!-- EXEC_SUMMARY_END -->
{0}------------------------------------------------

# Aprendizado Supervisionado

Parte 1
## Classificação com k-NN

Profa Silvia Moraes

A stack of colorful folders or documents, suggesting data organization. The folders are in various colors like red, orange, yellow, green, and blue, and are stacked in a way that creates a sense of depth and volume.

A stack of colorful folders or documents, suggesting data organization.

A stylized graphic of a brain composed of glowing circuit lines, symbolizing artificial intelligence or machine learning. The brain is depicted with a network of blue and purple lines, giving it a digital and futuristic appearance.

A stylized graphic of a brain composed of glowing circuit lines, symbolizing artificial intelligence or machine learning.

{1}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-5fb340ad68b0c71df0b56698b137e35b_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A stack of colorful folders or documents, suggesting data organization.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-390120de4fe440c42fea8154fcaad334_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A stylized graphic of a brain composed of glowing circuit lines, symbolizing artificial intelligence or machine learning.
<!-- /IMAGE_DESCRIPTION -->
## Roteiro

- Relembrando
  - Machine Learning: Aprendizado Supervisionado
  - Tarefas Preditivas
- Classificação
  - Classificadores Lineares
  - Algoritmo k-NN

{2}------------------------------------------------
## Subáreas da Inteligência Artificial

The diagram illustrates the subfields of Artificial Intelligence (IA) centered around a hub labeled "Inteligência Artificial (IA)". The subfields are arranged in a circular pattern around the center, with lines connecting them to the central hub. The subfields are:

- Aprendizado de Máquina (Machine Learning)** (highlighted in red)
  - Aprendizado Profundo (Deep Learning)
  - Aprendizado Supervisionado** (highlighted in green)
  - Aprendizado Não Supervisionado
  - Aprendizado por Reforço
  - Aprendizado auto-supervisionado
  - Aprendizado semissupervisionado
- Processamento de Linguagem Natural
  - Extração de Informações
  - Classificação de Texto
  - Tradução Automática
  - Perguntas e Respostas
  - Geração de Texto
- Raciocínio Automatizado
- Robótica
- IA Explicável
- Visão Computacional

Diagram showing subfields of Artificial Intelligence (IA) arranged around a central hub.

{3}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-1b7d539e02a202c2cf2d97698b911447_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram showing subfields of Artificial Intelligence (IA) arranged around a central hub.
<!-- /IMAGE_DESCRIPTION -->
## Aprendizado Supervisionado

- Exige que os **dados** estejam **rotulados** (anotados com suas respectivas classes/valores de saída)
- Os algoritmos que seguem esse tipo de aprendizado recebem pares de valores:
  - os dados de entrada (x) e
  - os valores de saída (rótulos) correspondentes (y).

**Saída (y):**  
rótulo/classe/anotação

**Entrada (x):**  
Imagem ou características

**Gato**

**Cachorro**

**Galinha**

<https://www.pexels.com/>

The diagram illustrates a supervised learning dataset. It shows three examples of input-output pairs. Each example consists of an input image (x) and a corresponding output label (y). The first example is a cat, labeled 'Gato'. The second example is a dog, labeled 'Cachorro'. The third example is a chicken, labeled 'Galinha'. The input images are arranged in a vertical stack, and the output labels are placed below them. A URL 'https://www.pexels.com/' is visible on the cat image.

Diagram of a supervised learning dataset showing three examples: a cat, a dog, and a chicken, each with its corresponding input image and output label.

**Dataset Anotado**

{4}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-9e6062272bbe3ddbb7c0606721d64cf0_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a supervised learning dataset showing three examples: a cat, a dog, and a chicken, each with its corresponding input image and output label.
<!-- /IMAGE_DESCRIPTION -->
## Aprendizado Supervisionado

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

Three photographs of Iris flowers are shown side-by-side. The left image is labeled 'Iris Virginica' and shows a light blue flower with white markings. The middle image is labeled 'Iris Setosa' and shows a dark blue flower. The right image is labeled 'Iris Versicolor' and shows a vibrant blue flower.

Three photographs of Iris flowers: Iris Virginica, Iris Setosa, and Iris Versicolor.

{5}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-764bb8d7c93b090e205d908e1a8cade4_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Three photographs of Iris flowers: Iris Virginica, Iris Setosa, and Iris Versicolor.
<!-- /IMAGE_DESCRIPTION -->
## Aprendizado Supervisionado

- O objetivo é encontrar um modelo capaz de mapear os valores de entrada ( $x$ ) nos valores de saída  $y$ .
- Em outras palavras, que aproxime  $f$ , tal que  $f(x) = y$ .
- Supervisão: ajuste usando o erro em relação à saída esperada.

The diagram illustrates the supervised learning process. It begins with a **Dataset Anotado** (Annotated Dataset) on the left, which consists of three images with labels: a cat labeled "Gato", a dog labeled "Cachorro", and a chicken labeled "Galinha". An arrow points from this dataset to a central box representing the **Algoritmo de Machine Learning Supervisionado** (Supervised Machine Learning Algorithm). Inside this box, the word **Treinamento** (Training) is shown above a small neural network icon. A second arrow points from the algorithm box to a final box on the right labeled **Modelo** (Model), which also contains a neural network icon.

Diagram of the supervised learning process: Dataset Anotado (Gato, Cachorro, Galinha) -> Algoritmo de Machine Learning Supervisionado (Treinamento) -> Modelo.

{6}------------------------------------------------

Modelo Probabilístico

<!-- IMAGE_DESCRIPTION: datalab-a7d78d22e465dea388b31d0739f9d0cd_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of the supervised learning process: Dataset Anotado (Gato, Cachorro, Galinha) -> Algoritmo de Machine Learning Supervisionado (Treinamento) -> Modelo.
<!-- /IMAGE_DESCRIPTION -->
## Aprendizado Supervisionado

- **Tarefa preditiva:** encontra uma função (modelo) a partir dos dados de treino que possa ser usada para prever um rótulo (classe) ou valor de um novo exemplo.
- Pode ser:
  - **classificação** (rótulos discretos)
  - **regressão** (rótulos contínuos)

{7}------------------------------------------------
### Classificação

The diagram illustrates a supervised machine learning classification workflow. It begins with an input image of a cat, labeled 'Imagem sem rótulo' (Image without label) and 'Entrada' (Input). An arrow points from this image to a central teal box representing the 'Algoritmo de Machine Learning Supervisionado' (Supervised Machine Learning Algorithm). Below this box is the label 'Generalização' (Generalization). An arrow points from the algorithm box to the output 'gato (96%)' (cat (96%)), which is labeled 'Predição' (Prediction). A smaller box labeled 'Modelo' (Model) is positioned below the main algorithm box, containing a neural network diagram.

Diagram of a supervised machine learning classification process.

- É o processo de automaticamente atribuir rótulos a dados.
- Pode ser do tipo
  - Binária: possui apenas duas classes
  - Multiclasse: possui mais de duas classes
- Pode atribuir
  - Um único rótulo (single label)
  - Vários rótulos (multi-label)

A photograph of a tomato sorting machine in operation. A red banner at the bottom of the image contains the text 'Máquina de triagem de tomate' (Tomato sorting machine) in green letters. The machine is sorting red tomatoes on a conveyor belt.

Tomato sorting machine with classification label.

{8}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-2ee59e629035d641140e55f4d215b0d7_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a supervised machine learning classification process.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-efca2dce0095c9dc2a68e9af6b2bfd40_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Tomato sorting machine with classification label.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-e6df2733626a85205c1db682e6259c46_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of supervised machine learning generalization.
<!-- /IMAGE_DESCRIPTION -->
### Regressão

- É o processo de automaticamente predizer novos valores  $y$ .
- Neste caso, os dados são anotados com valores.

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
| 2022 | 3.5 (predicted) |

Line graph showing data points from 2015 to 2021 and a dashed red line with a question mark for 2022, representing a regression model.

A scatter plot showing training data points (blue dots) and a fitted regression curve (red line). The x-axis ranges from 0 to 100, and the y-axis ranges from -1 to 4. The data points show a non-linear, wavy pattern, and the red curve follows this pattern, representing a non-linear regression model.

| x   | y (training data) | y (regression) |
|-----|-------------------|----------------|
| 0   | 0.5               | 0.5            |
| 20  | 1.0               | 1.0            |
| 40  | 0.0               | 0.0            |
| 60  | 1.5               | 1.5            |
| 80  | 3.5               | 3.5            |
| 100 | 3.0               | 3.0            |

Scatter plot with a fitted regression curve, showing training data points and a red regression line.

{9}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-91be14371a97fb5ce9eeb29ae18d07c3_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Line graph showing data points from 2015 to 2021 and a dashed red line with a question mark for 2022, representing a regression model.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-bedcca5cdf168e3508ef511d94ec514c_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Scatter plot with a fitted regression curve, showing training data points and a red regression line.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-7801d00a216dc4dc8a7d210dcb5fe3c5_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Scatter plot showing training data points (blue dots) and a fitted regression line (red line).
<!-- /IMAGE_DESCRIPTION -->
### Regressão

![Diagram of supervised machine learning training. A dataset of pairs [x, f(x)] is input into a supervised machine learning algorithm. The algorithm performs training (represented by a neural network icon) to create a model. The model then takes an input x and produces an output f(x), with a red x^2 indicating the specific function being learned.](f4fdd410cdb84df81274da55721e56fb_img.jpg)

$[x, f(x)]$   
[ 1, 1]  
[ 2, 4]  
[ 3, 9]  
[ 4, 16]  
[ 5, 25]

**Dataset Anotado**

$x$   $\xrightarrow{?}$   $f(x)$

**Algoritmo de Machine Learning Supervisionado**

**Treinamento**

**Modelo**

$x$   $\xrightarrow{x^2}$   $f(x)$

Diagram of supervised machine learning training. A dataset of pairs [x, f(x)] is input into a supervised machine learning algorithm. The algorithm performs training (represented by a neural network icon) to create a model. The model then takes an input x and produces an output f(x), with a red x^2 indicating the specific function being learned.

training data  
regression

Scatter plot showing training data points (blue dots) and a fitted regression line (red line). The x-axis ranges from 0 to 100, and the y-axis ranges from -1 to 4. The data points follow a parabolic trend, and the regression line fits the data well.

**6**  
**Entrada**

**Algoritmo de Machine Learning Supervisionado**

**Generalização**

**Modelo**

$x$   $\xrightarrow{x^2}$   $f(x)$

Diagram of supervised machine learning generalization. An input of 6 is fed into the trained model. The model generalizes the learned function to produce the output f(x), which is 36 (6 squared).

{10}------------------------------------------------
### Classificação

The diagram illustrates a classification process. On the left, a stack of documents is shown, with the top document labeled "Acme Article". Three lines branch out from this stack to three separate stacks of documents on the right. The top stack is labeled "Technology", the middle stack is labeled "Sports", and the bottom stack is labeled "Entertainment". Each stack on the right contains multiple documents, with the top document of each stack labeled "Test Article".

Diagram illustrating article classification from a source to three categories: Technology, Sports, and Entertainment.

{11}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-5b4e774d63e0e0ed73801a9247755e5f_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram illustrating article classification from a source to three categories: Technology, Sports, and Entertainment.
<!-- /IMAGE_DESCRIPTION -->
### Classificação

A close-up photograph of a grasshopper with brown and black striped patterns on its body and wings. It is positioned on a rough, light-colored rock surface.

A brown and black striped grasshopper on a rock.

A close-up photograph of a bright green katydid (leaf insect) resting on a smooth, pinkish surface. The insect's body is perfectly camouflaged to look like a green leaf.

A green katydid on a pink surface.

Como classificar Gafanhotos ?

{12}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-ec0158057f8ccaf74edba16682ec5444_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A brown and black striped grasshopper on a rock.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-e3b8510f6a2194e250205ab7bc38076d_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A green katydid on a pink surface.
<!-- /IMAGE_DESCRIPTION -->
### Classificação

Se os dados desses insetos fossem estruturados, que atributos/características seriam mais importantes e significativos para a classificação?

Diagram illustrating the classification attributes of an insect (grasshopper) based on its physical characteristics:

- Cor: {Verde, Marrom, Cinza, Outra}
- Tem asas?
- Comprimento do abdômen
- Comprimento do Tórax
- Comprimento das antenas
- Tamanho da mandíbula
- Comprimento das pernas
- Diâmetro dos orifícios de respiração

Diagram of a grasshopper with labeled anatomical features for classification.

{13}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-bb6d33498937738ff5dac8d91c9ebaad_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a grasshopper with labeled anatomical features for classification.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-7832324609ad3cc688064e0341612b32_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a grasshopper with labeled anatomical features for classification.
<!-- /IMAGE_DESCRIPTION -->
### Classificação

Se os dados desses insetos fossem estruturados, que atributos/características seriam mais importantes e significativos para a classificação?

Diagram illustrating the classification attributes of an insect (grasshopper) based on its body parts and color:

- Cor: {Verde, Marrom, Cinza, Outra}
- Tem asas?
- Comprimento do abdômen
- Comprimento do Tórax
- Comprimento das antenas
- Tamanho da mandíbula
- Diâmetro dos orifícios de respiração
- Comprimento das pernas

Diagram of a grasshopper with labeled anatomical features for classification.

{14}------------------------------------------------
### Classificação

Diagrama de um gafanhoto com labels para características físicas:

- Cor: {Verde, Marrom, Cinza, Outra}
- Comprimento do abdômen
- Comprimento do Tórax
- Comprimento das antenas
- Tamanho da mandíbula
- Comprimento das pernas
- Diâmetro dos orifícios de respiração

Diagrama de um gafanhoto com labels para características físicas: Cor: {Verde, Marrom, Cinza, Outra}, Comprimento do abdômen, Comprimento do Tórax, Comprimento das antenas, Tamanho da mandíbula, Comprimento das pernas, Diâmetro dos orifícios de respiração.

Se tivermos um **conjunto de dados anotados com as classes dos gafanhotos**, poderemos aplicar um algoritmo de classificação para prever a classe de novos insetos desse tipo.

| ID | Compr. Abdômen | Compr. Antenas | Classe    | ID | Compr. Abdômen | Compr. Antenas | Classe    |
|----|----------------|----------------|-----------|----|----------------|----------------|-----------|
| 1  | 2,7            | 5,5            | Gafanhoto | 6  | 2,9            | 1,9            | Gafanhoto |
| 2  | 8,0            | 9,1            | Esperança | 7  | 6,1            | 6,6            | Esperança |
| 3  | 0,9            | 4,7            | Gafanhoto | 8  | 0,5            | 1,0            | Gafanhoto |
| 4  | 1,1            | 3,1            | Gafanhoto | 9  | 8,3            | 6,6            | Esperança |
| 5  | 5,4            | 8,5            | Esperança | 10 | 8,1            | 4,7            | Esperança |

Qual a classe de um inseto com comprimento 5,1 de abdômen e 7,0 mm de antenas?

{15}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-589af9a5d6f5bbbdc8f482e364688676_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de um gafanhoto com labels para características físicas: Cor: {Verde, Marrom, Cinza, Outra}, Comprimento do abdômen, Comprimento do Tórax, Comprimento das antenas, Tamanho da mandíbula, Comprimento das pernas...
<!-- /IMAGE_DESCRIPTION -->
### Classificação

A scatter plot illustrating the classification of insects based on two morphological features: the length of the abdomen (x-axis) and the length of the antennae (y-axis). Both axes range from 1 to 10. The plot shows three distinct groups of data points: blue circles, red squares, and a single purple diamond. An arrow points from a detailed line drawing of an insect to the purple diamond, indicating its classification.

| Comprimento do abdômen | Comprimento das antenas | Classe         |
|------------------------|-------------------------|----------------|
| 1.0                    | 1.2                     | Blue Circle    |
| 1.2                    | 3.4                     | Blue Circle    |
| 1.2                    | 4.8                     | Blue Circle    |
| 2.8                    | 2.0                     | Blue Circle    |
| 2.8                    | 5.6                     | Blue Circle    |
| 5.1                    | 7.0                     | Purple Diamond |
| 5.5                    | 8.6                     | Red Square     |
| 6.8                    | 6.8                     | Red Square     |
| 8.2                    | 4.8                     | Red Square     |
| 8.2                    | 6.8                     | Red Square     |
| 8.2                    | 9.4                     | Red Square     |

Scatter plot showing the classification of insects based on antenna length and abdomen length.

Qual a classe de um inseto com comprimento 5,1 de abdômen e 7,0 mm de antenas?

{16}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-b05fbb6a015ea153c1e25245772b1a1b_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Scatter plot showing the classification of insects based on antenna length and abdomen length.
<!-- /IMAGE_DESCRIPTION -->
### Classificação
### Classificador Linear Simples

Se o exemplo desconhecido está acima da linha  
Então a classe é **Esperança**  
Senão a classe é **Gafanhoto**

The scatter plot shows a 2D coordinate system with both X and Y axes ranging from 1 to 10. A thick orange line, representing the decision boundary, slopes downwards from left to right, passing through approximately (2, 10) and (8, 0). Data points are categorized as follows:

- Gafanhoto (Blue Circles):** Located below the orange line at approximately (1, 1.2), (1, 3.5), (1, 4.8), (3, 2.0), and (3, 5.5).
- Esperança (Red Squares with Diagonal Stripes):** Located above the orange line at approximately (5.5, 8.5), (6.5, 6.8), (8.5, 4.8), (8.5, 6.8), (8.5, 9.5), and (9.5, 7.0).
- Unknown Example (Purple Diamond):** Located at approximately (5.5, 7.2), which is above the orange line, thus classified as 'Esperança'.

Scatter plot illustrating a simple linear classifier. The plot shows data points on a 2D grid (X and Y axes from 1 to 10). A thick orange line acts as the decision boundary. Points above the line are classified as 'Esperança' (represented by red squares with diagonal stripes), and points below the line are classified as 'Gafanhoto' (represented by blue circles). A purple diamond represents an unknown example being classified.

{17}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-fed39b841ae2dce01088b84bfc1e2789_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Scatter plot illustrating a simple linear classifier.
<!-- /IMAGE_DESCRIPTION -->
### Classificação
### Classificador Linear

Pode ser usado para mais dimensões.

Nesse caso, a divisão não será por uma reta (linha) mas por um hiperplano .

The figure consists of two side-by-side 3D plots within a single frame. Both plots show a 3D coordinate system with a grid. In the left plot, there are two sets of data points: red spheres and gray spheres. A yellow semi-transparent plane (the hyperplane) is positioned to separate the red points from the gray points. In the right plot, the same set of red and gray points is shown, but the yellow hyperplane is tilted at a different angle, demonstrating a different linear decision boundary for the same data.

Two 3D plots illustrating linear classification in 3D space. The left plot shows two classes of data points (red and gray) separated by a yellow hyperplane. The right plot shows the same data points with a yellow hyperplane that is tilted, illustrating a different linear decision boundary.

{18}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-ef25c3cf1fdb334fc8679e85ab5265ca_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Two 3D plots illustrating linear classification in 3D space.
<!-- /IMAGE_DESCRIPTION -->
### Classificação
### Classificador Linear

Limitação: resolve apenas problemas cujas classes são linearmente separáveis.

A scatter plot on a 10x10 grid with a yellow background. The x-axis and y-axis are both labeled from 1 to 10. Red squares are located in the upper-left region, and blue circles are in the lower-right region. A thick orange diagonal line, running from the bottom-left to the top-right, perfectly separates the two classes with no misclassifications.

Scatter plot showing perfect linear classification.

Classificação Perfeita

A scatter plot on a 100x100 grid with a light blue background. The x-axis and y-axis are both labeled from 10 to 100 in increments of 10. Red squares are in the upper-right region, and blue circles are in the lower-left region. A thick orange diagonal line separates the classes, with a few red squares misclassified in the lower-right area.

Scatter plot showing very good linear classification.

Classificação Muito Boa

A scatter plot on a 10x10 grid with a light green background. The x-axis and y-axis are both labeled from 1 to 10. Red squares and blue circles are scattered across the grid. A thick orange diagonal line is drawn, but it fails to separate the classes, with many red squares and blue circles misclassified on both sides of the line.

Scatter plot showing useless linear classification.

Classificação Inútil

{19}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-1c427123350e0e73e2a109b79069314b_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Scatter plot showing perfect linear classification.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-93587f920736a2fdcefeba94b29f302a_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Scatter plot showing very good linear classification.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-8a597e344d10e36bbb2f243f6c4e74c6_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Scatter plot showing useless linear classification.
<!-- /IMAGE_DESCRIPTION -->
### Classificação
### Classificador Linear
#### Exemplo: **Planta Iris**

- 150 amostras: Dataset Balanceado
  - 50 Iris Setosa,
  - 50 Iris Virginica e
  - 50 Iris Versicolor
- Podemos generalizar o classificador para N classes, encontrando N-1 hiperplanos:
  1. O primeiro hiperplano separa a Setosa das outras duas Versicolor/Virginica
  2. O segundo hiperplano separa Versicolor de Virginica

A scatter plot illustrating the linear classification of the Iris dataset. The plot shows three distinct clusters of data points: Setosa (blue pluses) in the lower-left, Versicolor (green dots) in the center, and Virginica (red crosses) in the upper-right. Two orange lines represent linear decision boundaries. The first line, with a steep negative slope, separates the Setosa cluster from the other two. The second line, with a shallower negative slope, separates the Versicolor cluster from the Virginica cluster. The axes are marked with tick marks but lack numerical labels.

Scatter plot of the Iris dataset showing three classes: Setosa (blue pluses), Versicolor (green dots), and Virginica (red crosses). Two orange lines represent linear decision boundaries. The first line separates Setosa from the other two classes. The second line separates Versicolor from Virginica.

{20}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-f85bf99d372e735d228361bf4d3cf7e6_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Scatter plot of the Iris dataset showing three classes: Setosa (blue pluses), Versicolor (green dots), and Virginica (red crosses).
<!-- /IMAGE_DESCRIPTION -->
### Algoritmo k-NN

**K- Nearest Neighbour :**  
algoritmo dos k vizinhos  
mais próximos.

Considera os objetos mais  
próximos com  
características semelhantes  
para prever a classe de  
um novo dado.

The diagram illustrates the K-Nearest Neighbour (k-NN) algorithm. It shows a 2D space with several data points. There are three red squares labeled 'A' and five blue circles labeled 'B'. A new data point, represented by a green circle with a question mark inside, is located in the center. A dashed green circle highlights the five nearest neighbors to this new point: three 'A's and two 'B's. This visualizes how the algorithm identifies the closest neighbors to a new, unlabeled data point to predict its class.

Diagram illustrating the K-Nearest Neighbour (k-NN) algorithm. A green circle with a question mark inside represents a new data point. It is surrounded by several data points: three red squares labeled 'A' and five blue circles labeled 'B'. A dashed green circle highlights the five nearest neighbors (three 'A's and two 'B's') to the new data point.

{21}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-79e1709a7317ead45379cbb8ff3ba802_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram illustrating the K-Nearest Neighbour (k-NN) algorithm.
<!-- /IMAGE_DESCRIPTION -->
### Algoritmo k-NN

- Algoritmo baseado em memória (Lazy)
  - Etapa de Treinamento:
    - **Não gera modelo:** apenas memorização dos dados rotulados
  - Etapa de Generalização:
    - Classifica um novo dado levando em consideração os k vizinhos mais próximos.
    - Usa uma medida de distância para calcular a proximidade dos dados vizinhos (distância euclidiana é bem usual).
    - Cada vizinho k próximo ao dado vota em uma classe.
    - A classe mais votada passa a ser a do novo dado.

{22}------------------------------------------------
### Algoritmo k-NN

Inicialização

Preparar o conjunto de dados (treinamento e teste)

Informar o valor de k

Para cada nova amostra do conjunto de teste faça

{

Calcular a distância para todas as amostras do conjunto de treinamento

Determinar o conjunto das k amostras mais próximas

Determinar o rótulo mais representativo entre os k vizinhos

}

retornar o conjunto de teste rotulado

$$D(Q, C) = \sqrt{\sum_{i=1}^n (q_i - c_i)^2}$$

A 2D scatter plot illustrating the k-Nearest Neighbors (k-NN) algorithm. The plot has a grid from 1 to 10 on both axes. Blue circles represent training samples, and red squares represent test samples. A purple diamond at approximately (5.5, 7.5) represents a query point Q. Concentric circles around Q indicate distance levels. Dotted lines connect Q to its four nearest blue training samples. A green arrow points from Q to the nearest red test sample at (6, 8.5), indicating the classification result.

{23}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-3b7c13851b2efcae74f526646918fb49_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A 2D scatter plot illustrating the k-Nearest Neighbors (k-NN) algorithm.
<!-- /IMAGE_DESCRIPTION -->
### Algoritmo k-NN

Exemplo:

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

- Aplicar o algoritmo para  $k=3$
- Usar distância de Manhattan (para simplificar o cálculo)

Dados

The scatter plot displays data points on a 2D grid with axes ranging from 0 to 10. The x-axis is labeled 'Atributo1' and the y-axis is labeled 'Atributo2'. Class A points (blue circles) are located at (5, 9), (7, 9), (8, 9), and (9, 8). Class B points (green circles) are located at (1, 3), (2, 3), (2, 5), (4, 4), and (2, 5). An unknown point (red circle with a question mark) is located at (5, 2).

| Classe | Atributo1 | Atributo2 |
|--------|-----------|-----------|
| A      | 5         | 9         |
| A      | 7         | 9         |
| A      | 8         | 9         |
| A      | 9         | 8         |
| B      | 1         | 3         |
| B      | 2         | 3         |
| B      | 2         | 5         |
| B      | 4         | 4         |
| ?      | 5         | 2         |

Scatter plot showing data points for classes A and B on a 2D grid. Class A points are blue circles, Class B points are green circles, and an unknown point is a red circle with a question mark.

{24}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-06ccd604e7eac77c7a5a323b6a913f15_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Scatter plot showing data points for classes A and B on a 2D grid.
<!-- /IMAGE_DESCRIPTION -->
### Algoritmo k-NN

Exemplo:

| ID | Atributo1 | Atributo2 | Classe |  | Amostra,DadoNovo | Distancia     | Valor Distância |
|----|-----------|-----------|--------|--|------------------|---------------|-----------------|
| 1  | 5         | 9         | A      |  | 1,9              | $ 5-5 + 9-2 $ | 7               |
| 2  | 7         | 9         | A      |  | 2,9              | $ 7-5 + 9-2 $ | 9               |
| 3  | 8         | 9         | A      |  | 3,9              | $ 8-5 + 9-2 $ | 10              |
| 4  | 9         | 8         | A      |  | 4,9              | $ 9-5 + 8-2 $ | 10              |
| 5  | 2         | 5         | B      |  | 5,9              | $ 2-5 + 5-2 $ | 6               |
| 6  | 4         | 4         | B      |  | 6,9              | $ 4-5 + 4-2 $ | 3               |
| 7  | 1         | 3         | B      |  | 7,9              | $ 1-5 + 3-2 $ | 5               |
| 8  | 2         | 3         | B      |  | 8,9              | $ 2-5 + 3-2 $ | 4               |
| 9  | 5         | 2         | ?      |  |                  |               |                 |

- Aplicar o algoritmo para  $k=3$
- Usar distância de Manhattan (para simplificar o cálculo)

{25}------------------------------------------------
### Algoritmo k-NN

Exemplo:

| ID | Atributo1 | Atributo2 | Classe     |  | Amostra,DadoNovo | Distancia     | Valor Distância |
|----|-----------|-----------|------------|--|------------------|---------------|-----------------|
| 1  | 5         | 9         | A          |  | 1,9              | $ 5-5 + 9-2 $ | 7               |
| 2  | 7         | 9         | A          |  | 2,9              | $ 7-5 + 9-2 $ | 9               |
| 3  | 8         | 9         | A          |  | 3,9              | $ 8-5 + 9-2 $ | 10              |
| 4  | 9         | 8         | A          |  | 4,9              | $ 9-5 + 8-2 $ | 10              |
| 5  | 2         | 5         | B          |  | 5,9              | $ 2-5 + 5-2 $ | 6               |
| 6  | 4         | 4         | B          |  | 6,9              | $ 4-5 + 4-2 $ | 3               |
| 7  | 1         | 3         | B          |  | 7,9              | $ 1-5 + 3-2 $ | 5               |
| 8  | 2         | 3         | B          |  | 8,9              | $ 2-5 + 3-2 $ | 4               |
| 9  | 5         | 2         | ? <b>B</b> |  |                  |               |                 |

B é classe predominante dos 3 vizinhos mais próximos

- Aplicar o algoritmo para  $k=3$
- Usar distância de Manhattan (para simplificar o cálculo)

{26}------------------------------------------------
### Algoritmo k-NN
#### - **Aspectos Positivos**

- Treinamento é simples (apenas armazenamento dos objetos rotulados);
- Constrói aproximações locais da função objetivo, pois são diferentes para cada objeto novo que foi classificado;
- Aplicável mesmo em problemas complexos;
- Incremental (quando novas amostras de treinamento estão disponíveis, basta memorizá-las).

{27}------------------------------------------------
### Algoritmo k-NN
#### - **Aspectos Negativos**

- Não gera um modelo
- Dependente da medida de distância (importante normalizar os dados)
- Predição pode ser custosa para muito objetos
- Alta dimensionalidade dos atributos afeta negativamente os algoritmos baseados em distância (quanto maior o número de atributos mais a distância do mais próximo aproxima-se do mais distante).

{28}------------------------------------------------
## Referências

Este material foi construído com base no material sobre DataMining dos professores Eamonn Keogh(University of California), Rodrigues Barros, Duncan e Renata de Paris e também nos capítulos:

- 4 - Inteligência Artificial: Uma abordagem de Aprendizagem de Máquina: Facelli e outros.
- 18 do livro Artificial Intelligence a Modern Approach: Russel & Norvig

<!-- IMAGE_DESCRIPTION_ORPHANS -->
## Imagens Curadas

Descrições preservadas para imagens detectadas no documento, mas sem referência markdown compatível no corpo principal.

<!-- IMAGE_DESCRIPTION: datalab-08a82c22d89d6b027ff69762ad096586_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A crystal ball on a wooden stand with a torn paper effect overlay.
<!-- /IMAGE_DESCRIPTION -->
<!-- /IMAGE_DESCRIPTION_ORPHANS -->
