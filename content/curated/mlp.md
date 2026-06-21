<!-- EXEC_SUMMARY_START -->
## Sumário
> *Leia antes de varrer o arquivo. Vá direto à seção relevante para a pergunta do aluno.*

- **Redes Feed Forward**
- **Rede MultiLayer Perceptron**
- **Arquitetura e Topologia**
  - Rede MultiLayer Perceptron
  - Rede MultiLayer Perceptron
  - Como definir a topologia de uma rede MLP?
  - Como definir a topologia de uma rede MLP?
  - Como definir a topologia de uma rede MLP?
  - Como definir a topologia de uma rede MLP?
  - Como definir a topologia de uma rede MLP?
  - Como definir a topologia de uma rede MLP?
  - Como definir a topologia de uma rede MLP?
  - Como definir a topologia de uma rede MLP?
- **Como definir a topologia de uma rede MLP?**
- **Como definir a topologia de uma rede MLP?**
- **Como definir a topologia de uma rede MLP?**
- **Como definir a topologia de uma rede MLP?**
- **Como definir a topologia de uma rede MLP?**
- **Quantos neurônios usamos na camada oculta?**
- **Como definir a topologia de uma rede MLP?**
- **Como definir a topologia de uma rede MLP?**
- **Como definir a topologia de uma rede MLP?**
- **Como definir a topologia de uma rede MLP?**
- **Como definir a topologia de uma rede MLP?**
- **Como definir a topologia de uma rede MLP?**
- **Como definir a topologia de uma rede MLP?**
- **Como definir a topologia de uma rede MLP?**
- **Como definir a topologia de uma rede MLP?**
- **Como definir a topologia de uma rede MLP?**
- **Como definir a topologia de uma rede MLP?**
- **Como definir a topologia de uma rede MLP?**
- **Como definir a topologia de uma rede MLP?**
- **Como definir a topologia de uma rede MLP?**
- **Como definir a topologia de uma rede MLP?**
- **Como definir a topologia de uma rede MLP?**
- **Revisitando a rede Perceptron**
  - Redes Feed Forward
  - Rede Perceptron
  - Rede Perceptron
  - Rede Perceptron
  - Rede Perceptron
  - Rede Perceptron
  - Rede Perceptron
  - Rede Perceptron
  - Rede Perceptron
  - Rede Perceptron
- **Rede Perceptron - Algoritmo de Treinamento**
- **Rede Perceptron**
- **Algoritmo Backpropagation**
  - Algoritmo de Treinamento para MLP
  - Algoritmo de Treinamento para MLP
  - Algoritmo de Treinamento para MLP
  - Algoritmo de Treinamento para MLP
  - Algoritmo de Treinamento para MLP
  - Algoritmo de Treinamento para MLP
  - Algoritmo de Treinamento para MLP
  - Algoritmo de Treinamento para MLP
  - Algoritmo de Treinamento para MLP
  - Algoritmo de Treinamento para MLP
  - Algoritmo de Treinamento para MLP
  - Algoritmo de Treinamento para MLP
  - Algoritmo de Treinamento para MLP
  - Algoritmo de Treinamento para MLP
  - Algoritmo de Treinamento para MLP
- **Algoritmo de Treinamento para MLP**
  - 4. Retropropagação:
- **Algoritmo de Treinamento para MLP**
  - 4. Retropropagação:
- **Algoritmo de Treinamento para MLP**
- **Algoritmo de Treinamento para MLP**
- **Algoritmo de Treinamento para MLP**
- **Revisitando as funções de ativação**
- **Algoritmo de Treinamento para MLP**
- **Algoritmo de Treinamento para MLP**
- **Algoritmo de Treinamento para MLP**
- **Algoritmo de Treinamento para MLP**
- **Algoritmo de Treinamento para MLP**
- ****Simulando uma rede MLP****
  - Simulando o treinamento do XOR
  - Simulando o treinamento do XOR
  - Simulando o treinamento do XOR
  - Simulando o treinamento do XOR
  - Simulando o treinamento do XOR
  - Simulando o treinamento do XOR
  - Simulando o treinamento do XOR
  - Simulando o treinamento do XOR
- **Retropropagação**
  - Função de Custo
  - Pesos Finais:
  - Implementando uma MLP
- **`sklearn.neural_network.MLPClassifier`**
  - Implementando uma MLP
- **Dinâmica**

<!-- EXEC_SUMMARY_END -->
<!-- DATALAB_CHUNK 1: pages 1-20 -->

{0}------------------------------------------------

An abstract graphic on the left side of the slide. It features a dark background with a glowing blue wireframe structure that resembles a sphere or a complex network. The structure is composed of numerous small blue dots (nodes) connected by thin, light blue lines (edges), creating a mesh-like appearance that curves and recedes into the distance.

Abstract graphic of a neural network structure.

# **Rede neural MultiLayer Perceptron (MLP)**

Silvia Moraes

{1}------------------------------------------------

**Redes Neurais Artificiais** são sistemas computacionais distribuídos compostos de unidades simples (neurônios), densamente interconectados.

An abstract digital visualization of artificial neural networks. The image features a dark blue background with a dense field of small, multi-colored dots (nodes) in shades of blue, purple, and yellow. On the left side, three distinct, glowing, funnel-like structures in cyan, magenta, and yellow emerge from the background, representing input or processing layers. These structures are composed of numerous fine, curved lines that converge towards the central field of nodes, symbolizing the complex, interconnected nature of the network.

Abstract visualization of artificial neural networks with glowing nodes and connections.

{2}------------------------------------------------

**Redes Neurais Artificiais** podem aplicadas em várias tarefas, em diferentes paradigmas de aprendizagem a depender da sua arquitetura:

- Classificação de dados, de texto, de imagem, ...
- Reconhecimento de objetos, faces, palavras (escritas ou faladas)...
- Regressão de dados: preços futuros de taxas de câmbio ou ações, previsão de vendas, previsão de demandas, ...
- Detecção de fraudes e anomalias
- Recomendação de produtos
- Agrupamento de dados, de objetos, de pessoas, ...
- Sumarização de dados
- Similaridade de dados
- ...

{3}------------------------------------------------
## Redes Feed Forward

Tarefas Supervisionadas: **classificação** o e **regressão**

A diagram of a single-layer perceptron. On the left, two input nodes labeled  $x_1$  and  $x_2$  are enclosed in a yellow dashed circle. Arrows from both nodes point to a single orange circular output node on the right.

Diagram of a single-layer Perceptron. Two input nodes labeled x1 and x2 are connected to a single orange output node.

Perceptron

A diagram of a multi-layer perceptron. On the left, two input nodes labeled  $x_1$  and  $x_2$  are enclosed in a yellow dashed circle. Arrows from these nodes connect to two green circular hidden nodes in the middle. Arrows from the hidden nodes connect to a single orange circular output node on the right. The entire network is enclosed in a red dashed oval.

Diagram of a MultiLayer Perceptron. Two input nodes x1 and x2 are connected to two green hidden nodes, which are then connected to an orange output node.

MultiLayer Perceptron

A diagram of a deep feedforward neural network. On the left, two circular icons of dogs are shown. Arrows from these icons point to a column of three purple circular nodes labeled 'INPUT'. Arrows from the input nodes connect to a column of four purple circular nodes labeled 'HIDDEN'. Arrows from the hidden nodes connect to a column of two purple circular nodes labeled 'OUTPUT'. An arrow from the output nodes points to the right.

Diagram of a deep feedforward neural network with three layers: Input, Hidden, and Output.

<https://sites.icmc.usp.br/andre/research/neural/>

Propagação: fluxo do sinal sempre para frente

{4}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-9e6062272bbe3ddbb7c0606721d64cf0_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single-layer Perceptron. Two input nodes labeled x1 and x2 are connected to a single orange output node.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-d62e2e2281009c16f4ee61660e716cd9_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a MultiLayer Perceptron. Two input nodes x1 and x2 are connected to two green hidden nodes, which are then connected to an orange output node.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-12a6537c92844d5b393104c02e8dfc2f_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a deep feedforward neural network with three layers: Input, Hidden, and Output.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-4356776ca004ecba5d599667a155d7d4_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a 3-layer MLP with 4 input nodes, 4 hidden nodes, and 4 output nodes.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-9cd90f495b95ad2116ff780248c26d95_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a 3-layer MLP with n input nodes, p hidden nodes, and k output nodes.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-f5a5f52bc25d95a7f616290c99e88ae6_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single-layer Perceptron.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-0c80c383f76034e117adf5e5eaadaaf3_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a deep neural network with input, hidden, and output layers.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-66e89867f97592fd4bfab0e4f2b2054f_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a neural network with two input nodes (x1, x2), three hidden nodes, and two output nodes (y1, y2).
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-5a01395925fc88802da68fb5ac0f31ff_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A diagram of a neural network with 4 input nodes (x0, x1, x2, x3) and 4 output nodes (y1, y2, y3, y4).
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-0b998e3ad8f9d104768642612605cb35_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a neural network with 4 layers.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-7c1ccebd0e8661557a8ffc00cfae58a0_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a neural network with 4 layers.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-0eb57eefa7cd45d30e68829ca8a03843_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a neural network with 4 layers.
<!-- /IMAGE_DESCRIPTION -->
## Rede MultiLayer Perceptron

- São **redes perceptron de múltiplas camadas**, contendo uma ou mais camadas ocultas.
- Resolve **problemas não linearmente separáveis**.
- É considerada uma **Shallow Learning** (em oposição à **Deep Learning**) especialmente quando possuem apenas uma camada oculta.

The diagram illustrates a Multi-Layer Perceptron (MLP) with three layers: INPUT, HIDDEN, and OUTPUT. On the left, two circular icons representing a dog and a cat are shown. Arrows from these icons point to the INPUT layer, which consists of three purple circles. The INPUT layer is fully connected to the HIDDEN layer, which also consists of three purple circles. The HIDDEN layer is fully connected to the OUTPUT layer, which consists of two purple circles. The entire network is set against a dark blue background.

Diagram of a Multi-Layer Perceptron (MLP) with three layers: INPUT, HIDDEN, and OUTPUT.

<https://sites.icmc.usp.br/andre/research/neural/>

The diagram illustrates a Multi-Layer Perceptron (MLP) with four layers. The first layer, labeled 'Camada de entrada (dados)', consists of four yellow squares. The second layer, labeled 'Camadas ocultas ou intermediárias (neurônios)', consists of three blue circles. The third layer, labeled 'Camada de Saída (neurônios)', consists of two green circles. The layers are fully connected, with arrows showing the flow of information from the input layer to the hidden layers and then to the output layer. The diagram is set against a light blue background.

Diagram of a Multi-Layer Perceptron (MLP) with four layers: Camada de entrada (dados), Camadas ocultas ou intermediárias (neurônios), and Camada de Saída (neurônios).

{5}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-e394c2b5c61344f6a12397f430086072_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a Multi-Layer Perceptron (MLP) with three layers: INPUT, HIDDEN, and OUTPUT.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-53f1f7d17b3e7aae62169c41d2a88a77_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a Multi-Layer Perceptron (MLP) with four layers: Camada de entrada (dados), Camadas ocultas ou intermediárias (neurônios), and Camada de Saída (neurônios).
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-7e670a2b556b53ea9002dfff3a420e08_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a fully connected MLP with 3 layers: input, hidden, and output.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-410562339ce067fdc6fa41940c118658_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a fully connected MLP with 3 layers.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-9b6b5924b48bf2fd5f347f88f06f45b3_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a fully connected MLP with 3 layers.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-32ff77da4286b58c4778033acaa10836_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a two-layer MultiLayer Perceptron.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-2b00743506f6a3bbd17af764162dc76d_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a 2-2-2 Multi-Layer Perceptron (MLP) architecture for XOR.
<!-- /IMAGE_DESCRIPTION -->
## Arquitetura e Topologia

A photograph of architectural and engineering tools on a white surface. A yellow and green pencil lies diagonally in the upper left. In the center is a stainless steel ball bearing. To the right is a vernier caliper with a silver frame and black jaws, showing a measurement of approximately 10.5 mm. Below the bearing is a technical drawing of a circular component with concentric circles, crosshairs, and a section line labeled 'A-A'. The drawing also includes a dimension line with the text 'Ø 10.5 x 4'. A protractor is partially visible in the bottom right corner, showing a 45-degree angle.

A photograph of architectural and engineering tools including a pencil, a ball bearing, and a vernier caliper on a technical drawing.

{6}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-afe5eb459b7c9cfe880b067777d876d8_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A photograph of architectural and engineering tools including a pencil, a ball bearing, and a vernier caliper on a technical drawing.
<!-- /IMAGE_DESCRIPTION -->
### Rede MultiLayer Perceptron

- Arquitetura e Topologia muitas vezes são usados como sinônimos.
- Eles realmente são fortemente relacionados.
- **Arquitetura corresponde ao tipo de rede e sua topologia.**
- **Topologia descreve o “desenho da rede”:** organização dos seus componentes
  - Número de camadas
  - Número de neurônios por camadas
  - Conexões

{7}------------------------------------------------
### Rede MultiLayer Perceptron

- Exemplo de Topologia :

The diagram illustrates a Multi-Layer Perceptron (MLP) topology. It consists of four layers of nodes:

- Camada de entrada (Input Layer):** Two black circular nodes labeled  $x_1$  and  $x_2$ .
- Camada Oculta ou Intermediária (Hidden Layer):** Three blue circular nodes labeled 1, 2, and 3.
- Camada Oculta ou Intermediária (Hidden Layer):** Two blue circular nodes labeled 4 and 5.
- Camada de Saída (Output Layer):** Two blue circular nodes labeled 6 and 7.

Connections and weights:

- From  $x_1$  to hidden nodes:  $W_{11}$  to node 1,  $W_{21}$  to node 2,  $W_{31}$  to node 3.
- From  $x_2$  to hidden nodes:  $W_{12}$  to node 1,  $W_{22}$  to node 2,  $W_{32}$  to node 3.
- From hidden nodes 1, 2, 3 to hidden nodes 4, 5:  $W_{41}$  to node 4,  $W_{51}$  to node 5;  $W_{42}$  to node 4,  $W_{52}$  to node 5;  $W_{43}$  to node 4,  $W_{53}$  to node 5.
- From hidden nodes 4, 5 to output nodes 6, 7:  $W_{64}$  to node 6,  $W_{74}$  to node 7;  $W_{65}$  to node 6,  $W_{75}$  to node 7.
- From hidden nodes 4, 5 to output nodes 6, 7:  $W_{40}$  to node 4,  $W_{50}$  to node 5;  $W_{60}$  to node 6,  $W_{70}$  to node 7.

Labels for layers:

- Camada de entrada
- Camada Oculta ou Intermediária
- Camada Oculta ou Intermediária
- Camada de Saída

Diagram of a Multi-Layer Perceptron (MLP) topology with 2 input nodes, 3 hidden nodes, and 2 output nodes.

**Exemplo MLP: 2 x 3 x 2 x 2**

Totalmente conectada

{8}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-990567efebf979be51f56d1150012c9d_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a Multi-Layer Perceptron (MLP) topology with 2 input nodes, 3 hidden nodes, and 2 output nodes.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-2b3a967f6ce4f23649be995a353e39f8_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a 3-layer MLP topology.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-9f6dec4d4e9fde40bce018861ef1278e_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a 2-2-2 MLP topology for XOR.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-e151d3468319b81f042ca232c4d82e4b_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a 3-layer MLP topology.
<!-- /IMAGE_DESCRIPTION -->
### Como definir a topologia de uma rede MLP?

- A topologia mais simples possui 3 camadas:
  - Camada de entrada: corresponde à camada de dados
  - Camada oculta: de neurônios
  - Camada de saída: de neurônios

O diagrama ilustra a topologia de uma rede MLP com três camadas. A camada de entrada (à esquerda) é composta por  $n$  neurônios, representados por retângulos azuis, com rótulos  $x_1, x_2, x_3, \dots, x_n$ . A camada oculta (no centro) contém  $m$  neurônios, representados por círculos amarelos. A camada de saída (à direita) contém  $k$  neurônios, representados por círculos verdes, com rótulos  $y_1, y_2, y_3, \dots, y_k$ . Linhas azuis representam as conexões entre os neurônios de uma camada para os neurônios da camada seguinte, mostrando uma conexão completa entre as camadas adjacentes.

Diagrama de uma rede MLP com 3 camadas: entrada, oculta e saída.

{9}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-562f471e8153729557e6a4ee6343c32c_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de uma rede MLP com 3 camadas: entrada, oculta e saída.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-844077b3034f0030b404207db0ad76b4_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de uma rede MLP com 3 camadas: entrada, oculta e saída.
<!-- /IMAGE_DESCRIPTION -->
### Como definir a topologia de uma rede MLP?

- A topologia mais simples possui 3 camadas:
  - Camada de entrada: corresponde à camada de dados
  - Camada oculta: de neurônios
  - Camada de saída: de neurônios

**Totalmente Conectada**  
Parcialmente Conectada

The diagram illustrates a fully connected Multilayer Perceptron (MLP) topology. It consists of three layers of nodes:

- Input Layer:** Represented by blue squares on the left, labeled  $x_1, x_2, x_3, \dots, x_n$ .
- Hidden Layer:** Represented by yellow circles in the middle.
- Output Layer:** Represented by green circles on the right, labeled  $y_1, y_2, y_3, \dots, y_k$ .

Connections are shown as blue lines between nodes in adjacent layers. Every node in the input layer is connected to every node in the hidden layer, and every node in the hidden layer is connected to every node in the output layer, representing a fully connected structure.

Diagram of a fully connected MLP topology with 3 layers: input, hidden, and output.

{10}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-e6df2733626a85205c1db682e6259c46_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a fully connected MLP topology with 3 layers: input, hidden, and output.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-1a827b10290f33d4fec04d0e8ef7a897_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a 3-layer MLP topology. The input layer (blue squares) has n nodes labeled x1, x2, x3, ..., xn. The hidden layer (yellow circles) has p nodes. The output layer (green circles) has k nodes labeled y1, y2, y3...
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-6e15fc9ea763541c5913d26f85072ae1_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a fully connected MLP with 3 layers: input (n nodes), hidden (p nodes), and output (k nodes).
<!-- /IMAGE_DESCRIPTION -->
### Como definir a topologia de uma rede MLP?

- A topologia mais simples possui 3 camadas:
  - Camada de entrada: corresponde à camada de dados
  - Camada oculta: de neurônios
  - Camada de saída: de neurônios
##### Totalmente Conectada

- $n$  dados de entrada
- $p$  neurônios na camada oculta
- $k$  neurônios na camada de saída
##### Parcialmente Conectada

The diagram illustrates a fully connected Multilayer Perceptron (MLP) with three layers. The input layer on the left consists of  $n$  blue square nodes labeled  $x_1, x_2, x_3, \dots, x_n$ . The hidden layer in the middle consists of  $p$  yellow circular nodes, with a vertical ellipsis between the third and last nodes. The output layer on the right consists of  $k$  green circular nodes labeled  $y_1, y_2, y_3, y_4, \dots, y_k$ . Every node in the input layer is connected to every node in the hidden layer, and every node in the hidden layer is connected to every node in the output layer, as indicated by the dense web of blue lines. Below the layers, the labels  $n$ ,  $x$ ,  $p$ ,  $x$ , and  $k$  are positioned under the input, hidden, and output layers respectively.

Diagram of a fully connected MLP with 3 layers: input, hidden, and output.

{11}------------------------------------------------
### Como definir a topologia de uma rede MLP?

- A topologia mais simples possui 3 camadas:
  - Camada de entrada: corresponde à camada de dados
  - Camada oculta: de neurônios
  - Camada de saída: de neurônios

A red star-shaped icon with the word "Pruning" written in white text inside it.

Red star icon with the word 'Pruning' inside.

Totalmente Conectada  
**Parcialmente Conectada**

Eliminação de conexões

A diagram of a 3-layer MLP. The input layer has nodes labeled

 $x_1, x_2, x_3, \dots, x_n$ 

represented by blue squares. The hidden layer has four yellow circles. The output layer has nodes labeled

 $y_1, y_2, y_3, y_4, \dots, y_k$ 

