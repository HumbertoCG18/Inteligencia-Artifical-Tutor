<!-- EXEC_SUMMARY_START -->
## Sumário
> *Leia antes de varrer o arquivo. Vá direto à seção relevante para a pergunta do aluno.*

- **Roteiro**
- **Subáreas da Inteligência Artificial**
- **Aprendizado Supervisionado**
  - Aprendizado Supervisionado
  - Aprendizado Supervisionado
  - Aprendizado Supervisionado
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
  - Classificação
  - Classificação
  - Classificação
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

# Aprendizado SupervisionadoParte 1

Classificação com k-NN

Profa Silvia Moraes

An abstract image showing a series of horizontal, glowing lines in various colors (red, orange, yellow, green, blue, purple) that appear to be data streams or signals. The lines are slightly blurred and have a sense of motion, suggesting a high-tech or digital theme.

Abstract image of colorful data streams.

An abstract image featuring a glowing, neon-like outline of a human brain. The brain is rendered in shades of purple and blue, with bright white and blue dots representing nodes or connections. The background is dark blue with faint, concentric hexagonal patterns, suggesting a digital or cyber environment.

Abstract image of a glowing brain.

{1}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-64662465bba247703fdec49c8f3309f9_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Abstract image of colorful data streams.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-5fb340ad68b0c71df0b56698b137e35b_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Abstract image of a glowing brain.
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

**Inteligência Artificial (IA)**

Raciocínio Automatizado

Robótica

IA Explicável

Visão Computacional

Diagram showing the subareas of Artificial Intelligence (IA) centered around a circular graphic. The central circle contains the text 'Inteligência Artificial (IA)'. Surrounding this are several subareas: Aprendizado de Máquina (Machine Learning), Processamento de Linguagem Natural, Visão Computacional, Robótica, Raciocínio Automatizado, and IA Explicável. The Aprendizado de Máquina subarea is further detailed with a list of specific learning types.

{3}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-1b7d539e02a202c2cf2d97698b911447_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram showing the subareas of Artificial Intelligence (IA) centered around a circular graphic.
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

The diagram shows three images with labels: a cat labeled 'Gato', a dog labeled 'Cachorro', and a chicken labeled 'Galinha'. Arrows indicate the flow from input (x) to output (y) for the cat image. A URL 'https://www.pexels.com/' is visible below the cat image.

<https://www.pexels.com/>

**Cachorro**

**Galinha**

**Dataset Anotado**

Diagram illustrating supervised learning with labeled images of a cat, a dog, and a chicken.

{4}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-9e6062272bbe3ddbb7c0606721d64cf0_img.jpg -->
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
| 7,0          | 3,2         | 4,7          | 1,4         | Iris-versicolor |
| 6,4          | 3,2         | 4,5          | 1,5         | Iris-versicolor |
| 6,3          | 3,3         | 6,0          | 2,5         | Iris-virginica  |
| 5,8          | 2,7         | 5,1          | 1,9         | Iris-virginica  |

**Atributo de saída**  
(atributo alvo ou meta)

**Rótulo**  
(Classes)

The image shows three distinct Iris flower species. The left image is a light blue/purple Iris Virginica. The middle image is a dark purple Iris Setosa. The right image is a medium purple Iris Versicolor. Each image has its label below it: 'Iris Virginica', 'Iris Setosa', and 'Iris Versicolor'.

Three images of Iris flowers: Iris Virginica (left), Iris Setosa (middle), and Iris Versicolor (right).

{5}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-764bb8d7c93b090e205d908e1a8cade4_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Three images of Iris flowers: Iris Virginica (left), Iris Setosa (middle), and Iris Versicolor (right).
<!-- /IMAGE_DESCRIPTION -->
### Aprendizado Supervisionado

- O objetivo é encontrar um modelo capaz de mapear os valores de entrada ( $x$ ) nos valores de saída  $y$ .
- Em outras palavras, que aproxime  $f$ , tal que  $f(x) = y$ .
- Supervisão: ajuste usando o erro em relação à saída esperada.

