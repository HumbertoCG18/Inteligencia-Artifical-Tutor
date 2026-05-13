<!-- EXEC_SUMMARY_START -->
## Sumário
> *Leia antes de varrer o arquivo. Vá direto à seção relevante para a pergunta do aluno.*

- **Roteiro**
  - A arquitetura de uma rede neural define o tipo de tarefa que ela pode executar.
- **Redes Feed Forward ➔**
- **Redes Recorrentes ↺**
  - Mapa auto-organizável
- **Redes Feed Forward**
- **Redes Feed ForwardRede Perceptron**
- **Redes Feed ForwardRede Perceptron - Topologia**
- **Redes Feed ForwardRede Perceptron - Topologia**
- **Redes Feed ForwardRede Perceptron - Topologia**
  - Redes Feed ForwardRede Perceptron - Topologia
  - Redes Feed ForwardRede Perceptron - Topologia
  - Redes Feed Forward Rede Perceptron - Topologia
  - Redes Feed Forward Rede Perceptron - Topologia
  - Redes Feed Forward Rede Perceptron - Topologia
  - Redes Feed Forward Rede Perceptron - Topologia
  - Redes Feed Forward Rede Perceptron - Topologia
- **Planta Iris**
- **Planta Iris**
- **Planta Iris**
- **Planta Iris**
- **Topologia para 2 classes Classificador Binario Neural**
  - Exemplo 2 – Dados desestruturados
  - Reconhecedor de Caracteres
  - Reconhecedor de Caracteres
  - Exemplo 3 – Dados desestruturados
  - Classificador de sentenças
  - Classificador de sentenças
  - Classificador de sentenças
- **Etapas Básicas de Construção de uma Rede Neural**
  - Rede Perceptron
  - Rede Perceptron
  - Rede Perceptron
  - Rede Perceptron
  - Rede Perceptron
  - Treinamento de Rede Neuronais
  - Treinamento de Redes Neuronais
- **Rede Perceptron - Algoritmo de Treinamento**
  - Rede Perceptron – Limitações
- **Tabela OR**
  - Rede Perceptron – Limitações
- **Tabela XOR**
  - Simulando uma Rede Perceptron
  - Simulando uma Rede Perceptron
  - Simulando uma Rede Perceptron
  - Simulando uma Rede Perceptron
  - Simulando uma Rede Perceptron
  - Simulando uma Rede Perceptron
  - Simulando uma Rede Perceptron
  - Simulando uma Rede Perceptron
  - Simulando uma Rede Perceptron
  - Simulando uma Rede Perceptron
  - Simulando uma Rede Perceptron
  - Simulando uma Rede Perceptron
  - Simulando uma Rede Perceptron
  - Simulando uma Rede Perceptron
  - Simulando uma Rede Perceptron Fase de Generalização
  - Simulando uma Rede Perceptron Fase de Generalização
  - Simulando uma Rede Perceptron Fase de Generalização
- **Exercicios**
- **Exercicios**
- **Exercicios**
  - Topologia para 2 classes Classificador Binario Neural
- **Exercicios**
- **Imagens Curadas**

<!-- EXEC_SUMMARY_END -->
<!-- DATALAB_CHUNK 1: pages 1-20 -->

{0}------------------------------------------------

# Green horizontal barRede Neural Perceptron

Silvia Moraes

An abstract graphic on the right side of the slide, featuring a network of glowing blue lines and dots on a dark background, resembling a wireframe model or a neural network structure.

Abstract blue wireframe graphic

{1}------------------------------------------------
## Roteiro

- Arquiteturas de Rede
- Redes FeedForward
- Revisitando a estrutura de um **neurônio** artificial
- Algoritmo de Aprendizado de uma rede perceptron
- Passo a passo de execução
- Limitação da rede

A glowing blue neural network diagram. It features several interconnected nodes, each represented by a cluster of small, luminous blue spheres. These nodes are connected by thick, glowing blue lines that represent the pathways of information flow. The background is a solid, deep black, which makes the vibrant blue colors of the network stand out. The overall effect is one of a complex, dynamic, and futuristic system.

A glowing blue neural network diagram.

{2}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-61972112770d9c8fb00883057954f885_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A glowing blue neural network diagram.
<!-- /IMAGE_DESCRIPTION -->
### A arquitetura de uma rede neural define o tipo de tarefa que ela pode executar.

<!-- IMAGE_DESCRIPTION: datalab-2df09d249c38abee55dbf0526dd6da0a_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de rede neural com camadas
<!-- /IMAGE_DESCRIPTION -->
## Redes Feed Forward ➔

Rede alimentadas para Frente

Diagramas de redes Feed Forward. À esquerda, um Perceptron com duas entradas ( $x_1$  e  $x_2$ ) e um único nó de saída laranja. À direita, um MultiLayer Perceptron com duas entradas ( $x_1$  e  $x_2$ ), duas camadas intermediárias (uma com dois nós verdes e outra com um nó verde) e um nó de saída laranja.

Diagramas de Perceptron e MultiLayer Perceptron

Perceptron

MultiLayer Perceptron

Diagrama de uma rede neural com camadas. À esquerda, a 'camada de entrada' com dois nós cinza. À direita, a 'camada de saída' com um nó cinza. Entre elas, duas 'camadas intermediárias' com nós vermelhos. Linhas representando as 'conexões' ligam os nós entre camadas adjacentes.

Diagrama de rede neural com camadas

<https://sites.icmc.usp.br/andre/research/neural/>

<!-- IMAGE_DESCRIPTION: datalab-69edc2887e907309499ac95b47ab6905_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagramas de Perceptron e MultiLayer Perceptron
<!-- /IMAGE_DESCRIPTION -->
## Redes Recorrentes ↺

Rede com retroalimentacao

Diagrama de uma Rede Recorrente. Possui três camadas: uma de entrada com três nós amarelos ( $x_1, x_2, x_3$ ), uma camada intermediária com seis nós azuis e uma camada de saída com três nós laranjas. Há conexões completas entre camadas adjacentes e também conexões de retroalimentação (loops) nos nós da camada intermediária.

Diagrama de Rede Recorrente

<!-- IMAGE_DESCRIPTION: datalab-aec7150315249ac202a63cc0e32323b8_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de Rede Recorrente
<!-- /IMAGE_DESCRIPTION -->
### Mapa auto-organizável

Redes de Kohonen

Diagrama de um Mapa auto-organizável (Rede de Kohonen). À esquerda, duas entradas ( $x_1$  e  $x_2$ ) são mostradas. À direita, há uma rede de 12 nós verdes organizados em uma matriz de 3 colunas por 4 linhas. Cada entrada está conectada a todos os nós da rede.

Diagrama de Mapa auto-organizável

Visualização de dados em um mapa auto-organizável. Uma rede de nós (representada por uma malha quadrada) é mostrada no centro. Dados de entrada (pontos vermelhos) são distribuídos ao redor da rede, e a rede se organiza para representar esses dados de forma não supervisionada.

Visualização de dados em um mapa auto-organizável

