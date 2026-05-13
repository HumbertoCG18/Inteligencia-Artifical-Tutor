<!-- EXEC_SUMMARY_START -->
## Sumário
> *Leia antes de varrer o arquivo. Vá direto à seção relevante para a pergunta do aluno.*

- **Roteiro**
  - Neurônio Biológico
  - Neurônio Artificial
  - Neurônio Biológico
  - Neurônio Artificial
  - Neurônio Biológico
  - Neurônio Artificial
  - Neurônio Biológico
  - Neurônio Artificial
  - Neurônio Biológico
  - Neurônio Artificial
  - Neurônio Biológico
  - Neurônio Artificial
  - Neurônio Biológico
  - Neurônio Biológico
- **Imagens Curadas**

<!-- EXEC_SUMMARY_END -->
{0}------------------------------------------------

# Green horizontal barIntrodução a redes neurais

Silvia Moraes

An abstract graphic on the right side of the slide, featuring a network of interconnected blue lines forming various geometric shapes like triangles and polygons. The lines are glowing against a dark background, with some nodes appearing as small, bright points.

Abstract blue wireframe graphic

{1}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-30a26f2d17ca95672702bf50fb4f0242_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Abstract blue wireframe graphic
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-dc1e692e5b7efd8e5a2a790c458646d9_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A white door slightly ajar, set against a solid blue background, symbolizing a transition or opportunity.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-d4e9f8f6bf5d7853ecae9c9633900af1_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A stylized illustration of a human brain composed of a dense network of nodes and connecting lines, set against a blue background with faint numerical data.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-d336e7ffee4f537d0805ca840ec28582_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A stylized, wireframe representation of a human brain, composed of interconnected nodes and lines, set against a blue background with faint numerical data and grid lines, symbolizing computational or artificial...
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-ec0158057f8ccaf74edba16682ec5444_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Abstract visualization of a neural network architecture.
<!-- /IMAGE_DESCRIPTION -->
## Roteiro

- Introdução
- Conceito de Rede Neural
- Neurônio Biológico x Neurônio Artificial
- Algumas arquiteturas de Redes Neuronais
- Introdução a rede neural Perceptron
- Topologias de rede

A glowing blue and cyan image of a biological neuron, showing the cell body and branching axons against a dark background. The neuron's soma is a bright, textured blue sphere, with several long, thin axons extending from it in various directions. The axons are also glowing with a cyan light, creating a complex network of lines against a black background. The overall effect is futuristic and scientific.

A glowing blue and cyan image of a biological neuron, showing the cell body and branching axons against a dark background.

{2}------------------------------------------------

Existem várias tarefas que **exigem atenção a diferentes eventos ao mesmo tempo e o processamento de informações variadas** para que sejam tomadas decisões e executadas ações convenientes.

A close-up, high-angle view of a complex, dark-colored maze or labyrinth. The maze is made of thick, dark material, possibly wood or plastic, with many interconnected paths and dead ends. The lighting is focused on the maze, making it stand out against a dark background. The perspective is from above, looking down into the maze, which creates a sense of depth and complexity.

A close-up, high-angle view of a complex, dark-colored maze or labyrinth, showing many interconnected paths and dead ends.

{3}------------------------------------------------

Tarefas até mesmo simples, como pegar um objeto, abrir uma porta ou mesmo caminhar envolvem a ação de **memória, aprendizado e coordenação.**

A white, paneled door is slightly ajar, set against a solid blue background. The door is open just enough to reveal a bright white space beyond, suggesting a transition or opportunity. The lighting is soft and even, highlighting the door and the surrounding wall.

A white door slightly ajar, set against a solid blue background, symbolizing a transition or opportunity.

{4}------------------------------------------------

O sistema nervoso, do qual faz parte o **cérebro**, é um conjunto complexo de células que determinam o funcionamento e comportamento dos seres vivos.