The diagram illustrates the supervised learning process. It starts with a **Dataset Anotado** (Annotated Dataset) on the left, which includes three images: a cat labeled **Gato**, a dog labeled **Cachorro**, and a chicken labeled **Galinha**. An arrow points from this dataset to a green box representing the **Algoritmo de Machine Learning Supervisionado** (Supervised Machine Learning Algorithm). Inside this box is a **Treinamento** (Training) icon, which shows a neural network diagram. Another arrow points from the algorithm box to the final **Modelo** (Model) icon, which also features a neural network diagram.

Diagram illustrating the supervised learning process. On the left, a 'Dataset Anotado' (Annotated Dataset) contains images of a cat (Gato), a dog (Cachorro), and a chicken (Galinha). An arrow points to a green box labeled 'Algoritmo de Machine Learning Supervisionado' (Supervised Machine Learning Algorithm) which contains a 'Treinamento' (Training) icon. Another arrow points to the final 'Modelo' (Model) icon.

{6}------------------------------------------------

Modelo Probabilístico

<!-- IMAGE_DESCRIPTION: datalab-a7d78d22e465dea388b31d0739f9d0cd_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram illustrating the supervised learning process.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-79e1709a7317ead45379cbb8ff3ba802_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram illustrating the k-NN algorithm.
<!-- /IMAGE_DESCRIPTION -->
### Aprendizado Supervisionado

- **Tarefa preditiva:** encontra uma função (modelo) a partir dos dados de treino que possa ser usada para prever um rótulo (classe) ou valor de um novo exemplo.
- Pode ser:
  - **classificação** (rótulos discretos)
  - **regressão** (rótulos contínuos)

{7}------------------------------------------------
### Classificação

The diagram illustrates the classification process. It starts with an input image of a cat, labeled "Imagem sem rótulo" and "Entrada". An arrow points to a green box labeled "Algoritmo de Machine Learning Supervisionado". Below this box is the word "Generalização" and a smaller box labeled "Modelo" containing a neural network icon. An arrow points from the algorithm box to the output "gato (96%)", which is labeled "Predição". The input image has a URL at the bottom: <https://www.pexels.com/>.

Diagram of the classification process

- É o processo de automaticamente atribuir rótulos a dados.
- Pode ser do tipo
  - Binária: possui apenas duas classes
  - Multiclasse: possui mais de duas classes
- Pode atribuir
  - Um único rótulo (single label)
  - Vários rótulos (multi-label)

An image showing a tomato sorting machine. A red label at the bottom of the image reads "Máquina de triagem de tomate".

Image of a tomato sorting machine

{8}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-2ee59e629035d641140e55f4d215b0d7_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of the classification process
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-efca2dce0095c9dc2a68e9af6b2bfd40_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Image of a tomato sorting machine
<!-- /IMAGE_DESCRIPTION -->
### Regressão

- É o processo de automaticamente predizer novos valores y.
- Neste caso, os dados são anotados com valores.

A line graph illustrating regression. The x-axis represents years from 2015 to 2022. The y-axis represents an unlabeled value. Data points are plotted for 2015, 2016, 2017, 2018, 2019, 2020, and 2021. A solid blue line connects these points. A dashed red line extends from the 2021 point to 2022, ending with a red question mark, indicating a prediction for the year 2022.

| Ano  | Valor (aproximado) |
|------|--------------------|
| 2015 | 0.5                |
| 2016 | 0.2                |
| 2017 | 1.5                |
| 2018 | 1.8                |
| 2019 | 0.8                |
| 2020 | 2.2                |
| 2021 | 1.8                |
| 2022 | 2.8 (predição)     |

Line graph showing data points from 2015 to 2021 and a prediction for 2022.

A scatter plot showing training data points (blue dots) and a fitted regression curve (red line). The x-axis ranges from 0 to 100, and the y-axis ranges from -1 to 4. The data points follow a periodic pattern, and the regression curve is a smooth fit to these points. A legend in the top left corner identifies the blue dots as 'training data' and the red line as 'regression'.