[https://pt.wikipedia.org/wiki/Mapas\\_de\\_Kohonen](https://pt.wikipedia.org/wiki/Mapas_de_Kohonen)

{3}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-b6e90f8ae3109449704b9b5c7951f631_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de Mapa auto-organizável
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-ed14725db41dc9fb8e9460b1478f8366_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Visualização de dados em um mapa auto-organizável
<!-- /IMAGE_DESCRIPTION -->
## Redes Feed Forward

Tarefas Supervisionadas: **classificação e regressão**

A diagram of a single neuron (Perceptron). It has two input nodes on the left, labeled  $x_1$  and  $x_2$ , both connected to a single output node on the right, which is colored orange.

Diagram of a Perceptron

Perceptron

A diagram of a MultiLayer Perceptron. It has two input nodes on the left, labeled  $x_1$  and  $x_2$ . These inputs are connected to two hidden nodes (colored green). Both hidden nodes are then connected to a single output node on the right (colored orange).

Diagram of a MultiLayer Perceptron

MultiLayer Perceptron

A diagram illustrating a feed-forward neural network architecture. On the left, two input images (a dog and a cat) are shown. These are connected to an 'INPUT' layer consisting of three purple nodes. This layer is connected to a 'HIDDEN' layer consisting of four purple nodes. The hidden layer is then connected to an 'OUTPUT' layer consisting of two purple nodes. Arrows indicate the forward flow of information from left to right.

Diagram of a Feed Forward Neural Network

<https://sites.icmc.usp.br/andre/research/neural/>

---

Propagação: fluxo do sinal sempre para frente →

{4}------------------------------------------------

A diagram of a single neuron, represented by an orange circle. Two input lines, labeled

 $x_1$ 

and

 $x_2$ 

, enter the neuron from the left. A single output line extends from the right side of the neuron.

Diagram of a single neuron (Perceptron) with two inputs, x1 and x2, connected to a single output node.

<!-- IMAGE_DESCRIPTION: datalab-d62e2e2281009c16f4ee61660e716cd9_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a MultiLayer Perceptron
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-12a6537c92844d5b393104c02e8dfc2f_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a Feed Forward Neural Network
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-5801c19431e76330430e92a598cc7a16_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single-layer perceptron network.
<!-- /IMAGE_DESCRIPTION -->
## Redes Feed ForwardRede Perceptron

- Perceptron é uma rede **muito simples**.
- Quando constituída de apenas um neurônio é chamada de perceptron elementar.
- Possui apenas **uma camada de neurônios**.
- Pode ter várias entradas e várias saídas.
- Trabalha com valores discretos e contínuos tanto para as entradas quanto para as saídas.
- Historicamente quando há valores contínuos, as redes com essas características eram chamadas de Adaline.
- Limitação: só consegue resolver problemas linearmente separáveis.

{5}------------------------------------------------

A diagram of a single neuron. It consists of an orange circular body. Two input lines, labeled

 $x_1$ 

and

 $x_2$ 

, enter the circle from the left. A single output line extends from the right side of the circle.

Diagram of a single neuron with two inputs, x1 and x2, and an orange circular body.

<!-- IMAGE_DESCRIPTION: datalab-9e6062272bbe3ddbb7c0606721d64cf0_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a Perceptron
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-547f726730e589392f239257a833ede3_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single neuron with two inputs, x1 and x2, and an orange circular body.
<!-- /IMAGE_DESCRIPTION -->
## Redes Feed ForwardRede Perceptron - Topologia

Como definir a quantidade valores de entrada, de camadas e neurônios da rede?

- Como esta rede tem apenas 1 camada, precisamos apenas definir a **os atributos de entrada e quantidade de neurônios** desta única camada.
- Normalmente, define-se um **neurônio para cada classe esperada**.
- Para entender, vamos ver um exemplo...

{6}------------------------------------------------

Diagram of a single neuron with two inputs, x1 and x2, and an orange circular output node.

<!-- IMAGE_DESCRIPTION: datalab-fc46871d72c65d3381d9201646d23439_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single neuron with two inputs, x1 and x2, and an orange circular output node.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-3121ebddccf183ca63bb9781be440a7e_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single neuron with two inputs, x1 and x2, and an orange circular output node.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-ebff22fb5dd6f50a90e44dca0f82f285_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single neuron with two inputs, x1 and x2, and an orange circular output node.
<!-- /IMAGE_DESCRIPTION -->
## Redes Feed ForwardRede Perceptron - Topologia

| cpf    | nome   | renda | dívida | classificação do cliente |
|--------|--------|-------|--------|--------------------------|
| 111... | João   | 2000  | 1000   | bom                      |
| 222... | Maria  | 3000  | 2000   | mau                      |
| 333... | Pedro  | 1000  | 500    | mau                      |
| 444... | Carlos | 3000  | 1500   | bom                      |

**Entradas:** Quais são atributos podem ser usados como entrada para rede ?

**Saídas :** Em quantas classes do algoritmo deve organizar os clientes?

{7}------------------------------------------------

Diagram of a single neuron with two inputs, x1 and x2, and an orange circular output node.
## Redes Feed ForwardRede Perceptron - Topologia

| cpf    | nome   | renda | dívida | classificação do cliente |
|--------|--------|-------|--------|--------------------------|
| 111... | João   | 2000  | 1000   | bom                      |
| 222... | Maria  | 3000  | 2000   | mau                      |
| 333... | Pedro  | 1000  | 500    | mau                      |
| 444... | Carlos | 3000  | 1500   | bom                      |

2 atributos de entrada

**Entradas:** Quais são atributos podem ser usados como entrada para rede ?

**Saídas :** Em quantas classes do algoritmo deve organizar os clientes?

{8}------------------------------------------------

Diagram of a single neuron with two inputs, x1 and x2, and an orange circular output node.
### Redes Feed ForwardRede Perceptron - Topologia

| cpf    | nome   | renda | dívida | classificação do cliente |
|--------|--------|-------|--------|--------------------------|
| 111... | João   | 2000  | 1000   | bom                      |
| 222... | Maria  | 3000  | 2000   | mau                      |
| 333... | Pedro  | 1000  | 500    | mau                      |
| 444... | Carlos | 3000  | 1500   | bom                      |

2 classes como saída

**Entradas:** Quais são atributos podem ser usados como entrada para rede ?

**Saídas :** Em quantas classes do algoritmo deve organizar os clientes?

{9}------------------------------------------------
#### Lembrando:

Redes neurais **trabalham somente com números**, por isso é comum realizar transformações nos dados.

E funcionam melhor com dados normalizados.

A background image showing vertical columns of glowing blue binary digits (0s and 1s) on a black background, resembling a digital rain effect. The digits are arranged in vertical streams, with some columns showing a continuous flow of 0s and 1s, while others are more sparse. The overall effect is a high-tech, digital aesthetic.

A background image showing vertical columns of glowing blue binary digits (0s and 1s) on a black background, resembling a digital rain effect.

{10}------------------------------------------------

Diagram of a single neuron with two inputs, x1 and x2, represented by lines connecting to an orange circular node.

<!-- IMAGE_DESCRIPTION: datalab-07f537f57749b75157f742525e6a8dbc_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A background image showing vertical columns of glowing blue binary digits (0s and 1s) on a black background, resembling a digital rain effect.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-cfef993dcc8fb513de79eb1f93cf26ae_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single neuron with two inputs, x1 and x2, represented by lines connecting to an orange circular node.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-d4af765160d04ecef538e5066006dc77_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single neuron with two inputs, x1 and x2, represented by lines connecting to an orange circular node.
<!-- /IMAGE_DESCRIPTION -->
### Redes Feed ForwardRede Perceptron - Topologia

| renda | dívida | classificação do cliente |
|-------|--------|--------------------------|
| 0,66  | 0,5    | 1                        |
| 1     | 1      | 0                        |
| 0,33  | 0,25   | 0                        |
| 1     | 0,75   | 1                        |

Diagram of a single neuron with two inputs, Renda - x1 and Divida - x2, represented by green arrows pointing to a yellow circular node. An output arrow points to the text 'Classificação Cliente'.

**Topologia menos usual.**

**Cada neurônio é capaz de decidir entre 2 classes:**

- Quando a rede devolve 0, significa que não é um cliente bom.
- Quando a rede devolve 1, significa que é um cliente bom.

{11}------------------------------------------------

Diagram of a single neuron with two inputs, x1 and x2, represented by lines connecting to an orange circular node.

<!-- IMAGE_DESCRIPTION: datalab-5a4e62bead259c258d069fd3663ea670_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single neuron with two inputs, Renda - x1 and Divida - x2, represented by green arrows pointing to a yellow circular node.
<!-- /IMAGE_DESCRIPTION -->
### Redes Feed Forward Rede Perceptron - Topologia

Classificação Cliente

| renda | dívida | D1 | D2 |
|-------|--------|----|----|
| 0,66  | 0,5    | 1  | 0  |
| 1     | 1      | 0  | 1  |
| 0,33  | 0,25   | 0  | 1  |
| 1     | 0,75   | 1  | 0  |

Diagram of a feedforward neural network with two input nodes (Renda - x1, Divida - x2) and two output nodes (1, 2). All nodes are fully connected. The output nodes are grouped by a bracket labeled 'Classificação Cliente'.

**Topologia mais usual.**

**Neurônio dedicados para cada classe:**

- Haverá uma saída esperada para cada neurônio.
- A saída da rede é dependente dos vários neurônios.
- Pode ser escolhido aquele de maior valor de saída.

{12}------------------------------------------------

Diagram of a single neuron with two inputs, x1 and x2, connected to an orange circular node.

<!-- IMAGE_DESCRIPTION: datalab-f9a14fbfecbd7d059226cc93677d721b_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single neuron (Perceptron) with two inputs, x1 and x2, connected to a single output node.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-1439cb942d9e363bbb3161b5540dd8c6_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a feedforward neural network with two input nodes (Renda - x1, Divida - x2) and two output nodes (1, 2).
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-af7916c89a458fdab6c3f443217388ae_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single neuron with two inputs, x1 and x2, connected to an orange circular node.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-410562339ce067fdc6fa41940c118658_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a neural network with two input nodes (Renda - x1, Divida - x2) and two output nodes (1, 2).
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-4801720824e4b5e2361a5564f91cfb70_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single neuron with two inputs, x1 and x2, connected to an orange circular node.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-a26e142d3df5bef41a84a9dd099d7825_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a neural network with two input nodes (Renda - x1, Divida - x2) and two output nodes (1, 2).
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-33ed1f9b27c7c21c797aa928b0f06851_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single neuron with two inputs, x1 and x2, connected to an orange circular node.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-9b6b5924b48bf2fd5f347f88f06f45b3_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a neural network with two input nodes (Renda - x1, Divida - x2) and two output nodes (1, 2).
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-fa859e4e468bfb2710a94527f2c504af_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single neuron with two inputs, x1 and x2, connected to an orange circular node.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-a83ba9e3e2c1e21dd69953a7b09e45b4_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a neural network with two input nodes (Renda - x1, Divida - x2) and two output nodes (1 and 2).
<!-- /IMAGE_DESCRIPTION -->
### Redes Feed Forward Rede Perceptron - Topologia

Classificação Cliente

Green arrow pointing to the first row of the table.

| renda | dívida | D1 | D2 |
|-------|--------|----|----|
| 0,66  | 0,5    | 1  | 0  |
| 1     | 1      | 0  | 1  |
| 0,33  | 0,25   | 0  | 1  |
| 1     | 0,75   | 1  | 0  |

Diagram of a neural network with two input nodes (Renda - x1, Divida - x2) and two output nodes (1, 2). Node 1 has a weight of 0,66 from x1 and 0,5 from x2. Arrows point from the output nodes to a bracket labeled 'Classificação Cliente'.

**Topologia mais usual.**

**Neurônio dedicados para cada classe:**

- Haverá uma saída esperada para cada neurônio.
- A saída da rede é dependente dos vários neurônios.
- Pode ser escolhido aquele de maior valor de saída.

{13}------------------------------------------------

Diagram of a single neuron with two inputs, x1 and x2, connected to an orange circular node.

<!-- IMAGE_DESCRIPTION: datalab-0cc86fe8fc37b0edc9581f2af9459a52_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Green arrow pointing to the first row of the table.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-a1d3651b1300f3670e3a9547bafc4db6_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Green arrow pointing to the first row of the table.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-9d5d3616a843e8063fdc3613055aaef8_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Green arrow pointing to the table.
<!-- /IMAGE_DESCRIPTION -->
### Redes Feed Forward Rede Perceptron - Topologia

Classificação Cliente

Green arrow pointing to the first row of the table.

| renda | dívida | D1 | D2 |
|-------|--------|----|----|
| 0,66  | 0,5    | 1  | 0  |
| 1     | 1      | 0  | 1  |
| 0,33  | 0,25   | 0  | 1  |
| 1     | 0,75   | 1  | 0  |

Diagram of a neural network with two input nodes (Renda - x1, Divida - x2) and two output nodes (1, 2). Node 1 has a weight of 0,66 from x1 and 0,5 from x2. Arrows point from the output nodes to a bracket labeled 'Classificação Cliente'.

**Topologia mais usual.**

**Neurônio dedicados para cada classe:**

- Haverá uma saída esperada para cada neurônio.
- A saída da rede é dependente dos vários neurônios.
- Pode ser escolhido aquele de maior valor de saída.

{14}------------------------------------------------

Diagram of a single neuron with two inputs, x1 and x2, connected to an orange circular node.
### Redes Feed Forward Rede Perceptron - Topologia

Classificação Cliente

Green arrow pointing to the left side of the table.

| renda | dívida | D1 | D2 |
|-------|--------|----|----|
| 0,66  | 0,5    | 1  | 0  |
| 1     | 1      | 0  | 1  |
| 0,33  | 0,25   | 0  | 1  |
| 1     | 0,75   | 1  | 0  |

Diagram of a neural network with two input nodes (Renda - x1, Divida - x2) and two output nodes (1, 2). All nodes are fully connected. Biases of 1 are shown above each node. The output nodes are grouped by a bracket labeled 'Classificação Cliente'.

**Topologia mais usual.**

**Neurônio dedicados para cada classe:**

- Haverá uma saída esperada para cada neurônio.
- A saída da rede é dependente dos vários neurônios.
- Pode ser escolhido aquele de maior valor de saída.

{15}------------------------------------------------

Diagram of a single neuron with two inputs, x1 and x2, connected to an orange circular node.

<!-- IMAGE_DESCRIPTION: datalab-0e240e8e4783e664047fbdb5fbd0989f_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Green arrow pointing to the left side of the table.
<!-- /IMAGE_DESCRIPTION -->
### Redes Feed Forward Rede Perceptron - Topologia

Classificação Cliente

| renda | dívida | D1 | D2 |
|-------|--------|----|----|
| 0,66  | 0,5    | 1  | 0  |
| 1     | 1      | 0  | 1  |
| 0,33  | 0,25   | 0  | 1  |
| 1     | 0,75   | 1  | 0  |

Green arrow pointing to the table.

Diagram of a neural network with two input nodes (Renda - x1, Divida - x2) and two output nodes (1 and 2). All inputs are connected to all outputs. Biases of 1 are shown for each output node. The output nodes are grouped by a bracket labeled 'Classificação Cliente'.

**Topologia mais usual.**

**Neurônio dedicados para cada classe:**

- Haverá uma saída esperada para cada neurônio.
- A saída da rede é dependente dos vários neurônios.
- Pode ser escolhido aquele de maior valor de saída.

{16}------------------------------------------------

Mais exemplos de  
topologia ...

An abstract visualization of a network graph. It features several glowing, yellowish-orange nodes connected by wavy, translucent lines representing edges. The background is a dark, reddish-brown color, and the overall effect is reminiscent of a complex network or a stylized neural network diagram.

Abstract visualization of a network graph with glowing nodes and wavy edges.

{17}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-7b1cea8c45c49887a750926f2135fa84_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Abstract visualization of a network graph with glowing nodes and wavy edges.
<!-- /IMAGE_DESCRIPTION -->
#### Exemplo 1 – Dados estruturados

An abstract visualization of a network structure, possibly representing a neural network or a complex graph. It features several interconnected nodes, each represented by a bright yellow circular center surrounded by a translucent orange ring. These nodes are connected by thick, wavy, semi-transparent lines in shades of orange and red. The background is a dark, deep red color, and the overall aesthetic is glowing and digital.

Abstract visualization of a neural network or graph structure.

{18}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-2150ae7f14a2e4ad1866ac0c8ec685ad_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Abstract visualization of a neural network or graph structure.
<!-- /IMAGE_DESCRIPTION -->
## Planta Iris

4 atributos de entrada

3 classes: Iris-setosa, Iris-versicolor, Iris-virginica

Diagrama de uma flor de Iris com rótulos das partes: Corola (conjunto de pétalas), Pétalas, Sépalas, and Cálice (conjunto de sépalas).

Diagrama de uma flor de Iris com rótulos das partes: Corola (conjunto de pétalas), Pétalas, Sépalas, and Cálice (conjunto de sépalas).

Gráfico de dispersão dos atributos de entrada das espécies Iris-setosa, Iris-versicolor e Iris-virginica. O gráfico mostra três clusters de pontos coloridos: azul para Iris-setosa, laranja para Iris-versicolor e verde para Iris-virginica. O Iris-setosa está isolado no canto inferior esquerdo, enquanto Iris-versicolor e Iris-virginica estão agrupados no canto superior direito, com alguma sobreposição.

Gráfico de dispersão dos atributos de entrada das espécies Iris-setosa, Iris-versicolor e Iris-virginica.

|   | sepal_length | sepal_width | petal_length | petal_width | species     |
|---|--------------|-------------|--------------|-------------|-------------|
| 0 | 5.1          | 3.5         | 1.4          | 0.2         | Iris-setosa |
| 1 | 4.9          | 3.0         | 1.4          | 0.2         | Iris-setosa |
| 2 | 4.7          | 3.2         | 1.3          | 0.2         | Iris-setosa |
| 3 | 4.6          | 3.1         | 1.5          | 0.2         | Iris-setosa |
| 4 | 5.0          | 3.6         | 1.4          | 0.2         | Iris-setosa |
| 5 | 5.4          | 3.9         | 1.7          | 0.4         | Iris-setosa |
| 6 | 4.6          | 3.4         | 1.4          | 0.3         | Iris-setosa |
| 7 | 5.0          | 3.4         | 1.5          | 0.2         | Iris-setosa |
| 8 | 4.4          | 2.9         | 1.4          | 0.2         | Iris-setosa |
| 9 | 4.9          | 3.1         | 1.5          | 0.1         | Iris-setosa |

{19}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-78ebfe3116918cd317b54c861da8d8d2_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de uma flor de Iris com rótulos das partes: Corola (conjunto de pétalas), Pétalas, Sépalas, and Cálice (conjunto de sépalas).
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-3468bcffa38de23cef94bfb460ccb301_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Gráfico de dispersão dos atributos de entrada das espécies Iris-setosa, Iris-versicolor e Iris-virginica.
<!-- /IMAGE_DESCRIPTION -->
## Planta Iris

4 atributos de entrada  
**2 classes: Iris-setosa, Nao Iris-setosa**

A scatter plot showing the relationship between four features (sepal length, sepal width, petal length, petal width) for three species of Iris. The species are Iris-setosa (blue), Iris-versicolor (orange), and Iris-virginica (green). A decision boundary line is drawn, separating the Iris-setosa cluster from the other two species.

species

- Iris-setosa
- Iris-versicolor
- Iris-virginica

Scatter plot of Iris dataset showing three species: Iris-setosa (blue), Iris-versicolor (orange), and Iris-virginica (green). A decision boundary line separates the Iris-setosa cluster from the others.

Diagram of an Iris flower showing its parts:

- Corola (conjunto de pétalas)
- Pétalas
- Sépalas
- Cálice (conjunto de sépalas)

Diagram of an Iris flower showing its parts: Corola (conjunto de pétalas), Pétalas, Sépalas, and Cálice (conjunto de sépalas).

|   | sepal_length | sepal_width | petal_length | petal_width | species     |
|---|--------------|-------------|--------------|-------------|-------------|
| 0 | 5.1          | 3.5         | 1.4          | 0.2         | Iris-setosa |
| 1 | 4.9          | 3.0         | 1.4          | 0.2         | Iris-setosa |
| 2 | 4.7          | 3.2         | 1.3          | 0.2         | Iris-setosa |
| 3 | 4.6          | 3.1         | 1.5          | 0.2         | Iris-setosa |
| 4 | 5.0          | 3.6         | 1.4          | 0.2         | Iris-setosa |
| 5 | 5.4          | 3.9         | 1.7          | 0.4         | Iris-setosa |
| 6 | 4.6          | 3.4         | 1.4          | 0.3         | Iris-setosa |
| 7 | 5.0          | 3.4         | 1.5          | 0.2         | Iris-setosa |
| 8 | 4.4          | 2.9         | 1.4          | 0.2         | Iris-setosa |
| 9 | 4.9          | 3.1         | 1.5          | 0.1         | Iris-setosa |

<!-- DATALAB_CHUNK 2: pages 21-40 -->

{20}------------------------------------------------

# Planta Iris

Diagram of an iris flower showing its components: Corola (conjunto de pétalas), Pétalas, Sépalas, and Cálice (conjunto de sépalas).

Diagram of an iris flower showing its components: Corola (conjunto de pétalas), Pétalas, Sépalas, and Cálice (conjunto de sépalas).

Diagram illustrating the processing of Iris plant attributes through a neural network structure. The inputs are: Comprimento da sépala ( $x_1$ ), Largura da sépala ( $x_2$ ), Comprimento da pétala ( $x_3$ ), and Largura da pétala ( $x_4$ ). These inputs are connected to weights ( $w_{1j}$ ,  $w_{2j}$ ,  $w_{3j}$ ,  $w_{4j}$ ), which are then summed ( $\Sigma$ ) and passed through an activation function ( $f$ ) to produce the output (Saida). A bias term is also shown as an input to the activation function.

Neural network diagram for Iris plant classification showing inputs (x1, x2, x3, x4) connected to weights (w1j, w2j, w3j, w4j), which are summed ($\Sigma$) and passed through an activation function (f) to produce an output (Saida).

Atributos dos objetos

Entrada com Dados estruturados

{21}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-96a7eac66ef72bb016c280278506ac63_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Scatter plot of Iris dataset showing three species: Iris-setosa (blue), Iris-versicolor (orange), and Iris-virginica (green).
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-63c666b05041841b01fdef9fa4153ff7_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of an Iris flower showing its parts: Corola (conjunto de pétalas), Pétalas, Sépalas, and Cálice (conjunto de sépalas).
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-3376f33dd811eb3e39ff47117c958ed9_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of an iris flower showing its components: Corola (conjunto de pétalas), Pétalas, Sépalas, and Cálice (conjunto de sépalas).
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-f756d8e1fde6bc6ebdf4a5d7f1b2a57a_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of an iris flower showing its parts: Corola (conjunto de pétalas), Pétalas, Sépalas, and Cálice (conjunto de sépalas).
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-15faea1eb0f5fbd0d54291a786091afc_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of an iris flower showing its parts: Corola (conjunto de pétalas), Pétalas, Sépalas, and Cálice (conjunto de sépalas).
<!-- /IMAGE_DESCRIPTION -->
## Planta Iris

The diagram illustrates a neural network model for Iris flower classification. It consists of four input nodes representing measured attributes, each connected to a summation node ( $\Sigma$ ) via a weight node ( $w_{ij}$ ). The inputs and their corresponding weights are: **Comprimento da sépala ( $x_1$ )** with weight **5.1**, **Largura da sépala ( $x_2$ )** with weight **3.5**, **Comprimento da pétala ( $x_3$ )** with weight **1.4**, and **Largura da pétala ( $x_4$ )** with weight **0.2**. The summation node  $\Sigma$  receives the weighted inputs and passes them to a function block  $f$ , which also receives input from a **Função de Ativação** (Activation Function). The output of the function block is labeled **Saída** (Output). A green arrow points to the input labels, identifying them as **Atributos dos objetos** (Object attributes).

Diagram of an Iris flower neural network model showing inputs, weights, summation, activation function, and output.

This diagram shows the anatomical structure of an Iris flower. It labels the **Corola (conjunto de pétalas)** (Corolla, set of petals), **Pétalas** (Petals), **Sépalas** (Sepals), and **Cálice (conjunto de sépalas)** (Calyx, set of sepals). The flower is shown in a cross-section view, highlighting the internal reproductive structures.

Diagram of an Iris flower showing its anatomical parts: Corolla (set of petals), Petals, Sepals, and Calyx (set of sepals).

Atributos dos objetos

Entrada com Dados estruturados

{22}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-c5655e700cc3e9aac7e9f4f07f30264d_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Neural network diagram for Iris plant classification showing inputs (x1, x2, x3, x4) connected to weights (w1j, w2j, w3j, w4j), which are summed (Σ) and passed through an activation function (f) to produce an output...
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-08a978a124d3ed6cf1a3d0cfd89418d0_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of an Iris flower neural network model showing inputs, weights, summation, activation function, and output.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-0b0dbdb00519a67d96c812ee07da3a1e_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of an Iris flower showing its anatomical parts: Corolla (set of petals), Petals, Sepals, and Calyx (set of sepals).
<!-- /IMAGE_DESCRIPTION -->
## Planta Iris

Diagram of an iris flower with labels: Corola (conjunto de pétalas), Pétalas, Sépalas, and Cálice (conjunto de sépalas).

Diagram of an iris flower showing its parts: Corola (conjunto de pétalas), Pétalas, Sépalas, and Cálice (conjunto de sépalas).
## Topologia para 2 classes Classificador Binario Neural

Diagram of a neural network topology for iris classification. It shows four input nodes ( $x_1, x_2, x_3, x_4$ ) connected to two output nodes (1 and 2). Node 1 is labeled "Iris-Setosa" and node 2 is labeled "Nao Iris-setosa".

Diagram of a neural network topology for iris classification. It shows four input nodes (x1, x2, x3, x4) connected to two output nodes (1 and 2). Node 1 is labeled 'Iris-Setosa' and node 2 is labeled 'Nao Iris-setosa'.

**Topologia: 4 x 2**

Camada de entrada(dados): 4

Camada de saída (neuronios): 2

Tipo de Planta Iris

| x1  | x2  | x3  | x4  | d1 | d2 |
|-----|-----|-----|-----|----|----|
| 5.1 | 3.5 | 1.4 | 0.2 | 1  | 0  |
| 7   | 3.2 | 4.7 | 1.4 | 0  | 1  |
| ... |     |     |     |    |    |

Iris-Setosa

Nao Iris-Setosa

{23}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-eb03559a4d92ea9ebd63ea9be663c50a_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a neural network topology for iris classification.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-d9843ac5dfc4bbe9e4d21b8898723b5e_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a neural network for sentence classification.
<!-- /IMAGE_DESCRIPTION -->
### Exemplo 2 – Dados desestruturados

A stylized illustration of a neural network. It features several glowing yellow circular nodes, each with a white center, connected by thick, wavy, orange-brown lines that resemble axons or synapses. The background is a dark, deep red color, and the overall aesthetic is futuristic and digital, representing interconnected data points or artificial intelligence.

A stylized illustration of a neural network with glowing yellow nodes and orange connections against a dark red background.

{24}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-7cdd3a0b8107619a3a05ea9ed16eff02_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A stylized illustration of a neural network with glowing yellow nodes and orange connections against a dark red background.
<!-- /IMAGE_DESCRIPTION -->
### Reconhecedor de Caracteres

- Considere como entrada de uma imagem de caracteres: 5 x 5.

A 5x5 grid of squares with a color gradient from dark blue in the top-left to light green in the bottom-right.

- Objetivo: identificar as imagens correspondentes a vogais:

Five 5x5 grids of squares, each containing a different pattern of green and white squares, representing different vowel characters.

{25}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-56a7fc5964ed9463fa47ca8a60568dec_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A 5x5 grid of squares with a color gradient from dark blue in the top-left to light green in the bottom-right.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-d4c143a69ccd7e28fe8d01dbc9dfbcfa_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Five 5x5 grids of squares, each containing a different pattern of green and white squares, representing different vowel characters.
<!-- /IMAGE_DESCRIPTION -->
### Reconhecedor de Caracteres

The diagram illustrates a character recognition system. On the left, a 5x5 grid of squares represents the input image, with a color gradient from dark blue to light green. Below this grid is the label "5x5". To the right of the grid is a vertical column of 25 squares, each corresponding to a pixel in the input. These squares are labeled  $pixel (x_1)$ ,  $pixel (x_2)$ ,  $pixel (x_3)$ , followed by three vertical dots, and finally  $pixel (x_{25})$ . Each pixel label is connected by an arrow to a circular node representing a weight, labeled  $w_{1j}$ ,  $w_{2j}$ ,  $w_{3j}$ , ...,  $w_{25j}$ . The word "Pesos" (Weights) is written above the weight nodes. All weight nodes have arrows pointing to a central circular node containing the summation symbol  $\Sigma$ . An arrow from the summation node points to a square box containing the letter  $f$ , representing the activation function. Below this box is the label "Função de Ativação" (Activation Function). An arrow from the right side of the box points to the word "Saida" (Output).

Diagram of a character recognizer neural network architecture.

Atributos dos objetos

{26}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-0c08e48c08f96934cd6bc6911f3069dc_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a character recognizer neural network architecture.
<!-- /IMAGE_DESCRIPTION -->
#### Reconhecedor de Caracteres

The diagram illustrates the architecture of a character recognizer. On the left, a 5x5 grid of green squares represents an input character. Below it, the binary representation of the grid is shown as a vertical vector of 25 bits (1s and 0s), with the first five bits being 11111. This vector is labeled "Atributos dos objetos" (Object attributes). To the right of the vector, the first three pixels are labeled  $pixel(x_1)$ ,  $pixel(x_2)$ , and  $pixel(x_3)$ , followed by vertical ellipses, and the last pixel is labeled  $pixel(x_{25})$ . Each pixel is connected to a corresponding weight node labeled  $w_{1j}$ ,  $w_{2j}$ ,  $w_{3j}$ , ...,  $w_{25j}$ . These weights are collectively labeled "Pesos" (Weights). The weighted inputs are summed in a node labeled  $\Sigma$ . The output of the summation is passed to a square block labeled  $f$ , which represents the "Função de Ativação" (Activation function). The final output is labeled "Saida" (Output). Below the activation function block, five small 5x5 grids show different binary patterns of green squares, representing the output for different input characters.

Diagram of a character recognizer neural network architecture showing input pixel extraction, weighted summation, and activation function.

{27}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-043e64d41a3368d138ace3816fd26469_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a character recognizer neural network architecture showing input pixel extraction, weighted summation, and activation function.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-eb5677b570ab2a3e9d8f5d35ca5b8a4d_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Five 5x5 grids showing the binary representation of characters A, E, I, O, U.
<!-- /IMAGE_DESCRIPTION -->
#### Reconhecedor de Caracteres

The diagram illustrates the input representation of characters. On the left, five 5x5 grids represent the characters A, E, I, O, and U. Each grid is associated with a binary vector of length 25 (e.g., 11111, 10001, 11111, 10001, 10001). These vectors are then processed through a layer of 25 attributes, labeled  $x_1, x_2, x_3, x_4, \dots, x_{25}$ . This layer is connected to five output nodes, labeled 1, 2, 3, 4, and 5, which correspond to the characters A, E, I, O, and U respectively.

Diagram showing the input representation of characters A, E, I, O, U as 5x5 grids and their corresponding binary vectors. These are then processed through a layer of 25 attributes (x1 to x25) which are then mapped to the five characters.

Atributos dos objetos

Topologia: 25 x 5

The diagram shows five 5x5 grids, each representing a character (A, E, I, O, U) in a binary format. Each grid consists of 25 cells, each containing either a green square (representing 1) or a white square (representing 0).

Five 5x5 grids showing the binary representation of characters A, E, I, O, U.

| $x_1, x_2, x_3, \dots, x_{25}$ | d1 | d2 | d3 | d4 | d5 |
|--------------------------------|----|----|----|----|----|
| 1,1,1,1,1,1,1,0,...            | 1  | 0  | 0  | 0  | 0  |
| 1,1,1,1,1,1,1,0,...            | 0  | 1  | 0  | 0  | 0  |
| 0,0,1,0,0,0,0,0,...            | 0  | 0  | 1  | 0  | 0  |
| 1,1,1,1,1,1,1,0,...            | 0  | 0  | 0  | 1  | 0  |
| 1,0,0,0,1,1,0,...              | 0  | 0  | 0  | 0  | 1  |
| ...                            |    |    |    |    |    |

{28}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-d17aa1fcc3b86503ad1dd0717a6c34c2_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram showing the input representation of characters A, E, I, O, U as 5x5 grids and their corresponding binary vectors.
<!-- /IMAGE_DESCRIPTION -->
### Exemplo 3 – Dados desestruturados

An abstract visualization of a network, likely representing a neural network or a complex data graph. It features several glowing, yellowish-orange nodes connected by thick, translucent, wavy lines that resemble axons or data streams. The background is a dark, deep red color, and the overall aesthetic is futuristic and digital.

Abstract visualization of a neural network or data graph.

{29}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-e84dd53f6912e1d1da8c934533cc599f_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Abstract visualization of a neural network or data graph.
<!-- /IMAGE_DESCRIPTION -->
### Classificador de sentenças

The diagram illustrates a sentence classifier architecture. On the left, an icon of a document represents the input sentence. Below it, a green arrow points to the word "Atributos" (Attributes). The input is processed through a series of tokens:  $token (x_1)$ ,  $token (x_2)$ ,  $token (x_3)$ , followed by vertical ellipsis dots, and finally  $token (x_n)$ . Each token is connected to a corresponding weight node:  $w_{1j}$ ,  $w_{2j}$ ,  $w_{3j}$ , ...,  $w_{nj}$ . These weight nodes are collectively labeled "Pesos" (Weights) and are all connected to a central summation node, represented by a circle with the symbol  $\Sigma$ . The output of the summation node is fed into a square box labeled  $f$ , which represents the "Função de Ativação" (Activation Function). An arrow points from the box to the word "Saida" (Output).

Diagram of a sentence classifier neural network architecture.

Tipicamente esse problema não é linearmente separável. Ele precisa de uma rede várias camadas.

{30}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-5414f65867392f05ba0063b208eeb5e1_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a sentence classifier neural network architecture.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-5d3455c6c2a37cb3aff761fedeb8644e_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a sentence classifier neural network architecture.
<!-- /IMAGE_DESCRIPTION -->
### Classificador de sentenças

The diagram illustrates a sentence classifier architecture. On the left, a box contains the sentence: *A infraestrutura do hotel era maravilhosa.* Below this, a green arrow points to the word **Atributos** (Attributes). To the right of the sentence, several attributes are listed with their corresponding binary values: *infraestrutura* ( $x_1$ ) with value 1, *hotel* ( $x_2$ ) with value 1, *ruim* ( $x_3$ ) with value 0, and *maravilhosa* ( $x_n$ ) with value 1. Each attribute is connected to a circular node representing a weight:  $w_{1j}$ ,  $w_{2j}$ ,  $w_{3j}$ , and  $w_{nj}$ . These nodes are collectively labeled **Pesos** (Weights). Arrows from these weight nodes point to a summation node, represented by a circle with the symbol  $\Sigma$ . The output of the summation node is then passed to a rectangular block labeled  $f$ , which represents the **Função de Ativação** (Activation Function). The final output of the system is labeled **Saída** (Output).

Diagram of a sentence classifier neural network architecture.

Tipicamente esse problema não é linearmente separável. Ele precisa de uma rede várias camadas.

{31}------------------------------------------------
### Classificador de sentenças

Sentença

$x_1$   
 $x_2$   
 $x_3$   
 $x_4$   
...  
 $x_n$

Atributos

k

Positiva

Negativa

Neutra

Diagram of a neural network for sentence classification. The input is a vector of attributes (x1, x2, x3, x4, ..., xn) labeled 'Sentença'. An arrow points from 'Atributos' to this input. The input is connected to a first hidden layer with nodes 1, 2, 3, 4, and k. This layer is fully connected to a second hidden layer with nodes 1, 2, and 3. The output nodes are labeled 'Positiva', 'Negativa', and 'Neutra'.

Veremos mais detalhes dessa topologia na aula sobre MultiLayer Perceptron.

Tipicamente esse problema não é linearmente separável. Ele precisa de uma rede várias camadas.

{32}------------------------------------------------
## Etapas Básicas de Construção de uma Rede Neural

```
graph LR; Dataset[(Dataset)] --> Pre[Pre-processamento]; Pre --> Treino[(Dataset Treino)]; Pre --> Teste[(Dataset Teste)]; Treino --> Treinamento[Fase de Treinamento]; Teste --> Generalizacao[Fase de Generalizacao]; Treinamento --> Modelo[Modelo]; Modelo --> Generalizacao; Generalizacao --> Resultados[Resultados];
```

The diagram illustrates the basic steps for building a neural network. It begins with a **Dataset** (represented by a grey cylinder) which undergoes **Pre-processamento** (Pre-processing, represented by a blue rectangle). This leads to two separate datasets: **Dataset Treino** (Training Dataset, represented by a dark blue cylinder) and **Dataset Teste** (Test Dataset, represented by a brown cylinder). The **Dataset Treino** is used in the **Fase de Treinamento** (Training Phase, represented by a blue rectangle), which produces a **Modelo** (Model, represented by a light green rectangle). The **Modelo** is then used in the **Fase de Generalizacao** (Generalization Phase, represented by a blue rectangle), which also takes the **Dataset Teste** as input. The final output is **Resultados** (Results).

Flowchart of basic steps for building a neural network: Dataset -> Pre-processing -> Training Dataset & Test Dataset -> Training Phase & Generalization Phase -> Model -> Results.

{33}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-c76da2d73c064464051d1583fd80bb6b_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Flowchart of basic steps for building a neural network: Dataset -> Pre-processing -> Training Dataset & Test Dataset -> Training Phase & Generalization Phase -> Model -> Results.
<!-- /IMAGE_DESCRIPTION -->
### Rede Perceptron

- Como já mencionado, essas redes só conseguem resolver problemas linearmente separáveis.
- O algoritmo de aprendizado desse tipo de rede, procura os coeficientes que traçam a reta que separa linearmente os dados de uma classe de outra.

A scatter plot on a light gray background. It contains two clusters of data points: blue dots in the upper right and red dots in the lower left. A solid black line, representing a linear classifier, runs diagonally from the middle-left towards the bottom-right, successfully separating the two groups of points. The label "#0" is positioned above the plot area.

A scatter plot showing two classes of data points (blue and red) that are linearly separable. A straight line separates the two groups. The plot is labeled #0.

{34}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-fae82236e4211f753df5789eb276d3a4_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A scatter plot showing two classes of data points (blue and red) that are linearly separable.
<!-- /IMAGE_DESCRIPTION -->
### Rede Perceptron

Revisitando um neurônio artificial j:

The diagram illustrates the structure of an artificial neuron  $j$ . It features an input layer with nodes  $x_0, x_1, x_2, x_3, \dots, x_n$ . Each input is connected to a corresponding weight node:  $w_{0j}$  (orange circle),  $w_{1j}$ ,  $w_{2j}$ ,  $w_{3j}$ ,  $\dots$ , and  $w_{nj}$  (green circles). The weights  $w_{1j}$  through  $w_{nj}$  are collectively labeled "Pesos". The weight  $w_{0j}$  is specifically labeled "Peso extra conhecido como bias" and is associated with the input  $x_0 = 1$ . All weighted inputs are fed into a summation node  $\Sigma$  (green circle). The output of the summation is  $v_j$ , which is then passed to an activation function  $f$  (green square). The final output is  $y_j$ , labeled "Saida". The activation function  $f$  is also labeled "Função de Ativação".

Diagram of an artificial neuron j. Inputs x0, x1, x2, x3, ..., xn are connected to weights w0j, w1j, w2j, w3j, ..., wnj. The weights are summed in a summation node $\Sigma$. The result vj is passed to an activation function f to produce the output yj. A label 'Peso extra conhecido como bias' is associated with w0j. A label 'Pesos' is associated with the other weights.

$$v_j = w_{0j} + \sum_{i=1}^n (x_i \times w_{ij})$$
$$y_j = f(v_j)$$

{35}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-dcc2d5a5b39f780e7a224bb01ba1ef6e_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of an artificial neuron j. Inputs x0, x1, x2, x3, ..., xn are connected to weights w0j, w1j, w2j, w3j, ..., wnj. The weights are summed in a summation node Σ. The result vj is passed to an activation function f...
<!-- /IMAGE_DESCRIPTION -->
### Rede Perceptron

Revisitando um neurônio artificial j:

$x_0$  →  $w_{0j}$  *Peso extra conhecido como bias*  
 $x_0 = 1$

$x_1$  →  $w_{1j}$

$x_2$  →  $w_{2j}$

$x_3$  →  $w_{3j}$

$\vdots$  →  $\vdots$

$x_n$  →  $w_{nj}$

*Pesos*

$\Sigma$  →  $v_j$  →  $f$  → Saida  $y_j$

Função de Ativação

Diagram of an artificial neuron j. Inputs x0, x1, x2, x3, ..., xn are shown on the left. x0 is a bias term with x0 = 1. Each input is connected to a weight node (w0j, w1j, w2j, w3j, ..., wnj). The weights are then summed in a summation node ($\Sigma$). The result is passed to an activation function node (f). The output is labeled 'Saida' and yj. A label 'Pesos' is placed near the summation node. A label 'Peso extra conhecido como bias' is placed near the bias weight w0j.

$$v_j = \sum_{i=0}^n (x_i \times w_{ij})$$

$$y_j = f(v_j)$$

{36}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-1142ba0197b158bb198186fe8baccc32_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of an artificial neuron j. Inputs x0, x1, x2, x3, ..., xn are shown on the left. x0 is a bias term with x0 = 1. Each input is connected to a weight node (w0j, w1j, w2j, w3j, ..., wnj). The weights are then...
<!-- /IMAGE_DESCRIPTION -->
### Rede Perceptron
#### Revisitando um neurônio artificial j:

- Existem várias funções de ativação para as redes neurais.
- As clássicas são:
  - Limiar ou degrau
  - Linear
  - Sigmoide: logística ou tangente hiperbólica
- Geralmente o Perceptron usa a função limiar.

Graph of the step function activation function, labeled (a) Limiar ou Degrau. The vertical axis is  $\phi(v_j)$  and the horizontal axis is  $\phi_j$ . The function is a dashed line that is constant at a negative value for  $\phi_j < 0$  and constant at a positive value for  $\phi_j \geq 0$ , with a vertical jump at the origin.

Graph of the step function activation function.

Graph of the linear function activation function, labeled (b) Linear. The vertical axis is  $\phi(v_j)$  and the horizontal axis is  $\phi_j$ . The function is a dashed line passing through the origin with a constant positive slope.

Graph of the linear function activation function.

Graph of the logistic function activation function, labeled (c) Logistica. The vertical axis is  $\phi(v_j)$  and the horizontal axis is  $\phi_j$ . The function is a dashed S-shaped curve passing through the origin, asymptotically approaching a negative constant as  $\phi_j \rightarrow -\infty$  and a positive constant as  $\phi_j \rightarrow \infty$ .

Graph of the logistic function activation function.

Graph of the hyperbolic tangent function activation function, labeled (d) Tangente Hiperbolica. The vertical axis is  $\phi(v_j)$  and the horizontal axis is  $\phi_j$ . The function is a dashed S-shaped curve passing through the origin, asymptotically approaching  $-1$  as  $\phi_j \rightarrow -\infty$  and  $1$  as  $\phi_j \rightarrow \infty$ .

Graph of the hyperbolic tangent function activation function.

{37}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-bf30e154f82662d212f21fccdfa2980f_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Graph of the step function activation function.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-a0fdaf0b566e05f53f0085cf41e2dbad_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Graph of the linear function activation function.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-fd38170a3981416226ab91f7437ba821_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Graph of the logistic function activation function.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-1cd6a2d6e58e0e6d75c879a999be06ef_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Graph of the hyperbolic tangent function activation function.
<!-- /IMAGE_DESCRIPTION -->
### Rede Perceptron

Revisitando um neurônio artificial j:

$x_0 \rightarrow w_{0j}$  *Peso extra conhecido como bias*  
 $x_0 = 1$

$x_1 \rightarrow w_{1j}$

$x_2 \rightarrow w_{2j}$

$x_3 \rightarrow w_{3j}$

$\vdots \quad \vdots$

$x_n \rightarrow w_{nj}$

*Pesos*

$\Sigma \xrightarrow{v_j} f \xrightarrow{\text{Saida}} y_j$

*Função de Ativação*

Diagram of an artificial neuron j. Inputs x0, x1, x2, x3, ..., xn are shown on the left. x0 is labeled 'x0 = 1' and 'Peso extra conhecido como bias'. The other inputs are connected to weights w0j, w1j, w2j, w3j, ..., wnj, which are collectively labeled 'Pesos'. All weighted inputs are summed in a circle labeled $\Sigma$. The result vj is passed to a square box labeled f, which is labeled 'Função de Ativação'. The output is labeled 'Saida yj'.

$$v_j = \sum_{i=0}^n (x_i \times w_{ij})$$

$$y_j = f(v_j)$$

*Função de ativação - Limiar*

$$f(v_j) = \begin{cases} 1 \text{ se } v_j \geq 0 \\ 0 \text{ se } v_j < 0 \end{cases}$$

{38}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-02bb4edc0dbdf4f0749ffd3e0ea2805c_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of an artificial neuron j. Inputs x0, x1, x2, x3, ..., xn are shown on the left. x0 is labeled 'x0 = 1' and 'Peso extra conhecido como bias'. The other inputs are connected to weights w0j, w1j, w2j, w3j, ......
<!-- /IMAGE_DESCRIPTION -->
### Treinamento de Rede Neuronais

Dataset com dados históricos, pre-processado e anotado com classes:

- **Divida o dataset** (harmonicamente, no caso de classes), em conjuntos disjuntos de:
- - **treino**: usado para o treinamento do modelo;
- - **validação**: usado para validar o modelo durante o treinamento;
- - **teste**: usado para verificar a solução, ou seja, a versão final do modelo, após o treinamento .

The figure displays three donut charts illustrating different dataset splits for training, validation, and testing. The legend on the right indicates that teal represents Treino, orange represents Validação, and purple represents Teste.

| Split | Treino (%) | Validação (%) | Teste (%) |
|-------|------------|---------------|-----------|
| 1     | 80         | 10            | 10        |
| 2     | 70         | 15            | 15        |
| 3     | 60         | 20            | 20        |

Three donut charts showing different dataset splits for training, validation, and testing. The first chart shows 80% training, 10% validation, and 10% testing. The second chart shows 70% training, 15% validation, and 15% testing. The third chart shows 60% training, 20% validation, and 20% testing. A legend on the right indicates that teal represents Treino, orange represents Validação, and purple represents Teste.

Fonte da Figura: <https://www.v7labs.com/blog/train-validation-test-set#:~:text=Training%20data%20is%20the%20set,after%20completing%20the%20training%20phase.>

{39}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-673e9e5873f9a4b71bbe7bac2cf6b758_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Three donut charts showing different dataset splits for training, validation, and testing.
<!-- /IMAGE_DESCRIPTION -->
### Treinamento de Redes Neuronais

Como os subconjuntos de treino, validação e teste são usados:

The diagram illustrates the iterative process of training a neural network model. It begins with the **Treino** (Training) phase, where a model is generated using the training dataset. This leads to the **Treinamento do modelo** (Model training) block. From there, the model is passed to the **Avaliação do modelo** (Model evaluation) block, which also receives input from the **Validação** (Validation) dataset. The evaluation block produces two possible outcomes: if the results **não atingiram** (did not reach) the desired accuracy, the process moves to **Ajustes nos algoritmos e/ou dados** (Adjustments in algorithms and/or data), which then loops back to the training block; if the results **atingiram** (reached) the desired accuracy, the process moves to the final **Avaliação final do modelo** (Final model evaluation) block, which is also informed by the **Teste** (Testing) dataset. Text labels explain that the model is tested using the validation dataset during the evaluation phase and the testing dataset during the final evaluation phase.

Diagram of the neural network training process showing training, validation, and testing phases.

$$\text{Acurácia} = \frac{\text{Número de predições corretas}}{\text{Total de predições}}$$

<!-- DATALAB_CHUNK 3: pages 41-60 -->

{40}------------------------------------------------

# Treinamento de Redes Neurais

- Os **ciclos de treinamento de uma rede** são medidos em **épocas**.
- Uma época **corresponde a passagem de todos os dados do conjunto de treino uma vez pela rede**.
- Para treinar uma rede são necessárias várias épocas.

{41}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-e151d3468319b81f042ca232c4d82e4b_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of the neural network training process showing training, validation, and testing phases.
<!-- /IMAGE_DESCRIPTION -->
## Rede Perceptron - Algoritmo de Treinamento

Algoritmo de Treinamento do Perceptron: usa Regra Delta (correção de erro)

- Sendo  $X = \{ (dados1; saidaDesejada1); (dados1; saidaDesejada2), \dots \}$
- A taxa de aprendizagem  $\eta$  (deve ser positiva).

```
Inicializar todos pesos da rede com zero :  $w_{ij} = 0$ 
Repetir ate encontrar erroGeral=0:
    epocas = epocas +1
    erroGeral = 0
    Para cada neuronio j: 1 a k da rede :
         $v_j = 0$ 
        Para cada atributo i: 0 a n dos dados de X :
             $v_j = v_j + x_i * w_{ij}$ 
         $y_j = f(v_j)$ 
         $erro_j = d_j - y_j$ 
        se  $erro_j \neq 0$  entao :
             $\delta = \eta * erro_j * x_i$ 
             $w_{ij} = w_{ij} + \delta$ 
    erroGeral = erroGeral + abs(erro_j)
```

{42}------------------------------------------------

Qual o objetivo  
do treinamento  
de uma rede  
neural?

O que estamos  
procurando?

A grayscale image of a neural network diagram. It features several spherical nodes connected by lines, representing neurons and their connections. The nodes are arranged in a grid-like pattern, with some in sharp focus and others blurred in the background, creating a sense of depth. The overall aesthetic is clean and technical.

{43}------------------------------------------------

**Os pesos sinápticos.**

São neles que o conhecimento  
adquirido pela rede fica armazenado.

{44}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-db267ff9c1b97bbae0cb0856be1d8734_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A grayscale image of a neural network diagram.
<!-- /IMAGE_DESCRIPTION -->
### Rede Perceptron – Limitações
## Tabela OR

| $x_1$ | $x_2$ | $d$ |
|-------|-------|-----|
| 0     | 0     | 0   |
| 0     | 1     | 1   |
| 1     | 0     | 1   |
| 1     | 1     | 1   |

Gráfico da função OR no plano  $x_1$ - $x_2$ . O eixo  $x_1$  é horizontal e o eixo  $x_2$  é vertical. Os pontos de dados são representados por círculos azuis:  $(0,0)$  rotulado com 0,  $(0,1)$  rotulado com 1,  $(1,0)$  rotulado com 1, e  $(1,1)$  rotulado com 1. Uma linha preta diagonal com declive negativo representa a separação linear proposta pelo perceptron, passando por  $(0, -0.5)$  e  $(0.5, 0)$ . Esta linha não consegue separar os pontos de classe 0 e 1, demonstrando a limitação de um único perceptron para problemas não linearmente separáveis.

Gráfico da função OR no plano x1-x2

{45}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-0e2f908bcaa3136175994fcf0c9c1a9f_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Gráfico da função OR no plano x1-x2
<!-- /IMAGE_DESCRIPTION -->
### Rede Perceptron – Limitações
## Tabela XOR

| $x_1$ | $x_2$ | $d$ |
|-------|-------|-----|
| 0     | 0     | 0   |
| 0     | 1     | 1   |
| 1     | 0     | 1   |
| 1     | 1     | 0   |

A scatter plot illustrating the XOR problem in a 2D space. The horizontal axis is labeled  $x_1$  and the vertical axis is labeled  $x_2$ . The origin is marked with 0. There are four data points represented by blue circles: (0,0), (0,1), (1,0), and (1,1). The point (0,1) is labeled '1'. The point (1,0) is labeled '1'. The point (1,1) is labeled '0' and has a large red question mark next to it, indicating the non-separability of the classes.

Scatter plot of XOR data points in a 2D space with axes x1 and x2. The points are at (0,0), (0,1), (1,0), and (1,1). The point (1,1) is labeled '0' and has a large red question mark next to it.

{46}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-068b3a3247570c4b78342a943f15de9e_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Scatter plot of XOR data points in a 2D space with axes x1 and x2.
<!-- /IMAGE_DESCRIPTION -->
### Simulando uma Rede Perceptron

- Pesos inicializados com zero:  $w_{10} = 0, w_{11} = 0, w_{12} = 0$
- limiar:  $Q(v_k) = \begin{cases} 1 & \text{se } v_k \geq 0 \\ 0 & \text{caso contrário} \end{cases}$ , taxa de aprendizagem:  $\eta = 1$

| x1 | x2 | d |
|----|----|---|
| 0  | 0  | 0 |
| 0  | 1  | 1 |
| 1  | 0  | 1 |
| 1  | 1  | 1 |

Diagram illustrating the propagation step of a perceptron. The neuron receives inputs  $x_0=1$  (bias),  $x_1$ , and  $x_2$  with weights  $w_{10}=0.0$ ,  $w_{11}=0.0$ , and  $w_{12}=0.0$ . The output is  $y_1=1.0$ . The table to the left provides the input data for the first row:  $x_1=0, x_2=0, d=0$ .

Diagram of a single neuron representing a perceptron. It shows inputs x0=1 (bias), x1, and x2 entering a circular node labeled '1'. Weights w10=0.0, w11=0.0, and w12=0.0 are shown on the connections. The output is y1=1.0. A table to the left shows input data. An arrow labeled 'propagação' points from the table to the neuron.

- $v_1 = x_0 \times w_{10} + x_1 \times w_{11} + x_2 \times w_{12}$
- $v_1 = 1 \times 0 + 0 \times 0 + 0 \times 0 = 0$
- $y_1 = Q(v_1) = Q(0) = 1.0$

- Ajuste dos pesos (Aplicando a regra delta)

- $erro_1 = d_1 - y_1 = 0 - 1.0 = -1.0$
- $w_{10} = w_{10} + \eta \times erro_1 \times x_0 = 0.0 + 1 \times -1.0 \times 1 = -1.0$
- $w_{11} = w_{11} + \eta \times erro_1 \times x_1 = 0.0 + 1 \times -1.0 \times 0 = 0.0$
- $w_{12} = w_{12} + \eta \times erro_1 \times x_2 = 0.0 + 1 \times -1.0 \times 0 = 0.0$

{47}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-be3e5fe8be7cc5a74f67a4b8ac93193d_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single neuron representing a perceptron.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-7e61b2e2506cc7e5d6e16ce9c9df25bb_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a perceptron neuron. It shows inputs x0=1 (bias), x1, and x2 entering a neuron node labeled '1'. Weights w10=0.0, w11=0.0, and w12=1.0 are shown on the connections. The output is Y1=1.0. An arrow labeled...
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-fe7304192caf64cda93b580c5e7e5c06_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single neuron representing a perceptron.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-376f80eb8a41369e87da63a0210d173e_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single neuron representing a perceptron.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-e2c120be98ede6deb60dd341f5a9803b_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single neuron (perceptron) with two inputs (x1, x2) and a bias (x0=1).
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-5e9af8986a5845504f251d3079da8078_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single neuron (perceptron) with two inputs (x1, x2) and a bias (x0=1).
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-c649cad02e45d7d9a16f3f5bdb332219_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single neuron (perceptron) with two inputs (x1, x2) and a bias (x0=1).
<!-- /IMAGE_DESCRIPTION -->
### Simulando uma Rede Perceptron

- **Pesos atuais:**  $w_{10} = -1.0, w_{11} = 0.0, w_{12} = 0.0$
- **limiar:**  $Q(v_k) = \begin{cases} 1 & \text{se } v_k \geq 0 \\ 0 & \text{caso contrário} \end{cases}$ , taxa de aprendizagem:  $\eta = 1$

| x1 | x2 | d |
|----|----|---|
| 0  | 0  | 0 |
| 0  | 1  | 1 |
| 1  | 0  | 1 |
| 1  | 1  | 1 |

Diagram illustrating the propagation step of a perceptron. The input nodes are  $x_0 = 1$  (bias),  $x_1$ , and  $x_2$ . The weights are  $w_{10} = -1.0$ ,  $w_{11} = 0.0$ , and  $w_{12} = 0.0$ . The summation node is labeled '1'. The output is  $y_1 = 0.0$ . An arrow labeled 'propagação' points to the right.

Diagram of a single-layer perceptron. It shows an input node x0=1 (bias) and two input nodes x1 and x2. The weights are w10=-1.0, w11=0.0, and w12=0.0. The summation node is labeled '1'. The output is y1=0.0. An arrow labeled 'propagação' points to the right.

- $v_1 = x_0 \times w_{10} + x_1 \times w_{11} + x_2 \times w_{12}$
- $v_1 = 1 \times -1.0 + 0 \times 0.0 + 1 \times 0.0 = -1.0$
- $y_1 = Q(v_1) = Q(-1.0) = 0.0$

- **Ajuste dos pesos (Aplicando a regra delta)**

- $erro_1 = d_1 - y_1 = 1 - 0.0 = 1.0$
- $w_{10} = w_{10} + \eta \times erro_1 \times x_0 = -1.0 + 1 \times 1.0 \times 1 = 0.0$
- $w_{11} = w_{11} + \eta \times erro_1 \times x_1 = 0.0 + 1 \times 1.0 \times 0 = 0.0$
- $w_{12} = w_{12} + \eta \times erro_1 \times x_2 = 0.0 + 1 \times 1.0 \times 1 = 1.0$

{48}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-a003ffe7299e0a48bceb7f1e45a4f1a3_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single-layer perceptron. It shows an input node x0=1 (bias) and two input nodes x1 and x2. The weights are w10=-1.0, w11=0.0, and w12=0.0. The summation node is labeled '1'. The output is y1=0.0. An arrow...
<!-- /IMAGE_DESCRIPTION -->
### Simulando uma Rede Perceptron

- Pesos atuais:  $w_{10} = 0.0, w_{11} = 0.0, w_{12} = 1.0$

- limiar:  $Q(v_k) = \begin{cases} 1 & \text{se } v_k \geq 0 \\ 0 & \text{caso contrário} \end{cases}$ , taxa de aprendizagem:  $\eta = 1$

| x1 | x2 | d |
|----|----|---|
| 0  | 0  | 0 |
| 0  | 1  | 1 |
| 1  | 0  | 1 |
| 1  | 1  | 1 |

The diagram illustrates a single neuron (perceptron) with three inputs:  $x_0 = 1$  (bias),  $x_1$ , and  $x_2$ . The weights connecting these inputs to the neuron are  $w_{10} = 0.0$ ,  $w_{11} = 0.0$ , and  $w_{12} = 1.0$ . The neuron's output is  $y_1 = 1.0$ . An arrow labeled "propagação" (propagation) points from the input table to the neuron diagram.

Diagram of a perceptron neuron. Inputs x0=1 (bias), x1, and x2 are shown. Weights w10=0.0, w11=0.0, and w12=1.0 are indicated. The neuron calculates v1 and outputs y1=1.0. An arrow labeled 'propagação' points from the input table to the neuron diagram.

- $v_1 = x_0 \times w_{10} + x_1 \times w_{11} + x_2 \times w_{12}$

- $v_1 = 1 \times 0.0 + 1 \times 0.0 + 0 \times 1.0 = 0.0$

- $y_1 = Q(v_1) = Q(0.0) = 1.0$

- Ajuste dos pesos (Aplicando a regra delta)

- $erro_1 = d_1 - y_1 = 1 - 1.0 = 0.0$

- quando o erro é zero, não há ajuste de pesos.

{49}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-0f1767577a073167eb9628d72034e083_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a perceptron neuron. Inputs x0=1 (bias), x1, and x2 are shown. Weights w10=0.0, w11=0.0, and w12=1.0 are indicated. The neuron calculates v1 and outputs y1=1.0. An arrow labeled 'propagação' points from the...
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-fb4274c4b7882a4059103f1dbca9b111_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a perceptron neuron. Inputs x0=1 (bias), x1, and x2 are shown. Weights w10=0.0, w11=0.0, and w12=1.0 are indicated. The neuron calculates v1 and outputs y1=1.0. An arrow labeled 'propagação' points to the...
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-bccc028d0e75bc30c41528056f581545_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a perceptron neuron. Inputs x0=1 (bias), x1=0, and x2=1 are shown. Weights w10=-1.0, w11=0.0, and w12=1.0 are indicated. The neuron calculates v1 = 0.0 and outputs y1 = 1.0. An arrow labeled 'propagação'...
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-03d9aaba6c1af8bfd8e42c1d2422ae5c_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a perceptron neuron. Inputs x0=1 (bias), x1, and x2 are shown. Weights w10=-1.0, w11=1.0, and w12=1.0 are indicated. The neuron calculates v1 and outputs y1=1.0. An arrow labeled 'propagação' points to the...
<!-- /IMAGE_DESCRIPTION -->
### Simulando uma Rede Perceptron

- Pesos atuais:  $w_{10} = 0.0, w_{11} = 0.0, w_{12} = 1.0$

- limiar:  $Q(v_k) = \begin{cases} 1 & \text{se } v_k \geq 0 \\ 0 & \text{caso contrário} \end{cases}$ , taxa de aprendizagem:  $\eta = 1$

| x1 | x2 | d |
|----|----|---|
| 0  | 0  | 0 |
| 0  | 1  | 1 |
| 1  | 0  | 1 |
| 1  | 1  | 1 |

Diagram illustrating the propagation step of a perceptron. The neuron receives three inputs:  $x_0 = 1$  (bias),  $x_1$ , and  $x_2$ . The weights connecting these inputs are  $w_{10} = 0.0$ ,  $w_{11} = 0.0$ , and  $w_{12} = 1.0$ . The neuron's output is  $Y_1 = 1.0$ . An arrow labeled "propagação" indicates the flow of information.

Diagram of a perceptron neuron. It shows inputs x0=1 (bias), x1, and x2 entering a neuron node labeled '1'. Weights w10=0.0, w11=0.0, and w12=1.0 are shown on the connections. The output is Y1=1.0. An arrow labeled 'propagação' points to the right.

- $v_1 = x_0 \times w_{10} + x_1 \times w_{11} + x_2 \times w_{12}$

- $v_1 = 1 \times 0.0 + 1 \times 0.0 + 1 \times 1.0 = 1.0$

- $y_1 = Q(v_1) = Q(1.0) = 1.0$

- Ajuste dos pesos (Aplicando a regra delta)

- $erro_1 = d_1 - y_1 = 1 - 1.0 = 0.0$

- quando o erro é zero, não há ajuste de pesos.

{50}------------------------------------------------
### Simulando uma Rede Perceptron

- Erro Acumulado para época 1 :
  - Erro Geral:
    - $= \text{abs}(\text{erroEntrada1}) + \text{abs}(\text{erroEntrada2}) + \text{abs}(\text{erroEntrada3}) + \text{abs}(\text{erroEntrada4}) =$
    - $= \text{abs}(-1.0) + \text{abs}(1.0) + \text{abs}(0.0) + \text{abs}(0.0)$
    - $= 2.0$
- Como ainda há erro, o algoritmo prossegue ...

{51}------------------------------------------------
### Simulando uma Rede Perceptron

- Pesos atuais:  $w_{10} = 0.0, w_{11} = 0.0, w_{12} = 1.0$

- limiar:  $Q(v_k) = \begin{cases} 1 & \text{se } v_k \geq 0 \\ 0 & \text{caso contrário} \end{cases}$ , taxa de aprendizagem:  $\eta = 1$

| x1 | x2 | d |
|----|----|---|
| 0  | 0  | 0 |
| 0  | 1  | 1 |
| 1  | 0  | 1 |
| 1  | 1  | 1 |

Diagram of a perceptron neuron. The neuron is represented by a circle containing the number 1. Inputs  $x_0=1$  (bias),  $x_1$ , and  $x_2$  are shown with arrows pointing to the neuron. Weights  $w_{10}=0.0$ ,  $w_{11}=0.0$ , and  $w_{12}=1.0$  are indicated next to the input arrows. The output  $y_1=1.0$  is shown with an arrow pointing away from the neuron. A horizontal arrow labeled "propagação" points to the right.

Diagram of a perceptron neuron. Inputs x0=1 (bias), x1, and x2 are shown. Weights w10=0.0, w11=0.0, and w12=1.0 are indicated. The neuron calculates v1 and outputs y1=1.0. An arrow labeled 'propagação' points to the right.

- $v_1 = x_0 \times w_{10} + x_1 \times w_{11} + x_2 \times w_{12}$

- $v_1 = 0 \times 0.0 + 0 \times 1.0 + 1 \times 0.0 = 0.0$

- $y_1 = Q(v_1) = Q(0.0) = 1.0$

- Ajuste dos pesos (Aplicando a regra delta)

- $erro_1 = d_1 - y_1 = 0 - 1.0 = -1.0$

- $w_{10} = w_{10} + \eta \times erro_1 \times x_0 = 0.0 + 1 \times -1.0 \times 1 = -1.0$

- $w_{11} = w_{11} + \eta \times erro_1 \times x_1 = 0.0 + 1 \times -1.0 \times 0 = 0.0$

- $w_{12} = w_{12} + \eta \times erro_1 \times x_2 = 1.0 + 1 \times -1.0 \times 0 = 1.0$

{52}------------------------------------------------
### Simulando uma Rede Perceptron

- **Pesos atuais:**  $w_{10} = -1.0, w_{11} = 0.0, w_{12} = 1.0$

- **limiar:**  $Q(v_k) = \begin{cases} 1 & \text{se } v_k \geq 0 \\ 0 & \text{caso contrário} \end{cases}$ , taxa de aprendizagem:  $\eta = 1$

| x1       | x2       | d        |
|----------|----------|----------|
| 0        | 0        | 0        |
| <b>0</b> | <b>1</b> | <b>1</b> |
| 1        | 0        | 1        |
| 1        | 1        | 1        |

Diagram illustrating the propagation step for the second row of the input table (x1=0, x2=1, d=1). The neuron receives inputs x0=1 (bias), x1=0, and x2=1. The weights are w10=-1.0, w11=0.0, and w12=1.0. The neuron calculates the weighted sum v1 = 0.0 and outputs y1 = 1.0. An arrow labeled 'propagação' points from the input table to the diagram.

Diagram of a perceptron neuron. Inputs x0=1 (bias), x1=0, and x2=1 are shown. Weights w10=-1.0, w11=0.0, and w12=1.0 are indicated. The neuron calculates v1 = 0.0 and outputs y1 = 1.0. An arrow labeled 'propagação' points from the input table to the diagram.

- $v_1 = x_0 \times w_{10} + x_1 \times w_{11} + x_2 \times w_{12}$

- $v_1 = 1 \times -1.0 + 0 \times 0.0 + 1 \times 1.0 = 0.0$

- $y_1 = Q(v_1) = Q(0.0) = 1.0$

- Ajuste dos pesos (Aplicando a regra delta)

- $erro_1 = d_1 - y_1 = 1 - 1.0 = 0.0$

- quando o erro é zero, não há ajuste de pesos.

{53}------------------------------------------------
### Simulando uma Rede Perceptron

- **Pesos atuais:**  $w_{10} = -1.0, w_{11} = 0.0, w_{12} = 1.0$

- **limiar:**  $Q(v_k) = \begin{cases} 1 & \text{se } v_k \geq 0 \\ 0 & \text{caso contrário} \end{cases}$ , taxa de aprendizagem:  $\eta = 1$

| x1 | x2 | d |
|----|----|---|
| 0  | 0  | 0 |
| 0  | 1  | 1 |
| 1  | 0  | 1 |
| 1  | 1  | 1 |

The diagram illustrates a single neuron (perceptron) with three inputs:  $x_0 = 1$  (bias),  $x_1$ , and  $x_2$ . The weights connecting these inputs to the neuron are  $w_{10} = -1.0$ ,  $w_{11} = 0.0$ , and  $w_{12} = 1.0$ . The neuron's output is  $y_1 = 0.0$ . An arrow labeled "propagação" points from the input table to the diagram.

Diagram of a single neuron (perceptron) showing inputs x0=1, x1, and x2 with weights w10=-1.0, w11=0.0, and w12=1.0 respectively. The neuron is represented by a circle with '1' inside, and its output is y1=0.0. An arrow labeled 'propagação' points from the input table to the diagram.

- $v_1 = x_0 \times w_{10} + x_1 \times w_{11} + x_2 \times w_{12}$

- $v_1 = 1 \times -1.0 + 1 \times 0.0 + 0 \times 1.0 = -1.0$

- $y_1 = Q(v_1) = Q(-1.0) = 0.0$

- Ajuste dos pesos (Aplicando a regra delta)

- $erro_1 = d_1 - y_1 = 1 - 0.0 = 1.0$

- $w_{10} = w_{10} + \eta \times erro_1 \times x_0 = -1.0 + 1 \times 1.0 \times 1 = 0.0$

- $w_{11} = w_{11} + \eta \times erro_1 \times x_1 = 0.0 + 1 \times 1.0 \times 1 = 1.0$

- $w_{12} = w_{12} + \eta \times erro_1 \times x_2 = 1.0 + 1 \times 1.0 \times 0 = 1.0$

{54}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-195611c20b2dc7ed0fa3033392e22908_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single neuron (perceptron) showing inputs x0=1, x1, and x2 with weights w10=-1.0, w11=0.0, and w12=1.0 respectively.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-0a06de972d61ab9bb901bd74dd4ff51f_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single neuron (perceptron) showing inputs x0=1, x1, and x2 with weights w10=0.0, w11=1.0, and w12=1.0 respectively.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-1f1614411edea7edfc86c839a608e1fc_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single neuron (perceptron) showing inputs x0=1, x1, and x2 with weights w10=-1.0, w11=1.0, and w12=1.0 respectively.
<!-- /IMAGE_DESCRIPTION -->
### Simulando uma Rede Perceptron

- Pesos atuais:  $w_{10} = 0.0, w_{11} = 1.0, w_{12} = 1.0$

- limiar:  $Q(v_k) = \begin{cases} 1 & \text{se } v_k \geq 0 \\ 0 & \text{caso contrário} \end{cases}$ , taxa de aprendizagem:  $\eta = 1$

| x1 | x2 | d |
|----|----|---|
| 0  | 0  | 0 |
| 0  | 1  | 1 |
| 1  | 0  | 1 |
| 1  | 1  | 1 |

The diagram illustrates a single neuron (perceptron) with three inputs: a bias term  $x_0 = 1$ , and two data inputs  $x_1$  and  $x_2$ . The neuron is represented by a circle containing the number '1'. Arrows from each input point to the neuron, labeled with their respective weights:  $w_{10} = 0.0$  for the bias,  $w_{11} = 1.0$  for  $x_1$ , and  $w_{12} = 1.0$  for  $x_2$ . The output of the neuron is labeled  $y_1 = 1.0$ . To the left of the inputs, there are red '1's next to  $x_1$  and  $x_2$ . A horizontal arrow labeled 'propagação' (propagation) points to the right, indicating the flow of information.

Diagram of a single neuron representing a perceptron. It shows inputs x0=1 (bias), x1, and x2 connected to a neuron node labeled '1'. Weights w10=0.0, w11=1.0, and w12=1.0 are shown. The output is y1=1.0. An arrow labeled 'propagação' points to the right.

- $v_1 = x_0 \times w_{10} + x_1 \times w_{11} + x_2 \times w_{12}$

- $v_1 = 1 \times 0.0 + 1 \times 1.0 + 1 \times 1.0 = 2.0$

- $y_1 = Q(v_1) = Q(2.0) = 1.0$

- Ajuste dos pesos (Aplicando a regra delta)

- $erro_1 = d_1 - y_1 = 1 - 1.0 = 0.0$

- quando o erro é zero, não há ajuste de pesos.

{55}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-0f6e3cdce0f01d6ccceabcced508bb5b_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single neuron (perceptron) with two inputs (x1, x2) and a bias term (x0=1).
<!-- /IMAGE_DESCRIPTION -->
### Simulando uma Rede Perceptron

- Erro Acumulado para época 2 :
  - Erro Geral:
    - $= \text{abs}(\text{erroEntrada1}) + \text{abs}(\text{erroEntrada2}) + \text{abs}(\text{erroEntrada3}) + \text{abs}(\text{erroEntrada4}) =$
    - $= \text{abs}(-1.0) + \text{abs}(0.0) + \text{abs}(1.0) + \text{abs}(0.0)$
    - $= 2.0$
- Como ainda há erro, o algoritmo prossegue ...

{56}------------------------------------------------
### Simulando uma Rede Perceptron

- **Pesos atuais:**  $w_{10} = 0.0, w_{11} = 1.0, w_{12} = 1.0$

- **limiar:**  $Q(v_k) = \begin{cases} 1 & \text{se } v_k \geq 0 \\ 0 & \text{caso contrário} \end{cases}$  , taxa de aprendizagem:  $\eta = 1$

| x1 | x2 | d |
|----|----|---|
| 0  | 0  | 0 |
| 0  | 1  | 1 |
| 1  | 0  | 1 |
| 1  | 1  | 1 |

The diagram illustrates a single neuron (perceptron) with three inputs:  $x_0 = 1$  (bias),  $x_1$ , and  $x_2$ . The weights connecting these inputs to the neuron are  $w_{10} = 0.0$ ,  $w_{11} = 1.0$ , and  $w_{12} = 1.0$ . The neuron's output is  $Y_1 = 1.0$ . An arrow labeled "propagação" (propagation) points from the input table to the neuron diagram.

Diagram of a single neuron (perceptron) showing inputs x0=1, x1, and x2 with weights w10=0.0, w11=1.0, and w12=1.0 respectively. The neuron is represented by a circle with '1' inside, and its output is Y1=1.0. An arrow labeled 'propagação' points from the input table to the neuron diagram.

- $v_1 = x_0 \times w_{10} + x_1 \times w_{11} + x_2 \times w_{12}$

- $v_1 = 1 \times 0.0 + 0 \times 1.0 + 0 \times 1.0 = 0.0$

- $y_1 = Q(v_1) = Q(0.0) = 1.0$

- Ajuste dos pesos (Aplicando a regra delta)

- $erro_1 = d_1 - y_1 = 0 - 1.0 = -1.0$

- $w_{10} = w_{10} + \eta \times erro_1 \times x_0 = 0.0 + 1 \times -1.0 \times 1 = -1.0$

- $w_{11} = w_{11} + \eta \times erro_1 \times x_1 = 1.0 + 1 \times -1.0 \times 0 = 1.0$

- $w_{12} = w_{12} + \eta \times erro_1 \times x_2 = 1.0 + 1 \times -1.0 \times 0 = 1.0$

{57}------------------------------------------------
### Simulando uma Rede Perceptron

- **Pesos atuais:**  $w_{10} = -1.0, w_{11} = 1.0, w_{12} = 1.0$

- **limiar:**  $Q(v_k) = \begin{cases} 1 & \text{se } v_k \geq 0 \\ 0 & \text{caso contrário} \end{cases}$  , taxa de aprendizagem:  $\eta = 1$

| x1 | x2 | d |
|----|----|---|
| 0  | 0  | 0 |
| 0  | 1  | 1 |
| 1  | 0  | 1 |
| 1  | 1  | 1 |

Diagram of a perceptron neuron. It shows an input layer with x0=1 (bias), x1, and x2. The neuron is represented by a circle with '1' inside. Arrows from x0, x1, and x2 point to the neuron with weights w10=-1.0, w11=1.0, and w12=1.0 respectively. The output is y1=1.0. A table to the left shows input data. An arrow labeled 'propagação' points from the table to the neuron.

- $v_1 = x_0 \times w_{10} + x_1 \times w_{11} + x_2 \times w_{12}$

- $v_1 = 1 \times -1.0 + 0 \times 1.0 + 1 \times 1.0 = 0.0$

- $y_1 = Q(v_1) = Q(0.0) = 1.0$

- Ajuste dos pesos (Aplicando a regra delta)

- $erro_1 = d_1 - y_1 = 1 - 1.0 = 0.0$

- quando o erro é zero, não há ajuste de pesos.

{58}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-e417ae35ab07134888be901c201d54cd_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a perceptron neuron. It shows an input layer with x0=1 (bias), x1, and x2. The neuron is represented by a circle with '1' inside. Arrows from x0, x1, and x2 point to the neuron with weights w10=-1.0...
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-212c50c4e3d043c989037a01e13c1a98_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a perceptron neuron. It shows an input layer with x0=1 (bias), x1, and x2. The neuron is represented by a circle with '1' inside. Arrows from x0, x1, and x2 point to the neuron with weights w10 = -1.0, w11 =...
<!-- /IMAGE_DESCRIPTION -->
### Simulando uma Rede Perceptron

- **Pesos atuais:**  $w_{10} = -1.0, w_{11} = 1.0, w_{12} = 1.0$

- **limiar:**  $Q(v_k) = \begin{cases} 1 & \text{se } v_k \geq 0 \\ 0 & \text{caso contrário} \end{cases}$ , taxa de aprendizagem:  $\eta = 1$

| x1       | x2       | d        |
|----------|----------|----------|
| 0        | 0        | 0        |
| 0        | 1        | 1        |
| <b>1</b> | <b>0</b> | <b>1</b> |
| 1        | 1        | 1        |

Diagram illustrating the propagation step of a perceptron. The neuron receives three inputs:  $x_0 = 1$  (bias),  $x_1$ , and  $x_2$ . The weights are  $w_{10} = -1.0$ ,  $w_{11} = 1.0$ , and  $w_{12} = 1.0$ . The neuron is currently processing the input vector  $(1, 0)$  (where  $x_1=1, x_2=0$ ), resulting in an output  $y_1 = 1.0$ . An arrow labeled "propagação" indicates the flow of information.

Diagram of a perceptron neuron. Inputs x0=1 (bias), x1, and x2 are shown. Weights w10=-1.0, w11=1.0, and w12=1.0 are indicated. The neuron calculates v1 and outputs y1=1.0. An arrow labeled 'propagação' points to the right.

- $v_1 = x_0 \times w_{10} + x_1 \times w_{11} + x_2 \times w_{12}$
- $v_1 = 1 \times -1.0 + 1 \times 1.0 + 0 \times 1.0 = 0.0$
- $y_1 = Q(v_1) = Q(0.0) = 1.0$

- Ajuste dos pesos (Aplicando a regra delta)

- $erro_1 = d_1 - y_1 = 1 - 1.0 = 0.0$
- quando o erro é zero, não há ajuste de pesos.

{59}------------------------------------------------
### Simulando uma Rede Perceptron

- Pesos atuais:  $w_{10} = -1.0, w_{11} = 1.0, w_{12} = 1.0$

- limiar:  $Q(v_k) = \begin{cases} 1 & \text{se } v_k \geq 0 \\ 0 & \text{caso contrário} \end{cases}$ , taxa de aprendizagem:  $\eta = 1$

| x1 | x2 | d |
|----|----|---|
| 0  | 0  | 0 |
| 0  | 1  | 1 |
| 1  | 0  | 1 |
| 1  | 1  | 1 |

Diagram illustrating the propagation step for the input (1, 1, 1). The neuron receives inputs  $x_0=1$  (bias),  $x_1=1$ , and  $x_2=1$ . The weights are  $w_{10}=-1.0$ ,  $w_{11}=1.0$ , and  $w_{12}=1.0$ . The output is  $Y_1=1.0$ .

Diagram of a single-layer perceptron neuron. Inputs x0=1 (bias), x1, and x2 are shown. Weights w10=-1.0, w11=1.0, and w12=1.0 connect these inputs to the neuron. The neuron's output is Y1=1.0. An arrow labeled 'propagação' points from the input table to the neuron diagram.

- $v_1 = x_0 \times w_{10} + x_1 \times w_{11} + x_2 \times w_{12}$

- $v_1 = 1 \times -1.0 + 1 \times 1.0 + 1 \times 1.0 = 1.0$

- $y_1 = Q(v_1) = Q(1.0) = 1.0$

- Ajuste dos pesos (Aplicando a regra delta)

- $\text{erro}_1 = d_1 - y_1 = 1 - 1.0 = 0.0$

- quando o erro é zero, não há ajuste de pesos.

<!-- DATALAB_CHUNK 4: pages 61-77 -->

{60}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-efbdfb3d9d5a7a7782ef29e131f9f280_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single-layer perceptron neuron.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-30387053b5b3fede6873f6a46a9ca4a9_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a perceptron neuron. Inputs x0=1, x1, and x2 are shown. Weights w10=-1.0, w11=1.0, and w12=1.0 connect these inputs to the neuron. The output is Y1=1.0. An arrow labeled 'propagação' points from the input...
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-db39acbd11df5eb7e79ab84562fb8f74_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single-layer perceptron neuron.
<!-- /IMAGE_DESCRIPTION -->
#### Simulando uma Rede Perceptron

- Erro Acumulado para época 3 :
  - Erro Geral:
    - $= \text{abs}(\text{erroEntrada1}) + \text{abs}(\text{erroEntrada2}) + \text{abs}(\text{erroEntrada3}) + \text{abs}(\text{erroEntrada4}) =$
    - $= \text{abs}(-1.0) + \text{abs}(0.0) + \text{abs}(0.0) + \text{abs}(0.0)$
    - $= 1.0$
- Como ainda há erro, o algoritmo prossegue ...

{61}------------------------------------------------
#### Simulando uma Rede Perceptron

- Pesos atuais:  $w_{10} = -1.0, w_{11} = 1.0, w_{12} = 1.0$

- limiar:  $Q(v_k) = \begin{cases} 1 & \text{se } v_k \geq 0 \\ 0 & \text{caso contrário} \end{cases}$ , taxa de aprendizagem:  $\eta = 1$

| x1 | x2 | d |
|----|----|---|
| 0  | 0  | 0 |
| 0  | 1  | 1 |
| 1  | 0  | 1 |
| 1  | 1  | 1 |

Diagram of a perceptron neuron. It shows an input layer with x0=1 (bias), x1, and x2. The neuron is represented by a circle with '1' inside. Arrows from x0, x1, and x2 point to the neuron with weights w10 = -1.0, w11 = 1.0, and w12 = 1.0 respectively. The output is Y1 = 0.0. A horizontal arrow labeled 'propagação' points to the right.

- $v_1 = x_0 \times w_{10} + x_1 \times w_{11} + x_2 \times w_{12}$
- $v_1 = 1 \times -1.0 + 0 \times 1.0 + 0 \times 1.0 = -1.0$
- $y_1 = Q(v_1) = Q(-1.0) = 0.0$

- Ajuste dos pesos (Aplicando a regra delta)

- $erro_1 = d_1 - y_1 = 0 - 0.0 = 0.0$

- quando o erro é zero, não há ajuste de pesos.

{62}------------------------------------------------
#### Simulando uma Rede Perceptron

- Pesos atuais:  $w_{10} = -1.0, w_{11} = 1.0, w_{12} = 1.0$

- limiar:  $Q(v_k) = \begin{cases} 1 & \text{se } v_k \geq 0 \\ 0 & \text{caso contrário} \end{cases}$ , taxa de aprendizagem:  $\eta = 1$

| x1 | x2 | d |
|----|----|---|
| 0  | 0  | 0 |
| 0  | 1  | 1 |
| 1  | 0  | 1 |
| 1  | 1  | 1 |

The diagram illustrates a single neuron (perceptron) with three inputs:  $x_0 = 1$  (bias),  $x_1$ , and  $x_2$ . The weights connecting these inputs to the neuron are  $w_{10} = -1.0$ ,  $w_{11} = 1.0$ , and  $w_{12} = 1.0$ . The neuron's output is  $y_1 = 1.0$ . An arrow labeled "propagação" points from the input table to the diagram.

Diagram of a single neuron representing a perceptron. Inputs x0=1 (bias), x1, and x2 are shown. Weights w10=-1.0, w11=1.0, and w12=1.0 are indicated. The neuron's output is y1=1.0. An arrow labeled 'propagação' points from the input table to the diagram.

- $v_1 = x_0 \times w_{10} + x_1 \times w_{11} + x_2 \times w_{12}$

- $v_1 = 1 \times -1.0 + 0 \times 1.0 + 1 \times 1.0 = 0.0$

- $y_1 = Q(v_1) = Q(0.0) = 1.0$

- Ajuste dos pesos (Aplicando a regra delta)

- $erro_1 = d_1 - y_1 = 1 - 1.0 = 0.0$

- quando o erro é zero, não há ajuste de pesos.

{63}------------------------------------------------
#### Simulando uma Rede Perceptron

- Pesos atuais:  $w_{10} = -1.0, w_{11} = 1.0, w_{12} = 1.0$

- limiar:  $Q(v_k) = \begin{cases} 1 & \text{se } v_k \geq 0 \\ 0 & \text{caso contrário} \end{cases}$ , taxa de aprendizagem:  $\eta = 1$

| x1 | x2 | d |
|----|----|---|
| 0  | 0  | 0 |
| 0  | 1  | 1 |
| 1  | 0  | 1 |
| 1  | 1  | 1 |

The diagram illustrates a single neuron (perceptron) with three inputs:  $x_0 = 1$  (bias),  $x_1$ , and  $x_2$ . The weights connecting these inputs to the neuron are  $w_{10} = -1.0$ ,  $w_{11} = 1.0$ , and  $w_{12} = 1.0$ . The neuron's output is  $y_1 = 1.0$ . An arrow labeled "propagação" points from the input table to the diagram.

Diagram of a single neuron (perceptron) showing inputs x0=1, x1, and x2 with weights w10=-1.0, w11=1.0, and w12=1.0 respectively. The neuron is represented by a circle with a '1' inside, and its output is y1=1.0. An arrow labeled 'propagação' points from the input table to the diagram.

- $v_1 = x_0 \times w_{10} + x_1 \times w_{11} + x_2 \times w_{12}$

- $v_1 = 1 \times -1.0 + 1 \times 1.0 + 0 \times 1.0 = 0.0$

- $y_1 = Q(v_1) = Q(0.0) = 1.0$

- Ajuste dos pesos (Aplicando a regra delta)

- $erro_1 = d_1 - y_1 = 1 - 1.0 = 0.0$

- quando o erro é zero, não há ajuste de pesos.

{64}------------------------------------------------
#### Simulando uma Rede Perceptron

- Pesos atuais:  $w_{10} = -1.0, w_{11} = 1.0, w_{12} = 1.0$

- limiar:  $Q(v_k) = \begin{cases} 1 & \text{se } v_k \geq 0 \\ 0 & \text{caso contrário} \end{cases}$ , taxa de aprendizagem:  $\eta = 1$

| x1 | x2 | d |
|----|----|---|
| 0  | 0  | 0 |
| 0  | 1  | 1 |
| 1  | 0  | 1 |
| 1  | 1  | 1 |

Diagram illustrating the propagation step of a perceptron. The neuron receives inputs  $x_0=1$ ,  $x_1$ , and  $x_2$  with weights  $w_{10}=-1.0$ ,  $w_{11}=1.0$ , and  $w_{12}=1.0$  respectively. The output is  $Y_1=1.0$ . An arrow labeled "propagação" points from the input table to the diagram.

Diagram of a perceptron neuron. Inputs x0=1, x1, and x2 are shown. Weights w10=-1.0, w11=1.0, and w12=1.0 connect these inputs to the neuron. The output is Y1=1.0. An arrow labeled 'propagação' points from the input table to the diagram.

- $v_1 = x_0 \times w_{10} + x_1 \times w_{11} + x_2 \times w_{12}$

- $v_1 = 1 \times -1.0 + 1 \times 1.0 + 1 \times 1.0 = 1.0$

- $y_1 = Q(v_1) = Q(1.0) = 1.0$

- Ajuste dos pesos (Aplicando a regra delta)

- $erro_1 = d_1 - y_1 = 1 - 1.0 = 0.0$

- quando o erro é zero, não há ajuste de pesos.

{65}------------------------------------------------
#### Simulando uma Rede Perceptron

- Erro Acumulado para época 4 :
  - Erro Geral:
    - $= \text{abs}(\text{erroEntrada1}) + \text{abs}(\text{erroEntrada2}) + \text{abs}(\text{erroEntrada3}) + \text{abs}(\text{erroEntrada4}) =$
    - $= \text{abs}(0.0) + \text{abs}(0.0) + \text{abs}(0.0) + \text{abs}(0.0)$
    - $= 0.0$
  - O algoritmo pára.
- Resultado:
  - O algoritmo encontrou os pesos adequados:  
 $w_{10} = -1.0, w_{11} = 1.0, w_{12} = 1.0$

{66}------------------------------------------------
#### Simulando uma Rede PerceptronFase de Generalização

- A rede está pronta para ser testada (ou usada).

- 1 Carrega-se, na topologia da rede, os pesos encontrados na fase de treinamento.

Diagram of a single-layer perceptron network. It features a central blue circular node labeled '1'. To its left are two input nodes, 'x1' and 'x2', each preceded by a red question mark. Arrows point from 'x1' and 'x2' to the central node, labeled with weights  $w_{11} = 1.0$  and  $w_{12} = 1.0$  respectively. Above the central node is a bias input  $x_0 = 1$  with an arrow pointing down to the node, labeled with weight  $w_{10} = -1.0$ . An arrow points from the central node to an output node labeled  $Y_1$ . Below the diagram, a horizontal arrow points to the right, labeled 'propagação'.

Diagram of a single-layer perceptron network. It features a central blue circular node labeled '1'. To its left are two input nodes, 'x1' and 'x2', each preceded by a red question mark. Arrows point from 'x1' and 'x2' to the central node, labeled with weights 'w11 = 1.0' and 'w12 = 1.0' respectively. Above the central node is a bias input 'x0 = 1' with an arrow pointing down to the node, labeled with weight 'w10 = -1.0'. An arrow points from the central node to an output node labeled 'Y1'. Below the diagram, a horizontal arrow points to the right, labeled 'propagação'.

**Modelo** = Corresponde a uma instancia do Algoritmo de IA gerada a partir dos dados de treinamento

- 2 Esta fase implementa apenas a propagação. Informa-se novos valores para as entradas e a rede gera a saída correspondente.

{67}------------------------------------------------
#### Simulando uma Rede PerceptronFase de Generalização

Testando o modelo:

| x1 | x2 |
|----|----|
| 0  | 0  |
| 0  | 1  |
| 1  | 0  |
| 1  | 1  |

Diagram of a single-layer perceptron neuron. Inputs  $x_1$  and  $x_2$  are shown with question marks. Weights  $w_{11}=1.0$ ,  $w_{12}=1.0$ , and bias  $w_{10}=-1.0$  are indicated. The neuron is labeled 1 and outputs  $Y_1$ . A horizontal arrow labeled "propagação" points to the right.

Diagram of a single-layer perceptron neuron. Inputs x1 and x2 are shown with question marks. Weights w11=1.0, w12=1.0, and bias w10=-1.0 are indicated. The neuron is labeled 1 and outputs Y1. A horizontal arrow labeled 'propagação' points to the right.

$$v_j = \sum_{i=0}^n (x_i \times w_{ij})$$

$$y_j = f(v_j)$$

Função de ativação - Limiar

$$f(v_j) = \begin{cases} 1 \text{ se } v_j \geq 0 \\ 0 \text{ se } v_j < 0 \end{cases}$$

{68}------------------------------------------------
### Simulando uma Rede Perceptron Fase de Generalização

Testando o modelo:

|   | x1 | x2 |
|---|----|----|
| → | 0  | 0  |
|   | 0  | 1  |
|   | 1  | 0  |
|   | 1  | 1  |

Diagram of a single neuron (perceptron) with two inputs ( $x_1, x_2$ ) and a bias ( $x_0 = 1$ ). The neuron is labeled '1' inside a circle. Weights are  $w_{11} = 1.0$ ,  $w_{12} = 1.0$ , and  $w_{10} = -1.0$ . The output is  $Y_1$ . An arrow labeled 'propagação' points to the right.

Diagram of a single neuron (perceptron) with two inputs (x1, x2) and a bias (x0=1). The neuron is labeled '1' inside a circle. Weights are w11=1.0, w12=1.0, and w10=-1.0. The output is Y1. An arrow labeled 'propagação' points to the right.

$$\begin{aligned}
 v_1 &= 1 \times -1.0 + \\
 &\quad 0 \times 1.0 \\
 &\quad 0 \times 1.0 \\
 &= -1 \\
 Y_1 &= Q(-1) = \mathbf{0}
 \end{aligned}$$

$$v_j = \sum_{i=0}^n (x_i \times w_{ij})$$

$$y_j = f(v_j)$$

Função de ativação - Limiar

$$f(v_j) = \begin{cases} 1 & \text{se } v_j \geq 0 \\ 0 & \text{se } v_j < 0 \end{cases}$$

{69}------------------------------------------------
#### Simulando uma Rede Perceptron Fase de Generalização

Testando o modelo:

| x1 | x2 |
|----|----|
| 0  | 0  |
| 0  | 1  |
| 1  | 0  |
| 1  | 1  |

Diagram of a single neuron (perceptron) with two inputs ( $x_1, x_2$ ) and a bias term ( $x_0 = 1$ ). The weights are  $w_{11} = 1.0$ ,  $w_{12} = 1.0$ , and  $w_{10} = -1.0$ . The output is  $Y_1$ . The diagram shows the propagation of inputs through the neuron.

Diagram of a single neuron (perceptron) with two inputs (x1, x2) and a bias term (x0=1). The weights are w11=1.0, w12=1.0, and w10=-1.0. The output is Y1. The diagram shows the propagation of inputs through the neuron.

$$\begin{aligned}
 v_1 &= 1 \times -1.0 + \\
 &\quad 0 \times 1.0 \\
 &\quad 1 \times 1.0 \\
 &= 0 \\
 Y_1 &= Q(0) = \mathbf{1}
 \end{aligned}$$

$$v_j = \sum_{i=0}^n (x_i \times w_{ij})$$

$$y_j = f(v_j)$$

Função de ativação - Limiar

$$f(v_j) = \begin{cases} 1 \text{ se } v_j \geq 0 \\ 0 \text{ se } v_j < 0 \end{cases}$$

{70}------------------------------------------------
### Simulando uma Rede Perceptron Fase de Generalização

Testando o modelo:

| x1 | x2 |
|----|----|
| 0  | 0  |
| 0  | 1  |
| 1  | 0  |
| 1  | 1  |

Diagram of a single neuron (perceptron) with two inputs (x1, x2) and a bias (x0=1). The neuron is labeled '1' and outputs Y1. Weights are w11=1.0, w10=-1.0, and w12=1.0. An arrow labeled 'propagação' points to the right.

Diagram of a single neuron (perceptron) with two inputs (x1, x2) and a bias (x0=1). The neuron is labeled '1' and outputs Y1. Weights are w11=1.0, w10=-1.0, and w12=1.0. An arrow labeled 'propagação' points to the right.

$$\begin{aligned}
 v1 &= 1 \times -1.0 + \\
 &\quad 1 \times 1.0 \\
 &\quad 0 \times 1.0 \\
 &= 0 \\
 Y1 &= Q(0) = \mathbf{1}
 \end{aligned}$$

$$v_j = \sum_{i=0}^n (x_i \times w_{ij})$$

$$y_j = f(v_j)$$

Função de ativação - Limiar

$$f(v_j) = \begin{cases} 1 \text{ se } v_j \geq 0 \\ 0 \text{ se } v_j < 0 \end{cases}$$

{71}------------------------------------------------
### Simulando uma Rede Perceptron Fase de Generalização

Testando o modelo:

| x1 | x2 |
|----|----|
| 0  | 0  |
| 0  | 1  |
| 1  | 0  |
| 1  | 1  |

Green arrow pointing right towards the input table.

Diagram of a single neuron (perceptron) with two inputs ( $x_1, x_2$ ) and a bias ( $x_0 = 1$ ). The neuron is labeled '1' inside a circle. Weights are  $w_{11} = 1.0$ ,  $w_{12} = 1.0$ , and  $w_{10} = -1.0$ . The output is  $Y_1$ . A horizontal arrow below the diagram is labeled 'propagação'.

Diagram of a single neuron (perceptron) with two inputs (x1, x2) and a bias (x0=1). The neuron is labeled '1' inside a circle. Weights are w11=1.0, w12=1.0, and w10=-1.0. The output is Y1. A horizontal arrow below the diagram is labeled 'propagação'.

$$\begin{aligned}
 v_1 &= 1 \times -1.0 + \\
 &\quad 1 \times 1.0 \\
 &\quad 1 \times 1.0 \\
 &= 1 \\
 Y_1 &= Q(1) = \mathbf{1}
 \end{aligned}$$

$$v_j = \sum_{i=0}^n (x_i \times w_{ij})$$

$$y_j = f(v_j)$$

Função de ativação - Limiar

$$f(v_j) = \begin{cases} 1 \text{ se } v_j \geq 0 \\ 0 \text{ se } v_j < 0 \end{cases}$$

{72}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-98987d547cba17427b4265c243e4ffbf_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Green arrow pointing right towards the input table.
<!-- /IMAGE_DESCRIPTION -->
## Exercicios

- **Atividade 1:** Implemente em Python o algoritmo de treinamento da rede Perceptron para as tabelas:
  - OR
  - AND
  - XOR

{73}------------------------------------------------
## Exercicios

- **Atividade 2:** Considere os dados da tabela, selecione os atributos mais adequados, faça o pre-processamento. E, a seguir, use uma rede perceptron para classificar os clientes. Use a mesma topologia da atividade anterior.

| <i>Cliente</i> | <i>Renda</i> | <i>Divida</i> | <i>Classe</i> |
|----------------|--------------|---------------|---------------|
| 101            | 2800         | 550           | bom           |
| 102            | 1300         | 500           | mau           |
| 103            | 1400         | 80            | bom           |
| 104            | 500          | 200           | mau           |
| 105            | 1100         | 270           | mau           |
| 106            | 1800         | 450           | bom           |
| 107            | 2400         | 650           | bom           |
| 108            | 1950         | 600           | bom           |
| 109            | 450          | 70            | mau           |
| 110            | 2750         | 730           | bom           |
| 111            | 850          | 90            | mau           |
| 112            | 1300         | 200           | mau           |
| 113            | 2100         | 750           | bom           |
| 114            | 900          | 300           | mau           |
| 115            | 2700         | 250           | bom           |
| 116            | 1600         | 500           | mau           |
| 117            | 1900         | 150           | bom           |
| 118            | 2500         | 800           | bom           |
| 119            | 1600         | 700           | mau           |
| 120            | 2300         | 500           | bom           |
| 121            | 2100         | 250           | bom           |

{74}------------------------------------------------
## Exercicios

- **Atividade 3:** Implemente em Python o algoritmo de treinamento da rede Perceptron como classificador binário para Planta Iris. Calcule também a acurácia.

{75}------------------------------------------------

# Planta Iris

Diagram of an iris flower with labels: Corola (conjunto de pétalas), Pétalas, Sépalas, and Cálice (conjunto de sépalas).

Diagram of an iris flower showing its parts: Corola (conjunto de pétalas), Pétalas, Sépalas, and Cálice (conjunto de sépalas).
### Topologia para 2 classes Classificador Binario Neural

Diagram of a neural network with 4 input nodes and 2 output nodes. The input nodes are labeled: Comprimento da sepala -  $x_1$ , Largura da sepala -  $x_2$ , Comprimento da petala -  $x_3$ , and Largura da petala -  $x_4$ . The output nodes are labeled 'Iris-Setosa' and 'Nao Iris-setosa'.

Neural network diagram showing 4 input nodes connected to 2 output nodes. The output nodes are labeled 'Iris-Setosa' and 'Nao Iris-setosa'.

**Topologia: 4 x 2**

Camada de entrada(dados): 4

Camada de saída (neuronios): 2

Tipo de Planta Iris

| x1  | x2  | x3  | x4  | d1 | d2 |
|-----|-----|-----|-----|----|----|
| 5.1 | 3.5 | 1.4 | 0.2 | 1  | 0  |
| 7   | 3.2 | 4.7 | 1.4 | 0  | 1  |
| ... |     |     |     |    |    |

Iris-Setosa

Nao Iris-Setosa

{76}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-0931f3e098bd4539041de11c50cec2d2_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Neural network diagram showing 4 input nodes connected to 2 output nodes.
<!-- /IMAGE_DESCRIPTION -->
## Exercicios

- **Atividade 4:** Implemente em Python o algoritmo de treinamento da rede Perceptron para reconhecer as letras . Teste usando letras com ruído.

Diagram illustrating the input representation and network topology for a perceptron. On the left, two 5x5 grids represent input patterns (letters 'I' and 'O' with noise). Below them is the label '5x5'. In the center, a vertical vector lists input attributes x1, x2, x3, x4, ..., x25. On the right, a network diagram shows two yellow circular nodes labeled '1' and '2'. Node 1 is connected to the input vector and labeled 'I'. Node 2 is connected to the input vector and has an output arrow labeled 'O'.

Atributos dos objetos **Topologia: 25 x 2**

<!-- IMAGE_DESCRIPTION: datalab-3b281ef3b6cc5f8ba97cbc011bfaac79_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram illustrating the input representation and network topology for a perceptron.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION_ORPHANS -->
## Imagens Curadas

Descrições preservadas para imagens detectadas no documento, mas sem referência markdown compatível no corpo principal.

<!-- IMAGE_DESCRIPTION: datalab-30a26f2d17ca95672702bf50fb4f0242_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Abstract blue wireframe graphic
<!-- /IMAGE_DESCRIPTION -->
<!-- /IMAGE_DESCRIPTION_ORPHANS -->