A 3D rendering of a human brain split vertically. The left hemisphere is covered in a white wireframe grid, while the right hemisphere is covered in a dense, tangled web of colorful lines (yellow, green, blue, red) representing neural activity or connections. The brain is resting on a dark, reflective surface.

A 3D rendering of a human brain split vertically. The left hemisphere is covered in a white wireframe grid, while the right hemisphere is covered in a dense, tangled web of colorful lines (yellow, green, blue, red) representing neural activity or connections. The brain is resting on a dark, reflective surface.

{5}------------------------------------------------

A **unidade fundamental** do sistema nervoso é o **neurônio**.

Célula nervosa diferente das demais que se caracteriza por **responder a estímulos externos e internos**; e por **transmitir impulsos** a outras células nervosas, musculares e glandulares..

A 3D rendering of a human brain split vertically. The left hemisphere is covered in a white, circuit-like pattern, while the right hemisphere is covered in a dense, tangled web of colorful lines (yellow, green, blue, red) representing neural activity or connections. The brain is set against a dark, textured background.

A 3D rendering of a human brain split vertically. The left hemisphere is covered in a white, circuit-like pattern, while the right hemisphere is covered in a dense, tangled web of colorful lines (yellow, green, blue, red) representing neural activity or connections. The brain is set against a dark, textured background.

{6}------------------------------------------------

**O cérebro humano  
possui cerca de 10 a 500  
bilhões de neurônios.**

A stylized, glowing blue and white representation of a human brain, overlaid with a complex network of lines and nodes, suggesting neural activity or data processing. The brain is shown in a semi-transparent view, revealing internal structures like the cerebrum and cerebellum. The network lines connect various points on the brain's surface, creating a web-like effect. The background is a solid blue color, and the overall aesthetic is futuristic and technological.

{7}------------------------------------------------

Estima-se que esteja  
organizado em **1000**  
**módulos.**

**Cada módulo com cerca  
de 500 redes neurais.**

A stylized, glowing blue brain composed of interconnected nodes and lines, representing a neural network structure, set against a dark blue background with faint numerical data.

A stylized, glowing blue brain composed of interconnected nodes and lines, representing a neural network structure, set against a dark blue background with faint numerical data.

{8}------------------------------------------------

Cada neurônio pode  
estar **conectado a**  
**centenas** ou até mesmo  
**milhares** de outros  
neurônios.

A stylized illustration of a human brain, rendered in a translucent, glowing blue-grey color. The brain is depicted as a complex network of nodes (small white dots) connected by a web of thin, light-colored lines, symbolizing neural connectivity. The background is a solid blue gradient, overlaid with faint, semi-transparent numerical data and grid lines, suggesting a digital or computational theme. The overall aesthetic is clean, modern, and scientific.

A stylized illustration of a human brain composed of a dense network of nodes and connecting lines, set against a blue background with faint numerical data.

{9}------------------------------------------------

As redes de neurônios  
trabalham de forma **massiva  
e paralela**, com **grande  
rapidez**.

O tempo de execução  
dos neurônios é normalmente  
de **0,001 segundos**.

A stylized, glowing blue brain composed of a dense network of nodes and connecting lines, set against a dark blue background with faint, scattered numbers and grid lines, suggesting a digital or artificial neural network.

A stylized, glowing blue brain composed of a dense network of nodes and connecting lines, set against a dark blue background with faint, scattered numbers and grid lines, suggesting a digital or artificial neural network.

{10}------------------------------------------------

Essas capacidades e habilidades motivaram o desenvolvimento de **técnicas computacionais inspiradas no cérebro humano.**

A stylized, wireframe representation of a human brain, composed of interconnected nodes and lines, set against a blue background with faint numerical data and grid lines, symbolizing computational or artificial intelligence.

A stylized, wireframe representation of a human brain, composed of interconnected nodes and lines, set against a blue background with faint numerical data and grid lines, symbolizing computational or artificial intelligence.

{11}------------------------------------------------

**Redes Neuronais Artificiais** são sistemas computacionais distribuídos compostos de unidades simples (neurônios), densamente interconectados.

