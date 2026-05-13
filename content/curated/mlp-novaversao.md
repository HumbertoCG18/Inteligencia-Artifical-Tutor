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
  - Tabela OR
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
- **4. Retropropagação:**
- **Algoritmo de Treinamento para MLP**
- **4. Retropropagação:**
- **Algoritmo de Treinamento para MLP**
  - Critérios de parada do algoritmo backpropagation:
- **Revisitando as funções de ativação**
- **Algoritmo de Treinamento para MLP**
- **Simulando uma rede MLP**
  - Simulando o treinamento do XOR
  - Simulando o treinamento do XOR
  - Simulando o treinamento do XOR
  - Simulando o treinamento do XOR
  - Simulando o treinamento do XOR
  - Simulando o treinamento do XOR
  - Simulando o treinamento do XOR
  - Simulando o treinamento do XOR
  - Simulando o treinamento do XOR
  - Retropropagação
  - Retropropagação
  - Camada Oculta
  - Retropropagação
  - Retropropagação
  - Retropropagação
  - Função de Custo
  - Simulando o treinamento do XOR
  - Pesos Finais:
  - Implementando uma MLP
- **`sklearn.neural_network.MLPClassifier`**
  - Implementando uma MLP
- **Dinâmica**

<!-- EXEC_SUMMARY_END -->
<!-- DATALAB_CHUNK 1: pages 1-20 -->

{0}------------------------------------------------

A stylized, glowing blue neural network diagram on a black background. The network is shaped like a dome or a sphere, composed of numerous nodes (small circles) connected by a web of lines. The nodes and lines are a vibrant blue color, with some nodes appearing brighter than others, creating a sense of depth and activity. The overall effect is that of a complex, interconnected system, possibly representing a brain or a sophisticated AI model.

A stylized, glowing blue neural network diagram on a black background, resembling a dome or sphere made of interconnected nodes and lines.

# Rede neural MultiLayer Perceptron (MLP)

Silvia Moraes

{1}------------------------------------------------

**Redes Neurais Artificiais** são sistemas computacionais distribuídos compostos de unidades simples (neurônios), densamente interconectados.

An abstract visualization of a neural network architecture. On the left, three distinct input nodes are shown, each emitting a vibrant, multi-colored beam (cyan, magenta, and yellow). These beams converge and spread into a dense, complex web of interconnected nodes and lines, representing the hidden layers of the network. The nodes are small, glowing squares in various colors (blue, green, yellow, red), and the connections are thin, glowing lines. The overall effect is a dynamic, glowing representation of a deep learning model's internal structure.

Abstract visualization of a neural network architecture.

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

Tarefas Supervisionadas: **classificação e regressão**

Diagram of a single perceptron with two inputs, x1 and x2, connected to a single orange output node.

Perceptron

Diagram of a MultiLayer Perceptron (MLP) with two input nodes (x1, x2), two hidden layers (each with two green nodes), and one output node (orange). The entire structure is enclosed in a dashed red oval.

MultiLayer Perceptron

Diagram of a feedforward neural network architecture. It shows an input layer with 3 nodes (represented by dog icons), a hidden layer with 4 nodes, and an output layer with 2 nodes. All nodes in adjacent layers are fully connected. The layers are labeled INPUT, HIDDEN, and OUTPUT.

<https://sites.icmc.usp.br/andre/research/neural/>

Propagação: fluxo do sinal sempre para frente →

{4}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-9e6062272bbe3ddbb7c0606721d64cf0_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single perceptron with two inputs, x1 and x2, connected to a single orange output node.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-d62e2e2281009c16f4ee61660e716cd9_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a MultiLayer Perceptron (MLP) with two input nodes (x1, x2), two hidden layers (each with two green nodes), and one output node (orange).
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-12a6537c92844d5b393104c02e8dfc2f_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a feedforward neural network architecture.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-e6df2733626a85205c1db682e6259c46_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a fully connected MLP with input, hidden, and output layers.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-410562339ce067fdc6fa41940c118658_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a fully connected MLP
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-9b6b5924b48bf2fd5f347f88f06f45b3_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a fully connected MLP
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-95e259e8cb3519025066052af263f8c0_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a 3-layer MLP network with 30 input nodes, 18 hidden nodes, and 10 output nodes.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-34b047489058d6400b412cd0ae2334ba_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a 4-layer MLP network with 30 input nodes, 18 hidden nodes, 14 hidden nodes, and 10 output nodes.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-0c80c383f76034e117adf5e5eaadaaf3_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a neural network architecture
<!-- /IMAGE_DESCRIPTION -->
## Rede MultiLayer Perceptron

- São **redes perceptron de múltiplas camadas**, contendo uma ou mais camadas ocultas.
- Resolve **problemas não linearmente separáveis**.
- É considerada uma **Shallow Learning** (em oposição à **Deep Learning**) especialmente quando possuem apenas uma camada oculta.

Diagram of a MultiLayer Perceptron (MLP) neural network. It shows an input layer with three nodes, a hidden layer with four nodes, and an output layer with two nodes. The input nodes are connected to the hidden nodes, and the hidden nodes are connected to the output nodes. The input is represented by two images of a dog, one blue and one pink, indicating a classification task. The network is fully connected between adjacent layers.

<https://sites.icmc.usp.br/andre/research/neural/>

Diagram of a MultiLayer Perceptron (MLP) neural network. It shows an input layer with three nodes (yellow squares), two hidden layers with four nodes each (blue circles), and an output layer with two nodes (green circles). The input nodes are connected to the hidden nodes, and the hidden nodes are connected to the output nodes. The network is fully connected between adjacent layers. Labels indicate 'Camada de entrada (dados)', 'Camadas ocultas ou intermediárias (neurônios)', and 'Camada de Saída (neurônios)'.

{5}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-e394c2b5c61344f6a12397f430086072_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a MultiLayer Perceptron (MLP) neural network.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-53f1f7d17b3e7aae62169c41d2a88a77_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a MultiLayer Perceptron (MLP) neural network.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-6629e8a87e7552e2454b7c3e9f6d73a0_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a Multi-Layer Perceptron (MLP) for XOR.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-9f6dec4d4e9fde40bce018861ef1278e_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a Multi-Layer Perceptron (MLP) network for XOR.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-32ff77da4286b58c4778033acaa10836_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a MultiLayer Perceptron
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-3b281ef3b6cc5f8ba97cbc011bfaac79_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a Multi-Layer Perceptron (MLP) with two input nodes (x1, x2), two hidden nodes, and two output nodes (y1, y2).
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-2b00743506f6a3bbd17af764162dc76d_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a MultiLayer Perceptron (MLP) neural network for XOR.
<!-- /IMAGE_DESCRIPTION -->
## Arquitetura e Topologia

A photograph showing a silver metal ball bearing being measured with a vernier caliper. The bearing is placed on a white sheet of paper containing a technical drawing of a mechanical part, which includes concentric circles, dimension lines, and section markers labeled 'A'. A yellow and green pencil lies diagonally to the left of the bearing. The caliper's scale is visible, showing measurements in millimeters (bottom) and inches (top), with markings such as '0.05 mm' and '1/128 in.' visible on the slide. Additional annotations on the drawing include '10.5x' and '45°'.

A photograph of a mechanical ball bearing being measured with a vernier caliper, resting on a technical drawing, with a pencil nearby.

{6}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-afe5eb459b7c9cfe880b067777d876d8_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A photograph of a mechanical ball bearing being measured with a vernier caliper, resting on a technical drawing, with a pencil nearby.
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

The diagram illustrates a MultiLayer Perceptron (MLP) topology. It consists of the following layers and connections:

- Camada de entrada (Input Layer):** Nodes  $x_1$  and  $x_2$  (black circles).
- Camada Oculta ou Intermediária (Hidden Layer 1):** Nodes 1, 2, and 3 (blue circles). Each node has a bias weight  $w_{i0}$  (e.g.,  $w_{10}$ ,  $w_{20}$ ,  $w_{30}$ ) and is connected to all nodes in the next layer.
- Camada Oculta ou Intermediária (Hidden Layer 2):** Nodes 4 and 5 (blue circles). Each node has a bias weight  $w_{i0}$  (e.g.,  $w_{40}$ ,  $w_{50}$ ) and is connected to all nodes in the next layer.
- Camada de Saída (Output Layer):** Nodes 6 and 7 (blue circles). Each node has a bias weight  $w_{i0}$  (e.g.,  $w_{60}$ ,  $w_{70}$ ) and produces outputs  $y_6$  and  $y_7$ .

All connections between nodes are labeled with synaptic weights  $w_{ij}$  (e.g.,  $w_{11}$ ,  $w_{21}$ ,  $w_{31}$  for connections from  $x_1$  to nodes 1, 2, and 3 respectively). The label "pesos sinápticos" (synaptic weights) is placed above the first hidden layer.

**Exemplo MLP: 2 x 3 x 2 x 2**

Totalmente conectada

Diagram of a MultiLayer Perceptron (MLP) with 2 input nodes, two hidden layers of 3 and 2 nodes respectively, and 2 output nodes. All nodes are fully connected to each other. Weights are labeled w\_ij and biases are labeled w\_i0.

{8}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-990567efebf979be51f56d1150012c9d_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a MultiLayer Perceptron (MLP) with 2 input nodes, two hidden layers of 3 and 2 nodes respectively, and 2 output nodes.
<!-- /IMAGE_DESCRIPTION -->
### Como definir a topologia de uma rede MLP?

- A topologia mais simples possui 3 camadas:
  - Camada de entrada: corresponde à camada de dados
  - Camada oculta: de neurônios
  - Camada de saída: de neurônios

The diagram illustrates a Multi-Layer Perceptron (MLP) network topology. It consists of three layers of neurons: an input layer, a hidden layer, and an output layer. The input layer is represented by blue squares labeled  $x_1, x_2, x_3, \dots, x_n$ . The hidden layer is represented by yellow circles. The output layer is represented by green circles labeled  $y_1, y_2, y_3, y_4, \dots, y_k$ . All neurons in the input layer are connected to all neurons in the hidden layer, and all neurons in the hidden layer are connected to all neurons in the output layer, as indicated by the blue lines connecting them.

Diagram of a Multi-Layer Perceptron (MLP) network topology showing input, hidden, and output layers.

{9}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-562f471e8153729557e6a4ee6343c32c_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a Multi-Layer Perceptron (MLP) network topology showing input, hidden, and output layers.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-7f17c430b9598e4d748a8041457810b3_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a Multi-Layer Perceptron (MLP) showing input, hidden, and output layers.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-a26e142d3df5bef41a84a9dd099d7825_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a Multi-Layer Perceptron (MLP) showing input, hidden, and output layers.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-2b3a967f6ce4f23649be995a353e39f8_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a Multi-Layer Perceptron (MLP) showing input, hidden, and output layers.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-844077b3034f0030b404207db0ad76b4_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a Multi-Layer Perceptron (MLP) showing input, hidden, and output layers.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-6e15fc9ea763541c5913d26f85072ae1_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a Multi-Layer Perceptron (MLP) network topology.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-2837ffdadcdb1e5bababa56b564e56ed_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a Multi-Layer Perceptron (MLP) network topology.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-e151d3468319b81f042ca232c4d82e4b_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a Multi-Layer Perceptron (MLP) network topology.
<!-- /IMAGE_DESCRIPTION -->
### Como definir a topologia de uma rede MLP?

- A topologia mais simples possui 3 camadas:
  - Camada de entrada: corresponde à camada de dados
  - Camada oculta: de neurônios
  - Camada de saída: de neurônios

**Totalmente Conectada**  
Parcialmente Conectada

The diagram illustrates a fully connected Multi-Layer Perceptron (MLP) with three layers. The input layer on the left consists of blue squares labeled  $x_1, x_2, x_3, \dots, x_n$ . The hidden layer in the middle consists of yellow circles. The output layer on the right consists of green circles labeled  $y_1, y_2, y_3, y_4, \dots, y_k$ . Every square in the input layer is connected to every circle in the hidden layer by a blue line. Similarly, every circle in the hidden layer is connected to every circle in the output layer by a blue line. Each output circle has a blue arrow pointing to its corresponding label  $y_i$ .

Diagram of a fully connected MLP with input, hidden, and output layers.

{10}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-06c9dba199685f028e690b771f51841d_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Blue arrow pointing right, indicating the transition from the 3-layer to the 4-layer network diagram.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-ca3c2d7203150c574a40cde4ac913a94_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Yellow arrow pointing left
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

O diagrama ilustra uma rede MLP totalmente conectada. À esquerda, há  $n$  blocos azuis representando os dados de entrada, rotulados como  $x_1, x_2, x_3, \dots, x_n$ . Cada um desses blocos está conectado a todos os  $p$  neurônios ocultos, representados por círculos amarelos. Abaixo dos neurônios ocultos, há  $k$  círculos verdes representando os neurônios de saída, rotulados como  $y_1, y_2, y_3, y_4, \dots, y_k$ . Cada neurônio oculto está conectado a todos os  $k$  neurônios de saída. Setas azuis apontam para cada saída  $y_i$ . Abaixo do diagrama, a notação  $n \times p \times k$  indica as dimensões das camadas:  $n$  entradas,  $p$  neurônios ocultos e  $k$  saídas.

Diagrama de uma rede MLP totalmente conectada com n entradas, p neurônios ocultos e k saídas.

{11}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-7e670a2b556b53ea9002dfff3a420e08_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de uma rede MLP totalmente conectada com n entradas, p neurônios ocultos e k saídas.
<!-- /IMAGE_DESCRIPTION -->
### Como definir a topologia de uma rede MLP?

- A topologia mais simples possui 3 camadas:
  - Camada de entrada: corresponde à camada de dados
  - Camada oculta: de neurônios
  - Camada de saída: de neurônios

Red starburst icon with the word 'Pruning' inside.

Totalmente Conectada  
**Parcialmente Conectada**

Eliminação de conexões

Diagram of a Multi-Layer Perceptron (MLP) showing input, hidden, and output layers. The input layer has nodes x1, x2, x3, ..., xn. The hidden layer has yellow nodes. The output layer has green nodes labeled y1, y2, y3, y4, ..., yk. Most connections are blue, but the bottom-most connection from xn to the bottom-most hidden node and its corresponding output node are highlighted in red, illustrating pruning.

{12}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-e3b8510f6a2194e250205ab7bc38076d_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Red starburst icon with the word 'Pruning' inside.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-bb6d33498937738ff5dac8d91c9ebaad_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Pruning icon
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-d25a962fde4b3171879749757440c3c5_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Pruning icon
<!-- /IMAGE_DESCRIPTION -->
#### Como definir a topologia de uma rede MLP?

- A topologia mais simples possui 3 camadas:
  - Camada de entrada: corresponde à camada de dados
  - Camada oculta: de neurônios
  - Camada de saída: de neurônios

A red starburst shape with the word "Pruning" written in white inside it.

Pruning icon

Totalmente Conectada  
**Parcialmente Conectada**

Eliminação de conexões

A diagram of a fully connected Multi-Layer Perceptron (MLP). It consists of an input layer with

 $n$ 

nodes labeled

 $x_1, x_2, x_3, \dots, x_n$ 

(represented by blue squares), a hidden layer with 4 nodes (represented by yellow circles), and an output layer with

 $k$ 

nodes labeled

 $y_1, y_2, y_3, y_4, \dots, y_k$ 

(represented by green circles). Every node in the input layer is connected to every node in the hidden layer, and every node in the hidden layer is connected to every node in the output layer. Arrows point from the output nodes to their respective labels

 $y_i$ 

.

Diagram of a fully connected MLP

{13}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-7832324609ad3cc688064e0341612b32_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Pruning icon: a red starburst shape with the word 'Pruning' inside.
<!-- /IMAGE_DESCRIPTION -->
#### Como definir a topologia de uma rede MLP?

- A topologia mais simples possui 3 camadas:
  - Camada de entrada: corresponde à camada de dados
  - Camada oculta: de neurônios
  - Camada de saída: de neurônios

Pruning icon: a red starburst shape with the word 'Pruning' inside.

Totalmente Conectada  
**Parcialmente Conectada**

Eliminação de conexões  
Eliminação de neurônios

Diagram of a Multi-Layer Perceptron (MLP) showing input, hidden, and output layers. The input layer has nodes x1, x2, x3, ..., xn. The first hidden layer has four yellow nodes. The second hidden layer has four green nodes. The output layer has nodes y1, y2, y3, y4, ..., yk. Connections are shown as blue lines between adjacent layers. A single red node is located at the bottom of the hidden layers, with red lines connecting it to all output nodes y1 through yk. This red node is also connected to the input nodes x1, x2, x3, and xn via red lines. The text 'Parcialmente Conectada' and 'Eliminação de conexões' is overlaid on this diagram, indicating that some connections (the red ones) are being added or considered for pruning.

{14}------------------------------------------------
#### Como definir a topologia de uma rede MLP?