| x   | y (training data) |
|-----|-------------------|
| 0   | 0.5               |
| 20  | 1.0               |
| 40  | 0.0               |
| 60  | 1.5               |
| 80  | 3.5               |
| 100 | 3.0               |

Scatter plot with a regression curve.

{9}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-91be14371a97fb5ce9eeb29ae18d07c3_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Line graph showing data points from 2015 to 2021 and a prediction for 2022.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-bedcca5cdf168e3508ef511d94ec514c_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Scatter plot with a regression curve.
<!-- /IMAGE_DESCRIPTION -->
### Regressão

The diagram illustrates the supervised machine learning process for regression. On the left, a **Dataset Anotado** (Annotated Dataset) is shown with the following data points:

| $x$ | $f(x)$ |
|-----|--------|
| 1   | 1      |
| 2   | 4      |
| 3   | 9      |
| 4   | 16     |
| 5   | 25     |

An arrow points from the dataset to a green box labeled **Algoritmo de Machine Learning Supervisionado** (Supervised Machine Learning Algorithm). Inside this box is a smaller white box labeled **Treinamento** (Training) which contains a small neural network icon. Above the input  $x$  and output  $f(x)$  in this box is a red question mark. An arrow points from this algorithm box to another green box labeled **Modelo** (Model). This box contains a neural network icon and shows the input  $x$  and output  $f(x)$ , with a red  $x^2$  above the output, indicating the learned function.

Diagram showing the supervised machine learning algorithm for regression using a small dataset.

Dataset Anotado

The figure shows a scatter plot of **training data** (blue dots) and a **regression** line (red curve) over a range of  $x$  values from 0 to 100. The y-axis ranges from -1 to 4. To the right of the plot, the number **6** is labeled as **Entrada** (Input). An arrow points from this input to a green box labeled **Algoritmo de Machine Learning Supervisionado** (Supervised Machine Learning Algorithm). Inside this box is a smaller white box labeled **Generalização** (Generalization) which contains a neural network icon. Above the input  $x$  and output  $f(x)$  in this box is a red  $x^2$ . An arrow points from this algorithm box to another green box labeled **Modelo** (Model), which contains a neural network icon and shows the input  $x$  and output  $f(x)$ , with a red  $x^2$  above the output.

Figure showing a scatter plot of training data and a regression line, followed by a diagram of the supervised machine learning algorithm for generalization.

{10}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-f4fdd410cdb84df81274da55721e56fb_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram showing the supervised machine learning algorithm for regression using a small dataset.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-f519a5be118c846f631c992412353fb9_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Figure showing a scatter plot of training data and a regression line, followed by a diagram of the supervised machine learning algorithm for generalization.
<!-- /IMAGE_DESCRIPTION -->
### Classificação

The diagram illustrates a classification process. On the left, a stack of documents, with the top one labeled "Acme Article", represents the input data. Three arrows originate from this stack and point to three distinct stacks of documents on the right. These stacks are labeled "Technology", "Sports", and "Entertainment", representing the output categories or classes. The "Technology" stack is cyan, the "Sports" stack is purple, and the "Entertainment" stack is blue.

Diagram illustrating text classification. A stack of documents labeled 'Acme Article' is shown on the left. Three arrows point from this stack to three separate stacks of documents on the right, labeled 'Technology', 'Sports', and 'Entertainment'.

{11}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-5b4e774d63e0e0ed73801a9247755e5f_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram illustrating text classification.
<!-- /IMAGE_DESCRIPTION -->
### Classificação

A close-up photograph of a brown and tan striped grasshopper, likely a species of Acrididae, resting on a rough, greyish-brown rocky or gravelly surface. The insect's body is elongated, and its legs are visible, adapted for jumping.

A brown and tan striped grasshopper on a rocky surface.

A close-up photograph of a bright green grasshopper, possibly a katydid, resting on a smooth, light pinkish surface. The insect's wings are folded over its back, and its long, thin legs are extended.

A bright green grasshopper on a pinkish surface.

Como classificar Gafanhotos ?