An abstract visualization of a neural network architecture. On the left, three distinct input nodes are shown, each emitting a vibrant, glowing stream of light (cyan, magenta, and yellow). These streams converge and spread into a dense, complex web of interconnected nodes and lines, represented by a multitude of small, colorful squares and dots. The network is depicted against a dark background, with the glowing elements creating a sense of dynamic energy and complexity.

Abstract visualization of a neural network architecture.

{12}------------------------------------------------

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

{13}------------------------------------------------

Qual a relação entre  
os neurônios  
biológicos e os  
artificiais?

A stylized illustration of several interconnected neurons. The neurons have glowing yellow cell bodies and branching axons that are illuminated with a warm orange and red light. The background is dark, making the glowing neurons stand out. The axons are thin and wavy, and the cell bodies are rounded and central.

A stylized illustration of several interconnected neurons, featuring glowing yellow cell bodies and branching axons, set against a dark background.

{14}------------------------------------------------

Os principais componentes de um neurônio são :

- **dendritos,**
- **corpo celular e**
- **axônio.**

A detailed illustration of several neurons against a dark, reddish-brown background. Each neuron features a prominent, glowing yellow cell body (soma) with multiple branching dendrites extending from it. Long, thin axons extend from the cell bodies, some of which are covered in segments of myelin sheath, appearing as alternating light and dark rings. The axons terminate in several small, glowing yellow spheres representing synaptic terminals. The overall style is a soft, glowing digital rendering.

Illustration of several neurons with yellow cell bodies and branching axons.

{15}------------------------------------------------

Como esses  
componentes são  
simulados em um  
neurônio artificial?

A stylized illustration of a neural network. It features several glowing yellow circular nodes, each surrounded by a soft orange aura. These nodes are interconnected by a web of thin, wavy lines in shades of orange and red. The background is a dark, deep red gradient, creating a sense of depth and energy. The overall aesthetic is futuristic and digital, representing the complex connections and data flow within an artificial neural network.

A stylized illustration of a neural network with glowing yellow nodes and orange connections.

{16}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-61972112770d9c8fb00883057954f885_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A glowing blue and cyan image of a biological neuron, showing the cell body and branching axons against a dark background.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-7ee2d12e8cbaacaf65b0c332d1c76daf_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A close-up, high-angle view of a complex, dark-colored maze or labyrinth, showing many interconnected paths and dead ends.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-9ebd85380ef496499e5f23ec0d9cd744_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A stylized, glowing blue and white representation of a human brain, overlaid with a complex network of lines and nodes, suggesting neural activity or data processing.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-78f163db583eb0c6d013e6f8ffe6d7d8_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A stylized illustration of several interconnected neurons, featuring glowing yellow cell bodies and branching axons, set against a dark background.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-d25a962fde4b3171879749757440c3c5_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Illustration of several neurons with yellow cell bodies and branching axons.
<!-- /IMAGE_DESCRIPTION -->
### Neurônio Biológico

Fonte: <https://www.deeplearningbook.com.br/>

Diagrama de um neurônio biológico. O corpo celular central contém o núcleo. Dendritos ramificam-se a partir do corpo celular, recebendo sinais. Um longo axônio estende-se a partir do corpo celular, conduzindo o impulso nervoso. O axônio termina em ramificações terminais. Setas vermelhas indicam o sentido do impulso nervoso, que flui dos dendritos, através do corpo celular e do axônio, para as ramificações terminais.

Diagrama de um neurônio biológico

<!-- IMAGE_DESCRIPTION: datalab-7b1cea8c45c49887a750926f2135fa84_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de um neurônio biológico
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-fed351d1b7c4568a439a8682c27f8cc3_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de um neurônio biológico
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-63c666b05041841b01fdef9fa4153ff7_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de um neurônio biológico
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-20ab59bc10b900f6cf8a34549848bbf4_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de um neurônio biológico
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-b25cc68846b070bbe56a949b011ba91c_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de um neurônio biológico
<!-- /IMAGE_DESCRIPTION -->
### Neurônio Artificial