- A topologia mais simples possui 3 camadas:  
  - Camada de entrada: corresponde `a camada de dados
  - Camada oculta: de neurônios
  - Camada de saída: de neurônios

Pruning

Pruning icon

Totalmente Conectada  
**Parcialmente Conectada**

Eliminação de conexões  
Eliminação de neurônios

A diagram of a Multi-Layer Perceptron (MLP) network. It features three layers: an input layer on the left with blue square nodes labeled  $x_1$ ,  $x_2$ ,  $x_3$ , and  $x_n$  (separated by a vertical ellipsis); a hidden layer in the middle with four yellow circular nodes; and an output layer on the right with green circular nodes labeled  $y_1$ ,  $y_2$ ,  $y_3$ ,  $y_4$ , and  $y_k$  (with a vertical ellipsis between  $y_4$  and  $y_k$ ). The network is fully connected, with lines representing connections between every node in one layer and every node in the next. Arrows point from the output nodes to their labels.

Diagram of a fully connected MLP

{15}------------------------------------------------
#### Como definir a topologia de uma rede MLP?

- A topologia mais simples possui 3 camadas:
  - **Camada de entrada:** corresponde à camada de dados
  - Camada oculta: de neurônios
  - Camada de saída: de neurônios

$n$ : quantidade de dados de entrada, número de features/atributos de entrada

The diagram illustrates a Multi-Layer Perceptron (MLP) neural network. It consists of three layers of neurons: an input layer with  $n$  neurons (represented by blue squares), a hidden layer with  $p$  neurons (represented by yellow circles), and an output layer with  $k$  neurons (represented by green circles). The input neurons are labeled  $x_1, x_2, x_3, \dots, x_n$ . The output neurons are labeled  $y_1, y_2, y_3, y_4, \dots, y_k$ . All neurons in adjacent layers are fully connected by blue lines. The labels  $n, x, p, x, k$  are placed below the respective columns of neurons. A red box highlights the input layer and its label  $n$ . A light orange box above the diagram contains the text: " $n$ : quantidade de dados de entrada, número de features/atributos de entrada".

Diagram of an MLP neural network topology showing input, hidden, and output layers.

{16}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-0f985b39edc1d52ba3600c438bc8f0a5_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of an MLP neural network topology showing input, hidden, and output layers.
<!-- /IMAGE_DESCRIPTION -->
##### Planta Iris

4 atributos de entrada

Diagram of an Iris flower showing its parts: Corola (conjunto de pétalas), Pétalas, Sépalas, and Cálice (conjunto de sépalas).

Diagram of an Iris flower showing its parts: Corola (conjunto de pétalas), Pétalas, Sépalas, and Cálice (conjunto de sépalas).

Scatter plot showing the distribution of Iris species (Iris-setosa, Iris-versicolor, Iris-virginica) based on four attributes. A linear decision boundary separates Iris-setosa from the other two species.

Scatter plot of Iris species (Iris-setosa, Iris-versicolor, Iris-virginica) based on four attributes. A linear decision boundary separates Iris-setosa from the other two species.

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
> **[Descrição de imagem]** Diagram of an Iris flower showing its parts: Corola (conjunto de pétalas), Pétalas, Sépalas, and Cálice (conjunto de sépalas).
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-fed39b841ae2dce01088b84bfc1e2789_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Scatter plot of Iris species (Iris-setosa, Iris-versicolor, Iris-virginica) based on four attributes.
<!-- /IMAGE_DESCRIPTION -->
#### Como definir a topologia de uma rede MLP?

- A topologia mais simples possui 3 camadas:
  - **Camada de entrada:** corresponde `a camada de dados
  - Camada oculta: de neurônios
  - Camada de saída: de neurônios

Diagram illustrating a specific MLP structure. The input layer has 4 nodes, labeled  $x_1$  to  $x_4$ , corresponding to features: Comprimento da sépala, Largura da sépala, Comprimento da pétala, and Largura da pétala. The network has a hidden layer with  $p$  nodes and an output layer with  $k$  nodes, producing outputs  $y_1, y_2, y_3, y_4, \dots, y_k$ . The topology is summarized as **4** x p x k. All nodes in adjacent layers are fully connected.

Diagram of a specific MLP with 4 input nodes, p hidden nodes, and k output nodes.

$n$ : quantidade de dados de entrada, número de features/atributos de entrada

Diagram illustrating a general MLP structure. The input layer has  $n$  nodes, labeled  $x_1, x_2, x_3, \dots, x_n$ . The network has a hidden layer with  $p$  nodes and an output layer with  $k$  nodes, producing outputs  $y_1, y_2, y_3, y_4, \dots, y_k$ . The input layer size is indicated by a red 'n' below the nodes. The topology is summarized as n x p x k. All nodes in adjacent layers are fully connected.

General diagram of an MLP with n input nodes, p hidden nodes, and k output nodes.

{18}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-dfe556fea00682b09a59427aaf72051c_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a specific MLP with 4 input nodes, p hidden nodes, and k output nodes.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-4356776ca004ecba5d599667a155d7d4_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** General diagram of an MLP with n input nodes, p hidden nodes, and k output nodes.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-79e1709a7317ead45379cbb8ff3ba802_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** General diagram of an MLP topology with n input nodes, p hidden nodes, and k output nodes.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-933ecd14c858bf3fc919222d8e357bc8_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** General diagram of an MLP topology.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-5478f70a6cef3e5672b2b22d28830cfb_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** General diagram of an MLP topology.
<!-- /IMAGE_DESCRIPTION -->
#### Como definir a topologia de uma rede MLP?

- A topologia mais simples possui 3 camadas:
  - Camada de entrada: corresponde à camada de dados
  - Camada oculta: de neurônios
  - **Camada de saída**: de neurônios

The diagram illustrates a Multi-Layer Perceptron (MLP) architecture. It consists of three layers of neurons: an input layer with  $n$  nodes (represented by blue squares), a hidden layer with  $p$  nodes (represented by yellow circles), and an output layer with  $k$  nodes (represented by green circles). The input nodes are labeled  $x_1, x_2, x_3, \dots, x_n$ . The hidden nodes are unlabeled. The output nodes are labeled  $y_1, y_2, y_3, y_4, \dots, y_k$ . All nodes in adjacent layers are fully connected by blue lines. The output layer is highlighted with a red rectangular box. Above the output layer, a label indicates  $k$ : quantidade de classes. Below the diagram, the dimensions are labeled as  $n \times p \times k$ .

Diagram of a Multi-Layer Perceptron (MLP) showing input, hidden, and output layers.

{19}------------------------------------------------
##### Planta Iris

4 atributos de entrada

3 classes: iris-setosa, iris-versicolor e iris-virginica

Diagrama de uma flor de íris com rótulos das partes: Corola (conjunto de pétalas), Pétalas, Sépalas, and Cálice (conjunto de sépalas).

Diagrama de uma flor de íris com rótulos das partes: Corola (conjunto de pétalas), Pétalas, Sépalas, and Cálice (conjunto de sépalas).

Gráfico de dispersão dos atributos de entrada das espécies de íris: Iris-setosa (azul), Iris-versicolor (laranja) e Iris-virginica (verde). O gráfico mostra a separação clara das espécies com base nos atributos de entrada.

Gráfico de dispersão dos atributos de entrada das espécies de íris: Iris-setosa (azul), Iris-versicolor (laranja) e Iris-virginica (verde).

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

<!-- IMAGE_DESCRIPTION: datalab-63c666b05041841b01fdef9fa4153ff7_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de uma flor de íris com rótulos das partes: Corola (conjunto de pétalas), Pétalas, Sépalas, and Cálice (conjunto de sépalas).
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-f85bf99d372e735d228361bf4d3cf7e6_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Gráfico de dispersão dos atributos de entrada das espécies de íris: Iris-setosa (azul), Iris-versicolor (laranja) e Iris-virginica (verde).
<!-- /IMAGE_DESCRIPTION -->
## Como definir a topologia de uma rede MLP?

- A topologia mais simples possui 3 camadas:
  - Camada de entrada: corresponde `a camada de dados
  - Camada oculta: de neurônios
  - **Camada de saída:** de neurônios

$4 \times p \times 3$   
 Comprimento da sépala  $x_1$    
 Largura da sépala  $x_2$    
 Comprimento da pétala  $x_3$    
 Largura da pétala  $x_4$

Output nodes:  
 $y_1$  setosa  
 $y_2$  versicolor  
 $y_3$  virginica

Diagram of an MLP for Iris classification with 4 input nodes, p hidden nodes, and 3 output nodes.

k: quantidade de classes

Input nodes:  $x_1, x_2, x_3, \dots, x_n$   
 Output nodes:  $y_1, y_2, y_3, y_4, \dots, y_k$

$n \times p \times k$

General diagram of an MLP topology with n input nodes, p hidden nodes, and k output nodes.

{21}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-c5655e700cc3e9aac7e9f4f07f30264d_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of an MLP for Iris classification with 4 input nodes, p hidden nodes, and 3 output nodes.
<!-- /IMAGE_DESCRIPTION -->
## Como definir a topologia de uma rede MLP?

- A topologia mais simples possui 3 camadas:
  - Camada de entrada: corresponde à camada de dados
  - **Camada oculta:** de neurônios
  - Camada de saída: de neurônios

Diagrama de uma rede MLP (Multi-Layer Perceptron) com 3 camadas:

- Camada de entrada:** Representada por  $n$  blocos azuis, rotulados  $x_1, x_2, x_3, \dots, x_n$ . Abaixo dos blocos, o número  $n$  indica a quantidade de neurônios.
- Camada oculta:** Representada por  $p$  blocos amarelos. Abaixo dos blocos, o número  $p$  indica a quantidade de neurônios.
- Camada de saída:** Representada por  $k$  blocos verdes, rotulados  $y_1, y_2, y_3, y_4, \dots, y_k$ . Abaixo dos blocos, o número  $k$  indica a quantidade de neurônios. Esta camada é destacada por um retângulo vermelho.

As camadas são conectadas entre si por linhas azuis, formando uma rede totalmente conectada. O número  $x$  aparece entre as camadas, indicando a conexão entre elas.

Diagrama de uma rede MLP com 3 camadas: entrada, oculta e saída.

{22}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-d53cd0fd1cf896a9353fd63de1505ba2_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de uma rede MLP com 3 camadas: entrada, oculta e saída.
<!-- /IMAGE_DESCRIPTION -->
## Como definir a topologia de uma rede MLP?

- A topologia mais simples possui 3 camadas:

Quantos neurônios usamos na camada oculta?

- Camada de entrada: corresponde `a camada de dados
- **Camada oculta:** de neurônios
- Camada de saída: de neurônios

The diagram illustrates a Multi-Layer Perceptron (MLP) architecture. It consists of three layers: an input layer, a hidden layer, and an output layer. The input layer has  $n$  inputs, represented by blue squares labeled  $x_1, x_2, x_3, ext{...}, x_n$ . The hidden layer has  $p$  neurons, represented by yellow circles. The output layer has  $k$  neurons, represented by green circles labeled  $y_1, y_2, y_3, y_4, ext{...}, y_k$ . The output layer is highlighted with a red rectangular box. All inputs are connected to all neurons in the hidden layer, and all neurons in the hidden layer are connected to all neurons in the output layer. Below the diagram, the dimensions are indicated as  $n imes p imes k$ .

Diagram of a Multi-Layer Perceptron (MLP) showing input, hidden, and output layers.

{23}------------------------------------------------
## Como definir a topologia de uma rede MLP?

- A topologia mais simples possui 3 camadas:

Quantos neurônios usamos na camada oculta?

- Camada de entrada: corresponde `a camada de dados
- **Camada oculta:** de neurônios
- Camada de saída: de neurônios

Diagram illustrating a specific MLP architecture for the Iris dataset. The input layer has 4 nodes ( $X_1$  to  $X_4$ ), representing features: *Comprimento da sépala*, *Largura da sépala*, *Comprimento da pétala*, and *Largura da pétala*. The hidden layer has  $p$  nodes, indicated by a large red question mark. The output layer has 3 nodes ( $y_1$  to  $y_3$ ), representing classes: *setosa*, *versicolor*, and *virginica*. The layers are labeled 4 x  $p$  x 3.

Diagram of a specific MLP for Iris classification with 4 inputs, p hidden neurons, and 3 outputs.

p: ?

Diagram illustrating a general MLP architecture. The input layer has  $n$  nodes ( $X_1, X_2, X_3, ..., X_n$ ). The hidden layer has  $p$  nodes. The output layer has  $k$  nodes ( $y_1, y_2, y_3, y_4, ..., y_k$ ), which is highlighted by a red box. The layers are labeled  $n$  x  $p$  x  $k$ .

General diagram of an MLP architecture with n inputs, p hidden neurons, and k outputs.

{24}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-4b87467ad9642943235f48f7d4b59449_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a specific MLP for Iris classification with 4 inputs, p hidden neurons, and 3 outputs.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-7e1c9b51e067a48cd0fcc9748d8bd8d8_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** General diagram of an MLP architecture with n inputs, p hidden neurons, and k outputs.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-9f9386d5b3d6cbeb1ed104a799320ebf_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a specific MLP for Iris dataset classification.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-3e2a8dc8c5537dbe703cdcb0e21e4e1b_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a specific MLP for Iris classification.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-b51423b6c049f5b5fcde42e50b58f18b_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of an MLP for the Iris dataset with 4 inputs, 4 hidden neurons, and 3 outputs.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-a4b963a07cc368283154762c4b156fe7_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** General MLP diagram with n inputs, p hidden neurons, and k outputs.
<!-- /IMAGE_DESCRIPTION -->
## Como definir a topologia de uma rede MLP?
## Quantos neurônios usamos na camada oculta?

- De forma objetiva **ainda não há como definir**.
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
- **Muitos neurônios** na camada oculta pode gerar **Overfitting**. Aumenta o tempo de processamento.

|                | Under-fitting | Optimal-fitting | Over-fitting |
|----------------|---------------|-----------------|--------------|
| Regression     |               |                 |              |
| Classification |               |                 |              |

Regression Under-fitting: A straight line attempting to fit a U-shaped distribution of blue dots, failing to capture the curve. Regression Optimal-fitting: A smooth parabolic curve that follows the general trend of the U-shaped blue dots. Regression Over-fitting: A highly erratic, jagged line that passes through every single blue dot, capturing noise rather than the trend. Classification Under-fitting: A simple straight line separating blue and red dots, misclassifying several points on both sides. Classification Optimal-fitting: A smooth curved boundary that effectively separates the cluster of red dots from the surrounding blue dots. Classification Over-fitting: A complex, convoluted boundary that twists to isolate every single red dot, including outliers, from the blue dots.

<https://towardsdatascience.com/techniques-for-handling-underfitting-and-overfitting-in-machine-learning-348daa2380b9>

{29}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-20727e57890be6da5692a02d13c0a8ec_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Regression Under-fitting: A straight line attempting to fit a U-shaped distribution of blue dots, failing to capture the curve.
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

- Camada de entrada: corresponde `a camada de dados
- **Camada oculta:** de neurônios
- Camada de saída: de neurônios

Diagram illustrating a specific MLP topology for the Iris dataset. The input layer has 4 nodes ( $x_1, x_2, x_3, x_4$ ) corresponding to features: Comprimento da sépala, Largura da sépala, Comprimento da pétala, and Largura da pétala. The hidden layer has  $p$  nodes. The output layer has 3 nodes ( $y_1, y_2, y_3$ ) corresponding to classes: setosa, versicolor, and virginica. The number of hidden nodes is calculated as:  
$$p = \sqrt{n \times k} = \sqrt{4 \times 3} = \sqrt{12} = 3,46$$

Diagram of a specific MLP for Iris dataset classification.

Diagram illustrating a general MLP topology. The input layer has  $n$  nodes ( $x_1, x_2, x_3, \dots, x_n$ ). The hidden layer has  $p$  nodes, indicated by a large red question mark. The output layer has  $k$  nodes ( $y_1, y_2, y_3, y_4, \dots, y_k$ ), which are highlighted by a red box. The number of hidden nodes is indicated by a label  $p: ?$ .

General diagram of an MLP topology.

{32}------------------------------------------------
## Como definir a topologia de uma rede MLP?

- A topologia mais simples possui 3 camadas:

Quantos neurônios usamos na camada oculta?

- Camada de entrada: corresponde à camada de dados
- **Camada oculta:** de neurônios
- Camada de saída: de neurônios

Diagram illustrating a specific MLP topology for the Iris dataset. The input layer has 4 nodes ( $x_1, x_2, x_3, x_4$ ) representing features: Comprimento da sépala, Largura da sépala, Comprimento da pétala, and Largura da pétala. The hidden layer has  $p$  nodes. The output layer has 3 nodes ( $y_1, y_2, y_3$ ) representing classes: setosa, versicolor, and virginica. The text  $p = 3 \text{ ou } 4$  is shown in red.

Diagram of a specific MLP for Iris classification.

Diagram illustrating a general MLP topology. The input layer has  $n$  nodes ( $x_1, x_2, x_3, \dots, x_n$ ). The hidden layer has  $p$  nodes, indicated by a large red question mark and a box labeled  $p: ?$ . The output layer has  $k$  nodes ( $y_1, y_2, y_3, y_4, \dots, y_k$ ), which are highlighted by a red box. The text  $n \times p \times k$  is shown at the bottom.

General diagram of an MLP topology.

{33}------------------------------------------------
## Como definir a topologia de uma rede MLP?

- A topologia mais simples possui 3 camadas:

Quantos neurônios usamos na camada oculta?