{12}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-ec0158057f8ccaf74edba16682ec5444_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A brown and tan striped grasshopper on a rocky surface.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-e3b8510f6a2194e250205ab7bc38076d_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A bright green grasshopper on a pinkish surface.
<!-- /IMAGE_DESCRIPTION -->
### Classificação

Se os dados desses insetos fossem estruturados, que atributos/características seriam mais importantes e significativos para a classificação?

Cor: {Verde, Marrom, Cinza, Outra}

Tem asas?

Comprimento do abdômen

Comprimento do Tórax

Comprimento das antenas

Tamanho da mandíbula

Diâmetro dos orifícios de respiração

Comprimento das pernas

O diagrama mostra um inseto (um gafanhoto) com várias partes do corpo destacadas por linhas e setas, indicando atributos para classificação. As partes destacadas são: o abdômen, o tórax, as antenas, a mandíbula, os orifícios de respiração e as pernas. Acima do inseto, há duas perguntas: 'Cor: {Verde, Marrom, Cinza, Outra}' e 'Tem asas?'.

Diagrama de um inseto com atributos de classificação

{13}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-bb6d33498937738ff5dac8d91c9ebaad_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de um inseto com atributos de classificação
<!-- /IMAGE_DESCRIPTION -->
### Classificação

Se os dados desses insetos fossem estruturados, que atributos/características seriam mais importantes e significativos para a classificação?

Cor: {Verde, Marrom, Cinza, Outra}

Tem asas?

Diagrama de um inseto com vários atributos destacados para classificação. Os atributos são: Comprimento do abdômen, Comprimento do Tórax, Comprimento das antenas, Tamanho da mandíbula, Comprimento das pernas e Diâmetro dos orifícios de respiração. Os atributos 'Comprimento do abdômen' e 'Comprimento das antenas' estão destacados com caixas vermelhas.

Comprimento do abdômen

Comprimento do Tórax

Comprimento das antenas

Tamanho da mandíbula

Comprimento das pernas

Diâmetro dos orifícios de respiração

Diagrama de um inseto com atributos destacados para classificação.

{14}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-7832324609ad3cc688064e0341612b32_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de um inseto com atributos destacados para classificação.
<!-- /IMAGE_DESCRIPTION -->
### Classificação

Diagrama de um gafanhoto com as seguintes características rotuladas:

- Cor: {Verde, Marrom, Cinza, Outra}
- Tem asas?
- Comprimento do abdômen
- Comprimento do Tórax
- Comprimento das antenas
- Tamanho da mandíbula
- Diâmetro dos orifícios de respiração
- Comprimento das pernas

Diagrama de um gafanhoto com labels de características físicas.

Se tivermos um **conjunto de dados anotados com as classes dos gafanhotos**, poderemos aplicar um algoritmo de classificação para predizer a classe de novos insetos desse tipo.

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
> **[Descrição de imagem]** Diagrama de um gafanhoto com labels de características físicas.
<!-- /IMAGE_DESCRIPTION -->
### Classificação

A scatter plot illustrating the relationship between the length of the abdomen (x-axis) and the length of the antennae (y-axis) for two classes of insects. The x-axis is labeled 'Comprimento do abdômen' and the y-axis is labeled 'Comprimento das antenas', both ranging from 1 to 10. The plot shows two distinct clusters of data points: blue circles (Class 1) and red squares (Class 2). A purple diamond represents a new data point at approximately (5.1, 7.0). An arrow points from a sketch of an insect to this new data point.

| Comprimento do abdômen | Comprimento das antenas | Classe     |
|------------------------|-------------------------|------------|
| 1.0                    | 1.2                     | 1          |
| 1.0                    | 4.8                     | 1          |
| 1.5                    | 3.5                     | 1          |
| 2.8                    | 5.6                     | 1          |
| 3.0                    | 2.0                     | 1          |
| 5.5                    | 8.5                     | 2          |
| 6.5                    | 6.8                     | 2          |
| 8.0                    | 9.2                     | 2          |
| 8.2                    | 6.8                     | 2          |
| 8.2                    | 4.8                     | 2          |
| 5.1                    | 7.0                     | Novo ponto |