Diagrama de um neurônio artificial. À esquerda, múltiplas entradas ( $x_1, x_2, \dots, x_p$ ) são conectadas a um somador ( $\Sigma$ ). Cada entrada  $x_i$  é multiplicada por um peso  $w_i$  antes de ser somada. O resultado da soma é processado por uma função de ativação  $f(a)$ , representada por um gráfico de degrau no centro. A saída resultante é denotada por  $y$ .

McCulloch – Pitts (1943)

Diagrama de um neurônio artificial

{17}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-8307f6b04df072c9332f9987e034272c_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de um neurônio artificial
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-77464a47f104d0d647b2414591137b64_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de um neurônio artificial
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-e636d7ccca0ad14c6b95201404324823_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de um neurônio artificial
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-73dff6b45b2b9ffd384bab3235f869af_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de um neurônio artificial
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-5793a44ffdadd039928e2f9fe6daae06_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de um neurônio artificial
<!-- /IMAGE_DESCRIPTION -->
### Neurônio Biológico
#### Dendritos:

são prolongamentos especializados na recepção de estímulos nervosos provenientes de outros neurônios ou do ambiente.

Fonte: <https://www.deeplearningbook.com.br/>

Diagrama de um neurônio biológico. O corpo celular central contém o núcleo. Dendritos ramificados se estendem do corpo celular, recebendo estímulos (indicados por setas vermelhas). Um longo axônio se estende do corpo celular, conduzindo o impulso nervoso (indicado por uma seta vermelha) para as ramificações terminais do axônio. Uma seta vermelha na base indica o sentido do impulso nervoso.

Diagrama de um neurônio biológico
### Neurônio Artificial

**X:**  $x_1, x_2, x_3, \dots, x_p$

O vetor X de dados simula os dendritos. Representa a entrada. X pode ser os dados de entrada da rede ou o sinal de saída de outros neurônios.

Diagrama de um neurônio artificial. À esquerda, um vetor de entrada X com componentes  $x_1, x_2, \dots, x_p$  é mostrado em um retângulo verde. Cada componente está conectada a um nó de soma ( $\Sigma$ ) por meio de um peso  $w_1, w_2, \dots, w_p$ . O resultado da soma é processado por uma função de ativação  $f(a)$ , representada por um gráfico de degrau no plano  $(a, f(a))$ . A saída final é  $y$ .

McCulloch – Pitts (1943)

Diagrama de um neurônio artificial

{18}------------------------------------------------
### Neurônio Biológico
#### Dendritos:

são prolongamentos especializados na recepção de estímulos nervosos provenientes de outros neurônios ou do ambiente.

Diagrama de um neurônio biológico. O corpo celular (soma) é central, com múltiplos dendritos ramificados para receber estímulos. Um longo axônio se estende do corpo celular, coberto por segmentos da bainha de mielina. A extremidade do axônio termina em várias sinapses, representadas por pequenos círculos rosas, onde o sinal é transmitido para outros neurônios.

Diagrama de um neurônio biológico com rótulos: Dendrito, Corpo celular, Axônio, Bainha de mielina e Sinapse.
### Neurônio Artificial

**X:  $x_1, x_2, x_3, \dots, x_p$**

O vetor X de dados simula os dendritos. Representa a entrada. X pode ser os dados de entrada da rede ou **o sinal de saída de outros neurônios**.

Diagrama de um neurônio artificial em duas camadas. Na primeira camada, as entradas  $x_1, x_2, x_3, \dots, x_n$  são conectadas a um nó de soma ( $\Sigma$ ) através de pesos  $w_{1j}, w_{2j}, w_{3j}, \dots, w_{nj}$ . O resultado da soma é passado por uma função de ativação  $\varphi$ . Na segunda camada, a saída da primeira camada é conectada a outro nó de soma ( $\Sigma$ ) através de pesos  $w_{1j}, w_{2j}, w_{3j}, \dots, w_{nj}$ . Este segundo resultado também é passado por uma função de ativação  $\varphi$  para gerar a saída final. Red arrows point to the input and output stages.