- Camada de entrada: corresponde `a camada de dados
- **Camada oculta:** de neurônios
- Camada de saída: de neurônios

4 x 4 x 3  
*Comprimento da sépala*  $X_1$   
*Largura da sépala*  $X_2$   
*Comprimento da pétala*  $X_3$   
*Largura da pétala*  $X_4$   
 $p = 4$  (arredondamos)  
 $y_1$  *setosa*  
 $y_2$  *versicolor*  
 $y_3$  *virginica*

Diagram of an MLP for the Iris dataset with 4 inputs, 4 hidden neurons, and 3 outputs.

$p: ?$

$X_1$   
 $X_2$   
 $X_3$   
 ...  
 $X_n$

?

$y_1$   
 $y_2$   
 $y_3$   
 $y_4$   
 ...  
 $y_k$

$n$  x  $p$  x  $k$

General MLP diagram with n inputs, p hidden neurons, and k outputs.

{34}------------------------------------------------
## Como definir a topologia de uma rede MLP?

Mais um exemplo: Tabela XOR

| $x_1$ | $x_2$ | $d$ |
|-------|-------|-----|
| 0     | 0     | 0   |
| 0     | 1     | 1   |
| 1     | 0     | 1   |
| 1     | 1     | 0   |

The diagram illustrates a feedforward neural network architecture. It consists of three layers of nodes: an input layer with  $n$  nodes (represented by blue squares), a hidden layer with  $p$  nodes (represented by yellow circles), and an output layer with  $k$  nodes (represented by green circles). The input nodes are labeled  $x_1, x_2, x_3, \dots, x_n$ . The output nodes are labeled  $y_1, y_2, y_3, y_4, \dots, y_k$ . Every node in one layer is connected to every node in the subsequent layer by a blue line, indicating a fully connected topology. Below the diagram, the labels  $n$ ,  $x$ ,  $p$ ,  $x$ , and  $k$  are placed, likely representing the number of nodes in each layer and the type of connection between them.

Diagram of a Multi-Layer Perceptron (MLP) network topology.

{35}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-8ba270d9a35a905e16a9b78e6b3ad2b8_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a neural network with two input nodes (x1, x2), three hidden nodes, and one output node.
<!-- /IMAGE_DESCRIPTION -->
## Como definir a topologia de uma rede MLP?

Mais um exemplo: Tabela XOR

| $x_1$ | $x_2$ | $d$ |
|-------|-------|-----|
| 0     | 0     | 0   |
| 0     | 1     | 1   |
| 1     | 0     | 1   |
| 1     | 1     | 0   |

Diagram illustrating the topology of a Multi-Layer Perceptron (MLP) network. The input layer consists of 2 nodes ( $x_1$ ,  $x_2$ ). The hidden layer consists of  $p$  nodes. The output layer consists of  $k$  nodes ( $y_1, y_2, y_3, y_4, \dots, y_k$ ). All nodes in adjacent layers are fully connected. The text "2 x p x k" is displayed below the diagram, indicating the dimensions of the layers.

Diagram of a Multi-Layer Perceptron (MLP) network topology. It shows an input layer with 2 nodes (x1, x2), a hidden layer with p nodes, and an output layer with k nodes (y1, y2, y3, y4, ..., yk). All nodes in adjacent layers are fully connected. The input nodes are blue squares, hidden nodes are yellow circles, and output nodes are green circles. Below the diagram, the text '2 x p x k' is displayed, with the '2' in red and the others in black.

{36}------------------------------------------------
## Como definir a topologia de uma rede MLP?

Mais um exemplo: Tabela XOR

| $x_1$ | $x_2$ | $d$ |
|-------|-------|-----|
| 0     | 0     | 0   |
| 0     | 1     | 1   |
| 1     | 0     | 1   |
| 1     | 1     | 0   |

The diagram illustrates a neural network topology for the XOR problem. It consists of three layers of nodes: an input layer with 2 blue square nodes labeled  $x_1$  and  $x_2$ ; a hidden layer with  $p$  yellow circular nodes (indicated by a vertical ellipsis between the third and fourth nodes); and an output layer with 2 green circular nodes labeled  $y_1$  and  $y_2$ . All nodes in adjacent layers are fully connected by blue lines. Below the diagram, the text "2 x p x 2" is displayed, where the first "2" and the "x" are blue, the "p" is black, and the second "x" and the final "2" are red.

Diagram of a Multi-Layer Perceptron (MLP) neural network topology for the XOR problem.

{37}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-78ff716475b2f65bf01c3a4d02d89fc4_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a Multi-Layer Perceptron (MLP) neural network topology for the XOR problem.
<!-- /IMAGE_DESCRIPTION -->
## Como definir a topologia de uma rede MLP?

Mais um exemplo: Tabela XOR

| x1 | x2 | d |
|----|----|---|
| 0  | 0  | 0 |
| 0  | 1  | 1 |
| 1  | 0  | 1 |
| 1  | 1  | 0 |

Diagram of a Multi-Layer Perceptron (MLP) for XOR. It shows two input nodes ( $x_1$ ,  $x_2$ ) connected to a hidden layer of  $p$  nodes (indicated by a red question mark). The hidden layer is connected to two output nodes ( $y_1$ ,  $y_2$ ). The diagram is labeled with '2' for inputs, 'p' for hidden nodes, and '2' for outputs.

Diagram of a Multi-Layer Perceptron (MLP) for XOR. It shows two input nodes (x1, x2) connected to a hidden layer of p nodes (indicated by a red question mark). The hidden layer is connected to two output nodes (y1, y2). The diagram is labeled with '2' for inputs, 'p' for hidden nodes, and '2' for outputs.

$$\begin{aligned} p &= \sqrt{n \times k} \\ &= \sqrt{2 \times 2} \\ &= \sqrt{4} = 2 \end{aligned}$$

{38}------------------------------------------------
## Como definir a topologia de uma rede MLP?

Mais um exemplo: Tabela XOR

| x1 | x2 | d |
|----|----|---|
| 0  | 0  | 0 |
| 0  | 1  | 1 |
| 1  | 0  | 1 |
| 1  | 1  | 0 |

Diagram of a Multi-Layer Perceptron (MLP) network for XOR. It has two input nodes (x1, x2) represented by blue squares, two hidden layers each with two yellow circular nodes, and two output nodes (y1, y2) represented by green circles. All nodes in adjacent layers are fully connected by blue lines.

2 x 2 x 2

$$\begin{aligned} p &= \sqrt{n \times k} \\ &= \sqrt{2 \times 2} \\ &= \sqrt{4} = 2 \end{aligned}$$

{39}------------------------------------------------
## Como definir a topologia de uma rede MLP?

- E o que fazer quando são necessárias mais camadas?
  - Você pode tentar usar a mesma regra.

Diagram illustrating a Multi-Layer Perceptron (MLP) network topology. The input layer consists of 30 nodes ( $x_1, x_2, x_3, \dots, x_{30}$ ). The hidden layer consists of 18 nodes. The output layer consists of 10 nodes ( $y_1, y_2, y_3, y_4, \dots, y_{10}$ ). All nodes in adjacent layers are fully connected. Below the diagram, the numbers 30, 18, and 10 are shown with 'x' between them, representing the number of nodes in each layer.

Diagram of a Multi-Layer Perceptron (MLP) network topology. It shows an input layer with 30 nodes (x1 to x30), a hidden layer with 18 nodes, and an output layer with 10 nodes (y1 to y10). All nodes in adjacent layers are fully connected. Below the diagram, the numbers 30, 18, and 10 are shown with 'x' between them, representing the number of nodes in each layer.

$$p = \sqrt{n \times k} = \sqrt{30 \times 10} = \sqrt{300} = 17,32$$

<!-- DATALAB_CHUNK 3: pages 41-60 -->

{40}------------------------------------------------

# Como definir a topologia de uma rede MLP?

- E o que fazer quando são necessárias mais camadas?
  - Você pode tentar usar a mesma regra.

Diagram of a 3-layer MLP network. The input layer has 30 nodes ( $x_1, x_2, x_3, \dots, x_{30}$ ). The hidden layer has 18 nodes. The output layer has 10 nodes ( $y_1, y_2, y_3, y_4, \dots, y_{10}$ ). All nodes in adjacent layers are fully connected. Below the diagram, the text "30 x 18 x 10" is displayed.

Diagram of a 3-layer MLP network with 30 input nodes, 18 hidden nodes, and 10 output nodes.

$$p = \sqrt{n \times k} = \sqrt{30 \times 10} = \sqrt{300} = 17,32$$

Blue arrow pointing right, indicating the transition from the 3-layer to the 4-layer network diagram.

Diagram of a 4-layer MLP network. The input layer has 30 nodes ( $x_1, x_2, x_3, \dots, x_{30}$ ). The first hidden layer has 18 nodes. The second hidden layer has 14 nodes. The output layer has 10 nodes ( $y_1, y_2, y_3, y_4, \dots, y_{10}$ ). All nodes in adjacent layers are fully connected. Below the diagram, the text "30 x 18 x 14 x 10" is displayed, with the number 14 in red.

Diagram of a 4-layer MLP network with 30 input nodes, 18 hidden nodes, 14 hidden nodes, and 10 output nodes.

$$p = \sqrt{n \times k} = \sqrt{18 \times 10} = \sqrt{180} = 13,41$$

{41}------------------------------------------------
## Como definir a topologia de uma rede MLP?

- Lembre-se:  
Independentemente da heurística usada para definir a topologia inicial, **você terá que realizar testes para encontrar a melhor topologia para a rede MLP.**

A stylized graphic of a human head profile, filled with a glowing blue neural network mesh, set against a black background. The mesh consists of numerous nodes connected by lines, forming a complex web that follows the contours of the head. The overall effect is one of digital intelligence or artificial neural networks.

A stylized graphic of a human head profile, filled with a glowing blue neural network mesh, set against a black background.

{42}------------------------------------------------

A grayscale image of a neural network diagram. It features several nodes, represented as shiny spheres, connected by lines. The nodes are arranged in a grid-like pattern, with some in sharp focus and others blurred in the background, creating a sense of depth. The overall aesthetic is clean and modern, typical of technical illustrations.

<!-- IMAGE_DESCRIPTION: datalab-2dfa6ac3edfe874f68aa0cbccaa42322_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A stylized, glowing blue neural network diagram on a black background, resembling a dome or sphere made of interconnected nodes and lines.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-4ab0be532558484d774d4efef9c94a56_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A stylized graphic of a human head profile, filled with a glowing blue neural network mesh, set against a black background.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-0d21e56f563c92ea5d8ec3218a00c618_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A grayscale image of a neural network diagram.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-c1448793af3cfb2ec356639a4d0bcaf7_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A grayscale image of a neural network diagram.
<!-- /IMAGE_DESCRIPTION -->
## Revisitando a rede Perceptron

{43}------------------------------------------------
### Redes Feed Forward

Tarefas Supervisionadas: **classificação e regressão**

A diagram of a single perceptron. It consists of two input nodes, labeled  $x_1$  and  $x_2$ , connected to a single orange output node. The entire structure is enclosed in a dashed red oval.

Perceptron

Diagram of a single Perceptron

A diagram of a MultiLayer Perceptron (MLP). It features two input nodes,  $x_1$  and  $x_2$ , connected to two green hidden nodes. These hidden nodes are then connected to a single orange output node.

Diagram of a MultiLayer Perceptron

MultiLayer Perceptron

A diagram illustrating a neural network architecture. On the left, two input images (a dog and a cat) are shown. These are connected to an 'INPUT' layer with three purple nodes. This layer is connected to a 'HIDDEN' layer with four purple nodes. The hidden layer is then connected to an 'OUTPUT' layer with two purple nodes. Arrows indicate the forward flow of information from left to right.

Diagram of a neural network architecture

<https://sites.icmc.usp.br/andre/research/neural/>

Propagação: fluxo do sinal sempre para frente →

{44}------------------------------------------------
### Rede Perceptron

- Limitação: só consegue resolver problemas linearmente separáveis.
- O algoritmo de aprendizado desse tipo de rede, procura os coeficientes que traçam a reta que separa linearmente os dados de uma classe de outra.

O gráfico mostra um plano bidimensional com dois conjuntos de pontos: um grupo de pontos azuis na parte superior e um grupo de pontos vermelhos na parte inferior. Uma linha preta sólida com inclinação negativa atravessa o plano, servindo como um limite de decisão que separa perfeitamente os pontos azuis dos vermelhos. O rótulo '#0' está centralizado acima da área do gráfico.

Gráfico de dispersão com dois grupos de pontos (azuis e vermelhos) e uma linha preta diagonal que os separa linearmente. O rótulo #0 está acima do gráfico.

{45}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-68ec8ddd77b91c6e59d90ca84ad64f11_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Gráfico de dispersão com dois grupos de pontos (azuis e vermelhos) e uma linha preta diagonal que os separa linearmente.
<!-- /IMAGE_DESCRIPTION -->
### Rede Perceptron

Revisitando um neurônio artificial j:

The diagram illustrates a single artificial neuron, labeled  $j$ . On the left, there is a vertical stack of input nodes. The top node is  $x_0 = 1$ , which is connected to a green circle representing the bias weight  $w_{0j}$ . Below it are nodes  $x_1, x_2, x_3, \dots, x_n$ , each connected to a white circle representing a weight  $w_{1j}, w_{2j}, w_{3j}, \dots, w_{nj}$ . These weights are collectively labeled "Pesos". All weighted inputs are connected to a central summation node, represented by a circle with the symbol  $\Sigma$ . The output of the summation node is  $v_j$ , which is then passed to a square box labeled  $f$ , representing the "Função de Ativação" (Activation Function). The final output of the neuron is  $y_j$ , labeled as "Saida" (Output).

Diagram of an artificial neuron j. Inputs x0=1 (bias), x1, x2, x3, ..., xn are connected to a summation node $\Sigma$ via weights w0j, w1j, w2j, w3j, ..., wnj. The weighted sum vj is passed to an activation function f to produce the output yj.

*Peso extra conhecido como bias*

$$v_j = w_{0j} + \sum_{i=1}^n (x_i \times w_{ij})$$

$$y_j = f(v_j)$$

**X:  $x_1, x_2, x_3, \dots, x_p$**   
O vetor X representa a entrada do neurônio. Pode ser os dados de entrada da rede ou o sinal de saída de outros neurônios.

{46}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-f5a5f52bc25d95a7f616290c99e88ae6_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a single Perceptron
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-e22af684d8e56d4c61e61bb5ddac1087_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of an artificial neuron j. Inputs x0=1 (bias), x1, x2, x3, ..., xn are connected to a summation node Σ via weights w0j, w1j, w2j, w3j, ..., wnj. The weighted sum vj is passed to an activation function f to...
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-f78e0a777a9c5dc76cda197cbee0f206_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Graph of the cost function (Custo (pesos)) versus weights (Pesos).
<!-- /IMAGE_DESCRIPTION -->
### Rede Perceptron

Revisitando um neurônio artificial j:

The diagram illustrates the structure of an artificial neuron  $j$ . On the left, a vertical stack of inputs is shown:  $x_0 = 1$  (highlighted in a red box),  $x_1$ ,  $x_2$ ,  $x_3$ , a vertical ellipsis, and  $x_n$ . Each input is connected to a corresponding weight node:  $w_{0j}$  (green circle),  $w_{1j}$ ,  $w_{2j}$ ,  $w_{3j}$ , a vertical ellipsis, and  $w_{nj}$  (all white circles). The  $w_{0j}$  node is labeled "Peso extra conhecido como bias" in a yellow box. Arrows from each weight node point to a summation node  $\Sigma$  (white circle), which is labeled "Pesos" in a yellow box. The output of the summation node is  $v_j$ . This value is then passed to a square box labeled  $f$ , which is labeled "Função de Ativação" below it. The output of the activation function is  $y_j$ , labeled "Saida" above it.

Diagram of an artificial neuron j. Inputs x0=1 (bias), x1, x2, x3, ..., xn are connected to weights w0j, w1j, w2j, w3j, ..., wnj. The weighted inputs are summed ($\Sigma$) to produce vj, which is then passed through an activation function f to produce the output yj.

$$v_j = w_{0j} + \sum_{i=1}^n (x_i \times w_{ij})$$
$$y_j = f(v_j)$$

**X:  $x_1, x_2, x_3, \dots, x_p$**   
O vetor X representa a entrada do neurônio. Pode ser os dados de entrada da rede ou o sinal de saída de outros neurônios.

{47}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-41aef1f5efab13d4f38f69e86c726062_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of an artificial neuron j. Inputs x0=1 (bias), x1, x2, x3, ..., xn are connected to weights w0j, w1j, w2j, w3j, ..., wnj. The weighted inputs are summed (Σ) to produce vj, which is then passed through an...
<!-- /IMAGE_DESCRIPTION -->
### Rede Perceptron

Revisitando um neurônio artificial j:

$x_0$   $x_0 = 1$

$x_1$   $w_{1j}$

$x_2$   $w_{2j}$

$x_3$   $w_{3j}$

$\vdots$   $\vdots$

$x_n$   $w_{nj}$

Peso extra conhecido como bias

Pesos

$\Sigma$

$v_j$

$f$

Saida  $y_j$

Função de Ativação

Diagram of an artificial neuron j. Inputs x0, x1, x2, x3, ..., xn are shown on the left. x0 is highlighted with a box containing 'x0 = 1'. Arrows from each input point to a weight (w0j, w1j, w2j, w3j, ..., wnj). These weights are grouped by a red box labeled 'Pesos'. An arrow from the weights points to a summation node ($\Sigma$). The output of the summation node is vj. An arrow from vj points to a box labeled 'f' (activation function). Below the box is the text 'Função de Ativação'. The output of the box is labeled 'Saida' and yj.

$$v_j = w_{0j} + \sum_{i=1}^n (x_i \times w_{ij})$$

$$y_j = f(v_j)$$

**W:  $w_1, w_2, w_3, \dots, w_p$**   
O vetor de pesos sinápticos W. Esses valores ponderam as entradas simulando variações na intensidade do sinal.

{48}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-ec3647789b5c38fb686f2a0833324e79_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of an artificial neuron j. Inputs x0, x1, x2, x3, ..., xn are shown on the left. x0 is highlighted with a box containing 'x0 = 1'. Arrows from each input point to a weight (w0j, w1j, w2j, w3j, ..., wnj). These...
<!-- /IMAGE_DESCRIPTION -->
### Rede Perceptron

Revisitando um neurônio artificial j:

$x_0$  →  $w_{0j}$  Peso extra conhecido como bias

$x_0 = 1$

$x_1$  →  $w_{1j}$

$x_2$  →  $w_{2j}$

$x_3$  →  $w_{3j}$

$\vdots$  →  $\vdots$

$x_n$  →  $w_{nj}$

Pesos

$\Sigma$

$v_j$

$f$

Saída  $y_j$

Função de Ativação

Diagram of an artificial neuron j. Inputs x0, x1, x2, x3, ..., xn are shown on the left. x0 is a bias term with x0 = 1. Each input is connected to a weight (w0j, w1j, w2j, w3j, ..., wnj). The weights are multiplied by the inputs and summed at a summation node ($\Sigma$). The result is vj, which is then passed through an activation function f to produce the output yj. A red box highlights the summation node and the activation function. A yellow box above the bias weight is labeled 'Peso extra conhecido como bias'. A red arrow points from the summation node to the mathematical formula for vj.

$$v_j = w_{0j} + \sum_{i=1}^n (x_i \times w_{ij})$$
$$y_j = f(v_j)$$

**$\Sigma$ :**  
Responsável por combinar os valores de entrada. Realiza uma soma ponderada das entradas pelos pesos.

{49}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-01e00200a536673d6cd0e6d8705047a0_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of an artificial neuron j. Inputs x0, x1, x2, x3, ..., xn are shown on the left. x0 is a bias term with x0 = 1. Each input is connected to a weight (w0j, w1j, w2j, w3j, ..., wnj). The weights are multiplied by...
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-8156aeb8a8af817a6465e8b75987e6e7_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Red arrow pointing from the EMQ formula to the cost function graph.
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

**Pesos**

$\Sigma$

$v_j$

$f$

Saída  $y_j$

Função de Ativação

Diagram of an artificial neuron j. Inputs x0, x1, x2, x3, ..., xn are shown on the left. x0 is a bias term with a constant value of 1. Each input is connected to a summation node $\Sigma$ via a weight w\_ij. The summation node outputs v\_j, which is then passed through an activation function f to produce the output y\_j. A red box highlights the summation, activation function, and output stage. A yellow box highlights the bias term w\_0j. A green box contains the mathematical formula for v\_j. A red arrow points from the activation function to the formula for y\_j.

$$v_j = w_{0j} + \sum_{i=1}^n (x_i \times w_{ij})$$
$$y_j = f(v_j)$$

**Função de transferência (ou ativação):**  
Responsável pela modulação do sinal propagado, gera valores excitatórios (positivos) ou inibitórios (zero).

{50}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-8f7c0bf0c75a31fee6b0c7392ff57c39_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of an artificial neuron j. Inputs x0, x1, x2, x3, ..., xn are shown on the left. x0 is a bias term with a constant value of 1. Each input is connected to a summation node Σ via a weight w_ij. The summation node...
<!-- /IMAGE_DESCRIPTION -->
### Rede Perceptron

Revisitando um neurônio artificial  $j$ :

- Existem várias funções de ativação para as redes neurais.
- As clássicas são:
  - Limiar ou degrau
  - Linear
  - Sigmoide: logística ou tangente hiperbólica
- Geralmente o Perceptron usa a função limiar.

Gráfico da função limiar ou degrau. O eixo vertical é  $\phi(v_j)$  e o eixo horizontal é  $\phi_j$ . A função é representada por uma linha tracejada que é constante para  $\phi_j < 0$  e muda abruptamente para um valor constante maior para  $\phi_j \geq 0$ .

(a) Limiar ou Degrau

Gráfico da função limiar ou degrau

Gráfico da função linear. O eixo vertical é  $\phi(v_j)$  e o eixo horizontal é  $\phi_j$ . A função é representada por uma linha tracejada diagonal com declive positivo, passando pela origem.

(b) Linear

Gráfico da função linear

Gráfico da função logística. O eixo vertical é  $\phi(v_j)$  e o eixo horizontal é  $\phi_j$ . A função é representada por uma curva em forma de 'S' (sigmoide) que varia entre dois valores assintóticos, passando pela origem.

(c) Logística

Gráfico da função logística

Gráfico da função tangente hiperbólica. O eixo vertical é  $\phi(v_j)$  e o eixo horizontal é  $\phi_j$ . A função é representada por uma curva em forma de 'S' (sigmoide) que varia entre dois valores assintóticos, passando pela origem, com uma declive mais acentuada no ponto de inflexão.

(d) Tangente Hiperbólica

Gráfico da função tangente hiperbólica

{51}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-2d62ff2bded0c21414a0f40fdf8fd537_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Gráfico da função limiar ou degrau
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-6dda36bad0978e272ca0420b0902b73a_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Gráfico da função linear
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-4134b40f9161ec8fcd3c28bdb48f80b0_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Gráfico da função logística
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-5314dd284c2a98c866862ee0f0fee301_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Gráfico da função tangente hiperbólica
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-8d1cd1205df3b1bc955934cfcfdacded_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Gráfico da função logística, uma curva em forma de S que varia de 0 a 1.
<!-- /IMAGE_DESCRIPTION -->
### Rede Perceptron

Revisitando um neurônio artificial  $j$ :

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

Graph of the logistic function activation function, labeled (c) Logística. The vertical axis is  $\phi(v_j)$  and the horizontal axis is  $\phi_j$ . The function is a dashed S-shaped curve that approaches a negative horizontal asymptote as  $\phi_j \rightarrow -\infty$  and a positive horizontal asymptote as  $\phi_j \rightarrow \infty$ , passing through the origin.

Graph of the logistic function activation function.

Graph of the hyperbolic tangent function activation function, labeled (d) Tangente Hiperbólica. The vertical axis is  $\phi(v_j)$  and the horizontal axis is  $\phi_j$ . The function is a dashed S-shaped curve that approaches a negative horizontal asymptote as  $\phi_j \rightarrow -\infty$  and a positive horizontal asymptote as  $\phi_j \rightarrow \infty$ , passing through the origin.

Graph of the hyperbolic tangent function activation function.

Usuais em MLP

{52}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-fd8369b549b3d1a5c848cbd83659cae9_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Graph of the step function activation function.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-11a2ed9ad059f4289e4475247d633e88_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Graph of the linear function activation function.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-a96c7e19f53f2350db97a90738a6fb51_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Graph of the logistic function activation function.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-caeb46d58919c727aa9d338ae9492077_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Graph of the hyperbolic tangent function activation function.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-41cd1b0cca77430b41ab28d088e82259_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Graph of the step function activation function, labeled (a) Limiar ou Degrau.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-36ea45381c7b7fcbc99ce438860f8f37_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Graph of the linear function activation function, labeled (b) Linear.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-607a666ece1fb3bad30cbe1e61ea0cc6_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Graph of the logistic function activation function, labeled (c) Logistica.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-b8b4869ad9fcbbc3ae62f07ead5fca1a_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Graph of the hyperbolic tangent function activation function, labeled (d) Tangente Hiperbolica.
<!-- /IMAGE_DESCRIPTION -->
### Rede Perceptron

Revisitando um neurônio artificial j:

$x_0$   $x_0 = 1$   $w_{0j}$  *Peso extra conhecido como bias*

$x_1$   $w_{1j}$

$x_2$   $w_{2j}$

$x_3$   $w_{3j}$

$\vdots$   $\vdots$

$x_n$   $w_{nj}$

**Pesos**

$\Sigma$

$v_j$

$f$

**Função de Ativação**

Saida

$y_j$

Diagram of an artificial neuron j. Inputs x0, x1, x2, x3, ..., xn are shown on the left. x0 is a bias term with a constant value of 1. Each input xi is connected to a weight wi\_j. All weighted inputs are summed in a summation node ($\Sigma$). The result v\_j is passed to an activation function f. The output of the function is labeled 'Saida' and y\_j. A red box highlights y\_j, with a red arrow pointing to it from a text box on the right. A yellow box above the bias weight w\_0j contains the text 'Peso extra conhecido como bias'. A label 'Pesos' is placed near the summation node. A label 'Função de Ativação' is placed below the activation function block.

$$v_j = w_{0j} + \sum_{i=1}^n (x_i \times w_{ij})$$
$$y_j = f(v_j)$$

**Y:**  
Sinal de saída do neurônio. Se o neurônio estiver em uma camada de saída, corresponde a saída rede.

{53}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-789ee0a267b24f34bd1f45313e86c9a4_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of an artificial neuron j. Inputs x0, x1, x2, x3, ..., xn are shown on the left. x0 is a bias term with a constant value of 1. Each input xi is connected to a weight wi_j. All weighted inputs are summed in a...
<!-- /IMAGE_DESCRIPTION -->
#### Rede Perceptron - Algoritmo de Treinamento

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
        Para cada atributo i: 1 a n dos dados de X :
             $v_j = v_j + x_i * w_{ij}$ 
         $y_j = f(v_j)$ 
         $erro_j = d_j - y_j$ 
        se  $erro_j \neq 0$  entao :
             $\delta = \eta * erro_j * x_i$ 
             $w_{ij} = w_{ij} + \delta$ 
    erroGeral = erroGeral + abs(erro_j)
```