Scatter plot showing the relationship between antenna length and abdomen length for two classes of insects. A new data point is highlighted with a purple diamond.

Qual a classe de um inseto com comprimento 5,1 de abdômen e 7,0 mm de antenas?

{16}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-b05fbb6a015ea153c1e25245772b1a1b_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Scatter plot showing the relationship between antenna length and abdomen length for two classes of insects.
<!-- /IMAGE_DESCRIPTION -->
### Classificação
#### Classificador Linear Simples

Se o exemplo desconhecido está acima da linha  
Então a classe é **Esperança**  
Senão a classe é **Gafanhoto**

| X   | Y   | Class                    |
|-----|-----|--------------------------|
| 1   | 1   | Blue Circle              |
| 1   | 3.5 | Blue Circle              |
| 1   | 4.8 | Blue Circle              |
| 3   | 2   | Blue Circle              |
| 3   | 5.6 | Blue Circle              |
| 5.5 | 7.1 | Purple Diamond (Unknown) |
| 5.8 | 8.6 | Red Square               |
| 6.8 | 6.8 | Red Square               |
| 8.2 | 4.8 | Red Square               |
| 8.2 | 9.4 | Red Square               |
| 8.5 | 6.8 | Red Square               |

A scatter plot illustrating a simple linear classifier. The plot shows a grid from 1 to 10 on both axes. A thick orange diagonal line runs from (1, 10) to (8, 0). Blue circles represent one class, and red squares with diagonal stripes represent another. A purple diamond represents an unknown example. The line separates the two classes, with the blue circles mostly below the line and the red squares mostly above it. The purple diamond is located above the line, indicating it should be classified as 'Esperança'.

{17}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-fed39b841ae2dce01088b84bfc1e2789_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A scatter plot illustrating a simple linear classifier.
<!-- /IMAGE_DESCRIPTION -->
### Classificação
#### Classificador Linear

Pode ser usado para mais dimensões.

Nesse caso, a divisão não será por uma reta (linha) mas por um hiperplano .

The figure consists of two side-by-side 3D plots. The left plot shows a 3D coordinate system with a grid on the base plane. It contains two sets of spheres: orange spheres and grey spheres. The orange spheres are clustered on the left side of the grid, and the grey spheres are clustered on the right side. The right plot shows the same 3D coordinate system, but with a yellow diagonal plane (hyperplane) that separates the orange spheres from the grey spheres. The orange spheres are now on one side of the plane, and the grey spheres are on the other side, demonstrating a linear classification.

Two 3D plots illustrating a linear classifier. The left plot shows a 3D coordinate system with a grid of orange and grey spheres. The right plot shows the same spheres separated by a yellow diagonal plane, representing a hyperplane.

{18}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-ef25c3cf1fdb334fc8679e85ab5265ca_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Two 3D plots illustrating a linear classifier.
<!-- /IMAGE_DESCRIPTION -->
### Classificação
#### Classificador Linear

Limitação: resolve apenas problemas cujas classes são linearmente separáveis.

A scatter plot on a yellow background with a grid. The x-axis and y-axis both range from 1 to 10. There are two classes of data points: blue circles and red squares with a diagonal line pattern. An orange diagonal line with a positive slope separates the two classes perfectly. All red squares are above and to the left of the line, and all blue circles are below and to the right of the line.

Scatter plot showing perfect linear separation between two classes.

Classificação Perfeita

A scatter plot on a light blue background with a grid. The x-axis and y-axis both range from 10 to 100. There are two classes of data points: blue circles and red squares with a diagonal line pattern. An orange diagonal line with a negative slope separates the two classes very well. Most red squares are above and to the right of the line, and most blue circles are below and to the left of the line, with only a few outliers on the wrong side of the line.

Scatter plot showing very good linear separation between two classes.

Classificação Muito Boa