represented by green circles. Blue lines represent connections between all input nodes and all hidden nodes, and between all hidden nodes and all output nodes. A red line highlights a specific connection from

 $x_n$ 

to the bottom hidden node, which then connects to

 $y_k$ 

, illustrating the concept of pruning.

Diagram of a 3-layer MLP showing input, hidden, and output layers with connections and pruning.

{12}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-e3b8510f6a2194e250205ab7bc38076d_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Red star icon with the word 'Pruning' inside.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-7f17c430b9598e4d748a8041457810b3_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a 3-layer MLP showing input, hidden, and output layers with connections and pruning.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-bb6d33498937738ff5dac8d91c9ebaad_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Red star icon with the word 'Pruning' inside.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-7832324609ad3cc688064e0341612b32_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Red star icon with the word 'Pruning' inside.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-a26e142d3df5bef41a84a9dd099d7825_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a 3-layer MLP showing input, hidden, and output layers with connections and pruning.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-d25a962fde4b3171879749757440c3c5_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Red star icon with the word 'Pruning' inside.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-95e259e8cb3519025066052af263f8c0_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram illustrating the process of adding a hidden layer to an MLP based on a heuristic rule.
<!-- /IMAGE_DESCRIPTION -->
### Como definir a topologia de uma rede MLP?

- A topologia mais simples possui 3 camadas:
  - Camada de entrada: corresponde à camada de dados
  - Camada oculta: de neurônios
  - Camada de saída: de neurônios

A red five-pointed star with the word "Pruning" written in white text inside it.

Red star icon with the word 'Pruning' inside.

Totalmente Conectada  
**Parcialmente Conectada**

Eliminação de conexões

A diagram of a Multilayer Perceptron (MLP) with three layers. The input layer on the left has blue square nodes labeled

 $x_1, x_2, x_3, \dots, x_n$ 

. The hidden layer in the middle has yellow circular nodes. The output layer on the right has green circular nodes labeled

 $y_1, y_2, y_3, y_4, \dots, y_k$ 

. Every node in one layer is connected to every node in the next layer by a blue line, representing a fully connected topology.

Diagram of a fully connected MLP with 3 layers.

{13}------------------------------------------------
### Como definir a topologia de uma rede MLP?

- A topologia mais simples possui 3 camadas:
  - Camada de entrada: corresponde à camada de dados
  - Camada oculta: de neurônios
  - Camada de saída: de neurônios

A red star-shaped icon with the word "Pruning" written in white text inside it.

Red star icon with the word 'Pruning' inside.

Totalmente Conectada  
**Parcialmente Conectada**

Eliminação de conexões  
Eliminação de neurônios

A diagram of a 3-layer MLP. The input layer (left) has blue squares labeled

 $x_1, x_2, x_3, \dots, x_n$ 

. The hidden layer (middle) has yellow circles. The output layer (right) has green circles labeled

 $y_1, y_2, y_3, y_4, \dots, y_k$ 

. Blue lines represent connections between all input nodes and all hidden nodes, and between all hidden nodes and all output nodes. A red line connects the bottom input node

 $x_n$ 

to a red circle at the bottom of the hidden layer, which is also connected to the bottom output node

 $y_k$ 

. This red circle and its connections are highlighted with red lines, indicating a pruning operation.

Diagram of a 3-layer MLP showing input, hidden, and output layers with connections and pruning.

{14}------------------------------------------------
### Como definir a topologia de uma rede MLP?

- A topologia mais simples possui 3 camadas:
  - Camada de entrada: corresponde à camada de dados
  - Camada oculta: de neurônios
  - Camada de saída: de neurônios

A red five-pointed star with the word "Pruning" written in white text inside it.

Red star icon with the word 'Pruning' inside.

Totalmente Conectada  
**Parcialmente Conectada**

Eliminação de conexões  
Eliminação de neurônios

A diagram of a Multilayer Perceptron (MLP) with three layers. The input layer on the left has nodes labeled

 $x_1, x_2, x_3, \dots, x_n$ 

, represented by blue squares. The hidden layer in the middle has four yellow circles. The output layer on the right has nodes labeled

 $y_1, y_2, y_3, y_4, \dots, y_k$ 

, represented by green circles. Every node in one layer is connected to every node in the next layer by a blue line, representing a fully connected topology.

Diagram of a fully connected MLP with 3 layers.

{15}------------------------------------------------
#### Como definir a topologia de uma rede MLP?

- A topologia mais simples possui 3 camadas:

- **Camada de entrada:** corresponde à camada de dados
- Camada oculta: de neurônios
- Camada de saída: de neurônios

n: quantidade de dados de entrada, número de features/atributos de entrada

The diagram illustrates a Multi-Layer Perceptron (MLP) with three layers:

- Input Layer:** Represented by blue squares, with  $n$  nodes labeled  $x_1, x_2, x_3, \dots, x_n$ . A red box highlights this layer and the label  $n$ .
- Hidden Layer:** Represented by yellow circles, with  $p$  nodes.
- Output Layer:** Represented by green circles, with  $k$  nodes labeled  $y_1, y_2, y_3, \dots, y_k$ .

Connections are shown between all nodes in adjacent layers, indicating a fully connected topology. The labels  $x$ ,  $p$ ,  $x$ , and  $k$  are placed below the respective layers.

Diagram of a 3-layer MLP topology. The input layer (blue squares) has n nodes labeled x1, x2, x3, ..., xn. The hidden layer (yellow circles) has p nodes. The output layer (green circles) has k nodes labeled y1, y2, y3, ..., yk. All nodes are fully connected to each other. A red box highlights the input layer and its label 'n'.

{16}------------------------------------------------
#### Planta Iris

4 atributos de entrada

The diagram illustrates the structure of an Iris flower. It shows a side view of the flower with labels for its main parts: 'Corola (conjunto de pétalas)' pointing to the pink petals, 'Pétalas' pointing to a single petal, 'Sépalas' pointing to the green sepals, and 'Cálice (conjunto de sépalas)' pointing to the base of the sepals. A detailed view of the center shows the yellow stamens and the green pistil.

Diagram of an Iris flower with labels for its parts: Corola (conjunto de pétalas), Pétalas, Sépalas, and Cálice (conjunto de sépalas).

A scatter plot showing the relationship between the four input attributes (sepal\_length, sepal\_width, petal\_length, petal\_width) for three species of Iris. The plot uses a grid system. The species are color-coded: Iris-setosa (blue), Iris-versicolor (orange), and Iris-virginica (green). A blue diagonal line is drawn across the plot, likely representing a decision boundary. The legend indicates the species for each color: blue for Iris-setosa, orange for Iris-versicolor, and green for Iris-virginica.

Scatter plot showing the relationship between sepal\_length, sepal\_width, petal\_length, and petal\_width for three species of Iris: Iris-setosa (blue), Iris-versicolor (orange), and Iris-virginica (green).

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

{17}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-93afce28d7dec5b2202789b31b4ef8ab_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of an Iris flower with labels for its parts: Corola (conjunto de pétalas), Pétalas, Sépalas, and Cálice (conjunto de sépalas).
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-fed39b841ae2dce01088b84bfc1e2789_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Scatter plot showing the relationship between sepal_length, sepal_width, petal_length, and petal_width for three species of Iris: Iris-setosa (blue), Iris-versicolor (orange), and Iris-virginica (green).
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-63c666b05041841b01fdef9fa4153ff7_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of an Iris flower showing its parts: Corola (conjunto de pétalas), Pétalas, Sépalas, and Cálice (conjunto de sépalas).
<!-- /IMAGE_DESCRIPTION -->
### Como definir a topologia de uma rede MLP?

- A topologia mais simples possui 3 camadas:

- **Camada de entrada:** corresponde à camada de dados
- Camada oculta: de neurônios
- Camada de saída: de neurônios

Diagram illustrating a simple MLP topology with 3 layers:

- Input Layer (x):** 4 nodes, labeled  $x_1, x_2, x_3, x_4$ . The number 4 is highlighted in red above the layer label.
- Hidden Layer (p):** 4 nodes, labeled  $p_1, p_2, p_3, p_4$ .
- Output Layer (k):** 4 nodes, labeled  $y_1, y_2, y_3, y_4$ .

Connections are shown between all nodes in adjacent layers. Labels for input features are: Comprimento da sépala ( $x_1$ ), Largura da sépala ( $x_2$ ), Comprimento da pétala ( $x_3$ ), and Largura da pétala ( $x_4$ ).

Diagram of a 3-layer MLP with 4 input nodes, 4 hidden nodes, and 4 output nodes.

n: quantidade de dados de entrada, número de features/atributos de entrada

Diagram illustrating a general MLP topology with 3 layers:

- Input Layer (x):**  $n$  nodes, labeled  $x_1, x_2, x_3, \dots, x_n$ . The entire input layer is enclosed in a red box.
- Hidden Layer (p):**  $p$  nodes, labeled  $p_1, p_2, p_3, \dots, p_p$ .
- Output Layer (k):**  $k$  nodes, labeled  $y_1, y_2, y_3, \dots, y_k$ .

Connections are shown between all nodes in adjacent layers.

Diagram of a 3-layer MLP with n input nodes, p hidden nodes, and k output nodes.

{18}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-79e1709a7317ead45379cbb8ff3ba802_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** General diagram of a 3-layer MLP.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-d53cd0fd1cf896a9353fd63de1505ba2_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a simple MLP topology with 3 layers: input, hidden, and output.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-7e1c9b51e067a48cd0fcc9748d8bd8d8_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** General diagram of an MLP topology.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-933ecd14c858bf3fc919222d8e357bc8_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** General diagram of an MLP topology with n input nodes, p hidden nodes, and k output nodes.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-5478f70a6cef3e5672b2b22d28830cfb_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** General diagram of an MLP topology.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-a4b963a07cc368283154762c4b156fe7_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** General diagram of an MLP topology.
<!-- /IMAGE_DESCRIPTION -->
#### Como definir a topologia de uma rede MLP?

- A topologia mais simples possui 3 camadas:
  - Camada de entrada: corresponde à camada de dados
  - Camada oculta: de neurônios
  - **Camada de saída:** de neurônios

The diagram illustrates a Multilayer Perceptron (MLP) with three layers. The input layer consists of  $n$  nodes, represented by blue squares, labeled  $x_1, x_2, x_3, \dots, x_n$ . The hidden layer consists of  $p$  nodes, represented by yellow circles. The output layer consists of  $k$  nodes, represented by green circles, labeled  $y_1, y_2, y_3, \dots, y_k$ . All nodes in one layer are connected to all nodes in the next layer. A red box highlights the output layer, and a text box above it states "k: quantidade de classes". Below the diagram, the labels  $n$ ,  $x$ ,  $p$ ,  $x$ , and  $k$  are positioned under their respective layers.

Diagram of a 3-layer MLP topology.

{19}------------------------------------------------
##### Planta Iris

4 atributos de entrada

3 classes: iris-setosa, iris-versicolor e iris-virginica

The diagram illustrates the structure of an Iris flower. It shows a side view of the flower with labels for the 'Corola (conjunto de pétalas)' (petal set) and 'Pétalas' (petals). Below, it shows the 'Sépalas' (sepals) and the 'Cálice (conjunto de sépalas)' (calyx). Dotted lines connect the labels to the corresponding parts of the flower.

Diagram of an Iris flower showing its parts: Corola (conjunto de pétalas), Pétalas, Sépalas, and Cálice (conjunto de sépalas).

A scatter plot showing the distribution of three Iris species based on sepal and petal measurements. The x-axis represents sepal length, and the y-axis represents sepal width. The legend indicates three species: Iris-setosa (blue dots), Iris-versicolor (orange dots), and Iris-virginica (green dots). A diagonal line is drawn across the plot, likely representing a decision boundary for classification. Iris-setosa is clustered in the bottom-left, Iris-versicolor in the middle, and Iris-virginica in the top-right.

Scatter plot showing the distribution of Iris species based on sepal and petal measurements.

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

<!-- IMAGE_DESCRIPTION: datalab-f85bf99d372e735d228361bf4d3cf7e6_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Scatter plot showing the distribution of Iris species based on sepal and petal measurements.
<!-- /IMAGE_DESCRIPTION -->
## Como definir a topologia de uma rede MLP?

- A topologia mais simples possui 3 camadas:
  - Camada de entrada: corresponde à camada de dados
  - Camada oculta: de neurônios
  - **Camada de saída:** de neurônios

Diagram illustrating a 3-layer MLP topology for classification. The input layer (4 nodes) corresponds to the features: Comprimento da sépala ( $x_1$ ), Largura da sépala ( $x_2$ ), Comprimento da pétala ( $x_3$ ), and Largura da pétala ( $x_4$ ). The hidden layer has  $p$  nodes. The output layer has 3 nodes, corresponding to the classes:  $y_1$  (setosa),  $y_2$  (versicolor), and  $y_3$  (virginica). The connections are fully connected between adjacent layers.

Diagram of a 3-layer MLP for Iris dataset classification.

Diagram illustrating a general 3-layer MLP topology. The input layer has  $n$  nodes ( $x_1, x_2, x_3, \dots, x_n$ ). The hidden layer has  $p$  nodes. The output layer has  $k$  nodes ( $y_1, y_2, y_3, \dots, y_k$ ), which are highlighted by a red box. A label above the box indicates  $k$ : quantidade de classes. The connections are fully connected between adjacent layers.

General diagram of a 3-layer MLP.

{21}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-c5655e700cc3e9aac7e9f4f07f30264d_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a 3-layer MLP for Iris dataset classification.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-4b87467ad9642943235f48f7d4b59449_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of an MLP topology for Iris dataset classification.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-9f9386d5b3d6cbeb1ed104a799320ebf_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a 4-3 MLP topology for Iris dataset classification.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-3e2a8dc8c5537dbe703cdcb0e21e4e1b_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a 3-layer MLP for Iris dataset classification.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-b51423b6c049f5b5fcde42e50b58f18b_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a 3-layer MLP for Iris dataset classification.
<!-- /IMAGE_DESCRIPTION -->
## Como definir a topologia de uma rede MLP?

- A topologia mais simples possui 3 camadas:
  - Camada de entrada: corresponde à camada de dados
  - **Camada oculta:** de neurônios
  - Camada de saída: de neurônios

The diagram illustrates a simple MLP topology with three layers of nodes. The input layer consists of  $n$  blue square nodes labeled  $x_1, x_2, x_3, \dots, x_n$ . The hidden layer consists of  $p$  yellow circular nodes. The output layer consists of  $k$  green circular nodes labeled  $y_1, y_2, y_3, \dots, y_k$ . All nodes in one layer are connected to all nodes in the next layer by blue lines. The output layer is highlighted with a red rectangular box. Below the diagram, the labels  $n$ ,  $x$ ,  $p$ ,  $x$ , and  $k$  are positioned under their respective layers.

Diagram of a simple MLP topology with 3 layers: input, hidden, and output.

{22}------------------------------------------------
## Como definir a topologia de uma rede MLP?

- A topologia mais simples possui 3 camadas:

Quantos neurônios usamos na camada oculta?

- Camada de entrada: corresponde à camada de dados
- **Camada oculta:** de neurônios
- Camada de saída: de neurônios

O diagrama ilustra a topologia de uma rede MLP com três camadas. A camada de entrada (à esquerda) contém  $n$  neurônios, representados por retângulos azuis, com rótulos  $x_1, x_2, x_3, \dots, x_n$  e o número  $n$  abaixo. A camada oculta (no meio) contém  $p$  neurônios, representados por círculos amarelos, com o número  $p$  abaixo. A camada de saída (à direita) contém  $k$  neurônios, representados por círculos verdes, com rótulos  $y_1, y_2, y_3, y_4, \dots, y_k$  e o número  $k$  abaixo. As conexões entre as camadas são representadas por linhas azuis, indicando uma conexão completa entre os neurônios de uma camada e os de uma camada adjacente. A camada de saída está destacada por um retângulo vermelho.

Diagrama de uma rede MLP com 3 camadas: entrada, oculta e saída.

{23}------------------------------------------------
## Como definir a topologia de uma rede MLP?

- A topologia mais simples possui 3 camadas:

Quantos neurônios usamos na camada oculta?

- Camada de entrada: corresponde à camada de dados
- **Camada oculta:** de neurônios
- Camada de saída: de neurônios

Diagram illustrating a simple MLP topology for classification. The input layer has 4 nodes (blue squares) representing features:  $x_1$  (Comprimento da sépala),  $x_2$  (Largura da sépala),  $x_3$  (Comprimento da pétala), and  $x_4$  (Largura da pétala). The hidden layer has  $p$  nodes (yellow circles), with a large red question mark indicating the unknown number of neurons. The output layer has 3 nodes (green circles) representing classes:  $y_1$  (setosa),  $y_2$  (versicolor), and  $y_3$  (virginica). Connections are shown between the input and hidden layers, and between the hidden and output layers.

Diagram of an MLP topology for Iris dataset classification.

Diagram illustrating a general MLP topology. The input layer has  $n$  nodes (blue squares) labeled  $x_1, x_2, x_3, \dots, x_n$ . The hidden layer has  $p$  nodes (yellow circles). The output layer has  $k$  nodes (green circles) labeled  $y_1, y_2, y_3, \dots, y_k$ . A red box highlights the output layer. A label  $p: ?$  is shown above the hidden layer, indicating the unknown number of neurons. Connections are shown between the input and hidden layers, and between the hidden and output layers.

General diagram of an MLP topology.

{24}------------------------------------------------
## Como definir a topologia de uma rede MLP?
## Quantos neurônios usamos na camada oculta?

- De forma objetiva **ainda não há como definir.**
- Utiliza-se **experimentação sistemática** para descobrir o que funciona melhor para seu conjunto de dados específico.
- Aplica-se **heurísticas** para estimar o número inicial de neurônios.

{25}------------------------------------------------
## Como definir a topologia de uma rede MLP?

E o problema se estende para as camadas...

**Quantas camadas ocultas são necessárias?**

- Vale a mesma resposta:
  - De forma objetiva **ainda não há como definir**.
  - Utiliza-se **experimentação sistemática** para descobrir o que funciona melhor para seu conjunto de dados específico.
  - Aplica-se **heurísticas** para estimar o número inicial de neurônios.

{26}------------------------------------------------
## Como definir a topologia de uma rede MLP?

- Algumas estratégias populares:
  - **Aleatório:** experimente configurações aleatórias de camadas e nós (neuronios) por camada.
  - **Grid:** tente uma pesquisa sistemática no número de camadas e nós por camada.
  - **Heurística:** tente uma pesquisa direcionada usando algoritmos que para encontrar as configurações ideais tal como algoritmo genético ou bayesiano.
  - **Exaustivo:** experimente todas as combinações de camadas e o número de nós; pode ser viável para pequenas redes e conjuntos de dados.

{27}------------------------------------------------
## Como definir a topologia de uma rede MLP?

- Orientações populares e algumas heurísticas conhecidas:
  - **Uma camada oculta costuma ser suficiente** para a maioria das aplicações;
  - Podem ser necessárias **várias camadas ocultas no caso de domínios com muitas entradas**. Quando precisa-se trabalhar com textos e imagens por exemplo.

{28}------------------------------------------------
## Como definir a topologia de uma rede MLP?

- Orientações populares e algumas heurísticas conhecidas:
- **Poucos neurônios** na camada oculta pode gerar **Underfitting**.
- **Muitos neurônios** na camada oculta pode gerar **Overfitting**.  
Aumenta o tempo de processamento.

|                | Under-fitting | Optimal-fitting | Over-fitting |
|----------------|---------------|-----------------|--------------|
| Regression     |               |                 |              |
| Classification |               |                 |              |

Underfitting in regression: A straight line is drawn through a set of blue data points that form a clear upward curve, failing to capture the underlying trend. Optimal fitting in regression: A smooth, parabolic curve is drawn through the blue data points, capturing the underlying trend. Overfitting in regression: A highly complex, jagged line is drawn through the blue data points, capturing every individual point but failing to capture the overall trend. Underfitting in classification: A single straight line is drawn through a set of blue and red data points, failing to separate the two classes effectively. Optimal fitting in classification: A smooth, curved boundary is drawn between the blue and red data points, separating the two classes. Overfitting in classification: A highly complex, jagged boundary is drawn between the blue and red data points, separating every individual point but failing to capture the overall pattern.