Diagrama de um neurônio artificial em duas camadas, mostrando entradas, pesos, soma, função de ativação e saídas.

{19}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-12de9b926df0384ec07702671827c9cd_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de um neurônio artificial em duas camadas, mostrando entradas, pesos, soma, função de ativação e saídas.
<!-- /IMAGE_DESCRIPTION -->
### Neurônio Biológico
#### Dendritos:

são prolongamentos especializados na recepção de estímulos nervosos provenientes de outros neurônios ou do ambiente. **Recebem sinais com intensidade e frequência diferentes.**

Diagrama de um neurônio biológico. O corpo celular central contém o núcleo. Dendritos ramificados se estendem do corpo celular, recebendo sinais (indicados por setas vermelhas). Um longo axônio se estende do corpo celular, terminando em ramificações terminais. Uma seta vermelha indica o sentido do impulso nervoso, que flui do corpo celular ao longo do axônio.

Fonte: <https://www.deeplearningbook.com.br/>

Diagrama de um neurônio biológico
### Neurônio Artificial

**W:  $w_1, w_2, w_3, \dots, w_p$**

O vetor de pesos sinápticos W simula as intensidades diferentes do sinal. Esses valores ponderam as entradas simulando variações na intensidade do sinal.

Diagrama de um neurônio artificial. As entradas  $x_1, x_2, \dots, x_p$  são multiplicadas pelos pesos  $w_1, w_2, \dots, w_p$  (representados em um vetor W) e somadas ( $\Sigma$ ). O resultado é então processado por uma função de ativação  $f(a)$  (representada por um gráfico de degrau), produzindo a saída  $y$ .

McCulloch – Pitts (1943)

Diagrama de um neurônio artificial

{20}------------------------------------------------
### Neurônio Biológico
#### Corpo Celular:

Recebe os estímulos dos dendritos , os combina e os processa.

Fonte: <https://www.deeplearningbook.com.br/>

Diagrama de um neurônio biológico. O corpo celular (soma) contém o núcleo. Dendritos ramificados recebem estímulos (indicados por setas vermelhas). Um longo axônio transmite o impulso nervoso (indicado por uma seta vermelha) para as ramificações terminais do axônio. Uma seta vermelha na base indica o 'Sentido do impulso nervoso'.

Diagrama de um neurônio biológico
### Neurônio Artificial
#### $\Sigma$ :

Responsável por combinar os valores de entrada. Realiza uma soma das entradas ponderadas pelos pesos.

Diagrama de um neurônio artificial. Entradas  $x_1, x_2, \dots, x_p$  são conectadas a um somador  $\Sigma$  (dentro de um retângulo verde) através de pesos  $w_1, w_2, \dots, w_p$ . O resultado da soma é processado por uma função de ativação  $f(a)$  (representada por um gráfico de degrau em um cubo 3D), resultando na saída  $y$ .

McCulloch – Pitts (1943)

Diagrama de um neurônio artificial

{21}------------------------------------------------
### Neurônio Biológico
#### Axônio:

Prolongamento do neurônio, responsável pela condução de impulsos elétricos gerados pelo corpo celular até outro local mais distante, geralmente outros neurônios. Em um adulto pode ter até 1m.

Diagrama de um neurônio biológico. O corpo celular contém o núcleo e é rodeado por dendritos. Um longo axônio se estende do corpo celular, terminando em ramificações. Setas vermelhas indicam o sentido do impulso nervoso, que flui dos dendritos, através do corpo celular e ao longo do axônio. Fonte: <https://www.deeplearningbook.com.br/>

Diagrama de um neurônio biológico
### Neurônio Artificial

**Função de transferência (ou ativação):** Responsável pela modulação do sinal propagado., gera valores excitatórios (positivos) ou inibitórios (negativos).