{54}------------------------------------------------
#### Rede Perceptron - Algoritmo de Treinamento

The diagram illustrates the signal propagation process in a Perceptron network. On the left, inputs  $x_0 = 1$ ,  $x_1$ ,  $x_2$ ,  $x_3$ ,  $\vdots$ , and  $x_n$  are shown. Each input is connected to a weight node:  $x_0 = 1$  connects to  $w_{0j}$ ,  $x_1$  to  $w_{1j}$ ,  $x_2$  to  $w_{2j}$ ,  $x_3$  to  $w_{3j}$ ,  $\vdots$  to  $\vdots$ , and  $x_n$  to  $w_{nj}$ . These weights are collectively labeled "Pesos". All weight nodes connect to a central summation node, represented by a circle containing the symbol  $\Sigma$ . The output of the summation node is fed into a square block labeled  $f$ , which represents the "Função de Ativação" (Activation Function). The output of this block is labeled "Saida" (Output). A large blue arrow at the bottom, labeled "Propagação do Sinal" (Signal Propagation), indicates the direction of the process from left to right.

Diagram of a Perceptron network showing signal propagation from inputs through weights to a summation node, then through an activation function to produce an output.

{55}------------------------------------------------

Dado um neurônio artificial  $j$ :

The diagram illustrates the structure of an artificial neuron  $j$ . On the left, there are inputs  $x_0 = 1$ ,  $x_1$ ,  $x_2$ ,  $x_3$ , a vertical ellipsis, and  $x_n$ . Each input is connected to a weight node:  $w_{0j}$  for  $x_0$ ,  $w_{1j}$  for  $x_1$ ,  $w_{2j}$  for  $x_2$ ,  $w_{3j}$  for  $x_3$ , another vertical ellipsis, and  $w_{nj}$  for  $x_n$ . The word "Pesos" (Weights) is written near these nodes. All weight nodes point to a central summation node, which is a circle containing the symbol  $\Sigma$ . An arrow from the  $w_{0j}$  node points directly to the top of the summation node. The summation node points to a square box labeled  $f$ , which represents the activation function. Below this box is the text "Função de Ativação" (Activation Function). An arrow points from the box  $f$  to the right, labeled "Saida" (Output).

Diagram of an artificial neuron j showing inputs x0 to xn, weights w0j to wnj, a summation node $\Sigma$, an activation function f, and the output Saida.

{56}------------------------------------------------

Dado um neurônio artificial  $j$ :

The diagram illustrates the structure and signal propagation of an artificial neuron  $j$ . On the left, inputs  $x_0 = 1$  (bias),  $x_1$ ,  $x_2$ ,  $x_3$ , and  $x_n$  are shown with red arrows. Each input  $x_i$  is connected to a weight  $w_{ij}$  represented by a circle. The weights  $w_{1j}$ ,  $w_{2j}$ ,  $w_{3j}$ , and  $w_{nj}$  are collectively labeled "Pesos". All weighted inputs are summed at a central node labeled  $\Sigma$ . The bias weight  $w_{0j}$  is also connected to this summation node. The output of the summation is passed to a square block labeled  $f$ , which is identified by an arrow from below as the "Função de Ativação". The final output is labeled "Saida".

Diagram of an artificial neuron j showing signal propagation from inputs x0 to xn through weights w0j to wnj, summation, and activation function f to produce an output.

Recebendo os dados de entrada  $X$

{57}------------------------------------------------

Dado um neurônio artificial  $j$ :

The diagram illustrates the structure of an artificial neuron  $j$ . On the left, there are inputs  $x_0 = 1$ ,  $x_1$ ,  $x_2$ ,  $x_3$ , a vertical ellipsis, and  $x_n$ . Each input is connected to a red circular node representing a weight:  $w_{0j}$  for  $x_0$ ,  $w_{1j}$  for  $x_1$ ,  $w_{2j}$  for  $x_2$ ,  $w_{3j}$  for  $x_3$ , and  $w_{nj}$  for  $x_n$ . The word "Pesos" (Weights) is written near these nodes. Arrows from each weight node point to a central white circular node containing the summation symbol  $\Sigma$ . An arrow from  $w_{0j}$  also points directly to this summation node. The output of the summation node points to a square box labeled  $f$ , which represents the "Função de Ativação" (Activation Function). An arrow from the box points to the final output, labeled "Saida" (Output).

Diagram of an artificial neuron j showing inputs, weights, summation, activation function, and output.

Ponderando as entradas  $X$  pelos pesos  $W$ :  $x_i * w_{ij}$

{58}------------------------------------------------

Dado um neurônio artificial j:

The diagram illustrates the structure of an artificial neuron  $j$ . On the left, inputs  $x_0 = 1$ ,  $x_1$ ,  $x_2$ ,  $x_3$ ,  $\dots$ , and  $x_n$  are shown. Each input is connected to a corresponding weight  $w_{0j}$ ,  $w_{1j}$ ,  $w_{2j}$ ,  $w_{3j}$ ,  $\dots$ , and  $w_{nj}$  represented by circles. The weighted inputs are then summed in a large red circle containing the symbol  $\Sigma$ . The label "Pesos" is positioned near these weights. The output of the summation is a red arrow pointing to a square block labeled  $f$ , which represents the activation function. Below this block is the label "Função de Ativação". The final output of the neuron is labeled "Saida".

Diagram of an artificial neuron j showing inputs x0=1, x1, x2, x3, ..., xn connected to weights w0j, w1j, w2j, w3j, ..., wnj. The weighted inputs are summed in a red circle labeled $\Sigma$. The sum is then passed to an activation function block labeled f, which produces the output 'Saida'. The label 'Pesos' is placed near the weights, and 'Função de Ativação' is placed below the activation function block.

Combinando os sinais:  $soma = w_{0j} + x_1 * w_{1j} + x_2 * w_{2j} + x_3 * w_{3j} + \dots x_n * w_{nj}$

{59}------------------------------------------------

Dado um neurônio artificial  $j$ :

The diagram illustrates the structure of an artificial neuron  $j$ . On the left, there are inputs  $x_0 = 1$ ,  $x_1$ ,  $x_2$ ,  $x_3$ , a vertical ellipsis, and  $x_n$ . Each input is connected to a weight node:  $x_0$  to  $w_{0j}$ ,  $x_1$  to  $w_{1j}$ ,  $x_2$  to  $w_{2j}$ ,  $x_3$  to  $w_{3j}$ , and  $x_n$  to  $w_{nj}$ . The weights are collectively labeled "Pesos". Arrows from each weight node point to a central summation node, which is a circle containing the symbol  $\Sigma$ . An arrow from the summation node points to a red square block labeled  $f$ , which represents the "Função de Ativação" (Activation Function). An arrow from the output of the activation function points to the final output, labeled "Saida" and  $y_j$ .

Diagram of an artificial neuron j showing inputs x0 to xn, weights w0j to wnj, a summation node $\Sigma$, an activation function f, and output yj.

Gerando o sinal de saída:  $y_j = f(\text{soma})$

<!-- DATALAB_CHUNK 4: pages 61-80 -->

{60}------------------------------------------------

# Rede Perceptron - Algoritmo de Treinamento

The diagram illustrates a single neuron in a Perceptron network. On the left, there are inputs  $x_0 = 1$ ,  $x_1$ ,  $x_2$ ,  $x_3$ , a vertical ellipsis, and  $x_n$ . Each input is connected to a weight node:  $x_0 = 1$  connects to  $w_{0j}$ ,  $x_1$  to  $w_{1j}$ ,  $x_2$  to  $w_{2j}$ ,  $x_3$  to  $w_{3j}$ , and  $x_n$  to  $w_{nj}$ . These weight nodes are collectively labeled "Pesos" (Weights). Arrows from each weight node point to a central summation node, which is a circle containing the symbol  $\Sigma$ . An arrow from the summation node points to a square box labeled  $f$ , representing the "Função de Ativação" (Activation Function). An arrow from this box points to the output, labeled "Saida" and  $y_j$ . A large blue arrow at the top, labeled "Ajuste dos pesos" (Weight adjustment), points from right to left, indicating the feedback loop in the training algorithm.

Diagram of a Perceptron network showing inputs, weights, summation, activation function, and output.

{61}------------------------------------------------

# Rede Perceptron - Algoritmo de Treinamento

The diagram illustrates the structure and training flow of a Perceptron. 
 At the top, a large blue arrow pointing left is labeled "Ajuste dos pesos".

Inputs on the left include a bias term  $x_0 = 1$  and variable inputs  $x_1, x_2, x_3, \dots, x_n$ . 
 Each input is associated with a weight:  $w_{0j}, w_{1j}, w_{2j}, w_{3j}, \dots, w_{nj}$ , collectively labeled "Pesos".