{29}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-20727e57890be6da5692a02d13c0a8ec_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Underfitting in regression: A straight line is drawn through a set of blue data points that form a clear upward curve, failing to capture the underlying trend.
<!-- /IMAGE_DESCRIPTION -->
## Como definir a topologia de uma rede MLP?

- Não existe uma fórmula para selecionar o número ideal de neurônios das camadas ocultas.
- No entanto, algumas dicas e heurísticas estão disponíveis na literatura da área:
  - O número de neurônios ocultos deve estar entre o tamanho da camada de entrada e o tamanho da camada de saída.
  - O número de neurônios ocultos deve ser  $2/3$  do tamanho da camada de entrada, mais o tamanho da camada de saída.
  - O número de neurônios ocultos deve ser menor que o dobro do tamanho da camada de entrada.

{30}------------------------------------------------
## Como definir a topologia de uma rede MLP?

- Uma aproximação pode ser obtida pela regra da pirâmide geométrica proposta por Masters (1993).
- Para uma rede de três camadas com  $n$  neurônios de entrada e  $k$  neurônios de saída, a camada oculta poderia ter:

$$\text{Numero} = \sqrt{n \times k}$$

{31}------------------------------------------------
## Como definir a topologia de uma rede MLP?

- A topologia mais simples possui 3 camadas:

Quantos neurônios usamos na camada oculta?

- Camada de entrada: corresponde à camada de dados
- **Camada oculta:** de neurônios
- Camada de saída: de neurônios

Diagram illustrating a simple MLP topology with 4 input nodes,  $p$  hidden nodes, and 3 output nodes. The input nodes are labeled  $x_1, x_2, x_3, x_4$  and correspond to the features: Comprimento da sépala, Largura da sépala, Comprimento da pétala, and Largura da pétala. The output nodes are labeled  $y_1, y_2, y_3$  and correspond to the classes: setosa, versicolor, and virginica. The number of hidden nodes  $p$  is determined by the formula:

$$p = \sqrt{n \times k} \\ = \sqrt{4 \times 3} \\ = \sqrt{12} = 3,46$$

Diagram of a 4-3 MLP topology for Iris dataset classification.

Diagram illustrating a general MLP topology with  $n$  input nodes,  $p$  hidden nodes, and  $k$  output nodes. The input nodes are labeled  $x_1, x_2, x_3, \dots, x_n$ . The hidden nodes are labeled  $p$  and are enclosed in a red box. The output nodes are labeled  $y_1, y_2, y_3, \dots, y_k$ . A red question mark is placed over the hidden layer, indicating the question of how many hidden nodes to use.

General diagram of an MLP topology with n input nodes, p hidden nodes, and k output nodes.

{32}------------------------------------------------
## Como definir a topologia de uma rede MLP?

- A topologia mais simples possui 3 camadas:

Quantos neurônios usamos na camada oculta?

- Camada de entrada: corresponde à camada de dados
- **Camada oculta:** de neurônios
- Camada de saída: de neurônios

Diagram illustrating a 3-layer MLP topology for classification. The input layer has 4 nodes (blue squares) representing features:  $x_1$  (Comprimento da sépala),  $x_2$  (Largura da sépala),  $x_3$  (Comprimento da pétala), and  $x_4$  (Largura da pétala). The hidden layer has  $p$  nodes (yellow circles). The output layer has 3 nodes (green circles) representing classes:  $y_1$  (setosa),  $y_2$  (versicolor), and  $y_3$  (virginica). The connections are fully connected between adjacent layers. The text  $p = 3 \text{ ou } 4$  is written below the hidden layer.

Diagram of a 3-layer MLP for Iris dataset classification.

Diagram illustrating a general MLP topology. The input layer has  $n$  nodes (blue squares) labeled  $x_1, x_2, x_3, \dots, x_n$ . The hidden layer has  $p$  nodes (yellow circles), with a large red question mark indicating the unknown number of nodes. The output layer has  $k$  nodes (green circles) labeled  $y_1, y_2, y_3, \dots, y_k$ . The connections are fully connected between adjacent layers. The text  $p: ?$  is written above the hidden layer, and the text  $n \quad x \quad p \quad x \quad k$  is written below the layers.

General diagram of an MLP topology.

{33}------------------------------------------------
## Como definir a topologia de uma rede MLP?

- A topologia mais simples possui 3 camadas:

Quantos neurônios usamos na camada oculta?

- Camada de entrada: corresponde à camada de dados
- **Camada oculta:** de neurônios
- Camada de saída: de neurônios

Diagram illustrating a 3-layer MLP topology for Iris dataset classification. The input layer has 4 nodes (blue squares) representing features:  $x_1$  (Comprimento da sépala),  $x_2$  (Largura da sépala),  $x_3$  (Comprimento da pétala), and  $x_4$  (Largura da pétala). The hidden layer has 4 nodes (yellow circles). The output layer has 3 nodes (green circles) representing classes:  $y_1$  (setosa),  $y_2$  (versicolor), and  $y_3$  (virginica). The number of nodes in each layer is indicated above them: 4, 4, and 3 respectively. The text  $p = 4$  (arrendondamos) is written in red below the hidden layer.

Diagram of a 3-layer MLP for Iris dataset classification.

Diagram illustrating a general MLP topology. The input layer has  $n$  nodes (blue squares) labeled  $x_1, x_2, x_3, \dots, x_n$ . The hidden layer has  $p$  nodes (yellow circles), with a large red question mark indicating the unknown number of nodes. The output layer has  $k$  nodes (green circles) labeled  $y_1, y_2, y_3, \dots, y_k$ . The number of nodes in each layer is indicated below them:  $n$ ,  $x$ ,  $p$ ,  $x$ , and  $k$ . A red box highlights the output layer, and a label  $p: ?$  is shown above the hidden layer.

General diagram of an MLP topology.

{34}------------------------------------------------
## Como definir a topologia de uma rede MLP?

Mais um exemplo: Tabela XOR

| x1 | x2 | d |
|----|----|---|
| 0  | 0  | 0 |
| 0  | 1  | 1 |
| 1  | 0  | 1 |
| 1  | 1  | 0 |

The diagram illustrates a Multilayer Perceptron (MLP) architecture with three layers of nodes:

- Input Layer (n):** Represented by blue squares. The nodes are labeled  $x_1, x_2, x_3, \dots, x_n$ .
- Hidden Layer (p):** Represented by yellow circles. The nodes are connected to all input nodes.
- Output Layer (k):** Represented by green circles. The nodes are connected to all hidden nodes. The outputs are labeled  $y_1, y_2, y_3, \dots, y_k$ .

Below the layers, the dimensions are labeled:  $n$  for the input layer,  $p$  for the hidden layer, and  $k$  for the output layer. The connections between layers are fully connected, as indicated by the dense web of blue lines.

Diagram of a fully connected MLP with 3 layers: input (n nodes), hidden (p nodes), and output (k nodes).

{35}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-2837ffdadcdb1e5bababa56b564e56ed_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a 2-4-k MLP architecture for XOR.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-78ff716475b2f65bf01c3a4d02d89fc4_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a 2-4-2 MLP architecture for XOR.
<!-- /IMAGE_DESCRIPTION -->
## Como definir a topologia de uma rede MLP?

Mais um exemplo: Tabela XOR

| x1 | x2 | d |
|----|----|---|
| 0  | 0  | 0 |
| 0  | 1  | 1 |
| 1  | 0  | 1 |
| 1  | 1  | 0 |

The diagram illustrates a Multilayer Perceptron (MLP) architecture for solving the XOR problem. It consists of three layers of nodes:

- Input Layer (x):** Two blue square nodes labeled  $x_1$  and  $x_2$ . A red number **2** is placed below the label  $x$ .
- Hidden Layer (p):** Four yellow circular nodes. A vertical ellipsis is shown between the third and fourth nodes. The label  $p$  is placed below the layer.
- Output Layer (k):** Four green circular nodes labeled  $y_1, y_2, y_3, y_4$ , with a vertical ellipsis between  $y_3$  and  $y_k$ . The label  $k$  is placed below the layer.

Connections are shown as blue lines from each input node to every hidden node, and from every hidden node to every output node.

Diagram of a 2-4-k MLP architecture for XOR.

{36}------------------------------------------------
## Como definir a topologia de uma rede MLP?

Mais um exemplo: Tabela XOR

| x1 | x2 | d |
|----|----|---|
| 0  | 0  | 0 |
| 0  | 1  | 1 |
| 1  | 0  | 1 |
| 1  | 1  | 0 |

The diagram illustrates a Multilayer Perceptron (MLP) architecture for solving the XOR problem. It consists of three layers:

- Input Layer:** Two blue squares representing input nodes  $x_1$  and  $x_2$ . Below them is the number **2** in blue, followed by the letter  $x$ .
- Hidden Layer:** Four yellow circles representing hidden nodes. Below them is the letter  $p$ .
- Output Layer:** Two green circles representing output nodes  $y_1$  and  $y_2$ . Below them is the number **2** in red, preceded by the letter  $x$ .

Connections are shown as blue lines between all nodes in adjacent layers, indicating a fully connected structure. The labels  $x_1$ ,  $x_2$ ,  $y_1$ , and  $y_2$  are placed near their respective nodes.

Diagram of a 2-4-2 MLP architecture for XOR.

{37}------------------------------------------------
## Como definir a topologia de uma rede MLP?

Mais um exemplo: Tabela XOR

| x1 | x2 | d |
|----|----|---|
| 0  | 0  | 0 |
| 0  | 1  | 1 |
| 1  | 0  | 1 |
| 1  | 1  | 0 |

Diagram illustrating a neural network topology for XOR. The input layer has 2 nodes ( $x_1, x_2$ ), the hidden layer has  $p$  nodes, and the output layer has 2 nodes ( $y_1, y_2$ ). A large red question mark is placed over the hidden layer. Below the diagram, the dimensions are labeled: 2 (input),  $x$ ,  $p$  (hidden),  $x$ , and 2 (output).

Diagram of a neural network topology for XOR. It shows an input layer with 2 nodes (x1, x2), a hidden layer with p nodes, and an output layer with 2 nodes (y1, y2). A large red question mark is placed over the hidden layer. Below the diagram, the dimensions are labeled: 2 (input), x, p (hidden), x, and 2 (output).

$$\begin{aligned} p &= \sqrt{n \times k} \\ &= \sqrt{2 \times 2} \\ &= \sqrt{4} = 2 \end{aligned}$$

{38}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-6629e8a87e7552e2454b7c3e9f6d73a0_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a neural network topology for XOR.
<!-- /IMAGE_DESCRIPTION -->
## Como definir a topologia de uma rede MLP?

Mais um exemplo: Tabela XOR

| x1 | x2 | d |
|----|----|---|
| 0  | 0  | 0 |
| 0  | 1  | 1 |
| 1  | 0  | 1 |
| 1  | 1  | 0 |

A diagram of a Multilayer Perceptron (MLP) with three layers. The input layer has two blue square nodes labeled  $x_1$  and  $x_2$ . The hidden layer has two yellow circular nodes. The output layer has two green circular nodes labeled  $y_1$  and  $y_2$ . All nodes in one layer are connected to all nodes in the next layer by blue lines.

Diagram of a 2-2-2 MLP topology for XOR.

2 x 2 x 2

$$\begin{aligned} p &= \sqrt{n \times k} \\ &= \sqrt{2 \times 2} \\ &= \sqrt{4} = 2 \end{aligned}$$

{39}------------------------------------------------
## Como definir a topologia de uma rede MLP?

- E o que fazer quando são necessárias mais camadas?
  - Você pode tentar usar a mesma regra.

The diagram illustrates a Multi-Layer Perceptron (MLP) topology with three layers of nodes. The input layer on the left consists of 30 blue square nodes, labeled  $x_1, x_2, x_3, \dots, x_{30}$ . The hidden layer in the middle consists of 18 yellow circular nodes, with a vertical ellipsis indicating intermediate nodes. The output layer on the right consists of 10 green circular nodes, labeled  $y_1, y_2, y_3, y_4, \dots, y_{10}$ . Every node in the input layer is connected to every node in the hidden layer, and every node in the hidden layer is connected to every node in the output layer, representing a fully connected architecture. Below the layers, the numbers 30, 18, and 10 are displayed, with an 'x' between the input and hidden layer counts, and another 'x' between the hidden and output layer counts.

Diagram of a 3-layer MLP topology.

$$p = \sqrt{n \times k} = \sqrt{30 \times 10} = \sqrt{300} = 17,32$$

<!-- DATALAB_CHUNK 3: pages 41-60 -->

{40}------------------------------------------------

# Como definir a topologia de uma rede MLP?

- E o que fazer quando são necessárias mais camadas?
  - Você pode tentar usar a mesma regra.

The diagram shows two MLP architectures connected by a large blue arrow pointing from left to right, indicating a transformation or addition of a layer.

**Left Architecture:** An input layer with 30 nodes (blue squares, labeled  $x_1, x_2, x_3, \dots, x_{30}$ ) is fully connected to a hidden layer with 18 nodes (yellow circles). This hidden layer is fully connected to an output layer with 10 nodes (green circles, labeled  $y_1, y_2, y_3, y_4, \dots, y_{10}$ ). Below the layers, the dimensions are listed as 30, x, 18, x, 10.

**Right Architecture:** The same input layer (30 nodes) is fully connected to the same hidden layer (18 nodes). A new hidden layer with 14 nodes (red circles) is added between the 18 and 10 layers. This new layer is fully connected to both the 18-node layer and the 10-node output layer. Below the layers, the dimensions are listed as 30, x, 18, x, 14, x, 10. The number 14 is highlighted in red.

Diagram illustrating the process of adding a hidden layer to an MLP based on a heuristic rule.

$$p = \sqrt{n \times k} = \sqrt{30 \times 10} = \sqrt{300} = 17,32$$

$$p = \sqrt{n \times k} = \sqrt{18 \times 10} = \sqrt{180} = 13,41$$

{41}------------------------------------------------

A stylized graphic of a human head silhouette, facing right, filled with a complex network of blue lines and dots. The network is dense and interconnected, representing a neural network topology. The background is black, and the network lines are a vibrant blue.

A stylized graphic of a human head silhouette filled with a complex network of blue lines and dots, representing a neural network topology.
## Como definir a topologia de uma rede MLP?

- Lembre-se: Independentemente da heurística usada para definir a topologia inicial, **você terá que realizar testes para encontrar a melhor topologia para a rede MLP.**

{42}------------------------------------------------

A 3D rendering of a neural network structure. It features a grid of interconnected nodes, represented as small, reflective metallic spheres. These nodes are connected by thin, dark lines, forming a complex web that recedes into the background, creating a sense of depth. The lighting is soft, highlighting the metallic texture of the spheres and the geometric pattern of the connections.

A 3D rendering of a neural network structure, showing interconnected nodes (spheres) and connections (lines), symbolizing a Perceptron or neural network architecture.

<!-- IMAGE_DESCRIPTION: datalab-0d21e56f563c92ea5d8ec3218a00c618_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A 3D rendering of a neural network structure, showing interconnected nodes (spheres) and connections (lines), symbolizing a Perceptron or neural network architecture.
<!-- /IMAGE_DESCRIPTION -->
## Revisitando a rede Perceptron

{43}------------------------------------------------
### Redes Feed Forward

Tarefas Supervisionadas: **classificação** o **e regressão**

A diagram of a single-layer Perceptron. It features two input nodes labeled  $x_1$  and  $x_2$  on the left, each with a small yellow arc below it. Arrows from these inputs point to a single orange output node on the right. The entire structure is enclosed in a red dashed oval. The word "Perceptron" is written below the diagram.

Diagram of a single-layer Perceptron.

A diagram of a two-layer MultiLayer Perceptron. It has two input nodes labeled  $x_1$  and  $x_2$  on the left, each with a small yellow arc below it. Arrows from these inputs connect to two green nodes in a hidden layer. Arrows from the hidden layer nodes connect to a single orange output node on the right.

Diagram of a two-layer MultiLayer Perceptron.

MultiLayer Perceptron

A diagram of a deep neural network on a dark blue background. It shows three layers of purple circular nodes. The first layer is labeled "INPUT" and contains three nodes, with a bracket to its left. The second layer is labeled "HIDDEN" and contains four nodes. The third layer is labeled "OUTPUT" and contains two nodes. Arrows indicate the flow of information from the input layer to the hidden layer, and from the hidden layer to the output layer. On the far left, there are two circular icons: the top one shows a white dog's head, and the bottom one shows a white cat sitting.

Diagram of a deep neural network with input, hidden, and output layers.

<https://sites.icmc.usp.br/andre/research/neural/>

→  
Propagação: fluxo do sinal sempre para frente

{44}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-8b40238e5eff3457dd5ae0011536e2d9_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a neural network with 3 input nodes (blue), 2 hidden nodes (blue), and 2 output nodes (red).
<!-- /IMAGE_DESCRIPTION -->
### Rede Perceptron

- Limitação: só consegue resolver problemas linearmente separáveis.
- O algoritmo de aprendizado desse tipo de rede, procura os coeficientes que traçam a reta que separa linearmente os dados de uma classe de outra.

#0

A scatter plot illustrating linear separability. The plot shows two classes of data points, blue and red, distributed on a 2D plane. A black diagonal line acts as a linear decision boundary, separating the blue points (mostly in the upper-right region) from the red points (mostly in the lower-left region). The label '#0' is positioned above the plot area.

{45}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-68ec8ddd77b91c6e59d90ca84ad64f11_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A scatter plot illustrating linear separability.
<!-- /IMAGE_DESCRIPTION -->
### Rede Perceptron

Revisitando um neurônio artificial j:

The diagram illustrates the internal structure of an artificial neuron  $j$ . On the left, a vertical stack of input values  $x_0, x_1, x_2, x_3, \dots, x_n$  is shown. The input  $x_0 = 1$  is highlighted in an orange box. The inputs  $x_1, x_2, x_3, \dots, x_n$  are grouped in a red box. Each input  $x_i$  is connected to a corresponding weight  $w_{ij}$  in a circle. The weight  $w_{0j}$  is highlighted in a green circle, and a yellow box next to it states "Peso extra conhecido como bias". The weights  $w_{1j}, w_{2j}, w_{3j}, \dots, w_{nj}$  are collectively labeled "Pesos". All weighted inputs are fed into a summation node  $\Sigma$ . The output of the summation is  $v_j$ , which is then passed to an activation function block  $f$ . The output of the activation function is labeled "Saida" and  $y_j$ . The activation function block is labeled "Função de Ativação".

Diagram of an artificial neuron j showing inputs, weights, summation, and activation function.

$$v_j = w_{0j} + \sum_{i=1}^n (x_i \times w_{ij})$$

$$y_j = f(v_j)$$

**X:**  $x_1, x_2, x_3, \dots, x_p$

O vetor  $X$  representa a entrada do neurônio.

Pode ser os dados de entrada da rede ou o sinal de saída de outros neurônios.

{46}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-e22af684d8e56d4c61e61bb5ddac1087_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of an artificial neuron j showing inputs, weights, summation, and activation function.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-41aef1f5efab13d4f38f69e86c726062_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of an artificial neuron j showing inputs, weights, summation, and activation function.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-8f7c0bf0c75a31fee6b0c7392ff57c39_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of an artificial neuron j showing inputs, weights, summation, and activation function.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-789ee0a267b24f34bd1f45313e86c9a4_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of an artificial neuron j showing inputs, weights, summation, and activation function.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-675af5bb2357ce5b510e613d04f66bdc_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of an artificial neuron j showing inputs, weights, summation, and activation function.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-3c99312f83459559d9a301148555d7b9_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of an artificial neuron j showing inputs, weights, summation, and activation function.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-9cd85f266cdb1fb3ad544eb3dd3bd5e4_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of an artificial neuron j showing inputs, weights, summation, and activation function.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-0ccaa59b5bc46884777e728ee3dadaa7_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of an artificial neuron j showing inputs, weights, summation, and activation function.
<!-- /IMAGE_DESCRIPTION -->
### Rede Perceptron

