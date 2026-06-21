<!-- EXEC_SUMMARY_START -->
## Sumário
> *Leia antes de varrer o arquivo. Vá direto à seção relevante para a pergunta do aluno.*

- **Roteiro**
  - A arquitetura de uma rede neural define o tipo de tarefa que ela pode executar.
- **Redes Feed Forward**
- **Redes Recorrentes**
  - Mapa auto-organizável
- **Redes Feed Forward**
- **Redes Feed ForwardRede Perceptron**
  - Redes Feed ForwardRede Perceptron - Topologia
  - Redes Feed ForwardRede Perceptron - Topologia
  - Redes Feed ForwardRede Perceptron - Topologia
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
  - **Exemplo 2 – Dados desestruturados**
  - Reconhecedor de Caracteres
  - Reconhecedor de Caracteres
  - Reconhecedor de Caracteres
  - Reconhecedor de Caracteres
  - Classificador de sentenças
  - Classificador de sentenças
  - Classificador de sentenças
- **Etapas Básicas de Construção de uma Rede Neural**
  - Rede Perceptron
  - Rede Perceptron
  - Rede Perceptron
  - Rede Perceptron
  - Rede Perceptron
  - Treinamento de Rede Neurais
  - Treinamento de Redes Neurais
- **Rede Perceptron - Algoritmo de Treinamento**
  - Rede Perceptron – Limitações
  - Rede Perceptron – Limitações
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
  - Simulando uma Rede PerceptronFase de Generalização
  - Simulando uma Rede PerceptronFase de Generalização
  - Simulando uma Rede PerceptronFase de Generalização
- **Exercicios**
- **Exercicios**
- **Exercicios**
  - Topologia para 2 classes Classificador Binario Neural
- **Exercicios**
- **Imagens Curadas**

<!-- EXEC_SUMMARY_END -->
<!-- DATALAB_CHUNK 1: pages 1-20 -->

{0}------------------------------------------------

A solid green horizontal bar located in the top left corner of the slide.

Green horizontal bar

# Rede Neural Perceptron

Silvia Moraes

An abstract geometric pattern on the right side of the slide, featuring glowing blue lines and dots forming a complex, interconnected structure against a dark background.

Abstract geometric pattern

{1}------------------------------------------------
## Roteiro

- Arquiteturas de Rede
- Redes FeedForward
- Revisitando a estrutura de um **neurônio** artificial
- Algoritmo de Aprendizado de uma rede perceptron
- Passo a passo de execução
- Limitação da rede

An abstract, artistic representation of a neural network. It features several glowing blue, spherical nodes of varying sizes, each with a complex, textured internal structure. These nodes are interconnected by a dense web of thin, translucent blue lines that resemble axons or dendrites. The entire structure is set against a dark, almost black background, which makes the glowing blue elements stand out prominently. The lighting is soft and diffused, giving the nodes a three-dimensional, ethereal appearance.

Abstract visualization of a neural network structure with glowing blue nodes and connections.

{2}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-61972112770d9c8fb00883057954f885_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Abstract visualization of a neural network structure with glowing blue nodes and connections.
<!-- /IMAGE_DESCRIPTION -->
### A arquitetura de uma rede neural define o tipo de tarefa que ela pode executar.
## Redes Feed Forward

Right-pointing arrow icon

Rede alimentadas para Frente

Perceptron      MultiLayer Perceptron

Diagram comparing a single-layer Perceptron and a MultiLayer Perceptron. The Perceptron shows two input nodes (x1, x2) connected to one output node. The MultiLayer Perceptron shows two input nodes connected to two hidden nodes, which are then connected to one output node.

Detailed diagram of a neural network with labels: 'camada de entrada' (input layer), 'camadas intermediárias' (intermediate layers), and 'camada de saída' (output layer). It shows a fully connected structure with nodes and connecting lines labeled 'conexões'.

<https://sites.icmc.usp.br/andre/research/neural/>

<!-- IMAGE_DESCRIPTION: datalab-7e2f2d03a5dda38b038fd4884629a2b4_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Right-pointing arrow icon
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-163688ca8da9787f5d48edd68d8cc75b_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram comparing a single-layer Perceptron and a MultiLayer Perceptron.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-d244183a8ff3d94b0dcf30140f51020d_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Detailed diagram of a neural network with labels: 'camada de entrada' (input layer), 'camadas intermediárias' (intermediate layers), and 'camada de saída' (output layer).
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-d62e2e2281009c16f4ee61660e716cd9_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a two-layer MultiLayer Perceptron.
<!-- /IMAGE_DESCRIPTION -->
## Redes Recorrentes

Circular arrow icon representing feedback

Rede com retroalimentacao

Diagram of a recurrent neural network (RNN) with three input nodes (x1, x2, x3) connected to a grid of blue nodes. The grid has two horizontal layers of blue nodes, with feedback loops between them, and is connected to three orange output nodes.

<!-- IMAGE_DESCRIPTION: datalab-1517552d07f4a8b389be86af8aff6424_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Circular arrow icon representing feedback
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-aec7150315249ac202a63cc0e32323b8_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a recurrent neural network (RNN) with three input nodes (x1, x2, x3) connected to a grid of blue nodes.
<!-- /IMAGE_DESCRIPTION -->
### Mapa auto-organizável

Diamond-shaped icon representing a self-organizing map

Redes de Kohonen

Diagram of a Kohonen layer, showing two input nodes (x1, x2) connected to a 3x3 grid of green nodes.

Diagram illustrating a Self-Organizing Map (SOM) with a grid of nodes and clusters of red data points.