The weighted inputs are combined in a summation node  $\Sigma$ . 
 The result is fed into a block  $f$  representing the "Função de Ativação". 
 The final output is labeled "Saida"  $y_j$ .

An error calculation is shown in red:  $\text{Erro} = d_j - y_j$ .

Diagram of a Perceptron network training process. It shows inputs x0 through xn being multiplied by weights w0j through wnj, summed at a sigma node, and passed through an activation function f to produce output yj. An error calculation Erro = dj - yj is shown, and a large arrow indicates weight adjustment back towards the inputs.

{62}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-284768c5ee1a05aa1b9ce396f606a040_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a Perceptron network showing signal propagation from inputs through weights to a summation node, then through an activation function to produce an output.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-675af5bb2357ce5b510e613d04f66bdc_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of an artificial neuron j showing inputs x0 to xn, weights w0j to wnj, a summation node Σ, an activation function f, and the output Saida.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-255efa1d461fc79b4ed367aaec11637f_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of an artificial neuron j showing signal propagation from inputs x0 to xn through weights w0j to wnj, summation, and activation function f to produce an output.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-3c99312f83459559d9a301148555d7b9_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of an artificial neuron j showing inputs, weights, summation, activation function, and output.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-9cd85f266cdb1fb3ad544eb3dd3bd5e4_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of an artificial neuron j showing inputs x0=1, x1, x2, x3, ..., xn connected to weights w0j, w1j, w2j, w3j, ..., wnj.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-0ccaa59b5bc46884777e728ee3dadaa7_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of an artificial neuron j showing inputs x0 to xn, weights w0j to wnj, a summation node Σ, an activation function f, and output yj.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-3766b291e69420b0437ae278b057b5ee_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a Perceptron network showing inputs, weights, summation, activation function, and output.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-fee87ee34f98efee162e918fbaeec613_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a Perceptron network training process.
<!-- /IMAGE_DESCRIPTION -->
## Rede Perceptron - Algoritmo de Treinamento

The diagram illustrates the structure of a Perceptron network. On the left, inputs  $x_0 = 1$ ,  $x_1$ ,  $x_2$ ,  $x_3$ ,  $\dots$ , and  $x_n$  are shown. Each input is connected to a corresponding weight node:  $w_{0j}$ ,  $w_{1j}$ ,  $w_{2j}$ ,  $w_{3j}$ ,  $\dots$ , and  $w_{nj}$ . These weight nodes are collectively labeled "Pesos". The outputs of the weight nodes are fed into a summation node, represented by a circle with the symbol  $\Sigma$ . The output of the summation node is then passed through an activation function, represented by a square box labeled  $f$ . The final output is labeled "Saida" and  $y_j$ . Below the activation function box is the label "Função de Ativação". A large blue arrow at the top, labeled "Ajuste dos pesos", points from the output back to the weights. A red rectangular box containing the text "Atualização dos pesos" is positioned to the right of the weight nodes.

Diagram of a Perceptron network showing the training algorithm. Inputs x0=1, x1, x2, x3, ..., xn are connected to weights w0j, w1j, w2j, w3j, ..., wnj. These weights are summed in a summation node $\Sigma$, which then passes through an activation function f to produce the output yj. A large blue arrow labeled 'Ajuste dos pesos' points from the output back to the weights. A red box labeled 'Atualização dos pesos' is also shown.

{63}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-feae5a5b6e128162dbced0860fd97b9b_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a Perceptron network showing the training algorithm.
<!-- /IMAGE_DESCRIPTION -->
## Rede Perceptron
### Tabela OR

| x1 | x2 | d |
|----|----|---|
| 0  | 0  | 0 |
| 0  | 1  | 1 |
| 1  | 0  | 1 |
| 1  | 1  | 1 |

No treinamento, encontramos os pesos:

$$w_{10} = -1.0, w_{11} = 1.0, w_{12} = 1.0$$

Gráfico da função OR no plano  $x_1$ - $x_2$ . O eixo  $x_1$  é horizontal e o eixo  $x_2$  é vertical. Há pontos azuis nas coordenadas (0,0), (0,1), (1,0) e (1,1). Os pontos (0,1), (1,0) e (1,1) estão rotulados com '1', e o ponto (0,0) está rotulado com '0'. Uma linha preta diagonal com declive negativo representa a fronteira de decisão, passando pelos pontos (0,1) e (1,0).

Gráfico da função OR no plano x1-x2

Fronteira de decisão:

$$w_{11}x_1 + w_{12}x_2 + w_{10} = 0$$

$$1.0x_1 + 1.0x_2 - 1.0 = 0$$

$$\mathbf{x_1 + x_2 - 1.0 = 0}$$

{64}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-808fbf3058e19e39757a0a84c7796059_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Gráfico da função OR no plano x1-x2
<!-- /IMAGE_DESCRIPTION -->
## Algoritmo Backpropagation

The image is a graphic design split vertically. The left side is white and contains the title 'Algoritmo Backpropagation' in a dark blue, sans-serif font. The right side is black and features a blue wireframe globe, showing latitude and longitude lines. A jagged, irregular black silhouette runs down the center, acting as a separator between the white text area and the black graphic area.

Abstract graphic featuring a blue wireframe globe on the right and a jagged black silhouette on the left, separating the text area from the graphic.

{65}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-31d640309e19a64318c874023ba0aadd_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Abstract graphic featuring a blue wireframe globe on the right and a jagged black silhouette on the left, separating the text area from the graphic.
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

O gráfico ilustra a função custo (pesos) no eixo vertical e os pesos no eixo horizontal. Uma curva azul representa a função custo, que é convexa. Um ponto preto na curva representa os 'Pesos iniciais'. Uma seta tracejada com pontas indica a direção do gradiente descendente, apontando para o 'Custo mínimo Global' na base da curva. Uma linha tracejada tangente à curva no ponto inicial indica a direção do 'Gradiente'.

Gráfico da função custo (pesos) vs pesos, mostrando o gradiente descendente.

{67}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-750677d35a0db0f1a6d44ede4e11d347_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Gráfico da função custo (pesos) vs pesos, mostrando o gradiente descendente.
<!-- /IMAGE_DESCRIPTION -->
### Algoritmo de Treinamento para MLP

- O backpropagation possui 2 etapas: **forward** e **backward**. Em cada etapa a rede é percorrida em um sentido.
  - A fase **forward (para frente)** – **propagação** - é utilizada para definir a saída da rede para um dado de entrada.
  - A fase **backward (para trás)** – **retropropagação** - utiliza a saída desejada e a saída gerada pela rede para atualizar os pesos de suas conexões.

O diagrama ilustra uma rede neural MLP com as seguintes características:

- Camada de entrada:** Dois nós de entrada,  $x_1$  e  $x_2$ .
- Camada Oculta ou Intermediária (1):** Três nós numerados 1, 2 e 3.
- Camada Oculta ou Intermediária (2):** Dois nós numerados 4 e 5.
- Camada de Saída:** Dois nós numerados 6 e 7, produzindo as saídas  $y_6$  e  $y_7$ .
- Conexões e Pesos:**
  - De  $x_1$  para os nós 1, 2 e 3: pesos  $w_{11}$ ,  $w_{21}$  e  $w_{31}$ .
  - De  $x_2$  para os nós 1, 2 e 3: pesos  $w_{12}$ ,  $w_{22}$  e  $w_{32}$ .
  - Do nó 1 para os nós 4 e 5: pesos  $w_{41}$  e  $w_{51}$ .
  - Do nó 2 para os nós 4 e 5: pesos  $w_{42}$  e  $w_{52}$ .
  - Do nó 3 para os nós 4 e 5: pesos  $w_{43}$  e  $w_{53}$ .
  - Do nó 4 para os nós 6 e 7: pesos  $w_{64}$  e  $w_{74}$ .
  - Do nó 5 para os nós 6 e 7: pesos  $w_{65}$  e  $w_{75}$ .
  - Termos de viés ( $b$ ): Cada nó na camada oculta e de saída possui um termo de viés ( $w_{10}$ ,  $w_{40}$ ,  $w_{60}$ ,  $w_{50}$ ,  $w_{70}$ ) conectado a ele a partir de cima.
- Fluxo:**
  - Propagação (fase forward):** Indicada por uma seta superior apontando para a direita, representando o fluxo de informação da entrada para a saída.
  - Retropropagação (fase backward):** Indicada por uma seta inferior apontando para a esquerda, representando o fluxo de erro da saída de volta para a entrada.

Diagrama de uma rede neural MLP com 2 camadas ocultas e 2 camadas de saída, ilustrando a propagação forward e a retropropagação backward.

{68}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-27788c2a26d9641e68232a4eff1299b9_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de uma rede neural MLP com 2 camadas ocultas e 2 camadas de saída, ilustrando a propagação forward e a retropropagação backward.
<!-- /IMAGE_DESCRIPTION -->
### Algoritmo de Treinamento para MLP

Cada neurônio da rede foi projetado para realizar dois cálculos:

- **Cálculo do sinal de saída:** corresponde a saída  $y$  de cada neurônio, expresso por uma função não linear aplicada à soma ponderada dos pesos pelas entradas em cada neurônio. Acontece na etapa de propagação.
- **Cálculo de uma estimativa do vetor gradiente:** corresponde os gradientes da superfície do erro em relação aos pesos conectados às entradas de um neurônio. Os gradientes são usados na etapa de retropropagação.

{69}------------------------------------------------
### Algoritmo de Treinamento para MLP

- Considere que a topologia da rede já está definida e que há um conjunto de Treino com  $N$  pares  $(X,D)$ , onde:
  - $X$  é o conjunto de entrada:  $\{x_1, x_2, x_3, x_4, ..x_Z\}$ , com  $Z$  entradas (atributos)
  - $D$  é o conjunto de saídas desejadas:  $\{d_1, d_2, d_3, d_4, ..x_M\}$ , com  $M$  saídas (uma para cada neurônio da camada de saída)

{70}------------------------------------------------
### Algoritmo de Treinamento para MLP

Diagram of a Multi-Layer Perceptron (MLP) showing two input nodes (x1, x2), two hidden layers with three nodes each, and two output nodes (y1, y2). A red arrow labeled 'Propagação' indicates the forward flow from left to right.