A scatter plot on a light green background with a grid. The x-axis ranges from 1 to 10 and the y-axis ranges from 1 to 10. There are two classes of data points: blue circles and red squares with a diagonal line pattern. An orange diagonal line with a positive slope is drawn through the data, but it fails to separate the two classes. Both blue circles and red squares are present on both sides of the line, indicating that the data is not linearly separable.

Scatter plot showing useless linear separation between two classes.

Classificação Inútil

{19}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-1c427123350e0e73e2a109b79069314b_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Scatter plot showing perfect linear separation between two classes.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-93587f920736a2fdcefeba94b29f302a_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Scatter plot showing very good linear separation between two classes.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-8a597e344d10e36bbb2f243f6c4e74c6_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Scatter plot showing useless linear separation between two classes.
<!-- /IMAGE_DESCRIPTION -->
### Classificação
#### Classificador Linear

Exemplo: **Planta Iris**

- 150 amostras: Dataset Balanceado
  - 50 Iris Setosa,
  - 50 Iris Virginica e
  - 50 Iris Versicolor
- Podemos generalizar o classificador para N classes, encontrando N-1 hiperplanos:
  1. O primeiro hiperplano separa a Setosa das outras duas Versicolor/Virginica
  2. O segundo hiperplano separa Versicolor de Virginica

A scatter plot illustrating the Iris dataset with three classes: Setosa (blue plus signs), Versicolor (green dots), and Virginica (red crosses). The plot shows two orange lines acting as linear classifiers. The first line separates the Setosa class from the other two. The second line separates the Versicolor class from the Virginica class. The axes are unlabeled but show relative positions of the data points.

Scatter plot of the Iris dataset showing three classes: Setosa (blue plus), Versicolor (green dots), and Virginica (red crosses). Two orange lines represent linear classifiers separating the classes.

{20}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-f85bf99d372e735d228361bf4d3cf7e6_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Scatter plot of the Iris dataset showing three classes: Setosa (blue plus), Versicolor (green dots), and Virginica (red crosses).
<!-- /IMAGE_DESCRIPTION -->
### Algoritmo k-NN

**K- Nearest Neighbour :**  
algoritmo dos k vizinhos  
mais próximos.

Considera os objetos mais  
próximos com  
características semelhantes  
para predizer a classe de  
um novo dado.

The diagram illustrates the k-Nearest Neighbors (k-NN) algorithm. A central green dot with a question mark represents the new data point. A dashed green circle indicates the neighborhood. Inside the circle are three red squares labeled 'A' and three blue circles labeled 'B'. Outside the circle are two red squares labeled 'A' and two blue circles labeled 'B'.

Diagram illustrating the k-NN algorithm. A central green dot with a question mark represents the new data point. A dashed green circle indicates the neighborhood. Inside the circle are three red squares labeled 'A' and three blue circles labeled 'B'. Outside the circle are two red squares labeled 'A' and two blue circles labeled 'B'.

{21}------------------------------------------------
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

A scatter plot on a yellow grid background illustrating the k-NN algorithm. A central purple diamond represents a query point Q. Concentric circles around it indicate increasing distances. Several blue circles (training points) and red squares (test points) are scattered on the grid. Dashed lines connect the query point to its k nearest neighbors, which are a mix of blue circles and red squares. The axes are labeled from 1 to 10.

{23}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-3b7c13851b2efcae74f526646918fb49_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A scatter plot on a yellow grid background illustrating the k-NN algorithm.
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

| Point | Atributo1 (x) | Atributo2 (y) | Class |
|-------|---------------|---------------|-------|
| A1    | 5             | 9             | A     |
| A2    | 7             | 9             | A     |
| A3    | 8             | 9             | A     |
| A4    | 9             | 8             | A     |
| B1    | 2             | 5             | B     |
| B2    | 4             | 4             | B     |
| B3    | 1             | 3             | B     |
| B4    | 2             | 3             | B     |
| ?     | 5             | 2             | ?     |