[https://pt.wikipedia.org/wiki/Mapas\\_de\\_Kohonen](https://pt.wikipedia.org/wiki/Mapas_de_Kohonen)

{3}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-172ebae7d9612607b671d36b7c2b9c54_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diamond-shaped icon representing a self-organizing map
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-2a16bc72fa4d0150523532baaa0ecfad_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a Kohonen layer, showing two input nodes (x1, x2) connected to a 3x3 grid of green nodes.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-0d6c7e0cc7082c9e796e73d173b731e8_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram illustrating a Self-Organizing Map (SOM) with a grid of nodes and clusters of red data points.
<!-- /IMAGE_DESCRIPTION -->
## Redes Feed Forward

Tarefas Supervisionadas: **classificação** o e **regressão**

```
graph LR; x1((x1)) --> output(( )); x2((x2)) --> output;
```

Diagram of a single-layer Perceptron. Two input nodes labeled x1 and x2 are connected to a single orange output node.

Perceptron

```
graph LR; x1((x1)) --> h1(( )); x1 --> h2(( )); x2((x2)) --> h1; x2 --> h2; h1 --> output(( )); h2 --> output;
```

Diagram of a two-layer MultiLayer Perceptron. Two input nodes labeled x1 and x2 are connected to two green hidden nodes, which are then connected to a single orange output node.

MultiLayer Perceptron

```
graph LR; subgraph INPUT; i1(( )); i2(( )); i3(( )); end; subgraph HIDDEN; h1(( )); h2(( )); h3(( )); h4(( )); end; subgraph OUTPUT; o1(( )); o2(( )); end; i1 --> h1; i1 --> h2; i1 --> h3; i1 --> h4; i2 --> h1; i2 --> h2; i2 --> h3; i2 --> h4; i3 --> h1; i3 --> h2; i3 --> h3; i3 --> h4; h1 --> o1; h1 --> o2; h2 --> o1; h2 --> o2; h3 --> o1; h3 --> o2; h4 --> o1; h4 --> o2;
```

Diagram of a deep feedforward neural network. It shows an input layer with three nodes (the first two contain dog and cat images), a hidden layer with four nodes, and an output layer with two nodes. Arrows indicate the forward flow of information from input to hidden to output.

<https://sites.icmc.usp.br/andre/research/neural/>

Propagação: fluxo do sinal sempre para frente

{4}------------------------------------------------

A diagram of a single neuron. On the left, there are two input labels,  $x_1$  and  $x_2$ , each enclosed in a small yellow circle. Two lines connect these input circles to a central orange circle, which represents the neuron's body. The entire diagram is set against a light gray background.

Diagram of a single neuron (Perceptron) with two inputs, x1 and x2, connected to a central orange circle representing the neuron body.

<!-- IMAGE_DESCRIPTION: datalab-12a6537c92844d5b393104c02e8dfc2f_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a deep feedforward neural network.
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

The diagram illustrates a single-layer perceptron topology. On the left, there are two input nodes, each represented by a small circle with a label  $x_1$  and  $x_2$  above it. Arrows from these two nodes point towards a single output node on the right, which is a larger orange circle representing the neuron.

Diagram of a single-layer perceptron topology. Two input nodes, labeled x1 and x2, are connected to a single output node (neuron) represented by an orange circle.

<!-- IMAGE_DESCRIPTION: datalab-9e6062272bbe3ddbb7c0606721d64cf0_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single-layer Perceptron. Two input nodes labeled x1 and x2 are connected to a single orange output node.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-f9a14fbfecbd7d059226cc93677d721b_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single neuron (Perceptron) with two inputs, x1 and x2, connected to a central orange circle representing the neuron body.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-547f726730e589392f239257a833ede3_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single-layer perceptron topology.
<!-- /IMAGE_DESCRIPTION -->
### Redes Feed ForwardRede Perceptron - Topologia

Como definir a quantidade valores de entrada, de camadas e neurônios da rede?

- Como esta rede tem apenas 1 camada, precisamos apenas definir a os **atributos de entrada e quantidade de neurônios** desta única camada.
- Normalmente, define-se um **neurônio para cada classe esperada**.
- Para entender, vamos ver um exemplo...

{6}------------------------------------------------

A diagram showing a simple feed-forward neural network. On the left, there are two input nodes represented by yellow circles, labeled  $x_1$  and  $x_2$ . Lines connect these two input nodes to a single output node on the right, which is represented by an orange circle.

Diagram of a simple feed-forward neural network with two input nodes labeled x1 and x2, and one output node represented by an orange circle.

<!-- IMAGE_DESCRIPTION: datalab-fc46871d72c65d3381d9201646d23439_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a simple feed-forward neural network with two input nodes labeled x1 and x2, and one output node represented by an orange circle.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-3121ebddccf183ca63bb9781be440a7e_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a simple feed-forward neural network with two input nodes labeled x1 and x2, and one output node represented by an orange circle.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-ebff22fb5dd6f50a90e44dca0f82f285_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a simple feed-forward network with two input nodes labeled x1 and x2, and one output node represented by an orange circle.
<!-- /IMAGE_DESCRIPTION -->
### Redes Feed ForwardRede Perceptron - Topologia

| cpf    | nome   | renda | dívida | classificação do cliente |
|--------|--------|-------|--------|--------------------------|
| 111... | João   | 2000  | 1000   | bom                      |
| 222... | Maria  | 3000  | 2000   | mau                      |
| 333... | Pedro  | 1000  | 500    | mau                      |
| 444... | Carlos | 3000  | 1500   | bom                      |

**Entradas:** Quais são atributos podem ser usados como entrada para rede ?

**Saídas :** Em quantas classes do algoritmo deve organizar os clientes?

{7}------------------------------------------------

A diagram showing two input nodes labeled  $x_1$  and  $x_2$  connected to a single output node represented by an orange circle.

Diagram of a simple feed-forward neural network with two input nodes labeled x1 and x2, and one output node represented by an orange circle.
### Redes Feed ForwardRede Perceptron - Topologia

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

A diagram showing a simple feed-forward network. On the left, there are two input nodes labeled  $x_1$  and  $x_2$ , each enclosed in a light yellow circle. Lines from these two nodes converge towards a single output node on the right, which is represented by a solid orange circle.

Diagram of a simple feed-forward network with two input nodes labeled x1 and x2, and one output node represented by an orange circle.
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

A decorative graphic on the right side of the slide featuring a vertical column of glowing blue binary code (0s and 1s) against a dark background, resembling a digital rain or data stream effect.

{10}------------------------------------------------

A diagram showing a single orange circular neuron. Two arrows point into it from the left, labeled

 $x_1$ 

and

 $x_2$ 

.

Diagram of a single neuron with two inputs labeled x1 and x2.

<!-- IMAGE_DESCRIPTION: datalab-07f537f57749b75157f742525e6a8dbc_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A decorative graphic on the right side of the slide featuring a vertical column of glowing blue binary code (0s and 1s) against a dark background, resembling a digital rain or data stream effect.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-cfef993dcc8fb513de79eb1f93cf26ae_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single neuron with two inputs labeled x1 and x2.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-d4af765160d04ecef538e5066006dc77_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single neuron with two inputs labeled x1 and x2.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-af7916c89a458fdab6c3f443217388ae_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single neuron with two inputs labeled x1 and x2.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-4801720824e4b5e2361a5564f91cfb70_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single neuron with two inputs labeled x1 and x2.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-33ed1f9b27c7c21c797aa928b0f06851_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single neuron with two inputs labeled x1 and x2.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-fa859e4e468bfb2710a94527f2c504af_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single neuron with two inputs labeled x1 and x2.
<!-- /IMAGE_DESCRIPTION -->
### Redes Feed ForwardRede Perceptron - Topologia

| renda | dívida | classificação do cliente |
|-------|--------|--------------------------|
| 0,66  | 0,5    | 1                        |
| 1     | 1      | 0                        |
| 0,33  | 0,25   | 0                        |
| 1     | 0,75   | 1                        |

A diagram of a perceptron neuron. It consists of a yellow circular node. Two arrows point into the node from the left, labeled "Renda -

 $x_1$ 

" and "Divida -

 $x_2$ 

". An arrow points out of the node to the right, labeled "Classificação Cliente".

Diagram of a perceptron neuron with inputs 'Renda - x1' and 'Divida - x2', and output 'Classificação Cliente'.

**Topologia menos usual.**

**Cada neurônio é capaz de decidir entre 2 classes:**

- Quando a rede devolve 0, significa que não é um cliente bom.
- Quando a rede devolve 1, significa que é um cliente bom.

{11}------------------------------------------------

A diagram showing a single orange circular neuron. Two arrows point into it from the left, labeled  $x_1$  and  $x_2$ .

Diagram of a single neuron with two inputs labeled x1 and x2.

<!-- IMAGE_DESCRIPTION: datalab-5a4e62bead259c258d069fd3663ea670_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a perceptron neuron with inputs 'Renda - x1' and 'Divida - x2', and output 'Classificação Cliente'.
<!-- /IMAGE_DESCRIPTION -->
### Redes Feed Forward Rede Perceptron - Topologia

Classificação Cliente

| renda | dívida | D1 | D2 |
|-------|--------|----|----|
| 0,66  | 0,5    | 1  | 0  |
| 1     | 1      | 0  | 1  |
| 0,33  | 0,25   | 0  | 1  |
| 1     | 0,75   | 1  | 0  |

A diagram of a perceptron network. Two input labels, 'Renda -  $x_1$ ' and 'Divida -  $x_2$ ', have arrows pointing to two yellow circular neurons labeled '1' and '2'. Neuron '1' has an output arrow pointing right, and neuron '2' also has an output arrow pointing right. A large green bracket on the right groups these two output arrows under the label 'Classificação Cliente'.

Diagram of a two-neuron perceptron network for client classification.

**Topologia mais usual.**

**Neurônio dedicados para cada classe:**

- Haverá uma saída esperada para cada neurônio.
- A saída da rede é dependente dos vários neurônios.
- Pode ser escolhido aquele de maior valor de saída.

{12}------------------------------------------------

A diagram showing a single orange circular neuron. Two inputs, labeled  $x_1$  and  $x_2$ , are shown as small circles with lines connecting them to the main neuron circle.

Diagram of a single neuron with two inputs labeled x1 and x2.

<!-- IMAGE_DESCRIPTION: datalab-1439cb942d9e363bbb3161b5540dd8c6_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a two-neuron perceptron network for client classification.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-a26e142d3df5bef41a84a9dd099d7825_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a two-neuron perceptron network for client classification.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-33809b11cc711711ebb7be1282fcd4b7_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Green arrow pointing right.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-9b6b5924b48bf2fd5f347f88f06f45b3_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a two-neuron perceptron network for client classification.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-9d5d3616a843e8063fdc3613055aaef8_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Green arrow pointing right.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-a83ba9e3e2c1e21dd69953a7b09e45b4_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a two-neuron perceptron network for client classification.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-cf66fc9af9270df2282965aee5368811_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Green arrow pointing right
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-552b051930a92af37b3eae7e67ef3b70_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Green arrow pointing right
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-00f222cd77da15608dc4d8c8c08999a5_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Green arrow pointing right
<!-- /IMAGE_DESCRIPTION -->
### Redes Feed Forward Rede Perceptron - Topologia

Classificação Cliente

A thick green arrow pointing horizontally from left to right, indicating the flow of data from the input table to the neural network diagram.

Green arrow pointing right towards the table.

| renda | dívida | D1 | D2 |
|-------|--------|----|----|
| 0,66  | 0,5    | 1  | 0  |
| 1     | 1      | 0  | 1  |
| 0,33  | 0,25   | 0  | 1  |
| 1     | 0,75   | 1  | 0  |

A diagram of a two-neuron perceptron network. Two input nodes on the left are labeled "Renda -  $x_1$ " and "Divida -  $x_2$ ". Two output nodes on the right are labeled "1" and "2". Weights are shown on the connections: 0,66 from  $x_1$  to node 1, 0,5 from  $x_2$  to node 1, 0,5 from  $x_1$  to node 2, and 0,66 from  $x_2$  to node 2. A bracket on the right groups the output nodes under the label "Classificação Cliente".

Diagram of a two-neuron perceptron network with inputs Renda (x1) and Divida (x2), and outputs for Classificação Cliente.

**Topologia mais usual.**

**Neurônio dedicados para cada classe:**

- Haverá uma saída esperada para cada neurônio.
- A saída da rede é dependente dos vários neurônios.
- Pode ser escolhido aquele de maior valor de saída.

{13}------------------------------------------------

A diagram showing a single orange circular neuron. Two inputs, labeled  $x_1$  and  $x_2$ , are shown as arrows pointing into the neuron from the left.

Diagram of a single neuron with two inputs labeled x1 and x2.

<!-- IMAGE_DESCRIPTION: datalab-0cc86fe8fc37b0edc9581f2af9459a52_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Green arrow pointing right towards the table.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-410562339ce067fdc6fa41940c118658_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a two-neuron perceptron network with inputs Renda (x1) and Divida (x2), and outputs for Classificação Cliente.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-a1d3651b1300f3670e3a9547bafc4db6_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Green arrow pointing right towards the table.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-665537d3e2b4e9dba8755321a1faea0b_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Green arrow pointing to the input table
<!-- /IMAGE_DESCRIPTION -->
### Redes Feed Forward Rede Perceptron - Topologia

Classificação Cliente

A thick green arrow pointing horizontally from left to right, indicating the flow of data from the input table to the neural network diagram.

Green arrow pointing right towards the table.

| renda | dívida | D1 | D2 |
|-------|--------|----|----|
| 0,66  | 0,5    | 1  | 0  |
| 1     | 1      | 0  | 1  |
| 0,33  | 0,25   | 0  | 1  |
| 1     | 0,75   | 1  | 0  |

A diagram of a perceptron network with two input nodes and two output nodes. The input nodes are labeled 'Renda -  $x_1$ ' and 'Divida -  $x_2$ '. The output nodes are labeled '1' (dark blue) and '2' (yellow). Weights are shown on the connections: 0,66 from  $x_1$  to node 1, 0,5 from  $x_2$  to node 1, 0,5 from  $x_1$  to node 2, and 0,66 from  $x_2$  to node 2. Each output node has an arrow pointing to the right, grouped under the label 'Classificação Cliente'.

Diagram of a two-neuron perceptron network for client classification.

**Topologia mais usual.**

**Neurônio dedicados para cada classe:**

- Haverá uma saída esperada para cada neurônio.
- A saída da rede é dependente dos vários neurônios.
- Pode ser escolhido aquele de maior valor de saída.

{14}------------------------------------------------

A diagram showing a single orange circular neuron. Two inputs, labeled  $x_1$  and  $x_2$ , are shown as small yellow circles with lines connecting them to the main neuron circle.

Diagram of a single neuron with two inputs labeled x1 and x2.
### Redes Feed Forward Rede Perceptron - Topologia

Classificação Cliente

| renda | dívida | D1 | D2 |
|-------|--------|----|----|
| 0,66  | 0,5    | 1  | 0  |
| 1     | 1      | 0  | 1  |
| 0,33  | 0,25   | 0  | 1  |
| 1     | 0,75   | 1  | 0  |

A thick green arrow pointing horizontally to the right, indicating the flow of data from the input table to the neural network diagram.

Green arrow pointing right.

A diagram of a feed-forward perceptron network. On the left, two inputs are labeled 'Renda -  $x_1$ ' and 'Divida -  $x_2$ '. Each input line has a blue weight of '1' next to it. These inputs connect to two yellow circular neurons labeled '1' and '2'. Neuron 1 has an output arrow pointing to the right. Neuron 2 also has an output arrow pointing to the right. A large green bracket on the right side groups the outputs of both neurons under the label 'Classificação Cliente'.

Diagram of a two-neuron perceptron network for client classification.

**Topologia mais usual.**

**Neurônio dedicados para cada classe:**

- Haverá uma saída esperada para cada neurônio.
- A saída da rede é dependente dos vários neurônios.
- Pode ser escolhido aquele de maior valor de saída.

{15}------------------------------------------------

A diagram showing a single orange circular neuron. Two inputs, labeled  $x_1$  and  $x_2$ , are shown as small yellow circles with lines connecting them to the main neuron circle.

Diagram of a single neuron with two inputs labeled x1 and x2.
### Redes Feed Forward Rede Perceptron - Topologia

Classificação Cliente

| renda | dívida | D1 | D2 |
|-------|--------|----|----|
| 0,66  | 0,5    | 1  | 0  |
| 1     | 1      | 0  | 1  |
| 0,33  | 0,25   | 0  | 1  |
| 1     | 0,75   | 1  | 0  |

A thick green arrow pointing horizontally to the right, indicating the flow of data from the input table to the neural network diagram.

Green arrow pointing right.

A diagram of a perceptron network with two input nodes and two output nodes. The input nodes are labeled 'Renda -  $x_1$ ' and 'Divida -  $x_2$ '. The output nodes are labeled '1' (yellow circle) and '2' (dark blue circle). Weights of '1' are shown on the connections from  $x_1$  to node 1 and from  $x_2$  to node 2. Arrows from each output node point to a bracket on the right labeled 'Classificação Cliente'.

Diagram of a two-neuron perceptron network for client classification.

**Topologia mais usual.**

**Neurônio dedicados para cada classe:**

- Haverá uma saída esperada para cada neurônio.
- A saída da rede é dependente dos vários neurônios.
- Pode ser escolhido aquele de maior valor de saída.

{16}------------------------------------------------

Mais exemplos de  
topologia ...

An abstract visualization of a network topology. The image features several glowing yellow nodes, each with a translucent orange-red border. These nodes are interconnected by a complex web of thin, translucent lines in shades of orange, red, and blue. The background is dark, with some blurred light spots, creating a sense of depth and connectivity. The overall aesthetic is futuristic and technical, representing a complex network structure.

Abstract visualization of a network topology with glowing nodes and connecting lines.

{17}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-7b1cea8c45c49887a750926f2135fa84_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Abstract visualization of a network topology with glowing nodes and connecting lines.
<!-- /IMAGE_DESCRIPTION -->
#### Exemplo 1 – Dados estruturados

An abstract illustration of a neural network. It features several glowing yellow nodes, which represent neurons, connected by a complex web of red and orange lines representing synapses. The background is dark, making the glowing elements stand out. The overall aesthetic is futuristic and scientific.

Abstract illustration of a neural network with glowing yellow nodes and red/orange connections.

{18}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-2150ae7f14a2e4ad1866ac0c8ec685ad_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Abstract illustration of a neural network with glowing yellow nodes and red/orange connections.
<!-- /IMAGE_DESCRIPTION -->
## Planta Iris

4 atributos de entrada

3 classes: Iris-setosa, Iris-versicolor, Iris-virginica

Diagrama anatómico de uma flor de íris. As partes rotuladas são: Corola (conjunto de pétalas), Pétalas, Sépalas, Cálice (conjunto de sépalas).

Diagrama anatómico de uma flor de íris com rótulos em português.

Gráfico de dispersão mostrando a separação das três espécies de íris com base em atributos de entrada. O eixo horizontal representa o comprimento da sépala (sepal\_length) e o eixo vertical representa o comprimento da pétala (petal\_length). As espécies são representadas por pontos coloridos: Iris-setosa (azul), Iris-versicolor (laranja) e Iris-virginica (verde). A Iris-setosa está isolada no canto inferior esquerdo, a Iris-versicolor no centro e a Iris-virginica no canto superior direito.

species

- Iris-setosa
- Iris-versicolor
- Iris-virginica

Gráfico de dispersão mostrando a separação das três espécies de íris com base em atributos de entrada.

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
> **[Descrição de imagem]** Diagrama anatómico de uma flor de íris com rótulos em português.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-3468bcffa38de23cef94bfb460ccb301_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Gráfico de dispersão mostrando a separação das três espécies de íris com base em atributos de entrada.
<!-- /IMAGE_DESCRIPTION -->
## Planta Iris

4 atributos de entrada

**2 classes: Iris-setosa, Nao Iris-setosa**

The diagram illustrates the structure of an Iris flower. It shows a side view of the flower with labels for its parts: 'Corola (conjunto de pétalas)' pointing to the pink petals, 'Pétalas' pointing to individual petals, 'Sépalas' pointing to the green sepals, and 'Cálice (conjunto de sépalas)' pointing to the green sepal structure at the base. A detailed view of the center shows the yellow stamens and the green pistil.

Diagram of an Iris flower showing its parts: Corola (conjunto de pétalas), Pétalas, Sépalas, and Cálice (conjunto de sépalas).

A scatter plot showing the distribution of three Iris species based on four attributes: sepal\_length, sepal\_width, petal\_length, and petal\_width. The plot is divided into three regions by a diagonal line. The bottom-left region contains blue dots representing Iris-setosa. The top-right region contains orange dots representing Iris-versicolor and green dots representing Iris-virginica. A legend in the bottom right corner identifies the species by color: blue for Iris-setosa, orange for Iris-versicolor, and green for Iris-virginica.

Scatter plot showing the distribution of Iris species (Iris-setosa, Iris-versicolor, Iris-virginica) based on sepal\_length, sepal\_width, petal\_length, and petal\_width. A diagonal line separates the Iris-setosa cluster (blue) from the other two species (orange and green).

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

Diagram of an Iris flower showing its parts: Corola (conjunto de pétalas), Pétalas, Sêpalas, and Cálice (conjunto de sépalas).

Diagram of an Iris flower with labeled parts: Corola (conjunto de pétalas), Pétalas, Sêpalas, and Cálice (conjunto de sépalas).

Diagram illustrating a neural network structure for processing Iris plant data. The input layer consists of four attributes: Comprimento da sépala ( $x_1$ ), Largura da sépala ( $x_2$ ), Comprimento da pétala ( $x_3$ ), and Largura da pétala ( $x_4$ ). These attributes are connected to four hidden nodes labeled  $w_{1j}$ ,  $w_{2j}$ ,  $w_{3j}$ , and  $w_{4j}$ , which are collectively labeled as Pesos. The outputs of these nodes are summed ( $\Sigma$ ) and passed through an activation function ( $f$ ) to produce the final Saida (Output). A green arrow points to the input attributes, labeled Atributos dos objetos. The entire network is labeled Entrada com Dados estruturados.

Comprimento da sépala ( $x_1$ )

Largura da sépala ( $x_2$ )

Comprimento da pétala ( $x_3$ )

Largura da pétala ( $x_4$ )

Atributos dos objetos

Pesos

$w_{1j}$

$w_{2j}$

$w_{3j}$

$w_{4j}$

$\Sigma$

$f$

Saida

Função de Ativação

Entrada com Dados estruturados

Neural network diagram for Iris plant classification.

{21}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-63c666b05041841b01fdef9fa4153ff7_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of an Iris flower showing its parts: Corola (conjunto de pétalas), Pétalas, Sépalas, and Cálice (conjunto de sépalas).
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-f85bf99d372e735d228361bf4d3cf7e6_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Scatter plot showing the distribution of Iris species (Iris-setosa, Iris-versicolor, Iris-virginica) based on sepal_length, sepal_width, petal_length, and petal_width.
<!-- /IMAGE_DESCRIPTION -->
## Planta Iris

Diagram of an Iris flower showing its parts: Corola (conjunto de pétalas), Pétalas, Sépalas, and Cálice (conjunto de sépalas).

Diagram of an Iris flower with labeled parts: Corola (conjunto de pétalas), Pétalas, Sépalas, and Cálice (conjunto de sépalas).

Diagram illustrating a neural network structure for Iris plant classification. The input layer consists of four nodes representing attributes:  $x_1$  (Comprimento da sépala),  $x_2$  (Largura da sépala),  $x_3$  (Comprimento da pétala), and  $x_4$  (Largura da pétala). These inputs are weighted by  $w_{1j}$ ,  $w_{2j}$ ,  $w_{3j}$ , and  $w_{4j}$  respectively, with weights labeled as 5.1, 3.5, 1.4, and 0.2. The weighted inputs are summed ( $\Sigma$ ) and passed through an activation function ( $f$ ) to produce the output (Saída).

Attributes of objects:  $x_1$  (Comprimento da sépala),  $x_2$  (Largura da sépala),  $x_3$  (Comprimento da pétala),  $x_4$  (Largura da pétala).

Weights (Pesos):  $w_{1j}$  (5.1),  $w_{2j}$  (3.5),  $w_{3j}$  (1.4),  $w_{4j}$  (0.2).

Summation ( $\Sigma$ ) and Activation Function ( $f$ ) lead to the output (Saída).

Neural network diagram for Iris plant classification.

Atributos dos objetos

Entrada com Dados estruturados

{22}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-3376f33dd811eb3e39ff47117c958ed9_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of an Iris flower with labeled parts: Corola (conjunto de pétalas), Pétalas, Sêpalas, and Cálice (conjunto de sépalas).
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-c5655e700cc3e9aac7e9f4f07f30264d_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Neural network diagram for Iris plant classification.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-55d74563d1b88865295879cdaffce3ff_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of an Iris flower with labeled parts: Corola (conjunto de pétalas), Pétalas, Sépalas, and Cálice (conjunto de sépalas).
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-d53cd0fd1cf896a9353fd63de1505ba2_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Neural network diagram for Iris plant classification.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-0484c5fce6aa2558cf08aa4125ecc08d_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of an Iris flower with labeled parts: Corola (conjunto de pétalas), Pétalas, Sépalas, and Cálice (conjunto de sépalas).
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-eb03559a4d92ea9ebd63ea9be663c50a_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Neural network diagram for Iris classification.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-463215de07c4f0ed8905717e2f8f55b6_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of an Iris flower with labeled parts: Corola (conjunto de pétalas), Pétalas, Sépalas, and Cálice (conjunto de sépalas).
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-0931f3e098bd4539041de11c50cec2d2_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Neural network diagram for Iris classification.
<!-- /IMAGE_DESCRIPTION -->
## Planta Iris
## Topologia para 2 classes Classificador Binario Neural

Diagram of an Iris flower showing its parts: Corola (conjunto de pétalas), Pétalas, Sépalas, and Cálice (conjunto de sépalas).

Diagram of an Iris flower with labeled parts: Corola (conjunto de pétalas), Pétalas, Sépalas, and Cálice (conjunto de sépalas).

Neural network diagram for Iris classification. Input layer has 4 nodes: Comprimento da sepala -  $x_1$ , Largura da sepala -  $x_2$ , Comprimento da petala -  $x_3$ , and Largura da petala -  $x_4$ . Output layer has 2 nodes: 1 (Iris-Setosa) and 2 (Nao Iris-setosa).

Neural network diagram for Iris classification. Input layer has 4 nodes: Comprimento da sepala - x1, Largura da sepala - x2, Comprimento da petala - x3, and Largura da petala - x4. Output layer has 2 nodes: 1 (Iris-Setosa) and 2 (Nao Iris-setosa).

**Topologia: 4 x 2**

Camada de entrada(dados): 4

Camada de saida (neuronios): 2

Tipo de Planta Iris

| x1  | x2  | x3  | x4  | d1 | d2 |
|-----|-----|-----|-----|----|----|
| 5.1 | 3.5 | 1.4 | 0.2 | 1  | 0  |
| 7   | 3.2 | 4.7 | 1.4 | 0  | 1  |
| ... |     |     |     |    |    |

Iris-Setosa

Nao Iris-Setosa

{23}------------------------------------------------
### **Exemplo 2 – Dados desestruturados**

An abstract visualization of a neural network or data structure. It features several glowing yellow-orange nodes connected by thin, translucent lines. The nodes are spherical and have a bright yellow center, surrounded by a translucent orange shell. The lines are thin and have a wavy, fibrous appearance, with some showing a gradient from orange to blue. The background is dark, with a reddish-brown hue, and there are some blurred light spots, giving it a sense of depth and complexity.

Abstract visualization of a neural network or data structure.

{24}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-7cdd3a0b8107619a3a05ea9ed16eff02_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Abstract visualization of a neural network or data structure.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-e84dd53f6912e1d1da8c934533cc599f_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Abstract visualization of a neural network or data structure.
<!-- /IMAGE_DESCRIPTION -->
### Reconhecedor de Caracteres

- Considere como entrada de uma imagem de caracteres: 5 x 5.

A 5x5 grid of colored squares. The colors transition from dark blue on the left to light cyan on the right, with shades of green in between. The grid is 5 columns wide and 5 rows high.

A 5x5 grid of colored squares representing an input image.

- Objetivo: identificar as imagens correspondentes a vogais:

Five 5x5 grids of colored squares, each representing a different vowel pattern. The patterns are as follows:

- Grid 1: All squares are green.
- Grid 2: The first three columns are green, and the last two columns are white.
- Grid 3: The first column is green, and the remaining four columns are white.
- Grid 4: The first four columns are green, and the last column is white.
- Grid 5: The first column is green, and the remaining four columns are white.

Five 5x5 grids of colored squares representing different vowel patterns.

{25}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-56a7fc5964ed9463fa47ca8a60568dec_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A 5x5 grid of colored squares representing an input image.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-d4c143a69ccd7e28fe8d01dbc9dfbcfa_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Five 5x5 grids of colored squares representing different vowel patterns.
<!-- /IMAGE_DESCRIPTION -->
### Reconhecedor de Caracteres

The diagram illustrates a character recognition process. On the left, a 5x5 grid of colored squares represents the input image, labeled "5x5". To its right is a vertical column of 25 colored squares, representing the extracted features. The main part of the diagram shows a neural network structure. On the left, a vertical column of 25 colored squares represents the input features. These are labeled as  $pixel(x_1)$ ,  $pixel(x_2)$ ,  $pixel(x_3)$ , followed by vertical dots, and then  $pixel(x_{25})$ . Each pixel input is connected to a corresponding weight node:  $W_{1j}$ ,  $W_{2j}$ ,  $W_{3j}$ , followed by vertical dots, and then  $W_{25j}$ . These weight nodes are collectively labeled "Pesos". Arrows from all weight nodes point to a central summation node, represented by a circle containing the Greek letter  $\Sigma$ . An arrow from the summation node points to a rectangular box labeled  $f$ , which represents the activation function. This box is also labeled "Função de Ativação". An arrow from the bottom of the  $f$  box points to the label "Função de Ativação". Finally, an arrow from the right side of the  $f$  box points to the label "Saida".

Diagram of a character recognition neural network architecture.

Atributos dos objetos

{26}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-0c08e48c08f96934cd6bc6911f3069dc_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a character recognition neural network architecture.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-043e64d41a3368d138ace3816fd26469_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a character recognition neural network architecture.
<!-- /IMAGE_DESCRIPTION -->
### Reconhecedor de Caracteres

The diagram illustrates a character recognition system architecture. On the left, a 5x5 grid of pixels is shown, with a binary representation below it: 11111, 10001, 11111, 10001, 10001. To the right of this grid is a vertical column of 25 colored squares, each labeled with a binary value (1 or 0). Below the 5x5 grid, the text "Atributos dos objetos" is displayed. The main processing flow consists of 25 input nodes labeled  $pixel(x_1)$ ,  $pixel(x_2)$ ,  $pixel(x_3)$ , ...,  $pixel(x_{25})$ . Each input node is connected to a corresponding weight node  $w_{1j}$ ,  $w_{2j}$ ,  $w_{3j}$ , ...,  $w_{25j}$ . These weight nodes are collectively labeled "Pesos". All weight nodes feed into a summation node  $\Sigma$ . The output of the summation node is fed into an activation function node  $f$ , which is labeled "Função de Ativação". The final output of the system is labeled "Saida".

5x5

Atributos dos objetos

$pixel(x_1)$ ,  $pixel(x_2)$ ,  $pixel(x_3)$ , ...,  $pixel(x_{25})$

$w_{1j}$ ,  $w_{2j}$ ,  $w_{3j}$ , ...,  $w_{25j}$

Pesos

$\Sigma$

$f$

Função de Ativação

Saida

Diagram of a character recognition neural network architecture.

{27}------------------------------------------------
### Reconhecedor de Caracteres

5x5

$x_1$   
 $x_2$   
 $x_3$   
 $x_4$   
...  
 $x_{25}$

1 → A  
2 → E  
3 → I  
4 → O  
5 → U

Diagram of a character recognition system showing a 5x5 input grid, a list of 25 attributes (x1 to x25), and a neural network topology with 5 output nodes labeled A, E, I, O, and U.

Atributos dos objetos

Topologia: 25 x 5

Diagram showing five 5x5 grids representing different character patterns, each with a unique arrangement of green and white squares.

| $x_1, x_2, x_3, \dots, x_{25}$ | d1 | d2 | d3 | d4 | d5 |
|--------------------------------|----|----|----|----|----|
| 1,1,1,1,1,1,0,...              | 1  | 0  | 0  | 0  | 0  |
| 1,1,1,1,1,1,0,...              | 0  | 1  | 0  | 0  | 0  |
| 0,0,1,0,0,0,0,...              | 0  | 0  | 1  | 0  | 0  |
| 1,1,1,1,1,1,0,...              | 0  | 0  | 0  | 1  | 0  |
| 1,0,0,0,1,1,0,...              | 0  | 0  | 0  | 0  | 1  |
| ...                            |    |    |    |    |    |

{28}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-d17aa1fcc3b86503ad1dd0717a6c34c2_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a character recognition system showing a 5x5 input grid, a list of 25 attributes (x1 to x25), and a neural network topology with 5 output nodes labeled A, E, I, O, and U.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-eb5677b570ab2a3e9d8f5d35ca5b8a4d_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram showing five 5x5 grids representing different character patterns, each with a unique arrangement of green and white squares.
<!-- /IMAGE_DESCRIPTION -->
#### **Exemplo 3 – Dados desestruturados**

An abstract visualization of a neural network or data structure. It features several glowing yellow-orange nodes connected by thin, translucent lines. The nodes are spherical with a bright yellow center and a darker orange outer shell. The lines are thin and have a wavy, fibrous appearance, with some showing internal structure. The background is dark, with a gradient from deep red to black, and some blurred light spots, giving it a sense of depth and complexity.

Abstract visualization of a neural network or data structure.

{29}------------------------------------------------
### Classificador de sentenças

The diagram illustrates a simple neural network for sentence classification. On the left, a stack of documents is shown. Below it, a green arrow points to the word 'Atributos'. The input layer consists of tokens  $x_1, x_2, x_3, \dots, x_n$ . Each token is connected to a corresponding weight node  $w_{1j}, w_{2j}, w_{3j}, \dots, w_{nj}$ . These weight nodes are collectively labeled 'Pesos'. Arrows from all weight nodes point to a central summation node  $\Sigma$ . The output of the summation node is fed into an activation function block labeled  $f$ , which is also labeled 'Função de Ativação'. The final output of the network is labeled 'Saida'.

```
graph LR; Atributos --> Tokens["token (x1), token (x2), token (x3), ..., token (xn)"]; Tokens --> Pesos["w1j, w2j, w3j, ..., wnj"]; Pesos --> Sigma["$\Sigma$"]; Sigma --> f["f"]; f --> Saida;
```

Diagram of a sentence classifier architecture showing tokens, weights, summation, and activation function.

Tipicamente esse problema não é linearmente separável. Ele precisa de uma rede várias camadas.

{30}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-5414f65867392f05ba0063b208eeb5e1_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a sentence classifier architecture showing tokens, weights, summation, and activation function.
<!-- /IMAGE_DESCRIPTION -->
### Classificador de sentenças

The diagram illustrates a single-layer neural network for sentence classification. On the left, a green box contains the sentence "A infraestrutura do hotel era maravilhosa." Below it, a green arrow points to the word "Atributos". The input layer consists of nodes labeled  $infraestrutura (x_1)$ ,  $hotel (x_2)$ ,  $ruim (x_3)$ , and  $maravilhosa (x_n)$ , with vertical ellipses between  $x_3$  and  $x_n$ . Each input node is connected to a corresponding weight node  $w_{1j}$ ,  $w_{2j}$ ,  $w_{3j}$ , and  $w_{nj}$ , with vertical ellipses between  $w_{3j}$  and  $w_{nj}$ . The connections are labeled with red numbers: 1 for  $x_1$ , 1 for  $x_2$ , 0 for  $x_3$ , and 1 for  $x_n$ . These weight nodes are collectively labeled "Pesos". All weight nodes point to a summation node  $\Sigma$ . The output of the summation node is passed to an activation function node  $f$ , which is labeled "Função de Ativação". The final output is labeled "Saida".

Diagram of a single-layer neural network for sentence classification.

Tipicamente esse problema não é linearmente separável. Ele precisa de uma rede várias camadas.

{31}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-5d3455c6c2a37cb3aff761fedeb8644e_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single-layer neural network for sentence classification.
<!-- /IMAGE_DESCRIPTION -->
### Classificador de sentenças

Sentença

Atributos

The diagram illustrates a neural network architecture for sentence classification. On the left, a vertical light blue box labeled 'Atributos' contains the input features  $x_1, x_2, x_3, x_4, \dots, x_n$ . A green arrow points from this box to the first layer of nodes. The first layer consists of five yellow circular nodes labeled 1, 2, 3, 4, and k. These nodes are fully connected to the second layer, which consists of three yellow circular nodes labeled 1, 2, and 3. Each node in the second layer has an arrow pointing to a classification label: 'Positiva' for node 1, 'Negativa' for node 2, and 'Neutra' for node 3.

Diagram of a three-layer neural network for sentence classification.

Veremos mais detalhes dessa topologia na aula sobre MultiLayer Perceptron.

Tipicamente esse problema não é linearmente separável. Ele precisa de uma rede várias camadas.

{32}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-d9843ac5dfc4bbe9e4d21b8898723b5e_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a three-layer neural network for sentence classification.
<!-- /IMAGE_DESCRIPTION -->
## Etapas Básicas de Construção de uma Rede Neural

```
graph LR; Dataset[(Dataset)] --> PreProcess[Pre-processamento]; PreProcess --> TrainDataset[(Dataset Treino)]; PreProcess --> TestDataset[(Dataset Teste)]; TrainDataset --> TrainPhase[Fase de Treinamento]; TrainPhase --> Modelo[Modelo]; Modelo --> GenPhase[Fase de Generalizacao]; TestDataset --> GenPhase; GenPhase --> Resultados[Resultados];
```

The diagram illustrates the basic steps for building a neural network. It starts with a **Dataset** (represented by a grey cylinder) which is processed through **Pre-processamento** (a blue rectangle). The output of pre-processing is split into two paths: one leading to **Dataset Treino** (a dark blue cylinder) and another leading to **Dataset Teste** (a brown cylinder). The **Dataset Treino** is used in the **Fase de Treinamento** (a blue rectangle), which produces a **Modelo** (a light green rectangle). The **Modelo** is then used in the **Fase de Generalizacao** (a blue rectangle), along with the **Dataset Teste**. The final output of the generalization phase is **Resultados**.

Flowchart of the basic steps for building a neural network.

{33}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-c76da2d73c064464051d1583fd80bb6b_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Flowchart of the basic steps for building a neural network.
<!-- /IMAGE_DESCRIPTION -->
### Rede Perceptron

- Como já mencionado, essas redes só conseguem resolver problemas linearmente separáveis.
- O algoritmo de aprendizado desse tipo de rede, procura os coeficientes que traçam a reta que separa linearmente os dados de uma classe de outra.

#0

A scatter plot illustrating linear separability. The plot shows two classes of data points, blue and red, distributed on a 2D plane. A black diagonal line acts as a linear decision boundary, separating the blue points (mostly in the upper-right region) from the red points (mostly in the lower-left region). The background is light gray.

{34}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-fae82236e4211f753df5789eb276d3a4_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A scatter plot illustrating linear separability.
<!-- /IMAGE_DESCRIPTION -->
### Rede Perceptron

Revisitando um neurônio artificial  $j$ :

The diagram illustrates the internal structure of an artificial neuron  $j$ . On the left, a vertical column of inputs is shown:  $x_0$ ,  $x_1$ ,  $x_2$ ,  $x_3$ , followed by vertical ellipsis dots, and  $x_n$ . Each input  $x_i$  is connected by an arrow to a corresponding weight node:  $w_{0j}$  (highlighted in orange),  $w_{1j}$ ,  $w_{2j}$ ,  $w_{3j}$ , and  $w_{nj}$ . A light blue box next to  $x_0$  contains the text  $x_0 = 1$ . A light blue rectangular box at the top right contains the text "Peso extra conhecido como bias". The weight nodes  $w_{1j}$  through  $w_{nj}$  are collectively labeled "Pesos". All weight nodes have arrows pointing to a central circular node labeled with the summation symbol  $\Sigma$ . An arrow labeled  $v_j$  points from the  $\Sigma$  node to a rectangular box labeled with the activation function  $f$ . Below this box, the text "Função de Ativação" is written. An arrow labeled "Saida" points from the  $f$  box to the final output  $y_j$ .

Diagram of an artificial neuron j showing inputs, weights, summation, and activation function.

$$v_j = w_{0j} + \sum_{i=1}^n (x_i \times w_{ij})$$

$$y_j = f(v_j)$$

{35}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-dcc2d5a5b39f780e7a224bb01ba1ef6e_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of an artificial neuron j showing inputs, weights, summation, and activation function.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-1142ba0197b158bb198186fe8baccc32_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of an artificial neuron j showing inputs, weights, summation, and activation function.
<!-- /IMAGE_DESCRIPTION -->
### Rede Perceptron

Revisitando um neurônio artificial  $j$ :

The diagram illustrates the internal structure of an artificial neuron  $j$ . On the left, a vertical column of inputs is shown:  $x_0$ ,  $x_1$ ,  $x_2$ ,  $x_3$ , followed by vertical ellipsis dots, and then  $x_n$ . Each input  $x_i$  is connected by an arrow to a corresponding weight node:  $w_{0j}$  (highlighted in orange),  $w_{1j}$ ,  $w_{2j}$ ,  $w_{3j}$ , and  $w_{nj}$ . A light blue box next to  $x_0$  contains the text  $x_0 = 1$ . A light blue box next to  $w_{0j}$  contains the text "Peso extra conhecido como bias". The weight nodes  $w_{1j}$ ,  $w_{2j}$ ,  $w_{3j}$ , and  $w_{nj}$  are collectively labeled "Pesos". Arrows from all weight nodes point towards a central circular node labeled with the summation symbol  $\Sigma$ . An arrow labeled  $v_j$  points from the  $\Sigma$  node to a rectangular box labeled with the activation function  $f$ . Below this box, the text "Função de Ativação" is written with an arrow pointing up to the box. An arrow labeled "Saida" points from the  $f$  box to the final output  $y_j$ .

Diagram of an artificial neuron j showing inputs, weights, summation, and activation function.

$$v_j = \sum_{i=0}^n (x_i \times w_{ij})$$

$$y_j = f(v_j)$$

{36}------------------------------------------------
### Rede Perceptron

Revisitando um neurônio artificial  $j$ :

- Existem várias funções de ativação para as redes neurais.
- As clássicas são:
  - Limiar ou degrau
  - Linear
  - Sigmoide: logística ou tangente hiperbólica
- Geralmente o Perceptron usa a função limiar.

A graph showing the step function  $\varphi(v_j)$  against  $\varphi_j$ . The function is zero for negative inputs and jumps to a constant positive value for positive inputs. The axes are labeled  $\varphi(v_j)$  and  $\varphi_j$ .

Graph of the Limiar ou Degrau (step) function.

(a) **Limiar ou Degrau**

A graph showing the linear function  $\varphi(v_j)$  against  $\varphi_j$ . The function is a straight line passing through the origin with a positive slope. The axes are labeled  $\varphi(v_j)$  and  $\varphi_j$ .

Graph of the Linear function.

(b) **Linear**

A graph showing the sigmoid function  $\varphi(v_j)$  against  $\varphi_j$ . The function is an S-shaped curve that starts near zero for negative inputs and approaches one for positive inputs. The axes are labeled  $\varphi(v_j)$  and  $\varphi_j$ .

Graph of the Logística (sigmoid) function.

(c) **Logística**

A graph showing the hyperbolic tangent function  $\varphi(v_j)$  against  $\varphi_j$ . The function is an S-shaped curve that passes through the origin, ranging from -1 to 1. The axes are labeled  $\varphi(v_j)$  and  $\varphi_j$ .

Graph of the Tangente Hiperbólica (hyperbolic tangent) function.

(d) **Tangente Hiperbólica**

{37}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-bf30e154f82662d212f21fccdfa2980f_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Graph of the Limiar ou Degrau (step) function.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-fd38170a3981416226ab91f7437ba821_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Graph of the Linear function.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-ca518d020435692dc156bf79eace3292_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Graph of the Logística (sigmoid) function.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-218a22cd9e17ef0657d47183984b118a_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Graph of the Tangente Hiperbólica (hyperbolic tangent) function.
<!-- /IMAGE_DESCRIPTION -->
### Rede Perceptron

Revisitando um neurônio artificial  $j$ :

The diagram illustrates the internal structure of an artificial neuron  $j$ . On the left, a vertical column of input nodes is shown. The top node is  $x_0$ , with a blue box below it containing  $x_0 = 1$ . Below it are  $x_1$ ,  $x_2$ ,  $x_3$ , and a vertical ellipsis, followed by  $x_n$ . Each input node  $x_i$  is connected by an arrow to a corresponding weight node  $w_{ij}$  (labeled  $w_{0j}$ ,  $w_{1j}$ ,  $w_{2j}$ ,  $w_{3j}$ , and  $w_{nj}$ ). The weight nodes  $w_{1j}$  through  $w_{nj}$  are collectively labeled "Pesos". The weight node  $w_{0j}$  is labeled "Peso extra conhecido como bias". All weight nodes have arrows pointing to a central circular node labeled  $\Sigma$  (summation). An arrow labeled  $v_j$  points from the  $\Sigma$  node to a rectangular box labeled  $f$ , which is labeled "Função de Ativação" below it. An arrow labeled "Saida" points from the  $f$  box to the output node  $y_j$ .

Diagram of an artificial neuron j showing inputs x0, x1, x2, x3, ..., xn, weights w0j, w1j, w2j, w3j, ..., wn, and a summation node $\Sigma$ leading to an activation function f.

$$v_j = \sum_{i=0}^n (x_i \times w_{ij})$$

$$y_j = f(v_j)$$

*Função de ativação - Limiar*

$$f(v_j) = \begin{cases} 1 & \text{se } v_j \geq 0 \\ 0 & \text{se } v_j < 0 \end{cases}$$

{38}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-02bb4edc0dbdf4f0749ffd3e0ea2805c_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of an artificial neuron j showing inputs x0, x1, x2, x3, ..., xn, weights w0j, w1j, w2j, w3j, ..., wn, and a summation node Σ leading to an activation function f.
<!-- /IMAGE_DESCRIPTION -->
### Treinamento de Rede Neurais

Dataset com dados históricos, pre-processado e anotado com classes:

- **Divida o dataset** (harmonicamente, no caso de classes), em conjuntos disjuntos de:
  - **treino**: usado para o treinamento do modelo;
  - **validação**: usado para validar o modelo durante o treinamento;
  - **teste**: usado para verificar a solução, ou seja, a versão final do modelo, após o treinamento .

The figure displays three donut charts representing different dataset splits. A legend on the right identifies the colors: red for 'Treino' (Training), blue for 'Validação' (Validation), and green for 'Teste' (Testing).

| Chart | Treino (%) | Validação (%) | Teste (%) |
|-------|------------|---------------|-----------|
| 1     | 80         | 10            | 10        |
| 2     | 70         | 15            | 15        |
| 3     | 60         | 20            | 20        |

Three donut charts illustrating different dataset splits for training, validation, and testing. The legend indicates: Treino (red), Validação (blue), and Teste (green).

Fonte da Figura: <https://www.v7labs.com/blog/train-validation-test-set#:~:text=Training%20data%20is%20the%20set,after%20completing%20the%20training%20phase.>

{39}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-673e9e5873f9a4b71bbe7bac2cf6b758_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Three donut charts illustrating different dataset splits for training, validation, and testing.
<!-- /IMAGE_DESCRIPTION -->
### Treinamento de Redes Neurais

Como os subconjuntos de treino, validação e teste são usados:

O diagrama ilustra o ciclo de treinamento e avaliação de um modelo de rede neural. O processo começa com o **Treino** (dataset de treino), onde o modelo é gerado. Este modelo é então enviado para a **Avaliação do modelo** (dataset de validação). Se os resultados não atingirem a acurácia desejada, ajustes nos algoritmos e/ou dados são feitos, e o modelo é reavaliado. Quando os resultados atingem a acurácia desejada, o modelo é enviado para a **Avaliação final do modelo** (dataset de teste).

```
graph TD; Treino[Treino] -- "Modelo é gerado usando o dataset de Treino" --> Treinamento[Treinamento do modelo]; Treinamento -- "Modelo" --> Avaliacao[Avaliação do modelo]; Avaliacao -- "Resultados não atingiram a acurácia desejada" --> Ajustes[Ajustes nos algoritmos e/ou dados]; Ajustes --> Treinamento; Avaliacao -- "Resultados atingiram a acurácia desejada" --> Avaliacao_Final[Avaliação final do modelo]; Avaliacao_Final -- "Modelo é testado usando os dados do dataset de Teste" --> Avaliacao_Final;
```

Modelo é testado usando os dados do dataset de Validação

Modelo é gerado usando o dataset de Treino

Modelo

Resultados **não atingiram** a acurácia desejada

Resultados **atingiram** a acurácia desejada

Modelo é testado usando os dados do dataset de Teste

Diagrama do fluxo de treinamento e avaliação de uma rede neural.

$$\text{Acurácia} = \frac{\text{Número de predições corretas}}{\text{Total de predições}}$$

<!-- DATALAB_CHUNK 3: pages 41-60 -->

{40}------------------------------------------------

# Treinamento de Redes Neurais

- Os **ciclos de treinamento de uma rede** são medidos em **épocas**.
- Uma época **corresponde a passagem de todos os dados do conjunto de treino uma vez pela rede.**
- Para treinar uma rede são necessárias várias épocas.

{41}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-e151d3468319b81f042ca232c4d82e4b_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama do fluxo de treinamento e avaliação de uma rede neural.
<!-- /IMAGE_DESCRIPTION -->
## Rede Perceptron - Algoritmo de Treinamento

Algoritmo de Treinamento do Perceptron: usa Regra Delta (correção de erro)

- Sendo  $X = \{ (dados1;saidaDesejada1); (dados1;saidaDesejada2), \dots \}$
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
        erroj =  $d_j - y_j$ 
        se erroj!=0 entao :
             $\text{delta} = \eta * \text{erroj} * x_i$ 
             $w_{ij} = w_{ij} + \text{delta}$ 
    erroGeral = erroGeral + abs(erroj)
```

{42}------------------------------------------------

Qual o objetivo  
do treinamento  
de uma rede  
neural?

O que estamos  
procurando?

A 3D rendering of a neural network structure. It features numerous metallic, reflective spheres of varying sizes connected by thin, dark lines. The spheres are arranged in a complex, interconnected pattern that recedes into the background, creating a sense of depth. The lighting is soft, highlighting the metallic texture of the spheres and the geometric arrangement of the connections.

A 3D rendering of a neural network structure, showing interconnected nodes (spheres) and connections (lines), symbolizing the architecture of a neural network.

{43}------------------------------------------------

**Os pesos sinápticos.**

São neles que o conhecimento  
adquirido pela rede fica armazenado.

{44}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-64662465bba247703fdec49c8f3309f9_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Abstract geometric pattern
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-db267ff9c1b97bbae0cb0856be1d8734_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A 3D rendering of a neural network structure, showing interconnected nodes (spheres) and connections (lines), symbolizing the architecture of a neural network.
<!-- /IMAGE_DESCRIPTION -->
### Rede Perceptron – Limitações

Tabela OR

| x1 | x2 | d |
|----|----|---|
| 0  | 0  | 0 |
| 0  | 1  | 1 |
| 1  | 0  | 1 |
| 1  | 1  | 1 |

A 2D plot illustrating the OR function. The horizontal axis is labeled x1 and the vertical axis is labeled x2. Both axes have tick marks at 0 and 1. Four blue circular data points are plotted at coordinates (0,0), (0,1), (1,0), and (1,1). The point (0,0) is labeled '0', and the other three points are labeled '1'. A solid black diagonal line with a negative slope passes through the plot, separating the (0,0) point from the other three points, representing a linear decision boundary for the OR function.

{45}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-0e2f908bcaa3136175994fcf0c9c1a9f_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A 2D plot illustrating the OR function. The horizontal axis is labeled x1 and the vertical axis is labeled x2. Both axes have tick marks at 0 and 1. Four blue circular data points are plotted at coordinates (0,0)...
<!-- /IMAGE_DESCRIPTION -->
### Rede Perceptron – Limitações

Tabela XOR

| x1 | x2 | d |
|----|----|---|
| 0  | 0  | 0 |
| 0  | 1  | 1 |
| 1  | 0  | 1 |
| 1  | 1  | 0 |

A 2D plot illustrating the XOR problem. The horizontal axis is labeled x1 and the vertical axis is labeled x2. Both axes have tick marks at 0 and 1. Four blue circular data points are plotted at the coordinates (0,0), (0,1), (1,0), and (1,1). The point (0,0) is labeled '0' below it. The point (0,1) is labeled '1' to its left. The point (1,0) is labeled '1' below it. The point (1,1) is labeled '0' to its right. A large red question mark '?' is positioned to the right of the plot, indicating the challenge of finding a linear decision boundary for this non-linearly separable dataset.

{46}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-068b3a3247570c4b78342a943f15de9e_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A 2D plot illustrating the XOR problem. The horizontal axis is labeled x1 and the vertical axis is labeled x2. Both axes have tick marks at 0 and 1. Four blue circular data points are plotted at the coordinates (0,0)...
<!-- /IMAGE_DESCRIPTION -->
### Simulando uma Rede Perceptron

- **Pesos** inicializados com zero:  $w_{10} = 0, w_{11} = 0, w_{12} = 0$
- limiar:  $Q(v_k) = \begin{cases} 1 & \text{se } v_k \geq 0 \\ 0 & \text{caso contrário} \end{cases}$ , taxa de aprendizagem:  $\eta = 1$

| x1 | x2 | d |
|----|----|---|
| 0  | 0  | 0 |
| 0  | 1  | 1 |
| 1  | 0  | 1 |
| 1  | 1  | 1 |

Diagram illustrating the forward pass (propagação) of the perceptron. Inputs  $x_1=0$  and  $x_2=0$  are multiplied by weights  $w_{11}=0.0$  and  $w_{12}=0.0$  respectively. The bias input  $x_0=1$  is multiplied by weight  $w_{10}=0.0$ . The weighted sum is  $v_1 = 0$ , which is then passed through the activation function  $Q$  to produce the output  $y_1 = 1.0$ .

Diagram of a single-layer perceptron simulation. A blue circle node contains the value '1'. Three arrows point into it from the left: one from 'x1' with weight 'w11=0.0', one from 'x2' with weight 'w12=0.0', and one from 'x0=1' with weight 'w10=0.0'. The node outputs 'y1 = 1.0' to the right. Below the diagram is a long arrow labeled 'propagação' pointing to the right.

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
> **[Descrição de imagem]** Diagram of a single-layer perceptron simulation.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-a003ffe7299e0a48bceb7f1e45a4f1a3_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single-layer perceptron simulation.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-8d66c9c295023a1380f9986d3663bb1e_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single-layer perceptron simulation.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-3442f31a562d1ef45bfa18b18a6a1ddc_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single-layer perceptron simulation.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-40a8c30f7ea5ecea4912e040c97c5b9c_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single-layer perceptron simulation.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-789ee0a267b24f34bd1f45313e86c9a4_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single-layer perceptron simulation.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-0a73b03fba21af142d619a9a662e6490_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single-layer perceptron simulation.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-9e8ebf03cae78f4f81b697548c2d7250_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single-layer perceptron simulation.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-7ed5d5770331f31ade15439a21c31425_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single-layer perceptron simulation.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-3337af75dfee8af7687b4f49914d6c93_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single-layer perceptron simulation.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-9b1ec0090070bdf52ea28763b8d52477_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single-layer perceptron simulation.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-b34c69e1ec326b01c3a485b27b1df5f6_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single-layer perceptron simulation.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-fed4a04822c24fb22cca3a14f4ddae83_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single-layer perceptron simulation.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-575d7d345b3ec04393bb2ec720ebabca_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single-layer perceptron simulation.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-61a7f401eb46fe99a71f27bc37493f04_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single-layer perceptron simulation.
<!-- /IMAGE_DESCRIPTION -->
### Simulando uma Rede Perceptron

- **Pesos atuais:**  $w_{10} = -1.0, w_{11} = 0.0, w_{12} = 0.0$
- limiar:  $Q(v_k) = \begin{cases} 1 & \text{se } v_k \geq 0 \\ 0 & \text{caso contrário} \end{cases}$ , taxa de aprendizagem:  $\eta = 1$

| x1 | x2 | d |
|----|----|---|
| 0  | 0  | 0 |
| 0  | 1  | 1 |
| 1  | 0  | 1 |
| 1  | 1  | 1 |

Diagram of a single-layer perceptron simulation. A blue circle node contains the value '1'. Three arrows point into it from the left: one from 'x0 = 1' (top), one from 'x1' (middle) with weight 'w11=0.0', and one from 'x2' (bottom) with weight 'w12=0.0'. The output arrow from the node is labeled 'y1 = 0.0'. The weights 'w10 = -1.0' and 'w11 = 0.0' are also shown near the top input. Below the diagram, a long arrow labeled 'propagação' points to the right.

- $v_1 = x_0 \times w_{10} + x_1 \times w_{11} + x_2 \times w_{12}$
- $v_1 = 1 \times -1.0 + 0 \times 0.0 + 1 \times 0.0 = -1.0$
- $y_1 = Q(v_1) = Q(-1.0) = 0.0$

- Ajuste dos pesos (Aplicando a regra delta)

- $erro_1 = d_1 - y_1 = 1 - 0.0 = 1.0$
- $w_{10} = w_{10} + \eta \times erro_1 \times x_0 = -1.0 + 1 \times 1.0 \times 1 = 0.0$
- $w_{11} = w_{11} + \eta \times erro_1 \times x_1 = 0.0 + 1 \times 1.0 \times 0 = 0.0$
- $w_{12} = w_{12} + \eta \times erro_1 \times x_2 = 0.0 + 1 \times 1.0 \times 1 = 1.0$

{48}------------------------------------------------
### Simulando uma Rede Perceptron

- **Pesos atuais:**  $w_{10} = 0.0, w_{11} = 0.0, w_{12} = 1.0$
- limiar:  $Q(v_k) = \begin{cases} 1 & \text{se } v_k \geq 0 \\ 0 & \text{caso contrário} \end{cases}$ , taxa de aprendizagem:  $\eta = 1$

| x1 | x2 | d |
|----|----|---|
| 0  | 0  | 0 |
| 0  | 1  | 1 |
| 1  | 0  | 1 |
| 1  | 1  | 1 |

Diagram illustrating the propagation of inputs to the perceptron node (labeled 1). The inputs are  $x_0 = 1$ ,  $x_1 = 1$  (with weight  $w_{11} = 0.0$ ), and  $x_2 = 0$  (with weight  $w_{12} = 1.0$ ). The output is  $Y_1 = 1.0$ . The weights  $w_{10} = 0.0$  and  $w_{11} = 0.0$  are also indicated. The process is labeled "propagação".

Diagram of a single-layer perceptron simulation. A blue circle node labeled '1' receives three inputs: x0 = 1 (top), x1 = 1 (left, with weight w11 = 0.0), and x2 = 0 (bottom-left, with weight w12 = 1.0). The output is Y1 = 1.0. A horizontal arrow labeled 'propagação' points to the right. The weights w10 = 0.0 and w11 = 0.0 are also indicated near the top input.

- $v_1 = x_0 \times w_{10} + x_1 \times w_{11} + x_2 \times w_{12}$
- $v_1 = 1 \times 0.0 + 1 \times 0.0 + 0 \times 1.0 = 0.0$
- $y_1 = Q(v_1) = Q(0.0) = 1.0$

- Ajuste dos pesos (Aplicando a regra delta)
  - $erro_1 = d_1 - y_1 = 1 - 1.0 = 0.0$
  - quando o erro é zero, não há ajuste de pesos.

{49}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-e2c120be98ede6deb60dd341f5a9803b_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single-layer perceptron. A blue circle node labeled '1' receives three inputs: x0 = 1 (top), x1 = 0 (left, with weight w11 = 1.0), and x2 = 0 (bottom-left, with weight w12 = 1.0). The weight w10 = -1.0 is...
<!-- /IMAGE_DESCRIPTION -->
### Simulando uma Rede Perceptron

- **Pesos atuais:**  $w_{10} = 0.0, w_{11} = 0.0, w_{12} = 1.0$
- limiar:  $Q(v_k) = \begin{cases} 1 & \text{se } v_k \geq 0 \\ 0 & \text{caso contrário} \end{cases}$ , taxa de aprendizagem:  $\eta = 1$

| x1 | x2 | d |
|----|----|---|
| 0  | 0  | 0 |
| 0  | 1  | 1 |
| 1  | 0  | 1 |
| 1  | 1  | 1 |

Diagram illustrating the propagation of inputs  $x_1$ ,  $x_2$ , and  $x_0=1$  through weights  $w_{11}=0.0$ ,  $w_{12}=1.0$ , and  $w_{10}=0.0$  into a node labeled 1, resulting in output  $Y_1 = 1.0$ . The process is labeled "propagação".

Diagram of a single-layer perceptron simulation. A blue circle node contains the value '1'. Three arrows point into it from the left: the top arrow is labeled 'x1' and 'w11=0.0', the middle arrow is labeled 'x2' and 'w12=1.0', and the bottom arrow is labeled 'x0=1' and 'w10=0.0'. An arrow points out of the node to the right, labeled 'Y1 = 1.0'. Below the node, a horizontal arrow points to the right, labeled 'propagação'.

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

- **Pesos atuais:**  $w_{10} = 0.0, w_{11} = 0.0, w_{12} = 1.0$
- limiar:  $Q(v_k) = \begin{cases} 1 & \text{se } v_k \geq 0 \\ 0 & \text{caso contrário} \end{cases}$ , taxa de aprendizagem:  $\eta = 1$

| x1 | x2 | d |
|----|----|---|
| 0  | 0  | 0 |
| 0  | 1  | 1 |
| 1  | 0  | 1 |
| 1  | 1  | 1 |

Diagram of a single-layer perceptron simulation. A blue circle node contains the number 1. Three arrows point into it from the left: a top arrow labeled 'x0 = 1' and 'w10 = 0.0', a middle arrow labeled 'x1' and 'w11 = 0.0', and a bottom arrow labeled 'x2' and 'w12 = 1.0'. An arrow points out of the node to the right, labeled 'Y1 = 1.0'. Below the node, a long horizontal arrow points to the right, labeled 'propagação'.

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
- limiar:  $Q(v_k) = \begin{cases} 1 & \text{se } v_k \geq 0 \\ 0 & \text{caso contrário} \end{cases}$ , taxa de aprendizagem:  $\eta = 1$

| x1 | x2 | d |
|----|----|---|
| 0  | 0  | 0 |
| 0  | 1  | 1 |
| 1  | 0  | 1 |
| 1  | 1  | 1 |

Diagram of a single-layer perceptron simulation. A table on the left shows input-output pairs (x1, x2, d). The second row (0, 1, 1) is highlighted in red. To the right, a diagram shows a node labeled '1' receiving inputs from x0=1, x1=0, and x2=1. Weights w10=-1.0, w11=0.0, and w12=1.0 are shown on the connections. The output is Y1=1.0. An arrow labeled 'propagação' points from the table to the diagram.

- $v_1 = x_0 \times w_{10} + x_1 \times w_{11} + x_2 \times w_{12}$
- $v_1 = 1 \times -1.0 + 0 \times 0.0 + 1 \times 1.0 = 0.0$
- $y_1 = Q(v_1) = Q(0.0) = 1.0$

- Ajuste dos pesos (Aplicando a regra delta)
  - $erro_1 = d_1 - y_1 = 1 - 1.0 = 0.0$
  - quando o erro é zero, não há ajuste de pesos.

{53}------------------------------------------------
### Simulando uma Rede Perceptron

- **Pesos atuais:**  $w_{10} = -1.0, w_{11} = 0.0, w_{12} = 1.0$
- limiar:  $Q(v_k) = \begin{cases} 1 & \text{se } v_k \geq 0 \\ 0 & \text{caso contrário} \end{cases}$ , taxa de aprendizagem:  $\eta = 1$

| x1 | x2 | d |
|----|----|---|
| 0  | 0  | 0 |
| 0  | 1  | 1 |
| 1  | 0  | 1 |
| 1  | 1  | 1 |

Diagram illustrating the propagation of inputs  $x_1=1$  and  $x_2=0$  into the perceptron node, resulting in output  $Y_1=0.0$ . The weights are  $w_{11}=0.0$ ,  $w_{10}=-1.0$ , and  $w_{12}=1.0$ . The bias input  $x_0=1$  is also shown.

Diagram of a single-layer perceptron simulation. A blue circle node labeled '1' receives three inputs: x0 = 1 (top), x1 = 1 (left, labeled '1' in red), and x2 = 0 (bottom, labeled '0' in red). Weights are shown on the connections: w11 = 0.0 (orange) from x1, w10 = -1.0 (orange) from x0, and w12 = 1.0 (orange) from x2. The output is Y1 = 0.0 (blue). A horizontal arrow labeled 'propagação' points to the right.

- $v_1 = x_0 \times w_{10} + x_1 \times w_{11} + x_2 \times w_{12}$
- $v_1 = 1 \times -1.0 + 1 \times 0.0 + 0 \times 1.0 = -1.0$
- $y_1 = Q(v_1) = Q(-1.0) = 0.0$

- Ajuste dos pesos (Aplicando a regra delta)
  - $erro_1 = d_1 - y_1 = 1 - 0.0 = 1.0$
  - $w_{10} = w_{10} + \eta \times erro_1 \times x_0 = -1.0 + 1 \times 1.0 \times 1 = 0.0$
  - $w_{11} = w_{11} + \eta \times erro_1 \times x_1 = 0.0 + 1 \times 1.0 \times 1 = 1.0$
  - $w_{12} = w_{12} + \eta \times erro_1 \times x_2 = 1.0 + 1 \times 1.0 \times 0 = 1.0$

{54}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-0f6e3cdce0f01d6ccceabcced508bb5b_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single-layer perceptron. A blue circle node labeled '1' receives three inputs: x0 = 1 (top), x1 (left, labeled '0'), and x2 (bottom, labeled '1'). Weights are w11 = 1.0 (from x1), w10 = -1.0 (from x0), and...
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-5e9af8986a5845504f251d3079da8078_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single-layer perceptron. A blue circle node labeled '1' receives three inputs: x0 = 1 (top), x1 = 0 (left, labeled '1'), and x2 = 0 (bottom, labeled '0'). Weights are w11 = 1.0 (from x1), w10 = -1.0 (from...
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-4b398c5e8c4fd656d5b7a61806400650_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single-layer perceptron. A blue circle node labeled '1' receives three inputs: x0 = 1 (top), x1 (left, labeled '1'), and x2 (bottom-left, labeled '1'). Weights are shown on the connections: w11 = 1.0 (from...
<!-- /IMAGE_DESCRIPTION -->
### Simulando uma Rede Perceptron

- **Pesos atuais:**  $w_{10} = 0.0, w_{11} = 1.0, w_{12} = 1.0$
- limiar:  $Q(v_k) = \begin{cases} 1 & \text{se } v_k \geq 0 \\ 0 & \text{caso contrário} \end{cases}$ , taxa de aprendizagem:  $\eta = 1$

| x1 | x2 | d |
|----|----|---|
| 0  | 0  | 0 |
| 0  | 1  | 1 |
| 1  | 0  | 1 |
| 1  | 1  | 1 |

Diagram of a single-layer perceptron simulation. A blue circle node contains the number '1'. Three arrows point into it from the left: a top arrow labeled 'x0 = 1' with weight 'w10 = 0.0', a middle arrow labeled 'x1' with weight 'w11 = 1.0', and a bottom arrow labeled 'x2' with weight 'w12 = 1.0'. An arrow points out of the node to the right, labeled 'Y1 = 1.0'. Below the node, a long horizontal arrow points to the right, labeled 'propagação'.

- $v_1 = x_0 \times w_{10} + x_1 \times w_{11} + x_2 \times w_{12}$
- $v_1 = 1 \times 0.0 + 1 \times 1.0 + 1 \times 1.0 = 2.0$
- $y_1 = Q(v_1) = Q(2.0) = 1.0$

- Ajuste dos pesos (Aplicando a regra delta)
  - $erro_1 = d_1 - y_1 = 1 - 1.0 = 0.0$ 
    - quando o erro é zero, não há ajuste de pesos.

{55}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-107c8e1abcb7033ad244e30e7a910045_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single-layer perceptron. A blue circle node contains the number 1. Three arrows point to it: a top arrow labeled 'x0 = 1' with weight 'w10 = -1.0', a left arrow labeled 'x1' with weight 'w11 = 1.0', and a...
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
- limiar:  $Q(v_k) = \begin{cases} 1 & \text{se } v_k \geq 0 \\ 0 & \text{caso contrário} \end{cases}$ , taxa de aprendizagem:  $\eta = 1$

| x1 | x2 | d |
|----|----|---|
| 0  | 0  | 0 |
| 0  | 1  | 1 |
| 1  | 0  | 1 |
| 1  | 1  | 1 |

Diagram of a single-layer perceptron simulation. A blue circle node contains the value '1'. Three arrows point into it from the left: the top arrow is labeled 'x0 = 1' and 'w10 = 0.0'; the middle arrow is labeled 'x1' and 'w11 = 1.0'; the bottom arrow is labeled 'x2' and 'w12 = 1.0'. An arrow points out of the node to the right, labeled 'Y1 = 1.0'. Below the node, a long horizontal arrow points to the right, labeled 'propagação'.

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
- limiar:  $Q(v_k) = \begin{cases} 1 & \text{se } v_k \geq 0 \\ 0 & \text{caso contrário} \end{cases}$ , taxa de aprendizagem:  $\eta = 1$

| x1 | x2 | d |
|----|----|---|
| 0  | 0  | 0 |
| 0  | 1  | 1 |
| 1  | 0  | 1 |
| 1  | 1  | 1 |

Diagram illustrating the forward pass of a perceptron. Inputs  $x_1=0$  and  $x_2=1$  are fed into the network along with the bias  $x_0=1$ . The weights are  $w_{10}=-1.0$ ,  $w_{11}=1.0$ , and  $w_{12}=1.0$ . The output is  $Y_1=1.0$ . The process is labeled "propagação".

Diagram of a single-layer perceptron simulation. A blue circle node labeled '1' receives three inputs: x0 = 1 (top), x1 = 0 (left), and x2 = 1 (bottom). The weights are w10 = -1.0, w11 = 1.0, and w12 = 1.0. The output is Y1 = 1.0. A horizontal arrow labeled 'propagação' points to the right.

- $v_1 = x_0 \times w_{10} + x_1 \times w_{11} + x_2 \times w_{12}$
- $v_1 = 1 \times -1.0 + 0 \times 1.0 + 1 \times 1.0 = 0.0$
- $y_1 = Q(v_1) = Q(0.0) = 1.0$

- Ajuste dos pesos (Aplicando a regra delta)
  - $erro_1 = d_1 - y_1 = 1 - 1.0 = 0.0$
  - quando o erro é zero, não há ajuste de pesos.

{58}------------------------------------------------
### Simulando uma Rede Perceptron

- **Pesos atuais:**  $w_{10} = -1.0, w_{11} = 1.0, w_{12} = 1.0$
- limiar:  $Q(v_k) = \begin{cases} 1 & \text{se } v_k \geq 0 \\ 0 & \text{caso contrário} \end{cases}$ , taxa de aprendizagem:  $\eta = 1$

| x1 | x2 | d |
|----|----|---|
| 0  | 0  | 0 |
| 0  | 1  | 1 |
| 1  | 0  | 1 |
| 1  | 1  | 1 |

Diagram of a single-layer perceptron simulation. A blue circle node contains the number '1'. Three arrows point into it from the left: a top arrow labeled 'x0 = 1' with weight 'w10 = -1.0', a middle arrow labeled 'x1' with weight 'w11 = 1.0', and a bottom arrow labeled 'x2' with weight 'w12 = 1.0'. The inputs x1 and x2 are shown in red text. An arrow points out of the node to the right, labeled 'Y1 = 1.0'. Below the node, a long horizontal arrow points to the right, labeled 'propagação'.

- $v_1 = x_0 \times w_{10} + x_1 \times w_{11} + x_2 \times w_{12}$
- $v_1 = 1 \times -1.0 + 1 \times 1.0 + 0 \times 1.0 = 0.0$
- $y_1 = Q(v_1) = Q(0.0) = 1.0$

- Ajuste dos pesos (Aplicando a regra delta)
  - $erro_1 = d_1 - y_1 = 1 - 1.0 = 0.0$
  - quando o erro é zero, não há ajuste de pesos.

{59}------------------------------------------------
### Simulando uma Rede Perceptron

- **Pesos atuais:**  $w_{10} = -1.0, w_{11} = 1.0, w_{12} = 1.0$
- limiar:  $Q(v_k) = \begin{cases} 1 & \text{se } v_k \geq 0 \\ 0 & \text{caso contrário} \end{cases}$ , taxa de aprendizagem:  $\eta = 1$

| x1 | x2 | d |
|----|----|---|
| 0  | 0  | 0 |
| 0  | 1  | 1 |
| 1  | 0  | 1 |
| 1  | 1  | 1 |

Diagram illustrating the propagation of inputs  $x_0=1$ ,  $x_1$ , and  $x_2$  into the perceptron node, resulting in output  $Y_1=1.0$ . The weights are  $w_{10}=-1.0$ ,  $w_{11}=1.0$ , and  $w_{12}=1.0$ . The propagation is labeled "propagação".

Diagram of a single-layer perceptron simulation. A blue circle node labeled '1' receives three inputs: x0 = 1 (top), x1 (left), and x2 (bottom-left). Weights are labeled on the connections: w10 = -1.0 (top), w11 = 1.0 (left), and w12 = 1.0 (bottom-left). The output is Y1 = 1.0. A red '1' is next to x1 and x2. A red '1' is also next to the first row of the table. An arrow labeled 'propagação' points to the right.

- $v_1 = x_0 \times w_{10} + x_1 \times w_{11} + x_2 \times w_{12}$
- $v_1 = 1 \times -1.0 + 1 \times 1.0 + 1 \times 1.0 = 1.0$
- $y_1 = Q(v_1) = Q(1.0) = 1.0$

- Ajuste dos pesos (Aplicando a regra delta)
  - $erro_1 = d_1 - y_1 = 1 - 1.0 = 0.0$ 
    - quando o erro é zero, não há ajuste de pesos.

<!-- DATALAB_CHUNK 4: pages 61-77 -->

{60}------------------------------------------------
#### Simulando uma Rede Perceptron

- Erro Acumulado para época 3 :
  - Erro Geral:
    - $= \text{abs}(\text{erroEntrada1}) + \text{abs}(\text{erroEntrada2}) + \text{abs}(\text{erroEntrada3}) + \text{abs}(\text{erroEntrada4}) =$
    - $= \text{abs}(-1.0) + \text{abs}(0.0) + \text{abs}(0.0) + \text{abs}(0.0)$
    - $= 1.0$
- Como ainda há erro, o algoritmo prossegue ...

{61}------------------------------------------------
#### Simulando uma Rede Perceptron

- **Pesos atuais:**  $w_{10} = -1.0, w_{11} = 1.0, w_{12} = 1.0$
- limiar:  $Q(v_k) = \begin{cases} 1 & \text{se } v_k \geq 0 \\ 0 & \text{caso contrário} \end{cases}$ , taxa de aprendizagem:  $\eta = 1$

| x1 | x2 | d |
|----|----|---|
| 0  | 0  | 0 |
| 0  | 1  | 1 |
| 1  | 0  | 1 |
| 1  | 1  | 1 |

Diagram of a single-layer perceptron simulation. A blue circle node labeled '1' receives three inputs: x0=1 (top), x1=0 (left), and x2=0 (bottom-left). Weights are shown on the connections: w10=-1.0 from x0, w11=1.0 from x1, and w12=1.0 from x2. The output is Y1=0.0. A horizontal arrow labeled 'propagação' points to the right.

- $v_1 = x_0 \times w_{10} + x_1 \times w_{11} + x_2 \times w_{12}$
- $v_1 = 1 \times -1.0 + 0 \times 1.0 + 0 \times 1.0 = -1.0$
- $y_1 = Q(v_1) = Q(-1.0) = 0.0$

- Ajuste dos pesos (Aplicando a regra delta)
  - $erro_1 = d_1 - y_1 = 0 - 0.0 = 0.0$
  - quando o erro é zero, não há ajuste de pesos.

{62}------------------------------------------------
#### Simulando uma Rede Perceptron

- **Pesos atuais:**  $w_{10} = -1.0, w_{11} = 1.0, w_{12} = 1.0$
- limiar:  $Q(v_k) = \begin{cases} 1 & \text{se } v_k \geq 0 \\ 0 & \text{caso contrário} \end{cases}$ , taxa de aprendizagem:  $\eta = 1$

| x1 | x2 | d |
|----|----|---|
| 0  | 0  | 0 |
| 0  | 1  | 1 |
| 1  | 0  | 1 |
| 1  | 1  | 1 |

Diagram of a single-layer perceptron. A blue circle node contains the number 1. Three arrows point to it: a top arrow labeled 'x0 = 1' with weight 'w10 = -1.0', a left arrow labeled 'x1' with weight 'w11 = 1.0', and a bottom-left arrow labeled 'x2' with weight 'w12 = 1.0'. An arrow points right from the node to the text 'Y1 = 1.0'. Below the table and diagram is a horizontal arrow labeled 'propagação'.

- $v_1 = x_0 \times w_{10} + x_1 \times w_{11} + x_2 \times w_{12}$
- $v_1 = 1 \times -1.0 + 0 \times 1.0 + 1 \times 1.0 = 0.0$
- $y_1 = Q(v_1) = Q(0.0) = 1.0$

- Ajuste dos pesos (Aplicando a regra delta)
  - $erro_1 = d_1 - y_1 = 1 - 1.0 = 0.0$ 
    - quando o erro é zero, não há ajuste de pesos.

{63}------------------------------------------------
#### Simulando uma Rede Perceptron

- **Pesos atuais:**  $w_{10} = -1.0, w_{11} = 1.0, w_{12} = 1.0$
- limiar:  $Q(v_k) = \begin{cases} 1 & \text{se } v_k \geq 0 \\ 0 & \text{caso contrário} \end{cases}$ , taxa de aprendizagem:  $\eta = 1$

| x1 | x2 | d |
|----|----|---|
| 0  | 0  | 0 |
| 0  | 1  | 1 |
| 1  | 0  | 1 |
| 1  | 1  | 1 |

Diagram of a single-layer perceptron simulation. A blue circle node contains the number '1'. Three arrows point into it from the left: a top arrow labeled 'x0 = 1' and 'w10 = -1.0', a middle arrow labeled 'x1' and 'w11 = 1.0', and a bottom arrow labeled 'x2' and 'w12 = 1.0'. A red '1' is next to 'x1' and a red '0' is next to 'x2'. An arrow points out of the node to the right, labeled 'Y1 = 1.0'. Below the node, a long arrow points to the right with the label 'propagação'.

- $v_1 = x_0 \times w_{10} + x_1 \times w_{11} + x_2 \times w_{12}$
- $v_1 = 1 \times -1.0 + 1 \times 1.0 + 0 \times 1.0 = 0.0$
- $y_1 = Q(v_1) = Q(0.0) = 1.0$

- Ajuste dos pesos (Aplicando a regra delta)
  - $erro_1 = d_1 - y_1 = 1 - 1.0 = 0.0$
  - quando o erro é zero, não há ajuste de pesos.

{64}------------------------------------------------
#### Simulando uma Rede Perceptron

- **Pesos atuais:**  $w_{10} = -1.0, w_{11} = 1.0, w_{12} = 1.0$
- limiar:  $Q(v_k) = \begin{cases} 1 & \text{se } v_k \geq 0 \\ 0 & \text{caso contrário} \end{cases}$ , taxa de aprendizagem:  $\eta = 1$

| x1 | x2 | d |
|----|----|---|
| 0  | 0  | 0 |
| 0  | 1  | 1 |
| 1  | 0  | 1 |
| 1  | 1  | 1 |

Diagram illustrating the forward pass (propagação) of the perceptron. Inputs  $x_1$  and  $x_2$  (both 1) are fed into the neuron along with the bias  $x_0 = 1$ . The weights are  $w_{10} = -1.0$ ,  $w_{11} = 1.0$ , and  $w_{12} = 1.0$ . The resulting output is  $Y_1 = 1.0$ .

Diagram of a single-layer perceptron simulation. A blue circle node labeled '1' receives three inputs: x0 = 1 (top), x1 (left), and x2 (bottom-left). Weights are labeled on the connections: w10 = -1.0 (from x0), w11 = 1.0 (from x1), and w12 = 1.0 (from x2). The output is Y1 = 1.0. A red '1' is next to x1 and x2. A red '1' is next to the first row of the table. An arrow labeled 'propagação' points from the table towards the node.

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
### Simulando uma Rede PerceptronFase de Generalização

- A rede está pronta para ser testada (ou usada).

- 1 Carrega-se, na topologia da rede, os pesos encontrados na fase de treinamento.

Diagrama de um neurônio de uma rede perceptron durante a fase de propagação. O neurônio é representado por um círculo azul contendo o número 1. Três entradas são mostradas:  $x_0 = 1$  (entrada de viés),  $x_1$  e  $x_2$ . Os pesos associados são  $w_{10} = -1.0$ ,  $w_{11} = 1.0$  e  $w_{12} = 1.0$ . As entradas  $x_1$  e  $x_2$  são precedidas por um ponto de interrogação (?). A saída do neurônio é  $Y_1$ . Uma seta horizontal na base do diagrama, apontando para a direita, é rotulada "propagação".

Diagrama de um neurônio de uma rede perceptron durante a fase de propagação.

**Modelo** = Corresponde a uma instancia do Algoritmo de IA gerada a partir dos dados de treinamento

- 2 Esta fase implementa apenas a propagação. Informa-se novos valores para as entradas e a rede gera a saída correspondente.

{67}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-5801c19431e76330430e92a598cc7a16_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de um neurônio de uma rede perceptron durante a fase de propagação.
<!-- /IMAGE_DESCRIPTION -->
#### Simulando uma Rede PerceptronFase de Generalização

Testando o modelo:

| x1 | x2 |
|----|----|
| 0  | 0  |
| 0  | 1  |
| 1  | 0  |
| 1  | 1  |

The diagram illustrates a single-layer perceptron model during the propagation phase. A central blue circle node is labeled '1'. Three inputs are shown:  $x_0 = 1$  (top),  $x_1$  (left, with a red question mark), and  $x_2$  (bottom-left, with a red question mark). Weights are indicated:  $w_{11} = 1.0$  (between  $x_1$  and the node),  $w_{12} = 1.0$  (between  $x_2$  and the node), and  $w_{10} = -1.0$  (between  $x_0$  and the node). An arrow points from the node to the output  $Y_1$ . A long horizontal arrow at the bottom is labeled 'propagação'.

Diagram of a single-layer perceptron model during propagation.

$$v_j = \sum_{i=0}^n (x_i \times w_{ij})$$

$$y_j = f(v_j)$$

*Função de ativação - Limiar*

$$f(v_j) = \begin{cases} 1 & \text{se } v_j \geq 0 \\ 0 & \text{se } v_j < 0 \end{cases}$$

{68}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-db39acbd11df5eb7e79ab84562fb8f74_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single-layer perceptron model during propagation.
<!-- /IMAGE_DESCRIPTION -->
#### Simulando uma Rede PerceptronFase de Generalização

Testando o modelo:

| x1 | x2 |
|----|----|
| 0  | 0  |
| 0  | 1  |
| 1  | 0  |
| 1  | 1  |

Diagram illustrating the propagation phase of a single-layer perceptron. The inputs are  $x_0 = 1$ ,  $x_1 = 0$ , and  $x_2 = 0$ . The weights are  $w_{11} = 1.0$ ,  $w_{12} = 1.0$ , and  $w_{10} = -1.0$ . The node output is  $Y_1$ . The process is labeled "propagação".

Diagram of a single-layer perceptron. A blue circle node labeled '1' receives three inputs: x0 = 1 (top), x1 = 0 (left, with weight w11 = 1.0), and x2 = 0 (bottom-left, with weight w12 = 1.0). The weight w10 = -1.0 is shown near the top input. The node outputs Y1. A horizontal arrow below the node is labeled 'propagação'.

$$\begin{aligned} v_1 &= 1 \times -1.0 + \\ &\quad 0 \times 1.0 \\ &\quad 0 \times 1.0 \\ &= -1 \\ Y_1 &= Q(-1) = \mathbf{0} \end{aligned}$$

$$v_j = \sum_{i=0}^n (x_i \times w_{ij})$$

$$y_j = f(v_j)$$

*Função de ativação - Limiar*

$$f(v_j) = \begin{cases} 1 & \text{se } v_j \geq 0 \\ 0 & \text{se } v_j < 0 \end{cases}$$

{69}------------------------------------------------
#### Simulando uma Rede PerceptronFase de Generalização

Testando o modelo:

| x1 | x2 |
|----|----|
| 0  | 0  |
| 0  | 1  |
| 1  | 0  |
| 1  | 1  |

Diagram illustrating the propagation phase of a single-layer perceptron. The inputs are  $x_0 = 1$ ,  $x_1$  (labeled 0), and  $x_2$  (labeled 1). The weights are  $w_{11} = 1.0$ ,  $w_{10} = -1.0$ , and  $w_{12} = 1.0$ . The output is  $Y_1$ . The process is labeled "propagação".

Diagram of a single-layer perceptron. A blue circle node labeled '1' receives three inputs: x0 = 1 (top), x1 (left, labeled '0'), and x2 (bottom, labeled '1'). Weights are w11 = 1.0 (from x1), w10 = -1.0 (from x0), and w12 = 1.0 (from x2). The output is Y1. A horizontal arrow below the diagram is labeled 'propagação'.

$$\begin{aligned} v_1 &= 1 \times -1.0 + \\ &\quad 0 \times 1.0 \\ &\quad 1 \times 1.0 \\ &= 0 \\ Y_1 &= Q(0) = \mathbf{1} \end{aligned}$$

$$v_j = \sum_{i=0}^n (x_i \times w_{ij})$$

$$y_j = f(v_j)$$

*Função de ativação - Limiar*

$$f(v_j) = \begin{cases} 1 & \text{se } v_j \geq 0 \\ 0 & \text{se } v_j < 0 \end{cases}$$

{70}------------------------------------------------
### Simulando uma Rede PerceptronFase de Generalização

Testando o modelo:

| x1 | x2 |
|----|----|
| 0  | 0  |
| 0  | 1  |
| 1  | 0  |
| 1  | 1  |

Diagram illustrating the propagation phase of a single-layer perceptron. The inputs are  $x_0 = 1$ ,  $x_1 = 0$ , and  $x_2 = 0$ . The weights are  $w_{11} = 1.0$ ,  $w_{10} = -1.0$ , and  $w_{12} = 1.0$ . The output is  $Y_1$ . The process is labeled "propagação".

Diagram of a single-layer perceptron. A blue circle node labeled '1' receives three inputs: x0 = 1 (top), x1 = 0 (left, labeled '1'), and x2 = 0 (bottom, labeled '0'). Weights are w11 = 1.0 (from x1), w10 = -1.0 (from x0), and w12 = 1.0 (from x2). The output is Y1. A horizontal arrow below the diagram is labeled 'propagação'.

$$\begin{aligned} v_1 &= 1 \times -1.0 + \\ &\quad 1 \times 1.0 \\ &\quad 0 \times 1.0 \\ &= 0 \\ Y_1 &= Q(0) = \mathbf{1} \end{aligned}$$

$$v_j = \sum_{i=0}^n (x_i \times w_{ij})$$

$$y_j = f(v_j)$$

*Função de ativação - Limiar*

$$f(v_j) = \begin{cases} 1 & \text{se } v_j \geq 0 \\ 0 & \text{se } v_j < 0 \end{cases}$$

{71}------------------------------------------------
### Simulando uma Rede PerceptronFase de Generalização

Testando o modelo:

| x1 | x2 |
|----|----|
| 0  | 0  |
| 0  | 1  |
| 1  | 0  |
| 1  | 1  |

Diagram illustrating the propagation phase of a single-layer perceptron. The inputs are  $x_0 = 1$ ,  $x_1$ , and  $x_2$ . The weights are  $w_{11} = 1.0$ ,  $w_{12} = 1.0$ , and  $w_{10} = -1.0$ . The output is  $Y_1$ . The process is labeled "propagação".

Diagram of a single-layer perceptron. A blue circle node labeled '1' receives three inputs: x0 = 1 (top), x1 (left, labeled '1'), and x2 (bottom-left, labeled '1'). Weights are shown on the connections: w11 = 1.0 (from x1), w12 = 1.0 (from x2), and w10 = -1.0 (from x0). The output is Y1. Below the diagram is a horizontal arrow labeled 'propagação'.

$$\begin{aligned} v_1 &= 1 \times -1.0 + \\ &\quad 1 \times 1.0 \\ &\quad 1 \times 1.0 \\ &= 1 \\ Y_1 &= Q(1) = \mathbf{1} \end{aligned}$$

$$v_j = \sum_{i=0}^n (x_i \times w_{ij})$$

$$y_j = f(v_j)$$

*Função de ativação - Limiar*

$$f(v_j) = \begin{cases} 1 & \text{se } v_j \geq 0 \\ 0 & \text{se } v_j < 0 \end{cases}$$

{72}------------------------------------------------
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
### Topologia para 2 classes Classificador Binario Neural

Diagram of an Iris flower showing its parts: Corola (conjunto de pétalas), Pétalas, Sépalas, and Cálice (conjunto de sépalas).

Diagram of an Iris flower with labeled parts: Corola (conjunto de pétalas), Pétalas, Sépalas, and Cálice (conjunto de sépalas).

Neural network diagram for Iris classification. Input layer has 4 nodes: Comprimento da sepala -  $x_1$ , Largura da sepala -  $x_2$ , Comprimento da petala -  $x_3$ , and Largura da petala -  $x_4$ . Output layer has 2 nodes: 1 (Iris-Setosa) and 2 (Nao Iris-setosa). Arrows show connections from each input node to each output node.

Neural network diagram for Iris classification. Input layer has 4 nodes: Comprimento da sepala - x1, Largura da sepala - x2, Comprimento da petala - x3, and Largura da petala - x4. Output layer has 2 nodes: 1 (Iris-Setosa) and 2 (Nao Iris-setosa).

**Topologia: 4 x 2**

Camada de entrada(dados): 4

Camada de saida (neuronios): 2

Tipo de Planta Iris

| x1  | x2  | x3  | x4  | d1 | d2 |
|-----|-----|-----|-----|----|----|
| 5.1 | 3.5 | 1.4 | 0.2 | 1  | 0  |
| 7   | 3.2 | 4.7 | 1.4 | 0  | 1  |
| ... |     |     |     |    |    |

Iris-Setosa

Nao Iris-Setosa

{76}------------------------------------------------
## Exercicios

- **Atividade 4:** Implemente em Python o algoritmo de treinamento da rede Perceptron para reconhecer as letras . Teste usando letras com ruído.

The diagram illustrates the input and output structure of a perceptron. On the left, two 5x5 grids of squares represent the input features. The first grid shows a digit '1' formed by dark green squares on a light green background. The second grid shows a digit '0' formed by dark green squares on a light green background. Below the first grid is the label '5x5'. To the right of the grids is a vertical column of 25 input nodes, labeled  $x_1, x_2, x_3, x_4, \dots, x_{25}$ . Two arrows originate from this column: one points to a yellow circular node labeled '1' (representing the target output for the digit '1'), and the other points to a yellow circular node labeled '2' (representing the target output for the digit '0'). An arrow also points away from node '2' towards the right, labeled '0'.

Diagram of a 25x2 perceptron topology for digit recognition.

Atributos dos objetos    Topologia: 25 x 2

<!-- IMAGE_DESCRIPTION: datalab-3b281ef3b6cc5f8ba97cbc011bfaac79_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a 25x2 perceptron topology for digit recognition.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION_ORPHANS -->
## Imagens Curadas

Descrições preservadas para imagens detectadas no documento, mas sem referência markdown compatível no corpo principal.

<!-- IMAGE_DESCRIPTION: datalab-2dfa6ac3edfe874f68aa0cbccaa42322_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Green horizontal bar
<!-- /IMAGE_DESCRIPTION -->
<!-- /IMAGE_DESCRIPTION_ORPHANS -->