Diagrama de um neurônio artificial. À esquerda, múltiplas entradas ( $x_1, x_2, \dots, x_p$ ) são conectadas a um somador ( $\Sigma$ ) através de pesos ( $w_1, w_2, \dots, w_p$ ). O resultado da soma é processado por uma função de transferência ( $f(a)$ ), representada por um gráfico de degrau no plano  $a-y$ . A saída final é  $y$ . Referência: McCulloch – Pitts (1943).

Diagrama de um neurônio artificial

{22}------------------------------------------------
### Neurônio Biológico
#### Axônio:

O contato entre a terminação de um axônio e o dendrito de outro neurônio é chamado de **Sinapse**.

As sinapses mediam as interações entre os neurônios, podendo ser excitatórias ou inibitórias.

Diagrama de dois neurônios biológicos. À esquerda, um neurônio com corpo celular rosa, núcleo escuro, dendritos rosas e um axônio longo cinza coberto por bainhas de mielina rosas. À direita, outro neurônio similar. O axônio do primeiro neurônio se conecta ao dendrito do segundo na região rotulada como 'Sinapse' em um oval verde. Linhas apontam para 'Bainha de mielina', 'Axônio', 'Corpo celular' e 'Dendrito' no segundo neurônio.

Diagrama de dois neurônios biológicos conectados por uma sinapse.

<!-- IMAGE_DESCRIPTION: datalab-893f3e40a8607bd256b676392d228f2a_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de dois neurônios biológicos conectados por uma sinapse.
<!-- /IMAGE_DESCRIPTION -->
#### Função de transferência (ou ativação):

Responsável pela modulação do sinal propagado., gera valores excitatórios (positivos) ou inibitórios (negativos).

{23}------------------------------------------------
### Neurônio Biológico
#### Axônio:

O contato entre a terminação de um axônio e o dendrito de outro neurônio é chamado de **Sinapse**.

As sinapses mediam as interações entre os neurônios, podendo ser excitatórias ou inibitórias.

Diagrama de um neurônio biológico. À esquerda, um neurônio com corpo celular rosa, núcleo escuro, dendritos ramificados e um axônio longo coberto por bainha de mielina (segmentos rosas). À direita, outro neurônio similar. O ponto de contato entre o axônio do primeiro e os dendritos do segundo é destacado por um oval verde com o rótulo 'Sinapse'.

Diagrama de um neurônio biológico com rótulos: Dendrito, Corpo celular, Axônio, Bainha de mielina e Sinapse.

<!-- IMAGE_DESCRIPTION: datalab-78ebfe3116918cd317b54c861da8d8d2_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de um neurônio biológico com rótulos: Dendrito, Corpo celular, Axônio, Bainha de mielina e Sinapse.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-ca81500b365ed30190cb2d9c38fc1f84_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de um neurônio biológico com rótulos: Dendrito, Corpo celular, Axônio, Bainha de mielina e Sinapse.
<!-- /IMAGE_DESCRIPTION -->
#### Função de transferência (ou ativação):

Responsável pela modulação do sinal propagado., gera valores excitatórios (positivos) ou inibitórios (negativos).

Se o neurônio estiver em uma camada de saída da rede, o sinal gerado corresponde a saída da rede.

Diagrama de uma rede neural artificial. À esquerda, dois círculos verdes representam a camada de entrada com setas apontando para eles. No centro, uma camada oculta com cinco círculos azuis. À direita, um único círculo amarelo representa a camada de saída com uma seta apontando para fora dele. Linhas conectam todos os círculos de uma camada aos da seguinte.

Diagrama de uma rede neural artificial com camadas de entrada, oculta e saída.

{24}------------------------------------------------

Como é a propagação de  
um sinal em um neurônio  
em uma rede artificial?

A stylized illustration of a neural network. It features several glowing, yellowish-orange circular nodes (representing neurons) connected by thick, wavy, translucent lines (representing synapses or weights). The background is a dark, deep red color, and the overall aesthetic is futuristic and digital.

Illustration of a neural network with glowing nodes and connections.