Scatter plot titled 'Dados' showing data points A (blue), B (green), and a query point ? (red) on a 2D grid. The x-axis and y-axis both range from 0 to 10. Points A are at (5,9), (7,9), (8,9), and (9,8). Points B are at (2,5), (4,4), (1,3), and (2,3). The query point ? is at (5,2).

{24}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-06ccd604e7eac77c7a5a323b6a913f15_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Scatter plot titled 'Dados' showing data points A (blue), B (green), and a query point ?
<!-- /IMAGE_DESCRIPTION -->
### Algoritmo k-NN

Exemplo:

| ID | Atributo1 | Atributo2 | Classe | Amostra, DadoNovo | Distancia       | Valor Distância |
|----|-----------|-----------|--------|-------------------|-----------------|-----------------|
| 1  | 5         | 9         | A      | 1,9               | $ 5-5  +  9-2 $ | 7               |
| 2  | 7         | 9         | A      | 2,9               | $ 7-5  +  9-2 $ | 9               |
| 3  | 8         | 9         | A      | 3,9               | $ 8-5  +  9-2 $ | 10              |
| 4  | 9         | 8         | A      | 4,9               | $ 9-5  +  8-2 $ | 10              |
| 5  | 2         | 5         | B      | 5,9               | $ 2-5  +  5-2 $ | 6               |
| 6  | 4         | 4         | B      | 6,9               | $ 4-5  +  4-2 $ | 3               |
| 7  | 1         | 3         | B      | 7,9               | $ 1-5  +  3-2 $ | 5               |
| 8  | 2         | 3         | B      | 8,9               | $ 2-5  +  3-2 $ | 4               |
| 9  | 5         | 2         | ?      |                   |                 |                 |

- Aplicar o algoritmo para  $k=3$
- Usar distância de Manhattan (para simplificar o cálculo)

{25}------------------------------------------------
### Algoritmo k-NN

Exemplo:

| ID | Atributo1 | Atributo2 | Classe | Amostra, DadoNovo | Distancia       | Valor Distância |
|----|-----------|-----------|--------|-------------------|-----------------|-----------------|
| 1  | 5         | 9         | A      | 1,9               | $ 5-5  +  9-2 $ | 7               |
| 2  | 7         | 9         | A      | 2,9               | $ 7-5  +  9-2 $ | 9               |
| 3  | 8         | 9         | A      | 3,9               | $ 8-5  +  9-2 $ | 10              |
| 4  | 9         | 8         | A      | 4,9               | $ 9-5  +  8-2 $ | 10              |
| 5  | 2         | 5         | B      | 5,9               | $ 2-5  +  5-2 $ | 6               |
| 6  | 4         | 4         | B      | 6,9               | $ 4-5  +  4-2 $ | 3               |
| 7  | 1         | 3         | B      | 7,9               | $ 1-5  +  3-2 $ | 5               |
| 8  | 2         | 3         | B      | 8,9               | $ 2-5  +  3-2 $ | 4               |
| 9  | 5         | 2         | ? B    |                   |                 |                 |

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
- Predição pode ser custosa para muitos objetos
- Alta dimensionalidade dos atributos afeta negativamente os algoritmos baseados em distância (quanto maior o número de atributos mais a distância do mais próximo aproxima-se do mais distante).

{28}------------------------------------------------
## Referências

Este material foi construído com base no material sobre DataMining dos professores Eamonn Keogh(University of California), Rodrigos Barros, Duncan e Renata de Paris e também nos capítulos:

- 4 - Inteligência Artificial: Uma abordagem de Aprendizagem de Máquina: Facelli e outros.
- 18 do livro Artificial Intelligence a Modern Approach: Russel & Norvig

<!-- IMAGE_DESCRIPTION_ORPHANS -->
## Imagens Curadas

Descrições preservadas para imagens detectadas no documento, mas sem referência markdown compatível no corpo principal.

<!-- IMAGE_DESCRIPTION: datalab-08a82c22d89d6b027ff69762ad096586_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A crystal ball on a stand, symbolizing a probabilistic model.
<!-- /IMAGE_DESCRIPTION -->
<!-- /IMAGE_DESCRIPTION_ORPHANS -->