Revisitando um neurônio artificial j:

The diagram illustrates the internal structure of an artificial neuron  $j$ . On the left, a vertical stack of input nodes is shown, enclosed in a red box. The top node is labeled  $x_0 = 1$  and is highlighted with a light orange background. Below it are nodes labeled  $x_1, x_2, x_3, \dots, x_n$ . Each input node  $x_i$  is connected by an arrow to a corresponding weight node  $w_{ij}$  (labeled  $w_{0j}, w_{1j}, w_{2j}, w_{3j}, \dots, w_{nj}$ ). The weight nodes are arranged vertically, with the top one  $w_{0j}$  having a green background. A yellow box labeled "Peso extra conhecido como bias" points to  $w_{0j}$ . The other weight nodes are labeled "Pesos". All weight nodes have arrows pointing to a central summation node  $\Sigma$ . The summation node outputs a value  $v_j$  to an activation function node  $f$ , which is labeled "Função de Ativação". The activation function node outputs the final output  $y_j$ , labeled "Saida".

Diagram of an artificial neuron j showing inputs, weights, summation, and activation function.

$$v_j = w_{0j} + \sum_{i=1}^n (x_i \times w_{ij})$$

$$y_j = f(v_j)$$

**X:**  $x_1, x_2, x_3, \dots, x_p$

O vetor  $X$  representa a entrada do neurônio.

Pode ser os dados de entrada da rede ou o sinal de saída de outros neurônios.

{47}------------------------------------------------
### Rede Perceptron

Revisitando um neurônio artificial j:

The diagram illustrates the internal structure of an artificial neuron  $j$ . On the left, a vertical stack of input nodes is shown, each connected to a corresponding weight node. The inputs are labeled  $x_0, x_1, x_2, x_3, \dots, x_n$ . The weight nodes are labeled  $w_{0j}, w_{1j}, w_{2j}, w_{3j}, \dots, w_{nj}$ . A red rectangular box encloses the entire set of weight nodes. A yellow callout box points to the  $w_{0j}$  node with the text "Peso extra conhecido como bias". Below the weight nodes, the word "Pesos" is written. Arrows from all weight nodes converge on a central summation node, represented by a circle with the Greek letter  $\Sigma$ . The output of this summation is labeled  $v_j$ . This value  $v_j$  is then passed to an activation function block, represented by a square containing the letter  $f$ . An arrow points to this block with the label "Função de Ativação". The final output of the neuron is labeled "Saida" and  $y_j$ .

Diagram of an artificial neuron j in a perceptron network.

$$v_j = w_{0j} + \sum_{i=1}^n (x_i \times w_{ij})$$

$$y_j = f(v_j)$$

**W:**  $w_1, w_2, w_3, \dots, w_p$

O vetor de pesos sinápticos

W. Esses valores ponderam as entradas simulando variações na intensidade do sinal.

{48}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-ec3647789b5c38fb686f2a0833324e79_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of an artificial neuron j in a perceptron network.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-01e00200a536673d6cd0e6d8705047a0_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of an artificial neuron j in a perceptron network.
<!-- /IMAGE_DESCRIPTION -->
### Rede Perceptron

Revisitando um neurônio artificial j:

The diagram illustrates the internal structure of an artificial neuron  $j$ . On the left, a vertical column of input nodes is shown, each containing a weight  $w_{ij}$  for  $i = 0, 1, 2, 3, \dots, n$ . The input  $x_0$  is specifically noted as  $x_0 = 1$ . These inputs are connected to a central summation node  $\Sigma$ , which is highlighted by a red rectangular box. A yellow callout box points to the  $w_{0j}$  node with the text "Peso extra conhecido como bias". Below the summation node, the word "Pesos" is written. The output of the summation node is  $v_j$ , which is then passed to an activation function block labeled  $f$ . The final output of the neuron is  $y_j$ , labeled as "Saida". A red arrow points from the summation node  $\Sigma$  to a green box containing the mathematical formula for the weighted sum and the activation function. An orange box on the right provides a detailed description of the summation node's role.

Peso extra conhecido como bias

Pesos

$$v_j = w_{0j} + \sum_{i=1}^n (x_i \times w_{ij})$$

$$y_j = f(v_j)$$

Saida  $y_j$

Função de Ativação

**$\Sigma$  :**  
Responsável por combinar os valores de entrada. Realiza uma soma ponderada das entradas pelos pesos.

Diagram of an artificial neuron j in a perceptron network.

{49}------------------------------------------------
### Rede Perceptron

Revisitando um neurônio artificial j:

The diagram illustrates the internal structure of an artificial neuron  $j$ . On the left, a vertical column of input nodes is shown. The top node is a green circle labeled  $W_{0j}$ , with an input  $x_0$  and a yellow box below it stating  $x_0 = 1$ . A yellow callout box points to this node with the text "Peso extra conhecido como bias". Below it are blue circles labeled  $W_{1j}$ ,  $W_{2j}$ ,  $W_{3j}$ , and  $W_{nj}$ , each receiving an input  $x_1$ ,  $x_2$ ,  $x_3$ , and  $x_n$  respectively. Vertical ellipses indicate intermediate inputs and weights. Arrows from all these weight nodes point to a central summation node  $\Sigma$ . A yellow callout box labeled "Pesos" points to the arrows entering the summation node. The summation node outputs a value  $v_j$  to a box labeled  $f$ , which is the activation function. A red box encloses the summation node and the activation function box. A red arrow points from the activation function box to a green box containing the equation  $v_j = w_{0j} + \sum_{i=1}^n (x_i \times w_{ij})$ . Below the activation function box, the text "Função de Ativação" is written. The output of the activation function is labeled "Saida" and is  $y_j$ . An orange box on the right contains a description of the activation function.

Peso extra conhecido como bias

Pesos

Função de Ativação

Saida

$y_j = f(v_j)$

**Função de transferência (ou ativação):**  
Responsável pela modulação do sinal propagado, gera valores excitatórios (positivos) ou inibitórios (zero).

Diagram of an artificial neuron j showing inputs, weights, summation, and activation function.

{50}------------------------------------------------
### Rede Perceptron

Revisitando um neurônio artificial  $j$ :

- Existem várias funções de ativação para as redes neurais.
- As clássicas são:
  - Limiar ou degrau
  - Linear
  - Sigmoide: logistica ou tangente hiperbolica
- Geralmente o Perceptron usa a função limiar.

The graph shows a step function on a coordinate system. The vertical axis is labeled  $\varphi(v_j)$  and the horizontal axis is labeled  $\varphi_j$ . The function is zero for negative inputs and jumps to a constant positive value for positive inputs.

(a) **Limiar ou Degrau**

Graph of the Limiar ou Degrau (Step) activation function.

The graph shows a straight line passing through the origin on a coordinate system. The vertical axis is labeled  $\varphi(v_j)$  and the horizontal axis is labeled  $\varphi_j$ .

(b) **Linear**

Graph of the Linear activation function.

The graph shows an S-shaped curve on a coordinate system. The vertical axis is labeled  $\varphi(v_j)$  and the horizontal axis is labeled  $\varphi_j$ . The curve starts near zero for negative inputs and approaches one for positive inputs.

(c) **Logistica**

Graph of the Logistica (Sigmoid) activation function.

The graph shows an S-shaped curve on a coordinate system, similar to the logistic function but centered at the origin. The vertical axis is labeled  $\varphi(v_j)$  and the horizontal axis is labeled  $\varphi_j$ .

(d) **Tangente Hiperbolica**

Graph of the Tangente Hiperbolica (Hyperbolic Tangent) activation function.

{51}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-2d62ff2bded0c21414a0f40fdf8fd537_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Graph of the Limiar ou Degrau (Step) activation function.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-6dda36bad0978e272ca0420b0902b73a_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Graph of the Linear activation function.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-4134b40f9161ec8fcd3c28bdb48f80b0_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Graph of the Logistica (Sigmoid) activation function.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-5314dd284c2a98c866862ee0f0fee301_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Graph of the Tangente Hiperbolica (Hyperbolic Tangent) activation function.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-fd8369b549b3d1a5c848cbd83659cae9_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Graph of the Limiar ou Degrau (step) activation function.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-a96c7e19f53f2350db97a90738a6fb51_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Graph of the Linear activation function.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-e6d17113d3c65cc31531ae8a73fe011f_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Graph of the Logistica (sigmoid) activation function.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-2031413999bae2fee78687b844944be6_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Graph of the Tangente Hiperbolica (hyperbolic tangent) activation function.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-41cd1b0cca77430b41ab28d088e82259_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Graph of the Limiar ou Degrau (Step) activation function.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-36ea45381c7b7fcbc99ce438860f8f37_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Graph of the Linear activation function.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-607a666ece1fb3bad30cbe1e61ea0cc6_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Graph of the Logistica (Sigmoid) activation function.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-b8b4869ad9fcbbc3ae62f07ead5fca1a_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Graph of the Tangente Hiperbolica (Hyperbolic Tangent) activation function.
<!-- /IMAGE_DESCRIPTION -->
### Rede Perceptron

Revisitando um neurônio artificial  $j$ :

- Existem várias funções de ativação para as redes neurais.
- As clássicas são:
  - Limiar ou degrau
  - Linear
  - Sigmoide: logistica ou tangente hiperbolica
- Geralmente o Perceptron usa a função limiar.

A graph showing the step function  $\varphi(v_j)$  against  $\varphi_j$ . The function is zero for negative inputs and jumps to a constant positive value for positive inputs.

Graph of the Limiar ou Degrau (step) activation function.

(a) **Limiar ou Degrau**

A graph showing the linear function  $\varphi(v_j)$  against  $\varphi_j$ . The function is a straight line passing through the origin with a positive slope.

Graph of the Linear activation function.

(b) **Linear**

A graph showing the sigmoid function  $\varphi(v_j)$  against  $\varphi_j$ . The function is an S-shaped curve that maps any real-valued number into the range (0, 1).

Graph of the Logistica (sigmoid) activation function.

(c) **Logistica**

A graph showing the hyperbolic tangent function  $\varphi(v_j)$  against  $\varphi_j$ . The function is an S-shaped curve that maps any real-valued number into the range (-1, 1).

Graph of the Tangente Hiperbolica (hyperbolic tangent) activation function.

(d) **Tangente Hiperbolica**

Usuais em MLP

{52}------------------------------------------------
### Rede Perceptron

Revisitando um neurônio artificial j:

The diagram illustrates the internal structure of an artificial neuron  $j$ . On the left, a vertical column of inputs is shown:  $x_0$ ,  $x_1$ ,  $x_2$ ,  $x_3$ , followed by vertical ellipsis dots, and  $x_n$ . Each input  $x_i$  is connected by an arrow to a corresponding weight node:  $w_{0j}$  (a green circle),  $w_{1j}$ ,  $w_{2j}$ ,  $w_{3j}$ , followed by vertical ellipsis dots, and  $w_{nj}$  (all blue circles). A yellow box next to  $x_0$  contains the text  $x_0 = 1$ . A yellow callout box points to the  $w_{0j}$  node with the text "Peso extra conhecido como bias". Arrows from all weight nodes point towards a central summation node, represented by a circle with the Greek letter  $\Sigma$ . The word "Pesos" is written near these arrows. An arrow labeled  $v_j$  points from the summation node to a square box labeled  $f$ , which represents the activation function. Below this box is the text "Função de Ativação". An arrow labeled "Saída" points from the  $f$  box to a red-outlined rectangle containing the output  $y_j$ .

Diagram of an artificial neuron j showing inputs, weights, summation, and activation function.

$$v_j = w_{0j} + \sum_{i=1}^n (x_i \times w_{ij})$$

$$y_j = f(v_j)$$

**Y:**  
Sinal de saída do neurônio. Se o neurônio estiver em uma camada de saída, corresponde a saída rede.

{53}------------------------------------------------
#### Rede Perceptron - Algoritmo de Treinamento

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
        Para cada atributo i: 1 a n dos dados de X :
             $v_j = v_j + x_i * w_{ij}$ 
         $y_j = f(v_j)$ 
         $erroj = d_j - y_j$ 
        se erroj!=0 entao :
             $delta = \eta * erroj * x_i$ 
             $w_{ij} = w_{ij} + delta$ 
    erroGeral = erroGeral + abs(erroj)