{25}------------------------------------------------

Dado um neurônio artificial **j**:

The diagram illustrates the structure of an artificial neuron **j**. On the left, there are  $n$  input nodes labeled  $x_1, x_2, x_3, \dots, x_n$ . Each input node is connected to a corresponding weight node labeled  $w_{1j}, w_{2j}, w_{3j}, \dots, w_{nj}$ . The weights are collectively labeled "Pesos". All weight nodes are connected to a central summation node, represented by a circle containing the symbol  $\Sigma$ . The output of the summation node is connected to a square box labeled  $f$ , which represents the "Função de Ativação" (Activation Function). The output of this box is labeled "Saida" (Output). A bias term, represented by a small dot, is also shown as an input to the activation function box.

Diagram of an artificial neuron j showing inputs x1 to xn, weights w1j to wnj, a summation node $\Sigma$, an activation function f, and output Saida.

{26}------------------------------------------------

Dado um neurônio artificial  $j$ :

The diagram illustrates the structure of an artificial neuron  $j$ . On the left, there are  $n$  input nodes labeled  $x_1, x_2, x_3, \dots, x_n$ . Each input node is connected to a corresponding weight node labeled  $w_{1j}, w_{2j}, w_{3j}, \dots, w_{nj}$  by a red arrow. The weight nodes are connected to a central summation node labeled  $\Sigma$  by black arrows. The word "Pesos" (Weights) is written above the summation node. The summation node is connected to a square box labeled  $f$  (the activation function) by a black arrow. Below the box is the text "Função de Ativação" (Activation Function). The output of the box is labeled "Saida" (Output) by a black arrow.

Diagram of an artificial neuron j showing inputs x1 to xn, weights w1j to wnj, a summation node $\Sigma$, an activation function f, and output Saida.

Recebendo os dados de entrada  $X$

{27}------------------------------------------------

Dado um neurônio artificial  $j$ :

The diagram illustrates the structure of an artificial neuron  $j$ . On the left, multiple input nodes  $x_1, x_2, x_3, \dots, x_n$  are shown. Each input  $x_i$  is connected to a corresponding weight node  $W_{ij}$  (labeled  $W_{1j}, W_{2j}, W_{3j}, \dots, W_{nj}$ ). These weight nodes are then connected to a central summation node, represented by a circle containing the symbol  $\Sigma$ . The label "Pesos" is positioned near this summation node. The output of the summation node is passed to a square block labeled  $f$ , which represents the activation function. Below this block, the text "Função de Ativação" is present. The final output of the neuron is labeled "Saida" (Output).

Diagram of an artificial neuron j. Inputs x1, x2, x3, ..., xn are connected to weights W1j, W2j, W3j, ..., Wnj respectively. These weights are then summed ($\Sigma$) and the result is passed through an activation function f to produce the output 'Saida'. The label 'Pesos' is placed near the summation node.

Ponderando as entradas  $X$  pelos pesos  $W$ :  $x_i * w_{ij}$

{28}------------------------------------------------

Dado um neurônio artificial j:

The diagram illustrates the structure of an artificial neuron. On the left, inputs  $x_1, x_2, x_3, \dots, x_n$  are shown. Each input is connected to a corresponding weight  $w_{1j}, w_{2j}, w_{3j}, \dots, w_{nj}$ . These weights are then connected to a central summation node, represented by a red circle with the symbol  $\Sigma$ . The word "Pesos" (Weights) is written near the weights. The output of the summation node is a red arrow pointing to a square block labeled  $f$ , which represents the activation function. Below this block is the label "Função de Ativação" (Activation Function). The output of the activation function is a black arrow pointing to the right, labeled "Saida" (Output).

Diagram of an artificial neuron j. Inputs x1, x2, x3, ..., xn are connected to weights w1j, w2j, w3j, ..., wnj. The weighted inputs are summed in a red circle labeled $\Sigma$. The sum is then passed to an activation function block labeled f, which produces the output 'Saida'. The label 'Pesos' is placed near the weights, and 'Função de Ativação' is placed below the activation function block.