1. Iniciar **os pesos da rede arbitrariamente** com valores não nulos.
2. Apresentar cada dado  $n$  de entrada do conjunto de treino e propagá-lo até a saída da rede (geração dos  $y$ 's da camada de saída), onde  $n = 1$  até  $N$ .
3. **Propagação:** Para cada neurônio  $k$  e entrada  $i$ .

$$v_k(n) = \sum_{i=0}^z (w_{ki}(n) \times x_i(n)) \quad y_k(n) = Q(v_k(n))$$

4. **Retropropagação:** Para cada neurônio  $k$ :  $\text{erro}_k = d_k - y_k$

$$\xi(n) = \frac{1}{2} \sum_{k=1}^j \text{erro}_k^2$$

**Energia do erro instantâneo:** combina os erros de todos neurônios da camada de saída para a entrada propagada.

{71}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-f8f8916ae391a1233c13ce738c699109_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a Multi-Layer Perceptron (MLP) showing two input nodes (x1, x2), two hidden layers with three nodes each, and two output nodes (y1, y2).
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-638a308af25f1f56b4456a1fc503f161_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a Multi-Layer Perceptron (MLP) showing two input nodes (x1, x2), two hidden layers with three nodes each, and two output nodes (y1, y2).
<!-- /IMAGE_DESCRIPTION -->
### Algoritmo de Treinamento para MLP

Diagram of a Multi-Layer Perceptron (MLP) showing two input nodes (x1, x2), two hidden layers with three nodes each, and two output nodes (y1, y2). A red arrow labeled 'Propagação' indicates the forward flow from left to right.

1. Iniciar **os pesos da rede arbitrariamente** com valores não nulos.
2. Apresentar cada dado  $n$  de entrada do conjunto de treino e propagá-lo até a saída da rede (geração dos  $y$ 's da camada de saída), onde  $n = 1$  até  $N$ .
3. **Propagação:** Para cada neurônio  $k$  e entrada  $i$ .

$$v_k(n) = \sum_{i=0}^z (w_{ki}(n) \times x_i(n)) \quad y_k(n) = Q(v_k(n))$$

4. **Retropropagação:** Para cada neurônio  $k$ :  $\text{erro}_k = d_k - y_k$

$$\xi(n) = \frac{1}{2} \sum_{k=1}^j \text{erro}_k^2$$

**Energia do erro instantâneo:** combina os erros de todos neurônios da camada de saída para a entrada propagada.

{72}------------------------------------------------
### Algoritmo de Treinamento para MLP

Diagram of a Multi-Layer Perceptron (MLP) showing propagation from input to output. On the left, two input nodes labeled x1 and x2 are connected to three hidden nodes labeled 1, 2, and 3. These three hidden nodes are connected to two output nodes labeled y1 and y2. A red arrow labeled 'Propagação' points from left to right above the diagram.

1. Iniciar **os pesos da rede arbitrariamente** com valores não nulos.
2. Apresentar cada dado  $n$  de entrada do conjunto de treino e propagá-lo até a saída da rede (geração dos  $y$ 's da camada de saída), onde  $n = 1$  até  $N$ .
3. **Propagação:** Para cada neurônio  $k$  e entrada  $i$ .

$$v_k(n) = \sum_{i=0}^z (w_{ki}(n) \times x_i(n)) \quad y_k(n) = Q(v_k(n))$$

4. **Retropropagação:** Para cada neurônio  $k$ :  $\text{erro}_k = d_k - y_k$

$$\xi(n) = \frac{1}{2} \sum_{k=1}^j \text{erro}_k^2$$

**Energia do erro instantâneo:** combina os erros de todos neurônios da camada de saída para a entrada propagada.

{73}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-e5ded249943a879ef58cae5b6b87c576_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a Multi-Layer Perceptron (MLP) showing propagation from input to output.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-4801e73fa692059f2ca78196e6e907be_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a Multi-Layer Perceptron (MLP) showing propagation.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-c98721cd60df9be3ed129ce2345d763d_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a Multi-Layer Perceptron (MLP) showing propagation from input to output.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-b68ed2f7c90787b2fcfeb6be5640ecd4_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a Multi-Layer Perceptron (MLP) showing propagation.
<!-- /IMAGE_DESCRIPTION -->
### Algoritmo de Treinamento para MLP

Diagram of a Multi-Layer Perceptron (MLP) showing propagation. Inputs x1 and x2 are connected to three hidden neurons (red circles 1, 2, 3). These neurons are connected to two output neurons (blue circles). The output neurons produce y1 and y2. Above the output neurons, a red arrow labeled 'Propagação' points to the right, with intermediate values y'1, y'2, and y'3 indicated above the hidden neurons.

1. Iniciar **os pesos da rede arbitrariamente** com valores não nulos.
2. Apresentar cada dado  $n$  de entrada do conjunto de treino e propagá-lo até a saída da rede (geração dos  $y$ 's da camada de saída), onde  $n = 1$  até  $N$ .
3. **Propagação:** Para cada neurônio  $k$  e entrada  $i$ .

$$v_k(n) = \sum_{i=0}^z (w_{ki}(n) \times x_i(n)) \quad y_k(n) = Q(v_k(n))$$

4. **Retropropagação:** Para cada neurônio  $k$ :  $\text{erro}_k = d_k - y_k$

$$\xi(n) = \frac{1}{2} \sum_{k=1}^j \text{erro}_k^2$$

**Energia do erro instantâneo:** combina os erros de todos neurônios da camada de saída para a entrada propagada.

{74}------------------------------------------------
### Algoritmo de Treinamento para MLP

Diagram of a Multi-Layer Perceptron (MLP) showing propagation from input to output. Inputs x1 and x2 are connected to three hidden neurons (blue circles) with weights y'1, y'2, and y'3. These hidden neurons are connected to two output neurons (red circles) labeled 1 and 2, which produce outputs y1 and y2. A red arrow labeled 'Propagação' indicates the forward flow of information.

1. Iniciar **os pesos da rede arbitrariamente** com valores não nulos.
2. Apresentar cada dado  $n$  de entrada do conjunto de treino e propagá-lo até a saída da rede (geração dos  $y$ 's da camada de saída), onde  $n = 1$  até  $N$ .
3. **Propagação:** Para cada neurônio  $k$  e entrada  $i$ .

$$v_k(n) = \sum_{i=0}^z (w_{ki}(n) \times x_i(n)) \quad y_k(n) = Q(v_k(n))$$

4. **Retropropagação:** Para cada neurônio  $k$ :  $\text{erro}_k = d_k - y_k$

$$\xi(n) = \frac{1}{2} \sum_{k=1}^j \text{erro}_k^2$$

**Energia do erro instantâneo:** combina os erros de todos neurônios da camada de saída para a entrada propagada.

{75}------------------------------------------------
### Algoritmo de Treinamento para MLP

Diagram of a Multi-Layer Perceptron (MLP) showing propagation. Inputs x1 and x2 are connected to three hidden neurons (blue circles). The hidden neurons are connected to two output neurons (red circles labeled 1 and 2), which produce outputs y1 and y2. A red arrow labeled 'Propagação' points from left to right above the diagram.

1. Iniciar **os pesos da rede arbitrariamente** com valores não nulos.
2. Apresentar cada dado  $n$  de entrada do conjunto de treino e propagá-lo até a saída da rede (geração dos  $y$ 's da camada de saída), onde  $n = 1$  até  $N$ .
3. **Propagação:** Para cada neurônio  $k$  e entrada  $i$ .

$$v_k(n) = \sum_{i=0}^z (w_{ki}(n) \times x_i(n)) \quad y_k(n) = Q(v_k(n))$$

4. **Retropropagação:** Para cada neurônio  $k$ :  $\text{erro}_k = d_k - y_k$

$$\xi(n) = \frac{1}{2} \sum_{k=1}^j \text{erro}_k^2$$

**Energia do erro instantâneo:** combina os erros de todos neurônios da camada de saída para a entrada propagada.

{76}------------------------------------------------
### Algoritmo de Treinamento para MLP

$$\text{erro}_1 = d_1 - y_1$$

$$\text{erro}_2 = d_2 - y_2$$

Diagram of a Multi-Layer Perceptron (MLP) with two input nodes (x1, x2), two hidden nodes, and two output nodes (y1, y2). A red arrow labeled 'Retropropagação' points from the output nodes back to the input nodes, indicating the error propagation process.

1. Iniciar os pesos da rede arbitrariamente com valores não nulos.
2. Apresentar cada dado  $n$  de entrada do conjunto de treino e propagá-lo até a saída da rede (geração dos  $y$ 's da camada de saída), onde  $n = 1$  até  $N$ .
3. Propagação: Para cada neurônio  $k$  e entrada  $i$ .

$$v_k(n) = \sum_{i=0}^z (w_{ki}(n) \times x_i(n)) \quad y_k(n) = Q(v_k(n))$$

4. Retropropagação: Para cada neurônio  $k$ :  $\text{erro}_k = d_k - y_k$

$$\xi(n) = \frac{1}{2} \sum_{k=1}^j \text{erro}_k^2$$

**Energia do erro instantâneo:** combina os erros de todos neurônios da camada de saída para a entrada propagada.

{77}------------------------------------------------
### Algoritmo de Treinamento para MLP

Diagram of a Multi-Layer Perceptron (MLP) showing retropropagation. It has two input nodes (x1, x2), three hidden nodes (blue), and two output nodes (red, labeled 1 and 2). Arrows point from the output nodes to the hidden nodes, and from the hidden nodes to the input nodes, representing the backward flow of error signals. A red arrow at the top is labeled 'Retropropagação'.

<!-- IMAGE_DESCRIPTION: datalab-08ccf644bfe3417a310e15f03a536ff8_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a Multi-Layer Perceptron (MLP) showing retropropagation.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-8b40238e5eff3457dd5ae0011536e2d9_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a Multi-Layer Perceptron (MLP) showing retropropagation.
<!-- /IMAGE_DESCRIPTION -->
#### 4. Retropropagação:

...

- Calcular os **gradientes da camada de saída**:  $\delta_k(n) = Q'(v_k(n)) \times erro_k(n)$
- Atualizar os pesos dos neurônios

$$\Delta w_{ki}(n) = \delta_k(n) \times \eta \times y_i(n)$$

Exemplos:  $\eta = \{0.01, 0.1, 0.5, 0.9\}$

onde  $\eta$  é a taxa de aprendizado (learning rate) intervalo típico  $(0:1)$

- Quanto menor o valor de  $\eta$ , **menor será a variação dos pesos da rede** de uma iteração para outra e mais suave será e **lenta** a trajetória no espaço de busca pelos pesos;
- Quanto maior o valor de  $\eta$ , haverá **maiores modificações nos pesos da rede** de uma iteração para outra e mais **rápido** será a trajetória no espaço de busca pelos pesos; porém isso **não garante uma boa aprendizagem**, a rede pode se tornar instável e oscilar.

{78}------------------------------------------------
### Algoritmo de Treinamento para MLP

Diagram of a Multi-Layer Perceptron (MLP) showing retropropagation. It has two input nodes (x1, x2), three hidden nodes (blue), and two output nodes (red, labeled 1 and 2). Arrows point from the output nodes to the hidden nodes, and from the hidden nodes to the input nodes, representing the backward flow of error signals. A red arrow at the top is labeled 'Retropropagação'.

4. Retropropagação: onde  $\alpha$  é a constante de momento (momentum rate) intervalo típico  $[0; 1]$

- Calcular os **gradientes da camada de saída**:
- Atualizar os pesos dos neurônios  $\Delta w_{ki}(n) = \delta_k(n) \times \eta \times y_i(n)$

$$w_{ki}(n+1) = w_{ki}(n) + \Delta w_{ki}(n) + \alpha \times w_{ki}(n-1)$$

Exemplos:  $\alpha = \{0.0, 0.1, 0.5, 0.9\}$

- Para evitar o perigo de instabilidade do algoritmo, foi introduzida uma **constante de momento** (momentum rate) :  $\alpha$
- Ela controla e estabiliza a atualização dos pesos.
- Evita que mínimos locais
- Acelera a descida do gradiente em direções com declividade constante.

{79}------------------------------------------------
### Algoritmo de Treinamento para MLP
#### 4. Retropropagação:

...

- Calcular os **gradientes das camadas ocultas**:

$$\delta_k(n) = Q'(v_k(n)) * \sum_{i=1}^t (\delta_j(n) * w_{jk}(n+1))$$

- Atualizar os pesos dos neurônios

$$\Delta w_{ki}(n) = \delta_k(n) \times \eta \times y_i(n)$$

$$w_{ki}(n+1) = w_{ki}(n) + \Delta w_{ki}(n) + \alpha \times w_{ki}(n-1)$$

Diagrama de uma rede neural com retropropagação. À esquerda, dois inputs rotulados  $x_1$  e  $x_2$ . À direita, uma camada oculta com três neurônios (um vermelho rotulado '1', dois azuis) e uma camada de saída com dois neurônios amarelos. Uma seta vermelha apontando para a esquerda acima dos neurônios é rotulada 'Retropropagação', indicando o fluxo de erro de volta.

Diagrama de uma rede neural com retropropagação.

onde  $j$  são os neurônios com os quais o neurônio  $k$  tem conexão à direita.

Como a camada à direita já sofreu retropropagação, seus pesos já foram atualizados, por isso aparece  $n+1$ .

<!-- DATALAB_CHUNK 5: pages 81-100 -->

{80}------------------------------------------------

# Algoritmo de Treinamento para MLP

<!-- IMAGE_DESCRIPTION: datalab-71f0fd23b2f06b621ba89a65ee3c284c_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de uma rede neural com retropropagação.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-59121d561a4158609b4c354b9ffd0605_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de uma rede neural com retropropagação.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-6334c962f5e106e3331e59946e4d166e_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de uma rede neural com retropropagação.
<!-- /IMAGE_DESCRIPTION -->
## 4. Retropropagação:

...

- Calcular os **gradientes das camadas ocultas**:

$$\delta_k(n) = Q'(v_k(n)) * \sum_{i=1}^t (\delta_j(n) * w_{jk}(n+1))$$

- Atualizar os pesos dos neurônios

$$\Delta w_{ki}(n) = \delta_k(n) \times \eta \times y_i(n)$$

$$w_{ki}(n+1) = w_{ki}(n) + \Delta w_{ki}(n) + \alpha \times w_{ki}(n-1)$$

Diagrama de uma rede neural com três camadas: uma camada de entrada com dois neurônios (azuis) rotulados  $x_1$  e  $x_2$ ; uma camada oculta com três neurônios (dois azuis, um vermelho rotulado '2'); e uma camada de saída com dois neurônios (amarelos). Uma seta vermelha apontando para a esquerda, rotulada 'Retropropagação', indica o fluxo de retropropagação da camada de saída de volta para a camada oculta e de entrada.

Diagrama de uma rede neural com retropropagação.

onde  $j$  são os neurônios com os quais o neurônio  $k$  tem conexão à direita.

Como a camada à direita já sofreu retropropagação, seus pesos já foram atualizados, por isso aparece  $n+1$ .

{81}------------------------------------------------
## Algoritmo de Treinamento para MLP
## 4. Retropropagação:

...

- Calcular os **gradientes das camadas ocultas**:

$$\delta_k(n) = Q'(v_k(n)) * \sum_{i=1}^t (\delta_j(n) * w_{jk}(n+1))$$

- Atualizar os pesos dos neurônios

$$\Delta w_{ki}(n) = \delta_k(n) \times \eta \times y_i(n)$$

$$w_{ki}(n+1) = w_{ki}(n) + \Delta w_{ki}(n) + \alpha \times w_{ki}(n-1)$$

Diagrama de uma rede neural com duas camadas ocultas e uma camada de saída. A camada de entrada tem dois neurônios,  $x_1$  e  $x_2$ . A primeira camada oculta tem três neurônios, sendo o terceiro destacado em vermelho com o número 3. A segunda camada oculta tem dois neurônios amarelos. A camada de saída tem dois neurônios amarelos. Uma seta vermelha apontando para a esquerda, rotulada 'Retropropagação', indica o fluxo de retropropagação da saída para a entrada.

Diagrama de uma rede neural com retropropagação.

onde  $j$  são os neurônios com os quais o neurônio  $k$  tem conexão à direita.

Como a camada à direita já sofreu retropropagação, seus pesos já foram atualizados, por isso aparece  $n+1$ .

{82}------------------------------------------------

# Algoritmo de Treinamento para MLP

- Ao final de uma época (passagem de todos os dados do conjunto de treino pela rede)
- Calcular o Erro Médio Quadrado (função de custo)

$$EMQ = \left( \sum_{i=1}^N \xi_i \right) / N$$

Corresponde ao erro médio encontrado para todo o conjunto de treino

É usado como critério de parada. Pode oscilar no início da aprendizagem, mas deve decrescer ao longo do treinamento.

$$\xi(n) = \frac{1}{2} \sum_{k=1}^j \text{erro}_k^2(n)$$

Lembrando que a energia do erro corresponde à combinação dos erros dos neurônios da camada de saída para uma entrada  $n$ .

{83}------------------------------------------------

# Algoritmo de Treinamento para MLP

- Ao final de uma época (passagem de todos os dados do conjunto de treino pela rede)
- Calcular o Erro Médio Quadrado (função de custo)

$$EMQ = \left( \sum_{i=1}^N \xi_i \right) / N$$

Corresponde ao erro médio encontrado para todo o conjunto de treino

Red arrow pointing from the EMQ formula to the cost function graph.

Graph of the cost function (Custo (pesos)) versus weights (Pesos). The curve is a parabola opening upwards. A black dot on the curve represents the 'Pesos iniciais' (initial weights). A dashed line tangent to the curve at this point is labeled 'Gradiente' (gradient). The lowest point of the curve is labeled 'Custo mínimo Global' (global minimum cost). Arrows along the curve point downwards towards the minimum point.

{84}------------------------------------------------
## Algoritmo de Treinamento para MLP
### Critérios de parada do algoritmo backpropagation:

- número pré-definido de épocas;
- valor pré-definido para o erro quadrado médio;
- variação do erro médio nas últimas x épocas inferior a um valor pré-definido (convergência);
- número de padrões corretamente classificados não se alterar;
- combinação desses critérios.

{85}------------------------------------------------
## Revisitando as funções de ativação

A decorative background element resembling a chalkboard filled with handwritten mathematical formulas and sketches. The content includes fragments such as

 $\sum x$ 

,

 $\sqrt{2434.56 - 8x + a^2 - T^2}$ 

,

 $3+3+4.31447$ 

,

 $3^2 = x^2 + yx$ 

,

 $24 + \frac{x}{y} + \frac{a^2 + 3^2}{c} + x^3$ 

,

 $m = 384. + n^{av}$ 

,

 $(x^2 + 34x + 4)$ 

,

 $u=14!$ 

,

 $\sum N_{50} - x - \frac{1}{2} [984 + x9 + p]$ 

,

 $x \leq 549$ 

,

 $r=4$ 

, and

 $\beta = 9 + x^2 + y^2$ 

. Diagrams include a circle with a sector, a coordinate system with a parabola, and various geometric shapes like a rectangle divided into parts. The entire section is bounded on the left by a jagged, white, torn-paper edge.

A collage of mathematical equations and diagrams on a dark background, separated from the text by a jagged white line.

{86}------------------------------------------------

# Algoritmo de Treinamento para MLP

- **Funções de ativação (ou de transferência):**
  - Modelos de redes neurais modernas usam funções de ativação não lineares.
  - Permitem que o modelo crie mapeamentos complexos entre as entradas e saídas da rede: essenciais para o aprendizado de dados complexos, como imagens, vídeo, áudio e conjuntos de dados que não são lineares ou têm alta dimensionalidade.

{87}------------------------------------------------

# Algoritmo de Treinamento para MLP

- Existem várias funções de ativação para as redes neurais.

Perceptron

(a) **Limiar ou Degrau**

The graph shows a step function where the output  $\phi(v_j)$  jumps from a lower constant value to a higher constant value at  $\phi_j = 0$ . The axes are labeled  $\phi(v_j)$  and  $\phi_j$ .

Graph of the step function activation function, labeled (a) Limiar ou Degrau.

(b) **Linear**

The graph shows a linear function represented by a dashed diagonal line passing through the origin. The axes are labeled  $\phi(v_j)$  and  $\phi_j$ .

Graph of the linear function activation function, labeled (b) Linear.

**MultiLayer Perceptron**  
(não lineares)

(c) **Logistica**

The graph shows a logistic (sigmoid) function, an S-shaped dashed curve that transitions smoothly between two horizontal asymptotes. The axes are labeled  $\phi(v_j)$  and  $\phi_j$ .

Graph of the logistic function activation function, labeled (c) Logistica.

(d) **Tangente Hiperbolica**

The graph shows a hyperbolic tangent function, an S-shaped dashed curve symmetric about the origin, transitioning between negative and positive asymptotes. The axes are labeled  $\phi(v_j)$  and  $\phi_j$ .

Graph of the hyperbolic tangent function activation function, labeled (d) Tangente Hiperbolica.

{88}------------------------------------------------

# Algoritmo de Treinamento para MLP

O gráfico mostra a função logística, que é uma curva em forma de S. O eixo horizontal (x) varia de -6 a 6, com marcas a cada 2 unidades. O eixo vertical (y) varia de 0 a 1, com marcas em 0, 0.5 e 1. A curva começa próxima de 0 para x = -6, passa por (0, 0.5) e tende a 1 para x = 6. A área sob a curva é preenchida com uma cor rosa suave.

Gráfico da função logística, uma curva em forma de S que varia de 0 a 1.

- Logística: valores entre  $[0;1]$  :  $Q(v_k) = \frac{1}{1+\exp(-v_k)}$ 
  - Gradiente suave, evitando “saltos” nos valores de saída.
  - Predições claras: Para X acima de 2 ou abaixo de -2, tende a trazer o valor Y (a predição) para a borda da curva, muito próximo de 1 ou 0.
  - Problema: Gradiente de fuga - para valores muito altos ou muito baixos de X, quase não há alteração na predição. Rede não aprende ou o aprendizado é lento. Saídas não centradas em zero. Computacionalmente caro

{89}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-d261c34ab67ef2c320a5b6a75ceed2c5_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A collage of mathematical equations and diagrams on a dark background, separated from the text by a jagged white line.
<!-- /IMAGE_DESCRIPTION -->
## Algoritmo de Treinamento para MLP

Graph of the hyperbolic tangent function, tanh(x), showing an S-shaped curve passing through the origin (0,0) with horizontal asymptotes at y = 1 and y = -1. The x-axis ranges from -5 to 5, and the y-axis ranges from -1 to 1. The area under the curve for x > 0 is shaded in pink.

- Tangente hiperbólica: valores entre  $[-1;1]$ :  $Q(v_k) = \tanh(v_k)$ 
  - Zero centrado - facilitando a modelagem de entradas com valores fortemente negativos, neutros e fortemente positivos.
  - Problema: Gradiente de fuga também.

{90}------------------------------------------------

# Algoritmo de Treinamento para MLP

Gráfico da função ReLU (Rectified Linear Unit). O eixo x varia de -10 a 10, e o eixo y varia de 0 a 10. A função é zero para x <= 0 e cresce linearmente com uma inclinação de 1 para x > 0. A área sob a curva para x > 0 é colorida de rosa.

ReLU: função mais recente

- RELU (RECTIFIED LINEAR UNIT):  $ReLU(x) = \max(0, x)$ 
  - Computacionalmente eficiente - converge rapidamente
  - Não linear - embora pareça uma função linear
  - Problema (Dying ReLU): quando as entradas se aproximam de zero, ou são negativas, o gradiente da função se torna zero, a rede não aprende.

{91}------------------------------------------------

A grayscale image of a neural network diagram. It features several nodes, represented as shiny spheres, connected by lines. The nodes are arranged in a grid-like pattern, with some in sharp focus and others blurred in the background, creating a sense of depth. The overall aesthetic is clean and technical.

<!-- IMAGE_DESCRIPTION: datalab-4661c6f3ed432deb140cecc3563739dd_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Graph of the hyperbolic tangent function, tanh(x), showing an S-shaped curve passing through the origin (0,0) with horizontal asymptotes at y = 1 and y = -1.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-52c2f593b127e110ac6fb67e135f1ad3_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Gráfico da função ReLU (Rectified Linear Unit).
<!-- /IMAGE_DESCRIPTION -->
## Simulando uma rede MLP

{92}------------------------------------------------
### Simulando o treinamento do XOR

- Conjunto de Treino: (-1 : Falso; 1- Verdadeiro)

A diagram of a neural network. On the left, there are two input nodes labeled  $x_1$  and  $x_2$ . Each input node is connected to three hidden nodes arranged vertically in the center. The three hidden nodes are all connected to a single output node on the right. An arrow points to the right from the output node.

Diagram of a neural network with two input nodes (x1, x2), three hidden nodes, and one output node.

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
### Simulando o treinamento do XOR

A diagram of a neural network with three layers. The input layer on the left has two nodes labeled  $x_1$  and  $x_2$ . The hidden layer in the middle has three nodes. The output layer on the right has one node with an arrow pointing to the right. All nodes in the input layer are connected to all nodes in the hidden layer, and all nodes in the hidden layer are connected to the node in the output layer.

Diagram of a neural network topology for XOR simulation.

- Observações:
  - Topologia-Exemplo: 2 x 3 x 1
  - Pesos iniciais gerados aleatoriamente
  - Constante de momento = 0 para simplificar o exemplo.

{94}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-b76d1b06cf06e1c28f844e68507b40ed_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a neural network topology for XOR simulation.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-a4eb9fe011f0e6dc8405f777c5f3f766_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a neural network for XOR simulation.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-796d2e601722450d6456085e0a801e1e_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a neural network for XOR simulation.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-e60c2d24a97a2855d98671d27ea43d0f_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a neural network for XOR simulation.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-67c5b121b58d497a6de5addf4e7bd555_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a neural network for XOR simulation.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-df935fc9efbd024af4ba77e46bb0bb19_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a neural network for XOR simulation.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-691626a7032a642bb74793336c37e274_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a neural network for XOR simulation.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-ca5555bb37f54857199d243feff8479e_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a neural network for XOR simulation.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-3922e505954d53f8864a44dc9ea664c6_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a neural network for XOR simulation.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-09ec8c855800290ecbc282cfef399c32_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Neural network diagram for XOR simulation.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-23d9fcc2863a6b0548d6b4e8abf15106_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a neural network for XOR simulation.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-3b8ac904c44dd47c5ccd03def99a19c4_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a neural network for XOR simulation.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-a66383962afcd0f0458f0d45c101fabf_img.jpg -->
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

The diagram illustrates a neural network with four nodes (1, 2, 3, 4) and their connections. Node 4 is the output node, while nodes 1, 2, and 3 are hidden nodes. The network takes two inputs,  $x_1$  and  $x_2$ , both set to -1. Each node also receives a bias input  $x_0 = 1$ .

Weights are as follows:

- From  $x_0$  to node 1:  $W_{10} = 0.85$
- From  $x_1$  to node 1:  $W_{11} = -0.74$
- From  $x_2$  to node 1:  $W_{12} = -0.97$
- From  $x_0$  to node 2:  $W_{20} = 0.19$
- From  $x_1$  to node 2:  $W_{21} = -0.43$
- From  $x_2$  to node 2:  $W_{22} = 0.58$
- From  $x_0$  to node 3:  $W_{30} = 0.65$
- From  $x_1$  to node 3:  $W_{31} = -0.62$
- From  $x_2$  to node 3:  $W_{32} = 0.33$
- From  $x_0$  to node 4:  $W_{40} = -0.73$
- From node 1 to node 4:  $W_{41} = -0.38$
- From node 2 to node 4:  $W_{42} = -0.87$
- From node 3 to node 4:  $W_{43} = -0.05$

The outputs for the hidden nodes are currently unknown, indicated by  $Y_1 = ?$ ,  $Y_2 = ?$ , and  $Y_3 = ?$ . The output for the final node is also unknown, indicated by  $Y_4 = ?$ .

Diagram of a neural network for XOR simulation showing forward propagation.

{95}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-d2417b04116c354deccb25d98a84a0fb_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a neural network for XOR simulation showing forward propagation.
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

Diagram of a neural network for XOR simulation. It shows an input layer with nodes x1 and x2 (both -1), a hidden layer with nodes 1, 2, and 3, and an output layer with node 4. Node 1 has a bias x0=1 and weights w10=0.85, w11=-0.74, w12=-0.97, resulting in Y1=0.98. Node 2 has a bias x0=1 and weights w20=0.19, w21=-0.43, w22=0.58, resulting in Y2=?. Node 3 has a bias x0=1 and weights w30=0.65, w31=-0.62, w32=0.33, resulting in Y3=?. Node 4 has a bias x0=1 and weights w40=-0.73, w41=0.38, w42=-0.87, w43=-0.05, resulting in Y4=?. Arrows indicate the flow of information from left to right.

$$v_1 = w_{10} + x_1 \times w_{11} + x_2 \times w_{12} = 0.85 + -1 \times -0.74 + -1 \times -0.97 = 2,56$$

$$y_1 = \tanh(2,56) = 0,98$$

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

Diagram of a neural network for XOR simulation. The network consists of an input layer with nodes  $x_1$  and  $x_2$  (both set to -1), a hidden layer with nodes 1, 2, and 3, and an output layer with node 4. Node 1 has output  $Y_1 = 0.98$ . Node 2 has output  $Y_2 = 0.04$  (circled in red). Node 3 has output  $Y_3 = ?$ . Node 4 has output  $Y_4 = ?$ . Weights are labeled on connections:  $w_{10} = 0.85$ ,  $w_{11} = -0.74$ ,  $w_{12} = -0.97$ ,  $w_{20} = 0.19$ ,  $w_{21} = -0.43$ ,  $w_{22} = 0.58$ ,  $w_{30} = 0.65$ ,  $w_{31} = -0.62$ ,  $w_{32} = 0.33$ ,  $w_{40} = -0.73$ ,  $w_{41} = 0.38$ ,  $w_{42} = -0.87$ . A calculation box shows the net input  $v_2$  for node 2:

$$v_2 = w_{20} + x_1 \times w_{21} + x_2 \times w_{22} = 0.19 + -1 \times -0.43 + -1 \times 0.58 = 0,04$$
$$y_2 = \tanh(0,04) = 0.039 = \sim 0,04$$

Diagram of a neural network for XOR simulation. It shows an input layer with nodes x1 and x2 (both -1), a hidden layer with nodes 1, 2, and 3, and an output layer with node 4. Node 1 has output Y1 = 0.98. Node 2 has output Y2 = 0.04 (circled in red). Node 3 has output Y3 = ?. Node 4 has output Y4 = ?. Weights are labeled on connections. A calculation box shows the net input v2 for node 2.

{97}------------------------------------------------
### Simulando o treinamento do XOR

Propagação

$$v_j = w_{j0} + \sum_{i=1}^n (x_i \times w_{ji})$$

$$y_j = f(v_j), \text{ onde } f(v_j) = \tanh(v_j)$$

| x1 | x2 | d  |
|----|----|----|
| -1 | -1 | -1 |
| -1 | 1  | 1  |
| 1  | -1 | 1  |
| 1  | 1  | -1 |

Diagram of a neural network for XOR simulation. The network consists of an input layer with nodes  $x_1$  and  $x_2$  (both with bias  $x_0 = 1$ ), three hidden nodes (1, 2, 3), and an output node (4). The weights are labeled on the connections. Node 3's output  $Y_3 = 0.73$  is circled in red. Node 4's output  $Y_4$  is marked with a question mark.

Weights:

- $w_{10} = 0.85$ ,  $w_{11} = -0.74$ ,  $w_{12} = -0.97$
- $w_{20} = 0.19$ ,  $w_{21} = -0.43$ ,  $w_{22} = 0.58$
- $w_{30} = 0.65$ ,  $w_{31} = -0.62$ ,  $w_{32} = 0.33$
- $w_{40} = -0.73$ ,  $w_{41} = 0.38$ ,  $w_{42} = -0.87$

Outputs:

- $Y_1 = 0.98$
- $Y_2 = 0.04$
- $Y_3 = 0.73$  (circled in red)
- $Y_4 = ?$

Diagram of a neural network for XOR simulation. It shows a forward pass with inputs x1 and x2, three hidden nodes (1, 2, 3), and one output node (4). Weights are labeled on connections. Node 3's output Y3 = 0.73 is circled in red. Node 4's output Y4 is marked with a question mark.

$$\begin{aligned} v_3 &= w_{30} + x_1 \times w_{31} + x_2 \times w_{32} = \\ &0.65 + -1 \times -0.62 + -1 \times 0.33 = \\ &0.94 \\ y_3 &= \tanh(0.94) = 0.73 \end{aligned}$$

{98}------------------------------------------------
### Simulando o treinamento do XOR

Propagação

$$v_j = w_{j0} + \sum_{i=1}^n (x_i \times w_{ji})$$

$$y_j = f(v_j), \text{ onde } f(v_j) = \tanh(v_j)$$

| x1 | x2 | d  |
|----|----|----|
| -1 | -1 | -1 |
| -1 | 1  | 1  |
| 1  | -1 | 1  |
| 1  | 1  | -1 |

The diagram illustrates a neural network architecture for XOR simulation. It consists of an input layer with nodes  $x_1$  and  $x_2$  (both with a bias term  $x_0 = 1$ ), two hidden layers, and an output layer.

- Hidden Layer 1 (Nodes 1 and 2):**
  - Node 1 receives inputs from  $x_0=1$  (weight  $w_{10}=-0.74$ ),  $x_1$  (weight  $w_{11}=-0.74$ ), and  $x_2$  (weight  $w_{12}=-0.97$ ).
  - Node 2 receives inputs from  $x_0=1$  (weight  $w_{20}=0.19$ ),  $x_1$  (weight  $w_{21}=-0.43$ ), and  $x_2$  (weight  $w_{22}=0.58$ ).
- Hidden Layer 2 (Nodes 3 and 4):**
  - Node 3 receives inputs from  $x_0=1$  (weight  $w_{30}=0.65$ ),  $x_1$  (weight  $w_{31}=-0.62$ ), and  $x_2$  (weight  $w_{32}=0.33$ ).
  - Node 4 (Output) receives inputs from  $x_0=1$  (weight  $w_{40}=-0.73$ ), Node 1 (weight  $w_{41}=0.38$ ), Node 2 (weight  $w_{42}=-0.87$ ), and Node 3 (weight  $w_{43}=-0.05$ ).

Outputs shown:  $Y_2 = 0.04$ ,  $Y_3 = 0.73$ , and the final output  $Y_4 = -0.39$  (circled in red).

Diagram of a neural network for XOR simulation. It shows two hidden layers (nodes 1, 2, 3) and one output layer (node 4). Inputs are x1 and x2 with bias x0=1. Weights are labeled w\_ij. Output Y4 is -0.39.

$$v_4 = w_{40} + y_1 \times w_{41} + y_2 \times w_{42} + y_3 \times w_{43} = -0.73 + 0.98 \times 0.38 + 0.04 \times -0.87 + 0.73 \times -0.05 = -0,4289$$

$$y_4 = \tanh(-0,4289) = -0.39...$$

{99}------------------------------------------------
### Simulando o treinamento do XOR

Retropropagação

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

Diagram of a neural network structure for XOR simulation. The network consists of an input layer with nodes  $x_1 = -1$  and  $x_2 = -1$  (both with bias  $x_0 = 1$ ), a hidden layer with nodes 1, 2, and 3 (each with bias  $x_0 = 1$ ), and an output layer with node 4 (with bias  $x_0 = 1$ ). The weights are labeled on the connections between nodes. The output values  $Y_1, Y_2, Y_3, Y_4$  are shown next to their respective nodes.

Weights:

- $W_{10} = 0.85$ ,  $W_{11} = -0.74$ ,  $W_{12} = -0.97$
- $W_{20} = 0.19$ ,  $W_{21} = -0.43$ ,  $W_{22} = 0.58$
- $W_{30} = 0.65$ ,  $W_{31} = -0.62$ ,  $W_{32} = 0.33$
- $W_{40} = -0.73$ ,  $W_{41} = 0.38$ ,  $W_{42} = -0.87$ ,  $W_{43} = -0.05$

Outputs:

- $Y_1 = 0.98$
- $Y_2 = 0.04$
- $Y_3 = 0.73$
- $Y_4 = -0.39$

Diagram of a neural network for XOR simulation. It has an input layer with nodes x1 and x2 (both with bias x0=1), a hidden layer with nodes 1, 2, and 3 (each with bias x0=1), and an output layer with node 4 (with bias x0=1). Weights are labeled on connections between nodes. Output values Y1, Y2, Y3, and Y4 are shown next to their respective nodes.

$$\begin{aligned}\text{erro}_4 &= d_4 - y_4 \\ &= -1 - -0,39 = \\ &\sim -0.61\end{aligned}$$

<!-- DATALAB_CHUNK 6: pages 101-116 -->

{100}------------------------------------------------
#### Simulando o treinamento do XOR

Retropropagação

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

- Input layer: Node x0=1 (bias), x1, x2.
- Hidden layer: Nodes 1, 2, 3. Each has bias x0=1.
- Output layer: Node 4. Has bias x0=1.
- Weights:
  - From x0 to 1: w10 = 0.85
  - From x1 to 1: w11 = -0.74
  - From x2 to 1: w12 = -0.97
  - From x0 to 2: w20 = 0.19
  - From x1 to 2: w21 = -0.43
  - From x2 to 2: w22 = 0.58
  - From x0 to 3: w30 = 0.65
  - From x1 to 3: w31 = -0.62
  - From x2 to 3: w32 = 0.33
  - From x0 to 4: w40 = -0.73
  - From 1 to 4: w41 = 0.38
  - From 2 to 4: w42 = -0.87
  - From 3 to 4: w43 = -0.05
- Outputs: Y1 = 0.98, Y2 = 0.04, Y3 = 0.73, Y4 = -0.39.

Diagram of a neural network for XOR simulation. It has two input nodes (x1, x2) with bias x0=1, three hidden nodes (1, 2, 3) with bias x0=1, and one output node (4) with bias x0=1. Weights are labeled w\_ij. Output values are Y1=0.98, Y2=0.04, Y3=0.73, and Y4=-0.39.

$$\xi(n) = \frac{1}{2} \sum_{k=1}^s erro_k^2$$

$$\begin{aligned}
 erro_4 &= d_4 - y_4 \\
 &= -1 - (-0.39) = \sim 0.61 \\
 \xi((-1,-1)) &= -0.61 \times -0.61 / 2 \\
 &= \sim 0.18
 \end{aligned}$$

{101}------------------------------------------------
### Simulando o treinamento do XOR

Retropropagação

$$\delta_k(n) = Q'(v_k(n)) \times erro_k(n)$$

$$\begin{aligned}
 v_4 &= w_{40} + y_1 \times w_{41} + y_2 \times w_{42} + y_3 \times w_{43} = \\
 &= -0.73 + 0.98 \times 0.38 + 0.04 \times -0.87 + 0.73 \times \\
 &\quad - 0.05 = -0,4289 \\
 \tanh'(-0,4289) &= 1 - \tanh(-0,4289)^2 = \\
 &= 1 - 0,1521 = 0,8479 \\
 \delta_4 &= -0,61 * 0,8479 = -0,5...
 \end{aligned}$$

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

Diagram of a neural network for XOR simulation. It has two input nodes (x1, x2) with bias x0=1. These connect to three hidden nodes (1, 2, 3) with bias x0=1. Hidden nodes connect to one output node (4) with bias x0=1. Weights are labeled: w10, w11, w12 for node 1; w20, w21, w22 for node 2; w30, w31, w32 for node 3; and w40, w41, w42, w43 for node 4. Output values are Y1, Y2, Y3, and Y4 = -0.39.

$$\begin{aligned}
 erro_4 &= d_4 - y_4 \\
 &= -1 - -0,39 = \sim -0.61
 \end{aligned}$$

{102}------------------------------------------------
#### Simulando o treinamento do XOR

Yellow arrow pointing left towards the retropropagation section.

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
 - Input nodes: x1, x2 (both with bias x0=1).  
 - Hidden nodes: 1, 2, 3. Node 1 output Y1 = 0.98; Node 2 output Y2 = 0.04; Node 3 output Y3 = 0.73.  
 - Output node: 4 (green). Output Y4 = -0.39.  
 - Weights to node 4: w41 = 0.38, w42 = -0.87, w43 = -0.05, w40 = -0.88 (circled in red).  
 - Weights from x0: w10 = 0.85, w20 = 0.19, w30 = 0.65.  
 - Weights from x1: w11 = -0.74, w21 = -0.43, w31 = -0.62.  
 - Weights from x2: w12 = -0.97, w22 = 0.58, w32 = 0.33.

Diagram of a neural network for XOR simulation. It has an input layer with nodes x1 and x2 (both with bias x0=1), a hidden layer with nodes 1, 2, and 3, and an output layer with node 4. Weights are labeled on connections between nodes. Node 4 is highlighted in green, and its weight w40 is circled in red.

$\eta = 0.3$   
 $\alpha = 0$   
 $\delta_4 = -0.61 \times 0.8479 = -0.5...$   
 $w_{40} = w_{40} + (-0.50 \times 0.3 \times 1) =$   
 $= -0.73 - 0.15 = -0.88$

$$w_{ki}(n+1) = w_{ki}(n) + \Delta w_{ki}(n) + \alpha \times w_{ki}(n-1)$$

{103}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-ef0572dbc0f9178ab84cc23b3753e18e_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Yellow arrow pointing left towards the retropropagation section.
<!-- /IMAGE_DESCRIPTION -->
#### Simulando o treinamento do XOR

Yellow arrow pointing left with the text 'Retropropagação' inside it.

$\eta = 0.3$   
 $\alpha = 0$   
 $\delta_4 = -0,61 * 0,8479 = -0,5...$   
 $w_{41} = w_{41} + (-0,50 \times 0.3 \times 0.98) =$   
 $= 0.38 - 0,147 = 0.23$

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

Neural network diagram for XOR simulation. It has two input nodes (x1, x2) with bias x0=1, three hidden nodes (1, 2, 3) with bias x0=1, and one output node (4) with bias x0=1. Weights are labeled: w10=0.85, w11=-0.74, w12=-0.97, w20=0.19, w21=-0.43, w22=0.58, w30=0.65, w31=-0.62, w32=0.33, w40=-0.88, w41=0.23 (circled in red), w42=-0.87, w43=-0.05. Output values are Y1=0.98, Y2=0.04, Y3=0.73, Y4=-0.39.

$$w_{ki}(n+1) = w_{ki}(n) + \Delta w_{ki}(n) + \alpha \times w_{ki}(n-1)$$

{104}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-240d66bb698171f40d1acd5b0c098e4f_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Yellow arrow pointing left with the text 'Retropropagação' inside it.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-2fc0e242cbd93c41bb82f48339de7ac1_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Yellow arrow pointing left with the text 'Retropropagação' inside it.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-83a718de2dd31ecd7acfb09449924e04_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Yellow arrow pointing left with the text 'Retropropagação' inside it.
<!-- /IMAGE_DESCRIPTION -->
#### Simulando o treinamento do XOR

Yellow arrow pointing left with the text 'Retropropagação' inside it.

$\eta = 0.3$   
 $\alpha = 0$   
 $\delta_4 = -0,61 \cdot 0,8479 = -0,5...$   
 $w_{42} = w_{42} + (-0,50 \times 0.3 \times 0.04) =$   
 $= -0.87 - 0,006 = -0.876$

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

Neural network diagram for XOR problem. It has two input nodes (x1, x2) with bias x0=1, three hidden nodes (1, 2, 3) with bias x0=1, and one output node (4) with bias x0=1. Weights are labeled: w10=0.85, w11=-0.74, w12=-0.97, w20=0.19, w21=-0.43, w22=0.58, w30=0.65, w31=-0.62, w32=0.33, w40=-0.88, w41=-0.23, w42=-0.87 (circled in red), w43=-0.05. Output values are Y1=0.98, Y2=0.04, Y3=0.73, Y4=-0.39.

$$w_{ki}(n+1) = w_{ki}(n) + \Delta w_{ki}(n) + \alpha \times w_{ki}(n-1)$$

{105}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-c2f5e14ca0ed0f7944c7606451f67d85_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Neural network diagram for XOR problem. It has two input nodes (x1, x2) with bias x0=1, three hidden nodes (1, 2, 3) with bias x0=1, and one output node (4) with bias x0=1. Weights are labeled: w10=0.85, w11=-0.74...
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-6ba310120ebcd99661c4ee1c58a1586c_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Neural network diagram for XOR problem. It has two input nodes (x1, x2) with bias x0=1, three hidden nodes (1, 2, 3) with bias x0=1, and one output node (4) with bias x0=1. Weights are labeled: w10=0.85, w11=-0.74...
<!-- /IMAGE_DESCRIPTION -->
#### Simulando o treinamento do XOR

Yellow arrow pointing left with the text 'Retropropagação' inside it.

$\eta = 0.3$   
 $\alpha = 0$   
 $\delta_4 = -0,61 * 0,8479 = -0,5...$   
 $w_{43} = w_{43} + (-0,50 \times 0.3 \times 0.73) =$   
 $= -0.05 - 0,1095 = -0.1595$

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

Neural network diagram for XOR problem. It has two input nodes (x1, x2) with bias x0=1, three hidden nodes (1, 2, 3) with bias x0=1, and one output node (4) with bias x0=1. Weights are labeled: w10=0.85, w11=-0.74, w12=-0.97, w20=0.19, w21=-0.43, w22=0.58, w30=0.65, w31=-0.62, w32=0.33, w40=-0.88, w41=-0.23, w42=-0.87, w43=-0.15. Output values are Y1=0.98, Y2=0.04, Y3=0.73, Y4=-0.39. The weight w43 is circled in red.

$$w_{ki}(n+1) = w_{ki}(n) + \Delta w_{ki}(n) + \alpha \times w_{ki}(n-1)$$

{106}------------------------------------------------
#### Simulando o treinamento do XOR

Yellow arrow pointing left
### Retropropagação

$$v_1 = w_{10} + x_1 \times w_{11} + x_2 \times w_{12} = 0.85 + -1 \times -0.74 + -1 \times -0.97 = 2,56$$

$$\tanh'(2,56) = 1 - \tanh(2,56)^2 = 1 - 0,97 = 0,03$$

$$\delta_4 = -0,5...$$

$$\delta_1 = 0,03 \times [-0,5 \times 0,23] = \sim -0,003$$

| x1 | x2 | d  |
|----|----|----|
| -1 | -1 | -1 |
| -1 | 1  | 1  |
| 1  | -1 | 1  |
| 1  | 1  | -1 |

Neural network diagram for XOR problem. It consists of an input layer with nodes x1 and x2 (both with bias x0=1), a hidden layer with nodes 1, 2, and 3, and an output layer with node 4 (with bias x0=1). Weights are labeled: w10, w11, w12 for node 1; w20, w21, w22 for node 2; w30, w31, w32 for node 3; and w40, w41, w42, w43 for node 4. Output values are Y1=0.98, Y2=0.04, Y3=0.73, and Y4=-0.39.

● Camada Oculta

● Gradiente Neurônio 1: -0.002781842410268394

● Gradiente Neurônio 2: 0.4444999763647362

● Gradiente Neurônio 3: 0.03803417896970686

$$\delta_k(n) = Q'(v_k(n)) * \sum_{i=1}^t (\delta_j(n) * w_{jk}(n+1))$$

{107}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-346324c08906e6d9320f632ab916f73e_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Neural network diagram for XOR problem. It consists of an input layer with nodes x1 and x2 (both with bias x0=1), a hidden layer with nodes 1, 2, and 3, and an output layer with node 4 (with bias x0=1). Weights are...
<!-- /IMAGE_DESCRIPTION -->
#### Simulando o treinamento do XOR
### Retropropagação

$$w_{10} = w_{10} + (-0,0027 \times 0,3 \times 1) = 0,85 + (-0,00081) = 0,84$$

$$v_1 = w_{10} + x_1 \times w_{11} + x_2 \times w_{12} = 0,85 + (-1) \times (-0,74) + (-1) \times (-0,97) = 2,56$$

$$\tanh'(2,56) = 1 - \tanh(2,56)^2 = 1 - 0,97 = 0,03$$

$$\delta_4 = -0,5 \dots$$

$$\delta_1 = 0,03 \times [-0,5 \times 0,23] = \sim -0,003$$

| x1 | x2 | d  |
|----|----|----|
| -1 | -1 | -1 |
| -1 | 1  | 1  |
| 1  | -1 | 1  |
| 1  | 1  | -1 |

Diagram of a neural network for XOR simulation. It has two input nodes (x1, x2) with bias x0=1, three hidden nodes (1, 2, 3) with bias x0=1, and one output node (4) with bias x0=1. Weights are labeled: w10=0.84, w11=-0.74, w12=-0.97, w20=0.19, w21=-0.43, w22=0.58, w30=0.65, w31=-0.62, w32=0.33, w40=-0.88, w41=0.23, w42=-0.87, w43=-0.15. Output values are Y1=0.98, Y2=0.04, Y3=0.73, Y4=-0.39.
### Camada Oculta

● Gradiente Neurônio 1: -0.002781842410268394

● Gradiente Neurônio 2: 0.4444999763647362

● Gradiente Neurônio 3: 0.03803417896970686

$$\Delta w_{ki}(n) = \delta_k(n) \times \eta \times y_i(n)$$

$$w_{ki}(n+1) = w_{ki}(n) + \Delta w_{ki}(n) + \alpha \times w_{ki}(n-1)$$

{108}------------------------------------------------
#### Simulando o treinamento do XOR
### Retropropagação

$$w_{11} = w_{11} + (-0,0027 \times 0,3 \times -1) = -0,74 + 0,00081 = -0,739 \approx -0,74$$

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

Diagrama de rede neural com 3 camadas: entrada (x0=1, x1, x2), oculta (neurônios 1, 2, 3) e saída (neurônio 4). Pesos e bias são mostrados nas conexões. Neurônio 1 tem w11=-0.74 (circulado em vermelho) e w12=-0.97. Neurônio 2 tem w21=-0.43 e w22=0.58. Neurônio 3 tem w31=-0.62 e w32=0.33. Neurônio 4 tem w41=0.23, w42=-0.87 e w43=-0.15. Bias w10=0.84, w20=0.19, w30=0.65, w40=-0.88. Saídas: y1=0.98, y2=0.04, y3=0.73, y4=-0.39.

$$v_1 = w_{10} + x_1 \times w_{11} + x_2 \times w_{12} = 0.85 + -1 \times -0.74 + -1 \times -0.97 = 2,56$$

$$\tanh'(2,56) = 1 - \tanh(2,56)^2 = 1 - 0,97 = 0,03$$

$$\delta_4 = -0,5 \dots$$

$$\delta_1 = 0,03 \times [-0,5 \times 0,23] \approx -0,003$$

$$\Delta w_{ki}(n) = \delta_k(n) \times \eta \times y_i(n)$$

$$w_{ki}(n+1) = w_{ki}(n) + \Delta w_{ki}(n) + \alpha \times w_{ki}(n-1)$$

{109}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-0eb57eefa7cd45d30e68829ca8a03843_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de rede neural com 3 camadas: entrada (x0=1, x1, x2), oculta (neurônios 1, 2, 3) e saída (neurônio 4).
<!-- /IMAGE_DESCRIPTION -->
#### Simulando o treinamento do XOR
### Retropropagação

$$w_{12} = w_{12} + (-0,0027 \times 0,3 \times -1) = -0,97 + 0,00081 = -0,96919 \approx -0,97$$

$$v_1 = w_{10} + x_1 \times w_{11} + x_2 \times w_{12} = 0,85 + -1 \times -0,74 + -1 \times -0,97 = 2,56$$

$$\tanh'(2,56) = 1 - \tanh(2,56)^2 = 1 - 0,97 = 0,03$$

$$\delta_4 = -0,5 \dots$$

$$\delta_1 = 0,03 \times [-0,5 \times 0,23] \approx -0,003$$

| x1 | x2 | d  |
|----|----|----|
| -1 | -1 | -1 |
| -1 | 1  | 1  |
| 1  | -1 | 1  |
| 1  | 1  | -1 |

Diagram of a neural network for XOR simulation. It has two input nodes (x1, x2) with bias x0=1, three hidden nodes (1, 2, 3) with bias x0=1, and one output node (4) with bias x0=1. Weights are labeled: w10=0.84, w11=-0.74, w12=-0.97 (circled in red), w20=0.19, w21=-0.43, w22=0.58, w30=0.65, w31=-0.62, w32=0.33, w40=-0.88, w41=0.23, w42=-0.87, w43=-0.15. Output values are Y1=0.98, Y2=0.04, Y3=0.73, Y4=-0.39.
#### Camada Oculta

- Gradiente Neurônio 1: -0.002781842410268394
- Gradiente Neurônio 2: 0.4444999763647362
- Gradiente Neurônio 3: 0.03803417896970686

$$\Delta w_{ki}(n) = \delta_k(n) \times \eta \times y_i(n)$$

$$w_{ki}(n+1) = w_{ki}(n) + \Delta w_{ki}(n) + \alpha \times w_{ki}(n-1)$$

{110}------------------------------------------------
#### Simulando o treinamento do XOR
### Retropropagação

| x1 | x2 | d  |
|----|----|----|
| -1 | -1 | -1 |
| -1 | 1  | 1  |
| 1  | -1 | 1  |
| 1  | 1  | -1 |

- Camada Oculta
- Gradiente Neurônio 1: -0.002781842410268394
- Gradiente Neurônio 2: 0.4444999763647362
- Gradiente Neurônio 3: 0.03803417896970686

The diagram illustrates a neural network architecture for XOR simulation. It consists of:

- Input Layer:** Two nodes,  $x_1$  and  $x_2$ , both with a bias term  $x_0 = 1$ .
- Hidden Layer:** Three nodes, labeled 1, 2, and 3, each with its own bias term  $x_0 = 1$ .
- Output Layer:** One node, labeled 4, with a bias term  $x_0 = 1$ .

 Connections and weights:

- From  $x_0=1$  to Node 1:  $W_{10} = 0.84$
- From  $x_1$  to Node 1:  $W_{11} = -0.74$
- From  $x_2$  to Node 1:  $W_{12} = -0.97$  (circled in red)
- From  $x_0=1$  to Node 2:  $W_{20} = 0.19$
- From  $x_1$  to Node 2:  $W_{21} = -0.43$
- From  $x_2$  to Node 2:  $W_{22} = 0.58$
- From  $x_0=1$  to Node 3:  $W_{30} = 0.65$
- From  $x_1$  to Node 3:  $W_{31} = -0.62$
- From  $x_2$  to Node 3:  $W_{32} = 0.33$
- From Node 1 to Node 4:  $W_{41} = 0.23$
- From Node 2 to Node 4:  $W_{42} = -0.87$
- From Node 3 to Node 4:  $W_{43} = -0.15$
- From  $x_0=1$  to Node 4:  $W_{40} = -0.88$

 Output values:

- $Y_1 = 0.98$
- $Y_2 = 0.04$
- $Y_3 = 0.73$
- $Y_4 = -0.39$

Diagram of a neural network for XOR simulation. It has two input nodes (x1, x2) with bias x0=1, three hidden nodes (1, 2, 3) with bias x0=1, and one output node (4) with bias x0=1. Weights are labeled on connections. Node 1 has output Y1=0.98, Node 2 has Y2=0.04, Node 3 has Y3=0.73, and Node 4 has Y4=-0.39. Weight W12 = -0.97 is circled in red.

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
### Simulando o treinamento do XOR

A diagram of a neural network with two input nodes labeled  $x_1$  and  $x_2$ . These inputs are connected to three hidden nodes. The hidden nodes are then connected to a single output node. The output node has an arrow pointing to the right, indicating the output of the network.

Diagram of a neural network for XOR simulation. It has two input nodes labeled x1 and x2, three hidden nodes, and one output node. All nodes are fully connected to each other. The output node has an arrow pointing to the right.
### Pesos Finais:

- Camada Oculta
  - Neurônio: 1:  $w[10]=2.545363016862031$ ,  
 $w[11]=-1.8662421473793356$ ,  $w[12]=-1.7588858258650666$
  - Neurônio: 2:  $w[20]=0.1914996892738543$ ,  
 $w[21]=-0.4332485003836084$ ,  $w[22]=0.5833743630800029$
  - Neurônio: 3:  $w[30]=0.655200823402003$   
 $w[31]=-0.6209562373205424$   $w[32]=0.3376845283666482$
- Camada de Saida
  - Neurônio: 4:  $w[40]=0.36071557007625865$ ,  
 $w[41]=2.388002191368662$ ,  $w[42]=4.357544216452374$ ,  
 $w[43]=-5.4985276529155485$

{113}------------------------------------------------
### Implementando uma MLP
## `sklearn.neural_network.MLPClassifier`

```
class sklearn.neural_network.MLPClassifier(hidden_layer_sizes=(100,), activation='relu', *, solver='adam', alpha=0.0001,
batch_size='auto', learning_rate='constant', learning_rate_init=0.001, power_t=0.5, max_iter=200, shuffle=True, random_state=None,
tol=0.0001, verbose=False, warm_start=False, momentum=0.9, nesterovs_momentum=True, early_stopping=False,
validation_fraction=0.1, beta_1=0.9, beta_2=0.999, epsilon=1e-08, n_iter_no_change=10, max_fun=15000) [source]
```

- **hidden\_layer\_sizes** : vetor com a quantidade de neurônios da camada oculta - default=(100,)
- **activation**{'identity', 'logistic', 'tanh', 'relu'}, default='relu' - função de ativação para camada oculta
  - 'identity', sem ativação, retorna  $f(x) = x$
  - 'logistic', função sigmoide logística , retorna  $f(x) = 1 / (1 + \exp(-x))$ .
  - 'tanh', função tangente hiperbólica, retorna  $f(x) = \tanh(x)$ .
  - 'relu', função *rectified linear unit*, retorna  $f(x) = \max(0, x)$

{114}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-c803f6f6e2c49429d2951832bd0f208d_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Abstract visualization of a neural network architecture.
<!-- /IMAGE_DESCRIPTION -->
### Implementando uma MLP

- **solver**{'lbfgs', 'sgd', 'adam'}, default='adam'  
Usado para otimização dos pesos.
  - 'sgd' : refere-se ao gradiente descendente estocástico..
  - 'adam' : refere-se ao otimizador baseado em gradiente.
  - 'lbfgs' : otimizador quasi-Newton methods.
- **learning\_rate\_init** float, default=0.001  
Taxa de aprendizagem, usada quando='sgd' ou 'adam'.
- **max\_iter** int, default=200 - Número máximo de iterações.
- **verbose** bool, default=False – Exibe mensagens sobre a rede.
- **Momentum** float, default=0.9 - Constante de momento para atualização do gradiente .  
Deve estar entre [0;1]. Somente usar quando solver='sgd'.

{115}------------------------------------------------
## Dinâmica

- **Atividade 1:** Implemente em Python o algoritmo de treinamento da rede MultiLayer Perceptron para o XOR.

| x1 | x2 | d |
|----|----|---|
| 0  | 0  | 0 |
| 0  | 1  | 1 |
| 1  | 0  | 1 |
| 1  | 1  | 0 |

Diagram of a MultiLayer Perceptron (MLP) neural network. The input layer has 2 nodes ( $x_1$  and  $x_2$ ). The hidden layer has 2 nodes. The output layer has 2 nodes ( $y_1$  and  $y_2$ ). All nodes in adjacent layers are fully connected. Below the diagram, the text "2 x 2 x 2" indicates the number of nodes in each layer.

Diagram of a MultiLayer Perceptron (MLP) neural network for XOR. It consists of an input layer with 2 nodes (x1, x2), a hidden layer with 2 nodes, and an output layer with 2 nodes (y1, y2). All nodes in adjacent layers are fully connected. Below the diagram, the text '2 x 2 x 2' indicates the number of nodes in each layer.