```

{54}------------------------------------------------
#### Rede Perceptron - Algoritmo de Treinamento

The diagram illustrates the forward pass (propagation of the signal) in a Perceptron network. On the left, input variables  $x_0 = 1$ ,  $x_1$ ,  $x_2$ ,  $x_3$ , and  $x_n$  are shown. Each input  $x_i$  is connected to a corresponding weight node  $w_{ij}$  (labeled  $w_{0j}$ ,  $w_{1j}$ ,  $w_{2j}$ ,  $w_{3j}$ , and  $w_{nj}$ ). These weight nodes are collectively labeled "Pesos". Arrows from all weight nodes point to a central summation node  $\Sigma$ . The output of the summation node is passed to an activation function block labeled  $f$ , which is labeled "Função de Ativação". The final output of the network is labeled "Saída". A large blue arrow at the bottom indicates the "Propagação do Sinal" (Signal Propagation) from left to right.

Diagram of a Perceptron network showing the forward pass (propagation of the signal).

{55}------------------------------------------------

Dado um neurônio artificial  $j$ :

The diagram illustrates the internal structure of an artificial neuron  $j$ . On the left, a vertical list of inputs  $x_0 = 1$ ,  $x_1$ ,  $x_2$ ,  $x_3$ , and  $x_n$  (with vertical ellipses between  $x_3$  and  $x_n$ ) is shown. Each input  $x_i$  is connected by an arrow to a corresponding weight node  $w_{ij}$  (where  $w_{0j}$  is at the top and  $w_{nj}$  is at the bottom). Vertical ellipses are also present between the weight nodes  $w_{3j}$  and  $w_{nj}$ . The word "Pesos" is placed to the left of the summation node. Arrows from all weight nodes  $w_{ij}$  point towards a central circular node labeled with the summation symbol  $\Sigma$ . An arrow from the  $\Sigma$  node points to a rectangular box labeled with the activation function  $f$ . Below this box, the text "Função de Ativação" is written with an upward-pointing arrow. Finally, an arrow exits the right side of the  $f$  box, labeled "Saida".

Diagram of an artificial neuron j showing inputs, weights, summation, and activation function.

{56}------------------------------------------------

Dado um neurônio artificial  $j$ :

The diagram illustrates the internal structure of an artificial neuron  $j$ . On the left, a series of input values  $x_0 = 1$ ,  $x_1$ ,  $x_2$ ,  $x_3$ , and  $x_n$  (with vertical ellipses between  $x_3$  and  $x_n$ ) are shown in red. Each input  $x_i$  is connected by a red arrow to a corresponding weight node  $w_{ij}$  (where  $w_{0j}$  is at the top and  $w_{nj}$  is at the bottom). Vertical ellipses are also present between the weight nodes  $w_{3j}$  and  $w_{nj}$ . The word "Pesos" is placed near the weight nodes. Arrows from all weight nodes  $w_{ij}$  point to a central circular node labeled  $\Sigma$ , representing the summation of weighted inputs. From the  $\Sigma$  node, an arrow points to a rectangular box labeled  $f$ , which represents the activation function. A label "Função de Ativação" with an upward-pointing arrow identifies this box. Finally, an arrow labeled "Saida" (Output) exits the  $f$  box to the right.

Diagram of an artificial neuron j showing the propagation of signal from inputs x0, x1, x2, x3, ..., xn through weights w0j, w1j, w2j, w3j, ..., wnj to a summation node $\Sigma$, then through an activation function f to produce the output Saida.

Recebendo os dados de entrada  $X$

{57}------------------------------------------------

Dado um neurônio artificial **j**:

The diagram illustrates the internal structure of an artificial neuron **j**. On the left, a vertical list of inputs  $x_0 = 1$ ,  $x_1$ ,  $x_2$ ,  $x_3$ , and  $x_n$  is shown, with vertical ellipses between  $x_3$  and  $x_n$ . Each input  $x_i$  is connected by an arrow to a corresponding weight node  $w_{ij}$  (represented by a red circle). These weight nodes are collectively labeled "Pesos". The weight node  $w_{0j}$  is also directly connected to the summation node  $\Sigma$  (a white circle). Arrows from all weight nodes  $w_{ij}$  and the direct connection from  $w_{0j}$  point to the summation node  $\Sigma$ . An arrow from  $\Sigma$  points to a rectangular box labeled  $f$ , which represents the "Função de Ativação". An arrow points from below to the  $f$  box, and another arrow points from the  $f$  box to the right, labeled "Saida".

Diagram of an artificial neuron j showing inputs, weights, summation, and activation function.

Ponderando as entradas **X** pelos pesos **W**:  $x_i * w_{ij}$

{58}------------------------------------------------

Dado um neurônio artificial **j**:

The diagram illustrates the internal structure of an artificial neuron **j**. On the left, a vertical column of inputs is shown:  $x_0 = 1$ ,  $x_1$ ,  $x_2$ ,  $x_3$ , followed by vertical ellipsis dots, and  $x_n$ . Each input  $x_i$  is connected by a black arrow to a corresponding weight node  $w_{ij}$  (represented by a light blue circle). These weight nodes are collectively labeled "Pesos". The inputs  $x_1$  through  $x_n$  are also connected by red arrows to a central red circle containing a summation symbol  $\Sigma$ . The weight node  $w_{0j}$  is connected to the  $\Sigma$  node by a black arrow. The output of the summation node is a red arrow pointing to a square box labeled  $f$ , which represents the "Função de Ativação". A black arrow points from below to the  $f$  box. Finally, a black arrow labeled "Saida" exits the  $f$  box to the right.

Diagram of an artificial neuron j showing inputs, weights, summation, and activation function.

Combinando os sinais:  $\text{soma} = w_{0j} + x_1 * w_{1j} + x_2 * w_{2j} + x_3 * w_{3j} + \dots x_n * w_{nj}$

{59}------------------------------------------------

Dado um neurônio artificial  $j$ :

The diagram illustrates the internal structure of an artificial neuron  $j$ . On the left, a vertical list of inputs  $x_0 = 1$ ,  $x_1$ ,  $x_2$ ,  $x_3$ , and  $x_n$  (with vertical ellipses between  $x_3$  and  $x_n$ ) is shown. Each input  $x_i$  is connected by an arrow to a corresponding weight node  $w_{ij}$  (where  $w_{0j}$  is at the top and  $w_{nj}$  is at the bottom). Vertical ellipses are also present between  $w_{3j}$  and  $w_{nj}$ . These weight nodes are collectively labeled "Pesos" (Weights). Arrows from all weight nodes  $w_{ij}$  point towards a central circular node labeled with the summation symbol  $\Sigma$ . An additional arrow from the input  $x_0 = 1$  also points directly to the  $\Sigma$  node. From the  $\Sigma$  node, an arrow points to a red square block labeled with the activation function  $f$ . This block is labeled "Função de Ativação" below it. An arrow points from the bottom into the  $f$  block. Finally, an arrow labeled "Saida" (Output) exits the  $f$  block to the right, pointing to the output  $y_j$ .

Diagram of an artificial neuron j showing inputs, weights, summation, and activation function.

Gerando o sinal de saída:  $y_j = f(\text{soma})$

<!-- DATALAB_CHUNK 4: pages 61-80 -->

{60}------------------------------------------------

# Rede Perceptron - Algoritmo de Treinamento

The diagram illustrates the architecture of a Perceptron network. On the left, a vertical stack of input nodes is shown, labeled  $x_0 = 1$ ,  $x_1$ ,  $x_2$ ,  $x_3$ , and  $x_n$ , with vertical ellipses between  $x_3$  and  $x_n$ . Each input node  $x_i$  is connected to a corresponding weight node  $w_{ij}$  (labeled  $w_{1j}$ ,  $w_{2j}$ ,  $w_{3j}$ , and  $w_{nj}$  with vertical ellipses between  $w_{3j}$  and  $w_{nj}$ ). These weight nodes are collectively labeled "Pesos". Arrows from all weight nodes point to a central summation node, represented by a circle containing the Greek letter  $\Sigma$ . An additional arrow from the input  $x_0 = 1$  also points to the summation node. The output of the summation node is passed to an activation function block, represented by a rectangle containing the symbol  $f$ . This block is labeled "Função de Ativação" below it. The final output of the network is labeled "Saída  $y_j$ ".

A large blue arrow at the top points to the left, labeled "Ajuste dos pesos", indicating the weight adjustment phase of the training algorithm.

Diagram of a Perceptron network architecture showing inputs, weights, summation, and activation function.

{61}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-284768c5ee1a05aa1b9ce396f606a040_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a Perceptron network showing the forward pass (propagation of the signal).
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-255efa1d461fc79b4ed367aaec11637f_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of an artificial neuron j showing the propagation of signal from inputs x0, x1, x2, x3, ..., xn through weights w0j, w1j, w2j, w3j, ..., wnj to a summation node Σ, then through an activation function f to...
<!-- /IMAGE_DESCRIPTION -->
## Rede Perceptron - Algoritmo de Treinamento

The diagram illustrates the architecture of a Perceptron network during the training phase. A large blue arrow at the top points to the left, labeled "Ajuste dos pesos" (Weight Adjustment).

On the left, the input vector  $x$  is shown with components  $x_0 = 1$ ,  $x_1$ ,  $x_2$ ,  $x_3$ , and  $x_n$ . Each input  $x_i$  is connected to a corresponding weight node  $w_{ij}$  (labeled "Pesos").

All weight nodes  $w_{ij}$  and the bias input  $x_0 = 1$  feed into a central summation node  $\Sigma$ .

The output of the summation node  $\Sigma$  is passed to an activation function block  $f$  (labeled "Função de Ativação").

The output of the activation function is the "Saída" (Output)  $y_j$ .

The error calculation is shown in a red box:  $\text{Erro} = d_j - y_j$ .

Diagram of a Perceptron network architecture showing inputs, weights, summation, and activation function.

{62}------------------------------------------------

# Rede Perceptron - Algoritmo de Treinamento

The diagram illustrates the architecture and training process of a Perceptron network. At the top, a large blue arrow labeled "Ajuste dos pesos" (Weight Adjustment) points to the left, indicating the direction of the training process.

The network structure consists of the following components:

- Inputs:** A set of input values  $x_0 = 1$ ,  $x_1$ ,  $x_2$ ,  $x_3$ , ...,  $x_n$ .
- Weights:** Each input  $x_i$  is multiplied by a corresponding weight  $w_{ij}$  (e.g.,  $w_{0j}$ ,  $w_{1j}$ ,  $w_{2j}$ ,  $w_{3j}$ , ...,  $w_{nj}$ ). These weights are collectively labeled as "Pesos" (Weights).
- Summation:** The weighted inputs are summed at a node labeled  $\Sigma$ .
- Activation Function:** The sum is passed to a function block labeled  $f$ , which represents the "Função de Ativação" (Activation Function).
- Output:** The final output of the network is labeled "Saída" (Output) and denoted as  $y_j$ .

A red box labeled "Atualização dos pesos" (Weight Update) is positioned near the summation node, indicating the point where the weights are updated during training.

Diagram of a Perceptron network showing the training process.

{63}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-3766b291e69420b0437ae278b057b5ee_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a Perceptron network architecture showing inputs, weights, summation, and activation function.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-fee87ee34f98efee162e918fbaeec613_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a Perceptron network architecture showing inputs, weights, summation, and activation function.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-feae5a5b6e128162dbced0860fd97b9b_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a Perceptron network showing the training process.
<!-- /IMAGE_DESCRIPTION -->
## Rede Perceptron

Tabela OR

| x1 | x2 | d |
|----|----|---|
| 0  | 0  | 0 |
| 0  | 1  | 1 |
| 1  | 0  | 1 |
| 1  | 1  | 1 |

A 2D plot showing the OR function's decision boundary. The horizontal axis is labeled x1 and the vertical axis is labeled x2. Both axes have tick marks at 0 and 1. Four blue circular data points are plotted at coordinates (0,0), (0,1), (1,0), and (1,1). A solid black line, representing the decision boundary, passes through the points (0,1) and (1,0). The region below and to the left of this line (where x1 + x2 < 1) is the region where the output is 0. The region above and to the right of the line (where x1 + x2 > 1) is the region where the output is 1.

No treinamento, encontramos os pesos:

$$w_{10} = -1.0, w_{11} = 1.0, w_{12} = 1.0$$

Fronteira de decisão:

$$w_{11}x_1 + w_{12}x_2 + w_{10} = 0$$

$$1.0x_1 + 1.0x_2 + -1.0 = 0$$

$$x_1 + x_2 - 1.0 = 0$$

{64}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-c742b64169a38a7f3f990172019878c8_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A 2D plot showing the OR function's decision boundary.
<!-- /IMAGE_DESCRIPTION -->
## Algoritmo Backpropagation

An abstract graphic on the right side of the slide. It features a dark, irregular silhouette on the left that resembles a brain or a cloud. To the right of this silhouette is a glowing blue network of interconnected nodes and lines, forming a spherical shape. The nodes are small dots, and the lines are thin, creating a mesh-like structure that represents a neural network or data connectivity.

Abstract graphic of a neural network structure.

{65}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-2dfa6ac3edfe874f68aa0cbccaa42322_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Abstract graphic of a neural network structure.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-9527c318a7c3357ff7bdce06540aa3a3_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A stylized graphic of a human head silhouette filled with a complex network of blue lines and dots, representing a neural network topology.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-31d640309e19a64318c874023ba0aadd_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Abstract graphic of a neural network structure.
<!-- /IMAGE_DESCRIPTION -->
### Algoritmo de Treinamento para MLP

- O algoritmo **Error Backpropagation** é usado para treinar a rede MLP.
- Foi introduzido na década de 70, mas sua importância só foi reconhecida **por volta de 1986**.
- Corresponde a uma **generalização da regra delta** usada no Perceptron.
- Este algoritmo tem importância também por ter **acabado com o pessimismo** sobre a técnica de redes neurais.
- **Caixa preta:** Na mesma proporção que ajudou, a introdução das camadas ocultas deixaram ainda mais difícil de entender o papel de cada elemento da rede.

{66}------------------------------------------------
### Algoritmo de Treinamento para MLP

- O algoritmo **Error Backpropagation** usa gradiente descendente.
- O método gradiente descendente consiste em encontrar, **de forma iterativa**, os valores dos parâmetros que minimizam determinada função de interesse.
- No caso, consiste em encontrar os pesos que minimizam o erro da rede.

O gráfico ilustra o processo de minimização do custo em um modelo de pesos. O eixo vertical é rotulado 'Custo (pesos)' e o eixo horizontal é rotulado 'Pesos'. Uma curva azul U-shaped representa a função de custo. Um ponto preto na curva é rotulado 'Pesos iniciais'. Uma linha tracejada preta tangente a essa curva é rotulada 'Gradiente'. Uma seta curva com setas menores ao longo dela aponta para o ponto de mínimo da curva, que é rotulado 'Custo mínimo Global'.

Gráfico de custo versus pesos mostrando o gradiente descendente.

{67}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-750677d35a0db0f1a6d44ede4e11d347_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Gráfico de custo versus pesos mostrando o gradiente descendente.
<!-- /IMAGE_DESCRIPTION -->
### Algoritmo de Treinamento para MLP

- O backpropagation possui 2 etapas: **forward** e **backward**. Em cada etapa a rede é percorrida em um sentido.
  - A fase **forward (para frente)** – **propagação** - é utilizada para definir a saída da rede para um dado de entrada.
  - A fase **backward (para trás)** – **retropropagação** - utiliza a saída desejada e a saída gerada pela rede para atualizar os pesos de suas conexões.

O diagrama ilustra a estrutura e o fluxo de dados de uma Rede Neural Artificial (MLP) durante o treinamento. A rede é composta por três camadas:

- Camada de entrada:** Representada por dois nós pretos à esquerda, rotulados  $x_1$  e  $x_2$ .
- Camada Oculta ou Intermediária:** Contém três nós azuis rotulados 1, 2 e 3.
- Camada Oculta ou Intermediária:** Contém dois nós azuis rotulados 4 e 5.
- Camada de Saída:** Contém dois nós azuis rotulados 6 e 7, com saídas finais  $y_6$  e  $y_7$ .

As conexões entre os nós são rotuladas com pesos  $W$ , como  $W_{11}$ ,  $W_{21}$ ,  $W_{31}$ ,  $W_{12}$ ,  $W_{22}$ ,  $W_{32}$ ,  $W_{10}$ ,  $W_{20}$ ,  $W_{30}$ ,  $W_{41}$ ,  $W_{51}$ ,  $W_{42}$ ,  $W_{52}$ ,  $W_{43}$ ,  $W_{53}$ ,  $W_{40}$ ,  $W_{50}$ ,  $W_{64}$ ,  $W_{74}$ ,  $W_{65}$ ,  $W_{75}$ ,  $W_{60}$  e  $W_{70}$ .

Dois fluxos de propagação são indicados por setas horizontais no topo e na base do diagrama:

- Propagação (fase forward):** Indicado por uma seta no topo apontando para a direita, representando o fluxo de dados da entrada para a saída.
- Retropropagação (fase backward):** Indicado por uma seta na base apontando para a esquerda, representando o fluxo de erros de volta para a atualização dos pesos.

Diagrama de uma Rede Neural Artificial (MLP) mostrando as fases de propagação forward e retropropagação backward.

{68}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-27788c2a26d9641e68232a4eff1299b9_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de uma Rede Neural Artificial (MLP) mostrando as fases de propagação forward e retropropagação backward.
<!-- /IMAGE_DESCRIPTION -->
### Algoritmo de Treinamento para MLP

Cada neurônio da rede foi projetado para realizar dois cálculos:

- **Cálculo do sinal de saída:** corresponde a saída  $y$  de cada neurônio, expresso por uma função não linear aplicada à soma ponderada dos pesos pelas entradas em cada neurônio. Acontece na etapa de propagação.
- **Cálculo de uma estimativa do vetor gradiente:** corresponde os gradientes da superfície do erro em relação aos pesos conectados às entradas de um neurônio. Os gradientes são usados na etapa de retropropagação.

{69}------------------------------------------------
### Algoritmo de Treinamento para MLP

- Considere que a topologia da rede já está definida e que há um conjunto de Treino com N pares (X,D), onde:
  - X é o conjunto de entrada:  $\{x_1, x_2, x_3, x_4, \dots, x_Z\}$ , com Z entradas (atributos)
  - D é o conjunto de saídas desejadas:  $\{d_1, d_2, d_3, d_4, \dots, d_M\}$ , com M saídas (uma para cada neurônio da camada de saída)

{70}------------------------------------------------
### Algoritmo de Treinamento para MLP

Diagram of a Multilayer Perceptron (MLP) showing the forward propagation process. The input layer has two nodes labeled x1 and x2. The hidden layer has three nodes. The output layer has two nodes labeled y1 and y2. A red arrow labeled 'Propagação' points from left to right, indicating the direction of information flow from input to output.

1. Iniciar os pesos da rede arbitrariamente com valores não nulos.
2. Apresentar cada dado  $n$  de entrada do conjunto de treino e propagá-lo até a saída da rede (geração dos  $y$ 's da camada de saída), onde  $n = 1$  até  $N$ .
3. **Propagação:** Para cada neurônio  $k$  e entrada  $i$ .

$$v_k(n) = \sum_{i=0}^Z (w_{ki}(n) \times x_i(n)) \qquad y_k(n) = Q(v_k(n))$$

4. **Retropropagação:** Para cada neurônio  $k$ :  $\text{erro}_k = d_k - y_k$

$$\xi(n) = \frac{1}{2} \sum_{k=1}^j \text{erro}_k^2$$

**Energia do erro instantâneo:** combina os erros de todos neurônios da camada de saída para a entrada propagada.

{71}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-f8f8916ae391a1233c13ce738c699109_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a Multilayer Perceptron (MLP) showing the forward propagation process.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-638a308af25f1f56b4456a1fc503f161_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a Multilayer Perceptron (MLP) showing the forward propagation process.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-e5ded249943a879ef58cae5b6b87c576_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a Multilayer Perceptron (MLP) showing the forward propagation process.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-4801e73fa692059f2ca78196e6e907be_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a Multilayer Perceptron (MLP) showing the forward propagation process.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-c98721cd60df9be3ed129ce2345d763d_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a 2-layer MLP showing forward propagation.
<!-- /IMAGE_DESCRIPTION -->
### Algoritmo de Treinamento para MLP

Diagram of a Multilayer Perceptron (MLP) showing the forward propagation process. It consists of three layers of nodes: an input layer with two nodes labeled x1 and x2, a hidden layer with three nodes, and an output layer with two nodes labeled y1 and y2. A red arrow at the top points to the right and is labeled 'Propagação', indicating the direction of information flow from input to output.

1. Iniciar os pesos da rede arbitrariamente com valores não nulos.
2. Apresentar cada dado  $n$  de entrada do conjunto de treino e propagá-lo até a saída da rede (geração dos  $y$ 's da camada de saída), onde  $n = 1$  até  $N$ .
3. **Propagação:** Para cada neurônio  $k$  e entrada  $i$ .

$$v_k(n) = \sum_{i=0}^Z (w_{ki}(n) \times x_i(n)) \qquad y_k(n) = Q(v_k(n))$$

4. **Retropropagação:** Para cada neurônio  $k$ :  $\text{erro}_k = d_k - y_k$

$$\xi(n) = \frac{1}{2} \sum_{k=1}^j \text{erro}_k^2$$

**Energia do erro instantâneo:** combina os erros de todos neurônios da camada de saída para a entrada propagada.

{72}------------------------------------------------
### Algoritmo de Treinamento para MLP

Diagram of a Multilayer Perceptron (MLP) showing the forward propagation process. The input layer has two nodes labeled x1 and x2. The hidden layer has three nodes labeled 1, 2, and 3. The output layer has two nodes labeled y1 and y2. A red arrow labeled 'Propagação' points from left to right, indicating the direction of information flow from input to output.

1. Iniciar os pesos da rede arbitrariamente com valores não nulos.
2. Apresentar cada dado  $n$  de entrada do conjunto de treino e propagá-lo até a saída da rede (geração dos  $y$ 's da camada de saída), onde  $n = 1$  até  $N$ .
3. **Propagação:** Para cada neurônio  $k$  e entrada  $i$ .

$$v_k(n) = \sum_{i=0}^Z (w_{ki}(n) \times x_i(n)) \quad y_k(n) = Q(v_k(n))$$

4. **Retropropagação:** Para cada neurônio  $k$ :  $\text{erro}_k = d_k - y_k$

$$\xi(n) = \frac{1}{2} \sum_{k=1}^j \text{erro}_k^2$$

**Energia do erro instantâneo:** combina os erros de todos neurônios da camada de saída para a entrada propagada.

{73}------------------------------------------------
### Algoritmo de Treinamento para MLP

Diagram of a Multilayer Perceptron (MLP) showing the forward propagation process. The input layer has two nodes labeled x1 and x2. The hidden layer has three nodes labeled 1, 2, and 3. The output layer has two nodes labeled y1 and y2. A red arrow labeled 'Propagação' points from left to right, indicating the direction of information flow. The hidden layer nodes are connected to the output layer nodes. The output layer nodes are labeled y'1, y'2, and y'3, which are the calculated outputs for the hidden layer nodes.

1. Iniciar os pesos da rede arbitrariamente com valores não nulos.
2. Apresentar cada dado  $n$  de entrada do conjunto de treino e propagá-lo até a saída da rede (geração dos  $y$ 's da camada de saída), onde  $n = 1$  até  $N$ .
3. **Propagação:** Para cada neurônio  $k$  e entrada  $i$ .

$$v_k(n) = \sum_{i=0}^Z (w_{ki}(n) \times x_i(n)) \quad y_k(n) = Q(v_k(n))$$

4. **Retropropagação:** Para cada neurônio  $k$ :  $\text{erro}_k = d_k - y_k$

$$\xi(n) = \frac{1}{2} \sum_{k=1}^j \text{erro}_k^2$$

**Energia do erro instantâneo:** combina os erros de todos neurônios da camada de saída para a entrada propagada.

{74}------------------------------------------------
### Algoritmo de Treinamento para MLP

The diagram illustrates a feedforward neural network with two layers. The input layer has two nodes labeled  $x_1$  and  $x_2$ . The hidden layer has three nodes, each represented by a blue circle, with intermediate values  $y'_1$ ,  $y'_2$ , and  $y'_3$  indicated. The output layer has two nodes, represented by red circles and labeled 1 and 2, which produce the final outputs  $y_1$  and  $y_2$ . A red arrow at the top, labeled "Propagação", points from left to right, indicating the direction of forward propagation.

Diagram of a 2-layer MLP showing forward propagation.

1. Iniciar os pesos da rede arbitrariamente com valores não nulos.
2. Apresentar cada dado  $n$  de entrada do conjunto de treino e propagá-lo até a saída da rede (geração dos  $y$ 's da camada de saída), onde  $n = 1$  até  $N$ .
3. **Propagação:** Para cada neurônio  $k$  e entrada  $i$ .

$$v_k(n) = \sum_{i=0}^Z (w_{ki}(n) \times x_i(n)) \qquad y_k(n) = Q(v_k(n))$$

4. **Retropropagação:** Para cada neurônio  $k$ :  $\text{erro}_k = d_k - y_k$

$$\xi(n) = \frac{1}{2} \sum_{k=1}^j \text{erro}_k^2$$

**Energia do erro instantâneo:** combina os erros de todos neurônios da camada de saída para a entrada propagada.

{75}------------------------------------------------
### Algoritmo de Treinamento para MLP

Diagram of an MLP architecture showing the forward pass (propagation). It consists of an input layer with two nodes labeled x1 and x2, a hidden layer with three blue nodes, and an output layer with two red nodes labeled 1 and 2. Red arrows indicate the flow of information from the input layer through the hidden layer to the output layer. A red arrow at the top is labeled 'Propagação'. The output nodes 1 and 2 have corresponding outputs y1 and y2.

1. Iniciar **os pesos da rede arbitrariamente** com valores não nulos.
2. Apresentar cada dado  $n$  de entrada do conjunto de treino e propagá-lo até a saída da rede (geração dos  $y$ 's da camada de saída), onde  $n = 1$  até  $N$ .
3. **Propagação:** Para cada neurônio  $k$  e entrada  $i$ .

$$v_k(n) = \sum_{i=0}^Z (w_{ki}(n) \times x_i(n)) \qquad y_k(n) = Q(v_k(n))$$

4. **Retropropagação:** Para cada neurônio  $k$ :  $\text{erro}_k = d_k - y_k$

$$\xi(n) = \frac{1}{2} \sum_{k=1}^j \text{erro}_k^2$$

**Energia do erro instantâneo:** combina os erros de todos neurônios da camada de saída para a entrada propagada.

{76}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-b68ed2f7c90787b2fcfeb6be5640ecd4_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of an MLP architecture showing the forward pass (propagation).
<!-- /IMAGE_DESCRIPTION -->
### Algoritmo de Treinamento para MLP

$$\begin{aligned} \text{erro}_1 &= d_1 - y_1 \\ \text{erro}_2 &= d_2 - y_2 \end{aligned}$$

The diagram illustrates a Multilayer Perceptron (MLP) with two input nodes ( $x_1, x_2$ ), two hidden nodes, and two output nodes ( $y_1, y_2$ ). A red arrow labeled 'Retropropagação' points from the output layer back towards the input layer, indicating the backward pass of error propagation.

Diagram of a 2-layer MLP showing forward and backward passes.

1. Iniciar os pesos da rede arbitrariamente com valores não nulos.
2. Apresentar cada dado  $n$  de entrada do conjunto de treino e propagá-lo até a saída da rede (geração dos  $y$ 's da camada de saída), onde  $n = 1$  até  $N$ .
3. **Propagação:** Para cada neurônio  $k$  e entrada  $i$ .

$$v_k(n) = \sum_{i=0}^z (w_{ki}(n) \times x_i(n)) \qquad y_k(n) = Q(v_k(n))$$

4. **Retropropagação:** Para cada neurônio  $k$ :  $\text{erro}_k = d_k - y_k$

$$\xi(n) = \frac{1}{2} \sum_{k=1}^j \text{erro}_k^2$$

**Energia do erro instantâneo:** combina os erros de todos neurônios da camada de saída para a entrada propagada.

{77}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-3b281ef3b6cc5f8ba97cbc011bfaac79_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a 2-layer MLP showing forward and backward passes.
<!-- /IMAGE_DESCRIPTION -->
### Algoritmo de Treinamento para MLP
#### 4. Retropropagação:

The diagram illustrates a neural network structure with two input nodes labeled  $x_1$  and  $x_2$ , three hidden nodes, and two output nodes labeled  $y_1$  and  $y_2$ . The output nodes are red circles containing the numbers 1 and 2. A red arrow at the top, labeled 'Retropropagação', points from the output layer back towards the input layer, representing the backward pass of the training algorithm.

Diagram of a neural network with two input nodes (x1, x2), three hidden nodes, and two output nodes (y1, y2). A red arrow labeled 'Retropropagação' points from the output nodes back towards the input nodes, indicating the backward pass of the training algorithm.

...

- Calcular os **gradientes da camada de saída**:  $\delta_k(n) = Q'(v_k(n)) \times erro_k(n)$
- Atualizar os pesos dos neurônios

$$\Delta w_{ki}(n) = \delta_k(n) \times \eta \times y_i(n)$$

Exemplos:  $\eta = \{0.01, 0.1, 0.5, 0.9\}$

onde  $\eta$  é a taxa de aprendizado (learning rate) intervalo típico

- Quanto menor o valor de  $\eta$ , **menor será a variação dos pesos da rede** de uma iteração para outra e mais suave será e **lenta** a trajetória no espaço de busca pelos pesos;
- Quanto maior o valor de  $\eta$ , haverá **maiores modificações nos pesos da rede** de uma iteração para outra e mais **rápido** será a trajetória no espaço de busca pelos pesos; porém isso **não garante uma boa aprendizagem**, a rede pode se tornar instável e oscilar.

{78}------------------------------------------------
### Algoritmo de Treinamento para MLP

Diagram illustrating a neural network structure with 3 input nodes (blue), 2 hidden nodes (blue), and 2 output nodes (red). The output nodes are labeled 1 and 2, with outputs  $y_1$  and  $y_2$  respectively. A red arrow labeled "Retropropagação" points from the output nodes back towards the input nodes, indicating the backward pass of the training algorithm.

Diagram of a neural network with 3 input nodes (blue), 2 hidden nodes (blue), and 2 output nodes (red). The output nodes are labeled 1 and 2, with outputs y1 and y2 respectively. A red arrow labeled 'Retropropagação' points from the output nodes back towards the input nodes, indicating the backward pass of the training algorithm.

4. Retropropagação: onde  $\alpha$  é a constante de momento (momentum rate) intervalo típico ...

• Calcular os gradientes da camada de saída:

• Atualizar os pesos dos neurônios  $\Delta w_{ki}(n) = \delta_k(n) \times \eta \times y_i(n)$

$$w_{ki}(n+1) = w_{ki}(n) + \Delta w_{ki}(n) + \alpha \times w_{ki}(n-1)$$

Exemplos:  $\alpha = \{0.0, 0.1, 0.5,$

$0.9\}$

- Para evitar o perigo de instabilidade do algoritmo, foi introduzindo uma **constante de momento** (momentum rate) :  $\alpha$
- Ela controla e estabiliza a atualização dos pesos.
- Evita que mínimos locais
- Acelera a descida do gradiente em direções com declividade constante.

{79}------------------------------------------------
### Algoritmo de Treinamento para MLP
#### 4. Retropropagação:

...

- Calcular os **gradientes das camadas ocultas**:

$$\delta_k(n) = Q'(v_k(n)) * \sum_{i=1}^t (\delta_i(n) * w_{ik}(n+1))$$

- Atualizar os pesos dos neurônios

$$\Delta w_{ki}(n) = \delta_k(n) \times \eta \times y_i(n)$$

$$w_{ki}(n+1) = w_{ki}(n) + \Delta w_{ki}(n) + \alpha \times w_{ki}(n-1)$$

Diagram of a neural network showing backpropagation. The input layer has two nodes labeled x1 and x2. The hidden layer has three nodes, with the top one highlighted in red and labeled '1'. The output layer has two nodes. A red arrow labeled 'Retropropagação' points from the output layer back to the input layer. Blue arrows show the forward pass from input to output. Black arrows show the backpropagation of error gradients from the output layer back to the hidden layer.

onde j são os neurônios com os quais o neurônio k tem conexão à direita.

Como a camada à direita já sofreu retropropagação, seus pesos já foram atualizados, por isso aparece n+1.

<!-- DATALAB_CHUNK 5: pages 81-100 -->

{80}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-71f0fd23b2f06b621ba89a65ee3c284c_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a neural network showing backpropagation.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-59121d561a4158609b4c354b9ffd0605_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a neural network showing backpropagation.
<!-- /IMAGE_DESCRIPTION -->
## Algoritmo de Treinamento para MLP
### 4. Retropropagação:

...

- Calcular os **gradientes das camadas ocultas**:

$$\delta_k(n) = Q'(v_k(n)) * \sum_{i=1}^t (\delta_i(n) * w_{ik}(n+1))$$

- Atualizar os pesos dos neurônios

$$\Delta w_{ki}(n) = \delta_k(n) \times \eta \times y_i(n)$$

$$w_{ki}(n+1) = w_{ki}(n) + \Delta w_{ki}(n) + \alpha \times w_{ki}(n-1)$$

Diagram of a neural network showing backpropagation. The input layer has two nodes labeled x1 and x2. The hidden layer has three nodes, with the middle one highlighted in red and labeled '2'. The output layer has two nodes. A red arrow labeled 'Retropropagação' points from the output layer back to the input layer, indicating the direction of gradient flow.

onde j são os neurônios com os quais o neurônio k tem conexão à direita.

Como a camada à direita já sofreu retropropagação, seus pesos já foram atualizados, por isso aparece n+1.

{81}------------------------------------------------
## Algoritmo de Treinamento para MLP
### 4. Retropropagação:

...

- Calcular os **gradientes das camadas ocultas**:

$$\delta_k(n) = Q'(v_k(n)) * \sum_{i=1}^t (\delta_i(n) * w_{ik}(n+1))$$

- Atualizar os pesos dos neurônios

$$\Delta w_{ki}(n) = \delta_k(n) \times \eta \times y_i(n)$$

$$w_{ki}(n+1) = w_{ki}(n) + \Delta w_{ki}(n) + \alpha \times w_{ki}(n-1)$$

The diagram illustrates a neural network with three layers: an input layer with nodes  $x_1$  and  $x_2$ ; a hidden layer with three nodes, the bottom one of which is red and labeled '3'; and an output layer with two yellow nodes. Blue arrows represent the forward pass from left to right. Red arrows represent the backward pass (retropropagação) from right to left, as indicated by a red arrow at the top labeled 'Retropropagação'. The red node '3' in the hidden layer is highlighted with a red border and a yellow number '3' inside.

Diagram of a neural network showing forward and backward passes.

onde  $j$  são os neurônios com os quais o neurônio  $k$  tem conexão à direita.

Como a camada à direita já sofreu retropropagação, seus pesos já foram atualizados, por isso aparece  $n+1$ .

{82}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-6334c962f5e106e3331e59946e4d166e_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a neural network showing forward and backward passes.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-ff1a293f8118c0f00dbfeb0ab843d6e6_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A neural network diagram showing three input nodes (1, 2, 3) and one output node (4).
<!-- /IMAGE_DESCRIPTION -->
## Algoritmo de Treinamento para MLP

- Ao final de uma época (passagem de todos os dados do conjunto de treino pela rede)
- Calcular o Erro Médio Quadrado (função de custo)

$$EMQ = \left( \sum_{i=1}^N \xi_i \right) / N$$

Corresponde ao erro médio encontrado para todo o conjunto de treino

É usado como critério de parada. Pode oscilar no início da aprendizagem, mas deve decrescer ao longo do treinamento.

$$\xi(n) = \frac{1}{2} \sum_{k=1}^j \text{erro}_k^2(n)$$

Lembrando que a energia do erro corresponde à combinação dos erros dos neurônios da camada de saída para uma entrada  $n$ .

{83}------------------------------------------------
## Algoritmo de Treinamento para MLP

- Ao final de uma época (passagem de todos os dados do conjunto de treino pela rede)
- Calcular o Erro Médio Quadrado (função de custo)

$$EMQ = \left( \sum_{i=1}^N \xi_i \right) / N$$

Corresponde ao erro médio encontrado para todo o conjunto de treino

Red arrow pointing right, indicating the flow from the formula to the graph.

Custo (pesos)

The graph illustrates the cost function during training. The vertical axis is labeled 'Custo (pesos)' and the horizontal axis is labeled 'Pesos'. A blue U-shaped curve represents the cost function. A black dot on the curve is labeled 'Pesos iniciais'. A dashed line tangent to the curve at this point is labeled 'Gradiente'. Arrows on the curve point towards the bottom, indicating the direction of optimization. The bottom of the curve is labeled 'Custo mínimo Global'.

Graph of Cost (pesos) vs. Pesos showing a U-shaped curve with a minimum point and a gradient line.

{84}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-8156aeb8a8af817a6465e8b75987e6e7_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Red arrow pointing right, indicating the flow from the formula to the graph.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-968957e79781017e2926107f764b6042_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Graph of Cost (pesos) vs. Pesos showing a U-shaped curve with a minimum point and a gradient line.
<!-- /IMAGE_DESCRIPTION -->
## Algoritmo de Treinamento para MLP

**Critérios de parada** do algoritmo backpropagation:

- número pré-definido de épocas;
- valor pré-definido para o erro quadrado médio;
- variação do erro médio nas últimas x épocas inferior a um valor pré-definido (convergência);
- número de padrões corretamente classificados não se alterar;
- combinação desses critérios.

{85}------------------------------------------------
## Revisitando as funções de ativação

A chalkboard filled with handwritten mathematical formulas and diagrams. The formulas include a summation

 $\sum_{h=0}^{\infty} x^{h+1} = \frac{x^2}{1-x}$ 

, a square root expression

 $\sqrt{2436.96 - 2x + 2x^2 - 75}$ 

, a system of equations

 $\begin{cases} xy = 2 \\ cx - cy = 25^2 \\ 2\pi = C \end{cases}$ 

, a fraction

 $\frac{24+x}{y} + \frac{24+3^2}{c} + \frac{2}{x}$ 

, a binomial expansion

 $(x^2 + 34x + \dots)$ 

, and a summation

 $\sum_{x=2}^{n=14!} N_{30} \cdot x - \frac{1}{2} [984 + x9 + p]$ 

. There are also geometric diagrams, including a circle with a shaded sector, a rectangle with an arrow, and a graph of a parabola

 $\beta = 9 + x^2 + y^2$ 

. A white silhouette of a person's head and shoulders is in the foreground on the left.

A chalkboard filled with handwritten mathematical formulas and diagrams, including calculus, algebra, and geometry, with a white silhouette of a person's head and shoulders in the foreground.

{86}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-d261c34ab67ef2c320a5b6a75ceed2c5_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A chalkboard filled with handwritten mathematical formulas and diagrams, including calculus, algebra, and geometry, with a white silhouette of a person's head and shoulders in the foreground.
<!-- /IMAGE_DESCRIPTION -->
## Algoritmo de Treinamento para MLP

- **Funções de ativação (ou de transferência):**
  - Modelos de redes neurais modernas usam funções de ativação não lineares.
  - Permitem que o modelo crie mapeamentos complexos entre as entradas e saídas da rede: essenciais para o aprendizado de dados complexos, como imagens, vídeo, áudio e conjuntos de dados que não são lineares ou têm alta dimensionalidade.

{87}------------------------------------------------
## Algoritmo de Treinamento para MLP

- Existem várias funções de ativação para as redes neurais.

Perceptron

A graph showing the step function  $\varphi(v_j)$  against  $\varphi_j$ . The function is zero for negative inputs and jumps to a constant positive value for positive inputs. The label (a) Limiar ou Degrau is in a yellow box below the graph.

Graph of the Limiar ou Degrau (Step) activation function.

A graph showing the linear function  $\varphi(v_j)$  against  $\varphi_j$ . The function is a straight line passing through the origin with a positive slope. The label (b) Linear is in a yellow box below the graph.

Graph of the Linear activation function.

**MultiLayer Perceptron**  
(não lineares)

A graph showing the sigmoid function  $\varphi(v_j)$  against  $\varphi_j$ . The function is an S-shaped curve that starts near zero, rises steeply through the origin, and approaches one. The label (c) Logistica is in a yellow box below the graph.

Graph of the Logistica (Sigmoid) activation function.

A graph showing the hyperbolic tangent function  $\varphi(v_j)$  against  $\varphi_j$ . The function is an S-shaped curve that passes through the origin, ranging from -1 to 1. The label (d) Tangente Hiperbolica is in a yellow box below the graph.

Graph of the Tangente Hiperbolica (Hyperbolic Tangent) activation function.

{88}------------------------------------------------
## Algoritmo de Treinamento para MLP

A graph of the sigmoid function, which is an S-shaped curve. The x-axis ranges from -6 to 6 with major ticks at -6, -4, -2, 0, 2, 4, and 6. The y-axis ranges from 0 to 1 with major ticks at 0, 0.5, and 1. The curve passes through the point (0, 0.5) and approaches 0 as x goes to negative infinity and 1 as x goes to positive infinity. The area under the curve is shaded in light pink.

Graph of the sigmoid function Q(v\_k) = 1 / (1 + exp(-v\_k)) showing its S-shaped curve between 0 and 1.

- Logística: valores entre  $[0;1]$  :  $Q(v_k) = \frac{1}{1+\exp(-v_k)}$ 
  - Gradiente suave, evitando “saltos” nos valores de saída.
  - Predições claras: Para  $X$  acima de 2 ou abaixo de -2, tende a trazer o valor  $Y$  (a predição) para a borda da curva, muito próximo de 1 ou 0.
  - Problema: Gradiente de fuga - para valores muito altos ou muito baixos de  $X$ , quase não há alteração na predição. Rede não aprende ou o aprendizado é lento. Saídas não centradas em zero. Computacionalmente caro

{89}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-8d1cd1205df3b1bc955934cfcfdacded_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Graph of the sigmoid function Q(v_k) = 1 / (1 + exp(-v_k)) showing its S-shaped curve between 0 and 1.
<!-- /IMAGE_DESCRIPTION -->
## Algoritmo de Treinamento para MLP

The figure shows a graph of the hyperbolic tangent function,  $Q(v_k) = \tanh(v_k)$ . The x-axis ranges from -5 to 5 with major ticks every 1 unit. The y-axis ranges from -1 to 1 with major ticks every 0.2 units. The curve is S-shaped, passing through the origin (0,0). It approaches -1 as  $v_k \rightarrow -\infty$  and approaches 1 as  $v_k \rightarrow \infty$ . The area under the curve for  $v_k > 0$  is shaded in light pink.

Graph of the hyperbolic tangent (tanh) activation function.

- Tangente hiperbólica: valores entre  $[-1;1]$ :  $Q(v_k) = \tanh(v_k)$ 
  - Zero centrado - facilitando a modelagem de entradas com valores fortemente negativos, neutros e fortemente positivos.
  - Problema: Gradiente de fuga também.

{90}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-4661c6f3ed432deb140cecc3563739dd_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Graph of the hyperbolic tangent (tanh) activation function.
<!-- /IMAGE_DESCRIPTION -->
## Algoritmo de Treinamento para MLP

A graph of the Rectified Linear Unit (ReLU) function. The x-axis ranges from -10 to 10 with major ticks at -10, -5, 0, 5, and 10. The y-axis ranges from 0 to 10 with major ticks at 2, 4, 6, 8, and 10. The function is zero for all negative x values and follows the line y=x for all positive x values. The area under the function for x > 0 is shaded in light blue.

Graph of the ReLU function, which is zero for negative inputs and increases linearly for positive inputs.

ReLU: função mais recente

- RELU (RECTIFIED LINEAR UNIT):  $ReLU(x) = \max(0, x)$ 
  - Computacionalmente eficiente - converge rapidamente
  - Não linear - embora pareça uma função linear
  - Problema (Dying ReLU): quando as entradas se aproximam de zero, ou são negativas, o gradiente da função se torna zero, a rede não aprende.

{91}------------------------------------------------

A 3D visualization of a neural network structure. It features a grid of interconnected nodes, represented as small, reflective metallic spheres. These nodes are connected by thin, dark lines, forming a complex, mesh-like pattern that recedes into the background, creating a sense of depth. The lighting is soft, highlighting the metallic texture of the spheres and the geometric arrangement of the connections.

A 3D visualization of a neural network structure, showing interconnected nodes (spheres) and connections (lines), representing the simulation of an MLP.

<!-- IMAGE_DESCRIPTION: datalab-c803f6f6e2c49429d2951832bd0f208d_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Abstract visualization of artificial neural networks with glowing nodes and connections.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-52c2f593b127e110ac6fb67e135f1ad3_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Graph of the ReLU function, which is zero for negative inputs and increases linearly for positive inputs.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-c1448793af3cfb2ec356639a4d0bcaf7_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A 3D visualization of a neural network structure, showing interconnected nodes (spheres) and connections (lines), representing the simulation of an MLP.
<!-- /IMAGE_DESCRIPTION -->
## **Simulando uma rede MLP**

{92}------------------------------------------------
### Simulando o treinamento do XOR

- Conjunto de Treino: (-1 : Falso; 1- Verdadeiro)

Diagrama de uma rede neural simples. À esquerda, duas entradas rotadas como  $x_1$  e  $x_2$  estão conectadas a três neurônios na camada oculta. Cada neurônio da camada oculta é conectado ao único neurônio na camada de saída, que possui uma seta apontando para a direita.

Diagrama de uma rede neural simples com duas camadas de entrada (x1, x2), três neurônios na camada oculta e um neurônio na camada de saída.

| x1 | x2 | d  |
|----|----|----|
| -1 | -1 | -1 |
| -1 | 1  | 1  |
| 1  | -1 | 1  |
| 1  | 1  | -1 |

- Função de Transferência
  - Camada oculta: tangente hiperbólica
  - Camada de saída: tangente hiperbólica
- Taxa de Aprendizagem:  $\eta = 0.3$
- Constante de momentum:  $\alpha = 0$
- Critérios de parada:
  - EMQ = 0.01 ou
  - Épocas: 1000

{93}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-8ba270d9a35a905e16a9b78e6b3ad2b8_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de uma rede neural simples com duas camadas de entrada (x1, x2), três neurônios na camada oculta e um neurônio na camada de saída.
<!-- /IMAGE_DESCRIPTION -->
### Simulando o treinamento do XOR

The diagram illustrates a neural network with three layers. The input layer consists of two nodes labeled  $x_1$  and  $x_2$ . The hidden layer consists of three nodes. The output layer consists of one node. All nodes in one layer are connected to all nodes in the next layer. The output node has an arrow pointing to the right, indicating the final output of the network.

Diagram of a 2x3x1 neural network topology for XOR simulation.

- Observações:
  - Topologia-Exemplo: 2 x 3 x 1
  - Pesos iniciais gerados aleatoriamente
  - Constante de momento = 0 para simplificar o exemplo.

{94}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-b76d1b06cf06e1c28f844e68507b40ed_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a 2x3x1 neural network topology for XOR simulation.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-a4eb9fe011f0e6dc8405f777c5f3f766_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a neural network for XOR simulation.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-796d2e601722450d6456085e0a801e1e_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a neural network for XOR simulation.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-235d1bc77e04effc9c7d98ef154009be_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a neural network for XOR simulation.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-2e18ae7359d8c32e96919956f238ecc5_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a neural network for XOR simulation.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-34d7353cac3d344f71ad82bd1eda40d1_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a neural network for XOR simulation.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-9bafc60bf378685e5e246c3ffad7b792_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a neural network for XOR simulation.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-a7450c80e88ad3f6ca1427ad84020998_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a neural network for XOR simulation.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-796573504cfca9cbe974cf7a125c0494_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a neural network for XOR simulation.
<!-- /IMAGE_DESCRIPTION -->
### Simulando o treinamento do XOR

Propagação

| x1 | x2 | d  |
|----|----|----|
| -1 | -1 | -1 |
| -1 | 1  | 1  |
| 1  | -1 | 1  |
| 1  | 1  | -1 |

The diagram illustrates the forward pass (propagation) of a neural network for XOR simulation. It consists of four layers of nodes:

- Input Layer:** Two input nodes,  $x_1$  and  $x_2$ , both with a bias of  $-1$ . Each input node also receives a bias input  $x_0 = 1$ .
- Hidden Layer 1:** Three nodes labeled 1, 2, and 3. Each node receives inputs from  $x_1$ ,  $x_2$ , and  $x_0$ .
  - Node 1:  $w_{11} = -0.74$ ,  $w_{12} = -0.97$ ,  $w_{10} = 0.85$ . Output:  $Y_1 = ?$
  - Node 2:  $w_{21} = -0.43$ ,  $w_{22} = 0.58$ ,  $w_{20} = 0.19$ . Output:  $Y_2 = ?$
  - Node 3:  $w_{31} = -0.62$ ,  $w_{32} = 0.33$ ,  $w_{30} = 0.65$ . Output:  $Y_3 = ?$
- Hidden Layer 2:** One node labeled 4. It receives inputs from nodes 1, 2, and 3, and a bias input  $x_0 = 1$ .
  - Node 4:  $w_{41} = -0.38$ ,  $w_{42} = -0.87$ ,  $w_{43} = -0.05$ ,  $w_{40} = -0.73$ . Output:  $Y_4 = ?$

Diagram of a neural network for XOR simulation during propagation.

{95}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-d2417b04116c354deccb25d98a84a0fb_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a neural network for XOR simulation during propagation.
<!-- /IMAGE_DESCRIPTION -->
### Simulando o treinamento do XOR

Propagação

$$v_j = w_{j0} + \sum_{i=1}^n (x_i \times w_{ji})$$

$y_j = f(v_j)$ , onde  
 $f(v_j) = \tanh(v_j)$

| x1 | x2 | d  |
|----|----|----|
| -1 | -1 | -1 |
| -1 | 1  | 1  |
| 1  | -1 | 1  |
| 1  | 1  | -1 |

Diagram illustrating the propagation of values through a neural network structure for XOR simulation.

Inputs:  $x_1 = -1$ ,  $x_2 = -1$ . Bias input  $x_0 = 1$  is provided to all nodes.

Weights and Calculations:

- Node 1:  $w_{11} = -0.74$ ,  $w_{12} = -0.97$ ,  $w_{10} = 0.85$ . Calculation:  $v_1 = w_{10} + x_1 \times w_{11} + x_2 \times w_{12} = 0.85 + (-1) \times (-0.74) + (-1) \times (-0.97) = 2.56$ . Output:  $y_1 = \tanh(2.56) = 0.98$ .
- Node 2:  $w_{21} = -0.43$ ,  $w_{22} = 0.58$ ,  $w_{20} = 0.19$ . Output:  $y_2 = ?$ .
- Node 3:  $w_{31} = -0.62$ ,  $w_{32} = 0.33$ ,  $w_{30} = 0.65$ . Output:  $y_3 = ?$ .
- Node 4:  $w_{41} = -0.38$ ,  $w_{42} = -0.87$ ,  $w_{43} = -0.05$ ,  $w_{40} = -0.73$ . Output:  $y_4 = ?$ .

Diagram of a neural network for XOR simulation. It shows three hidden nodes (1, 2, 3) and one output node (4). Inputs x1 and x2 are both -1. Weights are given for each connection. Node 1 has output Y1 = 0.98. Node 2 has output Y2 = ?. Node 3 has output Y3 = ?. Node 4 has output Y4 = ?. A calculation box shows the formula for v1 and the resulting y1.

$$v_1 = w_{10} + x_1 \times w_{11} + x_2 \times w_{12} = 0.85 + (-1) \times (-0.74) + (-1) \times (-0.97) = 2.56$$

$$y_1 = \tanh(2.56) = 0.98$$

{96}------------------------------------------------
### Simulando o treinamento do XOR

Propagação

$$v_j = w_{j0} + \sum_{i=1}^n (x_i \times w_{ji})$$

$y_j = f(v_j)$ , onde  
 $f(v_j) = \tanh(v_j)$

| x1 | x2 | d  |
|----|----|----|
| -1 | -1 | -1 |
| -1 | 1  | 1  |
| 1  | -1 | 1  |
| 1  | 1  | -1 |

Diagram illustrating the propagation of values through a neural network for XOR simulation. The network consists of three hidden nodes (1, 2, 3) and one output node (4).

Inputs:  $x_0 = 1$  (bias),  $x_1 = -1$ ,  $x_2 = -1$ .

Weights and Calculations:

- Node 1:  $w_{10} = 0.85$ ,  $w_{11} = -0.74$ ,  $w_{12} = -0.97$ . Output:  $Y_1 = 0.98$ .
- Node 2:  $w_{20} = 0.19$ ,  $w_{21} = -0.43$ ,  $w_{22} = 0.58$ . Output:  $Y_2 = 0.04$  (circled in red).
- Node 3:  $w_{30} = 0.65$ ,  $w_{31} = -0.62$ ,  $w_{32} = 0.33$ . Output:  $Y_3 = ?$ .
- Node 4:  $w_{40} = -0.73$ ,  $w_{41} = -0.38$ ,  $w_{42} = -0.87$ . Output:  $Y_4 = ?$ .

Calculation for Node 2 output:

$$v_2 = w_{20} + x_1 \times w_{21} + x_2 \times w_{22} = 0.19 + (-1) \times (-0.43) + (-1) \times 0.58 = 0.04$$
$$y_2 = \tanh(0.04) = 0.039 \approx 0.04$$

Diagram of a neural network for XOR simulation. It shows three hidden nodes (1, 2, 3) and one output node (4). Inputs x1 and x2 are both -1. Weights are given for each connection. Node 1 has output Y1 = 0.98. Node 2 has output Y2 = 0.04 (circled in red). Node 3 has output Y3 = ?. Node 4 has output Y4 = ?. A calculation box shows the formula for v2 and the resulting y2.

{97}------------------------------------------------
### Simulando o treinamento do XOR

Propagação

$$v_j = w_{j0} + \sum_{i=1}^n (x_i \times w_{ji})$$

$y_j = f(v_j)$ , onde  
 $f(v_j) = \tanh(v_j)$

| x1 | x2 | d  |
|----|----|----|
| -1 | -1 | -1 |
| -1 | 1  | 1  |
| 1  | -1 | 1  |
| 1  | 1  | -1 |

The diagram illustrates a neural network with four nodes (1, 2, 3, and 4) and their associated weights and outputs.

**Node 1:** Input  $x_0 = 1$  with weight  $w_{10} = 0.85$ . It receives inputs from  $x_1$  ( $w_{11} = -0.74$ ) and  $x_2$  ( $w_{12} = -0.97$ ). Output  $Y_1 = 0.98$ .

**Node 2:** Input  $x_0 = 1$  with weight  $w_{20} = 0.19$ . It receives inputs from  $x_1$  ( $w_{21} = -0.43$ ) and  $x_2$  ( $w_{22} = 0.58$ ). Output  $Y_2 = 0.04$ .

**Node 3:** Input  $x_0 = 1$  with weight  $w_{30} = 0.65$ . It receives inputs from  $x_1$  ( $w_{31} = -0.62$ ) and  $x_2$  ( $w_{32} = 0.33$ ). Output  $Y_3 = 0.73$  (circled in red).

**Node 4:** Input  $x_0 = 1$  with weight  $w_{40} = -0.73$ . It receives inputs from  $Y_1$  ( $w_{41} = -0.38$ ) and  $Y_2$  ( $w_{42} = -0.87$ ). Output  $Y_4 = ?$ .

**Calculation for Node 3:**

$$v_3 = w_{30} + x_1 \times w_{31} + x_2 \times w_{32} = 0.65 + (-1) \times (-0.62) + (-1) \times 0.33 = 0.94$$
$$y_3 = \tanh(0.94) = 0.73$$

Diagram of a neural network for XOR simulation, showing forward propagation through three hidden nodes and one output node.

{98}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-e60c2d24a97a2855d98671d27ea43d0f_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a neural network for XOR simulation, showing forward propagation through three hidden nodes and one output node.
<!-- /IMAGE_DESCRIPTION -->
### Simulando o treinamento do XOR

Propagação

$$v_j = w_{j0} + \sum_{i=1}^n (x_i \times w_{ji})$$

$y_j = f(v_j)$ , onde  
 $f(v_j) = \tanh(v_j)$

| x1 | x2 | d  |
|----|----|----|
| -1 | -1 | -1 |
| -1 | 1  | 1  |
| 1  | -1 | 1  |
| 1  | 1  | -1 |

The diagram illustrates a neural network with four nodes (1, 2, 3, 4) and their connections. The input nodes are 1, 2, and 3, and the output node is 4. The bias node is 0.

Input values:  $x_0 = 1$ ,  $x_1 = -1$ ,  $x_2 = -1$ .

Weights and intermediate values:

- Node 1:  $w_{11} = -0.74$ ,  $w_{12} = -0.97$ ,  $w_{10} = -0.73$ . Intermediate value:  $v_1 = -0.73 + (-1) \times (-0.74) + (-1) \times (-0.97) = 1.98$ . Output:  $y_1 = 0.98$ .
- Node 2:  $w_{21} = -0.43$ ,  $w_{22} = 0.58$ ,  $w_{20} = 0.19$ . Intermediate value:  $v_2 = 0.19 + (-1) \times (-0.43) + (-1) \times 0.58 = -0.36$ . Output:  $y_2 = 0.04$ .
- Node 3:  $w_{31} = -0.62$ ,  $w_{32} = 0.33$ ,  $w_{30} = 0.65$ . Intermediate value:  $v_3 = 0.65 + (-1) \times (-0.62) + (-1) \times 0.33 = 0.94$ . Output:  $y_3 = 0.73$ .
- Node 4:  $w_{41} = -0.38$ ,  $w_{42} = -0.87$ ,  $w_{43} = -0.05$ ,  $w_{40} = -0.73$ . Intermediate value:  $v_4 = -0.73 + 0.98 \times 0.38 + 0.04 \times -0.87 + 0.73 \times -0.05 = -0.4289$ . Output:  $y_4 = \tanh(-0.4289) = -0.39$ .

The final output  $y_4 = -0.39$  is circled in red.

Diagram of a neural network for XOR simulation, showing the propagation of values from input nodes to the output node.

{99}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-67c5b121b58d497a6de5addf4e7bd555_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a neural network for XOR simulation, showing the propagation of values from input nodes to the output node.
<!-- /IMAGE_DESCRIPTION -->
### Simulando o treinamento do XOR
## Retropropagação

| x1 | x2 | d  |
|----|----|----|
| -1 | -1 | -1 |
| -1 | 1  | 1  |
| 1  | -1 | 1  |
| 1  | 1  | -1 |

Neurônio 4 (Camada de Saida)

Erro: -0.6015309621707821

Erro Instantaneo:

0.1809197492250534

Gradiente =

-0.5060213352461277

The diagram illustrates a neural network with three layers: an input layer with two neurons (x1, x2), a hidden layer with three neurons (1, 2, 3), and an output layer with one neuron (4). The bias input x0 is set to 1 for all neurons.

**Forward Pass (Left Diagram):**

- Input layer: x1 = -1, x2 = -1.
- Hidden layer 1: Neuron 1 receives inputs from x0 (1), x1 (-1), and x2 (-1). Weights: W10 = 0.85, W11 = -0.74, W12 = -0.97. Output: Y1 = 0.98.
- Hidden layer 1: Neuron 2 receives inputs from x0 (1), x1 (-1), and x2 (-1). Weights: W20 = 0.19, W21 = -0.43, W22 = 0.58. Output: Y2 = 0.04.
- Hidden layer 1: Neuron 3 receives inputs from x0 (1), x1 (-1), and x2 (-1). Weights: W30 = 0.65, W31 = -0.62, W32 = 0.33. Output: Y3 = 0.73.
- Output layer: Neuron 4 receives inputs from hidden neurons 1, 2, and 3, plus bias x0 (1). Weights: W40 = -0.73, W41 = -0.38, W42 = -0.87, W43 = -0.05. Output: Y4 = -0.39.

**Error Calculation (Right Diagram):**

The error for the output neuron (Neuron 4) is calculated as:

$$\text{erro}_4 = d_4 - y_4$$
$$= -1 - -0,39 =$$
$$\sim -0.61$$

Diagram of a neural network for XOR simulation showing forward pass and error calculation for the output neuron.

<!-- DATALAB_CHUNK 6: pages 101-116 -->

{100}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-985267cff5b5d65ce5c180ff2ef37118_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a neural network for XOR simulation showing forward pass and error calculation for the output neuron.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-98d9a07b2cfa04ebea4e5a4b556d184a_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a neural network with 4 neurons.
<!-- /IMAGE_DESCRIPTION -->
#### Simulando o treinamento do XOR
#### Retropropagação

| x1 | x2 | d  |
|----|----|----|
| -1 | -1 | -1 |
| -1 | 1  | 1  |
| 1  | -1 | 1  |
| 1  | 1  | -1 |

Neurônio 4 (Camada de Saida)

Erro: -0.6015309621707821

Erro Instantaneo:

0.1809197492250534

Gradiente =

-0.5060213352461277

Diagram illustrating the XOR simulation using a neural network. The network consists of three input nodes (x1, x2, x0), three hidden nodes (1, 2, 3), and one output node (4).

Inputs: x1 = -1, x2 = -1, x0 = 1.

Weights and Outputs:

- Hidden Node 1: w11 = -0.74, w12 = -0.97, w10 = 0.85. Output: Y1 = 0.98.
- Hidden Node 2: w21 = -0.43, w22 = 0.58, w20 = 0.19. Output: Y2 = 0.04.
- Hidden Node 3: w31 = -0.62, w32 = 0.33, w30 = 0.65. Output: Y3 = 0.73.
- Output Node 4: w41 = -0.38, w42 = -0.87, w43 = -0.05, w40 = -0.73. Output: Y4 = -0.39.

Diagram of a neural network for XOR simulation. It shows three input nodes (x1, x2, x0) connected to three hidden nodes (1, 2, 3) and one output node (4). Weights and outputs are labeled for each connection. The output node 4 is highlighted in green, indicating it is the focus of the error calculation.

$$\xi(n) = \frac{1}{2} \sum_{k=1}^s \text{erro}_k^2$$

$$\begin{aligned} \text{erro}_4 &= d_4 - y_4 \\ &= -1 - -0.39 = \sim 0.61 \\ \xi((-1, -1)) &= -0.61 \times -0.61 / 2 \\ &= \sim 0.18 \end{aligned}$$

{101}------------------------------------------------
#### Simulando o treinamento do XOR

Yellow arrow pointing left, indicating the direction of backpropagation.

Retropropagação

$$\delta_k(n) = Q'(v_k(n)) \times \text{erro}_k(n)$$

| x1 | x2 | d  |
|----|----|----|
| -1 | -1 | -1 |
| -1 | 1  | 1  |
| 1  | -1 | 1  |
| 1  | 1  | -1 |

Neurônio 4 (Camada de Saida)

Erro: -0.6015309621707821

Erro Instantaneo:

0.1809197492250534

Gradiente =

-0.5060213352461277

Diagram illustrating the forward pass of a neural network for XOR simulation. The network consists of three input neurons (1, 2, 3) and one output neuron (4).

Inputs:  $x_1 = -1$ ,  $x_2 = -1$ ,  $x_0 = 1$ .

Weights and intermediate outputs:

- Neuron 1:  $w_{11} = -0.74$ ,  $w_{12} = -0.97$ ,  $w_{10} = 0.85$ . Output:  $Y_1 = 0.38$ .
- Neuron 2:  $w_{21} = -0.43$ ,  $w_{22} = 0.58$ ,  $w_{20} = 0.19$ . Output:  $Y_2 = 0.04$ .
- Neuron 3:  $w_{31} = -0.62$ ,  $w_{32} = 0.33$ ,  $w_{30} = 0.65$ . Output:  $Y_3 = 0.73$ .
- Neuron 4:  $w_{41} = 0.38$ ,  $w_{42} = -0.87$ ,  $w_{43} = -0.05$ ,  $w_{40} = -0.73$ . Output:  $Y_4 = -0.39$ .

Diagram of a neural network for XOR simulation. It shows three input neurons (1, 2, 3) and one output neuron (4). Inputs x1 and x2 are multiplied by weights w11, w12, w21, w22, w31, w32 and summed with bias x0=1 to produce outputs Y1, Y2, Y3. These are then multiplied by weights w41, w42, w43 and summed with bias w40 to produce the final output Y4.

$$v_4 = w_{40} + y_1 \times w_{41} + y_2 \times w_{42} + y_3 \times w_{43} = -0.73 + 0.98 \times 0.38 + 0.04 \times -0.87 + 0.73 \times -0.05 = -0.4289$$

$$\tanh'(-0.4289) = 1 - \tanh(-0.4289)^2 = 1 - 0.1521 = 0.8479$$

$$\delta_4 = -0.61 \times 0.8479 = -0.5172$$

$$\text{erro}_4 = d_4 - y_4 = -1 - -0.39 = -0.61$$

{102}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-f03929249a5b45fa7fb006ae5a5b88e4_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Yellow arrow pointing left, indicating the direction of backpropagation.
<!-- /IMAGE_DESCRIPTION -->
#### Simulando o treinamento do XOR

A large yellow arrow pointing to the left, with the word 'Retropropagação' (Backpropagation) written in black text inside it.

$$\Delta w_{ki}(n) = \delta_k(n) \times \eta \times y_i(n)$$

| x1 | x2 | d  |
|----|----|----|
| -1 | -1 | -1 |
| -1 | 1  | 1  |
| 1  | -1 | 1  |
| 1  | 1  | -1 |

Neurônio 4 (Camada de Saida)  
 Erro: -0.6015309621707821  
 Erro Instantaneo:  
 0.1809197492250534

$$\text{Gradiente} = -0.5060213352461277$$

A diagram of a neural network with 4 input nodes (x0, x1, x2, x3) and 4 output nodes (y1, y2, y3, y4). The nodes are arranged in two columns. The left column has nodes 1, 2, 3, and 4. The right column has nodes 1, 2, 3, and 4. Weights are labeled on the connections between nodes. For example, W10 = 0.85, W11 = -0.74, W12 = -0.97, W21 = -0.43, W22 = 0.58, W31 = -0.62, W32 = 0.33, W40 = 0.65, W41 = -0.38, W42 = -0.87, W43 = -0.05. The output nodes have values: Y1 = 0.98, Y2 = 0.04, Y3 = 0.73, Y4 = -0.39. The error for node 4 is -0.6015309621707821. The error for node 4 is also shown as -0.5060213352461277.

$$\eta = 0.3$$

$$\alpha = 0$$

$$\delta_4 = -0.61 \times 0.8479 = -0.5...$$

$$w_{40} = w_{40} + (-0.50 \times 0.3 \times 1) = -0.73 - 0.15 = -0.88$$

$$w_{ki}(n+1) = w_{ki}(n) + \Delta w_{ki}(n) + \alpha \times w_{ki}(n-1)$$

{103}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-ef0572dbc0f9178ab84cc23b3753e18e_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A large yellow arrow pointing to the left, with the word 'Retropropagação' (Backpropagation) written in black text inside it.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-240d66bb698171f40d1acd5b0c098e4f_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A large yellow arrow pointing to the left, with the word 'Retropropagação' (Backpropagation) written in black text inside it.
<!-- /IMAGE_DESCRIPTION -->
#### Simulando o treinamento do XOR

A large yellow arrow pointing to the left, with the word 'Retropropagação' (Backpropagation) written in black text inside it.

$$\Delta w_{ki}(n) = \delta_k(n) \times \eta \times y_i(n)$$

| x1 | x2 | d  |
|----|----|----|
| -1 | -1 | -1 |
| -1 | 1  | 1  |
| 1  | -1 | 1  |
| 1  | 1  | -1 |

Neurônio 4 (Camada de Saida)  
 Erro: -0.6015309621707821  
 Erro Instantaneo:  
 0.1809197492250534  
 Gradiente =  
 -0.5060213352461277

A neural network diagram showing three input nodes (1, 2, 3) and one output node (4). Each input node has a bias input x0 = 1. Weights are labeled on the connections: W10=0.85, W11=-0.74, W12=-0.97, W20=0.19, W21=-0.43, W22=0.58, W30=0.65, W31=-0.62, W32=0.33, W40=-0.88, W41=-0.23, W42=-0.87, W43=-0.05. Outputs are Y1=0.98, Y2=0.04, Y3=0.73, and Y4=-0.39. The weight W41 is circled in red.

$\eta=0.3$   
 $\alpha = 0$   
 $\delta 4 = -0,61 \times 0,8479 = -0,5...$   
 $w_{41} = w_{41} + (-0,50 \times 0,3 \times 0,98) = 0,38 - 0,147 = 0,23$

$$w_{ki}(n+1) = w_{ki}(n) + \Delta w_{ki}(n) + \alpha \times w_{ki}(n-1)$$

{104}------------------------------------------------
#### Simulando o treinamento do XOR

Retropropagação

$$\Delta w_{ki}(n) = \delta_k(n) \times \eta \times y_i(n)$$

| x1 | x2 | d  |
|----|----|----|
| -1 | -1 | -1 |
| -1 | 1  | 1  |
| 1  | -1 | 1  |
| 1  | 1  | -1 |

Neurônio 4 (Camada de Saida)  
 Erro: -0.6015309621707821  
 Erro Instantaneo:  
 0.1809197492250534  
 Gradiente =  
 -0.5060213352461277

Diagram details:  
 - Input nodes: x1, x2, x0=1  
 - Hidden nodes: 1, 2, 3  
 - Output node: 4  
 - Weights: W10=0.85, W11=-0.74, W12=-0.97, W20=0.19, W21=-0.43, W22=0.58, W30=0.65, W31=-0.62, W32=0.33, W40=-0.88, W41=-0.23, W42=-0.87, W43=-0.05  
 - Outputs: Y1=0.98, Y2=0.04, Y3=0.73, Y4=-0.39  
 - Node 4 is highlighted in green, and W42 is circled in red.

Diagram of a neural network for XOR simulation. It shows three input nodes (x1, x2, x0=1) connected to three hidden nodes (1, 2, 3) and one output node (4). Weights are labeled on the connections, and outputs are shown for each node. Node 4 is highlighted in green, and its weight W42 is circled in red.

$\eta=0.3$   
 $\alpha=0$   
 $\delta_4 = -0,61 \times 0,8479 = -0,5...$   
 $w_{42} = w_{42} + (-0,50 \times 0,3 \times 0,04) = -0,87 - 0,006 = -0,876$

$$w_{ki}(n+1) = w_{ki}(n) + \Delta w_{ki}(n) + \alpha \times w_{ki}(n-1)$$

{105}------------------------------------------------
#### Simulando o treinamento do XOR

Retropropagação

$$\Delta w_{ki}(n) = \delta_k(n) \times \eta \times y_i(n)$$

| x1 | x2 | d  |
|----|----|----|
| -1 | -1 | -1 |
| -1 | 1  | 1  |
| 1  | -1 | 1  |
| 1  | 1  | -1 |

Neurônio 4 (Camada de Saida)  
 Erro: -0.6015309621707821  
 Erro Instantaneo:  
 0.1809197492250534  
 Gradiente =  
 -0.5060213352461277

Diagram of a neural network for XOR simulation. It shows three input nodes (1, 2, 3) and one output node (4). Each input node has a bias input x0 = 1. Weights are labeled on the connections: W10=0.85, W11=-0.74, W12=-0.97, W20=0.19, W21=-0.43, W22=0.58, W30=0.65, W31=-0.62, W32=0.33, W40=-0.88, W41=-0.23, W42=-0.87, and W43=-0.15 (circled in red). Outputs are Y1=0.98, Y2=0.04, Y3=0.73, and Y4=-0.39.

$\eta=0.3$   
 $\alpha = 0$   
 $\delta_4 = -0,61 \times 0,8479 = -0,5...$   
 $w_{43} = w_{43} + (-0,50 \times 0,3 \times 0,73) = -0,05 - 0,1095 = -0,1595$

$$w_{ki}(n+1) = w_{ki}(n) + \Delta w_{ki}(n) + \alpha \times w_{ki}(n-1)$$

{106}------------------------------------------------
#### Simulando o treinamento do XOF
#### Retropropagação

| x1 | x2 | d  |
|----|----|----|
| -1 | -1 | -1 |
| -1 | 1  | 1  |
| 1  | -1 | 1  |
| 1  | 1  | -1 |

Diagram of a neural network with 4 layers. Layer 1 (input) has nodes x1 and x2 with values -1. Layer 2 (hidden) has nodes 1 and 2. Layer 3 (hidden) has node 3. Layer 4 (output) has node 4. Weights are labeled on connections. Outputs Y1=0.98, Y2=0.04, Y3=0.73, Y4=-0.39 are shown. A bias node x0=1 is connected to all nodes in layers 2, 3, and 4.

Diagram of a neural network with 4 layers. Layer 1 (input) has nodes x1 and x2 with values -1. Layer 2 (hidden) has nodes 1 and 2. Layer 3 (hidden) has node 3. Layer 4 (output) has node 4. Weights are labeled on connections. Outputs Y1=0.98, Y2=0.04, Y3=0.73, Y4=-0.39 are shown. A bias node x0=1 is connected to all nodes in layers 2, 3, and 4.

$$v_1 = w_{10} + x_1 \times w_{11} + x_2 \times w_{12} = 0.85 + -1 \times -0.74 + -1 \times -0.97 = 2,56$$

$$\tanh'(2,56) = 1 - \tanh(2,56)^2 = 1 - 0,97^2 = 0,03$$

$$\delta_4 = -0,5...$$

$$\delta_1 = 0,03 * [-0,5 * 0.23] = \sim -0,003$$

- Camada Oculta
- Gradiente Neurônio 1: -0.002781842410268394
- Gradiente Neurônio 2: 0.4444999763647362
- Gradiente Neurônio 3: 0.03803417896970686

$$\delta_k(n) = Q'(v_k(n)) * \sum_{i=1}^t (\delta_j(n) * w_{jk}(n+1))$$

{107}------------------------------------------------
#### Simulando o treinamento do XOF
#### Retropropagação

$$w_{10} = w_{10} + (-0,0027 \times 0,3 \times 1) = 0,85 + -0,00081 = 0,84$$

| x1 | x2 | d  |
|----|----|----|
| -1 | -1 | -1 |
| -1 | 1  | 1  |
| 1  | -1 | 1  |
| 1  | 1  | -1 |
#### Camada Oculta

- Gradiente Neurônio 1: -0.002781842410268394
- Gradiente Neurônio 2: 0.4444999763647362
- Gradiente Neurônio 3: 0.03803417896970686

Diagram illustrating the neural network structure and weights during backpropagation. The network consists of 4 layers (0 to 3) and 4 nodes (1 to 4). Weights are shown on connections between nodes. The diagram shows the forward pass results (Y1, Y2, Y3, Y4) and the backward pass (delta values) for the hidden nodes.

Diagram of a neural network with 4 layers. Layer 0 (input) has nodes x0=1, x1=-1, x2=-1. Layer 1 (hidden) has nodes 1, 2, 3. Layer 2 (hidden) has node 4. Layer 3 (output) has node 4. Weights are shown on connections. Node 1 output is Y1=0.98, Node 2 output is Y2=0.04, Node 3 output is Y3=0.73, Node 4 output is Y4=-0.39. A red circle highlights W10=0.84.

$$v_1 = w_{10} + x_1 \times w_{11} + x_2 \times w_{12} = 0.85 + -1 \times -0.74 + -1 \times -0.97 = 2,56$$

$$\tanh'(2,56) = 1 - \tanh(2,56)^2 = 1 - 0,97 = 0,03$$

$$\delta_4 = -0,5...$$

$$\delta_1 = 0,03 * [-0,5 * 0.23] = \sim -0,003$$

$$\Delta w_{ki}(n) = \delta_k(n) \times \eta \times y_i(n)$$

$$w_{ki}(n+1) = w_{ki}(n) + \Delta w_{ki}(n) + \alpha \times w_{ki}(n-1)$$

{108}------------------------------------------------
#### Simulando o treinamento do XOF
#### Retropropagação

$$w_{11} = w_{11} + (-0,0027 \times 0,3 \times -1) = -0,74 + 0,00081 = -0,739 = \sim -074$$

| x1 | x2 | d  |
|----|----|----|
| -1 | -1 | -1 |
| -1 | 1  | 1  |
| 1  | -1 | 1  |
| 1  | 1  | -1 |
#### Camada Oculta

- Gradiente Neurônio 1: -0.002781842410268394
- Gradiente Neurônio 2: 0.4444999763647362
- Gradiente Neurônio 3: 0.03803417896970686

Diagram of a neural network structure with 4 layers (0 to 3).  
 Layer 0 (Input):  $x_0 = 1$ ,  $x_1 = -1$ ,  $x_2 = -1$ .  
 Layer 1 (Hidden): Nodes 1, 2, 3.  
 Layer 2 (Hidden): Node 4.  
 Layer 3 (Output): Node 4.  
 Weights and outputs:  
 - Node 1:  $w_{10} = 0.84$ ,  $w_{11} = -0.74$  (highlighted),  $w_{12} = -0.97$ . Output  $Y_1 = 0.98$ .  
 - Node 2:  $w_{21} = -0.43$ ,  $w_{22} = 0.58$ . Output  $Y_2 = 0.04$ .  
 - Node 3:  $w_{31} = -0.62$ ,  $w_{32} = 0.33$ . Output  $Y_3 = 0.73$ .  
 - Node 4:  $w_{41} = -0.23$ ,  $w_{42} = -0.87$ ,  $w_{43} = -0.15$ . Output  $Y_4 = -0.39$ .  
 Bias weights:  $w_{10} = 0.84$ ,  $w_{20} = 0.19$ ,  $w_{30} = 0.65$ ,  $w_{40} = -0.88$ .

Diagram of a neural network with 4 layers. Layer 0 (input) has nodes x0=1, x1=-1, x2=-1. Layer 1 (hidden) has nodes 1, 2, 3. Layer 2 (hidden) has node 4. Layer 3 (output) has node 4. Weights are shown on connections. Node 1 output is Y1=0.98, Node 2 output is Y2=0.04, Node 3 output is Y3=0.73, Node 4 output is Y4=-0.39. A red oval highlights w11 = -0.74.

$$v_1 = w_{10} + x_1 \times w_{11} + x_2 \times w_{12} = 0.85 + -1 \times -0.74 + -1 \times -0.97 = 2,56$$

$$\tanh'(2,56) = 1 - \tanh(2,56)^2 = 1 - 0,97 = 0,03$$

$$\delta_4 = -0,5...$$

$$\delta_1 = 0,03 * [-0,5 * 0.23] = \sim -0,003$$

$$\Delta w_{ki}(n) = \delta_k(n) \times \eta \times y_i(n)$$

$$w_{ki}(n+1) = w_{ki}(n) + \Delta w_{ki}(n) + \alpha \times w_{ki}(n-1)$$

{109}------------------------------------------------
#### Simulando o treinamento do XOF
#### Retropropagação

$$w_{12} = w_{12} + (-0,0027 \times 0,3 \times -1) = -0,97 + 0,00081 = -0,96919 \approx -0,97$$

$$v_1 = w_{10} + x_1 \times w_{11} + x_2 \times w_{12} = 0.85 + -1 \times -0.74 + -1 \times -0.97 = 2,56$$

$$\tanh'(2,56) = 1 - \tanh(2,56)^2 = 1 - 0,97 = 0,03$$

$$\delta_4 = -0,5...$$

$$\delta_1 = 0,03 * [-0,5 * 0.23] = \sim -0,003$$

| x1 | x2 | d  |
|----|----|----|
| -1 | -1 | -1 |
| -1 | 1  | 1  |
| 1  | -1 | 1  |
| 1  | 1  | -1 |

Diagram of a neural network with 4 neurons. Neurons 1, 2, and 3 are in the hidden layer, and neuron 4 is in the output layer. Inputs x1 and x2 are multiplied by -1. Weights are shown on connections: W10=0.84, W11=-0.74, W12=-0.97, W20=0.19, W21=-0.43, W22=0.58, W30=0.65, W31=-0.62, W32=0.33, W40=-0.88, W41=-0.23, W42=-0.87, W43=-0.15. Outputs are Y1=0.98, Y2=0.04, Y3=0.73, Y4=-0.39. A red oval highlights W12=-0.97.

- Camada Oculta
- Gradiente Neurônio 1: -0.002781842410268394
- Gradiente Neurônio 2: 0.4444999763647362
- Gradiente Neurônio 3: 0.03803417896970686

$$\Delta w_{ki}(n) = \delta_k(n) \times \eta \times y_i(n)$$

$$w_{ki}(n+1) = w_{ki}(n) + \Delta w_{ki}(n) + \alpha \times w_{ki}(n-1)$$

{110}------------------------------------------------
#### Simulando o treinamento do XOR
#### Retropropagação

| x1 | x2 | d  |
|----|----|----|
| -1 | -1 | -1 |
| -1 | 1  | 1  |
| 1  | -1 | 1  |
| 1  | 1  | -1 |

Diagram illustrating the forward pass of a neural network for XOR simulation. The network consists of three hidden nodes (1, 2, 3) and one output node (4). Inputs are  $x_1 = -1$  and  $x_2 = -1$ . Each hidden node also receives a bias input  $x_0 = 1$ . Weights are shown for all connections. Node 1 outputs  $Y_1 = 0.98$ , Node 2 outputs  $Y_2 = 0.04$ , Node 3 outputs  $Y_3 = 0.73$ , and Node 4 outputs  $Y_4 = -0.39$ . The weight  $W_{12} = -0.97$  is circled in red.

Diagram of a neural network for XOR simulation. It has three hidden nodes (1, 2, 3) and one output node (4). Inputs are x1 and x2, both set to -1. Each hidden node also receives a bias input x0 = 1. Weights are shown for all connections. Node 1 outputs Y1 = 0.98, Node 2 outputs Y2 = 0.04, Node 3 outputs Y3 = 0.73, and Node 4 outputs Y4 = -0.39. The weight W12 = -0.97 is circled in red.

- Camada Oculta
- Gradiente Neurônio 1: -0.002781842410268394
- Gradiente Neurônio 2: 0.4444999763647362
- Gradiente Neurônio 3: 0.03803417896970686

$$\Delta w_{ki}(n) = \delta_k(n) \times \eta \times y_i(n)$$

$$w_{ki}(n+1) = w_{ki}(n) + \Delta w_{ki}(n) + \alpha \times w_{ki}(n-1)$$

{111}------------------------------------------------
#### Simulando o treinamento do XOR
### Função de Custo

- Época: 0 - Erro médio quadrado: 0.6382619197564264
- Época: 1 - Erro médio quadrado: 0.6217486395123959
- Época: 2 - Erro médio quadrado: 0.5710208319681408
- Época: 3 - Erro médio quadrado: 0.5473148706283855
- Época: 4 - Erro médio quadrado: 0.5355908980006899
- Época: 5 - Erro médio quadrado: 0.5285727922709779
- ...
- Época: 446 - Erro médio quadrado: 0.009972902630117393

{112}------------------------------------------------
#### Simulando o treinamento do XOR

The diagram illustrates a neural network structure for XOR simulation. It consists of three layers: an input layer with two nodes labeled  $x_1$  and  $x_2$ ; a hidden layer with three nodes; and an output layer with one node. All nodes in adjacent layers are fully connected by lines. The output node has an arrow pointing to the right, indicating the final result of the simulation.

Diagram of a neural network for XOR simulation.
### Pesos Finais:

- Camada Oculta
  - Neuronio: 1:  $w[10]=2.545363016862031$ ,  
 $w[11]=-1.8662421473793356$ ,  $w[12]=-1.7588858258650666$
  - Neuronio: 2:  $w[20]=0.1914996892738543$ ,  
 $w[21]=-0.4332485003836084$ ,  $w[22]=0.5833743630800029$
  - Neuronio: 3:  $w[30]=0.655200823402003$   
 $w[31]=-0.6209562373205424$   $w[32]=0.3376845283666482$
- Camada de Saida
  - Neuronio: 4:  $w[40]=0.36071557007625865$ ,  
 $w[41]=2.388002191368662$ ,  $w[42]=4.357544216452374$ ,  
 $w[43]=-5.4985276529155485$

{113}------------------------------------------------
### Implementando uma MLP
## `sklearn.neural_network.MLPClassifier`

```
class sklearn.neural_network.MLPClassifier(hidden_layer_sizes=(100,), activation='relu', *, solver='adam', alpha=0.0001, batch_size='auto', learning_rate='constant', learning_rate_init=0.001, power_t=0.5, max_iter=200, shuffle=True, random_state=None, tol=0.0001, verbose=False, warm_start=False, momentum=0.9, nesterovs_momentum=True, early_stopping=False, validation_fraction=0.1, beta_1=0.9, beta_2=0.999, epsilon=1e-08, n_iter_no_change=10, max_fun=15000)
```

[\[source\]](#)

- **hidden\_layer\_sizes** : vetor com a quantidade de neurônios da camada oculta - default=(100,)
- **activation**{'identity', 'logistic', 'tanh', 'relu'}, default='relu' - função de ativação para camada oculta
  - 'identity', sem ativação, retorna  $f(x) = x$
  - 'logistic', função sigmoide logística , retorna  $f(x) = 1 / (1 + \exp(-x))$ .
  - 'tanh', função tangente hiperbólica, retorna  $f(x) = \tanh(x)$ .
  - 'relu', função *rectified linear unit*, retorna  $f(x) = \max(0, x)$

{114}------------------------------------------------
### Implementando uma MLP

- **solver**{'lbfgs', 'sgd', 'adam'}, default='adam'  
Usado para otimizacao dos pesos.
  - 'sgd' : refere-se ao gradiente descente estocástico..
  - 'adam' : refere-se ao otimizador baseado em gradiente.
  - 'lbfgs' : otimizador quasi-Newton methods.
- **learning\_rate\_init** float, default=0.001  
Taxa de aprendizagem, usada quando='sgd' ou 'adam'.
- **max\_iter** int, default=200 - Numero máximo de iteracoes.
- **verbose** bool, default=False – Exibe mensagens sobre a rede.
- **Momentum** float, default=0.9 - Constante de momento para atualização do gradiente .  
Deve estar entre [0;1]. Somente usar quando solver solver='sgd'.

{115}------------------------------------------------
## Dinâmica

- **Atividade 1:** Implemente em Python o algoritmo de treinamento da rede MultiLayer Perceptron para o XOR.

| x1 | x2 | d |
|----|----|---|
| 0  | 0  | 0 |
| 0  | 1  | 1 |
| 1  | 0  | 1 |
| 1  | 1  | 0 |

The diagram illustrates a Multi-Layer Perceptron (MLP) architecture for the XOR problem. It consists of three layers: an input layer with 2 nodes (blue squares labeled  $x_1$  and  $x_2$ ), a hidden layer with 2 nodes (yellow circles), and an output layer with 2 nodes (green circles labeled  $y_1$  and  $y_2$ ). All nodes in adjacent layers are fully connected. Below the diagram, the layer sizes are indicated as 2, 2, and 2, separated by 'x' symbols. The first '2' is blue, the second '2' is red, and the third '2' is blue.

Diagram of a 2-2-2 Multi-Layer Perceptron (MLP) architecture for XOR.