Combinando os sinais:  $soma = x_1 * w_{1j} + x_2 * w_{2j} + x_3 * w_{3j} + \dots x_n * w_{nj}$

{29}------------------------------------------------

Dado um neurônio artificial  $j$ :

The diagram illustrates the structure of an artificial neuron  $j$ . On the left, inputs  $x_1, x_2, x_3, \dots, x_n$  are shown. Each input is connected to a corresponding weight  $w_{1j}, w_{2j}, w_{3j}, \dots, w_{nj}$ . The weights are grouped by the label "Pesos". The weighted inputs are then summed in a circle containing the symbol  $\Sigma$ . The output of the summation is passed to a red square block labeled  $f$ , which represents the activation function. This block is labeled "Função de Ativação". The final output is labeled "Saida".

Diagram of an artificial neuron j. Inputs x1, x2, x3, ..., xn are connected to weights w1j, w2j, w3j, ..., wnj. The weighted inputs are summed in a circle with the symbol $\Sigma$. The sum is then passed to a red square block labeled f, which represents the activation function. The output is labeled 'Saida'. The label 'Pesos' is placed near the weights, and 'Função de Ativação' is placed below the activation function block.

Gerando o sinal de saída:  $y_1 = f(\text{soma})$

<!-- IMAGE_DESCRIPTION: datalab-32a03202e95ff09a974e12e4be687885_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A stylized, glowing blue brain composed of interconnected nodes and lines, representing a neural network structure, set against a dark blue background with faint numerical data.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-349ca0a6a9c2e2651a4deeeaf8be6da1_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A stylized, glowing blue brain composed of a dense network of nodes and connecting lines, set against a dark blue background with faint, scattered numbers and grid lines, suggesting a digital or artificial neural...
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-662933fe00899933b36b5a214ac6095c_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A stylized illustration of a neural network with glowing yellow nodes and orange connections.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-19a5f0db57a21a0e82a7f326083e96fd_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de uma rede neural artificial com camadas de entrada, oculta e saída.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-71dea59c7a8cc6669fcce714dca70021_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Illustration of a neural network with glowing nodes and connections.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-0c08e48c08f96934cd6bc6911f3069dc_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of an artificial neuron j showing inputs x1 to xn, weights w1j to wnj, a summation node Σ, an activation function f, and output Saida.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-043e64d41a3368d138ace3816fd26469_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of an artificial neuron j showing inputs x1 to xn, weights w1j to wnj, a summation node Σ, an activation function f, and output Saida.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-d17aa1fcc3b86503ad1dd0717a6c34c2_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of an artificial neuron j. Inputs x1, x2, x3, ..., xn are connected to weights W1j, W2j, W3j, ..., Wnj respectively. These weights are then summed (Σ) and the result is passed through an activation function f...
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-2bacc162a73d75c43a7f90715832bd13_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of an artificial neuron j. Inputs x1, x2, x3, ..., xn are connected to weights w1j, w2j, w3j, ..., wnj. The weighted inputs are summed in a red circle labeled Σ. The sum is then passed to an activation function...
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-5414f65867392f05ba0063b208eeb5e1_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of an artificial neuron j. Inputs x1, x2, x3, ..., xn are connected to weights w1j, w2j, w3j, ..., wnj. The weighted inputs are summed in a circle with the symbol Σ. The sum is then passed to a red square block...
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION_ORPHANS -->
## Imagens Curadas

Descrições preservadas para imagens detectadas no documento, mas sem referência markdown compatível no corpo principal.

<!-- IMAGE_DESCRIPTION: datalab-8e592c58b5074d79831ff650c2c636df_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A 3D rendering of a human brain split vertically.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-a0167e3dcece9dcd8a378bcd98fb9cfa_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A 3D rendering of a human brain split vertically.
<!-- /IMAGE_DESCRIPTION -->
<!-- /IMAGE_DESCRIPTION_ORPHANS -->
